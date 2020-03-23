---
title: POS と新しいハードウェア デバイスの統合
description: このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 7.3.0, Retail July 2017 update
ms.openlocfilehash: d9252e4771bd6292407e8f9c2491f4eb3bbe718a
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117255"
---
# <a name="integrate-pos-with-a-new-hardware-device"></a><span data-ttu-id="c8283-103">POS と新しいハードウェア デバイスの統合</span><span class="sxs-lookup"><span data-stu-id="c8283-103">Integrate POS with a new hardware device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8283-104">このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c8283-104">This topic explains how to integrate POS with a new hardware device.</span></span> 


<span data-ttu-id="c8283-105">POS からハードウェア ステーションを呼び出すには、要求と応答を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-105">To call Hardware station from POS you need to use a request and a response:</span></span>

+ <span data-ttu-id="c8283-106">**HardwareStationDeviceActionRequest** - POS からハードウェア ステーションに送信された要求。</span><span class="sxs-lookup"><span data-stu-id="c8283-106">**HardwareStationDeviceActionRequest** - Request sent from POS to Hardware station.</span></span>
+ <span data-ttu-id="c8283-107">**HardwareStationDeviceActionResponse** - ハードウェア ステーションから POS に受信した要求。</span><span class="sxs-lookup"><span data-stu-id="c8283-107">**HardwareStationDeviceActionResponse** - Response received from Hardware station to POS.</span></span>

## <a name="hardwarestationdeviceactionrequest"></a><span data-ttu-id="c8283-108">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="c8283-108">HardwareStationDeviceActionRequest</span></span>

<span data-ttu-id="c8283-109">**HardwareStationDeviceActionRequest** の定義を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="c8283-109">The definition of **HardwareStationDeviceActionRequest** is shown in the following code example.</span></span>

```TypeScript
class HardwareStationDeviceActionRequest<TResponse extends HardwareStationDeviceActionResponse> extends Request<TResponse> {

  readonly device: string;
  readonly action: string;
  readonly actionData: any;
  constructor(device: string, action: string, actionData: any, correlationId?: string);

}
```

<span data-ttu-id="c8283-110">次の表で、このパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c8283-110">The parameters are described in the following table.</span></span>

| <span data-ttu-id="c8283-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c8283-111">Parameters</span></span> | <span data-ttu-id="c8283-112">データ型</span><span class="sxs-lookup"><span data-stu-id="c8283-112">Data type</span></span> | <span data-ttu-id="c8283-113">説明</span><span class="sxs-lookup"><span data-stu-id="c8283-113">Description</span></span>                     |
|------------|-----------|---------------------------------|
| <span data-ttu-id="c8283-114">デバイス</span><span class="sxs-lookup"><span data-stu-id="c8283-114">device</span></span>     | <span data-ttu-id="c8283-115">文字列</span><span class="sxs-lookup"><span data-stu-id="c8283-115">String</span></span>    | <span data-ttu-id="c8283-116">ハードウェア ステーションの要求に渡されるデバイス名は、ハードウェア ステーションのデバイス拡張コントローラー クラスに追加された**エクスポート**属性と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-116">Device name passed to the Hardware station request should be the same as the **Export** attribute added in the Hardware station Device extension controller class.</span></span>                                          |
| <span data-ttu-id="c8283-117">アクション</span><span class="sxs-lookup"><span data-stu-id="c8283-117">action</span></span>     | <span data-ttu-id="c8283-118">文字列</span><span class="sxs-lookup"><span data-stu-id="c8283-118">String</span></span>    | <span data-ttu-id="c8283-119">ハードウェア ステーション拡張機能で呼び出すメソッド。</span><span class="sxs-lookup"><span data-stu-id="c8283-119">Method to be called in the Hardware station extension.</span></span> <span data-ttu-id="c8283-120">メソッド名は文字列値として渡され、コア POS ハードウェア ステーション層は、ハードウェア ステーション拡張コードから対応するメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8283-120">The method name should be passed as string value and the core POS hardware station layer will call the corresponding method from your Hardware station extension code.</span></span> <span data-ttu-id="c8283-121">このメソッドは、ハードウェア ステーション拡張機能のメソッド名と完全に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-121">The method should exactly match the method name in your Hardware station extension.</span></span> <span data-ttu-id="c8283-122">ハードウェア ステーション拡張機能は、パラメーターとして渡される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-122">The Hardware station extension should be passed as parameter.</span></span> |
| <span data-ttu-id="c8283-123">actionData</span><span class="sxs-lookup"><span data-stu-id="c8283-123">actionData</span></span> | <span data-ttu-id="c8283-124">any</span><span class="sxs-lookup"><span data-stu-id="c8283-124">any</span></span>       | <span data-ttu-id="c8283-125">拡張機能に渡すカスタム パラメーター。</span><span class="sxs-lookup"><span data-stu-id="c8283-125">Custom parameter for extension to pass.</span></span>  |

### <a name="sample-code"></a><span data-ttu-id="c8283-126">サンプル コード</span><span class="sxs-lookup"><span data-stu-id="c8283-126">Sample code</span></span>

<span data-ttu-id="c8283-127">次のコード例では、**HardwareStationDeviceActionRequest** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="c8283-127">The following code examples creates a **HardwareStationDeviceActionRequest** object.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("Export attribute in Hardware station controller class",
    "extension method name in Hardware station", "Custom parameters/you can also pass custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="hardwarestationdeviceactionresponse"></a><span data-ttu-id="c8283-128">HardwareStationDeviceActionResponse</span><span class="sxs-lookup"><span data-stu-id="c8283-128">HardwareStationDeviceActionResponse</span></span>

<span data-ttu-id="c8283-129">**HardwareStationDeviceActionResponse** の定義を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="c8283-129">The definition of **HardwareStationDeviceActionResponse** is shown in the following code example.</span></span>

```TypeScript
class HardwareStationDeviceActionResponse extends Response {
  readonly response: any;
  constructor(response: any);
}
```
<span data-ttu-id="c8283-130">次の表で、このパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c8283-130">The parameters are described in the following table.</span></span>

| <span data-ttu-id="c8283-131">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c8283-131">Parameters</span></span> | <span data-ttu-id="c8283-132">データ型</span><span class="sxs-lookup"><span data-stu-id="c8283-132">Data type</span></span> | <span data-ttu-id="c8283-133">説明</span><span class="sxs-lookup"><span data-stu-id="c8283-133">Description</span></span>                                       |
|------------|-----------|---------------------------------------------------|
| <span data-ttu-id="c8283-134">応答</span><span class="sxs-lookup"><span data-stu-id="c8283-134">response</span></span>   | <span data-ttu-id="c8283-135">any</span><span class="sxs-lookup"><span data-stu-id="c8283-135">any</span></span>       | <span data-ttu-id="c8283-136">ハードウェア ステーション拡張コードから POS に送信された応答。</span><span class="sxs-lookup"><span data-stu-id="c8283-136">Response sent from the Hardware station extension code to POS.</span></span> |

## <a name="end-to-end-flow"></a><span data-ttu-id="c8283-137">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="c8283-137">End-to-end flow</span></span>

<span data-ttu-id="c8283-138">次の図は、POS、ハードウェア ステーション、ハードウェア デバイスのフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="c8283-138">The follow diagram shows the flow between POS, Hardware station, and the hardware device.</span></span>

![POS-HWS デバイス シーケンス図](./media/POSDeviceExtension.png)

## <a name="hardware-station-extension"></a><span data-ttu-id="c8283-140">ハードウェア ステーション拡張機能</span><span class="sxs-lookup"><span data-stu-id="c8283-140">Hardware station extension</span></span>

<span data-ttu-id="c8283-141">新しいハードウェア デバイスを呼び出すには、ハードウェア ステーション コードを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-141">To call your new hardware device, you must implement the Hardware station code.</span></span> <span data-ttu-id="c8283-142">ハードウェア ステーション コードから、ハードウェア デバイスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8283-142">From the Hardware station code, call your hardware device.</span></span>

<span data-ttu-id="c8283-143">ハードウェア ステーション拡張機能を実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="c8283-143">To implement the Hardware station extension, follow these steps:</span></span>

1.  <span data-ttu-id="c8283-144">新しい C# クラス ライブラリ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="c8283-144">Create a new C# class library project.</span></span>
2.  <span data-ttu-id="c8283-145">**HardwareStationController** と **IHardwareStationController** を拡張する新しいコントローラー クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="c8283-145">Add a new controller class that extends **HardwareStationController** and **IHardwareStationController**.</span></span>
3.  <span data-ttu-id="c8283-146">コントローラー クラスに**エクスポート**属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="c8283-146">Add the **Export** attribute to the controller class.</span></span> <span data-ttu-id="c8283-147">**エクスポート**属性は、すべて大文字で指定する必要があります。また、この値は POS 拡張機能のパラメーターとして渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-147">The **Export** attribute must be in all uppercase letters and you must pass this value as a parameter from POS extension.</span></span> <span data-ttu-id="c8283-148">POS **HardwareStationDeviceActionRequest** から渡されたデバイス パラメーターは、この値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c8283-148">The device parameter passed from the POS **HardwareStationDeviceActionRequest** must match this value.</span></span>
4.  <span data-ttu-id="c8283-149">このメソッドをコントローラー クラスに追加して、ハードウェア デバイスを呼び出すカスタム ロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="c8283-149">Add your method in controller class to implement your custom logic to call the hardware device.</span></span> <span data-ttu-id="c8283-150">このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。</span><span class="sxs-lookup"><span data-stu-id="c8283-150">This method will be passed as the second parameter (action parameter) to the POS **HardwareStationDeviceActionRequest**.</span></span>
5.  <span data-ttu-id="c8283-151">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="c8283-151">Build the project.</span></span>

<span data-ttu-id="c8283-152">MPOS にハードウェア ステーション拡張機能を展開し、ローカル ハードウェア ステーションを使用してテストするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c8283-152">To deploy the Hardware station extension in MPOS and test it using the local Hardware station:</span></span>

1. <span data-ttu-id="c8283-153">出力ライブラリを **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="c8283-153">Copy the output library to the **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span>
2. <span data-ttu-id="c8283-154">**HardwareStation.Extension.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="c8283-154">Open the **HardwareStation.Extension.config**.</span></span>
3. <span data-ttu-id="c8283-155">合成セクションに拡張ライブラリの詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="c8283-155">Add the extension library details under the composition section.</span></span>

  ```Xml
  <add source="assembly" value="your extension library name" />
  ```
 
4. <span data-ttu-id="c8283-156">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="c8283-156">Save the file.</span></span>
5. <span data-ttu-id="c8283-157">モダン POS を閉じます (実行中の場合)。</span><span class="sxs-lookup"><span data-stu-id="c8283-157">Close Modern POS if running.</span></span>
6. <span data-ttu-id="c8283-158">タスク マネージャーを開いて、**dllhost.exe** タスクを終了します。</span><span class="sxs-lookup"><span data-stu-id="c8283-158">Open Task Manager and end the **dllhost.exe** task.</span></span>
7. <span data-ttu-id="c8283-159">MPOS を起動して、ローカル ハードウェア ステーションを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="c8283-159">Launch MPOS and configure it to use local hardware station.</span></span>
8. <span data-ttu-id="c8283-160">シナリオを検証します。</span><span class="sxs-lookup"><span data-stu-id="c8283-160">Validate your scenario.</span></span>

<span data-ttu-id="c8283-161">クラウド POS を使用してテストするには、共有ハードウェア ステーションの **ext** フォルダーにハードウェア ステーション拡張 dll を配置し、共有ハードウェア ステーション フォルダーのカスタム ライブラリを使用して **HardwareStation.Extension.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="c8283-161">To test with Cloud POS, deploy the Hardware station extension dll to the shared Hardware station **ext** folder and update the **HardwareStation.Extension.config** file with the custom library in the shared Hardware station folder.</span></span>

## <a name="retail-sdk-samples"></a><span data-ttu-id="c8283-162">Retail SDK サンプル</span><span class="sxs-lookup"><span data-stu-id="c8283-162">Retail SDK samples</span></span>
<span data-ttu-id="c8283-163">次に、参照用の Retail SDK のサンプルをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="c8283-163">Here are some samples in the Retail SDK for reference:</span></span>

+ <span data-ttu-id="c8283-164">**POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="c8283-164">**POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample</span></span>
+ <span data-ttu-id="c8283-165">**ハードウェア ステーション**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="c8283-165">**Hardware station**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample</span></span>

## <a name="sample-hardware-station-code"></a><span data-ttu-id="c8283-166">ハードウェア ステーション コードのサンプル</span><span class="sxs-lookup"><span data-stu-id="c8283-166">Sample Hardware station code</span></span>

```C#
namespace Contoso
{
  namespace Commerce.HardwareStation.ISVExtensionDevice
  {

  using System;
  using System.Composition;
  using System.Web.Http;
  using Microsoft.Dynamics.Commerce.HardwareStation;
  /// <summary>;
  /// Fiscal register peripheral web API controller class.
  /// </summary>

  [Export("ISVEXTENSIONDEVICE", typeof(IHardwareStationController))]
  [Authorize]
  public class ISVExtensionDeviceController : HardwareStationController, IHardwareStationController
  {
  /// <summary>
  /// Sample.
  /// </summary>

  /// <param name="request">Custom request.<param>
  /// <returns>Result of Custom response.</returns>

      [HttpPost]
      public CustomResponse Sample(CustomRequest request)
      {
        ThrowIf.Null(request, "request");
        try
        {
          return null;
        }

        catch (Exception ex)
          {
            throw ex;
          }
      }
   }
   }
 }

```

## <a name="sample-pos-code-on-how-to-call-the-above-hardware-station-extension"></a><span data-ttu-id="c8283-167">上記のハードウェア ステーション拡張機能の呼び出し方法に関するサンプル POS コード</span><span class="sxs-lookup"><span data-stu-id="c8283-167">Sample POS code on how to call the above Hardware station extension</span></span>

<span data-ttu-id="c8283-168">POS 拡張機能から、このパターンを使用してハードウェア ステーションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c8283-168">From your POS extension, call the Hardware station by using this pattern.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("ISVEXTENSIONDEVICE",
     "Sample", "Custom parameters or custom object");
 return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
 ```

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
ms.openlocfilehash: dc143666855fb860da67d331225c83cee2e166c1
ms.sourcegitcommit: a2e562d2871623dbc584d4fc747ee138bd1f674d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/09/2019
ms.locfileid: "1870199"
---
# <a name="integrate-pos-with-a-new-hardware-device"></a><span data-ttu-id="97965-103">POS と新しいハードウェア デバイスの統合</span><span class="sxs-lookup"><span data-stu-id="97965-103">Integrate POS with a new hardware device</span></span>

<span data-ttu-id="97965-104">このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="97965-104">This topic explains how to integrate POS with a new hardware device.</span></span> <span data-ttu-id="97965-105">このトピックの情報は Dynamics 365 for Finance and Operations と Dynamics 365 for Retail プラットフォーム アップデート 8 のみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="97965-105">The information in this topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail platform update 8.</span></span>

<span data-ttu-id="97965-106">POS からハードウェア ステーションを呼び出すには、要求と応答を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-106">To call Hardware station from POS you need to use a request and a response:</span></span>

+ <span data-ttu-id="97965-107">**HardwareStationDeviceActionRequest** - POS からハードウェア ステーションに送信された要求。</span><span class="sxs-lookup"><span data-stu-id="97965-107">**HardwareStationDeviceActionRequest** - Request sent from POS to Hardware station.</span></span>
+ <span data-ttu-id="97965-108">**HardwareStationDeviceActionResponse** - ハードウェア ステーションから POS に受信した要求。</span><span class="sxs-lookup"><span data-stu-id="97965-108">**HardwareStationDeviceActionResponse** - Response received from Hardware station to POS.</span></span>

## <a name="hardwarestationdeviceactionrequest"></a><span data-ttu-id="97965-109">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="97965-109">HardwareStationDeviceActionRequest</span></span>

<span data-ttu-id="97965-110">**HardwareStationDeviceActionRequest** の定義を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="97965-110">The definition of **HardwareStationDeviceActionRequest** is shown in the following code example.</span></span>

```TypeScript
class HardwareStationDeviceActionRequest<TResponse extends HardwareStationDeviceActionResponse> extends Request<TResponse> {

  readonly device: string;
  readonly action: string;
  readonly actionData: any;
  constructor(device: string, action: string, actionData: any, correlationId?: string);

}
```

<span data-ttu-id="97965-111">次の表で、このパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="97965-111">The parameters are described in the following table.</span></span>

| <span data-ttu-id="97965-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97965-112">Parameters</span></span> | <span data-ttu-id="97965-113">データ型</span><span class="sxs-lookup"><span data-stu-id="97965-113">Data type</span></span> | <span data-ttu-id="97965-114">説明</span><span class="sxs-lookup"><span data-stu-id="97965-114">Description</span></span>                     |
|------------|-----------|---------------------------------|
| <span data-ttu-id="97965-115">デバイス</span><span class="sxs-lookup"><span data-stu-id="97965-115">device</span></span>     | <span data-ttu-id="97965-116">文字列</span><span class="sxs-lookup"><span data-stu-id="97965-116">String</span></span>    | <span data-ttu-id="97965-117">ハードウェア ステーションの要求に渡されるデバイス名は、ハードウェア ステーションのデバイス拡張コントローラー クラスに追加された**エクスポート**属性と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-117">Device name passed to the Hardware station request should be the same as the **Export** attribute added in the Hardware station Device extension controller class.</span></span>                                          |
| <span data-ttu-id="97965-118">アクション</span><span class="sxs-lookup"><span data-stu-id="97965-118">action</span></span>     | <span data-ttu-id="97965-119">文字列</span><span class="sxs-lookup"><span data-stu-id="97965-119">String</span></span>    | <span data-ttu-id="97965-120">ハードウェア ステーション拡張機能で呼び出すメソッド。</span><span class="sxs-lookup"><span data-stu-id="97965-120">Method to be called in the Hardware station extension.</span></span> <span data-ttu-id="97965-121">メソッド名は文字列値として渡され、コア POS ハードウェア ステーション層は、ハードウェア ステーション拡張コードから対応するメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="97965-121">The method name should be passed as string value and the core POS hardware station layer will call the corresponding method from your Hardware station extension code.</span></span> <span data-ttu-id="97965-122">このメソッドは、ハードウェア ステーション拡張機能のメソッド名と完全に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-122">The method should exactly match the method name in your Hardware station extension.</span></span> <span data-ttu-id="97965-123">ハードウェア ステーション拡張機能は、パラメーターとして渡される必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-123">The Hardware station extension should be passed as parameter.</span></span> |
| <span data-ttu-id="97965-124">actionData</span><span class="sxs-lookup"><span data-stu-id="97965-124">actionData</span></span> | <span data-ttu-id="97965-125">any</span><span class="sxs-lookup"><span data-stu-id="97965-125">any</span></span>       | <span data-ttu-id="97965-126">拡張機能に渡すカスタム パラメーター。</span><span class="sxs-lookup"><span data-stu-id="97965-126">Custom parameter for extension to pass.</span></span>  |

### <a name="sample-code"></a><span data-ttu-id="97965-127">サンプル コード</span><span class="sxs-lookup"><span data-stu-id="97965-127">Sample code</span></span>

<span data-ttu-id="97965-128">次のコード例では、**HardwareStationDeviceActionRequest** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="97965-128">The following code examples creates a **HardwareStationDeviceActionRequest** object.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("Export attribute in Hardware station controller class",
    "extension method name in Hardware station", "Custom parameters/you can also pass custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="hardwarestationdeviceactionresponse"></a><span data-ttu-id="97965-129">HardwareStationDeviceActionResponse</span><span class="sxs-lookup"><span data-stu-id="97965-129">HardwareStationDeviceActionResponse</span></span>

<span data-ttu-id="97965-130">**HardwareStationDeviceActionResponse** の定義を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="97965-130">The definition of **HardwareStationDeviceActionResponse** is shown in the following code example.</span></span>

```TypeScript
class HardwareStationDeviceActionResponse extends Response {
  readonly response: any;
  constructor(response: any);
}
```
<span data-ttu-id="97965-131">次の表で、このパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="97965-131">The parameters are described in the following table.</span></span>

| <span data-ttu-id="97965-132">パラメーター</span><span class="sxs-lookup"><span data-stu-id="97965-132">Parameters</span></span> | <span data-ttu-id="97965-133">データ型</span><span class="sxs-lookup"><span data-stu-id="97965-133">Data type</span></span> | <span data-ttu-id="97965-134">説明</span><span class="sxs-lookup"><span data-stu-id="97965-134">Description</span></span>                                       |
|------------|-----------|---------------------------------------------------|
| <span data-ttu-id="97965-135">応答</span><span class="sxs-lookup"><span data-stu-id="97965-135">response</span></span>   | <span data-ttu-id="97965-136">any</span><span class="sxs-lookup"><span data-stu-id="97965-136">any</span></span>       | <span data-ttu-id="97965-137">ハードウェア ステーション拡張コードから POS に送信された応答。</span><span class="sxs-lookup"><span data-stu-id="97965-137">Response sent from the Hardware station extension code to POS.</span></span> |

## <a name="end-to-end-flow"></a><span data-ttu-id="97965-138">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="97965-138">End-to-end flow</span></span>

<span data-ttu-id="97965-139">次の図は、POS、ハードウェア ステーション、ハードウェア デバイスのフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="97965-139">The follow diagram shows the flow between POS, Hardware station, and the hardware device.</span></span>

![POS-HWS デバイス シーケンス図](./media/POSDeviceExtension.png)

## <a name="hardware-station-extension"></a><span data-ttu-id="97965-141">ハードウェア ステーション拡張機能</span><span class="sxs-lookup"><span data-stu-id="97965-141">Hardware station extension</span></span>

<span data-ttu-id="97965-142">新しいハードウェア デバイスを呼び出すには、ハードウェア ステーション コードを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-142">To call your new hardware device, you must implement the Hardware station code.</span></span> <span data-ttu-id="97965-143">ハードウェア ステーション コードから、ハードウェア デバイスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="97965-143">From the Hardware station code, call your hardware device.</span></span>

<span data-ttu-id="97965-144">ハードウェア ステーション拡張機能を実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="97965-144">To implement the Hardware station extension, follow these steps:</span></span>

1.  <span data-ttu-id="97965-145">新しい C# クラス ライブラリ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="97965-145">Create a new C# class library project.</span></span>
2.  <span data-ttu-id="97965-146">**HardwareStationController** と **IHardwareStationController** を拡張する新しいコントローラー クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="97965-146">Add a new controller class that extends **HardwareStationController** and **IHardwareStationController**.</span></span>
3.  <span data-ttu-id="97965-147">コントローラー クラスに**エクスポート**属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="97965-147">Add the **Export** attribute to the controller class.</span></span> <span data-ttu-id="97965-148">**エクスポート**属性は、すべて大文字で指定する必要があります。また、この値は POS 拡張機能のパラメーターとして渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-148">The **Export** attribute must be in all uppercase letters and you must pass this value as a parameter from POS extension.</span></span> <span data-ttu-id="97965-149">POS **HardwareStationDeviceActionRequest** から渡されたデバイス パラメーターは、この値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="97965-149">The device parameter passed from the POS **HardwareStationDeviceActionRequest** must match this value.</span></span>
4.  <span data-ttu-id="97965-150">このメソッドをコントローラー クラスに追加して、ハードウェア デバイスを呼び出すカスタム ロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="97965-150">Add your method in controller class to implement your custom logic to call the hardware device.</span></span> <span data-ttu-id="97965-151">このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。</span><span class="sxs-lookup"><span data-stu-id="97965-151">This method will be passed as the second parameter (action parameter) to the POS **HardwareStationDeviceActionRequest**.</span></span>
5.  <span data-ttu-id="97965-152">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="97965-152">Build the project.</span></span>

<span data-ttu-id="97965-153">MPOS にハードウェア ステーション拡張機能を展開し、ローカル ハードウェア ステーションを使用してテストするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="97965-153">To deploy the Hardware station extension in MPOS and test it using the local Hardware station:</span></span>

1. <span data-ttu-id="97965-154">出力ライブラリを **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="97965-154">Copy the output library to the **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span>
2. <span data-ttu-id="97965-155">**HardwareStation.Extension.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="97965-155">Open the **HardwareStation.Extension.config**.</span></span>
3. <span data-ttu-id="97965-156">合成セクションに拡張ライブラリの詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="97965-156">Add the extension library details under the composition section.</span></span>

  ```Xml
  <add source="assembly" value="your extension library name" />
  ```
 
4. <span data-ttu-id="97965-157">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="97965-157">Save the file.</span></span>
5. <span data-ttu-id="97965-158">モダン POS を閉じます (実行中の場合)。</span><span class="sxs-lookup"><span data-stu-id="97965-158">Close Modern POS if running.</span></span>
6. <span data-ttu-id="97965-159">タスク マネージャーを開いて、**dllhost.exe** タスクを終了します。</span><span class="sxs-lookup"><span data-stu-id="97965-159">Open Task Manager and end the **dllhost.exe** task.</span></span>
7. <span data-ttu-id="97965-160">MPOS を起動して、ローカル ハードウェア ステーションを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="97965-160">Launch MPOS and configure it to use local hardware station.</span></span>
8. <span data-ttu-id="97965-161">シナリオを検証します。</span><span class="sxs-lookup"><span data-stu-id="97965-161">Validate your scenario.</span></span>

<span data-ttu-id="97965-162">クラウド POS を使用してテストするには、共有ハードウェア ステーションの **ext** フォルダーにハードウェア ステーション拡張 dll を配置し、共有ハードウェア ステーション フォルダーのカスタム ライブラリを使用して **HardwareStation.Extension.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="97965-162">To test with Cloud POS, deploy the Hardware station extension dll to the shared Hardware station **ext** folder and update the **HardwareStation.Extension.config** file with the custom library in the shared Hardware station folder.</span></span>

## <a name="retail-sdk-samples"></a><span data-ttu-id="97965-163">Retail SDK サンプル</span><span class="sxs-lookup"><span data-stu-id="97965-163">Retail SDK samples</span></span>
<span data-ttu-id="97965-164">次に、参照用の Retail SDK のサンプルをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="97965-164">Here are some samples in the Retail SDK for reference:</span></span>

+ <span data-ttu-id="97965-165">**POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="97965-165">**POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample</span></span>
+ <span data-ttu-id="97965-166">**ハードウェア ステーション**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="97965-166">**Hardware station**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample</span></span>

## <a name="sample-hardware-station-code"></a><span data-ttu-id="97965-167">ハードウェア ステーション コードのサンプル</span><span class="sxs-lookup"><span data-stu-id="97965-167">Sample Hardware station code</span></span>

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

## <a name="sample-pos-code-on-how-to-call-the-above-hardware-station-extension"></a><span data-ttu-id="97965-168">上記のハードウェア ステーション拡張機能の呼び出し方法に関するサンプル POS コード</span><span class="sxs-lookup"><span data-stu-id="97965-168">Sample POS code on how to call the above Hardware station extension</span></span>

<span data-ttu-id="97965-169">POS 拡張機能から、このパターンを使用してハードウェア ステーションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="97965-169">From your POS extension, call the Hardware station by using this pattern.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("ISVEXTENSIONDEVICE",
     "Sample", "Custom parameters or custom object");
 return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
 ```

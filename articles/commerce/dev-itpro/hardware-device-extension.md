---
title: POS と新しいハードウェア デバイスの統合
description: このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/27/2020
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
ms.dyn365.ops.version: AX 7.3.0, Retail July 2017 update, AX 10.0.11
ms.openlocfilehash: b0de86e48ee22b9051e0016397e89aa1171d6e16
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665042"
---
# <a name="integrate-pos-with-a-new-hardware-device"></a><span data-ttu-id="af143-103">POS と新しいハードウェア デバイスの統合</span><span class="sxs-lookup"><span data-stu-id="af143-103">Integrate POS with a new hardware device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af143-104">このトピックでは、新しいハードウェア デバイスに POS を統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="af143-104">This topic explains how to integrate POS with a new hardware device.</span></span> 

<span data-ttu-id="af143-105">POS からハードウェア ステーションを呼び出すには、要求と応答を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-105">To call Hardware station from POS you need to use a request and a response:</span></span>

+ <span data-ttu-id="af143-106">**HardwareStationDeviceActionRequest** - POS からハードウェア ステーションに送信された要求。</span><span class="sxs-lookup"><span data-stu-id="af143-106">**HardwareStationDeviceActionRequest** - Request sent from POS to Hardware station.</span></span>
+ <span data-ttu-id="af143-107">**HardwareStationDeviceActionResponse** - ハードウェア ステーションから POS に受信した要求。</span><span class="sxs-lookup"><span data-stu-id="af143-107">**HardwareStationDeviceActionResponse** - Response received from Hardware station to POS.</span></span>

<span data-ttu-id="af143-108">拡張するクラスは、使用している Retail SDK のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="af143-108">The class that you extend depends on which version of the Retail SDK you are using.</span></span>

+ <span data-ttu-id="af143-109">Retail SDK バージョン 10.0.11 以降では、**IController** インターフェイスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="af143-109">For Retail SDK version 10.0.11 or later, you extend the **IController** interface.</span></span>
+ <span data-ttu-id="af143-110">バージョン 10.0.11 以前の Retail SDKでは、**HardwareStationController** および **IHardwareStationController** のクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="af143-110">For Retail SDK prior to version 10.0.11, you extend the **HardwareStationController** and **IHardwareStationController** classes.</span></span>

## <a name="hardwarestationdeviceactionrequest"></a><span data-ttu-id="af143-111">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="af143-111">HardwareStationDeviceActionRequest</span></span>

<span data-ttu-id="af143-112">**HardwareStationDeviceActionRequest** の定義を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="af143-112">The definition of **HardwareStationDeviceActionRequest** is shown in the following code example.</span></span>

```TypeScript
class HardwareStationDeviceActionRequest<TResponse extends HardwareStationDeviceActionResponse> extends Request<TResponse> {

  readonly device: string;
  readonly action: string;
  readonly actionData: any;
  constructor(device: string, action: string, actionData: any, correlationId?: string);

}
```

<span data-ttu-id="af143-113">次の表で、このパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="af143-113">The parameters are described in the following table.</span></span>

| <span data-ttu-id="af143-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="af143-114">Parameters</span></span> | <span data-ttu-id="af143-115">データ型</span><span class="sxs-lookup"><span data-stu-id="af143-115">Data type</span></span> | <span data-ttu-id="af143-116">説明</span><span class="sxs-lookup"><span data-stu-id="af143-116">Description</span></span>                     |
|------------|-----------|---------------------------------|
| <span data-ttu-id="af143-117">デバイス</span><span class="sxs-lookup"><span data-stu-id="af143-117">device</span></span>     | <span data-ttu-id="af143-118">文字列</span><span class="sxs-lookup"><span data-stu-id="af143-118">String</span></span>    | <span data-ttu-id="af143-119">ハードウェア ステーションの要求に渡されるデバイス名は、ハードウェア ステーションのデバイス拡張コントローラー クラスに追加された**エクスポート**属性と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-119">Device name passed to the Hardware station request should be the same as the **Export** attribute added in the Hardware station Device extension controller class.</span></span>                                          |
| <span data-ttu-id="af143-120">アクション</span><span class="sxs-lookup"><span data-stu-id="af143-120">action</span></span>     | <span data-ttu-id="af143-121">文字列</span><span class="sxs-lookup"><span data-stu-id="af143-121">String</span></span>    | <span data-ttu-id="af143-122">ハードウェア ステーション拡張機能で呼び出すメソッド。</span><span class="sxs-lookup"><span data-stu-id="af143-122">Method to be called in the Hardware station extension.</span></span> <span data-ttu-id="af143-123">メソッド名は文字列値として渡され、コア POS ハードウェア ステーション層は、ハードウェア ステーション拡張コードから対応するメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="af143-123">The method name should be passed as string value and the core POS hardware station layer will call the corresponding method from your Hardware station extension code.</span></span> <span data-ttu-id="af143-124">このメソッドは、ハードウェア ステーション拡張機能のメソッド名と完全に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-124">The method should exactly match the method name in your Hardware station extension.</span></span> <span data-ttu-id="af143-125">ハードウェア ステーション拡張機能は、パラメーターとして渡される必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-125">The Hardware station extension should be passed as parameter.</span></span> |
| <span data-ttu-id="af143-126">actionData</span><span class="sxs-lookup"><span data-stu-id="af143-126">actionData</span></span> | <span data-ttu-id="af143-127">any</span><span class="sxs-lookup"><span data-stu-id="af143-127">any</span></span>       | <span data-ttu-id="af143-128">拡張機能に渡すカスタム パラメーター。</span><span class="sxs-lookup"><span data-stu-id="af143-128">Custom parameter for extension to pass.</span></span>  |

### <a name="sample-code"></a><span data-ttu-id="af143-129">サンプル コード</span><span class="sxs-lookup"><span data-stu-id="af143-129">Sample code</span></span>

<span data-ttu-id="af143-130">次のコード例では、**HardwareStationDeviceActionRequest** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="af143-130">The following code examples creates a **HardwareStationDeviceActionRequest** object.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("Export attribute in Hardware station controller class",
    "extension method name in Hardware station", "Custom parameters/you can also pass custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="hardwarestationdeviceactionresponse"></a><span data-ttu-id="af143-131">HardwareStationDeviceActionResponse</span><span class="sxs-lookup"><span data-stu-id="af143-131">HardwareStationDeviceActionResponse</span></span>

<span data-ttu-id="af143-132">**HardwareStationDeviceActionResponse** の定義を次のコード例に示します。</span><span class="sxs-lookup"><span data-stu-id="af143-132">The definition of **HardwareStationDeviceActionResponse** is shown in the following code example.</span></span>

```TypeScript
class HardwareStationDeviceActionResponse extends Response {
  readonly response: any;
  constructor(response: any);
}
```

<span data-ttu-id="af143-133">次の表で、このパラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="af143-133">The parameters are described in the following table.</span></span>

| <span data-ttu-id="af143-134">パラメーター</span><span class="sxs-lookup"><span data-stu-id="af143-134">Parameters</span></span> | <span data-ttu-id="af143-135">データ型</span><span class="sxs-lookup"><span data-stu-id="af143-135">Data type</span></span> | <span data-ttu-id="af143-136">説明</span><span class="sxs-lookup"><span data-stu-id="af143-136">Description</span></span>                                       |
|------------|-----------|---------------------------------------------------|
| <span data-ttu-id="af143-137">応答</span><span class="sxs-lookup"><span data-stu-id="af143-137">response</span></span>   | <span data-ttu-id="af143-138">any</span><span class="sxs-lookup"><span data-stu-id="af143-138">any</span></span>       | <span data-ttu-id="af143-139">ハードウェア ステーション拡張コードから POS に送信された応答。</span><span class="sxs-lookup"><span data-stu-id="af143-139">Response sent from the Hardware station extension code to POS.</span></span> |

## <a name="end-to-end-flow"></a><span data-ttu-id="af143-140">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="af143-140">End-to-end flow</span></span>

<span data-ttu-id="af143-141">次の図は、POS、ハードウェア ステーション、ハードウェア デバイスのフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="af143-141">The follow diagram shows the flow between POS, Hardware station, and the hardware device.</span></span>

![POS-HWS デバイス シーケンス図](./media/POSDeviceExtension.png)

## <a name="hardware-station-extension"></a><span data-ttu-id="af143-143">ハードウェア ステーション拡張機能</span><span class="sxs-lookup"><span data-stu-id="af143-143">Hardware station extension</span></span>

<span data-ttu-id="af143-144">新しいハードウェア デバイスを呼び出すには、ハードウェア ステーション コードを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-144">To call your new hardware device, you must implement the Hardware station code.</span></span> <span data-ttu-id="af143-145">ハードウェア ステーション コードから、ハードウェア デバイスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="af143-145">From the Hardware station code, call your hardware device.</span></span>

<span data-ttu-id="af143-146">Retail SDK バージョン10.0.11 以降の Hardware station 拡張機能を実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="af143-146">To implement the Hardware station extension for Retail SDK version 10.0.11 or later, follow these steps:</span></span>

1. <span data-ttu-id="af143-147">.NET Framework バージョン 4.6.1 を使用して新しい C# クラス ライブラリ プロジェクトを作成するか、または Retail SDK のサンプルのいずれかをテンプレート (**...\RetailSDK\SampleExtensions\HardwareStation\\**) として使用します。</span><span class="sxs-lookup"><span data-stu-id="af143-147">Create a new C# class library project with .NET Framework version 4.6.1 or use one of the samples in the Retail SDK as a template (**...\RetailSDK\SampleExtensions\HardwareStation\\**).</span></span> <span data-ttu-id="af143-148">このサンプルをテンプレートとして使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="af143-148">Using the sample as a template is recommended.</span></span>

2. <span data-ttu-id="af143-149">拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** を追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-149">In the extension project add the **Microsoft.Dynamics.Commerce.Hosting.Contracts** package using the NuGet package manager.</span></span> <span data-ttu-id="af143-150">NuGet パッケージは、**RetailSDK\pkgs** フォルダにあります。</span><span class="sxs-lookup"><span data-stu-id="af143-150">The NuGet packages can be found in the **RetailSDK\pkgs** folder.</span></span>

3. <span data-ttu-id="af143-151">**IController** インターフェイスを拡張する新しいコントローラ クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-151">Add a new controller class that extends the **IController** interface.</span></span>

4. <span data-ttu-id="af143-152">コントローラ クラスをクライアントに公開するには、コントローラ クラスに **RoutePrefix** 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-152">Add the **RoutePrefix** attribute to the controller class to expose the controller class to clients.</span></span>

    ```csharp
    [RoutePrefix("ISVEXTENSIONDEVICE")]  
    ```

5. <span data-ttu-id="af143-153">ハードウェア デバイスを呼び出すためのカスタム ロジックを実装するために、**HttpPost** 属性を持つメソッドをコントローラ クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-153">Add a method in the controller class with **HttpPost** attribute to implement your custom logic to call the hardware device.</span></span> <span data-ttu-id="af143-154">このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。</span><span class="sxs-lookup"><span data-stu-id="af143-154">This method will be passed as the second parameter (action parameter) to the POS **HardwareStationDeviceActionRequest**.</span></span> <span data-ttu-id="af143-155">拡張メソッドから、この拡張機能では、Retail SDK から関連する NuGet パッケージを含めることによって、印刷やキャッシュ ドロワーなどの他の要求を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="af143-155">From the extension method, the extension can call other requests, like printing and cash drawer, by including the relevant NuGet packages from the Retail SDK.</span></span>

    ```C#
    [HttpPost]
    public async Task<bool> IsReady(IEndpointContext context)
    {
    }
    ```

6.  <span data-ttu-id="af143-156">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="af143-156">Build the project.</span></span>

<span data-ttu-id="af143-157">Retail SDK バージョン 10.0.11 以前の Hardware station 拡張機能を実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="af143-157">To implement the Hardware station extension for Retail SDK prior to version 10.0.11, follow these steps:</span></span>

1.  <span data-ttu-id="af143-158">新しい C# クラス ライブラリ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="af143-158">Create a new C# class library project.</span></span>
2.  <span data-ttu-id="af143-159">**HardwareStationController** と **IHardwareStationController** を拡張する新しいコントローラー クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-159">Add a new controller class that extends **HardwareStationController** and **IHardwareStationController**.</span></span>
3.  <span data-ttu-id="af143-160">コントローラー クラスに**エクスポート**属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-160">Add the **Export** attribute to the controller class.</span></span> <span data-ttu-id="af143-161">**エクスポート**属性は、すべて大文字で指定する必要があります。また、この値は POS 拡張機能のパラメーターとして渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-161">The **Export** attribute must be in all uppercase letters and you must pass this value as a parameter from POS extension.</span></span> <span data-ttu-id="af143-162">POS **HardwareStationDeviceActionRequest** から渡されたデバイス パラメーターは、この値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="af143-162">The device parameter passed from the POS **HardwareStationDeviceActionRequest** must match this value.</span></span>
4.  <span data-ttu-id="af143-163">このメソッドをコントローラー クラスに追加して、ハードウェア デバイスを呼び出すカスタム ロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="af143-163">Add your method in controller class to implement your custom logic to call the hardware device.</span></span> <span data-ttu-id="af143-164">このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。</span><span class="sxs-lookup"><span data-stu-id="af143-164">This method will be passed as the second parameter (action parameter) to the POS **HardwareStationDeviceActionRequest**.</span></span>
5.  <span data-ttu-id="af143-165">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="af143-165">Build the project.</span></span>

<span data-ttu-id="af143-166">MPOS にハードウェア ステーション拡張機能を展開し、ローカル ハードウェア ステーションを使用してテストするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="af143-166">To deploy the Hardware station extension in MPOS and test it using the local Hardware station:</span></span>

1. <span data-ttu-id="af143-167">出力ライブラリを **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="af143-167">Copy the output library to the **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span>
2. <span data-ttu-id="af143-168">**HardwareStation.Extension.config** を開きます。</span><span class="sxs-lookup"><span data-stu-id="af143-168">Open the **HardwareStation.Extension.config**.</span></span>
3. <span data-ttu-id="af143-169">合成セクションに拡張ライブラリの詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="af143-169">Add the extension library details under the composition section.</span></span>

    ```Xml
    <add source="assembly" value="your extension library name" />
    ```
 
4. <span data-ttu-id="af143-170">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="af143-170">Save the file.</span></span>
5. <span data-ttu-id="af143-171">モダン POS を閉じます (実行中の場合)。</span><span class="sxs-lookup"><span data-stu-id="af143-171">Close Modern POS if running.</span></span>
6. <span data-ttu-id="af143-172">タスク マネージャーを開いて、**dllhost.exe** タスクを終了します。</span><span class="sxs-lookup"><span data-stu-id="af143-172">Open Task Manager and end the **dllhost.exe** task.</span></span>
7. <span data-ttu-id="af143-173">MPOS を起動して、ローカル ハードウェア ステーションを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="af143-173">Launch MPOS and configure it to use local hardware station.</span></span>
8. <span data-ttu-id="af143-174">シナリオを検証します。</span><span class="sxs-lookup"><span data-stu-id="af143-174">Validate your scenario.</span></span>

<span data-ttu-id="af143-175">クラウド POS を使用してテストするには、共有ハードウェア ステーションの **ext** フォルダーにハードウェア ステーション拡張 dll を配置し、共有ハードウェア ステーション フォルダーのカスタム ライブラリを使用して **HardwareStation.Extension.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="af143-175">To test with Cloud POS, deploy the Hardware station extension dll to the shared Hardware station **ext** folder and update the **HardwareStation.Extension.config** file with the custom library in the shared Hardware station folder.</span></span>

## <a name="retail-sdk-samples"></a><span data-ttu-id="af143-176">Retail SDK サンプル</span><span class="sxs-lookup"><span data-stu-id="af143-176">Retail SDK samples</span></span>
<span data-ttu-id="af143-177">次に、参照用の Retail SDK のサンプルをいくつか示します。</span><span class="sxs-lookup"><span data-stu-id="af143-177">Here are some samples in the Retail SDK for reference:</span></span>

+ <span data-ttu-id="af143-178">**POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="af143-178">**POS**: \RetailSDK\POS\Extensions\FiscalRegisterSample</span></span>
+ <span data-ttu-id="af143-179">**ハードウェア ステーション**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="af143-179">**Hardware station**: \RetailSDK\SampleExtensions\HardwareStation\Extension.FiscalRegisterSample</span></span>

## <a name="sample-code-for-retail-sdk-version-10011-or-later"></a><span data-ttu-id="af143-180">Retail SDK バージョン 10.0.11 以降のサンプル コード</span><span class="sxs-lookup"><span data-stu-id="af143-180">Sample code for Retail SDK version 10.0.11 or later</span></span>

```csharp
namespace Contoso
{
    namespace Commerce.HardwareStation.ISVExtensionDevice
    {

        using Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts;
        using System;
        using System.Threading.Tasks;

        /// <summary>;
        /// Sample hardware station extension
        /// </summary>

        [RoutePrefix("ISVEXTENSIONDEVICE")]
        public class ISVExtensionDeviceController : IController
        {
            /// <summary>
            /// Sample.
            /// </summary>

            /// <param name="request">Custom request.<param>
            /// <returns>Result of Custom response.</returns>

            [HttpPost]
            public async Task<CustomResponse> Sample(CustomRequest request, IEndpointContext context)
            {
                CustomResponse response;

                try
                {
                    response = new CustomResponse();
                }

                catch (Exception ex)
                {
                    throw ex;
                }
                return await Task.FromResult(response);
            }
        }

        public class CustomResponse
        {
            public string sampleProp { get; set; }

            public CustomResponse()
            {
                this.sampleProp = "sampleValue";
            }
        }
    }
}
```


## <a name="sample-code-for-retail-sdk-prior-to-version-10011"></a><span data-ttu-id="af143-181">Retail SDK バージョン 10.0.11 以前のサンプル コード</span><span class="sxs-lookup"><span data-stu-id="af143-181">Sample code for Retail SDK prior to version 10.0.11</span></span>

```csharp
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

## <a name="sample-pos-code-on-how-to-call-the-above-hardware-station-extension"></a><span data-ttu-id="af143-182">上記のハードウェア ステーション拡張機能の呼び出し方法に関するサンプル POS コード</span><span class="sxs-lookup"><span data-stu-id="af143-182">Sample POS code on how to call the above Hardware station extension</span></span>

<span data-ttu-id="af143-183">POS 拡張機能から、このパターンを使用してハードウェア ステーションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="af143-183">From your POS extension, call the Hardware station by using this pattern.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("ISVEXTENSIONDEVICE",
     "Sample", "Custom parameters or custom object");
 return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
 ```

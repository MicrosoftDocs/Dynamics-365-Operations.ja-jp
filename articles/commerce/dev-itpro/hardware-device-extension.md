---
title: POS と新しいハードウェア デバイスの統合
description: このトピックでは、新しいハードウェア デバイスに販売時点管理 (POS) を統合する方法について説明します。
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
ms.openlocfilehash: 8ca2e31e2fda26b3cdb664f3fd5e61ef6e79d3a4
ms.sourcegitcommit: 8adc65e26d78e229271eb427659a87ee5f371319
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814045"
---
# <a name="integrate-the-pos-with-a-new-hardware-device"></a><span data-ttu-id="109de-103">POS と新しいハードウェア デバイスの統合</span><span class="sxs-lookup"><span data-stu-id="109de-103">Integrate the POS with a new hardware device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="109de-104">このトピックでは、新しいハードウェア デバイスに販売時点管理 (POS) を統合する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="109de-104">This topic explains how to integrate the point of sale (POS) with a new hardware device.</span></span> 

<span data-ttu-id="109de-105">POS からハードウェア ステーションを呼び出すには、要求と応答を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-105">To call Hardware station from the POS, you must use a request and a response:</span></span>

+ <span data-ttu-id="109de-106">**HardwareStationDeviceActionRequest** – POS からハードウェア ステーションに送信される要求。</span><span class="sxs-lookup"><span data-stu-id="109de-106">**HardwareStationDeviceActionRequest** – The request that is sent from the POS to Hardware station.</span></span>
+ <span data-ttu-id="109de-107">**HardwareStationDeviceActionResponse** – ハードウェア ステーションから POS が受信した要求。</span><span class="sxs-lookup"><span data-stu-id="109de-107">**HardwareStationDeviceActionResponse** – The response that the POS receives from Hardware station.</span></span>

<span data-ttu-id="109de-108">拡張するクラスは、使用している Retail ソフトウェア開発キット (SDK) のバージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="109de-108">The class that you extend depends on the version of the Retail software development kit (SDK) that you're using.</span></span>

+ <span data-ttu-id="109de-109">Retail SDK バージョン 10.0.11 以降では、**IController** インターフェイスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="109de-109">For Retail SDK version 10.0.11 or later, you extend the **IController** interface.</span></span>
+ <span data-ttu-id="109de-110">バージョン 10.0.11 以前の Retail SDK バージョンでは、**HardwareStationController** および **IHardwareStationController** のクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="109de-110">For Retail SDK versions that are earlier than version 10.0.11, you extend the **HardwareStationController** and **IHardwareStationController** classes.</span></span>

## <a name="hardwarestationdeviceactionrequest"></a><span data-ttu-id="109de-111">HardwareStationDeviceActionRequest</span><span class="sxs-lookup"><span data-stu-id="109de-111">HardwareStationDeviceActionRequest</span></span>

<span data-ttu-id="109de-112">次のコード例は、**HardwareStationDeviceActionRequest** の定義を示します。</span><span class="sxs-lookup"><span data-stu-id="109de-112">The following code example shows the definition of **HardwareStationDeviceActionRequest**.</span></span>

```TypeScript
class HardwareStationDeviceActionRequest<TResponse extends HardwareStationDeviceActionResponse> extends Request<TResponse> {
    readonly device: string;
    readonly action: string;
    readonly actionData: any;
    constructor(device: string, action: string, actionData: any, correlationId?: string);
}
```

<span data-ttu-id="109de-113">次の表では、パラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="109de-113">The following table describes the parameters.</span></span>

| <span data-ttu-id="109de-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="109de-114">Parameter</span></span>  | <span data-ttu-id="109de-115">データ型</span><span class="sxs-lookup"><span data-stu-id="109de-115">Data type</span></span> | <span data-ttu-id="109de-116">説明</span><span class="sxs-lookup"><span data-stu-id="109de-116">Description</span></span> |
|------------|-----------|-------------|
| <span data-ttu-id="109de-117">デバイス</span><span class="sxs-lookup"><span data-stu-id="109de-117">device</span></span>     | <span data-ttu-id="109de-118">文字列</span><span class="sxs-lookup"><span data-stu-id="109de-118">String</span></span>    | <span data-ttu-id="109de-119">ハードウェア ステーションの要求に渡されるデバイス名は、ハードウェア ステーションのデバイス拡張機能コントローラー クラスに追加される**エクスポート**属性と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-119">The device name that is passed to the Hardware station request should match the **Export** attribute that is added in the Hardware station Device extension controller class.</span></span> |
| <span data-ttu-id="109de-120">アクション</span><span class="sxs-lookup"><span data-stu-id="109de-120">action</span></span>     | <span data-ttu-id="109de-121">文字列</span><span class="sxs-lookup"><span data-stu-id="109de-121">String</span></span>    | <span data-ttu-id="109de-122">ハードウェア ステーション拡張機能で呼び出す必要があるメソッド。</span><span class="sxs-lookup"><span data-stu-id="109de-122">The method that should be called in the Hardware station extension.</span></span> <span data-ttu-id="109de-123">メソッド名は、文字列値として渡される必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-123">The method name should be passed as a string value.</span></span> <span data-ttu-id="109de-124">コア POS ハードウェア ステーションの層レイヤーは、ハードウェア ステーション拡張機能コードから対応するメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="109de-124">The core POS Hardware station layer will then call the corresponding method from your Hardware station extension code.</span></span> <span data-ttu-id="109de-125">このメソッドは、ハードウェア ステーション拡張機能のメソッド名と完全に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-125">The method should exactly match the method name in your Hardware station extension.</span></span> <span data-ttu-id="109de-126">ハードウェア ステーション拡張機能は、パラメータとして渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-126">The Hardware station extension should be passed as a parameter.</span></span> |
| <span data-ttu-id="109de-127">actionData</span><span class="sxs-lookup"><span data-stu-id="109de-127">actionData</span></span> | <span data-ttu-id="109de-128">any</span><span class="sxs-lookup"><span data-stu-id="109de-128">any</span></span>       | <span data-ttu-id="109de-129">拡張機能を渡すためのカスタム パラメーター。</span><span class="sxs-lookup"><span data-stu-id="109de-129">A custom parameter for the extension to pass.</span></span> |

### <a name="sample-code"></a><span data-ttu-id="109de-130">サンプル コード</span><span class="sxs-lookup"><span data-stu-id="109de-130">Sample code</span></span>

<span data-ttu-id="109de-131">次のコードの例は､**HardwareStationDeviceActionRequest** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="109de-131">The following code example creates a **HardwareStationDeviceActionRequest** object.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("Export attribute in Hardware station controller class",
        "extension method name in Hardware station", "Custom parameters/you can also pass custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

## <a name="hardwarestationdeviceactionresponse"></a><span data-ttu-id="109de-132">HardwareStationDeviceActionResponse</span><span class="sxs-lookup"><span data-stu-id="109de-132">HardwareStationDeviceActionResponse</span></span>

<span data-ttu-id="109de-133">次のコード例は、**HardwareStationDeviceActionResponse** の定義を示します。</span><span class="sxs-lookup"><span data-stu-id="109de-133">The following code example shows the definition of **HardwareStationDeviceActionResponse**.</span></span>

```TypeScript
class HardwareStationDeviceActionResponse extends Response {
    readonly response: any;
    constructor(response: any);
}
```

<span data-ttu-id="109de-134">次の表では、パラメーターについて説明します。</span><span class="sxs-lookup"><span data-stu-id="109de-134">The following table describes the parameters.</span></span>

| <span data-ttu-id="109de-135">パラメーター</span><span class="sxs-lookup"><span data-stu-id="109de-135">Parameter</span></span>  | <span data-ttu-id="109de-136">データ型</span><span class="sxs-lookup"><span data-stu-id="109de-136">Data type</span></span> | <span data-ttu-id="109de-137">説明</span><span class="sxs-lookup"><span data-stu-id="109de-137">Description</span></span> |
|------------|-----------|-------------|
| <span data-ttu-id="109de-138">応答</span><span class="sxs-lookup"><span data-stu-id="109de-138">response</span></span>   | <span data-ttu-id="109de-139">any</span><span class="sxs-lookup"><span data-stu-id="109de-139">any</span></span>       | <span data-ttu-id="109de-140">ハードウェア ステーションから POS に送信される要求。</span><span class="sxs-lookup"><span data-stu-id="109de-140">The response that is sent from the Hardware station extension code to the POS.</span></span> |

## <a name="end-to-end-flow"></a><span data-ttu-id="109de-141">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="109de-141">End-to-end flow</span></span>

<span data-ttu-id="109de-142">次の図は、POS、ハードウェア ステーション、およびハードウェア デバイス間のフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="109de-142">The follow diagram shows the flow between the POS, Hardware station, and the hardware device.</span></span>

![フロー図](./media/POSDeviceExtension.png)

## <a name="hardware-station-extension"></a><span data-ttu-id="109de-144">ハードウェア ステーション拡張機能</span><span class="sxs-lookup"><span data-stu-id="109de-144">Hardware station extension</span></span>

<span data-ttu-id="109de-145">新しいハードウェア デバイスを呼び出すには、ハードウェア ステーション コードを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-145">To call your new hardware device, you must implement the Hardware station code.</span></span> <span data-ttu-id="109de-146">そのコードからハードウェア デバイスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="109de-146">You call your hardware device from that code.</span></span>

<span data-ttu-id="109de-147">Retail SDK バージョン10.0.11 以降の Hardware station 拡張機能を実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="109de-147">To implement the Hardware station extension for Retail SDK version 10.0.11 or later, follow these steps.</span></span>

1. <span data-ttu-id="109de-148">Microsoft .NET Framework バージョン 4.6.1を使用して、新しい C# クラス ライブラリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="109de-148">Create a new C# class library project by using the Microsoft .NET Framework version 4.6.1.</span></span> <span data-ttu-id="109de-149">または、Retail SDK に含まれているサンプルのいずれかをテンプレートとして使用します。</span><span class="sxs-lookup"><span data-stu-id="109de-149">Alternatively, use one of the samples in the Retail SDK as a template.</span></span> <span data-ttu-id="109de-150">(サンプルは **...\\RetailSDK\\SampleExtensions\\HardwareStation\\** で見つけることができます)。テンプレートとしてサンプルを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="109de-150">(You can find the samples at **...\\RetailSDK\\SampleExtensions\\HardwareStation\\**.) We recommend that you use a sample as a template.</span></span>
2. <span data-ttu-id="109de-151">拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-151">In the extension project, use the NuGet package manager to add the **Microsoft.Dynamics.Commerce.Hosting.Contracts** package.</span></span> <span data-ttu-id="109de-152">NuGet パッケージは、**RetailSDK\\pkgs** フォルダで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="109de-152">You can  find the NuGet packages in the **RetailSDK\\pkgs** folder.</span></span>
3. <span data-ttu-id="109de-153">**IController** インターフェイスを拡張する新しいコントローラ クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-153">Add a new controller class that extends the **IController** interface.</span></span>
4. <span data-ttu-id="109de-154">コントローラ クラスをクライアントに公開するには、コントローラ クラスに **RoutePrefix** 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-154">Add the **RoutePrefix** attribute to the controller class to expose the controller class to clients.</span></span>

    ```csharp
    [RoutePrefix("ISVEXTENSIONDEVICE")]
    ```

5. <span data-ttu-id="109de-155">ハードウェア デバイスを呼び出すためのカスタム ロジックを実装するために、**HttpPost** 属性を持つメソッドをコントローラー クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-155">To implement your custom logic to call the hardware device, in the controller class, add a method that has the **HttpPost** attribute.</span></span> <span data-ttu-id="109de-156">このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。</span><span class="sxs-lookup"><span data-stu-id="109de-156">This method will be passed as the second parameter (action parameter) to the POS **HardwareStationDeviceActionRequest**.</span></span> <span data-ttu-id="109de-157">拡張機能メソッドから、この拡張機能では、印刷やキャッシュ ドロワー要求などの他の要求を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="109de-157">From the extension method, the extension can call other requests, such as printing and cash drawer requests.</span></span> <span data-ttu-id="109de-158">Retail SDK から関連する NuGet パッケージのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="109de-158">Just include the relevant NuGet packages from the Retail SDK.</span></span>

    ```C#
    [HttpPost]
    public async Task<bool> IsReady(IEndpointContext context)
    {
    }
    ```

6. <span data-ttu-id="109de-159">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="109de-159">Build the project.</span></span>

<span data-ttu-id="109de-160">Retail SDK バージョン10.0.11 の Hardware station 拡張機能を実装するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="109de-160">To implement the Hardware station extension for Retail SDK versions that are earlier than version 10.0.11, follow these steps.</span></span>

1. <span data-ttu-id="109de-161">新しい C# クラス ライブラリ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="109de-161">Create a new C# class library project.</span></span>
2. <span data-ttu-id="109de-162">**HardwareStationController** と **IHardwareStationController** を拡張する新しいコントローラー クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-162">Add a new controller class that extends **HardwareStationController** and **IHardwareStationController**.</span></span>
3. <span data-ttu-id="109de-163">コントローラー クラスに**エクスポート**属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-163">Add the **Export** attribute to the controller class.</span></span> <span data-ttu-id="109de-164">**エクスポート**属性は、すべて大文字で指定する必要があり、値をパラメーターとして POS 拡張機能から渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-164">The **Export** attribute must be in all uppercase letters, and you must pass the value as a parameter from the POS extension.</span></span> <span data-ttu-id="109de-165">POS **HardwareStationDeviceActionRequest** から渡されるデバイス パラメータは、この値と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="109de-165">The device parameter that is passed from the POS **HardwareStationDeviceActionRequest** must match this value.</span></span>
4. <span data-ttu-id="109de-166">ハードウェア デバイスを呼び出すためのカスタム ロジックを実装するために、メソッドをコントローラ クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-166">To implement your custom logic to call the hardware device, add your method in the controller class.</span></span> <span data-ttu-id="109de-167">このメソッドは、POS **HardwareStationDeviceActionRequest** に対して 2 番目のパラメーター (アクション パラメーター) として渡されます。</span><span class="sxs-lookup"><span data-stu-id="109de-167">This method will be passed as the second parameter (action parameter) to the POS **HardwareStationDeviceActionRequest**.</span></span>
5. <span data-ttu-id="109de-168">プロジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="109de-168">Build the project.</span></span>

<span data-ttu-id="109de-169">Modern POS にハードウェア ステーション拡張機能を配置し、ローカル ハードウェア ステーションを使用してテストするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="109de-169">To deploy the Hardware station extension in Modern POS and test it by using the local Hardware station, follow these steps.</span></span>

1. <span data-ttu-id="109de-170">出力ライブラリを **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="109de-170">Copy the output library to the **C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder.</span></span>
2. <span data-ttu-id="109de-171">**HardwareStation.Extension.config** ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="109de-171">Open the **HardwareStation.Extension.config** file.</span></span>
3. <span data-ttu-id="109de-172">**合成** セクションで、拡張機能ライブラリの詳細を追加します。</span><span class="sxs-lookup"><span data-stu-id="109de-172">In the **composition** section, add the extension library details.</span></span>

    ```Xml
    <add source="assembly" value="your extension library name" />
    ```
 
4. <span data-ttu-id="109de-173">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="109de-173">Save the file.</span></span>
5. <span data-ttu-id="109de-174">現在実行中の場合は、Modern POS を閉じます。</span><span class="sxs-lookup"><span data-stu-id="109de-174">Close Modern POS if it's running.</span></span>
6. <span data-ttu-id="109de-175">タスク マネージャーを開いて、**dllhost.exe** タスクを終了します。</span><span class="sxs-lookup"><span data-stu-id="109de-175">Open Task Manager, and end the **dllhost.exe** task.</span></span>
7. <span data-ttu-id="109de-176">Modern POS を開いて、ローカル ハードウェア ステーションを使用するように構成します。</span><span class="sxs-lookup"><span data-stu-id="109de-176">Open Modern POS, and configure it to use the local Hardware station.</span></span>
8. <span data-ttu-id="109de-177">シナリオを検証します。</span><span class="sxs-lookup"><span data-stu-id="109de-177">Validate your scenario.</span></span>

<span data-ttu-id="109de-178">Cloud POS を使用してテストするには、ハードウェア ステーション拡張機能のダイナミクス リンク ライブラリ (DLL) を、共有ハードウェア ステーションの **ext** フォルダに配置します。</span><span class="sxs-lookup"><span data-stu-id="109de-178">To test by using Cloud POS, deploy the dynamics-link library (DLL) of the Hardware station extension to the shared Hardware station **ext** folder.</span></span> <span data-ttu-id="109de-179">次に、共有ハードウェア ステーション フォルダのカスタム ライブラリを使用して、**HardwareStation.Extension.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="109de-179">Then update the **HardwareStation.Extension.config** file with the custom library in the shared Hardware station folder.</span></span>

## <a name="retail-sdk-samples"></a><span data-ttu-id="109de-180">Retail SDK サンプル</span><span class="sxs-lookup"><span data-stu-id="109de-180">Retail SDK samples</span></span>

<span data-ttu-id="109de-181">Retail SDK には、参照用に使用できるサンプルがいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="109de-181">The Retail SDK includes some samples that you can use for reference.</span></span>

+ <span data-ttu-id="109de-182">**POS:** \\RetailSDK\\POS\\Extensions\\FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="109de-182">**POS:** \\RetailSDK\\POS\\Extensions\\FiscalRegisterSample</span></span>
+ <span data-ttu-id="109de-183">**ハードウェア ステーション:** \\RetailSDK\\SampleExtensions\\HardwareStation\\Extension.FiscalRegisterSample</span><span class="sxs-lookup"><span data-stu-id="109de-183">**Hardware station:** \\RetailSDK\\SampleExtensions\\HardwareStation\\Extension.FiscalRegisterSample</span></span>

## <a name="sample-code-for-retail-sdk-version-10011-or-later"></a><span data-ttu-id="109de-184">Retail SDK バージョン 10.0.11 以降のサンプル コード</span><span class="sxs-lookup"><span data-stu-id="109de-184">Sample code for Retail SDK version 10.0.11 or later</span></span>

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

## <a name="sample-code-for-retail-sdk-versions-before-version-10011"></a><span data-ttu-id="109de-185">Retail SDK バージョン 10.0.11 以前のサンプル コード</span><span class="sxs-lookup"><span data-stu-id="109de-185">Sample code for Retail SDK versions before version 10.0.11</span></span>

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

## <a name="sample-pos-code-to-call-the-hardware-station-extension"></a><span data-ttu-id="109de-186">ハードウェア ステーション拡張機能を呼び出すためのサンプル POS コード</span><span class="sxs-lookup"><span data-stu-id="109de-186">Sample POS code to call the Hardware station extension</span></span>

<span data-ttu-id="109de-187">POS 拡張機能から、次のパターンを使用してハードウェア ステーションを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="109de-187">From your POS extension, call the Hardware station by using the following pattern.</span></span>

```TypeScript
let hardwareStationDeviceActionRequest: HardwareStationDeviceActionRequest<HardwareStationDeviceActionResponse> =
    new HardwareStationDeviceActionRequest("ISVEXTENSIONDEVICE",
        "Sample", "Custom parameters or custom object");
return this.extensionContextRuntime.executeAsync(hardwareStationDeviceActionRequest);
```

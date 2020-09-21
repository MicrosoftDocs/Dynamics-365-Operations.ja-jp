---
title: 新しい Retail Server API の作成
description: このトピックでは、Retail SDK バージョン 10.0.11 以降を使用して新しい Retail Server API を作成する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 802c81b5d486c0cbd26da643cbedfdc09f58bbd0
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741473"
---
# <a name="create-a-new-retail-server-extension-api-retail-sdk-version-10011-and-later"></a><span data-ttu-id="d93e0-103">新しい Retail Server 拡張 API の作成 (Retail SDK バージョン 10.0.11 以降)</span><span class="sxs-lookup"><span data-stu-id="d93e0-103">Create a new Retail Server extension API (Retail SDK version 10.0.11 and later)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d93e0-104">このドキュメントでは、新しい Retail Server アプリケーション プログラミング インターフェイス (API) の作成方法、および POS または他のクライアントがそれを使用できるようにするための公開方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-104">This document explains how to create a new Retail Server application programming interface (API), and how to expose it so that POS or other clients can consume it.</span></span> <span data-ttu-id="d93e0-105">既存の Retail Server API の変更はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-105">Modification of the existing Retail Server APIs isn't supported.</span></span>

<span data-ttu-id="d93e0-106">このトピックは、Retail SDK バージョン 10.0.11 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-106">This topic applies to Retail SDK version 10.0.11 and later.</span></span>

<span data-ttu-id="d93e0-107">Retail ソフトウェア開発キット (SDK) には、Commerce Runtime (CRT) を含む、エンドツーエンドの Retail Server 拡張機能のサンプルがいくつか用意されているのみです。</span><span class="sxs-lookup"><span data-stu-id="d93e0-107">The Retail software development kit (SDK) includes only a few samples of end-to-end Retail Server extensions that include the Commerce Runtime (CRT).</span></span> <span data-ttu-id="d93e0-108">これらのサンプルをテンプレートとして使用して、拡張機能を起動できます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-108">You can use these samples as templates to start your extensions.</span></span> <span data-ttu-id="d93e0-109">サンプル拡張機能は、**RetailSDK\\SampleExtensions\\RetailServer** フォルダーで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-109">You can find the sample extensions in the **RetailSDK\\SampleExtensions\\RetailServer** folder.</span></span>

## <a name="end-to-end-sample-repository-in-the-retail-sdk"></a><span data-ttu-id="d93e0-110">Retail SDK のエンドツーエンド サンプル リポジトリ</span><span class="sxs-lookup"><span data-stu-id="d93e0-110">End-to-end sample repository in the Retail SDK</span></span>

| <span data-ttu-id="d93e0-111">サンプル拡張機能</span><span class="sxs-lookup"><span data-stu-id="d93e0-111">Sample extension</span></span><br><span data-ttu-id="d93e0-112">(RetailSDK\\SampleExtensions\\RetailServer)</span><span class="sxs-lookup"><span data-stu-id="d93e0-112">(RetailSDK\\SampleExtensions\\RetailServer)</span></span> | <span data-ttu-id="d93e0-113">CRT サンプル</span><span class="sxs-lookup"><span data-stu-id="d93e0-113">CRT sample</span></span><br><span data-ttu-id="d93e0-114">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span><span class="sxs-lookup"><span data-stu-id="d93e0-114">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span></span> | <span data-ttu-id="d93e0-115">POS サンプル</span><span class="sxs-lookup"><span data-stu-id="d93e0-115">POS sample</span></span><br><span data-ttu-id="d93e0-116">(RetailSDK\\POS\\Extensions)</span><span class="sxs-lookup"><span data-stu-id="d93e0-116">(RetailSDK\\POS\\Extensions)</span></span> |
|---------------------------------------------|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="d93e0-117">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-117">Extensions.StoreHoursSample</span></span>                 | <span data-ttu-id="d93e0-118">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-118">Extensions.StoreHoursSample</span></span>                | <span data-ttu-id="d93e0-119">StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-119">StoreHoursSample</span></span>                       |
| <span data-ttu-id="d93e0-120">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-120">Extensions.SalesTransactionSignatureSample</span></span>  | <span data-ttu-id="d93e0-121">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-121">Extensions.SalesTransactionSignatureSample</span></span> | <span data-ttu-id="d93e0-122">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-122">SalesTransactionSignatureSample</span></span>        |
| <span data-ttu-id="d93e0-123">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-123">Extensions.PrintPackingSlipSample</span></span>           | <span data-ttu-id="d93e0-124">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="d93e0-124">Extensions.PrintPackingSlipSample</span></span>          |                                        |
| <span data-ttu-id="d93e0-125">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="d93e0-125">Extensions.CrossLoyaltySample</span></span>               | <span data-ttu-id="d93e0-126">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="d93e0-126">Extensions.CrossLoyaltySample</span></span>              |                                        |

## <a name="extension-class-diagram"></a><span data-ttu-id="d93e0-127">拡張機能クラス ダイアグラム</span><span class="sxs-lookup"><span data-stu-id="d93e0-127">Extension class diagram</span></span>

<span data-ttu-id="d93e0-128">次の図は、拡張機能のクラス ダイアグラムを示しています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-128">The following illustration shows the class structure of the extension.</span></span>

![Commerce Scale Unit の拡張機能クラス ダイアグラム](media/RSExtensionClass.png)

## <a name="create-the-new-retail-server-api"></a><span data-ttu-id="d93e0-130">新しい Retail Server API の作成</span><span class="sxs-lookup"><span data-stu-id="d93e0-130">Create the new Retail Server API</span></span>

1. <span data-ttu-id="d93e0-131">CRT 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-131">Create the CRT extension.</span></span> <span data-ttu-id="d93e0-132">Retail Server 拡張機能を作成する前に、CRT 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-132">You must create the CRT extension before you create the Retail Server extension.</span></span> <span data-ttu-id="d93e0-133">Retail Server API には、パラメーターで CRT を呼び出すロジック以外のロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-133">A Retail Server API should have no logic except logic that calls the CRT with the parameters.</span></span>
2. <span data-ttu-id="d93e0-134">Microsoft .NET Framework バージョン 4.6.1 を使用する新しい C# クラス ライブラリ プロジェクトを作成するか、または Retail SDK 内の Retail Server のサンプルのいずれかをテンプレートとして使用します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-134">Create a new C# class library project that uses Microsoft .NET Framework version 4.6.1, or use any of the Retail Server samples in the Retail SDK as a template.</span></span>
3. <span data-ttu-id="d93e0-135">Retail Server 拡張機能プロジェクトで、CRT 拡張機能ライブラリまたはプロジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-135">In the Retail Server extension project, add a reference to your CRT extension library or project.</span></span> <span data-ttu-id="d93e0-136">この参照を使用して、CRT 要求、応答およびエンティティを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-136">This reference lets you call the CRT request, response, and entities.</span></span>
4. <span data-ttu-id="d93e0-137">Retail Server 拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-137">In the Retail Server extension project, add the **Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts** package using the NuGet package manager.</span></span> <span data-ttu-id="d93e0-138">NuGet パッケージは、**RetailSDK\\pkgs** フォルダにあります。</span><span class="sxs-lookup"><span data-stu-id="d93e0-138">The NuGet packages can be found in the **RetailSDK\\pkgs** folder.</span></span>
5. <span data-ttu-id="d93e0-139">新しいコントローラー クラスを作成し、**IController** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-139">Create a new controller class and extend it from **IController**.</span></span> <span data-ttu-id="d93e0-140">このコントローラー クラスには、Retail Server API によって公開される必要のあるメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-140">This controller class will contain the method that must be exposed by the Retail Server API.</span></span> <span data-ttu-id="d93e0-141">コントローラー クラス内で、CRT 要求を呼び出すメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-141">Inside the controller class, add methods to call the CRT request.</span></span> <span data-ttu-id="d93e0-142">新しいコントローラー クラスを、**CustomerController** や **ProductController** などの既存のコントローラー クラスから拡張しないでください。</span><span class="sxs-lookup"><span data-stu-id="d93e0-142">Don’t extend the new controller class from existing controller classes like **CustomerController** and **ProductController**.</span></span> <span data-ttu-id="d93e0-143">拡張クラスでは、**IController** クラスのみを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d93e0-143">Extension classes must extend only the **IController** class.</span></span>
6. <span data-ttu-id="d93e0-144">コントローラー クラス (コントローラー クラス名) 上で **RoutePrefix** 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-144">Add the **RoutePrefix** attribute on the controller class (Controller class name).</span></span>

    ```csharp
    [RoutePrefix("SimpleExtension")]  
    ```

7. <span data-ttu-id="d93e0-145">**BindEntity** 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-145">Add the **BindEntity** attribute.</span></span> <span data-ttu-id="d93e0-146">これは、新しいコントローラーを作成してエンティティを公開する場合に、コントローラー クラスで必要です。</span><span class="sxs-lookup"><span data-stu-id="d93e0-146">This is required on a controller class if you are creating a new controller and exposing an entity.</span></span>

```csharp
    [BindEntity(typeof(SimpleEntity))]
```

> [!NOTE]
> <span data-ttu-id="d93e0-147">拡張クラスがエンティティにバインドされている場合は、手順 6 と 7 が必要です。</span><span class="sxs-lookup"><span data-stu-id="d93e0-147">Step 6 and 7 are required if the extension class is bound to an entity.</span></span> <span data-ttu-id="d93e0-148">これらの手順は、エンティティではなく、単純型を返す非制限コントローラ クラスには必要ありません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-148">These steps are not required for an unbounded controller class returning simple types, not any entity.</span></span>

<span data-ttu-id="d93e0-149">次のサンプル コードでは、エンティティ、文字列、およびブール値を返す単純な Retail Server API を作成します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-149">The following sample code creates a simple Retail Server API to return an entity, a string, and a bool value.</span></span> <span data-ttu-id="d93e0-150">サンプルで使用されている CRT 要求および応答は、このサンプルには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-150">The CRT request and response used in the sample is not included in this sample.</span></span> <span data-ttu-id="d93e0-151">CRT 要求および応答の例については、[Commerce Runtime (CRT) の拡張機能およびトリガー](commerce-runtime-extensibility-trigger.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d93e0-151">For an example of the CRT request and response, see [Commerce runtime (CRT) extensibility and triggers](commerce-runtime-extensibility-trigger.md).</span></span>

### <a name="sample-code-for-a-controller-class-bounded-to-a-custom-entity"></a><span data-ttu-id="d93e0-152">カスタム エンティティにバインドされるコントローラ クラスのサンプルコード</span><span class="sxs-lookup"><span data-stu-id="d93e0-152">Sample code for a controller class bounded to a custom entity</span></span>

> [!NOTE]
> <span data-ttu-id="d93e0-153">拡張コードは、顧客や製品などの既存の OOB エンティティにバインドしてはいけません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-153">Extension code should not bound the existing OOB entity, such as Customer or Product.</span></span>

```csharp
    /// <summary>
        /// New extended controller.
        /// </summary>
        [RoutePrefix("SimpleExtension")]  
        [BindEntity(typeof(SimpleEntity))]
        public class SimpleExtensionController : IController
        {
            /// <summary>
            /// The action to get the string value.
            /// </summary>
            /// <param name="context">The context parameters.</param>
            /// <param name="stringValue">The string value parameters.</param>
            /// <returns>The string value.</returns>
            [HttpPost]
            [Authorization(CommerceRoles.Customer, CommerceRoles.Employee)]
            public async Task<string> GetStringValue(IEndpointContext context, string stringValue)
            {
                GetStringValueResponse resp = await context.ExecuteAsync<GetStringValueResponse>
                                         (new GetStringValueRequest(stringValue)).ConfigureAwait(false);
                return resp.StringValue;
            }

            /// <summary>
            /// The action to get the bool value.
            /// </summary>
            /// <param name="context">The context parameters.</param>
            /// <param name="boolValue">The string value parameters.</param>
            /// <returns>The bool value.</returns>
            [HttpPost]
            [Authorization(CommerceRoles.Customer, CommerceRoles.Employee)]
            public async Task<bool> GetBoolValue(IEndpointContext context, string boolValue)
            {
                GetBoolValueResponse resp = await context.ExecuteAsync<GetBoolValueResponse>
                                           (new GetBoolValueRequest(boolValue)).ConfigureAwait(false);
                return resp.BoolValue;
            }

            /// <summary>
            /// The action to get the simple entity.
            /// </summary>
            /// <param name="context">The context parameters.</param>
            /// <param name="name">The name parameters.</param>
            /// <returns>The simple entity.</returns>
            [HttpPost]
            [Authorization(CommerceRoles.Customer, CommerceRoles.Employee)]
            public async Task<SimpleEntity> GetSimpleEntity(IEndpointContext context, string name)
            {
                GetSimpleEntityResponse resp = await context.ExecuteAsync<GetSimpleEntityResponse>
                                               (new GetSimpleEntityRequest(name)).ConfigureAwait(false);
                return resp.SimpleEntityObj;
            }
        }
```

### <a name="sample-code-for-a-controller-class-not-bounded-to-a-custom-entity"></a><span data-ttu-id="d93e0-154">カスタム エンティティにバインドされていないコントローラ クラスのサンプルコード</span><span class="sxs-lookup"><span data-stu-id="d93e0-154">Sample code for a controller class not bounded to a custom entity</span></span>

```csharp
namespace Contoso.UnboundController.Sample
{
    using System.Threading.Tasks;
    using Microsoft.Dynamics.Commerce.Runtime.DataModel;
    using Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts;

    /// <summary>
    /// An extension unbounded controller sample.
    /// </summary>
    public class UnboundController : IController
    {
        /// <summary>
        /// A simple GET endpoint to demonstrate GET endpoints on an unbound controller.
        /// </summary>
        /// <returns>A simple true value to indicate the endpoint was reached.</returns>
        [HttpGet]
        [Authorization(CommerceRoles.Anonymous, CommerceRoles.Application, CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee, CommerceRoles.Storefront)]
        public Task<bool> SampleGet()
        {
            return Task.FromResult(true);
        }

        /// <summary>
        /// A simple POST endpoint to demonstrate POST endpoints on an unbound controller.
        /// </summary>
        /// <returns>A simple true value to indicate the endpoint was reached.</returns>
        [HttpPost]
        [Authorization(CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee)]
        public Task<bool> SamplePost()
        {
            return Task.FromResult(true);
        }
    }
}

```

<span data-ttu-id="d93e0-155">Retail Server API では、さまざまな承認ロールがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-155">The Retail Server APIs support different authorization roles.</span></span> <span data-ttu-id="d93e0-156">コントローラー メソッドへのアクセスは、コントローラー メソッドの**承認**属性で指定された承認ロールに基づいて許可されます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-156">Access to the controller method is permitted based on the authorization roles specified in the controller method **Authorizations** attribute.</span></span> <span data-ttu-id="d93e0-157">次のコード例には、サポートされている承認ロールが示されています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-157">The supported authorization roles are shown in the following code example.</span></span>

```csharp
    // Summary:
    // Represents the type of logon type.
    [DataContract]
    public static class CommerceRoles
    {
        //
        // Summary:
        //     Anonymous Role.
        [DataMember]
        public const string Anonymous = "Anonymous";
        //
        // Summary:
        //     SharePoint Role used by Connector.
        [DataMember]
        public const string Storefront = "Storefront";
        //
        // Summary:
        //     Employee Role.
        [DataMember]
        public const string Employee = "Employee";
        //
        // Summary:
        //     Customer Role.
        [DataMember]
        public const string Customer = "Customer";
        //
        // Summary:
        //     Represents the Device level of authentication.
        [DataMember]
        public const string Device = "Device";
        //
        // Summary:
        //     Represents Application level of authentication.
        [DataMember]
        public const string Application = "Application";
        //
        // Summary:
        //     The list of all possible Microsoft.Dynamics.Commerce.Runtime.DataModel.CommerceRoles
        //     values.
        public static readonly string[] All;
    }
 ```

8. <span data-ttu-id="d93e0-158">拡張機能プロジェクトをビルドし、バイナリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d93e0-158">Build the extension project, and copy the binary to the **\\RetailServer\\webroot\\bin\\Ext** folder.</span></span>
9. <span data-ttu-id="d93e0-159">**extensionComposition** セクションで新しい拡張ライブラリ名を追加して、**\\RetailServer\\webroot** フォルダーの Commerce Scale Unit **web.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-159">Update the Commerce Scale Unit **web.config** file in the **\\RetailServer\\webroot** folder by adding the new extension library name in the **extensionComposition** section.</span></span>

```xml
    <extensionComposition>
    <!-- Use fully qualified assembly names for ALL if you need to support loading from the Global Assembly Cache.
    If you host in an application with a bin folder, this is not required. -->
    <add source="assembly" value="SimpleExtensionSample" >
    </extensionComposition>
```

10. <span data-ttu-id="d93e0-160">Microsoft インターネット インフォメーション サービス (IIS) で、Commerce Scale Unit を再起動して、新しい拡張機能を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-160">In Microsoft Internet Information Services (IIS), restart the Commerce Scale Unit to load the new extension.</span></span>
11. <span data-ttu-id="d93e0-161">拡張機能が正常に読み込まれたことを確認するには、Retail Server のメタデータを参照します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-161">To verify that the extension loaded successfully, you can browse the Retail Server metadata.</span></span> <span data-ttu-id="d93e0-162">エンティティおよびメソッドが一覧に表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-162">Confirm that your entities and methods appear in the list.</span></span> <span data-ttu-id="d93e0-163">メタデータを参照するには、Web ブラウザーの次の形式で URL を開きます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-163">To browse the metadata, open a URL in the following format in a web browser:</span></span>

    <span data-ttu-id="d93e0-164">**https://RS-URL/Commerce/$metadata**</span><span class="sxs-lookup"><span data-stu-id="d93e0-164">**https://RS-URL/Commerce/$metadata**</span></span>

12. <span data-ttu-id="d93e0-165">クライアントで Retail Server 拡張機能を呼び出すには、クライアント Typescript プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d93e0-165">To call the Retail Server extension in your client, you must generate the client Typescript proxy.</span></span> <span data-ttu-id="d93e0-166">その後、プロキシを使用して、クライアントから新しい Retail Server API を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-166">You can then use the proxy to call your new Retail Server APIs from the client.</span></span>

<span data-ttu-id="d93e0-167">Retail Server 拡張 API を使用して、**EdmModelExtender** ファイルを拡張機能に追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-167">You don't need to add or include any **EdmModelExtender** files in the extension with the Retail Server extensions APIs.</span></span> <span data-ttu-id="d93e0-168">これらのファイルは、Retail SDK バージョン 10.0.10 またはそれ以前を使用している場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="d93e0-168">The files are required only if you are using Retail SDK version 10.0.10 or earlier.</span></span>


## <a name="generate-the-typescript-proxy-for-pos"></a><span data-ttu-id="d93e0-169">POS Typescript プロキシの生成</span><span class="sxs-lookup"><span data-stu-id="d93e0-169">Generate the Typescript proxy for POS</span></span>
<span data-ttu-id="d93e0-170">POS は Typescript プロキシ を使って、Retail サーバー API や CRT エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d93e0-170">The POS uses the Typescript proxy to access the Retail Server APIs and CRT entities.</span></span> <span data-ttu-id="d93e0-171">プロキシ クラスは、サービスを実行するためのクラスまたは Wrapper として機能し、プロキシ拡張機能を使用せずに Retail Server API やエンティティ メタデータを検索することによって、Retail Server API にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="d93e0-171">The proxy class acts as manger class or wrapper to access the Retail server APIs without the proxy extension manually finding the Retail server API and entities metadata.</span></span>

<span data-ttu-id="d93e0-172">**プロキシ ファイルを生成する手順**</span><span class="sxs-lookup"><span data-stu-id="d93e0-172">**Steps to generate the proxy files**</span></span>

1. <span data-ttu-id="d93e0-173">Visual Studio 2017 の **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** からサンプル プロキシ テンプレート プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-173">Open the sample proxy template project from **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** in Visual Studio 2017.</span></span> <span data-ttu-id="d93e0-174">必要に応じて名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-174">Rename it if required.</span></span>
2. <span data-ttu-id="d93e0-175">このプロキシ テンプレート プロジェクトに、Retail Server 拡張プロジェクトをプロジェクト参照プロジェクトとして追加します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-175">Add the Retail Server extension project as a project reference project to this proxy template project.</span></span> <span data-ttu-id="d93e0-176">既存の **StoreHoursSample** プロジェクト参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-176">Remove the existing **StoreHoursSample** project reference.</span></span>
3. <span data-ttu-id="d93e0-177">**Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** を右クリックし、**Edit Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-177">Right-click the **Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** and select **Edit Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj**.</span></span>
4. <span data-ttu-id="d93e0-178">**\<RetailServerExtensionAssemblies\>** ノードの下に、Retail Server 拡張機能のアセンブリ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-178">Under the **\<RetailServerExtensionAssemblies\>** node, specify your extension Retail Server assembly name.</span></span> <span data-ttu-id="d93e0-179">次の例は、アセンブリ名を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-179">The following example shows how to add the assembly name.</span></span>

    ```xml
      <ItemGroup>
        <RetailServerExtensionAssemblies Include="..\..\RetailServer\Extensions.Sample\bin\$(Configuration)\net461\$(AssemblyNamePrefix).RetailServer.Extension.Sample.dll" />
      </ItemGroup>
    ```

5.  <span data-ttu-id="d93e0-180">**コピー** ノードの下で、**DestinationFolder** パスを拡張フォルダーに更新して、生成されたプロキシファイルが POS 拡張フォルダーに自動的にコピーされるようにします。</span><span class="sxs-lookup"><span data-stu-id="d93e0-180">Under the **Copy** node, update the **DestinationFolder** path to your POS extension folder, so that generated proxy files are copied to the POS Extension folder automatically.</span></span> <span data-ttu-id="d93e0-181">生成されたプロキシ ファイルも **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-181">The generated proxy files will also be copied to **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService**.</span></span> <span data-ttu-id="d93e0-182">次の例は、パスを更新する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-182">The following example shows how to update the path.</span></span>

    ```xml
    <Copy SourceFiles="@(GeneratedDataServiceContracts)" DestinationFolder="$(SdkRootPath)\POS\Extensions\Sample\DataService" SkipUnchangedFiles="true" />
    ```

6. <span data-ttu-id="d93e0-183">変更が完了したら、プロキシ プロジェクトをビルドして typescript プロキシ ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-183">After the changes are complete, build the proxy project to generate the typescript proxy files.</span></span> <span data-ttu-id="d93e0-184">ビルドが完了すると、**\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** フォルダーでプロキシ ファイルが使用可能となり、そのフォルダーは**コピー** コマンドによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-184">When the build is completed the proxy files are available in the **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** folder and the folder specified in the **Copy** command.</span></span> <span data-ttu-id="d93e0-185">パスとフォルダー パスは、フォルダ構造によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d93e0-185">The path and folder path can vary based on the folder structure.</span></span>

## <a name="retail-server-extension-in-offline"></a><span data-ttu-id="d93e0-186">オフラインの Retail Server 拡張機能</span><span class="sxs-lookup"><span data-stu-id="d93e0-186">Retail server extension in offline</span></span>

<span data-ttu-id="d93e0-187">**Microsoft.Dynamics.Commerce.Hosting.Contracts** API を使用してビルトされた Retail Server 拡張機能は、オフライン実装でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="d93e0-187">A Retail Server extension built using the **Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts** API can be used in an offline implementation.</span></span> <span data-ttu-id="d93e0-188">個別の C# プロキシ ライブラリを生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="d93e0-188">You don't need to generate a separate C# proxy library.</span></span> <span data-ttu-id="d93e0-189">**\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにある Retail Server 拡張機能ライブラリをコピーして、 **RetailProxy.MPOSOffline.ext** 構成ファイルにこのライブラリを含めるように構成します。</span><span class="sxs-lookup"><span data-stu-id="d93e0-189">Copy the Retail Server extension library in the **\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder and update the **RetailProxy.MPOSOffline.ext** config file to include the this library.</span></span> <span data-ttu-id="d93e0-190">この拡張機能では、Typescript プロキシのみを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d93e0-190">This extension must only generate the Typescript proxy.</span></span> <span data-ttu-id="d93e0-191">SDK サンプルは、**\\RetailSDK\\SampleExtensions\\TypeScriptProxy)** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="d93e0-191">SDK samples can be found in the  **\\RetailSDK\\SampleExtensions\\TypeScriptProxy)** folder.</span></span>

<span data-ttu-id="d93e0-192">次の例は、**RetailProxy.MPOSOffline.ext** 構成ファイル内の **add** 要素を更新する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d93e0-192">The following example shows how to update the **add** element in the **RetailProxy.MPOSOffline.ext** config file.</span></span>

```xml
    <?xml version="1.0" encoding="utf-8"?> 
    <retailProxyExtensions> 
        <composition> 
            <add source="assembly" value="Contoso.RetailServer.StoreHoursSamp1e" /> 
        </composition> 
    </retailProxyExtensions> 
```


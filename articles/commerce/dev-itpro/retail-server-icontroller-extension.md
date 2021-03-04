---
title: Retail Server 拡張 API の作成 (Retail SDK バージョン 10.0.11 以降)
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
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-08-2019
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 9912b1f19469d6f8735abc308ccf3c58d4e25794
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5126680"
---
# <a name="create-a-retail-server-extension-api-retail-sdk-version-10011-and-later"></a><span data-ttu-id="3c582-103">Retail Server 拡張 API の作成 (Retail SDK バージョン 10.0.11 以降)</span><span class="sxs-lookup"><span data-stu-id="3c582-103">Create a Retail Server extension API (Retail SDK version 10.0.11 and later)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c582-104">このトピックでは、新しい Retail Server アプリケーション プログラミング インターフェイス (API) の作成方法、および 販売時点管理 (POS) または他のクライアントがそれを使用できるようにするための公開方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3c582-104">This topic explains how to create a new Retail Server application programming interface (API), and how to expose it so that point of sale (POS) or other clients can consume it.</span></span> <span data-ttu-id="3c582-105">既存の Retail Server API の変更はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3c582-105">Modification of the existing Retail Server APIs isn't supported.</span></span>

<span data-ttu-id="3c582-106">このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.11 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3c582-106">This topic applies to Retail software development kit (SDK) version 10.0.11 and later.</span></span>

<span data-ttu-id="3c582-107">Retail SDK には、Commerce Runtime (CRT) を含む、エンドツーエンドの Retail Server 拡張機能のサンプルがいくつか用意されているのみです。</span><span class="sxs-lookup"><span data-stu-id="3c582-107">The Retail SDK includes only a few samples of end-to-end Retail Server extensions that include the Commerce runtime (CRT).</span></span> <span data-ttu-id="3c582-108">これらのサンプルをテンプレートとして使用して、拡張機能を起動できます。</span><span class="sxs-lookup"><span data-stu-id="3c582-108">You can use these samples as templates to start your extensions.</span></span> <span data-ttu-id="3c582-109">サンプル拡張機能は、**RetailSDK\\SampleExtensions\\RetailServer** フォルダーで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="3c582-109">You can find the sample extensions in the **RetailSDK\\SampleExtensions\\RetailServer** folder.</span></span>

## <a name="end-to-end-sample-repository-in-the-retail-sdk"></a><span data-ttu-id="3c582-110">Retail SDK のエンドツーエンド サンプル リポジトリ</span><span class="sxs-lookup"><span data-stu-id="3c582-110">End-to-end sample repository in the Retail SDK</span></span>

| <span data-ttu-id="3c582-111">サンプル拡張機能</span><span class="sxs-lookup"><span data-stu-id="3c582-111">Sample extension</span></span><br><span data-ttu-id="3c582-112">(RetailSDK\\SampleExtensions\\RetailServer)</span><span class="sxs-lookup"><span data-stu-id="3c582-112">(RetailSDK\\SampleExtensions\\RetailServer)</span></span> | <span data-ttu-id="3c582-113">CRT サンプル</span><span class="sxs-lookup"><span data-stu-id="3c582-113">CRT sample</span></span><br><span data-ttu-id="3c582-114">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span><span class="sxs-lookup"><span data-stu-id="3c582-114">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span></span> | <span data-ttu-id="3c582-115">POS サンプル</span><span class="sxs-lookup"><span data-stu-id="3c582-115">POS sample</span></span><br><span data-ttu-id="3c582-116">(RetailSDK\\POS\\Extensions)</span><span class="sxs-lookup"><span data-stu-id="3c582-116">(RetailSDK\\POS\\Extensions)</span></span> |
|---------------------------------------------|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="3c582-117">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="3c582-117">Extensions.StoreHoursSample</span></span>                 | <span data-ttu-id="3c582-118">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="3c582-118">Extensions.StoreHoursSample</span></span>                | <span data-ttu-id="3c582-119">StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="3c582-119">StoreHoursSample</span></span>                       |
| <span data-ttu-id="3c582-120">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="3c582-120">Extensions.SalesTransactionSignatureSample</span></span>  | <span data-ttu-id="3c582-121">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="3c582-121">Extensions.SalesTransactionSignatureSample</span></span> | <span data-ttu-id="3c582-122">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="3c582-122">SalesTransactionSignatureSample</span></span>        |
| <span data-ttu-id="3c582-123">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="3c582-123">Extensions.PrintPackingSlipSample</span></span>           | <span data-ttu-id="3c582-124">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="3c582-124">Extensions.PrintPackingSlipSample</span></span>          |                                        |
| <span data-ttu-id="3c582-125">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="3c582-125">Extensions.CrossLoyaltySample</span></span>               | <span data-ttu-id="3c582-126">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="3c582-126">Extensions.CrossLoyaltySample</span></span>              |                                        |

## <a name="extension-class-diagram"></a><span data-ttu-id="3c582-127">拡張機能クラス ダイアグラム</span><span class="sxs-lookup"><span data-stu-id="3c582-127">Extension class diagram</span></span>

<span data-ttu-id="3c582-128">次の図は、拡張機能のクラス ダイアグラムを示しています。</span><span class="sxs-lookup"><span data-stu-id="3c582-128">The following illustration shows the class structure of the extension.</span></span>

![Commerce Scale Unit の拡張機能クラス ダイアグラム](media/RSExtensionClass.png)

> [!NOTE]
> <span data-ttu-id="3c582-130">Retail サーバーでは、IController と CommerceController の両方の拡張機能の読み込みはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="3c582-130">Retail server does not support loading both IController and CommerceController extensions.</span></span> <span data-ttu-id="3c582-131">両方のタイプの拡張機能を含めると、Retail サーバーの負荷は失敗します。</span><span class="sxs-lookup"><span data-stu-id="3c582-131">If you include both type of extensions, then Retail server load will fail.</span></span> <span data-ttu-id="3c582-132">拡張機能は IController または CommerceController のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c582-132">Extensions should have either IController or CommerceController.</span></span> <span data-ttu-id="3c582-133">IController 拡張機能に移行する場合は、すべての Retail サーバー拡張機能を IController に移行します。</span><span class="sxs-lookup"><span data-stu-id="3c582-133">If you are migrating to the IController extension, migrate all the Retail server extensions to IController.</span></span>

## <a name="create-a-new-retail-server-api"></a><span data-ttu-id="3c582-134">新しい Retail Server API の作成</span><span class="sxs-lookup"><span data-stu-id="3c582-134">Create a new Retail Server API</span></span>

1. <span data-ttu-id="3c582-135">CRT 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="3c582-135">Create the CRT extension.</span></span> <span data-ttu-id="3c582-136">Retail Server 拡張機能を作成する前に、CRT 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="3c582-136">You must create the CRT extension before you create the Retail Server extension.</span></span> <span data-ttu-id="3c582-137">Retail Server API には、パラメーターで CRT を呼び出すロジック以外のロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="3c582-137">A Retail Server API should have no logic except logic that calls the CRT with the parameters.</span></span>
2. <span data-ttu-id="3c582-138">Microsoft .NET フレームワーク バージョン netstandard 2.0 をターゲット フレームワークとして使用する、新しい C# クラス ライブラリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="3c582-138">Create a new C# class library project that uses the Microsoft .NET Framework version netstandard 2.0 as the target framework.</span></span> <span data-ttu-id="3c582-139">または、Retail SDK に含まれている Retail Server のサンプルのいずれかをテンプレートとして使用します。</span><span class="sxs-lookup"><span data-stu-id="3c582-139">Alternatively, use one of the Retail Server samples in the Retail SDK as a template.</span></span>
3. <span data-ttu-id="3c582-140">Retail Server 拡張機能プロジェクトで、CRT 拡張機能ライブラリまたはプロジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="3c582-140">In the Retail Server extension project, add a reference to your CRT extension library or project.</span></span> <span data-ttu-id="3c582-141">この参照を使用して、CRT 要求、応答およびエンティティを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3c582-141">This reference lets you call the CRT request, response, and entities.</span></span>
4. <span data-ttu-id="3c582-142">Retail Server 拡張機能プロジェクトで、NuGet パッケージ マネージャーを使用して、**Microsoft.Dynamics.Commerce.Hosting.Contracts** パッケージを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c582-142">In the Retail Server extension project, add the **Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts** package using the NuGet package manager.</span></span> <span data-ttu-id="3c582-143">NuGet パッケージは、**RetailSDK\\pkgs** フォルダにあります。</span><span class="sxs-lookup"><span data-stu-id="3c582-143">The NuGet packages can be found in the **RetailSDK\\pkgs** folder.</span></span>
5. <span data-ttu-id="3c582-144">新しい公開コントローラー クラスを作成し、**IController** からクラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="3c582-144">Create a new public controller class and extend it from **IController**.</span></span> <span data-ttu-id="3c582-145">このコントローラー クラスには、Retail Server API が公開する必要のあるメソッドが含まれているので、コントローラー クラスは公開である必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c582-145">This controller class will contain the method that the Retail Server API must expose, the controller class must be public.</span></span>
6. <span data-ttu-id="3c582-146">コントローラー クラス内で、CRT 要求を呼び出すメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="3c582-146">Inside the controller class, add methods to call the CRT request.</span></span> <span data-ttu-id="3c582-147">新しいコントローラー クラスを、**CustomerController**、**SalesOrdersController**、または **ProductController** などの既存のコントローラー クラスから拡張しないでください。</span><span class="sxs-lookup"><span data-stu-id="3c582-147">Don’t extend the new controller class from existing controller classes such as **CustomerController**, **SalesOrdersController**, or **ProductController**.</span></span> <span data-ttu-id="3c582-148">拡張クラスでは、**IController** クラスのみを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c582-148">Extension classes must extend only the **IController** class.</span></span>
7. <span data-ttu-id="3c582-149">コントローラー クラス (コントローラー クラス名) 上で **RoutePrefix** 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="3c582-149">Add the **RoutePrefix** attribute on the controller class (Controller class name).</span></span>

    ```csharp
    [RoutePrefix("SimpleExtension")]
    ```

8. <span data-ttu-id="3c582-150">コントローラー クラスで **BindEntity** 属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="3c582-150">Add the **BindEntity** attribute on the controller class.</span></span> <span data-ttu-id="3c582-151">この属性は、新しいコントローラーを作成してエンティティを公開する場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="3c582-151">This attribute is required if you're creating a new controller and exposing an entity.</span></span>

```csharp
[BindEntity(typeof(SimpleEntity))]
```

> [!NOTE]
> <span data-ttu-id="3c582-152">拡張クラスがエンティティにバインドされている場合は、手順 7 と 8 が必要です。</span><span class="sxs-lookup"><span data-stu-id="3c582-152">Steps 7 and 8 are required if the extension class is bound to an entity.</span></span> <span data-ttu-id="3c582-153">これらの手順は、エンティティではなく、単純型を返す非制限コントローラ クラスには必要ありません。</span><span class="sxs-lookup"><span data-stu-id="3c582-153">These steps are not required for an unbounded controller class returning simple types, not any entity.</span></span>

<span data-ttu-id="3c582-154">次のサンプル コードでは、エンティティ、文字列、およびブール値を返す単純な Retail Server API を作成します。</span><span class="sxs-lookup"><span data-stu-id="3c582-154">The following sample code creates a simple Retail Server API to return an entity, a string, and a bool value.</span></span> <span data-ttu-id="3c582-155">サンプルで使用されている CRT 要求および応答は、このサンプルには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="3c582-155">The CRT request and response used in the sample is not included in this sample.</span></span> <span data-ttu-id="3c582-156">CRT 要求および応答の例については、[Commerce Runtime (CRT) の拡張機能およびトリガー](commerce-runtime-extensibility-trigger.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c582-156">For an example of the CRT request and response, see [Commerce runtime (CRT) extensibility and triggers](commerce-runtime-extensibility-trigger.md).</span></span>

### <a name="sample-code-for-a-controller-class-bounded-to-a-custom-entity"></a><span data-ttu-id="3c582-157">カスタム エンティティにバインドされるコントローラ クラスのサンプルコード</span><span class="sxs-lookup"><span data-stu-id="3c582-157">Sample code for a controller class bounded to a custom entity</span></span>

> [!NOTE]
> <span data-ttu-id="3c582-158">拡張コードは、顧客や製品などの既存の OOB エンティティにバインドしてはいけません。</span><span class="sxs-lookup"><span data-stu-id="3c582-158">Extension code should not bound the existing OOB entity, such as Customer or Product.</span></span>

```csharp
// New extended controller.
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

### <a name="sample-code-for-a-controller-class-not-bounded-to-a-custom-entity"></a><span data-ttu-id="3c582-159">カスタム エンティティにバインドされていないコントローラ クラスのサンプルコード</span><span class="sxs-lookup"><span data-stu-id="3c582-159">Sample code for a controller class not bounded to a custom entity</span></span>

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

<span data-ttu-id="3c582-160">Retail Server API では、さまざまな承認ロールがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3c582-160">The Retail Server APIs support different authorization roles.</span></span> <span data-ttu-id="3c582-161">コントローラー メソッドへのアクセスは、コントローラー メソッドの **承認** 属性で指定された承認ロールに基づいて許可されます。</span><span class="sxs-lookup"><span data-stu-id="3c582-161">Access to the controller method is permitted based on the authorization roles that are specified in the controller method **Authorizations** attribute.</span></span> <span data-ttu-id="3c582-162">次の例は、サポートされている承認ロールを示しています。</span><span class="sxs-lookup"><span data-stu-id="3c582-162">The following example shows the supported authorization roles.</span></span> <span data-ttu-id="3c582-163">拡張コードは、**承認** 属性の代わりに **CommerceAuthorization** 属性を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="3c582-163">Extension code should not use the **CommerceAuthorization** attribute instead of the **Authorizations** attribute.</span></span> <span data-ttu-id="3c582-164">**CommerceAuthorization** 属性は、10.0.11 より前の SDK バージョンでのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="3c582-164">The **CommerceAuthorization** attribute is only supported in SDK versions earlier than 10.0.11.</span></span>


```csharp
// Represents the type of logon type.
[DataContract]
public static class CommerceRoles
{
    // Anonymous Role.
    [DataMember]
    public const string Anonymous = "Anonymous";

    // SharePoint Role used by Connector.
    [DataMember]
    public const string Storefront = "Storefront";

    // Employee Role.
    [DataMember]
    public const string Employee = "Employee";

    // Customer Role.
    [DataMember]
    public const string Customer = "Customer";

    // Represents the Device level of authentication.
    [DataMember]
    public const string Device = "Device";

    // Represents Application level of authentication.
    [DataMember]
    public const string Application = "Application";

    // The list of all possible Microsoft.Dynamics.Commerce.Runtime.DataModel.CommerceRoles values.
    public static readonly string[] All;
}
 ```

### <a name="register-the-extension"></a><span data-ttu-id="3c582-165">拡張機能の登録</span><span class="sxs-lookup"><span data-stu-id="3c582-165">Register the extension</span></span>

1. <span data-ttu-id="3c582-166">拡張機能プロジェクトをビルドし、バイナリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="3c582-166">Build the extension project, and copy the binary to the **\\RetailServer\\webroot\\bin\\Ext** folder.</span></span>
2. <span data-ttu-id="3c582-167">**extensionComposition** セクションで新しい拡張ライブラリ名を追加して、**\\RetailServer\\webroot** フォルダーの Commerce Scale Unit **web.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="3c582-167">Update the Commerce Scale Unit **web.config** file in the **\\RetailServer\\webroot** folder by adding the new extension library name in the **extensionComposition** section.</span></span>

    ```xml
    <extensionComposition>
        <!-- Use fully qualified assembly names for ALL if you need to support loading from the Global Assembly Cache.
        If you host in an application with a bin folder, this is not required. -->
        <add source="assembly" value="SimpleExtensionSample" >
    </extensionComposition>
    ```

3. <span data-ttu-id="3c582-168">インターネット インフォメーション サービス (IIS) で Commerce Scale Unit を再起動して、新しい拡張機能を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="3c582-168">In Internet Information Services (IIS), restart the Commerce Scale Unit to load the new extension.</span></span>

### <a name="validate-the-extension"></a><span data-ttu-id="3c582-169">拡張機能の検証</span><span class="sxs-lookup"><span data-stu-id="3c582-169">Validate the extension</span></span>

1. <span data-ttu-id="3c582-170">拡張機能が正常に読み込まれたことを確認するには、Retail Server のメタデータを参照します。</span><span class="sxs-lookup"><span data-stu-id="3c582-170">To verify that the extension loaded successfully, you can browse the Retail Server metadata.</span></span> <span data-ttu-id="3c582-171">エンティティおよびメソッドが一覧に表示されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3c582-171">Confirm that your entities and methods appear in the list.</span></span> <span data-ttu-id="3c582-172">メタデータを参照するには、Web ブラウザーの次の形式で URL を開きます。</span><span class="sxs-lookup"><span data-stu-id="3c582-172">To browse the metadata, open a URL in the following format in a web browser:</span></span>

    `https://RS-URL/Commerce/$metadata`

2. <span data-ttu-id="3c582-173">クライアントで Retail Server 拡張機能を呼び出すには、クライアント Typescript プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c582-173">To call the Retail Server extension in your client, you must generate the client Typescript proxy.</span></span> <span data-ttu-id="3c582-174">その後、プロキシを使用して、クライアントから新しい Retail Server API を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="3c582-174">You can then use the proxy to call your new Retail Server APIs from the client.</span></span>

<span data-ttu-id="3c582-175">Retail Server 拡張 API を使用して、**EdmModelExtender** ファイルを拡張機能に追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3c582-175">You don't have to add or include any **EdmModelExtender** files in the extension with the Retail Server extensions APIs.</span></span> <span data-ttu-id="3c582-176">これらのファイルは、Retail SDK バージョン 10.0.10 またはそれ以前を使用している場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="3c582-176">The files are required only if you're using Retail SDK version 10.0.10 or earlier.</span></span>

### <a name="debugging-rs-extension"></a><span data-ttu-id="3c582-177">RS 拡張機能のデバッグ</span><span class="sxs-lookup"><span data-stu-id="3c582-177">Debugging RS extension</span></span>

<span data-ttu-id="3c582-178">Visual Studio で RS 拡張機能プロジェクトをデバッグする方法。</span><span class="sxs-lookup"><span data-stu-id="3c582-178">To debug the RS extension project in Visual Studio.</span></span> <span data-ttu-id="3c582-179">**デバッグ > プロセスに添付する** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3c582-179">Go to **Debug > Attach to Process**.</span></span> <span data-ttu-id="3c582-180">w3wp.exe (Retail Server の IIS プロセス) を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c582-180">Select w3wp.exe (the IIS process for Retail Server).</span></span> <span data-ttu-id="3c582-181">複数の w3wp.exe プロセスがある場合は、プロセス ID に基づいて適切なプロセスを使用します。</span><span class="sxs-lookup"><span data-stu-id="3c582-181">If there are multiple w3wp.exe processes, use the correct process based on the process ID.</span></span> <span data-ttu-id="3c582-182">Retail サーバー プロセス IDは、**IIS > ワーカー プロセス** を使用するか、コマンド プロンプトと tasklist コマンドを使用して見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="3c582-182">The retail server process ID can be found using **IIS > Worker processes** or by using the command prompt and the tasklist command.</span></span>

## <a name="generate-the-typescript-proxy-for-pos"></a><span data-ttu-id="3c582-183">POS Typescript プロキシの生成</span><span class="sxs-lookup"><span data-stu-id="3c582-183">Generate the Typescript proxy for POS</span></span>

<span data-ttu-id="3c582-184">POS は Typescript プロキシ を使って、Retail サーバー API や CRT エンティティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3c582-184">The POS uses the Typescript proxy to access the Retail Server APIs and CRT entities.</span></span> <span data-ttu-id="3c582-185">プロキシ クラスは、サービスを実行するためのクラスまたは Wrapper として機能し、プロキシ拡張機能を使用せずに Retail Server API やエンティティ メタデータを検索することによって、Retail Server API にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3c582-185">The proxy class acts as manger class or wrapper to access the Retail server APIs without the proxy extension manually finding the Retail server API and entities metadata.</span></span>

### <a name="steps-to-generate-the-proxy-files"></a><span data-ttu-id="3c582-186">プロキシ ファイルを生成する手順</span><span class="sxs-lookup"><span data-stu-id="3c582-186">Steps to generate the proxy files</span></span>

1. <span data-ttu-id="3c582-187">Visual Studio 2017 では、サンプル プロキシ テンプレート プロジェクトを Visual Studio 2017 の **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** から開きます。</span><span class="sxs-lookup"><span data-stu-id="3c582-187">In Visual Studio 2017, open the sample proxy template project from **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** in Visual Studio 2017.</span></span> <span data-ttu-id="3c582-188">新しい名前が必要な場合は、プロジェクトの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="3c582-188">Rename the project if a new name is required.</span></span>
2. <span data-ttu-id="3c582-189">このプロキシ テンプレート プロジェクトに、Retail Server 拡張プロジェクトをプロジェクト参照プロジェクトとして追加します。</span><span class="sxs-lookup"><span data-stu-id="3c582-189">Add the Retail Server extension project to this proxy template project as a project reference project.</span></span> <span data-ttu-id="3c582-190">既存の **StoreHoursSample** プロジェクト参照を削除します。</span><span class="sxs-lookup"><span data-stu-id="3c582-190">Remove the existing **StoreHoursSample** project reference.</span></span>
3. <span data-ttu-id="3c582-191">**Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** プロジェクトを右クリックし、**Edit Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3c582-191">Right-click the **Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj** project, and then select **Edit Proxies.TypeScriptProxy.Extensions.StoreHoursSample.csproj**.</span></span>
4. <span data-ttu-id="3c582-192">**\<RetailServerExtensionAssemblies\>** ノードの下に、Retail Server 拡張機能のアセンブリ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="3c582-192">Under the **\<RetailServerExtensionAssemblies\>** node, specify your extension Retail Server assembly name.</span></span> <span data-ttu-id="3c582-193">次の例は、アセンブリ名を追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3c582-193">The following example shows how to add the assembly name.</span></span>

    ```xml
    <ItemGroup>
        <RetailServerExtensionAssemblies Include="..\..\RetailServer\Extensions.Sample\bin\$(Configuration)\net461\$(AssemblyNamePrefix).RetailServer.Extension.Sample.dll" />
    </ItemGroup>
    ```

5. <span data-ttu-id="3c582-194">**\<Copy\>** ノードの下で、POS 拡張フォルダーの **DestinationFolder** パスを更新して、生成されたプロキシファイルが POS 拡張フォルダーに自動的にコピーされるようにします。</span><span class="sxs-lookup"><span data-stu-id="3c582-194">Under the **\<Copy\>** node, update the **DestinationFolder** path of your POS extension folder, so that generated proxy files are automatically copied to the POS extension folder automatically.</span></span> <span data-ttu-id="3c582-195">生成されたプロキシ ファイルも **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="3c582-195">The generated proxy files will also be copied to **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService**.</span></span> <span data-ttu-id="3c582-196">次の例は、パスを更新する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3c582-196">The following example shows how to update the path.</span></span>

    ```xml
    <Copy SourceFiles="@(GeneratedDataServiceContracts)" DestinationFolder="$(SdkRootPath)\POS\Extensions\Sample\DataService" SkipUnchangedFiles="true" />
    ```

6. <span data-ttu-id="3c582-197">変更が完了したら、プロキシ プロジェクトをビルドして TypeScript プロキシ ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="3c582-197">After the changes are completed, build the proxy project to generate the TypeScript proxy files.</span></span> <span data-ttu-id="3c582-198">ビルドが完了すると、**\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** フォルダーでプロキシ ファイルが使用可能となり、そのフォルダーは **コピー** コマンドによって指定されます。</span><span class="sxs-lookup"><span data-stu-id="3c582-198">When the build is completed, the proxy files will be available in the **\\RetailSDK\\Code\\SampleExtensions\\TypeScriptProxy\\TypeScriptProxy.Extensions.StoreHoursSample\\DataService** folder and the folder that is specified in the **Copy** command.</span></span> <span data-ttu-id="3c582-199">パスとフォルダー パスは、フォルダ構造によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3c582-199">The path and folder path can vary, depending on the folder structure.</span></span>

## <a name="retail-server-extension-in-offline"></a><span data-ttu-id="3c582-200">オフラインの Retail Server 拡張機能</span><span class="sxs-lookup"><span data-stu-id="3c582-200">Retail server extension in offline</span></span>

<span data-ttu-id="3c582-201">**Microsoft.Dynamics.Commerce.Hosting.Contracts** API を使用してビルトされた Retail Server 拡張機能は、オフライン実装でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="3c582-201">A Retail Server extension built using the **Microsoft.Dynamics.Commerce.Runtime.Hosting.Contracts** API can be used in an offline implementation.</span></span> <span data-ttu-id="3c582-202">個別の C# プロキシ ライブラリを生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="3c582-202">You don't need to generate a separate C# proxy library.</span></span> <span data-ttu-id="3c582-203">**\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** フォルダーにある Retail Server 拡張機能ライブラリをコピーして、 **RetailProxy.MPOSOffline.ext** 構成ファイルにこのライブラリを含めるように構成します。</span><span class="sxs-lookup"><span data-stu-id="3c582-203">Copy the Retail Server extension library in the **\\Microsoft Dynamics 365\\70\\Retail Modern POS\\ClientBroker\\ext** folder and update the **RetailProxy.MPOSOffline.ext** config file to include the this library.</span></span> <span data-ttu-id="3c582-204">この拡張機能では、Typescript プロキシのみを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c582-204">This extension must only generate the Typescript proxy.</span></span> <span data-ttu-id="3c582-205">SDK サンプルは、**\\RetailSDK\\SampleExtensions\\TypeScriptProxy)** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="3c582-205">SDK samples can be found in the  **\\RetailSDK\\SampleExtensions\\TypeScriptProxy)** folder.</span></span>

<span data-ttu-id="3c582-206">次の例は、**RetailProxy.MPOSOffline.ext** 構成ファイル内の要素の **追加** を更新する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3c582-206">The following example shows how to update the **add** element in the **RetailProxy.MPOSOffline.ext** configuration  file.</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?> 
<retailProxyExtensions> 
    <composition> 
        <add source="assembly" value="Contoso.RetailServer.StoreHoursSample" /> 
    </composition> 
</retailProxyExtensions> 
```

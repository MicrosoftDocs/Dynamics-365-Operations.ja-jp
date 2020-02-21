---
title: 新しい Retail Server 拡張機能の作成
description: このトピックでは、新しい Commerce Scale Unit 拡張機能の作成方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 08/25/2019
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
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 0dcfb0fd1821f6a132e2df628c1d8ae96196f794
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004629"
---
# <a name="create-a-new-retail-server-extension"></a><span data-ttu-id="cb1d2-103">新しい Retail Server 拡張機能の作成</span><span class="sxs-lookup"><span data-stu-id="cb1d2-103">Create a new Retail Server extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb1d2-104">このドキュメントでは、新しい Commerce Scale Unit アプリケーション プログラミング インターフェイス (API) の作成方法、および POS または他のクライアントがそれを使用できるようにするための公開方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-104">This document explains how to create a new Commerce Scale Unit application programming interface (API), and how to expose it so that POS or other clients can consume it.</span></span> <span data-ttu-id="cb1d2-105">既存の Commerce Scale Unit API の変更はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-105">Modification of the existing Commerce Scale Unit APIs isn't supported.</span></span>

<span data-ttu-id="cb1d2-106">Retail ソフトウェア開発キット (SDK) には、Commerce Runtime (CRT) を含む、エンドツーエンドの Commerce Scale Unit 拡張機能のサンプルがいくつか用意されているのみです。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-106">The Retail software development kit (SDK) includes only a few samples of end-to-end Commerce Scale Unit extensions that include the Commerce Runtime (CRT).</span></span> <span data-ttu-id="cb1d2-107">これらのサンプルをテンプレートとして使用して、拡張機能を起動できます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-107">You can use these samples as templates to start your extensions.</span></span> <span data-ttu-id="cb1d2-108">サンプル拡張機能は、RetailSDK\\SampleExtensions\\RetailServer フォルダーで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-108">You can find the sample extensions in the RetailSDK\\SampleExtensions\\RetailServer folder.</span></span>

## <a name="end-to-end-sample-repository-in-the-retail-sdk"></a><span data-ttu-id="cb1d2-109">Retail SDK のエンドツーエンド サンプル リポジトリ</span><span class="sxs-lookup"><span data-stu-id="cb1d2-109">End-to-end sample repository in the Retail SDK</span></span>

| <span data-ttu-id="cb1d2-110">サンプル拡張機能</span><span class="sxs-lookup"><span data-stu-id="cb1d2-110">Sample extension</span></span><br><span data-ttu-id="cb1d2-111">(RetailSDK\\SampleExtensions\\RetailServer)</span><span class="sxs-lookup"><span data-stu-id="cb1d2-111">(RetailSDK\\SampleExtensions\\RetailServer)</span></span> | <span data-ttu-id="cb1d2-112">CRT サンプル</span><span class="sxs-lookup"><span data-stu-id="cb1d2-112">CRT sample</span></span><br><span data-ttu-id="cb1d2-113">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span><span class="sxs-lookup"><span data-stu-id="cb1d2-113">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span></span> | <span data-ttu-id="cb1d2-114">POS サンプル</span><span class="sxs-lookup"><span data-stu-id="cb1d2-114">POS sample</span></span><br><span data-ttu-id="cb1d2-115">(RetailSDK\\POS\\Extensions)</span><span class="sxs-lookup"><span data-stu-id="cb1d2-115">(RetailSDK\\POS\\Extensions)</span></span> |
|---------------------------------------------|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="cb1d2-116">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-116">Extensions.StoreHoursSample</span></span>                 | <span data-ttu-id="cb1d2-117">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-117">Extensions.StoreHoursSample</span></span>                | <span data-ttu-id="cb1d2-118">StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-118">StoreHoursSample</span></span>                       |
| <span data-ttu-id="cb1d2-119">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-119">Extensions.SalesTransactionSignatureSample</span></span>  | <span data-ttu-id="cb1d2-120">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-120">Extensions.SalesTransactionSignatureSample</span></span> | <span data-ttu-id="cb1d2-121">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-121">SalesTransactionSignatureSample</span></span>        |
| <span data-ttu-id="cb1d2-122">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-122">Extensions.PrintPackingSlipSample</span></span>           | <span data-ttu-id="cb1d2-123">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-123">Extensions.PrintPackingSlipSample</span></span>          |                                        |
| <span data-ttu-id="cb1d2-124">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-124">Extensions.CrossLoyaltySample</span></span>               | <span data-ttu-id="cb1d2-125">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="cb1d2-125">Extensions.CrossLoyaltySample</span></span>              |                                        |

## <a name="create-a-new-extension"></a><span data-ttu-id="cb1d2-126">新しい拡張機能の作成</span><span class="sxs-lookup"><span data-stu-id="cb1d2-126">Create a new extension</span></span>

<span data-ttu-id="cb1d2-127">このセクションの手順に従って、新しい Commerce Scale Unit 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-127">Follow the steps in this section to create a new Commerce Scale Unit extension.</span></span>

### <a name="end-to-end-flow"></a><span data-ttu-id="cb1d2-128">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="cb1d2-128">End-to-end flow</span></span>

<span data-ttu-id="cb1d2-129">次の図は、拡張機能のフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-129">The following illustration shows the flow of the extension.</span></span>

![Commerce Scale Unit の拡張機能フロー](media/RSExtensionFlow.png)

### <a name="extension-class-diagram"></a><span data-ttu-id="cb1d2-131">拡張機能クラス ダイアグラム</span><span class="sxs-lookup"><span data-stu-id="cb1d2-131">Extension class diagram</span></span>

<span data-ttu-id="cb1d2-132">次の図は、拡張機能のクラス ダイアグラムを示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-132">The following illustration shows the class structure of the extension.</span></span>

![Commerce Scale Unit の拡張機能クラス ダイアグラム](media/RSClassFlow.png)

### <a name="steps"></a><span data-ttu-id="cb1d2-134">ステップ</span><span class="sxs-lookup"><span data-stu-id="cb1d2-134">Steps</span></span>

1. <span data-ttu-id="cb1d2-135">Commerce Scale Unit 拡張機能を作成する前に、CRT 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-135">Before you create the Commerce Scale Unit extension, create the CRT extension.</span></span> <span data-ttu-id="cb1d2-136">Commerce Scale Unit API には、パラメーターで CRT を呼び出すロジック以外のロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-136">Commerce Scale Unit APIs should have no logic except logic that calls the CRT with the parameters.</span></span>
2. <span data-ttu-id="cb1d2-137">Microsoft .NET フレームワーク バージョン 4.6.1 以降をターゲット フレームワークとして使用する、新しい C\#クラス ライブラリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-137">Create a new C\# class library project that uses the Microsoft .NET Framework version 4.6.1 or later as the target framework.</span></span>
3. <span data-ttu-id="cb1d2-138">Commerce Scale Unit 拡張機能プロジェクトで、CRT 拡張機能ライブラリまたはプロジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-138">In the Commerce Scale Unit extension project, add a reference to your CRT extension library or project.</span></span> <span data-ttu-id="cb1d2-139">この参照を使用して、CRT 要求と応答を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-139">This reference lets you call the CRT request and response.</span></span> <span data-ttu-id="cb1d2-140">また、Commerce Scale Unit 拡張機能プロジェクトからのエンティティを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-140">It also lets you use the entities from the Commerce Scale Unit extension project.</span></span>
4. <span data-ttu-id="cb1d2-141">Commerce Scale Unit 拡張機能プロジェクトで、**NonBindableOperationController** または **CommerceController** を拡張する新しいコントローラー クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-141">In the Commerce Scale Unit extension project, create a new controller class that extends **NonBindableOperationController** or **CommerceController**.</span></span> <span data-ttu-id="cb1d2-142">基本クラスは、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-142">The base class depends on your scenario.</span></span> <span data-ttu-id="cb1d2-143">このコントローラー クラスには、Commerce Scale Unit API によって公開される必要のあるメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-143">This controller class will contain the method that must be exposed by the Commerce Scale Unit API.</span></span> <span data-ttu-id="cb1d2-144">コントローラー クラス内で、CRT 要求を呼び出すメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-144">Inside the controller class, add methods to call the CRT request.</span></span>

    ```C#
    /// <summary>;
    /// The controller to retrieve a new entity.
    /// <summary>
    [ComVisible(false)]
    public class SampleController : CommerceController<SampleEntity, long>;
    {
        ///<summary>;
        /// Gets the controller name used to load extended controller.
        /// <summary>
        public override string ControllerName
        {
            get { return "SampleEntity"; }
        }
        /// <summary>;
        /// Gets the sample entity.
        /// <summary>;
        /// <param name="parameters">The parameters to this action.</param>
        /// <returns>The list of sample entity.</returns>
        [HttpPost]
        [CommerceAuthorization(CommerceRoles.Anonymous, CommerceRoles.Customer, CommerceRoles.Device, CommerceRoles.Employee)]
        public System.Web.OData.PageResult<SampleEntity> GetSampleEntity(ODataActionParameters parameters)
        {
            if (parameters == null)
            {
                throw new ArgumentNullException("parameters");
            }
            var runtime = CommerceRuntimeManager.CreateRuntime(this.CommercePrincipal);
            QueryResultSettings queryResultSettings = QueryResultSettings.SingleRecord;
            queryResultSettings.Paging = new PagingInfo(10);
            var request = new CRTDataRequest((string)parameters["key"]) { QueryResultSettings = queryResultSettings };
            PagedResult<SampleEntity> sample = runtime.Execute<CRTDataResponse>(request, null);
            return this.ProcessPagedResults(sample);
        }
    }
    ```

5. <span data-ttu-id="cb1d2-145">**IEdmModelExtender** インターフェイスを拡張する **EdmModelExtender** (EDM) クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-145">Create an **EdmModelExtender** (EDM) class that extends the **IEdmModelExtender** interface.</span></span> <span data-ttu-id="cb1d2-146">このクラスには、Commerce Scale Unit API が公開するデータを説明するために使用される抽象データ モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-146">This class contains the abstract data model that is used to describe the data that a Commerce Scale Unit API exposes.</span></span> <span data-ttu-id="cb1d2-147">オープン データ プロトコル (OData) メタデータ ドキュメントは、クライアントの消費に対して公開されるサービスのデータ モデルを表したものです。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-147">An Open Data Protocol (OData) Metadata Document is a representation of a service's data model that is exposed for client consumption.</span></span> <span data-ttu-id="cb1d2-148">EDM の中心となる概念は、エンティティ、リレーションシップ、エンティティ セット、アクション、および機能です。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-148">The central concepts in the EDM are entities, relationships, entity sets, actions, and functions.</span></span>

    <span data-ttu-id="cb1d2-149">**IEdmModelExtender** インターフェイスには、抽象 **ExtendModel** メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-149">The **IEdmModelExtender** interface contains the abstract **ExtendModel** method.</span></span> <span data-ttu-id="cb1d2-150">このインターフェイスを拡張する場合、**ExtendModel** メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-150">When you extend this interface, you must implement the **ExtendModel** method.</span></span> <span data-ttu-id="cb1d2-151">**ExtendModel** メソッド内で、**CommerceModelBuilder** クラスを使用してクライアントに公開される EDM エンティティおよび機能を構築します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-151">Inside the **ExtendModel** method, you build the EDM entities and functions that will be exposed to the client by using the **CommerceModelBuilder** class.</span></span>

    <span data-ttu-id="cb1d2-152">**CommerceModelBuilder** クラスには、エンティティおよび機能を構築するのに使用される構築メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-152">The **CommerceModelBuilder** class contains the build method that is used to build the entities and functions.</span></span>

    | <span data-ttu-id="cb1d2-153">メソッド名</span><span class="sxs-lookup"><span data-stu-id="cb1d2-153">Method name</span></span>                                                                 | <span data-ttu-id="cb1d2-154">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="cb1d2-154">Return type</span></span>                              | <span data-ttu-id="cb1d2-155">説明</span><span class="sxs-lookup"><span data-stu-id="cb1d2-155">Description</span></span> |
    |-----------------------------------------------------------------------------|------------------------------------------|-------------|
    | <span data-ttu-id="cb1d2-156">BuildEntity\<TEntity\>() where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-156">BuildEntity\<TEntity\>() where TEntity : class</span></span>                              | <span data-ttu-id="cb1d2-157">EntityTypeConfiguration\<TEntity\></span><span class="sxs-lookup"><span data-stu-id="cb1d2-157">EntityTypeConfiguration\<TEntity\></span></span>       | <span data-ttu-id="cb1d2-158">このメソッドがエンティティを構築します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-158">This method builds an entity.</span></span> |
    | <span data-ttu-id="cb1d2-159">BuildEntitySet\<TEntity\>(string entitySetName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-159">BuildEntitySet\<TEntity\>(string entitySetName) where TEntity : class</span></span>       | <span data-ttu-id="cb1d2-160">EntitySetConfiguration\<TEntity\></span><span class="sxs-lookup"><span data-stu-id="cb1d2-160">EntitySetConfiguration\<TEntity\></span></span>        | <span data-ttu-id="cb1d2-161">このメソッドがエンティティ セットを構築します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-161">This method builds an entity set.</span></span> |
    | <span data-ttu-id="cb1d2-162">BuildComplexType\<TComplexType\>() where TComplexType : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-162">BuildComplexType\<TComplexType\>() where TComplexType : class</span></span>               | <span data-ttu-id="cb1d2-163">ComplexTypeConfiguration\<TComplexType\></span><span class="sxs-lookup"><span data-stu-id="cb1d2-163">ComplexTypeConfiguration\<TComplexType\></span></span> | <span data-ttu-id="cb1d2-164">このメソッドが、複雑なエンティティ タイプを構築します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-164">This method builds a complex entity type.</span></span> |
    | <span data-ttu-id="cb1d2-165">BuildEnumType\<TEnumType\>()</span><span class="sxs-lookup"><span data-stu-id="cb1d2-165">BuildEnumType\<TEnumType\>()</span></span>                                                | <span data-ttu-id="cb1d2-166">EnumTypeConfiguration\<TEnumType\></span><span class="sxs-lookup"><span data-stu-id="cb1d2-166">EnumTypeConfiguration\<TEnumType\></span></span>       | <span data-ttu-id="cb1d2-167">このメソッドが、列挙型を構築します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-167">This method builds an enumeration type.</span></span> |
    | <span data-ttu-id="cb1d2-168">BindAction(string actionName)</span><span class="sxs-lookup"><span data-stu-id="cb1d2-168">BindAction(string actionName)</span></span>                                               | <span data-ttu-id="cb1d2-169">ActionConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb1d2-169">ActionConfiguration</span></span>                      | <span data-ttu-id="cb1d2-170">このメソッドが、モデル ビルダーのアクションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-170">This method binds an action in the model builder.</span></span> <span data-ttu-id="cb1d2-171">アクションは HTTP POST 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-171">An action represents an HTTP POST request.</span></span> |
    | <span data-ttu-id="cb1d2-172">BindEntityAction\<TEntity\>(string actionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-172">BindEntityAction\<TEntity\>(string actionName) where TEntity : class</span></span>        | <span data-ttu-id="cb1d2-173">ActionConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb1d2-173">ActionConfiguration</span></span>                      | <span data-ttu-id="cb1d2-174">このメソッドが、モデルのエンティティ アクションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-174">This method binds an entity action of the model.</span></span> <span data-ttu-id="cb1d2-175">アクションは HTTP POST 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-175">An action represents an HTTP POST request.</span></span> |
    | <span data-ttu-id="cb1d2-176">BindEntitySetAction\<TEntity\>(string actionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-176">BindEntitySetAction\<TEntity\>(string actionName) where TEntity : class</span></span>     | <span data-ttu-id="cb1d2-177">ActionConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb1d2-177">ActionConfiguration</span></span>                      | <span data-ttu-id="cb1d2-178">このメソッドがエンティティ セット アクションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-178">This method binds an entity set action.</span></span> <span data-ttu-id="cb1d2-179">アクションは HTTP POST 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-179">An action represents an HTTP POST request.</span></span>             |
    | <span data-ttu-id="cb1d2-180">BindFunction(string functionName)</span><span class="sxs-lookup"><span data-stu-id="cb1d2-180">BindFunction(string functionName)</span></span>                                           | <span data-ttu-id="cb1d2-181">FunctionConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb1d2-181">FunctionConfiguration</span></span>                    | <span data-ttu-id="cb1d2-182">このメソッドが、モデル ビルダーの機能をバインドします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-182">This method binds a function in the model builder.</span></span> <span data-ttu-id="cb1d2-183">機能は HTTP GET 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-183">A function represents a HTTP GET request.</span></span> |
    | <span data-ttu-id="cb1d2-184">BindEntityFunction\<TEntity\>(string functionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-184">BindEntityFunction\<TEntity\>(string functionName) where TEntity : class</span></span>    | <span data-ttu-id="cb1d2-185">FunctionConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb1d2-185">FunctionConfiguration</span></span>                    | <span data-ttu-id="cb1d2-186">このメソッドが、モデルのエンティティ機能をバインドします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-186">This method binds an entity function of the model.</span></span> <span data-ttu-id="cb1d2-187">機能は HTTP GET 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-187">A function represents an HTTP GET request.</span></span> |
    | <span data-ttu-id="cb1d2-188">BindEntitySetFunction\<TEntity\>(string functionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="cb1d2-188">BindEntitySetFunction\<TEntity\>(string functionName) where TEntity : class</span></span> | <span data-ttu-id="cb1d2-189">FunctionConfiguration</span><span class="sxs-lookup"><span data-stu-id="cb1d2-189">FunctionConfiguration</span></span>                    | <span data-ttu-id="cb1d2-190">このメソッドがエンティティ セット機能をバインドします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-190">This method binds an entity set function.</span></span> <span data-ttu-id="cb1d2-191">機能は HTTP GET 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-191">A function represents an HTTP GET request.</span></span> |

    <span data-ttu-id="cb1d2-192">次の例は、EDM モデルを拡張する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-192">The following example shows how to extend the EDM model.</span></span>

    ```C#
    /// <summary>;
    /// The class to extend the EDM model.
    /// <summary>;
    [Export(typeof(IEdmModelExtender))]
    [ComVisible(false)]
    public class EdmModelExtender : IEdmModelExtender
    {
        /// <summary>;
        /// Extends the EDM model.
        /// <summary>;
        /// <param name="builder">The builder to build the EDM model.</param>
        public void ExtendModel(CommerceModelBuilder builder)
        {
            ThrowIf.Null(builder, "builder");
            // Extends entity sets.
            builder.BuildEntitySet<SampleEntity>("SampleEntity");
            // Extends entity set actions.
            var action = builder.BindEntitySetAction<SampleDataModel.StoreDayHours>("GetSampleEntity");
            action.Parameter<string>("Key");
            action.ReturnsCollectionFromEntitySet<SampleEntity>("SampleEntity");
        }
    }
    ```

6. <span data-ttu-id="cb1d2-193">拡張機能プロジェクトをビルドし、バイナリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーにドロップします。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-193">Build the extension project, and drop the binary into the **\\RetailServer\\webroot\\bin\\Ext** folder.</span></span>
7. <span data-ttu-id="cb1d2-194">**extensionComposition** セクションで新しい Commerce Scale Unit 拡張ライブラリ名を追加して、**\\RetailServer\\Webroot** フォルダーの Commerce Scale Unit web.config ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-194">Update the Commerce Scale Unit web.config file in the **\\RetailServer\\webroot** folder by adding the new extension library name in the **extensionComposition** section.</span></span>

    ```
    <extensionComposition>
    <!-- Please use fully qualified assembly names for ALL if you need to support loading from the Global Assembly Cache.
    If you host in an application with a bin folder, this is not required. -->
    <add source="assembly" value="SampleExtension" >;
    </extensionComposition>
    ```

8. <span data-ttu-id="cb1d2-195">Microsoft インターネット インフォメーション サービス (IIS) で、Commerce Scale Unit を再起動して、新しい拡張機能を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-195">In Microsoft Internet Information Services (IIS), restart Commerce Scale Unit to load the new extension.</span></span>
9. <span data-ttu-id="cb1d2-196">拡張機能が正常に読み込まれたことを確認するには、Commerce Scale Unit メタデータを参照し、エンティティとメソッドがリストに表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-196">To verify that the extension was successfully loaded, you can browse the Commerce Scale Unit metadata, and confirm that your entities and methods appear in the list.</span></span>

    <span data-ttu-id="cb1d2-197">メタデータを参照するには、Web ブラウザーの次の形式で URL を開きます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-197">To browse the metadata, open a URL in the following format in a web browser:</span></span>

    `https://Your Commerce Scale Unit URL/Commerce/$metadata`

10. <span data-ttu-id="cb1d2-198">クライアントで Commerce Scale Unit 拡張機能を呼び出すには、Commerce プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-198">To call the Commerce Scale Unit extension in your client, you must generate the Commerce proxy.</span></span> <span data-ttu-id="cb1d2-199">その後、プロキシを使用して、クライアントから新しい Commerce Scale Unit API を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-199">You can then use the proxy to call your new Commerce Scale Unit APIs from the client.</span></span>

    <span data-ttu-id="cb1d2-200">プロキシの生成方法については、[Retail プロキシの生成](typescript-proxy-retail-pos.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cb1d2-200">For information about how to generate the proxy, see [Generate Retail proxy](typescript-proxy-retail-pos.md).</span></span>

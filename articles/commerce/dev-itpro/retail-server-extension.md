---
title: 新しい Retail Server 拡張機能の作成
description: このトピックでは、新しい Commerce Scale Unit 拡張機能の作成方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 04/13/2020
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
ms.openlocfilehash: 1bb5d59bbd4e4d247b6747b9fe40579e89ba7327
ms.sourcegitcommit: dbff1c6bb371a443a0cd2a310f5a48d5c21b08ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2020
ms.locfileid: "3259598"
---
# <a name="create-a-new-retail-server-extension"></a><span data-ttu-id="6c127-103">新しい Retail Server 拡張機能の作成</span><span class="sxs-lookup"><span data-stu-id="6c127-103">Create a new Retail Server extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c127-104">このドキュメントでは、新しい Commerce Scale Unit アプリケーション プログラミング インターフェイス (API) の作成方法、および POS または他のクライアントがそれを使用できるようにするための公開方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6c127-104">This document explains how to create a new Commerce Scale Unit application programming interface (API), and how to expose it so that POS or other clients can consume it.</span></span> <span data-ttu-id="6c127-105">既存の Commerce Scale Unit API の変更はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6c127-105">Modification of the existing Commerce Scale Unit APIs isn't supported.</span></span>

<span data-ttu-id="6c127-106">Retail ソフトウェア開発キット (SDK) には、Commerce Runtime (CRT) を含む、エンドツーエンドの Commerce Scale Unit 拡張機能のサンプルがいくつか用意されているのみです。</span><span class="sxs-lookup"><span data-stu-id="6c127-106">The Retail software development kit (SDK) includes only a few samples of end-to-end Commerce Scale Unit extensions that include the Commerce Runtime (CRT).</span></span> <span data-ttu-id="6c127-107">これらのサンプルをテンプレートとして使用して、拡張機能を起動できます。</span><span class="sxs-lookup"><span data-stu-id="6c127-107">You can use these samples as templates to start your extensions.</span></span> <span data-ttu-id="6c127-108">サンプル拡張機能は、RetailSDK\\SampleExtensions\\RetailServer フォルダーで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="6c127-108">You can find the sample extensions in the RetailSDK\\SampleExtensions\\RetailServer folder.</span></span>

## <a name="end-to-end-sample-repository-in-the-retail-sdk"></a><span data-ttu-id="6c127-109">Retail SDK のエンドツーエンド サンプル リポジトリ</span><span class="sxs-lookup"><span data-stu-id="6c127-109">End-to-end sample repository in the Retail SDK</span></span>

| <span data-ttu-id="6c127-110">サンプル拡張機能</span><span class="sxs-lookup"><span data-stu-id="6c127-110">Sample extension</span></span><br><span data-ttu-id="6c127-111">(RetailSDK\\SampleExtensions\\RetailServer)</span><span class="sxs-lookup"><span data-stu-id="6c127-111">(RetailSDK\\SampleExtensions\\RetailServer)</span></span> | <span data-ttu-id="6c127-112">CRT サンプル</span><span class="sxs-lookup"><span data-stu-id="6c127-112">CRT sample</span></span><br><span data-ttu-id="6c127-113">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span><span class="sxs-lookup"><span data-stu-id="6c127-113">(RetailSDK\\SampleExtensions\\CommerceRuntime)</span></span> | <span data-ttu-id="6c127-114">POS サンプル</span><span class="sxs-lookup"><span data-stu-id="6c127-114">POS sample</span></span><br><span data-ttu-id="6c127-115">(RetailSDK\\POS\\Extensions)</span><span class="sxs-lookup"><span data-stu-id="6c127-115">(RetailSDK\\POS\\Extensions)</span></span> |
|---------------------------------------------|--------------------------------------------|----------------------------------------|
| <span data-ttu-id="6c127-116">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="6c127-116">Extensions.StoreHoursSample</span></span>                 | <span data-ttu-id="6c127-117">Extensions.StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="6c127-117">Extensions.StoreHoursSample</span></span>                | <span data-ttu-id="6c127-118">StoreHoursSample</span><span class="sxs-lookup"><span data-stu-id="6c127-118">StoreHoursSample</span></span>                       |
| <span data-ttu-id="6c127-119">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="6c127-119">Extensions.SalesTransactionSignatureSample</span></span>  | <span data-ttu-id="6c127-120">Extensions.SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="6c127-120">Extensions.SalesTransactionSignatureSample</span></span> | <span data-ttu-id="6c127-121">SalesTransactionSignatureSample</span><span class="sxs-lookup"><span data-stu-id="6c127-121">SalesTransactionSignatureSample</span></span>        |
| <span data-ttu-id="6c127-122">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="6c127-122">Extensions.PrintPackingSlipSample</span></span>           | <span data-ttu-id="6c127-123">Extensions.PrintPackingSlipSample</span><span class="sxs-lookup"><span data-stu-id="6c127-123">Extensions.PrintPackingSlipSample</span></span>          |                                        |
| <span data-ttu-id="6c127-124">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="6c127-124">Extensions.CrossLoyaltySample</span></span>               | <span data-ttu-id="6c127-125">Extensions.CrossLoyaltySample</span><span class="sxs-lookup"><span data-stu-id="6c127-125">Extensions.CrossLoyaltySample</span></span>              |                                        |

## <a name="create-a-new-extension"></a><span data-ttu-id="6c127-126">新しい拡張機能の作成</span><span class="sxs-lookup"><span data-stu-id="6c127-126">Create a new extension</span></span>

<span data-ttu-id="6c127-127">このセクションの手順に従って、新しい Commerce Scale Unit 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="6c127-127">Follow the steps in this section to create a new Commerce Scale Unit extension.</span></span>

### <a name="end-to-end-flow"></a><span data-ttu-id="6c127-128">エンド ツー エンド フロー</span><span class="sxs-lookup"><span data-stu-id="6c127-128">End-to-end flow</span></span>

<span data-ttu-id="6c127-129">次の図は、拡張機能のフローを示しています。</span><span class="sxs-lookup"><span data-stu-id="6c127-129">The following illustration shows the flow of the extension.</span></span>

![Commerce Scale Unit の拡張機能フロー](media/RSExtensionFlow.png)

### <a name="extension-class-diagram"></a><span data-ttu-id="6c127-131">拡張機能クラス ダイアグラム</span><span class="sxs-lookup"><span data-stu-id="6c127-131">Extension class diagram</span></span>

<span data-ttu-id="6c127-132">次の図は、拡張機能のクラス ダイアグラムを示しています。</span><span class="sxs-lookup"><span data-stu-id="6c127-132">The following illustration shows the class structure of the extension.</span></span>

![Commerce Scale Unit の拡張機能クラス ダイアグラム](media/RSClassFlow.png)

### <a name="steps"></a><span data-ttu-id="6c127-134">ステップ</span><span class="sxs-lookup"><span data-stu-id="6c127-134">Steps</span></span>

1. <span data-ttu-id="6c127-135">Commerce Scale Unit 拡張機能を作成する前に、CRT 拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="6c127-135">Before you create the Commerce Scale Unit extension, create the CRT extension.</span></span> <span data-ttu-id="6c127-136">Commerce Scale Unit API には、パラメーターで CRT を呼び出すロジック以外のロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="6c127-136">Commerce Scale Unit APIs should have no logic except logic that calls the CRT with the parameters.</span></span>
2. <span data-ttu-id="6c127-137">Microsoft .NET フレームワーク バージョン 4.6.1 以降をターゲット フレームワークとして使用する、新しい C\#クラス ライブラリ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c127-137">Create a new C\# class library project that uses the Microsoft .NET Framework version 4.6.1 or later as the target framework.</span></span>
3. <span data-ttu-id="6c127-138">Commerce Scale Unit 拡張機能プロジェクトで、CRT 拡張機能ライブラリまたはプロジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="6c127-138">In the Commerce Scale Unit extension project, add a reference to your CRT extension library or project.</span></span> <span data-ttu-id="6c127-139">この参照を使用して、CRT 要求と応答を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="6c127-139">This reference lets you call the CRT request and response.</span></span> <span data-ttu-id="6c127-140">また、Commerce Scale Unit 拡張機能プロジェクトからのエンティティを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="6c127-140">It also lets you use the entities from the Commerce Scale Unit extension project.</span></span>
4. <span data-ttu-id="6c127-141">Commerce Scale Unit 拡張機能プロジェクトで、**NonBindableOperationController** または **CommerceController** を拡張する新しいコントローラー クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c127-141">In the Commerce Scale Unit extension project, create a new controller class that extends **NonBindableOperationController** or **CommerceController**.</span></span> <span data-ttu-id="6c127-142">基本クラスは、シナリオによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6c127-142">The base class depends on your scenario.</span></span> <span data-ttu-id="6c127-143">このコントローラー クラスには、Commerce Scale Unit API によって公開される必要のあるメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c127-143">This controller class will contain the method that must be exposed by the Commerce Scale Unit API.</span></span> <span data-ttu-id="6c127-144">コントローラー クラス内で、CRT 要求を呼び出すメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="6c127-144">Inside the controller class, add methods to call the CRT request.</span></span>

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

5. <span data-ttu-id="6c127-145">**IEdmModelExtender** インターフェイスを拡張する **EdmModelExtender** (EDM) クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6c127-145">Create an **EdmModelExtender** (EDM) class that extends the **IEdmModelExtender** interface.</span></span> <span data-ttu-id="6c127-146">このクラスには、Commerce Scale Unit API が公開するデータを説明するために使用される抽象データ モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c127-146">This class contains the abstract data model that is used to describe the data that a Commerce Scale Unit API exposes.</span></span> <span data-ttu-id="6c127-147">オープン データ プロトコル (OData) メタデータ ドキュメントは、クライアントの消費に対して公開されるサービスのデータ モデルを表したものです。</span><span class="sxs-lookup"><span data-stu-id="6c127-147">An Open Data Protocol (OData) Metadata Document is a representation of a service's data model that is exposed for client consumption.</span></span> <span data-ttu-id="6c127-148">EDM の中心となる概念は、エンティティ、リレーションシップ、エンティティ セット、アクション、および機能です。</span><span class="sxs-lookup"><span data-stu-id="6c127-148">The central concepts in the EDM are entities, relationships, entity sets, actions, and functions.</span></span>

    <span data-ttu-id="6c127-149">**IEdmModelExtender** インターフェイスには、抽象 **ExtendModel** メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c127-149">The **IEdmModelExtender** interface contains the abstract **ExtendModel** method.</span></span> <span data-ttu-id="6c127-150">このインターフェイスを拡張する場合、**ExtendModel** メソッドを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c127-150">When you extend this interface, you must implement the **ExtendModel** method.</span></span> <span data-ttu-id="6c127-151">**ExtendModel** メソッド内で、**CommerceModelBuilder** クラスを使用してクライアントに公開される EDM エンティティおよび機能を構築します。</span><span class="sxs-lookup"><span data-stu-id="6c127-151">Inside the **ExtendModel** method, you build the EDM entities and functions that will be exposed to the client by using the **CommerceModelBuilder** class.</span></span>

    <span data-ttu-id="6c127-152">**CommerceModelBuilder** クラスには、エンティティおよび機能を構築するのに使用される構築メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6c127-152">The **CommerceModelBuilder** class contains the build method that is used to build the entities and functions.</span></span>

    | <span data-ttu-id="6c127-153">メソッド名</span><span class="sxs-lookup"><span data-stu-id="6c127-153">Method name</span></span>                                                                 | <span data-ttu-id="6c127-154">戻り値の型</span><span class="sxs-lookup"><span data-stu-id="6c127-154">Return type</span></span>                              | <span data-ttu-id="6c127-155">説明</span><span class="sxs-lookup"><span data-stu-id="6c127-155">Description</span></span> |
    |-----------------------------------------------------------------------------|------------------------------------------|-------------|
    | <span data-ttu-id="6c127-156">BuildEntity\<TEntity\>() where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="6c127-156">BuildEntity\<TEntity\>() where TEntity : class</span></span>                              | <span data-ttu-id="6c127-157">EntityTypeConfiguration\<TEntity\></span><span class="sxs-lookup"><span data-stu-id="6c127-157">EntityTypeConfiguration\<TEntity\></span></span>       | <span data-ttu-id="6c127-158">このメソッドがエンティティを構築します。</span><span class="sxs-lookup"><span data-stu-id="6c127-158">This method builds an entity.</span></span> |
    | <span data-ttu-id="6c127-159">BuildEntitySet\<TEntity\>(string entitySetName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="6c127-159">BuildEntitySet\<TEntity\>(string entitySetName) where TEntity : class</span></span>       | <span data-ttu-id="6c127-160">EntitySetConfiguration\<TEntity\></span><span class="sxs-lookup"><span data-stu-id="6c127-160">EntitySetConfiguration\<TEntity\></span></span>        | <span data-ttu-id="6c127-161">このメソッドがエンティティ セットを構築します。</span><span class="sxs-lookup"><span data-stu-id="6c127-161">This method builds an entity set.</span></span> |
    | <span data-ttu-id="6c127-162">BuildComplexType\<TComplexType\>() where TComplexType : class</span><span class="sxs-lookup"><span data-stu-id="6c127-162">BuildComplexType\<TComplexType\>() where TComplexType : class</span></span>               | <span data-ttu-id="6c127-163">ComplexTypeConfiguration\<TComplexType\></span><span class="sxs-lookup"><span data-stu-id="6c127-163">ComplexTypeConfiguration\<TComplexType\></span></span> | <span data-ttu-id="6c127-164">このメソッドが、複雑なエンティティ タイプを構築します。</span><span class="sxs-lookup"><span data-stu-id="6c127-164">This method builds a complex entity type.</span></span> |
    | <span data-ttu-id="6c127-165">BuildEnumType\<TEnumType\>()</span><span class="sxs-lookup"><span data-stu-id="6c127-165">BuildEnumType\<TEnumType\>()</span></span>                                                | <span data-ttu-id="6c127-166">EnumTypeConfiguration\<TEnumType\></span><span class="sxs-lookup"><span data-stu-id="6c127-166">EnumTypeConfiguration\<TEnumType\></span></span>       | <span data-ttu-id="6c127-167">このメソッドが、列挙型を構築します。</span><span class="sxs-lookup"><span data-stu-id="6c127-167">This method builds an enumeration type.</span></span> |
    | <span data-ttu-id="6c127-168">BindAction(string actionName)</span><span class="sxs-lookup"><span data-stu-id="6c127-168">BindAction(string actionName)</span></span>                                               | <span data-ttu-id="6c127-169">ActionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c127-169">ActionConfiguration</span></span>                      | <span data-ttu-id="6c127-170">このメソッドが、モデル ビルダーのアクションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="6c127-170">This method binds an action in the model builder.</span></span> <span data-ttu-id="6c127-171">アクションは HTTP POST 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="6c127-171">An action represents an HTTP POST request.</span></span> |
    | <span data-ttu-id="6c127-172">BindEntityAction\<TEntity\>(string actionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="6c127-172">BindEntityAction\<TEntity\>(string actionName) where TEntity : class</span></span>        | <span data-ttu-id="6c127-173">ActionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c127-173">ActionConfiguration</span></span>                      | <span data-ttu-id="6c127-174">このメソッドが、モデルのエンティティ アクションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="6c127-174">This method binds an entity action of the model.</span></span> <span data-ttu-id="6c127-175">アクションは HTTP POST 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="6c127-175">An action represents an HTTP POST request.</span></span> |
    | <span data-ttu-id="6c127-176">BindEntitySetAction\<TEntity\>(string actionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="6c127-176">BindEntitySetAction\<TEntity\>(string actionName) where TEntity : class</span></span>     | <span data-ttu-id="6c127-177">ActionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c127-177">ActionConfiguration</span></span>                      | <span data-ttu-id="6c127-178">このメソッドがエンティティ セット アクションをバインドします。</span><span class="sxs-lookup"><span data-stu-id="6c127-178">This method binds an entity set action.</span></span> <span data-ttu-id="6c127-179">アクションは HTTP POST 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="6c127-179">An action represents an HTTP POST request.</span></span>             |
    | <span data-ttu-id="6c127-180">BindFunction(string functionName)</span><span class="sxs-lookup"><span data-stu-id="6c127-180">BindFunction(string functionName)</span></span>                                           | <span data-ttu-id="6c127-181">FunctionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c127-181">FunctionConfiguration</span></span>                    | <span data-ttu-id="6c127-182">このメソッドが、モデル ビルダーの機能をバインドします。</span><span class="sxs-lookup"><span data-stu-id="6c127-182">This method binds a function in the model builder.</span></span> <span data-ttu-id="6c127-183">機能は HTTP GET 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="6c127-183">A function represents a HTTP GET request.</span></span> |
    | <span data-ttu-id="6c127-184">BindEntityFunction\<TEntity\>(string functionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="6c127-184">BindEntityFunction\<TEntity\>(string functionName) where TEntity : class</span></span>    | <span data-ttu-id="6c127-185">FunctionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c127-185">FunctionConfiguration</span></span>                    | <span data-ttu-id="6c127-186">このメソッドが、モデルのエンティティ機能をバインドします。</span><span class="sxs-lookup"><span data-stu-id="6c127-186">This method binds an entity function of the model.</span></span> <span data-ttu-id="6c127-187">機能は HTTP GET 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="6c127-187">A function represents an HTTP GET request.</span></span> |
    | <span data-ttu-id="6c127-188">BindEntitySetFunction\<TEntity\>(string functionName) where TEntity : class</span><span class="sxs-lookup"><span data-stu-id="6c127-188">BindEntitySetFunction\<TEntity\>(string functionName) where TEntity : class</span></span> | <span data-ttu-id="6c127-189">FunctionConfiguration</span><span class="sxs-lookup"><span data-stu-id="6c127-189">FunctionConfiguration</span></span>                    | <span data-ttu-id="6c127-190">このメソッドがエンティティ セット機能をバインドします。</span><span class="sxs-lookup"><span data-stu-id="6c127-190">This method binds an entity set function.</span></span> <span data-ttu-id="6c127-191">機能は HTTP GET 要求を表します。</span><span class="sxs-lookup"><span data-stu-id="6c127-191">A function represents an HTTP GET request.</span></span> |

    <span data-ttu-id="6c127-192">次の例は、EDM モデルを拡張する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6c127-192">The following example shows how to extend the EDM model.</span></span>

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

> [!NOTE]
> <span data-ttu-id="6c127-193">同一のエンティティの EdmModelExtender クラスではエンティティ名の重複を避けてください。</span><span class="sxs-lookup"><span data-stu-id="6c127-193">Do not duplicate the entity name in the EdmModelExtender class for the same entity.</span></span> <span data-ttu-id="6c127-194">これにより、プロキシ生成時に複数のマネージャ クラスとアダプタのクラスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="6c127-194">This will create multiple manager and Adapter classes during proxy generation.</span></span> <span data-ttu-id="6c127-195">例えば、**CustomEntity1** が拡張コードによって作成された新しいエンティティである場合、EdmModelExtender では、エンティティの名前が **CustomEntity1Sample** であれば、それが使用されている場所に同じ名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="6c127-195">For example, if **CustomEntity1** is the new entity created by the extension code, in the EdmModelExtender, if the entity is named **CustomEntity1Sample**, then use the same name wherever it used.</span></span> <span data-ttu-id="6c127-196">同一のエンティティに対して別の名前を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="6c127-196">Do not use a different name for the same entity.</span></span>

```C#
    builder.BuildEntitySet< CustomEntity1>(**"CustomEntity1Sample"**);
    action.ReturnsCollectionFromEntitySet< CustomEntity1>(**"CustomEntity1Sample"**);
```

6. <span data-ttu-id="6c127-197">拡張機能プロジェクトをビルドし、バイナリを **\\RetailServer\\webroot\\bin\\Ext** フォルダーにドロップします。</span><span class="sxs-lookup"><span data-stu-id="6c127-197">Build the extension project, and drop the binary into the **\\RetailServer\\webroot\\bin\\Ext** folder.</span></span>
7. <span data-ttu-id="6c127-198">**extensionComposition** セクションで新しい Commerce Scale Unit 拡張ライブラリ名を追加して、**\\RetailServer\\Webroot** フォルダーの Commerce Scale Unit web.config ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="6c127-198">Update the Commerce Scale Unit web.config file in the **\\RetailServer\\webroot** folder by adding the new extension library name in the **extensionComposition** section.</span></span>

    ```xml
    <extensionComposition>
    <!-- Please use fully qualified assembly names for ALL if you need to support loading from the Global Assembly Cache.
    If you host in an application with a bin folder, this is not required. -->
    <add source="assembly" value="SampleExtension" >;
    </extensionComposition>
    ```

8. <span data-ttu-id="6c127-199">Microsoft インターネット インフォメーション サービス (IIS) で、Commerce Scale Unit を再起動して、新しい拡張機能を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="6c127-199">In Microsoft Internet Information Services (IIS), restart Commerce Scale Unit to load the new extension.</span></span>
9. <span data-ttu-id="6c127-200">拡張機能が正常に読み込まれたことを確認するには、Commerce Scale Unit メタデータを参照し、エンティティとメソッドがリストに表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c127-200">To verify that the extension was successfully loaded, you can browse the Commerce Scale Unit metadata, and confirm that your entities and methods appear in the list.</span></span>

    <span data-ttu-id="6c127-201">メタデータを参照するには、Web ブラウザーの次の形式で URL を開きます。</span><span class="sxs-lookup"><span data-stu-id="6c127-201">To browse the metadata, open a URL in the following format in a web browser:</span></span>

    `https://Your Commerce Scale Unit URL/Commerce/$metadata`

10. <span data-ttu-id="6c127-202">クライアントで Commerce Scale Unit 拡張機能を呼び出すには、Commerce プロキシを生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c127-202">To call the Commerce Scale Unit extension in your client, you must generate the Commerce proxy.</span></span> <span data-ttu-id="6c127-203">その後、プロキシを使用して、クライアントから新しい Commerce Scale Unit API を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="6c127-203">You can then use the proxy to call your new Commerce Scale Unit APIs from the client.</span></span>

    <span data-ttu-id="6c127-204">プロキシの生成方法の詳細については、[Typescript および小売販売時点管理 (POS) の C# プロキシ](typescript-proxy-retail-pos.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c127-204">For information about how to generate the proxy, see [Typescript and C# proxies for Retail point of sale (POS)](typescript-proxy-retail-pos.md).</span></span>

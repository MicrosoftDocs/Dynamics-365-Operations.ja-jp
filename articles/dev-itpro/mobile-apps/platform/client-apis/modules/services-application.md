---
title: アプリケーション モジュール
description: アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。 各アプリケーションは、ページ、アクション、データクエリおよびそれらを結合するロジックで構成されています。 アプリケーションは主に宣言型メタデータ システムで記述され、付随的な拡張モデルを持つことができます。 &lt;br&gt;
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: ''
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f1efa1a07674ff7520ff1d306ee7427b57975913
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851507"
---
# <a name="application-module"></a><span data-ttu-id="0fdce-106">アプリケーション モジュール</span><span class="sxs-lookup"><span data-stu-id="0fdce-106">Application module</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="0fdce-107">アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。</span><span class="sxs-lookup"><span data-stu-id="0fdce-107">An application is a unit of runtime execution with sandboxing around concepts and data used inside of it.</span></span>
<span data-ttu-id="0fdce-108">各アプリケーションは、ページ、アクション、データクエリおよびそれらを結合するロジックで構成されています。</span><span class="sxs-lookup"><span data-stu-id="0fdce-108">Each application consists of pages, actions, data queries and logic that glue them together.</span></span> <span data-ttu-id="0fdce-109">アプリケーションは主に宣言型メタデータ システムで記述され、付随的な拡張モデルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="0fdce-109">An application is primarily described with a declarative metadata system, and can have an accompanying imperative extension model.</span></span> <br>
<span data-ttu-id="0fdce-110">アプリケーションの付随的な拡張は、一般に指定されたエントリポイントである [主な関数](#main) を持つスクリプト モジュールで定義されます。これにより、付随的なロジックをアプリケーション ライフ サイクルと統合できます。</span><span class="sxs-lookup"><span data-stu-id="0fdce-110">The imperative extension of the application is typically defined in a script module with a designated entry point, the [main function](#main), which allows the imperative logic to integrate with the application life cycle.</span></span>

## <a name="index"></a><span data-ttu-id="0fdce-111">指数</span><span class="sxs-lookup"><span data-stu-id="0fdce-111">Index</span></span>

### <a name="types"></a><span data-ttu-id="0fdce-112">種類</span><span class="sxs-lookup"><span data-stu-id="0fdce-112">Types</span></span>

* [<span data-ttu-id="0fdce-113">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0fdce-113">Application</span></span>](../interfaces/services-application-iapplication.md)
* [<span data-ttu-id="0fdce-114">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="0fdce-114">ApplicationMetadata</span></span>](../interfaces/services-application-iapplicationmetadata.md)

### <a name="functions"></a><span data-ttu-id="0fdce-115">関数</span><span class="sxs-lookup"><span data-stu-id="0fdce-115">Functions</span></span>

* [<span data-ttu-id="0fdce-116">main</span><span class="sxs-lookup"><span data-stu-id="0fdce-116">main</span></span>](services-application.md#main)

## <a name="types"></a><span data-ttu-id="0fdce-117">種類</span><span class="sxs-lookup"><span data-stu-id="0fdce-117">Types</span></span>


### <a name="application"></a><span data-ttu-id="0fdce-118">申請</span><span class="sxs-lookup"><span data-stu-id="0fdce-118">Application</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="0fdce-119">階層</span><span class="sxs-lookup"><span data-stu-id="0fdce-119">Hierarchy</span></span>

<span data-ttu-id="0fdce-120">申請</span><span class="sxs-lookup"><span data-stu-id="0fdce-120">Application</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="0fdce-121">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0fdce-121">Properties</span></span>

| <span data-ttu-id="0fdce-122">氏名</span><span class="sxs-lookup"><span data-stu-id="0fdce-122">Name</span></span> | <span data-ttu-id="0fdce-123">署名</span><span class="sxs-lookup"><span data-stu-id="0fdce-123">Signature</span></span> | <span data-ttu-id="0fdce-124">説明</span><span class="sxs-lookup"><span data-stu-id="0fdce-124">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="0fdce-125">minVersion</span><span class="sxs-lookup"><span data-stu-id="0fdce-125">minVersion</span></span>](../interfaces/services-application-iapplication.md#minversion) |<span data-ttu-id="0fdce-126">minVersion: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="0fdce-126">minVersion: string (optional)</span></span>  <br>|<span data-ttu-id="0fdce-127">このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。</span><span class="sxs-lookup"><span data-stu-id="0fdce-127">An optional marker to indicate the minimum platform version required by this component.</span></span> <span data-ttu-id="0fdce-128">これが指定され、プラットフォームの以前のバージョンへのコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。</span><span class="sxs-lookup"><span data-stu-id="0fdce-128">When this is specified and the component is attempted to be loaded in an older version of the platform, the corresponding workspace is not loaded and user is directed to install a newer version of the platform.</span></span><br>  |

#### <a name="methods"></a><span data-ttu-id="0fdce-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="0fdce-129">Methods</span></span>

| <span data-ttu-id="0fdce-130">氏名</span><span class="sxs-lookup"><span data-stu-id="0fdce-130">Name</span></span> | <span data-ttu-id="0fdce-131">署名</span><span class="sxs-lookup"><span data-stu-id="0fdce-131">Signature</span></span> | <span data-ttu-id="0fdce-132">説明</span><span class="sxs-lookup"><span data-stu-id="0fdce-132">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="0fdce-133">appInit</span><span class="sxs-lookup"><span data-stu-id="0fdce-133">appInit</span></span>](../interfaces/services-application-iapplication.md#appinit) |<span data-ttu-id="0fdce-134">appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="0fdce-134">appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any</span></span>|<span data-ttu-id="0fdce-135">このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="0fdce-135">This method is invoked at the point the application is about to run, with the instance of the application metadata loaded.</span></span> <span data-ttu-id="0fdce-136">渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。</span><span class="sxs-lookup"><span data-stu-id="0fdce-136">The metadata passed in can be still modified to change behaviors before this method returns.</span></span><br>  |


### <a name="applicationmetadata"></a><span data-ttu-id="0fdce-137">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="0fdce-137">ApplicationMetadata</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="0fdce-138">階層</span><span class="sxs-lookup"><span data-stu-id="0fdce-138">Hierarchy</span></span>

<span data-ttu-id="0fdce-139">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="0fdce-139">ApplicationMetadata</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="0fdce-140">プロパティ</span><span class="sxs-lookup"><span data-stu-id="0fdce-140">Properties</span></span>

| <span data-ttu-id="0fdce-141">氏名</span><span class="sxs-lookup"><span data-stu-id="0fdce-141">Name</span></span> | <span data-ttu-id="0fdce-142">署名</span><span class="sxs-lookup"><span data-stu-id="0fdce-142">Signature</span></span> | <span data-ttu-id="0fdce-143">説明</span><span class="sxs-lookup"><span data-stu-id="0fdce-143">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="0fdce-144">ColorName</span><span class="sxs-lookup"><span data-stu-id="0fdce-144">ColorName</span></span>](../interfaces/services-application-iapplicationmetadata.md#colorname) |<span data-ttu-id="0fdce-145">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0fdce-145">ColorName: string (optional)</span></span>  <br>|<span data-ttu-id="0fdce-146">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="0fdce-146">The theme color of the application</span></span><br>  |
| [<span data-ttu-id="0fdce-147">Configs</span><span class="sxs-lookup"><span data-stu-id="0fdce-147">Configs</span></span>](../interfaces/services-application-iapplicationmetadata.md#configs) |<span data-ttu-id="0fdce-148">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0fdce-148">Configs: [name: string]: any (optional)</span></span>  <br>|<span data-ttu-id="0fdce-149">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="0fdce-149">An application can have a set of named config supplied by the author or the resource provider</span></span><br>  |
| [<span data-ttu-id="0fdce-150">説明</span><span class="sxs-lookup"><span data-stu-id="0fdce-150">Description</span></span>](../interfaces/services-application-iapplicationmetadata.md#description) |<span data-ttu-id="0fdce-151">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0fdce-151">Description: string (optional)</span></span>  <br>|<span data-ttu-id="0fdce-152">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="0fdce-152">The description of the application</span></span><br>  |
| [<span data-ttu-id="0fdce-153">IconName</span><span class="sxs-lookup"><span data-stu-id="0fdce-153">IconName</span></span>](../interfaces/services-application-iapplicationmetadata.md#iconname) |<span data-ttu-id="0fdce-154">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="0fdce-154">IconName: string (optional)</span></span>  <br>|<span data-ttu-id="0fdce-155">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="0fdce-155">The representative icon of the application</span></span><br>  |
| [<span data-ttu-id="0fdce-156">ID</span><span class="sxs-lookup"><span data-stu-id="0fdce-156">Id</span></span>](../interfaces/services-application-iapplicationmetadata.md#id) |<span data-ttu-id="0fdce-157">Id: 文字列</span><span class="sxs-lookup"><span data-stu-id="0fdce-157">Id: string</span></span> <br>|<span data-ttu-id="0fdce-158">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="0fdce-158">The unique identifier of the application</span></span><br>  |
| [<span data-ttu-id="0fdce-159">タイトル</span><span class="sxs-lookup"><span data-stu-id="0fdce-159">Title</span></span>](../interfaces/services-application-iapplicationmetadata.md#title) |<span data-ttu-id="0fdce-160">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="0fdce-160">Title: string</span></span> <br>|<span data-ttu-id="0fdce-161">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="0fdce-161">The title of the application</span></span><br>  |

## <a name="functions"></a><span data-ttu-id="0fdce-162">関数</span><span class="sxs-lookup"><span data-stu-id="0fdce-162">Functions</span></span>


### <a name="main"></a><span data-ttu-id="0fdce-163">main</span><span class="sxs-lookup"><span data-stu-id="0fdce-163">main</span></span>
<span data-ttu-id="0fdce-164">main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)</span><span class="sxs-lookup"><span data-stu-id="0fdce-164">main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)</span></span>

<span data-ttu-id="0fdce-165">ビジネス ロジック モジュールの main メソッド。</span><span class="sxs-lookup"><span data-stu-id="0fdce-165">The main method of a business logic module.</span></span> <span data-ttu-id="0fdce-166">各ビジネス ロジック モジュール (JavaScript ファイルとして) では、1 つの主要な方法を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fdce-166">Each business logic module (as JavaScript file) must contain one main method.</span></span> <span data-ttu-id="0fdce-167">このメソッドは、モジュールが読み込まれ、初期化されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0fdce-167">The method is invoked when the module is loaded and is being initialized.</span></span> <span data-ttu-id="0fdce-168">メソッドは、このモジュールから実行するコンポーネントを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fdce-168">The method must return the component to run from this module.</span></span>


#### <a name="parameters"></a><span data-ttu-id="0fdce-169">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0fdce-169">Parameters</span></span>

| <span data-ttu-id="0fdce-170">氏名</span><span class="sxs-lookup"><span data-stu-id="0fdce-170">Name</span></span> | <span data-ttu-id="0fdce-171">種類</span><span class="sxs-lookup"><span data-stu-id="0fdce-171">Type</span></span> | <span data-ttu-id="0fdce-172">説明</span><span class="sxs-lookup"><span data-stu-id="0fdce-172">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="0fdce-173">metadataService</span><span class="sxs-lookup"><span data-stu-id="0fdce-173">metadataService</span></span>|[<span data-ttu-id="0fdce-174">MetadataService</span><span class="sxs-lookup"><span data-stu-id="0fdce-174">MetadataService</span></span>](../interfaces/services-business-logic-services-imetadataservice.md)||
| <span data-ttu-id="0fdce-175">dataService</span><span class="sxs-lookup"><span data-stu-id="0fdce-175">dataService</span></span>|[<span data-ttu-id="0fdce-176">DataService</span><span class="sxs-lookup"><span data-stu-id="0fdce-176">DataService</span></span>](../interfaces/services-business-logic-services-idataservice.md)||
| <span data-ttu-id="0fdce-177">cacheService</span><span class="sxs-lookup"><span data-stu-id="0fdce-177">cacheService</span></span>|[<span data-ttu-id="0fdce-178">CacheService</span><span class="sxs-lookup"><span data-stu-id="0fdce-178">CacheService</span></span>](../interfaces/services-business-logic-services-icacheservice.md)||
| <span data-ttu-id="0fdce-179">asyncService</span><span class="sxs-lookup"><span data-stu-id="0fdce-179">asyncService</span></span>|[<span data-ttu-id="0fdce-180">AsyncService</span><span class="sxs-lookup"><span data-stu-id="0fdce-180">AsyncService</span></span>](../interfaces/services-business-logic-services-iasyncservice.md)||

#### <a name="returns-applicationinterfacesservices-application-iapplicationmd"></a><span data-ttu-id="0fdce-181">[Application](../interfaces/services-application-iapplication.md) を返します</span><span class="sxs-lookup"><span data-stu-id="0fdce-181">Returns [Application](../interfaces/services-application-iapplication.md)</span></span>


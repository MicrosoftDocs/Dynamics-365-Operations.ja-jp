---
title: アプリケーション モジュール
description: アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。 各アプリケーションは、ページ、アクション、データ クエリおよびそれらを結合するロジックで構成されています。 アプリケーションは主に宣言型メタデータ システムで記述され、付随的な拡張モデルを持つことができます。
author: robinarh
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 85deae4eb8f77348419c6a35259b11e658ae5b51
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682562"
---
# <a name="application-module"></a><span data-ttu-id="732b3-105">アプリケーション モジュール</span><span class="sxs-lookup"><span data-stu-id="732b3-105">Application module</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="732b3-106">アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。</span><span class="sxs-lookup"><span data-stu-id="732b3-106">An application is a unit of runtime execution with sandboxing around concepts and data used inside of it.</span></span> <span data-ttu-id="732b3-107">各アプリケーションは、ページ、アクション、データ クエリおよびそれらを結合するロジックで構成されています。</span><span class="sxs-lookup"><span data-stu-id="732b3-107">Each application consists of pages, actions, data queries, and logic that glue them together.</span></span> <span data-ttu-id="732b3-108">アプリケーションは主に宣言型メタデータ システムで記述され、付随的な拡張モデルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="732b3-108">An application is primarily described with a declarative metadata system, and can have an accompanying imperative extension model.</span></span>

<span data-ttu-id="732b3-109">アプリケーションの付随的な拡張は、一般に指定されたエントリポイントである [主な関数](#main) を持つスクリプト モジュールで定義されます。これにより、付随的なロジックをアプリケーション ライフ サイクルと統合できます。</span><span class="sxs-lookup"><span data-stu-id="732b3-109">The imperative extension of the application is typically defined in a script module with a designated entry point, the [main function](#main), which allows the imperative logic to integrate with the application life cycle.</span></span>

## <a name="index"></a><span data-ttu-id="732b3-110">指数</span><span class="sxs-lookup"><span data-stu-id="732b3-110">Index</span></span>

### <a name="types"></a><span data-ttu-id="732b3-111">種類</span><span class="sxs-lookup"><span data-stu-id="732b3-111">Types</span></span>

* [<span data-ttu-id="732b3-112">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="732b3-112">Application</span></span>](../interfaces/services-application-iapplication.md)
* [<span data-ttu-id="732b3-113">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="732b3-113">ApplicationMetadata</span></span>](../interfaces/services-application-iapplicationmetadata.md)

### <a name="functions"></a><span data-ttu-id="732b3-114">関数</span><span class="sxs-lookup"><span data-stu-id="732b3-114">Functions</span></span>

* [<span data-ttu-id="732b3-115">main</span><span class="sxs-lookup"><span data-stu-id="732b3-115">main</span></span>](services-application.md#main)

## <a name="types"></a><span data-ttu-id="732b3-116">種類</span><span class="sxs-lookup"><span data-stu-id="732b3-116">Types</span></span>


### <a name="application"></a><span data-ttu-id="732b3-117">申請</span><span class="sxs-lookup"><span data-stu-id="732b3-117">Application</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="732b3-118">階層</span><span class="sxs-lookup"><span data-stu-id="732b3-118">Hierarchy</span></span>

<span data-ttu-id="732b3-119">申請</span><span class="sxs-lookup"><span data-stu-id="732b3-119">Application</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="732b3-120">プロパティ</span><span class="sxs-lookup"><span data-stu-id="732b3-120">Properties</span></span>

| <span data-ttu-id="732b3-121">氏名</span><span class="sxs-lookup"><span data-stu-id="732b3-121">Name</span></span> | <span data-ttu-id="732b3-122">署名</span><span class="sxs-lookup"><span data-stu-id="732b3-122">Signature</span></span> | <span data-ttu-id="732b3-123">説明</span><span class="sxs-lookup"><span data-stu-id="732b3-123">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="732b3-124">minVersion</span><span class="sxs-lookup"><span data-stu-id="732b3-124">minVersion</span></span>](../interfaces/services-application-iapplication.md#minversion) |<span data-ttu-id="732b3-125">minVersion: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="732b3-125">minVersion: string (optional)</span></span>  <br>|<span data-ttu-id="732b3-126">このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。</span><span class="sxs-lookup"><span data-stu-id="732b3-126">An optional marker to indicate the minimum platform version required by this component.</span></span> <span data-ttu-id="732b3-127">この値が指定され、プラットフォームの以前のバージョンでコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。</span><span class="sxs-lookup"><span data-stu-id="732b3-127">When this value is specified and the component tries to load in an older version of the platform, the corresponding workspace is not loaded and user is directed to install a newer version of the platform.</span></span><br>  |

#### <a name="methods"></a><span data-ttu-id="732b3-128">メソッド</span><span class="sxs-lookup"><span data-stu-id="732b3-128">Methods</span></span>

| <span data-ttu-id="732b3-129">氏名</span><span class="sxs-lookup"><span data-stu-id="732b3-129">Name</span></span> | <span data-ttu-id="732b3-130">署名</span><span class="sxs-lookup"><span data-stu-id="732b3-130">Signature</span></span> | <span data-ttu-id="732b3-131">説明</span><span class="sxs-lookup"><span data-stu-id="732b3-131">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="732b3-132">appInit</span><span class="sxs-lookup"><span data-stu-id="732b3-132">appInit</span></span>](../interfaces/services-application-iapplication.md#appinit) |<span data-ttu-id="732b3-133">appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="732b3-133">appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any</span></span>|<span data-ttu-id="732b3-134">このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="732b3-134">This method is invoked at the point the application is about to run, with the instance of the application metadata loaded.</span></span> <span data-ttu-id="732b3-135">渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。</span><span class="sxs-lookup"><span data-stu-id="732b3-135">The metadata passed in can be still modified to change behaviors before this method returns.</span></span><br>  |


### <a name="applicationmetadata"></a><span data-ttu-id="732b3-136">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="732b3-136">ApplicationMetadata</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="732b3-137">階層</span><span class="sxs-lookup"><span data-stu-id="732b3-137">Hierarchy</span></span>

<span data-ttu-id="732b3-138">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="732b3-138">ApplicationMetadata</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="732b3-139">プロパティ</span><span class="sxs-lookup"><span data-stu-id="732b3-139">Properties</span></span>

| <span data-ttu-id="732b3-140">氏名</span><span class="sxs-lookup"><span data-stu-id="732b3-140">Name</span></span> | <span data-ttu-id="732b3-141">署名</span><span class="sxs-lookup"><span data-stu-id="732b3-141">Signature</span></span> | <span data-ttu-id="732b3-142">説明</span><span class="sxs-lookup"><span data-stu-id="732b3-142">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="732b3-143">ColorName</span><span class="sxs-lookup"><span data-stu-id="732b3-143">ColorName</span></span>](../interfaces/services-application-iapplicationmetadata.md#colorname) |<span data-ttu-id="732b3-144">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="732b3-144">ColorName: string (optional)</span></span>  <br>|<span data-ttu-id="732b3-145">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="732b3-145">The theme color of the application</span></span><br>  |
| [<span data-ttu-id="732b3-146">Configs</span><span class="sxs-lookup"><span data-stu-id="732b3-146">Configs</span></span>](../interfaces/services-application-iapplicationmetadata.md#configs) |<span data-ttu-id="732b3-147">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="732b3-147">Configs: [name: string]: any (optional)</span></span>  <br>|<span data-ttu-id="732b3-148">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="732b3-148">An application can have a set of named config supplied by the author or the resource provider</span></span><br>  |
| [<span data-ttu-id="732b3-149">説明</span><span class="sxs-lookup"><span data-stu-id="732b3-149">Description</span></span>](../interfaces/services-application-iapplicationmetadata.md#description) |<span data-ttu-id="732b3-150">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="732b3-150">Description: string (optional)</span></span>  <br>|<span data-ttu-id="732b3-151">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="732b3-151">The description of the application</span></span><br>  |
| [<span data-ttu-id="732b3-152">IconName</span><span class="sxs-lookup"><span data-stu-id="732b3-152">IconName</span></span>](../interfaces/services-application-iapplicationmetadata.md#iconname) |<span data-ttu-id="732b3-153">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="732b3-153">IconName: string (optional)</span></span>  <br>|<span data-ttu-id="732b3-154">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="732b3-154">The representative icon of the application</span></span><br>  |
| [<span data-ttu-id="732b3-155">ID</span><span class="sxs-lookup"><span data-stu-id="732b3-155">ID</span></span>](../interfaces/services-application-iapplicationmetadata.md#id) |<span data-ttu-id="732b3-156">ID: 文字列</span><span class="sxs-lookup"><span data-stu-id="732b3-156">ID: string</span></span> <br>|<span data-ttu-id="732b3-157">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="732b3-157">The unique identifier of the application</span></span><br>  |
| [<span data-ttu-id="732b3-158">肩書き</span><span class="sxs-lookup"><span data-stu-id="732b3-158">Title</span></span>](../interfaces/services-application-iapplicationmetadata.md#title) |<span data-ttu-id="732b3-159">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="732b3-159">Title: string</span></span> <br>|<span data-ttu-id="732b3-160">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="732b3-160">The title of the application</span></span><br>  |

## <a name="functions"></a><span data-ttu-id="732b3-161">関数</span><span class="sxs-lookup"><span data-stu-id="732b3-161">Functions</span></span>


### <a name="main"></a><span data-ttu-id="732b3-162">main</span><span class="sxs-lookup"><span data-stu-id="732b3-162">main</span></span>
<span data-ttu-id="732b3-163">main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)</span><span class="sxs-lookup"><span data-stu-id="732b3-163">main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)</span></span>

<span data-ttu-id="732b3-164">ビジネス ロジック モジュールの main メソッド。</span><span class="sxs-lookup"><span data-stu-id="732b3-164">The main method of a business logic module.</span></span> <span data-ttu-id="732b3-165">各ビジネス ロジック モジュール (JavaScript ファイルとして) では、1 つの主要な方法を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="732b3-165">Each business logic module (as JavaScript file) must contain one main method.</span></span> <span data-ttu-id="732b3-166">このメソッドは、モジュールが読み込まれ、初期化されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="732b3-166">The method is invoked when the module is loaded and is being initialized.</span></span> <span data-ttu-id="732b3-167">メソッドは、このモジュールから実行するコンポーネントを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="732b3-167">The method must return the component to run from this module.</span></span>


#### <a name="parameters"></a><span data-ttu-id="732b3-168">パラメーター</span><span class="sxs-lookup"><span data-stu-id="732b3-168">Parameters</span></span>

| <span data-ttu-id="732b3-169">氏名</span><span class="sxs-lookup"><span data-stu-id="732b3-169">Name</span></span> | <span data-ttu-id="732b3-170">種類</span><span class="sxs-lookup"><span data-stu-id="732b3-170">Type</span></span> | <span data-ttu-id="732b3-171">説明</span><span class="sxs-lookup"><span data-stu-id="732b3-171">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="732b3-172">metadataService</span><span class="sxs-lookup"><span data-stu-id="732b3-172">metadataService</span></span>|[<span data-ttu-id="732b3-173">MetadataService</span><span class="sxs-lookup"><span data-stu-id="732b3-173">MetadataService</span></span>](../interfaces/services-business-logic-services-imetadataservice.md)||
| <span data-ttu-id="732b3-174">dataService</span><span class="sxs-lookup"><span data-stu-id="732b3-174">dataService</span></span>|[<span data-ttu-id="732b3-175">DataService</span><span class="sxs-lookup"><span data-stu-id="732b3-175">DataService</span></span>](../interfaces/services-business-logic-services-idataservice.md)||
| <span data-ttu-id="732b3-176">cacheService</span><span class="sxs-lookup"><span data-stu-id="732b3-176">cacheService</span></span>|[<span data-ttu-id="732b3-177">CacheService</span><span class="sxs-lookup"><span data-stu-id="732b3-177">CacheService</span></span>](../interfaces/services-business-logic-services-icacheservice.md)||
| <span data-ttu-id="732b3-178">asyncService</span><span class="sxs-lookup"><span data-stu-id="732b3-178">asyncService</span></span>|[<span data-ttu-id="732b3-179">AsyncService</span><span class="sxs-lookup"><span data-stu-id="732b3-179">AsyncService</span></span>](../interfaces/services-business-logic-services-iasyncservice.md)||

#### <a name="returns-application"></a><span data-ttu-id="732b3-180">[Application](../interfaces/services-application-iapplication.md) を返します</span><span class="sxs-lookup"><span data-stu-id="732b3-180">Returns [Application](../interfaces/services-application-iapplication.md)</span></span>


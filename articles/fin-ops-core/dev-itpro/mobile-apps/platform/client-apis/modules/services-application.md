---
title: アプリケーション モジュール
description: アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。
author: robinarh
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad918203cf245b018592abc4bbad938f7b889aad
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752990"
---
# <a name="application-module"></a><span data-ttu-id="be0ea-103">アプリケーション モジュール</span><span class="sxs-lookup"><span data-stu-id="be0ea-103">Application module</span></span>

[!include [banner](../../../../includes/banner.md)]

<span data-ttu-id="be0ea-104">アプリケーションとはその内部で使用される概念とデータの周りにサンドボックス化されたランタイム実行の単位です。</span><span class="sxs-lookup"><span data-stu-id="be0ea-104">An application is a unit of runtime execution with sandboxing around concepts and data used inside of it.</span></span> <span data-ttu-id="be0ea-105">各アプリケーションは、ページ、アクション、データ クエリおよびそれらを結合するロジックで構成されています。</span><span class="sxs-lookup"><span data-stu-id="be0ea-105">Each application consists of pages, actions, data queries, and logic that glue them together.</span></span> <span data-ttu-id="be0ea-106">アプリケーションは主に宣言型メタデータ システムで記述され、付随的な拡張モデルを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="be0ea-106">An application is primarily described with a declarative metadata system, and can have an accompanying imperative extension model.</span></span>

<span data-ttu-id="be0ea-107">アプリケーションの付随的な拡張は、一般に指定されたエントリポイントである [主な関数](#main) を持つスクリプト モジュールで定義されます。これにより、付随的なロジックをアプリケーション ライフ サイクルと統合できます。</span><span class="sxs-lookup"><span data-stu-id="be0ea-107">The imperative extension of the application is typically defined in a script module with a designated entry point, the [main function](#main), which allows the imperative logic to integrate with the application life cycle.</span></span>

## <a name="index"></a><span data-ttu-id="be0ea-108">指数</span><span class="sxs-lookup"><span data-stu-id="be0ea-108">Index</span></span>

### <a name="types"></a><span data-ttu-id="be0ea-109">種類</span><span class="sxs-lookup"><span data-stu-id="be0ea-109">Types</span></span>

* [<span data-ttu-id="be0ea-110">アプリケーション</span><span class="sxs-lookup"><span data-stu-id="be0ea-110">Application</span></span>](../interfaces/services-application-iapplication.md)
* [<span data-ttu-id="be0ea-111">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="be0ea-111">ApplicationMetadata</span></span>](../interfaces/services-application-iapplicationmetadata.md)

### <a name="functions"></a><span data-ttu-id="be0ea-112">関数</span><span class="sxs-lookup"><span data-stu-id="be0ea-112">Functions</span></span>

* [<span data-ttu-id="be0ea-113">main</span><span class="sxs-lookup"><span data-stu-id="be0ea-113">main</span></span>](services-application.md#main)

## <a name="types"></a><span data-ttu-id="be0ea-114">種類</span><span class="sxs-lookup"><span data-stu-id="be0ea-114">Types</span></span>


### <a name="application"></a><span data-ttu-id="be0ea-115">申請</span><span class="sxs-lookup"><span data-stu-id="be0ea-115">Application</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="be0ea-116">階層</span><span class="sxs-lookup"><span data-stu-id="be0ea-116">Hierarchy</span></span>

<span data-ttu-id="be0ea-117">申請</span><span class="sxs-lookup"><span data-stu-id="be0ea-117">Application</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="be0ea-118">プロパティ</span><span class="sxs-lookup"><span data-stu-id="be0ea-118">Properties</span></span>

| <span data-ttu-id="be0ea-119">氏名</span><span class="sxs-lookup"><span data-stu-id="be0ea-119">Name</span></span> | <span data-ttu-id="be0ea-120">署名</span><span class="sxs-lookup"><span data-stu-id="be0ea-120">Signature</span></span> | <span data-ttu-id="be0ea-121">説明</span><span class="sxs-lookup"><span data-stu-id="be0ea-121">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="be0ea-122">minVersion</span><span class="sxs-lookup"><span data-stu-id="be0ea-122">minVersion</span></span>](../interfaces/services-application-iapplication.md#minversion) |<span data-ttu-id="be0ea-123">minVersion: string (省略可)</span><span class="sxs-lookup"><span data-stu-id="be0ea-123">minVersion: string (optional)</span></span>  <br>|<span data-ttu-id="be0ea-124">このコンポーネントで必要な最小プラットフォーム バージョンを示すオプション マーカーです。</span><span class="sxs-lookup"><span data-stu-id="be0ea-124">An optional marker to indicate the minimum platform version required by this component.</span></span> <span data-ttu-id="be0ea-125">この値が指定され、プラットフォームの以前のバージョンでコンポーネントの読み込みが試行されるとき、対応するワークスペースは読み込まれず、ユーザーはプラットフォームの新しいバージョンのインストールを指示されます。</span><span class="sxs-lookup"><span data-stu-id="be0ea-125">When this value is specified and the component tries to load in an older version of the platform, the corresponding workspace is not loaded and user is directed to install a newer version of the platform.</span></span><br>  |

#### <a name="methods"></a><span data-ttu-id="be0ea-126">メソッド</span><span class="sxs-lookup"><span data-stu-id="be0ea-126">Methods</span></span>

| <span data-ttu-id="be0ea-127">氏名</span><span class="sxs-lookup"><span data-stu-id="be0ea-127">Name</span></span> | <span data-ttu-id="be0ea-128">署名</span><span class="sxs-lookup"><span data-stu-id="be0ea-128">Signature</span></span> | <span data-ttu-id="be0ea-129">説明</span><span class="sxs-lookup"><span data-stu-id="be0ea-129">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="be0ea-130">appInit</span><span class="sxs-lookup"><span data-stu-id="be0ea-130">appInit</span></span>](../interfaces/services-application-iapplication.md#appinit) |<span data-ttu-id="be0ea-131">appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any</span><span class="sxs-lookup"><span data-stu-id="be0ea-131">appInit(metadata: [ApplicationMetadata](../interfaces/services-application-iapplicationmetadata.md)): any</span></span>|<span data-ttu-id="be0ea-132">このメソッドは、アプリケーションが実行される時点で呼び出され、アプリケーション メタデータのインスタンスが読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="be0ea-132">This method is invoked at the point the application is about to run, with the instance of the application metadata loaded.</span></span> <span data-ttu-id="be0ea-133">渡されたメタデータは、このメソッドが戻る前に動作を変更するために変更できます。</span><span class="sxs-lookup"><span data-stu-id="be0ea-133">The metadata passed in can be still modified to change behaviors before this method returns.</span></span><br>  |


### <a name="applicationmetadata"></a><span data-ttu-id="be0ea-134">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="be0ea-134">ApplicationMetadata</span></span>

#### <a name="hierarchy"></a><span data-ttu-id="be0ea-135">階層</span><span class="sxs-lookup"><span data-stu-id="be0ea-135">Hierarchy</span></span>

<span data-ttu-id="be0ea-136">ApplicationMetadata</span><span class="sxs-lookup"><span data-stu-id="be0ea-136">ApplicationMetadata</span></span> <br>

#### <a name="properties"></a><span data-ttu-id="be0ea-137">プロパティ</span><span class="sxs-lookup"><span data-stu-id="be0ea-137">Properties</span></span>

| <span data-ttu-id="be0ea-138">氏名</span><span class="sxs-lookup"><span data-stu-id="be0ea-138">Name</span></span> | <span data-ttu-id="be0ea-139">署名</span><span class="sxs-lookup"><span data-stu-id="be0ea-139">Signature</span></span> | <span data-ttu-id="be0ea-140">説明</span><span class="sxs-lookup"><span data-stu-id="be0ea-140">Description</span></span> |
| ---- | --------- | ----------- |
| [<span data-ttu-id="be0ea-141">ColorName</span><span class="sxs-lookup"><span data-stu-id="be0ea-141">ColorName</span></span>](../interfaces/services-application-iapplicationmetadata.md#colorname) |<span data-ttu-id="be0ea-142">ColorName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="be0ea-142">ColorName: string (optional)</span></span>  <br>|<span data-ttu-id="be0ea-143">アプリケーションのテーマ色。</span><span class="sxs-lookup"><span data-stu-id="be0ea-143">The theme color of the application</span></span><br>  |
| [<span data-ttu-id="be0ea-144">Configs</span><span class="sxs-lookup"><span data-stu-id="be0ea-144">Configs</span></span>](../interfaces/services-application-iapplicationmetadata.md#configs) |<span data-ttu-id="be0ea-145">Configs: [名前: 文字列]: 任意 (オプション)</span><span class="sxs-lookup"><span data-stu-id="be0ea-145">Configs: [name: string]: any (optional)</span></span>  <br>|<span data-ttu-id="be0ea-146">アプリケーションは作成者またはリソース プロバイダーにより指定された名前付き構成のセットを持つことができます</span><span class="sxs-lookup"><span data-stu-id="be0ea-146">An application can have a set of named config supplied by the author or the resource provider</span></span><br>  |
| [<span data-ttu-id="be0ea-147">説明</span><span class="sxs-lookup"><span data-stu-id="be0ea-147">Description</span></span>](../interfaces/services-application-iapplicationmetadata.md#description) |<span data-ttu-id="be0ea-148">説明:文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="be0ea-148">Description: string (optional)</span></span>  <br>|<span data-ttu-id="be0ea-149">アプリケーションの説明</span><span class="sxs-lookup"><span data-stu-id="be0ea-149">The description of the application</span></span><br>  |
| [<span data-ttu-id="be0ea-150">IconName</span><span class="sxs-lookup"><span data-stu-id="be0ea-150">IconName</span></span>](../interfaces/services-application-iapplicationmetadata.md#iconname) |<span data-ttu-id="be0ea-151">IconName: 文字列 (オプション)</span><span class="sxs-lookup"><span data-stu-id="be0ea-151">IconName: string (optional)</span></span>  <br>|<span data-ttu-id="be0ea-152">アプリケーションの代表的なアイコン</span><span class="sxs-lookup"><span data-stu-id="be0ea-152">The representative icon of the application</span></span><br>  |
| [<span data-ttu-id="be0ea-153">ID</span><span class="sxs-lookup"><span data-stu-id="be0ea-153">ID</span></span>](../interfaces/services-application-iapplicationmetadata.md#id) |<span data-ttu-id="be0ea-154">ID: 文字列</span><span class="sxs-lookup"><span data-stu-id="be0ea-154">ID: string</span></span> <br>|<span data-ttu-id="be0ea-155">アプリケーションの一意の識別子</span><span class="sxs-lookup"><span data-stu-id="be0ea-155">The unique identifier of the application</span></span><br>  |
| [<span data-ttu-id="be0ea-156">肩書き</span><span class="sxs-lookup"><span data-stu-id="be0ea-156">Title</span></span>](../interfaces/services-application-iapplicationmetadata.md#title) |<span data-ttu-id="be0ea-157">タイトル: 文字列</span><span class="sxs-lookup"><span data-stu-id="be0ea-157">Title: string</span></span> <br>|<span data-ttu-id="be0ea-158">アプリケーションのタイトル。</span><span class="sxs-lookup"><span data-stu-id="be0ea-158">The title of the application</span></span><br>  |

## <a name="functions"></a><span data-ttu-id="be0ea-159">関数</span><span class="sxs-lookup"><span data-stu-id="be0ea-159">Functions</span></span>


### <a name="main"></a><span data-ttu-id="be0ea-160">main</span><span class="sxs-lookup"><span data-stu-id="be0ea-160">main</span></span>
<span data-ttu-id="be0ea-161">main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)</span><span class="sxs-lookup"><span data-stu-id="be0ea-161">main(metadataService: [MetadataService](../interfaces/services-business-logic-services-imetadataservice.md), dataService: [DataService](../interfaces/services-business-logic-services-idataservice.md), cacheService: [CacheService](../interfaces/services-business-logic-services-icacheservice.md), asyncService: [AsyncService](../interfaces/services-business-logic-services-iasyncservice.md)): [Application](../interfaces/services-application-iapplication.md)</span></span>

<span data-ttu-id="be0ea-162">ビジネス ロジック モジュールの main メソッド。</span><span class="sxs-lookup"><span data-stu-id="be0ea-162">The main method of a business logic module.</span></span> <span data-ttu-id="be0ea-163">各ビジネス ロジック モジュール (JavaScript ファイルとして) では、1 つの主要な方法を記述する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0ea-163">Each business logic module (as JavaScript file) must contain one main method.</span></span> <span data-ttu-id="be0ea-164">このメソッドは、モジュールが読み込まれ、初期化されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="be0ea-164">The method is invoked when the module is loaded and is being initialized.</span></span> <span data-ttu-id="be0ea-165">メソッドは、このモジュールから実行するコンポーネントを返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="be0ea-165">The method must return the component to run from this module.</span></span>


#### <a name="parameters"></a><span data-ttu-id="be0ea-166">パラメーター</span><span class="sxs-lookup"><span data-stu-id="be0ea-166">Parameters</span></span>

| <span data-ttu-id="be0ea-167">氏名</span><span class="sxs-lookup"><span data-stu-id="be0ea-167">Name</span></span> | <span data-ttu-id="be0ea-168">種類</span><span class="sxs-lookup"><span data-stu-id="be0ea-168">Type</span></span> | <span data-ttu-id="be0ea-169">説明</span><span class="sxs-lookup"><span data-stu-id="be0ea-169">Description</span></span> |
| ---- | ---- | ----------- |
| <span data-ttu-id="be0ea-170">metadataService</span><span class="sxs-lookup"><span data-stu-id="be0ea-170">metadataService</span></span>|[<span data-ttu-id="be0ea-171">MetadataService</span><span class="sxs-lookup"><span data-stu-id="be0ea-171">MetadataService</span></span>](../interfaces/services-business-logic-services-imetadataservice.md)||
| <span data-ttu-id="be0ea-172">dataService</span><span class="sxs-lookup"><span data-stu-id="be0ea-172">dataService</span></span>|[<span data-ttu-id="be0ea-173">DataService</span><span class="sxs-lookup"><span data-stu-id="be0ea-173">DataService</span></span>](../interfaces/services-business-logic-services-idataservice.md)||
| <span data-ttu-id="be0ea-174">cacheService</span><span class="sxs-lookup"><span data-stu-id="be0ea-174">cacheService</span></span>|[<span data-ttu-id="be0ea-175">CacheService</span><span class="sxs-lookup"><span data-stu-id="be0ea-175">CacheService</span></span>](../interfaces/services-business-logic-services-icacheservice.md)||
| <span data-ttu-id="be0ea-176">asyncService</span><span class="sxs-lookup"><span data-stu-id="be0ea-176">asyncService</span></span>|[<span data-ttu-id="be0ea-177">AsyncService</span><span class="sxs-lookup"><span data-stu-id="be0ea-177">AsyncService</span></span>](../interfaces/services-business-logic-services-iasyncservice.md)||

#### <a name="returns-application"></a><span data-ttu-id="be0ea-178">[Application](../interfaces/services-application-iapplication.md) を返します</span><span class="sxs-lookup"><span data-stu-id="be0ea-178">Returns [Application](../interfaces/services-application-iapplication.md)</span></span>



[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
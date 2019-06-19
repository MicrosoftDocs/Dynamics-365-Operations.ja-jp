---
title: 国/地域コードとコンフィギュレーション キー
description: この記事では、構成キーと国/地域の両方の実装の観点から適用できるシナリオを説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 4644
ms.assetid: 86eda511-b1a6-46d2-bd0f-f9991b727f1a
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdc3c7260047671acb12b229cf65d1928d0579e4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551077"
---
# <a name="countryregion-codes-and-configuration-keys"></a><span data-ttu-id="eaea0-103">国/地域コードとコンフィギュレーション キー</span><span class="sxs-lookup"><span data-stu-id="eaea0-103">Country/region codes and configuration keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eaea0-104">この記事では、構成キーと国/地域の両方の実装の観点から適用できるシナリオを説明します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-104">This article provides scenarios that are applicable from an implementation perspective for both configuration keys and country/region.</span></span>

### <a name="customer-table-schema"></a><span data-ttu-id="eaea0-105">顧客テーブル スキーマ</span><span class="sxs-lookup"><span data-stu-id="eaea0-105">Customer table schema</span></span>

| <span data-ttu-id="eaea0-106">フィールド名</span><span class="sxs-lookup"><span data-stu-id="eaea0-106">Field name</span></span>     | <span data-ttu-id="eaea0-107">フィールド ラベル</span><span class="sxs-lookup"><span data-stu-id="eaea0-107">Field label</span></span>     | <span data-ttu-id="eaea0-108">国のコンテキスト</span><span class="sxs-lookup"><span data-stu-id="eaea0-108">Country context</span></span> |
|----------------|-----------------|-----------------|
| <span data-ttu-id="eaea0-109">CustNum</span><span class="sxs-lookup"><span data-stu-id="eaea0-109">CustNum</span></span>        | <span data-ttu-id="eaea0-110">顧客番号</span><span class="sxs-lookup"><span data-stu-id="eaea0-110">Customer number</span></span> |                 |
| <span data-ttu-id="eaea0-111">CustName</span><span class="sxs-lookup"><span data-stu-id="eaea0-111">CustName</span></span>       | <span data-ttu-id="eaea0-112">顧客名</span><span class="sxs-lookup"><span data-stu-id="eaea0-112">Customer name</span></span>   |                 |
| <span data-ttu-id="eaea0-113">EinvoiceEANNum</span><span class="sxs-lookup"><span data-stu-id="eaea0-113">EinvoiceEANNum</span></span> | <span data-ttu-id="eaea0-114">EAN</span><span class="sxs-lookup"><span data-stu-id="eaea0-114">EAN</span></span>             | <span data-ttu-id="eaea0-115">DK</span><span class="sxs-lookup"><span data-stu-id="eaea0-115">DK</span></span>              |
| <span data-ttu-id="eaea0-116">FiscalCode</span><span class="sxs-lookup"><span data-stu-id="eaea0-116">FiscalCode</span></span>     | <span data-ttu-id="eaea0-117">会計年度コード</span><span class="sxs-lookup"><span data-stu-id="eaea0-117">Fiscal code</span></span>     | <span data-ttu-id="eaea0-118">IT</span><span class="sxs-lookup"><span data-stu-id="eaea0-118">IT</span></span>              |

### <a name="sample-data"></a><span data-ttu-id="eaea0-119">サンプル データ</span><span class="sxs-lookup"><span data-stu-id="eaea0-119">Sample data</span></span>

| <span data-ttu-id="eaea0-120">CustNum</span><span class="sxs-lookup"><span data-stu-id="eaea0-120">CustNum</span></span> | <span data-ttu-id="eaea0-121">CustName</span><span class="sxs-lookup"><span data-stu-id="eaea0-121">CustName</span></span>        | <span data-ttu-id="eaea0-122">EinvoiceEANNum{DK}</span><span class="sxs-lookup"><span data-stu-id="eaea0-122">EinvoiceEANNum{DK}</span></span> | <span data-ttu-id="eaea0-123">FiscalCode{IT}</span><span class="sxs-lookup"><span data-stu-id="eaea0-123">FiscalCode{IT}</span></span> | <span data-ttu-id="eaea0-124">DataAreaId</span><span class="sxs-lookup"><span data-stu-id="eaea0-124">DataAreaId</span></span> |
|---------|-----------------|--------------------|----------------|------------|
| <span data-ttu-id="eaea0-125">1</span><span class="sxs-lookup"><span data-stu-id="eaea0-125">1</span></span>       | <span data-ttu-id="eaea0-126">Contoso デンマーク</span><span class="sxs-lookup"><span data-stu-id="eaea0-126">Contoso Denmark</span></span> | <span data-ttu-id="eaea0-127">AA</span><span class="sxs-lookup"><span data-stu-id="eaea0-127">AA</span></span>                 | <span data-ttu-id="eaea0-128">{Empty}</span><span class="sxs-lookup"><span data-stu-id="eaea0-128">{Empty}</span></span>        | <span data-ttu-id="eaea0-129">DK</span><span class="sxs-lookup"><span data-stu-id="eaea0-129">DK</span></span>         |
| <span data-ttu-id="eaea0-130">2</span><span class="sxs-lookup"><span data-stu-id="eaea0-130">2</span></span>       | <span data-ttu-id="eaea0-131">Contoso イタリア</span><span class="sxs-lookup"><span data-stu-id="eaea0-131">Contoso Italy</span></span>   | <span data-ttu-id="eaea0-132">{Empty}</span><span class="sxs-lookup"><span data-stu-id="eaea0-132">{Empty}</span></span>            | <span data-ttu-id="eaea0-133">DD</span><span class="sxs-lookup"><span data-stu-id="eaea0-133">DD</span></span>             | <span data-ttu-id="eaea0-134">IT</span><span class="sxs-lookup"><span data-stu-id="eaea0-134">IT</span></span>         |

### <a name="sample-entity"></a><span data-ttu-id="eaea0-135">サンプル エンティティ</span><span class="sxs-lookup"><span data-stu-id="eaea0-135">Sample entity</span></span>

| <span data-ttu-id="eaea0-136">フィールド名</span><span class="sxs-lookup"><span data-stu-id="eaea0-136">Field name</span></span>     | <span data-ttu-id="eaea0-137">国のコンテキスト</span><span class="sxs-lookup"><span data-stu-id="eaea0-137">Country context</span></span> |
|----------------|-----------------|
| <span data-ttu-id="eaea0-138">CustomerNumber</span><span class="sxs-lookup"><span data-stu-id="eaea0-138">CustomerNumber</span></span> |                 |
| <span data-ttu-id="eaea0-139">CustomerName</span><span class="sxs-lookup"><span data-stu-id="eaea0-139">CustomerName</span></span>   |                 |
| <span data-ttu-id="eaea0-140">EAN</span><span class="sxs-lookup"><span data-stu-id="eaea0-140">EAN</span></span>            | <span data-ttu-id="eaea0-141">DK</span><span class="sxs-lookup"><span data-stu-id="eaea0-141">DK</span></span>              |
| <span data-ttu-id="eaea0-142">FiscalCode</span><span class="sxs-lookup"><span data-stu-id="eaea0-142">FiscalCode</span></span>     | <span data-ttu-id="eaea0-143">IT</span><span class="sxs-lookup"><span data-stu-id="eaea0-143">IT</span></span>              |

### <a name="scenario--field-level-only"></a><span data-ttu-id="eaea0-144">シナリオ: フィールド レベルでのみ</span><span class="sxs-lookup"><span data-stu-id="eaea0-144">Scenario – Field level only</span></span>

<span data-ttu-id="eaea0-145">開発者のアイザックは、地域の設定を含むフィールドがある顧客エンティティを作成します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-145">Isaac, a developer, builds a customer entity that has fields that contain regional settings.</span></span> <span data-ttu-id="eaea0-146">エンティティは OData によって消費されます。</span><span class="sxs-lookup"><span data-stu-id="eaea0-146">The entity is consumed through OData.</span></span>

<span data-ttu-id="eaea0-147">**読み取り操作の場合:** エンティティの消費者は、この情報を使用して、有効な地域マッピングを完了します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-147">**For read operations:** The consumer of the entity uses this information to complete an effective regional mapping.</span></span> <span data-ttu-id="eaea0-148">コンシューマーは、その地域に必要ではないフィールドを無視します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-148">The consumer ignores the fields that aren't required for that region.</span></span> <span data-ttu-id="eaea0-149">たとえば、デンマーク (DK) の消費者は、**EAN** フィールドおよびコア フィールドのみの値の読み取りに関連しています。</span><span class="sxs-lookup"><span data-stu-id="eaea0-149">For example, consumers in Denmark (DK) are concerned with reading the values of the **EAN** field and core fields only.</span></span>

<span data-ttu-id="eaea0-150">**書き込み操作の場合:** エンティティの消費者は、この情報を使用して、データを入力するために必要なフィールドのみを識別します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-150">**For write operations:** The consumer of the entity uses this information to identify only the fields that are required to populate data.</span></span> <span data-ttu-id="eaea0-151">コンシューマーは、地域のフィールドおよび関連するコア フィールドの検証が行われることを期待しています。</span><span class="sxs-lookup"><span data-stu-id="eaea0-151">The consumer expects validation to occur for regional fields and associated core fields.</span></span>

### <a name="behaviors--fields-only"></a><span data-ttu-id="eaea0-152">動作 – フィールドのみ</span><span class="sxs-lookup"><span data-stu-id="eaea0-152">Behaviors – Fields only</span></span>

| <span data-ttu-id="eaea0-153">シナリオ</span><span class="sxs-lookup"><span data-stu-id="eaea0-153">Scenario</span></span>                        | <span data-ttu-id="eaea0-154">説明</span><span class="sxs-lookup"><span data-stu-id="eaea0-154">Description</span></span> |
|---------------------------------|-------------|
| <span data-ttu-id="eaea0-155">デザイン</span><span class="sxs-lookup"><span data-stu-id="eaea0-155">Design</span></span>                          | <span data-ttu-id="eaea0-156">エンティティは、自動的にローカライズ プロパティを基になるフィールドから継承します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-156">Entities automatically inherit localization properties from underlying fields.</span></span> |
| <span data-ttu-id="eaea0-157">デザイン</span><span class="sxs-lookup"><span data-stu-id="eaea0-157">Design</span></span>                          | <span data-ttu-id="eaea0-158">開発者は、エンティティ フィールドのローカライズ プロパティを上書きまたは設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="eaea0-158">Developers can’t override or set localization properties on entity fields.</span></span> <span data-ttu-id="eaea0-159">これらのプロパティは、テーブルからのみ継承する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eaea0-159">These properties should be inherited only from tables.</span></span> <span data-ttu-id="eaea0-160">マップされていないフィールドにのみ上書き。</span><span class="sxs-lookup"><span data-stu-id="eaea0-160">Only override on unmapped fields.</span></span> |
| <span data-ttu-id="eaea0-161">読み取り動作 (OData メタデータ)</span><span class="sxs-lookup"><span data-stu-id="eaea0-161">Read behavior (OData metadata)</span></span>  | <span data-ttu-id="eaea0-162">OData のエンティティのコンシューマーは、メタデータまたは注釈を使用して、ローカライズするフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-162">The consumer of an entity from OData will have metadata or annotations to specify which fields are localized.</span></span> |
| <span data-ttu-id="eaea0-163">読み取り動作 (データ管理)</span><span class="sxs-lookup"><span data-stu-id="eaea0-163">Read behavior (Data management)</span></span> | <span data-ttu-id="eaea0-164">インポート/エクスポート フィールドでは、情報がエンドユーザーにわかりやすくなるように、メタデータに国/地域の値を表示します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-164">In import/export fields, metadata displays country/region values, so that this information is obvious to the end user.</span></span> |
| <span data-ttu-id="eaea0-165">読み取り動作</span><span class="sxs-lookup"><span data-stu-id="eaea0-165">Read behavior</span></span>                   | <span data-ttu-id="eaea0-166">会社間の読み取り操作中に、ローカライズされたフィールドのデータは、コンテキストが一致した場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="eaea0-166">During cross-company read operations, data from localized fields is displayed only if the context matches.</span></span> <span data-ttu-id="eaea0-167">これが既にテーブル/ビューを通じて実装されている必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="eaea0-167">Note that this should already be implemented through the table/view.</span></span> |
| <span data-ttu-id="eaea0-168">読み取り動作 (パフォーマンス)</span><span class="sxs-lookup"><span data-stu-id="eaea0-168">Read behavior (Performance)</span></span>     | <span data-ttu-id="eaea0-169">会社固有の読み取り操作中に、コンテキストが一致しない場合、ローカライズされたフィールドはクエリから削除されます。</span><span class="sxs-lookup"><span data-stu-id="eaea0-169">During company-specific read operations, localized fields are dropped from the query when the context doesn't match.</span></span> |
| <span data-ttu-id="eaea0-170">書き込み</span><span class="sxs-lookup"><span data-stu-id="eaea0-170">Write</span></span>                           | <span data-ttu-id="eaea0-171">ローカライズされたフィールドへの書き込み操作中に、フィールドがコンテキストに一致しない場合はハード エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-171">During write operations to localized fields, hard errors occur if the fields don't match the context.</span></span> |
| <span data-ttu-id="eaea0-172">(共有テーブル)</span><span class="sxs-lookup"><span data-stu-id="eaea0-172">(Shared table)</span></span>                  | <span data-ttu-id="eaea0-173">データ ソースまたはフィールドに、共有 (グローバル) テーブルである国/地域が含まれている場合、キーが適用されていない場合と同じようにすべての工程が無視されます。</span><span class="sxs-lookup"><span data-stu-id="eaea0-173">If the data source or fields contain a country/region that is a shared (global) table, all operations are ignored, just as if no keys are applied.</span></span> |

### <a name="behavior--data-source"></a><span data-ttu-id="eaea0-174">動作 – データ ソース</span><span class="sxs-lookup"><span data-stu-id="eaea0-174">Behavior – Data source</span></span>

<span data-ttu-id="eaea0-175">データ ソースで適用されるコンフィギュレーション キーと国/地域の動作は、フィールドの動作に似ています。</span><span class="sxs-lookup"><span data-stu-id="eaea0-175">The behavior of configuration keys and a country/region that are applied at the data source resembles the behavior of fields.</span></span> <span data-ttu-id="eaea0-176">これらの値は、フィールド レベルに適用された場合と同様に、データ ソースから推測されます。</span><span class="sxs-lookup"><span data-stu-id="eaea0-176">These values are inferred from the data source, just as if they are applied to the field level.</span></span> <span data-ttu-id="eaea0-177">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="eaea0-177">Here's an example.</span></span>

    Entity E1

        |_ Data Source 1 (DS1)

              Field1

              Field2

        |_Data Source 2 (DS2) UK

              Field3

              Field4

#### <a name="evaluation-at-the-entity-e1-level"></a><span data-ttu-id="eaea0-178">エンティティ E1 レベルで評価</span><span class="sxs-lookup"><span data-stu-id="eaea0-178">Evaluation at the entity E1 level</span></span>

    Entity E1

    |_F1

    |_F2

    |_F3 (UK inferred)

    |_F4 (UK inferred)

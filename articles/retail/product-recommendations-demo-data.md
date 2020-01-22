---
title: オムニ チャネル製品推奨事項のデモ データ
description: このドキュメントでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングルボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872329"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="48e73-103">オムニ チャネル製品推奨事項のデモ データ</span><span class="sxs-lookup"><span data-stu-id="48e73-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="48e73-104">このドキュメントでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングルボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="48e73-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="48e73-105">オムニ チャンネルの製品推奨事項は、編集上精選された、またはプログラムで生成された一連の製品一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="48e73-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="48e73-106">これらの一覧は、ビジネスのニーズに応じて、いくつかのシナリオで使用できます。</span><span class="sxs-lookup"><span data-stu-id="48e73-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="48e73-107">製品推奨事項一覧の詳細については、[製品推奨事項の概要](../commerce/product-recommendations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48e73-107">For more information about product recommendation lists, see [Product recommendations overview.](../commerce/product-recommendations.md)</span></span>

<span data-ttu-id="48e73-108">レベル 2 およびそれ以上の Dynamics 環境では、製品推奨事項は顧客データに基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="48e73-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="48e73-109">製品推奨事項のデモ データを使用しても、環境で既にプロビジョニングされている製品推奨ソリューション、およびその使用に関連するコストが無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="48e73-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="48e73-110">レベル 1 環境では、製品推奨事項は、csv ファイルに格納された静的デモ データのみに基づいています。</span><span class="sxs-lookup"><span data-stu-id="48e73-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="48e73-111">環境内の製品推奨事項デモ データの有効化</span><span class="sxs-lookup"><span data-stu-id="48e73-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="48e73-112">顧客はそれぞれの環境に **Dynamics 365 Commerce プレビュー デモ拡張機能**を配置する必要があります。これにより、製品推奨事項のデモ データが自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="48e73-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="48e73-113">既定のデモ データ</span><span class="sxs-lookup"><span data-stu-id="48e73-113">Default demo data</span></span>
<span data-ttu-id="48e73-114">各 Onebox タイプの環境には、コンマで区切られた **' reco_demo_data '** ファイルに格納されたプリロード済の一連の製品推奨事項のデモ データが含まれ、Retail Server 上のこのドキュメントと同じフォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="48e73-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="48e73-115">このデータは、次の列に沿って構成されています。</span><span class="sxs-lookup"><span data-stu-id="48e73-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="48e73-116">列名</span><span class="sxs-lookup"><span data-stu-id="48e73-116">Column name</span></span>         | <span data-ttu-id="48e73-117">必須</span><span class="sxs-lookup"><span data-stu-id="48e73-117">Mandatory</span></span>          | <span data-ttu-id="48e73-118">説明</span><span class="sxs-lookup"><span data-stu-id="48e73-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="48e73-119">有効値</span><span class="sxs-lookup"><span data-stu-id="48e73-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="48e73-120">レコリスト</span><span class="sxs-lookup"><span data-stu-id="48e73-120">RecoList</span></span>            | <span data-ttu-id="48e73-121">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="48e73-121">:heavy_check_mark:</span></span> | <span data-ttu-id="48e73-122">デモ データ ポイントが生成する特定の製品推奨事項リスト タイプ。</span><span class="sxs-lookup"><span data-stu-id="48e73-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="48e73-123">レコベストセリング</span><span class="sxs-lookup"><span data-stu-id="48e73-123">RecoBestSelling</span></span></li><li><span data-ttu-id="48e73-124">レコニュー</span><span class="sxs-lookup"><span data-stu-id="48e73-124">RecoNew</span></span></li><li><span data-ttu-id="48e73-125">レコトレンディング</span><span class="sxs-lookup"><span data-stu-id="48e73-125">RecoTrending</span></span></li><li><span data-ttu-id="48e73-126">レコカート</span><span class="sxs-lookup"><span data-stu-id="48e73-126">RecoCart</span></span></li><li><span data-ttu-id="48e73-127">レコピーポーオールソーバイ</span><span class="sxs-lookup"><span data-stu-id="48e73-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="48e73-128">オペレーティングユニットナンバー</span><span class="sxs-lookup"><span data-stu-id="48e73-128">OperatingUnitNumber</span></span> | <span data-ttu-id="48e73-129">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="48e73-129">:heavy_check_mark:</span></span> | <span data-ttu-id="48e73-130">製品推奨事項が提示される特定の作業単位番号。</span><span class="sxs-lookup"><span data-stu-id="48e73-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="48e73-131">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="48e73-131">Category</span></span>            |                    |    <span data-ttu-id="48e73-132">特定のリストが返されるカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="48e73-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="48e73-133">カテゴリが指定されていない場合は、リストはナビゲーション階層の上部にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="48e73-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="48e73-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="48e73-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="48e73-135">シードを必要とするリスト (レコピーポーオールソーバイおよびレコカート) については、それらのリストの製品には追加の製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48e73-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="48e73-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="48e73-136">ItemIds</span></span>             | <span data-ttu-id="48e73-137">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="48e73-137">:heavy_check_mark:</span></span> | <span data-ttu-id="48e73-138">**‘;’** で区切られ、結果として返される 1 つ以上の製品。</span><span class="sxs-lookup"><span data-stu-id="48e73-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="48e73-139">デモ データのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="48e73-139">Customize demo data</span></span>
<span data-ttu-id="48e73-140">顧客は、本社でコンフィギュレーションされた製品およびカテゴリ情報を使用して、既定のデモ データを編集できます。</span><span class="sxs-lookup"><span data-stu-id="48e73-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="48e73-141">CSV が更新されると、顧客に返される製品推奨事項に、その変更がすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="48e73-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="48e73-142">拡張機能には、レコモックデータセット .csv と呼ばれるデータファイルが含まれています。これにより、顧客は、モックの推奨結果の出力に使用するデータセットを制御できます。</span><span class="sxs-lookup"><span data-stu-id="48e73-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="48e73-143">ファイル名は、**ext.Recommendations.DemoFilePath** 設定を使用して、拡張コンフィギュレーションによって制御できます。</span><span class="sxs-lookup"><span data-stu-id="48e73-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="48e73-144">これにより、コンフィギュレーション時に簡単に切り替えることができる複数のデータセットを顧客が利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="48e73-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="48e73-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="48e73-145">Additional resources</span></span>

[<span data-ttu-id="48e73-146">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="48e73-146">Product recommendations overview</span></span>](../commerce/product-recommendations.md)

[<span data-ttu-id="48e73-147">環境計画</span><span class="sxs-lookup"><span data-stu-id="48e73-147">Environment planning</span></span>](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)

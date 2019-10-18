---
title: オムニ チャネル製品推奨事項のデモ データ
description: このドキュメントでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングルボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 81af4c1bb7828c9b346a3ef514d8657e853dcefb
ms.sourcegitcommit: c526cfd1f823df1ff33ded95e599a72f0a15cc5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2226139"
---
# <a name="omni-channel-product-recommendations-demo-data"></a><span data-ttu-id="0e424-103">オムニ チャネル製品推奨事項のデモ データ</span><span class="sxs-lookup"><span data-stu-id="0e424-103">Omni-channel product recommendations demo data</span></span>

<span data-ttu-id="0e424-104">このドキュメントでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングルボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0e424-104">This document aims to provide guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="0e424-105">オムニ チャンネルの製品推奨事項は、編集上精選された、またはプログラムで生成された一連の製品一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="0e424-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated ordered list of products.</span></span> <span data-ttu-id="0e424-106">これらの一覧は、ビジネスのニーズに応じて、いくつかのシナリオで使用できます。</span><span class="sxs-lookup"><span data-stu-id="0e424-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="0e424-107">製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendaitons-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0e424-107">For more information about product recommendation lists, see [Product recommendations overview.](product-recommendaitons-overview.md)</span></span>

<span data-ttu-id="0e424-108">レベル 2 およびそれ以上の Dynamics 環境では、製品推奨事項は顧客データに基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="0e424-108">For Tier-2 and higher Dynamics Environments product recommendations are automatically computed based on customer data.</span></span>
<span data-ttu-id="0e424-109">製品推奨事項のデモ データを使用しても、環境で既にプロビジョニングされている製品推奨ソリューション、およびその使用に関連するコストが無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="0e424-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="0e424-110">レベル 1 環境では、製品推奨事項は、csv ファイルに格納された静的デモ データのみに基づいています。</span><span class="sxs-lookup"><span data-stu-id="0e424-110">For Tier-1 environments product recommendations are based only off the static demo data stored in a csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="0e424-111">環境内の製品推奨事項デモ データの有効化</span><span class="sxs-lookup"><span data-stu-id="0e424-111">Enabling product recommendations demo data in an environment</span></span>

<span data-ttu-id="0e424-112">顧客はそれぞれの環境に **Dynamics 365 Commerce プレビュー デモ拡張機能**を配置する必要があります。これにより、製品推奨事項のデモ データが自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="0e424-112">Customers need to deploy the **Dynamics 365 Commerce Preview Demo Extension** to the respective environment, which automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="0e424-113">既定のデモ データ</span><span class="sxs-lookup"><span data-stu-id="0e424-113">Default demo data</span></span>
<span data-ttu-id="0e424-114">各 Onebox タイプの環境には、コンマで区切られた **' reco_demo_data '** ファイルに格納されたプリロード済の一連の製品推奨事項のデモ データが含まれ、Retail Server 上のこのドキュメントと同じフォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="0e424-114">Each Onebox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated **‘reco_demo_data.csv’** file, located in the same folder as this document on Retail Server.</span></span>

<span data-ttu-id="0e424-115">このデータは、次の列に沿って構成されています。</span><span class="sxs-lookup"><span data-stu-id="0e424-115">This data is structured along the following columns</span></span>

| <span data-ttu-id="0e424-116">列名</span><span class="sxs-lookup"><span data-stu-id="0e424-116">Column name</span></span>         | <span data-ttu-id="0e424-117">必須</span><span class="sxs-lookup"><span data-stu-id="0e424-117">Mandatory</span></span>          | <span data-ttu-id="0e424-118">説明</span><span class="sxs-lookup"><span data-stu-id="0e424-118">Description</span></span>                                                                                                                                 | <span data-ttu-id="0e424-119">有効値</span><span class="sxs-lookup"><span data-stu-id="0e424-119">Possible Values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="0e424-120">レコリスト</span><span class="sxs-lookup"><span data-stu-id="0e424-120">RecoList</span></span>            | <span data-ttu-id="0e424-121">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="0e424-121">:heavy_check_mark:</span></span> | <span data-ttu-id="0e424-122">デモ データ ポイントが生成する特定の製品推奨事項リスト タイプ。</span><span class="sxs-lookup"><span data-stu-id="0e424-122">The specific product   recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="0e424-123">レコベストセリング</span><span class="sxs-lookup"><span data-stu-id="0e424-123">RecoBestSelling</span></span></li><li><span data-ttu-id="0e424-124">レコニュー</span><span class="sxs-lookup"><span data-stu-id="0e424-124">RecoNew</span></span></li><li><span data-ttu-id="0e424-125">レコトレンディング</span><span class="sxs-lookup"><span data-stu-id="0e424-125">RecoTrending</span></span></li><li><span data-ttu-id="0e424-126">レコカート</span><span class="sxs-lookup"><span data-stu-id="0e424-126">RecoCart</span></span></li><li><span data-ttu-id="0e424-127">レコピーポーオールソーバイ</span><span class="sxs-lookup"><span data-stu-id="0e424-127">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="0e424-128">オペレーティングユニットナンバー</span><span class="sxs-lookup"><span data-stu-id="0e424-128">OperatingUnitNumber</span></span> | <span data-ttu-id="0e424-129">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="0e424-129">:heavy_check_mark:</span></span> | <span data-ttu-id="0e424-130">製品推奨事項が提示される特定の作業単位番号。</span><span class="sxs-lookup"><span data-stu-id="0e424-130">The specific   operating unit number where product recommendations are expected to be   surfaced in.</span></span>                                        |                                                                              |
| <span data-ttu-id="0e424-131">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="0e424-131">Category</span></span>            |                    |    <span data-ttu-id="0e424-132">特定のリストが返されるカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="0e424-132">The category the   specific list should be returned for.</span></span> <span data-ttu-id="0e424-133">カテゴリが指定されていない場合は、リストはナビゲーション階層の上部にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e424-133">If no category is specified, list is   for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="0e424-134">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="0e424-134">SeedItemId</span></span>          |                    |    <span data-ttu-id="0e424-135">シードを必要とするリスト (レコピーポーオールソーバイおよびレコカート) については、それらのリストの製品には追加の製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0e424-135">For lists that   require seed (RecoPeopleAlsoBuy and RecoCart) the product those lists should   show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="0e424-136">ItemIds</span><span class="sxs-lookup"><span data-stu-id="0e424-136">ItemIds</span></span>             | <span data-ttu-id="0e424-137">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="0e424-137">:heavy_check_mark:</span></span> | <span data-ttu-id="0e424-138">**‘;’** で区切られ、結果として返される 1 つ以上の製品。</span><span class="sxs-lookup"><span data-stu-id="0e424-138">One or more products   to be returned as the result, separated by **‘;’**.</span></span>                                                                  |                                                                              |


## <a name="customize-demo-data"></a><span data-ttu-id="0e424-139">デモ データのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0e424-139">Customize demo data</span></span>
<span data-ttu-id="0e424-140">顧客は、本社でコンフィギュレーションされた製品およびカテゴリ情報を使用して、既定のデモ データを編集できます。</span><span class="sxs-lookup"><span data-stu-id="0e424-140">Customers can edit the default demo data with any product and category information that is configured in HQ.</span></span> <span data-ttu-id="0e424-141">CSV が更新されると、顧客に返される製品推奨事項に、その変更がすぐに反映されます。</span><span class="sxs-lookup"><span data-stu-id="0e424-141">Once the CSV is updated, the Product Recommendations returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="0e424-142">拡張機能には、レコモックデータセット .csv と呼ばれるデータファイルが含まれています。これにより、顧客は、モックの推奨結果の出力に使用するデータセットを制御できます。</span><span class="sxs-lookup"><span data-stu-id="0e424-142">The extension contains a datafile called RecoMockDataset.csv which allows the customer to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="0e424-143">ファイル名は、**ext.Recommendations.DemoFilePath** 設定を使用して、拡張コンフィギュレーションによって制御できます。</span><span class="sxs-lookup"><span data-stu-id="0e424-143">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="0e424-144">これにより、コンフィギュレーション時に簡単に切り替えることができる複数のデータセットを顧客が利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0e424-144">This enables the customers to have multiple datasets available that can be switched between easily through configuration.</span></span>

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a><span data-ttu-id="0e424-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0e424-145">Additional resources</span></span>

[<span data-ttu-id="0e424-146">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="0e424-146">Product recommendations overview</span></span>](product-recommendations-overview.md)

[<span data-ttu-id="0e424-147">環境計画</span><span class="sxs-lookup"><span data-stu-id="0e424-147">Environment planning</span></span>](environment-planning.md)

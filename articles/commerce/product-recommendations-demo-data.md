---
title: 推奨事項とデモ データの作成
description: このトピックでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングル ボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cca6913375eec2565852676f3c1da5a67f71e14f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413625"
---
# <a name="create-recommendations-with-demo-data"></a><span data-ttu-id="80dbb-103">推奨事項とデモ データの作成</span><span class="sxs-lookup"><span data-stu-id="80dbb-103">Create recommendations with demo data</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80dbb-104">このトピックでは、事前設定されたカスタマイズ可能なデモ データを使用して、レベル 1 シングル ボックス環境でのオムニ チャネル製品の推奨事項を活用する方法についてのガイダンスを提供します。</span><span class="sxs-lookup"><span data-stu-id="80dbb-104">This topic provides guidance on how to leverage omni-channel product recommendations in Tier-1 single box environments using pre-populated, customizable demo data.</span></span>

<span data-ttu-id="80dbb-105">オムニ チャネルの製品推奨事項は、編集上精選された、またはプログラムで生成された製品一覧を提供します。</span><span class="sxs-lookup"><span data-stu-id="80dbb-105">Omni-channel product recommendations provide a set of editorially curated or programmatically generated list of products.</span></span> <span data-ttu-id="80dbb-106">これらの一覧は、ビジネスのニーズに応じて、いくつかのシナリオで使用できます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-106">These lists can be used in several scenarios, depending on the business need.</span></span> <span data-ttu-id="80dbb-107">製品推奨事項一覧の詳細については、[製品推奨事項の概要](product-recommendations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80dbb-107">For more information about product recommendation lists, see [Product recommendations overview](product-recommendations.md).</span></span>

<span data-ttu-id="80dbb-108">レベル 2 およびそれ以上の Dynamics 365 環境では、製品推奨事項は顧客データに基づいて自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-108">For Tier-2 and higher Dynamics 365 environments, product recommendations are automatically computed based on customer data.</span></span> <span data-ttu-id="80dbb-109">製品推奨事項のデモ データを使用しても、環境で既にプロビジョニングされている製品推奨ソリューション、およびその使用に関連するコストが無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="80dbb-109">Using product recommendations demo data does not disable any product recommendations solution already provisioned in the environment and any costs associated with its usage.</span></span>

<span data-ttu-id="80dbb-110">レベル 1 環境では、製品推奨事項は、.csv ファイルに格納された静的デモ データのみに基づいています。</span><span class="sxs-lookup"><span data-stu-id="80dbb-110">For Tier-1 environments, product recommendations are based only off the static demo data stored in a .csv file.</span></span>

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a><span data-ttu-id="80dbb-111">環境内の製品推奨事項デモ データの有効化</span><span class="sxs-lookup"><span data-stu-id="80dbb-111">Enabling product recommendations demo data in an environment</span></span>
<span data-ttu-id="80dbb-112">製品推奨事項デモ日付を有効にするには、それぞれの環境に Dynamics 365 Commerce プレビュー デモ拡張機能を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="80dbb-112">To enable product recommendations demo date, you need to deploy the Dynamics 365 Commerce Preview Demo Extension to the respective environment.</span></span> <span data-ttu-id="80dbb-113">これを行うと、製品推奨事項デモ データが自動的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="80dbb-113">Doing so automatically enables product recommendations demo data.</span></span>

## <a name="default-demo-data"></a><span data-ttu-id="80dbb-114">既定のデモ データ</span><span class="sxs-lookup"><span data-stu-id="80dbb-114">Default demo data</span></span>
<span data-ttu-id="80dbb-115">各 OneBox タイプの環境には、コンマで区切られた 'reco_demo_data.csv' ファイルに格納されたプリロード済の一連の製品推奨事項のデモ データが含まれ、Commerce Scale Unit 上にあります。</span><span class="sxs-lookup"><span data-stu-id="80dbb-115">Each OneBox type environment comes with a preloaded set of product recommendations demo data stored in the coma separated 'reco_demo_data.csv' file, located on the Commerce Scale Unit.</span></span>

<span data-ttu-id="80dbb-116">データは、次の列に沿って構成されています。</span><span class="sxs-lookup"><span data-stu-id="80dbb-116">The data is structured along the following columns.</span></span>

| <span data-ttu-id="80dbb-117">列名</span><span class="sxs-lookup"><span data-stu-id="80dbb-117">Column name</span></span>         | <span data-ttu-id="80dbb-118">必須</span><span class="sxs-lookup"><span data-stu-id="80dbb-118">Mandatory</span></span>          | <span data-ttu-id="80dbb-119">説明</span><span class="sxs-lookup"><span data-stu-id="80dbb-119">Description</span></span>                                                                                                                                 | <span data-ttu-id="80dbb-120">有効値</span><span class="sxs-lookup"><span data-stu-id="80dbb-120">Possible values</span></span>                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="80dbb-121">レコリスト</span><span class="sxs-lookup"><span data-stu-id="80dbb-121">RecoList</span></span>            | <span data-ttu-id="80dbb-122">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="80dbb-122">:heavy_check_mark:</span></span> | <span data-ttu-id="80dbb-123">デモ データ ポイントが生成する、特定の製品推奨事項リスト タイプ。</span><span class="sxs-lookup"><span data-stu-id="80dbb-123">The specific product recommendation list type that the demo data point is to generate.</span></span>                                                    | <ul><li><span data-ttu-id="80dbb-124">レコベストセリング</span><span class="sxs-lookup"><span data-stu-id="80dbb-124">RecoBestSelling</span></span></li><li><span data-ttu-id="80dbb-125">レコニュー</span><span class="sxs-lookup"><span data-stu-id="80dbb-125">RecoNew</span></span></li><li><span data-ttu-id="80dbb-126">レコトレンディング</span><span class="sxs-lookup"><span data-stu-id="80dbb-126">RecoTrending</span></span></li><li><span data-ttu-id="80dbb-127">レコカート</span><span class="sxs-lookup"><span data-stu-id="80dbb-127">RecoCart</span></span></li><li><span data-ttu-id="80dbb-128">レコピーポーオールソーバイ</span><span class="sxs-lookup"><span data-stu-id="80dbb-128">RecoPeopleAlsoBuy</span></span></li></ul> |
| <span data-ttu-id="80dbb-129">オペレーティングユニットナンバー</span><span class="sxs-lookup"><span data-stu-id="80dbb-129">OperatingUnitNumber</span></span> | <span data-ttu-id="80dbb-130">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="80dbb-130">:heavy_check_mark:</span></span> | <span data-ttu-id="80dbb-131">製品推奨事項が提示される特定の作業単位番号。</span><span class="sxs-lookup"><span data-stu-id="80dbb-131">The specific operating unit number where product recommendations are expected to be   surfaced.</span></span>                                        |                                                                              |
| <span data-ttu-id="80dbb-132">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="80dbb-132">Category</span></span>            |                    |    <span data-ttu-id="80dbb-133">特定のリストが返されるカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="80dbb-133">The category the specific list should be returned for.</span></span> <span data-ttu-id="80dbb-134">カテゴリが指定されていない場合、リストはナビゲーション階層の上部にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-134">If no category is specified, the list is for top of navigation hierarchy only.</span></span>    |                                                                              |
| <span data-ttu-id="80dbb-135">SeedItemId</span><span class="sxs-lookup"><span data-stu-id="80dbb-135">SeedItemId</span></span>          |                    |    <span data-ttu-id="80dbb-136">シードを必要とするリスト (RecoPeopleAlsoBuy および RecoCart) については、それらのリストの製品には追加の製品が表示されます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-136">For lists that require seed (RecoPeopleAlsoBuy and RecoCart), the product those lists should show additional products for.</span></span>            |                                                                              |
| <span data-ttu-id="80dbb-137">CustomerId</span><span class="sxs-lookup"><span data-stu-id="80dbb-137">CustomerId</span></span>          |                    |    <span data-ttu-id="80dbb-138">顧客識別子 (RecoPicks) を必要とするリスト。</span><span class="sxs-lookup"><span data-stu-id="80dbb-138">For lists that require a customer identifier (RecoPicks).</span></span>  <span data-ttu-id="80dbb-139">既定値 ' 0 ' はすべての顧客に適用されます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-139">The default value '0' applies to all customers.</span></span>          |                                                                              |
| <span data-ttu-id="80dbb-140">ItemIds</span><span class="sxs-lookup"><span data-stu-id="80dbb-140">ItemIds</span></span>             | <span data-ttu-id="80dbb-141">:ヘビー_チェック_マーク:</span><span class="sxs-lookup"><span data-stu-id="80dbb-141">:heavy_check_mark:</span></span> | <span data-ttu-id="80dbb-142">「;」で区切られ、結果として返される 1 つ以上の製品。</span><span class="sxs-lookup"><span data-stu-id="80dbb-142">One or more products to be returned as the result, separated by ';'.</span></span>                                                                  |                                                                              |

## <a name="customize-demo-data"></a><span data-ttu-id="80dbb-143">デモ データのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="80dbb-143">Customize demo data</span></span>
<span data-ttu-id="80dbb-144">本社でコンフィギュレーションされた製品およびカテゴリ情報を使用して、既定のデモ データを編集できます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-144">You can edit the default demo data with any product and category information configured in HQ.</span></span> <span data-ttu-id="80dbb-145">.csv を更新すると、顧客に返される製品推奨事項は変更をすぐに反映します。</span><span class="sxs-lookup"><span data-stu-id="80dbb-145">After you update the .csv, the product recommendations that are returned to customers will immediately reflect the changes.</span></span>

<span data-ttu-id="80dbb-146">拡張機能には、'RecoMockDataset.csv' と呼ばれるデータファイルが含まれています。これによりモックの推奨結果の出力に使用するデータセットを制御できます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-146">The extension contains a datafile called 'RecoMockDataset.csv', which allows you to control the dataset used to power the mock recommendations results.</span></span> <span data-ttu-id="80dbb-147">ファイル名は、**ext.Recommendations.DemoFilePath** 設定を使用して、拡張コンフィギュレーションによって制御できます。</span><span class="sxs-lookup"><span data-stu-id="80dbb-147">The file name can be controlled through extension configuration using the **ext.Recommendations.DemoFilePath** setting.</span></span> <span data-ttu-id="80dbb-148">これにより、コンフィギュレーション時に簡単に切り替えることができる複数のデータセットを利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="80dbb-148">This enables you to have multiple datasets available that can be switched between easily through configuration.</span></span>


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a><span data-ttu-id="80dbb-149">追加リソース</span><span class="sxs-lookup"><span data-stu-id="80dbb-149">Additional resources</span></span>

[<span data-ttu-id="80dbb-150">製品推奨事項の概要</span><span class="sxs-lookup"><span data-stu-id="80dbb-150">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="80dbb-151">Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する</span><span class="sxs-lookup"><span data-stu-id="80dbb-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="80dbb-152">製品推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="80dbb-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="80dbb-153">カスタマイズされた推奨事項の有効化</span><span class="sxs-lookup"><span data-stu-id="80dbb-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="80dbb-154">カスタマイズされた推奨事項のオプト アウト</span><span class="sxs-lookup"><span data-stu-id="80dbb-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="80dbb-155">"類似したルックを買う" 推奨を有効にする</span><span class="sxs-lookup"><span data-stu-id="80dbb-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="80dbb-156">POS での製品推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="80dbb-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="80dbb-157">トランザクション画面への推奨事項の追加</span><span class="sxs-lookup"><span data-stu-id="80dbb-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="80dbb-158">AI-ML 推奨事項結果の調整</span><span class="sxs-lookup"><span data-stu-id="80dbb-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="80dbb-159">収集された推奨事項の手動作成</span><span class="sxs-lookup"><span data-stu-id="80dbb-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="80dbb-160">製品推奨事項に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="80dbb-160">Product recommendations FAQ</span></span>](faq-recommendations.md)

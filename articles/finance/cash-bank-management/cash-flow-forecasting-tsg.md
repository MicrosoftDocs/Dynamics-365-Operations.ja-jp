---
title: キャッシュ フロー予測設定のトラブルシューティング
description: このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。 キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827317"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="08556-104">キャッシュ フロー予測設定のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="08556-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08556-105">このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。</span><span class="sxs-lookup"><span data-stu-id="08556-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="08556-106">キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。</span><span class="sxs-lookup"><span data-stu-id="08556-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="08556-107">キャッシュ フローが単一の法人に対してのみ表示される理由</span><span class="sxs-lookup"><span data-stu-id="08556-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="08556-108">キャッシュ フロー予測は、法人ごとに構成および計算されます。</span><span class="sxs-lookup"><span data-stu-id="08556-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="08556-109">Finance 分析情報の Power BI レポートおよびキャッシュ フロー予測機能が結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="08556-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="08556-110">キャッシュ フロー予測は、予測を確認したい法人ごとに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08556-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="08556-111">すべての法人におけるキャッシュ フロー予測の構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="08556-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="08556-112">または、キャッシュ フロー予測のすべての法人の構成を確認し、予定通りに設定されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="08556-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="08556-113">Power BI がすべてのキャッシュ フロー データを表示しないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="08556-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="08556-114">キャッシュ フロー予測が Power BI ビューに表示される前に、いくつかの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08556-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="08556-115">次のチェックリストを確認し、すべての手順が完了しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="08556-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="08556-116">各法人のキャッシュ フローを設定します。</span><span class="sxs-lookup"><span data-stu-id="08556-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="08556-117">一般会計パラメーターで、システム通貨とシステムの為替レート タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="08556-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="08556-118">元帳の会計通貨と為替レート タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="08556-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="08556-119">取引通貨と会計通貨間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="08556-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="08556-120">会計通貨とシステム通貨間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="08556-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="08556-121">会計通貨と各銀行通貨間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="08556-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="08556-122">以前のバージョンでキャッシュ フロー Power BI を使用できたのに、今はなぜ空白なのですか。</span><span class="sxs-lookup"><span data-stu-id="08556-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="08556-123">エンティティ格納の "キャッシュ フロー測定 V2" と "LedgerCovLiquidityMeasurement" 測定が構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="08556-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="08556-124">エンティティ ストアの使用方法については、[エンティティストアとのPower BI 統合](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08556-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="08556-125">Power BI コンテンツを表示するのに必要なすべての手順が完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="08556-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="08556-126">詳細については、[現金の概要 Power BI コンテンツ](Cash-Overview-Power-BI-content.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08556-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="08556-127">エンティティ格納のエンティティを更新しましたか。</span><span class="sxs-lookup"><span data-stu-id="08556-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="08556-128">データが最新かつ正確であるかを確認するために、エンティティを定期的に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08556-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="08556-129">特定のエンティティを手動で更新するには、**システム管理 \> 設定 \> エンティティ格納** の順に移動して、エンティティを選択してから **更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="08556-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="08556-130">データは自動的に更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="08556-130">The data can also be updated automatically.</span></span> <span data-ttu-id="08556-131">**エンティティ格納** ページで、**自動更新を有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="08556-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="08556-132">キャッシュフロー予測を計算する際に使用すべき計算方法はどれですか?</span><span class="sxs-lookup"><span data-stu-id="08556-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="08556-133">キャッシュ フロー予測計算方法には、2 つの重要な選択オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="08556-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="08556-134">**新規** オプションの場合、新規ドキュメントおよび前回のバッチ ジョブ実行後に変更があったドキュメントのキャッシュ フロー予測を計算します。</span><span class="sxs-lookup"><span data-stu-id="08556-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="08556-135">このオプションは、処理するドキュメントのサブセットが小さいため、短時間で終わる傾向があります。</span><span class="sxs-lookup"><span data-stu-id="08556-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="08556-136">**合計** オプションでは、システム内のすべてのドキュメントに対してキャッシュ フロー予測を再計算します。</span><span class="sxs-lookup"><span data-stu-id="08556-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="08556-137">このオプションでは、完了する作業が多いため時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="08556-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="08556-138">キャッシュ フロー予測の定期バッチ ジョブのパフォーマンスを向上させるにはどうすればいいですか?</span><span class="sxs-lookup"><span data-stu-id="08556-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="08556-139">キャッシュ フローは毎日一回、**新規** 計算方法を使ってオフピーク時間中に実行することを推奨しています。</span><span class="sxs-lookup"><span data-stu-id="08556-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="08556-140">週に 6 回このアプローチを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="08556-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="08556-141">次に、毎週一回アクティビティが最も少ない日に、**合計** 計算方法を使ってキャッシュ フロー予測を実行します。</span><span class="sxs-lookup"><span data-stu-id="08556-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


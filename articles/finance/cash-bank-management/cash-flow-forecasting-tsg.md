---
title: キャッシュ フロー予測設定のトラブルシューティング
description: このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。 キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232492"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="027cd-104">キャッシュ フロー予測設定のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="027cd-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="027cd-105">このトピックでは、キャッシュフロー予測を構成する際の質問に対する回答をご覧いただけます。</span><span class="sxs-lookup"><span data-stu-id="027cd-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="027cd-106">キャッシュ フロー、キャッシュ フローの更新、およびキャッシュ フロー Power BI の設定に関するよく寄せられる質問 (FAQ) を取り上げています。</span><span class="sxs-lookup"><span data-stu-id="027cd-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="027cd-107">キャッシュ フローが単一の法人に対してのみ表示される理由</span><span class="sxs-lookup"><span data-stu-id="027cd-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="027cd-108">キャッシュ フロー予測は、法人ごとに構成および計算されます。</span><span class="sxs-lookup"><span data-stu-id="027cd-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="027cd-109">Finance 分析情報の Power BI レポートおよびキャッシュ フロー予測機能が結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="027cd-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="027cd-110">キャッシュ フロー予測は、予測を確認したい法人ごとに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="027cd-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="027cd-111">すべての法人におけるキャッシュ フロー予測の構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="027cd-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="027cd-112">または、キャッシュ フロー予測のすべての法人の構成を確認し、予定通りに設定されているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="027cd-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="027cd-113">Power BI がすべてのキャッシュ フロー データを表示しないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="027cd-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="027cd-114">キャッシュ フロー予測が Power BI ビューに表示される前に、いくつかの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="027cd-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="027cd-115">次のチェックリストを確認し、すべての手順が完了しているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="027cd-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="027cd-116">各法人のキャッシュ フローを設定します。</span><span class="sxs-lookup"><span data-stu-id="027cd-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="027cd-117">一般会計パラメーターで、システム通貨とシステムの為替レート タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="027cd-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="027cd-118">元帳の会計通貨と為替レート タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="027cd-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="027cd-119">取引通貨と会計通貨間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="027cd-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="027cd-120">会計通貨とシステム通貨間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="027cd-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="027cd-121">会計通貨と各銀行通貨間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="027cd-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="027cd-122">以前のバージョンでキャッシュ フロー Power BI を使用できたのに、今はなぜ空白なのですか。</span><span class="sxs-lookup"><span data-stu-id="027cd-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="027cd-123">エンティティ格納の "キャッシュ フロー測定 V2" と "LedgerCovLiquidityMeasurement" 測定が構成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="027cd-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="027cd-124">エンティティ格納でデータを使用する方法に関しては、[エンティティ格納を使用した Power BI 統合](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) を参照し、Power BI のコンテンツを表示するのに必要なすべての手順を完了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="027cd-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="027cd-125">詳細については、[現金の概要 Power BI コンテンツ](Cash-Overview-Power-BI-content.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="027cd-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="027cd-126">エンティティ格納のエンティティを更新しましたか。</span><span class="sxs-lookup"><span data-stu-id="027cd-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="027cd-127">データが最新かつ正確であるかを確認するために、エンティティを定期的に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="027cd-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="027cd-128">特定のエンティティを手動で更新するには、**システム管理 \> 設定 \> エンティティ格納** の順に移動して、エンティティを選択してから **更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="027cd-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="027cd-129">データは自動的に更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="027cd-129">The data can also be updated automatically.</span></span> <span data-ttu-id="027cd-130">**エンティティ格納** ページで、**自動更新を有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="027cd-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
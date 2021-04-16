---
title: キャッシュ フローの予測 (プレビュー版)
description: このトピックでは、キャッシュ フローの予測機能について説明します。
author: ShivamPandey-msft
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6e4713aa4662714d1b2a3eeb62adce8608907054
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811414"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="10379-103">キャッシュ フローの予測 (プレビュー版)</span><span class="sxs-lookup"><span data-stu-id="10379-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="10379-104">キャッシュ フローは、すべての業務にとって重要です。</span><span class="sxs-lookup"><span data-stu-id="10379-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="10379-105">利益を上げている企業でも、差し迫った要求に合わせたキャッシュ フローを維持できなければ、債務超過に陥る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="10379-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="10379-106">Finance Insights のキャッシュ フロー予測機能を使用すると、現金残高を効果的に監視および管理する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="10379-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="10379-107">この機能は、機械学習を利用して、企業がキャッシュ フローを従来よりも正確に予測できるようにするものです。</span><span class="sxs-lookup"><span data-stu-id="10379-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="10379-108">また、経営者が現在のキャッシュ ポジションのコンテキストの中で機会を最適化する意思決定を行う場合にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="10379-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="10379-109">ほとんどの企業にとって、キャッシュ フローの管理とキャッシュ フローの予測を実行することは、冗長で反復的な手作業のプロセスです。</span><span class="sxs-lookup"><span data-stu-id="10379-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="10379-110">多くの企業は、複雑さの度合いが異なる Microsoft Excel ソリューションに依存しています。</span><span class="sxs-lookup"><span data-stu-id="10379-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="10379-111">キャッシュフローを正確に予測するにあたっては、次のような課題があります:</span><span class="sxs-lookup"><span data-stu-id="10379-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="10379-112">データが以下のような複数の場所に分散しているため、意思決定者が利用できません:</span><span class="sxs-lookup"><span data-stu-id="10379-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="10379-113">会計またはエンタープライズ リソース計画システム</span><span class="sxs-lookup"><span data-stu-id="10379-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="10379-114">ファイナンシャル プランニング ソフトウェア</span><span class="sxs-lookup"><span data-stu-id="10379-114">Financial planning software</span></span>
  - <span data-ttu-id="10379-115">Excel</span><span class="sxs-lookup"><span data-stu-id="10379-115">Excel</span></span>
  - <span data-ttu-id="10379-116">その他のソフトウェア アプリケーション</span><span class="sxs-lookup"><span data-stu-id="10379-116">Additional software applications</span></span> 
- <span data-ttu-id="10379-117">予測は、各ドメインや部門内で「縦割り」で管理されている内部の知識に基づいています。</span><span class="sxs-lookup"><span data-stu-id="10379-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="10379-118">財務が実現した後のキャッシュフロー予測の精度を測定することは、不確実で困難です。</span><span class="sxs-lookup"><span data-stu-id="10379-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="10379-119">キャッシュ フロー予測機能の詳細</span><span class="sxs-lookup"><span data-stu-id="10379-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="10379-120">キャッシュフロー予の測機能には以下の機能があります。</span><span class="sxs-lookup"><span data-stu-id="10379-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="10379-121">外部システムのキャッシュ フローデータをに簡単に  Dynamics 365 Finance に統合できます。</span><span class="sxs-lookup"><span data-stu-id="10379-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="10379-122">キャッシュフロー予測では、データのインポート/エクスポート フレームワークを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="10379-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="10379-123">このフレームワークを使うと、Excel OData との統合が簡単にできます。</span><span class="sxs-lookup"><span data-stu-id="10379-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="10379-124">また、複数のソースからのデータを組み合わせて、包括的なキャッシュ フロー ソリューションを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="10379-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="10379-125">インテリジェントなキャッシュ ポジションを導入します。</span><span class="sxs-lookup"><span data-stu-id="10379-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="10379-126">キャッシュ ポジションは、顧客の支払い行動に基づいて作成され、企業の口座に現金がいつ入金されるかを予測することができます。</span><span class="sxs-lookup"><span data-stu-id="10379-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="10379-127">また、仕入先への支払履歴パターンを分析して、将来の請求書や注文がいつ支払われるかを予測します。</span><span class="sxs-lookup"><span data-stu-id="10379-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="10379-128">AI Builder との自動統合による時系列予測を用いた長期予測に向けたインテリジェントなキャッシュフロー予測を導入します。</span><span class="sxs-lookup"><span data-stu-id="10379-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="10379-129">特定のキャッシュ フロー ポジション、または予測を保存、編集し、実際の財務と予測パフォーマンスを簡単に比較・測定する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="10379-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="10379-130">スナップショット比較を使用して、what-if 分析を可能にします。</span><span class="sxs-lookup"><span data-stu-id="10379-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="10379-131">たとえば、キャッシュフローの楽観的な見方、悲観的な見方、最も現実的な見方を表す複数のスナップショットを作成し、その違いを比較表示できます。</span><span class="sxs-lookup"><span data-stu-id="10379-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="10379-132">複数の通貨、法人を横断したキャッシュ フロー予測を表示し、銀行口座に関連するキャッシュ フローをフィルター処理して表示する機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="10379-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="10379-133">財務分析コードに関連する銀行口座をフィルター処理して表示できます。</span><span class="sxs-lookup"><span data-stu-id="10379-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="10379-134">Dynamics 365 Finance のキャッシュ フロー予測機能は、冗長で複雑で反復的なキャッシュ フロー予測をシンプルで自動化されたプロセスに変えることができます。</span><span class="sxs-lookup"><span data-stu-id="10379-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="10379-135">キャッシュ フロー予測の最も面倒な部分を自動化することで、重要な意思決定に集中し、目的のビジネス成果を生み出すことができます。</span><span class="sxs-lookup"><span data-stu-id="10379-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="10379-136">キャッシュフロー予測の分析コードを設定する</span><span class="sxs-lookup"><span data-stu-id="10379-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="10379-137">**キャッシュフロー予測の設定** ページの新しいタブでは、**キャッシュ フローの予測** ワークスペースでフィルター処理に使用する財務分析コードをコントロールできます。</span><span class="sxs-lookup"><span data-stu-id="10379-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="10379-138">このタブは、キャッシュ フロー予測機能が有効になっている場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="10379-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="10379-139">**分析コード** タブで、フィルター処理に使用する分析コードを一覧から選択し、方向キーを使用して右側の列に移動します。</span><span class="sxs-lookup"><span data-stu-id="10379-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="10379-140">キャッシュ フロー予測データのフィルター処理には、2 つの分析コードのみを選択できます。</span><span class="sxs-lookup"><span data-stu-id="10379-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="10379-141">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="10379-141">Privacy notice</span></span>
<span data-ttu-id="10379-142">プレビューは (1) Dynamics 365 Finance and Operations サービスを下回るプライバシーおよび少ないセキュリティ対策を使用している場合があり、(2) このサービスのためにサービス レベル アグリーメント (SLA) には含まれておらず、(3) 個人データや、その他の法律上またはコンプライアンス要件の対象となるデータの処理に使用されず、(4) サポートが制限されます。</span><span class="sxs-lookup"><span data-stu-id="10379-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Supply Chain Management の価格決定エンジンとのオンデマンド同期
description: このトピックでは、Dynamics 365 Sales からの Microsoft Dynamics 365 Supply Chain Management の価格決定エンジンを使用する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130656"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a><span data-ttu-id="1e6ed-103">Supply Chain Management の価格決定エンジンとのオンデマンド同期</span><span class="sxs-lookup"><span data-stu-id="1e6ed-103">Sync on-demand with the Supply Chain Management pricing engine</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="1e6ed-104">Microsoft Dynamics 365 Supply Chain Managementには、売買契約、価格リスト、顧客ロイヤルティ プログラム、プロモーション、および割引を処理する価格決定エンジンが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-104">Microsoft Dynamics 365 Supply Chain Management includes a pricing engine that handles trade agreements, price lists, customer loyalty programs, promotions, and discounts.</span></span> <span data-ttu-id="1e6ed-105">価格決定エンジンでは、複雑なルールを使用して、特定の見積または注文に対して最適な価格を決定します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-105">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span> <span data-ttu-id="1e6ed-106">デュアル書き込みを使用する場合は、Dynamics 365 Sales の 見積書 と 注文 ページで、Dynamics 365 Supply Chain Management からの静的な価格決定または価格決定エンジンのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-106">When you use dual-write, you use either static pricing or the pricing engine from Dynamics 365 Supply Chain Management on the Quote and Order pages in Dynamics 365 Sales.</span></span>

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a><span data-ttu-id="1e6ed-107">Sales の Supply Chain Management からの価格決定エンジンを使用する</span><span class="sxs-lookup"><span data-stu-id="1e6ed-107">Use the pricing engine from Supply Chain Management in Sales</span></span>

1. <span data-ttu-id="1e6ed-108">Sales で、**販売\>注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-108">In Sales, go to **Sales \> Orders**.</span></span>
2. <span data-ttu-id="1e6ed-109">新規注文を作成するには **新規** を選択するか、**自分の注文** リストから既存の注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-109">Select **New** to create a new order, or select an existing order in the **My Orders** list.</span></span>
3. <span data-ttu-id="1e6ed-110">新しい注文明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-110">Add a new order line.</span></span>
4. <span data-ttu-id="1e6ed-111">新しい注文を作成する場合は、アクション ウィンドウで **注文の価格** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-111">If you're creating a new order, select **Price Order** on the Action Pane.</span></span> <span data-ttu-id="1e6ed-112">既存の注文を更新する場合は、アクション ウィンドウで **再計算** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-112">If you're updating an existing order, select **Recalculate** on the Action Pane.</span></span>

    <span data-ttu-id="1e6ed-113">以下の列は、自動入力されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-113">The following columns are automatically filled in:</span></span>

    + <span data-ttu-id="1e6ed-114">詳細金額</span><span class="sxs-lookup"><span data-stu-id="1e6ed-114">Detail Amount</span></span>
    + <span data-ttu-id="1e6ed-115">割引率</span><span class="sxs-lookup"><span data-stu-id="1e6ed-115">Discount %</span></span>
    + <span data-ttu-id="1e6ed-116">割引</span><span class="sxs-lookup"><span data-stu-id="1e6ed-116">Discount</span></span>
    + <span data-ttu-id="1e6ed-117">送料を差し引いた金額</span><span class="sxs-lookup"><span data-stu-id="1e6ed-117">Pre-Freight Amount</span></span>
    + <span data-ttu-id="1e6ed-118">送料</span><span class="sxs-lookup"><span data-stu-id="1e6ed-118">Freight Amount</span></span>
    + <span data-ttu-id="1e6ed-119">税合計</span><span class="sxs-lookup"><span data-stu-id="1e6ed-119">Total Tax</span></span>
    + <span data-ttu-id="1e6ed-120">合計金額</span><span class="sxs-lookup"><span data-stu-id="1e6ed-120">Total Amount</span></span>
    
5. <span data-ttu-id="1e6ed-121">システムで取引と販売契約を考慮して価格を計算するには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-121">To ensure that the system considers trade and sales agreements to calculate the price:</span></span>
    1. <span data-ttu-id="1e6ed-122">Supply Chain Management 環境に移動します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-122">Navigate to your Supply Chain Management environment.</span></span>
    2. <span data-ttu-id="1e6ed-123">**売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-123">Navigate to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    3. <span data-ttu-id="1e6ed-124">サイド ナビゲーション バーの **価格** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-124">Select the **Prices** tab in the side navigation bar.</span></span>
    4. <span data-ttu-id="1e6ed-125">**売買契約評価** クイック タブで、**マニュアル エントリ** オプションのチェックを外します。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-125">Under the **Trade agreement evaluation** fastab, uncheck the **Manual entry** option.</span></span>

## <a name="how-it-works"></a><span data-ttu-id="1e6ed-126">この機能の動作</span><span class="sxs-lookup"><span data-stu-id="1e6ed-126">How it works</span></span>

<span data-ttu-id="1e6ed-127">Sales で **注文の価格** を選択すると、Supply Chain Management の **販売注文 \> 表示** タブの **合計** 機能が、関連付けられている販売注文に対して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-127">When you select **Price Order** in Sales, the **Totals** function on the **Sales Order \> View** tab in Supply Chain Management is called for the associated sales order.</span></span> <span data-ttu-id="1e6ed-128">Sales の注文合計の値は、Supply Chain Management の対応列への入力に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-128">The values in the order total in Sales are used to fill in the corresponding columns in Supply Chain Management.</span></span>

<span data-ttu-id="1e6ed-129">Supply Chain Management で販売注文の合計が計算されるとき、顧客や販売注文に一覧表示されている製品の既存の売買契約と販売契約書がこの計算で評価されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-129">When the sales order total is calculated in Supply Chain Management, the calculation evaluates the existing trade agreements and sales agreements for the customer and the products that are listed in the sales order.</span></span> <span data-ttu-id="1e6ed-130">この情報は、合計の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-130">This information is used to calculate the totals.</span></span> <span data-ttu-id="1e6ed-131">**注文の価格** が選択された場合、Supply Chain Management で行われたすべての設定が販売によって自動的に反映されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-131">When **Price Order** is selected, Sales automatically reflects all the setup that has been done in Supply Chain Management.</span></span>

## <a name="limitations"></a><span data-ttu-id="1e6ed-132">制限</span><span class="sxs-lookup"><span data-stu-id="1e6ed-132">Limitations</span></span>

<span data-ttu-id="1e6ed-133">Sales の列が入力されている場合は、次の制限事項が適用されます。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-133">When the columns in Sales are filled in, the following limitations apply:</span></span>

+ <span data-ttu-id="1e6ed-134">Supply Chain Management での請求金額と請求金額配賦の設定は、Sales ではレプリケートされません。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-134">The setup of charges and charge allocations in Supply Chain Management isn't replicated in Sales.</span></span>
+ <span data-ttu-id="1e6ed-135">価格決定では、Supply Chain Management の販売注文行ページの **小売チャネル** 列で指定された特別な小売価格は考慮しません。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-135">Pricing doesn't consider special retail pricing that is specified in the **Retail Channel** column on the sales order line page in Supply Chain Management.</span></span>
+ <span data-ttu-id="1e6ed-136">Supply Chain Management の **取引手当管理** セクションで定義されている割引は考慮されません。</span><span class="sxs-lookup"><span data-stu-id="1e6ed-136">Discounts that are defined in the **Trade Allowance Management** section of Supply Chain Management aren't considered.</span></span>

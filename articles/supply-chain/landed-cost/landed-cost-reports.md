---
title: 陸揚原価レポート
description: このトピックでは、陸揚原価モジュールで使用できるさまざまなタイプのレポートを検索して使用する方法について説明します。
author: sherry-zheng
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 41588b7dc037f6d748bac818f8707540ce8afe8d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020962"
---
# <a name="landed-cost-reports"></a><span data-ttu-id="8ac72-103">陸揚原価レポート</span><span class="sxs-lookup"><span data-stu-id="8ac72-103">Landed cost reports</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="outstanding-invoices"></a><span data-ttu-id="8ac72-104">未払い請求書</span><span class="sxs-lookup"><span data-stu-id="8ac72-104">Outstanding invoices</span></span>

<span data-ttu-id="8ac72-105">未払い請求書レポートには、各航海に関連付けられているさまざまな原価レベルのすべての未払い請求書の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-105">The outstanding invoices report contains a list of all outstanding invoices of the various cost levels that are associated with every voyage.</span></span> <span data-ttu-id="8ac72-106">これは、航海および航海コストを元帳トランザクションの一覧と共に、定期的に調整するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-106">It's used to reconcile the voyage and voyage costs together with the ledger transactions list on a regular basis.</span></span> <span data-ttu-id="8ac72-107">間接費が請求された後、レポートから削除されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-107">After an overhead cost has been invoiced, it's removed from the report.</span></span>

<span data-ttu-id="8ac72-108">未払い請求書レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-108">To generate an outstanding invoices report, follow these steps.</span></span>

1. <span data-ttu-id="8ac72-109">**陸揚原価 \> レポート \> 追跡 \> 未払い請求書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-109">Go to **Landed cost \> Reports \> Tracking \> Outstanding invoices**.</span></span>
1. <span data-ttu-id="8ac72-110">**未払い請求書** ダイアログ ボックスの、**現在の日付** フィールドで、日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-110">In the **Outstanding invoices** dialog box, in the **As at date** field, specify a date.</span></span> <span data-ttu-id="8ac72-111">その日付以前までに未払いだった請求書はすべて出力に含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-111">Any invoice that was outstanding on or before that date will be included in the output.</span></span>
1. <span data-ttu-id="8ac72-112">**表示** で、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-112">Under **Show**, select one of the following options:</span></span>

    - <span data-ttu-id="8ac72-113">**未請求の原価** – 見積原価値はあるが実際原価がない、請求済出荷の原価を含めます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-113">**Cost not invoiced** – Include costs for invoiced shipments that have an estimated cost value but no actual cost.</span></span>
    - <span data-ttu-id="8ac72-114">**未請求の在庫** – 請求はされているが、発注書がまだ受け取られていない原価を含めます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-114">**Stock not invoiced** – Include costs that have been invoiced, but that the purchase order hasn't yet been received for.</span></span>
    - <span data-ttu-id="8ac72-115">**すべて未請求** – **未請求の原価** オプションおよび **未請求の在庫** オプションの両方の結果を含めます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-115">**All not invoiced** – Include the results of both the **Cost not invoiced** option and the **Stock not invoiced** option.</span></span>

1. <span data-ttu-id="8ac72-116">**新しい原価を含める** オプションを *はい* に設定して、実際原価がまだなく、その在庫がまだ受け取られていない原価を含めます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-116">Set the **Include new costs** option to *Yes* to include costs that don't yet have an actual cost, and that inventory hasn't been received for.</span></span> <span data-ttu-id="8ac72-117">*いいえ* に設定すると、請求された原価だけがレポートに含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-117">If you set it to *No*, the report will include only costs that have been invoiced.</span></span>
1. <span data-ttu-id="8ac72-118">**表示** セクションで、レポートに含める各タイプの詳細を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8ac72-118">In the **View** section, enable each type of detail that you want to include on the report.</span></span>
1. <span data-ttu-id="8ac72-119">Microsoft Dynamics 365 Supply Chain Management の他のタイプのレポートと同様に、**出力先** クイック タブを使用してレポートの出力形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-119">As you do for other types of reports in Microsoft Dynamics 365 Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="8ac72-120">Supply Chain Management の他のタイプのレポートと同様に、**対象に含めるレコード** クイック タブを使用して、レポートに含めるレコードをさらに制限します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-120">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="8ac72-121">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-121">Select **OK** to generate the report.</span></span>

## <a name="activityprovider-analysis-reports"></a><span data-ttu-id="8ac72-122">活動/プロバイダー分析レポート</span><span class="sxs-lookup"><span data-stu-id="8ac72-122">Activity/provider analysis reports</span></span>

<span data-ttu-id="8ac72-123">活動/プロバイダー分析レポートを使用すると、各プロバイダーの時間見積が正しいことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-123">The activity/provider analysis reports let you review the accuracy of your time estimates for each provider.</span></span>

<span data-ttu-id="8ac72-124">活動/プロバイダー分析レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-124">To generate an activity/provider analysis report, follow these steps.</span></span>

1. <span data-ttu-id="8ac72-125">作成するレポートのタイプに応じて、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8ac72-125">Depending on the type of report that you want to create, follow one of these steps:</span></span>

    - <span data-ttu-id="8ac72-126">**陸揚原価 \> レポート \> 活動/プロバイダーを活動別に分析する** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-126">Go to **Landed cost \> Reports \> Analysis of activity/provider by activity**.</span></span> <span data-ttu-id="8ac72-127">この場合、時間見積は活動別にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-127">In this case, the time estimates will be grouped by activity.</span></span>
    - <span data-ttu-id="8ac72-128">**陸揚原価 \> レポート \> 活動/プロバイダーをプロバイダー別に分析する** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-128">Go to **Landed cost \> Reports \> Analysis of activity/provider by provider**.</span></span> <span data-ttu-id="8ac72-129">この場合、時間見積はプロバイダー別にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-129">In this case, the time estimates will be grouped by provider.</span></span>

    <span data-ttu-id="8ac72-130">**活動/プロバイダーを活動別に分析する** ダイアログ ボックスまたは **活動/プロバイダーをプロバイダー別に分析する** ダイアログ ボックスのいずれかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-130">Either the **Analysis of activity/provider by activity** dialog box or the **Analysis of activity/provider by provider** dialog box appears.</span></span> <span data-ttu-id="8ac72-131">どちらのダイアログ ボックスも同じオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-131">Both dialog boxes provide the same options.</span></span>

1. <span data-ttu-id="8ac72-132">Supply Chain Management の他のタイプのレポートと同様に、**出力先** クイック タブを使用してレポートの出力形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-132">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="8ac72-133">Supply Chain Management の他のタイプのレポートと同様に、**対象に含めるレコード** クイック タブを使用して、レポートに含めるレコードをさらに制限します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-133">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="8ac72-134">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-134">Select **OK** to generate the report.</span></span>

## <a name="voyage-costing-reports"></a><span data-ttu-id="8ac72-135">航海の原価計算レポート</span><span class="sxs-lookup"><span data-stu-id="8ac72-135">Voyage costing reports</span></span>

<span data-ttu-id="8ac72-136">航海の原価計算レポートには、レポートを生成するときに選択するオプションに応じて、品目の原価と、フォリオ、出荷コンテナー、または航海ごとの輸入原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-136">The voyage costing reports show the cost of the items and the import costs per folio, shipping container, or voyage, depending on the options that you select when you generate the report.</span></span> <span data-ttu-id="8ac72-137">各航海の原価計算レポートでは、航海の見積原価と実際原価を比較表示でき、複数の識別要因によって細分できます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-137">Each voyage costing report lets you view the estimated cost of a voyage versus the actual cost, and it can be broken down by the several identifying factors.</span></span>

<span data-ttu-id="8ac72-138">航海の原価計算レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-138">To generate a voyage costing report, follow these steps.</span></span>

1. <span data-ttu-id="8ac72-139">作成するレポートのタイプに応じて、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8ac72-139">Depending on the type of report that you want to create, follow one of these steps:</span></span>

    - <span data-ttu-id="8ac72-140">**陸揚原価 \> レポート \> 原価計算 \> 個々の原価による航海の原価計算** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-140">Go to **Landed cost \> Reports \> Costing \> Voyage costing by individual cost**.</span></span> <span data-ttu-id="8ac72-141">この場合、個々の原価オプションには、原価タイプ コードごとの各原価領域のインポート原価が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-141">In this case, the individual cost option will show import costs per cost area per cost type code.</span></span>
    - <span data-ttu-id="8ac72-142">**陸揚原価 \> レポート \> 原価計算 \> レポート カテゴリによる航海の原価計算** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-142">Go to **Landed cost \> Reports \> Costing \> Voyage costing by reporting category**.</span></span> <span data-ttu-id="8ac72-143">この場合、インポート原価はさまざまなレポート カテゴリに細分されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-143">In this case, the import cost will be broken down into the various reporting categories.</span></span> <span data-ttu-id="8ac72-144">原価タイプは、レポート カテゴリ別にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-144">Cost types are grouped by reporting categories.</span></span>

    <span data-ttu-id="8ac72-145">**個々の原価による航海の原価計算** ダイアログ ボックスまたは **レポート カテゴリによる航海の原価計算** ダイアログ ボックスのいずれかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-145">Either the **Voyage costing by individual cost** dialog box or the **Voyage costing by reporting category** dialog box appears.</span></span> <span data-ttu-id="8ac72-146">これらのダイアログ ボックスは類似しています。</span><span class="sxs-lookup"><span data-stu-id="8ac72-146">These dialog boxes are similar.</span></span> <span data-ttu-id="8ac72-147">この手順の残りの部分では、すべての違いを確認します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-147">Any differences are noted in the rest of this procedure.</span></span>

1. <span data-ttu-id="8ac72-148">**レポート カテゴリによる航海の原価計算** ダイアログ ボックスを開いた場合、**原価** フィールドで、次のいずれかの値を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-148">If you opened the **Voyage costing by reporting category** dialog box, in the **Cost** field, select one of the following values:</span></span>

    - <span data-ttu-id="8ac72-149">**原価価値** – この値は、自動で原価を使用して計算されるか、手動で原価領域で作成されるかのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="8ac72-149">**Cost value** – The value is either calculated by using auto costs or manually created in the cost area.</span></span>
    - <span data-ttu-id="8ac72-150">**見積済** – 商品の入庫後に、見積原価が設定されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-150">**Estimated** – After the goods have been received, the estimated cost is set.</span></span>
    - <span data-ttu-id="8ac72-151">**実際** – 注文が請求された後、実際原価が請求書の原価に設定されます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-151">**Actual** – After the order has been invoiced, the actual cost is set to the cost on the invoice.</span></span>
    - <span data-ttu-id="8ac72-152">**最良** – 前の 3 つのうち最も正確なオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-152">**Best** – The system will use whichever of the previous three options is most accurate.</span></span> <span data-ttu-id="8ac72-153">(このオプションを選択することをお勧めします。)</span><span class="sxs-lookup"><span data-stu-id="8ac72-153">(We recommend that you select this option.)</span></span>

1. <span data-ttu-id="8ac72-154">**品目別** オプションを *はい* に設定して、各品目の原価を表示します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-154">Set the **Per item** option to *Yes* to show the cost of each item.</span></span> <span data-ttu-id="8ac72-155">このオプションを *いいえ* に設定して、航海ごとの原価を表示します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-155">Set it to *No* to show costs per voyage.</span></span>
1. <span data-ttu-id="8ac72-156">**表示** セクションで、原価を細分するカテゴリを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-156">In the **View** section, select the categories to break down the cost by.</span></span>
1. <span data-ttu-id="8ac72-157">**分析コード** セクションで、レポートに含める分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-157">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="8ac72-158">Supply Chain Management の他のタイプのレポートと同様に、**出力先** クイック タブを使用してレポートの出力形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-158">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="8ac72-159">Supply Chain Management の他のタイプのレポートと同様に、**対象に含めるレコード** クイック タブを使用して、レポートに含めるレコードをさらに制限します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-159">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="8ac72-160">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-160">Select **OK** to generate the report.</span></span>

## <a name="shipping-container-receipts-list"></a><span data-ttu-id="8ac72-161">出荷コンテナーの入庫リスト</span><span class="sxs-lookup"><span data-stu-id="8ac72-161">Shipping container receipts list</span></span>

<span data-ttu-id="8ac72-162">出荷コンテナーの入庫リストには、予定日または予定日以前に未入庫の数量がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-162">The shipping container receipts list contains all unreceived quantities that are due on or before an expected date.</span></span> <span data-ttu-id="8ac72-163">倉庫スタッフはこのレポートを使用して、出荷コンテナーの予定商品を識別できます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-163">Warehouse staff can use this report to identify the expected goods on a shipping container.</span></span> <span data-ttu-id="8ac72-164">また、出荷コンテナーに入庫された商品を手動で検証するために使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-164">It can also be used to manually validate goods as they are received on a shipping container.</span></span>

<span data-ttu-id="8ac72-165">出荷コンテナーの入庫リストを生成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8ac72-165">To generate a shipping container receipts list, follow these steps.</span></span>

1. <span data-ttu-id="8ac72-166">**陸揚原価 \> レポート \> 追跡 \> 出荷コンテナーの入庫リスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-166">Go to **Landed cost \> Reports \> Tracking \> Shipping container receipts list**.</span></span>
1. <span data-ttu-id="8ac72-167">**出荷コンテナーの入庫リスト** ダイアログ ボックスの **予定日** フィールドで、日付を指定します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-167">In the **Shipping container receipts list** dialog box, in the **Expected date** field, specify a date.</span></span> <span data-ttu-id="8ac72-168">その日付以前までに未入庫だった数量はすべて出力に含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-168">Any quantities that were unreceived on or before that date will be included in the output.</span></span>
1. <span data-ttu-id="8ac72-169">**分析コード** セクションで、レポートに含める分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-169">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="8ac72-170">Supply Chain Management の他のタイプのレポートと同様に、**出力先** クイック タブを使用してレポートの出力形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-170">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="8ac72-171">Supply Chain Management の他のタイプのレポートと同様に、**対象に含めるレコード** クイック タブを使用して、レポートに含めるレコードをさらに制限します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-171">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="8ac72-172">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-172">Select **OK** to generate the report.</span></span>

## <a name="expected-delivery-report"></a><span data-ttu-id="8ac72-173">配送予定レポート</span><span class="sxs-lookup"><span data-stu-id="8ac72-173">Expected delivery report</span></span>

<span data-ttu-id="8ac72-174">配送予定レポートには、航海、出荷コンテナー、フォリオ、品目、および配送予定日に関する基本情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-174">The expected delivery report contains basic information about the voyage, shipping container, folio, items, and expected date of delivery.</span></span>

<span data-ttu-id="8ac72-175">配送予定レポートを生成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-175">To generate an expected delivery report, follow these steps.</span></span>

1. <span data-ttu-id="8ac72-176">**陸揚原価 \> レポート \> 追跡 \> 配送予定** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-176">Go to **Landed cost \> Reports \> Tracking \> Expected Delivery**.</span></span>
1. <span data-ttu-id="8ac72-177">**予定配送** ダイアログ ボックスの **予定日** フィールドで、最終目的地倉庫への商品の配送が予定されている日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-177">In the **Expected delivery** dialog box, in the **Expected date** field, select the date when delivery of the goods to the final destination warehouse is expected.</span></span> <span data-ttu-id="8ac72-178">その日付以前に予定日があり、まだ入庫していない任意の航海明細行が、その出力に含まれます。</span><span class="sxs-lookup"><span data-stu-id="8ac72-178">Any voyage line that has an expected date on or before that date, and that hasn't yet been received, will be included in the output.</span></span>
1. <span data-ttu-id="8ac72-179">オプション: **仕入先勘定** フィールドで、特定の仕入先からの配送のみを含める仕入先勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-179">Optional: In the **Vendor account** field, select a vendor account to include only deliveries from a specific vendor.</span></span>
1. <span data-ttu-id="8ac72-180">**分析コード** セクションで、レポートに含める分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-180">In the **Dimensions** section, select the dimensions to include on the report.</span></span>
1. <span data-ttu-id="8ac72-181">Supply Chain Management の他のタイプのレポートと同様に、**出力先** クイック タブを使用してレポートの出力形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-181">As you do for other types of reports in Supply Chain Management, use the **Destination** FastTab to select the output format of the report.</span></span>
1. <span data-ttu-id="8ac72-182">Supply Chain Management の他のタイプのレポートと同様に、**対象に含めるレコード** クイック タブを使用して、レポートに含めるレコードをさらに制限します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-182">As you do for other types of reports in Supply Chain Management, use the **Records to include** FastTab to further limit the records that will be included on the report.</span></span>
1. <span data-ttu-id="8ac72-183">**OK** を選択してレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="8ac72-183">Select **OK** to generate the report.</span></span>

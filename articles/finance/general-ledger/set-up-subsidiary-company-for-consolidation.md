---
title: 連結のための関連法人の設定
description: このトピックでは、連結会社の勘定表の使用方法について説明します。
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 44bd184514b24a816cc83f6b0070a5e08163921b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204812"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a><span data-ttu-id="b2eb3-103">連結のための関連法人の設定</span><span class="sxs-lookup"><span data-stu-id="b2eb3-103">Set up a subsidiary legal entity for consolidation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2eb3-104">連結関連法人の勘定科目の作成方法は、関連会社の勘定科目表の構造が連結法人の勘定科目表をどの程度反映しているかにもよって異なります。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-104">The method that you use to prepare subsidiary accounts for consolidation depends in part on the extent to which the structure of the chart of accounts in the subsidiary legal entity reflects the chart of accounts in the consolidated legal entity.</span></span>

<span data-ttu-id="b2eb3-105">期末決算の一環として連結を開始する前に、期末決算の準備作業を完了させておきますが、連結が完了するまでは関連会社の決算は行わないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-105">Before you start a consolidation as part of period-end closing, complete the preparatory activities for the period-end closing, but don't close the subsidiary accounts until the consolidation is completed.</span></span> <span data-ttu-id="b2eb3-106">期末決算の詳細については、[期末に一般会計を決算する](close-general-ledger-at-period-end.md) と [会計年度期間を決算する](tasks/close-fiscal-year.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-106">For more information about period-end closing, see [Close the general ledger at period end](close-general-ledger-at-period-end.md) and [Close the fiscal year](tasks/close-fiscal-year.md).</span></span>

> [!NOTE]
>  <span data-ttu-id="b2eb3-107">複数の法人の決算を連結形式でまとめるには、Management Reporter for Microsoft Dynamics 365 Finance を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="b2eb3-108">Management Reporter を使用すると、法人間の連結財務レポートを作成したり、Excel を使用して他のソースから連結データをインポートしたり、Dynamics 365 Finance で連結処理を実行しなくても、金額を任意の数の報告通貨に変換したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a><span data-ttu-id="b2eb3-109">関連会社の主勘定と連結の主勘定をマッピングする</span><span class="sxs-lookup"><span data-stu-id="b2eb3-109">Map subsidiary main accounts to consolidated main accounts</span></span>

<span data-ttu-id="b2eb3-110">関連法人の勘定科目表が連結法人の勘定科目表に従属しない、連結法人の主勘定に関連法人の主勘定をマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-110">If the chart of accounts in the subsidiary legal entity doesn't follow the chart of accounts in the consolidated legal entity, you can map the main accounts in the subsidiary to the main accounts in the consolidated legal entity.</span></span>

1. <span data-ttu-id="b2eb3-111">*関連法人* で、**一般会計 \> 設定** \> **勘定科目表 \> 勘定科目表** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-111">In the *subsidiary legal entity*, go to **General ledger \> Setup** \> **Chart of accounts \> Chart of accounts**.</span></span>
2. <span data-ttu-id="b2eb3-112">勘定科目表を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-112">Select a chart of accounts.</span></span> <span data-ttu-id="b2eb3-113">**主要勘定** クイック タブで、主要勘定を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-113">On the **Main accounts** FastTab, select a main account, and then select **Edit**.</span></span>
3. <span data-ttu-id="b2eb3-114">連結主勘定にマッピングする必要がある関連会社の各主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-114">Select each subsidiary main account that must be mapped to a consolidated main account.</span></span> <span data-ttu-id="b2eb3-115">**連結勘定** フィールドの **全般** クイックタブので、選択した関連会社の主勘定の残高または取引の振替先となる連結法人の勘定を入力してください。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-115">On the **General** FastTab, in the **Consolidation account** field, enter the account in the consolidated legal entity that the balance or transactions of the selected subsidiary main account must be transferred to.</span></span> <span data-ttu-id="b2eb3-116">複数の関連会社口座に対して同じ連結主勘定を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-116">You can enter the same consolidated main account for several subsidiary accounts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b2eb3-117">マッピングされた関連会社口座の主勘定タイプが、連結法人の口座の主勘定タイプと異なる場合、**合計** の主勘定タイプを持つ口座の値が連結中に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-117">If the main account types of the subsidiary accounts that are mapped differ from the main account types of the accounts in the consolidated legal entity, the values of accounts that have a main account type of **Total** are overwritten during consolidation.</span></span>

4. <span data-ttu-id="b2eb3-118">連結関連会社の財務分析コードに基づく報告書及び財務諸表を作成します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-118">Prepare reports and financial statements for the consolidated legal entity that are based on financial dimensions.</span></span> <span data-ttu-id="b2eb3-119">次の手順に従って、関連会社で使用されている財務分析コードを連結法人の財務分析コードにマッピングします。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-119">Follow these steps to map the financial dimensions that are used in the subsidiary accounts to the financial dimensions in the consolidated legal entity:</span></span>

    1. <span data-ttu-id="b2eb3-120">*関連法人* で、**一般会計 \> 設定 \> 財務分析コード \> 財務分析コード** に移動し、財務分析コードを選択し、**財務分析コード値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-120">In the *subsidiary legal entity*, go to **General ledger \> Setup \> Financial dimensions \> Financial dimensions**, select a financial dimension, and then select **Financial dimension values**.</span></span>
    2. <span data-ttu-id="b2eb3-121">連結法人の各財務分析コード値にマッピングする財務分析コード値を選択します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-121">Select the financial dimension value to map to a different financial dimension value in the consolidated legal entity.</span></span>
    3. <span data-ttu-id="b2eb3-122">**全般** クイックタブの、**グループ分析コード** フィールドで、連結法人の財務分析コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-122">On the **General** FastTab, in the **Group dimension** field, enter the financial dimension in the consolidated legal entity.</span></span> <span data-ttu-id="b2eb3-123">連結の際、この財務分析コードは、関連法人で選択された財務分析コードを使用している取引および残高に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-123">During consolidation, this financial dimension will be assigned to transactions and balances that use the selected financial dimension in the subsidiary legal entity.</span></span> <span data-ttu-id="b2eb3-124">ここに入力した財務分析コードを連結法人で使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-124">The financial dimensions that you enter here must be used in the consolidated legal entity.</span></span> <span data-ttu-id="b2eb3-125">グループ財務分析コードとして使用される財務分析コードを、複数の関連会社の財務分析コードに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-125">You can assign the financial dimension that is used as the group financial dimension to several subsidiary financial dimensions.</span></span>

5. <span data-ttu-id="b2eb3-126">オンラインの連結を行う場合は、次の手順に従って、意図した方法で転送が行われることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-126">If you're doing an online consolidation, follow these steps to ensure that the transfers occur as you intend:</span></span>

    1. <span data-ttu-id="b2eb3-127">*連結法人* で、**一般会計\> 定期 \> 連結 \> 連結 \[エクスポート\]** に移動し、**\[オンライン\]を連結する** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-127">In the *consolidated legal entity*, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Export to\]** to open the **Consolidate \[Online\]** page.</span></span>
    2. <span data-ttu-id="b2eb3-128">**条件** タブで、**連結勘定を使用する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-128">On the **Criteria** tab, select the **Use consolidation account** check box.</span></span>
    3. <span data-ttu-id="b2eb3-129">**財務分析コード** タブで、適切な財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-129">On the **Financial dimensions** tab, select the appropriate financial dimensions.</span></span>
    4. <span data-ttu-id="b2eb3-130">選択した各財務分析コードについて、**セグメントの表示順**  フィールドに数字を入力して、分析コードが表示される順番を示します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-130">For each financial dimension that you select, enter a number in the **Segment order** field to indicate the order that the dimensions should appear in.</span></span>

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a><span data-ttu-id="b2eb3-131">関連会社と連結法人で同一の勘定科目を管理してください</span><span class="sxs-lookup"><span data-stu-id="b2eb3-131">Maintain the same chart of accounts in the subsidiary and consolidated legal entities</span></span>

<span data-ttu-id="b2eb3-132">関連法人の主な勘定科目もは、連結法人の主な勘定科目と同じ勘定番号と同じ構造の勘定科目を含んでいる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-132">The main accounts in the subsidiary legal entity might have the same account numbers and the same structure for the chart of accounts as the main accounts in the consolidated legal entity.</span></span> <span data-ttu-id="b2eb3-133">この場合、連結会社の主勘定と連結法人の主勘定を手動でマッピングする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-133">In this case, you don't have to manually map the main accounts in the subsidiary to the main accounts in the consolidated legal entity.</span></span>

<span data-ttu-id="b2eb3-134">連結を開始する前に、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-134">Before you start the consolidation, follow these steps.</span></span>

1. <span data-ttu-id="b2eb3-135">*連結法人* で、**一般会計\> 定期 \> 連結 \> 連結 \[エクスポート\]** に移動し、**\[オンライン\]を連結する** を開きます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-135">In the *consolidated legal entity*, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Export to\]** to open the **Consolidate \[Online\]** page.</span></span>
2. <span data-ttu-id="b2eb3-136">**連結勘定を使用する** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-136">Select the **Use consolidation account** check box.</span></span> <span data-ttu-id="b2eb3-137">連結を行う際に、トランザクションと残高が自動的に適切な口座に転送されます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-137">During consolidation, transactions and balances will automatically be transferred to the correct account.</span></span>

> [!NOTE]
> <span data-ttu-id="b2eb3-138">勘定が一致していない場合は、連結が中止されてメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-138">If the accounts don't correspond, the consolidation stops, and you receive a message.</span></span>

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a><span data-ttu-id="b2eb3-139">既存の勘定科目表を基に、連結法人で使用する勘定科目表を作成する</span><span class="sxs-lookup"><span data-stu-id="b2eb3-139">Create a chart of accounts for the consolidated legal entity, based on an existing chart of accounts</span></span>

<span data-ttu-id="b2eb3-140">勘定科目表が連結法人で既に作成されていない場合であっても、連結を実行できます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-140">You can do a consolidation even if a chart of accounts hasn't already been created in the consolidated legal entity.</span></span>

- <span data-ttu-id="b2eb3-141">連結法人に使用する勘定構造を作成する場合は、この構造に関連会社の口座をマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-141">If you've planned the account structure that you want to use in the consolidated legal entity, you can map the subsidiary accounts to this structure.</span></span>
- <span data-ttu-id="b2eb3-142">関連会社の勘定をマッピングしない場合は、連結法人に関連会社データが移管された際に、連結法人内の勘定が自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-142">If you don't map any subsidiary accounts, the accounts in the consolidated legal entity are automatically created when subsidiary data is transferred to the consolidated legal entity.</span></span> <span data-ttu-id="b2eb3-143">これらの勘定は、主勘定に基づきます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-143">These accounts are based on the main account.</span></span> <span data-ttu-id="b2eb3-144">関連会社勘定と同一の勘定番号を有する連結法人の勘定科目には、その後のデータが蓄積されています。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-144">Subsequent data is accumulated in accounts in the consolidated legal entity that have the same account number as the subsidiary accounts.</span></span>

<span data-ttu-id="b2eb3-145">勘定をマッピングしたかどうかにかかわらず、このタイプの連結を実行する前に、連結法人の **連結** ページの **連結勘定を使用する** チェックボックスをオフにしてください。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-145">Regardless of whether you've mapped accounts, clear the **Use consolidation account** check box on the **Consolidate** page in the consolidated legal entity before you run this type of consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="b2eb3-146">この方法を利用して、関連会社の1つの法人の勘定科目表から連結法人の勘定科目表を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-146">You can use this method to create a chart of accounts in the consolidated legal entity from the chart of accounts in one of the subsidiary legal entities.</span></span> <span data-ttu-id="b2eb3-147">(詳細については、[連結勘定グループと追加の連結勘定](../budgeting/consolidation-account-groups-consolidation-accounts.md)を参照。)  そして、各連結主勘定に適切な連結換算原則を設定し、すべての関連会社の連結を実行します。</span><span class="sxs-lookup"><span data-stu-id="b2eb3-147">(For more information, see [Consolidation account groups and additional consolidation accounts](../budgeting/consolidation-account-groups-consolidation-accounts.md).) Then assign an appropriate consolidation conversion principle to each consolidated main account, and run the consolidation for all the subsidiary legal entities.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
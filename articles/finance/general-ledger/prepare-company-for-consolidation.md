---
title: 連結プロセスで使用する法人を準備する
description: 連結の過程では、複数の法人勘定セットのトランザクションを 1 つの法人勘定セットにまとめます。 このトピックでは、連結に向けて法人を準備する方法について説明します。
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
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990310"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="a9573-104">連結プロセスで使用する法人を準備する</span><span class="sxs-lookup"><span data-stu-id="a9573-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9573-105">連結の過程では、複数の法人勘定セットのトランザクションを 1 つの法人勘定セットにまとめます。</span><span class="sxs-lookup"><span data-stu-id="a9573-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="a9573-106">このトピックでは、連結に向けて法人を準備する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a9573-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="a9573-107">複数の法人の決算を連結形式でまとめるには、Management Reporter for Microsoft Dynamics 365 Finance を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a9573-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="a9573-108">Management Reporter を使用すると、法人間の連結財務レポートを作成したり、Excel を使用して他のソースから連結データをインポートしたり、Dynamics 365 Finance で連結処理を実行しなくても、金額を任意の数の報告通貨に変換したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="a9573-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="a9573-109">連結法人からは、財務諸表などのレポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="a9573-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="a9573-110">ただし、毎日のトランザクションで連結法人を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a9573-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="a9573-111">連結法人のデータベースとは異なるデータベースを使用する法人のデータに統合できます。</span><span class="sxs-lookup"><span data-stu-id="a9573-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="a9573-112">この連結プロセスは *インポート連結* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a9573-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="a9573-113">また、法人は、連結法人と同じデータベースを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a9573-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="a9573-114">この連結プロセスは *オンライン連結* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a9573-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="a9573-115">連結法人は、関連会社の結果および残高を収集します。</span><span class="sxs-lookup"><span data-stu-id="a9573-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="a9573-116">連結する連結法人を準備するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a9573-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="a9573-117">**一般会計 \> 設定 \> 組織 \> 法人** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9573-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="a9573-118">**新規** を選択して、連結法人にする新しい法人を作成します。</span><span class="sxs-lookup"><span data-stu-id="a9573-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="a9573-119">**財務連結プロセスに使用** チェック ボックスをオンにし、連結された法人に関する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="a9573-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="a9573-120">連結法人の財務諸表に表示されるものと同じ情報を入力してください。</span><span class="sxs-lookup"><span data-stu-id="a9573-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="a9573-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9573-121">Close the page.</span></span>
5. <span data-ttu-id="a9573-122">ページの右上隅のフィールドで連結法人を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9573-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="a9573-123">**一般会計 \> 設定 \> 元帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9573-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="a9573-124">連結法人の勘定科目表、会計カレンダー、会計通貨、オプションのレポート通貨、既定の為替レート タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="a9573-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="a9573-125">これを行うには、**一般会計 \> 設定 \> 通貨 \> 通貨の為替レート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9573-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="a9573-126">子会社法人の通貨について、関連する期間の為替レートを設定します。</span><span class="sxs-lookup"><span data-stu-id="a9573-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="a9573-127">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9573-127">Close the page.</span></span>
11. <span data-ttu-id="a9573-128">連結法人に外貨を使用する子会社がある場合は、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a9573-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="a9573-129">**一般会計\> 設定 \> 転記 \> 自動トランザクションの勘定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9573-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="a9573-130">**転記タイプ** フィールドで適切な勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9573-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="a9573-131">法人に親法人と財務的または運用上の相互に相互に依存する外国の関連会社が存在する場合は、**連結差額の転記タイプの損益勘定** に対して適切な勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9573-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="a9573-132">財政的または経営的に親法人に依存していない関連会社、または財政的または経営的に親法人に依存していない複数の関連会社の結果が含まれている法人を連結する場合、および換算方法を使用してデータを連結する場合は、**連結貸借対照表計上額** の転記タイプに対して適切な勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9573-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="a9573-133">**主勘定** フィールドで、外貨再評価調整に使用する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="a9573-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="a9573-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a9573-134">Close the page.</span></span>

    <span data-ttu-id="a9573-135">連結法人を早い段階で作成した場合、連結期間中の為替レートの変動に応じて、外貨建の金額を切り上げることができます。</span><span class="sxs-lookup"><span data-stu-id="a9573-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="a9573-136">**連結** 定期ジョブに連結法人が設定されました。</span><span class="sxs-lookup"><span data-stu-id="a9573-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="a9573-137">連結のインポートまたはオンライン連結を行います。</span><span class="sxs-lookup"><span data-stu-id="a9573-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="a9573-138">インポート連結を実行するには、**一般会計 \> 定期 \> 連結 \> 連結 \[からインポート\]** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9573-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="a9573-139">オンライン連結を実行するには、**一般会計 \> 定期 \> 連結 \> 連結 \[ オンライン \]** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a9573-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="a9573-140">連結を処理する前に、連結をする関連法人を準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9573-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="a9573-141">詳細については、[連結法人を設定する](set-up-subsidiary-company-for-consolidation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9573-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>

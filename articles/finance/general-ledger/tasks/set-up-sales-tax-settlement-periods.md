---
title: 売上税精算期間の設定
description: このトピックでは、Dynamics 365 Finance で売上税決済期間を設定する方法について説明します。
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e2e5340150623057e233ed0acf487c42c61deba2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222122"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="29ccd-103">売上税精算期間の設定</span><span class="sxs-lookup"><span data-stu-id="29ccd-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29ccd-104">このトピックでは、売上税決済期間を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="29ccd-105">売上税決済期間は、売上税の報告および支払が必要な間隔についての情報を含みます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="29ccd-106">決済プロセスは、特定の日付範囲の決済期間に実行できます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="29ccd-107">決済期間に関連付けられたすべての税コードが決済されます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="29ccd-108">関連する売上税所轄官庁の設定に応じて、未払税金は仕入先または総勘定元帳勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="29ccd-109">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="29ccd-110">ナビゲーション ウィンドウで、**モジュール > 税 > 間接税 > 売上税 > 売上税決済期間** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="29ccd-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-111">Select **New**.</span></span>
3. <span data-ttu-id="29ccd-112">**決済期間** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="29ccd-113">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="29ccd-114">**所轄官庁** フィールドで、決済期間について作成されたレポートおよび支払を受け取る売上税所轄官庁を選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="29ccd-115">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="29ccd-116">**支払条件** フィールドで、ドロップダウン メニューから目的のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="29ccd-117">関連する売上税所轄官庁を仕入先として設定すると、売上税の決済により、未処理の仕入先請求書が作成されます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="29ccd-118">支払条件では、未処理の仕入先請求書の期日を定義します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="29ccd-119">決済期間間隔のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="29ccd-120">期間毎の間隔の単位の単位数を入力します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="29ccd-121">たとえば、四半期は 3 か月あります。</span><span class="sxs-lookup"><span data-stu-id="29ccd-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="29ccd-122">**売上税決済にバッチ処理を使用する** のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="29ccd-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="29ccd-123">決済期間の決済プロセスは、バックグラウンドのバッチ ジョブとして処理することができます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="29ccd-124">これは、期間内に大量の税トランザクションを処理する必要があるときにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="29ccd-124">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="29ccd-125">現在、スペイン、日本、およびオランダではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="29ccd-125">Currently this is not supported in Spain, Japan, and the Netherlands.</span></span>
11. <span data-ttu-id="29ccd-126">**相殺税トランザクションの生成を防止** のチェック ボックスを選択またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="29ccd-126">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="29ccd-127">既定では、システムは決済プロセス中に相殺税トランザクションを生成しますが、期間内に大量の税トランザクションを処理する必要がある場合、パフォーマンスの問題を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="29ccd-127">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="29ccd-128">相殺税トランザクションの生成を防止するために、このチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-128">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="29ccd-129">**間隔** タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-129">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="29ccd-130">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-130">Select **Add**.</span></span>
14. <span data-ttu-id="29ccd-131">新しい行の **開始日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-131">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="29ccd-132">**終了日** フィールドに、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-132">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="29ccd-133">**新しい間隔** を選択します。</span><span class="sxs-lookup"><span data-stu-id="29ccd-133">Select **New period interval**.</span></span> <span data-ttu-id="29ccd-134">最初の間隔を入力すると、新しい期間は自動的に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-134">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="29ccd-135">必要に応じて、新しい間隔を後で追加することができます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-135">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="29ccd-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="29ccd-136">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
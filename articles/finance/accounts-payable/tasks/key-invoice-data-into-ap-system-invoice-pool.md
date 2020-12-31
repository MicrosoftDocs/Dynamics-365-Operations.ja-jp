---
title: 請求管理グループを使用した AP システムへの請求書データの入力
description: このトピックでは、仕入帳を使用して請求書を作成する方法について説明します。
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd6de42dda650d42d703e905f8d48f73b9e4afd6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445134"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="719e0-103">請求管理グループを使用した AP システムへの請求書データの入力</span><span class="sxs-lookup"><span data-stu-id="719e0-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="719e0-104">このトピックでは、仕入帳を使用して請求書を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="719e0-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="719e0-105">その後、請求書を発注書と一致させるために、また仕入先請求書のページにある経費を確定するために、請求書管理グループを使用します。</span><span class="sxs-lookup"><span data-stu-id="719e0-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="719e0-106">発注書の作成</span><span class="sxs-lookup"><span data-stu-id="719e0-106">Create a purchase order</span></span>
1. <span data-ttu-id="719e0-107">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > 発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="719e0-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="719e0-108">**新規** を選択して新しい発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="719e0-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="719e0-109">**仕入先** フィールドで、ドロップダウン リストの仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="719e0-110">たとえば、仕入先 **1001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="719e0-111">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-111">Select **OK**.</span></span>
5. <span data-ttu-id="719e0-112">**品目番号** フィールドで、ドロップダウン リストのサービス品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="719e0-113">たとえば、**S0001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-113">For example, select **S0001**.</span></span> <span data-ttu-id="719e0-114">正味金額は 75.00 です。</span><span class="sxs-lookup"><span data-stu-id="719e0-114">The net amount is 75.00.</span></span>  <span data-ttu-id="719e0-115">これは、請求書上に表示される金額です。</span><span class="sxs-lookup"><span data-stu-id="719e0-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="719e0-116">アクション ウィンドウで、**購買** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="719e0-117">**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="719e0-118">請求書の作成と転記</span><span class="sxs-lookup"><span data-stu-id="719e0-118">Create and post and invoice</span></span>
1. <span data-ttu-id="719e0-119">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 仕入帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="719e0-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="719e0-120">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-120">Select **New**.</span></span>
3. <span data-ttu-id="719e0-121">ルックアップを開いて、使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="719e0-122">使用する仕入帳の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="719e0-123">登録を開いて経費明細行を入力するには、**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="719e0-124">ルックアップで、仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="719e0-125">たとえば、仕入先 **1001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="719e0-126">**請求書** フィールドに、請求書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="719e0-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="719e0-127">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="719e0-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="719e0-128">**貸方** フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="719e0-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="719e0-129">**発注書** フィールドで、ドロップダウン リストを開いて、先ほど作成した発注書を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="719e0-130">**承認者** フィールドのドロップダウン リストで承認者を強調表示し、**選択** をクリックしてその承認者を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="719e0-131">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="719e0-132">プールから請求書を開き、発注書と照合させ、請求書プロセスを完了させます。</span><span class="sxs-lookup"><span data-stu-id="719e0-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="719e0-133">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 請求書 > 請求管理グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="719e0-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="719e0-134">**発注書** を選択して、管理グループの請求書から仕入先請求書を作成します。</span><span class="sxs-lookup"><span data-stu-id="719e0-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="719e0-135">確認する請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="719e0-136">**照合状態の更新** を選択して、照合を完了します。</span><span class="sxs-lookup"><span data-stu-id="719e0-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="719e0-137">アクション ウィンドウで、**オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="719e0-138">**ビューの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-138">Select **Change view**.</span></span>
7. <span data-ttu-id="719e0-139">**グリッド ビュー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="719e0-140">**投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-140">Select **Post**.</span></span>
9. <span data-ttu-id="719e0-141">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="719e0-141">Close the form.</span></span>
10. <span data-ttu-id="719e0-142">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 仕入先 > 仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="719e0-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="719e0-143">発注書に記載されていた仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="719e0-144">たとえば、仕入先 **1001** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="719e0-145">アクション ウィンドウで、**仕入先** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="719e0-146">**トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="719e0-147">作成した請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="719e0-147">Select the invoice that you created.</span></span> <span data-ttu-id="719e0-148">仕入帳昇給額は取り消されて、適切な経費勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="719e0-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  


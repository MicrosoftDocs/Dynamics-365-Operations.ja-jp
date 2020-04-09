---
title: 顧客支払の預金
description: 顧客支払を預金します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140187"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="20a68-103">顧客支払の預金</span><span class="sxs-lookup"><span data-stu-id="20a68-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="20a68-104">顧客支払を預金します。</span><span class="sxs-lookup"><span data-stu-id="20a68-104">Deposit customer payments.</span></span> <span data-ttu-id="20a68-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="20a68-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="20a68-106">**ナビゲーション ウィンドウ > モジュール > 売掛金勘定 > 支払 > 支払仕訳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="20a68-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="20a68-107">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-107">Select **New**.</span></span>
3. <span data-ttu-id="20a68-108">**名前**フィールドで、ドロップダウン メニューの **CustPay** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="20a68-109">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-109">Select **Lines**.</span></span>
5. <span data-ttu-id="20a68-110">**口座**フィールドで、支払を記録している顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="20a68-111">**貸方**フィールドに支払金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="20a68-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="20a68-112">金額を空白にし、支払済み請求書を選択してシステムに計算させることができます。</span><span class="sxs-lookup"><span data-stu-id="20a68-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="20a68-113">**支払参照**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="20a68-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="20a68-114">支払の参照は、入力する支払の小切手番号にすることができます。</span><span class="sxs-lookup"><span data-stu-id="20a68-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="20a68-115">預金伝票に支払を含めるためには、支払参照が必要となります。</span><span class="sxs-lookup"><span data-stu-id="20a68-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="20a68-116">[預金伝票の使用] ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="20a68-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="20a68-117">支払額を預金残高に含める場合、この設定を「はい」に変更します。</span><span class="sxs-lookup"><span data-stu-id="20a68-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="20a68-118">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-118">Select **New**.</span></span>
10. <span data-ttu-id="20a68-119">**口座**フィールドで、次回に支払う顧客を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="20a68-120">**貸方**フィールドに支払金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="20a68-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="20a68-121">**支払参照**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="20a68-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="20a68-122">**預金伝票の使用**ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="20a68-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="20a68-123">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-123">Select **Post**.</span></span> <span data-ttu-id="20a68-124">預金伝票を生成する前に、支払は転記されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="20a68-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="20a68-125">これは、預金伝票が生成された後に支払が変更しないようにするためです。</span><span class="sxs-lookup"><span data-stu-id="20a68-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="20a68-126">**機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-126">Select **Functions**.</span></span>
16. <span data-ttu-id="20a68-127">**預金伝票**を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="20a68-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-128">Select **OK**.</span></span> <span data-ttu-id="20a68-129">最初のページは預金伝票を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="20a68-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="20a68-130">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20a68-130">Select **OK**.</span></span> <span data-ttu-id="20a68-131">2 番目の手順は、預金伝票を印刷することですが、この手順は必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="20a68-131">The second step is to print the deposit slip, but this step is not required.</span></span>  


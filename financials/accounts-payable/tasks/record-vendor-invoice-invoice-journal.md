--- 
title: "請求仕訳帳の仕入先請求書の記録"
description: "このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。"
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="d7b40-103">請求仕訳帳の仕入先請求書の記録</span><span class="sxs-lookup"><span data-stu-id="d7b40-103">Record a vendor invoice in the invoice journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d7b40-104">このタスク ガイドでは、発注書に関連付けられていない仕入先請求書を記録する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="d7b40-105">このタイプの請求書の例には、消耗品やサービスの経費があります。</span><span class="sxs-lookup"><span data-stu-id="d7b40-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="d7b40-106">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="d7b40-107">[買掛金勘定] > [ワークスペース] > [仕入先請求書入力] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="d7b40-108">[新しい請求仕訳帳] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7b40-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="d7b40-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7b40-109">Click New.</span></span>
4. <span data-ttu-id="d7b40-110">[名前] フィールドで、仕訳帳名を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="d7b40-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="d7b40-112">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7b40-112">Click Lines.</span></span>
    * <span data-ttu-id="d7b40-113">[日付] フィールドで、総勘定元帳を更新する転記日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="d7b40-114">[勘定] フィールドで、仕入先を指定します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="d7b40-115">[請求書] フィールドに請求書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="d7b40-116">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="d7b40-117">[貸方] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d7b40-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="d7b40-118">[相手勘定] フィールドで、勘定番号を入力するか、ドロップ ダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="d7b40-119">売上税グループは、仕入先から既定値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="d7b40-120">[品目売上税グループ] は、[相手勘定] フィールドで指定された主勘定から既定値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="d7b40-121">[期日] は、支払条件に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="d7b40-122">[現金割引] は、仕入先から既定値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="d7b40-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d7b40-123">Click Post.</span></span>
13. <span data-ttu-id="d7b40-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d7b40-124">Close the page.</span></span>



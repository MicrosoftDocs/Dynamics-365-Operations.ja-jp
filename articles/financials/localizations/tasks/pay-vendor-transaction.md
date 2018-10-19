--- 
title: "顧客の受取手形の裏書による仕入先トランザクションの支払"
description: "このタスクは、顧客為替手形の裏書きによる仕入先トランザクションの支払について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor, DimensionLookup, LedgerTransVoucher
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: a166d6c8e6153fc086a23c03a1ffa6ca07e909ad
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="pay-a-vendor-transaction-by-endorsing-a-customer-bill-of-exchange"></a><span data-ttu-id="811f5-103">顧客の受取手形の裏書による仕入先トランザクションの支払</span><span class="sxs-lookup"><span data-stu-id="811f5-103">Pay a vendor transaction by endorsing a customer bill of exchange</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="811f5-104">このタスクは、顧客為替手形の裏書きによる仕入先トランザクションの支払について説明します。</span><span class="sxs-lookup"><span data-stu-id="811f5-104">This task walks you through paying a vendor transaction by endorsing a customer bill of exchange.</span></span>



<span data-ttu-id="811f5-105">このタスクを完了するには、少なくとも 1 つの [振出済] の状態の為替手形が必要です。</span><span class="sxs-lookup"><span data-stu-id="811f5-105">Before you can complete this task, you must have at least one bill of exchange with a status of "Drawn".</span></span>



<span data-ttu-id="811f5-106">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="811f5-106">This task was created using the demo data company JPMF.</span></span>


## <a name="endorse-a-customer-bill-of-exchange-to-a-vendor"></a><span data-ttu-id="811f5-107">仕入先に対する顧客の為替手形の裏書</span><span class="sxs-lookup"><span data-stu-id="811f5-107">Endorse a customer bill of exchange to a vendor</span></span>
1. <span data-ttu-id="811f5-108">[売掛金勘定] > [支払] > [為替手形] > [裏書為替手形] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="811f5-108">Go to Accounts receivable > Payments > Bill of exchange > Endorse bills of exchange.</span></span>
2. <span data-ttu-id="811f5-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="811f5-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="811f5-110">ステータスが「振出済」の為替手形を選択します。</span><span class="sxs-lookup"><span data-stu-id="811f5-110">Select a bill of exchange that has a status of "Drawn".</span></span>  
3. <span data-ttu-id="811f5-111">[仕入先に対する裏書] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="811f5-111">Click Endorse to vendor to open the drop dialog.</span></span>
4. <span data-ttu-id="811f5-112">[裏書日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="811f5-112">In the Date of endorsement field, enter a date.</span></span>
    * <span data-ttu-id="811f5-113">日付は、為替手形の期日より後にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="811f5-113">The date cannot be later than the due date of the bill of exchange.</span></span>  
5. <span data-ttu-id="811f5-114">[仕入先] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="811f5-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="811f5-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="811f5-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="811f5-116">例: 「JPMF-000001」というレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="811f5-116">For example: select the record 'JPMF-000001'.</span></span>  
7. <span data-ttu-id="811f5-117">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="811f5-117">In the Description field, type a value.</span></span>
8. <span data-ttu-id="811f5-118">[BusinessUnit] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="811f5-118">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="811f5-119">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="811f5-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="811f5-120">例: 「003」というレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="811f5-120">For example: select the record '003'.</span></span>  
10. <span data-ttu-id="811f5-121">[仕入先に対する裏書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="811f5-121">Click Endorse to vendor.</span></span>
11. <span data-ttu-id="811f5-122">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="811f5-122">Click Inquiry.</span></span>
12. <span data-ttu-id="811f5-123">[伝票] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="811f5-123">Click Voucher.</span></span>
    * <span data-ttu-id="811f5-124">会計伝票が裏書用に生成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="811f5-124">Verify that an accounting voucher is generated for the endorsement.</span></span>  



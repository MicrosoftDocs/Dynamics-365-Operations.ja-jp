---
title: 信用保証状の銀行融資契約の作成
description: このタスクは、信用保証状を処理する銀行融資契約を作成します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2fe6bfebcc0cc302d623a34fd994a57cbea1c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178678"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="9fada-103">信用保証状の銀行融資契約の作成</span><span class="sxs-lookup"><span data-stu-id="9fada-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9fada-104">このタスクは、信用保証状を処理する銀行融資契約を作成します。</span><span class="sxs-lookup"><span data-stu-id="9fada-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="9fada-105">このタスクでは、USMF というデモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="9fada-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="9fada-106">銀行融資契約の作成</span><span class="sxs-lookup"><span data-stu-id="9fada-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="9fada-107">[現金および銀行管理] > [信用保証状] > [銀行融資契約] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="9fada-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-108">Click New.</span></span>
3. <span data-ttu-id="9fada-109">[契約番号] フィールドで、トランザクションの銀行の契約番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="9fada-110">[銀行口座] フィールドで、信用保証状が開いている銀行口座番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="9fada-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="9fada-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9fada-112">[開始日] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="9fada-113">[終了日] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="9fada-114">[一般] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="9fada-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="9fada-115">[行の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-115">Click Add line.</span></span>
10. <span data-ttu-id="9fada-116">[融資タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="9fada-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="9fada-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9fada-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9fada-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="9fada-119">[限度] フィールドに、銀行との交渉に基づく金額を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="9fada-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-120">Click Save.</span></span>
15. <span data-ttu-id="9fada-121">[信用保証状] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="9fada-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="9fada-122">[計算方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9fada-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="9fada-123">必要に応じて、現金保証、払出コミッション、拡張コミッション、値コミッションの増加、または値コミッションの減少の計算方法および割合の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="9fada-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="9fada-125">銀行融資契約の拡張</span><span class="sxs-lookup"><span data-stu-id="9fada-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="9fada-126">[拡張] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9fada-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="9fada-127">[新しい契約番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="9fada-128">[終了日] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9fada-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="9fada-129">[拡張] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-129">Click Extend.</span></span>
5. <span data-ttu-id="9fada-130">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9fada-130">Click Save.</span></span>
6. <span data-ttu-id="9fada-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9fada-131">Close the page.</span></span>


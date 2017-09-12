--- 
title: "顧客月次締め請求書の作成および確認 (日本)"
description: "日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9d7266d60e27f6c56caa59ec979de2fefab550db
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-confirm-a-customer-consolidated-invoice-japan"></a><span data-ttu-id="1364b-103">顧客月次締め請求書の作成および確認 (日本)</span><span class="sxs-lookup"><span data-stu-id="1364b-103">Create and confirm a customer consolidated invoice (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1364b-104">日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。</span><span class="sxs-lookup"><span data-stu-id="1364b-104">In Japan, sales and purchase invoices during the month are consolidated at the end of the month to calculate the due amount.</span></span> 



<span data-ttu-id="1364b-105">このタスクでは、月締め請求書の作成と確定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1364b-105">Use this task to learn how to create and confirm a consolidated invoice.</span></span> 



<span data-ttu-id="1364b-106">このタスクを完了するためには、販売請求書または仕入請求書が事前に転記されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="1364b-106">In order to complete this task, the sales or purchase invoices should have been posted before running this task.</span></span>



<span data-ttu-id="1364b-107">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="1364b-107">This task uses the JPMF demo company data.</span></span>

1. <span data-ttu-id="1364b-108">[売掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1364b-108">Go to Accounts receivable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="1364b-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1364b-109">Click New.</span></span>
    * <span data-ttu-id="1364b-110">既定の [実行日] はセッション日付です。</span><span class="sxs-lookup"><span data-stu-id="1364b-110">The default Execution date is the session date.</span></span>  
    * <span data-ttu-id="1364b-111">月次締め日を上書きする場合は、[以下で指定する月次締め日の使用] スライダーを「はい」に指定します。</span><span class="sxs-lookup"><span data-stu-id="1364b-111">Specify the Use consolidation date specified below slider to be 'Yes' if you want to override the consolidation date.</span></span>  
    * <span data-ttu-id="1364b-112">例: 月締め日が 25 日に指定されている場合、このスライダーが「はい」に設定されていれば、24 日に連結を実行できます。</span><span class="sxs-lookup"><span data-stu-id="1364b-112">Example: When the consolidation date is specified as the 25th, you can run the consolidation on the 24th if you set this slider to 'Yes'.</span></span> <span data-ttu-id="1364b-113">[月次締め日] は手動で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1364b-113">You will have to manually specify a Consolidation date.</span></span>  
3. <span data-ttu-id="1364b-114">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1364b-114">Click OK.</span></span>
    * <span data-ttu-id="1364b-115">[月次締め請求書] が生成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1364b-115">Verify that the Consolidated invoice was generated.</span></span>  
    * <span data-ttu-id="1364b-116">1 つの月次締め請求書に記載されるのは 1 つのの顧客 ID だけです。</span><span class="sxs-lookup"><span data-stu-id="1364b-116">One Consolidated invoice will contain only one Customer account.</span></span> <span data-ttu-id="1364b-117">連結する顧客 ID が複数ある場合は、複数の月次締め請求書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="1364b-117">When there are multiple Customer accounts to be consolidated, multiple consolidated invoices will be generated.</span></span>  
4. <span data-ttu-id="1364b-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="1364b-118">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1364b-119">グリッド内の [月次締め請求書] の [締め ID] をクリックして [月次締め請求書] ページの詳細表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="1364b-119">Switch to the detail view of the Consolidated invoice page  by clicking on the Consolidation ID of the Consolidated invoice in the grid.</span></span>  
    * <span data-ttu-id="1364b-120">請求済の販売注文が月次締め請求書に含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1364b-120">Verify that invoiced sales orders are included in the consolidated invoice.</span></span>  
5. <span data-ttu-id="1364b-121">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1364b-121">Click Confirm.</span></span>
    * <span data-ttu-id="1364b-122">[確定] をクリックすると、[月次締め請求書のステータス] は「確定済」に変わります。</span><span class="sxs-lookup"><span data-stu-id="1364b-122">The Status of the consolidated invoice changes to be 'Confirmed' after you click Confirm.</span></span> <span data-ttu-id="1364b-123">確定後、月次締め請求書はロックされ編集できません。</span><span class="sxs-lookup"><span data-stu-id="1364b-123">When confirmed, the consolidated invoice will be locked and you cannot edit it.</span></span>  



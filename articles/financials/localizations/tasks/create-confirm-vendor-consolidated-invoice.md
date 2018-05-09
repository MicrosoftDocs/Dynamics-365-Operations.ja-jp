--- 
title: "仕入先月次締め請求書の作成および確認 (日本)"
description: "日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 61eb55d3ce240234500ec5b70ca52fe3e2e8b7d5
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="create-and-confirm-a-vendor-consolidated-invoice-japan"></a><span data-ttu-id="595f6-103">仕入先月次締め請求書の作成および確認 (日本)</span><span class="sxs-lookup"><span data-stu-id="595f6-103">Create and confirm a vendor consolidated invoice (Japan)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="595f6-104">日本では、その月の販売請求書および仕入請求書は、未払金額を計算するため月末に連結されます。</span><span class="sxs-lookup"><span data-stu-id="595f6-104">In Japan, sales and purchase invoices during the month are consolidated at the end of the month to calculate the due amount.</span></span> 



<span data-ttu-id="595f6-105">このタスクでは、仕入先の月次締め請求書の作成と確定について説明します。</span><span class="sxs-lookup"><span data-stu-id="595f6-105">This task walks you through creating and confirming a vendor consolidated invoice.</span></span>



<span data-ttu-id="595f6-106">このタスクを完了するためには、仕入請求書の転記が完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="595f6-106">Before you can complete this task, you must have posted purchase invoices.</span></span> 



<span data-ttu-id="595f6-107">このタスクは デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="595f6-107">This task was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="595f6-108">[買掛金勘定] > [定期処理タスク] > [月次締め請求書] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="595f6-108">Go to Accounts payable > Periodic tasks > Consolidated invoice.</span></span>
2. <span data-ttu-id="595f6-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="595f6-109">Click New.</span></span>
3. <span data-ttu-id="595f6-110">[実行日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="595f6-110">In the Execution date field, enter a date.</span></span>
4. <span data-ttu-id="595f6-111">[以下で指定する月次締め日の使用] チェックボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="595f6-111">Select or clear the Use consolidation date specified below check box.</span></span>
    * <span data-ttu-id="595f6-112">月次締め日を上書きする場合は、[月次締め日の使用] のスライダーを「はい」に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="595f6-112">If you want to override the consolidation date, you must set the Use consolidation date slider to be 'Yes'.</span></span>  
5. <span data-ttu-id="595f6-113">[月次締め日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="595f6-113">In the Consolidation date field, enter a date.</span></span>
    * <span data-ttu-id="595f6-114">例: 月次締め日が 25 日の場合、このスライダーを「はい」に設定していれば、24 日に連結を実行できます。</span><span class="sxs-lookup"><span data-stu-id="595f6-114">Example: When the consolidation date is the 25th, you can run the consolidation on the 24th if you set this slider to 'Yes'.</span></span> <span data-ttu-id="595f6-115">[月次締め日] は手動で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="595f6-115">You will have to manually specify a Consolidation date.</span></span>  
6. <span data-ttu-id="595f6-116">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="595f6-116">Click OK.</span></span>
    * <span data-ttu-id="595f6-117">生成された月次締め請求書を確認します。</span><span class="sxs-lookup"><span data-stu-id="595f6-117">Verify the generated  consolidate invoice.</span></span>  
7. <span data-ttu-id="595f6-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="595f6-118">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="595f6-119">グリッド内の [月次締め請求書] の [締め ID] をクリックして [月次締め請求書] ページの詳細表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="595f6-119">Switch to the detail view of the Consolidated invoice page by clicking on the Consolidation ID of the Consolidated invoice in the grid.</span></span>  
    * <span data-ttu-id="595f6-120">請求済の発注書が月次締め請求書に含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="595f6-120">Verify that the invoiced purchase orders are included in the consolidated invoice.</span></span>  
8. <span data-ttu-id="595f6-121">[確認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="595f6-121">Click Confirm.</span></span>



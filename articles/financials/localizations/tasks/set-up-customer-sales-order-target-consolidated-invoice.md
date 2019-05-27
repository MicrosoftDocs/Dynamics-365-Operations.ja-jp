---
title: 月次締め請求書の対象とする顧客および販売注文の設定
description: 通常日本では、顧客はすべてのトランザクションに月次締め請求書を使用します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTableListPage, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c9b1994c0f91282f5a66da2c9e259de202b52153
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552358"
---
# <a name="set-up-a-customer-and-sales-order-to-be-target-of-consolidated-invoice"></a><span data-ttu-id="eacb5-103">月次締め請求書の対象とする顧客および販売注文の設定</span><span class="sxs-lookup"><span data-stu-id="eacb5-103">Set up a customer and sales order to be target of consolidated invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eacb5-104">通常日本では、顧客はすべてのトランザクションに月次締め請求書を使用します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-104">In Japan, the customers usually use consolidated invoice for all transactions.</span></span> 



<span data-ttu-id="eacb5-105">このタスクを使用して、月次締め請求書を使用するための顧客および販売注文の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-105">Use this task to learn how to set up a customer and a sales order to use consolidated invoices.</span></span> 



<span data-ttu-id="eacb5-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-106">This task uses the JPMF demo company data.</span></span>


## <a name="set-up-a-customer-to-be-a-target-of-consolidated-invoice"></a><span data-ttu-id="eacb5-107">月次締め請求書の対象とする顧客の設定</span><span class="sxs-lookup"><span data-stu-id="eacb5-107">Set up a customer to be a target of consolidated invoice</span></span>
1. <span data-ttu-id="eacb5-108">[売掛金勘定] > [顧客] > [すべての顧客] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-108">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="eacb5-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eacb5-109">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="eacb5-110">[支払の既定値] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-110">Expand the Payment defaults section.</span></span>
    * <span data-ttu-id="eacb5-111">[支払条件] で [締日方法] が使用されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-111">Verify that the Terms of payment uses the Cutoff day method.</span></span>  
    * <span data-ttu-id="eacb5-112">方法が「締日」ではない場合、タスク ガイドのロックを解除し、[編集] をクリックしてこのフィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-112">If the method is not "Cutoff day", unlock the task guide and then click Edit to update this field.</span></span>  
    * <span data-ttu-id="eacb5-113">顧客に対する月次締め日を指定します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-113">Specify a consolidation day for the customer.</span></span>  
    * <span data-ttu-id="eacb5-114">このフィールドの更新には、[編集] をクリックする必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="eacb5-114">You might need to click Edit before you can update this field.</span></span>  

## <a name="set-a-sales-order-to-be-target-of-consolidated-invoice"></a><span data-ttu-id="eacb5-115">月次締め請求書の対象とする販売注文の設定</span><span class="sxs-lookup"><span data-stu-id="eacb5-115">Set a sales order to be target of consolidated invoice</span></span>
1. <span data-ttu-id="eacb5-116">[売掛金勘定] > [注文] > [すべての販売注文] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-116">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="eacb5-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="eacb5-117">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="eacb5-118">[ヘッダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="eacb5-118">Click Header.</span></span>
    * <span data-ttu-id="eacb5-119">[締めの対象] スライダーが「はい」に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-119">Verify that the Target of consolidation slider is set to 'Yes'.</span></span>  
    * <span data-ttu-id="eacb5-120">スライダーが「いいえ」に設定されている場合、タスク ガイドのロックを解除し、[編集] をクリックしてこのフィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="eacb5-120">If the slider is set to "No", unlock the task guide and then click Edit to update the field.</span></span>  


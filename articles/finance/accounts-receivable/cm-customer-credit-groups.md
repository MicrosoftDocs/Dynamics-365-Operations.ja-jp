---
title: 顧客の与信グループ
description: このトピックでは、顧客の与信グループに関する情報を提供します。
author: mikefalkner
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3cdf4f7e72a55292c64b7a9191974242aab85a90
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835319"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="d6642-103">顧客の与信グループ</span><span class="sxs-lookup"><span data-stu-id="d6642-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6642-104">与信限度額を共有する顧客のグループを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d6642-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="d6642-105">顧客請求書勘定で定義された個々の与信限度額も考慮されます。</span><span class="sxs-lookup"><span data-stu-id="d6642-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="d6642-106">顧客の与信グループのメンバーは、異なる法人から選択できます。</span><span class="sxs-lookup"><span data-stu-id="d6642-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="d6642-107">顧客の与信グループに含まれる顧客リストに顧客を追加すると、各顧客の与信限度額の有効期限は、グループに割り当てられている有効期限に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d6642-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="d6642-108">顧客の与信グループは、**顧客の与信グループ** ページ (**与信管理\>顧客の与信グループ\>顧客の与信グループ**) で設定できます。</span><span class="sxs-lookup"><span data-stu-id="d6642-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="d6642-109">**グループ番号** フィールドと **説明** フィールドに、グループの ID と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d6642-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="d6642-110">**与信限度額** と **通貨** フィールドに、グループのメンバーの与信限度額がシステムによってチェックされるときに使用する与信限度額と通貨を入力します。</span><span class="sxs-lookup"><span data-stu-id="d6642-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="d6642-111">**与信限度額の有効期限** フィールドに、与信限度額の期限が切れる日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d6642-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="d6642-112">顧客の与信グループには有効期限が必要です。</span><span class="sxs-lookup"><span data-stu-id="d6642-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="d6642-113">顧客の与信グループの設定を完了した後、法人と顧客 ID を指定することにより、顧客を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="d6642-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="d6642-114">顧客の与信グループに新しい顧客を追加すると、すべての法人間で同じ顧客 ID が検索され、顧客の与信グループにその顧客を追加するように求められます。</span><span class="sxs-lookup"><span data-stu-id="d6642-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="d6642-115">**指定の期間に達している残高** メニューを使用して、顧客の与信グループに含まれるすべての請求書の顧客のエイジング残高の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="d6642-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="d6642-116">**エイジング残高** ページには、請求書の顧客 ID の指定の期間に達している残高の概要が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d6642-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
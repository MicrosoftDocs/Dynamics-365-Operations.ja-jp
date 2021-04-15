---
title: 作業者へ貸与された品目の管理
description: 貸与品目は、会社から作業者に貸与される現物品目を管理者が追跡するのに役立つレコードです。
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: dccab8cc2b166fe0ca22e05c14ae858f47aaf3e1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803444"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="0044b-103">作業者へ貸与された品目の管理</span><span class="sxs-lookup"><span data-stu-id="0044b-103">Manage items that are lent to workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="0044b-104">貸与品目は、会社から作業者に貸与される現物品目を管理者が追跡するのに役立つレコードです。</span><span class="sxs-lookup"><span data-stu-id="0044b-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="0044b-105">次の項目は、会社が作業者に割り当てられる貸与品目の例です。</span><span class="sxs-lookup"><span data-stu-id="0044b-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="0044b-106">携帯電話</span><span class="sxs-lookup"><span data-stu-id="0044b-106">Mobile telephones</span></span>
-   <span data-ttu-id="0044b-107">自動車</span><span class="sxs-lookup"><span data-stu-id="0044b-107">Automobiles</span></span>
-   <span data-ttu-id="0044b-108">コンピュータ機器</span><span class="sxs-lookup"><span data-stu-id="0044b-108">Computer equipment</span></span>

<span data-ttu-id="0044b-109">個々の現物品目は、対応する貸与品目が必要です。</span><span class="sxs-lookup"><span data-stu-id="0044b-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="0044b-110">各貸与品目の記録では、従業員への貸与する品目、貸与の責任者、および貸与可能な日数を記録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0044b-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="0044b-111">キー、アクセス カード、制服などの複数の貸与品目を同時に作成できます。</span><span class="sxs-lookup"><span data-stu-id="0044b-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="0044b-112">品目を貸与する際には、貸与日と予定返却日を入力します。</span><span class="sxs-lookup"><span data-stu-id="0044b-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="0044b-113">品目が返却されたら、実際の返却日を入力します。</span><span class="sxs-lookup"><span data-stu-id="0044b-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="0044b-114">従業員は、従業員セルフ サービス ワークスペースを使用して、貸与品目レコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0044b-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="0044b-115">また、追加の現物品目を受け取った場合は既存のレコードを編集、または新しい貸与品目を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="0044b-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="0044b-116">ワークフローを設定して、承認プロセスを通じた新規または既存の貸与品目に対する変更を転送することができます。</span><span class="sxs-lookup"><span data-stu-id="0044b-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="0044b-117">管理者は、直属の部下への貸与品目を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0044b-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="0044b-118">また、従業員に代わって新しい貸与品目を追加するアクセス許可を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="0044b-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="0044b-119">紛失した貸与品目の勘定</span><span class="sxs-lookup"><span data-stu-id="0044b-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="0044b-120">品目が損傷または紛失した場合は、架空の返却レコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="0044b-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="0044b-121">その後、品目を削除するか概要に記録し、品目が利用できないことを示すために説明を変更します。</span><span class="sxs-lookup"><span data-stu-id="0044b-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="0044b-122">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0044b-122">Additional resources</span></span>
--------

[<span data-ttu-id="0044b-123">人事管理</span><span class="sxs-lookup"><span data-stu-id="0044b-123">Human resources</span></span>](index.md)





[!INCLUDE[footer-include](../includes/footer-banner.md)]
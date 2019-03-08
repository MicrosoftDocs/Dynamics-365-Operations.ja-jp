---
title: 経費精算書と複数の承認者
description: このトピックでは、2 人以上の承認を必要とする経費精算書に関する情報を提供します。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1483de5405895d60f0cb302ab622758b2b05d2ca
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "362421"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="b4f7d-103">経費精算書と複数の承認者</span><span class="sxs-lookup"><span data-stu-id="b4f7d-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4f7d-104">組織の経費の承認ポリシーに応じて、従業員が提出した経費レポートの承認を複数の人が行う必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="b4f7d-105">経費レポートの承認のワークフロー プロセスを設定する場合、経費レポートの承認者のタスクまたはステップを一つ以上含むワークフロー要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="b4f7d-106">たとえば、すべての経費レポートは、まず最初に精算書を提出した従業員の管理者、そして買掛金勘定コーディネーターにより承認されることが要求される場合があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="b4f7d-107">複数の経費レポートの承認者を要求するようにした場合、次の方法のいずれかでワークフロー要素を追加できます:</span><span class="sxs-lookup"><span data-stu-id="b4f7d-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="b4f7d-108">1 つのステップを有する 1 件の承認の要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-108">Add one approval element that has one step.</span></span> <span data-ttu-id="b4f7d-109">たとえば、ステップでは経費精算書をユーザー グループに割り当て、ユーザー グループのメンバーの 50 パーセントで承認される必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="b4f7d-110">複数のステップを有する 1 件の承認の要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="b4f7d-111">たとえば、承認要素は次のステップを有する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="b4f7d-112">経費レポートを提出した従業員の管理者がそれを承認します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="b4f7d-113">買掛金勘定の事務員は、受領および経費レポートの項目を確認します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="b4f7d-114">予算の所有者が経費レポートを承認します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="b4f7d-115">複数の承認要素を追加します。それぞれの要素には 1 つのステップがあります。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="b4f7d-116">たとえば、次の手順の個別の承認要素を追加できます。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="b4f7d-117">従業員の管理者が経費レポートを承認します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="b4f7d-118">予算の所有者が経費レポートを承認します。</span><span class="sxs-lookup"><span data-stu-id="b4f7d-118">The budget owner approves the expense report.</span></span>

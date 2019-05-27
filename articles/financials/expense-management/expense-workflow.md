---
title: 経費ワークフロー
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations でワークフロー システムを使用する方法を説明し、経費管理で経費精算書の確認プロセスを設定します。
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 037a6ae00b7d559f79860901f0cb2ad6ddddd7aa
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545975"
---
# <a name="expense-workflow"></a><span data-ttu-id="e12dc-103">経費ワークフロー</span><span class="sxs-lookup"><span data-stu-id="e12dc-103">Expense workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e12dc-104">Microsoft Dynamics 365 for Finance and Operations のワークフロー システムでは、経費管理で経費精算書の確認プロセスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="e12dc-105">以下の条件を使用するワークフローを設定して、経費精算書を誰が承認するかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="e12dc-106">従業員の報告階層と定義済みの承認制限</span><span class="sxs-lookup"><span data-stu-id="e12dc-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="e12dc-107">中間承認者および最終承認者をサポートする複数レベルの承認</span><span class="sxs-lookup"><span data-stu-id="e12dc-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="e12dc-108">財務分析コードとプロジェクトの責任</span><span class="sxs-lookup"><span data-stu-id="e12dc-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="e12dc-109">特定のユーザーまたはユーザー グループに割り当て</span><span class="sxs-lookup"><span data-stu-id="e12dc-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="e12dc-110">ワークフローの承認は、経費精算書、出張命令書、現金前貸し要求、付加価値税 (VAT) の払い戻しに作成できます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="e12dc-111">**例**</span><span class="sxs-lookup"><span data-stu-id="e12dc-111">**Example**</span></span>

<span data-ttu-id="e12dc-112">経費精算書の経費管理ワークフローの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="e12dc-113">従業員が経費精算書を作成して、保存します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="e12dc-114">従業員は承認のために経費精算書を提出します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="e12dc-115">承認者はワークフローの設定時に定義したルールに基づいて識別します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="e12dc-116">承認者が、承認を受ける準備ができた経費精算書の通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="e12dc-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="e12dc-117">承認者は経費精算書をレビューし、次の条件が満たされていることを確認します:</span><span class="sxs-lookup"><span data-stu-id="e12dc-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="e12dc-118">経費に経費ポリシーの違反がない。</span><span class="sxs-lookup"><span data-stu-id="e12dc-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="e12dc-119">経費がポリシーに違反した場合、承認者は有効な業務上の理由が経費精算書に記載されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="e12dc-120">電子レシートが経費計算書に添付されている。</span><span class="sxs-lookup"><span data-stu-id="e12dc-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="e12dc-121">承認者は経費精算書を承認します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="e12dc-122">経費精算書が、転記のために買掛金勘定コーディネーターに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="e12dc-123">次の手順のいずれかが行われるかは、自動転記がコンフィギュレーションされているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="e12dc-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="e12dc-124">自動転記を構成すると、経費報告書は支払処理され、経費精算書の状態が更新されます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="e12dc-125">自動転記が構成されていない場合、買掛金勘定コーディネーターがすべての元のレシートが提出済みで、レシートが経費精算書の経費に対応していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e12dc-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="e12dc-126">経費精算書に入力されたすべての税コードが正しいかどうかも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e12dc-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="e12dc-127">これらの条件を確認したら、経費報告書は転記されます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="e12dc-128">経費精算書を転記すると、経費精算書の支払が承認され、従業員に払い戻しが行われます。</span><span class="sxs-lookup"><span data-stu-id="e12dc-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

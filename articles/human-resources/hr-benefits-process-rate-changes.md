---
title: レート変更の処理
description: 新規または既存の給付金プランが適格性ルール設定に変更がある場合、Microsoft Dynamics 365 Human Resources で給付金レートの変更処理を行います。
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: da42ef6ea91b95903316e35b551b222b8ff3b946
ms.sourcegitcommit: 9723b5ff40c84677316d71e185cf862556b32cf9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2020
ms.locfileid: "3741462"
---
# <a name="process-rate-changes"></a><span data-ttu-id="96d01-103">レート変更の処理</span><span class="sxs-lookup"><span data-stu-id="96d01-103">Process rate changes</span></span>

<span data-ttu-id="96d01-104">新規または既存の給付金プランが適格性ルール設定に変更がある場合、Microsoft Dynamics 365 Human Resources で給付金レートの変更処理を行います。</span><span class="sxs-lookup"><span data-stu-id="96d01-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="96d01-105">新しい適格性ルールが作成されてプランに割り当てられる場合、新しい適格性オプションに基づいて作業者はプランが適格な状態になっているかどうかをチェックするために、システムが作業者の適格性を再実行するように求められます。</span><span class="sxs-lookup"><span data-stu-id="96d01-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="96d01-106">**給付金管理**ワークスペースにて、**処理**の下の**レート変更の更新処理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="96d01-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="96d01-107">**給付金レートの更新処理を実行**ダイアログ ボックスで、次のフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="96d01-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="96d01-108">フィールド</span><span class="sxs-lookup"><span data-stu-id="96d01-108">Field</span></span> | <span data-ttu-id="96d01-109">説明</span><span class="sxs-lookup"><span data-stu-id="96d01-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="96d01-110">**登録期間**</span><span class="sxs-lookup"><span data-stu-id="96d01-110">**Enrollment period**</span></span> | <span data-ttu-id="96d01-111">レート変更を処理する登録期間。</span><span class="sxs-lookup"><span data-stu-id="96d01-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="96d01-112">バックグラウンドで処理を実行する場合は、**バックグラウンドで実行**を選択し、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="96d01-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="96d01-113">処理情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="96d01-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="96d01-114">定期的なジョブを設定するには、**再実行**を選び、繰り返しの情報を入植し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96d01-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="96d01-115">ジョブ警告を設定するには、**警告**を選び、入庫する警告を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96d01-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="96d01-116">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96d01-116">Select **OK**.</span></span> <span data-ttu-id="96d01-117">設定したパラメータで処理が実行されます。</span><span class="sxs-lookup"><span data-stu-id="96d01-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="96d01-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="96d01-118">Select **OK**.</span></span>

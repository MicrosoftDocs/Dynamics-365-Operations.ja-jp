---
title: 固定報酬プランへの従業員の登録
description: 報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a129bf9a6cb6a3ef92597e2ff9d126e3e5ce973b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468254"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a><span data-ttu-id="72d69-103">固定報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="72d69-103">Enroll an employee in a fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="72d69-104">報酬および福利厚生のマネージャーは、基準賃金を管理する固定報酬プランに従業員を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="72d69-104">The compensation and benefits manager can assign employees to fixed compensation plans to manage their base pay.</span></span> <span data-ttu-id="72d69-105">この手順は、固定プランが作成され、有効となり、適格性ルールが計画に対して設定されることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="72d69-105">This procedure assumes that a fixed plan has been created and is active, and that eligibility rules have been set for the plan.</span></span> <span data-ttu-id="72d69-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="72d69-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="72d69-107">手順を開始するには、[人事管理] > [作業者] > [従業員] > [報酬] > [固定プラン] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72d69-107">To begin the procedure, go to Human resources > Workers > Employees > Compensation > Fixed plan</span></span>

1. <span data-ttu-id="72d69-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72d69-108">Click New.</span></span>
2. <span data-ttu-id="72d69-109">[アクション] フィールドに、従業員の報酬の変更について説明する雇用/再雇用型の [固定報酬アクション] を選択します。</span><span class="sxs-lookup"><span data-stu-id="72d69-109">In the Action field, select a Fixed compensation action of type Hire/Rehire to describe the change in the employee's compensation.</span></span>
3. <span data-ttu-id="72d69-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="72d69-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="72d69-111">[配置] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="72d69-111">In the Position field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="72d69-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="72d69-112">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="72d69-113">表示されているレベルは、職位におけるジョブの報酬レベルです。</span><span class="sxs-lookup"><span data-stu-id="72d69-113">The level that's displayed is from the Compensation Level of the Job on the Position.</span></span> <span data-ttu-id="72d69-114">報酬は、従業員に割り当てる前に、ジョブに設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72d69-114">The level must be set on the Job before compensation can be assigned to the employee.</span></span>  
6. <span data-ttu-id="72d69-115">[プラン] フィールドで、従業員の固定報酬プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="72d69-115">In the Plan field, select the fixed compensation plan for the employee.</span></span> <span data-ttu-id="72d69-116">[計画] ルックアップでは、従業員は適格性ルールに基づいて適格となるプランのみが表示されるようにフィルタ処理されます。</span><span class="sxs-lookup"><span data-stu-id="72d69-116">The Plan lookup is filtered to show only the plans that the employee is eligible for based on the Eligibility rules.</span></span>
7. <span data-ttu-id="72d69-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="72d69-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="72d69-118">報酬の発効日と有効期限における既定値は、作業者職位の割り当て開始日および終了日から取得されます。</span><span class="sxs-lookup"><span data-stu-id="72d69-118">The Effective and Expiration dates for the compensation default from the start and end dates for the worker's position assignment.</span></span> <span data-ttu-id="72d69-119">必要に応じて、これらの日付を調整できます。</span><span class="sxs-lookup"><span data-stu-id="72d69-119">You can adjust these dates as needed.</span></span>  
    * <span data-ttu-id="72d69-120">固定報酬プランがステップ計画である場合、従業員に対する正しい支払いレートを含む手順を選択します。</span><span class="sxs-lookup"><span data-stu-id="72d69-120">If the Fixed compensation plan is a step plan, select the step containing the correct pay rate for the employee.</span></span> <span data-ttu-id="72d69-121">固定報酬プランが段階的またはバンド プランである場合、従業員に対する正しい支払いレートを入力します。</span><span class="sxs-lookup"><span data-stu-id="72d69-121">If the fixed compensation plan is a grade or a band plan, enter the pay rate for the employee.</span></span> <span data-ttu-id="72d69-122">支払レートは、計画の許容設定およびジョブの報酬レベルの最小または最大基準点に対して検証されます。</span><span class="sxs-lookup"><span data-stu-id="72d69-122">The pay rate will be validated against the tolerance settings for the plan, and the minimum and maximum reference points for the job's compensation level.</span></span>  
8. <span data-ttu-id="72d69-123">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72d69-123">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
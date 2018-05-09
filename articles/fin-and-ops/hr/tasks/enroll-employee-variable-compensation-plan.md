--- 
title: "変動報酬プランへの従業員の登録"
description: "報酬および福利厚生マネージャーは、従業員の現金および現金以外の報奨を計算する変動報酬プランに従業員を登録できます。"
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7e460794b460f2557af6607276b3cd0727e2de85
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a><span data-ttu-id="a42b3-103">変動報酬プランへの従業員の登録</span><span class="sxs-lookup"><span data-stu-id="a42b3-103">Enroll an employee in a variable compensation plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a42b3-104">報酬および福利厚生マネージャーは、従業員の現金および現金以外の報奨を計算する変動報酬プランに従業員を登録できます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-104">The Compensation and Benefits manager can enroll employees in variable compensation plans to calculate cash and non-cash awards for employees.</span></span> <span data-ttu-id="a42b3-105">この手順は、変動報酬プランが [登録の有効化] フィールドで [はい] を設定することによって作成され、適格性ルールが変動報酬プランに対して作成されていることを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="a42b3-105">This procedure assumes that a variable compensation plan has been created with the Enable enrolment field set to Yes, and that eligibility rules have been created for that variable compensation plan.</span></span> <span data-ttu-id="a42b3-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="a42b3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a42b3-107">この手順を開始するには、[人事管理] > [作業者] > [従業員] > [報酬] > [変動プラン登録] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a42b3-107">To begin this procedure, go to Human resources > Workers > Employees > Compensation > Variable plan enrolment</span></span>

1. <span data-ttu-id="a42b3-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a42b3-108">Click New.</span></span>
2. <span data-ttu-id="a42b3-109">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-109">In the Plan field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a42b3-110">[プラン] ルックアップでは、従業員は適格性ルールに基づいて適格となる変動報酬のみが表示されるようにフィルタ処理されるようになります。</span><span class="sxs-lookup"><span data-stu-id="a42b3-110">The plan lookup will be filtered to only show the variable compensation plans that the employee is eligible for based on the eligibility rules.</span></span>  
3. <span data-ttu-id="a42b3-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a42b3-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a42b3-112">[一般] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-112">Toggle the expansion of the General section.</span></span>
5. <span data-ttu-id="a42b3-113">[有効日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="a42b3-113">In the Effective date field, enter a date.</span></span>
6. <span data-ttu-id="a42b3-114">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a42b3-114">Click Save.</span></span>
7. <span data-ttu-id="a42b3-115">[上書き] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-115">Toggle the expansion of the Overrides section.</span></span>
    * <span data-ttu-id="a42b3-116">選択された変動プランが割合である場合、採用ルールの日付は、従業員の採用日付を上書きするように、必要に応じて設定できます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-116">Optionally, a hire rule date can be set to override the hire date for an employee when the hire rule specified for the selected variable plan is Percent.</span></span>  
    * <span data-ttu-id="a42b3-117">変動プランがある基となるプランのパーセンテージである場合、従業員の報奨率は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-117">If the variable plan is a percent of basis plan, the award percentage can be overridden for the employee.</span></span> <span data-ttu-id="a42b3-118">変動報酬計画が単位数計画である場合、従業員の単位数は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-118">If the variable compensation plan is a number of units plan, the number of units can be overridden for the employee.</span></span>  
    * <span data-ttu-id="a42b3-119">従業員に一律の報酬量を与えられれば、金額はここで設定できます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-119">If the employee should be given a flat amount for their award, the amount can be set here.</span></span>  
8. <span data-ttu-id="a42b3-120">[組織の上書き] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-120">Toggle the expansion of the Organizational overrides section.</span></span>
    * <span data-ttu-id="a42b3-121">従業員の業績を考慮に入力すると、さまざまな部門のパフォーマンス、または従業員の職位に割り当てられた部門以外の部門は、部門上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a42b3-121">If the employee's performance should take into consideration, the performance of different departments, or a department other than the one assigned on the employee's position, the department can be overridden.</span></span> <span data-ttu-id="a42b3-122">割合の列は合計を 100 とする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a42b3-122">The Percent column should total 100.</span></span>  



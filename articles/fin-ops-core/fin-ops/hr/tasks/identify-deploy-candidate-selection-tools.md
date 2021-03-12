---
title: 候補者採用手段の確認と配置
description: 空席を充填する見込みのある候補者のプールを探すことは難しい場合があり、特に複数の固有のスキルが職位に求められる場合に困難です。
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8015d4e32da2ba80230aa0ad48576948f2fd1678
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797753"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="d2b0e-103">候補者採用手段の確認と配置</span><span class="sxs-lookup"><span data-stu-id="d2b0e-103">Identify and deploy candidate selection tools</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2b0e-104">空席を充填する見込みのある候補者のプールを探すことは難しい場合があり、特に複数の固有のスキルが職位に求められる場合に困難です。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="d2b0e-105">しかし、必要なスキルを持つ候補者が、その組織にすでに雇用されている場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="d2b0e-106">既存の従業員または新しい応募者の中から、特定のスキル セットを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="d2b0e-107">これにより、リクルーターは、募集中の職位への最近または過去の応募者を素早く一覧し、絞り込むことができます。また、既存の従業員の中から潜在的な候補を探すことができます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="d2b0e-108">このタスク記録を使用すると、募集中の職位に対して適切な従業員を検索するために、スキル マッピングの機能がどのように役立つか確認できます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="d2b0e-109">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d2b0e-110">[人事管理] > [コンピテンシー] > [スキル分析] > [スキル マッピング プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="d2b0e-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-111">Click New.</span></span>
3. <span data-ttu-id="d2b0e-112">[スキル マッピング] フィールドで、スキル マッピングの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="d2b0e-113">例: 経理担当。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-113">Example: Accountant.</span></span>
4. <span data-ttu-id="d2b0e-114">[説明] フィールドに、スキル マッピングの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="d2b0e-115">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="d2b0e-116">[プロファイルの取得] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="d2b0e-117">プロファイルの取得を使用すると、選択された従業員、職務、またはコースを検索基準として、証明書、スキル、および教育データを取得できます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="d2b0e-118">その後、基準、および状態 (必須でない場合) を追加または削除でき、基準の重要性をランク付けできます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="d2b0e-119">[職務] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-119">Click Job.</span></span>
8. <span data-ttu-id="d2b0e-120">[職務] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="d2b0e-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-121">Click OK.</span></span>
10. <span data-ttu-id="d2b0e-122">[範囲] クイック タブを展開し、部署などの追加情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-122">Expand the Range FastTab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="d2b0e-123">[証明書] クイック タブを展開し、証明書を表示または編集します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-123">Expand the Certificates FastTab to view or edit the certificates.</span></span>
12. <span data-ttu-id="d2b0e-124">[スキル] クイック タブを展開し、スキルを表示または編集します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-124">Expand the Skills FastTab to view or edit the skills.</span></span>
13. <span data-ttu-id="d2b0e-125">[教育] クイック タブを展開し、教育基準を表示または編集します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-125">Expand the Education FastTab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="d2b0e-126">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-126">Click Execute.</span></span>
15. <span data-ttu-id="d2b0e-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-127">Click OK.</span></span>
16. <span data-ttu-id="d2b0e-128">[結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-128">Click Result.</span></span>
17. <span data-ttu-id="d2b0e-129">[結果] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-129">Click Result.</span></span>
18. <span data-ttu-id="d2b0e-130">[再開] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-130">Click Resume.</span></span>
19. <span data-ttu-id="d2b0e-131">[証明書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-131">Click Certificates.</span></span>
    * <span data-ttu-id="d2b0e-132">表示される各従業員についてさらに掘り下げることができ、教育、スキル、職務経験について詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-132">You can drill further into each person listed and see details regarding their education, skills, and professional experience.</span></span>  
20. <span data-ttu-id="d2b0e-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-133">Close the page.</span></span>
21. <span data-ttu-id="d2b0e-134">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-134">Close the page.</span></span>
22. <span data-ttu-id="d2b0e-135">結果をもう一度選択します。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-135">Select result again.</span></span>
23. <span data-ttu-id="d2b0e-136">[レポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-136">Click Report.</span></span>
    * <span data-ttu-id="d2b0e-137">レポートでは、最適なマッチがレポートの先頭に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="d2b0e-138">ギャップのある要素が一覧されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-138">You can see that a gap element is listed.</span></span>  <span data-ttu-id="d2b0e-139">これは、スキル マッピングに表示されるレベルと、従業員に割り当てられたスキル レベルとの差です。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="d2b0e-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-140">Close the page.</span></span>
25. <span data-ttu-id="d2b0e-141">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2b0e-141">Click Save.</span></span>


---
title: スキルのマッピング
description: スキル マッピング検索を作成して、スキル マッピングの資格を持つ人物を Dynamics 365 Human Resources で検索できます。
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 03b7860fbde89097141cfe48f2c240dc127aa9c3
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076601"
---
# <a name="map-skills"></a><span data-ttu-id="514de-103">スキルのマッピング</span><span class="sxs-lookup"><span data-stu-id="514de-103">Map skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="514de-104">スキル マッピング検索を作成して、スキル マッピングの資格を持つ人物を Dynamics 365 Human Resources で検索できます。</span><span class="sxs-lookup"><span data-stu-id="514de-104">You can create a skill-mapping search to find a qualified person in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="514de-105">スキル マッピングでは、次の情報を参照して、入力した基準に対する結果が返されます:</span><span class="sxs-lookup"><span data-stu-id="514de-105">Skill-mapping searches return results for criteria you enter by looking through the following information:</span></span>

- <span data-ttu-id="514de-106">スキル</span><span class="sxs-lookup"><span data-stu-id="514de-106">Skills</span></span>
- <span data-ttu-id="514de-107">教育</span><span class="sxs-lookup"><span data-stu-id="514de-107">Education</span></span>
- <span data-ttu-id="514de-108">証明書</span><span class="sxs-lookup"><span data-stu-id="514de-108">Certificates</span></span>
- <span data-ttu-id="514de-109">職位</span><span class="sxs-lookup"><span data-stu-id="514de-109">Positions</span></span>
- <span data-ttu-id="514de-110">プロジェクト経験</span><span class="sxs-lookup"><span data-stu-id="514de-110">Project experience</span></span>

<span data-ttu-id="514de-111">たとえば、CPA を取得した組織内の人を検索できます。</span><span class="sxs-lookup"><span data-stu-id="514de-111">For example, you can find people in your organization who have earned their CPA.</span></span>

<span data-ttu-id="514de-112">スキル マッピング プロファイルを使用すると、現在の従業員から、業務のニーズに直接対応する資格を持つ候補者を検索できます。</span><span class="sxs-lookup"><span data-stu-id="514de-112">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>

> [!NOTE]
> <span data-ttu-id="514de-113">スキル マッピング検索に含めるよう選択した作業者、申請者、担当者のみを、スキル マッピングの結果一覧に表示したり、スキル プロファイルに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="514de-113">Only workers, applicants, and contact persons who are selected to be included in skill-mapping searches will display in a skill-mapping results list, or be included in a skill profile.</span></span> <span data-ttu-id="514de-114">作業者、申請者、担当者をスキルのマッピング検索に含める場合は、次の各ページで、ス **キル マッピングの対象に含める** の選択を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="514de-114">To include a person in skill mapping searches, set the **Include in skill mapping** selection to **Yes** in the following pages:</span></span><br>
> - <span data-ttu-id="514de-115">ワーカー</span><span class="sxs-lookup"><span data-stu-id="514de-115">Worker</span></span><br>
> - <span data-ttu-id="514de-116">従業員</span><span class="sxs-lookup"><span data-stu-id="514de-116">Employee</span></span><br>
> - <span data-ttu-id="514de-117">申請者</span><span class="sxs-lookup"><span data-stu-id="514de-117">Applicant</span></span><br>
> - <span data-ttu-id="514de-118">連絡先</span><span class="sxs-lookup"><span data-stu-id="514de-118">Contacts</span></span><br>

<span data-ttu-id="514de-119">スキル マッピングを作成するには、**従業員の開発 >リンク > スキル マッピング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="514de-119">To create a skill mapping, go to **Employee development > Links > Skill mapping**.</span></span> <span data-ttu-id="514de-120">スキル マッピングのプロファイルを作成するには、**従業員の開発 >リンク > スキル マッピング プロファイル** に移動します。</span><span class="sxs-lookup"><span data-stu-id="514de-120">To create a skill-mapping profile, go to **Employee development > Links > Skill mapping profiles**.</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="514de-121">スキル ギャップ分析およびスキル プロファイル分析</span><span class="sxs-lookup"><span data-stu-id="514de-121">Skill gap analysis and skill profile analysis</span></span>

<span data-ttu-id="514de-122">スキル プロファイル分析を作成して、従業員の能力一覧を表示できます。</span><span class="sxs-lookup"><span data-stu-id="514de-122">You can create a skill profile analysis to view a list of a person's competencies.</span></span> <span data-ttu-id="514de-123">スキル ギャップ分析を作成して、その人のスキルと仕事に必要なスキルを比較することができます。</span><span class="sxs-lookup"><span data-stu-id="514de-123">You can create a skill gap analysis to compare a person’s skills and the skills required for a job.</span></span>

<span data-ttu-id="514de-124">ギャップ分析を作成するには、**従業員の開発 > リンク > スキルギャップ分析ジョブ > 従業員** にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="514de-124">To create a gap analysis, go to **Employee development > Links > Skill gap analysis job - person**.</span></span> <span data-ttu-id="514de-125">スキル マッピングのプロファイル分析を作成するには、**従業員の開発 >リンク > スキル マッピング プロファイル分析** に移動します。</span><span class="sxs-lookup"><span data-stu-id="514de-125">To create a skill profile analysis, go to **Employee development > Links > Skill profile analysis**.</span></span>

## <a name="see-also"></a><span data-ttu-id="514de-126">参照</span><span class="sxs-lookup"><span data-stu-id="514de-126">See also</span></span>

[<span data-ttu-id="514de-127">スキルの構成</span><span class="sxs-lookup"><span data-stu-id="514de-127">Configure skills</span></span>](hr-develop-skills.md)<br>
[<span data-ttu-id="514de-128">スキルの入力</span><span class="sxs-lookup"><span data-stu-id="514de-128">Enter skills</span></span>](hr-develop-enter-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
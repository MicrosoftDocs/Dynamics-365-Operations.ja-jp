---
title: "給付金の適格性ポリシー"
description: "この記事は、だれに特定の給付金の受給資格があるのかを定義するのに役立つ給付金の適格性ポリシーに関する情報が提供されます。"
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 46dba3a61cf96b19b5bc4d2956d028bbbeaaa60e
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="benefit-eligibility-policies"></a><span data-ttu-id="fbf6e-103">給付金の適格性ポリシー</span><span class="sxs-lookup"><span data-stu-id="fbf6e-103">Benefit eligibility policies</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="fbf6e-104">このトピックは、だれに特定の給付金の受給資格があるのかを定義するのに役立つ給付金の適格性ポリシーに関する情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="fbf6e-105">給付金を作成する場合、どの従業員がどの給付金を利用できるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="fbf6e-106">次の表では、特定の従業員が利用できる給付金の例を示します。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="fbf6e-107">給付金</span><span class="sxs-lookup"><span data-stu-id="fbf6e-107">Benefit</span></span>          | <span data-ttu-id="fbf6e-108">給付金を利用できる人</span><span class="sxs-lookup"><span data-stu-id="fbf6e-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="fbf6e-109">健康保険</span><span class="sxs-lookup"><span data-stu-id="fbf6e-109">Health insurance</span></span> | <span data-ttu-id="fbf6e-110">全従業員</span><span class="sxs-lookup"><span data-stu-id="fbf6e-110">All employees</span></span>                   |
| <span data-ttu-id="fbf6e-111">携帯電話</span><span class="sxs-lookup"><span data-stu-id="fbf6e-111">Mobile phone</span></span>     | <span data-ttu-id="fbf6e-112">販売スタッフ、経営幹部</span><span class="sxs-lookup"><span data-stu-id="fbf6e-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="fbf6e-113">駐車許可証</span><span class="sxs-lookup"><span data-stu-id="fbf6e-113">Parking passes</span></span>   | <span data-ttu-id="fbf6e-114">経営幹部</span><span class="sxs-lookup"><span data-stu-id="fbf6e-114">Executives</span></span>                      |

<span data-ttu-id="fbf6e-115">次のコンポーネントは、適格性ポリシーの作成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="fbf6e-116">ポリシー ルール タイプ</span><span class="sxs-lookup"><span data-stu-id="fbf6e-116">Policy rule types</span></span>
-   <span data-ttu-id="fbf6e-117">給付金の適格性ポリシー</span><span class="sxs-lookup"><span data-stu-id="fbf6e-117">Benefit eligibility policies</span></span>

<span data-ttu-id="fbf6e-118">ポリシー ルール タイプは、特定のポリシー ルールを作成する際に使用するクエリ パラメーターを定義します。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="fbf6e-119">ポリシー ルール タイプを作成した後、給付金の適格性ポリシーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="fbf6e-120">ポリシーでは、1 つ以上の法人に適用される一連のルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="fbf6e-121">各ポリシー内では、先に作成した給付金の適格性ポリシー ルール タイプを表示できます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="fbf6e-122">ポリシー内のルールの範囲を定義します。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="fbf6e-123">たとえば、「**経営幹部**」という名前の給付金の適格性ポリシー ルール タイプを作成する場合、そのポリシー内にどのようなルールがあるかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="fbf6e-124">この例は、そのルールでは、「経営幹部」という言葉を含んだ肩書きがルールに含まれていることを示しています。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-124">In this example, the rule might state that any job title that contains the word “executive” should be included in the rule.</span></span> <span data-ttu-id="fbf6e-125">ルールのパラメーターまたはポリシーに含まれるルールを定義した後、給付金に特定のルールを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="fbf6e-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="see-also"></a><span data-ttu-id="fbf6e-126">参照</span><span class="sxs-lookup"><span data-stu-id="fbf6e-126">See also</span></span>
--------

[<span data-ttu-id="fbf6e-127">給付金プログラムの定義および管理</span><span class="sxs-lookup"><span data-stu-id="fbf6e-127">Defining and managing a benefit program</span></span>](manage-benefit-program.md)





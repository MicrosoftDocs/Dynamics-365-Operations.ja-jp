---
title: Dynamics 365 Talent - Onboard を使用した研修テンプレートの作成
description: このトピックでは、Dynamics 365 Talent - Onboard アプリを使用して新規採用者向けの研修用ガイドのテンプレートを作成する方法について説明します。 このタスクは、人事管理 (HCM) の採用から退職までの戦略における重要な第一歩です。
author: andreabichsel
manager: ''
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a1fac239524d4873a782e6a3d177a573a382d0f6
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552044"
---
# <a name="create-an-onboarding-template-by-using-dynamics-365-talent---onboard"></a><span data-ttu-id="37ac4-104">Dynamics 365 Talent - Onboard を使用した研修テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="37ac4-104">Create an onboarding template by using Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="37ac4-105">Microsoft Dynamics 365 Talent: Onboard には、できるだけ早く研修用ガイドを作成するのに役立つさまざまなテンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="37ac4-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="37ac4-106">これらのテンプレートを 1 つ以上使用することも、独自のテンプレートを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="37ac4-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="37ac4-107">Onboard には、独自のテンプレートを作成するときに使用できるサンプル テキストが用意されています。</span><span class="sxs-lookup"><span data-stu-id="37ac4-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="37ac4-108">そのため、ゼロから始めてもプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="37ac4-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="37ac4-109">既存のテンプレートからの採用テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="37ac4-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="37ac4-110">左側のメニューで、**テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="37ac4-111">**ギャラリーで人気のテンプレート**または**自分のテンプレート**から、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="37ac4-112">他のテンプレートを表示するには、**テンプレート ギャラリーのその他のテンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="37ac4-113">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="37ac4-114">テンプレートがギャラリーからのものである場合、**自分のテンプレートとして保存**を選択し、テンプレートの新しい名前を入力し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="37ac4-115">テンプレートが**自分のテンプレート**からのものである場合、**テンプレートとして保存**を選択し、テンプレートの新しい名前を入力し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="37ac4-116">[![既存のテンプレートからのテンプレートの作成](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="37ac4-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="37ac4-117">新しい研修テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="37ac4-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="37ac4-118">左側のメニューで、**テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="37ac4-119">**自分のテンプレート**で、**追加** (プラス記号 \[**+**\]) タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="37ac4-120">[![新しいテンプレートの作成](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="37ac4-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="37ac4-121">**ガイド テンプレートの作成**ダイアログ ボックスで、テンプレートの名前を入力し、次に**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="37ac4-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="37ac4-122">次のステップ</span><span class="sxs-lookup"><span data-stu-id="37ac4-122">Next steps</span></span>

- [<span data-ttu-id="37ac4-123">研修用ガイドとテンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="37ac4-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="37ac4-124">他の投稿者とコンテンツを共有する</span><span class="sxs-lookup"><span data-stu-id="37ac4-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="37ac4-125">タスクと研修中の従業員の状態の表示</span><span class="sxs-lookup"><span data-stu-id="37ac4-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="37ac4-126">Onboard での採用チームの作成</span><span class="sxs-lookup"><span data-stu-id="37ac4-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="37ac4-127">参照</span><span class="sxs-lookup"><span data-stu-id="37ac4-127">See also</span></span>

- [<span data-ttu-id="37ac4-128">Onboard アプリを試すか購入する</span><span class="sxs-lookup"><span data-stu-id="37ac4-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="37ac4-129">新機能</span><span class="sxs-lookup"><span data-stu-id="37ac4-129">What's new</span></span>](./whats-new.md)
- [<span data-ttu-id="37ac4-130">リリース ノート</span><span class="sxs-lookup"><span data-stu-id="37ac4-130">Release notes</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="37ac4-131">サポートの利用</span><span class="sxs-lookup"><span data-stu-id="37ac4-131">Get support</span></span>](./talent-support.md)

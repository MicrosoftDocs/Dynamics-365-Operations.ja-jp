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
ms.openlocfilehash: 55853418eacd179b7bb50b7e4385300bdcb27abe
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812905"
---
# <a name="create-an-onboarding-template-by-using-dynamics-365-talent---onboard"></a><span data-ttu-id="1b475-104">Dynamics 365 Talent - Onboard を使用した研修テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="1b475-104">Create an onboarding template by using Dynamics 365 Talent - Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b475-105">Microsoft Dynamics 365 Talent: Onboard には、できるだけ早く研修用ガイドを作成するのに役立つさまざまなテンプレートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="1b475-105">Microsoft Dynamics 365 Talent: Onboard provides various templates that can help you create an onboarding guide as quickly as possible.</span></span> <span data-ttu-id="1b475-106">これらのテンプレートを 1 つ以上使用することも、独自のテンプレートを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="1b475-106">You can use one or more of these templates, or you can create your own templates.</span></span> <span data-ttu-id="1b475-107">Onboard には、独自のテンプレートを作成するときに使用できるサンプル テキストが用意されています。</span><span class="sxs-lookup"><span data-stu-id="1b475-107">Onboard provides sample text that you can use when you create your own templates.</span></span> <span data-ttu-id="1b475-108">そのため、ゼロから始めてもプロセスは簡単です。</span><span class="sxs-lookup"><span data-stu-id="1b475-108">Therefore, the process is easy even if you start from scratch.</span></span>

## <a name="create-an-onboarding-template-from-an-existing-template"></a><span data-ttu-id="1b475-109">既存のテンプレートからの採用テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="1b475-109">Create an onboarding template from an existing template</span></span>

1. <span data-ttu-id="1b475-110">左側のメニューで、**テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-110">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="1b475-111">**ギャラリーで人気のテンプレート**または**自分のテンプレート**から、テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-111">Under **Popular templates from the gallery** or **My templates**, select a template.</span></span> <span data-ttu-id="1b475-112">他のテンプレートを表示するには、**テンプレート ギャラリーのその他のテンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-112">To view more templates, select **More in template gallery**.</span></span>
3. <span data-ttu-id="1b475-113">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="1b475-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="1b475-114">テンプレートがギャラリーからのものである場合、**自分のテンプレートとして保存**を選択し、テンプレートの新しい名前を入力し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-114">If the template is from the gallery, select **Save as my template**, enter a new name for the template, and select **Save**.</span></span>
    - <span data-ttu-id="1b475-115">テンプレートが**自分のテンプレート**からのものである場合、**テンプレートとして保存**を選択し、テンプレートの新しい名前を入力し、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-115">If the template is from **My templates**, select **Save as template**, enter a new name for the template, and select **Save**.</span></span>

    <span data-ttu-id="1b475-116">[![既存のテンプレートからのテンプレートの作成](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span><span class="sxs-lookup"><span data-stu-id="1b475-116">[![Creating a template from an existing template](./media/onboard-save-template.png)](./media/onboard-save-template.png)</span></span>

## <a name="create-a-new-onboarding-template"></a><span data-ttu-id="1b475-117">新しい研修テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="1b475-117">Create a new onboarding template</span></span>

1. <span data-ttu-id="1b475-118">左側のメニューで、**テンプレート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-118">On the left menu, select **Templates**.</span></span>
2. <span data-ttu-id="1b475-119">**自分のテンプレート**で、**追加** (プラス記号 \[**+**\]) タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-119">Under **My templates**, select the **Add** (plus sign \[**+**\]) tile.</span></span>

    <span data-ttu-id="1b475-120">[![新しいテンプレートの作成](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span><span class="sxs-lookup"><span data-stu-id="1b475-120">[![Creating a new template](./media/onboard-create-new-template.png)](./media/onboard-create-new-template.png)</span></span>

3. <span data-ttu-id="1b475-121">**ガイド テンプレートの作成**ダイアログ ボックスで、テンプレートの名前を入力し、次に**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1b475-121">In the **Create a guide template** dialog box, enter a name for the template, and then select **Save**.</span></span>

## <a name="next-steps"></a><span data-ttu-id="1b475-122">次のステップ</span><span class="sxs-lookup"><span data-stu-id="1b475-122">Next steps</span></span>

- [<span data-ttu-id="1b475-123">研修用ガイドとテンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="1b475-123">Edit onboarding guides and templates</span></span>](./onboard-edit-guides-templates.md)
- [<span data-ttu-id="1b475-124">他の投稿者とコンテンツを共有する</span><span class="sxs-lookup"><span data-stu-id="1b475-124">Share content with other contributors</span></span>](./onboard-share-template.md)
- [<span data-ttu-id="1b475-125">タスクと研修中の従業員の状態の表示</span><span class="sxs-lookup"><span data-stu-id="1b475-125">View the status of tasks and onboarding employees</span></span>](./onboard-view-status.md)
- [<span data-ttu-id="1b475-126">Onboard での採用チームの作成</span><span class="sxs-lookup"><span data-stu-id="1b475-126">Create hiring teams in Onboard</span></span>](./onboard-create-team.md)

### <a name="see-also"></a><span data-ttu-id="1b475-127">参照</span><span class="sxs-lookup"><span data-stu-id="1b475-127">See also</span></span>

- [<span data-ttu-id="1b475-128">Onboard アプリを試すか購入する</span><span class="sxs-lookup"><span data-stu-id="1b475-128">Try or buy the Onboard app</span></span>](https://dynamics.microsoft.com/talent/onboard/)
- [<span data-ttu-id="1b475-129">Dynamics 365 Talent の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="1b475-129">What's new or changed in Dynamics 365 Talent</span></span>](./whats-new.md)
- [<span data-ttu-id="1b475-130">リリース計画</span><span class="sxs-lookup"><span data-stu-id="1b475-130">Release plans</span></span>](https://docs.microsoft.com/business-applications-release-notes/index)
- [<span data-ttu-id="1b475-131">Microsoft Dynamics 365 Talent に関するサポートの利用</span><span class="sxs-lookup"><span data-stu-id="1b475-131">Get support for Microsoft Dynamics 365 Talent</span></span>](./talent-support.md)

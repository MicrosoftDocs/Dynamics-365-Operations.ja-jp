---
title: "Attract でのプロセス テンプレートの作成"
description: "このトピックでは、Attract でプロセス テンプレートを作成する方法について説明します。"
author: hasrivas
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: hasrivas
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 54c80f3d785ba7a7e0158c51201468f45796c193
ms.contentlocale: ja-jp
ms.lasthandoff: 10/22/2018

---

# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="e923a-103">Attract でのプロセス テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="e923a-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e923a-104">*採用プロセス テンプレート*には、ジョブの採用プロセスの一部として含まれる必要のあるすべての活動が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e923a-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="e923a-105">このトピックでは、Microsoft Dynamics 365 for Talent: Attract でのプロセス テンプレートの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="e923a-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="e923a-106">テンプレートを作成する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="e923a-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="e923a-107">テンプレートの作成は、Attract の包括採用アドオンの一部です。</span><span class="sxs-lookup"><span data-stu-id="e923a-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="e923a-108">テンプレート管理</span><span class="sxs-lookup"><span data-stu-id="e923a-108">Template management</span></span>

<span data-ttu-id="e923a-109">組織は、チーム メンバーもしくは管理者のみが、Attract でプロセス テンプレートを作成できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e923a-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="e923a-110">テンプレートの管理をコンフィギュレーションするには、**管理者センター** \> **テンプレートの管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="e923a-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="e923a-111">チーム メンバーが独自のテンプレートを作成できるようにするには、テンプレートの管理を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e923a-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="e923a-112">テンプレートの管理を有効にしない場合は、テンプレートを作成できるのは管理者のみになります。</span><span class="sxs-lookup"><span data-stu-id="e923a-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="e923a-113">既定のテンプレート</span><span class="sxs-lookup"><span data-stu-id="e923a-113">Default template</span></span>

<span data-ttu-id="e923a-114">管理者のみ、既定のテンプレートを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e923a-114">Only admins can set the default template.</span></span> <span data-ttu-id="e923a-115">ジョブの作成時にテンプレートが選択されていない場合、既定のテンプレートが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e923a-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="e923a-116">既定のテンプレートを設定するには、**管理者センター** \> **テンプレートの管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="e923a-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="e923a-117">既定のテンプレートにするテンプレートのカードで、省略記号ボタン (**...**) を選択し、**既定として設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="e923a-118">プロセス テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="e923a-118">Create a process template</span></span>

<span data-ttu-id="e923a-119">管理者、採用担当者、および採用マネージャーがプロセス テンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e923a-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="e923a-120">プロセス テンプレートは、*ステージ*および*活動*で構成されます。</span><span class="sxs-lookup"><span data-stu-id="e923a-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="e923a-121">ステージは 1 つまたは複数の活動をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="e923a-121">Stages group together one or more activities.</span></span> <span data-ttu-id="e923a-122">既定では、各プロセス テンプレートには、見込顧客、アプリケーション、およびオファー活動があります。</span><span class="sxs-lookup"><span data-stu-id="e923a-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="e923a-123">これらの活動を含むステージの名前を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e923a-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="e923a-124">**+ 新規ステージ**を選択して、さらにステージを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e923a-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="e923a-125">適切なステージにドラッグするか、活動リストでダブルクリックすることによって、活動をステージにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e923a-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="e923a-126">**応募のステータス**のページで、ステージ名が候補者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="e923a-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="e923a-127">ステージ名を選択する際には、このことを考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e923a-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="e923a-128">活動に関する詳細については、[Attract での採用プロセス活動](./activities-attract.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e923a-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="e923a-129">採用プロセス テンプレートを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e923a-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="e923a-130">**テンプレート**に移動する。</span><span class="sxs-lookup"><span data-stu-id="e923a-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="e923a-131">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-131">Select **New**.</span></span>
3. <span data-ttu-id="e923a-132">**テンプレート名**のフィールドで、テンプレートの名前を入力し、次に**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="e923a-133">**採用プロセスを選択**のリストで、**既定**を選択し、ジョブの承認を要求します。</span><span class="sxs-lookup"><span data-stu-id="e923a-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="e923a-134">候補者を有効または無効にする場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="e923a-135">オプション: ステージを追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="e923a-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="e923a-136">ステージを追加するには、**+ 新規ステージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="e923a-137">ステージを削除するには、ポインターをステージに移動して、表示されるごみ箱ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e923a-138">候補者、申請、およびオファー ステージを削除することはできませんが、名前を変更することは可能です。</span><span class="sxs-lookup"><span data-stu-id="e923a-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="e923a-139">オプション: 活動を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="e923a-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="e923a-140">活動を追加するには、右の活動一覧から適切なステージにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="e923a-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="e923a-141">または、活動をダブルクリックし、それを追加するステージを選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="e923a-142">活動を削除するには、活動を展開し、活動ヘッダーのごみ箱ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="e923a-143">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e923a-143">Select **Save**.</span></span>


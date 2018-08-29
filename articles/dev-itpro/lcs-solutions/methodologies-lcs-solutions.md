---
title: "Finance and Operations のソリューションに方法を追加"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の方法を作成および変更する方法について説明します。 また、方法の要件に関する情報も提供されます。"
author: kfend
manager: AnnBe
ms.date: 04/13/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Lifecycle Services
ms.custom: 197063
ms.assetid: 368f2356-62a6-4d9f-9f80-0acf7a986085
ms.search.region: Global
ms.author: omarc
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 31485cd75abf65e717f75f4d6f3b1f622a2b11eb
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="add-methodologies-to-finance-and-operations-solutions"></a><span data-ttu-id="5f077-104">Finance and Operations のソリューションに方法を追加</span><span class="sxs-lookup"><span data-stu-id="5f077-104">Add methodologies to Finance and Operations solutions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5f077-105">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) の方法を作成および変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5f077-105">This topic explains how to create and modify methodologies in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5f077-106">また、方法の要件に関する情報も提供されます。</span><span class="sxs-lookup"><span data-stu-id="5f077-106">It also provides information about the requirements for methodologies.</span></span>

<a name="methodology-requirements"></a><span data-ttu-id="5f077-107">方法の要件</span><span class="sxs-lookup"><span data-stu-id="5f077-107">Methodology requirements</span></span>
------------------------

<span data-ttu-id="5f077-108">方法論の最初の 2 つのフェーズは、LCS ソリューションの消費方法論からの学習と消費のフェーズです。</span><span class="sxs-lookup"><span data-stu-id="5f077-108">The first two phases of your methodology are the Learn and Consume phases from the LCS Solutions Consumption methodology.</span></span> 

<span data-ttu-id="5f077-109">学習段階において、製品の説明は、業務プロセス ライブラリ、マーケティング材料の説明または概要、およびソリューションの現在のバージョンでサポートされている機能と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f077-109">During the Learn phase, your product description must be aligned with your business process library, the descriptions or summaries in your marketing material, and the functionality that is supported in the current version of your solution.</span></span> <span data-ttu-id="5f077-110">学習フェーズには次の作業が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f077-110">The Learn phase includes the following tasks:</span></span>

-   <span data-ttu-id="5f077-111">**製品の説明** – マーケティングの説明を LCS の方法に追加して活用してください。</span><span class="sxs-lookup"><span data-stu-id="5f077-111">**Product description** – Take advantage of your marketing description by adding it to the LCS methodology.</span></span>
-   <span data-ttu-id="5f077-112">**概要の取得** – 機能やアーキテクチャに関する情報など、ソリューションのコンテンツが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f077-112">**Get an overview** – Include content for your solution, such as information about the features and architecture.</span></span>
-   <span data-ttu-id="5f077-113">**ヘルプを入手する方法** – ソリューションの構築と保守に貢献した人のために、会社の Web サイトへの番号、連絡先、または直接リンクを含めます。</span><span class="sxs-lookup"><span data-stu-id="5f077-113">**How to get help** – Include numbers, contacts, or direct links to your company's website, for people who help build and maintain the solution.</span></span>

<span data-ttu-id="5f077-114">消費フェーズは**オプション**です。</span><span class="sxs-lookup"><span data-stu-id="5f077-114">The Consume phase is **optional**.</span></span> <span data-ttu-id="5f077-115">会議室パイロット 1 (CRP1) を完了するために必要なタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f077-115">It includes tasks that are required in order to complete Conference room pilot 1 (CRP1).</span></span> 


<span data-ttu-id="5f077-116">詳細情報と消費のフェーズの後に、ソリューションを実装するためにその他の必要な手順を追加できます。</span><span class="sxs-lookup"><span data-stu-id="5f077-116">After the Learn and Consume phases, you can add any other steps that are required in order to implement your solution.</span></span> <span data-ttu-id="5f077-117">ソリューションに合うようにフェーズとタスクを変更するか、会社の実装方法を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5f077-117">You can either modify the phases and tasks so that they are aligned with your solution, or use your company's implementation methodology.</span></span>

## <a name="create-a-new-methodology"></a><span data-ttu-id="5f077-118">新しい方法の作成</span><span class="sxs-lookup"><span data-stu-id="5f077-118">Create a new methodology</span></span>
1.  <span data-ttu-id="5f077-119">LCS ホーム ページで、**方法の管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-119">On the LCS home page, select the **Manage methodologies** tile.</span></span>
2.  <span data-ttu-id="5f077-120">**新しい方法**ボタン (プラス記号 **+**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-120">Select the **New methodology** button (the plus sign [**+**]).</span></span>
3.  <span data-ttu-id="5f077-121">フィールドの値を設定し、**確定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-121">Set values for the fields, and then select **Confirm**.</span></span>
4.  <span data-ttu-id="5f077-122">フェーズおよびタスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="5f077-122">Create phases and tasks.</span></span>
5.  <span data-ttu-id="5f077-123">必要なリンクされているツールとリソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="5f077-123">Add any linked tools and resources that are required.</span></span>

## <a name="edit-a-methodology"></a><span data-ttu-id="5f077-124">方法を編集</span><span class="sxs-lookup"><span data-stu-id="5f077-124">Edit a methodology</span></span>
1.  <span data-ttu-id="5f077-125">LCS ホーム ページで、**方法の管理**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-125">On the LCS home page, select the **Manage methodologies** tile.</span></span>
2.  <span data-ttu-id="5f077-126">編集方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-126">Select the methodology to edit.</span></span>
3.  <span data-ttu-id="5f077-127">**方法の編集**ボタン (鉛筆記号) を選択し、方法を編集します。</span><span class="sxs-lookup"><span data-stu-id="5f077-127">Select the **Edit methodology** button (the pencil symbol), and edit the methodology.</span></span>

## <a name="edit-a-projects-methodology"></a><span data-ttu-id="5f077-128">プロジェクトの方法の編集</span><span class="sxs-lookup"><span data-stu-id="5f077-128">Edit a project's methodology</span></span>
<span data-ttu-id="5f077-129">特定のプロジェクトでのみ方法を編集するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5f077-129">Follow these steps to edit a methodology in a specific project only.</span></span>

1.  <span data-ttu-id="5f077-130">プロジェクトのホーム ページで、プロジェクト フェーズ上の省略記号 (**...**) ボタンを選択し、**方法の編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-130">On the project's home page, select the ellipsis (**...**) button above the project phases, and then select **Edit methodology**.</span></span>
2.  <span data-ttu-id="5f077-131">フェーズおよびタスクを編集します。</span><span class="sxs-lookup"><span data-stu-id="5f077-131">Edit the phases and tasks.</span></span>
3.  <span data-ttu-id="5f077-132">変更が必要な場合は、リンクされているツールおよびリソースを編集します。</span><span class="sxs-lookup"><span data-stu-id="5f077-132">Edit the linked tools and resources, if any changes are required.</span></span>

## <a name="change-a-projects-methodology"></a><span data-ttu-id="5f077-133">プロジェクトの方法の変更</span><span class="sxs-lookup"><span data-stu-id="5f077-133">Change a project’s methodology</span></span>
1.  <span data-ttu-id="5f077-134">プロジェクトのホーム ページで、プロジェクト フェーズ上の省略記号 (**...**) ボタンをクリックし、**方法を変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5f077-134">On the project's home page, click the ellipsis (**...**) button above the project phases, and then click **Change methodology**.</span></span>
2.  <span data-ttu-id="5f077-135">表示されるダイアログ ボックスで、**既存のフェーズとタスクを保持しますか?** オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="5f077-135">In the dialog box that appears, set the **Do you want to keep the existing phases and tasks?** option.</span></span> <span data-ttu-id="5f077-136">このオプションを**はい**に設定すると、手順 3 で選択した方法論のフェーズとタスクが現在の方法論の終わりに追加されます。</span><span class="sxs-lookup"><span data-stu-id="5f077-136">If you set this option to **Yes**, the phases and tasks from the methodology that you select in step 3 are added to the end of the current methodology.</span></span> <span data-ttu-id="5f077-137">オプションを**いいえ**に設定すると、現在の方法は、手順 3 で選択した方法に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="5f077-137">If you set the option to **No**, the current methodology is replaced with the methodology that you select in step 3.</span></span>
3.  <span data-ttu-id="5f077-138">プロジェクトで使用する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-138">Select a methodology to use with your project.</span></span>
4.  <span data-ttu-id="5f077-139">**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5f077-139">Select **Confirm**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="5f077-140">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="5f077-140">Additional resources</span></span>
--------

[<span data-ttu-id="5f077-141">AppSource の Dynamics 365 for Finance and Operations アプリを公開</span><span class="sxs-lookup"><span data-stu-id="5f077-141">Publishing an App for Dynamics 365 for Finance and Operations in AppSource</span></span>](lcs-solutions-app-source.md)


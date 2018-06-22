---
title: "LCS ソリューションへの方法の追加"
description: "このトピックでは、各種手法を作成および変更する方法について説明します。 また、方法の要件に関する情報も提供されます。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 493983c4ae0bd657df0fc00a54c933e2127846b8
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="add-a-methodology-to-an-lcs-solution"></a><span data-ttu-id="8d1e8-104">LCS ソリューションへの方法の追加</span><span class="sxs-lookup"><span data-stu-id="8d1e8-104">Add a methodology to an LCS solution</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d1e8-105">このトピックでは、各種手法を作成および変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-105">This topic explains how to create and modify methodologies.</span></span> <span data-ttu-id="8d1e8-106">また、方法の要件に関する情報も提供されます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-106">It also provides information about the requirements for methodologies.</span></span>

<a name="methodology-requirements"></a><span data-ttu-id="8d1e8-107">方法の要件</span><span class="sxs-lookup"><span data-stu-id="8d1e8-107">Methodology requirements</span></span>
------------------------

<span data-ttu-id="8d1e8-108">方法論の最初の 2 つのフェーズは、LCS ソリューションの消費方法論からの学習と消費のフェーズでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-108">The first two phases of your methodology must be the Learn and Consume phases from the LCS Solutions Consumption methodology.</span></span> <span data-ttu-id="8d1e8-109">学習段階の製品の説明は、業務プロセス ライブラリ、マーケティング材料の説明または概要、およびソリューションの現在のバージョンでサポートされている機能と一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-109">Your product description in the Learn phase must be aligned with your business process library, the descriptions or summaries in your marketing material, and the functionality that is supported in the current version of your solution.</span></span> <span data-ttu-id="8d1e8-110">学習フェーズには次の作業が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-110">The Learn phase includes the following tasks:</span></span>

-   <span data-ttu-id="8d1e8-111">**製品の説明** – マーケティングの説明を Microsoft Dynamics Lifecycle Services (LCS) の方法に追加して活用してください。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-111">**Product description** – Take advantage of your marketing description by adding it to the Microsoft Dynamics Lifecycle Services (LCS) methodology.</span></span>
-   <span data-ttu-id="8d1e8-112">**概要を取得** – 機能、アーキテクチャに関する情報など、ソリューションが示されます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-112">**Get an overview** – Include content for your solution, such as information about features, architecture, and more.</span></span>
-   <span data-ttu-id="8d1e8-113">**ヘルプを入手する方法** – ソリューションの構築と保守に貢献した人のために、会社の Web サイトへの番号、連絡先、または直接リンクを含めます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-113">**How to get help** – Include numbers, contacts, or direct links to your company's website, for people who contribute to building and maintaining the solution.</span></span>

<span data-ttu-id="8d1e8-114">消費フェーズには、会議室パイロット 1 (CRP1) を完了するために必要なタスクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-114">The Consume phase includes tasks that are required in order to complete Conference room pilot 1 (CRP1).</span></span> <span data-ttu-id="8d1e8-115">詳細情報と消費のフェーズの後に、ソリューションを実装するために必要な手順を追加します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-115">After the Learn and Consume phases, add the steps that are required in order to implement your solution.</span></span> <span data-ttu-id="8d1e8-116">ソリューションに合うようにフェーズとタスクを変更するか、会社の実装方法を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-116">You can either modify the phases and tasks so that they are aligned with your solution, or use your company’s implementation methodology.</span></span>

## <a name="create-a-new-methodology"></a><span data-ttu-id="8d1e8-117">新しい方法の作成</span><span class="sxs-lookup"><span data-stu-id="8d1e8-117">Create a new methodology</span></span>
1.  <span data-ttu-id="8d1e8-118">LCS ホーム ページで、**方法の管理**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-118">On the LCS home page, click the **Manage methodologies** tile.</span></span>
2.  <span data-ttu-id="8d1e8-119">**新しい方法**ボタン (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-119">Click the **New methodology** button (**+**).</span></span>
3.  <span data-ttu-id="8d1e8-120">フィールドの値を設定し、**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-120">Set values for the fields, and then click **Confirm**.</span></span>
4.  <span data-ttu-id="8d1e8-121">フェーズおよびタスクを作成します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-121">Create phases and tasks.</span></span>
5.  <span data-ttu-id="8d1e8-122">必要なリンクされているツールとリソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-122">Add any linked tools and resources that are required.</span></span>

## <a name="edit-a-methodology"></a><span data-ttu-id="8d1e8-123">方法を編集</span><span class="sxs-lookup"><span data-stu-id="8d1e8-123">Edit a methodology</span></span>
1.  <span data-ttu-id="8d1e8-124">LCS ホーム ページで、**方法の管理**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-124">On the LCS home page, click the **Manage methodologies** tile.</span></span>
2.  <span data-ttu-id="8d1e8-125">編集方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-125">Select the methodology to edit.</span></span>
3.  <span data-ttu-id="8d1e8-126">**方法の編集** (鉛筆) ボタンをクリックし、方法を編集します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-126">Click the **Edit methodology** (pencil) button, and edit the methodology.</span></span>

## <a name="edit-a-projects-methodology"></a><span data-ttu-id="8d1e8-127">プロジェクトの方法を編集</span><span class="sxs-lookup"><span data-stu-id="8d1e8-127">Edit a project’s methodology</span></span>
<span data-ttu-id="8d1e8-128">特定のプロジェクトでのみ方法を編集するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-128">Follow these steps to edit a methodology in a specific project only.</span></span>

1.  <span data-ttu-id="8d1e8-129">プロジェクトのホーム ページで、プロジェクト フェーズ上の省略記号 (**...**) ボタンをクリックし、**方法の編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-129">On the project's home page, click the ellipsis (**...**) button above the project phases, and then click **Edit methodology**.</span></span>
2.  <span data-ttu-id="8d1e8-130">フェーズおよびタスクを編集します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-130">Edit the phases and tasks.</span></span>
3.  <span data-ttu-id="8d1e8-131">変更が必要な場合は、リンクされているツールおよびリソースを編集します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-131">Edit the linked tools and resources, if any changes are required.</span></span>

## <a name="change-a-projects-methodology"></a><span data-ttu-id="8d1e8-132">プロジェクトの方法の変更</span><span class="sxs-lookup"><span data-stu-id="8d1e8-132">Change a project’s methodology</span></span>
1.  <span data-ttu-id="8d1e8-133">プロジェクトのホーム ページで、プロジェクト フェーズ上の省略記号 (**...**) ボタンをクリックし、**方法を変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-133">On the project's home page, click the ellipsis (**...**) button above the project phases, and then click **Change methodology**.</span></span>
2.  <span data-ttu-id="8d1e8-134">表示されるダイアログ ボックスで、**既存のフェーズとタスクを保持しますか?** オプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-134">In the dialog box that appears, set the **Do you want to keep the existing phases and tasks?** option.</span></span> <span data-ttu-id="8d1e8-135">このオプションを**はい**に設定すると、手順 3 で選択した方法論のフェーズとタスクが現在の方法論の終わりに追加されます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-135">If you set this option to **Yes**, the phases and tasks from the methodology that you select in step 3 are added to the end of the current methodology.</span></span> <span data-ttu-id="8d1e8-136">オプションを**いいえ**に設定すると、現在の方法は、手順 3 で選択した方法に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-136">If you set the option to **No**, the current methodology is replaced with the methodology that you select in step 3.</span></span>
3.  <span data-ttu-id="8d1e8-137">プロジェクトで使用する方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-137">Select a methodology to use with your project.</span></span>
4.  <span data-ttu-id="8d1e8-138">**確定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8d1e8-138">Click **Confirm**.</span></span>


<a name="additional-resources"></a><span data-ttu-id="8d1e8-139">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="8d1e8-139">Additional resources</span></span>
--------

[<span data-ttu-id="8d1e8-140">AppSource 向け LCS ソリューション ホームページ</span><span class="sxs-lookup"><span data-stu-id="8d1e8-140">LCS Solutions for AppSource home page</span></span>](lcs-solutions-app-source.md)





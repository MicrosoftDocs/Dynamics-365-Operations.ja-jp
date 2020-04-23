---
title: 条件評価
description: このトピックでは、資産管理の資産に条件評価テンプレートと登録を作成する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2694b3ee51e2619a94e7ea2f4039fb52adddbbc
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208918"
---
# <a name="condition-assessment"></a><span data-ttu-id="4412c-103">条件評価</span><span class="sxs-lookup"><span data-stu-id="4412c-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="4412c-104">このトピックでは、資産管理の資産に条件評価テンプレートと登録を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4412c-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="4412c-105">条件評価は定期的に実行され、主な目的は資産に関する条件データを作成および管理することです。</span><span class="sxs-lookup"><span data-stu-id="4412c-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="4412c-106">予防的メンテナンスの観点から見ると、現状や残存寿命などの重要な情報を監視することが重要です。</span><span class="sxs-lookup"><span data-stu-id="4412c-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="4412c-107">また、定期的に条件評価を行えば、工場の機械の状態を監視および比較することができます。</span><span class="sxs-lookup"><span data-stu-id="4412c-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="4412c-108">条件評価は、設備の多くの状態を測定および監視するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="4412c-109">例: 機械の振動を測定できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="4412c-110">さまざまなタイプの機器で資産管理に振動測定値を登録すると、最新の登録評価を検索し、振動測定値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="4412c-111">条件評価は資産に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="4412c-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="4412c-112">条件評価手順を実行する前に、資産タイプに条件評価テンプレートを設定します。</span><span class="sxs-lookup"><span data-stu-id="4412c-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="4412c-113">条件評価にテンプレートを使用する理由は、類似の資産の条件データの変動を回避するためです。</span><span class="sxs-lookup"><span data-stu-id="4412c-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="4412c-114">資産管理で条件評価を設定および使用する順序は次のとおりです。最初に、必要な条件評価テンプレートを設定します。</span><span class="sxs-lookup"><span data-stu-id="4412c-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="4412c-115">次に、**資産タイプ** フォームの資産タイプにテンプレートを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="4412c-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="4412c-116">最後に、**資産**フォームの資産に条件評価登録を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="4412c-117">条件評価テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="4412c-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="4412c-118">**資産管理** > **設定** > **資産タイプ** > **条件評価**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4412c-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="4412c-119">**新規** を選択して、新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="4412c-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="4412c-120">**テンプレート** フィールドに、テンプレートの ID を挿入します。</span><span class="sxs-lookup"><span data-stu-id="4412c-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="4412c-121">**名前**フィールドに、テンプレートの名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="4412c-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="4412c-122">**条件評価明細行**クイック タブで、適切な条件タイプと測定単位の選択を含む、条件評価に必要な明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="4412c-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="4412c-123">**資産タイプ**クイック タブで、条件評価テンプレートを使用する資産タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="4412c-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="4412c-124">画面上部にある**詳細**グループの**明細行**フィールドと**資産タイプ** フィールドには、選択した条件評価テンプレートに関連する評価明細行と資産タイプの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4412c-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="4412c-125">資産に対する条件評価登録の作成</span><span class="sxs-lookup"><span data-stu-id="4412c-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="4412c-126">**資産管理**  >  **共通**  >  **資産**  >  **全資産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4412c-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="4412c-127">そのリストで、条件評価登録を作成する対象の資産を選択します。</span><span class="sxs-lookup"><span data-stu-id="4412c-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="4412c-128">**一般**タブで、**条件評価**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4412c-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="4412c-129">**新規**をクリックして、新しい登録を作成します。</span><span class="sxs-lookup"><span data-stu-id="4412c-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="4412c-130">**日付**フィールドで条件評価の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="4412c-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="4412c-131">**作業者**フィールドで、評価登録を実行した作業者の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="4412c-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="4412c-132">**明細行**フィールドには、条件評価に設定された評価明細行の数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4412c-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="4412c-133">**テンプレート** フィールドで条件評価のテンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="4412c-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="4412c-134">テンプレートの名前は自動的に**名前**フィールドに挿入され、関連する登録明細行は**条件評価明細行**クイック タブに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="4412c-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="4412c-135">選択した条件評価に関連するメモを**メモ** クイック タブに挿入できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="4412c-136">各条件評価明細行ごとに、測定データを**値**フィールドに挿入します。</span><span class="sxs-lookup"><span data-stu-id="4412c-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="4412c-137">**条件評価行**クイック タブ > **コメント** フィールドに、選択した登録明細行に関連するコメントを挿入できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="4412c-138">明細行にコメントを追加すると、**コメント** チェック ボックスが自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="4412c-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="4412c-139">資産の条件評価登録を行った後、条件評価レポートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="4412c-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="4412c-140">また、作業指示書に条件評価を登録することもできます (**資産管理** > **共通** > **作業指示書** > **すべての作業指示書** > **条件評価**ボタン)。</span><span class="sxs-lookup"><span data-stu-id="4412c-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>

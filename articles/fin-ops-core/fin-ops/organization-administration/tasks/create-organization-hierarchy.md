---
title: 組織階層の作成
description: 組織階層を作成するには、次の手順に従います。
author: sericks007
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d27bec86302f3e6cef8318a0d846f31d2d9c6a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747396"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="b378d-103">組織階層の作成</span><span class="sxs-lookup"><span data-stu-id="b378d-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b378d-104">組織階層を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="b378d-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="b378d-105">業務について、さまざまな観点から表示と報告を行う組織階層を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b378d-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="b378d-106">たとえば、税金、法律、または法令についての報告に使用する 1 つの階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b378d-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="b378d-107">法的に必須でなくても、内部報告に使用する財務情報を報告する別の階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="b378d-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="b378d-108">組織階層を作成する前に、組織を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b378d-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="b378d-109">詳細については、「法人の作成」 または 「作業単位の作成」 のタスクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b378d-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="b378d-110">また、部署およびチームも作成できます。</span><span class="sxs-lookup"><span data-stu-id="b378d-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="b378d-111">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="b378d-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="b378d-112">階層の作成</span><span class="sxs-lookup"><span data-stu-id="b378d-112">Create a hierarchy</span></span>
1. <span data-ttu-id="b378d-113">**ナビゲーション ウィンドウ > モジュール > 組織管理 > 組織 > 組織階層** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b378d-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="b378d-114">**アクション ウィンドウ** で、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b378d-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="b378d-115">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b378d-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b378d-116">**目的** セクションで、**目的の割り当て** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b378d-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="b378d-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b378d-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="b378d-118">組織階層に割り当てる目的を選択します。</span><span class="sxs-lookup"><span data-stu-id="b378d-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="b378d-119">**割り当て済の階層** セクションで、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b378d-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="b378d-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b378d-120">In the list, mark the selected row.</span></span> <span data-ttu-id="b378d-121">作成した階層を検索します。</span><span class="sxs-lookup"><span data-stu-id="b378d-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="b378d-122">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b378d-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="b378d-123">階層への組織の追加</span><span class="sxs-lookup"><span data-stu-id="b378d-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="b378d-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b378d-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="b378d-125">階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="b378d-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="b378d-126">**割り当て済の階層** セクションで、**セクションで** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b378d-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="b378d-127">必要に応じて組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="b378d-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="b378d-128">組織を追加するには、**編集**、 次に **挿入** をクリックして組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="b378d-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="b378d-129">変更が完了したら、ドラフトを **保存** または変更を **公開** できます。</span><span class="sxs-lookup"><span data-stu-id="b378d-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
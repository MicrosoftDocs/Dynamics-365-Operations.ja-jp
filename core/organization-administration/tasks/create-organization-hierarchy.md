--- 
title: "組織階層の作成"
description: "組織階層を作成するには、次の手順に従います。"
author: sericks007
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: be64b137fc885747bcd9e3cf11013a18b7835d0e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="d2412-103">組織階層の作成</span><span class="sxs-lookup"><span data-stu-id="d2412-103">Create an organization hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2412-104">組織階層を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d2412-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="d2412-105">業務について、さまざまな観点から表示と報告を行う組織階層を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="d2412-106">たとえば、税金、法律、または法令についての報告に使用する 1 つの階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="d2412-107">法的に必須でなくても、内部報告に使用する財務情報を報告する別の階層を設定できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="d2412-108">組織階層を作成する前に、組織を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2412-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="d2412-109">詳細については、「法人の作成」または「作業単位の作成」のタスクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2412-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="d2412-110">また、部署およびチームも作成できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="d2412-111">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="d2412-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="d2412-112">階層の作成</span><span class="sxs-lookup"><span data-stu-id="d2412-112">Create a hierarchy</span></span>
1. <span data-ttu-id="d2412-113">[組織管理] > [組織] > [組織階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d2412-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="d2412-114">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2412-114">Click New.</span></span>
3. <span data-ttu-id="d2412-115">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d2412-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d2412-116">[目的の割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2412-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="d2412-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d2412-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2412-118">組織階層に割り当てる目的を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2412-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="d2412-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2412-119">Click Add.</span></span>
7. <span data-ttu-id="d2412-120">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="d2412-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d2412-121">作成した階層を検索します。</span><span class="sxs-lookup"><span data-stu-id="d2412-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="d2412-122">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2412-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="d2412-123">階層への組織の追加</span><span class="sxs-lookup"><span data-stu-id="d2412-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="d2412-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="d2412-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d2412-125">階層を選択します。</span><span class="sxs-lookup"><span data-stu-id="d2412-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="d2412-126">[階層の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d2412-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="d2412-127">必要に応じて組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="d2412-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="d2412-128">組織を追加するには、[編集]、[挿入] にクリックして組織を追加します。</span><span class="sxs-lookup"><span data-stu-id="d2412-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="d2412-129">変更が完了したら、ドラフトを保存または変更を公開できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  



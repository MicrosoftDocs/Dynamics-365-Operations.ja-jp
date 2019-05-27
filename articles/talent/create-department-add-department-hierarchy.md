---
title: 部門の作成および部門階層への追加
description: 部門は、組織のカテゴリまたは機能領域を表す作業単位です。 部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。 機能領域の報告に部門を使用できます。 部門は損益の職責を持つ場合があります。
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 7b6308c54d237d0d7558fc1f94647f7ca1ab82a1
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506177"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a><span data-ttu-id="4a361-106">部門の作成および部門階層への追加</span><span class="sxs-lookup"><span data-stu-id="4a361-106">Create departments and include them in the department hierarchy</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4a361-107">部門は、組織のカテゴリまたは機能領域を表す作業単位です。</span><span class="sxs-lookup"><span data-stu-id="4a361-107">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="4a361-108">部門は、販売、会計、または人事管理など、組織内の特定の領域を担当します。</span><span class="sxs-lookup"><span data-stu-id="4a361-108">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="4a361-109">機能領域の報告に部門を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4a361-109">You can use departments to report on functional areas.</span></span> <span data-ttu-id="4a361-110">部門は損益の職責を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="4a361-110">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="4a361-111">部門はコスト センターのグループを含む場合があります。</span><span class="sxs-lookup"><span data-stu-id="4a361-111">A department might include a group of cost centers.</span></span> <span data-ttu-id="4a361-112">職位は部門に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4a361-112">Positions can be assigned to departments.</span></span> <span data-ttu-id="4a361-113">部門を作成するには、**人事管理** &gt; **部門** &gt; **部門**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a361-113">To create a department, click **Human Resources** &gt; **Departments** &gt; **Department**.</span></span> <span data-ttu-id="4a361-114">次の表に、使用できるフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="4a361-114">The following table describes the fields that are available.</span></span>

| <span data-ttu-id="4a361-115">フィールド</span><span class="sxs-lookup"><span data-stu-id="4a361-115">Field</span></span>               | <span data-ttu-id="4a361-116">説明</span><span class="sxs-lookup"><span data-stu-id="4a361-116">Description</span></span>                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a361-117">氏名</span><span class="sxs-lookup"><span data-stu-id="4a361-117">Name</span></span>                | <span data-ttu-id="4a361-118">部門の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a361-118">Enter a name for the department.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="4a361-119">部門番号</span><span class="sxs-lookup"><span data-stu-id="4a361-119">Department number</span></span>   | <span data-ttu-id="4a361-120">番号順序コードが、**組織番号**参照に、**番号順序**ページで割り当てられている場合、既定値が自動的に生成されることがあります。</span><span class="sxs-lookup"><span data-stu-id="4a361-120">A default value might be generated automatically if a number sequence code is assigned to the **Organization number** reference on the **Number sequences** page.</span></span>                                                 |
| <span data-ttu-id="4a361-121">検索名</span><span class="sxs-lookup"><span data-stu-id="4a361-121">Search name</span></span>         | <span data-ttu-id="4a361-122">部門の検索に使用できる名前あるいは略称を入力します。</span><span class="sxs-lookup"><span data-stu-id="4a361-122">Enter a name or acronym that can be used to search for the department.</span></span>                                                                                                                                            |
| <span data-ttu-id="4a361-123">メモ</span><span class="sxs-lookup"><span data-stu-id="4a361-123">Memo</span></span>                | <span data-ttu-id="4a361-124">追加情報をここに入力します。</span><span class="sxs-lookup"><span data-stu-id="4a361-124">Enter any additional information here.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="4a361-125">階層</span><span class="sxs-lookup"><span data-stu-id="4a361-125">In hierarchy</span></span>        | <span data-ttu-id="4a361-126">チェック ボックスがオンの場合、部門が部門の階層に含まれることを示します。</span><span class="sxs-lookup"><span data-stu-id="4a361-126">A selected check box indicates that the department is included in the department hierarchy.</span></span> <span data-ttu-id="4a361-127">部門の階層に部門を追加する方法については、この記事の情報を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a361-127">For information about how to add a department to the department hierarchy, see the information later in this article.</span></span> |
| <span data-ttu-id="4a361-128">DUNS 番号</span><span class="sxs-lookup"><span data-stu-id="4a361-128">DUNS number</span></span>         | <span data-ttu-id="4a361-129">DUNS は、データ普遍的の番号付けシステムを意味します。</span><span class="sxs-lookup"><span data-stu-id="4a361-129">DUNS stands for Data Universal Number System.</span></span> <span data-ttu-id="4a361-130">これは Dun and Bradstreet が発行する 9 桁の番号です。</span><span class="sxs-lookup"><span data-stu-id="4a361-130">This is a nine-digit number that is issued by Dun & Bradstreet.</span></span>                                                                                                     |
| <span data-ttu-id="4a361-131">マネージャー</span><span class="sxs-lookup"><span data-stu-id="4a361-131">Manager</span></span>             | <span data-ttu-id="4a361-132">部門を管理するペルソナを入力します。</span><span class="sxs-lookup"><span data-stu-id="4a361-132">Enter the persona that manages the department.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="4a361-133">住所</span><span class="sxs-lookup"><span data-stu-id="4a361-133">Addresses</span></span>           | <span data-ttu-id="4a361-134">部門の住所情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="4a361-134">Add the address information for the department.</span></span> <span data-ttu-id="4a361-135">たとえば、部門が位置する建物の住所を追加します。</span><span class="sxs-lookup"><span data-stu-id="4a361-135">For example, add the mailing address for the building that the department is located in.</span></span>                                                                          |
| <span data-ttu-id="4a361-136">連絡先情報</span><span class="sxs-lookup"><span data-stu-id="4a361-136">Contact information</span></span> | <span data-ttu-id="4a361-137">部門の連絡先情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="4a361-137">Add contact information for the department.</span></span> <span data-ttu-id="4a361-138">たとえば、部門のサービスデスクの電話番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="4a361-138">For example, add a telephone number for the service desk in the department.</span></span>                                                                                           |

<span data-ttu-id="4a361-139">部門の階層に部門を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4a361-139">To add a department to the department hierarchy, follow these steps.</span></span>

1.  <span data-ttu-id="4a361-140">**人事管理** &gt; **部門** &gt; **部門の階層**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a361-140">Click **Human Resources** &gt; **Departments** &gt; **Department hierarchy**.</span></span>
2.  <span data-ttu-id="4a361-141">**編集**をクリックし、部門があるべき組織を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a361-141">Click **Edit**, and then select the organization that the department should be under.</span></span>
3.  <span data-ttu-id="4a361-142">**挿入**をクリックし、リストから**部門**を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a361-142">Click **Insert**, and select **Department** in the list.</span></span>
4.  <span data-ttu-id="4a361-143">表示される部門の一覧で、階層に追加する部門を選択します。</span><span class="sxs-lookup"><span data-stu-id="4a361-143">In the list of departments that appears, select the department to add to the hierarchy.</span></span>
5.  <span data-ttu-id="4a361-144">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="4a361-144">Save your changes.</span></span> <span data-ttu-id="4a361-145">階層のドラフト バージョンが作成されたことを知らせるメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4a361-145">You receive a message that a draft version of the hierarchy has been created.</span></span>
6.  <span data-ttu-id="4a361-146">準備が整ったら、階層デザイナーで**公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4a361-146">When you're ready, click **Publish** in the hierarchy designer.</span></span> <span data-ttu-id="4a361-147">階層をいつ公開する必要があるかを示す有効日を入力できます。</span><span class="sxs-lookup"><span data-stu-id="4a361-147">You can enter an effective date that indicates when the hierarchy should be published.</span></span> <span data-ttu-id="4a361-148">たとえば、次の暦年の期首に新しい部門を追加する場合、新しい暦年の 1 月 1 日に有効日を設定します。</span><span class="sxs-lookup"><span data-stu-id="4a361-148">For example, to add a new department at the beginning of the next calendar year, set the effective date to January 1 of the new calendar year.</span></span> <span data-ttu-id="4a361-149">階層を変更すると、その日付に対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="4a361-149">The changes to the hierarchy will take effect on that date.</span></span>

## <a name="steps-for-creating-a-department"></a><span data-ttu-id="4a361-150">部門を作成する手順</span><span class="sxs-lookup"><span data-stu-id="4a361-150">Steps for creating a department</span></span>
<span data-ttu-id="4a361-151">新しい部門を作成するためのステップ バイ ステップの手順については次のトピック [新しい部門の定義](../fin-and-ops/hr/tasks/define-new-departments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4a361-151">Refer to the [Define new departments](../fin-and-ops/hr/tasks/define-new-departments.md) topic for the step-by-step procedure for creating a new department.</span></span> 

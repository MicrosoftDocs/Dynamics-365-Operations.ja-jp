---
title: "テンプレート BOM の作成"
description: "テンプレート BOM はさまざまな方法を使用して作成できます。"
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a80cf596a3e7c7f08d493a0fb7350fad62d38c3e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="1385c-103">テンプレート BOM の作成</span><span class="sxs-lookup"><span data-stu-id="1385c-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1385c-104">テンプレート BOM は次のいずれかの方法を使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="1385c-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="1385c-105">すべての方法において、**開始日**および**終了日**フィールドは省略可能であり、情報提供のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="1385c-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="1385c-106">テンプレート BOM を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="1385c-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="1385c-107">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1385c-108">Ctrl + N キーを押して**テンプレート BOM の作成**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="1385c-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1385c-109">**参照から BOM 明細行をコピー**の下で、**手動**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="1385c-110">**品目番号**フィールドで、タイプ**BOM**の品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="1385c-111">**名前**フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1385c-112">**開始日**および**終了日**フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1385c-113">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-113">Click **OK**.</span></span>

<span data-ttu-id="1385c-114">新しい、空のテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1385c-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="1385c-115">別のテンプレート BOM に基づいてテンプレート BOM を作成する</span><span class="sxs-lookup"><span data-stu-id="1385c-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="1385c-116">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1385c-117">Ctrl + N キーを押して**テンプレート BOM の作成**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="1385c-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1385c-118">**参照から BOM 明細行をコピー**の下で、**テンプレート BOM**オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="1385c-119">**参照番号**フィールドで、新しいテンプレート BOM にコピーする既存のテンプレート BOM を選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="1385c-120">**名前**フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1385c-121">**開始日**および**終了日**フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1385c-122">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-122">Click **OK**.</span></span>

<span data-ttu-id="1385c-123">元のテンプレート BOM の明細行に対応する明細行を使用する、新しいテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1385c-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="1385c-124">品目 BOM に基づいてテンプレート BOM を作成する</span><span class="sxs-lookup"><span data-stu-id="1385c-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="1385c-125">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1385c-126">Ctrl + N キーを押して**テンプレート BOM の作成**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="1385c-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1385c-127">**参照から BOM 明細行をコピー**の下で、**BOM**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="1385c-128">**参照番号**フィールドで、BOM バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="1385c-129">BOM タイプの品目が**品目番号**にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="1385c-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="1385c-130">**名前**フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1385c-131">**開始日**および**終了日**フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1385c-132">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-132">Click **OK**.</span></span>

<span data-ttu-id="1385c-133">**部品表**に表示された BOM の明細行に対応する明細行を使用して、新しいテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1385c-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="1385c-134">生産 BOM に基づいてテンプレート BOM を作成する</span><span class="sxs-lookup"><span data-stu-id="1385c-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="1385c-135">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="1385c-136">Ctrl + N キーを押して**テンプレート BOM の作成**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="1385c-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="1385c-137">**参照から BOM 明細行をコピー**の下で、**生産**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="1385c-138">**参照番号**フィールドで、生産 BOM を選択します。</span><span class="sxs-lookup"><span data-stu-id="1385c-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="1385c-139">**名前**フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="1385c-140">**開始日**および**終了日**フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="1385c-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="1385c-141">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1385c-141">Click **OK**.</span></span>

<span data-ttu-id="1385c-142">**BOM**に表示された BOM の明細行に対応する明細行を使用して、新しいテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="1385c-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1385c-143">参照</span><span class="sxs-lookup"><span data-stu-id="1385c-143">See also</span></span>

[<span data-ttu-id="1385c-144">テンプレート BOM</span><span class="sxs-lookup"><span data-stu-id="1385c-144">Template BOMs</span></span>](template-boms.md)

  




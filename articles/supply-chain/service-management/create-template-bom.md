---
title: テンプレート BOM の作成
description: テンプレート BOM はさまざまな方法を使用して作成できます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b34cc2e9921df6e3ef619e2b2adaf8d2069fbac
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974563"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="20da0-103">テンプレート BOM の作成</span><span class="sxs-lookup"><span data-stu-id="20da0-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="20da0-104">テンプレート BOM は次のいずれかの方法を使用して作成できます。</span><span class="sxs-lookup"><span data-stu-id="20da0-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="20da0-105">すべての方法において、**開始日** および **終了日** フィールドは省略可能であり、情報提供のみを目的としています。</span><span class="sxs-lookup"><span data-stu-id="20da0-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="20da0-106">テンプレート BOM を手動で作成する</span><span class="sxs-lookup"><span data-stu-id="20da0-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="20da0-107">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="20da0-108">Ctrl + N キーを押して **テンプレート BOM の作成** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="20da0-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="20da0-109">**参照から BOM 明細行をコピー** の下で、**手動** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="20da0-110">**品目番号** フィールドで、タイプ **BOM** の品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="20da0-111">**名前** フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="20da0-112">**開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="20da0-113">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-113">Click **OK**.</span></span>

<span data-ttu-id="20da0-114">新しい、空のテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="20da0-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="20da0-115">別のテンプレート BOM に基づいてテンプレート BOM を作成する</span><span class="sxs-lookup"><span data-stu-id="20da0-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="20da0-116">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="20da0-117">Ctrl + N キーを押して **テンプレート BOM の作成** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="20da0-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="20da0-118">**参照から BOM 明細行をコピー** の下で、**テンプレート BOM** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="20da0-119">**参照番号** フィールドで、新しいテンプレート BOM にコピーする既存のテンプレート BOM を選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="20da0-120">**名前** フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="20da0-121">**開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="20da0-122">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-122">Click **OK**.</span></span>

<span data-ttu-id="20da0-123">元のテンプレート BOM の明細行に対応する明細行を使用する、新しいテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="20da0-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="20da0-124">品目 BOM に基づいてテンプレート BOM を作成する</span><span class="sxs-lookup"><span data-stu-id="20da0-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="20da0-125">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="20da0-126">Ctrl + N キーを押して **テンプレート BOM の作成** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="20da0-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="20da0-127">**参照から BOM 明細行をコピー** の下で、**BOM** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="20da0-128">**参照番号** フィールドで、BOM バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="20da0-129">BOM タイプの品目が **品目番号** にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="20da0-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="20da0-130">**名前** フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="20da0-131">**開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="20da0-132">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-132">Click **OK**.</span></span>

<span data-ttu-id="20da0-133">**部品表** に表示された BOM の明細行に対応する明細行を使用して、新しいテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="20da0-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="20da0-134">生産 BOM に基づいてテンプレート BOM を作成する</span><span class="sxs-lookup"><span data-stu-id="20da0-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="20da0-135">**サービス管理** \> **設定** \> **サービス対象** \> **テンプレート BOM** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="20da0-136">Ctrl + N キーを押して **テンプレート BOM の作成** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="20da0-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="20da0-137">**参照から BOM 明細行をコピー** の下で、**生産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="20da0-138">**参照番号** フィールドで、生産 BOM を選択します。</span><span class="sxs-lookup"><span data-stu-id="20da0-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="20da0-139">**名前** フィールドに、テンプレートの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="20da0-140">**開始日** および **終了日** フィールドに、テンプレート BOM を有効にする日付範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="20da0-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="20da0-141">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="20da0-141">Click **OK**.</span></span>

<span data-ttu-id="20da0-142">**BOM** に表示された BOM の明細行に対応する明細行を使用して、新しいテンプレート BOM が作成されます。</span><span class="sxs-lookup"><span data-stu-id="20da0-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="20da0-143">参照</span><span class="sxs-lookup"><span data-stu-id="20da0-143">See also</span></span>

[<span data-ttu-id="20da0-144">テンプレート BOM</span><span class="sxs-lookup"><span data-stu-id="20da0-144">Template BOMs</span></span>](template-boms.md)

  



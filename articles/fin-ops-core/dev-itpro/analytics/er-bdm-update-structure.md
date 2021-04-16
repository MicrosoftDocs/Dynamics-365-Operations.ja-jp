---
title: ビジネス ドキュメント テンプレートの構造の更新
description: このトピックでは、ビジネス ドキュメント管理機能を使用して、ビジネス ドキュメント テンプレートの構造を更新する方法について説明します。
author: NickSelin
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-12-01
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 203c9f0990051c1618660959dad0e184add68ffa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750487"
---
# <a name="update-the-structure-of-a-business-document-template"></a><span data-ttu-id="6e91a-103">ビジネス ドキュメント テンプレートの構造の更新</span><span class="sxs-lookup"><span data-stu-id="6e91a-103">Update the structure of a business document template</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6e91a-104">[ビジネス ドキュメント管理](er-business-document-management.md) テンプレート エディターの **テンプレート構造** ペインで 、Microsoft Excel のテンプレートに [新しいフィールドを追加](er-bdm-add-field-to-excel-template.md) することによって、ビジネス ドキュメント テンプレートを変更できます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-104">In the **Template structure** pane of the [Business document management](er-business-document-management.md) template editor, you can modify a business document template by [adding new fields](er-bdm-add-field-to-excel-template.md) to a template in Microsoft Excel.</span></span> <span data-ttu-id="6e91a-105">テンプレートの構造が Dynamics 365 Finance で自動的に更新されるので、**テンプレート構造** ペインで行った変更が反映されます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-105">The structure of the template is then automatically updated in Dynamics 365 Finance, so that it reflects the changes that you made in the **Template structure** pane.</span></span>

<span data-ttu-id="6e91a-106">Office 365 オンライン機能を使用してテンプレートを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-106">You can also modify a template by using Office 365 online functionality.</span></span> <span data-ttu-id="6e91a-107">たとえば、画像や図形などの新しい名前付きの項目を編集可能なワークシートに追加できます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-107">For example, you can add a new named item, such as a picture or shape, to the editable worksheet.</span></span> <span data-ttu-id="6e91a-108">この場合、財務でテンプレートの構造が自動的に更新されず、追加した項目は **テンプレート構造** ペインに表示されません。</span><span class="sxs-lookup"><span data-stu-id="6e91a-108">In this case, the structure of the template isn't automatically updated in Finance, and the item that you added doesn't appear in the **Template structure** pane.</span></span> <span data-ttu-id="6e91a-109">テンプレート エディター ページの **構造の更新** を選択して、Finance のテンプレート構造を手動で更新します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-109">Manually update the template structure in Finance by selecting **Update structure** on the template editor page.</span></span>

<span data-ttu-id="6e91a-110">この機能の詳細については、次の例を実行します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-110">For more information about this feature, complete the following example.</span></span>

## <a name="example-update-the-structure-of-a-business-document-template"></a><span data-ttu-id="6e91a-111">例: ビジネス ドキュメント テンプレートの構造の更新</span><span class="sxs-lookup"><span data-stu-id="6e91a-111">Example: Update the structure of a business document template</span></span>

<span data-ttu-id="6e91a-112">この例では、Office Online でテンプレートを変更した後に、システム管理者が Finance でビジネス ドキュメント テンプレートの構造を更新する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-112">This example shows how a system administrator can update the structure of a business document template in Finance after the template is modified in Office Online.</span></span> <span data-ttu-id="6e91a-113">以降のセクションでは、関連する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-113">The following sections explain the steps that are involved.</span></span>

### <a name="prepare-a-business-document-template-for-editing"></a><span data-ttu-id="6e91a-114">編集用のビジネス ドキュメント テンプレートの準備</span><span class="sxs-lookup"><span data-stu-id="6e91a-114">Prepare a business document template for editing</span></span>

<span data-ttu-id="6e91a-115">[ビジネス ドキュメント管理の概要](er-business-document-management.md) で、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-115">Complete the following procedures in [Business document management overview](er-business-document-management.md).</span></span>

1. [<span data-ttu-id="6e91a-116">ER パラメーターの構成</span><span class="sxs-lookup"><span data-stu-id="6e91a-116">Configure ER parameters</span></span>](er-business-document-management.md#configure-er-parameters)
2. [<span data-ttu-id="6e91a-117">ER ソリューションのインポート</span><span class="sxs-lookup"><span data-stu-id="6e91a-117">Import ER solutions</span></span>](er-business-document-management.md#import-er-solutions)
3. [<span data-ttu-id="6e91a-118">ビジネス ドキュメント管理の有効</span><span class="sxs-lookup"><span data-stu-id="6e91a-118">Enable Business document management</span></span>](er-business-document-management.md#enable-business-document-management)
4. [<span data-ttu-id="6e91a-119">パラメータのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6e91a-119">Configure parameters</span></span>](er-business-document-management.md#configure-parameters)

### <a name="edit-a-business-document-template"></a><span data-ttu-id="6e91a-120">ビジネス ドキュメント テンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="6e91a-120">Edit a business document template</span></span>

1. <span data-ttu-id="6e91a-121">**ビジネス ドキュメント管理** ワークスペースで、**新規ドキュメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-121">In the **Business document management** workspace, select **New document**.</span></span>
2. <span data-ttu-id="6e91a-122">**新しいテンプレートの作成** ページで、**自由書式の請求書 (ER サンプル)(Excel)** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-122">On the **Create a new template** page, select the **Free text invoice (ER sample)(Excel)** template.</span></span>
3. <span data-ttu-id="6e91a-123">**ドキュメントの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-123">Select **Create document**.</span></span>
4. <span data-ttu-id="6e91a-124">**タイトル** フィールドに、**FTI サンプル Litware** と入力します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-124">In the **Title** field, enter **FTI sample Litware**.</span></span>
5. <span data-ttu-id="6e91a-125">**OK** を選択して、新しいテンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-125">Select **OK** to create the new template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e91a-126">Office Online にまだサインインしていない場合は、[Office 365 サインイン ページに移動](er-business-document-management.md#frequently-asked-questions) します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-126">If you haven't yet signed in to Office Online, you're [directed to the Office 365 sign-in page](er-business-document-management.md#frequently-asked-questions).</span></span> <span data-ttu-id="6e91a-127">Finance 環境に戻るには、ブラウザーの **戻る** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-127">To return to your Finance environment, select the **Back** button in your browser.</span></span>

    <span data-ttu-id="6e91a-128">新しいテンプレートが、テンプレート エディター ページの Excel Online 埋め込みコントロールで編集するために開かれます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-128">The new template is opened for editing in the Excel Online embedded control on the template editor page.</span></span>

<span data-ttu-id="6e91a-129">[![ビジネス ドキュメント管理ワークスペースを使用して、ビジネス ドキュメント テンプレートの編集を開始する](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span><span class="sxs-lookup"><span data-stu-id="6e91a-129">[![Using the Business document management workspace to start to edit a business document template](./media/er-bdm-update-structure1.gif)](./media/er-bdm-update-structure1.gif)</span></span>

### <a name="review-the-current-structure-of-the-editable-template"></a><span data-ttu-id="6e91a-130">編集可能なテンプレートの現在の構造の確認</span><span class="sxs-lookup"><span data-stu-id="6e91a-130">Review the current structure of the editable template</span></span>

1. <span data-ttu-id="6e91a-131">Excel Online のリボンにある **表示** タブの **表示** グループで、**グリッド線** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-131">In Excel Online, on the ribbon, on the **View** tab, in the **Show** group, select **Gridlines**.</span></span>
2. <span data-ttu-id="6e91a-132">編集可能なテンプレートで、テンプレート タイトルの上の四角形を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-132">In the editable template, select the rectangle above the template title.</span></span> <span data-ttu-id="6e91a-133">この四角形は、**rptHeaderCompLogo** という名前の画像になります。</span><span class="sxs-lookup"><span data-stu-id="6e91a-133">This rectangle is a picture that is named **rptHeaderCompLogo**.</span></span>
3. <span data-ttu-id="6e91a-134">**テンプレート構造** ペインが非表示になっている場合は、**構造を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-134">If the **Template structure** pane is hidden, select **Show structure**.</span></span>
4. <span data-ttu-id="6e91a-135">**テンプレート構造** ペインで、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-135">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="6e91a-136">Finance のテンプレート構造では、**rptHeaderCompLogo** 項目が、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の子項目として表示されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6e91a-136">Notice that, in the template structure in Finance, the **rptHeaderCompLogo** item is presented as a child item of **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>

<span data-ttu-id="6e91a-137">[![ビジネス ドキュメント 管理ワークスペースを使用して編集可能なテンプレートの現在の構造を確認する](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span><span class="sxs-lookup"><span data-stu-id="6e91a-137">[![Using the Business document management workspace to review the current structure of an editable template](./media/er-bdm-update-structure2.gif)](./media/er-bdm-update-structure2.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-deleting-a-picture"></a><span data-ttu-id="6e91a-138">画像を削除して、ビジネス ドキュメント テンプレートの構造を更新する</span><span class="sxs-lookup"><span data-stu-id="6e91a-138">Update the structure of a business document template by deleting a picture</span></span>

1. <span data-ttu-id="6e91a-139">Excel Online の編集可能なテンプレートで、**rptHeaderCompLogo** の画像を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-139">In Excel Online, in the editable template, select the **rptHeaderCompLogo** picture.</span></span>
2. <span data-ttu-id="6e91a-140">次のいずれかの手順に従って、編集可能なテンプレートから選択した画像を削除します:</span><span class="sxs-lookup"><span data-stu-id="6e91a-140">Follow one of these steps to delete the selected picture from the editable template:</span></span>

    - <span data-ttu-id="6e91a-141">キーボードの **Delete** キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-141">Select the **Delete** key on your keyboard.</span></span>
    - <span data-ttu-id="6e91a-142">画像を選択したまま (または右クリック) にして、**切り取り** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-142">Select and hold (or right-click) the picture, and then select **Cut**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e91a-143">**rptHeaderCompLogo** 項目は、画像が Excel テンプレートに含まれない場合でも、Finance のテンプレート構造に現在も存在しています。</span><span class="sxs-lookup"><span data-stu-id="6e91a-143">The **rptHeaderCompLogo** item is currently still present in the template structure in Finance, even though the picture is no longer included in the Excel template.</span></span>

3. <span data-ttu-id="6e91a-144">**構造の更新** を選択し、Excel および Finance で編集可能なテンプレートの構造を同期します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-144">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
4. <span data-ttu-id="6e91a-145">**テンプレート構造** ペインで、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-145">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
5. <span data-ttu-id="6e91a-146">**rptHeaderCompLogo** 項目が Finance のテンプレート構造に含まれていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6e91a-146">Notice that the **rptHeaderCompLogo** item is no longer included in the template structure in Finance.</span></span>

<span data-ttu-id="6e91a-147">[![ビジネス ドキュメント管理ワークスペースを使用して、ビジネス ドキュメント テンプレートから画像を削除する](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span><span class="sxs-lookup"><span data-stu-id="6e91a-147">[![Using the Business document management workspace to delete a picture from a business document template](./media/er-bdm-update-structure3.gif)](./media/er-bdm-update-structure3.gif)</span></span>

### <a name="update-the-structure-of-a-business-document-template-by-adding-a-picture"></a><span data-ttu-id="6e91a-148">画像を追加して、ビジネス ドキュメント テンプレートの構造を更新する</span><span class="sxs-lookup"><span data-stu-id="6e91a-148">Update the structure of a business document template by adding a picture</span></span>

1. <span data-ttu-id="6e91a-149">Excel Online のリボンにある **挿入** タブの **図** グループで、**画像** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-149">In Excel Online, on the ribbon, on the **Insert** tab, in the **Illustrations** group, select **Picture**.</span></span>
2. <span data-ttu-id="6e91a-150">**ファイルの選択** を選択し、追加するイメージを参照して選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-150">Select **Choose file**, browse to the image that you want to add, select it, and then select **OK**.</span></span>
3. <span data-ttu-id="6e91a-151">**挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-151">Select **Insert**.</span></span>
4. <span data-ttu-id="6e91a-152">新しい画像を正しい位置になるまで移動します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-152">Move the new picture until it's in the correct place.</span></span> <span data-ttu-id="6e91a-153">既定では、Excel が画像に名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-153">By default, Excel names the picture.</span></span> <span data-ttu-id="6e91a-154">たとえば、画像に **画像 2** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="6e91a-154">For example, it might name the picture **Picture 2**.</span></span>
5. <span data-ttu-id="6e91a-155">**構造の更新** を選択し、Excel および Finance で編集可能なテンプレートの構造を同期します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-155">Select **Update structure** to sync the structure of the editable template in Excel and Finance.</span></span>
6. <span data-ttu-id="6e91a-156">**テンプレート構造** ペインで、**レポート \> 請求書 \> rptHeader \> rptHeaderPart1** の順に展開します。</span><span class="sxs-lookup"><span data-stu-id="6e91a-156">In the **Template structure** pane, expand **Report \> Invoice \> rptHeader \> rptHeaderPart1**.</span></span>
7. <span data-ttu-id="6e91a-157">新しい画像が Finance のテンプレート構造の項目として含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6e91a-157">Notice that the new picture is now included as an item in the template structure in Finance.</span></span>

<span data-ttu-id="6e91a-158">[![ビジネス ドキュメント管理ワークスペースを使用して、ビジネス ドキュメント テンプレートに画像を追加する](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span><span class="sxs-lookup"><span data-stu-id="6e91a-158">[![Using the Business document management workspace to add a picture to a business document template](./media/er-bdm-update-structure4.gif)](./media/er-bdm-update-structure4.gif)</span></span>

## <a name="related-links"></a><span data-ttu-id="6e91a-159">関連リンク</span><span class="sxs-lookup"><span data-stu-id="6e91a-159">Related links</span></span>

[<span data-ttu-id="6e91a-160">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="6e91a-160">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="6e91a-161">ビジネス ドキュメント管理の概要</span><span class="sxs-lookup"><span data-stu-id="6e91a-161">Business document management overview</span></span>](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: Microsoft Excel のビジネス ドキュメント テンプレートへの新しいフィールドの追加
description: このトピックでは、ビジネス ドキュメント管理機能を使用して、Microsoft Excel でビジネス ドキュメント テンプレートに新しいフィールドを追加する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8c3a905c90f5dd4ad3487f004a958c0dcd52115d
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893250"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a><span data-ttu-id="cee94-103">Microsoft Excel のビジネス ドキュメント テンプレートへの新しいフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="cee94-103">Add new fields to a business document template in Microsoft Excel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cee94-104">ビジネス ドキュメントを Microsoft Excel 形式で生成するために使用されるテンプレートに新しいフィールドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="cee94-104">You can add new fields to a template that is used to generate business documents in Microsoft Excel format.</span></span> <span data-ttu-id="cee94-105">これらのフィールドを、生成されたドキュメントにアプリケーションの必要な情報を入力するために使用されるプレースホルダーとして追加できます。</span><span class="sxs-lookup"><span data-stu-id="cee94-105">These fields can be added as placeholders that are used to fill generated documents with required information from the application.</span></span> <span data-ttu-id="cee94-106">追加するすべてのフィールドに、データソースへのバインドを指定し、テンプレートを使用してビジネス ドキュメントを生成するときにフィールドに入力するアプリケーション データを指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="cee94-106">For every field that you add, you can also specify a binding to the data sources, to specify what application data will be entered in the field when the template is used to generate business documents.</span></span>

<span data-ttu-id="cee94-107">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="cee94-107">To learn more about this feature, complete the example in this topic.</span></span> <span data-ttu-id="cee94-108">この例では、テンプレートを更新して、生成された自由書式の請求書のフォームのフィールドに入力する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cee94-108">This example shows how to update a template to fill in the fields in free text invoice forms that are generated.</span></span>

## <a name="configure-business-document-management-to-edit-templates"></a><span data-ttu-id="cee94-109">テンプレートを編集するための、ビジネス ドキュメント管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="cee94-109">Configure Business document management to edit templates</span></span>

<span data-ttu-id="cee94-110">ビジネス ドキュメント管理 (BDM) は、[電子報告 (ER) の概要](general-electronic-reporting.md) フレームワークを基に構築されているため、BDM を使用して作業を開始できるようにするには、必要な ER パラメーターと BDM パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cee94-110">Because Business document management (BDM) is built on top of the [Electronic reporting (ER) overview](general-electronic-reporting.md) framework, you must configure the required ER and BDM parameters before you can start to work with BDM.</span></span>

1.  <span data-ttu-id="cee94-111">Microsoft Dynamics 365 Financeのインスタンスにシステム管理者としてサインインします。</span><span class="sxs-lookup"><span data-stu-id="cee94-111">Sign in to the instance of Microsoft Dynamics 365 Finance as the system administrator.</span></span>
2.  <span data-ttu-id="cee94-112">[ビジネス ドキュメント管理の概要](er-business-document-management.md) トピックの例の、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="cee94-112">Complete the following steps of the example in the [Business document management overview](er-business-document-management.md) topic:</span></span>

    1.  <span data-ttu-id="cee94-113">ER パラメーターのコンフィギュレーション。</span><span class="sxs-lookup"><span data-stu-id="cee94-113">Configure ER parameters.</span></span>
    2.  <span data-ttu-id="cee94-114">BDM 有効にします。</span><span class="sxs-lookup"><span data-stu-id="cee94-114">Turn on BDM.</span></span>

<span data-ttu-id="cee94-115">これで、BDM を使用して、ビジネス ドキュメント テンプレートを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="cee94-115">You can now start to use BDM to edit business document templates.</span></span>

## <a name="import-er-solutions-that-contain-a-template"></a><span data-ttu-id="cee94-116">テンプレートを含む ER ソリューションのインポート</span><span class="sxs-lookup"><span data-stu-id="cee94-116">Import ER solutions that contain a template</span></span>

<span data-ttu-id="cee94-117">この手順の例では、正式に公開された ER ソリューションを使用しています。</span><span class="sxs-lookup"><span data-stu-id="cee94-117">The example in this procedure uses the officially published ER solution.</span></span> <span data-ttu-id="cee94-118">このソリューションの ER コンフィギュレーションを Finance の現在のインスタンスにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cee94-118">You must import the ER configurations of this solution into your current instance of Finance.</span></span>

<span data-ttu-id="cee94-119">このソリューションの**自由書式の請求書 (Excel)** ER 形式コンフィギュレーションには、BDM を使用して編集できる Excel 形式のビジネス ドキュメント テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cee94-119">The **Free text invoice (Excel)** ER format configuration of this solution contains the business document template in Excel format that can be edited by using BDM.</span></span> <span data-ttu-id="cee94-120">この ER 形式コンフィギュレーションの最新バージョンを Microsoft Dynamics Lifecycle サービス (LCS) からインポートします。</span><span class="sxs-lookup"><span data-stu-id="cee94-120">Import the latest version of this ER format configuration from Microsoft Dynamics Lifecycle Service (LCS).</span></span> <span data-ttu-id="cee94-121">対応する ER データ モデルと ER モデル マッピングのコンフィギュレーションが自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="cee94-121">The corresponding ER data model and ER model mapping configurations will be imported automatically.</span></span>

<span data-ttu-id="cee94-122">ER コンフィギュレーションをインポートする方法の詳細については、[ER コンフィギュレーション ライフサイクルの管理](general-electronic-reporting-manage-configuration-lifecycle.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cee94-122">For more information about how to import ER configurations, see [Manage the ER configuration lifecycle](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![LCS 共有アセット ライブラリ ページ](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a><span data-ttu-id="cee94-124">ER ソリューションテンプレートの編集</span><span class="sxs-lookup"><span data-stu-id="cee94-124">Edit the ER solution template</span></span>

1.  <span data-ttu-id="cee94-125">**ビジネス ドキュメント管理**のワークスペースへのアクセス権を持つユーザーとして、ログインします。</span><span class="sxs-lookup"><span data-stu-id="cee94-125">Sign in as a user who has access to the **Business document management** workspace.</span></span>
2.  <span data-ttu-id="cee94-126">**ビジネス ドキュメント管理**のワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="cee94-126">Open the **Business document management** workspace.</span></span>

    ![ビジネス ドキュメント管理のワークスペース](./media/BDM-AddFldExcel-Workspace.png)

3.  <span data-ttu-id="cee94-128">グリッドで、**自由書式の請求書 (Excel)** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-128">In the grid, select the **Free text invoice (Excel)** template.</span></span>
4.  <span data-ttu-id="cee94-129">右ウィンドウで、**新しいテンプレート**を選択すると、選択したテンプレートに基づく新しいテンプレートが作成されます。</span><span class="sxs-lookup"><span data-stu-id="cee94-129">In the right pane, select **New template** to create a new template that is based on the selected template.</span></span>
5.  <span data-ttu-id="cee94-130">**タイトル**フィールドに、新しいテンプレートのタイトルとして**自由書式の請求書 (Excel) Contoso** を入力します。</span><span class="sxs-lookup"><span data-stu-id="cee94-130">In the **Title** field, enter **Free text invoice (Excel) Contoso** as the title of the new template.</span></span>
6.  <span data-ttu-id="cee94-131">**OK** を選択して、編集プロセスの開始を確認します。</span><span class="sxs-lookup"><span data-stu-id="cee94-131">Select **OK** to confirm the start of the editing process.</span></span>

<span data-ttu-id="cee94-132">BDM テンプレートのエディターページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cee94-132">The BDM template editor page appears.</span></span> <span data-ttu-id="cee94-133">Microsoft 365 を使用して、選択したテンプレートを埋め込みコントロールでオンラインで編集できます。</span><span class="sxs-lookup"><span data-stu-id="cee94-133">You can use Microsoft 365 to edit the selected template online in the embedded control.</span></span>

![BDM テンプレートのエディター ページ](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a><span data-ttu-id="cee94-135">テンプレートに新しいフィールドのラベルを追加する</span><span class="sxs-lookup"><span data-stu-id="cee94-135">Add the label for a new field to the template</span></span>

1.  <span data-ttu-id="cee94-136">BDM テンプレート エディター ページの Excel リボンの**表示**タブで、編集可能な Excel テンプレートの**ヘッダーとグリッド線**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="cee94-136">On the BDM template editor page, on the Excel ribbon, on the **View** tab, select the **Headings and Gridlines** check boxes for the editable Excel template.</span></span>

    ![ヘッダーとグリッド線チェック ボックスをオンにする](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  <span data-ttu-id="cee94-138">セル **E8: F8** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-138">Select cells **E8:F8**.</span></span>
3.  <span data-ttu-id="cee94-139">Excel リボンの**ホーム**タブで、**結合して中央揃え**を選択して、選択したセルを新しい結合されたセル **E8: F8** に結合します。</span><span class="sxs-lookup"><span data-stu-id="cee94-139">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **E8:F8** cell.</span></span>
4.  <span data-ttu-id="cee94-140">結合されたセル **E8: F8** に、**URL** を入力します。</span><span class="sxs-lookup"><span data-stu-id="cee94-140">In the merged cell **E8:F8**, enter **URL**.</span></span>
5.  <span data-ttu-id="cee94-141">結合されたセル **E7:F7** を選択し、**書式のコピー/貼り付け**を選択して、結合されたセル **E8: F8** を選択して結合されたセル **E7:F7** と同じように書式設定します。</span><span class="sxs-lookup"><span data-stu-id="cee94-141">Select merged cell **E7:F7**, select **Format painter**, and then select merged cell **E8:F8** to format it in the same way as merged cell **E7:F7**.</span></span>

    ![テンプレートに追加する新しいフィールド ラベル](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a><span data-ttu-id="cee94-143">新しいフィールドのスペースを確保するテンプレートの書式設定</span><span class="sxs-lookup"><span data-stu-id="cee94-143">Format the template to reserve space for a new field</span></span>

1.  <span data-ttu-id="cee94-144">BDM テンプレート エディター ページで、結合されたセル **G8 H8** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-144">On the BDM template editor page, select merged cell **G8:H8**.</span></span>
2.  <span data-ttu-id="cee94-145">Excel リボンの**ホーム**タブで、**結合して中央揃え**を選択して、選択したセルを新しい結合されたセル **G8: H8** に結合します。</span><span class="sxs-lookup"><span data-stu-id="cee94-145">On the Excel ribbon, on the **Home** tab, select **Merge & Center** to merge the selected cells into a new merged **G8:H8** cell.</span></span>
3.  <span data-ttu-id="cee94-146">結合されたセル **G7:H7** を選択し、**書式のコピー/貼り付け**を選択して、結合されたセル **G8:H8** を選択して結合されたセル **G7:H7** と同じように書式設定します。</span><span class="sxs-lookup"><span data-stu-id="cee94-146">Select merged cell **G7:H7**, select **Format painter**, and then select merged cell **G8:H8** to format it in the same way as merged cell **G7:H7**.</span></span>

    ![新しいフィールド用に確保されたスペース](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  <span data-ttu-id="cee94-148">**名前**ボックス フィールドで **CompanyInfo** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-148">In the **Name** box field, select **CompanyInfo**.</span></span>

    <span data-ttu-id="cee94-149">現在の Excel テンプレートの **CompanyInfo** の範囲には、生成されたレポートのヘッダーに、販売者として現在の会社の詳細を記入するために使用するすべてのフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cee94-149">The **CompanyInfo** range of the current Excel template holds all the fields that are used to fill the header of a generated report with the details of the current company as a seller party.</span></span>

    ![選択された CompanyInfo の範囲](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a><span data-ttu-id="cee94-151">テンプレートに新しいフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="cee94-151">Add a new field to the template</span></span>

1.  <span data-ttu-id="cee94-152">**BDM テンプレート エディター** ページのアクション ウィンドウで、**形式の表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-152">On the **BDM template editor** page, on the Action Pane, select **Show format**.</span></span>
2.  <span data-ttu-id="cee94-153">**テンプレート構造**ウィンドウで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-153">In the **Template structure** pane, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cee94-154">新しいフィールドとして使用するテンプレートのセクションを調整する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cee94-154">You must adjust the section of the template that you want to use as a new field.</span></span> <span data-ttu-id="cee94-155">この調整は、結合されたセル **G8: H8** をフォーマットすることによって既に行われています。</span><span class="sxs-lookup"><span data-stu-id="cee94-155">You already made this adjustment by formatting merged cell **G8:H8**.</span></span>

    ![テンプレートに新しいフィールドを追加する](./media/BDM-AddFldExcel-AddCell.png)

3.  <span data-ttu-id="cee94-157">テンプレートにセルとして新しいフィールドを追加するには、**Excel\Cell** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-157">Select **Excel\Cell** to add a new field as a cell in the template.</span></span>

    <span data-ttu-id="cee94-158">テンプレートに新しい範囲を追加する場合は、**Excel\Range** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="cee94-158">You can select **Excel\Range** if you want to add a new range to the template.</span></span> <span data-ttu-id="cee94-159">入力される範囲には、複数のセルを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="cee94-159">The range that is entered can contain multiple cells.</span></span> <span data-ttu-id="cee94-160">これらのセルは、後で追加できます。</span><span class="sxs-lookup"><span data-stu-id="cee94-160">You can add these cells later.</span></span>
    
    <span data-ttu-id="cee94-161">追加するフィールドの現在のテンプレート構造に最も適した親コンポーネントであるため、**CompanyInfo** テンプレート コンポーネントが、**テンプレート構造**ウィンドウで自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="cee94-161">Notice that the **CompanyInfo** template component, is automatically selected in the **Template structure** pane, because it's the most suitable parent component in the current template structure for the field that you're adding.</span></span>
    
4.  <span data-ttu-id="cee94-162">**Excel の範囲** フィールドに、**CompanyURL_Value** を入力します。</span><span class="sxs-lookup"><span data-stu-id="cee94-162">In the **Excel range** field, enter **CompanyURL_Value**.</span></span>
5.  <span data-ttu-id="cee94-163">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-163">Select **OK**.</span></span>

    ![テンプレート構造に追加された CompanyURL_Value フィールド](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  <span data-ttu-id="cee94-165">**テンプレート構造**ウィンドウで、省略符号ボタン (...) を選択し、**バインディングの表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-165">In the **Template structure** pane, select the ellipsis button (...), and then select **Show bindings**.</span></span>

    ![選択されたバインディングの表示](./media/BDM-AddFldExcel-ShowBindings.png)

    <span data-ttu-id="cee94-167">**テンプレート構造**ウィンドウに、基になる ER 形式で使用できるデータ ソースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="cee94-167">The **Template structure** pane now shows the data sources that are available in the underlying ER format.</span></span>

7.  <span data-ttu-id="cee94-168">基になる ER 形式のデータ ソースに連結する予定のフィールドとして **CompanyInfo_Value** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-168">Select **CompanyInfo_Value** as the field that you plan to bind to a data source of the underlying ER format.</span></span>
8.  <span data-ttu-id="cee94-169">**テンプレート構造**ウィンドウの**データ ソース** セクションで、**モデル \> InvoiceBase \> CompanyInfo** を展開します。</span><span class="sxs-lookup"><span data-stu-id="cee94-169">In the **Data sources** section of the **Template structure** pane, expand **Model \> InvoiceBase \> CompanyInfo**.</span></span>
9.  <span data-ttu-id="cee94-170">**CompanyInfo** で、**WebsiteURI** 項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-170">Under **CompanyInfo**, select the **WebsiteURI** item.</span></span>

    ![選択された WebsiteURI](./media/BDM-AddFldExcel-BindURL.png)

10. <span data-ttu-id="cee94-172">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-172">Select **Bind**.</span></span>
11. <span data-ttu-id="cee94-173">**テンプレート構造**ウィンドウで、**保存**をクリックし、BDM テンプレート エディター ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cee94-173">In the **Template structure** pane, select **Save**, and then close the BDM template editor page.</span></span>

<span data-ttu-id="cee94-174">**ビジネス ドキュメント管理**ワークスペースでは、更新されたテンプレートが右ウィンドウの**テンプレート** タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cee94-174">In the **Business document management** workspace, the **Template** tab in the right pane shows the updated template.</span></span> <span data-ttu-id="cee94-175">グリッドで、編集したテンプレートの**ステータス** フィールドが**下書き**に変更され、**リビジョン** フィールドが空白でなくなっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cee94-175">In the grid, notice that the **Status** field for the edited template has been changed to **Draft**, and the **Revision** field is no longer blank.</span></span> <span data-ttu-id="cee94-176">これらの変更は、このテンプレートの編集のプロセスが開始されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="cee94-176">These changes indicate that the process of editing this template has been started.</span></span>

![ビジネス ドキュメント管理ワークスペースで編集されたテンプレート](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a><span data-ttu-id="cee94-178">会社設定の確認</span><span class="sxs-lookup"><span data-stu-id="cee94-178">Review company settings</span></span>

1.  <span data-ttu-id="cee94-179">**組織管理 \> 組織 \> 法人**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cee94-179">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>
2.  <span data-ttu-id="cee94-180">**連絡先情報**クイック タブに、会社 URL が入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="cee94-180">On the **Contact information** FastTab, verify that the company URL is entered.</span></span>

![法人ページに入力された会社 URL](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a><span data-ttu-id="cee94-182">更新されたテンプレートをテストするためのビジネス ドキュメントの生成</span><span class="sxs-lookup"><span data-stu-id="cee94-182">Generate business documents to test the updated template</span></span>

1.  <span data-ttu-id="cee94-183">アプリケーションで、会社を **USMF** に変更し、**売掛金勘定 \> 請求書 \> すべての自由書式の請求書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="cee94-183">In the application, change the company to **USMF**, and go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2.  <span data-ttu-id="cee94-184">請求書 **FTI-00000002** を選択し、**印刷管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-184">Select invoice **FTI-00000002**, and then select **Print management**.</span></span>
3.  <span data-ttu-id="cee94-185">左ウィンドウで、**モジュール - 売掛金勘定 \> ドキュメント \> 自由書式の請求書**を展開します。</span><span class="sxs-lookup"><span data-stu-id="cee94-185">In the left pane, expand **Module - accounts receivable \> Documents \> Free text invoice**.</span></span>
4.  <span data-ttu-id="cee94-186">**自由書式の請求書**で、**元のドキュメント** レベルを選択して、処理する請求書の範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="cee94-186">Under **Free text invoice**, select the **Original document** level to specify the scope of invoices for processing.</span></span>
5.  <span data-ttu-id="cee94-187">右ウィンドウの、**レポート形式**フィールドで、指定されたドキュメント レベルの**自由書式の請求書 (Excel) Contoso** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-187">In the right pane, in the **Report format** field, select the **Free text invoice (Excel) Contoso** template for the specified document level.</span></span>

    ![選択した自由書式の請求書 (Excel) Contoso テンプレート](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  <span data-ttu-id="cee94-189">**Esc** を押して、現在のページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cee94-189">Press **Esc** to close the current page.</span></span>
7.  <span data-ttu-id="cee94-190">**印刷 \> 選択済**を選択します。</span><span class="sxs-lookup"><span data-stu-id="cee94-190">Select **Print \> Selected**.</span></span>
8.  <span data-ttu-id="cee94-191">生成されたドキュメントをダウンロードして、Excel で開きます。</span><span class="sxs-lookup"><span data-stu-id="cee94-191">Download the generated document, and open it in Excel.</span></span>

    ![Excel の自由書式の請求書](./media/BDM-AddFldExcel-PreviewReport.png)

<span data-ttu-id="cee94-193">変更したテンプレートは、選択した品目に対して自由書式の請求書レポートを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cee94-193">The modified template is used to generate the free text invoice report for the selected item.</span></span> <span data-ttu-id="cee94-194">テンプレートに加えた変更によってこのレポートがどのように影響を受けるかを分析するには、別のアプリケーション セッションでテンプレートを変更した直後に、1 つのアプリケーション セッションでこのレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="cee94-194">To analyze how this report is affected by changes that you make to the template, run the report in one application session immediately after you change the template in another application session.</span></span>

## <a name="related-links"></a><span data-ttu-id="cee94-195">関連リンク</span><span class="sxs-lookup"><span data-stu-id="cee94-195">Related links</span></span>

[<span data-ttu-id="cee94-196">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="cee94-196">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="cee94-197">ビジネス ドキュメント管理の概要</span><span class="sxs-lookup"><span data-stu-id="cee94-197">Business document management overview</span></span>](er-business-document-management.md)

[<span data-ttu-id="cee94-198">OPENXML 形式のレポートを生成するコンフィギュレーションを設計する</span><span class="sxs-lookup"><span data-stu-id="cee94-198">Design a configuration for generating reports in OPENXML format</span></span>](tasks/er-design-reports-openxml-2016-11.md)

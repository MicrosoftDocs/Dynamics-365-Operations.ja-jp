---
title: Microsoft Office スタイルのビジネス ドキュメント管理ユーザー インターフェイス
description: このトピックでは、電子申告 (ER) フレームワークにおけるビジネス ドキュメント管理機能の新しいユーザー インターフェイスを使用する方法について説明します。
author: v-anamir
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e6c5081f71a18dfac83b7aea950395436b42f50e
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881039"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a><span data-ttu-id="6d413-103">Microsoft Office スタイルのビジネス ドキュメント管理ユーザー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6d413-103">Microsoft Office-style user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d413-104">ビジネス ドキュメント管理により、ビジネス ユーザーは Microsoft 365 サービスまたは適切な Microsoft Office デスクトップ アプリケーションを使用して、ビジネス ドキュメント テンプレートを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="6d413-105">編集にはデザインの変更や新しい配置が含まれ、、ユーザーが追加のデータを含めるためのプレースホルダーを追加するのにソース コードを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6d413-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="6d413-106">ビジネス ドキュメント管理の使用方法の詳細については、[ビジネス ドキュメント管理の概要](er-business-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d413-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="6d413-107">新しいユーザー インターフェイス (UI) は、より明確で使いやすくなっています。</span><span class="sxs-lookup"><span data-stu-id="6d413-107">The new user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="6d413-108">**ビジネス ドキュメント** エリアには、現在のプロバイダーに対して使用可能なテンプレートのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-108">The **Business document** area shows only the templates that are available for the current provider.</span></span> <span data-ttu-id="6d413-109">以前の UI では、**テンプレート** タブには、任意のプロバイダーに使用できるテンプレートが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="6d413-109">In the previous UI, the **Template** tab listed all the templates that were available for any providers.</span></span> <span data-ttu-id="6d413-110">また、同じロールを持つユーザーが作成および編集したテンプレートもすべて表示されています。</span><span class="sxs-lookup"><span data-stu-id="6d413-110">It also showed all the templates that were created and edited by any user who had the same role.</span></span>

<span data-ttu-id="6d413-111">**新しいドキュメント** ボタンを使用して、別のプロバイダーによって提供される電子申告 (ER) 形式コンフィギュレーションのテンプレートの作成および編集ができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-111">You can use the **New document** button to create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="6d413-112">このトピックの例において、プロバイダーは Microsoft です。</span><span class="sxs-lookup"><span data-stu-id="6d413-112">In the example in this topic, the provider is Microsoft.</span></span> <span data-ttu-id="6d413-113">また、Excel 形式の独自のテンプレートをアップロードしてテンプレートを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d413-113">Alternatively, you can create a template by uploading your own template in Excel format.</span></span>


> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RWAVQg]

<span data-ttu-id="6d413-114">[ビジネス ドキュメントの管理を使用して新しいビジネス ドキュメントを作成する](https://youtu.be/gAIYl-mM_pw) のビデオ (上記) は、YouTube で視聴可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d413-114">The [Create a new business document using Business document management](https://youtu.be/gAIYl-mM_pw) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="6d413-115">ビジネス ドキュメント管理の新しいドキュメント UI を有効にする</span><span class="sxs-lookup"><span data-stu-id="6d413-115">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="6d413-116">ビジネス ドキュメント管理の新しいドキュメント UI の使用を開始するには、**機能管理** ワークスペースで、**ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d413-116">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="6d413-117">すべての法人に対してこの機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6d413-117">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="6d413-118">**機能管理** ワークスペースの **すべて** タブで、リスト内の **ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d413-118">In the **Feature management** workspace, on the **All** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="6d413-119">**直ちに有効化** を選択し、選択した機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="6d413-119">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="6d413-120">ページを更新して、新しい機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="6d413-120">Refresh the page to access the new feature.</span></span>

## <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="6d413-121">他のプロバイダーが所有するテンプレートを編集</span><span class="sxs-lookup"><span data-stu-id="6d413-121">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="6d413-122">**ビジネス ドキュメント管理** ワークスペースで、**新規ドキュメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d413-122">In the **Business document management** workspace, select **New document**.</span></span>

    ![ビジネス ドキュメント管理のワークスペース](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="6d413-124">**選択** タブでテンプレートとして使用するドキュメントを選択し、**ドキュメントの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d413-124">On the **Select** tab, select the document to use as a template, and then select **Create document**.</span></span>

    ![ビジネス ドキュメントのダイアログボックス](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="6d413-126">新規のダイアログボックスの **タイトル** フィールドで、必要に応じてタイトルを変更します。</span><span class="sxs-lookup"><span data-stu-id="6d413-126">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="6d413-127">このタイトル テキストは、自動的に作成される新しい ER 形式コンフィギュレーションに名前を付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-127">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="6d413-128">このコンフィギュレーション (**顧客 FTI レポート (GER) コピー**) のドラフト バージョンには、編集したテンプレートが含まれ、現在のユーザーに対して ER 形式を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-128">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="6d413-129">他のすべてのユーザーは、基本 ER 形式コンフィギュレーションからの元のテンプレートを使用して、この ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="6d413-129">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="6d413-130">**名前** フィールドで、自動的に作成される編集可能なテンプレートの最初のリビジョンの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="6d413-130">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="6d413-131">**コメント** フィールドで、自動的に作成される編集可能なテンプレートのリビジョンの注釈を更新します。</span><span class="sxs-lookup"><span data-stu-id="6d413-131">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="6d413-132">**OK** を選択して、編集プロセスの開始を確認します。</span><span class="sxs-lookup"><span data-stu-id="6d413-132">Select **OK** to confirm the start of the editing process.</span></span>

    ![ドキュメント作成のダイアログボックス](./media/BDM_overview_new_template3.png)

<span data-ttu-id="6d413-134">**新規ドキュメント** ボタンは、ユーザーは別のプロバイダーによって提供される電子申告 (ER) 形式コンフィギュレーションのテンプレートの作成および編集のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-134">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="6d413-135">この例において、プロバイダーは Microsoft です。</span><span class="sxs-lookup"><span data-stu-id="6d413-135">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="6d413-136">**新規ドキュメント** を選択すると、現在のプロバイダーと他のプロバイダーが所有するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-136">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="6d413-137">テンプレートを選択すると、編集用に開かれます。</span><span class="sxs-lookup"><span data-stu-id="6d413-137">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="6d413-138">編集したテンプレートは、自動的に生成される新規 ER 形式コンフィギュレーションで保存されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-138">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

## <a name="upload-a-template-that-uses-an-existing-excel-format"></a><span data-ttu-id="6d413-139">既存の Excel 形式を使用するテンプレートのアップロード</span><span class="sxs-lookup"><span data-stu-id="6d413-139">Upload a template that uses an existing Excel format</span></span>
<span data-ttu-id="6d413-140">テンプレートをアップロードする前に、以下の手順に従って必要な情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d413-140">Follow these steps to provide required information before you upload a template.</span></span>

1. <span data-ttu-id="6d413-141">**ビジネス ドキュメント管理** ワークスペースで、**新規ドキュメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d413-141">In the **Business document management** workspace, select **New document**.</span></span>

    ![ビジネス ドキュメント管理のワークスペース](./media/BDM_overview_new_template1.png)
    
2. <span data-ttu-id="6d413-143">**新しいテンプレートを作成** ページの **アップロード** タブにある **テンプレート** タブで、**参照** を選択して、テンプレートとして使用する Excel ファイルの検索および選択をします。</span><span class="sxs-lookup"><span data-stu-id="6d413-143">On the **Create a new template** page, on the **Upload** tab, on the **Template** tab, select **Browse** to find and select the Excel file that you want to use as a template.</span></span> <span data-ttu-id="6d413-144">**テンプレート** セクションでは、**タイトル** および **説明** フィールドは自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-144">In the **Template** section, the **Title** and **Description** fields are automatically filled in.</span></span> <span data-ttu-id="6d413-145">自動的に作成される新しい ER 形式コンフィギュレーションの名前と説明を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d413-145">They specify the name and description of the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="6d413-146">必要に応じて、これらのフィールドを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-146">You can edit these fields as you require.</span></span>
3. <span data-ttu-id="6d413-147">**ドキュメント タイプ** セクションの **名前** フィールドで、ビジネス ドキュメントのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="6d413-147">In the **Document Type** section, in the **Name** field, specify the type of business document.</span></span> <span data-ttu-id="6d413-148">この値を使用して、正しいデータ ソース (つまり、ER モデル コンフィギュレーション) を検索します。</span><span class="sxs-lookup"><span data-stu-id="6d413-148">This value will be used to search the correct data source (that is, the ER model configuration).</span></span>

    ![テンプレート タブ](./media/BDM_overview_new_UI_import_21.jpg)

4. <span data-ttu-id="6d413-150">**データ ソース** タブの **フィルター** クイックタブで、**フィルターの適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d413-150">On the **Data source** tab, on the **Filter** FastTab, select **Apply filter**.</span></span> <span data-ttu-id="6d413-151">**データ ソース** セクションの **名前** フィールドは自動的に入力されるか、または手動で値を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-151">In the **Data source** section, the **Name** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="6d413-152">フィルターを使用し、名前、説明、国/地域コード、およびビジネス ドキュメントのタイプによって適切なデータ ソース名を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-152">You can use the filter to search for the appropriate data source name by name, description, country/region code, and business document type.</span></span>

    ![データ ソース タブ](./media/BDM_overview_new_UI_import_31.jpg)
    
    > [!NOTE]
    > <span data-ttu-id="6d413-154">**フィルター** クイックタブを使用して、正しいデータ ソース (つまり、ER モデル コンフィギュレーション) を検索します。</span><span class="sxs-lookup"><span data-stu-id="6d413-154">The **Filter** FastTab is used to search the correct data source (that is, the ER model configuration).</span></span> <span data-ttu-id="6d413-155">アップロードするドキュメントに最も適切なデータ ソースを検索するために、すべてのフィルター フィールドを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-155">You can edit all filter fields to find the most appropriate data source for the document that you're uploading.</span></span>
    > 
    > <span data-ttu-id="6d413-156">**フィルター** クイックタブの条件は、**OR** 条件として使用されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-156">The conditions on the **Filter** FastTab are used as **OR** conditions.</span></span>
    
5. <span data-ttu-id="6d413-157">**マッピング** タブで、**自動検出** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d413-157">On the **Mapping** tab, select **Auto detect**.</span></span> <span data-ttu-id="6d413-158">**ルート定義** フィールドは自動的に入力されるか、または手動で値を選択することができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-158">The **Root definition** field is automatically filled in, or you can manually select a value.</span></span> <span data-ttu-id="6d413-159">このタブには、テンプレートおよびモデルから要素のエンド マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d413-159">This tab shows the end mapping for the elements from the template and the model.</span></span>

    ![マッピング タブ](./media/BDM_overview_new_UI_import_41.jpg)
    
   > [!NOTE]
   > <span data-ttu-id="6d413-161">**テンプレート構造** セクションのマッピングでは、ユーザーの言語およびテンプレートのセル名におけるデータ ソースのラベルまたは説明の完全一致を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d413-161">The mapping in the **Template structure** section uses the full match of the labels or descriptions in the data source in the user's language, and in the cell name in the template.</span></span>

6. <span data-ttu-id="6d413-162">**ドキュメントの作成** を選択し、テンプレートの作成と編集プロセスの開始を確認します。</span><span class="sxs-lookup"><span data-stu-id="6d413-162">Select **Create document** to confirm that you want to create a template and start the editing process.</span></span>

<span data-ttu-id="6d413-163">詳細については、[ビジネス ドキュメント管理の概要](er-business-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d413-163">For more information, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="6d413-164">電子申告にプロバイダーがない場合、作成できます。</span><span class="sxs-lookup"><span data-stu-id="6d413-164">If there isn't a provider in Electronic reporting, you can create one.</span></span> <span data-ttu-id="6d413-165">有効なプロバイダーがない場合は、選択して有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="6d413-165">If there's no active provider, you can select to activate one.</span></span>

- <span data-ttu-id="6d413-166">プロバイダーを作成するには、**名前** フィールドでプロバイダーの名前を変更し、**インターネット アドレス** フィールドで新しいプロバイダーのインターネット アドレスを更新した後、**OK** を選択して確認します。</span><span class="sxs-lookup"><span data-stu-id="6d413-166">To create a provider, change the name of the provider in the **Name** field, update the internet address of the new provider in the **Internet address** field, and select **OK** to confirm.</span></span>

    ![BDM で新しいプロバイダーを作成する](./media/bdm_create_provider.png)
    
- <span data-ttu-id="6d413-168">既存のプロバイダーを有効にするには、**構成プロバイダー** フィールドでプロバイダーの名前を選択して **OK** を選択し、プロバイダーを有効に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d413-168">To activate existing provider, choose the name of the provider in the **Configuration provider** field, and select **OK** to set provider as active.</span></span>

    ![BDM でプロバイダーを有効化する](./media/bdm_choose_provider.png)

> [!NOTE]
> <span data-ttu-id="6d413-170">各 BDM テンプレートは、コンフィギュレーションの作成者としてプロバイダーを参照します。</span><span class="sxs-lookup"><span data-stu-id="6d413-170">Each BDM template refers to the provider as the author of the configuration.</span></span> <span data-ttu-id="6d413-171">そのため、テンプレートには有効なプロバイダーが必要です。</span><span class="sxs-lookup"><span data-stu-id="6d413-171">This is why an active provider is required for the template.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: (RCS) オプションの属性を使用して XML 形式のファイルをインポートする
description: このトピックでは、オプションの属性を含む XML 形式のファイルをインポートするため、ユーザーが ER 形式コンフィギュレーションをデザインする方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1290598d8dbd5b72d679ccf3e642e75b6dc3215
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182189"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="9317b-103">(RCS) オプションの属性を使用して XML 形式のファイルをインポートする</span><span class="sxs-lookup"><span data-stu-id="9317b-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9317b-104">次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションをデザインし、オプションの属性を含む XML 形式のファイルをインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9317b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="9317b-105">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9317b-105">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="9317b-106">始める前に、[Microsoft ダウンロードセンター](https://go.microsoft.com/fwlink/?linkid=874684) から IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ファイルをダウンロードし、ローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="9317b-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.  <span data-ttu-id="9317b-107">**すべてのワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9317b-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.  <span data-ttu-id="9317b-108">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9317b-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="9317b-109">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](er-configuration-provider-mark-it-active-2016-11.md)という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9317b-109">If you don’t see this configuration provider, complete the steps in the procedure [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.  <span data-ttu-id="9317b-110">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="9317b-111">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="9317b-111">Create a new data model configuration</span></span>
1.  <span data-ttu-id="9317b-112">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-112">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="9317b-113">**名前**フィールドに、「XML ファイルをインポートするモデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.  <span data-ttu-id="9317b-114">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-114">Click **Create configuration**.</span></span>
4.  <span data-ttu-id="9317b-115">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-115">Click **Designer**.</span></span>
5.  <span data-ttu-id="9317b-116">**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-116">Click **New** to open the drop dialog.</span></span>
6.  <span data-ttu-id="9317b-117">**名称**のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-117">In the **Name** field, type 'Root'.</span></span>
7.  <span data-ttu-id="9317b-118">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-118">Click **Add**.</span></span>
8.  <span data-ttu-id="9317b-119">**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-119">Click **New** to open the drop dialog.</span></span>
9.  <span data-ttu-id="9317b-120">**名称**のフィールドに、「リスト」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-120">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="9317b-121">**品目タイプ** フィールドで、**レコード リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-121">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="9317b-122">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-122">Click **Add**.</span></span>
12. <span data-ttu-id="9317b-123">**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-123">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="9317b-124">**名称**フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-124">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="9317b-125">**品目タイプ**フィールドで、**文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-125">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="9317b-126">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-126">Click **Add**.</span></span>
16. <span data-ttu-id="9317b-127">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-127">Click **Save**.</span></span>
17. <span data-ttu-id="9317b-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9317b-128">Close the page.</span></span>
18. <span data-ttu-id="9317b-129">**状態の変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-129">Click **Change status**.</span></span>
19. <span data-ttu-id="9317b-130">**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-130">Click **Complete**.</span></span>
20. <span data-ttu-id="9317b-131">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="9317b-132">データ インポート用の形式の作成</span><span class="sxs-lookup"><span data-stu-id="9317b-132">Create a format for data import</span></span>
1.  <span data-ttu-id="9317b-133">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-133">Click **Create configuration** to open the drop dialog.</span></span>
2.  <span data-ttu-id="9317b-134">**新規**フィールドで、「XML ファイルをインポートするモデルのデータ モデルに基づく形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.  <span data-ttu-id="9317b-135">**名前**フィールドに、'xml ファイルをインポートする形式' と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.  <span data-ttu-id="9317b-136">**データのインポートのサポート** フィールドで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-136">Select **Yes** in the **Supports data import** field.</span></span>
5.  <span data-ttu-id="9317b-137">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="9317b-138">XML 形式で受信するファイルを解析する形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="9317b-138">Design a format to parse incoming file in xml format</span></span>
1.  <span data-ttu-id="9317b-139">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-139">Click **Designer**.</span></span>
2.  <span data-ttu-id="9317b-140">**ルートの追加**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-140">Click **Add root** to open the drop dialog.</span></span>
3.  <span data-ttu-id="9317b-141">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-141">In the tree, select **XML\Element**.</span></span>
4.  <span data-ttu-id="9317b-142">**名称**のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-142">In the **Name** field, type 'root'.</span></span>
5.  <span data-ttu-id="9317b-143">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-143">Click **OK**.</span></span>
6.  <span data-ttu-id="9317b-144">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-144">Click **Add** to open the drop dialog.</span></span>
7.  <span data-ttu-id="9317b-145">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-145">In the tree, select **XML\Element**.</span></span>
8.  <span data-ttu-id="9317b-146">**名前**フィールドに、「ドキュメント」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-146">In the **Name** field, type 'document'.</span></span>
9.  <span data-ttu-id="9317b-147">**多様性**フィールドで、**1 つ、多数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-147">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="9317b-148">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-148">Click **OK**.</span></span>
11. <span data-ttu-id="9317b-149">ツリーで、**root\document** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-149">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="9317b-150">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="9317b-150">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="9317b-151">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-151">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="9317b-152">**名前**フィールドに、'ID' と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-152">In the **Name** field, type 'ID'.</span></span>
15. <span data-ttu-id="9317b-153">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-153">Click **OK**.</span></span>
16. <span data-ttu-id="9317b-154">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="9317b-155">解析された情報をデータ モデルに保存する形式マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="9317b-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="9317b-156">**形式をモデルにマップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="9317b-157">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-157">Click **New**.</span></span>
3. <span data-ttu-id="9317b-158">**定義**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="9317b-159">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9317b-160">**名前**フィールドに、「マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="9317b-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="9317b-161">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-161">Click **Save**.</span></span>
7. <span data-ttu-id="9317b-162">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-162">Click **Designer**.</span></span>
8. <span data-ttu-id="9317b-163">ツリーで、**形式**を展開します。</span><span class="sxs-lookup"><span data-stu-id="9317b-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="9317b-164">ツリーで、**format\root: XML Element(root)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="9317b-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10. <span data-ttu-id="9317b-165">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="9317b-166">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="9317b-166">(document)\*\*.</span></span>
11. <span data-ttu-id="9317b-167">**バインド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-167">Click **Bind**.</span></span>
12. <span data-ttu-id="9317b-168">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を展開します。</span><span class="sxs-lookup"><span data-stu-id="9317b-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="9317b-169">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="9317b-169">(document)\*\*.</span></span>
13. <span data-ttu-id="9317b-170">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="9317b-171">(ドキュメント)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="9317b-171">(document)\id\*\*.</span></span>
14. <span data-ttu-id="9317b-172">ツリーで、**List = format.root.document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="9317b-172">In the tree, expand **List = format.root.document**.</span></span>
15. <span data-ttu-id="9317b-173">ツリーで、**List = format.root.document\Code** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-173">In the tree, select **List = format.root.document\Code**.</span></span>
16. <span data-ttu-id="9317b-174">**バインド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-174">Click **Bind**.</span></span>
17. <span data-ttu-id="9317b-175">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-175">Click **Save**.</span></span>
18. <span data-ttu-id="9317b-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9317b-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="9317b-177">形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="9317b-177">Run format mapping</span></span>
1. <span data-ttu-id="9317b-178">**実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-178">Click **Run**.</span></span>
2. <span data-ttu-id="9317b-179">**参照**をクリックし、**IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="9317b-180">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9317b-181">選択したファイルは、「document」要素に「ID」属性が存在するように想定した形式デザインとしてインポートされませんでしたが、インポートされたファイルにそのような属性は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="9317b-181">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="9317b-182">XML 属性をオプションとして処理するよう形式構造を変更</span><span class="sxs-lookup"><span data-stu-id="9317b-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="9317b-183">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9317b-183">Close the page.</span></span>
2. <span data-ttu-id="9317b-184">ツリーで、**root\document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="9317b-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="9317b-185">ツリーで、**root\document\id** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="9317b-186">**存在しない属性に対する空の文字列**フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="9317b-187">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="9317b-188">変更をテストするための形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="9317b-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="9317b-189">**形式をモデルにマップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="9317b-190">**実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-190">Click **Run**.</span></span>
3. <span data-ttu-id="9317b-191">**参照**をクリックし、**IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9317b-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="9317b-192">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9317b-192">Click **OK**.</span></span>
5. <span data-ttu-id="9317b-193">生成したファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="9317b-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="9317b-194">同じファイルがフォーマット デザインとしてインポートされて、‘document’要素の‘ID’属性はオプションとして見なされます。</span><span class="sxs-lookup"><span data-stu-id="9317b-194">The same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>

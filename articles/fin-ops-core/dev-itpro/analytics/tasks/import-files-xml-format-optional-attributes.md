---
title: (RCS) オプションの属性を使用して XML 形式のファイルをインポートする
description: このトピックでは、オプションの属性を含む XML 形式のファイルをインポートするため、ユーザーが ER 形式コンフィギュレーションをデザインする方法を説明します。
author: NickSelin
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25ced72bc1bb1b18996c8bab986270fde0557ed3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744870"
---
# <a name="rcs-import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="86222-103">(RCS) オプションの属性を使用して XML 形式のファイルをインポートする</span><span class="sxs-lookup"><span data-stu-id="86222-103">(RCS) Import files in XML format with optional attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="86222-104">次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションをデザインし、オプションの属性を含む XML 形式のファイルをインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="86222-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="86222-105">この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86222-105">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span> <span data-ttu-id="86222-106">始める前に、[Microsoft ダウンロードセンター](https://go.microsoft.com/fwlink/?linkid=874684) から IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ファイルをダウンロードし、ローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="86222-106">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

1.    <span data-ttu-id="86222-107">**すべてのワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="86222-107">Go to **All workspaces** > **Electronic reporting**.</span></span>
2.    <span data-ttu-id="86222-108">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="86222-108">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="86222-109">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86222-109">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3.    <span data-ttu-id="86222-110">**コンフィギュレーションをレポートする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-110">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="86222-111">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="86222-111">Create a new data model configuration</span></span>
1.    <span data-ttu-id="86222-112">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-112">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="86222-113">**名前** フィールドに、「XML ファイルをインポートするモデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-113">In the **Name** field, type 'Model to import xml file'.</span></span>
3.    <span data-ttu-id="86222-114">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-114">Click **Create configuration**.</span></span>
4.    <span data-ttu-id="86222-115">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-115">Click **Designer**.</span></span>
5.    <span data-ttu-id="86222-116">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-116">Click **New** to open the drop dialog.</span></span>
6.    <span data-ttu-id="86222-117">**名称** のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-117">In the **Name** field, type 'Root'.</span></span>
7.    <span data-ttu-id="86222-118">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-118">Click **Add**.</span></span>
8.    <span data-ttu-id="86222-119">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-119">Click **New** to open the drop dialog.</span></span>
9.    <span data-ttu-id="86222-120">**名称** のフィールドに、「リスト」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-120">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="86222-121">**品目タイプ** フィールドで、**レコード リスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-121">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="86222-122">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-122">Click **Add**.</span></span>
12.    <span data-ttu-id="86222-123">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-123">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="86222-124">**名称** フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-124">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="86222-125">**品目タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-125">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="86222-126">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-126">Click **Add**.</span></span>
16.    <span data-ttu-id="86222-127">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-127">Click **Save**.</span></span>
17.    <span data-ttu-id="86222-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86222-128">Close the page.</span></span>
18.    <span data-ttu-id="86222-129">**状態の変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-129">Click **Change status**.</span></span>
19.    <span data-ttu-id="86222-130">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-130">Click **Complete**.</span></span>
20.    <span data-ttu-id="86222-131">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-131">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="86222-132">データ インポート用の形式の作成</span><span class="sxs-lookup"><span data-stu-id="86222-132">Create a format for data import</span></span>
1.    <span data-ttu-id="86222-133">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-133">Click **Create configuration** to open the drop dialog.</span></span>
2.    <span data-ttu-id="86222-134">**新規** フィールドで、「XML ファイルをインポートするモデルのデータ モデルに基づく形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-134">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3.    <span data-ttu-id="86222-135">**名前** フィールドに、'xml ファイルをインポートする形式' と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-135">In the **Name** field, type 'Format to import xml file'.</span></span>
4.    <span data-ttu-id="86222-136">**データのインポートのサポート** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-136">Select **Yes** in the **Supports data import** field.</span></span>
5.    <span data-ttu-id="86222-137">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-137">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="86222-138">XML 形式で受信するファイルを解析する形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="86222-138">Design a format to parse incoming file in xml format</span></span>
1.    <span data-ttu-id="86222-139">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-139">Click **Designer**.</span></span>
2.    <span data-ttu-id="86222-140">**ルートの追加** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-140">Click **Add root** to open the drop dialog.</span></span>
3.    <span data-ttu-id="86222-141">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-141">In the tree, select **XML\Element**.</span></span>
4.    <span data-ttu-id="86222-142">**名称** のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-142">In the **Name** field, type 'root'.</span></span>
5.    <span data-ttu-id="86222-143">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-143">Click **OK**.</span></span>
6.    <span data-ttu-id="86222-144">**追加** をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-144">Click **Add** to open the drop dialog.</span></span>
7.    <span data-ttu-id="86222-145">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-145">In the tree, select **XML\Element**.</span></span>
8.    <span data-ttu-id="86222-146">**名前** フィールドに、「ドキュメント」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-146">In the **Name** field, type 'document'.</span></span>
9.    <span data-ttu-id="86222-147">**多様性** フィールドで、**1 つ、多数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-147">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="86222-148">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-148">Click **OK**.</span></span>
11.    <span data-ttu-id="86222-149">ツリーで、**root\document** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-149">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="86222-150">**追加** をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="86222-150">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="86222-151">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-151">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="86222-152">**名前** フィールドに、'ID' と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-152">In the **Name** field, type 'ID'.</span></span>
15.    <span data-ttu-id="86222-153">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-153">Click **OK**.</span></span>
16.    <span data-ttu-id="86222-154">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-154">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="86222-155">解析された情報をデータ モデルに保存する形式マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="86222-155">Design a format mapping to save parsed information to data model</span></span>
1. <span data-ttu-id="86222-156">**形式をモデルにマップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-156">Click **Map format to model**.</span></span>
2. <span data-ttu-id="86222-157">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-157">Click **New**.</span></span>
3. <span data-ttu-id="86222-158">**定義** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-158">In the **Definition** field, enter or select a value.</span></span>
4. <span data-ttu-id="86222-159">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-159">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="86222-160">**名前** フィールドに、「マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="86222-160">In the **Name** field, type 'Mapping'.</span></span>
6. <span data-ttu-id="86222-161">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-161">Click **Save**.</span></span>
7. <span data-ttu-id="86222-162">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-162">Click **Designer**.</span></span>
8. <span data-ttu-id="86222-163">ツリーで、**形式** を展開します。</span><span class="sxs-lookup"><span data-stu-id="86222-163">In the tree, expand **format**.</span></span>
9. <span data-ttu-id="86222-164">ツリーで、**format\root: XML Element(root)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="86222-164">In the tree, expand **format\root: XML Element(root)**.</span></span>
10.    <span data-ttu-id="86222-165">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-165">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="86222-166">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="86222-166">(document)\*\*.</span></span>
11.    <span data-ttu-id="86222-167">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-167">Click **Bind**.</span></span>
12.    <span data-ttu-id="86222-168">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を展開します。</span><span class="sxs-lookup"><span data-stu-id="86222-168">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="86222-169">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="86222-169">(document)\*\*.</span></span>
13.    <span data-ttu-id="86222-170">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-170">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="86222-171">(ドキュメント)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="86222-171">(document)\id\*\*.</span></span>
14.    <span data-ttu-id="86222-172">ツリーで、**List = format.root.document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="86222-172">In the tree, expand **List = format.root.document**.</span></span>
15.    <span data-ttu-id="86222-173">ツリーで、**List = format.root.document\Code** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-173">In the tree, select **List = format.root.document\Code**.</span></span>
16.    <span data-ttu-id="86222-174">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-174">Click **Bind**.</span></span>
17.    <span data-ttu-id="86222-175">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-175">Click **Save**.</span></span>
18.    <span data-ttu-id="86222-176">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86222-176">Close the page.</span></span>
 
## <a name="run-format-mapping"></a><span data-ttu-id="86222-177">形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="86222-177">Run format mapping</span></span>
1. <span data-ttu-id="86222-178">**実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-178">Click **Run**.</span></span>
2. <span data-ttu-id="86222-179">**参照** をクリックし、**IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-179">Click **Browse** and select **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="86222-180">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-180">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="86222-181">選択したファイルは、「document」要素に「ID」属性が存在するように想定した形式デザインとしてインポートされませんでしたが、インポートされたファイルにそのような属性は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="86222-181">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="86222-182">XML 属性をオプションとして処理するよう形式構造を変更</span><span class="sxs-lookup"><span data-stu-id="86222-182">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="86222-183">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="86222-183">Close the page.</span></span>
2. <span data-ttu-id="86222-184">ツリーで、**root\document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="86222-184">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="86222-185">ツリーで、**root\document\id** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-185">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="86222-186">**存在しない属性に対する空の文字列** フィールドで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-186">Select **Yes** in the **Empty string for missing attribute** field.</span></span>
5. <span data-ttu-id="86222-187">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-187">Click **Save**.</span></span>
 
## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="86222-188">変更をテストするための形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="86222-188">Run format mapping to test changes</span></span>
1. <span data-ttu-id="86222-189">**形式をモデルにマップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-189">Click **Map format to model**.</span></span>
2. <span data-ttu-id="86222-190">**実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-190">Click **Run**.</span></span>
3. <span data-ttu-id="86222-191">**参照** をクリックし、**IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="86222-191">Click **Browse** and select the **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** file.</span></span>
4. <span data-ttu-id="86222-192">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="86222-192">Click **OK**.</span></span>
5. <span data-ttu-id="86222-193">生成したファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="86222-193">Review the generated file.</span></span> 

> [!NOTE]
> <span data-ttu-id="86222-194">同じファイルがフォーマット デザインとしてインポートされて、‘document’ 要素の ‘ID’ 属性はオプションとして見なされます。</span><span class="sxs-lookup"><span data-stu-id="86222-194">The same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
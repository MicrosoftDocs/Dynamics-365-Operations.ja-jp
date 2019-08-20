---
title: オプションの属性を使用して XML 形式でファイルをインポートする
description: このトピックでは、XML 形式で受信する電子ドキュメントを解析するために XML 属性を指定する ER 形式のデザインについて説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb5d721784f45097ab466f75d43256495aac36ca
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849998"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="626d0-103">オプションの属性を使用して XML 形式でファイルをインポートする</span><span class="sxs-lookup"><span data-stu-id="626d0-103">Import files in XML format with optional attributes</span></span>

<span data-ttu-id="626d0-104">XML 形式で受信する電子ドキュメントを解析するための電子申告 (ER) 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="626d0-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="626d0-105">XML 要素の特定の属性は、デザインされた ER 形式でオプションとして指定することができます。</span><span class="sxs-lookup"><span data-stu-id="626d0-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="626d0-106">これにより、該当する XML 属性のある受信ファイルとない受信ファイルを正しく処理することができます。</span><span class="sxs-lookup"><span data-stu-id="626d0-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="626d0-107">その後、アプリケーションのデータを更新するのに、これらのファイルからの内容を使用できます。</span><span class="sxs-lookup"><span data-stu-id="626d0-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="626d0-108">この機能の詳細を知るには、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部である [RCS オプションの属性を使用して XML 形式のファイルをインポートする](tasks/import-files-xml-format-optional-attributes.md) トピックの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="626d0-108">To learn more about this feature, complete the steps in the topic, [RCS Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="626d0-109">このタスク ガイドおよび関連するサンプル ファイは [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="626d0-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="626d0-110">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="626d0-110">Content description</span></span>       | <span data-ttu-id="626d0-111">ファイル</span><span class="sxs-lookup"><span data-stu-id="626d0-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="626d0-112">XML 形式のサンプル ファイル</span><span class="sxs-lookup"><span data-stu-id="626d0-112">Sample file in XML format</span></span> | <span data-ttu-id="626d0-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="626d0-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="626d0-114">タスク ガイド</span><span class="sxs-lookup"><span data-stu-id="626d0-114">Task guide</span></span>                | <span data-ttu-id="626d0-115">RCS オプションの attributes.axtr を使用して XML 形式のファイルをインポートする</span><span class="sxs-lookup"><span data-stu-id="626d0-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="626d0-116">次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションをデザインし、オプションの属性を含む XML 形式のファイルをインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="626d0-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="626d0-117">これらの手順を完了するには、まず手順の [コンフィギュレーションプロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) にある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="626d0-117">To complete these steps, you must first complete the steps in the procedure, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="626d0-118">始める前に、Microsoft ダウンロード センター (https://go.microsoft.com/fwlink/?linkid=874684) から IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ファイルをダウンロードし、ローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="626d0-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="626d0-119">**組織管理** > **ワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="626d0-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="626d0-120">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="626d0-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="626d0-121">この構成プロバイダーが表示されない場合は、[構成プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md) というトピックにある手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="626d0-121">If you don’t see this configuration provider, complete the steps in the topic, [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="626d0-122">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="626d0-123">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="626d0-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="626d0-124">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="626d0-125">**名前**フィールドに、「XML ファイルをインポートするモデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="626d0-126">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="626d0-127">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-127">Click **Designer**.</span></span>
5. <span data-ttu-id="626d0-128">**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="626d0-129">**名称**のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="626d0-130">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-130">Click **Add**.</span></span>
8. <span data-ttu-id="626d0-131">**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="626d0-132">**名称**のフィールドに、「リスト」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-132">In the **Name** field, type 'List'.</span></span>
10. <span data-ttu-id="626d0-133">**品目タイプ** フィールドで、**レコード リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-133">In the **Item type** field, select **Record list**.</span></span>
11. <span data-ttu-id="626d0-134">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-134">Click **Add**.</span></span>
12. <span data-ttu-id="626d0-135">**新規**をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-135">Click **New** to open the drop dialog.</span></span>
13. <span data-ttu-id="626d0-136">**名称**フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-136">In the **Name** field, type 'Code'.</span></span>
14. <span data-ttu-id="626d0-137">**品目タイプ**フィールドで、**文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-137">In the **Item type** field, select **String**.</span></span>
15. <span data-ttu-id="626d0-138">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-138">Click **Add**.</span></span>
16. <span data-ttu-id="626d0-139">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-139">Click **Save**.</span></span>
17. <span data-ttu-id="626d0-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="626d0-140">Close the page.</span></span>
18. <span data-ttu-id="626d0-141">**状態の変更**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-141">Click **Change status**.</span></span>
19. <span data-ttu-id="626d0-142">**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-142">Click **Complete**.</span></span>
20. <span data-ttu-id="626d0-143">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="626d0-144">データ インポート用の形式の作成</span><span class="sxs-lookup"><span data-stu-id="626d0-144">Create a format for data import</span></span>
1. <span data-ttu-id="626d0-145">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="626d0-146">**新規**フィールドで、「XML ファイルをインポートするモデルのデータ モデルに基づく形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="626d0-147">**名前**フィールドに、「XML ファイルをインポートする形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-147">In the **Nam**e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="626d0-148">**データのインポートのサポート** フィールドで**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="626d0-149">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="626d0-150">XML 形式で受信するファイルを解析する形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="626d0-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="626d0-151">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-151">Click **Designer**.</span></span>
2. <span data-ttu-id="626d0-152">**ルートの追加**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="626d0-153">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="626d0-154">**名称**のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="626d0-155">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-155">Click **OK**.</span></span>
6. <span data-ttu-id="626d0-156">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="626d0-157">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="626d0-158">**名前**フィールドに、「ドキュメント」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="626d0-159">**多様性**フィールドで、**1 つ、多数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-159">In the **Multiplicity** field, select **One many**.</span></span>
10. <span data-ttu-id="626d0-160">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-160">Click **OK**.</span></span>
11. <span data-ttu-id="626d0-161">ツリーで、**root\document** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-161">In the tree, select **root\document**.</span></span>
12. <span data-ttu-id="626d0-162">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="626d0-162">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="626d0-163">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-163">In the tree, select **XML\Attribute**.</span></span>
14. <span data-ttu-id="626d0-164">**名前**フィールドに、「ID」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-164">In the **Name** field, type 'id'.</span></span>
15. <span data-ttu-id="626d0-165">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-165">Click **OK**.</span></span>
16. <span data-ttu-id="626d0-166">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="626d0-167">解析された情報をデータ モデルに保存する形式マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="626d0-167">Design a format mapping to save parsed information to data model</span></span>
1.  <span data-ttu-id="626d0-168">**形式をモデルにマップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-168">Click **Map format to model**.</span></span>
2.  <span data-ttu-id="626d0-169">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-169">Click **New**.</span></span>
3.  <span data-ttu-id="626d0-170">**定義**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-170">In the **Definition** field, enter or select a value.</span></span>
4.  <span data-ttu-id="626d0-171">**名前**フィールドに、「マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="626d0-171">In the **Name** field, type 'Mapping'.</span></span>
5.  <span data-ttu-id="626d0-172">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-172">Click **Save**.</span></span>
6.  <span data-ttu-id="626d0-173">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-173">Click **Designer**.</span></span>
7.  <span data-ttu-id="626d0-174">ツリーで、**形式**を展開します。</span><span class="sxs-lookup"><span data-stu-id="626d0-174">In the tree, expand **format**.</span></span>
8.  <span data-ttu-id="626d0-175">ツリーで、**format\root: XML Element(root)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="626d0-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.  <span data-ttu-id="626d0-176">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="626d0-177">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="626d0-177">(document)\*\*.</span></span>
10. <span data-ttu-id="626d0-178">**バインド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-178">Click **Bind**.</span></span>
11. <span data-ttu-id="626d0-179">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を展開します。</span><span class="sxs-lookup"><span data-stu-id="626d0-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="626d0-180">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="626d0-180">(document)\*\*.</span></span>
12. <span data-ttu-id="626d0-181">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="626d0-182">(ドキュメント)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="626d0-182">(document)\id\*\*.</span></span>
13. <span data-ttu-id="626d0-183">ツリーで、**List = format.root.document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="626d0-183">In the tree, expand **List = format.root.document**.</span></span>
14. <span data-ttu-id="626d0-184">ツリーで、**List = format.root.document\Code** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-184">In the tree, select **List = format.root.document\Code**.</span></span>
15. <span data-ttu-id="626d0-185">**バインド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-185">Click **Bind**.</span></span>
16. <span data-ttu-id="626d0-186">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-186">Click **Save**.</span></span>
17. <span data-ttu-id="626d0-187">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="626d0-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="626d0-188">形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="626d0-188">Run format mapping</span></span>
1. <span data-ttu-id="626d0-189">**実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-189">Click **Run**.</span></span>
2. <span data-ttu-id="626d0-190">**参照**をクリックし、ファイル **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="626d0-191">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="626d0-192">選択したファイルは、「document」要素に「ID」属性が存在するように想定した形式デザインとしてインポートされませんでしたが、インポートされたファイルにそのような属性は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="626d0-192">The selected file has not been imported as the format design assumes the existence of ‘id’ attribute for the ‘document’ element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="626d0-193">XML 属性をオプションとして処理するよう形式構造を変更</span><span class="sxs-lookup"><span data-stu-id="626d0-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="626d0-194">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="626d0-194">Close the page.</span></span>
2. <span data-ttu-id="626d0-195">ツリーで、**root\document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="626d0-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="626d0-196">ツリーで、**root\document\id** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="626d0-197">**存在しない属性に対する空の文字列**フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="626d0-198">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="626d0-199">変更をテストするための形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="626d0-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="626d0-200">**形式をモデルにマップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="626d0-201">**実行**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-201">Click **Run**.</span></span>
3. <span data-ttu-id="626d0-202">**参照**をクリックし、ファイル **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。</span><span class="sxs-lookup"><span data-stu-id="626d0-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="626d0-203">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="626d0-203">Click **OK**.</span></span>
5. <span data-ttu-id="626d0-204">生成したファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="626d0-204">Review the generated file.</span></span> <span data-ttu-id="626d0-205">同じファイルが形式デザインとしてインポートされて、「document」要素の「ID」属性はオプションとして見なされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="626d0-205">Note that same file has been imported as the format design now consider the ‘id’ attribute for the ‘document’ element as optional.</span></span>

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
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14b14dd609805a7cf9331427012b991791698cfd
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686664"
---
# <a name="import-files-in-xml-format-with-optional-attributes"></a><span data-ttu-id="4d63e-103">オプションの属性を使用して XML 形式でファイルをインポートする</span><span class="sxs-lookup"><span data-stu-id="4d63e-103">Import files in XML format with optional attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d63e-104">XML 形式で受信する電子ドキュメントを解析するための電子申告 (ER) 形式をデザインできます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents in XML format.</span></span> <span data-ttu-id="4d63e-105">XML 要素の特定の属性は、デザインされた ER 形式でオプションとして指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-105">Certain attributes of XML elements can be specified in designed ER format as optional.</span></span> <span data-ttu-id="4d63e-106">これにより、該当する XML 属性のある受信ファイルとない受信ファイルを正しく処理することができます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-106">It will allow you to handle incoming files with and without such XML attributes properly.</span></span> <span data-ttu-id="4d63e-107">その後、アプリケーションのデータを更新するのに、これらのファイルからの内容を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-107">You can then use the content from these files to update application data.</span></span>

<span data-ttu-id="4d63e-108">この機能の詳細を知るには、7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部である [(RCS) オプションの属性を使用して XML 形式のファイルをインポートする](tasks/import-files-xml-format-optional-attributes.md) トピックの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-108">To learn more about this feature, complete the steps in the topic, [(RCS) Import files in XML format with optional attributes](tasks/import-files-xml-format-optional-attributes.md), which is part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process.</span></span> <span data-ttu-id="4d63e-109">このタスク ガイドおよび関連するサンプル ファイは [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684) からダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-109">You can download this task guide and associated sample files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>


| <span data-ttu-id="4d63e-110">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="4d63e-110">Content description</span></span>       | <span data-ttu-id="4d63e-111">ファイル</span><span class="sxs-lookup"><span data-stu-id="4d63e-111">File</span></span>                                                         |
|---------------------------|--------------------------------------------------------------|
| <span data-ttu-id="4d63e-112">XML 形式のサンプル ファイル</span><span class="sxs-lookup"><span data-stu-id="4d63e-112">Sample file in XML format</span></span> | <span data-ttu-id="4d63e-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span><span class="sxs-lookup"><span data-stu-id="4d63e-113">IncomingDocumentToLearnHowToHandleOptionalAttributes.xml</span></span>     |
| <span data-ttu-id="4d63e-114">タスク ガイド</span><span class="sxs-lookup"><span data-stu-id="4d63e-114">Task guide</span></span>                | <span data-ttu-id="4d63e-115">RCS オプションの attributes.axtr を使用して XML 形式のファイルをインポートする</span><span class="sxs-lookup"><span data-stu-id="4d63e-115">RCS Import files in XML format with optional attributes.axtr</span></span> |


<span data-ttu-id="4d63e-116">次のステップでは、システム管理者または電子申告開発者のロールに割り当てられているユーザーが、電子申告 (ER) の形式のコンフィギュレーションをデザインし、オプションの属性を含む XML 形式のファイルをインポートする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-116">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can design ER format configuration to import files in XML format containing optional attributes.</span></span> <span data-ttu-id="4d63e-117">これらの手順を完了するには、まず[コンフィギュレーション プロバイダーを作成し、有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d63e-117">To complete these steps, you must first complete the steps in the procedure, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="4d63e-118">始める前に、Microsoft ダウンロード センター (https://go.microsoft.com/fwlink/?linkid=874684) から IncomingDocumentToLearnHowToHandleOptionalAttributes.xml ファイルをダウンロードし、ローカルに保存します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-118">Before you begin, download and save locally the IncomingDocumentToLearnHowToHandleOptionalAttributes.xml file from Microsoft Download Center (https://go.microsoft.com/fwlink/?linkid=874684 ).</span></span>

1. <span data-ttu-id="4d63e-119">**組織管理** > **ワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-119">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="4d63e-120">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-120">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="4d63e-121">このコンフィギュレーション プロバイダーが表示されない場合、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) というトピックの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d63e-121">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="4d63e-122">**コンフィギュレーションをレポートする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-122">Click **Reporting configurations**.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="4d63e-123">新しいデータ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="4d63e-123">Create a new data model configuration</span></span>
1. <span data-ttu-id="4d63e-124">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-124">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="4d63e-125">**名前** フィールドに、「XML ファイルをインポートするモデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-125">In the **Name** field, type 'Model to import xml file'.</span></span>
3. <span data-ttu-id="4d63e-126">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-126">Click **Create configuration**.</span></span>
4. <span data-ttu-id="4d63e-127">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-127">Click **Designer**.</span></span>
5. <span data-ttu-id="4d63e-128">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-128">Click **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="4d63e-129">**名称** のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-129">In the **Name** field, type 'Root'.</span></span>
7. <span data-ttu-id="4d63e-130">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-130">Click **Add**.</span></span>
8. <span data-ttu-id="4d63e-131">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-131">Click **New** to open the drop dialog.</span></span>
9. <span data-ttu-id="4d63e-132">**名称** のフィールドに、「リスト」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-132">In the **Name** field, type 'List'.</span></span>
10.    <span data-ttu-id="4d63e-133">**品目タイプ** フィールドで、**レコード リスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-133">In the **Item type** field, select **Record list**.</span></span>
11.    <span data-ttu-id="4d63e-134">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-134">Click **Add**.</span></span>
12.    <span data-ttu-id="4d63e-135">**新規** をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-135">Click **New** to open the drop dialog.</span></span>
13.    <span data-ttu-id="4d63e-136">**名称** フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-136">In the **Name** field, type 'Code'.</span></span>
14.    <span data-ttu-id="4d63e-137">**品目タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-137">In the **Item type** field, select **String**.</span></span>
15.    <span data-ttu-id="4d63e-138">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-138">Click **Add**.</span></span>
16.    <span data-ttu-id="4d63e-139">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-139">Click **Save**.</span></span>
17.    <span data-ttu-id="4d63e-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-140">Close the page.</span></span>
18.    <span data-ttu-id="4d63e-141">**状態の変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-141">Click **Change status**.</span></span>
19.    <span data-ttu-id="4d63e-142">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-142">Click **Complete**.</span></span>
20.    <span data-ttu-id="4d63e-143">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-143">Click **OK**.</span></span>

## <a name="create-a-format-for-data-import"></a><span data-ttu-id="4d63e-144">データ インポート用の形式の作成</span><span class="sxs-lookup"><span data-stu-id="4d63e-144">Create a format for data import</span></span>
1. <span data-ttu-id="4d63e-145">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-145">Click **Create configuration** to open the drop dialog.</span></span>
2. <span data-ttu-id="4d63e-146">**新規** フィールドで、「XML ファイルをインポートするモデルのデータ モデルに基づく形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-146">In the **New** field, enter 'Format based on data model Model to import xml file'.</span></span>
3. <span data-ttu-id="4d63e-147">**名前** フィールドに、「XML ファイルをインポートする形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-147">In the **Nam** e field, type 'Format to import xml file'.</span></span> 
4. <span data-ttu-id="4d63e-148">**データのインポートのサポート** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-148">Select **Yes** in the **Supports data import** field.</span></span>
5. <span data-ttu-id="4d63e-149">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-149">Click **Create configuration**.</span></span>

## <a name="design-a-format-to-parse-incoming-file-in-xml-format"></a><span data-ttu-id="4d63e-150">XML 形式で受信するファイルを解析する形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="4d63e-150">Design a format to parse incoming file in xml format</span></span>
1. <span data-ttu-id="4d63e-151">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-151">Click **Designer**.</span></span>
2. <span data-ttu-id="4d63e-152">**ルートの追加** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-152">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="4d63e-153">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-153">In the tree, select **XML\Element**.</span></span>
4. <span data-ttu-id="4d63e-154">**名称** のフィールドに、「Root」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-154">In the **Name** field, type 'root'.</span></span>
5. <span data-ttu-id="4d63e-155">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-155">Click **OK**.</span></span>
6. <span data-ttu-id="4d63e-156">**追加** をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-156">Click **Add** to open the drop dialog.</span></span>
7. <span data-ttu-id="4d63e-157">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-157">In the tree, select **XML\Element**.</span></span>
8. <span data-ttu-id="4d63e-158">**名前** フィールドに、「ドキュメント」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-158">In the **Name** field, type 'document'.</span></span>
9. <span data-ttu-id="4d63e-159">**多様性** フィールドで、**1 つ、多数** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-159">In the **Multiplicity** field, select **One many**.</span></span>
10.    <span data-ttu-id="4d63e-160">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-160">Click **OK**.</span></span>
11.    <span data-ttu-id="4d63e-161">ツリーで、**root\document** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-161">In the tree, select **root\document**.</span></span>
12.    <span data-ttu-id="4d63e-162">**追加** をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-162">Click **Add** to open the drop dialog.</span></span>
13.    <span data-ttu-id="4d63e-163">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-163">In the tree, select **XML\Attribute**.</span></span>
14.    <span data-ttu-id="4d63e-164">**名前** フィールドに、「ID」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-164">In the **Name** field, type 'id'.</span></span>
15.    <span data-ttu-id="4d63e-165">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-165">Click **OK**.</span></span>
16.    <span data-ttu-id="4d63e-166">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-166">Click **Save**.</span></span>

## <a name="design-a-format-mapping-to-save-parsed-information-to-data-model"></a><span data-ttu-id="4d63e-167">解析された情報をデータ モデルに保存する形式マッピングのデザイン</span><span class="sxs-lookup"><span data-stu-id="4d63e-167">Design a format mapping to save parsed information to data model</span></span>
1.    <span data-ttu-id="4d63e-168">**形式をモデルにマップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-168">Click **Map format to model**.</span></span>
2.    <span data-ttu-id="4d63e-169">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-169">Click **New**.</span></span>
3.    <span data-ttu-id="4d63e-170">**定義** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-170">In the **Definition** field, enter or select a value.</span></span>
4.    <span data-ttu-id="4d63e-171">**名前** フィールドに、「マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-171">In the **Name** field, type 'Mapping'.</span></span>
5.    <span data-ttu-id="4d63e-172">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-172">Click **Save**.</span></span>
6.    <span data-ttu-id="4d63e-173">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-173">Click **Designer**.</span></span>
7.    <span data-ttu-id="4d63e-174">ツリーで、**形式** を展開します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-174">In the tree, expand **format**.</span></span>
8.    <span data-ttu-id="4d63e-175">ツリーで、**format\root: XML Element(root)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-175">In the tree, expand **format\root: XML Element(root)**.</span></span>
9.    <span data-ttu-id="4d63e-176">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-176">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="4d63e-177">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="4d63e-177">(document)\*\*.</span></span>
10.    <span data-ttu-id="4d63e-178">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-178">Click **Bind**.</span></span>
11.    <span data-ttu-id="4d63e-179">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を展開します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-179">In the tree, expand \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="4d63e-180">(ドキュメント)\*\*。</span><span class="sxs-lookup"><span data-stu-id="4d63e-180">(document)\*\*.</span></span>
12.    <span data-ttu-id="4d63e-181">ツリーで、\**format\root: XML Element(root)\document: XML Element 1* を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-181">In the tree, select \**format\root: XML Element(root)\document: XML Element 1..*</span></span> <span data-ttu-id="4d63e-182">(ドキュメント)\id\*\*。</span><span class="sxs-lookup"><span data-stu-id="4d63e-182">(document)\id\*\*.</span></span>
13.    <span data-ttu-id="4d63e-183">ツリーで、**List = format.root.document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-183">In the tree, expand **List = format.root.document**.</span></span>
14.    <span data-ttu-id="4d63e-184">ツリーで、**List = format.root.document\Code** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-184">In the tree, select **List = format.root.document\Code**.</span></span>
15.    <span data-ttu-id="4d63e-185">**バインド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-185">Click **Bind**.</span></span>
16.    <span data-ttu-id="4d63e-186">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-186">Click **Save**.</span></span>
17.    <span data-ttu-id="4d63e-187">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-187">Close the page.</span></span>

## <a name="run-format-mapping"></a><span data-ttu-id="4d63e-188">形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="4d63e-188">Run format mapping</span></span>
1. <span data-ttu-id="4d63e-189">**実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-189">Click **Run**.</span></span>
2. <span data-ttu-id="4d63e-190">**参照** をクリックし、ファイル **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-190">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
3. <span data-ttu-id="4d63e-191">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-191">Click **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="4d63e-192">選択したファイルは、「document」要素に「ID」属性が存在するように想定した形式デザインとしてインポートされませんでしたが、インポートされたファイルにそのような属性は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="4d63e-192">The selected file has not been imported as the format design assumes the existence of 'id' attribute for the 'document' element, but the imported file contains no such attribute.</span></span>

## <a name="modify-format-structure-to-handle-xml-attribute-as-optional"></a><span data-ttu-id="4d63e-193">XML 属性をオプションとして処理するよう形式構造を変更</span><span class="sxs-lookup"><span data-stu-id="4d63e-193">Modify format structure to handle xml attribute as optional</span></span>
1. <span data-ttu-id="4d63e-194">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4d63e-194">Close the page.</span></span>
2. <span data-ttu-id="4d63e-195">ツリーで、**root\document** を展開します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-195">In the tree, expand **root\document**.</span></span>
3. <span data-ttu-id="4d63e-196">ツリーで、**root\document\id** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-196">In the tree, select **root\document\id**.</span></span>
4. <span data-ttu-id="4d63e-197">**存在しない属性に対する空の文字列** フィールドで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-197">In the **Empty string for missing attribute** field, select **Yes**.</span></span>
5. <span data-ttu-id="4d63e-198">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-198">Click **Save**.</span></span>

## <a name="run-format-mapping-to-test-changes"></a><span data-ttu-id="4d63e-199">変更をテストするための形式マッピングの実行</span><span class="sxs-lookup"><span data-stu-id="4d63e-199">Run format mapping to test changes</span></span>
1. <span data-ttu-id="4d63e-200">**形式をモデルにマップ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-200">Click **Map format to model**.</span></span>
2. <span data-ttu-id="4d63e-201">**実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-201">Click **Run**.</span></span>
3. <span data-ttu-id="4d63e-202">**参照** をクリックし、ファイル **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-202">Click **Browse** and select the file, **IncomingDocumentToLearnHowToHandleOptionalAttributes.xml**.</span></span>
4. <span data-ttu-id="4d63e-203">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d63e-203">Click **OK**.</span></span>
5. <span data-ttu-id="4d63e-204">生成したファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="4d63e-204">Review the generated file.</span></span> <span data-ttu-id="4d63e-205">同じファイルが形式デザインとしてインポートされ、「document」要素の「ID」属性はオプションとして見なされることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4d63e-205">Note that same file has been imported as the format design now consider the 'id' attribute for the 'document' element as optional.</span></span>

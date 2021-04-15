---
title: PDF テンプレートに入力する ER コンフィギュレーションのデザイン
description: このトピックでは、PDF テンプレートに入力する電子レポート (ER) 形式をデザインする方法について説明します。
author: NickSelin
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7c1c21015a172d7ebaa3577d5d0e55c254ef871e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753291"
---
# <a name="design-er-configurations-to-fill-in-pdf-templates"></a><span data-ttu-id="fa0cc-103">PDF テンプレートに入力する ER コンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="fa0cc-103">Design ER configurations to fill in PDF templates</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fa0cc-104">このトピックの手順は、**システム管理者** ロールまたは **電子レポート開発者** ロールのユーザーが、レポート テンプレートとしての PDF ドキュメントを使いレポートを PDF として生成する電子レポート (ER) 形式をどのようにコンフィギュレーションできるかを示す例です。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-104">The procedures in this topic are examples that show how a user in either the **System administrator** role or the **Electronic reporting developer** role can configure an Electronic reporting (ER) format that generates reports as PDF files by using fillable PDF documents as report templates.</span></span> <span data-ttu-id="fa0cc-105">これらの手順は、Dynamics 365 Finance または Regulatory Configuration Services (RCS) のどの会社でも実行できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-105">These steps can be performed in any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fa0cc-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="fa0cc-106">Prerequisites</span></span>

<span data-ttu-id="fa0cc-107">開始する前に、このトピックの手順を実行するために使用するサービスに応じて、次のいずれかのタイプのアクセス権を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-107">Before you begin, you must have one of the following types of access, depending on the service that you use to complete the procedures in this topic:</span></span>

- <span data-ttu-id="fa0cc-108">次のいずれかのロールに対応する財務にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-108">Access to Finance for one of the following roles:</span></span>

    - <span data-ttu-id="fa0cc-109">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="fa0cc-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="fa0cc-110">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="fa0cc-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="fa0cc-111">システム管理者</span><span class="sxs-lookup"><span data-stu-id="fa0cc-111">System administrator</span></span>

- <span data-ttu-id="fa0cc-112">次のいずれかのロールに対応する RCS にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-112">Access to RCS for one of the following roles:</span></span>

    - <span data-ttu-id="fa0cc-113">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="fa0cc-113">Electronic reporting developer</span></span>
    - <span data-ttu-id="fa0cc-114">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="fa0cc-114">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="fa0cc-115">システム管理者</span><span class="sxs-lookup"><span data-stu-id="fa0cc-115">System administrator</span></span>

<span data-ttu-id="fa0cc-116">また、[コンフィギュレーション プロバイダーを作成しアクティブとマーク](tasks/er-configuration-provider-mark-it-active-2016-11.md) の手順を完成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-116">You must also complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="fa0cc-117">最後に、次のファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-117">Finally, download the following files.</span></span>

| <span data-ttu-id="fa0cc-118">コンテンツの説明</span><span class="sxs-lookup"><span data-stu-id="fa0cc-118">Content description</span></span>                       | <span data-ttu-id="fa0cc-119">ファイル名</span><span class="sxs-lookup"><span data-stu-id="fa0cc-119">File name</span></span>                                     |
|-------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="fa0cc-120">レポートの最初のページをテンプレート</span><span class="sxs-lookup"><span data-stu-id="fa0cc-120">Template for the first page of the report</span></span> | [<span data-ttu-id="fa0cc-121">IntrastatReportTemplate1.pdf</span><span class="sxs-lookup"><span data-stu-id="fa0cc-121">IntrastatReportTemplate1.pdf</span></span>](https://download.microsoft.com/download/0/8/3/0832c82b-4448-4562-afbf-01e0efc8d999/IntrastatReportTemplate1.pdf)                  |
| <span data-ttu-id="fa0cc-122">レポートの他のページをテンプレート</span><span class="sxs-lookup"><span data-stu-id="fa0cc-122">Template for other pages of the report</span></span>    | [<span data-ttu-id="fa0cc-123">IntrastatReportTemplate2.pdf</span><span class="sxs-lookup"><span data-stu-id="fa0cc-123">IntrastatReportTemplate2.pdf</span></span>](https://download.microsoft.com/download/c/7/a/c7a8a806-2192-4034-9052-e8b84b527d5e/IntrastatReportTemplate2.pdf)                  |
| <span data-ttu-id="fa0cc-124">ER フォーマットのサンプル - PDF</span><span class="sxs-lookup"><span data-stu-id="fa0cc-124">Sample ER format - PDF</span></span>                          | [<span data-ttu-id="fa0cc-125">イントラスタット レポート (PDF). バージョン .1.1.xml</span><span class="sxs-lookup"><span data-stu-id="fa0cc-125">Intrastat report (PDF).version.1.1.xml</span></span>](https://download.microsoft.com/download/a/8/7/a87aea3e-3f60-404c-8899-c471d20e7ea9/IntrastatreportPDFversion1.1.xml)        |
| <span data-ttu-id="fa0cc-126">ER フォーマットのサンプル - Excel</span><span class="sxs-lookup"><span data-stu-id="fa0cc-126">Sample ER format - Excel</span></span>                          | [<span data-ttu-id="fa0cc-127">イントラスタット (Excel からインポート). バージョン .1.1.xml</span><span class="sxs-lookup"><span data-stu-id="fa0cc-127">Intrastat (import from Excel).version.1.1.xml</span></span>](https://download.microsoft.com/download/a/2/c/a2c0c145-d989-4e55-9d47-9647c02e4ee4/IntrastatimportfromExcelversion1.1.xml) |
| <span data-ttu-id="fa0cc-128">サンプル データセット</span><span class="sxs-lookup"><span data-stu-id="fa0cc-128">Sample dataset</span></span>                            | [<span data-ttu-id="fa0cc-129">イントラスタット サンプル データ .xlsx</span><span class="sxs-lookup"><span data-stu-id="fa0cc-129">Intrastat sample data.xlsx</span></span>](https://download.microsoft.com/download/9/f/1/9f1c5b96-3800-475f-8cf6-1ddd42873758/Intrastatsampledata.xlsx)                    |

## <a name="design-the-format-configuration"></a><span data-ttu-id="fa0cc-130">形式のコンフィギュレーションをデザイン</span><span class="sxs-lookup"><span data-stu-id="fa0cc-130">Design the format configuration</span></span>

### <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a><span data-ttu-id="fa0cc-131">Microsoft 提供の設定リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="fa0cc-131">Get access to the list of configurations provided by Microsoft</span></span>

1. <span data-ttu-id="fa0cc-132">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-132">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="fa0cc-133">**Litware, Inc.** 事業者が使用可能で、有効としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-133">Make sure that the **Litware, Inc.** provider is available and marked as active.</span></span>
3. <span data-ttu-id="fa0cc-134">**Microsoft** プロバイダーのタイルで、**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-134">On the tile for the **Microsoft** provider, select **Repositories**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa0cc-135">**LCS** タイプのレポジトリが既に存在する場合、この手順の残りのステップを省略します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-135">If a repository of the **LCS** type already exists, skip the remaining steps of this procedure.</span></span>

4. <span data-ttu-id="fa0cc-136">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-136">Select **Add**.</span></span>
5. <span data-ttu-id="fa0cc-137">ドロップダウン ダイアログ ボックスの **コンフィギュレーション レポジトリ タイプ** フィールド グループで、**LCS** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-137">In the drop-down dialog box, in the **Configuration repository type** field group, select the **LCS** option.</span></span>
6. <span data-ttu-id="fa0cc-138">**レポジトリを作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-138">Select **Create repository**.</span></span>
7. <span data-ttu-id="fa0cc-139">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-139">Select **OK**.</span></span>

### <a name="get-the-model-configurations-provided-by-microsoft"></a><span data-ttu-id="fa0cc-140">Microsoft 提供のモデル コンフィギュレーションを取得</span><span class="sxs-lookup"><span data-stu-id="fa0cc-140">Get the model configurations provided by Microsoft</span></span>

1. <span data-ttu-id="fa0cc-141">**コンフィギュレーション リポジトリ** ページの左側で、**フィルターを表示** ボタン (じょうごシンボル) を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-141">On the left side of the **Configuration repositories** page, select the **Show filters** button (the funnel symbol).</span></span>
2. <span data-ttu-id="fa0cc-142">**タイプ** フィールドにある **LCS** の値フィルターを追加し、**で始まる** オペレーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-142">Add a filter for a value of **LCS** in the **Type** field, and use the **begins with** operator.</span></span>
3. <span data-ttu-id="fa0cc-143">**適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-143">Select **Apply**.</span></span>
4. <span data-ttu-id="fa0cc-144">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-144">Select **Open**.</span></span>
5. <span data-ttu-id="fa0cc-145">ツリーで、**イントラスタット モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-145">In the tree, select **Intrastat model**.</span></span>
6. <span data-ttu-id="fa0cc-146">**バージョン** FastTab で、バージョン **1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-146">On the **Versions** FastTab, select version **1**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa0cc-147">**バージョン** FastTab で **インポート** ボタンが使用できない場合、この手順の残りのステップを省略します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-147">If the **Import** button on the **Versions** FastTab is unavailable, skip the remaining steps of this procedure.</span></span>

7. <span data-ttu-id="fa0cc-148">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-148">Select **Import**.</span></span>
8. <span data-ttu-id="fa0cc-149">**はい** を選択し、**イントラスタット モデル** モデル コンフィギュレーションの選択されたバージョンのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-149">Select **Yes** to confirm the import of the selected version of the **Intrastat model** model configuration.</span></span>

### <a name="create-a-new-format-configuration"></a><span data-ttu-id="fa0cc-150">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="fa0cc-150">Create a new format configuration</span></span>

1. <span data-ttu-id="fa0cc-151">**電子レポート** ワークスペースで、**レポート コンフィギュレーション** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-151">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="fa0cc-152">ツリーで、**イントラスタット モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-152">In the tree, select **Intrastat model**.</span></span>
3. <span data-ttu-id="fa0cc-153">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-153">Select **Create configuration**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa0cc-154">**コンフィギュレーションの作成** ボタンが使用できない場合、**電子レポート** ワークスペースから開くことができる **電子レポート パラメーター** ページのデザイン モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-154">If the **Create configuration** button isn't available, you must turn on design mode on the **Electronic reporting parameters** page that can be opened from the **Electronic reporting** workspace.</span></span>

4. <span data-ttu-id="fa0cc-155">ドロップダウン ダイアログ ボックスにある **新しい** フィールド グループで、**データ モデル イントラスタットに基づくフォーマット** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-155">In the drop-down dialog box, in the **New** field group, select the **Format based on data model Intrastat** option.</span></span>
5. <span data-ttu-id="fa0cc-156">**名前** フィールドで、**イントラスタット レポート (PDF)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-156">In the **Name** field, enter **Intrastat report (PDF)**.</span></span>
6. <span data-ttu-id="fa0cc-157">**説明** フィールドで、**PDF フォーマットのイントラスタット レポート** を入力します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-157">In the **Description** field, enter **Intrastat report in PDF format**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa0cc-158">有効なコンフィギュレーション プロバイダーは自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-158">The active configuration provider is automatically entered.</span></span> <span data-ttu-id="fa0cc-159">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-159">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="fa0cc-160">たとえ他のプロバイダーがこのコンフィギュレーションを使用できても、管理することはできません。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-160">Although other providers can use this configuration, they won't be able to maintain it.</span></span>

7. <span data-ttu-id="fa0cc-161">オプション: **フォーマット タイプ** フィールドで、電子ドキュメントの特定形式を選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-161">Optional: In the **Format type** field, you can select a specific format of electronic document.</span></span> <span data-ttu-id="fa0cc-162">デザイン時に **PDF** を選択する場合、ER オペレーション デザイナーは形式に生成されたドキュメントのみに適用される形式要素のみを提供します (**PDF\File**、**PDF\PDF 合併**、など)。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-162">If you select **PDF**, at design time, the ER Operations designer will offer just the format elements that are applicable only to documents that are generated in PDF format (**PDF\File**, **PDF\PDF Merger**, etc.).</span></span> <span data-ttu-id="fa0cc-163">このフィールドを空白のままにすると、最初の形式要素が追加されるときに、ER オペレーション デザイナーのデザイン時に電子ドキュメントの形式が指定されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-163">If you leave this field blank, a format of electronic document will be specified at design time in the ER Operations designer when a first format element will be added.</span></span> <span data-ttu-id="fa0cc-164">たとえば、**Excel\File** を最初の形式要素として追加した場合、ER オペレーション デザイナーは Excel 形式で生成されたドキュメントのみに適用される形式要素だけを提供します (**Excel\Cell**、**Excel\Range**、など)。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-164">For example, if you add the **Excel\File** as the first format element, the ER Operations designer will offer you just the format elements that are applicable only to documents that are generated in Excel format (**Excel\Cell**, **Excel\Range**, etc.).</span></span> <span data-ttu-id="fa0cc-165">形式。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-165">format.</span></span>
8. <span data-ttu-id="fa0cc-166">**コンフィギュレーションの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-166">Select **Create configuration**.</span></span>

<span data-ttu-id="fa0cc-167">新しい ER 形式のコンフィギュレーションが作成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-167">A new ER format configuration is created.</span></span> <span data-ttu-id="fa0cc-168">このコンフィギュレーションの下書きバージョンを使用して、PDF 形式の電子ドキュメントを生成するように設計された ER 形式のコンポーネントを保存できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-168">You can use the draft version of this configuration to store the ER format component that is designed to generate electronic documents in PDF format.</span></span>

### <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="fa0cc-169">電子ドキュメントの形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="fa0cc-169">Design the format of an electronic document</span></span>

<span data-ttu-id="fa0cc-170">次に、作成した ER 形式のコンフィギュレーションで、PDF 形式の **イントラスタット コントロール** レポートを生成する ER 形式をデザインします。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-170">Next, in the ER format configuration that you created, you will design the ER format that generates the **Intrastat control** report in PDF format.</span></span> <span data-ttu-id="fa0cc-171">このレポートの最初のページには、レポートの概要および報告された対外貿易トランザクションの詳細を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-171">The first page of this report must show a summary of the report and details of the foreign trade transactions that are reported on.</span></span> <span data-ttu-id="fa0cc-172">他のページでは、報告された対外貿易トランザクションの詳細のみを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-172">The other pages must show only details of the foreign trade transactions that are reported on.</span></span> <span data-ttu-id="fa0cc-173">生成されるレポート ページのレイアウトが異なるため、PDF 形式の 2 つの異なるテンプレートが ER 形式で使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-173">Because the report pages that are generated must have different layouts, two different templates in PDF format will be used in the ER format.</span></span>

<span data-ttu-id="fa0cc-174">どの PDF ビューアーでも、ダウンロードした PDF テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-174">In any PDF viewer, open the PDF templates that you downloaded.</span></span> <span data-ttu-id="fa0cc-175">各テンプレートには、入力の必要がある複数のフィールドが含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-175">Notice that each template contains multiple fields that must be filled in.</span></span> <span data-ttu-id="fa0cc-176">各テンプレートでは、対外貿易トランザクションの詳細が 42 行として表示され、それぞれに 9 つのフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-176">In each template, details of foreign trade transactions are presented as 42 rows, each of which has nine fields.</span></span> <span data-ttu-id="fa0cc-177">行番号は各フィールドの名前の末尾に表示されます (例えば、**日付 1**… **日付 42** および **商品 1**… **商品 42**)。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-177">The row number appears at the end of each field's name (for example, **Date 1**…**Date 42** and **Commodity 1**…**Commodity 42**).</span></span>

<span data-ttu-id="fa0cc-178">次の図は、レポートの最初のページの PDF テンプレートを示しています。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-178">The following illustration shows the PDF template for the first page of the report.</span></span>

![テンプレート 1](media/rcs-ger-filloutpdf-template1.png)

<span data-ttu-id="fa0cc-180">次の図は、レポートの他のページの PDF テンプレートを示しています。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-180">The following illustration shows the PDF template for other pages of the report.</span></span>

![テンプレート 2](media/rcs-ger-filloutpdf-template2.png)

1. <span data-ttu-id="fa0cc-182">**構成** ページで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-182">On the **Configurations** page, select **Designer**.</span></span>
2. <span data-ttu-id="fa0cc-183">**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-183">Select **Add root**.</span></span>
3. <span data-ttu-id="fa0cc-184">ドロップダウン ダイアログ ボックスのツリーで、**PDF \> PDF 合併** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-184">In the drop-down dialog box, in the tree, select **PDF \> PDF Merger**.</span></span>

    <span data-ttu-id="fa0cc-185">形式のルート要素として **PDF 合併** 要素を選択するとき、実行時に生成されるすべての PDF ドキュメントが単一の最終 PDF ドキュメントにマージされます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-185">When you select the **PDF Merger** element as the root element of the format, all PDF documents that are generated at run time will be merged into a single final PDF document.</span></span> <span data-ttu-id="fa0cc-186">デザインした ER 形式を使用してすべての必要なドキュメントを生成する PDF テンプレートが 1 つだけの場合、**PDF ファイル** をルート要素として選択できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-186">If you need only one PDF template to generate all the required documents by using the ER format that you design, you can select **PDF file** as the root element.</span></span>

4. <span data-ttu-id="fa0cc-187">**名前** フィールドに、**アウトプット** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-187">In the **Name** field, enter **Output**.</span></span>
5. <span data-ttu-id="fa0cc-188">**言語の基本設定** フィールドで、**ユーザーの基本設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-188">In the **Language preferences** field, select **User preference**.</span></span> <span data-ttu-id="fa0cc-189">レポートは、実行したユーザーの優先言語で生成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-189">The report will be generated in the preferred language of the user who runs it.</span></span>
6. <span data-ttu-id="fa0cc-190">**カルチャの基本設定** フィールドで、**ユーザーの基本設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-190">In the **Culture preferences** field, select **User preference**.</span></span> <span data-ttu-id="fa0cc-191">レポートのページに表示される値と日付は、レポートを実行するユーザーの優先ロケールに基づいて書式設定されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-191">Values and dates that are presented on the pages of the report will be formatted based on the preferred locale of the user who runs the report.</span></span>
7. <span data-ttu-id="fa0cc-192">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-192">Select **OK**.</span></span>
8. <span data-ttu-id="fa0cc-193">アクション ウィンドウの **インポート** タブで、**PDF からインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-193">On the Action Pane, on the **Import** tab, select **Import from PDF**.</span></span>

    <span data-ttu-id="fa0cc-194">入力可能な PDF ドキュメントが、この ER 形式のテンプレートとしてインポートされるとき、すべての必要な ER 形式の要素 (**PDF ファイル**、**フィールド グループ** および **フィールド** 要素) が、インポートされる PDF ドキュメントの構造に基づいて、自動的にデザインされた形式に作成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-194">When a fillable PDF document is imported as a template for this ER format, all the required ER format elements (**PDF file**, **Field group**, and **Field** elements) are automatically created in the format that is designed, based on the structure of the PDF document that is imported.</span></span>

9. <span data-ttu-id="fa0cc-195">**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-195">Select **Browse**.</span></span> <span data-ttu-id="fa0cc-196">前提条件として事前にダウンロードした **IntrastatReportTemplate1.pdf** ファイルに移動して選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-196">Navigate to and select the **IntrastatReportTemplate1.pdf** file that you downloaded earlier as a prerequisite.</span></span>
10. <span data-ttu-id="fa0cc-197">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-197">Select **OK**.</span></span>

    <span data-ttu-id="fa0cc-198">選択したファイルが読み込まれ、**PDF からインポート** ダイアログ ボックスの **テンプレート** フィールドが入力されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-198">The selected file is loaded, and the **Template** field in the **Import from PDF** dialog box is filled in.</span></span>

11. <span data-ttu-id="fa0cc-199">**グループ フィールド** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-199">Set the **Group fields** option to **Yes**.</span></span> <span data-ttu-id="fa0cc-200">選択した PDF ドキュメントが任意のフィールドグループを含む場合は、作成された ER 形式の要素をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-200">If the selected PDF document contains any field groups, they will be used to group the ER format elements that are created.</span></span> <span data-ttu-id="fa0cc-201">この目的のために、**フィールド グループ** 形式の要素が作成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-201">A **Field group** format element will be created for this purpose.</span></span>

    <span data-ttu-id="fa0cc-202">このオプションを **いいえ** に設定する場合、必要な ER 形式の要素が、作成される **PDF ファイル** 形式の要素の下に入れ子になった要素の単純なリストとして作成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-202">If this option is set to **No**, the required ER format elements will be created as a flat list of elements that are nested under the **PDF File** format element that is created.</span></span>

12. <span data-ttu-id="fa0cc-203">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-203">Select **OK**.</span></span>

    ![PDF ダイアログ ボックスからインポート](media/rcs-ger-filloutpdf-importtemplate.png)

13. <span data-ttu-id="fa0cc-205">ツリーで、**アウトプット** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-205">In the tree, expand **Output**.</span></span>

    <span data-ttu-id="fa0cc-206">実行時に生成されるレポートの最初のページの作成を管理するために、**PDF ファイル** コンポーネントは自動的に作成されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-206">Notice that the **PDF File** component has been automatically created to manage the creation of the first page of the report that is generated at run time.</span></span>

14. <span data-ttu-id="fa0cc-207">ツリーで **アウトプット \> PDF ファイル** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-207">In the tree, expand **Output \> PDF File**.</span></span>

    <span data-ttu-id="fa0cc-208">書式設定要素の構造化された一覧が、先にインポートした入力可能な PDF ドキュメントの構造に基づいて、この ER 形式で自動的に作成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-208">Notice that the structured list of format elements has been automatically created in this ER format, based on the structure of the fillable PDF document that you imported earlier.</span></span>

15. <span data-ttu-id="fa0cc-209">ツリーで、**アウトプット \> PDF ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-209">In the tree, select **Output \> PDF File**.</span></span>
16. <span data-ttu-id="fa0cc-210">**名前** フィールドに、**ページ 1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-210">In the **Name** field, enter **Page 1**.</span></span>

    <span data-ttu-id="fa0cc-211">この形式要素は、**イントラスタット制御** レポートの最初のページを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-211">This format element will be used to generate the first page of the **Intrastat control** report.</span></span> <span data-ttu-id="fa0cc-212">このページには、レポートの概要および対外貿易トランザクションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-212">That page will show a summary of the report and details of foreign trade transactions.</span></span>

    <span data-ttu-id="fa0cc-213">**言語の詳細設定** フィールドを空白のままにする場合、親の **PDF 合併** 要素の **言語の詳細設定** 設定は、この形式要素を使用して生成されるレポートの言語を決定します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-213">If you leave the **Language preferences** field blank, the **Language preferences** setting of the parent **PDF Merger** element will determine the language of the report that is generated by using this format element.</span></span> <span data-ttu-id="fa0cc-214">別の値を選択して、親要素の設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-214">You can select another value to override the setting of the parent element.</span></span>

    <span data-ttu-id="fa0cc-215">**カルチャの詳細設定** フィールドを空白のままにする場合、親の **PDF 合併** 要素の **カルチャの詳細設定** 設定は、この形式要素を使用して生成されるレポートのロケールを決定します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-215">If you leave the **Culture preferences** field blank, the **Culture preferences** setting of the parent **PDF Merger** element will determine the locale of the report that is generated by using this format element.</span></span> <span data-ttu-id="fa0cc-216">ロケールによって、レポートのページで値と日付の形式が決まります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-216">The locale determines the format of values and dates on the pages of the report.</span></span> <span data-ttu-id="fa0cc-217">別の値を選択して、親要素の設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-217">You can select another value to override the setting of the parent element.</span></span>

17. <span data-ttu-id="fa0cc-218">アクションウィンドウで、**インポート** タブを選択します。**PDF から更新** ボタンは、選択した形式要素の **PDF ファイル** に使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-218">On the Action Pane, select the **Import** tab. Notice that the **Update from PDF** button has become available for selected format element, **PDF File**.</span></span>

    <span data-ttu-id="fa0cc-219">このボタンを使用して、更新された PDF テンプレートを編集した形式にインポートできます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-219">You can use this button to import the updated PDF template to the edited format.</span></span> <span data-ttu-id="fa0cc-220">更新された PDF テンプレートをインポートすると、それに応じて形式要素の一覧が変更されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-220">When the updated PDF template is imported, the list of format elements will be changed accordingly:</span></span>

    - <span data-ttu-id="fa0cc-221">更新された PDF テンプレートの新しいフィールドについては、編集された ER 形式で新しい形式の要素が作成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-221">For any new fields in the updated PDF template, new format elements are created in the edited ER format.</span></span>
    - <span data-ttu-id="fa0cc-222">更新された PDF テンプレートに、編集された ER 形式の既存の形式要素に対応するフィールドが含まれなくなった場合、それらの書式要素が ER 形式から削除されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-222">If the updated PDF template no longer includes fields that correspond to any existing format elements in the edited ER format, those format elements are deleted from the ER format.</span></span>

18. <span data-ttu-id="fa0cc-223">**形式** タブで、**添付ファイル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-223">On the **Format** tab, select **Attachments**.</span></span>

    <span data-ttu-id="fa0cc-224">読み込んだ PDF ドキュメントが編集した ER 形式で関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-224">Notice that the imported PDF document is attached to the edited ER format.</span></span>

    ![PDF ファイルのプレビュー](media/rcs-ger-filloutpdf-attachedtemplate.png)

19. <span data-ttu-id="fa0cc-226">この形式を引き続きデザインするには、2 番目の PDF テンプレートをインポートし、必要なバインドをデータ ソースに追加します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-226">Continue to design this format by importing the second PDF template, adding necessary bindings to data sources, and so on.</span></span>
20. <span data-ttu-id="fa0cc-227">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-227">Select **Save**.</span></span>
21. <span data-ttu-id="fa0cc-228">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-228">Close the page.</span></span>
22. <span data-ttu-id="fa0cc-229">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-229">Select **Delete**.</span></span>
23. <span data-ttu-id="fa0cc-230">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-230">Select **Yes**.</span></span>

<span data-ttu-id="fa0cc-231">新しい **PDF 合併**、**PDF ファイル**、**フィールド グループ** および **フィールド** 形式の要素を使用して PDF 形式のドキュメントを生成する方法については、サンプル ER 形式をインポートおよび分析します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-231">To learn how new **PDF Merger**, **PDF File**, **Field group** and **Field** format elements can be used to generate documents in PDF format, you can import and analyze the sample ER format.</span></span>

### <a name="import-the-format-configuration"></a><span data-ttu-id="fa0cc-232">書式設定のコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="fa0cc-232">Import the format configuration</span></span>

<span data-ttu-id="fa0cc-233">次に、以前にダウンロードしたサンプル ER 形式をインポートし、PDF 形式の **イントラスタット コントロール** レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-233">Next, you will import the sample ER format that you previously downloaded to generate the **Intrastat control** report in PDF format.</span></span> <span data-ttu-id="fa0cc-234">レポートの最初のページには、レポートの概要および報告された対外貿易トランザクションの詳細を表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-234">The first page of the report must show a summary of the report and details of the foreign trade transactions that are reported on.</span></span> <span data-ttu-id="fa0cc-235">他のページでは、報告された対外貿易トランザクションの詳細のみを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-235">The other pages must show only details of the foreign trade transactions that are reported on.</span></span>

1. <span data-ttu-id="fa0cc-236">**コンフィギュレーション** ページで、**交換 \> XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-236">On the **Configurations** page, select **Exchange \> Load from XML file**.</span></span>
2. <span data-ttu-id="fa0cc-237">**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-237">Select **Browse**.</span></span> <span data-ttu-id="fa0cc-238">前提条件として事前にダウンロードした **インストタット レポート (PDF). バージョン .1.1.xml** ファイルに移動して選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-238">Navigate to and select the **Intrastat report (PDF).version.1.1.xml** file that you downloaded earlier as a prerequisite.</span></span>
3. <span data-ttu-id="fa0cc-239">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-239">Select **OK**.</span></span>

## <a name="analyze-the-format-configuration"></a><span data-ttu-id="fa0cc-240">書式設定のコンフィギュレーションの分析</span><span class="sxs-lookup"><span data-stu-id="fa0cc-240">Analyze the format configuration</span></span>

### <a name="format-layout"></a><span data-ttu-id="fa0cc-241">形式レイアウト</span><span class="sxs-lookup"><span data-stu-id="fa0cc-241">Format layout</span></span>

1. <span data-ttu-id="fa0cc-242">**コンフィギュレーション** ページのツリーで、**イントラスタット モデル \> イントラスタット レポート (PDF)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-242">On the **Configurations** page, in the tree, select **Intrastat model \> Intrastat report (PDF)**.</span></span>
2. <span data-ttu-id="fa0cc-243">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-243">Select **Designer**.</span></span>
3. <span data-ttu-id="fa0cc-244">**詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-244">Select **Show details**.</span></span>
4. <span data-ttu-id="fa0cc-245">ツリーで、**アウトプット: PDF 合併** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-245">In the tree, expand **Output: PDF Merger**.</span></span>

    <span data-ttu-id="fa0cc-246">この ER 形式には、それぞれ異なる PDF 形式を使用する 2 つの **PDF ファイル** の要素が含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-246">Notice that this ER format contains two **PDF File** elements, each of which uses a different PDF template.</span></span> <span data-ttu-id="fa0cc-247">1 つのテンプレートを使用してレポートの最初のページを PDF 形式で生成し、もう 1 つのテンプレートを使用して他のページを生成します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-247">One template is used to generate the first page of the report in PDF format, and the other template is used to generate the other pages.</span></span>

5. <span data-ttu-id="fa0cc-248">ツリーで、**出力: PDF 合併 \> ページ 1: PDF ファイル (IntrastatReportTemplate1)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-248">In the tree, expand **Output: PDF Merger \> Page 1: PDF File (IntrastatReportTemplate1)**.</span></span>
6. <span data-ttu-id="fa0cc-249">ツリーで、**出力: PDF 合併 \> ページ N: PDF ファイル (IntrastatReportTemplate2)** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-249">In the tree, expand **Output: PDF Merger \> Page N: PDF File (IntrastatReportTemplate2)**.</span></span>

    <span data-ttu-id="fa0cc-250">2 つの PDF テンプレートの内容が異なるため、2 つの **PDF ファイル** 要素の入れ子になった形式要素の構造も異なります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-250">Notice that, because the content of the two PDF templates differs, the structure of the nested format elements for the two **PDF File** elements also differs.</span></span>

### <a name="format-mapping"></a><span data-ttu-id="fa0cc-251">形式マッピング</span><span class="sxs-lookup"><span data-stu-id="fa0cc-251">Format mapping</span></span>

1. <span data-ttu-id="fa0cc-252">**フォーマット デザイナー** ページで、**マッピング** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-252">On the **Format designer** page, select the **Mapping** tab.</span></span>
2. <span data-ttu-id="fa0cc-253">ツリーで、**ページング \> ページ** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-253">In the tree, expand **Paging \> Pages**.</span></span>

    ![モデル ツリーが展開される数式デザイナーのページ](media/rcs-ger-filloutpdf-reviewformat.png)

    <span data-ttu-id="fa0cc-255">次の詳細に留意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-255">Note the following details:</span></span>

    - <span data-ttu-id="fa0cc-256">**PDF ファイル** タイプの **アウトプット \> ページ 1** の形式要素は、どのデータ ソースにもバインドされず、この形式要素の **有効** 式は空になります。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-256">The **Output \> Page 1** format element of the **PDF File** type isn't bound to any data source, and the **Enabled** expression of this format element is empty.</span></span> <span data-ttu-id="fa0cc-257">したがって、実行時に **IntrastatReportTemplate1** の PDF テンプレートは、個々の PDF ドキュメントが生成されたときに 1 回だけ入力されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-257">Therefore, at run time, the **IntrastatReportTemplate1** PDF template will be filled in only one time when an individual PDF document is generated.</span></span>
    - <span data-ttu-id="fa0cc-258">**PDF ファイル** タイプの **アウトプット \> ページ N** の形式要素は、**レコード リスト** タイプの **ページング. ページ N** データ ソースにバインドされ、この形式要素の **有効** 式は空です。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-258">The **Output \> Page N** format element of the **PDF File** type is bound to the **Paging.PageN** data source of the **Record list** type, and the **Enabled** expression of this format element is empty.</span></span> <span data-ttu-id="fa0cc-259">したがって、実行時に **IntrastatReportTemplate2** の PDF テンプレートは、個々の PDF ドキュメントが生成されたときにバインド レコードから各レコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-259">Therefore, at run time, the **IntrastatReportTemplate2** PDF template will be filled in for each record from the bound record list when an individual PDF document is generated.</span></span>
    - <span data-ttu-id="fa0cc-260">**ページ1: PDF ファイル** と **ページ N: PDF ファイル** 形式の要素が **出力: PDF 合併** 形式の要素の子であるため、入力されたすべての PDF ドキュメントは 1 つの最終 PDF ドキュメントに統合されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-260">Because the **Page 1: PDF File** and **Page N: PDF File** format elements are children of the **Output: PDF Merger** format element, all PDF documents that are filled in will be merged into a single final PDF document.</span></span>
    - <span data-ttu-id="fa0cc-261">**ページング. ページ 1** と **ページング. ページ N** のデータ ソースは、**ページング. ページ** のデータ ソースからレコードのフィルタとして構成されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-261">The **Paging.Page1** and **Paging.PageN** data sources are configured as filters of records from the **Paging.Pages** data source.</span></span> <span data-ttu-id="fa0cc-262">このデータ ソースは、外部取引トランザクションのセット全体をバッチに分割するようにコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-262">This data source is configured to split the whole set of foreign trade transactions into batches.</span></span> <span data-ttu-id="fa0cc-263">バッチごとに、最大 42 レコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-263">Each batch contains up to 42 records.</span></span> <span data-ttu-id="fa0cc-264">トランザクションをバッチに分割するには、次の ER 式を使用します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-264">The following ER expression is used to split the transactions into batches:</span></span>

        <span data-ttu-id="fa0cc-265">SPLITLIST(Totals.CommodityRecord,42)</span><span class="sxs-lookup"><span data-stu-id="fa0cc-265">SPLITLIST(Totals.CommodityRecord,42)</span></span>

    - <span data-ttu-id="fa0cc-266">**ページング. ページ** のデータソースには、バッチに含まれている各レコードの詳細を返す **ページング. ページ. 列挙型** 要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-266">The **Paging.Pages** data source contains the **Paging.Pages.Enumerated** element that returns the details of each record that is included in a batch.</span></span> <span data-ttu-id="fa0cc-267">この詳細には、現在のバッチにおけるレコード シーケンスが含まれています (**ページング. ページ. 列挙型. 番号** フィールド)。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-267">These details include the record's sequence in the current batch (the **Paging.Pages.Enumerated.Number** field).</span></span> <span data-ttu-id="fa0cc-268">**ページング. ページ. 列挙型. 番号** フィールドは、**PDF フィールド** の形式要素にある **名前** 式で使用され、バッチのトランザクション番号に基づいて動的にフィールド名を生成します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-268">The **Paging.Pages.Enumerated.Number** field is used in the **Name** expression of **PDF Field** format elements to dynamically generate a field name that is based on the transaction number in a batch.</span></span> <span data-ttu-id="fa0cc-269">生成されたフィールド名は、使用される PDF テンプレートに正しい PDF フィールドを入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-269">The field name that is generated is then used to fill in the correct PDF field in the PDF template that is used.</span></span>
    - <span data-ttu-id="fa0cc-270">**PDF グループ** タイプの **アウトプット \> ページ N \> 詳細 2** の形式要素は、**レコード リスト** タイプの **ページング. ページ N. 列挙型** データ ソース (または **\@. 列挙型** であり **相対パス** ビュー モードが使用されている場合) にバインドされます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-270">The **Output \> Page N \> Details 2** format element of the **PDF Group** type is bound to the **Paging.PageN.Enumerated** data source (or **\@.Enumerated** if the **Relative path** view mode is used) of the **Record list** type.</span></span> <span data-ttu-id="fa0cc-271">したがって、実行時に PDF グループの入れ子になった要素が、バインドされたレコード リストのレコードごとに入力されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-271">Therefore, at run time, the nested elements of this PDF group will be filled in for each record from the bound record list.</span></span> <span data-ttu-id="fa0cc-272">このようにして、個々の PDF ラインは、**ページング. ページ N. 列挙型** リストの各 N 番目の 42 のレコードに対して以下のフィールドが入力されている場合、実質的には生成されます: 日付 N、方向 N、商品 N など。したがって、この点において **フィールド グループ** 形式要素の動作は **XML \> シーケンス** および **テキスト \> シーケンス** の形式要素の動作に似ています。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-272">In this way, individual PDF lines are virtually generated when for each Nth of 42 records of the **Paging.PageN.Enumerated** list the following PDF fields are filled in: Date N, Direction N, Commodity N, etc. Therefore, in this respect, the behavior of this **Field group** format element resembles the behavior of the **XML \> Sequence** and **Text \> Sequence** format elements.</span></span>

3. <span data-ttu-id="fa0cc-273">ツリーで、**アウトプット \> ページ N \> 詳細 2** を展開します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-273">In the tree, expand **Output \> Page N \> Details2**.</span></span>
4. <span data-ttu-id="fa0cc-274">ツリーで、**アウトプット \> ページ N \> 詳細 2 \> PageFooter** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-274">In the tree, select **Output \> Page N \> Details2 \> PageFooter**.</span></span>

    <span data-ttu-id="fa0cc-275">この形式要素の **名前** 属性は、**PageFooter** として定義されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-275">Notice that the **Name** attribute of this format element is defined as **PageFooter**.</span></span> <span data-ttu-id="fa0cc-276">また、書式要素の **名前** の式が空であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-276">Also notice that the **Name** expression of the format element is empty.</span></span>

5. <span data-ttu-id="fa0cc-277">ツリーで、**アウトプット \> ページ N \> 詳細 2 \> 訂正 1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-277">In the tree, select **Output \> Page N \> Details2 \> Correction 1**.</span></span>

    <span data-ttu-id="fa0cc-278">この形式要素の **名前** 属性は、**訂正 1** として定義されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-278">Notice that the **Name** attribute of this format element is defined as **Correction 1**.</span></span> <span data-ttu-id="fa0cc-279">また、書式要素の **名前** 式は、**ページング .FldName(「訂正」、\@. 番号)** で定義されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-279">Also notice that the **Name** expression of the format element is defined as **Paging.FldName("Correction",\@.Number)**.</span></span>

![マッピングが選択されている形式デザイナー](media/rcs-ger-filloutpdf-reviewformat2.png)

<span data-ttu-id="fa0cc-281">**フィールド** の形式要素は、親の **PDF ファイル** 形式要素のテンプレートとして定義される入力可能な PDF ドキュメントの個々のフィールドに入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-281">Note that the **Field** format element is used to fill in an individual field of a fillable PDF document that is defined as a template of the parent **PDF File** format element.</span></span> <span data-ttu-id="fa0cc-282">**PDF ファイル** 形式要素またはネストした要素のバインディングは、ネストした要素がある場合、対応する PDF フィールドに入力された値が指定されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-282">The binding of the **PDF File** format element or its nested elements, if it has any nested elements, specifies the value that is entered in corresponding PDF fields.</span></span> <span data-ttu-id="fa0cc-283">個々の形式要素によって入力される PDF フィールドを指定するには、**フィールド** 形式要素のさまざまなプロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-283">Different properties of the **Field** format element can be used to specify which PDF field is filled in by an individual format element:</span></span>

- <span data-ttu-id="fa0cc-284">**形式** タブでの形式要素の **名前** 属性</span><span class="sxs-lookup"><span data-stu-id="fa0cc-284">On the **Format** tab, the **Name** attribute of the format element</span></span>
- <span data-ttu-id="fa0cc-285">**マッピング** タブでの形式要素の **名前** 式</span><span class="sxs-lookup"><span data-stu-id="fa0cc-285">On the **Mapping** tab, the **Name** expression of the format element</span></span>

<span data-ttu-id="fa0cc-286">**フィールド** 形式要素に対して両方のプロパティが省略可能であるため、次の規則を適用して目的の PDF フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-286">Because both properties are optional for a **Field** format element, the following rules are applied to specify the target PDF field:</span></span>

- <span data-ttu-id="fa0cc-287">**名前** 属性が空白の場合、**名前** 式が実行時に空の文字列を返すと、実行時に例外がスローされ、PDF ドキュメントに入力するために使用されている PDF テンプレートで PDF フィールドが見つからないことをユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-287">If the **Name** attribute is blank, and the **Name** expression returns an empty string at run time, an exception is thrown at run time to notify the user that a PDF field can't be found in the PDF template that is being used to fill in the PDF document.</span></span>
- <span data-ttu-id="fa0cc-288">**名前** 属性が定義され、**名前** 式が空白の場合、形式要素の **名前** 属性と同じ名前の PDF フィールドが入力されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-288">If the **Name** attribute is defined, and the **Name** expression is blank, the PDF field that has the same name as the **Name** attribute of the format element is filled in.</span></span>
- <span data-ttu-id="fa0cc-289">**名前** 属性が定義され、**名前** 式がコンフィギュレーションされている場合、形式要素の **名前** 式によって返される値と同じ名前の PDF フィールドが入力されます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-289">If the **Name** attribute is defined, and the **Name** expression is configured, the PDF field that the same name as the value that is returned by the **Name** expression of the format element is filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="fa0cc-290">PDF チェック ボックスは、次の方法で選択したとおりに入力できます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-290">A PDF check box can be filled in as selected in the following ways:</span></span>
>
> - <span data-ttu-id="fa0cc-291">対応する **フィールド** 形式要素が、**True** 値を持つ **ブール値** データ タイプのデータ ソース フィールドに連結されている場合</span><span class="sxs-lookup"><span data-stu-id="fa0cc-291">When the corresponding **Field** format element is bound to a data source field of the **Boolean** data type that has the **True** value</span></span>
> - <span data-ttu-id="fa0cc-292">対応する **フィールド** 形式要素に、**1**、**True**、または **はい** のテキスト値を持つデータ ソース フィールドに連結され入れ子になった **文字列** 形式要素が含まれる場合</span><span class="sxs-lookup"><span data-stu-id="fa0cc-292">When the corresponding **Field** format element contains a nested **String** format element that is bound to a data source field that has a text value of **1**, **True**, or **Yes**</span></span>

## <a name="run-the-format-configuration"></a><span data-ttu-id="fa0cc-293">形式のコンフィギュレーションを実行</span><span class="sxs-lookup"><span data-stu-id="fa0cc-293">Run the format configuration</span></span>

### <a name="import-the-format-configuration"></a><span data-ttu-id="fa0cc-294">書式設定のコンフィギュレーションのインポート</span><span class="sxs-lookup"><span data-stu-id="fa0cc-294">Import the format configuration</span></span>

<span data-ttu-id="fa0cc-295">次に、**イントラスタット (Excel からインポート)** サンプル ER 形式を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-295">Next, you will load the **Intrastat (import from Excel)** sample ER format.</span></span> <span data-ttu-id="fa0cc-296">この形式は、ユーザーが選択した Microsoft Excel ブックを解析するために作成され、対外貿易トランザクションをシミュレートします。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-296">This format is designed to parse a user-selected Microsoft Excel workbook that simulates foreign trade transactions.</span></span>

1. <span data-ttu-id="fa0cc-297">**コンフィギュレーション** ページで、**交換 \> XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-297">On the **Configurations** page, select **Exchange \> Load from XML file**.</span></span>
2. <span data-ttu-id="fa0cc-298">**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-298">Select **Browse**.</span></span> <span data-ttu-id="fa0cc-299">前提条件として事前にダウンロードした **イントラスタット (Excel からインポート). バージョン .1.1.xml** ファイルに移動して選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-299">Navigate to and select the **Intrastat (import from Excel).version.1.1.xml** file that you downloaded earlier as a prerequisite.</span></span>
3. <span data-ttu-id="fa0cc-300">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-300">Select **OK**.</span></span>
4. <span data-ttu-id="fa0cc-301">ツリーで、**イントラスタット モデル \> イントラスタット (Excel からインポート)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-301">In the tree, select **Intrastat model \> Intrastat (import from Excel)**.</span></span>
5. <span data-ttu-id="fa0cc-302">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-302">Select **Edit**.</span></span>
6. <span data-ttu-id="fa0cc-303">**モデル マッピングの既定値** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-303">Set the **Default for model mapping** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="fa0cc-304">事前に、**イントラスタット モデル** コンフィギュレーションに対して **モデル マッピングの規定値** オプションを **はい** に設定した場合、または **イントラスタット モデル** コンフィギュレーションの下に入れ子になった別のコンフィギュレーションの場合、オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-304">If you previously set the **Default for model mapping** option to **Yes** for the **Intrastat model** configuration or another configuration that is nested under the **Intrastat model** configuration, set this option to **No**.</span></span>

    <span data-ttu-id="fa0cc-305">**モデル マッピングの規定値** が **はい** に設定されている場合、インポートされた **イントラスタット (Excel からインポート)** ER 形式は、**イントラスタット レポート (PDF)** 形式コンフィギュレーションの規定値のデータ ソースとして割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-305">When the **Default for model mapping** option is set to **Yes**, the imported **Intrastat (import from Excel)** ER format is assigned as the default data source for the **Intrastat report (PDF)** format configuration.</span></span> <span data-ttu-id="fa0cc-306">その後、**イントラスタット レポート (PDF)** 形式のコンフィギュレーションが実行されると、**イントラスタット (Excel からインポート)** ER 形式によって解析された Excel ブックの内容により、外部取引トランザクションがシミュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-306">Then, when the **Intrastat report (PDF)** format configuration is run, the content of the Excel workbook that is parsed by the **Intrastat (import from Excel)** ER format will simulate foreign trade transactions that must be reported.</span></span> <span data-ttu-id="fa0cc-307">次の図は、Excel ブックの例を示します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-307">The following illustration shows an example of an Excel workbook.</span></span>

    ![サンプル データが含まれる Excel ブック](media/rcs-ger-filloutpdf-excelworkbook.png)

### <a name="run-the-format-configuration"></a><span data-ttu-id="fa0cc-309">形式のコンフィギュレーションを実行</span><span class="sxs-lookup"><span data-stu-id="fa0cc-309">Run the format configuration</span></span>

1. <span data-ttu-id="fa0cc-310">**コンフィギュレーション** ページのツリーで、**イントラスタット モデル \> イントラスタット レポート (PDF)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-310">On the **Configurations** page, in the tree, select **Intrastat model \> Intrastat report (PDF)**.</span></span>
2. <span data-ttu-id="fa0cc-311">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-311">Select **Run**.</span></span>
3. <span data-ttu-id="fa0cc-312">**参照** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-312">Select **Browse**.</span></span> <span data-ttu-id="fa0cc-313">前提条件として事前にダウンロードした **イントラスタット サンプル データ .xlsx** ファイルに移動して選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-313">Navigate to and select the **Intrastat sample data.xlsx** file that you downloaded earlier as a prerequisite.</span></span>
4. <span data-ttu-id="fa0cc-314">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-314">Select **OK**.</span></span>
5. <span data-ttu-id="fa0cc-315">**レポートの方向** フィールドで、**両方** を選択して、インポートした Excel ブックのすべてのトランザクションを、生成される PDF レポートに入力します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-315">In the **Report direction** field, select **Both** to fill in all transactions from the imported Excel workbook in the PDF report that is generated.</span></span>
6. <span data-ttu-id="fa0cc-316">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-316">Select **OK**.</span></span>
7. <span data-ttu-id="fa0cc-317">生成された PDF ドキュメントを確認します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-317">Review the PDF document that is generated.</span></span>

<span data-ttu-id="fa0cc-318">次の図で、生成されるレポートの最初のページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-318">The follow illustration shows an example of the first page of the report that is generated.</span></span>

![生成されたレポートの最初のページ](media/rcs-ger-filloutpdf-generatedreport.png)

<span data-ttu-id="fa0cc-320">次の図で、生成されるレポートの別のページの例を示します。</span><span class="sxs-lookup"><span data-stu-id="fa0cc-320">The follow illustration shows an example of another page of the report that is generated.</span></span>

![生成されたレポートの別のページ](media/rcs-ger-filloutpdf-generatedreport2.png)

## <a name="additional-resources"></a><span data-ttu-id="fa0cc-322">追加リソース</span><span class="sxs-lookup"><span data-stu-id="fa0cc-322">Additional resources</span></span>

- [<span data-ttu-id="fa0cc-323">OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="fa0cc-323">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>](tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="fa0cc-324">Word 形式でレポートを生成するための ER コンフィギュレーションのデザイン</span><span class="sxs-lookup"><span data-stu-id="fa0cc-324">Design ER configurations to generate reports in Word format</span></span>](tasks/er-design-configuration-word-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

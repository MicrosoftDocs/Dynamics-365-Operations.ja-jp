---
title: OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)
description: このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fcceb0e4d5f3bec54598515da0a5cbd8d11def3d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769858"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="f84a8-103">OPENXML 形式でレポートを生成する ER コンフィギュレーションを設計する (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="f84a8-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f84a8-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子ドキュメントを OPENXML 形式で生成するためのテンプレートを含む新しい電子申告 (ER) のコンフィギュレーションを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="f84a8-105">このコンフィギュレーションは、仕入先支払を処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="f84a8-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順は GBSI 会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="f84a8-107">これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f84a8-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="f84a8-108">テンプレートを作成するときにインポートされる Excel ファイルも必要です。</span><span class="sxs-lookup"><span data-stu-id="f84a8-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="f84a8-109">このファイルは[支払レポートのテンプレート](https://go.microsoft.com/fwlink/?linkid=862266) からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="f84a8-110">支払データ モデルのコンフィギュレーションをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f84a8-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="f84a8-111">ナビゲーション ウィンドウで、**モジュール > 組織の管理 > ワークスペース > 電子レポート**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="f84a8-112">一覧で、サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーをマークします。このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](er-configuration-provider-mark-it-active-2016-11.md) という手順を最初に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f84a8-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="f84a8-113">**有効に設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-113">Select **Set active**.</span></span>
4. <span data-ttu-id="f84a8-114">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-114">Select **Repositories**.</span></span> <span data-ttu-id="f84a8-115">運営リソース タイプのリポジトリを、必要に応じて選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="f84a8-116">利用可能であれば、新しいリポジトリの作成に関する次の手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="f84a8-117">**追加**を選択してドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="f84a8-118">**構成リポジトリ タイプ**フィールドで、`Operations resourcesdd` を入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="f84a8-119">**レポジトリを作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="f84a8-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-120">Select **OK**.</span></span>
9. <span data-ttu-id="f84a8-121">**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-121">Select **Open**.</span></span>
10. <span data-ttu-id="f84a8-122">ツリーで、**支払モデル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="f84a8-123">**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-123">Select **Import**.</span></span> <span data-ttu-id="f84a8-124">このデータ モデルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="f84a8-124">Import this data model.</span></span> <span data-ttu-id="f84a8-125">これは、新しい形式のコンフィギュレーションでデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="f84a8-126">このコンフィギュレーションが既にインポートされている場合は、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="f84a8-127">**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-127">Select **Yes**.</span></span>
13. <span data-ttu-id="f84a8-128">電子レポートのページに戻るまで、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="f84a8-129">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="f84a8-129">Create a new format configuration</span></span>
1. <span data-ttu-id="f84a8-130">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="f84a8-131">ツリーで、**支払モデル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="f84a8-132">**コンフィギュレーションの作成**を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="f84a8-133">**新規**フィールドで、`Format based on data model PaymentModel` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="f84a8-134">PaymentModel のデータ モデルに基づく形式を作成します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="f84a8-135">**名前**フィールドに、`Sample worksheet report` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="f84a8-136">サンプル ワークシート レポート</span><span class="sxs-lookup"><span data-stu-id="f84a8-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="f84a8-137">**説明**フィールドで、`Sample worksheet report for vendors’ payments` を入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-137">In the **Description** field, type `Sample worksheet report for vendors’ payments`.</span></span> <span data-ttu-id="f84a8-138">仕入先の支払用サンプル ワークシート レポート。</span><span class="sxs-lookup"><span data-stu-id="f84a8-138">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="f84a8-139">**データ モデル定義**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="f84a8-140">**CustomerCreditTransferInitiation** の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="f84a8-141">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="f84a8-142">OPENXML ワークシート形式で新しいドキュメントを設計します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="f84a8-143">ツリーで、**Payment model\Sample worksheet report** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="f84a8-144">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f84a8-144">Select **Designer**.</span></span>
3. <span data-ttu-id="f84a8-145">アクション ウィンドウで、**インポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="f84a8-146">**Excel からインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="f84a8-147">**添付ファイル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-147">Select **Attachments**.</span></span> <span data-ttu-id="f84a8-148">既存の Excel ドキュメントをテンプレートとして添付します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="f84a8-149">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-149">Select **New**.</span></span>
7. <span data-ttu-id="f84a8-150">**ファイル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-150">Select **File**.</span></span> <span data-ttu-id="f84a8-151">既存の Excel ファイルをポイントします。</span><span class="sxs-lookup"><span data-stu-id="f84a8-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="f84a8-152">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-152">Close the page.</span></span>
9. <span data-ttu-id="f84a8-153">**テンプレート**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="f84a8-154">テンプレートとして使用する Excel の添付ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="f84a8-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-155">Select **OK**.</span></span> <span data-ttu-id="f84a8-156">ER 形式のコンポーネントが、MS Excel ドキュメント参照の構造 (名前付き範囲) に基づく設計形式で作成されていることに注意して下さい。</span><span class="sxs-lookup"><span data-stu-id="f84a8-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="f84a8-157">通貨コード別の合計を計算する新しいデータ ソースを作成します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="f84a8-158">**マッピング**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="f84a8-159">**ルートの追加**を選択して、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="f84a8-160">ツリーで、**Functions\Group by** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="f84a8-161">**名前**フィールドに、`PaymentByCurrency` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="f84a8-162">**次の基準でグループを編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="f84a8-163">ツリーで、**モデル**を展開し、**model\Payments** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="f84a8-164">**フィールドを追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="f84a8-165">**グループ化の対象**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-165">Select **What to group**.</span></span>
9. <span data-ttu-id="f84a8-166">ツリーで、**model\Payments** を展開し、**model\Payments\Currency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="f84a8-167">**フィールドを追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="f84a8-168">**グループ化されたフィールド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="f84a8-169">ツリーで、**model\Payments\Instructed Amount(InstructedAmount)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="f84a8-170">**フィールドを追加**を選択し、**集計フィールド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="f84a8-171">**方法**フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="f84a8-172">**合計集計**機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="f84a8-173">**名前**フィールドに、`TotalInstructuredAmount` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="f84a8-174">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-174">Select **Save**.</span></span>
17. <span data-ttu-id="f84a8-175">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-175">Close the page.</span></span>
18. <span data-ttu-id="f84a8-176">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="f84a8-177">データ ソースへの形式のコンポーネントのマッピング</span><span class="sxs-lookup"><span data-stu-id="f84a8-177">Map format components to data sources</span></span>
1. <span data-ttu-id="f84a8-178">ツリーで、**model\Payments\Initiating Party(InitiatingParty)\Name** および **Excel\ReportHeader\CompanyName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="f84a8-179">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-179">Select **Bind**.</span></span>
3. <span data-ttu-id="f84a8-180">ツリーで、**model\Payments\Creditor\Identification\Source ID(SourceID)** および **Excel\PaymLines\VendAccountName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="f84a8-181">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-181">Select **Bind**.</span></span>
5. <span data-ttu-id="f84a8-182">ツリーで、**model\Payments\Creditor\Name** および **Excel\PaymLines\VendName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="f84a8-183">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-183">Select **Bind**.</span></span>
7. <span data-ttu-id="f84a8-184">ツリーで、**model\Payments\Creditor Agent(CreditorAgent)\Name** および **Excel\PaymLines\Bank** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="f84a8-185">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-185">Select **Bind**.</span></span>
9. <span data-ttu-id="f84a8-186">ツリーで、**model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** および **Excel\PaymLines\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="f84a8-187">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-187">Select **Bind**.</span></span>
11. <span data-ttu-id="f84a8-188">ツリーで、**model\Payments\Creditor Account(CreditorAccount)\Identification\Number** および **Excel\PaymLines\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="f84a8-189">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-189">Select **Bind**.</span></span>
13. <span data-ttu-id="f84a8-190">ツリーで、**model\Payments\Instructed Amount(InstructedAmount)** および **Excel\PaymLines\Debit** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="f84a8-191">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-191">Select **Bind**.</span></span>
15. <span data-ttu-id="f84a8-192">ツリーで、**model\Payments\Currency** および **Excel\PaymLines\Currency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="f84a8-193">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-193">Select **Bind**.</span></span>
17. <span data-ttu-id="f84a8-194">ツリーで、**PaymentByCurrency\grouped\Currency** および **Excel\SummaryLines\SummaryCurrency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="f84a8-195">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-195">Select **Bind**.</span></span>
19. <span data-ttu-id="f84a8-196">ツリーで、**PaymentByCurrency\aggregated\TotalInstructuredAmount** および **Excel\SummaryLines\SummaryAmount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="f84a8-197">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-197">Select **Bind**.</span></span>
21. <span data-ttu-id="f84a8-198">ツリーで、**PaymentByCurrency** および **Excel\SummaryLines** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="f84a8-199">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-199">Select **Bind**.</span></span>
23. <span data-ttu-id="f84a8-200">ツリーで、**model\Payments** および **Excel\PaymLines** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="f84a8-201">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-201">Select **Bind**.</span></span>
25. <span data-ttu-id="f84a8-202">**保存**を選択し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="f84a8-203">支払処理用に作成されたコンフィギュレーションを使用する</span><span class="sxs-lookup"><span data-stu-id="f84a8-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="f84a8-204">**ステータスの変更**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-204">Select **Change status**.</span></span>
2. <span data-ttu-id="f84a8-205">**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-205">Select **Complete**.</span></span>
3. <span data-ttu-id="f84a8-206">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-206">Select **OK**.</span></span>
4. <span data-ttu-id="f84a8-207">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 支払設定 > 支払方法**の順で移動します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="f84a8-208">クイック フィルターを使用して、**支払方法**フィールドに **Electronic** 値でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="f84a8-209">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-209">Select **Edit**.</span></span>
7. <span data-ttu-id="f84a8-210">**ファイル形式**セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="f84a8-211">**一般的な電子申告**フィールドで、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="f84a8-212">**エクスポート形式のコンフィギュレーション**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="f84a8-213">**サンプル ワークシート レポート**のコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="f84a8-214">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-214">Select **Save**.</span></span>
11. <span data-ttu-id="f84a8-215">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f84a8-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="f84a8-216">支払仕訳帳の処理のテスト用に作成されたコンフィギュレーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="f84a8-217">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 支払 > 支払仕訳**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="f84a8-218">**新規**を選択して、新しい支払仕訳を作成します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="f84a8-219">**名前**フィールドで、**VendPay** と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="f84a8-220">**明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-220">Select **Lines**.</span></span>
5. <span data-ttu-id="f84a8-221">**口座**フィールドで、`GB_SI_000001` という値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="f84a8-222">**借方**を `1000` に設定します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="f84a8-223">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-223">Select **New**.</span></span>
8. <span data-ttu-id="f84a8-224">**口座**フィールドで、`GB_SI_000005` という値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="f84a8-225">**借方**を `2000` に設定します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="f84a8-226">**通貨**フィールドで、`EUR` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="f84a8-227">**相手勘定**フィールドで、`GBSI OPER` という値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="f84a8-228">**支払方法**フィールドで、`Electronic` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="f84a8-229">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-229">Select **Save**.</span></span>
14. <span data-ttu-id="f84a8-230">**支払の生成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="f84a8-231">**支払方法**フィールドで、`Electronic` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="f84a8-232">**ファイル名**フィールドに、`Payments` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="f84a8-233">**銀行口座**フィールドで、`GBSI OPER` と入力します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="f84a8-234">**OK** を選択し、もう一度 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="f84a8-235">この支払メッセージに使用される各通貨コードの支払明細行および合計の詳細を含む、作成されたワークシートを確認します。</span><span class="sxs-lookup"><span data-stu-id="f84a8-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


---
title: 詳細な口座調整のインポート プロセスの設定
description: 詳細な口座調整機能では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 Finance での銀行トランザクションに合わせて自動的に調整することができます。 この資料では、口座取引明細書のインポート機能を設定する方法について説明します。
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ca0001adfb73ab178a50e4346922273f0812c92
ms.sourcegitcommit: 4835acc3edacf8277937723d3f85a7875bd8de83
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2021
ms.locfileid: "5580944"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a><span data-ttu-id="a0d55-104">詳細な口座調整のインポート プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="a0d55-104">Set up the advanced bank reconciliation import process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0d55-105">詳細な口座調整機能では、電子口座取引明細書をインポートし、Dynamics 365 Finance での銀行トランザクションに合わせて自動的に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-105">The Advanced bank reconciliation feature lets you import electronic bank statements and automatically reconcile them with bank transactions in Dynamics 365 Finance.</span></span> <span data-ttu-id="a0d55-106">この資料では、口座取引明細書のインポート機能を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-106">This article explains how to set up the import functionality for your bank statements.</span></span> 

<span data-ttu-id="a0d55-107">口座取引明細書のインポートの設定は、電子口座取引明細書の形式によって異なります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-107">The setup for bank statement import varies, depending on the format of your electronic bank statement.</span></span> <span data-ttu-id="a0d55-108">Finance は、ISO20022、MT940、および BAI2 の 3 つの口座取引明細書の形式を包括的にサポートしています。</span><span class="sxs-lookup"><span data-stu-id="a0d55-108">Finance supports three bank statement formats out of the box: ISO20022, MT940, and BAI2.</span></span>

## <a name="set-time-zone-preference"></a><span data-ttu-id="a0d55-109">タイム ゾーンの基本設定</span><span class="sxs-lookup"><span data-stu-id="a0d55-109">Set time zone preference</span></span>
<span data-ttu-id="a0d55-110">口座取引明細書のインポート設定をコンフィギュレーションする場合、インポートされる口座取引明細書ファイル内の日時データのタイム ゾーンを考慮することが重要です。</span><span class="sxs-lookup"><span data-stu-id="a0d55-110">When you configure the bank statement import settings, it can be important to consider the time zone of the date-time data within the bank statement files that will be imported.</span></span> <span data-ttu-id="a0d55-111">既定では、任意の日付と時刻の値は協定世界時 (UTC) に既に含まれていると仮定されるため、データのインポート時にタイム ゾーン変換は適用されません。</span><span class="sxs-lookup"><span data-stu-id="a0d55-111">The default is to assume any date and time values are already in Coordinated Universal Time (UTC) and so no time zone conversion will be applied when you import the data.</span></span> 

<span data-ttu-id="a0d55-112">データのインポートに使用するタイム ゾーンを指定するためのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-112">There is an option available to specify a time zone to use for importing data.</span></span> <span data-ttu-id="a0d55-113">このオプションは、各 **ソース データ形式の詳細** ページの **タイム ゾーンの基本設定** フィールド (**データ管理ワークスペース > データ ソースの構成 > データ形式の選択 > 地域の設定** クイック タブ) で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a0d55-113">This option is available in the **Time zone preference** field on each **Source data format details** page (**Data management workspace > Configure data sources > Select a data format > Regional settings** FastTab).</span></span> <span data-ttu-id="a0d55-114">入力したこのタイム ゾーンの基本設定は、そのソース データ形式を使用するすべてのインポートに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-114">This time zone preference you enter will apply to all the imports that use that source data format.</span></span> <span data-ttu-id="a0d55-115">複数のタイム ゾーンからデータをインポートするために必要な数のデータ ソース形式を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-115">You can create as many data source formats as needed for importing data from multiple time zones.</span></span>  

<span data-ttu-id="a0d55-116">このタイム ゾーンは、ユーザーまたは会社のタイム ゾーンとは異なる場合があるため、日時データが使用しているタイム ゾーンを明確にしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-116">This time zone might not be the same as a user’s or company’s time zone, so be sure to clarify what time zone the date and time data is using.</span></span> <span data-ttu-id="a0d55-117">タイム ゾーンの基本設定を設定する際には、次の点を考慮することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-117">We recommend that you consider the following points when setting a time zone preference.</span></span> 

 - <span data-ttu-id="a0d55-118">タイム ゾーンの基本設定は、そのソース データ形式を使用しているすべてのインポートに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-118">The time zone preference will apply to all imports using that source data format.</span></span> <span data-ttu-id="a0d55-119">複数のタイム ゾーンからデータのインポートを処理するために必要な数のデータ ソース形式を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-119">You can create as many data source formats as needed to handle importing data from multiple time zones.</span></span> 
 
 - <span data-ttu-id="a0d55-120">タイム ゾーンの基本設定は、インポート ファイルの日時データのローカル タイム ゾーンである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-120">The time zone preference should be the local time zone of the date and time data in the import file.</span></span> 
 
 - <span data-ttu-id="a0d55-121">日時データのタイム ゾーンは、ユーザーまたは会社のタイム ゾーンとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-121">The time zone of the date and time data might not be the same as a user’s or company’s time zone.</span></span>
 
 - <span data-ttu-id="a0d55-122">ユーザーは、**ユーザー オプション** を使用して独自のタイム ゾーンを調整できます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-122">Users can adjust their own time zone using their **User options**.</span></span>

<span data-ttu-id="a0d55-123">次のアクションを使用すると、口座取引明細書をインポートする際に、起きる可能性のある日時の競合を最小限に抑えることができます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-123">Note that the following actions can help minimize potential date and time conflicts when you import bank statements.</span></span> 

 - <span data-ttu-id="a0d55-124">既に明細書がインポートされた銀行口座に関しては、タイム ゾーンの基本設定の変更を避けてください。</span><span class="sxs-lookup"><span data-stu-id="a0d55-124">Avoid changing the time zone preferences for any bank accounts that have already had statements imported.</span></span> <span data-ttu-id="a0d55-125">タイム ゾーンの基本設定を変更すると、タイム ゾーン調整により、既存の明細書に対する新しい明細書の順序に影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-125">Changing the time zone preference could impact the ordering of new statements relative to existing statements due to the time zone adjustment.</span></span> 
 
 - <span data-ttu-id="a0d55-126">選択したデータ ソース形式を使用するすべてのインポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-126">Review all the imports that use the selected data source format.</span></span> <span data-ttu-id="a0d55-127">その形式用に指定されたタイム ゾーンの基本設定は、その形式を使用するすべてのインポート プロジェクトに適用されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-127">The time zone preference specified for the format will apply to all the import projects that use that format.</span></span> <span data-ttu-id="a0d55-128">タイム ゾーンの基本設定の検証は、その形式を使用するすべてのインポート プロジェクトに対して適切です。</span><span class="sxs-lookup"><span data-stu-id="a0d55-128">Verify that the time zone preference is appropriate for all the import projects that use that format.</span></span>

## <a name="sample-files"></a><span data-ttu-id="a0d55-129">サンプル ファイル</span><span class="sxs-lookup"><span data-stu-id="a0d55-129">Sample files</span></span>
<span data-ttu-id="a0d55-130">すべての 3 つの形式には、電子口座取引明細書を元の形式から、Finance で使用できる形式に変換するファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="a0d55-130">For all three formats, you must have files that translate the electronic bank statement from the original format to a format that Finance can use.</span></span> <span data-ttu-id="a0d55-131">Microsoft Visual Studio のアプリケーション エクスプローラーの **リソース** ノードの下に必要なリソース ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-131">You can find the required resource files under the **Resources** node in Application Explorer in Microsoft Visual Studio.</span></span> <span data-ttu-id="a0d55-132">ファイルを見つけたら、1 つのわかる場所にコピーして、設定プロセス中に容易にアップロードできるようにします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-132">After you find the files, copy them to a single known location, so that you can more easily upload them during the setup process.</span></span>

| <span data-ttu-id="a0d55-133">リソース名</span><span class="sxs-lookup"><span data-stu-id="a0d55-133">Resource name</span></span>                                           | <span data-ttu-id="a0d55-134">ファイル名</span><span class="sxs-lookup"><span data-stu-id="a0d55-134">File name</span></span>                            |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="a0d55-135">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-135">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>              | <span data-ttu-id="a0d55-136">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-136">BAI2CSV-to-BAI2XML.xslt</span></span>              |
| <span data-ttu-id="a0d55-137">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-137">BankStmtImport\_BAI2XML\_to\_Reconciliation\_xslt</span></span>       | <span data-ttu-id="a0d55-138">BAI2XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-138">BAI2XML-to-Reconciliation.xslt</span></span>       |
| <span data-ttu-id="a0d55-139">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-139">BankStmtImport\_BankReconciliation\_to\_Composite\_xslt</span></span> | <span data-ttu-id="a0d55-140">BankReconciliation-to-Composite.xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-140">BankReconciliation-to-Composite.xslt</span></span> |
| <span data-ttu-id="a0d55-141">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-141">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span>   | <span data-ttu-id="a0d55-142">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-142">ISO20022XML-to-Reconciliation.xslt</span></span>   |
| <span data-ttu-id="a0d55-143">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-143">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>            | <span data-ttu-id="a0d55-144">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-144">MT940TXT-to-MT940XML.xslt</span></span>            |
| <span data-ttu-id="a0d55-145">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-145">BankStmtImport\_MT940XML\_to\_Reconciliation\_xslt</span></span>      | <span data-ttu-id="a0d55-146">MT940XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="a0d55-146">MT940XML-to-Reconciliation.xslt</span></span>      |
| <span data-ttu-id="a0d55-147">BankStmtImport\_SampleBankCompositeEntity\_xml</span><span class="sxs-lookup"><span data-stu-id="a0d55-147">BankStmtImport\_SampleBankCompositeEntity\_xml</span></span>          | <span data-ttu-id="a0d55-148">SampleBankCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="a0d55-148">SampleBankCompositeEntity.xml</span></span>        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="a0d55-149">口座取引明細書の形式と技術的な配置の例</span><span class="sxs-lookup"><span data-stu-id="a0d55-149">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="a0d55-150">詳細な口座調整のインポート ファイルの技術的な配置の定義、および 3 つの関連する口座取引明細書のサンプル ファイルの例を以下に示します。[インポート ファイルの例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="a0d55-150">Below are examples of the advanced bank reconciliation import file technical layout definitions and three related bank statement example files: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="a0d55-151">技術的なレイアウトの定義</span><span class="sxs-lookup"><span data-stu-id="a0d55-151">Technical layout definition</span></span>                             | <span data-ttu-id="a0d55-152">口座取引明細書のサンプル ファイル</span><span class="sxs-lookup"><span data-stu-id="a0d55-152">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="a0d55-153">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="a0d55-153">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="a0d55-154">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="a0d55-154">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="a0d55-155">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="a0d55-155">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="a0d55-156">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="a0d55-156">ISO20022StatementExample</span></span>](https://dmsstager3tx7y9x22.blob.core.windows.net/155d84ed-c250-48f3-b0b1-c5a431e7855b/iso20022-multiplestatements.xml?sv=2019-02-02&sr=b&sig=1bDx0f9SONFouCcwLNPhmFHNdxDOkaibNf5%2Btoj0f0A%3D&se=2021-03-11T01%3A05%3A41Z&sp=r)             |
| <span data-ttu-id="a0d55-157">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="a0d55-157">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="a0d55-158">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="a0d55-158">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a><span data-ttu-id="a0d55-159">ISO20022 口座取引明細書のインポートの設定</span><span class="sxs-lookup"><span data-stu-id="a0d55-159">Set up the import of ISO20022 bank statements</span></span>
<span data-ttu-id="a0d55-160">最初に、データ エンティティ フレームワークを使用して「ISO20022 口座取引明細書」の口座取引明細書の形式処理グループを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-160">First, you must define the bank statement format processing group for ISO20022 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="a0d55-161">**ワークスペース** &gt; **データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-161">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="a0d55-162">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-162">Click **Import**.</span></span>
3.  <span data-ttu-id="a0d55-163">**ISO20022** などの形式の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-163">Enter a name for the format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="a0d55-164">**ソース データ形式** フィールドを **XML-Element** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-164">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="a0d55-165">**エンティティ名** フィールドを **口座取引明細書** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-165">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="a0d55-166">インポート ファイルをアップロードするには、**アップロード** をクリックし、参照して先ほど保存した **SampleBankCompositeEntity.xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-166">To upload the import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="a0d55-167">口座取引明細書のエンティティがアップロードされ、マッピングが完了した後、エンティティの **マップの表示** アクションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-167">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="a0d55-168">口座取引明細書のエンティティは、4 つの別々のエンティティで構成される複合エンティティです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-168">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="a0d55-169">一覧で、**BankStatementDocumentEntity** を選択し、次に **マップの表示** アクションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-169">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="a0d55-170">**変換** タブで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-170">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="a0d55-171">シーケンス番号 1 で、**ファイルのアップロード** をクリックし, 先ほど保存した **ISO20022XML-to-Reconciliation.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-171">For sequence number 1, click **Upload file**, and select the **ISO20022XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="a0d55-172">**注記:** 変換ファイルは、標準形式で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-172">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="a0d55-173">銀行は多くの場合、この形式と異なるため、口座取引明細書の形式にマップする変換ファイルを更新する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a0d55-173">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. <span data-ttu-id="a0d55-174">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-174">Click **New**.</span></span>
12. <span data-ttu-id="a0d55-175">シーケンス番号 2 で、**ファイルのアップロード** をクリックし, 先ほど保存した **BankReconciliation-to-Composite.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-175">For sequence number 2, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
13. <span data-ttu-id="a0d55-176">**変換の適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-176">Click **Apply transforms**.</span></span>

<span data-ttu-id="a0d55-177">形式の処理グループを設定した後の次の手順は、「ISO20022 口座取引明細書」の口座取引明細書の形式ルールを定義することです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-177">After the format processing group is set up, the next step is to define the bank statement format rules for ISO20022 bank statements.</span></span>

1.  <span data-ttu-id="a0d55-178">**現金および銀行管理** &gt; **設定** &gt; **詳細な口座調整の設定** &gt; **口座取引明細書の形式** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-178">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="a0d55-179">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-179">Click **New**.</span></span>
3.  <span data-ttu-id="a0d55-180">**ISO20022** のように明細書の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-180">Specify a statement format, such as **ISO20022**.</span></span>
4.  <span data-ttu-id="a0d55-181">形式の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-181">Enter a name for the format.</span></span>
5.  <span data-ttu-id="a0d55-182">**処理グループ** フィールドを **ISO20022** などの先ほど定義したグループに設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-182">Set the **Processing group** field to the group that you defined earlier, such as **ISO20022**.</span></span>
6.  <span data-ttu-id="a0d55-183">**XML ファイル** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-183">Select the **XML file** check box.</span></span>

<span data-ttu-id="a0d55-184">最後の手順は、詳細な口座調整を有効にし、銀行口座の明細書の形式を設定することです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-184">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="a0d55-185">**現金および銀行管理** &gt; **銀行口座** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-185">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="a0d55-186">銀行口座を選択し、ファイルを開いて詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-186">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="a0d55-187">**調整** タブで、**詳細な口座調整** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-187">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="a0d55-188">**明細書形式** フィールドを **ISO20022** などの先ほど作成した形式に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-188">Set the **Statement format** field to the format that you created earlier, such as **ISO20022**.</span></span>

## <a name="set-up-the-import-of-mt940-bank-statements"></a><span data-ttu-id="a0d55-189">MT940 口座取引明細書のインポートの設定</span><span class="sxs-lookup"><span data-stu-id="a0d55-189">Set up the import of MT940 bank statements</span></span>
<span data-ttu-id="a0d55-190">最初に、データ エンティティ フレームワークを使用して、「MT940 口座取引明細書」の口座取引明細書の形式処理グループを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-190">First, you must define the bank statement format processing group for MT940 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="a0d55-191">**ワークスペース** &gt; **データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-191">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="a0d55-192">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-192">Click **Import**.</span></span>
3.  <span data-ttu-id="a0d55-193">**MT940** などの形式の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-193">Enter a name for the format, such as **MT940**.</span></span>
4.  <span data-ttu-id="a0d55-194">**ソース データ形式** フィールドを **XML-Element** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-194">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="a0d55-195">**エンティティ名** フィールドを **口座取引明細書** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-195">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="a0d55-196">インポート ファイルをアップロードするには、**アップロード** をクリックし、次に参照して先ほど保存した **SampleBankCompositeEntity.xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-196">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="a0d55-197">口座取引明細書のエンティティがアップロードされ、マッピングが完了した後、エンティティの **マップの表示** アクションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-197">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="a0d55-198">口座取引明細書のエンティティは、4 つの別々のエンティティで構成される複合エンティティです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-198">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="a0d55-199">一覧で、**BankStatementDocumentEntity** を選択し、次に **マップの表示** アクションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-199">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="a0d55-200">**変換** タブで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-200">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="a0d55-201">シーケンス番号 1 で、**ファイルのアップロード** をクリックし、先ほど保存した **MT940TXT-to-MT940XML.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-201">For sequence number 1, click **Upload file**, and select the **MT940TXT-to-MT940XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="a0d55-202">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-202">Click **New**.</span></span>
12. <span data-ttu-id="a0d55-203">シーケンス番号 2 で、**ファイルのアップロード** をクリックし、先ほど保存した **MT940XML-to-Reconciliation.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-203">For sequence number 2, click **Upload file**, and select the **MT940XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="a0d55-204">**注記:** 変換ファイルは、標準形式で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-204">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="a0d55-205">銀行は多くの場合、この形式と異なるため、口座取引明細書の形式にマップする変換ファイルを更新する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a0d55-205">Because banks often diverge from this format, you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. <span data-ttu-id="a0d55-206">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-206">Click **New**.</span></span>
14. <span data-ttu-id="a0d55-207">シーケンス番号 3 で、**ファイルのアップロード** をクリックし、先ほど保存した **BankReconciliation-to-Composite.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-207">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="a0d55-208">**変換の適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-208">Click **Apply transforms**.</span></span>

<span data-ttu-id="a0d55-209">形式の処理グループを設定したら、次に、「MT940 口座取引明細書」の口座取引明細書の形式ルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-209">After the format processing group is set up, the next step is to define the bank statement format rules for MT940 bank statements.</span></span>

1.  <span data-ttu-id="a0d55-210">**現金および銀行管理** &gt; **設定** &gt; **詳細な口座調整の設定** &gt; **口座取引明細書の形式** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-210">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="a0d55-211">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-211">Click **New**.</span></span>
3.  <span data-ttu-id="a0d55-212">**MT940** などの明細書の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-212">Specify a statement format, such as **MT940**.</span></span>
4.  <span data-ttu-id="a0d55-213">形式の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-213">Enter a name for the format.</span></span>
5.  <span data-ttu-id="a0d55-214">**処理グループ** フィールドを **MT940** などの先ほど定義したグループに設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-214">Set the **Processing group** field to the group that you defined earlier, such as **MT940**.</span></span>
6.  <span data-ttu-id="a0d55-215">**ファイル タイプ** フィールドを **txt** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-215">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="a0d55-216">最後の手順は、詳細な口座調整を有効にし、銀行口座の明細書の形式を設定することです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-216">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="a0d55-217">**現金および銀行管理** &gt; **銀行口座** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-217">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="a0d55-218">銀行口座を選択し、ファイルを開いて詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-218">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="a0d55-219">**調整** タブで、**詳細な口座調整** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-219">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="a0d55-220">選択内容、および詳細な口座調整を有効にしたことを確認した時点で、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-220">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="a0d55-221">**明細書形式** フィールドを **MT940** などの先ほど作成した形式に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-221">Set the **Statement format** field to the format that you created earlier, such as **MT940**.</span></span>

## <a name="set-up-the-import-of-bai2-bank-statements"></a><span data-ttu-id="a0d55-222">BAI2 口座取引明細書のインポートの設定</span><span class="sxs-lookup"><span data-stu-id="a0d55-222">Set up the import of BAI2 bank statements</span></span>
<span data-ttu-id="a0d55-223">最初に、データ エンティティ フレームワークを使用して「BAI2 口座取引明細書」の口座取引明細書の形式処理グループを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0d55-223">First, you must define the bank statement format processing group for BAI2 bank statements by using the data entity framework.</span></span>

1.  <span data-ttu-id="a0d55-224">**ワークスペース** &gt; **データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-224">Go to **Workspaces** &gt; **Data management**.</span></span>
2.  <span data-ttu-id="a0d55-225">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-225">Click **Import**.</span></span>
3.  <span data-ttu-id="a0d55-226">**BAI2** などの形式の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-226">Enter a name for the format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="a0d55-227">**ソース データ形式** フィールドを **XML-Element** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-227">Set the **Source data format** field to **XML-Element**.</span></span>
5.  <span data-ttu-id="a0d55-228">**エンティティ名** フィールドを **口座取引明細書** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-228">Set the **Entity name** field to **Bank statements**.</span></span>
6.  <span data-ttu-id="a0d55-229">インポート ファイルをアップロードするには、**アップロード** をクリックし、次に参照して先ほど保存した **SampleBankCompositeEntity.xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-229">To upload import files, click **Upload**, and then browse to select the **SampleBankCompositeEntity.xml** file that you saved earlier.</span></span>
7.  <span data-ttu-id="a0d55-230">口座取引明細書のエンティティがアップロードされ、マッピングが完了した後、エンティティの **マップの表示** アクションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-230">After the Bank statements entity is uploaded and the mapping is completed, click the **View map** action for the entity.</span></span>
8.  <span data-ttu-id="a0d55-231">口座取引明細書のエンティティは、4 つの別々のエンティティで構成される複合エンティティです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-231">The Bank statements entity is a composite entity that consists of four separate entities.</span></span> <span data-ttu-id="a0d55-232">一覧で、**BankStatementDocumentEntity** を選択し、次に **マップの表示** アクションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-232">In the list, select **BankStatementDocumentEntity**, and then click the **View map** action.</span></span>
9.  <span data-ttu-id="a0d55-233">**変換** タブで、**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-233">On the **Transformations** tab, click **New**.</span></span>
10. <span data-ttu-id="a0d55-234">シーケンス番号 1 で、**ファイルのアップロード** をクリックし、先ほど保存した **BAI2CSV-to-BAI2XML.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-234">For sequence number 1, click **Upload file**, and select the **BAI2CSV-to-BAI2XML.xslt** file that you saved earlier.</span></span>
11. <span data-ttu-id="a0d55-235">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-235">Click **New**.</span></span>
12. <span data-ttu-id="a0d55-236">シーケンス番号 2 で、**ファイルのアップロード** をクリックし、先ほど保存した **BAI2XML-to-Reconciliation.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-236">For sequence number 2, click **Upload file**, and select the **BAI2XML-to-Reconciliation.xslt** file that you saved earlier.</span></span> <span data-ttu-id="a0d55-237">**注記:** 変換ファイルは、標準形式で作成されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-237">**Note:** Transformation files are built for the standard format.</span></span> <span data-ttu-id="a0d55-238">銀行は多くの場合、この形式と異なるため、口座取引明細書の形式にマップする変換ファイルを更新する必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a0d55-238">Because banks often diverge from this format, and you may have to update the transformation file to map to your bank statement format.</span></span> <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. <span data-ttu-id="a0d55-239">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-239">Click **New**.</span></span>
14. <span data-ttu-id="a0d55-240">シーケンス番号 3 で、**ファイルのアップロード** をクリックし、先ほど保存した **BankReconciliation-to-Composite.xslt** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-240">For sequence number 3, click **Upload file**, and select the **BankReconciliation-to-Composite.xslt** file that you saved earlier.</span></span>
15. <span data-ttu-id="a0d55-241">**変換の適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-241">Click **Apply transforms**.</span></span>

<span data-ttu-id="a0d55-242">形式の処理グループを設定した後は、BAI2 口座取引明細書の口座取引明細書の形式のルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-242">After the format processing group is set up, the next step is to define the bank statement format rules for BAI2 bank statements.</span></span>

1.  <span data-ttu-id="a0d55-243">**現金および銀行管理** &gt; **設定** &gt; **詳細な口座調整の設定** &gt; **口座取引明細書の形式** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-243">Go to **Cash and bank management** &gt; **Setup** &gt; **Advanced bank reconciliation setup** &gt; **Bank statement format**.</span></span>
2.  <span data-ttu-id="a0d55-244">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-244">Click **New**.</span></span>
3.  <span data-ttu-id="a0d55-245">**BAI2** などの明細書の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-245">Specify a statement format, such as **BAI2**.</span></span>
4.  <span data-ttu-id="a0d55-246">形式の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-246">Enter a name for the format.</span></span>
5.  <span data-ttu-id="a0d55-247">**処理グループ** フィールドを **BAI2** などの先ほど定義したグループに設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-247">Set the **Processing group** field to the group that you defined earlier, such as **BAI2**.</span></span>
6.  <span data-ttu-id="a0d55-248">**ファイル タイプ** フィールドを **txt** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-248">Set the **File type** field to **txt**.</span></span>

<span data-ttu-id="a0d55-249">最後の手順は、詳細な口座調整を有効にし、銀行口座の明細書の形式を設定することです。</span><span class="sxs-lookup"><span data-stu-id="a0d55-249">The last step is to enable Advanced bank reconciliation and set the statement format on the bank account.</span></span>

1.  <span data-ttu-id="a0d55-250">**現金および銀行管理** &gt; **銀行口座** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-250">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="a0d55-251">銀行口座を選択し、ファイルを開いて詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-251">Select the bank account, and open it to view the details.</span></span>
3.  <span data-ttu-id="a0d55-252">**調整** タブで、**詳細な口座調整** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-252">On the **Reconciliation** tab, set the **Advanced bank reconciliation** option to **Yes**.</span></span>
4.  <span data-ttu-id="a0d55-253">選択内容、および詳細な口座調整を有効にしたことを確認した時点で、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-253">When you're prompted to confirm your selection and enable Advanced bank reconciliation, click **OK**.</span></span>
5.  <span data-ttu-id="a0d55-254">**明細書形式** フィールドを **BAI2** などの先ほど作成した形式に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-254">Set the **Statement format** field to the format that you created earlier, such as **BAI2**.</span></span>

## <a name="test-the-bank-statement-import"></a><span data-ttu-id="a0d55-255">口座取引明細書のインポートのテスト</span><span class="sxs-lookup"><span data-stu-id="a0d55-255">Test the bank statement import</span></span>
<span data-ttu-id="a0d55-256">最後の手順では、口座取引明細書がインポートできることをテストします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-256">The final step is to test that you can import your bank statement.</span></span>

1.  <span data-ttu-id="a0d55-257">**現金および銀行管理** &gt; **銀行口座** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-257">Go to **Cash and bank management** &gt; **Bank accounts**.</span></span>
2.  <span data-ttu-id="a0d55-258">詳細な口座調整機能が有効な銀行口座を選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-258">Select the bank account that Advanced bank reconciliation functionality is enabled for.</span></span>
3.  <span data-ttu-id="a0d55-259">**調整** タブで、**口座取引明細書** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-259">On the **Reconcile** tab, click **Bank statements**.</span></span>
4.  <span data-ttu-id="a0d55-260">**口座取引明細書** ページで、**明細書のインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-260">On the **Bank statement** page, click **Import statement**.</span></span>
5.  <span data-ttu-id="a0d55-261">**銀行口座** フィールドを選択した銀行口座に設定します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-261">Set the **Bank account** field to the selected bank account.</span></span> <span data-ttu-id="a0d55-262">**明細書形式** フィールドは、銀行口座の設定に基づいて自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-262">The **Statement format** field will be set automatically, based on the setting on the bank account.</span></span>
6.  <span data-ttu-id="a0d55-263">**参照** をクリックし、電子口座取引明細書ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-263">Click **Browse**, and select your electronic bank statement file.</span></span>
7.  <span data-ttu-id="a0d55-264">**アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a0d55-264">Click **Upload**.</span></span>
8.  <span data-ttu-id="a0d55-265">**OK** をクリックします</span><span class="sxs-lookup"><span data-stu-id="a0d55-265">Click **OK**.</span></span>

<span data-ttu-id="a0d55-266">インポートが成功した場合、明細書がインポートされたことを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a0d55-266">If the import is successful, you will receive a message that states that your statement was imported.</span></span> <span data-ttu-id="a0d55-267">インポートが失敗した場合、**データ管理** ワークスペースの **ジョブ履歴** セクションで、ジョブを検索します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-267">If the import wasn't successful, in the **Data management** workspace, in the **Job history** section, find the job.</span></span> <span data-ttu-id="a0d55-268">ジョブの **実行の詳細** をクリックして、**実行の要約** ページを開き、次に **実行ログの表示** をクリックしてインポート エラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="a0d55-268">Click **Execution details** for the job to open the **Execution summary** page, and then click **View execution log** to view the import errors.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

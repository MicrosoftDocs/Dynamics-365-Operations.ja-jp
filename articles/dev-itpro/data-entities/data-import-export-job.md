---
title: "データ インポート/エクスポート ジョブ"
description: "データ管理ワークスペースを使用して、データ インポート/エクスポート ジョブを作成して管理します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e79fcaa634c4b4eb601241d75da2f36f2455db4e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="data-import-and-export-jobs"></a><span data-ttu-id="47acc-103">データ インポート/エクスポート ジョブ</span><span class="sxs-lookup"><span data-stu-id="47acc-103">Data import and export jobs</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="47acc-104">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition でデータ インポート/エクスポート ジョブを管理して作成するには、**データ管理**ワークスペースを使用します。</span><span class="sxs-lookup"><span data-stu-id="47acc-104">To create and manage data import and export jobs in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you use the **Data management** workspace.</span></span> <span data-ttu-id="47acc-105">既定では、データ インポート/エクスポート プロセスにより、ターゲットのデータベースで各エンティティにステージング テーブルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-105">By default, the data import and export process creates a staging table for each entity in the target database.</span></span> <span data-ttu-id="47acc-106">ステージング テーブルにより、移動させる前にデータを確認、クリーンアップ、または変換できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-106">Staging tables let you verify, clean up, or convert data before you move it.</span></span>

## <a name="data-importexport-process"></a><span data-ttu-id="47acc-107">データ インポート/エクスポート プロセス</span><span class="sxs-lookup"><span data-stu-id="47acc-107">Data import/export process</span></span>
<span data-ttu-id="47acc-108">データをインポートまたはエクスポートする手順を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="47acc-108">Here are the steps to import or export data.</span></span>

1. <span data-ttu-id="47acc-109">次のタスクを完了するインポートまたはエクスポート ジョブを作成します。</span><span class="sxs-lookup"><span data-stu-id="47acc-109">Create an import or export job where you complete the following tasks:</span></span>

    - <span data-ttu-id="47acc-110">プロジェクト カテゴリを定義します。</span><span class="sxs-lookup"><span data-stu-id="47acc-110">Define the project category.</span></span>
    - <span data-ttu-id="47acc-111">インポートまたはエクスポートするエンティティを識別します。</span><span class="sxs-lookup"><span data-stu-id="47acc-111">Identify the entities to import or export.</span></span>
    - <span data-ttu-id="47acc-112">ジョブのデータ形式を設定します。</span><span class="sxs-lookup"><span data-stu-id="47acc-112">Set the data format for the job.</span></span>
    - <span data-ttu-id="47acc-113">論理グループ内で道理にかなった順序で処理されるように、エンティティに順序付けをします。</span><span class="sxs-lookup"><span data-stu-id="47acc-113">Sequence the entities, so that they are processed in logical groups and in an order that makes sense.</span></span>
    - <span data-ttu-id="47acc-114">ステージング テーブルを使用するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="47acc-114">Determine whether to use staging tables.</span></span>

2. <span data-ttu-id="47acc-115">ソース データとターゲット データが正しくマップされていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="47acc-115">Validate that the source data and target data are mapped correctly.</span></span>
3. <span data-ttu-id="47acc-116">インポート/エクスポート ジョブのセキュリティを確認します。</span><span class="sxs-lookup"><span data-stu-id="47acc-116">Verify the security for your import or export job.</span></span>
4. <span data-ttu-id="47acc-117">インポート/エクスポート ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="47acc-117">Run the import or export job.</span></span>
5. <span data-ttu-id="47acc-118">ジョブの履歴を確認して、期待どおりにジョブが実行されたことを検証します。</span><span class="sxs-lookup"><span data-stu-id="47acc-118">Validate that the job ran as expected by reviewing the job history.</span></span>
6. <span data-ttu-id="47acc-119">ステージング テーブルをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="47acc-119">Clean up the staging tables.</span></span>

<span data-ttu-id="47acc-120">このトピックの残りのセクションでは、プロセスの各ステップに関する詳細をさらに提供します。</span><span class="sxs-lookup"><span data-stu-id="47acc-120">The remaining sections of this topic provide more details about each step of the process.</span></span>

## <a name="create-an-import-or-export-job"></a><span data-ttu-id="47acc-121">インポートまたはエクスポート ジョブを作成する</span><span class="sxs-lookup"><span data-stu-id="47acc-121">Create an import or export job</span></span>
<span data-ttu-id="47acc-122">データ インポート/エクスポート ジョブは、1 回または複数回実行できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-122">A data import or export job can be run one time or many times.</span></span>

### <a name="define-the-project-category"></a><span data-ttu-id="47acc-123">プロジェクト カテゴリを定義する</span><span class="sxs-lookup"><span data-stu-id="47acc-123">Define the project category</span></span>
<span data-ttu-id="47acc-124">インポート/エクスポート ジョブにふさわしいプロジェクト カテゴリを選択する時間を取るようお勧めします。</span><span class="sxs-lookup"><span data-stu-id="47acc-124">We recommend that you take the time to select an appropriate project category for your import or export job.</span></span> <span data-ttu-id="47acc-125">プロジェクト カテゴリは、関連するジョブを管理するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="47acc-125">Project categories can help you manage related jobs.</span></span>

### <a name="identify-the-entities-to-import-or-export"></a><span data-ttu-id="47acc-126">インポートまたはエクスポートするエンティティを識別する</span><span class="sxs-lookup"><span data-stu-id="47acc-126">Identify the entities to import or export</span></span>
<span data-ttu-id="47acc-127">インポート/エクスポート ジョブに特定のエンティティを追加したり、適用するテンプレートを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-127">You can add specific entities to an import or export job or select a template to apply.</span></span> <span data-ttu-id="47acc-128">テンプレートは、ジョブにエンティティの一覧を入力します。</span><span class="sxs-lookup"><span data-stu-id="47acc-128">Templates fill a job with a list of entities.</span></span> <span data-ttu-id="47acc-129">[テンプレートの適用] オプションは、ジョブに名前を付けて保存した後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-129">The **Apply template** option is available after you give the job a name and save the job.</span></span>

### <a name="set-the-data-format-for-the-job"></a><span data-ttu-id="47acc-130">ジョブのデータ形式を設定する</span><span class="sxs-lookup"><span data-stu-id="47acc-130">Set the data format for the job</span></span>
<span data-ttu-id="47acc-131">エンティティを選択する時に、エクスポートまたはインポートするデータの形式を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-131">When you select an entity, you must select the format of the data that will be exported or imported.</span></span> <span data-ttu-id="47acc-132">[データ ソース設定] タイルを使用して、形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="47acc-132">You define formats by using the **Data sources setup** tile.</span></span> <span data-ttu-id="47acc-133">多くの組織は、デモ データ セットに既定で含まれている形式から開始します。</span><span class="sxs-lookup"><span data-stu-id="47acc-133">Many organizations start from the formats that are included by default in the demo data set.</span></span> <span data-ttu-id="47acc-134">これらの形式の一覧を以下に示します。</span><span class="sxs-lookup"><span data-stu-id="47acc-134">Here is a list of some of these formats:</span></span>

- <span data-ttu-id="47acc-135">AX (Microsoft Dynamics 365 for Finance and Operations, Enterprise edition で使用されているのと同じ形式でインポート/エクスポートする必要のあるデータ用)</span><span class="sxs-lookup"><span data-stu-id="47acc-135">AX (for data that must be imported or exported in the same format that is used for Microsoft Dynamics 365 for Finance and Operations, Enterprise edition)</span></span>
- <span data-ttu-id="47acc-136">ColonSeparated</span><span class="sxs-lookup"><span data-stu-id="47acc-136">ColonSeparated</span></span>
- <span data-ttu-id="47acc-137">CSV</span><span class="sxs-lookup"><span data-stu-id="47acc-137">CSV</span></span>
- <span data-ttu-id="47acc-138">Excel</span><span class="sxs-lookup"><span data-stu-id="47acc-138">Excel</span></span>
- <span data-ttu-id="47acc-139">パッケージ</span><span class="sxs-lookup"><span data-stu-id="47acc-139">Package</span></span>

### <a name="sequence-the-entities"></a><span data-ttu-id="47acc-140">エンティティに順序付けをする</span><span class="sxs-lookup"><span data-stu-id="47acc-140">Sequence the entities</span></span>
<span data-ttu-id="47acc-141">データ テンプレート、またはインポート/エクスポート ジョブで、エンティティに順序付けをすることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-141">Entities can be sequenced in a data template, or in import and export jobs.</span></span> <span data-ttu-id="47acc-142">1 つ以上のデータ エンティティが含まれるジョブを実行する場合、データ エンティティが正しく順序付けされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-142">When you run a job that contains more than one data entity, you must make sure that the data entities are correctly sequenced.</span></span> <span data-ttu-id="47acc-143">主にエンティティ間の機能依存関係に合うように、エンティティに順序付けします。</span><span class="sxs-lookup"><span data-stu-id="47acc-143">You sequence entities primarily so that you can address any functional dependencies among entities.</span></span> <span data-ttu-id="47acc-144">エンティティに機能依存関係がない場合は、並行インポートまたはエクスポートにスケジューリングできます。</span><span class="sxs-lookup"><span data-stu-id="47acc-144">If entities don’t have any functional dependencies, they can be scheduled for parallel import or export.</span></span>

#### <a name="execution-units-levels-and-sequences"></a><span data-ttu-id="47acc-145">実行単位、レベル、および順序</span><span class="sxs-lookup"><span data-stu-id="47acc-145">Execution units, levels, and sequences</span></span>
<span data-ttu-id="47acc-146">実行単位、実行単位のレベル、およびエンティティの順序はデータのエクスポートやインポートの順序をコントロールするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="47acc-146">The execution unit, level in the execution unit, and sequence of an entity help control the order that the data is exported or imported in.</span></span>

- <span data-ttu-id="47acc-147">異なる実行単位のエンティティは、並行処理されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-147">Entities in different execution units are processed in parallel.</span></span>
- <span data-ttu-id="47acc-148">各実行単位では、エンティティは同じレベルを持つ場合に並列処理されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-148">In each execution unit, entities are processed in parallel if they have the same level.</span></span>
- <span data-ttu-id="47acc-149">各レベルでは、そのレベルの順序番号に従ってエンティティが処理されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-149">In each level, entities are processed according to their sequence number in that level.</span></span>
- <span data-ttu-id="47acc-150">1 つのレベルが処理された後、次のレベルが処理されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-150">After one level has been processed, the next level is processed.</span></span>

#### <a name="resequencing"></a><span data-ttu-id="47acc-151">順序付け直し</span><span class="sxs-lookup"><span data-stu-id="47acc-151">Resequencing</span></span>
<span data-ttu-id="47acc-152">以下のような状況で、エンティティの順序付け直しを行なう場合があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-152">You might want to resequence your entities in the following situations:</span></span>

- <span data-ttu-id="47acc-153">すべての変更に 1 つのデータジョブだけを使用する場合、完全なジョブの実行時間を最適化するために、順序付け直しのオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-153">If only one data job is used for all your changes, you can use resequencing options to optimize the execution time for the full job.</span></span> <span data-ttu-id="47acc-154">これらの場合は、モジュールを表すのに実行単位、モジュールの機能領域を表すのにレベル、エンティティを表すのに順序を使用できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-154">In these cases, you can use the execution unit to represent the module, the level to represent the feature area in the module, and the sequence to represent the entity.</span></span> <span data-ttu-id="47acc-155">この方法を使用することで、複数のモジュールで並行作業できますが、1 つのモジュール内で順番に作業することもできます。</span><span class="sxs-lookup"><span data-stu-id="47acc-155">By using this approach, you can work across modules in parallel, but you can still work in sequence in a module.</span></span> <span data-ttu-id="47acc-156">並行工程が確実に成功するように、すべての依存関係を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-156">To help guarantee that parallel operations succeed, you must consider all dependencies.</span></span>
- <span data-ttu-id="47acc-157">複数のデータ ジョブを使用する場合は (たとえば、各モジュールに 1 つのジョブ)、優先順位を使用して、最適な実行のため、レベルおよびエンティティの順序に影響を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-157">If multiple data jobs are used (for example, one job for each module), you can use sequencing to affect the level and sequence of entities for optimal execution.</span></span>
- <span data-ttu-id="47acc-158">依存関係がまったくない場合は、最大の最適化のため、異なる実行単位でエンティティに順序付けをすることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-158">If there are no dependencies at all, you can sequence entities at different execution units for maximum optimization.</span></span>

<span data-ttu-id="47acc-159">[順序付け直し] メニューは、複数のエンティティが選択されている場合に使用可能です。</span><span class="sxs-lookup"><span data-stu-id="47acc-159">The **Resequencing** menu is available when multiple entities are selected.</span></span> <span data-ttu-id="47acc-160">実行単位、レベル、または順序オプションに基づいて、順序付け直しができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-160">You can resequence based on execution unit, level, or sequence options.</span></span> <span data-ttu-id="47acc-161">選択されたエンティティの順序付け直しの増分を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-161">You can set an increment to resequence the entities that have been selected.</span></span> <span data-ttu-id="47acc-162">各エンティティに選択されている単位やレベルや順序番号が、指定された増分で更新されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-162">The unit, level, and/or sequence number that is selected for each entity is updated by the specified increment.</span></span>

#### <a name="sorting"></a><span data-ttu-id="47acc-163">並べ替え</span><span class="sxs-lookup"><span data-stu-id="47acc-163">Sorting</span></span>
<span data-ttu-id="47acc-164">[並べ替え] オプションを使用して、エンティティ リストを連番で表示できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-164">Use can use the **Sort by** option to view the entity list in sequential order.</span></span>

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a><span data-ttu-id="47acc-165">ソース データとターゲット データが正しくマップされていることを検証する</span><span class="sxs-lookup"><span data-stu-id="47acc-165">Validate that the source data and target data are mapped correctly</span></span>
<span data-ttu-id="47acc-166">マッピングは、インポート、エクスポート ジョブの両方に適用される機能です。</span><span class="sxs-lookup"><span data-stu-id="47acc-166">Mapping is a function that applies to both import and export jobs.</span></span>

- <span data-ttu-id="47acc-167">インポート ジョブのコンテキストで、マッピングはソース ファイルのどの列がステージング テーブルの列になるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="47acc-167">In the context of an import job, mapping describes which columns in the source file become the columns in the staging table.</span></span> <span data-ttu-id="47acc-168">そのため、システムはソース ファイルのどの列のデータをステージング テーブルのどの列にコピーする必要があるかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-168">Therefore, the system can determine which column data in the source file must be copied into which column of the staging table.</span></span>
- <span data-ttu-id="47acc-169">エクスポート ジョブのコンテキストで、マッピングはステージング テーブル (つまりソース) のどの列が、ターゲット ファイルの列になるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="47acc-169">In the context of an export job, mapping describes which columns of the staging table (that is, the source) become the columns in the target file.</span></span>

<span data-ttu-id="47acc-170">ステージング テーブルとファイルで列の名前が一致すると、システムは自動的にその名前に基づいてマッピングを確立します。</span><span class="sxs-lookup"><span data-stu-id="47acc-170">If the column names in the staging table and the file match, the system automatically establishes the mapping, based on the names.</span></span> <span data-ttu-id="47acc-171">ただし、名前が異なる場合、列は自動的にマップされません。</span><span class="sxs-lookup"><span data-stu-id="47acc-171">However, if the names differ, columns aren’t mapped automatically.</span></span> <span data-ttu-id="47acc-172">こうした場合は、データ ジョブのエンティティで [マップの表示] オプションを選択して、マッピングを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-172">In these cases, you must complete the mapping by selecting the **View map** option on the entity in the data job.</span></span>

<span data-ttu-id="47acc-173">既定のビューである [マッピングの視覚化]、および [マッピング詳細] という 2 つのマッピング ビューがあります。</span><span class="sxs-lookup"><span data-stu-id="47acc-173">There are two mapping views: **Mapping visualization**, which is the default view, and **Mapping details**.</span></span> <span data-ttu-id="47acc-174">赤いアスタリスク (\\*) はエンティティの必須フィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="47acc-174">A red asterisk (\\*) identifies any required fields in the entity.</span></span> <span data-ttu-id="47acc-175">エンティティを使用して作業する前に、これらのフィールドをマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-175">These fields must be mapped before you can work with the entity.</span></span> <span data-ttu-id="47acc-176">エンティティを使用して作業する際に、必要に応じて他のフィールドのマップ解除をすることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-176">You can unmap other fields as you require when you work with the entity.</span></span> <span data-ttu-id="47acc-177">フィールドのマップ解除をするには、[エンティティ] 列、または [ソース] 列いずれかのフィールドを選択し、その後 [選択の削除] を選択します。</span><span class="sxs-lookup"><span data-stu-id="47acc-177">To unmap a field, select the field in either the **Entity** column or the **Source** column, and then select **Delete selection**.</span></span> <span data-ttu-id="47acc-178">[保存] を選択して変更を保存し、ページを閉じてプロジェクトに戻ります。</span><span class="sxs-lookup"><span data-stu-id="47acc-178">Select **Save** to save your changes, and then close the page to return to the project.</span></span> <span data-ttu-id="47acc-179">同じプロセスを使用して、インポート後にソースからステージングへのフィールド マッピングを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-179">You can use the same process to edit the field mapping from source to staging after you import.</span></span>

<span data-ttu-id="47acc-180">[ソース マッピングの生成] を選択すると、ページ上にマッピングを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-180">You can generate a mapping on the page by selecting **Generate source mapping**.</span></span> <span data-ttu-id="47acc-181">生成されたマッピングは、自動マッピングと同様に動作します。</span><span class="sxs-lookup"><span data-stu-id="47acc-181">A generated mapping behaves like an automatic mapping.</span></span> <span data-ttu-id="47acc-182">したがって、マップされていないフィールドは、手動でマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-182">Therefore, you must manually map any unmapped fields.</span></span>

![データ マッピング](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a><span data-ttu-id="47acc-184">インポート/エクスポート ジョブのセキュリティを確認する</span><span class="sxs-lookup"><span data-stu-id="47acc-184">Verify the security for your import or export job</span></span>
<span data-ttu-id="47acc-185">管理者以外のユーザーは特定のデータ ジョブにのみアクセスできるよう、**データ管理**ワークスペースへのアクセスを制限することができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-185">Access to the **Data management** workspace can be restricted, so that non-administrator users can access only specific data jobs.</span></span> <span data-ttu-id="47acc-186">データ ジョブへのアクセスとは、そのジョブの実行履歴への完全なアクセス、またステージング テーブルへのアクセスを意味します。</span><span class="sxs-lookup"><span data-stu-id="47acc-186">Access to a data job implies full access to the execution history of that job and access to the staging tables.</span></span> <span data-ttu-id="47acc-187">そのため、データ ジョブの作成時に、適切なアクセス制御が設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-187">Therefore, you must make sure that appropriate access controls are in place when you create a data job.</span></span>

### <a name="secure-a-job-by-roles-and-users"></a><span data-ttu-id="47acc-188">ロールおよびユーザー別にジョブをセキュリティ保護する</span><span class="sxs-lookup"><span data-stu-id="47acc-188">Secure a job by roles and users</span></span>
<span data-ttu-id="47acc-189">[適用可能なロール] メニューを使用して、ジョブを 1 つまたは複数のセキュリティ ロールに制限します。</span><span class="sxs-lookup"><span data-stu-id="47acc-189">Use the **Applicable roles** menu to restrict the job to one or more security roles.</span></span> <span data-ttu-id="47acc-190">これらのロールのユーザーだけが、そのジョブへのアクセス権を持ちます。</span><span class="sxs-lookup"><span data-stu-id="47acc-190">Only users in those roles will have access to the job.</span></span>

<span data-ttu-id="47acc-191">ジョブを特定のユーザーに制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="47acc-191">You can also restrict a job to specific users.</span></span> <span data-ttu-id="47acc-192">ロールではなくユーザー別にジョブを保護すると、複数のユーザーが 1 つのロールに割り当てられている場合よりいっそう制御されることになります。</span><span class="sxs-lookup"><span data-stu-id="47acc-192">When you secure a job by users instead of roles, there is more control if multiple users are assigned to a role.</span></span>

### <a name="secure-a-job-by-legal-entity"></a><span data-ttu-id="47acc-193">法人別にジョブをセキュリティ保護する</span><span class="sxs-lookup"><span data-stu-id="47acc-193">Secure a job by legal entity</span></span>
<span data-ttu-id="47acc-194">データ ジョブは、本質的にグローバルです。</span><span class="sxs-lookup"><span data-stu-id="47acc-194">Data jobs are global in nature.</span></span> <span data-ttu-id="47acc-195">したがって、ある法人内でデータ ジョブが作成され使用されると、そのジョブはシステムにいる他の法人内で表示されることになります。</span><span class="sxs-lookup"><span data-stu-id="47acc-195">Therefore, if a data job was created and used in a legal entity, the job will be visible in other legal entities in the system.</span></span> <span data-ttu-id="47acc-196">この既定の動作は、いくつかのアプリケーション シナリオでは望ましい場合があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-196">This default behavior might be preferred in some application scenarios.</span></span> <span data-ttu-id="47acc-197">たとえば、データ エンティティを使用して請求書をインポートする組織は、組織内のすべての部局の請求書エラーの管理を担当する集中請求処理チームを備える場合があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-197">For example, an organization that imports invoices by using data entities might provide a centralized invoice processing team that is responsible for managing invoice errors for all divisions in the organization.</span></span> <span data-ttu-id="47acc-198">このシナリオでは、集中請求処理チームにすべての法人からの請求書インポート ジョブへのアクセス権があることは有益です。</span><span class="sxs-lookup"><span data-stu-id="47acc-198">In this scenario, it’s useful for the centralized invoice processing team to have access to invoice import jobs from all legal entities.</span></span> <span data-ttu-id="47acc-199">したがって、法人の視点からこの既定の動作は要件を満たしています。</span><span class="sxs-lookup"><span data-stu-id="47acc-199">Therefore, the default behavior meets the requirement from a legal entity perspective.</span></span>

<span data-ttu-id="47acc-200">ただし、組織によっては法人ごとに請求書処理チームが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-200">However, an organization might want to have invoice processing teams per legal entity.</span></span> <span data-ttu-id="47acc-201">この場合、法人のチームは、自分の法人内の請求書インポート ジョブにのみアクセス権を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-201">In this case, a team in a legal entity should have access only to the invoice import job in its own legal entity.</span></span> <span data-ttu-id="47acc-202">この要件を満たすには、データ ジョブ内の [適用可能な法人] メニューを使用して、データ ジョブに対して法人ベースのアクセス制御をコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-202">To meet this requirement, you can configure legal entity–based access control on the data jobs by using the **Applicable legal entities** menu inside the data job.</span></span> <span data-ttu-id="47acc-203">コンフィギュレーションが完了したら、ユーザーは、現在サインイン中の法人で使用できるジョブのみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-203">After the configuration is done, users can see only jobs that are available in the legal entity that they are currently signed in to.</span></span> <span data-ttu-id="47acc-204">別の法人からジョブを表示するには、ユーザーはその法人に切り替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="47acc-204">To see jobs from another legal entity, users must switch to that legal entity.</span></span>

<span data-ttu-id="47acc-205">ロール、ユーザー、および法人別のセキュリティ保護をジョブに同時に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-205">A job can be secured by roles, users, and legal entity at the same time.</span></span>

## <a name="run-the-import-or-export-job"></a><span data-ttu-id="47acc-206">インポート/エクスポート ジョブを実行する</span><span class="sxs-lookup"><span data-stu-id="47acc-206">Run the import or export job</span></span>
<span data-ttu-id="47acc-207">ジョブを定義した後、[インポート] または [エクスポート] ボタンを選択することにより、そのジョブを 1 回実行できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-207">You can run a job one time by selecting the **Import** or **Export** button after you define the job.</span></span> <span data-ttu-id="47acc-208">定期的なジョブを設定するには、[定期的なデータ ジョブの作成] を選択します。</span><span class="sxs-lookup"><span data-stu-id="47acc-208">To set up a recurring job, select **Create recurring data job**.</span></span>

## <a name="validate-that-the-job-ran-as-expected"></a><span data-ttu-id="47acc-209">ジョブが期待どおりに実行されたことを検証する</span><span class="sxs-lookup"><span data-stu-id="47acc-209">Validate that the job ran as expected</span></span>
<span data-ttu-id="47acc-210">ジョブの履歴は、インポートおよびエクスポート ジョブ両方のトラブルシューティングと調査に使用できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-210">The job history is available for troubleshooting and investigation on both import and export jobs.</span></span> <span data-ttu-id="47acc-211">履歴ジョブの実行は、時間範囲別に整理されています。</span><span class="sxs-lookup"><span data-stu-id="47acc-211">Historical job runs are organized by time ranges.</span></span>

![ジョブ履歴範囲](./media/dixf-job-history.md.png)

<span data-ttu-id="47acc-213">各ジョブの実行により、次の詳細情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-213">Each job run provides the following details:</span></span>

- <span data-ttu-id="47acc-214">実行の詳細</span><span class="sxs-lookup"><span data-stu-id="47acc-214">Execution details</span></span>
- <span data-ttu-id="47acc-215">実行ログ</span><span class="sxs-lookup"><span data-stu-id="47acc-215">Execution log</span></span>

<span data-ttu-id="47acc-216">実行の詳細は、ジョブが処理した各データ エンティティの状態を示します。</span><span class="sxs-lookup"><span data-stu-id="47acc-216">Execution details show the state of each data entity that the job processed.</span></span> <span data-ttu-id="47acc-217">そのため、次の情報をすばやく見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-217">Therefore, you can quickly find the following information:</span></span>

- <span data-ttu-id="47acc-218">処理されたエンティティ</span><span class="sxs-lookup"><span data-stu-id="47acc-218">Which entities were processed</span></span>
- <span data-ttu-id="47acc-219">エンティティの、正しく処理されたレコード数と失敗した数</span><span class="sxs-lookup"><span data-stu-id="47acc-219">For an entity, how many records were successfully processed, and how many failed</span></span>
- <span data-ttu-id="47acc-220">各エンティティのステージング レコード</span><span class="sxs-lookup"><span data-stu-id="47acc-220">The staging records for each entity</span></span>

<span data-ttu-id="47acc-221">ステージング データは、エクスポート ジョブ用にファイルにダウンロードするか、インポート/エクスポート ジョブのパッケージとしてダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-221">You can download the staging data in a file for export jobs, or you can download it as a package for import and export jobs.</span></span>

<span data-ttu-id="47acc-222">実行の詳細から、実行ログも開くことができます。</span><span class="sxs-lookup"><span data-stu-id="47acc-222">From the execution details, you can also open the execution log.</span></span>

## <a name="clean-up-the-staging-tables"></a><span data-ttu-id="47acc-223">ステージング テーブルをクリーンアップする</span><span class="sxs-lookup"><span data-stu-id="47acc-223">Clean up the staging tables</span></span>
<span data-ttu-id="47acc-224">**データ管理**ワークスペースの**ステージング クリーンアップ**機能を使用して、ステージング テーブルをクリーンアップすることができます</span><span class="sxs-lookup"><span data-stu-id="47acc-224">You can clean up staging tables by using the **Staging clean up** feature in the **Data management** workspace.</span></span> <span data-ttu-id="47acc-225">以下のオプションを使用して、どのステージング テーブルからどのレコードを削除するかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="47acc-225">You can use the following options to select which records should be deleted from which staging table:</span></span>

- <span data-ttu-id="47acc-226">[エンティティ] – エンティティのみ提供すると、そのエンティティのステージング テーブルからのすべてのレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-226">**Entity** – If only an entity is provided, all records from that entity’s staging table are deleted.</span></span> <span data-ttu-id="47acc-227">すべてのデータ プロジェクトとすべてのジョブでそのエンティティのデータをすべてクリーンアップするには、このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="47acc-227">Select this option to clean up all the data for the entity across all data projects and all jobs.</span></span>
- <span data-ttu-id="47acc-228">[ジョブ ID] – ジョブ ID のみ提供すると、選択したジョブのすべてのエンティティのレコードすべてが、該当するステージング テーブルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-228">**Job ID** – If only a job ID is provided, all records for all entities in the selected job are deleted from the appropriate staging tables.</span></span>
- <span data-ttu-id="47acc-229">[データ プロジェクト] – データ プロジェクトのみ選択すると、すべてのエンティティのすべてのレコードが、選択したデータ プロジェクトのすべてのジョブで、削除されます。</span><span class="sxs-lookup"><span data-stu-id="47acc-229">**Data projects** – If only a data project is selected, all records for all entities and across all jobs for the selected data project are deleted.</span></span>

<span data-ttu-id="47acc-230">削除するレコード セットをさらに制限するために、オプションを組み合わせることもできます。</span><span class="sxs-lookup"><span data-stu-id="47acc-230">You can also combine the options to further restrict the record set that is deleted.</span></span>


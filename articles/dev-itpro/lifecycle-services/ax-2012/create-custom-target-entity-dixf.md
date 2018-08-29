---
title: "データのインポート/エクスポート フレームワークのカスタム ターゲット エンティティを作成する"
description: "このトピックでは、カスタム エンティティを作成して、Microsoft Dynamics AX のデータ インポート/エクスポート フレームワークを使用して、定義済みのエンティティに適合しないデータをインポート、エクスポート、または移行できるようにする方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18181
ms.assetid: 60c79bd4-1090-4e79-9a8c-2117d963647a
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b5d732e986c654656700791ddad044a8d7e37ad5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="create-custom-target-entities-for-the-data-importexport-framework"></a><span data-ttu-id="13bb3-103">データのインポート/エクスポート フレームワークのカスタム ターゲット エンティティを作成する</span><span class="sxs-lookup"><span data-stu-id="13bb3-103">Create custom target entities for the Data Import/Export Framework</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13bb3-104">このトピックでは、カスタム エンティティを作成して、Microsoft Dynamics AX のデータ インポート/エクスポート フレームワークを使用して、定義済みのエンティティに適合しないデータをインポート、エクスポート、または移行できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-104">This topic describes how to create a custom entity, so that you can use the Microsoft Dynamics AX Data Import/Export Framework to import, export, or migrate data that does not fit a predefined entity.</span></span>

<span data-ttu-id="13bb3-105">カスタム エンティティには、ステージング テーブル、プロジェクト、クエリ、クラス、および関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="13bb3-105">A custom entity requires a staging table, a project, a query, a class, and functions.</span></span> <span data-ttu-id="13bb3-106">**データ インポート/エクスポート用のカスタム エンティティの作成ウィザード** を使用してこれらの要素を作成、または手動で作成することができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-106">You can use the **Create a custom entity for data import/export Wizard** to create these elements for you, or you can create them manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="13bb3-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="13bb3-107">Prerequisites</span></span>
<span data-ttu-id="13bb3-108">開始する前に、作成しているエンティティに Microsoft Dynamics AX 内の、どのテーブルがマップされているかを把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-108">Before you begin, you must know which table in Microsoft Dynamics AX maps to the entity that you are creating.</span></span> <span data-ttu-id="13bb3-109">このテーブルは、エクスポートするデータのソースか、またはインポートするデータのターゲットのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="13bb3-109">This table is either the source of the data that you are exporting or the target of the data that you are importing.</span></span> <span data-ttu-id="13bb3-110">新しいテーブルを作成する必要がある場合、「[テーブルの作成方法](create-tables.md)」の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="13bb3-110">If you have to create a new table, follow the instructions in [How to: Create Tables](create-tables.md).</span></span>

## <a name="create-a-custom-entity-by-using-the-create-a-custom-entity-for-data-importexport-wizard"></a><span data-ttu-id="13bb3-111">データのインポート/エクスポート ウィザードでカスタム エンティティを作成ウィザードを使用してカスタム エンティティを作成する</span><span class="sxs-lookup"><span data-stu-id="13bb3-111">Create a custom entity by using the Create a custom entity for data import/export Wizard</span></span>
<span data-ttu-id="13bb3-112">**データのインポート/エクスポート ウィザードでカスタム エンティティを作成ウィザード**では、カスタム エンティティをすばやく作成できます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-112">The **Create a custom entity for data import/export Wizard** lets you quickly create a custom entity.</span></span>

1.  <span data-ttu-id="13bb3-113">**データのインポート/エクスポート フレームワーク** &gt; **共通** &gt; **データのインポート/エクスポート用のカスタム エンティティの作成**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-113">Go to **Data Import/Export Framework** &gt; **Common** &gt; **Create a custom entity for data import/export**.</span></span>
2.  <span data-ttu-id="13bb3-114">移行対象のエンティティに関連するテーブルを選択し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-114">Select the table that is related to the entity that you want to migrate, and then click **Next**.</span></span>
   <span data-ttu-id="13bb3-115">**注意**: ウィザードは、他のテーブルのデータ構造を継承しないテーブルにのみ関連付けられているカスタム エンティティを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-115">**Caution**: The wizard can be used to create custom entities that are associated only with tables that do not inherit data structures from other tables.</span></span>
3.  <span data-ttu-id="13bb3-116">**コード生成パラメーターの選択**ページで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="13bb3-116">On the **Select code generation parameters** page, follow these steps:</span></span>
    1.  <span data-ttu-id="13bb3-117">ステージング テーブル、クエリ、クラスの名前がウィザードに表示されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-117">The wizard suggests names for the staging table, query, and class.</span></span> <span data-ttu-id="13bb3-118">これらの名前を受け入れるか、それらを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-118">You can accept these names or change them.</span></span>
    2.  <span data-ttu-id="13bb3-119">エンティティから表示メニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-119">Select a display menu item for the entity.</span></span> <span data-ttu-id="13bb3-120">新しい表示メニュー項目を作成する必要がある場合、「[メニューとメニュー項目の作成方法](https://msdn.microsoft.com/library/5277205c-edb9-498e-b927-406237806217(AX.60).aspx)」の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="13bb3-120">If you have to create a new display menu item, follow the instructions in [How to: Create Menus and Menu Items](https://msdn.microsoft.com/library/5277205c-edb9-498e-b927-406237806217(AX.60).aspx).</span></span>
    3.  <span data-ttu-id="13bb3-121">テーブルで外部キーのデータを生成するためにメソッドとクエリのどちらを使用するかを選択します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-121">Select whether to use a method or a query to generate data for any foreign keys in the table.</span></span> <span data-ttu-id="13bb3-122">選択に応じて、**生成**メソッドがクラスに追加されるか、外部キーのソース テーブルがエンティティのクエリに追加されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-122">Depending on your selection, either a **generate** method is added to the class, or the source tables for the foreign keys are added to the query for the entity.</span></span>
    4.  <span data-ttu-id="13bb3-123">エンティティに 2 つのテーブルと関連しているデータが格納されているデータ ソースを使用する場合は、複合エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-123">If the entity will be used with a data source that contains related data from two tables, select composite entity.</span></span> <span data-ttu-id="13bb3-124">次に、**RowID** フィールドがステージング テーブル内に作成されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-124">The **RowID** field is then created in the staging table.</span></span> <span data-ttu-id="13bb3-125">このフィールドは、関連するデータの行を互いにマップするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-125">This field is used to map the rows of related data to each other.</span></span>
    5.  <span data-ttu-id="13bb3-126">エンティティに必要な値の設定が終了したら、**次** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-126">When you have finished setting the values that are required for your entity, click **Next**.</span></span>

4.  <span data-ttu-id="13bb3-127">**ターゲット テーブル内のフィールド**ページで、ターゲット テーブルのフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-127">On the **Fields in the target table** page, select the fields for the target table.</span></span> <span data-ttu-id="13bb3-128">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-128">Click **Next**.</span></span>
5.  <span data-ttu-id="13bb3-129">**ウィザード完了**ページで、**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-129">On the **Wizard complete** page, click **Finish**.</span></span> <span data-ttu-id="13bb3-130">データのインポート/エクスポート フレームワークは、Microsoft Dynamics AX アプリケーション オブジェクト ツリー (AOT) を開き、現在のレイヤーでユーザー定義のエンティティのプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-130">The Data Import/Export Framework opens the Microsoft Dynamics AX Application Object Tree (AOT) and creates a project for the custom entity in the current layer.</span></span>
6.  <span data-ttu-id="13bb3-131">選択したテーブルで拡張データ型 (EDT) が使用されている場合、EDT の外部キー関係を新しいステージング テーブルに追加するかどうかを 2 回尋ねられます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-131">If the table that you selected uses an extended data type (EDT), you are asked two times whether you want to add the ForeignKey relation from the EDT to the new staging table.</span></span> <span data-ttu-id="13bb3-132">毎回**はい**をクリックして、ForeignKey のリレーションシップを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-132">Click **Yes** each time to create the ForeignKey relationship.</span></span>
7.  <span data-ttu-id="13bb3-133">新しいターゲット エンティティとしては、カスタム エンティティを追加します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-133">Add the custom entity as a new target entity.</span></span> <span data-ttu-id="13bb3-134">エンティティによっては、いくつかの手動のステップが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-134">Depending on the entity, some manual steps might be required.</span></span> <span data-ttu-id="13bb3-135">ターゲット エンティティを作成する方法の詳細については、[データのインポート/エクスポート フレームワークを使用する移行データ (DIXF、DMF)](migrate-data-dixf.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="13bb3-135">For more information about how to create a target entity, see [Migrating data using the Data import/export framework (DIXF, DMF)](migrate-data-dixf.md).</span></span>

## <a name="manually-create-a-custom-entity"></a><span data-ttu-id="13bb3-136">カスタム エンティティの手動での作成</span><span class="sxs-lookup"><span data-stu-id="13bb3-136">Manually create a custom entity</span></span>
<span data-ttu-id="13bb3-137">このセクションでは、カスタム エンティティを手動で作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-137">This section describes how to manually create a custom entity.</span></span>

### <a name="create-a-staging-table-for-the-entity"></a><span data-ttu-id="13bb3-138">エンティティのステージング テーブルを作成する</span><span class="sxs-lookup"><span data-stu-id="13bb3-138">Create a staging table for the entity</span></span>

1.  <span data-ttu-id="13bb3-139">Microsoft Dynamics AX の AOT でエンティティのステージング テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-139">In Microsoft Dynamics AX, in the AOT, create a staging table for the entity.</span></span>
2.  <span data-ttu-id="13bb3-140">次の情報を使用して、ステージング テーブルのテーブル プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-140">Use the following information to set up the table properties for the staging table.</span></span>

    | <span data-ttu-id="13bb3-141">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="13bb3-141">Property name</span></span>               | <span data-ttu-id="13bb3-142">先頭値</span><span class="sxs-lookup"><span data-stu-id="13bb3-142">Value</span></span>   |
    |-----------------------------|---------|
    | <span data-ttu-id="13bb3-143">**SaveDataPerCompany**</span><span class="sxs-lookup"><span data-stu-id="13bb3-143">**SaveDataPerCompany**</span></span>      | <span data-ttu-id="13bb3-144">無</span><span class="sxs-lookup"><span data-stu-id="13bb3-144">No</span></span>      |
    | <span data-ttu-id="13bb3-145">**SupportInheritance**</span><span class="sxs-lookup"><span data-stu-id="13bb3-145">**SupportInheritance**</span></span>      | <span data-ttu-id="13bb3-146">無</span><span class="sxs-lookup"><span data-stu-id="13bb3-146">No</span></span>      |
    | <span data-ttu-id="13bb3-147">**TableType**</span><span class="sxs-lookup"><span data-stu-id="13bb3-147">**TableType**</span></span>               | <span data-ttu-id="13bb3-148">通常</span><span class="sxs-lookup"><span data-stu-id="13bb3-148">Regular</span></span> |
    | <span data-ttu-id="13bb3-149">**ConfigurationKey**</span><span class="sxs-lookup"><span data-stu-id="13bb3-149">**ConfigurationKey**</span></span>        | <span data-ttu-id="13bb3-150">DMF</span><span class="sxs-lookup"><span data-stu-id="13bb3-150">DMF</span></span>     |
    | <span data-ttu-id="13bb3-151">**ValidTimeStateFieldType**</span><span class="sxs-lookup"><span data-stu-id="13bb3-151">**ValidTimeStateFieldType**</span></span> | <span data-ttu-id="13bb3-152">None</span><span class="sxs-lookup"><span data-stu-id="13bb3-152">None</span></span>    |

3.  <span data-ttu-id="13bb3-153">次のプロパティを持つフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-153">Create fields that have the following properties.</span></span>

    | <span data-ttu-id="13bb3-154">フィールド名</span><span class="sxs-lookup"><span data-stu-id="13bb3-154">Field name</span></span>          | <span data-ttu-id="13bb3-155">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="13bb3-155">Extended data type</span></span>     | <span data-ttu-id="13bb3-156">列挙</span><span class="sxs-lookup"><span data-stu-id="13bb3-156">Enum</span></span>              |
    |---------------------|------------------------|-------------------|
    | <span data-ttu-id="13bb3-157">**DefinitionGroup**</span><span class="sxs-lookup"><span data-stu-id="13bb3-157">**DefinitionGroup**</span></span> | <span data-ttu-id="13bb3-158">DMFDefinitionGroupName</span><span class="sxs-lookup"><span data-stu-id="13bb3-158">DMFDefinitionGroupName</span></span> |                   |
    | <span data-ttu-id="13bb3-159">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="13bb3-159">**IsSelected**</span></span>      | <span data-ttu-id="13bb3-160">DMFIsSelected</span><span class="sxs-lookup"><span data-stu-id="13bb3-160">DMFIsSelected</span></span>          | <span data-ttu-id="13bb3-161">NoYes</span><span class="sxs-lookup"><span data-stu-id="13bb3-161">NoYes</span></span>             |
    | <span data-ttu-id="13bb3-162">**TransferStatus**</span><span class="sxs-lookup"><span data-stu-id="13bb3-162">**TransferStatus**</span></span>  |                        | <span data-ttu-id="13bb3-163">DMFTransferStatus</span><span class="sxs-lookup"><span data-stu-id="13bb3-163">DMFTransferStatus</span></span> |
    | <span data-ttu-id="13bb3-164">**ExecutionId**</span><span class="sxs-lookup"><span data-stu-id="13bb3-164">**ExecutionId**</span></span>     | <span data-ttu-id="13bb3-165">DMFExecutionId</span><span class="sxs-lookup"><span data-stu-id="13bb3-165">DMFExecutionId</span></span>         |                   |

4.  <span data-ttu-id="13bb3-166">次のプロパティを持つフィールド グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-166">Create field groups that have the following properties.</span></span>

    | <span data-ttu-id="13bb3-167">フィールド グループ名</span><span class="sxs-lookup"><span data-stu-id="13bb3-167">Field group name</span></span>                                                         | <span data-ttu-id="13bb3-168">ラベル</span><span class="sxs-lookup"><span data-stu-id="13bb3-168">Label</span></span>                                                                         | <span data-ttu-id="13bb3-169">フィールド</span><span class="sxs-lookup"><span data-stu-id="13bb3-169">Field</span></span>                                                                                        |
    |--------------------------------------------------------------------------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
    | <span data-ttu-id="13bb3-170">**ExclusionList**</span><span class="sxs-lookup"><span data-stu-id="13bb3-170">**ExclusionList**</span></span>                                                        | <span data-ttu-id="13bb3-171">**除外リスト**</span><span class="sxs-lookup"><span data-stu-id="13bb3-171">**Exclusion List**</span></span>                                                            | <span data-ttu-id="13bb3-172">**DefinitionGroup**</span><span class="sxs-lookup"><span data-stu-id="13bb3-172">**DefinitionGroup**</span></span>                                                                          |
    | <span data-ttu-id="13bb3-173">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-173">** **</span></span>                                                                    | <span data-ttu-id="13bb3-174">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-174">** **</span></span>                                                                         | <span data-ttu-id="13bb3-175">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="13bb3-175">**IsSelected**</span></span>                                                                               |
    | <span data-ttu-id="13bb3-176">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-176">** **</span></span>                                                                    | <span data-ttu-id="13bb3-177">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-177">** **</span></span>                                                                         | <span data-ttu-id="13bb3-178">**TransferStatus**</span><span class="sxs-lookup"><span data-stu-id="13bb3-178">**TransferStatus**</span></span>                                                                           |
    | <span data-ttu-id="13bb3-179">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-179">** **</span></span>                                                                    | <span data-ttu-id="13bb3-180">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-180">** **</span></span>                                                                         | <span data-ttu-id="13bb3-181">**ExecutionId**</span><span class="sxs-lookup"><span data-stu-id="13bb3-181">**ExecutionId**</span></span>                                                                              |
    | <span data-ttu-id="13bb3-182">**有効**</span><span class="sxs-lookup"><span data-stu-id="13bb3-182">**Enabled**</span></span>                                                              | <span data-ttu-id="13bb3-183">**有効**</span><span class="sxs-lookup"><span data-stu-id="13bb3-183">**Enabled**</span></span>                                                                   | <span data-ttu-id="13bb3-184">オプション: 既定でテンプレートに追加するステージング テーブルからのフィールド。</span><span class="sxs-lookup"><span data-stu-id="13bb3-184">Optional: Fields from the staging table that you want to include in the template by default.</span></span> |
    | <span data-ttu-id="13bb3-185">&lt;&lt;FunctionName\_Sequence&gt;&gt;例 – GeneratePostalAddress\_2</span><span class="sxs-lookup"><span data-stu-id="13bb3-185">&lt;&lt;FunctionName\_Sequence&gt;&gt;Example – GeneratePostalAddress\_2</span></span> | <span data-ttu-id="13bb3-186">&lt;&lt; 機能の説明 &gt;&gt;住所を生成する機能。</span><span class="sxs-lookup"><span data-stu-id="13bb3-186">&lt;&lt; Description of function &gt;&gt;Function to generate postal address.</span></span> | <span data-ttu-id="13bb3-187">指定されたメソッドのソースであるステージング テーブルのフィールド。</span><span class="sxs-lookup"><span data-stu-id="13bb3-187">The fields from the staging table that are the source for the specified method.</span></span>              |
    |                                                                          |                                                                               | <span data-ttu-id="13bb3-188">**CountryRegionId**</span><span class="sxs-lookup"><span data-stu-id="13bb3-188">**CountryRegionId**</span></span>                                                                          |
    | <span data-ttu-id="13bb3-189">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-189">** **</span></span>                                                                    | <span data-ttu-id="13bb3-190">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-190">** **</span></span>                                                                         | <span data-ttu-id="13bb3-191">**都道府県**</span><span class="sxs-lookup"><span data-stu-id="13bb3-191">**State**</span></span>                                                                                    |
    | <span data-ttu-id="13bb3-192">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-192">** **</span></span>                                                                    | <span data-ttu-id="13bb3-193">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-193">** **</span></span>                                                                         | <span data-ttu-id="13bb3-194">**市町村**</span><span class="sxs-lookup"><span data-stu-id="13bb3-194">**City**</span></span>                                                                                     |
    | <span data-ttu-id="13bb3-195">** **</span><span class="sxs-lookup"><span data-stu-id="13bb3-195">** **</span></span>                                                                    |                                                                               | <span data-ttu-id="13bb3-196">..</span><span class="sxs-lookup"><span data-stu-id="13bb3-196">..</span></span>                                                                                           |

5.  <span data-ttu-id="13bb3-197">テーブルのプライマリ インデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-197">Create a primary index for the table.</span></span>

    | <span data-ttu-id="13bb3-198">インデックス名</span><span class="sxs-lookup"><span data-stu-id="13bb3-198">Index name</span></span>                              | <span data-ttu-id="13bb3-199">プロパティ</span><span class="sxs-lookup"><span data-stu-id="13bb3-199">Properties</span></span>                             | <span data-ttu-id="13bb3-200">フィールド</span><span class="sxs-lookup"><span data-stu-id="13bb3-200">Fields</span></span>                                                 |
    |-----------------------------------------|----------------------------------------|--------------------------------------------------------|
    | <span data-ttu-id="13bb3-201">&lt;&lt;任意の名前&gt;&gt;.</span><span class="sxs-lookup"><span data-stu-id="13bb3-201">&lt;&lt;any name&gt;&gt;.</span></span> <span data-ttu-id="13bb3-202">例 – Idx</span><span class="sxs-lookup"><span data-stu-id="13bb3-202">Example – Idx</span></span> | <span data-ttu-id="13bb3-203">AllowDuplicates – いいえ</span><span class="sxs-lookup"><span data-stu-id="13bb3-203">AllowDuplicates – No</span></span>  | <span data-ttu-id="13bb3-204">**DefinitionGroup**</span><span class="sxs-lookup"><span data-stu-id="13bb3-204">**DefinitionGroup**</span></span>                                    |
    |   | <span data-ttu-id="13bb3-205">AlternateKey - はい</span><span class="sxs-lookup"><span data-stu-id="13bb3-205">AlternateKey - Yes</span></span> | <span data-ttu-id="13bb3-206">**DefinitionGroup**</span><span class="sxs-lookup"><span data-stu-id="13bb3-206">**DefinitionGroup**</span></span>                                    |
    |                                         |                                        | <span data-ttu-id="13bb3-207">**ExecutionId**</span><span class="sxs-lookup"><span data-stu-id="13bb3-207">**ExecutionId**</span></span>                                        |
    |                                         |                                        | <span data-ttu-id="13bb3-208">**一意性を定義するステージング テーブルのフィールド**</span><span class="sxs-lookup"><span data-stu-id="13bb3-208">**Fields from the staging table to define uniqueness**</span></span> |
    |                                         |                                        | <span data-ttu-id="13bb3-209">..</span><span class="sxs-lookup"><span data-stu-id="13bb3-209">..</span></span>                                                     |

6.  <span data-ttu-id="13bb3-210">ステージング テーブルとターゲット テーブル間の関係を指定します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-210">Specify the relationship between the staging table and the target table.</span></span> <span data-ttu-id="13bb3-211">この関係は、特定のステージング レコードを関連するターゲット エンティティに自動的にリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-211">This relation is used to automatically link a particular staging record with the related target entity.</span></span> <span data-ttu-id="13bb3-212">関係のノードを使用して関係を定義することはできない場合は、エンティティのクラスに addStagingLink() メソッドを使用しそれを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-212">If you cannot define the relationship by using the relation node, you should define it by using the addStagingLink() method in the entity class.</span></span>

    | <span data-ttu-id="13bb3-213">インデックス名</span><span class="sxs-lookup"><span data-stu-id="13bb3-213">Index name</span></span>                                    | <span data-ttu-id="13bb3-214">関係プロパティ</span><span class="sxs-lookup"><span data-stu-id="13bb3-214">Relation properties</span></span>                  | <span data-ttu-id="13bb3-215">関係フィールド</span><span class="sxs-lookup"><span data-stu-id="13bb3-215">Relation fields</span></span>                |
    |-----------------------------------------------|--------------------------------------|--------------------------------|
    | <span data-ttu-id="13bb3-216">&lt;&lt;ターゲット テーブル&gt;&gt;.</span><span class="sxs-lookup"><span data-stu-id="13bb3-216">&lt;&lt;Target Table&gt;&gt;.</span></span> <span data-ttu-id="13bb3-217">例 - ターゲット</span><span class="sxs-lookup"><span data-stu-id="13bb3-217">Example -Target</span></span> | <span data-ttu-id="13bb3-218">テーブル - &lt;&lt;ターゲット テーブル&gt;&gt;</span><span class="sxs-lookup"><span data-stu-id="13bb3-218">Table - &lt;&lt;Target Table&gt;&gt;</span></span> | <span data-ttu-id="13bb3-219">Staging.Field1 = Target.Field1</span><span class="sxs-lookup"><span data-stu-id="13bb3-219">Staging.Field1 = Target.Field1</span></span> |
    |                                               |                                      | <span data-ttu-id="13bb3-220">..</span><span class="sxs-lookup"><span data-stu-id="13bb3-220">..</span></span>                             |
    |                                               |                                      | <span data-ttu-id="13bb3-221">..</span><span class="sxs-lookup"><span data-stu-id="13bb3-221">..</span></span>                             |

### <a name="create-a-project"></a><span data-ttu-id="13bb3-222">プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="13bb3-222">Create a project</span></span>

<span data-ttu-id="13bb3-223">Microsoft Dynamics AX の AOT で、プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-223">In Microsoft Dynamics AX, in the AOT, create a project.</span></span>

### <a name="create-a-class-for-the-entity"></a><span data-ttu-id="13bb3-224">エンティティのクラスを作成します</span><span class="sxs-lookup"><span data-stu-id="13bb3-224">Create a class for the entity</span></span>

1.  <span data-ttu-id="13bb3-225">Microsoft Dynamics AX の AOT でエンティティのクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-225">In Microsoft Dynamics AX, in the AOT, create a class for the entity.</span></span>
2.  <span data-ttu-id="13bb3-226">クラス宣言では、次のプロパティを含めます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-226">In the class declaration, include the following properties:</span></span>

    -   <span data-ttu-id="13bb3-227">“\[DMFAttribute(true)\]” を指定します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-227">Specify “\[DMFAttribute(true)\]”.</span></span>
    -   <span data-ttu-id="13bb3-228">“DMFClassName extends DMFEntityBase” を指定します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-228">Specify “DMFClassName extends DMFEntityBase”.</span></span>
    -   <span data-ttu-id="13bb3-229">名前が**エンティティ**のステージング テーブルのオブジェクトを宣言します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-229">Declare the object for the staging table that has the name **entity**.</span></span>
    -   <span data-ttu-id="13bb3-230">ターゲット エンティティのメイン テーブルのオブジェクトを**ターゲット**という名前で宣言します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-230">Declare the object for the main table for the target entity with the name **target**.</span></span>

    <span data-ttu-id="13bb3-231">次の例は、**DMFCustomerEntityClass** クラスの宣言方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="13bb3-231">The following example shows how the **DMFCustomerEntityClass** class is declared.</span></span>

        [DMFAttribute(true)]
        class DMFCustomerEntityClass extends DMFEntityBase
        {

        DMFCustomerEntity entity;

        CustTable target;

        }

3.  <span data-ttu-id="13bb3-232">**新規**メソッドの作成は次のようにします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-232">Create the **new** method as follows:</span></span>

    -   <span data-ttu-id="13bb3-233">メソッドはステージング テーブルをパラメーターとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-233">The method must take the staging table as a parameter.</span></span>
    -   <span data-ttu-id="13bb3-234">値のエンティティは、パラメーターから初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-234">The value entity should be initialized from a parameter.</span></span>

    <span data-ttu-id="13bb3-235">次の例は、**DMFCustomerEntity** の **new** メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="13bb3-235">The following example shows the **new** method for **DMFCustomerEntity**.</span></span>

        Public void new(DMFCustomerEntity _entity)
        {
        entity = _entity;
        }

4.  <span data-ttu-id="13bb3-236">**コンストラクター** メソッドの作成は次のようにします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-236">Create the **construct** method as follows:</span></span>

    -   <span data-ttu-id="13bb3-237">メソッドはステージング テーブルをパラメーターとして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-237">The method must take the staging table as a parameter.</span></span>
    -   <span data-ttu-id="13bb3-238">このメソッドは、パラメーターを使用して現在のクラスのオブジェクトを作成して返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-238">The method must create and return the object of the current class by using a parameter.</span></span>

    <span data-ttu-id="13bb3-239">次の例は、**DMFCustomerEntity** の **construct** メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="13bb3-239">The following example shows the **construct** method for **DMFCustomerEntity**.</span></span>

        public static DMFCustomerEntityClass construct (DMFCustomerEntity _entity)
        {
        DMFCustomerEntityClass entityClass = new DMFCustomerEntityClass(_entity);
        return entityClass;
        }

5.  <span data-ttu-id="13bb3-240">**setTargetBuffer** メソッドの作成は次のようにします。</span><span class="sxs-lookup"><span data-stu-id="13bb3-240">Create the **setTargetBuffer** method as follows:</span></span>

    -   <span data-ttu-id="13bb3-241">ターゲット エンティティは、複数のデータ ソースを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-241">A target entity can have multiple data sources.</span></span> <span data-ttu-id="13bb3-242">1 つのデータ ソースは、エンティティを表すメイン テーブルです。</span><span class="sxs-lookup"><span data-stu-id="13bb3-242">One data source is the main table that represents the entity.</span></span> <span data-ttu-id="13bb3-243">**setTargetBuffer** メソッドで、**\_dataSourceName** パラメーターはターゲット エンティティ クエリに存在するデータ ソースを表します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-243">In the **setTargetBuffer** method, the **\_dataSourceName** parameter represents the data sources that are present in the target entity query.</span></span>
    -   <span data-ttu-id="13bb3-244">データ ソースによっては、データ ソースのテーブルのローカル インスタンスを初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-244">Depending on the data source, you might have to initialize a local instance of the table for the data source.</span></span> <span data-ttu-id="13bb3-245">ローカル インスタンスは、データ移行に必要な機能で使用できます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-245">The local instance can then be used in the functions that are required for data migration.</span></span> <span data-ttu-id="13bb3-246">ターゲットは、ターゲット エンティティを表すメイン テーブルによって初期化される必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-246">The target should be initialized by the main table that represents the target entity.</span></span>

    <span data-ttu-id="13bb3-247">次の例は、**setTargetBuffer** メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="13bb3-247">The following example shows the **setTargetBuffer** method.</span></span>

        public void setTargetBuffer(Common _common, Name _dataSourceName = ' ')
        {
        switch (_common.TableId)
        {
        Case tableNum(CustTable) :
        Target = _common;
        Break;
        }
        }

6.  <span data-ttu-id="13bb3-248">クラスの **RunOn** プロパティの値を **CalledFrom** に設定します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-248">Set the value of the **RunOn** property for the class to **CalledFrom**.</span></span>

### <a name="write-functions-to-import-and-export-data"></a><span data-ttu-id="13bb3-249">データをインポートおよびエクスポートする関数を記述</span><span class="sxs-lookup"><span data-stu-id="13bb3-249">Write functions to import and export data</span></span>

<span data-ttu-id="13bb3-250">次の 2 つの方法で、ステージングからターゲット エンティティにデータをマッピングすることができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-250">You can map data from the staging to the target entity in two ways:</span></span>
-   <span data-ttu-id="13bb3-251">ステージング エンティティのフィールドを直接ターゲット エンティティのフィールドに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-251">Assign a field in the staging entity directly to a field in the target entity.</span></span> <span data-ttu-id="13bb3-252">この場合、ステージング フィールドとターゲット フィールドのデータ型は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-252">In this case, the data types for the staging and target fields must be same.</span></span>
-   <span data-ttu-id="13bb3-253">X++ 関数を記述してフィールド値をステージングからターゲットに変換します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-253">Write an X++ function to transform the field values from staging to target.</span></span>

<span data-ttu-id="13bb3-254">定義したデータのインポートおよびエクスポート関数は、次の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-254">Data import and export functions that you define must perform the following actions:</span></span>
-   <span data-ttu-id="13bb3-255">**入力/ソース** – ステージング レコード全体は、ローカル変数としてクラスで使用できます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-255">**Input/Source** – The whole staging record is available to the class as a local variable.</span></span> <span data-ttu-id="13bb3-256">したがって、このクラスにパラメーターを渡す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="13bb3-256">Therefore, you do not have to pass any parameters to this class.</span></span>
-   <span data-ttu-id="13bb3-257">**出力/ターゲット** – 関数が実行された後、ターゲット エンティティのゼロまたは複数のフィールドが設定されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-257">**Output/Target** – After the function is run, zero or multiple fields in the target entity are set.</span></span> <span data-ttu-id="13bb3-258">関数の戻り値の型は、ターゲットに設定する必要がある 0 以上の値を保持できるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="13bb3-258">The return type of the function is a container that can hold zero or more values that should be set on the target.</span></span>

<span data-ttu-id="13bb3-259">特定の関数によって返される値のシーケンスは、**getReturnFields** メソッドで定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-259">The sequence of values that are returned by a particular function must be defined in the **getReturnFields** method.</span></span>
#### <a name="create-a-getreturnfields-method"></a><span data-ttu-id="13bb3-260">getReturnFields メソッドの作成</span><span class="sxs-lookup"><span data-stu-id="13bb3-260">Create a getReturnFields method</span></span>

<span data-ttu-id="13bb3-261">**getReturnFields** メソッドは、データ移行に使用される関数の既定の出力またはターゲット フィールドを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-261">The **getReturnFields** method is used to specify the default output or target fields for the functions that are used for data migration.</span></span> <span data-ttu-id="13bb3-262">メソッドのパラメーターの一部は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="13bb3-262">Some of the parameters for the method are as follows:</span></span>
-   <span data-ttu-id="13bb3-263">\_エンティティ – エンティティの名前。</span><span class="sxs-lookup"><span data-stu-id="13bb3-263">\_entity – The name of the entity.</span></span>
-   <span data-ttu-id="13bb3-264">\_名前 – 機能の名前。</span><span class="sxs-lookup"><span data-stu-id="13bb3-264">\_name – The name of the function.</span></span>

<span data-ttu-id="13bb3-265">**戻る**: この方法では次の情報を戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-265">**Return**: This method must return the following information:</span></span>
-   <span data-ttu-id="13bb3-266">コンテナー</span><span class="sxs-lookup"><span data-stu-id="13bb3-266">A container</span></span>
-   <span data-ttu-id="13bb3-267">メソッドを実行する必要のあるターゲット エンティティ クエリ内のデータ ソースの名前</span><span class="sxs-lookup"><span data-stu-id="13bb3-267">The name of the data source in the target entity query with which the method should be run</span></span>
-   <span data-ttu-id="13bb3-268">関数によって初期化されるターゲット エンティティ クエリ内のデータ ソース フィールドの名前</span><span class="sxs-lookup"><span data-stu-id="13bb3-268">The name of the data source field in the target entity query that should be initialized by the function</span></span>

#### <a name="create-an-addstaginglink-method"></a><span data-ttu-id="13bb3-269">AddStagingLink メソッドを作成する</span><span class="sxs-lookup"><span data-stu-id="13bb3-269">Create an addStagingLink method</span></span>

<span data-ttu-id="13bb3-270">**addStagingLink** メソッドは、ステージング テーブルの関係プロパティを使用してこの関係を定義できないときに、ステージング テーブルとターゲット テーブル間の関係を定義するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-270">The **addStagingLink** method is used to define the relationship between the staging table and target table when this relationship cannot be defined by using the relations property of the staging table.</span></span> <span data-ttu-id="13bb3-271">ターゲット クエリとステージング レコードは、このメソッドで使用できます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-271">The target query and the staging record are available in the method.</span></span> <span data-ttu-id="13bb3-272">したがって、コードを使用してターゲットとステージングの間の範囲を追加できます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-272">Therefore, the range between target and staging can be added by using code.</span></span> <span data-ttu-id="13bb3-273">次の例は、**DMFEmployeeEntityClass** クラスの **addStagingLink** メソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="13bb3-273">The following example shows the **addStagingLink** method for the **DMFEmployeeEntityClass** class.</span></span>
<span data-ttu-id="13bb3-274">public Query addStagingLink(Query query, TableId _entityTableId, Common _staging) { QueryBuildDataSource qbd; qbd = query.dataSourceTable(tableNum(HcmWorker)); qbd.addRange(fieldNum(HcmWorker,PersonnelNumber)).value(_staging.(fieldNum(DMFEmployeeEntity,PersonnelNumber))); return query; }</span><span class="sxs-lookup"><span data-stu-id="13bb3-274">public Query addStagingLink(Query query, TableId _entityTableId, Common _staging) { QueryBuildDataSource qbd; qbd = query.dataSourceTable(tableNum(HcmWorker)); qbd.addRange(fieldNum(HcmWorker,PersonnelNumber)).value(_staging.(fieldNum(DMFEmployeeEntity,PersonnelNumber))); return query; }</span></span> 

#### <a name="create-a-query-to-populate-the-target-entity"></a><span data-ttu-id="13bb3-275">ターゲット エンティティを設定するためのクエリを作成する</span><span class="sxs-lookup"><span data-stu-id="13bb3-275">Create a query to populate the target entity</span></span>

<span data-ttu-id="13bb3-276">エンティティを表すテーブルは、ターゲット エンティティ クエリに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-276">Tables that represent the entity should be added to the target entity query.</span></span> <span data-ttu-id="13bb3-277">手動プロジェクトのクエリを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-277">You must add a query for manual projects.</span></span>

### <a name="create-an-enum-field-in-the-target-entity"></a><span data-ttu-id="13bb3-278">ターゲットエンティティに列挙フィールドを作成する</span><span class="sxs-lookup"><span data-stu-id="13bb3-278">Create an enum field in the target entity</span></span>

<span data-ttu-id="13bb3-279">ターゲット エンティティの列挙フィールドは、ステージング テーブルの文字列フィールドで表されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-279">The enum field in the target entity is represented by a string field in the staging table.</span></span> <span data-ttu-id="13bb3-280">列挙型ラベル文字列を保持する適切な長さの文字列型の新しい EDT を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-280">You must create a new EDT of the string type that is of appropriate length to hold the enum label strings.</span></span> <span data-ttu-id="13bb3-281">ターゲットエンティティの列挙型フィールドとステージング テーブルの文字列フィールドの間の変換は、データ インポート/エクスポート フレームワークによって自動的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-281">The conversion between the enum field in the target entity and the string field in the staging table is handled automatically by the Data Import/Export Framework.</span></span>

### <a name="handle-the-refrecid-field"></a><span data-ttu-id="13bb3-282">RefRecId フィールドを処理します</span><span class="sxs-lookup"><span data-stu-id="13bb3-282">Handle the RefRecId field</span></span>

<span data-ttu-id="13bb3-283">ステージング テーブルには、通常、ナチュラル キー (文字列) があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-283">A staging table usually has natural keys (strings).</span></span> <span data-ttu-id="13bb3-284">ターゲット テーブルに他のテーブルの Recid が含まれている場合、RecId ナチュラル キーに変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-284">If the target table contains fields that are RecIds from other tables, you must convert the natural key to a RecId.</span></span> <span data-ttu-id="13bb3-285">この場合、2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-285">In this case, you have two options:</span></span>
-   <span data-ttu-id="13bb3-286">照会テーブルをターゲット エンティティ クエリに追加することができるように、データ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-286">Add a data source, so that the referenced table can be added to the target entity query.</span></span>
-   <span data-ttu-id="13bb3-287">機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-287">Create a function.</span></span>

#### <a name="add-a-data-source"></a><span data-ttu-id="13bb3-288">データ ソースの追加</span><span class="sxs-lookup"><span data-stu-id="13bb3-288">Add a data source</span></span>

<span data-ttu-id="13bb3-289">照会テーブルをターゲット エンティティ クエリに追加することができるように、データ ソースを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-289">You can add a data source, so that the referenced table can be added to the target entity query.</span></span> <span data-ttu-id="13bb3-290">たとえば、ターゲットの **VendTable** テーブルには **VendExceptionGroup** が含まれています。それは **VendExceptionGroup** テーブルから取得される RecId です。</span><span class="sxs-lookup"><span data-stu-id="13bb3-290">For example, the target **VendTable** table contains **VendExceptionGroup**, which is a RecId that comes from the **VendExceptionGroup** table.</span></span> <span data-ttu-id="13bb3-291">この場合、ステージング テーブルに **VendExceptionGroup** を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-291">In this case, the staging table must include **VendExceptionGroup**.</span></span> <span data-ttu-id="13bb3-292">**VendExceptionGroup** テーブルは、**VendTable** データ ソースの下でターゲット エンティティ クエリにも追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-292">The **VendExceptionGroup** table must also be added to the target entity query, under the **VendTable** data source.</span></span> <span data-ttu-id="13bb3-293">**VendTable** と **VendExecptionGroup** の間の関係は手動で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-293">The relationship between **VendTable** and **VendExecptionGroup** must be specified manually.</span></span> <span data-ttu-id="13bb3-294">リレーションシップは **VendTable** の **RefRecId** と **VendExceptionGroup** の [RecId] の間にしてください。</span><span class="sxs-lookup"><span data-stu-id="13bb3-294">The relationship should be between the **RefRecId** field in **VendTable** and the RecId on **VendExceptionGroup**.</span></span> <span data-ttu-id="13bb3-295">ステージング フィールド **DMFVendorEntity.VendExecptionGroup** は、**DMFVendorTargetEntity. DS:VendExceptionGroup.VendExceptionGroup** のターゲット フィールド クエリにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-295">The staging field **DMFVendorEntity.VendExecptionGroup** must be mapped to the target field query for **DMFVendorTargetEntity. DS:VendExceptionGroup.VendExceptionGroup**.</span></span> <span data-ttu-id="13bb3-296">多くのシナリオでは、ターゲット クエリのフィールドの名前がステージング フィールドと同じである場合、マッピングは自動的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-296">In many scenarios, if the name of the field in the target query is same as the staging field, the mapping is performed automatically.</span></span> <span data-ttu-id="13bb3-297">ターゲット フィールドをステージング フィールドに手動でマッピングすることもできます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-297">You can also manually map target fields to staging fields.</span></span>

#### <a name="create-a-function"></a><span data-ttu-id="13bb3-298">機能の作成</span><span class="sxs-lookup"><span data-stu-id="13bb3-298">Create a function</span></span>

<span data-ttu-id="13bb3-299">エンティティ クラスで関数を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-299">You can create a function on the entity class.</span></span> <span data-ttu-id="13bb3-300">ステージング テーブルの RefRecId フィールドの関連フィールドは、ステージング テーブルのナチュラル キーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-300">The related fields for the RefRecId field on the staging table should be natural keys from the staging table.</span></span> <span data-ttu-id="13bb3-301">文字列を RecId に変換するには、エンティティ クラスでメソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="13bb3-301">You create a method on the entity class to convert the string to a RecId.</span></span> <span data-ttu-id="13bb3-302">たとえば、CustTable テーブルには、CompanyNAFCode テーブルの RecId である CompanyNAFCode フィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-302">For example, the CustTable table includes the CompanyNAFCode field, which is the RecId of the CompanyNAFCode table.</span></span> <span data-ttu-id="13bb3-303">この場合、文字列 (DMFCustomerEntity.CompanyIdNAF) を RecId (CompanyNAFCode.RecID) に変換するために DMFCustomerEntityClass に関数を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="13bb3-303">In this case, you can create a function on DMFCustomerEntityClass to convert the string (DMFCustomerEntity.CompanyIdNAF) to a RecId (CompanyNAFCode.RecID).</span></span> <span data-ttu-id="13bb3-304">関数を作成するときは、ステージング テーブルのフィールド グループを作成する必要があり、エンティティ クラスの **getReturnFields** メソッドで、ターゲット上に戻りフィールドを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13bb3-304">When you create a function, you must create a field group for the staging table, and the return fields on the target must be specified in the **getReturnFields** method in the entity class.</span></span>







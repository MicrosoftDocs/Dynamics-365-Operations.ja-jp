---
title: "倉庫のコンフィギュレーション テンプレートを使用して、倉庫を設定する"
description: "このトピックでは倉庫のコンフィギュレーション テンプレートを使用して、倉庫を設定する方法について説明します。"
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 90a4276f261affd8c90f2deb7cd0b773d43e5485
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="87672-103">倉庫のコンフィギュレーション テンプレートを使用して、倉庫を設定する</span><span class="sxs-lookup"><span data-stu-id="87672-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="87672-104">このトピックでは倉庫のコンフィギュレーション テンプレートを使用して、倉庫を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87672-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="87672-105">使用できる事前定義されたコンフィギュレーション テンプレートが複数あります。</span><span class="sxs-lookup"><span data-stu-id="87672-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="87672-106">これらのテンプレートを使用する方法の詳細については、[コンフィギュレーション データ テンプレート](../../dev-itpro/data-entities/configuration-data-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87672-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="87672-107">コンフィギュレーション テンプレートが役に立つ際のシナリオ</span><span class="sxs-lookup"><span data-stu-id="87672-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="87672-108">コンフィギュレーション テンプレートがさまざまなシナリオで役に立ちます</span><span class="sxs-lookup"><span data-stu-id="87672-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="87672-109">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="87672-109">Here are some examples:</span></span>

- <span data-ttu-id="87672-110">テスト環境でのコンフィギュレーション設定を完了およびテストし、実稼働環境に設定をコピーするようになります。</span><span class="sxs-lookup"><span data-stu-id="87672-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="87672-111">倉庫設定を複数の法人に展開する、または同じ法人で新しい倉庫を作成します。</span><span class="sxs-lookup"><span data-stu-id="87672-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="87672-112">倉庫機能のデモをすばやく準備します。</span><span class="sxs-lookup"><span data-stu-id="87672-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="87672-113">既存品目および倉庫が、在庫管理での機能の代わりに、倉庫管理での機能を使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="87672-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="87672-114">このトピックでは、これらのシナリオの 1 つ目に注目します。</span><span class="sxs-lookup"><span data-stu-id="87672-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="87672-115">テスト環境から実稼働環境にコンフィギュレーション設定をコピーするため、コンフィギュレーション テンプレートを使用する方法を表示します。</span><span class="sxs-lookup"><span data-stu-id="87672-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="87672-116">テスト環境から実稼働環境にコンフィギュレーション設定をコピーします。</span><span class="sxs-lookup"><span data-stu-id="87672-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="87672-117">このシナリオでは、倉庫および一部のトランザクション処理のコンフィギュレーション設定は、既にテスト環境で存在します。</span><span class="sxs-lookup"><span data-stu-id="87672-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="87672-118">テスト環境から実稼働環境に倉庫のコンフィギュレーション設定をコピーするようになります。</span><span class="sxs-lookup"><span data-stu-id="87672-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="87672-119">コンフィギュレーション設定をコピーするときに、その他の関連する設定データを含めることが重要です。</span><span class="sxs-lookup"><span data-stu-id="87672-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="87672-120">たとえば、テスト環境から設定をコピーすることにより製品を設定します。</span><span class="sxs-lookup"><span data-stu-id="87672-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="87672-121">ただし、その製品を作成する前に、製品の固定のピッキング場所を設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="87672-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="87672-122">個々のコンフィギュレーション テンプレートがこの依存関係のタイプをサポートしていませんが、既定のデータ テンプレートはそれをサポートします。</span><span class="sxs-lookup"><span data-stu-id="87672-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="87672-123">これらの既定のデータ テンプレートは、コンフィギュレーション プロセスで簡単に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="87672-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="87672-124">既定の倉庫テンプレートのエクスポート</span><span class="sxs-lookup"><span data-stu-id="87672-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="87672-125">**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="87672-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87672-126">最初にこのワークスペースを使用する場合、続行する前に、すべてのデータ エンティティを読み込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="87672-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="87672-127">**テンプレート** タイルをオンにし、**既定のテンプレートの読み込み** を選択して既定のテンプレートを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="87672-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87672-128">**既定のテンプレートの読み込み** は、**拡張** 表示でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="87672-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="87672-129">**フレームワーク パラメーター** を選択し、次に **既定値の表示**フィールドで、**拡張表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87672-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="87672-130">既定のテンプレートが読み込まれた後、業務要件を満たすように変更することができます。</span><span class="sxs-lookup"><span data-stu-id="87672-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87672-131">既定のテンプレートを読み込み、テンプレートをインポートするには、システム管理者のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="87672-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="87672-132">この要求は、テンプレートにべてのエンティティが正しく読み込まれていることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="87672-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="87672-133">ユーザーが、会社の特定のデータのエクスポート元である法人にいることを確認します。</span><span class="sxs-lookup"><span data-stu-id="87672-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="87672-134">ワークスペースで、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87672-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="87672-135">新しいエクスポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="87672-135">Create a new export project.</span></span>
7. <span data-ttu-id="87672-136">**+ テンプレートの追加** を選択し、**400 - WMS** 既定の倉庫 テンプレートを検索します。</span><span class="sxs-lookup"><span data-stu-id="87672-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="87672-137">このテンプレートは、倉庫コンフィギュレーションのデータ エンティティを追加します。</span><span class="sxs-lookup"><span data-stu-id="87672-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87672-138">エクスポートしているデータをフィルター処理する必要がある場合 (たとえば、特定の倉庫に関連付けられているデータのみエクスポートする)、各データ エンティティを評価し、クエリを通してフィルタ処理を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87672-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="87672-139">または、すべてのデータをエクスポートし、エクスポート先のファイルで必要でないレコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="87672-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="87672-140">[**エクスポート**] の選択</span><span class="sxs-lookup"><span data-stu-id="87672-140">Select **Export**.</span></span> <span data-ttu-id="87672-141">プロジェクト内のすべてのデータ エンティティに関連付けられているデータがエクスポートされます。</span><span class="sxs-lookup"><span data-stu-id="87672-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="87672-142">データ パッケージの zip ファイルをダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="87672-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="87672-143">このファイルには、選択した形式 (たとえば、Excel 形式) のすべてのデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="87672-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="87672-144">前述の通り、データ パッケージ ファイル内のいくつかのレコードは、実稼働環境にインポートする前に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87672-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="87672-145">レコードを更新する場合は、ファイル名を変更しないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="87672-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="87672-146">倉庫のコンフィギュレーション設定をインポートします。</span><span class="sxs-lookup"><span data-stu-id="87672-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="87672-147">対象の環境で、ユーザーが倉庫データをインポートする会社にいることを確認します。</span><span class="sxs-lookup"><span data-stu-id="87672-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="87672-148">インポートを実行する前に、任意のデータの依存関係を識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87672-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="87672-149">たとえば、**倉庫管理** テンプレートには、**倉庫廃棄コード** と呼ばれるデータ エンティティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="87672-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="87672-150">このエンティティには、**廃棄コード** 設定ページ (**倉庫管理** > **設定** > **モバイル デバイス** > **廃棄コード**) に関連付けられているデータを含みます。</span><span class="sxs-lookup"><span data-stu-id="87672-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="87672-151">既存の設定が既に、販売注文の返品プロセスを処理する場合、**返品廃棄コード** フィールドに値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="87672-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="87672-152">このフィールドの廃棄コードは、**廃棄コード** データ エンティティに関連付けられており、**販売とマーケティング** テンプレートの一部です。</span><span class="sxs-lookup"><span data-stu-id="87672-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="87672-153">**廃棄コード** データ エンティティからのデータが **倉庫廃棄コード** フィールドからのデータの前にインポートされていない場合、インポートは失敗します。</span><span class="sxs-lookup"><span data-stu-id="87672-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="87672-154">**データ管理** ワークスペースで、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87672-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="87672-155">新しいインポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="87672-155">Create a new import project.</span></span>
4. <span data-ttu-id="87672-156">**+ ファイルの追加** を選択し、データ パッケージの zip ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="87672-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="87672-157">[**インポート**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="87672-157">Select **Import**.</span></span> <span data-ttu-id="87672-158">**拡張** 表示で、**フィルター** オプションを使用して、インポート中に発生する可能性のある問題の概要をすばやく取得します。</span><span class="sxs-lookup"><span data-stu-id="87672-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="87672-159">**実行表示** ログは、インポートされる各データ エンティティに関する詳細情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="87672-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="87672-160">ステージング データの表示を使用して、対象データにすばやくアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="87672-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="87672-161">この方法で、アプリケーションの関連するページで、インポートされたデータがどのようなものかを表示できます。</span><span class="sxs-lookup"><span data-stu-id="87672-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="87672-162">既定のデータ テンプレートを使用する場合、各データ エンティティのインポート順序が事前定義された方法で動作し、すべての依存データが最初にインポートされることを保証する助けになります。</span><span class="sxs-lookup"><span data-stu-id="87672-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="87672-163">カスタム データ エンティティがプロジェクトの一部である場合、正しい順序が定義されているのを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87672-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="87672-164">詳細については、「[コンフィギュレーション データ テンプレート](../../dev-itpro/data-entities/configuration-data-templates.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="87672-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="related-topic"></a><span data-ttu-id="87672-165">関連するトピック</span><span class="sxs-lookup"><span data-stu-id="87672-165">Related topic</span></span>

[<span data-ttu-id="87672-166">コンフィギュレーション データ テンプレート</span><span class="sxs-lookup"><span data-stu-id="87672-166">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)


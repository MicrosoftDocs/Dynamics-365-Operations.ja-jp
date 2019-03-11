---
title: コンフィギュレーション データ プロジェクト
description: このトピックでは、構成データ プロジェクトと構成データ テンプレートの概要、およびそれらを使用して Dynamics 365 for Finance and Operations のインスタンス間で企業の構成データを移動するプロセスの概要を示します。
author: mikefalkner
manager: AnnBe
ms.date: 09/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 77523
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2017-07-31
ms.dyn365.ops.version: Platform update 7
ms.openlocfilehash: a67ac88653f0a41e192435b60b36a64549b8fac3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368436"
---
# <a name="configuration-data-projects"></a><span data-ttu-id="fe742-103">コンフィギュレーション データ プロジェクト</span><span class="sxs-lookup"><span data-stu-id="fe742-103">Configuration data projects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe742-104">コンフィギュレーション データ プロジェクトは、Microsoft Dynamics 365 for Finance and Operations のインスタンス間での会社のコンフィギュレーション データ移動を管理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fe742-104">Configuration data projects are used to manage the movement of company configuration data between instances of Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="fe742-105">これらは、次のシナリオをサポートすることを目的としています。</span><span class="sxs-lookup"><span data-stu-id="fe742-105">They are intended to support the following scenarios:</span></span>

- <span data-ttu-id="fe742-106">**コンフィギュレーションのエクスポート** - エンティティのコンフィギュレーションを作成し、データ管理フレームワークを使用してコンフィギュレーションをパッケージにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="fe742-106">**Export of configurations** – Create configurations of entities, and use the data management framework to export the configurations to a package.</span></span>
- <span data-ttu-id="fe742-107">**コンフィギュレーションのインポート** – コンフィギュレーション パッケージをアップロードして、およびデータ管理フレームワークを使用して、パッケージをインポートします。</span><span class="sxs-lookup"><span data-stu-id="fe742-107">**Import of configurations** – Upload a configuration package, and use the data management framework to import the package.</span></span>

<span data-ttu-id="fe742-108">コンフィギュレーション データ パッケージは、**データ管理**ワークスペースでデータのインポートおよびエクスポート プロジェクトを使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="fe742-108">Configuration data packages are created by using data import and export projects in the **Data management** workspace.</span></span> <span data-ttu-id="fe742-109">**データのインポート** および **データのエクスポート** ページを使用すると、会社と共有データの移動を管理するために必要なエンティティを追加および削除できます。</span><span class="sxs-lookup"><span data-stu-id="fe742-109">The **Data import** and **Data export** pages let you add and remove the entities that you require in order to manage the movement of company and shared data.</span></span> <span data-ttu-id="fe742-110">コンフィギュレーションでエンティティの一覧を作成した後は、データ管理フレームワークを使用してパッケージを作成するコンフィギュレーションをエクスポート、またはインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="fe742-110">After you create the list of entities in your configuration, you can export or import the configuration by using the data management framework to create a package.</span></span> <span data-ttu-id="fe742-111">パッケージをローカルにエクスポートしてから、インポートのために別のインスタンスに移動することができます。</span><span class="sxs-lookup"><span data-stu-id="fe742-111">You can export packages locally and then move them to another instance for import.</span></span>

<span data-ttu-id="fe742-112">コンフィグレーション データ テンプレートは、データ プロジェクトで使用できる各モジュール領域のエンティティの事前定義リストです。</span><span class="sxs-lookup"><span data-stu-id="fe742-112">Configuration data templates are predefined lists of entities for each module area that can be used in a data project.</span></span> <span data-ttu-id="fe742-113">**データ管理** ワークスペース内の **テンプレート** ページを使用することにより、これらのテンプレートを作成、表示、および修正することができます。</span><span class="sxs-lookup"><span data-stu-id="fe742-113">You can create, view, and modify these templates by using the **Template** page in the **Data management** workspace.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe742-114">既定のコンフィギュレーション テンプレートは、Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 2017 年 7 月更新プログラムで配信されました。</span><span class="sxs-lookup"><span data-stu-id="fe742-114">Default configuration templates were delivered in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update.</span></span> <span data-ttu-id="fe742-115">コンフィギュレーション データ プロジェクト機能は、Microsoft Dynamics 365 for Operations プラットフォーム更新プログラム 7 でが利用可能です。</span><span class="sxs-lookup"><span data-stu-id="fe742-115">The Configuration data project feature is available in Microsoft Dynamics 365 for Operations platform update 7.</span></span> <span data-ttu-id="fe742-116">現在の製品リリースで、自分自身のテンプレートを作成および使用することができます。</span><span class="sxs-lookup"><span data-stu-id="fe742-116">You can create and use your own templates in the current product release.</span></span>

## <a name="process-for-working-with-configuration-data-projects"></a><span data-ttu-id="fe742-117">コンフィギュレーション データ プロジェクトを操作するためのプロセス</span><span class="sxs-lookup"><span data-stu-id="fe742-117">Process for working with configuration data projects</span></span>
<span data-ttu-id="fe742-118">コンフィギュレーション データ プロジェクトの使用を開始するときは、このプロセスに従うことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fe742-118">We recommend that you follow this process when you start to use configuration data projects.</span></span>

1. <span data-ttu-id="fe742-119">新しいデータ コンフィギュレーション ユーザー インターフェイス (UI) を取得して既定のファイル拡張子を設定することで、システムを設定します。</span><span class="sxs-lookup"><span data-stu-id="fe742-119">Set up your system by getting the new data configuration user interface (UI) and setting default file extensions.</span></span>
2. <span data-ttu-id="fe742-120">エクスポートおよびインポートの両方の構成テンプレートを設定します。</span><span class="sxs-lookup"><span data-stu-id="fe742-120">Set up configuration templates for both export and import.</span></span>
3. <span data-ttu-id="fe742-121">エクスポート用のコンフィギュレーション データ プロジェクトを作成して実行します。</span><span class="sxs-lookup"><span data-stu-id="fe742-121">Create and run a configuration data project for export.</span></span>
4. <span data-ttu-id="fe742-122">インポート用のコンフィギュレーション データ プロジェクトを作成して実行します。</span><span class="sxs-lookup"><span data-stu-id="fe742-122">Create and run a configuration data project for import.</span></span>

<span data-ttu-id="fe742-123">このトピックの残りの部分では、**データ管理**ワークスペースについて説明し、データ構成プロジェクト用にシステムを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fe742-123">The rest of this topic describes the **Data management** workspace and explains how to set up your system for data configuration projects.</span></span>

<span data-ttu-id="fe742-124">コンフィギュレーション テンプレートを設定する場合は、[コンフィギュレーション データ テンプレート](configuration-data-templates.md)を参照します。</span><span class="sxs-lookup"><span data-stu-id="fe742-124">If you're ready to set up a configuration template, see [Configuration data templates](configuration-data-templates.md).</span></span> <span data-ttu-id="fe742-125">構成データ プロジェクトを作成して実行する準備ができている場合は、[会社間コンフィギュレーション データをコピーする](copy-configuration.md)を参照します。</span><span class="sxs-lookup"><span data-stu-id="fe742-125">If you're ready to create and run a configuration data project, see [Copy configuration data from one company to another](copy-configuration.md).</span></span>

## <a name="data-management-workspace-overview"></a><span data-ttu-id="fe742-126">データ管理ワークスペースの概要</span><span class="sxs-lookup"><span data-stu-id="fe742-126">Data management workspace overview</span></span>
<span data-ttu-id="fe742-127">**データ管理** ワークスペースは、データ管理の重要なタスクへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="fe742-127">The **Data management** workspace provides access to important tasks for data management.</span></span> <span data-ttu-id="fe742-128">また、プロジェクトおよびプロジェクト実行タスクに関する情報も提供します。</span><span class="sxs-lookup"><span data-stu-id="fe742-128">It also provides information about projects and project execution tasks.</span></span>

<span data-ttu-id="fe742-129">コンフィギュレーション データ プロジェクトを作成した後、**データ管理**ワークスペースの**データ プロジェクト**グリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe742-129">After you've created a configuration data project, it appears in the **Data projects** grid in the **Data management** workspace.</span></span> <span data-ttu-id="fe742-130">プロジェクトごとに、コンフィギュレーション (インポートまたはエクスポート) のタイプ、およびプロジェクト カテゴリ (**プロジェクト**、**コンフィギュレーション**、**統合**、または**その他**) が表示されます。</span><span class="sxs-lookup"><span data-stu-id="fe742-130">For each project, the type of configuration (import or export) and the project category (**Project**, **Configuration**, **Integration**, or **Other**) are shown.</span></span> <span data-ttu-id="fe742-131">適切なプロジェクトでフィルター処理するには、グリッドの左側にある選択を使用します。</span><span class="sxs-lookup"><span data-stu-id="fe742-131">Use the selections to the left of the grid to filter by the appropriate project.</span></span>

<span data-ttu-id="fe742-132">プロジェクトを開くには、プロジェクトを選択し、**プロジェクトの読み込み** を選択して、**インポートまたはエクスポート** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="fe742-132">To open a project, select the project, and then select **Load project** to open the **Import or export** page.</span></span> <span data-ttu-id="fe742-133">**削除** ボタンを使用して、選択したプロジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="fe742-133">Use the **Delete** button to delete the selected projects.</span></span> <span data-ttu-id="fe742-134">また、**ダウンロード** ボタンを使用してプロジェクト定義をダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="fe742-134">You can also download the project definitions by using the **Download** button.</span></span>

<span data-ttu-id="fe742-135">**ジョブ履歴** を使用して、実行したプロジェクトの詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="fe742-135">Use **Job history** to find more details about the projects that you've run.</span></span> <span data-ttu-id="fe742-136">データ プロジェクトが実行された日付でフィルター処理するには、データ範囲フィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="fe742-136">Use the data range filters to filter by the dates when data projects were run.</span></span> <span data-ttu-id="fe742-137">実行の詳細を表示するには、ジョブを選択してから **実行の詳細** メニューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="fe742-137">You can view execution details by selecting a job and then using the **Execution details** menu.</span></span>

<span data-ttu-id="fe742-138">タスクのエクスポートについては、**ダウンロード ページ**ボタンを使用して、データ ワークスペースからデータをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="fe742-138">For export tasks, you can download the data from the workspace by using the **Download page** button.</span></span>

## <a name="set-up-your-system-to-manage-configuration-data-projects"></a><span data-ttu-id="fe742-139">システムを設定し、コンフィギュレーション データ プロジェクトを管理</span><span class="sxs-lookup"><span data-stu-id="fe742-139">Set up your system to manage configuration data projects</span></span>
<span data-ttu-id="fe742-140">開始する前に、新しいデータ コンフィギュレーション UI にアクセスできること、および既定データ ソースを設定していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fe742-140">Before you begin, make sure that you have access to the new data configuration UI, and that you've set up the default data sources.</span></span>

### <a name="get-the-new-ui"></a><span data-ttu-id="fe742-141">新しい UI を取得します</span><span class="sxs-lookup"><span data-stu-id="fe742-141">Get the new UI</span></span>
<span data-ttu-id="fe742-142">**データ管理** ワークスペースと、**テンプレート**、**データ エクスポート**、および**データ インポート** のページを更新して、これらが構成管理をサポートするようにしました。</span><span class="sxs-lookup"><span data-stu-id="fe742-142">We have updated the **Data management** workspace, and the **Template**, **Data export**, and **Data import** pages, so that they support configuration management.</span></span> <span data-ttu-id="fe742-143">ただし、更新されたページは拡張ビューでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="fe742-143">However, the updated pages are available only in Enhanced view.</span></span> <span data-ttu-id="fe742-144">標準ビューは、以前のリリースから更新されていません。</span><span class="sxs-lookup"><span data-stu-id="fe742-144">Standard view hasn't been updated from previous releases.</span></span>

#### <a name="change-to-the-new-ui-for-a-single-user"></a><span data-ttu-id="fe742-145">単一のユーザー用の新しい UI への変更</span><span class="sxs-lookup"><span data-stu-id="fe742-145">Change to the new UI for a single user</span></span>
<span data-ttu-id="fe742-146">システムのデフォルトの表示設定を変更して、法人ごとにユーザーの設定を保存できます。</span><span class="sxs-lookup"><span data-stu-id="fe742-146">The system's default view settings can be changed to save settings for each user per each legal entity.</span></span> <span data-ttu-id="fe742-147">単一ユーザーのビューを切り替えるには、**データ管理** ワークスペースの各ページで **拡張ビュー** ボタンを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe742-147">To switch the view for a single user, the user must select the **Enhanced view** button on each page in the **Data management** workspace.</span></span>

#### <a name="change-to-the-new-ui-for-all-users-in-all-legal-entities"></a><span data-ttu-id="fe742-148">すべての法人の、すべてのユーザー用の新しい UI への変更</span><span class="sxs-lookup"><span data-stu-id="fe742-148">Change to the new UI for all users in all legal entities</span></span>
1. <span data-ttu-id="fe742-149">**データ管理**ワークスペースで、**フレームワーク パラメーター** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fe742-149">In the **Data management** workspace, select the **Framework parameters** tile.</span></span>
2. <span data-ttu-id="fe742-150">すべてのユーザーおよび法人の**既定の表示**設定を**標準**から**拡張**に変更します。</span><span class="sxs-lookup"><span data-stu-id="fe742-150">Change the **View default** setting from **Standard** to **Enhanced** for all users and legal entities.</span></span>

### <a name="set-file-extensions-for-default-data-sources"></a><span data-ttu-id="fe742-151">既定のデータ ソースのファイル拡張子を設定</span><span class="sxs-lookup"><span data-stu-id="fe742-151">Set file extensions for default data sources</span></span>
<span data-ttu-id="fe742-152">**テンプレート** および **インポート/エクスポート** ページでは、データ管理フレームワークを使用して作成されたファイルを選択することでエンティティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="fe742-152">The **Template** and **Import/export** pages let you add entities by selecting a file that was created by using the data management framework.</span></span> <span data-ttu-id="fe742-153">さまざまな種類のデータ ソースに対して、次の既定のファイル名拡張子を追加しました。</span><span class="sxs-lookup"><span data-stu-id="fe742-153">We have added the following default file name extensions for the various types of data sources:</span></span>

- <span data-ttu-id="fe742-154">Microsoft Excel データ ソースの .xlsx</span><span class="sxs-lookup"><span data-stu-id="fe742-154">.xlsx for Microsoft Excel data sources</span></span>
- <span data-ttu-id="fe742-155">パッケージ データ ソースの .zip</span><span class="sxs-lookup"><span data-stu-id="fe742-155">.zip for package data sources</span></span>
- <span data-ttu-id="fe742-156">XML データ ソースの .xml</span><span class="sxs-lookup"><span data-stu-id="fe742-156">.xml for XML data sources</span></span>
- <span data-ttu-id="fe742-157">コンマ区切り値 (CSV) のデータ ソースの .csv</span><span class="sxs-lookup"><span data-stu-id="fe742-157">.csv for comma-separated values (CSV) data sources</span></span>
- <span data-ttu-id="fe742-158">区切りデータ ソースの .txt</span><span class="sxs-lookup"><span data-stu-id="fe742-158">.txt for delimited data sources</span></span>

<span data-ttu-id="fe742-159">他のファイル名拡張子を使用する場合は、ターゲットのデータ形式として使用される既定ファイル名の拡張子があるので、データ ソースを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fe742-159">If you want to use other file name extensions, you must update your data sources so that they have a default file name extension that will be used as the target data format.</span></span>

1. <span data-ttu-id="fe742-160">**データ管理**ワークスペースで、**データ ソースの構成**タイルを選択してから**データ ソース**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fe742-160">In the **Data management** workspace, select the **Configure data sources** tile, and then select **Data sources**.</span></span>
2. <span data-ttu-id="fe742-161">適切なデータ ソースに既定のファイル名拡張子を追加します。</span><span class="sxs-lookup"><span data-stu-id="fe742-161">Add a default file name extension to the appropriate data source.</span></span>

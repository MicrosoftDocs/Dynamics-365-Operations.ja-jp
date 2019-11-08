---
title: RCS および ER のアプリケーション固有のメタデータを準備する
description: このトピックでは、Regulatory configuration service (RCS) および電子レポート (ER) のアプリケーション固有のメタデータを準備する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 74750397dc344d74c018c27114357d3d05b95b7e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550110"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="d9b2d-103">RCS および ER のアプリケーション固有のメタデータを準備する</span><span class="sxs-lookup"><span data-stu-id="d9b2d-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d9b2d-104">このトピックでは、次のタスクの例について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="d9b2d-105">RCS で使用できるアプリケーション メタデータを準備する</span><span class="sxs-lookup"><span data-stu-id="d9b2d-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="d9b2d-106">ER コンフィギュレーションを使用してアプリケーション メタデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="d9b2d-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="d9b2d-107">接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="d9b2d-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="d9b2d-108">RCS で使用できるアプリケーション メタデータを準備する</span><span class="sxs-lookup"><span data-stu-id="d9b2d-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="d9b2d-109">次の手順では、**システム管理者**または**電子報告開発者**のロールを持つユーザーが、Regulatory Configuration Service (RCS) の ER モデル マッピング コンフィギュレーションを設計するためのアプリケーションのメタデータを含む、新しい電子レポート (ER) コンフィギュレーションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="d9b2d-110">この例で作成されたサンプル ER モデル マッピング コンフィギュレーションは、対外貿易トランザクションにアクセスするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="d9b2d-111">この例では、RCS を使用して、対外貿易ビジネスのドメインからの情報を含む電子ドキュメントを生成するアプリケーションの ER ソリューションを設計します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="d9b2d-112">ER データ モデルと必要なデータ ソース間のマッピングを指定するには、RCS でアプリケーションのメタデータにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="d9b2d-113">そのため、ER ソリューション設計プロセスの一部として、選択したビジネス ドメインに対する生成 ER レポートに現在必要とされるすべてのメタデータを含む、新しい ER メタデータ コンフィギュレーションを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="d9b2d-114">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順はすべての会社で実行することができます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="d9b2d-115">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d9b2d-116">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d9b2d-117">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)という手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="d9b2d-118">**メタデータ コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="d9b2d-119">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="d9b2d-120">ドロップダウン ダイアログ ボックスの**名前**フィールドに名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="d9b2d-121">この例では、**対外貿易メタデータ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="d9b2d-122">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="d9b2d-123">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-123">Select **Designer**.</span></span>
8. <span data-ttu-id="d9b2d-124">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9b2d-125">アプリケーション全体に対して、または選択したモデル、モジュールに対して、すべてのメタデータを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="d9b2d-126">どちらの場合も、レコードのテーブル、列挙体、および拡張データ型 (EDTs) のメタデータが自動的に追加されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="d9b2d-127">メタデータの追加のタイプが必要な場合、手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="d9b2d-128">対外貿易トランザクションに関連付けられたメタデータをいくつか追加し、手動でメタデータ項目を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="d9b2d-129">**データソースを追加 \> テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="d9b2d-130">**名前**フィールドにある**イントラスタット**の値をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="d9b2d-131">**イントラスタット** テーブル レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="d9b2d-132">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-132">Select **OK**.</span></span>

<span data-ttu-id="d9b2d-133">イントラスタットのレコード テーブルに関するメタデータ情報を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="d9b2d-134">ツリーで、**テーブル レコード イントラスタット\> \>リレーション \> イントラスタットコモディティ (テーブル レコード EcoResCategory)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="d9b2d-135">**メタデータの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9b2d-136">選択したレコード テーブルに必要な関係に関するメタデータは、手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="d9b2d-137">**データソースの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="d9b2d-138">**列挙**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="d9b2d-139">**名前**フィールドにある **IntrastatDirection** の値をフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="d9b2d-140">**IntrastatDirection** の列挙レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="d9b2d-141">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-141">Select **OK**.</span></span>
20. <span data-ttu-id="d9b2d-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-142">Select **Save**.</span></span>
21. <span data-ttu-id="d9b2d-143">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-143">Close the page.</span></span>
22. <span data-ttu-id="d9b2d-144">メタデータ コンフィギュレーションのドラフト バージョンの完了</span><span class="sxs-lookup"><span data-stu-id="d9b2d-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="d9b2d-145">**ステータスの変更 \> 完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="d9b2d-146">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-146">Select **OK**.</span></span>
    3. <span data-ttu-id="d9b2d-147">完了したバージョン 1 を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="d9b2d-148">完了したバージョンのメタデータ コンフィギュレーションをアプリケーションから XML ファイルとしてエクスポートする</span><span class="sxs-lookup"><span data-stu-id="d9b2d-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="d9b2d-149">**交換 \> XML ファイルとしてエクスポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="d9b2d-150">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-150">Select **OK**.</span></span>

<span data-ttu-id="d9b2d-151">作成した ER メタデータ コンフィギュレーションは、**対外貿易メタデータ .xml** ファイルとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="d9b2d-152">これをRCSにインポートすることで、対外貿易ビジネス ドメインのメタデータのソースとして使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="d9b2d-153">この情報に基づいて、アプリケーション メタデータと ER データ モデルとの間のマッピングを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="d9b2d-154">ER コンフィギュレーションを使用してアプリケーション メタデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="d9b2d-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="d9b2d-155">次の手順は、**システム管理者**または**電子レポート開発者**のロールを持つ RCS ユーザーが、アプリケーションのメタデータを使用して新しい ER モデル マッピングをデザインする方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="d9b2d-156">アプリケーション メタデータには、対外貿易トランザクションにアクセスするためのサンプル メタデータ セットを含む ER メタデータ コンフィギュレーションを使用してアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="d9b2d-157">これを完了する前に、ます次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="d9b2d-158">コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け</span><span class="sxs-lookup"><span data-stu-id="d9b2d-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="d9b2d-159">RCS で使用できるアプリケーション メタデータを準備する</span><span class="sxs-lookup"><span data-stu-id="d9b2d-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="d9b2d-160">**すべてのワークスペース \> 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d9b2d-161">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ**としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="d9b2d-162">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)という手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="d9b2d-163">アプリケーションのメタデータを含む ER メタデータ コンフィギュレーションをインポートします。これは対外貿易ビジネス ドメインのための電子ドキュメントを生成するようコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="d9b2d-164">このトピックの前の部分 [RCS で使用できるアプリケーション メタデータを準備する](#prepare-application-metadata-that-can-be-used-in-rcs)の手順で ER メタデータ コンフィギュレーションを作成し、XML ファイルとしてエクスポートしました。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="d9b2d-165">**メタデータ コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="d9b2d-166">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="d9b2d-167">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="d9b2d-168">参照し、**対外貿易メタデータ .xml** ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="d9b2d-169">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-169">Select **OK**.</span></span>
    6. <span data-ttu-id="d9b2d-170">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-170">Close the page.</span></span>

4. <span data-ttu-id="d9b2d-171">データ モデル コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="d9b2d-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="d9b2d-172">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="d9b2d-173">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="d9b2d-174">ドロップ ダウン ダイアログ ボックスの**名前**フィールドに、**対外貿易モデル**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="d9b2d-175">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="d9b2d-176">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="d9b2d-177">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d9b2d-178">**名前**フィールドに、**ルート**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="d9b2d-179">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="d9b2d-180">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d9b2d-181">**名前**フィールドに、**トランザクション**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="d9b2d-182">**品目タイプ** フィールドで、**レコード リスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="d9b2d-183">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="d9b2d-184">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d9b2d-185">**名前**フィールドに、**コモディティ コード**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="d9b2d-186">**品目タイプ**フィールドで、**文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="d9b2d-187">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-187">Select **Add**.</span></span>

    9. <span data-ttu-id="d9b2d-188">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d9b2d-189">名前フィールドに、**請求金額**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="d9b2d-190">**品目タイプ** フィールドで、**実数**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="d9b2d-191">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-191">Select **Add**.</span></span>

    10. <span data-ttu-id="d9b2d-192">**新規**を選択すると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="d9b2d-193">**名前**フィールドに、**日付**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="d9b2d-194">**品目タイプ** フィールドで、**日付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="d9b2d-195">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="d9b2d-196">**追加 \> ルート参照**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="d9b2d-197">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-197">Select **OK**.</span></span>
    13. <span data-ttu-id="d9b2d-198">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-198">Select **Save**.</span></span>
    14. <span data-ttu-id="d9b2d-199">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-199">Close the page.</span></span>
    15. <span data-ttu-id="d9b2d-200">**ステータスの変更 \> 完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="d9b2d-201">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-201">Select **OK**.</span></span>

5. <span data-ttu-id="d9b2d-202">モデル マッピング コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="d9b2d-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="d9b2d-203">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="d9b2d-204">ドロップ ダウン ダイアログ ボックスの**新規**フィールドに、**データ モデル対外貿易モデルに基づいたモデル マッピング**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="d9b2d-205">**名前**フィールドに、**対外貿易マッピング**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="d9b2d-206">**コンフィギュレーションの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="d9b2d-207">**必要条件**のクイック タブで、**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="d9b2d-208">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-208">Select **New**.</span></span>
    7. <span data-ttu-id="d9b2d-209">**必要条件のコンポーネント タイプ** フィールドで、**コンフィギュレーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="d9b2d-210">**対外貿易メタデータ** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="d9b2d-211">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-211">Select **Save**.</span></span> <span data-ttu-id="d9b2d-212">参照が**対外貿易メタデータ** コンフィギュレーションのバージョン 1 に追加されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="d9b2d-213">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="d9b2d-214">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-214">Close the page.</span></span>
    11. <span data-ttu-id="d9b2d-215">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="d9b2d-216">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="d9b2d-217">ツリーで、**Dynamics 365 for Operations \> テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="d9b2d-218">**ルートの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="d9b2d-219">**名前**フィールドに、**イントラスタット**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="d9b2d-220">**イントラスタット** テーブル レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="d9b2d-221">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d9b2d-222">現在使用されているメタデータ セットに追加されたテーブルは 2 つだけなので、2 つのテーブルのみが提供されています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="d9b2d-223">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="d9b2d-224">ツリーで、**イントラスタット \> AmountMST** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="d9b2d-225">ツリーで、**トランザクション = イントラスタット \> 請求金額**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="d9b2d-226">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="d9b2d-227">ツリーで、**イントラスタット \> TransDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="d9b2d-228">ツリーで、**トランザクション = イントラスタット \> 日付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="d9b2d-229">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="d9b2d-230">ツリーで、**イントラスタット \> \>リレーション \> イントラスタットコモディティ \> コード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="d9b2d-231">ツリーで、**トランザクション = イントラスタット \> コモディティ コード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="d9b2d-232">**バインド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="d9b2d-233">**検証**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="d9b2d-234">検証が完了した後、参照された ER メタデータ コンフィギュレーションのアプリケーション メタデータの詳細を使用して説明されているデータ ソース項目に、データ モデルの要素が正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="d9b2d-235">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-235">Select **Save**.</span></span>

<span data-ttu-id="d9b2d-236">必要に応じて、アプリケーションで既存のメタデータ セットを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="d9b2d-237">その後、新しい完了版の ER メタデータ コンフィギュレーションをエクスポートし、それを RCS にインポートして、インポートされたメタデータ コンフィギュレーションの新しいバージョンを参照してコンフィギュレーション済みモデル マッピングの前提条件を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="d9b2d-238">アプリケーション メタデータに関する情報を取得するこの方法は、ローカルに展開されたアプリケーションで利用できる唯一の方法です (ローカル ビジネス データ \[LBD\]、またはオンプレミスの場合、配置モデルはアプリケーションに使用されます)。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="d9b2d-239">接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="d9b2d-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="d9b2d-240">次の手順は、**システム管理者**または**電子レポート開発者**のロールを持つ RCS ユーザーが、アプリケーションのメタデータを使用して新しい ER モデル マッピングをデザインする方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="d9b2d-241">アプリケーションのメタデータは、RCS 接続されたアプリケーションを使用してオンラインでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="d9b2d-242">サンプル ER モデルマッピングは、対外貿易トランザクションにアクセスするようにコンフィギュレーションされます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="d9b2d-243">この手順を完了するには、まず RCS にある [コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="d9b2d-244">このトピックの前の部分にある [ER コンフィギュレーションを使用してアプリケーション メタデータにアクセスする](#access-application-metadata-by-using-an-er-configuration)の手順をまだ完了していない場合は、[Dynamics 365 for Finance and Operations 8.1 電子レポート タスク ガイド](https://go.microsoft.com/fwlink/?linkid=2082739)のページに移動し、次の ER コンフィギュレーション ファイルを事前にダウンロードし、ローカルに保存してください : **対外貿易メタデータ .xml**、**対外貿易モデル .xml**、および**対外貿易マッピング .xml**</span><span class="sxs-lookup"><span data-stu-id="d9b2d-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="d9b2d-245">必要な ER コンフィギュレーションの取得</span><span class="sxs-lookup"><span data-stu-id="d9b2d-245">Get required ER configurations</span></span>

<span data-ttu-id="d9b2d-246">このトピックの前の部分にある [ER コンフィギュレーションを使用したアプリケーション メタデータへのアクセス](#access-application-metadata-by-using-an-er-configuration)手順を既に完了している場合、現在の RCS インスタンスに必要なすべての ER コンフィギュレーション (対外貿易メタデータ、モデルおよびマッピングのコンフィギュレーション) は、既に存在しています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="d9b2d-247">その場合は、この手順をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="d9b2d-248">**すべてのワークスペース \> 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d9b2d-249">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="d9b2d-250">**対外貿易メタデータ .xml**、**対外貿易モデル .xml**、**対外貿易マッピング .xml** コンフィギュレーション ファイルを読み込み、それぞれについて、次の一連の手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="d9b2d-251">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="d9b2d-252">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="d9b2d-253">**参照**を選択し、ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="d9b2d-254">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="d9b2d-255">アプリケーションとの接続を登録する</span><span class="sxs-lookup"><span data-stu-id="d9b2d-255">Register the connection with the application</span></span>

1. <span data-ttu-id="d9b2d-256">**すべてのワークスペース \> 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d9b2d-257">**接続アプリケーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="d9b2d-258">コンフィギュレーションされたアプリケーションが Microsoft Azure に基づいており、RCS ユーザーが一般にアクセスできることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="d9b2d-259">現在の RCS ユーザーが、選択されたアプリケーションにアクセスでき、アプリケーションのメタデータにアクセスするための権限を持つユーザーとして登録されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="d9b2d-260">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-260">Select **New**.</span></span>
5. <span data-ttu-id="d9b2d-261">**名前**フィールドに、接続されたアプリケーションの名前として **MyConnectedApp** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="d9b2d-262">**アプリケーション** フィールドに、アプリケーションの URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="d9b2d-263">**テナント** フィールドに、アプリケーションのプロバイダーを指定します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="d9b2d-264">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-264">Select **Save**.</span></span> 
9. <span data-ttu-id="d9b2d-265">コンフィギュレーションされたアプリケーションへの接続を確認するときは、**リモート アプリケーションへの接続**ページで、**ここを選択して、選択したリモート アプリケーションに接続する** のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="d9b2d-266">**接続の確認**を選択し、コンフィギュレーションされたアプリケーションへのアクセスを検証します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="d9b2d-267">**閉じる**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-267">Select **Close**.</span></span>

<span data-ttu-id="d9b2d-268">この手順を完了して接続検証に成功すると、コンフィギュレーションされたアプリケーションのバージョンとテナントの詳細が、現在のグリッドで更新されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="d9b2d-269">既存のモデル マッピング コンフィギュレーションを確認する</span><span class="sxs-lookup"><span data-stu-id="d9b2d-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="d9b2d-270">**すべてのワークスペース \> 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="d9b2d-271">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="d9b2d-272">ツリーで、**対外貿易モデル \> 対外貿易マッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="d9b2d-273">**必要条件**のクイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9b2d-274">現在、このマッピングはメタデータのコンフィギュレーションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="d9b2d-275">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="d9b2d-276">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-276">Select **Designer**.</span></span>
5. <span data-ttu-id="d9b2d-277">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-277">Select **Designer**.</span></span>
6. <span data-ttu-id="d9b2d-278">ツリーで、**Dynamics 365 for Operations \> テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="d9b2d-279">**ルートの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-279">Select **Add root**.</span></span>
8. <span data-ttu-id="d9b2d-280">**テーブル** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9b2d-281">現在、このマッピングはメタデータのコンフィギュレーションを参照しています。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="d9b2d-282">このコンフィギュレーションのアプリケーション メタデータは、このモデル マッピングをデザインするときに提供されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="d9b2d-283">**キャンセル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="d9b2d-284">接続されたアプリケーションをモデル マッピングに割り当てる</span><span class="sxs-lookup"><span data-stu-id="d9b2d-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="d9b2d-285">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-285">Select **Edit**.</span></span>
2. <span data-ttu-id="d9b2d-286">**接続されたアプリケーション フィールド**で、**MyConnectedApp** アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9b2d-287">このマッピングは、選択した接続アプリケーションのメタデータを参照します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="d9b2d-288">マッピングがメタデータ コンフィギュレーションと接続されたアプリケーションを同時に参照する場合、接続されたアプリケーションのメタデータが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="d9b2d-289">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-289">Select **Designer**.</span></span>
4. <span data-ttu-id="d9b2d-290">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-290">Select **Designer**.</span></span>
5. <span data-ttu-id="d9b2d-291">ツリーで、**Dynamics 365 for Operations \> テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="d9b2d-292">**ルートの追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-292">Select **Add root**.</span></span>
7. <span data-ttu-id="d9b2d-293">**テーブル** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d9b2d-294">この時点で、マッピングは、割り当てられた接続アプリケーションのすべてのメタデータを使用するため、2 つ以上のアプリケーション テーブルが提供されました。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="d9b2d-295">**キャンセル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="d9b2d-296">**検証**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-296">Select **Validate**.</span></span>

<span data-ttu-id="d9b2d-297">これで、このマッピングに割り当てられた接続アプリケーションのメタデータの詳細を使用して、説明されているデータ ソース項目にデータ モデルの要素が正常にバインドされました。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="d9b2d-298">異なるバージョンのアプリケーションのメタデータを使用してこのモデル マッピングを評価する必要がある場合は、接続されている別のアプリケーションを登録しモデル マッピングに割り当て、新しいメタデータに対してそれを検証します。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9b2d-299">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d9b2d-299">Additional resources</span></span>

<span data-ttu-id="d9b2d-300">または、アプリケーションの **RCS で使用できるアプリケーション メタデータを準備する**タスク ガイド、**ER コンフィギュレーションを使用してアプリケーション メタデータにアクセスする**および RCS の**接続されているアプリケーションを使用してアプリケーション メタデータにアクセスする**タスク ガイドを再生することができます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="d9b2d-301">これらのタスク ガイドは、[Dynamics 365 for Finance and Operations 8.1 電子レポート タスク ガイド](https://go.microsoft.com/fwlink/?linkid=2082739)のページからダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="d9b2d-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>

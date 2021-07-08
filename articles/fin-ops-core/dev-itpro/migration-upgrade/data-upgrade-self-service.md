---
title: AX 2012 からのアップグレード - セルフサービス環境のデータ アップグレード
description: このトピックでは、セルフサービス環境で Microsoft Dynamics AX 2012 からデータ アップグレードを行う方法について説明します。
author: sarvanisathish
ms.date: 06/09/2021
ms.topic: article
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2021-06-30
ms.openlocfilehash: 159b9c0419434fe4b59593e364a79df0c1c20f22
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222498"
---
# <a name="upgrade-from-ax-2012---data-upgrade-in-self-service-environments"></a><span data-ttu-id="d3e9d-103">AX 2012 からのアップグレード - セルフサービス環境のデータ アップグレード</span><span class="sxs-lookup"><span data-stu-id="d3e9d-103">Upgrade from AX 2012 - Data upgrade in self-service environments</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="d3e9d-104">このトピックに記載されている一部またはすべての機能は、プレビュー リリースの一部として使用可能です。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-104">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="d3e9d-105">コンテンツおよび機能は、変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-105">The content and the functionality are subject to change.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d3e9d-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="d3e9d-106">Prerequisites</span></span>

1. <span data-ttu-id="d3e9d-107">まだインストールされていない場合、[.NET Core ソフトウェア開発キット (SDK)](https://dotnet.microsoft.com/download/dotnet/thank-you/sdk-3.1.409-windows-x64-installer) をダウンロードしてインストールしてください。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-107">Download and install the [.NET core software development kit (SDK)](https://dotnet.microsoft.com/download/dotnet/thank-you/sdk-3.1.409-windows-x64-installer) if it isn't already installed.</span></span>
2. <span data-ttu-id="d3e9d-108">Microsoft Dynamics Lifecycle Services (LCS) でセルフサービス環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-108">Create a self-service environment in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d3e9d-109">この環境は、**配置済み** 状態である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-109">The environment should be in a **Deployed** state.</span></span>
3. <span data-ttu-id="d3e9d-110">レプリケーション機能がインストールされ、ソース SQL Server インスタンスに対して有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-110">Make sure that the replication feature is installed and enabled for the source SQL Server instance.</span></span> <span data-ttu-id="d3e9d-111">レプリケーションが有効かどうかを確認するには、次の SQL スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-111">To determine whether replication is enabled, run the following SQL script.</span></span>

    ```sql
    -- If @installed is 0, replication must be added to the SQL Server installation.

    USE master;

    GO

    DECLARE @installed int;

    EXEC @installed = sys.sp_MS_replication_installed;

    SELECT @installed;
    ```

    <span data-ttu-id="d3e9d-112">レプリケーション コンポーネントがインストールされていない場合は、[SQL Server レプリケーションのインストール](/sql/database-engine/install-windows/install-sql-server-replication?view=sql-server-ver15)の手順に従いインストールします。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-112">If the replication components aren't installed, follow the steps in [Install SQL Server replication](/sql/database-engine/install-windows/install-sql-server-replication?view=sql-server-ver15) to install them.</span></span>

4. <span data-ttu-id="d3e9d-113">ソース データベース サーバーで SQL Server Agent を有効にして起動します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-113">Enable and start the SQL Server Agent on the source database server.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3e9d-114">ユーザーはソース データベースで **DB\_Owner** 権限を持ち、マスター データベースおよびソース データベースにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-114">A user should have the **DB\_Owner** privilege in the source database, and should have access to the master database and the source database.</span></span>

5. <span data-ttu-id="d3e9d-115">**Migration Toolkit の設定:** ソース データベース テーブルの一部をターゲット データベースに複製しない場合は、IgnoreTables.xml ファイルでそれらを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-115">**Migration toolkit setup:** If you don't want some of the source database tables to be replicated in the target database, you can specify them in the IgnoreTables.xml file.</span></span> <span data-ttu-id="d3e9d-116">同様に、一部の関数を複製しない場合は、IgnoreFunctions.xml ファイルでそれらを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-116">Likewise, if you don't want some of the functions to be replicated, you can specify them in the IgnoreFunctions.xml file.</span></span>

    - <span data-ttu-id="d3e9d-117">**IgnoreTables.xml ファイルのパス:** Data\\IgnoreTables.xml</span><span class="sxs-lookup"><span data-stu-id="d3e9d-117">**Path of the IgnoreTables.xml file:** Data\\IgnoreTables.xml</span></span>
    - <span data-ttu-id="d3e9d-118">**IgnoreFunctions.xml ファイルのパス:** Data\\IgnoreFunctions.xml</span><span class="sxs-lookup"><span data-stu-id="d3e9d-118">**Path of the IgnoreFunctions.xml file:** Data\\IgnoreFunctions.xml</span></span>

    <span data-ttu-id="d3e9d-119">次の例は、XML ファイルのテーブルおよび関数を指定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-119">The following examples show how to specify tables and functions in the XML files.</span></span>

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <IgnoreTables>
        <Name>
            <Table>USERADDHISTORYLIST</Table>
            <Table>TAXRECONCILIATIONREPORTTMP</Table>
            <Table>CASELOG</Table>
            <Table>SHAREDCATEGORYROLETYPE</Table>
            <Table>VATCSREPORTXMLATTRIBUTE_CZ</Table>
        </Name>
    </IgnoreTables>
    ```

    ```xml
    <?xml version="1.0" encoding="utf-8"?>
    <IgnoreFunctions>
        <Name>
            <Function>if_WHSInventReserveUnionDelta</Function>
        </Name>
    </IgnoreFunctions>
    ```

    > [!WARNING]
    > <span data-ttu-id="d3e9d-120">これらの XML ファイルで指定されたテーブルと関数はターゲット データベースに複製されないため、同じ形式に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-120">The tables and functions that are specified in these XML files won't be replicated in the target database, and the same format should be followed.</span></span>

> [!NOTE]
> <span data-ttu-id="d3e9d-121">上記の手順のいずれかが任意の時点で失敗した場合は、このトピック後半の[例外](#exceptions)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-121">If any of the preceding steps fail at any point, see the [Exceptions](#exceptions) section later in this topic.</span></span>

## <a name="configure-replication"></a><span data-ttu-id="d3e9d-122">レプリケーションの構成</span><span class="sxs-lookup"><span data-stu-id="d3e9d-122">Configure replication</span></span>

<span data-ttu-id="d3e9d-123">レプリケーション プロセスを開始する前に、LCS 環境の作成時に **配置済み** 状態になる点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-123">Before you begin the replication process, note that the LCS environment will be in a **Deployed** state when it's created.</span></span>

1. <span data-ttu-id="d3e9d-124">**AX2012DataUpgradeToolKit.exe** アプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-124">Run the **AX2012DataUpgradeToolKit.exe** application.</span></span>

    <span data-ttu-id="d3e9d-125">コンソール ウィンドウが開き、認証用の Microsoft サインイン ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-125">A console window is opened, and you're redirected to the Microsoft sign-in page for authentication.</span></span>

2. <span data-ttu-id="d3e9d-126">LCS へのサインインに使用する資格情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-126">Provide the credentials that are used to sign in to LCS.</span></span>

    <span data-ttu-id="d3e9d-127">認証に成功すると、ブラウザに以下のメッセージが表示されます。「認証が完了しました。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-127">After you're successfully authenticated, you receive the following message in the browser: "Authentication complete.</span></span> <span data-ttu-id="d3e9d-128">アプリケーションに戻ることができます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-128">You can return to the application.</span></span> <span data-ttu-id="d3e9d-129">このブラウザー タブを自由に閉じることができます。」</span><span class="sxs-lookup"><span data-stu-id="d3e9d-129">Feel free to close this browser tab."</span></span>

    <span data-ttu-id="d3e9d-130">これでブラウザー タブを閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-130">You can now close the browser tab.</span></span>

3. <span data-ttu-id="d3e9d-131">コンソール ウィンドウに **プロジェクト ID** の値を入力し、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-131">In the console window, enter the **Project-Id** value, and then select **Enter**.</span></span> <span data-ttu-id="d3e9d-132">次に、**環境 ID** の値を指定し、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-132">Then provide the **Environment-Id** value, and select **Enter**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3e9d-133">**プロジェクト ID** および **環境 ID** の値は、LCS の **環境の管理** ページで確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-133">You can find the **Project-Id** and **Environment-Id** values on the **Manage environment** page in LCS.</span></span> <span data-ttu-id="d3e9d-134">また、**環境 ID** の値は、**環境の詳細** ページでも確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-134">You can also find the **Environment-Id** value on the **Environment details** page.</span></span>

<span data-ttu-id="d3e9d-135">アプリケーションは LCS 環境に接続し、ターゲット データベースへの接続を検証します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-135">The application connects to the LCS environment and validates the connection to the target database.</span></span>

<span data-ttu-id="d3e9d-136">検証が成功すると、アプリケーションには、データ アップグレード プロセスの手順に対応する一連のメニュー オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-136">After the validation is successful, the application presents a set of menu options that correspond to the steps in the data upgrade process.</span></span> <span data-ttu-id="d3e9d-137">データのレプリケーションおよびアップグレードを完了するには、次の手順を順番に実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-137">To complete the data replication and upgrade, you should perform these steps in order.</span></span>

1. <span data-ttu-id="d3e9d-138">**データ アップグレードの準備: 環境の設定活動**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-138">**Data upgrade preparation: Environment setup activity**</span></span>

    <span data-ttu-id="d3e9d-139">この手順では、次の情報の入力が求められます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-139">This step prompts you for the following information:</span></span>

    - <span data-ttu-id="d3e9d-140">ソース データベースの詳細:</span><span class="sxs-lookup"><span data-stu-id="d3e9d-140">Details of the source database:</span></span>

        - <span data-ttu-id="d3e9d-141">ソース サーバー (*サーバー名\\サーバーインスタンス* の形式)</span><span class="sxs-lookup"><span data-stu-id="d3e9d-141">Source server (in the format *servername\\serverinstance*)</span></span>
        - <span data-ttu-id="d3e9d-142">ソース データベース名</span><span class="sxs-lookup"><span data-stu-id="d3e9d-142">Source database name</span></span>
        - <span data-ttu-id="d3e9d-143">ユーザー名</span><span class="sxs-lookup"><span data-stu-id="d3e9d-143">User name</span></span>
        - <span data-ttu-id="d3e9d-144">パスワード</span><span class="sxs-lookup"><span data-stu-id="d3e9d-144">Password</span></span>

    - <span data-ttu-id="d3e9d-145">ソース データベース サーバーの IP アドレス (許可リスト用)</span><span class="sxs-lookup"><span data-stu-id="d3e9d-145">IP address of the source database server (for the allowlist)</span></span>
    - <span data-ttu-id="d3e9d-146">配布データベース パス (**D:\\SQLServer\\Data** など)</span><span class="sxs-lookup"><span data-stu-id="d3e9d-146">Distribution database path (for example, **D:\\SQLServer\\Data**)</span></span>
    - <span data-ttu-id="d3e9d-147">レプリケーション スナップショット パス **(D:\\SQLServer\\Snapshot** など)</span><span class="sxs-lookup"><span data-stu-id="d3e9d-147">Replication snapshot path (for example, **D:\\SQLServer\\Snapshot**)</span></span>

    > [!WARNING]
    > <span data-ttu-id="d3e9d-148">指定した配布データベースとレプリケーション スナップショット パスには、十分な容量が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-148">The specified distribution database and replication snapshot paths should have enough space.</span></span> <span data-ttu-id="d3e9d-149">容量は、少なくともソース データベースのサイズにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-149">We recommend that the amount of space be at least the size of the source database.</span></span>

    <span data-ttu-id="d3e9d-150">この手順では、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-150">This step performs the following actions:</span></span>

    - <span data-ttu-id="d3e9d-151">ソース データベースへの接続を検証します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-151">Validate the connection to the source database.</span></span>
    - <span data-ttu-id="d3e9d-152">AX 2012 データベースのバージョンを検証します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-152">Validate the version of the AX 2012 database.</span></span>
    - <span data-ttu-id="d3e9d-153">ソースの IP アドレスを承認します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-153">Authorize the source IP address.</span></span>
    - <span data-ttu-id="d3e9d-154">ターゲット データベースを検証します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-154">Validate the target databases.</span></span>

2. <span data-ttu-id="d3e9d-155">**データ アップグレードの準備: データ アップグレードのターゲット環境を準備する**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-155">**Data upgrade preparation: Prepare the target environment for the data upgrade**</span></span>

    <span data-ttu-id="d3e9d-156">この手順により、LCS の環境の状態が **配置済み** から **レプリケーションの準備完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-156">This step changes the state of the LCS environment from **Deployed** to **Ready for replication**.</span></span>

3. <span data-ttu-id="d3e9d-157">**レプリケーション : ターゲット データベースのクリーンアップ**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-157">**Replication: Clean-up target database**</span></span>

    <span data-ttu-id="d3e9d-158">この手順では、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-158">This step performs the following actions:</span></span>

    1. <span data-ttu-id="d3e9d-159">LCS 環境の状態を、**レプリケーションの準備完了** から **レプリケーションの処理中** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-159">Change the state of the LCS environment from **Ready for replication** to **Replication in progress**.</span></span>
    2. <span data-ttu-id="d3e9d-160">ターゲット データベースのテーブル、ビュー、ストアド プロシージャ、およびユーザー定義関数のデータベース所有者 (dbo) オブジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-160">Delete the database owner (dbo) objects of tables, views, stored procedures, and user-defined functions in the target database.</span></span>

4. <span data-ttu-id="d3e9d-161">**レプリケーション: 配布の設定**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-161">**Replication: Set up distributor**</span></span>

    <span data-ttu-id="d3e9d-162">この手順により、ソース サーバーの **システム データベース** フォルダー下に配布データベースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-162">This step creates a distribution database under the **System Databases** folder on the source server.</span></span> <span data-ttu-id="d3e9d-163">この配布データベースは、レプリケーションに使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-163">This distribution database is used for replication.</span></span>

5. <span data-ttu-id="d3e9d-164">**レプリケーション: 主キー テーブル用にパブリケーションを設定する**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-164">**Replication: Set up publication for primary key tables**</span></span>

    <span data-ttu-id="d3e9d-165">この手順により、ソース サーバーの **レプリケーション** フォルダーの下に主キー テーブル用のパブリケーションが作成され、ターゲット データベースに複製されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-165">This step creates publications for primary key tables under the **Replication** folder on the source server and replicates them in the target database.</span></span> <span data-ttu-id="d3e9d-166">**ignore-table** エントリが指定されている場合、指定されたテーブルはレプリケーションから除外されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-166">If  any **ignore-table** entries are specified, the specified tables are exempted from replication.</span></span>

    <span data-ttu-id="d3e9d-167">**作成済みパブリッシャー:** AXDB\_PUB\_TABLE\_Obj\_\[\*\]</span><span class="sxs-lookup"><span data-stu-id="d3e9d-167">**Created publishers:** AXDB\_PUB\_TABLE\_Obj\_\[\*\]</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3e9d-168">このレプリケーション構成ステップが完了すると、バックグラウンドで実行される SQL ジョブとして実際のデータ レプリケーションが発生します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-168">After this replication configuration step is completed, actual data replication will occur as a SQL job that runs in the background.</span></span> <span data-ttu-id="d3e9d-169">このジョブは完了するまでに少し時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-169">This job will take some time to be completed.</span></span> <span data-ttu-id="d3e9d-170">レプリケーションの状態を表示するには **'rs**' オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-170">You can view the status of the replication by providing the **'rs**' option.</span></span>

6. <span data-ttu-id="d3e9d-171">**レプリケーション: 他のオブジェクト (機能) に対するパブリケーションの設定**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-171">**Replication: Set up publication for other objects (functions)**</span></span>

    <span data-ttu-id="d3e9d-172">この手順により、他のオブジェクト (機能) に対するパブリケーションが作成され、ターゲット データベースに複製されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-172">This step creates a publication for other objects (functions) and replicates them in the target database.</span></span> <span data-ttu-id="d3e9d-173">一部の関数を複製しない場合は、IgnoreFunctions.xml ファイルでそれらを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-173">If you don't want some of the functions to be replicated, you can specify them in the IgnoreFunctions.xml file.</span></span>

    <span data-ttu-id="d3e9d-174">**作成されたパブリッシャー:** AX\_PUB\_OtherObjects</span><span class="sxs-lookup"><span data-stu-id="d3e9d-174">**Created publisher:** AX\_PUB\_OtherObjects</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3e9d-175">レプリケーションは完了までに少し時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-175">The replication will take some time to be completed.</span></span> <span data-ttu-id="d3e9d-176">レプリケーションの状態を表示するには、**'rs'** オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-176">You can view the replication status by providing the **'rs'** option.</span></span>
    >
    > <span data-ttu-id="d3e9d-177">複製する関数がない場合、パブリケーションは作成されません。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-177">If there no functions to replicate, the publication won't be created.</span></span>

    > [!WARNING]
    > <span data-ttu-id="d3e9d-178">このステップの **DataReplicationStatus** プロパティが完了として表示されるまで、次のステップに進まないでください。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-178">Don't move on to next step until the **DataReplicationStatus** property for this step is shown as completed.</span></span>

7. <span data-ttu-id="d3e9d-179">**切替: 主キーのないテーブル用にパブリケーションを設定する**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-179">**Cutover: Set up publication for non-primary key tables**</span></span>

    <span data-ttu-id="d3e9d-180">この手順では、2 つのパブリケーションを作成します。1 つは主キーのないテーブルの複製に使用され、もう 1 つはロックされたテーブルの複製に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-180">This step creates two publications: one that is used to replicate non-primary key tables, and one that is used to replicate locked tables.</span></span>

    <span data-ttu-id="d3e9d-181">**パブリケーションの名前:** AX\_PUB\_NoPKTable, AX\_PUB\_TABLE\_LockedTable</span><span class="sxs-lookup"><span data-stu-id="d3e9d-181">**Publication names:** AX\_PUB\_NoPKTable, AX\_PUB\_TABLE\_LockedTable</span></span>

    <span data-ttu-id="d3e9d-182">主キー パブリケーションの作成中に AX サービスがスキーマ ロックを取得した場合、それらのテーブルは無視され、パブリケーションから除外されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-182">If AX Service acquires a schema lock during creation of the primary key publication, those tables will be ignored and omitted from the publication.</span></span> <span data-ttu-id="d3e9d-183">これらは、一時テーブルに追加され、切替パブリケーションの作成中にレプリケーション用にマークされます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-183">They will be added to temporary tables and marked for replication during creation of the cutover publication.</span></span>

    > [!WARNING]
    > <span data-ttu-id="d3e9d-184">このステップの **DataReplicationStatus** プロパティが完了として表示されるまで、次のステップに進まないでください。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-184">Don't move on to next step until the **DataReplicationStatus** property for this step is shown as completed.</span></span>

8. <span data-ttu-id="d3e9d-185">**切替: 主キーのないパブリケーションおよび一時テーブルの削除**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-185">**Cutover: Remove non-primary key publication and temporary tables**</span></span>

    <span data-ttu-id="d3e9d-186">この手順では、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-186">This step performs the following actions:</span></span>

    1. <span data-ttu-id="d3e9d-187">ソース データベースの主キーのないテーブルに対して作成された一時テーブルをクリーンアップします。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-187">Clean up the temporary tables that were created for non-primary key tables in the source database.</span></span>
    2. <span data-ttu-id="d3e9d-188">**AX\_PUB\_NoPKTable** というパブリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-188">Delete the **AX\_PUB\_NoPKTable** publication.</span></span>

9. <span data-ttu-id="d3e9d-189">**切替: 主キーのないテーブルに対する制約の作成**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-189">**Cutover: Create constraint for non-primary key tables**</span></span>

    <span data-ttu-id="d3e9d-190">この手順では、ソース データベースから主キーのないテーブルの制約を抽出し、それらをターゲット データベースに作成します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-190">This step extracts constraints for the non-primary key tables from the source database and creates them in the target database.</span></span>

10. <span data-ttu-id="d3e9d-191">**切替: レプリケーションの設定の削除**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-191">**Cutover: Remove replication setup**</span></span>

    <span data-ttu-id="d3e9d-192">この手順では、ソース データベース、配布データベース、およびレプリケーション スナップショットに作成されたすべてのパブリケーションを削除します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-192">This step deletes all the publications that were created in the source database, the distribution database, and the replication snapshot.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d3e9d-193">例外を発生させずに **スナップショット** フォルダーを削除するには、ソース データベースで次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-193">To remove the **Snapshot** folder without causing an exception, run the following script in the source database.</span></span> <span data-ttu-id="d3e9d-194">このスクリプトを実行しなくても、受信した例外メッセージは無視できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-194">Even if you don't run this script, you can ignore the exception message that you receive.</span></span>
    >
    > ```sql
    > EXEC master.dbo.sp_configure 'show advanced options', 1
    >
    > RECONFIGURE WITH OVERRIDE
    > 
    > EXEC master.dbo.sp_configure 'xp_cmdshell', 1
    > 
    > RECONFIGURE WITH OVERRIDE
    > ```

11. <span data-ttu-id="d3e9d-195">**レプリケーション後: 環境の状態をレプリケート済に更新する**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-195">**Post-replication: Update environment state to Replicated**</span></span>

    <span data-ttu-id="d3e9d-196">この手順では、LCS 環境の状態を、**レプリケーションの処理中** から **レプリケーション完了** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-196">This step changes the state of the LCS environment from **Replication in progress** to **Replication completed**.</span></span>

12. <span data-ttu-id="d3e9d-197">**データ アップグレード: トリガー アップグレード**</span><span class="sxs-lookup"><span data-stu-id="d3e9d-197">**Data Upgrade: Trigger upgrade**</span></span>

    <span data-ttu-id="d3e9d-198">この手順では、次のアクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-198">This step performs the following actions:</span></span>

    1. <span data-ttu-id="d3e9d-199">データのアップグレードの実行中に、LCS 環境の状態を **レプリケーション完了** から **データ アップグレードの処理中** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-199">While the data upgrade is occurring, change the state of the LCS environment from **Replication completed** to **Data upgrade in progress**.</span></span>
    2. <span data-ttu-id="d3e9d-200">データのアップグレード完了後に、LCS 環境の状態を **データ アップグレードの処理中** から **配置済み** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-200">After the data upgrade is completed, change the state of the LCS environment from **Data upgrade in progress** to **Deployed**.</span></span>

    <span data-ttu-id="d3e9d-201">この時点で、データ アップグレード プロセスが完了します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-201">At this point, the data upgrade process is completed.</span></span> <span data-ttu-id="d3e9d-202">プロセス内のすべての手順の状態が完了と表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-202">The status of all the steps in the process should be shown as completed.</span></span>

<span data-ttu-id="d3e9d-203">データのアップグレードに失敗すると、LCS 環境の状態は **失敗** し、失敗した手順のメニュー オプションの状態がコンソール アプリケーションで **再開** になります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-203">If data upgrade fails, the state of the LCS environment will be **Failed**, and the status of the menu option for the failed step will be **Resume** in the console application.</span></span> <span data-ttu-id="d3e9d-204">この場合、失敗した手順を再開します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-204">In this case, resume the failed step.</span></span> <span data-ttu-id="d3e9d-205">その後、LCS 環境の状態は、**サービス** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-205">The state of the LCS environment is then changed to **Servicing**.</span></span>

## <a name="reporting-section-of-the-application"></a><span data-ttu-id="d3e9d-206">アプリケーションのレポート セクション</span><span class="sxs-lookup"><span data-stu-id="d3e9d-206">Reporting section of the application</span></span>

<span data-ttu-id="d3e9d-207">次のオプションを使用して、レプリケーションの検証、レプリケーション ステータス、およびデータ アップグレードのステータスに関するレポートを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-207">You can use the following options to review the reports of the replication validation, replication status, and data upgrade status:</span></span>

- <span data-ttu-id="d3e9d-208">**dv) レポート:** レプリケーションを検証します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-208">**dv) Report:** Validate the replication.</span></span>

    <span data-ttu-id="d3e9d-209">このオプションは、ソース サーバー データベースとターゲット サーバー データベースのテーブルとレコードの数を比較した後、レポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-209">This option compares the number of tables and records in the source server database and the target server database, and then shows the report.</span></span> <span data-ttu-id="d3e9d-210">このオプションは、手順 12 が完了した後にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-210">You should use this option only after step 12 is completed.</span></span>

    <span data-ttu-id="d3e9d-211">レポート データは、**output/PostValidationInfo.csv** で確認できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-211">You can find the report data at **output/PostValidationInfo.csv**.</span></span>

- <span data-ttu-id="d3e9d-212">**rs) レポート:** レプリケーション ステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-212">**rs) Report:** Get the replication status.</span></span>

    <span data-ttu-id="d3e9d-213">このオプションは、作成されたパブリケーションのレプリケーション プロセスのレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-213">This option shows the report of the replication process for the publications that were created.</span></span> <span data-ttu-id="d3e9d-214">このオプションは、手順 3 が開始された後 (任意のパブリケーションのレプリケーション プロセス中) にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-214">You should use this option only after step 3 is started (that is, during the replication process for any publication).</span></span>

- <span data-ttu-id="d3e9d-215">**ds) レポート:** データ アップグレードのステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-215">**ds) Report:** Get the data upgrade status.</span></span>

    <span data-ttu-id="d3e9d-216">このオプションは、データ アップグレード プロセスのレポートを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-216">This option shows the report of the data upgrade process.</span></span> <span data-ttu-id="d3e9d-217">このオプションは、手順 12 を開始した後にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-217">You should use this option only after step 12 is started.</span></span>

## <a name="tooling-section-of-the-application"></a><span data-ttu-id="d3e9d-218">アプリケーションのツール セクション</span><span class="sxs-lookup"><span data-stu-id="d3e9d-218">Tooling section of the application</span></span>

- <span data-ttu-id="d3e9d-219">**リセット:** すべてのレプリケーション構成を削除することで、レプリケーションの設定をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-219">**Reset:** Reset the replication setup by removing all the replication configurations.</span></span> <span data-ttu-id="d3e9d-220">パブリケーションおよび配布データベースが削除されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-220">Publications and the distribution database are deleted.</span></span> <span data-ttu-id="d3e9d-221">すべてのメニュー オプションのステータスが **完了** から **リセット** モードにリセットされ、レプリケーションを最初からやり直すのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-221">The status of all menu options is reset from **Completed** to **Reset** mode to help you redo the replication from the beginning.</span></span>

- <span data-ttu-id="d3e9d-222">**すべてリセット:** すべてのメニュー オプションをリセットします。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-222">**Reset-all:** Reset all the menu options.</span></span>

    <span data-ttu-id="d3e9d-223">**リセット** オプションおよび **クリア** オプションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-223">**Reset** option and **Clear** option will be performed.</span></span> <span data-ttu-id="d3e9d-224">すべてのオプションが、**開始されていません** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-224">All the options will be changed to **Not Started**.</span></span>

- <span data-ttu-id="d3e9d-225">**クリア:** 環境設定の活動をクリアします。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-225">**Clear:** Clear the environment setup activity.</span></span> <span data-ttu-id="d3e9d-226">**プロジェクト ID** の値、**環境 ID** の値、ソース データベースの詳細など、すべての情報がキャッシュからクリアされます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-226">All information is cleared from the cache, such as the **project-Id** value, **Environment-Id** value, and source database details.</span></span> <span data-ttu-id="d3e9d-227">手順 1 のステータスが **開始されていません** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-227">The status of step 1 is changed to **Not Started**.</span></span>
- <span data-ttu-id="d3e9d-228">**ヘルプ:** データ アップグレードの移行を表示します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-228">**Help:** Show the data upgrade migration.</span></span> <span data-ttu-id="d3e9d-229">メニュー オプション ステータスは、更新されたステータスと共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-229">The menu option status is shown together with the updated status.</span></span>
- <span data-ttu-id="d3e9d-230">**終了:** アプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-230">**Exit:** Close the application.</span></span>

## <a name="learn-about-the-replication-configuration-and-status-via-sql-server-management-studio"></a><span data-ttu-id="d3e9d-231">SQL Server Management Studio 経由でのレプリケーションの構成とステータスについて</span><span class="sxs-lookup"><span data-stu-id="d3e9d-231">Learn about the replication configuration and status via SQL Server Management Studio</span></span>

<span data-ttu-id="d3e9d-232">SQL Server Management Studio (SSMS) で、オブジェクト エクスプローラーに **レプリケーション** フォルダーが含まれる場合、レプリケーション機能がサーバーにインストールされ、使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-232">In SQL Server Management Studio (SSMS), if Object Explorer includes a **Replication** folder, the replication feature is installed on the server and available.</span></span>

<span data-ttu-id="d3e9d-233">データ アップグレード プロセスの手順 3 が完了したら、**レプリケーション** フォルダー下にコンフィギュレーションされたパブリッシャーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-233">After step 3 of the data upgrade process is completed, you should find the publisher configured under the **Replication** folder.</span></span> <span data-ttu-id="d3e9d-234">レプリケーション ステータスを確認するには、**レプリケーション** フォルダーを選択したまま (または右クリック)、**レプリケーション モニターの起動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-234">To learn the replication status, select and hold (or right-click) the **Replication** folder, and then select **Launch Replication Monitor**.</span></span>

- <span data-ttu-id="d3e9d-235">レプリケーション モニターには、レプリケーション用に作成されたすべてのパブリッシャーを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-235">In the replication monitor, you can view all the publishers that have been created for replication.</span></span>
- <span data-ttu-id="d3e9d-236">**スナップショット** タブには、スナップショットのステータスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-236">On the **Snapshot** tab, you can view the status of the snapshot.</span></span>
- <span data-ttu-id="d3e9d-237">詳細ログ/トランザクションを表示するには、グリッド品目をダブルタップ (またはダブルクリック) します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-237">To view the detail log/transaction, double-tap (or double-click) a grid item.</span></span>
- <span data-ttu-id="d3e9d-238">ターゲットへのデータ レプリケーションを表示するには、**すべてのサブスクリプション** タブで、グリッド品目のサブスクリプションをダブルタップ (またはダブルクリック) します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-238">To view the data replication to the target, on the **All Subscription** tab, double-tap (or double-click) the subscription from the grid item.</span></span>

## <a name="exceptions"></a><span data-ttu-id="d3e9d-239">例外</span><span class="sxs-lookup"><span data-stu-id="d3e9d-239">Exceptions</span></span>

- <span data-ttu-id="d3e9d-240">ソース データベース サーバーに配布データベースが既に存在する場合は、次の手順に従って削除します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-240">If the distribution database already exists on the source database server, follow these steps to delete it:</span></span>

    1. <span data-ttu-id="d3e9d-241">ソース データベース サーバーで、**レプリケーション** フォルダーを展開し、**ローカル パブリケーション** フォルダーを選択したまま (または右クリック)、**スクリプトの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-241">On the source database server, expand the **Replication** folder, select and hold (or right-click) the **Local Publications** folder, and then select **Generate Scripts**.</span></span>

        <span data-ttu-id="d3e9d-242">**SQLスクリプトの生成** という名前のタブが開きます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-242">A tab that is named **Generate SQL Script** is opened.</span></span>

    2. <span data-ttu-id="d3e9d-243">**コンポーネントをドロップまたは無効にする** オプションを選択し、**スクリプトの生成** フィールドで、**新しいクエリ ウィンドウを開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-243">Select the **To drop or disable the components** option, and then, in the **Generate Script** field, select **Open in New Query Window**.</span></span>

        <span data-ttu-id="d3e9d-244">新しいクエリ ウィンドウでスクリプトが開きます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-244">The script is opened in a new query window.</span></span>

    3. <span data-ttu-id="d3e9d-245">ソース データベースで、スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-245">Run the script in the source database.</span></span>

- <span data-ttu-id="d3e9d-246">パブリケーションを作成すると、スナップショットの作成が失敗し、「データベース MicrosoftDynamicsAX のオブジェクトのプリフェッチに失敗しました」というエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-246">After you create a publication, snapshot creation might fail, and you might receive the following error message: "Prefetch objects failed for Database 'MicrosoftDynamicsAX'."</span></span>

    <span data-ttu-id="d3e9d-247">この例外を修正するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-247">To fix this exception, follow these steps:</span></span>

    1. <span data-ttu-id="d3e9d-248">**レプリケーション** フォルダーを選択したまま (または右クリック)、**レプリケーション モニターの起動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-248">Select and hold (or right-click) the **Replication** folder, and then select **Launch Replication Monitor**.</span></span>
    2. <span data-ttu-id="d3e9d-249">失敗したパブリケーションを選択したまま (または右クリック)、**スナップショットの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-249">Select and hold (or right-click) the failed publication, and then select **Generate Snapshot**.</span></span>
    3. <span data-ttu-id="d3e9d-250">スナップショットが生成された後は、**'rs'** オプションを使用してレプリケーションのステータスを表示できます。</span><span class="sxs-lookup"><span data-stu-id="d3e9d-250">After the snapshot is generated, you can view the replication status by using the **'rs'** option.</span></span>

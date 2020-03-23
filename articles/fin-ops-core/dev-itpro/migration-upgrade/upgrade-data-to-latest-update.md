---
title: 開発環境またはデモ環境でデータをアップグレードする
description: このトピックでは、Finance and Operations アプリケーション リリースのアップグレードについて説明します。
author: laneswenka
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 8ce5b0d8207178f3091e3194647729042997c0dc
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124840"
---
# <a name="upgrade-data-in-development-or-demo-environments"></a><span data-ttu-id="ca20f-103">開発環境またはデモ環境でデータをアップグレードする</span><span class="sxs-lookup"><span data-stu-id="ca20f-103">Upgrade data in development or demo environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca20f-104">このトピックでは、古いデータベースを最新の Finance and Operations のアプリケーション リリースにアップグレードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-104">This topic explains how to upgrade an older database to the latest Finance and Operations application release.</span></span>

<span data-ttu-id="ca20f-105">トピックでは、レベル 1 環境の Finance and Operations データベースを最新の更新プログラムにアップグレードするプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-105">The topic provides instructions for upgrading your Finance and Operations database in a Tier 1 environment to the latest update.</span></span> <span data-ttu-id="ca20f-106">レベル 1 環境は、開発、1 ボックス、またはデモ環境とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-106">A Tier 1 environment is also known as a development, one-box, or demo environment.</span></span> 

<span data-ttu-id="ca20f-107">運用環境を含むレベル 2 以上の環境では、[最新バージョンへのセルフサービス アップグレード](self-service-upgrade.md) で説明されているセルフ サービスのアップグレード手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-107">In Tier 2 or higher environments, including Production, you will run through the self-service upgrade steps as outlined in [Self-service upgrade to the latest version](self-service-upgrade.md).</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="ca20f-108">Finance and Operations の**プラットフォーム**を最新版に更新している場合、データベースをアップグレードする必要は**ありません**。</span><span class="sxs-lookup"><span data-stu-id="ca20f-108">You do **not** have to upgrade your database if you're updating to the latest **platform** of Finance and Operations.</span></span> <span data-ttu-id="ca20f-109">プラットフォーム更新プログラムには、下位互換性のあります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-109">Platform updates are backward-compatible.</span></span> <span data-ttu-id="ca20f-110">このトピックは、Microsoft Dynamics 365 for Operations バージョン 1611 (2016 年 11 月) から Finance and Operations 8.0 へのアップグレードなど、Finance and Operations アプリケーションのリリース間でのアップグレードのプロセスに対してのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-110">This topic applies only to the process of upgrading between releases of Finance and Operations applications, such as an upgrade from Microsoft Dynamics 365 for Operations version 1611 (November 2016) to Finance and Operations 8.0.</span></span>
> - <span data-ttu-id="ca20f-111">このプロセスは、Microsoft Azure BLOB ストレージに保存されているドキュメント添付ファイルのアップグレードには適用されません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-111">This process doesn't apply to the upgrade of document attachments that are stored in Microsoft Azure blob storage.</span></span>
> - <span data-ttu-id="ca20f-112">アップグレードされたすべてのカスタム コードは、データ アップグレード プロセスを実行する前に環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-112">All upgraded custom code has to be applied on the environment before running the data upgrade process.</span></span>
> - <span data-ttu-id="ca20f-113">バージョン 8.0 以降を使用している場合、アプリケーションのバージョンの間でデータのアップグレードは行われなくなりました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-113">If you are on version 8.0 or later, there is no longer a data upgrade between application versions.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="ca20f-114">準備</span><span class="sxs-lookup"><span data-stu-id="ca20f-114">Before you begin</span></span>

1. <span data-ttu-id="ca20f-115">現在のデータベースをバックアップします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-115">Back up your current database.</span></span>
2. <span data-ttu-id="ca20f-116">更新プログラムが既に正常に実行されている機能環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-116">You must have a functional environment that is already successfully running the update.</span></span>
3. <span data-ttu-id="ca20f-117">**ソース**環境では、アップグレードする前のバージョンに応じて次の修正プログラムのいずれかをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-117">In the **source** environment, you must install one of the following hotfixes, depending on the version that you're upgrading from.</span></span> <span data-ttu-id="ca20f-118">これらの修正プログラムは、SysSetupLog ロジックの問題を修正するため、アップグレード プロセスでアップグレード元のバージョンが検出されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-118">These hotfixes correct an issue in the SysSetupLog logic, so that the upgrade process can detect the version that you're upgrading from:</span></span>

   - <span data-ttu-id="ca20f-119">**2016 年 11 月リリースからアップグレードする場合 (1611 または 7.1 とも呼ばれる、ビルド 7.1.1541.3036):** KB 4023686、"最新のアプリケーションリリースにアップグレードすると、'ソース システムのバージョン情報が見つかりませんでした' というエラーが表示されます。"</span><span class="sxs-lookup"><span data-stu-id="ca20f-119">**If you're upgrading from the November 2016 release (also known as 1611 or 7.1, build 7.1.1541.3036):** KB 4023686, "'Could not find source system version information' error when you upgrade to the latest Application Release."</span></span>
   - <span data-ttu-id="ca20f-120">**2017 年 7 月リリース からアップグレードする場合 (7.2 とも呼ばれる、ビルド 7.2.11792.56024):** このバージョンに修正プログラムは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-120">**If you're upgrading from the July 2017 release (also known as 7.2, build 7.2.11792.56024):** No hotfix is required for this version.</span></span>
   - <span data-ttu-id="ca20f-121">このステップで必要なアプリケーション修正プログラムをインストールした後は、完全なデータベース同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-121">After you install application hotfixes required in this step, run a full database synchronization.</span></span> <span data-ttu-id="ca20f-122">このステップは、ゴールデン データベース環境で特に重要です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-122">This step is especially important for golden database environments.</span></span> <span data-ttu-id="ca20f-123">データベース全体の同期では、データベースをアップグレードするときに使用される SysSetupLog テーブルを設定します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-123">A full database synchronization fills the SysSetupLog table, which is used when the database is upgraded.</span></span> <span data-ttu-id="ca20f-124">SysSetup インターフェイスはトリガーされないため、この手順で Microsoft Visual Studio からデータベース同期を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-124">Don't run the database synchronization from Microsoft Visual Studio for this step, because the SysSetup interface won't be triggered.</span></span> <span data-ttu-id="ca20f-125">SysSetup インターフェイスを起動するには、管理者の **コマンド プロンプト** ウィンドウで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-125">To trigger the SysSetup interface, run the following command from an Administrator **Command Prompt** window.</span></span>

     ```Console
     cd J:\AosService\WebRoot\bin>

     Microsoft.Dynamics.AX.Deployment.Setup.exe -bindir "J:\AosService\PackagesLocalDirectory" -metadatadir        J:\AosService\PackagesLocalDirectory -sqluser axdeployuser -sqlserver localhost -sqldatabase axdb -setupmode sync -syncmode fullall -isazuresql false -sqlpwd \<password for axdeployuser\>
     ```

4. <span data-ttu-id="ca20f-126">Microsoft Dynamics AX 2012 からアップグレードする場合は、データ アップグレードを実行する前に、移行先の環境に次のアプリケーション X++ 修正プログラムをインストールします:</span><span class="sxs-lookup"><span data-stu-id="ca20f-126">If you're upgrading from Microsoft Dynamics AX 2012, install the following application X++ hotfixes in the destination environment before you run the data upgrade:</span></span>

    - <span data-ttu-id="ca20f-127">KB 4033183 - Dynamics AX 2012 R2 または Dynamics AX 2012 R3 Pre-CU8 non-retail アップグレードは、dbo.RETAILTILLLAYOUTZONE のオブジェクトが存在しないため失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-127">KB 4033183 - Dynamics AX 2012 R2 or Dynamics AX 2012 R3 Pre-CU8 non-retail upgrade fails with Object not found for dbo.RETAILTILLLAYOUTZONE.</span></span>
    - <span data-ttu-id="ca20f-128">KB 4040692 - Microsoft Dynamics 365 for Operations 7.2 への Dynamics AX 2012 R3 のアップグレードは、SalesLineIdx に RetailSalesLine の重複インデックスが存在するため失敗しました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-128">KB 4040692 - Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Operations 7.2 upgrade fails on RetailSalesLine duplicate index on SalesLineIdx.</span></span>
    - <span data-ttu-id="ca20f-129">KB 4035490 - GeneralJournalAccountEntry MainAccount フィールドのアップグレード スクリプトに関するパフォーマンスの問題。</span><span class="sxs-lookup"><span data-stu-id="ca20f-129">KB 4035490 - Performance issue with GeneralJournalAccountEntry MainAccount field upgrade script.</span></span>

5. <span data-ttu-id="ca20f-130">標準デモ データのデータベースとして開始されるデータベースをアップグレードする場合も、次のスクリプトも実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-130">If you're upgrading a database that began as a standard demo data database, you must also run the following script.</span></span> <span data-ttu-id="ca20f-131">このステップは、デモ データにカーネル X++ クラスの不適切なレコードが含まれているため必要です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-131">This step is required, because the demo data contains bad records for some kernel X++ classes.</span></span>

    ```sql
    delete from classidtable where id >= 0xf000 and id <= 0xffff
    ```

6. <span data-ttu-id="ca20f-132">Commerce Data Exchange (CDX) のすべてのジョブが正常に実行され、チャネル データベースのクラウド バージョンで同期されていないトランザクション データがないことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-132">Make sure that all Commerce Data Exchange (CDX) jobs have been successfully run, and that there is no unsynchronized transactional data in the cloud version of the channel database.</span></span>

## <a name="select-the-correct-data-upgrade-deployable-package"></a><span data-ttu-id="ca20f-133">適切なデータ アップグレード展開可能なパッケージを選択</span><span class="sxs-lookup"><span data-stu-id="ca20f-133">Select the correct data upgrade deployable package</span></span>

<span data-ttu-id="ca20f-134">最新の更新プログラムを実行しているターゲット環境用に最新のデータ アップグレード配置可能パッケージを入手するには、Microsoft Dynamics Lifecycle Services (LCS) 共有アセット ライブラリからダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-134">To obtain the latest data upgrade deployable package for a target environment that is running the latest update, download it from the Microsoft Dynamics Lifecycle Services (LCS) Shared asset library.</span></span>
1. <span data-ttu-id="ca20f-135">[LCS](https://lcs.dynamics.com/) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-135">Sign in to [LCS](https://lcs.dynamics.com/).</span></span>
2. <span data-ttu-id="ca20f-136">**共有資産** ライブラリ タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-136">Select the **Shared asset** library tile.</span></span>
3. <span data-ttu-id="ca20f-137">共有アセット ライブラリの**アセット タイプの選択**で、**ソフトウェア配置可能パッケージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-137">In the Shared asset library, under **Select asset type**, select **Software deployable package**.</span></span>
4. <span data-ttu-id="ca20f-138">配置可能パッケージ ファイルの一覧で、アップグレードに対応するデータ アップグレード パッケージを検索します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-138">In the list of deployable package files, find the data upgrade package that corresponds to your upgrade.</span></span>

    - <span data-ttu-id="ca20f-139">AX 2012 をアップグレードする場合、パッケージ名は **AX2012DataUpgrade** から始まります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-139">If you're upgrading from AX 2012, the package name starts with **AX2012DataUpgrade**.</span></span> <span data-ttu-id="ca20f-140">アップグレードするリリースに対応するパッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-140">Select the package that corresponds to the release you are upgrading to.</span></span> <span data-ttu-id="ca20f-141">たとえば、**AX2012DataUpgrade-10-0**。</span><span class="sxs-lookup"><span data-stu-id="ca20f-141">For example, **AX2012DataUpgrade-10-0**.</span></span>
    - <span data-ttu-id="ca20f-142">以前のリリースから最新の 10.0.X リリースにアップグレードする場合、パッケージ名は **DataUpgrade-10-0** です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-142">If you're upgrading from a previous release to the latest 10.0.X release, the package name is  **DataUpgrade-10-0**.</span></span> 
    - <span data-ttu-id="ca20f-143">以前のリリースからプレビュー リリースにアップグレードする場合は、パッケージ名に PREVIEW が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-143">If you're upgrading from a previous release to a preview release, the package name contains PREVIEW.</span></span> <span data-ttu-id="ca20f-144">たとえば、**DataUpgrade-10-0-2-PREVIEW** です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-144">For example, **DataUpgrade-10-0-2-PREVIEW**.</span></span>
5. <span data-ttu-id="ca20f-145">アップグレードする先のリリースに対応するパッケージを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-145">Select the package that corresponds to the release that you are upgrading to.</span></span> 

## <a name="upgrade-the-database"></a><span data-ttu-id="ca20f-146">データベースのアップグレード</span><span class="sxs-lookup"><span data-stu-id="ca20f-146">Upgrade the database</span></span>

1. <span data-ttu-id="ca20f-147">配置可能なデータ アップグレード パッケージを、**c:\\Temp** または任意の場所に展開します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-147">Extract the data upgrade deployable package to **C:\\Temp** or a location of your choice.</span></span>
   > [!NOTE] 
   > <span data-ttu-id="ca20f-148">これが LCS に接続されている開発環境であり LCS から直接データ アップグレード プロセスを実行する予定がある場合は、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-148">Skip this step if this is a development environment that is connected to LCS and you are planning to execute the data upgrade process directly from LCS.</span></span>

2. <span data-ttu-id="ca20f-149">アップグレード対象の最新の更新プログラムが既に実行されているデモ環境または開発環境に、ソース データベース (アップグレードするデータベース) のバックアップをインポートまたは復元します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-149">Import or restore a backup of the source database (the database that you will be upgrading) to the demo or development environment that is already running the latest update that you want to upgrade to.</span></span> <span data-ttu-id="ca20f-150">既存のデータベースをそのままにして、新しいデータベースに **imported\_new** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-150">Leave the existing database in place, and name your new database **imported\_new**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca20f-151">以前のリリースで実行されている実稼働データベースのデータのアップグレードを検査する場合: 実稼働環境からデモまたは開発環境にデータベースをコピーするには [標準ユーザー受け入れテスト (UAT) データベースのコピーのエクスポート](../database/dbmovement-scenario-exportuat.md) の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-151">If you are validating the data upgrade of your production database running on the earlier release: To copy a database from a production environment back to a demo or development environment, follow the steps in [Export a copy of the standard user acceptance testing (UAT) database](../database/dbmovement-scenario-exportuat.md).</span></span>   
    > 
    > <span data-ttu-id="ca20f-152">Azure 仮想マシン (VM) 間でアップロード/ダウンロードの速度を向上するには、AzCopy を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-152">For better upload/download speed between Azure virtual machines (VMs), we recommend that you use AzCopy.</span></span> <span data-ttu-id="ca20f-153">AzCopy をダウンロードする方法、およびそれを使用して Azure blob ストアにコピーまたは Azure blob ストアからコピーする方法については、[AzCopy Command-Line Utility でデータを転送する](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-153">For information about how to download AzCopy, and how to use it to copy to or from an Azure blob store, see [Transfer data with the AzCopy Command-Line Utility](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/).</span></span>

3. <span data-ttu-id="ca20f-154">接尾語 **\_orig** を追加することによって、元のデータベースの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-154">Rename the original database by adding the suffix **\_orig**.</span></span> <span data-ttu-id="ca20f-155">元のデータベースと同じ名前になるように、新しく復元したデータベースの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-155">Rename the newly restored database so that it has the same name as the original database.</span></span> <span data-ttu-id="ca20f-156">この方法で、2 つのデータベースが場所を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-156">In this way, the two databases switch places.</span></span>

    ```sql
    ALTER DATABASE <original Dynamics 365 database> MODIFY NAME = <original Dynamics 365 database>_ORIG
    ALTER DATABASE imported_new MODIFY NAME = <original Dynamics 365 database>
    ```

4. <span data-ttu-id="ca20f-157">元のデータベースに戻す必要がある場合に備えて、ソース データベースのバックアップを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-157">Create a backup of the source database, in case you have to revert to it.</span></span> <span data-ttu-id="ca20f-158">次のステップでソース データベースを変更するためこのステップは重要です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-158">This step is important because the following steps will modify the source database.</span></span>

5. <span data-ttu-id="ca20f-159">**c:\\Temp\\DataUpgrade** フォルダー (展開可能なパッケージを以前に展開した場所) からデータ アップグレード パッケージを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-159">Execute the data upgrade package from the **C:\\Temp\\DataUpgrade** folder (the location that you extracted the deployable package to earlier).</span></span> <span data-ttu-id="ca20f-160">データ アップグレード パッケージの実行は、ソフトウェア展開可能パッケージのインストールと同様です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-160">Executing a data upgrade package is similar to installing any software deployable package.</span></span> <span data-ttu-id="ca20f-161">詳細な指示については、[コマンド ラインからの配置可能なパッケージのインストール](../deployment/install-deployable-package.md#generate-a-runbook-from-the-topology)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-161">For detailed instructions, see [Install deployable packages from the command line](../deployment/install-deployable-package.md#generate-a-runbook-from-the-topology).</span></span> <span data-ttu-id="ca20f-162">**トポロジから Runbook を生成します** というセクションで開始し、**配置可能パッケージのインストール** セクションの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-162">Start at the section titled **Generate a runbook from the topology** then execute the steps in the section **Install a deployable package**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ca20f-163">開発環境上のデータベースをアップグレードする場合は、代わりに **管理 > 適用更新** サービス機能を使用して、LCS 環境ページから直接データ アップグレード パッケージを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-163">If you are upgrading a database on a development environment, you can instead execute the data upgrade package directly from the LCS environment page, using the **Maintain > Apply Updates** servicing functionality.</span></span> <span data-ttu-id="ca20f-164">これは、ユーザーが開発用 VM のローカル管理者である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-164">This does not require the user to be a local Administrator on the development VM.</span></span> <span data-ttu-id="ca20f-165">これは LCS の[2 月](https://blogs.msdn.microsoft.com/lcs/2018/02/13/lcs-february-2018-release-1-release-notes/)リリースから利用可能です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-165">This is available as of the [February](https://blogs.msdn.microsoft.com/lcs/2018/02/13/lcs-february-2018-release-1-release-notes/) release of LCS.</span></span> 
>
> <span data-ttu-id="ca20f-166">これにより、Finance and Operations のデータベース、チャネル データベースが更新され、財務諸表データベースがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-166">This will upgrade your Finance and Operations database, channel database, and reset the Financial reporting database.</span></span>

## <a name="re-enable-sql-change-tracking"></a><span data-ttu-id="ca20f-167">SQL 変更履歴の再有効化</span><span class="sxs-lookup"><span data-stu-id="ca20f-167">Re-enable SQL change tracking</span></span>

<span data-ttu-id="ca20f-168">データベース レベルで変更追跡が有効であるかどうかを確認するため、アップグレードされたデータベースに対して次の SQL を実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-168">Run the following SQL against the upgraded database to make sure that change tracking is enabled at the database level.</span></span> <span data-ttu-id="ca20f-169">お使いのデータベースの、**データベースの変更** コマンド名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-169">You must specify the name of your database in the **alter database** command.</span></span>

```sql
ALTER DATABASE [<your AX database name>] SET CHANGE_TRACKING = ON (CHANGE_RETENTION = 6 DAYS, AUTO_CLEANUP = ON)
```

## <a name="refresh-the-data-entities-list"></a><span data-ttu-id="ca20f-170">データ エンティティの一覧を更新</span><span class="sxs-lookup"><span data-stu-id="ca20f-170">Refresh the data entities list</span></span>

<span data-ttu-id="ca20f-171">プラットフォーム更新プログラム 14 またはそれ以降にアップグレードした場合は、データ管理ワークスペース のデータ エンティティ リスト (**データ管理** > **フレームワーク パラメーター** > **エンティティ設定** > **エンティティ リストを更新**) を更新し、エンティティ リストが最新のプラットフォームで再構築され、必要なメタデータがデータ管理操作に使用できることを確認す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-171">If you have upgraded to Platform update 14 or later, then you will need refresh the data entity list in the Data management workspace (**Data management** > **Framework parameters** > **Entity settings** > **Refresh entity list**) to ensure that the entity list is rebuilt on the latest platform and that the required metadata is available for data management operations.</span></span> 

## <a name="troubleshoot-upgrade-script-errors"></a><span data-ttu-id="ca20f-172">アップグレード スクリプト エラーのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ca20f-172">Troubleshoot upgrade script errors</span></span>

<span data-ttu-id="ca20f-173">このセクションでは、さまざまな問題のトラブルシューティングに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-173">This section provides information that can help you troubleshoot various issues.</span></span>

### <a name="rerun-the-runbook-after-a-data-upgrade-script-failure"></a><span data-ttu-id="ca20f-174">データ アップグレード スクリプトの失敗後、runbook を再実行</span><span class="sxs-lookup"><span data-stu-id="ca20f-174">Rerun the runbook after a data upgrade script failure</span></span>

<span data-ttu-id="ca20f-175">デプロイ可能なデータ アップグレード パッケージでは、標準的なデプロイ可能なパッケージよりも細かい粒度で Runbook を再実行できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-175">A data upgrade deployable package enables the runbook to be rerun in a more granular manner than a typical deployable package.</span></span> <span data-ttu-id="ca20f-176">データ アップグレード スクリプトは、Runbook のステップ 5 で実行されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-176">The data upgrade scripts begin to be run at Step 5 of the runbook.</span></span> <span data-ttu-id="ca20f-177">手順 5 で障害が発生した場合は、コマンド ウィンドウで出力を表示し、どのサブステップに到達したかが分かります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-177">If you experience a failure during Step 5, view the output in the command window to learn which substep you reached.</span></span> <span data-ttu-id="ca20f-178">たとえば、サブステップ 5.3 に達した場合、そのサブステップから返す次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-178">For example, if you reached substep 5.3, use the following command to rerun from that substep.</span></span>

```Console
AXUpdateInstaller.exe execute -runbookid=upgrade -rerunstep=5.3
```

<span data-ttu-id="ca20f-179">デバッグしているときは、データアップグレード部分全体とデータベースの同期を再実行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-179">When you're debugging, you don't have to rerun the whole data upgrade piece and database synchronization.</span></span> <span data-ttu-id="ca20f-180">失敗したスクリプトだけを再実行し続けることができます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-180">You can keep rerunning just the script that fails.</span></span>

### <a name="view-more-details-about-a-script-error"></a><span data-ttu-id="ca20f-181">スクリプト エラーに関するより詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-181">View more details about a script error</span></span>

<span data-ttu-id="ca20f-182">runbook インストーラが起動するバッチ プロセスを使用して、X++ でアップグレード スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-182">Upgrade scripts run in X++ by using a batch process that the runbook installer starts.</span></span> <span data-ttu-id="ca20f-183">Visual Studio のアプリケーション エクスプローラーでは、表示できる一部のクラスの前に **ReleaseUpdate** が付いています。</span><span class="sxs-lookup"><span data-stu-id="ca20f-183">In Application Explorer in Visual Studio, some classes that you can view are prefixed with **ReleaseUpdate**.</span></span> <span data-ttu-id="ca20f-184">runbook プロセス中にアップグレード スクリプトが失敗した場合、Microsoft SQL Server Management Studio を開き、次のコードを実行して ReleaseUpdateScriptsErrorLog を照会することでエラーの原因をさらに確認できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-184">If an upgrade script fails during the runbook process, you can learn more about the reason for the error by opening Microsoft SQL Server Management Studio and running the following code to query ReleaseUpdateScriptsErrorLog.</span></span>

```sql
select \* from RELEASEUPDATESCRIPTSERRORLOG
```

<span data-ttu-id="ca20f-185">このコードを Visual Studio 内の新しい実行可能なクラスに追加して、その動作を直接観察、デバッグ、および再作業することができます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-185">You can add this code to a new runnable class in Visual Studio, and directly observe, debug, and rework its behavior.</span></span>

### <a name="skip-failed-scripts"></a><span data-ttu-id="ca20f-186">失敗したスクリプトをスキップ</span><span class="sxs-lookup"><span data-stu-id="ca20f-186">Skip failed scripts</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca20f-187">このプロセスは、開発シナリオでのみ使用することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="ca20f-187">This process is intended to be used only in a development scenario.</span></span>

<span data-ttu-id="ca20f-188">指定回数失敗したすべてのスクリプトをスキップして、次の実行可能なスクリプトに移動することができます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-188">You can skip all scripts that have failed a specific number of times, and move to the next viable scripts.</span></span> <span data-ttu-id="ca20f-189">この機能は、トラブルシューティング プロセスに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-189">This functionality helps with the troubleshooting process.</span></span> <span data-ttu-id="ca20f-190">意図的に、プロセスは手動であるため、誤ってスクリプトをスキップする可能性は低くなります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-190">By design, the process is very manual, so that you're less likely to unintentionally skip scripts.</span></span>

<span data-ttu-id="ca20f-191">ReleaseUpdateConfiguration のテーブルに、**ScriptRetryCount** という新しいフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-191">In the ReleaseUpdateConfiguration table, there is a new field that is named **ScriptRetryCount**.</span></span> <span data-ttu-id="ca20f-192">このフィールドの値は、runbook プロセスがスクリプトを無視する前にスクリプトを再実行する回数を制御します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-192">The value in this field controls how many times the runbook process will rerun scripts before it ignores them.</span></span> <span data-ttu-id="ca20f-193">Runbook が実行されると、システムは、特定のスクリプトが失敗するたびに **ReleaseUpdateScriptsErrorLog.ErrorCount** フィールドを更新します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-193">When the runbook is run, the system updates the **ReleaseUpdateScriptsErrorLog.ErrorCount** field every time that a specific script fails.</span></span> <span data-ttu-id="ca20f-194">各スクリプトの新しい行が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-194">A new row is created for each script.</span></span>

<span data-ttu-id="ca20f-195">DataUpgrade パッケージ フォルダーの ..\\AosServices\\Scripts\\ に、IgnoreBlockingScripts.ps1 というスクリプトがあります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-195">In the DataUpgrade package folder, under ..\\AosServices\\Scripts\\, there is a script that is named IgnoreBlockingScripts.ps1.</span></span> <span data-ttu-id="ca20f-196">管理者 Windows PowerShell ウィンドウからこのスクリプトを実行し、**ScriptRetryCount**=**ErrorCount** となっているすべてのスクリプトをスキップします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-196">Run this script from an Administrator Windows PowerShell window to skip all scripts where **ScriptRetryCount**=**ErrorCount**.</span></span> <span data-ttu-id="ca20f-197">次に、スクリプトが無視されるように、失敗した Runbook ステップを再実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-197">Then rerun the runbook step that failed, so that scripts will be ignored.</span></span> <span data-ttu-id="ca20f-198">**ReleaseUpdateScriptsErrorLog.Ignored** フィールドは、スキップされる各スクリプトにも設定されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-198">The **ReleaseUpdateScriptsErrorLog.Ignored** field will also be set for each script that is skipped.</span></span> <span data-ttu-id="ca20f-199">そのため、後でスキップされたスクリプトを簡単に識別できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-199">Therefore, you can easily identify skipped scripts later.</span></span>

### <a name="monitor-the-duration-of-scripts-that-are-run"></a><span data-ttu-id="ca20f-200">実行されるスクリプトの存続期間の監視</span><span class="sxs-lookup"><span data-stu-id="ca20f-200">Monitor the duration of scripts that are run</span></span>

<span data-ttu-id="ca20f-201">正常に実行されたすべてのスクリプトでは、**ReleaseUpdateScriptsLog.DurationMins** 列で取得した分数を記録します</span><span class="sxs-lookup"><span data-stu-id="ca20f-201">Every script that is successfully run records the number of minutes that it took in the **ReleaseUpdateScriptsLog.DurationMins** column.</span></span> <span data-ttu-id="ca20f-202">したがって、データ アップグレード プロセスのパフォーマンスを調整しようとしているときに、最も実行時間が長いスクリプトを簡単に識別できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-202">Therefore, you can easily identify the longest-running scripts when you're trying to tune the performance of the data upgrade process.</span></span> <span data-ttu-id="ca20f-203">期間は各スクリプトが実行にかかる時間であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-203">Note that the duration is the amount of time that each script takes to run.</span></span> <span data-ttu-id="ca20f-204">ただし、複数のスクリプトが並列実行されるため、**DurationMins** 列の値の合計は、アップグレード プロセスの全体的な期間を超えます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-204">However, because multiple scripts run in parallel, the sum of values in the **DurationMins** column will exceed the overall duration of the upgrade process.</span></span>

## <a name="known-issues"></a><span data-ttu-id="ca20f-205">既知の問題</span><span class="sxs-lookup"><span data-stu-id="ca20f-205">Known issues</span></span>
### <a name="a-duplicate-key-was-found-for-the-object-that-is-named-dboresourcesetup"></a><span data-ttu-id="ca20f-206">dbo.RESOURCESETUP という名前のオブジェクトのキーの重複が見つかりました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-206">A duplicate key was found for the object that is named dbo.RESOURCESETUP</span></span>

<span data-ttu-id="ca20f-207">データベースをアップグレードするとき、Runbook プロセスのデータベースの同期フェーズで、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-207">When you upgrade a database, you might receive the following error message during the database synchronization phase of the runbook process:</span></span>

> <span data-ttu-id="ca20f-208">データベースの実行に失敗しました: オブジェクト名「dbo.RESOURCESETUP」およびインデックス名「I\_6716AK」の重複キーが検出されたため、CREATE UNIQUE INDEX ステートメントが終了しました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-208">Database execution failed: The CREATE UNIQUE INDEX statement terminated because a duplicate key was found for the object name 'dbo.RESOURCESETUP' and the index name 'I\_6716AK'</span></span>

<span data-ttu-id="ca20f-209">この問題は、今後の修正プログラムで解決される既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-209">This issue is a known issue that will be resolved in a future hotfix.</span></span> <span data-ttu-id="ca20f-210">この問題を回避するには、Management Studio からデータベースに対して次の SQL スクリプトを実行し、テーブルから重複した列を削除します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-210">The workaround is to delete the duplicate rows from the table by running the following SQL script against the database from Management Studio.</span></span>

```sql
delete RS from ResourceSetup as RS
join ResResourceIdentifier as RRI on RRI.RecId = RS.Resource_
join WrkCtrTable as WCT on WCT.RecId = RRI.RefRecId
join DirPartyTable as DPT on DPT.DataArea = WCT.DataAreaId
where DPT.DataArea != '' and RS.LegalEntity != DPT.RecId
```

### <a name="a-record-cant-be-selected-in-dimension-hierarchy-nodes-camdatadimensionhierarchynode"></a><span data-ttu-id="ca20f-211">レコードは、分析コード階層ノード (CAMDataDimensionHierarchyNode) で選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-211">A record can't be selected in Dimension hierarchy nodes (CAMDataDimensionHierarchyNode)</span></span>

<span data-ttu-id="ca20f-212">データベースをアップグレードするとき、Runbook プロセスのデータベースの同期フェーズで、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-212">When you upgrade a database, you might receive the following error message during the database synchronization phase of the runbook process:</span></span>

> <span data-ttu-id="ca20f-213">分析コード階層ノード (CAMDataDimensionHierarchyNode) でレコードを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-213">Cannot select a record in Dimension hierarchy nodes (CAMDataDimensionHierarchyNode).</span></span> <span data-ttu-id="ca20f-214">分析コード階層: 0。</span><span class="sxs-lookup"><span data-stu-id="ca20f-214">Dimension hierarchy: 0.</span></span> <span data-ttu-id="ca20f-215">SQL データベースによってエラーが出されました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-215">The SQL database has issued an error.</span></span> <span data-ttu-id="ca20f-216">オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[ODBC Driver 13 for SQL Server\]\[SQL Server\] 無効な列名「RELATIONTYPE」です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-216">Object Server DynamicsAXBatchManagement:  \[Microsoft\]\[ODBC Driver 13 for SQL Server\]\[SQL Server\]Invalid column name 'RELATIONTYPE'.</span></span> 

<span data-ttu-id="ca20f-217">この問題は、将来のリリースで解決される既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-217">This issue is a known issue that will be resolved in a future release.</span></span> <span data-ttu-id="ca20f-218">この問題を回避するには、Management Studio からデータベースに対して次の SQL スクリプトを実行し、いくつかのテーブルに欠落したフィールドを作成します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-218">The workaround is to create a missing field in several tables by running the following SQL script against the database from Management Studio.</span></span>

```sql
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
DROP PROCEDURE IF EXISTS [DBO].PATCHRELATIONTYPE
GO 

CREATE PROCEDURE [DBO].PATCHRELATIONTYPE
        @TABLENAME SYSNAME
    AS
    BEGIN
        DECLARE @TABLEID        INT ;
        DECLARE @FIELDID        INT ;
        DECLARE @FIELDNAME      SYSNAME;
        DECLARE @SQLTATEMENT NVARCHAR(1024);
        DECLARE @TOTALRECORDS   INT;
        DECLARE @ParmDefinition         NVARCHAR(150);

        SET NOCOUNT ON;

        SELECT @FIELDNAME = 'RELATIONTYPE';
        SELECT @FIELDID = 61453; --Hardcoded in code DBFIELD_DISCRIMINATOR
        IF OBJECT_ID(@TABLENAME, 'U') IS NULL 
        BEGIN
            PRINT @TABLENAME + ' table does not exists. Please provide a base table';
            RETURN;
        END

        IF EXISTS(SELECT 1 FROM SYS.COLUMNS
            WHERE NAME = @FIELDNAME
            AND OBJECT_ID = OBJECT_ID(@TABLENAME))
        BEGIN
            PRINT @TABLENAME + ' table contains RelationType. No patching needed.';
            RETURN;
        END
        PRINT @TABLENAME + ' table does not contain RelationType.';
        SELECT @TABLEID = ID FROM TABLEIDTABLE WHERE NAME = @TABLENAME;
        IF @@ROWCOUNT <> 1
        BEGIN
            PRINT @TABLENAME + ' was not present in TABLEIDTABLE. Cannot proceed!!';
            RETURN;
        END 

        -- Ensure that instancerelationtype is added. We don't want to randomly add relationtype to any table.
        IF NOT EXISTS (SELECT \* FROM SQLDICTIONARY WHERE TABLEID = @TABLEID AND NAME = 'InstanceRelationType')     
        BEGIN
            PRINT @TABLENAME + ' table does not exist. Please provide a base table';
            RETURN;
        END

        -- Ensure SQLDictionary is populated
        IF NOT EXISTS (SELECT \* FROM SQLDICTIONARY WHERE TABLEID = @TABLEID AND FIELDID = @FIELDID)
        BEGIN
            INSERT INTO SQLDICTIONARY (TABLEID, FIELDID, ARRAY, NAME, SQLNAME, FIELDTYPE, STRSIZE, SHADOW, RIGHTJUSTIFY, NULLABLE, FLAGS, RECVERSION)
            VALUES (@TABLEID,@FIELDID,1, @FIELDNAME, @FIELDNAME, 49, 0, 0, 0, 0, 0, 1);
            PRINT 'Inserted into SqlDictionary';
        END

        -- Actual alter statement
        SELECT @SQLTATEMENT = 'ALTER TABLE ' + @TABLENAME +  ' ADD ' + @FIELDNAME + ' BIGINT NOT NULL DEFAULT 0';
        PRINT 'Issuing ' + @SQLTATEMENT;
        EXEC (@SQLTATEMENT);

        SELECT @SQLTATEMENT = 'UPDATE ' + @TABLENAME +  ' SET RELATIONTYPE = 0';
        PRINT 'Issuing ' + @SQLTATEMENT;
        EXEC (@SQLTATEMENT);
    END;
GO
exec PatchRelationType  'CAMDATADIMENSIONHIERARCHYNODE'
exec PatchRelationType  'CAMDataJournal'
exec PatchRelationType  'CAMDataCostAccountingLedgerSourceEntryProvider'
exec PatchRelationType  'CAMDataImportedDimensionMember'
```

### <a name="an-index-cant-be-created-on-inventdistinctproduct"></a><span data-ttu-id="ca20f-219">InventDistinctProduct にインデックスを作成することはできません</span><span class="sxs-lookup"><span data-stu-id="ca20f-219">An index can't be created on InventDistinctProduct</span></span>

<span data-ttu-id="ca20f-220">データベースをアップグレードするとき、Runbook プロセスのデータベースの同期フェーズで、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-220">When you upgrade a database, you might receive the following error message during the database synchronization phase of the runbook process:</span></span>

> <span data-ttu-id="ca20f-221">InventDistinctProduct 索引を作成できません。製品列に重複キーが存在します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-221">Cannot create index on InventDistinctProduct a duplicate key exists on column Product.</span></span>

<span data-ttu-id="ca20f-222">この問題は、将来のリリースで解決される既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-222">This issue is a known issue that will be resolved in a future release.</span></span> <span data-ttu-id="ca20f-223">この問題を回避するには、InventDistinctProduct テーブルのすべてのレコードを削除してから、現在のステップから Runbook を再開します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-223">The workaround is to delete all records in the InventDistinctProduct table and then resume the runbook from the current step.</span></span> <span data-ttu-id="ca20f-224">InventDistinctProduct テーブル内のレコードは破棄できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-224">The records in the InventDistinctProduct table are disposable.</span></span> <span data-ttu-id="ca20f-225">それらは Finance and Operations が初めて開始されたとき、項目が登録されたとき、MRP が実行されたときに再生成されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-225">They will be regenerated the first time that Finance and Operations is started, when an item is created, or when MRP is run.</span></span> <span data-ttu-id="ca20f-226">InventDistinctProduct のすべてのレコードを削除するには、Management Studio から現在のデータベースに対して次のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-226">To delete all records in InventDistinctProduct, run the following query against the current database from Management Studio.</span></span>

```sql
truncate table InventDistinctProduct
```

<span data-ttu-id="ca20f-227">現在のステップから runbook を再開するには、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-227">To resume the runbook from the current step, run the following command.</span></span>

```Console
axupdateinstaller execute -runbookid=<your runbook name> -rerunstep=<the last step number>
```

<span data-ttu-id="ca20f-228">たとえば、このコマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-228">For example, you can use this command.</span></span>

```Console
axupdateinstaller execute -runbookid=dataupgrade -rerunstep=5.4
```

### <a name="an-exchange-rate-cant-be-found-when-demo-data-is-upgraded"></a><span data-ttu-id="ca20f-229">デモ データがアップグレードされている場合為替レートは見つかりません</span><span class="sxs-lookup"><span data-stu-id="ca20f-229">An exchange rate can't be found when demo data is upgraded</span></span>

<span data-ttu-id="ca20f-230">デモ データベースをアップグレードするとき、データ アップグレード パッケージを配置するときに、次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-230">When you upgrade a demo database, you might receive the following error message when you deploy the data upgrade package:</span></span>

> <span data-ttu-id="ca20f-231">交換日 2014 年 12 月 1 日時点の通貨 INR と BRL 間の為替レート タイプ既定に対する為替レートが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-231">An exchange rate cannot be found for exchange rate type Default between currencies INR and BRL on exchange date 12/1/2014.</span></span>

<span data-ttu-id="ca20f-232">デモ データをアップグレードするため、経費明細行がある TrvUnreconciledExpenseTransaction テーブルを確認します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-232">Because you're upgrading demo data, look in the TrvUnreconciledExpenseTransaction table, which is where the expense line is.</span></span> <span data-ttu-id="ca20f-233">通貨を **USD** に変更します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-233">Change the currency to **USD**.</span></span> <span data-ttu-id="ca20f-234">(データはデモ データなので、この経費行を保存するのに注意する必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="ca20f-234">(Because the data is demo data, you don't have to be careful to preserve this expense line.)</span></span>

```sql
update TrvUnreconciledExpenseTransaction
set transactioncurrencycode = 'USD'
where transactioncurrencycode = 'INR'
```

<span data-ttu-id="ca20f-235">または、データが元の環境 (旧バージョンなど) から元の環境に移動し、失われた為替レートを**総勘定元帳** &gt; **通貨** &gt; **通貨の為替レート**に追加します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-235">Alternatively, go to the original environment that the data came from (such as the old version), and add the missing exchange rate at **General Ledger** &gt; **Currencies** &gt; **Currency exchange rates**.</span></span> <span data-ttu-id="ca20f-236">2014 をカバーするインド ルピー (INR) およびブラジル レアル (BRL) のレコードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-236">You must add records for Indian rupee (INR) and Brazilian real (BRL) that cover 2014.</span></span> <span data-ttu-id="ca20f-237">次に、そのデータベースを新しい環境に持ち込み、そのデータベースに対してアップグレードを開始します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-237">Then bring that database into your new environment, and start the upgrade against that database.</span></span>

### <a name="the-interpreter-evaluation-stack-has-grown-during-a-call-to-the-kernel"></a><span data-ttu-id="ca20f-238">インタプリター評価スタックは、カーネルの呼び出し中に増加しました</span><span class="sxs-lookup"><span data-stu-id="ca20f-238">The interpreter evaluation stack has grown during a call to the kernel</span></span>

<span data-ttu-id="ca20f-239">UserInfom などのカーネル テーブルでデータベース ログを有効にした場合、次のエラー メッセージが表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-239">If you've enabled database logging on a kernel table such as UserInfom, you might receive the following error message:</span></span>

> <span data-ttu-id="ca20f-240">実行ステップ: 5.1</span><span class="sxs-lookup"><span data-stu-id="ca20f-240">Executing step: 5.1</span></span>  
> <span data-ttu-id="ca20f-241">データ アップグレードの必要条件</span><span class="sxs-lookup"><span data-stu-id="ca20f-241">prereq for data upgrade</span></span>  
> <span data-ttu-id="ca20f-242">データ アップグレードの必要条件</span><span class="sxs-lookup"><span data-stu-id="ca20f-242">prereq for data upgrade</span></span>  
> <span data-ttu-id="ca20f-243">未処理の例外の詳細情報: インタープリター評価スタックは、カーネル メソッド xRecord::Delete ()、height before call: 0、height after call: 3 の呼び出し中に増加しました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-243">Unhandled exception More Information: The interpreter evaluation stack has grown during a call to the kernel method xRecord::Delete (), height before call: 0, height after call: 3.</span></span> <span data-ttu-id="ca20f-244">未処理の例外の詳細情報: KernelInstance: カーネルが削除されたメモリにアクセスしています</span><span class="sxs-lookup"><span data-stu-id="ca20f-244">Unhandled exception More Information: KernelInstance: Kernel is accessing deleted memory</span></span>  
> <span data-ttu-id="ca20f-245">失敗したステップ</span><span class="sxs-lookup"><span data-stu-id="ca20f-245">The step failed</span></span>

<span data-ttu-id="ca20f-246">この問題を解決するには、**システム管理**&gt;**設定**&gt;**データベース ログ設定** でデータベース ログの設定を確認してください。</span><span class="sxs-lookup"><span data-stu-id="ca20f-246">To resolve this issue, review the database log setup at **System administration** &gt; **Setup** &gt; **Database log setup**.</span></span> <span data-ttu-id="ca20f-247">必要に応じてカーネル テーブルのレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-247">Remove records for kernel tables as you require.</span></span>

### <a name="the-batch-process-fails-to-start"></a><span data-ttu-id="ca20f-248">バッチ処理を開始できません</span><span class="sxs-lookup"><span data-stu-id="ca20f-248">The batch process fails to start</span></span>

<span data-ttu-id="ca20f-249">コンフィギュレーション キーが変更された後に環境が[メンテナンス モード](../sysadmin/maintenance-mode.md)のままになっていると、バッチ処理が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-249">The batch process can fail if the environment was left in [maintenance mode](../sysadmin/maintenance-mode.md) after the configuration keys were changed.</span></span> <span data-ttu-id="ca20f-250">この問題を解決するには、メンテナンス モードをオフにしてから、runbook プロセスを再開します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-250">To resolve this issue, turn maintenance mode off, and then resume the runbook process.</span></span>

### <a name="the-system-fails-to-locate-or-generate-a-user-guid"></a><span data-ttu-id="ca20f-251">システムは検索したりユーザー GUID を生成したりできません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-251">The system fails to locate or generate a user GUID</span></span>

<span data-ttu-id="ca20f-252">次のエラー メッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-252">You might receive the following error message:</span></span>

> <span data-ttu-id="ca20f-253">…ハンドルされない例外の追加情報: システムはユーザー GUIDの検索または生成に失敗しました…</span><span class="sxs-lookup"><span data-stu-id="ca20f-253">…Unhandled exception More Information: System failed to locate or generate a user GUID…</span></span>

<span data-ttu-id="ca20f-254">この問題を解決するのには、失敗した runbook ステップを再実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-254">To resolve this issue, rerun the runbook step that failed.</span></span> <span data-ttu-id="ca20f-255">次に、継続することができます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-255">You will then be able to continue.</span></span>

### <a name="pre-sync-or-post-sync-errors-on-releaseupdatedb71_ledgerperiodclose"></a><span data-ttu-id="ca20f-256">ReleaseUpdateDB71\_LedgerPeriodClose で事前同期または事後同期エラー</span><span class="sxs-lookup"><span data-stu-id="ca20f-256">Pre-sync or post-sync errors on ReleaseUpdateDB71\_LedgerPeriodClose</span></span>

<span data-ttu-id="ca20f-257">**ReleaseUpdateDB71\_LedgerPeriodClose** クラスの **preSyncLedgerPeriodCloseTemplateTask**、**updateMenuItemTypeForCurrencyReval**、または**updateLedgerPeriodCloseTemplateTask** メソッドでは、次のエラー メッセージの 1 つを受け取る可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-257">You might receive one of the following error messages on the **preSyncLedgerPeriodCloseTemplateTask**, **updateMenuItemTypeForCurrencyReval**, or **updateLedgerPeriodCloseTemplateTask** method in the **ReleaseUpdateDB71\_LedgerPeriodClose** class:</span></span>

> <span data-ttu-id="ca20f-258">必要なデータベース操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-258">Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-259">SQL データベースによってエラーが出されました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-259">The SQL database has issued an error.</span></span> <span data-ttu-id="ca20f-260">オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\] 無効な列名「TEMPLATE」です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-260">Object Server DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]Invalid column name 'TEMPLATE'.</span></span> <span data-ttu-id="ca20f-261">INSERT INTO LedgerPeriodCloseTemplateTaskTmp (TEMPLATE、AREA, NAME、MENUITEM、MENUITEMTYPE、 TARGETDAYSFROMPROJECTCOMPLETE、DUETIME、LEGALENTITYSELECTION、RECVERSION、PARTITION、RECID、CLOSINGROLE、LINENUM) SELECT T1.TEMPLATE、T1.AREA、T1.NAME、T1.MENUITEM、T1.MENUITEMTYPE、T1.TARGETDAYSFROMPROJECTCOMPLETE、T1.DUETIME、 T1.LEGALENTITYSELECTION、T1.RECVERSION、T1.PARTITIONT1.RECID、T1.CLOSINGROLE、0 FROM LedgerPeriodCloseTemplateTask T1 session 1013 (Admin) Microsoft.Dynamics.Ax.Xpp.ErrorException: Cannot execute the required database operation。</span><span class="sxs-lookup"><span data-stu-id="ca20f-261">INSERT INTO LedgerPeriodCloseTemplateTaskTmp ( TEMPLATE, AREA, NAME, MENUITEM, MENUITEMTYPE, TARGETDAYSFROMPROJECTCOMPLETE, DUETIME, LEGALENTITYSELECTION, RECVERSION, PARTITION, RECID, CLOSINGROLE, LINENUM) SELECT T1.TEMPLATE, T1.AREA, T1.NAME, T1.MENUITEM, T1.MENUITEMTYPE, T1.TARGETDAYSFROMPROJECTCOMPLETE, T1.DUETIME, T1.LEGALENTITYSELECTION, T1.RECVERSION, T1.PARTITION, T1.RECID, T1.CLOSINGROLE, 0 FROM LedgerPeriodCloseTemplateTask T1 session 1013 (Admin) Microsoft.Dynamics.Ax.Xpp.ErrorException: Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-262">SQL データベースによってエラーが出されました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-262">The SQL database has issued an error.</span></span>
> 
> <span data-ttu-id="ca20f-263">必要なデータベース操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-263">Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-264">SQL データベースによってエラーが出されました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-264">The SQL database has issued an error.</span></span> <span data-ttu-id="ca20f-265">オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\] 無効な列名「MENUITEMTYPE」です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-265">Object Server DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]Invalid column name 'MENUITEMTYPE'.</span></span> <span data-ttu-id="ca20f-266">UPDATE LedgerPeriodCloseTemplateTaskTmp SET MENUITEMTYPE = 0 WHERE MENUITEMTYPE = 2 AND MENUITEM = 'LedgerExchAdj' AND PARTITION = 5637144576 session 1013 (Admin) Microsoft.Dynamics.Ax.Xpp.ErrorException: 必要なデータベース操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-266">UPDATE LedgerPeriodCloseTemplateTaskTmp SET MENUITEMTYPE = 0 WHERE MENUITEMTYPE = 2 AND MENUITEM = 'LedgerExchAdj' AND PARTITION = 5637144576 session 1013 (Admin) Microsoft.Dynamics.Ax.Xpp.ErrorException: Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-267">SQL データベースによってエラーが出されました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-267">The SQL database has issued an error.</span></span>
> 
> <span data-ttu-id="ca20f-268">必要なデータベース操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-268">Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-269">SQL データベースによってエラーが出されました。</span><span class="sxs-lookup"><span data-stu-id="ca20f-269">The SQL database has issued an error.</span></span> <span data-ttu-id="ca20f-270">オブジェクト サーバー DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\] 無効な列名「TEMPLATE」です。</span><span class="sxs-lookup"><span data-stu-id="ca20f-270">Object Server DynamicsAXBatchManagement: \[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]Invalid column name 'TEMPLATE'.</span></span> <span data-ttu-id="ca20f-271">INSERT INTO LedgerPeriodCloseTemplateTask (TEMPLATE、AREA、NAME、MENUITEM、MENUITEMTYPE、TARGETDAYSFROMPROJECTCOMPLETE、DUETIME、LEGALENTITYSELECTION、RECVERSION、PARTITION、RECID、CLOSINGROLE、LINENUM) SELECT T1.TEMPLATE、T1.AREA、T1.NAME、 T1.MENUITEM、T1.MENUITEMTYPE、T1.TARGETDAYSFROMPROJECTCOMPLETE、T1.DUETIME、T1.LEGALENTITYSELECTION、T1.RECVERSION、 T1.PARTITION、T1.RECID、T1.CLOSINGROLE、T1.LINENUM FROM LedgerPeriodCloseTemplateTaskTmp T1 session 1013 (Admin)</span><span class="sxs-lookup"><span data-stu-id="ca20f-271">INSERT INTO LedgerPeriodCloseTemplateTask ( TEMPLATE, AREA, NAME, MENUITEM, MENUITEMTYPE, TARGETDAYSFROMPROJECTCOMPLETE, DUETIME, LEGALENTITYSELECTION, RECVERSION, PARTITION, RECID, CLOSINGROLE, LINENUM) SELECT T1.TEMPLATE, T1.AREA, T1.NAME, T1.MENUITEM, T1.MENUITEMTYPE, T1.TARGETDAYSFROMPROJECTCOMPLETE, T1.DUETIME, T1.LEGALENTITYSELECTION, T1.RECVERSION, T1.PARTITION, T1.RECID, T1.CLOSINGROLE, T1.LINENUM FROM LedgerPeriodCloseTemplateTaskTmp T1 session 1013 (Admin)</span></span>

<span data-ttu-id="ca20f-272">この問題を解決するには、Management Studio を使用して、データベースから LedgerPeriodCloseTemplateTaskTmp テーブルを手動でドロップします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-272">To resolve this issue, use Management Studio to manually drop the LedgerPeriodCloseTemplateTaskTmp table from the database.</span></span> <span data-ttu-id="ca20f-273">Runbook ステップを返します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-273">Then rerun the runbook step.</span></span> <span data-ttu-id="ca20f-274">この問題は、将来の修正プログラムで修正されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-274">This issue will be fixed in a future hotfix.</span></span>

### <a name="kb-number-3170386"></a><span data-ttu-id="ca20f-275">KB 番号 3170386</span><span class="sxs-lookup"><span data-stu-id="ca20f-275">KB number 3170386</span></span>

<span data-ttu-id="ca20f-276">KB 番号 3170386 がインストールされていない場合、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ca20f-276">If KB number 3170386 isn't installed, you will receive the following error message:</span></span>

> <span data-ttu-id="ca20f-277">サービス モデルの GlobalUpdate スクリプト: マシンでの AOSService ….</span><span class="sxs-lookup"><span data-stu-id="ca20f-277">GlobalUpdate script for service model: AOSService on machine ….</span></span> <span data-ttu-id="ca20f-278">その他 ….</span><span class="sxs-lookup"><span data-stu-id="ca20f-278">Etc ….</span></span> <span data-ttu-id="ca20f-279">UpgradeServiceHelper::WaitForDataUpgradeToComplete(Object\[\]…</span><span class="sxs-lookup"><span data-stu-id="ca20f-279">UpgradeServiceHelper::WaitForDataUpgradeToComplete(Object\[\]…</span></span> <span data-ttu-id="ca20f-280">失敗したステップ</span><span class="sxs-lookup"><span data-stu-id="ca20f-280">The step failed</span></span>

<span data-ttu-id="ca20f-281">このエラーは、データ アップグレードの事前同期または事後同期のサブステップに障害が起こったために発生します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-281">This error is caused by a failure in the pre-sync or the post-sync substep of the data upgrade.</span></span> <span data-ttu-id="ca20f-282">どのサブステップが失敗したかおよび失敗の詳細を特定するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ca20f-282">Follow these steps to determine which substep failed and the details of the failure.</span></span>

> [!NOTE]
> <span data-ttu-id="ca20f-283">事前同期または事後同期サブステップが手動で完了するまで障害が発生した Runbook ステップを再度実行することはできず、AutoDataUpgrade.config ファイルが更新されて、既に実行されているサブステップをスキップします。</span><span class="sxs-lookup"><span data-stu-id="ca20f-283">You can't rerun the failed runbook step until the pre-sync or post-sync substep has been manually completed, and the AutoDataUpgrade.config file has been updated to skip the substeps that have already been run.</span></span>

1. <span data-ttu-id="ca20f-284">ファイル エクスプローラーの **DataUpgradeAosServiceScripts** フォルダーで、ファイルが最後に変更された日付を降順に並べ替えてから、どの手順が失敗したかを特定するためにリストの上部にあるファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-284">In File Explorer, in the **DataUpgradeAosServiceScripts** folder, sort by descending order of the date when files were last modified, and then look at the file at the top of the list to determine which substep failed.</span></span>

    - <span data-ttu-id="ca20f-285">一番上のファイルの名前が **dbUpgrade*PreSync*Monitor.error.log** と付けられている場合は、同期前サブステップが失敗します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-285">If the top file is named **dbUpgrade*PreSync*Monitor.error.log**, the pre-sync substep failed.</span></span>
    - <span data-ttu-id="ca20f-286">一番上のファイルの名前が **dbUpgrade*PostSync*Monitor.error.log** と付けられている場合は、同期後サブステップが失敗します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-286">If the top file is named **dbUpgrade*PostSync*Monitor.error.log**, the post-sync substep failed.</span></span>

2. <span data-ttu-id="ca20f-287">Management Studio で、次の **SELECT** ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-287">In Management Studio, run the following **SELECT** statement.</span></span>

    ```sql
    SELECT * FROM RELEASEUPDATELOG
    ```

    <span data-ttu-id="ca20f-288">結果セットの最後から 2 番目のレコードには、すべての失敗のエラーとコール スタックがあります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-288">The second-to-last record in the result set will have the errors and call stacks for all the failures.</span></span>

### <a name="dmf-errors"></a><span data-ttu-id="ca20f-289">DMF エラー</span><span class="sxs-lookup"><span data-stu-id="ca20f-289">DMF errors</span></span>

<span data-ttu-id="ca20f-290">次のデータ移行フレームワーク (DMF) エラーのいずれかの方法が表示される場合は、修正プログラム サポート技術情報番号 3170386 をダウンロードし、アップグレード プロセスを再開します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-290">If you receive either of the following Data Migration Framework (DMF) errors, download hotfix KB number 3170386, and then restart the upgrade process.</span></span>

#### <a name="dmf-pre-sync-error"></a><span data-ttu-id="ca20f-291">DMF 事後同期エラー</span><span class="sxs-lookup"><span data-stu-id="ca20f-291">DMF pre-sync error</span></span>

> <span data-ttu-id="ca20f-292">バッチ エラー: initial.DAT.ReleaseUpdateDB70\_DMF.updateIntegrationActivityExecutionMessageIdPreSync (バッチ: AOS-F01B9F0CCC8、 9、情報、エラー、):\[\[1\]\[3、必要なデータベース操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-292">Batch error: initial.DAT.ReleaseUpdateDB70\_DMF.updateIntegrationActivityExecutionMessageIdPreSync (Batch:AOS-F01B9F0CCC8, 9, Info, Error, ):\[\[1\]\[3,Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-293">SQL データベースがエラーを発行しました。\]\[3,Object Server DynamicsAXBatchManagement: \]\[3,\[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]'GO' 付近に正しくない構文があります。\]\[3,</span><span class="sxs-lookup"><span data-stu-id="ca20f-293">The SQL database has issued an error.\]\[3,Object Server DynamicsAXBatchManagement: \]\[3,\[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]Incorrect syntax near 'GO'.\]\[3,</span></span>

#### <a name="dmf-post-sync-error"></a><span data-ttu-id="ca20f-294">DMF 事後同期エラー</span><span class="sxs-lookup"><span data-stu-id="ca20f-294">DMF post-sync error</span></span>

> <span data-ttu-id="ca20f-295">バッチ エラー: initial.DAT.ReleaseUpdateDB70\_DMF.updateIntegrationActivityExecutionMessageIdPostSync(バッチ: AOS-F01B9F0CCC8、 9、情報、エラー、):\[\[1\]\[3、必要なデータベース操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-295">Batch error: initial.DAT.ReleaseUpdateDB70\_DMF.updateIntegrationActivityExecutionMessageIdPostSync (Batch:AOS-F01B9F0CCC8, 9, Info, Error, ):\[\[1\]\[3,Cannot execute the required database operation.</span></span> <span data-ttu-id="ca20f-296">SQL データベースがエラーを発行しました。\]\[3,Object Server DynamicsAXBatchManagement: \]\[3,\[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]'GO' 付近に正しくない構文があります。\]\[3,</span><span class="sxs-lookup"><span data-stu-id="ca20f-296">The SQL database has issued an error.\]\[3,Object Server DynamicsAXBatchManagement: \]\[3,\[Microsoft\]\[SQL Server Native Client 11.0\]\[SQL Server\]Incorrect syntax near 'GO'.\]\[3,</span></span>

## <a name="encrypted-fields-in-demo-data"></a><span data-ttu-id="ca20f-297">デモ データの暗号化されたフィールド</span><span class="sxs-lookup"><span data-stu-id="ca20f-297">Encrypted fields in demo data</span></span>

<span data-ttu-id="ca20f-298">アップグレード後、データベースの暗号化されたフィールドの値は読み取れません。</span><span class="sxs-lookup"><span data-stu-id="ca20f-298">After upgrade, values in encrypted fields in the database will be unreadable.</span></span> <span data-ttu-id="ca20f-299">ただし、アップグレード後にこれらのフィールドに入力される新しい値は読み取り可能になります。</span><span class="sxs-lookup"><span data-stu-id="ca20f-299">However, new values that are entered in these fields after upgrade will be readable.</span></span> <span data-ttu-id="ca20f-300">この動作は、データ暗号化に使用される証明書に関連する技術的な制限のために発生します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-300">This behavior occurs because of a technical limitation that is related to the certificate that is used for data encryption.</span></span> <span data-ttu-id="ca20f-301">次のテーブルに、影響を受けるフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="ca20f-301">The following table shows the fields that are affected.</span></span>

| <span data-ttu-id="ca20f-302">Table.Field</span><span class="sxs-lookup"><span data-stu-id="ca20f-302">Table.Field</span></span>                                                      | <span data-ttu-id="ca20f-303">デモ データにデータが存在します</span><span class="sxs-lookup"><span data-stu-id="ca20f-303">Data exists in demo data</span></span> |
|------------------------------------------------------------------|--------------------------|
| <span data-ttu-id="ca20f-304">CreditCardAccountSetup.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="ca20f-304">CreditCardAccountSetup.SecureMerchantProperties</span></span>                  | <span data-ttu-id="ca20f-305">有</span><span class="sxs-lookup"><span data-stu-id="ca20f-305">Yes</span></span>                      |
| <span data-ttu-id="ca20f-306">ExchangeRateProviderConfigurationDetails.Value</span><span class="sxs-lookup"><span data-stu-id="ca20f-306">ExchangeRateProviderConfigurationDetails.Value</span></span>                   | <span data-ttu-id="ca20f-307">有</span><span class="sxs-lookup"><span data-stu-id="ca20f-307">Yes</span></span>                      |
| <span data-ttu-id="ca20f-308">RetailChannelPaymentConnectorLine.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="ca20f-308">RetailChannelPaymentConnectorLine.SecureMerchantProperties</span></span>       | <span data-ttu-id="ca20f-309">有</span><span class="sxs-lookup"><span data-stu-id="ca20f-309">Yes</span></span>                      |
| <span data-ttu-id="ca20f-310">RetailConnDatabaseProfile.ConnectionString</span><span class="sxs-lookup"><span data-stu-id="ca20f-310">RetailConnDatabaseProfile.ConnectionString</span></span>                       | <span data-ttu-id="ca20f-311">有</span><span class="sxs-lookup"><span data-stu-id="ca20f-311">Yes</span></span>                      |
| <span data-ttu-id="ca20f-312">RetailHardwareProfile.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="ca20f-312">RetailHardwareProfile.SecureMerchantProperties</span></span>                   | <span data-ttu-id="ca20f-313">有</span><span class="sxs-lookup"><span data-stu-id="ca20f-313">Yes</span></span>                      |
| <span data-ttu-id="ca20f-314">RetailHardwareProfileMerchantInfoEntity.SecureMerchantProperties</span><span class="sxs-lookup"><span data-stu-id="ca20f-314">RetailHardwareProfileMerchantInfoEntity.SecureMerchantProperties</span></span> | <span data-ttu-id="ca20f-315">有</span><span class="sxs-lookup"><span data-stu-id="ca20f-315">Yes</span></span>                      |
| <span data-ttu-id="ca20f-316">FiscalEstablishment\_BR.ConsumerEFDocCsc</span><span class="sxs-lookup"><span data-stu-id="ca20f-316">FiscalEstablishment\_BR.ConsumerEFDocCsc</span></span>                         | <span data-ttu-id="ca20f-317">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-317">No</span></span>                       |
| <span data-ttu-id="ca20f-318">FiscalEstablishmentEntity.CSC</span><span class="sxs-lookup"><span data-stu-id="ca20f-318">FiscalEstablishmentEntity.CSC</span></span>                                    | <span data-ttu-id="ca20f-319">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-319">No</span></span>                       |
| <span data-ttu-id="ca20f-320">FiscalEstablishmentStaging.CSC</span><span class="sxs-lookup"><span data-stu-id="ca20f-320">FiscalEstablishmentStaging.CSC</span></span>                                   | <span data-ttu-id="ca20f-321">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-321">No</span></span>                       |
| <span data-ttu-id="ca20f-322">HcmPersonIdentificationNumber.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="ca20f-322">HcmPersonIdentificationNumber.PersonIdentificationNumber</span></span>         | <span data-ttu-id="ca20f-323">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-323">No</span></span>                       |
| <span data-ttu-id="ca20f-324">HcmWorkerActionHire.PersonIdentificationNumber</span><span class="sxs-lookup"><span data-stu-id="ca20f-324">HcmWorkerActionHire.PersonIdentificationNumber</span></span>                   | <span data-ttu-id="ca20f-325">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-325">No</span></span>                       |
| <span data-ttu-id="ca20f-326">SysEmailSMPTPassword.Password</span><span class="sxs-lookup"><span data-stu-id="ca20f-326">SysEmailSMPTPassword.Password</span></span>                                    | <span data-ttu-id="ca20f-327">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-327">No</span></span>                       |
| <span data-ttu-id="ca20f-328">SysOAuthUserTokens.EncryptedAccessToken</span><span class="sxs-lookup"><span data-stu-id="ca20f-328">SysOAuthUserTokens.EncryptedAccessToken</span></span>                          | <span data-ttu-id="ca20f-329">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-329">No</span></span>                       |
| <span data-ttu-id="ca20f-330">SysOAuthUserTokens.EncryptedRefreshToken</span><span class="sxs-lookup"><span data-stu-id="ca20f-330">SysOAuthUserTokens.EncryptedRefreshToken</span></span>                         | <span data-ttu-id="ca20f-331">無</span><span class="sxs-lookup"><span data-stu-id="ca20f-331">No</span></span>                       |

## <a name="additional-resources"></a><span data-ttu-id="ca20f-332">追加リソース</span><span class="sxs-lookup"><span data-stu-id="ca20f-332">Additional resources</span></span>

[<span data-ttu-id="ca20f-333">Finance and Operationsで最新の更新プログラムに移行するためのプロセス</span><span class="sxs-lookup"><span data-stu-id="ca20f-333">Process for moving to the latest update of Finance and Operations</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/upgrade-latest-update)

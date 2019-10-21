---
title: 生産データベースのコピーのデバッグ
description: このトピックでは、Finance and Operations のデバッグおよび診断のシナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: a60dad258712440607f2001db988acc89e523ebe
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183417"
---
# <a name="debug-a-copy-of-the-production-database"></a><span data-ttu-id="15ec5-103">生産データベースのコピーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="15ec5-103">Debug a copy of the production database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15ec5-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="15ec5-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="15ec5-105">このチュートリアルでは、生産データの最新のコピーの特定のデータとトランザクションをデバッグする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-105">This tutorial shows how to debug specific data and transactions from a recent copy of production data.</span></span>

<span data-ttu-id="15ec5-106">このチュートリアルでは、次の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-106">In this tutorial, you will learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="15ec5-107">ユーザー受け入れテスト (UAT) 環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-107">Refresh the user acceptance testing (UAT) environment.</span></span>
> * <span data-ttu-id="15ec5-108">承認済リスト (「ホワイトリスト」) には、開発者の環境の IP アドレスを追加します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-108">Add the IP address of your developer environment to an approved list ("whitelist").</span></span>
> * <span data-ttu-id="15ec5-109">UAT データベースに接続できるように、開発者環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-109">Update your developer environment so that it connects to the UAT database.</span></span>
> * <span data-ttu-id="15ec5-110">ブレークポイントを設定し、データのデバッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-110">Set a breakpoint, and start to debug the data.</span></span>

<span data-ttu-id="15ec5-111">このシナリオの例として、既に稼働している顧客が、開発環境から生産トランザクションの最新のコピーをデバッグしようとしているということがあります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-111">As an example of this scenario, a customer who has already gone live wants to debug a recent copy of production transactions from his or her development environment.</span></span> <span data-ttu-id="15ec5-112">これにより、顧客は止まっている特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。</span><span class="sxs-lookup"><span data-stu-id="15ec5-112">In this way, the customer will be able to debug specific transactions that are stuck, or develop new features and reports by using realistic datasets.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15ec5-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="15ec5-113">Prerequisites</span></span>

<span data-ttu-id="15ec5-114">更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-114">To do a refresh operation, you must have your production environment deployed, or you must have a minimum of two standard UAT environments.</span></span> <span data-ttu-id="15ec5-115">このチュートリアルを完了するには、開発者環境が配置されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-115">To complete this tutorial, you must have a developer environment deployed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15ec5-116">デバッグの場合、UAT 環境で使用できるのと同じコードとビジネス ロジックを実行する DevTest 環境を使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="15ec5-116">For debugging, we highly recommend that you use a DevTest environment that runs the same code and business logic that are available in your UAT environment.</span></span> <span data-ttu-id="15ec5-117">バージョン コントロールで複数のブランチを使用する場合は、最新の UAT または生産トランザクションをデバッグするために使用される DevTest 環境を、UAT のパッケージを構築するために使用する同じブランチに接続した後、生産に使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="15ec5-117">If you use multiple branches in version control, we recommend that the DevTest environment that is used to debug recent UAT or production transactions be connected to the same branch that you use to build packages for UAT and, later, for production.</span></span> <span data-ttu-id="15ec5-118">これにより、互換性のあるスキーマになるため、DevTest 環境と UAT データベースの間でデータベースの同期を実行する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="15ec5-118">In this way, you don't have to run a database synchronization between your DevTest environment and UAT database, because the schema will be compatible.</span></span> <span data-ttu-id="15ec5-119">これまで、このような環境は、修正プログラム/サポート環境と呼ばれてきました。通常のコード プロモーション パス外となっているためです。</span><span class="sxs-lookup"><span data-stu-id="15ec5-119">Historically, this environment is known as a Hotfix/Support environment, because it's outside your usual code promotion path.</span></span>

## <a name="refresh-the-uat-environment"></a><span data-ttu-id="15ec5-120">UAT 環境を更新</span><span class="sxs-lookup"><span data-stu-id="15ec5-120">Refresh the UAT environment</span></span> 

<span data-ttu-id="15ec5-121">この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。</span><span class="sxs-lookup"><span data-stu-id="15ec5-121">This refresh operation overwrites the UAT environment with the latest copy of the production database.</span></span> <span data-ttu-id="15ec5-122">この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="15ec5-122">To complete this step, follow the instructions in [Refresh for training purposes](dbmovement-scenario-general-refresh.md).</span></span>

## <a name="add-your-ip-address-to-a-whitelist"></a><span data-ttu-id="15ec5-123">IP アドレスをホワイトリストに追加します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-123">Add your IP address to a whitelist</span></span>

<span data-ttu-id="15ec5-124">既定では、すべてのサンドボックス標準受け入れテスト環境で Microsoft Azure データベース プラットフォームとして SQL データベースを使用します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-124">By default, all Sandbox Standard Acceptance Test environments use Microsoft Azure SQL Database as their database platform.</span></span> <span data-ttu-id="15ec5-125">このような環境のデータベースは、最初に配置された Application Object Server (AOS) へのアクセスを制限するファイアウォールで保護されています。</span><span class="sxs-lookup"><span data-stu-id="15ec5-125">The databases for these environments are protected by firewalls that restrict access to the Application Object Server (AOS) with which it was originally deployed.</span></span>

<span data-ttu-id="15ec5-126">ただし、UAT データベースに直接開発環境 (クラウドにホストされているか、または Microsoft が管理) を接続できるように、例外を作ることができます。</span><span class="sxs-lookup"><span data-stu-id="15ec5-126">However, an exception can be made so that you can connect your developer environment (cloud-hosted or Microsoft-managed) directly to the UAT database.</span></span> <span data-ttu-id="15ec5-127">開発者環境を UAT データベースに直接接続するには、開発者仮想マシン (VM) で IP アドレスを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-127">To connect your developer environment directly to the UAT database, you must obtain your IP address on the developer virtual machine (VM).</span></span>

<span data-ttu-id="15ec5-128">サンドボックス AOS VM で、Microsoft SQL Server Management Studio (SSMS) を開き、Microsoft Dynamics Lifecycle Services (LCS) で環境の詳細のページから使用できる情報を使用してデータベースに接続します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-128">On the sandbox AOS VM, open Microsoft SQL Server Management Studio (SSMS), and connect to the database by using the information that is available from the environment details page in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="15ec5-129">ユーザー名レコードで **axdbadmin** を検索し、**{sqlServer\\sqlDatabase}** 形式のサーバーとデータベースに注目します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-129">Find the username record for **axdbadmin**, and note the server and database in the format **{sqlServer\\sqlDatabase}**.</span></span>

<span data-ttu-id="15ec5-130">SSMS で、SQL Server、ユーザー名、およびパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-130">In SSMS, enter the SQL Server, username, and password.</span></span> <span data-ttu-id="15ec5-131">**接続のプロパティ** タブで、LCS の **axdbadmin** レコードから明示的にデータベース名を入力します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-131">On the **Connection Properties** tab, explicitly enter the database name from the **axdbadmin** record in LCS.</span></span>

<span data-ttu-id="15ec5-132">接続したら、データベースに対してクエリを開き、次の Transact-SQL (T-SQL) コマンドで IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-132">After you're connected, open a query against the database, and enter your IP address in the following Transact-SQL (T-SQL) command.</span></span>

```
-- Create database-level firewall setting for IP a.b.c.d 
EXECUTE sp_set_database_firewall_rule N'Debugging rule for DevTest environment', 'a.b.c.d', 'a.b.c.d'; 
```

<span data-ttu-id="15ec5-133">開発環境に戻って SSMS を開き、UAT データベースに対して同じ **axdbadmin** 資格情報を使用して接続を試みます。</span><span class="sxs-lookup"><span data-stu-id="15ec5-133">Back in your developer environment, open SSMS, and try to connect by using the same **axdbadmin** credentials against the UAT database.</span></span> <span data-ttu-id="15ec5-134">次の手順に進む前に接続できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-134">Verify that you can connect before you continue with the next steps.</span></span>

> [!NOTE]
> <span data-ttu-id="15ec5-135">更新を実行するたびにファイアウォール ホワイトリストはリセットされます。</span><span class="sxs-lookup"><span data-stu-id="15ec5-135">Every time that a refresh is done, the firewall whitelist is reset.</span></span> <span data-ttu-id="15ec5-136">将来の必要なときに、このデータベースに DevTest 環境を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-136">You must add your DevTest environments back to this database when they are required in the future.</span></span>

## <a name="update-a-onebox-devtest-environment-to-connect-to-the-uat-database"></a><span data-ttu-id="15ec5-137">UAT データベースに接続する OneBox DevTest 環境を更新する</span><span class="sxs-lookup"><span data-stu-id="15ec5-137">Update a OneBox DevTest environment to connect to the UAT database</span></span>

<span data-ttu-id="15ec5-138">開発者環境で、データベース接続を変更するために web.config ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-138">In your developer environment, you must now update the web.config file to change the database connection.</span></span> <span data-ttu-id="15ec5-139">この手順を使用すると、データベースに対して UAT からコンフィギュレーションされたローカル コードとバイナリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="15ec5-139">This step will let you run your local code and binaries that are configured against the database from UAT.</span></span>

<span data-ttu-id="15ec5-140">サービス ドライブで **AoSService\\WebRoot** ディレクトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-140">On your Services drive, go to the **AoSService\\WebRoot** directory.</span></span> <span data-ttu-id="15ec5-141">(通常は、サービス ドライブはドライブ J または K です)。web.config という名前のファイルを検索し、*バックアップを作成*します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-141">(Typically, the Services drive is drive J or K.) Find the file that is named web.config, and *make a backup of it*.</span></span> <span data-ttu-id="15ec5-142">次に、メモ帳などのエディターで **web.config** ファイルを開き、次の構成を見つけます。</span><span class="sxs-lookup"><span data-stu-id="15ec5-142">Then open the **web.config** file in Notepad or another editor, and find the following configurations:</span></span>

- <span data-ttu-id="15ec5-143">DataAccess.Database</span><span class="sxs-lookup"><span data-stu-id="15ec5-143">DataAccess.Database</span></span>
- <span data-ttu-id="15ec5-144">DataAccess.DBServer</span><span class="sxs-lookup"><span data-stu-id="15ec5-144">DataAccess.DBServer</span></span>
- <span data-ttu-id="15ec5-145">DataAccess.SqlPwd</span><span class="sxs-lookup"><span data-stu-id="15ec5-145">DataAccess.SqlPwd</span></span>
- <span data-ttu-id="15ec5-146">DataAccess.SqlUser</span><span class="sxs-lookup"><span data-stu-id="15ec5-146">DataAccess.SqlUser</span></span>

<span data-ttu-id="15ec5-147">LCS で UAT 環境の環境詳細ページから値を使用するように、これらのコンフィギュレーションを更新します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-147">Update these configurations so that they use the values from the environment details page for the UAT environment in LCS.</span></span>

```
<add key="DataAccess.Database" value="<example_axdb_fromAzure>" />
<add key="DataAccess.DbServer" value="<example_axdb_server.database.windows.net>" />
<add key="DataAccess.SqlPwd" value="<axdbadmin_password_from_LCS>" />
<add key="DataAccess.SqlUser" value="axdbadmin" />
```
<span data-ttu-id="15ec5-148">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-148">Save the file.</span></span> <span data-ttu-id="15ec5-149">クラウドにホストされている環境で操作している場合は、IISRESET を実行します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-149">If you're operating in a cloud-hosted environment, run IISRESET.</span></span> <span data-ttu-id="15ec5-150">Microsoft が管理する開発者向けのコンピューターを使用していてアクセス許可が制限されている場合、必ず Microsoft Visual Studio を閉じてください。</span><span class="sxs-lookup"><span data-stu-id="15ec5-150">If you're on a Microsoft-managed developer machine and have limited permissions, make sure that Microsoft Visual Studio is closed.</span></span>

<span data-ttu-id="15ec5-151">最後に、Web ブラウザーを開き、DevTest 環境の URL に移動して、UAT データベースからデータを取得することを確認します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-151">Finally, open a web browser, go to the URL of your DevTest environment, and verify that you're pulling data from the UAT database.</span></span>

## <a name="debug-transactions-in-the-devtest-environment"></a><span data-ttu-id="15ec5-152">DevTest 環境でトランザクションをデバッグする</span><span class="sxs-lookup"><span data-stu-id="15ec5-152">Debug transactions in the DevTest environment</span></span>

<span data-ttu-id="15ec5-153">これで、環境が正しく再構成され、Visual Studio を開いてニーズを最も満たすアプリケーション コードでブレークポイントを設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="15ec5-153">Now that your environment is correctly reconfigured, you can open Visual Studio and set a breakpoint in the application code that best meets your needs.</span></span> <span data-ttu-id="15ec5-154">UAT 環境のユーザーは、DevTest 環境でのデバッグ中に影響を受けないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="15ec5-154">Note that users in the UAT environment aren't affected while you debug in the DevTest environment.</span></span>

## <a name="best-practices"></a><span data-ttu-id="15ec5-155">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="15ec5-155">Best practices</span></span>

<span data-ttu-id="15ec5-156">デバッグ エクスペリエンスがすばやく、信頼性の高いものになり、組織内の他のユーザーに影響しないことを保証するのに役立ついくつかの一般的なベスト プラクティスを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-156">Here are some common best practices that will help guarantee that your debugging experience is quick, reliable, and doesn't disrupt other users in your organization:</span></span>

- <span data-ttu-id="15ec5-157">DevTest 環境のコードとバイナリのバージョンが、UAT 環境のバージョンと正確に一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-157">Make sure that the version of the code and binaries in the DevTest environment exactly match the version in the UAT environment.</span></span> <span data-ttu-id="15ec5-158">展開用のパッケージを作成したのと同じブランチに DevTest 環境を接続します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-158">Connect the DevTest environment to the same branch that you build packages for deployment from.</span></span> <span data-ttu-id="15ec5-159">または、リリースされている最新のカスタマイズで最新の状態になっている "HotfixSupport" ブランチに接続します。</span><span class="sxs-lookup"><span data-stu-id="15ec5-159">Alternatively, connect it to a "HotfixSupport" branch that is kept up to date with the latest customizations that are released.</span></span>
- <span data-ttu-id="15ec5-160">Visual Studio からデータベースの同期を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="15ec5-160">Don't run a database synchronization from Visual Studio.</span></span> <span data-ttu-id="15ec5-161">そうしないと、UAT データベース内のスキーマの可用性に影響を与え、UAT 環境のユーザーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="15ec5-161">Otherwise, you will affect the availability of the schema in the UAT database and might affect users in the UAT environment.</span></span>

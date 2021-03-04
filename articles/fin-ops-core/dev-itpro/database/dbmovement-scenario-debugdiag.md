---
title: 生産データベースのコピーのデバッグ
description: このトピックでは、Finance and Operations のデバッグや診断シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: e89dfaf7997379eb8419f0dd03ba21221e99a1f1
ms.sourcegitcommit: 9f9045ad1fc4062a5d112cf312ba691c632aec96
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/26/2021
ms.locfileid: "5068486"
---
# <a name="debug-a-copy-of-the-production-database"></a><span data-ttu-id="5294a-103">生産データベースのコピーのデバッグ</span><span class="sxs-lookup"><span data-stu-id="5294a-103">Debug a copy of the production database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5294a-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="5294a-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="5294a-105">このチュートリアルでは、生産データの最新のコピーの特定のデータとトランザクションをデバッグする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5294a-105">This tutorial shows how to debug specific data and transactions from a recent copy of production data.</span></span>

<span data-ttu-id="5294a-106">このチュートリアルでは、次の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5294a-106">In this tutorial, you will learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="5294a-107">ユーザー受け入れテスト (UAT) 環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="5294a-107">Refresh the user acceptance testing (UAT) environment.</span></span>
> * <span data-ttu-id="5294a-108">承認済リスト (セーフ リスト) に開発者環境の IP アドレスを追加します。</span><span class="sxs-lookup"><span data-stu-id="5294a-108">Add the IP address of your developer environment to an approved list ("safe list").</span></span>
> * <span data-ttu-id="5294a-109">UAT データベースに接続できるように、開発者環境を更新します。</span><span class="sxs-lookup"><span data-stu-id="5294a-109">Update your developer environment so that it connects to the UAT database.</span></span>
> * <span data-ttu-id="5294a-110">ブレークポイントを設定し、データのデバッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="5294a-110">Set a breakpoint, and start to debug the data.</span></span>

<span data-ttu-id="5294a-111">このシナリオの例として、既に稼働している顧客が、開発環境から生産トランザクションの最新のコピーをデバッグしようとしていることがあります。</span><span class="sxs-lookup"><span data-stu-id="5294a-111">As an example of this scenario, a customer who has already gone live wants to debug a recent copy of production transactions from the development environment.</span></span> <span data-ttu-id="5294a-112">これにより、顧客は止まっている特定のトランザクションをデバッグしたり、または実際的なデータセットを使用して新しい機能とレポートを開発できます。</span><span class="sxs-lookup"><span data-stu-id="5294a-112">In this way, the customer will be able to debug specific transactions that are stuck, or develop new features and reports by using realistic datasets.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5294a-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="5294a-113">Prerequisites</span></span>

<span data-ttu-id="5294a-114">更新操作を行うには、実稼働環境を配置している必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="5294a-114">To do a refresh operation, you must have your production environment deployed, or you must have a minimum of two standard UAT environments.</span></span> <span data-ttu-id="5294a-115">このチュートリアルを完了するには、開発者環境が配置されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5294a-115">To complete this tutorial, you must have a developer environment deployed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5294a-116">デバッグの場合、UAT 環境で使用できるのと同じコードとビジネス ロジックを実行する DevTest 環境を使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5294a-116">For debugging, we highly recommend that you use a DevTest environment that runs the same code and business logic that are available in your UAT environment.</span></span> <span data-ttu-id="5294a-117">バージョン コントロールで複数のブランチを使用する場合は、最新の UAT または生産トランザクションをデバッグするために使用される DevTest 環境を、UAT のパッケージを構築するために使用する同じブランチに接続した後、生産に使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5294a-117">If you use multiple branches in version control, we recommend that the DevTest environment that is used to debug recent UAT or production transactions be connected to the same branch that you use to build packages for UAT and, later, for production.</span></span> <span data-ttu-id="5294a-118">これにより、互換性のあるスキーマになるため、DevTest 環境と UAT データベースの間でデータベースの同期を実行する必要がありません。</span><span class="sxs-lookup"><span data-stu-id="5294a-118">In this way, you don't have to run a database synchronization between your DevTest environment and UAT database, because the schema will be compatible.</span></span> <span data-ttu-id="5294a-119">これまで、このような環境は、修正プログラム/サポート環境と呼ばれてきました。通常のコード プロモーション パス外となっているためです。</span><span class="sxs-lookup"><span data-stu-id="5294a-119">Historically, this environment is known as a Hotfix/Support environment, because it's outside your usual code promotion path.</span></span>

## <a name="refresh-the-uat-environment"></a><span data-ttu-id="5294a-120">UAT 環境を更新</span><span class="sxs-lookup"><span data-stu-id="5294a-120">Refresh the UAT environment</span></span> 

<span data-ttu-id="5294a-121">この更新操作は、生産データベースの最新のコピーで UAT 環境を上書きします。</span><span class="sxs-lookup"><span data-stu-id="5294a-121">This refresh operation overwrites the UAT environment with the latest copy of the production database.</span></span> <span data-ttu-id="5294a-122">この手順を完了するには、[トレーニング目的での更新](dbmovement-scenario-general-refresh.md)の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5294a-122">To complete this step, follow the instructions in [Refresh for training purposes](dbmovement-scenario-general-refresh.md).</span></span>

## <a name="enable-database-access"></a><span data-ttu-id="5294a-123">データベース アクセスの有効化</span><span class="sxs-lookup"><span data-stu-id="5294a-123">Enable database access</span></span>

<span data-ttu-id="5294a-124">既定では、すべてのサンドボックス標準受け入れテスト環境で Microsoft Azure データベース プラットフォームとして SQL データベースを使用します。</span><span class="sxs-lookup"><span data-stu-id="5294a-124">By default, all Sandbox Standard Acceptance Test environments use Microsoft Azure SQL Database as their database platform.</span></span> <span data-ttu-id="5294a-125">このような環境のデータベースは、最初に配置された Application Object Server (AOS) へのアクセスを制限するファイアウォールで保護されています。</span><span class="sxs-lookup"><span data-stu-id="5294a-125">The databases for these environments are protected by firewalls that restrict access to the Application Object Server (AOS) with which it was originally deployed.</span></span>

<span data-ttu-id="5294a-126">データベースに接続するには、[ジャストインタイム アクセスの有効化](database-just-in-time-JIT-access.md) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5294a-126">To connect to the database, follow the instructions in [Enable just-in-time access](database-just-in-time-JIT-access.md).</span></span>

> [!NOTE]
> <span data-ttu-id="5294a-127">更新を実行するたびにファイアウォールのセーフ リストはリセットされます。</span><span class="sxs-lookup"><span data-stu-id="5294a-127">Every time that a refresh is done, the firewall safe list is reset.</span></span> <span data-ttu-id="5294a-128">将来の必要なときに、このデータベースに DevTest 環境を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5294a-128">You must add your DevTest environments back to this database when they are required in the future.</span></span>

## <a name="update-a-onebox-devtest-environment-to-connect-to-the-uat-database"></a><span data-ttu-id="5294a-129">UAT データベースに接続する OneBox DevTest 環境を更新する</span><span class="sxs-lookup"><span data-stu-id="5294a-129">Update a OneBox DevTest environment to connect to the UAT database</span></span>

<span data-ttu-id="5294a-130">開発者環境で、データベース接続を変更するために web.config ファイルを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5294a-130">In your developer environment, you must now update the web.config file to change the database connection.</span></span> <span data-ttu-id="5294a-131">この手順を使用すると、データベースに対して UAT からコンフィギュレーションされたローカル コードとバイナリを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5294a-131">This step will let you run your local code and binaries that are configured against the database from UAT.</span></span>

<span data-ttu-id="5294a-132">サービス ドライブで **AoSService\\WebRoot** ディレクトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="5294a-132">On your Services drive, go to the **AoSService\\WebRoot** directory.</span></span> <span data-ttu-id="5294a-133">(通常は、サービス ドライブはドライブ J または K です)。web.config という名前のファイルを検索し、*バックアップを作成* します。</span><span class="sxs-lookup"><span data-stu-id="5294a-133">(Typically, the Services drive is drive J or K.) Find the file that is named web.config, and *make a backup of it*.</span></span> <span data-ttu-id="5294a-134">次に、メモ帳などのエディターで **web.config** ファイルを開き、次の構成を見つけます。</span><span class="sxs-lookup"><span data-stu-id="5294a-134">Then open the **web.config** file in Notepad or another editor, and find the following configurations:</span></span>

- <span data-ttu-id="5294a-135">DataAccess.Database</span><span class="sxs-lookup"><span data-stu-id="5294a-135">DataAccess.Database</span></span>
- <span data-ttu-id="5294a-136">DataAccess.DBServer</span><span class="sxs-lookup"><span data-stu-id="5294a-136">DataAccess.DBServer</span></span>
- <span data-ttu-id="5294a-137">DataAccess.SqlPwd</span><span class="sxs-lookup"><span data-stu-id="5294a-137">DataAccess.SqlPwd</span></span>
- <span data-ttu-id="5294a-138">DataAccess.SqlUser</span><span class="sxs-lookup"><span data-stu-id="5294a-138">DataAccess.SqlUser</span></span>

<span data-ttu-id="5294a-139">LCS で UAT 環境の環境詳細ページから値を使用するように、これらのコンフィギュレーションを更新します。</span><span class="sxs-lookup"><span data-stu-id="5294a-139">Update these configurations so that they use the values from the environment details page for the UAT environment in LCS.</span></span>

```xml
<add key="DataAccess.Database" value="<example_axdb_fromAzure>" />
<add key="DataAccess.DbServer" value="<example_axdb_server.database.windows.net>" />
<add key="DataAccess.SqlPwd" value="<axdbadmin_password_from_LCS>" />
<add key="DataAccess.SqlUser" value="axdbadmin" />
```
<span data-ttu-id="5294a-140">ファイル保存します。</span><span class="sxs-lookup"><span data-stu-id="5294a-140">Save the file.</span></span> <span data-ttu-id="5294a-141">クラウドにホストされている環境で操作している場合は、IISRESET を実行します。</span><span class="sxs-lookup"><span data-stu-id="5294a-141">If you're operating in a cloud-hosted environment, run IISRESET.</span></span> <span data-ttu-id="5294a-142">Microsoft が管理する開発者向けのコンピューターを使用していてアクセス許可が制限されている場合、必ず Microsoft Visual Studio を閉じてください。</span><span class="sxs-lookup"><span data-stu-id="5294a-142">If you're on a Microsoft-managed developer machine and have limited permissions, make sure that Microsoft Visual Studio is closed.</span></span>

<span data-ttu-id="5294a-143">最後に、Web ブラウザーを開き、DevTest 環境の URL に移動して、UAT データベースからデータを取得することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5294a-143">Finally, open a web browser, go to the URL of your DevTest environment, and verify that you're pulling data from the UAT database.</span></span>

## <a name="debug-transactions-in-the-devtest-environment"></a><span data-ttu-id="5294a-144">DevTest 環境でトランザクションをデバッグする</span><span class="sxs-lookup"><span data-stu-id="5294a-144">Debug transactions in the DevTest environment</span></span>

<span data-ttu-id="5294a-145">これで、環境が正しく再構成され、Visual Studio を開いてニーズを最も満たすアプリケーション コードでブレークポイントを設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5294a-145">Now that your environment is correctly reconfigured, you can open Visual Studio and set a breakpoint in the application code that best meets your needs.</span></span> <span data-ttu-id="5294a-146">UAT 環境のユーザーは、DevTest 環境でのデバッグ中に影響を受けないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5294a-146">Note that users in the UAT environment aren't affected while you debug in the DevTest environment.</span></span>

### <a name="debugging-batch"></a><span data-ttu-id="5294a-147">バッチのデバッグ</span><span class="sxs-lookup"><span data-stu-id="5294a-147">Debugging batch</span></span>

<span data-ttu-id="5294a-148">バッチ・ジョブをデバッグする必要があるシナリオでは、デバッグ DevTest マシン上で、Visual Studio からデバッガーを関連付けるオプションとして表示される前にバッチ・サービスを再起動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5294a-148">For scenarios where you need to debug batch jobs, on the debugging DevTest machine, you may need to restart the batch service before it will show up as an option to attach the debugger from Visual Studio.</span></span> <span data-ttu-id="5294a-149">さらに、この DevTest マシンを独自のバッチ グループに分離して、デバッグするジョブが DevTest マシンで実行されるようにしておくと便利です。</span><span class="sxs-lookup"><span data-stu-id="5294a-149">In addition, it may also be helpful to isolate this DevTest machine in to its own batch group to ensure that any jobs that you want to debug will run on the DevTest machine.</span></span>

## <a name="best-practices"></a><span data-ttu-id="5294a-150">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="5294a-150">Best practices</span></span>

<span data-ttu-id="5294a-151">デバッグ エクスペリエンスがすばやく、信頼性の高いものになり、組織内の他のユーザーに影響しないことを保証するのに役立ついくつかの一般的なベスト プラクティスを以下に示します。</span><span class="sxs-lookup"><span data-stu-id="5294a-151">Here are some common best practices that will help guarantee that your debugging experience is quick, reliable, and doesn't disrupt other users in your organization:</span></span>

- <span data-ttu-id="5294a-152">DevTest 環境のコードとバイナリのバージョンが、UAT 環境のバージョンと正確に一致することを確認します。</span><span class="sxs-lookup"><span data-stu-id="5294a-152">Make sure that the version of the code and binaries in the DevTest environment exactly match the version in the UAT environment.</span></span> <span data-ttu-id="5294a-153">展開用のパッケージを作成したのと同じブランチに DevTest 環境を接続します。</span><span class="sxs-lookup"><span data-stu-id="5294a-153">Connect the DevTest environment to the same branch that you build packages for deployment from.</span></span> <span data-ttu-id="5294a-154">または、リリースされている最新のカスタマイズで最新の状態になっている "HotfixSupport" ブランチに接続します。</span><span class="sxs-lookup"><span data-stu-id="5294a-154">Alternatively, connect it to a "HotfixSupport" branch that is kept up to date with the latest customizations that are released.</span></span>
- <span data-ttu-id="5294a-155">Visual Studio からデータベースの同期を実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="5294a-155">Don't run a database synchronization from Visual Studio.</span></span> <span data-ttu-id="5294a-156">そうしないと、UAT データベース内のスキーマの可用性に影響を与え、UAT 環境のユーザーに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5294a-156">Otherwise, you will affect the availability of the schema in the UAT database and might affect users in the UAT environment.</span></span>
- <span data-ttu-id="5294a-157">最適なエクスペリエンスのため、UAT 環境として同じデータセンターに配置された開発者環境を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5294a-157">For the best experience, use a developer environment that was deployed in the same datacenter as the UAT environment.</span></span>

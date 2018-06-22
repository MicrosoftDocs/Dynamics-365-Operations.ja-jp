---
title: "生産データベースのコピーに対する X++ のデバッグ"
description: "このトピックでは、実稼働環境で問題を調査できるように X++ デバッグを構成する方法について説明します。"
author: tariqbell
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 199063
ms.assetid: 3c0551f3-6c96-4518-8acd-82d4638f9323
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8a26442b8eb92914d6e612d29ea2346d3cb9dbfc
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="debug-x-against-a-copy-of-a-production-database"></a><span data-ttu-id="488da-103">生産データベースのコピーに対する X++ のデバッグ</span><span class="sxs-lookup"><span data-stu-id="488da-103">Debug X++ against a copy of a production database</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="488da-104">このトピックでは、実稼働環境で問題を調査できるように X++ デバッグを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="488da-104">This topic explains how to configure X++ debugging so that you can investigate issues in the production environment.</span></span> <span data-ttu-id="488da-105">この手順では、生産データベースのコピーを作成し、コピーに接続するための開発環境をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="488da-105">For this procedure, you make a copy of the production database and then configure a developer environment to connect to the copy.</span></span>

## <a name="solution-overview"></a><span data-ttu-id="488da-106">ソリューションの概要</span><span class="sxs-lookup"><span data-stu-id="488da-106">Solution overview</span></span>

<span data-ttu-id="488da-107">実稼働環境で X++ のデバッグが必要な問題が発生したときは、システム管理者と開発者は連携して、デバッグを構成してから問題をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="488da-107">When an issue that requires X++ debugging occurs in a production environment, the system administrator and developer work together to configure debugging and then debug the issue.</span></span> <span data-ttu-id="488da-108">次の図は、プロセスの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="488da-108">The following illustration shows an overview of the process.</span></span>

<span data-ttu-id="488da-109">[![デバッグ プロセス](./media/debugxpp.jpg)](./media/debugxpp.jpg)</span><span class="sxs-lookup"><span data-stu-id="488da-109">[![Debugging process](./media/debugxpp.jpg)](./media/debugxpp.jpg)</span></span>

1. <span data-ttu-id="488da-110">Microsoft Dynamics Lifecycle Services (LCS) では、システム管理者がデータベースのコピーをサンドボックス ユーザー受け入れテスト (UAT) 環境に接続するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="488da-110">In Microsoft Dynamics Lifecycle Services (LCS), the system administrator requests that a copy of the database be connected to the sandbox user acceptance testing (UAT) environment.</span></span> <span data-ttu-id="488da-111">(つまり、データベース更新を要求します。)</span><span class="sxs-lookup"><span data-stu-id="488da-111">(In other words, request a database refresh.)</span></span>
2. <span data-ttu-id="488da-112">Microsoft Visual Studio Team Services (VSTS) では、開発者が実稼働環境で実行されている同じビルドにローカル コードを同期します。</span><span class="sxs-lookup"><span data-stu-id="488da-112">In Microsoft Visual Studio Team Services (VSTS), the developer synchronizes the local code to the same build that is running in the production environment.</span></span>
3. <span data-ttu-id="488da-113">Microsoft Azure SQL データベースのサンドボックス インスタンスでは、システム管理者が開発者に一時的な SQL サインインを作成します。</span><span class="sxs-lookup"><span data-stu-id="488da-113">In the sandbox instance of Microsoft Azure SQL Database, the system administrator creates a temporary SQL sign-in for the developer.</span></span> <span data-ttu-id="488da-114">開発者は、サンドボックス データベースに接続するための環境を設定します。</span><span class="sxs-lookup"><span data-stu-id="488da-114">The developer then configures the environment to connect to the sandbox database.</span></span>
4. <span data-ttu-id="488da-115">開発環境がサンドボックスのデータベースに接続できるように、ファイアウォールに例外が追加されています。</span><span class="sxs-lookup"><span data-stu-id="488da-115">A firewall exception is added so that the developer environment can connect to the sandbox database.</span></span>
5. <span data-ttu-id="488da-116">開発者は問題をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="488da-116">The developer debugs the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="488da-117">デバッグが完了したら、システム管理者は、一時的なサインインをサンド ボックスの SQL データベースから削除できます。</span><span class="sxs-lookup"><span data-stu-id="488da-117">When debugging is completed, the system administrator can remove the temporary sign-in from the sandbox SQL database.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="488da-118">準備</span><span class="sxs-lookup"><span data-stu-id="488da-118">Before you begin</span></span>

<span data-ttu-id="488da-119">実稼働環境で X++ デバッグ を構成する前に、次の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="488da-119">Before you begin to configure X++ debugging in a production environment, note the following points:</span></span>

- <span data-ttu-id="488da-120">デバッグためにデータの破損が発生する可能性がありますので、実稼働環境を直接デバッグできません。</span><span class="sxs-lookup"><span data-stu-id="488da-120">You can't debug directly against the production environment, because debugging might cause data corruption.</span></span> <span data-ttu-id="488da-121">ただし、開発者は実行時に値を操作できます。</span><span class="sxs-lookup"><span data-stu-id="488da-121">However, developers can manipulate values at runtime.</span></span> <span data-ttu-id="488da-122">あるいは、独自のインスタンスでは、開発者はデータを変更するコード変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="488da-122">Alternatively, in their own instance, developers can make a code change that changes data.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="488da-123">デバッグに使用される開発環境は、サンドボックス環境と同じ LCS プロジェクトに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="488da-123">The developer environment that is used for debugging must exist in the same LCS project as the sandbox environment.</span></span> <span data-ttu-id="488da-124">この要件は、サンドボックス データベースのセキュリティを強化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="488da-124">This requirement helps strengthen the security of the sandbox database.</span></span> <span data-ttu-id="488da-125">既定では、サンドボックスと生産 SQL データベースの両方にファイアウォールの制限があります。</span><span class="sxs-lookup"><span data-stu-id="488da-125">By default, there is a firewall restriction on both the sandbox and production SQL databases.</span></span> <span data-ttu-id="488da-126">この制限により、これらの環境内のサーバーのみがデータベースに接続できます。</span><span class="sxs-lookup"><span data-stu-id="488da-126">This restriction allows only servers in those environments to connect to the databases.</span></span> <span data-ttu-id="488da-127">デバッグを有効にするため、開発環境がサンドボックスのデータベースに接続できるように、ファイアウォールに例外が追加されています。</span><span class="sxs-lookup"><span data-stu-id="488da-127">To enable debugging, a firewall exception is added so that a developer environment can connect to the sandbox database.</span></span>

- <span data-ttu-id="488da-128">環境の IP アドレスがサンドボックス データベースに接続できるようにするため、開発者環境への 1 回限りの手動変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="488da-128">A one-time manual change to the developer environment is required, so that the IP address of the environment can connect to the sandbox database.</span></span> <span data-ttu-id="488da-129">IP アドレスを許可するために Microsoft サービス エンジニア リング チーム (DSE) に要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="488da-129">Submit a request to the Microsoft Service Engineering Team (DSE) to allow the IP address.</span></span>
- <span data-ttu-id="488da-130">デバッグにビルド環境を使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="488da-130">We recommend that you not use a build environment for debugging.</span></span> <span data-ttu-id="488da-131">それ以外の場合、コンピュータで開発者の活動が自動ビルド プロセスを中断するリスクがあります。</span><span class="sxs-lookup"><span data-stu-id="488da-131">Otherwise, there is a risk that the developer's activities on the computer might break the automated build process.</span></span>

## <a name="solution-details"></a><span data-ttu-id="488da-132">ソリューションの詳細</span><span class="sxs-lookup"><span data-stu-id="488da-132">Solution details</span></span>

<span data-ttu-id="488da-133">実稼動環境で問題が発生する場合は、システム管理者は LCS にサインインして、データベースのコピーをサンド ボックス環境に追加するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="488da-133">When an issue occurs in the production environment, the system administrator can sign in to LCS and request that a database copy be added to a sandbox environment.</span></span> <span data-ttu-id="488da-134">データベースのコピーの実行中、システム管理者は開発者に問題について通知することができます。</span><span class="sxs-lookup"><span data-stu-id="488da-134">While the database copy is running, the system administrator can notify the developer of the issue.</span></span> <span data-ttu-id="488da-135">開発者は、コードの正しいビルドに同期して、実稼働環境に合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="488da-135">The developer can then synchronize to the correct build of the code to match the production environment.</span></span>

1. <span data-ttu-id="488da-136">Microsoft Visual Studio のソース管理エクスプローラーで、同期するブランチのルート ノードを右クリックしてから、**詳細** &gt; **特定のバージョンを取得**を選択します。</span><span class="sxs-lookup"><span data-stu-id="488da-136">In Microsoft Visual Studio, in Source Control Explorer, right-click the root node of the branch to synchronize, and then select **Advanced** &gt; **Get specific version**.</span></span>
2. <span data-ttu-id="488da-137">ダイアログ ボックスで、**Type=Label** を選択してから省略記号 (**...**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="488da-137">In the dialog box, select **Type=Label**, and then select the ellipsis (**...**).</span></span>
3. <span data-ttu-id="488da-138">ダイアログ ボックスで**検索**を選択します。</span><span class="sxs-lookup"><span data-stu-id="488da-138">In the dialog box, select **Find**.</span></span> <span data-ttu-id="488da-139">ビルド サーバーからのすべてのビルドがリストに記載されます。</span><span class="sxs-lookup"><span data-stu-id="488da-139">All the builds from the build server are listed.</span></span>
4. <span data-ttu-id="488da-140">実稼動環境に現在配置されているビルドを選択し、フル ビルドの実行を選択します。</span><span class="sxs-lookup"><span data-stu-id="488da-140">Select the build that is currently deployed in the production environment, and then select to run a full build.</span></span> <span data-ttu-id="488da-141">データベースをコピーすると、システム管理者のみがサンド ボックス データベースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="488da-141">When the database is copied, only the system administrator will be able to access the sandbox database.</span></span> <span data-ttu-id="488da-142">システム管理者は、次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="488da-142">The system administrator must complete the following tasks:</span></span>

    - <span data-ttu-id="488da-143">従業員の給与など、サンドボックス データベースに不要なデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="488da-143">Remove any data that you don't want in the sandbox database, such as employee salaries.</span></span>
    - <span data-ttu-id="488da-144">ユーザーとして、開発者を有効または追加にします。</span><span class="sxs-lookup"><span data-stu-id="488da-144">Enable or add the developer as a user.</span></span>
    - <span data-ttu-id="488da-145">開発者が使用できる新しい SQL サインインを作成します。</span><span class="sxs-lookup"><span data-stu-id="488da-145">Create a new SQL sign-in that the developer can use.</span></span> <span data-ttu-id="488da-146">このステップにより、システム管理者はサンドボックス環境のセキュリティを維持できます。</span><span class="sxs-lookup"><span data-stu-id="488da-146">This step lets the system administrator maintain the security of the sandbox environment.</span></span> <span data-ttu-id="488da-147">開発者は限られた時間だけ 1 つのデータベースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="488da-147">The developer will have access to one database for only a limited time.</span></span> <span data-ttu-id="488da-148">新しい SQL サインインを作成するには、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="488da-148">Use the following code to create the new SQL sign-in.</span></span>

        ```
        CREATE USER devtempuser WITH PASSWORD = ''
        EXEC sp_addrolemember 'db_owner', 'devtempuser'
        ```

<span data-ttu-id="488da-149">次に、開発者は、Application Object Server (AOS) の web.config ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="488da-149">Next, the developer edits the web.config file for Application Object Server (AOS).</span></span>

1. <span data-ttu-id="488da-150">**J:\\AosService\\WebRoot\\web.config** に移動します。</span><span class="sxs-lookup"><span data-stu-id="488da-150">Go to **J:\\AosService\\WebRoot\\web.config**.</span></span>
2. <span data-ttu-id="488da-151">後で切り替えることができるように、元の web.config ファイルのコピーを保存します。</span><span class="sxs-lookup"><span data-stu-id="488da-151">Save a copy of the original web.config file, so that you can switch back later.</span></span>
3. <span data-ttu-id="488da-152">web.config ファイルの次のセクションを編集します。</span><span class="sxs-lookup"><span data-stu-id="488da-152">Edit the following section in the web.config file.</span></span>

    <span data-ttu-id="488da-153">**変更前**</span><span class="sxs-lookup"><span data-stu-id="488da-153">**Before your changes**</span></span>

    ```
    <add key="DataAccess.Database" value="sandboxDatabaseName" />
    <add key="DataAccess.DbServer" value="sandboxDbServerName.database.windows.net" />
    <add key="DataAccess.SqlPwd" value="password" />
    <add key="DataAccess.SqlUser" value="devtempuser" />
    ```

    <span data-ttu-id="488da-154">**変更後**</span><span class="sxs-lookup"><span data-stu-id="488da-154">**After your changes**</span></span>

    ```
    <add key="DataAccess.Database" value="TariqRTW_axdb_dd78f8aadbc6c481" />
    <add key="DataAccess.DbServer" value="vyxx2dflyo.database.windows.net" />
    <add key="DataAccess.SqlPwd" value="P@ssw0rd" />
    <add key="DataAccess.SqlUser" value="devtempuser" />
    ```

4. <span data-ttu-id="488da-155">問題をデバッグします。</span><span class="sxs-lookup"><span data-stu-id="488da-155">Debug the issue.</span></span>

<span data-ttu-id="488da-156">開発者が終了すると、 システム管理者はサンドボックス データベースから devtempuser を削除できます。</span><span class="sxs-lookup"><span data-stu-id="488da-156">After the developer has finished, the system administrator can remove devtempuser from the sandbox database.</span></span> <span data-ttu-id="488da-157">このステップにより、開発者はサンドボックス データベースに永続的にアクセスできなくなります。</span><span class="sxs-lookup"><span data-stu-id="488da-157">This step prevents the developer from having permanent access to the sandbox database.</span></span>


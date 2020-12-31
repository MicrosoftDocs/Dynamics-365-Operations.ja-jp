---
title: ドキュメント回覧エージェントを Windows サービスとして実行する
description: ドキュメント回覧エージェントは、デスクトップ アプリケーションまたは Microsoft Windows サービスのいずれかとして実行できます。 このトピックでは、正しく実行モードを選択するのに役立つ重要な情報を提供します。
author: TJVass
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.custom: 191133
ms.assetid: 7adc7228-4360-4a54-8a3e-4d916e727dd2
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: d749c3d1f288cc0facf7aafb91e13f54bfecb10c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688219"
---
# <a name="run-the-document-routing-agent-as-a-windows-service"></a><span data-ttu-id="dfd4b-104">ドキュメント回覧エージェントを Windows サービスとして実行する</span><span class="sxs-lookup"><span data-stu-id="dfd4b-104">Run the Document Routing Agent as a Windows service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfd4b-105">ドキュメント回覧エージェントには、実行モードを選択できるオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-105">The Document Routing Agent includes an option that lets you select the mode of execution.</span></span> <span data-ttu-id="dfd4b-106">このプロセスは、デスクトップ アプリケーションまたは Microsoft Windows サービスのいずれかとして実行できます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-106">The process can run as either a desktop application or a Microsoft Windows service.</span></span> <span data-ttu-id="dfd4b-107">アプリケーションは、Windows サービスとして実行されるとき、コンピューターの再起動後に自動的に起動することができます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-107">When the application runs as a Windows service, it can be started automatically after a computer restart.</span></span> <span data-ttu-id="dfd4b-108">また、特定のユーザー アカウントのセキュリティ コンテキストで実行するように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-108">It can also be configured to run under the security context of a specific user account.</span></span> <span data-ttu-id="dfd4b-109">この機能拡張により、顧客はネットワーク プリント サーバーなどのセキュリティで保護されたドメイン リソースでドキュメント ルート指定エージェントをホストできます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-109">This enhancement lets customers host the Document Routing Agent on secured domain resources such as network print servers.</span></span>

<span data-ttu-id="dfd4b-110">このトピックでは、正しく実行モードを選択するのに役立つ重要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-110">This topic provides important information that will help you select the correct execution mode.</span></span>

## <a name="service-applications"></a><span data-ttu-id="dfd4b-111">サービス アプリケーション</span><span class="sxs-lookup"><span data-stu-id="dfd4b-111">Service applications</span></span>
<span data-ttu-id="dfd4b-112">アプリケーションはユーザーがデスクトップ上で連携するプログラムです。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-112">An application is a program that a user interacts with on the desktop.</span></span> <span data-ttu-id="dfd4b-113">サービスは、バックグラウンドで実行され、アクティブなウィンドウを持たないプロセスです。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-113">A service is a process that runs in the background and doesn't have an active window.</span></span> <span data-ttu-id="dfd4b-114">ドキュメント回覧エージェントは現在、両方の実行モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-114">The Document Routing Agent now supports both execution modes.</span></span> <span data-ttu-id="dfd4b-115">他方ではなくそのモードを選択する理由、およびサービスとしてのプロセスの実行に関連するステップを理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-115">It's important that you understand why you might select one mode instead of the other and the steps that are involved in running the process as a service.</span></span> <span data-ttu-id="dfd4b-116">Windows サービスの詳細については、[Windows サービス アプリケーションの概要](/dotnet/framework/windows-services/introduction-to-windows-service-applications) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-116">For more information about Windows services, see [Introduction to Windows Service Applications](/dotnet/framework/windows-services/introduction-to-windows-service-applications).</span></span> <span data-ttu-id="dfd4b-117">バックグラウンド サービスとしてドキュメント回覧エージェントを実行する主な利点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-117">Here are some of the main benefits of running the Document Routing Agent as a background service:</span></span>

- <span data-ttu-id="dfd4b-118">コンピューターを再起動すると自動的にサービスが開始されるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-118">The service can be configured to start automatically after a computer restart.</span></span> <span data-ttu-id="dfd4b-119">ユーザー操作は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-119">No user intervention is required.</span></span>
- <span data-ttu-id="dfd4b-120">サービスは、バックグラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-120">The service runs in the background.</span></span> <span data-ttu-id="dfd4b-121">通知領域で実行される有効なアプリケーションはありません。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-121">No active application runs in the notification area.</span></span>
- <span data-ttu-id="dfd4b-122">このサービスは、ユーザーがキャッシュされた資格情報を使用してサインインせずに、ドキュメントをルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-122">The service routes documents without requiring that a user sign in by using cached credentials.</span></span>

<span data-ttu-id="dfd4b-123">ドキュメント回覧エージェントを Windows サービスとして実行することには多くの利点がありますが、制限もあります。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-123">Although there are many benefits of running the Document Routing Agent as a Windows service, there are also limitations.</span></span> <span data-ttu-id="dfd4b-124">次のセクションでは、カスタムのページ マージンを必要とする小切手などのドキュメント レポートの処理に影響する問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-124">The next section discusses an issue that affects the handling of document reports, such as checks, that require custom page margins.</span></span>

## <a name="documents-that-require-custom-margins"></a><span data-ttu-id="dfd4b-125">カスタム マージンを要求するドキュメント</span><span class="sxs-lookup"><span data-stu-id="dfd4b-125">Documents that require custom margins</span></span>
<span data-ttu-id="dfd4b-126">ドキュメント回覧エージェントが Windows サービスとして実行されるときは、ユーザー設定の余白を必要とする小切手などのドキュメント レポートをネットワーク プリンターに直接印刷することはできません。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-126">When the Document Routing Agent runs as a Windows service, document reports, such as checks, that require custom margins can't be printed directly to network printers.</span></span> <span data-ttu-id="dfd4b-127">代わりに、このドキュメント回覧エージェントは自動的にこれらのドキュメントをターゲット フォルダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-127">Instead, the Document Routing Agent automatically routes those document to a target folder.</span></span> <span data-ttu-id="dfd4b-128">アプリケーションの **設定** ダイアログ ボックスにある新しいコンフィギュレーション プロパティで、カスタム マージンを必要とするドキュメント レポートの対象となる場所を定義できます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-128">New configuration properties in the application's **Settings** dialog box let you define the target location for document reports that require custom margins.</span></span>

<span data-ttu-id="dfd4b-129">ドキュメント回覧エージェントは、デスクトップ アプリケーションとして実行されるときは、Adobe Reader の活用する続行して、Finance and Operations で選択されている共有プリンター デバイスにドキュメントをスプールします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-129">When the Document Routing Agent runs as a desktop application, it continues to take advantage of Adobe Reader to spool the document to the shared printer device that is selected in Finance and Operations.</span></span> <span data-ttu-id="dfd4b-130">カスタムの余白を設定したドキュメントを印刷する必要があるシナリオを処理するには、ドキュメント ルーティング エージェントを複数の場所にインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-130">To handle scenarios where documents that have custom margins must be printed, we recommend that you install the Document Routing Agent in multiple locations.</span></span> <span data-ttu-id="dfd4b-131">デスクトップ アプリケーション モードで実行されるドキュメント ルーティング エージェントでのみ、これらのドキュメントを処理するプリンターをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-131">Then install the printers that will handle those documents only on the Document Routing Agents that will run in desktop application mode.</span></span> <span data-ttu-id="dfd4b-132">または、実行後のプロセスを使用してターゲット ディレクトリ内のファイルを取得し適切な方法でそれらを指示します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-132">Alternatively, use a post-execution process to pick up the files in the target directory and direct them in the appropriate manner.</span></span>

## <a name="install-the-latest-build"></a><span data-ttu-id="dfd4b-133">最新ビルドのインストール</span><span class="sxs-lookup"><span data-stu-id="dfd4b-133">Install the latest build</span></span>
1. <span data-ttu-id="dfd4b-134">現在のドキュメント回覧エージェント構成ファイルのコピーを保存します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-134">Save a copy of the current Document Routing Agent configuration file.</span></span> <span data-ttu-id="dfd4b-135">このファイルは、C:\\Users\\&lt;UserID&gt;\\AppData\\Local\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing\\Microsoft.Dynamics.AX.Framework.DocumentRouting.config にあります。このパスでは、&lt;UserID&gt;は、ドキュメント ルーティング エージェントがインストールされた Active Directory Domain Services (AD DS) のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-135">This file is located at C:\\Users\\&lt;UserID&gt;\\AppData\\Local\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing\\Microsoft.Dynamics.AX.Framework.DocumentRouting.config. In this path, &lt;UserID&gt; is the Active Directory Domain Services (AD DS) user name that the Document Routing Agent was installed under.</span></span>
2. <span data-ttu-id="dfd4b-136">ドキュメント回覧エージェントの現在のバージョンをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-136">Uninstall the current version of the Document Routing Agent.</span></span>
3. <span data-ttu-id="dfd4b-137">[ネットワーク印刷を有効にするためにドキュメント回覧エージェントをインストールする](install-document-routing-agent.md)の手順に従って、ドキュメント回覧エージェントの最新バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-137">Install the latest version of the Document Routing Agent by following the instructions in [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="dfd4b-138">この時点でアプリケーションをインストールしますが、まだ実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-138">Although you install the application at this point, don't run it yet.</span></span>

4. <span data-ttu-id="dfd4b-139">手順 1 では、構成ファイルをコピーし、次のディレクトリに貼り付けます。c:\\ProgramData\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-139">Copy the configuration file from step 1, and paste it into the following directory: C:\\ProgramData\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing.</span></span> <span data-ttu-id="dfd4b-140">このステップにより、ドキュメント回覧エージェント アプリケーションの新しいバージョンに以前のすべての構成設定が使用されていることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-140">This step helps guarantee that all your previous configuration settings are used for the new version of the Document Routing Agent application.</span></span>
5. <span data-ttu-id="dfd4b-141">ドキュメント回覧エージェントを実行します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-141">Run the Document Routing Agent.</span></span>
6. <span data-ttu-id="dfd4b-142">Microsoft Azure Active Directory ( Azure AD) または Finance and Operations アプリの資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-142">Sign in by using your Microsoft Azure Active Directory (Azure AD) or your credentials for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="dfd4b-143">適切なメニュー項目をクリックして、設定およびプリンターを表示して確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-143">View and verify your settings and printers by clicking the appropriate menu items.</span></span>

<span data-ttu-id="dfd4b-144">次のセクションでは、Windows サービスの実行モードを選択するための詳細な手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-144">The next section provides detailed instructions for selecting the Windows service execution mode.</span></span>

## <a name="change-the-default-execution-mode"></a><span data-ttu-id="dfd4b-145">既定の実行モードの変更</span><span class="sxs-lookup"><span data-stu-id="dfd4b-145">Change the default execution mode</span></span>
<span data-ttu-id="dfd4b-146">既定では、ドキュメント回覧エージェントはデスクトップ アプリケーションとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-146">By default, the Document Routing Agent runs as a desktop application.</span></span> <span data-ttu-id="dfd4b-147">プロセスを Windows サービスとして実行するには、[[ドキュメント ルーティング エージェントをインストールしてネットワーク プリンタ デバイスを有効にする](install-document-routing-agent.md)] のプロセスに精通していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-147">To run the process as a Windows service, make sure that you're familiar with the process for [installing the Document Routing Agent to enable network printer devices](install-document-routing-agent.md).</span></span> <span data-ttu-id="dfd4b-148">その後次のタスクをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-148">Then complete the following tasks.</span></span>

### <a name="update-the-execution-mode-for-the-document-routing-agent"></a><span data-ttu-id="dfd4b-149">ドキュメント回覧エージェントの実行モードを更新</span><span class="sxs-lookup"><span data-stu-id="dfd4b-149">Update the execution mode for the Document Routing Agent</span></span>
1. <span data-ttu-id="dfd4b-150">デスクトップ アイコンを使用してドキュメント回覧エージェントを起動します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-150">Start the Document Routing Agent by using the desktop icon.</span></span>
2. <span data-ttu-id="dfd4b-151">**サインイン** オプションを選択し、Azure AD 資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-151">Select the **Sign In** option, and sign in by using your Azure AD credentials.</span></span>
3. <span data-ttu-id="dfd4b-152">リボンで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-152">On the ribbon, select **Settings**.</span></span>
4. <span data-ttu-id="dfd4b-153">**Windows Service として実行** オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-153">Enable the **Run as a Windows Service** option.</span></span>
5. <span data-ttu-id="dfd4b-154">ユーザー設定の余白を持つドキュメントに生成される PDF ファイルの対象となるフォルダーを提供します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-154">Provide a target folder for PDF files that are produced for documents that have custom margins.</span></span>
6. <span data-ttu-id="dfd4b-155">**OK** を選択し、ドキュメント回覧エージェント ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-155">Select **OK**, and close the Document Routing Agent window.</span></span>

### <a name="configure-and-start-the-windows-service"></a><span data-ttu-id="dfd4b-156">Windows サービスのコンフィギュレーションおよび開始</span><span class="sxs-lookup"><span data-stu-id="dfd4b-156">Configure and start the Windows service</span></span>
1. <span data-ttu-id="dfd4b-157">Windows で、Service Manager を開始します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-157">In Windows, start Service Manager.</span></span>
2. <span data-ttu-id="dfd4b-158">一覧で、**Microsoft Dynamics 365 for Finance and Operations ドキュメント ルーティング サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-158">In the list, select **Microsoft Dynamics 365 for Finance and Operations Document Routing Service**.</span></span>
3. <span data-ttu-id="dfd4b-159">名前を右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-159">Right-click the name, and then select **Properties**.</span></span>
4. <span data-ttu-id="dfd4b-160">**ログオン** タブで、**この勘定** オプションを選択し、サービスを実行するために使用される AD DS 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-160">On the **Log On** tab, select the **This account** option, and then supply the AD DS credentials that are used to run the service.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dfd4b-161">選択したアカウントが共有ネットワーク デバイスにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-161">Make sure that the selected account has access to the shared network devices.</span></span>

5. <span data-ttu-id="dfd4b-162">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-162">Select **OK**.</span></span>
6. <span data-ttu-id="dfd4b-163">サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-163">Start the service.</span></span>

<span data-ttu-id="dfd4b-164">ドキュメント回覧エージェントは現在 Windows サービス アプリケーションとして実行されています。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-164">The Document Routing Agent is now running as a Windows service.</span></span>

## <a name="troubleshooting-tips"></a><span data-ttu-id="dfd4b-165">ヒントのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="dfd4b-165">Troubleshooting tips</span></span>
### <a name="verify-the-network-printer-connection"></a><span data-ttu-id="dfd4b-166">ネットワーク プリンターの接続を確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-166">Verify the network printer connection</span></span>
- <span data-ttu-id="dfd4b-167">有効なアカウントにネットワーク プリンターへの十分なアクセス権があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-167">Verify that the active account has enough access rights to the network printer.</span></span>
- <span data-ttu-id="dfd4b-168">メモ帳または別のローカル アプリケーションを使用して、ユーザー アカウントがネットワーク デバイスに正常に印刷できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-168">Verify that the user account can successfully print to the network device by using Notepad or another local application.</span></span>

### <a name="verify-security-roles"></a><span data-ttu-id="dfd4b-169">セキュリティ ロールの確認</span><span class="sxs-lookup"><span data-stu-id="dfd4b-169">Verify security roles</span></span>
- <span data-ttu-id="dfd4b-170">ドキュメント ルート指定クライアントのインストールに使用されるアプリケーション リンクにアクセスするには、ユーザーは **ドキュメント ルート指定クライアント** のセキュリティ ロールの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-170">To access the application links that are used to install the Document Routing Agent, the user must be part of the **Document routing client** security role.</span></span>

### <a name="review-the-service-accounts-access-rights"></a><span data-ttu-id="dfd4b-171">サービス アカウントのアクセス権を確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-171">Review the service account's access rights</span></span>
- <span data-ttu-id="dfd4b-172">ネットワーク デバイスにアクセスできるドメイン アカウントとして **DocumentRoutingService** サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-172">Verify that the **DocumentRoutingService** service is running as a domain account that has access to the network devices.</span></span>

### <a name="refresh-the-azure-service-token"></a><span data-ttu-id="dfd4b-173">Azure サービス トークンを更新</span><span class="sxs-lookup"><span data-stu-id="dfd4b-173">Refresh the Azure service token</span></span>
- <span data-ttu-id="dfd4b-174">ドキュメント回覧エージェントが Windows サービスとして実行されている間は Azure 認証トークンを **90 日おきに更新する** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-174">Azure authentication tokens must be **refreshed every 90 days** while the Document Routing Agent is running as a Windows service.</span></span> <span data-ttu-id="dfd4b-175">サービス トークンを更新するには、クライアントを起動し、メニュー項目を使用してサインアウトし、再びサインインします。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-175">To refresh the service token, start the client, and then sign out and sign back in by using the menu items.</span></span>

### <a name="disable-shared-printers-for-remote-access"></a><span data-ttu-id="dfd4b-176">リモート アクセス用の共有プリンターを無効にします</span><span class="sxs-lookup"><span data-stu-id="dfd4b-176">Disable shared printers for remote access</span></span>
- <span data-ttu-id="dfd4b-177">Microsoft リモート デスクトップを使用してホスト マシンに接続するときは、**ローカル リソース** タブの **ローカル デバイスとリソース** セクションで、 **プリンター** オプションがオフになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-177">When you connect to the host machine by using Microsoft Remote Desktop, make sure that you clear the **Printers** option in the **Local devices and resources** section on the **Local Resources** tab.</span></span>

### <a name="review-the-event-logs"></a><span data-ttu-id="dfd4b-178">イベント ログを確認</span><span class="sxs-lookup"><span data-stu-id="dfd4b-178">Review the event logs</span></span>
1. <span data-ttu-id="dfd4b-179">ホスト コンピューターで、イベント ビューアーを開始します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-179">On the host machine, start Event Viewer.</span></span>
2. <span data-ttu-id="dfd4b-180">**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-DocumentRouting** でログを確認します。</span><span class="sxs-lookup"><span data-stu-id="dfd4b-180">Review the logs at **Application and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-DocumentRouting**.</span></span>

---
title: ドキュメント回覧エージェントを Windows サービスとして実行する
description: このトピックでは、ドキュメント回覧エージェントによって使用される実行モードの選択に役立つ情報を提供します。
author: RichdiMSFT
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.custom: 191133
ms.assetid: 7adc7228-4360-4a54-8a3e-4d916e727dd2
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: e195c2371430ff44aed23bd1e560a61d23cad151
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754282"
---
# <a name="run-the-document-routing-agent-as-a-windows-service"></a><span data-ttu-id="24def-103">ドキュメント回覧エージェントを Windows サービスとして実行する</span><span class="sxs-lookup"><span data-stu-id="24def-103">Run the Document Routing Agent as a Windows service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24def-104">ドキュメント回覧エージェントには、実行モードを選択できるオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="24def-104">The Document Routing Agent includes an option that lets you select the mode of execution.</span></span> <span data-ttu-id="24def-105">このプロセスは、デスクトップ アプリケーションまたは Microsoft Windows サービスのいずれかとして実行できます。</span><span class="sxs-lookup"><span data-stu-id="24def-105">The process can run as either a desktop application or a Microsoft Windows service.</span></span> <span data-ttu-id="24def-106">アプリケーションは、Windows サービスとして実行されるとき、コンピューターの再起動後に自動的に起動することができます。</span><span class="sxs-lookup"><span data-stu-id="24def-106">When the application runs as a Windows service, it can be started automatically after a computer restart.</span></span> <span data-ttu-id="24def-107">また、特定のユーザー アカウントのセキュリティ コンテキストで実行するように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="24def-107">It can also be configured to run under the security context of a specific user account.</span></span> <span data-ttu-id="24def-108">この機能拡張により、顧客はネットワーク プリント サーバーなどのセキュリティで保護されたドメイン リソースでドキュメント ルート指定エージェントをホストできます。</span><span class="sxs-lookup"><span data-stu-id="24def-108">This enhancement lets customers host the Document Routing Agent on secured domain resources such as network print servers.</span></span>

<span data-ttu-id="24def-109">このトピックでは、正しく実行モードを選択するのに役立つ重要な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="24def-109">This topic provides important information that will help you select the correct execution mode.</span></span>

## <a name="service-applications"></a><span data-ttu-id="24def-110">サービス アプリケーション</span><span class="sxs-lookup"><span data-stu-id="24def-110">Service applications</span></span>
<span data-ttu-id="24def-111">アプリケーションはユーザーがデスクトップ上で連携するプログラムです。</span><span class="sxs-lookup"><span data-stu-id="24def-111">An application is a program that a user interacts with on the desktop.</span></span> <span data-ttu-id="24def-112">サービスは、バックグラウンドで実行され、アクティブなウィンドウを持たないプロセスです。</span><span class="sxs-lookup"><span data-stu-id="24def-112">A service is a process that runs in the background and doesn't have an active window.</span></span> <span data-ttu-id="24def-113">ドキュメント回覧エージェントは現在、両方の実行モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="24def-113">The Document Routing Agent now supports both execution modes.</span></span> <span data-ttu-id="24def-114">他方ではなくそのモードを選択する理由、およびサービスとしてのプロセスの実行に関連するステップを理解しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="24def-114">It's important that you understand why you might select one mode instead of the other and the steps that are involved in running the process as a service.</span></span> <span data-ttu-id="24def-115">Windows サービスの詳細については、[Windows サービス アプリケーションの概要](/dotnet/framework/windows-services/introduction-to-windows-service-applications) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24def-115">For more information about Windows services, see [Introduction to Windows Service Applications](/dotnet/framework/windows-services/introduction-to-windows-service-applications).</span></span> <span data-ttu-id="24def-116">バックグラウンド サービスとしてドキュメント回覧エージェントを実行する主な利点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="24def-116">Here are some of the main benefits of running the Document Routing Agent as a background service:</span></span>

- <span data-ttu-id="24def-117">コンピューターを再起動すると自動的にサービスが開始されるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="24def-117">The service can be configured to start automatically after a computer restart.</span></span> <span data-ttu-id="24def-118">ユーザー操作は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="24def-118">No user intervention is required.</span></span>
- <span data-ttu-id="24def-119">サービスは、バックグラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="24def-119">The service runs in the background.</span></span> <span data-ttu-id="24def-120">通知領域で実行される有効なアプリケーションはありません。</span><span class="sxs-lookup"><span data-stu-id="24def-120">No active application runs in the notification area.</span></span>
- <span data-ttu-id="24def-121">このサービスは、ユーザーがキャッシュされた資格情報を使用してサインインせずに、ドキュメントをルーティングできます。</span><span class="sxs-lookup"><span data-stu-id="24def-121">The service routes documents without requiring that a user sign in by using cached credentials.</span></span>

<span data-ttu-id="24def-122">ドキュメント回覧エージェントを Windows サービスとして実行することには多くの利点がありますが、制限もあります。</span><span class="sxs-lookup"><span data-stu-id="24def-122">Although there are many benefits of running the Document Routing Agent as a Windows service, there are also limitations.</span></span> <span data-ttu-id="24def-123">次のセクションでは、カスタムのページ マージンを必要とする小切手などのドキュメント レポートの処理に影響する問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="24def-123">The next section discusses an issue that affects the handling of document reports, such as checks, that require custom page margins.</span></span>

## <a name="documents-that-require-custom-margins"></a><span data-ttu-id="24def-124">カスタム マージンを要求するドキュメント</span><span class="sxs-lookup"><span data-stu-id="24def-124">Documents that require custom margins</span></span>
<span data-ttu-id="24def-125">ドキュメント回覧エージェントが Windows サービスとして実行されるときは、ユーザー設定の余白を必要とする小切手などのドキュメント レポートをネットワーク プリンターに直接印刷することはできません。</span><span class="sxs-lookup"><span data-stu-id="24def-125">When the Document Routing Agent runs as a Windows service, document reports, such as checks, that require custom margins can't be printed directly to network printers.</span></span> <span data-ttu-id="24def-126">代わりに、このドキュメント回覧エージェントは自動的にこれらのドキュメントをターゲット フォルダーに転送します。</span><span class="sxs-lookup"><span data-stu-id="24def-126">Instead, the Document Routing Agent automatically routes those document to a target folder.</span></span> <span data-ttu-id="24def-127">アプリケーションの **設定** ダイアログ ボックスにある新しいコンフィギュレーション プロパティで、カスタム マージンを必要とするドキュメント レポートの対象となる場所を定義できます。</span><span class="sxs-lookup"><span data-stu-id="24def-127">New configuration properties in the application's **Settings** dialog box let you define the target location for document reports that require custom margins.</span></span>

<span data-ttu-id="24def-128">ドキュメント回覧エージェントは、デスクトップ アプリケーションとして実行されるときは、Adobe Reader の活用する続行して、Finance and Operations で選択されている共有プリンター デバイスにドキュメントをスプールします。</span><span class="sxs-lookup"><span data-stu-id="24def-128">When the Document Routing Agent runs as a desktop application, it continues to take advantage of Adobe Reader to spool the document to the shared printer device that is selected in Finance and Operations.</span></span> <span data-ttu-id="24def-129">カスタムの余白を設定したドキュメントを印刷する必要があるシナリオを処理するには、ドキュメント ルーティング エージェントを複数の場所にインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="24def-129">To handle scenarios where documents that have custom margins must be printed, we recommend that you install the Document Routing Agent in multiple locations.</span></span> <span data-ttu-id="24def-130">デスクトップ アプリケーション モードで実行されるドキュメント ルーティング エージェントでのみ、これらのドキュメントを処理するプリンターをインストールします。</span><span class="sxs-lookup"><span data-stu-id="24def-130">Then install the printers that will handle those documents only on the Document Routing Agents that will run in desktop application mode.</span></span> <span data-ttu-id="24def-131">または、実行後のプロセスを使用してターゲット ディレクトリ内のファイルを取得し適切な方法でそれらを指示します。</span><span class="sxs-lookup"><span data-stu-id="24def-131">Alternatively, use a post-execution process to pick up the files in the target directory and direct them in the appropriate manner.</span></span>

## <a name="install-the-latest-build"></a><span data-ttu-id="24def-132">最新ビルドのインストール</span><span class="sxs-lookup"><span data-stu-id="24def-132">Install the latest build</span></span>
1. <span data-ttu-id="24def-133">現在のドキュメント回覧エージェント構成ファイルのコピーを保存します。</span><span class="sxs-lookup"><span data-stu-id="24def-133">Save a copy of the current Document Routing Agent configuration file.</span></span> <span data-ttu-id="24def-134">このファイルは、C:\\Users\\&lt;UserID&gt;\\AppData\\Local\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing\\Microsoft.Dynamics.AX.Framework.DocumentRouting.config にあります。このパスでは、&lt;UserID&gt;は、ドキュメント ルーティング エージェントがインストールされた Active Directory Domain Services (AD DS) のユーザー名です。</span><span class="sxs-lookup"><span data-stu-id="24def-134">This file is located at C:\\Users\\&lt;UserID&gt;\\AppData\\Local\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing\\Microsoft.Dynamics.AX.Framework.DocumentRouting.config. In this path, &lt;UserID&gt; is the Active Directory Domain Services (AD DS) user name that the Document Routing Agent was installed under.</span></span>
2. <span data-ttu-id="24def-135">ドキュメント回覧エージェントの現在のバージョンをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="24def-135">Uninstall the current version of the Document Routing Agent.</span></span>
3. <span data-ttu-id="24def-136">[ネットワーク印刷を有効にするためにドキュメント回覧エージェントをインストールする](install-document-routing-agent.md)の手順に従って、ドキュメント回覧エージェントの最新バージョンをインストールします。</span><span class="sxs-lookup"><span data-stu-id="24def-136">Install the latest version of the Document Routing Agent by following the instructions in [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="24def-137">この時点でアプリケーションをインストールしますが、まだ実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="24def-137">Although you install the application at this point, don't run it yet.</span></span>

4. <span data-ttu-id="24def-138">手順 1 では、構成ファイルをコピーし、次のディレクトリに貼り付けます。c:\\ProgramData\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing。</span><span class="sxs-lookup"><span data-stu-id="24def-138">Copy the configuration file from step 1, and paste it into the following directory: C:\\ProgramData\\Microsoft\\Microsoft Dynamics 365 for Finance and Operations Document Routing.</span></span> <span data-ttu-id="24def-139">このステップにより、ドキュメント回覧エージェント アプリケーションの新しいバージョンに以前のすべての構成設定が使用されていることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="24def-139">This step helps guarantee that all your previous configuration settings are used for the new version of the Document Routing Agent application.</span></span>
5. <span data-ttu-id="24def-140">ドキュメント回覧エージェントを実行します。</span><span class="sxs-lookup"><span data-stu-id="24def-140">Run the Document Routing Agent.</span></span>
6. <span data-ttu-id="24def-141">Microsoft Azure Active Directory ( Azure AD) または Finance and Operations アプリの資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="24def-141">Sign in by using your Microsoft Azure Active Directory (Azure AD) or your credentials for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="24def-142">適切なメニュー項目をクリックして、設定およびプリンターを表示して確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-142">View and verify your settings and printers by clicking the appropriate menu items.</span></span>

<span data-ttu-id="24def-143">次のセクションでは、Windows サービスの実行モードを選択するための詳細な手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="24def-143">The next section provides detailed instructions for selecting the Windows service execution mode.</span></span>

## <a name="change-the-default-execution-mode"></a><span data-ttu-id="24def-144">既定の実行モードの変更</span><span class="sxs-lookup"><span data-stu-id="24def-144">Change the default execution mode</span></span>
<span data-ttu-id="24def-145">既定では、ドキュメント回覧エージェントはデスクトップ アプリケーションとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="24def-145">By default, the Document Routing Agent runs as a desktop application.</span></span> <span data-ttu-id="24def-146">プロセスを Windows サービスとして実行するには、[[ドキュメント ルーティング エージェントをインストールしてネットワーク プリンタ デバイスを有効にする](install-document-routing-agent.md)] のプロセスに精通していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="24def-146">To run the process as a Windows service, make sure that you're familiar with the process for [installing the Document Routing Agent to enable network printer devices](install-document-routing-agent.md).</span></span> <span data-ttu-id="24def-147">その後次のタスクをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="24def-147">Then complete the following tasks.</span></span>

### <a name="update-the-execution-mode-for-the-document-routing-agent"></a><span data-ttu-id="24def-148">ドキュメント回覧エージェントの実行モードを更新</span><span class="sxs-lookup"><span data-stu-id="24def-148">Update the execution mode for the Document Routing Agent</span></span>
1. <span data-ttu-id="24def-149">デスクトップ アイコンを使用してドキュメント回覧エージェントを起動します。</span><span class="sxs-lookup"><span data-stu-id="24def-149">Start the Document Routing Agent by using the desktop icon.</span></span>
2. <span data-ttu-id="24def-150">**サインイン** オプションを選択し、Azure AD 資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="24def-150">Select the **Sign In** option, and sign in by using your Azure AD credentials.</span></span>
3. <span data-ttu-id="24def-151">リボンで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24def-151">On the ribbon, select **Settings**.</span></span>
4. <span data-ttu-id="24def-152">**Windows Service として実行** オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="24def-152">Enable the **Run as a Windows Service** option.</span></span>
5. <span data-ttu-id="24def-153">ユーザー設定の余白を持つドキュメントに生成される PDF ファイルの対象となるフォルダーを提供します。</span><span class="sxs-lookup"><span data-stu-id="24def-153">Provide a target folder for PDF files that are produced for documents that have custom margins.</span></span>
6. <span data-ttu-id="24def-154">**OK** を選択し、ドキュメント回覧エージェント ウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="24def-154">Select **OK**, and close the Document Routing Agent window.</span></span>

### <a name="configure-and-start-the-windows-service"></a><span data-ttu-id="24def-155">Windows サービスのコンフィギュレーションおよび開始</span><span class="sxs-lookup"><span data-stu-id="24def-155">Configure and start the Windows service</span></span>
1. <span data-ttu-id="24def-156">Windows で、Service Manager を開始します。</span><span class="sxs-lookup"><span data-stu-id="24def-156">In Windows, start Service Manager.</span></span>
2. <span data-ttu-id="24def-157">一覧で、**Microsoft Dynamics 365 for Finance and Operations ドキュメント ルーティング サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24def-157">In the list, select **Microsoft Dynamics 365 for Finance and Operations Document Routing Service**.</span></span>
3. <span data-ttu-id="24def-158">名前を右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24def-158">Right-click the name, and then select **Properties**.</span></span>
4. <span data-ttu-id="24def-159">**ログオン** タブで、**この勘定** オプションを選択し、サービスを実行するために使用される AD DS 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="24def-159">On the **Log On** tab, select the **This account** option, and then supply the AD DS credentials that are used to run the service.</span></span>

    > [!NOTE]
    > <span data-ttu-id="24def-160">選択したアカウントは共有ネットワーク デバイスにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="24def-160">The selected account must have access to the shared network devices.</span></span>
    > <span data-ttu-id="24def-161">Windows サービスを実行するのに使用する Windows ドメイン アカウント (またはローカル コンピューター アカウント) は、ドキュメント回覧エージェントのデスクトップ アプリケーションを開始するアカウントと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="24def-161">The windows domain account ( or local machine account) used to run the windows service must be same as the account that starts the Document Routing Agent desktop app.</span></span>

5. <span data-ttu-id="24def-162">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="24def-162">Select **OK**.</span></span>
6. <span data-ttu-id="24def-163">サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="24def-163">Start the service.</span></span>

<span data-ttu-id="24def-164">ドキュメント回覧エージェントは現在 Windows サービス アプリケーションとして実行されています。</span><span class="sxs-lookup"><span data-stu-id="24def-164">The Document Routing Agent is now running as a Windows service.</span></span>

## <a name="troubleshooting-tips"></a><span data-ttu-id="24def-165">ヒントのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="24def-165">Troubleshooting tips</span></span>
### <a name="verify-the-network-printer-connection"></a><span data-ttu-id="24def-166">ネットワーク プリンターの接続を確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-166">Verify the network printer connection</span></span>
- <span data-ttu-id="24def-167">有効なアカウントにネットワーク プリンターへの十分なアクセス権があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-167">Verify that the active account has enough access rights to the network printer.</span></span>
- <span data-ttu-id="24def-168">メモ帳または別のローカル アプリケーションを使用して、ユーザー アカウントがネットワーク デバイスに正常に印刷できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-168">Verify that the user account can successfully print to the network device by using Notepad or another local application.</span></span>

### <a name="verify-security-roles"></a><span data-ttu-id="24def-169">セキュリティ ロールの確認</span><span class="sxs-lookup"><span data-stu-id="24def-169">Verify security roles</span></span>
- <span data-ttu-id="24def-170">ドキュメント ルート指定クライアントのインストールに使用されるアプリケーション リンクにアクセスするには、ユーザーは **ドキュメント ルート指定クライアント** のセキュリティ ロールの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="24def-170">To access the application links that are used to install the Document Routing Agent, the user must be part of the **Document routing client** security role.</span></span>

### <a name="review-the-service-accounts-access-rights"></a><span data-ttu-id="24def-171">サービス アカウントのアクセス権を確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-171">Review the service account's access rights</span></span>
- <span data-ttu-id="24def-172">ネットワーク デバイスにアクセスできるドメイン アカウントとして **DocumentRoutingService** サービスが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-172">Verify that the **DocumentRoutingService** service is running as a domain account that has access to the network devices.</span></span>

### <a name="refresh-the-azure-service-token"></a><span data-ttu-id="24def-173">Azure サービス トークンを更新</span><span class="sxs-lookup"><span data-stu-id="24def-173">Refresh the Azure service token</span></span>
- <span data-ttu-id="24def-174">ドキュメント回覧エージェントが Windows サービスとして実行されている間は Azure 認証トークンを **90 日おきに更新する** 必要があります。</span><span class="sxs-lookup"><span data-stu-id="24def-174">Azure authentication tokens must be **refreshed every 90 days** while the Document Routing Agent is running as a Windows service.</span></span> <span data-ttu-id="24def-175">サービス トークンを更新するには、クライアントを起動し、メニュー項目を使用してサインアウトし、再びサインインします。</span><span class="sxs-lookup"><span data-stu-id="24def-175">To refresh the service token, start the client, and then sign out and sign back in by using the menu items.</span></span>

### <a name="disable-shared-printers-for-remote-access"></a><span data-ttu-id="24def-176">リモート アクセス用の共有プリンターを無効にします</span><span class="sxs-lookup"><span data-stu-id="24def-176">Disable shared printers for remote access</span></span>
- <span data-ttu-id="24def-177">Microsoft リモート デスクトップを使用してホスト マシンに接続するときは、**ローカル リソース** タブの **ローカル デバイスとリソース** セクションで、 **プリンター** オプションがオフになっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-177">When you connect to the host machine by using Microsoft Remote Desktop, make sure that you clear the **Printers** option in the **Local devices and resources** section on the **Local Resources** tab.</span></span>

### <a name="review-the-event-logs"></a><span data-ttu-id="24def-178">イベント ログを確認</span><span class="sxs-lookup"><span data-stu-id="24def-178">Review the event logs</span></span>
1. <span data-ttu-id="24def-179">ホスト コンピューターで、イベント ビューアーを開始します。</span><span class="sxs-lookup"><span data-stu-id="24def-179">On the host machine, start Event Viewer.</span></span>
2. <span data-ttu-id="24def-180">**アプリケーションとサービス ログ** \> **Microsoft** \> **Dynamics** \> **AX-DocumentRouting** でログを確認します。</span><span class="sxs-lookup"><span data-stu-id="24def-180">Review the logs at **Application and Services Logs** \> **Microsoft** \> **Dynamics** \> **AX-DocumentRouting**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
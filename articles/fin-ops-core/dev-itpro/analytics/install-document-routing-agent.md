---
title: ネットワーク印刷を有効にするためにドキュメント回覧エージェントをインストールする
description: このトピックでは、Microsoft Dynamics 365 Finance の配置用にドキュメント回覧エージェントをインストールして構成する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.custom: 98663
ms.assetid: cd017bfd-2eba-4e8a-ab9b-a0ce393c2108
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85d5ffb2d5f56b2b8edc42c8f274a1834ddbe202
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687441"
---
# <a name="install-the-document-routing-agent-to-enable-network-printing"></a><span data-ttu-id="960c9-103">ネットワーク印刷を有効にするためにドキュメント回覧エージェントをインストールする</span><span class="sxs-lookup"><span data-stu-id="960c9-103">Install the Document Routing Agent to enable network printing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="960c9-104">このトピックでは、ドキュメント回覧エージェント (DRA) をインストールして構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="960c9-104">This topic describes how to install and configure the Document Routing Agent (DRA).</span></span>  <span data-ttu-id="960c9-105">DRA は、ネットワーク印刷シナリオを有効にするのに使用できる、ダウンロード可能なアプリケーションを提供します。</span><span class="sxs-lookup"><span data-stu-id="960c9-105">The DRA is a downloadable application that you can use to enable network printing scenarios.</span></span> <span data-ttu-id="960c9-106">クライアント内管理ページを使用して、特定の会社のためにネットワーク プリンターを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="960c9-106">You can enable network printers for specific companies by using in-client administrative pages.</span></span>

## <a name="preparing-to-install-the-document-routing-agent"></a><span data-ttu-id="960c9-107">ドキュメント回覧エージェントのインストールを準備</span><span class="sxs-lookup"><span data-stu-id="960c9-107">Preparing to install the Document Routing Agent</span></span>

- <span data-ttu-id="960c9-108">Windows 8.1、Windows 10、Microsoft Windows Server 2012 R2、または Microsoft Windows Server 2016 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="960c9-108">Supported on Windows 8.1, Windows 10, Microsoft Windows Server 2012 R2, or Microsoft Windows Server 2016.</span></span>
- <span data-ttu-id="960c9-109">ネットワーク印刷リソースへのアクセスには、Active Directory Domain Services (AD DS) 認証が必要です。</span><span class="sxs-lookup"><span data-stu-id="960c9-109">Access to network printing resources requires Active Directory Domain Services (AD DS) authentication.</span></span>
- <span data-ttu-id="960c9-110">DRA をインストールする場合は、管理者ユーザーとしてログインしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="960c9-110">When installing the DRA, make sure you are logged in as the Admin user.</span></span>
- <span data-ttu-id="960c9-111">DRA を構成するために使用される Microsoft Azure Active Directory (Azure AD) アカウントには、Azure テナントと同じドメインを共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="960c9-111">The Microsoft Azure Active Directory (Azure AD) account that is used to configure the DRA must share the same domain as the Azure tenant.</span></span>
- <span data-ttu-id="960c9-112">DRA には、クライアント上に .NET 4.62 以降と Adobe Acrobat Reader が必要です。</span><span class="sxs-lookup"><span data-stu-id="960c9-112">The DRA requires .NET 4.62 or later and Adobe Acrobat Reader on the client.</span></span>
- <span data-ttu-id="960c9-113">ドキュメントの拡大縮小を防止するために、Adobe クライアントの印刷設定をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="960c9-113">Configure Adobe client print settings to prevent document scaling.</span></span>

<span data-ttu-id="960c9-114">アプリケーションに登録されているネットワーク プリンターは、環境で定義されているすべての法人 (会社とも呼ばれます) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="960c9-114">Network printers that are registered for applications can be used by all legal entities (also known as companies) that are defined in the environment.</span></span> <span data-ttu-id="960c9-115">ネットワーク プリンター設定は会社固有です。</span><span class="sxs-lookup"><span data-stu-id="960c9-115">Network printer settings are company-specific.</span></span> <span data-ttu-id="960c9-116">したがって、管理者はユーザーのアクティブな会社に基づいてアクセスを制限できます。</span><span class="sxs-lookup"><span data-stu-id="960c9-116">Therefore, administrators can restrict access, based on the user's active company.</span></span> <span data-ttu-id="960c9-117">たとえば、有効な会社内のユーザーは、ドキュメント回覧エージェントによって登録されるすべてのネットワーク プリンターへアクセスできる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="960c9-117">For example, users in the active company might have access to all the network printers that are registered by the Document Routing Agent.</span></span> <span data-ttu-id="960c9-118">ただし、別の会社内のユーザーは、アクセスがその会社に対して明示的に有効になるまで、それらのプリンターへアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="960c9-118">However, users in another company won't have access to those printers until access is explicitly enabled for that company.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="960c9-119">重要な概念</span><span class="sxs-lookup"><span data-stu-id="960c9-119">Key concepts</span></span>
<span data-ttu-id="960c9-120">このトピックは、次の作業に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="960c9-120">This topic will help you with the following tasks:</span></span>

- <span data-ttu-id="960c9-121">アプリケーションでネットワーク印刷のサポートに関連する主要なコンポーネントを識別します。</span><span class="sxs-lookup"><span data-stu-id="960c9-121">Identify the key components that are involved in the support for network printing in applications.</span></span>
- <span data-ttu-id="960c9-122">ドキュメント回覧エージェントの機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="960c9-122">Learn about the function of the Document Routing Agent.</span></span>
- <span data-ttu-id="960c9-123">既存のアプリケーションに対して機能するようにドキュメント回覧エージェントをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="960c9-123">Configure the Document Routing Agent to work against an existing application.</span></span>
- <span data-ttu-id="960c9-124">管理ページを使用して、ネットワーク プリンタへのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="960c9-124">Use administration pages to manage access to network printers.</span></span>

## <a name="install-the-document-routing-agent"></a><span data-ttu-id="960c9-125">ドキュメント回覧エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="960c9-125">Install the Document Routing Agent</span></span>
<span data-ttu-id="960c9-126">アプリケーションは、ドキュメント回覧エージェントを使用して、ネットワーク プリンター デバイスへのドキュメントのスプーリングを管理します。</span><span class="sxs-lookup"><span data-stu-id="960c9-126">Applications use the Document Routing Agent to manage the spooling of documents to network printer devices.</span></span> <span data-ttu-id="960c9-127">Web アプリケーションに埋め込まれている直接リンクを使用して、クライアントを取得することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="960c9-127">You can obtain the client by using direct links that are embedded in the web application.</span></span> <span data-ttu-id="960c9-128">アプリケーションをローカル コンピューターにダウンロードするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="960c9-128">Use the following procedure to download the application to your local computer.</span></span> <span data-ttu-id="960c9-129">次に、コンピューターに接続されているローカル プリンターとネットワーク プリンターの両方に、単一配置からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="960c9-129">You will then be able to access both local and network printers that are connected to your computer, from a single deployment.</span></span>

1. <span data-ttu-id="960c9-130">**ネットワーク プリンターの管理** ページを開きます。(**組織管理** &gt; **設定** &gt; **ネットワーク プリンター**)</span><span class="sxs-lookup"><span data-stu-id="960c9-130">Open the **Manage network printers** page (**Organization administration** &gt; **Setup** &gt; **Network printers**).</span></span>
2. <span data-ttu-id="960c9-131">**オプション** タブの、**アプリケーション** グループで、**ドキュメント回覧エージェント インストーラーのダウンロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="960c9-131">On the **Options** tab, in the **Application** group, click **Download document routing agent installer**.</span></span>

    <span data-ttu-id="960c9-132">[![download-document-routing-agent-installer](./media/download-document-routing-agent-installer.png)](./media/download-document-routing-agent-installer.png)</span><span class="sxs-lookup"><span data-stu-id="960c9-132">[![download-document-routing-agent-installer](./media/download-document-routing-agent-installer.png)](./media/download-document-routing-agent-installer.png)</span></span>

3. <span data-ttu-id="960c9-133">インストール プロセスを開始するためにダウンロードしたファイルを実行します。</span><span class="sxs-lookup"><span data-stu-id="960c9-133">Run the downloaded file to begin the installation process.</span></span>
4. <span data-ttu-id="960c9-134">設定プロセスを完了します。</span><span class="sxs-lookup"><span data-stu-id="960c9-134">Complete the setup process.</span></span>

<span data-ttu-id="960c9-135">アプリケーションをインストールした後、アプリケーションのネットワーク プリンターとしてローカル プリンターの登録を開始できます。</span><span class="sxs-lookup"><span data-stu-id="960c9-135">After the application is installed, you can begin to register local printers as network printers for the applications.</span></span>

## <a name="configure-the-document-routing-agent"></a><span data-ttu-id="960c9-136">ドキュメント回覧エージェントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="960c9-136">Configure the Document Routing Agent</span></span>
<span data-ttu-id="960c9-137">処理中のドキュメントをホストする Azure サービスと通信できるように、クライアント アプリケーションを構成するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="960c9-137">Use the following procedure to configure the client application so that it can communicate with the Azure services that host the documents that are in-flight.</span></span>

1. <span data-ttu-id="960c9-138">アプリケーションを実行しているすべてのブラウザー インスタンスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="960c9-138">Close all browser instances that are running the application.</span></span> <span data-ttu-id="960c9-139">これにより、ローカル Azure 認証トークンがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="960c9-139">This resets the local Azure authentication tokens.</span></span>
2. <span data-ttu-id="960c9-140">デスクトップで、ドキュメント回覧エージェントを実行します。</span><span class="sxs-lookup"><span data-stu-id="960c9-140">On your desktop, run the Document Routing Agent.</span></span>
3. <span data-ttu-id="960c9-141">ツール バーで、**設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="960c9-141">On the toolbar, click **Settings**.</span></span>

    <span data-ttu-id="960c9-142">[![the-document-routing-agent-window](./media/the-document-routing-agent-window.png)](./media/the-document-routing-agent-window.png)</span><span class="sxs-lookup"><span data-stu-id="960c9-142">[![the-document-routing-agent-window](./media/the-document-routing-agent-window.png)](./media/the-document-routing-agent-window.png)</span></span>

4. <span data-ttu-id="960c9-143">次の設定を追加します。</span><span class="sxs-lookup"><span data-stu-id="960c9-143">Add the following settings:</span></span>

    - <span data-ttu-id="960c9-144">**アプリケーション ID** - アプリケーション固有の ID で、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="960c9-144">**Application ID** – The ID that is unique to the application and should be entered automatically.</span></span>
    - <span data-ttu-id="960c9-145">**Finance and Operations URL** – アプリケーションのベース URL。</span><span class="sxs-lookup"><span data-stu-id="960c9-145">**Finance and Operations URL** – The base URL of the application.</span></span>
    - <span data-ttu-id="960c9-146">**Azure AD テナント** – Azure AD のドメイン名。</span><span class="sxs-lookup"><span data-stu-id="960c9-146">**Azure AD tenant** – The domain name of the Azure AD.</span></span>

5. <span data-ttu-id="960c9-147">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="960c9-147">Click **OK**.</span></span>
6. <span data-ttu-id="960c9-148">**サインイン** をクリックしてアカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="960c9-148">Click **Sign In** to sign in to your account.</span></span>

    > [!NOTE]
    > <span data-ttu-id="960c9-149">アカウントは、アプリケーションに関連付けられている Azure AD と同じドメインを共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="960c9-149">The account must share the same domain as the Azure AD that is associated with the application.</span></span> <span data-ttu-id="960c9-150">ドキュメント回覧エージェントで、ドキュメントを処理する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="960c9-150">The Document Routing Agent is now ready to process documents.</span></span>

<span data-ttu-id="960c9-151">正常にサインインした後、**プリンター** ボタンがツールバーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="960c9-151">After you've successfully signed in, the **Printers** button becomes available on the toolbar.</span></span>

## <a name="register-network-printers"></a><span data-ttu-id="960c9-152">ネットワーク プリンターの登録</span><span class="sxs-lookup"><span data-stu-id="960c9-152">Register network printers</span></span>
<span data-ttu-id="960c9-153">この手順を実行する前に、ローカル ホスト コンピューターのすべてのネットワーク プリンターをインストールしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="960c9-153">Before you complete this procedure, make sure that you've installed all the network printers on the local host computer.</span></span> <span data-ttu-id="960c9-154">サービス登録にインストールされているすべてのプリンター デバイスは利用可能です。</span><span class="sxs-lookup"><span data-stu-id="960c9-154">All the printer devices that are installed will be available for service registration.</span></span> <span data-ttu-id="960c9-155">アプリケーションで公開するプリンターのみを選択してください。</span><span class="sxs-lookup"><span data-stu-id="960c9-155">Be sure to select only the printers that you want to expose in the applications.</span></span>

1. <span data-ttu-id="960c9-156">ツール バーで、**プリンター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="960c9-156">On the toolbar, click **Printers**.</span></span>
2. <span data-ttu-id="960c9-157">アプリケーションで使用できるようにするプリンターを選択します。</span><span class="sxs-lookup"><span data-stu-id="960c9-157">Select the printers to make available in the applications.</span></span>

    <span data-ttu-id="960c9-158">[![printers-to-add](./media/printers-to-add.png)](./media/printers-to-add.png)</span><span class="sxs-lookup"><span data-stu-id="960c9-158">[![printers-to-add](./media/printers-to-add.png)](./media/printers-to-add.png)</span></span>

3. <span data-ttu-id="960c9-159">プリンターの既定の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="960c9-159">Specify a default name for the printer.</span></span>
4. <span data-ttu-id="960c9-160">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="960c9-160">Click **OK**.</span></span>

<span data-ttu-id="960c9-161">この手順を完了した後、選択したプリンター デバイスはアプリケーションのネットワーク プリンター カタログに登録されます。</span><span class="sxs-lookup"><span data-stu-id="960c9-161">After you've completed this procedure, the selected printer devices are registered in the application's network printer catalog.</span></span> <span data-ttu-id="960c9-162">システム管理者は、アプリケーション内からプリンターへのアクセスを有効にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="960c9-162">System administrators can now enable the printers for access from within the application.</span></span>

## <a name="administer-network-printers"></a><span data-ttu-id="960c9-163">ネットワーク プリンターの管理</span><span class="sxs-lookup"><span data-stu-id="960c9-163">Administer network printers</span></span>
<span data-ttu-id="960c9-164">クライアントのページを使用して、1 つ以上のドキュメント回覧エージェントによって登録されているネットワーク プリンターへのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="960c9-164">Use client pages to manage access to the network printers that have been registered by one or more Document Routing Agents.</span></span> <span data-ttu-id="960c9-165">ネットワーク プリンターは、パスで一意に識別されます。</span><span class="sxs-lookup"><span data-stu-id="960c9-165">Network printers are uniquely identified by their path.</span></span> <span data-ttu-id="960c9-166">したがって、複数のドキュメント回覧エージェントによって登録されている場合でも、プリンターは一度に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="960c9-166">Therefore, printers are listed one time, even if they have been registered by more than one Document Routing Agent.</span></span> <span data-ttu-id="960c9-167">Application Object Server (AOS) のネットワーク プリンターを有効にするには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="960c9-167">Use the following procedure to activate the Application Object Server (AOS) network printers.</span></span>

1. <span data-ttu-id="960c9-168">**ネットワーク プリンターの管理** ページを開きます。(**組織管理** &gt; **設定** &gt; **ネットワーク プリンター**)</span><span class="sxs-lookup"><span data-stu-id="960c9-168">Open the **Manage network printers** page (**Organization administration** &gt; **Setup** &gt; **Network printers**).</span></span>

    <span data-ttu-id="960c9-169">[![manage-network-printers-page](./media/manage-network-printers-page.png)](./media/manage-network-printers-page.png)</span><span class="sxs-lookup"><span data-stu-id="960c9-169">[![manage-network-printers-page](./media/manage-network-printers-page.png)](./media/manage-network-printers-page.png)</span></span>

2. <span data-ttu-id="960c9-170">各ネットワーク プリンターにマップされている既存のエントリを編集します。</span><span class="sxs-lookup"><span data-stu-id="960c9-170">Edit the existing entries that are mapped to each network printer.</span></span> <span data-ttu-id="960c9-171">変更の一環として、接続パスを編集します。</span><span class="sxs-lookup"><span data-stu-id="960c9-171">As part of your changes, edit the connection path.</span></span>
3. <span data-ttu-id="960c9-172">**印刷先** フィールドにプリンタをオプションとして含めるには、**有効** フィールドを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="960c9-172">To include a printer as an option in the **Print Destinations** field, set the **Active** field to **Yes**.</span></span>

<span data-ttu-id="960c9-173">ネットワーク プリンターは、アプリケーションで使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="960c9-173">The network printers can now be used in the application.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="960c9-174">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="960c9-174">Frequently asked questions</span></span>
### <a name="does-the-document-routing-agent-have-to-be-installed-on-each-computer-where-a-user-connects-by-using-a-browser"></a><span data-ttu-id="960c9-175">ドキュメント回覧エージェントは、ユーザーがブラウザーを使い接続する各コンピューターにインストールする必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="960c9-175">Does the Document Routing Agent have to be installed on each computer where a user connects by using a browser?</span></span>

<span data-ttu-id="960c9-176">一連番号</span><span class="sxs-lookup"><span data-stu-id="960c9-176">No.</span></span> <span data-ttu-id="960c9-177">ドキュメント回覧エージェントのクライアント インストールは、プロビジョニングされた環境にアクセスする個人が共有できます。</span><span class="sxs-lookup"><span data-stu-id="960c9-177">Client installations of the Document Routing Agent can be shared by individuals who access the provisioned environment.</span></span> <span data-ttu-id="960c9-178">1 つまたは複数のプリント サーバーに、またはネットワーク プリンターへのアクセス権を持つドメインによってホストされている他のクライアントに、エージェントをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="960c9-178">We recommend that you install agents on one or more Print Servers or other domain-hosted clients that have access to network printers.</span></span>

### <a name="if-the-document-routing-agent-belongs-on-a-network-print-server-why-doesnt-the-client-run-as-a-service"></a><span data-ttu-id="960c9-179">ドキュメント回覧エージェントがネットワーク プリント サーバーに属している場合は、クライアントがサービスとして実行しないのはなぜですか?</span><span class="sxs-lookup"><span data-stu-id="960c9-179">If the Document Routing Agent belongs on a network Print Server, why doesn't the client run as a service?</span></span>

<span data-ttu-id="960c9-180">ドキュメント回覧エージェントは現在、サービスとしてのバックグラウンドでの実行をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="960c9-180">The Document Routing Agent now supports running in the background as a service.</span></span> <span data-ttu-id="960c9-181">クライアントの最新版をダウンロードしたことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="960c9-181">You need to ensure that you have downloaded the latest version of the client.</span></span> <span data-ttu-id="960c9-182">詳細については、[Windows サービスとしてドキュメント回覧エージェントを実行](run-document-routing-agent-as-windows-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="960c9-182">For more information, see [Run the Document Routing Agent as a Windows service](run-document-routing-agent-as-windows-service.md).</span></span>

### <a name="do-i-need-to-update-credentials-or-refresh-azure-authentication-tokens-on-a-recurring-basis"></a><span data-ttu-id="960c9-183">定期的に資格情報を更新するか、Azure 認証トークンを更新する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="960c9-183">Do I need to update credentials or refresh Azure authentication tokens on a recurring basis?</span></span>

<span data-ttu-id="960c9-184">はい。</span><span class="sxs-lookup"><span data-stu-id="960c9-184">Yes.</span></span> <span data-ttu-id="960c9-185">Azure Active Directory トークンは 90 日おきに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="960c9-185">The Azure Active Directory token must be refreshed every 90 days.</span></span> <span data-ttu-id="960c9-186">更新しなかった場合、DRA は認証できなくなり、印刷する指示のアプリケーションを取得できなくなります。</span><span class="sxs-lookup"><span data-stu-id="960c9-186">Failing to do so will prevent the DRA from being able to authenticate and retrieve printing instructions applications.</span></span>

### <a name="is-the-document-routing-agent-supported-on-microsoft-windows-server-2019"></a><span data-ttu-id="960c9-187">ドキュメント回覧エージェントは Microsoft Windows Server 2019 でサポートされていますか?</span><span class="sxs-lookup"><span data-stu-id="960c9-187">Is the Document Routing Agent supported on Microsoft Windows Server 2019?</span></span>

<span data-ttu-id="960c9-188">はい。</span><span class="sxs-lookup"><span data-stu-id="960c9-188">Yes.</span></span> <span data-ttu-id="960c9-189">ドキュメント回覧エージェントは Microsoft Windows Server 2019 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="960c9-189">The Document Routing Agent is supported on Microsoft Windows Server 2019.</span></span>

> [!NOTE]
> <span data-ttu-id="960c9-190">サーバーがバックグラウンド サービスを回避するよう構成されている場合、ドキュメント回覧エージェントのクライアントはサービスとして実行できません。</span><span class="sxs-lookup"><span data-stu-id="960c9-190">If the server is configured to prevent background service, the Document Routing Agent client will not be able to run as a service.</span></span> <span data-ttu-id="960c9-191">詳細については、[Windows サービスとしてドキュメント回覧エージェントを実行](run-document-routing-agent-as-windows-service.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="960c9-191">For more information, see [Run the Document Routing Agent as a Windows service](run-document-routing-agent-as-windows-service.md).</span></span>

### <a name="will-microsoft-add-support-for-microsoft-windows-server-2008-servers"></a><span data-ttu-id="960c9-192">Microsoft は Microsoft Windows Server 2008 サーバーのサポートを追加しますか?</span><span class="sxs-lookup"><span data-stu-id="960c9-192">Will Microsoft add support for Microsoft Windows Server 2008 servers?</span></span>

<span data-ttu-id="960c9-193">いいえ、この時点ではありません。</span><span class="sxs-lookup"><span data-stu-id="960c9-193">No, not at this time.</span></span> <span data-ttu-id="960c9-194">Azure の機能には、Microsoft Windows Server 2012 R2 および Microsoft Windows Server 2016 でのみ使用可能ないくつかの依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="960c9-194">There are several dependencies on Azure capabilities that are available only in Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016.</span></span>

### <a name="does-the-user-who-installs-the-document-routing-agent-have-to-be-part-of-a-finance-and-operations-apps-security-group"></a><span data-ttu-id="960c9-195">ドキュメント回覧エージェントをインストールするユーザーは、Finance and Operations アプリ セキュリティ グループの一部である必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="960c9-195">Does the user who installs the Document Routing Agent have to be part of a Finance and Operations apps security group?</span></span>

<span data-ttu-id="960c9-196">はい。</span><span class="sxs-lookup"><span data-stu-id="960c9-196">Yes.</span></span> <span data-ttu-id="960c9-197">エージェントのインストール リンクにアクセスするには、ユーザーは **ドキュメント ルート指定クライアント** のセキュリティ ロールの一部でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="960c9-197">To access the agent installation links, the user must be part of the **Document routing client** security role.</span></span>

### <a name="how-many-network-printers-can-the-document-routing-agent-support"></a><span data-ttu-id="960c9-198">ドキュメント回覧エージェントはいくつのネットワーク プリンターをサポートできますか。</span><span class="sxs-lookup"><span data-stu-id="960c9-198">How many network printers can the Document Routing Agent support?</span></span>

<span data-ttu-id="960c9-199">サポートされているネットワーク プリンターの数は、法人の数と配置されたネットワーク プリンターの数によって異なります。</span><span class="sxs-lookup"><span data-stu-id="960c9-199">The number of supported network printers depends on the number of legal entities and the number of network printers deployed.</span></span> <span data-ttu-id="960c9-200">50 台のプリンタと 1 つの法人組織がある場合は、単一のドキュメント ルーティング エージェントが負荷を処理できます (高可用性を確保するために複数のドキュメント ルーティング エージェントが必要になります)。</span><span class="sxs-lookup"><span data-stu-id="960c9-200">If you have fifty printers and one legal entity, a single Document Routing Agent can handle the load (although you'd want more than one to ensure high availability).</span></span> <span data-ttu-id="960c9-201">プリンタおよび法人の数が多い場合は、必要となるドキュメント回覧エージェントの数を決定するいくつかのパフォーマンス テストを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="960c9-201">If you have a large number of printers and legal entities, we recommend that you do some performance testing to determine the number of Document Routing Agents that you'll need.</span></span>

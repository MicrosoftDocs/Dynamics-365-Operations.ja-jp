---
title: Azure にカスタム ヘルプを展開
description: このトピックでは、Microsoft Dynamics 365 ヘルプ コンテンツを Azure Web アプリに展開する方法を示す例を紹介します。
author: edupont04
manager: AnnBe
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Operations
ms.openlocfilehash: 51921d205751a27f154229bdd533302140010055
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367018"
---
# <a name="deploy-custom-help-to-azure"></a><span data-ttu-id="72bbd-103">Azure にカスタム ヘルプを展開</span><span class="sxs-lookup"><span data-stu-id="72bbd-103">Deploy custom Help to Azure</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72bbd-104">このトピックでは、コンテンツをホストする Web アプリを設定する手順と、コンテンツを製品内の **ヘルプ** ウィンドウで検出可能にするように検索サービスを設定する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-104">This topic describes the steps for setting up a web app to host your content and for setting up a search service to make the content discoverable by the in-product **Help** pane.</span></span> <span data-ttu-id="72bbd-105">Microsoft Azure Web アプリを設定した後、その Web アプリを使用して、製品内の **ヘルプ** ウィンドウに接続されたコンテンツをホストします。</span><span class="sxs-lookup"><span data-stu-id="72bbd-105">You will set up a Microsoft Azure web app and then use that web app to host content that is connected to the in-product **Help** pane.</span></span>

<span data-ttu-id="72bbd-106">[Azure サブスクリプション](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing) をお持ちでない場合は、このトピックの手順を実行する前にアカウントを作成してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-106">If you don't have an [Azure subscription](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing), create an account before you follow the steps in this topic.</span></span> <span data-ttu-id="72bbd-107">12 か月間は無料のアカウントで開始できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-107">You can start with a free account for 12 months.</span></span> <span data-ttu-id="72bbd-108">詳細については、[今すぐ Azure 無料アカウントを作成する](https://azure.microsoft.com/free/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-108">For more information, see [Create your Azure free account today](https://azure.microsoft.com/free/).</span></span>

## <a name="get-started"></a><span data-ttu-id="72bbd-109">はじめに</span><span class="sxs-lookup"><span data-stu-id="72bbd-109">Get started</span></span>

<span data-ttu-id="72bbd-110">[ヘルプ ウィンドウで使用するコンテンツの準備](preparing-content.md) トピックでは、製品内の **ヘルプ** ウィンドウで使用できるようにヘルプ コンテンツを準備する手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-110">The [Prepare content for use with the Help pane](preparing-content.md) topic describes the steps for preparing Help content so that it can be used with the in-product **Help** pane.</span></span> <span data-ttu-id="72bbd-111">一連の HTML ファイルとそれに相当する JavaScript Object Notation (JSON) ファイルを取得したら、Web アプリと検索サービスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-111">After you have a set of HTML files and their equivalent JavaScript Object Notation (JSON) files, you can set up the web app and the search service.</span></span>

### <a name="process-overview"></a><span data-ttu-id="72bbd-112">プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="72bbd-112">Process overview</span></span>

<span data-ttu-id="72bbd-113">Azure リソースを作成するための一般的なプロセスは、次の手順で構成されます:</span><span class="sxs-lookup"><span data-stu-id="72bbd-113">The general process for creating your Azure resources consists of the following steps:</span></span>

1. <span data-ttu-id="72bbd-114">Azure ポータルで、[リソース グループを作成します](#resgr)。</span><span class="sxs-lookup"><span data-stu-id="72bbd-114">In the Azure portal, [create a resource group](#resgr).</span></span>
2. <span data-ttu-id="72bbd-115">Azure ポータルで、[Web アプリを作成](#webapp)、[ストレージ アカウント](#jsonstorage)、[検索サービス](#searchservice) を作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-115">In the Azure portal, [create a web app](#webapp), [a storage account](#jsonstorage), and [a search service](#searchservice).</span></span>

    - <span data-ttu-id="72bbd-116">Web アプリは、HTML ファイルを格納して提供します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-116">The web app stores and serves HTML files.</span></span> <span data-ttu-id="72bbd-117">HTML ファイルには、ヘルプ コンテンツが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72bbd-117">The HTML files contain your Help content.</span></span>
    - <span data-ttu-id="72bbd-118">ストレージ アカウントは、BLOB コンテナーを使用して JSON ファイルを格納します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-118">The storage account uses a blob container to store JSON files.</span></span> <span data-ttu-id="72bbd-119">JSON ファイルは、JSON 形式に変換された後のヘルプ ファイルであり、検索目的でコンテンツのインデックスを生成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-119">The JSON files are your Help files after they have been converted to JSON format so that they can be used to generate an index of your content for search purposes.</span></span> <span data-ttu-id="72bbd-120">詳細については、[カスタム ヘルプ ツールキット: ConvertHtmlToJson ツール](custom-help-toolkit-ConvertHtmlToJson.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-120">For more information, see [Custom Help Toolkit: The ConvertHtmlToJson tool](custom-help-toolkit-ConvertHtmlToJson.md).</span></span>
    - <span data-ttu-id="72bbd-121">検索サービスは、ヘルプ コンテンツのインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-121">The search service indexes the Help content.</span></span> <span data-ttu-id="72bbd-122">インデックスを使用すると、製品内の **ヘルプ** ウィンドウでコンテンツを検索できるようになります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-122">An index makes your content discoverable by the in-product **Help** pane.</span></span> <span data-ttu-id="72bbd-123">詳細については、[Azure Cognitive Search で基本的なインデックスを作成する](/azure/search/search-what-is-an-index) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-123">For more information, see [Create a basic index in Azure Cognitive Search](/azure/search/search-what-is-an-index).</span></span>

3. <span data-ttu-id="72bbd-124">ファイル転送プロトコル (File Transfer Protocol: FTP) を使用して Web アプリに [HTML ファイルをアップロード](#uploadhtml) します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-124">[Upload HTML files](#uploadhtml) to the web app by using File Transfer Protocol (FTP).</span></span>

    <span data-ttu-id="72bbd-125">この手順を完了すると、コンテンツが作成されたロケールに基づいて、HTML ファイルを関連する言語のサブフォルダーに配置します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-125">When you complete this step, you put the HTML files in the relevant language subfolders, based on the locales that the content was written for.</span></span> <span data-ttu-id="72bbd-126">これらのサブフォルダーに使用する名前の詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-126">For information about the names to use for these subfolders, see [Language and locale descriptors in the product and in Help](language-locale.md).</span></span>

4. <span data-ttu-id="72bbd-127">HTML ファイルの言語サブフォルダーに対応するサブフォルダーで、ストレージ コンテナーの Azure Blob Storage に [JSON ファイルをアップロード](#jsonstorage) します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-127">[Upload JSON files](#jsonstorage) into Azure Blob storage in the storage container, in subfolders that correspond to the language subfolders for the HTML files.</span></span>
5. <span data-ttu-id="72bbd-128">REST アプリケーション プログラミング インターフェイス (API) を使用して、検索サービスにデータ ソース、インデックス、インデクサーが含まれるように、[検索サービスを設定](#searchconfig) します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-128">[Configure the search service](#searchconfig) so that it has a data source, index, and indexer on the search service, by using the REST application programming interface (API).</span></span>

    <span data-ttu-id="72bbd-129">この例では、[Postman](https://www.postman.com/) という名前の API ツールを使用してREST API 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="72bbd-129">In this example, an API tool that is named [Postman](https://www.postman.com/) is used to make the REST API calls.</span></span> <span data-ttu-id="72bbd-130">言語固有のインデックス アナライザーを使用するには、言語固有のインデックスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-130">To use a language-specific index analyzer, you must create language-specific indexes.</span></span>

<span data-ttu-id="72bbd-131">このトピックの残りのセクションでは、Azure アカウントと有効なサブスクリプションを持っていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="72bbd-131">In the remaining sections of this topic, the assumption is that you have an Azure account and a valid subscription.</span></span> <span data-ttu-id="72bbd-132">[Azure サブスクリプション](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing) をお持ちでない場合は、始める前にアカウントを作成してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-132">If you don't have an [Azure subscription](/azure/guides/developer/azure-developer-guide#understanding-accounts-subscriptions-and-billing), create an account before you begin.</span></span> <span data-ttu-id="72bbd-133">12 か月間は無料のアカウントで開始できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-133">You can start with a free account for 12 months.</span></span> <span data-ttu-id="72bbd-134">詳細については、[今すぐ Azure 無料アカウントを作成する](https://azure.microsoft.com/free/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-134">For more information, see [Create your Azure free account today](https://azure.microsoft.com/free/).</span></span>

## <a name="create-a-resource-group"></a><a name="resgr"></a><span data-ttu-id="72bbd-135">リソース グループを作成する</span><span class="sxs-lookup"><span data-stu-id="72bbd-135">Create a resource group</span></span>

<span data-ttu-id="72bbd-136">Web アプリ、検索サービス、ストレージ アカウントをホストするには、最初に 1 つ以上のリソース グループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-136">To host your web app, search service, and storage account, you must first create one or more resource groups.</span></span> <span data-ttu-id="72bbd-137">管理を容易にするために、単一のリソース グループにすべてのリソースを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72bbd-137">We recommend that you create all resources in a single resource group to make management easier.</span></span> <span data-ttu-id="72bbd-138">詳細については、[リソース グループの作成](/azure/azure-resource-manager/management/manage-resource-groups-portal#create-resource-groups) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-138">For more information, see [Create resource groups](/azure/azure-resource-manager/management/manage-resource-groups-portal#create-resource-groups).</span></span>

1. <span data-ttu-id="72bbd-139">[Azure ポータル](https://portal.azure.com/) で、**リソース グループ** を選択し、**追加** を選択して、**MyCustomHelp** などのリソース グループの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-139">In the [Azure portal](https://portal.azure.com/), select **Resource groups**, select **Add**, and then specify a name for the resource group, such as **MyCustomHelp**.</span></span>
2. <span data-ttu-id="72bbd-140">リソース グループの作成を完了するには、**レビュー + 作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-140">Select **Review + Create** to finish creating the resource group.</span></span>

## <a name="create-a-web-app"></a><a name="webapp"></a><span data-ttu-id="72bbd-141">Web アプリの作成</span><span class="sxs-lookup"><span data-stu-id="72bbd-141">Create a web app</span></span>

<span data-ttu-id="72bbd-142">コンテンツをホストするには、Azure で Web アプリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-142">To host your content, you must create a web app in Azure.</span></span> <span data-ttu-id="72bbd-143">詳細については、[Azure で静的 HTML Web アプリを作成する](/azure/app-service/app-service-web-get-started-html) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-143">For more information, see [Create a static HTML web app in Azure](/azure/app-service/app-service-web-get-started-html).</span></span>

### <a name="create-the-web-app"></a><span data-ttu-id="72bbd-144">Web アプリの作成</span><span class="sxs-lookup"><span data-stu-id="72bbd-144">Create the web app</span></span>

1. <span data-ttu-id="72bbd-145">[Azure ポータル](https://portal.azure.com/) で、リソース グループに移動し、**追加**、**Web アプリ** の順に選択して、ランタイム スタックと **MyCustomHelpWebApp** などの Web アプリの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-145">In the [Azure portal](https://portal.azure.com/), go to your resource group, select **Add**, select **Web App**, and then specify the runtime stack and a name for the web app, such as **MyCustomHelpWebApp**.</span></span>

    <span data-ttu-id="72bbd-146">ランタイム スタックとして任意の .Net Core スタックを使用できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-146">You can use any .NET Core stack as the runtime stack.</span></span> <span data-ttu-id="72bbd-147">詳細については、[Azure で ASP.NET Core Web アプリを作成する](/azure/app-service/app-service-web-get-started-dotnet) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-147">For more information, see [Create an ASP.NET Core web app in Azure](/azure/app-service/app-service-web-get-started-dotnet).</span></span>

2. <span data-ttu-id="72bbd-148">展開が完了したら、**リソースに移動** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-148">After the deployment is completed, select **Go to resource**.</span></span>
3. <span data-ttu-id="72bbd-149">ページの左側で、**展開センター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-149">On the left side of the page, select **Deployment Center**.</span></span> <span data-ttu-id="72bbd-150">**手動での展開 (プッシュ/同期)** で、**FTP** を選択してから、**ダッシュボード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-150">Under **Manual Deployment (push/sync)**, select **FTP**, and then select **Dashboard**.</span></span>

    <span data-ttu-id="72bbd-151">*アプリ資格情報* または *ユーザーの資格情報* を使用して、コンテンツを Web アプリ にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-151">You can use either *app credentials* or *user credentials* to upload your content to the web app.</span></span> <span data-ttu-id="72bbd-152">アプリ資格情報を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72bbd-152">We recommend that you use app credentials.</span></span> <span data-ttu-id="72bbd-153">コンテンツをアップロードするには、FTP/FTPS エンドポイント、ユーザー名、パスワードが必要です。</span><span class="sxs-lookup"><span data-stu-id="72bbd-153">To upload your content, you must have the FTP/FTPS endpoint, the user name, and the password.</span></span>

    <span data-ttu-id="72bbd-154">続行する前に、ユーザー名とパスワードを一時的な場所にコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-154">You might want to copy the user name and password to a temporary location before you continue.</span></span> <span data-ttu-id="72bbd-155">また、展開を完了した後に資格情報をリセットすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72bbd-155">Additionally, we recommend that you reset the credentials after you've completed the deployment.</span></span> <span data-ttu-id="72bbd-156">詳細については、[Azure App Service の展開資格情報を設定する](/azure/app-service/deploy-configure-credentials) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-156">For more information, see [Configure deployment credentials for Azure App Service](/azure/app-service/deploy-configure-credentials).</span></span>

<span data-ttu-id="72bbd-157">次に、HTML ファイルを Web アプリに追加します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-157">Next, you will add your HTML files to the web app.</span></span> <span data-ttu-id="72bbd-158">[FileZilla](https://filezilla-project.org/)、[Visual Studio](https://www.visualstudio.com/vs/community/)、[Cyberduck](https://cyberduck.io/)、あるいは [WinSCP](https://winscp.net/index.php) などの FTP クライアントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-158">You can use an FTP client such as [FileZilla](https://filezilla-project.org/), [Visual Studio](https://www.visualstudio.com/vs/community/), [Cyberduck](https://cyberduck.io/), or [WinSCP](https://winscp.net/index.php).</span></span> <span data-ttu-id="72bbd-159">詳細については、[FTP/S を使用してアプリを Azure App Service に展開する](/azure/app-service/deploy-ftp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-159">For more information, see [Deploy your app to Azure App Service using FTP/S](/azure/app-service/deploy-ftp).</span></span>

### <a name="upload-html-files"></a><a name="uploadhtml"></a><span data-ttu-id="72bbd-160">HTML ファイルのアップロード</span><span class="sxs-lookup"><span data-stu-id="72bbd-160">Upload HTML files</span></span>

1. <span data-ttu-id="72bbd-161">使用する FTP クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-161">Open your preferred FTP client.</span></span> <span data-ttu-id="72bbd-162">Web アプリへのファイルのアップロードに関連するベスト プラクティスについては、[FTP/S を使用してアプリを Azure App Service に展開する](/azure/app-service/deploy-ftp) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-162">For information about best practices that are related to uploading files to a web app, see [Deploy your app to Azure App Service using FTP/S](/azure/app-service/deploy-ftp).</span></span>
2. <span data-ttu-id="72bbd-163">ホスト (Web アプリの展開センターからの FTPS エンドポイント値)、ユーザー名、パスワードを入力し、接続します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-163">Enter the host (the FTPS endpoint value from the Deployment Center for the web app), user name, and password, and then connect.</span></span>
3. <span data-ttu-id="72bbd-164">ホストの **/site/wwwroot** の下に、カスタム ヘルプ Web サイトがサポートする必要のある言語ごとの言語フォルダを作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-164">Under **/site/wwwroot** on the host, create a language folder for each language that your custom Help website must support.</span></span> <span data-ttu-id="72bbd-165">HTML ファイルおよびその他の関連ファイルを各言語フォルダーにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="72bbd-165">Upload the HTML files and other associated files to each language folder.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="72bbd-166">クライアントが必要とする言語に対応するフォルダ名を使用してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-166">Remember to use folder names that correspond to the languages that the client expects.</span></span> <span data-ttu-id="72bbd-167">詳細については、[製品およびヘルプの言語およびロケール記述子](language-locale.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-167">For more information, see [Language and locale descriptors in the product and in Help](language-locale.md).</span></span>

<span data-ttu-id="72bbd-168">これで、カスタム ヘルプ Web サイトが Azure に展開され、ブラウザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-168">Your custom Help website has now been deployed to Azure and should be visible in a browser.</span></span>

## <a name="create-a-storage-account"></a><a name="jsonstorage"></a><span data-ttu-id="72bbd-169">ストレージ アカウントを作成する</span><span class="sxs-lookup"><span data-stu-id="72bbd-169">Create a storage account</span></span>

<span data-ttu-id="72bbd-170">次に、BLOB コンテナーを使用して、検索サービスが使用する JSON ファイルを格納するストレージ アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-170">Next, create a storage account that uses a blob container to store the JSON files that the search service will use.</span></span> <span data-ttu-id="72bbd-171">Azure Storage の詳細については、[Azure Storage ドキュメント](/azure/storage/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-171">For more information about Azure Storage, see the [Azure Storage documentation](/azure/storage/).</span></span>

<span data-ttu-id="72bbd-172">カスタム ヘルプ ツールキット の一部である [ConvertHtmlToJson](custom-help-toolkit-ConvertHtmlToJson.md) ツールを使用して、HTML ヘルプ ファイルから JSON ファイルを生成できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-172">You can generate the JSON files from your HTML Help files by using the [ConvertHtmlToJson](custom-help-toolkit-ConvertHtmlToJson.md) tool that is part of the Custom Help Toolkit.</span></span>

1. <span data-ttu-id="72bbd-173">[Azure ポータル](https://portal.azure.com/) で、リソース グループに移動し、**追加**、**ストレージ アカウント** の順に選択して、**mycustomhelpstorage** などのストレージ アカウントの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-173">In the [Azure portal](https://portal.azure.com/), go to your resource group, select **Add**, select **Storage account**, and specify a name for the storage account, such as **mycustomhelpstorage**.</span></span> <span data-ttu-id="72bbd-174">次に、**レビュー + 作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-174">Then select **Review + Create**.</span></span> <span data-ttu-id="72bbd-175">詳細については、[ストレージ アカウントを作成する](/azure/storage/common/storage-account-create#create-a-storage-account) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-175">For more information, see [Create a storage account](/azure/storage/common/storage-account-create#create-a-storage-account).</span></span>
2. <span data-ttu-id="72bbd-176">ストレージアカウントを検証および作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-176">Validate and create the storage account.</span></span>

    <span data-ttu-id="72bbd-177">展開が完了したら、新しいストレージ アカウントがリソース グループの下に一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-177">After the deployment is completed, the new storage account is listed under the resource group.</span></span>

3. <span data-ttu-id="72bbd-178">ストレージ アカウントを選択し、ページの左側の **BLOB サービス** で **コンテナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-178">Select your storage account, and then, on the left side of the page, under **Blob Service**, select **Containers**.</span></span> <span data-ttu-id="72bbd-179">コンテナーを追加し、**mycustomhelpcontainer** などの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-179">Add a container, and specify a name, such as **mycustomhelpcontainer**.</span></span> <span data-ttu-id="72bbd-180">詳細については、[クイックスタート: Azure ポータルで Blob をアップロード、ダウンロード、一覧表示する](/azure/storage/blobs/storage-quickstart-blobs-portal) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-180">For more information, see [Quickstart: Upload, download, and list blobs with the Azure portal](/azure/storage/blobs/storage-quickstart-blobs-portal).</span></span>

<span data-ttu-id="72bbd-181">これで、JSON ファイルをアップロードできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="72bbd-181">You can now upload your JSON files.</span></span> <span data-ttu-id="72bbd-182">使用するフォルダー構造は、ソリューションの言語に一致するように、HTML ファイル用に作成したフォルダ構造と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-182">The folder structure that you use must match the folder structure that you created for the HTML files to match the languages of your solution.</span></span> <span data-ttu-id="72bbd-183">たとえば、Web アプリの **en-US** フォルダーに HTML ファイルがある場合、コンテナーに **en-US** フォルダーを作成し、このフォルダーに en-US JSON ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="72bbd-183">For example, if your web app has HTML files in an **en-US** folder, create an **en-US** folder in the container, and upload the en-US JSON files to this folder.</span></span>

<span data-ttu-id="72bbd-184">JSON ファイルを BLOB コンテナーにアップロードするには、いくつかの方法があります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-184">There are several ways to upload JSON files to the blob container.</span></span> <span data-ttu-id="72bbd-185">ユーザー インターフェイス (UI) を使用する場合、[Azure Storage エクスプローラー](/azure/storage/blobs/storage-quickstart-blobs-storage-explorer) は、Azure Storage を使用してファイル操作を管理できる便利なツールです。</span><span class="sxs-lookup"><span data-stu-id="72bbd-185">If you prefer to use a user interface (UI), [Azure Storage Explorer](/azure/storage/blobs/storage-quickstart-blobs-storage-explorer) is a convenient tool that lets you use Azure Storage to manage file operations.</span></span> <span data-ttu-id="72bbd-186">コマンド ライン オプションを使用する場合、AzCopy を使用できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-186">If you prefer a command-line option, you can use AzCopy.</span></span> <span data-ttu-id="72bbd-187">詳細については、[Windows の AzCopy からデータの転送](/azure/storage/common/storage-use-azcopy) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-187">For more information, see [Transfer data with the AzCopy on Windows](/azure/storage/common/storage-use-azcopy).</span></span>

## <a name="create-a-search-service"></a><a name="searchservice"></a><span data-ttu-id="72bbd-188">検索サービスの作成</span><span class="sxs-lookup"><span data-stu-id="72bbd-188">Create a search service</span></span>

<span data-ttu-id="72bbd-189">次に、コンテンツにインデックスを作成して、製品内の **ヘルプ** ウィンドウで検索できるように、検索サービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-189">Next, create a search service, so that the content can be indexed and is discoverable by the in-product **Help** pane.</span></span> <span data-ttu-id="72bbd-190">詳細については、[Azure Cognitive Search とは?](/azure/search/search-what-is-azure-search) を参照してください</span><span class="sxs-lookup"><span data-stu-id="72bbd-190">For more information, see [What is Azure Cognitive Search?](/azure/search/search-what-is-azure-search)</span></span>

- <span data-ttu-id="72bbd-191">[Azure ポータル](https://portal.azure.com/) で、リソース グループに移動し、**追加**、**Azure Cognitive Search** の順に選択して、**URL** で **mycustomhelpsearch** などのサービスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-191">In the [Azure portal](https://portal.azure.com/), go to your resource group, select **Add**, and select **Azure Cognitive Search**, and then, under **URL**, specify a name for the service, such as **mycustomhelpsearch**.</span></span> <span data-ttu-id="72bbd-192">次に、**レビュー + 作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-192">Then select **Review + Create**.</span></span>

    <span data-ttu-id="72bbd-193">サービスがリソース グループに追加されます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-193">The service is added to the resource group.</span></span>

## <a name="configure-the-search-service"></a><a name="searchconfig"></a><span data-ttu-id="72bbd-194">検索サービスを設定する</span><span class="sxs-lookup"><span data-stu-id="72bbd-194">Configure the search service</span></span>

<span data-ttu-id="72bbd-195">前のセクションでは、検索サービスを作成しました。</span><span class="sxs-lookup"><span data-stu-id="72bbd-195">In the previous section, you created a search service.</span></span> <span data-ttu-id="72bbd-196">このセクションでは、ロケールごとに [データソース](#searchdatasource)、[インデックス](#searchindex)、[インデクサー](#searchindexer) を作成して、それを設定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-196">In this section, you will configure it by creating a [data source](#searchdatasource), an [index](#searchindex), and an [indexer](#searchindexer) for each locale.</span></span> <span data-ttu-id="72bbd-197">これにより、BLOB コンテナーにアップロードした JSON ファイルはインデックスされ、検索可能になります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-197">The JSON files that you uploaded to the blob container will then be indexed and searchable.</span></span> <span data-ttu-id="72bbd-198">次の例では、[Postman](https://www.getpostman.com/) ツールを使用して、いくつかの API 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="72bbd-198">In the examples that follow, the [Postman](https://www.getpostman.com/) tool is used to make several API calls.</span></span> <span data-ttu-id="72bbd-199">ただし、独自のメソッドを使用して、これらの API を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-199">However, you can use your own method to call those APIs.</span></span>

### <a name="create-a-data-source"></a><a name="searchdatasource"></a><span data-ttu-id="72bbd-200">データ ソースを作成する</span><span class="sxs-lookup"><span data-stu-id="72bbd-200">Create a data source</span></span>

1. <span data-ttu-id="72bbd-201">Postman を開いて、新しい POST 要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-201">Open Postman, and create a new POST request.</span></span> <span data-ttu-id="72bbd-202">このツールに慣れていない場合は、[Postman を使用して Azure Cognitive Search REST API の探索](/azure/search/search-get-started-postman.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-202">If you're unfamiliar with this tool, see [Explore Azure Cognitive Search REST APIs using Postman](/azure/search/search-get-started-postman.md).</span></span>
2. <span data-ttu-id="72bbd-203">**リクエスト URL の入力** フィールドで、`https://[AzureSearchServicename].search.windows.net/datasources?api-version=2017-11-11` と入力します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-203">In the **Enter request URL** field, enter `https://[AzureSearchServicename].search.windows.net/datasources?api-version=2017-11-11`.</span></span> <span data-ttu-id="72bbd-204">**\[AzureSearchServicename\]** を、このトピックの [検索サービスの作成](#searchservice) セクションで作成した検索サービスの名前 (例えば、**mycustomhelpsearch**) に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-204">Replace **\[AzureSearchServicename\]** with the name of the search service that you created in the [Create a search service](#searchservice) section of this topic (for example, **mycustomhelpsearch**).</span></span>
3. <span data-ttu-id="72bbd-205">**ヘッダー** タブで、**"Content-type"** を **application/json** に設定し、Azure Cognitive Search サービスからのキーに対して **api-key** を設定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-205">On the **Headers** tab, set **"Content-type"** to **application/json**, and set **api-key** to the key from your Azure Cognitive Search service.</span></span> <span data-ttu-id="72bbd-206">キーは、検索サービスの左側にある **設定** の **アクセス キー** にあります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-206">You can find the key in **Access keys** under **Settings** on the left side of the search service.</span></span>
4. <span data-ttu-id="72bbd-207">**認証** タブで、**タイプ** を **非認証** に設定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-207">In the **Authorization** tab, set **Type** to **No Auth**.</span></span>
5. <span data-ttu-id="72bbd-208">**本文** タブで、次のテキストを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-208">On the **Body** tab, paste the following text.</span></span>

    ```json
    {
        "name" : "[datasourcename]",
        "type" : "azureblob",
        "credentials" :
        {
            "connectionString" : "DefaultEndpointsProtocol=https;AccountName=[StorageAccountName];AccountKey=[key];EndpointSuffix=core.windows.net"
        },
        "container" :
        {
            "name" : "[JSONStorageContainerName]"
        }
    }
    ```

    <span data-ttu-id="72bbd-209">次のパラメータを関連する値に置き換えます:</span><span class="sxs-lookup"><span data-stu-id="72bbd-209">Replace the following parameters with the relevant values:</span></span>

    - <span data-ttu-id="72bbd-210">**\[datasourcename\]** – **mycustomhelpdatasource** などの、データ ソースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-210">**\[datasourcename\]** – Specify a name for the data source, such as **mycustomhelpdatasource**.</span></span>
    - <span data-ttu-id="72bbd-211">**\[StorageAccountName\]** – [ストレージ アカウントの作成](#jsonstorage) セクションで作成したストレージ アカウントの名前 (例えば、**mycustomhelpstorage**) を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-211">**\[StorageAccountName\]** – Specify the name of the storage account that you created in the [Create a storage account](#jsonstorage) section (for example, **mycustomhelpstorage**).</span></span>
    - <span data-ttu-id="72bbd-212">**\[key\]** – ストレージ アカウントのアクセス キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-212">**\[key\]** – Specify the access key for your storage account.</span></span> <span data-ttu-id="72bbd-213">キーは、ストレージ アカウントの左側にある **設定** の **キー** にあります。</span><span class="sxs-lookup"><span data-stu-id="72bbd-213">You can find the key in **Keys** under **Settings** on the left side of the storage account.</span></span>
    - <span data-ttu-id="72bbd-214">**\[JSONStorageContainerName\]** – [ストレージ アカウントの作成](#jsonstorage) セクションで作成した BLOB コンテナー の名前 (例えば、**mycustomhelpcontainer**) を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-214">**\[JSONStorageContainerName\]** – Specify the name of the blob container that you created in the [Create a storage account](#jsonstorage) section (for example, **mycustomhelpcontainer**).</span></span>

6. <span data-ttu-id="72bbd-215">**送信** を選択し、**ステータス** フィールドの値が **201 Created** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-215">Select **Send**, and make sure that the value in the **Status** field is **201 Created**.</span></span>

<span data-ttu-id="72bbd-216">次に、サポートする各ロケールのコンテンツのインデックスを持つように、検索サービスを設定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-216">Next, you will configure the search service so that it has an index of the content for each locale that you want to support.</span></span>

### <a name="create-an-index"></a><a name="searchindex"></a><span data-ttu-id="72bbd-217">インデックスの作成</span><span class="sxs-lookup"><span data-stu-id="72bbd-217">Create an index</span></span>

1. <span data-ttu-id="72bbd-218">Postman で、次のパラメータを持つ新しい POST 要求を作成します:</span><span class="sxs-lookup"><span data-stu-id="72bbd-218">In Postman, create a new POST request that has the following parameters:</span></span>

    - <span data-ttu-id="72bbd-219">**URL**: `https://[AzureSearchServicename].search.windows.net/indexes?api-version=2017-11-11` (**\[AzureSearchServicename\]** を検索サービスの名前に置き換えます。)</span><span class="sxs-lookup"><span data-stu-id="72bbd-219">**URL**: `https://[AzureSearchServicename].search.windows.net/indexes?api-version=2017-11-11` (Replace **\[AzureSearchServicename\]** with the name of your search service.)</span></span>
    - <span data-ttu-id="72bbd-220">**タイプ** (**認証** タブ): **非認証**</span><span class="sxs-lookup"><span data-stu-id="72bbd-220">**Type** (on the **Authorization** tab): **No Auth**</span></span>
    - <span data-ttu-id="72bbd-221">**コンテンツ タイプ** (**ヘッダー** タブ): **application/json**</span><span class="sxs-lookup"><span data-stu-id="72bbd-221">**Content-Type** (on the **Headers** tab): **application/json**</span></span>
    - <span data-ttu-id="72bbd-222">**api-key** (**ヘッダー** タブ): Azure Cognitive Search サービスのキー</span><span class="sxs-lookup"><span data-stu-id="72bbd-222">**api-key** (on the **Headers** tab): The key from your Azure Cognitive Search service</span></span>

2. <span data-ttu-id="72bbd-223">**本文** タブで、次のテキストを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-223">On the **Body** tab, paste the following text.</span></span>

    ```json
    {
        "name" : "[IndexName]",
        "fields": [
            { "name": "id", "type": "Edm.String", "key": true,"searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "title", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true, "analyzer":"[AnalyzerName]" },
            { "name": "description", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true, "analyzer":"[AnalyzerName]" },
            { "name": "ms_search_form", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "ms_search_region", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "ms_locale", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "metadata_storage_path", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "metadata_storage_name", "type": "Edm.String", "searchable": true, "filterable": true, "sortable": true, "facetable": true },
            { "name": "metadata_storage_content_type", "type": "Edm.String", "searchable": true, "filterable": false, "sortable": false, "facetable": false }
        ]
    }
    ```

    <span data-ttu-id="72bbd-224">次のパラメータを関連する値に置き換えます:</span><span class="sxs-lookup"><span data-stu-id="72bbd-224">Replace the following parameters with the relevant values:</span></span>

    - <span data-ttu-id="72bbd-225">**\[IndexName\]** – **indexenus** など、作成するインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-225">**\[IndexName\]** – Specify the name of the index that should be created, such as **indexenus**.</span></span>
    - <span data-ttu-id="72bbd-226">**\[AnalyzerName\]** – **en.microsoft** など、使用する言語アナライザーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-226">**\[AnalyzerName\]** – Specify the name of the language analyzer that should be used, such as **en.microsoft**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72bbd-227">インデックスは、言語固有です。</span><span class="sxs-lookup"><span data-stu-id="72bbd-227">The index is language-specific.</span></span> <span data-ttu-id="72bbd-228">**タイトル** と **説明** フィールドには翻訳が含まれており、対応する言語アナライザーの値を設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="72bbd-228">The **title** and **description** fields contain translations, and it's important that you set the corresponding language analyzer value.</span></span> <span data-ttu-id="72bbd-229">作成するインデックスの言語に基づいて適切な値を使用します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-229">Use an appropriate value, based on the language of the index that you're creating.</span></span> <span data-ttu-id="72bbd-230">言語アナライザーの一覧については、[アナライザー リスト](/azure/search/index-add-language-analyzers#analyzer-list)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-230">For a list of language analyzers, see [Analyzer List](/azure/search/index-add-language-analyzers#analyzer-list).</span></span>

3. <span data-ttu-id="72bbd-231">**送信** を選択し、**ステータス** フィールドが **201 Created** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-231">Select **Send**, and make sure that the **Status** field is set to **201 Created**.</span></span>
4. <span data-ttu-id="72bbd-232">複数の言語用のカスタム ヘルプ コンテンツを用意した場合、これらの手順を繰り返して、言語ごとに固有インデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-232">If you prepared custom Help content for multiple languages, repeat these steps to create a unique index for each language.</span></span>

<span data-ttu-id="72bbd-233">インデックスは、インデクサーによって処理されるまでインデックスではありません。</span><span class="sxs-lookup"><span data-stu-id="72bbd-233">The index isn't an index until it has been processed by an indexer.</span></span> <span data-ttu-id="72bbd-234">リファレンス ブックの目次を考えてみてください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-234">Think of the table of contents in a reference book.</span></span> <span data-ttu-id="72bbd-235">本のさまざまなセクションを見つけるためのページ番号もリストされていなければ、実際には役に立ちません。</span><span class="sxs-lookup"><span data-stu-id="72bbd-235">It would not really be useful unless it also lists the page numbers for where to find the various sections in the book.</span></span> <span data-ttu-id="72bbd-236">同様に、検索サービスのインデクサーは、検索に基づいてインデックスを入力します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-236">Similarly, the indexer for your search service fills in the index, based on a search.</span></span> <span data-ttu-id="72bbd-237">詳細については、[Azure Cognitive Search のインデクサー](/azure/search/search-indexer-overview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-237">For more information, see [Indexers in Azure Cognitive Search](/azure/search/search-indexer-overview).</span></span>

### <a name="create-an-indexer"></a><a name="searchindexer"></a><span data-ttu-id="72bbd-238">インデクサーの作成</span><span class="sxs-lookup"><span data-stu-id="72bbd-238">Create an indexer</span></span>

1. <span data-ttu-id="72bbd-239">Postman で、次のパラメータを持つ新しい POST 要求を作成します:</span><span class="sxs-lookup"><span data-stu-id="72bbd-239">In Postman, create a new POST request that has the following parameters:</span></span>

    - <span data-ttu-id="72bbd-240">**URL**: `https://[AzureSearchServicename].search.windows.net/indexers?api-version=2017-11-11` (**\[AzureSearchServicename\]** を検索サービスの名前に置き換えます。)</span><span class="sxs-lookup"><span data-stu-id="72bbd-240">**URL**: `https://[AzureSearchServicename].search.windows.net/indexers?api-version=2017-11-11` (Replace **\[AzureSearchServicename\]** with the name of your search service.)</span></span>
    - <span data-ttu-id="72bbd-241">**タイプ** (**認証** タブ): **非認証**</span><span class="sxs-lookup"><span data-stu-id="72bbd-241">**Type** (on the **Authorization** tab): **No Auth**</span></span>
    - <span data-ttu-id="72bbd-242">**コンテンツ タイプ** (**ヘッダー** タブ): **application/json**</span><span class="sxs-lookup"><span data-stu-id="72bbd-242">**Content-Type** (on the **Headers** tab): **application/json**</span></span>
    - <span data-ttu-id="72bbd-243">**api-key** (**ヘッダー** タブ): Azure Cognitive Search サービスのキー</span><span class="sxs-lookup"><span data-stu-id="72bbd-243">**api-key** (on the **Headers** tab): The key from your Azure Cognitive Search service</span></span>

2. <span data-ttu-id="72bbd-244">**本文** タブで、次のテキストを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-244">On the **Body** tab, paste the following text.</span></span>

    ```json
    {
        "name" : "[IndexerName]",
        "dataSourceName" : "[DatasourceName]",
        "targetIndexName" : "[IndexName]",
        "schedule" : { "interval" : "PT10H" },
        "parameters" : { "configuration" : { "parsingMode" : "json" } },
        "fieldMappings" : [
            { "sourceFieldName" : "/title", "targetFieldName" : "title" },
            { "sourceFieldName" : "/ms.search.form", "targetFieldName" : "ms_search_form" },
            { "sourceFieldName" : "/ms.search.region", "targetFieldName" : "ms_search_region" },
            { "sourceFieldName" : "/ms.locale", "targetFieldName" : "ms_locale" },
            { "sourceFieldName" : "/description", "targetFieldName" : "description" }
        ]
    }
    ```

    <span data-ttu-id="72bbd-245">次のパラメータを関連する値に置き換えます:</span><span class="sxs-lookup"><span data-stu-id="72bbd-245">Replace the following parameters with the relevant values:</span></span>

    - <span data-ttu-id="72bbd-246">**\[IndexerName\]** – **indexerenus** など、作成するインデクサーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-246">**\[IndexerName\]** – Specify the name of the indexer that should be created, such as **indexerenus**.</span></span>
    - <span data-ttu-id="72bbd-247">**\[DatasourceName\]** – **mycustomhelpdatasource** など、作成したデータ ソースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-247">**\[DatasourceName\]** – Specify the name of the data source that you created, such as **mycustomhelpdatasource**.</span></span>
    - <span data-ttu-id="72bbd-248">**\[IndexName\]** – **indexenus** など、作成したインデックスの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-248">**\[IndexName\]** – Specify the name of the index that you created, such as **indexenus**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72bbd-249">このコンフィギュレーションでは、10 時間ごとに実行するようにスケジュールされたインデクサーを設定します (**"schedule" : { "interval" : "PT10H" }**)。</span><span class="sxs-lookup"><span data-stu-id="72bbd-249">This configuration will set up an indexer that is scheduled to run every 10 hours (**"schedule" : { "interval" : "PT10H" }**).</span></span> <span data-ttu-id="72bbd-250">ただし、間隔は必要に応じて調整できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-250">However, you can adjust the interval as appropriate.</span></span>

3. <span data-ttu-id="72bbd-251">**送信** を選択し、**ステータス** フィールドが **201 Created** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-251">Select **Send**, and make sure that the **Status** field is set to **201 Created**.</span></span>
4. <span data-ttu-id="72bbd-252">複数の言語用のカスタム ヘルプ コンテンツを用意した場合、これらの手順を繰り返して、インデックスごとに固有のインデクサーを作成します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-252">If you prepared custom Help content for multiple languages, repeat these steps to create a unique indexer for each index.</span></span>

> [!NOTE]
> <span data-ttu-id="72bbd-253">インデックスには、インデクサーが実行された後にのみデータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-253">An index will contain data only after its indexer has run.</span></span> <span data-ttu-id="72bbd-254">インデックスをすぐにテストする場合は、インデクサーを手動で実行することができます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-254">You might want to manually run the indexer if you're planning to test the index immediately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72bbd-255">コンテンツを更新する場合は、JSON ファイルを再生成して、保管サービスにアップロードしてください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-255">If you update your content, remember to regenerate the JSON files and upload them to the storage service.</span></span> <span data-ttu-id="72bbd-256">コンテンツを追加する場合は、インデクサーを手動で実行するか、次のスケジュールされた実行を待つことができます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-256">If you add content, you can either manually run the indexers or wait for the next scheduled run.</span></span> <span data-ttu-id="72bbd-257">更新されたコンテンツは、インデクサーが次に実行されるまで検索結果で利用できません。</span><span class="sxs-lookup"><span data-stu-id="72bbd-257">Your updated content won't be available in search results until the next time that the indexers are run.</span></span>

<span data-ttu-id="72bbd-258">オプションで、Postman を使用して検索をテストできます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-258">You can optionally use Postman to test the search.</span></span> <span data-ttu-id="72bbd-259">テストに Postman を使用する方法を示す例については、[JSON ファイルの検索](/azure/search/search-semi-structured-data#6---search-your-json-files) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-259">For an example that shows how to use Postman for testing, see [Search your JSON files](/azure/search/search-semi-structured-data#6---search-your-json-files).</span></span>

## <a name="next-steps"></a><span data-ttu-id="72bbd-260">次のステップ</span><span class="sxs-lookup"><span data-stu-id="72bbd-260">Next steps</span></span>

<span data-ttu-id="72bbd-261">このトピックのすべての手順を完了すると、ヘルプ コンテンツが Azure Web アプリ にアップロードされ、インデックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-261">If you completed all the steps in this topic, your Help content has now been uploaded to an Azure web app, and it has been indexed.</span></span>

<span data-ttu-id="72bbd-262">次の手順では、コンテンツを検出できるように **ヘルプ** ウィンドウを拡張します。</span><span class="sxs-lookup"><span data-stu-id="72bbd-262">The next step is to extend the **Help** pane so that it can detect your content.</span></span> <span data-ttu-id="72bbd-263">このようにして、ユーザーが Dynamics 365 ソリューションの **ヘルプ** ウィンドウを開くと、製品内の **ヘルプ** ウィンドウは、ヘルプへの状況依存リンクを生成できます。</span><span class="sxs-lookup"><span data-stu-id="72bbd-263">In that way, when users open the **Help** pane in your Dynamics 365 solution, the in-product **Help** pane will be able to generate context-sensitive links to your Help.</span></span> <span data-ttu-id="72bbd-264">詳細については、[カスタム ヘルプ Web サイトを ヘルプ ウィンドウに接続する](connect-help-pane.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72bbd-264">For more information, see [Connect a custom Help website to the Help pane](connect-help-pane.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="72bbd-265">参照</span><span class="sxs-lookup"><span data-stu-id="72bbd-265">See also</span></span>

[<span data-ttu-id="72bbd-266">カスタム ヘルプの概要</span><span class="sxs-lookup"><span data-stu-id="72bbd-266">Custom Help overview</span></span>](custom-help-overview.md)  
[<span data-ttu-id="72bbd-267">カスタム ヘルプ ツールキット</span><span class="sxs-lookup"><span data-stu-id="72bbd-267">Custom Help Toolkit</span></span>](custom-help-toolkit.md)  
[<span data-ttu-id="72bbd-268">製品およびヘルプの言語およびロケール記述子</span><span class="sxs-lookup"><span data-stu-id="72bbd-268">Language and locale descriptors in the product and in Help</span></span>](language-locale.md)

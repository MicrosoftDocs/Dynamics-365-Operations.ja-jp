---
title: Warehousing アプリのインストールとコンフィギュレーションの概要
description: このトピックでは、Dynamics 365 for Finance and Operations – Warehousing アプリをインストールおよびコンフィギュレーションする方法について説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysAADClientTable, WHSMobileAppField, WHSMobileAppFieldPriority, WHSRFMenu, WHSRFMenuItem, WHSWorker
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 267694
ms.assetid: d95d43b2-13ff-4189-a71a-3a1fb57d55ed
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: df0bc9ff2405cc2f370ea777a70e005a1ff338a0
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814953"
---
# <a name="install-and-configure-the-warehousing-app-overview"></a><span data-ttu-id="88aa1-103">Warehousing アプリのインストールとコンフィギュレーションの概要</span><span class="sxs-lookup"><span data-stu-id="88aa1-103">Install and configure the Warehousing app overview</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 
> <span data-ttu-id="88aa1-104">このトピックでは、クラウド配置の倉庫管理の構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-104">This topic describes how to configure warehousing for cloud deployments.</span></span> <span data-ttu-id="88aa1-105">オンプレミス配置の倉庫管理の構成方法を検索する場合、[オンプレミス配置の倉庫管理](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-105">If you are looking for how to configure warehousing for on-premises deployments, please see [Warehousing for on-premises deployments](../../dev-itpro/deployment/warehousing-for-on-premise-deployments.md).</span></span>


<span data-ttu-id="88aa1-106">このトピックでは、Dynamics 365 for Finance and Operations – Warehousing アプリをインストールおよびコンフィギュレーションする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-106">This topic describes how to install and configure Dynamics 365 for Finance and Operations – Warehousing app.</span></span>

<span data-ttu-id="88aa1-107">倉庫管理アプリは Google Play ストアおよび Windows ストアで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="88aa1-107">Warehousing app is available on Google Play Store and Windows Store.</span></span> <span data-ttu-id="88aa1-108">Dynamics 365 Supply Chain Management の現在のバージョンでは、このアプリはスタンドアロン コンポーネントとして提供されています。つまり、倉庫のタスクに使用されるデバイスに自己展開することを意味します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-108">For the current version of Dynamics 365 Supply Chain Management, this app is provided as a standalone component, which means self-deployment on devices used for warehouse tasks.</span></span> <span data-ttu-id="88aa1-109">このアプリを使用するには、各デバイスでアプリをダウンロードし、Supply Chain Management 環境に接続するように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-109">In order to use the app, you must download the app on each device and configure it to connect to your Supply Chain Management environment.</span></span> <span data-ttu-id="88aa1-110">このトピックでは、デバイスにアプリをインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-110">This topic describes how to install the app on your devices.</span></span> <span data-ttu-id="88aa1-111">また、Supply Chain Management 環境に接続するようにアプリを設定する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-111">It also explains how to configure the app to connect to your Supply Chain Management environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="88aa1-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="88aa1-112">Prerequisites</span></span>
<span data-ttu-id="88aa1-113">このアプリは Android および Windows オペレーティング システムで使用できます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-113">The app is available on Android and Windows operating systems.</span></span> <span data-ttu-id="88aa1-114">このアプリを使用するには、デバイスに次のサポートされているオペレーティング システムの 1 つがインストールされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-114">To use this app, you must have one of the following supported operating systems installed on your devices.</span></span> <span data-ttu-id="88aa1-115">次のサポートされているバージョンの 1 つである必要もあります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-115">You must also have one of the following supported versions.</span></span> <span data-ttu-id="88aa1-116">ハードウェアとソフトウェアがインストールをサポートする環境であるかどうかを評価するために役に立つ次の表の情報を使用します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-116">Use the information in the following table to evaluate if your hardware and software environment is ready to support the installation.</span></span>

| <span data-ttu-id="88aa1-117">プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="88aa1-117">Platform</span></span>                    | <span data-ttu-id="88aa1-118">バージョン</span><span class="sxs-lookup"><span data-stu-id="88aa1-118">Version</span></span>                                                                                                                                                                     |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88aa1-119">Android</span><span class="sxs-lookup"><span data-stu-id="88aa1-119">Android</span></span>                     | <span data-ttu-id="88aa1-120">4.4、5.0、6.0、7.0、8.0、9.0</span><span class="sxs-lookup"><span data-stu-id="88aa1-120">4.4, 5.0, 6.0, 7.0, 8.0, 9.0</span></span>                                                                                                                                                     |
| <span data-ttu-id="88aa1-121">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="88aa1-121">Windows (UWP)</span></span>               | <span data-ttu-id="88aa1-122">Windows 10 (すべてのバージョン)</span><span class="sxs-lookup"><span data-stu-id="88aa1-122">Windows 10 (all versions)</span></span>                                                                                                                                                   |
| <span data-ttu-id="88aa1-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="88aa1-123">Finance and Operations</span></span> | <span data-ttu-id="88aa1-124">Microsoft Dynamics 365 for Operations、バージョン 1611</span><span class="sxs-lookup"><span data-stu-id="88aa1-124">Microsoft Dynamics 365 for Operations, version 1611</span></span> <br><span data-ttu-id="88aa1-125">または</span><span class="sxs-lookup"><span data-stu-id="88aa1-125">-or-</span></span> <br><span data-ttu-id="88aa1-126">Microsoft Dynamics AX バージョン 7.0/7.0.1 および Microsoft Dynamics AX プラットフォーム更新プログラム 2 (KB 3210014)</span><span class="sxs-lookup"><span data-stu-id="88aa1-126">Microsoft Dynamics AX version 7.0/7.0.1 and Microsoft Dynamics AX platform update 2 with hotfix KB 3210014</span></span> |

## <a name="get-the-app"></a><span data-ttu-id="88aa1-127">アプリの取得</span><span class="sxs-lookup"><span data-stu-id="88aa1-127">Get the app</span></span>
-   <span data-ttu-id="88aa1-128">Windows (UWP)</span><span class="sxs-lookup"><span data-stu-id="88aa1-128">Windows (UWP)</span></span>
     - [<span data-ttu-id="88aa1-129">Windows ストアの Finance and Operations - Warehousing</span><span class="sxs-lookup"><span data-stu-id="88aa1-129">Finance and Operations - Warehousing on the Windows Store</span></span>](https://www.microsoft.com/store/apps/9p1bffd5tstm)
-   <span data-ttu-id="88aa1-130">Android</span><span class="sxs-lookup"><span data-stu-id="88aa1-130">Android</span></span>
    - [<span data-ttu-id="88aa1-131">Google Play ストアの Finance and Operations - Warehousing</span><span class="sxs-lookup"><span data-stu-id="88aa1-131">Finance and Operations - Warehousing on the Google Play Store</span></span>](https://play.google.com/store/apps/details?id=com.Microsoft.Dynamics365forOperationsWarehousing)

> [!NOTE]
> <span data-ttu-id="88aa1-132">Zebra App Gallery が使用されなくなり、倉庫管理アプリはその場所からはダウンロードできなくなります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-132">The Zebra App Gallery has been retired, which means that the Warehousing app will no longer be available for download from that location.</span></span>

## <a name="create-a-web-service-application-in-azure-active-directory"></a><span data-ttu-id="88aa1-133">Azure Active Directory で Web サービス アプリケーションを作成する</span><span class="sxs-lookup"><span data-stu-id="88aa1-133">Create a web service application in Azure Active Directory</span></span>
<span data-ttu-id="88aa1-134">アプリが特定の Supply Chain Management サーバーと対話できるようにするには、Supply Chain Management テナント用の Azure Active Directory に Web サービス アプリケーションを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-134">To enable the app to interact with a specific Supply Chain Management server, you must register a web service application in an Azure Active Directory for the Supply Chain Management tenant.</span></span> <span data-ttu-id="88aa1-135">セキュリティ上の理由から、使用する各デバイス用の Web サービス アプリケーションを作成するようにお勧めします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-135">For security reasons, we recommend that you create a web service application for each device that you use.</span></span> <span data-ttu-id="88aa1-136">Azure Active Directory (Azure AD) に Webサービス アプリケーションを作成するには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="88aa1-136">To create a web service application in Azure Active Directory (Azure AD), complete the following steps:</span></span>

1.  <span data-ttu-id="88aa1-137">Web ブラウザーで、<https://portal.azure.com>に移動します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-137">In a web browser, go to <https://portal.azure.com>.</span></span>
2.  <span data-ttu-id="88aa1-138">Azure サブスクリプションにアクセス可能なユーザーの名前とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-138">Enter the name and password for the user who has access to the Azure subscription.</span></span>
3.  <span data-ttu-id="88aa1-139">Azure ポータルの左のナビゲーション ウィンドウで、**Azure Active Directory** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-139">In Azure Portal, in the left navigation pane, click **Azure Active Directory**.</span></span>

    <span data-ttu-id="88aa1-140">[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-140">[![WMA-01-active-directory-example](./media/WMA-01-active-directory-example.png )](./media/WMA-01-active-directory-example.png)</span></span>

4.  <span data-ttu-id="88aa1-141">Supply Chain Management で使用されている Active Directory のインスタンスであることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-141">Ensure that the Active Directory instance is the one that is used by Supply Chain Management.</span></span>
5.  <span data-ttu-id="88aa1-142">ボックスの一覧で、**アプリの登録** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-142">In the list, click **App registrations**.</span></span> 

    <span data-ttu-id="88aa1-143">[![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-143">[![WMA-02-active-directory-app-registrations](./media/WMA-02-active-directory-app-registrations.png)](./media/WMA-02-active-directory-app-registrations.png)</span></span>

6.  <span data-ttu-id="88aa1-144">上部ウィンドウで、**新しい登録**をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-144">In the top pane, click **New registration**.</span></span> <span data-ttu-id="88aa1-145">**アプリケーションの登録ウィザード**が起動します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-145">The **Register an application wizard** starts.</span></span>
7.  <span data-ttu-id="88aa1-146">アプリケーションの名前を入力し、**この組織ディレクトリのアカウントのみ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-146">Enter a name for the application and select **Accounts in this organizational directory only**.</span></span> <span data-ttu-id="88aa1-147">**登録**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-147">Click **Register**.</span></span>  

    <span data-ttu-id="88aa1-148">[![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-148">[![WMA-03-active-directory-add-application](./media/WMA-03-active-directory-add-application.png)](./media/WMA-03-active-directory-add-application.png)</span></span>

8.  <span data-ttu-id="88aa1-149">新しいアプリの登録が開きます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-149">Your new app registration will open.</span></span> 

    <span data-ttu-id="88aa1-150">[![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-150">[![WMA-04-active-directory-configure-app](./media/WMA-04-active-directory-configure-app.png)](./media/WMA-04-active-directory-configure-app.png)</span></span>

9.  <span data-ttu-id="88aa1-151">後で必要になりますので、**申請 ID** 値を忘れないようにしてください</span><span class="sxs-lookup"><span data-stu-id="88aa1-151">Remember the **Application ID**, you will need it later.</span></span> <span data-ttu-id="88aa1-152">**申請 ID** は後で、**クライアント ID** として参照されます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-152">The **Application ID** will later be referred to as the **Client ID**.</span></span>
10. <span data-ttu-id="88aa1-153">**管理**ウィンドウの**証明書 & シークレット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-153">Click **Certificate & secrets** in the **Manage** pane.</span></span> <span data-ttu-id="88aa1-154">**新しいクライアント シークレット**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-154">Click on **New client secret**.</span></span> 

    <span data-ttu-id="88aa1-155">[![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-155">[![WMA-05-active-directory-create-key](./media/WMA-05-active-directory-create-key.png)](./media/WMA-05-active-directory-create-key.png)</span></span>

11. <span data-ttu-id="88aa1-156">**パスワード** セクションでキーの説明および期間を入力してキーを作成します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-156">Create a key by entering a key description and a duration in the **Passwords** section.</span></span> <span data-ttu-id="88aa1-157">**追加** をクリックし、 キーをコピーします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-157">Click **Add** and copy the key.</span></span> <span data-ttu-id="88aa1-158">このキーは、後で**クライアント シークレット**と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-158">This key will later be referred to as the **Client secret**.</span></span> 

    <span data-ttu-id="88aa1-159">[![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-159">[![WMA-06-active-directory-save-key](./media/WMA-06-active-directory-save-key.png)](./media/WMA-06-active-directory-save-key.png)</span></span>

## <a name="create-and-configure-a-user-account-in-supply-chain-management"></a><span data-ttu-id="88aa1-160">Supply Chain Management でユーザー アカウントを作成および設定する</span><span class="sxs-lookup"><span data-stu-id="88aa1-160">Create and configure a user account in Supply Chain Management</span></span>
<span data-ttu-id="88aa1-161">Supply Chain Management で Azure AD アプリケーションを使用可能にするには、次の構成手順を完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="88aa1-161">To enable Supply Chain Managementto use your Azure AD application, you need to complete the following configuration steps:</span></span>

1.  <span data-ttu-id="88aa1-162">倉庫管理アプリ ユーザー資格情報に対応するユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-162">Create a user that corresponds to the warehousing app user credentials.</span></span>
    1.  <span data-ttu-id="88aa1-163">**システム管理** &gt; **共通** &gt; **ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-163">Go to **System administration** &gt; **Common** &gt; **Users**.</span></span>
    2.  <span data-ttu-id="88aa1-164">新規ユーザーを作成します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-164">Create a new user.</span></span>
    3.  <span data-ttu-id="88aa1-165">次のスクリーンショットに示すとおり、倉庫モバイル デバイス ユーザーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-165">Assign the Warehouse mobile device user, as shown in the following screenshot.</span></span> 
    
        <span data-ttu-id="88aa1-166">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-166">[![wh-09-add-user-security-role](./media/wh-09-add-user-security-role.png)](./media/wh-09-add-user-security-role.png)</span></span>

2.  <span data-ttu-id="88aa1-167">Azure Active Directory アプリケーションと倉庫保管アプリ ユーザーを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-167">Associate your Azure Active Directory application with the warehousing app user.</span></span>
    1.  <span data-ttu-id="88aa1-168">Supply Chain Management で、**システム管理** &gt; **設定** &gt; **Azure Active Directory アプリケーション**に移動します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-168">In Supply Chain Management, go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
    2.  <span data-ttu-id="88aa1-169">新しい行を作成します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-169">Create a new line.</span></span>
    3.  <span data-ttu-id="88aa1-170">**クライアント ID** (前のセクションで取得したもの) を入力し、名前を設定し、以前に作成したユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-170">Enter the **Client ID** (obtained in the last section), give it a name, and select the previously created user.</span></span> <span data-ttu-id="88aa1-171">Supply Chain Management へのアクセスを紛失した場合に備えて、このページから簡単に削除できるように、すべてのデバイスにタグを付けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-171">We recommend that you tag all your devices so that you can easily remove their access to Supply Chain Management from this page in case they are lost.</span></span> 
    
        <span data-ttu-id="88aa1-172">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-172">[![wh-10-ad-applications-form](./media/wh-10-ad-applications-form.png)](./media/wh-10-ad-applications-form.png)</span></span>

## <a name="configure-the-application"></a><span data-ttu-id="88aa1-173">アプリケーションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="88aa1-173">Configure the application</span></span>
<span data-ttu-id="88aa1-174">Azure AD アプリケーションを使用して Supply Chain Management サーバーに接続するには、デバイス上でアプリをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-174">You must configure the app on the device to connect to the Supply Chain Management server through the Azure AD application.</span></span> <span data-ttu-id="88aa1-175">それには、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-175">To do this, complete the following steps.</span></span>

1.  <span data-ttu-id="88aa1-176">アプリで、**接続設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-176">In the app, go to **Connection settings**.</span></span>
2.  <span data-ttu-id="88aa1-177">**デモ モード** フィールドをクリアします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-177">Clear the **Demo mode** field.</span></span> <br>

    <span data-ttu-id="88aa1-178">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-178">[![wh-11-app-connection-settings-demo-mode](./media/wh-11-app-connection-settings-demo-mode-169x300.png)](./media/wh-11-app-connection-settings-demo-mode.png)</span></span>

3.  <span data-ttu-id="88aa1-179">次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-179">Enter the following information:</span></span> 
    + <span data-ttu-id="88aa1-180">**Azure Active Directory クライアント ID** - クライアント ID は「Active Directory に Web サービス アプリケーションを作成する」のステップ 9 で取得します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-180">**Azure Active directory client ID** - The client ID is obtained in step 9 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="88aa1-181">**Azure Active Directory クライアント シークレット** - クライアント シークレットは「Active Directory に Web サービス アプリケーションを作成する」のステップ 11 で取得します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-181">**Azure Active directory client secret** - The client secret is obtained in step 11 in "Create a web service application in Active Directory".</span></span> 
    + <span data-ttu-id="88aa1-182">**Azure Active Directory リソース** - Azure AD Directory リソースは Supply Chain Management のルート URL を示します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-182">**Azure Active directory resource** - The Azure AD directory resource depicts the Supply Chain Managementroot URL.</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="88aa1-183">スラッシュ (/) でこのフィールドを終了しないでください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-183">Do not end this field with a forward slash character (/).</span></span> 

    + <span data-ttu-id="88aa1-184">**Azure Active directory テナント** - Supply Chain Management サーバーで使用される Azure AD Directory のテナント: `https://login.windows.net/your-AD-tenant-ID`。</span><span class="sxs-lookup"><span data-stu-id="88aa1-184">**Azure Active directory tenant** - The Azure AD directory tenant used with the Supply Chain Management server: `https://login.windows.net/your-AD-tenant-ID`.</span></span> <span data-ttu-id="88aa1-185">例: `https://login.windows.net/contosooperations.onmicrosoft.com.`</span><span class="sxs-lookup"><span data-stu-id="88aa1-185">For example: `https://login.windows.net/contosooperations.onmicrosoft.com.`</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="88aa1-186">スラッシュ (/) でこのフィールドを終了しないでください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-186">Do not end this field with a forward slash character (/).</span></span> 
    
    + <span data-ttu-id="88aa1-187">**会社** - Supply Chain Management に、アプリケーションが接続する法的エンティティを入力します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-187">**Company** - Enter the legal entity in Supply Chain Management to which you want the application to connect.</span></span> <br>
    
    <span data-ttu-id="88aa1-188">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-188">[![wh-12-app-connection-settings](./media/wh-12-app-connection-settings-169x300.png)](./media/wh-12-app-connection-settings.png)</span></span>

4.  <span data-ttu-id="88aa1-189">アプリケーションの左上隅にある **戻る** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-189">Select the **Back** button in the top-left corner of the application.</span></span> <span data-ttu-id="88aa1-190">アプリケーションは Supply Chain Management サーバーに接続し、倉庫作業者のログイン画面が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-190">The application will now connect to your Supply Chain Management server and the log-in screen for the warehouse worker will display.</span></span>

    <span data-ttu-id="88aa1-191">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span><span class="sxs-lookup"><span data-stu-id="88aa1-191">[![wh-13-log-in-screen](./media/wh-13-log-in-screen-180x300.png)](./media/wh-13-log-in-screen.png)</span></span>

<span data-ttu-id="88aa1-192">モバイル デバイスのカメラを使用してバーコードをスキャンするために倉庫管理アプリを設定する方法の詳細については、[Dynamics 365 for Finance and Operations - Warehousing アプリでカメラを使用してバーコードをスキャンする](scan-bar-codes-using-a-camera.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-192">For information on how to set up the Warehousing app to scan bar codes using a camera on a mobile device, see [Scan bar codes using a camera in Dynamics 365 for Finance and Operations - Warehousing app](scan-bar-codes-using-a-camera.md).</span></span>

## <a name="remove-access-for-a-device"></a><span data-ttu-id="88aa1-193">デバイスへのアクセスを削除する</span><span class="sxs-lookup"><span data-stu-id="88aa1-193">Remove access for a device</span></span>
<span data-ttu-id="88aa1-194">デバイスの紛失またはセキュリティが侵害された場合、デバイスの Supply Chain Management へのアクセスを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88aa1-194">In case of a lost or compromised device, you must remove access to Supply Chain Management for the device.</span></span> <span data-ttu-id="88aa1-195">次の手順では、アクセスを削除するための推奨プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-195">The following steps describe the recommended process to remove access.</span></span>

1.  <span data-ttu-id="88aa1-196">**システム管理** &gt; **設定** &gt; **Azure Active Directory アプリケーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-196">Go to **System administration** &gt; **Setup** &gt; **Azure Active Directory applications**.</span></span>
2.  <span data-ttu-id="88aa1-197">アクセスを削除するデバイスに対応する行を削除します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-197">Delete the line that corresponds to the device to which you want to remove access.</span></span> <span data-ttu-id="88aa1-198">後で必要になりますので、削除したデバイスに使用されている**クライアント ID** を忘れないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="88aa1-198">Remember the **Client ID** used for the removed device, you will need it later.</span></span>
3.  <span data-ttu-id="88aa1-199"><https://portal.azure.com>で Azure ポータルにログインします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-199">Sign in to the Azure portal at <https://portal.azure.com>.</span></span>
4.  <span data-ttu-id="88aa1-200">左側のメニューにある **Active Directory** アイコンをクリックし、適切なディレクトリであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-200">Click the **Active Directory** icon on the left menu, and ensure that you are in the correct directory.</span></span>
5.  <span data-ttu-id="88aa1-201">ボックスの一覧で、**アプリの登録** をクリックし、構成したいアプリケーションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-201">In the list, click **App registrations**, and then click the application that you want to configure.</span></span> <span data-ttu-id="88aa1-202">コンフィギュレーション情報を含む**設定**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88aa1-202">The **Settings** page will appear with configuration information.</span></span>
6.  <span data-ttu-id="88aa1-203">アプリケーションの**クライアント ID** がこのセクションのステップ 2と同じであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88aa1-203">Ensure that the **Client ID** of the application is the same as in step 2 in this section.</span></span>
7.  <span data-ttu-id="88aa1-204">上部ウィンドウの **削除** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-204">Click the **Delete** button in the top pane.</span></span>
8.  <span data-ttu-id="88aa1-205">確認メッセージで **はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88aa1-205">Click **Yes** in the confirmation message.</span></span>

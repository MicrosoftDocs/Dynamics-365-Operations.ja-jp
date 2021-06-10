---
title: Retail ハードウェア ステーションのコンフィギュレーションとインストール
description: このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。 また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。
author: jashanno
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailHardwareStation
audience: IT Pro
ms.reviewer: josaw
ms.custom: 27161
ms.assetid: eb164a9d-5538-4b6f-81ad-87e05d92eca5
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 5d2203ce32602bbd197829c26e293d9a0ebb7ec4
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022641"
---
# <a name="configure-and-install-retail-hardware-station"></a><span data-ttu-id="8755b-104">Retail ハードウェア ステーションのコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="8755b-104">Configure and install Retail hardware station</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8755b-105">このトピックでは、セルフサービス機能を使用してレガシ Commerce ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8755b-105">This topic explains how to configure, download, and install the legacy Commerce hardware station by using self-service functionality.</span></span> <span data-ttu-id="8755b-106">シールされたセルフサービス インストーラーの詳細については、[シールされた Commerce セルフサービス コンポーネントの一括配置](dev-itpro/Enhanced-Mass-Deployment.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8755b-106">For more information about sealed self-service installers, see [Mass deployment of sealed Commerce self-service components](dev-itpro/Enhanced-Mass-Deployment.md).</span></span> <span data-ttu-id="8755b-107">また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="8755b-107">It also explains how to uninstall Retail hardware station.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8755b-108">このコンポーネントはサーバー証明書を利用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8755b-108">It is critical to note that this component utilizes a server certificate.</span></span> <span data-ttu-id="8755b-109">有効期限に対してサーバー証明書を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-109">Server certificates must be managed for expiration.</span></span> <span data-ttu-id="8755b-110">既定では、証明書は 1 つの暦年 (365 日) で期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="8755b-110">By default, a certificate expires in one calendar year (365 days).</span></span>

## <a name="download-retail-hardware-station-by-using-self-service"></a><span data-ttu-id="8755b-111">セルフサービスを使い、Retail ハードウェア ステーションをダウンロード</span><span class="sxs-lookup"><span data-stu-id="8755b-111">Download Retail hardware station by using self-service</span></span>

### <a name="configure-a-new-retail-hardware-station"></a><span data-ttu-id="8755b-112">新しい Retail Hardware Station のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8755b-112">Configure a new Retail hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="8755b-113">Retail (初回リリース) のアップグレードされていないバージョンである 2016 年 2 月を実行している場合は、手順 6 はスキップします。</span><span class="sxs-lookup"><span data-stu-id="8755b-113">If you're running the February 2016, non-upgraded version of Retail (Initial release), skip step 6.</span></span>

1. <span data-ttu-id="8755b-114">Azure AD 証明書を使用して、Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8755b-114">Use your Azure AD credentials to sign in to the Retail trial.</span></span>
2. <span data-ttu-id="8755b-115">**ようこそ** ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8755b-115">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="8755b-116">**すべての小売店舗** ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-116">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="8755b-117">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-117">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-118">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="8755b-118">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="8755b-119">**小売店舗詳細** ページや、**ハードウェア ステーション** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-119">On the **Retail store details** page, on the **Hardware stations** FastTab, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-120">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="8755b-120">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="8755b-121">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="8755b-121">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="8755b-122">**ハードウェア ステーション タイプ** フィールドで、**共有** を選択して、このハードウェア ステーションが Internet Information Services (IIS)、外部の販売時点管理 (POS) システムによって使用されるインストール済みのハードウェア ステーションであることを示します。</span><span class="sxs-lookup"><span data-stu-id="8755b-122">In the **Hardware station type** field, select **Shared** to indicate that this hardware station is an Internet Information Services (IIS), installed hardware station that will be used by external point of sale (POS) systems.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-123">値 **Shared** は、インストールが真に共有されているハードウェア ステーションのインストールであり、HTTPS 通信を介して機能することを示します。</span><span class="sxs-lookup"><span data-stu-id="8755b-123">The value **Shared** signifies that the installation is a truly shared hardware station installation, and that it works through HTTPS communication.</span></span> <span data-ttu-id="8755b-124">対照的に、**専用** という値はハードウェア ステーションが Modern POS の一部であり、プロセス間通信を通じて機能していることを示します。</span><span class="sxs-lookup"><span data-stu-id="8755b-124">By contrast, the value **Dedicated** signifies that the hardware station is a part of Modern POS, and that it works through inter-process communication.</span></span>

6. <span data-ttu-id="8755b-125">ハードウェア ステーションのプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-125">Select a hardware station profile.</span></span>

7. <span data-ttu-id="8755b-126">Retail ハードウェア ステーションをインストールするコンピュータのホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-126">Enter the host name of the computer that you're installing Retail hardware station on.</span></span> <span data-ttu-id="8755b-127">また、商業口座情報のコンピューターに関連付けられている電子決済 (EFT) ターミナル ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-127">Additionally, enter the electronic funds transfer (EFT) terminal ID that is associated with that computer for merchant account information.</span></span>

8. <span data-ttu-id="8755b-128">一括配置を使用して構成ファイルまたは初期インストールを活用するには、次のセクションの詳細説明にあるように、インストール中に使用する証明書の拇印を入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-128">To utilize the configuration file or initial installation using mass deployment, enter the certificate thumbprint that is to be used during the installation that's detailed in the next section.</span></span>

### <a name="download-the-retail-hardware-station-installer"></a><span data-ttu-id="8755b-129">Retail ハードウェア ステーション インストーラーをダウンロード</span><span class="sxs-lookup"><span data-stu-id="8755b-129">Download the Retail hardware station installer</span></span>

1. <span data-ttu-id="8755b-130">Azure AD 資格情報を使用して、Retail Headquarters または Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="8755b-130">Use your Azure AD credentials to sign in to the Retail headquarters or Retail trial.</span></span>
2. <span data-ttu-id="8755b-131">**ようこそ** ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8755b-131">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="8755b-132">**すべての小売店舗** ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-132">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="8755b-133">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-133">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-134">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="8755b-134">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="8755b-135">**小売店舗詳細** ページで、**ハードウェア ステーション** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-135">On the **Retail store details** page, select the **Hardware stations** FastTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-136">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="8755b-136">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="8755b-137">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="8755b-137">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="8755b-138">ダウンロードするハードウェア ステーションを選択し、**ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-138">Select the hardware station to download, and then select **Download**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="8755b-139">ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-139">Browsers might block the download pop-up that is generated.</span></span> <span data-ttu-id="8755b-140">**1 回許可** または **このサイトのオプション** &gt; **常に許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-140">You must select either **Allow once** or **Options for this site** &gt; **Always allow**.</span></span> <span data-ttu-id="8755b-141">その後、再度 **ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-141">Then select **Download** again.</span></span>

6. <span data-ttu-id="8755b-142">Internet Explorer ウィンドウの下部に表示される通知バーで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-142">On the Notification bar that appears at the bottom of the Internet Explorer window, select **Save**.</span></span> <span data-ttu-id="8755b-143">(通知バーは、他のブラウザでは別の場所に表示される場合があります。)</span><span class="sxs-lookup"><span data-stu-id="8755b-143">(The Notification bar might appear in a different place in other browsers.)</span></span>
7. <span data-ttu-id="8755b-144">一括配置またはコマンド ラインからの配置に必要な場合は、構成ファイルのダウンロードに対して上記の手順を繰り返します。これは、選択した **ダウンロード** ボタンの横にあるボタンです。</span><span class="sxs-lookup"><span data-stu-id="8755b-144">If needed for mass deployment or command line deployment, repeat the above steps for the configuration file download, which is a button next to the **Download** button that you previously selected.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="8755b-145">ダウンロードした構成ファイル名が、インストーラーのベース ファイル名と同じでない場合は、XML 構成ファイルを同じベース名に変更するか、コマンド ラインを使用してインストーラーを実行し、構成ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="8755b-145">If the configuration file downloaded does not have the same base file name as the installer, either rename the XML configuration file to be the same base name or run the installer using the command line to specify the configuration file.</span></span>
    > - <span data-ttu-id="8755b-146">Commerce ハードウェア ステーションのインストールには、構成ファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="8755b-146">Note that the configuration file is not required for the installation of Commerce hardware station.</span></span>

8. <span data-ttu-id="8755b-147">ファイルを保存したら、インストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="8755b-147">After the files have been saved, run the installer.</span></span> <span data-ttu-id="8755b-148">(この手順はブラウザによって異なる場合があります。)</span><span class="sxs-lookup"><span data-stu-id="8755b-148">(This step might differ depending on your browser.)</span></span>

### <a name="run-the-installer"></a><span data-ttu-id="8755b-149">インストーラーを実行</span><span class="sxs-lookup"><span data-stu-id="8755b-149">Run the installer</span></span>

> [!NOTE]
> <span data-ttu-id="8755b-150">Retail ハードウェア ステーション インストーラーを実行する前に、すべての[システム要件](../fin-ops-core/fin-ops/get-started/system-requirements.md)が満たされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="8755b-150">Before you run the Retail hardware station installer, make sure that all [system requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md) are met.</span></span>

<span data-ttu-id="8755b-151">Retail ハードウェア ステーション インストーラーは、まず関連付けられているファイルを抽出し、インストールを開始します。</span><span class="sxs-lookup"><span data-stu-id="8755b-151">The Retail hardware station installer first extracts the associated files and then begins the installation.</span></span>

1. <span data-ttu-id="8755b-152">インストーラーは、すべての前提条件が満たされていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="8755b-152">The installer validates that all prerequisites are met.</span></span> <span data-ttu-id="8755b-153">サイドローディング キーが必要な場合は、インストーラーがそれを要求します。</span><span class="sxs-lookup"><span data-stu-id="8755b-153">If a sideloading key is required, the installer requests it.</span></span> <span data-ttu-id="8755b-154">このキーは、各デバイスの **一般** の下にある **デバイス** ページにあります。</span><span class="sxs-lookup"><span data-stu-id="8755b-154">This key is found on the **Devices** page for each device, under **General**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="8755b-155">システムの再起動が必要な場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="8755b-155">If a system restart is required, the installer informs you of this requirement but can continue the installation.</span></span>
    > - <span data-ttu-id="8755b-156">小売販売時点管理の Object Linking and Embedding (OPOS) 標準に基づいたハードウェアを使用する前に、OPOS コモン コントロール オブジェクトをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-156">Before you can use hardware that is based on the Object Linking and Embedding for Retail Point of Sale (OPOS) standard, the OPOS Common Control Objects must be installed.</span></span> <span data-ttu-id="8755b-157">インストールされていない場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="8755b-157">If they aren't installed, the installer informs you of this requirement but can continue the installation.</span></span>

2. <span data-ttu-id="8755b-158">Retail Server URL を入力し (たとえば、`https://MyCompanyNameret.axcloud.dynamics.com/Commerce`)、**次** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-158">Enter the Retail Server URL (for example, `https://MyCompanyNameret.axcloud.dynamics.com/Commerce`), and then select **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-159">Retail Server の URL は **小売店舗詳細** ページ上の **ハードウェア ステーション** クイック タブの最上部で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="8755b-159">You can find the Retail Server URL at the top of the **Hardware stations** FastTab on the **Retail store details** page.</span></span>

3. <span data-ttu-id="8755b-160">HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-160">Select a valid Secure Sockets Layer (SSL) certificate to use for HTTPS communication.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-161">証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-161">The certificate must use private key storage, and server authentication must be listed in the enhanced key usage property.</span></span> <span data-ttu-id="8755b-162">また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8755b-162">Additionally, the certificate must be trusted locally, and it can't be expired.</span></span> <span data-ttu-id="8755b-163">ローカル コンピューターの個人用証明書格納場所に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-163">It must be stored in the personal certificate store location on the local computer.</span></span>

4. <span data-ttu-id="8755b-164">次のページでは、IIS アプリケーション プールで使用する必要があるユーザーを要求します。</span><span class="sxs-lookup"><span data-stu-id="8755b-164">The next page requests the user that should be used for the IIS application pool.</span></span> <span data-ttu-id="8755b-165">バージョン 1611 以降の既定では、インストーラーが自動的にサービス アカウントを作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8755b-165">By default in version 1611 and later, the installer can automatically create and use a service account.</span></span> <span data-ttu-id="8755b-166">ドメインを使用している場合や特定のコントロールが必要な場合は、チェックボックスをオフにして、アプリケーション プールが実行するユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-166">If you're on a domain or require more specific controls, clear the check box, and then enter the user name and password that the application pool should run under.</span></span>
5. <span data-ttu-id="8755b-167">使用する HTTPS ポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-167">Enter the HTTPS port to use.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="8755b-168">Retail で HTTPS ポートを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="8755b-168">You can find the HTTPS port in Retail.</span></span> <span data-ttu-id="8755b-169">(このトピックで前述したコンフィギュレーションの指示を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="8755b-169">(See the configuration instructions earlier in this topic).</span></span>
    > - <span data-ttu-id="8755b-170">インストーラーは自動的にホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-170">The installer automatically enters the host name.</span></span> <span data-ttu-id="8755b-171">何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更できます。</span><span class="sxs-lookup"><span data-stu-id="8755b-171">If, for any reason, you must change the host name for the installation, you can change it here.</span></span> <span data-ttu-id="8755b-172">ホスト名はシステムの完全修飾ドメイン名 (FQDN) でなければなりません。また、選択したハードウェア ステーション エントリの **ホスト名** フィールドに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-172">The host name must be the fully-qualified domain name (FQDN) of the system, and it must be entered in the **Host name** field for the selected hardware station entry.</span></span>

6. <span data-ttu-id="8755b-173">インストーラーは Retail ハードウェア ステーションをインストールし、インストールが成功したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8755b-173">The installer installs Retail hardware station and then indicates whether the installation was successful.</span></span>
7. <span data-ttu-id="8755b-174">インストールが完了したら、支払商社情報のインストール ツールが起動する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-174">When the installation is completed, the Install merchant information tool may start.</span></span> <span data-ttu-id="8755b-175">このインストーラーは、環境に接続し、選択したハードウェア ステーションの販売者の口座情報 (EFT IDなど) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="8755b-175">This installer connects to the environment and installs the merchant account information (such as the EFT ID) for the selected hardware station.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="8755b-176">インストールされているハードウェア ステーションが支払に関連する作業の使用されない場合、残りの手順を終了せずに **商社の情報をインストール** ウィンドウを閉じません。</span><span class="sxs-lookup"><span data-stu-id="8755b-176">If the hardware station that was installed won't be used for payment-related work, don't close the **Install merchant information** window without completing the remaining steps.</span></span> <span data-ttu-id="8755b-177">このインストールが正常に完了しないと、ハードウェア ステーションは機能しません。</span><span class="sxs-lookup"><span data-stu-id="8755b-177">The hardware station won't work unless this installation is successfully completed.</span></span>
    
    > - <span data-ttu-id="8755b-178">バージョン 10.0.6 以降では、Install マーチャント情報ツールは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8755b-178">For version 10.0.6 and above, the install merchant information tool is no longer used.</span></span> <span data-ttu-id="8755b-179">代わりに、ハードウェア ステーションのマーチャント情報は、ログオン時またはハードウェア ステーションが有効になったときに POS によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-179">Instead, the merchant information for the hardware station is set by the POS at the time of logon or when the hardware station is made active.</span></span> <span data-ttu-id="8755b-180">ハードウェア ステーションを有効にした後にも Retail サーバーを使用できない場合は、最後の商社プロパティが、Retail サーバーへの接続が再確立されるまでの間に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-180">If the retail server is not available when the hardware station is subsequently made active, the last known merchant properties will be used by until the connection to the retail server is re-established.</span></span> <span data-ttu-id="8755b-181">ハードウェア ステーションの更新と同時に、POS クライアントがバージョン 10.0.6 に更新されていないと、POS クライアントが同じまたはそれ以降のバージョンに更新されるまで、商社プロパティは更新されません。</span><span class="sxs-lookup"><span data-stu-id="8755b-181">If the POS client is not upgraded to version 10.0.6 at the same time the hardware station is upgraded, merchant properties will not be updated until the POS client is upgraded to an equal or later version.</span></span> 

8. <span data-ttu-id="8755b-182">支払商社情報のインストール ツールは、Azure AD 資格情報を要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-182">The Install merchant information tool might request Azure AD credentials.</span></span> <span data-ttu-id="8755b-183">Retail ハードウェア ステーションをインストールするユーザーの Azure AD 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-183">Enter the Azure AD credentials of the user who is installing Retail hardware station.</span></span>
9. <span data-ttu-id="8755b-184">Retail Server URL は、Retail ハードウェア ステーションのインストールによって決定され、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-184">The Retail Server URL is determined through the Retail hardware station installation and is entered automatically.</span></span> <span data-ttu-id="8755b-185">インストーラーは、この URL を使用して、ユーザーがアドレス帳を介して接続している店舗のリストをロードします。</span><span class="sxs-lookup"><span data-stu-id="8755b-185">The installer uses this URL to load the list of stores that the user is connected to via the address book.</span></span>
10. <span data-ttu-id="8755b-186">ハードウェア ステーションがインストールされた小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-186">Select the retail store that the hardware station was installed for.</span></span>
11. <span data-ttu-id="8755b-187">現在のコンピューターにインストールされていたハードウェア ステーションに一致するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-187">Select the hardware profile that matches the hardware station that was installed on the current computer.</span></span>
12. <span data-ttu-id="8755b-188">現在のコンピューターおよび Retail で既に完了している Retail ハードウェア ステーション構成に基づいて、ホスト名と EFT ターミナル ID が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8755b-188">Verify that the host names and EFT terminal IDs are correct, based on the current computer and the Retail hardware station configuration that has already been completed in Retail.</span></span> <span data-ttu-id="8755b-189">この情報を検証した後、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-189">After you've verified this information, select **Install**.</span></span>
13. <span data-ttu-id="8755b-190">商業口座情報が正しくインストールされたことを示すメッセージが表示されたら **閉じる** ボタンを選択してインストーラーを終了します。</span><span class="sxs-lookup"><span data-stu-id="8755b-190">When you receive a message that states that the merchant account information was installed correctly, exit the installer by selecting the **Close** button.</span></span>

## <a name="help-secure-retail-hardware-station"></a><span data-ttu-id="8755b-191">Retail ハードウェア ステーションのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="8755b-191">Help secure Retail hardware station</span></span>

<span data-ttu-id="8755b-192">現在のセキュリティ基準では、実稼動環境で次のオプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-192">Current security standards state that the following options should be set in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="8755b-193">ハードウェア ステーションのインストーラーは、セルフサービスによるインストールの一部として、これらのレジストリの編集を自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="8755b-193">The hardware station installer automatically makes these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="8755b-194">SSL を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-194">SSL should be disabled.</span></span>
- <span data-ttu-id="8755b-195">Transport Layer Security (TLS) version 1.2 (または現行最新バージョン) のみを有効にして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-195">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8755b-196">既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効になります。</span><span class="sxs-lookup"><span data-stu-id="8755b-196">By default, SSL and all version of TLS except TLS 1.2 are disabled.</span></span> <span data-ttu-id="8755b-197">これらを値の編集または有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="8755b-197">To edit or enable these values, follow these steps:</span></span>
    >
    > 1. <span data-ttu-id="8755b-198">Windows ロゴキーと R キーを同時に押して、**実行** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="8755b-198">Press the Windows logo key+R to open a **Run** window.</span></span>
    > 2. <span data-ttu-id="8755b-199">**開く** フィールドに、**Regedit** と入力してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-199">In the **Open** field, type **Regedit**, and then select **OK**.</span></span>
    > 3. <span data-ttu-id="8755b-200">**ユーザー アカウント コントロール** ウィンドウが現われたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-200">If a **User Account Control** window appears, select **Yes**.</span></span>
    > 4. <span data-ttu-id="8755b-201">新しい **レジストリ エディター** ウィンドウで、**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8755b-201">In the new **Registry Editor** window, go to **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols**.</span></span> <span data-ttu-id="8755b-202">TLS 1.2 のみを有効にするために、以下のキーは自動的に挿入されています:</span><span class="sxs-lookup"><span data-stu-id="8755b-202">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>
    >
    >    - <span data-ttu-id="8755b-203">TLS 1.2\\Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="8755b-203">TLS 1.2\\Server:Enabled=1</span></span>
    >    - <span data-ttu-id="8755b-204">TLS 1.2\\Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="8755b-204">TLS 1.2\\Server:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="8755b-205">TLS 1.2\\Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="8755b-205">TLS 1.2\\Client:Enabled=1</span></span>
    >    - <span data-ttu-id="8755b-206">TLS 1.2\\Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="8755b-206">TLS 1.2\\Client:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="8755b-207">TLS 1.1\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-207">TLS 1.1\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-208">TLS 1.1\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-208">TLS 1.1\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-209">TLS 1.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-209">TLS 1.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-210">TLS 1.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-210">TLS 1.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-211">SSL 3.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-211">SSL 3.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-212">SSL 3.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-212">SSL 3.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-213">SSL 2.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-213">SSL 2.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="8755b-214">SSL 2.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="8755b-214">SSL 2.0\\Client:Enabled=0</span></span>

- <span data-ttu-id="8755b-215">知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。</span><span class="sxs-lookup"><span data-stu-id="8755b-215">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="8755b-216">クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8755b-216">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="8755b-217">信頼された証明機関のみ、Retail ハードウェア ステーションを実行するコンピューター上で使用される証明書の調達に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-217">Only trusted certificate authorities should be used to procure certificates that will be used on computers that run Retail hardware station.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="8755b-218">ほどんどの一般的な下位セキュリティ ソフトウェアおよびサービスはすべての下位セキュリティ基準が無効になった後に動作を停止します。</span><span class="sxs-lookup"><span data-stu-id="8755b-218">Most common, lower-security software and services will stop working after all lower-security standards are disabled.</span></span> <span data-ttu-id="8755b-219">それらを再使用するには、前述のレジストリ キーに移動し、**有効** キーを **0** から **1** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8755b-219">To use them again, go to the preceding registry keys, and set the **Enabled** key from **0** to **1**.</span></span>
> - <span data-ttu-id="8755b-220">IIS と Payment Card Industry (PCI) の要件向けのセキュリティ ガイドラインを確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="8755b-220">It's critical that you review security guidelines for IIS and Payment Card Industry (PCI) requirements.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8755b-221">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="8755b-221">Troubleshooting</span></span>

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="8755b-222">Modern POS は、選択リストにあるハードウェア ステーションを検出できますが、ペアリングを完了することはできません</span><span class="sxs-lookup"><span data-stu-id="8755b-222">Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="8755b-223">**ソリューション:** 以下の潜在的障害ポイントを確認してください:</span><span class="sxs-lookup"><span data-stu-id="8755b-223">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="8755b-224">Modern POS を実行しているコンピュータは、Retail ハードウェア ステーションを実行しているコンピュータで使用される証明書を信頼します。</span><span class="sxs-lookup"><span data-stu-id="8755b-224">The computer that is running Modern POS trusts the certificate that is used on the computer that runs Retail hardware station.</span></span>

    - <span data-ttu-id="8755b-225">Web ブラウザーでこの設定を確認するには、次のURL `https://<Computer Name>:<Port Number>/HardwareStation/ping` に移動します。</span><span class="sxs-lookup"><span data-stu-id="8755b-225">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>
    - <span data-ttu-id="8755b-226">この URL は ping を使用してコンピュータにアクセスできるかどうかを確認し、ブラウザは証明書が信頼できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="8755b-226">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="8755b-227">(たとえば、Internet Explorer ではカギのシンボルがアドレス バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8755b-227">(For example, in Internet Explorer, a lock symbol appears in the address bar.</span></span> <span data-ttu-id="8755b-228">このシンボルを選択すると、Internet Explorer は証明書が現在信頼されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="8755b-228">When you select this symbol, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="8755b-229">表示される証明書の詳細を見ることで、ローカル コンピュータに証明書をインストールできます)。</span><span class="sxs-lookup"><span data-stu-id="8755b-229">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="8755b-230">Retail ハードウェア ステーションを実行するコンピュータで、ハードウェア ステーションで使用されるポートはファイアウォールで開かれます。</span><span class="sxs-lookup"><span data-stu-id="8755b-230">On the computer that runs Retail hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="8755b-231">小売ハードウェア ステーションのインストールの最後に実行される支払商社情報インストール ツールを使用して、小売ハードウェア ステーションに支払商社情報が正しくインストールされます。</span><span class="sxs-lookup"><span data-stu-id="8755b-231">Retail hardware station has properly installed merchant account information through the Install merchant information tool that runs at the end of the Retail hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="8755b-232">Modern POS が選択リストにあるハードウェア ステーションを検出できない</span><span class="sxs-lookup"><span data-stu-id="8755b-232">Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="8755b-233">**ソリューション:** 次の要素のいずれかによりこの問題が生じることがあり得ます。</span><span class="sxs-lookup"><span data-stu-id="8755b-233">**Solution:** Any one of the following factors can cause this issue:</span></span>

- <span data-ttu-id="8755b-234">Retail ハードウェア ステーションがコマース バックオフィスに正しく設定されていません。</span><span class="sxs-lookup"><span data-stu-id="8755b-234">Retail hardware station hasn't been set up correctly in Commerce headquarters.</span></span> <span data-ttu-id="8755b-235">このトピックで説明した手順を使用して、ハードウェア ステーションのプロファイルとハードウェア ステーションが正しく入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8755b-235">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="8755b-236">チャンネル構成を更新するジョブが実行されていません。</span><span class="sxs-lookup"><span data-stu-id="8755b-236">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="8755b-237">この場合、チャンネル構成用に 1070 のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="8755b-237">In this case, run the 1070 job for channel configuration.</span></span>
- <span data-ttu-id="8755b-238">そのコンピューターからハードウェア ステーションにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="8755b-238">The hardware station isn't accessible from that computer.</span></span> <span data-ttu-id="8755b-239">Web ブラウザーからハードウェア ステーション URL ping テストを利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8755b-239">Verify that the hardware station URL ping test is accessible from a web browser.</span></span> <span data-ttu-id="8755b-240">この URL は、ハードウェア ステーション インストーラーの最後にあり、`https://<Computer Name>:<Port Number>/HardwareStation/ping` の形式です</span><span class="sxs-lookup"><span data-stu-id="8755b-240">This URL can be found at the end of the hardware station installer and is in the following form: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>

## <a name="uninstall-retail-hardware-station"></a><span data-ttu-id="8755b-241">Retail ハードウェア ステーションのアンインストール</span><span class="sxs-lookup"><span data-stu-id="8755b-241">Uninstall Retail hardware station</span></span>

<span data-ttu-id="8755b-242">Microsoft Windows でコントロール パネルを使用して Retail ハードウェア ステーションをアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="8755b-242">You can use Control Panel in Microsoft Windows to uninstall Retail hardware station.</span></span>

1. <span data-ttu-id="8755b-243">Windows ロゴ キーを押し、検索ボックスに **コントロール パネル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="8755b-243">Press the Windows logo key, and then, in the search box, type **Control Panel**.</span></span> <span data-ttu-id="8755b-244">検索結果の一覧で、**コントロール パネル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-244">In the list of search results, select **Control Panel**.</span></span>
2. <span data-ttu-id="8755b-245">コントロール パネルで、**プログラム** &gt; **プログラムのアンインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-245">In Control Panel, select **Programs** &gt; **Uninstall a program**.</span></span> <span data-ttu-id="8755b-246">**プログラムと機能** ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="8755b-246">The **Programs and Features** window opens.</span></span>
3. <span data-ttu-id="8755b-247">**Microsoft Dynamics 365 for Retail ハードウェア ステーション** を選択し、プログラムの一覧の上にある **アンインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8755b-247">Select **Microsoft Dynamics 365 for Retail hardware station**, and then select **Uninstall** above the list of programs.</span></span>
4. <span data-ttu-id="8755b-248">アンインストールがプログラムの削除を完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="8755b-248">Wait for the uninstaller to finish removing the program.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

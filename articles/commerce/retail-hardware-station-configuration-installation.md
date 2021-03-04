---
title: Retail ハードウェア ステーションのコンフィギュレーションとインストール
description: このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。 また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。
author: jashanno
manager: AnnBe
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: a9013b5943a135be8a446e0bd2b1d54d8345d7d8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4979634"
---
# <a name="configure-and-install-retail-hardware-station"></a><span data-ttu-id="58337-104">Retail ハードウェア ステーションのコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="58337-104">Configure and install Retail hardware station</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="58337-105">このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="58337-105">This topic explains how to configure, download, and install Retail hardware station by using self-service.</span></span> <span data-ttu-id="58337-106">また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="58337-106">It also explains how to uninstall Retail hardware station.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58337-107">このコンポーネントはサーバー証明書を利用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="58337-107">It is critical to note that this component utilizes a server certificate.</span></span> <span data-ttu-id="58337-108">有効期限に対してサーバー証明書を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-108">Server certificates must be managed for expiration.</span></span> <span data-ttu-id="58337-109">既定では、証明書は 1 つの暦年 (365 日) で期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="58337-109">By default, a certificate expires in one calendar year (365 days).</span></span>

## <a name="download-retail-hardware-station-by-using-self-service"></a><span data-ttu-id="58337-110">セルフサービスを使い、Retail ハードウェア ステーションをダウンロード</span><span class="sxs-lookup"><span data-stu-id="58337-110">Download Retail hardware station by using self-service</span></span>

### <a name="configure-a-new-retail-hardware-station"></a><span data-ttu-id="58337-111">新しい Retail Hardware Station のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="58337-111">Configure a new Retail hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="58337-112">Retail (初回リリース) のアップグレードされていないバージョンである 2016 年 2 月を実行している場合は、手順 6 はスキップします。</span><span class="sxs-lookup"><span data-stu-id="58337-112">If you're running the February 2016, non-upgraded version of Retail (Initial release), skip step 6.</span></span>

1. <span data-ttu-id="58337-113">Azure AD 証明書を使用して、Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="58337-113">Use your Azure AD credentials to sign in to the Retail trial.</span></span>
2. <span data-ttu-id="58337-114">**ようこそ** ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="58337-114">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="58337-115">**すべての小売店舗** ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-115">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="58337-116">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="58337-116">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-117">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="58337-117">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="58337-118">**小売店舗詳細** ページや、**ハードウェア ステーション** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-118">On the **Retail store details** page, on the **Hardware stations** FastTab, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-119">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="58337-119">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="58337-120">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="58337-120">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="58337-121">**ハードウェア ステーション タイプ** フィールドで、**共有** を選択して、このハードウェア ステーションが Internet Information Services (IIS)、外部の販売時点管理 (POS) システムによって使用されるインストール済みのハードウェア ステーションであることを示します。</span><span class="sxs-lookup"><span data-stu-id="58337-121">In the **Hardware station type** field, select **Shared** to indicate that this hardware station is an Internet Information Services (IIS), installed hardware station that will be used by external point of sale (POS) systems.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-122">値 **Shared** は、インストールが真に共有されているハードウェア ステーションのインストールであり、HTTPS 通信を介して機能することを示します。</span><span class="sxs-lookup"><span data-stu-id="58337-122">The value **Shared** signifies that the installation is a truly shared hardware station installation, and that it works through HTTPS communication.</span></span> <span data-ttu-id="58337-123">対照的に、**専用** という値はハードウェア ステーションが Modern POS の一部であり、プロセス間通信を通じて機能していることを示します。</span><span class="sxs-lookup"><span data-stu-id="58337-123">By contrast, the value **Dedicated** signifies that the hardware station is a part of Modern POS, and that it works through inter-process communication.</span></span>

6. <span data-ttu-id="58337-124">ハードウェア ステーションのプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-124">Select a hardware station profile.</span></span>

7. <span data-ttu-id="58337-125">Retail ハードウェア ステーションをインストールするコンピュータのホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-125">Enter the host name of the computer that you're installing Retail hardware station on.</span></span> <span data-ttu-id="58337-126">また、商業口座情報のコンピューターに関連付けられている電子決済 (EFT) ターミナル ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-126">Additionally, enter the electronic funds transfer (EFT) terminal ID that is associated with that computer for merchant account information.</span></span>

8. <span data-ttu-id="58337-127">一括配置を使用して構成ファイルまたは初期インストールを活用するには、次のセクションの詳細説明にあるように、インストール中に使用する証明書の拇印を入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-127">To utilize the configuration file or initial installation using mass deployment, enter the certificate thumbprint that is to be used during the installation that's detailed in the next section.</span></span>

### <a name="download-the-retail-hardware-station-installer"></a><span data-ttu-id="58337-128">Retail ハードウェア ステーション インストーラーをダウンロード</span><span class="sxs-lookup"><span data-stu-id="58337-128">Download the Retail hardware station installer</span></span>

1. <span data-ttu-id="58337-129">Azure AD 資格情報を使用して、Retail Headquarters または Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="58337-129">Use your Azure AD credentials to sign in to the Retail headquarters or Retail trial.</span></span>
2. <span data-ttu-id="58337-130">**ようこそ** ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗** に移動します。</span><span class="sxs-lookup"><span data-stu-id="58337-130">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="58337-131">**すべての小売店舗** ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-131">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="58337-132">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="58337-132">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-133">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="58337-133">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="58337-134">**小売店舗詳細** ページで、**ハードウェア ステーション** クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-134">On the **Retail store details** page, select the **Hardware stations** FastTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-135">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="58337-135">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="58337-136">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="58337-136">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="58337-137">ダウンロードするハードウェア ステーションを選択し、**ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-137">Select the hardware station to download, and then select **Download**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="58337-138">ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58337-138">Browsers might block the download pop-up that is generated.</span></span> <span data-ttu-id="58337-139">**1 回許可** または **このサイトのオプション** &gt; **常に許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-139">You must select either **Allow once** or **Options for this site** &gt; **Always allow**.</span></span> <span data-ttu-id="58337-140">その後、再度 **ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-140">Then select **Download** again.</span></span>

6. <span data-ttu-id="58337-141">Internet Explorer ウィンドウの下部に表示される通知バーで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-141">On the Notification bar that appears at the bottom of the Internet Explorer window, select **Save**.</span></span> <span data-ttu-id="58337-142">(通知バーは、他のブラウザでは別の場所に表示される場合があります。)</span><span class="sxs-lookup"><span data-stu-id="58337-142">(The Notification bar might appear in a different place in other browsers.)</span></span>
7. <span data-ttu-id="58337-143">一括配置またはコマンド ラインからの配置に必要な場合は、構成ファイルのダウンロードに対して上記の手順を繰り返します。これは、選択した **ダウンロード** ボタンの横にあるボタンです。</span><span class="sxs-lookup"><span data-stu-id="58337-143">If needed for mass deployment or command line deployment, repeat the above steps for the configuration file download, which is a button next to the **Download** button that you previously selected.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="58337-144">ダウンロードした構成ファイル名が、インストーラーのベース ファイル名と同じでない場合は、XML 構成ファイルを同じベース名に変更するか、コマンド ラインを使用してインストーラーを実行し、構成ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="58337-144">If the configuration file downloaded does not have the same base file name as the installer, either rename the XML configuration file to be the same base name or run the installer using the command line to specify the configuration file.</span></span>
    > - <span data-ttu-id="58337-145">Commerce ハードウェア ステーションのインストールには、構成ファイルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="58337-145">Note that the configuration file is not required for the installation of Commerce hardware station.</span></span>

8. <span data-ttu-id="58337-146">ファイルを保存したら、インストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="58337-146">After the files have been saved, run the installer.</span></span> <span data-ttu-id="58337-147">(この手順はブラウザによって異なる場合があります。)</span><span class="sxs-lookup"><span data-stu-id="58337-147">(This step might differ depending on your browser.)</span></span>

### <a name="run-the-installer"></a><span data-ttu-id="58337-148">インストーラーを実行</span><span class="sxs-lookup"><span data-stu-id="58337-148">Run the installer</span></span>

> [!NOTE]
> <span data-ttu-id="58337-149">Retail ハードウェア ステーション インストーラーを実行する前に、すべての[システム要件](../fin-and-ops/get-started/system-requirements.md)が満たされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="58337-149">Before you run the Retail hardware station installer, make sure that all [system requirements](../fin-and-ops/get-started/system-requirements.md) are met.</span></span>

<span data-ttu-id="58337-150">Retail ハードウェア ステーション インストーラーは、まず関連付けられているファイルを抽出し、インストールを開始します。</span><span class="sxs-lookup"><span data-stu-id="58337-150">The Retail hardware station installer first extracts the associated files and then begins the installation.</span></span>

1. <span data-ttu-id="58337-151">インストーラーは、すべての前提条件が満たされていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="58337-151">The installer validates that all prerequisites are met.</span></span> <span data-ttu-id="58337-152">サイドローディング キーが必要な場合は、インストーラーがそれを要求します。</span><span class="sxs-lookup"><span data-stu-id="58337-152">If a sideloading key is required, the installer requests it.</span></span> <span data-ttu-id="58337-153">このキーは、各デバイスの **一般** の下にある **デバイス** ページにあります。</span><span class="sxs-lookup"><span data-stu-id="58337-153">This key is found on the **Devices** page for each device, under **General**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="58337-154">システムの再起動が必要な場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="58337-154">If a system restart is required, the installer informs you of this requirement but can continue the installation.</span></span>
    > - <span data-ttu-id="58337-155">小売販売時点管理の Object Linking and Embedding (OPOS) 標準に基づいたハードウェアを使用する前に、OPOS コモン コントロール オブジェクトをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-155">Before you can use hardware that is based on the Object Linking and Embedding for Retail Point of Sale (OPOS) standard, the OPOS Common Control Objects must be installed.</span></span> <span data-ttu-id="58337-156">インストールされていない場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="58337-156">If they aren't installed, the installer informs you of this requirement but can continue the installation.</span></span>

2. <span data-ttu-id="58337-157">Retail Server URL を入力し (たとえば、`https://MyCompanyNameret.axcloud.dynamics.com/Commerce`)、**次** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-157">Enter the Retail Server URL (for example, `https://MyCompanyNameret.axcloud.dynamics.com/Commerce`), and then select **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-158">Retail Server の URL は **小売店舗詳細** ページ上の **ハードウェア ステーション** クイック タブの最上部で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="58337-158">You can find the Retail Server URL at the top of the **Hardware stations** FastTab on the **Retail store details** page.</span></span>

3. <span data-ttu-id="58337-159">HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-159">Select a valid Secure Sockets Layer (SSL) certificate to use for HTTPS communication.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-160">証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-160">The certificate must use private key storage, and server authentication must be listed in the enhanced key usage property.</span></span> <span data-ttu-id="58337-161">また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="58337-161">Additionally, the certificate must be trusted locally, and it can't be expired.</span></span> <span data-ttu-id="58337-162">ローカル コンピューターの個人用証明書格納場所に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-162">It must be stored in the personal certificate store location on the local computer.</span></span>

4. <span data-ttu-id="58337-163">次のページでは、IIS アプリケーション プールで使用する必要があるユーザーを要求します。</span><span class="sxs-lookup"><span data-stu-id="58337-163">The next page requests the user that should be used for the IIS application pool.</span></span> <span data-ttu-id="58337-164">バージョン 1611 以降の既定では、インストーラーが自動的にサービス アカウントを作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="58337-164">By default in version 1611 and later, the installer can automatically create and use a service account.</span></span> <span data-ttu-id="58337-165">ドメインを使用している場合や特定のコントロールが必要な場合は、チェックボックスをオフにして、アプリケーション プールが実行するユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-165">If you're on a domain or require more specific controls, clear the check box, and then enter the user name and password that the application pool should run under.</span></span>
5. <span data-ttu-id="58337-166">使用する HTTPS ポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-166">Enter the HTTPS port to use.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="58337-167">Retail で HTTPS ポートを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="58337-167">You can find the HTTPS port in Retail.</span></span> <span data-ttu-id="58337-168">(このトピックで前述したコンフィギュレーションの指示を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="58337-168">(See the configuration instructions earlier in this topic).</span></span>
    > - <span data-ttu-id="58337-169">インストーラーは自動的にホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-169">The installer automatically enters the host name.</span></span> <span data-ttu-id="58337-170">何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更できます。</span><span class="sxs-lookup"><span data-stu-id="58337-170">If, for any reason, you must change the host name for the installation, you can change it here.</span></span> <span data-ttu-id="58337-171">ホスト名はシステムの完全修飾ドメイン名 (FQDN) でなければなりません。また、選択したハードウェア ステーション エントリの **ホスト名** フィールドに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-171">The host name must be the fully-qualified domain name (FQDN) of the system, and it must be entered in the **Host name** field for the selected hardware station entry.</span></span>

6. <span data-ttu-id="58337-172">インストーラーは Retail ハードウェア ステーションをインストールし、インストールが成功したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="58337-172">The installer installs Retail hardware station and then indicates whether the installation was successful.</span></span>
7. <span data-ttu-id="58337-173">インストールが完了したら、支払商社情報のインストール ツールが起動する場合があります。</span><span class="sxs-lookup"><span data-stu-id="58337-173">When the installation is completed, the Install merchant information tool may start.</span></span> <span data-ttu-id="58337-174">このインストーラーは、環境に接続し、選択したハードウェア ステーションの販売者の口座情報 (EFT IDなど) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="58337-174">This installer connects to the environment and installs the merchant account information (such as the EFT ID) for the selected hardware station.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="58337-175">インストールされているハードウェア ステーションが支払に関連する作業の使用されない場合、残りの手順を終了せずに **商社の情報をインストール** ウィンドウを閉じません。</span><span class="sxs-lookup"><span data-stu-id="58337-175">If the hardware station that was installed won't be used for payment-related work, don't close the **Install merchant information** window without completing the remaining steps.</span></span> <span data-ttu-id="58337-176">このインストールが正常に完了しないと、ハードウェア ステーションは機能しません。</span><span class="sxs-lookup"><span data-stu-id="58337-176">The hardware station won't work unless this installation is successfully completed.</span></span>
    
    > - <span data-ttu-id="58337-177">バージョン 10.0.6 以降では、Install マーチャント情報ツールは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="58337-177">For version 10.0.6 and above, the install merchant information tool is no longer used.</span></span> <span data-ttu-id="58337-178">代わりに、ハードウェア ステーションのマーチャント情報は、ログオン時またはハードウェア ステーションが有効になったときに POS によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="58337-178">Instead, the merchant information for the hardware station is set by the POS at the time of logon or when the hardware station is made active.</span></span> <span data-ttu-id="58337-179">ハードウェア ステーションを有効にした後にも Retail サーバーを使用できない場合は、最後の商社プロパティが、Retail サーバーへの接続が再確立されるまでの間に使用されます。</span><span class="sxs-lookup"><span data-stu-id="58337-179">If the retail server is not available when the hardware station is subsequently made active, the last known merchant properties will be used by until the connection to the retail server is re-established.</span></span> <span data-ttu-id="58337-180">ハードウェア ステーションの更新と同時に、POS クライアントがバージョン 10.0.6 に更新されていないと、POS クライアントが同じまたはそれ以降のバージョンに更新されるまで、商社プロパティは更新されません。</span><span class="sxs-lookup"><span data-stu-id="58337-180">If the POS client is not upgraded to version 10.0.6 at the same time the hardware station is upgraded, merchant properties will not be updated until the POS client is upgraded to an equal or later version.</span></span> 

8. <span data-ttu-id="58337-181">支払商社情報のインストール ツールは、Azure AD 資格情報を要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="58337-181">The Install merchant information tool might request Azure AD credentials.</span></span> <span data-ttu-id="58337-182">Retail ハードウェア ステーションをインストールするユーザーの Azure AD 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-182">Enter the Azure AD credentials of the user who is installing Retail hardware station.</span></span>
9. <span data-ttu-id="58337-183">Retail Server URL は、Retail ハードウェア ステーションのインストールによって決定され、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="58337-183">The Retail Server URL is determined through the Retail hardware station installation and is entered automatically.</span></span> <span data-ttu-id="58337-184">インストーラーは、この URL を使用して、ユーザーがアドレス帳を介して接続している店舗のリストをロードします。</span><span class="sxs-lookup"><span data-stu-id="58337-184">The installer uses this URL to load the list of stores that the user is connected to via the address book.</span></span>
10. <span data-ttu-id="58337-185">ハードウェア ステーションがインストールされた小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-185">Select the retail store that the hardware station was installed for.</span></span>
11. <span data-ttu-id="58337-186">現在のコンピューターにインストールされていたハードウェア ステーションに一致するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-186">Select the hardware profile that matches the hardware station that was installed on the current computer.</span></span>
12. <span data-ttu-id="58337-187">現在のコンピューターおよび Retail で既に完了している Retail ハードウェア ステーション構成に基づいて、ホスト名と EFT ターミナル ID が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="58337-187">Verify that the host names and EFT terminal IDs are correct, based on the current computer and the Retail hardware station configuration that has already been completed in Retail.</span></span> <span data-ttu-id="58337-188">この情報を検証した後、**インストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-188">After you've verified this information, select **Install**.</span></span>
13. <span data-ttu-id="58337-189">商業口座情報が正しくインストールされたことを示すメッセージが表示されたら **閉じる** ボタンを選択してインストーラーを終了します。</span><span class="sxs-lookup"><span data-stu-id="58337-189">When you receive a message that states that the merchant account information was installed correctly, exit the installer by selecting the **Close** button.</span></span>

## <a name="help-secure-retail-hardware-station"></a><span data-ttu-id="58337-190">Retail ハードウェア ステーションのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="58337-190">Help secure Retail hardware station</span></span>

<span data-ttu-id="58337-191">現在のセキュリティ基準では、実稼動環境で次のオプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-191">Current security standards state that the following options should be set in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="58337-192">ハードウェア ステーションのインストーラーは、セルフサービスによるインストールの一部として、これらのレジストリの編集を自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="58337-192">The hardware station installer automatically makes these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="58337-193">SSL を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-193">SSL should be disabled.</span></span>
- <span data-ttu-id="58337-194">Transport Layer Security (TLS) version 1.2 (または現行最新バージョン) のみを有効にして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-194">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="58337-195">既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効になります。</span><span class="sxs-lookup"><span data-stu-id="58337-195">By default, SSL and all version of TLS except TLS 1.2 are disabled.</span></span> <span data-ttu-id="58337-196">これらを値の編集または有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="58337-196">To edit or enable these values, follow these steps:</span></span>
    >
    > 1. <span data-ttu-id="58337-197">Windows ロゴキーと R キーを同時に押して、**実行** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="58337-197">Press the Windows logo key+R to open a **Run** window.</span></span>
    > 2. <span data-ttu-id="58337-198">**開く** フィールドに、**Regedit** と入力してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-198">In the **Open** field, type **Regedit**, and then select **OK**.</span></span>
    > 3. <span data-ttu-id="58337-199">**ユーザー アカウント コントロール** ウィンドウが現われたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-199">If a **User Account Control** window appears, select **Yes**.</span></span>
    > 4. <span data-ttu-id="58337-200">新しい **レジストリ エディター** ウィンドウで、**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols** に移動します。</span><span class="sxs-lookup"><span data-stu-id="58337-200">In the new **Registry Editor** window, go to **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols**.</span></span> <span data-ttu-id="58337-201">TLS 1.2 のみを有効にするために、以下のキーは自動的に挿入されています:</span><span class="sxs-lookup"><span data-stu-id="58337-201">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>
    >
    >    - <span data-ttu-id="58337-202">TLS 1.2\\Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="58337-202">TLS 1.2\\Server:Enabled=1</span></span>
    >    - <span data-ttu-id="58337-203">TLS 1.2\\Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="58337-203">TLS 1.2\\Server:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="58337-204">TLS 1.2\\Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="58337-204">TLS 1.2\\Client:Enabled=1</span></span>
    >    - <span data-ttu-id="58337-205">TLS 1.2\\Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="58337-205">TLS 1.2\\Client:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="58337-206">TLS 1.1\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-206">TLS 1.1\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-207">TLS 1.1\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-207">TLS 1.1\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-208">TLS 1.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-208">TLS 1.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-209">TLS 1.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-209">TLS 1.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-210">SSL 3.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-210">SSL 3.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-211">SSL 3.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-211">SSL 3.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-212">SSL 2.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-212">SSL 2.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="58337-213">SSL 2.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="58337-213">SSL 2.0\\Client:Enabled=0</span></span>

- <span data-ttu-id="58337-214">知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。</span><span class="sxs-lookup"><span data-stu-id="58337-214">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="58337-215">クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="58337-215">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="58337-216">信頼された証明機関のみ、Retail ハードウェア ステーションを実行するコンピューター上で使用される証明書の調達に使用されます。</span><span class="sxs-lookup"><span data-stu-id="58337-216">Only trusted certificate authorities should be used to procure certificates that will be used on computers that run Retail hardware station.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="58337-217">ほどんどの一般的な下位セキュリティ ソフトウェアおよびサービスはすべての下位セキュリティ基準が無効になった後に動作を停止します。</span><span class="sxs-lookup"><span data-stu-id="58337-217">Most common, lower-security software and services will stop working after all lower-security standards are disabled.</span></span> <span data-ttu-id="58337-218">それらを再使用するには、前述のレジストリ キーに移動し、**有効** キーを **0** から **1** に設定します。</span><span class="sxs-lookup"><span data-stu-id="58337-218">To use them again, go to the preceding registry keys, and set the **Enabled** key from **0** to **1**.</span></span>
> - <span data-ttu-id="58337-219">IIS と Payment Card Industry (PCI) の要件向けのセキュリティ ガイドラインを確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="58337-219">It's critical that you review security guidelines for IIS and Payment Card Industry (PCI) requirements.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="58337-220">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="58337-220">Troubleshooting</span></span>

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="58337-221">Modern POS は、選択リストにあるハードウェア ステーションを検出できますが、ペアリングを完了することはできません</span><span class="sxs-lookup"><span data-stu-id="58337-221">Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="58337-222">**ソリューション:** 以下の潜在的障害ポイントを確認してください:</span><span class="sxs-lookup"><span data-stu-id="58337-222">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="58337-223">Modern POS を実行しているコンピュータは、Retail ハードウェア ステーションを実行しているコンピュータで使用される証明書を信頼します。</span><span class="sxs-lookup"><span data-stu-id="58337-223">The computer that is running Modern POS trusts the certificate that is used on the computer that runs Retail hardware station.</span></span>

    - <span data-ttu-id="58337-224">Web ブラウザーでこの設定を確認するには、次のURL `https://<Computer Name>:<Port Number>/HardwareStation/ping` に移動します。</span><span class="sxs-lookup"><span data-stu-id="58337-224">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>
    - <span data-ttu-id="58337-225">この URL は ping を使用してコンピュータにアクセスできるかどうかを確認し、ブラウザは証明書が信頼できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="58337-225">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="58337-226">(たとえば、Internet Explorer ではカギのシンボルがアドレス バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="58337-226">(For example, in Internet Explorer, a lock symbol appears in the address bar.</span></span> <span data-ttu-id="58337-227">このシンボルを選択すると、Internet Explorer は証明書が現在信頼されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="58337-227">When you select this symbol, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="58337-228">表示される証明書の詳細を見ることで、ローカル コンピュータに証明書をインストールできます)。</span><span class="sxs-lookup"><span data-stu-id="58337-228">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="58337-229">Retail ハードウェア ステーションを実行するコンピュータで、ハードウェア ステーションで使用されるポートはファイアウォールで開かれます。</span><span class="sxs-lookup"><span data-stu-id="58337-229">On the computer that runs Retail hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="58337-230">小売ハードウェア ステーションのインストールの最後に実行される支払商社情報インストール ツールを使用して、小売ハードウェア ステーションに支払商社情報が正しくインストールされます。</span><span class="sxs-lookup"><span data-stu-id="58337-230">Retail hardware station has properly installed merchant account information through the Install merchant information tool that runs at the end of the Retail hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="58337-231">Modern POS が選択リストにあるハードウェア ステーションを検出できない</span><span class="sxs-lookup"><span data-stu-id="58337-231">Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="58337-232">**ソリューション:** 次の要素のいずれかによりこの問題が生じることがあり得ます。</span><span class="sxs-lookup"><span data-stu-id="58337-232">**Solution:** Any one of the following factors can cause this issue:</span></span>

- <span data-ttu-id="58337-233">Retail ハードウェア ステーションがコマース バックオフィスに正しく設定されていません。</span><span class="sxs-lookup"><span data-stu-id="58337-233">Retail hardware station hasn't been set up correctly in Commerce headquarters.</span></span> <span data-ttu-id="58337-234">このトピックで説明した手順を使用して、ハードウェア ステーションのプロファイルとハードウェア ステーションが正しく入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="58337-234">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="58337-235">チャンネル構成を更新するジョブが実行されていません。</span><span class="sxs-lookup"><span data-stu-id="58337-235">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="58337-236">この場合、チャンネル構成用に 1070 のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="58337-236">In this case, run the 1070 job for channel configuration.</span></span>
- <span data-ttu-id="58337-237">そのコンピューターからハードウェア ステーションにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="58337-237">The hardware station isn't accessible from that computer.</span></span> <span data-ttu-id="58337-238">Web ブラウザーからハードウェア ステーション URL ping テストを利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="58337-238">Verify that the hardware station URL ping test is accessible from a web browser.</span></span> <span data-ttu-id="58337-239">この URL は、ハードウェア ステーション インストーラーの最後にあり、`https://<Computer Name>:<Port Number>/HardwareStation/ping` の形式です</span><span class="sxs-lookup"><span data-stu-id="58337-239">This URL can be found at the end of the hardware station installer and is in the following form: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>

## <a name="uninstall-retail-hardware-station"></a><span data-ttu-id="58337-240">Retail ハードウェア ステーションのアンインストール</span><span class="sxs-lookup"><span data-stu-id="58337-240">Uninstall Retail hardware station</span></span>

<span data-ttu-id="58337-241">Microsoft Windows でコントロール パネルを使用して Retail ハードウェア ステーションをアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="58337-241">You can use Control Panel in Microsoft Windows to uninstall Retail hardware station.</span></span>

1. <span data-ttu-id="58337-242">Windows ロゴ キーを押し、検索ボックスに **コントロール パネル** と入力します。</span><span class="sxs-lookup"><span data-stu-id="58337-242">Press the Windows logo key, and then, in the search box, type **Control Panel**.</span></span> <span data-ttu-id="58337-243">検索結果の一覧で、**コントロール パネル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-243">In the list of search results, select **Control Panel**.</span></span>
2. <span data-ttu-id="58337-244">コントロール パネルで、**プログラム** &gt; **プログラムのアンインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-244">In Control Panel, select **Programs** &gt; **Uninstall a program**.</span></span> <span data-ttu-id="58337-245">**プログラムと機能** ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="58337-245">The **Programs and Features** window opens.</span></span>
3. <span data-ttu-id="58337-246">**Microsoft Dynamics 365 for Retail ハードウェア ステーション** を選択し、プログラムの一覧の上にある **アンインストール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="58337-246">Select **Microsoft Dynamics 365 for Retail hardware station**, and then select **Uninstall** above the list of programs.</span></span>
4. <span data-ttu-id="58337-247">アンインストールがプログラムの削除を完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="58337-247">Wait for the uninstaller to finish removing the program.</span></span>

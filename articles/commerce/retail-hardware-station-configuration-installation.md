---
title: Retail ハードウェア ステーションのコンフィギュレーションとインストール
description: このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。 また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。
author: jashanno
manager: AnnBe
ms.date: 09/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareStation
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 27161
ms.assetid: eb164a9d-5538-4b6f-81ad-87e05d92eca5
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d9e964f702b6902f42c4399906426edb1b7bda6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004617"
---
# <a name="configure-and-install-retail-hardware-station"></a><span data-ttu-id="de7dc-104">Retail ハードウェア ステーションのコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="de7dc-104">Configure and install Retail hardware station</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de7dc-105">このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-105">This topic explains how to configure, download, and install Retail hardware station by using self-service.</span></span> <span data-ttu-id="de7dc-106">また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-106">It also explains how to uninstall Retail hardware station.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="de7dc-107">このコンポーネントはサーバー証明書を利用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="de7dc-107">It is critical to note that this component utilizes a server certificate.</span></span> <span data-ttu-id="de7dc-108">有効期限に対してサーバー証明書を管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-108">Server certificates must be managed for expiration.</span></span> <span data-ttu-id="de7dc-109">既定では、証明書は 1 つの暦年 (365 日) で期限切れになります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-109">By default, a certificate expires in one calendar year (365 days).</span></span>

## <a name="download-retail-hardware-station-by-using-self-service"></a><span data-ttu-id="de7dc-110">セルフサービスを使い、Retail ハードウェア ステーションをダウンロード</span><span class="sxs-lookup"><span data-stu-id="de7dc-110">Download Retail hardware station by using self-service</span></span>

### <a name="configure-a-new-retail-hardware-station-profile-start-here-for-dynamics-365-for-retail-february-2016"></a><span data-ttu-id="de7dc-111">新しい Retail ハードウェア ステーション プロファイルをコンフィギュレーションする (Dynamics 365 for Retail、2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="de7dc-111">Configure a new Retail hardware station profile (Start here for Dynamics 365 for Retail, February 2016)</span></span>

> [!NOTE]
> <span data-ttu-id="de7dc-112">このステップは、Retail の 2016 年 2 月 (RTW) バージョンを実行している場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="de7dc-112">This procedure is required only if you're running the February 2016 (RTW) version of Retail.</span></span> <span data-ttu-id="de7dc-113">バージョン 1611 を実行している場合は、次の手順で開始します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-113">If you're running version 1611, start with the next procedure.</span></span>

1. <span data-ttu-id="de7dc-114">Microsoft Azure Active Directory (Azure AD) 証明書を使用して、Retail Headquarters または Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="de7dc-114">Use your Microsoft Azure Active Directory (Azure AD) credentials to sign in to the Retail headquarters or Retail trial.</span></span>
2. <span data-ttu-id="de7dc-115">**ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア ステーションのプロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-115">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware station profiles**.</span></span>
3. <span data-ttu-id="de7dc-116">**ハードウェア ステーションのプロファイル**ページの、アクション ペインで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-116">On the **Hardware station profile** page, on the Action Pane, select **New**.</span></span>
4. <span data-ttu-id="de7dc-117">**ハードウェア ステーション ID** フィールドに、一意なハードウェア ステーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-117">In the **Hardware station ID** field, enter a unique hardware station ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-118">**名前** フィールドは、固有のハードウェア ステーション プロファイルの説明に使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-118">The **Name** field is used for a description of the unique hardware station profile.</span></span>

5. <span data-ttu-id="de7dc-119">該当するフィールドにポート番号を入力し、ハードウェア プロファイルを選択してパッケージ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-119">In the appropriate fields, enter the port number, select a hardware profile, and select a package name.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-120">1 つのハードウェア ステーション パッケージのみが、デモ データが読み込まれた環境に提供されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-120">Only one hardware station package is provided for an environment that has been loaded with demo data.</span></span>

6. <span data-ttu-id="de7dc-121">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-121">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-new-retail-hardware-station-start-here-for-retail-version-1611-or-later"></a><span data-ttu-id="de7dc-122">新しい Retail ハードウェア ステーションをコンフィギュレーションする (Retail、バージョン 1611 以降)</span><span class="sxs-lookup"><span data-stu-id="de7dc-122">Configure a new Retail hardware station (Start here for Retail, version 1611 or later)</span></span>

> [!NOTE]
> <span data-ttu-id="de7dc-123">Retail (初回リリース) のアップグレードされていないバージョンである 2016 年 2 月を実行している場合は、手順 6 はスキップします。</span><span class="sxs-lookup"><span data-stu-id="de7dc-123">If you're running the February 2016, non-upgraded version of Retail (Initial release), skip step 6.</span></span>

1. <span data-ttu-id="de7dc-124">Azure AD 証明書を使用して、Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="de7dc-124">Use your Azure AD credentials to sign in to the Retail trial.</span></span>
2. <span data-ttu-id="de7dc-125">**ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗**に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-125">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="de7dc-126">**すべての小売店舗**ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-126">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="de7dc-127">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-127">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-128">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="de7dc-128">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="de7dc-129">**小売店舗詳細**ページや、**ハードウェア ステーション**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-129">On the **Retail store details** page, on the **Hardware stations** FastTab, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-130">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="de7dc-130">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="de7dc-131">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-131">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="de7dc-132">**ハードウェア ステーション タイプ** フィールドで、**共有**を選択して、このハードウェア ステーションが Internet Information Services (IIS)、外部の販売時点管理 (POS) システムによって使用されるインストール済みのハードウェア ステーションであることを示します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-132">In the **Hardware station type** field, select **Shared** to indicate that this hardware station is an Internet Information Services (IIS), installed hardware station that will be used by external point of sale (POS) systems.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-133">値 **Shared** は、インストールが真に共有されているハードウェア ステーションのインストールであり、HTTPS 通信を介して機能することを示します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-133">The value **Shared** signifies that the installation is a truly shared hardware station installation, and that it works through HTTPS communication.</span></span> <span data-ttu-id="de7dc-134">対照的に、**専用**という値はハードウェア ステーションが Modern POS の一部であり、プロセス間通信を通じて機能していることを示します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-134">By contrast, the value **Dedicated** signifies that the hardware station is a part of Modern POS, and that it works through inter-process communication.</span></span>

6. <span data-ttu-id="de7dc-135">実行しているバージョンに応じて、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-135">Follow one of these steps, depending on the version that you're running:</span></span>

    - <span data-ttu-id="de7dc-136">**バージョン 1611 の場合:** 該当するフィールドにポート番号を入力し、ハードウェア プロファイルを選択してパッケージ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-136">**For version 1611:** In the appropriate fields, enter the port number, select a hardware profile, and select a package name.</span></span>

        > [!NOTE]
        > <span data-ttu-id="de7dc-137">環境の作成時、1 つのハードウェア ステーション パッケージのみが、デモ データが読み込まれた環境に提供されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-137">Only one hardware station package is provided for an environment that has been loaded with demo data, at environment creation time.</span></span>

    - <span data-ttu-id="de7dc-138">**2016 年 2 月バージョンの場合:** ハードウェア ステーションのプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-138">**For the February 2016 version:** Select a hardware station profile.</span></span>

7. <span data-ttu-id="de7dc-139">Retail ハードウェア ステーションをインストールするコンピュータのホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-139">Enter the host name of the computer that you're installing Retail hardware station on.</span></span> <span data-ttu-id="de7dc-140">また、商業口座情報のコンピューターに関連付けられている電子決済 (EFT) ターミナル ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-140">Additionally, enter the electronic funds transfer (EFT) terminal ID that is associated with that computer for merchant account information.</span></span>

### <a name="download-the-retail-hardware-station-installer"></a><span data-ttu-id="de7dc-141">Retail ハードウェア ステーション インストーラーをダウンロード</span><span class="sxs-lookup"><span data-stu-id="de7dc-141">Download the Retail hardware station installer</span></span>

1. <span data-ttu-id="de7dc-142">Azure AD 証明書を使用して、小売用バックオフィスまたは Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="de7dc-142">Use your Azure AD credentials to sign in to the Retail headquarters or Retail trial.</span></span>
2. <span data-ttu-id="de7dc-143">**ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗**に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-143">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="de7dc-144">**すべての小売店舗**ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-144">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="de7dc-145">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-145">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-146">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="de7dc-146">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="de7dc-147">**小売店舗詳細**ページで、**ハードウェア ステーション**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-147">On the **Retail store details** page, select the **Hardware stations** FastTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-148">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="de7dc-148">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="de7dc-149">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-149">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="de7dc-150">ダウンロードするハードウェア ステーションを選択し、**ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-150">Select the hardware station to download, and then select **Download**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="de7dc-151">ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-151">Browsers might block the download pop-up that is generated.</span></span> <span data-ttu-id="de7dc-152">**1 回許可** または **このサイトのオプション** &gt; **常に許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-152">You must select either **Allow once** or **Options for this site** &gt; **Always allow**.</span></span> <span data-ttu-id="de7dc-153">その後、再度 **ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-153">Then select **Download** again.</span></span>
    > - <span data-ttu-id="de7dc-154">ハードウェア ステーションのプロファイルに基づいて、適切なパッケージがダウンロード用に自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-154">The correct installation package is automatically selected for download, based on the hardware station profile.</span></span>

6. <span data-ttu-id="de7dc-155">Internet Explorer ウィンドウの下部に表示される通知バーで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-155">On the Notification bar that appears at the bottom of the Internet Explorer window, select **Save**.</span></span> <span data-ttu-id="de7dc-156">(通知バーは、他のブラウザでは別の場所に表示される場合があります。)</span><span class="sxs-lookup"><span data-stu-id="de7dc-156">(The Notification bar might appear in a different place in other browsers.)</span></span>
7. <span data-ttu-id="de7dc-157">セットアップ インストーラが保存されたら、通知バーの、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-157">After the setup installer has been saved, on the Notification bar, select **Run**.</span></span> <span data-ttu-id="de7dc-158">(この手順はブラウザによって異なる場合があります。)</span><span class="sxs-lookup"><span data-stu-id="de7dc-158">(This step might differ, depending on your browser.)</span></span>

### <a name="run-the-installer"></a><span data-ttu-id="de7dc-159">インストーラーを実行</span><span class="sxs-lookup"><span data-stu-id="de7dc-159">Run the installer</span></span>

> [!NOTE]
> <span data-ttu-id="de7dc-160">Retail ハードウェア ステーション インストーラーを実行する前に、すべての[システム要件](../fin-and-ops/get-started/system-requirements.md)が満たされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="de7dc-160">Before you run the Retail hardware station installer, make sure that all [system requirements](../fin-and-ops/get-started/system-requirements.md) are met.</span></span>

<span data-ttu-id="de7dc-161">Retail ハードウェア ステーション インストーラーは、まず関連付けられているファイルを抽出し、インストールを開始します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-161">The Retail hardware station installer first extracts the associated files and then begins the installation.</span></span>

1. <span data-ttu-id="de7dc-162">インストーラーは、すべての前提条件が満たされていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-162">The installer validates that all prerequisites are met.</span></span> <span data-ttu-id="de7dc-163">サイドローディング キーが必要な場合は、インストーラーがそれを要求します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-163">If a sideloading key is required, the installer requests it.</span></span> <span data-ttu-id="de7dc-164">このキーは、各デバイスの **一般** の下にある**デバイス**ページにあります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-164">This key is found on the **Devices** page for each device, under **General**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="de7dc-165">システムの再起動が必要な場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-165">If a system restart is required, the installer informs you of this requirement but can continue the installation.</span></span>
    > - <span data-ttu-id="de7dc-166">小売販売時点管理の Object Linking and Embedding (OPOS) 標準に基づいたハードウェアを使用する前に、OPOS コモン コントロール オブジェクトをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-166">Before you can use hardware that is based on the Object Linking and Embedding for Retail Point of Sale (OPOS) standard, the OPOS Common Control Objects must be installed.</span></span> <span data-ttu-id="de7dc-167">インストールされていない場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-167">If they aren't installed, the installer informs you of this requirement but can continue the installation.</span></span>

2. <span data-ttu-id="de7dc-168">Retail Server URL を入力し (たとえば、`https://MyCompanyNameret.axcloud.dynamics.com/Commerce`)、**次** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-168">Enter the Retail Server URL (for example, `https://MyCompanyNameret.axcloud.dynamics.com/Commerce`), and then select **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-169">Retail Server の URL は **小売店舗詳細** ページ上の **ハードウェア ステーション** クイック タブの最上部で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-169">You can find the Retail Server URL at the top of the **Hardware stations** FastTab on the **Retail store details** page.</span></span>

3. <span data-ttu-id="de7dc-170">HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-170">Select a valid Secure Sockets Layer (SSL) certificate to use for HTTPS communication.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-171">証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-171">The certificate must use private key storage, and server authentication must be listed in the enhanced key usage property.</span></span> <span data-ttu-id="de7dc-172">また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-172">Additionally, the certificate must be trusted locally, and it can't be expired.</span></span> <span data-ttu-id="de7dc-173">ローカル コンピューターの個人用証明書格納場所に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-173">It must be stored in the personal certificate store location on the local computer.</span></span>

4. <span data-ttu-id="de7dc-174">次のページでは、IIS アプリケーション プールで使用する必要があるユーザーを要求します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-174">The next page requests the user that should be used for the IIS application pool.</span></span> <span data-ttu-id="de7dc-175">バージョン 1611 以降の既定では、インストーラーが自動的にサービス アカウントを作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-175">By default in version 1611 and later, the installer can automatically create and use a service account.</span></span> <span data-ttu-id="de7dc-176">ドメインを使用している場合や特定のコントロールが必要な場合は、チェックボックスをオフにして、アプリケーション プールが実行するユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-176">If you're on a domain or require more specific controls, clear the check box, and then enter the user name and password that the application pool should run under.</span></span>
5. <span data-ttu-id="de7dc-177">使用する HTTPS ポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-177">Enter the HTTPS port to use.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="de7dc-178">Retail で HTTPS ポートを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-178">You can find the HTTPS port in Retail.</span></span> <span data-ttu-id="de7dc-179">(このトピックで前述したコンフィギュレーションの指示を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="de7dc-179">(See the configuration instructions earlier in this topic).</span></span>
    > - <span data-ttu-id="de7dc-180">インストーラーは自動的にホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-180">The installer automatically enters the host name.</span></span> <span data-ttu-id="de7dc-181">何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更できます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-181">If, for any reason, you must change the host name for the installation, you can change it here.</span></span> <span data-ttu-id="de7dc-182">ホスト名はシステムの完全修飾ドメイン名 (FQDN) でなければなりません。また、選択したハードウェア ステーション エントリの **ホスト名**フィールドに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-182">The host name must be the fully-qualified domain name (FQDN) of the system, and it must be entered in the **Host name** field for the selected hardware station entry.</span></span>

6. <span data-ttu-id="de7dc-183">インストーラーは Retail ハードウェア ステーションをインストールし、インストールが成功したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-183">The installer installs Retail hardware station and then indicates whether the installation was successful.</span></span>
7. <span data-ttu-id="de7dc-184">インストールが完了したら、支払商社情報のインストール ツールが起動する場合があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-184">When the installation is completed, the Install merchant information tool may start.</span></span> <span data-ttu-id="de7dc-185">このインストーラーは、環境に接続し、選択したハードウェア ステーションの販売者の口座情報 (EFT IDなど) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="de7dc-185">This installer connects to the environment and installs the merchant account information (such as the EFT ID) for the selected hardware station.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="de7dc-186">インストールされているハードウェア ステーションが支払に関連する作業の使用されない場合、残りの手順を終了せずに**商社の情報をインストール**ウィンドウを閉じません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-186">If the hardware station that was installed won't be used for payment-related work, don't close the **Install merchant information** window without completing the remaining steps.</span></span> <span data-ttu-id="de7dc-187">このインストールが正常に完了しないと、ハードウェア ステーションは機能しません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-187">The hardware station won't work unless this installation is successfully completed.</span></span>
    
    > - <span data-ttu-id="de7dc-188">バージョン 10.0.6 以降では、Install マーチャント情報ツールは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="de7dc-188">For version 10.0.6 and above, the install merchant information tool is no longer used.</span></span> <span data-ttu-id="de7dc-189">代わりに、ハードウェア ステーションのマーチャント情報は、ログオン時またはハードウェア ステーションが有効になったときに POS によって設定されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-189">Instead, the merchant information for the hardware station is set by the POS at the time of logon or when the hardware station is made active.</span></span> <span data-ttu-id="de7dc-190">ハードウェア ステーションを有効にした後にも Retail サーバーを使用できない場合は、最後の商社プロパティが、Retail サーバーへの接続が再確立されるまでの間に使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-190">If the retail server is not available when the hardware station is subsequently made active, the last known merchant properties will be used by until the connection to the retail server is re-established.</span></span> <span data-ttu-id="de7dc-191">ハードウェア ステーションの更新と同時に、POS クライアントがバージョン 10.0.6 に更新されていないと、POS クライアントが同じまたはそれ以降のバージョンに更新されるまで、商社プロパティは更新されません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-191">If the POS client is not upgraded to version 10.0.6 at the same time the hardware station is upgraded, merchant properties will not be updated until the POS client is upgraded to an equal or later version.</span></span> 

8. <span data-ttu-id="de7dc-192">Install マーチャント情報ツールは、Azure AD 資格情報を要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-192">The Install merchant information tool might request Azure AD credentials.</span></span> <span data-ttu-id="de7dc-193">Retail ハードウェア ステーションをインストールするユーザーの Azure AD 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-193">Enter the Azure AD credentials of the user who is installing Retail hardware station.</span></span>
9. <span data-ttu-id="de7dc-194">Retail Server URL は、Retail ハードウェア ステーションのインストールによって決定され、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-194">The Retail Server URL is determined through the Retail hardware station installation and is entered automatically.</span></span> <span data-ttu-id="de7dc-195">インストーラーは、この URL を使用して、ユーザーがアドレス帳を介して接続している店舗のリストをロードします。</span><span class="sxs-lookup"><span data-stu-id="de7dc-195">The installer uses this URL to load the list of stores that the user is connected to via the address book.</span></span>
10. <span data-ttu-id="de7dc-196">ハードウェア ステーションがインストールされた小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-196">Select the retail store that the hardware station was installed for.</span></span>
11. <span data-ttu-id="de7dc-197">現在のコンピューターにインストールされていたハードウェア ステーションに一致するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-197">Select the hardware profile that matches the hardware station that was installed on the current computer.</span></span>
12. <span data-ttu-id="de7dc-198">現在のコンピューターおよび Retail で既に完了している Retail ハードウェア ステーション構成に基づいて、ホスト名と EFT ターミナル ID が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-198">Verify that the host names and EFT terminal IDs are correct, based on the current computer and the Retail hardware station configuration that has already been completed in Retail.</span></span> <span data-ttu-id="de7dc-199">この情報を検証した後、**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-199">After you've verified this information, select **Install**.</span></span>
13. <span data-ttu-id="de7dc-200">商業口座情報が正しくインストールされたことを示すメッセージが表示されたら**閉じる** ボタンを選択してインストーラーを終了します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-200">When you receive a message that states that the merchant account information was installed correctly, exit the installer by selecting the **Close** button.</span></span>

## <a name="help-secure-retail-hardware-station"></a><span data-ttu-id="de7dc-201">Retail ハードウェア ステーションのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="de7dc-201">Help secure Retail hardware station</span></span>

<span data-ttu-id="de7dc-202">現在のセキュリティ基準では、実稼動環境で次のオプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-202">Current security standards state that the following options should be set in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="de7dc-203">ハードウェア ステーションのインストーラーは、セルフサービスによるインストールの一部として、これらのレジストリの編集を自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="de7dc-203">The hardware station installer automatically makes these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="de7dc-204">SSL を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-204">SSL should be disabled.</span></span>
- <span data-ttu-id="de7dc-205">Transport Layer Security (TLS) version 1.2 (または現行最新バージョン) のみを有効にして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-205">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7dc-206">既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効になります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-206">By default, SSL and all version of TLS except TLS 1.2 are disabled.</span></span> <span data-ttu-id="de7dc-207">これらを値の編集または有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="de7dc-207">To edit or enable these values, follow these steps:</span></span>
    >
    > 1. <span data-ttu-id="de7dc-208">Windows ロゴキーと R キーを同時に押して、**実行**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-208">Press the Windows logo key+R to open a **Run** window.</span></span>
    > 2. <span data-ttu-id="de7dc-209">**開く**フィールドに、**Regedit** と入力してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-209">In the **Open** field, type **Regedit**, and then select **OK**.</span></span>
    > 3. <span data-ttu-id="de7dc-210">**ユーザー アカウント コントロール** ウィンドウが現われたら、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-210">If a **User Account Control** window appears, select **Yes**.</span></span>
    > 4. <span data-ttu-id="de7dc-211">新しい**レジストリ エディター** ウィンドウで、**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols** に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-211">In the new **Registry Editor** window, go to **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols**.</span></span> <span data-ttu-id="de7dc-212">TLS 1.2 のみを有効にするために、以下のキーは自動的に挿入されています:</span><span class="sxs-lookup"><span data-stu-id="de7dc-212">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>
    >
    >    - <span data-ttu-id="de7dc-213">TLS 1.2\\Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="de7dc-213">TLS 1.2\\Server:Enabled=1</span></span>
    >    - <span data-ttu-id="de7dc-214">TLS 1.2\\Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-214">TLS 1.2\\Server:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="de7dc-215">TLS 1.2\\Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="de7dc-215">TLS 1.2\\Client:Enabled=1</span></span>
    >    - <span data-ttu-id="de7dc-216">TLS 1.2\\Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-216">TLS 1.2\\Client:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="de7dc-217">TLS 1.1\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-217">TLS 1.1\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-218">TLS 1.1\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-218">TLS 1.1\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-219">TLS 1.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-219">TLS 1.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-220">TLS 1.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-220">TLS 1.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-221">SSL 3.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-221">SSL 3.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-222">SSL 3.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-222">SSL 3.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-223">SSL 2.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-223">SSL 2.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="de7dc-224">SSL 2.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="de7dc-224">SSL 2.0\\Client:Enabled=0</span></span>

- <span data-ttu-id="de7dc-225">知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。</span><span class="sxs-lookup"><span data-stu-id="de7dc-225">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="de7dc-226">クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7dc-226">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="de7dc-227">信頼された証明機関のみ、Retail ハードウェア ステーションを実行するコンピューター上で使用される証明書の調達に使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-227">Only trusted certificate authorities should be used to procure certificates that will be used on computers that run Retail hardware station.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="de7dc-228">ほどんどの一般的な下位セキュリティ ソフトウェアおよびサービスはすべての下位セキュリティ基準が無効になった後に動作を停止します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-228">Most common, lower-security software and services will stop working after all lower-security standards are disabled.</span></span> <span data-ttu-id="de7dc-229">それらを再使用するには、前述のレジストリ キーに移動し、**有効** キーを **0** から **1** に設定します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-229">To use them again, go to the preceding registry keys, and set the **Enabled** key from **0** to **1**.</span></span>
> - <span data-ttu-id="de7dc-230">IIS と Payment Card Industry (PCI) の要件向けのセキュリティ ガイドラインを確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="de7dc-230">It's critical that you review security guidelines for IIS and Payment Card Industry (PCI) requirements.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="de7dc-231">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="de7dc-231">Troubleshooting</span></span>

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="de7dc-232">Modern POS は、選択リストにあるハードウェア ステーションを検出できますが、ペアリングを完了することはできません</span><span class="sxs-lookup"><span data-stu-id="de7dc-232">Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="de7dc-233">**ソリューション:** 以下の潜在的障害ポイントを確認してください:</span><span class="sxs-lookup"><span data-stu-id="de7dc-233">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="de7dc-234">Modern POS を実行しているコンピュータは、Retail ハードウェア ステーションを実行しているコンピュータで使用される証明書を信頼します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-234">The computer that is running Modern POS trusts the certificate that is used on the computer that runs Retail hardware station.</span></span>

    - <span data-ttu-id="de7dc-235">Web ブラウザーでこの設定を確認するには、次のURL `https://<Computer Name>:<Port Number>/HardwareStation/ping` に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-235">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>
    - <span data-ttu-id="de7dc-236">この URL は ping を使用してコンピュータにアクセスできるかどうかを確認し、ブラウザは証明書が信頼できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-236">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="de7dc-237">(たとえば、Internet Explorer ではカギのシンボルがアドレス バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-237">(For example, in Internet Explorer, a lock symbol appears in the address bar.</span></span> <span data-ttu-id="de7dc-238">このシンボルを選択すると、Internet Explorer は証明書が現在信頼されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-238">When you select this symbol, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="de7dc-239">表示される証明書の詳細を見ることで、ローカル コンピュータに証明書をインストールできます)。</span><span class="sxs-lookup"><span data-stu-id="de7dc-239">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="de7dc-240">Retail ハードウェア ステーションを実行するコンピュータで、ハードウェア ステーションで使用されるポートはファイアウォールで開かれます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-240">On the computer that runs Retail hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="de7dc-241">小売ハードウェア ステーションのインストールの最後に実行される支払商社情報インストール ツールを使用して、小売ハードウェア ステーションに支払商社情報が正しくインストールされます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-241">Retail hardware station has properly installed merchant account information through the Install merchant information tool that runs at the end of the Retail hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="de7dc-242">Modern POS が選択リストにあるハードウェア ステーションを検出できない</span><span class="sxs-lookup"><span data-stu-id="de7dc-242">Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="de7dc-243">**ソリューション:** 次の要素のいずれかによりこの問題が生じることがあり得ます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-243">**Solution:** Any one of the following factors can cause this issue:</span></span>

- <span data-ttu-id="de7dc-244">Retail ハードウェア ステーションがコマース バックオフィスに正しく設定されていません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-244">Retail hardware station hasn't been set up correctly in Commerce headquarters.</span></span> <span data-ttu-id="de7dc-245">このトピックで説明した手順を使用して、ハードウェア ステーションのプロファイルとハードウェア ステーションが正しく入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-245">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="de7dc-246">チャンネル構成を更新するジョブが実行されていません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-246">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="de7dc-247">この場合、チャンネル構成用に 1070 のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-247">In this case, run the 1070 job for channel configuration.</span></span>
- <span data-ttu-id="de7dc-248">そのコンピューターからハードウェア ステーションにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="de7dc-248">The hardware station isn't accessible from that computer.</span></span> <span data-ttu-id="de7dc-249">Web ブラウザーからハードウェア ステーション URL ping テストを利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-249">Verify that the hardware station URL ping test is accessible from a web browser.</span></span> <span data-ttu-id="de7dc-250">この URL は、ハードウェア ステーション インストーラーの最後にあり、`https://<Computer Name>:<Port Number>/HardwareStation/ping` の形式です</span><span class="sxs-lookup"><span data-stu-id="de7dc-250">This URL can be found at the end of the hardware station installer and is in the following form: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>

## <a name="uninstall-retail-hardware-station"></a><span data-ttu-id="de7dc-251">Retail ハードウェア ステーションのアンインストール</span><span class="sxs-lookup"><span data-stu-id="de7dc-251">Uninstall Retail hardware station</span></span>

<span data-ttu-id="de7dc-252">Microsoft Windows でコントロール パネルを使用して Retail ハードウェア ステーションをアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-252">You can use Control Panel in Microsoft Windows to uninstall Retail hardware station.</span></span>

1. <span data-ttu-id="de7dc-253">Windows ロゴ キーを押し、検索ボックスに**コントロール パネル**と入力します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-253">Press the Windows logo key, and then, in the search box, type **Control Panel**.</span></span> <span data-ttu-id="de7dc-254">検索結果の一覧で、**コントロール パネル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-254">In the list of search results, select **Control Panel**.</span></span>
2. <span data-ttu-id="de7dc-255">コントロール パネルで、**プログラム** &gt; **プログラムのアンインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-255">In Control Panel, select **Programs** &gt; **Uninstall a program**.</span></span> <span data-ttu-id="de7dc-256">**プログラムと機能** ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-256">The **Programs and Features** window opens.</span></span>
3. <span data-ttu-id="de7dc-257">**Microsoft Dynamics 365 for Retail ハードウェア ステーション**を選択し、プログラムの一覧の上にある**アンインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7dc-257">Select **Microsoft Dynamics 365 for Retail hardware station**, and then select **Uninstall** above the list of programs.</span></span>
4. <span data-ttu-id="de7dc-258">アンインストールがプログラムの削除を完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="de7dc-258">Wait for the uninstaller to finish removing the program.</span></span>

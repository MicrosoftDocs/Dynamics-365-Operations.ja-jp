---
title: Retail ハードウェア ステーションのコンフィギュレーションとインストール
description: このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。 また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。
author: jashanno
manager: AnnBe
ms.date: 03/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareStation
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 27161
ms.assetid: eb164a9d-5538-4b6f-81ad-87e05d92eca5
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 380473cfb819adf881364fd2e6d50f5983ef0da8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564377"
---
# <a name="configure-and-install-retail-hardware-station"></a><span data-ttu-id="7e7c0-104">Retail ハードウェア ステーションのコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="7e7c0-104">Configure and install Retail hardware station</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e7c0-105">このトピックでは、セルフサービスを使用して Retail ハードウェア ステーションを構成、ダウンロード、およびインストールする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-105">This topic explains how to configure, download, and install Retail hardware station by using self-service.</span></span> <span data-ttu-id="7e7c0-106">また、Retail ハードウェア ステーションをアンインストールする方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-106">It also explains how to uninstall Retail hardware station.</span></span>

## <a name="download-retail-hardware-station-by-using-self-service"></a><span data-ttu-id="7e7c0-107">セルフサービスを使い、Retail ハードウェア ステーションをダウンロード</span><span class="sxs-lookup"><span data-stu-id="7e7c0-107">Download Retail hardware station by using self-service</span></span>

### <a name="configure-a-new-retail-hardware-station-profile-start-here-for-dynamics-365-for-retail-february-2016"></a><span data-ttu-id="7e7c0-108">新しい Retail ハードウェア ステーション プロファイルをコンフィギュレーションする (Dynamics 365 for Retail、2016 年 2 月)</span><span class="sxs-lookup"><span data-stu-id="7e7c0-108">Configure a new Retail hardware station profile (Start here for Dynamics 365 for Retail, February 2016)</span></span>

> [!NOTE]
> <span data-ttu-id="7e7c0-109">このステップは、Microsoft Dynamics 365 for Retail の February 2016 (RTW) バージョンを実行している場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-109">This procedure is required only if you're running the February 2016 (RTW) version of Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="7e7c0-110">バージョン 1611 を実行している場合は、次の手順で開始します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-110">If you're running version 1611, start with the next procedure.</span></span>

1. <span data-ttu-id="7e7c0-111">Microsoft Azure Active Directory (Azure AD) 証明書を使用して、小売用バックオフィスまたは Microsoft Dynamics 365 for Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-111">Use your Microsoft Azure Active Directory (Azure AD) credentials to sign in to the Retail headquarters or Microsoft Dynamics 365 for Retail trial.</span></span>
2. <span data-ttu-id="7e7c0-112">**ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア ステーションのプロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-112">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware station profiles**.</span></span>
3. <span data-ttu-id="7e7c0-113">**ハードウェア ステーションのプロファイル**ページの、アクション ペインで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-113">On the **Hardware station profile** page, on the Action Pane, select **New**.</span></span>
4. <span data-ttu-id="7e7c0-114">**ハードウェア ステーション ID** フィールドに、一意なハードウェア ステーション ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-114">In the **Hardware station ID** field, enter a unique hardware station ID.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-115">**名前** フィールドは、固有のハードウェア ステーション プロファイルの説明に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-115">The **Name** field is used for a description of the unique hardware station profile.</span></span>

5. <span data-ttu-id="7e7c0-116">該当するフィールドにポート番号を入力し、ハードウェア プロファイルを選択してパッケージ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-116">In the appropriate fields, enter the port number, select a hardware profile, and select a package name.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-117">1 つのハードウェア ステーション パッケージのみが、デモ データが読み込まれた環境に提供されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-117">Only one hardware station package is provided for an environment that has been loaded with demo data.</span></span>

6. <span data-ttu-id="7e7c0-118">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-118">On the Action Pane, select **Save**.</span></span>

### <a name="configure-a-new-retail-hardware-station-start-here-for-dynamics-365-for-retail-version-1611-or-later"></a><span data-ttu-id="7e7c0-119">新しい Retail ハードウェア ステーションをコンフィギュレーションする (Dynamics 365 for Retail、バージョン 1611 以降)</span><span class="sxs-lookup"><span data-stu-id="7e7c0-119">Configure a new Retail hardware station (Start here for Dynamics 365 for Retail, version 1611 or later)</span></span>

> [!NOTE]
> <span data-ttu-id="7e7c0-120">Dynamics 365 for Retail(初回リリース) のアップグレードされていないバージョンである 2016 年 2 月を実行している場合は、手順 6 はスキップします。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-120">If you're running the February 2016, non-upgraded version of Dynamics 365 for Retail (Initial release), skip step 6.</span></span>

1. <span data-ttu-id="7e7c0-121">Azure AD 証明書を使用して、Dynamics 365 for Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-121">Use your Azure AD credentials to sign in to the Dynamics 365 for Retail trial.</span></span>
2. <span data-ttu-id="7e7c0-122">**ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗**に移動します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-122">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="7e7c0-123">**すべての小売店舗**ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-123">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="7e7c0-124">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-124">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-125">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-125">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="7e7c0-126">**小売店舗詳細**ページや、**ハードウェア ステーション**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-126">On the **Retail store details** page, on the **Hardware stations** FastTab, select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-127">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-127">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="7e7c0-128">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-128">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="7e7c0-129">**ハードウェア ステーション タイプ** フィールドで、**共有**を選択して、このハードウェア ステーションが Internet Information Services (IIS)、外部の販売時点管理 (POS) システムによって使用されるインストール済みのハードウェア ステーションであることを示します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-129">In the **Hardware station type** field, select **Shared** to indicate that this hardware station is an Internet Information Services (IIS), installed hardware station that will be used by external point of sale (POS) systems.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-130">値 **Shared** は、インストールが真に共有されているハードウェア ステーションのインストールであり、HTTPS 通信を介して機能することを示します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-130">The value **Shared** signifies that the installation is a truly shared hardware station installation, and that it works through HTTPS communication.</span></span> <span data-ttu-id="7e7c0-131">対照的に、**専用**という値はハードウェア ステーションが Retail Modern POS の一部であり、プロセス間通信を通じて機能していることを示します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-131">By contrast, the value **Dedicated** signifies that the hardware station is a part of Retail Modern POS, and that it works through inter-process communication.</span></span>

6. <span data-ttu-id="7e7c0-132">実行しているバージョンに応じて、次のいずれかのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-132">Follow one of these steps, depending on the version that you're running:</span></span>

    - <span data-ttu-id="7e7c0-133">**バージョン 1611 の場合:** 該当するフィールドにポート番号を入力し、ハードウェア プロファイルを選択してパッケージ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-133">**For version 1611:** In the appropriate fields, enter the port number, select a hardware profile, and select a package name.</span></span>

        > [!NOTE]
        > <span data-ttu-id="7e7c0-134">環境の作成時、1 つのハードウェア ステーション パッケージのみが、デモ データが読み込まれた環境に提供されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-134">Only one hardware station package is provided for an environment that has been loaded with demo data, at environment creation time.</span></span>

    - <span data-ttu-id="7e7c0-135">**2016 年 2 月バージョンの場合:** ハードウェア ステーションのプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-135">**For the February 2016 version:** Select a hardware station profile.</span></span>

7. <span data-ttu-id="7e7c0-136">Retail ハードウェア ステーションをインストールするコンピュータのホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-136">Enter the host name of the computer that you're installing Retail hardware station on.</span></span> <span data-ttu-id="7e7c0-137">また、商業口座情報のコンピューターに関連付けられている電子決済 (EFT) ターミナル ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-137">Additionally, enter the electronic funds transfer (EFT) terminal ID that is associated with that computer for merchant account information.</span></span>

### <a name="download-the-retail-hardware-station-installer"></a><span data-ttu-id="7e7c0-138">Retail ハードウェア ステーション インストーラーをダウンロード</span><span class="sxs-lookup"><span data-stu-id="7e7c0-138">Download the Retail hardware station installer</span></span>

1. <span data-ttu-id="7e7c0-139">Azure AD 証明書を使用して、小売用バックオフィスまたは Dynamics 365 for Retail トライアル版にサインインします。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-139">Use your Azure AD credentials to sign in to the Retail headquarters or Dynamics 365 for Retail trial.</span></span>
2. <span data-ttu-id="7e7c0-140">**ようこそ**ページで、左上隅のメニューを使用して、**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗**に移動します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-140">On the **Welcome** page, use the menu in the upper left to go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
3. <span data-ttu-id="7e7c0-141">**すべての小売店舗**ページで、目的の店舗の小売チャネル ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-141">On the **All retail stores** page, select the retail channel ID of the desired store.</span></span> <span data-ttu-id="7e7c0-142">店舗の詳細ビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-142">The details view for the store appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-143">Houston 店舗は、デモ データ内の最も十分に用意されたストアです。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-143">The Houston store is the most thoroughly prepared store in the demo data.</span></span>

4. <span data-ttu-id="7e7c0-144">**小売店舗詳細**ページで、**ハードウェア ステーション**クイック タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-144">On the **Retail store details** page, select the **Hardware stations** FastTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-145">選択した店舗に使用される Retail Server URL は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-145">The Retail Server URL that is used for the selected store is read-only.</span></span> <span data-ttu-id="7e7c0-146">この URL は、Retail ハードウェア ステーションのインストール時に重要になります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-146">This URL will be important during the installation of Retail hardware station.</span></span>

5. <span data-ttu-id="7e7c0-147">ダウンロードするハードウェア ステーションを選択し、**ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-147">Select the hardware station to download, and then select **Download**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="7e7c0-148">ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-148">Browsers might block the download pop-up that is generated.</span></span> <span data-ttu-id="7e7c0-149">**1 回許可** または **このサイトのオプション** &gt; **常に許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-149">You must select either **Allow once** or **Options for this site** &gt; **Always allow**.</span></span> <span data-ttu-id="7e7c0-150">その後、再度 **ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-150">Then select **Download** again.</span></span>
    > - <span data-ttu-id="7e7c0-151">ハードウェア ステーションのプロファイルに基づいて、適切なパッケージがダウンロード用に自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-151">The correct installation package is automatically selected for download, based on the hardware station profile.</span></span>

6. <span data-ttu-id="7e7c0-152">Internet Explorer ウィンドウの下部に表示される通知バーで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-152">On the Notification bar that appears at the bottom of the Internet Explorer window, select **Save**.</span></span> <span data-ttu-id="7e7c0-153">(通知バーは、他のブラウザでは別の場所に表示される場合があります。)</span><span class="sxs-lookup"><span data-stu-id="7e7c0-153">(The Notification bar might appear in a different place in other browsers.)</span></span>
7. <span data-ttu-id="7e7c0-154">セットアップ インストーラが保存されたら、通知バーの、**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-154">After the setup installer has been saved, on the Notification bar, select **Run**.</span></span> <span data-ttu-id="7e7c0-155">(この手順はブラウザによって異なる場合があります。)</span><span class="sxs-lookup"><span data-stu-id="7e7c0-155">(This step might differ, depending on your browser.)</span></span>

### <a name="run-the-installer"></a><span data-ttu-id="7e7c0-156">インストーラーを実行</span><span class="sxs-lookup"><span data-stu-id="7e7c0-156">Run the installer</span></span>

> [!NOTE]
> <span data-ttu-id="7e7c0-157">Retail ハードウェア ステーション インストーラーを実行する前に、すべての[システム要件](../fin-and-ops/get-started/system-requirements.md)が満たされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-157">Before you run the Retail hardware station installer, make sure that all [system requirements](../fin-and-ops/get-started/system-requirements.md) are met.</span></span>

<span data-ttu-id="7e7c0-158">Retail ハードウェア ステーション インストーラーは、まず関連付けられているファイルを抽出し、インストールを開始します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-158">The Retail hardware station installer first extracts the associated files and then begins the installation.</span></span>

1. <span data-ttu-id="7e7c0-159">インストーラーは、すべての前提条件が満たされていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-159">The installer validates that all prerequisites are met.</span></span> <span data-ttu-id="7e7c0-160">サイドローディング キーが必要な場合は、インストーラーがそれを要求します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-160">If a sideloading key is required, the installer requests it.</span></span> <span data-ttu-id="7e7c0-161">このキーは、各デバイスの **一般** の下にある**デバイス**ページにあります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-161">This key is found on the **Devices** page for each device, under **General**.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="7e7c0-162">システムの再起動が必要な場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-162">If a system restart is required, the installer informs you of this requirement but can continue the installation.</span></span>
    > - <span data-ttu-id="7e7c0-163">小売販売時点管理の Object Linking and Embedding (OPOS) 標準に基づいたハードウェアを使用する前に、OPOS コモン コントロール オブジェクトをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-163">Before you can use hardware that is based on the Object Linking and Embedding for Retail Point of Sale (OPOS) standard, the OPOS Common Control Objects must be installed.</span></span> <span data-ttu-id="7e7c0-164">インストールされていない場合は、インストーラーでこれに関する要件を確認できますが、通常インストールを続行できます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-164">If they aren't installed, the installer informs you of this requirement but can continue the installation.</span></span>

2. <span data-ttu-id="7e7c0-165">Retail Server URL を入力し (たとえば、`https://MyCompanyNameret.axcloud.dynamics.com/Commerce`)、**次** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-165">Enter the Retail Server URL (for example, `https://MyCompanyNameret.axcloud.dynamics.com/Commerce`), and then select **Next**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-166">Retail Server の URL は **小売店舗詳細** ページ上の **ハードウェア ステーション** クイック タブの最上部で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-166">You can find the Retail Server URL at the top of the **Hardware stations** FastTab on the **Retail store details** page.</span></span>

3. <span data-ttu-id="7e7c0-167">HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-167">Select a valid Secure Sockets Layer (SSL) certificate to use for HTTPS communication.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-168">証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-168">The certificate must use private key storage, and server authentication must be listed in the enhanced key usage property.</span></span> <span data-ttu-id="7e7c0-169">また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-169">Additionally, the certificate must be trusted locally, and it can't be expired.</span></span> <span data-ttu-id="7e7c0-170">ローカル コンピューターの個人用証明書格納場所に保存する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-170">It must be stored in the personal certificate store location on the local computer.</span></span>

4. <span data-ttu-id="7e7c0-171">次のページでは、IIS アプリケーション プールで使用する必要があるユーザーを要求します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-171">The next page requests the user that should be used for the IIS application pool.</span></span> <span data-ttu-id="7e7c0-172">バージョン 1611 以降の既定では、インストーラーが自動的にサービス アカウントを作成して使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-172">By default in version 1611 and later, the installer can automatically create and use a service account.</span></span> <span data-ttu-id="7e7c0-173">ドメインを使用している場合や特定のコントロールが必要な場合は、チェックボックスをオフにして、アプリケーション プールが実行するユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-173">If you're on a domain or require more specific controls, clear the check box, and then enter the user name and password that the application pool should run under.</span></span>
5. <span data-ttu-id="7e7c0-174">使用する HTTPS ポートを入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-174">Enter the HTTPS port to use.</span></span>

    > [!NOTE]
    > - <span data-ttu-id="7e7c0-175">Dynamics 365 for Retail で HTTPS ポートを検索することができます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-175">You can find the HTTPS port in Dynamics 365 for Retail.</span></span> <span data-ttu-id="7e7c0-176">(このトピックで前述したコンフィギュレーションの指示を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-176">(See the configuration instructions earlier in this topic).</span></span>
    > - <span data-ttu-id="7e7c0-177">インストーラーは自動的にホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-177">The installer automatically enters the host name.</span></span> <span data-ttu-id="7e7c0-178">何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更できます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-178">If, for any reason, you must change the host name for the installation, you can change it here.</span></span> <span data-ttu-id="7e7c0-179">ホスト名はシステムの完全修飾ドメイン名 (FQDN) でなければなりません。また、選択したハードウェア ステーション エントリの **ホスト名**フィールドに入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-179">The host name must be the fully-qualified domain name (FQDN) of the system, and it must be entered in the **Host name** field for the selected hardware station entry.</span></span>

6. <span data-ttu-id="7e7c0-180">インストーラーは Retail ハードウェア ステーションをインストールし、インストールが成功したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-180">The installer installs Retail hardware station and then indicates whether the installation was successful.</span></span>
7. <span data-ttu-id="7e7c0-181">インストールが完了したら、支払商社情報のインストール ツールが起動します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-181">When the installation is completed, the Install merchant information tool starts.</span></span> <span data-ttu-id="7e7c0-182">このインストーラーは、環境に接続し、選択したハードウェア ステーションの販売者の口座情報 (EFT IDなど) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-182">This installer connects to the environment and installs the merchant account information (such as the EFT ID) for the selected hardware station.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-183">インストールされているハードウェア ステーションが支払に関連する作業の使用されない場合、残りの手順を終了せずに**商社の情報をインストール**ウィンドウを閉じません。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-183">If the hardware station that was installed won't be used for payment-related work, don't close the **Install merchant information** window without completing the remaining steps.</span></span> <span data-ttu-id="7e7c0-184">このインストールが正常に完了しないと、ハードウェア ステーションは機能しません。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-184">The hardware station won't work unless this installation is successfully completed.</span></span>

8. <span data-ttu-id="7e7c0-185">Install マーチャント情報ツールは、Azure AD 資格情報を要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-185">The Install merchant information tool might request Azure AD credentials.</span></span> <span data-ttu-id="7e7c0-186">Retail ハードウェア ステーションをインストールするユーザーの Azure AD 資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-186">Enter the Azure AD credentials of the user who is installing Retail hardware station.</span></span>
9. <span data-ttu-id="7e7c0-187">Retail Server URL は、Retail ハードウェア ステーションのインストールによって決定され、自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-187">The Retail Server URL is determined through the Retail hardware station installation and is entered automatically.</span></span> <span data-ttu-id="7e7c0-188">インストーラーは、この URL を使用して、ユーザーがアドレス帳を介して接続している店舗のリストをロードします。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-188">The installer uses this URL to load the list of stores that the user is connected to via the address book.</span></span>
10. <span data-ttu-id="7e7c0-189">ハードウェア ステーションがインストールされた小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-189">Select the retail store that the hardware station was installed for.</span></span>
11. <span data-ttu-id="7e7c0-190">現在のコンピューターにインストールされていたハードウェア ステーションに一致するハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-190">Select the hardware profile that matches the hardware station that was installed on the current computer.</span></span>
12. <span data-ttu-id="7e7c0-191">現在のコンピューターおよび Dynamics 365 for Retail で既に完了している Retail ハードウェア ステーション構成に基づいて、ホスト名と EFT ターミナル ID が正しことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-191">Verify that the host names and EFT terminal IDs are correct, based on the current computer and the Retail hardware station configuration that has already been completed in Dynamics 365 for Retail.</span></span> <span data-ttu-id="7e7c0-192">この情報を検証した後、**インストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-192">After you've verified this information, select **Install**.</span></span>
13. <span data-ttu-id="7e7c0-193">商業口座情報が正しくインストールされたことを示すメッセージが表示されたら**閉じる** ボタンを選択してインストーラーを終了します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-193">When you receive a message that states that the merchant account information was installed correctly, exit the installer by selecting the **Close** button.</span></span>

## <a name="help-secure-retail-hardware-station"></a><span data-ttu-id="7e7c0-194">Retail ハードウェア ステーションのセキュリティを強化する</span><span class="sxs-lookup"><span data-stu-id="7e7c0-194">Help secure Retail hardware station</span></span>

<span data-ttu-id="7e7c0-195">現在のセキュリティ基準では、実稼動環境で次のオプションを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-195">Current security standards state that the following options should be set in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="7e7c0-196">ハードウェア ステーションのインストーラーは、セルフサービスによるインストールの一部として、これらのレジストリの編集を自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-196">The hardware station installer automatically makes these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="7e7c0-197">SSL を無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-197">SSL should be disabled.</span></span>
- <span data-ttu-id="7e7c0-198">Transport Layer Security (TLS) version 1.2 (または現行最新バージョン) のみを有効にして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-198">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e7c0-199">既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効になります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-199">By default, SSL and all version of TLS except TLS 1.2 are disabled.</span></span> <span data-ttu-id="7e7c0-200">これらを値の編集または有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-200">To edit or enable these values, follow these steps:</span></span>
    >
    > 1. <span data-ttu-id="7e7c0-201">Windows ロゴキーと R キーを同時に押して、**実行**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-201">Press the Windows logo key+R to open a **Run** window.</span></span>
    > 2. <span data-ttu-id="7e7c0-202">**開く**フィールドに、**Regedit** と入力してから **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-202">In the **Open** field, type **Regedit**, and then select **OK**.</span></span>
    > 3. <span data-ttu-id="7e7c0-203">**ユーザー アカウント コントロール** ウィンドウが現われたら、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-203">If a **User Account Control** window appears, select **Yes**.</span></span>
    > 4. <span data-ttu-id="7e7c0-204">新しい**レジストリ エディター** ウィンドウで、**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-204">In the new **Registry Editor** window, go to **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\SecurityProviders\\SCHANNEL\\Protocols**.</span></span> <span data-ttu-id="7e7c0-205">TLS 1.2 のみを有効にするために、以下のキーは自動的に挿入されています:</span><span class="sxs-lookup"><span data-stu-id="7e7c0-205">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>
    >
    >    - <span data-ttu-id="7e7c0-206">TLS 1.2\\Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="7e7c0-206">TLS 1.2\\Server:Enabled=1</span></span>
    >    - <span data-ttu-id="7e7c0-207">TLS 1.2\\Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-207">TLS 1.2\\Server:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="7e7c0-208">TLS 1.2\\Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="7e7c0-208">TLS 1.2\\Client:Enabled=1</span></span>
    >    - <span data-ttu-id="7e7c0-209">TLS 1.2\\Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-209">TLS 1.2\\Client:DisabledByDefault=0</span></span>
    >    - <span data-ttu-id="7e7c0-210">TLS 1.1\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-210">TLS 1.1\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-211">TLS 1.1\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-211">TLS 1.1\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-212">TLS 1.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-212">TLS 1.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-213">TLS 1.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-213">TLS 1.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-214">SSL 3.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-214">SSL 3.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-215">SSL 3.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-215">SSL 3.0\\Client:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-216">SSL 2.0\\Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-216">SSL 2.0\\Server:Enabled=0</span></span>
    >    - <span data-ttu-id="7e7c0-217">SSL 2.0\\Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="7e7c0-217">SSL 2.0\\Client:Enabled=0</span></span>

- <span data-ttu-id="7e7c0-218">知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-218">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="7e7c0-219">クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-219">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="7e7c0-220">信頼された証明機関のみ、Retail ハードウェア ステーションを実行するコンピューター上で使用される証明書の調達に使用されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-220">Only trusted certificate authorities should be used to procure certificates that will be used on computers that run Retail hardware station.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="7e7c0-221">ほどんどの一般的な下位セキュリティ ソフトウェアおよびサービスはすべての下位セキュリティ基準が無効になった後に動作を停止します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-221">Most common, lower-security software and services will stop working after all lower-security standards are disabled.</span></span> <span data-ttu-id="7e7c0-222">それらを再使用するには、前述のレジストリ キーに移動し、**有効** キーを **0** から **1** に設定します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-222">To use them again, go to the preceding registry keys, and set the **Enabled** key from **0** to **1**.</span></span>
> - <span data-ttu-id="7e7c0-223">IIS と Payment Card Industry (PCI) の要件向けのセキュリティ ガイドラインを確認することが重要です。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-223">It's critical that you review security guidelines for IIS and Payment Card Industry (PCI) requirements.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="7e7c0-224">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="7e7c0-224">Troubleshooting</span></span>

### <a name="retail-modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="7e7c0-225">Retail Modern POS は、選択リストにあるハードウェア ステーションを検出できますが、ペアリングを完了することはできません</span><span class="sxs-lookup"><span data-stu-id="7e7c0-225">Retail Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="7e7c0-226">**ソリューション:** 以下の潜在的障害ポイントを確認してください:</span><span class="sxs-lookup"><span data-stu-id="7e7c0-226">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="7e7c0-227">Retail Modern POS を実行しているコンピュータは、Retail hardware station を実行しているコンピュータで使用される証明書を信頼します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-227">The computer that is running Retail Modern POS trusts the certificate that is used on the computer that runs Retail hardware station.</span></span>

    - <span data-ttu-id="7e7c0-228">Web ブラウザーでこの設定を確認するには、次のURL `https://<Computer Name>:<Port Number>/HardwareStation/ping` に移動します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-228">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>
    - <span data-ttu-id="7e7c0-229">この URL は ping を使用してコンピュータにアクセスできるかどうかを確認し、ブラウザは証明書が信頼できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-229">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="7e7c0-230">(たとえば、Internet Explorer ではカギのシンボルがアドレス バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-230">(For example, in Internet Explorer, a lock symbol appears in the address bar.</span></span> <span data-ttu-id="7e7c0-231">このシンボルを選択すると、Internet Explorer は証明書が現在信頼されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-231">When you select this symbol, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="7e7c0-232">表示される証明書の詳細を見ることで、ローカル コンピュータに証明書をインストールできます)。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-232">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="7e7c0-233">Retail ハードウェア ステーションを実行するコンピュータで、ハードウェア ステーションで使用されるポートはファイアウォールで開かれます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-233">On the computer that runs Retail hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="7e7c0-234">小売ハードウェア ステーションのインストールの最後に実行される支払商社情報インストール ツールを使用して、小売ハードウェア ステーションに支払商社情報が正しくインストールされます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-234">Retail hardware station has properly installed merchant account information through the Install merchant information tool that runs at the end of the Retail hardware station installer.</span></span>

### <a name="retail-modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="7e7c0-235">Retail Modern POS が選択リストにあるハードウェア ステーションを検出できない</span><span class="sxs-lookup"><span data-stu-id="7e7c0-235">Retail Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="7e7c0-236">**ソリューション:** 次の要素のいずれかによりこの問題が生じることがあり得ます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-236">**Solution:** Any one of the following factors can cause this issue:</span></span>

- <span data-ttu-id="7e7c0-237">小売ハードウェア ステーションが小売用バックオフィスに正しく設定されていない。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-237">Retail hardware station hasn't been set up correctly in Retail headquarters.</span></span> <span data-ttu-id="7e7c0-238">このトピックで説明した手順を使用して、ハードウェア ステーションのプロファイルとハードウェア ステーションが正しく入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-238">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="7e7c0-239">チャンネル構成を更新するジョブが実行されていません。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-239">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="7e7c0-240">この場合、チャンネル構成用に 1070 のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-240">In this case, run the 1070 job for channel configuration.</span></span>
- <span data-ttu-id="7e7c0-241">そのコンピューターからハードウェア ステーションにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-241">The hardware station isn't accessible from that computer.</span></span> <span data-ttu-id="7e7c0-242">Web ブラウザーからハードウェア ステーション URL ping テストを利用できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-242">Verify that the hardware station URL ping test is accessible from a web browser.</span></span> <span data-ttu-id="7e7c0-243">この URL は、ハードウェア ステーション インストーラーの最後にあり、`https://<Computer Name>:<Port Number>/HardwareStation/ping` の形式です</span><span class="sxs-lookup"><span data-stu-id="7e7c0-243">This URL can be found at the end of the hardware station installer and is in the following form: `https://<Computer Name>:<Port Number>/HardwareStation/ping`</span></span>

## <a name="uninstall-retail-hardware-station"></a><span data-ttu-id="7e7c0-244">Retail ハードウェア ステーションのアンインストール</span><span class="sxs-lookup"><span data-stu-id="7e7c0-244">Uninstall Retail hardware station</span></span>

<span data-ttu-id="7e7c0-245">Microsoft Windows でコントロール パネルを使用して Retail ハードウェア ステーションをアンインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-245">You can use Control Panel in Microsoft Windows to uninstall Retail hardware station.</span></span>

1. <span data-ttu-id="7e7c0-246">Windows ロゴ キーを押し、検索ボックスに**コントロール パネル**と入力します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-246">Press the Windows logo key, and then, in the search box, type **Control Panel**.</span></span> <span data-ttu-id="7e7c0-247">検索結果の一覧で、**コントロール パネル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-247">In the list of search results, select **Control Panel**.</span></span>
2. <span data-ttu-id="7e7c0-248">コントロール パネルで、**プログラム** &gt; **プログラムのアンインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-248">In Control Panel, select **Programs** &gt; **Uninstall a program**.</span></span> <span data-ttu-id="7e7c0-249">**プログラムと機能** ウィンドウが開きます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-249">The **Programs and Features** window opens.</span></span>
3. <span data-ttu-id="7e7c0-250">**Retail ハードウェア ステーション用 Microsoft Dynamics 365 for Retail** を選択し、プログラムの一覧の上にある**アンインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-250">Select **Microsoft Dynamics 365 for Retail for Retail hardware station**, and then select **Uninstall** above the list of programs.</span></span>
4. <span data-ttu-id="7e7c0-251">アンインストールがプログラムの削除を完了するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="7e7c0-251">Wait for the uninstaller to finish removing the program.</span></span>

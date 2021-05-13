---
title: Android および iOS での POS ハイブリッド アプリのセットアップ
description: このトピックでは、Android および iOS で POS ハイブリッド アプリをセットアップする方法を説明します。
author: mugunthanm
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-10-29
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 737c36e3b15c586b6e6c8ff982a61c90802b6919
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937078"
---
# <a name="set-up-pos-hybrid-app-on-android-and-ios"></a><span data-ttu-id="f9bd3-103">Android および iOS での POS ハイブリッド アプリのセットアップ</span><span class="sxs-lookup"><span data-stu-id="f9bd3-103">Set up POS hybrid app on Android and iOS</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9bd3-104">このトピックでは、Android および iOS デバイスで Retail POS ハイブリッド アプリを構築して実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-104">This topic shows how to build and run the Retail POS hybrid app on Android and iOS devices.</span></span> 

## <a name="overview"></a><span data-ttu-id="f9bd3-105">概要</span><span class="sxs-lookup"><span data-stu-id="f9bd3-105">Overview</span></span>

<span data-ttu-id="f9bd3-106">Retail ハイブリッド アプリは、[Xamarin](/xamarin/) を使用して構築されたシェルです。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-106">Retail hybrid app is shell built using [Xamarin](/xamarin/).</span></span> <span data-ttu-id="f9bd3-107">シェル内は、クラウド POS を読み込む Web ビュー コントローラーになっています。これは、このアプリケーションの設定で指定される Commerce Scale Unit URL に基づきます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-107">Inside the shell is a Web view controller that loads the cloud POS, which is based on the Commerce Scale Unit URL specified in the settings of this app.</span></span> <span data-ttu-id="f9bd3-108">これは、クラウド POS を内部で読み込む Android および iOS の Retail ハイブリッド アプリケーション シェルです。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-108">This is a Retail hybrid app shell for Android and iOS which will internally load the Cloud POS.</span></span> <span data-ttu-id="f9bd3-109">詳細については、[クラウド POS](/dynamics365/unified-operations/retail/mpos-or-cpos)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-109">For more information, see [Cloud POS](/dynamics365/unified-operations/retail/mpos-or-cpos).</span></span>

## <a name="development-tools"></a><span data-ttu-id="f9bd3-110">開発ツール</span><span class="sxs-lookup"><span data-stu-id="f9bd3-110">Development tools</span></span>
<span data-ttu-id="f9bd3-111">Retail ハイブリッド アプリは、Android および iOS スマートフォン プラットフォームをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-111">The Retail hybrid app supports the Android and iOS phone platforms.</span></span> <span data-ttu-id="f9bd3-112">このアプリは、Xamarin を使用して構築されています。つまり、開発用コンピューターには Xamarin をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-112">The app is built by using Xamarin, which means that you must install Xamarin on your development computer.</span></span> <span data-ttu-id="f9bd3-113">iOS アプリをビルドするには、Xamarin がインストールされている Mac が必要です。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-113">To build the iOS app, you must have a Mac that has Xamarin installed.</span></span> <span data-ttu-id="f9bd3-114">Microsoft Windows を実行しているコンピューターで Android および iOS の両方に対して開発を行うことができますが、Mac を使用して iOS プラットフォームのビルドを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-114">Although you can do development for both Android and iOS on a computer that runs Microsoft Windows, you must use a Mac to complete the build for the iOS platform.</span></span> <span data-ttu-id="f9bd3-115">Mac が共有チーム リソースである場合、ビルド処理のためだけ Mac を使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-115">If your Mac is a shared team resource, you might want to use a Mac just for the build process.</span></span> <span data-ttu-id="f9bd3-116">開発に使用するすべてのコンピューターに、Retail ソフトウェアの開発キット (Retail SDK) をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-116">You must copy the Retail software development kit (Retail SDK) on all the computers that you use for development.</span></span> <span data-ttu-id="f9bd3-117">Retail SDK は、「[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)」を使用してプロビジョニングされるすべての開発者 VM で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-117">The Retail SDK is available in all developer VMs that are provisioned for using [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/).</span></span>

<span data-ttu-id="f9bd3-118">Xamarin の詳細については、[Xamarin のドキュメント](/xamarin/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-118">For more information about Xamarin, see the [Xamarin documentation](/xamarin/).</span></span>

## <a name="set-up-and-install-xamarin-on-windows"></a><span data-ttu-id="f9bd3-119">Windows での Xamarin のセットアップとインストール</span><span class="sxs-lookup"><span data-stu-id="f9bd3-119">Set up and install Xamarin on Windows</span></span>

<span data-ttu-id="f9bd3-120">Windows で Xamarin をセットアップしてインストールするには、<https://docs.microsoft.com/xamarin/android/get-started/installation/windows> にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-120">To set up and install Xamarin on Windows, go to <https://docs.microsoft.com/xamarin/android/get-started/installation/windows>.</span></span>

### <a name="update-xamarin"></a><span data-ttu-id="f9bd3-121">Xamarin の更新</span><span class="sxs-lookup"><span data-stu-id="f9bd3-121">Update Xamarin</span></span>

> [!NOTE]
> <span data-ttu-id="f9bd3-122">Xamarin.Android SDK バージョン 10.0 未満の使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-122">We recommend that you use Xamarin.Android SDK version < 10.0.</span></span> 

<span data-ttu-id="f9bd3-123">Xamarin をインストールした後、最新の安定バージョンに更新する必要があります (Xamarin.Android SDK version は 10.0 未満でなければなりません)。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-123">After you've installed Xamarin, you must update it to the latest stable version (Xamarin.Android SDK version must be < 10.0).</span></span>

-   <span data-ttu-id="f9bd3-124">**Windows** - Microsoft Visual Studio で、**ツール** &gt; **オプション** &gt; **環境** &gt; **Xamarin** &gt; **その他** を順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-124">**Windows** - In Microsoft Visual Studio, click **Tools** &gt; **Options** &gt;**Environment** &gt; **Xamarin** &gt; **Other**.</span></span>
-   <span data-ttu-id="f9bd3-125">**Mac**: Xamarin Studio で、**更新の確認** &gt; **チャネルを更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-125">**Mac** - In Xamarin Studio, click **Check for Updates** &gt; **Update channel**.</span></span> <span data-ttu-id="f9bd3-126">このステップの詳細については、[更新チャンネルの変更](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-126">For more information about this step, see [Change the Updates Channel](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/).</span></span>

### <a name="build-the-android-retail-hybrid-app"></a><span data-ttu-id="f9bd3-127">Android Retail ハイブリッド アプリの構築</span><span class="sxs-lookup"><span data-stu-id="f9bd3-127">Build the Android Retail hybrid app</span></span>

> [!NOTE]
> <span data-ttu-id="f9bd3-128">Visual Studio 2019 以降を使用して Android アプリを構築することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-128">We recommend that you use Visual Studio 2019 or later to build the Android app.</span></span>

1. <span data-ttu-id="f9bd3-129">インストールが完了したら、Visual Studio を起動し、Microsoft アカウント (これは、Windows で使用するのと同じアカウント) を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-129">When installation is complete, launch Visual Studio and sign in with your Microsoft account (this is the same account that you use with Windows).</span></span> <span data-ttu-id="f9bd3-130">**ツール > オプション > Xamarin** または **ツール > オプション > Xamarin > その他** をクリックして、Xamarin の更新をチェックします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-130">Check for Xamarin updates by clicking **Tools > Options > Xamarin** or **Tools > Options > Xamarin > Other**.</span></span> <span data-ttu-id="f9bd3-131">ここには、**いますぐ確認** リンクがあります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-131">Here you'll find a **Check Now** link.</span></span> <span data-ttu-id="f9bd3-132">Xamarin のオプションが **ツール > オプション** に表示されない場合、インストールを確認するか、Visual Studio を再起動してみてください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-132">If you do not see an option for Xamarin in **Tools > Options**, review your installation, or try restarting Visual Studio.</span></span> <span data-ttu-id="f9bd3-133">**オプション** ダイアログ ボックスで Xamarin を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-133">You can also search for Xamarin in the **Options** dialog box.</span></span> <span data-ttu-id="f9bd3-134">必要な場合は、最新バージョンをダウンロードおよびインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-134">If needed, download and install the latest version.</span></span>
      
2.  <span data-ttu-id="f9bd3-135">Retail SDK フォルダーで、SampleExtensions\HybridApp\Android\solution を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-135">In the Retail SDK folder, open SampleExtensions\HybridApp\Android\solution.</span></span> <span data-ttu-id="f9bd3-136">エミュレーターを使用して構築および展開し、すべて正常に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-136">Build and deploy using the emulator and verify that everything appears as it should.</span></span>
  
3.  <span data-ttu-id="f9bd3-137">[Android 用 Visual Studio エミュレーター](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Android 用の Visual Studio エミュレーター") または Android 用のエミュレーターを使用して、POS ハイブリッド アプリを起動し、Commerce Scale Unit URL を入力して、保存します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-137">Using the [Visual Studio Emulator for Android](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Visual Studio Emulator for Android") or any emulator for Android, launch the POS hybrid app and enter the Commerce Scale Unit URL and save.</span></span>
  
4.  <span data-ttu-id="f9bd3-138">ログインして、デバイスをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-138">You should be able to sign in and activate the device.</span></span>

### <a name="build-the-ios-retail-hybrid-app"></a><span data-ttu-id="f9bd3-139">iOS Retail ハイブリッド アプリの構築</span><span class="sxs-lookup"><span data-stu-id="f9bd3-139">Build the iOS Retail hybrid app</span></span>

### <a name="connecting-to-a-mac"></a><span data-ttu-id="f9bd3-140">Mac に接続しています</span><span class="sxs-lookup"><span data-stu-id="f9bd3-140">Connecting to a Mac</span></span>

<span data-ttu-id="f9bd3-141">Windows で開発し、iOS アプリケーションを構築するためだけに Mac を使用している場合は、Windows と Mac を実行するコンピューターを接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-141">If you're developing on Windows and using the Mac just for building the iOS app then you must connect the computer that runs Windows and the Mac.</span></span> <span data-ttu-id="f9bd3-142">手順については、[Mac に接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-142">For instructions, see [Connecting to the Mac](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/).</span></span>

 ## <a name="set-up-and-install-xamarin-on-ios"></a><span data-ttu-id="f9bd3-143">iOS での Xamarin のセットアップとインストール</span><span class="sxs-lookup"><span data-stu-id="f9bd3-143">Set up and install Xamarin on iOS</span></span>

<span data-ttu-id="f9bd3-144">iOS で Xamarin をインストールに関する詳しい手順については、[Xamarin.iOS のインストール](/xamarin/ios/get-started/installation/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-144">For more detailed steps on installing Xamarin on iOS, refer to [Xamarin.iOS installation](/xamarin/ios/get-started/installation/).</span></span>

  1.  <span data-ttu-id="f9bd3-145"><https://developer.apple.com/xcode/> から Xcode をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-145">Download and install Xcode from <https://developer.apple.com/xcode/>.</span></span> <span data-ttu-id="f9bd3-146">[Xcode へのアカウントの追加](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com) で説明されている手順を使用して Apple ID を追加します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-146">Add your Apple ID using the instructions described in [Adding your account to Xcode](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com).</span></span>
  
  2.  <span data-ttu-id="f9bd3-147">[Xamarin.iOS のインストールおよび構成](https://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com) の手順に従って Xamarin をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-147">Download and install Xamarin by following the instructions in [Installing and configuring Xamarin.iOS](https://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com).</span></span>
  
  3.  <span data-ttu-id="f9bd3-148">Windows と Mac コンピューターの両方で Xamarin のインストールを完了したら、[Mac への接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-148">When you have completed installing Xamarin on both the Windows and Mac computers, follow the instructions in [Connecting to the Mac](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com).</span></span> <span data-ttu-id="f9bd3-149">これを行ったら、Windows コンピューターの Visual Studio から iOS および Mac を操作することができます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-149">After you do this, you can work with iOS and Mac from Visual Studio on the Windows computer.</span></span>
  
  ### <a name="build-the-ios-retail-hybrid-app"></a><span data-ttu-id="f9bd3-150">iOS Retail ハイブリッド アプリの構築</span><span class="sxs-lookup"><span data-stu-id="f9bd3-150">Build the iOS Retail hybrid app</span></span>
  
  1.  <span data-ttu-id="f9bd3-151">Retail SDK フォルダーで、SampleExtensions\HybridApp\iOS\solution を開きます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-151">In the Retail SDK folder, open SampleExtensions\HybridApp\iOS\solution.</span></span>
      <span data-ttu-id="f9bd3-152">Mac に接続して Visual Studio でアプリケーションを構築したら、iOS デバイスの種類を選択し、選択したデバイス上にアプリケーションを展開します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-152">After connecting to the Mac and building the application in Visual Studio, select the iOS device type and deploy the app on the selected device.</span></span>
      
       ![展開用 POS iOS アプリ VS 設定](./media/iOSSetting.png)
      
  2.  <span data-ttu-id="f9bd3-154">エミュレーターを使用して、**設定 > RetailMPOS** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-154">Using the Emulator, go to **Settings > RetailMPOS**.</span></span> <span data-ttu-id="f9bd3-155">Commerce Scale Unit URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-155">Enter the Commerce Scale Unit URL.</span></span>
      
       ![POS iOS アプリ設定](./media/iOSApp.png)
      
       ![RS URL の POS iOS アプリ設定](./media/iOSRSURL.png)
      
  3.  <span data-ttu-id="f9bd3-158">MPOS アプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-158">Launch the MPOS app.</span></span> <span data-ttu-id="f9bd3-159">ログインして、デバイスをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-159">You should be able to sign in and activate the device.</span></span>
  
## <a name="dedicated-hardware-station-support-for-the-hybrid-android-app"></a><span data-ttu-id="f9bd3-160">ハイブリッド Android アプリケーションに対応した専用ハードウェアステーション</span><span class="sxs-lookup"><span data-stu-id="f9bd3-160">Dedicated hardware station support for the hybrid Android app</span></span>
  
<span data-ttu-id="f9bd3-161">リリース8.1.3以降、専用ハードウェアステーションがハイブリッド Android アプリケーションに対応していします。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-161">Starting in release 8.1.3, dedicated hardware station support has been added to the hybrid Android app.</span></span> <span data-ttu-id="f9bd3-162">Retail Modern POS が周辺機器へのビルトインサポートしているのと同様に、 Android アプリは 専用のハードウェアステーションを使用して、IISベースのハードウェアステーションの配置をせずとも周辺機器に接続することができます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-162">In the same way that the Retail Modern POS has built-in support for peripheral devices, the Android app can also use the dedicated hardware station to connect to peripherals without needing to deploy an IIS-based hardware station.</span></span>
<span data-ttu-id="f9bd3-163">初期状態では、ハイブリッド Android アプリでは、ネットワーク接続経由での支払ターミナルとレシートプリンターの使用に対応しています。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-163">Out of the box, the hybrid Android app supports using payment terminals and receipt printers over network connections.</span></span> <span data-ttu-id="f9bd3-164">通常はネットワークを介したデバイスとの通信には、製造元によって指定された独自の通信プロトコルを順守する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-164">Communicating with devices over a network typically requires adherence to a proprietary communication protocol specified by the manufacturer.</span></span> <span data-ttu-id="f9bd3-165">ハイブリッド Android アプリの場合、標準の組み込み機能として、Adyen と Epson レシート プリンターに対応した Dynamics 365 Payment Connector が用意されています。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-165">For the hybrid Android app, out-of-the- box integrations are provided for the Dynamics 365 Payment Connector for Adyen and Epson receipt printers.</span></span> 

### <a name="out-of-the-box-supported-devices"></a><span data-ttu-id="f9bd3-166">初期設定で対応しているデバイス</span><span class="sxs-lookup"><span data-stu-id="f9bd3-166">Out-of-the-box supported devices</span></span>

| <span data-ttu-id="f9bd3-167">デバイス</span><span class="sxs-lookup"><span data-stu-id="f9bd3-167">Device</span></span> | <span data-ttu-id="f9bd3-168">説明</span><span class="sxs-lookup"><span data-stu-id="f9bd3-168">Description</span></span> |
| --- | --- |
| <span data-ttu-id="f9bd3-169">支払端末</span><span class="sxs-lookup"><span data-stu-id="f9bd3-169">Payment terminals</span></span> | <span data-ttu-id="f9bd3-170">Dynamics 365 Payment Connector for Adyen を介して [ADYEN支払ターミナルAPI](https://www.adyen.com/blog/introducing-the-terminal-api) が対応しているもの。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-170">Any supported by the [Adyen Payment Terminal API](https://www.adyen.com/blog/introducing-the-terminal-api) through the Dynamics 365 Payment Connector for Adyen.</span></span> |
| <span data-ttu-id="f9bd3-171">レシート プリンター</span><span class="sxs-lookup"><span data-stu-id="f9bd3-171">Receipt printer</span></span> | <span data-ttu-id="f9bd3-172">Epson SOAP HTTPインターフェイスに対応しているネットワーク対応のEpsonプリンター。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-172">Network-enabled Epson printers that support the Epson SOAP HTTP interface.</span></span><p><span data-ttu-id="f9bd3-173">ネットワーク対応 Star Micronics プリンター。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-173">Network-enabled Star Micronics printers.</span></span></p> |
| <span data-ttu-id="f9bd3-174">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="f9bd3-174">Cash drawer</span></span> | <span data-ttu-id="f9bd3-175">Dynamics 365 Commerce バージョン 10.0.8 での導入: ドロワー キック (d/k) ポートを介してネットワーク対応プリンターに接続されたキャッシュ ドロワー。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-175">Introduced in Dynamics 365 Commerce version 10.0.8: Cash drawers that are connected to network-enabled printers via the drawer kick (d/k) port.</span></span> |

<span data-ttu-id="f9bd3-176">その他の支払プロセッサや周辺機器への対応は、Payments および Hardware SDKs を通して ISVs から実装することができます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-176">Support for other payment processors and peripheral devices can be implemented by ISVs through the Payments and Hardware SDKs.</span></span> 

### <a name="set-up-peripherals-to-work-with-the-hybrid-android-app"></a><span data-ttu-id="f9bd3-177">周辺機器をハイブリッド Android アプリと連係させるための設定を行います</span><span class="sxs-lookup"><span data-stu-id="f9bd3-177">Set up peripherals to work with the hybrid Android app</span></span>

<span data-ttu-id="f9bd3-178">ハイブリッド Android アプリのハードウェアの直接対応を有効にするには、MPOSに対しす設定と同じ方法で専用のハードウェアステーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-178">To enable direct hardware support for the hybrid Android app, set up a dedicated hardware station in the same way it would be set up for MPOS.</span></span> <span data-ttu-id="f9bd3-179">専用もしくははIPCハードウェアステーションを設定する手順については、 [Retail 周辺機器](../retail-peripherals-overview.md#modern-pos-for-windows-with-an-ipc-built-in-hardware-station-1) を参照してください</span><span class="sxs-lookup"><span data-stu-id="f9bd3-179">Instructions for setting up the dedicated, or IPC, hardware station can be found in [Retail peripherals](../retail-peripherals-overview.md#modern-pos-for-windows-with-an-ipc-built-in-hardware-station-1)</span></span>

> [!NOTE]
> <span data-ttu-id="f9bd3-180">デモデータが付属している専用ハードウェアステーションは、ハイブリッド Android アプリと併用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-180">The dedicated hardware station provided with demo data should not be used with the hybrid Android app.</span></span> <span data-ttu-id="f9bd3-181">デモデータを含むハイブリッド Android アプリをテストするには、既存のハードウェアステーションを削除し、新しい専用ハードウェアステーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-181">To test the hybrid Android app in an environment with demo data, delete the existing hardware stations and create a new dedicated hardware station.</span></span> 
>
> <span data-ttu-id="f9bd3-182">これを行うには、**Retail とコマース > チャネル > 店舗 > すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-182">To do this, go to **Retail and Commerce > Channels > Stores > All stores**.</span></span> <span data-ttu-id="f9bd3-183">使用する店舗 (通常は "HOUSTON") を選択します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-183">Select the store that will be used, typically "HOUSTON".</span></span> 
>
> <span data-ttu-id="f9bd3-184">店舗の詳細 フォームで、 **ハードウェア ステーション** ファストタブまで下にスクロールしていきます。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-184">In the store details form, scroll down to the **Hardware stations** FastTab.</span></span> <span data-ttu-id="f9bd3-185">既存の専用ハードウェアステーションを削除して **追加** を選択して新しいハードウェアステーションのタイプに **専用** を追加します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-185">Remove the existing dedicated hardware station, then select **Add** to add a new hardware station of type **Dedicated**.</span></span> <span data-ttu-id="f9bd3-186">説明がオプションです。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-186">A description is optional.</span></span> <span data-ttu-id="f9bd3-187">ハードウェアステーションについてはその他の詳細は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-187">No other details are necessary for the hardware station.</span></span> 

<span data-ttu-id="f9bd3-188">支払コネクタを設定するには、 [Dynamics 365 Payment Connector for Adyen](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#setup-and-configuration) に記載されている標準の設定手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-188">To set up the payment connector, follow the standard setup steps noted in the [Dynamics 365 Payment Connector for Adyen](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#setup-and-configuration).</span></span> <span data-ttu-id="f9bd3-189">モダンPOSまたはIISハードウェアステーションコンフィギュレーションの更新という名称のセクションは省略します。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-189">Skip the section labeled "Update the Modern POS or IIS Hardware Station configuration."</span></span>

<span data-ttu-id="f9bd3-190">ネットワーク接続周辺機器の設定に関する詳細については、ドキュメント[ネットワーク周辺機器のサポート](./network-peripherals.md)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="f9bd3-190">For details on setting up network connected peripherals the docs [Support for network peripherals](./network-peripherals.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9bd3-191">追加リソース</span><span class="sxs-lookup"><span data-stu-id="f9bd3-191">Additional resources</span></span>
- [<span data-ttu-id="f9bd3-192">支払に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f9bd3-192">Payments FAQ</span></span>](payments-retail.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
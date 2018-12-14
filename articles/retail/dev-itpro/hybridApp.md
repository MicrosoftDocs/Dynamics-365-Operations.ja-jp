---
title: "Android および iOS での POS ハイブリッド アプリのセットアップ"
description: "このトピックでは、Android および iOS で POS ハイブリッド アプリをセットアップする方法を説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-29-10
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.translationtype: HT
ms.sourcegitcommit: 97a92e9fbb281abde39bfb4188e516f7d638a80f
ms.openlocfilehash: 102b78672a8c503546d7c551e6fef1b085dc9ca0
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pos-hybrid-app-on-android-and-ios"></a><span data-ttu-id="79c26-103">Android および iOS での POS ハイブリッド アプリのセットアップ</span><span class="sxs-lookup"><span data-stu-id="79c26-103">Set up POS hybrid app on Android and iOS</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="79c26-104">このトピックでは、Android および iOS デバイスで Retail POS ハイブリッド アプリを構築して実行する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="79c26-104">This topic shows how to build and run the Retail POS hybrid app on Android and iOS devices.</span></span> 

## <a name="overview"></a><span data-ttu-id="79c26-105">概要</span><span class="sxs-lookup"><span data-stu-id="79c26-105">Overview</span></span>

<span data-ttu-id="79c26-106">Retail ハイブリッド アプリは、[Xamarin](https://docs.microsoft.com/en-us/xamarin/) を使用して構築されたシェルです。</span><span class="sxs-lookup"><span data-stu-id="79c26-106">Retail hybrid app is shell built using [Xamarin](https://docs.microsoft.com/en-us/xamarin/).</span></span> <span data-ttu-id="79c26-107">シェル内は、クラウド POS を読み込む Web ビュー コントローラーになっています。これ、このアプリケーションの設定で指定される Retail サーバー URL に基づきます。</span><span class="sxs-lookup"><span data-stu-id="79c26-107">Inside the shell is a Web view controller that loads the cloud POS, which is based on the Retail server URL specified in the settings of this app.</span></span> <span data-ttu-id="79c26-108">これは、クラウド POS を内部で読み込む Android および iOS の Retail ハイブリッド アプリケーション シェルです。</span><span class="sxs-lookup"><span data-stu-id="79c26-108">This is a Retail hybrid app shell for Android and iOS which will internally load the Cloud POS.</span></span> <span data-ttu-id="79c26-109">詳細については、[クラウド POS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/mpos-or-cpos)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79c26-109">For more information, see [Cloud POS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/mpos-or-cpos).</span></span>

## <a name="development-tools"></a><span data-ttu-id="79c26-110">開発ツール</span><span class="sxs-lookup"><span data-stu-id="79c26-110">Development tools</span></span>
<span data-ttu-id="79c26-111">Retail ハイブリッド アプリは、Android および iOS スマートフォン プラットフォームをサポートします。</span><span class="sxs-lookup"><span data-stu-id="79c26-111">The Retail hybrid app supports the Android and iOS phone platforms.</span></span> <span data-ttu-id="79c26-112">このアプリは、Xamarin を使用して構築されています。つまり、開発用コンピューターには Xamarin をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c26-112">The app is built by using Xamarin, which means that you must install Xamarin on your development computer.</span></span> <span data-ttu-id="79c26-113">iOS アプリをビルドするには、Xamarin がインストールされている Mac が必要です。</span><span class="sxs-lookup"><span data-stu-id="79c26-113">To build the iOS app, you must have a Mac that has Xamarin installed.</span></span> <span data-ttu-id="79c26-114">Microsoft Windows を実行しているコンピューターで Android および iOS の両方に対して開発を行うことができますが、Mac を使用して iOS プラットフォームのビルドを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c26-114">Although you can do development for both Android and iOS on a computer that runs Microsoft Windows, you must use a Mac to complete the build for the iOS platform.</span></span> <span data-ttu-id="79c26-115">Mac が共有チーム リソースである場合、ビルド処理のためだけ Mac を使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="79c26-115">If your Mac is a shared team resource, you might want to use a Mac just for the build process.</span></span> <span data-ttu-id="79c26-116">開発に使用するすべてのコンピューターに、Retail ソフトウェアの開発キット (Retail SDK) をコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c26-116">You must copy the Retail software development kit (Retail SDK) on all the computers that you use for development.</span></span> <span data-ttu-id="79c26-117">Retail SDK は、[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) を使用してプロビジョニングされるすべての開発者 VM で使用できます。</span><span class="sxs-lookup"><span data-stu-id="79c26-117">The Retail SDK is available in all developer VMs that are provisioned for using [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/).</span></span>

<span data-ttu-id="79c26-118">Xamarin の詳細については、[ドXamarin のドキュメント](https://docs.microsoft.com/en-us/xamarin/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79c26-118">For more information about Xamarin, see the [Xamarin documentation](https://docs.microsoft.com/en-us/xamarin/).</span></span>

## <a name="set-up-and-install-xamarin-on-windows"></a><span data-ttu-id="79c26-119">Windows での Xamarin のセットアップとインストール</span><span class="sxs-lookup"><span data-stu-id="79c26-119">Set up and install Xamarin on Windows</span></span>

<span data-ttu-id="79c26-120">Windows で Xamarin をセットアップしてインストールするには、<https://docs.microsoft.com/en-us/xamarin/android/get-started/installation/windows> にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="79c26-120">To set up and install Xamarin on Windows, go to <https://docs.microsoft.com/en-us/xamarin/android/get-started/installation/windows>.</span></span>

### <a name="update-xamarin"></a><span data-ttu-id="79c26-121">Xamarin の更新</span><span class="sxs-lookup"><span data-stu-id="79c26-121">Update Xamarin</span></span>

<span data-ttu-id="79c26-122">Xamarin をインストールした後は、最新の安定バージョンに更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c26-122">After you've installed Xamarin, you must update it to the latest stable version.</span></span>

-   <span data-ttu-id="79c26-123">**Windows**: Microsoft Visual Studio で、**ツール**&gt;**オプション**&gt;**環境**&gt; **Xamarin** &gt;**その他**をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="79c26-123">**Windows** - In Microsoft Visual Studio, click **Tools** &gt; **Options** &gt;**Environment** &gt; **Xamarin** &gt; **Other**.</span></span>
-   <span data-ttu-id="79c26-124">**Mac**: Xamarin Studio で、**更新の確認** &gt; **チャネルを更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="79c26-124">**Mac** - In Xamarin Studio, click **Check for Updates** &gt; **Update channel**.</span></span> <span data-ttu-id="79c26-125">このステップの詳細については、「[https://developer.xamarin.com/recipes/cross-platform/ide/change\_updates\_channel/](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79c26-125">For more information about this step, see [https://developer.xamarin.com/recipes/cross-platform/ide/change\_updates\_channel/](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/).</span></span>

### <a name="build-the-android-retail-hybrid-app"></a><span data-ttu-id="79c26-126">Android Retail ハイブリッド アプリの構築</span><span class="sxs-lookup"><span data-stu-id="79c26-126">Build the Android Retail hybrid app</span></span>

1. <span data-ttu-id="79c26-127">インストールが完了したら、Visual Studio を起動し、Microsoft アカウント (これは、Windows で使用するのと同じアカウント) を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="79c26-127">When installation is complete, launch Visual Studio and sign in with your Microsoft account (this is the same account that you use with Windows).</span></span> <span data-ttu-id="79c26-128">**ツール > オプション > Xamarin** または **ツール > オプション > Xamarin > その他** をクリックして、Xamarin の更新をチェックします。</span><span class="sxs-lookup"><span data-stu-id="79c26-128">Check for Xamarin updates by clicking **Tools > Options > Xamarin** or **Tools > Options > Xamarin > Other**.</span></span> <span data-ttu-id="79c26-129">ここには、**いますぐ確認** リンクがあります。</span><span class="sxs-lookup"><span data-stu-id="79c26-129">Here you’ll find a **Check Now** link.</span></span> <span data-ttu-id="79c26-130">Xamarin のオプションが **ツール > オプション** に表示されない場合、インストールを確認するか、Visual Studio を再起動してみてください。</span><span class="sxs-lookup"><span data-stu-id="79c26-130">If you do not see an option for Xamarin in **Tools > Options**, review your installation, or try restarting Visual Studio.</span></span> <span data-ttu-id="79c26-131">**オプション** ダイアログ ボックスで Xamarin を検索することもできます。</span><span class="sxs-lookup"><span data-stu-id="79c26-131">You can also search for Xamarin in the **Options** dialog box.</span></span> <span data-ttu-id="79c26-132">必要な場合は、最新バージョンをダウンロードおよびインストールします。</span><span class="sxs-lookup"><span data-stu-id="79c26-132">If needed, download and install the latest version.</span></span>
      
2.  <span data-ttu-id="79c26-133">Retail SDK フォルダーで、SampleExtensions\HybridApp\Android\solution を開きます。</span><span class="sxs-lookup"><span data-stu-id="79c26-133">In the Retail SDK folder, open SampleExtensions\HybridApp\Android\solution.</span></span> <span data-ttu-id="79c26-134">エミュレーターを使用して構築および展開し、すべて正常に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="79c26-134">Build and deploy using the emulator and verify that everything appears as it should.</span></span>
  
3.  <span data-ttu-id="79c26-135">[Android 用 Visual Studio エミュレーター](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Android 用 Visual Studio エミュレーター") または Android 用のエミュレーターを使用して POS ハイブリッド アプリを起動し、Retail サーバー URL を入力して保存します。</span><span class="sxs-lookup"><span data-stu-id="79c26-135">Using the [Visual Studio Emulator for Android](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Visual Studio Emulator for Android") or any emulator for Android, launch the POS hybrid app and enter the Retail Server URL and save.</span></span>
  
4.  <span data-ttu-id="79c26-136">ログインして、デバイスをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="79c26-136">You should be able to sign in and activate the device.</span></span>

### <a name="build-the-ios-retail-hybrid-app"></a><span data-ttu-id="79c26-137">iOS Retail ハイブリッド アプリの構築</span><span class="sxs-lookup"><span data-stu-id="79c26-137">Build the iOS Retail hybrid app</span></span>

### <a name="connecting-to-a-mac"></a><span data-ttu-id="79c26-138">Mac に接続しています</span><span class="sxs-lookup"><span data-stu-id="79c26-138">Connecting to a Mac</span></span>

<span data-ttu-id="79c26-139">Windows で開発し、iOS アプリケーションを構築するためだけに Mac を使用している場合は、Windows と Mac を実行するコンピューターを接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79c26-139">If you're developing on Windows and using the Mac just for building the iOS app then you must connect the computer that runs Windows and the Mac.</span></span> <span data-ttu-id="79c26-140">手順については、[Mac に接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79c26-140">For instructions, see [Connecting to the Mac](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/).</span></span>

 ## <a name="set-up-and-install-xamarin-on-ios"></a><span data-ttu-id="79c26-141">iOS での Xamarin のセットアップとインストール</span><span class="sxs-lookup"><span data-stu-id="79c26-141">Set up and install Xamarin on iOS</span></span>

<span data-ttu-id="79c26-142">iOS で Xamarin をインストールに関する詳しい手順については、[Xamarin.iOS のインストール](https://docs.microsoft.com/en-us/xamarin/ios/get-started/installation/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79c26-142">For more detailed steps on installing Xamarin on iOS, refer to [Xamarin.iOS installation](https://docs.microsoft.com/en-us/xamarin/ios/get-started/installation/).</span></span>

  1.  <span data-ttu-id="79c26-143"><https://developer.apple.com/xcode/> から Xcode をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="79c26-143">Download and install Xcode from <https://developer.apple.com/xcode/>.</span></span> <span data-ttu-id="79c26-144">[Xcode へのアカウントの追加](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com) で説明されている手順を使用して Apple ID を追加します。</span><span class="sxs-lookup"><span data-stu-id="79c26-144">Add your Apple ID using the instructions described in [Adding your account to Xcode](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com).</span></span>
  
  2.  <span data-ttu-id="79c26-145">[Xamarin.iOS のインストールおよび構成](http://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com) の手順に従って Xamarin をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="79c26-145">Download and install Xamarin by following the instructions in [Installing and configuring Xamarin.iOS](http://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com).</span></span>
  
  3.  <span data-ttu-id="79c26-146">Windows と Mac コンピューターの両方で Xamarin のインストールを完了したら、[Mac への接続](http://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com) の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="79c26-146">When you have completed installing Xamarin on both the Windows and Mac computers, follow the instructions in [Connecting to the Mac](http://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com).</span></span> <span data-ttu-id="79c26-147">これを行ったら、Windows コンピューターの Visual Studio から iOS および Mac を操作することができます。</span><span class="sxs-lookup"><span data-stu-id="79c26-147">After you do this, you can work with iOS and Mac from Visual Studio on the Windows computer.</span></span>
  
  ### <a name="build-the-ios-retail-hybrid-app"></a><span data-ttu-id="79c26-148">iOS Retail ハイブリッド アプリの構築</span><span class="sxs-lookup"><span data-stu-id="79c26-148">Build the iOS Retail hybrid app</span></span>
  
  1.  <span data-ttu-id="79c26-149">Retail SDK フォルダーで、SampleExtensions\HybridApp\iOS\solution を開きます。</span><span class="sxs-lookup"><span data-stu-id="79c26-149">In the Retail SDK folder, open SampleExtensions\HybridApp\iOS\solution.</span></span>
      <span data-ttu-id="79c26-150">Mac に接続して Visual Studio でアプリケーションを構築したら、iOS デバイスの種類を選択し、選択したデバイス上にアプリケーションを展開します。</span><span class="sxs-lookup"><span data-stu-id="79c26-150">After connecting to the Mac and building the application in Visual Studio, select the iOS device type and deploy the app on the selected device.</span></span>
      
         ![展開用 POS iOS アプリ VS 設定](./media/iOSSetting.png)
      
  2.  <span data-ttu-id="79c26-152">エミュレーターを使用して、**設定 > RetailMPOS** に移動します。</span><span class="sxs-lookup"><span data-stu-id="79c26-152">Using the Emulator, go to **Settings > RetailMPOS**.</span></span> <span data-ttu-id="79c26-153">Retail サーバーの URL を入力してください。</span><span class="sxs-lookup"><span data-stu-id="79c26-153">Enter the Retail Server URL.</span></span>
      
         ![POS iOS アプリ設定](./media/iOSApp.png)
      
         ![RS URL の POS iOS アプリ設定](./media/iOSRSURL.png)
      
  3.  <span data-ttu-id="79c26-156">MPOS アプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="79c26-156">Launch the MPOS app.</span></span> <span data-ttu-id="79c26-157">ログインして、デバイスをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="79c26-157">You should be able to sign in and activate the device.</span></span>


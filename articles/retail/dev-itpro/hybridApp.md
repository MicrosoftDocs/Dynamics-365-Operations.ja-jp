---
title: Android および iOS での POS ハイブリッド アプリのセットアップ
description: このトピックでは、Android および iOS で POS ハイブリッド アプリをセットアップする方法を説明します。
author: mugunthanm
manager: AnnBe
ms.date: 11/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-29-10
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 102b78672a8c503546d7c551e6fef1b085dc9ca0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368491"
---
# <a name="set-up-pos-hybrid-app-on-android-and-ios"></a>Android および iOS での POS ハイブリッド アプリのセットアップ
[!include [banner](../includes/banner.md)]

このトピックでは、Android および iOS デバイスで Retail POS ハイブリッド アプリを構築して実行する方法を説明します。 

## <a name="overview"></a>概要

Retail ハイブリッド アプリは、[Xamarin](https://docs.microsoft.com/en-us/xamarin/) を使用して構築されたシェルです。 シェル内は、クラウド POS を読み込む Web ビュー コントローラーになっています。これ、このアプリケーションの設定で指定される Retail サーバー URL に基づきます。 これは、クラウド POS を内部で読み込む Android および iOS の Retail ハイブリッド アプリケーション シェルです。 詳細については、[クラウド POS](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/mpos-or-cpos)を参照してください。

## <a name="development-tools"></a>開発ツール
Retail ハイブリッド アプリは、Android および iOS スマートフォン プラットフォームをサポートします。 このアプリは、Xamarin を使用して構築されています。つまり、開発用コンピューターには Xamarin をインストールする必要があります。 iOS アプリをビルドするには、Xamarin がインストールされている Mac が必要です。 Microsoft Windows を実行しているコンピューターで Android および iOS の両方に対して開発を行うことができますが、Mac を使用して iOS プラットフォームのビルドを完了する必要があります。 Mac が共有チーム リソースである場合、ビルド処理のためだけ Mac を使用する場合があります。 開発に使用するすべてのコンピューターに、Retail ソフトウェアの開発キット (Retail SDK) をコピーする必要があります。 Retail SDK は、「[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)」を使用してプロビジョニングされるすべての開発者 VM で使用できます。

Xamarin の詳細については、[ドXamarin のドキュメント](https://docs.microsoft.com/en-us/xamarin/)を参照してください。

## <a name="set-up-and-install-xamarin-on-windows"></a>Windows での Xamarin のセットアップとインストール

Windows で Xamarin をセットアップしてインストールするには、<https://docs.microsoft.com/en-us/xamarin/android/get-started/installation/windows> にアクセスします。

### <a name="update-xamarin"></a>Xamarin の更新

Xamarin をインストールした後は、最新の安定バージョンに更新する必要があります。

-   **Windows** - Microsoft Visual Studio で、**ツール** &gt; **オプション** &gt; **環境** &gt; **Xamarin** &gt; **その他**を順にクリックします。
-   **Mac**: Xamarin Studio で、**更新の確認** &gt; **チャネルを更新** をクリックします。 このステップの詳細については、「[https://developer.xamarin.com/recipes/cross-platform/ide/change\_updates\_channel/](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/)」を参照してください。

### <a name="build-the-android-retail-hybrid-app"></a>Android Retail ハイブリッド アプリの構築

1. インストールが完了したら、Visual Studio を起動し、Microsoft アカウント (これは、Windows で使用するのと同じアカウント) を使用してサインインします。 **ツール > オプション > Xamarin** または **ツール > オプション > Xamarin > その他** をクリックして、Xamarin の更新をチェックします。 ここには、**いますぐ確認** リンクがあります。 Xamarin のオプションが **ツール > オプション** に表示されない場合、インストールを確認するか、Visual Studio を再起動してみてください。 **オプション** ダイアログ ボックスで Xamarin を検索することもできます。 必要な場合は、最新バージョンをダウンロードおよびインストールします。
      
2.  Retail SDK フォルダーで、SampleExtensions\HybridApp\Android\solution を開きます。 エミュレーターを使用して構築および展開し、すべて正常に表示されていることを確認します。
  
3.  「[Android 用 Visual Studio エミュレーター](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Emulator for Android 用 Visual Studio エミュレーター")」または Android 用のエミュレーターを使用して POS ハイブリッド アプリを起動し、Retail サーバー URL を入力して保存します。
  
4.  ログインして、デバイスをアクティブにすることができます。

### <a name="build-the-ios-retail-hybrid-app"></a>iOS Retail ハイブリッド アプリの構築

### <a name="connecting-to-a-mac"></a>Mac に接続しています

Windows で開発し、iOS アプリケーションを構築するためだけに Mac を使用している場合は、Windows と Mac を実行するコンピューターを接続する必要があります。 手順については、[Mac に接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) を参照してください。

 ## <a name="set-up-and-install-xamarin-on-ios"></a>iOS での Xamarin のセットアップとインストール

iOS で Xamarin をインストールに関する詳しい手順については、[Xamarin.iOS のインストール](https://docs.microsoft.com/en-us/xamarin/ios/get-started/installation/)を参照してください。

  1.  <https://developer.apple.com/xcode/> から Xcode をダウンロードしてインストールします。 [Xcode へのアカウントの追加](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com) で説明されている手順を使用して Apple ID を追加します。
  
  2.  [Xamarin.iOS のインストールおよび構成](http://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com) の手順に従って Xamarin をダウンロードしてインストールします。
  
  3.  Windows と Mac コンピューターの両方で Xamarin のインストールを完了したら、[Mac への接続](http://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com) の手順に従います。 これを行ったら、Windows コンピューターの Visual Studio から iOS および Mac を操作することができます。
  
  ### <a name="build-the-ios-retail-hybrid-app"></a>iOS Retail ハイブリッド アプリの構築
  
  1.  Retail SDK フォルダーで、SampleExtensions\HybridApp\iOS\solution を開きます。
      Mac に接続して Visual Studio でアプリケーションを構築したら、iOS デバイスの種類を選択し、選択したデバイス上にアプリケーションを展開します。
      
         ![展開用 POS iOS アプリ VS 設定](./media/iOSSetting.png)
      
  2.  エミュレーターを使用して、**設定 > RetailMPOS** に移動します。 Retail サーバーの URL を入力してください。
      
         ![POS iOS アプリ設定](./media/iOSApp.png)
      
         ![RS URL の POS iOS アプリ設定](./media/iOSRSURL.png)
      
  3.  MPOS アプリを起動します。 ログインして、デバイスをアクティブにすることができます。

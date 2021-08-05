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
ms.openlocfilehash: 4ba7c66f9fb567d32c7ce209a63b639e848fe1a8
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6346740"
---
# <a name="set-up-pos-hybrid-app-on-android-and-ios"></a>Android および iOS での POS ハイブリッド アプリのセットアップ
[!include [banner](../includes/banner.md)]

このトピックでは、Android および iOS デバイスで Retail POS ハイブリッド アプリを構築して実行する方法を説明します。 

## <a name="overview"></a>概要

Retail ハイブリッド アプリは、[Xamarin](/xamarin/) を使用して構築されたシェルです。 シェル内は、クラウド POS を読み込む Web ビュー コントローラーになっています。これは、このアプリケーションの設定で指定される Commerce Scale Unit URL に基づきます。 これは、クラウド POS を内部で読み込む Android および iOS の Retail ハイブリッド アプリケーション シェルです。 詳細については、[クラウド POS](/dynamics365/unified-operations/retail/mpos-or-cpos)を参照してください。

## <a name="development-tools"></a>開発ツール
Retail ハイブリッド アプリは、Android および iOS スマートフォン プラットフォームをサポートします。 このアプリは、Xamarin を使用して構築されています。つまり、開発用コンピューターには Xamarin をインストールする必要があります。 iOS アプリをビルドするには、Xamarin がインストールされている Mac が必要です。 Microsoft Windows を実行しているコンピューターで Android および iOS の両方に対して開発を行うことができますが、Mac を使用して iOS プラットフォームのビルドを完了する必要があります。 Mac が共有チーム リソースである場合、ビルド処理のためだけ Mac を使用する場合があります。 開発に使用するすべてのコンピューターに、Retail ソフトウェアの開発キット (Retail SDK) をコピーする必要があります。 Retail SDK は、「[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)」を使用してプロビジョニングされるすべての開発者 VM で使用できます。

Xamarin の詳細については、[Xamarin のドキュメント](/xamarin/)を参照してください。

## <a name="set-up-and-install-xamarin-on-windows"></a>Windows での Xamarin のセットアップとインストール

Windows で Xamarin をセットアップしてインストールするには、[Windows インストール](/xamarin/android/get-started/installation/windows) にアクセスします。

### <a name="update-xamarin"></a>Xamarin の更新

> [!NOTE]
> Xamarin.Android SDK バージョン 10.0 未満の使用をお勧めします。 

Xamarin をインストールした後、最新の安定バージョンに更新する必要があります (Xamarin.Android SDK version は 10.0 未満でなければなりません)。

-   **Windows** - Microsoft Visual Studio で、**ツール** &gt; **オプション** &gt; **環境** &gt; **Xamarin** &gt; **その他** を順にクリックします。
-   **Mac**: Xamarin Studio で、**更新の確認** &gt; **チャネルを更新** をクリックします。 このステップの詳細については、[更新チャンネルの変更](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/) を参照してください。

### <a name="build-the-android-retail-hybrid-app"></a>Android Retail ハイブリッド アプリの構築

> [!NOTE]
> Visual Studio 2019 以降を使用して Android アプリを構築することをお勧めします。

1. インストールが完了したら、Visual Studio を起動し、Microsoft アカウント (これは、Windows で使用するのと同じアカウント) を使用してサインインします。 **ツール > オプション > Xamarin** または **ツール > オプション > Xamarin > その他** をクリックして、Xamarin の更新をチェックします。 ここには、**いますぐ確認** リンクがあります。 Xamarin のオプションが **ツール > オプション** に表示されない場合、インストールを確認するか、Visual Studio を再起動してみてください。 **オプション** ダイアログ ボックスで Xamarin を検索することもできます。 必要な場合は、最新バージョンをダウンロードおよびインストールします。
      
2.  Retail SDK フォルダーで、SampleExtensions\HybridApp\Android\solution を開きます。 エミュレーターを使用して構築および展開し、すべて正常に表示されていることを確認します。
  
3.  [Android 用 Visual Studio エミュレーター](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Android 用の Visual Studio エミュレーター") または Android 用のエミュレーターを使用して、POS ハイブリッド アプリを起動し、Commerce Scale Unit URL を入力して、保存します。
  
4.  ログインして、デバイスをアクティブにすることができます。

### <a name="build-the-ios-retail-hybrid-app"></a>iOS Retail ハイブリッド アプリの構築

### <a name="connecting-to-a-mac"></a>Mac に接続しています

Windows で開発し、iOS アプリケーションを構築するためだけに Mac を使用している場合は、Windows と Mac を実行するコンピューターを接続する必要があります。 手順については、[Mac に接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) を参照してください。

 ## <a name="set-up-and-install-xamarin-on-ios"></a>iOS での Xamarin のセットアップとインストール

iOS で Xamarin をインストールに関する詳しい手順については、[Xamarin.iOS のインストール](/xamarin/ios/get-started/installation/)を参照してください。

  1.  <https://developer.apple.com/xcode/> から Xcode をダウンロードしてインストールします。 [Xcode へのアカウントの追加](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com) で説明されている手順を使用して Apple ID を追加します。
  
  2.  [Xamarin.iOS のインストールおよび構成](https://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com) の手順に従って Xamarin をダウンロードしてインストールします。
  
  3.  Windows と Mac コンピューターの両方で Xamarin のインストールを完了したら、[Mac への接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com) の手順に従います。 これを行ったら、Windows コンピューターの Visual Studio から iOS および Mac を操作することができます。
  
  ### <a name="build-the-ios-retail-hybrid-app"></a>iOS Retail ハイブリッド アプリの構築
  
  1.  Retail SDK フォルダーで、SampleExtensions\HybridApp\iOS\solution を開きます。
      Mac に接続して Visual Studio でアプリケーションを構築したら、iOS デバイスの種類を選択し、選択したデバイス上にアプリケーションを展開します。
      
       ![展開用 POS iOS アプリ VS 設定。](./media/iOSSetting.png)
      
  2.  エミュレーターを使用して、**設定 > RetailMPOS** に移動します。 Commerce Scale Unit URL を入力します。
      
       ![POS iOS アプリ設定。](./media/iOSApp.png)
      
       ![RS URL の POS iOS アプリ設定。](./media/iOSRSURL.png)
      
  3.  MPOS アプリを起動します。 ログインして、デバイスをアクティブにすることができます。


## <a name="hybrid-app-distribution"></a>ハイブリッド アプリの配布

Android および iOS アプリを配布するには、Android および iOS アプリ チームによって推奨された次の配布オプションを参照してください。

- [Android アプリの配布](https://developer.android.com/distribute/marketing-tools/alternative-distribution)
- [iOS アプリの配布](https://developer.apple.com/documentation/xcode/preparing-your-app-for-distribution)

  
## <a name="dedicated-hardware-station-support-for-the-hybrid-android-app"></a>ハイブリッド Android アプリケーションに対応した専用ハードウェアステーション
  
リリース8.1.3以降、専用ハードウェアステーションがハイブリッド Android アプリケーションに対応していします。 Retail Modern POS が周辺機器へのビルトインサポートしているのと同様に、 Android アプリは 専用のハードウェアステーションを使用して、IISベースのハードウェアステーションの配置をせずとも周辺機器に接続することができます。
初期状態では、ハイブリッド Android アプリでは、ネットワーク接続経由での支払ターミナルとレシートプリンターの使用に対応しています。 通常はネットワークを介したデバイスとの通信には、製造元によって指定された独自の通信プロトコルを順守する必要があります。 ハイブリッド Android アプリの場合、標準の組み込み機能として、Adyen と Epson レシート プリンターに対応した Dynamics 365 Payment Connector が用意されています。 

### <a name="out-of-the-box-supported-devices"></a>初期設定で対応しているデバイス

| デバイス | 説明 |
| --- | --- |
| 支払端末 | Dynamics 365 Payment Connector for Adyen を介して [ADYEN支払ターミナルAPI](https://www.adyen.com/blog/introducing-the-terminal-api) が対応しているもの。 |
| レシート プリンター | Epson SOAP HTTPインターフェイスに対応しているネットワーク対応のEpsonプリンター。<p>ネットワーク対応 Star Micronics プリンター。</p> |
| キャッシュ ドロワー | Dynamics 365 Commerce バージョン 10.0.8 での導入: ドロワー キック (d/k) ポートを介してネットワーク対応プリンターに接続されたキャッシュ ドロワー。 |

その他の支払プロセッサや周辺機器への対応は、Payments および Hardware SDKs を通して ISVs から実装することができます。 

### <a name="set-up-peripherals-to-work-with-the-hybrid-android-app"></a>周辺機器をハイブリッド Android アプリと連係させるための設定を行います

ハイブリッド Android アプリのハードウェアの直接対応を有効にするには、MPOSに対しす設定と同じ方法で専用のハードウェアステーションを設定します。 専用もしくははIPCハードウェアステーションを設定する手順については、 [Retail 周辺機器](../retail-peripherals-overview.md#modern-pos-for-windows-with-an-ipc-built-in-hardware-station-1) を参照してください

> [!NOTE]
> デモデータが付属している専用ハードウェアステーションは、ハイブリッド Android アプリと併用しないでください。 デモデータを含むハイブリッド Android アプリをテストするには、既存のハードウェアステーションを削除し、新しい専用ハードウェアステーションを作成します。 
>
> これを行うには、**Retail とコマース > チャネル > 店舗 > すべての店舗** の順に移動します。 使用する店舗 (通常は "HOUSTON") を選択します。 
>
> 店舗の詳細 フォームで、 **ハードウェア ステーション** ファストタブまで下にスクロールしていきます。 既存の専用ハードウェアステーションを削除して **追加** を選択して新しいハードウェアステーションのタイプに **専用** を追加します。 説明がオプションです。 ハードウェアステーションについてはその他の詳細は必要ありません。 

支払コネクタを設定するには、 [Dynamics 365 Payment Connector for Adyen](/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#setup-and-configuration) に記載されている標準の設定手順に従ってください。 モダンPOSまたはIISハードウェアステーションコンフィギュレーションの更新という名称のセクションは省略します。

ネットワーク接続周辺機器の設定に関する詳細については、ドキュメント[ネットワーク周辺機器のサポート](./network-peripherals.md)をご覧ください。

## <a name="additional-resources"></a>追加リソース
- [支払に関するよく寄せられる質問](payments-retail.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

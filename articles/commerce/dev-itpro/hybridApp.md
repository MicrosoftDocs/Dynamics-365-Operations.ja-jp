---
title: Android および iOS での POS ハイブリッド アプリのセットアップ
description: このトピックでは、Android および iOS で POS ハイブリッド アプリをセットアップする方法を説明します。
author: mugunthanm
manager: AnnBe
ms.date: 03/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2018-29-10
ms.dyn365.ops.version: AX 8.0, AX 8.1
ms.openlocfilehash: 25954d61ba58e6c4e7752f549b1965688c718891
ms.sourcegitcommit: 74d05a3a3de2e421eeab7117f2fd1fdaeb23f083
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117155"
---
# <a name="set-up-pos-hybrid-app-on-android-and-ios"></a>Android および iOS での POS ハイブリッド アプリのセットアップ
[!include [banner](../includes/banner.md)]

このトピックでは、Android および iOS デバイスで Retail POS ハイブリッド アプリを構築して実行する方法を説明します。 

## <a name="overview"></a>概要

Retail ハイブリッド アプリは、[Xamarin](https://docs.microsoft.com/xamarin/) を使用して構築されたシェルです。 シェル内は、クラウド POS を読み込む Web ビュー コントローラーになっています。これは、このアプリケーションの設定で指定される Commerce Scale Unit URL に基づきます。 これは、クラウド POS を内部で読み込む Android および iOS の Retail ハイブリッド アプリケーション シェルです。 詳細については、[クラウド POS](https://docs.microsoft.com/dynamics365/unified-operations/retail/mpos-or-cpos)を参照してください。

## <a name="development-tools"></a>開発ツール
Retail ハイブリッド アプリは、Android および iOS スマートフォン プラットフォームをサポートします。 このアプリは、Xamarin を使用して構築されています。つまり、開発用コンピューターには Xamarin をインストールする必要があります。 iOS アプリをビルドするには、Xamarin がインストールされている Mac が必要です。 Microsoft Windows を実行しているコンピューターで Android および iOS の両方に対して開発を行うことができますが、Mac を使用して iOS プラットフォームのビルドを完了する必要があります。 Mac が共有チーム リソースである場合、ビルド処理のためだけ Mac を使用する場合があります。 開発に使用するすべてのコンピューターに、Retail ソフトウェアの開発キット (Retail SDK) をコピーする必要があります。 Retail SDK は、「[Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)」を使用してプロビジョニングされるすべての開発者 VM で使用できます。

Xamarin の詳細については、[ドXamarin のドキュメント](https://docs.microsoft.com/xamarin/)を参照してください。

## <a name="set-up-and-install-xamarin-on-windows"></a>Windows での Xamarin のセットアップとインストール

Windows で Xamarin をセットアップしてインストールするには、<https://docs.microsoft.com/xamarin/android/get-started/installation/windows> にアクセスします。

### <a name="update-xamarin"></a>Xamarin の更新

> [!NOTE]
> Xamarin.Android SDK バージョン 10.0 未満の使用をお勧めします。 

Xamarin をインストールした後、最新の安定バージョンに更新する必要があります (Xamarin.Android SDK version は 10.0 未満でなければなりません)。

-   **Windows** - Microsoft Visual Studio で、**ツール** &gt; **オプション** &gt; **環境** &gt; **Xamarin** &gt; **その他**を順にクリックします。
-   **Mac**: Xamarin Studio で、**更新の確認** &gt; **チャネルを更新** をクリックします。 このステップの詳細については、[更新チャンネルの変更](https://developer.xamarin.com/recipes/cross-platform/ide/change_updates_channel/) を参照してください。

### <a name="build-the-android-retail-hybrid-app"></a>Android Retail ハイブリッド アプリの構築

1. インストールが完了したら、Visual Studio を起動し、Microsoft アカウント (これは、Windows で使用するのと同じアカウント) を使用してサインインします。 **ツール > オプション > Xamarin** または **ツール > オプション > Xamarin > その他** をクリックして、Xamarin の更新をチェックします。 ここには、**いますぐ確認** リンクがあります。 Xamarin のオプションが **ツール > オプション** に表示されない場合、インストールを確認するか、Visual Studio を再起動してみてください。 **オプション** ダイアログ ボックスで Xamarin を検索することもできます。 必要な場合は、最新バージョンをダウンロードおよびインストールします。
      
2.  Retail SDK フォルダーで、SampleExtensions\HybridApp\Android\solution を開きます。 エミュレーターを使用して構築および展開し、すべて正常に表示されていることを確認します。
  
3.  [Android 用 Visual Studio エミュレーター](https://visualstudio.microsoft.com/vs/msft-android-emulator/ "Android 用の Visual Studio エミュレーター") または Android 用のエミュレーターを使用して、POS ハイブリッド アプリを起動し、Commerce Scale Unit URL を入力して、保存します。
  
4.  ログインして、デバイスをアクティブにすることができます。

### <a name="build-the-ios-retail-hybrid-app"></a>iOS Retail ハイブリッド アプリの構築

### <a name="connecting-to-a-mac"></a>Mac に接続しています

Windows で開発し、iOS アプリケーションを構築するためだけに Mac を使用している場合は、Windows と Mac を実行するコンピューターを接続する必要があります。 手順については、[Mac に接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/connecting-to-mac/) を参照してください。

 ## <a name="set-up-and-install-xamarin-on-ios"></a>iOS での Xamarin のセットアップとインストール

iOS で Xamarin をインストールに関する詳しい手順については、[Xamarin.iOS のインストール](https://docs.microsoft.com/xamarin/ios/get-started/installation/)を参照してください。

  1.  <https://developer.apple.com/xcode/> から Xcode をダウンロードしてインストールします。 [Xcode へのアカウントの追加](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppStoreDistributionTutorial/AddingYourAccounttoXcode/AddingYourAccounttoXcode.html#//apple_ref/doc/uid/TP40013839-CH40-SW1) (apple.com) で説明されている手順を使用して Apple ID を追加します。
  
  2.  [Xamarin.iOS のインストールおよび構成](https://developer.xamarin.com/guides/ios/getting_started/installation/mac/) (xamarin.com) の手順に従って Xamarin をダウンロードしてインストールします。
  
  3.  Windows と Mac コンピューターの両方で Xamarin のインストールを完了したら、[Mac への接続](https://developer.xamarin.com/guides/ios/getting_started/installation/windows/xamarin-mac-agent/) (xamarin.com) の手順に従います。 これを行ったら、Windows コンピューターの Visual Studio から iOS および Mac を操作することができます。
  
  ### <a name="build-the-ios-retail-hybrid-app"></a>iOS Retail ハイブリッド アプリの構築
  
  1.  Retail SDK フォルダーで、SampleExtensions\HybridApp\iOS\solution を開きます。
      Mac に接続して Visual Studio でアプリケーションを構築したら、iOS デバイスの種類を選択し、選択したデバイス上にアプリケーションを展開します。
      
         ![展開用 POS iOS アプリ VS 設定](./media/iOSSetting.png)
      
  2.  エミュレーターを使用して、**設定 > RetailMPOS** に移動します。 Commerce Scale Unit URL を入力します。
      
         ![POS iOS アプリ設定](./media/iOSApp.png)
      
         ![RS URL の POS iOS アプリ設定](./media/iOSRSURL.png)
      
  3.  MPOS アプリを起動します。 ログインして、デバイスをアクティブにすることができます。
  
## <a name="dedicated-hardware-station-support-for-the-hybrid-android-app"></a>ハイブリッド Android アプリケーションに対応した専用ハードウェアステーション
  
リリース8.1.3以降、専用ハードウェアステーションがハイブリッド Android アプリケーションに対応していします。 Retail Modern POS が周辺機器へのビルトインサポートしているのと同様に、 Android アプリは 専用のハードウェアステーションを使用して、IISベースのハードウェアステーションの配置をせずとも周辺機器に接続することができます。
初期状態では、ハイブリッド Android アプリでは、ネットワーク接続経由での支払ターミナルとレシートプリンターの使用に対応しています。 通常はネットワークを介したデバイスとの通信には、製造元によって指定された独自の通信プロトコルを順守する必要があります。 ハイブリッド Android アプリの場合、標準の組み込み機能として、Adyen と Epsonレシートプリンターに対応した Dynamics 365支払コネクタが用意されています。 

### <a name="out-of-the-box-supported-devices"></a>初期設定で対応しているデバイス

| デバイス | 説明 |
| --- | --- |
| 支払端末 | Dynamics 365 Payment Connector for Adyen を介して [ADYEN支払ターミナルAPI](https://www.adyen.com/blog/introducing-the-terminal-api) が対応しているもの。 |
| レシート プリンター | Epson SOAP HTTPインターフェイスに対応しているネットワーク対応のEpsonプリンター。 |

その他の支払プロセッサや周辺機器への対応は、Payments および Hardware SDKs を通して ISVs から実装することができます。 

### <a name="set-up-peripherals-to-work-with-the-hybrid-android-app"></a>周辺機器をハイブリッド Android アプリと連係させるための設定を行います。

ハイブリッド Android アプリのハードウェアの直接対応を有効にするには、MPOSに対しす設定と同じ方法で専用のハードウェアステーションを設定します。 専用もしくははIPCハードウェアステーションを設定する手順については、 [Retail 周辺機器](../retail-peripherals-overview.md#modern-pos-for-windows-with-an-ipc-built-in-hardware-station-1) を参照してください。

> [!NOTE]
> デモデータが付属している専用ハードウェアステーションは、ハイブリッド Android アプリと併用しないでください。 デモデータを含むハイブリッド Android アプリをテストするには、既存のハードウェアステーションを削除し、新しい専用ハードウェアステーションを作成します。 
>
> これを行うには、**Retail とコマース > チャネル > 店舗 > すべての店舗**の順に移動します。 使用する店舗 (通常は "HOUSTON") を選択します。 
>
> 店舗の詳細 フォームで、 **Hardware stations** ファストタブまで下にスクロールしていきます。 既存の専用ハードウェアステーションを削除して **追加** を選択して新しいハードウェアステーションのタイプに **専用** を追加します。 説明がオプションです。 ハードウェアステーションについてはその他の詳細は必要ありません。 

支払コネクタを設定するには、 [Dynamics 365 Payment Connector for Adyen](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/adyen-connector?tabs=8-1-3#setup-and-configuration) に記載されている標準の設定手順に従ってください。 モダンPOSまたはIISハードウェアステーションコンフィギュレーションの更新という名称のセクションは省略します。

初期状態では、 Android アプリは Epson ePOS-Print プロトコルに対応している Epson ネットワークプリンターと通信します。 このインターフェイスを有効にするには、Epsonプリンターをネットワークに接続します。 ePOS-Print は、ユーザーがブラウザーから Epson ネットワーク プリンターにアクセスできる Web インターフェイスを通して有効になります。 通常、この Web インターフェイスには、 Web ブラウザーを開いて http://<printer IP address> と入力することでアクセスできます。 プリンターの IP アドレスは、ネットワークに接続し、電源をオフまたはオンにすることによって取得できます。 ネットワーク IP アドレス が取得されると、そのプリンターの IP アドレスを表示する受信確認が印刷されます。 ePOS-Printの設定詳細については、Epsonが提供しているれている資料を参照してください。 
      
EpsonプリンターにてePOS-印刷を有効にした後で、プリンターの電源を切り、再度電源を入れます。 デバイスがオンラインに接続した際に、デバイスのIPアドレスが表示されたレポートが印刷されている必要があります。 デバイスのIPアドレスを控え、Dynamics 365の POSレジスター フォーム へと移動します。 設定中の登録内容を選択し、開いて編集します。 リボン上の **レジスタ** タブにて、 **ハードウェア** という名称の小見出しから **IPアドレスの構成**  というアクションを参照してください。 このアクションにて、特定のレジスターで使用されるプリンターのIPアドレスと指定します。 プリンターの **IPアドレス** フィールドが使用できない場合は、レジスターに割り当てられているハードウェアプロファイルをチェックして、プリンタタイプが **ネットワーク** に設定されていることを確認します。 標準設定上ではEpsonプリンターにポートは必要ありません。

**10.0.8 の新機能** - ドロワー キック (dk) ポート経由で Epson ネットワーク プリンターに接続されたキャッシュ ドロワーがサポートされるようになりました。 ネットワーク対応の Epson プリンターに接続されているキャッシュ ドロワーを使用するには、上記の手順に従ってプリンターを構成します。 ハードウェア プロファイルで キャッシュ ドロワーを 'ネットワーク' タイプに設定します。 ハードウェア プロファイルが割り当てられているレジスターまたはハードウェア ステーションに移動し、 **IP アドレスのコンフィギュレーション** 機能を使用して、プリンターに対してコンフィギュレーションされているアドレスと同じであるキャッシュドロワーの IP アドレスを設定します。


### <a name="sharing-peripherals-using-built-in-peripheral-support"></a>内蔵周辺機器サポートを使用した周辺機器の共有

支払ターミナルおよびレシートプリンターは、POSクライアント Android とその他のMPOSデバイス間で共有することができます。 周辺機器はIISハードウェアステーションを介して共有することができますが、 その他の方法としては Android POSの組み込み周辺機器サポートを追加することによって、webサービスを介したハードウェアステーションを配置することなくこれらのデバイスを共有できるようになります。

Android POSクライアント間でデバイスを共有するには、IPおよびハードウェアプロファイルをレジスターに割り当てるのではなく、ハードウェアプロファイルを専用ハードウェアステーションに設定する必要があります。 これを行うには、**Retail とコマース > チャネル > 店舗 > すべての店舗**の順に移動します。 店舗を選択し、開いて編集します。 次に、店舗のハードウェアステーションの一覧を下方向にスクロールし、ハードウェアプロファイル、ネットワーク支払ターミナル、EFT設定、ネットワークプリンターをハードウェアステーションに割り当てます。 このシナリオでは、EFTターミナルIDを店舗レベルのハードウェアステーションにも割り当てる必要があります。

## <a name="additional-resources"></a>追加リソース
- [支払に関するよく寄せられる質問](payments-retail.md)


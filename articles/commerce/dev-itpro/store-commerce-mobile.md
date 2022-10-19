---
title: モバイル プラットフォーム用 Store Commerce アプリ
description: この記事では、Android および iOS 用の Microsoft Dynamics 365 Commerce Store Commerce アプリの使用を開始する方法について説明します。
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/07/2022
ms.locfileid: "9642341"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>モバイル プラットフォーム用 Store Commerce アプリ

[!include [banner](../includes/banner.md)]

この記事では、Android および iOS 用の Microsoft Dynamics 365 Commerce Store Commerce アプリの使用を開始する方法について説明します。

Android および iOS 用の Dynamics 365 Commerce モバイル アプリにより、小売環境にフル機能モバイル販売時点管理 (POS) デバイスを配置するプロセスがわかりやすく簡単になります。 Store Commerce モバイル アプリは、電話とタブレットのフォーム ファクターに [Windows 用 Store Commerce](store-commerce.md) のすべての機能と利点を提供します。 Store Commerce モバイル アプリは、Apple と Google Play アプリ ストアから直接インストールでき、配置したり更新するための新しいアプリケーション パッケージを開発者が作成する必要はありません。 

Store Commerce モバイル アプリは、現在の Retail ハイブリッド アプリとのフル機能パリティがあります。 さらに、iOS 用の Store Commerce には、専用のハードウェア ステーションのサポートが含まれるため、iOS デバイスは、共有のハードウェア ステーションを配置せずに、ネットワーク接続された支払ターミナル、レシート プリンター、キャッシュ ドロワーと通信できます。 

> [!IMPORTANT]
> Windows、Android および iOS 用の Store Commerce アプリは、Dynamics 365 Commerce 用の次世代の POS アプリケーションです。 現在の Modern POS (MPOS) アプリケーションとモバイル用の [Retail ハイブリッド アプリ](hybridapp.md) は、2023 年 10 月に廃止される予定です。 新しいすべての POS の配置に、Store Commerce または Cloud POS (CPOS) を使用することをお勧めします。 既存の顧客は、Retail ハイブリッド アプリから Store Commerce への移行を計画する必要があります。 MPOS と Retail ハイブリッド アプリの廃止スケジュールの詳細については、[Dynamics 365 Commerce の店舗内テクノロジー スタックを最新化する](https://www.microsoft.com/download/details.aspx?id=103896)を参照してください。 

## <a name="app-architecture"></a>アプリ アーキテクチャ

Store Commerce モバイル アプリは、ハイブリッド モードで配置される Windows 用 Store Commerce アプリと同じトポロジを使用します。 Store Commerce モバイル アプリは、Commerce Scale Unit (CSU) から CPOS を直接表示し、CSU を経由してヘッドレス コマースや Commerce headquarters に接続するシェル アプリケーションです。 シェル アプリケーション モデルを使用すると、Store Commerce アプリは、支払ターミナル、プリンター、キャッシュ ドロワー、その他の周辺機器との直接統合のための専用ハードウェア ステーションをサポートできます。 ハードウェア デバイスを使用するために共有のハードウェア ステーションを設定する必要はありません。 

Store Commerce モバイル アプリを更新するには、CSU を更新します。 新しいすべての POS 機能および特徴は、アプリケーションによって自動的に取得されます。 CSU の更新方法の詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) を参照してください。

シェル アプリは、アプリ ストアの更新を通じてサービスされます。 マイナー バージョンが一般提供 (GA) になると、Microsoft はアプリ ストアで公開します。 また、Microsoft は、マイナー バージョンの更新の間に修正プログラムを公開し、優先順位の高いバグ修正プログラムをリリースすることもあります。

## <a name="prerequisites"></a>必要条件

Store Commerce モバイル アプリには Dynamics 365 Commerce が必要で、特に Commerce headquarters と CSU コンポーネントが必要です。 次の表に、Android と iOS モバイル アプリに必要なオペレーティング システム (OS) と CSU の最小バージョンを示します。 

| 前提条件 | Android      | iOS  |
| ------------ | ------------ | ---- |
| OS バージョン   | 7.0          | 15.0 |
| CSU バージョン  | 9.38.22266.8 | 未確定  |

## <a name="install-the-app"></a>アプリのインストール

Store Commerce モバイル アプリは、Google Play ストアまたは Apple App Store から直接インストールできます。 

- [Android 用 Store Commerce アプリ](https://aka.ms/storecommerceandroid)
- iOS 用 Store Commerce アプリ (まもなく利用できます)

Android アプリ (.apk) と Apple アプリ (.ipa) パッケージは、Store Commerce アプリは Microsoft Dynamics Lifecycle Services の共有資産ライブラリからダウンロードすることもできます。 

## <a name="device-and-register-setup"></a>デバイスとレジスターの設定

Store Commerce モバイル アプリでレジスターを有効化する前に、Commerce Headquarters でデバイスとレジスターを設定する必要があります。 詳細は、[デバイスとレジスター](../implementation-considerations-devices.md)を参照してください。 

### <a name="device-setup"></a>デバイスの設定

新しいデバイスを作成して設定するには、次の手順に従います。

1. Commerce headquarters で、**小売とコマース \> チャネル設定 \> POS 設定 \> デバイス** の順に移動します。 
1. 新しいデバイスを作成し、配置するモバイル アプリに応じて、アプリケーション タイプとして **Modern POS - Android** または **Modern POS - iOS** を選択します。 

    > [!NOTE] 
    > **Modern POS - Android** および **Modern POS - iOS** アプリケーション タイプも、Android と iOS 用の現在のハイブリッド アプリの配置に使用されます。 MPOS が廃止された後、これらのアプリケーション タイプのラベルが **Store Commerce - Android** および **Modern POS - iOS** に更新されます。 

### <a name="register-setup"></a>設定の登録

新しいレジスターを作成して作成したデバイスに関連付けるか、既存のレジスターを新しいデバイスに関連付けることができます。 レジスターの詳細については、[レジスターの作成と関連付け](../tasks/create-associate-registers.md)を参照してください。

### <a name="screen-layout-setup"></a>画面レイアウトの設定

Dynamics 365 Commerce ライセンスで提供されているデモ データに含まれている画面レイアウトを別の目的で使用する場合、デバイスの画面解像度が縦方向で 480 &times; 853 ピクセル未満の場合、Store Commerce アプリは、含まれるコンパクト デザインを自動的に選択します。 ただし、最初から画面レイアウトを作成する場合、またはモバイル デバイスが、コンパクト レイアウトがサポートするよりも大きい解像度を使用する場合は、配置する予定の電話またはタブレットに適した解像度および関連するボタン グリッドを作成する必要があります。 画面レイアウト構成の詳細は、[POS ユーザー インターフェイスのビジュアル コンフィギュレーション](../pos-screen-layouts.md)を参照してください。 

デバイスとレジスターの構成が完了したら、Commerce Headquarters で **小売とコマース \> 小売とコマース ID \> 配送スケジュール** に移動し、レジスター ジョブを実行します。

## <a name="activate-a-device"></a>デバイスのアクティブ化

Store Commerce モバイル アプリでデバイスを有効にするには、次の手順の従います。

1. モバイル デバイスでアプリを開きます。
1. CPOS URL を入力します。これは、Lifecycle Services の環境の詳細のページ、または Commerce headquarters の **チャネル プロファイル** ページ (**小売とコマース \> チャネル設定 \> チャネル プロファイル**) で確認できます。
1. デバイスを管理するためのアクセス許可を持つ作業者の資格情報を使用してサインインします。
1. Commerce Headquarters で作成または再利用したレジスターに関連付けられている店舗を選択します。
1. Commerce Headquarters で作成したデバイスに関連付けられているレジスターを選択します。
1. デバイスは現在有効化されている必要があります。 選択した店舗に関連付けられている作業者のオペレーター ID とパスワードを使用して、レジスターにサインインできます。 

デバイスのアクティブ化の詳細については、[販売時点管理 (POS) デバイスのアクティブ化](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation)を参照してください。

## <a name="feature-parity-with-store-commerce-for-windows"></a>Windows 用 Store Commerce の機能パリティ

次の表では、Windows、Android、および iOS で Store Commerce アプリケーションの機能を比較します。

| フィーチャー                                                                               | ウィンドウ | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| 専用ハードウェア ステーション                                                            | 有効     | 有効     | 有効 |
| 共有ハードウェア ステーション                                                               | 有効     | 有効     | 有効 |
| ネットワーク周辺機器 (支払ターミナル、プリンター、キャッシュ ドロワー) との通信 | 有効     | 有効     | 有効 |
| ローカル ハードウェア ステーションを使用した販売時点管理 (OPOS) 周辺機器の OLE             | 有効     | 無効      | 無効  |
| オフライン モード                                                                          | 有効     | 無効      | 無効  |

## <a name="additional-resources"></a>追加リソース

[Store Commerce アプリ](store-commerce.md)

[Store Commerce または Cloud POS を選択する](../mpos-or-cpos.md)

[Store Commerce の設定とインストールに関する問題のトラブルシューティング](../troubleshoot/store-commerce-setup-installation.md)

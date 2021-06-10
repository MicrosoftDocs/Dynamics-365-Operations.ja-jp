---
title: Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)
description: このトピックでは、Store Commerce アプリの設定および構成方法について説明します。
author: mugunthanm
ms.date: 05/26/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-20-2020
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 8b7ba86d524735a4f986988d032e3b234ac17a1f
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/26/2021
ms.locfileid: "6103084"
---
# <a name="store-commerce-app-in-microsoft-dynamics-365-commerce-preview"></a>Microsoft Dynamics 365 Commerce での Store Commerce アプリ (プレビュー)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

このトピックは、Dynamics 365 Commerce バージョン 10.0.20 およびそれ以降に適用されます。

Microsoft Dynamics 365 Commerce の Store Commerce アプリは、レジ担当者、販売担当者、販売在庫担当者、在庫担当者、店長など第一線の作業者に、現金売りトランザクション、キャッシュ/シフト管理、顧客エンゲージメント、販売支援、クライアンテリング、エンドレス アイル、注文処理/フルフィルメント、在庫管理、レポートなどの豊富なコマース機能を提供します。

> [!NOTE]
> Store Commerceは、プレビュー アプリケーションとしてリリースされます。 Store Commerce では同じくプレビュー中の [Microsoft Edge WebView2](/microsoft-edge/webview2/) が使用されます。 したがって、運用環境では Store Commerce を使用しません。 Store Commerce は、一般に使用可能 (GA) になったら、運用環境で使用できます。

Store Commerce は、[Microsoft Edge WebView2](/microsoft-edge/webview2/) を使用してクラウド販売時点管理 (CPOS) を表示する Windows 用のシェル アプリです。 CPOS は Web ブラウザーでのみ実行できますが、Store Commerce は [Modern 販売時点管理](retail-modern-pos-architecture.md) のようなネイティブ WIndows アプリとして実行できます。 Store Commerce はローカル ハードウェア ステーションをサポートし、支払ターミナル、プリンター、キャッシュ ドロワーに直接統合できます。 ハードウェア デバイスを使用するために共有のハードウェア ステーションを設定する必要はありません。 

Store Commerce は、UI を表示するために、ユニバーサル Windows プラットフォーム (UTC) アプリ表示フレームワークではなく、Chromium エンジンを使用します。 Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。 MPOS と Store Commerce の主な違いは、Store Commerce がアプリを表示するのに Chromium エンジンを使用する点です。

## <a name="application-lifecycle-management-alm"></a>アプリケーション ライフサイクル管理 (ALM)

Store Commerce は、Windows デバイスで実行するアプリケーションです。 このアプリは [WIndows アプリ - Microsoft Store](https://www.microsoft.com/store/r/9PGK1J3KQ8JB) から入手でき、検出、ダウンロード、および展開が容易なため、展開やサービスのライフサイクル全体を簡略化します。 Store Commerce は、上位と下位の両方の互換性があります。 このアプリは、クラウド スケール ユニットおよび拡張機能とは別に更新できます。 このアプリは、Windows ポリシーを設定するか、Microsoft Store のアプリでサポートされている更新プログラムや配置ツールを使用して簡単に更新できます。 Modern POS では、アプリを取得して拡張機能でパッケージ化するためには手動による管理が必要ですが、Store Commerce は、Microsoft Store から配置する機能なので、ALM を大幅に簡素化できます。  

Store Commerce は CPOS を表示するシェルなので、CPOS を更新して更新後の CPOS 機能を利用する必要があります。 CPOS は、クラウド スケール ユニット (CSU) から更新できます。 CSU の更新の詳細については、[Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md) を参照する

![Store Commerce](media/StoreCommerce.PNG)

## <a name="store-commerce-is-the-future-of-mpos"></a>Store Commerce は MPOS の未来である

Store Commerce が MPOS と完全に同等の機能を持つようになった場合、MPOS は置き換えられます。 現時点では、Store Commerce はオフラインでの実行をサポートしません (Retail Server への接続がない場合)。 さまざまな POS アプリおよびトポロジの詳細については [Modern POS (MPOS) かクラウド POS かの選択](../mpos-or-cpos.md) を参照する

## <a name="choosing-between-store-commerce-and-mpos"></a>Store Commerce か MPOS かの選択

Store Commerce では CPOS が表示されますが、MPOS と同等の機能があります。 Store Commerce と MPOS はユニバーサル Windows プラットフォーム (UTC) アプリで、ローカル ハードウェア ステーションをサポートしています。 Store Commerce は現在、オフラインでサポートされていませんが、将来サポートされる予定です。 

Store Commerce は、UI を表示するためにChromium エンジンを使用しますので、MPOS や Store Commerce を Microsoft Store を通じて配置する場合に比べてレンダリング パフォーマンスが向上し、ALM は大幅に簡素化されます。一方、MPOS は LCS および HQ を使用したセルフサービスです。 将来、MPOS は廃止され、Store Commerce に置き換えられる予定です。 

店舗でオフライン サポートが不要な場合は、Store Commerce を選択します。 

アプリケーション タイプ | Store Commerce (プレビュー) | MPOS
---|---|---
操作環境 | Windows | Windows
ALM | Microsoft Store および CPOSは、CSU を通じて配置されています。 | LCS、HQ を使用するセルフサービス、および MPOS インストーラーを使用してパッケージ化およびインストールされます。
拡張子 | CPOS に配置されます。 | MPOS または独立した拡張機能パッケージと共にパッケージ化されています。
オフラインのサポート | なし (将来サポートされます。) | あり
ローカル ハードウェア ステーションのサポート | あり | あり
UI レンダリング エンジン | UI を表示する Curomium エンジン。 | UI を表示するための UWP アプリ フレームワーク。

## <a name="setup-and-installation"></a>設定およびインストール

### <a name="prerequisite"></a>前提条件

+ Microsoft Edge、アプリは Microsoft Edge WebView2 コントロールを使用するためです。

### <a name="hq-device-setup"></a>HQ デバイスの設定

Store Commerce のために、**Store Commerce** という名前の新しいアプリケーション タイプが **Retail と Commerce > POS セットアップ > デバイス>** に追加されます。 Store Commerce のデバイスを作成する場合は、**アプリケーションのタイプ** を **Store Commerce** に設定します。

Store Commerce のために[登録](../tasks/create-associate-registers.md) と[デバイス](../tasks/create-associate-device.md) を作成します。 その後、アプリを有効化し、デバイスの作成時に **アプリケーション タイプ** を **Store Commerce** に設定する前に、HQ の配送スケジュールからレジスター ジョブを実行します。

Store Commerce は、Microsoft Store でダウンロードおよびインストールできます。 アプリをダウンロードするには、これらの手順に従います。

1. [Windows アプリ- Microsoft Store](https://www.microsoft.com/store/r/9PGK1J3KQ8JB) を開き、**Store Commerce** を検索します。
2. **入手** を選択し、アプリをインストールします。  
3. Windows のスタート メニューで Store Commerce を検索し、アプリを開きます。

Store Commerce の起動後、次の手順に従って、アプリを構成および有効化します。

1.  アプリの開始ページに、クラウド POS の URL を入力します。 クラウド POS の URL は、LCS 環境の詳細ページ、または **Dynamics 365 Commerce > チャネル設定 > チャネル プロフィール** を参照してください。
2.  **保存** を選択します。
3.  URL を保存した後、手順に従って Store Commerce を有効にしてください。 アプリを有効にする詳細な手順については、[POS の有効化ガイド](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation) を参照してください。
4.  アプリが有効化された後、従業員アカウントでログインします。 これで、Commerce タスクを完了できます。

### <a name="troubleshooting-setup-issues"></a> 設定の問題に関するトラブルシューティング

#### <a name="reset-the-app"></a>アプリのリセット

無効な CPOS URL を入力して、変更したい場合、または、有効化の際にアプリがエラー状態にある場合は、アプリをリセットしてプロセスを再開できます。

1. 開始メニューでアプリを右クリックし、**詳細 > アプリの設定** を選択します。
2. アプリケーション設定ページを **リセット** ボタンまで下にスクロールします。
3. **リセット** を選択し、確認メッセージを確認します。

## <a name="customizing-the-app"></a>アプリのカスタマイズ

Store Commerce アプリは、Retail SDK の POS 拡張機能サポートを使用してカスタマイズできます。 POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更の実行、検証の追加、カスタム機能の追加を行うことができます。 - 詳細については、[販売時点管理 (POS) の拡張機能の概要](pos-extension/pos-extension-overview.md) を参照してください。

Retail SDK を使用して開発された拡張機能は CPOS、MPOS、および Store Commerce で使用しますが、拡張機能をパッケージ化して配置する方法は MPOS と CPOS によって異なります。

Store Commerce では CPOS が表示されるので、CPOS のパッケージと配置のオプションに従って店舗のコマース拡張機能を配置します。

### <a name="hardware-station-extensionhws"></a>ハードウェア ステーション拡張機能 (HWS)

また、このアプリをハードウェア デバイスと統合するために拡張することができ、[Store Commerce HWS 拡張機能パッケージを生成するためにサンプル拡張機能コードを GitHub に追加することができます](https://github.com/microsoft/Dynamics365Commerce.InStore/tree/release/9.28/src/PosSample)。 詳細については [POS と新しいハードウェア デバイスの統合](hardware-device-extension.md) を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)] 

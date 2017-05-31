---
title: "システム要件"
description: "このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Operations のシステム要件を一覧表示します。"
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: de2f71a21c5aac953349559c84283d0f76082d42
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017


---

# <a name="system-requirements"></a>システム要件

[!include[banner](../includes/banner.md)]


このトピックでは、現在のバージョンの Microsoft Dynamics 365 for Operations のシステム要件を一覧表示します。

<a name="supported-web-browsers"></a>サポートされている Web ブラウザー
----------------------

Microsoft Dynamics 365 for Operations Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

-   Windows 10 の Microsoft Edge (公開されている最新のバージョン)
-   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
-   Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン)
-   Mac OS X 10.10 (Yosemite)、 10.11 (El Capitan) または 10.12 (Sierra)、または Apple iPad の Apple Safari (公開されている最新のバージョン)

各 Web ブラウザの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。 

**メモ :**

-   タスク レコーダーから生成される画像をキャプチャして Microsoft Word ドキュメントに含めるには、Chrome 拡張機能をインストールする必要があります。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   ワークフロー エディターは ClickOnce アプリケーションとして起動されます。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをサポートします。 ワークフロー エディタ ClickOnce アプリケーションには、64 ビットの互換性のあるオペレーティング システムが必要です。
-   財務報告のレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Chrome を使用している場合、レポート デザイナーのクライアントをダウンロードするために ClickOnce 拡張機能をインストールする必要があります。 匿名モードで Chrome を使用している場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
-   PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS でサポートされている Web ブラウザー

Dynamics 365 for Operations の Retail Cloud POS は、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

-   Windows 10 の Microsoft Edge (公開されている最新のバージョン)
-   Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
-   Windows 10、Windows 8.1、または Windows 7 の Chrome (公開されている最新のバージョン)

## <a name="network-requirements"></a>ネットワーク要件
-   Dynamics 365 for Operations は、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 これは、ブラウザー クライアントから Dynamics 365 for Operations をホストする Microsoft Azure データ センターまでの待機時間です。 <http://www.azurespeed.com> でネットワーク待機時間をテストすることをお勧めします。
-   Dynamics 365 for Operations の帯域幅の要件はシナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) 以上の帯域幅が必要です。 ただし、大がかりなカスタマイズを必要とするワークスペースやシナリオなど、高度な伝送データ要件があるシナリオでは、帯域幅を増やすことをお勧めします。

一般に、Dynamics 365 for Operations は、インターネットに最適化されます。 ブラウザー クライアントから Azure データ センターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。 

**警告:** ユーザー数に帯域幅要件の最小値を掛けてクライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客には、Dynamics 365 for Operations のプレビュー バージョンを使用します。

## <a name="net-framework-requirements"></a>.NET Framework 要件
Dynamics 365 for Operations では、ドキュメント回覧エージェントなどのすべてのクリック ワンス アプリケーション用に .NET Framework バージョン 4.6.2 が必要です。 インストール手順については、[.NET Framework のインストール](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx) を参照してください。

## <a name="supported-microsoft-office-applications"></a>サポートされている Microsoft Office アプリケーション
-   Microsoft Excel と Word のアドインを実行するには、Windows か Mac 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要件の詳細については、[Office 統合トラブルシューティング](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting) を参照してください。
-   [Excel にエクスポート] または [Word にエクスポート] 機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS 要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail Modern POS は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   Retail Modern POS は Windows 10 Pro、Enterprise、また Enterprise Long Term Servicing Branch (LTSB) エディションでのみサポートされています。

### <a name="minimum-system-requirements"></a>最少システム要件

-   最少のサポートされている解像度は 1280 × 1024 です。
-   Retail Modern POS を実行するコンピュータは以下の要件を満たす必要があります。
    -   最低でも、2 ギガヘルツ (GHz) で動作するデュアルコア プロセッサが必要です。
    -   最低でも、3 ギガバイト (GB) の RAM が必要です。
    -   インターネットにアクセスできる必要があります。

## <a name="retail-hardware-station-requirements"></a>Retail hardware station 要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail hardware station は 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   Retail hardware station は、以下のオペレーティング システムでサポートされます。
    -   Windows 7 Professional、Enterprise、また Ultimate エディション **注記:** Windows 7 は Internet Explorer 11 が手動でシステムにインストールされている場合にのみサポートされます。
    -   Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション
    -   Windows 10 Pro、Enterprise、また Enterprise LTSB エディション

### <a name="minimum-system-requirements"></a>最少システム要件

コンピュータは、以下の項目をインストールし使用するためのすべてのシステム要件を満たす必要があります。

-   インターネット インフォメーション サービス (IIS)
-   サード パーティのハードウェア

## <a name="retail-store-scale-unit-requirements"></a>Retail Store スケール ユニット要件
### <a name="supported-operating-systems"></a>サポートされるオペレーティング システム

-   Retail Store スケール ユニットは 32 ビット アプリケーションですが、x86 と x64 アーキテクチャの両方で動作します。
-   Retail Store スケール ユニットは、以下のオペレーティング システムでサポートされます。
    -   Windows 7 Professional、Enterprise、また Ultimate エディション
    -   Windows 8.1 Update 1 Professional、Enterprise また Embedded エディション
    -   Windows 10 Pro、Enterprise、また Enterprise LTSB エディション

### <a name="minimum-system-requirements"></a>最少システム要件

-   4 GB の RAM
-   コアごとの CPU 最大処理スピード 1.6 GHz (最少 2 コア)
-   少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

### <a name="recommended-system-requirements"></a>推奨システム要件

-   6 GB の RAM
-   コアごとの最大処理スピード 2.4 GHz i7 (または同等のもの) (推奨 4 コア)
-   少なくとも 10 GB の空き領域 (チャンネル データベースが大量の領域を必要とする場合があります。）

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件
ローカル仮想マシン (VM) の開発要件については、[オンプレミス実行の VM](../dev-tools/access-instances.md) を参照してください。

<a name="see-also"></a>参照
--------

[Dynamics 365 for Operations の評価版を取得](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)





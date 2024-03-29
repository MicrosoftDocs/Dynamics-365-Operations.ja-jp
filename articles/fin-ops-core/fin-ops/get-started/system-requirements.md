---
title: クラウド配置のシステム要件
description: この記事では、現在のバージョンの財務と運用アプリのシステム要件を一覧表示します。
author: sericks007
ms.date: 02/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 8342f9d53615e4cebbb3670db966e497c57db5c4
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123932"
---
# <a name="system-requirements-for-cloud-deployments"></a>クラウド配置のシステム要件

[!include [banner](../includes/banner.md)]

この記事では、現在のバージョンの財務と運用アプリのシステム要件を一覧表示します。 作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを確認する必要があります。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

ユーザーは、これらの一般的なブラウザの最新バージョンを使用してアプリにアクセスできます。 

- Microsoft Edge (推奨: [Chromium ベースの Edge](https://support.microsoft.com/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf))
- Google Chrome
- Apple Safari
- Internet Explorer 11 (非推奨)

各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。

> [!NOTE]
> パフォーマンスを最適化し、最適なエクスペリエンスを提供するために、最新のブラウザ、特に Microsoft Edge の最新バージョンを使用することをお勧めします。 
> 
> **バージョン 10.0.21 以降:** Microsoft Edge の古いバージョンおよび Google Chrome (バージョン 83 以前) のユーザーには、ブラウザーを最新バージョンに更新するよう求めるメッセージが表示されます。

### <a name="internet-explorer-deprecation"></a>Internet Explorer の廃止

2020 年 12 月に Internet Explorer 11 のサポートが廃止され、2021 年 8 月にブラウザーのサポートが終了します。 詳細については、[Internet Explorer 非推奨のお知らせ](../../dev-itpro/get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10015-of-finance-and-operations-apps) を参照してください。

バージョン 10.0.20 から、Internet Explorer で財務と運用アプリにアクセスするユーザーに、そのブラウザのサポート終了に関する通知が表示されます。 2021 年 8 月 17 日より前に、複数の Internet Explorer ユーザーに対して、Internet Explorer サポートが間もなく終了するという情報メッセージが表示されます。 その日以降、サポートが正式に終了したという警告が Internet Explorer ユーザーに表示されます。 組織は、Internet Explorer がユーザーにとって必須になっている以外は、これらの通知を継続することが推奨されます。そのケースでは、**Internet Explorer のサポート終了通知** 機能を無効にし、ユーザー ベースを Microsoft Edge または他の最新のブラウザーに移行する内部プロセスに依存することによりこれらの通知の非表示を選択できます。 

バージョン 10.0.25 から、財務と運用アプリで Internet Explorer 11 の使用がブロックされます。 組織がそれ以前に Internet Explorer をブロックする必要があり、バージョン 10.0.21 以降を使用している場合は、Microsoft サポートに問い合わせてください。 

組織およびユーザーが今後の Internet Explorer のブロックに対応するために、2022 年 1 月以降、Internet Explorer ユーザーは Internet Explorer サポートが間もなくブロックされることを示す無視できないエラー メッセージを受信します。 このエラー メッセージは **Internet Explorer サポート終了通知** により制御 **されません**。 このメッセージを組織に対して非表示にする必要がある場合、顧客は Microsoft サポートに問い合わせる必要があります。

### <a name="special-considerations"></a>特別な注意事項

- タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。
- 財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。 Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。 匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
- PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。

## <a name="network-requirements"></a>ネットワーク要件

- アプリは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントからアプリをホストする Microsoft Azure データ センターまでの待機時間のことです。 [AzureSpeed.com](https://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。
- アプリに対する帯域幅の要件は、シナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。

一般に、アプリはインターネットに最適化されます。 ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客は、アプリのプレビュー バージョンを使用するべきです。

## <a name="net-framework-requirements"></a>.NET Framework 要件

アプリでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.6.2 が必要です。 インストール手順については、[開発者の .NET Framework のインストール](/dotnet/framework/install/guide-for-developers) を参照してください。

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

次の Microsoft Office アプリケーションがクラウドでサポートされています。

- Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
- Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件

ローカル仮想マシン (VM) の開発要件については、[ローカルで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-locally) を参照してください。

## <a name="database-collation"></a>データベース照合順序

クラウドで唯一サポートされているアプリケーション データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。 開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。 また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。

## <a name="additional-resources"></a>追加リソース

[評価版コピーの入手](../../dev-itpro/dev-tools/get-evaluation-copy.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]


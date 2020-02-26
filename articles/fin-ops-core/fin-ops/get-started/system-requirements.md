---
title: クラウド配置のシステム要件
description: このトピックでは、現在のバージョンの Finance and Operations アプリのシステム要件を一覧表示します。
author: sericks007
manager: AnnBe
ms.date: 09/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: da8d8e25ab76bff3a2f55e1673f0efbd14ebc7b5
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029831"
---
# <a name="system-requirements-for-cloud-deployments"></a>クラウド配置のシステム要件

[!include [banner](../includes/banner.md)]

このトピックでは、現在のバージョンの Dynamics 365 Finance および Dynamics 365 Supply Chain Management におけるクラウド配置のシステム要件を一覧表示します。 これらのアプリのいずれかをインストールする前に、このステップが適切な場合、作業しているシステムがネットワーク、ハードウェア、およびソフトウェアの最小要件を満たしているか、または超えているかを検証する必要があります。

## <a name="supported-web-browsers"></a>サポートされている Web ブラウザー

Web アプリケーションは、指定されたオペレーティング システムで実行される次のすべての Web ブラウザで実行できます。

- Windows 10 の Microsoft Edge (公開されている最新のバージョン)
- Windows 10、Windows 8.1、または Windows 7 の Internet Explorer 11
- Google Chrome (公開されている最新バージョン) 
- Apple Safari (公開されている最新バージョン)

各 Web ブラウザーの最新版を検索するには、ソフトウェア メーカーの Web サイトに移動します。

> [!NOTE]
> - タスク レコーダーがスクリーンショットをキャプチャし、生成された Microsoft Word ドキュメントにそれらを含めるには、プレリリース版の Chrome 拡張機能をインストールする必要があります。 <!---For instructions about how to install the extension, see [Screenshot Extension setup](../../dev-itpro/user-interface/task-recorder).-->
> - 財務報告のワークフロー エディターおよびレポート デザイナーは、ClickOnce アプリケーションとして起動されます。 それには 64 ビットの互換性のあるオペレーティング システムが必要です。 Microsoft Edge と Internet Explorer (Microsoft Windows のサポートされているバージョン) のみが、ClickOnce アプリケーションをそのままの状態でサポートします。 Chrom を使用している場合、ClickOnce アプリケーションを使用するには、[Meta4](https://chrome.google.com/webstore/detail/meta4-clickonce-launcher/jkncabbipkgbconhaajbapbhokpbgkdc) などの ClickOnce 拡張をインストールする必要があります。 匿名モードで Chrome を使用する場合、ClickOnce の拡張機能が匿名モードに対しても有効化されていることを確認します。
> - PDF ファイルをプレビューするには、Windows 10 の Microsoft Edge (公開されている最新のバージョン)、もしくは Windows 10、Windows 8.1、Windows 8、Windows 7、または Google Nexus 10 タブレットの Google Chrome (公開されている最新のバージョン) などの最新のブラウザを使用することをお勧めします。

## <a name="network-requirements"></a>ネットワーク要件

- アプリは、待機時間が 250 ～ 300 ミリ秒 (ms) 以下のネットワーク用に設計されています。 この待機時間は、ブラウザー クライアントからアプリをホストする Microsoft Azure データ センターまでの待機時間のことです。 [AzureSpeed.com](https://www.azurespeed.com) にてネットワークの待機時間をテストすることをお勧めします。
- アプリに対する帯域幅の要件は、シナリオによって異なります。 最も一般的なシナリオでは、毎秒 50 キロバイト (KBps) を超える帯域幅が必要です。 ただし、ワークスペースや大がかりなカスタマイズを含む高度な伝送データ要件があるシナリオには、帯域幅を増やすことを勧めます。

一般に、アプリはインターネットに最適化されます。 ブラウザー クライアントから Azure データセンターへのラウンド トリップの数は非常に小さく、全伝送データは圧縮されます。

> [!WARNING]
> ユーザー数に帯域幅要件の最小値を掛けて、クライアントの場所からの帯域幅要件を計算しないでください。 特定の場所の同時使用は非常に計算が困難です。 帯域幅の要件について懸念する顧客は、アプリのプレビュー バージョンを使用するべきです。

## <a name="net-framework-requirements"></a>.NET Framework 要件

アプリでは、ドキュメント回覧エージェントなどのすべての ClickOnce アプリケーション用として Microsoft .NET Framework バージョン 4.6.2 が必要です。 インストール手順については、[開発者の .NET Framework のインストール](https://msdn.microsoft.com/library/5a4x27ek(v=vs.110).aspx) を参照してください。

## <a name="supported-microsoft-office-applications"></a>サポートされる Microsoft Office アプリケーション

次の Microsoft Office アプリケーションがクラウドでサポートされています。

- Microsoft Excel と Word のアドインを実行するには、Windows 用の Microsoft Office 2016 をインストールしておく必要があります。 バージョン要求の詳細については、[Office 統合に関するトラブルシューティング](../../dev-itpro/office-integration/office-integration-troubleshooting.md) を参照してください。
- Excel にエクスポートまたはWord にエクスポート機能によって生成されたドキュメントを表示するには、Microsoft Office 2007 以降をインストールしておく必要があります。

## <a name="requirements-for-development-on-local-vms"></a>ローカル VM の開発要件

ローカル仮想マシン (VM) の開発要件については、[オンプレミスで実行されている VM](../../dev-itpro/dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。

## <a name="database-collation"></a>データベース照合順序

クラウドで唯一サポートされているアプリケーション データベースの照合順序は、**SQL\_Latin1\_General\_CP1\_CI\_AS** です。 開発環境の SQL Server とデータベース照合順序がこれに設定されていることを確認してください。 また、サンドボックスに発行されたすべてのコンフィギュレーション環境にこれと同じ照合順序があることを確認します。

## <a name="additional-resources"></a>追加リソース

[評価版コピーの入手](../../dev-itpro/dev-tools/get-evaluation-copy.md)

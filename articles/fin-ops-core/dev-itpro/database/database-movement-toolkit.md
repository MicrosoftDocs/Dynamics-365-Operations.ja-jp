---
title: データベース移動ツールキット
description: このトピックでは、データベース移動ツールキットをダウンロードして使用する方法について説明します。
author: laneswenka
ms.date: 12/02/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: 93e468211c9decb995955ca1ca252b1bbb1ef03d
ms.sourcegitcommit: 4c8223c9540fbc1c1e554962938058d432e4c681
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/05/2022
ms.locfileid: "8548066"
---
# <a name="database-movement-toolkit"></a>データベース移動ツールキット

データベース移動ツールキットは、Microsoft Dynamics Lifecycle Services (LCS) にホストされる ZIP ファイルです。 このツールキットをダウンロードできます。 開発環境とサンドボックス環境との間でのデータ移動に関するカスタマー エクスペリエンスを高める一連のスクリプトが含まれています。 このトピックでは、ツールキットのコンポーネント、ダウンロード方法、および最近の変更点について説明します。

## <a name="download-the-latest-version"></a>最新バージョンのダウンロード

ツールキットは、LCS 共有アセット ライブラリの **モデル** セクションで入手できます。  **データベース移動ツールキット** というタイトルのエントリを検索し、Tier1 DevTest 環境にダウンロードします。  

## <a name="toolkit-components"></a>ツールキット コンポーネント

このツールキットには、次の主要コンポーネントが含まれています。

- **Sqlpackage.exe** - このツールは Microsoft Azure SQL データベース、および Tier1 DevTest にホストされている SQL Server データベースに対して、抽出および公開アクションを実行するために使用します。  
- **PowerShell 7.0** - これは、並列処理機能を含む PowerShell の自己完結型バージョンであり、環境間でのデータ転送のパフォーマンスが向上します。  
- **PowerShell スクリプト** - AX 2012 データのアップグレードのようなシナリオでのエクスペリエンスを向上させ、自動化するためのスクリプトがいくつか用意されています。

## <a name="supported-scenarios"></a>サポートされているシナリオ

現在、このツールキットは次のシナリオをサポートしています。 今後、さらに追加される予定です。  

* [AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード](/d365F-O/fin-ops-core/dev-itpro/database/data-upgrade-self-service)

## <a name="versions"></a>バージョン

### <a name="version-5"></a>バージョン 5
| 機能 | 細目 |
| :------ | :------ |
| スキーマの発行 | CleanupSource および Cleanupsource スクリプトが追加されました。|
| データ転送 | 移動時間をキャプチャするためのタイマーが追加されました。|

### <a name="version-4"></a>バージョン 4
| 機能 | 細目 |
| :------ | :------ |
| スキーマの発行 | マイナーな改良。|

### <a name="version-3"></a>バージョン 3
| 機能 | 細目 |
| :------ | :------ |
| スキーマの発行 | PublishDiag.log にエラーを出力するようにスクリプトが修正されました。|

### <a name="version-2"></a>Version 2
| 機能 | 細目 |
| :------ | :------ |
| スキーマの発行 | Sqlpackage ディレクトリで現在のディレクトリ参照を使用するようにスクリプトが修正されました。|
| スキーマの発行 | ソース データベースからローカル ユーザーを削除し、環境固有のテーブルを整理するようにスクリプトが修正されました。|
| データ転送 | 欠落している PowerShell モジュールをインストールするようにスクリプトが修正されました。|

### <a name="version-1"></a>Version 1
| 機能 | 細目 |
| :------ | :------ |
| 初期 | ツールキットは LCS 共有 アセット ライブラリにアップロード済み。|




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
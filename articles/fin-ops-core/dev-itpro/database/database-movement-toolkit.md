---
title: データベース移動ツールキット
description: このトピックでは、データベース移動ツールキット (開発環境環境とサンドボックス環境との間でデータを移動するためのカスタマー エクスペリエンスを高める一連のスクリプト) をダウンロードして使用する方法について説明します。
author: laneswenka
manager: AnnBe
ms.date: 09/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 30
ms.openlocfilehash: 2cd828a8a5874f9e26c27097e210a43336c561de
ms.sourcegitcommit: 42dbebced4a99dfe703689b7e38c3c5caecd12e1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949238"
---
# <a name="database-movement-toolkit"></a>データベース移動ツールキット

データベース移動ツールキットは、Microsoft Dynamics Lifecycle Services (LCS) にホストされる ZIP ファイルです。 このツールキットをダウンロードできます。 開発環境とサンドボックス環境との間でのデータ移動に関するカスタマー エクスペリエンスを高める一連のスクリプトが含まれています。 このトピックでは、ツールキットのコンポーネント、ダウンロード方法、および最近の変更点について説明します。

## <a name="download-the-latest-version"></a>最新バージョンのダウンロード

ツールキットは、LCS 共有アセット ライブラリの**モデル** セクションで入手できます。  **データベース移動ツールキット**というタイトルのエントリを検索し、Tier1 DevTest 環境にダウンロードします。  

## <a name="toolkit-components"></a>ツールキット コンポーネント

このツールキットには、次の主要コンポーネントが含まれています。

- **Sqlpackage.exe** - このツールは Microsoft Azure SQL データベース、および Tier1 DevTest にホストされている SQL Server データベースに対して、抽出および公開アクションを実行するために使用します。  
- **PowerShell 7.0** - これは、並列処理機能を含む PowerShell の自己完結型バージョンであり、環境間でのデータ転送のパフォーマンスが向上します。  
- **PowerShell スクリプト** - AX 2012 データのアップグレードのようなシナリオでのエクスペリエンスを向上させ、自動化するためのスクリプトがいくつか用意されています。

## <a name="supported-scenarios"></a>サポートされているシナリオ

現在、このツールキットは次のシナリオをサポートしています。 今後、さらに追加される予定です。  

* [AX 2012 からのアップグレード - サンドボックス環境でのデータ アップグレード](../migration-upgrade/upgrade-data-sandbox-dacpac.md)

## <a name="versions"></a>バージョン

### <a name="version-1"></a>Version 1
| 機能 | 細目 |
| :------ | :------ |
| 初期 | ツールキットは LCS 共有 アセット ライブラリにアップロード済み。|



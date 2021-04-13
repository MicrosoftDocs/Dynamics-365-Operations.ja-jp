---
title: AX 2009 アップグレード - データ移行ツールを使用して、Dynamics AX 2009から Finance and Operations へ移行します。
description: このトピックでは、データ移行ツール (DMT) を使用して、 Microsoft Dynamics AX 2009 から Finance and Operations へデータを移行する方法を説明します。
author: kfend
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 291170f4581e40d294394644e871cdbfda57ea99
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751354"
---
# <a name="ax-2009-upgrade---use-the-data-migration-tool-to-migrate-from-dynamics-ax-2009-to-finance-and-operations"></a>AX 2009 アップグレード - データ移行ツールを使用して、Dynamics AX 2009から Finance and Operations へ移行します。 

[!include [banner](../includes/banner.md)]

AX 2009 から Finance and Operations へデータを移行するため Microsoft Dynamics AX 2009 データ移行ツール (DMT) を使用することができます。 DMT の使用は、唯一サポートされている AX 2009 からのアップグレード パスです。 DMT は、各バージョンのテーブル スキーマ間を検索してその間のギャップを埋めることができ、またデータを移動も行います。 

> [!NOTE]
> クラウドへの移行を開始するときは、[Dynamics 365移行プログラム](https://dynamics.microsoft.com/migration-program/)を使用した場合でも、無料で義務なしの移行評価を使用します。

## <a name="architecture"></a>アーキテクチャ
次の図では、DMT のアーキテクチャ、また、ソース システム (AX 2009) のデータの処理方法とターゲット システム (Finance and Operations) への移動方法について説明します。

![データ移行の技術フロー](media/dmt_technical_flow.png)

## <a name="data-migration-process"></a>データ移行プロセス

次の図で、AX 2009 インスタンスでデータを収集して準備し、新しい環境にそのデータをインポートする全体的なプロセスを示します。

![データ移行プロセス](media/dmt_process_flow.PNG)

DMT を使用してソース環境 (AX 2009) からデータをエクスポートする前に、次の前処理のタスクを完了させておく必要があります。

- ソース環境とターゲット環境との間のテーブル フィールドのマッピング
- ソース データへの変換の適用
- ソース データの既定値の設定
- クエリ フィルターの適用

ソース システムには複数の法人が存在することがあるため、移行するデータを含む法人を選択する必要があります。 選択した法人について、ソース テーブルとその行カウントを確認します。 仮想会社を表示することもできます。 最後に、法人が関連付けられている仮想会社と関連するテーブルを分析できます。

エクスポートしたデータの移行を成功させるには、ソース テーブルが同等のターゲット データ エンティティにマップされていることが必要です。 各テーブルのソースフィールドとターゲットフィールドの自動マッピングを可能にする Microsoft Excel マッピングファイルを使用してマッピングを設定します。 マッピング ファイルには、新しいデータ エンティティのスキーマからのデータと、いくつかのテーブルで必要な既定のデータも含まれます。

AX 2009 からデータを移行する前に、移行の要件を満たすために次のタスクを完了しておく必要があります。

- 選択した法人に基づいてに入力されたソース分析コードに対応する目標の分析コードを選択します。
- 選択した法人に含まれている在庫分析コードを確認します。
- 各法人の勘定科目表を選択するか、単一の勘定科目に複数の法人を連結します。
- 基本的な元帳設定を実行します。
- フィールドの拡張データ型 (EDT) に基づき、ソース データにデータ変換を適用します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
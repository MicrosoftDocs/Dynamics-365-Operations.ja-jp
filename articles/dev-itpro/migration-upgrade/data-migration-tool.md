---
title: "AX 2009 アップグレード - Dynamics AX 2009 から Dynamics 365 for Finance and Operations に移行するデーの移行ツールを使用する"
description: "このトピックでは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行するために、データ移行ツール (DMT) を使用する方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.translationtype: HT
ms.sourcegitcommit: 1aae5797e37b846a38f957b02870e213da528a2d
ms.openlocfilehash: c69143953d77d25de7eda971875b4ff9a81addb0
ms.contentlocale: ja-jp
ms.lasthandoff: 09/20/2018

---

# <a name="ax-2009-upgrade---use-the-data-migration-tool-to-migrate-from-dynamics-ax-2009-to-dynamics-365-for-finance-and-operations"></a>AX 2009 アップグレード - Dynamics AX 2009 から Dynamics 365 for Finance and Operations に移行するデーの移行ツールを使用する 

[!include [banner](../includes/banner.md)]

AX 2009 から Microsoft Dynamics 365 for Finance and Operations にデータを移行するために、Microsoft Dynamics AX 2009 データ移行ツール (DMT) を使用できます。 DMT の使用は、AX 2009 から Finance and Operations へのアップグレード パスでのみサポートされます。 DMT では、AX 2009 と Finance and Operations のテーブル スキーマを検索してその間のギャップを埋めることができるだけでなく、データを移動できます。 

## <a name="archictecture"></a>アーキテクチャ
次の図では、DMT のアーキテクチャ、ソース システム (AX 2009) のデータの処理方法とターゲット システム (Finance and Operations) に移動する方法について説明します。

![データ移行の技術フロー](media/dmt_technical_flow.png)

## <a name="data-migration-process"></a>データ移行プロセス

次の図では、AX 2009 インスタンスでデータを収集して準備し、Finance and Operations 環境にそのデータをインポートする全体的なプロセスを示します。

![データ移行プロセス](media/dmt_process_flow.PNG)

DMT を使用してソース環境 (AX 2009) からデータをエクスポートするには、次の処理前の作業を行う必要があります。

- ソース環境とターゲット環境との間のテーブル フィールドのマッピング
- ソース データへの変換の適用
- ソース データの既定値の設定
- クエリ フィルターの適用

ソース システムには複数の法人が存在することがあるため、移行するデータを含む法人を選択する必要があります。 選択した法人について、ソース テーブルとその行カウントを確認します。 仮想会社を表示することもできます。 最後に、法人が関連付けられている仮想会社と関連するテーブルを分析できます。

エクスポートしたデータの移行を成功させるには、ソース テーブルが同等のターゲット データ エンティティにマップされていることが必要です。 マッピングを設定するには、各テーブルのソース フィールドとターゲット フィールドの自動マッピングを可能にする Microsoft Excel マッピング ファイルを使用します。 マッピング ファイルには、データ エンティティの Finance and Operations スキーマからのデータと、いくつかのテーブルで必要な既定のデータも含まれます。

AX 2009 から Finance and Operations にデータを移行する前に、移行の要件を満たすために次の作業を実行する必要があります。

- 選択した法人に基づいてに入力されたソース分析コードに対応する目標の分析コードを選択します。
- 選択した法人に含まれている在庫分析コードを確認します。
- 各法人の勘定科目表を選択するか、単一の勘定科目に複数の法人を連結します。
- 基本的な元帳設定を実行します。
- フィールドの拡張データ型 (EDT) に基づき、ソース データにデータ変換を適用します。


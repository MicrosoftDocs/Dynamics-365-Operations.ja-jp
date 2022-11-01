---
title: 銀行仕訳帳の複合エンティティの更新
description: この記事では、追加の BankTransactionType フィールドを複合 BankJournalEntity に追加するために必要な手順を示します。
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer
ms.reviewer: kfend
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1855f9680ba6bcf8eb46608882a128b4a21f0dac
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715293"
---
# <a name="update-the-bank-journal-composite-entity"></a>銀行仕訳帳の複合エンティティの更新

[!include [banner](../includes/banner.md)]

この記事では、追加の BankTransactionType フィールドを複合 BankJournalEntity に追加するために必要な手順を示します。

次の手順を使用して、複合の BankJournalEntity に追加の BankTransactionType フィールドを追加します。

1.  次の銀行仕訳帳の複合エンティティ、エンティティ、ステージング テーブルをコンパイルして同期:
    -   複合エンティティ\\銀行仕訳帳エンティティ
    -   エンティティ\\銀行仕訳帳ヘッダー エンティティ
    -   エンティティ\\銀行仕訳帳明細行エンティティ
    -   テーブル\\銀行仕訳帳ヘッダー ステージング
    -   テーブル\\銀行仕訳帳明細行ステージング

2.  データ管理\\データ プロジェクト
    -   **データ ソース** レイアウトの **銀行トランザクション** タイプを公開します。
        -   ソースデータ形式 = XML-Element
        -   エンティティ名 = 銀行仕訳帳
        -   データ ファイルのアップロード = 新しいバージョンの SampleBankJournalCompositeEntity.xml
        -   既存のファイルを上書きするには、**はい** をクリックします。
        -   最初からマッピングを生成するためには、**はい** をクリックします。
        -   銀行トランザクション タイプがマップされていることを確認します。
            -   明細行エンティティの **マップの表示** をクリックします。
            -   銀行トランザクション タイプがソースからステージングにマップされたことを確認します。

3.  新しい明細書をインポートします。






[!INCLUDE[footer-include](../../includes/footer-banner.md)]

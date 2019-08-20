---
title: 銀行仕訳帳の複合エンティティの更新
description: 追加のBankTransactionType フィールドに複合 BankJournalEntity を追加するには以下の手順が必要です。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 974d6b3b11df92debdec26860fd9eea00a9f2313
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841780"
---
# <a name="update-the-bank-journal-composite-entity"></a>銀行仕訳帳の複合エンティティの更新

[!include [banner](../includes/banner.md)]

追加のBankTransactionType フィールドに複合 BankJournalEntity を追加するには以下の手順が必要です。

次の手順を使用して、複合の BankJournalEntity に追加の BankTransactionType フィールドを追加します。

1.  次の銀行仕訳帳の複合エンティティ、エンティティ、ステージング テーブルをコンパイルして同期:
    -   複合エンティティ\\銀行仕訳帳エンティティ
    -   エンティティ\\銀行仕訳帳ヘッダー エンティティ
    -   エンティティ\\銀行仕訳帳明細行エンティティ
    -   テーブル\\銀行仕訳帳ヘッダー ステージング
    -   テーブル\\銀行仕訳帳明細行ステージング

2.  データ管理\\データ プロジェクト
    -   **データ ソース**レイアウトの**銀行トランザクション**タイプを公開します。
        -   ソースデータ形式 = XML-Element
        -   エンティティ名 = 銀行仕訳帳
        -   データ ファイルのアップロード = 新しいバージョンの SampleBankJournalCompositeEntity.xml
        -   既存のファイルを上書きするには、**はい**をクリックします。
        -   最初からマッピングを生成するためには、**はい** をクリックします。
        -   銀行トランザクション タイプがマップされていることを確認します。
            -   明細行エンティティの **マップの表示** をクリックします。
            -   銀行トランザクション タイプがソースからステージングにマップされたことを確認します。

3.  新しい明細書をインポートします。





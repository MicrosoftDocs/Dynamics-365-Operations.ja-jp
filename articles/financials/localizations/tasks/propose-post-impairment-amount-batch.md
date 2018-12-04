--- 
title: "バッチごとの減損損失の提案と転記"
description: "このタスクは、バッチによる減損損失額の提案と転記について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f9cb207312fa5b73bd840a1bbadf40bc268483f2
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---

# <a name="propose-and-post-the-impairment-amount-by-batch"></a>バッチごとの減損損失の提案と転記

[!include [task guide banner](../../includes/task-guide-banner.md)]

このタスクは、バッチによる減損損失額の提案と転記について説明します。 このタスクを完了するには、減損テストが確認され、保存されている必要があります。 この手順では、JPMF デモ会社のデータを使用します。

1. [固定資産] > [定期処理のタスク] > [減損提案] の順に移動します。
2. [仕訳帳名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [減損テスト ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
7. [バックグラウンドで実行] セクションを展開します。
8. [バッチ処理] フィールドで [はい] を選択します。
9. [仕訳帳の作成] をクリックします。
10. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
    * バッチは非同期的に処理されます。 仕訳帳はまだ作成されていない可能性があります。  
11. ページを更新します。
    * ページを更新して、最新の情報を表示できます。 バッチがいつ処理されるかによっては、複数回更新する必要がある場合があります。  
12. 一覧で、目的のレコードを見つけ、選択します。
    * バッチがいつ処理されたかによっては、複数回ページを更新する必要がある場合があります。  
13. [明細行] をクリックします。
    * 固定資産が正しく作成され、減損損失額が正しいことを確認します。  
14. [転記] をクリックします。



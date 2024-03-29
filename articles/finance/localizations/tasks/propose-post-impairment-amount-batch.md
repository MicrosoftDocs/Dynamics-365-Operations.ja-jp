---
title: バッチごとの減損損失の提案と転記
description: このタスクは、バッチによる減損損失額の提案と転記について説明します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
ms.openlocfilehash: 88fa2d66d57a8e1cc1052ab78750a0b819750211
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275200"
---
# <a name="propose-and-post-the-impairment-amount-by-batch"></a>バッチごとの減損損失の提案と転記

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

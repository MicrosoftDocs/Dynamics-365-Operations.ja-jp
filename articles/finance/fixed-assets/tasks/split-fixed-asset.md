---
title: 固定資産の分割
description: この記事では、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880791"
---
# <a name="split-a-fixed-asset"></a>固定資産の分割

[!include [banner](../../includes/banner.md)]

この記事では、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。 

## <a name="create-a-new-fixed-asset"></a>新しい固定資産の作成

1. ナビゲーション ウィンドウで、**モジュール \> 固定資産 \> 固定資産 \> 固定資産** の順に移動します。
2. **新規** を選択します。
3. **固定資産グループ** フィールドで、値を入力または選択します。 分割処理で使用する固定資産番号を確認します。
4. **名前** フィールドに値を入力します。
5. フォームを閉じます。

## <a name="split-a-fixed-asset"></a>固定資産の分割

減価償却の対象となる資産を完全に分割する前に、資産帳簿のステータスを手動で **終了** から **オープン** に変更する必要があります。 この手順が必要となるのは、資産のトランザクションを転記する必要がある場合 (処分販売など) には、帳簿のステータスを **オープン** にする必要があるためです。 また、**総勘定元帳パラメーター** ページの **一般** タブで、**1 つの伝票内で複数のトランザクションを許可する** パラメーターもオンにする必要があります。 資産帳簿のステータスが変更され、1 つの伝票内の複数のトランザクションが許可された後に、次の手順を実行して資産を分割します。

1. 一覧で、分割する固定資産のリンクを選択します。
2. **帳簿** を選択します。 新しい資産に分割する帳簿を選択します。
3. **機能** を選択します。
4. **固定資産の分割** を選択します。
5. **分割先固定資産** フィールドで、値を入力または選択します。
6. **次の帳簿まで** フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。
7. **トランザクション日付** フィールドに、日付を入力します。
8. **割合** フィールドに数を入力します。
9. **仕訳帳名** フィールドで、値を入力または選択します。
10. **OK** を選択します。

## <a name="post-the-journal-transaction"></a>仕訳帳トランザクションの転記

1. ナビゲーション ウィンドウで、**モジュール \> 固定資産 \> 仕訳帳エントリー \> 固定資産の仕訳帳** に移動します。
2. リストで、分割処理で作成された仕訳帳を選択します。
3. **明細行** を選択します。

    - 作成した仕訳帳明細行を確認します。
    - 取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。
    - 取得トランザクションは、新しい資産に対して同じ金額で作成されます。

4. **投稿** を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

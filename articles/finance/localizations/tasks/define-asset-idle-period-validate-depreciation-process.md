---
title: 資産のアイドル期間の定義および減価償却プロセスの検証
description: このタスクでは、固定資産のアイドル期間の定義について説明します。
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
ms.search.form: AssetParameters, AssetIdlePeriodAssign_JP, AssetTable, AssetBook, AssetIdlePeriodUpdate_JP, AssetProfile, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
ms.openlocfilehash: 9e6e317d6735bfa90554db89bd94bdb70ea4fe6d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280591"
---
# <a name="define-asset-idle-period-and-validate-depreciation-process"></a>資産のアイドル期間の定義および減価償却プロセスの検証

[!include [banner](../../includes/banner.md)]

このタスクでは、固定資産のアイドル期間の定義について説明します。 

プロファイルまたは提案を検証します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="assign-number-sequence-in-fa-parameter-form"></a>FA パラメーター フォームの番号順序の割り当て
1. [固定資産] > [設定] > [固定資産パラメーター] の順に移動します。
2. [番号順序] タブをクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * 照会 = 固定資産のアイドル期間  
4. [番号順序コード] フィールドで、値を入力または選択します。
5. [保存] をクリックします。
6. ページを閉じます。

## <a name="assign-idle-period-for-a-fixed-asset"></a>固定資産のアイドル期間の割り当て
1. [固定資産] > [定期処理のタスク] > [固定資産へのアイドル期間の割り当て] の順に移動します。
2. [新規] をクリックします。
3. [説明] フィールドに値を入力します。
4. [一般] セクションを展開します。
5. [開始日] フィールドに日付を入力します。
    * 開始日 = 01/01/2016  
6. [終了日] フィールドで、日付を入力します。
    * 終了日 = 12/31/2017  
7. [理由] フィールドに値を入力します。
8. [アイドル期間] セクションを展開します。
9. [新規] をクリックします。
10. [固定資産グループ] フィールドで、値を入力または選択します。
    * EQUP-M  
11. [固定資産番号] フィールドで、値を入力または選択します。
    * EQUPM-000024  
12. [帳簿] フィールドで値を入力または選択します。
    * 200NDB_CUR  
13. [保存] をクリックします。
14. [確認] をクリックします。
15. ページを閉じます。

## <a name="validate-fixed-asset-book"></a>[固定資産帳簿] の検証
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * EQUPM-000024  
3. [帳簿] をクリックします。
4. 一覧で、目的のレコードを見つけ、選択します。
    * 200NDB_CUR  
5. [機能] をクリックします。
6. [アイドル期間の更新] をクリックします。
    * 固定資産帳簿に対して作成されたアイドル期間の検証が一覧表示されます。  
7. ページを閉じます。
8. [プロファイル] をクリックします。
    * アイドル期間に対する減価償却がゼロと表示されるプロファイルを検証します。  
9. ページを閉じます。
10. ページを閉じます。
11. ページを閉じます。

## <a name="execute-depreciation-proposal"></a>償却提案の実行
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで値を入力または選択します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [提案] をクリックします。
7. [償却提案] をクリックします。
8. [終了日] フィールドで、日付を入力します。
    * 終了日 = 12/31/2017  
9. [対象に含めるレコード] セクションを展開します。
10. [フィルター] をクリックします。
11. [リセット] をクリックします。
12. 一覧で、選択された行をマークします。
    * フィールド = 固定資産番号  
13. [基準] フィールドで、値を入力または選択します。
    * EQUPM-000024  
14. 一覧で、目的のレコードを見つけ、選択します。
    * フィールド = 予約  
15. [基準] フィールドで、値を入力または選択します。
    * 200NDB_CUR  
16. [OK] をクリックします。
17. [OK] をクリックします。
    * アイドル期間に対して作成された特別償却の仕訳帳は検証なし  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

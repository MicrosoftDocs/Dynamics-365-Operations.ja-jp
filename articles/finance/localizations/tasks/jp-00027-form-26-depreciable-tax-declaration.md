---
title: JP-00027 減価償却税申告のフォーム 26
description: このタスクでは、登録番号の固定資産への割り当て方法と申告 26 レポートの印刷について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntity, LogisticsPostalAddress, SysLookupMultiSelectGrid, LogisticsAddressCityLookup, AssetLocation, AssetLocationEdit_JP, AssetGroup, AssetTable, LedgerJournalTable, LedgerJournalTransAsset, DefaultDashboard
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 955a3869203f74757a412028807879be6474f97046db349045f9423be06ff2c0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713116"
---
# <a name="jp-00027-form-26-for-depreciable-tax-declaration"></a>JP-00027 減価償却税申告のフォーム 26

[!include [banner](../../includes/banner.md)]

このタスクでは、登録番号の固定資産への割り当て方法と申告 26 レポートの印刷について説明します。

このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。

この手順では、JPMF デモ会社のデータを使用します。 この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="create-a-registration-number"></a>登録番号の作成
1. [組織管理] > [組織] > [法人] の順に移動します。
2. 登録 ID をクリックします。
3. [新規] をクリックします。
4. [目的] フィールドで、値を入力または選択します。
    * 目的 = 固定資産  
5. [名前または説明] フィールドに値を入力します。
6. [住所] セクションを展開します。
7. [国/地域] フィールドに値を入力します。
8. [都道府県] フィールドで値を入力または選択します。
9. [市町村] フィールドで値を入力または選択します。
10. [保存] をクリックします。
11. [登録 ID] セクションを展開します。
12. [追加] をクリックします。
13. [登録タイプ] フィールドで、値を入力または選択します。
14. [登録番号] フィールドに値を入力します。
15. [一般] タブをクリックします。
16. [有効開始] フィールドで、日付を入力します。
17. [減価償却方法] フィールドで、オプションを選択します。
18. [保存] をクリックします。

## <a name="create-a-fixed-asset-location-and-assign-registration-number"></a>固定資産の場所の作成および登録番号の割り当て
1. [固定資産] > [設定] > [固定資産の属性] > [固定資産の場所] に移動します。
2. [新規] をクリックします。
3. [場所] フィールドで、値を入力します。
4. [名前] フィールドに値を入力します。
5. [住所] セクションを展開します。
6. [新規] をクリックします。
7. [名前または説明] フィールドで値を入力または選択します。
8. [登録番号] フィールドで、値を入力または選択します。
9. [OK] をクリックします。
10. [保存] をクリックします。

## <a name="define-location-to-the-fixed-asset-group"></a>固定資産グループへの場所の定義
1. [固定資産] > [設定] > [固定資産グループ] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * たとえば、[VEHI-A] を選択します。  
3. [編集] をクリックします。
4. [場所] フィールドで値を入力または選択します。
5. [保存] をクリックします。

## <a name="create-a-fixed-asset"></a>固定資産の作成
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
3. [固定資産グループ] フィールドで、値を入力または選択します。
4. [場所] セクションを展開します。
    * 固定資産の場所の既定値の検証  

## <a name="create-an-acquisition"></a>取得の作成
1. [固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで値を入力または選択します。
4. [保存] をクリックします。
5. [明細行] をクリックします。
6. [日付] フィールドに日付を入力します。
7. [勘定] フィールドで、任意の値を指定します。
8. [借方] フィールドに数値を入力します。
9. [転記] をクリックします。

## <a name="verify-the-form-26-report"></a>申告 26 レポートの確認
1. [固定資産] > [照会およびレポート] > [減価償却資産申告レポート] > [申告 26: 償却資産税の元帳レポート] と移動します。
2. [暦年] フィールドで値を入力または選択します。
3. [事業所用家屋資産番号] フィールドで、値を入力または選択します。
4. [登録番号] フィールドで、値を入力または選択します。
    * 必要な場所でレポートを表示/保存します。  印刷レポートの検証、固定資産を登録番号ごとに分類してグループ化します。  
    * 同様の固定資産の分類 n グループが、申告 26-1 n 申告 26-2 レポートに提示されます  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
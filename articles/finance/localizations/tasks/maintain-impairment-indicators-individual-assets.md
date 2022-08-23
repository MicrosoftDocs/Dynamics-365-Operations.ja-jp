---
title: 個別資産の減損インジケーターの管理
description: このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。
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
ms.search.form: AssetTable, AssetBook, AssetImpairmentIndicator_JP, AssetImpairmentReview_JP, SysQueryForm
ms.openlocfilehash: ee4e192a4ce3d79e85d9193e0db6144fc59b20d0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285731"
---
# <a name="maintain-impairment-indicators-on-individual-assets"></a>個別資産の減損インジケーターの管理

[!include [banner](../../includes/banner.md)]

このタスクを使用して、個別資産の減損インジケーターの管理方法を把握します。



この手順を実行する前に、「減損会計の共通パラメーターの設定」タスクを実行します。 



この手順では、JPMF デモ会社のデータを使用します。


## <a name="update-impairment-indicator-on-a-single-fixed-asset"></a>単一の固定資産の減損インジケーターを更新
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
    * 例: TOOLM-000006  
3. [帳簿] をクリックします。
4. [機能] をクリックします。
5. [減損インジケーターの更新] をクリックします。
6. [新規] をクリックします。
7. [日付の変更] フィールドに、日付を入力します。
    * 例: 2013-04-01  
8. [説明] フィールドに値を入力します。
9. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * この例では、フィールドに「3900000」を入力します。  
10. [回収可能金額] フィールドに、数値を入力します。
    * この例では、フィールドに「3350226」を入力します。  
11. [保存] をクリックします。

## <a name="update-impairment-indicator-on-the-impairment-management-form"></a>減損管理フォームの減損のインジケーターを更新
1. 次の順に移動します: [固定資産] > > .. > [減損管理]。
2. [クエリ] をクリックします。
3. 固定資産グループの行の、[基準] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. [OK] をクリックします。
5. 一覧で、目的のレコードを見つけ、選択します。
    * TOOLM-000007  
6. 一覧で、目的のレコードを見つけ、選択します。
    * TOOLM-000008  
7. [減損インジケーターの更新] をクリックします。
8. 一覧で、選択された行をマークします。
    * 固定資産番号「TOOLM-000007」を持つレコードを選択します。  
9. [日付の変更] フィールドに、日付を入力します。
    * 日付を定義 = 2013-04-01  
10. [説明] フィールドに値を入力します。
11. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * 2500000.00 を入力します。  
12. [回収可能金額] フィールドに、数値を入力します。
    * 入力 = 2000000.00。  
13. 一覧で、目的のレコードを見つけ、選択します。
    * 固定資産番号「TOOLM-000008」を持つ行を選択します。  
14. [日付の変更] フィールドに、日付を入力します。
15. [説明] フィールドに値を入力します。
16. [割引前キャッシュ フロー] フィールドに数値を入力します。
    * 2000000.00 を入力します。  
17. [回収可能金額] フィールドに、数値を入力します。
    * 1500000.00 を入力します。  
18. [インジケーターの更新] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

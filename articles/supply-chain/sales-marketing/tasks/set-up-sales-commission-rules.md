---
title: 販売コミッション ルールの設定
description: この手順は、販売コミッションの計算および追跡を設定して有効にする方法を示します。
author: Henrikan
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f42f2fbe22124dbaaf2c4bd2f4394f734d166d5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578899"
---
# <a name="set-up-sales-commission-rules"></a>販売コミッション ルールの設定

[!include [banner](../../includes/banner.md)]

この手順は、販売コミッションの計算および追跡を設定して有効にする方法を示します。 この手順は、顧客と品目両方のコミッション グループの作成方法、次に各グループに選択した顧客と製品をリンクする方法を示します。 これらのグループは次にコミッション計算の設定で使用されます。これらは、販売担当者にコミッションを与えるために、販売注文と合致する、顧客、品目、販売担当者の組み合わせである必要があります。 顧客および品目のコミッション グループの作成は、コミッションの計算が個々の顧客および/または品目に対してもできるため、オプションとなっています。 この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。


## <a name="set-up-commission-groups-and-commission-rates"></a>コミッション グループとコミッション レートの設定
1. **ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > コミッション > コミッションの顧客グループ** の順に移動します。
2. **新規** を選択します。
3. **グループ** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **保存** を選択します。
6. ページを閉じます。
7. **ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > コミッション > 品目グループ** の順に移動します。
8. **新規** を選択します。
9. **グループ** フィールドに値を入力します。
10. **名前** フィールドに値を入力します。
11. **保存** を選択します。
12. ページを閉じます。
13. **販売とマーケティング > コミッション > 販売グループ** の順に移動します。
    - コミッション売上グループは、該当するセールス グループに関連する顧客が、特定の商品を購入した場合にコミッションを受け取る資格がある、販売担当者ロールの従業員を指定します。  
    - USMF のデモ データの会社では、「米国販売担当者」と呼ばれる売上グループがあります。  
14. **アクション ウィンドウ** で、**一般** を選択します。
15. **販売担当者** をクリックします。 販売担当者 ページは、特定のコミッション グループに関連付けられる会社の販売担当者の一覧を表示します。 同じグループに複数の販売担当者を割り当て、パーセンテージ値として合計コミッション料金のそれぞれの比率を定義することができます。 すべての従業員のコミッション分配の合計は 100 を超えることはできません。 
16. 一覧で、選択された行をマークします。
17. **編集** を選択します。
18. **コミッション分配** を '50' に設定します。
19. **新規** をクリックします。
20. **名前** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
21. **クイック フィルター** を使用して、レコードを見つけます。 たとえば、「Susan Burk」という値で [名前] フィールドをフィルターします。
22. **選択** をクリックします。
23. **コミッション分配** を '50' に設定します。
24. **保存** をクリックします。
25. **販売とマーケティング > コミッション > コミッションの計算** の順に移動します。 **コミッションの計算** ページで、顧客および製品の事前設定された組み合わせが含まれる場合に、従業員が販売トランザクションに対して受け取るコミッション レートを定義します。 コミッション レートの設定の一部として、コミッションの計算基準、および割引を追加または除外するかどうかを指定します。 コミッション レートがいつ有効なのかという、有効期間の入力もできます。  
26. **新規** をクリックします。
27. **品目コード** フィールドで「グループ」を選択します。
28. **品目関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
29. 一覧で、以前に作成したグループを見つけ、選択します。
30. **顧客コード** フィールドで、'グループ' を選択します。
31. **顧客関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
32. 一覧で、以前に設定したグループを選択します。
33. **販売担当者関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
34. 一覧で、目的のレコードを見つけ、選択します。
    - 「行割引前」オプションを有効にしたままにします。  
    - コミッション値の計算の基礎になる、[収益] オプションを有効にしたままにします。    
35. [コミッション料率] フィールドに、数値を入力します。
36. **保存** をクリックします。

## <a name="setting-up-commission-posting"></a>コミッション転記の設定
1. **ナビゲーション ウィンドウ > 販売とマーケティング > コミッション > コミッションの転記** の順に移動します。 コミッション料金は従業員に支払うものであるため、**総勘定元帳** の適切な勘定に、適切な財務上の転記ができるように設定する必要があります。 これは、**コミッションの転記** ページで行われます。 現在の会社で使用できる設定を確認します。 通常、専用の経費勘定に対してコミッション金額が転記され、専用の支払勘定で相殺されます。 コミッション転記ルールの設定がない場合、システムは適用できるコミッションがある販売注文の請求を完了しません。  
2. ページを閉じます。

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a>顧客および製品のコミッション グループの割当
1. **ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 顧客 > すべての顧客** の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. 一覧で、選択された行のリンクをクリックします。
4. **編集** をクリックします。
5. **販売注文の既定値** セクションを展開します。
6. **コミッション グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、以前に作成したグループを選択します。
8. **売上グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
9. 一覧で、目的のレコードを見つけ、選択します。
10. **保存** をクリックします。
11. **ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品** の順に移動します。
12. **フィルター** を使用して、レコードを見つけます。 たとえば、「T0020」という値で [品目番号] フィールドをフィルターします。
13. 一覧で、選択された行のリンクをクリックします。
14. **編集** をクリックします。
15. **販売** セクションを展開します。
16. **コミッション グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
17. 一覧で、以前に作成したコミッショングループを選択します。
18. **保存** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
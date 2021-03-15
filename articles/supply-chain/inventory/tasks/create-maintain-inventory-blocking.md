---
title: 在庫ブロックの作成および管理
description: この手順では、在庫ブロックを使用することによって、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。
author: perlynne
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eab6730daa2eb7df0f91d99d1026d4736285fef9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000062"
---
# <a name="create-and-maintain-an-inventory-blocking"></a>在庫ブロックの作成および管理

[!include [banner](../../includes/banner.md)]

この手順では、在庫ブロックを使用することによって、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。 表示されているサンプル値を使用して、デモ データの会社 USMF の手順を実行できます。 この手順を開始する前に、使用可能な現物手持在庫の品目を設定する必要があります。


## <a name="create-an-inventory-blocking"></a>在庫ブロックの作成
1. **ナビゲーション ウィンドウ** で、**モジュール > 在庫管理 > 定期処理 > 在庫ブロック** の順に移動します。
2. **新規** をクリックします。
3. **品目番号** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、目的の品目を選択します。 ブロックする現物手持在庫の品目番号を選択します。 USMF を使用している場合、品目 M9201 を選択できます。  
5. **数量** フィールドに、数値を入力します。 品目 M9201 を使用する場合、200 未満を選択する必要があります。
6. **在庫分析コード** クイック タブを展開します。
7. **倉庫** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、目的のレコードを見つけ、選択します。 品目 M9201 を使用すると、倉庫 51 を選択できます。  
9. **保存** をクリックします。

## <a name="update-the-conditions-of-the-inventory-blocking"></a>在庫ブロックの条件の更新
1. **一般** クイック タブの **数量** フィールドに、数値を入力します。 [在庫数量] フィールドを更新し、ブロックする数量を反映します。  
2. **予定日** フィールドに日付を入力します。 予定日を割り当てることにより、ブロックされた在庫の引当可能日を指定することをお勧めします。 入庫予定オプションが在庫ブロックに対して選択されている場合、既定通り、ブロックを手動で作成する場合、この日付は予想されるトランザクションに表示されます。  
3. **保存** をクリックします。

## <a name="remove-the-inventory-blocking"></a>在庫ブロックの削除
1. **アクション ウィンドウ** で **削除** をクリックします。
2. **はい** をクリックします。
3. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
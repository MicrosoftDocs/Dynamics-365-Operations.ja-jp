---
title: 有効在庫数の確認
description: この手順では、特定の品目番号において現物手持在庫を確認する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3f6f601d2d48ede2c4db198ac5438aa32e056d
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829780"
---
# <a name="check-the-availability-of-stock"></a>有効在庫数の確認

[!include [banner](../../includes/banner.md)]

この手順では、特定の品目番号において現物手持在庫を確認する方法を示します。 またこれらは品目に関連する供給情報を取得する方法を表示します。 現物手持在庫とは使用可能である、つまり、購入済、受領済、登録済である手持在庫です。 手持在庫には使用可能な手持在庫が含まれる一方で、注文し、予定されているがまだ入庫されていない、または登録されていない在庫も含まれます。 デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。 USMF を使用すると、表示される例の値を使用できます。 通常、これらのタスクを実施するのは、倉庫作業者です。


## <a name="check-on-hand-inventory-for-an-item"></a>品目の手持在庫の確認
1. **ナビゲーション ウィンドウ > モジュール > 在庫管理 > 照会およびレポート > 手持在庫**の順に移動します。
2. **品目番号**行を選択します。 手持在庫を品目番号で照会するには、**手持在庫**が設定されているテーブルおよび**品目**番号が設定されているフィールドの行を選択します。
3. **基準**フィールドで、クエリする品目を選択します。 デモ データの会社 USMF を使用する場合は、「M9201」を選択できます。  
4. **OK**をクリックします。
5. **アクション ウィンドウ**で、**分析コード** をクリックします。 **分析コード**タブでは、自分の手持在庫をどれだけ詳細に表示するかを設定できます。 引当に関連するデータが必要な場合、高度な倉庫 (WMS) プロセスを使用する品目の在庫分析コードすべてを表示する必要があります。
6. **OK**をクリックします。
7. **アクション ウィンドウ**で、**関連情報**をクリックします。 このオプションが表示されない場合、追加のアクション ウィンドウの選択を確認するには、省略記号ボタン (…) をクリックする必要があります。
8. **供給の概要**をクリックします。 **供給の概要**タブには、手持在庫の数量、リード タイム、仕入先情報などの特定の品目における供給情報が表示されます。  
9. **手持**セクションを展開します。
10. **仕入先**セクションを展開します。
11. ページを閉じます。
12. ページを閉じます。

## <a name="check-physical-on-hand-inventory"></a>現物手持在庫の確認
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 照会およびレポート > 現物手持在庫**の順に移動します。
2. **品目番号**フィールドに値を入力します。 品目の一覧をフィルタ処理するための [サイト] および[倉庫] フィールドを使用できます。 
3. ページを更新します。
4. **アクション ウィンドウ**で、**分析コードの表示**をクリックします。 分析コード表示タブでは、自分の手持在庫をどれだけ詳細に表示するかを設定できます。
5. **OK**をクリックします。
6. ページを閉じます。

## <a name="check-on-hand-inventory-by-location"></a>手持在庫を保管場所ごとに確認する
1. **ナビゲーション ウィンドウ > モジュール > 倉庫管理 > 照会およびレポート > 保管場所ごとの手持在庫**の順に移動します。
2. **倉庫**フィールドに値を入力します。 USMF のデモ データ会社を使用すると、「51」を使用できます。  
3. ページを更新します。
4. **分析コードの表示**をクリックします。
5. **OK**をクリックします。
6. ページを閉じます。


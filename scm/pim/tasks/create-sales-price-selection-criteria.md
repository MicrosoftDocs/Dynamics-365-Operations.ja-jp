--- 
title: "販売価格の選択基準の作成"
description: "この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 633628e6250baa74df544e814ce6e9656a2f0b06
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="create-sales-price-selection-criteria"></a>販売価格の選択基準の作成

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。 この手順では、少なくとも 1 つの販売価格モデルが必要です。 この例では、デモ データの会社 USMF でスピーカー ソリューションの販売価格モデルに対して価格モデルを使用します。 通常、製品マネージャーがこの手順を使用します。


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>既存の販売価格モデルへの新しい条件の追加
1. [製品バリアント モデルの定義] をクリックします。
2. [製品コンフィギュレーション モデル] をクリックします。
3. リストで、モデル名のリンクをクリックせずに、スピーカー ソリューションの製品モデルの行を選択します。
4. [アクション] ウィンドウで、[モデル] をクリックします。
5. [価格モデル基準] をクリックします。
6. [新規] をクリックします。
7. [名前] フィールドに「顧客グループ 10」と入力します。
    * 価格モデル基準の名前を使用すると、基礎の選択基準を特定する場合に役立ちます。  
8. [価格モデル] フィールドで値を入力または選択します。
9. [注文タイプ] フィールドで [販売注文] を選択します。
    * 注文タイプで、選択クエリで使用できるデータベース フィールドが決まります。  
10. [発効日] フィールドに日付を入力します。
11. [有効期限] フィールドに、日付を入力します。
12. [保存] をクリックします。

## <a name="create-the-query-for-the-selection-criteria"></a>選択基準のクエリの作成
1. [編集] をクリックします。
2. [テーブル] フィールドで、[顧客] を選択します。 
3. [フィールド] フィールドで、[顧客グループ] を選択します。
    * この例では、選択基準に特定の顧客グループを使用します。  
4. [基準] フィールドで、[顧客グループ 10] を選択します。 
5. [OK] をクリックします。



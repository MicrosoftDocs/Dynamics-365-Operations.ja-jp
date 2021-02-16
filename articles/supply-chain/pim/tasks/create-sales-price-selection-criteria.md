---
title: 販売価格の選択基準の作成
description: この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431954"
---
# <a name="create-sales-price-selection-criteria"></a>販売価格の選択基準の作成

[!include [banner](../../includes/banner.md)]

この手順では、属性ベースの販売価格モデルに対して販売価格の選択基準を作成する方法を示します。 この手順では、少なくとも 1 つの販売価格モデルが必要です。 この例では、デモ データの会社 USMF でスピーカー ソリューションの販売価格モデルに対して価格モデルを使用します。 通常、製品マネージャーがこの手順を使用します。


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>既存の販売価格モデルへの新しい条件の追加
1. [製品バリアント モデルの定義] をクリックします。
2. [製品コンフィギュレーション モデル] をクリックします。
3. リストにて、モデル名のリンクをクリックせずに、スピーカー ソリューション製品モデルの行を選択します。
4. [アクション] ウィンドウで、[モデル] をクリックします。
5. [価格モデル基準] をクリックします。
6. [新規] をクリックします。
7. [名前] フィールドに 「顧客グループ 10」 と入力します。
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


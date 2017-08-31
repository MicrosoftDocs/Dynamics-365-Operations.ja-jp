--- 
title: "コンフィギュレーション可能な製品の属性ベースの価格決定の設定"
description: "この手順では、属性ベースの価格を設定する方法を示します。"
author: BibiSp
manager: AnnBe
ms.date: 10/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 473d01ecddfd58aa72a972ee901673534c9d7c9c
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>コンフィギュレーション可能な製品の属性ベースの価格決定の設定

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、属性ベースの価格を設定する方法を示します。 前提条件として、1 つ以上のコンポーネントと属性を持つ製品コンフィギュレーション モデルが必要です。 この例では、デモ データの会社 USMF のハイエンド スピーカーの製品モデルが使用されています。 通常、製品マネージャーがこの手順を使用します。


## <a name="create-a-new-price-model"></a>新しい価格モデルの作成
1. [製品バリアント モデルの定義] をクリックします。
2. [製品コンフィギュレーション モデル] をクリックします。
3. リストで、名前のリンクをクリックせずにハイエンド スピーカーの行を選択します。
4. [アクション] ウィンドウで、[モデル] をクリックします。
5. [価格モデル] をクリックします。
6. [新規] をクリックします。
7. [価格モデル名] フィールドに値を入力します。
    * 容易にモデルを識別できる名前を使用します。  
8. [説明] フィールドに値を入力します。
9. [保存] をクリックします。

## <a name="add-price-elements"></a>価格要素の追加
1. [編集] をクリックします。
    * 製品モデルの各コンポーネントごとに、価格の式のルールの基準価格要素および任意の数字を設定できます。 異なる通貨でも価格を追加できます。  
2. [基準価格の式] フィールドに値を入力します。
    * たとえば、「100」と入力します。   基準価格の式は、数値あるいは 1 つ以上の属性を含む算術計算で構成できます。  
3. [追加] をクリックします。
4. [名前] フィールドに、「シタン」と入力します。
    * 価格の式の名前は、価格要素が表す内容を識別する場合に役立ちます。 この例では、シタンのスピーカー キャビネットの仕上げオプションに対する価格要素を作成します。  
5. [条件の編集] をクリックします。
    * 価格の条件によって、属性の特定の組み合わせがある場合にのみ、価格の式の要素を確実に販売価格に含められます。  
6. [ConstraintBody] フィールドで、「CabinetFinish=="シタン"」と入力します。
7. [OK] をクリックします。
8. [式フィールド] に値を入力します。
    * たとえば、「50」と入力します。  
9. ページを閉じます。
10. ページを閉じます。



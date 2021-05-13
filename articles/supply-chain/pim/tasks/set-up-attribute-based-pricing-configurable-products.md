---
title: コンフィギュレーション可能な製品の属性ベースの価格決定の設定
description: このトピックでは、属性ベースの価格決定の方法を説明します。
author: ShylaThompson
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelList, PCPriceModel, PCConstraintEditor
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c30c520e7265c2676937f5191844f6789c364e6
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921244"
---
# <a name="set-up-attribute-based-pricing-for-configurable-products"></a>コンフィギュレーション可能な製品の属性ベースの価格決定の設定

[!include [banner](../../includes/banner.md)]

このトピックでは、属性ベースの価格決定の方法を説明します。 前提条件として、1 つ以上のコンポーネントと属性を持つ製品コンフィギュレーション モデルが必要です。 この例では、デモ データの会社 USMF のハイエンド スピーカーの製品モデルが使用されています。 通常、製品マネージャーがこの手順を使用します。


## <a name="create-a-new-price-model"></a>新しい価格モデルの作成

1. **製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。
1. リストで、名前のリンクを選択せずに、**ハイ エンド スピーカー** 行を選択します。
1. アクション ウィンドウで、**モデル** を選択します。
1. **価格モデル** を選択します。
1. **新規** を選択します。
1. **価格モデル名** フィールドに、値を入力します。 容易にモデルを識別できる名前を使用します。  
1. **説明** フィールドで、値を入力します。
1. **保存** を選択します。

## <a name="add-price-elements"></a>価格要素の追加

1. **編集** を選択します。 製品モデルの各コンポーネントごとに、価格の式のルールの基準価格要素および任意の数字を設定できます。 異なる通貨でも価格を追加できます。  
2. **基準価格の式** フィールドに、値を入力します。 たとえば、「100」と入力します。 基準価格の式は、数値あるいは 1 つ以上の属性を含む算術計算で構成できます。  
3. **追加** を選択します。
4. **名前** フィールドに、`Rosewood` と入力します。 価格の式の名前は、価格要素が表す内容を識別する場合に役立ちます。 この例では、シタンのスピーカー キャビネットの仕上げオプションに対する価格要素を作成します。  
5. **条件の編集** を選択します。 価格の条件によって、属性の特定の組み合わせがある場合にのみ、価格の式の要素を確実に販売価格に含められます。  
6. **ConstraintBody** フィールドに、`CabinetFinish=="Rosewood"` と入力します。
7. **OK** を選択します。
8. **式** フィールドに、値を入力します。 たとえば、`50` と入力します。 
9. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
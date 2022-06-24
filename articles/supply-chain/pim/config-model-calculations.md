---
title: 製品の構成モデルの計算
description: この記事では、製品の構成モデルの属性の計算を作成する方法について説明します
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35057a4fc59732fea24e4d953cafed633a936ec1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878935"
---
# <a name="product-configuration-model-calculations"></a>製品の構成モデルの計算

[!include [banner](../includes/banner.md)]

この記事では、製品の構成モデルの属性の計算を作成する方法について説明します。

## <a name="prerequisites"></a>必要条件

製品の構成モデルで計算を使用して、製品の構成値を計算することもできます。 計算の設定を開始する前に、関連する製品の構成モデルが存在している必要があります。 構成モデルの設定プロセスの概要と関連するタスクについては、[製品構成モデルの設定](set-up-maintain-product-configuration-model.md)を参照してください。

## <a name="create-a-calculation"></a>計算の作成

計算は、式とターゲットとなる属性で構成されます。 詳細については、[製品構成モデルの計算方法の FAQ](calculate-product-configuration-models.md) を参照してください。

既存の製品モデルの計算を作成するには、次の手順に従います。

1. **製品情報管理 \> 共通 \> 製品構成モデル** に移動します。
1. 製品の構成モデルを選択し、**編集** をクリックします。
1. **計算** クイック タブで、**追加** を選択して計算を追加し、次のフィールドを設定します :

    - **名前** – 計算の名前を入力します。
    - **説明** – 計算の説明を入力します。
    - **目標属性** - 計算の対象となる属性を選択します。

1. **式の編集** を選択します。
1. **計算の入力** ダイアログ ボックスで、必要な属性、演算子、値を式に追加します。 これら要素の使用方法の詳細については、[製品構成モデルにおける式の制約およびテーブル制約](expression-constraints-table-constraints-product-configuration-models.md)を参照してください。
1. 式の準備の完了後、**OK** を選択します。

## <a name="calculation-examples"></a>計算の例

このセクションでは、計算の機能を示すいくつかの例を示します。

### <a name="example-1"></a>例 1

次の例では、ターゲットの属性はブール型で、次の条件式を使用しています :

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

この式は、`decimalAttribute2` が `decimalAttribute1` より大きいか等しい場合は *True* 値をターゲット属性に返します。 それ以外の場合は、*False* のブール値が返されます。

### <a name="example-2"></a>例 2

この例では、テキスト属性 `textFixedList` をターゲット属性として使用します。 この属性には、次の固定リストが含まれます。

| 先頭値 | ソルバー値 |
|---|---|
| A | 1a |
| B | 2b |
| 貸方 | 2c |

次のスクリーンショットは、この属性の設定がご利用のシステムでどのように表示されるかを示しています。

![例 2 で使用する属性タイプの設定。](media/model-calculations-example2.png "例 2 で使用する属性タイプの設定")

この属性は、次の条件付きステートメントで使用されます :

`If[integerAttribute < 150, 0, 2]`

`integerAttribute` が 150未満の場合、このステートメントは固定リスト *A* の最初のレコードのテキスト値 を返します。それ以外の場合は、固定リスト *C* の 3 番目のレコードのテキスト値を返 します。

> [!NOTE]
> 固定リストはゼロ ベースのリスト (enum) と同等であり、その値は適切な整数値によってアクセスされます。 したがって、最初の固定リスト値 (*A*) は *0* に、2番目の値 (*B*) は *1* に、3番目の値 (*C*) は *2* に一致します。

### <a name="example-3"></a>例 3

この例では、前述の例の `textFixedList` ターゲット属性を使用しています。 また、もうひとつのテキスト属性である `textAttribute` を使用しており、その中には以下の固定リストが含まれています。

| 先頭値 | ソルバー値 |
|---|---|
| AA | 1aa |
| BB | 2bb |

次のスクリーンショットは、この属性の設定がご利用のシステムでどのように表示されるかを示しています。

![例 3 で使用する属性タイプの設定。](media/model-calculations-example3.png "例 3 で使用する属性タイプの設定")

`textFixedList` 属性の値は、以下の条件付きステートメントを用いて算出されます :

`If[textAttribute == "1aa", 0, 2]`

`textAttribute` の値が *1aa* に相当するソルバー値を持つ場合、この式は、 `textFixedList` 固定リストの最初のレコードである *A* のテキスト値を返します。それ以外の場合は、`textFixedList` 固定リストの3番目のレコード、*C* のテキスト値を返します。

> [!NOTE]
> - 条件付きステートメントは、属性のオプションの値を使用する必要があります。
> - 計算に使用できるのは、固定リストのテキスト属性のみです。

## <a name="see-also"></a>参照

- [製品コンフィギュレーション モデルの計算についてよく寄せられる質問](calculate-product-configuration-models.md)
- [製品コンフィギュレーション モデルへ式の制約の追加](tasks/add-expression-constraint-product-configuration-model.md)
- [製品コンフィギュレーション モデルの概要](product-configuration-models.md)

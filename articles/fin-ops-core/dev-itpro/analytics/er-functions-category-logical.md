---
title: 論理カテゴリ内の ER 関数のリスト
description: この記事では、電子申告 (ER) でサポートされる論理関数について説明します。
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 1d011968d9cfa4125e7283ca36c3558e3e79b93a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291297"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>論理カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子レポート (ER) 論理関数を使用して、論理値を操作して単一の式で複数の比較を実行したり、複数の条件をテストしたりできます。 この記事では、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務 | 説明 |
|----------|-------------|
| [かつ](er-functions-logical-and.md)                       | この関数は、指定したすべての条件が true である場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [ケース](er-functions-logical-case.md)                     | この関数は、指定された代替オプションに対して指定された式の値を評価し、指定された式の値に等しい最初のオプションの結果を返します。 それ以外の場合は、オプションの前にはない、呼び出された関数の最後の引数としてデフォルト結果が指定されている場合、オプションのデフォルト結果を返します。 返される値は、サポートされているいずれかのデータ型の値にすることができます。 |
| [次の値を含む](er-functions-logical-contains.md)             | この関数は、指定された入力に指定されたテキストが含まれるかどうかを決定します。 指定された入力が指定されたテキストを含む場合、関数は *TRUE* の **ブール値** を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [EndsWith](er-functions-logical-endswith.md)             | この関数は、指定された入力が指定されたテキストで終了するかどうかを決定します。 指定された入力が指定されたテキストで終了する場合、 関数は *TRUE* の **ブール値** を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [次の場合](er-functions-logical-if.md)                         | この関数は、特定の条件が満たされている場合、最初に指定された値を返します。 それ以外の場合、2 つ目に指定された値を返します。 返される値は、サポートされているいずれかのデータ型の値にすることができます。 |
| [ない](er-functions-logical-not.md)                       | この関数は、指定された条件の取消論理値を *ブール* 値として返します。 |
| [Or](er-functions-logical-or.md)                         | この関数は、指定したすべての条件が false である場合、**FALSE** の *ブール* 値を返します。 指定した任意の条件が true である場合、関数は **TRUE** の *ブール* 値を返します。 |
| [StartsWith](er-functions-logical-startswith.md)         | この関数は、指定された入力が指定されたテキストで始まるかどうかを決定します。 指定された入力が指定されたテキストで始まる場合、 関数は *TRUE* の **ブール値** を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [ValueIn](er-functions-logical-valuein.md)               | この関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。 指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | この関数は、*Int64* あるいは *整数* タイプの指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。 指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の *ブール* 値を返します。 それ以外の場合は、**FALSE** の *ブール* 値が返されます。 |


## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

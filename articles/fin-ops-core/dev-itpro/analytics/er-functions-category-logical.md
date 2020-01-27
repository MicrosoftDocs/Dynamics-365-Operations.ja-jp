---
title: 論理カテゴリ内の ER 関数のリスト
description: このトピックでは、電子申告 (ER) でサポートされる論理関数について説明します。
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 408b3c5ec37b24e0ccf6e368012a936701eedf0f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916640"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>論理カテゴリ内の ER 関数のリスト

[!include [banner](../includes/banner.md)]

電子レポート (ER) 論理関数を使用して、論理値を操作して単一の式で複数の比較を実行したり、複数の条件をテストしたりできます。 このトピックでは、これらの関数の概要を示します。

## <a name="list-of-supported-functions"></a>サポートされている関数のリスト

| 職務 | 説明 |
|----------|-------------|
| [かつ](er-functions-logical-and.md)                       | この関数は、指定したすべての条件が true である場合、**TRUE** の*ブール*値を返します。 それ以外の場合は、**FALSE** の*ブール*値が返されます。 |
| [ケース](er-functions-logical-case.md)                     | この関数は、指定された代替オプションに対して指定された式の値を評価し、指定された式の値に等しい最初のオプションの結果を返します。 それ以外の場合は、オプションの前にはない、呼び出された関数の最後の引数としてデフォルト結果が指定されている場合、オプションのデフォルト結果を返します。 返される値は、サポートされているいずれかのデータ型の値にすることができます。 |
| [次の場合](er-functions-logical-if.md)                         | この関数は、特定の条件が満たされている場合、最初に指定された値を返します。 それ以外の場合、2 つ目に指定された値を返します。 返される値は、サポートされているいずれかのデータ型の値にすることができます。 |
| [ない](er-functions-logical-not.md)                       | この関数は、指定された条件の取消論理値を*ブール*値として返します。 |
| [Or](er-functions-logical-or.md)                         | この関数は、指定したすべての条件が false である場合、**FALSE** の*ブール*値を返します。 指定した任意の条件が true である場合、関数は **TRUE** の*ブール*値を返します。 |
| [ValueIn](er-functions-logical-valuein.md)               | この関数は指定された入力が、指定されたリスト内の指定された項目の値と一致するかどうかを決定します。 指定された入力が、指定されたリストの少なくとも 1 つのレコードに対して指定された式を実行した結果と一致する場合、**TRUE** の*ブール*値を返します。 それ以外の場合は、**FALSE** の*ブール*値が返されます。 |

## <a name="additional-resources"></a>追加リソース

[電子申告の概要](general-electronic-reporting.md)

[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

[電子報告のフォーミュラ言語](er-formula-language.md)

---
title: GETENUMVALUEBYNAME ER 機能
description: このトピックでは、GETENUMVALUEBYNAME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 33ccf358dc5355cd00d5ff41ebd8148a334cba38
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743858"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER 機能

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` 関数は、*文字列*値して指定された列挙名を使用して、指定された列挙データソースの特定の*列挙*値を検索します。 *列挙*値が見つかった場合、関数によって返されます。 それ以外の場合、関数は **null** 列挙値を返します。

## <a name="syntax"></a>構文

```vb
GETENUMVALUEBYNAME (enumeration data source path, enumeration value text)
```

## <a name="arguments"></a>引数

`enumeration data source path`: *列挙型*

次のいずれかの列挙型のデータ ソースの有効なパス。

- 電子申告 (ER) モデル 列挙型
- ER 形式列挙型
- Microsoft Dynamics 365 Finance 列挙型

`enumeration value text`: *文字列*

単一の列挙型値の名前を表す文字列値。

## <a name="return-values"></a>戻り値

Nullable *列挙*

結果列挙型の値。

## <a name="usage-notes"></a>使用上の注意

*文字列*値として指定された列挙型値の名前を使用して*列挙*値が見つからない場合は、例外がスローされません。

## <a name="example"></a>例

次の図では、**ReportDirection**の列挙はデータ モデルで導入されます。 列挙型値のラベルが定義されていることに注意してください。

<p><a href="./media/ER-data-model-enumeration-values.PNG"><img src="./media/ER-data-model-enumeration-values.PNG" alt="Available values for a data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

次の図は、これらの詳細について説明しています。

- **$Direction** データソースが、ER レポートで構成されます。 このデータ ソースは、**ReportDirection** モデルの列挙型に基づいて構成されます。
- `$IsArrivals` 式は、この関数のパラメーターとして **$Direction** データ ソースに基づきモデル列挙型を使用するため設計されています。
- この比較式の値は、**TRUE** です。

<a href="./media/ER-data-model-enumeration-usage.PNG"><img src="./media/ER-data-model-enumeration-usage.PNG" alt="Example of data model enumeration" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

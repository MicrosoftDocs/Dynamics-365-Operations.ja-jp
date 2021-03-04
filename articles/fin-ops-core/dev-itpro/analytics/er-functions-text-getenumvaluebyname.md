---
title: GETENUMVALUEBYNAME ER 機能
description: このトピックでは、GETENUMVALUEBYNAME 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29d7ec6498090ea47259303237c5a64a26e4926b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685934"
---
# <a name="getenumvaluebyname-er-function"></a>GETENUMVALUEBYNAME ER 機能

[!include [banner](../includes/banner.md)]

`GETENUMVALUEBYNAME` 関数は、*文字列* 値して指定された列挙名を使用して、指定された列挙データソースの特定の *列挙* 値を検索します。 *列挙* 値が見つかった場合、関数によって返されます。 それ以外の場合、関数は **null** 列挙値を返します。

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

*文字列* 値として指定された列挙型値の名前を使用して *列挙* 値が見つからない場合は、例外がスローされません。

## <a name="example-1"></a>例 1

次の図では、**ReportDirection** の列挙はデータ モデルで導入されます。 列挙型値のラベルが定義されていることに注意してください。

![データ モデル列挙に使用可能な値](./media/ER-data-model-enumeration-values.PNG)

次の図は、これらの詳細について説明しています。

- **$Direction** データソースが、ER レポートで構成されます。 このデータ ソースは、**ReportDirection** モデルの列挙型に基づいて構成されます。
- `$IsArrivals` 式は、この関数のパラメーターとして **$Direction** データ ソースに基づきモデル列挙型を使用するため設計されています。
- この比較式の値は、**TRUE** です。

![データ モデル列挙の例](./media/ER-data-model-enumeration-usage.PNG)

## <a name="example-2"></a>例 2

`GETENUMVALUEBYNAME` および [`LISTOFFIELDS`](er-functions-list-listoffields.md) 関数を使用すると、サポートされている列挙の値とラベルをテキスト値としてフェッチできます。 (サポートされている列挙は、アプリケーション列挙、データ モデル列挙、形式列挙です。)

次の図では、**TransType** データ ソースはモデル マッピングで導入されます。 このデータ ソースは、**LedgerTransType** アプリケーション列挙を参照しています。

![アプリケーション列挙を参照するモデル マッピングのデータ ソース](./media/er-functions-text-getenumvaluebyname-example2-1.png)

次の図は、モデル マッピングで構成されている **TransTypeList** データ ソースを示しています。 このデータ ソースは、**TransType** アプリケーション列挙に基づいて構成されます。 この `LISTOFFIELDS` 関数は、すべての列挙値を、フィールドを含むレコードの一覧として返すために使用します。 このようにして、すべての列挙値の詳細が公開されます。

> [!NOTE]
> **EnumValue** フィールドは、`GETENUMVALUEBYNAME(TransType, TransTypeList.Name)` 式を使用して **TransTypeList** データソースに対して構成されます。 このフィールドは、このリストのすべてのレコードの列挙値を返します。

![選択した列挙のすべての列挙値をレコードの一覧として返すモデル マッピングのデータ ソース](./media/er-functions-text-getenumvaluebyname-example2-2.png)

次の図は、モデル マッピングで構成されている **VendTrans** データ ソースを示しています。 このデータ ソースは、**VendTrans** アプリケーション テーブルから仕入先トランザクション レコードを返します。 すべてのトランザクションの元帳タイプは、**TransType** フィールドの値によって定義されます。

> [!NOTE]
> **TransTypeTitle** フィールドは、`FIRSTORNULL(WHERE(TransTypeList, TransTypeList.EnumValue = @.TransType)).Label` 式を使用して **VendTrans** データソースに対して構成されます。 このフィールドは、この列挙値が使用可能な場合に、現在のトランザクションの列挙値のラベルをテキストとして返します。 それ以外の場合は、空白文字列の値を返します。
>
> **TransTypeTitle** フィールドは、データ モデルの **LedgerType** フィールドにバインドされ、データ ソースとしてデータモデルを使用するすべての ER 形式でこの情報を使用できます。

![仕入先トランザクションを返すモデル マッピングのデータ ソース](./media/er-functions-text-getenumvaluebyname-example2-3.png)

次の図は、[データ ソース デバッガー](er-debug-data-sources.md) を使用して、構成済みモデル マッピングをテストする方法を示しています。

![データ ソース デバッガーを使用して、構成済モデル マッピングをテストする](./media/er-functions-text-getenumvaluebyname-example2-4.gif)

データ モデルの **LedgerType** フィールドは、期待どおりにトランザクション タイプのラベルを公開します。

大量のトランザクション データにこのアプローチを使用する場合は、実行パフォーマンスを考慮する必要があります。 詳細については、[電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング](trace-execution-er-troubleshoot-perf.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

[電子申告形式の実行をトレースしてパフォーマンスの問題をトラブルシューティング](trace-execution-er-troubleshoot-perf.md)

[LISTOFFIELDS ER 関数](er-functions-list-listoffields.md)

[FIRSTORNULL ER 関数](er-functions-list-firstornull.md)

[WHERE ER 関数](er-functions-list-where.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
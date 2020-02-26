---
title: FORMAT ER 関数
description: このトピックでは、FORMAT 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: b09efeb6b5d8bd2ea452dbf7a9ddaeec2ab75c92
ms.sourcegitcommit: 0455a024185f79ecb82df61e6d994bd71dee5c10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/20/2020
ms.locfileid: "2974295"
---
# <a name="FORMAT">FORMAT ER 関数</a>

[!include [banner](../includes/banner.md)]

`FORMAT` 関数は、*N* 番目の引数で **%N** の出現を置き換えることで書式設定した後に、*文字列*値として指定された文字列を返します。

## <a name="syntax"></a>構文

```
FORMAT (string, argument 1[, argument 2, …, argument N])
```

## <a name="arguments"></a>引数

`string`: *文字列*

書式設定が必要な*文字列*タイプのデータ ソースを参照。 この引数は必須です。

`argument 1`: *文字列*

**%1** の出現に置き換えるために使用される最初の引数。 この引数は必須です。

`argument N`: *文字列*

**%2**、**%3** などの出現に置き換えるために使用される *N* 番目の引数。 これらの追加引数はオプションです。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

パラメーターに引数が指定されない場合は、文字列内では **"%N"** として返されます。 *実数*型の値では、既定の文字列変換が小数点第 2 位に制限されます。

## <a name="example"></a>例

次の図では、**PaymentModel** データ ソースが**顧客**コンポーネントを使用して顧客レコードの一覧を返します。 **ProcessingDate** フィールドを使用して、処理日の値を返します。

<a href="./media/picture-format-datasource.jpg"><img src="./media/picture-format-datasource.jpg" alt="PaymentModel data source" class="alignnone wp-image-290751 size-full" width="293" height="143" /></a>

選択した顧客の電子ファイルを生成するよう設計されている電子申告 (ER) 形式では、**PaymentModel** がデータ ソースとして選択され、プロセス フローを制御します。 選択した顧客がレポートを処理される日付に停止されている場合、例外であることをユーザーに通知し、スローされます。 このタイプの処理制御のために設計された式は、次のリソースを使用できます。

- 次のテキストを含むラベル SYS70894:

    - **EN-US 言語の場合:** "Nothing to print"
    - **DE 言語の場合:** "Nichts zu drucken"

- 次のテキストを含むラベル SYS18389:

    - **EN-US 言語の場合:** "顧客 %1 は停止 %2。"
    - **DE 言語の場合:** "Debitor '%1' wird für %2 gesperrt."

設計できる式を次に示します。

```
FORMAT (CONCATENATE (@"SYS70894", ". ", @"SYS18389"), model.Customer.Name, DATETIMEFORMAT (model.ProcessingDate, "d"))
```

レポートが 2015 年 12 月 17 日に **EN-US** カルチャおよび **EN-US** 言語で **Litware Retail** の顧客に対して処理される場合、この式は例外メッセージとしてユーザーに示すことができる次のテキストを返します:

*印刷するものはありません。顧客の Litware Retail は 12/17/2015 に停止されます。*

同じレポートが 2015 年 12 月 17 日に **DE** カルチャおよび **DE** 言語で **Litware Retail** の顧客に対して処理される場合、この式は別の日付形式を使用する次のテキストを返します。

*Nichts zu drucken。 Debitor 'Litware Retail' wird für 17.12.2015 gesperrt。*

>[!NOTE]
> 次の構文は ER の式でラベルに適用されます。
>
> - **Microsoft Dynamics 365 Finance アプリにあるリソースからのラベルの場合:** **\@X** がアプリケーション オブジェクト ツリー (AOT) のラベル ID にある **X**
> - **ER コンフィギュレーションに存在するラベルの場合:** **X** が ER コンフィギュレーションのラベル ID にある **@"GER_LABEL:X"**

## <a name="additional-resources"></a>追加リソース

[テキスト関数](er-functions-category-text.md)

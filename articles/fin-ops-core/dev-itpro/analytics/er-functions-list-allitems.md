---
title: ALLITEMS ER 関数
description: このトピックでは、ALLITEMS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1eae005a71f50a08c1ef85a7a93c3b2c407c8848
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559227"
---
# <a name="allitems-er-function"></a>ALLITEMS ER 関数

[!include [banner](../includes/banner.md)]

`ALLITEMS` 関数は、メモリ内の選択範囲として実行され、指定したパスと一致するすべての品目を表すレコードの一覧として、新しいフラット化した *レコード リスト* 値を返します。

## <a name="syntax"></a>構文

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>引数

`path`: *レコード リスト*

*レコード リスト* データ型のデータ ソースの項目の有効なパス。

## <a name="return-values"></a>戻り値

*レコード リスト*

レコードの結果リスト。

## <a name="usage-notes"></a>使用上の注意

パスは、*レコード リスト* データ型のデータ ソースの要素の有効なデータ ソース パスとして定義する必要があります。 パス文字列や日付などのデータ要素は、デザイン時に電子申告 (ER) 式ビルダーでエラーを生成する必要があります。

大量のデータが含まれる可能性のあるトランザクション データ ソースには、この関数を使用しないことをお勧めします。 代わりに、[ALLTEMSQUERY](er-functions-list-allitemsquery.md) 関数の使用を検討してください。

## <a name="example-1"></a>例 1

データソース **DS** として `SPLIT("abcdef" , 2)` を入力すると、`COUNT( ALLITEMS (DS))` 式は **3** を返します。

## <a name="example-2"></a>例 2

VendTable アプリケーション テーブルを参照する *レコード リスト* データ タイプのデータ ソースとして **Vend** を入力すると、`ALLITEMS (Vend.'<Relations'.ContactPerson)` 式は、**ContactPerson** テーブル構造を持ち、**ContactPerson.ContactForParty == VendTable.Party** 関係を使用してアクセスできるすべての連絡担当者を含み、参照された仕入先テーブルから仕入先に利用可能なレコードのフラット化されたリストを返します。

## <a name="additional-resources"></a>追加リソース

[リスト機能](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
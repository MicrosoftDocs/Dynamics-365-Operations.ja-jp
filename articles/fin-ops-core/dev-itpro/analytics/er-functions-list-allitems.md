---
title: ALLITEMS ER 関数
description: このトピックでは、ALLITEMS 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 15ab88512e49b51dbefa19056c3e1846715dcadb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687771"
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
---
title: NUMSEQVALUE ER 機能
description: このトピックでは、NUMSEQVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
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
ms.openlocfilehash: fbe5e5ac17af743f8293e4255d9713b528182f66
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041311"
---
# <a name="NUMSEQVALUE">NUMSEQVALUE ER 機能</a>

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` 関数は、指定された番号順序、範囲、およびスコープ ID に基づいて、番号順序の新しい生成値を表す*文字列*値を返します。 スコープ ID は、電子申告 (ER) 形式が実行されるコンテキストによって提供される会社コードと同じです。

## <a name="syntax-1"></a>構文 1

```vb
NUMSEQVALUE (number sequence code)
```

## <a name="syntax-2"></a>構文 2

```vb
NUMSEQVALUE (number sequence record ID)
```

## <a name="syntax-3"></a>構文 3

```vb
NUMSEQVALUE (number sequence code, scope type, scope ID)
```

## <a name="arguments"></a>引数

`number sequence code`: *文字列*

新しい値で必要な番号順序のコードを表すテキスト値。

`number sequence record ID`: *Int64*

新しい値で必要な番号順序の定義を含む、NumberSequenceTable テーブルの記録 ID を表す *Int64* 値。

`scope type`: *列挙値*

新しい値が必要な番号順序のスコープを定義する **ERExpressionNumberSequenceScopeType** 列挙型の列挙値。 使用可能な範囲タイプは、**共有**、**法人**、および**会社**です。

`scope ID`: *文字列*

指定したスコープ タイプに基づいて、スコープを識別する*文字列*値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

**共有**スコープ タイプでは、スコープ ID として空の文字列を指定します。

**会社**および**法人**スコープ タイプでは、会社コードとスコープ ID を指定します。 これらのスコープ タイプのスコープ ID として空の文字列を指定した場合、現在の会社コードが使用されます。

構文 1 を使用すると、番号順序が**会社**スコープ タイプに対して要求され、会社コードが ER 形式を実行するコンテキストによって提供されます。

## <a name="example-1"></a>例 1

ERフォーマットでは、*ユーザー入力パラメータ*タイプの **AskNumSeq** データ ソースを定義します。 このデータ ソースは、**説明**の拡張データ型 (EDT) を参照しています。 次に、*計算フィールド*タイプの **NumSeq** データ ソースを定義します。 このデータ ソースは、式 `NUMSEQVALUE (AskNumSeq)` が含まれています。 **NumSeq** データ ソースが呼び出されると、ダイアログ ボックスにコードを入力することにより、実行時に指定された番号順序の新しい生成値が返されます。 **会社**スコープ タイプに対して番号順序が要求されます。 会社コードは、ER 形式を実行するコンテキストによって提供されます。

## <a name="example-2"></a>例 2

モデル マッピングでは、次のデータ ソースが定義されます。

- *テーブル*タイプの **LedgerParms** データ ソース。 このデータ ソースは、LedgerParameters テーブルを指します。
- *計算フィールド*タイプの **NumSeq** データ ソース。 このデータ ソースは、式 `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)` が含まれています。

**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用に一般会計パラメーターでコンフィギュレーションされた、番号順序の新しく生成された値を返します。 この番号順序は、仕訳帳を一意に識別し、トランザクションをリンクするバッチ番号として機能します。

## <a name="example-3"></a>例 3

モデル マッピングでは、次のデータ ソースが定義されます。

- Microsoft Dynamics 365 Finance *列挙型* タイプの **enumScope** データ ソース。 このデータ ソースは、**ERExpressionNumberSequenceScopeType** 列挙型を参照しています。
- *計算フィールド*タイプの **NumSeq** データ ソース。 このデータ ソースは、式 `NUMSEQVALUE ("Gene_1", enumScope.Company, "")` が含まれています。

**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用にコンフィギュレーションされた **Gene\_1** 番号順序の新しく生成された値を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)

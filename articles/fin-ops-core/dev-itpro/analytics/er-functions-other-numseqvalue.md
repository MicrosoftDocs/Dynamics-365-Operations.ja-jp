---
title: NUMSEQVALUE ER 機能
description: この記事では、NUMSEQVALUE 電子申告 (ER) 関数の使用方法についての情報を提供します。
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 62255f0a47d3c67468cf2cf3922a1886c29c03d6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271556"
---
# <a name="numseqvalue-er-function"></a>NUMSEQVALUE ER 機能

[!include [banner](../includes/banner.md)]

`NUMSEQVALUE` 関数は、指定された番号順序、範囲、およびスコープ ID に基づいて、番号順序の新しい生成値を表す *文字列* 値を返します。 スコープ ID は、電子申告 (ER) 形式が実行されるコンテキストによって提供される会社コードと同じです。

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

新しい値が必要な番号順序のスコープを定義する **ERExpressionNumberSequenceScopeType** 列挙型の列挙値。 使用可能な範囲タイプは、**共有**、**法人**、および **会社** です。

`scope ID`: *文字列*

指定したスコープ タイプに基づいて、スコープを識別する *文字列* 値。

## <a name="return-values"></a>戻り値

*文字列*

結果テキスト値。

## <a name="usage-notes"></a>使用上の注意

**共有** スコープ タイプでは、スコープ ID として空の文字列を指定します。

**会社** および **法人** スコープ タイプでは、会社コードとスコープ ID を指定します。 これらのスコープ タイプのスコープ ID として空の文字列を指定した場合、現在の会社コードが使用されます。

構文 1 を使用すると、番号順序が **会社** スコープ タイプに対して要求され、会社コードが ER 形式を実行するコンテキストによって提供されます。

## <a name="example-1"></a>例 1

ERフォーマットでは、*ユーザー入力パラメータ* タイプの **AskNumSeq** データ ソースを定義します。 このデータ ソースは、**説明** の拡張データ型 (EDT) を参照しています。 次に、*計算フィールド* タイプの **NumSeq** データ ソースを定義します。 このデータ ソースは、式 `NUMSEQVALUE (AskNumSeq)` が含まれています。 **NumSeq** データ ソースが呼び出されると、ダイアログ ボックスにコードを入力することにより、実行時に指定された番号順序の新しい生成値が返されます。 **会社** スコープ タイプに対して番号順序が要求されます。 会社コードは、ER 形式を実行するコンテキストによって提供されます。

## <a name="example-2"></a>例 2

モデル マッピングでは、次のデータ ソースが定義されます。

- *テーブル* タイプの **LedgerParms** データ ソース。 このデータ ソースは、LedgerParameters テーブルを指します。
- *計算フィールド* タイプの **NumSeq** データ ソース。 このデータ ソースは、式 `NUMSEQVALUE ( LedgerParameters.'numRefJournalNum()'.NumberSequenceId)` が含まれています。

**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用に一般会計パラメーターでコンフィギュレーションされた、番号順序の新しく生成された値を返します。 この番号順序は、仕訳帳を一意に識別し、トランザクションをリンクするバッチ番号として機能します。

## <a name="example-3"></a>例 3

モデル マッピングでは、次のデータ ソースが定義されます。

- Microsoft Microsoft Dynamics 365 Finance *列挙型* タイプの **enumScope** データ ソース。 このデータ ソースは、**ERExpressionNumberSequenceScopeType** 列挙型を参照しています。
- *計算フィールド* タイプの **NumSeq** データ ソース。 このデータ ソースは、式 `NUMSEQVALUE ("Gene_1", enumScope.Company, "")` が含まれています。

**NumSeq** データ ソースが呼び出されると、ER 形式が実行されているコンテキストを提供する会社用にコンフィギュレーションされた **Gene\_1** 番号順序の新しく生成された値を返します。

## <a name="additional-resources"></a>追加リソース

[その他 (ビジネス ドメインの特定の) 関数](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

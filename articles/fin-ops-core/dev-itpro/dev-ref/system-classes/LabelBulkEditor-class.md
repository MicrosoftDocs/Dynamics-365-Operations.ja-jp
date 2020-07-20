---
title: LabelBulkEditor クラス
description: このトピックでは、LabelBulkEditor クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7532c770f75df8fb61875cd44379216f9eb007e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502895"
---
# <a name="class-labelbulkeditor"></a>クラス LabelBulkEditor

[!include [banner](../../includes/banner.md)]

```xpp
class LabelBulkEditor extends Object
```

LabelBulkEditor クラスを使用すると、ラベル ファイルが簡単に変更されます。

## <a name="remarks"></a>備考

LabelBulkEditor クラスは、Label.bulkEditor() メソッドを通じてインスタンス化されます。 ラベル ファイルは、クラスのインスタンスが作成されたときに変更用に開かれ、インスタンスがガベージ コレクションされたときにラベル ファイルは閉じられます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                  |
|-------------------------------------------------------------|------------------------------------------------------------------------------|
| public boolean delete(str label)                            | 指定したラベルを削除します。                                                   |
| public boolean modify(str label, str text, \[str comment\]) | 指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。 |
| public void new()                                           | LabelBulkEditor クラスのインスタンスを初期化します。                        |

## <a name="method-delete"></a>メソッド delete

指定したラベルを削除します。

```xpp
public boolean delete(str label)
```

### <a name="parameters---delete"></a>パラメーター - delete

ラベル  
ラベル ID を指定する文字列。 文字列には、アットマーク (@)、ラベル ファイル ID、数字が含まれている必要があります。

### <a name="return-value---delete"></a>戻り値 - delete

ラベルが削除された場合は true。それ以外の場合は false。

## <a name="method-modify"></a>メソッド modify

指定されたラベル ID に関連付けられているテキストおよびコメントを変更します。

```xpp
public boolean modify(str label, str text, [str comment])
```

### <a name="parameters---modify"></a>パラメーター - modify

ラベル  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

テキスト  
ラベル ID に関連付けられているコメントを指定する文字列。

<!-- -->

comment  
ラベル ID に関連付けられているコメントを指定する文字列。

### <a name="return-value---modify"></a>戻り値 - modify

ラベルが修正された場合は true。それ以外の場合は false。

## <a name="method-new"></a>メソッド new

LabelBulkEditor クラスのインスタンスを初期化します。

```xpp
public void new()
```


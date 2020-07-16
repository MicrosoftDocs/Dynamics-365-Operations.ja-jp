---
title: MessageWin クラス
description: このトピックでは､MessageWin クラスについて説明します。
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
ms.openlocfilehash: 577832717070aee36945c03db716af3dcb121394
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502573"
---
# <a name="class-messagewin"></a>クラス MessageWin

[!include [banner](../../includes/banner.md)]

```xpp
class MessageWin extends Object
```

MessageWin クラスを使用すると、messageWindow クラスの開発環境にアクセスできます。

## <a name="remarks"></a>備考

さらに MessageWin オブジェクトをインスタンス化することができますが、画面上に同一のメッセージ ウィンドウを参照します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                        | 説明                                           |
|-------------------------------|-------------------------------------------------------|
| public void clear()           | メッセージ ウィンドウをクリアします。                            |
| public void activate()        | メッセージ ウィンドウを現在のアクティブ ウィンドウにします。 |
| public void addLine(str line) | 行をメッセージ ウィンドウに記述します。                  |

## <a name="method-clear"></a>メソッド clear

メッセージ ウィンドウをクリアします。

```xpp
public void clear()
```

## <a name="method-activate"></a>メソッド activate

メッセージ ウィンドウを現在のアクティブ ウィンドウにします。

```xpp
public void activate()
```

### <a name="remarks---activate"></a>備考 - activate

バージョン 2.11 より前に、行が追加されたり内容が消去されるとメッセージ ウィンドウがフォーカスを取得します。 バージョン 2.11 以降では、開発者は、メッセージ ウィンドウを一番上のウィンドウにするためにこのメソッドを呼び出す必要があります。

## <a name="method-addline"></a>メソッド addLine

行をメッセージ ウィンドウに記述します。

```xpp
public void addLine(str line)
```

### <a name="parameters---addline"></a>パラメーター - addLine

明細行  
メッセージ ウィンドウへの書き込み明細行を含む文字列。


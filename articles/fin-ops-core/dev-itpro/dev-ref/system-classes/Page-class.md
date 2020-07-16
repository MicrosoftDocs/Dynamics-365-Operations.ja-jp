---
title: Page クラス
description: このトピックでは、Page クラスについて説明します。
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
ms.openlocfilehash: 52354804795ee853738bea1e973a49942239192d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502532"
---
# <a name="class-page"></a>クラス ページ

[!include [banner](../../includes/banner.md)]


```xpp
class Page extends Object
```

このページ クラスでは、作成、読み取り、更新、および X++ コードおよびメタデータを削除できます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                        | 説明                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| public boolean actionPaneControlEnabled(str controlName, \[boolean enabled\]) | アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。 |
| public boolean actionPaneControlVisible(str controlName, \[boolean visible\]) | アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。 |
| public Array activeActionPaneTabNames()                                       |                                                                          |
| public Common activeRecord(str dataSourceName)                                | 特定のデータ ソース名の有効なレコードを取得します。                   |
| public str name()                                                             | ページの名前を取得します。                                               |
| public PageArgs pageArgs()                                                    | page 引数を取得します。                                                 |
| public xFormRun formRun()                                                     |                                                                          |

## <a name="method-actionpanecontrolenabled"></a>メソッド actionPaneControlEnabled

アクション ウィンドウ上のコントロールの有効なプロパティの値を設定または取得します。

```xpp
public boolean actionPaneControlEnabled(str controlName, [boolean enabled])
```

### <a name="parameters---actionpanecontrolenabled"></a>パラメーター - actionPaneControlEnabled

controlName  
アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。

<!-- -->

有効  
アクション ウィンドウ コントロールが有効かどうかを指定する値、オプション。

### <a name="return-value---actionpanecontrolenabled"></a>戻り値 - actionPaneControlEnabled

アクション ペイン コントロールが有効かどうかを指定するブール値。

## <a name="method-actionpanecontrolvisible"></a>メソッド actionPaneControlVisible

アクション ウィンドウ上のコントロールの表示されるプロパティの値を設定または取得します。

```xpp
public boolean actionPaneControlVisible(str controlName, [boolean visible])
```

### <a name="parameters---actionpanecontrolvisible"></a>パラメーター - actionPaneControlVisible

controlName  
アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。

<!-- -->

表示  
アクション ウィンドウ コントロールが表示されるかどうかを指定する値、オプション。

### <a name="return-value---actionpanecontrolvisible"></a>戻り値 - actionPaneControlVisible

アクション ペイン コントロールが表示されるかどうかを指定するブール値。

## <a name="method-activeactionpanetabnames"></a>メソッド activeActionPaneTabNames

```xpp
public Array activeActionPaneTabNames()
```

### <a name="return-value---activeactionpanetabnames"></a>戻り値 - activeActionPaneTabNames

## <a name="method-activerecord"></a>メソッド activeRecord

特定のデータ ソース名の有効なレコードを取得します。

```xpp
public Common activeRecord(str dataSourceName)
```

### <a name="parameters---activerecord"></a>パラメーター - activeRecord

dataSourceName  
検索するデータ ソースの名前。

### <a name="return-value---activerecord"></a>戻り値 - activeRecord

特定のデータ ソース用の有効なレコード。

## <a name="method-name"></a>メソッド名

ページの名前を取得します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

ページ名。

## <a name="method-pageargs"></a>メソッド pageArgs

page 引数を取得します。

```xpp
public PageArgs pageArgs()
```

### <a name="return-value---pageargs"></a>戻り値 - pageArgs

page 引数。

## <a name="method-formrun"></a>メソッド formRun

```xpp
public xFormRun formRun()
```

### <a name="return-value---formrun"></a>戻り値 - formRun


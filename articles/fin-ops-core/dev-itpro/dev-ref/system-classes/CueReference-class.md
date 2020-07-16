---
title: CueReference クラス
description: このトピックでは、CueReference クラスについて説明します。
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
ms.openlocfilehash: 6db6fee2a79542fb020d03e856943b4bce379e17
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502699"
---
# <a name="class-cuereference"></a>クラス CueReference

[!include [banner](../../includes/banner.md)]

```xpp
class CueReference extends TreeNode
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                | 説明                                                                                                                       |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| public str cue(\[str value\])         |                                                                                                                                   |
| public str name(\[str value\])        | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public void new(str cueReferenceName) | TreeNode クラスの新しいインスタンスを初期化します。                                                                                 |

## <a name="method-cue"></a>メソッド cue

```xpp
public str cue([str value])
```

### <a name="parameters---cue"></a>パラメーター - cue

値  

### <a name="return-value---cue"></a>戻り値 - cue

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - 名前

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - 名前

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めないでください。
-   テーブルは、拡張データ型、基本列挙型、クラス、他のパブリックオブジェクトなど、他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

```xpp
public void new(str cueReferenceName)
```

### <a name="parameters---new"></a>パラメーター - new

cueReferenceName  
このフォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前。




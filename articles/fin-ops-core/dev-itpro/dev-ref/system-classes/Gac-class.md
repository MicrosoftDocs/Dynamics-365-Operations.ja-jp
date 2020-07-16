---
title: Gac クラス
description: このトピックでは、Gac クラスについて説明します。
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
ms.openlocfilehash: 4bbc2e2d2275299da98d37a47a05282c9247d7c3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502612"
---
# <a name="class-gac"></a>クラス Gac

[!include [banner](../../includes/banner.md)]


```xpp
class Gac extends Object
```

Gac クラスを使用すると、グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙できます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                 | 説明                                                   |
|----------------------------------------|---------------------------------------------------------------|
| public container enumerateAssemblies() | グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。 |
| public void new()                      | Gac クラスの新しいインスタンスを初期化します。                  |

## <a name="method-enumerateassemblies"></a>メソッド enumerateAssemblies

グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。

```xpp
public container enumerateAssemblies()
```

### <a name="return-value---enumerateassemblies"></a>戻り値 - enumerateAssemblies

GAC のアセンブリを表すコンテナーです。

## <a name="method-new"></a>メソッド new

Gac クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```



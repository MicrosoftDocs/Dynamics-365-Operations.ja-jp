---
title: G クラス
description: 文字 G で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 52381
ms.assetid: 6d4b3577-f254-4702-9878-ec3863c033fa
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30525a5e2d44a57c31e57796565e8e4401d68ffe
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833682"
---
# <a name="g-classes"></a>G クラス

[!include [banner](../includes/banner.md)]

文字 G で始まるシステム API クラス。

<a name="class-gac"></a>クラス Gac
---------

    class Gac extends Object

Gac クラスを使用すると、グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙できます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                 | 説明                                                   |
|----------------------------------------|---------------------------------------------------------------|
| public container enumerateAssemblies() | グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。 |
| public void new()                      | Gac クラスの新しいインスタンスを初期化します。                  |

### <a name="method-enumerateassemblies"></a>メソッド enumerateAssemblies

グローバル アセンブリ キャッシュ (GAC) のアセンブリを列挙します。

    public container enumerateAssemblies()

#### <a name="return-value"></a>戻り値

GAC のアセンブリを表すコンテナーです。

### <a name="method-new"></a>メソッド new

Gac クラスの新しいインスタンスを初期化します。

    public void new()




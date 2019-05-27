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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52381
ms.assetid: 6d4b3577-f254-4702-9878-ec3863c033fa
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 68bb58cea4ef68c09668f36270290180b528b83e
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537034"
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




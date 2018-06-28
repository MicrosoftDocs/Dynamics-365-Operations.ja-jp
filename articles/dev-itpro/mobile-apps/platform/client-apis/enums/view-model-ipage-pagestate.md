---
title: PageState
description: "ページを配置できるさまざまな高レベルの状態を表します。"
author: shadykdc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: 
ms.search.region: Global
ms.author: kashea
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 953361ef80f3ea2408cdea3f9c07416b4c97c76d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="pagestate-enumeration"></a>PageState 列挙

[!include [banner](../../../../includes/banner.md)]

ページを配置できるさまざまな高レベルの状態を表します。

## <a name="index"></a>指数

### <a name="enumeration-members"></a>列挙型メンバー

* [エラー](view-model-ipage-pagestate.md#error)
* [読み込み済み](view-model-ipage-pagestate.md#loaded)
* [読み込み中](view-model-ipage-pagestate.md#loading)
* [オフライン](view-model-ipage-pagestate.md#offline)
* [更新中](view-model-ipage-pagestate.md#refreshing)

## <a name="enumeration-members"></a>列挙型メンバー

### <a name="error"></a>エラー

エラー: 10 ページは現在、エラー状態にありますが、更新することでこの状態から抜け出すことができます。


### <a name="loaded"></a>loaded

loaded: 3 ページが完全に読み込まれ、更新可能であり、可能ならば送信できます。


### <a name="loading"></a>loading

loading: 2 ページが現在読み込まれています。


### <a name="offline"></a>オフライン

offline: 1 ページはオフライン モードで読み込まれたので更新できません。


### <a name="refreshing"></a>更新中

更新中: 4 ページは現在データを更新中です。




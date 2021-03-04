---
title: PageState 列挙
description: ページを配置できるさまざまな高レベルの状態を表します。
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cceb74591e4186ca7f3951f396d2c6f98d425ad5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687316"
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




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]
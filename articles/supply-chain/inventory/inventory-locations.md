---
title: 在庫場所
description: 在庫場所は、品目の保存場所、および WMS I 倉庫で品目がピッキングされる場所を特定するために基本倉庫 (WMS I) で使用されます。
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 490f510ca0a5522d7bc892733ff066ebc65bcd24
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432370"
---
# <a name="inventory-locations"></a>在庫場所

[!include [banner](../includes/banner.md)]

在庫場所は、品目の保存場所、および WMS I 倉庫で品目がピッキングされる場所を特定するために基本倉庫 (WMS I) で使用されます。

このトピックは、在庫管理モジュールの機能に適用されます。 これは、倉庫管理モジュールの機能には適用されません。

場所という用語は、品目が保管され、取得元となる場所を意味します。

各在庫場所に対し、品目の挿入先も指定できます。 既定では、どちらも同じです。 通常、品目の挿入と取り出しが行われるのは在庫場所の同じ側ですが、常にそうであるわけではありません。 たとえば、常用保管ラックに格納される品目は、一方の通路から挿入されて、別の通路から取り出されます。 主な入力は、倉庫、通路、ラック、棚、および在庫置場などの座標によって決まる場所の名前で指定されます。 この名前または ID は、手動で入力することも、[在庫場所] ページの保管場所の座標から生成することもできます。たとえば、通路 1、ラック 2、棚 3、在庫置場 4 という座標の場合、ID は 01-02-03-4 になります。
在庫場所のプロパティ

在庫場所には次のような特性があります。
-   サイズ (高さ、幅、奥行き、およびこれらによる体積)
-   倉庫、通路、ラック、棚、在庫置場の位置
-   場所タイプ (バルク場所、ピッキング場所、入荷ドック、出荷ドック、生産入力の場所、検査場所、かんばんスーパーマーケット)

オンライン システムでチェック テキストを使用すると、オペレータが特定の品目に対して正しい在庫場所を選択したかどうかを確認できます。 このチェック テキストは手動で作成することも、既定で作成されるようにすることもできます。

## <a name="sort-codes"></a>並べ替えコード
並べ替えコードは、在庫からの品目のピッキングに必要な情報 (バルク オーダーなど) を示すもので、このコードを使用してピッキング ラインの処理を最適化できます。 並べ替えコードは、通路やその他の座標にで指定できるほか、場所に対して手動で割り当てることもできます。

## <a name="blocked-locations"></a>ブロックされた在庫場所
たとえば、修理などのために、在庫場所が一時的にブロックされていることを示す必要が生じることがあります。 他には、入力または出力のいずれか一方のみがブロックされていることを表示したい場合もあります。

## <a name="tree-structure"></a>ツリー構造

[在庫場所] ページでは、倉庫のレイアウトを、在庫場所の座標に基づいて、設定した形式でツリー構造で表示できます。

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a>倉庫フォームで在庫場所を管理

1 つの倉庫から別の倉庫に場所をコピーし、ウィザードによって場所を作成することができます。 ウィザードを実行する前に、[倉庫] ページで既定の場所の名前を定義してあることを確認する必要があります。



<a name="additional-resources"></a>追加リソース
--------

[新しい倉庫レイアウトの作成](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
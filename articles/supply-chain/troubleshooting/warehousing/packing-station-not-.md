---
title: 梱包ステーションに製品の注記が表示されない
description: 梱包ステーションに製品の注記が表示されません。
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSPack
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 18c8d2d392b7950ee2d5fc388fc3f365b52a6795c908f9ed8cac12dc7b481c60
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760349"
---
# <a name="packing-station-doesnt-show-product-notes"></a>梱包ステーションに製品の注記が表示されない

KB 番号: 4614615

## <a name="symptoms"></a>現象

梱包指示が製品マスターまたは製品バリアントの関連付けとして追加された場合、梱包明細は梱包フォームに表示されません。

## <a name="resolution"></a>解像度

システムはデザイン通り動作しています。

梱包フォームに梱包明細を表示する現在のロジックには、注記が出荷に関連付けられている必要があります。

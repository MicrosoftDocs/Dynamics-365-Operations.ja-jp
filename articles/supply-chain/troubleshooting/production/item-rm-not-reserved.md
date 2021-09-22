---
title: 製造オーダーのリリース時に品目 RM を引当できない
description: 製造オーダーをリリースすると、"品目 RM を完全に引当できません。" というエラーが表示される場合があります。 全数量が利用可能であることを確認するか、手動で品目を引当します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476903"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>製造オーダーのリリース時に品目 RM を完全に引当できない

## <a name="symptoms"></a>現象

製造オーダーが倉庫にリリースされるときに、すべての BOM 明細行品目が物理的に使用可能ではない場合で、**倉庫にリリース** ポリシーが *完全引当を要求* に設定されていると、次のエラー メッセージが表示されます。

> 品目 RM を完全に引当することはできません。 数量がすべて使用可能であることを確認するか、BOM 明細行の [引当] フィールドが [手動] または [開始] に設定されている場合は、品目を手動で引当します。 注文を倉庫にリリースできませんでした。一部の材料を引き当てることができませんでした。

## <a name="resolution"></a>解決策

この動作は仕様であり、期待どおりに機能しています。 この問題を修正するには、"BOM 明細行の引当フィールドが手動または開始済に設定されている場合は、全数量が利用可能であることを確認するか、手動で品目を引当してください。" というエラー メッセージの指示に従ってください。

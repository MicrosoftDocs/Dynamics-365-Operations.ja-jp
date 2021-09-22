---
title: 有効な BOM バージョンおよびルート番号が挿入できません
description: 既定のサイトと倉庫が選択された製品にすでに定義されている場合、有効な BOM バージョンとルート番号を挿入するようには求められません。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476829"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>新しい製造オーダーの作成時に部品表とルートを挿入できません

## <a name="symptoms"></a>現象

新しい製造オーダーを作成する場合は、品目番号を入力すると、**サイト** および **倉庫** フィールドが、完成品目の **既定の注文設定** ページで定義されている既定のサイトと倉庫に自動的に設定されます。 また、有効な BOM 番号とルート番号が自動的に入力されるため、値の入力を求める以下のメッセージが表示されません。

> 部品表および工順の有効なバージョンを挿入しますか?

## <a name="resolution"></a>解決策

**既定の注文設定** ページで、サイトと倉庫がすでにある製品を選択した場合、BOM と工順の番号を挿入するように求められることはありません。 選択した製品に対してこれらの値が定義されていない場合にのみ、プロンプトが表示されます。

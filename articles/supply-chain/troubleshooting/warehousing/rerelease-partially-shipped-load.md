---
title: 部分的に出荷された積荷を倉庫に再リリースできない
description: 以前のバージョンでは、不完全な予約で特定の機能を使用している場合は、部分的に出荷された積荷を再リリースすることができませんでした。 これは修正されました。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0380e1963a38f2be55b31e06b3845f935661eed2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476893"
---
# <a name="cant-re-release-a-partially-shipped-load-to-the-warehouse"></a>部分的に出荷された積荷を倉庫に再リリースすることはできません

## <a name="symptoms"></a>現象

部分的に出荷された積荷を倉庫にリリースすることはできません。 倉庫にリリースすると、「操作完了」のメッセージが表示されますが、何も発生せず、残りの数量に対して作業が作成されません。 この問題は、輸送積荷機能を使用しているときに不完全な引当がある場合に発生します。

## <a name="resolution"></a>解決策

[KB の問題 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("部分的に出荷された積荷が再ウェーブおよび再処理される") は[リリース 10.0.15](/dynamics365/supply-chain/get-started/whats-new-scm-10-0-15) で修正されています。

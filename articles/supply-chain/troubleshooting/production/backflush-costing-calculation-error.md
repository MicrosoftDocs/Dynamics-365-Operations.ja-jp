---
title: 在庫原価計算中の一括引き落とし原価計算エラー
description: 以前のリリースでは、在庫原価計算中に一括引き落とし原価計算エラーが発生する場合があります。 問題が修正されました。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476861"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>在庫原価計算中の一括引き落とし原価計算エラー

## <a name="symptoms"></a>現象

リリース 10.0.13 より前のリリースでは、リーン生産原価計算フローを使用していない場合は、在庫決算中に次の誤った警告メッセージが表示されます。

> 日付 %1 で在庫決算を実行しようとしています。 期末と一致する日付 %1 での一括引き落とし原価計算の実行が登録されていません。 期末と一致する日付 %1 での一括引き落とし原価計算を必ず実行してください。 補助元帳および総勘定元帳において、在庫評価、売却済商品の原価、および差異は、この処理が実行されるまで正しくない可能性があります。

## <a name="resolution"></a>解決策

この問題は、リリース 10.0.13 またはそれ以降で修正されています。 詳細については、[KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296) を参照してください。

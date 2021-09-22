---
title: 最後のジョブの部分的な数量が報告された場合に進行中のジョブが終了する
description: 製造オーダーの最後のジョブで部分的な数量を報告するためにジョブ カード デバイスを使用している場合、以前のジョブのうち、ステータスが進行中になっているものがすべて終了します。
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 11511d4ac7524facdd0d647e9bc38fe09c282be1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476918"
---
# <a name="previous-in-progress-jobs-are-ended-when-reporting-partial-quantity-on-last-job"></a>最後のジョブの部分的な数量が報告された場合に進行中のジョブが終了する

## <a name="symptoms"></a>現象

製造オーダーの最後のジョブで部分的な数量を報告するためにジョブ カード デバイスを使用している場合、そのオーダーの以前のジョブのうち、ステータスが進行中になっているものがすべて自動的に終了します。

## <a name="resolution"></a>解決策

この動作は仕様です。 **製造オーダーの既定値** ページの **完了レポート** タブに、**エンド マーク ルート** という名前のオプションがあります。 このトピックが *はい* に設定されている場合は、作業者がジョブ カード デバイスまたはジョブ カード ターミナルを使用して最後の工程を報告したときに、工順カード仕訳帳が転記されます。 この仕訳帳では、すべての工程が完了としてマークされ、すべての生産ジョブが終了します。 **エンド マーク ルート** オプションが *はい* に設定されている場合、システムは、前回の工程を報告したときに作業者が選択したジョブ ステータスを考慮しません。 また、作業者が数量の全体または一部を報告しているかどうかも考慮されません。

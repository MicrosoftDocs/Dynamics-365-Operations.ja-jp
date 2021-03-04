---
title: プロセス製造のトラブルシューティング
description: このトピックでは、プロセス製造を操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 63993fca2164301d31dbfa1474a4cf5eb16273e6
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516819"
---
# <a name="troubleshoot-process-manufacturing"></a>プロセス製造のトラブルシューティング

このトピックでは、プロセス製造を操作する際に発生する可能性がある問題の修正方法について説明します。

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>製造オーダーの最後のジョブで部分的な数量を報告するためにジョブ カード デバイスを使用している場合、その注文の以前のジョブのうち、ステータスが "処理中" になっているものがすべて自動的に終了します。

この動作は仕様です。 **製造オーダーの既定値** ページの **完了レポート** タブに、**エンド マーク ルート** という名前のオプションがあります。 このトピックが *はい* に設定されている場合は、作業者がジョブ カード デバイスまたはジョブ カード ターミナルを使用して最後の工程を報告したときに、工順カード仕訳帳が転記されます。 この仕訳帳では、すべての工程が完了としてマークされ、すべての生産ジョブが終了します。 **エンド マーク ルート** オプションが *はい* に設定されている場合、システムは、前回の工程を報告したときに作業者が選択したジョブ ステータスを考慮しません。 また、作業者が数量の全体または一部を報告しているかどうかも考慮されません。

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>在庫決算を実行しようとすると、"期末と一致する日付 %1 では一括引き落とし原価計算の実行が登録されていません" という警告メッセージが表示されます。

リリース 10.0.13 より前のリリースでは、リーン生産原価計算フローを使用していない場合は、在庫決算中に次の誤った警告メッセージが表示されます。

> 日付 %1 で在庫決算を実行しようとしています。 期末と一致する日付 %1 での一括引き落とし原価計算の実行が登録されていません。 期末と一致する日付 %1 での一括引き落とし原価計算を必ず実行してください。 補助元帳および総勘定元帳において、在庫評価、売却済の商品の原価、および差異は、この処理が実行されるまで正しくない可能性があります。

この問題は、リリース 10.0.13 またはそれ以降で修正されています。 詳細については、[KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
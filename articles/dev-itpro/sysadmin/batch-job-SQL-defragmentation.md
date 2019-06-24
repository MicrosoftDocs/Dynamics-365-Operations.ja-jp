---
title: SQL インデックスの最適化を処理するバッチ ジョブ
description: このトピックでは、分割されたインデックスを再構築するために使用するシステム バッチ ジョブを説明します。
author: sericks
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: ganas
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Platform update 22
ms.openlocfilehash: c02a91b9c8d2e5943b2c4945769e86a6abdda0a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570306"
---
# <a name="batch-job-to-handle-sql-index-defragmentation"></a>SQL インデックスの最適化を処理するバッチ ジョブ

[!include[banner](../includes/banner.md)]


プラットフォーム更新プログラム 22 では、断片化したインデックスを再構築する新しいシステム バッチ ジョブが導入されました。 インデックスの断片化により、固有のシナリオでパフォーマンスが著しく低下します。 断片化の問題に対処し、データベースを最高のパフォーマンス状態に維持するため、このバッチ ジョブはスケジュールされた時間に定期的に激しく断片化したインデックスを再構築します。 既定では、そのジョブは毎日現地時間の午前 3:00 に最大 2 時間実行されるようにスケジュールされます。 再構築する必要がある断片化されたインデックスが多くないとバッチ ジョブが判断した場合は早期に完了します。  

このシステム ジョブは変更できません 週 1 回実行する場合は、スケジュールと頻度を変更できます。 システム ジョブは、週 1 回以上実行する必要があります。 

**システム ジョブ パラメーターを調整** ページでパラメータの値を変更し、ジョブを実行できる期間とターゲットとできるインデックスの数を最大値で指定できます。 DTU しきい値は、システムがビジー状態のときにこのジョブが開始するのを防ぎます。 既定の DTU しきい値が 50 の場合、つまりインデックスがジョブの再構築をスケジュールされているときにシステムが 50% 以上の DTU を使用している場合、ジョブはインデックスを再構築しないで早期に終了します。
 
![システム ジョブ調整パラメータ ページのスクリーンショット](media/SystemJobParameters.PNG "システム ジョブ調整パラメータ ページのスクリーンショット")
 
このジョブを実行すると、以下に影響を与える可能性があります。
-   SQL リソースの処理にかかる時間。
- ブロックされる場合があります。

## <a name="change-the-default-scheduled-timerecurrence"></a>スケジュールされた既定の時間/頻度の変更
1. **システム管理 > 照会 > バッチ ジョブ** の順に移動します。
2. *インデックスの再構築*を含むジョブの説明を検索します。   
3. レコードを選択します。  
4. メニュー項目**バッチ ジョブ > 再実行**をクリックします。  
5. スケジュールに合うようにスケジュール時間と頻度を変更します。

インデックス再構築の結果は、**システム管理 > 照会 > データベース > SQLインデックスの断片化の詳細**にあります。 

> [!Note]
> 場合によっては、断片化の前後で番号が同じであるかそれ以上であることがあります。 これは、Microsoft が侵入型オンライン再構築オプションを使用しているため通常です。 今後、オプションのオフライン再構築オプションの導入を計画しています。

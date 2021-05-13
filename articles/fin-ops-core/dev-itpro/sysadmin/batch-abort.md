---
title: 実行中のバッチ ジョブのキャンセル
description: このトピックでは、実行中のバッチ ジョブをキャンセルする方法について説明します。
author: karimelazzouni
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: kaelazzo
ms.search.validFrom: 2019-05-08
ms.dyn365.ops.version: Platform update 27
ms.openlocfilehash: 423f56940db8ee2f27687f44a5d78515c2f7b285
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908680"
---
# <a name="cancel-an-executing-batch-job"></a><a id="legacy-abort"></a>実行中のバッチ ジョブのキャンセル
[!include [banner](../includes/banner.md)]

> [!NOTE] 
> この機能は、Platform update 27 以降で利用できます。

すでに実行中のタスクが完了するのに長い時間がかかる場合、バッチ ジョブのキャンセルに長い時間がかかる場合があります。 このオプションを使用すると、システム管理者やバッチ ジョブ マネージャーは、キャンセル処理中のジョブに対してすでに実行されているタスクをキャンセルできます。 これは他の場所でシステムの使用に影響を与えている長時間実行中のジョブをキャンセルするはるかに高速なメカニズムを提供します。

>[!NOTE]
> この機能は注意して使用する必要があることが重要です。 実行中のプロセスをキャンセルすると、本質的に安全でないアクションのため、データが破損したり孤立したデータまたは不完全なデータが生成される可能性があります。 このアクションは、実行中のタスクによって引き起こされる他の問題を軽減するためにのみ使用するべきです。

実行中のタスクを直ちにキャンセルするには、次の手順を実行します。

1. **システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。
2. **状態** が **キャンセル** のバッチ ジョブを選択します。
3. **バッチ タスク** タブでタスク上の **中止** を選択し、**OK** を選択します。

## <a name="enhanced-cancellation-feature"></a>取消機能の強化
バージョン 10.0.16 から、バッチの取消機能の拡張機能が導入されました。 確認すると、キャンセルしようとするバッチ タスクを現在実行しているバッチ サーバーが再起動します。 これにより、機能は制限に大きな影響を与えるので、キャンセルしようとするジョブのタスクが適用される前の設定が解除されます。

新しい機能を使用するには、次の手順を参照してください。

1. バージョン 10.0.16 以降を実行するか、または必要な品質パッケージをインストールしてください。
2. [機能管理](../../fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースの **バッチ中止の強化** 機能を有効にします。
3. 同じ指示に従い、[実行しているバッチ ジョブをキャンセル](#legacy-abort) を実行します。
 
キャンセル タスクを実行しているバッチ サーバーを再起動するように求めるメッセージが表示されます。 これにより、他のバッチ ジョブの一覧が混乱する可能性があります。 キャンセル タスクを終了するには、次の手順に進む必要があります。

![キャンセル タスクを終了することを確認します。](https://user-images.githubusercontent.com/7556912/112464897-ba820680-8d6c-11eb-871a-e1aff1d82665.png)

サーバーで他の実行中のバッチ ジョブをキャンセルしたくない、実行中のすべてのジョブではなく単一タスクをキャンセルする古い動作を好む場合は、機能管理ワークスペースの **バッチ中止の強化** 機能をオフにし、再度[実行しているバッチ ジョブをキャンセル](#legacy-abort) を行えます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
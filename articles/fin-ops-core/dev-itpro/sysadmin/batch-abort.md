---
title: 実行中のバッチ ジョブの中止
description: このトピックでは、実行中のバッチ ジョブをキャンセルする方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
ms.author: hasaid
ms.search.validFrom: 2019-05-08
ms.dyn365.ops.version: Platform update 27
ms.openlocfilehash: 2852693220ae072566168682eae8eb5b8cd32386
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191801"
---
# <a name="abort-an-executing-batch-job"></a>実行中のバッチ ジョブの中止
[!include [banner](../includes/banner.md)]

> [!NOTE] 
> この機能は、Platform update 27 以降で利用できます。

すでに実行中のタスクが完了するのに長い時間がかかる場合、バッチ ジョブのキャンセルに長い時間がかかる場合があります。 中止オプションを使用すると、システム管理者やバッチ ジョブ マネージャーは、キャンセル処理中のジョブに対してすでに実行されているタスクを中止できます。 これは他の場所でシステムの使用に影響を与えている長時間実行中のジョブをキャンセルするはるかに高速なメカニズムを提供します。

>[!NOTE]
> この機能は注意して使用する必要があることが重要です。 実行中のプロセスをキャンセルすると、本質的に安全でないアクションのため、データが破損したり孤立したデータまたは不完全なデータが生成される可能性があります。 このアクションは、実行中のタスクによって引き起こされる他の問題を軽減するためにのみ使用するべきです。

実行中のタスクを直ちにキャンセルするには、次の手順を実行します。

1. **システム管理** \> **照会** \> **バッチ ジョブ** の順に移動します。
2. **状態** が **キャンセル** のバッチ ジョブを選択します。
3. **バッチ タスク** タブで タスク上の **中止** を選択し、**OK** をクリックします。

    ![バッチ タスクの中止](./media/batch-abort.PNG) 

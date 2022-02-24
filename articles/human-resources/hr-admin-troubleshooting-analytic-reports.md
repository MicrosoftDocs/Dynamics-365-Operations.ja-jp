---
title: トラブルシューティングの分析レポート
description: この記事では、顧客のデータの変更が、顧客のワークスペースに表示されない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419403"
---
# <a name="troubleshoot-analytic-reports"></a>トラブルシューティングの分析レポート

**問題点**

顧客のデータの変更がいずれかの顧客のワークスペースの **分析** タブに表示されません。

**原因**

既定では、Microsoft Power BI レポートは、測定の配置バッチ ジョブのスケジュールに基づいて 4 時間ごとに更新されます。

**解像度**

この問題は、単なるタイミングの問題である場合があります。 この手順に従ってバッチ ジョブを開始し、分析ワークスペースを更新します。

1. **システム管理\>リンク\>バッチ ジョブ\>バッチ ジョブ** で、**バッチ ジョブ** ページを開きます。 または、検索を使用して、**バッチ ジョブ** と入力します。
1. 一覧で **測定の配置** ジョブを検索します。
1. ページの上部で **編集** を選択して、開始予定日/時刻を現在の時刻に近い分析を更新する値に設定します。

![バッチ ジョブ](media/batch-jobs.png)

--- 
title: "明細書を転記するジョブのコンフィギュレーションおよび実行"
description: "この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。"
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f3587fe70dc6a0d8330063db77e625040a53da98
ms.contentlocale: ja-jp
ms.lasthandoff: 02/07/2018

---
# <a name="configure-and-run-a-job-to-post-statements"></a>明細書を転記するジョブのコンフィギュレーションおよび実行

[!include [task guide banner](../includes/task-guide-banner.md)]

この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。 この手順では、デモ データの会社 USRT を使用します。

1. すべてのワークスペース > .. に移動します > 小売店舗の財務。
2. [明細書の転記] をクリックします。
    * 組織階層を選択し、次に組織ノード ツリーで、個々の店舗またはノードを選択します。 店舗グループのバッチ ジョブを作成する場合は、ノードを選択します。  
    * 選択した項目を追加するには、矢印をクリックします。  
3. [バックグラウンドで実行] タブをクリックします。
4. [バッチ処理] チェック ボックスをオンまたはオフにします。
5. [再実行] をクリックします。
6. [開始日] フィールドに日付を入力します。
7. [開始時刻] フィールドに時刻を入力します。
    * 反復処理に関して、特定の実行回数の後終了させる、特定の日付で終了させる、または終了させないの中から選択します。 その後、ジョブの実行頻度を定義するためにさまざまなオプションを選択します。  
8. [OK] をクリックします。
9. [OK] をクリックします。



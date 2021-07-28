---
title: 明細書を転記するジョブの構成および実行
description: この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。
author: josaw1
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 422b1f7f8dc99e1c96da9e266cadcdc09e7aac71
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347469"
---
# <a name="configure-and-run-job-to-post-statements"></a>明細書を転記するジョブの構成および実行

[!include [banner](../includes/banner.md)]

この手順は、選択した店舗または店舗グループの明細書を転記する反復バッチ ジョブを構成し、実行する方法を説明します。 この手順では、デモ データの会社 USRT を使用します。

1. すべてのワークスペース > .. に移動します > 店舗財務。
2. 明細書のバッチ転記をクリックします。
    * 組織階層を選択し、次に組織ノード ツリーで、個々の店舗またはノードを選択します。 店舗グループのバッチ ジョブを作成する場合は、ノードを選択します。  
    * 選択した項目を追加するには、矢印をクリックします。  
3. バックグラウンド タブで実行をクリックします。![バックグラウンドで実行。](../dev-itpro/media/runbackground.png "バックグラウンドで実行") 
4. [バッチ処理] チェック ボックスをオンまたはオフにします。
![バッチ処理。](../dev-itpro/media/batchprocessing.png "バッチ処理 & 再実行") 
5. [再実行] をクリックします。
6. [開始日] フィールドに日付を入力します。
7. [開始時刻] フィールドに時刻を入力します。
    * 反復処理に関して、特定の実行回数の後終了させる、特定の日付で終了させる、または終了させないの中から選択します。 その後、ジョブの実行頻度を定義するためにさまざまなオプションを選択します。  
8. [OK] をクリックします。
9. [OK] をクリックします。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
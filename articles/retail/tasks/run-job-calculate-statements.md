---
title: 明細書を計算するジョブの構成および実行
description: この手順では、選択した店舗または店舗グループの明細書を作成および計算する反復バッチ ジョブを構成し、実行する方法を説明します。
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f52603672e95d0ae4973844851c4ed260484e5f0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "365181"
---
# <a name="configure-and-run-job-to-calculate-statements"></a>明細書を計算するジョブの構成および実行

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、選択した店舗または店舗グループの明細書を作成および計算する反復バッチ ジョブを構成し、実行する方法を説明します。 この手順では、デモ データの会社 USRT を使用します。

1. [すべてのワークスペース] > [小売店舗の財務] に移動します。
2. [明細書の計算] をクリックします。
    * 店舗グループのバッチ ジョブを作成する場合は、特定の店舗またはノードを選択します。  
    * 選択した項目を追加するには、矢印をクリックします。  
3. [バックグラウンドで実行] タブをクリックします。
4. バッチ処理中の場合は、[はい] を選択します。
5. [再実行] をクリックします。
6. [開始日] フィールドに日付を入力します。
7. [開始時刻] フィールドに時刻を入力します。
8. [終了日なし] のオプションを選択します。
9. [PatternUnit] フィールドに「日数」を入力します。
10. [間隔] フィールドに数値を入力します。
11. [OK] をクリックします。
12. [OK] をクリックします。


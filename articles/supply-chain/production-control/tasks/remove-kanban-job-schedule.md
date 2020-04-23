---
title: かんばん作業をスケジュールから削除する
description: この手順では、ジョブ ステータスを未定に戻すことによって、計画済みプロセスかんばんジョブをスケジュールから削除することに焦点をあてます。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0236faa9b534678ed232ac3572c8172c62e5241f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210597"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a>かんばん作業をスケジュールから削除する

[!include [banner](../../includes/banner.md)]

この手順では、ジョブ ステータスを未定に戻すことによって、計画済みプロセスかんばんジョブをスケジュールから削除することに焦点をあてます。 この手順の作成に使用するデモ データの会社は USMF です。 この手順は、作業現場の監督または生産計画担当者を対象としています。


## <a name="find-a-planned-kanban-job"></a>計画済かんばん作業を見つける
1. [生産管理] > [かんばん] > [かんばん作業スケジューリング] の順に移動します。
2. [作業セル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
    * 作業セル 1250 を選択します。  
4. [選択] をクリックします。
5. [ジョブ ステータスの表示] フィールドでは、「スケジュール済み」を選択します。

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a>計画済かんばん作業をスケジュールから削除する
1. 一覧で、目的のレコードを見つけ、選択します。
    * たとえば、2012 年 12 月 19 日付のジョブなど、ステータスが計画済みとなっているジョブを選択します。  
2. アクション ウィンドウで、[計画] をクリックします。
3. [ジョブ ステータスを元に戻す] をクリックします。
4. [OK] をクリックします。
    * これは、現在のジョブ ステータスを「計画済み」から「未定」に戻し、プロセス表から削除します。   


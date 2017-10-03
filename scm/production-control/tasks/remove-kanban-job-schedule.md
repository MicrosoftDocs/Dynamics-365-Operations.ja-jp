--- 
title: "かんばん作業をスケジュールから削除する"
description: "この手順では、ジョブ ステータスを未定に戻すことによって、計画済みプロセスかんばんジョブをスケジュールから削除することに焦点をあてます。"
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b1232fd4039c8021d9a4cd64d8b7c0f66a4f8f9f
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a>かんばん作業をスケジュールから削除する

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



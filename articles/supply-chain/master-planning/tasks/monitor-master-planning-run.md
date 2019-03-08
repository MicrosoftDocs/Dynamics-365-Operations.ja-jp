---
title: マスター プランの実行の監視
description: 生産計画担当者は、マスター プランの実行中であるかどうかを確認します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c2e158d8cbad1f5d4f377f6a8eb43487b34ffdc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "367504"
---
# <a name="monitor-a-master-planning-run"></a>マスター プランの実行の監視

[!include [task guide banner](../../includes/task-guide-banner.md)]

生産計画担当者は、マスター プランの実行中であるかどうかを確認します。 この手順を完了するのにデモ データの会社 USMF を使用します。


## <a name="run-master-planning"></a>マスター プランの実行
1. [マスター プラン] をクリックします。
    * 既定のダッシュボードでこれが見つかります。  
2. [計画] フィールドで値を入力または選択します。
    * 例: StaticPlan  
3. [実行] をクリックします。
4. [処理時間の追跡] フィールドで [はい] を選択します。
    * そのフィールドがすでに選択されている場合、この手順を省略します。  
5. [スレッド数] フィールドに数値を入力します。
6. [対象に含めるレコード] セクションを展開します。
7. [フィルター] をクリックします。
8. 一覧で、選択された行をマークします。
    * フィールド = 品目番号の行をマークします。  
9. [基準] フィールドで、値を入力または選択します。
    * 例: T0001  
10. [OK] をクリックします。
11. [OK] をクリックします。

## <a name="monitor-the-master-planning-run"></a>マスター プランの実行の監視
1. [履歴] をクリックします。
2. [照会] をクリックします。
3. [プロセス タスク期間] をクリックします。
4. 一覧で、目的のレコードを見つけ、選択します。
    * 各品目に対して、各計画ステップを完了するためにかかった期間の概要を取得できます。  


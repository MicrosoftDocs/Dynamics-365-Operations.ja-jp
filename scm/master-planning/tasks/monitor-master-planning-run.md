--- 
title: "マスター プランの実行の監視"
description: "生産計画担当者は、マスター プランの実行中であるかどうかを確認します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 8eb19ac9ded4dc2a091ff733f2f43cb6cafa1b43
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="monitor-a-master-planning-run"></a>マスター プランの実行の監視

[!include[task guide banner](../../includes/task-guide-banner.md)]

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



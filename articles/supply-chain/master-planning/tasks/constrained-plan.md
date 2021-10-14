---
title: 制約付き計画の生成
description: このトピックでは、材料制約と能力制約の両方を考慮した計画の作成方法を説明します。
author: ChristianRytt
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fea315d41d01cb578d7d60c9eb7006e4b6c3362
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578347"
---
# <a name="generate-a-constrained-plan"></a>制約付き計画の生成

[!include [banner](../../includes/banner.md)]

このトピックでは、材料制約と能力制約の両方を考慮した計画の作成方法を説明します。 計画により、材料が利用可能でないうちに生産が開始しないように、またリソースが予約超過にならないようにします。 

この手順の作成に使用するデモ データの会社は USMF です。 この手順は、生産の計画者を対象としています。


## <a name="set-up-a-constrained-plan"></a>制約付き計画の設定
1. ホーム ページで、**マスター プラン** ワークスペースを選択します。
2. ワークスペースの右側にあるリンクの一覧から、**マスター プラン** を選択します。
3. 一覧で、目的のレコードを見つけ、選択します。 例: **StaticPlan**  
4. **有限能力** フィールドで **はい** を選択します。
5. **有限能力タイム フェンス** フィールドに `30` と入力します。
6. **タイム フェンス (日)** セクションを展開します。
7. **能力** フィールドで **はい** を選択します。
8. **能力スケジューリング タイム フェンス (日)** フィールドに、数値を入力します。 例: `60`  
9. **計算済遅延** フィールドで、**はい** を選択します。
10. **遅延の計算タイム フェンス (日)** フィールドに、数値を入力します。 例: `60` 
11. **計算済遅延** セクションを展開します。
12. **計算済遅延を要求日に追加** フィールドで **はい** を選択します。
13. ページを閉じます。

## <a name="create-a-constrained-plan"></a>制約付き計画の作成
1. **実行** を選択します。
2. **マスター プラン** フィールドで、制約を設定した計画を入力または選択します。  
3. **OK** を選択します。
4. **計画オーダー** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
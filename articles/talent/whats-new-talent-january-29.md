---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 1 月 31 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fbbecd4e0f205c2f09ec30548756ff1a43872644
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899108"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a>Dynamics 365 Talent の新機能および変更された機能 (2019 年 1 月 31 日)

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

**ビルド 8.1.2128**

## <a name="core-hr-changes"></a>Core HR の変更

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>休暇人員カード上で実行された休暇には休暇の計画日は考慮されません
暦年に実行されない休暇プランを持っている人たちのために、**取得**カードがプランで定義された休暇年に取得された休暇を表示するようになりました。 たとえば、組織の休暇年が 6 月 1 日から 5 月 30 日で、ある従業員が 12 月に 3 日間休みを取った場合、1 月 15 日の**取得**カードには 3 日間が表示されます。 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>見越計上金額が層日付基準と一致しません
顧客が従業員のどのサービス日付が有効なのかを判断できるようにするために、休暇および欠勤 (**人事管理**パラメーター) に新しいオプションが追加されました。 一部の組織では日付は月末ですが、他の組織では翌月の初めになる場合があります。 たとえば、ある組織が 12 月 31 日に休暇を与え、別の組織は 1 月 1 日に休暇を与える場合があります。 このオプションでは、報酬を発行する時を選択できます。 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>作業者の採用アクションが「ワークフロー完了」の状態で止まっています
いくつかのワークフローが「ワークフロー完了」の状態で終了する問題を修正するための変更が行われました。 ワークフローが終了すると、新しいワークフローは「完了」の状態に移行するようになりました。 ワークフロー完了状態のワークフローはすべてエラー ステータスに移行され、必要に応じて更新または削除が可能になります。 

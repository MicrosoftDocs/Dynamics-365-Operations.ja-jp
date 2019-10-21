---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 2 月 7 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2019
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
ms.search.validFrom: 2019-02-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4005a8745e46a23fe16b94cab7b7aeb20f84035
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009765"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-february-7-2019"></a>Dynamics 365 Talent の新機能および変更された機能 (2019 年 2 月 7 日)

[!include [banner](includes/banner.md)]

このトピックでは、 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="interview-scheduling-enhancements"></a>面接のスケジューリングの拡張
エンド ツー エンドの面接のスケジューリング エクスペリエンスに改良が加えられました。 これで、内部候補者のカレンダーの空き状況を確認したり、スケジュールの推奨事項に内部候補者のカレンダーを使用したりできます。 詳細については、[面接のスケジューリングおよびフィードバック](interview-scheduling-feedback.md) を参照してください。

### <a name="job-posting-to-linkedin--company-mismatch-issue-fixed"></a>LinkedIn へのジョブ求人転記 – 会社が一致しない問題の修正
Attract から LinkedIn に転記されたジョブ求人が間違った会社名で表示される問題が修正されています。 詳細については、[Attract でのジョブの作成、承認、および転記](creating-jobs-attract.md) を参照してください。

### <a name="career-site-url-displayed-in-admin-settings"></a>管理者の設定に表示されるキャリア サイトの URL
**キャリア サイトの管理**の**管理者設定**にキャリア サイトのホーム ページの URL が表示されるようになりました。

## <a name="changes-in-core-hr"></a>Core HR の変更

**ビルド 8.1.2134**

### <a name="multiple-compensation-levels-supported-on-jobs"></a>ジョブでサポートされている複数の報酬レベル
この変更により、1 つのジョブに複数の報酬レベルを定義することが可能になり、同じジョブを使用する場合にプラン間で異なる従業員の固定報酬範囲が可能になります。 

例:    
*ジョブ* - アカウント マネージャー*関連付けられている報酬レベル:* B1 および B2 - 各レベルには、定義された値の範囲があります。 B1 = 最小 50,000、平均 60,000、最大 75,000 および B2 = 最小 65,000、平均 74,000、最大 85,000。 定義された適格性ルールに基づいて従業員に固定報酬を作成するときに、各固定プランは同じジョブとそのジョブの異なるレベルを指すようになりました。 これにより、異なる地域/会社でプランを定義し、これらの違いを説明するためにジョブを重複させることなく、同じジョブで異なる範囲を指すようにすることができます。

### <a name="compensation-level-field-has-been-added-to-the-employee-fixed-compensation-entity"></a>報酬レベル フィールドを従業員の固定報酬エンティティに追加 
この更新により、従業員の固定報酬のエンティティは**報酬レベル**フィールドを含むようになりました。 この追加によって、従業員の固定報酬プランの更新が簡単になりました。 

### <a name="update-job-family-when-updating-and-creating-new-positions"></a>新しい職位を更新および作成するときにジョブのファミリを更新する
職位のジョブを変更すると、**ジョブのファミリ**が選択されているジョブに基づいて既定として設定されるようになりました。

### <a name="performance-improvements-when-rendering-workspaces"></a>ワークスペースをレンダリングするときのパフォーマンスの向上
ワークスペースの分析タブはそれらのページにアクセスしたときにのみ読み込まれるようになりました。 ページの最初のレンダリングの際に、ページの左上隅にインジケーターが表示されます。

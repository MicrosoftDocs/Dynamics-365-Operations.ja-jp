---
title: Dynamics 365 for Talent の新機能および変更された機能 (2019 年 2 月 14 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-02-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5f96dd60652705de820e0661d417dcaee8143561
ms.sourcegitcommit: 5384200c3e33510c5b3ac31f2b22443e1076251f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2019
ms.locfileid: "390670"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-february-14-2019"></a>Dynamics 365 for Talent の新機能および変更された機能 (2019 年 2 月 14 日)

[!include [banner](includes/banner.md)]

このトピックでは、 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
このリリースには、マイナーなバグ修正が含まれています。

## <a name="changes-in-onboarding"></a>オンボードの変更
このリリースには、マイナーなバグ修正が含まれています。
 
## <a name="changes-in-core-hr"></a>Core HR の変更 
**ビルド 8.1.2146**

### <a name="employee-fixed-compensation-entity-doesnt-export-all-records"></a>従業員の固定報酬のエンティティは、すべてのレコードをエクスポートしない
この変更により、**従業員の固定報酬**エンティティですべてのレコードをエクスポートできます。 既存の従業員の固定報酬レコードを作成および更新するためにエンティティを使用することができます。 

### <a name="employment-end-date-doesnt-honor-employee-preferred-time-zone-settings"></a>雇用終了日が従業員の優先タイム ゾーンの設定を遵守しない
会社での雇用を作成または終了するときに、雇用終了日がユーザーの優先タイムゾーンを遵守するようになりました。
 
### <a name="uk-addresses-display-in-analytics-as-eastern-switzerland-addresses"></a>Analytics で英国の住所が東部スイスの住所として表示される
今回のリリースで、**人事管理**「場所別の人数」レポートでの住所の不整合を修正する変更が行われました。
 
### <a name="termination-code-is-not-populated-on-the-worker-position-assignment-record-when-ending-the-position"></a>職位の終了時に、作業者の職位の割り当てレコードに退職コードが設定されない
従業員の職位の割り当ての終了時に、「退職理由」コードを既定として設定する変更が加えられました。

### <a name="new-entity-created-for-job-compensation-levels"></a>ジョブの報酬レベルに対して作成された新しいエンティティ
新しいデータ管理フレームワーク (DMF) エンティティが作成されました。 エンティティは、報酬レベル、市場価値、およびシステムで定義されている各ジョブの調査情報の作成と更新を提供します。

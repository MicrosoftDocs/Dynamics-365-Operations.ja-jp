---
title: Dynamics 365 Talent (2019 年 11 月 19 日) の新機能または変更された機能
description: この記事では、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 11/19/2019
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
ms.search.validFrom: 2019-11-19
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aa984a01e9da30e6da07516fa2986833366a882b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527147"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-19-2019"></a>Dynamics 365 Talent (2019 年 11 月 19 日) の新機能または変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Talent の新機能および変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2621 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="platform-update-31-for-finance-and-operations-apps"></a>Finance and Operations アプリのプラットフォーム更新プログラム 31

詳細については、[Finance and Operations アプリの、プラットフォーム更新プログラム 31 のプレビュー機能 (2020 年 1 月)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31) を参照してください。

### <a name="feature-management-workspace-383856"></a>機能管理ワークスペース (383856)

**機能管理** ワークスペースでは、各リリースで可能になる機能の一覧を表示できます。 既定では、新機能が無効になっています。 ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。 機能管理の詳細については [機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) を参照してください。

すべての新機能は少なくとも 30 日間、通常は 30-60 日間、プレビューのままになります。 主な機能は、通常、プレビュー期間に従って毎年 10 月と 4 月に使用可能です。 **機能管理** ワークスペースに新しい機能が表示されたら、すぐにそれらをオンにすることができます。 一部の機能は既定でオンになっている場合があります。
 
場合によっては、通常は整数機能が有効になりますが、オフにすることはできません (**機能管理** ワークスペースなど)。
 
機能が一般に使用可能になったら、運用環境でオンまたはオフにすることができます。 **機能管理** ワークスペースは、プレビュー機能が必須になるタイミングを示します。 この日付は、通常、半年のリリース計画に沿って 10 月 1 日または 4 月 1 日になっています。 必須機能を無効にすることはできません。 必須になるまでは、すべての環境で機能を有効または無効にすることができます。

### <a name="message-appears-when-canceled-action-exists-for-a-position-382887"></a>職位に対するキャンセル アクションが存在するとメッセージが表示される (382887)

特定の職位を選択して、キャンセル アクションがその職位に対して唯一使用可能だった場合、以下のメッセージは表示されなくなります: **職位 xxxxxx に対して、未完了のアクションが進行中です**。

### <a name="in-learning-analytics-the-course-type-and-status-display-incorrect-data-381151"></a>ラーニング分析で、コース タイプとステータスに間違ったデータが表示される (381151)

今週のリリースにより、ラーニング分析で **コース タイプ** および **ステータス** が正しく表示されるようになりました。

### <a name="personnel-number-should-display-in-the-new-worker-form-banner-383832"></a>個人番号は新しい作業者フォーム バナーに表示されるべき (383832)

クイック リファレンスとして、**新しい作業者** フォームで、**個人番号** がバナーに表示されるようになりました。

### <a name="position-start-date-determines-the-job-record-to-use-when-retrieving-a-compensation-level-during-hire-350361"></a>職位の開始日は、採用中に報酬レベルを取得する場合に使用するジョブ レコードを決定する (350361)

このリリースにより、新しいジョブに割り当てられるレベルが **報酬開始日** によって決まるようになります。

### <a name="custom-pick-list-fields-in-the-position-table-arent-synchronized-to-common-data-service-387503"></a>職位テーブルのカスタム ピッキング リスト フィールドが、Common Data Service に同期されない (387503)

このリリースにより、ピッキング リストの品目が Common Data Service と同期されるようになりました。

### <a name="worker-address-entity-doesnt-synchronize-with-common-data-service-while-importing-new-data-349673"></a>新しいデータのインポート中、作業者の住所エンティティが Common Data Service に同期されない (349673)

今週のリリースにより、新しいデータのインポート中、住所データが Common Data Service に同期されるようになりました。

## <a name="in-preview"></a>プレビュー

### <a name="print-performance-reviews"></a>業績の確認の印刷

詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
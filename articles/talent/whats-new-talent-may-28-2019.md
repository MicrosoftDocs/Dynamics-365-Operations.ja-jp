---
title: Dynamics 365 Talent (2019 年 5 月 28 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 29e941ddab1b2746ccd74d6e335fec7742d1391e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529611"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a>Dynamics 365 Talent (2019 年 5 月 28 日) の新機能および変更された機能

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="coming-soon-in-attract"></a>Attract で間もなく公開

### <a name="job-approvals-on-home-page"></a>ホーム ページのジョブ承認

承認は、ダッシュボードの **承認** セクションに表示されます。 承認者は **自分に割り当て済み** で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、および割り当て日が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済** で自分のジョブを確認できます。ここでは送信したジョブをまだ承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2319 に適用されます。

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート

このリリースでは、次の Common Data Service エンティティでカスタム フィールドがサポートされるようになりました。給付金の計算レートの詳細、作業カレンダーの休日行、および雇用です。

### <a name="copy-position-now-includes-payroll-details"></a>職位のコピーに給与詳細が含まれるようにする
**職位のコピー** を使用してすべてのオプションを選択すると、給与の詳細情報がコピー情報に含まれるようになります。 

## <a name="in-preview-in-core-hr"></a>Core HR のプレビュー

### <a name="restrict-the-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまな種類の休暇を従業員に提供できます。 いくつかの休暇タイプは、従業員が休暇を送信するのに適していない可能性があり、その代わりに人事管理 (HR) によって管理されます。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

### <a name="new-page-to-validate-position-hierarchy-data"></a>職位階層データを検証する新しいページ

HR および管理者は、誤ってインポートされた循環参照に対して、管理階層を検証できます。 この新しいページは、**組織管理 > リンク > 職位 > 職位階層の検証** からアクセスできます。

### <a name="specify-reason-codes-on-leave-types"></a>休暇タイプの理由コードの指定

組織は、休暇申請に関する追加情報を要求する場合があります。 休暇タイプに理由コードを指定し、従業員は休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休暇申請で固有の休暇タイプについては理由コードが必要

従業員が休暇申請を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 この要件は、会社のポリシーや規制要件が原因であることがあります。 どの休暇タイプに理由コードが必要かを指定できます。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します

従業員の休暇を追跡し、どのように計算するかを理解する機能は、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇を付与することにも役立ちます。 HR において、トランザクション (交付、見越、調整、および要求) の表示が新しくなり、HR スタッフは休暇残高の背後にある理由を確認することができるようになりました。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
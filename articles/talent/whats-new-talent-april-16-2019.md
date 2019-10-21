---
title: Dynamics 365 Talent (2019 年 4 月 16 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0781a479ebf37334d8eba18ea6d69d7cfb9db9ea
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024140"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Dynamics 365 Talent (2019 年 4 月 16 日) の新機能および変更された機能

[!include [banner](includes/banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="process-auditing"></a>プロセスの監査

求人、職務申請、およびジョブ アプリケーションに加えられた変更を追跡できるようになりました。 詳細については、[採用データの変更の追跡](process-auditing.md) を参照してください。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2239 に適用されます。 かっこ内の数字は、Lifecycle Services (LCS) のサポート番号を参照しています。

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Common Data Service の報酬地域、報酬レベル、福利厚生オプションおよびスキル タイプのエンティティは、顧客フィールドのサポートを含むように更新されました。

このリリースでは、これらの Common Data Service のエンティティが、Talent: Core HR によって追加されたカスタム フィールドを含める機能を持つように更新されました。

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a>新しい Common Data Service エンティティは、報酬給付ルール、変動報酬プラン、変動報酬に対してサポートされます。

このリリースでは、報酬給付ルール、変動報酬プラン、および変動報酬エンティティが Common Data Service に追加されました。 これらのエンティティは、Talent: Core HR によって追加されたカスタム フィールドもサポートします。

### <a name="powerbi-refresh-issues-314342"></a>PowerBI の更新に関する問題 (314342)

この変更により、PowerBI レポートが正常に更新されるよう問題が修正されます。

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>従業員セルフサービスの移行タスクにおいて直接クリックできない (303309)

この変更により、従業員ロールを持つユーザーは、Talent のタスク リストから移行タスクを選択および更新できるようになります。

### <a name="performance-feedback-email-message-updated-309615"></a>パフォーマンス フィードバックのメール メッセージが更新されました (309615)

この変更により、フィードバックが正常に送信された時に確認メッセージが表示されるようになりました。

### <a name="missing-tables-in-word-template-308048"></a>Word テンプレート内の見つからないテーブル (308048)

この変更により、従業員およびスキル情報を含む Word テンプレートを作成する時、選択された従業員のスキルのみが Word ドキュメントに表示されます。

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>除籍チェックリストの適用時にエラーが表示されます。 (299877)

この変更により、作業者フォームから除籍チェックリストを直接適用した場合の問題が修正されます。

## <a name="in-preview"></a>プレビュー

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>理由コードを休暇タイプに指定できるようにする

組織は、休暇申請に関する追加情報が必要な場合があります。 休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>休暇申請で特定の休暇タイプに理由コードが必要

従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 これは、会社の方針または規制要件が原因である可能性があります。 どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します。

従業員の休暇を追跡し、どのように計算するかを理解することにより、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇の付与ができるようになります。 HR は、残高の背後にある理由を確認するための、トランザクション (交付、見越、調整、および要求) の表示が新しくなりました。

## <a name="coming-soon"></a>間もなく公開

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>重複する従業員チェックのためのユーザー インターフェイスの改良

この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するために、重複フォームは自動的に開きません。

### <a name="email-support-for-alerts"></a>アラートの電子メールサポート

Finance and Operations のプラットフォーム更新プログラム 25 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。



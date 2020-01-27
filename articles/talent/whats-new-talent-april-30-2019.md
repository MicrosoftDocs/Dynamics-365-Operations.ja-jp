---
title: Dynamics 365 Talent (2019 年 4 月 30 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/30/2019
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
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 38c30a878ada9ed0b63ade3d0f234aeffce0ad12
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897891"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-30-2019"></a>Dynamics 365 Talent (2019 年 4 月 30 日) の新機能および変更された機能

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2270 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="provide-feedback"></a>フィードバックの送信

フィードバックを提供するためのオプションは、Talent 内の**ヘルプ** メニュー (**?**) にあります。 このメニューから次のリソースにアクセスできます。

- フィードバック
- ヘルプ
- はじめに
- サポート
- アイデア
- バージョン情報

### <a name="improvements-to-the-user-interface-for-duplicate-employee-detection"></a>重複する従業員検出のためのユーザー インターフェイスの改良

この変更により、名前フィールドの設定時に重複が検出され、検出された重複の数がステータス インジケーターに表示されます。 提供されるリンクから、重複のうちいずれかを使用する必要があるかどうかを評価するためのページが表示されます。 データ入力の中断を回避するために、重複ページは自動的には開かれません。 ページを開くには、リンクを選択する必要があります。

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート

今週のリリースでは、次のエンティティでカスタム フィールドがサポートされるようになりました。雇用、福利厚生タイプ、および支払サイクルです。

### <a name="an-error-occurs-when-an-off-boarding-checklist-is-assigned-299877"></a>オフボードのチェックリストが割り当てられた場合、エラーが発生する (299877)

この変更により、退職プロセスにない従業員にオフボード チェックリストを割り当てる時に表示されるエラー メッセージが修正されます。

### <a name="the-exited-workers-link-opens-the-wrong-worker-309939"></a>退職した作業者のリンクで間違った作業者が開かれる (309939)

この変更により、別の法人から従業員を再雇用し、退職した作業者のリストからその従業員に移動しようとする場合に発生する問題が修正されます。

### <a name="the-employee-self-service-compensation-card-doesnt-show-summary-values-when-advanced-security-is-turned-on-315231"></a>高度なセキュリティがオンになっている場合、従業員セルフサービスの報酬カードに集計値が表示されない (315231)

この変更により、高度な報酬セキュリティを使用した場合に発生する問題が修正されます。 高度なセキュリティがオンになっている場合、従業員セルフサービスに従業員と管理者の両方の集計した報酬額が表示されるようになりました。 この変更の前は、集計値は 0 (ゼロ) として表示されていました。

### <a name="if-a-position-without-a-title-is-created-in-common-data-service-no-position-is-created-in-talent-314562"></a>Common Data Service においてタイトルのない職位が作成された場合、Talent に職位が作成されない (314562)

今週の変更により、Common Data Service で職位を作成しても、タイトルを入力しなかった場合に発生する問題が修正されます。

### <a name="error-message-in-performance-journal-entries-in-employee-self-service-314134"></a>従業員セルフサービスの業績仕訳帳入力でのエラー メッセージ (314134)

この変更により、従業員セルフサービスの業績仕訳帳入力に業績目標を関連付けた時に発生する問題が修正されます。

## <a name="in-preview"></a>プレビュー

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>理由コードを休暇タイプに指定できるようにする

組織は、休暇申請に関する追加情報を要求する場合があります。 休暇タイプに理由コードを指定し、従業員は休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休暇申請で固有の休暇タイプについては理由コードが必要

従業員が休暇申請を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 この要件は、会社のポリシーや規制要件が原因であることがあります。 どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します

従業員の休暇を追跡し、どのように計算するかを理解する機能は、人事管理 (HR) が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇を保証することにも役立ちます。 HR において、トランザクション (交付、見越、調整、および要求) の表示が新しくなり、HR スタッフは残高の背後にある理由を確認することができるようになりました。

## <a name="coming-soon"></a>間もなく公開

### <a name="email-support-for-alerts"></a>アラートの電子メールサポート

Finance and Operations のプラットフォーム更新プログラム 26 では、あるイベントによって通知がトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。

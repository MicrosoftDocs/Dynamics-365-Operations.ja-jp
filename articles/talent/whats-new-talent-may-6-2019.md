---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 5 月 6 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c04af27bcc446b516f14125e71fb707bfd1d7708
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529711"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-6-2019"></a>Dynamics 365 Talent の新機能および変更された機能 (2019 年 5 月 6 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更

### <a name="select-optional-documents-upon-offer-creation"></a>オファー時のオプション ドキュメントの選択

オファー パッケージ テンプレートを選択する時、Attract はそのパッケージ テンプレートから適用可能なオプション ドキュメントを選択するよう促すようになりました。 オファーの準備中、その他のオプション ドキュメントを追加できます。

## <a name="changes-in-onboard"></a>Onboard の変更

今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更

このセクションに記載された変更は、ビルド番号 8.1.2282 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

### <a name="platform-update-26-for-finance-and-operations"></a>Finance and Operations のプラットフォーム更新プログラム 26

Finance and Operations のプラットフォーム更新プログラム 26 に関する追加情報については、[Dynamics 365 Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26)を参照してください。 

### <a name="common-data-service-entity-support-for-custom-fields"></a>カスタム フィールドに対する Common Data Service エンティティのサポート

今週のリリースでは、次のエンティティでカスタム フィールドがサポートされるようになりました。給付金計算頻度、給付金の計算レート、福利厚生タイプ、作業カレンダー、作業カレンダーの休日、支払サイクル、および作業者 ID タイプです。

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>一括登録から離脱し、層基準を「勤続日数」に変更しても、初期見越計上レートは更新されない (318526)

従業員を一括登録し、層基準を変更すると、初期見越計上は選択した層基準を反映するようになりました。

### <a name="workflow-showing-duplicate-place-holders-313636"></a>重複するプレース ホルダーを示すワークフロー (313636)

このリリースでの変更により、ワークフロー通知の送信時にプレース ホルダーが重複することはなくなりました。

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>「Excel で開く」の使用時に分析コード フィールドが更新されない (176261)

このリリースにより、**作業者** のページから **Excelで開く** を使用して財務分析コードを更新できるようになりました。 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Common Data Service で作成された作業者の住所が Talent に同期されない (317555)

この変更により、Common Data Service で作成された住所が Talent: Core HR で更新されるようになります。


## <a name="in-preview"></a>プレビュー

### <a name="new-page-to-validate-position-hierarchy-data"></a>職位階層データを検証する新しいページ

人事管理 (HR) および 管理者は、誤ってインポートされた循環参照に対して、管理階層を検証できるようになりました。 この新しいページは、**組織管理 > リンク > 職位 > 職位階層の検証** からアクセスできます。

### <a name="specify-reason-codes-on-leave-types"></a>休暇タイプの理由コードの指定

組織は、休暇申請に関する追加情報を要求する場合があります。 休暇タイプに理由コードを指定し、従業員は休暇申請で理由コードを選択できるようになりました。

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>休暇申請で固有の休暇タイプについては理由コードが必要

従業員が休暇申請を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。 この要件は、会社のポリシーや規制要件が原因であることがあります。 どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>HR の休暇および欠勤トランザクション リストを提供します

従業員の休暇を追跡し、どのように計算するかを理解する機能は、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇を付与することにも役立ちます。 HR において、トランザクション (交付、見越、調整、および要求) の表示が新しくなり、HR スタッフは残高の背後にある理由を確認することができるようになりました。

## <a name="coming-soon"></a>間もなく公開

### <a name="indicate-instance-type-when-provisioning-talent"></a>Talent のプロビジョニング時に、インスタンス タイプを示す

Talent の新しいインスタンスのプロビジョニング時に、インスタンス タイプが **実稼働** か **サンドボックス** であるかを示すことができ、新しい機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、実稼働インスタンス タイプに更新されます。 既存のインスタンスのいずれかをサンドボックス インスタンス タイプに更新する場合は、変更要求を開始するようサポートに連絡してください。

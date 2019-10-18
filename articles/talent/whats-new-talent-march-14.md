---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 14 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
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
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c3beef9ef4e73eaf76f861735bb154fa630703f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023910"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-14-2019"></a>Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 14 日)

[!include [banner](includes/banner.md)]

このトピックでは、 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
このリリースには、マイナーなバグ修正が含まれています。

## <a name="changes-in-onboarding"></a>オンボードの変更
このリリースには、マイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
**ビルド 8.1.2186**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>重複するセキュリティ ロールを使用している場合、パフォーマンス管理はすべてのシナリオで機能しません
今回のリリースで行われた変更により、標準または重複ロールを使用するときに、パフォーマンス管理のシナリオが有効になりました。

### <a name="mass-assign-checklists-to-workers"></a>作業員へのチェックリストを一括割り当てしてください。
この変更により、複数の従業員を選択し、それらの従業員に複数のチェックリストを一括割り当てできるようになりました。 

### <a name="platform-update-24-for-finance-and-operations"></a>Finance and Operations のプラットフォーム更新プログラム 24
Finance and Operations のプラットフォーム更新プログラム 24 の詳細については、[Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24) を参照してください。 プラットフォーム 24 の大幅な変更は次のとおりです。 

- 人材では、警告が有効になります。
- Office ヘッダーに対応するようになった更新済みのナビゲーション バー。

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>職場の場所を更新すると、コンテキストが作業者リストの先頭に切り替わります
現在のリリースでは、職場の場所を変更しても、職場の場所の割り当て時に表示されている作業員のコンテキストが切り替わらなくなりました。

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>職位の割り当ての終了日が、作業者の採用および移動の際に正しく表示されません
アクションを使用するときに、職位割り当ての終了日がユーザーの優先タイム ゾーンに基づいて正しく表示されるようになりました。

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service 職務のエンティティは職務タイプと職務権限フィールドの更新を許可しません。
Common Data Service エンティティは、Common Data Service を使用して更新する際、正しく同期するようになりました。

## <a name="coming-soon"></a>間もなく公開

###  <a name="advanced-compensation-security-fixed-and-variable"></a>高度な報酬セキュリティ (固定および変動)
多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。 これらは、経営幹部または地域の従業員向けのものである可能性があります。 この変更により、HR は組織内のさまざまな従業員グループの報酬プランを管理および維持できます。 固定および変動プランにはセキュリティ ロールを割り当てることができます。これは、プランへのアクセス権とプランに関連する従業員データ (給与または特別償却レコードなど) を決定します。 アクセス権を持つロールのみが、それらの従業員の報酬を処理できます。

###  <a name="email-support-for-alerts"></a>アラートの電子メールサポート
Finance and Operations のプラットフォーム更新プログラム 24 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。

### <a name="duplicate-employee-check-interface-changes"></a>重複する従業員チェック: インターフェイスの変更
この変更により、名前のフィールドを入力すると重複が検出され、見つかった数がステータスに表示されるようになります。 提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。 データ入力の中断を回避するため、重複フォームは自動的に開きません。

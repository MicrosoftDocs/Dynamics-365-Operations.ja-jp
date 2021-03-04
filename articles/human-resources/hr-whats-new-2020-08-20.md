---
title: Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 8 月 20 日)
description: このトピックでは、2020 年 8 月 20 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 8/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46dadb8834195c5dd06cd1c56d79324def7d9f2d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527484"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 8 月 20 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3478 に適用されます。 一部のヘッダーにあるかっこ内の数字は、参照用に Lifecycle Services (LCS) のサポート番号を参照しています。

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>休暇の予定と保留中の休暇情報を、プープル ワークスペースのカードに表示する

**ピープル** ワークスペースの休暇カードと欠勤カードで、休暇の予定と保留中の休暇申請オプションが使用できるようになりました。

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>従業員セルフサービスの従業員ロールの場合、プライベート フィールドは既定で [はい] になっていません (477106)

従業員が従業員セルフサービスの **個人情報** ページを使用して新しい住所レコードを追加すると、**プライベート フィールド** の既定値が **はい** になります。 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>従業員管理の採用候補クイックタブで、表示される候補の数が誤って表示される (470110)

**人事管理** ページで、採用候補者の数を正確に表示するようになりました。 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>見越計上がゼロに設定されていると、退職した従業員の病欠を入力できない (446195)

休暇トランザクションは、将来的に退職する従業員に対しても認められるようになりましたが、見越計上はゼロに設定されます。 休暇トランザクションは、従業員の退職日まで入力可能です。 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>新しい作業者のフォームにカスタム フィールドを追加すると、休暇管理のアクション ペインのフィールドが無効になる (473314)

新しい **作業者** フォームにカスタム フィールドが追加されている場合は、**休暇管理** の新規 **作業者** フォーム上のアクション ペインのオプションは無効化されます。

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>休暇のコメント フィールドを必須にしても、コメントが未入力のままで休暇申請ができてしまう (473543)

コメント フィールドは必須になり、休暇の申請時にはこの設定に従うようになりました。 必須フィールドはプレビュー機能です。

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF エンティティで休暇付与の一時停止が可能

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="in-preview"></a>プレビュー

### <a name="mandatory-fields"></a>必須項目

人事管理のパーソナル化機能を使用することにより、フィールドを必須にすることができます。 この機能には **保存されたビュー** が必要です。 保存されたビューに関する詳細については、次を参照してください。

- [保存ビュー - Dynamics 365 2020 リリース ウェーブ 2 プランの一般提供](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) 
- [保存されたビューを十分に活用するフォームの作成](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、以下を参照してください。

- Dynamics 365 2020 リリース ウェーブ 1 プランでの [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams)
- [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a>間もなく公開

### <a name="human-resources-app-in-teams-preview-features"></a>Teams の Human Resources アプリにおけるプレビュー機能
 
-  **通知** : 休暇申請の提出者と承認者は、Teams の人事アプリで通知されます。 承認者は休暇申請を承認、または拒否することができ、申請が承認または拒否された場合は送信者に通知されます。
 
- **マネージャーの休暇カレンダー** : マネージャーは、直属の部下の承認済み休暇、および保留中の休暇をカレンダーで確認することができます。 このビューを使用すると、チームのメンバーの休暇を簡単に把握することができます。

### <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Common Data Service ですぐに使用可能になります。

## <a name="known-issues"></a>既知の問題

**機能管理** ワークスペースには、通常使用可能な場合にプレビュー機能として無効になっている機能が表示される場合があります。 正しくないステータスを示す一般的な機能を以下に示します。 

- 給付金管理
- ケース管理
- データベースのログ記録 (監査)
- 1 つの会社または 1 つの計画の休暇の見越計上
- 休暇の見越計上の中断
- 残高調整の理由コードとコメント
- 休暇の売買
- 休暇および欠勤カレンダー
- 休暇繰越ルール
- 休暇の見越計上の監査
- 休暇の見越計上の削除
- 休暇の見越計上の丸め
- 1 つの休暇計画で複数の休暇タイプを構成
- 短期休暇の更新
- 見越計上に従業員の FTE を使用する
- 会社間報酬ビュー
- 業績の確認の印刷
- 休暇の見越計上における休日の修正

### <a name="benefit-plan-employee-entity"></a>福利厚生プランの従業員エンティティ 

**BenefitsPlanEmployee** エンティティに関する2つの問題が発見されました。 作業者の登録をインポートする際に、**補充コード** と **計画タイプ コード** が正しく設定されません。 この問題が発生すると、従業員の福利厚生プランが **作業者の福利厚生プラン** フォームと、従業員セルフサービスの **オープン登録** フォームに正しく表示されません。 この問題は、従業員セルフ サービスでプランを選択する機能にも影響します。 現時点では回避策はありません。 この問題については優先度を挙げて取り組み、次のリリースで修正を展開していきます。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
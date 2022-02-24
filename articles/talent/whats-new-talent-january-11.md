---
title: Dynamics 365 Talent - Core HR (2019 年 1 月 11 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent - Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 01/11/2019
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
ms.search.validFrom: 2019-01-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d49a4aca368e3de10ae37b56c6d286d78f7f369a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461776"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-january-11-2019"></a>Dynamics 365 Talent - Core HR (2019 年 1 月 11 日) の新機能および変更された機能

**ビルド 8.1.2100**

このトピックでは、Core HR の新機能または変更された機能について説明します。

## <a name="changes"></a>変更

### <a name="validate-leave-requests-by-forecasting-available-balance"></a>利用可能な残高を予測して休暇要求を検証
今回のリリースで行われた変更では、従業員が現在の残高から差し引くことがなく、将来の休暇期間を依頼できるようにします。 将来行われる要求に標準のワークフローが使用されます。 詳細については、[作業時間に基づいて休暇を見越計上する](leave-accrue-hours-worked.md) をお読みください。

### <a name="view-forecasted-leave-balance-in-ess-and-people"></a>ESS および人員で予測休暇残高を表示
このフィーチャーにより、HR、管理者、および従業員による将来の休暇期間の残高の表示が可能になります。 従業員は、**従業員セルフ サービス** ワークスペースで将来の残高を確認でき、HR は **人員** ワークスペースを使用して同じ情報にアクセスできます。

### <a name="notifications-for-changing-leave-balances"></a>休暇の残高を変更するための通知
休暇の残高は、従業員の現在の残高を表示します。 将来の残高は、**従業員セルフ サービス** および **人員** ワークスペースで「現在の日付」を入力して予測残高を計算することで利用できます。

次のエリアの予測残高を表示するためのナビゲーションが追加されました。
  - **従業員セルフ サービス** ワークスペース上の **休暇** カード。
  - **マネージャー セルフ サービス** ワークスペース上の **休暇および欠勤** カード。
  - **人員** ワークスペース上の **休暇および欠勤** ページ。

### <a name="allow-decimals-for-variable-compensation-plans-cash-plans"></a>変動報酬プラン (現金プラン) の小数点以下の許可
変動現金報酬および計画は、金額に対する柔軟性が追加され、小数点以下の値が上書きされるようになりました。

### <a name="unable-to-change-the-dates-on-variable-comp-enrollments-after-the-plan-is-saved"></a>プラン保存後の変動報酬登録の日付変更の不可
この変更により、計画の保存後に計画終了日を更新 (延長または期限切れ) することができます。 開始日と終了日に関係なく、プランを有効化または無効化することはできます。

### <a name="payroll-information-available-when-assigned-the-payroll-admin-security-role"></a>給与管理者セキュリティロールを割り当てられたときに利用可能な給与情報
要求プロセス中に給与管理者のロールが給与情報にアクセスできるように更新されました。

### <a name="employee-self-service--position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>従業員セルフ サービス | タイルからの職位階層のドリルダウンで親ノードを取得できません
職位階層を新しいワークスペースに追加して組織構造内を移動するときに発生するエラーを解消するための変更が行われました。

### <a name="new-validation-message-when-personnel-number-sequence-is-in-use"></a>個人番号順序が使用されているときの新しい検証メッセージ
従業員を採用し、次の従業員番号が使用されているときの問題を明確にするために変更が加えられました。

### <a name="employee-self-service-workspace-selected-as-the-initial-startup-page"></a>初期起動ページとして選択された従業員セルフ サービス ワークスペース
**従業員セルフ サービス** ワークスペースがユーザーの初期起動ページとして選択されており、そのユーザーに従業員ロールが割り当てられていない場合、システムは既定のダッシュボードにリダイレクトされます。

### <a name="termination-reason-code-updates-position-assignment-record"></a>退職理由コードが職位の割り当てレコードを更新
退職の理由コードは、従業員の退職および職位の終了に際して職位の割り当てを更新するようになりました。 

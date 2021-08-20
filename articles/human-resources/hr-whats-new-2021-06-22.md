---
title: Dynamics 365 Human Resources (2021 年 6 月 22 日) の新機能または変更された機能
description: このトピックでは、2021 年 6 月 22 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 897c25df96017c5be1ae789027d178ca6b3ccc0410b4f65c7d2557b39e840134
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735354"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Dynamics 365 Human Resources (2021 年 6 月 22 日) の新機能または変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4258 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 雇用されていない作業者についてユーザーに通知する機能 - 詳細なアクセスが有効で、機能管理で **雇用されていない作業者すべての表示** 機能が無効になっている場合、雇用されていない作業者フォームにバナーが表示されます。 バナーは、ユーザーに **雇用されていない作業者すべての表示** 機能をオンにするよう指示します。 | 適用できません| [雇用されていない作業者](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| 給付金管理適格性ルールに対するカスタム フィールドのサポート | [適格性処理のカスタム フィールド サポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[適格性ルールの構成](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| 休暇見越計上のトランザクション監査 | 適用できません | [休暇見越計上のトランザクション監査](hr-leave-and-absence-accrue.md)|
| 休暇ワークフロー エクスペリエンスの強化 | [休暇ワークフロー エクスペリエンスの強化](https://go.microsoft.com/fwlink/?linkid=2147528) | [休暇申請](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 問題 |  説明 |
| --- | --- | --- |
| 583052 | フィードバックを受け取るユーザーは、受け取ったフィードバックを編集することができる | 業績仕訳に対するフィードバックを受け取った従業員が **外部リンクの追加** を選択すると、フォームが編集可能になり、従業員は受け取ったパフォーマンス フィードバックを編集できるようになります。 |
| 522281 | 報酬管理の報酬構造タイルで従業員数を選択すると、不正確な結果になる| 報酬ワークスペースから報酬プランにドリルダウンすると、正しい従業員数が表示されるようになりました。 |
| 580683 | 従業員とマネージャーのロールに割り当てられたユーザーが、メモの添付や、業績仕訳の更新ができない | 従業員とマネージャーのロールに割り当てられたユーザーは、メモの添付や、業績仕訳の更新を行うことはできません。 ユーザーに次のエラーが表示されます。「業績仕訳帳入力でレコードを作成できません (HcmPerfJournal)。 セキュリティ ポリシーのアクセスが拒否されました。」 |
| 583077 | 休暇および欠勤に関する会社のカレンダーに、従業員の誤った生年月日が表示される | ユーザーは、休暇および欠勤に関する会社のカレンダーで従業員の正しい生年月日を確認できるようになります。 |
| 586996 | 1 つの会社にアクセスが制限されている場合、会社全体で休暇を表示する機能により、残高が空になる | 会社全体で休暇を表示する機能が有効な場合、ユーザーは従業員の将来の休暇残高を正しく表示できます。 |
| 581014 | 会社間の休暇ビューおよび欠勤ビューを有効にすると、将来の残高を表示するときにエラーが発生する | 会社全体で休暇を表示する機能が有効な場合に将来の休暇残高がユーザーに表示されるエラーは修正されました。 |
| 509404 | 部門人数分析が、部門間の従業員の異動を考慮しません。 | 従業員がある部門から別の部門に移行したとき、現在の年度内に職位の詳細が期限切れになる場合、部門人数分析のデータは、従業員が切り替えられる古い部門を反映しません。 |
| 584851 | 給付金貸方の比例配分ルールを「なし」にすることにより、貸方を提供しない |フレックス貸方の比例配分ルールを「なし」にすることにより、従業員はいつ採用されたかにかかわらず、従業員の受給期間の貸方がゼロになります。 これは修正され、、従業員が給付金期間が始まる前に採用されている場合、完全なフレックス クレジットを受け取ることができるようになりましたが、給付金機関が始まった後に採用された場合はそうではありません。 |
| 584897 | 「基本外部機能を使用」職務権限を複製するとエラーが発生する | 「基本外部機能を使用」職務権限を複製しようとすると、ユーザーには「UserDefinedAppHostDialogView という識別子を持つオブジェクトが見つかりません」というエラーが表示されます。 |
| 575692 | 保留中の作業者が休暇および欠勤の見越計上を使用できない | **合理化された従業員の入力** が有効な場合、休暇および欠勤の見越計上は将来の採用で実行されます。 |
| 580110 | 給与統合に会社を追加すると、オプションがプロジェクトを更新しないに設定されている場合でも、すべてのエンティティを使用できるように統合がリセットされる | 顧客がエンティティを削除した場合、または給与統合のデータ プロジェクトを変更し、プロジェクトの自動更新を回避するオプションを設定している場合、統合に新しい会社を追加すると、設定は無視され、プロジェクトが更新されます。  |
| 584518 |パフォーマンスの問題を処理する福利厚生の登録 | このバグは、レガシーの福利厚生登録プロセスのパフォーマンスの問題に対処しました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| プラットフォーム 更新プログラム 10.0.19 (43) | プラットフォーム更新プログラム10.0.19 は、2021 年 6 月 28 日のサービス リリースで、展開を開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.19 のプラットフォーム更新プログラム (2021 年 6 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19) を参照してください。 |
|  勤続年数表示の切り替え | この機能は、異なる日付を使用して、**合理化された従業員の入力** フォームと **ユーザー** フォームに表示される金属年数を計算するオプションを提供します。  これは、Human Resources パラメーターで使用可能になります。 |
|  休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  特定の休暇タイプに対して添付ファイルを必須にする | この機能を管理者が使用すると、特定の休暇タイプで休暇申請を送信する際に、添付ファイルの追加を必須に設定できます。 |
|  休暇タイプごとに休暇単位を構成する | この機能により、管理者は各休暇タイプの休暇単位 (時間または日) を構成することができます。  |
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

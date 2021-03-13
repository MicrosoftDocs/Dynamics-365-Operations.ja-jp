---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 5 月 28 日)
description: このトピックでは、2020 年 5 月 28 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 05/28/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 662b34994231727b0d693cac148547b404475346
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127828"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 5 月 28 日)

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3287 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>休暇プラン (447498) ごとに複数のタイプを有効にすると、LeaveRequest エンティティは機能しません

この変更により、**LeaveEnrollmentV2Entity** で複数の休暇タイプを有効にしたときに発生するエラーを修正できるようになりました。

## <a name="batch-contention-reduction-feature-preview-446619"></a>バッチの競合軽減機能 (プレビュー) (446619)

この機能を有効にすると、タスクの選択とジョブの完了時のバッチ フレームワーク テーブルでブロックの減少が期待できます。

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict で作業者の保存中に、People でレコードの編集ができない (427915)

この変更により、新しい作業者を追加したり、住所情報を更新したり、言語設定を変更したりするときのエラーが修正されます。 この固有のシナリオでは、レコードを更新できなかったことを示すエラーが表示されます。 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>承認済の休暇申請に添付ファイルを追加して再提出できない (425407)

この変更により、承認済の休暇申請への添付ファイルが可能になりました。

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>ユーザーは別の法人のフォームで従業員の報酬を入力できる (409529)

この変更により、誤った法人の報酬レコードが誤って入力されないように報酬オプションが無効になります。

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>従業員を異動する際に、作業者の職位の割り当て日が職位の期間よりも前である場合のエラー (429402)

このシナリオで従業員を異動する際のエラー メッセージは、この問題を修正するために必要な変更をより的確に説明するために更新されています。

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>従業員セルフサービス福利厚生の添付ファイル機能
 
これで、従業員が登録している各プランの福利厚生登録プロセス中に、添付ファイルを追加できます。 **作業者登録福利厚生** フォーム内で添付ファイルを表示できます。

## <a name="in-preview"></a>プレビュー

## <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。 

## <a name="leave-suspension"></a>休暇の停止

従業員に対し Human Resources で休暇および欠勤を中断できます。 休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。 一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。 詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>ユーザー エクスペリエンスを更新し、見越計上の中断が表示されるようになりました (429550)

ユーザー エクスペリエンスは、計画に対して見越計上が中断されたことを示します。

## <a name="coming-soon"></a>間もなく公開

## <a name="database-logging-in-preview-in-june"></a>データベース ログ (6 月のプレビュー)

データベース ログ機能を使用すると、監視するテーブルとフィールドを決定できます。 また、Change Tracking を起動するイベントを決定することもできます。 時間の経過に伴う変更を確認するために、照会機能を使用できます。

## <a name="buy-and-sell-leave-in-preview-june-1"></a>休暇の売買 (6 月 1 日のプレビュー)

一部の組織では、従業員が休暇を購入または売却できるという利点があります。 このプロセスは、多くの場合、手動で管理します。 この機能により、人事部門のポリシーと申請をより自動化された方法で管理できるようになり、休暇管理プロセスを合理化しながらミスを排除するのに役立ちます。 詳細については、以下を参照してください。

- [休暇の売買ポリシーの管理](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [休暇の売買](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ
 
福利厚生管理エンティティはリリースされてます。 DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単にコンフィギュレーションできます。 福利厚生管理テンプレートは、データの移動にも使用できます。 テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>休暇付与の一時停止に理由コードが追加されました (6 月 1 日)

見越計上の中断に理由コードが追加されました。

## <a name="carry-forward-rules-june-1"></a>繰越ルール (6 月 1 日)

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>指定した休暇タイプに対する休暇付与の一時停止 (6 月 1 日)

今回のリリースでは、人事部は無給休暇の休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。 無給休暇のタイプを指定できますが、必須ではあります。 他の休暇種類に基づいて、任意の休暇を停止することができます。

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF エンティティで休暇付与の一時停止が可能 (6 月 1 日)

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)
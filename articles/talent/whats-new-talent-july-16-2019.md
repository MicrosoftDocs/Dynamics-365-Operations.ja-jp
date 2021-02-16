---
title: Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 16 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 07/16/2019
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
ms.search.validFrom: 2019-07-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: cd7f288e5c1015f4266db527adfcd62a5dbbc95f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528102"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-16-2019"></a>Dynamics 365 Talent の新機能または変更された機能 (2019 年 7 月 16 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。

## <a name="changes-in-attract"></a>Attract の変更
今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。

### <a name="coming-soon-in-attract"></a>Attract で間もなく公開
#### <a name="job-approvals-appear-on-the-home-page"></a>ホーム ページ上のジョブ承認の表示

承認は、ダッシュボードの **承認** セクションに表示されます。 承認者は **自分に割り当て済み** で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。 承認のジョブを送信するユーザーは、**ユーザーにより要求済** で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。

## <a name="changes-in-onboard"></a>Onboard の変更
今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。

## <a name="changes-in-core-hr"></a>Core HR の変更
このセクションに記載された変更は、ビルド番号 8.1.2390 に適用されます。

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>カスタム フィールドをサポートする Common Data Service エンティティ

- BusinessProcessCalendar                     
- BusinessProcessGroupAssignment         
- BusinessProcessStage                          
- BusinessProcessTemplateHeader          
- BusinessProcessTemplateTask            
- HcmBenefitOption                              
- HcmBenefitType                                  
- HcmCompensationGrid                            
- HcmCompensationLevel                          
- HcmCompensationPayFrequency                 
- HcmCompensationReferencePointSetup        
- HcmCompensationReferencePointSetupLine 
- HcmCompensationRegion                     
- HcmCompFixedPlanTable                     
- HcmEmployment                                
- HcmEthnicOrigin                                
- HcmFixedCompensationEvent                 
- HcmJob                                           
- HcmJobFunction
- HcmJobType
- HcmLanguageCode
- HcmPayrollCalculationFrequency
- HcmPosition
- HcmPositionType
- HcmSkillType
- HcmVeteranStatus
- HcmWorkCalendarHoliday
- HcmWorkCalendarHolidayLine
- HcmWorker
- HcmWorkerPersonalDetail
- LeaveType
- OMDepartment
- OMLegalEntity
- PayCycle
- PayPeriod
- PayrollBenefitCalculationRate
- PayrollBenefitCalculationRateDetail
- PayrollEarningCode

### <a name="unable-to-see-goals-and-reviews-in-manager-self-service"></a>マネージャー セルフサービスで目標および確認が表示されない

今週の変更により、マネージャー セルフサービスでスキップ レベル管理の目標と確認の表示および編集ができるようになりました。

### <a name="goal-form-cannot-be-closed-after-a-user-edits-any-goal-field"></a>ユーザーが目標フィールドを編集した後、目標フォームを閉じることができない

このリリースでは、**閉じる** を選択しても目標フォームが閉じない問題が修正されています。

### <a name="creating-new-goals-and-saving-displays-error"></a>新しい目標の作成および表示エラーの保存

このリリースでは、従業員およびマネージャー セルフサービスで目標を保存する際の問題が修正されます。

### <a name="unable-to-add-a-field-to-position-details"></a>職位の詳細にフィールドを追加できない 

このリリースにより、職位の詳細でカスタム フィールドがサポートされるようになりました。
 
### <a name="unable-to-set-up-expiring-date-on-the-earning-code-through-data-management"></a>データ管理により、所得コードの有効期限を設定できない

変更により、データ管理の所得コードに有効期限を設定できるようになりました。

### <a name="new-custom-fields-dont-sync-quickly-enough"></a>新しいカスタム フィールドが迅速に同期されない

今週のリリースにより、Common Data Service へのカスタム フィールドの同期のパフォーマンスが大幅に改善されました。

### <a name="entity-export-to-database-jobs-fail-with-error-message-format-of-the-initialization-string-does-not-conform-to-specification-starting-at-index-0"></a>データベース ジョブへのエンティティ エクスポートの失敗とエラーメッセージ: 「初期化文字列の形式が、インデックス 0 で始まる仕様に準拠していません。」

このリリースで、データベースのバッチ ジョブが失敗する問題が修正されます。 手動で更新するには

1. **データ管理** に移動します。
2. **データベースへのエンティティのエクスポートのコンフィギュレーション** を選択します。
3. ターゲット データベースへの接続文字列を再入力し、**保存** を選択します。

### <a name="smtp-email-configuration-suddenly-fails-with-error-message-the-smtp-server-requires-a-secure-connection-or-the-client-was-not-authenticated"></a>SMTP 電子メールのコンフィギュレーションが突然エラー メッセージと共に失敗する: 「SMTP サーバーがセキュリティで保護された接続を必要としてるか、またはクライアントが認証されていません。」

このリリースで、SMTP 電子メール コンフィギュレーションが突然失敗する問題が修正されます。 手動で更新するには

1. **システム管理** に移動します。
2. **電子メール パラメーター** を選択します。
3. **SMTP** を選択します。 
4. SMTP サーバーに使用するユーザー名とパスワードを再入力し、**保存** をクリックします。

## <a name="in-preview"></a>プレビュー

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>プレビュー機能は、サンドボックス インスタンスでのみ有効です。

Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを **実稼働** または **サンドボックス** のどちらかに指定することができます。 **サンドボックス** タイプのインスタンスにより、新機能を事前にテストできるようになります。 既存の Talent のインスタンスすべては、**実稼働** インスタンス タイプに更新されます。 既存のインスタンスのいずれかを **サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) に連絡してください。

変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。

### <a name="restrict-leave-types-in-time-off-requests"></a>休暇申請で休暇タイプを制限する

組織はさまざまな種類の休暇を従業員に提供できます。 ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。 それらの休暇タイプは、HR によって代わりに管理されることがあります。 このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。 

### <a name="view-performance-information-for-direct-and-extended-reports-in-manager-self-service"></a>マネージャー セルフサービスの直接および拡張レポートに関する業績情報の確認

新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。 現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。 また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスを確実に、スムーズに行うことができます。 この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。

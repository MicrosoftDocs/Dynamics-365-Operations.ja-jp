---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 13 日)
description: この記事では、2020 年 4 月 13 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a43b55c075102056ed7c752b72a85f2c9012d46
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051044"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 4 月 13 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.3136 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="new-production-release-cadence"></a>新しい生産リリース リズム

今週のリリースでは、Human Resources のリリース頻度が毎週更新から隔週の更新に移行します。 安全な展開プラクティスとの整合性を確保し、サービスの安定性と信頼性の高い標準を維持するために、すべての地域にサービス更新を展開するプロセスは 2 週間のロールアウトになります。 プロセスの各ステージで展開が成功したことを確認するために、追加のテストとモニターが実行されます。 リリース頻度の詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>丸めタイプを指定した後に丸め精度フィールドを編集できない (435616)

この変更により、**丸めタイプ** フィールドを更新した後に **丸め精度** フィールドが使用できるようになりました。

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>休暇計画に対して見越計上期間がない場合、休暇登録の終了日を編集できない (413628)

"フィールド 見越計上日の基準を入力する必要があります" というエラーを発生させることなく、登録終了日を編集できるようになりました。

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>雇用エンティティが Dataverse に同期されない (430834)

この変更により、財務分析コードを追加した後、雇用データが Dataverse に同期されなかった問題が修正されます。 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>作業カレンダー時間間隔エンティティのマルチ ペアレンティングの削除 (431775)

この変更により、**作業カレンダー時間間隔** エンティティのマルチ ペアレンティングが削除されます。

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>CAST 関数を使用したフィルターは OData 呼び出し職位作業者割り当てエンティティでは機能しません (431699)

この更新には、**職位作業者割り当て** エンティティに対して OData 内で CAST 関数を使用したフィルターを許可する変更が含まれています。

## <a name="in-preview"></a>プレビュー

## <a name="leave-suspension"></a>休暇の停止

従業員に対し Human Resources で休暇および欠勤を中断できます。 休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。 一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。 詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。

## <a name="carry-forward-rules"></a>繰越ルール

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="known-issues"></a>既知の問題

## <a name="employment-details-entity"></a>雇用の詳細エンティティ

**雇用の詳細** エンティティが次のフィールドで更新されました:

- **PayFrequency**
- **雇用カテゴリ ID**
- **雇用タイプ**
- **EmploymentType ID**
- **福利厚生の雇用状況**

これらのフィールドの設定データは、**機能管理** ワークスペースで有効になっている福利厚生の管理に依存します。 インポート中にエラーが発生するため、**雇用の詳細** エンティティのこれらのフィールドを入力または更新しないでください。

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>一部の環境で、SharePoint プレビューが機能しない

SharePoint で保存されているドキュメントのドキュメント プレビューが機能しない場合は、次の手順を実行します。

1. 管理者のユーザー アカウントにユーザー レコードに関連付けられたメールがあることを確認します。 この情報は、**ユーザー** ページで確認できます。 メールが設定されていない場合は、OData Excel アドインを使用してメールとプロバイダーを追加する必要があります。 既定では、Excel デザインにメール アドレスは表示されません。 Excel デザインを編集し、すべてのフィールドを追加し、適用して更新する必要があります。 これらのステップを完了すると、管理者アカウントを更新できます。

2. 管理者アカウントにメール アカウントが関連付けられたら、人事管理に管理者としてサインインします。

3. SharePoint で添付ファイルにアクセスして、ドキュメントのプレビューを開始します。

4. 添付ファイルにアクセスできる他のユーザー アカウントでサインインし、適切にプレビューが機能することを確認します。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
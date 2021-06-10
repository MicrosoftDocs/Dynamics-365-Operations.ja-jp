---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 11 日)
description: このトピックでは、2020 年 6 月 11 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6b0bb1c6d00cdd816534caddd83a71f2f0a3cc3
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054311"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 11 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.3316 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>合理化された従業員フォームにより、子フォームの閉じる (X) ボタンが機能しなくなることがある (442369)

新しい **作業者** フォームが有効になっていると、閉じる (**X**) ボタンが子フォームで機能しないことがありました。 この問題は断続的でした。 離れて戻ってきた後に、フォームを開じることができます。 たとえば、左側のメニュー項目を選択し、**作業者** フォームに戻ってから閉じることができます。 今週のリリースでは、この問題が修正されています。 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>作業者の個人連絡担当者エンティティが、親の関係タイプを持つ個人連絡先をエクスポートしない

このリリースでは、**作業者の個人連絡担当者** エンティティが、すべての関係タイプをエクスポートします。

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity は、既定で Ceridian 給与統合パッケージの一部である必要があります (448506)

この変更により、**HcmPositionWorkerAssignmentV2Entity** が Ceridian 給与統合パッケージに含まれるようになりました。

## <a name="in-preview"></a>プレビュー

## <a name="database-logging"></a>データベースのログ

データベース ログ機能を使用すると、監視するテーブルとフィールドを決定できます。 また、Change Tracking を起動するイベントを決定することもできます。 これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。 詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。

## <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、[Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md) を参照してください。 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ
 
福利厚生管理エンティティはリリースされてます。 DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。 福利厚生管理テンプレートは、データの移動に使用できます。 テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。

## <a name="buy-and-sell-leave"></a>休暇の売買 

一部の組織では、従業員が休暇を購入または売却できるという利点があります。 このプロセスは、多くの場合、手動で管理します。 この機能により、人事部門のポリシーと申請の管理を自動化します。 休暇管理プロセスを合理化し、ミスをなくすことができます。 詳細については、以下を参照してください。

- [休暇の売買ポリシーの管理](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [休暇の売買](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>1 社または 1 プランの有給休暇

顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。 この機能により、異なる休暇年数または有給休暇ポリシーを持つ顧客のために有給休暇プロセスを明確にします。 詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。

## <a name="add-attachments-to-time-off-requests"></a>添付ファイルを休暇申請に追加

承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。 従業員はこれらの添付ファイルを追加できます。 また、休暇申請がどのように更新されるかについても、より深く理解することができます。 詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。

## <a name="add-reason-code-to-accrual-suspensions"></a>休暇付与の一時停止に理由コードが追加されました 

見越計上の中断に理由コードが追加されました。

## <a name="carry-forward-rules"></a>繰越ルール 

繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。 たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。 詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>指定した休暇タイプに対する休暇付与の一時停止

無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。 無給休暇のタイプを指定できますが、必須ではあります。 他の休暇種類に基づいて、任意の休暇を停止することができます。

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF エンティティで休暇付与の一時停止が可能 

DMF エンティティが見越し計上の停止に使用できるようになりました 。

## <a name="coming-soon"></a>間もなく公開

## <a name="new-platform-capabilities"></a>新しいプラットフォーム機能 

個人用設定を使用すると、フィールドを必須にすることができます。 この機能を使用するには、**保存されているビュー** を有効にする必要があります。

## <a name="configure-the-name-of-employee-self-service"></a>従業員セルフ サービス名のコンフィギュレーション

人事管理パラメータで新しいオプションが使用可能になり、従業員セルフ サービス ワークスペースの名前をセルフ サービスに更新します。 

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
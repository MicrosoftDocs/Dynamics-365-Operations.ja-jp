---
title: Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 7 月 23 日)
description: このトピックでは、2020 年 7 月 23 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0672e3039f54a4591db49eee00d69bf5e4278fd
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528452"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 7 月 23 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。 変更は、ビルド番号 8.1.3416 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>職位の財務分析コードの削除が想定された機能をしない (445476)

職位から分析コードを削除すると、Common Data Service からも同じ職位が削除されてしまう。

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>階層にない職位が非アクティブな職位を表示する (397257)

非アクティブな (有効期間が切れている) 職位が、**階層内の職位** として職位階層に表示されなくなる。 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>データ管理フレームワーク (DMF) インポートにおける LeaveEnrollmentEntity と HcmWorkerEntity との間で検証処理が発生し、データの読み込みが遅くなる (442324)

このリリースでの変更により、**LeaveEnrollmentEntity** のパフォーマンスが向上します。

## <a name="unable-to-personalize-in-organization-administration-447490"></a>組織管理のカスタマイズができない (447490)

今回の変更では、**組織の管理** でリンクをカスタマイズできるようになります。

## <a name="in-preview"></a>プレビュー

## <a name="mandatory-fields"></a>必須項目 

人事管理のパーソナル化機能を使用することにより、項目を必須にすることができます。 この機能には **保存されたビュー** が必要です。

## <a name="human-resources-application-in-teams"></a>Teams の Human Resources アプリケーション

従業員は、Microsoft Teams 内で休暇の表示および申請ができます。 ボットと対話して、休暇申請を作成できます。 詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ
 
福利厚生管理エンティティはリリースされてます。 DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。 福利厚生管理テンプレートは、データの移動に使用できます。 テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。

## <a name="buy-and-sell-leave"></a>休暇の売買 

一部の組織では、従業員が休暇を購入または売却できるという利点があります。 このプロセスは、多くの場合、手動で管理します。 この機能により、人事部門のポリシーと申請の管理を自動化します。 休暇管理プロセスを合理化し、ミスをなくすことができます。 詳細については、以下を参照してください。

- [休暇の売買ポリシーの管理](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [休暇の売買](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>1 社または 1 プランの有給休暇

顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。 この機能を使用することで、異なる休暇年数や有給休暇ポリシーを持つ顧客に向けた有給休暇のプロセスを明確化します。 詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。

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

## <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service に含まれるチェックリスト エンティティ

オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Common Data Service ですぐに使用可能になります。

## <a name="platform-changes"></a>プラットフォームの変更

プラットフォーム 更新プログラム 10.0.12 (36)

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

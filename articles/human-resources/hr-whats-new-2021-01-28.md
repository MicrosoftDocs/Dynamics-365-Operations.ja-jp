---
title: Dynamics 365 Human Resources 2021 年 1 月 28 日の新機能および変更された機能
description: このトピックでは、2021 年 1 月 28 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b4739b5b1b6c61e829dd931ba8d4c9e0e49c8aed
ms.sourcegitcommit: fb335954f73eaa2233ef6fb1e7fab1ece3c50756
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2021
ms.locfileid: "5081294"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Dynamics 365 Human Resources 2021 年 1 月 28 日の新機能および変更された機能

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3906 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 福利厚生理由コードを **従業員管理** ワークスペースに統合する | -- | [理由コードの設定](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。


| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 539456 | カレンダーは、**詳細情報のない欠席のみを表示する** パラメータが有効な場合、ホバー テキストに休暇の種類を表示します。 | **詳細情報のない欠席のみを表示する** オプションが有効化されている場合、要求の日付がホバーに表示されるようになりました。 |
| 528907 | 従業員ロール上の法人へのアクセスを許可すると、マネージャーが従業員セルフサービスの **マイチーム** エリアで従業員の休暇残高を確認できない。 |このオプションを設定すると、マネージャーは休暇残数活動を引き続き確認できます。 |
| 526280 | HcmWorkerEntity、HcmEmployeeEntity、HcmContractorEntity でアクセス許可エラーが発生する。 | 非システム管理者ロールのユーザーが、NationalityCountryRegion フィールドのアクセス許可エラーにより、一覧表示されているエンティティをエクスポートできない。 ユーザーは、この情報をエクスポートするために引き続き次の権限が必要です : HcmWorkerEntityMaintain、HcmWorkerEntityView、HcmEmployeeEntityMaintain、HcmEmployeeEntityView、HcmContractorEntityMaintain、HCMContractorEntityView 。 |
| 542147 | 従業員セルフサービスで銀行口座を追加する場合、**銀行口座番号** と **ルーティング番号** フィールドが必須となる。 | 従業員が銀行口座の詳細を追加する際に、**銀行口座番号** と **ルーティング番号** のフィールドが必須となるエラーを修正しました。 これらのフィールドは、新たな銀行口座情報を保存する際に必須項目ではなくなりました。 |
| 543641 | 郵便番号が電子レポートに入力されない。 | カバレッジコード L から Q の ACA レポートで郵便番号が入力されないバグを修正しました。 |
| 545402 | UserBranding.js ファイルのルーティング変更を追加し、404 エラーを削除します。 | コンソールで 404 エラーが表示されなくなりました。 |

## <a name="in-preview"></a>プレビュー   

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams の Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |
| マネージャーの休暇を会社間で表示 | [マネージャーの従業員休暇を会社間で表示](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [休暇と欠勤のパラメータのコンフィギュレーション](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| 福利厚生の確認メール | この機能により、従業員が従業員セルフサービスの給付金登録エクスペリエンスからチェックアウトする際に、確認メールを送信するオプションが提供されます。 この機能は 2 月 1 日にリリースされます。 詳細については、[会社ごとの福利厚生管理パラメータの構成](hr-benefits-setup-parameters-per-company.md)を参照してください。 |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse の専門用語の更新

2020 年 11 月より、 Common Data Service は [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro) に改名されます。 詳細については、Power Apps ブログの [公式声明](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)を参照してください。 この改名に関連して、用語 Dataverse が更新されています。 たとえば、*エンティティ* は *テーブル* になり、*フィールド* は *列* になります。 詳細については、[用語の更新](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)を参照してください。

このリリースでは、Dynamics 365 Human Resources と Dataverse の統合に関する用語は、アプリケーション全体で更新されており、これら変更が反映されています。 たとえば、**Common Data Service 統合** フォームが **Microsoft Dataverse 統合** となっています。

Dynamics 365 Human Resources と Microsoft Dataverse の統合の詳細については、[Microsoft Dataverse の統合を構成する](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) と [Microsoft Dataverse の仮想テーブルを構成する](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
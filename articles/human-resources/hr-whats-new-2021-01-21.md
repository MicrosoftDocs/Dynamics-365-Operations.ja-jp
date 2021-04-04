---
title: Dynamics 365 Human Resources 2021 年 1 月 21 日の新機能および変更された機能
description: このトピックでは、2021 年 1 月 21 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
manager: tfehr
ms.date: 01/21/2021
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
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fc3bb035686a46030514aca1f5ad03a2681845fd
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463529"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Dynamics 365 Human Resources 2021 年 1 月 21 日の新機能および変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2020 リリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。


## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.3866 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| プラットフォーム更新プログラム 10.0.16(40) | -- | [Finance and Operations アプリのバージョン 10.0.16 のプラットフォーム更新プログラム (2021 年 2 月)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16) |
| ワークフローの申請と承認の強化 | [組織および人事管理ワークフロー エクスペリエンスの強化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [自分のリストに割り当てられた作業項目を配置するコンフィギュレーション オプション](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| フォーム1095-C、フォーム1095-B、レガシ-の福利厚生に関する電子報告に対する、アフォーダブルケア法 (ACA) 準拠の更新 | -- | -- | 
| 福利厚生管理では、米国に拠点を置く法人に対する ACA に準拠するレポートに対応します | -- | [福利厚生管理での ACA レポートの生成](hr-benefits-management-aca-reports.md) |
| 福利厚生管理に、福利厚生レート層および福利厚生率の2層エンティティが含まれています  | -- | -- |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 533079 | 控除を表示しようとする場合のナビゲーション エラー: 「フォームが間違って呼び出されました」。 | **対象の日付時点** の福利厚生控除を表示する際のエラーの修正。 |
| 543641 | 郵便番号が電子レポートに入力されない。  | 補充コードが M から Q の場合に、ACA の福利厚生管理用の電子レポートに表示されない内部バグを修正しました。 |
| 542815 | 従業員セルフサービスの個人連絡先画面で、従業員が他の人の個人連絡先を参照できてしまう。 | 従業員セルフサービスの個人連絡先の **編集** フォームで、当人の連絡先のみを取得するようクエリに制限がされておらず、キーボード ショートカットをするとて他者の連絡先を表示できてしまう問題を修正しました。 |
| 536157 | IsVirtualEntityPackageInstalled() 呼び出しの影響で、システム管理ページで、**Microsoft Dataverse 統合** ページを開けない。 | 問題が発生して、Human Resources で  **Microsoft Dataverse 統合** ページを読み込めない。 |
| 533079 | 控除を表示しようとする場合のナビゲーション エラー: 「フォームが間違って呼び出されました」。 | **指定日時点** で、福利構成管理の **控除** フォームを表示する際に発生するエラーの修正。 |
| 537264 | 候補者レコードの **人物情報** クイックタブが表示されない。 | 候補者レコードで、人物の情報が参照できるようになりました。 |
| 537267 | 社内の候補者レコードで **職務経験** が表示されない。 | 社内の候補者レコードで **職務経験** クイックタブが表示されるようになりました。 社内の候補者である場合、**職務経験** が組織内の候補者の職歴を表示する **職歴** に置換えられています。 内部候補はどちらにも該当し、表示される必要があります。 |
| 537067 | **雇用主への連絡を許可する** は表示されません。 | 候補者レコードの **職業経験の編集** ペインに **雇用主との接触を許可** コントロールが追加されました。 |
| 525957 | 転送の完了後も、内部候補者の **候補者の状態** が更新されない。 | 転送の完了後 (**作業者転送して新規職位に割り当てる** ページで **職位の変更** or **続行** ボタンが選択されている) は、候補者レコードの **状態** は、**採用済** に変更される必要があります。 |
| 537051 | インドのルピーとトルコのリラの通貨記号が Dataverse と同期しない | インドのルピーとトルコのリラの通貨記号が Dataverse と同期するようになりました。 |
| 534846 | データ管理には採用テーブルが有効化されている必要があります。 | 採用依頼や求職者向けに作成された新しいテーブルが、データ管理に対応するようになりました。 これにより、テーブルの変更追跡が有効になり、Dataverse 仮想テーブルの OData の変更追跡が有効になります。 |
| 533474 | Microsoft.SqlServer.XEvent.dll への欠落している参照の修正。 | Microsoft.SqlServer.XEvent.dll の組み立て負荷例外が、一部の環境で仮想テーブルの設定 Dataverseをブロックしている。 |
| 481122 | 退職した職位を示す **ユーザー** のワークスペース。 | 退職した職位は、**ユーザー** ワークスペースでオープンな職位として表示されます。 退職した職位は表示されなくなりました。 | 
| 541978 | 基本メール アドレスを BaseWorker エンティティに追加します。 | この変更により、作業者の基本メール アドレスが HcmWorkerBaseEntity に追加されました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| Microsoft Teams の Human Resources アプリ | [Microsoft Teams の従業員の休暇および欠勤体験](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Teams での休暇要求の管理](hr-teams-leave-app.md) |
| LinkedIn タレント ハブとの統合 | [LinkedIn タレント ハブとの統合](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn Talent Hub との統合](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| マネージャーの休暇を会社間で表示 | [マネージャーの従業員休暇を会社間で表示](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [休暇と欠勤のパラメータのコンフィギュレーション](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|休暇残高に追加の分析情報を提供する| [休暇残高に追加の分析情報を提供する](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [従業員の休暇の管理](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| マネージャーは職位の採用要求を送信できます | [マネージャーは空いている職位の採用要求を送信できます](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [採用要求の追加](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| 人材管理で改善された候補者のプロファイル | [人材管理で改善された候補者のプロファイル](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [候補者プロファイルの追加または編集](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| 簡素化された採用プロバイダーとの統合を有効化 | [簡素化された採用プロバイダーとの統合を有効化](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [職務候補者の採用](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>間もなく公開
| 機能 | 細目 |
| --- | --- |
| 福利厚生の確認メール | この機能により、従業員が従業員セルフサービスの給付金登録エクスペリエンスからチェックアウトする際に、確認メールを送信するオプションが提供されます。 詳細については、[会社ごとの福利厚生管理パラメータの構成](hr-benefits-setup-parameters-per-company.md)を参照してください。 |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse の専門用語の更新

2020 年 11 月より、 Common Data Service は [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro) に改名されます。 詳細については、Power Apps ブログの [公式声明](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)を参照してください。 この改名に関連して、用語 Dataverse が更新されています。 たとえば、*エンティティ* は *テーブル* になり、*フィールド* は *列* になります。 詳細については、[用語の更新](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)を参照してください。

このリリースでは、Dynamics 365 Human Resources と Dataverse の統合に関する用語は、アプリケーション全体で更新されており、これら変更が反映されています。 たとえば、**Common Data Service 統合** フォームが **Microsoft Dataverse 統合** となっています。

Dynamics 365 Human Resources と Microsoft Dataverse の統合の詳細については、[Microsoft Dataverse の統合を構成する](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) と [Microsoft Dataverse の仮想テーブルを構成する](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities)を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
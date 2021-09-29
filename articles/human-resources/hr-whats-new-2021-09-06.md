---
title: Dynamics 365 Human Resources の新機能と変更された機能 2021 年 9 月 6 日
description: このトピックでは、2021 年 9 月 6 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 09/06/2021
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
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2add53b4b014cb65caacff03bf175078d2b70d8f
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485910"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Dynamics 365 Human Resources の新機能と変更された機能 2021 年 9 月 6 日

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Microsoft Dynamics 365 Human Resources の新機能、変更された機能または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4443 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| フィーチャー | リリース計画 | ドキュメント |
|---|---|---|
| 休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | このリリースでは、休暇マネージャーのワークスペース ビューを更新しています。 詳細については、[休暇マネージャー ロールのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168107)を参照してください。 |
| 休暇タイプごとに添付ファイル要件を構成する | [休暇タイプごとに添付ファイル要件を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168108) |
| 休暇タイプごとに休暇単位を構成する | [休暇タイプごとに休暇単位を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新する可能性があります:

| 問題の番号 | 問題 | 説明 |
|---|---|---|
| 610128 | HcmDiscussionOverallCommentEntity を使用した場合のデータの公開に関するエラー | Excel のワークブックから HcmDiscussionOverralCommentEntity エンティティにデータを公開すると、次のエラーが発生する場合がありました: 「HcmTopicOverrall タイプのデータソース レコードが見つかりません。」 |
| 589073 | EEO-1 レポートでは、 **性別** フィールドの「該当なし」と空白の値を「女性」の値としてカウントしています。 | **性別** フィールドに **男性** が指定されていない場合、EEO-1 レポートには既定値として **女性** が入力されます。 |
| 589617 | ユーザーの役割が特定の法人に限定されている場合に、休暇カードの残数、購入可能額、販売可能額が表示されない問題がありました。 | ユーザー (従業員の役割) が特定の法人に限定されている場合、**休暇残数** カード、および **購入可能** と **販売可能** フィールドに残高が正しく表示されません。 |
| 604310 | ユーザーに休暇階層が割り当てられていない場合、[休暇マネージャ] タブは非表示にします。 | ある法人で、会社間パラメータが有効で、少なくとも 1 つの休暇階層がユーザーに関連付けられていない限り、**休暇マネージャ** タブはセルフサービス ポータルで非表示にする必要があります。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオン/オフにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| フィーチャー | リリース計画 | ドキュメント |
|---|---|---|
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md) |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [支払準備完了](/dynamics365/human-resources/hr-compensation-payroll) |
| Eligibility のカスタム フィールド |[適格性処理でのカスタム フィールドのサポート](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [適格性処理でのカスタム フィールドの使用](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

| フィーチャー | 細目 |
|---|---|
| プラットフォーム 更新プログラム 10.0.21 (45) | プラットフォーム更新プログラム 10.0.21 のロールアウトは、2021 年 10 月 4 日のサービス リリースで開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) を参照してください。 |
| 福利厚生の明細書 | 従業員の現在の福利厚生選択を確認するための福利厚生明細書。 詳細については、リリース サイクル ドキュメント[福利厚生の明細書](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement)を参照してください。 |

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

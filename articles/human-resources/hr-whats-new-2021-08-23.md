---
title: Dynamics 365 Human Resources 2021 年 8 月 23 日の新機能または変更された機能
description: このトピックでは、2021 年 8 月 23 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c3448c373600ffebca82be41fb5849b952dfe1
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686830"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Dynamics 365 Human Resources 2021 年 8 月 23 日の新機能または変更された機能

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Microsoft Dynamics 365 Human Resources の新機能、変更された機能または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4419 に適用されます。

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新する可能性があります:

| 問題の番号 | 問題 | 説明 |
| --- | --- | --- |
| 594066 | 連絡先情報を削除できない | 従業員の連絡先情報レコードの削除を選択すると、選択したレコード以外の連絡先情報レコードが削除されます。 |
| 611339 | 個人用設定を追加すると、銀行口座はフィルタを無視して最初のレコードをフェッチする | 個人用設定を追加すると、データ ソース クエリの実行後に個人用設定クエリを実行した場合、銀行口座リストでは、詳細が表示されている作業者に関係なく、最初のレコードがクエリでフェッチされます。 |
| 591806 | オンボード期日のタスクの計算が間違っている | 次の条件が存在する場合、期日が誤って計算されます。作成されたチェックリストは、拡張された時間範囲 (2005年から2050年など) を使用するカレンダーを使用しており、ユーザーの設定で中部標準時以外のタイム ゾーンが使用されている。 |   
| 592749 | **従業員セルフ サービス** で休暇残り日数が正しくない | 従業員が複数の法人で雇用されている場合に、会社間休暇ビューが有効になっていると、休暇残り日数が正しく表示されない場合があります。 |
| 603133 | 休暇を申請する場合の予期しない警告 | 休暇を申請する場合、**合計** フィールドの前に **半日** フィールドに入力すると 、予期しない警告が発生します。 |
| 606546 | 承認済の休暇で、選択用のフィールドが表示されない | 複数の承認済休暇申請を選択するチェック ボックスが表示されません。 |
| 597059 | **会社の休暇と欠勤カレンダー** に作業者が表示されない | 申請された日付範囲に休暇申請が拒否された日付が含まれる場合、作業者が **会社の休暇と欠勤カレンダー** に表示されません。 |


## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオン/オフにする方法の詳細については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| フィーチャー | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|
| 休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | このリリースでは、休暇マネージャーのワークスペース ビューを更新しています。 詳細については、[休暇マネージャー ロールのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168107)を参照してください。 |
| 休暇タイプごとに添付ファイル要件を構成する | [休暇タイプごとに添付ファイル要件を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168108)|
| 休暇タイプごとに休暇単位を構成する | [休暇タイプごとに休暇単位を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [支払準備完了](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>間もなく公開

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/) を参照してください。

| フィーチャー | 細目 |
| --- | --- |
| プラットフォーム 更新プログラム 10.0.21 (45) | プラットフォーム更新プログラム 10.0.21 のロールアウトは、2021 年 10 月 4 日のサービス リリースで開始する予定です。 詳細については、[Finance and Operations アプリのバージョン 10.0.21 のプラットフォーム更新プログラム (2021 年 10 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) を参照してください。 |

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

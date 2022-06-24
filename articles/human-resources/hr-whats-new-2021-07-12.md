---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 7 月 12 日)
description: この記事では、2021 年 7 月 12 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 259004773c4e5a7d8865d563da9bcfea3a116632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870961"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Dynamics 365 Human Resources の新機能または変更された機能 (2021 年 7 月 12 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の新機能、変更された機能または間もなく近日公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4353 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
|  勤続年数表示の切り替え | |この機能は、異なる日付を使用して、**合理化された従業員の入力** ページと **ユーザー** ページに表示される勤続年数を計算するオプションを提供します。  これは、[Human Resources パラメーター](/dynamics365/human-resources/hr-setup-parameters)で使用可能になります。 |


### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 この記事が最初に公開された後に、ビルドに加えたバグ修正を含めるために、この記事を更新する可能性があります。

| 問題の番号 | 問題 |  Description |
| --- | --- | --- |
| 595871 | Human Resources のバージョン情報ウィンドウに誤った Dataverse 用語があります | Common Data Service のブランドを Dataverseに変更したことにより、Microsoft Dynamics 365 Human Resources 情報ペイン (**ヘルプとサポート > バージョン情報**) の用語が更新されました。 |
| 598676 | 合理化された従業員入力フォームがタスクに上書きされる場合、保存されたビューで使用するとエラーが発生する場合があります| **作業者** ページで、合理化された従業員エントリ機能がオンになっている場合、保存されたビューで **編集のために常に開く** が設定されていると、アプリケーションが失敗することがあります。 |
| 592344 |役職に関する労災の項目は、福利厚生管理が有効になっている場合にのみ読めるようになります | 労災の情報は、レガシー福利厚生機能を使用して作成されます。  福利厚生管理が有効な場合、フィールドは読み取り専用になります。 福利厚生管理がオンになっていて、HR 共有パラメーターで **レガシー福利厚生フォーム非表示** が **はい** に設定されている場合、**労働災害補償** タブは非表示になります。 |
| 598617 | **HcmDiscussion** フォームのアクティブ化タブは、パーソナライズが適用されると無限ループを引き起こします | グリッド ビューと詳細ビューの両方で **編集用に常に開いている** がオンになっている場合、上書きされたタスク メソッドのタブをアクティブ化するコードは、どのコントロールにフォーカスを設定するかについてのパーソナライズと競合し、無限ループを作成します。 |
| 593553 | パフォーマンス仕訳帳の仕訳帳の日付フィールドが UTC で表示されている | パフォーマンス ジャーナルの **ジャーナル日付** フィールドは、システム日付設定で定義されたタイム ゾーンではなく UTC タイム ゾーンで表示されるため、一部のタイム ゾーンでは日付が正しくありません。 |
| 586930 | 業績目標のための活動の開始は、全く異なるレコードを開く | 機能管理で「パフォーマンス ジャーナル拡張レポート ビュー」機能が有効になっている場合、**従業員セルフ サービス** の **マイ チーム** タブで拡張レポートのパフォーマンス目標を選択すると、選択した従業員ではなく、従業員の目標が開きます。 |
| 569959 |  HcmPositionWorkerAssignmentV2 エンティティはポジションに作業者を割り当てません | エンティティを介して位置割り当てレコードを追加すると、ユーザーがエラーを受け取り、公開に失敗しました。 |
| 582259 | VETS 4212 レポートでは、2020 フォームの代わりに 2017 フォームが使用されます | 2020 形式に更新されます。  新しいフォーマットをロードするには、**レポート構成** に移動し、左側の列の VETS-4212 レポートを削除します。 **電子報告 - リポジトリ - HR リソース** に移動し、**開く** を選択します。  **VETS-4212 PDF 印刷** を選択し、**インポート** を選択します。|


## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 簡素化された給与統合 (給与統合 API) を有効にする | [簡素化された給与プロバイダーとの統合を有効にする](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [給与統合 API](hr-admin-integration-payroll-api-introduction.md)|
|  休暇マネージャの休暇管理の有効化 | [休暇マネージャの休暇管理の有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [休暇マネージャー ロールの構成](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  休暇タイプごとに添付ファイル要件を構成する | [休暇タイプごとに添付ファイル要件を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  休暇タイプごとに休暇単位を構成する | [休暇タイプごとに休暇単位を構成する](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[休暇および欠勤タイプのコンフィギュレーション](https://go.microsoft.com/fwlink/?linkid=2168215)|
| 従業員の支払準備完了のマークの有効化 | [従業員の支払準備完了のマークの有効化](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [支払準備完了](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| プラットフォーム 更新プログラム 10.0.20 (44) | プラットフォーム更新プログラム 10.0.20 は、2021 年 7 月 26 日のサービス リリースで、展開を開始する予定です。 詳細については、[財務と運用アプリのバージョン 10.0.20 のプラットフォーム更新プログラム (2021 年 8 月)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) を参照してください。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

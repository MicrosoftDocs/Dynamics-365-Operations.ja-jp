---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2021 年 3 月 22 日)
description: このトピックでは、2021 年 3 月 22 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13520ca55c98fb1acb6185af393550b12fbc2072
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693531"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2021 年 3 月 22 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の新機能、変更された機能、または間もなく公開される機能について説明します。

更新プロセスとスケジュールの詳細については、[更新プロセス](hr-admin-setup-update-process.md) を参照してください。

新機能と予想される一般提供日の詳細については、[Dynamics 365 Human Resources 2021 リリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="in-this-release"></a>今回のリリース

今回のリリースには、次の新機能とバグ修正が含まれています。 変更は、ビルド番号 8.1.4049 に適用されます。

### <a name="new-features"></a>新機能

このリリースでは、次の機能が一般に使用可能です。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 行き詰まったバッチ ジョブのキャンセルとリセットを強制するオプション (560976) | NA | [行き詰まったバッチ ジョブのリセット](./hr-admin-troubleshooting-batch-execution.md) |
| 新しい福利厚生計画を作成するための UX のマイナーな更新 (419941) | NA | [給付金プランの作成](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>バグ修正

このリリースには、次のバグ修正が含まれています。

> [!NOTE]
> 私たちの目標は、この情報をできるだけ早くお客様にお届けすることです。 このトピックが最初に公開された後に、ビルドに加えたバグ修正を含めるために、このトピックを更新することがあります。

| 問題の番号 | 出庫 |  説明 |
| --- | --- | --- |
| 554239 | **BusinessProcessTaskTaskGnment** テーブルに関連するエンティティのパフォーマンスの向上 | テーブルに推奨されるインデックスを追加して 、**BusinessProcessTaskTaskGnment** テーブルに関連するエンティティのパフォーマンスを向上させます。 |
| 566061 | 夜間同期から V2 エンティティのフォールバック コードを削除 | 夜間 Dataverse 同期の V2 フォールバック コードを削除します。フォールバックは不要になったので、フィルター処理された同期が予期した通り動作しなくなりました。 この変更により、Dataverse データ同期の整合性が強化されます。 |
| 538024 | [労働手当プラン] > [チェックアウトの開始エラーの削除] | [作業者の給付金] フォームの [給付金計画] オプションのチェックアウトを削除する際に発生するエラーが修正されました。 |
| 557965 | **福利厚生** ワークスペース: **有効なライフ イベント** リンクは、常に **リンク** セクションに表示されている必要があります | **リンク** セクションに **有効なライフ イベントのリンク** が表示されたが、**(プレビュー) 給付金管理ワークスペース** 機能のこの機能が無効になっている状態で移動しようとするとエラーが発生する問題を修正しました。 ワークスペースの有効化の詳細については、[福利厚生管理ワークスペース](hr-benefits-management-workspace.md)を参照してください。 |
| 556672 | **合理化された従業員の入力** が機能管理で有効化された場合に、退職した従業員の見越計上を処理できない | 機能管理で **合理化された従業員の入力** が有効になっている場合、休暇計画を見越計上するためのオプションが **従業員の作業履歴** の **その他のオプション** に追加されました。 |
| 562656 | **SysRecordChangeLogValidTimeState** メニュー項目が、セキュリティ特権と **SystemExternalBasicMaintain** セキュリティ職務権限の拡張機能に含まれる | システム以外の管理者ロールに、日付マネージャー フォームの **変更の表示** ボタンが表示されません。 |
| 505989 | ライフ イベント処理: 使用した日付による適格性の変更が正しく処理されない | 適格性処理の変更が現在の職位のみではなく職位の開始日に依存する問題を修正しました。 |
| 562286 | 作業者の退職により Dataverse に複数の更新が送信される | 作業者が退職すると、複数の更新操作が Dataverse に送信され、同じ変更に対して 2 つの更新通知が表示されます。 Power Automate フローがアクションからトリガーするよう構成されている場合、これにより複数のトリガーが発生する場合があります。 |
| 527340 | 休暇および休暇登録開始時に「表現できない DateTime」エラーが表示される | 休暇登録を選択する際、エラーは表示されなくなりました。 |
| 561663 | クラスターのプロビジョニングの待機時間の間隔を引き上げる | インフラストラクチャ セキュリティおよびクラスター プロビジョニングの更新との整合性を向上しました。 |
| 486129 | **職位 > 変更の管理** のカスタム フィールドを編集できない | **職位** の **変更の管理** タブでカスタム フィールドが編集できない問題を修正しました。 |

## <a name="in-preview"></a>プレビュー

次の新機能はプレビュー中です。 機能をオンまたはオフにする方法については、[機能の管理](hr-admin-manage-features.md) を参照してください。

| 機能 | リリース計画 | ドキュメント |
| --- | --- | --- |
| 給付金管理ワークスペース | [給付金管理ワークスペース (プレビュー)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [給付金管理ワークスペース](hr-benefits-management-workspace.md) |
| 従業員がビジネスの連絡先情報を編集するのを制限する | [従業員がビジネスの連絡先情報を編集するのを制限する](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [個人情報の編集の制限](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>間もなく公開

| 機能 | 細目 |
| --- | --- |
| マネージャーが従業員に対して入力したスキルは、ワークフローで自動承認できます | 間もなく公開予定。 |

予定されている機能とリリースの完全な一覧については、[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/) を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 のリリース ウェーブ 1 の概要](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
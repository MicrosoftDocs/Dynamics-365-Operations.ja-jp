---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 3 日)
description: この記事では、2020 年 3 月 3 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
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
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf5b5ce9efbd2014164db213ff20d28d20ecf3e
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712307"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 3 月 3 日)

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2955 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service ソリューションが、次の変更で利用可能になりました。

次の変更により、新しい Common Data Service ソリューションがまもなく利用可能になります。

| 説明 | 計上額 |
| ----------------------------------------- | --- |
| **職務/職位**エンティティの変更 | 追加された**報酬地域**</br>追加された**財務分析コード** |
| **作業者**エンティティの変更 | 追加された**名前の順序**</br>追加された**自宅から作業**</br>追加された**言語**</br>追加された**勤続日数**</br>追加された**記念日**</br>追加された**元の採用日付** |
| **雇用**エンティティの変更 | 追加された**財務分析コード**</br>追加された**退職理由**</br>**移行日**から名前変更された**退職日**</br>追加された**猶予期間** |
| **作業者住所**エンティティの変更 | 追加された**番地**</br>廃止としてマークされた**住所行 1**、**住所行 2**、および**住所行 3** |
| 新しい変動報酬の設定エンティティ | **変動報酬プラン タイプ**</br>**変動報酬プラン**</br>**給付ルール**</br>**変動報酬プラン レベル** |
| 新しい**作業者カレンダー雇用**エンティティ | 追加された**作業カレンダー エンティティ** |
| 新しい**給与職位詳細**エンティティ | 追加された**給与職位詳細** |
| 新しい**肩書**エンティティ | 追加済み**タイトル**。 新しい**タイトル** エンティティが、Human Resources と Common Data Service の間の同期プロセスに含まれます。 **職位**または**ジョブ** エンティティから最初に参照されることはありません。 |

今後数週間のうちに、これらのエンティティの変更がすべての環境で使用できるようになります。 Human Resources の最新 Common Data Service ソリューションを手動でインストールするには、次の操作を行います。

1.  [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) に移動します。

2.  **環境**を選択します。

3.  アップグレードする環境を検索します。 環境は、Human Resources の**バージョン情報**フォームで、**Common Data Service 情報**セクションの**環境名**に対応している必要があります。

4.  環境の詳細を表示するための環境を選択します。

5.  上部の操作バーで、**ソリューションの管理**を選択します。 新しいブラウザー ウィンドウが開き、環境のコンテキストで**Dynamics 365 管理センター**に移動します。

6.  **ソリューション** リストで、**Dynamics 365 Human Resources アンカー**を選択します。

7.  最新のソリューションを適用するには、**アップグレード**を選択します。

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>休暇登録データ エンティティを含むインポートの問題 (406082)

新しい登録日が前のプランの登録期限日より後である場合、同じタイプの新しい休暇プランに従業員を登録できるようになります。

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>DMF の 401k payrollWorkerEnrolledBenefitDetail エンティティでの利益率のエクスポートに関する問題 (420700)

この変更により、**payrollWorkerEnrolledBenefitDetail** エンティティのエキスポート機能が修正され、雇用主貢献度の現在の値が反映されるようになりました。

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>合理化された作業者のフォームを検索すると、個人フィールドに入力する必要があるというメッセージが表示されます (402525)

従業員を検索する場合、**個人** フィールドに入力する必要があるというメッセージは表示されなくなります。

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>ノート フィールドの値がスキルの追加フォームに表示されません (380134)

この変更により、従業員のセルフ サービスの**スキルの追加**フォームを個人用設定する場合に発生する問題が修正されます。

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>従業員を移動する場合、複数の固定報酬プランが期限切れになりません (389466)

この変更により、古い職位のすべての有効な固定報酬レコードが移行日に期限切れになります。

## <a name="in-preview"></a>プレビュー

次のプレビュー機能が 2020 年 2 月 3 日に利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)
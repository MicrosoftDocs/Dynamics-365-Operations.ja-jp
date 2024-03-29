---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 12 日)
description: この記事では、2020 年 2 月 12 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ce265627bf5cef023770be3f8953e12d49866be
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686914"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 12 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2867 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>既存のエンティティ CompFixedEmpls および HcmPersonImage は、OData からアクセス可能である必要がある (414178)

今週のリリースにより、**CompFixedEmpls** と **HcmPersonImage** エンティティはパブリックになり、ODAta を介して使用できるようになりました。

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>雇用の詳細が有効でない場合、Dataverse からの雇用の削除は機能しない (403193)

この変更により、有効な雇用の詳細が存在しない場合でも、Dataverse 経由で雇用を削除できるようになります。

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>コース登録ワークフローは、2 回目の承認後に完了およびエラーにステータスを変更する (409749)

コース登録ワークフローは、複数の承認者が使用できるように更新されました。

## <a name="in-preview"></a>プレビュー

2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。

## <a name="coming-soon"></a>間もなく公開

### <a name="platform-update-32"></a>プラットフォーム update 32 

プラットフォームの更新 32 はまもなく使用可能になります。 [プラットフォームの更新 32 に関する詳細情報はこちらを参照してください](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md)。

### <a name="updated-dataverse-solution"></a>更新された Dataverse ソリューション

次の変更により、新しい Dataverse ソリューションがまもなく利用可能になります。

| 説明 | 計上額 |
| ----------------------------------------- | --- |
| **職務/職位** エンティティの変更 | 追加された **報酬地域**</br>追加された **財務分析コード** |
| **作業者** エンティティの変更 | 追加された **名前の順序**</br>追加された **自宅から作業**</br>追加された **言語**</br>追加された **勤続日数**</br>追加された **記念日**</br>追加された **元の採用日付** |
| **雇用** エンティティの変更 | 追加された **財務分析コード**</br>追加された **退職理由**</br>**移行日** から名前変更された **退職日**</br>追加された **猶予期間** |
| **作業者住所** エンティティの変更 | 追加された **番地**</br>廃止としてマークされた **住所行 1**、**住所行 2**、および **住所行 3** |
| 新しい変動報酬の設定エンティティ | **変動報酬プラン タイプ**</br>**変動報酬プラン**</br>**給付ルール**</br>**変動報酬プラン レベル** |
| 新しい **作業者カレンダー雇用** エンティティ | 追加された **作業カレンダー エンティティ** |
| 新しい **給与職位詳細** エンティティ | 追加された **給与職位詳細** |
| 新しい **肩書** エンティティ | 追加済み **タイトル**。 新しい **タイトル** エンティティが、Human Resources と Dataverse の間の同期プロセスに含まれます。 **職位** または **ジョブ** エンティティから最初に参照されることはありません。 |

## <a name="see-also"></a>参照

[Human Resources の新機能および変更された機能](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
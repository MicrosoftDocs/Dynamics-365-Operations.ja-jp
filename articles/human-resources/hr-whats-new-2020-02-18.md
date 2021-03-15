---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 18 日)
description: この記事では、2020 年 2 月 18 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e087095807f587536f2dad7e65fbc8beaa88878e
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128068"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 18 日)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2903 に適用されます。 ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。

## <a name="platform-update-32"></a>プラットフォーム update 32 

プラットフォーム更新プログラム 32 が使用できるようになりました。 詳細については、[Finance and Operations アプリのプラットフォーム更新プログラム 32 (2020 年 2 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32) を参照してください。

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>合理化された従業員フォームで表示オプションを変更すると、検索値が記憶される (383833)

新しい **作業者** フォームでは、表示オプションを変更して変更を適用したときに検索値が記憶されるようになりました。

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>プレビュー機能で報酬管理の概要タイルが間違ったフォームにリダイレクトされる (401861)

固定および変動報酬管理タイルでは、新しい **作業者** フォームに正しいレコードが表示されるようになりました。 合理化された従業員フォームのプレビュー機能にのみ適用されます。 このプレビュー機能は、**機能管理** で有効にすることができます。 詳細については [機能の管理](hr-admin-manage-features.md) を参照してください。

## <a name="empty-status-field-for-some-leave-request-records-in-dataverse-414915"></a>Dataverse の一部の休暇申請レコードの空のステータス フィールド (414915)

この変更により、休暇申請の **ステータス** フィールドが **確認** に設定されている場合の Dataverse の問題が修正されます。 Dataverse でステータスが反映されるようになりました。

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>割り当てられた職務でのみ使用可能なスキル ギャップ分析 (411390)

Human Resources で定義されているすべての職務に対してスキル ギャップ分析を行うことができるようになりました。

## <a name="system-currency-doesnt-sync-from-dataverse-to-human-resources-in-new-environments-418011"></a>新しい環境で、システム通貨が Dataverse から Human Resources に同期しない (418011)

Dataverse のシステム通貨を Human Resources に同期できるようになりました。

## <a name="in-preview"></a>プレビュー

- [休暇のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [福利厚生管理のプレビュー機能](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>間もなく公開

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
[Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[更新プロセス](hr-admin-setup-update-process.md)</br>
[機能の管理](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 3 日)
description: この記事では、2020 年 2 月 3 日に更新された Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 09af17051450c14f806282df193aaaa08d7bd3fd0e522475b7d0aea82d8b132c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772667"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-3-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 3 日)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2809 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

## <a name="cant-remove-activities-from-performance-review-form-403542"></a>業績の確認フォームからは活動を削除できません (403542)

選択した活動は、**業績の確認** フォームの **削除** ボタンを使用して削除できます。

## <a name="in-preview"></a>プレビュー

2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md) を参照してください。

## <a name="coming-soon"></a>間もなく公開

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
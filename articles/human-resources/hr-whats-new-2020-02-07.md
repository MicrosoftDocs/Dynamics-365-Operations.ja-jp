---
title: Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 7 日)
description: この記事では、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78043273fb98a12a8d33f7bb94ba8ad2e9fb49fb
ms.sourcegitcommit: 13c4a6f98ccce243d6befde90992aefcf562bdab
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029960"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Dynamics 365 Human Resources の新機能および変更された機能 (2020 年 2 月 7 日)

この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。 変更は、ビルド番号 8.1.2835 に適用されます。 ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>ラーニング分析で、教室が空白の場合にコースが表示されない (388289)

教室が空白の場合、ラーニング分析ページにコースが表示されるようになりました。

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>職位検索でタイムゾーンが考慮されない (405344)

職位が空いているかどうかを検証する際、空いている職位の検索でタイムゾーンが考慮されるようになりました。

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>現在の休暇残高分析ビューが、休暇申請を送信した後の現在の休暇残高で更新されない (409756)

現在の休暇残高に送信された休暇申請が含まれるようになりました。

## <a name="in-preview"></a>プレビュー

2020 年 2 月 3 日に次のプレビュー機能が利用可能になります。

- **休暇および欠勤のプレビュー機能** - 詳細については、[休暇および欠勤のプレビュー機能](hr-leave-and-absence-overview.md?leave-and-absence-preview-features) を参照してください。

- **福利厚生管理プレビュー機能** - 既知の問題など、詳細については[福利厚生管理の概要](hr-benefits-management-overview.md)を参照してください。

## <a name="coming-soon"></a>間もなく公開

### <a name="platform-update-32"></a>プラットフォーム update 32 

プラットフォームの更新 32 はまもなく使用可能になります。 [プラットフォームの更新 32 に関する詳細情報はこちらを参照してください](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32)。

### <a name="updated-common-data-service-solution"></a>更新された Common Data Service ソリューション

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
| 新しい**肩書**エンティティ | 追加済み**タイトル**。 新しい**肩書**エンティティは、Human Resources と Common Data Service 間で同期プロセスに含められますが、最初は**職位**または**職務**エンティティから参照されることはありません。 |


---
title: 従業員のコンピテンシーと開発 Power BI コンテンツ
description: この記事では、従業員のコンピテンシーと開発 Power BI コンテンツについて説明します。
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.openlocfilehash: 1ddc117c83e551374bc8da6872429e3bb9eeee58
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280961"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>従業員のコンピテンシーと開発 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

この記事では、従業員のコンピテンシーと開発 Power BI コンテンツについて説明します。 

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
コンテンツ パックをデータに接続した後に、レポートに組織のデータが表示されます。 以前に Microsoft Power BI を使用したことがない場合、詳細については [Power BI のガイド付き学習](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData) 参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート                             | コンテンツ                                               |
|-----------------------------------|--------------------------------------------------------|
| コンピテンシーと開発の分析 | チーム メンバーのスキル タイプとタイプ別のチーム メンバーのスキル |
| スキル プロファイル                     | 選択された従業員のスキル プロファイル                |
| スキル分析                    | タイプ別スキルおよび評価                              |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
アプリケーションのデータは、従業員のコンピテンシーと開発コンテンツ パックにレポートを入力するのに使用されます。 次の表に、コンテンツ パックが基づいているエンティティを示します。

| エンティティ                            | コンテンツ                                                                                                   | 他のエンティティとの関係 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Workforce\_CalendarOffset         | レポートをスライスするカレンダーのオフセット                                                                          | |
| Workforce\_Company                | レポートをフィルター処理する会社                                                                             | |
| Workforce\_Compensation           | 時間経過に伴う支払レートと頻度                                                                           | |
| Workforce\_CurrentCompensation    | 現在の日付時点の支払レートと頻度                                                              | Workforce\_Company、Workforce\_CurrentCompensation、Workforce\_Demographics、Workforce\_Job、Workforce\_Position |
| Workforce\_CurrentPosition        | 現在の日付時点での職位、フルタイム相当 (FTE)、空いている職位、欠員から採用済みになった職位 | Workforce\_Job Workforce\_Position |
| Workforce\_CurrentWorker          | 現在の日付時点での作業者、期日経過日数、人員                                                         | Workforce\_Company Workforce\_Compensation、Workforce\_GeographicLocation、Workforce\_Performance、Workforce\_PersonSkill、Workforce\_WorkerName、Workforce\_ReportsToWorkerName、Workforce\_WorkerTitle、Workforce\_Demographics、Workforce\_Job、Workforce\_Employment、Workforce\_Position |
| Workforce\_Date                   | 日、週、月、年                                                                             | |
| Workforce\_Demographics           | 生年月日、性別、出身民族、配偶者の有無                                                   | |
| Workforce\_Employment             | 開始日、終了日、移行日                                                                  | |
| Workforce\_GeographicLocation     | 市町村、市区郡、郵便番号、都道府県                                                           | |
| Workforce\_Job                    | 職務、タイプ、役職                                                                                  | |
| Workforce\_JobPreferredSkill      | 重要性、評価、スキル、スキル レベル                                                                 | Workforce\_Skill、Workforce\_Job |
| Workforce\_PastPositionAssignment | 割り当て理由、開始日、終了日、職務                                                           | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_Performance            | 評価、説明、評価モデル                                                                      | |
| Workforce\_PersonSkill            | レベル、取得日、スキル                                                                               | Workforce\_Skill |
| Workforce\_PersonSkillAnalysis    | 証明済、レベル、取得日、スキル                                                                    | Workforce\_WorkerName、Workforce\_Skill |
| Workforce\_Position               | 部門、FTE、職位、職位のタイプ、役職                                                        | |
| Workforce\_PositionTrend          | 時間経過に伴う職位、FTE、職務                                                                          | Workforce\_CalendarOffset, Workforce\_Date, Workforce\_Job, Workforce\_Position |
| Workforce\_ReportsToWorkerName    | 名、姓、フルネーム                                                                       | |
| Workforce\_Skill                  | スキル、スキル タイプおよび評価                                                                              | |
| Workforce\_TerminatedWorker       | 退職済作業者、退職日、役職、職位、職務                                             | Workforce\_Company、Workforce\_Compensation、Workforce\_GeographicLocation、Workforce\_Performance、Workforce\_WorkerName、Workforce\_ReportsToWorkerName、Workforce\_CalendarOffset、Workforces\_Date、Workforce\_WorkerTitle、Workforce\_Demographics、Workforce\_Employment、Workforce\_Job、Workforce\_Position |
| Workforce\_WorkerName             | 名、姓、フルネーム                                                                       | |
| Workforce\_WorkerTitle            | 役職と勤続日数                                                                                   | |
| Workorce\_WorkerTrend             | 時間経過に伴う作業者、人員、会社、職位                                                        | Workforce\_Company、Workforce\_Compensation、Workforce\_GeographicLocation、Workforce\_Performance、Workforce\_WorkerName、Workforce\_ReportsToWorkerName、Workforce\_CalendarOffset、Workforces\_Date、Workforce\_WorkerTitle、Workforce\_Demographics、Workforce\_Employment、Workforce\_Job |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

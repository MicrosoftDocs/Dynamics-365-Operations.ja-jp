---
title: 組織トレーニング Power BI の内容
description: この記事では、財務と運用 - 組織トレーニング Power BI コンテンツについて説明します。
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
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.openlocfilehash: 2e80810dbeb536dccf6e13b5fca6a85f4858d8da
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267245"
---
# <a name="organizational-training-power-bi-content"></a>組織トレーニング Power BI の内容

[!include [banner](../includes/banner.md)]

この記事では、財務と運用 - 組織トレーニング Power BI コンテンツについて説明します。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
コンテンツ パックをデータに接続した後に、レポートに組織のデータが表示されます。 以前に Microsoft Power BI を使用したことがない場合、詳細については [Power BI のガイド付き学習](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData) 参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート           | コンテンツ                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| コースの分析 | 場所による登録、コース参加者のステータス、および登録リスト |
| コースのタイプ    | スキル別コース タイプ                                                       |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
アプリケーション データは、組織トレーニング コンテンツ パックにレポートを入力するのに使用されます。 次の表に、コンテンツ パックが基づいているエンティティを示します。

| エンティティ                    | コンテンツ                                                         | 他のエンティティとの関係 |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Training\_CalendarOffset  | レポートをスライスするカレンダーのオフセット                                | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_Company         | レポートをフィルター処理する会社                                   | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_Course          | コース、説明、講師名、場所、部屋、およびステータス | Training\_CourseAgenda、Training\_CourseAttendees、Training\_CourseSkill |
| Training\_CourseAgenda    | 議題、コース、および開始時間と終了時間                          | Training\_Company、Training\_CalendarOffset、Training\_Date、Training\_Course |
| Training\_CourseAttendees | 名前、ステータス、ジョブ、および登録日付                         | Training\_Company、Training\_CalendarOffset、Training\_Date、Training\_Demographics、Training\_Employment、Training\_Course、 Training\_WorkerName、raining\_WorkerTitle、Training\_Job、Training\_Position |
| Training\_CourseSkill     | スキル、スキル タイプ、およびレベル                                     | Training\_Course |
| Training\_Date            | 日、週、月、年                                   | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_Demographics    | 生年月日、性別、出身民族、配偶者の有無         | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_Employment      | 開始日、終了日、移行日                        | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_Job             | 職務、タイプ、役職                                        | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_Position        | 職位、タイトル、およびフルタイム相当額 (FTE)                  | Training\_CourseAgenda、Training\_CourseAttendees |
| Training\_WorkerName      | 名、姓、フルネーム                             | Training\_CourseAttendees |
| Training\_WorkerTitle     | 役職と勤続日数                                         | Training\_CourseAttendees |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

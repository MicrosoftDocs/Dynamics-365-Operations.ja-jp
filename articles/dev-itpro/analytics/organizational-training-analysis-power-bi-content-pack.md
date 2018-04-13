---
title: "組織トレーニング Power BI コンテンツ"
description: "このトピックでは、Finance and Operations - 組織トレーニング Power BI コンテンツについて説明します。"
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 18567a3241fce02e17df368f544e545fad93e1d9
ms.contentlocale: ja-jp
ms.lasthandoff: 03/23/2018

---

# <a name="organizational-training-power-bi-content"></a>組織トレーニング Power BI コンテンツ

[!INCLUDE [banner](../includes/banner.md)]

このトピックでは、Finance and Operations - 組織トレーニング Power BI コンテンツについて説明します。 

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
コンテンツ パックを Finance and Operations データに接続した後に、レポートには組織のデータが表示されます。 Microsoft Power BI を以前に使用したことがない場合は、詳細については「[Power BI のガイド付きの学習](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)」を参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート           | コンテンツ                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| コースの分析 | 場所による登録、コース参加者のステータス、および登録リスト |
| コースのタイプ    | スキル別コース タイプ                                                       |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)」を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
Finance and Operations のデータは、組織トレーニング コンテンツ パックにレポートを入力するのに使用されます。 次の表に、コンテンツ パックが基づいているエンティティを示します。

| エンティティ                    | コンテンツ                                                         | 他のエンティティとの関係                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Training\_CalendarOffset  | レポートをスライスするカレンダーのオフセット                                | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Company         | レポートをフィルター処理する会社                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Course          | コース、説明、講師名、場所、部屋、およびステータス | Training\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Training\_CourseAgenda    | 議題、コース、および開始時間と終了時間                          | Training\_Company Training\_CalendarOffset Training\_Date Training\_Course                                                                                                                         |
| Training\_CourseAttendees | 名前、ステータス、ジョブ、および登録日付                         | Training\_Company Training\_CalendarOffset Training\_Date Training\_Demographics Training\_Employment Training\_Course Training\_WorkerName Training\_WorkerTitle Training\_Job Training\_Position |
| Training\_CourseSkill     | スキル、スキル タイプ、およびレベル                                     | Training\_Course                                                                                                                                                                                   |
| Training\_Date            | 日、週、月、年                                   | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Demographics    | 生年月日、性別、出身民族、配偶者の有無         | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Employment      | 開始日、終了日、移行日                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Job             | 職務、タイプ、役職                                        | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_Position        | 職位、タイトル、およびフルタイム相当額 (FTE)                  | Training\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Training\_WorkerName      | 名、姓、フルネーム                             | Training\_CourseAttendees                                                                                                                                                                          |
| Training\_WorkerTitle     | 役職と勤続日数                                         | Training\_CourseAttendees                                                                                                                                                                          |






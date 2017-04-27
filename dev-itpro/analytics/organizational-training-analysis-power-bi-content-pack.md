---
title: "Organizational Training Power BI コンテンツ"
description: "このトピックでは、Dynamics 365 for Operations - Organizational Training Power BI コンテンツについて説明します。 コンテンツ パックにアクセスする方法、およびコンテンツ パックを構築するために使用されたデータ モデルとエンティティについて説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organizational Training Power BI コンテンツ

[!include[banner](../includes/banner.md)]


このトピックでは、Dynamics 365 for Operations - Organizational Training Power BI コンテンツについて説明します。 コンテンツ パックにアクセスする方法、およびコンテンツ パックを構築するために使用されたデータ モデルとエンティティについて説明します。

<a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
--------------------------

Organizational Training コンテンツ パックは、Microsoft Dynamics Lifecycle Services (LCS) の共有資産ライブラリにあります。 コンテンツ パックのダウンロード方法および Microsoft Dynamics 365 for Operations データに接続する方法の詳細については、「[Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md)」を参照してください。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
内容パックを Dynamics 365 for Operations データに接続した後に、レポートには組織のデータが表示されます。 Microsoft Power BI を以前に使用したことがない場合は、詳細については「[Guided Learning page for Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)」を参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート           | コンテンツ                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| コースの分析 | 場所による登録、コース参加者のステータス、および登録リスト |
| コースのタイプ    | スキル別コース タイプ                                                       |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[Create and Configure A Dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)」を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
Dynamics 365 for Operations データを使用して、Organizational Training コンテンツ パックにレポートを入力します。 次の表に、コンテンツ パックが基づいているエンティティを示します。

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

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 これらの計算メジャーは、主要業績評価指標 (KPI) およびコンテンツ パックで使用するためのレポートを計算するために使用されます。 レポートおよびダッシュボードに追加の計算を含める場合は、LCS から Training.pbix ファイルをダウンロードして変更することができます。 このファイルはコンテンツ パックを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)






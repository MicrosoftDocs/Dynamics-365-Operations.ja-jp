---
title: "Recruiting Power BI コンテンツの採用"
description: "このトピックでは Dynamics 365 for Operations - Recruiting Power BI コンテンツについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 15780e7db5867a2f6a484ceb663e617345c033c2
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="recruiting-power-bi-content"></a>Recruiting Power BI コンテンツの採用

[!include[banner](../includes/banner.md)]


このトピックでは Dynamics 365 for Operations - Recruiting Power BI コンテンツについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

<a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
--------------------------

Recruiting コンテンツ パックは、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリにあります。 コンテンツ パックのダウンロード方法および Microsoft Dynamics 365 for Operations データに接続する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
コンテンツ パックを Dynamics 365 for Operations データに接続した後に、レポートに組織のデータが表示されます。 Microsoft Power BI を以前に使用したことがない場合は、詳細については「[Power BI のガイド付きの学習](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)」を参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート                        | コンテンツ                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| 申請者の分析           | ジョブ別申請者、申請者ソース、場所別申請者、および申請者の合計数           |
| 申請者のステータス             | タイプおよびステータス別申請者および申請者のステータス                                                    |
| 申請者の人口統計       | 年齢と性別別申請者、教育レベルとステータス別申請者                             |
| 採用分析          | 正味雇用率、平均雇用日数、悪い雇用者の割合、採用にかかる費用                    |
| 採用プロジェクト分析 | 採用プロジェクト数、採用プロジェクトによる空き状況、採用プロジェクトによる申請者数 |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)」を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
Dynamics 365 for Operations のデータを使用して、採用コンテンツ パックに情報を入力します。 次の表に、コンテンツ パックが基づいているエンティティを示します。

| エンティティ                          | コンテンツ                                                         | 他のエンティティとの関係                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Recruiting\_Applicant           | 応募者、雇用申請者、正味雇用率、および費用          | Recruiting\_ApplicantName Recruiting\_Company Recruiting\_CalendarOffset Recuriting\_Date Recruiting\_GeographicLocation Recruiting\_Demographics Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject                                |
| Recruiting\_ApplicantName       | 申請者の名、姓、フルネーム                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_CalendarOffset      | レポートをスライスするカレンダーのオフセット                                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Company             | レポートをフィルター処理する会社                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Date                | 日、週、月、年                                   | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Demographics        | 生年月日、性別、出身民族、配偶者の有無         | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_EmployedApplicant   | 申請者、パフォーマンス、開始日、および申請者のタイプ           | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_ApplicantName Recruiting\_Employment Recruiting\_Performance Recruiting\_Job Recruiting\_Media Recruiting\_RecruitmentProject          |
| Recruiting\_Employment          | 開始日、終了日、移行日                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_GeographicLocation  | 市町村、市区郡、郵便番号、都道府県                 | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Job                 | 職務、タイプ、役職                                        | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Media               | 申請者のソース                                             | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_Performance         | 評価、説明、評価モデル                            | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_RecruitmentProject  | プロジェクト説明、プロジェクト ステータス、空き状況                | Recruiting\_Applicant Recruiting\_EmployedApplicant Recruiting\_TerminatedApplicant                                                                                                                                                               |
| Recruiting\_TerminatedApplicant | 退職済申請者、理由、パフォーマンス、終了日 | Recruiting\_Company Recruiting\_CalendarOffset Recruiting\_Date Recruiting\_GeographicLocation Recruiting\_Performance Recruiting\_Demographics Recruiting\_Employment Recruiting\_Media Recruiting\_RecruitmentProject Recruiting\_ApplicantName |

これらのエンティティは、計算メジャーを作成するために使用されました。 これらの計算メジャーは、主要業績評価指標 (KPI) およびコンテンツ パックで使用するためのレポートを計算するために使用されます。 レポートおよびダッシュボードに追加の計算を含める場合は、LCS から Recruiting.pbix ファイルをダウンロードして変更することができます。 このファイルはコンテンツ パックを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)






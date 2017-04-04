---
title: "Power BI採用の内容"
description: "このトピックでは、]Power BI採用の内容365 for Operationsについて説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。"
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d307733193b388149f83dd420cc7003edcf7749a
ms.lasthandoff: 03/31/2017


---

# <a name="recruiting-power-bi-content"></a>Power BI採用の内容

このトピックでは、]Power BI採用の内容365 for Operationsについて説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。

<a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
--------------------------

Microsoft Dynamics Lifecycle Services (LCS)の共有資産のライブラリの採用のコンテンツ パックを検索できます。 コンテンツ パックをダウンロードし、データのMicrosoft Dynamics 365に接続する方法の詳細については、" "を参照してください]、[Microsoftパートナー (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
工程365 for OperationsデータにコンテンツPack接続されたら、レポートは、組織のデータが表示されます。 は、Microsoft Power BIの前に使用していない場合は、そのコンフィギュレーションに関する情報を入手ことができます。[導かれるPower BI説明します] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)のページを。 コンテンツ パックに含まれるレポートに追加情報を含むテーブルの両方とグラフがあります。 次の表にレポートを示します。

| レポート                        | コンテンツ                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| 申請者の分析           | 場所によってジョブ、申請者ソース、申請者、および申請者の合計数による申請者           |
| 申請者のステータス             | タイプおよびステータスに応じて申請者、および申請者のステータス                                                    |
| 申請者の人口統計       | 期間と性別別の申請者、および教育のレベルおよびステータスに応じて申請者                             |
| 採用の分析          | 従業員への正味雇用率、平均日目、採用率、採用の原価                    |
| 採用プロジェクトの分析 | 採用プロジェクト別採用プロジェクト、開始、採用プロジェクト別の申請者の数 |

これらのレポートのグラフとタイルをフィルタ処理しダッシュボードにとグラフをタイルでそのPIN。 Power BIにフィルタPINでな方法の詳細について表示する[ダッシュボード作成してコンフィギュレーション] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)を。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
工程365 for Operationsデータが採用のコンテンツPackレポートの情報も使用されます。 次の表に、コンテンツ パックが基づいているエンティティに示します。

| エンティティ                          | コンテンツ                                                         | 他のエンティティとの関係                                                                                                                                                                                                                 |
|---------------------------------|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_採用の申請者           | 申請者、雇用申請者は、雇用の率と原価          | \_CalendarOffset Recuriting\_する\_会社を採用する採用の\_ApplicantNameは\_RecruitmentProjectを採用する\_メディアを採用する\_ジョブを採用する\_人口統計を採用する採用の\_GeographicLocationの日付を入力します。                                |
| 採用の\_ApplicantName       | 申請者名]ボックスに、完全名                   | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| 採用の\_CalendarOffset      | スライス レポートへのカレンダーの相殺                                | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| \_採用の会社             | レポートをフィルタ処理する会社                                   | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| \_採用の日付                | 日、週、月、年                                   | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| \_採用の人口統計        | 、性別、種族的出身と配偶者の有無誕生日         | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| 採用の\_EmployedApplicant   | 申請者、パフォーマンス、開始日、および申請者のタイプ           | \_RecruitmentProjectを採用する\_メディアを採用する\_ジョブを採用する\_パフォーマンスを採用する\_を採用する\_ApplicantNameを採用する\_GeographicLocationを採用する\_日付を採用する\_CalendarOffsetを採用する\_採用の会社          |
| \_採用の雇用          | 開始日、終了日、および遷移の日付                        | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| 採用の\_GeographicLocation  | 市町村、郵便番号、市区郡、都道府県または地域                 | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| \_採用のジョブ                 | 職務、および職位タイプ                                        | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| \_採用のメディア               | 申請者のソース                                             | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| \_採用のパフォーマンス         | 評価、説明、および評価モデル                            | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| 採用の\_RecruitmentProject  | プロジェクト説明、プロジェクト ステータス、開始                | \_TerminatedApplicantを採用する\_EmployedApplicantを採用する\_採用の申請者                                                                                                                                                               |
| 採用の\_TerminatedApplicant | 完成した申請者、理由、パフォーマンス、終了日 | \_ApplicantNameを採用する\_RecruitmentProjectを採用する\_メディアを採用する\_を採用する\_人口統計を採用する\_パフォーマンスを採用する\_GeographicLocationを採用する\_日付を採用する\_CalendarOffsetを採用する\_採用の会社 |

これらのエンティティがと計算メジャーを作成するのに使用されます。 これらの計算メジャーは、コンテンツ パックで使用されるレポートおよび主要業績評価指標(KPIs)を計算するために使用します。 レポートおよびダッシュボードの追加の計算を含める場合は、LCSからのRecruiting.pbixファイルのダウンロードを変更できます。 このファイルはコンテンツ パックを作成するのに使用される既定のデータ モデルです。 変更をすると、追加した情報を含むダッシュボードと組織のコンテンツ パックを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)




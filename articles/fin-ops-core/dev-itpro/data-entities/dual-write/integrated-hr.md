---
title: 統合された作業者、職務、職位
description: このトピックでは、Microsoft Dynamics 365 アプリの統合された作業者データに関する情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8192f6d0b40204ca09a937509006725b4b6c226f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683515"
---
# <a name="integrated-worker-job-and-position"></a>統合された作業者、職務、職位

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



作業者データは、複数の Microsoft Dynamics 365 アプリでマスターできます。 たとえば、人事管理 (HR) データは、Dynamics 365 Human Resources、Dynamics 365 Commerce、Dynamics 365 Supply Chain Management で管理できます。 データの出所に関係なく、バックグラウンドで統合されます。 作業者に関するデータを統合する機能により、あらゆる Dynamics 365 アプリで作業者データを柔軟にマスターできます。 また、Dynamics 365 アプリの情報を包括的に把握することもできます。

## <a name="human-resources"></a>人事管理

HR データの統合には、Dynamics 365 の Finance and Operations アプリとモデル駆動型アプリ間での HR データのマッピングが含まれます。

## <a name="templates"></a>テンプレート

HR データには、従業員と契約社員、職位、職務に関する情報が含まれます。 次の表に示すように、テーブル マップのコレクションは、データ操作中に連携して動作します。

| Finance and Operations アプリ | Dynamics 365 モデル駆動型アプリ | 説明 |
|-----------------------------|----------------------------------|-------------|
| 報酬ジョブ機能 | cdm\_jobfunctions | |
| 報酬ジョブ タイプ | cdm\_jobtypes | |
| 雇用 | cdm\_employments | |
| 雇用の詳細 | cdm\_employments | |
| 職務 | cdm\_jobs | |
| ジョブの詳細 | cdm\_jobs | |
| 職位の詳細 | cdm\_jobpositions | |
| 職位の期間 | cdm\_jobpositions | |
| 職位階層 | cdm\_jobpositions | |
| 職位タイプ | cdm\_positiontypes | |
| 職位作業者割り当て | cdm\_positionworkerassignmentmaps | |
| ワーカー | cdm\_workers | Dynamics 365 Finance と Supply Chain Management では、作業者は従業員または契約社員のいずれかに分類されます。 Dataverse では、作業者をボランティアとして分類することもできます。 データが Finance と Supply Chain Management に変換されると、ボランティアは契約社員になります。 |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [job function](includes/JobFunction-cdm-jobfunctions.md)]

[!include [job type](includes/JobType-cdm-jobtypes.md)]

[!include [employment](includes/Employment-cdm-employments.md)]

[!include [employment detail](includes/EmploymentDetail-cdm-employments.md)]

[!include [job](includes/Job-cdm-jobs.md)]

[!include [job detail](includes/JobDetail-cdm-jobs.md)]

[!include [position detail](includes/PositionDetail-cdm-jobpositions.md)]

[!include [position duration](includes/PositionDuration-cdm-jobpositions.md)]

[!include [position hierarchy](includes/PositionHierarchy-cdm-jobpositions.md)]

[!include [position type](includes/PositionType-cdm-positiontypes.md)]

[!include [position worker assignment](includes/PositionWorkerAssignment-cdm-positionworkerassignmentmaps.md)]

[!include [worker](includes/Worker-cdm-workers.md)]

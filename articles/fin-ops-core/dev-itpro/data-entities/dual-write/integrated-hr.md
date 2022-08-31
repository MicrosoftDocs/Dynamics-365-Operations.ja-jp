---
title: 作業者、職務、および職位の統合
description: この記事では、Microsoft Dynamics 365 アプリの統合された作業者データに関する情報を提供します。
author: RamaKrishnamoorthy
ms.date: 01/08/2020
ms.topic: article
audience: Developer
ms.reviewer: sericks
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c217702d7203095e32bd6e19d9aa1bd049da0dc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289226"
---
# <a name="integrated-worker-job-and-position"></a>作業者、職務、および職位の統合

[!include [banner](../../includes/banner.md)]



1 つのアプリでのみマスターされている間は、作業者データは複数の Dynamics 365 アプリ間で同期できます。 たとえば、人事管理 (HR) データは Dynamics 365 Human Resources でマスターし、Dynamics 365 Commerce、Dynamics 365 Finance、および Dynamics 365 Supply Chain Management と同期することができます。 データは、バックグラウンドでシームレスに統合されます。 作業者に関するデータを統合する機能により、すべての Dynamics 365 アプリで同じデータを操作して、情報を包括的に把握することができます。

## <a name="human-resources"></a>Human Resources

HR データの統合には、財務と運用アプリと Customer Engagement アプリ間での HR データのマッピングが含まれます。

## <a name="templates"></a>テンプレート

HR データには、従業員と契約社員、職位、職務に関する情報が含まれます。 次の表に示すように、テーブル マップのコレクションは、データ操作中に連携して動作します。

財務と運用アプリ | Customer Engagement アプリ     | 説明
|-----------------------------|----------------------------------|-------------|
[報酬ジョブ機能](mapping-reference.md#105) | cdm_jobfunctions | |
[報酬ジョブ タイプ](mapping-reference.md#108) | cdm_jobtypes | |
[雇用職務権限](mapping-reference.md#225) | msdyn_employmentjobfunctions | |
[会社ごとの雇用](mapping-reference.md#104) | cdm_employments | |
[職務](mapping-reference.md#107) | cdm_jobs | |
[職位 V2](mapping-reference.md#106) | cdm_jobpositions | |
[職位タイプ](mapping-reference.md#110) | cdm_positiontypes | |
[職位作業者割り当て](mapping-reference.md#111) | cdm_positionworkerassignmentmaps | |
[ワーカー](mapping-reference.md#113) | cdm_workers | Dynamics 365 Finance および Supply Chain Management では、作業者は従業員または契約社員のいずれかに分類されます。 Dataverse では、作業者をボランティアとして分類することもできます。 データが Finance と Supply Chain Management に変換されると、ボランティアは契約社員になります。 |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

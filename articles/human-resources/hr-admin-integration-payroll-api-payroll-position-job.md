---
title: 給与職位職務
description: このトピックでは、Dynamics 365 Human Resources における給与職位職務エンティティに対するクエリの詳細および例を示します。
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9444a36f5ddf92bd41008c83ec77ab7ff5191fa3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019349"
---
# <a name="payroll-position-job"></a>給与職位職務

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources における給与職位職務リレーションシップに対するクエリの詳細および例を示します。

## <a name="properties"></a>プロパティ

| プロパティ<br>**現物名**<br>**_種類_** | 使用 | 説明 |
| --- | --- | --- |
| **ジョブ ID**<br>mshr_jobid<br>*文字列* | 読み取り専用<br>必須 |ジョブの ID。 |
| **発効日**<br>mshr_validto<br>*日時オフセット* | 読み取り専用 <br>必須 | 転記とジョブの関係が有効である日付。 |
| **失効日**<br>mshr_validto<br>*日時オフセット* | 読み取り専用 <br>必須 | 職位とジョブの関係が有効である日付。  |
| **職位 ID**<br>mshr_positionid<br>*文字列* | 読み取り専用<br>必須 | 職位の ID。 |
| **基本フィールド**<br>mshr_primaryfield<br>*文字列* | 必須<br>システム生成 |  |
| **職位職務 ID の値**<br>_mshr_fk_positionjob_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollpositionjobentity の mshr_PayrollPositionJobEntity |この職位に関連付けられているジョブの ID です。|
| **固定報酬の報酬計画 ID 値**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | 読み取り専用<br>必須<br>外部キー: mshr_payrollfixedcompensationplanentity の mshr_FixedCompPlan_id  | この職位に関連付けられている固定報酬計画の ID です。 |
| **給与職位職務エンティティ ID**<br>mshr_payrollpositionjobentityid<br>*Guid* | 必須<br>システム生成。 | システムで生成する、ジョブを一意に識別する GUID 値です。  |


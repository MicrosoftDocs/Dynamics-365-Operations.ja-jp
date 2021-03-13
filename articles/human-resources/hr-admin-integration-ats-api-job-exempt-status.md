---
title: ジョブ除外する状態
description: このトピックでは、Dynamics 365 Human Resources におけるジョブ除外状態のオプション セットについて説明します。
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0cd6ffc01793c8ff12e36175c7c9feaf8a4b3cdf
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125572"
---
# <a name="job-exempt-status"></a>ジョブ除外する状態

このトピックでは、Dynamics 365 Human Resources におけるジョブ除外状態のオプション セットについて説明します。

物理名 : cdm_jobexemptstatus

このリストでは、FLSA ジョブ除外状態の値のオプションセットを指定します。 これは、既存の cdm_jobexemptstatus オプション セットで提供されます。

| 先頭値 | ラベル | 説明 |
| --- | --- | --- |
| 200000000 | 控除 | ジョブは、FLSA ガイドラインに基づく除外の状態です。 |
| 200000001 | NonExempt | ジョブは、FLSA ガイドラインに基づく非除外の状態です。 |
| 200000002 | 適用しない | FLSA の状態のガイドラインはジョブには適用されません。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)

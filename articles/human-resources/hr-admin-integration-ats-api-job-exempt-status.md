---
title: ジョブ除外する状態
description: このトピックでは、Dynamics 365 Human Resources におけるジョブ除外状態のオプション セットについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 29d3c4fd37a219b520172c6866c5fec488c698f7
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8064994"
---
# <a name="job-exempt-status"></a>ジョブ除外する状態


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: ジョブ除外する状態
description: このトピックでは、Dynamics 365 Human Resources におけるジョブ除外状態のオプション セットについて説明します。
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798300"
---
# <a name="job-exempt-status"></a>ジョブ除外する状態

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
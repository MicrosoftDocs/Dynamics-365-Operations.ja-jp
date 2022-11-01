---
title: 申請者の統合結果
description: この記事では、Dynamics 365 Human Resources の申請者統合結果オプションについて説明します。
author: jaredha
ms.date: 09/12/2022
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
ms.openlocfilehash: 86f3f75e538268644cea4f927f04c07aae115f00
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702231"
---
# <a name="applicant-integration-result"></a>申請者の統合結果


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の申請者統合結果オプションについて説明します。

物理名 : mshr_hcmapplicantintegrationresult

このリストは、候補者レコードの状態を表わします。

| 先頭値 | ラベル | 説明 |
| --- | --- | --- |
| 200000000 | 処理されません | 候補者がまだ検討中です。 |
| 200000001 | 雇用 | 候補者が採用されました。 |
| 200000002 | 未採用 | 候補者を採用しない決定が下されました。 |
| 200000003 | 解除済み | 候補者は検討から外されました。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

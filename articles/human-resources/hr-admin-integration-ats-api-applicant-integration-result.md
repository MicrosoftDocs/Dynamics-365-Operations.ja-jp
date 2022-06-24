---
title: 申請者の統合結果
description: この記事では、Dynamics 365 Human Resources の申請者統合結果オプションについて説明します。
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
ms.openlocfilehash: 84f0ba9b197866935535a68006cfdb8c18fa3ad1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902317"
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

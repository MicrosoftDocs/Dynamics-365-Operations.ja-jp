---
title: 採用で要求する職位の状態
description: この記事では、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。
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
ms.openlocfilehash: 736bdbfb8759ab61202d1f17e3cdc8294be0ba84
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846417"
---
# <a name="recruiting-request-position-status"></a>採用で要求する職位の状態


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。

物理名 : mshr_hcmrecruitingrequestpositionstatus

このリストでは、 RecruitingRequestPosition エンティティ内の採用で要求する職位の状態に対するオプション セットを提供します。

| 先頭値 | ラベル | 説明 |
| --- | --- | --- |
| 200000000 | 空いている | 募集中となっている職位です。 これは、現在アクティブな職位の割り当てがないことを示すものではありません。 採用時に職位に従業員が存在する場合があります。 これは、職位が採用要求のコンテキストにおいて採用に利用できる状態のみを示します。 |
| 200000001 | 採用済み | 職位への割り当てに従業員が選択されています。 |
| 200000002 | 取消済 | この職位に対する採用の要求はキャンセルされました。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

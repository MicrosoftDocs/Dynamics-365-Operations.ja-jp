---
title: 採用で要求する職位の状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。
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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464721"
---
# <a name="recruiting-request-position-status"></a>採用で要求する職位の状態

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources の採用で要求する職位の状態のオプションセットについて説明します。

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
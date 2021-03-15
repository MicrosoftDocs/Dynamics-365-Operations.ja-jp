---
title: 採用で要求する状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。
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
ms.openlocfilehash: 55ed9c391a1b5f86c3c443b9fceeee5c2301444d
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125957"
---
# <a name="recruiting-request-status"></a>採用で要求する状態

このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。

物理名 : mshr_hcmrecruitingrequeststatus

このリストは、RecruitingRequest に対して、状態値のオプション セットを提供します。

| 先頭値 | ラベル | 説明 |
| --- | --- | --- |
| 200000000 | ドラフト | 要求が下書きの状態となっているため、アクティブな採用を行うことができません。 |
| 200000001 | 確認中 | 要求がすでに送信されており、ワークフローによる承認を受け付中です。 ワークフローが有効になっている場合にのみ使用できます。 |
| 200000002 | 保留中 | 要求が保留中のワークフロー アクションです。 ワークフローが有効になっている場合にのみ使用できます。 |
| 200000003 | 取消済 | 要求がキャンセルされました。 ワークフローが有効になっている場合にのみ使用できます。 |
| 200000004 | 拒否済 | 要求が否認されました。 ワークフローが有効になっている場合にのみ使用できます。 |
| 200000005 | 使用可能 | ワークフローが完了して承認されると、その要求に対して有効な採用を行う準備が整います。 |
| 200000006 | 終了済 | 採用要求が完了しました。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用要求のクエリの例](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
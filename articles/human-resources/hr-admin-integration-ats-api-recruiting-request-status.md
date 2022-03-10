---
title: 採用で要求する状態
description: このトピックでは、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。
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
ms.openlocfilehash: d845179077fc2e04dfb3bd05eaa70b0a2a016121
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067104"
---
# <a name="recruiting-request-status"></a>採用で要求する状態


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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

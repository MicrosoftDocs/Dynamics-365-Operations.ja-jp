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
ms.openlocfilehash: 91360b07915ba10472768ac32b473e6daf7163fa8aed24e6aabaaa91f0ec7154
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723674"
---
# <a name="recruiting-request-status"></a>採用で要求する状態

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
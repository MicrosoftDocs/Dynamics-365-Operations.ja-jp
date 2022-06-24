---
title: 採用で要求する状態
description: この記事では、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。
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
ms.openlocfilehash: 6a8cb8bc61786425c996b976a2914e7b650e3941
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859607"
---
# <a name="recruiting-request-status"></a>採用で要求する状態


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Dynamics 365 Human Resources の採用で要求する状態のオプションセットについて説明します。

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

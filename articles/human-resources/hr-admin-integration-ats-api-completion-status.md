---
title: 完了の状態
description: このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。
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
ms.openlocfilehash: da91084d30873b79033d789beab829da9fbdb010
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065549"
---
# <a name="completion-status"></a>完了の状態


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。

物理名 : mshr_hcmcompletionstatus

このリストは、候補者の審査に対して、状態値のオプション セットを提供します。 

| 先頭値 | ラベル | 説明 |
| --- | --- | --- |
| 200000000 | 未完了 | 候補者の審査がまだ完了していません。 |
| 200000001 | 成功 | 候補者が審査に合格しました。 |
| 200000002 | 不合格 | 候補者が審査に不合格となりました。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

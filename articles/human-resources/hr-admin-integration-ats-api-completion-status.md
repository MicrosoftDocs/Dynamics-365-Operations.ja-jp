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
ms.openlocfilehash: 54ad5cc8f5f18d57b6713304cceb985acfdc93d1
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055367"
---
# <a name="completion-status"></a>完了の状態

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
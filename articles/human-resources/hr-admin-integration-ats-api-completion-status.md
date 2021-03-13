---
title: 完了の状態
description: このトピックでは、Dynamics 365 Human Resources における完了の状態のオプションについて説明します。
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
ms.openlocfilehash: e9024e00b5d25117fd255084609c4f8db9284f32
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125692"
---
# <a name="completion-status"></a>完了の状態

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

---
title: 審査頻度の生成方法
description: このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。
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
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126149"
---
# <a name="screening-frequency-generate-from"></a>審査頻度の生成方法

このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。

物理名 : mshr_hcmfrequencygeneratefrom

このリストでは、次に必要な審査の計算開始日を決定するため値のオプションセットを提供します。

| 先頭値 | ラベル | 説明 |
| --- | --- | --- |
| 200000000 未選択 | 値が選択されていません。 |
| 200000001 完了日 | 最終審査の完了日からの計算となります。 |
| 200000002 必要な日付 | 要求された審査の最終日から計算します。 |

## <a name="see-also"></a>参照

[申請者追跡システム統合APIの概要](hr-admin-integration-ats-api-introduction.md)<br>
[採用する採用候補者に対するクエリの例](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
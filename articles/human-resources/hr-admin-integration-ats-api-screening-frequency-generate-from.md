---
title: 審査頻度の生成方法
description: このトピックでは、Dynamics 365 Human Resources における審査頻度の生成方法のオプション セットについて説明します。
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
ms.openlocfilehash: ae5ad3e556f40cedd385d8aadded9ef76447a98b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054095"
---
# <a name="screening-frequency-generate-from"></a>審査頻度の生成方法

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

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
---
title: Power Apps 管理センターで環境を作成できない
description: この記事では、管理者が Microsoft Power Apps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cc62d3c8fe560d4f7d2e754a79de6fec3ef6041b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882927"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps 管理センターで環境を作成できない


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**問題点**

- テナント/環境の管理者が Microsoft Power Apps 管理者センターで環境を作成することができません。
- ユーザーは、環境を作る権限を付与するライセンスを持っていません。

**ソリューション**

テナント管理者が、環境を作成するユーザーに有効な Power Apps P2 ライセンスを割り当てている必要があります。 次の Microsoft Dynamics サービス 計画では、環境を作成するアクセス許可が提供されます。

| 全体の製品の最小管理単位 (SKU)       | Power Apps P2 サービス計画  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | Power Apps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | Power Apps for Dynamics 365 |

さまざまな Microsoft Office SKU も、スタンドアロンの Power Apps プラン 2 SKU と一緒にこの権利を提供することに注意してください。 重要な点は、これらの SKU のいずれかが必要であることです。

1. [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) に移動します。
2. 次の手順に従って、環境を作成します [人事管理のプロビジョニング](/dynamics365/unified-operations/talent/provisioning-talent)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

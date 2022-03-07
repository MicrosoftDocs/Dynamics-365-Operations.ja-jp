---
title: Power Apps 管理センターで環境を作成できない
description: この記事では、管理者が Microsoft Power Apps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 664c644c9b34e3489b4134040e165d26202dbd38
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113261"
---
# <a name="cant-create-an-environment-in-the-power-apps-admin-center"></a>Power Apps 管理センターで環境を作成できない

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
2. 次の手順に従って、環境を作成します [人事管理のプロビジョニング](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent)。

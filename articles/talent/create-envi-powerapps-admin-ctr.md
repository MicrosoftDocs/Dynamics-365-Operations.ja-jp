---
title: PowerApps 管理者センターで環境を作成することができない
description: このトピックでは、管理者が Microsoft PowerApps 管理者センターで環境を作成することができない場合の対処方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 97d44dc034cb8097fc0ecf9ac4e485425f097102
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "857249"
---
# <a name="cant-create-an-environment-in-the-powerapps-admin-center"></a>PowerApps 管理センターで環境を作成できない

[!include [banner](includes/banner.md)]

**払出**

- テナント/環境の管理者が Microsoft PowerApps 管理者センターで環境を作成することができません。
- 環境の作成手順を実行する権限をユーザーに提供するライセンスは、その手順を実行しているユーザーに直接割り当てられていません。

**ソリューション**

テナント管理者が、環境の作成手順を実行するユーザーに、有効な PowerApps P2 ライセンスを直接割り当てていることを確認します。 その権限を提供する Microsoft Dynamics サービス プランは次のとおりです。

| 全体の最小在庫管理単位 (SKU)       | PowerApps P2 サービス計画  |
|------------------------------------------------|----------------------------|
| Microsoft Dynamics 365 for Operations          | PowerApps for Dynamics 365 |
| Microsoft Dynamics 365 Plan Enterprise Edition | PowerApps for Dynamics 365 |

さまざまな Microsoft Office SKU も、スタンドアロンの PowerApps プラン 2 SKU と一緒にこの権利を提供することに注意してください。 重要な点は、これらの SKU のいずれかが必要であることです。

1. [https://preview.admin.powerapps.com/environments](https://preview.admin.powerapps.com/environments) に移動します。
2. 次の手順に従って、環境を作成します [Talent のプロビジョニング](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent)。

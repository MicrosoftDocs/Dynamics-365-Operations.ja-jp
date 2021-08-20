---
title: サービスのための社内資産
description: このトピックでは、Microsoft Dynamics 365 Field Service を使用して顧客資産と社内資産の両方にサービスを提供する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0700025288bda1b2c67cc3ff26dc2e737216a5f8f5265464c6c62d9cb890b580
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742313"
---
# <a name="in-house-assets-for-servicing"></a>サービスのための社内資産

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Field Service は、顧客資産をサービスするように設計されています。 Dynamics 365 Supply Chain Management の資産管理は、社内資産を維持するように設計されています。 この 2 つのアプリを統合すると、Field Service を使用して顧客資産と社内資産の両方にサービスを提供できます。 また、機能の場所または階層に基づいて資産を分類し、詳細レベルでサービスを追跡することもできます。

詳細については、[Dynamics 365 Field Service と Supply Chain Management の統合](/dynamics365/field-service/supply-chain-field-service-integration) を参照してください。

## <a name="templates"></a>テンプレート

社内資産には、次のテーブルに示すように、データの相互作用中に連携して作業するコア テーブル マップのコレクションが含まれます。

| Finance and Operations アプリ | Customer Engagement アプリ | 説明 |
|-----------------------------|-----------------------------------|-------------|
[資産管理資産のライフサイクル モデル](mapping-reference.md#119) | msdyn_assetlifecyclemodels | |
[資産管理資産のライフサイクル状態](mapping-reference.md#120) | msdyn_assetlifecyclestates | |
[資産管理資産のタイプ](mapping-reference.md#124) | msdyn_customerassetcategories | |
[資産管理資産](mapping-reference.md#125) | msdyn_customerassets | |
[資産管理機能の場所のライフサイクル モデル](mapping-reference.md#134) | msdyn_functionallocationlifecyclemodels | |
[資産管理機能の場所のライフサイクル状態](mapping-reference.md#135) | msdyn_functionallocationlifecyclestates | |
[資産管理機能の場所のタイプ](mapping-reference.md#137) | msdyn_functionallocationtypes | |
[資産管理機能の場所](mapping-reference.md#136) | msdyn_functionallocations | |
[資産管理メーカー](mapping-reference.md#153) | msdyn_manufacturers | |
[資産管理モデル](mapping-reference.md#154) | msdyn_models | |
[資産管理の保証](mapping-reference.md#209) | msdyn_warranties | |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

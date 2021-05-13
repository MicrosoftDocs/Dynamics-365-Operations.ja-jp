---
title: サービスのための社内資産
description: このトピックでは、Microsoft Dynamics 365 Field Service を使用して顧客資産と社内資産の両方にサービスを提供する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: ebda6b5679ec601513fb6d046725b396e69fe0f3
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941417"
---
# <a name="in-house-assets-for-servicing"></a>サービスのための社内資産

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Field Service は、顧客資産をサービスするように設計されています。 Dynamics 365 Supply Chain Management の資産管理は、社内資産を維持するように設計されています。 この 2 つのアプリを統合すると、Field Service を使用して顧客資産と社内資産の両方にサービスを提供できます。 また、機能の場所または階層に基づいて資産を分類し、詳細レベルでサービスを追跡することもできます。

詳細については、[Dynamics 365 Field Service と Supply Chain Management の統合](/dynamics365/field-service/supply-chain-field-service-integration) を参照してください。

## <a name="templates"></a>テンプレート

社内資産には、次のテーブルに示すように、データの相互作用中に連携して作業するコア テーブル マップのコレクションが含まれます。

| Finance and Operations アプリ | Dynamics 365 のモデル駆動型アプリ | 説明 |
|-----------------------------|-----------------------------------|-------------|
| 資産管理資産のライフサイクル モデル | msdyn\_assetlifecyclemodels | |
| 資産管理資産のライフサイクル状態 | msdyn\_assetlifecyclestates | |
| 資産管理資産 | msdyn\_customerassets | |
| 資産管理資産のタイプ | msdyn\_customerassetcategories | |
| 資産管理機能の場所のライフサイクル モデル | msdyn\_functionallocationlifecyclemodels | |
| 資産管理機能の場所のライフサイクル状態 | msdyn\_functionallocationlifecyclestates | |
| 資産管理機能の場所 | msdyn\_functionallocations | |
| 資産管理機能の場所のタイプ | msdyn\_functionallocationtypes | |
| 資産管理メーカー | msdyn\_manufacturers | |
| 資産管理モデル | msdyn\_models | |
| 資産管理の保証 | msdyn\_warranties | |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [lifecycle models](includes/AssetManagementAssetLifecycleModels-msdyn-assetlifecyclemodels.md)]

[!include [lifecycle states](includes/AssetManagementAssetLifecycleStates-msdyn-assetlifecyclestates.md)]

[!include [assets](includes/AssetManagementAssets-msdyn-customerassets.md)]

[!include [asset types](includes/AssetManagementAssetTypes-msdyn-customerassetcategories.md)]

[!include [functional location lifecycle models](includes/AssetManagementFunctionalLocationLifecycleModels-msdyn-functionallocationlifecyclemodels.md)]

[!include [functional location lifecycle states](includes/AssetManagementFunctionalLocationLifecycleStates-msdyn-functionallocationlifecyclestates.md)]

[!include [functional locations](includes/AssetManagementFunctionalLocations-msdyn-functionallocations.md)]

[!include [functional location types](includes/AssetManagementFunctionalLocationTypes-msdyn-functionallocationtypes.md)]

[!include [manufacturers](includes/AssetManagementManufacturers-msdyn-manufacturers.md)]

[!include [models](includes/AssetManagementModels-msdyn-models.md)]

[!include [warranty](includes/AssetManagementWarranty-msdyn-warranties.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
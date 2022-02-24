---
title: 顧客ロイヤルティ カードと報酬ポイント
description: このトピックでは、二重書き込みでの顧客ロイヤルティ カードと報酬ポイントに関するデータの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683501"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>顧客ロイヤルティ カードと報酬ポイント

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

企業は、顧客の買い物と支出パターンに基づいて、顧客を分類し、高度なサービスを提供します。 例えば、Dynamics 365 Commerce では、顧客ロイヤルティ カード、報酬ポイント、ロイヤルティに基づく買い物による価格設定、報奨ベースの買い物に役立つように、インフラストラクチャと機能が搭載されています。 顧客のロイヤルティ カードと Commerce での報奨ポイントに関するデータが Dataverse に同期されている場合、Customer Engagement アプリでそのデータを使用できます。 たとえば、Dynamics 365 Customer Service のユーザーは、このデータを使用して、ヘルプデスクを介して同じ高度なサービスを提供することができます。

## <a name="templates"></a>テンプレート

| Finance and Operations アプリ | Dynamics 365 のモデル駆動型アプリ | 説明 |
|-----------------------------|-----------------------------------|-------------|
| ロイヤルティ カード                | msdyn\_loyaltycards               | このテンプレートは、顧客のロイヤリティ カードに関する情報を同期します。 |
| ロイヤルティ報酬ポイント       | msdyn\_loyaltyrewardpoints        | このテンプレートは、顧客の報酬ポイントに関する情報を同期します。 |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]

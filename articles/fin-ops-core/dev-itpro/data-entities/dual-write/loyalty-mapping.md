---
title: 顧客ロイヤルティ カードと報酬ポイント
description: このトピックでは、Finance and Operations アプリと Common Data Service の間の顧客ロイヤルティカードと報酬ポイントに関するデータの統合について説明します。
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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: e7e67946930404ab7ba0c7fccf468722f723d675
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172972"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>顧客ロイヤルティ カードと報酬ポイント

[!include [banner](../../includes/banner.md)]



企業は、顧客の買い物と支出パターンに基づいて、顧客を分類し、高度なサービスを提供します。 アプリケーションの Microsoft Dynamics 365 スイートで、Dynamics 365 Commerce は、顧客ロイヤルティ カード、報酬ポイント、ロイヤルティに基づく買い物による価格設定、報奨ベースの買い物に役立つように、インフラストラクチャと機能が搭載されています。 顧客のロイヤルティ カードと Commerce の報奨ポイントに関するデータがCommon Data Serviceに同期されている場合、Dynamics 365 のモデル駆動型アプリケーションでそのデータを使用できます。 たとえば、Dynamics 365 Customer Service のユーザーは、このデータを使用して、ヘルプデスクを介して同じ高度なサービスを提供することができます。

## <a name="templates"></a>テンプレート

| Finance and Operations アプリ | Dynamics 365 のモデル駆動型アプリ | 説明 |
|-----------------------------|-----------------------------------|-------------|
| ロイヤルティ カード                | msdyn\_loyaltycards               | このテンプレートは、顧客のロイヤリティ カードに関する情報を同期します。 |
| ロイヤルティ報酬ポイント       | msdyn\_loyaltyrewardpoints        | このテンプレートは、顧客の報酬ポイントに関する情報を同期します。 |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]

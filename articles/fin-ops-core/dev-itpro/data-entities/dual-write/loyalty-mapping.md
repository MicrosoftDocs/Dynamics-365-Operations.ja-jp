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
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="62a1d-103">顧客ロイヤルティ カードと報酬ポイント</span><span class="sxs-lookup"><span data-stu-id="62a1d-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="62a1d-104">企業は、顧客の買い物と支出パターンに基づいて、顧客を分類し、高度なサービスを提供します。</span><span class="sxs-lookup"><span data-stu-id="62a1d-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="62a1d-105">アプリケーションの Microsoft Dynamics 365 スイートで、Dynamics 365 Commerce は、顧客ロイヤルティ カード、報酬ポイント、ロイヤルティに基づく買い物による価格設定、報奨ベースの買い物に役立つように、インフラストラクチャと機能が搭載されています。</span><span class="sxs-lookup"><span data-stu-id="62a1d-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="62a1d-106">顧客のロイヤルティ カードと Commerce の報奨ポイントに関するデータがCommon Data Serviceに同期されている場合、Dynamics 365 のモデル駆動型アプリケーションでそのデータを使用できます。</span><span class="sxs-lookup"><span data-stu-id="62a1d-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="62a1d-107">たとえば、Dynamics 365 Customer Service のユーザーは、このデータを使用して、ヘルプデスクを介して同じ高度なサービスを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="62a1d-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="62a1d-108">テンプレート</span><span class="sxs-lookup"><span data-stu-id="62a1d-108">Templates</span></span>

| <span data-ttu-id="62a1d-109">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="62a1d-109">Finance and Operations apps</span></span> | <span data-ttu-id="62a1d-110">Dynamics 365 のモデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="62a1d-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="62a1d-111">説明</span><span class="sxs-lookup"><span data-stu-id="62a1d-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="62a1d-112">ロイヤルティ カード</span><span class="sxs-lookup"><span data-stu-id="62a1d-112">Loyalty card</span></span>                | <span data-ttu-id="62a1d-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="62a1d-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="62a1d-114">このテンプレートは、顧客のロイヤリティ カードに関する情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="62a1d-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="62a1d-115">ロイヤルティ報酬ポイント</span><span class="sxs-lookup"><span data-stu-id="62a1d-115">Loyalty reward points</span></span>       | <span data-ttu-id="62a1d-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="62a1d-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="62a1d-117">このテンプレートは、顧客の報酬ポイントに関する情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="62a1d-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
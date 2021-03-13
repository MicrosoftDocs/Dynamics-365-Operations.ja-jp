---
title: B2B 組織の組織モデリング階層の作成
description: このトピックでは、企業間 (B2B) 組織の組織モデリング階層を作成する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035930"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a><span data-ttu-id="699f5-103">B2B 組織の組織モデリング階層の作成</span><span class="sxs-lookup"><span data-stu-id="699f5-103">Create org modeling hierarchies for B2B organizations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="699f5-104">このトピックでは、Microsoft Dynamics 365 Commerce で企業間 (B2B) 組織の組織モデリング階層を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="699f5-104">This topic describes how to create organizational modeling hierarchies for business-to-business (B2B) organizations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="699f5-105">Commerce 本部では、取引先組織は顧客および顧客階層のエンティティで表されます。</span><span class="sxs-lookup"><span data-stu-id="699f5-105">In Commerce headquarters, business partner organizations are represented by customer and customer hierarchy entities.</span></span> <span data-ttu-id="699f5-106">取引先組織とそのユーザーは顧客として表され、顧客階層を使用してこれらの顧客を関連付けします。</span><span class="sxs-lookup"><span data-stu-id="699f5-106">The business partner organization and its users are represented as customers, and customer hierarchies are used to associate those customers with each other.</span></span>

<span data-ttu-id="699f5-107">取引先が B2B e コマース サイトへの参加を要求すると、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="699f5-107">When a business partner request to join a B2B e-commerce site is approved, the following actions are performed:</span></span>

- <span data-ttu-id="699f5-108">システムに 2 つの新しい顧客レコードが作成されます : 取引先組織の場合は **組織タイプ** 顧客レコード、依頼者の場合は **担当者タイプ** 顧客レコード (申請を行った取引先組織のユーザー)。</span><span class="sxs-lookup"><span data-stu-id="699f5-108">Two new customer records are created in the system: a **Type Organization** customer record for the business partner organization and a **Type Person** customer record for the requestor (that is, the business partner user who submitted the request).</span></span>
- <span data-ttu-id="699f5-109">**顧客 \> 顧客階層** の下に新しい顧客階層レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="699f5-109">A new customer hierarchy record is created under **Customer \> Customer hierarchy**.</span></span> <span data-ttu-id="699f5-110">このレコードには、次のヘッダー プロパティがあります :</span><span class="sxs-lookup"><span data-stu-id="699f5-110">This record has the following header properties:</span></span>

    - <span data-ttu-id="699f5-111">**顧客階層 ID** - 顧客階層の固有 ID です。</span><span class="sxs-lookup"><span data-stu-id="699f5-111">**Customer hierarchy ID** – A unique ID for the customer hierarchy.</span></span> <span data-ttu-id="699f5-112">この ID では、Commerce 本部の [Commerce] 共有パラメータで定義されている番号順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="699f5-112">This ID uses the number sequence that is defined in Commerce shared parameters in Commerce headquarters.</span></span>
    - <span data-ttu-id="699f5-113">**名前** - オンボード リクエストで指定した取引先組織の名称です。</span><span class="sxs-lookup"><span data-stu-id="699f5-113">**Name** – The organization name of the business partner, as specified in the onboarding request.</span></span>
    - <span data-ttu-id="699f5-114">**目的** - このプロパティは、**B2B 組織** の定義済の値に設定されます 。</span><span class="sxs-lookup"><span data-stu-id="699f5-114">**Purpose** – This property is set to the predefined value **B2B organization**.</span></span>
    - <span data-ttu-id="699f5-115">**組織** - 取引先の顧客 ID です。</span><span class="sxs-lookup"><span data-stu-id="699f5-115">**Organization** – The customer ID of the business partner.</span></span>

<span data-ttu-id="699f5-116">顧客階層レコードの詳細を次に示します :</span><span class="sxs-lookup"><span data-stu-id="699f5-116">Here are the details of the customer hierarchy record:</span></span>

- <span data-ttu-id="699f5-117">申請者の顧客レコードは顧客階層に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="699f5-117">The customer record of the requestor is associated with the customer hierarchy.</span></span>
- <span data-ttu-id="699f5-118">管理者ロールは申請者に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="699f5-118">The administrator role is associated with the requestor.</span></span>

<span data-ttu-id="699f5-119">管理者が B2B サイトの取引先組織にユーザーを追加すると、Commerce 本部にユーザーごとの新しい顧客レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="699f5-119">When the administrator adds more users are to the business partner organization on a B2B site, a new customer record for each user is created in Commerce headquarters.</span></span> <span data-ttu-id="699f5-120">この顧客レコードは、取引先の関連する顧客階層レコードにも追加され、"ユーザー"のロールを持ちます。</span><span class="sxs-lookup"><span data-stu-id="699f5-120">This customer record is also added to the relevant customer hierarchy record for the business partner and has the role of a "user."</span></span>

> [!NOTE]
> <span data-ttu-id="699f5-121">ほとんどの場合、階層内のすべての顧客レコードの対応するプロパティ値は一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="699f5-121">In most cases, the corresponding property values of all customer records in a hierarchy should match.</span></span> <span data-ttu-id="699f5-122">たとえば、すべての取引先ユーザーは共通する製品価格とする必要があるため、価格グループと関連する構成は一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="699f5-122">For example, because all business partner users should get similar prices for products, their price group and associated configurations should match.</span></span> <span data-ttu-id="699f5-123">ただし、この整合性はシステムが適用します。</span><span class="sxs-lookup"><span data-stu-id="699f5-123">However, the system doesn't enforce this consistency.</span></span> <span data-ttu-id="699f5-124">したがって、関連する Commerce 本部のユーザーは、特定の階層内のすべての顧客のプロパティ値と構成が一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="699f5-124">Therefore, the relevant Commerce headquarters users are responsible for ensuring that the property values and configurations match for all customers in a given hierarchy.</span></span>

<span data-ttu-id="699f5-125">Commerce 本部のユーザーは、階層内のすべての顧客レコードのプロパティ値を並べて表示することができます。</span><span class="sxs-lookup"><span data-stu-id="699f5-125">Commerce headquarters users can look at the property values for all customer records in the hierarchy in a side-by-side view.</span></span> <span data-ttu-id="699f5-126">ドロップダウン メニューのタブ名を選択して、関連する顧客レコードのプロパティを選択します。</span><span class="sxs-lookup"><span data-stu-id="699f5-126">Select the relevant customer record properties by selecting the tab names on the drop-down menu.</span></span> <span data-ttu-id="699f5-127">ユーザーは、このビューからプロパティの値を直接確認したり、編集したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="699f5-127">Users can directly view and edit the property values from this view.</span></span> <span data-ttu-id="699f5-128">または、管理者の顧客レコードからすべての値をすべてのユーザーの顧客レコードに適用する場合は、顧客階層の詳細で **上書き** を選択します。</span><span class="sxs-lookup"><span data-stu-id="699f5-128">Alternatively, if you want to apply all the values from the administrator customer record to all the user customer records, select **Override** in the customer hierarchy details.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="699f5-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="699f5-129">Additional resources</span></span>

[<span data-ttu-id="699f5-130">B2B eコマース サイトの設定</span><span class="sxs-lookup"><span data-stu-id="699f5-130">Set up a B2B e-commerce site</span></span>](set-up-b2b-site.md)

[<span data-ttu-id="699f5-131">B2B eコマース サイトでのビジネス パートナー ユーザーの管理</span><span class="sxs-lookup"><span data-stu-id="699f5-131">Manage business partner users on B2B e-commerce sites</span></span>](manage-b2b-users.md)

[<span data-ttu-id="699f5-132">B2B eコマース サイト用の顧客アカウントの支払方法の構成</span><span class="sxs-lookup"><span data-stu-id="699f5-132">Configure the customer account payment method for B2B e-commerce sites</span></span>](payment-method.md)

[<span data-ttu-id="699f5-133">B2B eコマース サイトの製品数量制限の設定</span><span class="sxs-lookup"><span data-stu-id="699f5-133">Set product quantity limits for B2B e-commerce sites</span></span>](quantity-limits.md)

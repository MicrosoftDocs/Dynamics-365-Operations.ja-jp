---
title: Common Data Service の企業概念
description: このトピックでは、Finance and Operations と Common Data Service 間の企業データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa4d54fd7b3ab407751ad6ca1032d742c23eed41
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184534"
---
## <a name="company-concept-in-common-data-service"></a><span data-ttu-id="3a7a2-103">Common Data Service の企業概念</span><span class="sxs-lookup"><span data-stu-id="3a7a2-103">Company concept in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="3a7a2-104">Finance and Operations では、*企業*の概念は、法的コンストラクトとビジネス コンストラクトの両方です。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="3a7a2-105">また、データのセキュリティと可視性の境界でもあります。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="3a7a2-106">ユーザーは常に単一の会社のコンテキストで作業し、データのほとんどは会社によってストライプされます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="3a7a2-107">Common Data Service は、同等の概念を持っていません。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-107">Common Data Service doesn't have an equivalent concept.</span></span> <span data-ttu-id="3a7a2-108">最も近い概念は、主にユーザー データのセキュリティと可視性の境界である*事業単位*です。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="3a7a2-109">この概念は、企業概念と同じ法的またはビジネス上の意味を持ちません。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="3a7a2-110">事業単位と企業は同等の概念ではないため、Common Data Service 統合を目的として 1 対 1 (1:1) のマッピングを強制することはできません。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Common Data Service integration.</span></span> <span data-ttu-id="3a7a2-111">ただし、ユーザーは既定でアプリケーションと Common Data Service にて同じレコードを表示する必要があるため、Microsoft では cdm\_ 企業、という名の Common Data Service に新しいエンティティが導入されています。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-111">However, because users must, by default, be able to see the same records in the application and Common Data Service, Microsoft has introduced a new entity in Common Data Service that is named cdm\_Company.</span></span> <span data-ttu-id="3a7a2-112">このエンティティは、アプリケーションの企業エンティティと同等です。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="3a7a2-113">レコードの可視性はアプリケーションと Common Data Service 間で同等で、すぐに使用できることを保証するために、Common Data Service のデータに向けた次の設定をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-113">To help guarantee that visibility of records is equivalent between the application and Common Data Service out of the box, we recommend the following setup for data in Common Data Service:</span></span>

+ <span data-ttu-id="3a7a2-114">デュアル書き込みが有効になっている Finance and Operations の企業レコードごとに、関連付けられた cdm\_ 企業レコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-114">For each Finance and Operations Company record that is enabled for dual-write, an associated cdm\_Company record is created.</span></span>
+ <span data-ttu-id="3a7a2-115">cdm\_ 企業レコードが作成され、デュアル書き込みが有効になると、同じ名前の既定の事業単位が作成されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-115">When a cdm\_Company record is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="3a7a2-116">既定のチームは、その事業単位に対して自動的に作成されますが、事業単位は使用されません。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="3a7a2-117">同じ名前を持つ別の所有者チームが、作成されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="3a7a2-118">また、事業単位にも関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="3a7a2-119">既定では、作成され、Common Data Service に二重に書き込まれたレコードの所有者は、関連付けられた事業単位にリンクされている「DW 所有者」チームに設定されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-119">By default, the owner of any record that is created and dual-written to Common Data Service is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="3a7a2-120">次の図では、Common Data Service のデータ設定の例を示します。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-120">The following illustration shows an example of this data setup in Common Data Service.</span></span>

![Common Data Service のデータ設定](media/dual-write-company-1.png)

<span data-ttu-id="3a7a2-122">この構成により、USMF 会社に関連するレコードは、Common Data Serviceの USMF 事業単位にリンクされているチームによって所有されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-122">Because of this configuration, any record that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Common Data Service.</span></span> <span data-ttu-id="3a7a2-123">したがって、事業単位レベルの可視性に設定されたセキュリティ ロールを通じて、その事業単位にアクセスできるユーザーは、これらのレコードを表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those records.</span></span> <span data-ttu-id="3a7a2-124">次の例は、チームを使用してこれらのレコードへの正しいアクセスを提供する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-124">The following example shows how teams can be used to provide the correct access to those records.</span></span>

+ <span data-ttu-id="3a7a2-125">「営業マネージャー」のロールは、「USMF セールス」チームのメンバーに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="3a7a2-126">「営業マネージャー」のロールを持つユーザーは、自分が所属する同じ事業単位のメンバーである任意の取引先企業レコードにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-126">Users who have the "Sales Manager" role can access any account records that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="3a7a2-127">「USMF セールス」チームは、前述の USMF 事業単位にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="3a7a2-128">したがって、「USMF セールス」チームのメンバーは、 Finance and Operations の USMF 会社エンティティから来た「USMF DW」ユーザーが所有するアカウントを確認できます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![チームの使用方法](media/dual-write-company-2.png)

<span data-ttu-id="3a7a2-130">前の図に示すように、事業単位、企業、およびチーム間の 1:1 マッピングは、出発点に過ぎません。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="3a7a2-131">この例では、新しい「ヨーロッパ」の事業単位が DEMF と ESMF の両方の Common Data Service にて手動で作成されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-131">In this example, a new "Europe" business unit is manually created in Common Data Service as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="3a7a2-132">この新しいルートの事業単位は、デュアル書き込みとは無関係です。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="3a7a2-133">ただし、関連するセキュリティー ロールの**親 / 子 BU** にデータの可視性を設定することにより、DEMF および ESMF の両方のアカウント データに対する「EUR 営業」チームのメンバーにアクセスできるよう使用できます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="3a7a2-134">最後に、デュアル書き込みによってどの所有者チームが決定されるかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-134">A final topic to discuss is how dual-write determines which owner team it should assign records to.</span></span> <span data-ttu-id="3a7a2-135">この動作は、cdm\_ 企業レコードの**既定の所有チーム**フィールドによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company record.</span></span> <span data-ttu-id="3a7a2-136">cdm\_ 企業レコードがデュアル書き込みに対して有効になっている場合、プラグインは関連付けられた事業単位と所有者チームを自動的に作成し (存在しない場合)、**既定の所有チーム**フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-136">When a cdm\_Company record is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="3a7a2-137">管理者は、このフィールドを別の値に変更できます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="3a7a2-138">ただし、エンティティがデュアル書き込みを有効にしている限り、管理者はフィールドをクリアできません。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

![既定の所有チーム フィールド](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="3a7a2-140">企業のストライピングとブートストラップ</span><span class="sxs-lookup"><span data-stu-id="3a7a2-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="3a7a2-141">Common Data Service 統合は、企業の識別子を使用してデータをストライプすることにより、企業パリティをもたらします。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-141">Common Data Service integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="3a7a2-142">次の図に示すように、すべての企業の固有エンティティは、cdm\_ 企業エンティティと多対1 (N:1) の関係を持つよう拡張されます。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-142">As the following illustration shows, all company-specific entities are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

![企業の固有エンティティと cdm_ 企業エンティティ間の N:1 関係](media/dual-write-bootstrapping.png)

+ <span data-ttu-id="3a7a2-144">レコードの場合、企業が追加および保存された後、値は読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-144">For records, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="3a7a2-145">したがって、ユーザーは正しい企業を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="3a7a2-146">企業データを持つレコードのみが、アプリケーションと Common Data Service 間の二重書き込みの対象となります。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-146">Only records that have company data are eligible for dual-write between the application and Common Data Service.</span></span>
+ <span data-ttu-id="3a7a2-147">既存の Common Data Service データによって、管理者主導のブートストラップ エクスペリエンスがまもなく利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="3a7a2-147">For existing Common Data Service data, an admin-led bootstrapping experience will soon be available.</span></span>
---
title: "グローバル アドレス帳および追加のアドレス帳の構成方法を計画する"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations のグローバル アドレス帳と追加のアドレス帳を設定しコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。 決定の中には、組織階層など、製品の他の領域に対して行われている決定を確認する必要があります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirAddressBook, DirAddressBookTeam, DirParameters, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23341
ms.assetid: a41cd8de-9ee0-4275-aea5-131db5326e5b
ms.search.region: Global
ms.author: shiva.pandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 12bd0a02899c04b0511e2a50bc4a724d5074d13e
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="plan-how-to-configure-the-global-address-book-and-additional-address-books"></a><span data-ttu-id="4a8cc-104">グローバル アドレス帳および追加のアドレス帳の構成方法を計画する</span><span class="sxs-lookup"><span data-stu-id="4a8cc-104">Plan how to configure the global address book and additional address books</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4a8cc-105">この記事は、Microsoft Dynamics 365 for Finance and Operations のグローバル アドレス帳と追加のアドレス帳を設定しコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-105">This article describes the considerations and decisions that you must make during the planning process, before you set up and configure the global address book and any additional address books in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="4a8cc-106">決定の中には、組織階層など、製品の他の領域に対して行われている決定を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-106">Some of the decisions will require that you confirm the decisions that have been made for other areas of the product, such as the organization hierarchy.</span></span>

<a name="global-address-book"></a><span data-ttu-id="4a8cc-107">グローバル アドレス帳</span><span class="sxs-lookup"><span data-stu-id="4a8cc-107">Global address book</span></span>
-------------------

<span data-ttu-id="4a8cc-108">グローバル アドレス帳の使用を開始する前に、その既定値を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-108">Before you begin to work with the global address book, you must determine the default values for it.</span></span> <span data-ttu-id="4a8cc-109">これらの既定値は作成した追加のアドレス帳に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-109">These default values are then used for any additional address books that you create.</span></span> 

<span data-ttu-id="4a8cc-110">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="4a8cc-110">**Decisions:**</span></span>

-   <span data-ttu-id="4a8cc-111">どの順序で、名前を**個人**タイプの関係者レコードに表示しますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-111">What sequence should names be displayed in for party records of the **Person** type?</span></span> <span data-ttu-id="4a8cc-112">姓、ミドルネーム、名の順序など。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-112">For example, one sequence is last name, middle name, first name.</span></span>
-   <span data-ttu-id="4a8cc-113">ロール レコードが削除された場合、関係者レコードをアドレス帳から削除しますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-113">Should party records be deleted from the address book when the role record is deleted?</span></span> <span data-ttu-id="4a8cc-114">たとえば、顧客レコードを削除する場合、関係者レコードも削除しますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-114">For example, if a customer record is deleted, should the party record also be deleted?</span></span>
-   <span data-ttu-id="4a8cc-115">新しいレコードを作成する場合、重複レコードがグローバル アドレス帳にあることをユーザーに通知しますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-115">When a new record is created, should users be notified if a duplicate record is found in the global address book?</span></span>
-   <span data-ttu-id="4a8cc-116">関係者レコードの情報にデータ普遍的の番号付けシステム (DUNS) 番号を含めますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-116">Should the Data Universal Numbering System (DUNS) number be included in a party record’s information?</span></span>
-   <span data-ttu-id="4a8cc-117">DUNS 番号が関係者レコードに含まれる場合、番号の独自性をチェックしますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-117">If the DUNS number is included in a party record, should the uniqueness of the number be checked?</span></span>
-   <span data-ttu-id="4a8cc-118">関係者レコードをグローバル アドレス帳に作成する場合、既定の関係者タイプ、担当者、または組織は必要ですか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-118">When a party record is created in the global address book, do you want a default party type, person, or organization?</span></span>
-   <span data-ttu-id="4a8cc-119">どのユーザー ロールが関係者レコードの個人住所および連絡先情報へのアクセス権を持ちますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-119">Which user roles should have access to the private addresses and contact information of party records?</span></span>

## <a name="additional-address-books"></a><span data-ttu-id="4a8cc-120">追加のアドレス帳</span><span class="sxs-lookup"><span data-stu-id="4a8cc-120">Additional address books</span></span>
<span data-ttu-id="4a8cc-121">グローバル アドレス帳を作成すると、必要に応じて組織の各会社別または事業品目別のアドレス帳など追加のアドレス帳を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-121">After you create the global address book, you can create additional address books as you require, such as a separate address book for each company in your organization or for each line of business.</span></span> <span data-ttu-id="4a8cc-122">たとえば、Fabrikam は、複数の会社と複数の事業品目を持つ国際組織です。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-122">For example, Fabrikam is an international organization that has multiple companies and multiple lines of business.</span></span> <span data-ttu-id="4a8cc-123">Fabrikam では、事業品目ごとにアドレス帳を作成しようとしています。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-123">Fabrikam plans to create an address book for each line of business.</span></span> <span data-ttu-id="4a8cc-124">エアー ツール事業といった複数の場所にまたがる事業品目に対して、Fabrikam では場所ごとのアドレス帳の作成を計画します。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-124">For lines of business that occur in more than one location, such as the pneumatic tools business, Fabrikam plans to create an address book for each location.</span></span> <span data-ttu-id="4a8cc-125">Fabrikam の IT マネージャーの Chris は、必要なアドレス帳の一覧を次のように作成しました。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-125">Chris, the IT manager at Fabrikam, has created the following list of address books that are required.</span></span> <span data-ttu-id="4a8cc-126">この一覧には、各アドレス帳に含める必要がある関係者レコードについても記載しています。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-126">This list also also describes the party records that each address book must include.</span></span>

-   <span data-ttu-id="4a8cc-127">**公共部門契約 (PubSC)** – Fabrikam が結ぶ公共部門契約に関連するすべての関係者の関係者レコード。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-127">**Public Sector Contracts (PubSC)** – Party records for all parties that are involved in the public sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="4a8cc-128">**民間部門契約 (PriSC)** – Fabrikam が結ぶ民間部門契約に関連するすべての関係者の関係者レコード。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-128">**Private Sector Contracts (PriSC)** – Party records for all parties that are involved in the private sector contracts that Fabrikam holds.</span></span>
-   <span data-ttu-id="4a8cc-129">**電子ツール (ET)** – 電子ツールの購買または販売に関わるすべての関係者、または Fabrikam-Japan で Fabrikam による提供または Fabrikam のために購入する電子ツールに関係するすべての関係者の関係レコード。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-129">**Electronic Tools (ET)** – Party records for all parties that are involved in the purchase or sale of electronic tools, or that otherwise interact with the electronic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="4a8cc-130">**エアー ツール (PTJPN)** – エアー ツールの購買または販売に関わるすべての関係者、または Fabrikam-Japan で Fabrikam による提供または Fabrikam のために購入するエアー ツールに関係するすべての関係者の関係レコード。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-130">**Pneumatic Tools (PTJPN)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-Japan company.</span></span>
-   <span data-ttu-id="4a8cc-131">**エアー ツール (PTUSA)** – エアー ツールの購買または販売に関わるすべての関係者、または Fabrikam-US で Fabrikam による提供または Fabrikam のために購入するエアー ツールに関係するすべての関係者の関係レコード。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-131">**Pneumatic Tools (PTUSA)** – Party records for all parties that are involved in the purchase or sale of pneumatic tools, or that otherwise interact with the pneumatic tools that are provided by or purchased for Fabrikam in the Fabrikam-US company.</span></span>

<span data-ttu-id="4a8cc-132">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="4a8cc-132">**Decision:**</span></span>

-   <span data-ttu-id="4a8cc-133">追加のアドレス帳をいくつ作成しますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-133">How many additional address books will you create?</span></span>

### <a name="address-book-security"></a><span data-ttu-id="4a8cc-134">アドレス帳のセキュリティ</span><span class="sxs-lookup"><span data-stu-id="4a8cc-134">Address book security</span></span>

<span data-ttu-id="4a8cc-135">アドレス帳はいつでも作成でき、アドレス帳のセキュリティ パラメーターもいつでも設定できます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-135">You can create address books at any time, and you can also set security parameters for the address books at any time.</span></span> <span data-ttu-id="4a8cc-136">セキュリティ権限のアドレス帳への設定は必須ではありませんが、設定していない場合、組織内のすべての作業者がそのアドレス帳にあるすべての関係者レコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-136">You aren't required to set security privileges for an address book, but if you don't, all workers in your organization can view all party records in that address book.</span></span> <span data-ttu-id="4a8cc-137">関係者レコードのセキュリティ権限は、アドレス帳で設定できます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-137">You can set security privileges to party records through address books.</span></span> <span data-ttu-id="4a8cc-138">セキュリティ権限はチームに基づいています。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-138">Security privileges are based on teams.</span></span> <span data-ttu-id="4a8cc-139">このアプローチでは、アドレス帳へのアクセス権を持つチームに割り当てられている作業者のみが、そのアドレス帳の関係者レコードを表示できることを保証します。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-139">This approach guarantees that only workers who are assigned to a team that has access to an address book can view the party records in that address book.</span></span> <span data-ttu-id="4a8cc-140">各アドレス帳へのアクセス権を持つチームを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-140">You must select the teams that have access to each address book.</span></span> <span data-ttu-id="4a8cc-141">アドレス帳ごとにセキュリティ権限を設定して、特定のチームに対してアクセスを許可または禁止できます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-141">For each address book, you can set security privileges that allow or deny access to specific teams.</span></span> <span data-ttu-id="4a8cc-142">あるチームにアドレス帳への権限を付与すると、そのチーム内のすべてのメンバーが、アドレス帳内のレコードを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-142">If you grant a team privileges to an address book, all members of that team can view the records in the address book.</span></span> <span data-ttu-id="4a8cc-143">アドレス帳へのアクセス権をチームに付与しない場合、そのチームのメンバーは、アドレス帳とアドレス帳の内容を表示できません。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-143">If you don't grant a team access to an address book, the members of that team can't view the address book or its contents.</span></span> 

<span data-ttu-id="4a8cc-144">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="4a8cc-144">**Decision:**</span></span>

-   <span data-ttu-id="4a8cc-145">どのチームが作成した新しい各アドレス帳へのアクセス権を持ちますか。</span><span class="sxs-lookup"><span data-stu-id="4a8cc-145">Which teams should have access to each new address book that you will create?</span></span>





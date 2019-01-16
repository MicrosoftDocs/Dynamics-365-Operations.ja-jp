---
title: "グローバル アドレス帳"
description: "グローバル アドレス帳は、組織に関連付けられている人と組織の関係を理解するのに役立ちます。 たとえば、顧客がマーケティング キャンペーンの仕入先である場合や、組織の作業者が仕入先である場合があります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/05/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, DirPartyTableRoles
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23521
ms.assetid: bb6c02fa-cd91-4ca8-a58c-020502b19074
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: f5da52b9a10be13ab208536c80a6307e4674f35b
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---

# <a name="global-address-book"></a><span data-ttu-id="2128c-104">グローバル アドレス帳</span><span class="sxs-lookup"><span data-stu-id="2128c-104">Global address book</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2128c-105">グローバル アドレス帳は、連携する会社のすべての内部および外部担当者と組織が格納されている必要があるマスター データに対する中央リポジトリです。</span><span class="sxs-lookup"><span data-stu-id="2128c-105">The global address book is a centralized repository for master data that must be stored for all internal and external persons and organizations that the company interacts with.</span></span> <span data-ttu-id="2128c-106">関係者レコードに関連付けられているデータには、関係者の名前、住所、および連絡先情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2128c-106">The data that is associated with party records includes the party's name, address, and contact information.</span></span> <span data-ttu-id="2128c-107">その他の詳細は、関係者が個人か組織かによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2128c-107">Other details vary, depending on whether the party is a person or an organization.</span></span> <span data-ttu-id="2128c-108">各関係者レコードは関係者に割り当てられ、各関係者は会社で 1 つまたは複数の関係者ロールに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="2128c-108">Each party record is assigned to a party, and each party can be associated with one or more party roles in a company.</span></span> <span data-ttu-id="2128c-109">関係者ロールには、顧客、見込顧客、作業者、ユーザー、仕入先、競合他社、申請者、および連絡先が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2128c-109">Party roles include customer, prospect, worker, user, vendor, competitor, applicant, and contact.</span></span> <span data-ttu-id="2128c-110">たとえば、組織関係者ファースト アップ コンサルタントは、顧客、取引関係、および CEE 会社での仕入先ロールと関連付けられ、さらに CEU 会社における仕入先ロールにも関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="2128c-110">For example, the organization party First Up Consultants, can be associated with customer, business relation, and vendor roles in the CEE company, and can also be associated with the vendor role in the CEU company.</span></span> <span data-ttu-id="2128c-111">この共有データの利点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2128c-111">Here are some of the benefits of this shared data:</span></span>

- <span data-ttu-id="2128c-112">このデータは、人や組織が会社の他の分野とどのような関係を持っているかを示しています。</span><span class="sxs-lookup"><span data-stu-id="2128c-112">The data shows the relationships that people and organizations have with other areas of the company.</span></span> <span data-ttu-id="2128c-113">ある組織が仕入先と顧客などの複数の役割を持つ場合、2 つの組織の関係が変わります。</span><span class="sxs-lookup"><span data-stu-id="2128c-113">The relationship between two organizations changes when one organization has multiple roles, such as vendor and customer.</span></span><span data-ttu-id="2128c-114">2 つの組織間の通信も変化します。</span><span class="sxs-lookup"><span data-stu-id="2128c-114"> Communication between the two organization also changes.</span></span><span data-ttu-id="2128c-115">他の組織とのより緊密なパートナーシップを促進するために交渉できる特別協定がある可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2128c-115"> There might be special agreements that can be negotiated to encourage a closer partnership with the other organization.</span></span>
- <span data-ttu-id="2128c-116">設定および管理がより簡単になりました。</span><span class="sxs-lookup"><span data-stu-id="2128c-116">Setup and maintenance are easier.</span></span> <span data-ttu-id="2128c-117">たとえば、アドレスが変更されたときに、更新は 1 箇所のみで行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2128c-117">For example, when an address changes, the update must be made in only one place.</span></span> <span data-ttu-id="2128c-118">その他すべての関連付けられているレコードは自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="2128c-118">All the other associated records are updated automatically.</span></span>

## <a name="how-the-global-address-book-works"></a><span data-ttu-id="2128c-119">グローバル アドレス帳がどのように機能するか</span><span class="sxs-lookup"><span data-stu-id="2128c-119">How the global address book works</span></span>

<span data-ttu-id="2128c-120">次の図は、関係者レコード、関係者ロール、場所、およびトランザクションがアドレス帳とどのようにやり取りし、関連するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="2128c-120">The following illustration shows how party records, party roles, locations, and transactions interact and relate to an address book.</span></span> <span data-ttu-id="2128c-121">図が示すように、関係者レコードは 1 つ以上のアドレス帳に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="2128c-121">As the illustration shows, a party record can belong to one or more address books.</span></span> <span data-ttu-id="2128c-122">各関係者レコードは、1 つ以上の場所や住所に格納でき、関係者ロールが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="2128c-122">Each party record can store one or more locations, or addresses, and is assigned a party role.</span></span> <span data-ttu-id="2128c-123">パーティ レコードに割り当てられているロールには、それに関連付けられた特定のトランザクション タイプを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2128c-123">The role that is assigned to the party record can have specific transactions types associated with it.</span></span> <span data-ttu-id="2128c-124">次のセクションでは、関係者ロール、場所、およびトランザクション タイプについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="2128c-124">The following sections provide more information about party roles, locations, and transaction types.</span></span> <span data-ttu-id="2128c-125">次の図は、グローバル アドレス帳に関連して関係者、関係者の役割、場所、およびトランザクションが対話する方法をグラフで表したものです。</span><span class="sxs-lookup"><span data-stu-id="2128c-125">The following image is a graphical representation of the ways that parties, party roles, locations, and transactions interact in relation to the global address book.</span></span>

<span data-ttu-id="2128c-126">[![AX エンティティおよびトランザクションのグローバル アドレス帳の相互作用](./media/address-book-structure-300x157.png)](./media/address-book-structure.png)</span><span class="sxs-lookup"><span data-stu-id="2128c-126">[![Global address book interaction with AX entities and transactions](./media/address-book-structure-300x157.png)](./media/address-book-structure.png)</span></span>

### <a name="party-roles"></a><span data-ttu-id="2128c-127">関係者ロール</span><span class="sxs-lookup"><span data-stu-id="2128c-127">Party roles</span></span>

<span data-ttu-id="2128c-128">関係者レコードに関連付けられているロールは、関係者ロールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="2128c-128">Roles that are associated with party records are referred to as party roles.</span></span> <span data-ttu-id="2128c-129">パーティーの役割はいくつかあり、パーティーの両方のタイプ (個人と組織) に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="2128c-129">There are several party roles, and they can be assigned to both party types, person and organization.</span></span> <span data-ttu-id="2128c-130">各関係者ロールの定義を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2128c-130">Here are the definitions for each party role:</span></span>

- <span data-ttu-id="2128c-131">**顧客** - 他の個人、会社、またはエンティティによって生産される商品やサービスを購入する個人、会社、または他のエンティティ。</span><span class="sxs-lookup"><span data-stu-id="2128c-131">**Customer** – Individuals, companies, or other entities who purchase goods and services that are produced by other individuals, companies, or entities.</span></span>
- <span data-ttu-id="2128c-132">**見込顧客** – 法人にサービスや便益を提供する可能性のある当事者。</span><span class="sxs-lookup"><span data-stu-id="2128c-132">**Prospect** – A party that might provide a service or benefit to a legal entity.</span></span>
- <span data-ttu-id="2128c-133">**作業者** – 従業員または契約社員のロールを引き受け、サービスと引き換えに給与が支払われる人。</span><span class="sxs-lookup"><span data-stu-id="2128c-133">**Worker** – A person who assumes the role of an employee or a contractor, and who is paid in exchange for services.</span></span>
- <span data-ttu-id="2128c-134">**ユーザー** – システムのユーザーになっている人物。</span><span class="sxs-lookup"><span data-stu-id="2128c-134">**User** – A person who is a user of the system.</span></span>
- <span data-ttu-id="2128c-135">**仕入先** – 支払いと引き換えに、1 社かそれ以上の法人に製品を供給する関係者。</span><span class="sxs-lookup"><span data-stu-id="2128c-135">**Vendor** – A party that supplies products to one or more legal entities in exchange for payment.</span></span>
- <span data-ttu-id="2128c-136">**競合他社** - 自社が提供する商品やサービスのような商品やサービスを提供する個人や組織。</span><span class="sxs-lookup"><span data-stu-id="2128c-136">**Competitor** – A person or organization that provides goods or services that are similar to the goods or services that your business provides.</span></span>
- <span data-ttu-id="2128c-137">**申請者** - 組織内の業務をしたり、空席の職務を埋めるための正式な書面または電子形式の要求を行う人。</span><span class="sxs-lookup"><span data-stu-id="2128c-137">**Applicant** – A person who makes a formal written or electronic request to work for or fill an open position in an organization.</span></span>
- <span data-ttu-id="2128c-138">**連絡先** - 組織の内部または外部のいずれかで、エントリーを作成した個人。</span><span class="sxs-lookup"><span data-stu-id="2128c-138">**Contact** – A person, either inside or outside your organization, that you have created an entry for.</span></span><span data-ttu-id="2128c-139">このエントリでは、個人の住所、電子メール アドレス、電話や FAX 番号、および Web ページの URL などの情報を保存できます。</span><span class="sxs-lookup"><span data-stu-id="2128c-139"> In this entry, you can save information such as the person's street and email addresses, telephone and fax numbers, and webpage URLs.</span></span>

### <a name="creating-new-party-records"></a><span data-ttu-id="2128c-140">新しい関係者レコードを作成しています</span><span class="sxs-lookup"><span data-stu-id="2128c-140">Creating new party records</span></span>

<span data-ttu-id="2128c-141">グローバル アドレス帳にパーティ レコードを入力する方法は 2 つあります。</span><span class="sxs-lookup"><span data-stu-id="2128c-141">There are two ways to enter party records in the global address book:</span></span>

- <span data-ttu-id="2128c-142">**ロールがわからないときに関係者レコードを作成する** - パーティーレコードを作成るときにロール タイプがわからない場合 (例: 関係者が顧客か営業案件かわからない場合)、グローバル アドレス帳にレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="2128c-142">**Creating a party record when you don't know the role** – When you create a party record and don't know the role type (for example, you don't know whether the party is a customer or an opportunity), you create the record in the global address book.</span></span> <span data-ttu-id="2128c-143">ロール タイプを後で選択することができます。</span><span class="sxs-lookup"><span data-stu-id="2128c-143">You can select the role type later.</span></span>
- <span data-ttu-id="2128c-144">**ロールがわかっているときに関係者レコードを作成する** - 関係者のロール タイプがわかっている場合、そのタイプに適切なページでレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2128c-144">**Creating a party record when you know the role** – If you know the role type for the party, you can create a record on the appropriate page for that type.</span></span> <span data-ttu-id="2128c-145">たとえば、関係者が顧客である場合、 **顧客** ページでレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="2128c-145">For example, if the party is a customer, you create a record on the **Customer** page.</span></span> <span data-ttu-id="2128c-146">関係者のロール タイプのページを使用してレコードを作成および保存すると、レコードがグローバル アドレス帳で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="2128c-146">When you create and save a record by using the page for the party's role type, the record is automatically created in the global address book.</span></span>

### <a name="party-roles-and-transactions"></a><span data-ttu-id="2128c-147">関係者ロールとトランザクション</span><span class="sxs-lookup"><span data-stu-id="2128c-147">Party roles and transactions</span></span>

<span data-ttu-id="2128c-148">業務プロセスの一部であるトランザクションについては、複数の関係者が各トランザクションに関連付けられている場合があります。</span><span class="sxs-lookup"><span data-stu-id="2128c-148">For transactions that are a part of the business processes, multiple parties might be associated with each transaction.</span></span> <span data-ttu-id="2128c-149">たとえばプロジェクト見積で参照する必要がある顧客です。</span><span class="sxs-lookup"><span data-stu-id="2128c-149">An example is a customer that needs to be referenced on project quotations.</span></span>

### <a name="parties-locations-addresses-and-contact-information"></a><span data-ttu-id="2128c-150">関係者の場所、住所、および連絡先情報</span><span class="sxs-lookup"><span data-stu-id="2128c-150">Parties locations, addresses, and contact information</span></span>

<span data-ttu-id="2128c-151">各関係者レコードの住所、場所および連絡先情報は、その相手に関連付けられているすべての関係者ロール間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="2128c-151">Each party record's addresses, locations, and contact information are shared across all the party roles that are associated with that party.</span></span> <span data-ttu-id="2128c-152">したがって、この情報のいずれかが変更されると、それに応じて他のすべての関連レコードも更新されます。</span><span class="sxs-lookup"><span data-stu-id="2128c-152">Therefore, when any of this information is changed, all other associated records are updated accordingly.</span></span>

### <a name="locations-and-transactions"></a><span data-ttu-id="2128c-153">場所とトランザクション</span><span class="sxs-lookup"><span data-stu-id="2128c-153">Locations and transactions</span></span>

<span data-ttu-id="2128c-154">関係者が担うロールがトランザクションに含まれているとき、トランザクションの詳細が入力されると、その関係者の場所、住所、または連絡先情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2128c-154">When a party role is included in a transaction, the location, address, or contact information of the party can be accessed when transaction details are entered.</span></span>


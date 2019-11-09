---
title: 登録 ID
description: このトピックでは、登録 ID の設定と使用に関する情報を提供します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 264824
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a0b978228e26ec70457a4bcb1c064070953909b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175500"
---
# <a name="registration-ids"></a><span data-ttu-id="3469b-103">登録 ID</span><span class="sxs-lookup"><span data-stu-id="3469b-103">Registration IDs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3469b-104">このトピックでは、登録 ID の設定と使用に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3469b-104">This topic provides information about setting up and using registration IDs.</span></span>

<span data-ttu-id="3469b-105">多くの国や地域には、登録番号または ID を記録するためのさまざまな規則と条件があります。</span><span class="sxs-lookup"><span data-stu-id="3469b-105">Many countries and regions have different regulations and requirements for recording registration numbers or IDs.</span></span> <span data-ttu-id="3469b-106">このトピックでは、異なる欧州諸国/地域の関係者に必要な設定の概要とサポートされる登録タイプの処理について説明します。</span><span class="sxs-lookup"><span data-stu-id="3469b-106">This topic provides an overview of the required settings and processing of supported registration types for parties in different European countries/regions.</span></span> <span data-ttu-id="3469b-107">すべての国や地域には、それぞれの管轄で提供される登録番号に関連するさまざまな国固有の機能をサポートするための要件があります。</span><span class="sxs-lookup"><span data-stu-id="3469b-107">All countries/regions have their requirements for supporting various country-specific functionalities related to registration numbers provided by different state offices.</span></span> <span data-ttu-id="3469b-108">登録番号の例には、社会保障番号 (SSN)、連邦税 ID (TIN)、および欧州 VAT ID (EU VAT ID) などがあります。</span><span class="sxs-lookup"><span data-stu-id="3469b-108">Examples of registration numbers include, social security number (SSN), tax identification number (TIN), and European VAT identification (EU VAT ID).</span></span> <span data-ttu-id="3469b-109">この機能は、一部のヨーロッパ諸国の国別要件を考慮に入れ、すべての地域のすべての国に統一されたフレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="3469b-109">This feature provides unified framework for all countries in all regions taking into account country-specific requirements of some European countries.</span></span> <span data-ttu-id="3469b-110">次のセクションでは、登録 ID を設定して処理するために使用される情報の流れ全体について説明します。</span><span class="sxs-lookup"><span data-stu-id="3469b-110">The following sections describe the overall flow of information that is used for setting up and processing registration IDs.</span></span>

## <a name="registration-type-creation"></a><span data-ttu-id="3469b-111">登録タイプの作成</span><span class="sxs-lookup"><span data-stu-id="3469b-111">Registration type creation</span></span>
<span data-ttu-id="3469b-112">登録 ID を入力する前に、各関係者が対象となる登録番号のタイプごとに登録タイプを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3469b-112">Before you can enter registration ID, you must set up registration types for the different types of registration numbers that each party is subject to.</span></span> <span data-ttu-id="3469b-113">**組織管理** &gt; **グローバル アドレス帳** &gt; **登録タイプ** &gt; **登録タイプ**ページに進み、異なる国/地域の仕入先、顧客、作業者、法人の登録タイプを作成して管理します。</span><span class="sxs-lookup"><span data-stu-id="3469b-113">Go to **Organization administration** &gt; **Global address book** &gt; **Registration types** &gt; **Registration types**  page to create and manage registration types for vendors, customers, workers, and legal entities in different countries/regions.</span></span>

|<span data-ttu-id="3469b-114">フィールド</span><span class="sxs-lookup"><span data-stu-id="3469b-114">Field</span></span>                 |<span data-ttu-id="3469b-115">説明</span><span class="sxs-lookup"><span data-stu-id="3469b-115">Description</span></span>      |
|------------------------------|----------------------------|                                                                           
| <span data-ttu-id="3469b-116">氏名</span><span class="sxs-lookup"><span data-stu-id="3469b-116">Name</span></span>                | <span data-ttu-id="3469b-117">登録タイプの名前。</span><span class="sxs-lookup"><span data-stu-id="3469b-117">The name of the registration type.</span></span> |                                                                           
| <span data-ttu-id="3469b-118">説明</span><span class="sxs-lookup"><span data-stu-id="3469b-118">Description</span></span>         | <span data-ttu-id="3469b-119">登録タイプの説明。</span><span class="sxs-lookup"><span data-stu-id="3469b-119">The description of the registration type.</span></span> |
| <span data-ttu-id="3469b-120">国/地域</span><span class="sxs-lookup"><span data-stu-id="3469b-120">Country/region</span></span>      | <span data-ttu-id="3469b-121">国/地域の固有 ID。</span><span class="sxs-lookup"><span data-stu-id="3469b-121">The unique identifier of the country/region.</span></span>|
| <span data-ttu-id="3469b-122">税務署長殿</span><span class="sxs-lookup"><span data-stu-id="3469b-122">Tax authority</span></span>       | <span data-ttu-id="3469b-123">登録タイプに関連付けられる税務当局。</span><span class="sxs-lookup"><span data-stu-id="3469b-123">The tax authority that is associated with the registration type.</span></span>|
| <span data-ttu-id="3469b-124">次のものに制限</span><span class="sxs-lookup"><span data-stu-id="3469b-124">Restricted to</span></span>       | <span data-ttu-id="3469b-125">なし、個人、組織の税登録タイプに適用する制限の種類。</span><span class="sxs-lookup"><span data-stu-id="3469b-125">The kind of restriction that applies to the tax registration type: None, Person, Organization.</span></span>|
| <span data-ttu-id="3469b-126">書式設定</span><span class="sxs-lookup"><span data-stu-id="3469b-126">Format</span></span>              | <span data-ttu-id="3469b-127">登録タイプの検証フォーマット。</span><span class="sxs-lookup"><span data-stu-id="3469b-127">The validation format for the registration type.</span></span>|
| <span data-ttu-id="3469b-128">更新可能</span><span class="sxs-lookup"><span data-stu-id="3469b-128">Can be updated</span></span>      | <span data-ttu-id="3469b-129">登録タイプに対する登録番号を入力した後で更新できる場合に定義します。</span><span class="sxs-lookup"><span data-stu-id="3469b-129">Defines if the registration number for the registration type can be updated after it is entered.</span></span>|
| <span data-ttu-id="3469b-130">固有</span><span class="sxs-lookup"><span data-stu-id="3469b-130">Unique</span></span>              | <span data-ttu-id="3469b-131">登録タイプの登録番号が他と重複しない場合に定義します。</span><span class="sxs-lookup"><span data-stu-id="3469b-131">Defines if the registration number for the registration type is unique.</span></span> |
| <span data-ttu-id="3469b-132">主要国</span><span class="sxs-lookup"><span data-stu-id="3469b-132">Primary for country</span></span> | <span data-ttu-id="3469b-133">当事者が特定の国で 1 つ以上の住所に関連付けられ、登録 ID がこれらの住所すべてに有効である場合、その国での基本住所を 1 つ指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3469b-133">If a party is associated with one or more addresses in particular country and the registration ID is valid for all these addresses, you must designate one address as primary for the country.</span></span> <span data-ttu-id="3469b-134">基本として 1 つの ID のみ登録できます。</span><span class="sxs-lookup"><span data-stu-id="3469b-134">You can only register one ID as primary.</span></span> <span data-ttu-id="3469b-135">国の住所の基本にのみ登録番号を入力できる場合に定義します。</span><span class="sxs-lookup"><span data-stu-id="3469b-135">Defines if the registration number can be entered only for primary for country address.</span></span> |

## <a name="assign-a-registration-type-to-a-registration-category"></a><span data-ttu-id="3469b-136">登録カテゴリへの登録タイプの割り当て</span><span class="sxs-lookup"><span data-stu-id="3469b-136">Assign a registration type to a registration category</span></span>
<span data-ttu-id="3469b-137">登録カテゴリは、税、関税、他の目的に関して特定の国/地域で使用するを許可された国/地域の登録 ID です。</span><span class="sxs-lookup"><span data-stu-id="3469b-137">Registration category is country/region registration identifier approved for using in particular country/region for tax, customs and other purposes.</span></span> <span data-ttu-id="3469b-138">このカテゴリは、特定の登録 ID (チェック ディジットなど含む) および異なるレポートに含まれる登録 ID の検証ルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="3469b-138">This category defines validation rules of particular registration ID (including check digits etc.) and inclusion registration ID in different reports.</span></span> <span data-ttu-id="3469b-139">**組織管理** &gt; **グローバル アドレス帳** &gt; **登録タイプ** &gt; **登録カテゴリ**のページを使用して、サポートされている登録カテゴリに特定の国の登録タイプを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3469b-139">Use the page **Organization administration** &gt; **Global address book** &gt; **Registration types** &gt; **Registration categories** to assign registration type of particular country to supported registration category.</span></span>

| <span data-ttu-id="3469b-140">フィールド</span><span class="sxs-lookup"><span data-stu-id="3469b-140">Field</span></span>            | <span data-ttu-id="3469b-141">説明</span><span class="sxs-lookup"><span data-stu-id="3469b-141">Description</span></span>|
|-----------------------|----------------|
| <span data-ttu-id="3469b-142">登録タイプ</span><span class="sxs-lookup"><span data-stu-id="3469b-142">Registration type</span></span>     | <span data-ttu-id="3469b-143">特定の国/地域での登録タイプ。</span><span class="sxs-lookup"><span data-stu-id="3469b-143">The registration type in particular country/region.</span></span>|
| <span data-ttu-id="3469b-144">次のものに制限</span><span class="sxs-lookup"><span data-stu-id="3469b-144">Restricted to</span></span>         | <span data-ttu-id="3469b-145">制限の種類は、なし、個人、組織の税登録タイプに適用されます。</span><span class="sxs-lookup"><span data-stu-id="3469b-145">The kind of restriction applies to the tax registration type: None, Person, Organization.</span></span>|
| <span data-ttu-id="3469b-146">登録カテゴリ</span><span class="sxs-lookup"><span data-stu-id="3469b-146">Registration category</span></span> | <span data-ttu-id="3469b-147">国で使用するために承認された固有の登録 ID。</span><span class="sxs-lookup"><span data-stu-id="3469b-147">The unique registration identifier approved for using in the country.</span></span> <span data-ttu-id="3469b-148">サポートされるカテゴリの完全なリストは、このトピックの後半で表示されます。</span><span class="sxs-lookup"><span data-stu-id="3469b-148">The full list of supported categories is shown later in this topic.</span></span> |

## <a name="enter-registration-ids-for-global-address-book-records"></a><span data-ttu-id="3469b-149">グローバル アドレス帳レコードの登録 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="3469b-149">Enter registration IDs for Global address book records</span></span>

<span data-ttu-id="3469b-150">グローバル アドレス帳 (GAB) には、顧客、仕入先、連絡先、取引関係、法人の連結された住所情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3469b-150">The global address book (GAB) contains consolidated address information for customers, vendors, contacts, business relations, and legal entities.</span></span> <span data-ttu-id="3469b-151">詳細については、「[グローバル アドレス帳の概要](../../fin-and-ops/organization-administration/overview-global-address-book.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3469b-151">For more information see, [Global address book overview](../../fin-and-ops/organization-administration/overview-global-address-book.md).</span></span> <span data-ttu-id="3469b-152">グローバル アドレス帳に格納されている関係者レコードは、1 つ以上の住所レコードを格納できます。</span><span class="sxs-lookup"><span data-stu-id="3469b-152">The party records that are stored in the global address book can contain one or more address records.</span></span> <span data-ttu-id="3469b-153">これらの住所は、請求または配送など、さまざまな目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="3469b-153">These addresses are used for different purposes, such as billing or delivery.</span></span> <span data-ttu-id="3469b-154">顧客、仕入先、作業者、法人の住所情報に対する登録 ID を設定できます。</span><span class="sxs-lookup"><span data-stu-id="3469b-154">You can set up registration IDs for address information for customers, vendors, workers, and legal entities.</span></span> <span data-ttu-id="3469b-155">登録 ID を入力する関係者 (法人、仕入先、顧客、作業者) レコードを検索し、関係者、法人、仕入先、顧客、作業者に関連するフォームでの**登録 ID** をクリックして、**アドレスの管理**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="3469b-155">Find the party (legal entity, vendor, customer, worker) record for which you want to enter the register ID, and then click **Registration IDs** on forms related to party, legal entity, vendor, customer, worker to open the **Manage addresses** page.</span></span> <span data-ttu-id="3469b-156">**税登録**タブで、**追加**をクリックし、登録 ID に関する次の情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="3469b-156">On the **Tax registration** tab, click **Add**, and enter following information about the registration ID.</span></span>


|<span data-ttu-id="3469b-157">フィールド</span><span class="sxs-lookup"><span data-stu-id="3469b-157">Field</span></span>                |<span data-ttu-id="3469b-158">説明</span><span class="sxs-lookup"><span data-stu-id="3469b-158">Description</span></span>                                                |
|---------------------|-----------------------------------------------------------|
| <span data-ttu-id="3469b-159">登録タイプ</span><span class="sxs-lookup"><span data-stu-id="3469b-159">Registration type</span></span>   | <span data-ttu-id="3469b-160">選択した国/地域での登録タイプ。</span><span class="sxs-lookup"><span data-stu-id="3469b-160">The registration type in the selected country/region.</span></span>     |
| <span data-ttu-id="3469b-161">登録番号</span><span class="sxs-lookup"><span data-stu-id="3469b-161">Registration number</span></span> | <span data-ttu-id="3469b-162">当事者の登録 ID。</span><span class="sxs-lookup"><span data-stu-id="3469b-162">The party registration ID.</span></span>                                |
| <span data-ttu-id="3469b-163">説明</span><span class="sxs-lookup"><span data-stu-id="3469b-163">Description</span></span>         | <span data-ttu-id="3469b-164">登録番号の説明。</span><span class="sxs-lookup"><span data-stu-id="3469b-164">The description of the registration number.</span></span>               |
| <span data-ttu-id="3469b-165">項</span><span class="sxs-lookup"><span data-stu-id="3469b-165">Section</span></span>             | <span data-ttu-id="3469b-166">登録番号に関する追加情報。</span><span class="sxs-lookup"><span data-stu-id="3469b-166">The additional information about the registration number.</span></span> |
| <span data-ttu-id="3469b-167">発行機関</span><span class="sxs-lookup"><span data-stu-id="3469b-167">Issuing agency</span></span>      | <span data-ttu-id="3469b-168">登録番号を発行した機関。</span><span class="sxs-lookup"><span data-stu-id="3469b-168">The authority that issued the registration number.</span></span>        |
| <span data-ttu-id="3469b-169">発行日</span><span class="sxs-lookup"><span data-stu-id="3469b-169">Issued date</span></span>         | <span data-ttu-id="3469b-170">登録番号の発行日。</span><span class="sxs-lookup"><span data-stu-id="3469b-170">The issued date for the registration number.</span></span>              |
| <span data-ttu-id="3469b-171">開始</span><span class="sxs-lookup"><span data-stu-id="3469b-171">Effective</span></span>           | <span data-ttu-id="3469b-172">登録番号の有効日。</span><span class="sxs-lookup"><span data-stu-id="3469b-172">The effective date for the registration number.</span></span>           |
| <span data-ttu-id="3469b-173">有効期限</span><span class="sxs-lookup"><span data-stu-id="3469b-173">Expiration</span></span>          | <span data-ttu-id="3469b-174">登録番号の有効期限。</span><span class="sxs-lookup"><span data-stu-id="3469b-174">The expiration date for the registration number.</span></span>          |

> [!NOTE]
> <span data-ttu-id="3469b-175">法人、仕入先、顧客の課税控除番号は、VAT ID に関連して関係者に対して入力された登録 ID から選択できます。</span><span class="sxs-lookup"><span data-stu-id="3469b-175">The tax exempt number of legal entity, vendor, customer can be selected from registration IDs related to the VAT ID and entered for the party.</span></span>

## <a name="search-for-records-by-registration-id"></a><span data-ttu-id="3469b-176">登録 ID ごとのレコードの検索</span><span class="sxs-lookup"><span data-stu-id="3469b-176">Search for records by registration ID</span></span>
<span data-ttu-id="3469b-177">登録 ID に基づいた関係者レコードの検索が、関係者、法人、仕入先、顧客、および作業者に関連するフォームで使用できます。</span><span class="sxs-lookup"><span data-stu-id="3469b-177">Search for party records based on a registration ID is available on forms related to party, legal entity, vendor, customer, and worker.</span></span> <span data-ttu-id="3469b-178">**登録 ID 検索**をクリックして、**登録 ID 検索基準**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="3469b-178">Click **Registration ID search** to open the **Registration ID search criteria** page.</span></span> <span data-ttu-id="3469b-179">検索基準を指定して**検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3469b-179">Specify search criteria and click **Find**.</span></span> <span data-ttu-id="3469b-180">グローバル アドレス帳から選択されたレコードと関係者レコードに関連付けられているタイプがシステムによって表示されます。</span><span class="sxs-lookup"><span data-stu-id="3469b-180">The system will display the selected records from the global address book and the associated types of party record.</span></span>

## <a name="supported-registration-categories"></a><span data-ttu-id="3469b-181">サポートされる登録カテゴリ</span><span class="sxs-lookup"><span data-stu-id="3469b-181">Supported registration categories</span></span>
<span data-ttu-id="3469b-182">次のテーブルに、サポートされている登録タイプの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="3469b-182">The following table lists the supported registration types.</span></span> <span data-ttu-id="3469b-183">登録 ID について Microsoft Dynamics AX 2012 のフィールドで使い慣れている場合、この表を使って Dynamics 365 Finance の登録カテゴリにそれらのフィールドをマップします。</span><span class="sxs-lookup"><span data-stu-id="3469b-183">If you're familiar with the Microsoft Dynamics AX 2012 fields for registration IDs, this table also maps those fields to the Dynamics 365 Finance registration categories.</span></span>

| <span data-ttu-id="3469b-184">Finance 登録カテゴリ</span><span class="sxs-lookup"><span data-stu-id="3469b-184">Finance Registration category</span></span>         |<span data-ttu-id="3469b-185">国/地域</span><span class="sxs-lookup"><span data-stu-id="3469b-185">Country/Region</span></span>  | <span data-ttu-id="3469b-186">Dynamics AX 2012 の用語/フィールド</span><span class="sxs-lookup"><span data-stu-id="3469b-186">Dynamics AX 2012 term/field</span></span>|
|---------------------------------------------------------------|---------------------|---------------------------------|
| <span data-ttu-id="3469b-187">VAT</span><span class="sxs-lookup"><span data-stu-id="3469b-187">VAT ID</span></span>                                                        | <span data-ttu-id="3469b-188">欧州連合 (EU) のすべての国</span><span class="sxs-lookup"><span data-stu-id="3469b-188">All countries of the European Union (EU)</span></span>|  <span data-ttu-id="3469b-189">課税控除番号 (AX 2012 R3 での法律タイプ TAX ID)</span><span class="sxs-lookup"><span data-stu-id="3469b-189">Tax exempt number (Legislative type TAX ID in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-190">エンタープライズ ID (COID)</span><span class="sxs-lookup"><span data-stu-id="3469b-190">Enterprise ID (COID)</span></span>                                          | <span data-ttu-id="3469b-191">ベルギー チェコ共和国 エストニア ハンガリー ラトビア リトアニア ポーランド スイス</span><span class="sxs-lookup"><span data-stu-id="3469b-191">Belgium Czech Republic Estonia Hungary Latvia Lithuania Poland Switzerland</span></span> | <span data-ttu-id="3469b-192">企業番号 (EnterpriseNumber) 登録番号 (RegNum\_W) 登録番号 (RegNum\_W) 登録番号 (RegNum\_W) 登録番号 (RegNum\_W) 企業コード (EnterpriseCode) 登録番号 (RegNum\_W) UID (AX 2012 R3 での法律タイプ UID)</span><span class="sxs-lookup"><span data-stu-id="3469b-192">Enterprise number (EnterpriseNumber) Registration number (RegNum\_W) Registration number (RegNum\_W) Registration number (RegNum\_W) Registration number (RegNum\_W) Enterprise code (EnterpriseCode) Registration number (RegNum\_W) UID (Legislative type UID in AX 2012 R3)</span></span> |
| <span data-ttu-id="3469b-193">支店 ID</span><span class="sxs-lookup"><span data-stu-id="3469b-193">Branch ID</span></span>                                                     | <span data-ttu-id="3469b-194">ベルギー</span><span class="sxs-lookup"><span data-stu-id="3469b-194">Belgium</span></span>            | <span data-ttu-id="3469b-195">支店番号 (BranchNumber)</span><span class="sxs-lookup"><span data-stu-id="3469b-195">Branch number (BranchNumber)</span></span>|
| <span data-ttu-id="3469b-196">Spisová značka (登録番号、発行機関、セクション)</span><span class="sxs-lookup"><span data-stu-id="3469b-196">Spisová značka (Registration number, Issuing agency, Section)</span></span> | <span data-ttu-id="3469b-197">チェコ共和国</span><span class="sxs-lookup"><span data-stu-id="3469b-197">Czech Republic</span></span>     | <span data-ttu-id="3469b-198">挿入番号 (CommercialRegisterInsetNumber) 商業登記で維持 (CommercialRegister) 商業登記のセクション (CommercialRegisterSection)</span><span class="sxs-lookup"><span data-stu-id="3469b-198">Inset number (CommercialRegisterInsetNumber) Kept at commercial register (CommercialRegister) Section of commercial register (CommercialRegisterSection)</span></span>|
| <span data-ttu-id="3469b-199">税関顧客 ID</span><span class="sxs-lookup"><span data-stu-id="3469b-199">Customs customer ID</span></span>                                           | <span data-ttu-id="3469b-200">フィンランド</span><span class="sxs-lookup"><span data-stu-id="3469b-200">Finland</span></span> | <span data-ttu-id="3469b-201">税関顧客番号 (CustomsCustomerNumber\_FI)</span><span class="sxs-lookup"><span data-stu-id="3469b-201">Customs customer number (CustomsCustomerNumber\_FI)</span></span>|
| <span data-ttu-id="3469b-202">INN</span><span class="sxs-lookup"><span data-stu-id="3469b-202">INN</span></span>                                                           | <span data-ttu-id="3469b-203">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-203">Russian Federation</span></span>| <span data-ttu-id="3469b-204">INN (AX 2012 R3 での法律タイプ INN)</span><span class="sxs-lookup"><span data-stu-id="3469b-204">INN (Legislative type INN in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-205">RRC</span><span class="sxs-lookup"><span data-stu-id="3469b-205">RRC</span></span>                                                           | <span data-ttu-id="3469b-206">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-206">Russian Federation</span></span>| <span data-ttu-id="3469b-207">RRC (AX 2012 R3 での法律タイプ RRC)</span><span class="sxs-lookup"><span data-stu-id="3469b-207">RRC (Legislative type RRC in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-208">OKDP</span><span class="sxs-lookup"><span data-stu-id="3469b-208">OKDP</span></span>                                                          | <span data-ttu-id="3469b-209">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-209">Russian Federation</span></span>| <span data-ttu-id="3469b-210">OKDP (AX 2012 R3 での法律タイプ OKDP)</span><span class="sxs-lookup"><span data-stu-id="3469b-210">OKDP (Legislative type OKDP in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-211">OKPO</span><span class="sxs-lookup"><span data-stu-id="3469b-211">OKPO</span></span>                                                          | <span data-ttu-id="3469b-212">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-212">Russian Federation</span></span>| <span data-ttu-id="3469b-213">OKPO (AX 2012 R3 での法律タイプ OKPO)</span><span class="sxs-lookup"><span data-stu-id="3469b-213">OKPO (Legislative type OKPO in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-214">RCOAD</span><span class="sxs-lookup"><span data-stu-id="3469b-214">RCOAD</span></span>                                                         | <span data-ttu-id="3469b-215">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-215">Russian Federation</span></span>| <span data-ttu-id="3469b-216">RCOAD (AX 2012 R3 での法律タイプ RCOAD)</span><span class="sxs-lookup"><span data-stu-id="3469b-216">RCOAD (Legislative type RCOAD in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-217">OGRN</span><span class="sxs-lookup"><span data-stu-id="3469b-217">OGRN</span></span>                                                          | <span data-ttu-id="3469b-218">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-218">Russian Federation</span></span>| <span data-ttu-id="3469b-219">OGRN (AX 2012 R3 での法律タイプ OGRN)</span><span class="sxs-lookup"><span data-stu-id="3469b-219">OGRN (Legislative type OGRN in AX 2012 R3)</span></span> |
| <span data-ttu-id="3469b-220">SNILS</span><span class="sxs-lookup"><span data-stu-id="3469b-220">SNILS</span></span>                                                         | <span data-ttu-id="3469b-221">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-221">Russian Federation</span></span>| <span data-ttu-id="3469b-222">SNILS (AX 2012 R3 での法律タイプ SNILS)</span><span class="sxs-lookup"><span data-stu-id="3469b-222">SNILS (Legislative type SNILS in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-223">CIFTS</span><span class="sxs-lookup"><span data-stu-id="3469b-223">CIFTS</span></span>                                                         | <span data-ttu-id="3469b-224">ロシア連邦</span><span class="sxs-lookup"><span data-stu-id="3469b-224">Russian Federation</span></span>| <span data-ttu-id="3469b-225">CIFTS (AX 2012 R3 での法律タイプ CIFTS)</span><span class="sxs-lookup"><span data-stu-id="3469b-225">CIFTS (Legislative type CIFTS in AX 2012 R3)</span></span>|
| <span data-ttu-id="3469b-226">パスポート</span><span class="sxs-lookup"><span data-stu-id="3469b-226">Passport</span></span>                                                      | <span data-ttu-id="3469b-227">スペイン</span><span class="sxs-lookup"><span data-stu-id="3469b-227">Spain</span></span>             | <span data-ttu-id="3469b-228">パスポート</span><span class="sxs-lookup"><span data-stu-id="3469b-228">Passport</span></span>|
| <span data-ttu-id="3469b-229">公式の ID ドキュメント</span><span class="sxs-lookup"><span data-stu-id="3469b-229">Official identification document</span></span>                              | <span data-ttu-id="3469b-230">スペイン</span><span class="sxs-lookup"><span data-stu-id="3469b-230">Spain</span></span>             | <span data-ttu-id="3469b-231">公式の ID ドキュメント</span><span class="sxs-lookup"><span data-stu-id="3469b-231">Official identification document</span></span>|
| <span data-ttu-id="3469b-232">居住証明書</span><span class="sxs-lookup"><span data-stu-id="3469b-232">Residence certificate</span></span>                                         | <span data-ttu-id="3469b-233">スペイン</span><span class="sxs-lookup"><span data-stu-id="3469b-233">Spain</span></span>             | <span data-ttu-id="3469b-234">居住証明書</span><span class="sxs-lookup"><span data-stu-id="3469b-234">Residence certificate</span></span>|
| <span data-ttu-id="3469b-235">他の ID ドキュメント</span><span class="sxs-lookup"><span data-stu-id="3469b-235">Other identification document</span></span>                                 | <span data-ttu-id="3469b-236">スペイン</span><span class="sxs-lookup"><span data-stu-id="3469b-236">Spain</span></span>             | <span data-ttu-id="3469b-237">他の ID ドキュメント</span><span class="sxs-lookup"><span data-stu-id="3469b-237">Other identification document</span></span>|
| <span data-ttu-id="3469b-238">調査されていません</span><span class="sxs-lookup"><span data-stu-id="3469b-238">Not censused</span></span>                                                  | <span data-ttu-id="3469b-239">スペイン</span><span class="sxs-lookup"><span data-stu-id="3469b-239">Spain</span></span>             | <span data-ttu-id="3469b-240">AX 2012 R3 では使用できません</span><span class="sxs-lookup"><span data-stu-id="3469b-240">Not available in AX 2012 R3</span></span>|


<span data-ttu-id="3469b-241">必須の前提条件を含む登録 ID 処理の詳細については、Lifecycle Services (LCS) での VAT ID に関する次のタスク記録を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3469b-241">For more information about registration IDs processing, including required prerequisites, see the following task recordings for VAT ID in Lifecycle Services (LCS):</span></span>

-   <span data-ttu-id="3469b-242">VAT ID の設定</span><span class="sxs-lookup"><span data-stu-id="3469b-242">Set up VAT ID</span></span>
-   <span data-ttu-id="3469b-243">仕入先の VAT ID 登録</span><span class="sxs-lookup"><span data-stu-id="3469b-243">VAT ID registration of vendor</span></span>
-   <span data-ttu-id="3469b-244"> VAT ID を使用する関係者の検索</span><span class="sxs-lookup"><span data-stu-id="3469b-244">Party search using VAT ID</span></span>




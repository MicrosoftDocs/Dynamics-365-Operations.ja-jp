---
title: 統合済み顧客マスター
description: このトピックでは、Finance and Operations と Common Data Service 間の顧客データの統合について説明します。
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
ms.openlocfilehash: 269346d38eeb3812c352d16f9d50fbcd09307c12
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124592"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="2056d-103">統合された顧客マスター</span><span class="sxs-lookup"><span data-stu-id="2056d-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="2056d-104">顧客レコードは、複数のアプリケーションで習得するのが一般的です。</span><span class="sxs-lookup"><span data-stu-id="2056d-104">It's typical for customer records to be mastered in more than one application.</span></span> <span data-ttu-id="2056d-105">たとえば、営業活動は Sales アプリケーションを通じて商用顧客レコードを取り込むことができ、電子商取引または小売販売は、Finance and Operations アプリケーションを通じて顧客レコードを取り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="2056d-105">For example, sales activity can bring in commercial customer records through a Sales application, and e-Commerce or retail sales can bring in customer records through a Finance and Operations application.</span></span> <span data-ttu-id="2056d-106">顧客レコードの発生元にかかわらず、アプリケーションの境界およびインフラストラクチャの違いを越えてバックグラウンドで統合されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-106">Regardless of where the customer record originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> <span data-ttu-id="2056d-107">統合された顧客マスタリングは、マルチ マスタリング シナリオの処理に役立ち、Dynamics 365 アプリケーション スイートに顧客の包括的な情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="2056d-107">Integrated customer mastering helps handle multi-mastering scenarios and provides a comprehensive view of the customer to the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="2056d-108">顧客データ フロー</span><span class="sxs-lookup"><span data-stu-id="2056d-108">Customer data flow</span></span>

<span data-ttu-id="2056d-109">*顧客*は、アプリケーションで明確に定義された概念です。</span><span class="sxs-lookup"><span data-stu-id="2056d-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="2056d-110">したがって、顧客データの統合は、2 つのアプリケーションの間で顧客の概念を調和させるだけです。</span><span class="sxs-lookup"><span data-stu-id="2056d-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="2056d-111">次の図は、顧客データ フローを示します。</span><span class="sxs-lookup"><span data-stu-id="2056d-111">The following illustration shows the customer data flow.</span></span>

![顧客データ フロー](media/dual-write-customer-data-flow.png)

<span data-ttu-id="2056d-113">顧客は、商用 / 組織の顧客および消費者 / エンド ユーザーの 2 種類に大きく分類できます。</span><span class="sxs-lookup"><span data-stu-id="2056d-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="2056d-114">これら 2 種類の顧客は、Finance and Operations と Common Data Service にて、異なる方法で格納および処理されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="2056d-115">Finance and Operations では、商用 / 組織の顧客および消費者 / エンド ユーザーの両方が、**CustTable** (CustomerCustomerV3Entity) という名前の単一のテーブルで習得され、**タイプ**属性に基づいて分類されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustomerCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="2056d-116">(**タイプ**が**組織**に設定されている場合、顧客は商用 / 組織の顧客であり、**タイプ**が**人材**に設定されている場合、顧客はコンシューマ / エンド ユーザーです。) 主な連絡担当者情報は、SMMContactPersonEntity エンティティを介して処理されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-116">(If **Type** is set to **Organization**, the customer is a commercial/organizational customer, and if **Type** is set to **Person**, the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="2056d-117">Common Data Serviceでは、商取引 / 組織の顧客は口座エンティティで習得され、**リレーションシップ タイプ**属性が**顧客**に設定されている場合、顧客として識別されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="2056d-118">コンシューマ / エンド ユーザーと連絡担当者の両方が、連絡先エンティティによって表されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="2056d-119">コンシューマー / エンド ユーザーおよび連絡担当者の間を明確に分離するために、**連絡先**エンティティには**販売可能**という名前のブール フラグがあります。</span><span class="sxs-lookup"><span data-stu-id="2056d-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="2056d-120">**販売可能**が **True** の場合、連絡先はコンシューマー / エンド ユーザーであり、その連絡先に対して見積と注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2056d-120">When **Sellable** is **True**, the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="2056d-121">**販売可能が**が **False** の場合、連絡先は顧客の主要な連絡担当者にすぎません。</span><span class="sxs-lookup"><span data-stu-id="2056d-121">When **Sellable** is **False**, the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="2056d-122">販売不能な取引先担当者が見積または注文プロセスに参加する場合、**販売可能**が **True** に設定され、取引先担当者に販売可能な取引先担当者としてフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="2056d-123">販売可能な取引先担当者になった連絡先は、引き続き販売可能な連絡先です。</span><span class="sxs-lookup"><span data-stu-id="2056d-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="2056d-124">テンプレート</span><span class="sxs-lookup"><span data-stu-id="2056d-124">Templates</span></span>

<span data-ttu-id="2056d-125">顧客データには、顧客グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、顧客に関するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="2056d-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="2056d-126">次の表に示すように、エンティティ マップのコレクションは、顧客データ操作中に連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="2056d-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="2056d-127">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="2056d-127">Finance and Operations apps</span></span> | <span data-ttu-id="2056d-128">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="2056d-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="2056d-129">説明</span><span class="sxs-lookup"><span data-stu-id="2056d-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="2056d-130">CDS 連絡先 V2</span><span class="sxs-lookup"><span data-stu-id="2056d-130">CDS Contacts V2</span></span>             | <span data-ttu-id="2056d-131">連絡先</span><span class="sxs-lookup"><span data-stu-id="2056d-131">contacts</span></span>                        | <span data-ttu-id="2056d-132">このテンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。</span><span class="sxs-lookup"><span data-stu-id="2056d-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="2056d-133">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="2056d-133">Customer groups</span></span>             | <span data-ttu-id="2056d-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="2056d-134">msdyn_customergroups</span></span>            | <span data-ttu-id="2056d-135">このテンプレートは、顧客グループ情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="2056d-136">顧客支払方法</span><span class="sxs-lookup"><span data-stu-id="2056d-136">Customer payment method</span></span>     | <span data-ttu-id="2056d-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="2056d-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="2056d-138">このテンプレートは、顧客支払方法に関する情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="2056d-139">顧客 V3</span><span class="sxs-lookup"><span data-stu-id="2056d-139">Customers V3</span></span>                | <span data-ttu-id="2056d-140">勘定</span><span class="sxs-lookup"><span data-stu-id="2056d-140">accounts</span></span>                        | <span data-ttu-id="2056d-141">このテンプレートは、商業および組織顧客の顧客マスター情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="2056d-142">顧客 V3</span><span class="sxs-lookup"><span data-stu-id="2056d-142">Customers V3</span></span>                | <span data-ttu-id="2056d-143">連絡先</span><span class="sxs-lookup"><span data-stu-id="2056d-143">contacts</span></span>                        | <span data-ttu-id="2056d-144">このテンプレートは、消費者およびエンド ユーザーの顧客マスター データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="2056d-145">ロイヤルティ カード</span><span class="sxs-lookup"><span data-stu-id="2056d-145">Loyalty card</span></span>                | <span data-ttu-id="2056d-146">msdyn_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="2056d-146">msdyn_loyaltycards</span></span>              | <span data-ttu-id="2056d-147">このテンプレートは、顧客のロイヤリティ カード情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-147">This template synchronizes customer loyalty card information.</span></span>
<span data-ttu-id="2056d-148">名前の接辞</span><span class="sxs-lookup"><span data-stu-id="2056d-148">Name affixes</span></span>                | <span data-ttu-id="2056d-149">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="2056d-149">msdyn_nameaffixes</span></span>               | <span data-ttu-id="2056d-150">このテンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-150">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2056d-151">支払期日明細行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="2056d-151">Payment day lines CDS V2</span></span>    | <span data-ttu-id="2056d-152">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="2056d-152">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="2056d-153">このテンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-153">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2056d-154">支払期日 CDS</span><span class="sxs-lookup"><span data-stu-id="2056d-154">Payment days CDS</span></span>            | <span data-ttu-id="2056d-155">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="2056d-155">msdyn_paymentdays</span></span>               | <span data-ttu-id="2056d-156">このテンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-156">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2056d-157">支払スケジュール行</span><span class="sxs-lookup"><span data-stu-id="2056d-157">Payment schedule lines</span></span>      | <span data-ttu-id="2056d-158">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="2056d-158">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="2056d-159">顧客および仕入先の支払スケジュール明細行に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-159">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2056d-160">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="2056d-160">Payment schedule</span></span>            | <span data-ttu-id="2056d-161">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="2056d-161">msdyn_paymentschedules</span></span>          | <span data-ttu-id="2056d-162">このテンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-162">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="2056d-163">支払条件</span><span class="sxs-lookup"><span data-stu-id="2056d-163">Terms of payment</span></span>            | <span data-ttu-id="2056d-164">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="2056d-164">msdyn_paymentterms</span></span>              | <span data-ttu-id="2056d-165">このテンプレートは、顧客および仕入先の支払条件 (支払に関する条件) に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="2056d-165">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]

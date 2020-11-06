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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 36716c302d86bc5715798bf4cf4899f666d0872c
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997457"
---
# <a name="integrated-customer-master"></a><span data-ttu-id="4b92e-103">統合された顧客マスター</span><span class="sxs-lookup"><span data-stu-id="4b92e-103">Integrated customer master</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="4b92e-104">顧客データは、複数の Dynamics 365 アプリケーションでマスターできます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-104">Customer data can be mastered in more than one Dynamics 365 application.</span></span> <span data-ttu-id="4b92e-105">たとえば、顧客レコードは Dynamics 365 Sales (Dynamics 365のモデル駆動型アプリ) の営業活動から発生する場合があり、レコードは Dynamics 365 Commerce ( Finance and Operationsアプリの) 小売活動を通じて発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="4b92e-105">For example, a customer record can originate though sales activity in Dynamics 365 Sales (a model-driven app in Dynamics 365), or a record can originate through retail activity in Dynamics 365 Commerce (a Finance and Operations app).</span></span> <span data-ttu-id="4b92e-106">顧客データの発生元の場所を問わず、バックグラウンドで統合されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-106">No matter where where the customer data originates, it is integrated behind the scenes.</span></span> <span data-ttu-id="4b92e-107">統合された顧客マスターを使用すると、任意の Dynamics 365 アプリケーションに顧客データをマスタに分配することができ、Dynamics 365 application スイートを介して顧客の包括的なビューを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-107">Integrated customer master gives you the flexibility to master customer data in any Dynamics 365 application and provides a comprehensive view of the customer across the Dynamics 365 application suite.</span></span>

## <a name="customer-data-flow"></a><span data-ttu-id="4b92e-108">顧客データ フロー</span><span class="sxs-lookup"><span data-stu-id="4b92e-108">Customer data flow</span></span>

<span data-ttu-id="4b92e-109">*顧客* は、アプリケーションで明確に定義された概念です。</span><span class="sxs-lookup"><span data-stu-id="4b92e-109">*Customer* is a well-defined concept in applications.</span></span> <span data-ttu-id="4b92e-110">したがって、顧客データの統合は、2 つのアプリケーションの間で顧客の概念を調和させるだけです。</span><span class="sxs-lookup"><span data-stu-id="4b92e-110">Therefore, the integration of customer data just involves harmonizing the customer concept between the two applications.</span></span> <span data-ttu-id="4b92e-111">次の図は、顧客データ フローを示します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-111">The following illustration shows the customer data flow.</span></span>

![顧客データ フロー](media/dual-write-customer-data-flow.png)

<span data-ttu-id="4b92e-113">顧客は、商用 / 組織の顧客および消費者 / エンド ユーザーの 2 種類に大きく分類できます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-113">Customers can be broadly classified into two types: commercial/organizational customers and consumers/end users.</span></span> <span data-ttu-id="4b92e-114">これら 2 種類の顧客は、Finance and Operations と Common Data Service にて、異なる方法で格納および処理されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-114">These two types of customers are stored and handled differently in Finance and Operations and Common Data Service.</span></span>

<span data-ttu-id="4b92e-115">Finance and Operations では、商用 / 組織の顧客および消費者 / エンド ユーザーの両方が、 **CustTable** (CustCustomerV3Entity) という名前の単一のテーブルでマスターされ、 **タイプ** 属性に基づいて分類されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-115">In Finance and Operations, both commercial/organizational customers and consumers/end users are mastered in a single table that is named **CustTable** (CustCustomerV3Entity), and they are classified based on the **Type** attribute.</span></span> <span data-ttu-id="4b92e-116">( **タイプ** が **組織** に設定されている場合、顧客は商用 / 組織の顧客であり、 **タイプ** が **人材** に設定されている場合、顧客はコンシューマ / エンド ユーザーです。) 主な連絡担当者情報は、SMMContactPersonEntity エンティティを介して処理されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-116">(If **Type** is set to **Organization** , the customer is a commercial/organizational customer, and if **Type** is set to **Person** , the customer is a consumer/end user.) The primary contact person information is handled through the SMMContactPersonEntity entity.</span></span>

<span data-ttu-id="4b92e-117">Common Data Serviceでは、商取引 / 組織の顧客は口座エンティティで習得され、 **リレーションシップ タイプ** 属性が **顧客** に設定されている場合、顧客として識別されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-117">In Common Data Service, commercial/organizational customers are mastered in the Account entity and are identified as customers when the **RelationshipType** attribute is set to **Customer**.</span></span> <span data-ttu-id="4b92e-118">コンシューマ / エンド ユーザーと連絡担当者の両方が、連絡先エンティティによって表されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-118">Both consumers/end users and the contact person are represented by the Contact entity.</span></span> <span data-ttu-id="4b92e-119">コンシューマー / エンド ユーザーおよび連絡担当者の間を明確に分離するために、 **連絡先** エンティティには **販売可能** という名前のブール フラグがあります。</span><span class="sxs-lookup"><span data-stu-id="4b92e-119">To provide a clear separation between a consumer/end user and a contact person, the **Contact** entity has a Boolean flag that is named **Sellable**.</span></span> <span data-ttu-id="4b92e-120">**販売可能** が **True** の場合、連絡先はコンシューマー / エンド ユーザーであり、その連絡先に対して見積と注文を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-120">When **Sellable** is **True** , the contact is a consumer/end user, and quotations and orders can be created for that contact.</span></span> <span data-ttu-id="4b92e-121">**販売可能が** が **False** の場合、連絡先は顧客の主要な連絡担当者にすぎません。</span><span class="sxs-lookup"><span data-stu-id="4b92e-121">When **Sellable** is **False** , the contact is just a primary contact person of a customer.</span></span>

<span data-ttu-id="4b92e-122">販売不能な取引先担当者が見積または注文プロセスに参加する場合、 **販売可能** が **True** に設定され、取引先担当者に販売可能な取引先担当者としてフラグが設定されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-122">When a non-sellable contact participates in a quotation or order process, **Sellable** is set to **True** to flag the contact as a sellable contact.</span></span> <span data-ttu-id="4b92e-123">販売可能な取引先担当者になった連絡先は、引き続き販売可能な連絡先です。</span><span class="sxs-lookup"><span data-stu-id="4b92e-123">A contact that has become a sellable contact remains a sellable contact.</span></span>

## <a name="templates"></a><span data-ttu-id="4b92e-124">テンプレート</span><span class="sxs-lookup"><span data-stu-id="4b92e-124">Templates</span></span>

<span data-ttu-id="4b92e-125">顧客データには、顧客グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、顧客に関するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-125">Customer data includes all information about the customer, such as the customer group, addresses, contact information, payment profile, invoice profile, and loyalty status.</span></span> <span data-ttu-id="4b92e-126">次の表に示すように、エンティティ マップのコレクションは、顧客データ操作中に連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-126">A collection of entity maps works together during customer data interaction, as shown in the following table.</span></span>

<span data-ttu-id="4b92e-127">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="4b92e-127">Finance and Operations apps</span></span> | <span data-ttu-id="4b92e-128">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="4b92e-128">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="4b92e-129">説明</span><span class="sxs-lookup"><span data-stu-id="4b92e-129">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="4b92e-130">CDS 連絡先 V2</span><span class="sxs-lookup"><span data-stu-id="4b92e-130">CDS Contacts V2</span></span>             | <span data-ttu-id="4b92e-131">連絡先</span><span class="sxs-lookup"><span data-stu-id="4b92e-131">contacts</span></span>                        | <span data-ttu-id="4b92e-132">このテンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。</span><span class="sxs-lookup"><span data-stu-id="4b92e-132">This template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="4b92e-133">顧客グループ</span><span class="sxs-lookup"><span data-stu-id="4b92e-133">Customer groups</span></span>             | <span data-ttu-id="4b92e-134">msdyn_customergroups</span><span class="sxs-lookup"><span data-stu-id="4b92e-134">msdyn_customergroups</span></span>            | <span data-ttu-id="4b92e-135">このテンプレートは、顧客グループ情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-135">This template synchronizes customer group information.</span></span>
<span data-ttu-id="4b92e-136">顧客支払方法</span><span class="sxs-lookup"><span data-stu-id="4b92e-136">Customer payment method</span></span>     | <span data-ttu-id="4b92e-137">msdyn_customerpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="4b92e-137">msdyn_customerpaymentmethods</span></span>    | <span data-ttu-id="4b92e-138">このテンプレートは、顧客支払方法に関する情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-138">This template synchronizes customer payment method information.</span></span>
<span data-ttu-id="4b92e-139">顧客 V3</span><span class="sxs-lookup"><span data-stu-id="4b92e-139">Customers V3</span></span>                | <span data-ttu-id="4b92e-140">勘定</span><span class="sxs-lookup"><span data-stu-id="4b92e-140">accounts</span></span>                        | <span data-ttu-id="4b92e-141">このテンプレートは、商業および組織顧客の顧客マスター情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-141">This template synchronizes customer master information for commercial and organizational customers.</span></span>
<span data-ttu-id="4b92e-142">顧客 V3</span><span class="sxs-lookup"><span data-stu-id="4b92e-142">Customers V3</span></span>                | <span data-ttu-id="4b92e-143">連絡先</span><span class="sxs-lookup"><span data-stu-id="4b92e-143">contacts</span></span>                        | <span data-ttu-id="4b92e-144">このテンプレートは、消費者およびエンド ユーザーの顧客マスター データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-144">This template synchronizes customer master data for consumers and end users.</span></span>
<span data-ttu-id="4b92e-145">名前の接辞</span><span class="sxs-lookup"><span data-stu-id="4b92e-145">Name affixes</span></span>                | <span data-ttu-id="4b92e-146">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="4b92e-146">msdyn_nameaffixes</span></span>               | <span data-ttu-id="4b92e-147">このテンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-147">This template synchronizes name affixes reference data, for both customers and vendors.</span></span>
<span data-ttu-id="4b92e-148">支払期日明細行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="4b92e-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="4b92e-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="4b92e-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="4b92e-150">このテンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-150">This template synchronizes payment day lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="4b92e-151">支払期日 CDS</span><span class="sxs-lookup"><span data-stu-id="4b92e-151">Payment days CDS</span></span>            | <span data-ttu-id="4b92e-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="4b92e-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="4b92e-153">このテンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-153">This template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="4b92e-154">支払スケジュール行</span><span class="sxs-lookup"><span data-stu-id="4b92e-154">Payment schedule lines</span></span>      | <span data-ttu-id="4b92e-155">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="4b92e-155">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="4b92e-156">顧客および仕入先の支払スケジュール明細行に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-156">Syncs payment schedule lines reference data, for both customers and vendors.</span></span>
<span data-ttu-id="4b92e-157">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="4b92e-157">Payment schedule</span></span>            | <span data-ttu-id="4b92e-158">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="4b92e-158">msdyn_paymentschedules</span></span>          | <span data-ttu-id="4b92e-159">このテンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-159">This template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="4b92e-160">支払条件</span><span class="sxs-lookup"><span data-stu-id="4b92e-160">Terms of payment</span></span>            | <span data-ttu-id="4b92e-161">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="4b92e-161">msdyn_paymentterms</span></span>              | <span data-ttu-id="4b92e-162">このテンプレートは、顧客および仕入先の支払条件 (支払に関する条件) に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="4b92e-162">This template synchronizes payment terms (terms of payment) reference data, for both customers and vendors.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]

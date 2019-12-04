---
title: 統合済み仕入先マスター
description: このトピックでは、Finance and Operations アプリと Common Data Service 間の仕入先データの統合について説明します。
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
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770991"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="a5cd7-103">統合済み仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="a5cd7-103">Integrated vendor master</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5cd7-104">*仕入先*という用語は、サプライ チェーン プロセスの一部で、ビジネスに商品を供給するサプライヤー組織または個人事業主を指します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-104">The term *vendor* refers to a supplier organization or a sole proprietor that is part of the supply chain process, and that supplies goods for the business.</span></span> <span data-ttu-id="a5cd7-105">*仕入先*は、Finance and Operations アプリで確立された概念ですが、他の Dynamics 365 アプリには仕入先の概念は存在しません。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-105">Although *vendor* is an established concept in Finance and Operations apps, a vendor concept doesn't exist in other Dynamics 365 apps.</span></span> <span data-ttu-id="a5cd7-106">代わりに、一部の企業は顧客情報と仕入先情報の両方を格納するために、アカウント エンティティを過負荷にします。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-106">Instead, some businesses overload the Account entity to store both customer information and vendor information.</span></span> <span data-ttu-id="a5cd7-107">他の企業では、カスタム ベンダーの概念を使用します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-107">Other businesses use a custom vendor concept.</span></span> <span data-ttu-id="a5cd7-108">Common Data Service 統合は、これらの設計の両方をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-108">Common Data Service integration supports both these designs.</span></span> <span data-ttu-id="a5cd7-109">したがって、ビジネス シナリオに応じて、いずれかの設計を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-109">Therefore, you can enable either of the designs, depending on your business scenario.</span></span>

<span data-ttu-id="a5cd7-110">Finance and Operations アプリと他の Dynamics 365 アプリ間の仕入先データの統合により、データをマルチ マスターにできます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-110">Integration of vendor data between Finance and Operations apps and other Dynamics 365 apps lets you multi-master the data.</span></span> <span data-ttu-id="a5cd7-111">仕入先データの発生元にかかわらず、アプリケーションの境界およびインフラストラクチャの違いを越えてバックグラウンドで統合されます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-111">Regardless of where the vendor data originates, it's integrated behind the scenes across application boundaries and infrastructure differences.</span></span> 

### <a name="vendor-data-flow"></a><span data-ttu-id="a5cd7-112">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="a5cd7-112">Vendor data flow</span></span>

<span data-ttu-id="a5cd7-113">仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、顧客情報から仕入先情報を分離する場合は、新しい仕入先設計を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-113">If you want to use other Dynamics 365 apps for vendor mastering, and you want to isolate vendor information from customer information, you can use the new vendor design.</span></span>

![仕入先データ フロー](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="a5cd7-115">仕入先のマスタリングにその他の Dynamics 365 アプリを使用し、仕入先情報を格納するためアカウント エンティティを使用し続ける場合は、新しく拡張された仕入先設計を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-115">If you want to use other Dynamics 365 apps for vendor mastering, and you want to continue to use the Account entity to store vendor information, you can use the new extended vendor design.</span></span> <span data-ttu-id="a5cd7-116">この設計では、仕入先グループおよび仕入先転記プロファイルなどの拡張された仕入先情報が仕入先詳細に保存されます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-116">In this design, extended vendor information, such as the vendor group and vendor posting profile, are stored in the vendor detail.</span></span>

![拡張された仕入先データ フロー](media/dual-write-vendor-detail.jpg)

<span data-ttu-id="a5cd7-118">仕入先の連絡先情報は、顧客の連絡先情報に似ています。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-118">Vendor contact information resembles customer contact information.</span></span> <span data-ttu-id="a5cd7-119">その背後では、連絡担当者の情報が保存され、同じエンティティから取得されます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-119">Behind the scenes, the contact person's information is stored and retrieved from the same entities.</span></span>

## <a name="templates"></a><span data-ttu-id="a5cd7-120">テンプレート</span><span class="sxs-lookup"><span data-stu-id="a5cd7-120">Templates</span></span>

<span data-ttu-id="a5cd7-121">仕入先データには、仕入先グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、仕入先に関するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="a5cd7-122">次の表に示すように、エンティティ マップのコレクションは、仕入先データの操作中に連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-122">A collection of entity maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="a5cd7-123">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="a5cd7-123">Finance and Operations apps</span></span> | <span data-ttu-id="a5cd7-124">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="a5cd7-124">Other Dynamics 365 apps</span></span>         | <span data-ttu-id="a5cd7-125">説明</span><span class="sxs-lookup"><span data-stu-id="a5cd7-125">Description</span></span>
----------------------------|---------------------------------|------------
<span data-ttu-id="a5cd7-126">仕入先 V2</span><span class="sxs-lookup"><span data-stu-id="a5cd7-126">Vendor V2</span></span>               | <span data-ttu-id="a5cd7-127">口座</span><span class="sxs-lookup"><span data-stu-id="a5cd7-127">Account</span></span> | <span data-ttu-id="a5cd7-128">アカウント エンティティを使用して仕入先情報を格納する企業は、引き続き同じ方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-128">Businesses that use the Account entity to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="a5cd7-129">また、Finance and Operations アプリ統合により、明示的な仕入先機能を利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="a5cd7-130">仕入先 V2</span><span class="sxs-lookup"><span data-stu-id="a5cd7-130">Vendor V2</span></span>               | <span data-ttu-id="a5cd7-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="a5cd7-131">Msdyn\_vendors</span></span> | <span data-ttu-id="a5cd7-132">仕入先向けのカスタム ソリューションを使用する企業は、Finance and Operations アプリ統合の Common Data Service により導入されている直定の仕入先概念を利用できます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Common Data Service because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="a5cd7-133">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="a5cd7-133">Vendor groups</span></span> | <span data-ttu-id="a5cd7-134">msdyn_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="a5cd7-134">msdyn_vendorgroups</span></span> | <span data-ttu-id="a5cd7-135">このテンプレートは、仕入先グループ情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="a5cd7-136">仕入先支払方法</span><span class="sxs-lookup"><span data-stu-id="a5cd7-136">Vendor payment method</span></span> | <span data-ttu-id="a5cd7-137">msdyn_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="a5cd7-137">msdyn_vendorpaymentmethods</span></span> | <span data-ttu-id="a5cd7-138">このテンプレートは、仕入先支払方法に関する情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="a5cd7-139">CDS 連絡先 V2</span><span class="sxs-lookup"><span data-stu-id="a5cd7-139">CDS Contacts V2</span></span>             | <span data-ttu-id="a5cd7-140">連絡先</span><span class="sxs-lookup"><span data-stu-id="a5cd7-140">contacts</span></span>                        | <span data-ttu-id="a5cd7-141">[連絡先](dual-write-customer.md#cds-contacts-v2-to-contacts) テンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-141">The [contacts](dual-write-customer.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="a5cd7-142">支払スケジュール行</span><span class="sxs-lookup"><span data-stu-id="a5cd7-142">Payment schedule lines</span></span>      | <span data-ttu-id="a5cd7-143">msdyn_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="a5cd7-143">msdyn_paymentschedulelines</span></span>      | <span data-ttu-id="a5cd7-144">[支払スケジュール行](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) テンプレートは、顧客および仕入先の参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-144">The [payment schedule lines](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="a5cd7-145">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="a5cd7-145">Payment schedule</span></span>            | <span data-ttu-id="a5cd7-146">msdyn_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="a5cd7-146">msdyn_paymentschedules</span></span>          | <span data-ttu-id="a5cd7-147">[支払スケジュール](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) テンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-147">The [payment schedules](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a5cd7-148">支払期日明細行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="a5cd7-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="a5cd7-149">msdyn_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="a5cd7-149">msdyn_paymentdaylines</span></span>           | <span data-ttu-id="a5cd7-150">[支払期日明細行](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) テンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-150">The [payment day lines](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="a5cd7-151">支払期日 CDS</span><span class="sxs-lookup"><span data-stu-id="a5cd7-151">Payment days CDS</span></span>            | <span data-ttu-id="a5cd7-152">msdyn_paymentdays</span><span class="sxs-lookup"><span data-stu-id="a5cd7-152">msdyn_paymentdays</span></span>               | <span data-ttu-id="a5cd7-153">[支払期日](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) テンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-153">The [payment days](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a5cd7-154">支払条件</span><span class="sxs-lookup"><span data-stu-id="a5cd7-154">Terms of payment</span></span>            | <span data-ttu-id="a5cd7-155">msdyn_paymentterms</span><span class="sxs-lookup"><span data-stu-id="a5cd7-155">msdyn_paymentterms</span></span>              | <span data-ttu-id="a5cd7-156">[支払条件](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) テンプレートは、顧客および仕入先の支払条件に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-156">The [terms of payment](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="a5cd7-157">名前の接辞</span><span class="sxs-lookup"><span data-stu-id="a5cd7-157">Name affixes</span></span>                | <span data-ttu-id="a5cd7-158">msdyn_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="a5cd7-158">msdyn_nameaffixes</span></span>               | <span data-ttu-id="a5cd7-159">[名前の接辞](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) テンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="a5cd7-159">The [name affixes](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]

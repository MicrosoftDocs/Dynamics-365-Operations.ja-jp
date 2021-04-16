---
title: 統合された仕入先マスター
description: このトピックでは、Finance and Operations アプリと Dataverse 間の仕入先データの統合について説明します。
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f57a20ed56a761894b2cedf8835310dac098b098
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750621"
---
# <a name="integrated-vendor-master"></a><span data-ttu-id="1d855-103">統合された仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="1d855-103">Integrated vendor master</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="1d855-104">*仕入先* という用語は、サプライヤー組織、または会社に商品やサービスを提供している唯一の個人事業主を指します。</span><span class="sxs-lookup"><span data-stu-id="1d855-104">The term *vendor* refers to a supplier organization, or a sole proprietor who supplies goods or services to a business.</span></span> <span data-ttu-id="1d855-105">*仕入先* は、Microsoft Dynamics 365 Supply Chain Management で確立されていますが、Dynamics 365 のモデル駆動型アプリには仕入先の概念は存在しません。</span><span class="sxs-lookup"><span data-stu-id="1d855-105">Although *vendor* is an established concept in Microsoft Dynamics 365 Supply Chain Management, no vendor concept exists in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="1d855-106">ただし、**取引先企業/連絡先** テーブルをオーバーロードして、仕入先情報を格納することができます。</span><span class="sxs-lookup"><span data-stu-id="1d855-106">However, you can overload the **Account/Contact** table to store vendor information.</span></span> <span data-ttu-id="1d855-107">この統合型仕入先マスターは、Dynamics 365のモデル駆動アプリケーションで明示的なベンダー概念を導入します。</span><span class="sxs-lookup"><span data-stu-id="1d855-107">The integrated vendor master introduces an explicit vendor concept in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="1d855-108">新しい仕入先設計を使用するか、仕入先データを **取引先企業/連絡先** テーブルに格納することができます。</span><span class="sxs-lookup"><span data-stu-id="1d855-108">You can either use the new vendor design or store vendor data in the **Account/Contact** table.</span></span> <span data-ttu-id="1d855-109">デュアル書き込みでは、両方の手法がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1d855-109">Dual-write supports both approaches.</span></span>

<span data-ttu-id="1d855-110">どちらの手法でも、仕入先データは Dynamics 365 Supply Chain Management、Dynamics 365 Sales、Dynamics 365 Field Service、および Power Apps の各ポータル間で統合されます。</span><span class="sxs-lookup"><span data-stu-id="1d855-110">In both approaches, the vendor data is integrated between Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service, and Power Apps portals.</span></span> <span data-ttu-id="1d855-111">Supply Chain Management では、購買要求や発注書などのワークフローでデータを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d855-111">In Supply Chain Management, the data is available for workflows such as purchase requisitions and purchase orders.</span></span>

## <a name="vendor-data-flow"></a><span data-ttu-id="1d855-112">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="1d855-112">Vendor data flow</span></span>

<span data-ttu-id="1d855-113">仕入先データを Dataverse の **取引先企業/連絡先** テーブルに格納しない場合は、新規仕入先設計を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d855-113">If you don't want to store vendor data in the **Account/Contact** table in Dataverse, you can use the new vendor design.</span></span>

![仕入先データ フロー](media/dual-write-vendor-data-flow.png)

<span data-ttu-id="1d855-115">**取引先企業/連絡先** テーブルで仕入先データを格納し続ける場合は、この拡張仕入先設計を使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d855-115">If you want to continue to store vendor data in the **Account/Contact** table, you can use the extended vendor design.</span></span> <span data-ttu-id="1d855-116">拡張仕入先設計を使用するには、デュアル書き込みソリューション パッケージで仕入先ワークフローをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d855-116">To use the extended vendor design, you must configure the vendor workflows in the dual-write solution package.</span></span> <span data-ttu-id="1d855-117">詳細については、[仕入先設計間での切り替え](vendor-switch.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d855-117">For more information, see [Switch between vendor designs](vendor-switch.md).</span></span>

![拡張された仕入先データ フロー](media/dual-write-vendor-detail.jpg)

> [!TIP]
> <span data-ttu-id="1d855-119">セルフサービス仕入先の Power Apps ポータルを使用している場合は、その仕入先情報は Finance and Operations アプリに直接フローできます。</span><span class="sxs-lookup"><span data-stu-id="1d855-119">If you're using Power Apps portals for self-service vendors, the vendor information can flow directly to Finance and Operations apps.</span></span>

## <a name="templates"></a><span data-ttu-id="1d855-120">テンプレート</span><span class="sxs-lookup"><span data-stu-id="1d855-120">Templates</span></span>

<span data-ttu-id="1d855-121">仕入先データには、仕入先グループ、住所、連絡先情報、支払プロファイル、請求書プロファイル、およびロイヤルティ ステータスなど、仕入先に関するすべての情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1d855-121">Vendor data includes all information about the vendor, such as the vendor group, addresses, contact information, payment profile, and invoice profile.</span></span> <span data-ttu-id="1d855-122">次の表に示すように、テーブル マップのコレクションは、仕入先データの操作中に連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="1d855-122">A collection of table maps work together during vendor data interaction, as shown in the following table.</span></span>

<span data-ttu-id="1d855-123">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="1d855-123">Finance and Operations apps</span></span> | <span data-ttu-id="1d855-124">その他の Dynamics 365 アプリ</span><span class="sxs-lookup"><span data-stu-id="1d855-124">Other Dynamics 365 apps</span></span>     | <span data-ttu-id="1d855-125">説明</span><span class="sxs-lookup"><span data-stu-id="1d855-125">Description</span></span>
----------------------------|-----------------------------|------------
<span data-ttu-id="1d855-126">仕入先 V2</span><span class="sxs-lookup"><span data-stu-id="1d855-126">Vendor V2</span></span>                   | <span data-ttu-id="1d855-127">口座</span><span class="sxs-lookup"><span data-stu-id="1d855-127">Account</span></span>                     | <span data-ttu-id="1d855-128">取引先企業テーブルを使用して仕入先情報を格納する企業は、引き続き同じ方法で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d855-128">Businesses that use the Account table to store vendor information can continue to use it in the same way.</span></span> <span data-ttu-id="1d855-129">また、Finance and Operations アプリ統合により、明示的な仕入先機能を利用することもできます。</span><span class="sxs-lookup"><span data-stu-id="1d855-129">They can also take advantage of the explicit vendor functionality that is coming because of Finance and Operations apps integration.</span></span>
<span data-ttu-id="1d855-130">仕入先 V2</span><span class="sxs-lookup"><span data-stu-id="1d855-130">Vendor V2</span></span>                   | <span data-ttu-id="1d855-131">Msdyn\_vendors</span><span class="sxs-lookup"><span data-stu-id="1d855-131">Msdyn\_vendors</span></span>              | <span data-ttu-id="1d855-132">仕入先向けのカスタム ソリューションを使用する企業は、Finance and Operations アプリ統合による Dataverse で導入されている直定の仕入先概念を利用できます。</span><span class="sxs-lookup"><span data-stu-id="1d855-132">Businesses that use a custom solution for vendors can take advantage of the out-of-box vendor concept that is being introduced in Dataverse because of Finance and Operations apps integration.</span></span> 
<span data-ttu-id="1d855-133">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="1d855-133">Vendor groups</span></span>               | <span data-ttu-id="1d855-134">msdyn\_vendorgroups</span><span class="sxs-lookup"><span data-stu-id="1d855-134">msdyn\_vendorgroups</span></span>         | <span data-ttu-id="1d855-135">このテンプレートは、仕入先グループ情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-135">This template synchronizes vendor group information.</span></span>
<span data-ttu-id="1d855-136">仕入先支払方法</span><span class="sxs-lookup"><span data-stu-id="1d855-136">Vendor payment method</span></span>       | <span data-ttu-id="1d855-137">msdyn\_vendorpaymentmethods</span><span class="sxs-lookup"><span data-stu-id="1d855-137">msdyn\_vendorpaymentmethods</span></span> | <span data-ttu-id="1d855-138">このテンプレートは、仕入先支払方法に関する情報を同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-138">This template synchronizes vendor payment method information.</span></span>
<span data-ttu-id="1d855-139">CDS 連絡先 V2</span><span class="sxs-lookup"><span data-stu-id="1d855-139">CDS Contacts V2</span></span>             | <span data-ttu-id="1d855-140">連絡先</span><span class="sxs-lookup"><span data-stu-id="1d855-140">contacts</span></span>                    | <span data-ttu-id="1d855-141">[連絡先](customer-mapping.md#cds-contacts-v2-to-contacts) テンプレートでは、顧客と仕入先の両方について、基本、二次、三次の連絡先情報がすべて同期されます。</span><span class="sxs-lookup"><span data-stu-id="1d855-141">The [contacts](customer-mapping.md#cds-contacts-v2-to-contacts) template synchronizes all primary, secondary, and tertiary contact information, for both customers and vendors.</span></span>
<span data-ttu-id="1d855-142">支払スケジュール行</span><span class="sxs-lookup"><span data-stu-id="1d855-142">Payment schedule lines</span></span>      | <span data-ttu-id="1d855-143">msdyn\_paymentschedulelines</span><span class="sxs-lookup"><span data-stu-id="1d855-143">msdyn\_paymentschedulelines</span></span> | <span data-ttu-id="1d855-144">[支払スケジュール行](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) テンプレートは、顧客および仕入先の参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-144">The [payment schedule lines](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) template synchronizes reference data for customers and vendors.</span></span>
<span data-ttu-id="1d855-145">支払スケジュール</span><span class="sxs-lookup"><span data-stu-id="1d855-145">Payment schedule</span></span>            | <span data-ttu-id="1d855-146">msdyn\_paymentschedules</span><span class="sxs-lookup"><span data-stu-id="1d855-146">msdyn\_paymentschedules</span></span>     | <span data-ttu-id="1d855-147">[支払スケジュール](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) テンプレートは、顧客および仕入先の支払スケジュールに関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-147">The [payment schedules](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) template synchronizes payment schedule reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1d855-148">支払期日明細行 CDS V2</span><span class="sxs-lookup"><span data-stu-id="1d855-148">Payment day lines CDS V2</span></span>    | <span data-ttu-id="1d855-149">msdyn\_paymentdaylines</span><span class="sxs-lookup"><span data-stu-id="1d855-149">msdyn\_paymentdaylines</span></span>      | <span data-ttu-id="1d855-150">[支払期日明細行](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) テンプレートは、顧客および仕入先の支払期日明細行に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-150">The [payment day lines](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) template synchronizes payment day lines reference data for customers and vendors.</span></span>
<span data-ttu-id="1d855-151">支払期日 CDS</span><span class="sxs-lookup"><span data-stu-id="1d855-151">Payment days CDS</span></span>            | <span data-ttu-id="1d855-152">msdyn\_paymentdays</span><span class="sxs-lookup"><span data-stu-id="1d855-152">msdyn\_paymentdays</span></span>          | <span data-ttu-id="1d855-153">[支払期日](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) テンプレートは、顧客および仕入先の支払期日に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-153">The [payment days](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) template synchronizes payment days reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1d855-154">支払条件</span><span class="sxs-lookup"><span data-stu-id="1d855-154">Terms of payment</span></span>            | <span data-ttu-id="1d855-155">msdyn\_paymentterms</span><span class="sxs-lookup"><span data-stu-id="1d855-155">msdyn\_paymentterms</span></span>         | <span data-ttu-id="1d855-156">[支払条件](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) テンプレートは、顧客および仕入先の支払条件に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-156">The [terms of payment](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) template synchronizes payment terms reference data, for both customers and vendors.</span></span>
<span data-ttu-id="1d855-157">名前の接辞</span><span class="sxs-lookup"><span data-stu-id="1d855-157">Name affixes</span></span>                | <span data-ttu-id="1d855-158">msdyn\_nameaffixes</span><span class="sxs-lookup"><span data-stu-id="1d855-158">msdyn\_nameaffixes</span></span>          | <span data-ttu-id="1d855-159">[名前の接辞](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) テンプレートは、顧客および仕入先の名前の接辞に関する参照データを同期します。</span><span class="sxs-lookup"><span data-stu-id="1d855-159">The [name affixes](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) template synchronizes name affixes reference data, for both customers and vendors.</span></span>

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
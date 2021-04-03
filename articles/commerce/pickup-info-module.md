---
title: 集荷情報モジュール
description: このトピックでは、集荷情報モジュールと、Microsoft Dynamics 365 Commerce のチェックアウト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263183"
---
# <a name="pickup-information-module"></a><span data-ttu-id="79213-103">集荷情報モジュール</span><span class="sxs-lookup"><span data-stu-id="79213-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="79213-104">このトピックでは、集荷情報モジュールと、Microsoft Dynamics 365 Commerce のチェックアウト ページにそれを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="79213-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="79213-105">集荷情報モジュールをチェックアウト モジュールで使用して、注文集荷情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="79213-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="79213-106">顧客は、使用可能な集荷日時を表示したり、注文を集荷するための適切な時間を選択したりできます。</span><span class="sxs-lookup"><span data-stu-id="79213-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="79213-107">たとえば、顧客は 3 月 21 日の午後 3 時にサンフランシスコの店舗から注文を受け取ることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="79213-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="79213-108">Commerce 本社では、適切な店舗の集荷時間帯がコンフィギュレーションされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="79213-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="79213-109">詳細については、[顧客集荷の時間スロットの作成と更新](dev-itpro/pickup-timeslots.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79213-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="79213-110">集荷情報モジュールがチェックアウト ページに作成されていても、集荷用に選択されている店舗に対して時間帯が定義されていない場合は、モジュールに情報が表示されますが、ユーザーは時間帯時間帯を選択できません。</span><span class="sxs-lookup"><span data-stu-id="79213-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="79213-111">時間帯は省略可能であり、注文する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="79213-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="79213-112">複数の店舗で集荷するために複数の品目が選択されている場合は、集荷モジュールを使用して、時間帯を使用できる場合に、ユーザーが各店舗の時間帯を選択できます。</span><span class="sxs-lookup"><span data-stu-id="79213-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="79213-113">時間帯とチェックアウト集荷情報モジュールのサポートは、Dynamics 365 Commerce バージョン 10.0.15 以降で利用できます。</span><span class="sxs-lookup"><span data-stu-id="79213-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="79213-114">次の図は、チェックアウト ページの集荷情報モジュールを使用した時間帯の選択例を示しています。</span><span class="sxs-lookup"><span data-stu-id="79213-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![チェックアウト ページの集荷情報モジュールの例](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="79213-116">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="79213-116">Module properties</span></span>

- <span data-ttu-id="79213-117">**見出し** – モジュールの見出しを入力します。</span><span class="sxs-lookup"><span data-stu-id="79213-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="79213-118">発注後に時間帯情報を表示する</span><span class="sxs-lookup"><span data-stu-id="79213-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="79213-119">注文が行われると、選択した時間帯に関する情報が [注文確認モジュール](order-confirmation-module.md)と[注文明細モジュール](account-management.md#order-details-page)に表示されます。</span><span class="sxs-lookup"><span data-stu-id="79213-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="79213-120">この 2 つのモジュールには、**時間帯情報の表示** プロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="79213-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="79213-121">注文プロセス中に選択した時間帯を表示できるようにするには、このプロパティを **True** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="79213-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="79213-122">チェックアウト集荷情報モジュールをページに追加する</span><span class="sxs-lookup"><span data-stu-id="79213-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="79213-123">集荷情報モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79213-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="79213-124">次の図は、集配明細行品目の時間帯を含む電子商取引のチェックアウト ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="79213-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![集配明細行品目の時間帯を含む電子商取引のチェックアウト ページの例](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="79213-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="79213-126">Additional resources</span></span>

[<span data-ttu-id="79213-127">顧客集荷の時間スロットの作成と更新</span><span class="sxs-lookup"><span data-stu-id="79213-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="79213-128">チェックアウト モジュール</span><span class="sxs-lookup"><span data-stu-id="79213-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="79213-129">注文確認モジュール</span><span class="sxs-lookup"><span data-stu-id="79213-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="79213-130">注文詳細のモジュール</span><span class="sxs-lookup"><span data-stu-id="79213-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: 既定の顧客の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce でチャネルを作成する時に使用する既定の顧客を作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ba1d10a897f349703737068d772423f7d0292944
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413667"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="065df-103">既定の顧客の作成</span><span class="sxs-lookup"><span data-stu-id="065df-103">Create a default customer</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="065df-104">このトピックでは、Microsoft Dynamics 365 Commerce でチャネルを作成する時に使用する既定の顧客を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="065df-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="065df-105">概要</span><span class="sxs-lookup"><span data-stu-id="065df-105">Overview</span></span>

<span data-ttu-id="065df-106">チャネルを作成する場合、既定の顧客を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="065df-106">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="065df-107">顧客グループおよび顧客のアドレス帳を最初に作成した後に、簡単に既定の顧客を作成できます。</span><span class="sxs-lookup"><span data-stu-id="065df-107">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="065df-108">顧客グループの作成</span><span class="sxs-lookup"><span data-stu-id="065df-108">Create a customer group</span></span>

<span data-ttu-id="065df-109">顧客グループがまだ存在しない場合、1 つ作成できます。</span><span class="sxs-lookup"><span data-stu-id="065df-109">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="065df-110">たとえば、卸売、小売り、インターネット、従業員など、異なる顧客グループを表すグループがあります。</span><span class="sxs-lookup"><span data-stu-id="065df-110">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="065df-111">顧客グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="065df-111">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="065df-112">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 顧客 \> 顧客グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="065df-112">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="065df-113">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-113">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="065df-114">**顧客グループ** ボックスに、顧客グループ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-114">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="065df-115">**説明** ボックスに、適切な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-115">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="065df-116">**支払条件** ボックスに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-116">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="065df-117">**請求書の期日から支払日までの時間** ボックスに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-117">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="065df-118">該当する場合は、**既定の税グループ** ボックスに、税グループを入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-118">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="065df-119">該当する場合は、**税込価格** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="065df-119">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="065df-120">該当する場合は、**既定の損金処理の理由** ボックスに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-120">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="065df-121">次の図は、コンフィギュレーションされた複数の顧客グループを示しています。</span><span class="sxs-lookup"><span data-stu-id="065df-121">The following image shows several configured customer groups.</span></span>

![顧客グループ](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="065df-123">顧客のアドレス帳の作成</span><span class="sxs-lookup"><span data-stu-id="065df-123">Create a customer address book</span></span>

<span data-ttu-id="065df-124">顧客はアドレス帳に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="065df-124">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="065df-125">まだ作成されていない場合、1 つ作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="065df-125">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="065df-126">顧客のアドレス帳を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="065df-126">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="065df-127">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> アドレス帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="065df-127">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="065df-128">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-128">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="065df-129">**名前** ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-129">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="065df-130">**説明** ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-130">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="065df-131">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-131">On the action pane, select **Save**.</span></span>

<span data-ttu-id="065df-132">次の図は、アドレス帳の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="065df-132">The following image shows an example address book.</span></span>

![アドレス帳](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="065df-134">既定の顧客の作成</span><span class="sxs-lookup"><span data-stu-id="065df-134">Create a default customer</span></span>

<span data-ttu-id="065df-135">既定の顧客を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="065df-135">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="065df-136">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 顧客 \> すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="065df-136">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="065df-137">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-137">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="065df-138">**タイプ** ドロップダウン リストで、「個人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-138">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="065df-139">**顧客アカウント** ドロップ ダウン リストで、アカウント番号を選択または入力します (たとえば、「100001」)。</span><span class="sxs-lookup"><span data-stu-id="065df-139">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="065df-140">**名** ドロップダウン リストで、名前を選択または入力します (たとえば、「既定」)。</span><span class="sxs-lookup"><span data-stu-id="065df-140">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="065df-141">**ミドル ネーム** ドロップダウン リストで、名前を選択または入力します (たとえば、「小売」)。</span><span class="sxs-lookup"><span data-stu-id="065df-141">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="065df-142">**姓** ドロップダウン リストで、名前を選択または入力します (たとえば、「顧客」)。</span><span class="sxs-lookup"><span data-stu-id="065df-142">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="065df-143">**通貨** ドロップダウン リストで、通貨を選択または入力します (たとえば、「USD」)。</span><span class="sxs-lookup"><span data-stu-id="065df-143">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="065df-144">**通貨** ドロップダウン リストで、以前に作成した顧客グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-144">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="065df-145">**アドレス帳** ドロップダウン リストで、既存の顧客のアドレス帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="065df-145">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="065df-146">**保存** を選択して保存し、新しい顧客の顧客詳細画面に戻ります。</span><span class="sxs-lookup"><span data-stu-id="065df-146">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="065df-147">既定の顧客の住所を追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="065df-147">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="065df-148">次の図は、顧客作成の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="065df-148">The following image shows an example of customer creation.</span></span>

![既定の顧客の作成](media/default-customer-creation.png)

<span data-ttu-id="065df-150">次の図は、既定の顧客のコンフィギュレーションを示しています。</span><span class="sxs-lookup"><span data-stu-id="065df-150">The following image shows a default customer configuration.</span></span>

![顧客コンフィギュレーションのサンプル](media/default-customer-configuration1.png)

<span data-ttu-id="065df-152">顧客詳細画面の既定値のほとんどはそのままにすることができますが、2 つの値は変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="065df-152">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="065df-153">顧客詳細画面で、**販売注文の既定値** を展開します。</span><span class="sxs-lookup"><span data-stu-id="065df-153">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="065df-154">**サイト** ドロップダウン リストで、コンフィギュレーション済みのサイトを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-154">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="065df-155">**倉庫** ドロップダウン リストで、コンフィギュレーション済みの倉庫を選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="065df-155">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="065df-156">次の図は、顧客のコンフィギュレーションの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="065df-156">The following image shows an example customer configuration.</span></span>

![顧客コンフィギュレーションの例](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="065df-158">追加リソース</span><span class="sxs-lookup"><span data-stu-id="065df-158">Additional resources</span></span>

[<span data-ttu-id="065df-159">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="065df-159">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="065df-160">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="065df-160">Channel setup prerequisites</span></span>](channels-prerequisites.md)

---
title: 既定の顧客の作成
description: このトピックでは、Microsoft Dynamics 365 Commerce でチャネルを作成する時に使用する既定の顧客を作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: ecdf4e5618d3397527bf83977857fbe3f8dbb265
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799182"
---
# <a name="create-a-default-customer"></a><span data-ttu-id="2f586-103">既定の顧客の作成</span><span class="sxs-lookup"><span data-stu-id="2f586-103">Create a default customer</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2f586-104">このトピックでは、Microsoft Dynamics 365 Commerce でチャネルを作成する時に使用する既定の顧客を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2f586-104">This topic describes how to create a default customer to use when creating a channel in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2f586-105">チャネルを作成する場合、既定の顧客を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f586-105">When creating a channel, you will need to provide a default customer.</span></span> <span data-ttu-id="2f586-106">顧客グループおよび顧客のアドレス帳を最初に作成した後に、簡単に既定の顧客を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2f586-106">A default customer can easily be created after first creating the customer group and customer address book.</span></span>

## <a name="create-a-customer-group"></a><span data-ttu-id="2f586-107">顧客グループの作成</span><span class="sxs-lookup"><span data-stu-id="2f586-107">Create a customer group</span></span>

<span data-ttu-id="2f586-108">顧客グループがまだ存在しない場合、1 つ作成できます。</span><span class="sxs-lookup"><span data-stu-id="2f586-108">If no customer groups exist yet, you can create one.</span></span> <span data-ttu-id="2f586-109">たとえば、卸売、小売り、インターネット、従業員など、異なる顧客グループを表すグループがあります。</span><span class="sxs-lookup"><span data-stu-id="2f586-109">Examples may be groups to represent different customer groups, such as wholesale, retail, Internet, Employees, etc.</span></span>

<span data-ttu-id="2f586-110">顧客グループを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2f586-110">To create a customer group, follow these steps.</span></span>

1. <span data-ttu-id="2f586-111">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 顧客 \> 顧客グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f586-111">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> Customer groups**.</span></span>
1. <span data-ttu-id="2f586-112">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-112">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2f586-113">**顧客グループ** ボックスに、顧客グループ ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-113">In the **Customer group** box, enter a customer group ID.</span></span>
1. <span data-ttu-id="2f586-114">**説明** ボックスに、適切な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-114">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="2f586-115">**支払条件** ボックスに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-115">In the **Terms of payment** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="2f586-116">**請求書の期日から支払日までの時間** ボックスに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-116">In the **Time between invoice due date and payment date** box, enter an appropriate value.</span></span>
1. <span data-ttu-id="2f586-117">該当する場合は、**既定の税グループ** ボックスに、税グループを入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-117">In the **Default tax group** box, enter a tax group if applicable.</span></span>
1. <span data-ttu-id="2f586-118">該当する場合は、**税込価格** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2f586-118">Select the **Prices include sales tax** check box if applicable.</span></span>
1. <span data-ttu-id="2f586-119">該当する場合は、**既定の損金処理の理由** ボックスに、適切な値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-119">In the **Default write-off reason** box, enter an appropriate value, if applicable.</span></span>

<span data-ttu-id="2f586-120">次の図は、コンフィギュレーションされた複数の顧客グループを示しています。</span><span class="sxs-lookup"><span data-stu-id="2f586-120">The following image shows several configured customer groups.</span></span>

![顧客グループ](media/customer-groups.png)

## <a name="create-a-customer-address-book"></a><span data-ttu-id="2f586-122">顧客のアドレス帳の作成</span><span class="sxs-lookup"><span data-stu-id="2f586-122">Create a customer address book</span></span>

<span data-ttu-id="2f586-123">顧客はアドレス帳に関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f586-123">A customer needs to be associated with an address book.</span></span> <span data-ttu-id="2f586-124">まだ作成されていない場合、1 つ作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f586-124">If one has not yet been created, then you will need to create one.</span></span>

<span data-ttu-id="2f586-125">顧客のアドレス帳を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2f586-125">To create a customer address book, follow these steps.</span></span>

1. <span data-ttu-id="2f586-126">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> チャネル設定 \> アドレス帳** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f586-126">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Address Books**.</span></span>
1. <span data-ttu-id="2f586-127">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-127">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2f586-128">**名前** ボックスに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-128">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="2f586-129">**説明** ボックスに、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-129">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="2f586-130">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-130">On the action pane, select **Save**.</span></span>

<span data-ttu-id="2f586-131">次の図は、アドレス帳の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f586-131">The following image shows an example address book.</span></span>

![アドレス帳](media/address-book.png)

## <a name="create-a-default-customer"></a><span data-ttu-id="2f586-133">既定の顧客の作成</span><span class="sxs-lookup"><span data-stu-id="2f586-133">Create a default customer</span></span>

<span data-ttu-id="2f586-134">既定の顧客を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2f586-134">To create a default customer, follow these steps.</span></span>

1. <span data-ttu-id="2f586-135">ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 顧客 \> すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2f586-135">In the navigation pane, go to **Modules \> Retail and commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="2f586-136">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-136">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="2f586-137">**タイプ** ドロップダウン リストで、「個人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-137">In the **Type** drop-down list, select "Person".</span></span>
1. <span data-ttu-id="2f586-138">**顧客アカウント** ドロップ ダウン リストで、アカウント番号を選択または入力します (たとえば、「100001」)。</span><span class="sxs-lookup"><span data-stu-id="2f586-138">In the **Customer account** drop-down list, select or enter an account number (for example, "100001").</span></span>
1. <span data-ttu-id="2f586-139">**名** ドロップダウン リストで、名前を選択または入力します (たとえば、「既定」)。</span><span class="sxs-lookup"><span data-stu-id="2f586-139">In the **First name** drop-down list, select or enter a name (for example, "Default").</span></span>
1. <span data-ttu-id="2f586-140">**ミドル ネーム** ドロップダウン リストで、名前を選択または入力します (たとえば、「小売」)。</span><span class="sxs-lookup"><span data-stu-id="2f586-140">In the **Middle name** drop-down list, select or enter a name (for example, "Retail").</span></span>
1. <span data-ttu-id="2f586-141">**姓** ドロップダウン リストで、名前を選択または入力します (たとえば、「顧客」)。</span><span class="sxs-lookup"><span data-stu-id="2f586-141">In the **Last name** drop-down list, select or enter a name (for example, "Customer").</span></span>
1. <span data-ttu-id="2f586-142">**通貨** ドロップダウン リストで、通貨を選択または入力します (たとえば、「USD」)。</span><span class="sxs-lookup"><span data-stu-id="2f586-142">In the **Currency** drop-down list, select or enter a currency (for example, "USD").</span></span>
1. <span data-ttu-id="2f586-143">**通貨** ドロップダウン リストで、以前に作成した顧客グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-143">In the **Currency** drop-down list, select the customer group created previously.</span></span>
1. <span data-ttu-id="2f586-144">**アドレス帳** ドロップダウン リストで、既存の顧客のアドレス帳を選択します。</span><span class="sxs-lookup"><span data-stu-id="2f586-144">In the **Address books**  drop-down list, select an existing customer address book.</span></span>
1. <span data-ttu-id="2f586-145">**保存** を選択して保存し、新しい顧客の顧客詳細画面に戻ります。</span><span class="sxs-lookup"><span data-stu-id="2f586-145">Select **Save** to save and return to customer details screen for the new customer.</span></span>

> [!NOTE]
> <span data-ttu-id="2f586-146">既定の顧客の住所を追加する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2f586-146">It is not necessary to add an address for a default customer.</span></span>

<span data-ttu-id="2f586-147">次の図は、顧客作成の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f586-147">The following image shows an example of customer creation.</span></span>

![既定の顧客の作成](media/default-customer-creation.png)

<span data-ttu-id="2f586-149">次の図は、既定の顧客のコンフィギュレーションを示しています。</span><span class="sxs-lookup"><span data-stu-id="2f586-149">The following image shows a default customer configuration.</span></span>

![顧客コンフィギュレーションのサンプル](media/default-customer-configuration1.png)

<span data-ttu-id="2f586-151">顧客詳細画面の既定値のほとんどはそのままにすることができますが、2 つの値は変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f586-151">Most of the default values on the customer detials screen can remain, but two values should be changed.</span></span>

1. <span data-ttu-id="2f586-152">顧客詳細画面で、**販売注文の既定値** を展開します。</span><span class="sxs-lookup"><span data-stu-id="2f586-152">On the customer details screen, expand **Sales order defaults**.</span></span>
1. <span data-ttu-id="2f586-153">**サイト** ドロップダウン リストで、コンフィギュレーション済みのサイトを選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-153">In the **Site** drop-down list, select or enter a pre-configured site.</span></span>
1. <span data-ttu-id="2f586-154">**倉庫** ドロップダウン リストで、コンフィギュレーション済みの倉庫を選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="2f586-154">In the **Warehouse** drop-down list, and select or enter a pre-configured warehouse.</span></span>

<span data-ttu-id="2f586-155">次の図は、顧客のコンフィギュレーションの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="2f586-155">The following image shows an example customer configuration.</span></span>

![顧客コンフィギュレーションの例](media/default-customer-configuration2.png)

## <a name="additional-resources"></a><span data-ttu-id="2f586-157">追加リソース</span><span class="sxs-lookup"><span data-stu-id="2f586-157">Additional resources</span></span>

[<span data-ttu-id="2f586-158">チャネルの概要</span><span class="sxs-lookup"><span data-stu-id="2f586-158">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="2f586-159">チャネル設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="2f586-159">Channel setup prerequisites</span></span>](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

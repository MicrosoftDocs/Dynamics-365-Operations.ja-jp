---
title: 仕入先勘定の作成
description: この手順では、仕入先勘定の作成方法と住所および連絡先情報の追加方法を示します。
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017210"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="c3240-103">仕入先勘定の作成</span><span class="sxs-lookup"><span data-stu-id="c3240-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c3240-104">この手順では、仕入先勘定の作成方法と住所および連絡先情報の追加方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c3240-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="c3240-105">この手順では、購買目的および財務目的のためのすべてのフィールドを設定する方法は表示されません。</span><span class="sxs-lookup"><span data-stu-id="c3240-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="c3240-106">これらのフィールドについての詳細は、フィールドの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3240-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="c3240-107">デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="c3240-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c3240-108">通常、仕入先勘定は、調達担当者または売掛金勘定担当者によって作成されます。</span><span class="sxs-lookup"><span data-stu-id="c3240-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="c3240-109">仕入先勘定の作成</span><span class="sxs-lookup"><span data-stu-id="c3240-109">Create a vendor account</span></span>
1. <span data-ttu-id="c3240-110">**ナビゲーション ウィンドウ > モジュール > 調達 > 仕入先 > すべての仕入先** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c3240-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="c3240-111">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3240-111">Click **New**.</span></span>
3. <span data-ttu-id="c3240-112">**仕入先口座** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="c3240-113">フィールドには自動的に値を入力できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3240-113">The value may be populated automatically.</span></span> <span data-ttu-id="c3240-114">その場合、この手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="c3240-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="c3240-115">個人または組織の仕入先勘定を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c3240-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="c3240-116">この操作は、フィールドが使用可能になるときに影響します。</span><span class="sxs-lookup"><span data-stu-id="c3240-116">This will affect which fields are available.</span></span> <span data-ttu-id="c3240-117">この例では、組織の仕入先口座を作成します。</span><span class="sxs-lookup"><span data-stu-id="c3240-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="c3240-118">**名前** フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3240-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="c3240-119">仕入先が既にシステムに登録されている当事者である場合、このフィールドでドロップダウンを使用し、仕入先を選択できます。また、新しい仕入先口座では、既に登録されている住所と連絡先情報を継承します。</span><span class="sxs-lookup"><span data-stu-id="c3240-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="c3240-120">**グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3240-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="c3240-121">仕入先グループは、次の共通のパラメーターを持つ仕入先をグループ化するために使用されます。支払条件、決済期間、売上税グループを含む在庫転記の勘定科目、既定の勘定科目、製品のフィルター コードおよび供給予測コンフィギュレーション。</span><span class="sxs-lookup"><span data-stu-id="c3240-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="c3240-122">**従業員数** フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="c3240-123">**組織番号** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="c3240-124">住所の追加</span><span class="sxs-lookup"><span data-stu-id="c3240-124">Add an address</span></span>
1. <span data-ttu-id="c3240-125">**住所** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c3240-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="c3240-126">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3240-126">Click **Add**.</span></span>
3. <span data-ttu-id="c3240-127">**目的** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3240-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="c3240-128">1 つ以上の目的を選択できます。</span><span class="sxs-lookup"><span data-stu-id="c3240-128">You can select one or more purposes.</span></span> <span data-ttu-id="c3240-129">これらは該当する目的に正しい住所を選択するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3240-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="c3240-130">たとえば、目的が 「請求書」 であれば、請求書を送付する際に住所が使用されます。</span><span class="sxs-lookup"><span data-stu-id="c3240-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="c3240-131">**名前または説明** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="c3240-132">**国/地域** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c3240-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="c3240-133">住所の詳細を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-133">Enter the address details.</span></span> <span data-ttu-id="c3240-134">選択した国/地域により、国/地域の住所の形式に対応して、表示されるフィールドが決まります。</span><span class="sxs-lookup"><span data-stu-id="c3240-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="c3240-135">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3240-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="c3240-136">連絡先情報の追加</span><span class="sxs-lookup"><span data-stu-id="c3240-136">Add contact information</span></span>
1. <span data-ttu-id="c3240-137">**連絡先情報** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c3240-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="c3240-138">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3240-138">Click **Add**.</span></span>
3. <span data-ttu-id="c3240-139">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="c3240-140">**タイプ** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c3240-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="c3240-141">**連絡先の電話番号/住所** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c3240-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="c3240-142">これが基本連絡先である場合は、この [主要] チェック ボックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c3240-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="c3240-143">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c3240-143">Click **Save**.</span></span>
7. <span data-ttu-id="c3240-144">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c3240-144">Close the page.</span></span>
8. <span data-ttu-id="c3240-145">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c3240-145">Close the page.</span></span>


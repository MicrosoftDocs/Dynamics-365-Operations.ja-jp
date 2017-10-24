--- 
title: "売上税の元帳転記グループの設定"
description: "売上税が計算されると、元帳転記グループで指定されている主勘定に転記されます。"
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 10386719e925e53e26c7e547b29a72873a4d000d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a><span data-ttu-id="5ded9-103">売上税の元帳転記グループの設定</span><span class="sxs-lookup"><span data-stu-id="5ded9-103">Set up ledger posting groups for sales tax</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ded9-104">売上税が計算されると、元帳転記グループで指定されている主勘定に転記されます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-104">Sales tax is calculated and posted to main accounts that are specified in the Ledger posting groups.</span></span> <span data-ttu-id="5ded9-105">元帳転記グループは各売上税コードに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-105">Ledger posting groups are attached to each sales tax code.</span></span> <span data-ttu-id="5ded9-106">各売上税コードに対して個別の元帳転記グループを設定するか、すべての売上税コードに対して 1 つの元帳転記グループを使用するか、または売上税コードに複数の元帳転記グループを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-106">You can set up individual ledger posting groups for each sales tax code, use one ledger posting group for all sales tax codes or assign multiple ledger posting groups to the sales tax codes.</span></span> <span data-ttu-id="5ded9-107">このレコードでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-107">This recording uses the DEMF demo company.</span></span> 

1. <span data-ttu-id="5ded9-108">[税] > [設定] > [売上税] > [元帳転記グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-108">Go to Tax > Setup > Sales tax > Ledger posting groups.</span></span>
2. <span data-ttu-id="5ded9-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ded9-109">Click New.</span></span>
3. <span data-ttu-id="5ded9-110">[元帳転記グループ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-110">In the Ledger posting group field, type a value.</span></span>
4. <span data-ttu-id="5ded9-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5ded9-112">[売上税支払] フィールドで、税務当局に売上税を支払う主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-112">In the Sales tax payable field, select the main account for outgoing sales taxes that are payable to the tax authority.</span></span>
    * <span data-ttu-id="5ded9-113">売上税の徴収は、税務当局に代わって課税対象の商品やサービスを販売するときに行います。</span><span class="sxs-lookup"><span data-stu-id="5ded9-113">Sales taxes are collected on behalf of the tax authority when you sell taxable goods and services.</span></span>  
6. <span data-ttu-id="5ded9-114">[売上税収入] フィールドで、税務当局から税金を受け取る主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-114">In the Sales tax receivable filed, select the main account for incoming taxes that are received from the tax authority.</span></span>
    * <span data-ttu-id="5ded9-115">仕入先は、税務当局に代わって課税対象の商品やサービスが購入されるときに税を徴収します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-115">Vendors collect taxes on behalf of the tax authority when you buy taxable goods and services.</span></span> <span data-ttu-id="5ded9-116">このフィールドは、[総勘定元帳のパラメーター] ページの [売上税課税ルールの適用] オプションが選択されている場合には使用できません。</span><span class="sxs-lookup"><span data-stu-id="5ded9-116">This field is not available if the Apply sales tax taxation rules option is selected in the General ledger parameters page.</span></span> <span data-ttu-id="5ded9-117">その代わり、仕入先に支払われる売上税は、仕入と同じ勘定の借方に記入されます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-117">Instead, sales taxes that are paid to vendors are debited to the same account as the purchase.</span></span>   
7. <span data-ttu-id="5ded9-118">[利用税経費] フィールドで、EU の逆請求 GST/HST の一部として仕入先から税務当局に申告または報告が行われていない、控除可能な利用税を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-118">In the Use tax expense field, select  the main account for posting deductible Use taxes that are not claimed or reported to the tax authority by vendors as part of EU reverse charge GST/HST.</span></span>
    * <span data-ttu-id="5ded9-119">[使用税] オプションは、トランザクションに使用する [売上税グループ] の [売上税コード] に対して選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ded9-119">The Use tax option needs to be selected for the Sales tax code in the Sales tax group that is used in the transaction.</span></span>  <span data-ttu-id="5ded9-120">このフィールドは、[総勘定元帳のパラメーター] ページの [売上税課税ルールの適用] オプションが選択されている場合には使用できません。</span><span class="sxs-lookup"><span data-stu-id="5ded9-120">This field is not be available if the Apply sales tax taxation rules option is selected in the General ledger parameters page.</span></span>   
8. <span data-ttu-id="5ded9-121">[使用税支払勘定] フィールドで、税務当局に支払う利用税を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-121">In the Use tax payable field, select the main account for posting incoming Use taxes that are payable to tax authorities.</span></span>
    * <span data-ttu-id="5ded9-122">[使用税] オプションは、使用税を転記する [売上税グループ] の [売上税コード] で選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ded9-122">The Use tax option needs to be selected in the Sales tax code in the Sales tax group to post Use tax.</span></span> <span data-ttu-id="5ded9-123">総勘定元帳のパラメータで [売上税課税ルールの適用] オプションが選択されている場合、トランザクションの経費勘定への相殺転記が行われます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-123">If Apply sales tax taxation rules option is selected in General ledger parameters, the offset is posted to the transaction’s expense account.</span></span>   
9. <span data-ttu-id="5ded9-124">[決済勘定] フィールドで、[使用税支払勘定] および [売上税収入] フィールドで指定された勘定科目の正味残高を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-124">In the Settlement account field, select the main account  that the net balance of the ledger accounts specified in the Use tax payable and Sales tax receivable fields will be posted.</span></span>
    * <span data-ttu-id="5ded9-125">残高は、売上税の決済と転記のジョブが実行された場合に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-125">The balance will be created when the Sales tax settle and post job is ran.</span></span>  <span data-ttu-id="5ded9-126">決済期間において税務当局が仕入先と関連付けられている場合、残高は仕入先に転記されます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-126">If the Tax authority for the settlement period is associated with a vendor account, the balance is posted to the vendor account instead.</span></span>   
10. <span data-ttu-id="5ded9-127">[仕入先現金割引] フィールドで、この元帳転記グループと関連付けられた売上税コードについての現金割引を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-127">In the Vendor cash discount field, select the main account to post cash discount for Sales tax codes associated with this Ledger posting group.</span></span>
    * <span data-ttu-id="5ded9-128">これはオプションです。勘定が入力されていない場合、現金割引コードの主勘定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-128">This is optional and if no account is entered,  the main account on Cash discount codes will be used.</span></span> <span data-ttu-id="5ded9-129">[売上税] グループの現金割引オプションで逆請求売上税を使用している場合、元帳転記グループごとに異なる勘定を使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="5ded9-129">It can be useful to use different accounts per Ledger posting group if using the reverse sales tax on cash discount option on Sales tax groups.</span></span>  
11. <span data-ttu-id="5ded9-130">[顧客現金割引] フィールドで、この元帳転記グループと関連付けられた売上税コードについての現金割引を転記する主勘定を選択します。</span><span class="sxs-lookup"><span data-stu-id="5ded9-130">In the Customer case discount field, select the main account to post cash discount for Sales tax codes associated with this Ledger posting group.</span></span>
    * <span data-ttu-id="5ded9-131">これはオプションです。勘定が入力されていない場合、現金割引コードの主勘定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ded9-131">This is optional and if no account is entered, the main account on the Cash discount codes will be used.</span></span> <span data-ttu-id="5ded9-132">[売上税] グループの現金割引オプションで逆請求売上税を使用している場合、元帳転記グループごとに異なる勘定を使用すると便利です。</span><span class="sxs-lookup"><span data-stu-id="5ded9-132">It can be useful to use different accounts per Ledger posting group if using the reverse sales tax on cash discount option on Sales tax groups.</span></span>  
12. <span data-ttu-id="5ded9-133">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ded9-133">Click Save.</span></span>



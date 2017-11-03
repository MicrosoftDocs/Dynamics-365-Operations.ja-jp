---
title: "固定資産の取得の転記勘定"
description: "この記事は、資産の取得について総勘定元帳の転記勘定を設定する方法を説明します。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: a1a7da48b45566217399bc1d01a9c6e87ad56ec8
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="c3cfa-103">固定資産の取得の転記勘定</span><span class="sxs-lookup"><span data-stu-id="c3cfa-103">Fixed asset acquisition posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c3cfa-104">この記事は、資産の取得について総勘定元帳の転記勘定を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="c3cfa-105">固定資産の取得の転記に使用される勘定は、資産を取得するのに使用された方法によって異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="c3cfa-106">[固定資産転記プロファイル] ページの [勘定科目] タブで、元帳に転記する固定資産勘定を設定するための取得と取得原価調整を選択します。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="c3cfa-107">仕訳帳および発注書では、通常、勘定科目は貸借対照表の勘定で、新しい固定資産の取得金額は借方に転記されます。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="c3cfa-108">この勘定は仕訳帳に表示されず、トランザクションで置き換えることができません。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="c3cfa-109">相手勘定も貸借対象表の勘定です。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="c3cfa-110">一般的な仕訳帳および固定資産仕訳帳では、この勘定は、資産の取得の支払に使用される銀行口座になることがよくあります。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="c3cfa-111">相手勘定は、仕訳帳で提示される既定の勘定です。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="c3cfa-112">相手勘定は、仕訳帳で勘定科目表の他のどの勘定にも変更でき、また固定資産を仕入先から購入した場合は仕入先勘定にも変更できます。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="c3cfa-113">買掛金勘定の [請求仕訳帳] または [発注書] が固定資産の取得に使用される場合、固定資産トランザクションの相手勘定は、そのトランザクションで選択された仕入先勘定に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="c3cfa-114">[総勘定元帳] の [固定資産の在庫仕訳帳] を使用して転記された取得の場合、固定資産は外部のソースから購入されたのではなく、会社の在庫から移動されています。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="c3cfa-115">したがって、相手勘定は、在庫管理の在庫品目に対する在庫払出勘定になります。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="c3cfa-116">詳細については、「[調達によって取得される資産の取得](acquire-assets-procurement.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c3cfa-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>





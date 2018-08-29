---
title: "ハイブリッド顧客注文"
description: "ハイブリッド顧客注文は 1 つの注文で、顧客によって店舗で処理できる製品と、集配や後日出荷される製品を含みます。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 88d12641fa05953f7082158303237b7ba40c3fe2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="hybrid-customer-orders"></a><span data-ttu-id="0f0f0-103">ハイブリッド顧客注文</span><span class="sxs-lookup"><span data-stu-id="0f0f0-103">Hybrid customer orders</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f0f0-104">ハイブリッド顧客注文は 1 つの注文で、顧客によって店舗で処理できる製品と、集配や後日出荷される製品を含みます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-104">A hybrid customer order is a single order, which contains products that can be carried out of the store by the customer, as well as products that will be picked up or shipped later.</span></span>

<span data-ttu-id="0f0f0-105">Microsoft Dynamics 365 for Retail では、顧客注文のすべての製品または選択された製品の処理を選択できます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-105">In Microsoft Dynamics 365 for Retail, you can select either carry out all products or carry out selected products for a customer order.</span></span> <span data-ttu-id="0f0f0-106">注文が作成されると、処理としてマークされた製品ラインが自動的に請求され、これは注文が作成された後集荷される注文の場合も同じです。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-106">The product lines that are marked as carry out are automatically invoiced after the order is created, similarly this is the same for an order that is to be picked-up after the order is created.</span></span> <span data-ttu-id="0f0f0-107">ハイブリッド注文の支払金額は、処理行の総額のある集荷および出荷製品ラインに預金率を追加することによって決まります。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-107">The amount due on hybrid orders is determined by adding the deposit percentage on pick and ship product lines with the full amount of the carry out lines.</span></span> <span data-ttu-id="0f0f0-108">ハイブリッド注文の場合、システムは顧客注文モードと現金売りモードとを次のように切り替えます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-108">For hybrid orders, the system switches between customer order mode and cash and carry mode as follows:</span></span>

-   <span data-ttu-id="0f0f0-109">カート内の全製品を **配送実行** に設定する場合、注文は現金売りトランザクションとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-109">If all products in the cart are set to **Carry out delivery**, the order will be handled as a Cash and Carry transaction.</span></span>
-   <span data-ttu-id="0f0f0-110">カート内のいくつかまたはすべての製品を **集配** または **出荷配送** に設定する場合、注文は顧客注文トランザクションとして処理されます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-110">If any or all lines in the cart are set to either **Pick** or **ship delivery**, the order will be handled as a Customer order transaction.</span></span>

<span data-ttu-id="0f0f0-111">カート行が選択され、**選択されたピッキング**、**選択された出荷**、または **選択対象の実行** が選択されている場合、特定のカート行はその配送方法で設定されます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-111">If a cart line is selected and **Pick selected**, **Ship selected**, or **Carry out selected** is selected, only the specific cart line is set with that delivery method.</span></span> <span data-ttu-id="0f0f0-112">この場合、工程の下流の流れは通常どおり続きます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-112">In that case, the downstream flow of the operation continues as usual.</span></span> <span data-ttu-id="0f0f0-113">ただし、選択されているカート行がない状態で **選択されたピッキング**、**選択された出荷**、または **選択対象の実行** が選択された場合、すべてのカート行を一覧化する新しいページが開きます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-113">However, if **Pick selected**, **Ship selected**, or **Carry out selected** is selected without a cart line being selected, a new page opens that lists all the cart lines.</span></span> <span data-ttu-id="0f0f0-114">この画面で、一度に複数行を選択して、配送方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-114">On that screen, you can select multiple lines at once for setting the delivery method.</span></span> <span data-ttu-id="0f0f0-115">選択している行にその方法を使用する場合、行に割り当てられた前の配送方法は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="0f0f0-115">When you use that method for selecting lines, any previous delivery method that has been assigned to the line will be overridden.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0f0f0-116">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0f0f0-116">Additional resources</span></span>
--------

[<span data-ttu-id="0f0f0-117">顧客注文の概要</span><span class="sxs-lookup"><span data-stu-id="0f0f0-117">Customer orders overview</span></span>](customer-orders-overview.md)





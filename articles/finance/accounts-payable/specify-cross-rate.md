---
title: クロス レートの指定
description: このトピックでは、Microsoft Dynamics 365 Finance のクロス レートに関する情報を提供します。
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eafaf660470cec5fd82454660f2f59b86d488d0c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810297"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="8a057-103">クロス レートの指定</span><span class="sxs-lookup"><span data-stu-id="8a057-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a057-104">このトピックでは、クロス レートの目的、および請求書で支払決済するときのクロス レート指定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8a057-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="8a057-105">次の基準がすべて適用される場合、クロス レートを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a057-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="8a057-106">請求書で支払を決済する。</span><span class="sxs-lookup"><span data-stu-id="8a057-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="8a057-107">支払の明細行と請求書の明細行が異なる通貨を使用する。</span><span class="sxs-lookup"><span data-stu-id="8a057-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="8a057-108">いずれの通貨も会計通貨ではない。</span><span class="sxs-lookup"><span data-stu-id="8a057-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="8a057-109">クロス レートは、支払トランザクションの通貨を支払会計通貨に換算するためには使用されません。</span><span class="sxs-lookup"><span data-stu-id="8a057-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="8a057-110">代わりに、為替レート テーブルからの為替レートは、支払トランザクションの通貨金額と支払の会計通貨金額の値の計算のために取得されます。</span><span class="sxs-lookup"><span data-stu-id="8a057-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="8a057-111">たとえば、会計通貨が USD で、請求書の通貨が CAD で、支払の通貨が EUR の場合です。</span><span class="sxs-lookup"><span data-stu-id="8a057-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="8a057-112">クロス レートを使用して為替レートを入力すると、CAD と EUR の間で直接換算でき、USD を介する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8a057-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="8a057-113">請求書と基本支払を選択すると、請求明細行にクロス レートを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="8a057-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="8a057-114">クロス レートは、決済日時点での、これらのトランザクションの通貨間の為替レートです。</span><span class="sxs-lookup"><span data-stu-id="8a057-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="8a057-115">次のページのいずれかに移動します:</span><span class="sxs-lookup"><span data-stu-id="8a057-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="8a057-116">**売掛金勘定 > 共通 > 顧客 > すべての顧客**</span><span class="sxs-lookup"><span data-stu-id="8a057-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="8a057-117">**買掛金勘定 > 共通 > 仕入先 > すべての仕入先**</span><span class="sxs-lookup"><span data-stu-id="8a057-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="8a057-118">**調達 > 共通 > 仕入先 > すべての仕入先**</span><span class="sxs-lookup"><span data-stu-id="8a057-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="8a057-119">未処理トランザクションを決済する顧客または仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a057-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="8a057-120">顧客用に、**すべての顧客** リスト ページで、**収集 > 未処理トランザクションの決済** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a057-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="8a057-121">仕入先用に、**すべての仕入先** リスト ページで、**請求書 > 未処理トランザクションの決済** に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a057-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="8a057-122">基本支払であるトランザクションを選択し、**支払をマーク** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a057-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="8a057-123">**マーク** 列のチェック ボックスがオンになり、**基本支払** 列に情報アイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8a057-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="8a057-124">**クロス レート** フィールドに、決済日現在の請求通貨と支払通貨の間の為替レートを入力します。</span><span class="sxs-lookup"><span data-stu-id="8a057-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
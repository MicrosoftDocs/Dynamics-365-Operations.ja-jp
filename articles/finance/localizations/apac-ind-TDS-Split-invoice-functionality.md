---
title: 分割請求機能
description: ここでは、請求書を配送先や税勘定番号 (TAN) で分割するための設定と機能について説明します。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023393"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="5195a-103">分割請求機能</span><span class="sxs-lookup"><span data-stu-id="5195a-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5195a-104">ここでは、請求書を配送先や税勘定番号 (TAN) で分割するための設定と機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="5195a-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="5195a-105">**買掛金勘定パラメータ ー** ページの **全般** タブで、**製品受領** や **請求書** のチェックボックスを選択すると、配送先や TAN が異なる商品の領収書や請求書を **発注書** ページに掲載して分割することができます。</span><span class="sxs-lookup"><span data-stu-id="5195a-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="5195a-106">転記された請求書は、配送先や TAN を使用して分割されます。</span><span class="sxs-lookup"><span data-stu-id="5195a-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="5195a-107">**概要更新** タブの、**基づく分割** クイック タブで、**配送情報** 行の **確認書**、**ピッキング リスト**、**梱包明細**、**請求書** オプションを **はい** に設定すると、**販売注文** ページの異なる請求書行に異なる配送先やTANが定義されている確認書、ピッキング リスト、梱包明細、請求書を転記して分割することができます。</span><span class="sxs-lookup"><span data-stu-id="5195a-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="5195a-108">請求書は、まず配送先の住所で分割され、次に TAN で分割されます。</span><span class="sxs-lookup"><span data-stu-id="5195a-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="5195a-109">**配信情報** のオプションが **はい** に設定されていない場合、請求書は 1 枚の請求書として計上されます。</span><span class="sxs-lookup"><span data-stu-id="5195a-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="5195a-110">請求書の分割は行われません。</span><span class="sxs-lookup"><span data-stu-id="5195a-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="5195a-111">送り状の行の配送先や TAN が異なる場合に、梱包伝票を分割して郵送するには、**配送情報** の **梱包明細オプション** を **はい** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5195a-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="5195a-112">送り状の行の配送先や TAN が異なる場合に、請求書を分割して郵送するには、**配送情報** の **請求書** オプションを **はい** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5195a-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="5195a-113">送り状の行の配送先が異なり、TAN が同一請求書を郵送するには、**配送情報** の **請求書** オプションを **いいえ** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5195a-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="5195a-114">請求書が配送先ごとに分割されます。</span><span class="sxs-lookup"><span data-stu-id="5195a-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="5195a-115">例</span><span class="sxs-lookup"><span data-stu-id="5195a-115">Example</span></span>

<span data-ttu-id="5195a-116">この例では、**買掛金勘定パラメーター** ページの **集計更新** タブで、**配送情報** の **請求** オプションが **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="5195a-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="5195a-117">配送先と TAN が以下のように設定された購入請求書が計上されます:</span><span class="sxs-lookup"><span data-stu-id="5195a-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="5195a-118">**品目明細 1:** 配送先住所 1、TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="5195a-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="5195a-119">**品目明細 2:** 配送先住所 1、TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="5195a-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="5195a-120">**品目明細 3:** 配送先住所 2、TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="5195a-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="5195a-121">**品目明細 4:** 配送先住所 3、TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="5195a-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="5195a-122">この場合、元の請求書は 2 つの請求書に分割され、以下のように転記されます:</span><span class="sxs-lookup"><span data-stu-id="5195a-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="5195a-123">請求書 1 は、品目明細 1 と品目明細 2 の両方に転記されていますが、これは両ラインの配送先と TAN が同じであるためです。</span><span class="sxs-lookup"><span data-stu-id="5195a-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="5195a-124">請求書 2 は品目明細 3 に対して転記されます。</span><span class="sxs-lookup"><span data-stu-id="5195a-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="5195a-125">請求書 3 は品目明細 4 に対して転記されます。</span><span class="sxs-lookup"><span data-stu-id="5195a-125">Invoice 3 is posted for item line 4.</span></span>

---
title: しきい値制限と例外しきい値制限
description: このトピックでは、源泉徴収税 (TDS) のしきい値と例外制限について説明します。
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
ms.openlocfilehash: 1bf0d3a01ede559d288581d3b58b3777d0e608dc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023382"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a><span data-ttu-id="f2e9d-103">しきい値制限と例外しきい値制限</span><span class="sxs-lookup"><span data-stu-id="f2e9d-103">Threshold limit and exception threshold limit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2e9d-104">このトピックでは、源泉徴収税 (TDS) のしきい値と例外制限について説明します。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-104">This topic describes the threshold and exception limits for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="f2e9d-105">請求書および支払の TDS は、**源泉徴収税コンポーネント** ページで TDS 税コンポーネントに対して定義されたしきい値制限と例外しきい値制限を考慮して常に計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-105">The TDS on invoices and payments is always calculated considering the threshold limit and exception threshold limit defined for the TDS tax components on the **Withholding tax components** page.</span></span> <span data-ttu-id="f2e9d-106">TDS 税コンポーネントは、TDS 税グループに含まれる TDS 税コードに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-106">The TDS tax components are attached to TDS tax codes, which are included in the TDS tax groups.</span></span> <span data-ttu-id="f2e9d-107">TDS 税グループは仕入先と顧客に関連付けられ、請求書レベルまたは支払レベルで TDS を計算します。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-107">The TDS tax groups are attached to vendors and customers to calculate TDS at the invoice-level or payment-level.</span></span>

<span data-ttu-id="f2e9d-108">TDS が計算されるのは、仕入先の特定の TDS グループで転記されたトランザクションまたは累積トランザクションの金額が、**源泉徴収税コンポーネント** ページで指定されたしきい値制限を超えた場合です。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-108">TDS is calculated if the amount for a transaction or the cumulative transactions posted with a specific TDS group for a vendor exceeds the threshold limit specified on the **Withholding tax components** page.</span></span> <span data-ttu-id="f2e9d-109">TDS は、累積トランザクション金額が指定されたしきい値制限を超えるまで計算されません。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-109">TDS will not be calculated until the cumulative transaction amount exceeds the specified threshold limit.</span></span>

<span data-ttu-id="f2e9d-110">TDS コンポーネントのしきい値制限と共に例外しきい値制限が指定されている場合、TDS は、累積トランザクション金額が指定されたしきい値制限を超えていなくても、特定のトランザクション金額が例外しきい値制限を超えたときに計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-110">If an exception threshold limit is specified along with the threshold limit for a TDS component, TDS is calculated when a specific transaction amount exceeds the exception threshold limit even if the cumulative transaction amount does not exceed the specified threshold limit.</span></span>

### <a name="example"></a><span data-ttu-id="f2e9d-111">例</span><span class="sxs-lookup"><span data-stu-id="f2e9d-111">Example</span></span>
<span data-ttu-id="f2e9d-112">TDS という税コンポーネントを設定し、契約社員という TDS 税グループに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-112">A tax component called TDS is set up and attached to the TDS tax group called Contractor.</span></span> <span data-ttu-id="f2e9d-113">TDS 税コンポーネントのしきい値は 50,000、例外しきい値は 20,000 と定義されています。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-113">The threshold has been defined as 50,000 and exception threshold has been defined as 20,000 for TDS tax component.</span></span> <span data-ttu-id="f2e9d-114">TDS グループの契約社員は、仕入先 1 の既定の TDS グループとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-114">The TDS group contractor is defined as the default TDS group for vendor 1.</span></span>

<span data-ttu-id="f2e9d-115">仕入先 1 に対して 10000 の仕入請求書 001 が転記されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-115">A purchase invoice 001 is posted for vendor 1 for 10000.</span></span> <span data-ttu-id="f2e9d-116">請求金額がしきい値制限または例外しきい値制限を超えていないため、TDS は請求書に対して計算されません。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-116">TDS is not calculated for the invoice because the invoice amount has not crossed the threshold limit or exception threshold limit.</span></span> <span data-ttu-id="f2e9d-117">仕入先 1 に対して 25,000 の仕入請求書 002 が転記されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-117">A purchase invoice 002 is posted for vendor 1 for 25,000.</span></span> <span data-ttu-id="f2e9d-118">請求金額が例外しきい値制限を超えたため、TDS は請求書に対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-118">TDS is calculated for the invoice because the invoice amount has crossed the exception threshold limit.</span></span> <span data-ttu-id="f2e9d-119">仕入先 1 に対して 20,000 の仕入請求書 003 が転記されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-119">A purchase invoice 003 is posted for Vendor 1 for 20,000.</span></span> <span data-ttu-id="f2e9d-120">仕入先に対して発行された 3 つの請求書の合計請求金額がしきい値制限を超えたため、TDS が請求書に対して計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-120">TDS is calculated for the invoice because the total invoice amount of the three invoices that are issued for the vendor has crossed the threshold limit.</span></span> <span data-ttu-id="f2e9d-121">TDS は、TDS が以前に計算されていない仕入先に対して発行されたすべての請求書で計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-121">TDS is calculated on all invoices that are issued for the vendor on which the TDS has not been calculated earlier.</span></span> <span data-ttu-id="f2e9d-122">したがって、TDS は請求書 001 と 003 の合計請求金額である 30,000 で計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-122">Therefore, TDS is calculated on 30,000, which is the total invoice amount of invoice 001 and 003.</span></span>

<span data-ttu-id="f2e9d-123">しきい値制限および例外しきい値制限が TDS の計算で考慮されないのは、トランザクションに関連付けられている TDS グループの TDS 税コードに対して 、**しきい値を無視する** チェック ボックスが選択されている場合です。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-123">The threshold limit and exception threshold limit are not considered for the TDS calculation if the **Overlook threshold** check box is selected for TDS tax codes in the TDS group that is attached to the transaction.</span></span> <span data-ttu-id="f2e9d-124">しきい値制限は、**しきい値を無視する** チェック ボックスの対象である TDS グループの TDS 税コードでは使用されません。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-124">The threshold limit won't be used in the TDS tax codes in the TDS group that the **Overlook threshold** check box is for.</span></span>

<span data-ttu-id="f2e9d-125">一部の請求書の特定の TDS グループで **しきい値を無視する** チェック ボックスが選択されているが、特定の仕入先/顧客に対して作成された他の請求書については選択されていない場合、以前に計算されていないすべての請求書の累計金額を考慮して、少数の請求書のしきい値制限を無視しない TDS の計算が行われる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-125">If the **Overlook threshold** check box is selected for a specific TDS group for some invoices, but not selected for other invoices that were created for a specific vendor/customer, the calculation of TDS without overlooking the threshold limit for few invoices may take place considering the cumulative amount on all invoices on which TDS hasn't been calculated earlier.</span></span>

<span data-ttu-id="f2e9d-126">たとえば、しきい値制限は 25000 です。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-126">For example, the threshold limit is 25000.</span></span> <span data-ttu-id="f2e9d-127">次の請求書が、仕入先 A に対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-127">The following invoices are created for Vendor A.</span></span>

- <span data-ttu-id="f2e9d-128">請求書 1 – 2,0000 – (**しきい値を無視する** チェック ボックスは選択されていません): TDS は計算されません。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-128">Invoice 1 – 2,0000 – (**Overlook threshold** check box is not selected): TDS is not calculated.</span></span>

- <span data-ttu-id="f2e9d-129">請求書 2 – 4,000 – (**しきい値を無視する** チェック ボックスは選択されています): TDS は 4,000 で計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-129">Invoice 2 – 4,000 – (**Overlook threshold** check box is selected): TDS is calculated on 4,000.</span></span>

- <span data-ttu-id="f2e9d-130">請求書 2 – 3,000 – (**しきい値を無視する** チェック ボックスは選択されていません): TDS は、累計請求金額として計算されます。つまり、27,000 (20000+4000+3000) がしきい値制限を超過しました。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-130">Invoice 2 – 3,000 – (**Overlook threshold** check box is not selected): TDS is calculated as the cumulative invoice amount, that is, 27,000 (20000+4000+3000) exceeded the threshold limit.</span></span> <span data-ttu-id="f2e9d-131">TDS は、TDS が以前に計算されていない請求書の累計金額、つまり 23,000 (20000+3000) に基づいて計算されます。</span><span class="sxs-lookup"><span data-stu-id="f2e9d-131">TDS is calculated on the cumulative amount of invoices on which the TDS has not been calculated earlier, that is, 23,000 (20000+3000).</span></span>

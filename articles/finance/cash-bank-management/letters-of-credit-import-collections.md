---
title: 信用状および輸入取立
description: この記事は、信用状および輸入取立に関する一般情報を提供します。 どちらのタイプの銀行ドキュメントも、国境をまたぐ商品売買によく使用されます。
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLCImport
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 18321
ms.assetid: 5c97ab81-632b-4043-a940-674bcb496c80
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c31b8af25ea231f23ac5f4968760257b3f5894f
ms.sourcegitcommit: 74b10104338222a945684d841d60ab4b8e570168
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "3899448"
---
# <a name="letters-of-credit-and-import-collections"></a><span data-ttu-id="fede9-104">信用状および輸入取立</span><span class="sxs-lookup"><span data-stu-id="fede9-104">Letters of credit and import collections</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fede9-105">この記事は、信用状および輸入取立に関する一般情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="fede9-105">This article provides general information about letters of credit and import collections.</span></span> <span data-ttu-id="fede9-106">どちらのタイプの銀行ドキュメントも、国境をまたぐ商品売買によく使用されます。</span><span class="sxs-lookup"><span data-stu-id="fede9-106">Both types of bank document are often used for the purchase and sale of goods across international borders.</span></span>

<a name="letters-of-credit"></a><span data-ttu-id="fede9-107">信用状</span><span class="sxs-lookup"><span data-stu-id="fede9-107">Letters of credit</span></span>
-----------------

<span data-ttu-id="fede9-108">信用状は国際取引に使用され、支払が確実に行われるようにします。</span><span class="sxs-lookup"><span data-stu-id="fede9-108">Letters of credit are used for international transactions and help guarantee that payments will be made.</span></span> <span data-ttu-id="fede9-109">信用状は銀行が発行する契約であり、銀行は、買主と売主の契約が満たされた場合に買主に代わって確実に支払を行うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="fede9-109">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to guarantee payment on behalf of a buyer, provided that the terms of the agreement between the buyer and seller are met.</span></span> <span data-ttu-id="fede9-110">信用状は荷為替信用状 (DC) と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="fede9-110">A letter of credit is also referred to as a documentary credit (DC).</span></span>

<span data-ttu-id="fede9-111">輸入信用状の場合、法人は信用状の購入者または申請者です。</span><span class="sxs-lookup"><span data-stu-id="fede9-111">For an import letter of credit, the legal entity is the buyer or the applicant for the letter of credit.</span></span> <span data-ttu-id="fede9-112">輸出信用状の場合、法人は信用状の販売者または受益者です。</span><span class="sxs-lookup"><span data-stu-id="fede9-112">For an export letter of credit, the legal entity is the seller or the beneficiary of the letter of credit.</span></span> <span data-ttu-id="fede9-113">以下の関係者が信用状にかかわります。</span><span class="sxs-lookup"><span data-stu-id="fede9-113">The following parties are involved in a letter of credit:</span></span>

-   <span data-ttu-id="fede9-114">商品に対する支払の意志がある申請者 (買主)</span><span class="sxs-lookup"><span data-stu-id="fede9-114">The applicant (buyer) who intends to pay for the goods</span></span>
-   <span data-ttu-id="fede9-115">支払を受ける受益者 (売主)</span><span class="sxs-lookup"><span data-stu-id="fede9-115">The beneficiary (seller) who will receive the payment</span></span>
-   <span data-ttu-id="fede9-116">信用状を発行する発行銀行</span><span class="sxs-lookup"><span data-stu-id="fede9-116">The issuing bank that issues the letter of credit</span></span>
-   <span data-ttu-id="fede9-117">申請者に代わって取引を実行する通知銀行</span><span class="sxs-lookup"><span data-stu-id="fede9-117">The advising bank that carries out the transaction on behalf of the applicant</span></span>

<span data-ttu-id="fede9-118">信用状には、商品の説明、必要な書類、船積日、およびその日を過ぎると支払が行われない有効期限が記載されます。</span><span class="sxs-lookup"><span data-stu-id="fede9-118">The letter of credit includes a description of the goods, any required documents, the date of shipment, and the expiration date after which payment won't be made.</span></span> <span data-ttu-id="fede9-119">発行銀行は信用状の委託証拠金を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="fede9-119">The issuing bank collects a margin for the letter of credit.</span></span> 

<span data-ttu-id="fede9-120">信用状は **取消可能** または **取消不可** のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="fede9-120">A letter of credit can be **revocable** or **irrevocable**.</span></span> <span data-ttu-id="fede9-121">信用状の種類は、**譲渡可**、**譲渡付加**、または **リボルビング** のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="fede9-121">The nature of a letter of credit can be **transferable**, **non-transferable**, or **revolving**.</span></span> <span data-ttu-id="fede9-122">一般に、信用状は取消不能な確定契約であり、完全で正確な船積書類が提出されたときに、特定の受益者に支払がなされます。</span><span class="sxs-lookup"><span data-stu-id="fede9-122">Typically, a letter of credit is an irrevocable and confirmed agreement that payment will be made to a specific beneficiary upon submission of complete and accurate shipping documentation.</span></span>

## <a name="import-collections"></a><span data-ttu-id="fede9-123">輸入取立</span><span class="sxs-lookup"><span data-stu-id="fede9-123">Import collections</span></span>
<span data-ttu-id="fede9-124">輸入取立は、船積書類を銀行を通じて国際輸入者 (買主) に届ける、銀行の同意に基づく、銀行と輸出者 (売主) との間の契約です。</span><span class="sxs-lookup"><span data-stu-id="fede9-124">An import collection is an agreement between the bank and the exporter (seller), in which the bank agrees to deliver the shipping documentation to the international importer (buyer).</span></span> <span data-ttu-id="fede9-125">銀行は、出荷された商品に対する支払を、現金または支払に対する署名済手形で受け取ったときに、船積書類を届けることになります。</span><span class="sxs-lookup"><span data-stu-id="fede9-125">The bank is expected to deliver the shipping documentation upon receipt of payment for the shipped goods in cash, or upon receipt of a signed draft toward the payment.</span></span> 

<span data-ttu-id="fede9-126">輸入取立は、輸入された商品を受け取るための船積書類を買主が受領したときに、売主に確実に支払が行われることを保証します。</span><span class="sxs-lookup"><span data-stu-id="fede9-126">An import collection helps guarantee that the seller is paid when the buyer collects the shipping documents to take delivery of the imported goods.</span></span>




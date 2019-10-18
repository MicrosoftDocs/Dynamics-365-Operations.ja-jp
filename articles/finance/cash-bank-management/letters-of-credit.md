---
title: 信用状
description: 信用状は、国境をまたぐ商品売買によく使用される銀行ドキュメントです。
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankLCImport
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 18271
ms.assetid: aa594beb-bdb2-4117-91c2-d097d9401b0f
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db85db993c5368eaaa6ddfcc3dd02a2c2aa2be01
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188306"
---
# <a name="letters-of-credit"></a><span data-ttu-id="2d59b-103">信用状</span><span class="sxs-lookup"><span data-stu-id="2d59b-103">Letters of credit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d59b-104">信用状は、国境をまたぐ商品売買によく使用される銀行ドキュメントです。</span><span class="sxs-lookup"><span data-stu-id="2d59b-104">Letters of credit are bank documents that are commonly used for the purchase and sale of goods across international borders.</span></span> 

<span data-ttu-id="2d59b-105">信用状は国際取引に使用され、支払が確実に行われるようにします。</span><span class="sxs-lookup"><span data-stu-id="2d59b-105">Letters of credit are used for international transactions to ensure that payments will be made.</span></span> <span data-ttu-id="2d59b-106">信用状は銀行が発行する契約であり、銀行は、買主と売主の契約が満たされた場合に買主に代わって確実に支払を行うことに同意します。</span><span class="sxs-lookup"><span data-stu-id="2d59b-106">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span> <span data-ttu-id="2d59b-107">なお、信用状は荷為替信用状 (DC) と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="2d59b-107">Note that a letter of credit is also referred to as a documentary credit (DC).</span></span> 

<span data-ttu-id="2d59b-108">輸入信用状の場合、法人は信用状の購入者または申請者です。</span><span class="sxs-lookup"><span data-stu-id="2d59b-108">For an import letter of credit, the legal entity is the buyer or the applicant for the letter of credit.</span></span> <span data-ttu-id="2d59b-109">輸出信用状の場合、法人は信用状の販売者または受益者です。</span><span class="sxs-lookup"><span data-stu-id="2d59b-109">For an export letter of credit, the legal entity is the seller or the beneficiary of the letter of credit.</span></span> <span data-ttu-id="2d59b-110">以下の関係者が信用状にかかわります。</span><span class="sxs-lookup"><span data-stu-id="2d59b-110">The following parties are involved with a letter of credit:</span></span> 

 - <span data-ttu-id="2d59b-111">商品に対する支払の意志がある申請者 (買主)</span><span class="sxs-lookup"><span data-stu-id="2d59b-111">The applicant (buyer) who intends to pay for the goods</span></span> 
 - <span data-ttu-id="2d59b-112">支払を受ける受益者 (売主)</span><span class="sxs-lookup"><span data-stu-id="2d59b-112">The beneficiary (seller) who will receive the payment</span></span>
 - <span data-ttu-id="2d59b-113">信用状を発行する発行銀行</span><span class="sxs-lookup"><span data-stu-id="2d59b-113">The issuing bank that issues the letter of credit</span></span>
 - <span data-ttu-id="2d59b-114">申請者に代わって取引を実行する通知銀行</span><span class="sxs-lookup"><span data-stu-id="2d59b-114">The advising bank that carries out the transaction on behalf of the applicant</span></span>

<span data-ttu-id="2d59b-115">信用状には、商品の説明、必要な書類、船積日、およびその日を過ぎると支払が行われない有効期限が記載されます。</span><span class="sxs-lookup"><span data-stu-id="2d59b-115">The letter of credit includes a description of the goods, any required documents, the date of shipment, and the expiration date after which payment will not be made.</span></span> <span data-ttu-id="2d59b-116">発行銀行は信用状の委託証拠金を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="2d59b-116">The issuing bank collects a margin for the letter of credit.</span></span> 

<span data-ttu-id="2d59b-117">信用状は [取消可能] または [取消不可] のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="2d59b-117">A letter of credit can be revocable or irrevocable.</span></span> <span data-ttu-id="2d59b-118">信用状の種類は、譲渡可、譲渡付加、またはリボルビングのいずれかです。</span><span class="sxs-lookup"><span data-stu-id="2d59b-118">The nature of a letter of credit can be transferable, non transferable, or revolving.</span></span> <span data-ttu-id="2d59b-119">一般に、信用状は取消不能な確定契約であり、完全で正確な船積書類が提出されたときに、特定の受益者に支払がなされます。</span><span class="sxs-lookup"><span data-stu-id="2d59b-119">Typically, a letter of credit is an irrevocable and confirmed agreement that payment will be made to a specific beneficiary upon submission of complete and accurate shipping documentation.</span></span>

<span data-ttu-id="2d59b-120">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d59b-120">For more information, see the following topics:</span></span>

[<span data-ttu-id="2d59b-121">信用状のインポート</span><span class="sxs-lookup"><span data-stu-id="2d59b-121">Import a letter of credit</span></span>](tasks/import-letter-credit.md)

[<span data-ttu-id="2d59b-122">信用状のエクスポート</span><span class="sxs-lookup"><span data-stu-id="2d59b-122">Export a letter of credit</span></span>](tasks/export-letter-credit.md)

[<span data-ttu-id="2d59b-123">信用状の銀行融資の作成</span><span class="sxs-lookup"><span data-stu-id="2d59b-123">Create a bank facility for a letter of credit</span></span>](tasks/create-bank-facility-agreement-letter-credit.md)


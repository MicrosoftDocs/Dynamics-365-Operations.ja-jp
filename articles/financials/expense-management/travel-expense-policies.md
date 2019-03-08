---
title: 経費ポリシーを定義します
description: Microsoft Dynamics 365 for Finance and Operations では、作業者が経費精算書と出張費要求を入力して提出する際に従う必要がある経費ポリシーを定義できます。
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "342434"
---
# <a name="expense-policies"></a><span data-ttu-id="2556c-103">経費ポリシー</span><span class="sxs-lookup"><span data-stu-id="2556c-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2556c-104">作業者が経費精算書と出張費要求を入力して提出する際に従う必要があるポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2556c-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="2556c-105">経費ポリシーを実装すると、経費を効率的に管理できます。</span><span class="sxs-lookup"><span data-stu-id="2556c-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="2556c-106">たとえば、ニューヨークでのホテルの 1 泊料金は USD 250 以下にするというホテル経費のポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="2556c-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="2556c-107">経費精算書または宿泊料金がこの金額を超える出張費要求を作業者が提出すると、システムが通知をします</span><span class="sxs-lookup"><span data-stu-id="2556c-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="2556c-108">作業者が、経費に関するポリシー金額を超えました。</span><span class="sxs-lookup"><span data-stu-id="2556c-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="2556c-109">作業者が受け取るメッセージをコンフィギュレーションできます</span><span class="sxs-lookup"><span data-stu-id="2556c-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="2556c-110">ポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="2556c-110">define the policy.</span></span>      
        
<span data-ttu-id="2556c-111">次の 3 種類のポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="2556c-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="2556c-112">警告: 作業者は経費精算書や出張費要求を提出できますが、経費はすべての承認者にマークされ</span><span class="sxs-lookup"><span data-stu-id="2556c-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="2556c-113">その後の報告用に。</span><span class="sxs-lookup"><span data-stu-id="2556c-113">for later reporting.</span></span>        

- <span data-ttu-id="2556c-114">エラー: 経費精算書や出張費要求を提出する前に、経費を変更してポリシーに準拠するように作業者に要求します。</span><span class="sxs-lookup"><span data-stu-id="2556c-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="2556c-115">妥当性: 経費精算書や出張費要求を提出する前に、ポリシー金額を超えることに関する妥当性を入力するように作業者または管理者に要求します。</span><span class="sxs-lookup"><span data-stu-id="2556c-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="2556c-116">また、経費ポリシーの有効期間の日付範囲を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="2556c-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="2556c-117">たとえば、デンマーク間の便の航空運賃</span><span class="sxs-lookup"><span data-stu-id="2556c-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="2556c-118">およびニューヨーク市間では、休暇旅行シーズンのピーク時に高くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="2556c-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="2556c-119">制限する航空経費ルールを定義できます</span><span class="sxs-lookup"><span data-stu-id="2556c-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="2556c-120">ニューヨーク行きの航空運賃を DKK 5000 に制限し、このルールが 3 月 15 日から有効になるよう指定できます</span><span class="sxs-lookup"><span data-stu-id="2556c-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="2556c-121">9 月 15 日。</span><span class="sxs-lookup"><span data-stu-id="2556c-121">September 15.</span></span>

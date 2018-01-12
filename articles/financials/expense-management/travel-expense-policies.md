---
title: "経費ポリシーを定義します"
description: "Microsoft Dynamics 365 for Finance and Operations, Enterprise edition で、作業者が経費精算書と出張費要求を入力して提出する際に従う必要がある経費ポリシーを定義できます。"
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi2
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: e04fae56cf0ed988b267477ba1ed327e8e8f72c0
ms.contentlocale: ja-jp
ms.lasthandoff: 01/12/2018

---

# <a name="expense-policies"></a><span data-ttu-id="49767-103">経費ポリシー</span><span class="sxs-lookup"><span data-stu-id="49767-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="49767-104">作業者が経費精算書と出張費要求を入力して提出する際に従う必要があるポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="49767-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="49767-105">経費ポリシーを実装すると、経費を効率的に管理できます。</span><span class="sxs-lookup"><span data-stu-id="49767-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="49767-106">たとえば、ニューヨークでのホテルの 1 泊料金は USD 250 以下にするというホテル経費のポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="49767-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="49767-107">宿泊料金がこの金額を超える経費精算書を作業者が提出すると、経費に関するポリシー金額を超えたことが作業者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="49767-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="49767-108">ポリシーの定義時に作業者に送信するメッセージをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="49767-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="49767-109">次の 3 種類のポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="49767-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="49767-110">警告: 作業者は経費精算書や出張費要求を提出できますが、経費はすべての承認者にマークされ</span><span class="sxs-lookup"><span data-stu-id="49767-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="49767-111">その後の報告用に。</span><span class="sxs-lookup"><span data-stu-id="49767-111">for later reporting.</span></span> 
 - <span data-ttu-id="49767-112">エラー: 経費精算書や出張費要求を提出する前に、経費を変更してポリシーに準拠するように作業者に要求します。</span><span class="sxs-lookup"><span data-stu-id="49767-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="49767-113">妥当性: 経費精算書や出張費要求を提出する前に、ポリシー金額を超えることに関する妥当性を入力するように作業者または管理者に要求します。</span><span class="sxs-lookup"><span data-stu-id="49767-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="49767-114">また、経費ポリシーの有効期間の日付範囲を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="49767-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="49767-115">たとえば、デンマーク発着ニューヨーク便の航空運賃は、休暇の旅行シーズンのピーク時に高くなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="49767-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="49767-116">ニューヨーク行きの航空運賃を DKK 5000 に制限する航空経費ルールを定義し、このルールが 3 月 15 日から 9 月 15 日まで有効になるように指定することができます。</span><span class="sxs-lookup"><span data-stu-id="49767-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 


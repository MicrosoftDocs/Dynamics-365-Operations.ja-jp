---
title: 経費ポリシーを定義します
description: Microsoft Dynamics 365 Finance では、作業者が経費精算書と出張費要求を入力して提出する際に従う必要がある経費ポリシーを定義できます。
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389718"
---
# <a name="define-expense-policies"></a><span data-ttu-id="6cb3f-103">経費ポリシーを定義します</span><span class="sxs-lookup"><span data-stu-id="6cb3f-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cb3f-104">作業者が経費精算書と出張費要求を入力して提出する際に従う必要があるポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="6cb3f-105">経費ポリシーを実装すると、経費を効率的に管理できます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="6cb3f-106">たとえば、ニューヨークでのホテルの 1 泊料金は USD 250 以下にするというホテル経費のポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="6cb3f-107">経費精算書または宿泊料金がこの金額を超える出張費要求を作業者が提出すると、システムが通知をします</span><span class="sxs-lookup"><span data-stu-id="6cb3f-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="6cb3f-108">作業者が、経費に関するポリシー金額を超えました。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="6cb3f-109">作業者が受け取るメッセージをコンフィギュレーションできます</span><span class="sxs-lookup"><span data-stu-id="6cb3f-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="6cb3f-110">ポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-110">define the policy.</span></span>      
        
<span data-ttu-id="6cb3f-111">次の 3 種類のポリシーを定義できます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="6cb3f-112">警告: 作業者は経費精算書や出張費要求を提出できますが、経費はすべての承認者にマークされ</span><span class="sxs-lookup"><span data-stu-id="6cb3f-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="6cb3f-113">その後の報告用に。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-113">for later reporting.</span></span>        

- <span data-ttu-id="6cb3f-114">エラー: 経費精算書や出張費要求を提出する前に、経費を変更してポリシーに準拠するように作業者に要求します。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="6cb3f-115">妥当性: 経費精算書や出張費要求を提出する前に、ポリシー金額を超えることに関する妥当性を入力するように作業者または管理者に要求します。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="6cb3f-116">ポリシーのヒント</span><span class="sxs-lookup"><span data-stu-id="6cb3f-116">Policy tips</span></span>
<span data-ttu-id="6cb3f-117">経費管理に関する新しいポリシーを作成する際に役立つ提案を示します。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="6cb3f-118">ポリシーは日付に対して有効であり、経費が発生した日付より後の日付でポリシーが作成されている場合は有効になりません。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="6cb3f-119">たとえば、今日、50 ドルの最大食費を適用する新しいポリシーを作成していて、既存の経費が機能の昨日の日付で入力されている場合、このポリシーはチェックされません。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="6cb3f-120">明細化できる経費カテゴリに対するポリシーを作成する場合、経費明細行のタイプの条件を追加することを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="6cb3f-121">レシートを必要とするポリシーは明細行に対しては意味を持たない場合があり、ヘッダー行または非明細行にのみ適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="6cb3f-122">経費管理ポリシーは、既定ではソース エンティティに対して評価されます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="6cb3f-123">会社間のシナリオでは、代わりにターゲット エンティティ (借用エンティティ) に対して評価するポリシーを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="6cb3f-124">ターゲット エンティティに対してポリシーを実行するには、**機能の管理** ワークスペースの [借入法人との経費ポリシーの評価] 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="6cb3f-125">ポリシーを評価する場合</span><span class="sxs-lookup"><span data-stu-id="6cb3f-125">When to evaluate policies</span></span>

<span data-ttu-id="6cb3f-126">経費管理パラメータには、明細行を保存する時または経費精算書を送信する時のいずれかの時に経費管理ポリシーを評価するというオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="6cb3f-127">明細行を保存する時に評価するよう選択した場合、ユーザーは経費精算書を一度に完了するために必要な事柄を早く確認できることになります。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="6cb3f-128">それ以外の場合は、ワークフローへの送信中、その終了時に検証が実行されるようにした場合に、ポリシーの評価を遅らせることができ、時間を節約できます。</span><span class="sxs-lookup"><span data-stu-id="6cb3f-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>

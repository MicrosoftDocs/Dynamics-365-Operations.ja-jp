---
title: 顧客の与信管理
description: ''
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 11da8b7fb59bc8f3e2568ada27db753cc815b9c2
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015293"
---
# <a name="customer-credit-management-overview"></a><span data-ttu-id="37bd7-102">顧客の与信管理の概要</span><span class="sxs-lookup"><span data-stu-id="37bd7-102">Customer credit management overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="37bd7-103">顧客の与信管理を使用して、与信限度額を管理し、作成した与信ルールに基づいて転記プロセス中の販売注文のフローを制御できます。</span><span class="sxs-lookup"><span data-stu-id="37bd7-103">Customer credit management allows you to manage credit limits and control the flow of sales orders through the posting process based on credit rules that you create.</span></span> 

<span data-ttu-id="37bd7-104">与信管理を使用するプロセスには、次の手順の一部かまたは全部を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="37bd7-104">The process for using credit management can include some or all of the following steps:</span></span>
- <span data-ttu-id="37bd7-105">与信価値に関する追加の情報を提供する信用属性を使用して顧客を更新する</span><span class="sxs-lookup"><span data-stu-id="37bd7-105">Update customers with credit attributes that provide additional information about their credit worthiness</span></span> 
- <span data-ttu-id="37bd7-106">与信限度額調整を使用して、顧客の与信限度額を作成する</span><span class="sxs-lookup"><span data-stu-id="37bd7-106">Create credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="37bd7-107">ビジネス ニーズに基づいて一時的に与信限度額を増加または減少する場合、与信限度額調整を使用して顧客の一時的な与信限度額を作成する</span><span class="sxs-lookup"><span data-stu-id="37bd7-107">Create temporary credit limits for customers using credit limit adjustments when you want to increase or decrease their credit limit temporarily based on business needs</span></span>
- <span data-ttu-id="37bd7-108">保険や保証に関する情報など、与信限度額に影響を与える可能性のある情報を追加する</span><span class="sxs-lookup"><span data-stu-id="37bd7-108">Add additional information that can affect the credit limit such as insurance and guarantees</span></span>
- <span data-ttu-id="37bd7-109">単一の与信限度額を共有できるように、顧客間をリンクする顧客与信グループを作成する</span><span class="sxs-lookup"><span data-stu-id="37bd7-109">Create customer credit groups that link customers together so they can share a single credit limit</span></span>
- <span data-ttu-id="37bd7-110">リスク スコアを顧客に割り当て、それらのスコアを使用して、与信限度額調整を使用する顧客の与信限度額を自動的に生成する</span><span class="sxs-lookup"><span data-stu-id="37bd7-110">Assign risk scores to customers and then use those scores to automatically generate credit limits for customers using credit limit adjustments</span></span>
- <span data-ttu-id="37bd7-111">リスク、支払条件、与信限度額、期限切れ金額、使用された与信限度額の割合などの要因に基づいて、1 つ以上の転記プロセス中に注文を保留するブロック ルールを作成する</span><span class="sxs-lookup"><span data-stu-id="37bd7-111">Create blocking rules that will place an order on hold during one or more posting processes based on factors such as risk, payment terms, credit limits, overdue amounts, and percentage of credit limit used</span></span>
- <span data-ttu-id="37bd7-112">保留中の販売注文の一覧を管理し、保留の理由を確認して、問題を軽減する</span><span class="sxs-lookup"><span data-stu-id="37bd7-112">Manage a list of sales orders that are on hold, review the reasons for the hold, and mitigate the issues</span></span>
- <span data-ttu-id="37bd7-113">販売注文をリリースし、転記プロセスを継続できるようにする</span><span class="sxs-lookup"><span data-stu-id="37bd7-113">Release sales orders and allow it to continue through the posting process</span></span>
- <span data-ttu-id="37bd7-114">与信限度額の変更と販売注文リリースの承認を管理するためのワークフローを設定する</span><span class="sxs-lookup"><span data-stu-id="37bd7-114">Set up workflow to manage the approval of credit limit changes and sales order releases</span></span>


<a name="additional-resources"></a><span data-ttu-id="37bd7-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="37bd7-115">Additional resources</span></span>
--------
[<span data-ttu-id="37bd7-116">顧客与信管理パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="37bd7-116">Customer credit management parameters setup</span></span>](./cm-credit-mgmt-setup.md)

[<span data-ttu-id="37bd7-117">顧客与信管理の設定情報</span><span class="sxs-lookup"><span data-stu-id="37bd7-117">Customer credit management setup information</span></span>](./cm-setup-information.md)

[<span data-ttu-id="37bd7-118">顧客の与信管理情報の追加</span><span class="sxs-lookup"><span data-stu-id="37bd7-118">Add credit management information for a customer</span></span>](./cm-add-credit-mgmt-information-customer.md)

[<span data-ttu-id="37bd7-119">顧客の与信グループ</span><span class="sxs-lookup"><span data-stu-id="37bd7-119">Customer credit groups</span></span>](./cm-customer-credit-groups.md)

[<span data-ttu-id="37bd7-120">顧客の与信限度額調整</span><span class="sxs-lookup"><span data-stu-id="37bd7-120">Customer credit limit adjustments</span></span>](./cm-credit-limit-adjustments.md)

[<span data-ttu-id="37bd7-121">販売注文の与信保留</span><span class="sxs-lookup"><span data-stu-id="37bd7-121">Credit holds for sales orders</span></span>](./cm-sales-order-credit-holds.md)

[<span data-ttu-id="37bd7-122">顧客与信管理の定期処理タスク</span><span class="sxs-lookup"><span data-stu-id="37bd7-122">Customer credit management periodic tasks</span></span>](./cm-periodic-tasks.md)



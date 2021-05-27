---
title: システム管理者に権限がないため、注文の保留を解除できない
description: システム管理者に権限がないため、注文の保留を解除できません。
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026694"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="86c98-103">システム管理者に権限がないため、注文の保留を解除できない</span><span class="sxs-lookup"><span data-stu-id="86c98-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="86c98-104">KB 番号: 4614642</span><span class="sxs-lookup"><span data-stu-id="86c98-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="86c98-105">現象</span><span class="sxs-lookup"><span data-stu-id="86c98-105">Symptoms</span></span>

<span data-ttu-id="86c98-106">システム管理者は、注文の保留コードに特定のロールが割り当てられていない限り、販売注文の保留を解除できません。</span><span class="sxs-lookup"><span data-stu-id="86c98-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="86c98-107">解像度</span><span class="sxs-lookup"><span data-stu-id="86c98-107">Resolution</span></span>

<span data-ttu-id="86c98-108">販売注文の保留のクリアなど、一部の操作へのアクセスは、業務ポリシーの設定によって行われます。</span><span class="sxs-lookup"><span data-stu-id="86c98-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="86c98-109">システム管理者には通常、このタイプの操作は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="86c98-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="86c98-110">多くの場合、特定のタスクを実行するためのアクセスがビジネス ポリシーによって制御され、組織内の特定の人物だけがそのタスクを実行するよう承認されています。</span><span class="sxs-lookup"><span data-stu-id="86c98-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="86c98-111">たとえば、ワークフローの承認の結果である承認や、ワークフロー コンフィギュレーションの結果である特定のタスクなどがあります。</span><span class="sxs-lookup"><span data-stu-id="86c98-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="86c98-112">注文に関連付けられているワークフローがない場合でも、原則は類似しています。</span><span class="sxs-lookup"><span data-stu-id="86c98-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="86c98-113">関連する役割は、注文保留をクリアする権利を持つ組織内の特定のユーザー グループを示します。</span><span class="sxs-lookup"><span data-stu-id="86c98-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="86c98-114">そのアプローチは定義された業務ポリシーに違反するため、この権限は必ずすべての管理者に付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="86c98-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>

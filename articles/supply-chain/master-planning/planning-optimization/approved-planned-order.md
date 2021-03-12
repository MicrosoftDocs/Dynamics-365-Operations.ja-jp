---
title: 計画オーダーの承認
description: このトピックでは、計画最適化でサポートされる計画された注文の承認について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983572"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="82bfe-103">計画オーダーの承認</span><span class="sxs-lookup"><span data-stu-id="82bfe-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82bfe-104">このトピックでは、計画最適化で計画された注文のステータスを更新する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="82bfe-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="82bfe-105">計画された注文の承認は、計画オーダーから確定された注文を作成する方法としては任意のステップであることに留意してください。</span><span class="sxs-lookup"><span data-stu-id="82bfe-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="82bfe-106">修正済の計画された注文を承認することを推奨します。それ以外の場合は、編集は無視され、次の計画の実行時に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="82bfe-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![計画された注文フロー](media/approved-planned-orders-1.png)

<span data-ttu-id="82bfe-108">**状態** フィールドでは、以下の値を使用して進捗状況を表示します :</span><span class="sxs-lookup"><span data-stu-id="82bfe-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="82bfe-109">**未処理 :** マスタープ ランンが計画された注文を生成する場合、計画された注文は *未処理* の状態となります。</span><span class="sxs-lookup"><span data-stu-id="82bfe-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="82bfe-110">この状態になっている計画された注文は、次の計画実行時に削除されます。</span><span class="sxs-lookup"><span data-stu-id="82bfe-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="82bfe-111">**完了 :** 計画された注文を確定しないと判断した場合は、状態を *完了* に変更して、この計画された注文の評価を完了したことを表わします。</span><span class="sxs-lookup"><span data-stu-id="82bfe-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="82bfe-112">*未処理* と *完了* の状態 は、システムによって同じように扱われることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="82bfe-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="82bfe-113">**承認済 :** 編集を維持する場合や、計画された注文を確定する場合は、*承認済み* に変更してください。</span><span class="sxs-lookup"><span data-stu-id="82bfe-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="82bfe-114">*承認済みの* 状態で計画された注文は、マスタープランで固定され、供給が見込まれているとみなされるため、後のマスタープランの実行中に変更や削除されません。</span><span class="sxs-lookup"><span data-stu-id="82bfe-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="82bfe-115">これを達成するため、計画ロジックはマスター プラン中に、*承認済* 計画オーダーを古い計画バージョンから新しい計画バージョンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="82bfe-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="82bfe-116">ただし、 *承認済* の計画された注文は、特定のマスタープラン内でのみ供給されると見なされます。</span><span class="sxs-lookup"><span data-stu-id="82bfe-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="82bfe-117">計画された注文は、**マスター プラン** ワークスペース、**計画オーダー** リスト、または **計画製造オーダー**、**計画発注書**、**計画移動** リストから管理できます。</span><span class="sxs-lookup"><span data-stu-id="82bfe-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>

---
title: メンテナンス要求のタイプ
description: このトピックでは、資産管理でメンテナンス要求のタイプを設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d353f084e0d3e056f1b5ff5af6437ba211def8ec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208987"
---
# <a name="maintenance-request-types"></a><span data-ttu-id="f7953-103">メンテナンス要求のタイプ</span><span class="sxs-lookup"><span data-stu-id="f7953-103">Maintenance request types</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f7953-104">メンテナンス要求タイプは、メンテナンス要求を分類する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7953-104">Maintenance request types are used to categorize maintenance requests.</span></span> <span data-ttu-id="f7953-105">たとえば、予防的メンテナンスおよび修繕メンテナンスに関連するメンテナンス要求のタイプがあるとします。</span><span class="sxs-lookup"><span data-stu-id="f7953-105">For example, you might have maintenance request types that are related to preventive maintenance and corrective maintenance.</span></span> <span data-ttu-id="f7953-106">または、資産の修復 (Depot 修復) の管理に使用される特殊メンテナンス要求のタイプもあります。</span><span class="sxs-lookup"><span data-stu-id="f7953-106">Or you might have a special maintenance request type that is used to manage repair of assets (depot repair).</span></span>

<span data-ttu-id="f7953-107">メンテナンス依頼のタイプは、メンテナンス要求のライフサイクルの状態グループ (メンテナンス ライフサイクル モデル) との所属を定義します。</span><span class="sxs-lookup"><span data-stu-id="f7953-107">A maintenance request type defines the affiliation with a maintenance request lifecycle state group (maintenance lifecycle model).</span></span> <span data-ttu-id="f7953-108">メンテナンス要求のライフサイクル モデルは、メンテナンス要求に対して設定できるライフサイクルの状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="f7953-108">Maintenance request lifecycle models define the lifecycle states that can be set for a maintenance request.</span></span> <span data-ttu-id="f7953-109">(メンテナンス要求ライフサイクルの状態の例には、**作成済**、**有効**、および**終了済**が含まれます。)</span><span class="sxs-lookup"><span data-stu-id="f7953-109">(Examples of maintenance request lifecycle states include **Created**, **Active**, and **Ended**.)</span></span>

1. <span data-ttu-id="f7953-110">**資産管理** \> **設定** \> **メンテナンス要求** \> **メンテナンス要求のタイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f7953-110">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Maintenance request types**.</span></span>
2. <span data-ttu-id="f7953-111">**新規**を選択して、メンテナンス要求のタイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7953-111">Select **New** to create a maintenance request type.</span></span>
3. <span data-ttu-id="f7953-112">**メンテナンス要求のタイプ**フィールドで、メンテナンス依頼のタイプの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7953-112">In the **Maintenance request type** field, enter an ID for the maintenance request type.</span></span>
4. <span data-ttu-id="f7953-113">**名前**フィールドに、名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="f7953-113">In the **Name** field, enter a name.</span></span>
5. <span data-ttu-id="f7953-114">**一般**クイック タブでは、**メンテナンス要求のライフサイクル モデル** フィールドで、メンテナンス要求のライフサイクル モデルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7953-114">On the **General** FastTab, in the **Maintenance request lifecycle model** field, select a maintenance request lifecycle model.</span></span>
6. <span data-ttu-id="f7953-115">**ワーク オーダー タイプ** フィールドで、ワーク オーダー タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f7953-115">In the **Work order type** field, select a work order type.</span></span> <span data-ttu-id="f7953-116">メンテナンス要求がワーク オーダーに変換されると、そのワーク オーダーは、メンテナンス要求のタイプに関連するワーク オーダータイプを自動的に取得します。</span><span class="sxs-lookup"><span data-stu-id="f7953-116">When a maintenance request is converted to a work order, the work order automatically gets the work order type that is related to the maintenance request type.</span></span>

<span data-ttu-id="f7953-117">次の図は、**メンテナンス要求のタイプ** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7953-117">The following illustration shows an example of the **Maintenance request types** page.</span></span>

![メンテナンス要求のタイプ ページ](media/07-setup-for-requests.png)

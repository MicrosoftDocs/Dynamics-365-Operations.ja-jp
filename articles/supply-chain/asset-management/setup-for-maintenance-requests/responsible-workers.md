---
title: メンテナンス担当作業者
description: このトピックでは、資産管理でメンテナンス担当作業者を設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkerResponsible
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 113ee2b45c569c7dae3609f1027e31c4e5e5c54a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432073"
---
# <a name="responsible-maintenance-workers"></a><span data-ttu-id="0c190-103">メンテナンス担当作業者</span><span class="sxs-lookup"><span data-stu-id="0c190-103">Responsible maintenance workers</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0c190-104">メンテナンス担当作業者は、資産タイプ、資産、機能的な場所、メンテナンス作業タイプ カテゴリ、メンテナンス作業タイプ、メンテナンス作業タイプ バリアント、および取引に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="0c190-104">Responsible maintenance workers can be related to asset types, assets, functional locations, maintenance job type categories, maintenance job types, maintenance job type variants, and trades.</span></span> <span data-ttu-id="0c190-105">作業指示書およびメンテナンス要求で使用し、作業指示書を担当するメンテナンス作業者に関する基本設定を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="0c190-105">They can be used on work orders and maintenance requests to indicate a preference about the maintenance workers who should be responsible for a work order.</span></span> <span data-ttu-id="0c190-106">(ただし、これらのメンテナンス作業者は、必ずしも作業指示を実行する予定の作業員と同じではありません。) この機能の使用はオプションです。</span><span class="sxs-lookup"><span data-stu-id="0c190-106">(However, those maintenance workers aren't necessarily the same workers who are scheduled to carry out the work order.) Use of this functionality is optional.</span></span> <span data-ttu-id="0c190-107">たとえば、特定の作業タイプまたは作業領域の担当作業者または作業者グループを選択するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c190-107">For example, it can be used to select responsible workers or worker groups for specific work types or work areas.</span></span>

<span data-ttu-id="0c190-108">作業指示書のライフサイクルまたはメンテナンス要求のライフサイクル中に、メンテナンス担当作業者を変更または更新できます。</span><span class="sxs-lookup"><span data-stu-id="0c190-108">During a work order lifecycle or a maintenance request lifecycle, responsible maintenance workers can be changed or updated.</span></span> <span data-ttu-id="0c190-109">この変更または更新は、たとえば、メンテナンス要求のライフサイクルの状態の変更や作業指示書のライフサイクルの状態に関連付けられる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0c190-109">This change or update might be related to, for example, a change in the maintenance request lifecycle state or the work order lifecycle state.</span></span>

<span data-ttu-id="0c190-110">**メンテナンス担当作業者** ページの設定は、作業指示書のスケジューリング中には使用 *されません*。</span><span class="sxs-lookup"><span data-stu-id="0c190-110">The setup on the **Responsible maintenance workers** page is *not* used during work order scheduling.</span></span>

> [!NOTE]
> <span data-ttu-id="0c190-111">資産管理では、作業指示書のスケジューリング中に作業指示書に割り当てられる可能性のある *優先* メンテナンス作業者を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0c190-111">In Asset Management, you can also set up *preferred* maintenance workers who might be allocated to work orders during work order scheduling.</span></span>

<span data-ttu-id="0c190-112">メンテナンス担当作業者を設定する前に、選択可能な作業者およびメンテナンス作業員グループを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c190-112">Before you can set up responsible maintenance workers, you must set up the workers and maintenance worker groups that should be available for selection.</span></span> <span data-ttu-id="0c190-113">作業者およびメンテナンス作業者グループを設定する方法については、[メンテナンス作業者および作業者グループ](../setup-for-objects/workers-and-worker-groups.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c190-113">For information about how to set up workers and maintenance worker groups, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).</span></span>

## <a name="set-up-responsible-maintenance-workers"></a><span data-ttu-id="0c190-114">メンテナンス担当作業者の設定</span><span class="sxs-lookup"><span data-stu-id="0c190-114">Set up responsible maintenance workers</span></span>

1. <span data-ttu-id="0c190-115">**資産管理** \> **設定** \> **作業者** \> **メンテナンス担当作業者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0c190-115">Select **Asset management** \> **Setup** \> **Workers** \> **Responsible maintenance workers**.</span></span>
2. <span data-ttu-id="0c190-116">**新規** を選択してレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="0c190-116">Select **New** to create a record.</span></span>
3. <span data-ttu-id="0c190-117">最初に、既定のメンテナンス担当作業者またはメンテナンス担当作業者グループ設定を作成し、**メンテナンス担当作業者グループ** フィールドまたは **担当作業者** フィールドのみを設定します。</span><span class="sxs-lookup"><span data-stu-id="0c190-117">First create a default responsible maintenance worker or responsible maintenance worker group setup, where you set only the **Responsible maintenance worker group** field and/or the **Responsible worker** field.</span></span> <span data-ttu-id="0c190-118">残りのフィールドは空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="0c190-118">Leave the remaining fields blank.</span></span> <span data-ttu-id="0c190-119">この既定の設定は、作業指示書の内容と他のより具体的な組み合わせが一致しない場合に、作業指示書のスケジューリング中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="0c190-119">This default setup will be used during work order scheduling if no other, more specific combination matches the contents of the work order.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0c190-120">メンテナンス要求の作成中に、**すべてのメンテナンス要求** ページでメンテナンス担当作業者またはメンテナンス担当作業者グループを選択できるようになると、資産管理はすべてのメンテナンス担当作業者レコードを調べて、一致する可能性があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="0c190-120">During creation of a maintenance request, when a responsible maintenance worker or responsible maintenance worker group is made available for selection on the **All maintenance requests** page, Asset Management goes through all responsible maintenance worker records to check for a possible match.</span></span> <span data-ttu-id="0c190-121">常に最も限定的な組み合わせを最初にチェックします。</span><span class="sxs-lookup"><span data-stu-id="0c190-121">It always checks the most specific combination first.</span></span> <span data-ttu-id="0c190-122">つまり、資産管理は、まず **取引** フィールドの一致をチェックします。</span><span class="sxs-lookup"><span data-stu-id="0c190-122">In other words, Asset Management first checks for a match for the **Trade** field.</span></span> <span data-ttu-id="0c190-123">一致が見つからない場合は、**メンテナンス作業タイプ バリアント** フィールドの一致がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="0c190-123">If no match is found, it checks for a match for the **Maintenance job type variant** field.</span></span> <span data-ttu-id="0c190-124">一致が見つからない場合は、**メンテナンス作業タイプ バリアント** フィールドなどの一致がチェックされます。</span><span class="sxs-lookup"><span data-stu-id="0c190-124">If no match is found, it checks for a match for the **Maintenance job type** field, and so on.</span></span> <span data-ttu-id="0c190-125">ページのレイアウトでわかるように、この動作は、最も具体的な組み合わせを見つけるために、資産管理が各レコードを右から左に一致をチェックすることを意味します。(最初に **取引**、次に **メンテナンス作業タイプ バリアント**、次に **メンテナンス作業**、次に **メンテナンス作業タイプ カテゴリ**、次に **機能的な場所**、次に **資産**、最後に **資産タイプ**)</span><span class="sxs-lookup"><span data-stu-id="0c190-125">As you can see in the layout of the page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match (first **Trade**, then **Maintenance job type variant**, then **Maintenance job type**, then **Maintenance job type category**, then **Functional location**, then **Asset**, and finally **Asset type**).</span></span> <span data-ttu-id="0c190-126">一致するものが見つからない場合は、これらの 7 つのフィールドに選択がない既定のレコードが使用されます。</span><span class="sxs-lookup"><span data-stu-id="0c190-126">If no match is found, the default record that has no selections in those seven fields is used.</span></span>

<span data-ttu-id="0c190-127">次の図は、**メンテナンス担当作業者** ページの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="0c190-127">The following illustration shows an example of the **Responsible maintenance workers** page.</span></span>

![担当メンテナンス作業者ページ](media/08-setup-for-requests.png)

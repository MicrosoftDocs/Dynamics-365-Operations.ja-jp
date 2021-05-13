---
title: 不適合の承認を担当する作業者
description: このトピックでは、不適合の承認を担当する作業者を構成する方法について説明します。
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5979cb33146a00c3ea49ada9577140b24c07928f
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956732"
---
# <a name="workers-responsible-for-approving-nonconformances"></a><span data-ttu-id="23dfe-103">不適合の承認を担当する作業者</span><span class="sxs-lookup"><span data-stu-id="23dfe-103">Workers responsible for approving nonconformances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23dfe-104">このトピックでは、不適合の承認を担当する作業者を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-104">This topic describes how to configure workers that are responsible for approving nonconformances.</span></span>

<span data-ttu-id="23dfe-105">ユーザーが修正や操作などの詳細の入力を開始する前に、不適合を承認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23dfe-105">Nonconformances must be approved before users can start to enter details such as corrections or operations.</span></span> <span data-ttu-id="23dfe-106">ユーザーが不適合を承認または否認する前に、ユーザー ID (ユーザー レコード) は作業者レコードにリンクされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="23dfe-106">Before users can approve or reject nonconformances, their user ID (user record) must be linked to a worker record.</span></span> <span data-ttu-id="23dfe-107">オプションで、品質を担当する作業者を構成し、ある作業者が別の作業者の代わりに作業を承認できるようにします。</span><span class="sxs-lookup"><span data-stu-id="23dfe-107">You can optionally configure workers that are responsible for quality and then allow one worker to approve work on behalf of another worker.</span></span>

## <a name="enable-a-user-for-nonconformance-processing"></a><span data-ttu-id="23dfe-108">不適合処理に対しユーザーを有効化</span><span class="sxs-lookup"><span data-stu-id="23dfe-108">Enable a user for nonconformance processing</span></span>

<span data-ttu-id="23dfe-109">ユーザーが不適合を承認または否認する前に、ユーザー レコードを作業者レコードにリンクする必要があります。</span><span class="sxs-lookup"><span data-stu-id="23dfe-109">Before a user can approve or reject nonconformances, you must link their user record to a worker record.</span></span> <span data-ttu-id="23dfe-110">その後、承認フィールドが自動的に設定され、現在のユーザーがタイムシートに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="23dfe-110">The approval fields can then be automatically set, and the current user can be automatically filled in for the timesheet.</span></span> <span data-ttu-id="23dfe-111">ユーザーがドキュメントのメモを使用する前に、ユーザー オプションでドキュメント処理を有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="23dfe-111">Before the user can use the document notes, you must activate document handling in their user options.</span></span>

1. <span data-ttu-id="23dfe-112">**システム管理 \> ユーザー \> ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-112">Go to **System administration \> Users \> Users**.</span></span>
1. <span data-ttu-id="23dfe-113">不適合を承認または否認できるユーザーを検索して開きます。</span><span class="sxs-lookup"><span data-stu-id="23dfe-113">Find and open the user who should be able to approve or reject nonconformances.</span></span>
1. <span data-ttu-id="23dfe-114">**個人** フィールドに、現在のユーザー レコードに関連付けらた作業者の名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-114">Set the **Person** field to the name of the worker that is related to the current user record.</span></span>
1. <span data-ttu-id="23dfe-115">アクション ウィンドウで、**ユーザー オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-115">On the Action Pane, select **User options**.</span></span>
1. <span data-ttu-id="23dfe-116">現在のユーザー レコードの **オプション** ページの **基本設定** タブで、**ドキュメントの処理の有効化** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-116">On the **Options** page for the current user record, on the **Preferences** tab, set the **Enable document handling** option to *Yes*.</span></span>
1. <span data-ttu-id="23dfe-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="23dfe-117">Close the pages.</span></span>

## <a name="define-workers-that-are-responsible-for-quality"></a><span data-ttu-id="23dfe-118">品質を担当する作業者の定義</span><span class="sxs-lookup"><span data-stu-id="23dfe-118">Define workers that are responsible for quality</span></span>

1. <span data-ttu-id="23dfe-119">**在庫管理 \> 設定 \> 品質管理 \> 品質の担当作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-119">Go to **Inventory management \> Setup \> Quality control \> Workers responsible for quality**.</span></span>
2. <span data-ttu-id="23dfe-120">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-120">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="23dfe-121">**作業者** フィールドで、品質データを入力する作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-121">In the **Worker** field, select the worker that enters quality data.</span></span>
4. <span data-ttu-id="23dfe-122">**担当作業者** フィールドで、選択した作業者が代わりに作業を入力する作業者を選択します。</span><span class="sxs-lookup"><span data-stu-id="23dfe-122">In the **Worker responsible** field, select the worker that the selected worker enters work on behalf of.</span></span> <span data-ttu-id="23dfe-123">不適合が作成および更新されると、この作業者は既定で **作業者** フィールドに入力されます。</span><span class="sxs-lookup"><span data-stu-id="23dfe-123">When nonconformances are created and updated, this worker will be entered by default in **Worker** fields.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="23dfe-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="23dfe-124">Additional resources</span></span>

- [<span data-ttu-id="23dfe-125">品質管理の概要</span><span class="sxs-lookup"><span data-stu-id="23dfe-125">Quality management overview</span></span>](quality-management-processes.md)
- [<span data-ttu-id="23dfe-126">品質および不適合管理の有効化</span><span class="sxs-lookup"><span data-stu-id="23dfe-126">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="23dfe-127">品質諸費用</span><span class="sxs-lookup"><span data-stu-id="23dfe-127">Quality charges</span></span>](quality-charges.md)
- [<span data-ttu-id="23dfe-128">不適合の検査ゾーン</span><span class="sxs-lookup"><span data-stu-id="23dfe-128">Quarantine zones for nonconformances</span></span>](quality-quarantine-zones.md)
- [<span data-ttu-id="23dfe-129">不適合の診断タイプ</span><span class="sxs-lookup"><span data-stu-id="23dfe-129">Diagnostic types for nonconformances</span></span>](quality-diagnostic-types.md)
- [<span data-ttu-id="23dfe-130">不適合の品質諸費用</span><span class="sxs-lookup"><span data-stu-id="23dfe-130">Quality charges for nonconformances</span></span>](quality-charges.md)
- [<span data-ttu-id="23dfe-131">不適合の工程</span><span class="sxs-lookup"><span data-stu-id="23dfe-131">Operations for nonconformances</span></span>](quality-operations.md)
- [<span data-ttu-id="23dfe-132">倉庫プロセスに対する品質管理</span><span class="sxs-lookup"><span data-stu-id="23dfe-132">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

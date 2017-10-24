---
title: "クラウドの POS と MPOS の拡張ログオン機能の設定"
description: "このトピックでは、クラウド POS と Retail Modern POS (MPOS) の拡張ログオンを設定するためのオプションについて説明します。"
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 92353
ms.assetid: 7473e237-fbc8-41d5-8ba0-920242747488
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e29aea4509dd323c295b02f289fbcfa46fab3392
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-extended-logon-functionality-for-cloud-pos-and-mpos"></a><span data-ttu-id="41e5b-103">クラウドの POS と MPOS の拡張ログオン機能の設定</span><span class="sxs-lookup"><span data-stu-id="41e5b-103">Set up extended logon functionality for Cloud POS and MPOS</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="41e5b-104">このトピックでは、クラウド POS と Retail Modern POS (MPOS) の拡張ログオンを設定するためのオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="41e5b-104">This topic covers your options for setting up extended logon for Cloud POS and Retail Modern POS (MPOS).</span></span>

<a name="setting-up-extended-logon"></a><span data-ttu-id="41e5b-105">拡張ログオンの設定</span><span class="sxs-lookup"><span data-stu-id="41e5b-105">Setting up extended logon</span></span>
=========================

<span data-ttu-id="41e5b-106">バーコード マスクの設定は、[**小売**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**機能プロファイル**] にあります。</span><span class="sxs-lookup"><span data-stu-id="41e5b-106">You can find the setup for bar code masks at **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Functionality profiles**.</span></span> <span data-ttu-id="41e5b-107">[**機能**] クイック タブには、拡張ログオンに関連付けられる次のオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="41e5b-107">The **Functions** FastTab includes the following options that are related to extended logon.</span></span>

### <a name="staff-bar-code-logon"></a><span data-ttu-id="41e5b-108">スタッフ バーコード ログオン</span><span class="sxs-lookup"><span data-stu-id="41e5b-108">Staff bar code logon</span></span>

<span data-ttu-id="41e5b-109">[**スタッフ バーコード ログオン**] オプションが有効な場合、POS 資格情報に割り当てられた拡張ログオンを持っている作業者は、バーコードを使用してログオンできます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-109">When the **Staff bar code logon** option is enabled, workers who have an extended logon assigned to their point of sale (POS) credentials can log on by using a bar code.</span></span>

### <a name="staff-bar-code-logon-requires-password"></a><span data-ttu-id="41e5b-110">スタッフ バーコード ログオンにパスワードが必要</span><span class="sxs-lookup"><span data-stu-id="41e5b-110">Staff bar code logon requires password</span></span>

<span data-ttu-id="41e5b-111">パスワードが必要となる [**スタッフ バーコード ログオン**] オプションが有効な場合は、スタッフ バーコード ログオンは表示された拡張ログオンに割り当てられている作業者のみが選択されます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-111">When the **Staff bar code logon requires password** option is enabled, the staff bar code logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="41e5b-112">このオプションを有効にする場合、作業者はパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41e5b-112">Workers must still enter their password when this option is enabled.</span></span>

### <a name="staff-card-logon"></a><span data-ttu-id="41e5b-113">スタッフ カード ログオン</span><span class="sxs-lookup"><span data-stu-id="41e5b-113">Staff card logon</span></span>

<span data-ttu-id="41e5b-114">[**スタッフ カード ログオン**] オプションが有効な場合、POS 資格情報に割り当てられた拡張ログオンを持っている作業者は、磁気ストライプを使用してログオンできます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-114">When the **Staff card logon** option is enabled, workers who have an extended logon assigned to their POS credentials can log on by using a magnetic stripe.</span></span>

### <a name="staff-card-logon-requires-password"></a><span data-ttu-id="41e5b-115">スタッフ カード ログオンにパスワードが必要</span><span class="sxs-lookup"><span data-stu-id="41e5b-115">Staff card logon requires password</span></span>

<span data-ttu-id="41e5b-116">パスワードが必要となる [**スタッフ カード ログオン**] オプションが有効な場合は、スタッフ カード ログオンは表示された拡張ログオンに割り当てられている作業者のみが選択されます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-116">When the **Staff card logon requires password** option is enabled, the staff card logon selects only the worker who is assigned to the extended logon that is presented.</span></span> <span data-ttu-id="41e5b-117">このオプションを有効にする場合、作業者はパスワードを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41e5b-117">Workers must still enter their password when this option is enabled.</span></span>

<a name="assigning-an-extended-logon"></a><span data-ttu-id="41e5b-118">拡張ログオンの割り当て</span><span class="sxs-lookup"><span data-stu-id="41e5b-118">Assigning an extended logon</span></span>
===========================

<span data-ttu-id="41e5b-119">既定では、マネージャのみが作業者に拡張ログオンを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-119">By default, only managers can assign extended logon to workers.</span></span> <span data-ttu-id="41e5b-120">拡張ログオンを割り当てるには、POS で [**拡張ログオン**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="41e5b-120">To assign extended logon, go to **Extended log on** in POS.</span></span> <span data-ttu-id="41e5b-121">検索フィールドに、オペレーター ID を入力して、作業者を検索します。</span><span class="sxs-lookup"><span data-stu-id="41e5b-121">Then search for a worker by entering his or her operator ID in the search field.</span></span> <span data-ttu-id="41e5b-122">作業者を選択し、[**割り当て**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41e5b-122">Select the worker, and then click **Assign**.</span></span> <span data-ttu-id="41e5b-123">次のページで、作業者に割り当てる拡張ログオンを機械に通すかスキャンします。</span><span class="sxs-lookup"><span data-stu-id="41e5b-123">On the next page, swipe or scan the extended logon to assign to the worker.</span></span> <span data-ttu-id="41e5b-124">読み取りまたはスキャンが正常に読み取られた場合、[**OK**] ボタンが使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="41e5b-124">If the swipe or scan is successfully read, the **OK** button becomes available.</span></span> <span data-ttu-id="41e5b-125">その作業者の拡張ログオンを保存する場合、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41e5b-125">Click **OK** to save the extended logon for that worker.</span></span>

<a name="deleting-an-extended-logon"></a><span data-ttu-id="41e5b-126">拡張ログオンの削除</span><span class="sxs-lookup"><span data-stu-id="41e5b-126">Deleting an extended logon</span></span>
==========================

<span data-ttu-id="41e5b-127">作業者に割り当てられている拡張ログオンを削除するには、[**拡張ログオン**] 操作にて作業者を検索します。</span><span class="sxs-lookup"><span data-stu-id="41e5b-127">To delete the extended logon that is assigned to a worker, search for the worker by using the **Extended log on** operation.</span></span> <span data-ttu-id="41e5b-128">作業者を選択し、[**割り当て解除**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="41e5b-128">Select the worker, and then click **Unassign**.</span></span> <span data-ttu-id="41e5b-129">その作業者と関連付けられるすべての拡張ログオン資格情報が削除されます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-129">All extended logon credentials that are associated with that worker are removed.</span></span>

<a name="extending-extended-logon"></a><span data-ttu-id="41e5b-130">拡張ログオンの拡張</span><span class="sxs-lookup"><span data-stu-id="41e5b-130">Extending extended logon</span></span>
========================

<span data-ttu-id="41e5b-131">ログオン サービスはパーム スキャナーなどの追加ログオン デバイスをサポートするために、拡張できます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-131">The logon service can be extended to support additional extended logon devices, such as palm scanners.</span></span> <span data-ttu-id="41e5b-132">詳細については、POS 拡張ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="41e5b-132">For more information, see the POS extensibility documentation.</span></span>

<a name="using-extended-logon"></a><span data-ttu-id="41e5b-133">拡張ログオンの使用</span><span class="sxs-lookup"><span data-stu-id="41e5b-133">Using extended logon</span></span>
====================

<span data-ttu-id="41e5b-134">拡張ログオンを構成すると、作業者にバーコードまたは磁気ストライプが割り当てられ、作業者は POS ログオン ページが表示されている間に、自分のカードを読み取るか、またはスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="41e5b-134">When extended logon is configured, and a worker has been assigned a bar code or magnetic stripe, the worker just has to swipe or scan his or her card while the POS logon page is displayed.</span></span> <span data-ttu-id="41e5b-135">ログオンを続行する前にパスワードが必要な場合、作業者は自分のパスワードを入力するように要求されます。</span><span class="sxs-lookup"><span data-stu-id="41e5b-135">If a password is also required before logon can proceed, the worker is prompted to enter his or her password.</span></span>





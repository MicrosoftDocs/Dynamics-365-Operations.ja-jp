---
title: 二重書き込み設定後に法人を編集する
description: このトピックでは、二重書き込みの設定後に、会社または法人を追加または削除する方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bae36ca88a3ca1409f70bc2056657692f2ec5b57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688213"
---
# <a name="edit-a-legal-entity-after-dual-write-setup"></a><span data-ttu-id="0857e-103">二重書き込み設定後に法人を編集する</span><span class="sxs-lookup"><span data-stu-id="0857e-103">Edit a legal entity after dual-write setup</span></span> 

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="0857e-104">二重書き込みウィザードにより、二重書き込みの設定後に会社または法人を追加または削除することが可能になります。</span><span class="sxs-lookup"><span data-stu-id="0857e-104">The dual-write wizard enables you to add or remove a company or legal entity after dual-write has been set up.</span></span> <span data-ttu-id="0857e-105">これは、二重書き込み環境のリンクを解除して再リンクすることなく実行できます。</span><span class="sxs-lookup"><span data-stu-id="0857e-105">You can do this without having to unlink and relink your dual-write environment.</span></span> 

<span data-ttu-id="0857e-106">このウィザードを使用すると、Finance and Operations アプリを Dataverse 環境にリンクすることができます。</span><span class="sxs-lookup"><span data-stu-id="0857e-106">The wizard enables you to link your Finance and Operations apps to Dataverse environments.</span></span> <span data-ttu-id="0857e-107">このウィザードの一部として、1 つ以上の会社または法人を選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="0857e-107">As part of this wizard, you also can select one or more companies or legal entities.</span></span> <span data-ttu-id="0857e-108">企業または法人の一覧は静的なままではなく、常に変化しています。</span><span class="sxs-lookup"><span data-stu-id="0857e-108">The company or legal entity list doesn’t remain static and is constantly changing.</span></span> <span data-ttu-id="0857e-109">これは、特に段階的なロールアウトまたは買収の一部として、新しい会社を追加する必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="0857e-109">This is because you may need to add new companies, especially as part of a phased rollout or acquisitions.</span></span> <span data-ttu-id="0857e-110">これまでは、システムのダウンタイムがないと企業や法人を追加できませんでした。そのため、環境のリンクを解除して再リンクする必要がありました。</span><span class="sxs-lookup"><span data-stu-id="0857e-110">Until now, you were unable to add a company or legal entity without system down-time, which required you to unlink and relink your environment.</span></span> <span data-ttu-id="0857e-111">これらはすべて、特に既存のデータのために、費用が高くなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="0857e-111">All of this can be expensive, especially because of pre-existing data.</span></span> <span data-ttu-id="0857e-112">この機能を使用すると、既存の二重書き込み環境とのリンクを解除することなく、実稼働環境に会社を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="0857e-112">With this feature, you can add a company in a live environment without the need to unlink your existing dual-write environment.</span></span>

## <a name="add-a-company-or-legal-entity-after-dual-write-has-been-set-up"></a><span data-ttu-id="0857e-113">二重書き込みが設定された後の会社または法人の追加</span><span class="sxs-lookup"><span data-stu-id="0857e-113">Add a company or legal entity after dual-write has been set up</span></span> 

<span data-ttu-id="0857e-114">二重書き込みが設定された後に会社または法人を追加するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0857e-114">Follow these steps to add a company or legal entity after dual-write has been set up.</span></span>

1. <span data-ttu-id="0857e-115">**二重書き込みテーブル マップ** リスト ページで、**環境の詳細** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0857e-115">On the **Dual-write table map** list page, select the **Environment details** button.</span></span>

![環境の詳細ボタンを選択する](media/select-environment-details.png)

2. <span data-ttu-id="0857e-117">**法人** タブには、環境をリンクするための二重書き込みウィザードで選択した会社が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0857e-117">On the **Legal entities** tab, you see the company that you selected as part of the dual-write wizard to link environments.</span></span> <span data-ttu-id="0857e-118">この例では、会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="0857e-118">In this example, the company is USMF.</span></span>

![選択した会社が表示されている法人タブ](media/legal-entities.png)

3. <span data-ttu-id="0857e-120">**法人を追加** を選択して、1 つ以上の会社を二重書き込みに追加します。</span><span class="sxs-lookup"><span data-stu-id="0857e-120">Select **Add legal entity** to add one or more companies to dual-write.</span></span> <span data-ttu-id="0857e-121">この例では、GBSI です。</span><span class="sxs-lookup"><span data-stu-id="0857e-121">In this example, GBSI.</span></span> <span data-ttu-id="0857e-122">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0857e-122">Select **Save**.</span></span>

![新しい法人の追加](media/add-legal-entity.png)

  <span data-ttu-id="0857e-124">この時点で、法人は更新を開始します。</span><span class="sxs-lookup"><span data-stu-id="0857e-124">At this point, the legal entities start updating.</span></span> <span data-ttu-id="0857e-125">現在実行中または一時停止中のテーブル マップは、既存のデータをコピーすることによって初期書き込みプロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="0857e-125">The table maps that are currently running or paused go through the initial write process by copying pre-existing data.</span></span> <span data-ttu-id="0857e-126">プロセスが完了するまでは、テーブル マップを変更するアクションは実行しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="0857e-126">Until the process is completed, we recommend that you do not perform any actions to modify your table maps.</span></span> 

![法人の更新が進行中](media/update-progress.png)

  >[!NOTE]
  > <span data-ttu-id="0857e-128">この操作は、次のいずれかの条件に当てはまる場合に失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="0857e-128">This operation may fail if either of the following conditions are true:</span></span> 
  >
  > * <span data-ttu-id="0857e-129">1 つ以上のテーブル マップが既に初期書き込みの状態になっているときに、新しい会社を追加または削除します。</span><span class="sxs-lookup"><span data-stu-id="0857e-129">You add or remove a new company when one or more table maps is already in the Initial writes state.</span></span> <span data-ttu-id="0857e-130">これは、システムが既存のデータをコピーするプロセスです。</span><span class="sxs-lookup"><span data-stu-id="0857e-130">This the process where the system is copying pre-existing data.</span></span> 
  >
  > * <span data-ttu-id="0857e-131">1 つ以上のテーブル マップが一時停止の状態になっているときに、会社を削除します。</span><span class="sxs-lookup"><span data-stu-id="0857e-131">You remove a company when one or more table maps is in the Paused state.</span></span> 

4. <span data-ttu-id="0857e-132">プロセスが完了すると、法人が正常に更新されたことを示すバナーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="0857e-132">After the process is complete, a banner displays informing you that the legal entities have been updated successfully.</span></span> <span data-ttu-id="0857e-133">これで、テーブル マップの更新を再開することができます。</span><span class="sxs-lookup"><span data-stu-id="0857e-133">You can now resume updates to your table maps.</span></span> 

![法人の更新に成功しました](media/legal-entities-updated.png)


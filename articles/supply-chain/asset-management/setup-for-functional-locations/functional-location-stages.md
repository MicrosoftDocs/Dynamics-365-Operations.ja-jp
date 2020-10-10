---
title: 機能的な場所のライフサイクルの状態
description: このトピックでは、資産管理に機能的な場所の状態とライフサイクル モデルを設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eedc21dde32671b4f5539ac4e798a8e1329c191
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3890109"
---
# <a name="functional-location-lifecycle-states"></a><span data-ttu-id="d1c31-103">機能的な場所のライフサイクルの状態</span><span class="sxs-lookup"><span data-stu-id="d1c31-103">Functional location lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="d1c31-104">このトピックでは、資産管理に機能的な場所のライフサイクルの状態とライフサイクル モデルを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-104">This topic describes how to set up functional location lifecycle states and lifecycle models in Asset Management.</span></span> <span data-ttu-id="d1c31-105">機能的な場所のライフサイクルの状態は、機能的な場所が経由できる状態 (作成、アクティブ、終了など) を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-105">Functional location lifecycle states define the states that a functional location can go through, for example, created, active, and ended.</span></span> <span data-ttu-id="d1c31-106">**すべての機能的な場所**のリスト ページで、ライフサイクルの状態に関係なく、すべての機能的な場所を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-106">You are able to view all functional locations, regardless of their lifecycle state, in the **All functional locations** list page.</span></span> <span data-ttu-id="d1c31-107">機能的な場所の状態を変更するには、**すべての機能的な場所**リスト ページで機能場所の状態を選択し、**機能的な場所の状態を更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-107">You can change the state of a functional location by selecting it in the **All functional locations** list page and selecting **Update functional location state**.</span></span>

## <a name="set-up-functional-location-lifecycle-states"></a><span data-ttu-id="d1c31-108">機能的な場所のライフサイクル状態の設定</span><span class="sxs-lookup"><span data-stu-id="d1c31-108">Set up functional location lifecycle states</span></span>

1. <span data-ttu-id="d1c31-109">**資産管理** > **設定** > **機能的な場所** > **ライフサイクルの状態**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-109">Select **Asset management** > **Setup** > **Functional locations** > **Lifecycle states**.</span></span>
2. <span data-ttu-id="d1c31-110">**新規**を選択して、新しい機能的な場所の状態を作成します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-110">Select **New** to create a new functional location state.</span></span>
3. <span data-ttu-id="d1c31-111">**ライフサイクルの状態**フィールドに状態 ID を、また**名前**フィールドに機能的な場所の名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-111">Insert the state ID in the **Lifecycle state** field and a name for the functional location state in the **Name** field.</span></span> <span data-ttu-id="d1c31-112">**ライフサイクル モデル**フィールドでは、機能的な場所の状態を使用する機能的な場所のライフサイクル モデルの数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-112">In the **Lifecycle models** field, you can see the number of functional location lifecycle models that uses the functional location state.</span></span>
4. <span data-ttu-id="d1c31-113">**一般**クイック タブで、機能的な場所をこの状態で有効にする必要がある場合は、**有効**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-113">On the **General** FastTab, select "Yes" on the **Active** toggle button if the functional location should be active at this state.</span></span>
5. <span data-ttu-id="d1c31-114">機能的な場所と同じ名前の資産を自動的に作成し、この状態で機能的な場所にインストールできる場合は、**資産の作成**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-114">Select "Yes" on the **Create assets** toggle button if it should be possible to automatically create an asset with the same name as the functional location and install it on the functional location at this state.</span></span>  
>[!NOTE]
><span data-ttu-id="d1c31-115">このトグル ボタンは、**機能的な場所のタイプ**のフォームの、**一般**クイック タブの**資産タイプ** フィールドに関連しています (**資産管理** > **設定** > **機能的な場所** > **機能的な場所のタイプ**)。</span><span class="sxs-lookup"><span data-stu-id="d1c31-115">This toggle button relates to the **Asset type** field on the **General** FastTab in the **Functional location types** form (**Asset management** > **Setup** > **Functional locations** > **Functional location types**).</span></span>
6. <span data-ttu-id="d1c31-116">この状態で機能的な場所の名前を変更できる場合は、**場所の名前を変更**を変更できる場合は、トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-116">Select "Yes" on the **Rename location** toggle button if it should be possible to change the name of the functional location at this state.</span></span>
7. <span data-ttu-id="d1c31-117">この状態で機能的な場所に新しいサブ場所を追加できる場合は、**新しいサブ場所**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-117">Select "Yes" on the **New sub locations** toggle button if it should be possible to add new sub locations to the functional location at this state.</span></span>
8. <span data-ttu-id="d1c31-118">この状態で機能的な場所に資産を導入できる場合は、**資産の導入**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-118">Select "Yes" on the **Install assets** toggle button if it should be possible to install assets on the functional location at this state.</span></span>
9. <span data-ttu-id="d1c31-119">この状態で機能的な場所を削除できる場合は、**機能的な場所の削除**トグル ボタンで「はい」を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-119">Select "Yes" on the **Delete functional location** toggle button if it should be possible to delete the functional location at this state.</span></span>
10. <span data-ttu-id="d1c31-120">機能的な場所に導入されているすべての資産の資産ライフサイクルの状態を、この状態で自動的に更新する場合は、**ライフサイクルの状態**フィールドで、資産の状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-120">Select an asset state in the **Lifecycle state** field if you want the asset lifecycle state for all assets installed on the functional location to be automatically updated at this state.</span></span> <span data-ttu-id="d1c31-121">例: 機能的な場所を閉じて、機能的な場所のライフサイクル状態を 「終了」に設定した場合は、その機能的な場所に導入されている資産のライフサイクル状態を自動的に 「使用されていない」に変更できます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-121">Example: If you close down a functional location, and set the functional location lifecycle state to "Ended", you may want to automatically change the lifecycle state of the assets installed on that functional location to "Not in use".</span></span>


>[!NOTE]
><span data-ttu-id="d1c31-122">機能的な場所のライフサイクル状態、ライフサイクル モデル、およびタイプは、ワーク オーダーのライフサイクル状態、ワーク オーダー ライフサイクル モデル、およびワーク オーダー タイプと関連し、同じ方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-122">Functional location lifecycle states, lifecycle models, and types are related and used in the same way as work order lifecycle states, work order lifecycle models, and work order types.</span></span> 

## <a name="set-up-functional-location-lifecycle-models"></a><span data-ttu-id="d1c31-123">機能的な場所のライフサイクル モデルの設定</span><span class="sxs-lookup"><span data-stu-id="d1c31-123">Set up functional location lifecycle models</span></span>

<span data-ttu-id="d1c31-124">機能的な場所に必要なライフサイクル状態を作成したら、それらをグループに分割することができます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-124">When you have created the lifecycle states required for your functional locations, they can be divided into groups.</span></span> <span data-ttu-id="d1c31-125">これは、さまざまなタイプの機能的な場所に使用できるライフサイクル モデル フローを作成するために行われます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-125">This is done to create the lifecycle model flow that may be used for different types of functional locations.</span></span> <span data-ttu-id="d1c31-126">少なくとも、1 つの標準の機能的な場所のライフサイクル モデルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d1c31-126">As a minimum, one standard functional location lifecycle model should be created.</span></span>

1. <span data-ttu-id="d1c31-127">**資産管理** > **設定** > **機能的な場所** > **ライフサイクル モデル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-127">Select **Asset management** > **Setup** > **Functional locations** > **Lifecycle models**.</span></span>
2. <span data-ttu-id="d1c31-128">**新規**を選択して、新しいライフサイクル モデルを作成します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-128">Select **New** to create a new lifecycle model.</span></span>
3. <span data-ttu-id="d1c31-129">**ライフサイクル モデル** フィールドにライフサイクル モデル ID を、また**名前**フィールドにライフサイクル モデルの名前を挿入します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-129">Insert the lifecycle model ID in the **Lifecycle model** field and a name for the lifecycle model in the **Name** field.</span></span> <span data-ttu-id="d1c31-130">**機能的な場所のタイプ**および**ライフサイクルの状態**フィールドでは、ライフサイクル モデルを使用する機能的な場所のタイプの数と、ライフサイクル モデルで選択された状態の数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-130">In the **Functional location types** and **Lifecycle states** fields, you can see the number of functional location types that uses the lifecycle model and the number of states selected in the lifecycle model.</span></span>
4. <span data-ttu-id="d1c31-131">**ライフサイクルの状態**クイック タブで、モデルに含める必要がある状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-131">On the **Lifecycle states** FastTab, select the states that should be included in the model.</span></span> <span data-ttu-id="d1c31-132">これは、**残りのライフスタイル状態**セクションの状態をクリックし、![前方矢印](media/02-setup-for-functional-locations.png) ボタンをクリックすることにより実行されます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-132">This is done by clicking on a state in the **Lifecycle states remaining** section and clicking the ![forward arrow](media/02-setup-for-functional-locations.png) button.</span></span>
5. <span data-ttu-id="d1c31-133">モデルで使用可能なすべての状態を選択する場合は ![使用可能なすべてのステージを選択](media/03-setup-for-functional-locations.png) ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d1c31-133">If you want to select all the available states for a model, click the ![select all available stages](media/03-setup-for-functional-locations.png) button.</span></span> <span data-ttu-id="d1c31-134">すべての状態は、**選択されたライフサイクル状態**セクションに転送されます。</span><span class="sxs-lookup"><span data-stu-id="d1c31-134">All states are transferred to the **Lifecycle states selected** section.</span></span>
6. <span data-ttu-id="d1c31-135">選択した状態をモデルから削除する場合は、**選択されたライフサイクル状態**セクションで状態を選択し ![戻る矢印](media/04-setup-for-functional-locations.png) ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-135">If you want to remove a selected state from the model, select the state in the **Lifecycle states selected** section and then select the ![back arrow](media/04-setup-for-functional-locations.png) button.</span></span>
7. <span data-ttu-id="d1c31-136">**ライフサイクル状態の更新プログラム**を選択して、選択した状態に従うことができるライフサイクル状態を定義します。</span><span class="sxs-lookup"><span data-stu-id="d1c31-136">Select **Lifecycle state updates** to define which lifecycle states can follow a selected state.</span></span>

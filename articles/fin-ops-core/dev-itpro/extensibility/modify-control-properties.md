---
title: 拡張機能を使用して、フォーム コントロールのプロパティを変更する
description: このトピックでは、拡張機能を使用してコントロールのプロパティを変更する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 103794fc9c68ca6bf2cc45ecec6a1b2fb89f3710
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191581"
---
# <a name="modify-the-properties-of-form-controls-through-extension"></a><span data-ttu-id="904b3-103">拡張機能を使用して、フォーム コントロールのプロパティを変更する</span><span class="sxs-lookup"><span data-stu-id="904b3-103">Modify the properties of form controls through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="904b3-104">多くの場合、ユーザーがアプリとやりとりするには、変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="904b3-104">Often, the way that users interact with the application requires modification.</span></span> <span data-ttu-id="904b3-105">通常、ページ上のコントロールを非表示または無効にしたり、標準ラベルをより適切なラベルに置き換えたり、ユーザーが必要とする新しいコントロールを追加したりします。</span><span class="sxs-lookup"><span data-stu-id="904b3-105">Typically, you hide or disable controls on the page, replace standard labels with labels that are more appropriate, or even add new controls that the user requires.</span></span> <span data-ttu-id="904b3-106">また、フォーム拡張子を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="904b3-106">You can also create a form extension.</span></span> 

> [!TIP]
> <span data-ttu-id="904b3-107">フォーム コントロール イベント上のイベント サブスクリプションを使用して、より高い柔軟性を実現することができます。</span><span class="sxs-lookup"><span data-stu-id="904b3-107">You can achieve even more flexibility through event subscription on form control events.</span></span> <span data-ttu-id="904b3-108">この方法については、他のトピックで説明します。</span><span class="sxs-lookup"><span data-stu-id="904b3-108">This approach is discussed in other topics.</span></span> <span data-ttu-id="904b3-109">このトピックでは、メタデータの変更に焦点を当てます。</span><span class="sxs-lookup"><span data-stu-id="904b3-109">In this topic, the focus is on metadata changes.</span></span>

## <a name="example"></a><span data-ttu-id="904b3-110">例</span><span class="sxs-lookup"><span data-stu-id="904b3-110">Example</span></span>

<span data-ttu-id="904b3-111">顧客は **リリース済製品の詳細** ページの **在庫の管理** クイック タブへの変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="904b3-111">The customer requires changes to the **Manage inventory** FastTab on the **Released product details** page.</span></span> <span data-ttu-id="904b3-112">クイック タブのラベルを変更、CW 構成を表示するフィールド グループを無効化、および新しいコントロールを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="904b3-112">You must change the label of the FastTab, disable the field group that shows the catch weight configuration, and add new controls.</span></span> <span data-ttu-id="904b3-113">(この例では、新しいコントロールはデータ ソース内の既存のフィールドにバインドされません)。</span><span class="sxs-lookup"><span data-stu-id="904b3-113">(For this example, the new controls aren't bound to existing fields in the data source).</span></span>

<span data-ttu-id="904b3-114">必要な変更を行うには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="904b3-114">Follow these steps to make the required changes.</span></span>

1. <span data-ttu-id="904b3-115">拡張モデルでは、**EcoResProductDetailsExtended** フォームの拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="904b3-115">In the extension model, create an extension of the **EcoResProductDetailsExtended** form.</span></span>
2. <span data-ttu-id="904b3-116">フォーム デザイン ツリーを通じて、**TabPageInventory** タブ ページ (**デザイン** &gt; **タブ** &gt; **詳細** &gt; **GroupDetails** &gt; **TabHeader** &gt; **TabPageInventory**) に移動し、デザイナーでそれを選択して、**プロパティ** シートを開きます。</span><span class="sxs-lookup"><span data-stu-id="904b3-116">Navigate through the form design tree to the **TabPageInventory** tab page (**Design** &gt; **Tab** &gt; **Details** &gt; **GroupDetails** &gt; **TabHeader** &gt; **TabPageInventory**), select it in the designer, and open the **Property** sheet.</span></span>
3. <span data-ttu-id="904b3-117">**キャプション**プロパティを目的の値に更新します。</span><span class="sxs-lookup"><span data-stu-id="904b3-117">Update the **Caption** property to the desired value.</span></span>

    ![キャプション プロパティ](media/ModifyControlProperties01.jpg)

4. <span data-ttu-id="904b3-119">タブ ページを右クリックし、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="904b3-119">Right-click the tab page, and then select **New**.</span></span> <span data-ttu-id="904b3-120">新しいコントロールで必要なプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="904b3-120">Set the required properties on the new control.</span></span> <span data-ttu-id="904b3-121">また、すぐそばのコンテナでコントロールを上下に移動して、適切に配置することができます。</span><span class="sxs-lookup"><span data-stu-id="904b3-121">You can also move the control up and down in the immediate container to position it correctly.</span></span>

    > [!NOTE]
    > <span data-ttu-id="904b3-122">または、新しいコントロールに表示するサブノードを右クリックし、**Insert sibling** を選択し、追加するコントロールのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="904b3-122">Alternatively, right-click the subnode that the new control should appear after, select **Insert sibling**, and then select the type of control to add.</span></span>

    ![兄弟コマンドの挿入](media/ModifyControlProperties02.jpg)

    <span data-ttu-id="904b3-124">もちろん、対応するデータ ソースからバインドされたコントロールをドラッグすることもできます。</span><span class="sxs-lookup"><span data-stu-id="904b3-124">Of course, you can just drag bound controls over from the corresponding data source.</span></span>

5. <span data-ttu-id="904b3-125">**PdsCatchWeight** グループ コントロールをオンにし、**有効** プロパティを **いいえ** に変更します。</span><span class="sxs-lookup"><span data-stu-id="904b3-125">Select the **PdsCatchWeight** group control, and change the **Enabled** property to **No**.</span></span>

    ![PdsCatchWeight グループ コントロールのプロパティを有効化](media/ModifyControlProperties03.jpg)

    > [!NOTE]
    > <span data-ttu-id="904b3-127">**有効**および**表示**のようにメタデータのプロパティを変更した場合、実行時にその状態のままでコントロールの保証はありません。</span><span class="sxs-lookup"><span data-stu-id="904b3-127">If you change metadata properties such as **Enabled** and **Visible**, there is no guarantee that the control will stay in that state at runtime.</span></span> <span data-ttu-id="904b3-128">フォームが読み込まれた後、そのフォームのビジネス ロジックは、コードを使用してコントロールの状態を変更できます。</span><span class="sxs-lookup"><span data-stu-id="904b3-128">After a form is loaded, business logic on that form can change the state of controls through code.</span></span>

<span data-ttu-id="904b3-129">完了したら、ページには追加のフィールドが含まれ、CW 情報を編集することはできず、クイック タブ全体のキャプションが異なります。</span><span class="sxs-lookup"><span data-stu-id="904b3-129">When you've finished, the page includes additional fields, catch weight information can't be edited, and the whole FastTab has a different caption.</span></span> 

![変更されたクイック タブ](media/ModifyControlProperties04.jpg)

> [!NOTE]
> <span data-ttu-id="904b3-131">コントロールで **AutoDeclaration** プロパティを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="904b3-131">You can't modify the **AutoDeclaration** property on controls.</span></span> <span data-ttu-id="904b3-132">ただし、コードから名前でコントロールにアクセスすることはできます。</span><span class="sxs-lookup"><span data-stu-id="904b3-132">However, you can still access the controls by name from code.</span></span> 

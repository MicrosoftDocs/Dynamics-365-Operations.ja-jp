---
title: フィールドに数を表示
description: このトピックでは、正確で、迅速に表示される数を計算する方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 08a4c0043b989824d6fbb7e8362e116b058f7cab
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506219"
---
# <a name="show-counts-in-fields"></a><span data-ttu-id="47431-103">フィールドに数を表示</span><span class="sxs-lookup"><span data-stu-id="47431-103">Show counts in fields</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="47431-104">**pageLink** コントロールを使用してカウント (合計) を表示することができますが、行数をカウントする前にターゲット ページが読み込まれるため遅くなることがあります。</span><span class="sxs-lookup"><span data-stu-id="47431-104">Although a **pageLink** control can be used to show counts (totals), it can be slow, because it must load the target page before it counts the number of rows.</span></span> <span data-ttu-id="47431-105">また、取得される行の数に制限があるため、計算される数は正しくない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="47431-105">Additionally, the count that is calculated can be incorrect, because there is a limit on the number of rows that are retrieved.</span></span>

![カウントを表示するタイルを持つワークスペース](media/optimizing-workspace/Tiles_Original.png)

<span data-ttu-id="47431-107">モバイル ワークスペースをより迅速に動作させる場合は、通常のフィールドを使用してカウントを表示し、そのフィールドをモバイル クライアントの **pageLink** コントロールとしてモデル化することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="47431-107">If you want to make mobile workspaces work more quickly, we recommended that you use a regular field to show the count and then model the field as a **pageLink** control in the mobile client.</span></span>

<span data-ttu-id="47431-108">次の例では、フリート管理アプリを使用しています。</span><span class="sxs-lookup"><span data-stu-id="47431-108">The following example uses the Fleet Management app.</span></span> <span data-ttu-id="47431-109">フリート管理アプリでは、ワークスペースに顧客、予約、および車両の合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="47431-109">In the Fleet Management app, the workspace shows the total number of customers, reservations, and vehicles.</span></span> <span data-ttu-id="47431-110">以前は、これらのカウントはターゲットとして AllCustomers、AllReservations、および AllVehicles を持っていた **pageLink** コントロールに起因していました。</span><span class="sxs-lookup"><span data-stu-id="47431-110">Previously, these counts came from a **pageLink** control that had AllCustomers, AllReservations, and AllVehicles as targets.</span></span> <span data-ttu-id="47431-111">**pageLink** コントロールは行を読み込み、カウントを実行しました。</span><span class="sxs-lookup"><span data-stu-id="47431-111">The **pageLink** control loaded the rows and did the count.</span></span> <span data-ttu-id="47431-112">(この方法は、推奨される方法ではありません。)</span><span class="sxs-lookup"><span data-stu-id="47431-112">(This approach isn't the recommended approach.)</span></span>

<span data-ttu-id="47431-113">推奨される方法を使用するようワークスペース ページをコンフィギュレーションするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="47431-113">Follow these steps to configure the workspace page to use the recommended approach.</span></span>

1. <span data-ttu-id="47431-114">サーバーで、サーバー上のフィールドを含む新しいフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="47431-114">On the server, create a new form to contain fields that are also on the server.</span></span> <span data-ttu-id="47431-115">(既存のフォームに新しいフィールドを追加することもできます。)</span><span class="sxs-lookup"><span data-stu-id="47431-115">(You can also add the new fields to an existing form).</span></span> <span data-ttu-id="47431-116">次の図では、3 つのフィールドがある新しい **FMMobSummary** フォームが作成されます。</span><span class="sxs-lookup"><span data-stu-id="47431-116">In the following illustration, a new **FMMobSummary** form is created that has three fields.</span></span>

    ![3 つのフィールドを含むフォーム](media/optimizing-workspace/FMMobSummary.png)

2. <span data-ttu-id="47431-118">**FMMobSummary** フォームのモバイル アプリ デザイナーを使用してページを作成します。</span><span class="sxs-lookup"><span data-stu-id="47431-118">Create a page by using the mobile app designer for the **FMMobSummary** form.</span></span>

    ![デザイナーでの新しいページ](media/optimizing-workspace/NewPageInDesigner.png)

3. <span data-ttu-id="47431-120">フィールドを **pageLink** コントロールに変換する業務ロジックを更新します。</span><span class="sxs-lookup"><span data-stu-id="47431-120">Update the business logic to transform the fields into a **pageLink** control.</span></span> <span data-ttu-id="47431-121">フィールドにナビゲーション ターゲットを追加するには **configureControl** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="47431-121">Use the **configureControl** method to add a navigation target to the fields.</span></span> <span data-ttu-id="47431-122">フィールドは、次に **pageLink** コントロールとして設定されます。</span><span class="sxs-lookup"><span data-stu-id="47431-122">The fields are then configured as **pageLink** controls.</span></span> <span data-ttu-id="47431-123">**configureControl** メソッドの引数は、ページ名、コントロール名、および更新が必要なプロパティのオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="47431-123">The arguments for the **configureControl** method are the page name, the control name, and an object of properties that must be updated.</span></span>
4. <span data-ttu-id="47431-124">ワークスペースのデザインを更新します。</span><span class="sxs-lookup"><span data-stu-id="47431-124">Update the workspace design.</span></span> <span data-ttu-id="47431-125">ワークスペース ページの一部として概要ページを埋め込みします。</span><span class="sxs-lookup"><span data-stu-id="47431-125">Embed the summary page as a part in the workspace page.</span></span> <span data-ttu-id="47431-126">**pageLink** コントロールとして構成されるようになったフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="47431-126">Reference the fields that are now configured as **pageLink** controls.</span></span> <span data-ttu-id="47431-127">スタイルを提供して **showCount:true** プロパティを設定し、カウントが **pageLink** コントロールに表示されるようにします。</span><span class="sxs-lookup"><span data-stu-id="47431-127">Provide a style, and set the **showCount:true** property, so that the count is shown on the **pageLink** control.</span></span>

    ![ビジネス ロジックの変更](media/optimizing-workspace/ChangesToBL.png)

<span data-ttu-id="47431-129">この方法を使用することにより、**pageLink** コントロールのローカライズされたラベルも取得します。</span><span class="sxs-lookup"><span data-stu-id="47431-129">By using this approach, you also get the localized labels for **pageLink** controls.</span></span> <span data-ttu-id="47431-130">ワークスペースが読み込まれると、結果ははるかに高速になります。</span><span class="sxs-lookup"><span data-stu-id="47431-130">The result is a much faster experience when workspaces are loaded.</span></span>


---
title: 経費の委任の管理
description: 経費委任ユーザーは、組織内で別の従業員の代理として経費精算書を作成および管理できます。
author: KimANelson
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2020-01-10
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 0871017ebe111464e79800ef83b90931afb50df0
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124119"
---
# <a name="manage-expense-delegation"></a><span data-ttu-id="357f3-103">経費の委任の管理</span><span class="sxs-lookup"><span data-stu-id="357f3-103">Manage expense delegation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="357f3-104">経費委任ユーザーは、組織内で別の従業員の代理として経費精算書を作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="357f3-104">An expense delegate user can create and manage expense reports on behalf of another employee in the organization.</span></span>

## <a name="configuring-expense-delegation"></a><span data-ttu-id="357f3-105">経費の委任のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="357f3-105">Configuring expense delegation</span></span>

<span data-ttu-id="357f3-106">ユーザーを経費委任者として設定するには、**経費管理 > 設定 > 一般 > 委任**に移動して**委任**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="357f3-106">To set up a user as an expense delegate, go to **Expense management > Setup > General > Delegates** to open the **Delegates** page.</span></span> <span data-ttu-id="357f3-107">**新規**を選択し、定義した委任を持たせる従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="357f3-107">Select **New** and then select the employee that will have a delegate defined.</span></span> <span data-ttu-id="357f3-108">委任ユーザーのエイリアスと、委任期間の開始日と終了日を入力します。</span><span class="sxs-lookup"><span data-stu-id="357f3-108">Enter the alias of the delegate user and the start and end date for the delegation period.</span></span>

## <a name="managing-expense-delegation-on-behalf-of-another-employee"></a><span data-ttu-id="357f3-109">別の従業員に代わって経費の委任を管理する</span><span class="sxs-lookup"><span data-stu-id="357f3-109">Managing expense delegation on behalf of another employee</span></span>

<span data-ttu-id="357f3-110">機能管理キーの**委任リストページの有効化**がオンになっている場合、**自分に委任された経費**リスト ページが使用できるようになるために、**経費管理 > 自分の経費 > 自分に委任された経費**に移動します。</span><span class="sxs-lookup"><span data-stu-id="357f3-110">If the feature management key **Enable expense delegates list page** is enabled, the **Expenses delegated to me** list page will be available by navigating to **Expense management > My expenses > Expenses delegated to me**.</span></span>

<span data-ttu-id="357f3-111">委任ユーザーは、ユーザーに委任された既存の経費精算書をすばやくフィルタ処理し、検索することができます。</span><span class="sxs-lookup"><span data-stu-id="357f3-111">A delegate user can quickly filter and search on existing expense reports that hae been delegated to the user.</span></span> <span data-ttu-id="357f3-112">ユーザーは、**新しい経費精算書**をクリックして、他のユーザーの代わりに新しい経費精算書をすばやく作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="357f3-112">The user can also quickly create a new expense report on behalf of other users by clicking **New expense report**.</span></span>

<span data-ttu-id="357f3-113">委任ユーザーは、他の従業員に代わって経費精算書を作成および管理することもできるようになるために、**経費管理 > 自分の経費 > 経費精算書**に移動して、**その他のユーザーの経費**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="357f3-113">Delegate users can also create and manage expense reports on behalf of other employees by navigating to **Expense management > My expenses > Expense reports** and clicking the **Open other user's expenses** button.</span></span>

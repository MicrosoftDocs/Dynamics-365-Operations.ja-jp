---
title: プロセスの自動化
description: このトピックでは、プロセスの自動化を使用して、バッチ サーバーによって実行されるプロセスを簡単にスケジューリングする方法について詳しく説明します。
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 479f621ef05519f4f2c97112a0115dccdbf24c52
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682512"
---
# <a name="process-automation"></a><span data-ttu-id="02491-103">プロセスの自動化</span><span class="sxs-lookup"><span data-stu-id="02491-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="02491-104">プロセスの自動化を使用すると、バッチ サーバーによって実行されるプロセスを簡単にスケジューリングすることができます。</span><span class="sxs-lookup"><span data-stu-id="02491-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="02491-105">更新されたスケジュール済作業のカレンダー表示では、、エンド ユーザーがスケジュール済および完了済の作業を表示してアクションを実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="02491-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="02491-106">管理</span><span class="sxs-lookup"><span data-stu-id="02491-106">Administration</span></span>

<span data-ttu-id="02491-107">すべてのプロセス自動化の全体管理ページは、システム管理モジュールの **設定** メニューにあります。</span><span class="sxs-lookup"><span data-stu-id="02491-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="02491-108">このページには、システムで設定されているすべての自動化されたプロセス (シリーズ) が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="02491-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="02491-109">また、このページから新しいプロセスの自動化を直接追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="02491-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="02491-110">シリーズを設定した後は、この一覧から各シリーズを管理できます。</span><span class="sxs-lookup"><span data-stu-id="02491-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="02491-111">スケジュール済の作業をしばらく一時停止する場合は、シリーズ全体を編集するか、削除するか、リスト ビューにすべての発生を表示するか、シリーズを無効にするかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="02491-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="02491-112">機能を無効にしても、機能管理で無効になっているプロセスは表示されません。</span><span class="sxs-lookup"><span data-stu-id="02491-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="02491-113">さらに、プロセス自動化スケジューリング エンジンでは、無効な機能に対して発生またはバックグラウンド プロセスがスケジュールされることはありません。</span><span class="sxs-lookup"><span data-stu-id="02491-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="02491-114">機能を再度有効にすると、過去のすべてのスケジュールされた出来事またはバックグラウンド プロセスが直ちに実行されます。</span><span class="sxs-lookup"><span data-stu-id="02491-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="02491-115">カレンダー表示</span><span class="sxs-lookup"><span data-stu-id="02491-115">Calendar view</span></span>

<span data-ttu-id="02491-116">プロセス自動化の主な利点の 1 つとして、スケジュール済の作業を単純なカレンダー表示で確認できる機能があります。</span><span class="sxs-lookup"><span data-stu-id="02491-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="02491-117">この表示では、一度に 1 週間の作業を表示できます。</span><span class="sxs-lookup"><span data-stu-id="02491-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="02491-118">このビューは、**プロセスの自動化** ページの右側に表示されます。</span><span class="sxs-lookup"><span data-stu-id="02491-118">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="02491-119">選択したシリーズのスケジュール済の作業が設定されます。</span><span class="sxs-lookup"><span data-stu-id="02491-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="02491-120">[![プロセス自動化カレンダー](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="02491-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="02491-121">発生の変更</span><span class="sxs-lookup"><span data-stu-id="02491-121">Occurrence changes</span></span>

<span data-ttu-id="02491-122">それぞれの発生は、その発生を作成したシリーズによって定義されている他の発生に影響を与えることなく変更できます。</span><span class="sxs-lookup"><span data-stu-id="02491-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="02491-123">スケジュール済の作業の発生をカレンダー表示から編集するには、**表示/編集** ボタンを選択して **発生** を選択します。</span><span class="sxs-lookup"><span data-stu-id="02491-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="02491-124">このページにより、シリーズの設定ウィザードで最初に表示されたすべての設定にアクセスでき、選択した発生に対して 1 回限りの変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="02491-124">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="02491-125">スケジュール済の作業の発生は、カレンダー表示の **無効** ボタンを選択することによって無効にすることもできます。</span><span class="sxs-lookup"><span data-stu-id="02491-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="02491-126">開発者のドキュメント</span><span class="sxs-lookup"><span data-stu-id="02491-126">Developer documentation</span></span>

<span data-ttu-id="02491-127">プロセス自動化フレームワークを使用すると、開発者はプロセス自動化フレームワークを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="02491-127">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="02491-128">[プロセス自動化フレームワーク](../process-automation/process-automation-framework.md) ドキュメントでは、プロセス自動化ウィザードでスケジュールされたバッチ サーバーによって実行され、カレンダー表示に自動的に表示される必要があるカスタム プロセスを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="02491-128">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>

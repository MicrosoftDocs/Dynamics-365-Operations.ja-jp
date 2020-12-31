---
title: プロセスの自動化のフレームワークの開発
description: このトピックでは、プロセス自動化フレームワークを使用する開発の概要について説明します。
author: RyanCCarlson2
manager: AnnBe
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 44f85c7805f4cc36067e184ff24de14dea7941b4
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685415"
---
# <a name="process-automation-framework-development"></a><span data-ttu-id="a528f-103">プロセスの自動化のフレームワークの開発</span><span class="sxs-lookup"><span data-stu-id="a528f-103">Process automation framework development</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a528f-104">プロセスの自動化を使用すると、バッチ サーバーによって実行されるプロセスを簡単にスケジューリングすることができます。</span><span class="sxs-lookup"><span data-stu-id="a528f-104">Process automation enables simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="a528f-105">プロセス自動化フレームワークは、プロセスの自動化を実装できる API のセットです。</span><span class="sxs-lookup"><span data-stu-id="a528f-105">The process automation framework is a set of APIs that lets you implement process automation.</span></span>

<span data-ttu-id="a528f-106">プロセスの自動化を実装するには、パブリック API のみを使用し、次のガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a528f-106">You should use only the public APIs to implement process automation, and you should follow these guidelines:</span></span>

- <span data-ttu-id="a528f-107">プロセス自動化テーブルから選択、挿入、または直接参照を行わないでください。</span><span class="sxs-lookup"><span data-stu-id="a528f-107">Don't select from, insert into, or directly reference the process automation tables.</span></span>
- <span data-ttu-id="a528f-108">フレームワークを拡張したり、コードをクラスに統合したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="a528f-108">Don't extend the framework or integrate your code with the classes.</span></span>
- <span data-ttu-id="a528f-109">挿入、更新、削除などのテーブル イベントにはサブスクライブしないでください。</span><span class="sxs-lookup"><span data-stu-id="a528f-109">Don't subscribe to table events such as insert, update, and delete.</span></span> <span data-ttu-id="a528f-110">Finance and Operations アプリは、これらのイベントのほとんどをスキップします。</span><span class="sxs-lookup"><span data-stu-id="a528f-110">Finance and Operations apps skip most of those events.</span></span>
- <span data-ttu-id="a528f-111">必要な機能が不足している場合は、機能要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="a528f-111">If functionality that you require is missing, submit feature requests.</span></span>

<span data-ttu-id="a528f-112">Microsoft は今後の機能追加を計画します。</span><span class="sxs-lookup"><span data-stu-id="a528f-112">Microsoft plans to add features in the future.</span></span> <span data-ttu-id="a528f-113">プロセス自動化フレームワークに深く統合しすぎると、これらの機能が追加された場合に統合が機能しなくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a528f-113">If you integrate too deeply with the process automation framework, your integration might break when those features are added.</span></span>

<span data-ttu-id="a528f-114">プロセス自動化フレームワークの一部の例は、リリース品質コードを代表するものではありません。</span><span class="sxs-lookup"><span data-stu-id="a528f-114">Some of the examples for the process automation framework aren't representative of release-quality code.</span></span> <span data-ttu-id="a528f-115">フレームワークを使用して構築されたプロセスは、常にすべてのベスト プラクティスと品質基準に準拠していることが期待されます。</span><span class="sxs-lookup"><span data-stu-id="a528f-115">As always, the expectation is that processes that are built by using the framework will follow all best practices and quality standards.</span></span>

<span data-ttu-id="a528f-116">プロセス自動化の詳細については、[プロセスの自動化](../sysadmin/process-automation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a528f-116">For more information about process automation, see [Process automation](../sysadmin/process-automation.md).</span></span>

## <a name="definitions"></a><span data-ttu-id="a528f-117">定義</span><span class="sxs-lookup"><span data-stu-id="a528f-117">Definitions</span></span>

| <span data-ttu-id="a528f-118">相談</span><span class="sxs-lookup"><span data-stu-id="a528f-118">Term</span></span>               | <span data-ttu-id="a528f-119">定義</span><span class="sxs-lookup"><span data-stu-id="a528f-119">Definition</span></span> |
|--------------------|------------|
| <span data-ttu-id="a528f-120">呼び出し</span><span class="sxs-lookup"><span data-stu-id="a528f-120">Poller</span></span>             | <span data-ttu-id="a528f-121">呼び出しは、毎分実施される重要なシステムのバッチ プロセスで、プロセス自動化フレームワークのさまざまなサブシステムを起動します。</span><span class="sxs-lookup"><span data-stu-id="a528f-121">The poller is a system-critical batch process that runs every minute and invokes various subsystems of the process automation framework.</span></span> <span data-ttu-id="a528f-122">スケジュールを参照して、実行する準備ができているプロセスを判別し、フレームワークのランタイム側を起動して、プロセスが確実に実行されるようにします。</span><span class="sxs-lookup"><span data-stu-id="a528f-122">It consults the schedule to determine which processes are ready to run, and then it invokes the runtime side of the framework to ensure that processes are run.</span></span> |
| <span data-ttu-id="a528f-123">スケジュール済プロセス</span><span class="sxs-lookup"><span data-stu-id="a528f-123">Scheduled process</span></span>  | <span data-ttu-id="a528f-124">スケジュール済プロセスとは、ユーザーによってユーザー インターフェイス (UI) でスケジュールされたプロセスのことです。</span><span class="sxs-lookup"><span data-stu-id="a528f-124">A scheduled process is a process that is scheduled in the user interface (UI) by a user.</span></span> <span data-ttu-id="a528f-125">これらのプロセスの発生は、カレンダー表示できます。</span><span class="sxs-lookup"><span data-stu-id="a528f-125">Occurrences for these processes can be seen in a calendar view.</span></span> |
| <span data-ttu-id="a528f-126">バックグラウンド プロセス</span><span class="sxs-lookup"><span data-stu-id="a528f-126">Background process</span></span> | <span data-ttu-id="a528f-127">バックグラウンド プロセスは、*ポーリング プロセス* とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a528f-127">A background process is also known as a *polled process*.</span></span> <span data-ttu-id="a528f-128">これはユーザーの入力を必要とせずに頻繁に実行されるプロセスで、バックグラウンド プロセスを実行します。</span><span class="sxs-lookup"><span data-stu-id="a528f-128">It's a process that runs frequently, without requiring user input, and performs some background processing.</span></span> <span data-ttu-id="a528f-129">一般会計への補助元帳の転送はひとつの例です。</span><span class="sxs-lookup"><span data-stu-id="a528f-129">Subledger transfer to the general ledger is an example.</span></span> |
| <span data-ttu-id="a528f-130">種類</span><span class="sxs-lookup"><span data-stu-id="a528f-130">Type</span></span>               | <span data-ttu-id="a528f-131">このトピックおよび関連トピックでは、[タイプ登録](type-registration.md)で説明したように、*タイプ* という用語は **ProcessScheduleType** を指します。</span><span class="sxs-lookup"><span data-stu-id="a528f-131">In this topic and related topics, the term *type* refers to **ProcessScheduleType**, as discussed in [Type registration](type-registration.md).</span></span> |
| <span data-ttu-id="a528f-132">シリーズ</span><span class="sxs-lookup"><span data-stu-id="a528f-132">Series</span></span>             | <span data-ttu-id="a528f-133">登録済タイプのすべてのプロセスには、シリーズが必要です。</span><span class="sxs-lookup"><span data-stu-id="a528f-133">Every process that has a registered type must have a series.</span></span> <span data-ttu-id="a528f-134">スケジュール済プロセスのシリーズは、ユーザーによって UI の中に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a528f-134">Series for scheduled processes are created in the UI by users.</span></span> <span data-ttu-id="a528f-135">バックグラウンド プロセスのためのシリーズは、シリーズの登録を通じて作成されます。</span><span class="sxs-lookup"><span data-stu-id="a528f-135">Series for background processes are created through series registration.</span></span> <span data-ttu-id="a528f-136">詳細については、[シリーズ登録](series-registration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a528f-136">For more information, see [Series registration](series-registration.md).</span></span> |
| <span data-ttu-id="a528f-137">日時</span><span class="sxs-lookup"><span data-stu-id="a528f-137">Date and time</span></span>      | <span data-ttu-id="a528f-138">すべてのフレームワークの日付は協定世界時 (UTC) で保存されますが、ユーザーの優先タイムゾーンに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a528f-138">All framework dates are stored in Coordinated Universal Time (UTC) but shown in the user's preferred time zone.</span></span> |

## <a name="tasks"></a><span data-ttu-id="a528f-139">仕事</span><span class="sxs-lookup"><span data-stu-id="a528f-139">Tasks</span></span>

<span data-ttu-id="a528f-140">プロセス自動化ソリューションの実装は、一連のタスクで構成され、必須タスクとオプション タスクがあります。</span><span class="sxs-lookup"><span data-stu-id="a528f-140">Implementation of a process automation solution consists of a set of tasks, some of which are required and some of which are optional.</span></span>

<span data-ttu-id="a528f-141">UI のカスタマイズのほとんどは、バックグラウンド プロセスでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a528f-141">Most of the UI customizations aren't supported for background processes.</span></span> <span data-ttu-id="a528f-142">**シリーズ** リスト ページ、および結果とメッセージのログがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a528f-142">The **Series** list page and logging of results and messages are supported.</span></span>

| <span data-ttu-id="a528f-143">タスク</span><span class="sxs-lookup"><span data-stu-id="a528f-143">Task</span></span>                                                | <span data-ttu-id="a528f-144">スケジュール済プロセスに必須</span><span class="sxs-lookup"><span data-stu-id="a528f-144">Required for a scheduled process</span></span> | <span data-ttu-id="a528f-145">バックグラウンド プロセスに必須</span><span class="sxs-lookup"><span data-stu-id="a528f-145">Required for a background process</span></span> |
|-----------------------------------------------------|----------------------------------|-----------------------------------|
| [<span data-ttu-id="a528f-146">タイプ登録</span><span class="sxs-lookup"><span data-stu-id="a528f-146">Type registration</span></span>](type-registration.md)           | <span data-ttu-id="a528f-147">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-147">Yes</span></span> | <span data-ttu-id="a528f-148">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-148">Yes</span></span> |
| [<span data-ttu-id="a528f-149">シリーズ登録</span><span class="sxs-lookup"><span data-stu-id="a528f-149">Series registration</span></span>](series-registration.md)       | <span data-ttu-id="a528f-150">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="a528f-150">Not supported</span></span> | <span data-ttu-id="a528f-151">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-151">Yes</span></span> |
| [<span data-ttu-id="a528f-152">プロセス パラメーター</span><span class="sxs-lookup"><span data-stu-id="a528f-152">Process parameters</span></span>](process-parameters.md)         | <span data-ttu-id="a528f-153">なし</span><span class="sxs-lookup"><span data-stu-id="a528f-153">No</span></span> | <span data-ttu-id="a528f-154">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="a528f-154">Not supported</span></span> |
| [<span data-ttu-id="a528f-155">構成可能なユーザーのクエリ</span><span class="sxs-lookup"><span data-stu-id="a528f-155">User-configurable queries</span></span>](user-queries.md)        | <span data-ttu-id="a528f-156">なし</span><span class="sxs-lookup"><span data-stu-id="a528f-156">No</span></span> | <span data-ttu-id="a528f-157">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="a528f-157">Not supported</span></span> |
| [<span data-ttu-id="a528f-158">プロセスの実行</span><span class="sxs-lookup"><span data-stu-id="a528f-158">Run processes</span></span>](run-process.md)                     | <span data-ttu-id="a528f-159">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-159">Yes</span></span> | <span data-ttu-id="a528f-160">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-160">Yes</span></span> |
| [<span data-ttu-id="a528f-161">結果とメッセージを記録する</span><span class="sxs-lookup"><span data-stu-id="a528f-161">Log results and messages</span></span>](log-results.md)          | <span data-ttu-id="a528f-162">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-162">Yes</span></span> | <span data-ttu-id="a528f-163">あり</span><span class="sxs-lookup"><span data-stu-id="a528f-163">Yes</span></span> |
| [<span data-ttu-id="a528f-164">ユーザー インターフェイスのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="a528f-164">Customize the user interface</span></span>](ui-customization.md) | <span data-ttu-id="a528f-165">なし</span><span class="sxs-lookup"><span data-stu-id="a528f-165">No</span></span> | <span data-ttu-id="a528f-166">[ユーザー インターフェイスのカスタマイズ](ui-customization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a528f-166">See [Customize the user interface](ui-customization.md).</span></span> |

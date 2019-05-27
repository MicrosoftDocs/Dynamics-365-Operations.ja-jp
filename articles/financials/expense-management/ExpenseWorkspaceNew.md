---
title: 経費精算書の再設計
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の経費精算書エントリのために再設計され再考された経験に関する情報を提供します。 この新しいエクスペリエンスにより、経費精算書を完成させるプロセスが簡略化され、必要な時間が短縮されます。
author: ryansandness
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 3039cda3f2cf9259ca06207bdf941bc6b0fb28e1
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538696"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="a6274-104">経費精算書の再設計</span><span class="sxs-lookup"><span data-stu-id="a6274-104">Expense reports reimagined</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="a6274-105">経費精算書エントリは、経費精算書の完成単純化および必要な時間を節約するために再設計されています。</span><span class="sxs-lookup"><span data-stu-id="a6274-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="a6274-106">新しい経費のエクスペリエンスに関する主なコンポーネントは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a6274-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="a6274-107">委任経費にアクセスできる新しい経費管理ワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="a6274-108">新しいレシート照合エクスペリエンスにより、ヘッダーレベルの入庫をより良く表示し、経費明細行にレシートを添付するプロセスを簡略化することができます。</span><span class="sxs-lookup"><span data-stu-id="a6274-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="a6274-109">新しい読み取り専用グリッドで、多数の経費明細行と追加のデータ列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a6274-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="a6274-110">明細行と分割行をすべて表示して、親経費と共に表示できます。</span><span class="sxs-lookup"><span data-stu-id="a6274-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="a6274-111">経費を編集するための簡略化されたウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="a6274-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="a6274-112">問題の内容および解決方法を理解するための正しいコンテキストがあることを保証するための再設計されたエラー、警告およびポリシー メッセージ。</span><span class="sxs-lookup"><span data-stu-id="a6274-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="a6274-113">Microsoft は、ユーザーが作業を完了する前、および箇条書きメッセージのような不完全な問題に取り組む前に現れた数々のメッセージを解決しました。</span><span class="sxs-lookup"><span data-stu-id="a6274-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="a6274-114">組織で必要なフィールド、オプションのフィールド、およびキャプチャしないフィールドを指定するための新しいページ。</span><span class="sxs-lookup"><span data-stu-id="a6274-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="a6274-115">このページでは、ユーザーが設定する必要があるフィールドの数を減らします。</span><span class="sxs-lookup"><span data-stu-id="a6274-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="a6274-116">経費精算書の新しい概観により、もはや精算書が会計担当者向けに設計されたようには見えません。</span><span class="sxs-lookup"><span data-stu-id="a6274-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="a6274-117">新しいエクスペリエンスを有効にするには、**機能管理**ワークスペースを使用して、**経費精算書の再設計**機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="a6274-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="a6274-118">この機能をオンにすると、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="a6274-119">既存の経費ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a6274-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="a6274-120">経費フィールド表示の新しいメニュー項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="a6274-121">経費精算書 (既存のページ) の既存のメニュー項目または経費精算書のフィールドは削除されません。</span><span class="sxs-lookup"><span data-stu-id="a6274-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="a6274-122">ワークフローと承認を行っても、既存の経費精算書ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="a6274-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="a6274-123">新しいユーザー向けビデオの使用にあたり</span><span class="sxs-lookup"><span data-stu-id="a6274-123">Getting started video for new users</span></span>

<span data-ttu-id="a6274-124">経費エントリの主要な機能を表示する短いビデオを見ることができます。</span><span class="sxs-lookup"><span data-stu-id="a6274-124">You can watch a short video that shows the main features of expense entry.</span></span>

> [!NOTE]
> <span data-ttu-id="a6274-125">ビデオはまだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="a6274-125">The video isn't available yet.</span></span> <span data-ttu-id="a6274-126">このトピックでは、ビデオが使用可能になったときに更新されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-126">This topic will be updated when the video is available.</span></span>

## <a name="new-features"></a><span data-ttu-id="a6274-127">新機能</span><span class="sxs-lookup"><span data-stu-id="a6274-127">New features</span></span>

| <span data-ttu-id="a6274-128">新機能</span><span class="sxs-lookup"><span data-stu-id="a6274-128">New feature</span></span> | <span data-ttu-id="a6274-129">説明</span><span class="sxs-lookup"><span data-stu-id="a6274-129">Description</span></span> |
|---|----|
| <span data-ttu-id="a6274-130">経費フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="a6274-130">Expense field visibility</span></span> | <span data-ttu-id="a6274-131">新しい設定ページでは、組織に対して無効となるフィールド、どのフィールドを必須とするか、および推奨されるフィールドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a6274-131">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="a6274-132">必須フィールド</span><span class="sxs-lookup"><span data-stu-id="a6274-132">Required fields</span></span> | <span data-ttu-id="a6274-133">新しい単純なコンフィギュレーションを使用すると、ポリシー フレームワークを使用しなくてもいくつかのフィールドを必要に応じて作成できます。</span><span class="sxs-lookup"><span data-stu-id="a6274-133">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="a6274-134">オプション フィールド</span><span class="sxs-lookup"><span data-stu-id="a6274-134">Optional fields</span></span> | <span data-ttu-id="a6274-135">省略可能なフィールドの 2 番目のページが追加されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-135">A second page for optional fields is added.</span></span> <span data-ttu-id="a6274-136">これにより、従業員はフィールドを設定する必要はありませんが、フィールドは簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a6274-136">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="a6274-137">未添付の領収書を追加</span><span class="sxs-lookup"><span data-stu-id="a6274-137">Add unattached receipts</span></span> | <span data-ttu-id="a6274-138">経費精算書に未添付の精算書を追加する機能は、ワークスペースおよび経費精算書にさらに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-138">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="a6274-139">メッセージングの強化</span><span class="sxs-lookup"><span data-stu-id="a6274-139">Improved messaging</span></span> | <span data-ttu-id="a6274-140">警告またはエラーのある経費明細行の方が見やすいです。</span><span class="sxs-lookup"><span data-stu-id="a6274-140">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="a6274-141">メッセージ バーのメッセージの減少</span><span class="sxs-lookup"><span data-stu-id="a6274-141">Reduction in messages in the message bar</span></span>| <span data-ttu-id="a6274-142">情報ログ メッセージの数が減少し、重複メッセージが表示されないようにするための作業が行われました。</span><span class="sxs-lookup"><span data-stu-id="a6274-142">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="a6274-143">グループ化された共通のアクション</span><span class="sxs-lookup"><span data-stu-id="a6274-143">Grouped together common actions</span></span> | <span data-ttu-id="a6274-144">このインターフェイスは、一般的な明細行レベル アクションのほとんどに新しいアクション ボタンが追加され、ヘッダーには省略記号ボタン (...) および比較的頻繁でないアクションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="a6274-144">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="a6274-145">可視性を高める新しいワークスペース</span><span class="sxs-lookup"><span data-stu-id="a6274-145">New workspace to increase visibility</span></span> | <span data-ttu-id="a6274-146">新しいワークスペースは、ユーザーが別のエリアに移動するための機能およびリンクを統一します。</span><span class="sxs-lookup"><span data-stu-id="a6274-146">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="a6274-147">経費作成時の既存の経費およびレシートの追加</span><span class="sxs-lookup"><span data-stu-id="a6274-147">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="a6274-148">経費精算書を作成するときに、すべてまたは選択した経費およびレシートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="a6274-148">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="a6274-149">為替レート計算機能</span><span class="sxs-lookup"><span data-stu-id="a6274-149">Exchange rate calculator</span></span> | <span data-ttu-id="a6274-150">為替レート計算機能が追加されており、この機能を使用すると、立て替えた複数通貨換算の為替レートを計算できます。</span><span class="sxs-lookup"><span data-stu-id="a6274-150">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="a6274-151">新しい経費明細行の保存および追加</span><span class="sxs-lookup"><span data-stu-id="a6274-151">Save and add new expense lines</span></span> | <span data-ttu-id="a6274-152">新しい経費が入力されると、**保存**と**新しい**ボタンの使用が可能となり、経費明細行をすばやく入力するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a6274-152">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="a6274-153">分割行と明細行のより良い可視性</span><span class="sxs-lookup"><span data-stu-id="a6274-153">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="a6274-154">明細行と分割行は経費の一覧に直接追加され、表示を強化し、ポリシー エラーまたはその他のエラーがあるかどうかを容易に判断できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a6274-154">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="a6274-155">明細表示時にレシートを表示</span><span class="sxs-lookup"><span data-stu-id="a6274-155">Show receipts during itemization</span></span> | <span data-ttu-id="a6274-156">明細表示時にレシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-156">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="a6274-157">最初のリリースは、経費エントリのシナリオに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="a6274-157">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="a6274-158">経費精算書のレビューまたは承認シナリオでは、既存の経費エントリ ページが引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-158">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="a6274-159">次の機能は既存のページに表示されますが、新しいページにはまだ存在しません。</span><span class="sxs-lookup"><span data-stu-id="a6274-159">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="a6274-160">これらの機能は、次の数リリースにわたって再紹介されます。</span><span class="sxs-lookup"><span data-stu-id="a6274-160">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="a6274-161">承認</span><span class="sxs-lookup"><span data-stu-id="a6274-161">Approvals</span></span>
- <span data-ttu-id="a6274-162">買掛金勘定承および会計を編集する機能</span><span class="sxs-lookup"><span data-stu-id="a6274-162">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="a6274-163">複数のエントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="a6274-163">Multiple entry points</span></span>
- <span data-ttu-id="a6274-164">出張費要求の統合</span><span class="sxs-lookup"><span data-stu-id="a6274-164">Travel requisition integration</span></span>
- <span data-ttu-id="a6274-165">経費フィールド表示のデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="a6274-165">Data entity for expense field visibility</span></span>
- <span data-ttu-id="a6274-166">日当経費のエントリ</span><span class="sxs-lookup"><span data-stu-id="a6274-166">Entry for per-diem expenses</span></span>
- <span data-ttu-id="a6274-167">明細行レベルのワークフロー</span><span class="sxs-lookup"><span data-stu-id="a6274-167">Line-level workflow</span></span>
- <span data-ttu-id="a6274-168">中間承認者のサポート</span><span class="sxs-lookup"><span data-stu-id="a6274-168">Interim approver support</span></span>
- <span data-ttu-id="a6274-169">高度な明細表示</span><span class="sxs-lookup"><span data-stu-id="a6274-169">Advanced itemization</span></span>

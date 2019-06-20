---
title: 経費精算書の再設計
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の経費精算書エントリのために再設計され再考された経験に関する情報を提供します。 この新しいエクスペリエンスにより、経費精算書を完成させるプロセスが簡略化され、必要な時間が短縮されます。
author: ryansandness
manager: AnnBe
ms.date: 05/20/2019
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
ms.openlocfilehash: c7a2b95456e812970b135d83f0f7e503310ce185
ms.sourcegitcommit: 97ed74889a09ef385f6ecbab69e84a05ff42ee41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/20/2019
ms.locfileid: "1592640"
---
# <a name="expense-reports-reimagined"></a><span data-ttu-id="78706-104">経費精算書の再設計</span><span class="sxs-lookup"><span data-stu-id="78706-104">Expense reports reimagined</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="78706-105">経費精算書エントリは、経費精算書の完成単純化および必要な時間を節約するために再設計されています。</span><span class="sxs-lookup"><span data-stu-id="78706-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="78706-106">新しい経費のエクスペリエンスに関する主なコンポーネントは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="78706-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="78706-107">委任経費にアクセスできる新しい経費管理ワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="78706-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="78706-108">新しいレシート照合エクスペリエンスにより、ヘッダーレベルの入庫をより良く表示し、経費明細行にレシートを添付するプロセスを簡略化することができます。</span><span class="sxs-lookup"><span data-stu-id="78706-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="78706-109">新しい読み取り専用グリッドで、多数の経費明細行と追加のデータ列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="78706-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="78706-110">明細行と分割行をすべて表示して、親経費と共に表示できます。</span><span class="sxs-lookup"><span data-stu-id="78706-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="78706-111">経費を編集するための簡略化されたウィンドウ。</span><span class="sxs-lookup"><span data-stu-id="78706-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="78706-112">問題の内容および解決方法を理解するための正しいコンテキストがあることを保証するための再設計されたエラー、警告およびポリシー メッセージ。</span><span class="sxs-lookup"><span data-stu-id="78706-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="78706-113">Microsoft は、ユーザーが作業を完了する前、および箇条書きメッセージのような不完全な問題に取り組む前に現れた数々のメッセージを解決しました。</span><span class="sxs-lookup"><span data-stu-id="78706-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="78706-114">組織で必要なフィールド、オプションのフィールド、およびキャプチャしないフィールドを指定するための新しいページ。</span><span class="sxs-lookup"><span data-stu-id="78706-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="78706-115">このページでは、ユーザーが設定する必要があるフィールドの数を減らします。</span><span class="sxs-lookup"><span data-stu-id="78706-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="78706-116">経費精算書の新しい概観により、もはや精算書が会計担当者向けに設計されたようには見えません。</span><span class="sxs-lookup"><span data-stu-id="78706-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="78706-117">新しいエクスペリエンスを有効にするには、**機能管理**ワークスペースを使用して、**経費精算書の再設計**機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="78706-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="78706-118">この機能をオンにすると、次のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="78706-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="78706-119">既存の経費ワークスペースは、新しいワークスペースに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="78706-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="78706-120">経費フィールド表示の新しいメニュー項目が追加されます。</span><span class="sxs-lookup"><span data-stu-id="78706-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="78706-121">経費精算書 (既存のページ) の既存のメニュー項目または経費精算書のフィールドは削除されません。</span><span class="sxs-lookup"><span data-stu-id="78706-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="78706-122">ワークフローと承認を行っても、既存の経費精算書ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="78706-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="78706-123">新しいユーザー向けビデオの使用にあたり</span><span class="sxs-lookup"><span data-stu-id="78706-123">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="78706-124">[Dynamics 365 for Finance and Operations の経費エクスペリエンス](https://youtu.be/Ocy-MsTvEE0) ビデオ (上記参照) は、YouTube で入手可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="78706-124">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="78706-125">新機能</span><span class="sxs-lookup"><span data-stu-id="78706-125">New features</span></span>

| <span data-ttu-id="78706-126">新機能</span><span class="sxs-lookup"><span data-stu-id="78706-126">New feature</span></span> | <span data-ttu-id="78706-127">説明</span><span class="sxs-lookup"><span data-stu-id="78706-127">Description</span></span> |
|---|----|
| <span data-ttu-id="78706-128">経費フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="78706-128">Expense field visibility</span></span> | <span data-ttu-id="78706-129">新しい設定ページでは、組織に対して無効となるフィールド、どのフィールドを必須とするか、および推奨されるフィールドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="78706-129">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="78706-130">必須フィールド</span><span class="sxs-lookup"><span data-stu-id="78706-130">Required fields</span></span> | <span data-ttu-id="78706-131">新しい単純なコンフィギュレーションを使用すると、ポリシー フレームワークを使用しなくてもいくつかのフィールドを必要に応じて作成できます。</span><span class="sxs-lookup"><span data-stu-id="78706-131">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="78706-132">オプション フィールド</span><span class="sxs-lookup"><span data-stu-id="78706-132">Optional fields</span></span> | <span data-ttu-id="78706-133">省略可能なフィールドの 2 番目のページが追加されます。</span><span class="sxs-lookup"><span data-stu-id="78706-133">A second page for optional fields is added.</span></span> <span data-ttu-id="78706-134">これにより、従業員はフィールドを設定する必要はありませんが、フィールドは簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="78706-134">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="78706-135">未添付の領収書を追加</span><span class="sxs-lookup"><span data-stu-id="78706-135">Add unattached receipts</span></span> | <span data-ttu-id="78706-136">経費精算書に未添付の精算書を追加する機能は、ワークスペースおよび経費精算書にさらに表示されます。</span><span class="sxs-lookup"><span data-stu-id="78706-136">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="78706-137">メッセージングの強化</span><span class="sxs-lookup"><span data-stu-id="78706-137">Improved messaging</span></span> | <span data-ttu-id="78706-138">警告またはエラーのある経費明細行の方が見やすいです。</span><span class="sxs-lookup"><span data-stu-id="78706-138">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="78706-139">メッセージ バーのメッセージの減少</span><span class="sxs-lookup"><span data-stu-id="78706-139">Reduction in messages in the message bar</span></span>| <span data-ttu-id="78706-140">情報ログ メッセージの数が減少し、重複メッセージが表示されないようにするための作業が行われました。</span><span class="sxs-lookup"><span data-stu-id="78706-140">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="78706-141">グループ化された共通のアクション</span><span class="sxs-lookup"><span data-stu-id="78706-141">Grouped together common actions</span></span> | <span data-ttu-id="78706-142">このインターフェイスは、一般的な明細行レベル アクションのほとんどに新しいアクション ボタンが追加され、ヘッダーには省略記号ボタン (...) および比較的頻繁でないアクションが追加されています。</span><span class="sxs-lookup"><span data-stu-id="78706-142">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="78706-143">可視性を高める新しいワークスペース</span><span class="sxs-lookup"><span data-stu-id="78706-143">New workspace to increase visibility</span></span> | <span data-ttu-id="78706-144">新しいワークスペースは、ユーザーが別のエリアに移動するための機能およびリンクを統一します。</span><span class="sxs-lookup"><span data-stu-id="78706-144">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="78706-145">経費作成時の既存の経費およびレシートの追加</span><span class="sxs-lookup"><span data-stu-id="78706-145">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="78706-146">経費精算書を作成するときに、すべてまたは選択した経費およびレシートを追加できます。</span><span class="sxs-lookup"><span data-stu-id="78706-146">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="78706-147">為替レート計算機能</span><span class="sxs-lookup"><span data-stu-id="78706-147">Exchange rate calculator</span></span> | <span data-ttu-id="78706-148">為替レート計算機能が追加されており、この機能を使用すると、立て替えた複数通貨換算の為替レートを計算できます。</span><span class="sxs-lookup"><span data-stu-id="78706-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="78706-149">新しい経費明細行の保存および追加</span><span class="sxs-lookup"><span data-stu-id="78706-149">Save and add new expense lines</span></span> | <span data-ttu-id="78706-150">新しい経費が入力されると、**保存**と**新しい**ボタンの使用が可能となり、経費明細行をすばやく入力するために役立ちます。</span><span class="sxs-lookup"><span data-stu-id="78706-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="78706-151">分割行と明細行のより良い可視性</span><span class="sxs-lookup"><span data-stu-id="78706-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="78706-152">明細行と分割行は経費の一覧に直接追加され、表示を強化し、ポリシー エラーまたはその他のエラーがあるかどうかを容易に判断できるようにします。</span><span class="sxs-lookup"><span data-stu-id="78706-152">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="78706-153">明細表示時にレシートを表示</span><span class="sxs-lookup"><span data-stu-id="78706-153">Show receipts during itemization</span></span> | <span data-ttu-id="78706-154">明細表示時にレシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="78706-154">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="78706-155">最初のリリースは、経費エントリのシナリオに重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="78706-155">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="78706-156">経費精算書のレビューまたは承認シナリオでは、既存の経費エントリ ページが引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="78706-156">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="78706-157">次の機能は既存のページに表示されますが、新しいページにはまだ存在しません。</span><span class="sxs-lookup"><span data-stu-id="78706-157">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="78706-158">これらの機能は、次の数リリースにわたって再紹介されます。</span><span class="sxs-lookup"><span data-stu-id="78706-158">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="78706-159">承認</span><span class="sxs-lookup"><span data-stu-id="78706-159">Approvals</span></span>
- <span data-ttu-id="78706-160">買掛金勘定承および会計を編集する機能</span><span class="sxs-lookup"><span data-stu-id="78706-160">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="78706-161">複数のエントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="78706-161">Multiple entry points</span></span>
- <span data-ttu-id="78706-162">出張費要求の統合</span><span class="sxs-lookup"><span data-stu-id="78706-162">Travel requisition integration</span></span>
- <span data-ttu-id="78706-163">経費フィールド表示のデータ エンティティ</span><span class="sxs-lookup"><span data-stu-id="78706-163">Data entity for expense field visibility</span></span>
- <span data-ttu-id="78706-164">日当経費のエントリ</span><span class="sxs-lookup"><span data-stu-id="78706-164">Entry for per-diem expenses</span></span>
- <span data-ttu-id="78706-165">明細行レベルのワークフロー</span><span class="sxs-lookup"><span data-stu-id="78706-165">Line-level workflow</span></span>
- <span data-ttu-id="78706-166">中間承認者のサポート</span><span class="sxs-lookup"><span data-stu-id="78706-166">Interim approver support</span></span>
- <span data-ttu-id="78706-167">高度な明細表示</span><span class="sxs-lookup"><span data-stu-id="78706-167">Advanced itemization</span></span>

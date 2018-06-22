---
title: "フォーム パターンの選択"
description: "このトピックでは、移行するフォームに最適なフォーム パターンを選択するのに役立つ情報を提供します。"
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 28681
ms.assetid: 09a51876-8c9d-41ed-ab81-b780894a4281
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f6c75e07557c9b32b81d597dca4e7cff7eb232d6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="select-a-form-pattern"></a><span data-ttu-id="fc8ca-103">フォーム パターンの選択</span><span class="sxs-lookup"><span data-stu-id="fc8ca-103">Select a form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc8ca-104">このトピックでは、移行するフォームに最適なフォーム パターンを選択するのに役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-104">This topic provides information that will help you select the best form pattern for the forms that you migrate.</span></span> 

<a name="introduction"></a><span data-ttu-id="fc8ca-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="fc8ca-105">Introduction</span></span>
------------

<span data-ttu-id="fc8ca-106">フォームパターンの選択は、フォームを移行するプロセスの重要なステップです。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-106">The selection of a form pattern is an important step in the process of migrating a form.</span></span> <span data-ttu-id="fc8ca-107">ターゲット フォームに最適なパターンでは、必要な移行作業の量が減少します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-107">A pattern that is a good fit for the target form reduces the amount of migration work that is required.</span></span> <span data-ttu-id="fc8ca-108">対照的に、適切ではないパターンは無駄な時間と労力を引き起こす可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-108">By contrast, a pattern that isn't a good fit can cause wasted time and effort.</span></span> <span data-ttu-id="fc8ca-109">したがって、移行するフォームに最適なフォーム パターンを選択できるよう、調査を行うことが重要です。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-109">Therefore, it's important that you do some investigation, so that you can select the best form pattern for the form that you're migrating.</span></span> <span data-ttu-id="fc8ca-110">フォームの適切なパターンを決定するためのガイダンスおよびヒントを次に示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-110">Here is some guidance and tips for determining the appropriate pattern for a form:</span></span>

-   <span data-ttu-id="fc8ca-111">フォーム デザイナーでフォームのメタデータを調べます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-111">Investigate the form’s metadata in the form designer.</span></span> <span data-ttu-id="fc8ca-112">よく注意して次の詳細を閉じてください。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-112">Pay close attention to the following details:</span></span>
    -   <span data-ttu-id="fc8ca-113">フォーム名</span><span class="sxs-lookup"><span data-stu-id="fc8ca-113">Form name</span></span>
    -   <span data-ttu-id="fc8ca-114">Form.Design.Style</span><span class="sxs-lookup"><span data-stu-id="fc8ca-114">Form.Design.Style</span></span>
    -   <span data-ttu-id="fc8ca-115">コントロール名</span><span class="sxs-lookup"><span data-stu-id="fc8ca-115">Control names</span></span>
    -   <span data-ttu-id="fc8ca-116">コントロールが整理される方法</span><span class="sxs-lookup"><span data-stu-id="fc8ca-116">The way that the controls are organized</span></span>
    -   <span data-ttu-id="fc8ca-117">番号とデータ ソースの名前</span><span class="sxs-lookup"><span data-stu-id="fc8ca-117">The number and names of the data sources</span></span>
-   <span data-ttu-id="fc8ca-118">フォームを実行して、情報が表示される方法を確認することでフォームのビジュアルを調べます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-118">Investigate the form’s visuals by running the form and looking at the way information is displayed.</span></span>

## <a name="selecting-a-form-pattern-via-metadata"></a><span data-ttu-id="fc8ca-119">メタデータを通じてフォーム パターンを選択</span><span class="sxs-lookup"><span data-stu-id="fc8ca-119">Selecting a form pattern via metadata</span></span>
### <a name="use-formdesignstyle-for-guidance"></a><span data-ttu-id="fc8ca-120">ガイダンスに Form.Design.Style を使用</span><span class="sxs-lookup"><span data-stu-id="fc8ca-120">Use Form.Design.Style for guidance</span></span>

<span data-ttu-id="fc8ca-121">**Form.Design.Style** プロパティには多くの場合、フォームの以前対象となっていたパターンの名前が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-121">The **Form.Design.Style** property often contains the name of the pattern that was previously targeted for the form.</span></span> <span data-ttu-id="fc8ca-122">**スタイル** プロパティはメタデータと正確に一致し、次の表を使用して、フォームに適合する可能性があるパターンを検出することができます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-122">If the **Style** property correctly matches the metadata, you can use the following table to find a pattern that is likely to be a good fit for the form.</span></span>

| <span data-ttu-id="fc8ca-123">Form.Design.Style value</span><span class="sxs-lookup"><span data-stu-id="fc8ca-123">Form.Design.Style value</span></span>                                                                          | <span data-ttu-id="fc8ca-124">対応するパターン</span><span class="sxs-lookup"><span data-stu-id="fc8ca-124">Corresponding pattern</span></span>                                                                                           |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ca-125">DetailsFormMaster</span><span class="sxs-lookup"><span data-stu-id="fc8ca-125">DetailsFormMaster</span></span>                                                                                | [<span data-ttu-id="fc8ca-126">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="fc8ca-126">Details Master</span></span>](details-master-form-pattern.md)                              |
| <span data-ttu-id="fc8ca-127">DetailsFormTransaction</span><span class="sxs-lookup"><span data-stu-id="fc8ca-127">DetailsFormTransaction</span></span>                                                                           | [<span data-ttu-id="fc8ca-128">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="fc8ca-128">Details Transaction</span></span>](details-transaction-form-pattern.md)                    |
| <span data-ttu-id="fc8ca-129">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-129">Dialog</span></span>                                                                                           | [<span data-ttu-id="fc8ca-130">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-130">Dialog</span></span>](dialog-form-pattern.md)                                              |
| <span data-ttu-id="fc8ca-131">DropDialog</span><span class="sxs-lookup"><span data-stu-id="fc8ca-131">DropDialog</span></span>                                                                                       | [<span data-ttu-id="fc8ca-132">ドロップ ダイアログ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-132">Drop Dialog</span></span>](drop-dialog-form-pattern.md)                                    |
| <span data-ttu-id="fc8ca-133">単なるフィールドが存在する FormPart</span><span class="sxs-lookup"><span data-stu-id="fc8ca-133">FormPart, where there are just fields</span></span>                                                            | [<span data-ttu-id="fc8ca-134">フォーム パート 情報ボックス カード</span><span class="sxs-lookup"><span data-stu-id="fc8ca-134">Form Part FactBox Card</span></span>](factbox-form-patterns.md)                            |
| <span data-ttu-id="fc8ca-135">グリッドが存在する FormPart</span><span class="sxs-lookup"><span data-stu-id="fc8ca-135">FormPart, where there is a grid</span></span>                                                                  | [<span data-ttu-id="fc8ca-136">フォーム パート 情報ボックス グリッド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-136">Form Part FactBox Grid</span></span>](factbox-form-patterns.md)                            |
| <span data-ttu-id="fc8ca-137">ListPage</span><span class="sxs-lookup"><span data-stu-id="fc8ca-137">ListPage</span></span>                                                                                         | [<span data-ttu-id="fc8ca-138">リスト ページ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-138">List Page</span></span>](list-page-form-pattern.md)                                        |
| <span data-ttu-id="fc8ca-139">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-139">Lookup</span></span>                                                                                           | [<span data-ttu-id="fc8ca-140">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-140">Lookup</span></span>](lookup-form-pattern.md)                                              |
| <span data-ttu-id="fc8ca-141">SimpleList</span><span class="sxs-lookup"><span data-stu-id="fc8ca-141">SimpleList</span></span>                                                                                       | [<span data-ttu-id="fc8ca-142">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-142">Simple List</span></span>](simple-list-form-pattern.md)                                    |
| <span data-ttu-id="fc8ca-143">ナビゲーション リストにフィールドが 2 ～ 3 個の場合は SimpleListDetails (推奨)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-143">SimpleListDetails, where there are 2–3 fields in the navigation list (recommended)</span></span>               | [<span data-ttu-id="fc8ca-144">簡易リストと詳細 – リスト グリッド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-144">Simple List Details – List Grid</span></span>](simple-list-details-form-pattern.md)    |
| <span data-ttu-id="fc8ca-145">ナビゲーション リストにフィールドが 4 ～ 5 個の場合は SimpleListDetails</span><span class="sxs-lookup"><span data-stu-id="fc8ca-145">SimpleListDetails, where there are and 4–5 fields in the navigation list</span></span>                         | [<span data-ttu-id="fc8ca-146">簡易リストと詳細 – 表形式のグリッド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-146">Simple List Details – Tabular Grid</span></span>](simple-list-details-form-pattern.md) |
| <span data-ttu-id="fc8ca-147">ツリーがある場合は SimpleListDetails (まれ)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-147">SimpleListDetails, where there is a tree (rare)</span></span>                                                  | [<span data-ttu-id="fc8ca-148">簡易リストと詳細 – ツリー</span><span class="sxs-lookup"><span data-stu-id="fc8ca-148">Simple List Details – Tree</span></span>](simple-list-details-form-pattern.md)         |
| <span data-ttu-id="fc8ca-149">TableOfContents</span><span class="sxs-lookup"><span data-stu-id="fc8ca-149">TableOfContents</span></span>                                                                                  | [<span data-ttu-id="fc8ca-150">目次</span><span class="sxs-lookup"><span data-stu-id="fc8ca-150">Table of Contents</span></span>](table-of-contents-form-pattern.md)                        |
| <span data-ttu-id="fc8ca-151">自動には**概要**タブ、**一般**タブ、および単一のデータ ソースが存在する</span><span class="sxs-lookup"><span data-stu-id="fc8ca-151">Auto, where there is an **Overview** tab, a **General** tab, and a single data source</span></span>            | [<span data-ttu-id="fc8ca-152">タスク シングル</span><span class="sxs-lookup"><span data-stu-id="fc8ca-152">Task Single</span></span>](task-single-form-pattern.md)                                    |
| <span data-ttu-id="fc8ca-153">自動には**概要**タブ、**一般**タブ、またはヘッダーを含めたラインの 2 つのセットが存在する</span><span class="sxs-lookup"><span data-stu-id="fc8ca-153">Auto, where there are two sets of **Overview** tabs, **General** tabs, and/or headers plus lines</span></span> | [<span data-ttu-id="fc8ca-154">タスク ダブル</span><span class="sxs-lookup"><span data-stu-id="fc8ca-154">Task Double</span></span>](task-double-form-pattern.md)                                    |
| <span data-ttu-id="fc8ca-155">自動には1 つのレコードにフォーカスが存在する</span><span class="sxs-lookup"><span data-stu-id="fc8ca-155">Auto, where there is focus on a single record</span></span>                                                    | [<span data-ttu-id="fc8ca-156">簡易詳細</span><span class="sxs-lookup"><span data-stu-id="fc8ca-156">Simple Details</span></span>](simple-details-form-pattern.md)                              |
| <span data-ttu-id="fc8ca-157">自動には「ルックアップ」で終了するフォーム名が存在する</span><span class="sxs-lookup"><span data-stu-id="fc8ca-157">Auto, where the form name ends in “Lookup”</span></span>                                                       | [<span data-ttu-id="fc8ca-158">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-158">Lookup</span></span>](lookup-form-pattern.md)                                              |
| <span data-ttu-id="fc8ca-159">自動には 1 つのタブ コントロールと**次へ**/**前へ**ボタンがある</span><span class="sxs-lookup"><span data-stu-id="fc8ca-159">Auto, where there is a single tab control and **Next**/**Previous** buttons</span></span>                      | [<span data-ttu-id="fc8ca-160">ウィザード</span><span class="sxs-lookup"><span data-stu-id="fc8ca-160">Wizard</span></span>](wizard-form-pattern.md)                                              |
| <span data-ttu-id="fc8ca-161">自動には「ウィザード」で終了するフォーム名が存在する</span><span class="sxs-lookup"><span data-stu-id="fc8ca-161">Auto, where the form name ends in “Wizard”</span></span>                                                       | [<span data-ttu-id="fc8ca-162">ウィザード</span><span class="sxs-lookup"><span data-stu-id="fc8ca-162">Wizard</span></span>](wizard-form-pattern.md)                                              |
| <span data-ttu-id="fc8ca-163">自動にはグリッドとボタンが存在する</span><span class="sxs-lookup"><span data-stu-id="fc8ca-163">Auto, where there is just a grid and some buttons</span></span>                                                | [<span data-ttu-id="fc8ca-164">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-164">Simple List</span></span>](simple-list-form-pattern.md)                                    |

###  <a name="when-a-form-doesnt-match-the-style-property"></a><span data-ttu-id="fc8ca-165">フォームが Style プロパティと一致しないとき</span><span class="sxs-lookup"><span data-stu-id="fc8ca-165">When a form doesn't match the Style property</span></span>

<span data-ttu-id="fc8ca-166">場合によっては、フォームに間違った **Form.Design.Style** プロパティ値があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-166">Sometimes, a form has an incorrect **Form.Design.Style** property value.</span></span>

| <span data-ttu-id="fc8ca-167">Form.Design.Style value</span><span class="sxs-lookup"><span data-stu-id="fc8ca-167">Form.Design.Style value</span></span> | <span data-ttu-id="fc8ca-168">可能性のあるフォームの実際の値</span><span class="sxs-lookup"><span data-stu-id="fc8ca-168">What the form might actually be</span></span>                                                                                  |
|-------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ca-169">DetailsFormMaster</span><span class="sxs-lookup"><span data-stu-id="fc8ca-169">DetailsFormMaster</span></span>       | <span data-ttu-id="fc8ca-170">DetailsFormTransaction、明細行の詳細がある場合、またはコントロールの名前に「明細行」を含む場合</span><span class="sxs-lookup"><span data-stu-id="fc8ca-170">DetailsFormTransaction, if there is lines detail, or if controls have names that contain “lines"</span></span>                 |
| <span data-ttu-id="fc8ca-171">SimpleList</span><span class="sxs-lookup"><span data-stu-id="fc8ca-171">SimpleList</span></span>              | <span data-ttu-id="fc8ca-172">グリッドが複数といくつかのカスタム フィルター フィールドがある場合は SimpleListDetails。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-172">SimpleListDetails, if there is more than just a grid and some custom filter fields</span></span>                               |
| <span data-ttu-id="fc8ca-173">SimpleListDetails</span><span class="sxs-lookup"><span data-stu-id="fc8ca-173">SimpleListDetails</span></span>       | <span data-ttu-id="fc8ca-174">グリッドが 1 つだけといくつかのカスタム フィルター フィールドがある場合は SimpleList。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-174">SimpleList, if there is just a grid and some custom filter fields</span></span>                                                |
| <span data-ttu-id="fc8ca-175">SimpleList</span><span class="sxs-lookup"><span data-stu-id="fc8ca-175">SimpleList</span></span>              | <span data-ttu-id="fc8ca-176">ListPage、**パーツ** ノードに数多くの情報ボックスがある場合、または対応する詳細フォームがそのフォームにある場合</span><span class="sxs-lookup"><span data-stu-id="fc8ca-176">ListPage, if there are numerous FactBoxes in the **Parts** node, or if the form has a corresponding Details Form</span></span> |

## <a name="selecting-a-form-pattern-via-visuals"></a><span data-ttu-id="fc8ca-177">ビジュアルを通じてフォーム パターンを選択</span><span class="sxs-lookup"><span data-stu-id="fc8ca-177">Selecting a form pattern via visuals</span></span>
<span data-ttu-id="fc8ca-178">この方法はフォームのメタデータを見るよりもあまり役に立ちませんが、フォームについて実行し調べることによってさまざまな情報を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-178">Although this approach is less useful than looking at the form metadata, you can get a lot of information about a form by running and examining it.</span></span> <span data-ttu-id="fc8ca-179">追加のデータ ポイントとしてフォーム ビジュアルを使用すると、フォーム パターンを選択するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-179">Use the form visuals as an additional data point to help you select a form pattern.</span></span> <span data-ttu-id="fc8ca-180">ターゲット フォームのようなフォームを見つけるために、移行したフォームのスクリーン ショットを参照します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-180">Look through the screen shots of migrated forms to find a form that looks like the target form.</span></span> <span data-ttu-id="fc8ca-181">また、パターンの記述または目的がフォームの説明/目的と一致していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-181">Additionally, make sure that the description or intent of the pattern matches the description/intent of the form.</span></span>

## <a name="selecting-a-form-pattern-via-the-designer"></a><span data-ttu-id="fc8ca-182">デザイナーを通じてフォーム パターンを選択</span><span class="sxs-lookup"><span data-stu-id="fc8ca-182">Selecting a form pattern via the designer</span></span>

<span data-ttu-id="fc8ca-183">ターゲット フォームの **デザイン** ノードを右クリックし、**パターンの適用** を選択して適用するパターンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-183">Right-click the **Design** node of the target form, select **Apply pattern**, and then click the pattern to apply.</span></span>

## <a name="form-pattern-reference-guide"></a><span data-ttu-id="fc8ca-184">フォームのパターンの参照ガイド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-184">Form pattern reference guide</span></span>
### <a name="list-of-classes-of-top-level-form-patterns"></a><span data-ttu-id="fc8ca-185">最上位レベルのフォーム パターンのクラスのリスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-185">List of classes of top-level form patterns</span></span>

| <span data-ttu-id="fc8ca-186">フォーム パターン</span><span class="sxs-lookup"><span data-stu-id="fc8ca-186">Form pattern</span></span>                                                                                                        | <span data-ttu-id="fc8ca-187">これは何に使用されますか ?</span><span class="sxs-lookup"><span data-stu-id="fc8ca-187">What it's used for</span></span>                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ca-188">[詳細マスター](details-master-form-pattern.md) (2 つのバリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-188">[Details Master](details-master-form-pattern.md) (two variants)</span></span>                   | <span data-ttu-id="fc8ca-189">複雑なエンティティの詳細を表示するフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-189">A form that displays the details of a complex entity</span></span>                                                                  |
| [<span data-ttu-id="fc8ca-190">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="fc8ca-190">Details Transaction</span></span>](details-transaction-form-pattern.md)                        | <span data-ttu-id="fc8ca-191">このフォームは、複雑なトランザクション エンティティとその行の詳細 (例えば、注文とその行) を表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-191">A form that displays the details of a complex transaction entity and its lines (for example, and order and its lines)</span></span> |
| <span data-ttu-id="fc8ca-192">[ダイアログ](dialog-form-pattern.md) (6 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-192">[Dialog](dialog-form-pattern.md) (six variants)</span></span>                                   | <span data-ttu-id="fc8ca-193">一連の情報を収集するダイアログとして使用されるフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-193">A form that is used as a dialog to gather a set of information</span></span>                                                        |
| <span data-ttu-id="fc8ca-194">[ドロップ ダイアログ](drop-dialog-form-pattern.md) (2 つのバリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-194">[Drop Dialog](drop-dialog-form-pattern.md) (two variants)</span></span>                         | <span data-ttu-id="fc8ca-195">アクションにコンテキストを提供するための小さな情報のセットを収集するためにドロップ ダイアログとして使用されるフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-195">A form that is used as a drop dialog to gather a small set of information to provide context for an action</span></span>            |
| <span data-ttu-id="fc8ca-196">[情報ボックス](factbox-form-patterns.md) (2 つのバリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-196">[FactBox](factbox-form-patterns.md) (two variants)</span></span>                                | <span data-ttu-id="fc8ca-197">関連するレコードまたはレコードのセットに関する情報を表示する Microsoft Dynamics AX 2012 FactBox。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-197">A Microsoft Dynamics AX 2012 FactBox that displays information about a related record or set of records</span></span>               |
| [<span data-ttu-id="fc8ca-198">リスト ページ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-198">List Page</span></span>](list-page-form-pattern.md)                                            | <span data-ttu-id="fc8ca-199">Dynamics AX 2012 のリスト ページ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-199">A Dynamics AX 2012 List Page</span></span>                                                                                          |
| <span data-ttu-id="fc8ca-200">[ルックアップ](lookup-form-pattern.md) (3 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-200">[Lookup](lookup-form-pattern.md) (three variants)</span></span>                                 | <span data-ttu-id="fc8ca-201">ルックアップとして使用されるフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-201">A form that is used as a lookup</span></span>                                                                                       |
| <span data-ttu-id="fc8ca-202">[簡易詳細](simple-details-form-pattern.md) (4 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-202">[Simple Details](simple-details-form-pattern.md) (four variants)</span></span>                  | <span data-ttu-id="fc8ca-203">1 つのレコードに特化したフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-203">A form that is focused on a single record</span></span>                                                                             |
| [<span data-ttu-id="fc8ca-204">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-204">Simple List</span></span>](simple-list-form-pattern.md)                                        | <span data-ttu-id="fc8ca-205">レコードあたり 10 未満のフィールドが含まれるグリッドとして簡易エンティティの詳細を表示するフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-205">A form that displays details for a simple entity as a grid that has fewer than 10 fields per record</span></span>                   |
| <span data-ttu-id="fc8ca-206">[簡易リストと詳細](simple-list-details-form-pattern.md) (3 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-206">[Simple List & Details](simple-list-details-form-pattern.md) (three variants)</span></span> | <span data-ttu-id="fc8ca-207">中規模な複雑さのエンティティに関する情報を表示するフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-207">A form that displays information about an entity of medium complexity</span></span>                                                 |
| [<span data-ttu-id="fc8ca-208">目次</span><span class="sxs-lookup"><span data-stu-id="fc8ca-208">Table of Contents</span></span>](table-of-contents-form-pattern.md)                            | <span data-ttu-id="fc8ca-209">セットアップ情報または大まかに関連する情報のセットが表示されるフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-209">A form that displays setup information or loosely related information sets</span></span>                                            |
| <span data-ttu-id="fc8ca-210">タスク (2 つのバリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-210">Task (two variants)</span></span>                                                                                                 | <span data-ttu-id="fc8ca-211">レガシ フォーム パターンは、マスタ エンティティまたはトランザクション エンティティを表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-211">A legacy form pattern that is used to display master or transaction entities</span></span>                                          |
| [<span data-ttu-id="fc8ca-212">ウィザード</span><span class="sxs-lookup"><span data-stu-id="fc8ca-212">Wizard</span></span>](wizard-form-pattern.md)                                                  | <span data-ttu-id="fc8ca-213">一定の順序に従って情報を収集するユーザーに一連のタブ ページを表示するフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-213">A form that displays a set of tab pages to the user to gather information in a predetermined order</span></span>                    |
| [<span data-ttu-id="fc8ca-214">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="fc8ca-214">Operational Workspace</span></span>](workspace-form-pattern.md)                                | <span data-ttu-id="fc8ca-215">活動の概要を表示するために使用され、ナビゲーションの主な手段を意味するフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-215">A form that is used to display an overview of an activity and is meant to be a primary means of navigation</span></span>            |
| <span data-ttu-id="fc8ca-216">ワークスペース パノラマ セクション (3 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-216">Workspace Panorama Sections (three variants)</span></span>                                                                        | <span data-ttu-id="fc8ca-217">運用ワークスペースに (フォームのパーツ コントロールを通じて) パノラマ セクションに内容を表示するためのフォーム</span><span class="sxs-lookup"><span data-stu-id="fc8ca-217">A form that is used to show content for a panorama section (via a Form Part Control) in the Operational Workspace</span></span>     |

### <a name="finding-forms-that-currently-use-a-particular-form-pattern"></a><span data-ttu-id="fc8ca-218">特定のフォーム パターンを現在使用しているフォームを検索</span><span class="sxs-lookup"><span data-stu-id="fc8ca-218">Finding forms that currently use a particular form pattern</span></span>

<span data-ttu-id="fc8ca-219">特定のフォーム パターンを現在使用しているフォームの一覧全体については、Microsoft Visual Studio 内から**フォーム パターン**レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-219">For a full list of forms that are currently using a particular form pattern, generate the **Form Patterns** report from within Microsoft Visual Studio.</span></span> <span data-ttu-id="fc8ca-220">レポートを実行する詳細については、[フォーム パターン アドイン](form-pattern-add-ins.md) を参照してください。Excel でレポートをフィルター処理し、特定のパターンを使用するフォームを検索できます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-220">For information on running the report, see [Form pattern add-ins](form-pattern-add-ins.md). You can filter the report in Excel to find forms that use a particular pattern.</span></span>

### <a name="form-pattern-visuals-and-descriptions"></a><span data-ttu-id="fc8ca-221">フォームのパターンのビジュアルと説明</span><span class="sxs-lookup"><span data-stu-id="fc8ca-221">Form pattern visuals and descriptions</span></span>

<span data-ttu-id="fc8ca-222">フォーム パターン クラスごとに、各バリアントに関する情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-222">For each form pattern class, information is provided about each variant.</span></span> <span data-ttu-id="fc8ca-223">この情報には、簡単な説明と例フォームの図が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-223">This information includes a short description and an illustration of an example form.</span></span>

#### <a name="details-master"></a><span data-ttu-id="fc8ca-224">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="fc8ca-224">Details Master</span></span>

<span data-ttu-id="fc8ca-225">[詳細マスター](details-master-form-pattern.md)\[既定\] このフォーム パターンは、クイック タブ上の複雑なエンティティの詳細を表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-225">[Details Master](details-master-form-pattern.md)\[Default\] This form pattern is used to display the details of a complex entity on FastTabs.</span></span> <span data-ttu-id="fc8ca-226">グリッド ビューと詳細ビューが含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-226">It includes a grid view and a details view.</span></span>

<span data-ttu-id="fc8ca-227">フォーム: CustTable</span><span class="sxs-lookup"><span data-stu-id="fc8ca-227">Form: CustTable</span></span> 

![image001](./media/image001.jpg)

![image002](./media/image002.jpg)

<span data-ttu-id="fc8ca-230">[詳細マスター / 標準タブ](details-master-form-pattern.md) フォームに多数のクイック タブ (>15) があり、カテゴリにグループ化できる場合は、この詳細マスター バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-230">[Details Master w/ Standard Tabs](details-master-form-pattern.md) Use this Details Master variant when your form has a large number of FastTabs (>15) that can be grouped into categories.</span></span>

<span data-ttu-id="fc8ca-231">フォーム: HcmWorker</span><span class="sxs-lookup"><span data-stu-id="fc8ca-231">Form: HcmWorker</span></span> 

<span data-ttu-id="fc8ca-232">[![image003](./media/image003.jpg)](./media/image003.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-232">[![image003](./media/image003.jpg)](./media/image003.jpg)</span></span>

<span data-ttu-id="fc8ca-233">[![HowToSelectAFormPattern(31)](./media/howtoselectaformpattern-31.jpg)](./media/howtoselectaformpattern-31.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-233">[![HowToSelectAFormPattern (31)](./media/howtoselectaformpattern-31.jpg)](./media/howtoselectaformpattern-31.jpg)</span></span>



#### <a name="details-transaction"></a><span data-ttu-id="fc8ca-234">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="fc8ca-234">Details Transaction</span></span>

<span data-ttu-id="fc8ca-235">[詳細トランザクション](details-transaction-form-pattern.md) このフォーム パターンを使用して、複雑なトランザクションエンティティとその行の詳細 (例えば、注文とその行) を表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-235">[Details Transaction](details-transaction-form-pattern.md) Use this form patter to show the details of a complex transaction entity and its lines (for example, an order and its lines).</span></span>

<span data-ttu-id="fc8ca-236">フォーム: SalesTable</span><span class="sxs-lookup"><span data-stu-id="fc8ca-236">Form: SalesTable</span></span> 

<span data-ttu-id="fc8ca-237">[![HowToSelectAFormPattern(32)](./media/howtoselectaformpattern-32.jpg)](./media/howtoselectaformpattern-32.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-237">[![HowToSelectAFormPattern (32)](./media/howtoselectaformpattern-32.jpg)](./media/howtoselectaformpattern-32.jpg)</span></span>

<span data-ttu-id="fc8ca-238">[![HowToSelectAFormPattern(33)](./media/howtoselectaformpattern-33.jpg)](./media/howtoselectaformpattern-33.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-238">[![HowToSelectAFormPattern (33)](./media/howtoselectaformpattern-33.jpg)](./media/howtoselectaformpattern-33.jpg)</span></span>



#### <a name="dialog"></a><span data-ttu-id="fc8ca-239">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-239">Dialog</span></span>

<span data-ttu-id="fc8ca-240">[ダイアログ – 基本](dialog-form-pattern.md)\[既定\] このフォームのパターンは一連の情報を収集または表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-240">[Dialog – Basic](dialog-form-pattern.md)\[Default\] This form pattern is used to gather or show a set of information.</span></span>

<span data-ttu-id="fc8ca-241">フォーム: ProjTableCreate</span><span class="sxs-lookup"><span data-stu-id="fc8ca-241">Form: ProjTableCreate</span></span>

<span data-ttu-id="fc8ca-242">[![HowToSelectAFormPattern(34)](./media/howtoselectaformpattern-34.jpg)](./media/howtoselectaformpattern-34.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-242">[![HowToSelectAFormPattern (34)](./media/howtoselectaformpattern-34.jpg)](./media/howtoselectaformpattern-34.jpg)</span></span>

<span data-ttu-id="fc8ca-243">[ダイアログ – 読み取り専用](dialog-form-pattern.md) ダイアログが編集できない情報だけを表示する場合は、このダイアログバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-243">[Dialog – Read Only](dialog-form-pattern.md) Use this Dialog variant when your Dialog just displays information that can't be edited.</span></span> <span data-ttu-id="fc8ca-244">**閉じる**ボタンだけがあります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-244">It has only a **Close** button.</span></span>

<span data-ttu-id="fc8ca-245">フォーム: SalesTablePostings</span><span class="sxs-lookup"><span data-stu-id="fc8ca-245">Form: SalesTablePostings</span></span>

<span data-ttu-id="fc8ca-246">[![HowToSelectAFormPattern(35)](./media/howtoselectaformpattern-35.jpg)](./media/howtoselectaformpattern-35.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-246">[![HowToSelectAFormPattern (35)](./media/howtoselectaformpattern-35.jpg)](./media/howtoselectaformpattern-35.jpg)</span></span>

<span data-ttu-id="fc8ca-247">[ダイアログ – クイック タブ](dialog-form-pattern.md) ダイアログの内容がクイック タブにグループ化されている場合は、このダイアログ バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-247">[Dialog – FastTabs](dialog-form-pattern.md) Use this Dialog variant when your Dialog content is grouped into FastTabs.</span></span>

<span data-ttu-id="fc8ca-248">現在、製品にはありません。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-248">None currently in product.</span></span>

<span data-ttu-id="fc8ca-249">[![HowToSelectAFormPattern(36)](./media/howtoselectaformpattern-36.jpg)](./media/howtoselectaformpattern-36.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-249">[![HowToSelectAFormPattern (36)](./media/howtoselectaformpattern-36.jpg)](./media/howtoselectaformpattern-36.jpg)</span></span>

<span data-ttu-id="fc8ca-250">[ダイアログ – タブ](dialog-form-pattern.md) ダイアログの内容をタブにグループ化する必要がある場合は、このダイアログ バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-250">[Dialog – Tabs](dialog-form-pattern.md) Use this Dialog variant when your Dialog content must be grouped into tabs.</span></span>

<span data-ttu-id="fc8ca-251">フォーム: CaseDetailCreate</span><span class="sxs-lookup"><span data-stu-id="fc8ca-251">Form: CaseDetailCreate</span></span>

![HowToSelectAFormPattern (37)](./media/howtoselectaformpattern-37.jpg)

<span data-ttu-id="fc8ca-253">[ダイアログ – 二重タブ](dialog-form-pattern.md) ダイアログコンテンツに2つのタブが重ねて表示されている場合は、このダイアログバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-253">[Dialog – Double Tabs](dialog-form-pattern.md) Use this Dialog variant when your Dialog content has two tabs that are stacked on top of each other.</span></span>

<span data-ttu-id="fc8ca-254">フォーム: PurchTableReferences</span><span class="sxs-lookup"><span data-stu-id="fc8ca-254">Form: PurchTableReferences</span></span>

![HowToSelectAFormPattern (38)](./media/howtoselectaformpattern-38.jpg)



#### <a name="drop-dialog"></a><span data-ttu-id="fc8ca-256">ドロップ ダイアログ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-256">Drop Dialog</span></span>

<span data-ttu-id="fc8ca-257">[ドロップ ダイアログ](drop-dialog-form-pattern.md)\[既定\] このフォーム パターンは、フィールド数が少ない場合 (5 未満) にアクションを開始するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-257">[Drop Dialog](drop-dialog-form-pattern.md)\[Default\] This form pattern is used to initiate actions when the number of fields is small (less than five).</span></span>

<span data-ttu-id="fc8ca-258">フォーム: CustCollectionsNewActivityAction</span><span class="sxs-lookup"><span data-stu-id="fc8ca-258">Form: CustCollectionsNewActivityAction</span></span>

<span data-ttu-id="fc8ca-259">[![HowToSelectAFormPattern(39)](./media/howtoselectaformpattern-39.jpg)](./media/howtoselectaformpattern-39.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-259">[![HowToSelectAFormPattern (39)](./media/howtoselectaformpattern-39.jpg)](./media/howtoselectaformpattern-39.jpg)</span></span>

<span data-ttu-id="fc8ca-260">[ドロップ ダイアログ – 読み取り専用](drop-dialog-form-pattern.md) ドロップ ダイアログのフィールドが編集できない場合は、このドロップ ダイアログ バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-260">[Drop Dialog – Read Only](drop-dialog-form-pattern.md) Use this Drop Dialog variant when the fields in the Drop Dialog aren't editable.</span></span> <span data-ttu-id="fc8ca-261">**OK**/**閉じる**ボタンはモデル化されません。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-261">No **OK**/**Close** button is modeled.</span></span>

<span data-ttu-id="fc8ca-262">現在、例が製品に存在しません。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-262">No example currently exists in the product.</span></span>

#### <a name="factbox"></a><span data-ttu-id="fc8ca-263">情報ボックス</span><span class="sxs-lookup"><span data-stu-id="fc8ca-263">FactBox</span></span>

<span data-ttu-id="fc8ca-264">[情報ボックス グリッド](factbox-form-patterns.md) この情報ボックス バリアントを使用して、関連情報の子コレクションを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-264">[FacbBox Grid](factbox-form-patterns.md) Use this FactBox variant to show a child collection of related information.</span></span>

<span data-ttu-id="fc8ca-265">フォーム: ContactsInfoPart</span><span class="sxs-lookup"><span data-stu-id="fc8ca-265">Form: ContactsInfoPart</span></span>

![HowToSelectAFormPattern (40)](./media/howtoselectaformpattern-40.jpg)

<span data-ttu-id="fc8ca-267">[情報ボックス カード](factbox-form-patterns.md) この情報ボックス バリアントを使用して、一連の関連フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-267">[FactBox Card](factbox-form-patterns.md) Use this FactBox variant to show a set of related fields.</span></span>

<span data-ttu-id="fc8ca-268">フォーム: CustStatisticsStatistics</span><span class="sxs-lookup"><span data-stu-id="fc8ca-268">Form: CustStatisticsStatistics</span></span>

![HowToSelectAFormPattern (41)](./media/howtoselectaformpattern-41.jpg)

#### <a name="list-page"></a><span data-ttu-id="fc8ca-270">リスト ページ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-270">List Page</span></span>

<span data-ttu-id="fc8ca-271">[リスト ページ](list-page-form-pattern.md) Dynamics AX 2012 のリストページは、レコード閲覧とそのレコードの操作に最適化されたグリッドです。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-271">[List Page](list-page-form-pattern.md) The Dynamics AX 2012 list page that is just a grid that is optimized for browsing records and acting on those records.</span></span>

<span data-ttu-id="fc8ca-272">フォーム: SalesTableListPage</span><span class="sxs-lookup"><span data-stu-id="fc8ca-272">Form: SalesTableListPage</span></span>

![HowToSelectAFormPattern (42)](./media/howtoselectaformpattern-42.jpg)

#### <a name="lookup"></a><span data-ttu-id="fc8ca-274">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="fc8ca-274">Lookup</span></span>

<span data-ttu-id="fc8ca-275">[基本のルックアップ](lookup-form-pattern.md)\[既定\] このフォーム パターンは、ルックアップ フォームが下部にオプションのフィルターまたはボタンを持つグリッドまたはツリーである場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-275">[Lookup Basic](lookup-form-pattern.md)\[Default\] This form pattern is used if the lookup form is a grid or tree that has optional filters or buttons at the bottom.</span></span>

<span data-ttu-id="fc8ca-276">フォーム: SysLanguageLookup</span><span class="sxs-lookup"><span data-stu-id="fc8ca-276">Form: SysLanguageLookup</span></span>

<span data-ttu-id="fc8ca-277">[![HowToSelectAFormPattern(43)](./media/howtoselectaformpattern-43.jpg)](./media/howtoselectaformpattern-43.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-277">[![HowToSelectAFormPattern (43)](./media/howtoselectaformpattern-43.jpg)](./media/howtoselectaformpattern-43.jpg)</span></span>

<span data-ttu-id="fc8ca-278">[プレビュー付きのルックアップ](lookup-form-pattern.md) このルックアップ バリアントを使用して、ときに、基本的なパターンだけでなく、現在のレコードのプレビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-278">[Lookup w/Preview](lookup-form-pattern.md) Use this Lookup variant when, in addition to the basic pattern, a preview of the current record is also shown.</span></span>

<span data-ttu-id="fc8ca-279">フォーム: HcmWorkerLookup</span><span class="sxs-lookup"><span data-stu-id="fc8ca-279">Form: HcmWorkerLookup</span></span>

![HowToSelectAFormPattern (44)](./media/howtoselectaformpattern-44.jpg)

<span data-ttu-id="fc8ca-281">[タブ付きのルックアップ](lookup-form-pattern.md) ルックアップの複数のビュー (グリッドビュー / ツリービュー、複数のフィルタリングされたリストなど) がある場合は、このルックアップ バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-281">[Lookup w/Tabs](lookup-form-pattern.md) Use this Lookup variant when there are multiple views of a lookup (for example, a grid view/tree view or multiple filtered lists).</span></span>

<span data-ttu-id="fc8ca-282">フォーム: CaseCategoryLookup</span><span class="sxs-lookup"><span data-stu-id="fc8ca-282">Form: CaseCategoryLookup</span></span>

![HowToSelectAFormPattern (45)](./media/howtoselectaformpattern-45.jpg)



#### <a name="panorama-section"></a><span data-ttu-id="fc8ca-284">パノラマ セクション</span><span class="sxs-lookup"><span data-stu-id="fc8ca-284">Panorama Section</span></span>

<span data-ttu-id="fc8ca-285">[フォーム パート セクション リスト](section-list-form-pattern.md) このフォーム パターンを使用して、ワークスペース セクションにリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-285">[Form Part Section List](section-list-form-pattern.md) Use this form pattern to show a list in a workspace section.</span></span> <span data-ttu-id="fc8ca-286">これは別のフォームとしてモデル化し、フォーム パーツ コントロールを介してワークスペースにレンダリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-286">This should be modeled as a separate form and rendered in the workspace via a Form Part Control.</span></span>

<span data-ttu-id="fc8ca-287">[フォーム パート セクション リスト - ダブル](section-list-form-pattern.md) セカンダリ リストを表示する必要がある場合は、このバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-287">[Form Part Section List - Double](section-list-form-pattern.md) Use this variant when you must also show a secondary list.</span></span> <span data-ttu-id="fc8ca-288">このセカンダリ リストは最初は表示されません。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-288">This secondary list isn't initially visible.</span></span>

<span data-ttu-id="fc8ca-289">[ハブ パート グラフ](section-chart-form-pattern.md) このバリアントを使用して、ワークスペース セクション にグラフを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-289">[Hub Part Chart](section-chart-form-pattern.md) Use this variant to show a chart in a workspace section.</span></span> <span data-ttu-id="fc8ca-290">これは別のフォームとしてモデル化し、フォーム パーツ コントロールを介してワークスペースにレンダリングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-290">This should be modeled as a separate form and rendered in the workspace via a Form Part Control.</span></span>

<span data-ttu-id="fc8ca-291">フォーム: VendInvoiceJourCountChart</span><span class="sxs-lookup"><span data-stu-id="fc8ca-291">Form: VendInvoiceJourCountChart</span></span>

<span data-ttu-id="fc8ca-292">[![HowToSelectAFormPattern(1)](./media/howtoselectaformpattern-1.jpg)](./media/howtoselectaformpattern-1.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-292">[![HowToSelectAFormPattern (1)](./media/howtoselectaformpattern-1.jpg)](./media/howtoselectaformpattern-1.jpg)</span></span>



#### <a name="simple-details"></a><span data-ttu-id="fc8ca-293">簡易詳細</span><span class="sxs-lookup"><span data-stu-id="fc8ca-293">Simple Details</span></span>

<span data-ttu-id="fc8ca-294">[ツールバーおよびフィールド付き簡易詳細](simple-details-form-pattern.md) このフォーム パターンを使用して、単一の基本レコードのフィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-294">[Simple Details w/Toolbar and Fields](simple-details-form-pattern.md) Use this form pattern to show fields for a single base record.</span></span>

<span data-ttu-id="fc8ca-295">フォーム: AgreementLine</span><span class="sxs-lookup"><span data-stu-id="fc8ca-295">Form: AgreementLine</span></span>

![HowToSelectAFormPattern (2)](./media/howtoselectaformpattern-2.jpg)

<span data-ttu-id="fc8ca-297">[クイック タブ付き簡易詳細](simple-details-form-pattern.md) レコードの情報がクイック タブにまとめられている場合は、この簡易詳細バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-297">[Simple Details w/FastTabs](simple-details-form-pattern.md) Use this Simple Details variant when the record’s information is organized into FastTabs.</span></span>

<span data-ttu-id="fc8ca-298">フォーム: PlanActivityServiceDetails</span><span class="sxs-lookup"><span data-stu-id="fc8ca-298">Form: PlanActivityServiceDetails</span></span>

![HowToSelectAFormPattern (3)](./media/howtoselectaformpattern-3.jpg)

<span data-ttu-id="fc8ca-300">[標準タブ付き簡易詳細](simple-details-form-pattern.md) レコードの情報が通常のタブにまとめられている場合は、この簡易詳細バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-300">[Simple Details w/Standard Tabs](simple-details-form-pattern.md) Use this Simple Details variant when the record’s information is organized into regular tabs.</span></span>

<span data-ttu-id="fc8ca-301">フォーム: HcmEmploymentDateManager</span><span class="sxs-lookup"><span data-stu-id="fc8ca-301">Form: HcmEmploymentDateManager</span></span>

![HowToSelectAFormPattern (4)](./media/howtoselectaformpattern-4.jpg)

<span data-ttu-id="fc8ca-303">[パノラマ付き簡易詳細](simple-details-form-pattern.md) この簡易詳細バリアントを使用して、水平方向にスクロールするパノラマにレコードの情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-303">[Simple Details w/Panorama](simple-details-form-pattern.md) Use this Simple Details variant to display a record’s information in a horizontally scrolling panorama.</span></span>

<span data-ttu-id="fc8ca-304">フォーム: PdsMRCEventTracker</span><span class="sxs-lookup"><span data-stu-id="fc8ca-304">Form: PdsMRCEventTracker</span></span>

![HowToSelectAFormPattern (5)](./media/howtoselectaformpattern-5.jpg)


#### <a name="simple-list"></a><span data-ttu-id="fc8ca-306">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-306">Simple List</span></span>

<span data-ttu-id="fc8ca-307">[簡易リスト](simple-list-form-pattern.md) このフォーム パターンは簡易エンティティのデータを管理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-307">[Simple List](simple-list-form-pattern.md) This form pattern is used to maintain data for simple entities.</span></span>

<span data-ttu-id="fc8ca-308">フォーム: CustGroup</span><span class="sxs-lookup"><span data-stu-id="fc8ca-308">Form: CustGroup</span></span>

![HowToSelectAFormPattern (6)](./media/howtoselectaformpattern-6.jpg)



#### <a name="simple-list-and-details"></a><span data-ttu-id="fc8ca-310">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="fc8ca-310">Simple List and Details</span></span>

<span data-ttu-id="fc8ca-311">[簡易リストと詳細 – リスト グリッド](simple-list-details-form-pattern.md)\[既定\] このフォーム パターンは中程度の複雑さのエンティティのデータを管理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-311">[Simple List & Details – List Grid](simple-list-details-form-pattern.md)\[Default\] This form pattern is used to maintain data for entities of medium complexity.</span></span> <span data-ttu-id="fc8ca-312">ナビゲーション リストの 2 ～ 3 フィールドが含まれるリスト グリッドは、現在のバージョンでは、このフォーム スタイルの優先パターンです。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-312">A list grid that has 2–3 fields in the navigation list is the preferred pattern for this form style in the current version.</span></span>

<span data-ttu-id="fc8ca-313">フォーム: PaymTerm</span><span class="sxs-lookup"><span data-stu-id="fc8ca-313">Form: PaymTerm</span></span>

![HowToSelectAFormPattern (7)](./media/howtoselectaformpattern-7.jpg)

<span data-ttu-id="fc8ca-315">[簡易リストと詳細 – 表形式のグリッド](simple-list-details-form-pattern.md) この簡易リストと詳細のバリアントは、フォームのリスト部分に 3 つ以上のフィールドが必要な場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-315">[Simple List & Details – Tabular Grid](simple-list-details-form-pattern.md) Use this Simple List & Details variant if you require more than three fields in the list part of the form.</span></span>

<span data-ttu-id="fc8ca-316">フォーム: ExchangeRate</span><span class="sxs-lookup"><span data-stu-id="fc8ca-316">Form: ExchangeRate</span></span>

![HowToSelectAFormPattern (8)](./media/howtoselectaformpattern-8.jpg)

<span data-ttu-id="fc8ca-318">[簡易リストと詳細 – ツリー](simple-list-details-form-pattern.md) フォームのリスト部分がツリーの場合は、この簡易リストと詳細のバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-318">[Simple List & Details – Tree](simple-list-details-form-pattern.md) Use this Simple List & Details variant if the list part of the form is a tree.</span></span>

<span data-ttu-id="fc8ca-319">フォーム: FiscalCalendars</span><span class="sxs-lookup"><span data-stu-id="fc8ca-319">Form: FiscalCalendars</span></span>

![HowToSelectAFormPattern (9)](./media/howtoselectaformpattern-9.jpg)



#### <a name="table-of-contents"></a><span data-ttu-id="fc8ca-321">目次</span><span class="sxs-lookup"><span data-stu-id="fc8ca-321">Table of Contents</span></span>

<span data-ttu-id="fc8ca-322">[目次](table-of-contents-form-pattern.md) このフォーム パターンを使用して、設定情報または大まかに関連する情報のセットを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-322">[Table of Contents](table-of-contents-form-pattern.md) Use this form pattern to show setup information or loosely related information sets.</span></span>

<span data-ttu-id="fc8ca-323">フォーム: CustParameters</span><span class="sxs-lookup"><span data-stu-id="fc8ca-323">Form: CustParameters</span></span>

![HowToSelectAFormPattern (10)](./media/howtoselectaformpattern-10.jpg)



#### <a name="task"></a><span data-ttu-id="fc8ca-325">タスク</span><span class="sxs-lookup"><span data-stu-id="fc8ca-325">Task</span></span>

<span data-ttu-id="fc8ca-326">[タスク シングル](task-single-form-pattern.md) このレガシ フォーム パターンは、エンティティを表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-326">[Task Single](task-single-form-pattern.md) This legacy form pattern is used to display entities.</span></span> <span data-ttu-id="fc8ca-327">これは、新しいフォームではなく、移行にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-327">It should be used only for migration, not for new forms.</span></span>

<span data-ttu-id="fc8ca-328">フォーム: LedgerJournalTable</span><span class="sxs-lookup"><span data-stu-id="fc8ca-328">Form: LedgerJournalTable</span></span>

![HowToSelectAFormPattern (11)](./media/howtoselectaformpattern-11.jpg)

<span data-ttu-id="fc8ca-330">[タスク ダブル](task-double-form-pattern.md) このレガシ フォーム パターンは、トランザクション エンティティを表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-330">[Task Double](task-double-form-pattern.md) This legacy form pattern is used to display transaction entities.</span></span> <span data-ttu-id="fc8ca-331">これは、新しいフォームではなく、移行にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-331">It should be used only for migration, not for new forms.</span></span>

<span data-ttu-id="fc8ca-332">フォーム: HRMAbsenceTableHistory</span><span class="sxs-lookup"><span data-stu-id="fc8ca-332">Form: HRMAbsenceTableHistory</span></span>

![HowToSelectAFormPattern (12)](./media/howtoselectaformpattern-12.jpg)



#### <a name="wizard"></a><span data-ttu-id="fc8ca-334">ウィザード</span><span class="sxs-lookup"><span data-stu-id="fc8ca-334">Wizard</span></span>

<span data-ttu-id="fc8ca-335">[ウィザード](wizard-form-pattern.md) このフォーム パターンはあらじめ設定された順序で情報を収集するために、ユーザーに一連のページ ビューを表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-335">[Wizard](wizard-form-pattern.md) This form pattern is used to display a set of page views to the user to gather information in a predetermined order.</span></span>

<span data-ttu-id="fc8ca-336">フォーム: WrkCtrBulkResReqEditWizard</span><span class="sxs-lookup"><span data-stu-id="fc8ca-336">Form: WrkCtrBulkResReqEditWizard</span></span>

![HowToSelectAFormPattern (13)](./media/howtoselectaformpattern-13.jpg)



#### <a name="workspace"></a><span data-ttu-id="fc8ca-338">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="fc8ca-338">Workspace</span></span>

<span data-ttu-id="fc8ca-339">[運用ワークスペース](workspace-form-pattern.md)\[既定\] これは、ワークスペース パターンで推奨されているパフォーマンスが向上したバリアントです。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-339">[Operational Workspace](workspace-form-pattern.md)\[Default\] This is the preferred, performance-enhanced variant of the Workspace pattern.</span></span>

<span data-ttu-id="fc8ca-340">フォーム: FmClerkWorkspace</span><span class="sxs-lookup"><span data-stu-id="fc8ca-340">Form: FmClerkWorkspace</span></span>

![HowToSelectAFormPattern (1)](./media/howtoselectaformpattern-1.png)

<span data-ttu-id="fc8ca-342">ワークスペース: これは古いワークスペース パターンです。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-342">Workspace: This is the old Workspace pattern.</span></span> <span data-ttu-id="fc8ca-343">これはまもなく削除されるため、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-343">It will be removed soon, so don't use it.</span></span> <span data-ttu-id="fc8ca-344">ここでは完全を期すためだけに含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-344">It is included here only for completeness.</span></span>

<span data-ttu-id="fc8ca-345">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-345">Do not use.</span></span>

## <a name="subpattern-reference-guide"></a><span data-ttu-id="fc8ca-346">サブパターン参照ガイド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-346">Subpattern reference guide</span></span>
### <a name="list-of-subpattern-classes"></a><span data-ttu-id="fc8ca-347">サブパターン クラスのリスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-347">List of subpattern classes</span></span>

| <span data-ttu-id="fc8ca-348">フォーム パターン</span><span class="sxs-lookup"><span data-stu-id="fc8ca-348">Form pattern</span></span>                                                                                                     | <span data-ttu-id="fc8ca-349">これは何に使用されますか ?</span><span class="sxs-lookup"><span data-stu-id="fc8ca-349">What it's used for</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ca-350">[カスタム フィルター](custom-filter-group-subpattern.md) (2 つのバリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-350">[Custom Filters](custom-filter-group-subpattern.md) (two variants)</span></span>             | <span data-ttu-id="fc8ca-351">QuickFilters およびその他のモデル化されたカスタム フィルターを表示するコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-351">Containers that display QuickFilters and any other modeled custom filters</span></span>                           |
| <span data-ttu-id="fc8ca-352">フィールド (5 つのバリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-352">Fields (five variants)</span></span>                                                                                           | <span data-ttu-id="fc8ca-353">主に個々のフィールドを表示するコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-353">Containers that primarily display individual fields</span></span>                                                 |
| [<span data-ttu-id="fc8ca-354">分析コード式ビルダー</span><span class="sxs-lookup"><span data-stu-id="fc8ca-354">Dimension Expression Builder</span></span>](../financial/dimension-expression-builder-subpattern.md)     | <span data-ttu-id="fc8ca-355">分析コード式ビルダー コントロールを含むコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-355">Containers that include a Dimension Expression Builder control</span></span>                                      |
| [<span data-ttu-id="fc8ca-356">分析コード エントリ コントロール</span><span class="sxs-lookup"><span data-stu-id="fc8ca-356">Dimension Entry Control</span></span>](../financial/dimension-entry-control-subpattern.md)               | <span data-ttu-id="fc8ca-357">分析コード エントリ コントロールを含むコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-357">Containers that include a Dimension Entry Control</span></span>                                                   |
| [<span data-ttu-id="fc8ca-358">リスト パネル</span><span class="sxs-lookup"><span data-stu-id="fc8ca-358">List Panel</span></span>](list-panel-subpattern.md)                                         | <span data-ttu-id="fc8ca-359">ユーザーがアイテムを移動する 2 つのリストを表示するコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-359">Containers that display two lists that users move items between</span></span>                                     |
| [<span data-ttu-id="fc8ca-360">入れ子になった簡易リストおよび詳細</span><span class="sxs-lookup"><span data-stu-id="fc8ca-360">Nested Simple List and Details</span></span>](nested-simple-list-details-subpattern.md) | <span data-ttu-id="fc8ca-361">簡単な簡易リストと詳細フォームをフォームのセクション内に埋め込むために使用されるコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-361">Containers that are used to embed a simpler Simple List and Details form inside a section in a form</span></span> |
| [<span data-ttu-id="fc8ca-362">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-362">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)                         | <span data-ttu-id="fc8ca-363">フィールド セットの上にアクションを表示するコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-363">Containers that display actions above a set of fields</span></span>                                               |
| <span data-ttu-id="fc8ca-364">[ツールバーおよびリスト](toolbar-list-subpattern.md) (2 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-364">[Toolbar and List](toolbar-list-subpattern.md) (two variants)</span></span>              | <span data-ttu-id="fc8ca-365">1 ～ 2 グリッドを超えるアクションを表示するコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-365">Containers that display actions above 1–2 grids</span></span>                                                     |
| <span data-ttu-id="fc8ca-366">ワークスペース関連 (8 バリアント)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-366">Workspace-related (eight variants)</span></span>                                                                               | <span data-ttu-id="fc8ca-367">操作可能なワークスペース内のさまざまなセクションに対応するコンテナー (複数)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-367">Containers that correspond to various sections inside an Operational Workspace</span></span>                      |

### <a name="finding-containers-that-require-that-a-subpattern-be-applied-on-a-form"></a><span data-ttu-id="fc8ca-368">フォーム上で適用されるサブパターンが必要なコンテナーの検索</span><span class="sxs-lookup"><span data-stu-id="fc8ca-368">Finding containers that require that a subpattern be applied on a form</span></span>

<span data-ttu-id="fc8ca-369">フォームが Visual Studio デザイナーで開かれていると、デザイナーの上部にあるコントロール検索ボックスで「指定されていません」を検索することによって、まだサブパターンを適用する必要のあるコンテナーを簡単に検索できます (次のスクリーン ショットに図示)。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-369">When a form is open in the Visual Studio designer, you can easily search for containers that must still have subpatterns applied by searching for “unspecified” in the control search box at the top of the designer (as shown in the following screen shot).</span></span>

<span data-ttu-id="fc8ca-370">[![HowToSelectAFormPattern(15)](./media/howtoselectaformpattern-15.jpg)](./media/howtoselectaformpattern-15.jpg)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-370">[![HowToSelectAFormPattern (15)](./media/howtoselectaformpattern-15.jpg)](./media/howtoselectaformpattern-15.jpg)</span></span>

### <a name="subpattern-visuals-and-descriptions"></a><span data-ttu-id="fc8ca-371">サブパターンのビジュアルと説明</span><span class="sxs-lookup"><span data-stu-id="fc8ca-371">Subpattern visuals and descriptions</span></span>

<span data-ttu-id="fc8ca-372">サブパターン クラスごとに、各バリアントに関する情報が提供されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-372">For each subpattern class, information is provided about each variant.</span></span> <span data-ttu-id="fc8ca-373">この情報には、簡単な説明と例フォームの図が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-373">This information includes a short description and an illustration of an example form.</span></span>

#### <a name="custom-filters"></a><span data-ttu-id="fc8ca-374">カスタム フィルター</span><span class="sxs-lookup"><span data-stu-id="fc8ca-374">Custom Filters</span></span>

<span data-ttu-id="fc8ca-375">[カスタム フィルター](custom-filter-group-subpattern.md) カスタム フィルターがモデル化されている場合は、このフォーム パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-375">[Custom Filters](custom-filter-group-subpattern.md) Use this form pattern when custom filters are modeled.</span></span> <span data-ttu-id="fc8ca-376">QuickFilter は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-376">QuickFilter isn't required.</span></span>

<span data-ttu-id="fc8ca-377">フォーム: LedgerJournalTable (TopFields)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-377">Form: LedgerJournalTable (TopFields)</span></span>

![HowToSelectAFormPattern (16)](./media/howtoselectaformpattern-16.jpg)

<span data-ttu-id="fc8ca-379">[カスタムと クイック フィルター](../financial/dimension-entry-control-subpattern.md) QuickFilter が必要な場合は、このバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-379">[Custom and Quick Filters](../financial/dimension-entry-control-subpattern.md) Use this variant when a QuickFilter is required.</span></span>

<span data-ttu-id="fc8ca-380">フォーム: CustTable (CustomFilterGroup)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-380">Form: CustTable (CustomFilterGroup)</span></span>

![HowToSelectAFormPattern (17)](./media/howtoselectaformpattern-17.jpg)



#### <a name="fields"></a><span data-ttu-id="fc8ca-382">フィールド</span><span class="sxs-lookup"><span data-stu-id="fc8ca-382">Fields</span></span>

<span data-ttu-id="fc8ca-383">[フィールドおよびフィールド グループ](fields-field-groups-subpattern.md) このフォーム パターンを使用して、フィールドのみを含むコンテナーの応答レイアウトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-383">[Fields and Field Groups](fields-field-groups-subpattern.md) Use this form pattern to get a responsive layout for containers that contain only fields.</span></span>

<span data-ttu-id="fc8ca-384">フォーム: InventLocation (LocationNames)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-384">Form: InventLocation (LocationNames)</span></span>

![HowToSelectAFormPattern (18)](./media/howtoselectaformpattern-18.jpg)

<span data-ttu-id="fc8ca-386">[表形式フィールド](tabular-fields-subpattern.md) このフォーム パターンを使用して、フィールドの構造化されたレイアウトを取得します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-386">[Tabular Fields](tabular-fields-subpattern.md) Use this form pattern to get a structured layout of fields.</span></span> <span data-ttu-id="fc8ca-387">主に合計のためです。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-387">It is intended primarily for totals.</span></span>

<span data-ttu-id="fc8ca-388">フォーム: LedgerJournalTransVendPaym (残高)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-388">Form: LedgerJournalTransVendPaym (Balances)</span></span>

![HowToSelectAFormPattern (19)](./media/howtoselectaformpattern-19.jpg)

<span data-ttu-id="fc8ca-390">[テキスト入力](fill-text-subpattern.md) このフォーム パターンは、単一入力コントロールで全幅が必要な場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-390">[Fill Text](fill-text-subpattern.md) Use this form pattern when a single input control requires full width.</span></span>

<span data-ttu-id="fc8ca-391">フォーム: FmRental (メモ)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-391">Form: FmRental (Notes)</span></span>

![HowToSelectAFormPattern (20)](./media/howtoselectaformpattern-20.jpg)

<span data-ttu-id="fc8ca-393">[水平フィールドおよびボタン グループ](horizontal-fields-buttons-group-subpattern.md) フィールドにインライン アクションがある場合は、このフォーム パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-393">[Horizontal Fields and Button Group](horizontal-fields-buttons-group-subpattern.md) Use this form pattern when a field has an inline action.</span></span>

<span data-ttu-id="fc8ca-394">フォーム: SalesTable (GroupHeaderAddressHeaderOverview)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-394">Form: SalesTable (GroupHeaderAddressHeaderOverview)</span></span>

![HowToSelectAFormPattern (21)](./media/howtoselectaformpattern-21.jpg)

<span data-ttu-id="fc8ca-396">[画像のプレビュー](image-preview-subpattern.md) このフォーム パターンは、イメージ コントロール (およびオプションの関連フィールド) を持つコンテナーに使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-396">[Image Preview](image-preview-subpattern.md) Use this form pattern for containers that have image controls (and optional related fields).</span></span>

<span data-ttu-id="fc8ca-397">フォーム: RetailVisualProfile (ログイン)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-397">Form: RetailVisualProfile (Login)</span></span>

![HowToSelectAFormPattern (22)](./media/howtoselectaformpattern-22.jpg)



#### <a name="toolbar-and-list"></a><span data-ttu-id="fc8ca-399">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="fc8ca-399">Toolbar and List</span></span>

<span data-ttu-id="fc8ca-400">[ツールバーおよびフィールド](toolbar-list-subpattern.md) アクションとグリッドのみを持つコンテナーでこのフォーム パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-400">[Toolbar and List](toolbar-list-subpattern.md) Use this form pattern on containers that have only actions and a grid.</span></span>

<span data-ttu-id="fc8ca-401">フォーム: VendTable (TabCommunication)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-401">Form: VendTable (TabCommunication)</span></span>

![HowToSelectAFormPattern (23)](./media/howtoselectaformpattern-23.jpg)

<span data-ttu-id="fc8ca-403">[ツールバーおよびリスト: 二重](toolbar-list-subpattern.md) コンテナーに2 つのグリッドがある場合、このツールバーおよびリスト バリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-403">[Toolbar and List – Double](toolbar-list-subpattern.md) Use this Toolbar and List variant when the containers have two grids.</span></span>

<span data-ttu-id="fc8ca-404">フォーム: SalesQuickQuote (TabPageExistingItems)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-404">Form: SalesQuickQuote (TabPageExistingItems)</span></span>

![HowToSelectAFormPattern (24)](./media/howtoselectaformpattern-24.jpg)



#### <a name="workspace-related"></a><span data-ttu-id="fc8ca-406">関連するワークスペース</span><span class="sxs-lookup"><span data-stu-id="fc8ca-406">Workspace Related</span></span>

<span data-ttu-id="fc8ca-407">[セクション タイル](section-tiles-subpattern.md) このバリアントを使用して、ワークスペースのセクションに一連のタイル/グラフを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-407">[Section Tiles](section-tiles-subpattern.md) Use this variant to show a set of tiles/charts in a workspace section.</span></span> <span data-ttu-id="fc8ca-408">これは、ワークスペース フォームのタブ ページでモデル化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-408">This should be modeled in a tab page on the workspace form.</span></span> <span data-ttu-id="fc8ca-409">グラフはフォーム パーツ コントロールを使用して定義されます</span><span class="sxs-lookup"><span data-stu-id="fc8ca-409">Charts are defined by using Form Part Controls</span></span>

<span data-ttu-id="fc8ca-410">フォーム: SalesOrderProcessingWorkspace</span><span class="sxs-lookup"><span data-stu-id="fc8ca-410">Form: SalesOrderProcessingWorkspace</span></span>

![HowToSelectAFormPattern (25)](./media/howtoselectaformpattern-25.jpg)

<span data-ttu-id="fc8ca-412">[セクション関連リンク](section-related-links-subpattern.md) このバリアントを使用して、ワークスペースのセクションに一連のハイパーリンクを表示します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-412">[Section Related Links](section-related-links-subpattern.md) Use this variant to show a set of hyperlinks in a workspace section.</span></span> <span data-ttu-id="fc8ca-413">これは、ワークスペース フォームのタブ ページでモデル化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-413">This should be modeled in a tab page on the workspace form.</span></span>

<span data-ttu-id="fc8ca-414">フォーム: SalesOrderProcessingWorkspace</span><span class="sxs-lookup"><span data-stu-id="fc8ca-414">Form: SalesOrderProcessingWorkspace</span></span>

![HowToSelectAFormPattern (26)](./media/howtoselectaformpattern-26.jpg)

<span data-ttu-id="fc8ca-416">[セクション タブ付きリスト](section-tabbed-list-subpattern.md) 複数のリスト バリアントを含める必要がある場合に、このバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-416">[Section Tabbed List](section-tabbed-list-subpattern.md) Use this variant when multiple list variants must be included.</span></span> <span data-ttu-id="fc8ca-417">一度に 1 つだけ表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-417">Only one is shown at a time.</span></span>

<span data-ttu-id="fc8ca-418">[セクション積み上げグラフ](section-stacked-chart-subpattern.md) 運用ワークスペースに 2 つのグラフを含める必要がある場合に、このバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-418">[Section Stacked Chart](section-stacked-chart-subpattern.md) Use this variant when you must include up to two charts in an Operational Workspace.</span></span>

<span data-ttu-id="fc8ca-419">[セクション PowerBI](section-powerbi-subpattern.md) Power BI セクションを含める必要がある場合に、このバリアントを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-419">[Section PowerBI](section-powerbi-subpattern.md) Use this variant when a Power BI section must be included.</span></span>

<span data-ttu-id="fc8ca-420">[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md) このフォームのパターンを使用して、ワークスペースに 1 つのフィルターを追加します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-420">[Workspace Page Filter Group](workspace-filter-group-subpattern.md) Use this form pattern to add a single filter to your workspace.</span></span>

<span data-ttu-id="fc8ca-421">[フィルターおよびツールバー – 積み上げ](filters-toolbar-subpattern.md) このサブパターンをフォーム パート セクション リスト パターンで使用すると、フィルターの下にアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-421">[Filters and Toolbar – Stacked](filters-toolbar-subpattern.md) Use this subpattern in the Form Part Section List pattern, so that actions appear below filters.</span></span>

<span data-ttu-id="fc8ca-422">[フィルターおよびツール バー – インライン](filters-toolbar-subpattern.md) このサブパターンをフォーム パート セクション リスト パターンで使用すると、フィルターとアクションが同じ行に表示されます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-422">[Filters and Toolbar – Inline](filters-toolbar-subpattern.md) Use this subpattern in the Form Part Section List pattern, so that filters and actions appear on the same line.</span></span>



#### <a name="other"></a><span data-ttu-id="fc8ca-423">外</span><span class="sxs-lookup"><span data-stu-id="fc8ca-423">Other</span></span>

<span data-ttu-id="fc8ca-424">[入れ子になった簡易リストおよび詳細](nested-simple-list-details-subpattern.md) このフォーム パターンを使用すると、よりシンプルな簡易リストと詳細フォームをタブまたはグループ内に埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-424">[Nested Simple List & Details](nested-simple-list-details-subpattern.md) Use this form pattern to embed a simpler Simple List & Details form inside a tab or group.</span></span>

<span data-ttu-id="fc8ca-425">フォーム: HcmJob (TaskTabPage)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-425">Form: HcmJob (TaskTabPage)</span></span>

![HowToSelectAFormPattern (27)](./media/howtoselectaformpattern-27.jpg)

<span data-ttu-id="fc8ca-427">[リスト パネル](list-panel-subpattern.md) このフォーム パターンは、ユーザーが 2 つのリストの間でアイテムを前後に移動する必要がある場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-427">[List Panel](list-panel-subpattern.md) Use this form pattern when users must move items back and forth between two lists.</span></span>

<span data-ttu-id="fc8ca-428">フォーム: CLIControls\_ListPanel (FormTabPageControl1)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-428">Form: CLIControls\_ListPanel (FormTabPageControl1)</span></span>

![HowToSelectAFormPattern (28)](./media/howtoselectaformpattern-28.jpg)

<span data-ttu-id="fc8ca-430">[ツールバーおよびフィールド](toolbar-fields-subpattern.md) アクションとフィールドのみを持つコンテナーでこのフォーム パターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-430">[Toolbar and Fields](toolbar-fields-subpattern.md) Use this form pattern on containers that have only actions and fields</span></span>

<span data-ttu-id="fc8ca-431">フォーム: HcmPosition (WorkerAssignmentTabPage)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-431">Form: HcmPosition (WorkerAssignmentTabPage)</span></span>

![HowToSelectAFormPattern (29)](./media/howtoselectaformpattern-29.jpg)

<span data-ttu-id="fc8ca-433">[分析コード エントリ コントロール](../financial/dimension-entry-control-subpattern.md) 分析コード エントリ コントロールのみを持つタブページにこのフォームパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-433">[Dimension Entry Control](../financial/dimension-entry-control-subpattern.md) Use this form pattern on tab pages that have only a Dimension Entry Control.</span></span>

<span data-ttu-id="fc8ca-434">フォーム: CustTable (TabFinancialDimensions)</span><span class="sxs-lookup"><span data-stu-id="fc8ca-434">Form: CustTable (TabFinancialDimensions)</span></span>

![HowToSelectAFormPattern (30)](./media/howtoselectaformpattern-30.jpg)

<span data-ttu-id="fc8ca-436">[分析コード式ビルダー](../financial/dimension-expression-builder-subpattern.md) このフォーム パターンは、分析コード式ビルダー コントロールを含むコンテナーで使用します。</span><span class="sxs-lookup"><span data-stu-id="fc8ca-436">[Dimension Expression Builder](../financial/dimension-expression-builder-subpattern.md) Use this form pattern on containers that include a Dimension Expression Builder control.</span></span>





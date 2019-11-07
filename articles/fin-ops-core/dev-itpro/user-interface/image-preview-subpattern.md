---
title: 画像のプレビューのサブパターン
description: この記事では、イメージ プレビュー フォームのサブパターンについて説明します。 このサブパターンは、フォーム コンテナ内、特にクイック タブまたはグループ内に表示されるほとんどの画像に使用できます。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 12444
ms.assetid: ac176ec7-7f14-47b8-908c-d2175a29fc5c
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5221bf43eb8da1c1d1b484b528d6f507af7febb8
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658837"
---
# <a name="image-preview-subpattern"></a><span data-ttu-id="f4f64-104">画像のプレビューのサブパターン</span><span class="sxs-lookup"><span data-stu-id="f4f64-104">Image Preview subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4f64-105">この記事では、イメージ プレビュー フォームのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f4f64-105">This article provides information about the Image Preview form subpattern.</span></span> <span data-ttu-id="f4f64-106">このサブパターンは、フォーム コンテナ内、特にクイック タブまたはグループ内に表示されるほとんどの画像に使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4f64-106">This subpattern can be used for most images that appear within a form container, especially within a FastTab or Group.</span></span> 

<a name="usage"></a><span data-ttu-id="f4f64-107">用途</span><span class="sxs-lookup"><span data-stu-id="f4f64-107">Usage</span></span>
-----

<span data-ttu-id="f4f64-108">イメージ プレビューは、特にクイック タブまたはグループ内のフォーム コンテナー内に表示される大部分のイメージで使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4f64-108">Image Preview can be used for most images that appear within a form container, especially within a FastTab or Group.</span></span> <span data-ttu-id="f4f64-109">このサブパターンは、FieldsAndFieldGroup サブパターンと FillText サブパターンと一緒に使用して、画像と関連するフィールドを結合することができます。</span><span class="sxs-lookup"><span data-stu-id="f4f64-109">This subpattern can be used in conjunction with the FieldsAndFieldGroup and FillText subpatterns to combine images and any associated fields.</span></span> <span data-ttu-id="f4f64-110">このサブパターンは、タイルまたはボタンに対しては、あるいはフィールド ステータス イメージに対しては使用されません。</span><span class="sxs-lookup"><span data-stu-id="f4f64-110">This subpattern isn't used for tiles or buttons, or for field status images.</span></span>

### <a name="typical-contents"></a><span data-ttu-id="f4f64-111">標準的な内容</span><span class="sxs-lookup"><span data-stu-id="f4f64-111">Typical contents</span></span>

-   <span data-ttu-id="f4f64-112">ツールバー (ActionPane、**スタイル**=**ストライプ**)</span><span class="sxs-lookup"><span data-stu-id="f4f64-112">Toolbar (ActionPane where **Style**=**Strip**)</span></span>
-   <span data-ttu-id="f4f64-113">画像</span><span class="sxs-lookup"><span data-stu-id="f4f64-113">Image</span></span>
-   <span data-ttu-id="f4f64-114">サブパターンを含めることができます:</span><span class="sxs-lookup"><span data-stu-id="f4f64-114">Can contain subpatterns:</span></span>
    -   <span data-ttu-id="f4f64-115">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="f4f64-115">Fields and Field Groups</span></span>
    -   <span data-ttu-id="f4f64-116">テキスト入力</span><span class="sxs-lookup"><span data-stu-id="f4f64-116">Fill text</span></span>

## <a name="wireframe"></a><span data-ttu-id="f4f64-117">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="f4f64-117">Wireframe</span></span>
<span data-ttu-id="f4f64-118">[![画像プレビューのワイヤーフレーム](./media/imagepreview1.png)](./media/imagepreview1.png)</span><span class="sxs-lookup"><span data-stu-id="f4f64-118">[![Wireframe of Image Preview](./media/imagepreview1.png)](./media/imagepreview1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="f4f64-119">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="f4f64-119">Pattern changes</span></span>
<span data-ttu-id="f4f64-120">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4f64-120">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="f4f64-121">フィールドは、任意のフィールドがある場合、画像の右側にあります。</span><span class="sxs-lookup"><span data-stu-id="f4f64-121">Fields are to the right of the image, if there are any fields.</span></span>
-   <span data-ttu-id="f4f64-122">画像の上のアクション ウィンドウは関連付けられたアクション (たとえば、アップロードおよび選択) に使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4f64-122">An ActionPane above the image can be used for associated actions (for example, Upload and Select).</span></span>

## <a name="model"></a><span data-ttu-id="f4f64-123">モデル</span><span class="sxs-lookup"><span data-stu-id="f4f64-123">Model</span></span>
### <a name="image-only--high-level-structure"></a><span data-ttu-id="f4f64-124">イメージのみ – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="f4f64-124">Image only – High-level structure</span></span>

- <span data-ttu-id="f4f64-125">\[コンテナー\] (列 = 固定 – 1)</span><span class="sxs-lookup"><span data-stu-id="f4f64-125">\[Container\] (Columns = Fixed – 1)</span></span>

    - <span data-ttu-id="f4f64-126">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f4f64-126">*Toolbar (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="f4f64-127">画像</span><span class="sxs-lookup"><span data-stu-id="f4f64-127">Image</span></span>

### <a name="image-and-fields--high-level-structure"></a><span data-ttu-id="f4f64-128">イメージやフィールド – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="f4f64-128">Image and fields – High-level structure</span></span>

- <span data-ttu-id="f4f64-129">\[コンテナー\] (列 = 固定 – 1)</span><span class="sxs-lookup"><span data-stu-id="f4f64-129">\[Container\] (Columns = Fixed – 1)</span></span>

    - <span data-ttu-id="f4f64-130">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f4f64-130">*Toolbar (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="f4f64-131">画像</span><span class="sxs-lookup"><span data-stu-id="f4f64-131">Image</span></span>
    - <span data-ttu-id="f4f64-132">グループ化</span><span class="sxs-lookup"><span data-stu-id="f4f64-132">Group</span></span>

        - <span data-ttu-id="f4f64-133">画像</span><span class="sxs-lookup"><span data-stu-id="f4f64-133">Image</span></span>
        - <span data-ttu-id="f4f64-134">グループ - メモ: フィールドのサブパターンを使用</span><span class="sxs-lookup"><span data-stu-id="f4f64-134">Group - Note: uses a fields subpattern</span></span>

### <a name="core-components"></a><span data-ttu-id="f4f64-135">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f4f64-135">Core components</span></span>

-   <span data-ttu-id="f4f64-136">画像のプレビューのサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="f4f64-136">Apply the Image Preview subpattern to the container control.</span></span>
-   <span data-ttu-id="f4f64-137">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="f4f64-137">Address BP Warnings:</span></span>
    -   <span data-ttu-id="f4f64-138">繰り越された AX6.3 BP チェック以外に必要な追加の BP チェックはありません。</span><span class="sxs-lookup"><span data-stu-id="f4f64-138">No additional BP checks are required beyond the AX6.3 BP checks that were carried forward.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="f4f64-139">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="f4f64-139">Related container patterns</span></span>

-   [<span data-ttu-id="f4f64-140">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="f4f64-140">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="f4f64-141">テキスト入力</span><span class="sxs-lookup"><span data-stu-id="f4f64-141">Fill Text</span></span>](fill-text-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="f4f64-142">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="f4f64-142">UX guidelines</span></span>
<span data-ttu-id="f4f64-143">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="f4f64-143">The verification checklist shows the steps for manually verifying that the form complies with the UX guidelines.</span></span> <span data-ttu-id="f4f64-144">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f4f64-144">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="f4f64-145">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="f4f64-145">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="f4f64-146">**画像のプレビューのガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="f4f64-146">**Image Preview guidelines:**</span></span>
    -   <span data-ttu-id="f4f64-147">すべてのフィールドは画像の右側に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4f64-147">Any fields should be placed to the right of the image.</span></span>

## <a name="examples"></a><span data-ttu-id="f4f64-148">例</span><span class="sxs-lookup"><span data-stu-id="f4f64-148">Examples</span></span>
<span data-ttu-id="f4f64-149">フォーム: **RetailVisualProfile** **(ログイン)**</span><span class="sxs-lookup"><span data-stu-id="f4f64-149">Form: **RetailVisualProfile** **(Login)**</span></span> 

<span data-ttu-id="f4f64-150">[![画像プレビューの例](./media/imagepreview2.png)](./media/imagepreview2.png)</span><span class="sxs-lookup"><span data-stu-id="f4f64-150">[![Example of Image Preview](./media/imagepreview2.png)](./media/imagepreview2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="f4f64-151">リソース</span><span class="sxs-lookup"><span data-stu-id="f4f64-151">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="f4f64-152">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="f4f64-152">Typically used by patterns</span></span>

-   [<span data-ttu-id="f4f64-153">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="f4f64-153">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="f4f64-154">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="f4f64-154">Details Transaction</span></span>](details-transaction-form-pattern.md)
-   [<span data-ttu-id="f4f64-155">簡易詳細</span><span class="sxs-lookup"><span data-stu-id="f4f64-155">Simple Details</span></span>](simple-details-form-pattern.md)
-   [<span data-ttu-id="f4f64-156">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="f4f64-156">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="f4f64-157">目次</span><span class="sxs-lookup"><span data-stu-id="f4f64-157">Table of Contents</span></span>](table-of-contents-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="f4f64-158">付録</span><span class="sxs-lookup"><span data-stu-id="f4f64-158">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="f4f64-159">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f4f64-159">Frequently asked questions</span></span>

<span data-ttu-id="f4f64-160">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="f4f64-160">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="f4f64-161">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="f4f64-161">Open issues</span></span>

<span data-ttu-id="f4f64-162">なし。</span><span class="sxs-lookup"><span data-stu-id="f4f64-162">None.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="f4f64-163">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="f4f64-163">AX 2012 content</span></span>

<span data-ttu-id="f4f64-164">[![画像プレビューの例](./media/imagepreview3.png)](./media/imagepreview3.png)</span><span class="sxs-lookup"><span data-stu-id="f4f64-164">[![Example of Image Preview](./media/imagepreview3.png)](./media/imagepreview3.png)</span></span>

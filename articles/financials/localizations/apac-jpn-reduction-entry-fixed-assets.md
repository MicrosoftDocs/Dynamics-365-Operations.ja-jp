---
title: "固定資産の圧縮記帳の設定"
description: "この記事は、固定資産の圧縮記帳に関する情報および、固定資産の圧縮記帳を Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition で設定する方法について説明します。 圧縮記帳は、政府助成金を使用して取得される固定資産の特別な会計処理です。 耐用年数中に、これらの資産の法人所得税を繰延する場合に使用できます。"
author: rake-gui
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetReductionEntryMassUpdate_JP, AssetReductionEntryProfile_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2871
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8afa215915606fe3924a640ee629ae5a6f8f7286
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="set-up-reduction-entries-for-fixed-assets"></a><span data-ttu-id="6b415-105">固定資産の圧縮記帳の設定</span><span class="sxs-lookup"><span data-stu-id="6b415-105">Set up reduction entries for fixed assets</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6b415-106">この記事は、固定資産の圧縮記帳に関する情報および、固定資産の圧縮記帳を Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition で設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b415-106">This article provides information about reduction entries for fixed assets and how to set them up in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="6b415-107">圧縮記帳は、政府助成金を使用して取得される固定資産の特別な会計処理です。</span><span class="sxs-lookup"><span data-stu-id="6b415-107">Reduction entries are a special accounting treatment for fixed assets that you acquire by using a government subsidy.</span></span> <span data-ttu-id="6b415-108">耐用年数中に、これらの資産の法人所得税を繰延する場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6b415-108">You can use them to defer the corporate income tax for those assets throughout their service life.</span></span> 

<span data-ttu-id="6b415-109">政府助成金を使用して固定資産を取得すると、助成は非課税の収益として処理されます。</span><span class="sxs-lookup"><span data-stu-id="6b415-109">When you acquire a fixed asset by using a government subsidy, the subsidy is treated as taxable revenue.</span></span> <span data-ttu-id="6b415-110">ただし、すべての政府補助金を収益として説明すると、結果として法人所得税が大きくなり、補助金の助成効果が減少します。</span><span class="sxs-lookup"><span data-stu-id="6b415-110">However, if you account for the whole government grant as revenue, the result is a large amount of corporate income tax, which reduces the subsidizing effect of the grant.</span></span> <span data-ttu-id="6b415-111">したがって、圧縮記帳と呼ばれる特殊な会計処理が許可されています。</span><span class="sxs-lookup"><span data-stu-id="6b415-111">Therefore, a special accounting treatment called a reduction entry is permitted.</span></span> <span data-ttu-id="6b415-112">基本的に、圧縮記帳は、取得した固定資産の耐用年数中の法人所得税を延期します。</span><span class="sxs-lookup"><span data-stu-id="6b415-112">Basically, reduction entries defer the corporate income tax throughout the service life of the fixed asset that is acquired.</span></span> <span data-ttu-id="6b415-113">2 種類の会計処理が許可されています。</span><span class="sxs-lookup"><span data-stu-id="6b415-113">Two types of accounting treatment are allowed:</span></span>

-   <span data-ttu-id="6b415-114">**直接オフ メソッド** – 政府助成金の金額は、固定資産の取得原価から直接控除されます。</span><span class="sxs-lookup"><span data-stu-id="6b415-114">**Direct-off method** – The amount of the government subsidy is deducted directly from the acquisition cost of the fixed asset.</span></span>
-   <span data-ttu-id="6b415-115">**積立メソッド** – 政府助成金の金額は、貸借対照表の株主資本側面の個別の値として管理されます。</span><span class="sxs-lookup"><span data-stu-id="6b415-115">**Reserve method** – The amount of the government subsidy is maintained as a separate value on the equity side of the balance sheet.</span></span> <span data-ttu-id="6b415-116">政府助成金の金額は、固定資産の正味簿価額に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="6b415-116">The government subsidy amount doesn't affect the net book value of the fixed asset.</span></span>

<span data-ttu-id="6b415-117">圧縮記帳の固定資産転記プロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b415-117">You can set up a fixed asset posting profile for reduction entries.</span></span> <span data-ttu-id="6b415-118">または**処分**タイプのトランザクションの勘定を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b415-118">You can also set up accounts for the transactions of the **Disposal** type.</span></span> <span data-ttu-id="6b415-119">圧縮記帳の固定資産を転記する時、トランザクション金額はこれらの勘定から取得されます。</span><span class="sxs-lookup"><span data-stu-id="6b415-119">The transaction amounts are retrieved from these accounts when you post a fixed asset with a reduction entry.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6b415-120">必要条件</span><span class="sxs-lookup"><span data-stu-id="6b415-120">Prerequisites</span></span>
<span data-ttu-id="6b415-121">次の表に、開始する前に準備が整っている必要のある前提条件を示します。</span><span class="sxs-lookup"><span data-stu-id="6b415-121">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b415-122">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="6b415-122">Category</span></span></th>
<th><span data-ttu-id="6b415-123">前提条件</span><span class="sxs-lookup"><span data-stu-id="6b415-123">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b415-124">国/地域</span><span class="sxs-lookup"><span data-stu-id="6b415-124">Country/region</span></span></td>
<td><span data-ttu-id="6b415-125">法人の基本住所が日本である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b415-125">The primary address for the legal entity must be in Japan.</span></span> <span data-ttu-id="6b415-126">または、法人のローカライズされた機能の地域が日本である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b415-126">Alternatively, the localized functionality region for the legal entity must be in Japan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b415-127">関連する設定作業</span><span class="sxs-lookup"><span data-stu-id="6b415-127">Related setup tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="6b415-128">既定の帳簿、理由コード、および番号順序などの、基本的な固定資産パラメーターを<strong>固定資産パラメーター</strong> ページで確実に設定します。</span><span class="sxs-lookup"><span data-stu-id="6b415-128">Make sure that you've set up basic fixed asset parameters, such as a default book, reason codes, and number sequences, on the <strong>Fixed assets parameters</strong> page.</span></span></li>
<li><span data-ttu-id="6b415-129">固定資産グループを<strong>固定資産グループ</strong>ページで定義します。</span><span class="sxs-lookup"><span data-stu-id="6b415-129">Define a fixed asset group on the <strong>Fixed asset groups</strong> page.</span></span></li>
<li><span data-ttu-id="6b415-130">減価償却量を転記するための、通貨および丸めルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="6b415-130">Set up currencies and rounding rules to post depreciation amounts.</span></span></li>
<li><span data-ttu-id="6b415-131"><strong>固定資産の場所</strong>ページで固定資産の場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="6b415-131">Set up fixed asset locations on the <strong>Fixed assets locations</strong> page.</span></span></li>
<li><span data-ttu-id="6b415-132">減価償却の会計カレンダーを設定し、元帳にカレンダーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6b415-132">Set up a fiscal calendar for depreciation, and assign the calendar to a ledger.</span></span></li>
<li><span data-ttu-id="6b415-133">固定資産レコードが作成済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b415-133">Make sure that you've created a fixed asset record.</span></span></li>
<li><span data-ttu-id="6b415-134"><strong>帳簿</strong>ページで固定資産に帳簿が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b415-134">Make sure that you've set up a book for the fixed asset on the <strong>Book </strong>page.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6b415-135">Finance and Operations では、既存の固定資産の機能の最上部で、圧縮記帳の機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b415-135">Finance and Operations implements the reduction entry feature on top of existing fixed asset features.</span></span> <span data-ttu-id="6b415-136">圧縮記帳を使用するには、既存の固定資産の機能の使用に加えて次の作業を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b415-136">To use reduction entries, you must complete the following tasks in addition to using the existing fixed asset features.</span></span>

### <a name="assigning-a-reduction-entry-document-to-a-fixed-asset-book"></a><span data-ttu-id="6b415-137">固定資産帳簿への圧縮記帳ドキュメントの割り当て</span><span class="sxs-lookup"><span data-stu-id="6b415-137">Assigning a reduction entry document to a fixed asset book</span></span>

<span data-ttu-id="6b415-138">**固定資産**ページを使用して固定資産に圧縮記帳ドキュメントを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6b415-138">Use the **Fixed assets** page to assign a reduction entry document to a fixed asset.</span></span>

### <a name="assigning-a-reduction-entry-document-to-multiple-fixed-asset-books"></a><span data-ttu-id="6b415-139">圧縮記帳ドキュメントの複数の固定資産帳簿への割り当て</span><span class="sxs-lookup"><span data-stu-id="6b415-139">Assigning a reduction entry document to multiple fixed asset books</span></span>

<span data-ttu-id="6b415-140">**圧縮記帳の一括更新**ページを使用して、圧縮記帳ドキュメントを複数の固定資産に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="6b415-140">Use the **Mass update for reduction entry document** page to assign a reduction entry document to multiple fixed assets.</span></span>

### <a name="setting-up-a-fixed-asset-posting-profile-for-reduction-entries"></a><span data-ttu-id="6b415-141">圧縮記帳への固定資産転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="6b415-141">Setting up a fixed asset posting profile for reduction entries</span></span>

<span data-ttu-id="6b415-142">**固定資産転記プロファイル** ページを使用して、圧縮記帳の転記プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="6b415-142">Use the **Fixed asset posting profiles** page to set up a posting profile for reduction entries.</span></span> <span data-ttu-id="6b415-143">また、圧縮記帳に適用された資産を減価償却する、転記プロファイルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b415-143">You can also set up a posting profile to depreciate the asset that is applied with a reduction entry.</span></span>

## <a name="depreciate-fixed-assets-with-reduction-entry-posted"></a><span data-ttu-id="6b415-144">圧縮記帳が転記されている固定資産の減価償却</span><span class="sxs-lookup"><span data-stu-id="6b415-144">Depreciate fixed assets with reduction entry posted</span></span>

<span data-ttu-id="6b415-145">[圧縮記帳が転記されている固定資産の減価償却](./tasks/depreciation-fixed-assets-reduction-entry-posted.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b415-145">See [Depreciate fixed assets with reduction entry posted](./tasks/depreciation-fixed-assets-reduction-entry-posted.md).</span></span>

## <a name="create-and-assign-a-reduction-entry-document-for-a-government-grant-subsidy"></a><span data-ttu-id="6b415-146">政府助成金の圧縮記帳ドキュメントの作成および割り当て</span><span class="sxs-lookup"><span data-stu-id="6b415-146">Create and assign a reduction entry document for a government grant subsidy</span></span>

<span data-ttu-id="6b415-147">[政府助成金の圧縮記帳ドキュメントの作成および割り当て](./tasks/create-assign-reduction-document.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b415-147">See [Create and assign a reduction entry document for a government grant subsidy](./tasks/create-assign-reduction-document.md).</span></span>

## <a name="dispose-of-a-fixed-asset-with-reduction-entry"></a><span data-ttu-id="6b415-148">圧縮記帳のある固定資産の処分</span><span class="sxs-lookup"><span data-stu-id="6b415-148">Dispose of a fixed asset with reduction entry</span></span>

<span data-ttu-id="6b415-149">[圧縮記帳のある固定資産の処分](./tasks/dispose-fixed-asset-reduction-entry.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="6b415-149">See [Dispose of a fixed asset with reduction entry](./tasks/dispose-fixed-asset-reduction-entry.md)</span></span>


## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="6b415-150">システム管理者向け技術情報</span><span class="sxs-lookup"><span data-stu-id="6b415-150">Technical information for system administrators</span></span>
<span data-ttu-id="6b415-151">このタスクを完了するために使用するページに対するアクセス権限がない場合は、システム管理者に連絡し、次の表に示される情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6b415-151">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

| <span data-ttu-id="6b415-152">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="6b415-152">Category</span></span>           | <span data-ttu-id="6b415-153">前提条件</span><span class="sxs-lookup"><span data-stu-id="6b415-153">Prerequisite</span></span>                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b415-154">コンフィギュレーション キー</span><span class="sxs-lookup"><span data-stu-id="6b415-154">Configuration keys</span></span> | <span data-ttu-id="6b415-155">**資産コンフィギュレーション** キーが、[**データ ディクショナリ**] &gt; [**コンフィギュレーション キー**] ノードで使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6b415-155">Make sure that the **Asset configuration** key is available under the **Data Dictionary** &gt; **Configuration Keys** node.</span></span> |




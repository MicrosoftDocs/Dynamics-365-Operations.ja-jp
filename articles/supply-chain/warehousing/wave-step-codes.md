---
title: ウェーブ ステップ コード
description: このトピックでは、ウェーブ ステップ コードの概要とその使用方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992360"
---
# <a name="wave-step-codes"></a><span data-ttu-id="28618-103">ウェーブ ステップ コード</span><span class="sxs-lookup"><span data-stu-id="28618-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="28618-104">ウェーブ ステップ コードについて</span><span class="sxs-lookup"><span data-stu-id="28618-104">About wave step codes</span></span>

<span data-ttu-id="28618-105">ウェーブ ステップ コードとは、ユーザーが設定し、ウェーブ メソッドの特定のインスタンスを対応するテンプレートにリンクするために使用できるコードです。</span><span class="sxs-lookup"><span data-stu-id="28618-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="28618-106">テンプレートには、補充、コンテナー詰め、ラベル印刷、積荷構築、および並べ替えのためのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="28618-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="28618-107">ウェーブ ステップ コードが使用されていない場合、ユーザーはウェーブ メソッド インスタンスから特定のテンプレートを参照する自由書式のテキストを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28618-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="28618-108">ユーザーは、ウェーブ テンプレートの特定のウェーブ ステップ メソッドに追加するウェーブ ステップのテキストが、ターゲット テンプレートのウェーブ ステップ テキストと完全に一致するよう確認する必要があるため、自由書式のテキストのエラーが容易に発生します。</span><span class="sxs-lookup"><span data-stu-id="28618-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="28618-109">特定のウェーブ ステップ タイプに対するウェーブ ステップ コードが、別のページで設定されます。</span><span class="sxs-lookup"><span data-stu-id="28618-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="28618-110">ウェーブ ステップ コードを必要とするウェーブ テンプレート内の各ウェーブ ステップ メソッド インスタンスに関しては、ドロップダウン リストでウェーブ ステップ コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="28618-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="28618-111">ドロップダウン リストでの選択により、自由書式のテキスト入力が置き換えられ、人為的エラーのリスクと影響を軽減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="28618-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="28618-112">設定コードは、ウェーブ テンプレートのウェーブ ステップ メソッドをメソッドのターゲット テンプレートにリンクするために使用します。</span><span class="sxs-lookup"><span data-stu-id="28618-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="28618-113">ウェーブ ステップ コードの使用はオプションであり、取得は法人ごとに行われます。</span><span class="sxs-lookup"><span data-stu-id="28618-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="28618-114">したがって、特定の法人がその機能を使用すると、その法人の既存のすべてのウェーブ ステップ コードが新しい構造にアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="28618-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="28618-115">設定デモ</span><span class="sxs-lookup"><span data-stu-id="28618-115">Setup demo</span></span> 

<span data-ttu-id="28618-116">このデモでは、**USMF** デモ データの会社を使用して、デモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="28618-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="28618-117">ウェーブ ステップ コードを有効にする</span><span class="sxs-lookup"><span data-stu-id="28618-117">Enable wave step codes</span></span>

<span data-ttu-id="28618-118">ウェーブ ステップ コード機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="28618-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="28618-119">**倉庫管理 \> 設定 \> 倉庫管理パラメーター**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="28618-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="28618-120">**一般**タブの、**ウェーブ処理**クイック タブで、**ウェーブ ステップ コードの有効化**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="28618-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="28618-121">既存のすべてのウェーブ ステップ自由書式のテキストが新しい構造にアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="28618-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="28618-122">法人に対するこのアップグレードが完了した後、**ウェーブ ステップ コードの有効化**オプションは**倉庫管理パラメーター** ページで使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="28618-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="28618-123">アップグレード中に検証が実行され、アップグレードに失敗した場合は、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="28618-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="28618-124">次の競合が原因で、アップグレードが失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="28618-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="28618-125">ウェーブ ステップ自由書式のテキストが重複して存在します。</span><span class="sxs-lookup"><span data-stu-id="28618-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="28618-126">カスタマイズが存在します。</span><span class="sxs-lookup"><span data-stu-id="28618-126">Customizations exist.</span></span>
- <span data-ttu-id="28618-127">ウェーブ ステップ メソッド インスタンスに関連付けられているウェーブ ステップ自由書式のテキストが、予測されたテンプレート タイプと一致しません。</span><span class="sxs-lookup"><span data-stu-id="28618-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="28618-128">検証中に特定される競合を解決した後に、アップグレード プロセスを再実行できます。</span><span class="sxs-lookup"><span data-stu-id="28618-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="28618-129">アップグレードが成功すると、**ウェーブ ステップ コード** ページ (**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ ステップ コード**) が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="28618-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="28618-130">このページには、ウェーブ ステップ コード機能が有効になった際にアップグレードされたウェーブ ステップコードが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="28618-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="28618-131">新しいウェーブ ステップ コードの作成</span><span class="sxs-lookup"><span data-stu-id="28618-131">Create new wave step codes</span></span>

<span data-ttu-id="28618-132">**ウェーブ ステップ コード** ページを使用して、ウェーブ ステップ コードを作成および削除できます。</span><span class="sxs-lookup"><span data-stu-id="28618-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="28618-133">それぞれの新しいウェーブ ステップ コードとそれに関連付けられた ID は、すべてのウェーブ ステップ タイプ間で一意である必要があり、特定のウェーブ ステップ タイプに対して定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="28618-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="28618-134">ウェーブ ステップ コードの適用</span><span class="sxs-lookup"><span data-stu-id="28618-134">Apply wave step codes</span></span>

<span data-ttu-id="28618-135">該当するウェーブ ステップ コードを定義した後、それらをウェーブ プロセス メソッドに適用できます。</span><span class="sxs-lookup"><span data-stu-id="28618-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="28618-136">ウェーブ ステップ コードを適用するには、該当するターゲット テンプレートに移動します。</span><span class="sxs-lookup"><span data-stu-id="28618-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="28618-137">次に示すのは、ウェーブ ステップ コードが指すよう指定されたターゲット テンプレートです。</span><span class="sxs-lookup"><span data-stu-id="28618-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="28618-138">**補充テンプレート:** 倉庫管理 \> 設定 \> 補充 \> 補充テンプレート</span><span class="sxs-lookup"><span data-stu-id="28618-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="28618-139">**積荷構築テンプレート:** 倉庫管理 \> 設定 \> 積荷 \> 積荷構築テンプレート</span><span class="sxs-lookup"><span data-stu-id="28618-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="28618-140">**並べ替えテンプレート:** 倉庫管理 \> 設定 \> 梱包 \> 並べ替えテンプレートの出荷</span><span class="sxs-lookup"><span data-stu-id="28618-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="28618-141">**コンテナー詰めテンプレート:** 倉庫管理 \> 設定 \> コンテナー \> コンテナー構築テンプレート</span><span class="sxs-lookup"><span data-stu-id="28618-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="28618-142">**ラベル印刷テンプレート:** 倉庫管理 \> 設定 \> ドキュメント回覧 \> ウェーブ ラベル テンプレート</span><span class="sxs-lookup"><span data-stu-id="28618-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="28618-143">このリストのテンプレートは、ウェーブ テンプレートで選択されているウェーブ プロセス メソッドから参照される場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="28618-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="28618-144">ウェーブ テンプレートにあるウェーブ プロセス メソッドのウェーブ ステップ コードがテンプレート タイプのいずれかのウェーブ ステップ コードと一致する場合、そのテンプレートが適用されます。</span><span class="sxs-lookup"><span data-stu-id="28618-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="28618-145">サンプル シナリオ</span><span class="sxs-lookup"><span data-stu-id="28618-145">Sample scenario</span></span>

<span data-ttu-id="28618-146">次の手順を実行すると、作成した補充テンプレートがウェーブ テンプレートに適用されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="28618-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="28618-147">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ ステップ コード**の順に移動し、**補充**タイプに対するウェーブ ステップ コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="28618-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="28618-148">**倉庫管理 \> 設定 \> 補充 \> 補充テンプレート**の順に移動し、補充テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="28618-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="28618-149">補充テンプレートで、**補充**タイプに対して作成したウェーブ ステップ コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="28618-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="28618-150">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート**の順に移動し、使用するウェーブ テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="28618-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="28618-151">テンプレートの、**メソッド** クイック タブで、**補充**メソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="28618-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="28618-152">**ウェーブ ステップ コード**で、補充テンプレートで選択したウェーブ ステップ コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="28618-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

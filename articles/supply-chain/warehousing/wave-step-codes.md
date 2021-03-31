---
title: ウェーブ ステップ コード
description: このトピックでは、ウェーブ ステップ コードの概要とその使用方法について説明します。
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c28134b9be92802196b4861cbd20801419ef8d23
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212678"
---
# <a name="wave-step-codes"></a><span data-ttu-id="03b75-103">ウェーブ ステップ コード</span><span class="sxs-lookup"><span data-stu-id="03b75-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03b75-104">ウェーブ ステップ コードとは、ユーザーが設定し、ウェーブ メソッドの特定のインスタンスを対応するテンプレートにリンクするために使用できるコードです。</span><span class="sxs-lookup"><span data-stu-id="03b75-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="03b75-105">テンプレートには、補充、コンテナー詰め、ラベル印刷、積荷構築、および並べ替えのためのテンプレートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="03b75-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="03b75-106">ウェーブ ステップ コードが使用されていない場合、ユーザーはウェーブ メソッド インスタンスから特定のテンプレートを参照する自由書式のテキストを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b75-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="03b75-107">ユーザーは、ウェーブ テンプレートの特定のウェーブ ステップ メソッドに追加するウェーブ ステップのテキストが、ターゲット テンプレートのウェーブ ステップ テキストと完全に一致するよう確認する必要があるため、自由書式のテキストのエラーが容易に発生します。</span><span class="sxs-lookup"><span data-stu-id="03b75-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="03b75-108">特定のウェーブ ステップ タイプに対するウェーブ ステップ コードが、別のページで設定されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="03b75-109">ウェーブ ステップ コードを必要とするウェーブ テンプレート内の各ウェーブ ステップ メソッド インスタンスに関しては、ドロップダウン リストでウェーブ ステップ コードを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b75-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="03b75-110">ドロップダウン リストでの選択により、自由書式のテキスト入力が置き換えられ、人為的エラーのリスクと影響を軽減するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="03b75-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="03b75-111">設定コードは、ウェーブ テンプレートのウェーブ ステップ メソッドをメソッドのターゲット テンプレートにリンクするために使用します。</span><span class="sxs-lookup"><span data-stu-id="03b75-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="03b75-112">ウェーブ ステップ コード機能の使用はオプションです。</span><span class="sxs-lookup"><span data-stu-id="03b75-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="03b75-113">すべての法人に対し、組織全体で有効になっています。</span><span class="sxs-lookup"><span data-stu-id="03b75-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="03b75-114">設定デモ</span><span class="sxs-lookup"><span data-stu-id="03b75-114">Setup demo</span></span> 

<span data-ttu-id="03b75-115">このデモでは、**USMF** デモ データの会社を使用して、デモ データをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b75-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="03b75-116">ウェーブ ステップ コードを有効にする</span><span class="sxs-lookup"><span data-stu-id="03b75-116">Enable wave step codes</span></span>

<span data-ttu-id="03b75-117">ウェーブ ステップ コード機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="03b75-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="03b75-118">**機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="03b75-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="03b75-119">**組織全体のウェーブ ステップ コード** と呼ばれる機能を有効にする場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="03b75-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="03b75-120">すべての法人に存在するすべてのウェーブ ステップ自由書式のテキストが新しい構造にアップグレードされます。</span><span class="sxs-lookup"><span data-stu-id="03b75-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="03b75-121">このアップグレードがすべての法人に対して完了した後、機能は有効になります。</span><span class="sxs-lookup"><span data-stu-id="03b75-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="03b75-122">1 つ以上の法人に対して機能が有効にできなかった場合、その機能はすべての法人に対して有効になりません。</span><span class="sxs-lookup"><span data-stu-id="03b75-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="03b75-123">有効化の間、データ アップグレード時に検証が実行されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="03b75-124">アップグレードに失敗した場合、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="03b75-125">次の競合が原因で、アップグレードが失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="03b75-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="03b75-126">ウェーブ ステップ自由書式のテキストが重複して存在します。</span><span class="sxs-lookup"><span data-stu-id="03b75-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="03b75-127">カスタマイズが存在します。</span><span class="sxs-lookup"><span data-stu-id="03b75-127">Customizations exist.</span></span>
- <span data-ttu-id="03b75-128">ウェーブ ステップ メソッド インスタンスに関連付けられているウェーブ ステップ自由書式のテキストが、予測されたテンプレート タイプと一致しません。</span><span class="sxs-lookup"><span data-stu-id="03b75-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="03b75-129">検証中に特定される競合を解決した後に、機能の有効化を再試行できます。</span><span class="sxs-lookup"><span data-stu-id="03b75-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="03b75-130">機能が有効になると、**ウェーブ ステップ コード** ページ (**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ ステップ コード**) が使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="03b75-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="03b75-131">このページには、組織全体のウェーブ ステップ コード機能が有効になった際にアップグレードされたウェーブ ステップコードが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="03b75-132">新しいウェーブ ステップ コードの作成</span><span class="sxs-lookup"><span data-stu-id="03b75-132">Create new wave step codes</span></span>

<span data-ttu-id="03b75-133">**ウェーブ ステップ コード** ページを使用して、ウェーブ ステップ コードを作成および削除できます。</span><span class="sxs-lookup"><span data-stu-id="03b75-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="03b75-134">それぞれの新しいウェーブ ステップ コードとそれに関連付けられた ID は、すべてのウェーブ ステップ タイプ間で一意である必要があり、特定のウェーブ ステップ タイプに対して定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="03b75-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="03b75-135">ウェーブ ステップ コードの適用</span><span class="sxs-lookup"><span data-stu-id="03b75-135">Apply wave step codes</span></span>

<span data-ttu-id="03b75-136">該当するウェーブ ステップ コードを定義した後、それらをウェーブ プロセス メソッドに適用できます。</span><span class="sxs-lookup"><span data-stu-id="03b75-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="03b75-137">ウェーブ ステップ コードを適用するには、該当するターゲット テンプレートに移動します。</span><span class="sxs-lookup"><span data-stu-id="03b75-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="03b75-138">次に示すのは、ウェーブ ステップ コードが指すよう指定されたターゲット テンプレートです。</span><span class="sxs-lookup"><span data-stu-id="03b75-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="03b75-139">**補充テンプレート:** 倉庫管理 \> 設定 \> 補充 \> 補充テンプレート</span><span class="sxs-lookup"><span data-stu-id="03b75-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="03b75-140">**積荷構築テンプレート:** 倉庫管理 \> 設定 \> 積荷 \> 積荷構築テンプレート</span><span class="sxs-lookup"><span data-stu-id="03b75-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="03b75-141">**並べ替えテンプレート:** 倉庫管理 \> 設定 \> 梱包 \> 並べ替えテンプレートの出荷</span><span class="sxs-lookup"><span data-stu-id="03b75-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="03b75-142">**コンテナー詰めテンプレート:** 倉庫管理 \> 設定 \> コンテナー \> コンテナー構築テンプレート</span><span class="sxs-lookup"><span data-stu-id="03b75-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="03b75-143">**ラベル印刷テンプレート:** 倉庫管理 \> 設定 \> ドキュメント回覧 \> ウェーブ ラベル テンプレート</span><span class="sxs-lookup"><span data-stu-id="03b75-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="03b75-144">このリストのテンプレートは、ウェーブ テンプレートで選択されているウェーブ プロセス メソッドから参照される場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="03b75-145">ウェーブ テンプレートにあるウェーブ プロセス メソッドのウェーブ ステップ コードがテンプレート タイプのいずれかのウェーブ ステップ コードと一致する場合、そのテンプレートが適用されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="03b75-146">サンプル シナリオ</span><span class="sxs-lookup"><span data-stu-id="03b75-146">Sample scenario</span></span>

<span data-ttu-id="03b75-147">次の手順を実行すると、作成した補充テンプレートがウェーブ テンプレートに適用されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="03b75-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="03b75-148">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ ステップ コード** の順に移動し、**補充** タイプに対するウェーブ ステップ コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="03b75-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="03b75-149">**倉庫管理 \> 設定 \> 補充 \> 補充テンプレート** の順に移動し、補充テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="03b75-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="03b75-150">補充テンプレートで、**補充** タイプに対して作成したウェーブ ステップ コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="03b75-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="03b75-151">**倉庫管理 \> 設定 \> ウェーブ \> ウェーブ テンプレート** の順に移動し、使用するウェーブ テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="03b75-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="03b75-152">テンプレートの、**メソッド** クイック タブで、**補充** メソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="03b75-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="03b75-153">**ウェーブ ステップ コード** で、補充テンプレートで選択したウェーブ ステップ コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="03b75-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="03b75-154">これらの手順を各法人に対して実行します。</span><span class="sxs-lookup"><span data-stu-id="03b75-154">You perform these steps for each legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
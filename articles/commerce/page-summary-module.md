---
title: ページ集計モジュール
description: このトピックでは、ページ集計モジュールと、これを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 04/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f1adae7169b210f21fe8b95e2c35b6051d4edd6d
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022852"
---
# <a name="page-summary-modules"></a><span data-ttu-id="993e3-103">ページ集計モジュール</span><span class="sxs-lookup"><span data-stu-id="993e3-103">Page summary modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="993e3-104">このトピックでは、ページ集計モジュールと、これを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="993e3-104">This topic covers page summary modules and describes how to add them to templates in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="993e3-105">ページ集計モジュールは、検索エンジンやソーシャル共有サイトが使用できるページ集計メタ データの入力を簡略化するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="993e3-105">Page summary modules help simplify the entry of page summary metadata that can be used by search engines and social sharing sites.</span></span> <span data-ttu-id="993e3-106">このメタデータには正規化されたリンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="993e3-106">This metadata includes canonical links.</span></span>

<span data-ttu-id="993e3-107">Dynamics 365 Commerce モジュール ライブラリには、ページ集計、カテゴリ ページ集計、リスト ページ集計、および製品ページ集計のモジュールなど、複数のページ集計モジュールが含まれています。</span><span class="sxs-lookup"><span data-stu-id="993e3-107">The Dynamics 365 Commerce module library contains several page summary modules, such as page summary, category page summary, list page summary, and product page summary modules.</span></span> <span data-ttu-id="993e3-108">各ページ集計モジュールには、そのモジュールが使用される特定のページ タイプを対象とする検索エンジン最適化 (SEO) メタデータがあります。</span><span class="sxs-lookup"><span data-stu-id="993e3-108">Each page summary module has search engine optimization (SEO) metadata that is tuned for the specific page types that the module will be used for.</span></span> <span data-ttu-id="993e3-109">すべての集計ページ モジュールは、次のセクションで説明するのと同じプロパティ セットを共有します。</span><span class="sxs-lookup"><span data-stu-id="993e3-109">All summary page modules share the same set of properties, which are described in the next section.</span></span>

> [!NOTE]
> <span data-ttu-id="993e3-110">Commerce モジュール ライブラリ バージョン 9.27 以上に含まれている製品ページの集計モジュールは、[Schema.org の製品スキーマ](https://schema.org/product) を使用して、JSON 形式の基本的な製品メタデータをページのヘッダー セクションに挿入しています。</span><span class="sxs-lookup"><span data-stu-id="993e3-110">The product page summary module, included with Commerce module library version 9.27 and higher, uses the [Schema.org product schema](https://schema.org/product) to insert basic JSON product metadata into a product page's header section.</span></span> <span data-ttu-id="993e3-111">このメタデータは、購入ボックス モジュールおよび他の製品ページ メタデータで使用されるのと同じ Commerce Runtime (CRT) API データ アクションを使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="993e3-111">This metadata is automatically generated using the same Commerce Runtime (CRT) API data actions used by the buy box module and other product page metadata.</span></span> <span data-ttu-id="993e3-112">多くの場合、製品メタデータで構成されている Schema.org は、主要な検索エンジンが豊富な検索結果を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="993e3-112">Schema.org structured product metadata is often used by major search engines to render rich search results.</span></span> <span data-ttu-id="993e3-113">既定では、製品ページの集計モジュールには、製品名、製品の説明、オファー (通貨および価格決定) 情報、および Schema.org の製品スキーマ仕様ごとの既定の画像の場所が含まれます。</span><span class="sxs-lookup"><span data-stu-id="993e3-113">By default, the product page summary module includes the product name, product description, offer (currency and pricing) information, and default image location per the Schema.org product schema specification.</span></span> <span data-ttu-id="993e3-114">必要に応じて、このモジュールと使用されるデータ アクションを Commerce オンライン SDK を使用して拡張し、メタデータ要件を強化または変更できます。</span><span class="sxs-lookup"><span data-stu-id="993e3-114">If necessary, this module and the data actions used by it can be extended using the Commerce online SDK to augment or modify metadata requirements.</span></span>


## <a name="summary-page-module-properties"></a><span data-ttu-id="993e3-115">集計ページ モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="993e3-115">Summary page module properties</span></span>

| <span data-ttu-id="993e3-116">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="993e3-116">Property name</span></span> | <span data-ttu-id="993e3-117">値</span><span class="sxs-lookup"><span data-stu-id="993e3-117">Values</span></span> | <span data-ttu-id="993e3-118">説明</span><span class="sxs-lookup"><span data-stu-id="993e3-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="993e3-119">肩書き</span><span class="sxs-lookup"><span data-stu-id="993e3-119">Title</span></span> | <span data-ttu-id="993e3-120">テキスト</span><span class="sxs-lookup"><span data-stu-id="993e3-120">Text</span></span> | <span data-ttu-id="993e3-121">サイト ページのタイトル。</span><span class="sxs-lookup"><span data-stu-id="993e3-121">The title of the site page.</span></span> |
| <span data-ttu-id="993e3-122">説明</span><span class="sxs-lookup"><span data-stu-id="993e3-122">Description</span></span> | <span data-ttu-id="993e3-123">テキスト</span><span class="sxs-lookup"><span data-stu-id="993e3-123">Text</span></span> | <span data-ttu-id="993e3-124">サイト ページの内容の簡単な説明。</span><span class="sxs-lookup"><span data-stu-id="993e3-124">A brief description of the site page's contents.</span></span> |
| <span data-ttu-id="993e3-125">キーワード</span><span class="sxs-lookup"><span data-stu-id="993e3-125">Keywords</span></span> | <span data-ttu-id="993e3-126">テキスト</span><span class="sxs-lookup"><span data-stu-id="993e3-126">Text</span></span> | <span data-ttu-id="993e3-127">サイト ページに関連する一連のコンマ区切りのキーワード。</span><span class="sxs-lookup"><span data-stu-id="993e3-127">A series of comma-separated keywords that are relevant to the site page.</span></span> |
| <span data-ttu-id="993e3-128">Twitter タグの無効化</span><span class="sxs-lookup"><span data-stu-id="993e3-128">Disable Twitter Tags</span></span> | <span data-ttu-id="993e3-129">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="993e3-129">**True** or **False**</span></span> | <span data-ttu-id="993e3-130">このプロパティが **True** に設定されている場合、HTML で Twitter タグは表示されません。</span><span class="sxs-lookup"><span data-stu-id="993e3-130">If this property is set to **True**, Twitter tags won't be rendered in the HTML.</span></span> |
| <span data-ttu-id="993e3-131">画像の共有</span><span class="sxs-lookup"><span data-stu-id="993e3-131">Sharing image</span></span> | <span data-ttu-id="993e3-132">使用できる画像の一覧で選択された画像</span><span class="sxs-lookup"><span data-stu-id="993e3-132">An image that is selected in a list of available images</span></span> | <span data-ttu-id="993e3-133">サイト ページが共有されている場合に使用する画像。</span><span class="sxs-lookup"><span data-stu-id="993e3-133">The image to use when the site page is shared.</span></span> |
| <span data-ttu-id="993e3-134">Facebook OG タグの無効化</span><span class="sxs-lookup"><span data-stu-id="993e3-134">Disable Facebook OG tags</span></span> | <span data-ttu-id="993e3-135">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="993e3-135">**True** or **False**</span></span> | <span data-ttu-id="993e3-136">このプロパティが **True** に設定されている場合、HTML で Facebook Open Graph (OG) タグは表示されません。</span><span class="sxs-lookup"><span data-stu-id="993e3-136">If this property is set to **True**, Facebook Open Graph (OG) tags won't be rendered in the HTML.</span></span> |
| <span data-ttu-id="993e3-137">アプリケーション設定で指定された接頭語と接尾語を無視する</span><span class="sxs-lookup"><span data-stu-id="993e3-137">Ignore the prefix and suffix specified in the application settings</span></span> | <span data-ttu-id="993e3-138">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="993e3-138">**True** or **False**</span></span> | <span data-ttu-id="993e3-139">このプロパティが **True** に設定されている場合、サイト レベルの接頭語と接尾語の設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="993e3-139">If this property is set to **True**, the site-level prefix and suffix settings will be ignored.</span></span> |

## <a name="add-a-page-summary-module-to-a-template"></a><span data-ttu-id="993e3-140">テンプレートへのページ集計モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="993e3-140">Add a page summary module to a template</span></span>

<span data-ttu-id="993e3-141">テンプレートにページ集計モジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="993e3-141">To add a page summary module to a template, follow these steps.</span></span>

1. <span data-ttu-id="993e3-142">サイトのコマース サイト ビルダで、**テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="993e3-142">In Commerce site builder for your site, select **Templates**.</span></span>
1. <span data-ttu-id="993e3-143">テンプレートを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="993e3-143">Select a template, and then select **Edit**.</span></span>
1. <span data-ttu-id="993e3-144">**HTML ヘッド** スロットで省略 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="993e3-144">In the **HTML Head** slot, select the ellipsis (**...**), and then select **Add module**.</span></span>
1. <span data-ttu-id="993e3-145">**モジュールの追加** ダイアログ ボックスで、**ページ集計モジュール** (または、**リスト ページ集計** などの、別のページ集計モジュール) を選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="993e3-145">In the **Add Module** dialog box, select the **Page summary** module (or another page summary module, such as **List page summary**), and then select **OK**.</span></span> <span data-ttu-id="993e3-146">テンプレートを使用するページ タイプ用の適切なページ集計モジュールが追加されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="993e3-146">Make sure that you add the appropriate page summary module for the page types that the template will be used for.</span></span>

    ![新しいモジュールの追加](media/page-summary-1.png)

<span data-ttu-id="993e3-148">集計モジュールを追加した後、次の図の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="993e3-148">After the summary module is added, it should resemble the example in the following illustration.</span></span> <span data-ttu-id="993e3-149">これでモジュールが構成され、テンプレートを保存および公開できます。</span><span class="sxs-lookup"><span data-stu-id="993e3-149">The module can now be configured, and the template can be saved and published.</span></span>

![追加されたページ集計モジュール](media/page-summary-2.png)

> [!NOTE]
> <span data-ttu-id="993e3-151">テンプレートで既定値を設定できますが、これらの値はテンプレートを使用するページ上で上書きできます。</span><span class="sxs-lookup"><span data-stu-id="993e3-151">Although you can set default values in the template, those values can be overridden on pages that use the template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="993e3-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="993e3-152">Additional resources</span></span>

[<span data-ttu-id="993e3-153">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="993e3-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="993e3-154">既定のページ モジュール</span><span class="sxs-lookup"><span data-stu-id="993e3-154">Default page module</span></span>](default-page-module.md)

[<span data-ttu-id="993e3-155">外部およびインライン スクリプト モジュール</span><span class="sxs-lookup"><span data-stu-id="993e3-155">External and inline script modules</span></span>](script-module.md)

[<span data-ttu-id="993e3-156">メタタグ モジュール</span><span class="sxs-lookup"><span data-stu-id="993e3-156">Metatags module</span></span>](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

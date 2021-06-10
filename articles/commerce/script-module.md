---
title: 外部およびインライン スクリプト モジュール
description: このトピックでは、外部およびインライン スクリプト モジュールと、これらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。
author: samjarawan
ms.date: 04/02/2021
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
ms.openlocfilehash: b38d6ec657dec37737cc345cb9ea872fd78791fc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018594"
---
# <a name="external-and-inline-script-modules"></a><span data-ttu-id="5aad1-103">外部およびインライン スクリプト モジュール</span><span class="sxs-lookup"><span data-stu-id="5aad1-103">External and inline script modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5aad1-104">このトピックでは、外部およびインライン スクリプト モジュールと、これらを Microsoft Dynamics 365 Commerce のテンプレートに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5aad1-104">This topic covers external and inline script modules and describes how to add them to templates in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5aad1-105">外部およびインライン スクリプト モジュールを使用して、クライアント側の JavaScript スクリプトをサイト ページに追加できます。</span><span class="sxs-lookup"><span data-stu-id="5aad1-105">External and inline script modules let you add client-side JavaScript scripts to site pages.</span></span> <span data-ttu-id="5aad1-106">スクリプトは、インラインの場合、または外部ファイルから呼び出す場合があります。</span><span class="sxs-lookup"><span data-stu-id="5aad1-106">The scripts can be inline, or they can be called from an external file.</span></span> <span data-ttu-id="5aad1-107">外部およびインライン スクリプト モジュールは、テンプレートの **HTML Head**、**本文の開始**、または **本文の終了** に追加できます。</span><span class="sxs-lookup"><span data-stu-id="5aad1-107">External and inline script modules can be added to a template's **HTML Head**, **Body Begin**, or **Body End** slot.</span></span>

<span data-ttu-id="5aad1-108">次の図は、外部およびインライン スクリプト モジュールが、テンプレートでサポートされているさまざまなスロットに追加された例を示しています。</span><span class="sxs-lookup"><span data-stu-id="5aad1-108">The following illustration shows an example where external and inline script modules have been added to the various supported slots in a template.</span></span>

![テンプレートのさまざまなスロットのスクリプト モジュール](media/script-modules-1.png)

## <a name="external-script-module-properties"></a><span data-ttu-id="5aad1-110">外部スクリプト モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="5aad1-110">External script module properties</span></span>

| <span data-ttu-id="5aad1-111">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5aad1-111">Property name</span></span> | <span data-ttu-id="5aad1-112">値</span><span class="sxs-lookup"><span data-stu-id="5aad1-112">Values</span></span> | <span data-ttu-id="5aad1-113">説明</span><span class="sxs-lookup"><span data-stu-id="5aad1-113">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5aad1-114">スクリプト ソース</span><span class="sxs-lookup"><span data-stu-id="5aad1-114">Script source</span></span> | <span data-ttu-id="5aad1-115">テキスト</span><span class="sxs-lookup"><span data-stu-id="5aad1-115">Text</span></span> | <span data-ttu-id="5aad1-116">スクリプト ファイルの場所の URL です。</span><span class="sxs-lookup"><span data-stu-id="5aad1-116">The URL of the script file location.</span></span> |
| <span data-ttu-id="5aad1-117">スクリプトの非同期実行</span><span class="sxs-lookup"><span data-stu-id="5aad1-117">Execute script asynchronously</span></span> | <span data-ttu-id="5aad1-118">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5aad1-118">**True** or **False**</span></span> | <span data-ttu-id="5aad1-119">このプロパティが **True** に設定されている場合、スクリプトは非同期で実行されます。</span><span class="sxs-lookup"><span data-stu-id="5aad1-119">If this property is set to **True**, the script will run asynchronously.</span></span> |
| <span data-ttu-id="5aad1-120">スクリプト実行の延期</span><span class="sxs-lookup"><span data-stu-id="5aad1-120">Defer script execution</span></span> | <span data-ttu-id="5aad1-121">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="5aad1-121">**True** or **False**</span></span> | <span data-ttu-id="5aad1-122">このプロパティが **True** に設定されている場合、ページの実行が完了するとスクリプトが実行されます。</span><span class="sxs-lookup"><span data-stu-id="5aad1-122">If this property is set to **True**, the script will run when the page has finished running.</span></span> |

## <a name="inline-script-module-properties"></a><span data-ttu-id="5aad1-123">インライン スクリプト モジュールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="5aad1-123">Inline script module properties</span></span>

| <span data-ttu-id="5aad1-124">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="5aad1-124">Property name</span></span> | <span data-ttu-id="5aad1-125">値</span><span class="sxs-lookup"><span data-stu-id="5aad1-125">Values</span></span> | <span data-ttu-id="5aad1-126">説明</span><span class="sxs-lookup"><span data-stu-id="5aad1-126">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5aad1-127">インライン スクリプト</span><span class="sxs-lookup"><span data-stu-id="5aad1-127">Inline script</span></span> | <span data-ttu-id="5aad1-128">テキスト</span><span class="sxs-lookup"><span data-stu-id="5aad1-128">Text</span></span> | <span data-ttu-id="5aad1-129">HTML ページの **\<script\>** タグにインラインがインサートされるスクリプト ステートメントのコレクション。</span><span class="sxs-lookup"><span data-stu-id="5aad1-129">The collection of scripting statements that will be inserted inline into **\<script\>** tags on the HTML page.</span></span> |

## <a name="content-security-policy"></a><span data-ttu-id="5aad1-130">コンテンツ セキュリティ ポリシー</span><span class="sxs-lookup"><span data-stu-id="5aad1-130">Content security policy</span></span>

<span data-ttu-id="5aad1-131">コンテンツ セキュリティ ポリシー (CSP) が有効の場合、外部スクリプトが実行されない場合があります。</span><span class="sxs-lookup"><span data-stu-id="5aad1-131">If content security policy (CSP) is enabled, external scripts might not run.</span></span> <span data-ttu-id="5aad1-132">外部スクリプトを実行するには、最初にそれらのドメイン URL を Commerce サイト ビルダーの **script-src** CSP ディレクティブに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5aad1-132">To enable external scripts to run, you must first add their domain URLs to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="5aad1-133">詳細については、[コンテンツ セキュリティ ポリシーの管理](manage-csp.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aad1-133">For more information, see [Manage Content Security Policy](manage-csp.md).</span></span>

## <a name="add-a-script-module-to-a-template"></a><span data-ttu-id="5aad1-134">テンプレートへのスクリプト モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="5aad1-134">Add a script module to a template</span></span>

<span data-ttu-id="5aad1-135">作業テンプレートにスクリプト モジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5aad1-135">To add a script module to a template, follow these steps.</span></span>

1. <span data-ttu-id="5aad1-136">サイトのコマース サイト ビルダで、**テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5aad1-136">In Commerce site builder for your site, select **Templates**.</span></span>
1. <span data-ttu-id="5aad1-137">テンプレートを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5aad1-137">Select a template, and then select **Edit**.</span></span>
1. <span data-ttu-id="5aad1-138">**本文の開始** スロットで、省略記号ボタン (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5aad1-138">In the **Body Begin** slot, select the ellipsis (**...**), and then select **Add module**.</span></span>

    ![新しいモジュールの追加](media/script-modules-2.png)

1. <span data-ttu-id="5aad1-140">**モジュールの追加** ダイアログ ボックスで、**外部スクリプト** モジュールまたは **インライン スクリプト** モジュールを選択し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5aad1-140">In the **Add Module** dialog box, select either the **External script** module or the **Inline script** module, and then select **OK**.</span></span>

    ![スクリプト モジュールの追加](media/script-modules-3.png)

<span data-ttu-id="5aad1-142">スクリプト モジュールを追加した後、次の図の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="5aad1-142">After the script module is added, it should resemble the example in the following illustration.</span></span> <span data-ttu-id="5aad1-143">これでモジュールが構成され、テンプレートを保存および公開できます。</span><span class="sxs-lookup"><span data-stu-id="5aad1-143">The module can now be configured, and the template can be saved and published.</span></span>

![追加された内部スクリプト モジュール](media/script-modules-4.png)

## <a name="additional-resources"></a><span data-ttu-id="5aad1-145">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5aad1-145">Additional resources</span></span>

[<span data-ttu-id="5aad1-146">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="5aad1-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5aad1-147">既定のページ モジュール</span><span class="sxs-lookup"><span data-stu-id="5aad1-147">Default page module</span></span>](default-page-module.md)

[<span data-ttu-id="5aad1-148">ページ集計モジュール</span><span class="sxs-lookup"><span data-stu-id="5aad1-148">Page summary modules</span></span>](page-summary-module.md)

[<span data-ttu-id="5aad1-149">メタタグ モジュール</span><span class="sxs-lookup"><span data-stu-id="5aad1-149">Metatags module</span></span>](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

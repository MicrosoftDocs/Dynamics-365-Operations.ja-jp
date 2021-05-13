---
title: 既定のページ モジュール
description: このトピックでは、既定のページ モジュールと、これを Microsoft Dynamics 365 Commerce のページ テンプレートに追加する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4035406affdc6566bd6dcf0b423803fd6d919105
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853508"
---
# <a name="default-page-module"></a><span data-ttu-id="10cac-103">既定のページ モジュール</span><span class="sxs-lookup"><span data-stu-id="10cac-103">Default page module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10cac-104">このトピックでは、既定のページ モジュールと、これを Microsoft Dynamics 365 Commerce のページ テンプレートに追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="10cac-104">This topic covers default page modules and describes how to add them to page templates in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="10cac-105">既定のページ モジュールは、ページのルート コンテナーとなる特別なモジュールで、テンプレートの **本文** スロットにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="10cac-105">The default page module is a special module that becomes the root container of a page and can be added only to a template's **Body** slot.</span></span> <span data-ttu-id="10cac-106">既定のページ モジュールは、次の例に示すように、コマース サイト ビルダ ページ エディターに表示されるコア スロット (**ヘッダー スロット**、**サブ ヘッダー スロット**、**メイン スロット**、**サブフッター スロット**、および **フッター スロット**) を定義します。</span><span class="sxs-lookup"><span data-stu-id="10cac-106">The default page module defines the core slots (**Header Slot**, **Sub Header Slot**, **Main Slot**, **Sub Footer Slot**, and **Footer Slot**) that appear in the Commerce site builder page editor, as shown in the following example illustration.</span></span>

![ページ モジュール スロット](media/page-module-1.png)

<span data-ttu-id="10cac-108">コマース モジュール ライブラリは、既定のページ モジュールの 1 つのタイプのみを提供します。</span><span class="sxs-lookup"><span data-stu-id="10cac-108">The Commerce module library provides only one type of default page module.</span></span> <span data-ttu-id="10cac-109">ただし、 [コマース オンライン チャンネル機能拡張ソフトウェア開発キット (SDK)](e-commerce-extensibility/overview.md) を使用して、必要に応じて追加のカスタムの既定のページ モジュールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="10cac-109">However, you can use the [Commerce online channel extensibility software development kit (SDK)](e-commerce-extensibility/overview.md) to create additional, custom default page modules as you require.</span></span>

## <a name="page-module-properties"></a><span data-ttu-id="10cac-110">ページ モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="10cac-110">Page module properties</span></span>

| <span data-ttu-id="10cac-111">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="10cac-111">Property name</span></span> | <span data-ttu-id="10cac-112">値</span><span class="sxs-lookup"><span data-stu-id="10cac-112">Values</span></span> | <span data-ttu-id="10cac-113">説明</span><span class="sxs-lookup"><span data-stu-id="10cac-113">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="10cac-114">[メイン コンテキストへスキップ] のテキスト</span><span class="sxs-lookup"><span data-stu-id="10cac-114">Skip to main content text</span></span> | <span data-ttu-id="10cac-115">テキスト</span><span class="sxs-lookup"><span data-stu-id="10cac-115">Text</span></span> | <span data-ttu-id="10cac-116">ページの「メイン コンテンツにスキップ」リンクに表示されるリンク テキスト。</span><span class="sxs-lookup"><span data-stu-id="10cac-116">The link text that should appear in the "skip to main content" link on the page.</span></span> <span data-ttu-id="10cac-117">既定値は **メイン コンテンツ にスキップ** です。</span><span class="sxs-lookup"><span data-stu-id="10cac-117">The default value is **Skip to main content**.</span></span> |
| <span data-ttu-id="10cac-118">テーマ</span><span class="sxs-lookup"><span data-stu-id="10cac-118">Theme</span></span> | <span data-ttu-id="10cac-119">使用できるテーマの一覧で選択されたテーマ</span><span class="sxs-lookup"><span data-stu-id="10cac-119">A theme that is selected in a list of available themes</span></span> | <span data-ttu-id="10cac-120">このテンプレートから派生されたページに使用するテーマ。</span><span class="sxs-lookup"><span data-stu-id="10cac-120">The theme to use for the pages that are derived from this template.</span></span><p><span data-ttu-id="10cac-121"><strong> 注: </strong> このプロパティは非推奨になり、将来のリリースで削除されます。</span><span class="sxs-lookup"><span data-stu-id="10cac-121"><strong>Note:</strong> This property has been deprecated and will be removed in a future release.</span></span> <span data-ttu-id="10cac-122">テーマは、サイト レベルでのみ設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="10cac-122">Themes should be set only at the site level.</span></span></p> |
| <span data-ttu-id="10cac-123">サインインが必要ですか?</span><span class="sxs-lookup"><span data-stu-id="10cac-123">Requires sign-in?</span></span> | <span data-ttu-id="10cac-124">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="10cac-124">**True** or **False**</span></span> | <span data-ttu-id="10cac-125">このブール値プロパティは、ページへのアクセスにユーザーのサインインが必要かどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="10cac-125">This Boolean property controls whether access to the page requires user sign-in.</span></span> <span data-ttu-id="10cac-126">**True** に設定されている場合、サインインしていないユーザーはサインイン ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="10cac-126">If it's set to **True**, users who aren't signed in will be redirected to the sign-in page.</span></span> |

## <a name="add-a-default-page-module-to-a-template"></a><span data-ttu-id="10cac-127">テンプレートへの既定ページ モジュールの追加</span><span class="sxs-lookup"><span data-stu-id="10cac-127">Add a default page module to a template</span></span>

<span data-ttu-id="10cac-128">テンプレートに既定ページ モジュールを追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="10cac-128">To add a default page module to a template, follow these steps.</span></span>

1. <span data-ttu-id="10cac-129">サイトのコマース サイト ビルダで、**テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10cac-129">In Commerce site builder for your site, select **Templates**.</span></span>
1. <span data-ttu-id="10cac-130">テンプレートを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10cac-130">Select a template, and then select **Edit**.</span></span>
1. <span data-ttu-id="10cac-131">**本文** スロットで、省略記号 (**...**) を選択し、**モジュールの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10cac-131">In the **Body** slot, select the ellipsis (**...**), and then select **Add module**.</span></span>

    ![新しいモジュールの追加](media/page-module-2.png)

1. <span data-ttu-id="10cac-133">**モジュールの追加** ダイアログ ボックスで、**規定のページ** モジュールを選択して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="10cac-133">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>

    ![既定のページ モジュールの追加](media/page-module-3.png)

<span data-ttu-id="10cac-135">既定のページ モジュールを追加した後、次の図の例のようになります。</span><span class="sxs-lookup"><span data-stu-id="10cac-135">After the default page module is added, it should resemble the example in the following illustration.</span></span> <span data-ttu-id="10cac-136">これでモジュールが構成され、テンプレートを保存および公開できます。</span><span class="sxs-lookup"><span data-stu-id="10cac-136">The module can now be configured, and the template can be saved and published.</span></span>

![既定のページ モジュールが追加された](media/page-module-4.png)

## <a name="additional-resources"></a><span data-ttu-id="10cac-138">追加リソース</span><span class="sxs-lookup"><span data-stu-id="10cac-138">Additional resources</span></span>

[<span data-ttu-id="10cac-139">モジュール ライブラリの概要</span><span class="sxs-lookup"><span data-stu-id="10cac-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="10cac-140">ページ集計モジュール</span><span class="sxs-lookup"><span data-stu-id="10cac-140">Page summary modules</span></span>](page-summary-module.md)

[<span data-ttu-id="10cac-141">外部およびインライン スクリプト モジュール</span><span class="sxs-lookup"><span data-stu-id="10cac-141">External and inline script modules</span></span>](script-module.md)

[<span data-ttu-id="10cac-142">メタタグ モジュール</span><span class="sxs-lookup"><span data-stu-id="10cac-142">Metatags module</span></span>](metatags-module.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

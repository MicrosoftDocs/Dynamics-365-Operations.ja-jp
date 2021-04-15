---
title: サイト テーマの選択
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794070"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="d8ff8-103">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="d8ff8-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d8ff8-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d8ff8-105">サイトのレイアウトおよびスタイル (たとえば、フォント、サイズ、および色) は、選択し、サイトに適用するテーマによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="d8ff8-106">テーマは会社の開発者が作成し、配置します。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="d8ff8-107">テーマの概要については、[テーマの概要](e-commerce-extensibility/theming.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="d8ff8-108">テーマを作成し、配置する方法の詳細については、[新しいテーマの作成](e-commerce-extensibility/create-theme.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="d8ff8-109">既定では、サイトを最初に作成した時に、**Fabrikam** という名前のテーマが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="d8ff8-110">この既定のテーマは、Commerce モジュール ライブラリの一部として提供されます。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="d8ff8-111">サイトに追加のテーマを配置した後、サイトをコンフィギュレーションして、それらの 1 つを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="d8ff8-112">サイトのテーマの選択</span><span class="sxs-lookup"><span data-stu-id="d8ff8-112">Select the site theme</span></span>

<span data-ttu-id="d8ff8-113">サイトに適用するテーマを選択するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="d8ff8-114">サイト作成環境で、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="d8ff8-115">**サイトの管理**\>**拡張性** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="d8ff8-116">**テーマ** の下で、ドロップダウン メニューでテーマを選択します。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="d8ff8-117">選択したテーマをサイトに適用するには、**保存して公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="d8ff8-118">選択したテーマは、**拡張性** のページで **保存して公開** を選択してすぐにサイトに公開されます。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="d8ff8-119">適用する前にサイトでテーマをプレビューするには、開発またはサンドボックス環境を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d8ff8-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8ff8-120">追加リソース</span><span class="sxs-lookup"><span data-stu-id="d8ff8-120">Additional resources</span></span>

[<span data-ttu-id="d8ff8-121">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="d8ff8-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d8ff8-122">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="d8ff8-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d8ff8-123">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="d8ff8-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d8ff8-124">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="d8ff8-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d8ff8-125">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="d8ff8-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d8ff8-126">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="d8ff8-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="d8ff8-127">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="d8ff8-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="d8ff8-128">テーマの概要</span><span class="sxs-lookup"><span data-stu-id="d8ff8-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="d8ff8-129">新しいテーマの作成</span><span class="sxs-lookup"><span data-stu-id="d8ff8-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

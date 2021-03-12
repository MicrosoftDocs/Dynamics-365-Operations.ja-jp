---
title: サイト テーマの選択
description: このトピックでは、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982409"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="5a89b-103">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="5a89b-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a89b-104">このトピックでは、Microsoft Dynamics 365 Commerce のサイトのテーマを設定または変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5a89b-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5a89b-105">概要</span><span class="sxs-lookup"><span data-stu-id="5a89b-105">Overview</span></span>

<span data-ttu-id="5a89b-106">サイトのレイアウトおよびスタイル (たとえば、フォント、サイズ、および色) は、選択し、サイトに適用するテーマによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="5a89b-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="5a89b-107">テーマは会社の開発者が作成し、配置します。</span><span class="sxs-lookup"><span data-stu-id="5a89b-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="5a89b-108">テーマの概要については、[テーマの概要](e-commerce-extensibility/theming.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a89b-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="5a89b-109">テーマを作成し、配置する方法の詳細については、[新しいテーマの作成](e-commerce-extensibility/create-theme.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a89b-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="5a89b-110">既定では、サイトを最初に作成した時に、**Fabrikam** という名前のテーマが使用されます。</span><span class="sxs-lookup"><span data-stu-id="5a89b-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="5a89b-111">この既定のテーマは、Commerce モジュール ライブラリの一部として提供されます。</span><span class="sxs-lookup"><span data-stu-id="5a89b-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="5a89b-112">サイトに追加のテーマを配置した後、サイトをコンフィギュレーションして、それらの 1 つを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5a89b-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="5a89b-113">サイトのテーマの選択</span><span class="sxs-lookup"><span data-stu-id="5a89b-113">Select the site theme</span></span>

<span data-ttu-id="5a89b-114">サイトに適用するテーマを選択するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5a89b-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="5a89b-115">サイト作成環境で、サイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="5a89b-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="5a89b-116">**サイトの管理**\>**拡張性** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5a89b-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="5a89b-117">**テーマ** の下で、ドロップダウン メニューでテーマを選択します。</span><span class="sxs-lookup"><span data-stu-id="5a89b-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="5a89b-118">選択したテーマをサイトに適用するには、**保存して公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5a89b-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="5a89b-119">選択したテーマは、**拡張性** のページで **保存して公開** を選択してすぐにサイトに公開されます。</span><span class="sxs-lookup"><span data-stu-id="5a89b-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="5a89b-120">適用する前にサイトでテーマをプレビューするには、開発またはサンドボックス環境を使用できます。</span><span class="sxs-lookup"><span data-stu-id="5a89b-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a89b-121">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5a89b-121">Additional resources</span></span>

[<span data-ttu-id="5a89b-122">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="5a89b-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="5a89b-123">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="5a89b-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5a89b-124">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="5a89b-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5a89b-125">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="5a89b-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5a89b-126">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="5a89b-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5a89b-127">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="5a89b-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5a89b-128">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="5a89b-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="5a89b-129">テーマの概要</span><span class="sxs-lookup"><span data-stu-id="5a89b-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="5a89b-130">新しいテーマの作成</span><span class="sxs-lookup"><span data-stu-id="5a89b-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)


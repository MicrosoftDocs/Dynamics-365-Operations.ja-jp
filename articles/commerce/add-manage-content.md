---
title: コンテンツを追加する方法
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトでコンテンツを追加、および管理する方法を説明します。
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2232dc7cdd24416b0df0919b96cd5d1f8113299f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914657"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="e7714-103">コンテンツを追加する方法</span><span class="sxs-lookup"><span data-stu-id="e7714-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e7714-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトでコンテンツを追加、および管理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="e7714-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="e7714-105">概要</span><span class="sxs-lookup"><span data-stu-id="e7714-105">Overview</span></span>

<span data-ttu-id="e7714-106">サイトの概観、およびコンテンツを変更するには、さまざまな方法があります。</span><span class="sxs-lookup"><span data-stu-id="e7714-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="e7714-107">必要なカスタマイズのレベルによっては、これらの変更の多くは開発者以外でも実装することができます。</span><span class="sxs-lookup"><span data-stu-id="e7714-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="e7714-108">たとえば、テンプレートを構築したり、テーマを選択したり、モジュールを選択およびコンフィギュレーションするためのコードを記述する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e7714-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="e7714-109">これに対して、E コマース ソフトウェア開発キット (SDK) および Microsoft Dynamics Lifecycle Services (LCS) の配置ワークフローを使用する必要があるため、新しいテーマまたはモジュールを作成するには開発スキルが必要です。</span><span class="sxs-lookup"><span data-stu-id="e7714-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="e7714-110">次のトピックでは、サイトのコンテンツの追加および管理方法について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="e7714-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="e7714-111">サイトの中で開発者を必要としない領域に重点を置いています。</span><span class="sxs-lookup"><span data-stu-id="e7714-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="e7714-112">必要に応じて、SDK 作業を必要とするタスクを指摘します。</span><span class="sxs-lookup"><span data-stu-id="e7714-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="e7714-113">既存のサイト ページのテキスト、画像、またはビデオを変更するには、[モジュールの使用](work-with-modules.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7714-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="e7714-114">Web コンテンツの作成者に、簡単で、ブランドイメージに沿った作成エクスペリエンスを保証するには、[テンプレートの使用](work-with-templates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7714-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="e7714-115">サイト ページのセクションを並べ替えるには、[レイアウトの使用](work-with-layouts.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7714-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="e7714-116">サイト ページのフォント、色、および一般的な外観を変更するには、[サイトのテーマの選択](select-site-theme.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7714-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7714-117">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e7714-117">Additional resources</span></span>

[<span data-ttu-id="e7714-118">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="e7714-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="e7714-119">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="e7714-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="e7714-120">公開グループで動作</span><span class="sxs-lookup"><span data-stu-id="e7714-120">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="e7714-121">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="e7714-121">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="e7714-122">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="e7714-122">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="e7714-123">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="e7714-123">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="e7714-124">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="e7714-124">Customize site navigation</span></span>](customize-site-navigation.md)

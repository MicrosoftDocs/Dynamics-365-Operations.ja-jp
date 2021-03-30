---
title: コンテンツを追加する方法
description: このトピックでは、Microsoft Dynamics 365 Commerceサイト ビルダーの Web 作成ツール セットを使用してコンテンツを管理するための場所と方法の概要と選択リンクを示します。
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eb0b1c3f77bb71ba04c9110ed25fb80c2f2e61f4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208066"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="df2c1-103">コンテンツを追加する方法</span><span class="sxs-lookup"><span data-stu-id="df2c1-103">Ways to add content</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df2c1-104">このトピックでは、Microsoft Dynamics 365 Commerce サイト ビルダーの Web 作成ツールセットを使用してコンテンツを管理する方法に関する概要とドキュメントのリンクを示します。</span><span class="sxs-lookup"><span data-stu-id="df2c1-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

## <a name="overview"></a><span data-ttu-id="df2c1-105">概要</span><span class="sxs-lookup"><span data-stu-id="df2c1-105">Overview</span></span>

<span data-ttu-id="df2c1-106">サイトの概観、およびコンテンツを変更するには、さまざまな方法があります。</span><span class="sxs-lookup"><span data-stu-id="df2c1-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="df2c1-107">必要なカスタマイズ レベルによっては、これらの変更の多くを、Dynamics 365 Commerce に含まれている Web 作成ツールセットであるサイト ビルダー内の開発者以外のユーザーが実装することができます。</span><span class="sxs-lookup"><span data-stu-id="df2c1-107">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="df2c1-108">サイト ビルダーを使用すると、テンプレートの作成、テーマの選択、コードを記述せずにモジュールの選択やコンフィギュレーションを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="df2c1-108">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="df2c1-109">これに対して、E コマース ソフトウェア開発キット (SDK) および Microsoft Dynamics Lifecycle Services (LCS) の配置ワークフローを使用する必要があるため、新しいテーマまたはモジュールを作成するには開発スキルが必要です。</span><span class="sxs-lookup"><span data-stu-id="df2c1-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="df2c1-110">次のトピックは、サイト コンテンツを追加および管理する方法を理解するための出発点として役立ちます。</span><span class="sxs-lookup"><span data-stu-id="df2c1-110">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="df2c1-111">リストされているトピックのほとんどは、開発者を必要としないサイトの領域に焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="df2c1-111">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="df2c1-112">基本的なコンテンツの編集である場合もあれば、サイト管理タスクに焦点を当てている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="df2c1-112">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="df2c1-113">これらの各トピックは、SDK の作業が必要な特定のタスクを示します。</span><span class="sxs-lookup"><span data-stu-id="df2c1-113">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="df2c1-114">各トピックでは、既にサイトがプロビジョニングされており、サイトのサイト ビルダー ツールセットへのアクセスが許可されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="df2c1-114">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="df2c1-115">次のいずれかのトピックを選択して、開始します。</span><span class="sxs-lookup"><span data-stu-id="df2c1-115">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="df2c1-116">サイト ビルダーおよびこのドキュメント内で使用されているコンテンツ管理用語についてよく理解するには、[ページ モデルの用語集](page-elements-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-116">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="df2c1-117">モジュールがコンテンツ管理ワークフロー内でどのように機能するかを理解するには、[モジュールの使用](work-with-modules.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-117">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="df2c1-118">既存のサイト ページのテキスト、画像、またはビデオを変更するには、[モジュールの使用](work-with-modules.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-118">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="df2c1-119">フラグメントによってコンテンツ管理の効率と柔軟性を高める方法を確認するには、[フラグメントの使用](work-with-fragments.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-119">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="df2c1-120">Web コンテンツ作成者に対してブランドイメージに沿った作成エクスペリエンスを成功させるには、[テンプレートとレイアウトの概要](templates-layouts-overview.md)および[テンプレートの使用](work-with-templates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-120">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="df2c1-121">サイト ページのセクションを並べ替えるには、[レイアウトの使用](work-with-layouts.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-121">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="df2c1-122">サイト ページのフォント、色、および一般的な外観を変更するには、[サイトのテーマの選択](select-site-theme.md)または [CSS 上書きファイルの使用](css-override-files.md)参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-122">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="df2c1-123">新しいナビゲーション オプションの並べ替えまたは追加をするには、[サイト ナビゲーションのカスタマイズ](customize-site-navigation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-123">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="df2c1-124">一連の広範な Web コンテンツの変更をステージ、プレビュー、および発行する方法について[公開グループの作業](publish-groups.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df2c1-124">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df2c1-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="df2c1-125">Additional resources</span></span>

[<span data-ttu-id="df2c1-126">作成ページの概要</span><span class="sxs-lookup"><span data-stu-id="df2c1-126">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="df2c1-127">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="df2c1-127">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="df2c1-128">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="df2c1-128">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="df2c1-129">クロスチャネル共有の有効化と使用</span><span class="sxs-lookup"><span data-stu-id="df2c1-129">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
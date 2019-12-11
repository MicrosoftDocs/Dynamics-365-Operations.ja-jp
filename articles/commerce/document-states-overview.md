---
title: ドキュメントの状態とライフサイクル
description: このトピックでは、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: a34d10edbf84ac1814afdc7107727aea68a303e0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770438"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="226dd-103">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="226dd-103">Document states and lifecycle</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="226dd-104">このトピックでは、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。</span><span class="sxs-lookup"><span data-stu-id="226dd-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="226dd-105">ドキュメントの状態の説明</span><span class="sxs-lookup"><span data-stu-id="226dd-105">Document state descriptions</span></span>

<span data-ttu-id="226dd-106">[ページ要素](page-elements-overview.md)のトピックでは、コンテンツ管理システム (CMS) 内のさまざまなドキュメント タイプを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="226dd-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="226dd-107">これらのドキュメント タイプは、オーサリング ツールで複数の状態を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="226dd-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="226dd-108">ドキュメントの状態によって、データの競合を防ぎ、バージョン管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="226dd-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="226dd-109">これらは、ドキュメントを変更できるユーザー、ドキュメントを変更できる場合、および他のユーザーが変更を表示できる場合を決定します。</span><span class="sxs-lookup"><span data-stu-id="226dd-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="226dd-110">次の表は、コマースのページ要素の可能なドキュメント状態を示しています。</span><span class="sxs-lookup"><span data-stu-id="226dd-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="226dd-111">ドキュメントの状態</span><span class="sxs-lookup"><span data-stu-id="226dd-111">Document state</span></span> | <span data-ttu-id="226dd-112">説明</span><span class="sxs-lookup"><span data-stu-id="226dd-112">Description</span></span> |
|---|---|
| <span data-ttu-id="226dd-113">チェックアウトされました</span><span class="sxs-lookup"><span data-stu-id="226dd-113">Checked out</span></span> | <span data-ttu-id="226dd-114">CMS 品目がチェックアウトされると、他の認証されたシステム ユーザーがそれを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="226dd-114">When a CMS item is checked out to you, it can't be edited by any other authenticated system users.</span></span> <span data-ttu-id="226dd-115">品目に対して行った変更は、そのユーザーに対してのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="226dd-115">Any changes that you make to the item are visible only to you.</span></span> |
| <span data-ttu-id="226dd-116">チェックインされました</span><span class="sxs-lookup"><span data-stu-id="226dd-116">Checked in</span></span> | <span data-ttu-id="226dd-117">CMS 項目をチェック インすると、他の認証されたシステム ユーザーはすべての変更を参照できます。その後、そのユーザーは、その品目をチェックアウトして編集することができます。</span><span class="sxs-lookup"><span data-stu-id="226dd-117">When a CMS item is checked in, all changes are visible to other authenticated system users, and those users can then check out the item and edit it.</span></span> <span data-ttu-id="226dd-118">各チェックインでは、品目の履歴にドキュメント バージョンのレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="226dd-118">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="226dd-119">公開済</span><span class="sxs-lookup"><span data-stu-id="226dd-119">Published</span></span> | <span data-ttu-id="226dd-120">CMS 品目が公開されると、サイトにプッシュされ、認証されていない外部ユーザーによってインターネット上で検出可能になります。</span><span class="sxs-lookup"><span data-stu-id="226dd-120">When a CMS item is published, it's pushed to your live site and becomes discoverable on the internet by non-authenticated external users.</span></span> <span data-ttu-id="226dd-121">品目は、チェックインされている場合にのみ公開できます。</span><span class="sxs-lookup"><span data-stu-id="226dd-121">Items can be published only if they have been checked in.</span></span> |
| <span data-ttu-id="226dd-122">保存されました</span><span class="sxs-lookup"><span data-stu-id="226dd-122">Saved</span></span> | <span data-ttu-id="226dd-123">チェックアウト済みの CMS 品目に対して行われた変更は、品目がチェックインまたは公開される前に CMS に保存できます。</span><span class="sxs-lookup"><span data-stu-id="226dd-123">Changes that have been made to a checked-out CMS item can be saved to the CMS before the item is checked in or published.</span></span> <span data-ttu-id="226dd-124">これらの保存された変更内容は、品目がチェックインされるまで、他の認証されたシステム ユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="226dd-124">These saved changes aren't visible to other authenticated system users until the item is checked in.</span></span> <span data-ttu-id="226dd-125">品目が公開されるまで、外部ユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="226dd-125">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="226dd-126">破棄済チェックアウト</span><span class="sxs-lookup"><span data-stu-id="226dd-126">Discarded check out</span></span> | <span data-ttu-id="226dd-127">チェックアウトされた CMS 項目を破棄すると、保存されていたすべての変更が削除され、品目は最後にチェックインされたバージョンに戻ります。</span><span class="sxs-lookup"><span data-stu-id="226dd-127">When a checked-out CMS item is discarded, all saved changes are deleted, and the item reverts to the version that was most recently checked in.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="226dd-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="226dd-128">Additional resources</span></span>

[<span data-ttu-id="226dd-129">コンテンツを追加する方法</span><span class="sxs-lookup"><span data-stu-id="226dd-129">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="226dd-130">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="226dd-130">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="226dd-131">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="226dd-131">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="226dd-132">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="226dd-132">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="226dd-133">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="226dd-133">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="226dd-134">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="226dd-134">Customize site navigation</span></span>](customize-site-navigation.md)

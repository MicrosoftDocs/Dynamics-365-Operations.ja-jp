---
title: ドキュメントの状態とライフサイクル
description: このトピックでは、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。
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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413758"
---
# <a name="document-states-and-lifecycle"></a><span data-ttu-id="df0f4-103">ドキュメントの状態とライフサイクル</span><span class="sxs-lookup"><span data-stu-id="df0f4-103">Document states and lifecycle</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df0f4-104">このトピックでは、Microsoft Dynamics 365 Commerce のページ要素のさまざまなドキュメントの状態について説明します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-104">This topic covers the various document states of page elements in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="document-state-descriptions"></a><span data-ttu-id="df0f4-105">ドキュメントの状態の説明</span><span class="sxs-lookup"><span data-stu-id="df0f4-105">Document state descriptions</span></span>

<span data-ttu-id="df0f4-106">[ページ要素](page-elements-overview.md)のトピックでは、コンテンツ管理システム (CMS) 内のさまざまなドキュメント タイプを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-106">The [Page elements](page-elements-overview.md) topic lists various documents types in the content management system (CMS).</span></span> <span data-ttu-id="df0f4-107">これらのドキュメント タイプは、オーサリング ツールで複数の状態を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-107">These document types can have several states in the authoring tool.</span></span> <span data-ttu-id="df0f4-108">ドキュメントの状態によって、データの競合を防ぎ、バージョン管理を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-108">The document states help prevent data conflicts and enforce version control.</span></span> <span data-ttu-id="df0f4-109">これらは、ドキュメントを変更できるユーザー、ドキュメントを変更できる場合、および他のユーザーが変更を表示できる場合を決定します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-109">They determine who can change the documents, when the documents can be changed, and when changes can be viewed by other people.</span></span>

<span data-ttu-id="df0f4-110">次の表は、コマースのページ要素の可能なドキュメント状態を示しています。</span><span class="sxs-lookup"><span data-stu-id="df0f4-110">The following table shows the possible document states of page elements in Commerce.</span></span>

| <span data-ttu-id="df0f4-111">ドキュメントの状態</span><span class="sxs-lookup"><span data-stu-id="df0f4-111">Document state</span></span>      | <span data-ttu-id="df0f4-112">サイト ビルダー アクション</span><span class="sxs-lookup"><span data-stu-id="df0f4-112">Site builder action</span></span>        | <span data-ttu-id="df0f4-113">説明</span><span class="sxs-lookup"><span data-stu-id="df0f4-113">Description</span></span>                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="df0f4-114">チェックアウト済み</span><span class="sxs-lookup"><span data-stu-id="df0f4-114">Checked out</span></span>         | <span data-ttu-id="df0f4-115">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-115">Select **Edit**.</span></span>           | <span data-ttu-id="df0f4-116">該当するドキュメントが、チェックアウトされています。</span><span class="sxs-lookup"><span data-stu-id="df0f4-116">The applicable document is checked out to you.</span></span> <span data-ttu-id="df0f4-117">ドキュメントがこの状態の間は、他の認証されたシステム ユーザーがドキュメントを変更することはできず、ドキュメントに加えた変更は自分だけに表示されます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-117">While a document is in this state, it can't be changed by other authenticated system users, and any changes that you make to the document are visible only to you.</span></span> |
| <span data-ttu-id="df0f4-118">保存されました</span><span class="sxs-lookup"><span data-stu-id="df0f4-118">Saved</span></span>               | <span data-ttu-id="df0f4-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-119">Select **Save**.</span></span>           | <span data-ttu-id="df0f4-120">チェックアウトしたドキュメントに対して行われた変更はデータベースに保存されますが、ドキュメントはまだチェックインまたは公開されていません。</span><span class="sxs-lookup"><span data-stu-id="df0f4-120">Changes that have been made to a checked-out document are saved to the database, but the document isn't yet checked in or published.</span></span> <span data-ttu-id="df0f4-121">保存された変更は、作成者が **編集完了** を選択するまで、他の認証済みシステム ユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="df0f4-121">The saved changes aren't visible to other authenticated system users until the author selects **Finish editing**.</span></span> <span data-ttu-id="df0f4-122">品目が公開されるまで、外部ユーザーには表示されません。</span><span class="sxs-lookup"><span data-stu-id="df0f4-122">They aren't visible to external users until the item is published.</span></span> |
| <span data-ttu-id="df0f4-123">破棄済チェックアウト</span><span class="sxs-lookup"><span data-stu-id="df0f4-123">Discarded check out</span></span> | <span data-ttu-id="df0f4-124">**編集の破棄** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-124">Select **Discard edits**.</span></span>  | <span data-ttu-id="df0f4-125">チェックアウトしたドキュメントへのすべての変更が破棄され、品目はチェックインされた最後のバージョンに戻ります。</span><span class="sxs-lookup"><span data-stu-id="df0f4-125">All changes to the checked-out document are discarded, and the item reverts to the last version that was checked in.</span></span> |
| <span data-ttu-id="df0f4-126">チェックインされました</span><span class="sxs-lookup"><span data-stu-id="df0f4-126">Checked in</span></span>          | <span data-ttu-id="df0f4-127">**編集完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-127">Select **Finish editing**.</span></span> | <span data-ttu-id="df0f4-128">編集したドキュメントがチェックインされます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-128">The edited document is checked in.</span></span> <span data-ttu-id="df0f4-129">すべての変更は、他の認証済みシステム ユーザーに表示され、それらのユーザーはドキュメントを編集できます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-129">All changes are visible to other authenticated system users, and those users can then edit the document.</span></span> <span data-ttu-id="df0f4-130">各チェックインでは、品目の履歴にドキュメント バージョンのレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-130">Each check-in creates a document version record in the item's history.</span></span> |
| <span data-ttu-id="df0f4-131">公開済</span><span class="sxs-lookup"><span data-stu-id="df0f4-131">Published</span></span>           | <span data-ttu-id="df0f4-132">**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="df0f4-132">Select **Publish**.</span></span>        | <span data-ttu-id="df0f4-133">ドキュメントが発行され、変更が実際のサイトにプッシュされ、外部ユーザーによって検出可能になります。</span><span class="sxs-lookup"><span data-stu-id="df0f4-133">The document is published, and the changes are pushed to your live site and become discoverable by external users.</span></span> <span data-ttu-id="df0f4-134">**編集完了** を選択して、最初にチェックインした場合にのみ、アイテムを発行できます。</span><span class="sxs-lookup"><span data-stu-id="df0f4-134">Items can be published only if they have first been checked in by selecting **Finish editing**.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="df0f4-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="df0f4-135">Additional resources</span></span>

[<span data-ttu-id="df0f4-136">コンテンツを追加する方法</span><span class="sxs-lookup"><span data-stu-id="df0f4-136">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="df0f4-137">ページ モデルの用語集</span><span class="sxs-lookup"><span data-stu-id="df0f4-137">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="df0f4-138">公開グループの作業</span><span class="sxs-lookup"><span data-stu-id="df0f4-138">Work with publish groups</span></span>](publish-groups.md)

[<span data-ttu-id="df0f4-139">クロスチャネル共有の有効化と使用</span><span class="sxs-lookup"><span data-stu-id="df0f4-139">Enable and use cross-channel sharing</span></span>](cross-channel-sharing.md)

[<span data-ttu-id="df0f4-140">モジュールで動作</span><span class="sxs-lookup"><span data-stu-id="df0f4-140">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="df0f4-141">フラグメントで動作</span><span class="sxs-lookup"><span data-stu-id="df0f4-141">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="df0f4-142">テンプレートとレイアウトの概要</span><span class="sxs-lookup"><span data-stu-id="df0f4-142">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="df0f4-143">サイト ナビゲーションのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="df0f4-143">Customize site navigation</span></span>](customize-site-navigation.md)

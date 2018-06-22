---
title: "フォーム キャプションの変更"
description: "このトピックでは、ユーザーが Web ブラウザーで現在のページを識別するためのフォーム キャプションを変更する方法について説明します。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 917fb767d2f865c51849928bb51b1debf56d23d0
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="change-the-caption-on-a-form"></a><span data-ttu-id="49216-103">フォームのキャプションの変更</span><span class="sxs-lookup"><span data-stu-id="49216-103">Change the caption on a form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49216-104">フォームのキャプションは、Web ブラウザーのアドレス バーの横にあるページ タブに表示され、ユーザーが現在開いているページを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="49216-104">The form caption appears in the page tab next to the web browser's Address bar and helps the user identify the page that is currently open.</span></span> <span data-ttu-id="49216-105">メタデータでは、フォームのキャプションはフォームのデザインのプロパティで表されます。</span><span class="sxs-lookup"><span data-stu-id="49216-105">In metadata, the form caption is represented by a property on the form design.</span></span> <span data-ttu-id="49216-106">したがって、キャプションを変更するには、フォーム デザインの **Caption** プロパティを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49216-106">Therefore, to change the caption, you must modify the **Caption** property on the form design.</span></span> <span data-ttu-id="49216-107">拡張機能によってこの変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="49216-107">You can make this change through extension.</span></span> <span data-ttu-id="49216-108">拡張モデルで選択したフォームの拡張子を作成し、通常どおり**キャプション** プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="49216-108">Create an extension of the selected form in the extension model, and then change the **Caption** property as usual.</span></span>

![キャプション プロパティの変更](media/ChangeCaption01.jpg)

<span data-ttu-id="49216-110">次の図は、ブラウザーでのフォーム キャプションの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="49216-110">The following illustration shows what the form caption looks like in a browser.</span></span>

![ブラウザーでのフォーム キャプション](media/ChangeCaption02.jpg)

> [!NOTE]
> <span data-ttu-id="49216-112">フォームのデザインの他のプロパティはいずれも変更できません。</span><span class="sxs-lookup"><span data-stu-id="49216-112">None of the other properties on the form design can be changed.</span></span>


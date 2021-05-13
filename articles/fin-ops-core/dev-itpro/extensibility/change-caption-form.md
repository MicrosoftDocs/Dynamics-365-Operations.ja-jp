---
title: 拡張機能によって、フォームのキャプションを変更します。
description: このトピックでは、ユーザーが Web ブラウザーで現在のページを識別するためのフォーム キャプションを変更する方法について説明します。
author: ivanv-microsoft
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 96a7e87cd1db1a455704ecdba539c159fbda026f
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866092"
---
# <a name="change-the-captions-of-forms-through-extension"></a><span data-ttu-id="f9a49-103">拡張機能によって、フォームのキャプションを変更します。</span><span class="sxs-lookup"><span data-stu-id="f9a49-103">Change the captions of forms through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9a49-104">フォームのキャプションは、Web ブラウザーのアドレス バーの横にあるページ タブに表示され、ユーザーが現在開いているページを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f9a49-104">The form caption appears in the page tab next to the web browser's Address bar and helps the user identify the page that is currently open.</span></span> <span data-ttu-id="f9a49-105">メタデータでは、フォームのキャプションはフォームのデザインのプロパティで表されます。</span><span class="sxs-lookup"><span data-stu-id="f9a49-105">In metadata, the form caption is represented by a property on the form design.</span></span> <span data-ttu-id="f9a49-106">したがって、キャプションを変更するには、フォーム デザインの **Caption** プロパティを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9a49-106">Therefore, to change the caption, you must modify the **Caption** property on the form design.</span></span> <span data-ttu-id="f9a49-107">拡張機能によってこの変更を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f9a49-107">You can make this change through extension.</span></span> <span data-ttu-id="f9a49-108">拡張モデルで選択したフォームの拡張子を作成し、通常どおり **キャプション** プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="f9a49-108">Create an extension of the selected form in the extension model, and then change the **Caption** property as usual.</span></span>

![キャプション プロパティの変更](media/ChangeCaption01.jpg)

<span data-ttu-id="f9a49-110">次の図は、ブラウザーでのフォーム キャプションの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="f9a49-110">The following illustration shows what the form caption looks like in a browser.</span></span>

![ブラウザーでのフォーム キャプション](media/ChangeCaption02.jpg)

> [!NOTE]
> <span data-ttu-id="f9a49-112">フォームのデザインの他のプロパティはいずれも変更できません。</span><span class="sxs-lookup"><span data-stu-id="f9a49-112">None of the other properties on the form design can be changed.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: 拡張機能によって、フォームのキャプションを変更します。
description: このトピックでは、ユーザーが Web ブラウザーで現在のページを識別するためのフォーム キャプションを変更する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: fb8e9e8bf8a1389b603a7ff938ad049c04cd1ea8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369295"
---
# <a name="change-the-captions-of-forms-through-extension"></a>拡張機能によって、フォームのキャプションを変更します。

[!include [banner](../includes/banner.md)]

フォームのキャプションは、Web ブラウザーのアドレス バーの横にあるページ タブに表示され、ユーザーが現在開いているページを識別するのに役立ちます。 メタデータでは、フォームのキャプションはフォームのデザインのプロパティで表されます。 したがって、キャプションを変更するには、フォーム デザインの **Caption** プロパティを変更する必要があります。 拡張機能によってこの変更を行うことができます。 拡張モデルで選択したフォームの拡張子を作成し、通常どおり**キャプション** プロパティを変更します。

![キャプション プロパティの変更](media/ChangeCaption01.jpg)

次の図は、ブラウザーでのフォーム キャプションの外観を示しています。

![ブラウザーでのフォーム キャプション](media/ChangeCaption02.jpg)

> [!NOTE]
> フォームのデザインの他のプロパティはいずれも変更できません。

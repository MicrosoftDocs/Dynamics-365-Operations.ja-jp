---
title: アプリケーション チェッカー
description: このトピックでは、Application チェッカー ツールについて説明します。
author: AndreasHassing
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: anniels
ms.search.validFrom: 2020-09-22
ms.dyn365.ops.version: Platform update 25
ms.openlocfilehash: 8a72ccbe248e3f428e1f48d5544775e7d75bd145
ms.sourcegitcommit: ad5b7676fc1213316e478afcffbfaee7d813f3bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2020
ms.locfileid: "3885350"
---
# <a name="application-checker"></a><span data-ttu-id="89382-103">アプリケーション チェッカー</span><span class="sxs-lookup"><span data-stu-id="89382-103">Application checker</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89382-104">Application チェッカー ツールは、アプリケーション コード (ソースとメタデータの両方) を、これまではできなかった方法で把握できるようにする一連のテクノロジです。</span><span class="sxs-lookup"><span data-stu-id="89382-104">The application checker tool is a set of technologies that allow you to gain insight into your application code (both source and metadata) in ways that have not been possible before.</span></span> <span data-ttu-id="89382-105">このテクノロジは、XML のソース コードとメタデータの両方の表現に基づいており、XQuery 言語を使用してソースコードに対する宣言クエリを表すことによって、豊富な検索機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="89382-105">The technology is based on representing both source code and metadata in XML and providing rich search facilities by using the XQuery language to express declarative queries over the source code.</span></span> <span data-ttu-id="89382-106">現在の実装は、BaseX リポジトリ内で実行され、開発者のボックスでローカルに実行されます。</span><span class="sxs-lookup"><span data-stu-id="89382-106">The current implementation runs inside a BaseX repository, which runs locally on the developer's box.</span></span> 

<span data-ttu-id="89382-107">アプリケーション チェッカーをインストールして使用する方法については、[Dynamics365FO-AppChecker](https://github.com/microsoft/Dynamics365FO-AppChecker) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89382-107">For information about how to install and use the application checker, see [Dynamics365FO-AppChecker](https://github.com/microsoft/Dynamics365FO-AppChecker).</span></span>


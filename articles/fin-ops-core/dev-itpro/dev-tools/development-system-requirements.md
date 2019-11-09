---
title: 開発システム要件
description: このトピックでは、開発のシステム要件を一覧表示します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 33221
ms.assetid: f39dbe39-7dc3-463c-923e-f22af231b979
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60dc9d97d6d474d994be245d518820db5efeeae7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191691"
---
# <a name="development-system-requirements"></a><span data-ttu-id="b1ada-103">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="b1ada-103">Development system requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1ada-104">このトピックでは、開発のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="b1ada-104">This topic lists the system requirements for development.</span></span>

<span data-ttu-id="b1ada-105">開発環境は、ローカルまたは Microsoft Azure でホストできます。</span><span class="sxs-lookup"><span data-stu-id="b1ada-105">Development environments can be hosted locally or in Microsoft Azure.</span></span> <span data-ttu-id="b1ada-106">ビルド プロセス、X++ コンパイル、および相互参照情報の生成は、通常、16 GB のメモリと 2 つの CPU コアを搭載したマシンでは十分に動作します。</span><span class="sxs-lookup"><span data-stu-id="b1ada-106">The build process, X++ compilation and generation of cross reference information, will typically run satisfactorily on machines with 16 GB of memory and 2 CPU cores.</span></span> <span data-ttu-id="b1ada-107">ただし、コンパイラではリソースが使用されるため、特に同時実行されているその他のプロセスからのリソースの競合がある場合、より多くの RAM とコアが高速のコンパイルに変換される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b1ada-107">However, the compiler will use available resources, so more RAM and more cores may translate into faster compilations, especially if there is contention for the resources from other processes running concurrently.</span></span> <span data-ttu-id="b1ada-108">このような場合、4 コアで 24 GB のメモリをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b1ada-108">In such cases, we recommend 24 GB of memory with 4 cores.</span></span> <span data-ttu-id="b1ada-109">開発環境には AOS Web アプリケーション、Visual Studio、Management Reporter、および SQL Server など同時に実行される可能性がある多数のコンポーネントが含まれているため、少なくとも、 2 つの CPU コアを推奨します。</span><span class="sxs-lookup"><span data-stu-id="b1ada-109">At a minimum, 2 CPU cores are recommended because the developer environment contains many components that may be running concurrently, including the AOS web application, Visual Studio, Management Reporter, and SQL Server.</span></span>



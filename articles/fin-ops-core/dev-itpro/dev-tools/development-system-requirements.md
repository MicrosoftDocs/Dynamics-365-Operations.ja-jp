---
title: 開発システム要件
description: このトピックでは、開発のシステム要件を一覧表示します。
author: RobinARH
ms.date: 06/20/2017
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 33221
ms.assetid: f39dbe39-7dc3-463c-923e-f22af231b979
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b507900f9eb8d11d4dec1b79ed16b202ef9129f
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866350"
---
# <a name="development-system-requirements"></a><span data-ttu-id="a59b5-103">開発システム要件</span><span class="sxs-lookup"><span data-stu-id="a59b5-103">Development system requirements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a59b5-104">このトピックでは、開発のシステム要件を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="a59b5-104">This topic lists the system requirements for development.</span></span>

<span data-ttu-id="a59b5-105">開発環境は、ローカルまたは Microsoft Azure でホストできます。</span><span class="sxs-lookup"><span data-stu-id="a59b5-105">Development environments can be hosted locally or in Microsoft Azure.</span></span> <span data-ttu-id="a59b5-106">ビルド プロセス、X++ コンパイル、および相互参照情報の生成は、通常、16 GB のメモリと 2 つの CPU コアを搭載したマシンで十分に動作します。</span><span class="sxs-lookup"><span data-stu-id="a59b5-106">The build process, X++ compilation, and generation of cross reference information, typically run satisfactorily on machines with 16 GB of memory and two CPU cores.</span></span> <span data-ttu-id="a59b5-107">コンパイラではリソースを使用するため、特に同時プロセスからのリソースの競合がある場合、より多くの RAM とコアがコンパイルを高速化することができます。</span><span class="sxs-lookup"><span data-stu-id="a59b5-107">The compiler uses available resources, so more RAM and more cores can speed up compilation, especially if there is contention for the resources from other concurrent processes.</span></span> <span data-ttu-id="a59b5-108">同時プロセスを実行している場合は、4 つのコアで 24 GBのメモリをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a59b5-108">If you are running concurrent processes, then we recommend 24 GB of memory with four cores.</span></span> <span data-ttu-id="a59b5-109">同時に実行される可能性のあるコンポーネントが開発環境に多数含まれているので、少なくとも 2 つの CPU コアをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a59b5-109">At a minimum, two CPU cores are recommended because the developer environment contains many components that may be running concurrently.</span></span> <span data-ttu-id="a59b5-110">コンポーネントには、AOS Web アプリケーション、Visual Studio、Management Reporter および SQL Server が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a59b5-110">The components include the AOS web application, Visual Studio, Management Reporter, and SQL Server.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
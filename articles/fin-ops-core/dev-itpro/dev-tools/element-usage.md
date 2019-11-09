---
title: 要素の使用方法を決定するためのコマンド
description: この記事では、アプリケーションでの要素の使用方法を決定するために、Microsoft Visual studio ツールに追加されたコマンドについて説明します。
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
ms.custom: 4984
ms.assetid: e9590e78-6aae-4c3a-b50b-786351cfc0ff
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d762651e5f876674533d79ea602cfedbf001f142
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191687"
---
# <a name="commands-for-determining-how-elements-are-used"></a><span data-ttu-id="8fd9a-103">要素の使用方法を決定するためのコマンド</span><span class="sxs-lookup"><span data-stu-id="8fd9a-103">Commands for determining how elements are used</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fd9a-104">この記事では、アプリケーションでの要素の使用方法を決定するために、Microsoft Visual studio ツールに追加されたコマンドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-104">This article reviews the commands that have been added to the Microsoft Visual studio Tools to help you determine how elements are used in an application.</span></span> 

<span data-ttu-id="8fd9a-105">一般的なアプリケーションでは要素数が多いため、Microsoft Visual Studio Tools にコマンドが追加され、要素の使用方法を簡単に判断できます。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-105">Because of the large number of elements in a typical application, commands have been added to the Microsoft Visual Studio Tools to make it easier to determine how an element is used.</span></span>

## <a name="finding-where-elements-are-used"></a><span data-ttu-id="8fd9a-106">要素が使用されている場所を検索</span><span class="sxs-lookup"><span data-stu-id="8fd9a-106">Finding where elements are used</span></span>

<span data-ttu-id="8fd9a-107">ビルド操作中に、要素の使用方法を示すために使用できる相互参照情報が生成されます。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-107">During build operations, cross-reference information is generated that can be used to show how elements are used.</span></span> <span data-ttu-id="8fd9a-108">要素を右クリックしてから **参照の検索** をクリックし、要素が使用される場所の一覧を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-108">You can right-click an element and then click **Find References** to display a list of the locations where that element is used.</span></span> <span data-ttu-id="8fd9a-109">リスト内の品目のいずれかをクリックすると、要素のデザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-109">When you click one of the items in the list, the designer for the element opens.</span></span> <span data-ttu-id="8fd9a-110">[![23\_DevoToolsConcept](./media/23_devotoolsconcept.png)](./media/23_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="8fd9a-110">[![23\_DevoToolsConcept](./media/23_devotoolsconcept.png)](./media/23_devotoolsconcept.png)</span></span>

## <a name="viewing-a-reference-diagram"></a><span data-ttu-id="8fd9a-111">参照ダイアグラムの表示</span><span class="sxs-lookup"><span data-stu-id="8fd9a-111">Viewing a reference diagram</span></span>

<span data-ttu-id="8fd9a-112">テーブルなどの上位レベルの要素を右クリックすると、**参照の表示**コマンドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-112">When you right-click some higher-level elements, such as tables, the **View Reference** command is available.</span></span> <span data-ttu-id="8fd9a-113">このコマンドは、現在の要素に関連する要素を示すグラフィックを作成します。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-113">This command produces a graphic that shows the elements that are related to the current element.</span></span> <span data-ttu-id="8fd9a-114">グラフィック内の項目を右クリックしてから **定義に移動** をクリックし、これらの要素に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="8fd9a-114">You can right-click the items in the graphic and then click **Go To Definition** to navigate to those elements.</span></span> <span data-ttu-id="8fd9a-115">[![24\_DevoToolsConcept](./media/24_devotoolsconcept.png)](./media/24_devotoolsconcept.png)</span><span class="sxs-lookup"><span data-stu-id="8fd9a-115">[![24\_DevoToolsConcept](./media/24_devotoolsconcept.png)](./media/24_devotoolsconcept.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8fd9a-116">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="8fd9a-116">Additional resources</span></span>

[<span data-ttu-id="8fd9a-117">開発ツールの概要</span><span class="sxs-lookup"><span data-stu-id="8fd9a-117">Development tools overview</span></span>](development-tools-overview.md)

[<span data-ttu-id="8fd9a-118">要素デザイナー</span><span class="sxs-lookup"><span data-stu-id="8fd9a-118">Element designers</span></span>](element-designers.md)



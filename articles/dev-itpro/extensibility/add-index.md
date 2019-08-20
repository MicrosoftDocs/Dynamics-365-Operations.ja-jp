---
title: 拡張機能を使用してテーブルにインデックスを追加
description: このトピックでは、テーブルにインデックスを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 01d8f3c7ff1b8bcc666d1e85f16c2bb4ad535d48
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794866"
---
# <a name="add-indexes-to-tables-through-extension"></a><span data-ttu-id="61ed7-103">拡張機能を使用してテーブルにインデックスを追加</span><span class="sxs-lookup"><span data-stu-id="61ed7-103">Add indexes to tables through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61ed7-104">多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="61ed7-104">Often, you extend tables so that you can store additional data for later but also quickly access the data that is based on the new fields.</span></span> <span data-ttu-id="61ed7-105">したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。</span><span class="sxs-lookup"><span data-stu-id="61ed7-105">Therefore, it's often beneficial to have a dedicated index that speeds up the database search.</span></span> <span data-ttu-id="61ed7-106">拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="61ed7-106">You can add a new index to an existing table through extension.</span></span> <span data-ttu-id="61ed7-107">既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="61ed7-107">To add an index to an existing table, you extend the selected table and then create an index just as you would create an index on a new table.</span></span> <span data-ttu-id="61ed7-108">新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="61ed7-108">You can add both new and existing fields so that they are part of the new index.</span></span>

<span data-ttu-id="61ed7-109">次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。</span><span class="sxs-lookup"><span data-stu-id="61ed7-109">In the following illustration, an InventTable extension is used to define an index for a new field on the InventTable table.</span></span>

![新しいインデックス](media/AddIndex.jpg) 

> [!WARNING]
> <span data-ttu-id="61ed7-111">固有のインデックスを作成するのに、この手法は用いないでください。</span><span class="sxs-lookup"><span data-stu-id="61ed7-111">You should not use this approach to create unique indexes.</span></span> <span data-ttu-id="61ed7-112">この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。</span><span class="sxs-lookup"><span data-stu-id="61ed7-112">This change is an intrusive change that might break the solutions of other independent software vendors (ISVs) if those solutions are deployed in the same environment.</span></span> <span data-ttu-id="61ed7-113">この機能は、将来のプラットフォーム リリースでは削除されます。</span><span class="sxs-lookup"><span data-stu-id="61ed7-113">This capability will be removed in future platform releases.</span></span>

## <a name="extend-standard-indexes"></a><span data-ttu-id="61ed7-114">標準インデックスの拡張</span><span class="sxs-lookup"><span data-stu-id="61ed7-114">Extend standard indexes</span></span>

<span data-ttu-id="61ed7-115">標準インデックスを拡張して追加の (含まれる) 列を追加できますが、これにはいくつか条件があります:</span><span class="sxs-lookup"><span data-stu-id="61ed7-115">You can extend standard indexes and add additional (included) columns but there are some conditions:</span></span>

+   <span data-ttu-id="61ed7-116">インデックスが非クラスター化されています。</span><span class="sxs-lookup"><span data-stu-id="61ed7-116">The index is non-clustered.</span></span>
+   <span data-ttu-id="61ed7-117">インデックスが一意ではありません。</span><span class="sxs-lookup"><span data-stu-id="61ed7-117">The index is not unique.</span></span>

<span data-ttu-id="61ed7-118">標準インデックスの拡張には、次の制約が適用されます:</span><span class="sxs-lookup"><span data-stu-id="61ed7-118">The following constraints apply to extending a standard index:</span></span>

+   <span data-ttu-id="61ed7-119">既存の列を削除できません。</span><span class="sxs-lookup"><span data-stu-id="61ed7-119">You cannot delete existing columns.</span></span>
+ <span data-ttu-id="61ed7-120">既存の列の順序を変更できません。</span><span class="sxs-lookup"><span data-stu-id="61ed7-120">You cannot change the order of the existing columns.</span></span>
+   <span data-ttu-id="61ed7-121">標準インデックスを無効化できません。</span><span class="sxs-lookup"><span data-stu-id="61ed7-121">You cannot disable standard indexes.</span></span>

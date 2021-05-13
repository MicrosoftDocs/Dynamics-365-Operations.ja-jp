---
title: 拡張機能を使用してテーブルにインデックスを追加
description: このトピックでは、テーブルにインデックスを追加する方法について説明します。
author: ivanv-microsoft
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 36f7f0d61cccd13e16d6e2b98581427930f40aa8
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865849"
---
# <a name="add-indexes-to-tables-through-extension"></a><span data-ttu-id="179ea-103">拡張機能を使用してテーブルにインデックスを追加</span><span class="sxs-lookup"><span data-stu-id="179ea-103">Add indexes to tables through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="179ea-104">多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="179ea-104">Often, you extend tables so that you can store additional data for later but also quickly access the data that is based on the new fields.</span></span> <span data-ttu-id="179ea-105">したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。</span><span class="sxs-lookup"><span data-stu-id="179ea-105">Therefore, it's often beneficial to have a dedicated index that speeds up the database search.</span></span> <span data-ttu-id="179ea-106">拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="179ea-106">You can add a new index to an existing table through extension.</span></span> <span data-ttu-id="179ea-107">既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="179ea-107">To add an index to an existing table, you extend the selected table and then create an index just as you would create an index on a new table.</span></span> <span data-ttu-id="179ea-108">新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="179ea-108">You can add both new and existing fields so that they are part of the new index.</span></span>

<span data-ttu-id="179ea-109">次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。</span><span class="sxs-lookup"><span data-stu-id="179ea-109">In the following illustration, an InventTable extension is used to define an index for a new field on the InventTable table.</span></span>

![新しいインデックス](media/AddIndex.jpg) 

> [!WARNING]
> <span data-ttu-id="179ea-111">固有のインデックスを作成するのに、この手法は用いないでください。</span><span class="sxs-lookup"><span data-stu-id="179ea-111">You should not use this approach to create unique indexes.</span></span> <span data-ttu-id="179ea-112">この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。</span><span class="sxs-lookup"><span data-stu-id="179ea-112">This change is an intrusive change that might break the solutions of other independent software vendors (ISVs) if those solutions are deployed in the same environment.</span></span> <span data-ttu-id="179ea-113">この機能は、将来のプラットフォーム リリースでは削除されます。</span><span class="sxs-lookup"><span data-stu-id="179ea-113">This capability will be removed in future platform releases.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
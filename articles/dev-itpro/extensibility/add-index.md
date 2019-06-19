---
title: 拡張機能を使用してテーブルにインデックスを追加
description: このトピックでは、テーブルにインデックスを追加する方法について説明します。
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
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 3dab4107711edd95859b694c22085d4464811914
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550919"
---
# <a name="add-indexes-to-tables-through-extension"></a><span data-ttu-id="38cc3-103">拡張機能を使用してテーブルにインデックスを追加</span><span class="sxs-lookup"><span data-stu-id="38cc3-103">Add indexes to tables through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38cc3-104">多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="38cc3-104">Often, you extend tables so that you can store additional data for later but also quickly access the data that is based on the new fields.</span></span> <span data-ttu-id="38cc3-105">したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。</span><span class="sxs-lookup"><span data-stu-id="38cc3-105">Therefore, it's often beneficial to have a dedicated index that speeds up the database search.</span></span> <span data-ttu-id="38cc3-106">拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="38cc3-106">You can add a new index to an existing table through extension.</span></span> <span data-ttu-id="38cc3-107">既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。</span><span class="sxs-lookup"><span data-stu-id="38cc3-107">To add an index to an existing table, you extend the selected table and then create an index just as you would create an index on a new table.</span></span> <span data-ttu-id="38cc3-108">新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="38cc3-108">You can add both new and existing fields so that they are part of the new index.</span></span>

> [!NOTE]
> <span data-ttu-id="38cc3-109">新しいインデックスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="38cc3-109">You can create new indexes.</span></span> <span data-ttu-id="38cc3-110">ただし、既存のインデックスを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="38cc3-110">However, you can't modify existing indexes.</span></span>

<span data-ttu-id="38cc3-111">次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。</span><span class="sxs-lookup"><span data-stu-id="38cc3-111">In the following illustration, an InventTable extension is used to define an index for a new field on the InventTable table.</span></span>

![新しいインデックス](media/AddIndex.jpg) 

> [!WARNING]
> <span data-ttu-id="38cc3-113">固有のインデックスを作成するのに、この手法は用いないでください。</span><span class="sxs-lookup"><span data-stu-id="38cc3-113">You should not use this approach to create unique indexes.</span></span> <span data-ttu-id="38cc3-114">この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。</span><span class="sxs-lookup"><span data-stu-id="38cc3-114">This change is an intrusive change that might break the solutions of other independent software vendors (ISVs) if those solutions are deployed in the same environment.</span></span> <span data-ttu-id="38cc3-115">この機能は、将来のプラットフォーム リリースでは削除されます。</span><span class="sxs-lookup"><span data-stu-id="38cc3-115">This capability will be removed in future platform releases.</span></span>

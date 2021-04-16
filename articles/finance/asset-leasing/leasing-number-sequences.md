---
title: 番号順序の割り当て
description: このトピックでは、リース ID の番号順序を作成する方法について説明します。 また、インデックスの再評価プロセスで使用される固有 ID の作成方法についても説明します。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0b5d622df1e5dcdf7f1322328bce7e185f8edb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819821"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="d1c30-104">番号順序の割り当て</span><span class="sxs-lookup"><span data-stu-id="d1c30-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d1c30-105">このトピックでは、リース ID の番号順序を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="d1c30-106">また、インデックスの再評価プロセスで使用される固有 ID の作成方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="d1c30-107">**資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="d1c30-108">**番号順序** サイド タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="d1c30-109">サイド バーの **番号順序** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="d1c30-110">**リース ID** 照会の番号順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="d1c30-111">この番号順序は、各リースの固有識別子を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1c30-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="d1c30-112">**プロセス ID** 照会の番号順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="d1c30-113">この番号順序は、各インデックス 再評価プロセスの固有識別子を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1c30-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="d1c30-114">**終了提案 ID** の照会に使用する番号順序を選択します。</span><span class="sxs-lookup"><span data-stu-id="d1c30-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="d1c30-115">この番号順序は、終了の提案で使用する固有識別子を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d1c30-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
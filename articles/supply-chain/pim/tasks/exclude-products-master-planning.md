---
title: マスター プランから製品を除外する場合は、製品ライフサイクルの状態を作成
description: この手順では、マスター プランおよび BOM レベルの計算から製品を除外する新製品ライフサイクルの状態を作成する方法を示します。
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818040"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="b5cb9-103">マスター プランから製品を除外する場合は、製品ライフサイクルの状態を作成</span><span class="sxs-lookup"><span data-stu-id="b5cb9-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5cb9-104">この手順では、マスター プランおよび BOM レベルの計算から製品を除外する新製品ライフサイクルの状態を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="b5cb9-105">古い形式の状態を作成します</span><span class="sxs-lookup"><span data-stu-id="b5cb9-105">Create an obsolete state</span></span>
1. <span data-ttu-id="b5cb9-106">[製品情報管理] > [設定] > [製品ライフサイクルの状態] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="b5cb9-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-107">Click New.</span></span>
3. <span data-ttu-id="b5cb9-108">[状態] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="b5cb9-109">[計画に対して有効] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="b5cb9-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="b5cb9-111">リリース済製品に古い形式の状態を関連付ける</span><span class="sxs-lookup"><span data-stu-id="b5cb9-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="b5cb9-112">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-112">Close the page.</span></span>
2. <span data-ttu-id="b5cb9-113">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="b5cb9-114">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b5cb9-115">たとえば、「M00」という値を含む [検索名] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="b5cb9-116">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-116">Click Edit.</span></span>
5. <span data-ttu-id="b5cb9-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b5cb9-118">[製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b5cb9-118">In the Product lifecycle state field, enter or select a value.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
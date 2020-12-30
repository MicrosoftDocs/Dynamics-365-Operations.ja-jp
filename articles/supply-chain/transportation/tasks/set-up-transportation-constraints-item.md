---
title: 品目の配送制約の設定
description: この手順では、選択した品目が選択したハブを通じて配送されないよう配送制約を設定します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f351da832f8fa62935d09c6ce6ede277971dbbbc
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431747"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="65a80-103">品目の配送制約の設定</span><span class="sxs-lookup"><span data-stu-id="65a80-103">Set up transportation constraints for an item</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65a80-104">この手順では、選択した品目が選択したハブを通じて配送されないよう配送制約を設定します。</span><span class="sxs-lookup"><span data-stu-id="65a80-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="65a80-105">通常、このタスクを実施するのは、配送コーディネーターです。</span><span class="sxs-lookup"><span data-stu-id="65a80-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="65a80-106">デモ データ会社 USMF でこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="65a80-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="65a80-107">品目制約の作成</span><span class="sxs-lookup"><span data-stu-id="65a80-107">Create an item constaint</span></span>
1. <span data-ttu-id="65a80-108">[制約] に移動します。</span><span class="sxs-lookup"><span data-stu-id="65a80-108">Go to Constraints.</span></span>
2. <span data-ttu-id="65a80-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65a80-109">Click New.</span></span>
3. <span data-ttu-id="65a80-110">[品目の制約] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="65a80-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="65a80-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="65a80-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="65a80-112">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="65a80-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="65a80-113">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="65a80-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="65a80-114">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="65a80-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="65a80-115">[ハブ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="65a80-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="65a80-116">[制約アクション] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65a80-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="65a80-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65a80-117">Click Save.</span></span>
11. <span data-ttu-id="65a80-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65a80-118">Close the page.</span></span>


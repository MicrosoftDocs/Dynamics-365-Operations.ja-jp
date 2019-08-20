---
title: 品目の配送制約の設定
description: この手順では、選択した品目が選択したハブを通じて配送されないよう配送制約を設定します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSConstraint, InventLocationIdLookup, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f686b29151cfbbeeffbf1f8fb98ea6ce5bc51d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836072"
---
# <a name="set-up-transportation-constraints-for-an-item"></a><span data-ttu-id="4160b-103">品目の配送制約の設定</span><span class="sxs-lookup"><span data-stu-id="4160b-103">Set up transportation constraints for an item</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4160b-104">この手順では、選択した品目が選択したハブを通じて配送されないよう配送制約を設定します。</span><span class="sxs-lookup"><span data-stu-id="4160b-104">This procedure will set up a transportation constraint to prevent a selected item from being transported through a selected hub.</span></span> <span data-ttu-id="4160b-105">通常、このタスクを実施するのは、配送コーディネーターです。</span><span class="sxs-lookup"><span data-stu-id="4160b-105">This task would typically be carried out by a Transportation coordinator.</span></span> <span data-ttu-id="4160b-106">デモ データ会社 USMF でこの手順を使うか、または独自のデータを使うことができます。</span><span class="sxs-lookup"><span data-stu-id="4160b-106">You can use this procedure in the USMF demo data company or on your own data.</span></span>


## <a name="create-an-item-constaint"></a><span data-ttu-id="4160b-107">品目制約の作成</span><span class="sxs-lookup"><span data-stu-id="4160b-107">Create an item constaint</span></span>
1. <span data-ttu-id="4160b-108">[制約] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4160b-108">Go to Constraints.</span></span>
2. <span data-ttu-id="4160b-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4160b-109">Click New.</span></span>
3. <span data-ttu-id="4160b-110">[品目の制約] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4160b-110">In the Item constraint field, type a value.</span></span>
4. <span data-ttu-id="4160b-111">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4160b-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="4160b-112">[サイト] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4160b-112">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="4160b-113">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4160b-113">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="4160b-114">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4160b-114">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="4160b-115">[ハブ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4160b-115">In the Hub field, enter or select a value.</span></span>
9. <span data-ttu-id="4160b-116">[制約アクション] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4160b-116">In the Constraint action field, select an option.</span></span>
10. <span data-ttu-id="4160b-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4160b-117">Click Save.</span></span>
11. <span data-ttu-id="4160b-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4160b-118">Close the page.</span></span>


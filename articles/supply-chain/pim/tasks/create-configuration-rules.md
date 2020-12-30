---
title: コンフィギュレーション ルールの作成
description: この手順は、分析コード ベースのコンフィギュレーションを使用して BOM 明細行の特定の組み合わせを使用または禁止できるコンフィギュレーション ルールを作成します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bc0af4d95e9430d0b5c8b7fc9a4ade076802044
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431967"
---
# <a name="create-configuration-rules"></a><span data-ttu-id="f580e-103">コンフィギュレーション ルールの作成</span><span class="sxs-lookup"><span data-stu-id="f580e-103">Create configuration rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f580e-104">この手順は、分析コード ベースのコンフィギュレーションを使用して BOM 明細行の特定の組み合わせを使用または禁止できるコンフィギュレーション ルールを作成します。</span><span class="sxs-lookup"><span data-stu-id="f580e-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="f580e-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="f580e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f580e-106">これは、分析コード ベースのコンフィギュレーションでの組み合わせの作成方法を説明する 8 つの手順の 7 番目です。</span><span class="sxs-lookup"><span data-stu-id="f580e-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="f580e-107">[製品情報管理] > [部品表およびフォーミュラ] > [部品表] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f580e-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="f580e-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f580e-109">[分析コードベースのコンフィギュレーションの BOM] を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="f580e-110">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="f580e-111">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-111">Click Change view.</span></span>
5. <span data-ttu-id="f580e-112">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-112">Click Header view.</span></span>
    * <span data-ttu-id="f580e-113">[コンフィギュレーション ルート] クイック タブにアクセスするヘッダー表示を開きます。</span><span class="sxs-lookup"><span data-stu-id="f580e-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="f580e-114">[コンフィギュレーション ルート] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="f580e-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="f580e-115">[コンフィギュレーション ルート] クイック タブを展開モードにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f580e-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="f580e-116">[コンフィギュレーション ルール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="f580e-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-117">Click New.</span></span>
9. <span data-ttu-id="f580e-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f580e-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="f580e-119">[品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f580e-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f580e-120">現在のコンフィギュレーション グループの品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f580e-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="f580e-121">ルールの条件を表す 1 つを選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="f580e-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f580e-123">[方法] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="f580e-124">別のコンフィギュレーション グループの品目の選択または選択解除を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="f580e-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="f580e-125">[派生グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f580e-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f580e-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f580e-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f580e-128">目的のコンフィギュレーション グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="f580e-129">[派生品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="f580e-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="f580e-130">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f580e-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f580e-131">選択された方法によって選択または選択解除となる品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="f580e-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="f580e-132">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f580e-132">Close the page.</span></span>


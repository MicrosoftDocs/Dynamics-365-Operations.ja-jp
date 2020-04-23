---
title: コンフィギュレーション ルートの定義
description: この手順では、コンフィギュレーション グループの表示順序を決定するコンフィギュレーション ルートの定義を対象としています。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49535f241c6fcca79df64ee18616ba581b5ca941
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203667"
---
# <a name="define-configuration-route"></a><span data-ttu-id="8e2c4-103">コンフィギュレーション ルートの定義</span><span class="sxs-lookup"><span data-stu-id="8e2c4-103">Define configuration route</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8e2c4-104">この手順では、コンフィギュレーション グループの表示順序を決定するコンフィギュレーション ルートの定義を対象としています。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-104">This procedure focuses on defining a configuration route that determines the sequence in which the configuration groups will be presented.</span></span> <span data-ttu-id="8e2c4-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8e2c4-106">これは、分析コード ベースのコンフィギュレーションでの組み合わせの作成方法を説明する 8 つの手順の 6 番目です。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-106">This is the sixth procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="8e2c4-107">[製品情報管理] > [部品表およびフォーミュラ] > [部品表] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="8e2c4-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8e2c4-109">[アクション] ウィンドウで、[オプション] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-109">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="8e2c4-110">[ビューの変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-110">Click Change view.</span></span>
5. <span data-ttu-id="8e2c4-111">[ヘッダーの表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-111">Click Header view.</span></span>
6. <span data-ttu-id="8e2c4-112">[コンフィギュレーション ルート] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-112">Expand or collapse the Configuration route section.</span></span>
7. <span data-ttu-id="8e2c4-113">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-113">Click Add.</span></span>
8. <span data-ttu-id="8e2c4-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8e2c4-115">[コンフィギュレーション グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-115">In the Configuration group field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="8e2c4-116">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-116">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="8e2c4-117">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-117">Click Add.</span></span>
12. <span data-ttu-id="8e2c4-118">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-118">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8e2c4-119">[コンフィギュレーション グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-119">In the Configuration group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="8e2c4-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-120">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8e2c4-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-121">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8e2c4-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8e2c4-122">Click Save.</span></span>


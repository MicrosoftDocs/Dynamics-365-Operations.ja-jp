---
title: POS レジスターの財務分析コードの作成とレジスターの分析コード値のコンフィギュレーション
description: この手順では、販売時点管理 (POS) レジスターの財務分析コードの作成について説明し、レジスターの財務分析コード値をコンフィギュレーションする方法を示します。
author: jashanno
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c51c77f4b9f411ae45fb955032aa40cb34738e9a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964773"
---
# <a name="create-financial-dimensions-for-pos-registers-and-configure-dimension-values-on-registers"></a><span data-ttu-id="b720d-103">POS レジスターの財務分析コードの作成とレジスターの分析コード値のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b720d-103">Create financial dimensions for POS registers and configure dimension values on registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b720d-104">この手順では、販売時点管理 (POS) レジスターの財務分析コードの作成について説明し、レジスターの財務分析コード値をコンフィギュレーションする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b720d-104">This procedure walks through creating financial dimensions for point of sale (POS) registers, and demonstrates how to configure financial dimension values on registers.</span></span> <span data-ttu-id="b720d-105">この手順には、分析コード セットおよび勘定構造の作成など、他の関連手順は含まれません。</span><span class="sxs-lookup"><span data-stu-id="b720d-105">This procedure doesn't include other related steps, such as creating dimension sets and account structures.</span></span> <span data-ttu-id="b720d-106">これらのタスクは他のトピックで示されます。</span><span class="sxs-lookup"><span data-stu-id="b720d-106">Those tasks can be found in other topics.</span></span> <span data-ttu-id="b720d-107">このレコードでは、MXMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="b720d-107">This recording uses USRT demo company.</span></span>

1. <span data-ttu-id="b720d-108">[総勘定元帳] > [勘定科目表] > [分析コード] > [財務分析コード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b720d-108">Go to General ledger > Chart of accounts > Dimensions > Financial dimensions.</span></span>
2. <span data-ttu-id="b720d-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-109">Click New.</span></span>
3. <span data-ttu-id="b720d-110">[値の使用元] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b720d-110">In the Use values from field, select an option.</span></span>
4. <span data-ttu-id="b720d-111">[分析コード名] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b720d-111">In the Dimension name field, type a value.</span></span>
5. <span data-ttu-id="b720d-112">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-112">Click Activate.</span></span>
6. <span data-ttu-id="b720d-113">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-113">Click Close.</span></span>
7. <span data-ttu-id="b720d-114">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-114">Click Activate.</span></span>
8. <span data-ttu-id="b720d-115">[分析コード値] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-115">Click Dimension values.</span></span>
9. <span data-ttu-id="b720d-116">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b720d-116">Close the page.</span></span>
10. <span data-ttu-id="b720d-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-117">Click Save.</span></span>
11. <span data-ttu-id="b720d-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b720d-118">Close the page.</span></span>
12. <span data-ttu-id="b720d-119">小売りとコマース > チャネル設定 > POS 設定 > レジスターの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b720d-119">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
13. <span data-ttu-id="b720d-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="b720d-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="b720d-121">[財務分析コード] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="b720d-121">Toggle the expansion of the Financial dimensions section.</span></span>
15. <span data-ttu-id="b720d-122">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-122">Click Edit.</span></span>
16. <span data-ttu-id="b720d-123">[ターミナル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="b720d-123">In the Terminal field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="b720d-124">リストで、更新されたレジスターの分析コード値を参照して選択します。</span><span class="sxs-lookup"><span data-stu-id="b720d-124">In the list, find and select the dimension value for the register being updated.</span></span>
18. <span data-ttu-id="b720d-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b720d-125">Click Save.</span></span>


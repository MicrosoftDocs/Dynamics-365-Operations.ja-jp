---
title: バーコード タイプの管理
description: この手順は、ピッキング リスト レポートの一部として使用される、新しいバーコードの定義を設定する方法を示します。
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BarcodeSetup, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 979726a1d094146b546bbc6d31963367de2c59f5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204082"
---
# <a name="maintain-barcode-types"></a><span data-ttu-id="b10c9-103">バーコード タイプの管理</span><span class="sxs-lookup"><span data-stu-id="b10c9-103">Maintain barcode types</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b10c9-104">この手順は、ピッキング リスト レポートの一部として使用される、新しいバーコードの定義を設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="b10c9-105">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="b10c9-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="b10c9-106">USMF を使用すると、表示される例の値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="b10c9-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="b10c9-107">通常、これらのタスクを実施するのは、倉庫マネージャーです。</span><span class="sxs-lookup"><span data-stu-id="b10c9-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="b10c9-108">[バーコード] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="b10c9-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10c9-109">Click New.</span></span>
3. <span data-ttu-id="b10c9-110">[バーコード設定] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="b10c9-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b10c9-112">[バーコード タイプ] フィールドでオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="b10c9-113">USMF を使用している場合、「Code 39」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="b10c9-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="b10c9-114">[サイズ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="b10c9-115">[最大の長さ] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="b10c9-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10c9-116">Click Save.</span></span>
9. <span data-ttu-id="b10c9-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b10c9-117">Close the page.</span></span>
10. <span data-ttu-id="b10c9-118">[在庫および倉庫管理パラメーター] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="b10c9-119">[バーコード設定] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b10c9-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="b10c9-120">以前に作成したバーコード設定を選択します。しかしバーコード形式は、プロセスで使用されているレコード タイプに対する固有識別子の形式と一致している必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b10c9-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="b10c9-121">たとえば、ピッキング ルートに対するバーコード形式は、通常番号順序であるピッキング ルート参照の形式と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b10c9-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="b10c9-122">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b10c9-122">Click Save.</span></span>
13. <span data-ttu-id="b10c9-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b10c9-123">Close the page.</span></span>


---
title: 販売時点管理 (POS) 視覚プロファイルの作成
description: この手順では、新しい POS (販売時点管理) の視覚プロファイルの作成方法を説明します。
author: jashanno
manager: AnnBe
ms.date: 12/05/2015
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b265a94c6d8f9e2534e1509e4f33c6f8a05eded0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140949"
---
# <a name="create-point-of-sale-pos-visual-profiles"></a><span data-ttu-id="cfdc4-103">販売時点管理 (POS) 視覚プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="cfdc4-103">Create point of sale (POS) visual profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cfdc4-104">この手順では、新しい POS (販売時点管理) の視覚プロファイルの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-104">This procedure walks through creating a new point of sale (POS) visual profile.</span></span> <span data-ttu-id="cfdc4-105">視覚プロファイルには、POS レジスターの外観を決定する基本情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-105">A visual profile contains basic information that determines the appearance of POS registers.</span></span> <span data-ttu-id="cfdc4-106">複数の視覚プロファイルを作成し、特定のレジスタで使用するプロファイルを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-106">You can create several visual profiles and assign specific profiles to run on specific registers.</span></span> <span data-ttu-id="cfdc4-107">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-107">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="cfdc4-108">Retail と Commerce > チャネル設定 > POS 設定 > POS プロファイル > 視覚プロファイルの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-108">Go to Retail and Commerce > Channel setup > POS setup > POS profiles > Visual profiles.</span></span>
2. <span data-ttu-id="cfdc4-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-109">Click New.</span></span>
3. <span data-ttu-id="cfdc4-110">[プロファイル番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-110">In the Profile number field, type a value.</span></span>
4. <span data-ttu-id="cfdc4-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cfdc4-112">[アプリケーション タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-112">In the Application type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="cfdc4-113">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="cfdc4-114">[テーマ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-114">In the Theme field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cfdc4-115">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="cfdc4-116">[アクセント色] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-116">In the Accent color field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="cfdc4-117">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="cfdc4-118">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="cfdc4-119">[バックグラウンドでログイン] セクションの拡張を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-119">Toggle the expansion of the Login background section.</span></span>
13. <span data-ttu-id="cfdc4-120">[横の画像 ID] フィールドで、画像 ID を選択するか、または入力します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-120">In the Landscape image ID field, select or enter an image ID.</span></span>
14. <span data-ttu-id="cfdc4-121">[ポートレイト画像 ID] フィールドで、画像 ID を選択または入力します。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-121">In the Portrait image ID field, select or enter an image ID.</span></span>
15. <span data-ttu-id="cfdc4-122">[バックグラウンド] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-122">Toggle the expansion of the Background section.</span></span>
16. <span data-ttu-id="cfdc4-123">RequestPopup 画像 ID。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-123">RequestPopup the Image ID.</span></span>
17. <span data-ttu-id="cfdc4-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="cfdc4-125">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cfdc4-125">Click Save.</span></span>


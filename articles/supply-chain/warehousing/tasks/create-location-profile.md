---
title: 場所プロファイルの作成
description: 倉庫の場所は、場所のプロパティに関連したプロファイルを有している必要があります。たとえば、ある場所では品目の混合が許容されているかどうかなどです。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9e1217a1105e1d53fc937f927e066e392f1ef14
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847330"
---
# <a name="create-a-location-profile"></a><span data-ttu-id="9feba-103">場所プロファイルの作成</span><span class="sxs-lookup"><span data-stu-id="9feba-103">Create a location profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9feba-104">倉庫の場所は、場所のプロパティに関連したプロファイルを有している必要があります。たとえば、ある場所では品目の混合が許容されているかどうかなどです。</span><span class="sxs-lookup"><span data-stu-id="9feba-104">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location, for example, whether the location allows mixed items.</span></span> <span data-ttu-id="9feba-105">この手順では、ライセンスプレートの管理が必要ない場所のプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9feba-105">In this procedure we’ll create a profile for a location that doesn’t require license plate control.</span></span> <span data-ttu-id="9feba-106">混合された品目と混合された在庫の状況を有効にして、循環棚卸を可能にします。</span><span class="sxs-lookup"><span data-stu-id="9feba-106">We’ll enable mixed items, and mixed inventory statuses, and allow cycle counting.</span></span> <span data-ttu-id="9feba-107">デモ データの会社 USMF でこの手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9feba-107">You can use this procedure in the USMF demo data company.</span></span>

1. <span data-ttu-id="9feba-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9feba-108">Click New.</span></span>
2. <span data-ttu-id="9feba-109">[場所プロファイル ID] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9feba-109">In the Location profile ID field, type a value.</span></span>
3. <span data-ttu-id="9feba-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9feba-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9feba-111">[場所形式] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9feba-111">In the Location format field, enter or select a value.</span></span>
5. <span data-ttu-id="9feba-112">[場所タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9feba-112">In the Location type field, enter or select a value.</span></span>
6. <span data-ttu-id="9feba-113">[ドック管理プロファイルID] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9feba-113">In the Dock management profile ID field, enter or select a value.</span></span>
7. <span data-ttu-id="9feba-114">[混合保管を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9feba-114">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="9feba-115">[混合在庫状態を許可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9feba-115">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="9feba-116">[循環棚卸] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9feba-116">Select Yes in the Allow cycle counting field.</span></span>
10. <span data-ttu-id="9feba-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9feba-117">Click Save.</span></span>
11. <span data-ttu-id="9feba-118">[倉庫管理] > [設定] > [倉庫] > [場所プロファイル] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9feba-118">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>


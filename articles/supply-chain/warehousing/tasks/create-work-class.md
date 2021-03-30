---
title: 作業クラスの作成
description: この手順では、作業クラスを設定する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49b110b93e6f0f886d180f9f2725245faad7afab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239041"
---
# <a name="create-a-work-class"></a><span data-ttu-id="4b2a3-103">作業クラスの作成</span><span class="sxs-lookup"><span data-stu-id="4b2a3-103">Create a work class</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b2a3-104">この手順では、作業クラスを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-104">This procedure shows you how to set up a work class.</span></span> <span data-ttu-id="4b2a3-105">作業クラスは、倉庫作業者がモバイル デバイスで処理できるワーク オーダー明細行のタイプを指示または制限するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-105">Work classes are used to direct and/or limit the type of work order lines that a warehouse worker can process on a mobile device.</span></span> <span data-ttu-id="4b2a3-106">作業者が処理できる明細行は、倉庫作業者がアクセス権を持つモバイル デバイスの作業クラスと、作業明細行に指定された作業クラスにより決定されます。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-106">The lines that a worker can process are determined from the work classes on the mobile device menu items that the warehouse worker has access to and the work class that's specified on the work lines.</span></span> <span data-ttu-id="4b2a3-107">また、作業クラスは、ワーク オーダー明細行に対して設定されている場所を検証するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-107">Work classes can also be used to validate the put location for a work order line.</span></span> <span data-ttu-id="4b2a3-108">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-108">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4b2a3-109">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="4b2a3-110">[倉庫管理] > [設定] > [作業] > [作業クラス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-110">Go to Warehouse management > Setup > Work > Work classes.</span></span>
2. <span data-ttu-id="4b2a3-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-111">Click New.</span></span>
3. <span data-ttu-id="4b2a3-112">[作業クラス ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-112">In the Work class ID field, type a value.</span></span>
4. <span data-ttu-id="4b2a3-113">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4b2a3-114">[ワーク オーダー タイプ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-114">In the Work order type field, select an option.</span></span>
6. <span data-ttu-id="4b2a3-115">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-115">Click New.</span></span>
7. <span data-ttu-id="4b2a3-116">[場所タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-116">In the Location type field, type a value.</span></span>
    * <span data-ttu-id="4b2a3-117">場所のタイプを選択すると、ピッキング後に品目を配置できる場所の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-117">If you select a location type, this sets a restriction on where items can be put after they've been picked.</span></span> <span data-ttu-id="4b2a3-118">この設定は、場所のディレクティブが場所を解決しようとする場合、または倉庫作業者がモバイル デバイスのメニュー項目に手動で場所を提供する場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-118">This setting is used when a location directive tries to resolve the location, or if a warehouse worker manually provides the location for the mobile device menu item.</span></span>  
8. <span data-ttu-id="4b2a3-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4b2a3-119">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
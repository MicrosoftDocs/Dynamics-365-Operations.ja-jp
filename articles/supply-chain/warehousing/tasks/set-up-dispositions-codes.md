---
title: 廃棄コードの設定
description: この手順では、返品注文の受信プロセスでモバイル デバイスで使用できる廃棄コードの設定を中心に説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85402e05d55367da5fe89b242ad8eafc727b441e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "324126"
---
# <a name="set-up-dispositions-codes"></a><span data-ttu-id="29007-103">廃棄コードの設定</span><span class="sxs-lookup"><span data-stu-id="29007-103">Set up dispositions codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29007-104">この手順では、返品注文の受信プロセスでモバイル デバイスで使用できる廃棄コードの設定を中心に説明します。</span><span class="sxs-lookup"><span data-stu-id="29007-104">This procedure focuses on the setup of a disposition code that can be used on a mobile device for the return order receiving process.</span></span> <span data-ttu-id="29007-105">廃棄コードは、品目を受け取るときに使用できるルールのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="29007-105">Disposition codes are a collection of rules that can be used when items are received.</span></span> <span data-ttu-id="29007-106">たとえば、作業ユーザーがモバイル デバイスを使用して破損した品目を受け取る場合に、そのユーザーは破損した品目の廃棄コードをスキャンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="29007-106">For example, when a work user uses a mobile device to receive items that were damaged, the user must scan a disposition code for damaged items.</span></span> <span data-ttu-id="29007-107">受入済の商品の在庫状態、作業テンプレート、および場所のディレクティブは、スキャンした廃棄コードから決定することができます。</span><span class="sxs-lookup"><span data-stu-id="29007-107">The inventory status of the goods received, the work template, and the location directive can be determined from the scanned disposition code.</span></span> <span data-ttu-id="29007-108">発注書の入荷プロセスおよび完了したプロセスの製造オーダー レポートでは、廃棄コードの使用はオプションです。</span><span class="sxs-lookup"><span data-stu-id="29007-108">For the purchase order receiving process and the production order report as finished process, the use of a disposition code is optional.</span></span> <span data-ttu-id="29007-109">販売注文の返品入庫プロセスでは、品目がモバイル デバイスを使用して登録されている場合、廃棄コードの使用は必須です。</span><span class="sxs-lookup"><span data-stu-id="29007-109">For the sales order return receiving process, if the items are registered using a mobile device, the use of disposition code is mandatory.</span></span>  <span data-ttu-id="29007-110">このガイドは、デモ データの会社 USMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="29007-110">This guide was created using the demo data company USMF.</span></span> <span data-ttu-id="29007-111">この手順は、倉庫マネージャーを対象としています。</span><span class="sxs-lookup"><span data-stu-id="29007-111">This procedure is intended for the warehouse manager.</span></span> 

1. <span data-ttu-id="29007-112">[倉庫管理] > [設定] > [モバイル デバイス] > [廃棄コード] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="29007-112">Go to Warehouse management > Setup > Mobile device > Disposition codes.</span></span>
2. <span data-ttu-id="29007-113">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="29007-113">Click New.</span></span>
    * <span data-ttu-id="29007-114">顧客からの返品に使用する新しい廃棄コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="29007-114">Create a new disposition code to use for customer returns.</span></span>  
3. <span data-ttu-id="29007-115">[廃棄コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29007-115">In the Disposition code field, type a value.</span></span>
4. <span data-ttu-id="29007-116">[在庫状態] フィールドで、在庫ブロックのある在庫状態を選択します。</span><span class="sxs-lookup"><span data-stu-id="29007-116">In the Inventory status field, select an inventory status where there is inventory blocking.</span></span>
    * <span data-ttu-id="29007-117">USMF を使用している場合は、[ブロック] を選択します。</span><span class="sxs-lookup"><span data-stu-id="29007-117">If you're using USMF, select 'Blocking'.</span></span> <span data-ttu-id="29007-118">注文明細行の既定のステータスを上書きする場合は、廃棄コードに在庫状態を追加できます。</span><span class="sxs-lookup"><span data-stu-id="29007-118">You can add an inventory status to the disposition code to override the default status that’s on the order lines.</span></span>  
5. <span data-ttu-id="29007-119">[作業テンプレート] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29007-119">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="29007-120">オプション: 返品注文に関連付けられる作業テンプレート コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="29007-120">Optional: Select a work template code that is associated with a return order.</span></span> <span data-ttu-id="29007-121">値が入力されていない場合は、作業テンプレートは、システムでコンフィギュレーションされた標準のルールを使用して解決されます。</span><span class="sxs-lookup"><span data-stu-id="29007-121">If no value is provided, the work template will be resolved using the standard rules configured in your system.</span></span> <span data-ttu-id="29007-122">作業テンプレートを選択すると、この廃棄コードを使用できるプロセスが制限されます。</span><span class="sxs-lookup"><span data-stu-id="29007-122">Selecting a work template will limit the processes this disposition code can be used with.</span></span> <span data-ttu-id="29007-123">たとえば、廃棄コードが、ワーク オーダー タイプが発注書である作業テンプレートを含む場合、顧客からの返品品目の登録に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="29007-123">For example, if a disposition code has a work template with a work order of type purchase order, it can’t be used to register items that are returned by customers.</span></span>  
6. <span data-ttu-id="29007-124">[返品廃棄コード] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="29007-124">In the Return disposition code field, type a value.</span></span>
    * <span data-ttu-id="29007-125">返品廃棄コードにより、登録された品目の返品注文プロセスの残りが決まります。</span><span class="sxs-lookup"><span data-stu-id="29007-125">The return disposition code determines the remainder of the return order process for the items registered.</span></span> <span data-ttu-id="29007-126">この例では、顧客は貸方票を受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="29007-126">In this example, the customer should receive a credit note.</span></span> <span data-ttu-id="29007-127">アクションの貸方を含む返品廃棄コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="29007-127">Add a returns disposition code that contains an action Credit.</span></span>  


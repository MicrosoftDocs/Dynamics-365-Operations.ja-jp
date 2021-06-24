---
title: POS でシリアル番号管理された製品の返品
description: このトピックでは、Microsoft Dynamics 365 Commerce POS (POS) アプリケーションの返品プロセスの一部としてシリアル番号が付された品目を検証するための機能について説明します。
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129817"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="7b7c2-103">POS でシリアル番号管理された製品の返品</span><span class="sxs-lookup"><span data-stu-id="7b7c2-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7b7c2-104">このトピックでは、Microsoft Dynamics 365 Commerce POS (POS) アプリケーションの返品プロセスの一部としてシリアル番号が付された品目を検証するための機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="7b7c2-105">Commerce バージョン 10.0.20 リリース以降では、**POS での統合返品処理エクスペリエンス** という新しい機能が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="7b7c2-106">POS での返品注文処理時にシリアル番号の検証を使用するには、この機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="7b7c2-107">この機能が有効な場合に提供される他の機能の詳細については、[POS での返品の作成](POS-returns.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="7b7c2-108">機能を有効にした後で無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="7b7c2-109">シリアル番号付き返品を検証するためのオプション</span><span class="sxs-lookup"><span data-stu-id="7b7c2-109">Options for validating serialized returns</span></span>

<span data-ttu-id="7b7c2-110">**POS での統合返品処理エクスペリエンス** 機能を有効にすると、組織が、POS を通じてシリアル番号で制御される品目の返品検証を実行できます。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="7b7c2-111">この機能により、返品されるシリアル番号が販売された元のシリアル番号と異なる場合に警告を表示できます。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="7b7c2-112">Commerce Version 10.0.20 リリース以降では、ユーザーが受信するメッセージは警告メッセージのみです。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="7b7c2-113">ユーザーは、当初販売されたシリアル番号とは異なるシリアル番号に対する返品処理を続行できます。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="7b7c2-114">**POS での統合返品処理エクスペリエンス** 機能が有効になった後に組織に対してシリアル番号の検証を構成するには、Commerce Headquarters の **Retail と Commerce \> 本社の設定 \> パラメーター \> コマース パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="7b7c2-115">**在庫** タブの **店舗在庫操作** クイックタブで、**POS 返品時にシリアル番号の検証を有効にする** オプションを **はい** に設定 します。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="7b7c2-116">POS でシリアル番号が設定された品目の返品の処理</span><span class="sxs-lookup"><span data-stu-id="7b7c2-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="7b7c2-117">**POS 返品でのシリアル番号の検証を有効にする** オプションが **はい** に設定されている場合、POS を使用してシリアル番号管理されている品目が返品されれば、ユーザーは **返品可能な製品** ページの詳細ペインに返品行のシリアル番号を入力できます。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="7b7c2-118">入力したシリアル番号が販売トランザクションで販売された元のシリアル番号と一致しない場合、ユーザーに警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="7b7c2-119">ただし、アプリケーションによりユーザーが返品の転記を続行できなくなることはありません。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="7b7c2-120">現在、POS では、元の注文数量が 1 つ以下の返品明細行でのみシリアル番号の検証がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="7b7c2-121">元の販売注文行が POS 以外のチャンネルで作成されている場合、特定の販売行のシリアル番号が付いた品目の注文済数量が複数の場合、POS を使用して品目を適切に返品することはできません。</span><span class="sxs-lookup"><span data-stu-id="7b7c2-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7b7c2-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="7b7c2-122">Additional resources</span></span>

[<span data-ttu-id="7b7c2-123">POS での返品の作成</span><span class="sxs-lookup"><span data-stu-id="7b7c2-123">Create returns in POS</span></span>](POS-returns.md)

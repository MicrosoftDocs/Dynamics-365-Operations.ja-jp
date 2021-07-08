---
title: 仕入先コードが特定の製品および日付に対して承認されていない場合
description: 計画オーダーを確定する、または発注書に明細行を追加しようとすると、仕入先コードが製品と日付に対して承認されていないというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294122"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="d455d-103">仕入先コードが特定の製品および日付に対して承認されていない場合</span><span class="sxs-lookup"><span data-stu-id="d455d-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="d455d-104">エラーコード: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="d455d-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="d455d-105">現象</span><span class="sxs-lookup"><span data-stu-id="d455d-105">Symptoms</span></span>

<span data-ttu-id="d455d-106">計画オーダーを確定する、または発注書に明細行を追加しようとする際に、次のエラー メッセージが表示されます:</span><span class="sxs-lookup"><span data-stu-id="d455d-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="d455d-107">仕入先コード %1 は、%3 の %2 に対して承認されていません。</span><span class="sxs-lookup"><span data-stu-id="d455d-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="d455d-108">原因</span><span class="sxs-lookup"><span data-stu-id="d455d-108">Cause</span></span>

<span data-ttu-id="d455d-109">**承認仕入先チェック メソッド** フィールドが指定された製品に対して *警告のみ* または *許可しない* に設定され、仕入先には現在その製品を供給する権限がないためです。</span><span class="sxs-lookup"><span data-stu-id="d455d-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="d455d-110">解決策</span><span class="sxs-lookup"><span data-stu-id="d455d-110">Resolution</span></span>

<span data-ttu-id="d455d-111">この問題を解決するには、関連する製品の仕入先チェックを無効にするか、仕入先を承認します。</span><span class="sxs-lookup"><span data-stu-id="d455d-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="d455d-112">製品の仕入先チェックを無効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d455d-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="d455d-113">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d455d-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d455d-114">関連する製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="d455d-114">Open the relevant product.</span></span>
1. <span data-ttu-id="d455d-115">**購買** クイック タブで、**承認仕入先チェック メソッド** フィールドを *警告のみ* または *許可しない* 以外の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="d455d-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="d455d-116">製品の仕入先を承認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d455d-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="d455d-117">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d455d-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="d455d-118">関連する品目を開きます。</span><span class="sxs-lookup"><span data-stu-id="d455d-118">Open the relevant item.</span></span>
1. <span data-ttu-id="d455d-119">アクション ウィンドウの、**購買** タブの、**承認仕入先** グループで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d455d-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="d455d-120">**承認仕入先** リスト ページで、行をグリッドに追加し、それに対して次の値を設定します:</span><span class="sxs-lookup"><span data-stu-id="d455d-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="d455d-121">**仕入先** – 現在の製品を承認する仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="d455d-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="d455d-122">**有効日** – 仕入先が承認される最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="d455d-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="d455d-123">**有効期限** – 仕入先が承認されている最後の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="d455d-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="d455d-124">詳細については、[特定の製品に対する仕入先の承認](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d455d-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>

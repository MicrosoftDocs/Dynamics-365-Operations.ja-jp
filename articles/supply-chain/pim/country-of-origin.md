---
title: 原産国
description: 多くの組織では、仕入先に証明書を発行して、製品が特定の認証基準を満たしていることを確認しています。 多くの場合、これら証明書は原産国によって異なります。 このトピックでは、原産国機能に関する情報を提供します。これにより、製品を原産国にリンクさせ、製品の認証を追跡することができます。
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596250"
---
# <a name="country-of-origin"></a><span data-ttu-id="26ec7-105">原産国</span><span class="sxs-lookup"><span data-stu-id="26ec7-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26ec7-106">多くの組織では、仕入先に証明書を発行して、製品が特定の認証基準を満たしていることを確認しています。</span><span class="sxs-lookup"><span data-stu-id="26ec7-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="26ec7-107">多くの場合、これら証明書は原産国によって異なります。</span><span class="sxs-lookup"><span data-stu-id="26ec7-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="26ec7-108">原産国機能を使用すると、製品を原産国にリンクさせ、製品の認証を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="26ec7-109">送信元と送信先の国を構成する</span><span class="sxs-lookup"><span data-stu-id="26ec7-109">Configure source and destination countries</span></span>

<span data-ttu-id="26ec7-110">製品の証明書を発行する前に、製品の出荷先の国とその原産国の国をを結びつける必要があります。</span><span class="sxs-lookup"><span data-stu-id="26ec7-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="26ec7-111">**製品情報管理 \> 設定 \> プロダクト コンプライアンス \> 原産国 \> 原産国ルール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="26ec7-112">既存の国の設定を選択して編集するか、アクション ペインで**新規** を選択して新しい国の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="26ec7-113">選択された国、または新しい国に対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="26ec7-114">フィールド</span><span class="sxs-lookup"><span data-stu-id="26ec7-114">Field</span></span> | <span data-ttu-id="26ec7-115">説明</span><span class="sxs-lookup"><span data-stu-id="26ec7-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="26ec7-116">品目番号</span><span class="sxs-lookup"><span data-stu-id="26ec7-116">Item number</span></span> | <span data-ttu-id="26ec7-117">製品の品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="26ec7-118">発送先国</span><span class="sxs-lookup"><span data-stu-id="26ec7-118">Destination country</span></span> | <span data-ttu-id="26ec7-119">製品の送付先となる国を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="26ec7-120">発送元の国</span><span class="sxs-lookup"><span data-stu-id="26ec7-120">Origin country</span></span> | <span data-ttu-id="26ec7-121">製品の送付先となる国を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="26ec7-122">この設定の目的は、送信元と送信先の国が指定されているパーツの原産国を含む部品表 (BOM) レポートの生成を容易にすることです。</span><span class="sxs-lookup"><span data-stu-id="26ec7-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="26ec7-123">このレポートは、部品がどこから来て、どこに向かっているのかを全体的に把握する際に有用です。</span><span class="sxs-lookup"><span data-stu-id="26ec7-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="26ec7-124">仕入先証明書を追跡する</span><span class="sxs-lookup"><span data-stu-id="26ec7-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="26ec7-125">**原産国の仕入先証明書** ページを使用して、仕入先に発行する証明書を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="26ec7-126">発行する証明書ドキュメントと、顧客に対する報告方法を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="26ec7-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="26ec7-127">この機能は、証明書の管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="26ec7-128">また、請求書、梱包伝票、および/または注文確認書に関連する証明書番号を表示するかどうかを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="26ec7-129">証明書情報を設定するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="26ec7-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="26ec7-130">**製品情報管理 \> 設定 \> プロダクト コンプライアンス \> 原産国 \> 原産国仕入先証明書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="26ec7-131">既存の証明書の設定を選択して編集するか、アクション ペインで**新規** を選択して新しい証明書の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="26ec7-132">選択された証明書、または新しい証明書に対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="26ec7-133">フィールド</span><span class="sxs-lookup"><span data-stu-id="26ec7-133">Field</span></span> | <span data-ttu-id="26ec7-134">説明</span><span class="sxs-lookup"><span data-stu-id="26ec7-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="26ec7-135">仕入先勘定</span><span class="sxs-lookup"><span data-stu-id="26ec7-135">Vendor account</span></span> | <span data-ttu-id="26ec7-136">証明書を発行した仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="26ec7-137">品目番号</span><span class="sxs-lookup"><span data-stu-id="26ec7-137">Item number</span></span> | <span data-ttu-id="26ec7-138">証明書を発行した品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="26ec7-139">国/地域</span><span class="sxs-lookup"><span data-stu-id="26ec7-139">Country/region</span></span> | <span data-ttu-id="26ec7-140">この証明書を使用刷る必要のある配送先の国、または地域。</span><span class="sxs-lookup"><span data-stu-id="26ec7-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="26ec7-141">証明書番号</span><span class="sxs-lookup"><span data-stu-id="26ec7-141">Certificate number</span></span> | <span data-ttu-id="26ec7-142">発行した証明書の ID 番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="26ec7-143">開始</span><span class="sxs-lookup"><span data-stu-id="26ec7-143">Effective</span></span> | <span data-ttu-id="26ec7-144">現在の証明書が有効となる最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="26ec7-145">有効期限</span><span class="sxs-lookup"><span data-stu-id="26ec7-145">Expiration</span></span> | <span data-ttu-id="26ec7-146">現在の証明書が有効となる最終日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="26ec7-147">請求書に印刷する</span><span class="sxs-lookup"><span data-stu-id="26ec7-147">Print on invoice</span></span> | <span data-ttu-id="26ec7-148">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が請求書に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="26ec7-149">梱包明細に印刷する</span><span class="sxs-lookup"><span data-stu-id="26ec7-149">Print on packing slip</span></span> | <span data-ttu-id="26ec7-150">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が梱包明細に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="26ec7-151">販売注文書に印刷する</span><span class="sxs-lookup"><span data-stu-id="26ec7-151">Print on sales order</span></span> | <span data-ttu-id="26ec7-152">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が販売注文書に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="26ec7-153">BOM レポートに原産国を含める</span><span class="sxs-lookup"><span data-stu-id="26ec7-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="26ec7-154">BOM レポートを生成する場合は、**原産国ルール** のページで、原産国と仕向国を指定した各パーツの原産国を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="26ec7-155">**製品管理情報 \> 製品 \> リリースされた製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="26ec7-156">製品を選択、または作成して、 **リリース済み製品の詳細**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="26ec7-157">アクション ペインの、**エンジニア**タブの、**BOM**グループで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="26ec7-158">アクション ウィンドウの表示されたページで、**BOM \> 印刷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="26ec7-159">**部品表明細行** ダイアログ ボックスで、**出荷先の国** フィールドにレポートで表示する目的地の国を設定します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="26ec7-160">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-160">Select **OK**.</span></span>

<span data-ttu-id="26ec7-161">各パートの原産国に関する情報を表示するレポートが生成、表示されます。</span><span class="sxs-lookup"><span data-stu-id="26ec7-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="26ec7-162">レポートの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="26ec7-162">Here is an example of the report.</span></span>

<span data-ttu-id="26ec7-163">![原産国のレポート](media/country-of-origin-report.png "原産国のレポート")</span><span class="sxs-lookup"><span data-stu-id="26ec7-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>

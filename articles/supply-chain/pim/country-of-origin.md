---
title: 原産国
description: 多くの組織では、仕入先に証明書を発行して、製品が特定の認証基準を満たしていることを確認しています。 多くの場合、これら証明書は原産国によって異なります。 このトピックでは、原産国機能に関する情報を提供します。これにより、製品を原産国にリンクさせ、製品の認証を追跡することができます。
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: b07747752dd09f39c3a7a9a647cc3d10cc4b5cc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829549"
---
# <a name="country-of-origin"></a><span data-ttu-id="b3d36-105">原産国</span><span class="sxs-lookup"><span data-stu-id="b3d36-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3d36-106">多くの組織では、仕入先に証明書を発行して、製品が特定の認証基準を満たしていることを確認しています。</span><span class="sxs-lookup"><span data-stu-id="b3d36-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="b3d36-107">多くの場合、これら証明書は原産国によって異なります。</span><span class="sxs-lookup"><span data-stu-id="b3d36-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="b3d36-108">原産国機能を使用すると、製品を原産国にリンクさせ、製品の認証を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="b3d36-109">原産国機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="b3d36-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="b3d36-110">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3d36-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b3d36-111">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="b3d36-112">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="b3d36-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b3d36-113">**モジュール :** *製品情報管理*</span><span class="sxs-lookup"><span data-stu-id="b3d36-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="b3d36-114">**機能名 :** *原産国管理機能*</span><span class="sxs-lookup"><span data-stu-id="b3d36-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="b3d36-115">送信元と送信先の国を構成する</span><span class="sxs-lookup"><span data-stu-id="b3d36-115">Configure source and destination countries</span></span>

<span data-ttu-id="b3d36-116">製品の証明書を発行する前に、製品の出荷先の国とその原産国の国をを結びつける必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3d36-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="b3d36-117">**製品情報管理 \> 設定 \> プロダクト コンプライアンス \> 原産国 \> 原産国ルール** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="b3d36-118">既存の国の設定を選択して編集するか、アクション ペインで **新規** を選択して新しい国の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="b3d36-119">選択された国、または新しい国に対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="b3d36-120">フィールド</span><span class="sxs-lookup"><span data-stu-id="b3d36-120">Field</span></span> | <span data-ttu-id="b3d36-121">説明</span><span class="sxs-lookup"><span data-stu-id="b3d36-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="b3d36-122">品目番号</span><span class="sxs-lookup"><span data-stu-id="b3d36-122">Item number</span></span> | <span data-ttu-id="b3d36-123">製品の品目番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="b3d36-124">発送先国</span><span class="sxs-lookup"><span data-stu-id="b3d36-124">Destination country</span></span> | <span data-ttu-id="b3d36-125">製品の送付先となる国を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="b3d36-126">発送元の国</span><span class="sxs-lookup"><span data-stu-id="b3d36-126">Origin country</span></span> | <span data-ttu-id="b3d36-127">製品の送付先となる国を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="b3d36-128">この設定の目的は、送信元と送信先の国が指定されているパーツの原産国を含む部品表 (BOM) レポートの生成を容易にすることです。</span><span class="sxs-lookup"><span data-stu-id="b3d36-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="b3d36-129">このレポートは、部品がどこから来て、どこに向かっているのかを全体的に把握する際に有用です。</span><span class="sxs-lookup"><span data-stu-id="b3d36-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="b3d36-130">仕入先証明書を追跡する</span><span class="sxs-lookup"><span data-stu-id="b3d36-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="b3d36-131">**原産国の仕入先証明書** ページを使用して、仕入先に発行する証明書を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="b3d36-132">発行する証明書ドキュメントと、顧客に対する報告方法を決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3d36-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="b3d36-133">この機能は、証明書の管理に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="b3d36-134">また、請求書、梱包伝票、および/または注文確認書に関連する証明書番号を表示するかどうかを選択することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="b3d36-135">証明書情報を設定するには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="b3d36-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="b3d36-136">**製品情報管理 \> 設定 \> プロダクト コンプライアンス \> 原産国 \> 原産国仕入先証明書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="b3d36-137">既存の証明書の設定を選択して編集するか、アクション ペインで **新規** を選択して新しい証明書の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="b3d36-138">選択された証明書、または新しい証明書に対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="b3d36-139">フィールド</span><span class="sxs-lookup"><span data-stu-id="b3d36-139">Field</span></span> | <span data-ttu-id="b3d36-140">説明</span><span class="sxs-lookup"><span data-stu-id="b3d36-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="b3d36-141">仕入先勘定</span><span class="sxs-lookup"><span data-stu-id="b3d36-141">Vendor account</span></span> | <span data-ttu-id="b3d36-142">証明書を発行した仕入先を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="b3d36-143">品目番号</span><span class="sxs-lookup"><span data-stu-id="b3d36-143">Item number</span></span> | <span data-ttu-id="b3d36-144">証明書を発行した品目を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="b3d36-145">国/地域</span><span class="sxs-lookup"><span data-stu-id="b3d36-145">Country/region</span></span> | <span data-ttu-id="b3d36-146">この証明書を使用刷る必要のある配送先の国、または地域。</span><span class="sxs-lookup"><span data-stu-id="b3d36-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="b3d36-147">証明書番号</span><span class="sxs-lookup"><span data-stu-id="b3d36-147">Certificate number</span></span> | <span data-ttu-id="b3d36-148">発行した証明書の ID 番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="b3d36-149">開始</span><span class="sxs-lookup"><span data-stu-id="b3d36-149">Effective</span></span> | <span data-ttu-id="b3d36-150">現在の証明書が有効となる最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="b3d36-151">有効期限</span><span class="sxs-lookup"><span data-stu-id="b3d36-151">Expiration</span></span> | <span data-ttu-id="b3d36-152">現在の証明書が有効となる最終日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="b3d36-153">請求書に印刷する</span><span class="sxs-lookup"><span data-stu-id="b3d36-153">Print on invoice</span></span> | <span data-ttu-id="b3d36-154">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が請求書に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="b3d36-155">梱包明細に印刷する</span><span class="sxs-lookup"><span data-stu-id="b3d36-155">Print on packing slip</span></span> | <span data-ttu-id="b3d36-156">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が梱包明細に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="b3d36-157">販売注文書に印刷する</span><span class="sxs-lookup"><span data-stu-id="b3d36-157">Print on sales order</span></span> | <span data-ttu-id="b3d36-158">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が販売注文書に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="b3d36-159">BOM レポートに原産国を含める</span><span class="sxs-lookup"><span data-stu-id="b3d36-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="b3d36-160">BOM レポートを生成する場合は、**原産国ルール** のページで、原産国と仕向国を指定した各パーツの原産国を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="b3d36-161">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b3d36-162">製品を選択、または作成して、 **リリース済み製品の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="b3d36-163">アクション ペインの、**エンジニア** タブの、**BOM** グループで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="b3d36-164">アクション ウィンドウの表示されたページで、**BOM \> 印刷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="b3d36-165">**部品表明細行** ダイアログ ボックスで、**出荷先の国** フィールドにレポートで表示する目的地の国を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="b3d36-166">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-166">Select **OK**.</span></span>

<span data-ttu-id="b3d36-167">各パートの原産国に関する情報を表示するレポートが生成、表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3d36-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="b3d36-168">レポートの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b3d36-168">Here is an example of the report.</span></span>

<span data-ttu-id="b3d36-169">![原産国のレポート](media/country-of-origin-report.png "原産国のレポート")</span><span class="sxs-lookup"><span data-stu-id="b3d36-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
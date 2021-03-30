---
title: デュアルユース商品
description: このトピックでは、デュアルユース商品として識別された製品を追跡し、関連する製品と仕向国ごとに証明書番号を保存し、関連する請求書、梱包伝票、および/または販売注文書に有効な証明書番号を印刷する方法について説明します。
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: a6cc730f8d672d906072a9b97b737dbdea9faf2d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243204"
---
# <a name="dual-use-goods"></a><span data-ttu-id="03bd7-103">デュアルユース商品</span><span class="sxs-lookup"><span data-stu-id="03bd7-103">Dual-use goods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03bd7-104">デュアルユース商品とは、一般的には、民生用と軍事用の両方の用途を持つ品目です。</span><span class="sxs-lookup"><span data-stu-id="03bd7-104">Dual-use goods are typically items that have both civilian and military applications.</span></span> <span data-ttu-id="03bd7-105">たとえば、化学物質は肥料や爆発物として使用される場合があります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-105">For example, a chemical might be used as either a fertilizer or an explosive.</span></span> <span data-ttu-id="03bd7-106">多くの国では、デュアルユース商品の輸出、輸入、輸送に適用される特別な規制があります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-106">Many countries have special regulations that apply to the export, import, and transportation of dual-use goods.</span></span> <span data-ttu-id="03bd7-107">したがって、デュアルユース商品の国際取引に携わる企業は、様々な政策や証明書を把握しておくことが重要です。</span><span class="sxs-lookup"><span data-stu-id="03bd7-107">Therefore, it's important that companies that are involved in the international trade of dual-use goods keep track of the various policies and certificates.</span></span>

<span data-ttu-id="03bd7-108">デュアルユース機能を使用することで、デュアルユース商品として識別された製品を追跡し、関連する製品と仕向国ごとに証明書番号を保存し、関連する請求書、梱包伝票、および/または販売注文書に有効な証明書番号を印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-108">The dual-use feature helps companies keep track of products that are identified as dual-use goods, stores certificate numbers for each relevant product and destination country, and print valid certificate numbers on relevant invoices, packing slips, and/or sales orders.</span></span> <span data-ttu-id="03bd7-109">これにより、製品の出荷時に、常に最新の証明書を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-109">It helps ensure that, when your products are shipped, they always include up-to-date certifications.</span></span>

<span data-ttu-id="03bd7-110">たとえば、以下のシナリオを考えてみます :</span><span class="sxs-lookup"><span data-stu-id="03bd7-110">Consider the following scenario:</span></span>

1. <span data-ttu-id="03bd7-111">ご利用のシステムの **デュアルユースの国設定** ページでは、フランスへの出荷に証明書が必要であることを示しています。</span><span class="sxs-lookup"><span data-stu-id="03bd7-111">The **Dual use country setup** page in your system indicates that shipments to France require a certification.</span></span>
2. <span data-ttu-id="03bd7-112">商品 X-100 の **リリース済製品の詳細** ページには、これがデュアルユース商品であることが示されています。</span><span class="sxs-lookup"><span data-stu-id="03bd7-112">The **Released product details** page for product X-100 indicates that it's a dual-use good.</span></span> <span data-ttu-id="03bd7-113">コード、カテゴリー、グループ、政府を組み合わせにより、製品が属する輸出管理の分類を示します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-113">Together, the code, category, group, and regime indicate the export control classification that the product belongs to.</span></span>
3. <span data-ttu-id="03bd7-114">**デュアルユース証明書** ページには、フランスに出荷される際の、製品 X-100 の証明書が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03bd7-114">The **Dual use certificates** page includes a certificate for product X-100 when it's shipped to France.</span></span> <span data-ttu-id="03bd7-115">この証明書は 2020年1月1日 に期限が切れます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-115">This certificate expires January 1, 2020.</span></span>
4. <span data-ttu-id="03bd7-116">2020年6月17日に、フランスに拠点を置く顧客企業のに向けて販売注文を作成し、その注文には製品X-100が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03bd7-116">On June 17, 2020, you create a sales order for a customer company that is based in France, and the order includes product X-100.</span></span>
5. <span data-ttu-id="03bd7-117">販売注文を保存すると、システムによって次の情報が決定されます :</span><span class="sxs-lookup"><span data-stu-id="03bd7-117">When you save the sales order, the system determines the following information:</span></span>

    1. <span data-ttu-id="03bd7-118">この注文には、デュアルユースの商品が使用されている商品が含まれていますか？</span><span class="sxs-lookup"><span data-stu-id="03bd7-118">Does the order include any products that are dual-use goods?</span></span>
    2. <span data-ttu-id="03bd7-119">注文にデュアルユース商品が含まれている場合、送信先の国ではデュアル使用の証明書を必要としていますか？</span><span class="sxs-lookup"><span data-stu-id="03bd7-119">If the order includes dual-use goods, does the destination country require dual-use certificates?</span></span>
    3. <span data-ttu-id="03bd7-120">送信先の国がデュアルユース証明書を要求している場合、デュアルユース商品ごとに有効な証明書が存在していますか？</span><span class="sxs-lookup"><span data-stu-id="03bd7-120">If the country requires dual-use certificates, does a valid certificate exist for each dual-use good for the destination country?</span></span>

6. <span data-ttu-id="03bd7-121">この注文には製品 X-100 が含まれており、かつ製品はフランスに出荷されており、製品にはフランスの証明書が存在します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-121">The order includes product X-100, the product is being shipped to France, and a French certificate exists for the product.</span></span> <span data-ttu-id="03bd7-122">ただし、証明書の有効期限は切れています。</span><span class="sxs-lookup"><span data-stu-id="03bd7-122">However, the certificate has expired.</span></span> <span data-ttu-id="03bd7-123">そのため、次のような警告メッセージが表示されます。「この販売注文に含まれる1つ以上のデュアルユース商品に含まれているデュアルユース証明書が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="03bd7-123">Therefore, you receive the following warning message: "Dual use certificates for one or more dual-use items in this sales order aren't valid.</span></span> <span data-ttu-id="03bd7-124">確認作業を進めますか？」</span><span class="sxs-lookup"><span data-stu-id="03bd7-124">Do you want to proceed with the confirmation?"</span></span>

<span data-ttu-id="03bd7-125">このトピックでは、デュアルユース賞品を設定し、このシナリオに対応するにあたって必要となるすべての設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-125">This topic explains how to configure all the settings that are required to set up dual-use goods and support this scenario.</span></span>

## <a name="define-dual-use-requirements-for-each-relevant-country"></a><span data-ttu-id="03bd7-126">関連する国ごとにデュアルユースの要件を定義する</span><span class="sxs-lookup"><span data-stu-id="03bd7-126">Define dual-use requirements for each relevant country</span></span>

<span data-ttu-id="03bd7-127">デュアルユース商品に対する要件は国によって異なります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-127">Different countries have different requirements for dual-use goods.</span></span> <span data-ttu-id="03bd7-128">**デュアルユースの国設定**  ページを使用して、証明書が必要な国と不要な国を把握することができます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-128">You use the **Dual use country setup** page to keep track of the countries that do and don't require a certificate.</span></span> <span data-ttu-id="03bd7-129">ここで指定した情報は、販売注文の作成時にチェックされ、必要な証明書の提出が通知されます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-129">The information that you specify here is checked when you create sales orders, and you will be reminded to provide the required certifications.</span></span>

<span data-ttu-id="03bd7-130">さまざまな国のデュアルユース要件に関する情報を設定するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-130">To set up the information about dual-use requirements for different countries, follow these steps.</span></span>

1. <span data-ttu-id="03bd7-131">**製品情報管理 \> 設定 \> 製品コンプライアンス \> デュアルユース製品 \>デュアルユースの国設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-131">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use country setup**.</span></span>
2. <span data-ttu-id="03bd7-132">既存の国設定を選択して編集するか、アクション ウィンドウで **新規** を選択して新たな国の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-132">Select an existing country setup to edit it, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="03bd7-133">選択された国設定、または新たな国設定に対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-133">Set the following values for the selected or new country setup.</span></span>

    | <span data-ttu-id="03bd7-134">フィールド</span><span class="sxs-lookup"><span data-stu-id="03bd7-134">Field</span></span> | <span data-ttu-id="03bd7-135">説明</span><span class="sxs-lookup"><span data-stu-id="03bd7-135">Description</span></span> |
    |---|---|
    | <span data-ttu-id="03bd7-136">国/地域</span><span class="sxs-lookup"><span data-stu-id="03bd7-136">Country/region</span></span> | <span data-ttu-id="03bd7-137">要件を追跡している国を選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-137">Select the country that you're tracking requirements for.</span></span> |
    | <span data-ttu-id="03bd7-138">必要な証明書</span><span class="sxs-lookup"><span data-stu-id="03bd7-138">Certificate Required</span></span> | <span data-ttu-id="03bd7-139">デュアルユース商品の認証が必要な国の場合は、このチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="03bd7-139">Select this check box for countries that require a certification for dual-use goods.</span></span> <span data-ttu-id="03bd7-140">この認証が必要ない国についてはオフにしてください。</span><span class="sxs-lookup"><span data-stu-id="03bd7-140">Clear it for countries that don't require this certification.</span></span> |

## <a name="create-dual-use-categories"></a><span data-ttu-id="03bd7-141">デュアルユース カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="03bd7-141">Create dual-use categories</span></span>

<span data-ttu-id="03bd7-142">多くの場合、デュアルユースの商品は、輸出管理分類番号 (ECCN) に従って分類される必要があります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-142">Dual-use goods must often be categorized according to their export control classification number (ECCN).</span></span> <span data-ttu-id="03bd7-143">ECCN とは、商品や技術などの要素に基づいて項目を分類する英数字のコードです。</span><span class="sxs-lookup"><span data-stu-id="03bd7-143">The ECCN is an alphanumeric code that categorizes items based on factors such as the commodity and technology.</span></span> <span data-ttu-id="03bd7-144">**デュアル使用カテゴリ** ページでは、レポートに使用するカテゴリのリストを作成できます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-144">The **Dual use categories** page helps you make a list of the categories that you use, for reporting purposes.</span></span>

<span data-ttu-id="03bd7-145">デュアル使用カテゴリを設定するには、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="03bd7-145">To set up dual-use categories, follow these steps.</span></span>

1. <span data-ttu-id="03bd7-146">**製品情報管理 \> 設定 \> 製品コンプライアンス \> デュアルユース製品 \>デュアルユースのカテゴリ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-146">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use categories**.</span></span>
2. <span data-ttu-id="03bd7-147">既存の糧ふぉりを選択して編集するか、アクション ペインで **新規** を選択して新しいカテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-147">Select an existing category to edit it, or select **New** on the Action Pane to create a new category.</span></span>
3. <span data-ttu-id="03bd7-148">選択されたカテゴリ、または新しいカテゴリに対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-148">Set the following values for the selected or new category.</span></span>

    | <span data-ttu-id="03bd7-149">フィールド</span><span class="sxs-lookup"><span data-stu-id="03bd7-149">Fields</span></span> | <span data-ttu-id="03bd7-150">説明</span><span class="sxs-lookup"><span data-stu-id="03bd7-150">Description</span></span> |
    |---|---|
    | <span data-ttu-id="03bd7-151">デュアル ユースのコード</span><span class="sxs-lookup"><span data-stu-id="03bd7-151">Dual use code</span></span> | <span data-ttu-id="03bd7-152">ECCN の完全なコードを入力します (例 : *3a001*)。</span><span class="sxs-lookup"><span data-stu-id="03bd7-152">Enter the full ECCN code (for example, *3A001*).</span></span>|
    | <span data-ttu-id="03bd7-153">デュアル ユースのカテゴリ</span><span class="sxs-lookup"><span data-stu-id="03bd7-153">Dual use category</span></span> | <span data-ttu-id="03bd7-154">ECCN コードのコマース コントロール リスト (CCL) カテゴリ部分を入力します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-154">Enter the commerce control list (CCL) category part of the ECCN code.</span></span> <span data-ttu-id="03bd7-155">たとえば、ECCN コード *3A001* の場合、この値は *3* になります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-155">For example, for the ECCN code *3A001*, this value is *3*.</span></span> |
    | <span data-ttu-id="03bd7-156">デュアル ユースのグループ</span><span class="sxs-lookup"><span data-stu-id="03bd7-156">Dual use group</span></span> | <span data-ttu-id="03bd7-157">ECCN コードの製品グループ部分を入力します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-157">Enter the product group part of the ECCN code.</span></span> <span data-ttu-id="03bd7-158">たとえば、ECCN コード *3A001* の場合、この値は *A* になります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-158">For example, for the ECCN code *3A001*, this value is *A*.</span></span> |
    | <span data-ttu-id="03bd7-159">デュアル ユースの政府</span><span class="sxs-lookup"><span data-stu-id="03bd7-159">Dual use regime</span></span> | <span data-ttu-id="03bd7-160">品目の対象となる政府を入力してください。</span><span class="sxs-lookup"><span data-stu-id="03bd7-160">Enter the regime code for the item.</span></span> <span data-ttu-id="03bd7-161">このコードは、品目がデュアルユース商品として分類されている理由を識別します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-161">This code identifies the reason why the item is classified as a dual-use good.</span></span> <span data-ttu-id="03bd7-162">たとえば、ECCN コード *3A001* の場合、この値は *001* になります。</span><span class="sxs-lookup"><span data-stu-id="03bd7-162">For example, for the ECCN code *3A001*, this value is *001*.</span></span> |

## <a name="apply-dual-use-categories-to-products"></a><span data-ttu-id="03bd7-163">製品にデュアルユースのカテゴリを適用する</span><span class="sxs-lookup"><span data-stu-id="03bd7-163">Apply dual-use categories to products</span></span>

<span data-ttu-id="03bd7-164">製品をデュアルユースの商品として識別し、デュアルユースのカテゴリーを適用するには、以下の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="03bd7-164">To identify a product as a dual-use good and apply a dual-use category to it, follow these steps.</span></span>

1. <span data-ttu-id="03bd7-165">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-165">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="03bd7-166">製品を選択、または作成して、 **リリース済み製品の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-166">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="03bd7-167">**対外貿易** クイックタブで、**デュアルユース製品** オプションを **はい** に設定し、現在の製品をデュアルユース商品をして識別します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-167">On the **Foreign trade** FastTab, set the **Dual use products** option to **Yes** to identify the current product as a dual-use good.</span></span>
1. <span data-ttu-id="03bd7-168">現在の製品に適用されるコードを、**デュアル ユース コード** フィールドに設定します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-168">Set the **Dual use code** field to the code that applies to the current product.</span></span> <span data-ttu-id="03bd7-169">(このコードは **デュアル ユースのカテゴリ** ページで定義されています。)</span><span class="sxs-lookup"><span data-stu-id="03bd7-169">(You defined this code on the **Dual use categories** page.)</span></span>

<span data-ttu-id="03bd7-170">この設定は、販売注文を作成する際に確認されます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-170">This setup is checked when you create a sales order.</span></span>

## <a name="set-up-dual-use-certificates"></a><span data-ttu-id="03bd7-171">デュアルユースの証明書を設定する</span><span class="sxs-lookup"><span data-stu-id="03bd7-171">Set up dual-use certificates</span></span>

<span data-ttu-id="03bd7-172">**デュアルユースの証明書** ページを使用して、製品や国ごとに必要なデュアルユース証明書を設定して管理します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-172">You use the **Dual use certificates** page to set up and manage the required dual-use certificates for each product and country.</span></span> <span data-ttu-id="03bd7-173">各証明書の詳細 (国や有効期間など) を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-173">You can track each certificate's details, such as the country and the dates of validity.</span></span> <span data-ttu-id="03bd7-174">オプションを設定して、この情報を印刷する場所を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-174">You can also set options to specify where this information should be printed.</span></span> <span data-ttu-id="03bd7-175">たとえば、この情報は、請求書、梱包明細、および／または販売注文書に印刷できます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-175">For example, the information can be printed on the invoice, packing slip, and/or sales order.</span></span> <span data-ttu-id="03bd7-176">この設定は、販売注文を作成する際に確認されます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-176">This setup is checked when you create a sales order.</span></span>

1. <span data-ttu-id="03bd7-177">**製品情報管理 \> 設定 \> 製品コンプライアンス \> デュアルユース製品 \>デュアルユースの証明書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-177">Go to **Product information management \> Setup \> Product compliance \> Dual use products \> Dual use certificates**.</span></span>
2. <span data-ttu-id="03bd7-178">既存の証明書の設定を選択して編集するか、またはアクション ペインで **新規** を選択して新しい証明書の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-178">Select an existing certificate to edit it, or select **New** on the Action Pane to create a new certificate.</span></span>
3. <span data-ttu-id="03bd7-179">選択された証明書、または新しい証明書に対して以下の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-179">Set the following values for the selected or new certificate.</span></span>

    | <span data-ttu-id="03bd7-180">フィールド</span><span class="sxs-lookup"><span data-stu-id="03bd7-180">Field</span></span> | <span data-ttu-id="03bd7-181">説明</span><span class="sxs-lookup"><span data-stu-id="03bd7-181">Description</span></span> |
    |---|---|
    | <span data-ttu-id="03bd7-182">品目番号</span><span class="sxs-lookup"><span data-stu-id="03bd7-182">Item number</span></span> | <span data-ttu-id="03bd7-183">この証明書が適用されるデュアルユース商品の品目番号を選択してください。</span><span class="sxs-lookup"><span data-stu-id="03bd7-183">Select the item number of the dual-use good that this certificate applies to.</span></span> |
    | <span data-ttu-id="03bd7-184">国/地域</span><span class="sxs-lookup"><span data-stu-id="03bd7-184">Country/region</span></span> | <span data-ttu-id="03bd7-185">この証明書を使用刷る必要のある配送先の国、または地域。</span><span class="sxs-lookup"><span data-stu-id="03bd7-185">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="03bd7-186">証明書番号</span><span class="sxs-lookup"><span data-stu-id="03bd7-186">Certificate number</span></span> | <span data-ttu-id="03bd7-187">仕入先または顧客に発行される証明書に表示される番号。</span><span class="sxs-lookup"><span data-stu-id="03bd7-187">The number that appears on the certificate that is issued to the vendor or customer.</span></span> |
    | <span data-ttu-id="03bd7-188">開始</span><span class="sxs-lookup"><span data-stu-id="03bd7-188">Effective</span></span> | <span data-ttu-id="03bd7-189">現在の証明書が有効となる最初の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-189">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="03bd7-190">有効期限</span><span class="sxs-lookup"><span data-stu-id="03bd7-190">Expiration</span></span> | <span data-ttu-id="03bd7-191">現在の証明書が有効となる最終日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="03bd7-191">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="03bd7-192">請求書に印刷する</span><span class="sxs-lookup"><span data-stu-id="03bd7-192">Print on invoice</span></span> | <span data-ttu-id="03bd7-193">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が請求書に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-193">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="03bd7-194">梱包明細に印刷する</span><span class="sxs-lookup"><span data-stu-id="03bd7-194">Print on packing slip</span></span> | <span data-ttu-id="03bd7-195">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が梱包明細に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-195">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="03bd7-196">販売注文書に印刷する</span><span class="sxs-lookup"><span data-stu-id="03bd7-196">Print on sales order</span></span> | <span data-ttu-id="03bd7-197">このチェック ボックスをオンにすると、指定された日付の範囲で、指定された国に対応する証明書番号が販売注文書に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="03bd7-197">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
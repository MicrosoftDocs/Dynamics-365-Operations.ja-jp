---
title: "データのインポート/エクスポート フレームワーク サービスのデモ ファイル"
description: "このトピックでは、データ インポート/エクスポート フレームワーク (DIXF)のデモ ファイルとそれに対応するエンティティの一覧を示します。"
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 29921
ms.assetid: 70033f55-eddd-4e5a-8f91-5e8670d104c5
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 30ad3e50b1a018266a51dd28e4f16927cdb421f7
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="demo-files-for-the-data-importexport-framework"></a><span data-ttu-id="633d5-103">データのインポート/エクスポート フレームワーク サービスのデモ ファイル</span><span class="sxs-lookup"><span data-stu-id="633d5-103">Demo files for the Data import/export framework</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="633d5-104">デモ ファイルは、Microsoft Dynamics AX 2012 の Contoso デモデータと共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="633d5-104">The demo files can be used together with the Contoso demo data for Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="633d5-105">具体的には、ファイルは CEU Contoso Entertainment Systems (West) 会社と組み合わせて使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="633d5-105">Specifically, the files are intended to be used together with the CEU Contoso Entertainment Systems (West) company.</span></span>

## <a name="source-data-format-settings-for-demo-files"></a><span data-ttu-id="633d5-106">デモ ファイルのソース データ形式設定</span><span class="sxs-lookup"><span data-stu-id="633d5-106">Source data format settings for demo files</span></span>
<span data-ttu-id="633d5-107">次のテーブルに、ソース データ形式に入力する必要のあるコンフィギュレーション設定を示します。</span><span class="sxs-lookup"><span data-stu-id="633d5-107">The following table lists the configuration settings that you should enter for the source data format.</span></span>

| <span data-ttu-id="633d5-108">設定</span><span class="sxs-lookup"><span data-stu-id="633d5-108">Setting</span></span>                         | <span data-ttu-id="633d5-109">先頭値</span><span class="sxs-lookup"><span data-stu-id="633d5-109">Value</span></span>                                             |
|---------------------------------|---------------------------------------------------|
| <span data-ttu-id="633d5-110">**ファイル形式**</span><span class="sxs-lookup"><span data-stu-id="633d5-110">**File format**</span></span>                 | <span data-ttu-id="633d5-111">区切り</span><span class="sxs-lookup"><span data-stu-id="633d5-111">Delimited</span></span>                                         |
| <span data-ttu-id="633d5-112">**先頭行のヘッダー**</span><span class="sxs-lookup"><span data-stu-id="633d5-112">**First row header**</span></span>            | <span data-ttu-id="633d5-113">選択済</span><span class="sxs-lookup"><span data-stu-id="633d5-113">Selected</span></span>                                          |
| <span data-ttu-id="633d5-114">**行区切り**</span><span class="sxs-lookup"><span data-stu-id="633d5-114">**Row delimiter**</span></span>               | <span data-ttu-id="633d5-115">{CR}{LF}</span><span class="sxs-lookup"><span data-stu-id="633d5-115">{CR}{LF}</span></span>                                          |
| <span data-ttu-id="633d5-116">**列区切り**</span><span class="sxs-lookup"><span data-stu-id="633d5-116">**Column delimiter**</span></span>            | <span data-ttu-id="633d5-117">コンマ {,}</span><span class="sxs-lookup"><span data-stu-id="633d5-117">Comma {,}</span></span>                                         |
| <span data-ttu-id="633d5-118">**テキスト修飾子**</span><span class="sxs-lookup"><span data-stu-id="633d5-118">**Text qualifier**</span></span>              | <span data-ttu-id="633d5-119">"</span><span class="sxs-lookup"><span data-stu-id="633d5-119">"</span></span>                                                 |
| <span data-ttu-id="633d5-120">**コード ページ**</span><span class="sxs-lookup"><span data-stu-id="633d5-120">**Code page**</span></span>                   | <span data-ttu-id="633d5-121">1252 西ヨーロッパ (Windows)</span><span class="sxs-lookup"><span data-stu-id="633d5-121">1252 Western European (Windows)</span></span>                   |
| <span data-ttu-id="633d5-122">**Unicode**</span><span class="sxs-lookup"><span data-stu-id="633d5-122">**Unicode**</span></span>                     | <span data-ttu-id="633d5-123">未選択</span><span class="sxs-lookup"><span data-stu-id="633d5-123">Not selected</span></span>                                      |
| <span data-ttu-id="633d5-124">**言語ロケール**</span><span class="sxs-lookup"><span data-stu-id="633d5-124">**Language locale**</span></span>             | <span data-ttu-id="633d5-125">ja</span><span class="sxs-lookup"><span data-stu-id="633d5-125">en-us</span></span>                                             |
| <span data-ttu-id="633d5-126">**分析コード**</span><span class="sxs-lookup"><span data-stu-id="633d5-126">**Dimension code**</span></span>              | <span data-ttu-id="633d5-127">CostCenter、Department、または ExpensePurpose を選択します。</span><span class="sxs-lookup"><span data-stu-id="633d5-127">Select CostCenter, Department, or ExpensePurpose.</span></span> |
| <span data-ttu-id="633d5-128">**勘定科目表の区切り記号**</span><span class="sxs-lookup"><span data-stu-id="633d5-128">**Chart of accounts delimiter**</span></span> | -                                                 |



## <a name="file-list"></a><span data-ttu-id="633d5-129">ファイル リスト</span><span class="sxs-lookup"><span data-stu-id="633d5-129">File list</span></span>
<span data-ttu-id="633d5-130">次のテーブルに、各エンティティに関連付けられているデモ ファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="633d5-130">The following table lists the demo files that are associated with each entity.</span></span>

<span data-ttu-id="633d5-131">**名前**</span><span class="sxs-lookup"><span data-stu-id="633d5-131">**Name**</span></span>

<span data-ttu-id="633d5-132">**Dynamics AX バージョン**</span><span class="sxs-lookup"><span data-stu-id="633d5-132">**Dynamics AX version**</span></span>

<span data-ttu-id="633d5-133">**デモ ファイル**</span><span class="sxs-lookup"><span data-stu-id="633d5-133">**Demo files**</span></span>

<span data-ttu-id="633d5-134">AIF</span><span class="sxs-lookup"><span data-stu-id="633d5-134">AIF</span></span>

<span data-ttu-id="633d5-135">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-135">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-136">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-136">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-137">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-137">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-138">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-138">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-139">·         AifInboundPortEntity ·         AifLookupEntryEntity ·         AifOutboundPortEntity ·         AIfWebSitesEntity ·         CustVendAIFPaymTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-139">·         AifInboundPortEntity ·         AifLookupEntryEntity ·         AifOutboundPortEntity ·         AIfWebSitesEntity ·         CustVendAIFPaymTableEntity</span></span>

<span data-ttu-id="633d5-140">資産</span><span class="sxs-lookup"><span data-stu-id="633d5-140">Asset</span></span>

<span data-ttu-id="633d5-141">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-141">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-142">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span><span class="sxs-lookup"><span data-stu-id="633d5-142">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span></span>

<span data-ttu-id="633d5-143">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-143">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-144">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span><span class="sxs-lookup"><span data-stu-id="633d5-144">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span></span>

<span data-ttu-id="633d5-145">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-145">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-146">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-146">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL</span></span>

<span data-ttu-id="633d5-147">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-147">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-148">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL ·         AssetParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-148">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL ·         AssetParametersEntity</span></span>

<span data-ttu-id="633d5-149">属性タイプ</span><span class="sxs-lookup"><span data-stu-id="633d5-149">Attribute types</span></span>

<span data-ttu-id="633d5-150">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-150">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-151">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-151">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="633d5-152">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-152">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-153">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-153">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="633d5-154">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-154">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-155">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-155">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="633d5-156">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-156">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-157">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-157">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="633d5-158">属性</span><span class="sxs-lookup"><span data-stu-id="633d5-158">Attributes</span></span>

<span data-ttu-id="633d5-159">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-159">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-160">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-160">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="633d5-161">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-161">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-162">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-162">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="633d5-163">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-163">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-164">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-164">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="633d5-165">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-165">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-166">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-166">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="633d5-167">監査ポリシー</span><span class="sxs-lookup"><span data-stu-id="633d5-167">Audit policy</span></span>

<span data-ttu-id="633d5-168">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-168">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-169">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-169">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-170">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-170">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-171">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-171">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-172">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-172">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-173">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-173">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-174">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-174">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-175">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-175">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-176">銀行パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-176">Bank parameters</span></span>

<span data-ttu-id="633d5-177">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-177">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-178">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-178">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-179">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-179">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-180">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-180">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-181">·         BankParametersEnitty</span><span class="sxs-lookup"><span data-stu-id="633d5-181">·         BankParametersEnitty</span></span>

<span data-ttu-id="633d5-182">BarcodeSetup</span><span class="sxs-lookup"><span data-stu-id="633d5-182">BarcodeSetup</span></span>

<span data-ttu-id="633d5-183">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-183">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-184">·         BarCodeSetupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-184">·         BarCodeSetupEntity\_Basic</span></span>

<span data-ttu-id="633d5-185">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-185">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-186">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span><span class="sxs-lookup"><span data-stu-id="633d5-186">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span></span>

<span data-ttu-id="633d5-187">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-187">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-188">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span><span class="sxs-lookup"><span data-stu-id="633d5-188">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span></span>

<span data-ttu-id="633d5-189">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-189">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-190">バッチ グループ</span><span class="sxs-lookup"><span data-stu-id="633d5-190">Batch group</span></span>

<span data-ttu-id="633d5-191">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-191">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-192">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-192">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-193">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-193">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-194">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-194">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-195">·         BatchGroupEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-195">·         BatchGroupEntity</span></span>

<span data-ttu-id="633d5-196">BOM</span><span class="sxs-lookup"><span data-stu-id="633d5-196">BOM</span></span>

<span data-ttu-id="633d5-197">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-197">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-198">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-198">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span></span>

<span data-ttu-id="633d5-199">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-199">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-200">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-200">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span></span>

<span data-ttu-id="633d5-201">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-201">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-202">·         BOMEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-202">·         BOMEntity\_Basic</span></span>

<span data-ttu-id="633d5-203">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-203">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-204">·         BOMEntity ·         BOMEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-204">·         BOMEntity ·         BOMEntity\_Basic</span></span>

<span data-ttu-id="633d5-205">BOMVersion</span><span class="sxs-lookup"><span data-stu-id="633d5-205">BOMVersion</span></span>

<span data-ttu-id="633d5-206">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-206">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-207">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-207">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span></span>

<span data-ttu-id="633d5-208">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-208">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-209">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-209">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span></span>

<span data-ttu-id="633d5-210">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-210">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-211">·         BOMVersionEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-211">·         BOMVersionEntity\_Basic</span></span>

<span data-ttu-id="633d5-212">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-212">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-213">·         BOMVersionEntity ·         BOMVersionEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-213">·         BOMVersionEntity ·         BOMVersionEntity\_Basic</span></span>

<span data-ttu-id="633d5-214">予算</span><span class="sxs-lookup"><span data-stu-id="633d5-214">Budget</span></span>

<span data-ttu-id="633d5-215">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-215">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-216">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-216">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-217">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-217">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-218">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-218">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-219">·         BudgetParametersEntity ·         BudgetTransactionLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-219">·         BudgetParametersEntity ·         BudgetTransactionLineEntity</span></span>

<span data-ttu-id="633d5-220">ビジネス インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="633d5-220">Business intelligence</span></span>

<span data-ttu-id="633d5-221">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-221">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-222">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-222">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-223">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-223">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-224">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-224">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-225">·         BIConfigruationEntity ·         BITimePeriodsMDXEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-225">·         BIConfigruationEntity ·         BITimePeriodsMDXEntity</span></span>

<span data-ttu-id="633d5-226">ケースのワークフロー</span><span class="sxs-lookup"><span data-stu-id="633d5-226">Case workflow</span></span>

<span data-ttu-id="633d5-227">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-227">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-228">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-228">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="633d5-229">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-229">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-230">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-230">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="633d5-231">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-231">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-232">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-232">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="633d5-233">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-233">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-234">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-234">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="633d5-235">カテゴリ階層</span><span class="sxs-lookup"><span data-stu-id="633d5-235">Category hierarchies</span></span>

<span data-ttu-id="633d5-236">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-236">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-237">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-237">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>  

<span data-ttu-id="633d5-238">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-238">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-239">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-239">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>

<span data-ttu-id="633d5-240">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-240">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-241">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-241">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>

<span data-ttu-id="633d5-242">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-242">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-243">·         EcoResAttributeEntity ·         EcoResAttributeTypeEntity ·         EcoResCategoryHierarchyEntity ·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-243">·         EcoResAttributeEntity ·         EcoResAttributeTypeEntity ·         EcoResCategoryHierarchyEntity ·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>

<span data-ttu-id="633d5-244">カテゴリ テーブル</span><span class="sxs-lookup"><span data-stu-id="633d5-244">Category table</span></span>

<span data-ttu-id="633d5-245">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-245">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-246">·         CategoryTableEntity\_Project</span><span class="sxs-lookup"><span data-stu-id="633d5-246">·         CategoryTableEntity\_Project</span></span>

<span data-ttu-id="633d5-247">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-247">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-248">·         CategoryTableEntity\_Project</span><span class="sxs-lookup"><span data-stu-id="633d5-248">·         CategoryTableEntity\_Project</span></span>

<span data-ttu-id="633d5-249">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-249">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-250">·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span><span class="sxs-lookup"><span data-stu-id="633d5-250">·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span></span>

<span data-ttu-id="633d5-251">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-251">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-252">·         CategoryTableEntity ·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span><span class="sxs-lookup"><span data-stu-id="633d5-252">·         CategoryTableEntity ·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span></span>

<span data-ttu-id="633d5-253">勘定構造のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="633d5-253">Configure account structures</span></span>

<span data-ttu-id="633d5-254">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-254">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-255">·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-255">·         DimensionHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-256">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-256">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-257">·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-257">·         DimensionHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-258">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-258">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-259">·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-259">·         DimensionHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-260">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-260">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-261">·         DimensionHierarchyEntity ·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-261">·         DimensionHierarchyEntity ·         DimensionHierarchyEntity\_Basic</span></span>

  <span data-ttu-id="633d5-262">ContactPerson</span><span class="sxs-lookup"><span data-stu-id="633d5-262">ContactPerson</span></span>

<span data-ttu-id="633d5-263">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-263">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-264">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-264">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span></span>

<span data-ttu-id="633d5-265">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-265">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-266">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-266">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span></span>

<span data-ttu-id="633d5-267">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-267">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-268">·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-268">·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="633d5-269">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-269">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-270">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-270">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="633d5-271">ContactPersonAddress</span><span class="sxs-lookup"><span data-stu-id="633d5-271">ContactPersonAddress</span></span>

<span data-ttu-id="633d5-272">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-272">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-273">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-273">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="633d5-274">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-274">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-275">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-275">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="633d5-276">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-276">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-277">·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-277">·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="633d5-278">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-278">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-279">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-279">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="633d5-280">原価会計パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-280">Cost accounting parameters</span></span>

<span data-ttu-id="633d5-281">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-281">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-282">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-282">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-283">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-283">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-284">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-284">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-285">·         COSParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-285">·         COSParametersEntity</span></span>

  <span data-ttu-id="633d5-286">顧客</span><span class="sxs-lookup"><span data-stu-id="633d5-286">Customer</span></span>

<span data-ttu-id="633d5-287">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-287">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-288">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span><span class="sxs-lookup"><span data-stu-id="633d5-288">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span></span>

<span data-ttu-id="633d5-289">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-289">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-290">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span><span class="sxs-lookup"><span data-stu-id="633d5-290">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span></span>

<span data-ttu-id="633d5-291">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-291">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-292">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-292">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span></span>

<span data-ttu-id="633d5-293">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-293">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-294">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-294">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span></span>

<span data-ttu-id="633d5-295">顧客の住所</span><span class="sxs-lookup"><span data-stu-id="633d5-295">Customer address</span></span>

<span data-ttu-id="633d5-296">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-296">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-297">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-297">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="633d5-298">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-298">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-299">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-299">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="633d5-300">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-300">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-301">·         CustomerAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-301">·         CustomerAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-302">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-302">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-303">·         CustomerAddressEntity ·         CustomerAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-303">·         CustomerAddressEntity ·         CustomerAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-304">部門</span><span class="sxs-lookup"><span data-stu-id="633d5-304">Departments</span></span>

<span data-ttu-id="633d5-305">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-305">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-306">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-306">·         DepartmentEntity\_Basic</span></span>

<span data-ttu-id="633d5-307">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-307">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-308">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-308">·         DepartmentEntity\_Basic</span></span>

<span data-ttu-id="633d5-309">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-309">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-310">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-310">·         DepartmentEntity\_Basic</span></span>

<span data-ttu-id="633d5-311">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-311">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-312">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-312">·         DepartmentEntity\_Basic</span></span>

  <span data-ttu-id="633d5-313">分析コード</span><span class="sxs-lookup"><span data-stu-id="633d5-313">Dimensions</span></span>

<span data-ttu-id="633d5-314">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-314">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-315">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-315">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span></span>

<span data-ttu-id="633d5-316">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-316">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-317">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-317">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span></span>

<span data-ttu-id="633d5-318">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-318">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-319">·         DimensionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-319">·         DimensionsEntity\_Basic</span></span>

<span data-ttu-id="633d5-320">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-320">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-321">·         DimensionAttributeValueEntity ·         DimensionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-321">·         DimensionAttributeValueEntity ·         DimensionsEntity\_Basic</span></span>

  <span data-ttu-id="633d5-322">DocuType</span><span class="sxs-lookup"><span data-stu-id="633d5-322">DocuType</span></span>

<span data-ttu-id="633d5-323">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-323">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-324">·         DocuTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-324">·         DocuTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-325">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-325">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-326">·         DocuTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-326">·         DocuTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-327">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-327">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-328">·         DocuTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-328">·         DocuTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-329">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-329">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-330">·         DocuTypeEntity ·         DocuTypeEntity\_Basic ·         DocuTableEnabledEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-330">·         DocuTypeEntity ·         DocuTypeEntity\_Basic ·         DocuTableEnabledEntity</span></span>

  <span data-ttu-id="633d5-331">ドキュメント管理</span><span class="sxs-lookup"><span data-stu-id="633d5-331">Document management</span></span>

<span data-ttu-id="633d5-332">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-332">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-333">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-333">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-334">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-334">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-335">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-335">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-336">·         CollabSiteParametersEntity ·         ContentTypeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-336">·         CollabSiteParametersEntity ·         ContentTypeEntity</span></span>

<span data-ttu-id="633d5-337">電子署名</span><span class="sxs-lookup"><span data-stu-id="633d5-337">Electronic signatures</span></span>

<span data-ttu-id="633d5-338">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-338">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-339">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-339">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-340">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-340">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-341">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-341">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-342">·         SIGParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-342">·         SIGParametersEntity</span></span>

<span data-ttu-id="633d5-343">従業員</span><span class="sxs-lookup"><span data-stu-id="633d5-343">Employee</span></span>

<span data-ttu-id="633d5-344">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-344">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-345">·         EmployeeEntity\_Address ·         EmployeeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-345">·         EmployeeEntity\_Address ·         EmployeeEntity\_Basic</span></span>

<span data-ttu-id="633d5-346">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-346">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-347">·         EmployeeEntity\_Address ·         EmployeeEntityBasic</span><span class="sxs-lookup"><span data-stu-id="633d5-347">·         EmployeeEntity\_Address ·         EmployeeEntityBasic</span></span>

<span data-ttu-id="633d5-348">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-348">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-349">·         EmployeeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-349">·         EmployeeEntity\_Basic</span></span>

<span data-ttu-id="633d5-350">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-350">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-351">·         EmployeeEntity ·         EmployeeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-351">·         EmployeeEntity ·         EmployeeEntity\_Basic</span></span>

<span data-ttu-id="633d5-352">従業員の住所</span><span class="sxs-lookup"><span data-stu-id="633d5-352">Employee address</span></span>

<span data-ttu-id="633d5-353">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-353">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-354">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-354">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="633d5-355">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-355">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-356">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-356">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="633d5-357">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-357">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-358">·         EmployeeAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-358">·         EmployeeAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-359">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-359">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-360">·         EmployeeAddressEntity ·         EmployeeAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-360">·         EmployeeAddressEntity ·         EmployeeAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-361">エンタープライズ ポータル</span><span class="sxs-lookup"><span data-stu-id="633d5-361">Enterprise Portal</span></span>

<span data-ttu-id="633d5-362">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-362">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-363">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-363">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-364">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-364">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-365">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-365">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-366">·         EPDocuParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-366">·         EPDocuParametersEntity</span></span>

  <span data-ttu-id="633d5-367">環境的持続可能なパラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-367">Environmental sustainability parameter</span></span>

<span data-ttu-id="633d5-368">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-368">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-369">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-369">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-370">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-370">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-371">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-371">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-372">·         EMSParameterEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-372">·         EMSParameterEntity</span></span>

<span data-ttu-id="633d5-373">経費精算書パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-373">Expense report parameters</span></span>

<span data-ttu-id="633d5-374">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-374">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-375">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-375">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-376">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-376">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-377">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-377">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-378">·         TrvParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-378">·         TrvParametersEntity</span></span>

<span data-ttu-id="633d5-379">経費精算書の委任</span><span class="sxs-lookup"><span data-stu-id="633d5-379">Expense report delegation</span></span>

<span data-ttu-id="633d5-380">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-380">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-381">·         TrvAppEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-381">·         TrvAppEmplSubEntity\_Basic</span></span>

<span data-ttu-id="633d5-382">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-382">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-383">·         TrvAppEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-383">·         TrvAppEmplSubEntity\_Basic</span></span>

<span data-ttu-id="633d5-384">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-384">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-385">·         TrvApEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-385">·         TrvApEmplSubEntity\_Basic</span></span>

<span data-ttu-id="633d5-386">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-386">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-387">·         TrvAppEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-387">·         TrvAppEmplSubEntity\_Basic</span></span>

<span data-ttu-id="633d5-388">経費精算書のコスト</span><span class="sxs-lookup"><span data-stu-id="633d5-388">Expense report cost</span></span>

<span data-ttu-id="633d5-389">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-389">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-390">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-390">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-391">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-391">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-392">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-392">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-393">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-393">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-394">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-394">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-395">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-395">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-396">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-396">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="633d5-397">経費精算書カテゴリ</span><span class="sxs-lookup"><span data-stu-id="633d5-397">Expense report category</span></span>

<span data-ttu-id="633d5-398">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-398">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-399">·         TrvExpSubCateogoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-399">·         TrvExpSubCateogoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-400">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-400">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-401">·         TrvExpSubCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-401">·         TrvExpSubCategoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-402">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-402">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-403">·         TrvExpSubCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-403">·         TrvExpSubCategoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-404">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-404">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-405">·         TrvExpSubCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-405">·         TrvExpSubCategoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-406">経費精算書の支払方法</span><span class="sxs-lookup"><span data-stu-id="633d5-406">Expense report payment method</span></span>

<span data-ttu-id="633d5-407">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-407">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-408">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-408">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="633d5-409">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-409">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-410">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-410">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="633d5-411">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-411">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-412">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-412">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="633d5-413">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-413">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-414">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-414">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="633d5-415">経費精算書カテゴリのコード マッピング</span><span class="sxs-lookup"><span data-stu-id="633d5-415">Expense report category code mapping</span></span>

<span data-ttu-id="633d5-416">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-416">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-417">·         TrvPBSCatCodesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-417">·         TrvPBSCatCodesEntity\_Basic</span></span>

<span data-ttu-id="633d5-418">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-418">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-419">·         TrvPBSCatCodesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-419">·         TrvPBSCatCodesEntity\_Basic</span></span>

<span data-ttu-id="633d5-420">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-420">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-421">·         TrvPBSCatCodeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-421">·         TrvPBSCatCodeEntity\_Basic</span></span>

<span data-ttu-id="633d5-422">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-422">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-423">·         TrvPBSCatCodesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-423">·         TrvPBSCatCodesEntity\_Basic</span></span>

<span data-ttu-id="633d5-424">経費精算書ポリシー</span><span class="sxs-lookup"><span data-stu-id="633d5-424">Expense report policy</span></span>

<span data-ttu-id="633d5-425">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-425">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-426">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-426">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-427">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-427">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-428">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-428">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-429">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-429">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-430">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-430">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-431">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-431">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-432">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-432">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="633d5-433">経費精算書の検証方法</span><span class="sxs-lookup"><span data-stu-id="633d5-433">Expense report validate payment</span></span>

<span data-ttu-id="633d5-434">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-434">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-435">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-435">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="633d5-436">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-436">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-437">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-437">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="633d5-438">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-438">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-439">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-439">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="633d5-440">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-440">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-441">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-441">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="633d5-442">対外貿易</span><span class="sxs-lookup"><span data-stu-id="633d5-442">Foreign trade</span></span>

<span data-ttu-id="633d5-443">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-443">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-444">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-444">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-445">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-445">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-446">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-446">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-447">·         InstrastatStatParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-447">·         InstrastatStatParametersEntity</span></span>

<span data-ttu-id="633d5-448">グローバル アドレス帳パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-448">Global address book parameters</span></span>

<span data-ttu-id="633d5-449">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-449">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-450">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-450">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-451">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-451">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-452">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-452">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-453">·         DirParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-453">·         DirParametersEntity</span></span>

<span data-ttu-id="633d5-454">人事管理</span><span class="sxs-lookup"><span data-stu-id="633d5-454">Human resources</span></span>

<span data-ttu-id="633d5-455">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-455">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-456">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-456">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-457">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-457">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-458">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-458">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-459">·         HRMParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-459">·         HRMParametersEntity</span></span>

<span data-ttu-id="633d5-460">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="633d5-460">Inventory</span></span>

<span data-ttu-id="633d5-461">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-461">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-462">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="633d5-462">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span></span>

<span data-ttu-id="633d5-463">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-463">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-464">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="633d5-464">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span></span>

<span data-ttu-id="633d5-465">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-465">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-466">·         InventJournalEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-466">·         InventJournalEntity\_RU</span></span>

<span data-ttu-id="633d5-467">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-467">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-468">·         InventJournalEntity ·         InventJournalEntity\_RU ·         InventParametersEntity ·         InventTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-468">·         InventJournalEntity ·         InventJournalEntity\_RU ·         InventParametersEntity ·         InventTableEntity</span></span>

<span data-ttu-id="633d5-469">在庫在庫の計量単位</span><span class="sxs-lookup"><span data-stu-id="633d5-469">Inventory Inventory unit of measure</span></span>

<span data-ttu-id="633d5-470">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-470">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-471">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-471">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span></span>

<span data-ttu-id="633d5-472">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-472">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-473">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-473">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span></span>

<span data-ttu-id="633d5-474">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-474">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-475">·         UnitOfMeasureEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-475">·         UnitOfMeasureEntity\_Basic</span></span>

<span data-ttu-id="633d5-476">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-476">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-477">·         UnitOfMeasureEntity ·         UnitOfMeasureEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-477">·         UnitOfMeasureEntity ·         UnitOfMeasureEntity\_Basic</span></span>

<span data-ttu-id="633d5-478">職務</span><span class="sxs-lookup"><span data-stu-id="633d5-478">Jobs</span></span>

<span data-ttu-id="633d5-479">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-479">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-480">·         HcmJobDetailsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-480">·         HcmJobDetailsEntity\_Basic</span></span>

<span data-ttu-id="633d5-481">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-481">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-482">·         HcmJobDetailsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-482">·         HcmJobDetailsEntity\_Basic</span></span>

<span data-ttu-id="633d5-483">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-483">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-484">·         HcmJobDetailsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-484">·         HcmJobDetailsEntity\_Basic</span></span>

<span data-ttu-id="633d5-485">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-485">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-486">·         HcmJobDetailEntity ·         HcmJobDetailsEntity\_Basic ·         HcmPositionDetailEntity ·         HcmSharedParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-486">·         HcmJobDetailEntity ·         HcmJobDetailsEntity\_Basic ·         HcmPositionDetailEntity ·         HcmSharedParametersEntity</span></span>

  <span data-ttu-id="633d5-487">Ledger</span><span class="sxs-lookup"><span data-stu-id="633d5-487">Ledger</span></span>

<span data-ttu-id="633d5-488">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-488">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-489">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span><span class="sxs-lookup"><span data-stu-id="633d5-489">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span></span>

<span data-ttu-id="633d5-490">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-490">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-491">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span><span class="sxs-lookup"><span data-stu-id="633d5-491">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span></span>

<span data-ttu-id="633d5-492">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-492">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-493">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-493">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU</span></span>

<span data-ttu-id="633d5-494">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-494">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-495">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU ·         LedgerParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-495">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU ·         LedgerParametersEntity</span></span>

<span data-ttu-id="633d5-496">主勘定</span><span class="sxs-lookup"><span data-stu-id="633d5-496">Main account</span></span>

<span data-ttu-id="633d5-497">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-497">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-498">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span><span class="sxs-lookup"><span data-stu-id="633d5-498">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span></span>

<span data-ttu-id="633d5-499">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-499">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-500">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span><span class="sxs-lookup"><span data-stu-id="633d5-500">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span></span>

<span data-ttu-id="633d5-501">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-501">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-502">·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span><span class="sxs-lookup"><span data-stu-id="633d5-502">·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span></span>

<span data-ttu-id="633d5-503">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-503">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-504">·         MainAccountEntity ·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span><span class="sxs-lookup"><span data-stu-id="633d5-504">·         MainAccountEntity ·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span></span>

<span data-ttu-id="633d5-505">マイレージ レート層</span><span class="sxs-lookup"><span data-stu-id="633d5-505">Mileage rate tiers</span></span>

<span data-ttu-id="633d5-506">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-506">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-507">·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-507">·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="633d5-508">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-508">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-509">·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-509">·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="633d5-510">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-510">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-511">·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-511">·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="633d5-512">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-512">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-513">·         TrvCostTypeRatesEntity ·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-513">·         TrvCostTypeRatesEntity ·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="633d5-514">整理番号</span><span class="sxs-lookup"><span data-stu-id="633d5-514">Number sequence</span></span>

<span data-ttu-id="633d5-515">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-515">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-516">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-516">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-517">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-517">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-518">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-518">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-519">·         NumberSequenceTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-519">·         NumberSequenceTableEntity</span></span>

<span data-ttu-id="633d5-520">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="633d5-520">Office Add-ins</span></span>

<span data-ttu-id="633d5-521">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-521">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-522">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-522">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-523">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-523">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-524">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-524">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-525">·         DocuDataSourceEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-525">·         DocuDataSourceEntity</span></span>

<span data-ttu-id="633d5-526">Operations リソース</span><span class="sxs-lookup"><span data-stu-id="633d5-526">Operations resources</span></span>

<span data-ttu-id="633d5-527">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-527">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-528">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-528">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-529">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-529">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-530">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-530">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-531">·         WrkCtrParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-531">·         WrkCtrParametersEntity</span></span>

<span data-ttu-id="633d5-532">組織</span><span class="sxs-lookup"><span data-stu-id="633d5-532">Organization</span></span>

<span data-ttu-id="633d5-533">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-533">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-534">·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-534">·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-535">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-535">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-536">·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-536">·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-537">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-537">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-538">·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-538">·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-539">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-539">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-540">·         OMHierarchyEntity ·         OMOperatingUnitEntity ·         OrganizationHierarchyEntity ·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-540">·         OMHierarchyEntity ·         OMOperatingUnitEntity ·         OrganizationHierarchyEntity ·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="633d5-541">Outlook</span><span class="sxs-lookup"><span data-stu-id="633d5-541">Outlook</span></span>

<span data-ttu-id="633d5-542">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-542">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-543">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-543">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-544">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-544">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-545">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-545">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-546">·         SmmParametersTableEntity ·         SysEmailParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-546">·         SmmParametersTableEntity ·         SysEmailParametersEntity</span></span>

<span data-ttu-id="633d5-547">Payroll</span><span class="sxs-lookup"><span data-stu-id="633d5-547">Payroll</span></span>

<span data-ttu-id="633d5-548">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-548">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-549">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-549">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-550">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-550">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-551">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-551">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-552">·         PRLPayrollParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-552">·         PRLPayrollParametersEntity</span></span>

<span data-ttu-id="633d5-553">ポリシー</span><span class="sxs-lookup"><span data-stu-id="633d5-553">Policies</span></span>

<span data-ttu-id="633d5-554">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-554">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-555">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-555">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-556">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-556">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-557">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-557">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-558">·         SysPolicySourceDocumentRuleEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-558">·         SysPolicySourceDocumentRuleEntity</span></span>

<span data-ttu-id="633d5-559">職位</span><span class="sxs-lookup"><span data-stu-id="633d5-559">Positions</span></span>

<span data-ttu-id="633d5-560">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-560">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-561">·         PositionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-561">·         PositionsEntity\_Basic</span></span>

<span data-ttu-id="633d5-562">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-562">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-563">·         PostionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-563">·         PostionsEntity\_Basic</span></span>

<span data-ttu-id="633d5-564">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-564">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-565">·         PositionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-565">·         PositionsEntity\_Basic</span></span>

<span data-ttu-id="633d5-566">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-566">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-567">·         PositionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-567">·         PositionsEntity\_Basic</span></span>

<span data-ttu-id="633d5-568">PriceDiscount</span><span class="sxs-lookup"><span data-stu-id="633d5-568">PriceDiscount</span></span>

<span data-ttu-id="633d5-569">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-569">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-570">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span><span class="sxs-lookup"><span data-stu-id="633d5-570">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span></span>

<span data-ttu-id="633d5-571">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-571">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-572">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span><span class="sxs-lookup"><span data-stu-id="633d5-572">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span></span>

<span data-ttu-id="633d5-573">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-573">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-574">·         PriceDiscountEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-574">·         PriceDiscountEntity\_RU</span></span>

<span data-ttu-id="633d5-575">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-575">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-576">·         PriceDiscAdmTransEntity ·         PriceDiscountEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-576">·         PriceDiscAdmTransEntity ·         PriceDiscountEntity\_RU</span></span>

<span data-ttu-id="633d5-577">品目</span><span class="sxs-lookup"><span data-stu-id="633d5-577">Product</span></span>

<span data-ttu-id="633d5-578">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-578">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-579">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchaseSalesInvent</span><span class="sxs-lookup"><span data-stu-id="633d5-579">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchaseSalesInvent</span></span>

<span data-ttu-id="633d5-580">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-580">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-581">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchSalesInvent</span><span class="sxs-lookup"><span data-stu-id="633d5-581">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchSalesInvent</span></span>

<span data-ttu-id="633d5-582">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-582">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-583">·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-583">·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU</span></span>

<span data-ttu-id="633d5-584">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-584">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-585">·         ProdParametersEntity ·         ProductEntity ·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU ·         ProductMasterEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-585">·         ProdParametersEntity ·         ProductEntity ·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU ·         ProductMasterEntity</span></span>

<span data-ttu-id="633d5-586">Project</span><span class="sxs-lookup"><span data-stu-id="633d5-586">Project</span></span>

<span data-ttu-id="633d5-587">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-587">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-588">·         ProjectEtnity\_Basic ·         ProjectEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-588">·         ProjectEtnity\_Basic ·         ProjectEntity\_Enum</span></span>

<span data-ttu-id="633d5-589">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-589">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-590">·         ProjectEntity\_Basic ·         ProjectEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="633d5-590">·         ProjectEntity\_Basic ·         ProjectEntity\_Enum</span></span>

<span data-ttu-id="633d5-591">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-591">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-592">·         ProjectEntity\_PSA</span><span class="sxs-lookup"><span data-stu-id="633d5-592">·         ProjectEntity\_PSA</span></span>

<span data-ttu-id="633d5-593">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-593">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-594">·         ProjectEntity\_PSA ·         ProjInvoiceTableEntity ·         ProjJournalTransEntity ·         ProjOnAccTransEntity ·         ProjServerSettingsEntity ·         ProjTableEntitySyncParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-594">·         ProjectEntity\_PSA ·         ProjInvoiceTableEntity ·         ProjJournalTransEntity ·         ProjOnAccTransEntity ·         ProjServerSettingsEntity ·         ProjTableEntitySyncParametersEntity</span></span>

<span data-ttu-id="633d5-595">ProjectHourJournal</span><span class="sxs-lookup"><span data-stu-id="633d5-595">ProjectHourJournal</span></span>

<span data-ttu-id="633d5-596">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-596">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-597">·         ProjectHourJournalEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-597">·         ProjectHourJournalEntity\_Basic</span></span>

<span data-ttu-id="633d5-598">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-598">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-599">·         ProjectHourJournalEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-599">·         ProjectHourJournalEntity\_Basic</span></span>

<span data-ttu-id="633d5-600">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-600">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-601">·         ProjectHourEntity\_PSA</span><span class="sxs-lookup"><span data-stu-id="633d5-601">·         ProjectHourEntity\_PSA</span></span>

<span data-ttu-id="633d5-602">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-602">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-603">·         ProjectHourEntity\_PSA</span><span class="sxs-lookup"><span data-stu-id="633d5-603">·         ProjectHourEntity\_PSA</span></span>

<span data-ttu-id="633d5-604">PurchLine</span><span class="sxs-lookup"><span data-stu-id="633d5-604">PurchLine</span></span>

<span data-ttu-id="633d5-605">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-605">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-606">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="633d5-606">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span></span>

<span data-ttu-id="633d5-607">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-607">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-608">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="633d5-608">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span></span>

<span data-ttu-id="633d5-609">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-609">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-610">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="633d5-610">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span></span>

<span data-ttu-id="633d5-611">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-611">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-612">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="633d5-612">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span></span>

<span data-ttu-id="633d5-613">PurchTable</span><span class="sxs-lookup"><span data-stu-id="633d5-613">PurchTable</span></span>

<span data-ttu-id="633d5-614">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-614">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-615">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="633d5-615">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span></span>

<span data-ttu-id="633d5-616">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-616">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-617">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="633d5-617">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span></span>

<span data-ttu-id="633d5-618">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-618">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-619">·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-619">·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span></span>

<span data-ttu-id="633d5-620">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-620">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-621">·         PurchTableEntity ·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-621">·         PurchTableEntity ·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span></span>

<span data-ttu-id="633d5-622">工順</span><span class="sxs-lookup"><span data-stu-id="633d5-622">Route</span></span>

<span data-ttu-id="633d5-623">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-623">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-624">·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-624">·         RouteEntity\_Basic</span></span>

<span data-ttu-id="633d5-625">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-625">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-626">·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-626">·         RouteEntity\_Basic</span></span>

<span data-ttu-id="633d5-627">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-627">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-628">·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-628">·         RouteEntity\_Basic</span></span>

<span data-ttu-id="633d5-629">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-629">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-630">·         RouteEntity ·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-630">·         RouteEntity ·         RouteEntity\_Basic</span></span>

<span data-ttu-id="633d5-631">工順工程</span><span class="sxs-lookup"><span data-stu-id="633d5-631">Route operations</span></span>

<span data-ttu-id="633d5-632">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-632">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-633">·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-633">·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="633d5-634">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-634">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-635">·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-635">·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="633d5-636">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-636">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-637">·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-637">·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="633d5-638">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-638">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-639">·         RouteOperationsEntity ·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-639">·         RouteOperationsEntity ·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="633d5-640">SalesLine</span><span class="sxs-lookup"><span data-stu-id="633d5-640">SalesLine</span></span>

<span data-ttu-id="633d5-641">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-641">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-642">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span><span class="sxs-lookup"><span data-stu-id="633d5-642">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span></span>

<span data-ttu-id="633d5-643">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-643">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-644">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span><span class="sxs-lookup"><span data-stu-id="633d5-644">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span></span>

<span data-ttu-id="633d5-645">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-645">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-646">·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="633d5-646">·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span></span>

<span data-ttu-id="633d5-647">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-647">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-648">·         SalesLineEntity ·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="633d5-648">·         SalesLineEntity ·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span></span>

<span data-ttu-id="633d5-649">SalesTable</span><span class="sxs-lookup"><span data-stu-id="633d5-649">SalesTable</span></span>

<span data-ttu-id="633d5-650">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-650">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-651">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span><span class="sxs-lookup"><span data-stu-id="633d5-651">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span></span>

<span data-ttu-id="633d5-652">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-652">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-653">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span><span class="sxs-lookup"><span data-stu-id="633d5-653">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span></span>

<span data-ttu-id="633d5-654">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-654">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-655">·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-655">·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span></span>

<span data-ttu-id="633d5-656">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-656">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-657">·         SalesTableEntity ·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-657">·         SalesTableEntity ·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span></span>

<span data-ttu-id="633d5-658">サービス管理</span><span class="sxs-lookup"><span data-stu-id="633d5-658">Service management</span></span>

<span data-ttu-id="633d5-659">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-659">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-660">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-660">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-661">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-661">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-662">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-662">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-663">·         SmaParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-663">·         SmaParametersEntity</span></span>

<span data-ttu-id="633d5-664">サーバー コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="633d5-664">Server configuration</span></span>

<span data-ttu-id="633d5-665">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-665">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-666">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-666">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-667">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-667">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-668">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-668">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-669">·         SysServerConfigEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-669">·         SysServerConfigEntity</span></span>

<span data-ttu-id="633d5-670">共有カテゴリ</span><span class="sxs-lookup"><span data-stu-id="633d5-670">Shared categories</span></span>

<span data-ttu-id="633d5-671">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-671">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-672">·         SharedCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-672">·         SharedCategoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-673">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-673">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-674">·         SharedCaegoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-674">·         SharedCaegoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-675">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-675">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-676">·         SharedCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-676">·         SharedCategoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-677">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-677">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-678">·         SharedCategoryEntity ·         SharedCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-678">·         SharedCategoryEntity ·         SharedCategoryEntity\_Basic</span></span>

<span data-ttu-id="633d5-679">サーバー構成 SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="633d5-679">Server configuration SQL Server Reporting Services</span></span>

<span data-ttu-id="633d5-680">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-680">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-681">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-681">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-682">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-682">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-683">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-683">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-684">·         SRSReportDeploymentEntity ·         SRSServersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-684">·         SRSReportDeploymentEntity ·         SRSServersEntity</span></span>

<span data-ttu-id="633d5-685">定期売買パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-685">Subscription parameters</span></span>

<span data-ttu-id="633d5-686">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-686">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-687">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-687">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-688">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-688">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-689">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-689">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-690">·         SubscriptionParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-690">·         SubscriptionParametersEntity</span></span>

<span data-ttu-id="633d5-691">システム パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-691">System parameters</span></span>

<span data-ttu-id="633d5-692">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-692">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-693">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-693">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-694">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-694">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-695">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-695">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-696">·         SystemParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-696">·         SystemParametersEntity</span></span>

<span data-ttu-id="633d5-697">TaxAuthorityAddress</span><span class="sxs-lookup"><span data-stu-id="633d5-697">TaxAuthorityAddress</span></span>

<span data-ttu-id="633d5-698">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-698">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-699">·         TaxAuthrorityAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-699">·         TaxAuthrorityAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-700">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-700">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-701">·         TaxAuthorityAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-701">·         TaxAuthorityAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-702">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-702">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-703">·         TaxAuthorityAddressEntity\_BR ·         TaxAuthorityAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-703">·         TaxAuthorityAddressEntity\_BR ·         TaxAuthorityAddressEntity\_RU</span></span>

<span data-ttu-id="633d5-704">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-704">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-705">·         TaxAuthorityAddressEntity ·         TaxAuthroityAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-705">·         TaxAuthorityAddressEntity ·         TaxAuthroityAddressEntity\_RU</span></span>

<span data-ttu-id="633d5-706">TaxData</span><span class="sxs-lookup"><span data-stu-id="633d5-706">TaxData</span></span>

<span data-ttu-id="633d5-707">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-707">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-708">·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-708">·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="633d5-709">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-709">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-710">·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-710">·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="633d5-711">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-711">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-712">·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-712">·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="633d5-713">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-713">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-714">·         TaxDataEntity ·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-714">·         TaxDataEntity ·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="633d5-715">TaxGroupData</span><span class="sxs-lookup"><span data-stu-id="633d5-715">TaxGroupData</span></span>

<span data-ttu-id="633d5-716">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-716">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-717">·         TaxGroupDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-717">·         TaxGroupDataEntity\_Basic</span></span>

<span data-ttu-id="633d5-718">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-718">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-719">·         TaxGroupDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-719">·         TaxGroupDataEntity\_Basic</span></span>

<span data-ttu-id="633d5-720">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-720">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-721">·         TaxGroupDataEntity\_BR</span><span class="sxs-lookup"><span data-stu-id="633d5-721">·         TaxGroupDataEntity\_BR</span></span>

<span data-ttu-id="633d5-722">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-722">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-723">·         TaxGroupDataEntity ·         TaxGroupDataEntity\_BR</span><span class="sxs-lookup"><span data-stu-id="633d5-723">·         TaxGroupDataEntity ·         TaxGroupDataEntity\_BR</span></span>

<span data-ttu-id="633d5-724">TaxGroupHeading</span><span class="sxs-lookup"><span data-stu-id="633d5-724">TaxGroupHeading</span></span>

<span data-ttu-id="633d5-725">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-725">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-726">·         TaxGroupHeadingEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-726">·         TaxGroupHeadingEntity\_Basic</span></span>

<span data-ttu-id="633d5-727">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-727">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-728">·         TaxGroupHeadingEntity\_\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-728">·         TaxGroupHeadingEntity\_\_Basic</span></span>

<span data-ttu-id="633d5-729">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-729">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-730">·         TaxGroupHeadingEntity\_W</span><span class="sxs-lookup"><span data-stu-id="633d5-730">·         TaxGroupHeadingEntity\_W</span></span>

<span data-ttu-id="633d5-731">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-731">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-732">·         TaxGroupHeadingEntity ·         TaxGroupHeadingEntity\_W</span><span class="sxs-lookup"><span data-stu-id="633d5-732">·         TaxGroupHeadingEntity ·         TaxGroupHeadingEntity\_W</span></span>

<span data-ttu-id="633d5-733">TaxItemGroupHeading</span><span class="sxs-lookup"><span data-stu-id="633d5-733">TaxItemGroupHeading</span></span>

<span data-ttu-id="633d5-734">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-734">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-735">·         TaxItemGroupHeadingEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-735">·         TaxItemGroupHeadingEntity\_Basic</span></span>

<span data-ttu-id="633d5-736">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-736">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-737">·         TaxItemGroupHeadingEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-737">·         TaxItemGroupHeadingEntity\_Basic</span></span>

<span data-ttu-id="633d5-738">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-738">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-739">·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="633d5-739">·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span></span>

<span data-ttu-id="633d5-740">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-740">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-741">·         TaxItemGroupHeadingEntity ·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="633d5-741">·         TaxItemGroupHeadingEntity ·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span></span>

<span data-ttu-id="633d5-742">TaxLedgerAccountGroup</span><span class="sxs-lookup"><span data-stu-id="633d5-742">TaxLedgerAccountGroup</span></span>  

<span data-ttu-id="633d5-743">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-743">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-744">·         TaxLedgerAccountGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-744">·         TaxLedgerAccountGroupEntity\_Basic</span></span>

<span data-ttu-id="633d5-745">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-745">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-746">·         TaxLedgerAccountGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-746">·         TaxLedgerAccountGroupEntity\_Basic</span></span>

<span data-ttu-id="633d5-747">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-747">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-748">·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-748">·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span></span>

<span data-ttu-id="633d5-749">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-749">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-750">·         TaxLedgerAccountGroupEntity ·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-750">·         TaxLedgerAccountGroupEntity ·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span></span>

<span data-ttu-id="633d5-751">TaxOnItem</span><span class="sxs-lookup"><span data-stu-id="633d5-751">TaxOnItem</span></span>

<span data-ttu-id="633d5-752">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-752">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-753">·         TaxOnItemEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-753">·         TaxOnItemEntity\_Basic</span></span>

<span data-ttu-id="633d5-754">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-754">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-755">·         TaxOnItemEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-755">·         TaxOnItemEntity\_Basic</span></span>

<span data-ttu-id="633d5-756">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-756">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-757">·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="633d5-757">·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span></span>

<span data-ttu-id="633d5-758">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-758">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-759">·         TaxOnItemEntity ·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="633d5-759">·         TaxOnItemEntity ·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span></span>

<span data-ttu-id="633d5-760">TaxParameters</span><span class="sxs-lookup"><span data-stu-id="633d5-760">TaxParameters</span></span>

<span data-ttu-id="633d5-761">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-761">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-762">·         TaxParametersEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-762">·         TaxParametersEntity\_Basic</span></span>

<span data-ttu-id="633d5-763">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-763">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-764">·         TaxParametersEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-764">·         TaxParametersEntity\_Basic</span></span>

<span data-ttu-id="633d5-765">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-765">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-766">·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-766">·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span></span>

<span data-ttu-id="633d5-767">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-767">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-768">·         TaxParametersEntity ·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-768">·         TaxParametersEntity ·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span></span>

<span data-ttu-id="633d5-769">TaxPeriodHead</span><span class="sxs-lookup"><span data-stu-id="633d5-769">TaxPeriodHead</span></span>

<span data-ttu-id="633d5-770">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-770">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-771">·         TaxPeriodHeadEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-771">·         TaxPeriodHeadEntity\_Basic</span></span>

<span data-ttu-id="633d5-772">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-772">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-773">·         TaxPeriodHeadEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-773">·         TaxPeriodHeadEntity\_Basic</span></span>

<span data-ttu-id="633d5-774">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-774">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-775">·         TaxPeriodHeadEntity\_HU</span><span class="sxs-lookup"><span data-stu-id="633d5-775">·         TaxPeriodHeadEntity\_HU</span></span>

<span data-ttu-id="633d5-776">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-776">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-777">·         TaxPeriodHeadEntity ·         TaxPeriodHead\_HU</span><span class="sxs-lookup"><span data-stu-id="633d5-777">·         TaxPeriodHeadEntity ·         TaxPeriodHead\_HU</span></span>

<span data-ttu-id="633d5-778">TaxTable</span><span class="sxs-lookup"><span data-stu-id="633d5-778">TaxTable</span></span>  

<span data-ttu-id="633d5-779">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-779">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-780">·         TaxTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-780">·         TaxTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-781">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-781">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-782">·         TaxTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-782">·         TaxTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-783">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-783">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-784">·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span><span class="sxs-lookup"><span data-stu-id="633d5-784">·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span></span>

<span data-ttu-id="633d5-785">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-785">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-786">·         TaxTableEntity ·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span><span class="sxs-lookup"><span data-stu-id="633d5-786">·         TaxTableEntity ·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span></span>

<span data-ttu-id="633d5-787">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="633d5-787">Vendor group</span></span>

<span data-ttu-id="633d5-788">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-788">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-789">·         VendGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-789">·         VendGroupEntity\_Basic</span></span>

<span data-ttu-id="633d5-790">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-790">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-791">·         VendGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-791">·         VendGroupEntity\_Basic</span></span>

<span data-ttu-id="633d5-792">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-792">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-793">·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-793">·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span></span>

<span data-ttu-id="633d5-794">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-794">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-795">·         VendGroupEntity ·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="633d5-795">·         VendGroupEntity ·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span></span>

<span data-ttu-id="633d5-796">ベンダー</span><span class="sxs-lookup"><span data-stu-id="633d5-796">Vendor</span></span>

<span data-ttu-id="633d5-797">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-797">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-798">·         VendorEntity\_Address ·         VendorEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-798">·         VendorEntity\_Address ·         VendorEntity\_Basic</span></span>

<span data-ttu-id="633d5-799">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-799">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-800">·         VendorEntity\_Address ·         VendorEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-800">·         VendorEntity\_Address ·         VendorEntity\_Basic</span></span>

<span data-ttu-id="633d5-801">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-801">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-802">·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-802">·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span></span>

<span data-ttu-id="633d5-803">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-803">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-804">·         VendorEntity ·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="633d5-804">·         VendorEntity ·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span></span>

<span data-ttu-id="633d5-805">仕入先の住所</span><span class="sxs-lookup"><span data-stu-id="633d5-805">Vendor address</span></span>

<span data-ttu-id="633d5-806">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-806">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-807">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MultipeAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-807">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MultipeAddressValues</span></span>

<span data-ttu-id="633d5-808">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-808">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-809">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MulitipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="633d5-809">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MulitipleAddressValues</span></span>

<span data-ttu-id="633d5-810">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-810">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-811">·         VendorAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-811">·         VendorAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-812">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-812">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-813">·         VendorAddressEntity ·         VendorAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-813">·         VendorAddressEntity ·         VendorAddressEntity\_Basic</span></span>

<span data-ttu-id="633d5-814">仕入先請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="633d5-814">Vendor invoice header</span></span>  

<span data-ttu-id="633d5-815">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-815">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-816">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-816">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-817">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-817">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-818">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-818">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-819">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-819">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-820">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-820">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-821">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-821">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-822">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-822">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-823">仕入先請求明細行</span><span class="sxs-lookup"><span data-stu-id="633d5-823">Vendor invoice line</span></span>    

<span data-ttu-id="633d5-824">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-824">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-825">·         VendInvoiceInfoLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-825">·         VendInvoiceInfoLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-826">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-826">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-827">·         VendInvoiceInfoLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-827">·         VendInvoiceInfoLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-828">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-828">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-829">·         VendInvoiceInfoLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-829">·         VendInvoiceInfoLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-830">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-830">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-831">·         VendInvoiceInfoLineEntity\_Basci</span><span class="sxs-lookup"><span data-stu-id="633d5-831">·         VendInvoiceInfoLineEntity\_Basci</span></span>

<span data-ttu-id="633d5-832">仕入先請求書テーブル</span><span class="sxs-lookup"><span data-stu-id="633d5-832">Vendor invoice table</span></span>

<span data-ttu-id="633d5-833">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-833">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-834">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-834">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-835">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-835">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-836">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-836">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-837">·         VendInvoiceInfoTableEntity ·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-837">·         VendInvoiceInfoTableEntity ·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-838">仕入先請求書パラメーター</span><span class="sxs-lookup"><span data-stu-id="633d5-838">Vendor invoice parameters</span></span>  

<span data-ttu-id="633d5-839">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-839">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-840">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-840">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-841">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-841">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-842">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-842">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-843">·         VendParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-843">·         VendParametersEntity</span></span>

<span data-ttu-id="633d5-844">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="633d5-844">Work Calendar</span></span>

<span data-ttu-id="633d5-845">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-845">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-846">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-846">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-847">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-847">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-848">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-848">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-849">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-849">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-850">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-850">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-851">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-851">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-852">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-852">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-853">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="633d5-853">Workflow</span></span>    

<span data-ttu-id="633d5-854">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-854">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-855">·         WorkflowWorkItemQueueEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-855">·         WorkflowWorkItemQueueEntity\_Basic</span></span>

<span data-ttu-id="633d5-856">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-856">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-857">·         WorkflowWorkItemQueueEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-857">·         WorkflowWorkItemQueueEntity\_Basic</span></span>

<span data-ttu-id="633d5-858">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-858">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-859">·         WorkflowWorkItemQueueEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-859">·         WorkflowWorkItemQueueEntity\_Basic</span></span>

<span data-ttu-id="633d5-860">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-860">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-861">·         WorkflowTableEntity ·         WorkflowWorkItemQueueEntity ·         WorkflowWorkItemQueueEntity\_basic</span><span class="sxs-lookup"><span data-stu-id="633d5-861">·         WorkflowTableEntity ·         WorkflowWorkItemQueueEntity ·         WorkflowWorkItemQueueEntity\_basic</span></span>

<span data-ttu-id="633d5-862">WorkTimeLine</span><span class="sxs-lookup"><span data-stu-id="633d5-862">WorkTimeLine</span></span>

<span data-ttu-id="633d5-863">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-863">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-864">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-864">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-865">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-865">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-866">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-866">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-867">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-867">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-868">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-868">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-869">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-869">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-870">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-870">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="633d5-871">WorkTimeTable</span><span class="sxs-lookup"><span data-stu-id="633d5-871">WorkTimeTable</span></span>      

<span data-ttu-id="633d5-872">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="633d5-872">Dynamics AX 2012</span></span>

<span data-ttu-id="633d5-873">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-873">·         WorkTimeTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-874">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="633d5-874">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="633d5-875">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-875">·         WorkTimeTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-876">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="633d5-876">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="633d5-877">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-877">·         WorkTimeTableEntity\_Basic</span></span>

<span data-ttu-id="633d5-878">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="633d5-878">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="633d5-879">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="633d5-879">·         WorkTimeTableEntity\_Basic</span></span>



## <a name="xml-demo-files"></a><span data-ttu-id="633d5-880">XML デモ ファイル</span><span class="sxs-lookup"><span data-stu-id="633d5-880">XML demo files</span></span>
<span data-ttu-id="633d5-881">次のファイルは、Microsoft Dynamics AX 2012 R2 および AX 2012 R3 の累積的な更新プログラム 7 と共に出荷されるデータ インポート/エクスポート フレームワークのバージョンで使用できます。</span><span class="sxs-lookup"><span data-stu-id="633d5-881">The following files are available in the versions of Data Import/Export Framework that ship with cumulative update 7 for Microsoft Dynamics AX 2012 R2 and AX 2012 R3.</span></span>

|                                   |                                   |
|-----------------------------------|-----------------------------------|
| <span data-ttu-id="633d5-882">AifInboundPortEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-882">AifInboundPortEntity</span></span>              | <span data-ttu-id="633d5-883">ProjInvoiceTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-883">ProjInvoiceTableEntity</span></span>            |
| <span data-ttu-id="633d5-884">AifLookupEntryEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-884">AifLookupEntryEntity</span></span>              | <span data-ttu-id="633d5-885">ProjJournalTransEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-885">ProjJournalTransEntity</span></span>            |
| <span data-ttu-id="633d5-886">AifOutboundPortEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-886">AifOutboundPortEntity</span></span>             | <span data-ttu-id="633d5-887">ProjOnAccTransEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-887">ProjOnAccTransEntity</span></span>              |
| <span data-ttu-id="633d5-888">AIfWebSitesEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-888">AIfWebSitesEntity</span></span>                 | <span data-ttu-id="633d5-889">ProjServerSettingsEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-889">ProjServerSettingsEntity</span></span>          |
| <span data-ttu-id="633d5-890">AssetEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-890">AssetEntity</span></span>                       | <span data-ttu-id="633d5-891">ProjTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-891">ProjTableEntity</span></span>                   |
| <span data-ttu-id="633d5-892">AssetParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-892">AssetParametersEntity</span></span>             | <span data-ttu-id="633d5-893">PurchLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-893">PurchLineEntity</span></span>                   |
| <span data-ttu-id="633d5-894">BankParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-894">BankParametersEntity</span></span>              | <span data-ttu-id="633d5-895">PurchTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-895">PurchTableEntity</span></span>                  |
| <span data-ttu-id="633d5-896">BarCodeSetupEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-896">BarCodeSetupEntity</span></span>                | <span data-ttu-id="633d5-897">RouteEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-897">RouteEntity</span></span>                       |
| <span data-ttu-id="633d5-898">BatchGroupEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-898">BatchGroupEntity</span></span>                  | <span data-ttu-id="633d5-899">RouteOperationsEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-899">RouteOperationsEntity</span></span>             |
| <span data-ttu-id="633d5-900">BIConfigurationEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-900">BIConfigurationEntity</span></span>             | <span data-ttu-id="633d5-901">SalesLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-901">SalesLineEntity</span></span>                   |
| <span data-ttu-id="633d5-902">BITimePeriodsMDXEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-902">BITimePeriodsMDXEntity</span></span>            | <span data-ttu-id="633d5-903">SalesTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-903">SalesTableEntity</span></span>                  |
| <span data-ttu-id="633d5-904">BOMEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-904">BOMEntity</span></span>                         | <span data-ttu-id="633d5-905">SharedCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-905">SharedCategoryEntity</span></span>              |
| <span data-ttu-id="633d5-906">BOMVersionEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-906">BOMVersionEntity</span></span>                  | <span data-ttu-id="633d5-907">SIGParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-907">SIGParametersEntity</span></span>               |
| <span data-ttu-id="633d5-908">BudgetParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-908">BudgetParametersEntity</span></span>            | <span data-ttu-id="633d5-909">SmaParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-909">SmaParametersEntity</span></span>               |
| <span data-ttu-id="633d5-910">BudgetTransactionLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-910">BudgetTransactionLineEntity</span></span>       | <span data-ttu-id="633d5-911">SmmParametersTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-911">SmmParametersTableEntity</span></span>          |
| <span data-ttu-id="633d5-912">CategoryTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-912">CategoryTableEntity</span></span>               | <span data-ttu-id="633d5-913">SRSReportDeploymentEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-913">SRSReportDeploymentEntity</span></span>         |
| <span data-ttu-id="633d5-914">CollabSiteParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-914">CollabSiteParametersEntity</span></span>        | <span data-ttu-id="633d5-915">SRSServersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-915">SRSServersEntity</span></span>                  |
| <span data-ttu-id="633d5-916">ContactPersonAddressEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-916">ContactPersonAddressEntity</span></span>        | <span data-ttu-id="633d5-917">SubscriptionParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-917">SubscriptionParametersEntity</span></span>      |
| <span data-ttu-id="633d5-918">ContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-918">ContactPersonEntity</span></span>               | <span data-ttu-id="633d5-919">SyncParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-919">SyncParametersEntity</span></span>              |
| <span data-ttu-id="633d5-920">ContentTypeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-920">ContentTypeEntity</span></span>                 | <span data-ttu-id="633d5-921">SysEmailParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-921">SysEmailParametersEntity</span></span>          |
| <span data-ttu-id="633d5-922">COSParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-922">COSParametersEntity</span></span>               | <span data-ttu-id="633d5-923">SysPolicySourceDocumentRuleEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-923">SysPolicySourceDocumentRuleEntity</span></span> |
| <span data-ttu-id="633d5-924">CustomerAddressEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-924">CustomerAddressEntity</span></span>             | <span data-ttu-id="633d5-925">SysServerConfigEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-925">SysServerConfigEntity</span></span>             |
| <span data-ttu-id="633d5-926">CustomerEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-926">CustomerEntity</span></span>                    | <span data-ttu-id="633d5-927">SystemParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-927">SystemParametersEntity</span></span>            |
| <span data-ttu-id="633d5-928">CustVendAIFPaymTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-928">CustVendAIFPaymTableEntity</span></span>        | <span data-ttu-id="633d5-929">TaxAuthorityAddressEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-929">TaxAuthorityAddressEntity</span></span>         |
| <span data-ttu-id="633d5-930">DimensionAttributeValueEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-930">DimensionAttributeValueEntity</span></span>     | <span data-ttu-id="633d5-931">TaxDataEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-931">TaxDataEntity</span></span>                     |
| <span data-ttu-id="633d5-932">DimensionHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-932">DimensionHierarchyEntity</span></span>          | <span data-ttu-id="633d5-933">TaxGroupDataEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-933">TaxGroupDataEntity</span></span>                |
| <span data-ttu-id="633d5-934">DirParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-934">DirParametersEntity</span></span>               | <span data-ttu-id="633d5-935">TaxGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-935">TaxGroupHeadingEntity</span></span>             |
| <span data-ttu-id="633d5-936">DocuDataSourceEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-936">DocuDataSourceEntity</span></span>              | <span data-ttu-id="633d5-937">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-937">TaxItemGroupHeadingEntity</span></span>         |
| <span data-ttu-id="633d5-938">DocuTableEnabledEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-938">DocuTableEnabledEntity</span></span>            | <span data-ttu-id="633d5-939">TaxLedgerAccountGroupEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-939">TaxLedgerAccountGroupEntity</span></span>       |
| <span data-ttu-id="633d5-940">DocuTypeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-940">DocuTypeEntity</span></span>                    | <span data-ttu-id="633d5-941">TaxOnItemEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-941">TaxOnItemEntity</span></span>                   |
| <span data-ttu-id="633d5-942">EcoResAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-942">EcoResAttributeEntity</span></span>             | <span data-ttu-id="633d5-943">TaxParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-943">TaxParametersEntity</span></span>               |
| <span data-ttu-id="633d5-944">EcoResAttributeTypeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-944">EcoResAttributeTypeEntity</span></span>         | <span data-ttu-id="633d5-945">TaxPeriodHeadEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-945">TaxPeriodHeadEntity</span></span>               |
| <span data-ttu-id="633d5-946">EcoResCategoryHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-946">EcoResCategoryHierarchyEntity</span></span>     | <span data-ttu-id="633d5-947">TaxTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-947">TaxTableEntity</span></span>                    |
| <span data-ttu-id="633d5-948">EcoResCategoryHierarchyRoleEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-948">EcoResCategoryHierarchyRoleEntity</span></span> | <span data-ttu-id="633d5-949">TrvAppEmplSubEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-949">TrvAppEmplSubEntity</span></span>               |
| <span data-ttu-id="633d5-950">EmployeeAddressEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-950">EmployeeAddressEntity</span></span>             | <span data-ttu-id="633d5-951">TrvCostTypeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-951">TrvCostTypeEntity</span></span>                 |
| <span data-ttu-id="633d5-952">EmployeeEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-952">EmployeeEntity</span></span>                    | <span data-ttu-id="633d5-953">TrvCostTypeRatesEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-953">TrvCostTypeRatesEntity</span></span>            |
| <span data-ttu-id="633d5-954">EMSParameterEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-954">EMSParameterEntity</span></span>                | <span data-ttu-id="633d5-955">TrvExpSubCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-955">TrvExpSubCategoryEntity</span></span>           |
| <span data-ttu-id="633d5-956">EPDocuParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-956">EPDocuParametersEntity</span></span>            | <span data-ttu-id="633d5-957">TrvParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-957">TrvParametersEntity</span></span>               |
| <span data-ttu-id="633d5-958">HcmJobDetailEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-958">HcmJobDetailEntity</span></span>                | <span data-ttu-id="633d5-959">TrvPayMethodEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-959">TrvPayMethodEntity</span></span>                |
| <span data-ttu-id="633d5-960">HcmPositionDetailEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-960">HcmPositionDetailEntity</span></span>           | <span data-ttu-id="633d5-961">TrvPBSCatCodesEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-961">TrvPBSCatCodesEntity</span></span>              |
| <span data-ttu-id="633d5-962">HcmSharedParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-962">HcmSharedParametersEntity</span></span>         | <span data-ttu-id="633d5-963">TrvPolicyEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-963">TrvPolicyEntity</span></span>                   |
| <span data-ttu-id="633d5-964">HRMParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-964">HRMParametersEntity</span></span>               | <span data-ttu-id="633d5-965">TrvValidatePaymentEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-965">TrvValidatePaymentEntity</span></span>          |
| <span data-ttu-id="633d5-966">IntrastatStateParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-966">IntrastatStateParametersEntity</span></span>    | <span data-ttu-id="633d5-967">UnitOfMeasureEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-967">UnitOfMeasureEntity</span></span>               |
| <span data-ttu-id="633d5-968">InventJournalEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-968">InventJournalEntity</span></span>               | <span data-ttu-id="633d5-969">VendGroupEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-969">VendGroupEntity</span></span>                   |
| <span data-ttu-id="633d5-970">InventParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-970">InventParametersEntity</span></span>            | <span data-ttu-id="633d5-971">VendInvoiceInfoLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-971">VendInvoiceInfoLineEntity</span></span>         |
| <span data-ttu-id="633d5-972">InventTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-972">InventTableEntity</span></span>                 | <span data-ttu-id="633d5-973">VendInvoiceInfoTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-973">VendInvoiceInfoTableEntity</span></span>        |
| <span data-ttu-id="633d5-974">LedgerJournalEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-974">LedgerJournalEntity</span></span>               | <span data-ttu-id="633d5-975">VendorAddressEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-975">VendorAddressEntity</span></span>               |
| <span data-ttu-id="633d5-976">LedgerParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-976">LedgerParametersEntity</span></span>            | <span data-ttu-id="633d5-977">VendorEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-977">VendorEntity</span></span>                      |
| <span data-ttu-id="633d5-978">MainAccountEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-978">MainAccountEntity</span></span>                 | <span data-ttu-id="633d5-979">VendParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-979">VendParametersEntity</span></span>              |
| <span data-ttu-id="633d5-980">OMHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-980">OMHierarchyEntity</span></span>                 | <span data-ttu-id="633d5-981">WorkCalendarDateEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-981">WorkCalendarDateEntity</span></span>            |
| <span data-ttu-id="633d5-982">OMOperatingUnitEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-982">OMOperatingUnitEntity</span></span>             | <span data-ttu-id="633d5-983">WorkCalendarDateLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-983">WorkCalendarDateLineEntity</span></span>        |
| <span data-ttu-id="633d5-984">OrganizationHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-984">OrganizationHierarchyEntity</span></span>       | <span data-ttu-id="633d5-985">WorkCalendarTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-985">WorkCalendarTableEntity</span></span>           |
| <span data-ttu-id="633d5-986">PriceDiscAdmTransEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-986">PriceDiscAdmTransEntity</span></span>           | <span data-ttu-id="633d5-987">WorkflowTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-987">WorkflowTableEntity</span></span>               |
| <span data-ttu-id="633d5-988">PRLPayrollParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-988">PRLPayrollParametersEntity</span></span>        | <span data-ttu-id="633d5-989">WorkflowWorkItemQueueEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-989">WorkflowWorkItemQueueEntity</span></span>       |
| <span data-ttu-id="633d5-990">ProdParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-990">ProdParametersEntity</span></span>              | <span data-ttu-id="633d5-991">WorkTimeLineEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-991">WorkTimeLineEntity</span></span>                |
| <span data-ttu-id="633d5-992">ProductEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-992">ProductEntity</span></span>                     | <span data-ttu-id="633d5-993">WorkTimeTableEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-993">WorkTimeTableEntity</span></span>               |
| <span data-ttu-id="633d5-994">ProductMasterEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-994">ProductMasterEntity</span></span>               | <span data-ttu-id="633d5-995">WrkCtrParametersEntity</span><span class="sxs-lookup"><span data-stu-id="633d5-995">WrkCtrParametersEntity</span></span>            |







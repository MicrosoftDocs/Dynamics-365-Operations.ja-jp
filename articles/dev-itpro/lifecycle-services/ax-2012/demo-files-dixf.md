---
title: "データ インポート/エクスポート フレームワーク (DIFX) のデモ ファイル"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 2cdebfe3c9ec8ce44d845f6c5bcdeed733a3aacd
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="demo-files-for-the-data-importexport-framework-dixf"></a><span data-ttu-id="353e7-103">データ インポート/エクスポート フレームワーク (DIFX) のデモ ファイル</span><span class="sxs-lookup"><span data-stu-id="353e7-103">Demo files for the Data Import/Export Framework (DIXF)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="353e7-104">デモ ファイルは、Microsoft Dynamics AX 2012 の Contoso デモデータと共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="353e7-104">The demo files can be used together with the Contoso demo data for Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="353e7-105">具体的には、ファイルは CEU Contoso Entertainment Systems (West) 会社と組み合わせて使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="353e7-105">Specifically, the files are intended to be used together with the CEU Contoso Entertainment Systems (West) company.</span></span>

## <a name="source-data-format-settings-for-demo-files"></a><span data-ttu-id="353e7-106">デモ ファイルのソース データ形式設定</span><span class="sxs-lookup"><span data-stu-id="353e7-106">Source data format settings for demo files</span></span>
<span data-ttu-id="353e7-107">次のテーブルに、ソース データ形式に入力する必要のあるコンフィギュレーション設定を示します。</span><span class="sxs-lookup"><span data-stu-id="353e7-107">The following table lists the configuration settings that you should enter for the source data format.</span></span>

| <span data-ttu-id="353e7-108">設定</span><span class="sxs-lookup"><span data-stu-id="353e7-108">Setting</span></span>                         | <span data-ttu-id="353e7-109">先頭値</span><span class="sxs-lookup"><span data-stu-id="353e7-109">Value</span></span>                                             |
|---------------------------------|---------------------------------------------------|
| <span data-ttu-id="353e7-110">**ファイル形式**</span><span class="sxs-lookup"><span data-stu-id="353e7-110">**File format**</span></span>                 | <span data-ttu-id="353e7-111">区切り</span><span class="sxs-lookup"><span data-stu-id="353e7-111">Delimited</span></span>                                         |
| <span data-ttu-id="353e7-112">**先頭行のヘッダー**</span><span class="sxs-lookup"><span data-stu-id="353e7-112">**First row header**</span></span>            | <span data-ttu-id="353e7-113">選択済</span><span class="sxs-lookup"><span data-stu-id="353e7-113">Selected</span></span>                                          |
| <span data-ttu-id="353e7-114">**行区切り**</span><span class="sxs-lookup"><span data-stu-id="353e7-114">**Row delimiter**</span></span>               | <span data-ttu-id="353e7-115">{CR}{LF}</span><span class="sxs-lookup"><span data-stu-id="353e7-115">{CR}{LF}</span></span>                                          |
| <span data-ttu-id="353e7-116">**列区切り**</span><span class="sxs-lookup"><span data-stu-id="353e7-116">**Column delimiter**</span></span>            | <span data-ttu-id="353e7-117">コンマ {,}</span><span class="sxs-lookup"><span data-stu-id="353e7-117">Comma {,}</span></span>                                         |
| <span data-ttu-id="353e7-118">**テキスト修飾子**</span><span class="sxs-lookup"><span data-stu-id="353e7-118">**Text qualifier**</span></span>              | <span data-ttu-id="353e7-119">"</span><span class="sxs-lookup"><span data-stu-id="353e7-119">"</span></span>                                                 |
| <span data-ttu-id="353e7-120">**コード ページ**</span><span class="sxs-lookup"><span data-stu-id="353e7-120">**Code page**</span></span>                   | <span data-ttu-id="353e7-121">1252 西ヨーロッパ (Windows)</span><span class="sxs-lookup"><span data-stu-id="353e7-121">1252 Western European (Windows)</span></span>                   |
| <span data-ttu-id="353e7-122">**Unicode**</span><span class="sxs-lookup"><span data-stu-id="353e7-122">**Unicode**</span></span>                     | <span data-ttu-id="353e7-123">未選択</span><span class="sxs-lookup"><span data-stu-id="353e7-123">Not selected</span></span>                                      |
| <span data-ttu-id="353e7-124">**言語ロケール**</span><span class="sxs-lookup"><span data-stu-id="353e7-124">**Language locale**</span></span>             | <span data-ttu-id="353e7-125">ja</span><span class="sxs-lookup"><span data-stu-id="353e7-125">en-us</span></span>                                             |
| <span data-ttu-id="353e7-126">**分析コード**</span><span class="sxs-lookup"><span data-stu-id="353e7-126">**Dimension code**</span></span>              | <span data-ttu-id="353e7-127">CostCenter、Department、または ExpensePurpose を選択します。</span><span class="sxs-lookup"><span data-stu-id="353e7-127">Select CostCenter, Department, or ExpensePurpose.</span></span> |
| <span data-ttu-id="353e7-128">**勘定科目表の区切り記号**</span><span class="sxs-lookup"><span data-stu-id="353e7-128">**Chart of accounts delimiter**</span></span> | -                                                 |



## <a name="file-list"></a><span data-ttu-id="353e7-129">ファイル リスト</span><span class="sxs-lookup"><span data-stu-id="353e7-129">File list</span></span>
<span data-ttu-id="353e7-130">次のテーブルに、各エンティティに関連付けられているデモ ファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="353e7-130">The following table lists the demo files that are associated with each entity.</span></span>

<span data-ttu-id="353e7-131">**名前**</span><span class="sxs-lookup"><span data-stu-id="353e7-131">**Name**</span></span>

<span data-ttu-id="353e7-132">**Dynamics AX バージョン**</span><span class="sxs-lookup"><span data-stu-id="353e7-132">**Dynamics AX version**</span></span>

<span data-ttu-id="353e7-133">**デモ ファイル**</span><span class="sxs-lookup"><span data-stu-id="353e7-133">**Demo files**</span></span>

<span data-ttu-id="353e7-134">AIF</span><span class="sxs-lookup"><span data-stu-id="353e7-134">AIF</span></span>

<span data-ttu-id="353e7-135">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-135">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-136">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-136">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-137">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-137">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-138">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-138">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-139">·         AifInboundPortEntity ·         AifLookupEntryEntity ·         AifOutboundPortEntity ·         AIfWebSitesEntity ·         CustVendAIFPaymTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-139">·         AifInboundPortEntity ·         AifLookupEntryEntity ·         AifOutboundPortEntity ·         AIfWebSitesEntity ·         CustVendAIFPaymTableEntity</span></span>

<span data-ttu-id="353e7-140">資産</span><span class="sxs-lookup"><span data-stu-id="353e7-140">Asset</span></span>

<span data-ttu-id="353e7-141">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-141">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-142">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span><span class="sxs-lookup"><span data-stu-id="353e7-142">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span></span>

<span data-ttu-id="353e7-143">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-143">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-144">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span><span class="sxs-lookup"><span data-stu-id="353e7-144">·         AssetEntity\_Basic ·         AssetEntity\_TextQualifier</span></span>

<span data-ttu-id="353e7-145">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-145">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-146">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-146">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL</span></span>

<span data-ttu-id="353e7-147">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-147">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-148">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL ·         AssetParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-148">·         AssetEntity\_BR ·         AssetEntity\_CN ·         AssetEntity\_CZ ·         AssetEntity\_IN ·         AssetEntity\_LV ·         AssetEntity\_PL ·         AssetParametersEntity</span></span>

<span data-ttu-id="353e7-149">属性タイプ</span><span class="sxs-lookup"><span data-stu-id="353e7-149">Attribute types</span></span>

<span data-ttu-id="353e7-150">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-150">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-151">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-151">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="353e7-152">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-152">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-153">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-153">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="353e7-154">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-154">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-155">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-155">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="353e7-156">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-156">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-157">·         AttributeTypesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-157">·         AttributeTypesEntity\_Basic</span></span>

<span data-ttu-id="353e7-158">属性</span><span class="sxs-lookup"><span data-stu-id="353e7-158">Attributes</span></span>

<span data-ttu-id="353e7-159">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-159">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-160">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-160">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="353e7-161">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-161">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-162">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-162">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="353e7-163">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-163">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-164">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-164">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="353e7-165">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-165">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-166">·         AttributeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-166">·         AttributeEntity\_Basic</span></span>

<span data-ttu-id="353e7-167">監査ポリシー</span><span class="sxs-lookup"><span data-stu-id="353e7-167">Audit policy</span></span>

<span data-ttu-id="353e7-168">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-168">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-169">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-169">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-170">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-170">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-171">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-171">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-172">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-172">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-173">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-173">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-174">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-174">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-175">·         AuditPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-175">·         AuditPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-176">銀行パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-176">Bank parameters</span></span>

<span data-ttu-id="353e7-177">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-177">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-178">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-178">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-179">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-179">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-180">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-180">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-181">·         BankParametersEnitty</span><span class="sxs-lookup"><span data-stu-id="353e7-181">·         BankParametersEnitty</span></span>

<span data-ttu-id="353e7-182">BarcodeSetup</span><span class="sxs-lookup"><span data-stu-id="353e7-182">BarcodeSetup</span></span>

<span data-ttu-id="353e7-183">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-183">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-184">·         BarCodeSetupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-184">·         BarCodeSetupEntity\_Basic</span></span>

<span data-ttu-id="353e7-185">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-185">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-186">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span><span class="sxs-lookup"><span data-stu-id="353e7-186">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span></span>

<span data-ttu-id="353e7-187">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-187">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-188">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span><span class="sxs-lookup"><span data-stu-id="353e7-188">·         BarCodeSetupEntity ·         BarCodeSetupEntity\_Retail</span></span>

<span data-ttu-id="353e7-189">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-189">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-190">バッチ グループ</span><span class="sxs-lookup"><span data-stu-id="353e7-190">Batch group</span></span>

<span data-ttu-id="353e7-191">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-191">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-192">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-192">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-193">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-193">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-194">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-194">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-195">·         BatchGroupEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-195">·         BatchGroupEntity</span></span>

<span data-ttu-id="353e7-196">BOM</span><span class="sxs-lookup"><span data-stu-id="353e7-196">BOM</span></span>

<span data-ttu-id="353e7-197">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-197">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-198">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-198">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span></span>

<span data-ttu-id="353e7-199">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-199">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-200">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-200">·         BOMEntity\_Basic ·         BOMEntity\_Enum</span></span>

<span data-ttu-id="353e7-201">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-201">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-202">·         BOMEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-202">·         BOMEntity\_Basic</span></span>

<span data-ttu-id="353e7-203">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-203">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-204">·         BOMEntity ·         BOMEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-204">·         BOMEntity ·         BOMEntity\_Basic</span></span>

<span data-ttu-id="353e7-205">BOMVersion</span><span class="sxs-lookup"><span data-stu-id="353e7-205">BOMVersion</span></span>

<span data-ttu-id="353e7-206">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-206">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-207">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-207">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span></span>

<span data-ttu-id="353e7-208">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-208">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-209">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-209">·         BOMVersionEntity\_Default ·         BomVersionEntity\_Enum</span></span>

<span data-ttu-id="353e7-210">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-210">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-211">·         BOMVersionEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-211">·         BOMVersionEntity\_Basic</span></span>

<span data-ttu-id="353e7-212">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-212">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-213">·         BOMVersionEntity ·         BOMVersionEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-213">·         BOMVersionEntity ·         BOMVersionEntity\_Basic</span></span>

<span data-ttu-id="353e7-214">予算</span><span class="sxs-lookup"><span data-stu-id="353e7-214">Budget</span></span>

<span data-ttu-id="353e7-215">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-215">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-216">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-216">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-217">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-217">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-218">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-218">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-219">·         BudgetParametersEntity ·         BudgetTransactionLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-219">·         BudgetParametersEntity ·         BudgetTransactionLineEntity</span></span>

<span data-ttu-id="353e7-220">ビジネス インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="353e7-220">Business intelligence</span></span>

<span data-ttu-id="353e7-221">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-221">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-222">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-222">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-223">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-223">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-224">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-224">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-225">·         BIConfigruationEntity ·         BITimePeriodsMDXEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-225">·         BIConfigruationEntity ·         BITimePeriodsMDXEntity</span></span>

<span data-ttu-id="353e7-226">ケースのワークフロー</span><span class="sxs-lookup"><span data-stu-id="353e7-226">Case workflow</span></span>

<span data-ttu-id="353e7-227">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-227">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-228">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-228">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="353e7-229">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-229">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-230">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-230">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="353e7-231">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-231">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-232">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-232">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="353e7-233">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-233">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-234">·         CaseWorkFlowEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-234">·         CaseWorkFlowEntity\_Basic</span></span>

<span data-ttu-id="353e7-235">カテゴリ階層</span><span class="sxs-lookup"><span data-stu-id="353e7-235">Category hierarchies</span></span>

<span data-ttu-id="353e7-236">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-236">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-237">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-237">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>  

<span data-ttu-id="353e7-238">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-238">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-239">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-239">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>

<span data-ttu-id="353e7-240">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-240">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-241">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-241">·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>

<span data-ttu-id="353e7-242">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-242">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-243">·         EcoResAttributeEntity ·         EcoResAttributeTypeEntity ·         EcoResCategoryHierarchyEntity ·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity ·         EcoResCategoryHierarchyRoleEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-243">·         EcoResAttributeEntity ·         EcoResAttributeTypeEntity ·         EcoResCategoryHierarchyEntity ·         EcoResCategoryHierarchyEntity\_Basic ·         EcoResCategoryHierarchyRoleEntity ·         EcoResCategoryHierarchyRoleEntity\_Basic</span></span>

<span data-ttu-id="353e7-244">カテゴリ テーブル</span><span class="sxs-lookup"><span data-stu-id="353e7-244">Category table</span></span>

<span data-ttu-id="353e7-245">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-245">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-246">·         CategoryTableEntity\_Project</span><span class="sxs-lookup"><span data-stu-id="353e7-246">·         CategoryTableEntity\_Project</span></span>

<span data-ttu-id="353e7-247">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-247">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-248">·         CategoryTableEntity\_Project</span><span class="sxs-lookup"><span data-stu-id="353e7-248">·         CategoryTableEntity\_Project</span></span>

<span data-ttu-id="353e7-249">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-249">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-250">·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span><span class="sxs-lookup"><span data-stu-id="353e7-250">·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span></span>

<span data-ttu-id="353e7-251">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-251">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-252">·         CategoryTableEntity ·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span><span class="sxs-lookup"><span data-stu-id="353e7-252">·         CategoryTableEntity ·         CategoryTableEntity\_Project ·         CategoryTableEntity\_Project\_BR ·         CategoryTableEntity\_Project\_TH</span></span>

<span data-ttu-id="353e7-253">勘定構造のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="353e7-253">Configure account structures</span></span>

<span data-ttu-id="353e7-254">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-254">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-255">·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-255">·         DimensionHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-256">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-256">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-257">·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-257">·         DimensionHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-258">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-258">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-259">·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-259">·         DimensionHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-260">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-260">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-261">·         DimensionHierarchyEntity ·         DimensionHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-261">·         DimensionHierarchyEntity ·         DimensionHierarchyEntity\_Basic</span></span>

  <span data-ttu-id="353e7-262">ContactPerson</span><span class="sxs-lookup"><span data-stu-id="353e7-262">ContactPerson</span></span>

<span data-ttu-id="353e7-263">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-263">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-264">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-264">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span></span>

<span data-ttu-id="353e7-265">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-265">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-266">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-266">·         ContactPersonEntity\_Address ·         ContactPersonEntity\_Basic</span></span>

<span data-ttu-id="353e7-267">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-267">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-268">·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-268">·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="353e7-269">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-269">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-270">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-270">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="353e7-271">ContactPersonAddress</span><span class="sxs-lookup"><span data-stu-id="353e7-271">ContactPersonAddress</span></span>

<span data-ttu-id="353e7-272">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-272">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-273">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-273">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="353e7-274">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-274">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-275">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-275">·         ContactPersonAddressEntity\_Basic ·         ContactPersonAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="353e7-276">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-276">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-277">·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-277">·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="353e7-278">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-278">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-279">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-279">·         ContactPersonAddressEntity ·         ContactPersonAddressEntity\_RU</span></span>

<span data-ttu-id="353e7-280">原価会計パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-280">Cost accounting parameters</span></span>

<span data-ttu-id="353e7-281">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-281">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-282">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-282">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-283">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-283">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-284">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-284">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-285">·         COSParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-285">·         COSParametersEntity</span></span>

  <span data-ttu-id="353e7-286">顧客</span><span class="sxs-lookup"><span data-stu-id="353e7-286">Customer</span></span>

<span data-ttu-id="353e7-287">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-287">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-288">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span><span class="sxs-lookup"><span data-stu-id="353e7-288">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span></span>

<span data-ttu-id="353e7-289">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-289">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-290">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span><span class="sxs-lookup"><span data-stu-id="353e7-290">·         CustomerEntity\_Person ·         CustomerEntity\_ContactInfo ·         CustomerEntity\_Dimensions\_Enums</span></span>

<span data-ttu-id="353e7-291">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-291">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-292">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-292">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span></span>

<span data-ttu-id="353e7-293">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-293">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-294">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-294">·         CustomerEntity\_Basic ·         CustomerEntity\_BR ·         CustonerEntity\_PL ·         CustomerEntity\_RU</span></span>

<span data-ttu-id="353e7-295">顧客の住所</span><span class="sxs-lookup"><span data-stu-id="353e7-295">Customer address</span></span>

<span data-ttu-id="353e7-296">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-296">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-297">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-297">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="353e7-298">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-298">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-299">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-299">·         CustomerAddressEntity\_Basic ·         CustomerAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="353e7-300">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-300">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-301">·         CustomerAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-301">·         CustomerAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-302">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-302">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-303">·         CustomerAddressEntity ·         CustomerAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-303">·         CustomerAddressEntity ·         CustomerAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-304">部門</span><span class="sxs-lookup"><span data-stu-id="353e7-304">Departments</span></span>

<span data-ttu-id="353e7-305">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-305">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-306">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-306">·         DepartmentEntity\_Basic</span></span>

<span data-ttu-id="353e7-307">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-307">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-308">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-308">·         DepartmentEntity\_Basic</span></span>

<span data-ttu-id="353e7-309">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-309">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-310">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-310">·         DepartmentEntity\_Basic</span></span>

<span data-ttu-id="353e7-311">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-311">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-312">·         DepartmentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-312">·         DepartmentEntity\_Basic</span></span>

  <span data-ttu-id="353e7-313">分析コード</span><span class="sxs-lookup"><span data-stu-id="353e7-313">Dimensions</span></span>

<span data-ttu-id="353e7-314">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-314">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-315">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-315">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span></span>

<span data-ttu-id="353e7-316">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-316">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-317">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-317">·         DimensionsEntity\_Basic ·         DimensionsEntity\_Enum</span></span>

<span data-ttu-id="353e7-318">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-318">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-319">·         DimensionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-319">·         DimensionsEntity\_Basic</span></span>

<span data-ttu-id="353e7-320">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-320">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-321">·         DimensionAttributeValueEntity ·         DimensionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-321">·         DimensionAttributeValueEntity ·         DimensionsEntity\_Basic</span></span>

  <span data-ttu-id="353e7-322">DocuType</span><span class="sxs-lookup"><span data-stu-id="353e7-322">DocuType</span></span>

<span data-ttu-id="353e7-323">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-323">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-324">·         DocuTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-324">·         DocuTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-325">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-325">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-326">·         DocuTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-326">·         DocuTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-327">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-327">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-328">·         DocuTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-328">·         DocuTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-329">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-329">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-330">·         DocuTypeEntity ·         DocuTypeEntity\_Basic ·         DocuTableEnabledEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-330">·         DocuTypeEntity ·         DocuTypeEntity\_Basic ·         DocuTableEnabledEntity</span></span>

  <span data-ttu-id="353e7-331">ドキュメント管理</span><span class="sxs-lookup"><span data-stu-id="353e7-331">Document management</span></span>

<span data-ttu-id="353e7-332">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-332">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-333">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-333">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-334">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-334">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-335">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-335">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-336">·         CollabSiteParametersEntity ·         ContentTypeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-336">·         CollabSiteParametersEntity ·         ContentTypeEntity</span></span>

<span data-ttu-id="353e7-337">電子署名</span><span class="sxs-lookup"><span data-stu-id="353e7-337">Electronic signatures</span></span>

<span data-ttu-id="353e7-338">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-338">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-339">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-339">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-340">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-340">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-341">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-341">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-342">·         SIGParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-342">·         SIGParametersEntity</span></span>

<span data-ttu-id="353e7-343">従業員</span><span class="sxs-lookup"><span data-stu-id="353e7-343">Employee</span></span>

<span data-ttu-id="353e7-344">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-344">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-345">·         EmployeeEntity\_Address ·         EmployeeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-345">·         EmployeeEntity\_Address ·         EmployeeEntity\_Basic</span></span>

<span data-ttu-id="353e7-346">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-346">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-347">·         EmployeeEntity\_Address ·         EmployeeEntityBasic</span><span class="sxs-lookup"><span data-stu-id="353e7-347">·         EmployeeEntity\_Address ·         EmployeeEntityBasic</span></span>

<span data-ttu-id="353e7-348">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-348">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-349">·         EmployeeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-349">·         EmployeeEntity\_Basic</span></span>

<span data-ttu-id="353e7-350">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-350">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-351">·         EmployeeEntity ·         EmployeeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-351">·         EmployeeEntity ·         EmployeeEntity\_Basic</span></span>

<span data-ttu-id="353e7-352">従業員の住所</span><span class="sxs-lookup"><span data-stu-id="353e7-352">Employee address</span></span>

<span data-ttu-id="353e7-353">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-353">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-354">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-354">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="353e7-355">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-355">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-356">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-356">·         EmployeeAddressEntity\_Basic ·         EmployeeAddressEntity\_MultipleAddressValues</span></span>

<span data-ttu-id="353e7-357">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-357">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-358">·         EmployeeAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-358">·         EmployeeAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-359">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-359">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-360">·         EmployeeAddressEntity ·         EmployeeAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-360">·         EmployeeAddressEntity ·         EmployeeAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-361">エンタープライズ ポータル</span><span class="sxs-lookup"><span data-stu-id="353e7-361">Enterprise Portal</span></span>

<span data-ttu-id="353e7-362">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-362">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-363">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-363">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-364">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-364">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-365">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-365">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-366">·         EPDocuParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-366">·         EPDocuParametersEntity</span></span>

  <span data-ttu-id="353e7-367">環境的持続可能なパラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-367">Environmental sustainability parameter</span></span>

<span data-ttu-id="353e7-368">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-368">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-369">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-369">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-370">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-370">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-371">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-371">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-372">·         EMSParameterEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-372">·         EMSParameterEntity</span></span>

<span data-ttu-id="353e7-373">経費精算書パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-373">Expense report parameters</span></span>

<span data-ttu-id="353e7-374">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-374">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-375">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-375">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-376">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-376">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-377">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-377">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-378">·         TrvParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-378">·         TrvParametersEntity</span></span>

<span data-ttu-id="353e7-379">経費精算書の委任</span><span class="sxs-lookup"><span data-stu-id="353e7-379">Expense report delegation</span></span>

<span data-ttu-id="353e7-380">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-380">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-381">·         TrvAppEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-381">·         TrvAppEmplSubEntity\_Basic</span></span>

<span data-ttu-id="353e7-382">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-382">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-383">·         TrvAppEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-383">·         TrvAppEmplSubEntity\_Basic</span></span>

<span data-ttu-id="353e7-384">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-384">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-385">·         TrvApEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-385">·         TrvApEmplSubEntity\_Basic</span></span>

<span data-ttu-id="353e7-386">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-386">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-387">·         TrvAppEmplSubEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-387">·         TrvAppEmplSubEntity\_Basic</span></span>

<span data-ttu-id="353e7-388">経費精算書のコスト</span><span class="sxs-lookup"><span data-stu-id="353e7-388">Expense report cost</span></span>

<span data-ttu-id="353e7-389">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-389">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-390">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-390">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-391">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-391">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-392">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-392">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-393">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-393">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-394">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-394">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-395">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-395">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-396">·         TrvCostTypeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-396">·         TrvCostTypeEntity\_Basic</span></span>

<span data-ttu-id="353e7-397">経費精算書カテゴリ</span><span class="sxs-lookup"><span data-stu-id="353e7-397">Expense report category</span></span>

<span data-ttu-id="353e7-398">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-398">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-399">·         TrvExpSubCateogoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-399">·         TrvExpSubCateogoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-400">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-400">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-401">·         TrvExpSubCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-401">·         TrvExpSubCategoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-402">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-402">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-403">·         TrvExpSubCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-403">·         TrvExpSubCategoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-404">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-404">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-405">·         TrvExpSubCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-405">·         TrvExpSubCategoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-406">経費精算書の支払方法</span><span class="sxs-lookup"><span data-stu-id="353e7-406">Expense report payment method</span></span>

<span data-ttu-id="353e7-407">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-407">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-408">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-408">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="353e7-409">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-409">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-410">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-410">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="353e7-411">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-411">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-412">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-412">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="353e7-413">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-413">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-414">·         TrvPayMethodEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-414">·         TrvPayMethodEntity\_Basic</span></span>

<span data-ttu-id="353e7-415">経費精算書カテゴリのコード マッピング</span><span class="sxs-lookup"><span data-stu-id="353e7-415">Expense report category code mapping</span></span>

<span data-ttu-id="353e7-416">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-416">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-417">·         TrvPBSCatCodesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-417">·         TrvPBSCatCodesEntity\_Basic</span></span>

<span data-ttu-id="353e7-418">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-418">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-419">·         TrvPBSCatCodesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-419">·         TrvPBSCatCodesEntity\_Basic</span></span>

<span data-ttu-id="353e7-420">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-420">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-421">·         TrvPBSCatCodeEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-421">·         TrvPBSCatCodeEntity\_Basic</span></span>

<span data-ttu-id="353e7-422">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-422">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-423">·         TrvPBSCatCodesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-423">·         TrvPBSCatCodesEntity\_Basic</span></span>

<span data-ttu-id="353e7-424">経費精算書ポリシー</span><span class="sxs-lookup"><span data-stu-id="353e7-424">Expense report policy</span></span>

<span data-ttu-id="353e7-425">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-425">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-426">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-426">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-427">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-427">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-428">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-428">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-429">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-429">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-430">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-430">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-431">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-431">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-432">·         TrvPolicyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-432">·         TrvPolicyEntity\_Basic</span></span>

<span data-ttu-id="353e7-433">経費精算書の検証方法</span><span class="sxs-lookup"><span data-stu-id="353e7-433">Expense report validate payment</span></span>

<span data-ttu-id="353e7-434">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-434">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-435">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-435">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="353e7-436">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-436">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-437">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-437">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="353e7-438">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-438">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-439">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-439">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="353e7-440">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-440">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-441">·         TrvValidatePaymentEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-441">·         TrvValidatePaymentEntity\_Basic</span></span>

<span data-ttu-id="353e7-442">対外貿易</span><span class="sxs-lookup"><span data-stu-id="353e7-442">Foreign trade</span></span>

<span data-ttu-id="353e7-443">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-443">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-444">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-444">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-445">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-445">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-446">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-446">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-447">·         InstrastatStatParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-447">·         InstrastatStatParametersEntity</span></span>

<span data-ttu-id="353e7-448">グローバル アドレス帳パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-448">Global address book parameters</span></span>

<span data-ttu-id="353e7-449">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-449">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-450">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-450">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-451">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-451">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-452">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-452">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-453">·         DirParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-453">·         DirParametersEntity</span></span>

<span data-ttu-id="353e7-454">人事管理</span><span class="sxs-lookup"><span data-stu-id="353e7-454">Human resources</span></span>

<span data-ttu-id="353e7-455">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-455">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-456">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-456">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-457">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-457">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-458">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-458">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-459">·         HRMParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-459">·         HRMParametersEntity</span></span>

<span data-ttu-id="353e7-460">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="353e7-460">Inventory</span></span>

<span data-ttu-id="353e7-461">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-461">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-462">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="353e7-462">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span></span>

<span data-ttu-id="353e7-463">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-463">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-464">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="353e7-464">·         InventJournalEntity\_Item defaults ·         InventJournalEntity\_UpdateConfiguration</span></span>

<span data-ttu-id="353e7-465">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-465">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-466">·         InventJournalEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-466">·         InventJournalEntity\_RU</span></span>

<span data-ttu-id="353e7-467">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-467">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-468">·         InventJournalEntity ·         InventJournalEntity\_RU ·         InventParametersEntity ·         InventTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-468">·         InventJournalEntity ·         InventJournalEntity\_RU ·         InventParametersEntity ·         InventTableEntity</span></span>

<span data-ttu-id="353e7-469">在庫在庫の計量単位</span><span class="sxs-lookup"><span data-stu-id="353e7-469">Inventory Inventory unit of measure</span></span>

<span data-ttu-id="353e7-470">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-470">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-471">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-471">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span></span>

<span data-ttu-id="353e7-472">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-472">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-473">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-473">·         UnitOfMeasureEntity\_Basic ·         UnitOfMeasureEntity\_Enum</span></span>

<span data-ttu-id="353e7-474">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-474">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-475">·         UnitOfMeasureEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-475">·         UnitOfMeasureEntity\_Basic</span></span>

<span data-ttu-id="353e7-476">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-476">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-477">·         UnitOfMeasureEntity ·         UnitOfMeasureEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-477">·         UnitOfMeasureEntity ·         UnitOfMeasureEntity\_Basic</span></span>

<span data-ttu-id="353e7-478">職務</span><span class="sxs-lookup"><span data-stu-id="353e7-478">Jobs</span></span>

<span data-ttu-id="353e7-479">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-479">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-480">·         HcmJobDetailsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-480">·         HcmJobDetailsEntity\_Basic</span></span>

<span data-ttu-id="353e7-481">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-481">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-482">·         HcmJobDetailsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-482">·         HcmJobDetailsEntity\_Basic</span></span>

<span data-ttu-id="353e7-483">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-483">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-484">·         HcmJobDetailsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-484">·         HcmJobDetailsEntity\_Basic</span></span>

<span data-ttu-id="353e7-485">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-485">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-486">·         HcmJobDetailEntity ·         HcmJobDetailsEntity\_Basic ·         HcmPositionDetailEntity ·         HcmSharedParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-486">·         HcmJobDetailEntity ·         HcmJobDetailsEntity\_Basic ·         HcmPositionDetailEntity ·         HcmSharedParametersEntity</span></span>

  <span data-ttu-id="353e7-487">Ledger</span><span class="sxs-lookup"><span data-stu-id="353e7-487">Ledger</span></span>

<span data-ttu-id="353e7-488">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-488">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-489">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span><span class="sxs-lookup"><span data-stu-id="353e7-489">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span></span>

<span data-ttu-id="353e7-490">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-490">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-491">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span><span class="sxs-lookup"><span data-stu-id="353e7-491">·         LedgerBalanceEntity\_APPaymentJournal ·         LedgerBalanceEntity\_ARPaymentJournal ·         LedgerBalanceEntity\_GeneralJournal</span></span>

<span data-ttu-id="353e7-492">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-492">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-493">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-493">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU</span></span>

<span data-ttu-id="353e7-494">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-494">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-495">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU ·         LedgerParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-495">·         LedgerJounalEntity\_AU ·         LedgerJournalEntity\_CN ·         LedgerJournalEntity\_ES ·         LedgerJournalEntity\_IN ·         LedgerJournalEntity\_IS ·         LedgerJournalEntity\_LT ·         LedgerJournalEntity\_LV ·         LedgerJournal\_PL ·         LedgerJournalEntity\_RU ·         LedgerParametersEntity</span></span>

<span data-ttu-id="353e7-496">主勘定</span><span class="sxs-lookup"><span data-stu-id="353e7-496">Main account</span></span>

<span data-ttu-id="353e7-497">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-497">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-498">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span><span class="sxs-lookup"><span data-stu-id="353e7-498">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span></span>

<span data-ttu-id="353e7-499">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-499">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-500">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span><span class="sxs-lookup"><span data-stu-id="353e7-500">·         MAinAccountEntity\_Basic ·         MainAccountEntity\_Dimensions ·         MainAccountEntity\_FinancialStatements</span></span>

<span data-ttu-id="353e7-501">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-501">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-502">·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span><span class="sxs-lookup"><span data-stu-id="353e7-502">·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span></span>

<span data-ttu-id="353e7-503">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-503">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-504">·         MainAccountEntity ·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span><span class="sxs-lookup"><span data-stu-id="353e7-504">·         MainAccountEntity ·         MainAccountEntity\_BR ·         MainAccountEntity\_ES</span></span>

<span data-ttu-id="353e7-505">マイレージ レート層</span><span class="sxs-lookup"><span data-stu-id="353e7-505">Mileage rate tiers</span></span>

<span data-ttu-id="353e7-506">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-506">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-507">·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-507">·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="353e7-508">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-508">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-509">·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-509">·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="353e7-510">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-510">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-511">·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-511">·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="353e7-512">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-512">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-513">·         TrvCostTypeRatesEntity ·         TrvCostTypeRatesEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-513">·         TrvCostTypeRatesEntity ·         TrvCostTypeRatesEntity\_Basic</span></span>

<span data-ttu-id="353e7-514">整理番号</span><span class="sxs-lookup"><span data-stu-id="353e7-514">Number sequence</span></span>

<span data-ttu-id="353e7-515">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-515">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-516">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-516">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-517">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-517">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-518">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-518">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-519">·         NumberSequenceTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-519">·         NumberSequenceTableEntity</span></span>

<span data-ttu-id="353e7-520">Office アドイン</span><span class="sxs-lookup"><span data-stu-id="353e7-520">Office Add-ins</span></span>

<span data-ttu-id="353e7-521">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-521">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-522">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-522">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-523">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-523">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-524">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-524">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-525">·         DocuDataSourceEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-525">·         DocuDataSourceEntity</span></span>

<span data-ttu-id="353e7-526">Operations リソース</span><span class="sxs-lookup"><span data-stu-id="353e7-526">Operations resources</span></span>

<span data-ttu-id="353e7-527">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-527">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-528">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-528">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-529">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-529">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-530">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-530">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-531">·         WrkCtrParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-531">·         WrkCtrParametersEntity</span></span>

<span data-ttu-id="353e7-532">組織</span><span class="sxs-lookup"><span data-stu-id="353e7-532">Organization</span></span>

<span data-ttu-id="353e7-533">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-533">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-534">·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-534">·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-535">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-535">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-536">·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-536">·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-537">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-537">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-538">·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-538">·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-539">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-539">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-540">·         OMHierarchyEntity ·         OMOperatingUnitEntity ·         OrganizationHierarchyEntity ·         OrganizationHierarchyEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-540">·         OMHierarchyEntity ·         OMOperatingUnitEntity ·         OrganizationHierarchyEntity ·         OrganizationHierarchyEntity\_Basic</span></span>

<span data-ttu-id="353e7-541">Outlook</span><span class="sxs-lookup"><span data-stu-id="353e7-541">Outlook</span></span>

<span data-ttu-id="353e7-542">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-542">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-543">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-543">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-544">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-544">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-545">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-545">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-546">·         SmmParametersTableEntity ·         SysEmailParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-546">·         SmmParametersTableEntity ·         SysEmailParametersEntity</span></span>

<span data-ttu-id="353e7-547">Payroll</span><span class="sxs-lookup"><span data-stu-id="353e7-547">Payroll</span></span>

<span data-ttu-id="353e7-548">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-548">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-549">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-549">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-550">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-550">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-551">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-551">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-552">·         PRLPayrollParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-552">·         PRLPayrollParametersEntity</span></span>

<span data-ttu-id="353e7-553">ポリシー</span><span class="sxs-lookup"><span data-stu-id="353e7-553">Policies</span></span>

<span data-ttu-id="353e7-554">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-554">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-555">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-555">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-556">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-556">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-557">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-557">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-558">·         SysPolicySourceDocumentRuleEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-558">·         SysPolicySourceDocumentRuleEntity</span></span>

<span data-ttu-id="353e7-559">職位</span><span class="sxs-lookup"><span data-stu-id="353e7-559">Positions</span></span>

<span data-ttu-id="353e7-560">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-560">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-561">·         PositionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-561">·         PositionsEntity\_Basic</span></span>

<span data-ttu-id="353e7-562">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-562">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-563">·         PostionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-563">·         PostionsEntity\_Basic</span></span>

<span data-ttu-id="353e7-564">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-564">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-565">·         PositionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-565">·         PositionsEntity\_Basic</span></span>

<span data-ttu-id="353e7-566">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-566">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-567">·         PositionsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-567">·         PositionsEntity\_Basic</span></span>

<span data-ttu-id="353e7-568">PriceDiscount</span><span class="sxs-lookup"><span data-stu-id="353e7-568">PriceDiscount</span></span>

<span data-ttu-id="353e7-569">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-569">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-570">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span><span class="sxs-lookup"><span data-stu-id="353e7-570">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span></span>

<span data-ttu-id="353e7-571">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-571">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-572">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span><span class="sxs-lookup"><span data-stu-id="353e7-572">·         PriceDiscEntity\_DiscountJournal ·         PriceDiscEntity\_Enum ·         PriceDiscEntity\_Price-And-DiscJournal</span></span>

<span data-ttu-id="353e7-573">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-573">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-574">·         PriceDiscountEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-574">·         PriceDiscountEntity\_RU</span></span>

<span data-ttu-id="353e7-575">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-575">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-576">·         PriceDiscAdmTransEntity ·         PriceDiscountEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-576">·         PriceDiscAdmTransEntity ·         PriceDiscountEntity\_RU</span></span>

<span data-ttu-id="353e7-577">品目</span><span class="sxs-lookup"><span data-stu-id="353e7-577">Product</span></span>

<span data-ttu-id="353e7-578">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-578">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-579">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchaseSalesInvent</span><span class="sxs-lookup"><span data-stu-id="353e7-579">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchaseSalesInvent</span></span>

<span data-ttu-id="353e7-580">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-580">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-581">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchSalesInvent</span><span class="sxs-lookup"><span data-stu-id="353e7-581">·         ProductEntity\_DimensionGroups ·         ProductEntity\_PurchSalesInvent</span></span>

<span data-ttu-id="353e7-582">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-582">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-583">·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-583">·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU</span></span>

<span data-ttu-id="353e7-584">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-584">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-585">·         ProdParametersEntity ·         ProductEntity ·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU ·         ProductMasterEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-585">·         ProdParametersEntity ·         ProductEntity ·         ProductEntityEntity\_Basic ·         ProductEntityEntity\_BR ·         ProductEntityEntity\_IN ·         ProductEntityEntity\_RU ·         ProductMasterEntity</span></span>

<span data-ttu-id="353e7-586">Project</span><span class="sxs-lookup"><span data-stu-id="353e7-586">Project</span></span>

<span data-ttu-id="353e7-587">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-587">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-588">·         ProjectEtnity\_Basic ·         ProjectEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-588">·         ProjectEtnity\_Basic ·         ProjectEntity\_Enum</span></span>

<span data-ttu-id="353e7-589">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-589">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-590">·         ProjectEntity\_Basic ·         ProjectEntity\_Enum</span><span class="sxs-lookup"><span data-stu-id="353e7-590">·         ProjectEntity\_Basic ·         ProjectEntity\_Enum</span></span>

<span data-ttu-id="353e7-591">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-591">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-592">·         ProjectEntity\_PSA</span><span class="sxs-lookup"><span data-stu-id="353e7-592">·         ProjectEntity\_PSA</span></span>

<span data-ttu-id="353e7-593">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-593">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-594">·         ProjectEntity\_PSA ·         ProjInvoiceTableEntity ·         ProjJournalTransEntity ·         ProjOnAccTransEntity ·         ProjServerSettingsEntity ·         ProjTableEntitySyncParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-594">·         ProjectEntity\_PSA ·         ProjInvoiceTableEntity ·         ProjJournalTransEntity ·         ProjOnAccTransEntity ·         ProjServerSettingsEntity ·         ProjTableEntitySyncParametersEntity</span></span>

<span data-ttu-id="353e7-595">ProjectHourJournal</span><span class="sxs-lookup"><span data-stu-id="353e7-595">ProjectHourJournal</span></span>

<span data-ttu-id="353e7-596">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-596">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-597">·         ProjectHourJournalEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-597">·         ProjectHourJournalEntity\_Basic</span></span>

<span data-ttu-id="353e7-598">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-598">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-599">·         ProjectHourJournalEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-599">·         ProjectHourJournalEntity\_Basic</span></span>

<span data-ttu-id="353e7-600">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-600">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-601">·         ProjectHourEntity\_PSA</span><span class="sxs-lookup"><span data-stu-id="353e7-601">·         ProjectHourEntity\_PSA</span></span>

<span data-ttu-id="353e7-602">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-602">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-603">·         ProjectHourEntity\_PSA</span><span class="sxs-lookup"><span data-stu-id="353e7-603">·         ProjectHourEntity\_PSA</span></span>

<span data-ttu-id="353e7-604">PurchLine</span><span class="sxs-lookup"><span data-stu-id="353e7-604">PurchLine</span></span>

<span data-ttu-id="353e7-605">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-605">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-606">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="353e7-606">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span></span>

<span data-ttu-id="353e7-607">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-607">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-608">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="353e7-608">·         PurchLineEntity\_Basic1 ·         PurchLineEntity\_Basic2</span></span>

<span data-ttu-id="353e7-609">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-609">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-610">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="353e7-610">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span></span>

<span data-ttu-id="353e7-611">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-611">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-612">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="353e7-612">·         PurchLineEntity\_Basic ·         PurchLineEntity\_BR ·         PurchLineEntity\_HU ·         PurchLineEntity\_LT</span></span>

<span data-ttu-id="353e7-613">PurchTable</span><span class="sxs-lookup"><span data-stu-id="353e7-613">PurchTable</span></span>

<span data-ttu-id="353e7-614">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-614">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-615">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="353e7-615">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span></span>

<span data-ttu-id="353e7-616">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-616">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-617">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span><span class="sxs-lookup"><span data-stu-id="353e7-617">·         PurchTableEntity\_Basic1 ·         PurchTableEntity\_Basic2</span></span>

<span data-ttu-id="353e7-618">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-618">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-619">·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-619">·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span></span>

<span data-ttu-id="353e7-620">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-620">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-621">·         PurchTableEntity ·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-621">·         PurchTableEntity ·         PurchTableEntity\_Basic ·         PurchTableEntity\_HU ·         PurchTableEntity\_LT ·         PurchTableEntity\_LV ·         PurchTableEntity\_PL</span></span>

<span data-ttu-id="353e7-622">工順</span><span class="sxs-lookup"><span data-stu-id="353e7-622">Route</span></span>

<span data-ttu-id="353e7-623">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-623">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-624">·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-624">·         RouteEntity\_Basic</span></span>

<span data-ttu-id="353e7-625">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-625">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-626">·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-626">·         RouteEntity\_Basic</span></span>

<span data-ttu-id="353e7-627">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-627">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-628">·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-628">·         RouteEntity\_Basic</span></span>

<span data-ttu-id="353e7-629">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-629">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-630">·         RouteEntity ·         RouteEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-630">·         RouteEntity ·         RouteEntity\_Basic</span></span>

<span data-ttu-id="353e7-631">工順工程</span><span class="sxs-lookup"><span data-stu-id="353e7-631">Route operations</span></span>

<span data-ttu-id="353e7-632">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-632">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-633">·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-633">·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="353e7-634">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-634">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-635">·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-635">·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="353e7-636">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-636">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-637">·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-637">·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="353e7-638">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-638">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-639">·         RouteOperationsEntity ·         RouteOperationsEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-639">·         RouteOperationsEntity ·         RouteOperationsEntity\_Basic</span></span>

<span data-ttu-id="353e7-640">SalesLine</span><span class="sxs-lookup"><span data-stu-id="353e7-640">SalesLine</span></span>

<span data-ttu-id="353e7-641">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-641">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-642">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span><span class="sxs-lookup"><span data-stu-id="353e7-642">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span></span>

<span data-ttu-id="353e7-643">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-643">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-644">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span><span class="sxs-lookup"><span data-stu-id="353e7-644">·         SalesLineEntity\_Basic ·         SalesLineEntity\_Basic1 ·         SalesLineEntity\_DefaultsHeader</span></span>

<span data-ttu-id="353e7-645">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-645">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-646">·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="353e7-646">·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span></span>

<span data-ttu-id="353e7-647">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-647">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-648">·         SalesLineEntity ·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span><span class="sxs-lookup"><span data-stu-id="353e7-648">·         SalesLineEntity ·         SalesLineEntity\_HU ·         SalesLineEntity\_RU ·         SalesLineEntity\_LT</span></span>

<span data-ttu-id="353e7-649">SalesTable</span><span class="sxs-lookup"><span data-stu-id="353e7-649">SalesTable</span></span>

<span data-ttu-id="353e7-650">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-650">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-651">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span><span class="sxs-lookup"><span data-stu-id="353e7-651">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span></span>

<span data-ttu-id="353e7-652">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-652">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-653">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span><span class="sxs-lookup"><span data-stu-id="353e7-653">·         SalesTableEntity\_Basic ·         SalesTableEntity\_Basic1</span></span>

<span data-ttu-id="353e7-654">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-654">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-655">·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-655">·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span></span>

<span data-ttu-id="353e7-656">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-656">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-657">·         SalesTableEntity ·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-657">·         SalesTableEntity ·         SalesTableEntity\_HU ·         SalesTableEntity\_IN ·         SalesTableEntity\_LT ·         SalesTableEntity\_LV ·         SalesTableEntity\_PL</span></span>

<span data-ttu-id="353e7-658">サービス管理</span><span class="sxs-lookup"><span data-stu-id="353e7-658">Service management</span></span>

<span data-ttu-id="353e7-659">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-659">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-660">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-660">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-661">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-661">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-662">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-662">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-663">·         SmaParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-663">·         SmaParametersEntity</span></span>

<span data-ttu-id="353e7-664">サーバー コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="353e7-664">Server configuration</span></span>

<span data-ttu-id="353e7-665">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-665">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-666">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-666">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-667">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-667">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-668">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-668">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-669">·         SysServerConfigEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-669">·         SysServerConfigEntity</span></span>

<span data-ttu-id="353e7-670">共有カテゴリ</span><span class="sxs-lookup"><span data-stu-id="353e7-670">Shared categories</span></span>

<span data-ttu-id="353e7-671">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-671">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-672">·         SharedCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-672">·         SharedCategoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-673">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-673">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-674">·         SharedCaegoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-674">·         SharedCaegoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-675">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-675">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-676">·         SharedCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-676">·         SharedCategoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-677">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-677">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-678">·         SharedCategoryEntity ·         SharedCategoryEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-678">·         SharedCategoryEntity ·         SharedCategoryEntity\_Basic</span></span>

<span data-ttu-id="353e7-679">サーバー構成 SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="353e7-679">Server configuration SQL Server Reporting Services</span></span>

<span data-ttu-id="353e7-680">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-680">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-681">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-681">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-682">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-682">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-683">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-683">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-684">·         SRSReportDeploymentEntity ·         SRSServersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-684">·         SRSReportDeploymentEntity ·         SRSServersEntity</span></span>

<span data-ttu-id="353e7-685">定期売買パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-685">Subscription parameters</span></span>

<span data-ttu-id="353e7-686">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-686">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-687">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-687">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-688">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-688">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-689">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-689">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-690">·         SubscriptionParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-690">·         SubscriptionParametersEntity</span></span>

<span data-ttu-id="353e7-691">システム パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-691">System parameters</span></span>

<span data-ttu-id="353e7-692">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-692">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-693">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-693">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-694">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-694">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-695">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-695">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-696">·         SystemParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-696">·         SystemParametersEntity</span></span>

<span data-ttu-id="353e7-697">TaxAuthorityAddress</span><span class="sxs-lookup"><span data-stu-id="353e7-697">TaxAuthorityAddress</span></span>

<span data-ttu-id="353e7-698">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-698">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-699">·         TaxAuthrorityAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-699">·         TaxAuthrorityAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-700">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-700">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-701">·         TaxAuthorityAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-701">·         TaxAuthorityAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-702">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-702">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-703">·         TaxAuthorityAddressEntity\_BR ·         TaxAuthorityAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-703">·         TaxAuthorityAddressEntity\_BR ·         TaxAuthorityAddressEntity\_RU</span></span>

<span data-ttu-id="353e7-704">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-704">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-705">·         TaxAuthorityAddressEntity ·         TaxAuthroityAddressEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-705">·         TaxAuthorityAddressEntity ·         TaxAuthroityAddressEntity\_RU</span></span>

<span data-ttu-id="353e7-706">TaxData</span><span class="sxs-lookup"><span data-stu-id="353e7-706">TaxData</span></span>

<span data-ttu-id="353e7-707">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-707">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-708">·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-708">·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="353e7-709">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-709">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-710">·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-710">·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="353e7-711">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-711">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-712">·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-712">·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="353e7-713">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-713">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-714">·         TaxDataEntity ·         TaxDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-714">·         TaxDataEntity ·         TaxDataEntity\_Basic</span></span>

<span data-ttu-id="353e7-715">TaxGroupData</span><span class="sxs-lookup"><span data-stu-id="353e7-715">TaxGroupData</span></span>

<span data-ttu-id="353e7-716">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-716">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-717">·         TaxGroupDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-717">·         TaxGroupDataEntity\_Basic</span></span>

<span data-ttu-id="353e7-718">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-718">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-719">·         TaxGroupDataEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-719">·         TaxGroupDataEntity\_Basic</span></span>

<span data-ttu-id="353e7-720">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-720">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-721">·         TaxGroupDataEntity\_BR</span><span class="sxs-lookup"><span data-stu-id="353e7-721">·         TaxGroupDataEntity\_BR</span></span>

<span data-ttu-id="353e7-722">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-722">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-723">·         TaxGroupDataEntity ·         TaxGroupDataEntity\_BR</span><span class="sxs-lookup"><span data-stu-id="353e7-723">·         TaxGroupDataEntity ·         TaxGroupDataEntity\_BR</span></span>

<span data-ttu-id="353e7-724">TaxGroupHeading</span><span class="sxs-lookup"><span data-stu-id="353e7-724">TaxGroupHeading</span></span>

<span data-ttu-id="353e7-725">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-725">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-726">·         TaxGroupHeadingEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-726">·         TaxGroupHeadingEntity\_Basic</span></span>

<span data-ttu-id="353e7-727">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-727">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-728">·         TaxGroupHeadingEntity\_\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-728">·         TaxGroupHeadingEntity\_\_Basic</span></span>

<span data-ttu-id="353e7-729">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-729">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-730">·         TaxGroupHeadingEntity\_W</span><span class="sxs-lookup"><span data-stu-id="353e7-730">·         TaxGroupHeadingEntity\_W</span></span>

<span data-ttu-id="353e7-731">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-731">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-732">·         TaxGroupHeadingEntity ·         TaxGroupHeadingEntity\_W</span><span class="sxs-lookup"><span data-stu-id="353e7-732">·         TaxGroupHeadingEntity ·         TaxGroupHeadingEntity\_W</span></span>

<span data-ttu-id="353e7-733">TaxItemGroupHeading</span><span class="sxs-lookup"><span data-stu-id="353e7-733">TaxItemGroupHeading</span></span>

<span data-ttu-id="353e7-734">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-734">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-735">·         TaxItemGroupHeadingEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-735">·         TaxItemGroupHeadingEntity\_Basic</span></span>

<span data-ttu-id="353e7-736">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-736">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-737">·         TaxItemGroupHeadingEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-737">·         TaxItemGroupHeadingEntity\_Basic</span></span>

<span data-ttu-id="353e7-738">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-738">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-739">·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="353e7-739">·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span></span>

<span data-ttu-id="353e7-740">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-740">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-741">·         TaxItemGroupHeadingEntity ·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="353e7-741">·         TaxItemGroupHeadingEntity ·         TaxItemGroupHeadingEntity\_HU ·         TaxItemGroupHeadingEntity\_IN</span></span>

<span data-ttu-id="353e7-742">TaxLedgerAccountGroup</span><span class="sxs-lookup"><span data-stu-id="353e7-742">TaxLedgerAccountGroup</span></span>  

<span data-ttu-id="353e7-743">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-743">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-744">·         TaxLedgerAccountGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-744">·         TaxLedgerAccountGroupEntity\_Basic</span></span>

<span data-ttu-id="353e7-745">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-745">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-746">·         TaxLedgerAccountGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-746">·         TaxLedgerAccountGroupEntity\_Basic</span></span>

<span data-ttu-id="353e7-747">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-747">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-748">·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-748">·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span></span>

<span data-ttu-id="353e7-749">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-749">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-750">·         TaxLedgerAccountGroupEntity ·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-750">·         TaxLedgerAccountGroupEntity ·         TaxLedgerAccountGroupEntity\_Basic ·         TaxLedgerAccountGroupEntity\_BR ·         TaxLedgerAccountGroupEntity\_HU ·         TaxLedgerAccountGroupEntity\_RU</span></span>

<span data-ttu-id="353e7-751">TaxOnItem</span><span class="sxs-lookup"><span data-stu-id="353e7-751">TaxOnItem</span></span>

<span data-ttu-id="353e7-752">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-752">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-753">·         TaxOnItemEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-753">·         TaxOnItemEntity\_Basic</span></span>

<span data-ttu-id="353e7-754">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-754">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-755">·         TaxOnItemEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-755">·         TaxOnItemEntity\_Basic</span></span>

<span data-ttu-id="353e7-756">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-756">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-757">·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="353e7-757">·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span></span>

<span data-ttu-id="353e7-758">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-758">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-759">·         TaxOnItemEntity ·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span><span class="sxs-lookup"><span data-stu-id="353e7-759">·         TaxOnItemEntity ·         TaxOnItemEntity\_BR ·         TaxOnItemEntity\_IN</span></span>

<span data-ttu-id="353e7-760">TaxParameters</span><span class="sxs-lookup"><span data-stu-id="353e7-760">TaxParameters</span></span>

<span data-ttu-id="353e7-761">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-761">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-762">·         TaxParametersEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-762">·         TaxParametersEntity\_Basic</span></span>

<span data-ttu-id="353e7-763">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-763">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-764">·         TaxParametersEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-764">·         TaxParametersEntity\_Basic</span></span>

<span data-ttu-id="353e7-765">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-765">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-766">·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-766">·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span></span>

<span data-ttu-id="353e7-767">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-767">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-768">·         TaxParametersEntity ·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-768">·         TaxParametersEntity ·         TaxParametersEntity\_CZ ·         TaxParametersEntity\_IN ·         TaxParametersEntity\_RU</span></span>

<span data-ttu-id="353e7-769">TaxPeriodHead</span><span class="sxs-lookup"><span data-stu-id="353e7-769">TaxPeriodHead</span></span>

<span data-ttu-id="353e7-770">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-770">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-771">·         TaxPeriodHeadEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-771">·         TaxPeriodHeadEntity\_Basic</span></span>

<span data-ttu-id="353e7-772">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-772">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-773">·         TaxPeriodHeadEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-773">·         TaxPeriodHeadEntity\_Basic</span></span>

<span data-ttu-id="353e7-774">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-774">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-775">·         TaxPeriodHeadEntity\_HU</span><span class="sxs-lookup"><span data-stu-id="353e7-775">·         TaxPeriodHeadEntity\_HU</span></span>

<span data-ttu-id="353e7-776">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-776">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-777">·         TaxPeriodHeadEntity ·         TaxPeriodHead\_HU</span><span class="sxs-lookup"><span data-stu-id="353e7-777">·         TaxPeriodHeadEntity ·         TaxPeriodHead\_HU</span></span>

<span data-ttu-id="353e7-778">TaxTable</span><span class="sxs-lookup"><span data-stu-id="353e7-778">TaxTable</span></span>  

<span data-ttu-id="353e7-779">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-779">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-780">·         TaxTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-780">·         TaxTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-781">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-781">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-782">·         TaxTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-782">·         TaxTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-783">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-783">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-784">·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span><span class="sxs-lookup"><span data-stu-id="353e7-784">·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span></span>

<span data-ttu-id="353e7-785">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-785">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-786">·         TaxTableEntity ·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span><span class="sxs-lookup"><span data-stu-id="353e7-786">·         TaxTableEntity ·         TaxTableEntity\_BR ·         TaxTableEntity\_IN ·         TaxTableEntity\_RU ·         TaxTableEntity\_TH</span></span>

<span data-ttu-id="353e7-787">仕入先グループ</span><span class="sxs-lookup"><span data-stu-id="353e7-787">Vendor group</span></span>

<span data-ttu-id="353e7-788">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-788">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-789">·         VendGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-789">·         VendGroupEntity\_Basic</span></span>

<span data-ttu-id="353e7-790">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-790">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-791">·         VendGroupEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-791">·         VendGroupEntity\_Basic</span></span>

<span data-ttu-id="353e7-792">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-792">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-793">·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-793">·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span></span>

<span data-ttu-id="353e7-794">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-794">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-795">·         VendGroupEntity ·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span><span class="sxs-lookup"><span data-stu-id="353e7-795">·         VendGroupEntity ·         VendGroupEntity\_Basic ·         VendGroupEntity\_PL</span></span>

<span data-ttu-id="353e7-796">ベンダー</span><span class="sxs-lookup"><span data-stu-id="353e7-796">Vendor</span></span>

<span data-ttu-id="353e7-797">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-797">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-798">·         VendorEntity\_Address ·         VendorEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-798">·         VendorEntity\_Address ·         VendorEntity\_Basic</span></span>

<span data-ttu-id="353e7-799">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-799">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-800">·         VendorEntity\_Address ·         VendorEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-800">·         VendorEntity\_Address ·         VendorEntity\_Basic</span></span>

<span data-ttu-id="353e7-801">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-801">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-802">·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-802">·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span></span>

<span data-ttu-id="353e7-803">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-803">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-804">·         VendorEntity ·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span><span class="sxs-lookup"><span data-stu-id="353e7-804">·         VendorEntity ·         VendorEntity\_Basic ·         VendorEntity\_BR ·         VendorEntity\_PL ·         VendorEntity\_RU</span></span>

<span data-ttu-id="353e7-805">仕入先の住所</span><span class="sxs-lookup"><span data-stu-id="353e7-805">Vendor address</span></span>

<span data-ttu-id="353e7-806">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-806">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-807">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MultipeAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-807">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MultipeAddressValues</span></span>

<span data-ttu-id="353e7-808">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-808">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-809">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MulitipleAddressValues</span><span class="sxs-lookup"><span data-stu-id="353e7-809">·         VendorAddressEntity\_Basic ·         VendorAddressEntity\_MulitipleAddressValues</span></span>

<span data-ttu-id="353e7-810">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-810">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-811">·         VendorAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-811">·         VendorAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-812">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-812">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-813">·         VendorAddressEntity ·         VendorAddressEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-813">·         VendorAddressEntity ·         VendorAddressEntity\_Basic</span></span>

<span data-ttu-id="353e7-814">仕入先請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="353e7-814">Vendor invoice header</span></span>  

<span data-ttu-id="353e7-815">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-815">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-816">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-816">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-817">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-817">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-818">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-818">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-819">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-819">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-820">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-820">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-821">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-821">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-822">·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-822">·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-823">仕入先請求明細行</span><span class="sxs-lookup"><span data-stu-id="353e7-823">Vendor invoice line</span></span>    

<span data-ttu-id="353e7-824">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-824">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-825">·         VendInvoiceInfoLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-825">·         VendInvoiceInfoLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-826">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-826">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-827">·         VendInvoiceInfoLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-827">·         VendInvoiceInfoLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-828">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-828">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-829">·         VendInvoiceInfoLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-829">·         VendInvoiceInfoLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-830">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-830">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-831">·         VendInvoiceInfoLineEntity\_Basci</span><span class="sxs-lookup"><span data-stu-id="353e7-831">·         VendInvoiceInfoLineEntity\_Basci</span></span>

<span data-ttu-id="353e7-832">仕入先請求書テーブル</span><span class="sxs-lookup"><span data-stu-id="353e7-832">Vendor invoice table</span></span>

<span data-ttu-id="353e7-833">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-833">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-834">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-834">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-835">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-835">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-836">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-836">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-837">·         VendInvoiceInfoTableEntity ·         VendInvoiceInfoTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-837">·         VendInvoiceInfoTableEntity ·         VendInvoiceInfoTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-838">仕入先請求書パラメーター</span><span class="sxs-lookup"><span data-stu-id="353e7-838">Vendor invoice parameters</span></span>  

<span data-ttu-id="353e7-839">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-839">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-840">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-840">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-841">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-841">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-842">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-842">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-843">·         VendParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-843">·         VendParametersEntity</span></span>

<span data-ttu-id="353e7-844">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="353e7-844">Work Calendar</span></span>

<span data-ttu-id="353e7-845">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-845">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-846">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-846">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-847">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-847">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-848">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-848">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-849">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-849">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-850">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-850">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-851">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-851">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-852">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-852">·         WorkCalendarDateEntity\_Basic ·         WorkCalendarDateLineEntity\_Basic ·         WorkCalendarTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-853">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="353e7-853">Workflow</span></span>    

<span data-ttu-id="353e7-854">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-854">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-855">·         WorkflowWorkItemQueueEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-855">·         WorkflowWorkItemQueueEntity\_Basic</span></span>

<span data-ttu-id="353e7-856">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-856">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-857">·         WorkflowWorkItemQueueEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-857">·         WorkflowWorkItemQueueEntity\_Basic</span></span>

<span data-ttu-id="353e7-858">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-858">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-859">·         WorkflowWorkItemQueueEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-859">·         WorkflowWorkItemQueueEntity\_Basic</span></span>

<span data-ttu-id="353e7-860">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-860">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-861">·         WorkflowTableEntity ·         WorkflowWorkItemQueueEntity ·         WorkflowWorkItemQueueEntity\_basic</span><span class="sxs-lookup"><span data-stu-id="353e7-861">·         WorkflowTableEntity ·         WorkflowWorkItemQueueEntity ·         WorkflowWorkItemQueueEntity\_basic</span></span>

<span data-ttu-id="353e7-862">WorkTimeLine</span><span class="sxs-lookup"><span data-stu-id="353e7-862">WorkTimeLine</span></span>

<span data-ttu-id="353e7-863">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-863">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-864">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-864">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-865">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-865">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-866">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-866">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-867">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-867">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-868">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-868">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-869">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-869">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-870">·         WorkTimeLineEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-870">·         WorkTimeLineEntity\_Basic</span></span>

<span data-ttu-id="353e7-871">WorkTimeTable</span><span class="sxs-lookup"><span data-stu-id="353e7-871">WorkTimeTable</span></span>      

<span data-ttu-id="353e7-872">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="353e7-872">Dynamics AX 2012</span></span>

<span data-ttu-id="353e7-873">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-873">·         WorkTimeTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-874">Microsoft Dynamics AX 2012 Feature Pack </span><span class="sxs-lookup"><span data-stu-id="353e7-874">Microsoft Dynamics AX 2012 Feature Pack</span></span>

<span data-ttu-id="353e7-875">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-875">·         WorkTimeTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-876">Microsoft Dynamics AX 2012 (InformationSource)</span><span class="sxs-lookup"><span data-stu-id="353e7-876">Microsoft Dynamics AX 2012 (InformationSource)</span></span>

<span data-ttu-id="353e7-877">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-877">·         WorkTimeTableEntity\_Basic</span></span>

<span data-ttu-id="353e7-878">Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3 の累積更新プログラム 7</span><span class="sxs-lookup"><span data-stu-id="353e7-878">cumulative update 7 for Microsoft Dynamics AX 2012 R2/Microsoft Dynamics AX 2012 R3</span></span>

<span data-ttu-id="353e7-879">·         WorkTimeTableEntity\_Basic</span><span class="sxs-lookup"><span data-stu-id="353e7-879">·         WorkTimeTableEntity\_Basic</span></span>



## <a name="xml-demo-files"></a><span data-ttu-id="353e7-880">XML デモ ファイル</span><span class="sxs-lookup"><span data-stu-id="353e7-880">XML demo files</span></span>
<span data-ttu-id="353e7-881">次のファイルは、Microsoft Dynamics AX 2012 R2 および AX 2012 R3 の累積的な更新プログラム 7 と共に出荷されるデータ インポート/エクスポート フレームワークのバージョンで使用できます。</span><span class="sxs-lookup"><span data-stu-id="353e7-881">The following files are available in the versions of Data Import/Export Framework that ship with cumulative update 7 for Microsoft Dynamics AX 2012 R2 and AX 2012 R3.</span></span>

|                                   |                                   |
|-----------------------------------|-----------------------------------|
| <span data-ttu-id="353e7-882">AifInboundPortEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-882">AifInboundPortEntity</span></span>              | <span data-ttu-id="353e7-883">ProjInvoiceTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-883">ProjInvoiceTableEntity</span></span>            |
| <span data-ttu-id="353e7-884">AifLookupEntryEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-884">AifLookupEntryEntity</span></span>              | <span data-ttu-id="353e7-885">ProjJournalTransEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-885">ProjJournalTransEntity</span></span>            |
| <span data-ttu-id="353e7-886">AifOutboundPortEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-886">AifOutboundPortEntity</span></span>             | <span data-ttu-id="353e7-887">ProjOnAccTransEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-887">ProjOnAccTransEntity</span></span>              |
| <span data-ttu-id="353e7-888">AIfWebSitesEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-888">AIfWebSitesEntity</span></span>                 | <span data-ttu-id="353e7-889">ProjServerSettingsEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-889">ProjServerSettingsEntity</span></span>          |
| <span data-ttu-id="353e7-890">AssetEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-890">AssetEntity</span></span>                       | <span data-ttu-id="353e7-891">ProjTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-891">ProjTableEntity</span></span>                   |
| <span data-ttu-id="353e7-892">AssetParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-892">AssetParametersEntity</span></span>             | <span data-ttu-id="353e7-893">PurchLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-893">PurchLineEntity</span></span>                   |
| <span data-ttu-id="353e7-894">BankParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-894">BankParametersEntity</span></span>              | <span data-ttu-id="353e7-895">PurchTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-895">PurchTableEntity</span></span>                  |
| <span data-ttu-id="353e7-896">BarCodeSetupEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-896">BarCodeSetupEntity</span></span>                | <span data-ttu-id="353e7-897">RouteEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-897">RouteEntity</span></span>                       |
| <span data-ttu-id="353e7-898">BatchGroupEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-898">BatchGroupEntity</span></span>                  | <span data-ttu-id="353e7-899">RouteOperationsEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-899">RouteOperationsEntity</span></span>             |
| <span data-ttu-id="353e7-900">BIConfigurationEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-900">BIConfigurationEntity</span></span>             | <span data-ttu-id="353e7-901">SalesLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-901">SalesLineEntity</span></span>                   |
| <span data-ttu-id="353e7-902">BITimePeriodsMDXEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-902">BITimePeriodsMDXEntity</span></span>            | <span data-ttu-id="353e7-903">SalesTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-903">SalesTableEntity</span></span>                  |
| <span data-ttu-id="353e7-904">BOMEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-904">BOMEntity</span></span>                         | <span data-ttu-id="353e7-905">SharedCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-905">SharedCategoryEntity</span></span>              |
| <span data-ttu-id="353e7-906">BOMVersionEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-906">BOMVersionEntity</span></span>                  | <span data-ttu-id="353e7-907">SIGParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-907">SIGParametersEntity</span></span>               |
| <span data-ttu-id="353e7-908">BudgetParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-908">BudgetParametersEntity</span></span>            | <span data-ttu-id="353e7-909">SmaParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-909">SmaParametersEntity</span></span>               |
| <span data-ttu-id="353e7-910">BudgetTransactionLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-910">BudgetTransactionLineEntity</span></span>       | <span data-ttu-id="353e7-911">SmmParametersTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-911">SmmParametersTableEntity</span></span>          |
| <span data-ttu-id="353e7-912">CategoryTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-912">CategoryTableEntity</span></span>               | <span data-ttu-id="353e7-913">SRSReportDeploymentEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-913">SRSReportDeploymentEntity</span></span>         |
| <span data-ttu-id="353e7-914">CollabSiteParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-914">CollabSiteParametersEntity</span></span>        | <span data-ttu-id="353e7-915">SRSServersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-915">SRSServersEntity</span></span>                  |
| <span data-ttu-id="353e7-916">ContactPersonAddressEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-916">ContactPersonAddressEntity</span></span>        | <span data-ttu-id="353e7-917">SubscriptionParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-917">SubscriptionParametersEntity</span></span>      |
| <span data-ttu-id="353e7-918">ContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-918">ContactPersonEntity</span></span>               | <span data-ttu-id="353e7-919">SyncParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-919">SyncParametersEntity</span></span>              |
| <span data-ttu-id="353e7-920">ContentTypeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-920">ContentTypeEntity</span></span>                 | <span data-ttu-id="353e7-921">SysEmailParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-921">SysEmailParametersEntity</span></span>          |
| <span data-ttu-id="353e7-922">COSParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-922">COSParametersEntity</span></span>               | <span data-ttu-id="353e7-923">SysPolicySourceDocumentRuleEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-923">SysPolicySourceDocumentRuleEntity</span></span> |
| <span data-ttu-id="353e7-924">CustomerAddressEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-924">CustomerAddressEntity</span></span>             | <span data-ttu-id="353e7-925">SysServerConfigEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-925">SysServerConfigEntity</span></span>             |
| <span data-ttu-id="353e7-926">CustomerEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-926">CustomerEntity</span></span>                    | <span data-ttu-id="353e7-927">SystemParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-927">SystemParametersEntity</span></span>            |
| <span data-ttu-id="353e7-928">CustVendAIFPaymTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-928">CustVendAIFPaymTableEntity</span></span>        | <span data-ttu-id="353e7-929">TaxAuthorityAddressEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-929">TaxAuthorityAddressEntity</span></span>         |
| <span data-ttu-id="353e7-930">DimensionAttributeValueEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-930">DimensionAttributeValueEntity</span></span>     | <span data-ttu-id="353e7-931">TaxDataEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-931">TaxDataEntity</span></span>                     |
| <span data-ttu-id="353e7-932">DimensionHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-932">DimensionHierarchyEntity</span></span>          | <span data-ttu-id="353e7-933">TaxGroupDataEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-933">TaxGroupDataEntity</span></span>                |
| <span data-ttu-id="353e7-934">DirParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-934">DirParametersEntity</span></span>               | <span data-ttu-id="353e7-935">TaxGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-935">TaxGroupHeadingEntity</span></span>             |
| <span data-ttu-id="353e7-936">DocuDataSourceEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-936">DocuDataSourceEntity</span></span>              | <span data-ttu-id="353e7-937">TaxItemGroupHeadingEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-937">TaxItemGroupHeadingEntity</span></span>         |
| <span data-ttu-id="353e7-938">DocuTableEnabledEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-938">DocuTableEnabledEntity</span></span>            | <span data-ttu-id="353e7-939">TaxLedgerAccountGroupEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-939">TaxLedgerAccountGroupEntity</span></span>       |
| <span data-ttu-id="353e7-940">DocuTypeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-940">DocuTypeEntity</span></span>                    | <span data-ttu-id="353e7-941">TaxOnItemEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-941">TaxOnItemEntity</span></span>                   |
| <span data-ttu-id="353e7-942">EcoResAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-942">EcoResAttributeEntity</span></span>             | <span data-ttu-id="353e7-943">TaxParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-943">TaxParametersEntity</span></span>               |
| <span data-ttu-id="353e7-944">EcoResAttributeTypeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-944">EcoResAttributeTypeEntity</span></span>         | <span data-ttu-id="353e7-945">TaxPeriodHeadEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-945">TaxPeriodHeadEntity</span></span>               |
| <span data-ttu-id="353e7-946">EcoResCategoryHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-946">EcoResCategoryHierarchyEntity</span></span>     | <span data-ttu-id="353e7-947">TaxTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-947">TaxTableEntity</span></span>                    |
| <span data-ttu-id="353e7-948">EcoResCategoryHierarchyRoleEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-948">EcoResCategoryHierarchyRoleEntity</span></span> | <span data-ttu-id="353e7-949">TrvAppEmplSubEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-949">TrvAppEmplSubEntity</span></span>               |
| <span data-ttu-id="353e7-950">EmployeeAddressEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-950">EmployeeAddressEntity</span></span>             | <span data-ttu-id="353e7-951">TrvCostTypeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-951">TrvCostTypeEntity</span></span>                 |
| <span data-ttu-id="353e7-952">EmployeeEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-952">EmployeeEntity</span></span>                    | <span data-ttu-id="353e7-953">TrvCostTypeRatesEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-953">TrvCostTypeRatesEntity</span></span>            |
| <span data-ttu-id="353e7-954">EMSParameterEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-954">EMSParameterEntity</span></span>                | <span data-ttu-id="353e7-955">TrvExpSubCategoryEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-955">TrvExpSubCategoryEntity</span></span>           |
| <span data-ttu-id="353e7-956">EPDocuParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-956">EPDocuParametersEntity</span></span>            | <span data-ttu-id="353e7-957">TrvParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-957">TrvParametersEntity</span></span>               |
| <span data-ttu-id="353e7-958">HcmJobDetailEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-958">HcmJobDetailEntity</span></span>                | <span data-ttu-id="353e7-959">TrvPayMethodEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-959">TrvPayMethodEntity</span></span>                |
| <span data-ttu-id="353e7-960">HcmPositionDetailEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-960">HcmPositionDetailEntity</span></span>           | <span data-ttu-id="353e7-961">TrvPBSCatCodesEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-961">TrvPBSCatCodesEntity</span></span>              |
| <span data-ttu-id="353e7-962">HcmSharedParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-962">HcmSharedParametersEntity</span></span>         | <span data-ttu-id="353e7-963">TrvPolicyEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-963">TrvPolicyEntity</span></span>                   |
| <span data-ttu-id="353e7-964">HRMParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-964">HRMParametersEntity</span></span>               | <span data-ttu-id="353e7-965">TrvValidatePaymentEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-965">TrvValidatePaymentEntity</span></span>          |
| <span data-ttu-id="353e7-966">IntrastatStateParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-966">IntrastatStateParametersEntity</span></span>    | <span data-ttu-id="353e7-967">UnitOfMeasureEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-967">UnitOfMeasureEntity</span></span>               |
| <span data-ttu-id="353e7-968">InventJournalEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-968">InventJournalEntity</span></span>               | <span data-ttu-id="353e7-969">VendGroupEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-969">VendGroupEntity</span></span>                   |
| <span data-ttu-id="353e7-970">InventParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-970">InventParametersEntity</span></span>            | <span data-ttu-id="353e7-971">VendInvoiceInfoLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-971">VendInvoiceInfoLineEntity</span></span>         |
| <span data-ttu-id="353e7-972">InventTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-972">InventTableEntity</span></span>                 | <span data-ttu-id="353e7-973">VendInvoiceInfoTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-973">VendInvoiceInfoTableEntity</span></span>        |
| <span data-ttu-id="353e7-974">LedgerJournalEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-974">LedgerJournalEntity</span></span>               | <span data-ttu-id="353e7-975">VendorAddressEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-975">VendorAddressEntity</span></span>               |
| <span data-ttu-id="353e7-976">LedgerParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-976">LedgerParametersEntity</span></span>            | <span data-ttu-id="353e7-977">VendorEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-977">VendorEntity</span></span>                      |
| <span data-ttu-id="353e7-978">MainAccountEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-978">MainAccountEntity</span></span>                 | <span data-ttu-id="353e7-979">VendParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-979">VendParametersEntity</span></span>              |
| <span data-ttu-id="353e7-980">OMHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-980">OMHierarchyEntity</span></span>                 | <span data-ttu-id="353e7-981">WorkCalendarDateEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-981">WorkCalendarDateEntity</span></span>            |
| <span data-ttu-id="353e7-982">OMOperatingUnitEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-982">OMOperatingUnitEntity</span></span>             | <span data-ttu-id="353e7-983">WorkCalendarDateLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-983">WorkCalendarDateLineEntity</span></span>        |
| <span data-ttu-id="353e7-984">OrganizationHierarchyEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-984">OrganizationHierarchyEntity</span></span>       | <span data-ttu-id="353e7-985">WorkCalendarTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-985">WorkCalendarTableEntity</span></span>           |
| <span data-ttu-id="353e7-986">PriceDiscAdmTransEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-986">PriceDiscAdmTransEntity</span></span>           | <span data-ttu-id="353e7-987">WorkflowTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-987">WorkflowTableEntity</span></span>               |
| <span data-ttu-id="353e7-988">PRLPayrollParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-988">PRLPayrollParametersEntity</span></span>        | <span data-ttu-id="353e7-989">WorkflowWorkItemQueueEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-989">WorkflowWorkItemQueueEntity</span></span>       |
| <span data-ttu-id="353e7-990">ProdParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-990">ProdParametersEntity</span></span>              | <span data-ttu-id="353e7-991">WorkTimeLineEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-991">WorkTimeLineEntity</span></span>                |
| <span data-ttu-id="353e7-992">ProductEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-992">ProductEntity</span></span>                     | <span data-ttu-id="353e7-993">WorkTimeTableEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-993">WorkTimeTableEntity</span></span>               |
| <span data-ttu-id="353e7-994">ProductMasterEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-994">ProductMasterEntity</span></span>               | <span data-ttu-id="353e7-995">WrkCtrParametersEntity</span><span class="sxs-lookup"><span data-stu-id="353e7-995">WrkCtrParametersEntity</span></span>            |







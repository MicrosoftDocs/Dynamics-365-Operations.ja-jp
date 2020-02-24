---
title: コマース チャネルの会計統合の設定
description: このトピックでは、コマース チャネルの会計統合機能を設定するためのガイドラインを提供します。
author: josaw
manager: annbe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b221bfede5d1db8d7970e1efede85e8dba7fe017
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023223"
---
# <a name="set-up-the-fiscal-integration-for-commerce-channels"></a><span data-ttu-id="8677c-103">コマース チャネルの会計統合の設定</span><span class="sxs-lookup"><span data-stu-id="8677c-103">Set up the fiscal integration for Commerce channels</span></span>

[!include [banner](../includes/banner.md)]

## <a name="introduction"></a><span data-ttu-id="8677c-104">はじめに</span><span class="sxs-lookup"><span data-stu-id="8677c-104">Introduction</span></span>

<span data-ttu-id="8677c-105">このトピックでは、コマース チャネルの会計統合機能を設定するためのガイドラインを提供します。</span><span class="sxs-lookup"><span data-stu-id="8677c-105">This topic provides guidelines for setting up the fiscal integration functionality for Commerce channels.</span></span> <span data-ttu-id="8677c-106">会計統合の詳細については、[コマースチャネルの会計統合の概要](fiscal-integration-for-retail-channel.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-106">For more information about the fiscal integration, see [Overview of fiscal integration for Commerce channels](fiscal-integration-for-retail-channel.md).</span></span>

<span data-ttu-id="8677c-107">会計統合を設定するプロセスには、次のタスクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8677c-107">The process of setting up the fiscal integration includes the following tasks:</span></span>

1. <span data-ttu-id="8677c-108">会計プリンターなどの会計登録目的で使用される会計デバイスまたはサービスを表す、会計コネクタをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8677c-108">Configure fiscal connectors that represent fiscal devices or services that are used for fiscal registration purposes, such as fiscal printers.</span></span>
2. <span data-ttu-id="8677c-109">会計コネクタによって会計デバイスまたはサービスに登録される会計ドキュメントを生成するドキュメント プロバイダーをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8677c-109">Configure document providers that generate fiscal documents that will be registered in fiscal devices or services by fiscal connectors.</span></span>
3. <span data-ttu-id="8677c-110">一連の会計登録のステップと、各ステップごとに使用される会計コネクタおよび会計ドキュメント プロバイダーを定義する会計登録プロセスをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="8677c-110">Configure the fiscal registration process that defines a sequence of fiscal registration steps and the fiscal connectors and fiscal document providers that are used for each step.</span></span>
4. <span data-ttu-id="8677c-111">会計登録プロセスを販売時点管理 (POS) 機能プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8677c-111">Assign the fiscal registration process to point of sale (POS) functionality profiles.</span></span>
5. <span data-ttu-id="8677c-112">コネクタ技術プロファイルをハードウェア プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8677c-112">Assign connector technical profiles to hardware profiles.</span></span>

## <a name="set-up-a-fiscal-registration-process"></a><span data-ttu-id="8677c-113">会計登録プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="8677c-113">Set up a fiscal registration process</span></span>

<span data-ttu-id="8677c-114">会計統合機能を使用する前に、次の設定をコンフィギュレーションする必要があります:</span><span class="sxs-lookup"><span data-stu-id="8677c-114">Before you use the fiscal integration functionality, you should configure the following settings.</span></span>

1. <span data-ttu-id="8677c-115">コマース パラメーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="8677c-115">Update Commerce parameters.</span></span>

    1. <span data-ttu-id="8677c-116">**コマース共有パラメーター** ページの、**一般**タブで、**会計統合の有効化**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-116">On the **Commerce shared parameters** page, on the **General** tab, set the **Enable fiscal integration** option to **Yes**.</span></span> <span data-ttu-id="8677c-117">**番号順序**タブで、次の参照の番号順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="8677c-117">On the **Number sequences** tab, define the number sequences for the following references:</span></span>

        - <span data-ttu-id="8677c-118">会計技術プロファイル番号</span><span class="sxs-lookup"><span data-stu-id="8677c-118">Fiscal technical profile number</span></span>
        - <span data-ttu-id="8677c-119">会計コネクタ グループ番号</span><span class="sxs-lookup"><span data-stu-id="8677c-119">Fiscal connector group number</span></span>
        - <span data-ttu-id="8677c-120">登録プロセス番号</span><span class="sxs-lookup"><span data-stu-id="8677c-120">Registration process number</span></span>

    2. <span data-ttu-id="8677c-121">**コマース パラメーター** ページで、会計機能プロファイル番号の番号順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="8677c-121">On the **Commerce parameters** page, define the number sequence for the fiscal functional profile number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-122">番号順序はオプションです。</span><span class="sxs-lookup"><span data-stu-id="8677c-122">Number sequences are optional.</span></span> <span data-ttu-id="8677c-123">会計統合エンティティのすべての番号は、番号順序からまたは手動で生成できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-123">Numbers for all fiscal integration entities can be generated either from number sequences or manually.</span></span>

2. <span data-ttu-id="8677c-124">会計コネクタおよび会計ドキュメント プロバイダーのコンフィギュレーションをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8677c-124">Upload configurations of fiscal connectors and fiscal document providers.</span></span>

    <span data-ttu-id="8677c-125">会計ドキュメント プロバイダーは、会計デバイスまたはサービスとのやり取りにも使用される形式で POS に登録されているトランザクションおよびイベントを表す会計ドキュメントを生成を担当します。</span><span class="sxs-lookup"><span data-stu-id="8677c-125">A fiscal document provider is responsible for generating fiscal documents that represent transactions and events that are registered on the POS in a format that is also used for the interaction with a fiscal device or service.</span></span> <span data-ttu-id="8677c-126">たとえば、会計ドキュメント プロバイダーは、XML 形式表記の会計レシートを生成する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-126">For example, a fiscal document provider might generate a representation of a fiscal receipt in an XML format.</span></span>

    <span data-ttu-id="8677c-127">会計コネクタは、会計デバイスまたはサービスとの通信を担当します。</span><span class="sxs-lookup"><span data-stu-id="8677c-127">A fiscal connector is responsible for the communication with a fiscal device or service.</span></span> <span data-ttu-id="8677c-128">たとえば、会計コネクタは、会計ドキュメント プロバイダーが XML 形式で作成した会計レシートを会計プリンターに送信する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-128">For example, a fiscal connector might send a fiscal receipt that a fiscal document provider created in an XML format to a fiscal printer.</span></span> <span data-ttu-id="8677c-129">会計統合コンポーネントの詳細については、「[会計デバイスの会計登録プロセスおよび会計統合サンプル](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-129">For more details about fiscal integration components, see [Fiscal registration process and fiscal integration samples for fiscal devices](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices).</span></span>

    1. <span data-ttu-id="8677c-130">**会計コネクタ** ページ (**小売とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタ**) で、会計統合のために使用する予定のデバイスまたはサービスごとに XML コンフィギュレーションをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8677c-130">On the **Fiscal connectors** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors**), upload an XML configuration for each device or service that you plan to use for fiscal integration purposes.</span></span>

        > [!TIP]
        > <span data-ttu-id="8677c-131">**表示**を選択することによって、現在の会計コネクタに関連するすべての機能および技術プロファイルを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-131">By selecting **View**, you can view all functional and technical profiles that are related to the current fiscal connector.</span></span>

    2. <span data-ttu-id="8677c-132">**会計ドキュメント プロバイダー** ページ (**小売とコマース \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー**) で、使用する予定のデバイスまたはサービスごとに XML コンフィギュレーションをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8677c-132">On the **Fiscal document providers** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal document providers**), upload an XML configuration for each device or service that you plan to use.</span></span>

        > [!TIP]
        > <span data-ttu-id="8677c-133">**表示**を選択することによって、現在の会計ドキュメント プロバイダーに関連するすべての機能プロファイルを表示できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-133">By selecting **View**, you can view all functional profiles that are related to the current fiscal document provider.</span></span>

    <span data-ttu-id="8677c-134">会計コネクタおよび会計ドキュメント プロバイダーのコンフィギュレーションの例については、「[Retail SDK の会計統合サンプル](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-134">For examples of configurations of fiscal connectors and fiscal document providers, see [Fiscal integration samples in the Retail SDK](fiscal-integration-for-retail-channel.md#fiscal-integration-samples-in-the-retail-sdk).</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-135">データ マッピングは、会計ドキュメント プロバイダーの一部と見なされます。</span><span class="sxs-lookup"><span data-stu-id="8677c-135">Data mapping is considered part of a fiscal document provider.</span></span> <span data-ttu-id="8677c-136">同じコネクター (たとえば、州固有の規則) に異なるデータ マッピングを設定するには、異なる会計文書プロバイダーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-136">To set up different data mappings for the same connector (for example, state-specific regulations), you should create different fiscal document providers.</span></span>

3. <span data-ttu-id="8677c-137">コネクタ機能プロファイルおよびコネクタ技術プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-137">Create connector functional profiles and connector technical profiles.</span></span>

    1. <span data-ttu-id="8677c-138">**コネクタ機能プロファイル** ページ (**小売とコマース \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル**) で、この会計コネクタに関連する会計コネクタおよび会計ドキュメント プロバイダーの組み合わせごとにコネクタ機能プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-138">On the **Connector functional profiles** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Connector functional profiles**), create a connector functional profile for each combination of a fiscal connector and a fiscal document provider that is related to this fiscal connector.</span></span>

        1. <span data-ttu-id="8677c-139">コネクタ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-139">Select a connector name.</span></span>
        2. <span data-ttu-id="8677c-140">ドキュメント プロバイダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-140">Select a document provider.</span></span>

        <span data-ttu-id="8677c-141">コネクタ機能プロファイルのデータ マッピング パラメーターを変更できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-141">You can change the data mapping parameters in a connector functional profile.</span></span> <span data-ttu-id="8677c-142">会計ドキュメント プロバイダー構成で定義されている既定のパラメーターを復元するには、**更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-142">To restore the default parameters that are defined in the fiscal document provider configuration, select **Update**.</span></span>

        <span data-ttu-id="8677c-143">**例**</span><span class="sxs-lookup"><span data-stu-id="8677c-143">**Examples**</span></span>

        |   | <span data-ttu-id="8677c-144">形式</span><span class="sxs-lookup"><span data-stu-id="8677c-144">Format</span></span> | <span data-ttu-id="8677c-145">例</span><span class="sxs-lookup"><span data-stu-id="8677c-145">Example</span></span> |
        |---|--------|---------|
        | <span data-ttu-id="8677c-146">**VAT 率の設定**</span><span class="sxs-lookup"><span data-stu-id="8677c-146">**VAT rates settings**</span></span> | <span data-ttu-id="8677c-147">値 : VATrate</span><span class="sxs-lookup"><span data-stu-id="8677c-147">value : VATrate</span></span> | <span data-ttu-id="8677c-148">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="8677c-148">1 : 2000, 2 : 1800</span></span> |
        | <span data-ttu-id="8677c-149">**VAT コードのマッピング**</span><span class="sxs-lookup"><span data-stu-id="8677c-149">**VAT codes mapping**</span></span> | <span data-ttu-id="8677c-150">VATcode : 値</span><span class="sxs-lookup"><span data-stu-id="8677c-150">VATcode : value</span></span> | <span data-ttu-id="8677c-151">vat20: 1、vat18: 2</span><span class="sxs-lookup"><span data-stu-id="8677c-151">vat20 : 1, vat18 : 2</span></span> |
        | <span data-ttu-id="8677c-152">**支払/入金タイプのマッピング**</span><span class="sxs-lookup"><span data-stu-id="8677c-152">**Tender types mapping**</span></span> | <span data-ttu-id="8677c-153">TenderType: 値</span><span class="sxs-lookup"><span data-stu-id="8677c-153">TenderType : value</span></span> | <span data-ttu-id="8677c-154">現金 : 1, カード : 2</span><span class="sxs-lookup"><span data-stu-id="8677c-154">Cash : 1, Card : 2</span></span> |

        > [!NOTE]
        > <span data-ttu-id="8677c-155">コネクタ機能プロファイルは、会社に固有です。</span><span class="sxs-lookup"><span data-stu-id="8677c-155">Connector functional profiles are company-specific.</span></span> <span data-ttu-id="8677c-156">異なる会社で会計コネクタと会計ドキュメント プロバイダーの同じ組み合わせを使用する予定の場合は、会社ごとにコネクタ機能プロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-156">If you plan to use the same combination of a fiscal connector and a fiscal document provider in different companies, you should create a connector functional profile for each company.</span></span>

    2. <span data-ttu-id="8677c-157">**コネクタ技術プロファイル** ページ (**小売とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル**) で、会計コネクタごとにコネクタ技術プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-157">On the **Connector technical profiles** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**), create a connector technical profile for each fiscal connector.</span></span>

        1. <span data-ttu-id="8677c-158">コネクタ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-158">Select a connector name.</span></span>
        2. <span data-ttu-id="8677c-159">コネクタ タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-159">Select a connector type.</span></span> <span data-ttu-id="8677c-160">ハードウェア ステーションに接続されているデバイスについては、**ローカル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-160">For devices that are connected to a Hardware station, select **Local**.</span></span>

            > [!NOTE]
            > <span data-ttu-id="8677c-161">ローカル コネクタだけが現在サポートされています。</span><span class="sxs-lookup"><span data-stu-id="8677c-161">Only local connectors are currently supported.</span></span>

        <span data-ttu-id="8677c-162">コネクタ技術プロファイルの**デバイス**および**設定**タブで、パラメーターを変更できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-162">Parameters on the **Device** and **Settings** tabs in a connector technical profile can be changed.</span></span> <span data-ttu-id="8677c-163">会計コネクタ構成で定義されている既定のパラメーターを復元するには、**更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-163">To restore the default parameters that are defined in the fiscal connector configuration, select **Update**.</span></span> <span data-ttu-id="8677c-164">XML 構成の新しいバージョンが読み込まれている間は、現在の会計コネクタまたは会計ドキュメント プロバイダーが既に使用されていることを示すメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-164">While a new version of an XML configuration is loaded, you receive a message that states that the current fiscal connector or fiscal document provider is already being used.</span></span> <span data-ttu-id="8677c-165">この手順では、コネクタ機能プロファイルとコネクタ技術プロファイルで以前に行われた手動変更を上書きしません。</span><span class="sxs-lookup"><span data-stu-id="8677c-165">This procedure doesn't override manual changes that were previously made in connector functional profiles and connector technical profiles.</span></span> <span data-ttu-id="8677c-166">新しいコンフィギュレーションから既定のパラメーター セットを適用するには、**コネクタ機能プロファイル**ページまたは**コネクタ技術プロファイル**ページで、**更新**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-166">To apply the default set of parameters from a new configuration, on the **Connector functional profiles** page or the **Connector technical profiles** page, select **Update**.</span></span>

4. <span data-ttu-id="8677c-167">会計コネクタ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-167">Create fiscal connector groups.</span></span>

    <span data-ttu-id="8677c-168">会計コネクタ グループは、同じ機能を実行し、会計登録プロセスの同じ手順で使用される会計コネクタの機能プロファイルを組み合わせます</span><span class="sxs-lookup"><span data-stu-id="8677c-168">A fiscal connector group combines functional profiles of fiscal connectors that perform identical functions and are used at the same step of a fiscal registration process.</span></span> <span data-ttu-id="8677c-169">たとえば、店舗で複数の会計処理用プリンター モデルが使用できる場合、それらの会計プリンターの会計コネクタは会計コネクタ グループで組み合わされます。</span><span class="sxs-lookup"><span data-stu-id="8677c-169">For example, if several fiscal printer models can be used in a store, fiscal connectors for those fiscal printers can be combined in a fiscal connector group.</span></span>

    1. <span data-ttu-id="8677c-170">**会計コネクタ グループ** ページ (**小売とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタグループ**) で、新しい会計コネクタ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-170">On the **Fiscal connector group** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connector groups**), create a new fiscal connector group.</span></span>
    2. <span data-ttu-id="8677c-171">機能プロファイルをコネクタ グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="8677c-171">Add functional profiles to the connector group.</span></span> <span data-ttu-id="8677c-172">**機能プロファイル**タブで**追加**を選択してから、プロファイル番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-172">On the **Functional profiles** tab, select **Add**, and select a profile number.</span></span> <span data-ttu-id="8677c-173">コネクタ グループの各会計コネクタには 1 つの機能プロファイルしか含めることができません。</span><span class="sxs-lookup"><span data-stu-id="8677c-173">Each fiscal connector in a connector group can only have one functional profile.</span></span>
    3. <span data-ttu-id="8677c-174">機能プロファイルの使用を中断するには、**無効化**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-174">To suspend use of the functional profile, set the **Disable** option to **Yes**.</span></span> <span data-ttu-id="8677c-175">この変更は、現在のコネクタ グループのみに影響します。</span><span class="sxs-lookup"><span data-stu-id="8677c-175">This change affects only the current connector group.</span></span> <span data-ttu-id="8677c-176">他のコネクタ グループで同じ機能プロファイルを引き続き使用できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-176">You can continue to use the same functional profile in other connector groups.</span></span>

5. <span data-ttu-id="8677c-177">会計登録プロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-177">Create a fiscal registration process.</span></span>

    <span data-ttu-id="8677c-178">会計登録プロセスは、登録ステップおよび各ステップで使用されるコネクタ グループの順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-178">A fiscal registration process is defined by the sequence of registration steps and the connector group that is used for each step.</span></span>

    1. <span data-ttu-id="8677c-179">**会計登録プロセス** ページ (**小売とコマース \> チャネル設定 \> 会計統合 \> 会計登録プロセス**) で、会計統合の固有のプロセスごとに新しいレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="8677c-179">On the **Fiscal registration process** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal registration processes**), create a new record for each unique process of fiscal registration.</span></span>
    2. <span data-ttu-id="8677c-180">プロセスに登録ステップを追加します:</span><span class="sxs-lookup"><span data-stu-id="8677c-180">Add registration steps to the process:</span></span>

        1. <span data-ttu-id="8677c-181">**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-181">Select **Add**.</span></span>
        2. <span data-ttu-id="8677c-182">会計コネクタ タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-182">Select a fiscal connector type.</span></span>
        3. <span data-ttu-id="8677c-183">**グループ番号**フィールドで、適切な会計コネクタ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-183">In the **Group number** field, select an appropriate fiscal connector group.</span></span>

6. <span data-ttu-id="8677c-184">会計登録プロセスのエンティティを POS プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8677c-184">Assign entities of the fiscal registration process to POS profiles.</span></span>

    1. <span data-ttu-id="8677c-185">**POS 機能プロファイル** ページ (**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル**) で、会計登録プロセスを POS 機能プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8677c-185">On the **POS functionality profiles** page (**Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**), assign the fiscal registration process to a POS functionality profile.</span></span> <span data-ttu-id="8677c-186">**編集**を選択してから、**会計登録プロセス** タブの**プロセス番号**フィールドで、プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-186">Select **Edit**, and then, on the **Fiscal registration process** tab, in the **Process number** field, select a process.</span></span>
    2. <span data-ttu-id="8677c-187">**POS ハードウェア プロファイル** ページ (**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル**) で、コネクタ技術プロファイルをハードウェア プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8677c-187">On the **POS hardware profile** page (**Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**), assign connector technical profiles to a hardware profile.</span></span> <span data-ttu-id="8677c-188">**編集**を選択し、**会計周辺機器**タブに明細行を追加してから、**プロファイル番号**フィールドで、コネクタ技術プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-188">Select **Edit**, add a line on the **Fiscal peripherals** tab, and then, in the **Profile number** field, select a connector technical profile.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-189">同じハードウェア プロファイルに、複数の技術プロファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-189">You can add several technical profiles to the same hardware profile.</span></span> <span data-ttu-id="8677c-190">ただし、ハードウェア プロファイルまたは POS 機能プロファイルには、各会計コネクタ グループとの共通部分が 1 つしかありません。</span><span class="sxs-lookup"><span data-stu-id="8677c-190">However, a hardware profile or POS functionality profile should have only one intersection with any fiscal connector group.</span></span>

    <span data-ttu-id="8677c-191">会計登録フローは会計登録プロセスおよび会計統合コンポーネントのいくつかのパラメーターによって定義されます。会計ドキュメント プロバイダーの Commerce runtime 拡張機能および会計コネクタのハードウェア ステーション拡張機能。</span><span class="sxs-lookup"><span data-stu-id="8677c-191">The fiscal registration flow is defined by the fiscal registration process and also by some parameters of fiscal integration components: the Commerce runtime extension for the fiscal document provider and the Hardware station extension for the fiscal connector.</span></span>

    - <span data-ttu-id="8677c-192">イベントのサブスクリプションおよび会計登録のトランザクションは、会計ドキュメント プロバイダーで事前定義されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-192">The subscription of events and transactions to fiscal registration is predefined in the fiscal document provider.</span></span>
    - <span data-ttu-id="8677c-193">会計ドキュメント プロバイダーは、会計登録に使用される会計コネクタを識別することも担当します。</span><span class="sxs-lookup"><span data-stu-id="8677c-193">The fiscal document provider is also responsible for identifying the fiscal connector that is used for fiscal registration.</span></span> <span data-ttu-id="8677c-194">会計登録プロセスの現在のステップに対して指定されている会計コネクタ グループに含まれるコネクタ機能プロファイルと、POS が対になっているハードウェア ステーションのハードウェア プロファイルに割り当てられているコネクタ技術プロファイルが一致します。</span><span class="sxs-lookup"><span data-stu-id="8677c-194">It matches the connector functional profiles that are included in the fiscal connector group that is specified for the current step of the fiscal registration process with the connector technical profile that is assigned to the hardware profile of the Hardware station that the POS is paired to.</span></span>
    - <span data-ttu-id="8677c-195">会計ドキュメント プロバイダーは、会計ドキュメント プロバイダー構成からのデータのマッピング設定を使用し、会計ドキュメントの生成中に税金や支払などのトランザクション/イベント データを変換します。</span><span class="sxs-lookup"><span data-stu-id="8677c-195">The fiscal document provider uses the data mapping settings from the fiscal document provider configuration to transform transaction/event data such as taxes and payments while a fiscal document is generated.</span></span>
    - <span data-ttu-id="8677c-196">会計ドキュメント プロバイダーが会計ドキュメントを生成する場合、通信方法に応じて、会計コネクタはそれを会計デバイスにそのまま送信するか、またはそれを解析しデバイスのアプリケーション プログラミング インターフェイス (API) の一連のコマンドに変換できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-196">When the fiscal document provider generates a fiscal document, the fiscal connector can either send it to the fiscal device as is, or parse it and transform it into a sequence of commands of the device application programming interface (API), depending on how the communication is handled.</span></span>

7. <span data-ttu-id="8677c-197">**会計登録プロセス** ページ (**Retail とコマース \> チャネル設定 \> 会計統合 \> 会計登録プロセス**) で、**検証**を選択して会計統合プロセスを検証します。</span><span class="sxs-lookup"><span data-stu-id="8677c-197">On the **Fiscal registration process** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal registration processes**), select **Validate** to validate the fiscal registration process.</span></span>

    <span data-ttu-id="8677c-198">次の例で示すように、このタイプの検証を実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8677c-198">We recommend that you run this type of validation in the following cases:</span></span>

    - <span data-ttu-id="8677c-199">新しい登録プロセスをPOS 機能プロファイルおよびハードウェア プロファイルへ割り当てる場合を含む、新しい登録プロセスのすべての設定が完了した後。</span><span class="sxs-lookup"><span data-stu-id="8677c-199">After you've completed all the settings for a new registration process, including when you assign registration processes to POS functionality profiles and hardware profiles.</span></span>
    - <span data-ttu-id="8677c-200">既存の会計登録プロセスに変更を加え、それらの変更が原因で異なる会計コネクタが実行時に選択されるようになった後 (たとえば、会計登録プロセス手順のコネクタ グループを変更して、コネクタ グループのコネクタ機能プロファイルを有効にする、またはコネクタ グループに新しいコネクタ機能プロファイルを追加する場合)。</span><span class="sxs-lookup"><span data-stu-id="8677c-200">After you make changes to an existing fiscal registration process, and those changes might cause a different fiscal connector to be selected at runtime (for example, if you change the connector group for a fiscal registration process step, enable a connector functional profile in a connector group, or add a new connector functional profile to a connector group).</span></span>
    - <span data-ttu-id="8677c-201">コネクタ技術プロファイルのハードウェア プロファイルへの割り当てで変更を加えた後。</span><span class="sxs-lookup"><span data-stu-id="8677c-201">After you make changes in the assignment of connector technical profiles to hardware profiles.</span></span>

8. <span data-ttu-id="8677c-202">**配送スケジュール**ページで、**1070** および **1090** ジョブを実行してチャネル データベースにデータを転送します。</span><span class="sxs-lookup"><span data-stu-id="8677c-202">On the **Distribution schedule** page, run the **1070** and **1090** jobs to transfer data to the channel database.</span></span>

## <a name="set-up-fiscal-texts-for-discounts"></a><span data-ttu-id="8677c-203">割引用の会計テキストの設定</span><span class="sxs-lookup"><span data-stu-id="8677c-203">Set up fiscal texts for discounts</span></span>

<span data-ttu-id="8677c-204">場合によっては、割引が適用される場合に特別なテキストが会計レシートに印刷される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-204">In some cases, a special text must be printed on a fiscal receipt if a discount is applied.</span></span> <span data-ttu-id="8677c-205">**会計コネクタ グループ** ページ (**Retail とコマース \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ**) で、割引用の会計テキストを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-205">You can set up fiscal texts for discounts on the **Fiscal connector group** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connector groups**).</span></span>

- <span data-ttu-id="8677c-206">POS で適用される手動割引の場合は、POS 機能プロファイルで**製品割引**情報コードとして指定されている情報コードまたは情報コードグループの会計テキストを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-206">For manual discounts that are applied at the POS, you should set a fiscal text for the info code or info code group that is specified as the **Product discount** info code in the POS functionality profile.</span></span>

    1. <span data-ttu-id="8677c-207">**会計コネクタ グループ**ページで、**会計レシートのテキスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-207">On the **Fiscal connector group** page, select **Text for fiscal receipt**.</span></span>
    2. <span data-ttu-id="8677c-208">**情報コード**タブで、**追加**を選択し、情報コードまたは情報コード グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-208">On the **Info codes** tab, select **Add**, and select an info code or info code group.</span></span>
    3. <span data-ttu-id="8677c-209">**情報コード番号**で、値を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-209">In the **Info code number**, select a value.</span></span>
    4. <span data-ttu-id="8677c-210">**サブコード番号**フィールドで、選択されている情報コードにサブコードが必要な場合は、値を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-210">In the **Subcode number** field, select a value if a subcode is required for the selected info code.</span></span>
    5. <span data-ttu-id="8677c-211">**会計レシートのテキスト** フィールドで、会計レシートに印刷する必要がある会計テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-211">In the **Text for fiscal receipt** field, specify a fiscal text that should be printed on a fiscal receipt.</span></span>
    6. <span data-ttu-id="8677c-212">**ユーザー入力を会計レシートに印刷**オプションを**はい**に設定して、会計レシート上のテキストをユーザーが POS で手動で入力する情報で上書きします。</span><span class="sxs-lookup"><span data-stu-id="8677c-212">Set the **Print user input on fiscal receipt** option to **Yes** to override the text on a fiscal receipt with information that a user manually enters at the POS.</span></span> <span data-ttu-id="8677c-213">このオプションは、**テキスト**の入力タイプである情報コードにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-213">This option applies only to info codes that have an input type of **Text**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-214">情報コード グループ、リンクされた情報コード、トリガーされた情報コードが使用されるシナリオをサポートするため、いくつかの情報コードの会計テキストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-214">You can specify a fiscal text for several info codes to support scenarios where info code groups, linked info codes, and triggered info codes are used.</span></span> <span data-ttu-id="8677c-215">これらのシナリオでは、会計レシートには、割引が適用されたトランザクション明細行にリンクされているすべての情報コードからの会計テキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8677c-215">In these scenarios, the fiscal receipt will contain the fiscal texts from all info codes that are linked to the transaction line where the discount was applied.</span></span>

- <span data-ttu-id="8677c-216">チャネル固有の割引については、割引 ID の会計テキストを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-216">For channel-specific discounts, you should define a fiscal text for the discount ID.</span></span>

    1. <span data-ttu-id="8677c-217">**会計コネクタ グループ**ページで、**会計レシートのテキスト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-217">On the **Fiscal connector group** page, select **Text for fiscal receipt**.</span></span>
    2. <span data-ttu-id="8677c-218">**割引**タブで、**追加**を選択し、割引 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-218">On the **Discounts** tab, select **Add**, and select a discount ID.</span></span>
    3. <span data-ttu-id="8677c-219">**会計レシートのテキスト** フィールドで、会計レシートに印刷する必要がある会計テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-219">In the **Text for fiscal receipt** field, specify a fiscal text that should be printed on a fiscal receipt.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-220">同じトランザクション明細行にいくつかの割引が適用される場合、会計レシートにはそれらのトランザクション明細行にリンクされているすべての割引からの会計テキストが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8677c-220">If several discounts are applied to the same transaction line, the fiscal receipt will contain fiscal texts from all discounts that are linked to those transaction line.</span></span>

## <a name="set-error-handling-settings"></a><span data-ttu-id="8677c-221">エラーの処理の設定</span><span class="sxs-lookup"><span data-stu-id="8677c-221">Set error handling settings</span></span>

<span data-ttu-id="8677c-222">会計統合で使用可能なエラー処理オプションは、会計登録プロセスで設定されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-222">The error handling options that are available in the fiscal integration are set in the fiscal registration process.</span></span> <span data-ttu-id="8677c-223">会計統合のエラー処理の詳細については、「[エラー処理](fiscal-integration-for-retail-channel.md#error-handling)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-223">For more information about error handling in the fiscal integration, see [Error handling](fiscal-integration-for-retail-channel.md#error-handling).</span></span>

1. <span data-ttu-id="8677c-224">**会計登録プロセス** ページ (**Retail とコマース \> チャネル設定 \> 会計統合 \> 会計登録プロセス**) で、会計統合プロセスごとに次のパラメーターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-224">On the **Fiscal registration process** page (**Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal registration processes**), you can set the following parameters for each step of the fiscal registration process:</span></span>

    - <span data-ttu-id="8677c-225">**スキップを許可** – このパラメーターは、エラー処理ダイアログ ボックスで**スキップ** オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8677c-225">**Allow skip** – This parameter enables the **Skip** option in the error handling dialog box.</span></span>
    - <span data-ttu-id="8677c-226">**登録済としてマークを許可** – このパラメーターは、エラー処理ダイアログ ボックスで、**登録済としてマーク** オプションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="8677c-226">**Allow mark as registered** – This parameter enables the **Mark as registered** option in the error handling dialog box.</span></span>
    - <span data-ttu-id="8677c-227">**エラーでも続行** : このパラメーターが有効になっている場合、トランザクションまたはイベントの会計登録が失敗しても、会計登録プロセスは POS レジスターで続行できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-227">**Continue on error** – If this parameter is enabled, the fiscal registration process can continue on the POS register if the fiscal registration of a transaction or event fails.</span></span> <span data-ttu-id="8677c-228">それ以外の場合、次の取引またはイベントの会計登録を実行するため、オペレーターは失敗した会計登録を再試行するか、スキップ、あるいは取引またはイベントを登録済としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-228">Otherwise, to run the fiscal registration of the next transaction or event, the operator must retry the failed fiscal registration, skip it, or mark the transaction or event as registered.</span></span> <span data-ttu-id="8677c-229">詳細については、[任意の会計登録](fiscal-integration-for-retail-channel.md#optional-fiscal-registration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-229">For more information, see [Optional fiscal registration](fiscal-integration-for-retail-channel.md#optional-fiscal-registration).</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-230">**エラーでも続行**パラメーターが有効になっている場合、**スキップを許可**および**登録済としてマークを許可**パラメータは自動的に無効になります。</span><span class="sxs-lookup"><span data-stu-id="8677c-230">If the **Continue on error** parameter is enabled, the **Allow skip** and **Allow mark as registered** parameters are automatically disabled.</span></span>

2. <span data-ttu-id="8677c-231">エラー処理ダイアログ ボックスの**スキップ**および**登録済としてマーク**オプションには、**登録をスキップまたは登録済としてマークを許可**のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="8677c-231">The **Skip** and **Mark as registered** options in the error handling dialog box require the **Allow skip registration or mark as registered** permission.</span></span> <span data-ttu-id="8677c-232">したがって、**アクセス許可グループ** ページ (**Retail とコマース \> 従業員 \> アクセス許可グループ**) で、**登録のスキップまたは登録済としてマークを許可**のアクセス許可を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8677c-232">Therefore, on the **Permission groups** page (**Retail and Commerce \> Employees \> Permission groups**), enable the **Allow skip registration or mark as registered** permission.</span></span>
3. <span data-ttu-id="8677c-233">**スキップ**および**登録済としてマーク** オプションは、会計登録が失敗した場合に演算子が追加情報を入力するようにします。</span><span class="sxs-lookup"><span data-stu-id="8677c-233">The **Skip** and **Mark as registered** options let operators enter additional information when fiscal registration fails.</span></span> <span data-ttu-id="8677c-234">この機能を使用可能にするには、会計コネクタ グループの**スキップ**および**登録済としてマーク**情報コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-234">To make this functionality available, you should specify the **Skip** and **Mark as registered** info codes on a fiscal connector group.</span></span> <span data-ttu-id="8677c-235">これにより、演算子が入力した情報は、会計トランザクションにリンクされている情報コード トランザクションとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-235">The information that operators enter is then saved as an info code transaction that is linked to the fiscal transaction.</span></span> <span data-ttu-id="8677c-236">情報コードの詳細については、「[情報コードおよび情報コード グループ](../info-codes-retail.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-236">For more details about info codes, see [Info codes and info code groups](../info-codes-retail.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-237">**製品**トリガー関数は、会計コネクタ グループの**スキップ**および**登録済としてマーク**に使用される情報コード用にはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8677c-237">The **Product** trigger function isn't supported for the info codes that are used for **Skip** and **Mark as registered** in fiscal connector groups.</span></span>

    - <span data-ttu-id="8677c-238">**会計コネクタ グループ** ページの、**情報コード** タブで、**スキップ**および**登録済としてマーク** フィールドの情報コードまたは情報コード グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-238">On the **Fiscal connector group** page, on the **Info codes** tab, select info codes or info code groups in the **Skip** and **Mark as registered** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8677c-239">1 つの会計ドキュメントおよび 1 つの非会計ドキュメントは、会計登録プロセスのどの手順においても生成できます。</span><span class="sxs-lookup"><span data-stu-id="8677c-239">One fiscal document and one non-fiscal document can be generated on any step of a fiscal registration process.</span></span> <span data-ttu-id="8677c-240">会計ドキュメント プロバイダー拡張機能は、会計または非会計ドキュメントに関連するものとして、すべてのタイプのトランザクションまたはイベントを識別します。</span><span class="sxs-lookup"><span data-stu-id="8677c-240">A fiscal document provider extension identifies every type of transaction or event as related to fiscal or non-fiscal documents.</span></span> <span data-ttu-id="8677c-241">エラー処理機能は、会計ドキュメントのみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="8677c-241">The error handling feature applies only to fiscal documents.</span></span>
    >
    > - <span data-ttu-id="8677c-242">**会計ドキュメント** – 正常に登録される必要がある必須ドキュメント (たとえば、会計レシート)。</span><span class="sxs-lookup"><span data-stu-id="8677c-242">**Fiscal document** – A mandatory document that should be registered successfully (for example, a fiscal receipt).</span></span>
    > - <span data-ttu-id="8677c-243">**非会計ドキュメント** – トランザクションまたはイベントの補足ドキュメント (たとえば、ギフト カード明細)。</span><span class="sxs-lookup"><span data-stu-id="8677c-243">**Non-fiscal document** – A supplementary document for the transaction or event (for example, a gift card slip).</span></span>

4. <span data-ttu-id="8677c-244">正常性エラーが発生した後、オペレータが現在の操作（取引の作成または終了処理など）の処理を続行する必要がある場合は、**アクセス許可グループ** ページ (**Retail とコマース \>従業員\>アクセス許可グループ**) で**正常性チェック エラーのスキップを許可**のアクセス許可を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-244">If the operator must be able to continue to process the current operation (for example, creation or finalization of a transaction) after a health check error occurs, you should enable the **Allow skip health check error** permission on the **Permission groups** page (**Retail and Commerce \> Employees \> Permission groups**).</span></span> <span data-ttu-id="8677c-245">正常性チェック手順の詳細については、[会計登録正常性チェック](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8677c-245">For more information about the health check procedure, see [Fiscal registration health check](fiscal-integration-for-retail-channel.md#fiscal-registration-health-check).</span></span>

## <a name="set-up-fiscal-xz-reports-from-the-pos"></a><span data-ttu-id="8677c-246">POS からの会計 X/Z レポートの設定</span><span class="sxs-lookup"><span data-stu-id="8677c-246">Set up fiscal X/Z reports from the POS</span></span>

<span data-ttu-id="8677c-247">会計 X/Z レポートの POS での実行を有効にするには、POS レイアウトに新しいボタンを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-247">To enable fiscal X/Z reports to be run from the POS, you should add new buttons to a POS layout.</span></span>

- <span data-ttu-id="8677c-248">**ボタン グリッド** ページで、[ボタン グリッド デザイナーを使用して POS レイアウトに POS 操作を追加する](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) の手順に従って、デザイナーをインストールし、POS レイアウトを更新します。</span><span class="sxs-lookup"><span data-stu-id="8677c-248">On the **Button grids** page, follow the instructions in [Add POS operations to POS layouts by using Button grid designer](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) to install the designer and update a POS layout.</span></span>

    1. <span data-ttu-id="8677c-249">更新するレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-249">Select the layout to update.</span></span> 
    2. <span data-ttu-id="8677c-250">新しいボタンを追加し、**会計 X を印刷**ボタン プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-250">Add a new button, and set the **Print fiscal X** button property.</span></span>
    3. <span data-ttu-id="8677c-251">新しいボタンを追加し、**会計 Z を印刷**ボタン プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-251">Add a new button, and set the **Print fiscal Z** button property.</span></span>
    4. <span data-ttu-id="8677c-252">**配送スケジュール** ページで、**1090** ジョブを実行してチャネル データベースに変更を転送します。</span><span class="sxs-lookup"><span data-stu-id="8677c-252">On the **Distribution schedule** page, run the **1090** job to transfer changes to the channel database.</span></span>

## <a name="enable-manual-execution-of-postponed-fiscal-registration"></a><span data-ttu-id="8677c-253">延期された会計登録の手動実行を有効化</span><span class="sxs-lookup"><span data-stu-id="8677c-253">Enable manual execution of postponed fiscal registration</span></span>

<span data-ttu-id="8677c-254">延期された会計登録の手動実行を有効にするには、POS レイアウトに新しいボタンを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8677c-254">To enable manual execution of a postponed fiscal registration, you should add a new button to a POS layout.</span></span>

- <span data-ttu-id="8677c-255">**ボタン グリッド** ページで、[ボタン グリッド デザイナーを使用して POS レイアウトに POS 操作を追加する](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) の手順に従って、デザイナーをインストールし、POS レイアウトを更新します。</span><span class="sxs-lookup"><span data-stu-id="8677c-255">On the **Button grids** page, follow the instructions in [Add POS operations to POS layouts by using Button grid designer](../dev-itpro/add-pos-operations.md#add-a-custom-operation-button-to-the-pos-layout-in-retail-headquarters) to install the designer and update a POS layout.</span></span>

    1. <span data-ttu-id="8677c-256">更新するレイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="8677c-256">Select the layout to update.</span></span>
    2. <span data-ttu-id="8677c-257">新しいボタンを追加し、**会計登録のプロセスを完了**ボタン プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="8677c-257">Add a new button, and set the **Complete fiscal registration process** button property.</span></span>
    3. <span data-ttu-id="8677c-258">**配送スケジュール** ページで、**1090** ジョブを実行してチャネル データベースに変更を転送します。</span><span class="sxs-lookup"><span data-stu-id="8677c-258">On the **Distribution schedule** page, run the **1090** job to transfer your changes to the channel database.</span></span>

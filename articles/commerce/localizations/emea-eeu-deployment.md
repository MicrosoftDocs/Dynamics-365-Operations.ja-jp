---
title: チェコ共和国、ハンガリー、およびポーランドの事前請求書レポート印刷の配置ガイドライン
description: このトピックでは、チェコ共和国、ハンガリー、およびポーランドで POS から事前請求書の印刷を有効にするコマース コンポーネントの拡張機能を作成する方法について説明します。
author: anmukh
manager: ezubov
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Eastern Europe
ms.search.industry: Retail
ms.author: anmukh
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e04549e9812b31879f7aa5ae8e4f1c9e5a8db113
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057574"
---
# <a name="deployment-guidelines-for-advance-invoice-report-printing-for-czech-republic-hungary-and-poland"></a><span data-ttu-id="b11c7-103">チェコ共和国、ハンガリー、およびポーランドの事前請求書レポート印刷の配置ガイドライン</span><span class="sxs-lookup"><span data-stu-id="b11c7-103">Deployment guidelines for Advance Invoice report printing for Czech Republic, Hungary, and Poland</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b11c7-104">このトピックでは、チェコ共和国、ハンガリー、およびポーランドで Dynamics 365 Commerce のローカライゼーションを有効にする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-104">This topic shows how to enable the Dynamics 365 Commerce localization for Czech Republic, Hungary, and Poland.</span></span> <span data-ttu-id="b11c7-105">ローカライズは、コマース コンポーネントのいくつかの拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="b11c7-105">The localization consists of several extensions of Commerce components.</span></span> <span data-ttu-id="b11c7-106">これらの拡張機能は、販売時点管理 (POS) から**事前請求書**レポートを印刷できるようにします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-106">These extensions let you print the **Advance Invoice** report from Point of Sale (POS).</span></span> <span data-ttu-id="b11c7-107">チェコ共和国、ハンガリー、およびポーランドのローカライズの詳細については、[東ヨーロッパのコマース向け事前請求書](./emea-eeu-advance-invoices-for-retail.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b11c7-107">For more information about localization for Czech Republic, Hungary, and Poland, see [Advance invoices for Commerce for Eastern Europe](./emea-eeu-advance-invoices-for-retail.md).</span></span>

<span data-ttu-id="b11c7-108">ローカライズは、小売ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="b11c7-108">The localization is part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="b11c7-109">詳細については、[Retail ソフトウェア開発キット (SDK) アーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b11c7-109">For information, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="b11c7-110">ローカライズは、Commerce runtime (CRT) と POS に対する拡張機能で構成されます。</span><span class="sxs-lookup"><span data-stu-id="b11c7-110">The localization consists of extensions for the Commerce runtime (CRT) and POS.</span></span> <span data-ttu-id="b11c7-111">このローカライズを有効にするには、CRT コンフィギュレーション ファイルを変更しおよび変更し、POS プロジェクトを構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b11c7-111">To enable this localization, you must modify the CRT configuration file and modify and build POS projects.</span></span> <span data-ttu-id="b11c7-112">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-112">We recommend that you use an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="b11c7-113">また Microsoft Visual Studio チーム サービスといった、どのファイルも変更されていないソース管理システムを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-113">We also recommend that you use a source control system, such as Microsoft Visual Studio Team Services, where no files have been changed yet.</span></span>

## <a name="development-environment"></a><span data-ttu-id="b11c7-114">開発環境</span><span class="sxs-lookup"><span data-stu-id="b11c7-114">Development environment</span></span>

<span data-ttu-id="b11c7-115">開発環境を設定するこれらの手順を完了し、機能をテストできるようにします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-115">Complete these procedures to set up a development environment, so that you can test the functionality.</span></span>

### <a name="crt-extension-components"></a><span data-ttu-id="b11c7-116">CRT 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b11c7-116">CRT extension components</span></span>

1. <span data-ttu-id="b11c7-117">CRT 向け拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-117">Find the extensions configuration file for CRT.</span></span>

    <span data-ttu-id="b11c7-118">ファイル名は **commerceruntime.ext.config** で、IIS Commerce Scale Unit サイトの下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="b11c7-118">The file is named **commerceruntime.ext.config**, and is located in the **bin\\ext** folder under the IIS Commerce Scale Unit site location.</span></span>

2. <span data-ttu-id="b11c7-119">拡張機能コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-119">Register the CRT change in the extensions configuration file.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.UseAdvanceInvoice" />
    ```

    > [!WARNING]
    > <span data-ttu-id="b11c7-120">commerceruntime.config ファイルは編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="b11c7-120">Do **not** edit the commerceruntime.config file.</span></span> <span data-ttu-id="b11c7-121">このファイルは、カスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="b11c7-121">This file isn't intended for any customizations.</span></span>

### <a name="modern-pos-extension-components"></a><span data-ttu-id="b11c7-122">Modern POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b11c7-122">Modern POS extension components</span></span>

1. <span data-ttu-id="b11c7-123">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-123">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="b11c7-124">また、**Run** コマンドを使用して、Microsoft Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-124">Additionally, make sure that you can run Modern POS from Microsoft Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b11c7-125">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="b11c7-125">Modern POS must not be customized.</span></span> <span data-ttu-id="b11c7-126">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b11c7-126">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

2. <span data-ttu-id="b11c7-127">適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-127">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate location.</span></span>

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AdvanceInvoice"
            }
        ]
    }
    ```

3. <span data-ttu-id="b11c7-128">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-128">Rebuild the solution.</span></span>
4. <span data-ttu-id="b11c7-129">デバッガーで Modern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-129">Run Modern POS in the debugger and test the functionality.</span></span>

### <a name="cloud-pos-extension-components"></a><span data-ttu-id="b11c7-130">クラウド POS 拡張コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b11c7-130">Cloud POS extension components</span></span>

1. <span data-ttu-id="b11c7-131">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-131">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
2. <span data-ttu-id="b11c7-132">適切な場所に次の行を追加して、**InternalExtensions\extensions.json** で拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-132">Enable the extensions to be loaded in **extensions.json** by adding the following lines in the appropriate location.</span></span>

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AdvanceInvoice"
            }
        ]
    }
    ```

3. <span data-ttu-id="b11c7-133">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-133">Rebuild the solution.</span></span>
4. <span data-ttu-id="b11c7-134">デバッガーでクラウド POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="b11c7-134">Run Cloud POS in the debugger and test the functionality.</span></span>

### <a name="set-up-required-parameters-in-headquarters"></a><span data-ttu-id="b11c7-135">バックオフィスで要求されるパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="b11c7-135">Set up required parameters in Headquarters</span></span>

<span data-ttu-id="b11c7-136">詳細については、[東ヨーロッパにおけるコマース向け事前請求書](./emea-eeu-advance-invoices-for-retail.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b11c7-136">For more information, see [Advance invoices for Commerce for Eastern Europe](./emea-eeu-advance-invoices-for-retail.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="b11c7-137">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="b11c7-137">Production environment</span></span>

<span data-ttu-id="b11c7-138">以下の手順に従い、コマース コンポーネントを含む配置可能パッケージを作成して、それらのパッケージを実稼働環境で適用します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-138">Follow these steps to create deployable packages that contain Commerce components, and to apply those packages in a production environment.</span></span>

1. <span data-ttu-id="b11c7-139">**クラウド POS 拡張コンポーネント**、またはこのトピックで既に見た**Modern POS 拡張コンポーネント**セクションで手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-139">Complete the steps in the **Cloud POS extension components** or **Modern POS extension components** sections earlier in this topic.</span></span>
2. <span data-ttu-id="b11c7-140">**RetailSdk\\Assets** フォルダーの下にあるパッケージ構成ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="b11c7-140">Make the following change in the package configuration files under the **RetailSdk\\Assets** folder.</span></span>

    <span data-ttu-id="b11c7-141">**Commerceruntime.ext.config** コンフィギュレーション ファイルで、**構成**セクションに次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-141">In the **commerceruntime.ext.config** configuration files, add the following lines to the **composition** section.</span></span>

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.UseAdvanceInvoice" />
    ```

3. <span data-ttu-id="b11c7-142">Retail SDK で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-142">Run **msbuild** for the Retail SDK to create deployable packages.</span></span>
4. <span data-ttu-id="b11c7-143">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="b11c7-143">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="b11c7-144">詳細については、[配置可能なパッケージの作成](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b11c7-144">For more information, see [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>

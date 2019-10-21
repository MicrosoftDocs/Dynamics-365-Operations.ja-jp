---
title: 拡張機能にオーバーレイをリファクタリングするモデルの制限を緩和
description: このトピックでは、オーバーレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する方法について説明します。 これは、モデルが Microsoft Dynamics 365 for Finance and Operations 8.0 にシールされているために、必要です。
author: CGarty
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: CGarty
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 19401e71e69ca73a55bdd13daed04a6557066d7c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191576"
---
# <a name="relax-model-restrictions-to-refactor-overlayering-into-extensions"></a><span data-ttu-id="211db-104">オーバレイを拡張機能にリファクタリングするため、モデルの制限を緩和する</span><span class="sxs-lookup"><span data-stu-id="211db-104">Relax model restrictions to refactor overlayering into extensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="211db-105">Dynamics 365 for Finance and Operations 8.0 およびこれ以降のすべてのリリースでは、Microsoft のコードをカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="211db-105">Dynamics 365 for Finance and Operations 8.0, and all subsequent releases, will not allow Microsoft’s code to be customized by using over-layering.</span></span> <span data-ttu-id="211db-106">動作の変更や追加には、拡張機能を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="211db-106">Instead, extension capabilities should be used to modify and add behavior.</span></span> <span data-ttu-id="211db-107">「オーバーレイを使用しない」という制限は、すべてのお客様が最新の機能と修正プログラムを利用できるように、シンプルで更新しやすく、常に最新のバージョンが実行されるクラウド ERP サービスをお客様に提供するための製品の展開において、重要な要素です。</span><span class="sxs-lookup"><span data-stu-id="211db-107">The "no over-layering" restriction is a key part of the evolution of the product toward providing customers with a cloud ERP service that is simple to update and always running the most recent version possible to allow all customers to receive the benefits of the latest features and fixes.</span></span>

<span data-ttu-id="211db-108">コードを 8.0 以降にアップグレードした後、コンパイルを行うと、オーバーレイを使用するカスタマイズが残っている場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="211db-108">After you upgrade code to 8.0 or later, when you compile, any customizations that still use over-layering will cause errors.</span></span> <span data-ttu-id="211db-109">コードのリファクタリングを行うには、オーバーレイされているモデルのモデル記述子ファイルで一時的にオーバーレイの制限を緩和できます。</span><span class="sxs-lookup"><span data-stu-id="211db-109">To refactor the code, the over-layering restriction can be temporarily relaxed in the model descriptor file of the model that is being over-layered.</span></span> <span data-ttu-id="211db-110">この一時的な緩和は、開発環境およびデモ環境でのみ利用できます。スタンダード承認テスト以上のサンドボックス環境や実稼働環境などのランタイム環境には適用できません。</span><span class="sxs-lookup"><span data-stu-id="211db-110">This temporary relaxation only works on development and demo environments and cannot be deployed on runtime environments like Standard Acceptance Test (or higher) sandbox or production environments.</span></span> <span data-ttu-id="211db-111">記述子の制限を緩和することで、段階的にコードを拡張機能へとリファクタリングし、コンパイル、実行、テストを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="211db-111">Relaxing the descriptor restriction will enable the code to be gradually refactored to extensions, compiled, run, and then tested.</span></span> 

## <a name="detailed-process"></a><span data-ttu-id="211db-112">詳細なプロセス</span><span class="sxs-lookup"><span data-stu-id="211db-112">Detailed process</span></span>
<span data-ttu-id="211db-113">モデルの制限を緩和するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="211db-113">Complete the following steps to relax model restrictions.</span></span> <span data-ttu-id="211db-114">この手順は、クラウド環境で実行することも、ローカルの仮想マシン (VM) で実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="211db-114">This procedure can be completed on a cloud environment or a local virtual machine (VM).</span></span>

1. <span data-ttu-id="211db-115">Dynamics 365 for Finance and Operations 8.0 開発環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="211db-115">Deploy a Dynamics 365 for Finance and Operations 8.0 development environment.</span></span> 
2. <span data-ttu-id="211db-116">Lifecycle Services (LCS) のコード アップグレード サービスを実行して、ソリューションをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="211db-116">Run the Lifecycle Services (LCS) code upgrade service to upgrade the solution.</span></span>
3. <span data-ttu-id="211db-117">コンパイルできるように、必要に応じて Microsoft のモデルでのオーバーレイを一時的に許可します。</span><span class="sxs-lookup"><span data-stu-id="211db-117">Temporarily allow over-layering in Microsoft models as needed to enable compilation.</span></span>
    
    <span data-ttu-id="211db-118">a.</span><span class="sxs-lookup"><span data-stu-id="211db-118">a.</span></span> <span data-ttu-id="211db-119">C:\AOSService\PackagesLocalDirectory フォルダーで目的のモデルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="211db-119">Locate the desired model within the C:\AOSService\PackagesLocalDirectory folder.</span></span>
    
    <span data-ttu-id="211db-120">b.</span><span class="sxs-lookup"><span data-stu-id="211db-120">b.</span></span> <span data-ttu-id="211db-121">記述子のフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="211db-121">Navigate to the descriptor folder.</span></span> <span data-ttu-id="211db-122">たとえば、\Currency\Descriptor フォルダーなどです。</span><span class="sxs-lookup"><span data-stu-id="211db-122">For example, \Currency\Descriptor.</span></span>
    
    <span data-ttu-id="211db-123">c.</span><span class="sxs-lookup"><span data-stu-id="211db-123">c.</span></span> <span data-ttu-id="211db-124">XML ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="211db-124">Open the XML file.</span></span> <span data-ttu-id="211db-125">たとえば、Currency.xml ファイルなどです。</span><span class="sxs-lookup"><span data-stu-id="211db-125">For example, Currency.xml.</span></span>
    
    <span data-ttu-id="211db-126">d.</span><span class="sxs-lookup"><span data-stu-id="211db-126">d.</span></span> <span data-ttu-id="211db-127">**Customization** メタデータ要素を **AxModelInfo** メタデータ要素の内側に追加して、**AllowAndWarn** を指定します。ファイルの冒頭はこのようになります。</span><span class="sxs-lookup"><span data-stu-id="211db-127">Add a **Customization** metadata element inside the **AxModelInfo** metadata element to indicate **AllowAndWarn** so that the start of the file now looks like this.</span></span>
            
    ```xml
    <AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <AppliedUpdates xmlns:d2p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" />
    <Customization>AllowAndWarn</Customization>
    ```
    
4. <span data-ttu-id="211db-128">オーバーレイをリファクタリングして拡張機能にし、テストします。</span><span class="sxs-lookup"><span data-stu-id="211db-128">Refactor over-layering to extensions and test.</span></span> <span data-ttu-id="211db-129">​オーバーレイを削除できるように、拡張機能を利用します。</span><span class="sxs-lookup"><span data-stu-id="211db-129">Make use of extension capabilities to eliminate over-layering.</span></span> <span data-ttu-id="211db-130">必要な場合には、拡張機能の要求を行います。</span><span class="sxs-lookup"><span data-stu-id="211db-130">If needed, make extensibility requests.</span></span>
5. <span data-ttu-id="211db-131">Microsoft のモデルに対する一時的な変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="211db-131">Revert the temporary changes to Microsoft models.</span></span> <span data-ttu-id="211db-132">オーバーレイを使用するモデルの展開はできなくなるため、記述子ファイルを更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="211db-132">The deployment of a model that uses over-layering will not be possible, so it's important to ensure that the descriptor file is updated.</span></span>
 
## <a name="prototyping-extensibility-requests"></a><span data-ttu-id="211db-133">拡張機能の要求のプロトタイピング</span><span class="sxs-lookup"><span data-stu-id="211db-133">Prototyping extensibility requests</span></span>
<span data-ttu-id="211db-134">拡張機能を使用するようにソリューションを徐々に移行していく中で、ソリューションにおける課題を解消するために拡張機能の要求が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="211db-134">As a solution gradually migrates toward extensions, there will be places where an extensibility request is required to unblock the solution.</span></span> <span data-ttu-id="211db-135">ソリューションの課題を解消し、拡張機能を使用するための移行プロセスをスムーズに進めるために何が必要なのかを十分に把握するために、拡張機能のプロトタイプを別のモデルとして作成することができます。</span><span class="sxs-lookup"><span data-stu-id="211db-135">To fully understand what is needed to unblock a solution and smooth the migration process toward extensions, extension capabilities can be prototyped in a separate model.</span></span>

1. <span data-ttu-id="211db-136">オーバーレイをリファクタリングするために必要な拡張機能を特定します。</span><span class="sxs-lookup"><span data-stu-id="211db-136">Identify the need for an extension capability to refactor some over-layering.</span></span>
2. <span data-ttu-id="211db-137">拡張機能のプロトタイプを拡張機能プロトタイプ モデルに追加します。</span><span class="sxs-lookup"><span data-stu-id="211db-137">Add a prototype of extension capabilities into an extension prototype model.</span></span>

   - <span data-ttu-id="211db-138">列挙型の拡張については、対象の列挙型のコピーを拡張機能プロトタイプ モデルに追加して、拡張可能の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="211db-138">For enumeration extensibility, put a copy of the enumeration into the extension prototype model and mark it as extensible.</span></span>
    
   - <span data-ttu-id="211db-139">抽出メソッドの拡張については、抽出されたメソッドとオーバーレイされたオリジナルのプロトタイプを拡張機能プロトタイプ モデルに作成します。</span><span class="sxs-lookup"><span data-stu-id="211db-139">For extract method extensibility, prototype the extracted method and the overlayered original in the extension prototype model.</span></span>
    
3. <span data-ttu-id="211db-140">プロトタイプの拡張機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="211db-140">Use the prototype extension capability.</span></span>
4. <span data-ttu-id="211db-141">プロトタイプの拡張機能で問題がなければ、対応する要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="211db-141">If the prototype extension capability is sufficient, create a matching request.</span></span>
5. <span data-ttu-id="211db-142">その拡張機能をプラットフォームやアプリケーションに実装する際には、プロトタイプの拡張機能および関連するオーバーレイはすべて、拡張機能プロトタイプ モデルから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="211db-142">When the extension capability has been implemented in the platform or application, the prototype extension capability and any associated over-layering should be removed from the extension prototype model.</span></span>
6. <span data-ttu-id="211db-143">ソリューションのすべてのオーバーレイが拡張機能にリファクタリングされ、拡張機能プロトタイプ モデルが空になったら、ソリューションのリファクタリングは完了です。</span><span class="sxs-lookup"><span data-stu-id="211db-143">After the solution has all over-layering refactored to extensions and the extension prototype model is empty, the solution refactoring is complete.</span></span>

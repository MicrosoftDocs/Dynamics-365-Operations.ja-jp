---
title: 拡張機能にオーバーレイをリファクタリングするモデルの制限を緩和
description: このトピックでは、オーバーレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する方法について説明します。
author: CGarty
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: CGarty
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 5180cf3f0ed02d8f4966319fe5ee5030196f219d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749904"
---
# <a name="relax-model-restrictions-to-refactor-overlayering-into-extensions"></a><span data-ttu-id="4fcdc-103">オーバーレイを拡張機能にリファクタリングするため、モデルの制限を緩和する</span><span class="sxs-lookup"><span data-stu-id="4fcdc-103">Relax model restrictions to refactor overlayering into extensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fcdc-104">バージョン 8.0 以降の Finance and Operations アプリの開発ツールでは、オーバーレイヤリングを利用して Microsoft コードをカスタマイズすることができません。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-104">Development tools for Finance and Operations apps, starting with version 8.0, do not allow Microsoft code to be customized by using over-layering.</span></span> <span data-ttu-id="4fcdc-105">動作の変更や追加には、拡張機能を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-105">Instead, extension capabilities should be used to modify and add behavior.</span></span> <span data-ttu-id="4fcdc-106">「オーバーレイを使用しない」という制限は、すべてのお客様が最新の機能と修正プログラムを利用できるように、アップデートが簡単で常に最新のバージョンで稼働するクラウドサービスをお客様に提供することに向けて、製品を進化させていく上で重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-106">The "no over-layering" restriction is a key part of the evolution of the product toward providing customers with a cloud service that is simple to update and always running the most recent version possible to allow all customers to receive the benefits of the latest features and fixes.</span></span>

<span data-ttu-id="4fcdc-107">Dynamics AX 2012や Dynamics 365 for Finance and Operations バージョン7からコードをアップグレードした後で、オーバーレイを使用するカスタマイズを行った場合、コンパイル時にエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-107">After you upgrade code from Dynamics AX 2012 or from Dynamics 365 for Finance and Operations version 7, any customizations that still use over-layering will cause errors when you compile your code.</span></span> <span data-ttu-id="4fcdc-108">コードのリファクタリングを行うには、オーバーレイされているモデルのモデル記述子ファイルで一時的にオーバーレイの制限を緩和できます。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-108">To refactor the code, the over-layering restriction can be temporarily relaxed in the model descriptor file of the model that is being over-layered.</span></span> <span data-ttu-id="4fcdc-109">この一時的な緩和は、開発環境およびデモ環境でのみ利用できます。スタンダード承認テスト以上のサンドボックス環境や実稼働環境などのランタイム環境には適用できません。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-109">This temporary relaxation only works on development and demo environments and cannot be deployed on runtime environments like Standard Acceptance Test (or higher) sandbox or production environments.</span></span> <span data-ttu-id="4fcdc-110">記述子の制限を緩和することで、段階的にコードを拡張機能へとリファクタリングし、コンパイル、実行、テストを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-110">Relaxing the descriptor restriction will enable the code to be gradually refactored to extensions, compiled, run, and then tested.</span></span> 

## <a name="detailed-process"></a><span data-ttu-id="4fcdc-111">詳細なプロセス</span><span class="sxs-lookup"><span data-stu-id="4fcdc-111">Detailed process</span></span>
<span data-ttu-id="4fcdc-112">モデルの制限を緩和するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-112">Complete the following steps to relax model restrictions.</span></span> <span data-ttu-id="4fcdc-113">この手順は、クラウド環境で実行することも、ローカルの仮想マシン (VM) で実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-113">This procedure can be completed on a cloud environment or a local virtual machine (VM).</span></span>

1. <span data-ttu-id="4fcdc-114">Finance and Operations アプリの開発環境を展開します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-114">Deploy the development environment for the Finance and Operations app.</span></span> 
2. <span data-ttu-id="4fcdc-115">Lifecycle Services (LCS) のコード アップグレード サービスを実行して、ソリューションをアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-115">Run the Lifecycle Services (LCS) code upgrade service to upgrade the solution.</span></span>
3. <span data-ttu-id="4fcdc-116">コンパイルできるように、必要に応じて Microsoft のモデルでのオーバーレイを一時的に許可します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-116">Temporarily allow over-layering in Microsoft models as needed to enable compilation.</span></span>
    
    <span data-ttu-id="4fcdc-117">a.</span><span class="sxs-lookup"><span data-stu-id="4fcdc-117">a.</span></span> <span data-ttu-id="4fcdc-118">C:\AOSService\PackagesLocalDirectory フォルダーで目的のモデルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-118">Locate the desired model within the C:\AOSService\PackagesLocalDirectory folder.</span></span>
    
    <span data-ttu-id="4fcdc-119">b.</span><span class="sxs-lookup"><span data-stu-id="4fcdc-119">b.</span></span> <span data-ttu-id="4fcdc-120">記述子のフォルダーに移動します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-120">Navigate to the descriptor folder.</span></span> <span data-ttu-id="4fcdc-121">たとえば、\Currency\Descriptor フォルダーなどです。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-121">For example, \Currency\Descriptor.</span></span>
    
    <span data-ttu-id="4fcdc-122">c.</span><span class="sxs-lookup"><span data-stu-id="4fcdc-122">c.</span></span> <span data-ttu-id="4fcdc-123">XML ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-123">Open the XML file.</span></span> <span data-ttu-id="4fcdc-124">たとえば、Currency.xml ファイルなどです。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-124">For example, Currency.xml.</span></span>
    
    <span data-ttu-id="4fcdc-125">d.</span><span class="sxs-lookup"><span data-stu-id="4fcdc-125">d.</span></span> <span data-ttu-id="4fcdc-126">**Customization** メタデータ要素を **AxModelInfo** メタデータ要素の内側に追加して、**AllowAndWarn** を指定します。ファイルの冒頭はこのようになります。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-126">Add a **Customization** metadata element inside the **AxModelInfo** metadata element to indicate **AllowAndWarn** so that the start of the file now looks like this.</span></span>
            
    ```xml
    <AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <AppliedUpdates xmlns:d2p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" />
    <Customization>AllowAndWarn</Customization>
    ```
    
4. <span data-ttu-id="4fcdc-127">オーバーレイをリファクタリングして拡張機能にし、テストします。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-127">Refactor over-layering to extensions and test.</span></span> <span data-ttu-id="4fcdc-128">​オーバーレイを削除できるように、拡張機能を利用します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-128">Make use of extension capabilities to eliminate over-layering.</span></span> <span data-ttu-id="4fcdc-129">必要な場合には、拡張機能の要求を行います。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-129">If needed, make extensibility requests.</span></span>
5. <span data-ttu-id="4fcdc-130">Microsoft のモデルに対する一時的な変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-130">Revert the temporary changes to Microsoft models.</span></span> <span data-ttu-id="4fcdc-131">オーバーレイを使用するモデルの展開はできなくなるため、記述子ファイルを更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-131">The deployment of a model that uses over-layering will not be possible, so it's important to ensure that the descriptor file is updated.</span></span>
 
## <a name="prototyping-extensibility-requests"></a><span data-ttu-id="4fcdc-132">拡張機能の要求のプロトタイピング</span><span class="sxs-lookup"><span data-stu-id="4fcdc-132">Prototyping extensibility requests</span></span>
<span data-ttu-id="4fcdc-133">拡張機能を使用するようにソリューションを徐々に移行していく中で、ソリューションにおける課題を解消するために拡張機能の要求が必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-133">As a solution gradually migrates toward extensions, there will be places where an extensibility request is required to unblock the solution.</span></span> <span data-ttu-id="4fcdc-134">ソリューションの課題を解消し、拡張機能を使用するための移行プロセスをスムーズに進めるために何が必要なのかを十分に把握するために、拡張機能のプロトタイプを別のモデルとして作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-134">To fully understand what is needed to unblock a solution and smooth the migration process toward extensions, extension capabilities can be prototyped in a separate model.</span></span>

1. <span data-ttu-id="4fcdc-135">オーバーレイをリファクタリングするために必要な拡張機能を特定します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-135">Identify the need for an extension capability to refactor some over-layering.</span></span>
2. <span data-ttu-id="4fcdc-136">拡張機能のプロトタイプを拡張機能プロトタイプ モデルに追加します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-136">Add a prototype of extension capabilities into an extension prototype model.</span></span>

   - <span data-ttu-id="4fcdc-137">列挙型の拡張については、対象の列挙型のコピーを拡張機能プロトタイプ モデルに追加して、拡張可能の設定を行います。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-137">For enumeration extensibility, put a copy of the enumeration into the extension prototype model and mark it as extensible.</span></span>
    
   - <span data-ttu-id="4fcdc-138">抽出メソッドの拡張については、抽出されたメソッドとオーバーレイされたオリジナルのプロトタイプを拡張機能プロトタイプ モデルに作成します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-138">For extract method extensibility, prototype the extracted method and the overlayered original in the extension prototype model.</span></span>
    
3. <span data-ttu-id="4fcdc-139">プロトタイプの拡張機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-139">Use the prototype extension capability.</span></span>
4. <span data-ttu-id="4fcdc-140">プロトタイプの拡張機能で問題がなければ、対応する要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-140">If the prototype extension capability is sufficient, create a matching request.</span></span>
5. <span data-ttu-id="4fcdc-141">その拡張機能をプラットフォームやアプリケーションに実装する際には、プロトタイプの拡張機能および関連するオーバーレイはすべて、拡張機能プロトタイプ モデルから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-141">When the extension capability has been implemented in the platform or application, the prototype extension capability and any associated over-layering should be removed from the extension prototype model.</span></span>
6. <span data-ttu-id="4fcdc-142">ソリューションのすべてのオーバーレイが拡張機能にリファクタリングされ、拡張機能プロトタイプ モデルが空になったら、ソリューションのリファクタリングは完了です。</span><span class="sxs-lookup"><span data-stu-id="4fcdc-142">After the solution has all over-layering refactored to extensions and the extension prototype model is empty, the solution refactoring is complete.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
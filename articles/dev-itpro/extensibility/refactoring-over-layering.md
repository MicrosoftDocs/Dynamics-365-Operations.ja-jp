---
title: "モデル制限を緩和し、拡張機能へのオーバーレイのリファクタリングを有効化する"
description: "このトピックでは、モデル制限の緩和と、拡張機能へのオーバーレイのリファクタリングの有効化に関する情報を提供します。 これは、モデルが Microsoft Dynamics 365 for Finance and Operations 8.0 でシールされているために必要です。"
author: CGarty
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: CGarty
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c3e31a6420c503093c55dfb6589b58a8aaf2326b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="relax-model-restrictions-to-enable-the-refactoring-of-over-layering-into-extensions"></a><span data-ttu-id="f0d13-104">モデル制限を緩和し、拡張機能へのオーバーレイのリファクタリングを有効化する</span><span class="sxs-lookup"><span data-stu-id="f0d13-104">Relax model restrictions to enable the refactoring of over-layering into extensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0d13-105">Dynamics 365 for Finance and Operations 8.0 およびこれ以降のすべてのリリースでは、オーバーレイを使用して Microsoft のコードをカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f0d13-105">Dynamics 365 for Finance and Operations 8.0, and all subsequent releases, will not allow Microsoft’s code to be customized by using over-layering.</span></span> <span data-ttu-id="f0d13-106">代わりに、変更および動作を追加するため拡張機能が使用される必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0d13-106">Instead, extension capabilities should be used to modify and add behavior.</span></span> <span data-ttu-id="f0d13-107">「超過レイヤーなし」制限は、クラウド ERP サービスが顧客に提供するのに対する製品の発展の重要な部分です。それはすべての顧客が最新機能および最新修正の益を得られるよう、簡単に更新でき常に利用可能な最新バージョンを実行しています。</span><span class="sxs-lookup"><span data-stu-id="f0d13-107">The "no over-layering" restriction is a key part of the evolution of the product toward providing customers with a cloud ERP service that is simple to update and always running the most recent version possible to allow all customers to receive the benefits of the latest features and fixes.</span></span>

<span data-ttu-id="f0d13-108">コードを 8.0 以降にアップグレードすると、コンパイルの際にオーバーレイをまだ使用するカスタマイズにエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-108">After you upgrade code to 8.0 or later, when you compile, any customizations that still use over-layering will cause errors.</span></span> <span data-ttu-id="f0d13-109">コードをリファクターするには、オーバーレイされているモデルのモデル記述子ファイルで、オーバーレイ制限を一時的に緩和することができます。</span><span class="sxs-lookup"><span data-stu-id="f0d13-109">To refactor the code, the over-layering restriction can be temporarily relaxed in the model descriptor file of the model that is being over-layered.</span></span> <span data-ttu-id="f0d13-110">この一時的な緩和は、開発環境およびデモ環境でのみ機能し、スタンダード承認テスト (またはそれ以上) のサンドボックス環境や実稼動環境などのランタイム環境には配置できません。</span><span class="sxs-lookup"><span data-stu-id="f0d13-110">This temporary relaxation only works on development and demo environments and cannot be deployed on runtime environments like Standard Acceptance Test (or higher) sandbox or production environments.</span></span> <span data-ttu-id="f0d13-111">記述子制限を緩和すると、拡張機能に徐々にリファクタリングされ、コンパイルされ、実行され、およびテストされるコードが有効になります。</span><span class="sxs-lookup"><span data-stu-id="f0d13-111">Relaxing the descriptor restriction will enable the code to be gradually refactored to extensions, compiled, run, and then tested.</span></span> 

## <a name="detailed-process"></a><span data-ttu-id="f0d13-112">詳細なプロセス</span><span class="sxs-lookup"><span data-stu-id="f0d13-112">Detailed process</span></span>
<span data-ttu-id="f0d13-113">モデル制限を緩和するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-113">Complete the following steps to relax model restrictions.</span></span> <span data-ttu-id="f0d13-114">クラウド環境またはローカル仮想マシン (VM) では、この手順を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f0d13-114">This procedure can be completed on a cloud environment or a local virtual machine (VM).</span></span>

1. <span data-ttu-id="f0d13-115">Finance and Operations 8.0 開発環境向けに Dynamics 365 を導入します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-115">Deploy a Dynamics 365 for Finance and Operations 8.0 development environment.</span></span> 
2. <span data-ttu-id="f0d13-116">ソリューションをアップグレードするには、Lifecycle Services (LCS) コード アップグレード サービスを実行します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-116">Run the Lifecycle Services (LCS) code upgrade service to upgrade the solution.</span></span>
3. <span data-ttu-id="f0d13-117">コンパイルを有効にするための必要に応じて Microsoft モデルでオーバーレイを一時的に許可します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-117">Temporarily allow over-layering in Microsoft models as needed to enable compilation.</span></span>
    
    <span data-ttu-id="f0d13-118">a.</span><span class="sxs-lookup"><span data-stu-id="f0d13-118">a.</span></span> <span data-ttu-id="f0d13-119">C:\AOSService\PackagesLocalDirectory フォルダー内で目的のモデルを検索します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-119">Locate the desired model within the C:\AOSService\PackagesLocalDirectory folder.</span></span>
    
    <span data-ttu-id="f0d13-120">b.</span><span class="sxs-lookup"><span data-stu-id="f0d13-120">b.</span></span> <span data-ttu-id="f0d13-121">記述子フォルダに移動します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-121">Navigate to the descriptor folder.</span></span> <span data-ttu-id="f0d13-122">たとえば、\Currency\Descriptor です。</span><span class="sxs-lookup"><span data-stu-id="f0d13-122">For example, \Currency\Descriptor.</span></span>
    
    <span data-ttu-id="f0d13-123">c.</span><span class="sxs-lookup"><span data-stu-id="f0d13-123">c.</span></span> <span data-ttu-id="f0d13-124">XML ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f0d13-124">Open the XML file.</span></span> <span data-ttu-id="f0d13-125">たとえば、Currency.xml です。</span><span class="sxs-lookup"><span data-stu-id="f0d13-125">For example, Currency.xml.</span></span>
    
    <span data-ttu-id="f0d13-126">d.</span><span class="sxs-lookup"><span data-stu-id="f0d13-126">d.</span></span> <span data-ttu-id="f0d13-127">**AllowAndWarn** を示す **AxModelInfo** メタデータ要素内に**カスタマイズ**メタデータ要素を追加すると、ファイルの先頭は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="f0d13-127">Add a **Customization** metadata element inside the **AxModelInfo** metadata element to indicate **AllowAndWarn** so that the start of the file now looks like this.</span></span>
            
    ```xml
    <AxModelInfo xmlns:i="http://www.w3.org/2001/XMLSchema-instance">
    <AppliedUpdates xmlns:d2p1="http://schemas.microsoft.com/2003/10/Serialization/Arrays" />
    <Customization>AllowAndWarn</Customization>
    ```
    
4. <span data-ttu-id="f0d13-128">拡張機能へのオーバーレイのリファクタリングおよびテスト。</span><span class="sxs-lookup"><span data-stu-id="f0d13-128">Refactor over-layering to extensions and test.</span></span> <span data-ttu-id="f0d13-129">オーバーレイを解消するための拡張機能を利用します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-129">Make use of extension capabilities to eliminate over-layering.</span></span> <span data-ttu-id="f0d13-130">必要な場合は、拡張機能の要求を行います。</span><span class="sxs-lookup"><span data-stu-id="f0d13-130">If needed, make extensibility requests.</span></span>
5. <span data-ttu-id="f0d13-131">Microsoft モデルへの一時的な変更を元に戻します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-131">Revert the temporary changes to Microsoft models.</span></span> <span data-ttu-id="f0d13-132">オーバーレイを使用するモデルの展開はできなくなるため、記述子ファイルを更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="f0d13-132">The deployment of a model that uses over-layering will not be possible, so it's important to ensure that the descriptor file is updated.</span></span>
 
## <a name="prototyping-extensibility-requests"></a><span data-ttu-id="f0d13-133">プロトタイプ拡張機能の要求</span><span class="sxs-lookup"><span data-stu-id="f0d13-133">Prototyping extensibility requests</span></span>
<span data-ttu-id="f0d13-134">拡張子に向けてソリューションが段階的に移行する際、ソリューションを解除するための拡張性要求が必要とされる場所があります。</span><span class="sxs-lookup"><span data-stu-id="f0d13-134">As a solution gradually migrates toward extensions, there will be places where an extensibility request is required to unblock the solution.</span></span> <span data-ttu-id="f0d13-135">ソリューションのブロックを解除し、拡張機能への移行プロセスをスムーズにするために必要なものを完全に理解するために、拡張機能を別のモデルでプロトタイプ化することができます。</span><span class="sxs-lookup"><span data-stu-id="f0d13-135">To fully understand what is needed to unblock a solution and smooth the migration process toward extensions, extension capabilities can be prototyped in a separate model.</span></span>

1. <span data-ttu-id="f0d13-136">いくつかのオーバーレイをリファクターする拡張機能の必要性を識別します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-136">Identify the need for an extension capability to refactor some over-layering.</span></span>
2. <span data-ttu-id="f0d13-137">拡張機能のプロトタイプを拡張プロトタイプ モデルに追加します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-137">Add a prototype of extension capabilities into an extension prototype model.</span></span>

   - <span data-ttu-id="f0d13-138">列挙の拡張機能のために、列挙のコピーを拡張プロトタイプ モデルに入れ、それを拡張可能としてマークします。</span><span class="sxs-lookup"><span data-stu-id="f0d13-138">For enumeration extensibility, put a copy of the enumeration into the extension prototype model and mark it as extensible.</span></span>
    
   - <span data-ttu-id="f0d13-139">メソッド抽出の拡張機能のために、拡張プロトタイプ モデルで、抽出されたメソッドとオーバーレイされたオリジナルを作成します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-139">For extract method extensibility, prototype the extracted method and the overlayered original in the extension prototype model.</span></span>
    
3. <span data-ttu-id="f0d13-140">プロトタイプの拡張機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-140">Use the prototype extension capability.</span></span>
4. <span data-ttu-id="f0d13-141">プロトタイプの拡張機能が不十分な場合は、対応する要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-141">If the prototype extension capability is sufficient, create a matching request.</span></span>
5. <span data-ttu-id="f0d13-142">拡張機能がプラットフォームまたはアプリケーションに実装されている場合、プロトタイプ拡張機能およびそれに関連するオーバーレイを拡張プロトタイプ モデルから削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f0d13-142">When the extension capability has been implemented in the platform or application, the prototype extension capability and any associated over-layering should be removed from the extension prototype model.</span></span>
6. <span data-ttu-id="f0d13-143">拡張機能にリファクタリングされたすべてのオーバーレイがソリューションにあり、拡張プロトタイプ モデルが空白になると、ソリューション リファクタリングは完了します。</span><span class="sxs-lookup"><span data-stu-id="f0d13-143">After the solution has all over-layering refactored to extensions and the extension prototype model is empty, the solution refactoring is complete.</span></span>


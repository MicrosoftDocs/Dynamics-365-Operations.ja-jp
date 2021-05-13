---
title: X++ の Visual Studio 2017 の要件
description: このトピックでは X++ の Visual Studio拡張機能を実行するために必要な Visual Studio 2017 コンポーネントの一覧を示します。
author: jorisdg
ms.date: 04/01/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.author: jorisde
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8dbafdac2dbab7057f921d128c84eedd02680049
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880702"
---
# <a name="visual-studio-2017-requirements-for-x"></a><span data-ttu-id="ce17f-103">X++ の Visual Studio 2017 の要件</span><span class="sxs-lookup"><span data-stu-id="ce17f-103">Visual Studio 2017 requirements for X++</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce17f-104">このトピックでは X++ の **Visual Studio** 拡張機能を実行するために必要な Visual Studio 2017 コンポーネントの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="ce17f-104">This topic lists the Visual Studio 2017 components that are required to run the **Visual Studio** extension for X++.</span></span>

> [!NOTE]
> <span data-ttu-id="ce17f-105">Lifecycle Services (LCS) から配置されたダウンロード可能な仮想ハード ドライブ (VHD) または仮想マシンに Visual Studio を手動でインストールすることはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="ce17f-105">We do not recommend installing Visual Studio manually on the downloadable virtual hard drive (VHD) or virtual machines deployed from Lifecycle Services (LCS).</span></span> <span data-ttu-id="ce17f-106">代わりに、新しい仮想マシンをダウンロードまたは配置することを強く推奨します。</span><span class="sxs-lookup"><span data-stu-id="ce17f-106">Instead, we strongly recommend that you download or deploy a new virtual machine.</span></span> <span data-ttu-id="ce17f-107">バージョン10.0.13 以降に配置された仮想マシンにはすべて Visual Studio 2017 とその前提条件がインストールされ、マシンの互換性とセキュリティを維持するために Visual Studio の外部に他の更新が付属しています。</span><span class="sxs-lookup"><span data-stu-id="ce17f-107">Virtual machines deployed with versions 10.0.13 or later all have Visual Studio 2017 and its prerequisites installed, and come with other updates outside of Visual Studio to help keep the machines compatible and secure.</span></span>

## <a name="visual-studio-editions"></a><span data-ttu-id="ce17f-108">Visual Studio エディション</span><span class="sxs-lookup"><span data-stu-id="ce17f-108">Visual Studio editions</span></span>

<span data-ttu-id="ce17f-109">Visual Studio のサポートされているエディションは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="ce17f-109">The supported editions of Visual Studio include:</span></span>

- <span data-ttu-id="ce17f-110">Visual Studio 2017 Professional</span><span class="sxs-lookup"><span data-stu-id="ce17f-110">Visual Studio 2017 Professional</span></span>
- <span data-ttu-id="ce17f-111">Visual Studio 2017 Enterprise</span><span class="sxs-lookup"><span data-stu-id="ce17f-111">Visual Studio 2017 Enterprise</span></span>

> [!NOTE]
> <span data-ttu-id="ce17f-112">Visual Studio のエディションが異なれば、ライセンス要件とコストも異なります。</span><span class="sxs-lookup"><span data-stu-id="ce17f-112">Different Visual Studio editions have different licensing requirements and costs.</span></span> <span data-ttu-id="ce17f-113">詳細については、[Visual Studio](https://visualstudio.microsoft.com) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce17f-113">For more information, see [Visual Studio](https://visualstudio.microsoft.com).</span></span>

## <a name="required-visual-studio-components"></a><span data-ttu-id="ce17f-114">必要とされる Visual Studio コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce17f-114">Required Visual Studio components</span></span>

<span data-ttu-id="ce17f-115">次の表に、必要な Visual Studio コンポーネントを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="ce17f-115">The following table lists the required Visual Studio components.</span></span>

| <span data-ttu-id="ce17f-116">種類</span><span class="sxs-lookup"><span data-stu-id="ce17f-116">Type</span></span> | <span data-ttu-id="ce17f-117">氏名</span><span class="sxs-lookup"><span data-stu-id="ce17f-117">Name</span></span> | <span data-ttu-id="ce17f-118">必須</span><span class="sxs-lookup"><span data-stu-id="ce17f-118">Required</span></span> | <span data-ttu-id="ce17f-119">摘要</span><span class="sxs-lookup"><span data-stu-id="ce17f-119">Notes</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="ce17f-120">ワークロード</span><span class="sxs-lookup"><span data-stu-id="ce17f-120">Workload</span></span> | <span data-ttu-id="ce17f-121">.NET デスクトップ開発</span><span class="sxs-lookup"><span data-stu-id="ce17f-121">.NET desktop development</span></span> | <span data-ttu-id="ce17f-122">あり</span><span class="sxs-lookup"><span data-stu-id="ce17f-122">Yes</span></span> | |
| <span data-ttu-id="ce17f-123">個々のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce17f-123">Individual component</span></span> | <span data-ttu-id="ce17f-124">モデリング SDK</span><span class="sxs-lookup"><span data-stu-id="ce17f-124">Modeling SDK</span></span> | <span data-ttu-id="ce17f-125">あり</span><span class="sxs-lookup"><span data-stu-id="ce17f-125">Yes</span></span> | |
| <span data-ttu-id="ce17f-126">個々のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="ce17f-126">Individual component</span></span> | <span data-ttu-id="ce17f-127">DGML エディター</span><span class="sxs-lookup"><span data-stu-id="ce17f-127">DGML editor</span></span> | <span data-ttu-id="ce17f-128">なし</span><span class="sxs-lookup"><span data-stu-id="ce17f-128">No</span></span> | <span data-ttu-id="ce17f-129">このコンポーネントは、有向グラフ マークアップ言語を使用する依存関係グラフ機能で使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce17f-129">This component is used for dependency graph features using the Directed Graph Markup Language.</span></span> |
| <span data-ttu-id="ce17f-130">Visual Studio Marketplace</span><span class="sxs-lookup"><span data-stu-id="ce17f-130">Visual Studio Marketplace</span></span> | <span data-ttu-id="ce17f-131">Microsoft Reporting Services プロジェクト</span><span class="sxs-lookup"><span data-stu-id="ce17f-131">Microsoft Reporting Services Projects</span></span> | <span data-ttu-id="ce17f-132">あり</span><span class="sxs-lookup"><span data-stu-id="ce17f-132">Yes</span></span> | <span data-ttu-id="ce17f-133">このコンポーネントは、レポート開発に必要です。</span><span class="sxs-lookup"><span data-stu-id="ce17f-133">This component is needed for report development.</span></span> <span data-ttu-id="ce17f-134">コンポーネントがインストールされていない場合、Visual Studio はレポート デザインを開こうとすると、メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="ce17f-134">If the component isn't installed, Visual Studio will prompt you when you try to open report designs.</span></span> |

## <a name="dynamics-365-commerce"></a><span data-ttu-id="ce17f-135">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="ce17f-135">Dynamics 365 Commerce</span></span>

<span data-ttu-id="ce17f-136">コマースおよび Visual Studio 2017 の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce17f-136">For more information on Commerce and Visual Studio 2017, see these topics.</span></span>

- [<span data-ttu-id="ce17f-137">Retail SDK の Visual Studio 2015 から Visual Studio 2017 への移行</span><span class="sxs-lookup"><span data-stu-id="ce17f-137">Migrate the Retail SDK from Visual Studio 2015 to Visual Studio 2017</span></span>](../../../commerce/dev-itpro/retail-sdk/migrate-sdk.md)
- [<span data-ttu-id="ce17f-138">バージョン 10.0.10 から 10.0.13 における開発と ALM の変更</span><span class="sxs-lookup"><span data-stu-id="ce17f-138">Development and ALM changes from version 10.0.10 to 10.0.13</span></span>](../../../commerce/dev-itpro/dev-changes-10-13.md)

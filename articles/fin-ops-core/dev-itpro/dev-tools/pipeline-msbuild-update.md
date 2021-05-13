---
title: Azure Pipelines でのレガシ パイプラインの更新
description: このトピックでは、Azure Pipelines でのレガシ パイプラインを更新して、新しいバージョンの Visual Studio を使用する方法について説明します。
author: jorisdg
ms.date: 09/23/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16807192c52d23dd0784c2f0ed8311257db91bd8
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866238"
---
# <a name="update-a-legacy-pipeline-in-azure-pipelines"></a><span data-ttu-id="0e113-103">Azure Pipelines でのレガシ パイプラインの更新</span><span class="sxs-lookup"><span data-stu-id="0e113-103">Update a legacy pipeline in Azure Pipelines</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0e113-104">このドキュメントは、ビルド仮想マシン上で実行する場合でも、[新しいビルド パイプライン](hosted-build-automation.md) には適用されません。</span><span class="sxs-lookup"><span data-stu-id="0e113-104">This documentation does not apply to the [new build pipeline](hosted-build-automation.md), even if you run it on the build virtual machine.</span></span>

> <span data-ttu-id="0e113-105">バージョン 10.0.13 またはそれ以降が配置された仮想マシン上で **Visual Studio 2017** が使用可能な場合でも、**VSTest** を使用した単体テストをサポートするのに必要なビルド スクリプトには、バージョン 10.0.15 が必要です。</span><span class="sxs-lookup"><span data-stu-id="0e113-105">Even though **Visual Studio 2017** is available on virtual machines deployed with version 10.0.13 or later, the build scripts needed to support unit testing using **VSTest** require version 10.0.15.</span></span>

<span data-ttu-id="0e113-106">**Azure Pipelines** パイプラインは、**MSBuild** および **VS テスト** などの **Visual Studio** ツールのバージョンを明示的に指定します。</span><span class="sxs-lookup"><span data-stu-id="0e113-106">An **Azure Pipelines** pipeline explicitly specifies the versions of **Visual Studio** tools such as **MSBuild** and **VS Test**.</span></span> <span data-ttu-id="0e113-107">これらの製品の新しいバージョンのサポートを継続するために、新しい仮想マシンはプレインストールされている **Visual Studio** よりも新しいバージョンで配置されます。</span><span class="sxs-lookup"><span data-stu-id="0e113-107">To continue supporting newer versions of these products, new virtual machines will be deployed with newer versions of **Visual Studio** pre-installed.</span></span> <span data-ttu-id="0e113-108">新しいバージョンを使用するために、既存のパイプラインはすべて手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e113-108">Any existing pipelines need to be manually updated to use the newer version.</span></span>

## <a name="determine-if-your-pipeline-needs-to-be-updated"></a><span data-ttu-id="0e113-109">パイプラインを更新する必要があるかどうか確認する</span><span class="sxs-lookup"><span data-stu-id="0e113-109">Determine if your pipeline needs to be updated</span></span>

<span data-ttu-id="0e113-110">バージョン 10.0.13 を使用して配置されたビルドおよび開発仮想マシンには **Visual Studio 2017** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0e113-110">Build and development virtual machines deployed with version 10.0.13 include **Visual Studio 2017**.</span></span> <span data-ttu-id="0e113-111">2021 年 4 月のリリースでは、[Visual Studio 2015 のサポートは非推奨](../get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10011-of-finance-and-operations-apps) になります。</span><span class="sxs-lookup"><span data-stu-id="0e113-111">Support for [Visual Studio 2015 will be deprecated](../get-started/removed-deprecated-features-platform-updates.md#platform-updates-for-version-10011-of-finance-and-operations-apps) in the April 2021 release.</span></span> <span data-ttu-id="0e113-112">ビルド仮想マシンに **Visual Studio 2017** が含まれていない場合、バージョン 10.0.13 またはそれ以降の新しいビルド仮想マシンを配置する計画をするか、または新しく [ホストされるビルド パイプライン](hosted-build-automation.md) の使用を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e113-112">If your build virtual machine does not include **Visual Studio 2017** you must plan to deploy a new build virtual machine with version 10.0.13 or later, or consider using the new [hosted build pipeline](hosted-build-automation.md).</span></span>

<span data-ttu-id="0e113-113">ビルド仮想マシンに Visual Studio 2017 がインストールされている場合、新しいバージョンの **MSBuild** と **VS テスト** を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0e113-113">If your build virtual machine has Visual Studio 2017 installed, you can use the newer versions of **MSBuild** and **VS Test**.</span></span> <span data-ttu-id="0e113-114">パイプラインがバージョン 10.0.13 以前の仮想マシン配置によって作成されている場合、パイプラインを手動で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e113-114">If your pipeline was created by a virtual machine deployment prior to version 10.0.13, you will have to manually update the pipeline.</span></span>

<span data-ttu-id="0e113-115">最後に、**ソリューションのビルド** ステップでビルド パイプラインを確認できます。</span><span class="sxs-lookup"><span data-stu-id="0e113-115">Finally, you can check your build pipeline on the **Build the solution** step.</span></span> <span data-ttu-id="0e113-116">**MSBuild のバージョン** プロパティは、使用中の **Visual Studio** のバージョンを示しています。</span><span class="sxs-lookup"><span data-stu-id="0e113-116">The **MSBuild Version** property indicates the version of **Visual Studio** in use.</span></span>

| <span data-ttu-id="0e113-117">MSBuild のバージョン</span><span class="sxs-lookup"><span data-stu-id="0e113-117">MSBuild version</span></span> | <span data-ttu-id="0e113-118">Visual Studio のバージョン</span><span class="sxs-lookup"><span data-stu-id="0e113-118">Visual Studio version</span></span> |
|---|---|
| <span data-ttu-id="0e113-119">MSBuild 14.0</span><span class="sxs-lookup"><span data-stu-id="0e113-119">MSBuild 14.0</span></span> | <span data-ttu-id="0e113-120">Visual Studio2015</span><span class="sxs-lookup"><span data-stu-id="0e113-120">Visual Studio 2015</span></span> |
| <span data-ttu-id="0e113-121">MSBuild 15.0</span><span class="sxs-lookup"><span data-stu-id="0e113-121">MSBuild 15.0</span></span> | <span data-ttu-id="0e113-122">Visual Studio2017</span><span class="sxs-lookup"><span data-stu-id="0e113-122">Visual Studio 2017</span></span> |

## <a name="updating-the-azure-pipelines-pipeline"></a><span data-ttu-id="0e113-123">Azure Pipelines のパイプラインを更新する</span><span class="sxs-lookup"><span data-stu-id="0e113-123">Updating the Azure Pipelines pipeline</span></span>

> [!NOTE]
> <span data-ttu-id="0e113-124">**Azure Pipelines** のパイプラインを更新して、**Visual Studio 2017** を使用できるようにするには、ビルドの仮想マシンのバージョンが 10.0.15 またはそれ以降に更新されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="0e113-124">To update an **Azure Pipelines** pipeline to use **Visual Studio 2017**, ensure your build virtual machine has been updated to version 10.0.15 or newer.</span></span>

<span data-ttu-id="0e113-125">パイプラインの 3 つのタスク内にある、次の 4 つのプロパティを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0e113-125">The following four properties, in three tasks in the pipeline, need to be updated.</span></span>

| <span data-ttu-id="0e113-126">タスク名</span><span class="sxs-lookup"><span data-stu-id="0e113-126">Task name</span></span> | <span data-ttu-id="0e113-127">タスクのプロパティ</span><span class="sxs-lookup"><span data-stu-id="0e113-127">Task property</span></span> | <span data-ttu-id="0e113-128">元の値</span><span class="sxs-lookup"><span data-stu-id="0e113-128">Old value</span></span> | <span data-ttu-id="0e113-129">新しい値</span><span class="sxs-lookup"><span data-stu-id="0e113-129">New value</span></span>|
| --- | --- | --- | ---|
| <span data-ttu-id="0e113-130">ソリューションをビルドする</span><span class="sxs-lookup"><span data-stu-id="0e113-130">Build the solution</span></span> | <span data-ttu-id="0e113-131">MSBuild のバージョン</span><span class="sxs-lookup"><span data-stu-id="0e113-131">MSBuild Version</span></span> | <span data-ttu-id="0e113-132">MSBuild 14.0</span><span class="sxs-lookup"><span data-stu-id="0e113-132">MSBuild 14.0</span></span> | <span data-ttu-id="0e113-133">MSBuild 15.0</span><span class="sxs-lookup"><span data-stu-id="0e113-133">MSBuild 15.0</span></span> |
| <span data-ttu-id="0e113-134">データベース同期</span><span class="sxs-lookup"><span data-stu-id="0e113-134">Database Sync</span></span> | <span data-ttu-id="0e113-135">MSBuild のバージョン</span><span class="sxs-lookup"><span data-stu-id="0e113-135">MSBuild Version</span></span> | <span data-ttu-id="0e113-136">MSBuild 14.0</span><span class="sxs-lookup"><span data-stu-id="0e113-136">MSBuild 14.0</span></span> | <span data-ttu-id="0e113-137">MSBuild 15.0</span><span class="sxs-lookup"><span data-stu-id="0e113-137">MSBuild 15.0</span></span> |
| <span data-ttu-id="0e113-138">テストの実行</span><span class="sxs-lookup"><span data-stu-id="0e113-138">Execute Tests</span></span> | <span data-ttu-id="0e113-139">プラットフォーム バージョンのテスト</span><span class="sxs-lookup"><span data-stu-id="0e113-139">Test platform version</span></span> | <span data-ttu-id="0e113-140">Visual Studio2015</span><span class="sxs-lookup"><span data-stu-id="0e113-140">Visual Studio 2015</span></span> | <span data-ttu-id="0e113-141">Visual Studio2017</span><span class="sxs-lookup"><span data-stu-id="0e113-141">Visual Studio 2017</span></span> |
| <span data-ttu-id="0e113-142">テストの実行</span><span class="sxs-lookup"><span data-stu-id="0e113-142">Execute Tests</span></span> | <span data-ttu-id="0e113-143">その他のコンソール オプション</span><span class="sxs-lookup"><span data-stu-id="0e113-143">Other console options</span></span> | `/Platform:X64 /InIsolation /UseVsixExtensions:true` | `/Platform:X64 /InIsolation /TestAdapterPath:"$(VsixExtensionFolder)"` |



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
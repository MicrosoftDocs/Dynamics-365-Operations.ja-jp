---
title: "Retail チャネル拡張機能を最新の Retail SDK にアップグレード"
description: "このトピックでは、以前のリリースから Retail チャネル拡張機能を Retail SDK の最新の更新プログラムにアップグレードする方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 11/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: kfendd
ms.search.scope: Operations, Retail
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 209/07/2018
ms.dyn365.ops.version: AX 7.3.5
ms.translationtype: HT
ms.sourcegitcommit: d4e5d20d7f632a074cffdbe57e6a31140adf17c5
ms.openlocfilehash: 767ffaf742dc794dc60fe74942d2b295ac918d07
ms.contentlocale: ja-jp
ms.lasthandoff: 12/11/2018

---

# <a name="upgrade-the-retail-channel-extension-to-the-latest-retail-sdk"></a><span data-ttu-id="d75c8-103">Retail チャネル拡張機能を最新の Retail SDK にアップグレード</span><span class="sxs-lookup"><span data-stu-id="d75c8-103">Upgrade the Retail channel extension to the latest Retail SDK</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d75c8-104">このトピックでは、以前のリリースから Retail SDK の最新の更新プログラムにアップグレードする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-104">This topic provides information about how to upgrade to the latest update of the Retail SDK from earlier releases.</span></span> <span data-ttu-id="d75c8-105">プロセス全体とサポートされるシナリオの情報が含まれていますが、このトピックではプロセスの各ステップに関する詳細な指示は提示しません。</span><span class="sxs-lookup"><span data-stu-id="d75c8-105">The overall process and the supported scenario information are included, but this topic doesn’t provide detailed instructions of every step in the process.</span></span> <span data-ttu-id="d75c8-106">このトピックは、Dynamics 365 for Retail および Dynamics 365 for Finance and Operations 7.3 バージョン以上に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-106">This topic is applicable for Dynamics 365 for Retail and Dynamics 365 for Finance and Operations 7.3 version and higher.</span></span>
<span data-ttu-id="d75c8-107">以下のセクションは新しい Retail SDK に拡張機能を手動で移動する方法を説明しますが、Azure DevOps または Git などのソース管理システムを使用してこれを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-107">The following sections will walk through how to manually move your extension to the new Retail SDK, however you can do this using any source control system like Azure DevOps or Git.</span></span>

## <a name="update-the-retail-sdk"></a><span data-ttu-id="d75c8-108">Retail SDK の更新</span><span class="sxs-lookup"><span data-stu-id="d75c8-108">Update the Retail SDK</span></span>
<span data-ttu-id="d75c8-109">新しいバイナリの修正プログラムを適用することで Retail SDK を更新するときに、既存の Retail SDK フォルダー内に新しい **更新** フォルダーと、更新済の SDK のコピーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-109">When you update the Retail SDK by applying a new binary hotfix, a new **Update** folder is created inside the existing RetailSDK folder and a copy of the updated SDK is created.</span></span> <span data-ttu-id="d75c8-110">新しい環境を配置する場合、新しい Retail SDK は仮想マシン (VM) のサービス ボリュームまたはダウンロード可能な VHD の C ドライブにあります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-110">If you deploy a new environment, the new Retail SDK is located in the services volume of the virtual machine (VM) or in the C drive of the downloadable VHD.</span></span>

### <a name="retail-sdk-components"></a><span data-ttu-id="d75c8-111">Retail SDK のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="d75c8-111">Retail SDK components</span></span>

<span data-ttu-id="d75c8-112">Retail SDK の更新は、主に次のコンポーネントで構成されます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-112">The Retail SDK updates consist mainly of the following components:</span></span>

-   <span data-ttu-id="d75c8-113">資産: 拡張機能に関連するコンフィギュレーション ファイル変更。</span><span class="sxs-lookup"><span data-stu-id="d75c8-113">Assets: Configuration file changes related to extensions.</span></span>
-   <span data-ttu-id="d75c8-114">ビルド ツール: カスタマイズ パッケージおよびバージョン管理設定。</span><span class="sxs-lookup"><span data-stu-id="d75c8-114">Build tools: Customization package and versioning settings.</span></span>
-   <span data-ttu-id="d75c8-115">データベース: 拡張 DB スクリプト。</span><span class="sxs-lookup"><span data-stu-id="d75c8-115">Database: Extension DB scripts.</span></span>
-   <span data-ttu-id="d75c8-116">ドキュメント: サンプルを実行する方法。</span><span class="sxs-lookup"><span data-stu-id="d75c8-116">Documents: Instructions to run the samples.</span></span>
-   <span data-ttu-id="d75c8-117">パッケージ: 配置パッケージ。</span><span class="sxs-lookup"><span data-stu-id="d75c8-117">Package: Deployment package.</span></span>
-   <span data-ttu-id="d75c8-118">支払の外部参照: 支払パッケージング フォルダー。</span><span class="sxs-lookup"><span data-stu-id="d75c8-118">Payment externals: Payment packaging folders.</span></span>
-   <span data-ttu-id="d75c8-119">支払: 支払のサンプル コード。</span><span class="sxs-lookup"><span data-stu-id="d75c8-119">Payment: Payment sample code.</span></span>
-   <span data-ttu-id="d75c8-120">POS: Modern POS および Cloud POS のアプリケーション コードとサンプル</span><span class="sxs-lookup"><span data-stu-id="d75c8-120">POS: Modern and Cloud POS App code and samples.</span></span>
-   <span data-ttu-id="d75c8-121">参照: すべてのバイナリ参照およびコマース アナライザー プロキシ ツール。</span><span class="sxs-lookup"><span data-stu-id="d75c8-121">References: All binary reference and commerce analyzer proxy tool.</span></span>
-   <span data-ttu-id="d75c8-122">サンプル拡張機能: 拡張機能のサンプル プロジェクト。</span><span class="sxs-lookup"><span data-stu-id="d75c8-122">Sample extensions: Extension sample projects.</span></span>

## <a name="upgrade-scenarios"></a><span data-ttu-id="d75c8-123">アップグレード シナリオ</span><span class="sxs-lookup"><span data-stu-id="d75c8-123">Upgrade scenarios</span></span>
<span data-ttu-id="d75c8-124">次のシナリオのいずれかでアップグレードを完了することができます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-124">Upgrade can be completed for one of the following scenarios:</span></span>

  - <span data-ttu-id="d75c8-125">特定のバイナリ修正プログラムを更新する。</span><span class="sxs-lookup"><span data-stu-id="d75c8-125">Update to a specific binary hotfix.</span></span>
  - <span data-ttu-id="d75c8-126">カスタム コードをアップグレードする。</span><span class="sxs-lookup"><span data-stu-id="d75c8-126">Upgrade your custom code.</span></span>
  - <span data-ttu-id="d75c8-127">最新のアプリケーション リリースにアップグレードする。</span><span class="sxs-lookup"><span data-stu-id="d75c8-127">Upgrade to the latest application release.</span></span>

<span data-ttu-id="d75c8-128">SDK アップグレード プロセスは、バージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-128">The process for SDK upgrade varies between versions.</span></span> <span data-ttu-id="d75c8-129">バージョン 7.3 以降では、すべての Retail コンポーネントがシールされており、拡張点を使用してのみカスタマイズを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-129">With version 7.3 and higher, we sealed all of the Retail components and customizations must be completed only by using the extension points.</span></span> <span data-ttu-id="d75c8-130">これにより、コード アップグレード作業が容易になります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-130">This should result in an easier code upgrade experience.</span></span> <span data-ttu-id="d75c8-131">ただし、7.0、7.1、または 7.2 からアップグレードした場合と、インライン変更を行った場合、インラインを拡張機能に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-131">However, if you are upgrading from 7.0, 7.1, or 7.2 and if you have made inline changes, you must move the inline changes to extensions.</span></span> <span data-ttu-id="d75c8-132">これには追加の作業が必要になります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-132">This will require additional work.</span></span>

<span data-ttu-id="d75c8-133">次の表では、コードがシールされているバージョンに関する一部の概要情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-133">The following tables provide some high-level information about which version the code is sealed.</span></span> <span data-ttu-id="d75c8-134">アンシールド バージョンからシールド バージョンにアップグレードする場合は、すべてのカスタマイズを識別し、拡張機能にインライン カスタマイズを移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-134">If you are upgrading from an unsealed version to a sealed version, you should identify all of your customizations and move any inline customizations to extensions.</span></span> <span data-ttu-id="d75c8-135">インライン カスタマイズを移動するには、これを行うために必要な拡張ポイントがすべてあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-135">To move the inline customizations, verify that you have all of the necessary extension points to do this.</span></span> <span data-ttu-id="d75c8-136">ない場合は、拡張機能の要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-136">If you don't, submit an extensibility request.</span></span> 

> [!NOTE]
> <span data-ttu-id="d75c8-137">バージョン 7.3 以上にアップグレードする際、7.1 で行った POS インラインの変更の一部を書き換える必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-137">You might have to rewrite some of the POS inline changes that were completed in 7.1 when you upgrade to version 7.3 or higher.</span></span>

| <span data-ttu-id="d75c8-138">**アプリケーションのバージョン**</span><span class="sxs-lookup"><span data-stu-id="d75c8-138">**Application version**</span></span>                 | <span data-ttu-id="d75c8-139">**CRT シールド**</span><span class="sxs-lookup"><span data-stu-id="d75c8-139">**CRT sealed**</span></span> | <span data-ttu-id="d75c8-140">**HWS シールド**</span><span class="sxs-lookup"><span data-stu-id="d75c8-140">**HWS sealed**</span></span> | <span data-ttu-id="d75c8-141">**POS シールド**</span><span class="sxs-lookup"><span data-stu-id="d75c8-141">**POS sealed**</span></span> | <span data-ttu-id="d75c8-142">**DB シールド**</span><span class="sxs-lookup"><span data-stu-id="d75c8-142">**DB sealed**</span></span> | <span data-ttu-id="d75c8-143">**Retail プロキシ シールド**</span><span class="sxs-lookup"><span data-stu-id="d75c8-143">**Retail proxy sealed**</span></span> |
|-----------------------------------------|----------------|----------------|----------------|---------------|-------------------------|
| <span data-ttu-id="d75c8-144">アプリケーション リリース 8.1</span><span class="sxs-lookup"><span data-stu-id="d75c8-144">Application release 8.1</span></span>                 | <span data-ttu-id="d75c8-145">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-145">Yes</span></span>            | <span data-ttu-id="d75c8-146">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-146">Yes</span></span>            | <span data-ttu-id="d75c8-147">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-147">Yes</span></span>            | <span data-ttu-id="d75c8-148">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-148">Yes</span></span>           | <span data-ttu-id="d75c8-149">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-149">Yes</span></span>                     |
| <span data-ttu-id="d75c8-150">アプリケーション リリース 8.0</span><span class="sxs-lookup"><span data-stu-id="d75c8-150">Application release 8.0</span></span>                 | <span data-ttu-id="d75c8-151">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-151">Yes</span></span>            | <span data-ttu-id="d75c8-152">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-152">Yes</span></span>            | <span data-ttu-id="d75c8-153">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-153">Yes</span></span>            | <span data-ttu-id="d75c8-154">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-154">Yes</span></span>           | <span data-ttu-id="d75c8-155">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-155">Yes</span></span>                     |
| <span data-ttu-id="d75c8-156">アプリケーション 7.3</span><span class="sxs-lookup"><span data-stu-id="d75c8-156">Application 7.3</span></span>                         | <span data-ttu-id="d75c8-157">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-157">Yes</span></span>            | <span data-ttu-id="d75c8-158">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-158">Yes</span></span>            | <span data-ttu-id="d75c8-159">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-159">Yes</span></span>            | <span data-ttu-id="d75c8-160">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-160">Yes</span></span>           | <span data-ttu-id="d75c8-161">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-161">Yes</span></span>                     |
| <span data-ttu-id="d75c8-162">2017 年 7 月のリリース (アプリケーション 7.2)</span><span class="sxs-lookup"><span data-stu-id="d75c8-162">July 2017 release (Application 7.2)</span></span>     | <span data-ttu-id="d75c8-163">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-163">Yes</span></span>            | <span data-ttu-id="d75c8-164">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-164">Yes</span></span>            | <span data-ttu-id="d75c8-165">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-165">Yes</span></span>            | <span data-ttu-id="d75c8-166">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-166">Yes</span></span>           | <span data-ttu-id="d75c8-167">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-167">No</span></span>                      |
| <span data-ttu-id="d75c8-168">リリース 1611 (アプリケーション 7.1)</span><span class="sxs-lookup"><span data-stu-id="d75c8-168">Release 1611 (Application 7.1)</span></span>          | <span data-ttu-id="d75c8-169">有</span><span class="sxs-lookup"><span data-stu-id="d75c8-169">Yes</span></span>            | <span data-ttu-id="d75c8-170">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-170">No</span></span>             | <span data-ttu-id="d75c8-171">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-171">No</span></span>             | <span data-ttu-id="d75c8-172">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-172">No</span></span>            | <span data-ttu-id="d75c8-173">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-173">No</span></span>                      |
| <span data-ttu-id="d75c8-174">2016 年 2 月リリース (アプリケーション 7.0)</span><span class="sxs-lookup"><span data-stu-id="d75c8-174">February 2016 release (Application 7.0)</span></span> | <span data-ttu-id="d75c8-175">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-175">No</span></span>             | <span data-ttu-id="d75c8-176">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-176">No</span></span>             | <span data-ttu-id="d75c8-177">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-177">No</span></span>             | <span data-ttu-id="d75c8-178">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-178">No</span></span>            | <span data-ttu-id="d75c8-179">無</span><span class="sxs-lookup"><span data-stu-id="d75c8-179">No</span></span>                      |

## <a name="upgrade-the-retail-channel-extension-from-73-to-a-higher-version"></a><span data-ttu-id="d75c8-180">7.3 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="d75c8-180">Upgrade the Retail channel extension from 7.3 to a higher version</span></span>

<span data-ttu-id="d75c8-181">コード アップグレードを実行している場合、Retail SDK の次のコンポーネントをアップグレードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-181">If you are completing a code upgrade, the following Retail SDK components must be upgraded.</span></span> <span data-ttu-id="d75c8-182">これらの各コンポーネントは、Retail SDK 内のフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="d75c8-182">Each of these components are folders inside the Retail SDK.</span></span>

> [!NOTE]
> <span data-ttu-id="d75c8-183">ソース管理/マージ ツールを使用してコード アップグレードを完了できます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-183">Code upgrade can be completed using a source control/merge tool.</span></span> <span data-ttu-id="d75c8-184">変更を追跡して必要に応じて戻すことができるように、このプロセスでソース コード管理ツールを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-184">We recommend using a source control tool for this process so that you can track the changes and revert if required.</span></span> <span data-ttu-id="d75c8-185">ソース管理を使用していない場合、コードをアップグレードする前に、古いおよび新しい Retail SDK フォルダーのバックアップを作成することを確認します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-185">If you are not using any source control, before you upgrade the code, be sure to make a back up of the old and new retail SDK folder.</span></span>

- <span data-ttu-id="d75c8-186">**資産:** カスタム アセンブリを含めるために次の拡張構成ファイルのいずれかを変更した場合、これらの変更を新しい**資産フォルダー**にある同じ構成ファイルに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-186">**Assets:** If you have modified any of the following extension config files to include your custom assemblies, you must move those changes to the same config files in the new **Asset folder**.</span></span>

  - <span data-ttu-id="d75c8-187">CommerceRuntime.Ext.config - CRT 拡張。</span><span class="sxs-lookup"><span data-stu-id="d75c8-187">CommerceRuntime.Ext.config - CRT extensions.</span></span>
  - <span data-ttu-id="d75c8-188">CommerceRuntime.MPOSOffline.Ext.config - CRT オフライン拡張。</span><span class="sxs-lookup"><span data-stu-id="d75c8-188">CommerceRuntime.MPOSOffline.Ext.config - CRT offline extensions.</span></span>
  - <span data-ttu-id="d75c8-189">HardwareStation.Extension.config - ハードウェア ステーションと支払拡張機能。</span><span class="sxs-lookup"><span data-stu-id="d75c8-189">HardwareStation.Extension.config - Hardware station and payment extensions.</span></span>
  - <span data-ttu-id="d75c8-190">RetailProxy.MPOSOffline.ext.config - Retail プロキシ拡張機能。</span><span class="sxs-lookup"><span data-stu-id="d75c8-190">RetailProxy.MPOSOffline.ext.config - Retail proxy extensions.</span></span>

- <span data-ttu-id="d75c8-191">**ビルド ツール:** **ビルド ツール** フォルダーには、パッケージング、ビルド設定と pfx、および snk ファイルに関連するファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d75c8-191">**Build tools:** The **Build tools** folder contains the files related to packaging, build settings and pfx, and snk files.</span></span> <span data-ttu-id="d75c8-192">以前のバージョンで変更を加えた場合は、以下のファイルをマージおよび更新します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-192">Merge or update the following files if you have made any changes in the older versions:</span></span>

  - <span data-ttu-id="d75c8-193">Customization.settings</span><span class="sxs-lookup"><span data-stu-id="d75c8-193">Customization.settings</span></span>
  - <span data-ttu-id="d75c8-194">Microsoft.Dynamics.RetailSdk.Build.props</span><span class="sxs-lookup"><span data-stu-id="d75c8-194">Microsoft.Dynamics.RetailSdk.Build.props</span></span>
  - <span data-ttu-id="d75c8-195">作成したカスタム pfx または snk ファイル。</span><span class="sxs-lookup"><span data-stu-id="d75c8-195">Any custom pfx or snk files that you have created.</span></span>

- <span data-ttu-id="d75c8-196">**データベース:** カスタム SQL スクリプトをすべてコピーしてドロップします: ...\\RetailSDK\\Database\\Upgrade\\Custom</span><span class="sxs-lookup"><span data-stu-id="d75c8-196">**Database:** Copy and drop all your custom SQL scripts: ...\\RetailSDK\\Database\\Upgrade\\Custom</span></span>

- <span data-ttu-id="d75c8-197">**オンライン ストア:** オンライン ストア Web プロジェクトまたはオンライン拡張コードがある場合、このフォルダーに含めます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-197">**Online Store:** If you have an online store web project or online extension code, include it in this folder.</span></span> 
  > [!NOTE]
  > <span data-ttu-id="d75c8-198">Retail 配置可能パッケージには、パッケージ用のオンライン ストア コードは含まれません。</span><span class="sxs-lookup"><span data-stu-id="d75c8-198">Retail deployable package will not include online store code for packaging.</span></span>

- <span data-ttu-id="d75c8-199">**支払の外部参照**: 支払拡張アセンブリすべてをコピーして以下の**支払アセンブリ** フォルダーに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-199">**Payment externals**: Copy and paste all of your payment extension assemblies to the following **Payment assemblies** folders:</span></span>

  - <span data-ttu-id="d75c8-200">IPaymentDeviceAssemblies</span><span class="sxs-lookup"><span data-stu-id="d75c8-200">IPaymentDeviceAssemblies</span></span>
  - <span data-ttu-id="d75c8-201">IPaymentProcessorAssemblies</span><span class="sxs-lookup"><span data-stu-id="d75c8-201">IPaymentProcessorAssemblies</span></span>
  - <span data-ttu-id="d75c8-202">PaymentWebFiles</span><span class="sxs-lookup"><span data-stu-id="d75c8-202">PaymentWebFiles</span></span>

- <span data-ttu-id="d75c8-203">**支払:** このフォルダーにすべての支払拡張プロジェクトをマージします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-203">**Payments:** Merge all of your payment extension projects into this folder.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d75c8-204">新しい支払拡張機能プロジェクトを作成したが、このフォルダーは何も変更しなかった場合、ビルドとパッケージング プロセスの一部として含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-204">If you created a new payment extension project and did not modify anything in this folder, you can include it as part of the build and packaging process.</span></span> <span data-ttu-id="d75c8-205">**RetailSDK** フォルダーで **dirs.proj** を更新し、カスタム プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-205">Update **dirs.proj** in the **RetailSDK** folder to build your custom project.</span></span> <span data-ttu-id="d75c8-206">次に、支払拡張機能の格納場所で **Customization.settings** ファイルを更新し、パッケージの作成時にカスタム プロジェクトがビルドされるようにします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-206">Next, update the **Customization.settings** file with the payment extension drop location so that during package creation your custom project is built.</span></span> <span data-ttu-id="d75c8-207">必ず、パッケージの一部として拡張機能を含めます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-207">Make sure to include the extension as part of the packaging.</span></span>

- <span data-ttu-id="d75c8-208">**POS:** 生成されたプロキシを含む任意の POS 拡張機能がある場合、POS 拡張機能を *…\\RetailSDK\\POS\\Extensions* から新しい Retail SDK POS 拡張子フォルダー *RetailSDK\\POS\\Extensions* にコピーします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-208">**POS:** If you have any POS extensions, including the generated proxy, copy your POS extensions from *…\\RetailSDK\\POS\\Extensions* to the new Retail SDK POS extension folder, *RetailSDK\\POS\\Extensions*.</span></span> <span data-ttu-id="d75c8-209">拡張機能をコピーしたら、*POS\\Extensions* フォルダー内の extension.json ファイルを更新して、コピーした新しい POS 拡張機能とマージします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-209">After you copy the extensions,  update and merge the extension.json file inside the *POS\\Extensions* folder with the new POS extensions folder you copied.</span></span>

  <span data-ttu-id="d75c8-210">たとえば、**CustomExtension** フォルダーをコピーした場合、以下に示すように extension.json を更新します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-210">For example, if you copied the **CustomExtension** folder, then you would update extension.json as shown below.</span></span>
  ```Typescript

   {
   "extensionPackages": [
   {
     "baseUrl": "SampleExtensions"
   },
   {
    "baseUrl": "SampleExtensions2"
   },
   {
    "baseUrl": "CustomExtension"
   }
  ]
   }
  ```
 
 <span data-ttu-id="d75c8-211">ビルド中に変更を POS がコンパイルできるように、カスタム拡張機能パッケージで tsconfig.json を更新する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-211">You should also update tsconfig.json with the custom extension package so that the POS can compile the changes during build.</span></span>

- <span data-ttu-id="d75c8-212">**参照:** **Commerce ランタイム**、**ハードウェア ステーション**、**プロキシ** などのすべての拡張機能出力アセンブリと、へのすべての外部アセンブリを参照フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-212">**Reference:** Copy all of your extension output assemblies, such as **Commerce runtime**, **Hardware station**, **proxy**, and any external assemblies, to the reference folder.</span></span> <span data-ttu-id="d75c8-213">配置およびパッケージの一部として含めようとしているすべてのアセンブリを含めます。</span><span class="sxs-lookup"><span data-stu-id="d75c8-213">Include any assemblies that you want included as part of your deployment and packaging.</span></span>

- <span data-ttu-id="d75c8-214">**Commerce ランタイム (CRT) と小売サーバー (RS) 拡張:** CRT および RS 拡張機能プロジェクトすべてを **Retail SDK** フォルダーの下にコピーします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-214">**Commerce runtime (CRT) and retail server (RS) extensions:** Copy all of your CRT and RS extension projects under the **Retail SDK** folder.</span></span> <span data-ttu-id="d75c8-215">msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが *RetailSDK\\Reference* フォルダーに設定されるように、必ず、CRT および RS 拡張ソリューション ファイルの詳細を **RetailSDK フォルダー**にある dirs.proj ファイルに含めてください。</span><span class="sxs-lookup"><span data-stu-id="d75c8-215">Make sure to include the CRT and RS extension solution file details in the dirs.proj file under the **RetailSDK folder** so that during msbuild, all of the extension project is built and the output path for the project assemblies is set to the *RetailSDK\\Reference* folder.</span></span>

- <span data-ttu-id="d75c8-216">**ハードウェア ステーション (HWS) および支払拡張機能:** すべてのハードウェア ステーション (HWS) と支払拡張プロジェクトを **Retail SDK** フォルダーの下にコピーします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-216">**Hardware station (HWS) and payment extensions:** Copy all of your hardware station (HWS) and payment extension projects under the **Retail SDK** folder.</span></span> <span data-ttu-id="d75c8-217">msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが *RetailSDK\\Reference* フォルダーに設定されるように、必ず、HWS および支払拡張ソリューション ファイルの詳細を **RetailSDK** フォルダーにある dirs.proj ファイルに含めてください。</span><span class="sxs-lookup"><span data-stu-id="d75c8-217">Make sure to include the HWS and payment extension solution file details in the dirs.proj file under the **RetailSDK** folder so that during msbuild, all of the extension projects are built and the output path for the project assemblies is set to the *RetailSDK\\Reference* folder.</span></span>

- <span data-ttu-id="d75c8-218">**Retail プロキシ拡張:** すべての Retail プロキシ拡張プロジェクトを **Retail SDK** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d75c8-218">**Retail proxy extensions:** Copy all of your retail proxy extension projects under the **Retail SDK** folder.</span></span> <span data-ttu-id="d75c8-219">msbuild 中にすべての拡張プロジェクトがビルドされ、プロジェクト アセンブリの出力パスが *RetailSDK\\Reference* フォルダーに設定されるように、必ず、プロキシ ソリューション ファイルの詳細を **RetailSDK** フォルダーにある dirs.proj ファイルに含めてください。</span><span class="sxs-lookup"><span data-stu-id="d75c8-219">Make sure to include the proxy solution file details in the dirs.proj file under the **RetailSDK** folder so that during msbuild, all of the extension projects are built and the output path for the project assemblies is set to the *RetailSDK\\Reference* folder.</span></span>

> [!NOTE]
> <span data-ttu-id="d75c8-220">Retail SDK フォルダーのルートで **msbuild** を実行します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-220">Run **msbuild** on the root of the Retail SDK folder.</span></span> <span data-ttu-id="d75c8-221">配置可能小売パッケージを生成するために、Microsoft Visual Studio 開発者コマンド ライン ツールを使用します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-221">Use the Microsoft Visual Studio developer command-line tool to generate the retail deployable packages.</span></span>

<span data-ttu-id="d75c8-222">すべてのコンポーネントをアップグレードしたら、Retail 配置可能パッケージを配置し、配置を検証して、Retail SDK ファイルをリポジトリに追加します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-222">After you have upgraded all of the components, deploy the Retail deployable packages, validate the deployment, and add the Retail SDK files to the repository.</span></span>

## <a name="upgrade-the-retail-channel-extension-from-72-to-a-higher-version"></a><span data-ttu-id="d75c8-223">7.2 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="d75c8-223">Upgrade the Retail channel extension from 7.2 to a higher version</span></span>
<span data-ttu-id="d75c8-224">前のセクション **7.3 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする**で説明した手順は、Retail プロキシを除くすべての小売コンポーネントでも同じです。</span><span class="sxs-lookup"><span data-stu-id="d75c8-224">The steps mentioned  in the previous section, **Upgrade the retail channel extension from 7.3 to higher versions**, will remain same for all the retail components except the Retail proxy.</span></span> <span data-ttu-id="d75c8-225">RS 拡張機能を持つ CRT があり、**customization.settings** ファイルに基づいて TypeScript セッションが自動生成された場合、7.2 では、Retail プロキシ プロジェクトでインライン変更を完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-225">In 7.2, you must have completed inline changes in the retail proxy project if you have CRT with RS extension and the typescript proxy was auto-generated based on the **customization.settings** file.</span></span>

<span data-ttu-id="d75c8-226">プロキシを 7.3 にアップグレードするには、[Typescript および小売販売時点管理 (POS) の C# プロキシ](typescript-proxy-retail-pos.md)のトピックの手順を完了した後、Retail SDK フォルダーにプロキシを移動し、構成ファイル **RetailProxy.MPOSOffline.ext.config** を更新します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-226">To upgrade your proxy to 7.3, complete the steps in the topic, [Typescript and C# proxies for Retail point of sale (POS)](typescript-proxy-retail-pos.md) and then move the proxy to the Retail SDK folder and then update the config file, **RetailProxy.MPOSOffline.ext.config**.</span></span>

## <a name="upgrade-the-retail-channel-extension-from-71-to-a-higher-version"></a><span data-ttu-id="d75c8-227">7.1 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="d75c8-227">Upgrade the Retail channel extension from 7.1 to a higher version</span></span>
<span data-ttu-id="d75c8-228">7.1 では、POS およびプロキシ カスタマイズ インラインのほとんどを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-228">In 7.1, you should have completed most of the POS and Proxy customizations inline.</span></span> <span data-ttu-id="d75c8-229">それ以上のアプリケーション リリースにアップグレードするは、すべてのインライン変更を拡張機能に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-229">To upgrade to higher a application release, you should move all of your inline changes to extensions.</span></span> <span data-ttu-id="d75c8-230">バイナリ修正プログラムのアップグレードの場合、新しい Retail SDK とのコード マージを実行し、パッケージを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-230">If it is a binary hotfix upgrade, then you must perform a code merge with the new Retail SDK and then regenerate the package.</span></span>

## <a name="upgrade-the-retail-channel-extension-from-70-to-a-higher-version"></a><span data-ttu-id="d75c8-231">7.0 からそれ以上のバージョンに Retail チャネル拡張機能をアップグレードする</span><span class="sxs-lookup"><span data-stu-id="d75c8-231">Upgrade the Retail channel extension from 7.0 to a higher version</span></span>
<span data-ttu-id="d75c8-232">7.0 では、カスタマイズ インラインのほとんどを完了している必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-232">In 7.0, you should have completed most of the customizations inline.</span></span> <span data-ttu-id="d75c8-233">それ以上のアプリケーション リリースにアップグレードするは、すべてのインライン変更を拡張機能に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-233">To upgrade to higher a application release, you should move all of your inline changes to extensions.</span></span> <span data-ttu-id="d75c8-234">バイナリ修正プログラムのアップグレードの場合、新しい Retail SDK とのコード マージを実行し、パッケージを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d75c8-234">If it is binary hotfix upgrade, you must perform a code merge with the new Retail SDK and regenerate the package.</span></span>

## <a name="generate-a-deployable-package-for-validation"></a><span data-ttu-id="d75c8-235">検証用の配置可能パッケージを生成する</span><span class="sxs-lookup"><span data-stu-id="d75c8-235">Generate a deployable package for validation</span></span>
<span data-ttu-id="d75c8-236">トピック[配置可能な小売パッケージの作成](retail-sdk/retail-sdk-packaging.md)の手順を完了し、検証用の配置可能パッケージを生成します。</span><span class="sxs-lookup"><span data-stu-id="d75c8-236">Complete the steps in the topic, [Create retail deployable packages](retail-sdk/retail-sdk-packaging.md), to generate the deployable package for validation.</span></span>


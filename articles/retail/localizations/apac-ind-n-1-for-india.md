---
title: インドにおけるアップグレードおよび N-1 のサポート
description: このトピックでは、インドでの小売顧客向けの N-1 サポート概要を提供します。
author: DmitryAkimoff
manager: ezubov
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: India
ms.search.industry: Retail
ms.author: dmakimo
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 5407976f48750951fcf5766576c6c48b0df69058
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2023379"
---
# <a name="support-for-upgrade-and-n-1-for-india"></a><span data-ttu-id="bf347-103">インドにおけるアップグレードおよび N-1 のサポート</span><span class="sxs-lookup"><span data-stu-id="bf347-103">Support for upgrade and N-1 for India</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bf347-104">このトピックでは、インドでの Phased Rollout (N-1) 小売コンポーネントの設定および使用に必要な手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="bf347-104">This topic describes the steps needed to set up and use Phased Rollout (N-1) retail components for India.</span></span> <span data-ttu-id="bf347-105">N-1 のアップグレード手順およびワークフローは、基本的に一般的な Dynamics 365 Retail 環境のものと同じです。</span><span class="sxs-lookup"><span data-stu-id="bf347-105">The upgrade procedure and the workflow for N-1 are basically the same as for a general Dynamics 365 Retail environment.</span></span> <span data-ttu-id="bf347-106">N-1 のインストールおよび使用の一般的な情報は、[Retail のアップグレードおよび N-1 のサポート](../dev-itpro/overview-upgrade-n-minus1.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf347-106">For general information about N-1 installation and usage, see [Upgrade and N-1 support for Retail](../dev-itpro/overview-upgrade-n-minus1.md).</span></span>

<span data-ttu-id="bf347-107">さらに、次の手順はアップグレードのために重要です。</span><span class="sxs-lookup"><span data-stu-id="bf347-107">In addition, the following steps are important for upgrade:</span></span>

- <span data-ttu-id="bf347-108">Dynamics 365 Retail Headquarters および AX 2012 Retail コンポーネントの両方が商品及びサービス税 (GST) 計算をサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf347-108">Both Dynamics 365 Retail Headquarters and AX 2012 Retail components must support Goods and Services Tax (GST) calculation.</span></span> <span data-ttu-id="bf347-109">詳細については、[必要条件](#prerequisites) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf347-109">See the [Prerequisites](#prerequisites) section for details.</span></span>
- <span data-ttu-id="bf347-110">AX 2012 チャネル側で Dynamics 365 Retail のために準備されたコンフィギュレーションを使用するには、GST コンフィギュレーションのダウングレードが必要です。</span><span class="sxs-lookup"><span data-stu-id="bf347-110">Downgrade of the GST configuration is required to use the configuration prepared for Dynamics 365 Retail at the AX 2012 channel side.</span></span>
- <span data-ttu-id="bf347-111">配送スケジュールには、Dynamics 365 Retail Headquarters と AX 2012 チャンネル間で GST コンフィギュレーションおよび税計算結果を同期するために必要となる、追加のアップロード ジョブおよびダウンロード ジョブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bf347-111">Distribution schedule includes additional upload and download jobs required to synchronize GST configuration and tax calculation results between Dynamics 365 Retail Headquarters and AX 2012 channels.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bf347-112">必要条件</span><span class="sxs-lookup"><span data-stu-id="bf347-112">Prerequisites</span></span>

- <span data-ttu-id="bf347-113">AX 2013 R3 小売コンポーネントを GST Update 2、[KB4058327](https://fix.lcs.dynamics.com/Issue/Details?kb=4058327&bugId=3898178&qc=acbe1a0b3f5d9240d56a94a633fa69fbfe4be0cf98587fd05a7807e082210a12)、またはそれ以降に更新します。</span><span class="sxs-lookup"><span data-stu-id="bf347-113">Update AX 2013 R3 retail components to GST Update 2, [KB4058327](https://fix.lcs.dynamics.com/Issue/Details?kb=4058327&bugId=3898178&qc=acbe1a0b3f5d9240d56a94a633fa69fbfe4be0cf98587fd05a7807e082210a12), or higher.</span></span> <span data-ttu-id="bf347-114">詳細については、[インド GST 更新 2 - リリース ノート](https://mbs.microsoft.com/Files/customer/AX/Downloads/Taxupdates/Release-Note-India-GST-Update-2.pdf)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf347-114">For details, see [India GST Update 2 - Release Notes](https://mbs.microsoft.com/Files/customer/AX/Downloads/Taxupdates/Release-Note-India-GST-Update-2.pdf).</span></span>
- <span data-ttu-id="bf347-115">基本的な N-1 環境を設定します。</span><span class="sxs-lookup"><span data-stu-id="bf347-115">Set up basic N-1 environment.</span></span> <span data-ttu-id="bf347-116">詳細については、[Phased Rollout (N-1) のインストール、コンフィギュレーション、および切替ガイド](../dev-itpro/n-1-installation-configuration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bf347-116">For more information, refer to [Phased Rollout (N-1) installation, configuration, and cutover guide](../dev-itpro/n-1-installation-configuration.md).</span></span>
- <span data-ttu-id="bf347-117">[インド向けキャッシュ レジスターの商品およびサービス税 (GST) の統合](./apac-ind-cash-registers.md) ガイドに基づき、Dynamics 365 Retail Headquarters でインド向けの Retail 用商品とサービス税 (GST) を設定します。</span><span class="sxs-lookup"><span data-stu-id="bf347-117">Set up Goods and Services Tax (GST) for Retail for India in Dynamics 365 Retail Headquarters according to the [Goods and Services Tax (GST) integration for cash registers for India](./apac-ind-cash-registers.md) guide.</span></span>

## <a name="periodic-procedure-to-downgrade-tax-configuration"></a><span data-ttu-id="bf347-118">税コンフィギュレーションをダウングレードする定期処理</span><span class="sxs-lookup"><span data-stu-id="bf347-118">Periodic procedure to downgrade tax configuration</span></span>

<span data-ttu-id="bf347-119">GST コンフィギュレーションは AX 2012 および Dynamics 365 Retail のバージョン間で異なります。</span><span class="sxs-lookup"><span data-stu-id="bf347-119">GST configuration data differs between AX 2012 and Dynamics 365 Retail versions.</span></span> <span data-ttu-id="bf347-120">データを変換するには、特別な定期処理手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf347-120">A special periodic procedure should be run to transform data.</span></span> <span data-ttu-id="bf347-121">この手順を実行するには、以下の内容を実行します:</span><span class="sxs-lookup"><span data-stu-id="bf347-121">To run this procedure, do the following:</span></span>

1. <span data-ttu-id="bf347-122">Retail Headquarters にサインインして、**小売 \> Retail IT \> N-1 から税構成を処理する**に移動します。</span><span class="sxs-lookup"><span data-stu-id="bf347-122">Sign in to Retail headquarters, and go to **Retail \> Retail IT \> Process tax configuration from N-1**.</span></span>
2. <span data-ttu-id="bf347-123">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bf347-123">Click **OK**.</span></span>

<span data-ttu-id="bf347-124">税構成の変更が行われて確定するたび、データを AX 2012 チャネルに送信する間に上記の操作を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf347-124">Each time tax configuration changes are made and finalized the above operation should be run before sending the data to the AX 2012 channel.</span></span>

---
title: 予算案の有効化 (プレビュー)
description: このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222537"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="39ee5-103">予算案の有効化 (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="39ee5-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="39ee5-104">このトピックでは、財務インサイトの予算案機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="39ee5-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="39ee5-105">Microsoft Dynamics Lifecycle Services (LCS) で環境ページの情報を使用して、その環境に対する Azure SQL のプライマリ インスタンスに接続します。</span><span class="sxs-lookup"><span data-stu-id="39ee5-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="39ee5-106">次の Transact-SQL (T-SQL) コマンドを実行して、サンドボックス環境のフライトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="39ee5-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="39ee5-107">(Application Object Server \[AOS\] にリモートで接続する前に、LCS で IP アドレスに対してアクセスを有効にする必要がある場合があります。)</span><span class="sxs-lookup"><span data-stu-id="39ee5-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="39ee5-108">バージョン 10.0.20 以降を使用している場合や、Service Fabric のデプロイを使用している場合は、この手順をスキップします。</span><span class="sxs-lookup"><span data-stu-id="39ee5-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="39ee5-109">財務インサイト チームは既にフライトを有効にしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="39ee5-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="39ee5-110">**機能管理** ワークスペースに機能が表示されない場合や、有効にしようとしたときに問題が発生した場合は、<fiap@microsoft.com> までご連絡ください。</span><span class="sxs-lookup"><span data-stu-id="39ee5-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="39ee5-111">**機能管理** ワークスペースを開き、次の手順に従います:</span><span class="sxs-lookup"><span data-stu-id="39ee5-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="39ee5-112">**更新プログラムの確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39ee5-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="39ee5-113">**予算案** を検索し、その機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="39ee5-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="39ee5-114">**予算作成 \>設定 \> 基本予算作成 \> 予算案 (プレビュー)** に移動して、**機能の有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="39ee5-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

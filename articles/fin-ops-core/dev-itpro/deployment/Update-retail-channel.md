---
title: Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用
description: このトピックでは、クラウドでホストされているコマース チャネル コンポーネントへの更新プログラムと拡張機能を適用する方法について説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: d6b47b1ebfb7339d99d7913ebe3167321e8f0d88
ms.sourcegitcommit: abd1dd6cc00daee847480828d8a3ba567bc17714
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2021
ms.locfileid: "5117447"
---
# <a name="apply-updates-and-extensions-to-commerce-scale-unit-cloud"></a><span data-ttu-id="4ba19-103">Commerce Scale Unit (クラウド) への更新プログラムと拡張機能の適用</span><span class="sxs-lookup"><span data-stu-id="4ba19-103">Apply updates and extensions to Commerce Scale Unit (cloud)</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4ba19-104">アプリケーション バージョン 8.1.2 以降でレベル 2 サンドボックスまたは運用環境を更新し、Commerce Scale Unit (CSU) を初期化した場合は、チャネル コンポーネントも更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ba19-104">If you are updating a Tier-2 sandbox or production environment on application version 8.1.2 or newer and have initialized Commerce Scale Unit (CSU), you will also need to update channel components.</span></span> <span data-ttu-id="4ba19-105">このトピックでは、CSU に更新と拡張を適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-105">This topic shows how to apply updates and extensions to CSU.</span></span>

<span data-ttu-id="4ba19-106">CSU の更新は累積的です。</span><span class="sxs-lookup"><span data-stu-id="4ba19-106">Updates to CSU are cumulative.</span></span> <span data-ttu-id="4ba19-107">つまり、適用する更新すべてに、以前のリリースされたすべての変更がが含まれます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-107">This means that any update that you apply will include all previously released changes.</span></span> <span data-ttu-id="4ba19-108">Dynamics 365 Commerce の拡張の配置可能パッケージを適用することも累積的なプロセスであり、拡張機能の以前に配置されたバージョンが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-108">Applying a Dynamics 365 Commerce deployable package for extensions is also a cumulative process and will replace the previously deployed version of the extension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4ba19-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="4ba19-109">Prerequisites</span></span>

<span data-ttu-id="4ba19-110">続行する前に、まず更新および拡張機能 (該当する場合) を環境に適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ba19-110">Before you proceed, you must first apply updates and extensions (if applicable) to the environment.</span></span> <span data-ttu-id="4ba19-111">詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ba19-111">For more information, see [Apply updates to cloud environments](apply-deployable-package-system.md).</span></span>

<span data-ttu-id="4ba19-112">CSU を更新するには、それぞれについて、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-112">To update CSU, complete the following steps for each:</span></span>

1. <span data-ttu-id="4ba19-113">**環境の詳細** ページで、**環境機能 > Retail およびコマース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-113">On the **Environment details** page, go to **Environment features > Retail and Commerce**.</span></span>
2. <span data-ttu-id="4ba19-114">**コマース配置設定** ページで、**更新** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-114">On the **Commerce deployment setup** page, select **Update**.</span></span>
3. <span data-ttu-id="4ba19-115">選択パネルで、更新先のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-115">In the selection panel, select the version to update to.</span></span>
4. <span data-ttu-id="4ba19-116">最新のサービス更新プログラムを適用して最新の機能にアクセスすることも、最新の品質更新プログラムに更新して、現在展開されているサービス更新プログラムの品質改善を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-116">You can choose to update to the newest service update to access the latest features, or you can update to the latest quality update to apply quality improvements for the currently deployed service update.</span></span> <span data-ttu-id="4ba19-117">詳細については、[Lifecycle Services (LCS) から更新プログラムをダウンロード](../migration-upgrade/download-hotfix-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ba19-117">For more information, see [Download updates from Lifecycle Services (LCS)](../migration-upgrade/download-hotfix-lcs.md).</span></span>
5. <span data-ttu-id="4ba19-118">また、同時に拡張機能を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-118">You can choose to apply an extension at the same time.</span></span> 

<span data-ttu-id="4ba19-119">拡張機能を CSU に適用するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-119">To apply an extension to a CSU, complete the following steps:</span></span>

1. <span data-ttu-id="4ba19-120">**コマース配置設定** ページで、**拡張機能の適用** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-120">On the **Commerce deployment setup** page, select **Apply Extension**.</span></span>
2. <span data-ttu-id="4ba19-121">選択パネルで、適用する拡張機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-121">In the selection panel, select the extension to apply.</span></span>

> [!NOTE]
> <span data-ttu-id="4ba19-122">LCS の **コマース配置設定ページ** でパッケージを展開する前に、まず Microsoft Dynamics Lifecycle Services (LCS) でコマース配置可能パッケージをプロジェクト資産ライブラリにアップロードしてください。</span><span class="sxs-lookup"><span data-stu-id="4ba19-122">You must first upload the Commerce deployable package to the project asset library in Microsoft Dynamics Lifecycle Services (LCS) before you can select to deploy it on the **Commerce deployment setup page** in LCS.</span></span>

<span data-ttu-id="4ba19-123">**更新プログラムの適用** および **拡張機能の適用** 操作の両方はダウンタイム (最大 1 時間) を伴い、場合によっては最大 2 時間以上になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="4ba19-123">Both **Apply updates** and **Apply extension** operations will involve a period of downtime that may last up to 1 hour, or in some cases up to 2 hours or more.</span></span> <span data-ttu-id="4ba19-124">たとえば、CSU の米国以外の場所を更新する場合、大量のデータ、または複雑なスキーマの更新が行われます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-124">For example, when updating non-US locations of CSU, large data volumes, or complex schema updates.</span></span> <span data-ttu-id="4ba19-125">ダウンタイム期間の現実的な予測については、運用環境で使用する予定のものと同等の更新およびデータセットに対するサンドボックス UAT のダウンタイム期間を記録します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-125">For a realistic estimate of the downtime duration, note the downtime duration in Sandbox UAT for an equivalent update and dataset that you plan to use in your production environment.</span></span> <span data-ttu-id="4ba19-126">この時間中、次のことが発生します。</span><span class="sxs-lookup"><span data-stu-id="4ba19-126">During this time, the following will occur:</span></span>

- <span data-ttu-id="4ba19-127">クラウドでホストされている Commerce チャネルは機能しません (POS オフライン機能が有効な場合を除く)。</span><span class="sxs-lookup"><span data-stu-id="4ba19-127">Cloud-hosted Commerce channels will not function (unless POS offline capability is enabled).</span></span>
- <span data-ttu-id="4ba19-128">オフライン機能が有効になっている POS デバイスの機能が制限されます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-128">POS devices that have the offline capability feature enabled will have reduced functionality.</span></span>
- <span data-ttu-id="4ba19-129">CCSU に依存しているすべての電子商取引クライアントが中断されます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-129">Any e-commerce clients that are dependent on CCSU will be disrupted.</span></span>
- <span data-ttu-id="4ba19-130">CSU でホストされているチャネルも影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="4ba19-130">Channels hosted on CSUs will remain unaffected.</span></span>
- <span data-ttu-id="4ba19-131">本社機能も影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="4ba19-131">Head office functionality will remain unaffected.</span></span>

> [!NOTE]
> <span data-ttu-id="4ba19-132">拡張機能と更新プログラムを同時に適用するには、1 回のダウンタイムが必要なため、複数のダウンタイムを避ける効果的な方法です。</span><span class="sxs-lookup"><span data-stu-id="4ba19-132">Applying an extension and an update at the same time requires a single downtime, and can be an effective way of averting multiple downtimes.</span></span>

## <a name="view-history"></a><span data-ttu-id="4ba19-133">履歴の表示</span><span class="sxs-lookup"><span data-stu-id="4ba19-133">View history</span></span>
<span data-ttu-id="4ba19-134">最新の操作履歴をスケールユニットで表示するには、**アクション** タブの **履歴** を選択し、**スケール ユニットの履歴** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-134">To view the history of recent operations on a Scale Unit, select **History** on the **Action** tab to open the **Scale Unit History** page.</span></span> <span data-ttu-id="4ba19-135">このページでは、初期化、サービス更新、品質更新、バージョン、拡張機能の詳細、その他の関連情報など、最近の操作を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-135">On this page, you can view recent operations such as initialize, service update, quality update, version, extension details, and other relevant information.</span></span>

## <a name="csu-auto-update-sequence"></a><span data-ttu-id="4ba19-136">CSU の自動更新順序</span><span class="sxs-lookup"><span data-stu-id="4ba19-136">CSU auto-update sequence</span></span>

> [!NOTE]
> <span data-ttu-id="4ba19-137">CSUの自動更新は、徐々にすべてのコマース顧客に展開されます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-137">Auto-update for CSU is being gradually rolled out to all Commerce customers.</span></span> <span data-ttu-id="4ba19-138">LCS プロジェクトの所有者または環境管理者である場合は、CSU の自動更新が LCS プロジェクトに展開されるときに、電子メールで通知されます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-138">If you are a LCS project owner or environment administrator, you'll recieve an email notification when CSU auto-update is rolled out to your LCS project.</span></span>

<span data-ttu-id="4ba19-139">CSU は、Microsoft によって自動更新された後、次の順序で実行されます。</span><span class="sxs-lookup"><span data-stu-id="4ba19-139">When CSU is auto-updated by Microsoft, it takes place in the following sequence.</span></span>

![CSU の自動更新順序](./media/CSU-auto-update-timeline.png)



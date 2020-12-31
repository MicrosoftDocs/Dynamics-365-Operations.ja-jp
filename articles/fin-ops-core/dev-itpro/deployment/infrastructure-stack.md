---
title: セルフサービス配置の概要
description: このトピックでは、セルフサービス配置の概要を示します。
author: rashmansur
manager: AnnBe
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: ef720d78b5d3be5056fd60dc79a8931f53afec8d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681625"
---
# <a name="self-service-deployment-overview"></a><span data-ttu-id="f9072-103">セルフサービス配置の概要</span><span class="sxs-lookup"><span data-stu-id="f9072-103">Self-service deployment overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="f9072-104">クラウド環境では、セルフサービス配置が可能です。</span><span class="sxs-lookup"><span data-stu-id="f9072-104">Self-service deployment is available for cloud environments.</span></span> <span data-ttu-id="f9072-105">セルフ サービス配置により、簡単な配置が可能になり配置時間が大幅に減少します。</span><span class="sxs-lookup"><span data-stu-id="f9072-105">Self-service deployment enables easier deployment and significantly reduced deployment times.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f9072-106">この機能は、Microsoft Azure の国/地域に基づいて段階的にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="f9072-106">The functionality for this feature will be released incrementally, based on your Microsoft Azure country/region.</span></span> <span data-ttu-id="f9072-107">ただし、この機能は現在、Finance and Operations アプリのサインアップ過程にいる **新しい顧客** のみ利用可能です。</span><span class="sxs-lookup"><span data-stu-id="f9072-107">However, this functionality is currently available only for **new customers** who are in the process of signing up for Finance and Operations apps.</span></span> <span data-ttu-id="f9072-108">現在の顧客の既存の環境に変更はありません。</span><span class="sxs-lookup"><span data-stu-id="f9072-108">There is no change in existing environments for current customers.</span></span>
>
> <span data-ttu-id="f9072-109">すべての新しい顧客にこの機能が表示されるわけではない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="f9072-109">Note that not all new customers will see this functionality.</span></span> <span data-ttu-id="f9072-110">ただし、アクセス権を持つ新しい顧客の数は、徐々に増加します。</span><span class="sxs-lookup"><span data-stu-id="f9072-110">However, the number of new customers who have access to it will gradually increase.</span></span> 

## <a name="whats-new-or-changed"></a><span data-ttu-id="f9072-111">新規または変更</span><span class="sxs-lookup"><span data-stu-id="f9072-111">What’s new or changed</span></span>

<span data-ttu-id="f9072-112">セルフ サービス機能を使用する顧客は、Lifecycle Services (LCS) エクスペリエンスにおいて次の変更が見られます。</span><span class="sxs-lookup"><span data-stu-id="f9072-112">Customers using the self-service capabilities will see the following changes in their Lifecycle Services (LCS) experience.</span></span> 

- <span data-ttu-id="f9072-113">配置はセルフ サービスであり、平均 30 分以内に完了することができます。</span><span class="sxs-lookup"><span data-stu-id="f9072-113">Deployment is self-service and can be completed within an average time of 30 minutes.</span></span> <span data-ttu-id="f9072-114">配置のリード タイムや待機時間はなくなります。</span><span class="sxs-lookup"><span data-stu-id="f9072-114">There are no longer lead times and wait times for deployment.</span></span> <span data-ttu-id="f9072-115">いつ配置するかを制御し、環境が展開されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f9072-115">You can control when you deploy, and verify that the environment is deployed.</span></span> <span data-ttu-id="f9072-116">このエクスペリエンスは、現在のエクスペリエンスと同じです。</span><span class="sxs-lookup"><span data-stu-id="f9072-116">This experience is the same as the current experience.</span></span> <span data-ttu-id="f9072-117">詳細については、 [セルフサービス配置の FAQ](deploymentFAQ.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9072-117">For more information, see [Self-service deployment FAQ](deploymentFAQ.md).</span></span>

   ![配置設定](media/deployment-settings.png)

- <span data-ttu-id="f9072-119">レベル 2 以上のサンドボックス環境へのリモート デスクトップ アクセスがなくなります。</span><span class="sxs-lookup"><span data-stu-id="f9072-119">You will no longer have remote desktop access to the Tier 2+ sandbox environments.</span></span> <span data-ttu-id="f9072-120">リモート デスクトップ アクセスが必要なすべての操作は、セルフ サービス アクションとして使用可能になりました。</span><span class="sxs-lookup"><span data-stu-id="f9072-120">All operations that need remote desktop access are now available as self-service actions.</span></span> <span data-ttu-id="f9072-121">次の図に、環境の **メンテナンス** \> **データベース メニューの移動** オプションにおける操作の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="f9072-121">The following image shows some of the operations in the environment’s **Maintain** \> **Move database menu** option.</span></span> <span data-ttu-id="f9072-122">詳細については、[配置のメンテナンス操作](maintenanceoperationsguide-newinfrastructure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9072-122">For more information, see [Maintenance operations for deployments](maintenanceoperationsguide-newinfrastructure.md).</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f9072-123">リモート デスクトップ アクセスは、セルフ サービス展開を使用して配置された環境にのみ制限されます。</span><span class="sxs-lookup"><span data-stu-id="f9072-123">Remote desktop access will be restricted only to environments deployed using the self-service deployment.</span></span> <span data-ttu-id="f9072-124">既存の環境または既存の顧客に変更はありません。</span><span class="sxs-lookup"><span data-stu-id="f9072-124">There is no change to existing environments or existing customers.</span></span> 

   ![セルフ サービス アクション](media/Self-service-actions.png)

- <span data-ttu-id="f9072-126">診断機能は、同じままです。リモート デスクトップ アクセスなしでトラブルシューティングが可能になります。</span><span class="sxs-lookup"><span data-stu-id="f9072-126">The diagnostics capabilities will remain the same, which enables troubleshooting without remote desktop access.</span></span> <span data-ttu-id="f9072-127">詳細については、[セルフサービス配置で配置された環境のトラブルシューティング](troubleshoot-newinfrastructure.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9072-127">For more information, see [Troubleshoot environments deployed through self-service deployment](troubleshoot-newinfrastructure.md).</span></span> 

   ![環境の監視](media/environment-monitoring.png)

- <span data-ttu-id="f9072-129">レベル 2 以上では SQL Server アクセスはありません。</span><span class="sxs-lookup"><span data-stu-id="f9072-129">You will not have SQL Server access on Tier 2+.</span></span> <span data-ttu-id="f9072-130">Just-In-Time アクセスを使用して SQL データベース アクセスすることは引き続きできます。</span><span class="sxs-lookup"><span data-stu-id="f9072-130">You will continue to have SQL database access using just-in-time access.</span></span>

- <span data-ttu-id="f9072-131">カスタマイズのための結合された配置可能パッケージを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9072-131">You will need to provide a combined deployable package for customizations.</span></span> <span data-ttu-id="f9072-132">つまり、ISV パッケージを含む、すべてのカスタム拡張機能パッケージは、1 つのソフトウェア配置可能パッケージとして配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9072-132">That is, all custom extension packages, including ISV packages, must be deployed as a single software deployable package.</span></span> <span data-ttu-id="f9072-133">一度に 1 つのモジュールを配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="f9072-133">You will not be able to deploy one module at a time.</span></span> <span data-ttu-id="f9072-134">これは常に推奨されるベスト プラクティスであり、適用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f9072-134">This was always a recommended best practice and is now enforced.</span></span>

- <span data-ttu-id="f9072-135">ドキュメントのプレビュー エクスペリエンスが改善され、印刷処理の性能が向上しました。</span><span class="sxs-lookup"><span data-stu-id="f9072-135">The document preview experience has been improved to deliver greater fidelity with the printed output.</span></span> <span data-ttu-id="f9072-136">この変更前は、画面に表示されたドキュメントは、HTML ビューアーを使用して表示されていました。</span><span class="sxs-lookup"><span data-stu-id="f9072-136">Before this change, documents viewed on screen were displayed using an HTML viewer.</span></span> <span data-ttu-id="f9072-137">HTML 形式では、組み込みドリルスルー リンクや折りたたみ可能なセクションなどのインタラクティブ機能がサポートされていましたが、これはサービスによって表示されるドキュメントの実際の表示ではありませんでした。</span><span class="sxs-lookup"><span data-stu-id="f9072-137">Although the HTML format supported interactive functions like embedded drill-thru links and collapsible sections, this was not a true representation of the document rendered by the service.</span></span> <span data-ttu-id="f9072-138">新しい埋め込み PDF ビューアーを使用して、顧客は印刷されたドキュメントと一致するプレビューにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f9072-138">With the new embedded PDF Viewer, customers have access to a preview that's consistent with the printed documents.</span></span> <span data-ttu-id="f9072-139">詳細については、[埋め込みビュアーを使用してPDFドキュメントのプレビューをする](../analytics/preview-pdf-documents.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f9072-139">For more information, see [Preview PDF documents with an embedded viewer](../analytics/preview-pdf-documents.md).</span></span>

- <span data-ttu-id="f9072-140">組み込み SSRS フレームワークを使用して表示されるドキュメント レポートでは、カスタム フォントはサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f9072-140">Custom fonts are no longer supported for document reports rendered using the built-in SSRS framework.</span></span> <span data-ttu-id="f9072-141">Finance and Operations アプリには、クラウドでホストされるサービスによって表示されるドキュメントに使用できる、何百もの [標準のビジネス対応フォント](../analytics/supported-fonts.md) へのアクセスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f9072-141">Finance and Operations apps include access to hundreds of [standard, business-ready fonts](../analytics/supported-fonts.md) available for documents rendered by the cloud-hosted service.</span></span> <span data-ttu-id="f9072-142">このポートフォリオは、サービスが新しい地域や業界に拡大するにつれて増え続けます。</span><span class="sxs-lookup"><span data-stu-id="f9072-142">This portfolio will continue to grow as the service expands into new regions and industries.</span></span> <span data-ttu-id="f9072-143">ただし、サービスでは、顧客環境でのカスタム フォントのインストールはサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f9072-143">However, the service no longer supports the installation of custom fonts in customer environments.</span></span> <span data-ttu-id="f9072-144">サービスでサポートされるフォントのコレクションを拡張する要求は、その都度考慮されます。</span><span class="sxs-lookup"><span data-stu-id="f9072-144">Requests to expand the collection of fonts supported by the service will be considered on a case-by-case basis.</span></span>

- <span data-ttu-id="f9072-145">サービスでは、SQL Server Reporting Services (SSRS) レポートに埋め込まれた Visual Basic スクリプトを使用して定義されるビジネス ロジックはサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f9072-145">The service no longer supports business logic defined using Visual Basic script embedded in SQL Server Reporting Services (SSRS) reports.</span></span> <span data-ttu-id="f9072-146">実行時にデータを書式設定および評価するために使用される Tablix コントロールで定義された Visual Basic 式は、引き続き完全にサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f9072-146">Visual Basic expressions defined in Tablix controls used to format and evaluate data at runtime will continue to be fully supported.</span></span> <span data-ttu-id="f9072-147">ただし、サービスは Visual Basic スクリプト関数で定義された指示を無視します。</span><span class="sxs-lookup"><span data-stu-id="f9072-147">However, the service will ignore instructions defined in Visual Basic script functions.</span></span> <span data-ttu-id="f9072-148">この変更は、サービスのセキュリティと信頼性の向上に必要でした。</span><span class="sxs-lookup"><span data-stu-id="f9072-148">This change was necessary to improve the security and reliability of the service.</span></span>

- <span data-ttu-id="f9072-149">サブレポートは、SSRS 開発ツールを使用して定義されたドキュメント レポートではサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f9072-149">Sub reports are no longer supported in document reports defined using the SSRS development tools.</span></span> <span data-ttu-id="f9072-150">サブレポートを含むアプリケーション ソリューションは、再作成するか、サービスでサポートされる他のレポート オプションを活用するソリューションに置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9072-150">Application solutions that include sub reports will need to be recreated or replaced with solutions that take advantage of other reporting options supported by the service.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="f9072-151">サブレポート項目のサポートは、プラットフォーム更新プログラム 36 リリースと共に再導入されました。</span><span class="sxs-lookup"><span data-stu-id="f9072-151">Support for sub report items has been re-introduced with the Platform update 36 release.</span></span> <span data-ttu-id="f9072-152">適切に書式設定されたサブレポート項目を含むソリューションに依存する顧客は、プラットフォーム更新 36 またはそれ以降で実行されるセルフサービス配置に移行できます。</span><span class="sxs-lookup"><span data-stu-id="f9072-152">Customers dependent on solutions that include properly formatted sub report items can transition to self-service deployments running on Platform update 36 or later.</span></span>

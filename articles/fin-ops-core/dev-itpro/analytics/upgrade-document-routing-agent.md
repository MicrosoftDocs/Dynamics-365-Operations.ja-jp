---
title: ドキュメント回覧エージェントのアップグレード
description: このトピックでは、ドキュメント巡回エージェントをアップグレードする方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f33afb444654c23007b9a22d25d5871f81fa6c30
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191555"
---
# <a name="upgrade-the-document-routing-agent"></a><span data-ttu-id="060d4-103">ドキュメント回覧エージェントのアップグレード</span><span class="sxs-lookup"><span data-stu-id="060d4-103">Upgrade the Document Routing Agent</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="060d4-104">プラットフォーム更新プログラム 12 には、ネットワーク印刷機能を提供するコンポーネントに対するいくつかの重要な拡張機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="060d4-104">Platform update 12 includes several important enhancements to the components that provide network printing capabilities.</span></span> <span data-ttu-id="060d4-105">たとえば、印刷ジョブ キューを管理するソリューションは、印刷ジョブの管理サービスが大量の印刷要件を満たすために調整されるよう再設計されました。</span><span class="sxs-lookup"><span data-stu-id="060d4-105">For example, the solution for managing the print job queue has been redesigned so that the Print Job Management service can be scaled to satisfy high-volume printing requirements.</span></span> <span data-ttu-id="060d4-106">印刷ジョブの管理サービスには、市場バージョンのドキュメント回覧エージェント (DRA) クライアントと下位互換性のあるバージョンがありますが、顧客がオンプレミスでホストされている既存の DRA クライアントを**すべて**アップグレードすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="060d4-106">Although the Print Job Management service is backward-compatible with in-market versions of the Document Routing Agent (DRA) client, we strongly recommend that customers upgrade **all** existing DRA clients that are hosted on-premises.</span></span>

<span data-ttu-id="060d4-107">DRA の既存のインストールをプラットフォーム更新プログラム 12 またはそれ以降のバージョンにアップグレードしない場合は、次の問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="060d4-107">If you don't upgrade existing installations of the DRA to Platform update 12 or later, you might experience the following issues:</span></span>

- <span data-ttu-id="060d4-108">アプリケーションで監視可能なパフォーマンスの低下</span><span class="sxs-lookup"><span data-stu-id="060d4-108">Observable performance degradation in applications</span></span>
- <span data-ttu-id="060d4-109">孤立した印刷ジョブに関連する文書の消失</span><span class="sxs-lookup"><span data-stu-id="060d4-109">Document loss that is associated with orphaned print jobs</span></span>
- <span data-ttu-id="060d4-110">カスタムの余白がある印刷ドキュメントの一貫性のない処理</span><span class="sxs-lookup"><span data-stu-id="060d4-110">Inconsistent handling of printed documents that have custom margins</span></span>

<span data-ttu-id="060d4-111">IT 管理者は、DRA をホストするために使用される各ドメイン リソースに対して、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="060d4-111">IT administrators must perform the following procedures on each domain resource that is used to host a DRA.</span></span>

## <a name="get-started"></a><span data-ttu-id="060d4-112">はじめに</span><span class="sxs-lookup"><span data-stu-id="060d4-112">Get started</span></span>
<span data-ttu-id="060d4-113">DRA を Microsoft Windows サービスとして引き続き実行するには、サービスを実行するために使用されるドメイン アカウントのユーザー名とパスワードの両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="060d4-113">To continue to run the DRA as a Microsoft Windows service, you must have both the user name and the password of the domain account that is used to run the service.</span></span> <span data-ttu-id="060d4-114">この情報は、アップグレード完了後に使用可能になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="060d4-114">This information must be available after the upgrade is completed.</span></span> <span data-ttu-id="060d4-115">有効なサービス アカウントの情報を検索するには、Microsoft 管理コンソール (MMC) サービス スナップインを起動し、一覧から **Microsoft Dynamics 365 ドキュメント回覧サービス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="060d4-115">To find the information for the active service account, start the Microsoft Management Console (MMC) Services snap-in, and select **Microsoft Dynamics 365 Document Routing Service** in the list.</span></span>

![マネージャー スナップイン](media/Services_dialog.png)

## <a name="uninstall-an-existing-document-routing-agent"></a><span data-ttu-id="060d4-117">既存のドキュメント回覧エージェントのアンインストール</span><span class="sxs-lookup"><span data-stu-id="060d4-117">Uninstall an existing Document Routing Agent</span></span>
<span data-ttu-id="060d4-118">**プログラムと機能**を開き、**Microsoft Dynamics 365 for Finance and Operations: ドキュメント回覧**を検索し、削除します。</span><span class="sxs-lookup"><span data-stu-id="060d4-118">Open **Programs and Features**, and then find and uninstall **Microsoft Dynamics 365 for Finance and Operations: Document Routing**.</span></span>

![プログラム ウィンドウのアンインストールまたは変更](media/Programs_and_Features_dialog.png)

<span data-ttu-id="060d4-120">アンインストールのプロセス中に、Microsoft Dynamics 365 ドキュメント回覧サービス アプリケーションを終了するメッセージが表示された場合は、**セットアップが完了したら、アプリケーションを自動的に閉じて再起動します。** を選択します。</span><span class="sxs-lookup"><span data-stu-id="060d4-120">During the uninstallation process, if you're prompted to close the Microsoft Dynamics 365 Document Routing Service application, select **Automatically close applications and attempt to restart them after setup is complete.**</span></span>

![アプリケーションの終了を促すダイアログ ボックス](media/Uninstall_DRA_services.png)

## <a name="install-the-latest-document-routing-agent"></a><span data-ttu-id="060d4-122">最新のドキュメント回覧エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="060d4-122">Install the latest Document Routing Agent</span></span>
<span data-ttu-id="060d4-123">定期売買で使用可能な最新の DRA をインストールする方法の詳細については、[ネットワーク プリンター デバイスを有効にするためにドキュメント回覧エージェントをインストールする](install-document-routing-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="060d4-123">For information about how to install the latest DRA that is available with your subscription, see [Install the Document Routing Agent to enable network printer devices](install-document-routing-agent.md).</span></span>

> [!NOTE]
> <span data-ttu-id="060d4-124">アップグレード後に DRA クライアントを開いて、ネットワーク ユーザーの資格情報を更新してください。</span><span class="sxs-lookup"><span data-stu-id="060d4-124">Be sure to open the DRA client after upgrading to refresh network user credentials.</span></span>

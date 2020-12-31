---
title: ドキュメント回覧エージェントの更新
description: このトピックでは、ドキュメント回覧エージェントを更新する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4169f32fa30f9c4e32de546c5df5507553f56d0e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687415"
---
# <a name="update-the-document-routing-agent"></a><span data-ttu-id="a51d1-103">ドキュメント回覧エージェントの更新</span><span class="sxs-lookup"><span data-stu-id="a51d1-103">Update the Document Routing Agent</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a51d1-104">印刷ジョブ キューを管理するソリューションは、顧客が大容量印刷の要件を満たすために Dynamics 365 Finance and Operations アプリを適切に拡張できるように設計されています。</span><span class="sxs-lookup"><span data-stu-id="a51d1-104">The solution for managing the print job queue is designed to allow customers to properly scale Dynamics 365 Finance and Operations apps to satisfy high-volume printing requirements.</span></span> <span data-ttu-id="a51d1-105">印刷ジョブの管理に使用されるパブリック サービス エンドポイントは下位互換性がありますが、顧客が **すべて** の既存のドキュメント回覧エージェント (Document Routing Agent: DRA) クライアントを更新することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a51d1-105">Although public service endpoints used to manage print jobs are backward-compatible, we strongly recommend that customers update **all** existing Document Routing Agent (DRA) clients.</span></span>

<span data-ttu-id="a51d1-106">DRA の既存のインストールを最新バージョンに更新しないと、次のような問題が発生する可能性があります:</span><span class="sxs-lookup"><span data-stu-id="a51d1-106">If you don't update existing installations of the DRA the most current version, you might experience issues such as:</span></span>

- <span data-ttu-id="a51d1-107">アプリケーションで監視可能なパフォーマンスの低下</span><span class="sxs-lookup"><span data-stu-id="a51d1-107">Observable performance degradation in applications</span></span>
- <span data-ttu-id="a51d1-108">孤立した印刷ジョブに関連する文書の消失</span><span class="sxs-lookup"><span data-stu-id="a51d1-108">Document loss that is associated with orphaned print jobs</span></span>
- <span data-ttu-id="a51d1-109">カスタムの余白がある印刷ドキュメントの一貫性のない処理</span><span class="sxs-lookup"><span data-stu-id="a51d1-109">Inconsistent handling of printed documents that have custom margins</span></span>

<span data-ttu-id="a51d1-110">IT 管理者は、DRA をホストするために使用される各ドメイン リソースに対して、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-110">IT administrators must perform the following procedures on each domain resource that is used to host a DRA.</span></span>

> [!NOTE]
> <span data-ttu-id="a51d1-111">DRA 更新プログラムを完了すると、IT 管理者は、ホストサーバー経由で接続しているすべてのプリンターを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-111">When you complete a DRA update, IT administrators should register any printers that are connected through the host server.</span></span> <span data-ttu-id="a51d1-112">ネットワーク パスによって識別されるネットワーク プリンターでは、パスが変更されていない限りは更新の必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a51d1-112">For network printers that are identified by their network paths, if the paths have not changed, updates are not required.</span></span>

## <a name="get-started"></a><span data-ttu-id="a51d1-113">はじめに</span><span class="sxs-lookup"><span data-stu-id="a51d1-113">Get started</span></span>
<span data-ttu-id="a51d1-114">DRA を Microsoft Windows サービスとして引き続き実行するには、サービスを実行するために使用されるドメイン アカウントのユーザー名とパスワードの両方が必要です。</span><span class="sxs-lookup"><span data-stu-id="a51d1-114">To continue to run the DRA as a Microsoft Windows service, you must have both the user name and the password of the domain account that is used to run the service.</span></span> <span data-ttu-id="a51d1-115">この情報は、更新プログラム完了後に使用可能になっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a51d1-115">This information must be available after the update is completed.</span></span> <span data-ttu-id="a51d1-116">有効なサービス アカウントの情報を検索するには、Microsoft 管理コンソール (MMC) サービス スナップインを起動し、一覧から **Microsoft Dynamics 365 ドキュメント回覧サービス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-116">To find the information for the active service account, start the Microsoft Management Console (MMC) Services snap-in, and select **Microsoft Dynamics 365 Document Routing Service** in the list.</span></span>

![マネージャー スナップイン](media/Services_dialog.png)

## <a name="uninstall-an-existing-document-routing-agent"></a><span data-ttu-id="a51d1-118">既存のドキュメント回覧エージェントのアンインストール</span><span class="sxs-lookup"><span data-stu-id="a51d1-118">Uninstall an existing Document Routing Agent</span></span>
<span data-ttu-id="a51d1-119">**プログラムと機能** を開き、**Microsoft Dynamics 365 for Finance and Operations: ドキュメント回覧** を検索し、削除します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-119">Open **Programs and Features**, and then find and uninstall **Microsoft Dynamics 365 for Finance and Operations: Document Routing**.</span></span>

![プログラム ウィンドウのアンインストールまたは変更](media/Programs_and_Features_dialog.png)

<span data-ttu-id="a51d1-121">アンインストールのプロセス中に、Microsoft Dynamics 365 ドキュメント回覧サービス アプリケーションを終了するメッセージが表示された場合は、**セットアップが完了したら、アプリケーションを自動的に閉じて再起動します。** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a51d1-121">During the uninstallation process, if you're prompted to close the Microsoft Dynamics 365 Document Routing Service application, select **Automatically close applications and attempt to restart them after setup is complete.**</span></span>

![アプリケーションの終了を促すダイアログ ボックス](media/Uninstall_DRA_services.png)

## <a name="install-the-latest-document-routing-agent"></a><span data-ttu-id="a51d1-123">最新のドキュメント回覧エージェントのインストール</span><span class="sxs-lookup"><span data-stu-id="a51d1-123">Install the latest Document Routing Agent</span></span>
<span data-ttu-id="a51d1-124">定期売買で使用可能な最新の DRA をインストールする方法の詳細については、[ネットワーク プリンター デバイスを有効にするためにドキュメント回覧エージェントをインストールする](install-document-routing-agent.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a51d1-124">For information about how to install the latest DRA that is available with your subscription, see [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a51d1-125">アップグレード後に DRA クライアントを開いて、ネットワーク ユーザーの資格情報を更新してください。</span><span class="sxs-lookup"><span data-stu-id="a51d1-125">Be sure to open the DRA client after upgrading to refresh network user credentials.</span></span>

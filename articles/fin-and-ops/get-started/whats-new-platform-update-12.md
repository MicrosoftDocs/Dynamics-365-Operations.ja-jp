---
title: Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 の新機能または変更された機能について説明します。 このバージョンは 2017 年 11 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: e577d51d-42d2-47c5-b388-93c8219c692a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 134152790a55fd5e5b21d683b034eeab6be9291b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547997"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-12-november-2017"></a><span data-ttu-id="85586-104">Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="85586-104">What's new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 12 (November 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85586-105">このトピックでは、Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="85586-105">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 12.</span></span> <span data-ttu-id="85586-106">このバージョンは 2017 年 11 月にリリースされ、ビルド番号は 7.0.4709 です。</span><span class="sxs-lookup"><span data-stu-id="85586-106">This version was released in November 2017 and has a build number of 7.0.4709.</span></span>

<span data-ttu-id="85586-107">新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85586-107">Go to the [Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to find supplemental information about new features and learn more about what new features are in development.</span></span> <span data-ttu-id="85586-108">プラットフォーム更新プログラム 12 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=863949) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85586-108">For information about the bug fixes included in Platform update 12, log in to Lifecycle Services (LCS) and view this [KB article](https://go.microsoft.com/fwlink/?linkid=863949).</span></span>

## <a name="browser-client--discover-and-learn-currently-available-keyboard-shortcuts"></a><span data-ttu-id="85586-109">ブラウザー クライアント - 現在利用可能なキーボード ショートカットを見つけて学ぶ</span><span class="sxs-lookup"><span data-stu-id="85586-109">Browser client – Discover and learn currently available keyboard shortcuts</span></span>

<span data-ttu-id="85586-110">キーボード ショートカットの説明書を検索する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="85586-110">You no longer need to search through documentation to learn keyboard shortcuts.</span></span> <span data-ttu-id="85586-111">代わりに、ユーザー インターフェイスから直接、現在利用可能なキーボード ショートカットを見つけることができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="85586-111">Instead, you can now discover currently available keyboard shortcuts directly from the user interface.</span></span> <span data-ttu-id="85586-112">コントロールを右クリックし、**ショートカットの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="85586-112">Simply right-click on a control and select **View shortcuts**.</span></span> <span data-ttu-id="85586-113">これにより、ページの場所に応じて使用できるショートカットが一覧表示されたダイアログボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="85586-113">This will open a dialog box listing the shortcuts that you can use based on where you are on the page.</span></span> 

<span data-ttu-id="85586-114">詳細については、「[キーボード ショートカット](shortcut-keys.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85586-114">For more information, see [Keyboard shortcuts](shortcut-keys.md).</span></span>

## <a name="development-and-build-environments-in-a-customer-lcs-implementation-project-are-monitored-and-managed-by-microsoft"></a><span data-ttu-id="85586-115">顧客の LCS 実装プロジェクトの開発環境とビルド環境は、Microsoft によって監視および管理されています。</span><span class="sxs-lookup"><span data-stu-id="85586-115">Development and build environments in a customer LCS implementation project are monitored and managed by Microsoft</span></span>

<span data-ttu-id="85586-116">お客様が Finance and Operations の運用または実装を行っている顧客の場合、開発、テスト、および運用を有効にする環境のセットが提供されます。</span><span class="sxs-lookup"><span data-stu-id="85586-116">If you're a customer operating or implementing Finance and Operations, you are provided with a set of environments to enable development, testing, and production.</span></span> <span data-ttu-id="85586-117">サンドボックス (階層 2) と実稼働環境は、Microsoft によって管理されていますが、IT スタッフが開発者とビルド環境の管理を担当します。</span><span class="sxs-lookup"><span data-stu-id="85586-117">Sandbox (Tier-2) and production environments are managed by Microsoft, while your IT staff is responsible for managing developer and build environments.</span></span> <span data-ttu-id="85586-118">この機能では、開発者および開発者環境およびビルド環境を含む、Microsoft サブスクリプションで実行中の Lifecycle Services (LCS) 実装プロジェクト内のすべての環境が、Microsoft によりモニターおよび管理されます。</span><span class="sxs-lookup"><span data-stu-id="85586-118">With this feature, all environments in a Lifecycle Services (LCS) implementation project that are running in the Microsoft subscription, including developer and build environments, are monitored and managed by Microsoft.</span></span> <span data-ttu-id="85586-119">これにより、IT スタッフは、セキュリティ パッチの適用やこれらの環境への更新など、セキュリティの監視と管理を行う必要がなくなります。</span><span class="sxs-lookup"><span data-stu-id="85586-119">This relieves your IT staff from having to monitor and manage security, including applying security patches and updates for these environments.</span></span> <span data-ttu-id="85586-120">これは、オンプレミスまたは顧客またはパートナーの Microsoft Azure サブスクリプションで実行される開発環境およびビルド環境には影響しません。</span><span class="sxs-lookup"><span data-stu-id="85586-120">This does not affect development and build environments running on-premises or in the customer's or partner's own Microsoft Azure subscription.</span></span>

<span data-ttu-id="85586-121">開発者が実行する開発およびアプリケーション管理タスクは、開発仮想マシン (VM) のローカル管理者権限を必要とせずに実行できます。</span><span class="sxs-lookup"><span data-stu-id="85586-121">Development and application management tasks performed by developers can be done without requiring local administrator rights on the development virtual machine (VM).</span></span> <span data-ttu-id="85586-122">顧客は、Microsoft のサブスクリプションで実行されている開発環境およびビルド環境の VM 管理者アカウントにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="85586-122">Customers will not have access to the VM admin account of development and build environments running in the Microsoft subscription.</span></span>

<span data-ttu-id="85586-123">詳細については、この LCS ブログ トピック、[制限された管理者のアクセス](https://blogs.msdn.microsoft.com/lcs/2017/10/31/restricted-admin-access-with-platform-12-updates/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85586-123">For more information, refer to this LCS blog topic, [Restricted Admin Access](https://blogs.msdn.microsoft.com/lcs/2017/10/31/restricted-admin-access-with-platform-12-updates/).</span></span>

## <a name="enabling-sql-triggers-in-bring-your-own-database-byod"></a><span data-ttu-id="85586-124">「独自のデータベースを戻す」 (BYOD) で、SQL トリガーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="85586-124">Enabling SQL triggers in 'bring your own database' (BYOD)</span></span>

<span data-ttu-id="85586-125">BYOD とも呼ばれる「自分のデータベースの持ち込み」機能により Dynamics 365 for Finance and Operations から 独自の SQL Azure データベースに段階的にデータ エンティティをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="85586-125">The 'bring your own database' feature, also called BYOD, enables incrementally exporting data entities from Dynamics 365 for Finance and Operations into your own SQL Azure database.</span></span> <span data-ttu-id="85586-126">現時点で、出力先データベースに SQL データベース トリガーがある場合、BYOD プロセスは効率的なバルク データ転送を有効にするためにトリガーをバイパスします。</span><span class="sxs-lookup"><span data-stu-id="85586-126">If your destination database contains SQL database triggers, at present, the BYOD process bypasses triggers to enable efficient bulk data transfer.</span></span>

<span data-ttu-id="85586-127">エクスポートされたデータまたは BYOD のために、独自のデータベースで SQL データベース トリガーを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="85586-127">You can now use SQL database triggers in your own database, for data that is exported or BYOD.</span></span> <span data-ttu-id="85586-128">これにより、下流のプロセスが BYOD プロセスと容易に統合できるようになります。</span><span class="sxs-lookup"><span data-stu-id="85586-128">This allows for downstream processes to easily integrate with the BYOD processes.</span></span>

## <a name="export-b2b-users-to-azure-ad"></a><span data-ttu-id="85586-129">B2B ユーザーの Azure AD へのエクスポート</span><span class="sxs-lookup"><span data-stu-id="85586-129">Export B2B users to Azure AD</span></span>

<span data-ttu-id="85586-130">企業間 (B2B) ユーザーを Azure Active Directory (Azure AD) に自動的にエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="85586-130">You can automatically export business-to-business (B2B) users to Azure Active Directory (Azure AD).</span></span>

<span data-ttu-id="85586-131">過去には、B2B ユーザーは .csv ファイルに手動でエクスポートされていました。</span><span class="sxs-lookup"><span data-stu-id="85586-131">In the past, B2B users were exported manually to a .csv file.</span></span> <span data-ttu-id="85586-132">その後、Azure AD テナントの管理者は、このファイルを使用して Azure ポータルを使用してユーザーを Azure AD に手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85586-132">Then the Azure AD tenant administrator had to use this file to manually add the users to Azure AD using the Azure portal.</span></span>

<span data-ttu-id="85586-133">自動エクスポート機能を有効にするには、ワンタイム設定と構成プロセスを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85586-133">To enable the automatic export feature, a one-time setup and configuration process must be completed.</span></span> <span data-ttu-id="85586-134">このプロセスが完了したら、新しいユーザーのプロビジョニング ワークフロー タスクを使用して、Azure AD に B2B ユーザーを自動的にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="85586-134">When the process is completed, you can use the Provision new user workflow task to automatically export B2B users to Azure AD.</span></span>

<span data-ttu-id="85586-135">1回限りの設定とコンフィギュレーションでは、次のことが必要になります。</span><span class="sxs-lookup"><span data-stu-id="85586-135">The one-time set up and configuration means that you'll need to:</span></span>

- <span data-ttu-id="85586-136">Azure AD で B2B 招待サービス アプリケーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="85586-136">Set up a B2B invitation service application in Azure AD.</span></span>
- <span data-ttu-id="85586-137">Finance and Operations で B2B 招待サービスの設定のコンフィギュレーションをします。</span><span class="sxs-lookup"><span data-stu-id="85586-137">Configure the B2B invitation service settings in Finance and Operations.</span></span>

<span data-ttu-id="85586-138">詳細については、[Azure AD に B2B ユーザーをエクスポート](../../dev-itpro/sysadmin/implement-b2b.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85586-138">For more information, see [Export B2B users to Azure AD](../../dev-itpro/sysadmin/implement-b2b.md).</span></span>

## <a name="personalizations-can-easily-be-shared-with-one-or-more-roles-in-your-organization"></a><span data-ttu-id="85586-139">個人用設定は、組織の 1 つまたは複数の役割と簡単に共有できます。</span><span class="sxs-lookup"><span data-stu-id="85586-139">Personalizations can easily be shared with one or more roles in your organization</span></span>

<span data-ttu-id="85586-140">個人用設定機能では、ラベルの名前を変更する、コントロールを追加、移動、非表示にする、サイズを変更する、アプリケーション全体のフォームでグリッド列を追加または並べ替えるなど、ユーザー インターフェイスに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="85586-140">Personalization capabilities enable a user to make changes to the user interface, such as renaming labels, adding, moving or hiding controls, resizing, adding or re-ordering grid columns on forms across the application.</span></span> <span data-ttu-id="85586-141">個人用設定では、エンド ユーザーが、アプリケーション内と Power BI のコンテンツを示す新しいワークスペースを作成することが可能です。</span><span class="sxs-lookup"><span data-stu-id="85586-141">Personalization also makes it possible for an end user to create new workspaces showing content from within the application as well as from Power BI.</span></span> <span data-ttu-id="85586-142">これらの機能により、アプリケーションのカスタマイズを行う必要性が減り、代わりにユーザーが必要なユーザー インターフェイスを最初から作成したり、既製のコンテンツを修正して作成することができます。</span><span class="sxs-lookup"><span data-stu-id="85586-142">These features reduce the need to make customizations to the application and instead allow a user to potentially create the required user interface, either starting from scratch or by modifying ready-made content.</span></span>

<span data-ttu-id="85586-143">管理者は、ユーザーが行った個人用設定をエクスポートする機能を既に持っており、インポート プロセスを使用して組織内のロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="85586-143">Administrators already have the ability to export a personalization done by a user and apply that to other users or roles within the organization through an import process.</span></span> <span data-ttu-id="85586-144">パーソナル化をインポートすることなく、管理者がパーソナル化管理フォームからパーソナル化を他のユーザーと共有できるようにすることで簡素化されます。</span><span class="sxs-lookup"><span data-stu-id="85586-144">This will be simplified by allowing an administrator to share personalizations with others from the personalization administration form, without having to import the personalization.</span></span>

<span data-ttu-id="85586-145">また、この機能により、管理者は個人用設定を適用する方法をより細かく制御できます。</span><span class="sxs-lookup"><span data-stu-id="85586-145">Additionally, this feature gives the administrator more control over how to apply a personalization.</span></span> <span data-ttu-id="85586-146">既存の個人用設定を置き換えるのではなく、管理者は任意で既存の個人用設定に新しい個人用設定を追加することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="85586-146">Instead of replacing existing personalizations, an administrator can optionally choose to add the new personalizations to any existing ones.</span></span>

## <a name="reporting-document-routing-agent-scale-improvements"></a><span data-ttu-id="85586-147">レポート: ドキュメント回覧エージェントのスケールの強化</span><span class="sxs-lookup"><span data-stu-id="85586-147">Reporting: Document Routing Agent scale improvements</span></span>

<span data-ttu-id="85586-148">ドキュメント回覧エージェントは、さらにネットワーク プリンター デバイスをサポートできるように拡張されています。</span><span class="sxs-lookup"><span data-stu-id="85586-148">The Document Routing Agent has been enhanced to offer support for more network printer devices.</span></span> <span data-ttu-id="85586-149">最大 50 のネットワーク プリンターをサポートする機能により、クライアントは一般的な印刷作業負荷を処理するための準備ができています。</span><span class="sxs-lookup"><span data-stu-id="85586-149">With the ability to support up to 50 network printers, clients are better prepared to handle common printing workloads.</span></span> <span data-ttu-id="85586-150">インテリジェントなドキュメント キュー管理を活用する最新のプラットフォーム更新プログラムを展開した後、ドキュメント回覧エージェントをアップグレードするだけです。</span><span class="sxs-lookup"><span data-stu-id="85586-150">Simply upgrade the Document Routing Agent after deploying the latest platform update to take advantage of the intelligent document queue management.</span></span>

> [!NOTE]
> <span data-ttu-id="85586-151">最新バージョンのドキュメント ルーティング エージェントを、会社のドメインでホストされているローカルのプリント サーバーに配置するには、次のインストールの指示を参照してください。[プリンター デバイスを有効にするためにドキュメント ルーティング エージェントをインストールする](../../dev-itpro/analytics/install-document-routing-agent.md)。</span><span class="sxs-lookup"><span data-stu-id="85586-151">Refer to the following installation instructions to deploy the latest version of the Document Routing Agent onto local print servers hosted on the corporate domain, [Install the Document Routing Agent to enable network printer devices](../../dev-itpro/analytics/install-document-routing-agent.md).</span></span>

## <a name="table-extension--previewpartref-property"></a><span data-ttu-id="85586-152">テーブル拡張 - PreviewPartRef プロパティ</span><span class="sxs-lookup"><span data-stu-id="85586-152">Table extension – PreviewPartRef property</span></span>

<span data-ttu-id="85586-153">このリリースには、テーブル拡張を介して **PreviewPartRef** プロパティの値を変更する機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="85586-153">This release includes the ability to change the value of the **PreviewPartRef** property via a table extension.</span></span> <span data-ttu-id="85586-154">この機能を使用すると、TMSRoute のプレビューの強化など、既存へのプレビューを強化できます。</span><span class="sxs-lookup"><span data-stu-id="85586-154">This feature provides an enhanced preview to existing fields, such as an enhanced preview for TMSRoute.</span></span>

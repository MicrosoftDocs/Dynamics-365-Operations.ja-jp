---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 6 (2017 年 4 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 6 の新機能または変更された機能について説明します。 このバージョンは 2017 年 4 月にリリースされ、ビルド番号は 7.0.4509.16180 です。
author: tonyafehr
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.assetid: 13d2b8a5-c2e0-4f32-a43b-7726ae20392c
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: ''
ms.dyn365.ops.version: Platform update 6
ms.openlocfilehash: b998298fee72ec545df579b564a99d4b7e229d17
ms.sourcegitcommit: 4d6ec2b1a9674712e1efb8c46b919d554f21a2b3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2019
ms.locfileid: "2627567"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-6-april-2017"></a><span data-ttu-id="5802e-104">Dynamics 365 for Operations プラットフォーム更新プログラム 6 (2017 年 4 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="5802e-104">What's new or changed in Dynamics 365 for Operations platform update 6 (April 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5802e-105">このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 6 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="5802e-105">This topic describes features that are either new or changed in Dynamics 365 for Operations platform update 6.</span></span> <span data-ttu-id="5802e-106">このバージョンは 2017 年 4 月にリリースされ、ビルド番号は 7.0.4509.16180 です。</span><span class="sxs-lookup"><span data-stu-id="5802e-106">This version was released in April 2017 and has a build number of 7.0.4509.16180.</span></span>

## <a name="browser-framework--powerapps-host-control"></a><span data-ttu-id="5802e-107">ブラウザー フレームワーク – PowerApps ホスト コントロール</span><span class="sxs-lookup"><span data-stu-id="5802e-107">Browser framework – PowerApps Host control</span></span>

<span data-ttu-id="5802e-108">Dynamics 365 for Operations は、開発者に対して新しいコントロールである PowerApps ホスト コントロールを導入します。</span><span class="sxs-lookup"><span data-stu-id="5802e-108">Dynamics 365 for Operations introduces a new control for developers, the PowerApps Host control.</span></span> <span data-ttu-id="5802e-109">このコントロールにより、開発者は Dynamics 365 for Operations フォーム内で PowerApp をホストまたは埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="5802e-109">This control allows a developer to host or embed a PowerApp within a Dynamics 365 for Operations form.</span></span> <span data-ttu-id="5802e-110">詳細については、[PowerApps ホスト コントロール](../../dev-itpro/user-interface/powerapps-host-control.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5802e-110">For more details, see [PowerApps Host control](../../dev-itpro/user-interface/powerapps-host-control.md).</span></span>

## <a name="browser-client--ability-to-model-toolbar-actions-in-the-overflow-menu"></a><span data-ttu-id="5802e-111">ブラウザー クライアント - オーバーフロー メニューのツール バー アクションをモデル化する機能</span><span class="sxs-lookup"><span data-stu-id="5802e-111">Browser client – Ability to model toolbar actions in the overflow menu</span></span>

<span data-ttu-id="5802e-112">ツールバー内の特定のボタンを常にオーバーフローで表示するように設計することで、フォーム上に簡潔なアクション ストーリーを提供することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5802e-112">You can now provide a cleaner action story on forms by designating certain buttons in toolbars to always render in overflow.</span></span> <span data-ttu-id="5802e-113">これにより、ユーザーが頻繁に使用する操作と、まれにしか使用されない操作とを区別することが容易になります。</span><span class="sxs-lookup"><span data-stu-id="5802e-113">This makes it easier to differentiate actions that users will commonly use versus those that are infrequently or rarely used.</span></span> <span data-ttu-id="5802e-114">この機能を利用するには、ツールバー内にあるボタン グループの新しい **AlwaysInOverflow** メタデータ プロパティを試してください。</span><span class="sxs-lookup"><span data-stu-id="5802e-114">To utilize this feature, try the new **AlwaysInOverflow** metadata property on Button groups inside Toolbars.</span></span>

## <a name="build-automation--automatic-update-of-model-version-during-build"></a><span data-ttu-id="5802e-115">ビルド自動化 - ビルド中のモデル バージョンの自動更新</span><span class="sxs-lookup"><span data-stu-id="5802e-115">Build automation – Automatic update of model version during build</span></span>

<span data-ttu-id="5802e-116">自動ビルド中に、ビルド中のモデルのバージョンが更新され、ビルド番号が反映されます。</span><span class="sxs-lookup"><span data-stu-id="5802e-116">During an automated build, versions of models that are being built are updated to reflect the build number.</span></span> <span data-ttu-id="5802e-117">これにより、お客様は、Azure DevOps のビルド履歴に戻り、Dynamics 365 for Operations ウィンドウのモデル バージョンをトレースできます。</span><span class="sxs-lookup"><span data-stu-id="5802e-117">This allows customers the ability to trace the model versions in the Dynamics 365 for Operations About window back to the build history in Azure DevOps.</span></span>

## <a name="build-automation--option-to-include-runtime-packages-in-the-deployable-package-of-the-automated-build-output"></a><span data-ttu-id="5802e-118">ビルド自動化 - 自動ビルド出力の配置可能パッケージにランタイム パッケージを含めるオプション</span><span class="sxs-lookup"><span data-stu-id="5802e-118">Build automation – Option to include runtime packages in the deployable package of the automated build output</span></span>

<span data-ttu-id="5802e-119">ビルド定義の新しいオプションでは、自動ビルドに指示を出して、ビルド出力用に生成された配置可能なパッケージのすべてのソース管理ランタイム パッケージを含めるようにします。</span><span class="sxs-lookup"><span data-stu-id="5802e-119">A new option in the build definition instructs the automated build to include any source-controlled runtime packages in the deployable package that is generated for the build output.</span></span> <span data-ttu-id="5802e-120">これにより、お客様は、カスタム コードと ISV などのサード パーティが提供するランタイム パッケージの両方が含まれる、自動ビルドによって生成された 1 つのパッケージを展開できます。</span><span class="sxs-lookup"><span data-stu-id="5802e-120">This allows customers to deploy one package, generated by the automated build, that includes both custom code as well as runtime packages supplied by third parties, such as ISVs.</span></span>

## <a name="document-management--attachment-storage-cleanup"></a><span data-ttu-id="5802e-121">ドキュメント管理 - ストレージ クリーンアップの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="5802e-121">Document management – Attachment storage cleanup</span></span>

<span data-ttu-id="5802e-122">Dynamics AX 7.0 がリリースされたとき、添付ファイル用のデータベースの記憶領域が使用されなくなりました。ただし、移行する必要のあるプラットフォーム機能が一部残っています。</span><span class="sxs-lookup"><span data-stu-id="5802e-122">When Dynamics AX 7.0 was released, the database storage for attachments was deprecated; however, some platform functionality remained that needed to be migrated.</span></span> <span data-ttu-id="5802e-123">Dynamics 365 for Operations プラットフォーム更新プログラム 6 では、最後に残ったプラットフォーム使用状況が削除され、移行ボタンが**ドキュメント管理パラメーター** フォームに追加されました。</span><span class="sxs-lookup"><span data-stu-id="5802e-123">In Dynamics 365 for Operations platform update 6, the last remaining platform usage was removed and a migration button was added to the **Document Management Parameters** form.</span></span> <span data-ttu-id="5802e-124">移行ボタンを使用して、アップグレード後にデータベースに残っている可能性のあるファイルをクリーンアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="5802e-124">The migration button can be used to clean up any files that might remain in the database after an upgrade.</span></span> <span data-ttu-id="5802e-125">移行により、データベースに格納されている添付ファイルが BLOB ストレージに移行されます。</span><span class="sxs-lookup"><span data-stu-id="5802e-125">The migration will migrate any attachments stored in the database to Blob storage.</span></span> <span data-ttu-id="5802e-126">詳細については、[最新のプラットフォーム更新プログラムにアップグレード](../../dev-itpro/migration-upgrade/upgrade-latest-platform-update.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5802e-126">For more information, see [Upgrade to the latest platform update](../../dev-itpro/migration-upgrade/upgrade-latest-platform-update.md).</span></span>

## <a name="number-sequence-scope-extensibility"></a><span data-ttu-id="5802e-127">番号順序スコープの拡張性</span><span class="sxs-lookup"><span data-stu-id="5802e-127">Number sequence scope extensibility</span></span>

<span data-ttu-id="5802e-128">拡張機能を通じて番号シーケンス スコープを拡張することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5802e-128">You can now extend the number sequence scope through extensions.</span></span> <span data-ttu-id="5802e-129">数字シーケンスの範囲は、数字シーケンスを使用する組織を定義します。</span><span class="sxs-lookup"><span data-stu-id="5802e-129">The scope of a number sequence defines which organization uses the number sequence.</span></span> <span data-ttu-id="5802e-130">スコープを会計年度期間と組み合わせて、さらに特定の数値シーケンスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="5802e-130">The scope can be combined with fiscal calendar periods to create even more specific number sequences.</span></span> <span data-ttu-id="5802e-131">詳細については、「[番号順序スコープの拡張](../../dev-itpro/extensibility/extend-number-sequence-scope.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5802e-131">For more information, see [Extend the number sequence scope](../../dev-itpro/extensibility/extend-number-sequence-scope.md).</span></span>

## <a name="mobile"></a><span data-ttu-id="5802e-132">携帯電話</span><span class="sxs-lookup"><span data-stu-id="5802e-132">Mobile</span></span>

- <span data-ttu-id="5802e-133">異なるユーザー グループに対してワークスペースの表示を設定する機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="5802e-133">Added the ability to set workspace visibility for different user groups.</span></span>

    - <span data-ttu-id="5802e-134">モバイル ユーザーに、Web クライアントで基になるフォームにアクセスできないページは表示されません。</span><span class="sxs-lookup"><span data-stu-id="5802e-134">Mobile users will not see pages that they do not have access to in the underlying form in the web client.</span></span> <span data-ttu-id="5802e-135">プラットフォーム更新プログラム 6 より前に、いずれかのページにアクセスできない場合は空のモバイル ワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5802e-135">Before Platform update 6, users could see empty mobile workspaces if they did not have access to any of the pages.</span></span> <span data-ttu-id="5802e-136">また、ユーザーのグループに対してワークスペース全体の表示を変更することができません。</span><span class="sxs-lookup"><span data-stu-id="5802e-136">Also, the visibility of an entire workspace for a group of users could not be modified.</span></span>
    - <span data-ttu-id="5802e-137">新しいセキュリティ属性と API が導入され、メニュー項目に基づいたモバイル ワークスペースの表示を宣言しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="5802e-137">New security attributes and APIs are introduced, making it easy to declare visibility of a mobile workspace based on menu items.</span></span> <span data-ttu-id="5802e-138">これらの API を使用して、特定のユーザー グループのモバイル ワークスペースへのアクセスを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="5802e-138">These APIs can be used to override mobile workspace access for specific user groups.</span></span>

- <span data-ttu-id="5802e-139">必要な属性を自動検出する機能が追加され、フォームとテーブル メタデータを使用して、データの入力中に必須としてモバイル フィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="5802e-139">Added the ability to auto detect required attributes, through form and table metadata, to denote mobile fields as mandatory during data entry.</span></span> <span data-ttu-id="5802e-140">アクション データは、必要なフィールドの値が指定されない場合、サーバーに送信することはできません。</span><span class="sxs-lookup"><span data-stu-id="5802e-140">Action data cannot be submitted to the server if values for the required fields are not provided.</span></span> <span data-ttu-id="5802e-141">(要求: プラットフォーム更新プログラム 6 とモバイルの 4 月リリース。)</span><span class="sxs-lookup"><span data-stu-id="5802e-141">(Requirement: Platform update 6 and Mobile April release.)</span></span>
- <span data-ttu-id="5802e-142">Dynamics 365 for Operations がサポートするすべての言語のモバイル ワークスペースを完全にローカライズするためのオプション。</span><span class="sxs-lookup"><span data-stu-id="5802e-142">Option to fully localize mobile workspaces for all Dynamics 365 for Operations supported languages.</span></span>

## <a name="ideas-portal"></a><span data-ttu-id="5802e-143">アイデア ポータル</span><span class="sxs-lookup"><span data-stu-id="5802e-143">Ideas portal</span></span>

<span data-ttu-id="5802e-144">Dynamics 365 for Operations アイデア フォーラムは、 [アイデア ポータル](https://experience.dynamics.com/ideas/) にて使用可能となっています。</span><span class="sxs-lookup"><span data-stu-id="5802e-144">Dynamics 365 for Operations Ideas forum is now available on our [Ideas portal](https://experience.dynamics.com/ideas/).</span></span> <span data-ttu-id="5802e-145">アイデア ポータルでは、すべての Dynamics 365 for Operations ユーザーは、定期的に新しいアイデアを送信、既存のアイデアを採決、およびそのアイデアの状態を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="5802e-145">With the Ideas portal, all Dynamics 365 for Operations users can submit new ideas, vote on existing ideas, and track status of their ideas in a consistent manner.</span></span> <span data-ttu-id="5802e-146">これは、現在、製品の外部 ([https://experience.dynamics.com/ideas](https://experience.dynamics.com/ideas/)) およびアプリケーション内の両方から達成できます。</span><span class="sxs-lookup"><span data-stu-id="5802e-146">This can now be achieved from both outside of the product ([https://experience.dynamics.com/ideas](https://experience.dynamics.com/ideas/)) and from within the application.</span></span> <span data-ttu-id="5802e-147">このスクリーンショットは、Dynamics 365 for Operations からアイデア ポータルにナビゲートする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5802e-147">The screenshot shows how to navigate to the Ideas portal from within Dynamics 365 for Operations.</span></span>

<span data-ttu-id="5802e-148">[![ideas-menu](./media/ideas-menu.png)](./media/ideas-menu.png)</span><span class="sxs-lookup"><span data-stu-id="5802e-148">[![ideas-menu](./media/ideas-menu.png)](./media/ideas-menu.png)</span></span>

<span data-ttu-id="5802e-149">Dynamics 365 for Operations フォーラムに移動するには**アイデア**のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5802e-149">Click the **Ideas** link to go to the Dynamics 365 for Operations forum.</span></span>



- <span data-ttu-id="5802e-150">フォーラムには既存のアイデアがあらかじめ設定されているため、顧客やパートナーはすぐに新しいアイデアを投票したり提案したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="5802e-150">The forums are pre-populated with existing ideas, so customers and partners can immediately vote or suggest new ideas.</span></span>
- <span data-ttu-id="5802e-151">状態および時間を使用してアイデアをフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="5802e-151">You can filter ideas by using status and time.</span></span> <span data-ttu-id="5802e-152">上位のアイデア、話題のアイデア、および新しいアイデアを素早く表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="5802e-152">You can also quickly view top, hot, and new ideas.</span></span>
- <span data-ttu-id="5802e-153">特定のアイデアにアップ投票またはダウン投票することができます (アイデアごとに 1 票)。</span><span class="sxs-lookup"><span data-stu-id="5802e-153">You can either vote up or down on a specific idea (one vote per idea).</span></span> <span data-ttu-id="5802e-154">新しいアイディアを投票したり提案したりするには、Microsoft アカウントを使用してサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5802e-154">To vote or suggest a new idea, you need to sign in using a Microsoft account.</span></span>
- <span data-ttu-id="5802e-155">**個人用フィードバック** 機能を使用すると、提出された提案、提案のステータス、受け取った合計投票数の詳細なビューを表示できます。</span><span class="sxs-lookup"><span data-stu-id="5802e-155">The **My Feedback** feature allows you to see a detailed view of your submitted ideas, the status of your ideas, and the total votes received.</span></span>

<span data-ttu-id="5802e-156">[![ideas-options](./media/ideas-options.png)](./media/ideas-options.png)</span><span class="sxs-lookup"><span data-stu-id="5802e-156">[![ideas-options](./media/ideas-options.png)](./media/ideas-options.png)</span></span>

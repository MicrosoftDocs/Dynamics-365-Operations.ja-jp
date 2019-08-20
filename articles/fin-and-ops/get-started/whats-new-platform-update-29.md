---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 (2019 年 10 月) の機能をプレビューする
description: このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 でプレビューされる機能について説明します。
author: tonyafehr
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: Platform update 29
ms.openlocfilehash: 3207dac83eb68c01d67eb62166fab20916ecf7f5
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863647"
---
# <a name="preview-features-in-dynamics-365-for-finance-and-operations-platform-update-29-october-2019"></a><span data-ttu-id="16a21-103">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 (2019 年 10 月) の機能をプレビューする</span><span class="sxs-lookup"><span data-stu-id="16a21-103">Preview features in Dynamics 365 for Finance and Operations platform update 29 (October 2019)</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="16a21-104">このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 29 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="16a21-104">This topic describes features that are new or changed in Dynamics 365 for Finance and Operations platform update 29.</span></span> <span data-ttu-id="16a21-105">このバージョンのビルド番号は 7.0.5372 です。</span><span class="sxs-lookup"><span data-stu-id="16a21-105">This version has a build number of 7.0.5372.</span></span> <span data-ttu-id="16a21-106">一般提供開始日は 10 月ですが、新機能は 8 月の初期リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="16a21-106">While the general availability date is in October, the new features are available for early release in August.</span></span> <span data-ttu-id="16a21-107">プラットフォーム更新プログラム 29 の詳細については [追加リソース](whats-new-platform-update-28.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-107">For more information about Platform update 29, see [Additional resources](whats-new-platform-update-28.md#additional-resources).</span></span>


## <a name="feature-management"></a><span data-ttu-id="16a21-108">機能管理</span><span class="sxs-lookup"><span data-stu-id="16a21-108">Feature management</span></span>
<span data-ttu-id="16a21-109">機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="16a21-109">The Feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="16a21-110">プラットフォーム更新プログラム29には、次のような追加機能が追加されています:</span><span class="sxs-lookup"><span data-stu-id="16a21-110">In Platform update 29, additional features have been added, including:</span></span>
- <span data-ttu-id="16a21-111">有効になっていないすべての機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="16a21-111">Enable all features that are not enabled.</span></span>
- <span data-ttu-id="16a21-112">更新後にすべての機能を自動的に有効にします。</span><span class="sxs-lookup"><span data-stu-id="16a21-112">Automatically enable all features after an update.</span></span>
- <span data-ttu-id="16a21-113">既存のコンフィギュレーション キーが有効になっているなど、条件に基づいて機能を有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="16a21-113">Do not allow a feature to be enabled based on a condition, such as an existing config key is turned on.</span></span>
- <span data-ttu-id="16a21-114">新しい機能を手動で検索して、機能の一覧に追加する **更新の確認** というボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="16a21-114">Add a button called **Check for updates** that manually searches for new features and adds them to the list of features.</span></span>

<span data-ttu-id="16a21-115">詳細については [機能管理の概要](feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-115">For more information, see [Feature management overview](feature-management/feature-management-overview.md).</span></span>

## <a name="data-management-job-history-clean-up"></a><span data-ttu-id="16a21-116">データ管理ジョブ履歴のクリーンアップ</span><span class="sxs-lookup"><span data-stu-id="16a21-116">Data management job history clean up</span></span>
<span data-ttu-id="16a21-117">実行履歴の定期的なクリーンアップをスケジュールするには、データ管理の [ジョブ履歴クリーンアップ機能](../../dev-itpro/data-entities/data-import-export-job.md#job-history-clean-up-available-in-platform-update-29-and-later) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="16a21-117">[Job history clean-up functionality](../../dev-itpro/data-entities/data-import-export-job.md#job-history-clean-up-available-in-platform-update-29-and-later) in Data management must be used to schedule a periodic cleanup of the execution history.</span></span> <span data-ttu-id="16a21-118">この機能は、現在は推奨されていない既存のステージング テーブルのクリーンアップ機能を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="16a21-118">This functionality replaces the existing staging table clean-up functionality, which is now deprecated.</span></span>

## <a name="business-events-catalog-security"></a><span data-ttu-id="16a21-119">ビジネス イベント カタログのセキュリティ</span><span class="sxs-lookup"><span data-stu-id="16a21-119">Business events catalog security</span></span>
<span data-ttu-id="16a21-120">[ロールベース セキュリティ](../../dev-itpro/business-events/home-page.md#role-based-security-for-business-events) は、ビジネス イベント カタログの個々のビジネス イベントに適用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16a21-120">[Role-based security](../../dev-itpro/business-events/home-page.md#role-based-security-for-business-events) can be now applied to individual business events in the business event catalog.</span></span> <span data-ttu-id="16a21-121">このセキュリティを有効にしてコンフィギュレーションすると、ユーザーは、ロールがアクセス権を持つビジネス イベントのみを表示したり、購読したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="16a21-121">When this security is enabled and configured, users will be able to only view and subscribe to business events to which their roles have access.</span></span> <span data-ttu-id="16a21-122">このセキュリティは、 Microsoft Flow などの統合シナリオにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="16a21-122">This security also applies to integration scenarios, such as Microsoft Flow.</span></span>

## <a name="attachment-recovery"></a><span data-ttu-id="16a21-123">添付ファイルの回復</span><span class="sxs-lookup"><span data-stu-id="16a21-123">Attachment recovery</span></span>
<span data-ttu-id="16a21-124">レコード 添付ファイルのごみ箱を提供する添付ファイルの回復機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="16a21-124">An attachment recovery feature has been added that provides a recycle bin for record attachments.</span></span> <span data-ttu-id="16a21-125">削除後の設定された期間、ユーザーおよび管理者は、新しく削除された添付ファイルフォームを使用して、削除された添付ファイルを回復できます。</span><span class="sxs-lookup"><span data-stu-id="16a21-125">For a configured period of time after deletion, users and administrators can recover deleted attachments using the new deleted attachments forms.</span></span> <span data-ttu-id="16a21-126">詳細については、以下 [ドキュメント管理のコンフィギュレーション](../../fin-and-ops/organization-administration/configure-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-126">For details, see [Configure document management](../../fin-and-ops/organization-administration/configure-document-management.md).</span></span>

## <a name="session-idle-timeout"></a><span data-ttu-id="16a21-127">セッション アイドル タイムアウト</span><span class="sxs-lookup"><span data-stu-id="16a21-127">Session idle timeout</span></span>
<span data-ttu-id="16a21-128">セッション アイドル タイムアウトは、セッションがタイムアウトして閉じるまでにユーザーが非アクティブになれる時間の長さを表します。</span><span class="sxs-lookup"><span data-stu-id="16a21-128">The session idle timeout is the amount of time a user can be inactive before the user's session times out and is closed.</span></span> <span data-ttu-id="16a21-129">プラットフォーム更新プログラム 29では、ユーザーインターフェイスに Web ブラウザー セッション タイムアウト設定が公開され、既定値が 60 分ではなく 30 分に最適化されています。</span><span class="sxs-lookup"><span data-stu-id="16a21-129">With Platform update 29, the web browser session timeout setting is exposed in the user interface and is optimized for a default value of 30 minutes instead of 60 minutes.</span></span> <span data-ttu-id="16a21-130">最大60分まで値を変更および設定できますが、システムに余分な負荷が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="16a21-130">You can still change and set the value up to 60 minutes, but that may cause an extra load on the system.</span></span> <span data-ttu-id="16a21-131">詳細については、 [セッション アイドル タイムアウトの設定](../../dev-itpro/sysadmin/session-idle-timeout.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-131">For more information, see [Set the session idle timeout](../../dev-itpro/sysadmin/session-idle-timeout.md).</span></span>

## <a name="visual-refresh-of-the-web-client-to-align-with-the-fluent-design-language"></a><span data-ttu-id="16a21-132">Fluent Design言語に合わせたWeb クライアントのビジュアル更新</span><span class="sxs-lookup"><span data-stu-id="16a21-132">Visual refresh of the web client to align with the Fluent design language</span></span>
<span data-ttu-id="16a21-133">Dynamics 365アプリ全体の取り組みの一環として、Web クライアントのビジュアル更新に向けて段階的に取り組んでおり、コントロールとページを Microsoft Fluent Design言語とより密接に連携させています。</span><span class="sxs-lookup"><span data-stu-id="16a21-133">As part of the Dynamics 365 app-wide effort, we are incrementally working toward a visual refresh of the web client to more closely align controls and pages with the Microsoft Fluent design language.</span></span> <span data-ttu-id="16a21-134">プラットフォーム 更新プログラム 29 には、変更の初期セットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="16a21-134">An initial set of changes are included in Platform update 29.</span></span> <span data-ttu-id="16a21-135">詳細については、リリース計画の [Fluent Design言語に合わせたWeb クライアントのビジュアル更新](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/visual-refresh-web-client-align-fluent-design-language) トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-135">For more information, see the [Visual refresh of the web client to align with the Fluent design language](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/visual-refresh-web-client-align-fluent-design-language) topic in the Release Plans.</span></span>

##  <a name="saved-views-preview"></a><span data-ttu-id="16a21-136">保存されたビュー (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="16a21-136">Saved views (Preview)</span></span>
<span data-ttu-id="16a21-137">保存されたビュープがプレビューで使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16a21-137">Saved views are now available in preview.</span></span> <span data-ttu-id="16a21-138">この機能は、個人用設定サブシステムの大幅な拡張機能であり、ユーザーは、ページごとに複数の名前を付けた個人用設定セットを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="16a21-138">This feature represents a significant enhancement to the personalization subsystem, and allows users to have multiple named sets of personalizations per page.</span></span> <span data-ttu-id="16a21-139">リストページでは、これらのビューにフィルターを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="16a21-139">For list pages, these views can also contain filters.</span></span> <span data-ttu-id="16a21-140">ビューはセキュリティ ロールに対して公開できるので、個人用設定の管理もビューを使用することで大幅に簡単になります。</span><span class="sxs-lookup"><span data-stu-id="16a21-140">Management of personalizations is also substantially easier with views, as views can be published to security roles.</span></span> <span data-ttu-id="16a21-141">開発者環境でこの機能を有効にする方法の詳細については、 [保存されたビュー](saved-views.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-141">For more information about how to enable this feature in a developer environment, see [Saved views](saved-views.md).</span></span> <span data-ttu-id="16a21-142">また、 [保存されたビューを十分に活用するフォームの作成](../../dev-itpro/user-interface/understanding-saved-views.md) トピックも参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-142">Also refer to the [Build forms that fully utilize saved views](../../dev-itpro/user-interface/understanding-saved-views.md) topic.</span></span> <span data-ttu-id="16a21-143">このプレビュー機能は、一般に使用可能になるまで進化し変更し続けることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-143">Note that this preview feature will continue to evolve and change until it becomes generally available.</span></span> 

## <a name="new-grid-control-preview"></a><span data-ttu-id="16a21-144">新しいグリッド コントロール (プレビュー)</span><span class="sxs-lookup"><span data-stu-id="16a21-144">New grid control (Preview)</span></span> 
<span data-ttu-id="16a21-145">[新しいグリッド コントロール](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/user-productivity-new-grid) がプレビューで使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16a21-145">The [new grid control](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/user-productivity-new-grid) is now available in preview.</span></span> <span data-ttu-id="16a21-146">この新しいグリッドは既存のグリッド コントロールに代わるものであり、より高速なレンダリング、よりスムーズなスクロール、グリッド内でのより簡単なナビゲーション、ドラッグ アンド ドロップによる列の並べ替えなどの機能を備えています。</span><span class="sxs-lookup"><span data-stu-id="16a21-146">This new grid serves as a replacement for the existing grid control and features faster rendering, smoother scrolling, easier navigation in the grid, and drag-and-drop column reordering.</span></span> <span data-ttu-id="16a21-147">新しいグリッドでは、フッターの表形式グリッドの数値列の下部に総計を表示することもできます。これは、列ヘッダーの右クリック コンテキスト メニューを使用して有効にできます。</span><span class="sxs-lookup"><span data-stu-id="16a21-147">The new grid also allows for grand totals at the bottom of numeric columns in tabular grids in a footer that can be enabled using the right-click context menu from column headers.</span></span> <span data-ttu-id="16a21-148">有効にすると、すべての表形式とリストのグリッドが自動的に新しいグリッドを使用するように切り替わります。ただし、非反応拡張コントロールを含むグリッドがページにある場合は、既存のグリッドコントロールがそのページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="16a21-148">Once enabled, all tabular and list grids will automatically switch to use the new grid, unless the page has a grid with a non-react extensible control, in which case the existing grid control will be used on that page.</span></span> <span data-ttu-id="16a21-149">このプレビュー機能は、一般に使用可能になるまで進化し変更し続けることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-149">Note that this preview feature will continue to evolve and change until it becomes generally available.</span></span>

<span data-ttu-id="16a21-150">新しいグリッドコントロールを試すには、開発者環境のURLに &debug=reactGridを追加します。</span><span class="sxs-lookup"><span data-stu-id="16a21-150">To try out the new grid control, simply add &debug=reactGrid into the URL of your developer environment.</span></span> <span data-ttu-id="16a21-151">フライティングによって、他の環境で機能が動作しなくなることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-151">Note that flighting will prevent the feature from being operational in other environments.</span></span>  

## <a name="workflow-work-item-notifications-in-the-action-center"></a><span data-ttu-id="16a21-152">アクション センターのワークフロー作業項目通知</span><span class="sxs-lookup"><span data-stu-id="16a21-152">Workflow work item notifications in the action center</span></span> 
<span data-ttu-id="16a21-153">ユーザー は、 **設定** > **ユーザー オプション** > **ワークフロー** > **通知** > **アクションセンターに通知を送信** に移動して、アクション センターで通知を受信することを選択できます。</span><span class="sxs-lookup"><span data-stu-id="16a21-153">Users can now opt-in to receive notifications in the Action Center by going to **Settings** > **User options** > **Workflow** > **Notifications** > **Send notifications to Action Center**.</span></span> <span data-ttu-id="16a21-154">有効にすると、ユーザーに割り当てられた新しい作業項目ごとに通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="16a21-154">When enabled, the user will receive a notification for each new work item that is assigned to them.</span></span>

## <a name="workflows-can-now-support-reset"></a><span data-ttu-id="16a21-155">ワークフローがリセットをサポートできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16a21-155">Workflows can now support reset</span></span>
<span data-ttu-id="16a21-156">ワークフローは、必要に応じて **WorkflowIRecallUnrecoverable** インターフェイスを実装することによって、ワークフロー履歴フォームからのリセットをサポートできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="16a21-156">Workflows can now support reset from the Workflow History form by optionally implementing the **WorkflowIRecallUnrecoverable** interface.</span></span> <span data-ttu-id="16a21-157">仕入先請求書ワークフローでは、このインターフェイスを使用して、修復できない仕入先請求書ワークフローを取り消して、キャンセル済の状態にすることができます。</span><span class="sxs-lookup"><span data-stu-id="16a21-157">The vendor invoice workflow has used this interface to allow unrecoverable vendor invoice workflows to be recalled and placed in a canceled state.</span></span>

## <a name="workflow-deletion-will-confirm-business-event-subscription-deletions"></a><span data-ttu-id="16a21-158">ワークフローの削除によって、ビジネス イベント サブスクリプションの削除が確認されます。</span><span class="sxs-lookup"><span data-stu-id="16a21-158">Workflow deletion will confirm business event subscription deletions</span></span>
<span data-ttu-id="16a21-159">ワークフローに関連付けられたビジネス イベント サブスクリプションが見つかると、ユーザーがワークフローの削除による影響を十分に認識できるように、関連するすべてのビジネス イベント サブスクリプションの一覧が確認ダイアログボックスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="16a21-159">When business event subscriptions associated with the workflow are found, a confirmation dialog box will provide a list of any related business event subscriptions so that the user is fully aware of the effects of deleting the workflow.</span></span>

## <a name="improved-payloads-for-workflow-business-events"></a><span data-ttu-id="16a21-160">ワークフロー ビジネス イベントのためのペイロードの改善</span><span class="sxs-lookup"><span data-stu-id="16a21-160">Improved payloads for workflow business events</span></span>
<span data-ttu-id="16a21-161">標準ワークフロー コンテキストが、所有者、作成者、前回のメモを含むすべてのワークフロー ビジネス イベントのペイロードに追加されました。</span><span class="sxs-lookup"><span data-stu-id="16a21-161">Standard workflow context has been added to the payloads for all Workflow Business Events including owner, originator, and last note.</span></span>

## <a name="flow-templates-for-workflow-work-item"></a><span data-ttu-id="16a21-162">ワークフロー作業項目のフロー テンプレート</span><span class="sxs-lookup"><span data-stu-id="16a21-162">Flow templates for workflow work item</span></span>
<span data-ttu-id="16a21-163">フローテンプレートは、作業項目の完了を容易にするフローを作成する際に便利な開始点を提供するために作成されました。</span><span class="sxs-lookup"><span data-stu-id="16a21-163">Flow templates have been created to provide a useful starting point for building Flows that facilitate work item completion.</span></span> <span data-ttu-id="16a21-164">詳細については [ワークフロー ビジネス イベント](../../dev-itpro/business-events/business-events-workflow.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-164">For more information, see [Workflow Business Events](../../dev-itpro/business-events/business-events-workflow.md).</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="16a21-165">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="16a21-165">Extensibility enhancements</span></span>
<span data-ttu-id="16a21-166">プラットフォーム更新プログラム 29では、次の拡張機能が追加されました。</span><span class="sxs-lookup"><span data-stu-id="16a21-166">The following enhanced extensibility capabilities have been added in Platform update 29:</span></span>

- <span data-ttu-id="16a21-167">WorkflowApprovalプロパティ、WorkflowTaskプロパティの拡張、およびWorkflowOutcomesのWorkflowTaskへの追加を有効にします (Ref# 198831)。</span><span class="sxs-lookup"><span data-stu-id="16a21-167">Enable extension of WorkflowApproval properties, WorkflowTask properties, and addition of WorkflowOutcomes into a WorkflowTask (Ref# 198831).</span></span>
- <span data-ttu-id="16a21-168">テーブル フィールド グループからのフォームのフィールドに対してイベント トリガーを有効にします (Ref# 247364)。</span><span class="sxs-lookup"><span data-stu-id="16a21-168">Enable event triggering for fields on forms that come from table field groups (Ref# 247364).</span></span>
- <span data-ttu-id="16a21-169">クラス宣言で FormObservable 属性の使用を有効にします (Ref# 198797) 。</span><span class="sxs-lookup"><span data-stu-id="16a21-169">Enable the use of the FormObservable attribute in class declarations (Ref# 198797).</span></span>
- <span data-ttu-id="16a21-170">拡張子の既定の名前にモデル名を追加して競合を減らします (Ref# 300468)。</span><span class="sxs-lookup"><span data-stu-id="16a21-170">Add model name to extension default naming to reduce conflicts (Ref# 300468).</span></span>
- <span data-ttu-id="16a21-171">フォーム データソースおよびセキュリティ権限で、拡張テーブル フィールドの使用を有効にします (Ref# 315634)。</span><span class="sxs-lookup"><span data-stu-id="16a21-171">Enable use of extension table fields in form datasources and security privileges (Ref# 315634).</span></span>
- <span data-ttu-id="16a21-172">標準フォーム コントロールのカスタム権限では、拡張フォームに設定されたアクセス許可プロパティ値を考慮する必要があります (Ref# 313650)。</span><span class="sxs-lookup"><span data-stu-id="16a21-172">Custom privilege for a standard form control should consider needed permission property value set on extension form (Ref# 313650).</span></span>
- <span data-ttu-id="16a21-173">拡張機能によって追加されたテーブル表示メソッドをルックアップ メソッドとして使用できるようにします (Ref# 243486)。</span><span class="sxs-lookup"><span data-stu-id="16a21-173">Allow table display methods added via extension to be used as lookup methods (Ref# 243486).</span></span>
- <span data-ttu-id="16a21-174">拡張機能を使用して、フォーム データソースに表示メソッドを追加できるようにします (Ref# 256004) 。</span><span class="sxs-lookup"><span data-stu-id="16a21-174">Enable display methods to be added to Form Datasources via extension (Ref# 256004).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16a21-175">追加リソース</span><span class="sxs-lookup"><span data-stu-id="16a21-175">Additional resources</span></span>

### <a name="platform-update-29-bug-fixes"></a><span data-ttu-id="16a21-176">プラットフォーム アップデート 29 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="16a21-176">Platform update 29 bug fixes</span></span>
<span data-ttu-id="16a21-177">プラットフォーム更新 29 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="16a21-177">For information about the bug fixes included in each of the updates that are part of Platform update 29, sign in to Lifecycle Services (LCS) and view this [KB article](https://fix.lcs.dynamics.com).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="16a21-178">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="16a21-178">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="16a21-179">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="16a21-179">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="16a21-180">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="16a21-180">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="16a21-181">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="16a21-181">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="16a21-182">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="16a21-182">Removed and deprecated features</span></span>
<span data-ttu-id="16a21-183">[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="16a21-183">The [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="16a21-184">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="16a21-184">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="16a21-185">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="16a21-185">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="16a21-186">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="16a21-186">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="16a21-187">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="16a21-187">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="16a21-188">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="16a21-188">Typically, these are functional updates that need to be made to the compiler.</span></span>
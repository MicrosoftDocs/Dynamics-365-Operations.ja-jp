---
title: "Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 (2018 年 3 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 の新機能または変更された機能について説明します。 このバージョンは 2018 年 3 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 06/8/18
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: a765d51c-52d3-45c5-b578-63b5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform update 13, Platform update 14, Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: aa5eab6dbf2cc604239cac199817ead6bef6f3de
ms.openlocfilehash: c91114a7d9912b7fdaa962c38faf780b5aa0a249
ms.contentlocale: ja-jp
ms.lasthandoff: 06/08/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-15-march-2018"></a><span data-ttu-id="0ca4e-104">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 (2018 年 3 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="0ca4e-104">What's new or changed in Dynamics 365 for Finance and Operations platform update 15 (March 2018)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ca4e-105">このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 15 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-105">This topic describes features that are either new or changed in Dynamics 365 for Finance and Operations platform update 15.</span></span> 

> [!NOTE]
> <span data-ttu-id="0ca4e-106">このプラットフォームのリリースは累積されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-106">This platform release is cumulative.</span></span> <span data-ttu-id="0ca4e-107">プラットフォーム更新 13、プラットフォーム更新 14、プラットフォーム更新 15 からの新しい機能および変更された機能、およびそれ以前のすべての更新プログラムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-107">It contains new or changed features from Platform update 13, Platform update 14, and Platform update 15, as well as all earlier updates.</span></span> 

### <a name="announcing-the-dynamics-365-spring-18-release-notes"></a><span data-ttu-id="0ca4e-108">Dynamics 365 2018 年春リリース ノートの発表</span><span class="sxs-lookup"><span data-stu-id="0ca4e-108">Announcing the Dynamics 365 Spring '18 release notes</span></span>
<span data-ttu-id="0ca4e-109">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="0ca4e-109">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span> 

<span data-ttu-id="0ca4e-110">[2018 年春リリース ノートをダウンロードします](http://download.microsoft.com/download/1/C/0/1C0A4DB7-9CE8-4D25-AC7F-65579E713BA8/ReleaseNotes_Dynamics365_03192018.pdf)。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-110">[Download the Spring '18 release notes](http://download.microsoft.com/download/1/C/0/1C0A4DB7-9CE8-4D25-AC7F-65579E713BA8/ReleaseNotes_Dynamics365_03192018.pdf).</span></span> <span data-ttu-id="0ca4e-111">計画に使用できる単一の PDF 内のすべての詳細を、端から端まで徹底的に捕捉しました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-111">We've captured all the details, end to end, top to bottom, in a single PDF that you can use for planning.</span></span> 

### <a name="platform-update-15-bug-fixes"></a><span data-ttu-id="0ca4e-112">プラットフォーム アップデート 15 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="0ca4e-112">Platform update 15 bug fixes</span></span>
<span data-ttu-id="0ca4e-113">プラットフォーム更新プログラム 15 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=869898) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-113">For information about the bug fixes included in Platform update 15, log in to Lifecycle Services (LCS) and view this [KB article](https://go.microsoft.com/fwlink/?linkid=869898).</span></span>

## <a name="ability-to-color-grid-rows-without-overlayering-via-formdatasource-ondisplayoptioninitialize-event"></a><span data-ttu-id="0ca4e-114">FormDataSource OnDisplayOptionInitialize イベントを介してオーバーレイすることなくグリッド行の色分けをする機能</span><span class="sxs-lookup"><span data-stu-id="0ca4e-114">Ability to color grid rows without overlayering via FormDataSource OnDisplayOptionInitialize event</span></span>
<span data-ttu-id="0ca4e-115">オーバーレイすることなくグリッド行の色分けをする機能が、FormDataSource 上で OnDisplayOptionInitialize イベントを介して可能になりました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-115">The ability to color grid rows without overlayering is now possible via the OnDisplayOptionInitialize event on FormDataSource.</span></span>

## <a name="accessibility-support-for-controls-and-forms-developed-using-the-cloud-platform"></a><span data-ttu-id="0ca4e-116">クラウド プラットフォームを使用して開発されたコントロールとフォームのユーザー補助サポート</span><span class="sxs-lookup"><span data-stu-id="0ca4e-116">Accessibility support for controls and forms developed using the cloud platform</span></span> 

<span data-ttu-id="0ca4e-117">アクセス可能なソフトウェアを提供するに対する取り組みを再確認することにより、この更新プログラムは既に豊富なユーザー補助機能セットを増やすことに焦点を当てています。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-117">Reaffirming our commitment to providing accessible software, this update focuses on broadening our already rich accessibility feature set.</span></span> <span data-ttu-id="0ca4e-118">これらの更新プログラムは、Microsoft のアクセシビリティ標準に準拠するために、グリッド、表、フォームなどの多くのプラットフォーム コンポーネントを改善します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-118">These updates improve many platform components such as grids, tables, and forms to comply with Microsoft’s Accessibility Standards.</span></span> <span data-ttu-id="0ca4e-119">キーボードを使用したタスクの実行の詳細サポートには、スクリーン リーダー、ハイコントラスト テーマや完全なラベル サポート、およびクラウド プラットフォームを使用して作成されたアプリケーションとの豊富な統合があり、これにより障害のあるユーザーのための追加環境が提供されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-119">With additional support for performing tasks via the keyboard, there is richer integration with screen readers, high contrast theming and full label support, and applications built using the cloud platform which provide additional opportunities for users with disabilities.</span></span>

## <a name="client-based-alerts"></a><span data-ttu-id="0ca4e-120">クライアントに基づく警告</span><span class="sxs-lookup"><span data-stu-id="0ca4e-120">Client-based alerts</span></span> 
<span data-ttu-id="0ca4e-121">クライアント ベースの警告機能を使用すると、Finance and Operations クライアントを離れずに警告ルールを定義できます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-121">Client-based alert functionality enables a user to define an alert rule without leaving the Finance and Operations client.</span></span> <span data-ttu-id="0ca4e-122">請求書の支払いや顧客の住所変更など、ビジネス イベントに基づいて警告を定義できます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-122">Users can define alerts based on business events, such as when an invoice is paid or a customer changes an address.</span></span> <span data-ttu-id="0ca4e-123">特定の条件が満たされる場合、ユーザーに警告する通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-123">When specific conditions are met, the system will show a notification to alert the user.</span></span> 

<span data-ttu-id="0ca4e-124">Dynamics 365 for Finance and Operations の重大なイベントの通知システムは、警告によって形成されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-124">Alerts form a notification system for critical events in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0ca4e-125">警告を使用することで、作業日に追跡するイベントに関する情報を常に受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-125">You can use alerts to stay informed about events that you want to keep track of during the workday.</span></span> <span data-ttu-id="0ca4e-126">また、独自のルール セットを簡単に設定して、延滞出荷、削除された注文、変更された価格、またはその他対応が必要なイベントに関する警告を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-126">You can also easily set up your own set of rules so that you are alerted about overdue deliveries, orders that are deleted, prices that change, or other events that you must respond to.</span></span>

<span data-ttu-id="0ca4e-127">警告の詳細については、[警告の概要](alerts-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-127">For more information about alerts, see [Alerts overview](alerts-overview.md).</span></span>

## <a name="embed-powerapps"></a><span data-ttu-id="0ca4e-128">PowerApps の埋め込み</span><span class="sxs-lookup"><span data-stu-id="0ca4e-128">Embed PowerApps</span></span>
<span data-ttu-id="0ca4e-129">開発者や非テクニカル ユーザーがコードを記述することなくカスタム ビジネス アプリを構築できるサービスである Microsoft PowerApps はサポートされています。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-129">Microsoft PowerApps, a service that allows developers and nontechnical users to build custom business apps without writing code, is now supported.</span></span> <span data-ttu-id="0ca4e-130">埋め込み PowerApp はページに追加できるだけでなく、編集、削除、または共有することができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-130">You can add an embedded PowerApp to a page as well as edit, delete, or share the embedded PowerApp.</span></span> <span data-ttu-id="0ca4e-131">また、Finance and Operations からのデータを活用する PowerApp を構築することができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-131">You can also build a PowerApp to leverage data from Finance and Operations.</span></span> <span data-ttu-id="0ca4e-132">詳細については、「[PowerApps の埋め込み](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-132">For more information, see [Embed PowerApps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).</span></span> 

## <a name="extension-and-overlayering-options-in-visual-studio"></a><span data-ttu-id="0ca4e-133">Visual Studio の拡張子およびオーバーレイヤ オプション</span><span class="sxs-lookup"><span data-stu-id="0ca4e-133">Extension and overlayering options in Visual Studio</span></span>
<span data-ttu-id="0ca4e-134">今回のリリースでは、Visual Studio で拡張機能とオーバーレイ オプションを表示する方法を調整しました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-134">In this release we have adjusted how the extension and overlayering options are presented in Visual Studio.</span></span> <span data-ttu-id="0ca4e-135">拡張オプションが最初に表示され、オーバーレイオ プションが「カスタマイズ」から「オーバーレイ」に変更され、より明示的になりました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-135">The extension options are now shown first and the overlayering option has changed from "Customize" to "Overlayer" to be more explicit.</span></span>
<span data-ttu-id="0ca4e-136">いつでも可能な場合は、拡張子を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-136">Extensions should be used whenever possible.</span></span> 

<span data-ttu-id="0ca4e-137">カスタマイズ オプションが推奨される使用順に表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-137">The customization options are now shown in the recommended order of use:</span></span>
1.  <span data-ttu-id="0ca4e-138">拡張機能を作成</span><span class="sxs-lookup"><span data-stu-id="0ca4e-138">Create extension</span></span>
2.  <span data-ttu-id="0ca4e-139">新しいプロジェクトに拡張機能を作成する</span><span class="sxs-lookup"><span data-stu-id="0ca4e-139">Create extension in new project</span></span>
3.  <span data-ttu-id="0ca4e-140">オーバーレイヤー</span><span class="sxs-lookup"><span data-stu-id="0ca4e-140">Overlayer</span></span>

## <a name="message-center-has-been-upgraded-to-the-new-action-center-with-improved-notification-visuals-and-capabilities"></a><span data-ttu-id="0ca4e-141">メッセージ センターは、通知ビジュアルと機能が改良された新しいアクション センターにアップグレードされました</span><span class="sxs-lookup"><span data-stu-id="0ca4e-141">Message Center has been upgraded to the new Action Center with improved notification visuals and capabilities</span></span>
<span data-ttu-id="0ca4e-142">メッセージ センターは、新しいアクション センターにアップグレードされました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-142">The Message Center has been upgraded to the new Action Center.</span></span> <span data-ttu-id="0ca4e-143">ビジュアルが最新の通知インターフェイスを反映するために更新されただけではなく、新しいメッセージング API を使用してアクション センターに送信されるメッセージに、通知の保持を含む追加機能、メッセージに関連付けられた 1 つ以上のアクションを指定する機能、ユーザーのリストまたはロールのリストにメッセージを送信する機能が付属します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-143">Not only have the visuals been refreshed to reflect a more modern notification interface, but messages sent to the Action Center using the new messaging API also come with additional capabilities including notification persistence, the ability to specify one or more actions associated with a message, and the ability to send a message to a list of users or a list of roles.</span></span> <span data-ttu-id="0ca4e-144">メッセージ センターへルーティングされたすべての既存のメッセージはアクション センターへ自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-144">All existing messages that were routed to the Message Center will automatically be surfaced in the Action Center.</span></span>

## <a name="move-master-data-from-one-environment-to-another-using-the-excel-add-in"></a><span data-ttu-id="0ca4e-145">Excel アドインを使用した別の環境へのマスター データの移動</span><span class="sxs-lookup"><span data-stu-id="0ca4e-145">Move master data from one environment to another using the Excel add-in</span></span> 
<span data-ttu-id="0ca4e-146">Dynamics 365 for Talent では、「はじめに」 Workbooks が提供され、ユーザーが Excel を使用して対話形式でデータを表示、編集、作成できます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-146">Dynamics 365 for Talent provides “getting started” workbooks so users can use Excel to interactively view, edit, and create data.</span></span> <span data-ttu-id="0ca4e-147">Excel アドインを使用するこれらのワークブックは、生産的な環境設定操作を実現します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-147">These workbooks, powered by the Excel add-in, provide a productive environment configuration experience.</span></span>
<span data-ttu-id="0ca4e-148">この拡張機能では、ある環境から Excel にデータを読み込み、環境アドレスを変更してから、そのデータを新しい環境に公開することにより、データをある環境から別の環境に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-148">With this enhancement, you can move data from one environment to another by reading data into Excel from one environment, change the environment address, and then publish the data into the new environment.</span></span>

<span data-ttu-id="0ca4e-149">詳細については、「[環境データのコピー](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#copy-environment-data)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-149">For more information, see [Copy environment data](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/office-integration/use-excel-add-in#copy-environment-data).</span></span>

## <a name="one-voucher-deprecation"></a><span data-ttu-id="0ca4e-150">1 つの伝票の廃止</span><span class="sxs-lookup"><span data-stu-id="0ca4e-150">One voucher deprecation</span></span>
<span data-ttu-id="0ca4e-151">財務仕訳帳 (一般仕訳帳、固定資産仕訳帳、仕入先支払仕訳帳など) の既存の機能を使用して、1 つの伝票のコンテキストで複数の補助元帳トランザクションを入力できます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-151">The existing functionality for financial journals (general journal, fixed asset journal, vendor payment journal, and so on) lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="0ca4e-152">この機能を「1 つの伝票」と呼びます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-152">This functionality is referred to as “One voucher.”</span></span> <span data-ttu-id="0ca4e-153">1 つの伝票機能により、決済、税計算、補助元帳の一般会計への調整、財務報告などの間に問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-153">The One voucher functionality causes issues during settlement, tax calculation, reconciliation of a subledger to the general ledger, financial reporting, and more.</span></span> <span data-ttu-id="0ca4e-154">これらの問題のため、1 つの伝票機能は廃止されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-154">Because of these issues, the One voucher functionality will be made obsolete.</span></span> <span data-ttu-id="0ca4e-155">ただし、この機能に依存する機能的なギャップがあるため、機能が一度に無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-155">However, because there are functional gaps that depend on this functionality, the functionality won't become obsolete all at once.</span></span> <span data-ttu-id="0ca4e-156">代わりに、次のスケジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-156">Instead, we will use the following schedule:</span></span>
-   <span data-ttu-id="0ca4e-157">**18 年春リリース** – 機能は、一般会計パラメーターによって既定で、オフになります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-157">**Spring '18 release** – The functionality will be turned off by default, through a General ledger parameter.</span></span> <span data-ttu-id="0ca4e-158">ただし、組織が単一伝票文書に記載されているビジネス シナリオ ギャップの範囲内にシナリオがある場合、機能をオンにできます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-158">However, you can turn the functionality on if your organization has a scenario that falls in the business scenario gaps that are listed in the One voucher documentation.</span></span>
    -  <span data-ttu-id="0ca4e-159">顧客が 1 つの伝票を必要としないビジネス シナリオがある場合、機能をオンにしないでください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-159">If a customer has a business scenario that doesn't require One voucher, don't turn the functionality on.</span></span> <span data-ttu-id="0ca4e-160">この機能が使用される場合、単一伝票文書に記載されている領域の「不具合」は修正されません。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-160">We won't fix “bugs” in the areas that are identified in the One voucher documentation if this functionality is used.</span></span>
    - <span data-ttu-id="0ca4e-161">機能のギャップのいずれかに機能が必要でない限り、Microsoft Dynamics 365 Finance and Operations への統合に 1 つの伝票を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-161">Stop using One voucher for integrations into Microsoft Dynamics 365 Finance and Operations, unless the functionality is required for one of the functional gaps.</span></span>
-   <span data-ttu-id="0ca4e-162">**18 年秋およびそれ以降のリリース** – 機能的なギャップが埋まります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-162">**Fall '18 and later releases** – The functional gaps will be filled.</span></span> <span data-ttu-id="0ca4e-163">機能的なギャップが埋められた後、1 つの伝票の機能が完全にオフになります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-163">After the functional gaps are filled, the One voucher functionality will be permanently turned off.</span></span>

<span data-ttu-id="0ca4e-164">この機能の使用と廃止に関する詳細については、[1 つの伝票ドキュメント](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/general-ledger/one-voucher)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-164">See the [One voucher documentation](https://docs.microsoft.com/en-us/dynamics365/unified-operations/financials/general-ledger/one-voucher) for detailed information about the use and deprecation of this functionality.</span></span>


## <a name="power-users-can-add-custom-fields-to-forms-without-developer-customization"></a><span data-ttu-id="0ca4e-165">Power User は、開発者カスタマイズなしのフォームにカスタム フィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-165">Power users can add custom fields to forms without developer customization</span></span> 
<span data-ttu-id="0ca4e-166">多くのアプリケーションのカスタマイズには、既存のテーブルへの 1 つまたは複数のフィールドの追加、およびそれらをアプリケーション フォームに含めることがあります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-166">Many application customizations involve adding one or more fields to existing tables and including them in application forms.</span></span> <span data-ttu-id="0ca4e-167">ほとんどのカスタマイズは、フィールドを追加で構成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-167">Most of your customizations may be comprised of adding fields.</span></span>

<span data-ttu-id="0ca4e-168">開発、テスト、およびコード ライフ サイクル管理のために開発者が操作する必要があるため、カスタマイズは高価です。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-168">Customizations are expensive because they require developer intervention for development, test, and code life cycle management.</span></span> <span data-ttu-id="0ca4e-169">カスタマイズは、ある環境から別の環境にも管理および移行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-169">Customizations also need to be managed and migrated from one environment to another.</span></span>  

<span data-ttu-id="0ca4e-170">Dynamics 365 for Finance and Operations のフォームへのカスタム フィールドの追加を簡単にしました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-170">We have made it easier to add custom fields to forms in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="0ca4e-171">開発者向けのカスタマイズは不要になりました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-171">Developer customization is no longer needed.</span></span> <span data-ttu-id="0ca4e-172">代わりに、パワー ユーザーはカスタム フィールドをテーブルに追加してから、個人用設定を使用してフォームにそのフィールドを配置できます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-172">Instead, a power user can add a custom field to a table and then place that field on the form using personalization.</span></span> <span data-ttu-id="0ca4e-173">IT 管理者は個人用設定を組織内で他のユーザーと共有できます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-173">An IT administrator can then share the personalization with others in your organization.</span></span> <span data-ttu-id="0ca4e-174">カスタム フィールドを作成および管理する方法の詳細については、[カスタム フィールド](user-defined-fields.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-174">For information about how to create and manage custom fields, see [Custom fields](user-defined-fields.md).</span></span>

## <a name="sr-10-certifications-for-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="0ca4e-175">(SR 10) Finance and Operations の Dynamics 365 の証明書</span><span class="sxs-lookup"><span data-stu-id="0ca4e-175">(SR 10) Certifications for Dynamics 365 for Finance and Operations</span></span> 

<span data-ttu-id="0ca4e-176">**ISO 27001(Secure)** – ISO 27001 認証は、サービスが情報セキュリティ管理システム (ISMS) で概説されているコントロールおよび仕様に準拠していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-176">**ISO 27001(Secure)** – ISO 27001 certification confirms that the service complies with the controls and specifications outlined in the information security management system (ISMS).</span></span> <span data-ttu-id="0ca4e-177">ISO 27001 を達成することにより、お客様のビジネスを実行するために当社のサービスが安全であることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-177">By achieving ISO 27001, this helps to ensure that our service is secure for you to run your business on.</span></span> <span data-ttu-id="0ca4e-178">これを選択した場合は、ISO27001 認定サービスでビジネスを実行していることを監査人に安心させることで、自分のビジネスを証明するサポートにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-178">This also helps to support your efforts to certify your own business, if you choose to do so, by reassuring your auditors that you are running your business on an ISO27001 certified service.</span></span>

<span data-ttu-id="0ca4e-179">**ISO 27018 (個人データの保護)** – ISO 27018 は、クラウド内の個人情報の保護を対象としています。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-179">**ISO 27018 (Protects personal data)** – ISO 27018 focuses on protection of personal data in the cloud.</span></span> <span data-ttu-id="0ca4e-180">Dynamics 365 for Finance and Operations は、ISO 27018 認証を取得しています。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-180">Dynamics 365 for Finance and Operations has achieved ISO 27018 certification.</span></span> <span data-ttu-id="0ca4e-181">マイクロソフトのサービスを使用して業務を管理するとき、個人の機密データはクラウドで安全かつ保護されることを理解していただくことを望みます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-181">We want you to know that when you are using our service to manage your business, your personal and sensitive data is safe and protected in the cloud.</span></span> <span data-ttu-id="0ca4e-182">また、業務に独自の ISO 27018 認証の取得を選択した場合、監査担当者は Finance and Operations に ISO 27108 認証があることを評価します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-182">Additionally, if you choose to gain your own ISO 27018 certification for your business, your auditors will appreciate that Finance and Operations has ISO 27108 certification.</span></span> 

<span data-ttu-id="0ca4e-183">**SOC-1/Type-2 および SOC-2/Type-2** – サービス組織制御レポート (SOC) は、クラウド サービスに財務データが安全かつ保護されていることを保証するためのコントロールの設定があることを確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-183">**SOC-1/Type-2 and SOC-2/Type-2** – The service organization controls report (SOC) helps to confirm that a cloud service has controls in place to ensure that financial data is secure and protected.</span></span> <span data-ttu-id="0ca4e-184">Finance and Operations は SOC-1/Type-2 および SOC-2/Type-2 認証を獲得しました。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-184">Finance and Operations has achieved SOC-1/Type-2 and SOC-2/Type-2 certification.</span></span>


## <a name="support-for-display-and-edit-methods-on-form-data-sources-using-augmentation-classes-extensionof"></a><span data-ttu-id="0ca4e-185">拡張クラス (ExtensionOf) を使用したフォーム データ ソースの表示および編集メソッドのサポート</span><span class="sxs-lookup"><span data-stu-id="0ca4e-185">Support for display and edit methods on form data sources using augmentation classes (ExtensionOf)</span></span>

<span data-ttu-id="0ca4e-186">次の例では、テーブルやフォームの強化されたクラスの表示/編集メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-186">The following examples use Display/Edit methods on augmented classes for tables and forms.</span></span>

#### <a name="class-extension-for-a-form"></a><span data-ttu-id="0ca4e-187">フォームのクラスの拡張機能</span><span class="sxs-lookup"><span data-stu-id="0ca4e-187">Class extension for a form</span></span>

```
[ExtensionOf(formstr(abForm))]
public final class abClassForm_Extension
{
    private Name previousName;
    private Counter noOfChanges;

    public display Name formExt_Display()
    {
        return previousName;
    }

    public edit Name formExt_Edit(boolean _set, Name _value)
    {
        if (_set)
        {
            noOfChanges++;
            previousName = strFmt("%1 %2", _value, noOfChanges);
        }

        return previousName;
    }
}
  ``` 
#### <a name="class-extension-for-a-table"></a><span data-ttu-id="0ca4e-188">テーブルのクラスの拡張機能</span><span class="sxs-lookup"><span data-stu-id="0ca4e-188">Class extension for a table</span></span>
  ``` 
[ExtensionOf(tablestr(abTable))]
public final class abClassTable_Extension
{
    public display Name tableExt_Display()
    {
        return "tableExt_Display " + this.FirstName + " " + this.LastName;
    }

    public edit Name tableExt_Edit(boolean _set, Name _value)
    {
        if (_set)
        {
            this.FirstName = "tableExt_Edit " +_value;
        }

        return this.FirstName;
    }
}
  ``` 
<span data-ttu-id="0ca4e-189">フォームまたはフォーム拡張は、DataMethod プロパティに `<ClassName>.<MethodName>` を指定することによって、フォーム コントロールから表示および編集メソッドを消費することができます。</span><span class="sxs-lookup"><span data-stu-id="0ca4e-189">The form or form extension can then consume the display and edit methods from a form control by providing the `<ClassName>.<MethodName>` in the DataMethod property.</span></span>


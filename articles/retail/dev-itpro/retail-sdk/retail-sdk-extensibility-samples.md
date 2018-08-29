---
title: "Retail ソフトウェア開発キット (SDK) の拡張機能サンプル"
description: "Retail SDK には、拡張機能サンプルが含まれています。 これらのサンプルは、Retail をカスタマイズするさまざまな方法について学ぶ良い方法です。"
author: mugunthanm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 89803
ms.assetid: 565d9e98-77eb-4495-987a-ad9e2de303cc
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 33c2ea2172fd234fed3edf08fc37a0b8ff58cba3
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="retail-software-development-kit-sdk-extensibility-samples"></a><span data-ttu-id="e3fa5-104">Retail ソフトウェア開発キット (SDK) の拡張機能サンプル</span><span class="sxs-lookup"><span data-stu-id="e3fa5-104">Retail software development kit (SDK) extensibility samples</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3fa5-105">Retail SDK には、拡張機能サンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-105">The Retail SDK includes extensibility samples.</span></span> <span data-ttu-id="e3fa5-106">これらのサンプルは、Retail をカスタマイズするさまざまな方法について学ぶ良い方法です。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-106">These samples are a good way to learn about different ways to customize Retail.</span></span>  

<span data-ttu-id="e3fa5-107">Retail ソフトウェアの開発キット (SDK) には、機能拡張のサンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-107">The Retail software development kit (SDK) includes extensibility samples.</span></span> <span data-ttu-id="e3fa5-108">これらのプロジェクトを定型プロジェクトとして使用して、特定のカスタマイズを開始することができます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-108">You can also use these projects as boilerplate projects to get started with a specific customization.</span></span> <span data-ttu-id="e3fa5-109">たとえば、新しい commerce runtime (CRT) 拡張子を開始するには、CommerceRuntime サンプル プロジェクトのいずれかを新しいフォルダーにコピーし、プロジェクトのインポート パスを調整でき、それからプロジェクトで作業を開始できます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-109">For example, to start a new commerce runtime (CRT) extension, you can just copy one of the CommerceRuntime sample projects into a new folder, adjust the project import paths, and then start working in the project.</span></span> <span data-ttu-id="e3fa5-110">ほとんどのサンプルでは、追加のステップ バイ ステップの手順は、Retail SDK\\ドキュメント フォルダーで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-110">For most of the samples, additional step-by-step instructions are available in the Retail SDK\\Documents folder.</span></span> <span data-ttu-id="e3fa5-111">次のテーブルにサンプルの高レベルなリストを示します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-111">The following table provides a high-level list of the samples.</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e3fa5-112"><strong>サンプル名</strong></span><span class="sxs-lookup"><span data-stu-id="e3fa5-112"><strong>Sample name</strong></span></span></td>
<td><span data-ttu-id="e3fa5-113"><strong>説明</strong></span><span class="sxs-lookup"><span data-stu-id="e3fa5-113"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="e3fa5-114"><strong>説明されているタスク</strong></span><span class="sxs-lookup"><span data-stu-id="e3fa5-114"><strong>Tasks that are demonstrated</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3fa5-115">CrossLoyalty</span><span class="sxs-lookup"><span data-stu-id="e3fa5-115">CrossLoyalty</span></span></td>
<td><span data-ttu-id="e3fa5-116">この例には、AdventureWorks と Contoso の 2 つの小売業者が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-116">This sample includes two retailers, AdventureWorks and Contoso.</span></span> <span data-ttu-id="e3fa5-117">Contoso 小売業者は、AdventureWorks から顧客が獲得するロイヤルティ ポイントを受け付けます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-117">The Contoso retailer accepts loyalty points that customers earn from AdventureWorks.</span></span> <span data-ttu-id="e3fa5-118">このサンプルでは、簡単な新しい CRT サービスを作成して、Retail Modern POS ボタンがクリックされたときにそのサービスを呼び出す方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-118">The sample shows how to create a simple new CRT service and call it when a button in Retail Modern POS is clicked.</span></span> <span data-ttu-id="e3fa5-119">クロス ロイヤルティのシナリオをシミュレートします。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-119">It simulates the cross-loyalty scenario.</span></span> <span data-ttu-id="e3fa5-120">構成、CRT、Retail サーバー、Retail プロキシ、販売時点管理 (POS) (Modern POS と Cloud POS の両方) に変更があります。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-120">There are changes to the configuration, CRT, Retail Server, Retail Proxy, and point of sale (POS) (both Modern POS and Cloud POS).</span></span> <span data-ttu-id="e3fa5-121">この例では、最新の POS オフライン モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-121">This sample supports offline mode for Modern POS.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3fa5-122">新しい CRT と Retail サーバーの拡張機能、または新しいサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-122">Create a new CRT and Retail Server extension, or a new service.</span></span></li>
<li><span data-ttu-id="e3fa5-123">個別のプロジェクトとして新しい工程を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-123">Create a new operation as a separate project.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3fa5-124">EmailPreference</span><span class="sxs-lookup"><span data-stu-id="e3fa5-124">EmailPreference</span></span></td>
<td><span data-ttu-id="e3fa5-125">この例では、拡張プロパティを使用してエンティティを拡張する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-125">This sample shows how to use extension properties to extend an entity.</span></span> <span data-ttu-id="e3fa5-126">拡張エンティティは、Microsoft Dynamics 365 for Retail とチャネル データベースの両方に保持され、POS クライアントは値へのアクセスを可能にします。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-126">The extended entity is persisted in both the Microsoft Dynamics 365 for Retail and channel databases, and the POS client enables access to the value.</span></span> <span data-ttu-id="e3fa5-127">新しい値は、RetailRealtimeTransaction サービスを介して Retail に同期的に書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-127">The new value is written synchronously to Retail via the RetailRealtimeTransaction service.</span></span> <span data-ttu-id="e3fa5-128">拡張機能プロパティは自動的にフローするため、CRT または Retail サーバーに必要なカスタマイズはありません。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-128">No customization is required in the CRT or Retail Server, because extension properties flow automatically.</span></span> <span data-ttu-id="e3fa5-129">ページ、テーブル、Real-time Service (RTS) クライアント、Commerce Data Exchange (CDX)、チャネル データベース、POS (Modern POS と Cloud POS の両方) に変更があります。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-129">There are changes to pages, tables, the Real-time Service (RTS) client, Commerce Data Exchange (CDX), the channel database, and the POS (both Modern POS and Cloud POS).</span></span> <span data-ttu-id="e3fa5-130">この例では、オフライン モードをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-130">This sample doesn&#39;t support offline mode.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3fa5-131">既存の Modern POS/クラウド POS の表示またはページを変更します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-131">Modify an existing Modern POS/Cloud POS view or page.</span></span></li>
<li><span data-ttu-id="e3fa5-132">Real-time Service を拡張します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-132">Extend the Real-time Service.</span></span></li>
<li><span data-ttu-id="e3fa5-133">拡張プロパティを使用して、カスタム フィールド値をデータベースに格納します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-133">Use extension properties to store custom field values in the database.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3fa5-134">StoreHours</span><span class="sxs-lookup"><span data-stu-id="e3fa5-134">StoreHours</span></span></td>
<td><span data-ttu-id="e3fa5-135">この例は、Retail とチャネルの両方に新しいビジネス エンティティ (StoreHours) を作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-135">This sample shows how to create a new business entity (StoreHours) across both Retail and the channel.</span></span> <span data-ttu-id="e3fa5-136">テーブル、CDX、チャネル データベース、CRT、Retail サーバー、POS (Modern POS と Cloud POS の両方) に変更があります。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-136">There are changes to tables, CDX, the channel database, the CRT, Retail Server, and the POS (both Modern POS and Cloud POS).</span></span> <span data-ttu-id="e3fa5-137">この例では、最新の POS オフライン モードをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-137">This sample supports offline mode for Modern POS.</span></span></td>
<td><ul>
<li><span data-ttu-id="e3fa5-138">新しい CRT と Retail サーバーの拡張機能、または新しいサービスを作成します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-138">Create a new CRT and Retail Server extension, or a new service.</span></span></li>
<li><span data-ttu-id="e3fa5-139">既存の MPOS/クラウド POS の表示またはページを変更します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-139">Modify an existing MPOS/Cloud POS view or page.</span></span></li>
<li><span data-ttu-id="e3fa5-140">CDX を使用して、チャネルにカスタム テーブル データを送信します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-140">Send the custom table data to the channel by using CDX.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3fa5-141">HealthCheck</span><span class="sxs-lookup"><span data-stu-id="e3fa5-141">HealthCheck</span></span></td>
<td><span data-ttu-id="e3fa5-142">この例は、機能を追加して既存の CRT サービスを拡張する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-142">This sample shows how to expand an existing CRT service by adding functionality.</span></span> <span data-ttu-id="e3fa5-143">この場合、その他のシステムの正常性は、既に存在する RunHealthCheckServiceRequest サービスの一環として確認することができます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-143">In this case, the health of some other system can be checked as part of the RunHealthCheckServiceRequest service that already exists.</span></span> <span data-ttu-id="e3fa5-144">CRT および CRT テスト ホストに変更があります。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-144">There are changes to the CRT and CRT Test Host.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3fa5-145">ExtensionProperties</span><span class="sxs-lookup"><span data-stu-id="e3fa5-145">ExtensionProperties</span></span></td>
<td><span data-ttu-id="e3fa5-146">この例は、CRT の次のカスタマイズの戦略を示しています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-146">This sample shows the following customization strategies for the CRT:</span></span>
<ul>
<li><span data-ttu-id="e3fa5-147">サービス、エンティティ、要求、および応答の拡張プロパティ</span><span class="sxs-lookup"><span data-stu-id="e3fa5-147">Extension properties for service, entity, request, and response</span></span></li>
<li><span data-ttu-id="e3fa5-148">トリガー</span><span class="sxs-lookup"><span data-stu-id="e3fa5-148">Triggers</span></span></li>
<li><span data-ttu-id="e3fa5-149">通知</span><span class="sxs-lookup"><span data-stu-id="e3fa5-149">Notifications</span></span></li>
<li><span data-ttu-id="e3fa5-150">通知ハンドラー</span><span class="sxs-lookup"><span data-stu-id="e3fa5-150">Notification handlers</span></span></li>
</ul></td>
<td><span data-ttu-id="e3fa5-151">拡張プロパティを使用して、カスタム フィールド値をデータベースに格納します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-151">Use extension properties to store custom field values in a database.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3fa5-152">CommerceRuntime テスト ホスト</span><span class="sxs-lookup"><span data-stu-id="e3fa5-152">CommerceRuntime Test Host</span></span></td>
<td><span data-ttu-id="e3fa5-153">このツールは、Retail サーバーに似た通常の CRT ホストを模倣します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-153">This tool mimics a typical CRT host that resembles Retail Server.</span></span> <span data-ttu-id="e3fa5-154">Retail サーバーまたは UI クライアントでの変更を必要としない CRT 拡張機能の簡単なテストをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-154">It supports simple testing of CRT extensions that doesn&#39;t require changes in Retail Server or UI clients.</span></span> <span data-ttu-id="e3fa5-155">CRT に必要なサービスを登録して、それを実行するだけです。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-155">You just register the services that are required for the CRT and run it.</span></span> <span data-ttu-id="e3fa5-156"><strong>注記:</strong> CRT 拡張機能の一部である可能性のある RealTimeTransaction サービスコールは正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-156"><strong>Note:</strong> RealTimeTransaction service calls that might be part of a CRT extension won&#39;t work correctly.</span></span> <span data-ttu-id="e3fa5-157">これらのサービス コールをテストするには、代わりに RetailServer テスト クライアント サンプルを使用します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-157">To test these service calls, use the RetailServer Test Client sample instead.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3fa5-158">RetailServer テスト クライアント</span><span class="sxs-lookup"><span data-stu-id="e3fa5-158">RetailServer Test Client</span></span></td>
<td><span data-ttu-id="e3fa5-159">この単純なアプリケーションを使用すると、Retail サーバーの呼び出し、Retail プロキシを通してのオフライン モードの呼び出し、またはその両方を行なえます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-159">You can use this simple application to make Retail Server calls, offline mode calls through the Retail Proxy, or both.</span></span> <span data-ttu-id="e3fa5-160">このサンプル アプリケーションはクライアントとして機能します。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-160">This sample application acts as a client.</span></span> <span data-ttu-id="e3fa5-161">POS クライアントと似ていますが、UI の変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-161">It resembles the POS clients but requires no UI changes.</span></span> <span data-ttu-id="e3fa5-162">したがって、迅速なテストと開発をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-162">Therefore, it supports rapid testing and development.</span></span> <span data-ttu-id="e3fa5-163">このツールを使用すると、UI チームに渡す前に、チャンネル データベース、RTS、CRT、および/または Retail サーバーのカスタマイズを検証できます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-163">You can use this tool to verify customizations of the channel database, RTS, CRT, and/or Retail Server before you hand them off to the UI team.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3fa5-164">OnlineStore</span><span class="sxs-lookup"><span data-stu-id="e3fa5-164">OnlineStore</span></span></td>
<td><span data-ttu-id="e3fa5-165">この例は、Eコマース SDK の使用を紹介する ASP.NET の実装です。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-165">This sample is an ASP.NET implementation that showcases the use of the Ecommerce SDK.</span></span> <span data-ttu-id="e3fa5-166">これには、ストア フロントと公開ジョブの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-166">It includes both a store front and a publishing job.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3fa5-167">OpenIdConnectUtility</span><span class="sxs-lookup"><span data-stu-id="e3fa5-167">OpenIdConnectUtility</span></span></td>
<td><span data-ttu-id="e3fa5-168">この例では、Google ID を使用して顧客コンテキスト (C2) で Retail サーバー を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-168">This sample lets you call Retail Server in a customer context (C2) by using a Google Identity.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e3fa5-169">CashDispenser (HardwareStation)</span><span class="sxs-lookup"><span data-stu-id="e3fa5-169">CashDispenser (HardwareStation)</span></span></td>
<td><span data-ttu-id="e3fa5-170">この例は、現金自動支払機を統合できるように Retail ハードウェア ステーションをカスタマイズする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-170">This sample shows how to customize Retail Hardware Station so that a cash dispenser can be integrated.</span></span></td>
<td><span data-ttu-id="e3fa5-171">新しいハードウェア ステーション プロジェクトを作成し、新しい周辺機器をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-171">Create a new Hardware Station project and support for new peripherals.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e3fa5-172">Rambler (HardwareStation)</span><span class="sxs-lookup"><span data-stu-id="e3fa5-172">Rambler (HardwareStation)</span></span></td>
<td><span data-ttu-id="e3fa5-173">この例は、新築平屋携帯カード リーダーを統合できるようにハードウェア ステーションをカスタマイズする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-173">This sample shows how to customize Hardware Station so that a Rambler Mobile Card Reader can be integrated.</span></span></td>
<td><span data-ttu-id="e3fa5-174">新しいハードウェア ステーション プロジェクトを作成し、新しい周辺機器をサポートします。</span><span class="sxs-lookup"><span data-stu-id="e3fa5-174">Create a new Hardware Station project and support for new peripherals.</span></span></td>
</tr>
</tbody>
</table>







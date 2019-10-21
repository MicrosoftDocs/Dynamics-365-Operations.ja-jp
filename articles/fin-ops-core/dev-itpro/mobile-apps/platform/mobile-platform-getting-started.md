---
title: モバイル プラットフォームを使い始める
description: このトピックでは、モバイル プラットフォームでの開発方法について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: f5aa0c60-25cc-4453-8df9-efab19b7e272
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: 29956a05b8ecbf8e008bdbb071611fba0956aa24
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248722"
---
# <a name="get-started-with-the-mobile-platform"></a><span data-ttu-id="0f047-103">モバイル プラットフォームを使い始める</span><span class="sxs-lookup"><span data-stu-id="0f047-103">Get started with the mobile platform</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0f047-104">開発環境を取得した後、開発を開始するために次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="0f047-104">After you acquire a development environment, complete the following procedures to get started with development.</span></span>

### <a name="get-the-fleet-management-mobile-forms"></a><span data-ttu-id="0f047-105">フリーと管理モバイル フォームを取得する</span><span class="sxs-lookup"><span data-stu-id="0f047-105">Get the Fleet Management mobile forms</span></span>

<span data-ttu-id="0f047-106">**フリート管理** モジュール内に新しい専用のフォームを作成しました。</span><span class="sxs-lookup"><span data-stu-id="0f047-106">We have created new, purpose-built forms in the **Fleet Management** module.</span></span> <span data-ttu-id="0f047-107">これらのフォームはモバイル アプリケーション専用に使用されており、Web クライアントからは使用されません。</span><span class="sxs-lookup"><span data-stu-id="0f047-107">These forms are used specifically for the mobile app and aren't meant to be used through the web client.</span></span>

1.  <span data-ttu-id="0f047-108">[フリート管理プロジェクトを含むファイルをダウンロードする](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.axpp ファイル)。</span><span class="sxs-lookup"><span data-stu-id="0f047-108">[Download the file that contains the Fleet Management project](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.axpp file).</span></span>
2.  <span data-ttu-id="0f047-109">ZIP ファイルの内容を開発用コンピュータの一時的な場所に抽出します。</span><span class="sxs-lookup"><span data-stu-id="0f047-109">Extract the contents of the zip file to a temporary location on the development computer.</span></span>
3.  <span data-ttu-id="0f047-110">Visual Studio を使用して、プロジェクト (.axpp) ファイルをインポートします (**Finance and Operations** &gt; **プロジェクトのインポート**をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="0f047-110">Import the project (.axpp) file by using Microsoft Visual Studio (click **Finance and Operations** &gt; **Import Project**).</span></span>
4.  <span data-ttu-id="0f047-111">プロジェクト ファイルをインポートした後は、プロジェクトまたはモジュールをビルドします。</span><span class="sxs-lookup"><span data-stu-id="0f047-111">After you've imported the project file, build the project or module.</span></span>

### <a name="get-the-sample-workspace"></a><span data-ttu-id="0f047-112">サンプル ワークスペースを取得します</span><span class="sxs-lookup"><span data-stu-id="0f047-112">Get the sample workspace</span></span>

<span data-ttu-id="0f047-113">引当管理のためのサンプルのワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="0f047-113">We provide a sample workspace for Reservation management.</span></span> <span data-ttu-id="0f047-114">このワークスペースは、**フリート管理**モジュールに基づいています。</span><span class="sxs-lookup"><span data-stu-id="0f047-114">This workspace is based on the **Fleet Management** module.</span></span>

1.  <span data-ttu-id="0f047-115">[サンプル ワークスペースを含むファイルをダウンロードする](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.xml ファイル)。</span><span class="sxs-lookup"><span data-stu-id="0f047-115">[Download the file that contains the sample workspace](https://github.com/Microsoft/Dynamics365-for-Operations-mobile-FleetManagementSamples) (.xml file).</span></span>
2.  <span data-ttu-id="0f047-116">非生産クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="0f047-116">Sign in to your non-production client.</span></span> <span data-ttu-id="0f047-117">(管理者としてログインする必要があります)。</span><span class="sxs-lookup"><span data-stu-id="0f047-117">(You must sign in as an administrator.)</span></span>
3.  <span data-ttu-id="0f047-118">アドレス バーで、**&mode=mobile** を URL の末尾に追加してから Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="0f047-118">In the address bar, add **&mode=mobile** to the end of the URL, and then press Enter.</span></span>
4.  <span data-ttu-id="0f047-119">クライアントで、**設定** &gt; **モバイル アプリ**と移動します。</span><span class="sxs-lookup"><span data-stu-id="0f047-119">In the client, go to **Settings** &gt; **Mobile app**.</span></span> <span data-ttu-id="0f047-120">モバイル アプリ デザイナーは、クライアントの横にドッキングして表示されます。</span><span class="sxs-lookup"><span data-stu-id="0f047-120">The mobile app designer will appear docked next to the client.</span></span>
5.  <span data-ttu-id="0f047-121">**オーバーフロー** ボタン (**…**) をクリックし、**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f047-121">Click the **Overflow** button (**…**), and then click **Import**.</span></span>
6.  <span data-ttu-id="0f047-122">ページの下部に表示される**参照**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f047-122">Click the **Browse** button that appears at the bottom of the page.</span></span>
7.  <span data-ttu-id="0f047-123">表示されるファイル選択ダイアログ ボックスで、以前に zip ファイルから抽出した XML ファイルのいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="0f047-123">In the file selection dialog box that appears, select one of the XML files that you previously extracted from the zip file.</span></span>
8.  <span data-ttu-id="0f047-124">アプリがモバイル アプリ デザイナーに読み込まれた後、ページの下部にある**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f047-124">After the app has been loaded into the mobile app designer, click **Done** at the bottom of the page.</span></span>
9.  <span data-ttu-id="0f047-125">**ワークスペースの公開**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f047-125">Click **Publish workspace**.</span></span>

### <a name="get-the-mobile-app"></a><span data-ttu-id="0f047-126">モバイル アプリの取得</span><span class="sxs-lookup"><span data-stu-id="0f047-126">Get the mobile app</span></span>

<span data-ttu-id="0f047-127">モバイル アプリは、最も一般的なモバイル オペレーティング システムで利用可能です。</span><span class="sxs-lookup"><span data-stu-id="0f047-127">The mobile app is being made available for the most popular mobile operating systems.</span></span> <span data-ttu-id="0f047-128">アプリケーションにログインするためには、Dynamics 365 Unified Operations のインスタンスと、有効なユーザー資格情報が必要です。</span><span class="sxs-lookup"><span data-stu-id="0f047-128">You must have a Dynamics 365 Unified Operations instance and valid user credentials in order to log in to the app.</span></span>

-   <span data-ttu-id="0f047-129">Android (現在利用可能) - [Google Play Store の Finance and Operations モバイル アプリ](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)</span><span class="sxs-lookup"><span data-stu-id="0f047-129">Android (available now) - [Finance and Operations mobile app on the Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)</span></span>
-   <span data-ttu-id="0f047-130">iPhone (現在利用可能) - [iTunes アプリ ストアの Finance and Operations モバイル アプリ](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)</span><span class="sxs-lookup"><span data-stu-id="0f047-130">iPhone (available now) - [Finance and Operations mobile app on the iTunes apps store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)</span></span>

<span data-ttu-id="0f047-131">完了です</span><span class="sxs-lookup"><span data-stu-id="0f047-131">You're done!</span></span> <span data-ttu-id="0f047-132">モバイル デバイスからアプリを起動してサンプル ワークスペースを表示します。</span><span class="sxs-lookup"><span data-stu-id="0f047-132">Launch the app from your mobile device to see the sample workspace.</span></span>

### <a name="additional-resources"></a><span data-ttu-id="0f047-133">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0f047-133">Additional resources</span></span>

[<span data-ttu-id="0f047-134">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="0f047-134">Architecture</span></span>](mobile-platform-architecture.md) 

[<span data-ttu-id="0f047-135">クライアント APIs リファレンス</span><span class="sxs-lookup"><span data-stu-id="0f047-135">Client APIs reference</span></span>](client-apis/client-apis-reference.md)

[<span data-ttu-id="0f047-136">サーバー APIs 参照</span><span class="sxs-lookup"><span data-stu-id="0f047-136">Server APIs reference</span></span>](mobile-workspace-server-apis.md)

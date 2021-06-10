---
title: POS 拡張機能の概要
description: このトピックでは、新しい独立した POS 拡張モデルおよびシールドされたソフトウェア開発キット (SDK) を使用して販売時点管理 (POS) 拡張機能を作成する方法に関する情報を提供します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 857d93d0ed9ee11615269d314ca4ed54a6ce4410
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984264"
---
# <a name="pos-extension-overview"></a><span data-ttu-id="ad3b2-103">POS 拡張機能の概要</span><span class="sxs-lookup"><span data-stu-id="ad3b2-103">POS extension overview</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="ad3b2-104">販売時点管理 (POS) アプリは、Retail ソフトウェア開発キット (SDK) のPOS拡張機能を使用して独自に拡張できます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-104">Point of Sale (POS) apps can be extended independently by using the POS extension feature of the Retail software development kit (SDK).</span></span> <span data-ttu-id="ad3b2-105">POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更、検証の追加、カスタム機能の追加を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-105">You can modify and create the POS user experience, enhance or modify out-of-box functionality, add validations, and add custom features.</span></span>

<span data-ttu-id="ad3b2-106">拡張機能は、次の方法で実現できます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-106">You can use extensions in the following ways:</span></span>

+ <span data-ttu-id="ad3b2-107">**POS ユーザー インターフェース (UI) の拡張:** ビューに応じて、カスタム列、アプリ バー ボタン、およびカスタム コントロールを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-107">**Extend the POS user interface (UI):** You can add custom columns, app bar buttons, and custom controls, depending on the view.</span></span> <span data-ttu-id="ad3b2-108">カート ビューとウェルカム ページは、画面レイアウト デザイナーを使用して構成することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-108">The cart view and the welcome page can be configured by using the screen layout designer.</span></span> <span data-ttu-id="ad3b2-109">他のビューは、カスタム コードを記述して拡張できます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-109">Other views can be extended by writing custom code.</span></span>
+ <span data-ttu-id="ad3b2-110">**POS ビジネス ロジックのオーバーライド:** POS 要求ハンドラーをオーバーライドして POS ビジネス ロジックを拡張し、カスタム ロジックを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-110">**Override POS business logic:** By overriding the POS request handlers, you can extend POS business logic to add custom logic.</span></span>
+ <span data-ttu-id="ad3b2-111">**プレトリガーとポストトリガー:** POS 操作の前または後にカスタム ロジックを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-111">**Add pre-triggers and post-triggers:** You can add custom logic before or after any POS operation.</span></span>
+ <span data-ttu-id="ad3b2-112">**API の使用:** POS によって、拡張機能のシナリオで使用できる API と ユーザー エクスペリエンス (UX) のコントロールが公開されます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-112">**Consume APIs:** POS exposes APIs and user experience (UX) controls that can be consumed in extension scenarios.</span></span>
+ <span data-ttu-id="ad3b2-113">**カスタム UX と API:** POS を拡張して、新しい機能や仕様をサポートするカスタム ビューおよび API を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-113">**Add custom UX and APIs:** You can extend POS to add custom views and APIs that support new functionality and features.</span></span>
+ <span data-ttu-id="ad3b2-114">**カスタム操作の追加:** カスタム操作を追加してカスタム機能を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-114">**Add custom operations:** You can add custom operations to perform custom functionality.</span></span>

<span data-ttu-id="ad3b2-115">次のトピックでは、独立した POS 拡張モデルおよびシールド SDK を使用して POS 拡張機能を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-115">The following topics explain how to create a POS extension by using the independent POS extension model and sealed SDK.</span></span>

+ [<span data-ttu-id="ad3b2-116">POS 拡張機能の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="ad3b2-116">Getting started with POS extensions</span></span>](pos-extension-getting-started.md)
+ [<span data-ttu-id="ad3b2-117">POS 拡張機能パッケージ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="ad3b2-117">Create a POS extension package project</span></span>](create-pos-extension-package.md)
+ [<span data-ttu-id="ad3b2-118">Modern POS 拡張パッケージの .appx ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="ad3b2-118">Create an .appx file for a Modern POS extension package</span></span>](create-pos-extension-appx.md)
+ [<span data-ttu-id="ad3b2-119">POS 拡張機能のデバッグ</span><span class="sxs-lookup"><span data-stu-id="ad3b2-119">Debug POS extensions</span></span>](debug-pos-extension.md)

<span data-ttu-id="ad3b2-120">このトピックは、Retail SDK 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-120">This topic applies to version 10.0.18 and later of the Retail SDK.</span></span>

## <a name="supported-apps"></a><span data-ttu-id="ad3b2-121">対応アプリ</span><span class="sxs-lookup"><span data-stu-id="ad3b2-121">Supported apps</span></span>

<span data-ttu-id="ad3b2-122">POS アプリは異なっていても、コード ベースは同じです。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-122">The different POS apps have the same code base.</span></span> <span data-ttu-id="ad3b2-123">ただし、プラットフォームとアプリ タイプに応じて、拡張機能のパッケージ化、配置、および表示の方法が異なります。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-123">However, the extensions are packaged, deployed, and rendered differently, depending on the platform and the app type.</span></span> <span data-ttu-id="ad3b2-124">作成したカスタマイズは、異なるアプリのコードの複製または書き直しの要求を行わずに、アプリ タイプ全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-124">Customizations that you develop will work across app types without requiring that the code is duplicated or rewritten for different apps.</span></span> <span data-ttu-id="ad3b2-125">拡張機能コンポーネントがアプリ固有のものである場合がありますが、拡張機能コードの大部分はアプリ全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-125">Although some extension components might be app-specific, most of the extension code can work across apps.</span></span>

<span data-ttu-id="ad3b2-126">次の表に、POS 拡張機能を作成できるアプリを示します。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-126">The following table shows that apps that you can create POS extensions for.</span></span>

| <span data-ttu-id="ad3b2-127"> アプリ</span><span class="sxs-lookup"><span data-stu-id="ad3b2-127">App</span></span> | <span data-ttu-id="ad3b2-128">説明</span><span class="sxs-lookup"><span data-stu-id="ad3b2-128">Description</span></span> |
|---|---|
| <span data-ttu-id="ad3b2-129">販売時点管理 (POS)</span><span class="sxs-lookup"><span data-stu-id="ad3b2-129">Point of Sale (POS)</span></span> | <span data-ttu-id="ad3b2-130">POS により、レジ担当者、販売在庫担当者、在庫担当者、店長など、第一線の作業者がさまざまなコマース操作を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-130">POS lets first-line workers, such as cashiers, sales and inventory associates, stock clerks, and store managers, perform various commerce operations.</span></span> <span data-ttu-id="ad3b2-131">Microsoft Dynamics 365 Commerce ソリューションは、これらの操作をプラットフォームおよびフォーム ファクター間で実行できるように、さまざまなデバイス タイプを提供します。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-131">The Microsoft Dynamics 365 Commerce solution provides different device types, so that these operations can be performed across platforms and form factors.</span></span> |
| <span data-ttu-id="ad3b2-132">Modern 販売時点管理 (MPOS)</span><span class="sxs-lookup"><span data-stu-id="ad3b2-132">Modern Point of Sale (MPOS)</span></span> | <span data-ttu-id="ad3b2-133">MPOS は、Windows デバイスで実行されるユニバーサル Windows プラットフォーム (UTC) アプリです。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-133">MPOS is a Universal Windows Platform (UWP) app that runs on a Windows device.</span></span> <span data-ttu-id="ad3b2-134">MPOS クライアントは、Hardware Station を使用して、キャッシュ ドロワー、クレジット カード リーダー、プリンターなどの周辺機器とも通信できます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-134">The MPOS client can communicate with peripheral devices, such as cash drawers, credit card readers, and printers, by using Hardware Station.</span></span> |
| <span data-ttu-id="ad3b2-135">クラウド販売時点管理 (CPOS)</span><span class="sxs-lookup"><span data-stu-id="ad3b2-135">Cloud Point of Sale (CPOS)</span></span> | <span data-ttu-id="ad3b2-136">CPOS は、ブラウザーで実行される POS のホストされたバージョンです。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-136">CPOS is a hosted version of POS that runs in a browser.</span></span> <span data-ttu-id="ad3b2-137">CPOS アプリは、クラウドに配置されます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-137">The CPOS app is deployed in the cloud.</span></span> |
| <span data-ttu-id="ad3b2-138">Store Commerce</span><span class="sxs-lookup"><span data-stu-id="ad3b2-138">Store Commerce</span></span> | <span data-ttu-id="ad3b2-139">Dynamics 365 Commerce の Store Commerce アプリは、Windows デバイスで実行される Microsoft Store からの Windows アプリです。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-139">The Store Commerce app in Dynamics 365 Commerce is a Windows app from Microsoft Store that runs on a Windows device.</span></span> <span data-ttu-id="ad3b2-140">アプリの表示には、Curomium エンジンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-140">The Chromium engine is used to render the app.</span></span> <span data-ttu-id="ad3b2-141">Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-141">The Chromium engine has better rendering performance than the native JavaScript UWP app in Windows.</span></span> <span data-ttu-id="ad3b2-142">Store Commerce が MPOS と完全に同等の機能を持つようになった場合、MPOS は置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-142">When Store Commerce has full functional parity with MPOS, it will replace MPOS.</span></span> <span data-ttu-id="ad3b2-143">現時点では、Store Commerce はオフラインでの実行をサポートしません (Retail Server への接続がない場合)。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-143">Currently, Store Commerce doesn't support running offline (when there is no connectivity to Retail Server).</span></span> |
| <span data-ttu-id="ad3b2-144">iOS ハイブリッド アプリ</span><span class="sxs-lookup"><span data-stu-id="ad3b2-144">iOS hybrid app</span></span> | <span data-ttu-id="ad3b2-145">iOS ハイブリッド アプリは iOS デバイスで実行されるシェル アプリ (ラッパー) です。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-145">The iOS hybrid app is a shell app (wrapper) that runs on an iOS device.</span></span> <span data-ttu-id="ad3b2-146">シェルで CPOS をホストします。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-146">The shell hosts CPOS.</span></span> |
| <span data-ttu-id="ad3b2-147">Android ハイブリッド アプリ</span><span class="sxs-lookup"><span data-stu-id="ad3b2-147">Android hybrid app</span></span> | <span data-ttu-id="ad3b2-148">Android ハイブリッド アプリは Android デバイスで実行されるシェル アプリです。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-148">The Android hybrid app is a shell app that runs on an Android device.</span></span> <span data-ttu-id="ad3b2-149">シェルで CPOS をホストします。</span><span class="sxs-lookup"><span data-stu-id="ad3b2-149">The shell hosts CPOS.</span></span> |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

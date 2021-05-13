---
title: POS 拡張機能の概要
description: このトピックでは、新しい独立した POS 拡張モデルおよびシールド SDK を使用して POS 拡張機能を作成する方法について説明します。
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
ms.openlocfilehash: 26857a258f313cd5197292328b69ca075d699014
ms.sourcegitcommit: fd15b02fc9caa1c05e56abdc276a7f4b23b0d8f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5960152"
---
# <a name="point-of-sale-pos-extension-overview"></a><span data-ttu-id="3227f-103">販売時点管理 (POS) 拡張機能の概要</span><span class="sxs-lookup"><span data-stu-id="3227f-103">Point of Sale (POS) extension overview</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="3227f-104">Retail SDK の POS 拡張機能を使用して、POS アプリケーションを個別に拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="3227f-104">A POS application can be extended independently by using the POS extension feature of the Retail SDK.</span></span> <span data-ttu-id="3227f-105">POS のユーザー エクスペリエンスの変更と作成、標準の機能拡張または変更の実行、検証の追加、カスタム機能の追加を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3227f-105">You can modify and create the POS user experience, make out-of-box functional enhancements or modifications, add validations, and add custom features.</span></span> <span data-ttu-id="3227f-106">拡張機能を使用すると、次のことが可能です。</span><span class="sxs-lookup"><span data-stu-id="3227f-106">Using extensions, you can:</span></span>

+ <span data-ttu-id="3227f-107">POS UI の拡張: ビューに応じて、カスタム列、アプリ バー ボタン、およびカスタム コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="3227f-107">Extend the POS UI: Add custom columns, app bar buttons, and custom controls depending on the view.</span></span> <span data-ttu-id="3227f-108">画面レイアウト デザイナーを使用した、カート ビューとようこそ画面サポートの構成。</span><span class="sxs-lookup"><span data-stu-id="3227f-108">The cart view and the welcome screen support configuration using the screen layout designer.</span></span> <span data-ttu-id="3227f-109">他のビューは、カスタム コードを記述して拡張できます。</span><span class="sxs-lookup"><span data-stu-id="3227f-109">Other views can be extended by writing custom code.</span></span>
+ <span data-ttu-id="3227f-110">POS ビジネス ロジックのオーバーライド: POS ビジネス ロジックを拡張し、POS 要求ハンドラーをオーバーライドしてカスタム ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="3227f-110">Override POS business logic: Extend POS business logic to add custom logic by overriding the POS request handlers.</span></span>
+ <span data-ttu-id="3227f-111">プレトリガーとポストトリガー: POS 操作の前または後にカスタム ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="3227f-111">Pre- and post-triggers: Add custom logic before or after any POS operation.</span></span>
+ <span data-ttu-id="3227f-112">APIの使用: POS によって、拡張機能のシナリオで使用できる API と UX のコントロールが公開されます。</span><span class="sxs-lookup"><span data-stu-id="3227f-112">Consume APIs: POS exposes APIs and UX controls that can be consumed in extension scenarios.</span></span>
+ <span data-ttu-id="3227f-113">カスタム UX と API: POS を拡張してカスタム ビューおよび API を追加し、新しい機能と特徴をサポートします。</span><span class="sxs-lookup"><span data-stu-id="3227f-113">Custom UX and APIs: Extend POS to add custom views and APIs to support new functionalities and features.</span></span>
+ <span data-ttu-id="3227f-114">カスタム操作: カスタム操作を追加してカスタム機能を実行します。</span><span class="sxs-lookup"><span data-stu-id="3227f-114">Custom operations: Add custom operations to perform custom functionalities.</span></span>

<span data-ttu-id="3227f-115">これらのトピックでは、独立した POS 拡張モデルおよびシールド SDK を使用して POS 拡張機能を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3227f-115">These topics explain how to create a POS extension using the independent POS extension model and sealed SDK.</span></span> <span data-ttu-id="3227f-116">このトピックは、Retail ソフトウェア開発キット (SDK) バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3227f-116">This topic applies to Retail software development kit (SDK) version 10.0.18 and later.</span></span>

+ [<span data-ttu-id="3227f-117">POS 拡張機能を開始する</span><span class="sxs-lookup"><span data-stu-id="3227f-117">Getting started with POS extensions</span></span>](pos-extension-getting-started.md)
+ [<span data-ttu-id="3227f-118">POS 拡張機能パッケージ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="3227f-118">Create a POS extension package project</span></span>](create-pos-extension-package.md)
+ [<span data-ttu-id="3227f-119">Modern POS 拡張 appx ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="3227f-119">Create a Modern POS extension appx file</span></span>](create-pos-extension-appx.md)
+ [<span data-ttu-id="3227f-120">POS 拡張機能のデバッグ</span><span class="sxs-lookup"><span data-stu-id="3227f-120">Debug a POS extension</span></span>](debug-pos-extension.md)

## <a name="supported-apps"></a><span data-ttu-id="3227f-121">対応アプリ</span><span class="sxs-lookup"><span data-stu-id="3227f-121">Supported apps</span></span>

<span data-ttu-id="3227f-122">コード ベースは異なる POS アプリケーションでも同じですが、拡張機能のパッケージ化、配置方法、および表示方法は、プラットフォームとアプリ タイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3227f-122">The code base is same for the different POS applications but how the extensions are packaged, deployed, and rendered varies by platform and the app type.</span></span> <span data-ttu-id="3227f-123">作成したカスタマイズは、異なるアプリのコードの複製または書き直しを行わずに、異なるアプリ タイプで使用できす。</span><span class="sxs-lookup"><span data-stu-id="3227f-123">Customizations that you develop work across different app types without duplicating or rewriting the code for different apps.</span></span> <span data-ttu-id="3227f-124">アプリ固有の拡張機能コンポーネントが存在する場合がありますが、拡張機能コードの大部分はアプリ全体で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3227f-124">There may be some extension components that are app-specific, but most of the extension code can work across apps.</span></span>

<span data-ttu-id="3227f-125">次の表にあるアプリの POS 拡張機能を作成できます。</span><span class="sxs-lookup"><span data-stu-id="3227f-125">You can create POS extensions for the apps in the following table.</span></span>

<span data-ttu-id="3227f-126"> アプリ</span><span class="sxs-lookup"><span data-stu-id="3227f-126">App</span></span> | <span data-ttu-id="3227f-127">説明</span><span class="sxs-lookup"><span data-stu-id="3227f-127">Description</span></span>
---|---
<span data-ttu-id="3227f-128">販売時点管理 (POS)</span><span class="sxs-lookup"><span data-stu-id="3227f-128">Point of Sale (POS)</span></span> | <span data-ttu-id="3227f-129">POS では、レジ担当者、販売在庫担当者、在庫担当者、店長など、第一線の作業者がさまざまなコマース操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="3227f-129">POS allows first-line workers, such as cashiers, sales and inventory associates, stock clerks, and store managers to perform various commerce operations.</span></span> <span data-ttu-id="3227f-130">Dynamics 365 Commerce ソリューションは、これらの操作をプラットフォームおよびフォーム ファクター間で実行するためのさまざまなデバイス タイプを提供します。</span><span class="sxs-lookup"><span data-stu-id="3227f-130">The Dynamics 365 Commerce solution provides different device types to perform these operations across platform and form factors.</span></span>
<span data-ttu-id="3227f-131">Modern 販売時点管理 (MPOS)</span><span class="sxs-lookup"><span data-stu-id="3227f-131">Modern-Point of Sale (MPOS)</span></span> | <span data-ttu-id="3227f-132">MPOS は、Windows デバイスで実行されるユニバーサル Windows プラットフォーム (UTC) アプリです。</span><span class="sxs-lookup"><span data-stu-id="3227f-132">MPOS is a Universal Windows Platform (UWP) app that runs on a Windows device.</span></span> <span data-ttu-id="3227f-133">MPOS クライアントは、Hardware Station を使用して、キャッシュ ドロワー、クレジット カード リーダー、プリンターなどの周辺機器とも通信できます。</span><span class="sxs-lookup"><span data-stu-id="3227f-133">The MPOS client can communicate with peripheral devices, such as cash drawers, credit card readers, and printers, by using Hardware Station.</span></span>
<span data-ttu-id="3227f-134">クラウド販売時点管理 (CPOS)</span><span class="sxs-lookup"><span data-stu-id="3227f-134">Cloud Point of Sale (CPOS)</span></span> | <span data-ttu-id="3227f-135">CPOS は、ブラウザで実行される POS のホストされたバージョンです。</span><span class="sxs-lookup"><span data-stu-id="3227f-135">CPOS is a hosted version of the POS that runs in the browser.</span></span> <span data-ttu-id="3227f-136">CPOS アプリは、クラウドに配置されます。</span><span class="sxs-lookup"><span data-stu-id="3227f-136">The CPOS app is deployed in the cloud.</span></span>
<span data-ttu-id="3227f-137">Store Commerce</span><span class="sxs-lookup"><span data-stu-id="3227f-137">Store Commerce</span></span> | <span data-ttu-id="3227f-138">Microsoft Dynamics 365 Commerce の Store Commerce アプリは、Windows デバイスで実行される Microsoft Store からの Windows アプリです。</span><span class="sxs-lookup"><span data-stu-id="3227f-138">Store Commerce app in Microsoft Dynamics 365 Commerce is a Windows app from the Microsoft Store that runs on a Windows device.</span></span> <span data-ttu-id="3227f-139">Store Commerce アプリでは、アプリを表示するのに Chromium エンジンを使用します。</span><span class="sxs-lookup"><span data-stu-id="3227f-139">The Store Commerce app uses the Chromium engine to render the app.</span></span> <span data-ttu-id="3227f-140">Chromium エンジンは、Windows の ネイティブの JavaScript UWP アプリよりも表示パフォーマンスが優れています。</span><span class="sxs-lookup"><span data-stu-id="3227f-140">The Chromium engine has better rendering performance than the native JavaScript UWP app in Windows.</span></span> <span data-ttu-id="3227f-141">Store Commerce が MPOS と完全に同等の機能を持つようになった場合、Store Commerce は MPOS に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="3227f-141">Store Commerce will replace MPOS when Store Commerce has full functional parity with MPOS.</span></span> <span data-ttu-id="3227f-142">現時点では、Store Commerce はオフラインでの実行をサポートしません (Retail Server への接続がない場合)。</span><span class="sxs-lookup"><span data-stu-id="3227f-142">Currently, Store Commerce doesn't support running offline (when there is no connectivity to Retail Server).</span></span>
<span data-ttu-id="3227f-143">iOS ハイブリッド アプリ</span><span class="sxs-lookup"><span data-stu-id="3227f-143">iOS hybrid app</span></span> | <span data-ttu-id="3227f-144">iOS ハイブリッド アプリは iOS デバイスで実行されるシェル アプリ (ラッパー) です。</span><span class="sxs-lookup"><span data-stu-id="3227f-144">The iOS hybrid app is a shell app (wrapper) that runs on an iOS device.</span></span> <span data-ttu-id="3227f-145">シェルで CPOS をホストします。</span><span class="sxs-lookup"><span data-stu-id="3227f-145">The shell hosts CPOS.</span></span>
<span data-ttu-id="3227f-146">Android ハイブリッド アプリ</span><span class="sxs-lookup"><span data-stu-id="3227f-146">Android hybrid app</span></span> | <span data-ttu-id="3227f-147">Android ハイブリッド アプリは Android デバイスで実行されるシェル アプリです。</span><span class="sxs-lookup"><span data-stu-id="3227f-147">The Android hybrid app is a shell app that runs on an Android device.</span></span> <span data-ttu-id="3227f-148">シェルで CPOS をホストします。</span><span class="sxs-lookup"><span data-stu-id="3227f-148">The shell hosts CPOS.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

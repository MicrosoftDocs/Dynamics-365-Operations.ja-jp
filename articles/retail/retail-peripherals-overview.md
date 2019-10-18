---
title: 小売周辺機器
description: このトピックでは、小売周辺機器に関連する概念を説明します。
author: rubencdelgado
manager: AnnBe
ms.date: 01/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, RetailDevice, RetailHardwareProfile
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cf4eb74acbd305eb67861ab3f09648bf8af8f86c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025056"
---
# <a name="retail-peripherals"></a><span data-ttu-id="a2146-103">小売周辺機器</span><span class="sxs-lookup"><span data-stu-id="a2146-103">Retail peripherals</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a2146-104">このトピックでは、小売周辺機器に関連する概念を説明します。</span><span class="sxs-lookup"><span data-stu-id="a2146-104">This topic explains the concepts that are related to retail peripherals.</span></span> <span data-ttu-id="a2146-105">周辺機器を販売時点管理 (POS) と接続するさまざまな方法、および POS との接続の管理を担当するコンポーネントについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a2146-105">It describes the various ways that peripherals can be connected to the point of sale (POS) and the components that are responsible for managing the connection with the POS.</span></span>

## <a name="concepts"></a><span data-ttu-id="a2146-106">概念</span><span class="sxs-lookup"><span data-stu-id="a2146-106">Concepts</span></span>

### <a name="pos-registers"></a><span data-ttu-id="a2146-107">POS レジスター</span><span class="sxs-lookup"><span data-stu-id="a2146-107">POS registers</span></span>

<span data-ttu-id="a2146-108">ナビゲーション: **小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **レジスター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-108">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="a2146-109">販売時点管理 (POS) レジは、POS の特定のインスタンスの特性を定義するのに使用するエンティティです。</span><span class="sxs-lookup"><span data-stu-id="a2146-109">The point of sale (POS) register is an entity that is used to define the characteristics of a specific instance of the POS.</span></span> <span data-ttu-id="a2146-110">これらの特性には、レジスターで使用される小売周辺機器のハードウェア プロファイルまたはセットアップ、レジスターがマップされているストア、そのレジスターにログオンしているユーザーのビジュアル エクスペリエンスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2146-110">These characteristics include the hardware profile or setup for retail peripherals that will be used at the register, the store that the register is mapped to, and the visual experience for the user who signs in to that register.</span></span>

### <a name="devices"></a><span data-ttu-id="a2146-111">デバイス</span><span class="sxs-lookup"><span data-stu-id="a2146-111">Devices</span></span>

<span data-ttu-id="a2146-112">ナビゲーション: **小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **デバイス** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-112">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**.</span></span> <span data-ttu-id="a2146-113">デバイスとは、POS レジスターにマップされているデバイスの物理的なインスタンスを表すエンティティです。</span><span class="sxs-lookup"><span data-stu-id="a2146-113">A device is an entity that represents a physical instance of a device that is mapped to a POS register.</span></span> <span data-ttu-id="a2146-114">デバイスが作成されると、POS レジスターにマップされます。</span><span class="sxs-lookup"><span data-stu-id="a2146-114">When a device is created, it's mapped to a POS register.</span></span> <span data-ttu-id="a2146-115">デバイス エンティティは、POS レジスターが有効化された時間、使用しているクライアントのタイプ、および特定のデバイスに配置されているアプリケーション パッケージに関する情報を追跡します。</span><span class="sxs-lookup"><span data-stu-id="a2146-115">The device entity tracks information about when a POS register is activated, the type of client that is being used, and the application package that has been deployed to a specific device.</span></span> <span data-ttu-id="a2146-116">デバイスは、次のアプリケーション タイプにマップすることができます: Retail Modern POS、Retail Cloud POS、Retail Modern POS – Windows Phone、Retail Modern POS – Android、および Retail Modern POS – iOS。</span><span class="sxs-lookup"><span data-stu-id="a2146-116">Devices can be mapped to the following application types: Retail Modern POS, Retail Cloud POS, Retail Modern POS – Windows Phone, Retail Modern POS – Android, and Retail Modern POS – iOS.</span></span>

### <a name="retail-modern-pos"></a><span data-ttu-id="a2146-117">Retail Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-117">Retail Modern POS</span></span>

<span data-ttu-id="a2146-118">Modern POS は、Microsoft Windows の POS プログラムです。</span><span class="sxs-lookup"><span data-stu-id="a2146-118">Modern POS is the POS program for Microsoft Windows.</span></span> <span data-ttu-id="a2146-119">これは、Windows 10 オペレーティング システム (OS) に配置できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-119">It can be deployed on Windows 10 operating systems (OSs).</span></span>

### <a name="cloud-pos"></a><span data-ttu-id="a2146-120">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="a2146-120">Cloud POS</span></span>

<span data-ttu-id="a2146-121">クラウド POS は Modern POS プログラムのブラウザ ベースのバージョンで、Web ブラウザでアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a2146-121">Cloud POS is a browser-based version of the Modern POS program that can be accessed in a web browser.</span></span>

### <a name="modern-pos-for-ios"></a><span data-ttu-id="a2146-122">iOS 用 Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-122">Modern POS for iOS</span></span>

<span data-ttu-id="a2146-123">iOS 用 Modern POS は iOS ベース バージョンの Modern POS で、iOS デバイスに配置できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-123">Modern POS for iOS is an iOS-based version of the Modern POS program that can be deployed on iOS devices.</span></span>

### <a name="modern-pos-for-android"></a><span data-ttu-id="a2146-124">Android 用 Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-124">Modern POS for Android</span></span>

<span data-ttu-id="a2146-125">Android 用 Modern POS は Android ベース バージョンの Modern POS で、Android デバイスに配置できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-125">Modern POS for Android is an Android-based version of the Modern POS program that can be deployed on Android devices.</span></span>

### <a name="pos-peripherals"></a><span data-ttu-id="a2146-126">POS 周辺機器</span><span class="sxs-lookup"><span data-stu-id="a2146-126">POS peripherals</span></span>

<span data-ttu-id="a2146-127">POS 周辺機器は、POS 機能用に明示的にサポートされているデバイスです。</span><span class="sxs-lookup"><span data-stu-id="a2146-127">POS peripherals are devices that are explicitly supported for POS functions.</span></span> <span data-ttu-id="a2146-128">これらの周辺機器は、特定のクラスに分けられます。</span><span class="sxs-lookup"><span data-stu-id="a2146-128">These peripherals are typically divided into specific classes.</span></span> <span data-ttu-id="a2146-129">これらのクラスに関する詳細については、このトピックの「デバイス クラス」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-129">For more information about these classes, see the "Device classes" section of this topic.</span></span>

### <a name="hardware-station"></a><span data-ttu-id="a2146-130">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="a2146-130">Hardware station</span></span>

<span data-ttu-id="a2146-131">ナビゲーション: **小売** &gt; **チャネル** &gt; **小売店舗** &gt; **すべての小売店舗**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-131">Navigation: Click **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span> <span data-ttu-id="a2146-132">店舗を選択して、**ハードウェア ステーション** クイック タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-132">Select a store, and then click the **Hardware stations** FastTab.</span></span> <span data-ttu-id="a2146-133">**ハードウェア ステーション** 設定は、小売周辺機器ロジックを配置するインスタンスを定義するのに使用されるチャンネル レベルの設定です。</span><span class="sxs-lookup"><span data-stu-id="a2146-133">The **Hardware station** setting is a channel-level setting that is used to define instances where the retail peripheral logic will be deployed.</span></span> <span data-ttu-id="a2146-134">チャンネル レベルのこの設定は、ハードウェア ステーションの特性を決定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-134">This setting at the channel level is used to determine characteristics of the hardware station.</span></span> <span data-ttu-id="a2146-135">また、特定の店舗で Modern POS インスタンスに使用するハードウェア ステーションを一覧表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-135">It's also used to list hardware stations that are available for a Modern POS instance in a given store.</span></span> <span data-ttu-id="a2146-136">ハードウェア ステーションは、Windows 用 Modern POS プログラムに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="a2146-136">The hardware station is built into the Modern POS program for Windows.</span></span> <span data-ttu-id="a2146-137">ハードウェア ステーションは、Microsoft インターネット インフォメーション サービス (IIS) のスタンドアロン プログラムとして別に配置することもできます。</span><span class="sxs-lookup"><span data-stu-id="a2146-137">The hardware station can also be deployed independently as a stand-alone Microsoft Internet Information Services (IIS) program.</span></span> <span data-ttu-id="a2146-138">この場合は、ネットワークからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a2146-138">In this case, it can be accessed via a network.</span></span>

### <a name="hardware-profile"></a><span data-ttu-id="a2146-139">ハードウェア プロファイル</span><span class="sxs-lookup"><span data-stu-id="a2146-139">Hardware profile</span></span>

<span data-ttu-id="a2146-140">ナビゲーション: **小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-140">Navigation: Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="a2146-141">ハードウェア プロファイルは、POS レジスター用またはハードウェア ステーション用にコンフィギュレーションされているデバイスのリストです。</span><span class="sxs-lookup"><span data-stu-id="a2146-141">The hardware profile is a list of devices that are configured for a POS register or a hardware station.</span></span> <span data-ttu-id="a2146-142">ハードウェア プロファイルは、POS レジスターまたはハードウェア ステーションに直接マップできます。</span><span class="sxs-lookup"><span data-stu-id="a2146-142">The hardware profile can be mapped directly to a POS register or a hardware station.</span></span>

## <a name="devices-classes"></a><span data-ttu-id="a2146-143">デバイス クラス</span><span class="sxs-lookup"><span data-stu-id="a2146-143">Devices classes</span></span>
<span data-ttu-id="a2146-144">POS 周辺機器は、クラスに分けられています。</span><span class="sxs-lookup"><span data-stu-id="a2146-144">POS peripherals are typically divided into classes.</span></span> <span data-ttu-id="a2146-145">このセクションでは、Modern POS をサポートするデバイスの概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="a2146-145">This section describes and gives an overview of the devices that Modern POS supports.</span></span>

### <a name="printer"></a><span data-ttu-id="a2146-146">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-146">Printer</span></span>

<span data-ttu-id="a2146-147">プリンタには、従来型の POS レシート プリンターおよび全ページ プリンタが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2146-147">Printers include traditional POS receipt printers and full-page printers.</span></span> <span data-ttu-id="a2146-148">プリンタは、Retail POS 用 Object linking and embedding (OPOS) および Microsoft Windows ドライバ インターフェースを通してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a2146-148">Printer are supported through Object Linking and Embedding for Retail POS (OPOS) and Microsoft Windows driver interfaces.</span></span> <span data-ttu-id="a2146-149">2 つまでのプリンタを同時に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-149">Up to two printers can be used at the same time.</span></span> <span data-ttu-id="a2146-150">この機能により、現金店頭払いの顧客のレシートがレシート プリンタで印刷されるている間に、詳細情報を伴う顧客の注文全体が別のプリンタで印刷されるというシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-150">This capability supports scenarios where cash-and-carry customer receipts are printed on receipt printers, whereas customer orders, which carry more information, are printed on a full-page printer.</span></span> <span data-ttu-id="a2146-151">レシート プリンタは、コンピュータに USB で直接接続するか、ネットワークにイーサネットで接続するか、または Bluetooth で接続できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-151">Receipt printers can be connected directly to a computer via USB, connected to a network via Ethernet, or connected via Bluetooth.</span></span>

### <a name="scanner"></a><span data-ttu-id="a2146-152">スキャナー</span><span class="sxs-lookup"><span data-stu-id="a2146-152">Scanner</span></span>

<span data-ttu-id="a2146-153">2 つまでのバーコード スキャナーを同時に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-153">Up to two bar code scanners can be used at the same time.</span></span> <span data-ttu-id="a2146-154">この機能により、チェック アウトの時間の時間短縮のため、大きなあるいは重い品目のスキャンのために携帯式のスキャナーが必要で、同時にほとんどの標準サイズの品目に対しては固定埋め込みスキャナーを使用する場合のシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-154">This capability supports scenarios where a scanner that is more mobile is required in order to scan large or heavy items, whereas a fixed embedded scanner is used for most standard-sized items, to speed up checkout times.</span></span> <span data-ttu-id="a2146-155">スキャナーは、OPOS、Universal Windows Platform (UWP)、またはキーボード ウェッジ インターフェイスでサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a2146-155">Scanners can be supported through OPOS, Universal Windows Platform (UWP), or keyboard wedge interfaces.</span></span> <span data-ttu-id="a2146-156">スキャナーをコンピューターに接続するために、USB または Bluetooth も使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-156">USB or Bluetooth can be used to connect a scanner to a computer.</span></span>

### <a name="msr"></a><span data-ttu-id="a2146-157">MSR</span><span class="sxs-lookup"><span data-stu-id="a2146-157">MSR</span></span>

<span data-ttu-id="a2146-158">OPOS ドライバを使用して、1 つの USB 磁気ストライプ リーダー (MSR) を設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-158">One USB magnetic stripe reader (MSR) can be set up by using OPOS drivers.</span></span> <span data-ttu-id="a2146-159">電子決済 (EFT) の支払トランザクションにスタンドアロン MSR を使用する場合、MSR は支払コネクタで管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-159">If you want to use a stand-alone MSR for electronic funds transfer (EFT) payment transactions, the MSR must be managed by a payment connector.</span></span> <span data-ttu-id="a2146-160">支払コネクタとは別のスタンドアロン MSR は、顧客ロイヤルティ エントリ、従業員のサインイン、およびギフト カード エントリに使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-160">Stand-alone MSRs can be used for customer loyalty entry, employee sign-in, and gift card entry, independently of the payment connector.</span></span>

### <a name="cash-drawer"></a><span data-ttu-id="a2146-161">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-161">Cash drawer</span></span>

<span data-ttu-id="a2146-162">ハードウェア プロファイルごとに、2 つのキャッシュ ドロワーをサポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a2146-162">Two cash drawers can be supported per hardware profile.</span></span> <span data-ttu-id="a2146-163">この機能により、レジスターごとに 2 つの有効なシフトを同時に使用することが可能になります。</span><span class="sxs-lookup"><span data-stu-id="a2146-163">This capability enables two active shifts per register to be available at the same time.</span></span> <span data-ttu-id="a2146-164">共有シフトの場合、または複数のモバイル POS デバイスでキャッシュ ドロワーを同時に使用する場合、ハードウェア プロファイルごとに 1 つのキャッシュ ドロワーのみが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a2146-164">In the case of a shared shift, or a cash drawer that is used by multiple mobile POS devices at the same time, only one cash drawer is allowed per hardware profile.</span></span> <span data-ttu-id="a2146-165">キャッシュ ドロワーは、コンピュータに USB で直接接続するか、ネットワークにイーサネットで接続するか、またはレシート プリンターに RJ12 インターフェースで接続できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-165">Cash drawers can be connected directly to a computer via USB, connected to a network, or connected to a receipt printer via an RJ12 interface.</span></span> <span data-ttu-id="a2146-166">場合によっては、キャッシュ ドロワーは Bluetooth でも接続できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-166">In some cases, cash drawers can also be connected via Bluetooth.</span></span>

### <a name="line-display"></a><span data-ttu-id="a2146-167">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="a2146-167">Line display</span></span>

<span data-ttu-id="a2146-168">ライン ディスプレイは、製品、トランザクションの残高などの必要な情報をトランザクションの間に顧客に示すのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-168">Line displays are used to show products, transaction balances, and other useful information to the customer during a transaction.</span></span> <span data-ttu-id="a2146-169">1 つのライン ディスプレイは、OPOS ドライバーを使用して USB でコンピュータに接続できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-169">One line display can be connected to the computer via USB by using OPOS drivers.</span></span>

### <a name="signature-capture"></a><span data-ttu-id="a2146-170">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="a2146-170">Signature capture</span></span>

<span data-ttu-id="a2146-171">署名の取得デバイスは、OPOS ドライバを使用して USB で直接コンピュータに接続できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-171">Signature capture devices can be connected directly to a computer via USB by using OPOS drivers.</span></span> <span data-ttu-id="a2146-172">署名の取得デバイスが設定されている場合、顧客はデバイスに署名するように要求されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-172">When signature capture is configured, the customer is prompted to sign on the device.</span></span> <span data-ttu-id="a2146-173">署名がなされると、承認用にレジ担当者に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-173">After the signature is provided, it's shown to the cashier for acceptance.</span></span>

### <a name="scale"></a><span data-ttu-id="a2146-174">スケール</span><span class="sxs-lookup"><span data-stu-id="a2146-174">Scale</span></span>

<span data-ttu-id="a2146-175">スケールは、OPOS ドライバーを使用して USP でコンピュータに接続できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-175">Scales can be connected to the computer via USP by using OPOS drivers.</span></span> <span data-ttu-id="a2146-176">「計量」製品とマークされた製品がトランザクションに追加されると、POS は スケールの重量を読み、トランザクションに製品を追加し、スケールから得られる数値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a2146-176">When a product that is marked as a "Weighed" product is added to a transaction, the POS reads the weight from the scale, adds the product to the transaction, and uses the quantity that the scale provided.</span></span>

### <a name="pin-pad"></a><span data-ttu-id="a2146-177">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="a2146-177">PIN pad</span></span>

<span data-ttu-id="a2146-178">個人 ID 番号 (PIN) パッドは、OPOS でサポートされますが、支払コネクタで管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-178">Personal identification number (PIN) pads are supported through OPOS, but they must be managed via a payment connector.</span></span>

### <a name="secondary-display"></a><span data-ttu-id="a2146-179">二次表示</span><span class="sxs-lookup"><span data-stu-id="a2146-179">Secondary display</span></span>

<span data-ttu-id="a2146-180">二次表示が設定された場合、基本情報は 2 番目の Windows ディスプレイに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-180">When a secondary display is configured, the number 2 Windows display is used to show basic information.</span></span> <span data-ttu-id="a2146-181">二次表示の目的は、独立系ソフトウェア ベンダー (ISV) による拡張をサポートすることです。追加設定なしの場合、二次表示はコンフィギュレーション不可能で、限定的な内容しか表示しません。</span><span class="sxs-lookup"><span data-stu-id="a2146-181">The purpose of the secondary display is to support independent software vendor (ISV) extension, because out of the box, the secondary display isn't configurable and shows limited content.</span></span>

### <a name="payment-device"></a><span data-ttu-id="a2146-182">支払デバイス</span><span class="sxs-lookup"><span data-stu-id="a2146-182">Payment device</span></span>

<span data-ttu-id="a2146-183">支払デバイスのサポートは、支払コネクタを通して実装されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-183">Payment device support is implemented through the payment connector.</span></span> <span data-ttu-id="a2146-184">支払デバイスは、他のデバイス クラスが提供する機能の 1 つまたは複数を実行できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-184">Payment devices can perform one or many of the functions that other device classes provide.</span></span> <span data-ttu-id="a2146-185">支払デバイスは、MSR/カード リーダー、ライン ディスプレイ、署名キャプチャ デバイスまたは PIN パッド として機能します。</span><span class="sxs-lookup"><span data-stu-id="a2146-185">For example, a payment device can function as an MSR/card reader, line display, signature capture device, or PIN pad.</span></span> <span data-ttu-id="a2146-186">支払デバイスのサポートは、ハードウェア プロファイルに含まれる他のデバイスのスタンドアロン デバイス サポートとは関係なく実装されています。</span><span class="sxs-lookup"><span data-stu-id="a2146-186">Support for payment devices is implemented independently of the stand-alone device support that is provided for other devices that are included in the hardware profile.</span></span>

## <a name="supported-interfaces"></a><span data-ttu-id="a2146-187">サポートされているインターフェース</span><span class="sxs-lookup"><span data-stu-id="a2146-187">Supported interfaces</span></span>

### <a name="opos"></a><span data-ttu-id="a2146-188">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-188">OPOS</span></span>

<span data-ttu-id="a2146-189">できるだけ多くのデバイスで Retail が使用できることを保証するため、サポートされる基本小売周辺機器プラットフォームは POS 業界標準用の OLE です。</span><span class="sxs-lookup"><span data-stu-id="a2146-189">To help guarantee that the largest range of devices can be used with Retail, the OLE for POS industry standard is the primary retail peripheral device platform that is supported.</span></span> <span data-ttu-id="a2146-190">POS 業界標準用 OLE は、小売周辺機器の業界標準の通信プロトコルを設定する National Retail Federation (NRF) により作成されました。</span><span class="sxs-lookup"><span data-stu-id="a2146-190">The OLE for POS standard was produced by the National Retail Federation (NRF), which establishes industry-standard communication protocols for retail peripheral devices.</span></span> <span data-ttu-id="a2146-191">OPOS は、POS標準用 OLE の実装として広く採用されています。</span><span class="sxs-lookup"><span data-stu-id="a2146-191">OPOS is a widely adopted implementation of the OLE for POS standard.</span></span> <span data-ttu-id="a2146-192">これは 90 年代半ばに作成され、それ以降、数回更新されています。</span><span class="sxs-lookup"><span data-stu-id="a2146-192">It was developed in the mid-1990s and has been updated several times since then.</span></span> <span data-ttu-id="a2146-193">OPOS は、Windows ベースの POS システムに POS ハードウェアを簡単に統合できるデバイス ドライバ アーキテクチャを提供します。</span><span class="sxs-lookup"><span data-stu-id="a2146-193">OPOS provides a device driver architecture that enables easy integration of POS hardware with Windows–based POS systems.</span></span> <span data-ttu-id="a2146-194">OPOSは、互換性のある POS ハードウェアとソフトウェアの間の処理通信を制御します。</span><span class="sxs-lookup"><span data-stu-id="a2146-194">OPOS controls handle communication between compatible hardware and the POS software.</span></span> <span data-ttu-id="a2146-195">OPOS コントロールは、2 つ部分から構成されます:</span><span class="sxs-lookup"><span data-stu-id="a2146-195">An OPOS control consists of two parts:</span></span>

- <span data-ttu-id="a2146-196">**コントロール オブジェクト** – デバイス クラス (ライン ディスプレイなど) のコントロール オブジェクトは、ソフトウェアプログラムにインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="a2146-196">**Control object** – The control object for a device class (such as line displays) provides the interface for the software program.</span></span> <span data-ttu-id="a2146-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) は、コモン コントロール オブジェクト (CCO) と呼ばれる標準化された一式の OPOS コントロール オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="a2146-197">Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) provides a standardized set of OPOS control objects that are known as the common control objects (CCOs).</span></span> <span data-ttu-id="a2146-198">CCO は、Retail の POS コンポーネントをテストするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-198">The CCOs are used to test the POS component of Retail.</span></span> <span data-ttu-id="a2146-199">したがって、このテストにより、Retail が OPOS によってデバイス クラスをサポートする場合、メーカーは OPOS 用に作成されたサービス オブジェクトを提供できるように多くのデバイス タイプがサポートまたは提供されることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-199">Therefore, the testing helps guarantee that, if Retail supports a device class through OPOS, many device types can be supported, provided that the manufacturer provides a service object that is built for OPOS.</span></span> <span data-ttu-id="a2146-200">各デバイス タイプを明示的にテストする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-200">You don't have to explicitly test each device type.</span></span>
- <span data-ttu-id="a2146-201">**サービス オブジェクト** – サービス オブジェクトはコントロール オブジェクト (CCO) とデバイス間の通信を提供します。</span><span class="sxs-lookup"><span data-stu-id="a2146-201">**Service object** – The service object provides communication between the control object (CCO) and the device.</span></span> <span data-ttu-id="a2146-202">通常、デバイスのサービス オブジェクトはデバイス メーカーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-202">Typically, the service object for a device is provided by the device manufacturer.</span></span> <span data-ttu-id="a2146-203">ただし、場合によっては、製造元のサイトからサービス オブジェクトをダウンロードする必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-203">However, in some cases, you might have to download the service object from the manufacturer's website.</span></span> <span data-ttu-id="a2146-204">たとえば、最新のサービス オブジェクトが利用可能かもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-204">For example, a more recent service object might be available.</span></span> <span data-ttu-id="a2146-205">メーカーの Web サイトのアドレスを特定するには、ハードウェアのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-205">To find the address of the manufacturer's website, see your hardware documentation.</span></span>

<span data-ttu-id="a2146-206">[![コントロール オブジェクトとサービス オブジェクト](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)</span><span class="sxs-lookup"><span data-stu-id="a2146-206">[![Control object and service object](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png)</span></span>

<span data-ttu-id="a2146-207">POS 用 OLE の OPOS での実装をサポートすることで、デバイス メーカーと POS のパブリッシャーが標準を正しく実装している限り、以前に組み合わせテストされていない POS システムとサポート デバイスの組み合わせでも正しく動作することが保証されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-207">Support for the OPOS implementation of OLE for POS helps guarantee that, if the device manufacturers and POS publishers implement the standard correctly, POS systems and supported devices can work together, even if they weren't previously tested together.</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-208">OPOS サポートは、OPOS ドライバーがあるすべてのデバイスのサポートを保証するものではありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-208">OPOS support doesn't guarantee support for all devices that have OPOS drivers.</span></span> <span data-ttu-id="a2146-209">Retail は最初に OPOS によりそのデバイス タイプまたはクラスをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-209">Retail must first support that device type, or class, through OPOS.</span></span> <span data-ttu-id="a2146-210">また、サービス オブジェクトが最新バージョンの CCO に対応した最新のものではないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-210">In addition, service objects might not always be up to date with the latest version of the CCOs.</span></span> <span data-ttu-id="a2146-211">一般に、サービス オブジェクトのクオリティには差異があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-211">You should also be aware that, in general, the quality of service objects varies.</span></span>

### <a name="windows"></a><span data-ttu-id="a2146-212">ウィンドウ(&W)</span><span class="sxs-lookup"><span data-stu-id="a2146-212">Windows</span></span>

<span data-ttu-id="a2146-213">POS レシートの印刷は、OPOS に最適化されています。</span><span class="sxs-lookup"><span data-stu-id="a2146-213">Receipt printing at the POS is optimized for OPOS.</span></span> <span data-ttu-id="a2146-214">一般に、OPOS による印刷は Windows による印刷より高速です。</span><span class="sxs-lookup"><span data-stu-id="a2146-214">OPOS tends to be much faster than printing through Windows.</span></span> <span data-ttu-id="a2146-215">したがって、40 列のレシートを高速のトランザクション タイムで印刷する必要のある小売環境では、OPOS を使用することが最善です。</span><span class="sxs-lookup"><span data-stu-id="a2146-215">Therefore, it's a good idea to use OPOS, especially in retail environments where 40-column receipts are printed and transaction times must be fast.</span></span> <span data-ttu-id="a2146-216">ほとんどのデバイスについては、OPOS コントロールを使用します。</span><span class="sxs-lookup"><span data-stu-id="a2146-216">For most devices, you will use OPOS controls.</span></span> <span data-ttu-id="a2146-217">ただし、一部の OPOS レシート プリンターは Windows ドライバもサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-217">However, some OPOS receipt printers also support Windows drivers.</span></span> <span data-ttu-id="a2146-218">Windows ドライバを使用する場合、最新のフォントにアクセス可能で、複数のレジスターと 1 つのプリンターをネットワーク化できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-218">By using a Windows driver, you can access the latest fonts and network one printer for multiple registers.</span></span> <span data-ttu-id="a2146-219">ただし、Windows ドライバーの使用には短所があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-219">However, there are drawbacks to using Windows drivers.</span></span> <span data-ttu-id="a2146-220">短所の例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a2146-220">Here are some examples of these drawbacks:</span></span>

- <span data-ttu-id="a2146-221">Windows ドライバを使用する場会、画像は印刷開始前にレンダリングされます。</span><span class="sxs-lookup"><span data-stu-id="a2146-221">When Windows drivers are used, images are rendered before printing occurs.</span></span> <span data-ttu-id="a2146-222">したがって、印刷は OPOS コントロールを使用するプリンタより遅くなる傾向があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-222">Therefore, printing tends to be slower than it is on printers that use OPOS controls.</span></span>
- <span data-ttu-id="a2146-223">プリンターを通して接続されているデバイス (「デイジー チェーン」) は 、Windows ドライバーを使用している間、正しく動作しないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-223">Devices that are connected through the printer ("daisy-chained") might not work correctly when Windows drivers are used.</span></span> <span data-ttu-id="a2146-224">たとえば、キャッシュ ドロワーが開かないかもしれず、伝票プリンタが指示通り動かないかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-224">For example, the cash drawer might not open, or the slip printer might not word as you expect.</span></span>
- <span data-ttu-id="a2146-225">OPOS は、紙切断または伝票印刷など小売レシート プリンターに特有の広範な変数をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-225">OPOS also supports a more extensive set of variables that are specific to retail receipt printers, such as paper cutting or slip printing.</span></span>

<span data-ttu-id="a2146-226">使用している Windows プリンターで OPOS コントロールが使用できる場合、Retail でプリンターを正しく使用できるはずです。</span><span class="sxs-lookup"><span data-stu-id="a2146-226">If OPOS controls are available for the Windows printer that you're using, the printer should still work correctly with Retail.</span></span>

### <a name="universal-windows-platform"></a><span data-ttu-id="a2146-227">Universal Windows Platform</span><span class="sxs-lookup"><span data-stu-id="a2146-227">Universal Windows Platform</span></span>

<span data-ttu-id="a2146-228">小売周辺機器の場合の UWP は、プラグ アンド プレイ デバイス用 Windows サポートに関連しています。</span><span class="sxs-lookup"><span data-stu-id="a2146-228">UWP, in the case of retail peripherals, is related to Windows support for Plug and Play devices.</span></span> <span data-ttu-id="a2146-229">プラグ アンド プレイ デバイスがそのデバイス タイプをサポートする Windows OS バージョンに接続された場合、デバイスを使用するためのドライバーは必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-229">When a Plug and Play device is connected to a Windows OS version that supports that type of device, no driver is required for the device to be used as intended.</span></span> <span data-ttu-id="a2146-230">たとえば、Windows が Bluetooth のスピーカー デバイスを検出すると、OS はそのデバイスが **スピーカー** クラス タイプを持つことを認識します。</span><span class="sxs-lookup"><span data-stu-id="a2146-230">For example, if Windows detects a Bluetooth speaker device, the OS knows that the device has the **Speaker** class type.</span></span> <span data-ttu-id="a2146-231">したがって、そのデバイスをスピーカーとして処理します。</span><span class="sxs-lookup"><span data-stu-id="a2146-231">Therefore, and it treats that device as a speaker.</span></span> <span data-ttu-id="a2146-232">追加の設定は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-232">No additional setup is required.</span></span> <span data-ttu-id="a2146-233">POS デバイスの場合、多くの USB デバイスを接続でき、Windows はヒューマン インターフェイス デバイス (HID) として認識します。</span><span class="sxs-lookup"><span data-stu-id="a2146-233">In the case of POS devices, many USB devices can be plugged in, and Windows will recognize them as Human Interface Devices (HIDs).</span></span> <span data-ttu-id="a2146-234">ただし、デバイスがクラスまたはタイプを指定しないため、そのデバイスの機能を認識することができない場合があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-234">However, it might not be able to determine the capabilities that the device provides, because the device doesn't specify the class, or type, of device.</span></span> <span data-ttu-id="a2146-235">Windows 10 で、バーコード スキャナーおよび MSR のデバイス クラスが追加されました。</span><span class="sxs-lookup"><span data-stu-id="a2146-235">In Windows 10, device classes for bar code scanners and MSRs have been added.</span></span> <span data-ttu-id="a2146-236">したがって、デバイスがこれらのクラスの 1 つのデバイスとして Windows 10 に自分を申告すると、Windows は適切なタイミングでデバイスのイベントを聞き取ります。</span><span class="sxs-lookup"><span data-stu-id="a2146-236">Therefore, if a device declares itself to Windows 10 as a device of one of these classes, Windows will listen for events from the device at the appropriate times.</span></span> <span data-ttu-id="a2146-237">Modern POS は MSR およびスキャナーの UWP をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-237">Modern POS supports UWP MSRs and scanners.</span></span> <span data-ttu-id="a2146-238">したがって、これらのデバイスの 1 つからの入力を受け入れられるようになり、これらのクラスの 1 つに属するデバイスが接続されると、デバイスは使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a2146-238">Therefore, when it's ready for input from one of these devices, and a device that belongs to one of these classes is connected, the device can be used.</span></span> <span data-ttu-id="a2146-239">たとえば、UWP バーコード スキャナーが Windows 10 のコンピュータに接続された場合、Modern POS 用にバーコード サインインが設定され、サインイン画面でバーコード スキャナーが有効になります。</span><span class="sxs-lookup"><span data-stu-id="a2146-239">For example, if a UWP bar code scanner is plugged into a Windows 10 computer, and bar code sign-in is configured for Modern POS, the bar code scanner will become active on the sign-in screen.</span></span> <span data-ttu-id="a2146-240">追加の設定は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-240">No additional setup is required.</span></span> <span data-ttu-id="a2146-241">ポイント オブ サービス UWP デバイスの追加クラスが Windows に追加されています。</span><span class="sxs-lookup"><span data-stu-id="a2146-241">Additional classes of point of service UWP devices are being added to Windows.</span></span> <span data-ttu-id="a2146-242">これらのクラスには、キャッシュ ドロワーやレシート プリンターのクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a2146-242">These classes include classes for cash drawers and receipt printers.</span></span> <span data-ttu-id="a2146-243">これらの新しいデバイス クラスの Modern POS でのサポートは保留中です。</span><span class="sxs-lookup"><span data-stu-id="a2146-243">Support for these new device classes in Modern POS is pending.</span></span>

### <a name="keyboard-wedge"></a><span data-ttu-id="a2146-244">キーボード ウェッジ</span><span class="sxs-lookup"><span data-stu-id="a2146-244">Keyboard wedge</span></span>

<span data-ttu-id="a2146-245">キーボード ウェッジのデバイスは、データがキーボードで入力されているかのようにコンピューターにそのデータを送信します。</span><span class="sxs-lookup"><span data-stu-id="a2146-245">Keyboard wedge devices send data to the computer as if that data were typed on a keyboard.</span></span> <span data-ttu-id="a2146-246">したがって既定では、POS で有効なフィールドが、スキャンまたは読み取りされたデータを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a2146-246">Therefore, by default, the field that is active at the POS will receive the data that is scanned or swiped.</span></span> <span data-ttu-id="a2146-247">場合によっては、この動作により誤ったタイプのデータが誤ったフィールドにスキャンされることがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-247">In some cases, this behavior can cause the wrong type of data to be scanned into the wrong field.</span></span> <span data-ttu-id="a2146-248">たとえば、クレジット カードのデータ入力を対象とするフィールドにバーコードがスキャン入力されるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-248">For example, a bar code might be scanned into a field that is intended for input of credit card data.</span></span> <span data-ttu-id="a2146-249">多くの場合、スキャンまたは読み取りされたデータが、バーコードなのかカードの読み取りなのかを決定するロジックが POS にあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-249">In many cases, there is logic at the POS that determines whether the data that is scanned or swiped is a bar code or card swipe.</span></span> <span data-ttu-id="a2146-250">したがって、データが正しく処理されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-250">Therefore, the data is handled correctly.</span></span> <span data-ttu-id="a2146-251">ただし、デバイスがキーボード ウェッジ デバイスの代わりに OPOS として設定されている場合は、そのデバイスのデータをどのように処理するかを詳細に制御できます。データが送られてくるデバイスについて多くのことが「知られている」からです。</span><span class="sxs-lookup"><span data-stu-id="a2146-251">However, when devices are set up as OPOS instead of keyboard wedge devices, there is more control over how the data from those devices can be consumed, because more is "known" about the device that the data originates from.</span></span> <span data-ttu-id="a2146-252">たとえば、バーコード スキャナーのデータはバーコードとして自動的に認識され、キーボード ウェッジ デバイスを使用した一般的なストリング検索の場合より、データベースの関連レコードは早く簡単に検索できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-252">For example, data from a bar code scanner is automatically recognized as a bar code, and the associated record in the database is found more easily and faster than if a generic string search were used, as in the case of keyboard wedge devices.</span></span>

### <a name="native-printer"></a><span data-ttu-id="a2146-253">ネイティブ プリンタ</span><span class="sxs-lookup"><span data-stu-id="a2146-253">Native printer</span></span>

<span data-ttu-id="a2146-254">ネイティブ (または、タイプがハードウェア プロファイルで指定されている「デバイス」の) プリンタは、ユーザーがコンピュータで設定されているプリンタを選択することを求めるように設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-254">Native (or "Device" as the type is named in the hardware profile) printers can be configured to prompt the user to select a printer that is configured for the computer.</span></span> <span data-ttu-id="a2146-255">**デバイス**タイプのプリンタが設定され、Modern POS が印刷のコマンドを検出した場合、ユーザーはリストからプリンターを選択するように要求されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-255">When a printer of the **Device** type is configured, if Modern POS encounters a print command, the user is prompted to select a printer in a list.</span></span> <span data-ttu-id="a2146-256">この動作は、Windows ドライバーの動作とは異なります。ハードウェア プロファイルの **Windows** プリンター タイプは、プリンターの一覧を表示しません。</span><span class="sxs-lookup"><span data-stu-id="a2146-256">This behavior differs from the behavior for Windows drivers, because the **Windows** printer type in the hardware profile doesn't show a list of printers.</span></span> <span data-ttu-id="a2146-257">代わりに、指定されたプリンタが**デバイス名**フィールドに入力されていることが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-257">Instead, it requires that a named printer be provided in the **Device name** field.</span></span>

### <a name="windows"></a><span data-ttu-id="a2146-258">ウィンドウ(&W)</span><span class="sxs-lookup"><span data-stu-id="a2146-258">Windows</span></span>

<span data-ttu-id="a2146-259">**Windows** デバイス タイプは、プリンターにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-259">The **Windows** device type is used for printers only.</span></span> <span data-ttu-id="a2146-260">Windows プリンターがハードウェア プロファイルに設定されている場合、特定のプリンター名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-260">When a Windows printer is configured in the hardware profile, the specific printer name must be provided.</span></span> <span data-ttu-id="a2146-261">Modern POS が印刷のイベントを検出した時、Windows プリンターが設定されている場合、イベントは指定された Windows プリンターに渡されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-261">When Modern POS encounters print events, if a Windows printer is configured, the event will be passed to the specified Windows printer.</span></span> <span data-ttu-id="a2146-262">ユーザーがプリンタを選択するよう促すメッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="a2146-262">The user won't be prompted to select a printer.</span></span>

### <a name="network"></a><span data-ttu-id="a2146-263">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-263">Network</span></span>

<span data-ttu-id="a2146-264">ネットワーク対応のキャッシュ ドロワー、レシート プリンター、支払ターミナルは、Windows 用 Modern POS および Android 用 Modern POS アプリケーションに組み込まれたプロセス間通信 (IPC) のハードウェア ステーションを経由して直接、あるいは他の Modern POS クライアントの IIS ハードウェア ステーションを経由して、ネットワークで使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-264">Network-addressable cash drawers, receipt printers, and payment terminals can be used over a network, either directly through the Interprocess Communications (IPC) hardware station that is built into the Modern POS for Windows and Modern POS for Android applications or through the IIS hardware station for other Modern POS clients.</span></span>

## <a name="hardware-station-deployment-options"></a><span data-ttu-id="a2146-265">ハードウェア ステーションの配置オプション</span><span class="sxs-lookup"><span data-stu-id="a2146-265">Hardware station deployment options</span></span>

### <a name="ipc-built-in"></a><span data-ttu-id="a2146-266">IPC (組み込み)</span><span class="sxs-lookup"><span data-stu-id="a2146-266">IPC (built-in)</span></span>

<span data-ttu-id="a2146-267">プロセス間通信 (IPC) ハードウェア ステーションは、Windows 用 Modern POS および Android 用 Modern POS に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="a2146-267">The Interprocess Communications (IPC) hardware station is built into the Modern POS for Windows and Modern POS for Android application.</span></span> <span data-ttu-id="a2146-268">IPC のハードウェア ステーションを使用するには、Windows アプリケーション用 Modern POS を使用するレジスターにハードウェア プロファイルを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a2146-268">To use the IPC hardware station, assign a hardware profile to a register that will use the Modern POS for Windows application.</span></span> <span data-ttu-id="a2146-269">次に、レジスタが使用される店舗用に**専用**タイプのハードウェア ステーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-269">Then create a hardware station of the **Dedicated** type for the store where the register will be used.</span></span> <span data-ttu-id="a2146-270">Modern POS を起動すると、IPC のハードウェア ステーションが有効になり、次いで設定された POS の周辺機器が使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="a2146-270">When you start Modern POS, the IPC hardware station will be active, and the POS peripherals that have been configured will be ready to use.</span></span> <span data-ttu-id="a2146-271">一時的に何らかの理由でローカル ハードウエアが必要でない場合、**ハードウェア ステーションの管理**操作を使用して、ハードウェア ステーションの機能をオフにします。</span><span class="sxs-lookup"><span data-stu-id="a2146-271">If you temporarily don't require the local hardware for some reason, use the **Manage hardware stations** operation to turn off the hardware station capabilities.</span></span> <span data-ttu-id="a2146-272">Modern POS は、ネットワーク周辺機器と直接通信するためにも IPC ハードウェア ステーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="a2146-272">Modern POS can also use the IPC hardware station to communicate directly with network peripherals.</span></span>

### <a name="iis"></a><span data-ttu-id="a2146-273">IIS</span><span class="sxs-lookup"><span data-stu-id="a2146-273">IIS</span></span>

<span data-ttu-id="a2146-274">2 つの方法で、スタンドアロンのバージョンのハードウェア ステーションまたは IIS を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-274">You can use the IIS or stand-alone version of the hardware station in two ways.</span></span> <span data-ttu-id="a2146-275">記述子「IIS」は、POS アプリケーションが Microsoft Internet Information Services を介してハードウェア ステーションと接続していることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a2146-275">The descriptor "IIS" implies that the POS application connects to the hardware station via Microsoft Internet Information Services.</span></span> <span data-ttu-id="a2146-276">POS アプリケーションは、デバイスが接続されているコンピュータで実行される Web サービスを介して IIS ハードウェア ステーションに接続します。</span><span class="sxs-lookup"><span data-stu-id="a2146-276">The POS application connects to the IIS hardware station via web services that run on a computer where the devices are connected.</span></span> <span data-ttu-id="a2146-277">IIS を使用すると、ハードウェア ステーションに接続されている小売周辺機器は、IIS ハードウェア ステーションと同じネットワークにつながるどの POS レジスターでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-277">When IIS is used, the retail peripherals that are connected to a hardware station can be used by any POS register that is on the same network as the IIS hardware station.</span></span> <span data-ttu-id="a2146-278">Windows 用 Modern POS のみに小売周辺機器サポートが組み込まれているため、他のすべての Modern POS アプリケーションは、ハードウェア プロファイルでコンフィギュレーションされたPOS周辺機器と通信するために IIS ハードウェア ステーションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-278">Because only Modern POS for Windows includes built-in support for retail peripherals, all other Modern POS applications must use the IIS hardware station to communicate with POS peripherals that are configured in the hardware profile.</span></span> <span data-ttu-id="a2146-279">したがって、IIS ハードウェア ステーションの各インスタンスは、Web サービスおよびデバイスと通信するアプリケーションを実行するコンピュータが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-279">Therefore, each instance of the IIS hardware station requires a computer that runs the web service and application that communicates with the devices.</span></span> <span data-ttu-id="a2146-280">IIS ハードウェア ステーションは、すべての非 Windows Modern POS アプリケーションに必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-280">The IIS hardware station is required for all non-Windows Modern POS applications.</span></span>

#### <a name="dedicated"></a><span data-ttu-id="a2146-281">専用</span><span class="sxs-lookup"><span data-stu-id="a2146-281">Dedicated</span></span>

<span data-ttu-id="a2146-282">Modern POS は**専用**タイプのハードウェア ステーションを、アプリケーションが使用しているコンピュータに直接接続されている周辺機器を検出するのに使用します。</span><span class="sxs-lookup"><span data-stu-id="a2146-282">Modern POS uses hardware stations of the **Dedicated** type to detect that peripherals are directly connected to the computer where the app is being used.</span></span> <span data-ttu-id="a2146-283">ただし、**専用**タイプは、IIS のハードウェア ステーションにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-283">However, the **Dedicated** type can also be used for IIS hardware stations.</span></span> <span data-ttu-id="a2146-284">従来の固定 POS のシナリオでは、POS アプリケーションとしてクラウド POS を使用し、**専用**タイプのハードウェア ステーションがクラウド POS を実行するのと同じコンピュータに配置される IIS ハードウェア ステーションとして使用されていました。</span><span class="sxs-lookup"><span data-stu-id="a2146-284">In a traditional, fixed POS scenario that uses Cloud POS as the POS application, the **Dedicated** hardware station type is used for IIS hardware stations that are deployed on the same computer that is running Cloud POS.</span></span> <span data-ttu-id="a2146-285">小売周辺機器の視点から見ると、従来の固定 POS のシナリオの小売周辺機器サポートより、専用 IIS ハードウェア ステーションの方が優れています。</span><span class="sxs-lookup"><span data-stu-id="a2146-285">From a retail peripherals perspective, the dedicated IIS hardware station has better retail peripheral support for traditional, fixed POS scenarios.</span></span> <span data-ttu-id="a2146-286">専用ハードウェア ステーションは、ハードウェア プロファイルでサポートされているすべての周辺機器をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-286">Dedicated hardware stations support all peripherals that are supported in the hardware profile.</span></span>

#### <a name="shared"></a><span data-ttu-id="a2146-287">共有</span><span class="sxs-lookup"><span data-stu-id="a2146-287">Shared</span></span>

<span data-ttu-id="a2146-288">共有ハードウェア ステーションは、1日の間に複数の POS デバイスで使用されることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="a2146-288">Shared hardware stations are intended to be used by multiple POS devices through the course of the day.</span></span> <span data-ttu-id="a2146-289">共有ハードウェア ステーションは、キャッシュ ドロワー、レシート プリンター、支払ターミナルのみをサポートするよう最適化されています。</span><span class="sxs-lookup"><span data-stu-id="a2146-289">Shared hardware stations are optimized to support only cash drawers, receipt printers, and payment terminals.</span></span> <span data-ttu-id="a2146-290">スタンドアロンのバーコード スキャナー、MSR、ライン ディスプレイ、スケール、その他のデバイスを直接接続することはできません。</span><span class="sxs-lookup"><span data-stu-id="a2146-290">You can't directly connect stand-alone bar code scanners, MSRs, line displays, scales, or other devices.</span></span> <span data-ttu-id="a2146-291">接続すると、複数の POS デバイスがそれらの周辺機器を同時に使用しようとして競合が生じます。</span><span class="sxs-lookup"><span data-stu-id="a2146-291">Otherwise, conflicts will occur when multiple POS devices try to claim those peripherals at the same time.</span></span> <span data-ttu-id="a2146-292">サポートされているデバイス用の競合は、以下のように管理されています:</span><span class="sxs-lookup"><span data-stu-id="a2146-292">Here is how conflicts are managed for supported devices:</span></span>

- <span data-ttu-id="a2146-293">**キャッシュ ドロワー** – キャッシュ ドロワーはデバイスに送信されるイベントによって開きます。</span><span class="sxs-lookup"><span data-stu-id="a2146-293">**Cash drawer** – The cash drawer is opened via an event that is sent to the device.</span></span> <span data-ttu-id="a2146-294">キャッシュ ドロワーが呼び出されたときに発生する唯一の問題は、キャッシュ ドロワーがすでに開いている場合です。</span><span class="sxs-lookup"><span data-stu-id="a2146-294">The only issue that can occur when a cash drawer is called occurs if the cash drawer is already open.</span></span> <span data-ttu-id="a2146-295">共有ハードウェア ステーションの場合、キャッシュ ドロワーはハードウェア プロファイルで**共有**と設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-295">In the case of shared hardware stations, the cash drawer should be set to **Shared** in the hardware profile.</span></span> <span data-ttu-id="a2146-296">この設定は、POS が [open] コマンドを送信する時に、キャッシュ ドロワーがすでに開いているかどうかの確認をすることを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="a2146-296">This setting prevents the POS from checking whether the cash drawer is already open when it sends open commands.</span></span>
- <span data-ttu-id="a2146-297">**レシート プリンター** – 2つのレシート印刷コマンドがハードウェア ステーションに同時に送信されると、デバイスによってはどちらかのコマンドが失われてしまうことがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-297">**Receipt printer** – If two receipt printing commands are sent to the hardware station at the same time, one of the commands can be lost, depending on the device.</span></span> <span data-ttu-id="a2146-298">デバイスによっては、この問題を防ぐための内部メモリまたはプールがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-298">Some devices have internal memory or pooling that can prevent this issue.</span></span> <span data-ttu-id="a2146-299">印刷コマンドが正常に終了しない場合、レジ担当者はエラー メッセージを受信し、POS から印刷コマンドを再試行できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-299">If a print command isn't successful, the cashier receives an error message and can retry the print command from the POS.</span></span>
- <span data-ttu-id="a2146-300">**支払ターミナル** – レジ担当者が既に使用中の支払ターミナルに支払/入金のトランザクションを送信しようとした場合、ターミナルが使用中であり後でもう一度試すようにレジ担当者に求めるメッセージがレジ担当者に通知されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-300">**Payment terminal** – If a cashier tries to tender a transaction on a payment terminal that is already being used, a message notifies the cashier that the terminal is being used and asks the cashier to try again later.</span></span> <span data-ttu-id="a2146-301">通常、レジ担当者はターミナルが既に使用中であることがわかり、他のトランザクションが完了するまで待機してから、支払/入金を再度送信します。</span><span class="sxs-lookup"><span data-stu-id="a2146-301">Usually, cashiers can see that a terminal is already being used and will wait until the other transaction is completed before they try to tender again.</span></span>

<span data-ttu-id="a2146-302">将来のリリースでは、サポートされていないデバイスが共有ハードウェア ステーションにマップされているハードウェア プロファイルで設定されているかどうかを検証する予定です。</span><span class="sxs-lookup"><span data-stu-id="a2146-302">Validation is planned for a future release, to detect whether unsupported devices are set up for a hardware profile that is mapped to a shared hardware station.</span></span> <span data-ttu-id="a2146-303">サポートされていないデバイスが検出された場合、デバイスが共有ハードウェア ステーションでサポートされていないことを知らせるメッセージがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-303">If any unsupported devices are detected, the user will receive a message that states that the devices aren't supported for shared hardware stations.</span></span> <span data-ttu-id="a2146-304">共有ハードウェア ステーションの場合、**支払/入金での選択** オプションは、レジスター レベルで **はい** と設定されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-304">In the case of shared hardware stations, the **Select upon tendering** option is set to **Yes** at the register level.</span></span> <span data-ttu-id="a2146-305">これにより、POS のトランザクションで支払/入金が選択された場合、POS ユーザーはハードウェア ステーションを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="a2146-305">The POS user is then prompted to select a hardware station when a tender is selected for a transaction at the POS.</span></span> <span data-ttu-id="a2146-306">ハードウェア ステーションが支払/入金時にのみ選択された場合、ハードウェア ステーションの選択はモバイルのシナリオの POS ワークフローに直接追加されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-306">When the hardware station is selected only at the time of tender, the hardware station selection is added directly to the POS workflow for mobile scenarios.</span></span> <span data-ttu-id="a2146-307">付加的なメリットとして、共有シナリオの場合には支払ターミナルのライン ディスプレイは使用されません。</span><span class="sxs-lookup"><span data-stu-id="a2146-307">As an additional benefit, the line display on the payment terminal isn't used for shared scenarios.</span></span> <span data-ttu-id="a2146-308">支払ターミナルがライン ディスプレイとして使用されると、トランザクションが完了するまでそのターミナルの他のユーザーの使用がブロックされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-308">If the payment terminal is used as a line display, other users might be blocked from using that terminal until the transaction is completed.</span></span> <span data-ttu-id="a2146-309">モバイルのシナリオでは、ラインはトランザクションに長期に渡って追加されることがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-309">In mobile scenarios, lines might be added to a transaction over a longer period.</span></span> <span data-ttu-id="a2146-310">したがって、デバイスの最適な使用を保証するために **支払/入金での選択** オプションが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-310">Therefore, the **Select upon tendering** option is required in order to ensure optimum device availability.</span></span>

### <a name="network-peripherals"></a><span data-ttu-id="a2146-311">ネットワーク周辺機器</span><span class="sxs-lookup"><span data-stu-id="a2146-311">Network peripherals</span></span>

<span data-ttu-id="a2146-312">ハードウェア プロファイルのデバイスのネットワーク指定は、キャッシュ ドロワー、レシート プリンター、支払ターミナルのネットワーク経由での接続を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a2146-312">The network designation for devices in the hardware profile enables cash drawers, receipt printers, and payment terminals to be connected via a network connection.</span></span>

#### <a name="modern-pos-for-windows"></a><span data-ttu-id="a2146-313">Windows 用の Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-313">Modern POS for Windows</span></span>

<span data-ttu-id="a2146-314">ネットワーク周辺機器の IP アドレスは、2 箇所で指定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-314">You can specify IP addresses for network peripherals in two places.</span></span> <span data-ttu-id="a2146-315">Modern POS の Windows クライアントが一式のネットワーク周辺機器を使用している場合、レジスタ自体のアクション ペインの **IP コンフィギュレーション** オプションを使用してこれらのデバイスの IP アドレスを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-315">If the Modern POS Windows client is using a single set of network peripherals, you should set the IP addresses for those devices by using the **IP configuration** option on the Action Pane for the register itself.</span></span> <span data-ttu-id="a2146-316">POS レジスタで共有されているネットワーク デバイスの場合、ネットワーク デバイスを割り当てているハードウェア プロファイルを共有ハードウェア ステーションに直接マップすることができます。</span><span class="sxs-lookup"><span data-stu-id="a2146-316">In the case of network devices that will be shared among POS registers, a hardware profile that has network devices assigned to it can be mapped directly to a shared hardware station.</span></span> <span data-ttu-id="a2146-317">IP アドレスを割り当てるには、**小売店舗** ページでハードウェア ステーションを選択し、**ハードウェア ステーション** セクションの **IP コンフィギュレーション** オプションを使用し、そのハードウェア ステーションに割り当てられているネットワーク デバイスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a2146-317">To assign IP addresses, select that hardware station on the **Retail stores** page, and then use the **IP configuration** option in the **Hardware stations** section to specify the network devices that are assigned to that hardware station.</span></span> <span data-ttu-id="a2146-318">ネットワーク デバイスのみを使用するハードウェア ステーションの場合、ハードウェア ステーション自体を配置する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-318">For hardware stations that have only network devices, you don't have to deploy the hardware station itself.</span></span> <span data-ttu-id="a2146-319">この場合、小売店舗内の場所に従ってネットワーク対応可能なデバイスを概念的にグループ化するためにのみ、ハードウェア ステーションは必要となります。</span><span class="sxs-lookup"><span data-stu-id="a2146-319">In this case, the hardware station is required only in order to conceptually group network-addressable devices according to their location in the retail store.</span></span>

#### <a name="modern-pos-for-android"></a><span data-ttu-id="a2146-320">Android 用 Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-320">Modern POS for Android</span></span>

<span data-ttu-id="a2146-321">現在の Retail バージョン 8.1.3 では、Android 用 Modern POS アプリケーションに組み込みの IPC ハードウェア ステーションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2146-321">As of Retail version 8.1.3, the Modern POS for Android application includes a built-in IPC hardware station.</span></span> <span data-ttu-id="a2146-322">このハードウェア ステーションは、ネットワーク プリンターおよび支払コネクタとの通信をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-322">This hardware station supports communicating with network printers and payment connectors.</span></span> <span data-ttu-id="a2146-323">詳細については、[Android 用 Hybrid アプリに関する docs の記事](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/hybridapp#dedicated-hardware-station-support-for-the-hybrid-android-app) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-323">For more information, visit the [Hybrid app for Android docs article](https://docs.microsoft.com/dynamics365/unified-operations/retail/dev-itpro/hybridapp#dedicated-hardware-station-support-for-the-hybrid-android-app).</span></span> 

#### <a name="cloud-pos-and-modern-pos-for-ios"></a><span data-ttu-id="a2146-324">クラウド POS および iOS 用 Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-324">Cloud POS and Modern POS for iOS</span></span>

<span data-ttu-id="a2146-325">物理的に接続されている周辺機器およびネットワーク対応可能な周辺機器の駆動ロジックは、ハードウェア ステーションに含まれています。</span><span class="sxs-lookup"><span data-stu-id="a2146-325">The logic that drives physically connected and network-addressable peripherals is contained in the hardware station.</span></span> <span data-ttu-id="a2146-326">したがって Windows 用 以外の Modern POS クライアントの場合、周辺機器がハードウェア ステーションに物理的に接続されているかネットワークに対応しているかに関係なく、POS とそれらの周辺機器との通信を可能にするためには、IIS ハードウェア ステーションを配置し有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-326">Therefore, for all POS clients except Modern POS for Windows, an IIS hardware station must be deployed and active to enable the POS to communicate with peripherals, regardless of whether those peripherals are physically connected to a hardware station or addressed over the network.</span></span>

## <a name="setup-and-configuration"></a><span data-ttu-id="a2146-327">設定およびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a2146-327">Setup and configuration</span></span>

### <a name="hardware-station-installation"></a><span data-ttu-id="a2146-328">ハードウェア ステーションのインストール</span><span class="sxs-lookup"><span data-stu-id="a2146-328">Hardware station installation</span></span>

<span data-ttu-id="a2146-329">詳細については、 [Retail ハードウェア ステーションのコンフィギュレーションとインストール](retail-hardware-station-configuration-installation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-329">For information, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>

### <a name="modern-pos-for-windows-setup-and-configuration"></a><span data-ttu-id="a2146-330">Windows 用 Modern POS の設定とコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a2146-330">Modern POS for Windows setup and configuration</span></span>

<span data-ttu-id="a2146-331">詳細については、「[Retail Modern POS のコンフィギュレーションとインストール](retail-modern-pos-device-activation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-331">For information, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>

### <a name="opos-device-setup-and-configuration"></a><span data-ttu-id="a2146-332">OPOS デバイスの設定とコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a2146-332">OPOS device setup and configuration</span></span>

<span data-ttu-id="a2146-333">OPOS コンポーネントに関する詳細については、このドキュメントの「サポートされているインターフェース」のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-333">For more information about OPOS components, see the "Supported interfaces" section of this document.</span></span> <span data-ttu-id="a2146-334">通常、OPOS ドライバーはデバイス メーカーから提供されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-334">Typically, OPOS drivers are provided by the device manufacturer.</span></span> <span data-ttu-id="a2146-335">OPOS デバイス ドライバをインストールすると、Windows レジストリの以下のどこか 1 つの場所にキーを追加します:</span><span class="sxs-lookup"><span data-stu-id="a2146-335">When an OPOS device driver is installed, it adds a key to the Windows registry in one of the following locations:</span></span>

- <span data-ttu-id="a2146-336">**32 ビット システム:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-336">**32-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREOLEforRetailServiceOPOS</span></span>
- <span data-ttu-id="a2146-337">**64 ビット システム:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-337">**64-bit system:** HKEY\_LOCAL\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS</span></span>

<span data-ttu-id="a2146-338">ServiceOPOS レジストリ内では、設定されているデバイスは OPOS デバイス クラスに従って編成されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-338">Within the ServiceOPOS registry location, configured devices are organized according to the OPOS device class.</span></span> <span data-ttu-id="a2146-339">複数のデバイス ドライバが保存されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-339">Multiple device drivers are saved.</span></span>

## <a name="supported-scenarios-by-hardware-station-type"></a><span data-ttu-id="a2146-340">ハードウェア ステーションのタイプによりサポートされるシナリオ</span><span class="sxs-lookup"><span data-stu-id="a2146-340">Supported scenarios by hardware station type</span></span>

### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a><span data-ttu-id="a2146-341">クライアント サポート – IPC ハードウェア ステーション対 IIS ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-341">Client support – IPC hardware station vs. IIS hardware station</span></span>

<span data-ttu-id="a2146-342">次の表に、サポートされるトポロジや配置シナリオを示しています。</span><span class="sxs-lookup"><span data-stu-id="a2146-342">The following table shows the topologies and deployment scenarios that are supported.</span></span>

| <span data-ttu-id="a2146-343">クライアント</span><span class="sxs-lookup"><span data-stu-id="a2146-343">Client</span></span>      | <span data-ttu-id="a2146-344">IPC ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-344">IPC hardware station</span></span> | <span data-ttu-id="a2146-345">IIS ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-345">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="a2146-346">Windows アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a2146-346">Windows app</span></span> | <span data-ttu-id="a2146-347">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-347">Yes</span></span>                  | <span data-ttu-id="a2146-348">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-348">Yes</span></span>                  |
| <span data-ttu-id="a2146-349">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="a2146-349">Cloud POS</span></span>   | <span data-ttu-id="a2146-350">いいえ</span><span class="sxs-lookup"><span data-stu-id="a2146-350">No</span></span>                   | <span data-ttu-id="a2146-351">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-351">Yes</span></span>                  |
| <span data-ttu-id="a2146-352">Android</span><span class="sxs-lookup"><span data-stu-id="a2146-352">Android</span></span>     | <span data-ttu-id="a2146-353">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-353">Yes</span></span>                  | <span data-ttu-id="a2146-354">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-354">Yes</span></span>                  |
| <span data-ttu-id="a2146-355">iOS</span><span class="sxs-lookup"><span data-stu-id="a2146-355">iOS</span></span>         | <span data-ttu-id="a2146-356">いいえ</span><span class="sxs-lookup"><span data-stu-id="a2146-356">No</span></span>                   | <span data-ttu-id="a2146-357">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-357">Yes</span></span>                  |

### <a name="network-peripherals"></a><span data-ttu-id="a2146-358">ネットワーク周辺機器</span><span class="sxs-lookup"><span data-stu-id="a2146-358">Network peripherals</span></span>

<span data-ttu-id="a2146-359">ネットワーク周辺機器は、Windows アプリケーション用 Modern POSに組み込まれたハードウェア ステーションを通じて直接サポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="a2146-359">Network peripherals can be supported directly through the hardware station that is built into the Modern POS for Windows application.</span></span> <span data-ttu-id="a2146-360">他のすべてのクライアントの場合、IIS ハードウェア ステーションを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-360">For all other clients, you must deploy an IIS hardware station.</span></span>

| <span data-ttu-id="a2146-361">クライアント</span><span class="sxs-lookup"><span data-stu-id="a2146-361">Client</span></span>      | <span data-ttu-id="a2146-362">IPC ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-362">IPC hardware station</span></span> | <span data-ttu-id="a2146-363">IIS ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-363">IIS hardware station</span></span> |
|-------------|----------------------|----------------------|
| <span data-ttu-id="a2146-364">Windows アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a2146-364">Windows app</span></span> | <span data-ttu-id="a2146-365">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-365">Yes</span></span>                  | <span data-ttu-id="a2146-366">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-366">Yes</span></span>                  |
| <span data-ttu-id="a2146-367">クラウド POS</span><span class="sxs-lookup"><span data-stu-id="a2146-367">Cloud POS</span></span>   | <span data-ttu-id="a2146-368">いいえ</span><span class="sxs-lookup"><span data-stu-id="a2146-368">No</span></span>                   | <span data-ttu-id="a2146-369">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-369">Yes</span></span>                  |
| <span data-ttu-id="a2146-370">Android</span><span class="sxs-lookup"><span data-stu-id="a2146-370">Android</span></span>     | <span data-ttu-id="a2146-371">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-371">Yes</span></span>                  | <span data-ttu-id="a2146-372">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-372">Yes</span></span>                  |
| <span data-ttu-id="a2146-373">iOS</span><span class="sxs-lookup"><span data-stu-id="a2146-373">iOS</span></span>         | <span data-ttu-id="a2146-374">いいえ</span><span class="sxs-lookup"><span data-stu-id="a2146-374">No</span></span>                   | <span data-ttu-id="a2146-375">はい</span><span class="sxs-lookup"><span data-stu-id="a2146-375">Yes</span></span>                  |

## <a name="supported-device-types-by-hardware-station-type"></a><span data-ttu-id="a2146-376">ハードウェア ステーションのタイプによりサポートされるデバイス タイプ</span><span class="sxs-lookup"><span data-stu-id="a2146-376">Supported device types by hardware station type</span></span>

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="a2146-377">IPC (組み込み) ハードウェア ステーションを含む Windows 用 Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-377">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a2146-378">サポートされているデバイス クラス</span><span class="sxs-lookup"><span data-stu-id="a2146-378">Supported device class</span></span></th>
<th><span data-ttu-id="a2146-379">サポートされているインターフェース</span><span class="sxs-lookup"><span data-stu-id="a2146-379">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a2146-380">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-380">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-381">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-381">OPOS</span></span></li>
<li><span data-ttu-id="a2146-382">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-382">Windows driver</span></span></li>
<li><span data-ttu-id="a2146-383">デバイス</span><span class="sxs-lookup"><span data-stu-id="a2146-383">Device</span></span></li>
<li><span data-ttu-id="a2146-384">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-384">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-385">プリンター 2</span><span class="sxs-lookup"><span data-stu-id="a2146-385">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-386">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-386">OPOS</span></span></li>
<li><span data-ttu-id="a2146-387">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-387">Windows driver</span></span></li>
<li><span data-ttu-id="a2146-388">デバイス</span><span class="sxs-lookup"><span data-stu-id="a2146-388">Device</span></span></li>
<li><span data-ttu-id="a2146-389">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-389">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-390">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="a2146-390">Line display</span></span></td>
<td><span data-ttu-id="a2146-391">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-391">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-392">デュアル ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="a2146-392">Dual display</span></span></td>
<td><span data-ttu-id="a2146-393">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-393">Windows driver</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-394">MSR</span><span class="sxs-lookup"><span data-stu-id="a2146-394">MSR</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-395">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-395">OPOS</span></span></li>
<li><span data-ttu-id="a2146-396">UWP (設定の必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a2146-396">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="a2146-397">キーボード ウェッジ (設定の必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a2146-397">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-398">ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-398">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-399">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-399">OPOS</span></span></li>
<li><span data-ttu-id="a2146-400">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-400">Network</span></span>
<p><span data-ttu-id="a2146-401"><strong>注記:</strong> <strong>共有シフトを使用</strong>がドロワーに設定されている場合、ドロワーは 1 つだけ設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-401"><strong>Note:</strong> Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-402">ドロワー 2</span><span class="sxs-lookup"><span data-stu-id="a2146-402">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-403">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-403">OPOS</span></span></li>
<li><span data-ttu-id="a2146-404">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-404">Network</span></span>
<p><span data-ttu-id="a2146-405"><strong>注記:</strong> <strong>共有シフトを使用</strong>がドロワーに設定されている場合、ドロワーは 1 つだけ設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-405"><strong>Note:</strong> Only one drawer can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-406">スキャナー</span><span class="sxs-lookup"><span data-stu-id="a2146-406">Scanner</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-407">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-407">OPOS</span></span></li>
<li><span data-ttu-id="a2146-408">UWP (設定の必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a2146-408">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="a2146-409">キーボード ウェッジ (設定の必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a2146-409">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-410">スキャナー 2</span><span class="sxs-lookup"><span data-stu-id="a2146-410">Scanner 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-411">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-411">OPOS</span></span></li>
<li><span data-ttu-id="a2146-412">UWP (設定の必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a2146-412">UWP (No setup is required.)</span></span></li>
<li><span data-ttu-id="a2146-413">キーボード ウェッジ (設定の必要はありません)。</span><span class="sxs-lookup"><span data-stu-id="a2146-413">Keyboard wedge (No setup is required.)</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-414">スケール</span><span class="sxs-lookup"><span data-stu-id="a2146-414">Scale</span></span></td>
<td><span data-ttu-id="a2146-415">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-415">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-416">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="a2146-416">PIN pad</span></span></td>
<td><span data-ttu-id="a2146-417">OPOS (サポートは、支払コネクタのカスタマイズによって提供されます)。</span><span class="sxs-lookup"><span data-stu-id="a2146-417">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-418">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="a2146-418">Signature capture</span></span></td>
<td><span data-ttu-id="a2146-419">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-419">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-420">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-420">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-421">カスタム デバイス サポート</span><span class="sxs-lookup"><span data-stu-id="a2146-421">Custom device support</span></span></li>
<li><span data-ttu-id="a2146-422">ネットワーク (詳細については、 支払コネクタのドキュメントを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="a2146-422">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a><span data-ttu-id="a2146-423">専用 IIS ハードウェア ステーションを持つすべての Modern POS クライアント</span><span class="sxs-lookup"><span data-stu-id="a2146-423">All Modern POS clients that have a dedicated IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-424">IIS ハードウェア ステーションが「専用」である場合、POS クライアントとハードウェア ステーション間には 1 対 1 の関係があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-424">When the IIS hardware station is "dedicated," there is a one-to-one relationship between the POS client and the hardware station.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a2146-425">サポートされているデバイス クラス</span><span class="sxs-lookup"><span data-stu-id="a2146-425">Supported device class</span></span></th>
<th><span data-ttu-id="a2146-426">サポートされているインターフェース</span><span class="sxs-lookup"><span data-stu-id="a2146-426">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a2146-427">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-427">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-428">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-428">OPOS</span></span></li>
<li><span data-ttu-id="a2146-429">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-429">Windows driver</span></span>
<p><span data-ttu-id="a2146-430"><strong>注記:</strong> ネットワーク上の Windows プリンターの場合、ハードウェア ステーションのユーザーはプリンターへのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-430"><strong>Note:</strong> For Windows printers on a network, the user of the hardware station must have permission to access the printer.</span></span></p>
</li>
<li><span data-ttu-id="a2146-431">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-431">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-432">プリンター 2</span><span class="sxs-lookup"><span data-stu-id="a2146-432">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-433">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-433">OPOS</span></span></li>
<li><span data-ttu-id="a2146-434">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-434">Windows driver</span></span></li>
<li><span data-ttu-id="a2146-435">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-435">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-436">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="a2146-436">Line display</span></span></td>
<td><span data-ttu-id="a2146-437">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-437">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-438">MSR</span><span class="sxs-lookup"><span data-stu-id="a2146-438">MSR</span></span></td>
<td><span data-ttu-id="a2146-439">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-439">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-440">ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-440">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-441">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-441">OPOS</span></span></li>
<li><span data-ttu-id="a2146-442">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-442">Network</span></span>
<p><span data-ttu-id="a2146-443"><strong>注記:</strong> <strong>共有シフトを使用</strong> が設定されている場合、ハードウェア プロファイルごとにドロワーは 1 つだけ設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-443"><strong>Note:</strong> Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-444">ドロワー 2</span><span class="sxs-lookup"><span data-stu-id="a2146-444">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-445">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-445">OPOS</span></span></li>
<li><span data-ttu-id="a2146-446">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-446">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-447">スキャナー</span><span class="sxs-lookup"><span data-stu-id="a2146-447">Scanner</span></span></td>
<td><span data-ttu-id="a2146-448">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-448">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-449">スキャナー 2</span><span class="sxs-lookup"><span data-stu-id="a2146-449">Scanner 2</span></span></td>
<td><span data-ttu-id="a2146-450">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-450">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-451">スケール</span><span class="sxs-lookup"><span data-stu-id="a2146-451">Scale</span></span></td>
<td><span data-ttu-id="a2146-452">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-452">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-453">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="a2146-453">PIN pad</span></span></td>
<td><span data-ttu-id="a2146-454">OPOS (サポートは、支払コネクタのカスタマイズによって提供されます)。</span><span class="sxs-lookup"><span data-stu-id="a2146-454">OPOS (Support is provided through customization of the payment connector.)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-455">Sig.</span><span class="sxs-lookup"><span data-stu-id="a2146-455">Sig.</span></span> <span data-ttu-id="a2146-456">キャプチャ</span><span class="sxs-lookup"><span data-stu-id="a2146-456">capture</span></span></td>
<td><span data-ttu-id="a2146-457">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-457">OPOS</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2146-458">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-458">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-459">カスタム デバイス サポート</span><span class="sxs-lookup"><span data-stu-id="a2146-459">Custom device support</span></span></li>
<li><span data-ttu-id="a2146-460">ネットワーク (詳細については、 支払コネクタのドキュメントを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="a2146-460">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="a2146-461">共有 IIS ハードウェア ステーションを持つすべての Modern POS クライアント</span><span class="sxs-lookup"><span data-stu-id="a2146-461">All Modern POS clients that have a shared IIS hardware station</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-462">IIS ハードウェア ステーションが「共有」の場合、複数のデバイスがハードウェア ステーションを同時に使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-462">When the IIS hardware station is "shared," multiple devices can use the hardware station at the same time.</span></span> <span data-ttu-id="a2146-463">このシナリオでは、次の表に示すデバイスのみを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-463">For this scenario, you should use only the devices that are listed in the following table.</span></span> <span data-ttu-id="a2146-464">バーコード スキャナーや MSR など、この表にないデバイスを共有しようとする場合、複数のデバイスが同じ周辺機器を要求しようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a2146-464">If you try to share devices that aren't listed here, such as bar code scanners and MSRs, errors will occur when multiple devices try to claim the same peripheral.</span></span> <span data-ttu-id="a2146-465">将来、そのようなコンフィギュレーションは明示的に禁止されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-465">In the future, such a configuration will be explicitly prevented.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="a2146-466">サポートされているデバイス クラス</span><span class="sxs-lookup"><span data-stu-id="a2146-466">Supported device class</span></span></th>
<th><span data-ttu-id="a2146-467">サポートされているインターフェース</span><span class="sxs-lookup"><span data-stu-id="a2146-467">Supported interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a2146-468">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-468">Printer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-469">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-469">OPOS</span></span></li>
<li><span data-ttu-id="a2146-470">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-470">Windows driver</span></span>
<p><span data-ttu-id="a2146-471"><strong>注記:</strong> ネットワーク上の Windows プリンターの場合、ハードウェア ステーションのユーザーはプリンターへのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-471"><strong>Note:</strong> For Windows printers on a network, the user of the hardware station must have permission to access the printer.</span></span></p>
</li>
<li><span data-ttu-id="a2146-472">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-472">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-473">プリンター 2</span><span class="sxs-lookup"><span data-stu-id="a2146-473">Printer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-474">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-474">OPOS</span></span></li>
<li><span data-ttu-id="a2146-475">Windows ドライバー</span><span class="sxs-lookup"><span data-stu-id="a2146-475">Windows driver</span></span></li>
<li><span data-ttu-id="a2146-476">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-476">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-477">ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-477">Drawer</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-478">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-478">OPOS</span></span></li>
<li><span data-ttu-id="a2146-479">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-479">Network</span></span>
<p><span data-ttu-id="a2146-480"><strong>注記:</strong> <strong>共有シフトを使用</strong> が設定されている場合、ハードウェア プロファイルごとにドロワーは 1 つだけ設定できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-480"><strong>Note:</strong> Only one drawer per hardware profile can be set up if <strong>Use shared shift</strong> is configured on the drawer.</span></span></p>
</li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-481">ドロワー 2</span><span class="sxs-lookup"><span data-stu-id="a2146-481">Drawer 2</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-482">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-482">OPOS</span></span></li>
<li><span data-ttu-id="a2146-483">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="a2146-483">Network</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="a2146-484">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-484">Payment terminal</span></span></td>
<td>
<ul>
<li><span data-ttu-id="a2146-485">カスタム デバイス サポート</span><span class="sxs-lookup"><span data-stu-id="a2146-485">Custom device support</span></span></li>
<li><span data-ttu-id="a2146-486">ネットワーク (詳細については、 支払コネクタのドキュメントを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="a2146-486">Network (For more information, see the payment connector documentation.)</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a><span data-ttu-id="a2146-487">サポートされるシナリオのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a2146-487">Configuration for supported scenarios</span></span>

<span data-ttu-id="a2146-488">ハードウェア プロファイルの作成方法の詳細については、[レジスターとハードウェア ステーションを含むチャネル クライアントの定義と管理](define-maintain-channel-clients-registers-hw-stations.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-488">For more information about how to create hardware profiles, see [Define and maintain channel clients, including registers and hardware stations](define-maintain-channel-clients-registers-hw-stations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-489">Retail バージョン 1611 では、ハードウェア ステーションのプロファイルは使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="a2146-489">For Retail version 1611, the hardware station profile is no longer used.</span></span> <span data-ttu-id="a2146-490">これまでハードウェア ステーションのプロファイルで設定されていた属性は、ハードウェア ステーション自体の一部になりました。</span><span class="sxs-lookup"><span data-stu-id="a2146-490">Attributes that you previously set up in the hardware station profile are now part of the hardware station itself.</span></span>

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a><span data-ttu-id="a2146-491">IPC (組み込み) ハードウェア ステーションを含む Windows 用 Modern POS</span><span class="sxs-lookup"><span data-stu-id="a2146-491">Modern POS for Windows with an IPC (built-in) hardware station</span></span>

<span data-ttu-id="a2146-492">このコンフィギュレーションは、従来の固定 POS レジスターの最も一般的なコンフィギュレーションです。</span><span class="sxs-lookup"><span data-stu-id="a2146-492">This configuration is the most typical configuration for traditional, fixed POS registers.</span></span> <span data-ttu-id="a2146-493">このシナリオでは、ハードウェア プロファイルの情報は、レジスタ自体に直接マップされます。</span><span class="sxs-lookup"><span data-stu-id="a2146-493">For this scenario, the hardware profile information is mapped directly to the register itself.</span></span> <span data-ttu-id="a2146-494">EFT ターミナル番号も、レジスタ自体に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-494">The EFT terminal number should also be set on the register itself.</span></span> <span data-ttu-id="a2146-495">このコンフィギュレーションを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a2146-495">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="a2146-496">すべての必須の周辺機器が設定されたハードウェア プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-496">Create a hardware profile where all the required peripherals are configured.</span></span>
2. <span data-ttu-id="a2146-497">POS レジスターにハードウェア プロファイルをマップします。</span><span class="sxs-lookup"><span data-stu-id="a2146-497">Map the hardware profile to the POS register.</span></span>
3. <span data-ttu-id="a2146-498">POS レジスタが使用される小売店舗用に**専用**タイプのハードウェア ステーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-498">Create a hardware station of the **Dedicated** type for the retail store where the POS register will be used.</span></span> <span data-ttu-id="a2146-499">説明がオプションです。</span><span class="sxs-lookup"><span data-stu-id="a2146-499">A description is optional.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2146-500">ハードウェア ステーションに他のプロパティを設定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a2146-500">You don't have to set any other properties on the hardware station.</span></span> <span data-ttu-id="a2146-501">ハードウェア プロファイルなど他の必須情報はすべて、レジスタ自体から取得されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-501">All other required information, such as the hardware profile, will come from the register itself.</span></span>

4. <span data-ttu-id="a2146-502">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-502">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
5. <span data-ttu-id="a2146-503">店舗に新しいハードウェア プロファイルを同期させるため、**1090** 配分スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-503">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="a2146-504">POS に変更を同期させるため、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-504">Click **Run now** to sync changes to the POS.</span></span>
6. <span data-ttu-id="a2146-505">店舗に新しいハードウェア ステーションを同期させるため、**1070** 配分スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-505">Select the **1070** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="a2146-506">POS に変更を同期させるため、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-506">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="a2146-507">Windows 用 Modern POS をインストールして有効化します。</span><span class="sxs-lookup"><span data-stu-id="a2146-507">Install and activate Modern POS for Windows.</span></span>
8. <span data-ttu-id="a2146-508">Windows 用 Modern POS を起動し、接続されている周辺機器の使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="a2146-508">Start Modern POS for Windows, and begin to use the connected peripheral devices.</span></span>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a><span data-ttu-id="a2146-509">専用 IIS ハードウェア ステーションを持つすべての Modern POS クライアント</span><span class="sxs-lookup"><span data-stu-id="a2146-509">All Modern POS clients that have a dedicated IIS hardware station</span></span>

<span data-ttu-id="a2146-510">1 つの POS レジスター専用で使用されているハードウェア ステーションを持つすべての Modern POS クライアントに、このコンフィギュレーションは使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-510">This configuration can be used for all Modern POS clients that have a hardware station that is used exclusively by one POS register.</span></span> <span data-ttu-id="a2146-511">このコンフィギュレーションを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a2146-511">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="a2146-512">すべての必須の周辺機器が設定されたハードウェア プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-512">Create a hardware profile where all the required peripherals are configured.</span></span>
2. <span data-ttu-id="a2146-513">POS レジスタが使用される小売店舗用に**専用**タイプのハードウェア ステーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-513">Create a hardware station of the **Dedicated** type for the retail store where the POS register will be used.</span></span>
3. <span data-ttu-id="a2146-514">専用のハードウェア ステーションで、次のプロパティを設定します:</span><span class="sxs-lookup"><span data-stu-id="a2146-514">On the dedicated hardware station, set the following properties:</span></span>

    - <span data-ttu-id="a2146-515">**ホスト名** – ハードウェア ステーションをホストするコンピュータの名前。</span><span class="sxs-lookup"><span data-stu-id="a2146-515">**Host name** – The name of the host computer where the hardware station will run.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a2146-516">クラウド POS の場合、クラウド POS が実行されているローカル コンピュータの特定は **localhost** の使用で解決できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-516">Cloud POS can resolve **localhost** to determine the local computer where Cloud POS is running.</span></span> <span data-ttu-id="a2146-517">ただし、クラウド POS とハードウェア ステーションのペアリングに必要な証明書は、コンピュータ名が「Localhost」となっている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-517">However, the certificate that is required in order to pair Cloud POS with the hardware station must also have "Localhost" as the computer name.</span></span> <span data-ttu-id="a2146-518">問題を回避するには、必要に応じて、店舗の各専用ハードウェア ステーションのインスタンス一覧をリストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a2146-518">To avoid issues, we recommend that you list an instance of each dedicated hardware station for the store, as required.</span></span> <span data-ttu-id="a2146-519">各ハードウェア ステーション毎に、ハードウェア ステーションが配置される特定のコンピュータ名がホスト名となる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-519">For each hardware station, the host name should be the specific computer name where the hardware station will be deployed.</span></span>

    - <span data-ttu-id="a2146-520">**ポート** – ハードウェア ステーションが Modern POS クライアントとの通信に使用するポート。</span><span class="sxs-lookup"><span data-stu-id="a2146-520">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    - <span data-ttu-id="a2146-521">**ハードウェア プロファイル** – ハードウェア ステーション自体にハードウェア プロファイルが提供されない場合、レジスターに割り当てられているハードウェア プロファイルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-521">**Hardware profile** – If the hardware profile isn't provided on the hardware station itself, the hardware profile that is assigned to the register will be used.</span></span>
    - <span data-ttu-id="a2146-522">**EFT POS の数** – EFT 認証の送信に使用する EFT ターミナル ID。</span><span class="sxs-lookup"><span data-stu-id="a2146-522">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="a2146-523">この ID は、クレジット カード プロセッサによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-523">This ID is provided by the credit card processor.</span></span>
    - <span data-ttu-id="a2146-524">**パッケージ名** – ハードウェア ステーションの配置に使用するハードウェア ステーション パッケージ。</span><span class="sxs-lookup"><span data-stu-id="a2146-524">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4. <span data-ttu-id="a2146-525">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-525">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
5. <span data-ttu-id="a2146-526">店舗に新しいハードウェア プロファイルを同期させるため、**1090** 配分スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-526">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="a2146-527">POS に変更を同期させるため、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-527">Click **Run now** to sync changes to the POS.</span></span>
6. <span data-ttu-id="a2146-528">店舗に新しいハードウェア ステーションを同期させるため、**1040** 配分スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-528">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="a2146-529">POS に変更を同期させるため、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-529">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="a2146-530">ハードウェア ステーションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="a2146-530">Install the hardware station.</span></span> <span data-ttu-id="a2146-531">ハードウェア ステーションをインストールする方法の詳細については、[Retail ハードウェア ステーションのコンフィギュレーションとインストール](retail-hardware-station-configuration-installation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-531">For more information about how to install the hardware station, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>
8. <span data-ttu-id="a2146-532">Modern POS をインストールして有効化します。</span><span class="sxs-lookup"><span data-stu-id="a2146-532">Install and activate Modern POS.</span></span> <span data-ttu-id="a2146-533">Modern POS をインストールする方法の詳細については、「[Retail Modern POS のコンフィギュレーションとインストール](retail-modern-pos-device-activation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-533">For more information about how to install Modern POS, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>
9. <span data-ttu-id="a2146-534">Modern POS にサイン インするには、**非ドロワー操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-534">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
10. <span data-ttu-id="a2146-535">**ハードウェア ステーションの管理**操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="a2146-535">Start the **Manage hardware stations** operation.</span></span>
11. <span data-ttu-id="a2146-536">**管理** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-536">Click **Manage**.</span></span>
12. <span data-ttu-id="a2146-537">ハードウェア ステーションの管理ページで、ハードウェア ステーションを起動するオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2146-537">On the hardware station management page, set the option to turn on the hardware station.</span></span>
13. <span data-ttu-id="a2146-538">使用するハードウェア ステーションを選択し、**ペア** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-538">Select the hardware station to use, and then click **Pair**.</span></span>
14. <span data-ttu-id="a2146-539">ハードウェア ステーションのペアリングが終わった後、**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-539">After the hardware station is paired, click **Close**.</span></span>
15. <span data-ttu-id="a2146-540">ハードウェア ステータスの選択ページで、最後に選択されたハードウェア ステーションをクリックして有効にします。</span><span class="sxs-lookup"><span data-stu-id="a2146-540">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a><span data-ttu-id="a2146-541">共有 IIS ハードウェア ステーションを持つすべての Modern POS クライアント</span><span class="sxs-lookup"><span data-stu-id="a2146-541">All Modern POS clients that have a shared IIS hardware station</span></span>

<span data-ttu-id="a2146-542">このコンフィギュレーションは、他のデバイスとハードウェア ステーションを共有するすべての Modern POS クライアントで使用できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-542">This configuration can be used for all Modern POS clients that share hardware stations with other devices.</span></span> <span data-ttu-id="a2146-543">このコンフィギュレーションを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a2146-543">To set up this configuration, follow these steps.</span></span>

1. <span data-ttu-id="a2146-544">必須の周辺機器が設定されたハードウェア プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-544">Create a hardware profile where the required peripherals are configured.</span></span>
2. <span data-ttu-id="a2146-545">POS レジスタが使用される小売店舗用に**共有**タイプのハードウェア ステーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="a2146-545">Create a hardware station of the **Shared** type for the retail store where the POS register will be used.</span></span>
3. <span data-ttu-id="a2146-546">共有のハードウェア ステーションで、次のプロパティを設定します:</span><span class="sxs-lookup"><span data-stu-id="a2146-546">On the shared hardware station, set the following properties:</span></span>

    - <span data-ttu-id="a2146-547">**ホスト名** – ハードウェア ステーションをホストするコンピュータの名前。</span><span class="sxs-lookup"><span data-stu-id="a2146-547">**Host name** – The name of the host computer where the hardware station will run.</span></span>
    - <span data-ttu-id="a2146-548">**説明** – ハードウェア ステーションを識別する助けとなるテキスト、**返品**または**店の前**など。</span><span class="sxs-lookup"><span data-stu-id="a2146-548">**Description** – Text that will help identify the hardware station, such as **Returns** or **Front of store**.</span></span>
    - <span data-ttu-id="a2146-549">**ポート** – ハードウェア ステーションが Modern POS クライアントとの通信に使用するポート。</span><span class="sxs-lookup"><span data-stu-id="a2146-549">**Port** – The port to use for the hardware station to communicate with the Modern POS client.</span></span>
    - <span data-ttu-id="a2146-550">**ハードウェア プロファイル** – 共有ハードウェア ステーションの場合、各ハードウェア ステーションにハードウェア プロファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-550">**Hardware profile** – For shared hardware stations, each hardware station should have a hardware profile.</span></span> <span data-ttu-id="a2146-551">ハードウェア プロファイルはハードウェア ステーション間で共有できます。しかし、各ハードウェア ステーションにマップされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-551">Hardware profiles can be shared among hardware stations, but they must be mapped to each hardware station.</span></span> <span data-ttu-id="a2146-552">また、複数のデバイスが同じ共有ハードウェア ステーションを使用する場合、共有シフトの使用をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a2146-552">In addition, we recommend that you use shared shifts when multiple devices use the same shared hardware station.</span></span> <span data-ttu-id="a2146-553">共有シフトの設定には、**小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-553">To set up a shared shift, click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span> <span data-ttu-id="a2146-554">個々の共有ハードウェア プロファイルでキャッシュ ドロワーを選択し、**共有シフト ドロワー** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2146-554">For each shared hardware profile, select the cash drawer, and set the **Shared shift drawer** option to **Yes**.</span></span>
    - <span data-ttu-id="a2146-555">**EFT POS の数** – EFT 認証の送信に使用する EFT ターミナル ID。</span><span class="sxs-lookup"><span data-stu-id="a2146-555">**EFT POS number** – The EFT terminal ID to use when EFT authorizations are sent.</span></span> <span data-ttu-id="a2146-556">この ID は、クレジット カード プロセッサによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-556">This ID is provided by the credit card processor.</span></span>
    - <span data-ttu-id="a2146-557">**パッケージ名** – ハードウェア ステーションの配置に使用するハードウェア ステーション パッケージ。</span><span class="sxs-lookup"><span data-stu-id="a2146-557">**Package name** – The hardware station package to use when the hardware station is deployed.</span></span>

4. <span data-ttu-id="a2146-558">店舗に必要な各追加ハードウェア ステーションについて、手順 2 と 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a2146-558">Repeat steps 2 and 3 for each additional hardware station that is required in the store.</span></span>
5. <span data-ttu-id="a2146-559">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-559">Click **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
6. <span data-ttu-id="a2146-560">店舗に新しいハードウェア プロファイルを同期させるため、**1090** 配分スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-560">Select the **1090** distribution schedule to sync the new hardware profile to the store.</span></span> <span data-ttu-id="a2146-561">POS に変更を同期させるため、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-561">Click **Run now** to sync changes to the POS.</span></span>
7. <span data-ttu-id="a2146-562">店舗に新しいハードウェア ステーションを同期させるため、**1040** 配分スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-562">Select the **1040** distribution schedule to sync the new hardware station to the store.</span></span> <span data-ttu-id="a2146-563">POS に変更を同期させるため、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-563">Click **Run now** to sync changes to the POS.</span></span>
8. <span data-ttu-id="a2146-564">手順 2 と 3 で設定したハードウェア ステーションを、各ホスト コンピューターにインストールします。</span><span class="sxs-lookup"><span data-stu-id="a2146-564">Install the hardware station on each host computer that you set up in steps 2 and 3.</span></span> <span data-ttu-id="a2146-565">ハードウェア ステーションをインストールする方法の詳細については、[Retail ハードウェア ステーションのコンフィギュレーションとインストール](retail-hardware-station-configuration-installation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-565">For more information about how to install the hardware station, see [Retail hardware station configuration and installation](retail-hardware-station-configuration-installation.md).</span></span>
9. <span data-ttu-id="a2146-566">Modern POS をインストールして有効化します。</span><span class="sxs-lookup"><span data-stu-id="a2146-566">Install and activate Modern POS.</span></span> <span data-ttu-id="a2146-567">Modern POS をインストールする方法の詳細については、「[Retail Modern POS のコンフィギュレーションとインストール](retail-modern-pos-device-activation.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-567">For more information about how to install Modern POS, see [Retail Modern POS configuration and installation](retail-modern-pos-device-activation.md).</span></span>
10. <span data-ttu-id="a2146-568">Modern POS にサイン インするには、**非ドロワー操作の実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a2146-568">Sign in to Modern POS, and select **Perform non-drawer operations**.</span></span>
11. <span data-ttu-id="a2146-569">**ハードウェア ステーションの管理**操作を開始します。</span><span class="sxs-lookup"><span data-stu-id="a2146-569">Start the **Manage hardware stations** operation.</span></span>
12. <span data-ttu-id="a2146-570">**管理** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-570">Click **Manage**.</span></span>
13. <span data-ttu-id="a2146-571">ハードウェア ステーションの管理ページで、ハードウェア ステーションを起動するオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="a2146-571">On the hardware station management page, set the option to turn on the hardware station.</span></span>
14. <span data-ttu-id="a2146-572">使用するハードウェア ステーションを選択し、**ペア** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-572">Select the hardware station to use, and then click **Pair**.</span></span>
15. <span data-ttu-id="a2146-573">Modern POS が使用する各ハードウェア ステーションについて、手順 14 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="a2146-573">Repeat step 14 for each hardware station that Modern POS will use.</span></span>
16. <span data-ttu-id="a2146-574">すべての必要なハードウェア ステーションのペアリングが終了したら、**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-574">After all the required hardware stations are paired, click **Close**.</span></span>
17. <span data-ttu-id="a2146-575">ハードウェア ステータスの選択ページで、最後に選択されたハードウェア ステーションをクリックして有効にします。</span><span class="sxs-lookup"><span data-stu-id="a2146-575">On the hardware station selection page, click the recently selected hardware station to make it active.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2146-576">デバイスが異なるハードウェア ステーションをしばしば使用する場合、支払/入金プロセスを開始するときにレジ担当者がハードウェア ステーションを選択するよう促すようにように Modern POS を設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a2146-576">If devices often use different hardware stations, we recommend that you configure Modern POS to prompt cashiers to select a hardware station when they begin the tender process.</span></span> <span data-ttu-id="a2146-577">**小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **レジスター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-577">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span> <span data-ttu-id="a2146-578">レジスターを選択し、**支払/入金での選択** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a2146-578">Select the register, and then set the **Select upon tender** option to **Yes**.</span></span> <span data-ttu-id="a2146-579">チャンネル データベースへの同期変更に、**1090** 配送スケジュールを使用します。</span><span class="sxs-lookup"><span data-stu-id="a2146-579">Use the **1090** distribution schedule to sync changes to the channel database.</span></span>

## <a name="extensibility"></a><span data-ttu-id="a2146-580">拡張性</span><span class="sxs-lookup"><span data-stu-id="a2146-580">Extensibility</span></span>

<span data-ttu-id="a2146-581">ハードウェア ステーションの拡張性のシナリオの情報については [ハードウェア ステーションの拡張](dev-itpro/hardware-station-extensibility.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-581">For information about extensibility scenarios for the hardware station, see [Hardware Station extensibility](dev-itpro/hardware-station-extensibility.md).</span></span>

## <a name="security"></a><span data-ttu-id="a2146-582">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="a2146-582">Security</span></span>

<span data-ttu-id="a2146-583">現在のセキュリティ基準によると、実稼動環境で次の設定をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-583">According to current security standards, the following settings should be used in a production environment:</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-584">ハードウェア ステーションのインストーラーは、セルフサービスによるインストールの一部として、これらのレジストリの編集を自動的に行います。</span><span class="sxs-lookup"><span data-stu-id="a2146-584">The hardware station installer will automatically make these registry edits as part of the installation through self-service.</span></span>

- <span data-ttu-id="a2146-585">Secure Sockets Layer (SSL) は無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-585">Secure Sockets Layer (SSL) should be disabled.</span></span>
- <span data-ttu-id="a2146-586">Transport Layer Security (TLS) version 1.2 (または現行最新バージョン) のみを有効にして使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-586">Only Transport Layer Security (TLS) version 1.2 (or the current highest version) should be enabled and used.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a2146-587">既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効です。</span><span class="sxs-lookup"><span data-stu-id="a2146-587">By default, SSL and all versions of TLS except TLS 1.2 are disabled.</span></span>

    <span data-ttu-id="a2146-588">これらを値の編集または有効化するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a2146-588">To edit or enable these values, follow these steps:</span></span>

    1. <span data-ttu-id="a2146-589">Windows ロゴキーと R キーを同時に押して、**実行**ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="a2146-589">Press the Windows logo key+R to open a **Run** window.</span></span>
    2. <span data-ttu-id="a2146-590">**オープン** フィールドで **Regedit** とタイプし、次に **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-590">In the **Open** field, type **Regedit**, and then click **OK**.</span></span>
    3. <span data-ttu-id="a2146-591">**ユーザー アカウント コントロール** メッセージ ボックス現われたら、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-591">If a **User Account Control** message box appears, click **Yes**.</span></span>
    4. <span data-ttu-id="a2146-592">**Registry Editor** ウィンドウで、**HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2146-592">In the **Registry Editor** window, navigate to **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**.</span></span> <span data-ttu-id="a2146-593">TLS 1.2 のみを有効にするために、以下のキーは自動的に挿入されています:</span><span class="sxs-lookup"><span data-stu-id="a2146-593">The following keys have been automatically entered to allow for TLS 1.2 only:</span></span>

        - <span data-ttu-id="a2146-594">TLS 1.2Server:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="a2146-594">TLS 1.2Server:Enabled=1</span></span>
        - <span data-ttu-id="a2146-595">TLS 1.2Server:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="a2146-595">TLS 1.2Server:DisabledByDefault=0</span></span>
        - <span data-ttu-id="a2146-596">TLS 1.2Client:Enabled=1</span><span class="sxs-lookup"><span data-stu-id="a2146-596">TLS 1.2Client:Enabled=1</span></span>
        - <span data-ttu-id="a2146-597">TLS 1.2Client:DisabledByDefault=0</span><span class="sxs-lookup"><span data-stu-id="a2146-597">TLS 1.2Client:DisabledByDefault=0</span></span>
        - <span data-ttu-id="a2146-598">TLS 1.1Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-598">TLS 1.1Server:Enabled=0</span></span>
        - <span data-ttu-id="a2146-599">TLS 1.1Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-599">TLS 1.1Client:Enabled=0</span></span>
        - <span data-ttu-id="a2146-600">TLS 1.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-600">TLS 1.0Server:Enabled=0</span></span>
        - <span data-ttu-id="a2146-601">TLS 1.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-601">TLS 1.0Client:Enabled=0</span></span>
        - <span data-ttu-id="a2146-602">SSL 3.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-602">SSL 3.0Server:Enabled=0</span></span>
        - <span data-ttu-id="a2146-603">SSL 3.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-603">SSL 3.0Client:Enabled=0</span></span>
        - <span data-ttu-id="a2146-604">SSL 2.0Server:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-604">SSL 2.0Server:Enabled=0</span></span>
        - <span data-ttu-id="a2146-605">SSL 2.0Client:Enabled=0</span><span class="sxs-lookup"><span data-stu-id="a2146-605">SSL 2.0Client:Enabled=0</span></span>

- <span data-ttu-id="a2146-606">知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。</span><span class="sxs-lookup"><span data-stu-id="a2146-606">No additional network ports should be open, unless they are required for known, specified reasons.</span></span>
- <span data-ttu-id="a2146-607">クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2146-607">Cross-origin resource sharing must be disabled and must specify the allowed origins that are accepted.</span></span>
- <span data-ttu-id="a2146-608">ハードウェア ステーションを実行するコンピュータで使用する証明書の取得には、信頼された証明機関のみを使用してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-608">Only trusted certificate authorities should be used to obtain certificates that will be used on computers that run the hardware station.</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-609">IIS と Payment Card Industry (PCI) 要件のセキュリティ ガイドラインを確認することが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="a2146-609">It's very important that you review security guidelines for IIS and the Payment Card Industry (PCI) requirements.</span></span>

## <a name="peripheral-simulator"></a><span data-ttu-id="a2146-610">周辺機器シミュレーター</span><span class="sxs-lookup"><span data-stu-id="a2146-610">Peripheral simulator</span></span>

<span data-ttu-id="a2146-611">詳細については、[Retail 周辺機器シミュレーター](dev-itpro/retail-peripheral-simulator.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-611">For information, see [Retail peripheral simulator](dev-itpro/retail-peripheral-simulator.md).</span></span>

## <a name="microsoft-tested-peripheral-devices"></a><span data-ttu-id="a2146-612">マイクロソフトでテストされた周辺機器</span><span class="sxs-lookup"><span data-stu-id="a2146-612">Microsoft-tested peripheral devices</span></span>

### <a name="ipc-built-in-hardware-station"></a><span data-ttu-id="a2146-613">IPC (組み込み) ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-613">IPC (built-in) hardware station</span></span>

<span data-ttu-id="a2146-614">次の周辺機器は、Windows 用 Modern POS に組み込まれた IPC ハードウェア ステーションを使用してテストされています。</span><span class="sxs-lookup"><span data-stu-id="a2146-614">The following peripherals were tested by using the IPC hardware station that is built into Modern POS for Windows.</span></span>

#### <a name="printer"></a><span data-ttu-id="a2146-615">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-615">Printer</span></span>

| <span data-ttu-id="a2146-616">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-616">Manufacturer</span></span> | <span data-ttu-id="a2146-617">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-617">Model</span></span>      | <span data-ttu-id="a2146-618">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-618">Interface</span></span> | <span data-ttu-id="a2146-619">備考</span><span class="sxs-lookup"><span data-stu-id="a2146-619">Comments</span></span>                |
|--------------|------------|-----------|-------------------------|
| <span data-ttu-id="a2146-620">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-620">Epson</span></span>        | <span data-ttu-id="a2146-621">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="a2146-621">Tm-T88IV</span></span>   | <span data-ttu-id="a2146-622">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-622">OPOS</span></span>      |                         |
| <span data-ttu-id="a2146-623">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-623">Epson</span></span>        | <span data-ttu-id="a2146-624">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="a2146-624">TM-T88V</span></span>    | <span data-ttu-id="a2146-625">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-625">OPOS</span></span>      |                         |
| <span data-ttu-id="a2146-626">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-626">Epson</span></span>        | <span data-ttu-id="a2146-627">ePOS-Print</span><span class="sxs-lookup"><span data-stu-id="a2146-627">ePOS-Print</span></span> | <span data-ttu-id="a2146-628">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-628">Custom</span></span>    | <span data-ttu-id="a2146-629">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-629">Connected via network</span></span>   |
| <span data-ttu-id="a2146-630">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-630">Star</span></span>         | <span data-ttu-id="a2146-631">TSP650II</span><span class="sxs-lookup"><span data-stu-id="a2146-631">TSP650II</span></span>   | <span data-ttu-id="a2146-632">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-632">OPOS</span></span>      |                         |
| <span data-ttu-id="a2146-633">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-633">Star</span></span>         | <span data-ttu-id="a2146-634">TSP650II</span><span class="sxs-lookup"><span data-stu-id="a2146-634">TSP650II</span></span>   | <span data-ttu-id="a2146-635">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-635">Custom</span></span>    | <span data-ttu-id="a2146-636">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-636">Connected via network</span></span>   |
| <span data-ttu-id="a2146-637">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-637">Star</span></span>         | <span data-ttu-id="a2146-638">mPOP</span><span class="sxs-lookup"><span data-stu-id="a2146-638">mPOP</span></span>       | <span data-ttu-id="a2146-639">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-639">OPOS</span></span>      | <span data-ttu-id="a2146-640">Bluetooth 経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-640">Connected via Bluetooth</span></span> |
| <span data-ttu-id="a2146-641">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-641">HP</span></span>           | <span data-ttu-id="a2146-642">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="a2146-642">F7M67AA</span></span>    | <span data-ttu-id="a2146-643">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-643">OPOS</span></span>      | <span data-ttu-id="a2146-644">Powered USB</span><span class="sxs-lookup"><span data-stu-id="a2146-644">Powered USB</span></span>             |

#### <a name="bar-code-scanner"></a><span data-ttu-id="a2146-645">バーコード スキャナー</span><span class="sxs-lookup"><span data-stu-id="a2146-645">Bar code scanner</span></span>

| <span data-ttu-id="a2146-646">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-646">Manufacturer</span></span>  | <span data-ttu-id="a2146-647">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-647">Model</span></span>         | <span data-ttu-id="a2146-648">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-648">Interface</span></span> | <span data-ttu-id="a2146-649">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-649">Comments</span></span> |
|---------------|---------------|-----------|----------|
| <span data-ttu-id="a2146-650">Motorola</span><span class="sxs-lookup"><span data-stu-id="a2146-650">Motorola</span></span>      | <span data-ttu-id="a2146-651">DS9208</span><span class="sxs-lookup"><span data-stu-id="a2146-651">DS9208</span></span>        | <span data-ttu-id="a2146-652">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-652">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-653">ハネウェル</span><span class="sxs-lookup"><span data-stu-id="a2146-653">Honeywell</span></span>     | <span data-ttu-id="a2146-654">1900</span><span class="sxs-lookup"><span data-stu-id="a2146-654">1900</span></span>          | <span data-ttu-id="a2146-655">UWP</span><span class="sxs-lookup"><span data-stu-id="a2146-655">UWP</span></span>       |          |
| <span data-ttu-id="a2146-656">記号</span><span class="sxs-lookup"><span data-stu-id="a2146-656">Symbol</span></span>        | <span data-ttu-id="a2146-657">LS2208</span><span class="sxs-lookup"><span data-stu-id="a2146-657">LS2208</span></span>        | <span data-ttu-id="a2146-658">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-658">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-659">HP 統合済</span><span class="sxs-lookup"><span data-stu-id="a2146-659">HP Integrated</span></span> | <span data-ttu-id="a2146-660">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="a2146-660">E1L07AA</span></span>       | <span data-ttu-id="a2146-661">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-661">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-662">Datalogic</span><span class="sxs-lookup"><span data-stu-id="a2146-662">Datalogic</span></span>     | <span data-ttu-id="a2146-663">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="a2146-663">Magellan 8400</span></span> | <span data-ttu-id="a2146-664">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-664">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="a2146-665">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="a2146-665">PIN pad</span></span>

| <span data-ttu-id="a2146-666">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-666">Manufacturer</span></span> | <span data-ttu-id="a2146-667">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-667">Model</span></span>  | <span data-ttu-id="a2146-668">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-668">Interface</span></span> | <span data-ttu-id="a2146-669">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-669">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="a2146-670">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-670">VeriFone</span></span>     | <span data-ttu-id="a2146-671">1000SE</span><span class="sxs-lookup"><span data-stu-id="a2146-671">1000SE</span></span> | <span data-ttu-id="a2146-672">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-672">OPOS</span></span>      | <span data-ttu-id="a2146-673">支払コネクターのカスタマイズが必要</span><span class="sxs-lookup"><span data-stu-id="a2146-673">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="a2146-674">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-674">Payment terminal</span></span>

| <span data-ttu-id="a2146-675">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-675">Manufacturer</span></span> | <span data-ttu-id="a2146-676">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-676">Model</span></span>        | <span data-ttu-id="a2146-677">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-677">Interface</span></span> | <span data-ttu-id="a2146-678">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-678">Comments</span></span>                                                                       |
|--------------|--------------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a2146-679">Equinox</span><span class="sxs-lookup"><span data-stu-id="a2146-679">Equinox</span></span>      | <span data-ttu-id="a2146-680">L5300</span><span class="sxs-lookup"><span data-stu-id="a2146-680">L5300</span></span>        | <span data-ttu-id="a2146-681">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-681">Custom</span></span>    | <span data-ttu-id="a2146-682">支払コネクターのカスタマイズが必要</span><span class="sxs-lookup"><span data-stu-id="a2146-682">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="a2146-683">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-683">VeriFone</span></span>     | <span data-ttu-id="a2146-684">MX925</span><span class="sxs-lookup"><span data-stu-id="a2146-684">MX925</span></span>        | <span data-ttu-id="a2146-685">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-685">Custom</span></span>    | <span data-ttu-id="a2146-686">支払コネクターのカスタマイズが必要。ネットワークおよびUSB接続</span><span class="sxs-lookup"><span data-stu-id="a2146-686">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="a2146-687">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-687">VeriFone</span></span>     | <span data-ttu-id="a2146-688">MX915</span><span class="sxs-lookup"><span data-stu-id="a2146-688">MX915</span></span>        | <span data-ttu-id="a2146-689">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-689">Custom</span></span>    | <span data-ttu-id="a2146-690">支払コネクターのカスタマイズが必要。ネットワークおよびUSB接続</span><span class="sxs-lookup"><span data-stu-id="a2146-690">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="a2146-691">Verifone</span><span class="sxs-lookup"><span data-stu-id="a2146-691">Verifone</span></span>     | <span data-ttu-id="a2146-692">コメントの確認</span><span class="sxs-lookup"><span data-stu-id="a2146-692">See comments</span></span> | <span data-ttu-id="a2146-693">Adyen</span><span class="sxs-lookup"><span data-stu-id="a2146-693">Adyen</span></span>     | <span data-ttu-id="a2146-694">Adyen コネクタは、[ここ](https://www.adyen.com/pos-payments/terminals) に表示されるすべてのデバイスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a2146-694">The Adyen connector supports all devices listed [here](https://www.adyen.com/pos-payments/terminals)</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="a2146-695">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-695">Cash drawer</span></span>

| <span data-ttu-id="a2146-696">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-696">Manufacturer</span></span> | <span data-ttu-id="a2146-697">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-697">Model</span></span>     | <span data-ttu-id="a2146-698">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-698">Interface</span></span> | <span data-ttu-id="a2146-699">備考</span><span class="sxs-lookup"><span data-stu-id="a2146-699">Comments</span></span>                |
|--------------|-----------|-----------|-------------------------|
| <span data-ttu-id="a2146-700">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-700">Star</span></span>         | <span data-ttu-id="a2146-701">mPOP</span><span class="sxs-lookup"><span data-stu-id="a2146-701">mPOP</span></span>      | <span data-ttu-id="a2146-702">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-702">OPOS</span></span>      | <span data-ttu-id="a2146-703">Bluetooth 経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-703">Connected via Bluetooth</span></span> |
| <span data-ttu-id="a2146-704">APG</span><span class="sxs-lookup"><span data-stu-id="a2146-704">APG</span></span>          | <span data-ttu-id="a2146-705">Atwood</span><span class="sxs-lookup"><span data-stu-id="a2146-705">Atwood</span></span>    | <span data-ttu-id="a2146-706">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-706">Custom</span></span>    | <span data-ttu-id="a2146-707">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-707">Connected via network</span></span>   |
| <span data-ttu-id="a2146-708">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-708">Star</span></span>         | <span data-ttu-id="a2146-709">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="a2146-709">SMD2-1317</span></span> | <span data-ttu-id="a2146-710">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-710">OPOS</span></span>      |                         |
| <span data-ttu-id="a2146-711">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-711">HP</span></span>           | <span data-ttu-id="a2146-712">QT457AA</span><span class="sxs-lookup"><span data-stu-id="a2146-712">QT457AA</span></span>   | <span data-ttu-id="a2146-713">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-713">OPOS</span></span>      |                         |

#### <a name="line-display"></a><span data-ttu-id="a2146-714">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="a2146-714">Line display</span></span>

| <span data-ttu-id="a2146-715">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-715">Manufacturer</span></span>  | <span data-ttu-id="a2146-716">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-716">Model</span></span>   | <span data-ttu-id="a2146-717">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-717">Interface</span></span> | <span data-ttu-id="a2146-718">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-718">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="a2146-719">HP 統合済</span><span class="sxs-lookup"><span data-stu-id="a2146-719">HP integrated</span></span> | <span data-ttu-id="a2146-720">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="a2146-720">G6U79AA</span></span> | <span data-ttu-id="a2146-721">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-721">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-722">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-722">Epson</span></span>         | <span data-ttu-id="a2146-723">M58DC</span><span class="sxs-lookup"><span data-stu-id="a2146-723">M58DC</span></span>   | <span data-ttu-id="a2146-724">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-724">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="a2146-725">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="a2146-725">Signature capture</span></span>

| <span data-ttu-id="a2146-726">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-726">Manufacturer</span></span> | <span data-ttu-id="a2146-727">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-727">Model</span></span>  | <span data-ttu-id="a2146-728">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-728">Interface</span></span> | <span data-ttu-id="a2146-729">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-729">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="a2146-730">Scriptel</span><span class="sxs-lookup"><span data-stu-id="a2146-730">Scriptel</span></span>     | <span data-ttu-id="a2146-731">ST1550</span><span class="sxs-lookup"><span data-stu-id="a2146-731">ST1550</span></span> | <span data-ttu-id="a2146-732">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-732">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="a2146-733">スケール</span><span class="sxs-lookup"><span data-stu-id="a2146-733">Scale</span></span>

| <span data-ttu-id="a2146-734">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-734">Manufacturer</span></span> | <span data-ttu-id="a2146-735">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-735">Model</span></span>         | <span data-ttu-id="a2146-736">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-736">Interface</span></span> | <span data-ttu-id="a2146-737">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-737">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="a2146-738">Datalogic</span><span class="sxs-lookup"><span data-stu-id="a2146-738">Datalogic</span></span>    | <span data-ttu-id="a2146-739">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="a2146-739">Magellan 8400</span></span> | <span data-ttu-id="a2146-740">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-740">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="a2146-741">MSR</span><span class="sxs-lookup"><span data-stu-id="a2146-741">MSR</span></span>

| <span data-ttu-id="a2146-742">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-742">Manufacturer</span></span> | <span data-ttu-id="a2146-743">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-743">Model</span></span>       | <span data-ttu-id="a2146-744">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-744">Interface</span></span> | <span data-ttu-id="a2146-745">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-745">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="a2146-746">Magtek</span><span class="sxs-lookup"><span data-stu-id="a2146-746">Magtek</span></span>       | <span data-ttu-id="a2146-747">21073075</span><span class="sxs-lookup"><span data-stu-id="a2146-747">21073075</span></span>    | <span data-ttu-id="a2146-748">UWP</span><span class="sxs-lookup"><span data-stu-id="a2146-748">UWP</span></span>       |          |
| <span data-ttu-id="a2146-749">Magtek</span><span class="sxs-lookup"><span data-stu-id="a2146-749">Magtek</span></span>       | <span data-ttu-id="a2146-750">21073062</span><span class="sxs-lookup"><span data-stu-id="a2146-750">21073062</span></span>    | <span data-ttu-id="a2146-751">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-751">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-752">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-752">HP</span></span>           | <span data-ttu-id="a2146-753">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="a2146-753">IDRA-334133</span></span> | <span data-ttu-id="a2146-754">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-754">OPOS</span></span>      |          |

### <a name="dedicated-iis-hardware-station"></a><span data-ttu-id="a2146-755">専用 IIS ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-755">Dedicated IIS hardware station</span></span>

<span data-ttu-id="a2146-756">次の周辺機器は、専用 (共有ではない) IIS ハードウェア ステーションを使用して、Windows 用 Modern POS およびクラウド POS とともにテストされています。</span><span class="sxs-lookup"><span data-stu-id="a2146-756">The following peripherals were tested by using a dedicated (not shared) IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

#### <a name="printer"></a><span data-ttu-id="a2146-757">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-757">Printer</span></span>

| <span data-ttu-id="a2146-758">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-758">Manufacturer</span></span> | <span data-ttu-id="a2146-759">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-759">Model</span></span>    | <span data-ttu-id="a2146-760">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-760">Interface</span></span> | <span data-ttu-id="a2146-761">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-761">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="a2146-762">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-762">Epson</span></span>        | <span data-ttu-id="a2146-763">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="a2146-763">Tm-T88IV</span></span> | <span data-ttu-id="a2146-764">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-764">OPOS</span></span>      |                           |
| <span data-ttu-id="a2146-765">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-765">Epson</span></span>        | <span data-ttu-id="a2146-766">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="a2146-766">TM-T88V</span></span>  | <span data-ttu-id="a2146-767">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-767">OPOS</span></span>      |                           |
| <span data-ttu-id="a2146-768">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-768">Star</span></span>         | <span data-ttu-id="a2146-769">TSP650II</span><span class="sxs-lookup"><span data-stu-id="a2146-769">TSP650II</span></span> | <span data-ttu-id="a2146-770">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-770">OPOS</span></span>      |                           |
| <span data-ttu-id="a2146-771">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-771">Star</span></span>         | <span data-ttu-id="a2146-772">TSP650II</span><span class="sxs-lookup"><span data-stu-id="a2146-772">TSP650II</span></span> | <span data-ttu-id="a2146-773">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-773">Custom</span></span>    | <span data-ttu-id="a2146-774">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-774">Connected via network</span></span>     |
| <span data-ttu-id="a2146-775">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-775">HP</span></span>           | <span data-ttu-id="a2146-776">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="a2146-776">F7M67AA</span></span>  | <span data-ttu-id="a2146-777">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-777">OPOS</span></span>      | <span data-ttu-id="a2146-778">Powered USB</span><span class="sxs-lookup"><span data-stu-id="a2146-778">Powered USB</span></span>               |

#### <a name="bar-code-scanner"></a><span data-ttu-id="a2146-779">バーコード スキャナー</span><span class="sxs-lookup"><span data-stu-id="a2146-779">Bar code scanner</span></span>

| <span data-ttu-id="a2146-780">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-780">Manufacturer</span></span>  | <span data-ttu-id="a2146-781">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-781">Model</span></span>   | <span data-ttu-id="a2146-782">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-782">Interface</span></span> | <span data-ttu-id="a2146-783">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-783">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="a2146-784">Motorola</span><span class="sxs-lookup"><span data-stu-id="a2146-784">Motorola</span></span>      | <span data-ttu-id="a2146-785">DS9208</span><span class="sxs-lookup"><span data-stu-id="a2146-785">DS9208</span></span>  | <span data-ttu-id="a2146-786">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-786">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-787">記号</span><span class="sxs-lookup"><span data-stu-id="a2146-787">Symbol</span></span>        | <span data-ttu-id="a2146-788">LS2208</span><span class="sxs-lookup"><span data-stu-id="a2146-788">LS2208</span></span>  | <span data-ttu-id="a2146-789">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-789">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-790">HP 統合済</span><span class="sxs-lookup"><span data-stu-id="a2146-790">HP Integrated</span></span> | <span data-ttu-id="a2146-791">E1L07AA</span><span class="sxs-lookup"><span data-stu-id="a2146-791">E1L07AA</span></span> | <span data-ttu-id="a2146-792">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-792">OPOS</span></span>      |          |

#### <a name="pin-pad"></a><span data-ttu-id="a2146-793">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="a2146-793">PIN pad</span></span>

| <span data-ttu-id="a2146-794">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-794">Manufacturer</span></span> | <span data-ttu-id="a2146-795">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-795">Model</span></span>  | <span data-ttu-id="a2146-796">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-796">Interface</span></span> | <span data-ttu-id="a2146-797">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-797">Comments</span></span>                                        |
|--------------|--------|-----------|-------------------------------------------------|
| <span data-ttu-id="a2146-798">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-798">VeriFone</span></span>     | <span data-ttu-id="a2146-799">1000SE</span><span class="sxs-lookup"><span data-stu-id="a2146-799">1000SE</span></span> | <span data-ttu-id="a2146-800">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-800">OPOS</span></span>      | <span data-ttu-id="a2146-801">支払コネクターのカスタマイズが必要</span><span class="sxs-lookup"><span data-stu-id="a2146-801">Requires customization of the payment connector</span></span> |

#### <a name="payment-terminal"></a><span data-ttu-id="a2146-802">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-802">Payment terminal</span></span>

| <span data-ttu-id="a2146-803">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-803">Manufacturer</span></span> | <span data-ttu-id="a2146-804">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-804">Model</span></span> | <span data-ttu-id="a2146-805">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-805">Interface</span></span> | <span data-ttu-id="a2146-806">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-806">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a2146-807">Equinox</span><span class="sxs-lookup"><span data-stu-id="a2146-807">Equinox</span></span>      | <span data-ttu-id="a2146-808">L5300</span><span class="sxs-lookup"><span data-stu-id="a2146-808">L5300</span></span> | <span data-ttu-id="a2146-809">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-809">Custom</span></span>    | <span data-ttu-id="a2146-810">支払コネクターのカスタマイズが必要</span><span class="sxs-lookup"><span data-stu-id="a2146-810">Requires customization of the payment connector</span></span>                                |
| <span data-ttu-id="a2146-811">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-811">VeriFone</span></span>     | <span data-ttu-id="a2146-812">MX925</span><span class="sxs-lookup"><span data-stu-id="a2146-812">MX925</span></span> | <span data-ttu-id="a2146-813">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-813">Custom</span></span>    | <span data-ttu-id="a2146-814">支払コネクターのカスタマイズが必要。ネットワークおよびUSB接続</span><span class="sxs-lookup"><span data-stu-id="a2146-814">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="a2146-815">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-815">VeriFone</span></span>     | <span data-ttu-id="a2146-816">MX915</span><span class="sxs-lookup"><span data-stu-id="a2146-816">MX915</span></span> | <span data-ttu-id="a2146-817">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-817">Custom</span></span>    | <span data-ttu-id="a2146-818">支払コネクターのカスタマイズが必要。ネットワークおよびUSB接続</span><span class="sxs-lookup"><span data-stu-id="a2146-818">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="a2146-819">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-819">Cash drawer</span></span>

| <span data-ttu-id="a2146-820">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-820">Manufacturer</span></span> | <span data-ttu-id="a2146-821">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-821">Model</span></span>     | <span data-ttu-id="a2146-822">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-822">Interface</span></span> | <span data-ttu-id="a2146-823">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-823">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="a2146-824">APG</span><span class="sxs-lookup"><span data-stu-id="a2146-824">APG</span></span>          | <span data-ttu-id="a2146-825">Atwood</span><span class="sxs-lookup"><span data-stu-id="a2146-825">Atwood</span></span>    | <span data-ttu-id="a2146-826">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-826">Custom</span></span>    | <span data-ttu-id="a2146-827">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-827">Connected via network</span></span> |
| <span data-ttu-id="a2146-828">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-828">Star</span></span>         | <span data-ttu-id="a2146-829">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="a2146-829">SMD2-1317</span></span> | <span data-ttu-id="a2146-830">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-830">OPOS</span></span>      |                       |
| <span data-ttu-id="a2146-831">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-831">HP</span></span>           | <span data-ttu-id="a2146-832">QT457AA</span><span class="sxs-lookup"><span data-stu-id="a2146-832">QT457AA</span></span>   | <span data-ttu-id="a2146-833">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-833">OPOS</span></span>      |                       |

#### <a name="line-display"></a><span data-ttu-id="a2146-834">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="a2146-834">Line display</span></span>

| <span data-ttu-id="a2146-835">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-835">Manufacturer</span></span>  | <span data-ttu-id="a2146-836">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-836">Model</span></span>   | <span data-ttu-id="a2146-837">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-837">Interface</span></span> | <span data-ttu-id="a2146-838">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-838">Comments</span></span> |
|---------------|---------|-----------|----------|
| <span data-ttu-id="a2146-839">HP 統合済</span><span class="sxs-lookup"><span data-stu-id="a2146-839">HP integrated</span></span> | <span data-ttu-id="a2146-840">G6U79AA</span><span class="sxs-lookup"><span data-stu-id="a2146-840">G6U79AA</span></span> | <span data-ttu-id="a2146-841">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-841">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-842">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-842">Epson</span></span>         | <span data-ttu-id="a2146-843">M58DC</span><span class="sxs-lookup"><span data-stu-id="a2146-843">M58DC</span></span>   | <span data-ttu-id="a2146-844">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-844">OPOS</span></span>      |          |

#### <a name="signature-capture"></a><span data-ttu-id="a2146-845">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="a2146-845">Signature capture</span></span>

| <span data-ttu-id="a2146-846">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-846">Manufacturer</span></span> | <span data-ttu-id="a2146-847">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-847">Model</span></span>  | <span data-ttu-id="a2146-848">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-848">Interface</span></span> | <span data-ttu-id="a2146-849">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-849">Comments</span></span> |
|--------------|--------|-----------|----------|
| <span data-ttu-id="a2146-850">Scriptel</span><span class="sxs-lookup"><span data-stu-id="a2146-850">Scriptel</span></span>     | <span data-ttu-id="a2146-851">ST1550</span><span class="sxs-lookup"><span data-stu-id="a2146-851">ST1550</span></span> | <span data-ttu-id="a2146-852">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-852">OPOS</span></span>      |          |

#### <a name="scale"></a><span data-ttu-id="a2146-853">スケール</span><span class="sxs-lookup"><span data-stu-id="a2146-853">Scale</span></span>

| <span data-ttu-id="a2146-854">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-854">Manufacturer</span></span> | <span data-ttu-id="a2146-855">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-855">Model</span></span>         | <span data-ttu-id="a2146-856">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-856">Interface</span></span> | <span data-ttu-id="a2146-857">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-857">Comments</span></span> |
|--------------|---------------|-----------|----------|
| <span data-ttu-id="a2146-858">Datalogic</span><span class="sxs-lookup"><span data-stu-id="a2146-858">Datalogic</span></span>    | <span data-ttu-id="a2146-859">Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="a2146-859">Magellan 8400</span></span> | <span data-ttu-id="a2146-860">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-860">OPOS</span></span>      |          |

#### <a name="msr"></a><span data-ttu-id="a2146-861">MSR</span><span class="sxs-lookup"><span data-stu-id="a2146-861">MSR</span></span>

| <span data-ttu-id="a2146-862">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-862">Manufacturer</span></span> | <span data-ttu-id="a2146-863">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-863">Model</span></span>       | <span data-ttu-id="a2146-864">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-864">Interface</span></span> | <span data-ttu-id="a2146-865">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-865">Comments</span></span> |
|--------------|-------------|-----------|----------|
| <span data-ttu-id="a2146-866">Magtek</span><span class="sxs-lookup"><span data-stu-id="a2146-866">Magtek</span></span>       | <span data-ttu-id="a2146-867">21073075</span><span class="sxs-lookup"><span data-stu-id="a2146-867">21073075</span></span>    | <span data-ttu-id="a2146-868">UWP</span><span class="sxs-lookup"><span data-stu-id="a2146-868">UWP</span></span>       |          |
| <span data-ttu-id="a2146-869">Magtek</span><span class="sxs-lookup"><span data-stu-id="a2146-869">Magtek</span></span>       | <span data-ttu-id="a2146-870">21073062</span><span class="sxs-lookup"><span data-stu-id="a2146-870">21073062</span></span>    | <span data-ttu-id="a2146-871">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-871">OPOS</span></span>      |          |
| <span data-ttu-id="a2146-872">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-872">HP</span></span>           | <span data-ttu-id="a2146-873">IDRA-334133</span><span class="sxs-lookup"><span data-stu-id="a2146-873">IDRA-334133</span></span> | <span data-ttu-id="a2146-874">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-874">OPOS</span></span>      |          |

### <a name="shared-iis-hardware-station"></a><span data-ttu-id="a2146-875">共有 IIS ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="a2146-875">Shared IIS hardware station</span></span>

<span data-ttu-id="a2146-876">次の周辺機器は、共有 IIS ハードウェア ステーションを使用して、Windows 用 Modern POS およびクラウド POS とともにテストされています。</span><span class="sxs-lookup"><span data-stu-id="a2146-876">The following peripherals were tested by using a shared IIS hardware station together with Modern POS for Windows and Cloud POS.</span></span>

> [!NOTE]
> <span data-ttu-id="a2146-877">プリンター、支払ターミナル、キャッシュ ドロワーのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="a2146-877">Only a printer, payment terminal, and cash drawer are supported.</span></span>

#### <a name="printer"></a><span data-ttu-id="a2146-878">プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-878">Printer</span></span>

| <span data-ttu-id="a2146-879">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-879">Manufacturer</span></span> | <span data-ttu-id="a2146-880">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-880">Model</span></span>    | <span data-ttu-id="a2146-881">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-881">Interface</span></span> | <span data-ttu-id="a2146-882">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-882">Comments</span></span>                  |
|--------------|----------|-----------|---------------------------|
| <span data-ttu-id="a2146-883">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-883">Epson</span></span>        | <span data-ttu-id="a2146-884">Tm-T88IV</span><span class="sxs-lookup"><span data-stu-id="a2146-884">Tm-T88IV</span></span> | <span data-ttu-id="a2146-885">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-885">OPOS</span></span>      |                           |
| <span data-ttu-id="a2146-886">Epson</span><span class="sxs-lookup"><span data-stu-id="a2146-886">Epson</span></span>        | <span data-ttu-id="a2146-887">TM-T88V</span><span class="sxs-lookup"><span data-stu-id="a2146-887">TM-T88V</span></span>  | <span data-ttu-id="a2146-888">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-888">OPOS</span></span>      |                           |
| <span data-ttu-id="a2146-889">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-889">Star</span></span>         | <span data-ttu-id="a2146-890">TSP650II</span><span class="sxs-lookup"><span data-stu-id="a2146-890">TSP650II</span></span> | <span data-ttu-id="a2146-891">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-891">OPOS</span></span>      |                           |
| <span data-ttu-id="a2146-892">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-892">Star</span></span>         | <span data-ttu-id="a2146-893">TSP650II</span><span class="sxs-lookup"><span data-stu-id="a2146-893">TSP650II</span></span> | <span data-ttu-id="a2146-894">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-894">Custom</span></span>    | <span data-ttu-id="a2146-895">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-895">Connected via network</span></span>     |
| <span data-ttu-id="a2146-896">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-896">HP</span></span>           | <span data-ttu-id="a2146-897">F7M67AA</span><span class="sxs-lookup"><span data-stu-id="a2146-897">F7M67AA</span></span>  | <span data-ttu-id="a2146-898">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-898">OPOS</span></span>      | <span data-ttu-id="a2146-899">Powered USB</span><span class="sxs-lookup"><span data-stu-id="a2146-899">Powered USB</span></span>               |

#### <a name="payment-terminal"></a><span data-ttu-id="a2146-900">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-900">Payment terminal</span></span>

| <span data-ttu-id="a2146-901">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-901">Manufacturer</span></span> | <span data-ttu-id="a2146-902">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-902">Model</span></span> | <span data-ttu-id="a2146-903">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-903">Interface</span></span> | <span data-ttu-id="a2146-904">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-904">Comments</span></span>                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a2146-905">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-905">VeriFone</span></span>     | <span data-ttu-id="a2146-906">MX925</span><span class="sxs-lookup"><span data-stu-id="a2146-906">MX925</span></span> | <span data-ttu-id="a2146-907">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-907">Custom</span></span>    | <span data-ttu-id="a2146-908">支払コネクターのカスタマイズが必要。ネットワークおよびUSB接続</span><span class="sxs-lookup"><span data-stu-id="a2146-908">Requires customization of the payment connector; connected via network and USB</span></span> |
| <span data-ttu-id="a2146-909">VeriFone</span><span class="sxs-lookup"><span data-stu-id="a2146-909">VeriFone</span></span>     | <span data-ttu-id="a2146-910">MX915</span><span class="sxs-lookup"><span data-stu-id="a2146-910">MX915</span></span> | <span data-ttu-id="a2146-911">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-911">Custom</span></span>    | <span data-ttu-id="a2146-912">支払コネクターのカスタマイズが必要。ネットワークおよびUSB接続</span><span class="sxs-lookup"><span data-stu-id="a2146-912">Requires customization of the payment connector; connected via network and USB</span></span> |

#### <a name="cash-drawer"></a><span data-ttu-id="a2146-913">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-913">Cash drawer</span></span>

| <span data-ttu-id="a2146-914">メーカー</span><span class="sxs-lookup"><span data-stu-id="a2146-914">Manufacturer</span></span> | <span data-ttu-id="a2146-915">モデル</span><span class="sxs-lookup"><span data-stu-id="a2146-915">Model</span></span>     | <span data-ttu-id="a2146-916">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="a2146-916">Interface</span></span> | <span data-ttu-id="a2146-917">コメント</span><span class="sxs-lookup"><span data-stu-id="a2146-917">Comments</span></span>              |
|--------------|-----------|-----------|-----------------------|
| <span data-ttu-id="a2146-918">APG</span><span class="sxs-lookup"><span data-stu-id="a2146-918">APG</span></span>          | <span data-ttu-id="a2146-919">Atwood</span><span class="sxs-lookup"><span data-stu-id="a2146-919">Atwood</span></span>    | <span data-ttu-id="a2146-920">ユーザー設定</span><span class="sxs-lookup"><span data-stu-id="a2146-920">Custom</span></span>    | <span data-ttu-id="a2146-921">ネットワーク経由で接続</span><span class="sxs-lookup"><span data-stu-id="a2146-921">Connected via network</span></span> |
| <span data-ttu-id="a2146-922">Star</span><span class="sxs-lookup"><span data-stu-id="a2146-922">Star</span></span>         | <span data-ttu-id="a2146-923">SMD2-1317</span><span class="sxs-lookup"><span data-stu-id="a2146-923">SMD2-1317</span></span> | <span data-ttu-id="a2146-924">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-924">OPOS</span></span>      |                       |
| <span data-ttu-id="a2146-925">HP</span><span class="sxs-lookup"><span data-stu-id="a2146-925">HP</span></span>           | <span data-ttu-id="a2146-926">QT457AA</span><span class="sxs-lookup"><span data-stu-id="a2146-926">QT457AA</span></span>   | <span data-ttu-id="a2146-927">OPOS</span><span class="sxs-lookup"><span data-stu-id="a2146-927">OPOS</span></span>      |                       |

## <a name="troubleshooting"></a><span data-ttu-id="a2146-928">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a2146-928">Troubleshooting</span></span>

### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a><span data-ttu-id="a2146-929">Modern POS は、選択リストにあるハードウェア ステーションを検出できますが、ペアリングを完了することはできません</span><span class="sxs-lookup"><span data-stu-id="a2146-929">Modern POS can detect the hardware station in its list for selection, but it can't complete the pairing</span></span>

<span data-ttu-id="a2146-930">**ソリューション:** 以下の潜在的障害ポイントを確認してください:</span><span class="sxs-lookup"><span data-stu-id="a2146-930">**Solution:** Verify the following list of potential failure points:</span></span>

- <span data-ttu-id="a2146-931">Modern POS を実行しているコンピュータは、ハードウェア ステーションを実行しているコンピュータで使用される証明書を信頼します。</span><span class="sxs-lookup"><span data-stu-id="a2146-931">The computer that is running Modern POS trusts the certificate that is used on the computer that runs the hardware station.</span></span>

    - <span data-ttu-id="a2146-932">Web ブラウザーでこの設定を確認するには、次のURL `https://<Computer Name>:<Port Number>/HardwareStation/ping` に移動します。</span><span class="sxs-lookup"><span data-stu-id="a2146-932">To verify this setup, in a web browser, go to the following URL: `https://<Computer Name>:<Port Number>/HardwareStation/ping`.</span></span>
    - <span data-ttu-id="a2146-933">この URL は ping を使用してコンピュータにアクセスできるかどうかを確認し、ブラウザは証明書が信頼できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a2146-933">This URL uses a ping to verify that the computer can be accessed, and the browser indicates whether the certificate is trusted.</span></span> <span data-ttu-id="a2146-934">(たとえば、Internet Explorer ではカギのアイコンがアドレス バーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a2146-934">(For example, in Internet Explorer, a lock icon appears in the address bar.</span></span> <span data-ttu-id="a2146-935">このアイコンをクリックすると、Internet Explorer は証明書が現在信頼されているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2146-935">When you click this icon, Internet Explorer verifies whether the certificate is currently trusted.</span></span> <span data-ttu-id="a2146-936">表示される証明書の詳細を見ることで、ローカル コンピュータに証明書をインストールできます)。</span><span class="sxs-lookup"><span data-stu-id="a2146-936">You can install the certificate on the local computer by viewing the details of the certificate that is shown.)</span></span>

- <span data-ttu-id="a2146-937">ハードウェア ステーションを実行するコンピュータで、ハードウェア ステーションで使用されるポートはファイアウォールで開かれます。</span><span class="sxs-lookup"><span data-stu-id="a2146-937">On the computer that runs the hardware station, the port that will be used by the hardware station is opened in the firewall.</span></span>
- <span data-ttu-id="a2146-938">ハードウェア ステーションのインストールの最後に実行される支払商社情報インストール ツールを使用して、ハードウェア ステーションに支払商社情報が正しくインストールされます。</span><span class="sxs-lookup"><span data-stu-id="a2146-938">The hardware station has correctly installed merchant account information through the Install merchant information tool that runs at the end of the hardware station installer.</span></span>

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a><span data-ttu-id="a2146-939">Modern POS が選択リストにあるハードウェア ステーションを検出できない</span><span class="sxs-lookup"><span data-stu-id="a2146-939">Modern POS can't detect the hardware station in its list for selection</span></span>

<span data-ttu-id="a2146-940">**ソリューション:** 次の要素のいずれかによりこの問題が生じることがあります:</span><span class="sxs-lookup"><span data-stu-id="a2146-940">**Solution:** Either of the following factors can cause this issue:</span></span>

- <span data-ttu-id="a2146-941">ハードウェア ステーションが本社に正しく設定されていない。</span><span class="sxs-lookup"><span data-stu-id="a2146-941">The hardware station hasn't been set up correctly in headquarters.</span></span> <span data-ttu-id="a2146-942">このトピックで説明した手順を使用して、ハードウェア ステーションのプロファイルとハードウェア ステーションが正しく入力されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2146-942">Use the steps earlier in this topic to verify that the hardware station profile and the hardware station are correctly entered.</span></span>
- <span data-ttu-id="a2146-943">チャンネル構成を更新するジョブが実行されていません。</span><span class="sxs-lookup"><span data-stu-id="a2146-943">The jobs haven't been run to update the channel configuration.</span></span> <span data-ttu-id="a2146-944">この場合、チャンネル構成用に 1070 のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="a2146-944">In this case, run the 1070 job for channel configuration.</span></span>

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a><span data-ttu-id="a2146-945">Modern POS が新しいキャッシュ ドロワーの設定を反映していない</span><span class="sxs-lookup"><span data-stu-id="a2146-945">Modern POS doesn't reflect new cash drawer settings</span></span>

<span data-ttu-id="a2146-946">**ソリューション:** 現在のバッチを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a2146-946">**Solution:** Close the current batch.</span></span> <span data-ttu-id="a2146-947">キャッシュ ドロワーへの変更は、現在のバッチが閉じられるまで Modern POS では更新されません。</span><span class="sxs-lookup"><span data-stu-id="a2146-947">Changes to the cash drawer aren't updated to Modern POS until the current batch is closed.</span></span>

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a><span data-ttu-id="a2146-948">Modern POS が周辺機器の問題を報告している</span><span class="sxs-lookup"><span data-stu-id="a2146-948">Modern POS is reporting an issue with a retail peripheral</span></span>

<span data-ttu-id="a2146-949">**ソリューション:** この問題の一般的な原因を挙げます。</span><span class="sxs-lookup"><span data-stu-id="a2146-949">**Solution:** Here are some typical causes of this issue:</span></span>

- <span data-ttu-id="a2146-950">他のデバイス ドライバの Configuration Utility が終了していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a2146-950">Make sure that other device driver configuration utilities are closed.</span></span> <span data-ttu-id="a2146-951">これらのユーティリティが開かれている場合、Modern POS またはハードウェア ステーションのデバイス要求を邪魔することがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-951">If these utilities are open, they might prevent Modern POS or the hardware station from claiming the device.</span></span>
- <span data-ttu-id="a2146-952">小売周辺機器が複数の POS のデバイスで共有されている場合、次のカテゴリの 1 つに属していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-952">If the retail peripheral is shared with multiple POS devices, make sure that it belongs to one of the following categories:</span></span>

    - <span data-ttu-id="a2146-953">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="a2146-953">Cash drawer</span></span>
    - <span data-ttu-id="a2146-954">レシート プリンター</span><span class="sxs-lookup"><span data-stu-id="a2146-954">Receipt printer</span></span>
    - <span data-ttu-id="a2146-955">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="a2146-955">Payment terminal</span></span>

    <span data-ttu-id="a2146-956">周辺機器がこれらのカテゴリのいずれかに属していない場合、ハードウェア ステーションは周辺機器を複数の POS デバイスで共有するようにはデザインされていません。</span><span class="sxs-lookup"><span data-stu-id="a2146-956">If the peripheral doesn't belong to one of these categories, the hardware station isn't designed to enable the peripheral to be shared among multiple POS devices.</span></span>

- <span data-ttu-id="a2146-957">場合によっては、デバイス ドライバによってコモン コントロール オブジェクト (CCO) が正しく動作できなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-957">Sometimes, device drivers can cause the common control objects (CCOs) to stop working correctly.</span></span> <span data-ttu-id="a2146-958">新たにインストールされたデバイスが正しく作動していない場合、またはそのほかの問題に気づく場合、通常は CCO を再インストールすることで問題を解決できます。</span><span class="sxs-lookup"><span data-stu-id="a2146-958">If a device has recently been installed, but it isn't working properly or you notice other issues, you can often resolve the issue by reinstalling the CCOs.</span></span> <span data-ttu-id="a2146-959">CCO をダウンロードするには、<http://monroecs.com/oposccos_current.htm> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2146-959">To download the CCOs, visit <http://monroecs.com/oposccos_current.htm>.</span></span>
- <span data-ttu-id="a2146-960">テストまたはトラブルシューティングのために頻繁に周辺機器を変更する場合、キャッシュが自然に更新されるのを待つ代わりに IIS をリセットする必要があるかもしれません。</span><span class="sxs-lookup"><span data-stu-id="a2146-960">If you make frequent peripheral changes during testing or troubleshooting, you might have to reset IIS instead of waiting for the cache to refresh itself.</span></span> <span data-ttu-id="a2146-961">IIS のリセットには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a2146-961">To reset IIS, follow these steps:</span></span>

    1. <span data-ttu-id="a2146-962">**開始** メニューから **CMD** とタイプします。</span><span class="sxs-lookup"><span data-stu-id="a2146-962">From the **Start** menu, type **CMD**.</span></span>
    2. <span data-ttu-id="a2146-963">検索結果で、右クリックで **コマンド プロンプト**、次いで **管理者として実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-963">In the search results, right-click **Command prompt**, and then click **Run as administrator**.</span></span>
    3. <span data-ttu-id="a2146-964">**コマンド プロンプト**ウィンドウで、**iisreset /Restart** とタイプして Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="a2146-964">In the **Command prompt** window, type **iisreset /Restart** and then press Enter.</span></span>
    4. <span data-ttu-id="a2146-965">IIS の再起動後、Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="a2146-965">After IIS has restarted, restart Modern POS.</span></span>

- <span data-ttu-id="a2146-966">周辺機器に頻繁に変更を加え、POS クライアントを頻繁に起動および終了した場合、前の POS セッションの dllhost プロセスが現在のセッションに干渉することがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-966">While you're making frequent changes to peripheral devices, if you also frequently start and exit the POS client, the dllhost process from a previous POS session can interfere with the current session.</span></span> <span data-ttu-id="a2146-967">この場合、前のセッションを管理するダイナミックリンク ライブラリ (DLL) のホストを閉じるまで、デバイスが使用可能にならないことがあります。</span><span class="sxs-lookup"><span data-stu-id="a2146-967">In this case, a device might not be usable until you close the dynamic-link library (DLL) host that is managing the previous session.</span></span> <span data-ttu-id="a2146-968">DLL ホストを終了するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a2146-968">To close the DLL host, follow these steps:</span></span>

    1. <span data-ttu-id="a2146-969">**開始** メニューから **タスク マネージャ** とタイプします。</span><span class="sxs-lookup"><span data-stu-id="a2146-969">From the **Start** menu, type **Task manager**.</span></span>
    2. <span data-ttu-id="a2146-970">検索結果から、**タスク マネージャ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-970">In the search results, click **Task manager**.</span></span>
    3. <span data-ttu-id="a2146-971">タスク マネージャの **詳細** タブで **名前** というラベルの付いた列ヘッダーをクリックし、テーブルを名前のアルファベット順に並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="a2146-971">In Task manager, on the **Details** tab, click the column header that is labeled **Name** to sort the table alphabetically by name.</span></span>
    4. <span data-ttu-id="a2146-972">dllhost.exe が見つかるまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="a2146-972">Scroll down until you find dllhost.exe.</span></span>
    5. <span data-ttu-id="a2146-973">各 DLL ホストを選択し、**タスクの終了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a2146-973">Select each DLL host, and then click **End task**.</span></span>
    6. <span data-ttu-id="a2146-974">DLL ホストが終了したら、Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="a2146-974">After the DLL hosts have been closed, restart Modern POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2146-975">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="a2146-975">Additional resources</span></span>

[<span data-ttu-id="a2146-976">小売の周辺機器シミュレーター</span><span class="sxs-lookup"><span data-stu-id="a2146-976">Retail peripheral simulator</span></span>](dev-itpro/retail-peripheral-simulator.md)

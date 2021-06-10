---
title: ネットワーク周辺機器のサポート
description: このトピックでは、店舗でサポートされているネットワーク周辺機器の概要について説明します。
author: rubendel
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: ac533bef9c7d075b690250eaec6f8c35ee914f5c
ms.sourcegitcommit: d84329f903d359ae042e8c0a4594982a7e06756f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/06/2021
ms.locfileid: "5984262"
---
# <a name="support-for-network-peripherals"></a><span data-ttu-id="8024f-103">ネットワーク周辺機器のサポート</span><span class="sxs-lookup"><span data-stu-id="8024f-103">Support for network peripherals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8024f-104">このトピックでは、店舗におけるネットワーク周辺機器のサポートおよび設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="8024f-104">This topic describes the support for and setup of network peripherals in the store.</span></span>

## <a name="key-terms"></a><span data-ttu-id="8024f-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="8024f-105">Key terms</span></span>

| <span data-ttu-id="8024f-106">期間</span><span class="sxs-lookup"><span data-stu-id="8024f-106">Term</span></span> | <span data-ttu-id="8024f-107">説明</span><span class="sxs-lookup"><span data-stu-id="8024f-107">Description</span></span> |
|---|---|
| <span data-ttu-id="8024f-108">登録</span><span class="sxs-lookup"><span data-stu-id="8024f-108">Register</span></span> | <span data-ttu-id="8024f-109">販売時点管理 (POS) レジスターのインスタンスを構成するために使用されるエンティティ。</span><span class="sxs-lookup"><span data-stu-id="8024f-109">The entity that is used to configure an instance of a point of sale (POS) register.</span></span> |
| <span data-ttu-id="8024f-110">デバイス</span><span class="sxs-lookup"><span data-stu-id="8024f-110">Device</span></span> | <span data-ttu-id="8024f-111">POS レジスタの物理的なインスタンスとそれに割り当てられた最新の POS アプリケーションの表現。</span><span class="sxs-lookup"><span data-stu-id="8024f-111">A representation of the physical instance of a POS register and the Modern POS application that is assigned to it.</span></span> |
| <span data-ttu-id="8024f-112">専用ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="8024f-112">Dedicated hardware station</span></span> | <span data-ttu-id="8024f-113">Windows 用 Modern POS および Android アプリケーション用 Modern POS に組み込まれているプロセス間通信 (IPC) ハードウェア ステーション。</span><span class="sxs-lookup"><span data-stu-id="8024f-113">The hardware station business logic that is built into the Modern POS for Windows and Modern POS for Android applications.</span></span> |
| <span data-ttu-id="8024f-114">ドロワーのキック (d/k) ポート</span><span class="sxs-lookup"><span data-stu-id="8024f-114">Drawer kick (d/k) port</span></span> | <span data-ttu-id="8024f-115">キャッシュ ドロワーをレシート プリンターに接続するための従来の方法。</span><span class="sxs-lookup"><span data-stu-id="8024f-115">A traditional method for connecting a cash drawer to a receipt printer.</span></span> |
| <span data-ttu-id="8024f-116">ネットワーク周辺機器</span><span class="sxs-lookup"><span data-stu-id="8024f-116">Network peripherals</span></span> | <span data-ttu-id="8024f-117">ネットワーク対応型の支払ターミナル、レシート プリンター、キャッシュ ドロワーの組み込みサポート。</span><span class="sxs-lookup"><span data-stu-id="8024f-117">Built-in support for network-enabled payment terminals, receipt printers, and cash drawers.</span></span> |
| <span data-ttu-id="8024f-118">ESC/P</span><span class="sxs-lookup"><span data-stu-id="8024f-118">ESC/P</span></span> | <span data-ttu-id="8024f-119">"Escape/P" とも呼ばれるプリンターの Epson 標準コードは、販売時点管理プリンターにコマンドを送信するために一般的に使用されている、Epsonで作成されたプリンター コントロール言語です。</span><span class="sxs-lookup"><span data-stu-id="8024f-119">Epson Standard Code for Printers, aslo know as "Escape/P, is printer a control language created by Epson that is commonly used to send commands to point of sale printers.</span></span> |

## <a name="supported-pos-clients-and-devices"></a><span data-ttu-id="8024f-120">サポートされている POS クライアントとデバイス</span><span class="sxs-lookup"><span data-stu-id="8024f-120">Supported POS clients and devices</span></span>

<span data-ttu-id="8024f-121">ネットワーク周辺機器用の機能は、Windows 用 Modern POS および Android POS クライアント用 Modern POS でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8024f-121">Functionality for network peripherals is supported by the Modern POS for Windows and Modern POS for Android POS clients.</span></span>

<span data-ttu-id="8024f-122">この機能は、ネットワーク対応型の支払ターミナルとレシート プリンターをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="8024f-122">This functionality supports network-enabled payment terminals and receipt printers.</span></span> <span data-ttu-id="8024f-123">キャッシュ ドロワーのサポートを提供するには、d/k ポートを介して、キャッシュ ドロワーをネットワーク対応型のレシート プリンターに接続します。</span><span class="sxs-lookup"><span data-stu-id="8024f-123">You can provide cash drawer support by connecting the cash drawer to the network-enabled receipt printer via the d/k port.</span></span>

<span data-ttu-id="8024f-124">この機能に対するすぐに使える、[Adyen 向け Microsoft Dynamics 365 Payment Connector](./adyen-connector.md?tabs=8-1-3) によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="8024f-124">Out-of-box support for this functionality is provided by the [Microsoft Dynamics 365 Payment Connector for Adyen](./adyen-connector.md?tabs=8-1-3).</span></span> <span data-ttu-id="8024f-125">ただし、その他の支払コネクタは、コマース ソフトウェア開発キット (SDK) を介してサポートされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8024f-125">However, other payment connectors might be supported via the Commerce software development kit (SDK).</span></span> <span data-ttu-id="8024f-126">サポートされているレシート プリンターには、Star Micronics と Epson のネットワーク対応型レシート プリンターがあります。</span><span class="sxs-lookup"><span data-stu-id="8024f-126">Supported receipt printers include network-enabled receipt printers from Star Micronics and Epson.</span></span>

<span data-ttu-id="8024f-127">すぐに使えるサポートは、Epson および Star Micronics レシート プリンターのネットワーク プロトコルに対して提供されます。</span><span class="sxs-lookup"><span data-stu-id="8024f-127">Out-of-box support is provided for network protocols for Epson and Star Micronics receipt printers.</span></span> <span data-ttu-id="8024f-128">d/k ポートを介してこれらのプリンターに接続されたキャッシュ ドロワーは、ESC/P プロトコルを介してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="8024f-128">Cash drawers that are connected to those printers via the d/k port are supported via ESC/P protocols.</span></span>

## <a name="set-up-network-peripherals"></a><span data-ttu-id="8024f-129">ネットワーク周辺機器のセットアップ</span><span class="sxs-lookup"><span data-stu-id="8024f-129">Set up network peripherals</span></span>

### <a name="adyen-payment-terminal"></a><span data-ttu-id="8024f-130">Adyen 支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="8024f-130">Adyen payment terminal</span></span>

<span data-ttu-id="8024f-131">Adyen 支払ターミナルの設定方法については、[Adyen の Dynamics 365 支払コネクタ](./adyen-connector.md?tabs=8-1-3#pos-payment-terminal)の「POS 支払ターミナル」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8024f-131">For information about how to set up an Adyen payment terminal, see the "POS payment terminal" section in [Dynamics 365 Payment Connector for Adyen](./adyen-connector.md?tabs=8-1-3#pos-payment-terminal).</span></span>

### <a name="epson-or-star-micronics-receipt-printer-and-a-cash-drawer"></a><span data-ttu-id="8024f-132">Epson または Star Micronics レシート プリンターとキャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="8024f-132">Epson or Star Micronics receipt printer and a cash drawer</span></span>

<span data-ttu-id="8024f-133">Commerce でネットワーク周辺機器をサポートするには、各メーカー固有の通信プロトコルを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8024f-133">For Commerce to support network peripherals, you must implement communication protocols that are unique for each manufacturer.</span></span> <span data-ttu-id="8024f-134">印刷プロトコルが一覧に表示されていない場合、標準ではサポートされておらず、カスタマイズが必要です。</span><span class="sxs-lookup"><span data-stu-id="8024f-134">If a printing protocol isn't listed here, it isn't supported out of box and will require customization.</span></span> 

#### <a name="epson-prerequisite"></a><span data-ttu-id="8024f-135">Epson の前提条件</span><span class="sxs-lookup"><span data-stu-id="8024f-135">Epson prerequisite</span></span>

<span data-ttu-id="8024f-136">プリンターが Epson ePOS 印刷をサポートしている場合は、Epson 社の製品マニュアルを参照して、Epson プリンターの Web サイトにアクセスして ePOS 印刷を有効にする方法について参照してください。</span><span class="sxs-lookup"><span data-stu-id="8024f-136">If your printer supports Epson ePOS-Print, see Epson's product manuals for information about how to access the Epson Printers Configuration Website and enable ePOS-Print.</span></span> <span data-ttu-id="8024f-137">ePOS 印刷が構成されている場合、プリンターは電源サイクル後に、IP アドレスを示す勘定書を印刷します。</span><span class="sxs-lookup"><span data-stu-id="8024f-137">When ePOS-Print is configured, the printer will print a chit that shows its IP address after a power cycle.</span></span>

#### <a name="star-micronics-prerequisite"></a><span data-ttu-id="8024f-138">Star Micronics の前提条件</span><span class="sxs-lookup"><span data-stu-id="8024f-138">Star Micronics prerequisite</span></span>

<span data-ttu-id="8024f-139">イーサネットをサポートするネットワーク対応 Star Micronics プリンターは、Star Micronics プリンター ユーティリティを使用してネットワーク プロトコルを使用するように構成できます。</span><span class="sxs-lookup"><span data-stu-id="8024f-139">Network-enabled Star Micronics printers that support Ethernet can be configured to use network protocols through the Star Micronics Printer Utility.</span></span> <span data-ttu-id="8024f-140">ネットワーク印刷をサポートする Star Micronics デバイスの設定方法については、「Star Micronics」で提供されているドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8024f-140">For information about how to set up Star Micronics devices to support network printing, see the documentation that is provided by Star Micronics.</span></span> <span data-ttu-id="8024f-141">デバイスが正しく構成されている場合は、プリンター ユーティリティのユーザー インターフェイス (UI) を通じて、プリンターの IP アドレスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="8024f-141">When a device is correctly configured, the IP address of the printer can be obtained through the user interface (UI) of the printer utility.</span></span>

#### <a name="set-up-a-hardware-profile"></a><span data-ttu-id="8024f-142">ハードウェア プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="8024f-142">Set up a hardware profile</span></span>

1. <span data-ttu-id="8024f-143">Dynamics 365 Commerce で、**ハードウェア プロファイル** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8024f-143">In Dynamics 365 Commerce, search for **Hardware profiles**.</span></span>
2. <span data-ttu-id="8024f-144">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-144">Select **New**.</span></span>
3. <span data-ttu-id="8024f-145">ハードウェア プロファイル番号を割り当て、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8024f-145">Assign a hardware profile number, and then enter a description.</span></span>
4. <span data-ttu-id="8024f-146">さまざまなデバイス タイプのクイック タブで、次のデバイス タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="8024f-146">On the FastTabs for different device types, set up the following device types.</span></span>

    | <span data-ttu-id="8024f-147">デバイス</span><span class="sxs-lookup"><span data-stu-id="8024f-147">Device</span></span> | <span data-ttu-id="8024f-148">種類</span><span class="sxs-lookup"><span data-stu-id="8024f-148">Type</span></span> | <span data-ttu-id="8024f-149">デバイス名</span><span class="sxs-lookup"><span data-stu-id="8024f-149">Device name</span></span> | <span data-ttu-id="8024f-150">追加の詳細</span><span class="sxs-lookup"><span data-stu-id="8024f-150">Additional details</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="8024f-151">プリンター</span><span class="sxs-lookup"><span data-stu-id="8024f-151">Printer</span></span> | <span data-ttu-id="8024f-152">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8024f-152">Network</span></span> | <span data-ttu-id="8024f-153">**Epson** または **Star**</span><span class="sxs-lookup"><span data-stu-id="8024f-153">**Epson** or **Star**</span></span> | <span data-ttu-id="8024f-154">デバイス名は大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="8024f-154">The device name is case-sensitive.</span></span> <span data-ttu-id="8024f-155">**レシート プロファイル ID** を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8024f-155">Assign a **Receipt profile ID**.</span></span> |
    | <span data-ttu-id="8024f-156">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="8024f-156">Cash drawer</span></span> | <span data-ttu-id="8024f-157">ネットワーク</span><span class="sxs-lookup"><span data-stu-id="8024f-157">Network</span></span> | <span data-ttu-id="8024f-158">**Epson** または **Star**</span><span class="sxs-lookup"><span data-stu-id="8024f-158">**Epson** or **Star**</span></span> | <span data-ttu-id="8024f-159">デバイス名は大文字と小文字が区別されます。</span><span class="sxs-lookup"><span data-stu-id="8024f-159">The device name is case-sensitive.</span></span> <span data-ttu-id="8024f-160">キャッシュ ドロワーが複数の POS デバイスによって共有される場合は、**共有シフトの使用** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8024f-160">Set the **Use shared shift** option to **Yes** if the cash drawer will be shared by multiple POS devices.</span></span> |

5. <span data-ttu-id="8024f-161">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-161">Select **Save**.</span></span>

#### <a name="set-up-modern-pos-for-windows-or-modern-pos-for-android-clients-that-have-built-in-hardware-station-logic"></a><span data-ttu-id="8024f-162">ビルトインのハードウェア ステーション ロジックを持つクライアントに対して、Windows 用 Modern POS または Android クライアント用 Modern POS を設定します。</span><span class="sxs-lookup"><span data-stu-id="8024f-162">Set up Modern POS for Windows or Modern POS for Android clients that have built-in hardware station logic</span></span>

1. <span data-ttu-id="8024f-163">Dynamics 365 Commerce で、**レジスター** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8024f-163">In Dynamics 365 Commerce, search for **Registers**.</span></span>
2. <span data-ttu-id="8024f-164">レジスター番号を選択してレジスターを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-164">Select a register by selecting the register number, and then select **Edit**.</span></span>
3. <span data-ttu-id="8024f-165">作成したハードウェア プロファイルをレジスターに割り当てて、専用の支払ターミナルを使用するようにします。</span><span class="sxs-lookup"><span data-stu-id="8024f-165">Assign the hardware profile that you just created to the register that should use a dedicated payment terminal.</span></span> <span data-ttu-id="8024f-166">このレジスターにマップされているデバイスには、Windows アプリケーション用のモダン POS か Android アプリケーション用のモダン POS のいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8024f-166">The device that is mapped to this register must use either the Modern POS for Windows application or the Modern POS for Android application.</span></span>
4. <span data-ttu-id="8024f-167">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-167">Select **Save**.</span></span>
5. <span data-ttu-id="8024f-168">アクション ウィンドウの **レジスター** タブで、**IP アドレスの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-168">On the Action Pane, on the **Registers** tab, select **Configure IP addresses**.</span></span>
6. <span data-ttu-id="8024f-169">**プリンター** のクイックタブで、プリンターの IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8024f-169">On the **Printer** FastTab, enter the IP address of the printer.</span></span> <span data-ttu-id="8024f-170">ポート番号のフィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="8024f-170">Leave the field for the port number blank.</span></span>
7. <span data-ttu-id="8024f-171">**キャッシュ ドロワー** のクイックタブで、プリンターの IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8024f-171">On the **Cash drawer** FastTab, enter the IP address of the printer.</span></span> <span data-ttu-id="8024f-172">ポート番号のフィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="8024f-172">Leave the field for the port number blank.</span></span>
8. <span data-ttu-id="8024f-173">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-173">Select **Save**.</span></span>
9. <span data-ttu-id="8024f-174">**すべての店舗** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8024f-174">Search for **All stores**.</span></span>
10. <span data-ttu-id="8024f-175">**小売チャンネル ID** 値を選択して店舗を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-175">Select a store by selecting its **Retail Channel Id** value, and then select **Edit**.</span></span>
11. <span data-ttu-id="8024f-176">**ハードウエア ステーション** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-176">On the **Hardware stations** FastTab, select **Add**.</span></span>
12. <span data-ttu-id="8024f-177">**ハードウェア ステーション タイプ** フィールドを **専用** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8024f-177">Set the **Hardware station type** field to **Dedicated**.</span></span>
13. <span data-ttu-id="8024f-178">説明を入力しますが、ハードウェア プロファイルを設定したり、このハードウェア ステーションにその他の値は設定したりしないでください。</span><span class="sxs-lookup"><span data-stu-id="8024f-178">Enter a description, but don't specify a hardware profile or set any other values for this hardware station.</span></span>
14. <span data-ttu-id="8024f-179">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-179">Select **Save**.</span></span>
15. <span data-ttu-id="8024f-180">**配布スケジュール** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8024f-180">Search for **Distribution schedules**.</span></span>
16. <span data-ttu-id="8024f-181">配分スケジュール **1090** を選択して、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-181">Select distribution schedule **1090**, and then select **Run now**.</span></span>
17. <span data-ttu-id="8024f-182">配分スケジュール **1070** を選択して、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-182">Select distribution schedule **1070**, and then select **Run now**.</span></span>

<span data-ttu-id="8024f-183">iOS 用 Modern POS およびクラウド アプリケーション用 Modern POS には、組み込みのハードウェア ステーション ロジックはありません。</span><span class="sxs-lookup"><span data-stu-id="8024f-183">The Modern POS for iOS and Modern POS for Cloud applications don't have built-in hardware station logic.</span></span> <span data-ttu-id="8024f-184">このいずれかのアプリケーションを使用している場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="8024f-184">If you're using either of these applications, follow these steps.</span></span>

1. <span data-ttu-id="8024f-185">Dynamics 365 Commerce で、**すべての店舗** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8024f-185">In Dynamics 365 Commerce, search for **All stores**.</span></span>
2. <span data-ttu-id="8024f-186">**小売チャンネル ID** 値を選択して店舗を選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-186">Select a store by selecting its **Retail Channel Id** value, and then select **Edit**.</span></span>
3. <span data-ttu-id="8024f-187">**ハードウエア ステーション** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-187">On the **Hardware stations** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="8024f-188">**ハードウェア ステーション タイプ** フィールドを **共有** に設定します。</span><span class="sxs-lookup"><span data-stu-id="8024f-188">Set the **Hardware station type** field to **Shared**.</span></span>
5. <span data-ttu-id="8024f-189">説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8024f-189">Enter a description.</span></span> <span data-ttu-id="8024f-190">ハードウェア ステーションは、組み込みのハードウェア ステーション ロジックを持つ POS クライアントを含め、複数の POS クライアントで共有できます。</span><span class="sxs-lookup"><span data-stu-id="8024f-190">This hardware station can be shared by multiple POS clients, including POS clients that have built-in hardware station logic.</span></span>
6. <span data-ttu-id="8024f-191">**ハードウェア プロファイル** フィールドで、ドロップダウン矢印を使用して、ネットワーク周辺機器のハードウェア プロファイルをこのハードウェア ステーションに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="8024f-191">In the **Hardware profile** field, use the drop-down arrow to assign the hardware profile for network peripherals to this hardware station.</span></span>
7. <span data-ttu-id="8024f-192">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-192">Select **Save**.</span></span>
8. <span data-ttu-id="8024f-193">レシート プリンターとキャッシュ ドロワーのハードウェア ステーションが選択されている状態で、**IP アドレスの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-193">While the hardware station for the receipt printer and cash drawer is still selected, select **Configure IP addresses**.</span></span>
9. <span data-ttu-id="8024f-194">プリンターのクイックタブで、プリンターの IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8024f-194">On the printer FastTab, enter the IP address of the printer.</span></span> <span data-ttu-id="8024f-195">ポート番号のフィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="8024f-195">Leave the field for the port number blank.</span></span>
10. <span data-ttu-id="8024f-196">キャッシュ ドロワーのクイックタブで、プリンターの IP アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="8024f-196">On the cash drawer FastTab, enter the IP address of the printer.</span></span> <span data-ttu-id="8024f-197">ポート番号のフィールドを空欄のままにします。</span><span class="sxs-lookup"><span data-stu-id="8024f-197">Leave the field for the port number blank.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8024f-198">共有ハードウェア ステーションを設定する方法の詳細については、[小売りハードウェア ステーションの設定とインストール](../retail-hardware-station-configuration-installation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8024f-198">For detailed information about how to set up shared hardware stations, see [Configure and install Retail hardware station](../retail-hardware-station-configuration-installation.md).</span></span>

11. <span data-ttu-id="8024f-199">**保存** を選択します</span><span class="sxs-lookup"><span data-stu-id="8024f-199">Select **Save**</span></span>
12. <span data-ttu-id="8024f-200">**配布スケジュール** を検索します。</span><span class="sxs-lookup"><span data-stu-id="8024f-200">Search for **Distribution schedules**.</span></span>
13. <span data-ttu-id="8024f-201">配分スケジュール **1090** を選択して、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-201">Select distribution schedule **1090**, and then select **Run now**.</span></span>
14. <span data-ttu-id="8024f-202">配分スケジュール **1070** を選択して、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8024f-202">Select distribution schedule **1070**, and then select **Run now**.</span></span>

### <a name="sharing-network-peripherals"></a><span data-ttu-id="8024f-203">ネットワーク周辺機器の共有</span><span class="sxs-lookup"><span data-stu-id="8024f-203">Sharing network peripherals</span></span>

<span data-ttu-id="8024f-204">ネットワーク レシート プリンターとキャッシュ ドロワーは、複数の POS デバイスで共有できます。</span><span class="sxs-lookup"><span data-stu-id="8024f-204">Network receipt printers and cash drawers can be shared by multiple POS devices.</span></span> <span data-ttu-id="8024f-205">これらを共有するには、共有ハードウェア ステーションを使用して、デバイスへの接続を仲介することができます。</span><span class="sxs-lookup"><span data-stu-id="8024f-205">To share them, you can use a shared hardware station to broker the connection to the devices.</span></span> <span data-ttu-id="8024f-206">または、Windows 用 Modern POS または Android 用 Modern POS を使用している場合は、レジスターのプロパティで同じデバイスを直接コンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="8024f-206">Alternatively, if you're using Modern POS for Windows or Modern POS for Android, you can configure the same devices directly in the register properties.</span></span>

<span data-ttu-id="8024f-207">支払ターミナルは、共有ハードウェア ステーションが支払ターミナルへの接続を仲介するために配置されている場合にのみ共有できます。</span><span class="sxs-lookup"><span data-stu-id="8024f-207">Payment terminals can be shared only if a shared hardware station is deployed to broker the connection to the payment terminal.</span></span> <span data-ttu-id="8024f-208">レジスター レベルで同じ支払ターミナルの IP アドレスを直接設定することによって、支払ターミナルを共有することはできません。</span><span class="sxs-lookup"><span data-stu-id="8024f-208">You can't share a payment terminal by setting the same payment terminal IP address directly at the register level.</span></span> <span data-ttu-id="8024f-209">この方法を使用した場合、個々の POS クライアントがデバイスをロックして要求すると、問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="8024f-209">If you try to use this approach, issues will occur when individual POS clients try to lock and claim the device.</span></span>

## <a name="related-articles"></a><span data-ttu-id="8024f-210">関連記事</span><span class="sxs-lookup"><span data-stu-id="8024f-210">Related articles</span></span>

- [<span data-ttu-id="8024f-211">Android と iOS での POS ハイブリッドアプリの設定</span><span class="sxs-lookup"><span data-stu-id="8024f-211">Set up POS hybrid app on Android and iOS</span></span>](./hybridapp.md)
- [<span data-ttu-id="8024f-212">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="8024f-212">Dynamics 365 Payment Connector for Adyen</span></span>](./adyen-connector.md?tabs=8-1-3)
- [<span data-ttu-id="8024f-213">専用の支払ターミナルおよびプリンターとキャッシュ ドロワーのプロンプト</span><span class="sxs-lookup"><span data-stu-id="8024f-213">Dedicated payment terminals and prompts for a printer and cash drawer</span></span>](../pos-multi-hws.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

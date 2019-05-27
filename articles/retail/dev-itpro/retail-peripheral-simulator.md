---
title: 小売の周辺機器シミュレーター
description: このトピックでは、Dynamics 365 for Retail で提供される周辺機器シミュレーター ツールについて説明します。
author: rubencdelgado
manager: AnnBe
ms.date: 03/22/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailHardwareProfile, RetailTerminalTable, EcoResProductDetailsExtended, RetailCDXSchedule, RetailStoreTable
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Retail
ms.custom: 266544
ms.assetid: 16f31e70-15fc-441e-9727-e6a31c3a48f5
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 890718315c768d9909aceab8bd602cb42328fd75
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537536"
---
# <a name="peripheral-simulator-for-retail"></a><span data-ttu-id="de7c2-103">小売の周辺機器シミュレーター</span><span class="sxs-lookup"><span data-stu-id="de7c2-103">Peripheral simulator for Retail</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de7c2-104">小売の周辺機器シミュレーターは、Microsoft Dynamics 365 for Retail の一部として、またスタンドアロン ユーティリティとして、Microsoft が提供しているユーティリティです。</span><span class="sxs-lookup"><span data-stu-id="de7c2-104">The peripheral simulator for Retail is a utility that Microsoft provides as part of Microsoft Dynamics 365 for Retail and as a standalone utility.</span></span> <span data-ttu-id="de7c2-105">ユーティリティには 2 つの主要コンポーネント、*仮想周辺機器シミュレーター* および *販売時点管理シミュレーター* があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-105">The utility has two primary components, a *virtual peripheral simulator* and a *point of sale (POS) simulator*.</span></span>

<span data-ttu-id="de7c2-106">仮想周辺機器シミュレーターは主に、通常は物理的に POS 周辺機器が必要なシナリオのテストをサポートするために提供されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-106">The virtual peripheral simulator is provided primarily to support testing of scenarios that usually require physical POS peripheral devices.</span></span> <span data-ttu-id="de7c2-107">POS シミュレーターでは、POS クライアントを配置しなくても Retail の物理的な周辺機器との互換性をテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-107">The POS simulator is used to test the compatibility of physical peripheral devices with Retail without having to deploy the POS client.</span></span>

## <a name="install-the-peripheral-simulator-for-retail"></a><span data-ttu-id="de7c2-108">Retail 用周辺機器シミュレーターのインストール</span><span class="sxs-lookup"><span data-stu-id="de7c2-108">Install the peripheral simulator for Retail</span></span>

1. <span data-ttu-id="de7c2-109">**小売** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2. <span data-ttu-id="de7c2-110">**ダウンロード** をクリックし、**PeripheralSimulator** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-110">Click **Download**, and then click **PeripheralSimulator**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-111">周辺機器シミュレーターをダウンロードするには、ポップアップ ブロッカーをオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-111">You must turn off pop-up blockers before you can download the peripheral simulator.</span></span>

3. <span data-ttu-id="de7c2-112">ダウンロードが完了した後、**ダウンロード** フォルダーを開き、**VirtualPeripherals.msi** をダブルクリックすると、インストーラーが開始します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-112">After the download is completed, open the **Downloads** folder, and double-click **VirtualPeripherals.msi** to start the installer.</span></span>
4. <span data-ttu-id="de7c2-113">既定の設定を使用して周辺機器シミュレーターをインストールします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-113">Install the peripheral simulator by using the default settings.</span></span>

<span data-ttu-id="de7c2-114">周辺機器シミュレーターの他に、Monroe Consulting Services からコモン コントロール オブジェクトをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-114">Besides the peripheral simulator, you must install the common control objects from Monroe Consulting Services.</span></span> <span data-ttu-id="de7c2-115">それ以外の方法では、周辺機器シミュレーターは正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-115">Otherwise, the peripheral simulator won't work correctly.</span></span> <span data-ttu-id="de7c2-116">共通のコントロール オブジェクトをダウンロードするには、<http://monroecs.com/oposccos_current.htm> に移動してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-116">To download the common control objects, go to <http://monroecs.com/oposccos_current.htm>.</span></span>

## <a name="virtual-peripheral-simulator"></a><span data-ttu-id="de7c2-117">仮想周辺機器シミュレーター</span><span class="sxs-lookup"><span data-stu-id="de7c2-117">Virtual peripheral simulator</span></span>

<span data-ttu-id="de7c2-118">仮想周辺機器シミュレーターは、小売環境で使用される周辺機器の設定、テスト、トラブルシューティングに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-118">The virtual peripheral simulator helps you set up, test, and troubleshoot peripheral devices that are used in retail environments.</span></span> <span data-ttu-id="de7c2-119">Retail 周辺機器のテストを簡素化したり、正しくない設定または障害が発生しているデバイス ドライバーによって生じた問題を分離するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-119">It can be used to streamline the testing of retail peripherals, and to isolate issues that are caused by incorrect setup or malfunctioning device drivers.</span></span> <span data-ttu-id="de7c2-120">周辺機器シミュレータには、Retail がサポートするデバイスの仮想バージョンを搭載したデスクトップ プログラムが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-120">The peripheral simulator includes a desktop program that features virtual versions of devices that Retail supports.</span></span> <span data-ttu-id="de7c2-121">各仮想デバイスのセクションには、デバイスと Retail POS 間のインタラクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-121">A section for each virtual device shows the interaction between the device and the retail POS.</span></span> <span data-ttu-id="de7c2-122">また、さまざまな POS シナリオに有効な入力を提供するために使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-122">You can also use it to provide input that is valid for various POS scenarios.</span></span> <span data-ttu-id="de7c2-123">周辺シミュレーターは、POS と次の仮想デバイス間の相互作用をサポートします:</span><span class="sxs-lookup"><span data-stu-id="de7c2-123">The peripheral simulator supports interaction between the POS and the following virtual devices:</span></span>

- <span data-ttu-id="de7c2-124">**プリンター** – 仮想周辺機器シミュレーターは POS プリンターに対して設定されている入庫を表示できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-124">**Printer** – The virtual peripheral simulator can show receipts that are configured for a POS printer.</span></span>
- <span data-ttu-id="de7c2-125">**ライン ディスプレイ** – 現物ライン ディスプレイの活動を示す場合は、仮想ライン ディスプレイを設定できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-125">**Line display** – You can configure a virtual line display to show activity on a physical line display.</span></span>
- <span data-ttu-id="de7c2-126">**磁気ストライプ リーダー (MSR)** – 仮想周辺機器シミュレーターから POS にシミュレートされた磁気ストライプのイベントを送信できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-126">**Magnetic stripe reader (MSR)** – You can send simulated magnetic stripe events to the POS from the virtual peripheral simulator.</span></span>
- <span data-ttu-id="de7c2-127">**ドロワー** – 現物キャッシュ ドロワーをシミュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-127">**Drawer** – You can simulate a physical cash drawer.</span></span>
- <span data-ttu-id="de7c2-128">**ドロワー 2** – 周辺シミュレーターに 2 番目のキャッシュ ドロワーを設定することにより、2 つのアクティブなシフトを持つ 1 つの POS レジスターを含むシナリオをシミュレートできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-128">**Drawer 2** – By setting up a second cash drawer in the peripheral simulator, you can simulate scenarios that involve a single POS register that has two active shifts.</span></span>
- <span data-ttu-id="de7c2-129">**スキャナー** – 周辺機器シミュレーターがサポートする仮想バーコード スキャナーは、バーコード スキャン イベントを発行することができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-129">**Scanner** – The virtual bar code scanner that the virtual peripheral simulator supports can issue bar code scan events.</span></span>
- <span data-ttu-id="de7c2-130">**スケール** – A の仮想スケールは POS と計量品目との相互作用をシミュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-130">**Scale** – A virtual scale lets you simulate the interaction of weighed items with the POS.</span></span>
- <span data-ttu-id="de7c2-131">**個人識別番号 (PIN) パッド** – PIN パッドの操作をシミュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-131">**Personal identification number (PIN) pad** – You can simulate PIN pad operations.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-132">支払コネクタによる現物の PIN パッドのサポートを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-132">You must implement support for a physical PIN pad through the payment connector.</span></span>

- <span data-ttu-id="de7c2-133">**署名のキャプチャ** – 仮想周辺機器シミュレーターには、顧客アカウントの支払いなど、一部の入札に必要な署名を求めるプロンプトが表示されるように設定できる仮想署名キャプチャ デバイスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-133">**Signature capture** – The virtual peripheral simulator includes a virtual signature capture device that you can set up to prompt for signatures that are required for some tenders, such as customer account payments.</span></span>
- <span data-ttu-id="de7c2-134">**支払ターミナル** – 仮想支払ターミナルは、POS から仮想支払デバイスへのアプリケーション プログラミング インターフェイス (API) コールをテストするカスタム支払コネクタと組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-134">**Payment terminal** – A virtual payment terminal can be used in conjunction with a custom payment connector to test application programming interface (API) calls from the POS to a virtual payment device.</span></span> <span data-ttu-id="de7c2-135">仮想支払端末を使用するには、支払コネクタを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-135">To use the virtual payment terminal, you must implement a payment connector.</span></span> <span data-ttu-id="de7c2-136">詳細については、<支払コネクタと支払デバイスの実装 (ホワイト ペーパー)>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-136">For more information, see <Implementing a payment connector and payment device (white paper)>.</span></span>

<span data-ttu-id="de7c2-137">仮想周辺機器シミュレータを使用して、バーコード スキャナと MSR から発生するキーボード ウェッジのイベントをシミュレートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-137">You can also use the virtual peripheral simulator to simulate keyboard wedge events that originate from a bar code scanner and MSR.</span></span> <span data-ttu-id="de7c2-138">仮想周辺機器のシミュレーターは、Retail POS 用 Object linking and embedding (OPOS) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-138">The virtual peripheral simulator specifically supports Object Linking and Embedding for Retail POS (OPOS) devices.</span></span>

### <a name="key-scenarios--virtual-peripheral-simulator"></a><span data-ttu-id="de7c2-139">重要なシナリオ – 仮想周辺機器シミュレーター</span><span class="sxs-lookup"><span data-stu-id="de7c2-139">Key scenarios – Virtual peripheral simulator</span></span>

#### <a name="troubleshooting"></a><span data-ttu-id="de7c2-140">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="de7c2-140">Troubleshooting</span></span>

<span data-ttu-id="de7c2-141">周辺シミュレーターを使用し、デバイスの設定をトラブルシューティングできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-141">You can use the peripheral simulator to troubleshoot device setup.</span></span> <span data-ttu-id="de7c2-142">周辺機器シミュレーターまたは同じクラスのセカンド デバイスがない場合、どこで問題が発生したかを特定することが困難になる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-142">If you don't have the peripheral simulator or a second device of the same class, it can be difficult to determine where issues originate.</span></span> <span data-ttu-id="de7c2-143">ただし、周辺シミュレーターがある場合は、仮想デバイスを設定でき、物理デバイスに使用する同じコード パスとビジネス ロジックを実行できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-143">However, when you have the peripheral simulator, you can set up virtual devices, and run the same code paths and business logic that are used for physical devices.</span></span> <span data-ttu-id="de7c2-144">周辺機器シミュレーター側からの仮想デバイスと物理デバイス間の主な違いは、サービス オブジェクト、またはデバイス ドライバです。</span><span class="sxs-lookup"><span data-stu-id="de7c2-144">From the perspective of the peripheral simulator, the main difference between virtual devices and physical devices is the service object, or device driver.</span></span> <span data-ttu-id="de7c2-145">物理デバイスの場合は、サービス オブジェクトはデバイス メーカーによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-145">For physical devices, the service object is provided by the device manufacturer.</span></span> <span data-ttu-id="de7c2-146">対照的に、仮想デバイスの場合、サービス オブジェクトは周辺機器シミュレーターの一部として用意されています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-146">By contrast, for virtual devices, the service objects are provided as part of the peripheral simulator.</span></span> <span data-ttu-id="de7c2-147">周辺機器シミューレーターが正常に機能している場合、ハードウェア プロファイルのデバイス名を実際のデバイスの名前に変更した後にデバイスが正常に機能しない場合は、メーカーが提出したサービス オブジェクトに問題があると想定できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-147">When the peripheral simulator is working correctly, if a device doesn't work correctly after the device name in the hardware profile is changed to the name of a real device, you can assume that there's an issue with the service object that the manufacturer provided.</span></span>

#### <a name="training"></a><span data-ttu-id="de7c2-148">トレーニング</span><span class="sxs-lookup"><span data-stu-id="de7c2-148">Training</span></span>

<span data-ttu-id="de7c2-149">物理的なハードウェアの設定が利用できない場合、周辺機器シミュレーターを使用し、実際的なレイヤーをキャッシャー トレーニングに追加できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-149">You can use the peripheral simulator to add a realistic layer to cashier training when a physical hardware setup isn't available.</span></span> <span data-ttu-id="de7c2-150">周辺機器シミュレーターがトレーニングのシナリオに含まれている場合、レジ担当者は、製品のバーコードのスキャンやギフト カードの読み取りなどのインプットを提供し、さらに特定のトランザクションに対してどの入庫が印刷されるかを確認することにより、より効果的に POS を操作できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-150">When the peripheral simulator is included in training scenarios, the cashier can more effectively interact with the POS by providing input such as product bar code scans and gift card swipes, and by observing which receipts are printed for a specific transaction.</span></span>

#### <a name="testing"></a><span data-ttu-id="de7c2-151">テスト</span><span class="sxs-lookup"><span data-stu-id="de7c2-151">Testing</span></span>

<span data-ttu-id="de7c2-152">周辺機器シミュレーターを使用し、仮想環境の物理的なハードウェアを配置せずに、製品のバーコードや受領書フォーマットなどをテストできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-152">You can use the peripheral simulator to test product bar codes, receipt formats, and so on, without having to deploy physical hardware in a virtual environment.</span></span> <span data-ttu-id="de7c2-153">物理的なハードウェアが必要とされず、ハードウェア ステーションまたは物理的なコンピューターの POS を配置する必要がないため、バック オフィスに行われた変更をより迅速にテストできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-153">Because physical hardware isn't required, and you don't have to deploy a POS client on a hardware station or a physical computer, you can more quickly test changes that are made in the back office.</span></span>

### <a name="set-up-the-virtual-peripheral-simulator"></a><span data-ttu-id="de7c2-154">仮想周辺機器シミュレーターの設定</span><span class="sxs-lookup"><span data-stu-id="de7c2-154">Set up the virtual peripheral simulator</span></span>

#### <a name="set-up-a-hardware-profile"></a><span data-ttu-id="de7c2-155">ハードウェア プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="de7c2-155">Set up a hardware profile</span></span>

1. <span data-ttu-id="de7c2-156">周辺機器シミュレーターを設定するには、**小売り** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-156">To set up the peripheral simulator, go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2. <span data-ttu-id="de7c2-157">**新規**をクリックしてプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-157">Click **New** to create a profile.</span></span>
3. <span data-ttu-id="de7c2-158">**プロファイル番号** および **説明** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-158">Enter values in the **Profile number** and **Description** fields.</span></span>
4. <span data-ttu-id="de7c2-159">テストする必要がある仮想デバイスを設定するには、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-159">Use the following table to set up the virtual devices that must be tested.</span></span> <span data-ttu-id="de7c2-160">表の列の説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-160">Here is an explanation of the columns in the table:</span></span>

   - <span data-ttu-id="de7c2-161">**デバイス** - この列はデバイスを設定するためクイック タブの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-161">**Device** – This column gives the name of the FastTab where you set up the device.</span></span>
   - <span data-ttu-id="de7c2-162">**機器タイプ** – この列は、デバイスの名前のラベルが付いているフィールドで選択した値を提供します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-162">**Device type** – This column gives the value that you select in the field that is labeled with the name of the device.</span></span>
   - <span data-ttu-id="de7c2-163">**デバイス名** – この列はデバイス名に対して入力する正確な値を提供します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-163">**Device name** – This column gives the exact value that you enter for the device name.</span></span>

     > [!IMPORTANT]
     > <span data-ttu-id="de7c2-164">ハードウェア ステーションがこれらの特定の名前を使用し、デバイスに対処するため、ここで指定されたデバイスは必須です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-164">The device names that are given here are required, because the hardware station uses these specific names to address the devices.</span></span> <span data-ttu-id="de7c2-165">次の特定の名前を使用しない場合、デバイスは使用できません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-165">If you don't use the following specific names, the device won't be usable.</span></span>

     <span data-ttu-id="de7c2-166">バーコード スキャナーと MSR のキーボード ウェッジのイベントをシミュレーションするには、ハードウェア プロファイルでの特定の設定は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-166">No specific setup in the hardware profile is required in order to simulate keyboard wedge events from the bar code scanner and MSR.</span></span>

     | <span data-ttu-id="de7c2-167">デバイス</span><span class="sxs-lookup"><span data-stu-id="de7c2-167">Device</span></span>            | <span data-ttu-id="de7c2-168">デバイス タイプ</span><span class="sxs-lookup"><span data-stu-id="de7c2-168">Device type</span></span> | <span data-ttu-id="de7c2-169">デバイス名</span><span class="sxs-lookup"><span data-stu-id="de7c2-169">Device name</span></span>              |
     |-------------------|-------------|--------------------------|
     | <span data-ttu-id="de7c2-170">プリンター</span><span class="sxs-lookup"><span data-stu-id="de7c2-170">Printer</span></span>           | <span data-ttu-id="de7c2-171">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-171">OPOS</span></span>        | <span data-ttu-id="de7c2-172">MockOPOSPrinter</span><span class="sxs-lookup"><span data-stu-id="de7c2-172">MockOPOSPrinter</span></span>          |
     | <span data-ttu-id="de7c2-173">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="de7c2-173">Line display</span></span>      | <span data-ttu-id="de7c2-174">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-174">OPOS</span></span>        | <span data-ttu-id="de7c2-175">MockOPOSLineDisplay</span><span class="sxs-lookup"><span data-stu-id="de7c2-175">MockOPOSLineDisplay</span></span>      |
     | <span data-ttu-id="de7c2-176">MSR</span><span class="sxs-lookup"><span data-stu-id="de7c2-176">MSR</span></span>               | <span data-ttu-id="de7c2-177">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-177">OPOS</span></span>        | <span data-ttu-id="de7c2-178">MockOPOSMSR</span><span class="sxs-lookup"><span data-stu-id="de7c2-178">MockOPOSMSR</span></span>              |
     | <span data-ttu-id="de7c2-179">手形振出人</span><span class="sxs-lookup"><span data-stu-id="de7c2-179">Drawer</span></span>            | <span data-ttu-id="de7c2-180">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-180">OPOS</span></span>        | <span data-ttu-id="de7c2-181">MockOPOSDrawer1</span><span class="sxs-lookup"><span data-stu-id="de7c2-181">MockOPOSDrawer1</span></span>          |
     | <span data-ttu-id="de7c2-182">Drawer2</span><span class="sxs-lookup"><span data-stu-id="de7c2-182">Drawer2</span></span>           | <span data-ttu-id="de7c2-183">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-183">OPOS</span></span>        | <span data-ttu-id="de7c2-184">MockOPOSDrawers</span><span class="sxs-lookup"><span data-stu-id="de7c2-184">MockOPOSDrawers</span></span>          |
     | <span data-ttu-id="de7c2-185">スキャナー</span><span class="sxs-lookup"><span data-stu-id="de7c2-185">Scanner</span></span>           | <span data-ttu-id="de7c2-186">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-186">OPOS</span></span>        | <span data-ttu-id="de7c2-187">MockOPOSScanner</span><span class="sxs-lookup"><span data-stu-id="de7c2-187">MockOPOSScanner</span></span>          |
     | <span data-ttu-id="de7c2-188">スケール</span><span class="sxs-lookup"><span data-stu-id="de7c2-188">Scale</span></span>             | <span data-ttu-id="de7c2-189">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-189">OPOS</span></span>        | <span data-ttu-id="de7c2-190">MockOPOSScale</span><span class="sxs-lookup"><span data-stu-id="de7c2-190">MockOPOSScale</span></span>            |
     | <span data-ttu-id="de7c2-191">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="de7c2-191">PIN Pad</span></span>           | <span data-ttu-id="de7c2-192">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-192">OPOS</span></span>        | <span data-ttu-id="de7c2-193">MockOPOSPinPad</span><span class="sxs-lookup"><span data-stu-id="de7c2-193">MockOPOSPinPad</span></span>           |
     | <span data-ttu-id="de7c2-194">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="de7c2-194">Signature capture</span></span> | <span data-ttu-id="de7c2-195">OPOS</span><span class="sxs-lookup"><span data-stu-id="de7c2-195">OPOS</span></span>        | <span data-ttu-id="de7c2-196">MockOPOSSignatureCapture</span><span class="sxs-lookup"><span data-stu-id="de7c2-196">MockOPOSSignatureCapture</span></span> |

#### <a name="assign-the-hardware-profile-to-a-register"></a><span data-ttu-id="de7c2-197">レジスターへのハードウェア プロファイルの割り当て</span><span class="sxs-lookup"><span data-stu-id="de7c2-197">Assign the hardware profile to a register</span></span>

1. <span data-ttu-id="de7c2-198">ハードウェア プロファイルを作成した後に、チャンネルは、**小売りとコマース** &gt; **チャネル設定** &gt; **POS の設定** &gt; **登録** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-198">After the hardware profile is created, go to **Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Registers**.</span></span>
2. <span data-ttu-id="de7c2-199">**POS レジスター** リストでは、周辺機器シミュレーターを使用する必要があるレジスターに対して、**レジスター番号** フィールドにあるリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-199">In the **POS registers** list, click the link in the **Register number** field for the register that should use the peripheral simulator.</span></span>
3. <span data-ttu-id="de7c2-200">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-200">Click **Edit**.</span></span>
4. <span data-ttu-id="de7c2-201">**プロファイル** セクションの **ハードウェア プロファイル** フィールドでは、仮想周辺機器用に作成したハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-201">In the **Profiles** section, in the **Hardware profile** field, select the hardware profile that you created for virtual peripherals.</span></span>
5. <span data-ttu-id="de7c2-202">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-202">Click **Save**.</span></span>

#### <a name="synchronize-changes-to-the-channel-database"></a><span data-ttu-id="de7c2-203">チャンネル データベースへの変更の同期</span><span class="sxs-lookup"><span data-stu-id="de7c2-203">Synchronize changes to the channel database</span></span>

1. <span data-ttu-id="de7c2-204">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-204">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
2. <span data-ttu-id="de7c2-205">**1090** 配送スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-205">Select the **1090** distribution schedule.</span></span>
3. <span data-ttu-id="de7c2-206">POS への変更を同期させるには、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-206">Click **Run now** to synchronize changes to the POS.</span></span>

<span data-ttu-id="de7c2-207">データが同期されると、新しいハードウェア プロファイルとレジスターへの変更は、チャンネル データベースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-207">After the data is synchronized, the new hardware profile and changes on the register are available in the channel database.</span></span>

## <a name="using-the-virtual-peripheral-simulator"></a><span data-ttu-id="de7c2-208">仮想周辺機器シミュレーターの使用</span><span class="sxs-lookup"><span data-stu-id="de7c2-208">Using the virtual peripheral simulator</span></span>

<span data-ttu-id="de7c2-209">バーチャル ペリフェラル シミュレーターを起動するには、コンピュータの **開始** をクリックし、**Peripheral simulator for Retail** と入力して、検索結果に表示されたときにアプリを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-209">To start the virtual peripheral simulator, click **Start** on your computer, type **Peripheral simulator for Retail**, and then select the app when it appears in the search results.</span></span> <span data-ttu-id="de7c2-210">周辺機器シミュレーションを開始した後、**仮想周辺機器を使用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-210">After you start the peripheral simulator, click **Use virtual peripherals**.</span></span> <span data-ttu-id="de7c2-211">サポートされているデバイスはウィンドウの左側のタブとしてリストされます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-211">The supported devices will be listed as tabs on the left side of the window.</span></span> <span data-ttu-id="de7c2-212">特定のデバイスを表示するには、そのデバイスのタブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-212">To view a specific device, click the tab for that device.</span></span>

### <a name="line-display-capabilities"></a><span data-ttu-id="de7c2-213">ライン ディスプレイ機能</span><span class="sxs-lookup"><span data-stu-id="de7c2-213">Line display capabilities</span></span>

<span data-ttu-id="de7c2-214">仮想ライン ディスプレイを設定すると、POS トランザクションでスキャンする際に、品目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-214">When the virtual line display is configured, it shows line items as they are scanned in the POS transaction.</span></span> <span data-ttu-id="de7c2-215">明細行品目に加えて、支払 / 入金が POS で選択されている場合に支払われる合計を表示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-215">In addition to line items, the display shows the total that is due when a tender is selected at the POS.</span></span> <span data-ttu-id="de7c2-216">また、支払/入金を入力すると、トランザクションに対してまだ支払がされていない金額が表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-216">It also shows the balance that is due if a tender is entered but a balance is still due for the transaction.</span></span> <span data-ttu-id="de7c2-217">POS が使用されていない場合は、レジが終了したことを示すメッセージを表示できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-217">When the POS isn't being used, a message can be shown to indicate that the till is closed.</span></span> <span data-ttu-id="de7c2-218">ハードウェア プロファイルの **ライン ディスプレイ** FastTab のメッセージを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-218">You must configure the message on the **Line display** FastTab in the hardware profile.</span></span>

### <a name="cash-drawer-capabilities"></a><span data-ttu-id="de7c2-219">キャッシュ ドロワー機能</span><span class="sxs-lookup"><span data-stu-id="de7c2-219">Cash drawer capabilities</span></span>

<span data-ttu-id="de7c2-220">仮想キャッシュ ドロワーを使用するようにハードウェア プロファイルが構成されている場合、POS は、支払/入金申告などのドロワー操作に応答して、有効なシフトに対してキャッシュ ドロワーを開きます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-220">When the hardware profile is configured to use virtual cash drawers, the POS opens the cash drawer for the active shift in response to drawer operations such as tender declarations.</span></span> <span data-ttu-id="de7c2-221">POS は、レジ担当者が標準現金店頭払いトランザクション中に現金を変更または預金できるように、キャッシュ ドロワーも開きます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-221">The POS also opens the cash drawer so that the cashier can make change or deposit cash during standard cash-and-carry transactions.</span></span> <span data-ttu-id="de7c2-222">仮想キャッシュ ドロワーには **メイン ドロワー** および **セカンド ドロワー**のラベルがあります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-222">The virtual cash drawers have the labels **Main drawer** and **Secondary drawer**.</span></span> <span data-ttu-id="de7c2-223">これらのラベルはハードウェア プロファイルにドロワーとドロワー 2 とそれぞれ表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-223">These labels represent Drawer and Drawer 2 in the hardware profile, respectively.</span></span> <span data-ttu-id="de7c2-224">ドロワーが閉まると、終了したキャッシュ ドロワーの画像が表示され、終了したキャッシュ ドロワーのボタンには **ドロワーを開く** というラベルが付きます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-224">When a drawer is closed, an image of a closed cash drawer is shown, and the button on the closed cash drawer is labeled **Open drawer**.</span></span> <span data-ttu-id="de7c2-225">このボタンをクリックすると、開いていることを示す開いているキャッシュ ドロワーの画像と置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-225">If you click this button, the image is replaced with an image of an open cash drawer to indicate that the drawer is now open.</span></span> <span data-ttu-id="de7c2-226">開いているキャッシュ ドロワーのボタンには **ドロワーを閉める** というラベルが付きます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-226">The button on the open cash drawer is labeled **Close drawer**.</span></span>

<span data-ttu-id="de7c2-227">POS の複数の操作により、キャッシュ ドロワーを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-227">Several operations at the POS can cause the cash drawer to open.</span></span> <span data-ttu-id="de7c2-228">キャッシュ ドロワーが開いている間はほとんどの操作を続行できません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-228">Most operations can't proceed while the cash drawer is open.</span></span> <span data-ttu-id="de7c2-229">一部の営業終了処理は例外となります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-229">The exceptions are some end-of-day procedures.</span></span> <span data-ttu-id="de7c2-230">POS ユーザーが、キャッシュ ドロワーが開いている間に操作を実行できないことを示すエラー メッセージが表示された場合は、ユーザーは仮想または現物キャッシュ ドロワーを閉じて操作を続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-230">If the POS user receives an error message that states that an operation can't be performed while the cash drawer is open, the user must close the virtual or physical cash drawer to proceed.</span></span> <span data-ttu-id="de7c2-231">キャッシュ ドロワーがハードウェア プロファイルで **共有** とマークされている場合、システムは、操作の前にドロワーが閉じられていることを確認しません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-231">If a cash drawer is marked as **Shared** in the hardware profile, the system doesn't verify that the drawer is closed before an operation.</span></span> <span data-ttu-id="de7c2-232">キャッシュ ドロワーを開いていても、通常通りに操作が進みます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-232">The operation proceeds as usual, even if the cash drawer is open.</span></span> <span data-ttu-id="de7c2-233">この動作は、キャッシュ ドロワーが販売担当者間で共有され、販売担当者がキャッシュ ドロワーを使用する一方で、他の販売担当者が自分の POS デバイスの不適切なタスクを実行するシナリオをサポートします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-233">This behavior supports scenarios where cash drawers are shared among sales associates, and where one associate uses a cash drawer while another associate performs unrelated tasks on his or her own POS device.</span></span> <span data-ttu-id="de7c2-234">キャッシュ ドロワーにした変更は、現在のシフトを閉じ、新しいシフトを開けるまでは確認できません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-234">Changes that are made to the cash drawer aren't evident until the current shift is closed and a new shift is opened.</span></span>

### <a name="msr-capabilities"></a><span data-ttu-id="de7c2-235">MSR 機能</span><span class="sxs-lookup"><span data-stu-id="de7c2-235">MSR capabilities</span></span>

<span data-ttu-id="de7c2-236">周辺機器シミュレーターは、OPOS モードまたはキーボード ウェッジ モードで操作することにより、仮想 MSR 操作に対して堅牢なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-236">The peripheral simulator provides robust support for virtual MSR operations by working in either OPOS mode or keyboard wedge mode.</span></span> <span data-ttu-id="de7c2-237">OPOS モードでは OPOS デバイスとして機能するようにハードウェア プロファイルで MSR を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-237">OPOS mode requires that the MSR be configured in the hardware profile to work as an OPOS device.</span></span> <span data-ttu-id="de7c2-238">キーボード ウェッジ モードは Microsoft Windows に、キーボード ウェッジ データ イベントを送信するのみです。</span><span class="sxs-lookup"><span data-stu-id="de7c2-238">Keyboard wedge mode just sends keyboard wedge data events to Microsoft Windows.</span></span> <span data-ttu-id="de7c2-239">設定が異なること以外にも、OPOS とキーボード ウェッジ モードは次の点において違います。</span><span class="sxs-lookup"><span data-stu-id="de7c2-239">Besides differences in setup, OPOS and keyboard wedge modes differ in the following ways:</span></span>

- <span data-ttu-id="de7c2-240">POS クライアントでは、ロイヤルティまたはギフト カードのエントリに対して磁気ストライプ データを有効にするシナリオなど、特定のシナリオに対して、OPOS MSR デバイスが有効になります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-240">The POS client enables OPOS MSR devices for specific scenarios, such as scenarios that allow for magnetic stripe data for loyalty or gift card entry.</span></span>
- <span data-ttu-id="de7c2-241">キーボード ウェッジ モードでは、データが送信されると、周辺機器シミュレーターがキーボード ウェッジ データを有効なフィールドに送信します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-241">In keyboard wedge mode, the peripheral simulator sends keyboard wedge data to the field that is active when the data is sent.</span></span> <span data-ttu-id="de7c2-242">この動作は、データがキーボードにより入力された場合に実行される動作に似ています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-242">This behavior resembles the behavior that occurs if the data is entered by using a keyboard.</span></span> <span data-ttu-id="de7c2-243">キーボード ウェッジとして MSR を使用するには、ユーザーはデータが正しいフィールド受信されるように、Retail Modern POS (MPOS) に切り替える必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-243">To use the MSR as a keyboard wedge, the user must switch to Retail Modern POS (MPOS) to make sure that data is received in the correct field.</span></span> <span data-ttu-id="de7c2-244">したがって、データが正しいフィールドに送信されるかを確認できる時間をユーザーに与えるため、遅延を設定できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-244">Therefore, you can configure a delay, so that the user has time to make sure that the data will be sent to the correct field.</span></span>

#### <a name="testing-gift-and-payment-card-swipes"></a><span data-ttu-id="de7c2-245">ギフト カードや支払カードの読み取りのテスト</span><span class="sxs-lookup"><span data-stu-id="de7c2-245">Testing gift and payment card swipes</span></span>

<span data-ttu-id="de7c2-246">周辺機器シミュレーターが提供する仮想 MSR はギフト カードや支払カードの読み取りにおけるシナリオをテストするために特定の MSR データを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-246">The virtual MSR that the peripheral simulator provides also lets you configure specific MSR data to test scenarios for gift and payment card swipes.</span></span> <span data-ttu-id="de7c2-247">カードを作成するには、プラス記号 (**+**) タンをクリックし、カードのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-247">To create a card, click the plus sign (**+**) button, and select the type of card.</span></span> <span data-ttu-id="de7c2-248">その後、定義しているカードの有効期限の月と年を含め、カード番号を指定するか、または POS に送信する必要があるデータを追跡します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-248">Then specify the card number or track data that should be sent to the POS, together with the expiration month and year for the card that you're defining.</span></span> <span data-ttu-id="de7c2-249">**カードの種類** フィールドで選択した値は、カードにマップできるだけのラベルです。</span><span class="sxs-lookup"><span data-stu-id="de7c2-249">The value that you select in the **Type of card** field is just a label that can be mapped to a card.</span></span> <span data-ttu-id="de7c2-250">このラベルにより、周辺機器シミュレーターでカードを読み取ると、カードを識別し易くなります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-250">This label makes it easier to identify cards when they are swiped through the peripheral simulator.</span></span> <span data-ttu-id="de7c2-251">画像の上の左矢印 (**&lt;**) および右矢印 (**&gt;**) ボタンを使用して、周辺機器シミュレーターで設定されたカードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-251">You can select cards that have been configured in the peripheral simulator by using the left arrow (**&lt;**) and right arrow (**&gt;**) buttons above the image of the card.</span></span> <span data-ttu-id="de7c2-252">プラス記号 (**+**) ボタンの隣にある **編集** および **削除** ボタンを使用することにより、カードを編集または削除できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-252">You can edit and delete cards by using the **Edit** and **Delete** buttons next to the plus sign (**+**) button.</span></span>

### <a name="pin-pad"></a><span data-ttu-id="de7c2-253">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="de7c2-253">PIN pad</span></span>

<span data-ttu-id="de7c2-254">PIN パッドのシミュレーターを設定し、OPOS PIN パッドをシミュレートできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-254">You can configure the PIN pad simulator to simulate an OPOS PIN pad.</span></span> <span data-ttu-id="de7c2-255">電子決済 (EFT) トランザクションが POS で実行され、PIN の入力を必要とするとき、ハードウェア ステーションは、PIN デバイスを呼び出して、PIN 入力を要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-255">When an electronic funds transfer (EFT) transaction is performed at the POS and requires that a PIN be entered, the hardware station calls the PIN device to prompt for PIN entry.</span></span> <span data-ttu-id="de7c2-256">操作するには、周辺機器シミュレーターの PIN パッドが EFT 支払コネクターをサポートしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-256">To work, the PIN pad in the peripheral simulator must support an EFT payment connector.</span></span>

### <a name="printer"></a><span data-ttu-id="de7c2-257">プリンター</span><span class="sxs-lookup"><span data-stu-id="de7c2-257">Printer</span></span>

<span data-ttu-id="de7c2-258">仮想周辺機器のプリンタには、POS から印刷されると入庫が表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-258">The virtual peripheral printer just shows receipts as they are printed from the POS.</span></span> <span data-ttu-id="de7c2-259">印刷工程で複数の入庫が作成される場合、入庫をスクロールできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-259">If a print operation produces multiple receipts, you can scroll through the receipts.</span></span>

#### <a name="configure-receipt-printing"></a><span data-ttu-id="de7c2-260">入庫印刷の構成</span><span class="sxs-lookup"><span data-stu-id="de7c2-260">Configure receipt printing</span></span>

1. <span data-ttu-id="de7c2-261">**小売** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-261">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profiles**.</span></span>
2. <span data-ttu-id="de7c2-262">仮想周辺機器用に作成したハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-262">Select the hardware profile that you created for virtual peripherals.</span></span>
3. <span data-ttu-id="de7c2-263">**プリンタ** FastTab で、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-263">On the **Printer** FastTab, click **Edit**.</span></span>
4. <span data-ttu-id="de7c2-264">**レシート プロファイル ID** フィールドで、レシート プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-264">In the **Receipt profile ID** field, select a receipt profile.</span></span>
5. <span data-ttu-id="de7c2-265">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-265">Click **Save**.</span></span>

#### <a name="scale"></a><span data-ttu-id="de7c2-266">スケール</span><span class="sxs-lookup"><span data-stu-id="de7c2-266">Scale</span></span>

<span data-ttu-id="de7c2-267">スケールの製品が POS トランザクションに追加され、スケールが設定されると、POS によってスケールから重量を取得します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-267">When a scale product is added to the POS transaction, and a scale is configured, the POS retrieves the weight from the scale.</span></span> <span data-ttu-id="de7c2-268">仮想スケールと物理的スケールについては、製品がトランザクションに追加される前に製品と重量を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-268">For both the virtual and physical scale, the product or weight should be specified before the product is added to the transaction.</span></span> <span data-ttu-id="de7c2-269">スケール製品をトランザクションに追加する前に、周辺機器シミュレーターに移動し、プラス記号 (**+**) およびマイナス記号 (**–**) ボタンを使用して、スケールがレポートする必要がある重量を調整します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-269">Before you add the scale product to the transaction, go to the scale in the peripheral simulator, and use the plus sign (**+**) and minus sign (**–**) buttons to adjust the weight that the scale should report.</span></span> <span data-ttu-id="de7c2-270">**現在の値** フィールドで目的の重量を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-270">You can also enter the desired weight directly in the **Current value** field.</span></span> <span data-ttu-id="de7c2-271">プラス記号 (**+**)、**編集**、および **削除** ボタンを使用することにより、重量単位を調整できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-271">You can adjust the units of weight for the scale by using the plus sign (**+**), **Edit**, and **Delete** buttons.</span></span> <span data-ttu-id="de7c2-272">これにより、単位は、重さを測る製品またはスケールを使用するロケールをベースに指定されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-272">In this way, units can be specified based on the products that are weighed or the locale where the scale is used.</span></span>

##### <a name="configure-a-scale-product"></a><span data-ttu-id="de7c2-273">スケール製品の設定</span><span class="sxs-lookup"><span data-stu-id="de7c2-273">Configure a scale product</span></span>

1. <span data-ttu-id="de7c2-274">**小売** &gt; **製品とカテゴリ** &gt; **カテゴリ別リリース済製品**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-274">Go to **Retail** &gt; **Products and categories** &gt; **Released products by category**.</span></span>
2. <span data-ttu-id="de7c2-275">製品レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-275">Open the product record.</span></span>
3. <span data-ttu-id="de7c2-276">重さを測る製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-276">Select the product to weigh.</span></span>
4. <span data-ttu-id="de7c2-277">**小売** FastTab で **スケール製品** オプションを **いいえ** から **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-277">On the **Retail** FastTab, set the **Scale product** option from **No** to **Yes**.</span></span>

##### <a name="synchronize-changes-to-the-channel-database"></a><span data-ttu-id="de7c2-278">チャンネル データベースへの変更の同期</span><span class="sxs-lookup"><span data-stu-id="de7c2-278">Synchronize changes to the channel database</span></span>

1. <span data-ttu-id="de7c2-279">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-279">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
2. <span data-ttu-id="de7c2-280">**1040** 配送スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-280">Select the **1040** distribution schedule.</span></span>
3. <span data-ttu-id="de7c2-281">POS への変更を同期させるには、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-281">Click **Run now** to synchronize changes to the POS.</span></span>

<span data-ttu-id="de7c2-282">データが同期されると、スケールの製品が POS トランザクションに追加され、POS は重量に対してスケールをチェックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-282">After the data is synchronized, when a scale product is added to the POS transaction, the POS checks the scale for the weight.</span></span>

#### <a name="signature-capture"></a><span data-ttu-id="de7c2-283">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="de7c2-283">Signature capture</span></span>

<span data-ttu-id="de7c2-284">仮想署名のキャプチャ デバイスは、使用している支払/入金が署名を必要とする場合、仮想署名のキャプチャ パッドに署名を提供するようユーザーに要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-284">The virtual signature capture device prompts the user to provide a signature on the virtual signature capture pad when the tender that is used requires a signature.</span></span> <span data-ttu-id="de7c2-285">ユーザーが署名を承諾すると、POS に署名を表示できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-285">The user can accept the signature to show it at the POS.</span></span> <span data-ttu-id="de7c2-286">そして、レジ担当者が署名を承諾できるようになります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-286">The cashier can then accept the signature.</span></span> <span data-ttu-id="de7c2-287">署名は支払/入金とともに保存され、バック オフィスに他のトランザクション データとともに同期されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-287">The signature is then saved together with the tender and is synchronized to the back office together with other transaction data.</span></span>

##### <a name="set-up-a-tender-to-require-a-signature"></a><span data-ttu-id="de7c2-288">署名を要求するよう支払/入金を設定する</span><span class="sxs-lookup"><span data-stu-id="de7c2-288">Set up a tender to require a signature</span></span>

1. <span data-ttu-id="de7c2-289">**小売** &gt; **チャンネル** &gt; **小売店舗** &gt; **すべての小売店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-289">Go to **Retail** &gt; **Channels** &gt; **Retail stores** &gt; **All retail stores**.</span></span>
2. <span data-ttu-id="de7c2-290">小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-290">Select the retail store.</span></span>
3. <span data-ttu-id="de7c2-291">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-291">Click **Edit**.</span></span>
4. <span data-ttu-id="de7c2-292">**設定** をクリックしてから、**設定** セクションで、**支払方法** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-292">Click **Set up**, and then, in the **Set up** section, click **Payment methods**.</span></span>
5. <span data-ttu-id="de7c2-293">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-293">Click **Edit**.</span></span>
6. <span data-ttu-id="de7c2-294">署名を要求する支払方法を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-294">Select the payment method that requires a signature.</span></span>
7. <span data-ttu-id="de7c2-295">**一般l** セクションの **署名キャプチャ** で **署名キャプチャ デバイスの使用** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-295">In the **General** section, under **Signature Capture**, set the **Use signature capture device** option to **Yes**.</span></span>
8. <span data-ttu-id="de7c2-296">**署名キャプチャの最小額** フィールドで、署名のキャプチャをトリガする必要がある最小額を入力します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-296">In the **Signature capture minimum amount** field, enter the minimum amount that should trigger signature capture.</span></span>

##### <a name="synchronize-changes-to-the-channel-database"></a><span data-ttu-id="de7c2-297">チャンネル データベースへの変更の同期</span><span class="sxs-lookup"><span data-stu-id="de7c2-297">Synchronize changes to the channel database</span></span>

1. <span data-ttu-id="de7c2-298">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-298">Go to **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
2. <span data-ttu-id="de7c2-299">**1070** 配送スケジュールを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-299">Select the **1070** distribution schedule.</span></span>
3. <span data-ttu-id="de7c2-300">POS への変更を同期させるには、**今すぐ実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-300">Click **Run now** to synchronize changes to the POS.</span></span>

<span data-ttu-id="de7c2-301">データが同期されると、署名を必要とする支払/入金が使用され、金額が署名のしきい値を満たす場合は、POS は仮想署名のキャプチャ デバイスで署名を要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-301">After the data is synchronized, when a tender is used that requires a signature, and the amount meets the signature threshold, the POS prompts for a signature on the virtual signature capture device.</span></span>

#### <a name="additional-configuration"></a><span data-ttu-id="de7c2-302">追加設定</span><span class="sxs-lookup"><span data-stu-id="de7c2-302">Additional configuration</span></span>

<span data-ttu-id="de7c2-303">周辺機器シミュレーターのコンフィギュレーション ファイルを編集して、テストしているシナリオに対してさらに適切に取り組むことができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-303">You can edit the peripheral simulator's configuration file to more appropriately address the scenarios that you're testing.</span></span> <span data-ttu-id="de7c2-304">構成ファイルは C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config で見つけることができます。構成ファイルはスケール上でのテストに使用可能な単位、テストで使用可能なカードの種類、およびバー コード タイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-304">You can find the configuration file at C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. The configuration file defines the units that are available for testing on the scale, the card types that are available for testing, and bar code types.</span></span> <span data-ttu-id="de7c2-305">たとえば、コンフィギュレーション ファイルのテキスト値の変更することによって、実行時に選択できる新しいカード タイプまたは新しい測定単位を追加できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-305">For example, by modifying the text values in the configuration file, you can add a new card type or a new unit of measure that can be selected at runtime.</span></span> <span data-ttu-id="de7c2-306">新しい値は、アプリケーションの再起動後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-306">The new values will appear after the app is restarted.</span></span>

#### <a name="troubleshooting"></a><span data-ttu-id="de7c2-307">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="de7c2-307">Troubleshooting</span></span>

<span data-ttu-id="de7c2-308">周辺機器シミュレーターの活動は、周辺機器シミュレーター内に記録されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-308">Activities for the peripheral simulator are logged in the peripheral simulator.</span></span> <span data-ttu-id="de7c2-309">ログは C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config で見つけることができます。周辺機器シミュレーターも Windows イベント ログに問題をレポートします。これには **アプリケーションとサービス ログ** &gt; **Microsoft** &gt; **DynamicsAX** でアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-309">You can find the log at C:\\Program Files (x86)\\Microsoft Dynamics 365\\70\\VirtualPeripherals\\Microsoft.Dynamics.Commerce.VirtualPeripherals.Client.exe.config. The peripheral simulator also reports issues to the Windows event log, which you can access at **Application and Services Logs** &gt; **Microsoft** &gt; **DynamicsAX**.</span></span>

<span data-ttu-id="de7c2-310">MPOS または周辺機器シミュレーターを使用する場合に、ハードウェア プロファイルまたはその他の領域に加えた変更が明示的でない場合、チャンネルのデータベースにデータを同期する上で使用する配送スケジューラ ジョブを確認します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-310">If changes that you made to the hardware profile or other areas aren't evident when you use MPOS or the peripheral simulator, check the distribution scheduler jobs that you used to synchronize the data to the channel database.</span></span> <span data-ttu-id="de7c2-311">変更が同期された後に、POS でまだ確認できない場合、POS クライアントを再起動します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-311">If the changes were synchronized but still aren't evident at the POS, restart the POS client.</span></span>

<span data-ttu-id="de7c2-312">コンフィギュレーションされたキャッシュ ドロワーへの変更は、新しいシフトが作成されるまで有効になりません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-312">Changes to configured cash drawers aren't effective until a new shift is created.</span></span> <span data-ttu-id="de7c2-313">そのため、キャッシュ ドロワーに変更を加えた場合、新しいキャッシュ ドロワーの設定をテストするには、既存のシフトが常に閉まっているかを確認します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-313">Therefore, if you make changes to cash drawers, make sure that you always close the existing shift to test the new cash drawer setup.</span></span>

<span data-ttu-id="de7c2-314">メーカーのドライバがモンロー顧問サービスのコモン コントロール オブジェクトの後にインストールされている場合、ドライバが原因でコモン コントロール オブジェクトが正しく動作しなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-314">Sometimes, if a manufacturer's driver is installed after the common control objects from Monroe Consulting Services, the driver can cause the common control objects to stop working correctly.</span></span> <span data-ttu-id="de7c2-315">この場合、コモン コントロール オブジェクトを再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-315">In this case, you should reinstall the common control objects.</span></span>

<span data-ttu-id="de7c2-316">インストール時に、仮想周辺機器シミュレータに関連する特定のアセンブリが誤って登録されている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-316">At install time, it's possible that certain assemblies related to the virtual peripheral simulator were registered incorrectly.</span></span> <span data-ttu-id="de7c2-317">この問題は、仮想デバイスを使用しようとすると「OPOS_E_CLOSED」というエラーに関連することがよくあります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-317">This issue is often associated with an 'OPOS_E_CLOSED' error when attempting to use a virtual device.</span></span> <span data-ttu-id="de7c2-318">これは、Windows アセンブリ登録ツールを実行して修正できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-318">This can be corrected by running the Windows Assembly Registration tool.</span></span> <span data-ttu-id="de7c2-319">アセンブリ (Microsoft.Dynamics.Commerce.VirtualPeripherals.ServiceObjects.dll) を登録するには、管理者としてコマンド プロンプトを開き、'regasm /codebase "C:\Program Files (x86)\Microsoft Dynamics 365\70\Peripheral simulator for Retail\Microsoft.Dynamics.Commerce.VirtualPeripherals.ServiceObjects.dll"' を実行します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-319">To register the assembly (called Microsoft.Dynamics.Commerce.VirtualPeripherals.ServiceObjects.dll), open a command prompt as administrator and run 'regasm /codebase "C:\Program Files (x86)\Microsoft Dynamics 365\70\Peripheral simulator for Retail\Microsoft.Dynamics.Commerce.VirtualPeripherals.ServiceObjects.dll"'.</span></span>

## <a name="pos-simulator"></a><span data-ttu-id="de7c2-320">POS シミュレーター</span><span class="sxs-lookup"><span data-stu-id="de7c2-320">POS simulator</span></span>

<span data-ttu-id="de7c2-321">POS シミュレーターを使用すると、デバイスの製造元、独立系ソフトウェア ベンダー (ISV)、および小売業者が POS を配置しなくても周辺機器をテストできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-321">The POS simulator lets device manufacturers, independent software vendors (ISVs), and retailers test peripheral devices without having to deploy the POS.</span></span> <span data-ttu-id="de7c2-322">MPOS およびスタンドアロン ハードウェア ステーションと同様のビジネス ロジックを小売周辺機器に使用することにより、POS シミュレーターはスタンドアロン ユーティリティとして POS とのデバイス ドライバーの互換性を判断できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-322">By using the same business logic for retail peripherals as MPOS and the standalone hardware station, the POS simulator can determine device driver compatibility with the POS as a standalone utility.</span></span> <span data-ttu-id="de7c2-323">したがって、デバイスの選択は、POS のセットアップと展開とは独立して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-323">Therefore, device selection can occur independently of POS setup and deployment.</span></span>

<span data-ttu-id="de7c2-324">POS シミュレーターは、Retail 用の独立したスタンドアロン ユーティリティとしても提供されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-324">The POS simulator is also provided as a standalone utility that is independent of Retail.</span></span> <span data-ttu-id="de7c2-325">スタンドアロン ユーティリティとして、POS シミュレータは主に周辺デバイスの互換性をテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-325">As a standalone utility, the POS simulator is primarily used to test peripheral device compatibility.</span></span> <span data-ttu-id="de7c2-326">POS シミュレーターを使用してテストされたデバイスのみ、新しい POS の配置に許容可能です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-326">Only devices that are tested by using the POS simulator are acceptable for new deployments of the POS.</span></span> <span data-ttu-id="de7c2-327">テストは、デバイス メーカー自体が推進する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-327">Testing should be driven by the device manufacturers themselves.</span></span> <span data-ttu-id="de7c2-328">POS シミュレーターの概要の各パートは、互換性テストに POS シミュレーターを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-328">Parts of the POS simulator overview are intended to explain how the POS simulator is used for compatibility testing.</span></span> <span data-ttu-id="de7c2-329">POS またはスタンドアロン ハードウェア ステーションとの互換性についてデバイスをテストすることに関心があるメーカーは、drpc@microsoft.com まで電子メールを送信してプログラムに関する情報を求める必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-329">Manufacturers that are interested in testing their devices for compatibility with the POS or standalone hardware station should send an email to drpc@microsoft.com to request information about the program.</span></span>

### <a name="using-the-pos-simulator"></a><span data-ttu-id="de7c2-330">POS シミュレーターの使用</span><span class="sxs-lookup"><span data-stu-id="de7c2-330">Using the POS simulator</span></span>

1. <span data-ttu-id="de7c2-331">コンピューターの**開始** をクリックし、**小売の周辺シミュレーター**を入力してから、検索結果に表示されるアプリを選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-331">Click **Start** on your computer, type **Peripheral simulator for Retail**, and then select the app when it appears in the search results.</span></span>
2. <span data-ttu-id="de7c2-332">**仮想周辺機器を使用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-332">Click **Use virtual peripherals**.</span></span> <span data-ttu-id="de7c2-333">サポートされているデバイスはウィンドウの左側のタブとしてリストされます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-333">The supported devices will be listed as tabs on the left side of the window.</span></span> <span data-ttu-id="de7c2-334">特定のデバイスを表示するには、そのデバイスのタブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-334">To view a specific device, click the tab for that device.</span></span>

<span data-ttu-id="de7c2-335">POS シミュレーターは、次のデバイスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-335">The POS simulator supports the following devices:</span></span>

- <span data-ttu-id="de7c2-336">ライン ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="de7c2-336">Line display</span></span>
- <span data-ttu-id="de7c2-337">キャッシュ ドロワー</span><span class="sxs-lookup"><span data-stu-id="de7c2-337">Cash drawer</span></span>
- <span data-ttu-id="de7c2-338">MSR</span><span class="sxs-lookup"><span data-stu-id="de7c2-338">MSR</span></span>
- <span data-ttu-id="de7c2-339">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="de7c2-339">PIN pad</span></span>
- <span data-ttu-id="de7c2-340">プリンター</span><span class="sxs-lookup"><span data-stu-id="de7c2-340">Printer</span></span>
- <span data-ttu-id="de7c2-341">スケール</span><span class="sxs-lookup"><span data-stu-id="de7c2-341">Scale</span></span>
- <span data-ttu-id="de7c2-342">署名キャプチャ パッド</span><span class="sxs-lookup"><span data-stu-id="de7c2-342">Signature capture pad</span></span>
- <span data-ttu-id="de7c2-343">バーコード スキャナー</span><span class="sxs-lookup"><span data-stu-id="de7c2-343">Bar code scanner</span></span>
- <span data-ttu-id="de7c2-344">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="de7c2-344">Payment terminal</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-345">支払ターミナルには、支払コネクタが必要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-345">A payment terminal requires that a payment connector be present.</span></span> <span data-ttu-id="de7c2-346">詳細については、[支払ターミナルと支払の統合](end-to-end-payment-extension.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-346">For more information, see [Payment integration with a payment terminal](end-to-end-payment-extension.md).</span></span>

<span data-ttu-id="de7c2-347">サポートされているデバイスの一覧に**設定**タブがあります。**設定**タブを使用して、POS シミュレーターとテストされているデバイスとの通信方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-347">Below the list of supported devices, there is a **Settings** tab. You can use the **Settings** tab to specify how the POS simulator should communicate with the devices that are being tested.</span></span> <span data-ttu-id="de7c2-348">**ランタイム**を選択すると、POS シミュレーターがデバイスと通信するのに使用する方法は、組み込みハードウェア局を持つ MPOS が通信する方法と類似するようになります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-348">If **Runtime** is selected, the method that the POS simulator uses to communicate with the device resembles the method that MPOS that has a built-in hardware station communicates.</span></span> <span data-ttu-id="de7c2-349">**Win32** が選択されている場合、POS シミュレーターはデバイスと直接通信します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-349">If **Win32** is selected, the POS simulator communicates directly with the device.</span></span> <span data-ttu-id="de7c2-350">この通信方法は、スタンドアロン ハードウェア ステーションが通信する方法に似ています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-350">This communication method resembles the method that a standalone hardware station communicates.</span></span>

<span data-ttu-id="de7c2-351">**設定**タブで、テストを実行しているユーザーに関する詳細も提供できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-351">On the **Settings** tab, you can also provide details about the user who is performing the tests.</span></span> <span data-ttu-id="de7c2-352">これらの詳細は、互換性テストを行うメーカーにとって重要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-352">These details are important for manufacturers that perform compatibility testing.</span></span>

### <a name="configuring-the-pos-simulator"></a><span data-ttu-id="de7c2-353">POS シミュレーターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="de7c2-353">Configuring the POS simulator</span></span>

<span data-ttu-id="de7c2-354">サポートされているデバイス クラスごとに、POS シミュレーターは複数のデバイスを設定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-354">For each supported device class, the POS simulator lets you set up multiple devices.</span></span> <span data-ttu-id="de7c2-355">たとえば、複数のプリンターは、POS シミュレーターでコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-355">For example, several printers can be configured in the POS simulator.</span></span> <span data-ttu-id="de7c2-356">**プリンター** タブで、ユーザーは設定されたデバイスを順番に調べ、必要に応じてテストすることができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-356">Then, on the **Printer** tab, the user can cycle through the configured devices and test them as required.</span></span>

<span data-ttu-id="de7c2-357">デバイスで使用可能なセットアップ パラメーターは、デバイスのタイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-357">The setup parameters that are available for a device depend on the type of device.</span></span> <span data-ttu-id="de7c2-358">新しいデバイスを設定するには、テストするデバイスのクラスを選択し、[プラス記号 (**+**)] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-358">To set up a new device, select the class of device to test, and then click the plus sign (**+**) button.</span></span> <span data-ttu-id="de7c2-359">利用可能なデバイスパラメーターのメニューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-359">A menu of the available device parameters appears.</span></span>

<span data-ttu-id="de7c2-360">すでに作成されているデバイスを編集するには、左矢印 (**&lt;**) と右矢印 (**&gt;**) ボタンを使用して適切なデバイスを見つけ、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-360">To edit a device that has already been created, use the left arrow (**&lt;**) and right arrow (**&gt;**) buttons to find the appropriate device, and then click **Edit**.</span></span>

#### <a name="configure-an-opos-device"></a><span data-ttu-id="de7c2-361">OPOS デバイスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="de7c2-361">Configure an OPOS device</span></span>

1. <span data-ttu-id="de7c2-362">デバイス タイプとして **OPOS** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-362">Select **OPOS** as the device type.</span></span>
2. <span data-ttu-id="de7c2-363">デバイス ドライバーの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-363">Select the name of the device driver.</span></span> <span data-ttu-id="de7c2-364">この値は必須です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-364">This value is required.</span></span> <span data-ttu-id="de7c2-365">このリストには、デバイスがテストされているローカル マシンにインストールされているすべての OPOS サービス オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-365">This list includes all the OPOS service objects that are installed on the local machine where devices are being tested.</span></span> <span data-ttu-id="de7c2-366">手動でデバイス ドライバー名を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-366">You can also manually enter the device driver name.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de7c2-367">POS シミュレーターを使用して OPOS デバイスをテストする前に、OPOS コモン コントロール オブジェクトをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-367">Before you can test OPOS devices by using the POS simulator, OPOS common control objects must be installed.</span></span> <span data-ttu-id="de7c2-368">これらのオブジェクトは、製造業者が提供するサービス オブジェクトとは別個のものです。</span><span class="sxs-lookup"><span data-stu-id="de7c2-368">These objects are separate are separate from the service objects that the manufacturer provides.</span></span>

3. <span data-ttu-id="de7c2-369">残りの必須フィールドにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-369">Enter data in the rest of the required fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-370">テスト用に機器をコンフィギュレーションするときは、POS シミュレーションが POS との互換性を確認できるようにするために、すべてのフィールドの値が必要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-370">When you configure devices for testing, all fields are required, so that the POS simulator can confirm compatibility with the POS.</span></span>

4. <span data-ttu-id="de7c2-371">デバイスがカジュアル テストまたは互換性テストに必要なレベルに構成されているときは、**デバイスの保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-371">When the device is configured to the level that is required for either casual testing or compatibility testing, click **Save device**.</span></span>

#### <a name="configure-a-network-device"></a><span data-ttu-id="de7c2-372">ネットワーク デバイスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="de7c2-372">Configure a network device</span></span>

<span data-ttu-id="de7c2-373">POS シミュレーターは、ネットワーク デバイスをテストするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-373">The POS simulator can be used to test network devices.</span></span> <span data-ttu-id="de7c2-374">次のネットワーク デバイスがそのまま使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-374">The following network devices are supported out of the box:</span></span>

- <span data-ttu-id="de7c2-375">**キャッシュ ドロワー:** APG Atwood</span><span class="sxs-lookup"><span data-stu-id="de7c2-375">**Cash drawer:** APG Atwood</span></span>
- <span data-ttu-id="de7c2-376">**レシート プリンター:** Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="de7c2-376">**Receipt printer:** Star TSP650II</span></span>
- <span data-ttu-id="de7c2-377">**支払ターミナル:** 支払ターミナルはネットワークデバイスとして構成することができますが、支払ターミナルのテストにはカスタム支払コネクタが必要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-377">**Payment terminal:** Although a payment terminal can be configured as network devices, any testing of a payment terminal requires a custom payment connector.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-378">支払ターミナルはそのまま使用できません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-378">No payment terminals are supported out of the box.</span></span>

1. <span data-ttu-id="de7c2-379">デバイス タイプとして **ネットワーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-379">Select **Network** as the device type.</span></span>
2. <span data-ttu-id="de7c2-380">残りのフィールドのデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-380">Enter data for the rest of the fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-381">デバイス ドライバー名、モデル、およびバージョンのフィールドは、テスト対象のデバイス固有の実装のバージョンを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-381">The fields for the device driver name, model, and version can help identify the version of the device-specific implementation that is being tested.</span></span> <span data-ttu-id="de7c2-382">デバイスは IP 上で独自の通信プロトコルを持つ傾向があるため、カスタム実装には特定の属性でラベルを付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-382">Because devices tend to have their own communication protocol over IP, custom implementations should be labeled with specific attributes.</span></span>

3. <span data-ttu-id="de7c2-383">デバイスがカジュアル テストまたは互換性テストに必要なレベルに構成されているときは、**デバイスの保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-383">When the device is configured to the level that is required for either casual testing or compatibility testing, click **Save device**.</span></span>

#### <a name="windows-devices"></a><span data-ttu-id="de7c2-384">Windows デバイス</span><span class="sxs-lookup"><span data-stu-id="de7c2-384">Windows devices</span></span>

<span data-ttu-id="de7c2-385">POS シミュレーターは、Windows プリンターをテストするためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-385">The POS simulator can also be used to test Windows printers.</span></span> <span data-ttu-id="de7c2-386">セットアップ パラメーターは、OPOS デバイスのパラメーターと同じです。</span><span class="sxs-lookup"><span data-stu-id="de7c2-386">The setup parameters are the same as the parameters for OPOS devices.</span></span>

1. <span data-ttu-id="de7c2-387">デバイス タイプとして **プリンター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-387">Select **Printer** as the device type.</span></span>
2. <span data-ttu-id="de7c2-388">残りの必須フィールドにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-388">Enter data in the rest of the required fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="de7c2-389">テスト用に機器をコンフィギュレーションするときは、POS シミュレーションが POS との互換性を確認できるようにするために、すべてのフィールドの値が必要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-389">When you configure devices for testing, all fields are required, so that the POS simulator can confirm compatibility with the POS.</span></span>

3. <span data-ttu-id="de7c2-390">デバイスがカジュアル テストまたは互換性テストに必要なレベルに構成されているときは、**デバイスの保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-390">When the device is configured to the level that is required for either casual testing or compatibility testing, click **Save device**.</span></span>

### <a name="testing-devices"></a><span data-ttu-id="de7c2-391">デバイスのテスト</span><span class="sxs-lookup"><span data-stu-id="de7c2-391">Testing devices</span></span>

<span data-ttu-id="de7c2-392">各デバイス クラスには、固有のテスト機能があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-392">Each device class has unique testing capabilities.</span></span> <span data-ttu-id="de7c2-393">デバイス固有のテストに加えて、各デバイスには**自己テスト**機能があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-393">In addition to device-specific tests, each device has a **Self-test** function.</span></span>

<span data-ttu-id="de7c2-394">デバイスの互換性をテストするときは、デバイスを設定してから、緑の矢印をクリックして自己テストを開始します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-394">When you're testing a device for compatibility, set up the device, and then click the green arrow to begin the self-test.</span></span> <span data-ttu-id="de7c2-395">各デバイスで、POS (**ランタイム**モードで) またはスタンドアロン ハードウェアステーション (**Win32** モードで) のデバイスの互換性を決定するために、異なる一連のテストが実行されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-395">For each device, a different set of tests is performed to determine the device's compatibility with the POS (in **Runtime** mode) or the standalone hardware station (in **Win32** mode).</span></span> <span data-ttu-id="de7c2-396">一部のデバイスでは、テストにはユーザー操作が必要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-396">For some devices, the test requires user interaction.</span></span> <span data-ttu-id="de7c2-397">たとえば、バーコード スキャナーの自己テストは、バーコードのスキャンを必要とします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-397">For example, the self-test for a bar code scanner requires that a bar code be scanned.</span></span> <span data-ttu-id="de7c2-398">したがって、セルフテストはユーザーにバーコードをスキャンするよう指示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-398">Therefore, the self-test will instruct the user to scan a bar code.</span></span>

<span data-ttu-id="de7c2-399">各セルフ テストおよび各手動操作による結果は、デバイス テスト ページの **ログ** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-399">Results from each self-test and each manual operation are shown in the **Log** section of the device test page.</span></span> <span data-ttu-id="de7c2-400">**ログ** セクションをクリア、または結果をエクスポートしてファイルに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-400">You can clear the **Log** section, or you can export the results and save them to a file.</span></span> <span data-ttu-id="de7c2-401">エクスポート ログの結果が公式互換性テストでどう使用されるかについては、このトピックの後半で「デバイス メーカーへの指示」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-401">For information about how the exported log results can be used for official compatibility testing, see the "Instructions for device manufacturers" section later in this topic.</span></span>

<span data-ttu-id="de7c2-402">自己テストを中止するには、[赤い四角形] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-402">To stop a self-test, click the red square.</span></span> <span data-ttu-id="de7c2-403">たとえば、デバイスが応答しない場合、自己テストを中止する必要が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-403">For example, you might have to stop a self-test if the device becomes non-responsive.</span></span> <span data-ttu-id="de7c2-404">赤い四角は、セルフテストが進行中の場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-404">The red square can be used only when a self-test is in progress.</span></span>

### <a name="device-specific-settings-to-be-aware-of"></a><span data-ttu-id="de7c2-405">デバイス固有の設定</span><span class="sxs-lookup"><span data-stu-id="de7c2-405">Device-specific settings to be aware of</span></span>

<span data-ttu-id="de7c2-406">このセクションでは、完了するために必要な設定が記載されています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-406">This section lists settings that you might require some help to complete.</span></span>

#### <a name="line-display-gt-settings-tab"></a><span data-ttu-id="de7c2-407">ライン ディスプレイ &gt;設定タブ</span><span class="sxs-lookup"><span data-stu-id="de7c2-407">Line display &gt; Settings tab</span></span>

<span data-ttu-id="de7c2-408">自由書式のフィールドに入力されている値を表示するには、**ロックとクレーム** をクリックしてデバイスを要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-408">To view the values that are entered in a free text field, click **Lock and claim** to claim the device.</span></span>

1. <span data-ttu-id="de7c2-409">**テキストの表示**をクリックし、デバイスに送信されたテキストを表示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-409">Click **Display text**, and view the text that was sent to the device.</span></span>
2. <span data-ttu-id="de7c2-410">ライン ディスプレイからテキストを消去するには、**テキストをクリア**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-410">Click **Clear text** to clear the text from the line display.</span></span>
3. <span data-ttu-id="de7c2-411">**リリース**をクリックしてライン ディスプレイをリリースし、他のプロセスに使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-411">Click **Release** to release the line display, so that it can be used for other processes.</span></span>

#### <a name="line-display-gt-advanced-tab-settings"></a><span data-ttu-id="de7c2-412">ライン ディスプレイ &gt;詳細タブ設定</span><span class="sxs-lookup"><span data-stu-id="de7c2-412">Line display &gt; Advanced tab settings</span></span>

- <span data-ttu-id="de7c2-413">**バイナリ変換** - ライン ディスプレイによって、テキストをバイナリ形式に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-413">**Binary conversion** – Some line displays require that text be converted into binary format.</span></span> <span data-ttu-id="de7c2-414">この変換が必要かどうかを確認するのには、デバイスのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-414">To determine whether this conversion is required, see the device’s documentation.</span></span>
- <span data-ttu-id="de7c2-415">**文字セット** - デバイスに送信される文字のコード ページ。</span><span class="sxs-lookup"><span data-stu-id="de7c2-415">**Character set** – The code page for the characters that are sent to the device.</span></span> <span data-ttu-id="de7c2-416">特定のコード ページの識別子については、<https://msdn.microsoft.com/en-us/library/windows/desktop/dd317756(v=vs.85).aspx> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-416">For the identifiers of specific code pages, see <https://msdn.microsoft.com/en-us/library/windows/desktop/dd317756(v=vs.85).aspx>.</span></span>

#### <a name="msr"></a><span data-ttu-id="de7c2-417">MSR</span><span class="sxs-lookup"><span data-stu-id="de7c2-417">MSR</span></span>

- <span data-ttu-id="de7c2-418">**MSR を開いて要求** – MSR からデータを受信するように POS シミュレーターを準備します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-418">**Open and claim MSR** – Prepare the POS simulator to receive data from the MSR.</span></span>
- <span data-ttu-id="de7c2-419">**MSR をリリースして閉じる** – テストが完了したときに、MSR デバイスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-419">**Release and close MSR** – Close the MSR device when testing is completed.</span></span>
- <span data-ttu-id="de7c2-420">**カード情報** - MSR デバイスでスキャンしたカードからのデータ。</span><span class="sxs-lookup"><span data-stu-id="de7c2-420">**Card info** – Data from the card that was scanned on the MSR device.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="de7c2-421">実際のクレジット カードは、デバイス テストに使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-421">Actual credit cards should never be used for device testing.</span></span> <span data-ttu-id="de7c2-422">期限切れのクレジットカードであっても、テストには使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-422">Even expired credit cards should not be used for testing.</span></span>

#### <a name="pin-pad"></a><span data-ttu-id="de7c2-423">PIN パッド</span><span class="sxs-lookup"><span data-stu-id="de7c2-423">PIN pad</span></span>

<span data-ttu-id="de7c2-424">**両方のタブに表示される設定**</span><span class="sxs-lookup"><span data-stu-id="de7c2-424">**Settings that appear on both tabs**</span></span>

- <span data-ttu-id="de7c2-425">**ロック** – PIN パッド デバイスをロックして、POS シミュレーターでのみ使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-425">**Lock** – Lock the PIN pad device so that it can be used only with the POS simulator.</span></span>
- <span data-ttu-id="de7c2-426">**エントリを取得** – PIN データを受信する POS シミュレーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-426">**Get entry** – Enable the POS simulator to receive PIN data.</span></span>
- <span data-ttu-id="de7c2-427">**操作のキャンセル** - PIN パッドに送信された要求をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-427">**Cancel operation** – Cancel the request that was sent to the PIN pad.</span></span>
- <span data-ttu-id="de7c2-428">**リリース** – PIN パッド デバイスをリリースします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-428">**Release** – Release the PIN pad device.</span></span>

<span data-ttu-id="de7c2-429">**設定タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-429">**Settings tab**</span></span>

- <span data-ttu-id="de7c2-430">**金額** - 顧客の受入のために PIN パッド デバイスに送信する金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-430">**Amount** – The amount to send to the PIN pad device for customer acceptance.</span></span>
- <span data-ttu-id="de7c2-431">**勘定番号** - 必要な場合は、感情番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-431">**Account number** – Specify the account number, if it's required.</span></span>
- <span data-ttu-id="de7c2-432">**暗号化された PIN** - デバイスから受信した暗号化された PIN。</span><span class="sxs-lookup"><span data-stu-id="de7c2-432">**Encrypted PIN** – The encrypted PIN that is received from the device.</span></span>
- <span data-ttu-id="de7c2-433">**追加のセキュリティ データ** - 暗号化された PIN に使用される暗号を指定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-433">**Additional security data** – Specify the cryptography that is used for the encrypted PIN.</span></span>

<span data-ttu-id="de7c2-434">**詳細タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-434">**Advanced tab**</span></span>

- <span data-ttu-id="de7c2-435">**タイムアウト** – デバイスからの応答に待機する秒数を指定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-435">**Timeout** – Specify the number of seconds to wait for a response from the device.</span></span>
- <span data-ttu-id="de7c2-436">**排他** - 有効にするには、PIN パッド デバイスが要求されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-436">**Exclusive** – Require that the PIN pad device be claimed before it can be enabled.</span></span>
- <span data-ttu-id="de7c2-437">**上書き** – デバイスが応答していない場合に、デバイスに送信された前のコマンドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-437">**Override** – Override previous commands that were sent to device when the device isn't responding.</span></span>

#### <a name="scale"></a><span data-ttu-id="de7c2-438">スケール</span><span class="sxs-lookup"><span data-stu-id="de7c2-438">Scale</span></span>

- <span data-ttu-id="de7c2-439">**タイムアウト** – タイムアウトの間隔。</span><span class="sxs-lookup"><span data-stu-id="de7c2-439">**Timeout** – The time-out interval.</span></span> <span data-ttu-id="de7c2-440">重量が読み取られる前に、スケールに製品を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-440">Product should be put on the scale before the weight is read.</span></span> <span data-ttu-id="de7c2-441">スケールが指定した期間内に応答されない場合、要求がキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-441">If the scale doesn't respond within the specified interval, the request is canceled.</span></span>

#### <a name="signature-capture"></a><span data-ttu-id="de7c2-442">署名キャプチャ</span><span class="sxs-lookup"><span data-stu-id="de7c2-442">Signature capture</span></span>

<span data-ttu-id="de7c2-443">**設定タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-443">**Settings tab**</span></span>

- <span data-ttu-id="de7c2-444">**フォーム名** – 署名要求の送信時に、一部の署名キャプチャ デバイスではフォーム名が必要です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-444">**Form name** – Some signature capture devices require a form name when the signature request is sent.</span></span>
- <span data-ttu-id="de7c2-445">**(16 進数での) 署名** – デバイスから受信した署名のデータの 16 進数の値。</span><span class="sxs-lookup"><span data-stu-id="de7c2-445">**Signature (in HEX)** – The hex value for the signature data that is received from the device.</span></span>
- <span data-ttu-id="de7c2-446">**表示する署名** – デバイスから受信した署名のイメージ。</span><span class="sxs-lookup"><span data-stu-id="de7c2-446">**Rendered signature** – The image of the signature that is received from the device.</span></span>

<span data-ttu-id="de7c2-447">**詳細タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-447">**Advanced tab**</span></span>

- <span data-ttu-id="de7c2-448">**タイムアウト** – タイムアウトの間隔。</span><span class="sxs-lookup"><span data-stu-id="de7c2-448">**Timeout** – The time-out interval.</span></span> <span data-ttu-id="de7c2-449">署名キャプチャ デバイスが指定した期間内に応答されない場合、要求がキャンセルされます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-449">If the signature capture device doesn't respond within the specified interval, the request is canceled.</span></span>
- <span data-ttu-id="de7c2-450">**排他** - 有効にするには、PIN パッド デバイスが要求されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-450">**Exclusive** – Require that the PIN pad device be claimed before it can be enabled.</span></span>
- <span data-ttu-id="de7c2-451">**上書き** – デバイスが応答していない場合に、デバイスに送信された前のコマンドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-451">**Override** – Override previous commands that were sent to device when the device isn't responding.</span></span>
- <span data-ttu-id="de7c2-452">**ロック** – デバイスをロックして、POS シミュレーターで使用するようにデバイスを要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-452">**Lock** – Lock the device and claim it for use by the POS simulator.</span></span>
- <span data-ttu-id="de7c2-453">**エントリを取得** – デバイスから署名を要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-453">**Get entry** – Request the signature from the device.</span></span>
- <span data-ttu-id="de7c2-454">**操作のキャンセル** - 署名要求をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-454">**Cancel operation** – Cancel the signature request.</span></span>
- <span data-ttu-id="de7c2-455">**リリース** – 他のプロセスで使用できるようにデバイスをリリースします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-455">**Release** – Release the device so that it can be used by other processes.</span></span>

#### <a name="bar-code-scanner"></a><span data-ttu-id="de7c2-456">バーコード スキャナー</span><span class="sxs-lookup"><span data-stu-id="de7c2-456">Bar code scanner</span></span>

- <span data-ttu-id="de7c2-457">**スキャナーを開いて要求** – スキャナーを開いて要求します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-457">**Open and claim scanner** – Open and claim the scanner.</span></span> <span data-ttu-id="de7c2-458">POS シミュレーターは、この操作が正常に完了した後にスキャン イベントを受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-458">The POS simulator can receive scan events after this operation is completed successfully.</span></span>
- <span data-ttu-id="de7c2-459">**スキャナーをリリースして閉じる** – スキャナーを他のプロセスで使用可能にします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-459">**Release and close the scanner** – Make the scanner available for other processes.</span></span>
- <span data-ttu-id="de7c2-460">**スキャンした情報** – バーコード スキャナーから受信したデータ。</span><span class="sxs-lookup"><span data-stu-id="de7c2-460">**Scanned information** – The data that was received from the bar code scanner.</span></span>

#### <a name="payment-terminal"></a><span data-ttu-id="de7c2-461">支払ターミナル</span><span class="sxs-lookup"><span data-stu-id="de7c2-461">Payment terminal</span></span>

<span data-ttu-id="de7c2-462">**それぞれのタブに表示される設定**</span><span class="sxs-lookup"><span data-stu-id="de7c2-462">**Settings that appear on every tab**</span></span>

- <span data-ttu-id="de7c2-463">**操作を選択** – デバイス上で実行する特定の操作を選択します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-463">**Select an operation** – Select a specific operation to perform on the device.</span></span> <span data-ttu-id="de7c2-464">オプションには、**すべて**、**カードで支払う**、**カードへの返金**、および **支払の無効化** があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-464">Options include **All**, **Pay by card**, **Refund by card**, and **Void payment**.</span></span>
- <span data-ttu-id="de7c2-465">**ロックと要求** – POS シミュレーターで使えるようにデバイスを準備します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-465">**Lock and claim** – Prepare the device so that it can be used by the POS simulator.</span></span>
- <span data-ttu-id="de7c2-466">**明細行品目の更新** – 指定した明細行品目の詳細をデバイスに送信してください。</span><span class="sxs-lookup"><span data-stu-id="de7c2-466">**Update line items** – Send specified line item details to the device.</span></span>
- <span data-ttu-id="de7c2-467">**支払の承認** - 支払の承認を要求する支払コネクタに指示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-467">**Authorize payment** – Instruct the payment connector to request payment authorization.</span></span>
- <span data-ttu-id="de7c2-468">**支払のキャプチャ** - 以前の承認をキャプチャするよう支払コネクタに指示します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-468">**Capture payment** – Instruct the payment connector to capture the previous authorization.</span></span>
- <span data-ttu-id="de7c2-469">**リリース** – デバイスをリリースします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-469">**Release** – Release the device.</span></span>

<span data-ttu-id="de7c2-470">**設定タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-470">**Settings tab**</span></span>

<span data-ttu-id="de7c2-471">**設定** タブには、支払の承認が要求されたときにデバイスに送信されるプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-471">The **Settings** tab contains properties that are sent to the device when a payment authorization is requested.</span></span>

- <span data-ttu-id="de7c2-472">**請求書番号** – POS で生成される請求書番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-472">**Invoice number** – Specify the invoice number that is generated at the POS.</span></span>
- <span data-ttu-id="de7c2-473">**テスト モード** – テスト トランザクションが実行されていることを示す値。</span><span class="sxs-lookup"><span data-stu-id="de7c2-473">**Test mode** – A value that indicates that a test transaction is being performed.</span></span>
- <span data-ttu-id="de7c2-474">**支払コネクタ** – 使用する支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="de7c2-474">**Payment connector** – The name of the payment connector to use.</span></span>
- <span data-ttu-id="de7c2-475">**借方キャッシュ バック限度** - 借方トランザクションが実行されるときにデバイス上で要求できるキャッシュ バックの最大金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-475">**Debit cashback limit** – The maximum amount of cash back that can be requested on the device when a debit transaction is performed.</span></span>
- <span data-ttu-id="de7c2-476">**ロケール** – 使用されるロケール。</span><span class="sxs-lookup"><span data-stu-id="de7c2-476">**Locale** – The locale that is used.</span></span> <span data-ttu-id="de7c2-477">ロケールは、POS シミュレーター用の構成ファイルで定義されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-477">Locales are defined in the configuration file for the POS simulator.</span></span>
- <span data-ttu-id="de7c2-478">**最大許容金額** – 指定されたトランザクションで処理できる最大金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-478">**Maximum amount allowed** – The maximum amount that can be processed for a given transaction.</span></span>
- <span data-ttu-id="de7c2-479">**最小許容金額** – 指定されたトランザクションで処理できる最小金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-479">**Minimum amount allowed** – The minimum amount that can be processed for a given transaction.</span></span>
- <span data-ttu-id="de7c2-480">**署名キャプチャの最小量** – 顧客が署名を提供するように促される最低額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-480">**Signature capture minimum amount** – The lowest amount that the customer is prompted to provide a signature for.</span></span>
- <span data-ttu-id="de7c2-481">**ターミナル ID** – プロセッサが提供したトランザクション プロパティに含まれるターミナル ID。</span><span class="sxs-lookup"><span data-stu-id="de7c2-481">**Terminal ID** – The terminal ID that is included in the transaction properties that the processor provided.</span></span>

<span data-ttu-id="de7c2-482">**行タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-482">**Lines tab**</span></span>

<span data-ttu-id="de7c2-483">**明細行** タブには、ライン ディスプレイとして使用されている場合に、デバイスに送信できるデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-483">The **Lines** tab contains data that can be sent to the device when it's used as a line display.</span></span>

- <span data-ttu-id="de7c2-484">**説明** - デバイスに表示されるトランザクション明細行の製品説明。</span><span class="sxs-lookup"><span data-stu-id="de7c2-484">**Description** – The product description for the transaction line to show on the device.</span></span>
- <span data-ttu-id="de7c2-485">**割引** - トランザクション明細行に適用される割引金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-485">**Discount** – The discount amount that is applied to the transaction line.</span></span>
- <span data-ttu-id="de7c2-486">**拡張された税込明細行** - 製品明細行の金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-486">**Extended line with tax** – The product line amount.</span></span> <span data-ttu-id="de7c2-487">この金額には税金が含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-487">This amount includes tax.</span></span>
- <span data-ttu-id="de7c2-488">**行項目 ID** – トランザクション明細行の製品 ID。</span><span class="sxs-lookup"><span data-stu-id="de7c2-488">**Line item ID** – The product ID for the transaction line.</span></span>
- <span data-ttu-id="de7c2-489">**数量** – トランザクション明細行の数量。</span><span class="sxs-lookup"><span data-stu-id="de7c2-489">**Quantity** – The quantity for the transaction line.</span></span>
- <span data-ttu-id="de7c2-490">**最小在庫管理単位** – デバイスに表示する測定単位。</span><span class="sxs-lookup"><span data-stu-id="de7c2-490">**Stock keeping unit** – The unit of measure to show on the device.</span></span>
- <span data-ttu-id="de7c2-491">**単価** – トランザクション明細行の販売価格。</span><span class="sxs-lookup"><span data-stu-id="de7c2-491">**Unit price** – The selling price for the transaction line.</span></span>
- <span data-ttu-id="de7c2-492">**統一商品コード** – トランザクション明細行のためにスキャンされたバーコード。</span><span class="sxs-lookup"><span data-stu-id="de7c2-492">**Universal product code** – The bar code that was scanned for the transaction line.</span></span>
- <span data-ttu-id="de7c2-493">**無効** – トランザクションからトランザクション行が削除されたことを示す値。</span><span class="sxs-lookup"><span data-stu-id="de7c2-493">**Is voided** – A value that indicates that the transaction line has been voided from the transaction.</span></span>

<span data-ttu-id="de7c2-494">**詳細タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-494">**Advanced tab**</span></span>

<span data-ttu-id="de7c2-495">**詳細** タブには、デバイスに表示できる小計の情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-495">The **Advanced** tab contains subtotal information that can be shown on the device.</span></span>

- <span data-ttu-id="de7c2-496">**割引金額** - トランザクション上の割引の合計金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-496">**Discount amount** – The total amount for discounts on the transaction.</span></span>
- <span data-ttu-id="de7c2-497">**小計金額** – トランザクションの小計。</span><span class="sxs-lookup"><span data-stu-id="de7c2-497">**Subtotal amount** – The subtotal for the transaction.</span></span> <span data-ttu-id="de7c2-498">この金額には、税金が含まれていません。</span><span class="sxs-lookup"><span data-stu-id="de7c2-498">This amount doesn't include tax.</span></span>
- <span data-ttu-id="de7c2-499">**税額** – トランザクションの税額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-499">**Tax amount** – The tax amount for the transaction.</span></span>
- <span data-ttu-id="de7c2-500">**合計金額** – 予定されている合計金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-500">**Total amount** – The total amount that is due.</span></span> <span data-ttu-id="de7c2-501">この金額には税金と割引が含まれます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-501">This amount includes tax and discounts.</span></span>
- <span data-ttu-id="de7c2-502">**通貨** - トランザクションに使用される通貨。</span><span class="sxs-lookup"><span data-stu-id="de7c2-502">**Currency** – The currency that is used for the transaction.</span></span>

<span data-ttu-id="de7c2-503">**支払情報タブ**</span><span class="sxs-lookup"><span data-stu-id="de7c2-503">**Payment info tab**</span></span>

<span data-ttu-id="de7c2-504">**支払情報** タブには、承認が処理された後に、支払コネクタから受信したデータが含まれています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-504">The **Payment info** tab contains data that is received from the payment connector after an authorization has been processed.</span></span>

- <span data-ttu-id="de7c2-505">**承認** – 承認要求が承認されているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="de7c2-505">**Is approved** – A value that indicates whether the authorization request is approved.</span></span>
- <span data-ttu-id="de7c2-506">**マスクされたカード番号** - デバイスによって提供されるマスクされたカード番号です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-506">**Card number masked** – The masked card number that is provided by the device.</span></span> <span data-ttu-id="de7c2-507">通常、カード番号の最後の 4 桁のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-507">Typically, only the last four digits of the card number are shown.</span></span>
- <span data-ttu-id="de7c2-508">**カード タイプ** - トランザクションに使用されるカードの問題です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-508">**Card type** – The issue for the card that is used in the transaction.</span></span>
- <span data-ttu-id="de7c2-509">**承認済金額** - カードの支払に対して承認されている金額。</span><span class="sxs-lookup"><span data-stu-id="de7c2-509">**Approved amount** – The amount that is authorized for the card payment.</span></span>
- <span data-ttu-id="de7c2-510">**支払 SDK データ** – 認証コードや支払プロセッサが提供するその他のデータなど、支払ソフトウェア開発キット (SDK) が提供する追加データ。</span><span class="sxs-lookup"><span data-stu-id="de7c2-510">**Payment SDK data** – Additional data that the payment software development kit (SDK) can provide, such as the authorization code and other data that the payment processor provides.</span></span>
- <span data-ttu-id="de7c2-511">**署名データ** – デバイスによって提供される 16 進署名データ。</span><span class="sxs-lookup"><span data-stu-id="de7c2-511">**Signature data** – Hexadecimal signature data that is provided by the device.</span></span>
- <span data-ttu-id="de7c2-512">**支払エラー** – 認証要求中に発生したエラー。</span><span class="sxs-lookup"><span data-stu-id="de7c2-512">**Payment errors** – Any errors that occurred during the authorization request.</span></span>

## <a name="instructions-for-device-manufacturers"></a><span data-ttu-id="de7c2-513">デバイス メーカーに対する指示</span><span class="sxs-lookup"><span data-stu-id="de7c2-513">Instructions for device manufacturers</span></span>

<span data-ttu-id="de7c2-514">Retail との互換性を一覧表示できるようにデバイスを送信するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-514">To submit a device so that it can be listed for compatibility with Retail,  follow these steps.</span></span>

1. <span data-ttu-id="de7c2-515">**設定**タブで、要求されたすべての連絡先情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-515">On the **Settings** tab, specify all contact information that is requested.</span></span> <span data-ttu-id="de7c2-516">全フィールドが必須です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-516">All fields are required.</span></span> <span data-ttu-id="de7c2-517">個人の連絡先情報は、Microsoft の社内用です。</span><span class="sxs-lookup"><span data-stu-id="de7c2-517">The personal contact information is for Microsoft internal use.</span></span> <span data-ttu-id="de7c2-518">互換性のあると提出されたデバイスに問題がある場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-518">It will be used only if there are issues with devices that have been submitted as compatible.</span></span>
2. <span data-ttu-id="de7c2-519">各デバイス用に、**デバイス**タブで、デバイスを設定し、すべてのフィールドの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-519">For each device, on the **Devices** tab, set up the device, and provide values for all fields.</span></span> <span data-ttu-id="de7c2-520">各順列で、新しいデバイスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-520">For each permutation, a new device must be specified.</span></span> <span data-ttu-id="de7c2-521">たとえば、USB およびシリアル用に、指定されたデバイス モードがテストされる場合、2 つの互換性レポートが送信される必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-521">For example, if a given device mode is tested for USB and serial, two compatibility reports must be submitted.</span></span> <span data-ttu-id="de7c2-522">1 つのデバイスから次のデバイスへの差異を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-522">Any variance from one device to the next should be indicated.</span></span> <span data-ttu-id="de7c2-523">次に、互換性のためにデバイスが記載されている場合、そのデバイスを実装するユーザーに非常に限定された情報を提供できます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-523">Then, when devices are listed for compatibility, very specific information can be provided to people who implement the devices.</span></span> <span data-ttu-id="de7c2-524">デバイスの互換性に関する情報が多く提供されるほど、実装の成功率が高くなり、サポートの問題が少なくなります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-524">The more information that can be provided about device compatibility, the higher the success rate for implementations and the fewer support issues will be raised.</span></span>
3. <span data-ttu-id="de7c2-525">デバイスおよび設定に必要な情報を入力した後に、デバイスをテストします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-525">After you've entered the required information for devices and settings, test the device.</span></span>

    1. <span data-ttu-id="de7c2-526">テストしているデバイスのログを消去します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-526">Clear the log for the device that you're testing.</span></span>
    2. <span data-ttu-id="de7c2-527">**自己テスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-527">Click **Self-test**.</span></span>
    3. <span data-ttu-id="de7c2-528">テストが正常に完了したときは、テストの結果をエクスポートして保存します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-528">When a test has been completed successfully, export the test results, and save them.</span></span> <span data-ttu-id="de7c2-529">ファイルに、テストを容易に識別する名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-529">Give the file a name that will make the test easy to identify.</span></span> <span data-ttu-id="de7c2-530">ファイル名として、メーカーの名前とデバイス モデルの省略形を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="de7c2-530">We suggest that you use an abbreviated form of the manufacturer's name and the device model as the file name.</span></span>

<span data-ttu-id="de7c2-531">次の例は、エクスポートされたファイルに含まれるデータを示しています。</span><span class="sxs-lookup"><span data-stu-id="de7c2-531">The following example shows the data that is included in the exported file.</span></span>

```
<?xml version="1.0" encoding="utf-8"?>  
<Report xmlns:i="http://www.w3.org/2001/XMLSchema-instance" xmlns="http://schemas.datacontract.org/2004/07/Microsoft.Dynamics.Commerce.VirtualPeripherals.Modules">  
   <CreationDateTime>05/27/2017 19:34:50</CreationDateTime>  
   <ManufacturerInfo>  
    <ManufacturerName>Contoso </ManufacturerName>  
    <ManufacturerWebsite>http://www.contoso.com</ManufacturerWebsite>  
    <SupportEmail>support@contoso.com</SupportEmail>  
    <SupportTelephoneNumber>555-555-5555</SupportTelephoneNumber>  
    <SupportWebsite>http://www.contoso.com</SupportWebsite>  
    <TechnicalContactEmail>karen@contoso.com</TechnicalContactEmail>  
    <TechnicalContactName>Karen Berg</TechnicalContactName>  
    <TechnicalContactPhone>555-555-5555</TechnicalContactPhone>  
  </ManufacturerInfo>  
  <DeviceInfo i:type="OposDevice">  
   <DeviceDriverName>MockOPOSDrawer1</DeviceDriverName>  
   <DeviceModel>Model1</DeviceModel>  
   <DriverVersion>V2</DriverVersion>  
   <FirmwareVersion>V1</FirmwareVersion>  
  <HardwareType>OPOS</HardwareType>  
  <ConnectionType>USB</ConnectionType>  
  <DriverDownloadLink>htttp://model1.drivers.contoso.com</DriverDownloadLink>  
 <DeviceInfo i:type="OposDevice">
 <LogItems>  
  <LogMessage>  
     <LogType>Info</LogType>  
     <Message>The cash drawer is opened successfully.</Message>  
     <Timestamp>05/27/2017 19:48:14</Timestamp>  
  </LogMessage>  
  <LogMessage>  
     <LogType>Info</LogType>  
     <Message>The cash drawer open operation elapsed time: 00:00:00.053</Message>  
     <Timestamp>05/27/2017 19:48:14</Timestamp>  
  </LogMessage>  
  <LogMessage>  
      <LogType>Info</LogType>  
      <Message>The cash drawer status check operation is completed successfully.</Message>  
      <Timestamp>05/27/2017 19:48:14</Timestamp>  
   </LogMessage>  
   <LogMessage>  
      <LogType>Info</LogType>  
      <Message>The cash drawer status check operation elapsed time: 00:00:00.045</Message>  
      <Timestamp>05/27/2017 19:48:14</Timestamp>  
   </LogMessage>  
      <LogMessage>  
      <LogType>Info</LogType>  
      <Message>Test finished successfully.</Message>  
      <Timestamp>05/27/2017 19:48:14</Timestamp>  
    </LogMessage>  
  </LogItems>  
</Report>
```

<span data-ttu-id="de7c2-532">最終的には、レポート (連絡先の個人情報を除く) に含まれているデータがデバイス互換性 Web サイトに表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-532">Eventually, the data that is included in the report (except personal contact information) will be listed on a device compatibility website.</span></span> <span data-ttu-id="de7c2-533">顧客環境の管理に使用される設計および配置のツールでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-533">It will also be listed in design and deployment tools that are used to manage customer environments.</span></span>

<span data-ttu-id="de7c2-534">正常なログを、drpc@microsoft.com に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de7c2-534">Successful logs should be sent to drpc@microsoft.com.</span></span> <span data-ttu-id="de7c2-535">件名行に、メーカーの名前とデバイス モデルを含めます。</span><span class="sxs-lookup"><span data-stu-id="de7c2-535">Include the manufacturer’s name and the device model in the subject line.</span></span>

<span data-ttu-id="de7c2-536">互換性のテストを実行しているサポート、およびその他の照会については、drpc@microsoft.com に電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="de7c2-536">For support if you're performing compatibility tests, and for other inquiries, send an email to drpc@microsoft.com.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de7c2-537">追加リソース</span><span class="sxs-lookup"><span data-stu-id="de7c2-537">Additional resources</span></span>

[<span data-ttu-id="de7c2-538">小売周辺機器の概要</span><span class="sxs-lookup"><span data-stu-id="de7c2-538">Retail peripherals overview</span></span>](../retail-peripherals-overview.md)

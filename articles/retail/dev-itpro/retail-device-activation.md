---
title: 小売販売時点管理 (POS) デバイスのライセンス認証
description: この記事では、Retail Cloud POS および Retail Modern POS の新しいガイド付きデバイスの有効化について説明し、ユーザーが手動で登録およびデバイスID情報を入力しなくても簡単にデバイスをアクティブ化できるクライアントの簡略化について説明します。
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailSharedParameters, RetailDevice
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail, Core
ms.custom: 18341
ms.assetid: 3dc4c413-e341-4d01-bc49-dc24e35dd8a7
ms.search.region: Global
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 1131051c262c67e4bdcd83f5343170c16d160eab
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811130"
---
# <a name="retail-point-of-sale-pos-device-activation"></a><span data-ttu-id="682e2-103">小売販売時点管理 (POS) デバイスのライセンス認証</span><span class="sxs-lookup"><span data-stu-id="682e2-103">Retail point of sale (POS) device activation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="682e2-104">この記事では、Retail Cloud POS および Retail Modern POS の新しいガイド付きデバイスの有効化について説明し、ユーザーが手動で登録およびデバイスID情報を入力しなくても簡単にデバイスをアクティブ化できるクライアントの簡略化について説明します。</span><span class="sxs-lookup"><span data-stu-id="682e2-104">This article explains the new guided device activation for Retail Cloud POS and Retail Modern POS, and explains the client simplifications that help users easily activate devices without having to manually enter register and device ID information.</span></span> 

<a name="checklist-to-follow-before-activation"></a><span data-ttu-id="682e2-105">起動前のチェックリスト</span><span class="sxs-lookup"><span data-stu-id="682e2-105">Checklist to follow before activation</span></span>
-------------------------------------

1.  <span data-ttu-id="682e2-106">HQ で**有効化のためにデバイスを検証**チェックを完了し、デバイスが検証をパスしたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-106">Complete the **Validate devices for activation** check in HQ, and make sure that the device passes validation.</span></span>
2.  <span data-ttu-id="682e2-107">デバイスを有効化しているクライアント マシンで、Retail サーバー URL 正常性チェックにアクセスし、正常性チェックが承認されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-107">On the client machine where you're activating the device, access the Retail Server URL health check, and make sure that the health check is passed.</span></span> <span data-ttu-id="682e2-108">次の形式を使用します: https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping</span><span class="sxs-lookup"><span data-stu-id="682e2-108">Use the following format: https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping</span></span>
3.  <span data-ttu-id="682e2-109">作業者は、Microsoft Azure Active Directory (AAD) アカウント (**外部 ID 下**) にマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-109">The worker must be mapped to a Microsoft Azure Active Directory (AAD) account (under **External identity**).</span></span>
4.  <span data-ttu-id="682e2-110">マッピングする AAD アカウントは、同じテナントに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-110">The AAD account to map must belong to the same tenant.</span></span>
5.  <span data-ttu-id="682e2-111">作業者を AAD アカウントにマップするには、Microsoft Dynamics Lifecycle Services (LCS) の管理者アカウントを使用して HQ に サインインします。</span><span class="sxs-lookup"><span data-stu-id="682e2-111">To map the worker to the AAD account, sign in to HQ by using the Admin account for Microsoft Dynamics Lifecycle Services (LCS).</span></span>
6.  <span data-ttu-id="682e2-112">作業者がマネージャー ロール内のユーザーとして設定されていることを確認します (検証でチェックされます)。</span><span class="sxs-lookup"><span data-stu-id="682e2-112">Make sure that the worker is set up as a user in the Manager role (checked by validation).</span></span>
7.  <span data-ttu-id="682e2-113">チャネルが公開されていることを確認します (検証でチェックされます)。</span><span class="sxs-lookup"><span data-stu-id="682e2-113">Make sure that the channel is published (checked by validation).</span></span>
8.  <span data-ttu-id="682e2-114">チャネル データベースに本社から同期したデータが含まれており、ダウンロード ジョブが実行されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-114">Make sure that the channel database has the synced data from HQ, and that download jobs are running.</span></span> <span data-ttu-id="682e2-115">これを確認するには、ストアのチャネル データベースで次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="682e2-115">To check this, run the following command in the channel database for the store.</span></span>

        select * from crt.STORAGELOOKUPVIEW

    <span data-ttu-id="682e2-116">データが返され、結果が空ではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-116">Make sure that data is returned, and that the result isn't empty.</span></span>

9.  <span data-ttu-id="682e2-117">**登録** (検証によって確認) でハードウェア プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="682e2-117">Set up the hardware profile under **Register** (checked by validation).</span></span>
10. <span data-ttu-id="682e2-118">レジスターおよび店舗に画面レイアウトがあることを確認します (検証でチェックされます)。</span><span class="sxs-lookup"><span data-stu-id="682e2-118">Make sure that the register and store have a screen layout (checked by validation).</span></span>
11. <span data-ttu-id="682e2-119">基本住所が法人に対して設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-119">Make sure that a primary address is set up for the legal entity.</span></span>
12. <span data-ttu-id="682e2-120">言語が Commerce Data Exchange: Real-time Service ユーザー プロファイル (デモ データでの JBB) に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-120">Make sure that the language is set up for the Commerce Data Exchange: Real-time Service user profile (JBB in the demo data).</span></span>
13. <span data-ttu-id="682e2-121">リアルタイム サービス プロファイルに適切なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-121">Make sure that the Real-time Service profile has the correct access.</span></span>
14. <span data-ttu-id="682e2-122">電子決済 (EFT) のコンフィギュレーションの値があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="682e2-122">Make sure that the electronic funds transfer (EFT) configuration value is present.</span></span>

## <a name="activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation"></a><span data-ttu-id="682e2-123">ガイド付きの有効化を使用して、Modern POS または Cloud POS デバイスを有効化</span><span class="sxs-lookup"><span data-stu-id="682e2-123">Activate a Modern POS or Cloud POS device by using guided activation</span></span>
1.  <span data-ttu-id="682e2-124">Modern POS またはクラウド POS 用の初期デバイスの有効化ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="682e2-124">Open the initial device activation page for Modern POS or Cloud POS.</span></span> <span data-ttu-id="682e2-125">サインインするように求められます。</span><span class="sxs-lookup"><span data-stu-id="682e2-125">You're prompted to sign in.</span></span>
2.  <span data-ttu-id="682e2-126">**始める前に**ページで、指示に従い、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="682e2-126">On the **Before you start** page, follow the instructions, and then click **Next**.</span></span>

    ![POS ウィザード (ページを開始する前に)](./media/p24.png)

3.  <span data-ttu-id="682e2-128">Cloud POS または Modern POS を起動します。</span><span class="sxs-lookup"><span data-stu-id="682e2-128">Start Cloud POS or Modern POS.</span></span>
4.  <span data-ttu-id="682e2-129">AAD 資格情報を使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="682e2-129">Use your AAD credentials to sign in.</span></span> <span data-ttu-id="682e2-130">AAD アカウントが既にマッピングされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-130">The AAD account must already be mapped.</span></span> <span data-ttu-id="682e2-131">手順については、 [Configure, install, and activate Retail Modern POS (MPOS) の構成、インストール、およびアクティベーション](../retail-modern-pos-device-activation.md).を参照してください。</span><span class="sxs-lookup"><span data-stu-id="682e2-131">For instructions, see [Configure, install, and activate Retail Modern POS (MPOS)](../retail-modern-pos-device-activation.md).</span></span> <span data-ttu-id="682e2-132">クラウド POS で、サーバー URL は、アドレス バーに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="682e2-132">For Cloud POS, the server URL is automatically entered in the address bar.</span></span> <span data-ttu-id="682e2-133">Modern POS で、サーバー URL をコピーし貼り付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-133">For Modern POS, you must copy and paste the server URL.</span></span>

    <span data-ttu-id="682e2-134">[![POS ウィザード、サーバー URL ページの追加](./media/p18.png)](./media/p18.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-134">[![POS Wizard, add server URL page](./media/p18.png)](./media/p18.png)</span></span>

5.  <span data-ttu-id="682e2-135">店舗のリストを入力するには、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="682e2-135">Click **Next** to populate the list of stores.</span></span>
6.  <span data-ttu-id="682e2-136">一覧で適切な店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="682e2-136">Select the correct store in the list.</span></span>

    <span data-ttu-id="682e2-137">[![POS ウィザード、店舗ページの選択](./media/p20.png)](./media/p20.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-137">[![POS Wizard, select the store page](./media/p20.png)](./media/p20.png)</span></span>

7.  <span data-ttu-id="682e2-138">適切なレジスターとデバイスを選択します。</span><span class="sxs-lookup"><span data-stu-id="682e2-138">Select the correct register and device.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="682e2-139">このデバイスは **保留中**、**非有効化**、または **有効化** とすることができます。</span><span class="sxs-lookup"><span data-stu-id="682e2-139">The device can be **Pending**, **De-activated**, or **Activated**.</span></span> <span data-ttu-id="682e2-140">または、Retail HQ **デバイスをストアからレジスターに関連付ける**設定を有効にする場合は、関連付けられているデバイスを持たないレジスターの一覧を表示する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-140">Alternatively, if you turned on the Retail HQ **Allow devices to be associated to registers from store** setting, you might see a list of registers that have no device associated with them.</span></span> 

    <span data-ttu-id="682e2-141">[![POS ウィザード、レジスターおよびデバイス ページの選択](./media/p22.png)](./media/p22.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-141">[![POS Wizard, select register and device page](./media/p22.png)](./media/p22.png)</span></span>

8.  <span data-ttu-id="682e2-142">**有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="682e2-142">Click **Activate**.</span></span> <span data-ttu-id="682e2-143">デバイスを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-143">The device should be activated.</span></span> 

    <span data-ttu-id="682e2-144">[![POS ウィザード、有効化されたデバイスのページ](./media/p23.png)](./media/p23.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-144">[![POS Wizard, device activated page](./media/p23.png)](./media/p23.png)</span></span>

## <a name="create-a-device-id-from-modern-pos-and-cloud-pos"></a><span data-ttu-id="682e2-145">モダン POS とクラウド POS からデバイス ID を作成する</span><span class="sxs-lookup"><span data-stu-id="682e2-145">Create a device ID from Modern POS and Cloud POS</span></span>
<span data-ttu-id="682e2-146">Modern POS または Cloud POS からデバイスを作成する (すなわち、自動的にデバイス ID を生成する) 機能を追加しました。これにより、デバイスがまだマップされていないレジスターにデバイスを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="682e2-146">We have added features to create a device (that is, automatically generate a device ID) from Modern POS or Cloud POS, so that the device can be associated with a register that doesn't yet have devices mapped to it.</span></span> <span data-ttu-id="682e2-147">この機能は、HQ の設定を次のように設定した場合にのみ Modern POS で使用できます。</span><span class="sxs-lookup"><span data-stu-id="682e2-147">This functionality can be used in Modern POS only if you set the HQ settings as follows.</span></span>

1.  <span data-ttu-id="682e2-148">**Retail** &gt; **本社の設定** &gt; **パラメータ** &gt; **小売共有パラメーター** &gt; **一般**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="682e2-148">Go to **Retail** &gt; **Headquarters setup** &gt; **Parameters** &gt; **Retail shared parameters** &gt; **General**.</span></span>
2.  <span data-ttu-id="682e2-149">**デバイス** で **デバイスからの登録を許可する** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="682e2-149">Under **Devices,** set **Allow register association from device** to **Yes**.</span></span>
3.  <span data-ttu-id="682e2-150">Modern POS クライアントで、ガイド付きの有効化フローの**関連付けられているデバイスがありません**とリストされているレジスターを選択するときにデバイスを追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="682e2-150">In the Modern POS client, you can now add a device when you select a register that is listed as **No associated devices** in the guided activation flow.</span></span>
4.  <span data-ttu-id="682e2-151">レジスターを選択した後に、レジスター マッピングを持たないデバイスを選択するか、**またはデバイスを追加**リンクを使用するかのいずれかを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="682e2-151">After you select the register, you can either select a device that doesn't have register mapping or use the **Or, Add a Device** link.</span></span>
5.  <span data-ttu-id="682e2-152">**またはデバイスを追加**リンクをクリックし、新しいデバイス ID を入力するか、または**新しいデバイス ID を自動的に作成する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="682e2-152">Click the **Or, Add a Device** link, and then either enter the new device ID or select **Automatically create a new device ID for me**.</span></span>
6.  <span data-ttu-id="682e2-153">**有効化**をクリックして新しいデバイス ID を作成し、選択したレジスタへの関連付け、および有効化が完了します。</span><span class="sxs-lookup"><span data-stu-id="682e2-153">Click **Activate** to create a new device ID, associate it with the selected register, and complete the activation.</span></span>

## <a name="activate-the-device-for-modern-pos-by-using-a-configuration-file"></a><span data-ttu-id="682e2-154">コンフィギュレーション ファイルを使用して Modern POS のデバイスを有効化</span><span class="sxs-lookup"><span data-stu-id="682e2-154">Activate the device for Modern POS by using a configuration file</span></span>
<span data-ttu-id="682e2-155">IT プロフェッショナルは、Modern POS と一緒にダウンロードできるコンフィギュレーション ファイルを使用して、Modern POS のデバイス アクティベーションを簡単に設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="682e2-155">IT Pros can now easily configure device activation for Modern POS by using a configuration file that can be downloaded together with Modern POS.</span></span> <span data-ttu-id="682e2-156">このファイルは、適切な Modern POS デバイス (**Retail** &gt; **チャネル設定** &gt; **POS 設定** &gt; **デバイス**) の**デバイス**ページで利用できます。   </span><span class="sxs-lookup"><span data-stu-id="682e2-156">This file is now available on the **Devices** page for the appropriate Modern POS device (**Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**).</span></span> 

<span data-ttu-id="682e2-157">[![構成ファイルのダウンロード](./media/p16_11_16-1024x481.png)](./media/p16_11_16.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-157">[![Configuration file download](./media/p16_11_16-1024x481.png)](./media/p16_11_16.png)</span></span> 

<span data-ttu-id="682e2-158">コンフィギュレーション ファイルは、Retail サーバー URL、デバイス ID、およびデバイスの有効化のためのレジスター番号を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="682e2-158">The configuration file is used to enter the Retail Server URL, device ID, and register number for device activation.</span></span> <span data-ttu-id="682e2-159">インストール時に、インストーラーはファイルを選択し、デバイスのライセンチ値を設定します。</span><span class="sxs-lookup"><span data-stu-id="682e2-159">During installation, the installer selects this file and populates the values for device activation.</span></span> <span data-ttu-id="682e2-160">**重要:** ユーザーは Modern POS セルフサービス パッケージと同じフォルダにファイルを置いて、.exe ファイルを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="682e2-160">**Important:** The user must put the file in the same folder as the Modern POS self-service package and run the .exe file.</span></span> 

<span data-ttu-id="682e2-161">[![構成ファイル](./media/p17_11_16-1024x532.png)](./media/p17_11_16.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-161">[![Configuration file](./media/p17_11_16-1024x532.png)](./media/p17_11_16.png)</span></span> 

<span data-ttu-id="682e2-162">Modern POS は手動入力モードで起動し、Retail サーバー URL、デバイス ID、およびレジスター ID は、有効化のために事前設定されています。</span><span class="sxs-lookup"><span data-stu-id="682e2-162">Modern POS starts in Manual entry mode, and the Retail Server URL, device ID, and register ID are pre-populated for activation.</span></span>

## <a name="activate-the-device-for-cloud-pos-by-using-syntactic-sugar"></a><span data-ttu-id="682e2-163">糖衣構文を使用して Cloud POS のデバイスを有効化します。</span><span class="sxs-lookup"><span data-stu-id="682e2-163">Activate the device for Cloud POS by using syntactic sugar</span></span>
<span data-ttu-id="682e2-164">IT プロフェッショナルは、Cloud POS URL の一部として、デバイス ID とレジスター ID を提供することで、Cloud POS のデバイス アクティベーションを設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="682e2-164">IT Pros can now configure device activation for Cloud POS by providing the device ID and register ID as the part of the Cloud POS URL.</span></span> <span data-ttu-id="682e2-165">**デバイス** ページの **クラウド POS URL** フィールドにリンクがあります。</span><span class="sxs-lookup"><span data-stu-id="682e2-165">The link is available in the **Cloud POS URL** field on the **Devices** page.</span></span> <span data-ttu-id="682e2-166">(**小売** &gt; **チャネル設定** &gt; **POS 設定** &gt; **デバイス**)。</span><span class="sxs-lookup"><span data-stu-id="682e2-166">(**Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**).</span></span> 

<span data-ttu-id="682e2-167">クラウド POS は手動入力モードで起動し、Retail サーバー URL、デバイス ID、およびレジスター IDは、有効化のために事前設定されています。</span><span class="sxs-lookup"><span data-stu-id="682e2-167">Cloud POS starts in Manual entry mode, and the Retail Server URL, device ID, and register ID are pre-populated for activation.</span></span>

<span data-ttu-id="682e2-168">[![クラウド POS URL フィールド](./media/p15_11_16.png)](./media/p15_11_16.png)</span><span class="sxs-lookup"><span data-stu-id="682e2-168">[![Cloud POS URL field](./media/p15_11_16.png)](./media/p15_11_16.png)</span></span> 




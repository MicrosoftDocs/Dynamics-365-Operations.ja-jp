---
title: スウェーデンの制御ユニットとの POS の統合サンプル (レガシ)
description: このトピックは、スウェーデンの管理単位統合サンプルのビルドとインストールのガイドです。
author: EvgenyPopovMBS
manager: Annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Sweden
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-2-28
ms.dyn365.ops.version: 7.3.2
ms.openlocfilehash: f0f81d1b20ada852dbcee2f91bee30adb59a5629
ms.sourcegitcommit: 9c401a4adba260704b0b1cb9fe8e148bbb5afeed
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2020
ms.locfileid: "3120891"
---
# <a name="sample-for-pos-integration-with-control-units-for-sweden-legacy"></a><span data-ttu-id="90816-103">スウェーデンの制御ユニットとの POS の統合サンプル (レガシ)</span><span class="sxs-lookup"><span data-stu-id="90816-103">Sample for POS integration with control units for Sweden (legacy)</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="90816-104">このサンプル会計統合機能は、[会計統合フレームワーク](./fiscal-integration-for-retail-channel.md)を利用しておらず、今後の更新で非推奨になります。</span><span class="sxs-lookup"><span data-stu-id="90816-104">This sample fiscal integration functionality does not take advantage of the [fiscal integration framework](./fiscal-integration-for-retail-channel.md) and will be deprecated in later updates.</span></span> <span data-ttu-id="90816-105">代わりに、[スウェーデンのコントロール ユニット統合サンプル](./emea-swe-fi-sample.md#migrating-from-the-earlier-integration-sample)を使用してください。</span><span class="sxs-lookup"><span data-stu-id="90816-105">You should use the [Control unit integration sample for Sweden](./emea-swe-fi-sample.md#migrating-from-the-earlier-integration-sample) instead.</span></span>

<span data-ttu-id="90816-106">**サンプル コードの通知**</span><span class="sxs-lookup"><span data-stu-id="90816-106">**SAMPLE CODE NOTICE**</span></span>

<span data-ttu-id="90816-107">**このサンプルコードは現状のまま利用可能です。明示的または黙示的を問わず、特定の目的への適合性、正確性、完全性、結果、または商品性の条件に関して、Microsoft は一切保証しません。このサンプル コードの使用またはその結果に対するリスクは、すべてお客様が負うものとします。**</span><span class="sxs-lookup"><span data-stu-id="90816-107">**THIS SAMPLE CODE IS MADE AVAILABLE AS IS.  MICROSOFT MAKES NO WARRANTIES, WHETHER EXPRESS OR IMPLIED, OF FITNESS FOR A PARTICULAR PURPOSE, OF ACCURACY OR COMPLETENESS OF RESPONSES, OF RESULTS, OR CONDITIONS OF MERCHANTABILITY.  THE ENTIRE RISK OF THE USE OR THE RESULTS FROM THE USE OF THIS SAMPLE CODE REMAINS WITH THE USER.**</span></span>

<span data-ttu-id="90816-108">**技術サポートは提供されません。コード配布を許可する Microsoft の使用許諾契約がない限り、このコードを配布することはできません。**</span><span class="sxs-lookup"><span data-stu-id="90816-108">**NO TECHNICAL SUPPORT IS PROVIDED.  YOU MAY NOT DISTRIBUTE THIS CODE UNLESS YOU HAVE A LICENSE AGREEMENT WITH MICROSOFT THAT ALLOWS YOU TO DO SO.**</span></span>

<span data-ttu-id="90816-109">このサンプルでは、Retail Modern POS または クラウド POS を会計登録と統合する Dynamics 365 Commerce 拡張機能を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="90816-109">This sample shows how to create Dynamics 365 Commerce extensions to integrate Retail Modern POS or Cloud POS with a fiscal register.</span></span> <span data-ttu-id="90816-110">特に、このサンプルには Retail POS をスウェーデンの管理単位と統合するコードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="90816-110">Specifically, this sample includes the code for integrating Retail POS with control units for Sweden.</span></span> <span data-ttu-id="90816-111">コントロール ユニットは、POS がペアリングされているハードウェア ステーションに物理的に接続されていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="90816-111">It's assumed that a control unit is physically connected to a Hardware station that POS is paired with.</span></span> <span data-ttu-id="90816-112">たとえば、このサンプルでは Retail Innovation HTT AB の CleanCash® Type A 管理単位のアプリケーション プログラミング インターフェイス (API) を使用します。</span><span class="sxs-lookup"><span data-stu-id="90816-112">As an example, this sample uses the application programming interface (API) of the CleanCash® Type A control unit by Retail Innovation HTT AB.</span></span> <span data-ttu-id="90816-113">CleanCash® API のバージョン1.1.4 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="90816-113">Version 1.1.4 of the CleanCash® API is used.</span></span> <span data-ttu-id="90816-114">API およびドキュメントを含む統合パッケージについては、デバイスの製造元に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="90816-114">For the integration package that includes the API and documentation, contact the manufacturer of the device.</span></span>

<span data-ttu-id="90816-115">このサンプルは、Retail ソフトウェア開発キット (SDK) の一部です。</span><span class="sxs-lookup"><span data-stu-id="90816-115">This sample is a part of the Retail software development kit (SDK).</span></span> <span data-ttu-id="90816-116">小売 SDK のダウンロードと使用方法については、 [小売 ソフトウェアの開発キット(SDK) のアーキテクチャ](../dev-itpro/retail-sdk/retail-sdk-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90816-116">For information about how to install and use the Retail SDK, see the [Retail software development kit (SDK) architecture](../dev-itpro/retail-sdk/retail-sdk-overview.md).</span></span>

<span data-ttu-id="90816-117">このサンプルは、ハードウェア ステーション、Commerce Runtime (CRT)、および 販売時点管理 (POS) で構成されます。</span><span class="sxs-lookup"><span data-stu-id="90816-117">This sample consists of extensions for the Hardware station, commerce runtime (CRT), and point of sale (POS).</span></span> <span data-ttu-id="90816-118">このサンプルを実行するには、ハードウェア ステーション、CRT、および POS プロジェクトを変更して構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90816-118">To run this sample, you must modify and build the Hardware station, CRT, and POS projects.</span></span> <span data-ttu-id="90816-119">このトピックで説明されている変更を加えるために、修正していない Retail SDK を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="90816-119">We recommend that use you an unmodified Retail SDK to make the changes that are described in this topic.</span></span> <span data-ttu-id="90816-120">ファイルの更新がされていない場合は、Microsoft Visual Studio Online (VSO)のようなソース管理システムを利用することを推奨します。</span><span class="sxs-lookup"><span data-stu-id="90816-120">We also recommend that you use a source control system, such as Microsoft Visual Studio Online (VSO), where no files have been changed yet.</span></span>

> [!NOTE]
> <span data-ttu-id="90816-121">使用しているコマースのバージョンによって、このトピックの手順の一部が異なります。</span><span class="sxs-lookup"><span data-stu-id="90816-121">Some steps in the procedures in this topic differ, depending on the version of Commerce that you're using.</span></span> <span data-ttu-id="90816-122">詳細については、 [Dynamics 365 Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90816-122">For more information, see [What's new or changed in Dynamics 365 Retail](../get-started/whats-new.md).</span></span>

> [!NOTE]
> <span data-ttu-id="90816-123">Commerce 10.0.8 およびそれ以降では、Retail Server は Commerce Scale Unit と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="90816-123">In Commerce 10.0.8 and above, Retail Server is known as Commerce Scale Unit.</span></span> <span data-ttu-id="90816-124">このトピックは、アプリの以前の複数のバージョンに適用されるため、このトピック全体で *Retail サーバー*を使用します。</span><span class="sxs-lookup"><span data-stu-id="90816-124">Because this topic applies to multiple previous versions of the app, *Retail Server* is used throughout the topic.</span></span>


## <a name="overview-of-integration-with-control-units"></a><span data-ttu-id="90816-125">コントロール ユニットとの統合の概要</span><span class="sxs-lookup"><span data-stu-id="90816-125">Overview of integration with control units</span></span>

<span data-ttu-id="90816-126">サンプルには、次の機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="90816-126">The sample includes the following capabilities:</span></span>

- <span data-ttu-id="90816-127">営業、返品、レシートのコピーは、POS がペアリングされているハードウェア ステーションに物理的に接続済みのコントロール ユニットに自動登録されます。</span><span class="sxs-lookup"><span data-stu-id="90816-127">Sales, returns, and receipt copies are automatically registered in a control unit that is connected to the Hardware station that is paired with the POS.</span></span>
- <span data-ttu-id="90816-128">登録されたトランザクションのコントロール ユニットの制御コードと製造番号は、コントロール ユニットからキャプチャされ、トランザクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="90816-128">The control code and the manufacturing number of the control unit for a registered transaction are captured from the control unit and saved in the transaction.</span></span> <span data-ttu-id="90816-129">(このデータは_会計データ_とも呼ばれます。) 会計データは、**店舗のトランザクション** ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="90816-129">(This data is also referred to as _fiscal data_.) The fiscal data can be viewed on the **Store transactions** page.</span></span>
- <span data-ttu-id="90816-130">コントロール ユニットの制御コードと製造番号のカスタム フィールドはレシート形式に追加できるため、トランザクションの会計データをレシートに印刷できます。</span><span class="sxs-lookup"><span data-stu-id="90816-130">Custom fields for the control code and the manufacturing number of the control unit can be added to a receipt format, so that you can print the fiscal data for the transaction on a receipt.</span></span>
- <span data-ttu-id="90816-131">トランザクションの会計データは、**電子ジャーナル (スウェーデン)** チャネル レポートに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="90816-131">The fiscal data for a transaction is printed on the **Electronic journal (Sweden)** channel report.</span></span>
- <span data-ttu-id="90816-132">コントロール ユニットでのトランザクションの登録中に障害が発生した場合、トランザクションの会計データは空白のままになります。</span><span class="sxs-lookup"><span data-stu-id="90816-132">If a failure occurs during the registration of a transaction in the control unit, the fiscal data for the transaction remains blank.</span></span> <span data-ttu-id="90816-133">この場合、新しいトランザクションを開始することはできず、現在のシフトを閉じることもできません。</span><span class="sxs-lookup"><span data-stu-id="90816-133">In this case, a new transaction can't be started, and the current shift can't be closed.</span></span> <span data-ttu-id="90816-134">オペレーターは、未登録のトランザクションをコントロール ユニットに再登録するよう求められます。</span><span class="sxs-lookup"><span data-stu-id="90816-134">The operator will be asked to try to register the unregistered transaction again in the control unit.</span></span> <span data-ttu-id="90816-135">2 回目の試行が失敗した場合、オペレーターは、特別な許可があれば登録をスキップできます。</span><span class="sxs-lookup"><span data-stu-id="90816-135">If the second attempt fails, the operator can skip the registration, provided that the operator has a special permission.</span></span> <span data-ttu-id="90816-136">オペレーターがコントロール ユニットでのトランザクションの登録をスキップした場合、このイベントに関する情報は会計データではなくトランザクションに保存されます。</span><span class="sxs-lookup"><span data-stu-id="90816-136">If the operator skips the registration of a transaction in the control unit, information about this event is saved in the transaction instead of the fiscal data.</span></span>

> [!NOTE]
> <span data-ttu-id="90816-137">現時点では、コントロール ユニット統合サンプルは顧客注文をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="90816-137">Currently, the control unit integration sample doesn't support customer orders.</span></span> <span data-ttu-id="90816-138">ただし、顧客注文をサポートするサンプルは、後日入手可能になります。</span><span class="sxs-lookup"><span data-stu-id="90816-138">However, a sample that supports customer orders will be available at a later date.</span></span>

## <a name="setting-up-integration-with-control-units"></a><span data-ttu-id="90816-139">コントロール ユニットとの統合のセットアップ</span><span class="sxs-lookup"><span data-stu-id="90816-139">Setting up integration with control units</span></span>

<span data-ttu-id="90816-140">Retail POS がスウェーデンのコントロール ユニットと統合されるように、次の設定を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="90816-140">You must specify the following settings, so that Retail POS is integrated with control units for Sweden.</span></span>

1. <span data-ttu-id="90816-141">会計登録の構成を作成し、ハードウェア プロファイルに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="90816-141">Create fiscal register configurations, and assign them to hardware profiles:</span></span>

    1. <span data-ttu-id="90816-142">**会計登録の構成**ページで、新しい会計登録の構成レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="90816-142">On the **Fiscal register configurations** page, create a new fiscal register configuration record.</span></span> <span data-ttu-id="90816-143">構成の名前と説明を設定します。</span><span class="sxs-lookup"><span data-stu-id="90816-143">Set the name and the description of the configuration.</span></span>
    2. <span data-ttu-id="90816-144">構成の内容を入力します。</span><span class="sxs-lookup"><span data-stu-id="90816-144">Fill in the configuration content.</span></span> <span data-ttu-id="90816-145">このサンプルで構成は、消費税コードとコントロール ユニットの VAT グループ間のマッピングを確立する XML ファイルです。</span><span class="sxs-lookup"><span data-stu-id="90816-145">For this sample, a configuration is an XML file that establishes the mapping between sales tax codes and a control unit's VAT groups.</span></span> <span data-ttu-id="90816-146">最大 4 つの消費税コードをマッピングできます。</span><span class="sxs-lookup"><span data-stu-id="90816-146">You can map up to four sales tax codes.</span></span> <span data-ttu-id="90816-147">次の構成例では、**VAT10** および **VAT20** はマッピングする必要がある消費税コードを表しています。</span><span class="sxs-lookup"><span data-stu-id="90816-147">In the following example of a configuration, **VAT10** and **VAT20** represent sales tax codes that must be mapped.</span></span>

        ``` xml
        <UnitConfiguration>
            <TaxMapping>
                <Tax taxCode="VAT10" controlUnitTaxId="1"/>
                <Tax taxCode="VAT20" controlUnitTaxId="2"/>
            </TaxMapping>
        </UnitConfiguration>
        ```

        <span data-ttu-id="90816-148">アクション ペインで**サンプル構成のエクスポート** をクリックして、サンプル構成をエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="90816-148">You can also export a sample configuration by clicking **Export sample configuration** on the Action Pane.</span></span>

    3. <span data-ttu-id="90816-149">**ハードウェア プロファイル**ページで、POS がペアリングされ、コントロール ユニットが接続されているハードウェア ステーションのハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="90816-149">On the **Hardware profiles** page, select the hardware profile of the Hardware station that the POS is paired with and the control unit is connected to.</span></span> <span data-ttu-id="90816-150">**会計登録**ファストタブで、以下のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="90816-150">On the **Fiscal register** FastTab, set the following fields:</span></span>

        - <span data-ttu-id="90816-151">**会計登録** フィールドで、**サードパーティ要因**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90816-151">In the **Fiscal register** field, select **Third-party driver**.</span></span>
        - <span data-ttu-id="90816-152">**構成**フィールドで、作成した会計登録の構成名を選択します。</span><span class="sxs-lookup"><span data-stu-id="90816-152">In the **Configuration** field, select the name of the fiscal register configuration that you just created.</span></span>

2. <span data-ttu-id="90816-153">レシートレイアウト用のカスタム フィールドを設定し、コントロール ユニットの制御コードと製造番号がレシートに印刷されるようにします。</span><span class="sxs-lookup"><span data-stu-id="90816-153">Set up custom fields for receipt layouts, so that the control code and the manufacturing number of the control unit are printed on receipts:</span></span>

    1. <span data-ttu-id="90816-154">**言語テキスト** ページで、カスタムレシートレイアウト フィールドのキャプションに 2 つのレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="90816-154">On the **Language text** page, add two records for the captions of the custom receipt layout fields.</span></span> <span data-ttu-id="90816-155">適切なフィールドで、キャプションの言語 ID (たとえば**sv-se**)、テキスト ID (たとえば **900001** や **900002**)、キャプション テキスト (たとえば**制御コード**や**コントロール ユニット ID** ) を指定します。</span><span class="sxs-lookup"><span data-stu-id="90816-155">In the appropriate fields, specify the language ID for the captions (for example, **sv-se**), the text ID (for example, **900001** and **900002**), and the caption text (for example, **Control code** and **Control unit ID**).</span></span>
    2. <span data-ttu-id="90816-156">**カスタム フィールド** ページで、カスタムレシートレイアウトのフィールドに 2 つのレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="90816-156">On the **Custom fields** page, add two records for the custom receipt layout fields.</span></span> <span data-ttu-id="90816-157">**タイプ**フィールドで、**レシート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="90816-157">In the **Type** field, select **Receipt**.</span></span> <span data-ttu-id="90816-158">カスタム レシート レイアウトのフィールドの名前とキャプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="90816-158">Specify names and captions for the custom receipt layout fields:</span></span>

        - <span data-ttu-id="90816-159">制御コード:</span><span class="sxs-lookup"><span data-stu-id="90816-159">Control code:</span></span>

            - <span data-ttu-id="90816-160">**名前:** **FiscalRegisterControlCode**</span><span class="sxs-lookup"><span data-stu-id="90816-160">**Name:** **FiscalRegisterControlCode**</span></span>
            - <span data-ttu-id="90816-161">**キャプション テキスト ID**: 制御コード フィールドに指定したテキスト ID (前の例では **900001**)</span><span class="sxs-lookup"><span data-stu-id="90816-161">**Caption text ID:** The text ID that you specified for the control code field (**900001** in the preceding example)</span></span>

        - <span data-ttu-id="90816-162">コントロール ユニットの製造番号:</span><span class="sxs-lookup"><span data-stu-id="90816-162">Manufacturing number of the control unit:</span></span>

            - <span data-ttu-id="90816-163">**名前:** **FiscalRegisterId**</span><span class="sxs-lookup"><span data-stu-id="90816-163">**Name:** **FiscalRegisterId**</span></span>
            - <span data-ttu-id="90816-164">**キャプション テキスト ID**: コントロール ユニット ID フィールドに指定したテキスト ID (前の例では **900002**)</span><span class="sxs-lookup"><span data-stu-id="90816-164">**Caption text ID:** The text ID that you specified for the control unit ID field (**900002** in the preceding example)</span></span>

    3. <span data-ttu-id="90816-165">販売レシートの形式については、レシート レイアウトの**フッター** セクションのレシート形式デザイナーで、指定されたキャプションのフィールドを追加します (前の例では**制御コード**および**コントロール ユニット**)。</span><span class="sxs-lookup"><span data-stu-id="90816-165">For sales receipt formats, in the Receipt format designer, in the **Footer** section of the receipt layout, add the fields for the specified captions (**Control code** and **Control unit ID** in the preceding example).</span></span>

3. <span data-ttu-id="90816-166">店舗の作業者の POS アクセス許可グループおよび個々のアクセス許可の設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="90816-166">Update POS permissions groups and individual permission settings for store workers.</span></span> <span data-ttu-id="90816-167">アクセス許可グループに割り当てられている作業者が会計登録を省略できるようにするには、**会計登録のスキップを許可する**チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="90816-167">To allow workers who are assigned to the permission group to skip the fiscal registration, select the **Allow skip fiscal registration** check box.</span></span>

## <a name="development-environment"></a><span data-ttu-id="90816-168">開発環境</span><span class="sxs-lookup"><span data-stu-id="90816-168">Development environment</span></span>

<span data-ttu-id="90816-169">サンプルをテストして拡張できるように開発環境を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="90816-169">Follow these steps to set up a development environment so that you can test and extend the sample.</span></span>

1. <span data-ttu-id="90816-170">ハードウェア ステーション コンポーネントを拡張します。</span><span class="sxs-lookup"><span data-stu-id="90816-170">Extend the Hardware station component:</span></span>

    1. <span data-ttu-id="90816-171">**RetailSDK\\SampleExtensions\\HardwareStation**から ハードウェア ステーション ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="90816-171">Open the Hardware station solution under **RetailSDK\\SampleExtensions\\HardwareStation**.</span></span>
    2. <span data-ttu-id="90816-172">**HardwareStation.Extension.FiscalRegisterSample.csproj** 拡張機能プロジェクトを検索し、コンパイルします。</span><span class="sxs-lookup"><span data-stu-id="90816-172">Find the **HardwareStation.Extension.FiscalRegisterSample.csproj** extension project, and compile it.</span></span>
    3. <span data-ttu-id="90816-173">拡張機能アセンブリおよび設定を検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-173">Find extension assemblies and configurations.</span></span>

        # <a name="retail-73-and-earlier"></a>[<span data-ttu-id="90816-174">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="90816-174">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

        <span data-ttu-id="90816-175">**Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-175">Find the following files in **Extension.FiscalRegisterSample\\bin\\Debug**:</span></span>

        - <span data-ttu-id="90816-176">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="90816-176">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
        - <span data-ttu-id="90816-177">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="90816-177">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>
        - <span data-ttu-id="90816-178">**Interop.CleanCash\_1\_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="90816-178">The **Interop.CleanCash\_1\_1.dll** assembly</span></span>

        # <a name="retail-731-and-later"></a>[<span data-ttu-id="90816-179">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-179">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="90816-180">**Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-180">Find the following files in **Extension.FiscalRegisterSample\\bin\\Debug**:</span></span>

        - <span data-ttu-id="90816-181">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="90816-181">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
        - <span data-ttu-id="90816-182">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="90816-182">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>
        - <span data-ttu-id="90816-183">**Interop.CleanCash\_1\_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="90816-183">The **Interop.CleanCash\_1\_1.dll** assembly</span></span>

        # <a name="retail-100-and-later"></a>[<span data-ttu-id="90816-184">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-184">Retail 10.0 and later</span></span>](#tab/retail-10-0)

        <span data-ttu-id="90816-185">**Extension.FiscalRegisterSample\\bin\\Debug** から以下のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-185">Find the following files in **Extension.FiscalRegisterSample\\bin\\Debug**:</span></span>

        - <span data-ttu-id="90816-186">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="90816-186">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll** assembly</span></span>
        - <span data-ttu-id="90816-187">**Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="90816-187">The **Contoso.Commerce.HardwareStation.FiscalRegisterSample.dll.config** configuration</span></span>

        <span data-ttu-id="90816-188">**RetailSDK\\References\\Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1\\lib\\net451** にて次のファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-188">Find the following file in **RetailSDK\\References\\Microsoft.Dynamics.Commerce.CleanCashInterop.1.0.1\\lib\\net451**:</span></span>

        - <span data-ttu-id="90816-189">**Interop.CleanCash\_1\_1.dll** アセンブリ</span><span class="sxs-lookup"><span data-stu-id="90816-189">The **Interop.CleanCash\_1\_1.dll** assembly</span></span>

        ---

    4. <span data-ttu-id="90816-190">ファイルを配置した ハードウェア ステーション マシンにコピーします。</span><span class="sxs-lookup"><span data-stu-id="90816-190">Copy the files to a deployed Hardware station machine:</span></span>

        - <span data-ttu-id="90816-191">**リモート ハードウェア ステーション:** ファイルを、Microsoft インターネット インフォメーション サービス (IIS) ハードウェア ステーション サイトの場所の **bin** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="90816-191">**Remote Hardware station:** Copy the files to the **bin** folder under the Microsoft Internet Information Services (IIS) Hardware station site location.</span></span>
        - <span data-ttu-id="90816-192">**ローカル ハードウェア ステーション:** Modern POS クライアント ブローカーの場所にファイルをコピーします。</span><span class="sxs-lookup"><span data-stu-id="90816-192">**Local Hardware station:** Copy the files to the Modern POS client broker location.</span></span>

    5. <span data-ttu-id="90816-193">ハードウェア ステーションの拡張機能のコンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-193">Find the configuration file for Hardware station's extensions.</span></span>

        # <a name="retail-73-and-earlier"></a>[<span data-ttu-id="90816-194">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="90816-194">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

        - <span data-ttu-id="90816-195">**リモート ハードウェア ステーション:** ファイルの名前は **hardwarestation.shared.config**で、IIS ハードウェア ステーション サイトの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="90816-195">**Remote Hardware station:** The file is named **hardwarestation.shared.config**, and it's under the IIS Hardware station site location.</span></span>
        - <span data-ttu-id="90816-196">**ローカル ハードウェア ステーション:** ファイルの名前は **HardwareStation.Dedicated.config**で、Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="90816-196">**Local Hardware station:** The file is named **HardwareStation.Dedicated.config**, and it's under the Modern POS client broker location.</span></span>

        # <a name="retail-731-and-later"></a>[<span data-ttu-id="90816-197">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-197">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="90816-198">ファイルの名前は **HardwareStation.Extension.config** です。</span><span class="sxs-lookup"><span data-stu-id="90816-198">The file is named **HardwareStation.Extension.config**:</span></span>

        - <span data-ttu-id="90816-199">**リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="90816-199">**Remote Hardware station:** The file is located under the IIS Hardware station site location.</span></span>
        - <span data-ttu-id="90816-200">**ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="90816-200">**Local Hardware station:** The file is located under the Modern POS client broker location.</span></span>

        # <a name="retail-100-and-later"></a>[<span data-ttu-id="90816-201">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-201">Retail 10.0 and later</span></span>](#tab/retail-10-0)

        <span data-ttu-id="90816-202">ファイルの名前は **HardwareStation.Extension.config** です。</span><span class="sxs-lookup"><span data-stu-id="90816-202">The file is named **HardwareStation.Extension.config**:</span></span>

        - <span data-ttu-id="90816-203">**リモート ハードウェア ステーション:** ファイルは IIS ハードウェア ステーション サイトの場所に保存されています。</span><span class="sxs-lookup"><span data-stu-id="90816-203">**Remote Hardware station:** The file is located under the IIS Hardware station site location.</span></span>
        - <span data-ttu-id="90816-204">**ローカル ハードウェア ステーション:** ファイルは Modern POS クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="90816-204">**Local Hardware station:** The file is located under the Modern POS client broker location.</span></span>

        ---

    6. <span data-ttu-id="90816-205">コンフィギュレーション ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="90816-205">Add the following section to the **composition** section of the config file.</span></span>

        # <a name="retail-73-and-earlier"></a>[<span data-ttu-id="90816-206">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="90816-206">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-later"></a>[<span data-ttu-id="90816-207">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-207">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-100-and-later"></a>[<span data-ttu-id="90816-208">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-208">Retail 10.0 and later</span></span>](#tab/retail-10-0)

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
        ```

        ---

    7. <span data-ttu-id="90816-209">ハードウェア ステーション サービスを再起動します。</span><span class="sxs-lookup"><span data-stu-id="90816-209">Restart the Hardware station service:</span></span>

        - <span data-ttu-id="90816-210">**リモート ハードウェア ステーション:** IIS マネージャーからハードウェア ステーション サイトを再起動します。</span><span class="sxs-lookup"><span data-stu-id="90816-210">**Remote Hardware station:** Restart the Hardware station site from IIS Manager.</span></span>
        - <span data-ttu-id="90816-211">**ローカル ハードウェア ステーション:** タスク マネージャーで **dllhost.exe** プロセスを終了して、Modern POS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="90816-211">**Local Hardware station:** End the **dllhost.exe** process in Task Manager, and then restart Modern POS.</span></span>

2. <span data-ttu-id="90816-212">CRT コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="90816-212">Extend the CRT component:</span></span>

    1. <span data-ttu-id="90816-213">**RetailSdk\\SampleExtensions\\CommerceRuntime** 配下の、 CRT ソリューション、 **CommerceRuntimeSamples.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="90816-213">Open the CRT solution, **CommerceRuntimeSamples.sln**, under **RetailSdk\\SampleExtensions\\CommerceRuntime**.</span></span>
    2. <span data-ttu-id="90816-214">**Runtime.Extensions.FiscalRegisterReceiptSample** プロジェクトを探して、構築します。</span><span class="sxs-lookup"><span data-stu-id="90816-214">Find the **Runtime.Extensions.FiscalRegisterReceiptSample** project, and build it.</span></span>
    3. <span data-ttu-id="90816-215">CRT の ext.config ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-215">Find the ext.config file for CRT:</span></span>

        - <span data-ttu-id="90816-216">**Retail Server:** : ファイルは IIS 小売サーバー が格納されている場所の **bin\\ext** フォルダー 配下に **commerceRuntime.ext.config** という名前で作成されています。</span><span class="sxs-lookup"><span data-stu-id="90816-216">**Retail Server:** The file is named **commerceRuntime.ext.config**, and it's under the **bin\\ext** folder under the IIS Retail server site location.</span></span>
        - <span data-ttu-id="90816-217">**Modern POS上のローカル CRT :** ファイルは、ローカル CRT クライアントブローカーが格納されている場所の **bin\\ext** フォルダ配下に、 **CommerceRuntime.MPOSOffline.Ext.config** という名前で作成されています。</span><span class="sxs-lookup"><span data-stu-id="90816-217">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's under the **bin\\ext** folder under the local CRT client broker location.</span></span>

    4. <span data-ttu-id="90816-218">コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="90816-218">Register the CRT change in the configuration file.</span></span>

        ``` xml
        <add source="type" value="Contoso.Commerce.Runtime.FiscalRegisterReceipt, Contoso.Commerce.Runtime.FiscalRegisterReceipt" />
        ```

        > [!NOTE]
        > <span data-ttu-id="90816-219">commerceruntime.config および CommerceRuntime.MPOSOffline.config ファイルを編集しては**いけません**。</span><span class="sxs-lookup"><span data-stu-id="90816-219">Do **not** edit the commerceruntime.config and CommerceRuntime.MPOSOffline.config files.</span></span> <span data-ttu-id="90816-220">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="90816-220">These files aren't intended for any customizations.</span></span>

    5. <span data-ttu-id="90816-221">**Extensions.FiscalRegisterReceiptSample\\bin\\Debug** で、 **Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** アセンブリを検索します。</span><span class="sxs-lookup"><span data-stu-id="90816-221">Find the **Contoso.Commerce.Runtime.FiscalRegisterReceiptSample.dll** assembly file in **Extensions.FiscalRegisterReceiptSample\\bin\\Debug**.</span></span>
    6. <span data-ttu-id="90816-222">アセンブリを CRT 拡張機能フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="90816-222">Copy the assembly to the CRT extensions folder:</span></span>

        - <span data-ttu-id="90816-223">**小売りサーバー:** アセンブリを IIS Retail Server が格納されている場所の配下にある **\\bin\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="90816-223">**Retail Server:** Copy the assembly to the **\\bin\\ext** folder under the IIS Retail server site location.</span></span>
        - <span data-ttu-id="90816-224">**Local CRT on Modern POS:** アセンブリをローカル CRT クライアント ブローカーがある場所の下の **\\\ext** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="90816-224">**Local CRT on Modern POS:** Copy the assembly to the **\\ext** folder under the local CRT client broker location.</span></span>

        > [!NOTE]
        > <span data-ttu-id="90816-225">CRT および Retail サーバーに対するコードの変更はすべて、RetailSdk\\SampleExtensions の一部となります。</span><span class="sxs-lookup"><span data-stu-id="90816-225">All the code changes for CRT and Retail Server are all part of RetailSdk\\SampleExtensions.</span></span> <span data-ttu-id="90816-226">したがって、上記の手順は、これらのコードの変更を構築、配置、およびテストする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="90816-226">Therefore, the preceding steps show how to build, deploy, and test these code changes.</span></span>

3. <span data-ttu-id="90816-227">Modern POS コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="90816-227">Extend the Modern POS component:</span></span>

    1. <span data-ttu-id="90816-228">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="90816-228">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="90816-229">また、Modern POS が **Run** コマンドを使用して、Microsoft Visual Studio から実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="90816-229">Also make sure that Modern POS can be run from Microsoft Visual Studio using the **Run** command.</span></span> <span data-ttu-id="90816-230">(Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="90816-230">(Modern POS must not be customized.</span></span> <span data-ttu-id="90816-231">ユーザー アカウント制御 \[UAC\] を有効にし、必要に応じて既にインストールされている Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="90816-231">You must enable User Account Control \[UAC\], and you must uninstall previously installed instances of Modern POS as required.)</span></span>
    2. <span data-ttu-id="90816-232">**Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。</span><span class="sxs-lookup"><span data-stu-id="90816-232">Include **FiscalRegisterSample** in the **Pos.Extensions** project.</span></span>
    3. <span data-ttu-id="90816-233">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="90816-233">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    4. <span data-ttu-id="90816-234">以下の行を適切な場所に追加することで、 **Extensions\\extensions.json** の拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="90816-234">Enable the extension in **Extensions\\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    5. <span data-ttu-id="90816-235">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="90816-235">Rebuild the solutions.</span></span>
    6. <span data-ttu-id="90816-236">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="90816-236">Run Modern POS in the debugger, and test the functionality.</span></span>

4. <span data-ttu-id="90816-237">クラウド POS コンポーネントの拡張。</span><span class="sxs-lookup"><span data-stu-id="90816-237">Extend the Cloud POS component:</span></span>

    1. <span data-ttu-id="90816-238">**RetailSdk\\POS\\CloudPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="90816-238">Open the solution at **RetailSdk\\POS\\CloudPOS.sln**, and make sure that it can be compiled without errors.</span></span>
    2. <span data-ttu-id="90816-239">**Pos.Extensions** プロジェクトの **FiscalRegisterSample** を含めます。</span><span class="sxs-lookup"><span data-stu-id="90816-239">Include **FiscalRegisterSample** in the **Pos.Extensions** project.</span></span>
    3. <span data-ttu-id="90816-240">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="90816-240">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    4. <span data-ttu-id="90816-241">以下の行を適切な場所に追加することで、 **Extensions\\extensions.json** の拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="90816-241">Enable the extension in **Extensions\\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "debugBuildsOnly": false,
            "baseUrl": "FiscalRegisterSample"
        }
        ```

    5. <span data-ttu-id="90816-242">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="90816-242">Rebuild the solutions.</span></span>
    6. <span data-ttu-id="90816-243">**実行**コマンドを使用してソリューションを実行し、Retail SDK ハンドブックにあるで手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="90816-243">Run the solution by using the **Run** command and following the steps in the Retail SDK handbook.</span></span>
    7. <span data-ttu-id="90816-244">機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="90816-244">Test the functionality.</span></span>

5. <span data-ttu-id="90816-245">本社で、会計登録構成と、その他の必要なパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="90816-245">Set up the fiscal register configuration and other required parameters in Headquarters.</span></span> <span data-ttu-id="90816-246">詳細については、[スウェーデンのキャッシュ レジスター機能](emea-swe-cash-registers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90816-246">For more information, see [Cash register functionality for Sweden](emea-swe-cash-registers.md).</span></span>

## <a name="production-environment"></a><span data-ttu-id="90816-247">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="90816-247">Production environment</span></span>

<span data-ttu-id="90816-248">以下の手順に従い、実稼働環境でコマース コンポーネントを含む配置可能パッケージを作成して適用します。</span><span class="sxs-lookup"><span data-stu-id="90816-248">Follow these steps to create and apply deployable packages that contain Commerce components in a production environment.</span></span>

1. <span data-ttu-id="90816-249">POS コンポーネントの拡張</span><span class="sxs-lookup"><span data-stu-id="90816-249">Extend the POS component</span></span>

    1. <span data-ttu-id="90816-250">除外リストから **FiscalRegisterSample** フォルダーを削除して、**tsconfig.json** でコンパイルされる拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="90816-250">Enable the extension to be compiled in **tsconfig.json** by removing the **FiscalRegisterSample** folder from the exclude list.</span></span>
    2. <span data-ttu-id="90816-251">以下の行を適切な場所に追加することで、 **Extensions\\extensions.json** の拡張機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="90816-251">Enable the extension in **Extensions\\extensions.json** by adding the following lines in the appropriate place.</span></span>

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

2. <span data-ttu-id="90816-252">**RetailSdk\\Assets** フォルダのパッケージ構成ファイルに、次の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="90816-252">Make the following changes in the package config files under the **RetailSdk\\Assets** folder:</span></span>

    1. <span data-ttu-id="90816-253">**commerceruntime.ext.config** および **CommerceRuntime.MPOSOffline.Ext.config** 構成ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="90816-253">Add the following section to the **composition** section of the **commerceruntime.ext.config** and **CommerceRuntime.MPOSOffline.Ext.config** config files.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
        ```

    2. <span data-ttu-id="90816-254">ハードウェア ステーション構成ファイルの **構成** セクションに、次のセクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="90816-254">Add the following section to the **composition** section of the Hardware station configuration file.</span></span>

        # <a name="retail-73-and-earlier"></a>[<span data-ttu-id="90816-255">Retail 7.3 以前</span><span class="sxs-lookup"><span data-stu-id="90816-255">Retail 7.3 and earlier</span></span>](#tab/retail-7-3)

        <span data-ttu-id="90816-256">**HardwareStation.Shared.config** および **HardwareStation.Dedicated.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="90816-256">Modify the **HardwareStation.Shared.config** and **HardwareStation.Dedicated.config** configuration files.</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```

        # <a name="retail-731-and-later"></a>[<span data-ttu-id="90816-257">Retail 7.3.1 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-257">Retail 7.3.1 and later</span></span>](#tab/retail-7-3-1)

        <span data-ttu-id="90816-258">**HardwareStation.Extension.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="90816-258">Modify the **HardwareStation.Extension.config** configuration file:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
        ```
        
        # <a name="retail-100-and-later"></a>[<span data-ttu-id="90816-259">Retail 10.0 およびそれ以降</span><span class="sxs-lookup"><span data-stu-id="90816-259">Retail 10.0 and later</span></span>](#tab/retail-10-0)

        <span data-ttu-id="90816-260">**HardwareStation.Extension.config** 構成ファイルを変更します。</span><span class="sxs-lookup"><span data-stu-id="90816-260">Modify the **HardwareStation.Extension.config** configuration file:</span></span>

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
        ```

        ---

3. <span data-ttu-id="90816-261">**BuildTools\\Customization.settings** パッケージ カスタマイズ コンフィギュレーション ファイルに以下の変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="90816-261">Make the following changes in the **BuildTools\\Customization.settings** package customization configuration file:</span></span>

   - <span data-ttu-id="90816-262">展開可能なパッケージにハードウェア ステーション拡張機能を含めるために、次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="90816-262">Add the following line to include the Hardware station extension in deployable packages:</span></span>
        ``` xml
        <ISV_CommerceRuntime_CustomizableFileInclude="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll"/>
        ```

4. <span data-ttu-id="90816-263">Retail SDK 全体で **msbuild** を実行し、配置可能なパッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="90816-263">Run **msbuild** for the whole Retail SDK to create deployable packages.</span></span>
5. <span data-ttu-id="90816-264">Microsoft Dynamics Lifecycle Services (LCS) 経由または手動でパッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="90816-264">Apply the packages via Microsoft Dynamics Lifecycle Services (LCS) or manually.</span></span> <span data-ttu-id="90816-265">詳細については、[Retail SDK パッケージ](../dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="90816-265">For more information, see [Retail SDK packaging](../dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>


---
title: イタリア向け電子請求書のアドオンの使用を開始する
description: このトピックでは、Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management におけるイタリアの電子請求アドオンで使用する電子請求アドオンを使い始める際に有用な情報を提供します。
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 08d41244d3ec785127db8f69e37dd522a463c388
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988543"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="38c07-103">イタリア向け電子請求書のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="38c07-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="38c07-104">イタリア向けの電子請求書アドオンは、現時点では Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management の電子請求書で利用できるすべての機能に対応していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="38c07-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="38c07-105">このトピックでは、イタリア向けの電子請求書作成アドオンの使用を開始するにあたっての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="38c07-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="38c07-106">このガイドでは、Regulatory Configuration Services (RCS) 、財務における、国ごとに異なる構成手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="38c07-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="38c07-107">また、サービスを介してイタリア固有の **FatturaPA** 形式で生成された電子請求書を送信するための手順、および処理の結果を確認する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="38c07-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="38c07-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="38c07-108">Prerequisites</span></span>

<span data-ttu-id="38c07-109">このトピックの手順を実行する前に、 [電子請求アドオンを使用する](e-invoicing-get-started.md)に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38c07-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="38c07-110">RCS の設定</span><span class="sxs-lookup"><span data-stu-id="38c07-110">RCS setup</span></span>

<span data-ttu-id="38c07-111">RCS の設定を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="38c07-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="38c07-112">**FatturaPA** 形式で顧客の電子請求書をエクスポートする際に使用する電子請求書の機能をインポートします。</span><span class="sxs-lookup"><span data-stu-id="38c07-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="38c07-113">電子請求書の作成、提出、回答の受信に必要な形式の構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="38c07-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="38c07-114">電子請求書の提出シナリオに対応したイベントを構成します。</span><span class="sxs-lookup"><span data-stu-id="38c07-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="38c07-115">電子請求書機能を公開する。</span><span class="sxs-lookup"><span data-stu-id="38c07-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="38c07-116">"電子請求のアドオン機能" は、電子請求書のアドオン サーバーを使用するように構成および公開されたリソースの総称です。</span><span class="sxs-lookup"><span data-stu-id="38c07-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="38c07-117">この場合は、顧客の電子請求書のエクスポートは、これから設定を行う電子請求書の機能となります。</span><span class="sxs-lookup"><span data-stu-id="38c07-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="38c07-118">電子請求書機能をインポートする</span><span class="sxs-lookup"><span data-stu-id="38c07-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="38c07-119">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="38c07-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="38c07-120">**グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求書** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="38c07-121">**電子請求書機能** ページで、**インポート** を選択して、グローバル レポジトリから電子請求書の機能をインポートします。</span><span class="sxs-lookup"><span data-stu-id="38c07-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="38c07-122">利用可能な機能の一覧が表示されない場合は、**同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="38c07-123">**電子請求書のエクスポート (IT)** 機能を選択し、**インポート** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="38c07-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![電子請求書エクスポート (IT) 機能のインポート](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="38c07-125">**電子請求書エクスポート (IT)** 機能をグローバル レポジトリからインポートすると、次のセクションで説明されているすべての設定もインポートされます。</span><span class="sxs-lookup"><span data-stu-id="38c07-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="38c07-126">電子請求書エクスポート (IT) 機能の新しいバージョンを作成する</span><span class="sxs-lookup"><span data-stu-id="38c07-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="38c07-127">**電子請求機能** ページの **バージョン** タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![新しい電子請求書機能のバージョンを追加する](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="38c07-129">次に、電子請求書の機能に関連付けられている電子レポート (ER) の形式を構成します。</span><span class="sxs-lookup"><span data-stu-id="38c07-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="38c07-130">**構成** タブで、**追加** を選択して構成のバージョンを管理します。</span><span class="sxs-lookup"><span data-stu-id="38c07-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![電子請求書機能の構成バージョンを管理する](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="38c07-132">この手順では、イタリアの電子請求書のエクスポートに使用されるさまざまなファイルの ER 形式を追加、構成します。</span><span class="sxs-lookup"><span data-stu-id="38c07-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="38c07-133">イタリアの FatturaPA 電子請求書では、次の標準的な構成を使用するか、電子請求書に使用する実際のカスタム構成を使用してください。</span><span class="sxs-lookup"><span data-stu-id="38c07-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="38c07-134">売上請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="38c07-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="38c07-135">プロジェクト請求書 (IT)</span><span class="sxs-lookup"><span data-stu-id="38c07-135">Project invoice (IT)</span></span>

    <span data-ttu-id="38c07-136">別の電子請求書機能から派生した電子請求機能を作成する場合、すべての ER 形式は元の機能から継承されます。</span><span class="sxs-lookup"><span data-stu-id="38c07-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="38c07-137">特定の ER 形式ファイルの構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="38c07-138">**編集** または **表示** を選択して **形式デザイナ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="38c07-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![形式デザイナー ページを開く](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="38c07-140">**形式デザイナー** ページを使用して、ER 形式ファイルの構成を編集、確認します。</span><span class="sxs-lookup"><span data-stu-id="38c07-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![形式デザイナーのページ](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="38c07-142">電子請求書機能の設定を管理する</span><span class="sxs-lookup"><span data-stu-id="38c07-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="38c07-143">**電子請求機能**  ページの **設定** タブで、**追加** や **削除**、**編集** を選択して、電子請求機能の設定を管理します。</span><span class="sxs-lookup"><span data-stu-id="38c07-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![電子請求書機能の設定を管理する](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="38c07-145">この手順では、電子請求書に適用するイベントを構成します。これには、**FatturaPA** 形式やデジタル署名 (必要な場合) における XML 出力ファイルの生成が含まれます。</span><span class="sxs-lookup"><span data-stu-id="38c07-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="38c07-146">売上請求書機能の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="38c07-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="38c07-147">**電子請求機能** ページ上の **設定** タブで、**機能の設定** 列で、**売上請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="38c07-148">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-148">Select **Edit**.</span></span>
3. <span data-ttu-id="38c07-149">**機能のバージョン設定** ページで、**アクション** タブを選択してアクションの一覧を管理します。</span><span class="sxs-lookup"><span data-stu-id="38c07-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="38c07-150">アクションは、イベントを完全に実行するために、順番に従って実行する必要がある操作の一覧を定義します。</span><span class="sxs-lookup"><span data-stu-id="38c07-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![アクション タブ](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="38c07-152">アクション ID</span><span class="sxs-lookup"><span data-stu-id="38c07-152">Action ID</span></span> | <span data-ttu-id="38c07-153">アクション名</span><span class="sxs-lookup"><span data-stu-id="38c07-153">Action name</span></span>        | <span data-ttu-id="38c07-154">アクション説明</span><span class="sxs-lookup"><span data-stu-id="38c07-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="38c07-155">1</span><span class="sxs-lookup"><span data-stu-id="38c07-155">1</span></span>         | <span data-ttu-id="38c07-156">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="38c07-156">Transform document</span></span> | <span data-ttu-id="38c07-157">電子請求書の XML ファイルを **FatturaPA** 形式で作成します。</span><span class="sxs-lookup"><span data-stu-id="38c07-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="38c07-158">2</span><span class="sxs-lookup"><span data-stu-id="38c07-158">2</span></span>         | <span data-ttu-id="38c07-159">ドキュメントに署名</span><span class="sxs-lookup"><span data-stu-id="38c07-159">Sign document</span></span>      | <span data-ttu-id="38c07-160">XML ファイルにデジタル署名を適用します。</span><span class="sxs-lookup"><span data-stu-id="38c07-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="38c07-161">適用のルールを表示、管理するには、**適用ルール** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="38c07-162">適用ルールは、アクションが実行されるコンテキストを定義します。</span><span class="sxs-lookup"><span data-stu-id="38c07-162">Applicability rules define the context where the action will be run.</span></span>

    ![適合性ルール タブ](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="38c07-164">変数を表示、管理するには、**変数** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![変数タブ](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="38c07-166">アクションの実行に必要となるパブリック変数を定義します。</span><span class="sxs-lookup"><span data-stu-id="38c07-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="38c07-167">プロジェクトの請求書機能の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="38c07-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="38c07-168">**プロジェクト請求書** 機能の設定の構成に必要な手順と設定は、**販売請求書** 機能の設定手順と設定方法と共通しています。</span><span class="sxs-lookup"><span data-stu-id="38c07-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="38c07-169">プロジェクト請求書を使用する場合は、売上請求書の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38c07-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="38c07-170">環境にの電子請求書機能を割り当てる</span><span class="sxs-lookup"><span data-stu-id="38c07-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="38c07-171">**電子請求書機能** ページの **環境** タブで、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="38c07-172">**環境** フィールドで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="38c07-173">**有効開始** フィールドで、環境が有効になる日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="38c07-174">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-174">Select **Enable**.</span></span> 

![電子請求書環境を有効化する](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="38c07-176">電子請求書の機能を公開する</span><span class="sxs-lookup"><span data-stu-id="38c07-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="38c07-177">電子請求書機能を公開するには、バージョンの状態を **完了**、または **公開済** に変更します。</span><span class="sxs-lookup"><span data-stu-id="38c07-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="38c07-178">バージョンの状態を完了に変更する</span><span class="sxs-lookup"><span data-stu-id="38c07-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="38c07-179">**電子請求書機能** ページの **バージョン** タブで、状態が **下書き** となっている電子請求書機能のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="38c07-180">**ステータスの変更 \> 完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="38c07-181">バージョンの状態を公開済みに変更する</span><span class="sxs-lookup"><span data-stu-id="38c07-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="38c07-182">**電子請求書機能** ページの **バージョン** タブで、状態が **完了** となっている電子請求書機能のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="38c07-183">**状態の変更 \> 公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-183">Select **Change status \> Publish**.</span></span>

![電子請求書機能の状態を変更する](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="38c07-185">財務における電子請求書のアドオン統合を設定する</span><span class="sxs-lookup"><span data-stu-id="38c07-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="38c07-186">財務の設定を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="38c07-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="38c07-187">ER データ モデル、ERデータ モデル マッピング、および FatturaPA 請求書のコンテキスト構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="38c07-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="38c07-188">イタリアの電子請求書にデジタル署名をするために必要となる証明書を構成します。</span><span class="sxs-lookup"><span data-stu-id="38c07-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="38c07-189">ER データ モデル、データ モデル マッピング、形式をインポートする</span><span class="sxs-lookup"><span data-stu-id="38c07-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="38c07-190">**電子レポート** ワークスペースで、**ビジネス ドキュメント サービス** 構成プロバイダーが **有効** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="38c07-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="38c07-191">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="38c07-192">**グローバル リソース \>  開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="38c07-193">**請求書モデル**、**請求書モデルマッピング**、**顧客請求書コンテキスト モデル** をインポートします。</span><span class="sxs-lookup"><span data-stu-id="38c07-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="38c07-194">イタリア向け顧客電子請求書のエクスポートを有効化する</span><span class="sxs-lookup"><span data-stu-id="38c07-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="38c07-195">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="38c07-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="38c07-196">**機能** タブで、機能参照 **IT00036** 行の **有効** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="38c07-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![FatturaPA 機能を有効にする](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="38c07-198">電子ドキュメントを構成する</span><span class="sxs-lookup"><span data-stu-id="38c07-198">Configure electronic documents</span></span>

1. <span data-ttu-id="38c07-199">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="38c07-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="38c07-200">**電子ドキュメント** タブで、**追加** を選択し、イタリア向けの電子請求書の生成に必要となるテーブルを入力します。</span><span class="sxs-lookup"><span data-stu-id="38c07-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="38c07-201">**テーブル名 :** 顧客請求書仕訳帳</span><span class="sxs-lookup"><span data-stu-id="38c07-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="38c07-202">**テーブル名 :** プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="38c07-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="38c07-203">各テーブルについて、関連するドキュメントのコンテキストを定義します :</span><span class="sxs-lookup"><span data-stu-id="38c07-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="38c07-204">**顧客請求書仕訳帳** で、**顧客請求書のコンテキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="38c07-205">**プロジェクト請求書** で、**プロジェクト請求書のコンテキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-205">For **Project invoice**, select **Project invoice context**.</span></span>

![応答タイプを設定する](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="38c07-207">電子請求書の処理</span><span class="sxs-lookup"><span data-stu-id="38c07-207">Electronic invoice processing</span></span>

<span data-ttu-id="38c07-208">財務の処置を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="38c07-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="38c07-209">電子請求書のアドオンを介してイタリア向けの電子請求書を生成する</span><span class="sxs-lookup"><span data-stu-id="38c07-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="38c07-210">実行ログを表示し、処理結果を確認する</span><span class="sxs-lookup"><span data-stu-id="38c07-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="38c07-211">一般的な電子請求書</span><span class="sxs-lookup"><span data-stu-id="38c07-211">Generate electronic invoices</span></span>

<span data-ttu-id="38c07-212">**構成可能な電子請求のアドオン統合** 機能を有効にして、**IT00036** 機能を有効にすると、イタリア向けの電子請求書を生成する従来の財務プロセスは使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="38c07-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="38c07-213">これは、**電子ドキュメントの送信** という名前の新しいプロセスによって置き換えられ ます。</span><span class="sxs-lookup"><span data-stu-id="38c07-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="38c07-214">電子請求書ドキュメントの要求に基づいてドキュメントを手動で送信することができます。</span><span class="sxs-lookup"><span data-stu-id="38c07-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="38c07-215">続行する前に、イタリア向けの電子請求書に必要な設定が完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="38c07-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="38c07-216">詳細については、[顧客の電子請求書の作成](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="38c07-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="38c07-217">電子請求書のアドオンを有効化することで、そのトピックで説明されている一部の設定手順が使用できなくなる可能性があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="38c07-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="38c07-218">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの送信** に移動します。</span><span class="sxs-lookup"><span data-stu-id="38c07-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="38c07-219">ドキュメントを初めて送信する場合は、**ドキュメントの再送信** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="38c07-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="38c07-220">サービスを使用してドキュメントを再送信する必要がある場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="38c07-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="38c07-221">**含めるレコード** クイックタブで、**フィルター** を選択して **照会** ダイアログ ボックスを開きます。ここでは送信するドキュメントを選択するクエリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="38c07-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![電子ドキュメント ダイアログ ボックスの送信](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="38c07-223">フィルター クエリ</span><span class="sxs-lookup"><span data-stu-id="38c07-223">Filter query</span></span>

1. <span data-ttu-id="38c07-224">**照会** ダイアログ ボックスで、売上請求書とプロジェクト請求書の両方のフィルター条件を構成する、または条件を空白のままにして未提出のすべての請求書をすべて含めるようにします。</span><span class="sxs-lookup"><span data-stu-id="38c07-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![送信フィルター条件を設定する](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="38c07-226">**OK** を選択して **照会** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="38c07-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="38c07-227">**OK** を選択し、選択したドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="38c07-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="38c07-228">注意 : このサービスを利用して初めて書類を提出する際は、電子請求書アドオンとの接続を確認するように促されます。</span><span class="sxs-lookup"><span data-stu-id="38c07-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="38c07-229">**ここをクリックして電子ドキュメント送信サービスに接続する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="38c07-230">送信ログの表示</span><span class="sxs-lookup"><span data-stu-id="38c07-230">View submission logs</span></span>

<span data-ttu-id="38c07-231">全ての提出書類の提出ログを見ることができます。</span><span class="sxs-lookup"><span data-stu-id="38c07-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="38c07-232">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="38c07-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="38c07-233">**ドキュメント タイプ** フィールドで、必要な電子ドキュメントをフィルタ処理する **顧客請求書仕訳帳**、または **プロジェクト請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="38c07-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![提出書類のログを表示するドキュメント タイプの選択](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="38c07-235">**提出状態** 列に表示される値は、提出プロセスの状態を表します。</span><span class="sxs-lookup"><span data-stu-id="38c07-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="38c07-236">これは、プロセスが構成通りに実行されたかどうか、追加のアクションが必要かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="38c07-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="38c07-237">アクション ウィンドウで、**照会\> 提出の詳細** を選択して、提出実行ログの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="38c07-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![提出書類ログの詳細を表示する](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="38c07-239">**処理中のアクション** クイックタブで、RCS で設定された機能のバージョンで構成されているアクションの実行ログを表示できます。</span><span class="sxs-lookup"><span data-stu-id="38c07-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="38c07-240">**状態** 列には、アクションが正常に実行されたかどうかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="38c07-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="38c07-241">**アクション ファイル** のクイックタブでは、アクションの実行中に生成された中間ファイルを表示できます。</span><span class="sxs-lookup"><span data-stu-id="38c07-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="38c07-242">**表示** を選択すると、出力XMLファイルが **FatturaPA** 形式でダウンロードされ、その内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="38c07-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38c07-243">関連トピック</span><span class="sxs-lookup"><span data-stu-id="38c07-243">Related topics</span></span>

- [<span data-ttu-id="38c07-244">電子請求書アドオン機能の概要</span><span class="sxs-lookup"><span data-stu-id="38c07-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="38c07-245">電子請求書のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="38c07-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="38c07-246">電子請求のアドオン設定</span><span class="sxs-lookup"><span data-stu-id="38c07-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)

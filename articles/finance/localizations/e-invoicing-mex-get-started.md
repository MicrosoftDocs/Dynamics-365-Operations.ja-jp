---
title: メキシコ用電子請求の使用を開始する
description: このトピックでは、メキシコ向けの電子請求の使用を開始するにあたっての情報を提供します。
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c1112ba8394afb3aa9c9b4f68249524498bd8b32
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894886"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a><span data-ttu-id="5c413-103">メキシコ用電子請求の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="5c413-103">Get started with Electronic invoicing for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="5c413-104">メキシコ向けの電子請求は、現在のところ、Comprobante Fiscal Digital por Internet (CFDI) 文書で利用できるすべての機能、および Microsoft Dynamics 365 Finance や Dynamics 365 Supply Chain Management に組み込まれている関連する統合で利用できるすべての機能のすべてには対応していない場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c413-104">Electronic invoicing for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="5c413-105">このトピックでは、メキシコ向けの電子請求の使用を開始するにあたっての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c413-105">This topic provides information that will help you get started with Electronic invoicing for Mexico.</span></span> <span data-ttu-id="5c413-106">このガイドでは、Regulatory Configuration Services (RCS) 、財務における、国ごとに異なる構成手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="5c413-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="5c413-107">また、サービスを介して CFDI の請求書を提出するために金融機関で行う必要のある手順や、処理結果や CFDI の請求書の状況を確認する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="5c413-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5c413-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="5c413-108">Prerequisites</span></span>

<span data-ttu-id="5c413-109">このトピックの手順を実行する前に、 [電子請求の使用を開始する](e-invoicing-get-started.md)に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c413-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="5c413-110">RCS の設定</span><span class="sxs-lookup"><span data-stu-id="5c413-110">RCS setup</span></span>

<span data-ttu-id="5c413-111">RCS の設定を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="5c413-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="5c413-112">CFDI の請求書を処理するための電子請求書機能をインポートします。</span><span class="sxs-lookup"><span data-stu-id="5c413-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="5c413-113">CFDI 請求書の作成、提出、回答の受け取り、取消の提出、回答の受け取りに必要なフォーマットの構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="5c413-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="5c413-114">CFDI 請求書の提出シナリオに対応したイベントを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c413-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="5c413-115">CFDI の請求書を処理するための電子請求書機能を公開します。</span><span class="sxs-lookup"><span data-stu-id="5c413-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="5c413-116">"電子請求機能" は、電子請求書のアドオン サーバーを使用するように構成および公開されたリソースの総称です。</span><span class="sxs-lookup"><span data-stu-id="5c413-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="5c413-117">この場合、CFDI 請求書 (MX) は、これから設定する電子請求書機能です。</span><span class="sxs-lookup"><span data-stu-id="5c413-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="5c413-118">電子請求書機能をインポートする</span><span class="sxs-lookup"><span data-stu-id="5c413-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="5c413-119">RCS アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="5c413-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="5c413-120">**グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求書** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="5c413-121">**電子請求書機能** ページで、 **インポート** を選択して、グローバル レポジトリから **CFDI 請求書 (MX)** の機能をインポートします。</span><span class="sxs-lookup"><span data-stu-id="5c413-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c413-122">機能が一覧に表示されない場合は、**同期** を選択し、手順3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5c413-122">If you don't see the feature in the list, select **Synchronize**, and then repeat step 3.</span></span>

![CFDI 請求書 (MX) 機能のインポート](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="5c413-124">グローバル レポジトリから **CFDI 請求書 (MX)** 機能をインポートすると、構成やアクションを含むすべての機能設定もインポートされます。</span><span class="sxs-lookup"><span data-stu-id="5c413-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="5c413-125">CFDI請求書エクスポート (MX) 機能の新しいバージョンを作成する</span><span class="sxs-lookup"><span data-stu-id="5c413-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="5c413-126">たとえば、URL を更新する必要がある場合は、新しいバージョンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5c413-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="5c413-127">詳細については、[電子請求書 CFDI](tasks/mx-00010-e-invoicing-cfdi.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="5c413-128">**電子請求機能** ページの **バージョン** タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![新しい電子請求書機能のバージョンを追加する](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="5c413-130">構成のバージョンを更新する</span><span class="sxs-lookup"><span data-stu-id="5c413-130">Update the configuration version</span></span>

1. <span data-ttu-id="5c413-131">**電子請求機能** ページの **構成** タブで、**追加** または **削除** を選択して、構成のバージョン (ER ファイル形式の構成) を管理します。</span><span class="sxs-lookup"><span data-stu-id="5c413-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![電子請求書機能の構成を管理する](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="5c413-133">新しいバージョンを作成すると、すべての構成が最後に発行されたバージョンから継承されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="5c413-134">CFDI 請求書を処理するには、次のコ構成が必要となります :</span><span class="sxs-lookup"><span data-stu-id="5c413-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="5c413-135">CFDI 請求書 (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="5c413-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="5c413-136">CFDI 応答メッセージのインポート</span><span class="sxs-lookup"><span data-stu-id="5c413-136">CFDI response message import</span></span>
    - <span data-ttu-id="5c413-137">CFDI エラー ログのインポート</span><span class="sxs-lookup"><span data-stu-id="5c413-137">CFDI error log import</span></span>
    - <span data-ttu-id="5c413-138">CFDI 取消申請 (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="5c413-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="5c413-139">CFDI 請求書 (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="5c413-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="5c413-140">一覧で構成バージョンを選択し、**編集** または **表示** を選択すると、**形式デザイナ** ページが表示されます。このページで、構成の編集や表示をすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c413-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![形式デザイナー ページを開く](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="5c413-142">**形式デザイナー** ページを使用して、ER 形式ファイルの構成を編集、確認します。</span><span class="sxs-lookup"><span data-stu-id="5c413-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="5c413-143">詳細については、[電子ドキュメントのコンフィギュレーションの作成](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-143">For more information, see [Create electronic document configurations](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![形式デザイナーのページ](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="5c413-145">電子請求書機能の設定を管理する</span><span class="sxs-lookup"><span data-stu-id="5c413-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="5c413-146">**電子請求機能**  ページの **設定** タブで、**追加** や **削除**、**編集** を選択して、電子請求機能の設定を管理します。</span><span class="sxs-lookup"><span data-stu-id="5c413-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![電子請求書機能の設定を管理する](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="5c413-148">認証に使用する CFDI 請求書を送信するには (XML ファイルを生成し、XML ファイルを送信して応答を処理する) 、**売上請求書** 機能の設定が必要となります。</span><span class="sxs-lookup"><span data-stu-id="5c413-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="5c413-149">CFDI 請求書の取り消しを送信するには、**取り消し** 機能と **取り消し機能の設定** が必要です。</span><span class="sxs-lookup"><span data-stu-id="5c413-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="5c413-150">売上請求書機能の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="5c413-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="5c413-151">**電子請求機能** ページ上の **設定** タブで、**機能の設定** 列で、**売上請求書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="5c413-152">**編集** を選択し、アクションや適用ルール、変数を構成します。</span><span class="sxs-lookup"><span data-stu-id="5c413-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![電子請求書機能の設定を編集する](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="5c413-154">**機能のバージョン設定** ページで、**アクション** タブを選択してアクションの一覧を管理します。</span><span class="sxs-lookup"><span data-stu-id="5c413-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="5c413-155">アクションは、イベントを完全に実行するために、順番に従って実行する必要がある操作の一覧を定義します。</span><span class="sxs-lookup"><span data-stu-id="5c413-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![アクション タブ](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="5c413-157">アクション ID</span><span class="sxs-lookup"><span data-stu-id="5c413-157">Action ID</span></span> | <span data-ttu-id="5c413-158">アクション</span><span class="sxs-lookup"><span data-stu-id="5c413-158">Action</span></span>                   | <span data-ttu-id="5c413-159">アクション名</span><span class="sxs-lookup"><span data-stu-id="5c413-159">Action name</span></span>                                  | <span data-ttu-id="5c413-160">アクション説明</span><span class="sxs-lookup"><span data-stu-id="5c413-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="5c413-161">1</span><span class="sxs-lookup"><span data-stu-id="5c413-161">1</span></span>         | <span data-ttu-id="5c413-162">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="5c413-162">Transform document</span></span>       | <span data-ttu-id="5c413-163">CFDI デジタル署名を含まない電子請求書を生成する</span><span class="sxs-lookup"><span data-stu-id="5c413-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="5c413-164">CFDI 請求書を生成します。</span><span class="sxs-lookup"><span data-stu-id="5c413-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="5c413-165">2</span><span class="sxs-lookup"><span data-stu-id="5c413-165">2</span></span>         | <span data-ttu-id="5c413-166">ドキュメントに署名</span><span class="sxs-lookup"><span data-stu-id="5c413-166">Sign document</span></span>            | <span data-ttu-id="5c413-167">デジタル署名</span><span class="sxs-lookup"><span data-stu-id="5c413-167">Digital sign</span></span>                                 | <span data-ttu-id="5c413-168">提出に使用する電子請求書にデジタル署名をします。</span><span class="sxs-lookup"><span data-stu-id="5c413-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="5c413-169">3</span><span class="sxs-lookup"><span data-stu-id="5c413-169">3</span></span>         | <span data-ttu-id="5c413-170">メキシコ PAC サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="5c413-170">Call Mexican PAC service</span></span> | <span data-ttu-id="5c413-171">CFDI 電子請求書を送信する</span><span class="sxs-lookup"><span data-stu-id="5c413-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="5c413-172">Windows Communication Foundation (WCF) クライアントは、CFDI 電子請求書を送信します。</span><span class="sxs-lookup"><span data-stu-id="5c413-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="5c413-173">4</span><span class="sxs-lookup"><span data-stu-id="5c413-173">4</span></span>         | <span data-ttu-id="5c413-174">応答の処理</span><span class="sxs-lookup"><span data-stu-id="5c413-174">Process response</span></span>         | <span data-ttu-id="5c413-175">Web サービスの応答を分析する</span><span class="sxs-lookup"><span data-stu-id="5c413-175">Analyze web service response</span></span>                 | <span data-ttu-id="5c413-176">Web サービスの応答を分析し、エラーログを返します。</span><span class="sxs-lookup"><span data-stu-id="5c413-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="5c413-177">Mexican PAC webサービスの URL を設定する</span><span class="sxs-lookup"><span data-stu-id="5c413-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="5c413-178">**機能のバージョン設定**  ページで、**アクション** タブの  **アクション** クイックタブで、**メキシコ向け PAC サービスの呼び出し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="5c413-179">**パラメーター** クイックタブの **URL アドレス パラメーター**  フィールドに、CFDI 電子請求書の提出に使用する webサービスの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c413-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="5c413-180">**取り消し** と **取り消し申請** 機能設定で使用する **メキシコ向け PAC サービス アクションの呼び出し** の URL を更新するには、同じ手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="5c413-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="5c413-181">電子請求書の環境に下書きのバージョンを割り当てる</span><span class="sxs-lookup"><span data-stu-id="5c413-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="5c413-182">**電子請求書機能** ページの **環境** タブで、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="5c413-183">**環境** フィールドで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="5c413-184">**有効開始** フィールドで、環境が有効になる日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="5c413-185">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-185">Select **Enable**.</span></span>

![電子請求書の環境を有効化する](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="5c413-187">バージョンの状態を完了に変更する</span><span class="sxs-lookup"><span data-stu-id="5c413-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="5c413-188">**電子請求書機能** ページの **バージョン** タブで、状態が **下書き** となっている電子請求書機能のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="5c413-189">**ステータスの変更 \> 完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="5c413-190">バージョンの状態を公開済みに変更する</span><span class="sxs-lookup"><span data-stu-id="5c413-190">Change the version status to Published</span></span>

- <span data-ttu-id="5c413-191">**電子請求機能**  ページの **バージョン** タブで、**状態の変更 \> 公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="5c413-192">電子請求書の機能を公開する</span><span class="sxs-lookup"><span data-stu-id="5c413-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="5c413-193">**電子請求書機能**  ページで、 **バージョン** タブを選択して、**CFDI 請求書 (MX)** 機能の状態を管理します。</span><span class="sxs-lookup"><span data-stu-id="5c413-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="5c413-194">**状態の変更** を選択して、機能の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="5c413-194">Select **Change status** to change the status of the feature.</span></span>

![電子請求書機能の状態を変更する](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a><span data-ttu-id="5c413-196">財務における電子請求統合を設定する</span><span class="sxs-lookup"><span data-stu-id="5c413-196">Set up Electronic invoicing  integration in Finance</span></span>

<span data-ttu-id="5c413-197">財務で電子請求を設定するには、次の作業を行う必要があります :</span><span class="sxs-lookup"><span data-stu-id="5c413-197">To set up Electronic invoicing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="5c413-198">ER データ モデル、ER データ モデル マッピング、および CFDI 請求書で必要となる形式をインポートします。</span><span class="sxs-lookup"><span data-stu-id="5c413-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="5c413-199">CFDI 請求書の更新に使用する応答タイプを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c413-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="5c413-200">これらの応答タイプは、認定証明書プロバイダー (PAC) サーバーからの応答に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="5c413-201">ER データ モデル、ERデータ モデル マッピング、CFDI 請求書で使用するコンテキスト構成をインポートする</span><span class="sxs-lookup"><span data-stu-id="5c413-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="5c413-202">財務にログインします。</span><span class="sxs-lookup"><span data-stu-id="5c413-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="5c413-203">**電子レポート** ワークスペースの、**構成プロバイダー** セクションで、**Microsoft** タイトルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="5c413-204">この構成プロバイダーが **有効** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="5c413-205">プロバイダーを **有効化** を設定する方法については、[構成プロバイダーを作成して有効化としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-205">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="5c413-206">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="5c413-207">**グローバル リソース \>  開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="5c413-208">**請求書モデル**、**請求書モデル マッピング**、**CFDI 請求書形式 (MX)**、**CFDI 請求書の取消申請の形式 (MX)**、**CFDI 請求書の取消形式 (MX)** をインポートします。</span><span class="sxs-lookup"><span data-stu-id="5c413-208">Import **Invoice model**, **Invoice model mapping**, **CFDI invoice format (MX)**, **CFDI invoice cancelation request format (MX)**, and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="5c413-209">CFDI の請求書の処理に使用する機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="5c413-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="5c413-210">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="5c413-211">**機能** タブで、**MX-00010** と **MX-00016** の機能参照のそれぞれの行の **有効** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5c413-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![CFDI の請求書の処理に使用する機能を有効にする](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="5c413-213">ER の構成をインポートして CFDI 請求書の更新に使用する応答タイプを設定する</span><span class="sxs-lookup"><span data-stu-id="5c413-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="5c413-214">ER コンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="5c413-214">Import ER configurations</span></span>

1. <span data-ttu-id="5c413-215">**電子レポート** ワークスペースの、**構成プロバイダー** セクションで、**Microsoft** タイトルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="5c413-216">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="5c413-217">**グローバル リソース \>  開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="5c413-218">**応答メッセージのインポート モデル**、**CFDI エラー ログ インポート (MX)**、**CFDI 応答メッセージのインポート (MX)** をインポートします。</span><span class="sxs-lookup"><span data-stu-id="5c413-218">Import **Response message model**, **CFDI error log import (MX)**, and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="5c413-219">応答タイプを設定する</span><span class="sxs-lookup"><span data-stu-id="5c413-219">Set up the response types</span></span>

1. <span data-ttu-id="5c413-220">**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="5c413-221">**電子ドキュメント** タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="5c413-222">顧客請求書仕訳帳を入力し、**テーブル名** フィールドでプロジェクト請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="5c413-223">各テーブルについて、関連するドキュメントのコンテキストを定義します :</span><span class="sxs-lookup"><span data-stu-id="5c413-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="5c413-224">**顧客請求書仕訳帳** に、**顧客請求書のコンテキスト** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c413-224">For **Customer invoice journal**, enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="5c413-225">**プロジェクト請求書** に、**プロジェクト請求書のコンテキスト** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c413-225">For **Project invoice**, enter **Project invoice context**.</span></span>

4. <span data-ttu-id="5c413-226">**応答タイプ** を選択して、電子請求から返され、顧客の請求書仕訳帳やプロジェクトの請求書に含まれる応答タイプを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c413-226">Select **Response types** to configure the response types that can be returned from Electronic invoicing and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="5c413-227">**新規** を選択し、続いて **応答タイプ** フィールドで、**応答** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-227">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="5c413-228">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="5c413-229">**モデル マッピング** フィールドで、**応答メッセージのインポート形式 - 応答メッセージからモデル マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="5c413-230">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-230">Select **Save**.</span></span>
9. <span data-ttu-id="5c413-231">**新規** を選択し、続いて **応答タイプ** フィールドで、**ResponseData** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-231">Select **New**, and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="5c413-232">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="5c413-233">**モデル マッピング** フィールドで、**CFDI 応答データのインポート形式 (詳細) - 応答データインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="5c413-234">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="5c413-235">財務での電子請求書の処理</span><span class="sxs-lookup"><span data-stu-id="5c413-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="5c413-236">財務における CFDI 請求書の処理中には、電子請求を使用して次のタスクを実行できます :</span><span class="sxs-lookup"><span data-stu-id="5c413-236">During the processing of CFDI invoices in Finance through Electronic invoicing, you can perform the following tasks:</span></span>

- <span data-ttu-id="5c413-237">CFDI 請求書を送信します。</span><span class="sxs-lookup"><span data-stu-id="5c413-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="5c413-238">送信の実行ログを表示する。</span><span class="sxs-lookup"><span data-stu-id="5c413-238">View the submission execution logs.</span></span>
- <span data-ttu-id="5c413-239">CFDI 請求書の取り消しを送信する。</span><span class="sxs-lookup"><span data-stu-id="5c413-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="5c413-240">CFDI 請求書の送信</span><span class="sxs-lookup"><span data-stu-id="5c413-240">Submit CFDI invoices</span></span>

<span data-ttu-id="5c413-241">**構成可能な電子請求の統合** 機能を有効化すると、CFDI 請求書の提出に使用する **電子請求書のエクスポート/インポート** 処理 (**売掛金勘定 \> 請求書 \> 電子請求書**) は使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="5c413-241">After you turn on the **Configurable Electronic invoicing integration** feature, the **Export/Import electronic invoice** process (**Accounts receivable \> Invoices \> E-invoices**) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="5c413-242">これは、**電子ドキュメントの送信** という名前の新しいプロセスによって置き換えられ ます。</span><span class="sxs-lookup"><span data-stu-id="5c413-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="5c413-243">新しい **電子ドキュメントの送信** プロセスを使用する前に、メキシコ向けの電子請求書に必要な設定が完了していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="5c413-244">詳細については、[CFDI レイアウト バージョン 3.3](./latam-mex-cfdi-3-3.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-244">For more information, see [CFDI layout version 3.3](./latam-mex-cfdi-3-3.md).</span></span>

1. <span data-ttu-id="5c413-245">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの送信** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="5c413-246">ドキュメントを初めて送信する場合は、必ず **ドキュメントの再送信** オプションを **いいえ** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="5c413-247">サービスを使用してドキュメントを再送信する必要がある場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5c413-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="5c413-248">**含めるレコード** クイックタブで、**フィルター** を選択して **照会** ダイアログ ボックスを開きます。ここでは送信するドキュメントを選択するクエリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5c413-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![CFDI ドキュメントの送信](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="5c413-250">このサービスを利用して初めて書類を提出する際は、電子請求との接続を確認するように促されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="5c413-251">**ここをクリックして電子ドキュメント送信サービスに接続する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="5c413-252">送信ログの表示</span><span class="sxs-lookup"><span data-stu-id="5c413-252">View submission logs</span></span>

<span data-ttu-id="5c413-253">すべての提出書類の提出ログ、または提出された提出書類のみのログを確認できます。</span><span class="sxs-lookup"><span data-stu-id="5c413-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="5c413-254">すべての提出ログを表示する</span><span class="sxs-lookup"><span data-stu-id="5c413-254">View all submission logs</span></span>

<span data-ttu-id="5c413-255">**構成可能な電子請求の統合** 機能を有効にすると、ドキュメントの提出プロセスをフォローする新しいページが利用可能となります。</span><span class="sxs-lookup"><span data-stu-id="5c413-255">After you turn on the **Configurable Electronic invoicing integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="5c413-256">このページを使用して全ての提出書類の提出ログを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="5c413-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="5c413-257">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="5c413-258">**ドキュメント タイプ**  フィールドで、**顧客請求書仕訳帳** を選択して必要な電子ドキュメントをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5c413-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![提出書類のログを表示するドキュメント タイプの選択](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="5c413-260">アクション ウィンドウで、**照会\> 提出の詳細** を選択して、提出実行ログの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="5c413-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![提出書類ログの詳細を表示する](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="5c413-262">提出書類ログの情報は、次の3つのクイック タブに分かれています :</span><span class="sxs-lookup"><span data-stu-id="5c413-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="5c413-263">**処理中のアクション** - このクイックタブでは、RCS で設定された機能のバージョンで構成されているアクションの実行ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="5c413-264">**状態** 列には、アクションが正常に実行されたかどうかが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="5c413-265">**アクション ファイル** - こクイックタブでは、アクションの実行中に生成された中間ファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="5c413-266">**表示** を選択する と、ファイルをダウンロードして表示できます。</span><span class="sxs-lookup"><span data-stu-id="5c413-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="5c413-267">**アクション ログの処理** - このクイックタブには、電子請求とターゲットの web サービスの間の通信結果が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-267">**Processing action log** – This FastTab shows the results of the communication between Electronic invoicing and the target web service.</span></span> <span data-ttu-id="5c413-268">また、web サービスからの処理によって返された内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="5c413-269">**エラーコード** 列には、web サービスの認証で返されたリターン コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="5c413-270">送信された CFDI 請求書が承認されると、その状態が **承認済** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="5c413-271">CFDI 請求書から送信ログを表示する</span><span class="sxs-lookup"><span data-stu-id="5c413-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="5c413-272">**構成可能な電子請求の統合** 機能を有効にすると、CFDI 請求書から提出書類のログを表示することも可能です。</span><span class="sxs-lookup"><span data-stu-id="5c413-272">After you turn on the **ConfigurableElectronic invoicing integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="5c413-273">**売掛金勘定 \> 照会およびレポート\> CFDI (電子請求書)** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="5c413-274">**設定可能な電子請求の統合** 機能が有効にした後に送信された CFDI 請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>
3. <span data-ttu-id="5c413-275">アクション ウィンドウの **履歴** タブで、**電子ドキュメント ログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![CFDI 請求書から送信ログを表示する](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="5c413-277">**構成可能な電子請求の統合** 機能が有効になる前に送信された請求書の場合は、**履歴** ボタンを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5c413-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="5c413-278">**構成可能な電子請求の統合** 機能が有効になった後に送信された請求書の場合は、**履歴** ボタンは使用できません。</span><span class="sxs-lookup"><span data-stu-id="5c413-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="5c413-279">CFDI 請求書の取り消しを送信する</span><span class="sxs-lookup"><span data-stu-id="5c413-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="5c413-280">**構成可能な電子請求の統合** 機能を有効化すると、CFDI 請求書の取り消しに使用する従来のプロセスが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="5c413-280">After you turn on the **Configurable Electronic invoicing integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="5c413-281">**電子ドキュメントの送信ログ** ページに埋め込まれた新しい取り消しプロセスに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="5c413-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="5c413-282">**売掛金勘定 \> 照会およびレポート\> CFDI (電子請求書)** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="5c413-283">CFDI 請求書の状態が **承認済** の場合は、**機能 \> CFDI の取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-283">If the CFDI invoice has a status of **Approved**, select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="5c413-284">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="5c413-285">CFDI 請求書を選択し、**機能 \> 関連する提出書類を送信する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="5c413-286">提出に関する説明を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="5c413-287">すべての取り消し提出ログを表示する</span><span class="sxs-lookup"><span data-stu-id="5c413-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="5c413-288">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c413-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="5c413-289">**ドキュメント タイプ**  フィールドで、**顧客請求書仕訳帳** を選択し、顧客請求書仕訳帳ドキュメントをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="5c413-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="5c413-290">CFDI 請求書を選択し、アクション ウィンドウで、**照会 \> 関連する提出書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c413-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="5c413-291">**関連する提出書類** ページには、特定の CFDI 請求書に関連する提出書類とその提出書類の状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="5c413-292">次の図では、最初の行は、CFDI 請求書の承認を要求する提出書類を表します。</span><span class="sxs-lookup"><span data-stu-id="5c413-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="5c413-293">2 行目は、その CFDI 請求書を取り消しした提出書類を表します。</span><span class="sxs-lookup"><span data-stu-id="5c413-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![取り消し提出ログを表示する](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="5c413-295">アクション ウィンドウで、**照会\> 提出の詳細** を選択して、提出実行ログの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="5c413-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![提出書類の取り消しログの詳細を表示する](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="5c413-297">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="5c413-297">Privacy notice</span></span>
<span data-ttu-id="5c413-298">**CFDI メキシコの電子請求 (MX)** 機能を有効にするには、組織の税務登録 ID を含む一部のデータの送信が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5c413-298">Enabling the **CFDI Mexican electronic invoice (MX)** feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="5c413-299">これは、政府の web サービスとの統合に必要な所定の形式で、この税務当局に電子請求書を送信する目的で、税務当局から権限を与えられた第三者機関に送信されます。</span><span class="sxs-lookup"><span data-stu-id="5c413-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="5c413-300">管理者は、**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動して、**CFDI メキシコの電子請求 (MX)** 機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5c413-300">An administrator can enable and disable the **CFDI Mexican electronic invoice (MX)** feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="5c413-301">**機能** タブを選択し、**CFDI メキシコの電子請求 (MX)** 機能を含む行を選択して、適切な選択を行います。</span><span class="sxs-lookup"><span data-stu-id="5c413-301">Select the **Features** tab, select the rows containing the **CFDI Mexican electronic invoice (MX)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="5c413-302">これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="5c413-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="5c413-303">詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5c413-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c413-304">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5c413-304">Additional resources</span></span>

- [<span data-ttu-id="5c413-305">電子請求の概要</span><span class="sxs-lookup"><span data-stu-id="5c413-305">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="5c413-306">電子請求の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="5c413-306">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="5c413-307">電子請求の設定</span><span class="sxs-lookup"><span data-stu-id="5c413-307">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
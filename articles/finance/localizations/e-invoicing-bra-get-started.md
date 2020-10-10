---
title: ブラジル向け電子請求のアドオンの使用を開始する
description: このトピックでは、ブラジル における Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management の電子請求のアドオンを使い始める際に役立つ情報を提供します。
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835992"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="9c75c-103">ブラジル向け電子請求のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="9c75c-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="9c75c-104">ブラジル向けの電子請求書アドオンは、現在のところ、Microsoft Dynamics 365 Finance や Dynamics 365 Supply Chain Management に組み込まれている会計文書の統合で利用できる機能のすべてに対応していません。</span><span class="sxs-lookup"><span data-stu-id="9c75c-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="9c75c-105">このトピックでは、ブラジ向け電子請求書作成アドオンの使用を開始するにあたっての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="9c75c-106">このガイドでは、Regulatory Configuration Services (RCS) 、財務、Supply Chain Management における、国ごとに異なる構成手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="9c75c-107">また、サービスを通じて NF-E 会計ドキュメント (電子請求書ドキュメントモデル 55) を提出するプロセス、および処理結果と会計ドキュメントの状態を確認する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9c75c-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="9c75c-108">Prerequisites</span></span>

<span data-ttu-id="9c75c-109">このトピックの手順を実行する前に、 [電子請求アドオンを使用する](e-invoicing-get-started.md)に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="9c75c-110">RCS の設定</span><span class="sxs-lookup"><span data-stu-id="9c75c-110">RCS setup</span></span>

<span data-ttu-id="9c75c-111">RCS の設定を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="9c75c-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="9c75c-112">NF-E 会計ドキュメントで使用する電子請求書機能をインポートします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="9c75c-113">NF-e 会計書類を提出して承認を得るために必要となるファイル形式を確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="9c75c-114">承認された NF-e の取消申請に必要となるファイル形式を確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="9c75c-115">NF-e 会計書類を提出して承認を得るために必要となるイベントを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="9c75c-116">承認された NF-e の取消申請を行うために必要となるイベントを構成します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="9c75c-117">電子請求書作成アドオン環境に電子請求書機能を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="9c75c-118">電子請求書機能を公開する。</span><span class="sxs-lookup"><span data-stu-id="9c75c-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="9c75c-119">"電子請求のアドオン機能" は、電子請求書のアドオン サーバーを使用するように構成および公開されたリソースの総称です。</span><span class="sxs-lookup"><span data-stu-id="9c75c-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="9c75c-120">電子請求書機能の設定では、電子申告 (ER) 構成フォーマットを使用して設定可能なエクスポートおよびインポートファイルを作成し、アクションおよびアクション フローを使用して、リクエストの送信、応答のインポート、応答内容の解析に設定可能なルールの作成を可能にするなどの機能が組み合わされています。</span><span class="sxs-lookup"><span data-stu-id="9c75c-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="9c75c-121">電子請求書機能をインポートする</span><span class="sxs-lookup"><span data-stu-id="9c75c-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="9c75c-122">RCS アカウントにサインインします</span><span class="sxs-lookup"><span data-stu-id="9c75c-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="9c75c-123">**グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求書** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="9c75c-124">**電子請求書機能** ページで、**インポート** を選択して、グローバルレポジトリから  NF-e  の会計ドキュメントの電子請求機能をインポートします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![ボタンのインポート](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="9c75c-126">NF-E 会計ドキュメント機能を選択し、**インポート** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![NF-e 機能のインポート](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="9c75c-128">NF-e 会計ドキュメント機能の新しいバージョンを作成する</span><span class="sxs-lookup"><span data-stu-id="9c75c-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="9c75c-129">**電子請求機能** ページの **バージョン** タブで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![新しい電子請求書機能のバージョンを追加する](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="9c75c-131">構成のバージョンを更新する</span><span class="sxs-lookup"><span data-stu-id="9c75c-131">Update the configuration version</span></span>

1. <span data-ttu-id="9c75c-132">**電子請求機能** ページの**構成**タブで、**追加** または **削除** を選択して、構成のバージョン (ER ファイル形式の構成) を管理します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![電子請求書機能の構成を管理する](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="9c75c-134">NF-e 会計文書機能の新しいバージョンを作成すると、すべての構成バージョン (ERファイル形式) が最新バージョンから継承されます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="9c75c-135">NF-e 会計文書を提出して承認を得るには、以下の構成バージョンが必要です :</span><span class="sxs-lookup"><span data-stu-id="9c75c-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="9c75c-136">NFe 送信エクスポートの形式</span><span class="sxs-lookup"><span data-stu-id="9c75c-136">NFe submit export format</span></span>
        - <span data-ttu-id="9c75c-137">NFe 応答メッセージのインポート</span><span class="sxs-lookup"><span data-stu-id="9c75c-137">NFe response message import</span></span>
        - <span data-ttu-id="9c75c-138">NFe エラー ログのインポート</span><span class="sxs-lookup"><span data-stu-id="9c75c-138">NFe error log import</span></span>

    - <span data-ttu-id="9c75c-139">NF-e の取り消しを提出するには、次の構成バージョンが必要です :</span><span class="sxs-lookup"><span data-stu-id="9c75c-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="9c75c-140">NFe 取り消しエクスポートの形式</span><span class="sxs-lookup"><span data-stu-id="9c75c-140">NFe cancel export format</span></span>

2. <span data-ttu-id="9c75c-141">一覧で構成バージョンを選択し、**編集**または **表示**を選択すると、**形式デザイナ** ページが表示されます。このページで、構成の編集や表示をすることができます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![形式デザイナー ページを開く](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="9c75c-143">**形式デザイナー**ページを使用して、ER 形式ファイルの構成を編集、確認します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="9c75c-144">詳細については、[電子ドキュメントのコンフィギュレーションの作成](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![形式デザイナーのページ](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="9c75c-146">電子請求書機能の設定を管理する</span><span class="sxs-lookup"><span data-stu-id="9c75c-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="9c75c-147">**電子請求機能** ページの**設定**タブで、**追加** または **削除** を選択して、電子請求機能の設定 (NF-e イベント) を管理します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![電子請求書機能の設定を管理する](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="9c75c-149">その他の電子請求機能から派生した NF-e 会計ドキュメント機能の新しいバージョンを作成すると、すべての機能設定 (NF-eイベント) が最新バージョンから継承されます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="9c75c-150">NF-e の会計書類を提出して承認を得るには、**提出**機能の設定が必要となります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="9c75c-151">NF-e の取り消しを提出するには、**取り消し**機能の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="9c75c-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="9c75c-152">提出機能の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="9c75c-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="9c75c-153">**電子請求機能** ページ上の **設定**タブで、**機能の設定** 列で、**提出**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="9c75c-154">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-154">Select **Edit**.</span></span>

    ![電子請求書機能の設定を編集する](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="9c75c-156">**機能のバージョン設定**ページで、**アクション**タブを選択してアクションの一覧を管理します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![アクション タブ](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="9c75c-158">NF-e 会計書類を提出して承認を得るために必要となるアクションを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="9c75c-159">アクション ID</span><span class="sxs-lookup"><span data-stu-id="9c75c-159">Action ID</span></span> | <span data-ttu-id="9c75c-160">アクション名</span><span class="sxs-lookup"><span data-stu-id="9c75c-160">Action name</span></span>                  | <span data-ttu-id="9c75c-161">アクション説明</span><span class="sxs-lookup"><span data-stu-id="9c75c-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="9c75c-162">1</span><span class="sxs-lookup"><span data-stu-id="9c75c-162">1</span></span>         | <span data-ttu-id="9c75c-163">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="9c75c-163">Transform document</span></span>           | <span data-ttu-id="9c75c-164">提出に使用する NF-e XML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="9c75c-165">2</span><span class="sxs-lookup"><span data-stu-id="9c75c-165">2</span></span>         | <span data-ttu-id="9c75c-166">ドキュメントに署名</span><span class="sxs-lookup"><span data-stu-id="9c75c-166">Sign document</span></span>                | <span data-ttu-id="9c75c-167">XML ファイルにデジタル証明書を適用します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="9c75c-168">3</span><span class="sxs-lookup"><span data-stu-id="9c75c-168">3</span></span>         | <span data-ttu-id="9c75c-169">ブラジル SEFAZ サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="9c75c-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="9c75c-170">署名された XML ファイルを web サービスに提出して承認を得ます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="9c75c-171">4</span><span class="sxs-lookup"><span data-stu-id="9c75c-171">4</span></span>         | <span data-ttu-id="9c75c-172">応答の処理</span><span class="sxs-lookup"><span data-stu-id="9c75c-172">Process response</span></span>             | <span data-ttu-id="9c75c-173">Web サービスの応答を取得する。</span><span class="sxs-lookup"><span data-stu-id="9c75c-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="9c75c-174">5</span><span class="sxs-lookup"><span data-stu-id="9c75c-174">5</span></span>         | <span data-ttu-id="9c75c-175">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="9c75c-175">Transform document</span></span>           | <span data-ttu-id="9c75c-176">応答として受信したファイルの内容を解析します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="9c75c-177">6</span><span class="sxs-lookup"><span data-stu-id="9c75c-177">6</span></span>         | <span data-ttu-id="9c75c-178">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="9c75c-178">Transform document</span></span>           | <span data-ttu-id="9c75c-179">提出状態の問い合わせに使用する XML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="9c75c-180">7</span><span class="sxs-lookup"><span data-stu-id="9c75c-180">7</span></span>         | <span data-ttu-id="9c75c-181">ブラジル SEFAZ サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="9c75c-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="9c75c-182">提出状態を要求する XML ファイルを送信します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="9c75c-183">8</span><span class="sxs-lookup"><span data-stu-id="9c75c-183">8</span></span>         | <span data-ttu-id="9c75c-184">応答の処理</span><span class="sxs-lookup"><span data-stu-id="9c75c-184">Process response</span></span>             | <span data-ttu-id="9c75c-185">Web サービスの応答を取得する。</span><span class="sxs-lookup"><span data-stu-id="9c75c-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="9c75c-186">SEFAZ webサービスの URL を設定する</span><span class="sxs-lookup"><span data-stu-id="9c75c-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="9c75c-187">**機能のバージョン設定** ページで、**アクション** タブの **アクション**クイックタブで、**ブラジルの SEFAZ サービスの呼び出し**(アクションID  **3**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="9c75c-188">**パラメーター** クイックタブの**URL アドレス パラメーター**  フィールドに、NF-e の提出に使用する SEFAZ webサービスの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="9c75c-189">**アクション** クイックタブで、**ブラジルの SEFAZ サービスの呼び出し** (アクション ID **7**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7**).</span></span>
4. <span data-ttu-id="9c75c-190">**パラメーター** クイックタブの**URL アドレス パラメーター**  フィールドに、NF-e の提出に使用する SEFAZ webサービスの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="9c75c-191">取り消し機能の設定を構成する</span><span class="sxs-lookup"><span data-stu-id="9c75c-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="9c75c-192">**電子請求機能** ページ上の **設定**タブで、**機能の設定** 列で、**取り消し**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="9c75c-193">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-193">Select **Edit**.</span></span>
3. <span data-ttu-id="9c75c-194">**機能のバージョン設定**ページで、**アクション**タブを選択してアクションの一覧を管理します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="9c75c-195">承認された NF-e の取消申請に必要となるアクションを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="9c75c-196">アクション ID</span><span class="sxs-lookup"><span data-stu-id="9c75c-196">Action ID</span></span> | <span data-ttu-id="9c75c-197">アクション名</span><span class="sxs-lookup"><span data-stu-id="9c75c-197">Action name</span></span>                  | <span data-ttu-id="9c75c-198">アクション説明</span><span class="sxs-lookup"><span data-stu-id="9c75c-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="9c75c-199">1</span><span class="sxs-lookup"><span data-stu-id="9c75c-199">1</span></span>         | <span data-ttu-id="9c75c-200">ドキュメントの変換</span><span class="sxs-lookup"><span data-stu-id="9c75c-200">Transform document</span></span>           | <span data-ttu-id="9c75c-201">取り消しに使用する NF-e XML ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="9c75c-202">2</span><span class="sxs-lookup"><span data-stu-id="9c75c-202">2</span></span>         | <span data-ttu-id="9c75c-203">ドキュメントに署名</span><span class="sxs-lookup"><span data-stu-id="9c75c-203">Sign document</span></span>                | <span data-ttu-id="9c75c-204">XML ファイルにデジタル証明書を適用します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="9c75c-205">3</span><span class="sxs-lookup"><span data-stu-id="9c75c-205">3</span></span>         | <span data-ttu-id="9c75c-206">ブラジル SEFAZ サービスの呼び出し</span><span class="sxs-lookup"><span data-stu-id="9c75c-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="9c75c-207">署名された XML ファイルを web サービスに提出して取り消しをします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="9c75c-208">4</span><span class="sxs-lookup"><span data-stu-id="9c75c-208">4</span></span>         | <span data-ttu-id="9c75c-209">応答の処理</span><span class="sxs-lookup"><span data-stu-id="9c75c-209">Process response</span></span>             | <span data-ttu-id="9c75c-210">Web サービスの応答を取得する。</span><span class="sxs-lookup"><span data-stu-id="9c75c-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="9c75c-211">SEFAZ webサービスの URL を設定する</span><span class="sxs-lookup"><span data-stu-id="9c75c-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="9c75c-212">**機能のバージョン設定** ページで、**アクション** タブの **アクション**クイックタブで、**ブラジルの SEFAZ サービスの呼び出し**(アクションID  **3**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3**).</span></span>
2. <span data-ttu-id="9c75c-213">**パラメーター** クイックタブの**URL アドレス パラメーター**  フィールドに、承認済み NF-e の取り消しを行う SEFAZ webサービスの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="9c75c-214">電子請求書の環境を有効にして下書きのバージョンを割り当てる</span><span class="sxs-lookup"><span data-stu-id="9c75c-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="9c75c-215">**電子請求書機能** ページの **環境** タブで、**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="9c75c-216">**環境**フィールドで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="9c75c-217">**有効開始** フィールドで、環境が有効になる日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="9c75c-218">**有効化** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-218">Select **Enable**.</span></span>

![電子請求書の環境を有効化する](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="9c75c-220">状態を完了に変更する</span><span class="sxs-lookup"><span data-stu-id="9c75c-220">Change the status to Completed</span></span>

1. <span data-ttu-id="9c75c-221">**電子請求書機能** ページの **バージョン**タブで、状態が**下書き** となっている電子請求書機能のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="9c75c-222">**ステータスの変更 \> 完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="9c75c-223">状態を公開に変更する</span><span class="sxs-lookup"><span data-stu-id="9c75c-223">Change the status to Publish</span></span>

1. <span data-ttu-id="9c75c-224">**電子請求書機能** ページの **バージョン**タブで、状態が**完了** となっている電子請求書機能のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="9c75c-225">**状態の変更 \> 公開**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-225">Select **Change status \> Publish**.</span></span>

![電子請求書機能を公開する](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="9c75c-227">財務や Supply Chain Management における電子請求書のアドオン統合を設定する</span><span class="sxs-lookup"><span data-stu-id="9c75c-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="9c75c-228">設定を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="9c75c-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="9c75c-229">ブラジル向け NF-e 連邦機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="9c75c-230">特定の ER データ モデル、データ モデル マッピング、NF-e 会計ドキュメントに必要な形式をインポートします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="9c75c-231">ER の構成をインポートし、送信プロセスが返された後に会計ドキュメントの状態を更新するために必要となる応答タイプを設定します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="9c75c-232">ブラジル向け NF-e 連邦機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="9c75c-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="9c75c-233">**組織管理 \> 設定 \> 電子ドキュメント パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="9c75c-234">**機能** タブで、機能参照**BR00053**行の **有効** チェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="9c75c-235">NF-e 会計ドキュメントに必要となる ER データ モデル マッピングをインポートする</span><span class="sxs-lookup"><span data-stu-id="9c75c-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="9c75c-236">財務にログインします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="9c75c-237">**電子レポート**ワークスペースの、**構成プロバイダー**セクションで、**Microsoft**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="9c75c-238">この構成プロバイダーが**有効**に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="9c75c-239">プロバイダーを**有効化**を設定する方法については、[構成プロバイダーを作成して有効化としてマークする](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-239">For information about how to set a provider to **Active**, see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="9c75c-240">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="9c75c-241">**グローバル リソース \>  開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="9c75c-242">**会計ドキュメントのマッピング**構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="9c75c-243">ER構成をインポートして会計ドキュメントの応答タイプを設定する</span><span class="sxs-lookup"><span data-stu-id="9c75c-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="9c75c-244">**電子レポート**ワークスペースの、**構成プロバイダー**セクションで、**Microsoft**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="9c75c-245">**リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="9c75c-246">**グローバル リソース \>  開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="9c75c-247">**NF-e エラーログのインポート (BR)**、**NF-e 応答データのインポート形式 (BR)**、および**NF-e 応答メッセージのインポート (BR)** をインポートします。</span><span class="sxs-lookup"><span data-stu-id="9c75c-247">Import **NF-e error log import (BR)**, **NF-e response data import format (BR)**, and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="9c75c-248">**組織管理 \> 設定 \> 電子ドキュメント パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="9c75c-249">**電子ドキュメント** タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="9c75c-250">**テーブル名**フィールドに、**会計ドキュメント ヘッダー**を入力し ます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="9c75c-251">**ドキュメント コンテキスト**フィールドで、**顧客請求書コンテキスト モデル - 会計ドキュメントのコンテキスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="9c75c-252">**応答タイプ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-252">Select **Response types**.</span></span>
9. <span data-ttu-id="9c75c-253">**新規**を選択し、続いて**応答タイプ**フィールドで、**応答** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-253">Select **New**, and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="9c75c-254">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="9c75c-255">**モデル マッピング** フィールドで、**応答メッセージのインポート形式 - 応答メッセージからモデル マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="9c75c-256">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-256">Select **Save**.</span></span>
13. <span data-ttu-id="9c75c-257">**新規**を選択し、続いて**応答タイプ**フィールドで、**ResponseData** と入力します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-257">Select **New**, and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="9c75c-258">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="9c75c-259">**モデル マッピング** フィールドで、**NFe 応答データのインポート形式 - 応答データインポート**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="9c75c-260">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="9c75c-261">電子請求書の処理</span><span class="sxs-lookup"><span data-stu-id="9c75c-261">Electronic invoice processing</span></span>

<span data-ttu-id="9c75c-262">財務の処置を行う際には、次の作業を実行します :</span><span class="sxs-lookup"><span data-stu-id="9c75c-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="9c75c-263">電子請求書のアドオンを使用して会計ドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="9c75c-264">送信の実行ログを表示し、処理の結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="9c75c-265">電子請求書アドオンを使用して会計書類の取り消しを送信します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="9c75c-266">SEFAZ 承認用の NF-e 会計ドキュメントを送信する</span><span class="sxs-lookup"><span data-stu-id="9c75c-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="9c75c-267">**構成可能な電子請求書作成アドオンの統合**機能を有効化すると、NF-e 会計書類を提出して承認を得る (**エクスポート/インポート NF-e プロセス**) 従来のプロセスが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization (**Export/Import NF-e process**) can no longer be used.</span></span> <span data-ttu-id="9c75c-268">これは、**電子ドキュメントの送信** という名前の新しいプロセスによって置き換えられ ます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="9c75c-269">続行する前に、顧客の会計事務所が発行した顧客の会計書類モデル 55 が 1 つ以上あることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="9c75c-270">これらの会計ドキュメントの方向は **発信** に設定されている必要があり、状態を**作成**する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-270">The direction for these fiscal documents must be set to **Outgoing**, and the status must be **Created**.</span></span> <span data-ttu-id="9c75c-271">詳細については、[顧客会計ドキュメントの発行 (ブラジル)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="9c75c-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="9c75c-272">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの送信**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="9c75c-273">ドキュメントを初めて送信する場合は、必ず**ドキュメントの再送信** オプションを **いいえ** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="9c75c-274">サービスを使用してドキュメントを再送信する必要がある場合は、このオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="9c75c-275">**含めるレコード** クイックタブで、**フィルター**を選択して**照会**ダイアログ ボックスを開きます。ここでは送信するドキュメントを選択するクエリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="9c75c-276">**範囲** タブで **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="9c75c-277">**テーブル名**フィールドに、**会計ドキュメント ヘッダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="9c75c-278">**派生テーブル**フィールドに、**会計ドキュメント ヘッダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="9c75c-279">**フィールド** フィールドで、**番号**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="9c75c-280">**基準** フィールドに、送信する必要のある会計ドキュメントの番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="9c75c-281">**OK** を選択して**照会**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="9c75c-282">**OK** を選択し、選択したドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="9c75c-283">このサービスを利用して初めて書類を提出する際は、電子請求書アドオンとの接続を確認するように促されます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="9c75c-284">**ここをクリックして電子ドキュメント送信サービスに接続する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="9c75c-285">すべての提出ログを表示する</span><span class="sxs-lookup"><span data-stu-id="9c75c-285">View all submission logs</span></span>

<span data-ttu-id="9c75c-286">**構成可能な電子請求書作成アドオンの統合**機能を有効にすると、ドキュメントの提出プロセスをフォローする新しいページが利用可能となります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="9c75c-287">このページを使用して全ての提出書類の提出ログを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="9c75c-288">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="9c75c-289">**ドキュメント タイプ** フィールドで、**会計ドキュメントのヘッダー**を選択して会計ドキュメントのみをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="9c75c-290">アクション ウィンドウで、**照会\> 提出の詳細**を選択して、提出実行ログの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![提出書類ログの詳細を表示する](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="9c75c-292">NF-e 会計ドキュメントの場合、**エラーコード**列には SEFAZ web サービスによって返されたリターン コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="9c75c-293">会計ドキュメント ページを介して提出ログを表示する</span><span class="sxs-lookup"><span data-stu-id="9c75c-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="9c75c-294">**構成可能な電子請求書作成アドオンの統合**機能を有効にすると、会計ドキュメント ページを介して提出書類のログを表示することも可能です。</span><span class="sxs-lookup"><span data-stu-id="9c75c-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="9c75c-295">**一般会計 \> 照会とレポート \> 会計ドキュメント \> すべての会計ドキュメント**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="9c75c-296">電子請求アドオンで以前に送信された会計ドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="9c75c-297">アクション ウィンドウの **NF-e 連邦** タブで、**電子ドキュメント ログ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![会計ドキュメント ページから提出ログを表示する](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="9c75c-299">SEFAZ 取り消しに使用する承認済の NF-e 会計ドキュメントを送信する</span><span class="sxs-lookup"><span data-stu-id="9c75c-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="9c75c-300">**構成可能な電子請求書作成アドオンの統合** 機能を有効化すると、NF-e 会計書類の取り消しに使用する従来のプロセスが使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="9c75c-301">**電子ドキュメントの送信ログ** ページに埋め込まれた新しい取り消しプロセスに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="9c75c-302">承認済の NF-e 会計ドキュメントの顧客会計文書の取消が実行されたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="9c75c-303">詳細については、[顧客会計ドキュメントの取り消し (ブラジル)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="9c75c-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="9c75c-304">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="9c75c-305">会計ドキュメントを選択し、**機能 \> 関連する提出書類を送信する**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="9c75c-306">提出に関する説明を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="9c75c-307">すべての取り消し提出ログを表示する</span><span class="sxs-lookup"><span data-stu-id="9c75c-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="9c75c-308">**組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="9c75c-309">**ドキュメント タイプ** フィールドで、**会計ドキュメントのヘッダー**を選択して会計ドキュメントのみをフィルタ処理します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="9c75c-310">会計ドキュメントを選択し、アクション ウィンドウで、**照会 \> 関連する提出書類**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="9c75c-311">関連する提出書類は、最初に作成された主要な提出書類に関連付けられている提出書類です。</span><span class="sxs-lookup"><span data-stu-id="9c75c-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="9c75c-312">たとえば、特定の NF-e を承認する提出書類は、メインの提出書類です。</span><span class="sxs-lookup"><span data-stu-id="9c75c-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="9c75c-313">SEFAZ 内の同一の NF-e の取り消しを要求する提出書類は、関連付けられている提出書類です。</span><span class="sxs-lookup"><span data-stu-id="9c75c-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="9c75c-314">これは、別の提出書類を通じて行われたジョブの取り消しを申請している場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="9c75c-315">**関連する提出書類** ページには、特定の会計ドキュメントに関連する提出書類とその提出書類の状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="9c75c-316">次の図では、最初の行は、会計ドキュメントの承認を要求する提出書類を表します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="9c75c-317">2 行目は、その会計ドキュメントを取り消しした提出書類を表します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![取り消し提出ログを表示する](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="9c75c-319">アクション ウィンドウで、**照会\> 提出の詳細**を選択して、提出実行ログの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="9c75c-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![提出書類の取り消しログの詳細を表示する](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="9c75c-321">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="9c75c-321">Privacy notice</span></span>
<span data-ttu-id="9c75c-322">BR-00053 (NF-e 連邦) 機能を有効にすると、組織の税務登録 ID を含む、一部のデータを送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="9c75c-323">これは、政府の web サービスとの統合に必要な所定の形式で、この税務当局に電子請求書を送信する目的で、税務当局から権限を与えられた第三者機関に送信されます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="9c75c-324">管理者は、**組織管理 \> 設定 \>電子ドキュメント パラメータ**に移動して、BR-00053 (NF-e 連邦) 機能を有効、または無効にすることができ ます。</span><span class="sxs-lookup"><span data-stu-id="9c75c-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="9c75c-325">**機能** タブを選択し 、BR-00053 機能が含まれている行を選択して、適切な選択を行います。</span><span class="sxs-lookup"><span data-stu-id="9c75c-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="9c75c-326">これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="9c75c-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="9c75c-327">詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c75c-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="9c75c-328">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9c75c-328">Additional resources</span></span>

- [<span data-ttu-id="9c75c-329">電子請求書アドオン機能の概要</span><span class="sxs-lookup"><span data-stu-id="9c75c-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="9c75c-330">電子請求書のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="9c75c-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="9c75c-331">電子請求のアドオン設定</span><span class="sxs-lookup"><span data-stu-id="9c75c-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)

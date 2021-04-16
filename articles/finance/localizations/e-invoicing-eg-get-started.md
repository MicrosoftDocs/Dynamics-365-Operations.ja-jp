---
title: エジプト向けの電子請求を開始する
description: このトピックでは、Finance および Supply Chain Management でエジプト向けの電子請求を使い始めるための情報を提供します。
author: gionoder
ms.date: 03/29/2021
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
ms.openlocfilehash: f6175a50a88d2d636bfafc5988265b8657630758
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840199"
---
# <a name="get-started-with-electronic-invoicing-for-egypt"></a><span data-ttu-id="bba12-103">エジプト向けの電子請求を開始する</span><span class="sxs-lookup"><span data-stu-id="bba12-103">Get started with Electronic invoicing for Egypt</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="bba12-104">このトピックでは、エジプト向けの電子請求を使い始めるための情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="bba12-104">This topic provides information that will help you get started with Electronic invoicing for Egypt.</span></span> <span data-ttu-id="bba12-105">このトピックでは、RCS (Regulatory Configuration Services) の国別の設定手順を説明し、[電子請求を開始する](e-invoicing-get-started.md)で説明されている手順を補完しています。</span><span class="sxs-lookup"><span data-stu-id="bba12-105">The topic guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS), and complement the steps described in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a><span data-ttu-id="bba12-106">エジプトの電子請求 (EG) 機能の国別コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bba12-106">Country-specific configuration for Egyptian electronic invoice (EG) Electronic invoicing feature</span></span>

<span data-ttu-id="bba12-107">**エジプト請求書 (EG) 電子請求機能** のパラメーターの一部は、既定値で公開されます。</span><span class="sxs-lookup"><span data-stu-id="bba12-107">Some of the parameters from the **Egyptian electronic invoice (EG) Electronic invoicing feature** are published with default values.</span></span> <span data-ttu-id="bba12-108">サービス環境に電子請求機能を導入する前に、値を確認し、業務処理のニーズをより反映するように更新してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-108">Review the values and if necessary, update the values to better reflect your business operation before you deploy the Electronic invoicing feature to the Service environment.</span></span>

<span data-ttu-id="bba12-109">このセクションは、トピック [電子請求を開始する](e-invoicing-get-started.md)の **電子請求機能の国別構成** セクションを補完するものです。</span><span class="sxs-lookup"><span data-stu-id="bba12-109">This section complements the **Country-specific configuration for Electronic invoicing feature** section in the topic [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="bba12-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="bba12-110">Prerequisites</span></span>

<span data-ttu-id="bba12-111">このセクションの手順を完了する前に、以下のことを行います。</span><span class="sxs-lookup"><span data-stu-id="bba12-111">Before you complete the procedure in this section, you must:</span></span>

- <span data-ttu-id="bba12-112">[電子請求サービス管理を開始する](e-invoicing-get-started-service-administration.md)の **デジタル証明書シークレットを作成する** セクションの説明に従って、デジタル証明書シークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="bba12-112">Create a digital certificate secret, as described in the **Create digital certificate secret** section in [Get started with Electronic invoicing service administration](e-invoicing-get-started-service-administration.md).</span></span> <span data-ttu-id="bba12-113">テストの目的で、エジプトの税務当局は、テストおよびソリューション検証フェーズでのみ使用する必要がある特定のテスト デジタル証明書を提供しています。</span><span class="sxs-lookup"><span data-stu-id="bba12-113">For testing purposes, the Egyptian tax authority provides specific test digital certificates that must be used only during testing and solution validation phases.</span></span> <span data-ttu-id="bba12-114">詳細については、[エジプト電子請求 SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) のリンクを使って、エジプト勢当局 Web サイトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-114">For more information, consult the Egyptian tax authority website using the link provided in the [Egyptian e-invoicing SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).</span></span>

1. <span data-ttu-id="bba12-115">RCS の **グローバリゼーション機能** ワークスペースの **機能** セクションで、 **電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-115">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="bba12-116">**電子請求機能** ページで、作成した **エジプト電子請求 (EG)** 電子請求機能が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bba12-116">On the **Electronic invoicing Features** page, verify that the **Egyptian electronic invoice (EG)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="bba12-117">**バージョン** タブで、**ドラフト** バージョンが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bba12-117">On the **Versions** tab, verify the **Draft** version is selected.</span></span>
4. <span data-ttu-id="bba12-118">グリッドの **設定** タブで、**売上請求書** 機能の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-118">On the **Setups** tab, in the grid, select **Sales invoice** feature setup.</span></span>
5. <span data-ttu-id="bba12-119">**編集** を選択し、**アクション** フィールド グループの **アクション** タブで、**エジプト税務当局に向けた json 文書に署名する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-119">Select **Edit**, and on the **Actions** tab in the **Actions** field group, select **Sign json document for Egyptian Tax Authority**.</span></span>
6. <span data-ttu-id="bba12-120">**パラメーター** フィールド グループでパラメーター **証明書名** を選択し、電子請求機能で使用するために作成されたデジタル証明書の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-120">In the **Parameters** field group, select the parameter, **Certificate name** and select the name of the digital certificate created to use with the Electronic invoicing feature.</span></span>
7. <span data-ttu-id="bba12-121">**アクション** フィールド グループで、**エジプト ETA サービスとの統合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-121">In the **Actions** field group, select **Integrate with Egyptian ETA service**.</span></span> <span data-ttu-id="bba12-122">このアクションが 2 回発生した場合は、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="bba12-122">Repeat this step for the two occurrences of this action.</span></span>
8. <span data-ttu-id="bba12-123">**パラメーター** フィールド グループで、**Web サービス URL** および **ログイン サービス URL** を選択し、必要に応じて URL パラメーターを確認してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-123">In the **Parameters** field group, select **Web service URL** and **Login service URL** and, if necessary, review the URL parameters.</span></span> <span data-ttu-id="bba12-124">[エジプトの電子請求の SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) で提供されているリンクを使用して、エジプトの税務当局の Web サイトを参照し、テストおよび実稼働の URL を取得してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-124">Consult the Egyptian tax authority website to get the Testing and Production URL, using the link provided in the [Egyptian e-invoicing SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).</span></span>
9. <span data-ttu-id="bba12-125">**保存** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bba12-125">Select **Save** and close the page.</span></span>
10. <span data-ttu-id="bba12-126">電子請求機能をサービス環境にデプロイするには、[電子請求を開始する](e-invoicing-get-started.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-126">To deploy the Electronic invoicing feature to the Service environment, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a><span data-ttu-id="bba12-127">エジプトの電子請求 (EG) 機能のアプリケーション設定の国別コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="bba12-127">Country-specific configuration of the application setup for the Egyptian electronic invoice (EG) Electronic invoicing feature</span></span>

<span data-ttu-id="bba12-128">Finance および Supply Chain Management に接続されたアプリケーションに対してアプリケーション設定をデプロイする前に、これらのステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="bba12-128">Complete these steps before you deploy the Application setup to your Finance or Supply Chain Management Connected application.</span></span>

<span data-ttu-id="bba12-129">このセクションは、トピック [電子請求を開始する](e-invoicing-get-started.md)の **アプリケーション設定** セクションを補完するものです。</span><span class="sxs-lookup"><span data-stu-id="bba12-129">This section complements the **Country-specific configuration of application setup** section in the topic [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="bba12-130">RCS の **グローバリゼーション機能** ワークスペースの **機能** セクションで、 **電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-130">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing** tile.</span></span>
2. <span data-ttu-id="bba12-131">**電子請求機能** ページで、**エジプト電子請求 (EG)** 電子請求機能が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bba12-131">In the **Electronic invoicing Features** page, verify that the **Egyptian electronic invoice (EG)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="bba12-132">**バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="bba12-132">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="bba12-133">**設定** タブで、**アプリケーション設定** を選択し、**接続済みアプリケーション** フィールドで、配置するアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-133">On the **Setups** tab, select **Application setup** and in the **Connected application** field, select the application where you want to deploy.</span></span>
5. <span data-ttu-id="bba12-134">**テーブル名** フィールドで、顧客請求書仕訳帳が選択されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="bba12-134">In the **Table name** field, verify that the customer invoice journal is selected.</span></span>
6. <span data-ttu-id="bba12-135">**応答タイプ** を選択し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-135">Select **Response types**, and then select **New**.</span></span>
7. <span data-ttu-id="bba12-136">**応答タイプ** フィールドに "Response" と入力し、**説明** フィールドに "Description" と入力します。</span><span class="sxs-lookup"><span data-stu-id="bba12-136">In the **Response type** field, enter "Response" and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="bba12-137">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-137">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="bba12-138">**モデル マッピング** フィールドで、**応答メッセージからモデル マッピング** を **(プレビュー) 応答メッセージのインポート形式** と共に選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-138">In the **Model mapping** field, select **Model mapping from response message**, with **(Preview) Response message import format**, and then select **Save**.</span></span>
10. <span data-ttu-id="bba12-139">**新規** を選択し、続いて **応答タイプ** フィールドで、固定値として "ResponseData" と入力します。</span><span class="sxs-lookup"><span data-stu-id="bba12-139">Select **New** and in the **Response type** field, enter "ResponseData" as a fixed value.</span></span> <span data-ttu-id="bba12-140">**説明** フィールドに、"Description" と入力します。</span><span class="sxs-lookup"><span data-stu-id="bba12-140">In the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="bba12-141">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-141">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="bba12-142">**データ エンティティ名** フィールドに、**売上請求書ヘッダー V2** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bba12-142">In the **Data entity name** field, select **Sales invoice headers V2**.</span></span>
13. <span data-ttu-id="bba12-143">**モデル マッピング** フィールドで、**エジプトの応答データのインポート** を **(プレビュー) エジプトの応答データのインポート** と共に選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bba12-143">In the **Model mapping** field, select **Egypt response data import**, with **(Preview) Egypt response data import** and then select **Save**.</span></span>
14. <span data-ttu-id="bba12-144">Finance および Supply Chain Management に接続されたアプリケーションに対してアプリケーション設定をデプロイするには[電子請求を開始する](e-invoicing-get-started.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-144">To deploy the application setup to the Finance or Supply Chain Management connected application, see [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="bba12-145">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="bba12-145">Privacy notice</span></span>

<span data-ttu-id="bba12-146">**エジプトの電子請求 (EG)** 機能を有効にするには、組織の税務登録 ID を含む一部のデータの送信が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="bba12-146">Enabling the **Egyptian electronic invoice (EG)** feature may require sending limited data, including the organization tax registration ID.</span></span> <span data-ttu-id="bba12-147">このデータは、政府の Web サービスとの統合に必要な所定の形式で、この税務当局に電子請求書を送信する目的で、税務当局から権限を与えられた第三者機関に送信されます。</span><span class="sxs-lookup"><span data-stu-id="bba12-147">This data will be transmitted to third-party agencies authorized by the tax authority for the purpose of sending electronic invoices to this tax authority in the predefined format that's required for integration with the government's web service.</span></span> <span data-ttu-id="bba12-148">管理者は、**組織管理** > **設定** > **電子ドキュメント パラメーター** に移動して、機能を有効、または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="bba12-148">An administrator can enable and disable the feature by navigating to **Organization administration** > **Setup** > **Electronic document parameters**.</span></span> <span data-ttu-id="bba12-149">**機能** タブで、**エジプトの電子請求 (EG)** 機能を含む行を選択して、適切な選択を行います。</span><span class="sxs-lookup"><span data-stu-id="bba12-149">On the **Features** tab, select the row that contains the **Egyptian electronic invoice (EG)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="bba12-150">これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="bba12-150">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="bba12-151">詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bba12-151">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bba12-152">追加リソース</span><span class="sxs-lookup"><span data-stu-id="bba12-152">Additional resources</span></span>

- [<span data-ttu-id="bba12-153">電子請求の概要</span><span class="sxs-lookup"><span data-stu-id="bba12-153">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="bba12-154">電子請求サービスの管理を開始する</span><span class="sxs-lookup"><span data-stu-id="bba12-154">Get started with Electronic invoicing service administration</span></span>](e-invoicing-get-started-service-administration.md)
- [<span data-ttu-id="bba12-155">電子請求の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="bba12-155">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="bba12-156">エジプトの顧客電子請求書</span><span class="sxs-lookup"><span data-stu-id="bba12-156">Customer electronic invoices in Egypt</span></span>](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

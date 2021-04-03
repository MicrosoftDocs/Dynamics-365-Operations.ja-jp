---
title: エジプトの電子請求アドオンの使用を開始する
description: このトピックでは、エジプトにおける Finance および Supply Chain Management の電子請求アドオンを使い始める際に役立つ情報を提供します。
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
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
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592601"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a><span data-ttu-id="adc43-103">エジプトの電子請求アドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="adc43-103">Get started with the Electronic invoicing add-on for Egypt</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="adc43-104">このトピックでは、エジプトの電子請求アドオンの使用を開始するにあたっての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="adc43-104">This topic provides information that will help you get started with the Electronic invoicing add-on for Egypt.</span></span> <span data-ttu-id="adc43-105">このトピックでは、Regulatory Configuration Services (RCS) で国ごとに異なる構成手順について説明し、[電子請求アドオンの使用を開始する](e-invoicing-get-started.md)で説明されている手順を補完します。</span><span class="sxs-lookup"><span data-stu-id="adc43-105">The topic guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS), and complement the steps described in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a><span data-ttu-id="adc43-106">エジプトの電子請求 (EG) 機能の国別コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="adc43-106">Country-specific configuration for Egyptian electronic invoice (EG) Electronic invoicing feature</span></span>

<span data-ttu-id="adc43-107">エジプトの電子請求 (EG) 機能を構成するには、一部の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adc43-107">To configure the Egyptian electronic invoice (EG) Electronic invoicing feature, there are some steps to complete.</span></span> <span data-ttu-id="adc43-108">構成の一部のパラメーターは既定値で公開されているため、事業運営に合わせて確認および更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adc43-108">Some of the parameters from the configurations are published with default values, so they must be reviewed and updated to better fit your business operation.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="adc43-109">必要条件</span><span class="sxs-lookup"><span data-stu-id="adc43-109">Prerequisites</span></span>

<span data-ttu-id="adc43-110">このセクションの手順を完了する前に、以下のことを行います。</span><span class="sxs-lookup"><span data-stu-id="adc43-110">Before you complete the procedure in this section, you must:</span></span>

- <span data-ttu-id="adc43-111">[電子請求アドオン サービス管理の使用を開始する](e-invoicing-get-started-service-administration.md)の **デジタル証明書シークレットの作成** セクションの説明に従って、デジタル証明書シークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="adc43-111">Create a digital certificate secret, as described in **Create digital certificate secret** section in [Get started with the Electronic invoicing add-on service administration](e-invoicing-get-started-service-administration.md).</span></span> <span data-ttu-id="adc43-112">テストの目的で、エジプトの税務当局は、テストおよびソリューション検証フェーズでのみ使用する必要がある特定のテスト デジタル証明書を提供しています。</span><span class="sxs-lookup"><span data-stu-id="adc43-112">For testing purposes, the Egyptian tax authority provides specific test digital certificates that must be used only during testing and solution validation phases.</span></span> <span data-ttu-id="adc43-113">詳細については、[エジプトの電子請求の SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adc43-113">For more information, consult the Egyptian tax authority web site using the link provided in the [Egyptian e-invoicing SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).</span></span>
- <span data-ttu-id="adc43-114">[電子請求のアドオンの使用を開始する](e-invoicing-get-started.md)の **組織のプロバイダー配下に電子請求機能を作成する** に説明されているように、組織にエジプトの電子請求 (EG) 機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="adc43-114">Create an Egyptian electronic invoice (EG) Electronic invoicing feature for your organization, as described in the **Create an Electronic invoicing feature under your organization provider** section in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="adc43-115">RCS で、**グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求のアドオン** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-115">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing add-on** tile.</span></span>
2. <span data-ttu-id="adc43-116">**電子請求アドオン機能** ページで、作成した **エジプトの電子請求 (EG)** 機能が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="adc43-116">On the **Electronic invoicing add-on Features** page, verify that the **Egyptian electronic invoice (EG)** Electronic invoicing feature you created is selected.</span></span>
3. <span data-ttu-id="adc43-117">**バージョン** タブで、**ドラフト** バージョンが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="adc43-117">On the **Versions** tab, verify the **Draft** version is selected.</span></span>
4. <span data-ttu-id="adc43-118">グリッドの **設定** タブで、**売上請求書** 機能の設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-118">On the **Setups** tab, in the grid, select **Sales invoice** feature setup.</span></span>
5. <span data-ttu-id="adc43-119">**編集** を選択し、**アクション** フィールド グループの **アクション** タブで、**エジプト税務当局に向けた json 文書に署名する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-119">Select **Edit**, and on the **Actions** tab in the **Actions** field group, select **Sign json document for Egyptian Tax Authority**.</span></span>
6. <span data-ttu-id="adc43-120">**パラメーター** フィールド グループでパラメーター **証明書名** を選択し、電子請求機能で使用するために作成されたデジタル証明書の名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-120">In the **Parameters** field group, select the parameter, **Certificate name** and select the name of the digital certificate created to use with the Electronic invoicing feature.</span></span>
7. <span data-ttu-id="adc43-121">**アクション** フィールド グループで、**エジプト ETA サービスとの統合** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-121">In the **Actions** field group, select **Integrate with Egyptian ETA service**.</span></span> <span data-ttu-id="adc43-122">このアクションが 2 回発生した場合は、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="adc43-122">Repeat this step for the two occurrences of this action.</span></span>
8. <span data-ttu-id="adc43-123">**パラメーター** フィールド グループで、**Web サービス URL** および **ログイン サービス URL** を選択し、必要に応じて URL パラメーターを確認してください。</span><span class="sxs-lookup"><span data-stu-id="adc43-123">In the **Parameters** field group, select **Web service URL** and **Login service URL** and, if necessary, review the URL parameters.</span></span> <span data-ttu-id="adc43-124">[エジプトの電子請求の SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/) で提供されているリンクを使用して、エジプトの税務当局の Web サイトを参照し、テストおよび実稼働の URL を取得してください。</span><span class="sxs-lookup"><span data-stu-id="adc43-124">Consult the Egyptian tax authority website to get the Testing and Production URL, using the link provided in the [Egyptian e-invoicing SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).</span></span>
9. <span data-ttu-id="adc43-125">**保存** を選択して、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="adc43-125">Select **Save** and close the page.</span></span>
10. <span data-ttu-id="adc43-126">アプリケーションの設定を構成するには、[電子請求アドオンの使用を開始する](e-invoicing-get-started.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adc43-126">To configure the application setup, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a><span data-ttu-id="adc43-127">エジプトの電子請求 (EG) 機能のアプリケーション設定の国別コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="adc43-127">Country-specific configuration of the application setup for the Egyptian electronic invoice (EG) Electronic invoicing feature</span></span>

<span data-ttu-id="adc43-128">**エジプトの電子請求 (EG)** 機能のアプリケーション設定のコンフィギュレーションのため、特定の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adc43-128">The configuration of the Application setup for **Egyptian electronic invoice (EG)** Electronic invoicing feature requires that specific steps be accomplished.</span></span> <span data-ttu-id="adc43-129">電子請求機能を電子請求アドオン サービス環境に配置する前に、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="adc43-129">You must accomplish those steps before you deploy your Electronic invoicing feature to your Electronic invoicing add-on service environment.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="adc43-130">必要条件</span><span class="sxs-lookup"><span data-stu-id="adc43-130">Prerequisites</span></span>

<span data-ttu-id="adc43-131">このセクションの手順を完了する前に、**エジプトの電子請求 (EG)** 機能を作成して開始し、トピック [電子請求アドオンの使用を開始する](e-invoicing-get-started.md)の **アプリケーションの設定を構成する** セクションの説明に従って、**エジプトの電子請求 (EG)** のアプリケーション設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="adc43-131">Before you complete the procedure in this section, create and initiate a **Egyptian electronic invoice (EG)** Electronic invoicing feature to configure the application setup for **Egyptian electronic invoice (EG)** Electronic invoicing feature, as described in the **Configure the application setup** section in the topic, [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

1. <span data-ttu-id="adc43-132">RCS で、**グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求のアドオン** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-132">In RCS, in the **Features** section of the **Globalization feature** workspace, select the **Electronic invoicing add-on** tile.</span></span>
2. <span data-ttu-id="adc43-133">**電子請求アドオン機能** ページで、**エジプトの電子請求 (EG)** 機能が選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="adc43-133">In the **Electronic invoicing add-on Features** page, verify that the **Egyptian electronic invoice (EG)** Electronic invoicing feature is selected.</span></span>
3. <span data-ttu-id="adc43-134">**バージョン** タブで、**ドラフト** バージョンが選択されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="adc43-134">On the **Versions** tab, verify that the **Draft** version is selected.</span></span>
4. <span data-ttu-id="adc43-135">**設定** タブで、**アプリケーション設定** を選択し、**接続済みアプリケーション** フィールドで、配置するアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-135">On the **Setups** tab, select **Application setup** and in the **Connected application** field, select the application where you want to deploy.</span></span>
5. <span data-ttu-id="adc43-136">**テーブル名** フィールドで、顧客請求書仕訳帳が選択されているか確認します。</span><span class="sxs-lookup"><span data-stu-id="adc43-136">In the **Table name** field, verify that the customer invoice journal is selected.</span></span>
6. <span data-ttu-id="adc43-137">**応答タイプ** を選択し、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-137">Select **Response types**, and then select **New**.</span></span>
7. <span data-ttu-id="adc43-138">**応答タイプ** フィールドに "Response" と入力し、**説明** フィールドに "Description" と入力します。</span><span class="sxs-lookup"><span data-stu-id="adc43-138">In the **Response type** field, enter "Response" and in the **Description** field, enter "Description".</span></span>
8. <span data-ttu-id="adc43-139">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-139">In the **Submission status** field, select **Pending**.</span></span>
9. <span data-ttu-id="adc43-140">**モデル マッピング** フィールドで、**応答メッセージからモデル マッピング** を **(プレビュー) 応答メッセージのインポート形式** と共に選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-140">In the **Model mapping** field, select **Model mapping from response message**, with **(Preview) Response message import format**, and then select **Save**.</span></span>
10. <span data-ttu-id="adc43-141">**新規** を選択し、続いて **応答タイプ** フィールドで、固定値として "ResponseData" と入力します。</span><span class="sxs-lookup"><span data-stu-id="adc43-141">Select **New** and in the **Response type** field, enter "ResponseData" as a fixed value.</span></span> <span data-ttu-id="adc43-142">**説明** フィールドに、"Description" と入力します。</span><span class="sxs-lookup"><span data-stu-id="adc43-142">In the **Description** field, enter "Description".</span></span>
11. <span data-ttu-id="adc43-143">**提出の状態** フィールドで **保留** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-143">In the **Submission status** field, select **Pending**.</span></span>
12. <span data-ttu-id="adc43-144">**データ エンティティ名** フィールドに、**売上請求書ヘッダー V2** と入力します。</span><span class="sxs-lookup"><span data-stu-id="adc43-144">In the **Data entity name** field, select **Sales invoice headers V2**.</span></span>
13. <span data-ttu-id="adc43-145">**モデル マッピング** フィールドで、**エジプトの応答データのインポート** を **(プレビュー) エジプトの応答データのインポート** と共に選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="adc43-145">In the **Model mapping** field, select **Egypt response data import**, with **(Preview) Egypt response data import** and then select **Save**.</span></span>
14. <span data-ttu-id="adc43-146">電子請求機能を配置する方法については、[電子請求アドオンの使用を開始する](e-invoicing-get-started.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adc43-146">To deploy the Electronic invoicing feature, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="adc43-147">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="adc43-147">Privacy notice</span></span>

<span data-ttu-id="adc43-148">**エジプトの電子請求 (EG)** 機能を有効にするには、組織の税務登録 ID を含む一部のデータの送信が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="adc43-148">Enabling the **Egyptian electronic invoice (EG)** feature may require sending limited data, including the organization tax registration ID.</span></span> <span data-ttu-id="adc43-149">このデータは、政府の Web サービスとの統合に必要な所定の形式で、この税務当局に電子請求書を送信する目的で、税務当局から権限を与えられた第三者機関に送信されます。</span><span class="sxs-lookup"><span data-stu-id="adc43-149">This data will be transmitted to third-party agencies authorized by the tax authority for the purpose of sending electronic invoices to this tax authority in the predefined format that's required for integration with the government's web service.</span></span> <span data-ttu-id="adc43-150">管理者は、**組織管理** > **設定** > **電子ドキュメント パラメーター** に移動して、機能を有効、または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="adc43-150">An administrator can enable and disable the feature by navigating to **Organization administration** > **Setup** > **Electronic document parameters**.</span></span> <span data-ttu-id="adc43-151">**機能** タブで、**エジプトの電子請求 (EG)** 機能を含む行を選択して、適切な選択を行います。</span><span class="sxs-lookup"><span data-stu-id="adc43-151">On the **Features** tab, select the row that contains the **Egyptian electronic invoice (EG)** feature, and then make the appropriate selection.</span></span> <span data-ttu-id="adc43-152">これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="adc43-152">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="adc43-153">詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="adc43-153">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adc43-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="adc43-154">Additional resources</span></span>

- [<span data-ttu-id="adc43-155">電子請求アドオンの概要</span><span class="sxs-lookup"><span data-stu-id="adc43-155">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="adc43-156">電子請求アドオン サービス管理の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="adc43-156">Get started with Electronic invoicing add-on service administration</span></span>](e-invoicing-get-started-service-administration.md)
- [<span data-ttu-id="adc43-157">電子請求アドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="adc43-157">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="adc43-158">エジプトの顧客電子請求書</span><span class="sxs-lookup"><span data-stu-id="adc43-158">Customer electronic invoices in Egypt</span></span>](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

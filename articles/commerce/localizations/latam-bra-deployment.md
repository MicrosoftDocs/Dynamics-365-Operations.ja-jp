---
title: ブラジル向け Dynamics 365 Commerce ローカライズの設定と展開
description: このトピックでは、ブラジル向け Microsoft Dynamics 365 Commerce ローカライズの設定と展開の方法について説明します。
author: v-ankvik
ms.date: 06/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: v-chgri
ms.search.region: Brazil
ms.search.industry: Retail
ms.author: v-ankvik
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7263a25cc50f2f4f785ed30aa11edd08a5913ac3
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303398"
---
# <a name="set-up-and-deploy-the-dynamics-365-commerce-localization-for-brazil"></a><span data-ttu-id="5857c-103">ブラジル向け Dynamics 365 Commerce ローカライズの設定と展開</span><span class="sxs-lookup"><span data-stu-id="5857c-103">Set up and deploy the Dynamics 365 Commerce localization for Brazil</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5857c-104">このトピックでは、ブラジル向け Microsoft Dynamics 365 Commerce ローカライズの設定と展開の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5857c-104">This topic covers how to set up and deploy the Microsoft Dynamics 365 Commerce localization for Brazil.</span></span>

<span data-ttu-id="5857c-105">ブラジル向け Dynamics 365 Commerce ローカライズには、次の Commerce コンポーネントが含まれます: Commerce Runtime (CRT)、Retail Server、および販売時点管理 (POS)。</span><span class="sxs-lookup"><span data-stu-id="5857c-105">The Dynamics 365 Commerce localization for Brazil includes several extensions of the following Commerce components: the Commerce runtime (CRT), Retail Server, and point of sale (POS).</span></span> <span data-ttu-id="5857c-106">これらの拡張機能を使用すると、電子会計書類の登録が延期される場合、ブラジル固有の税金の計算、小売販売用の電子会計ドキュメントの生成、カスタムフィールドを持つ DANFE (Documento Auxiliar de Nota Fiscal Eletrônica) の会計レシートの印刷、ブラジル固有の顧客情報の管理、オフライン代替モードでの販売の発行が可能になります。</span><span class="sxs-lookup"><span data-stu-id="5857c-106">These extensions let you calculate Brazil-specific taxes, generate electronic fiscal documents for retail sales, print DANFE (Documento Auxiliar de Nota Fiscal Eletrônica) fiscal receipts that have custom fields, manage Brazil-specific customer information, and issue sales in offline contingency mode, where registration of electronic fiscal documents is postponed.</span></span> <span data-ttu-id="5857c-107">ブラジル向け Commerce ローカライズの詳細については、[ブラジルのローカライズ スコープ](../../finance/localizations/latam-bra-scope.md) および[ブラジル向け Commerce ローカライズ](latam-bra-commerce-localization.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-107">For more information about the Commerce localization for Brazil, see [Brazilian localization scope](../../finance/localizations/latam-bra-scope.md) and [Commerce localization for Brazil](latam-bra-commerce-localization.md).</span></span>

<span data-ttu-id="5857c-108">このトピックで説明する拡張機能は、会計統合のフレームワークに基づいて開発されました。</span><span class="sxs-lookup"><span data-stu-id="5857c-108">The extensions that are described in this topic were developed based on the fiscal integration framework.</span></span> <span data-ttu-id="5857c-109">会計統合機能の詳細については、[Commerce チャネルの会計統合の概要](fiscal-integration-for-retail-channel.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-109">For information about the fiscal integration functionality, see [Overview of fiscal integration for Commerce channels](fiscal-integration-for-retail-channel.md).</span></span> <span data-ttu-id="5857c-110">[電子申告 (ER) は ](../../dev-itpro/analytics/general-electronic-reporting.md)、電子会計ドキュメントの電子化の形式を実装するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5857c-110">[Electronic reporting (ER)](../../dev-itpro/analytics/general-electronic-reporting.md) is used to implement formats for Brazilian electronic fiscal documents.</span></span>

## <a name="enable-brazil-specific-commerce-functionality"></a><span data-ttu-id="5857c-111">ブラジル固有の Commerce 機能の有効化</span><span class="sxs-lookup"><span data-stu-id="5857c-111">Enable Brazil-specific Commerce functionality</span></span>

<span data-ttu-id="5857c-112">このセクションでは、ブラジルに固有で推奨される Commerce 本社の設定を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5857c-112">This section describes how to configure Commerce headquarters settings that are specific to and recommended for Brazil.</span></span> <span data-ttu-id="5857c-113">詳細については、[Commerce のホーム ページ](../index.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-113">For more information, see the [Commerce home page](../index.md).</span></span>

<span data-ttu-id="5857c-114">ブラジル固有の機能を有効にして使用するには、Commerce 本社で次の設定を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-114">To enable and use the Brazil-specific functionality, you must configure the following settings in Commerce headquarters.</span></span>

1. <span data-ttu-id="5857c-115">法人の基本住所で、**国/地域** フィールドを **BRA** (ブラジル) に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-115">In the primary address of the legal entity, set the **Country/region** field to **BRA** (Brazil).</span></span>
1. <span data-ttu-id="5857c-116">ブラジルにあるすべての店舗の POS 機能プロファイルで、 **ISO コード フィールド** を **BR** (ブラジル) に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-116">In the POS functionality profile of every store that is located in Brazil, set the **ISO code** field to **BR** (Brazil).</span></span>
1. <span data-ttu-id="5857c-117">**システム管理 \> ワークスペースs \> 機能の管理** に移動し、**すべて** タブで、次の機能キーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="5857c-117">Go to **System administration \> Workspaces \> Feature management**, and then, on the **All** tab, enable the following feature keys:</span></span>

    - <span data-ttu-id="5857c-118">(ブラジル) ブラジルに固有の Commerce 機能</span><span class="sxs-lookup"><span data-stu-id="5857c-118">(Brazil) Commerce functionality that is specific to Brazil</span></span>
    - <span data-ttu-id="5857c-119">小売明細書 - トリクル フィード</span><span class="sxs-lookup"><span data-stu-id="5857c-119">Retail statements - Trickle feed</span></span>
    - <span data-ttu-id="5857c-120">会計統合フレームワークの内部および外部コネクタのサポート</span><span class="sxs-lookup"><span data-stu-id="5857c-120">Support for internal and external connectors in the fiscal integration framework</span></span>
    - <span data-ttu-id="5857c-121">ドキュメントの登録の延期</span><span class="sxs-lookup"><span data-stu-id="5857c-121">Postponed registration of documents</span></span>
    - <span data-ttu-id="5857c-122">小売店舗のユーザー定義の証明書プロファイル</span><span class="sxs-lookup"><span data-stu-id="5857c-122">User-defined certificate profiles for retail stores</span></span>

## <a name="set-up-electronic-reporting"></a><span data-ttu-id="5857c-123">電子申告の設定</span><span class="sxs-lookup"><span data-stu-id="5857c-123">Set up electronic reporting</span></span>

<span data-ttu-id="5857c-124">Microsoft Dynamics Lifecycle Services (LCS) から電子会計ドキュメント用の ER コンフィギュレーションをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="5857c-124">You can download the ER configurations for the electronic fiscal documents from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="5857c-125">詳細については、[電子申告 (ER) コンフィギュレーションのインポート](../../dev-itpro/analytics/electronic-reporting-import-ger-configurations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-125">For more information, see [Import Electronic reporting (ER) configurations](../../dev-itpro/analytics/electronic-reporting-import-ger-configurations.md).</span></span> <span data-ttu-id="5857c-126">次の手順に示すコンフィギュレーションの最新バージョンをダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-126">You must download the latest versions of the configurations that are listed in the following procedure.</span></span>

<span data-ttu-id="5857c-127">Commerce 本社で電子申告を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5857c-127">To set up electronic reporting in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5857c-128">**組織管理 \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-128">Go to **Organization Administration \> Workspaces \> Electronic Reporting**.</span></span>
1. <span data-ttu-id="5857c-129">**Microsoft** コンフィギュレーション プロバイダーのタイルで、省略記号 (**...**)を選択し、**有効に設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-129">On the tile for the **Microsoft** configuration provider, select the ellipsis (**...**), and then select **Set active**.</span></span>
1. <span data-ttu-id="5857c-130">タイルで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-130">On the tile, select **Repositories**.</span></span>
1. <span data-ttu-id="5857c-131">**グローバル** コンフィギュレーション リポジトリを選択し、アクション ペインで **開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-131">Select the **Global** configuration repository, and then, on the Action Pane, select **Open**.</span></span>
1. <span data-ttu-id="5857c-132">**Regulatory Configuration Service に接続する** ダイアログ ボックスで、**Regulatory Configuration Service に接続するには、ここをクリックしてください** を選択し、ダイアログ ボックスに戻って **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-132">In the **Connect to Regulatory Configuration Service** dialog box, select **Click here to connect to Regulatory Configuration Service**, return to the dialog box, and then select **OK**.</span></span>
1. <span data-ttu-id="5857c-133">次のデータ モデル、データ モデル マッピング、および形式コンフィギュレーションの最新の共有バージョンをインポートします。</span><span class="sxs-lookup"><span data-stu-id="5857c-133">Import the latest shared versions of the following data model, data model mapping, and format configurations:</span></span>

    - <span data-ttu-id="5857c-134">(プレビュー) 会計ドキュメントのマッピング</span><span class="sxs-lookup"><span data-stu-id="5857c-134">(Preview) Fiscal documents mapping</span></span>
    - <span data-ttu-id="5857c-135">(プレビュー) NF-e キャンセル エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5857c-135">(Preview) NF-e cancel export format (BR)</span></span>
    - <span data-ttu-id="5857c-136">(プレビュー) NF-e 状態要求エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5857c-136">(Preview) NF-e status request export format (BR)</span></span>
    - <span data-ttu-id="5857c-137">(プレビュー) NF-e 送信エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5857c-137">(Preview) NF-e submit export format (BR)</span></span>
    - <span data-ttu-id="5857c-138">(プレビュー) NFC-e 送信エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5857c-138">(Preview) NFC-e submit export format (BR)</span></span>
    - <span data-ttu-id="5857c-139">(プレビュー) NFC-e コンティンジェンシー エクスポートの形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5857c-139">(Preview) NFC-e contingency export format (BR)</span></span>
    - <span data-ttu-id="5857c-140">(プレビュー) NFC-e 会計ドキュメントのマッピング</span><span class="sxs-lookup"><span data-stu-id="5857c-140">(Preview) NFC-e fiscal documents mapping</span></span>
    - <span data-ttu-id="5857c-141">(プレビュー) NFC-e 会計ドキュメントの検証形式 (BR)</span><span class="sxs-lookup"><span data-stu-id="5857c-141">(Preview) NFC-e fiscal documents validation format (BR)</span></span>

1. <span data-ttu-id="5857c-142">**組織管理 \> ワークスペース \> 電子申告** の順に移動し、**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-142">Go to **Organization administration \> Workspaces \> Electronic reporting**, and select **Reporting configurations**.</span></span>
1. <span data-ttu-id="5857c-143">**会計ドキュメントのマッピング** を選択し、**既定のモデル マッピング** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-143">Select **Fiscal documents mapping**, and then set the **Default model mapping** option to **No**.</span></span>
1. <span data-ttu-id="5857c-144">**NFC-e 会計ドキュメントのマッピング** を選択し、**既定のモデル マッピング** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-144">Select **NFC-e fiscal documents mapping**, and then set the **Default model mapping** option to **Yes**.</span></span>
1. <span data-ttu-id="5857c-145">**組織管理 \> 設定 \> ブラジル パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-145">Go to **Organization Administration \> Setup \> Brazilian parameters**.</span></span>
1. <span data-ttu-id="5857c-146">**小売タブ** の **形式マッピング** フィールドで、**NFC-e 会計ドキュメント検証形式 (BR)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-146">On the **Retail** tab, in the **Format mapping** field, select **NFC-e fiscal documents validation format (BR)**.</span></span>

## <a name="set-up-a-fiscal-establishment-and-nf-e-federal-parameters"></a><span data-ttu-id="5857c-147">会計施設および NF-e パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="5857c-147">Set up a fiscal establishment and NF-e federal parameters</span></span>

<span data-ttu-id="5857c-148">Commerce 本社に会計施設および NF-e (Nota Fiscal Eletrônica) の連邦パラメータを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5857c-148">To set up a fiscal establishment and NF-e (Nota Fiscal Eletrônica) federal parameters in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5857c-149">**組織管理 \> 組織 \> 会計機関 \> 会計機関** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-149">Go to **Organization administration \> Organizations \> Fiscal establishments \> Fiscal establishment**.</span></span>
1. <span data-ttu-id="5857c-150">**税務登録番号 - CNPJ, IE & CCM** フィールドで、税登録番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-150">In the **Tax registration numbers - CNPJ, IE & CCM** field, enter the tax registration numbers.</span></span>
1. <span data-ttu-id="5857c-151">**施設の住所フィールド** で、住所を入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-151">In the **Address of the establishment** field, enter an address.</span></span>
1. <span data-ttu-id="5857c-152">CSC トークンと CS C英数字のコードを入力して、CSC (Código de Segurança do Contribuinte) 暗号化を設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-152">Set up CSC (Código de Segurança do Contribuinte) encryption by entering the CSC token and CSC alphanumeric code.</span></span>
1. <span data-ttu-id="5857c-153">税務当局サービスによる認証と会計ドキュメントのデジタル署名に適切なデジタル証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-153">Select the appropriate digital certificate for authentication with the tax authority service and digital signing of fiscal documents.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5857c-154">**会計施設** ページで構成された証明書は、オフライン代替モードで POS で発行され、Commerce 本社を通じて承認のために送信される NFC-e (Nota Fiscal de Consumidor Eletrônica) ドキュメントに使用されます。</span><span class="sxs-lookup"><span data-stu-id="5857c-154">The certificate that is configured on the **Fiscal establishment** page is used for NFC-e (Nota Fiscal de Consumidor Eletrônica) documents that are issued in POS in offline contingency mode and then submitted for authorization through Commerce headquarters.</span></span> <span data-ttu-id="5857c-155">会計ドキュメントをオフライン代替モードで署名できるようにするには、POS のオフライン証明書ストレージに証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-155">To enable fiscal documents to be signed in offline contingency mode, you must install a certificate in the offline certificate storage of the POS.</span></span> <span data-ttu-id="5857c-156">詳細については、[オフライン代替モードでの商品の現金店頭払い売上の作成](latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) および[代替モードで発行された NFC-e の登録の延期](latam-bra-nfce-contingency-mode.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-156">For more information, see [Make a cash-and-carry sale of goods in offline contingency mode](latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) and [Postponed registration of NFC-e issued in contingency mode](latam-bra-nfce-contingency-mode.md).</span></span>

1. <span data-ttu-id="5857c-157">**NF-E WEB SERVICE** の、**環境** フィールドで、**テスト** または **生産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-157">Under **NF-E WEB SERVICE**, in the **Environment** field, select **Testing** or **Production.**</span></span>
1. <span data-ttu-id="5857c-158">**NFC-E WEB SERVICE** の、**環境** フィールドで、**テスト** または **生産** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-158">Under **NFC-E WEB SERVICE**, in the **Environment** field, select **Testing** or **Production.**</span></span>
1. <span data-ttu-id="5857c-159">NF-e および NFC-e 機能のバージョンを指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-159">Specify the versions of the NF-e and NFC-e features.</span></span>
1. <span data-ttu-id="5857c-160">**NF-E WEB SERVICE** の、**所轄官庁** フィールドで、**NF-e 連邦パラメーター \> Web サービス \> 所轄官庁** で使用される値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-160">Under **NF-E WEB SERVICE**, in the **Authority** field, enter the value used at **NF-e federal parameters \> Web services \> Authority**.</span></span>
1. <span data-ttu-id="5857c-161">**NFC-E WEB SERVICE** の、**所轄官庁** フィールドで、**NF-e 連邦パラメーター \> Web サービス \> 所轄官庁** で使用される値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-161">Under **NFC-E WEB SERVICE**, in the **Authority** field, enter the value used at **NF-e federal parameters \> Web services \> Authority**.</span></span>
1. <span data-ttu-id="5857c-162">**組織の管理 \> 組織 \> 会計施設 \> 電子会計ドキュメント \> NF-e 連邦パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-162">Go to **Organization administration \> Organizations \> Fiscal establishments \> Electronic fiscal documents \> NF-e federal parameters**.</span></span>
1. <span data-ttu-id="5857c-163">必要な状態に対して新しい所轄官庁を作成するか、既存の所轄官庁を使用します。</span><span class="sxs-lookup"><span data-stu-id="5857c-163">Create new authorities for the required states, or use existing authorities.</span></span>
1. <span data-ttu-id="5857c-164">各状態について、**NFC-e の照会のインターネット アドレス** フィールドに、QR コード URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-164">For each state, in the **Internet address for NFC-e inquiry** field, enter QR code URLs.</span></span>
1. <span data-ttu-id="5857c-165">各状態について、適切な環境のすべての Web サービスのエンドポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-165">For each state, specify the endpoints for all web services of the appropriate environments.</span></span>

## <a name="set-up-address-books"></a><span data-ttu-id="5857c-166">アドレス帳を設定します</span><span class="sxs-lookup"><span data-stu-id="5857c-166">Set up address books</span></span>

<span data-ttu-id="5857c-167">Commerce 本社のブラジルの顧客、店舗、および作業者に同じアドレス帳を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5857c-167">To add the same address book for Brazilian customers, stores, and workers in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5857c-168">**Retail とコマース \> 顧客 \> 顧客サービス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-168">Go to **Retail and Commerce \> Customers \> All customers**.</span></span>
1. <span data-ttu-id="5857c-169">**一般** タブの **アドレス帳** フィールドで、必要に応じて顧客の小売アドレス帳を追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-169">On the **General** tab, in the **Address books** field, add retail address books for customers as required.</span></span>
1. <span data-ttu-id="5857c-170">**Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-170">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5857c-171">**一般** タブの **顧客アドレス帳** フィールドおよび **従業員アドレス帳** フィールドで、店舗のアドレス帳を追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-171">On the **General** tab, in the **Customer address book** and **Employee address book** fields, add the address books for the stores.</span></span>
1. <span data-ttu-id="5857c-172">**Retail と Commerce \> 従業員 \> 作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-172">Go to **Retail and Commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="5857c-173">**作業者集計** タブの **アドレス帳** フィールドで、作業者のアドレス帳を追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-173">On the **Worker summary** tab, in the **Address books** field, add the address books for workers.</span></span>

## <a name="set-up-sales-tax-for-pos"></a><span data-ttu-id="5857c-174">POS の消費税を設定します</span><span class="sxs-lookup"><span data-stu-id="5857c-174">Set up sales tax for POS</span></span>

<span data-ttu-id="5857c-175">Commerce 本社で POS の消費税を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5857c-175">To set up sales tax for POS in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5857c-176">**税 \> 間接税 \> 売上税 \> 売上税コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-176">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
1. <span data-ttu-id="5857c-177">さまざまな税タイプと税コードに対して必要な消費税コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-177">Create the required sales tax codes for different tax types and taxation codes.</span></span> <span data-ttu-id="5857c-178">返品による消費税コードを含めます。</span><span class="sxs-lookup"><span data-stu-id="5857c-178">Include sales tax codes for returns.</span></span>
1. <span data-ttu-id="5857c-179">**税 \> 間接税 \> 売上税 \> 消費税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax group**.</span></span>
1. <span data-ttu-id="5857c-180">小売販売および返品用の消費税グループを作成し、作成した消費税コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-180">Create sales tax groups for retail sales and returns, and add the sales tax codes that you just created.</span></span>
1. <span data-ttu-id="5857c-181">**Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-181">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5857c-182">**消費税グループ** および **返品用の消費税グループ** フィールドで、作成した消費税グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-182">In the **Sales tax group** and **Sales tax group for returns** fields, select the sales tax groups that you just created.</span></span>
1. <span data-ttu-id="5857c-183">**税 \> 間接税 \> 消費税 \> 品目消費税グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-183">Go to **Tax \> Indirect taxes \> Sales tax \> Item sales tax groups**.</span></span>
1. <span data-ttu-id="5857c-184">**小売の品目消費税グループ** という名前の品目消費税グループを作成し、既に作成した消費税コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-184">Create an item sales tax group that is named **Item sales tax groups for retail**, and add the sales tax codes that you created earlier.</span></span>
1. <span data-ttu-id="5857c-185">**組織管理 \> セットアップ \> 会計ドキュメント ソース テキスト** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-185">Go to **Organization administration \> Setup \> Fiscal document source texts**.</span></span>
1. <span data-ttu-id="5857c-186">小売税の負担に対する会計ドキュメント ソース テキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-186">Create a fiscal document source text for retail tax burden.</span></span> <span data-ttu-id="5857c-187">**制限** フィールドを **外部** に設定し、**会計情報** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-187">Set the **Restriction** field to **External** and the **Fiscal information** option to **No**.</span></span>
1. <span data-ttu-id="5857c-188">**組織管理 \> 設定 \> ブラジル パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-188">Go to **Organization administration \> Setup \> Brazilian parameters**.</span></span>
1. <span data-ttu-id="5857c-189">**小売** タブの **テキスト ID** フィールドで、小売税の負担のソース テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-189">On the **Retail** tab, in the **Text ID** field, specify the source text for retail tax burden.</span></span>
1. <span data-ttu-id="5857c-190">**Retail と Commerce \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-190">Go to **Retail and Commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="5857c-191">必要な製品を選択し、ブラジル固有の次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-191">Select the desired products, and set the following Brazil-specific fields:</span></span>

    - <span data-ttu-id="5857c-192">**販売** タブで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5857c-192">On the **Sell** tab:</span></span>

        - <span data-ttu-id="5857c-193">品目消費税グループ</span><span class="sxs-lookup"><span data-stu-id="5857c-193">Item sales tax group</span></span>

    - <span data-ttu-id="5857c-194">**会計情報** タブで、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="5857c-194">On the **Fiscal information** tab:</span></span>

        - <span data-ttu-id="5857c-195">課税元</span><span class="sxs-lookup"><span data-stu-id="5857c-195">Taxation origin</span></span>
        - <span data-ttu-id="5857c-196">製品タイプ</span><span class="sxs-lookup"><span data-stu-id="5857c-196">Product type</span></span>
        - <span data-ttu-id="5857c-197">会計分類コード</span><span class="sxs-lookup"><span data-stu-id="5857c-197">Fiscal classification code</span></span>
        - <span data-ttu-id="5857c-198">概算連邦税率</span><span class="sxs-lookup"><span data-stu-id="5857c-198">Approximate federal tax percentage</span></span>
        - <span data-ttu-id="5857c-199">概算状態税率</span><span class="sxs-lookup"><span data-stu-id="5857c-199">Approximate state tax percentage</span></span>
        - <span data-ttu-id="5857c-200">概算市税率</span><span class="sxs-lookup"><span data-stu-id="5857c-200">Approximate city tax percentage</span></span>

1. <span data-ttu-id="5857c-201">**税 \> 設定 \> 売上税 \> CFOP コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-201">Go to **Tax \> Setup \> Sales tax \> CFOP codes**.</span></span>
1. <span data-ttu-id="5857c-202">小売返品に使用する CFOP (Código Fiscal de Operações e de Prestações) コードの **会計参照必須** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-202">Set the **Fiscal reference required** option to **No** for CFOP (Código Fiscal de Operações e de Prestações) codes that are used for retail returns.</span></span>

## <a name="set-up-a-retail-store"></a><span data-ttu-id="5857c-203">小売店舗の設定</span><span class="sxs-lookup"><span data-stu-id="5857c-203">Set up a retail store</span></span>

<span data-ttu-id="5857c-204">Commerce 本社で小売店舗を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5857c-204">To set up a retail store in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5857c-205">**在庫管理 \> 設定 \> 在庫詳細 \> 倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-205">Go to **Inventory management \> Setup \> Inventory breakdown \> Warehouses**.</span></span>
1. <span data-ttu-id="5857c-206">店舗の倉庫を作成し、住所を指定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-206">Create warehouses for the stores, and specify addresses.</span></span>
1. <span data-ttu-id="5857c-207">**Retail と Commerce \> チャンネル \> 店舗 \> すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-207">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
1. <span data-ttu-id="5857c-208">店舗を選択し、ブラジル固有の次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-208">Create the stores, and set the following Brazil-specific fields:</span></span>

    - <span data-ttu-id="5857c-209">税込価格</span><span class="sxs-lookup"><span data-stu-id="5857c-209">Prices include sales tax</span></span>
    - <span data-ttu-id="5857c-210">売上税グループ</span><span class="sxs-lookup"><span data-stu-id="5857c-210">Sales tax group</span></span>
    - <span data-ttu-id="5857c-211">返品用の消費税グループ</span><span class="sxs-lookup"><span data-stu-id="5857c-211">Sales tax group for returns</span></span>
    - <span data-ttu-id="5857c-212">既定の顧客</span><span class="sxs-lookup"><span data-stu-id="5857c-212">Default customer</span></span>

        > [!NOTE]
        > <span data-ttu-id="5857c-213">既定の顧客は、店舗と同じアドレス帳に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-213">The default customer should be included in the same address book as the store.</span></span>

1. <span data-ttu-id="5857c-214">前の手順で作成した店舗の支払方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-214">Set up payment methods for the stores that you created in the previous step.</span></span>
1. <span data-ttu-id="5857c-215">**Retail と Commerce \> 本社の設定 \> コマース スケジューラ** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5857c-215">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler**.</span></span>
1. <span data-ttu-id="5857c-216">使用するチャネル データベースに、既に作成した店舗を追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-216">Add the stores that you created earlier to the channel database that is used.</span></span>
1. <span data-ttu-id="5857c-217">**小売りとコマース\> チャンネル設定 \> POS 設定 \> レジスター の順に移動します**。</span><span class="sxs-lookup"><span data-stu-id="5857c-217">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
1. <span data-ttu-id="5857c-218">POS レジスターを選択し、ブラジル固有の次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-218">Create POS registers, and set the following Brazil-specific fields:</span></span>

    - <span data-ttu-id="5857c-219">NFC-e シリーズ</span><span class="sxs-lookup"><span data-stu-id="5857c-219">NFC-e series</span></span>
    - <span data-ttu-id="5857c-220">NFC-e 代替シリーズ</span><span class="sxs-lookup"><span data-stu-id="5857c-220">NFC-e contingency series</span></span>
    - <span data-ttu-id="5857c-221">NF-e シリーズ</span><span class="sxs-lookup"><span data-stu-id="5857c-221">NF-e series</span></span>

1. <span data-ttu-id="5857c-222">**小売りとコマース\> チャンネル設定 \> POS 設定 \> デバイス の順に移動します**。</span><span class="sxs-lookup"><span data-stu-id="5857c-222">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
1. <span data-ttu-id="5857c-223">作成した POS レジスター用のデバイスを作成および構成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-223">Create and configure devices for the POS registers that you just created.</span></span>
1. <span data-ttu-id="5857c-224">**組織管理 \> 組織 \> 組織階層** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-224">Go to **Organization administration \> Organizations \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="5857c-225">**事業単位別小売店舗** 組織階層を選択し、**表示** を選択し、**編集 \> 小売チャネルの挿入** を選択し、既にに作成した店舗を階層内の適切な事業単位に追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-225">Select **Retail Stores by Business Unit** organization hierarchy, select **View**, select **Edit \> Insert retail channel**, and add the stores that you created earlier to the appropriate business units in the hierarchy.</span></span> <span data-ttu-id="5857c-226">次に、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="5857c-226">Then publish the changes.</span></span>
1. <span data-ttu-id="5857c-227">**Retail POS の転記** の目的を、**事業単位別小売店舗** 組織階層に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="5857c-227">Assign the **Retail POS posting** purpose to the **Retail Stores by Business Unit** organization hierarchy.</span></span>
1. <span data-ttu-id="5857c-228">**Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-228">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="5857c-229">チャネル更新を公開します。</span><span class="sxs-lookup"><span data-stu-id="5857c-229">Publish the channel updates.</span></span>
1. <span data-ttu-id="5857c-230">**Retail と Commerce \> チャネル設定 \> POS プロファイル \> レシート プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-230">Go to **Retail and Commerce \> Channel setup \> POS profiles \> Receipt profiles**.</span></span>
1. <span data-ttu-id="5857c-231">DANFEの レシート レイアウトを作成し、そのレイアウトをレシート プロファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-231">Create receipt layouts for DANFE, and add the layouts to the receipt profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="5857c-232">レシート設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-232">The default company of the user who creates the receipt setup should be the same legal entity where the language text setup is created.</span></span> <span data-ttu-id="5857c-233">または、ユーザーの既定の会社、およびレシート設定の作成対象の店舗の法人の両方で、同じ言語テキスト設定を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-233">Alternatively, the same language text setup should be created in both the user's default company and the legal entity of the store that the receipt setup is created for.</span></span>

<span data-ttu-id="5857c-234">レシート形式デザイナーで、必要なレシート形式ごとに、適切なレシート セクションにブラジルのカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-234">In the receipt format designer, add Brazilian custom fields to the appropriate receipt section for every receipt format that is required.</span></span> <span data-ttu-id="5857c-235">レシート形式の使用方法の詳細については、[レシート テンプレートと印刷](../receipt-templates-printing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-235">For more information about how to work with receipt formats, see [Receipt templates and printing](../receipt-templates-printing.md).</span></span>

## <a name="set-up-the-fiscal-registration-process"></a><span data-ttu-id="5857c-236">会計登録プロセスの設定</span><span class="sxs-lookup"><span data-stu-id="5857c-236">Set up the fiscal registration process</span></span>

<span data-ttu-id="5857c-237">Commerce 本社で会計登録プロセスを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5857c-237">To set up the fiscal registration process in Commerce headquarters, follow these steps.</span></span> <span data-ttu-id="5857c-238">詳細情報については、[コマース チャネルの会計統合の設定](./setting-up-fiscal-integration-for-retail-channel.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-238">For more information, see [Set up the fiscal integration for Commerce channels](./setting-up-fiscal-integration-for-retail-channel.md).</span></span>

1. <span data-ttu-id="5857c-239">**Retail とコマース \> 本社の設定 \> パラメーター \> コマース共有パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-239">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce shared parameters**.</span></span>
1. <span data-ttu-id="5857c-240">**一般** タブで、**会計統合の有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-240">On the **General** tab, set the **Enable fiscal integration** option to **Yes**.</span></span>
1. <span data-ttu-id="5857c-241">**Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計コネクタ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-241">Go to **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connectors**.</span></span>
1. <span data-ttu-id="5857c-242">[Commerce 会計統合リポジトリ (repo)](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations) からコネクタ構成を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5857c-242">Load the connector configuration from the [Commerce Fiscal Integration repository (repo)](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations).</span></span> <span data-ttu-id="5857c-243">[**Configurations\\Connectors**](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations%2FConnectors) には次のファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="5857c-243">The following files are located under [**Configurations\\Connectors**](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations%2FConnectors):</span></span>

    - <span data-ttu-id="5857c-244">SubmitConnector.xml</span><span class="sxs-lookup"><span data-stu-id="5857c-244">SubmitConnector.xml</span></span>
    - <span data-ttu-id="5857c-245">ContingencyConnector.xml</span><span class="sxs-lookup"><span data-stu-id="5857c-245">ContingencyConnector.xml</span></span>

1. <span data-ttu-id="5857c-246">**Retail と Commerce \> チャネル設定 \> 会計統合 \> 会計ドキュメント プロバイダー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-246">Go to **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal document providers**.</span></span>
1. <span data-ttu-id="5857c-247">[Commerce 会計統合リポジトリ (repo)](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations) からドキュメント プロバイダー コンフィギュレーションを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5857c-247">Load the document provider configurations from the [Commerce Fiscal Integration repo](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations).</span></span> <span data-ttu-id="5857c-248">[**Configurations\\DocumentProviders**](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations%2FDocumentProviders) には次の構成ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="5857c-248">The following configuration files are located under [**Configurations\\DocumentProviders**](https://msazure.visualstudio.com/D365/_git/Commerce-Samples-EndToEndSolutions?path=%2Fsrc%2FFiscalIntegration%2FElectronicFiscalDocumentsBrazil%2FConfigurations%2FDocumentProviders):</span></span>

    - <span data-ttu-id="5857c-249">SubmitProvider.xml</span><span class="sxs-lookup"><span data-stu-id="5857c-249">SubmitProvider.xml</span></span>
    - <span data-ttu-id="5857c-250">ContingencyProvider.xml</span><span class="sxs-lookup"><span data-stu-id="5857c-250">ContingencyProvider.xml</span></span>

1. <span data-ttu-id="5857c-251">**Retail と Commerce \> チャネル設定 \> 会計統合 \> コネクタ機能プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-251">Go to **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector functional profiles**.</span></span>
1. <span data-ttu-id="5857c-252">コンフィギュレーションを読み込んだばかりのドキュメント プロバイダーごとに、コネクタ機能プロファイルを作成し、既にコンフィギュレーションを読み込んだ会計コネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-252">For each document provider that you just loaded the configuration for, create connector functional profiles, and select the fiscal connectors that you loaded the configuration for earlier.</span></span> <span data-ttu-id="5857c-253">必要に応じて、データ マッピング設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="5857c-253">Update data mapping settings as required.</span></span>
1. <span data-ttu-id="5857c-254">**Retail とコマース \> チャネル設定 \> 会計統合 \> コネクタ技術プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-254">Go to **Retail and Commerce \> Channel setup \> Fiscal integration \> Connector technical profiles**.</span></span>
1. <span data-ttu-id="5857c-255">3 つのコネクタ技術プロファイルを作成し、既にコンフィギュレーションを読み込んだ会計コネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-255">Create three connector technical profiles, and select the fiscal connectors that you loaded the configuration for earlier.</span></span> <span data-ttu-id="5857c-256">必要に応じて、接続設定を更新します。</span><span class="sxs-lookup"><span data-stu-id="5857c-256">Update connection settings as required.</span></span>
1. <span data-ttu-id="5857c-257">**Retail と Commerc \> チャネル設定 \> 会計統合 \> 会計コネクタ グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-257">Go to **Retail and Commerce \> Channel setup \> Fiscal integration \> Fiscal connector group**.</span></span>
1. <span data-ttu-id="5857c-258">既に作成した各コネクタ機能プロファイル用に 3 つの会計コネクタ グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-258">Create three fiscal connector groups, one for each connector functional profile that you created earlier.</span></span>
1. <span data-ttu-id="5857c-259">**Retail と Commerce \> チャネル設定 \> 会計統合 \> 登録プロセス** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-259">Go to **Retail and Commerce \> Channel setup \> Fiscal integration \> Registration process**.</span></span>
1. <span data-ttu-id="5857c-260">登録プロセスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-260">Create a registration process.</span></span> <span data-ttu-id="5857c-261">登録手順として、作成した会計コネクタ グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-261">As registration steps, select the fiscal connector groups that you just created.</span></span>
1. <span data-ttu-id="5857c-262">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 機能プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-262">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="5857c-263">登録プロセスを有効化する店舗にリンクされている機能プロファイルを選択し、**会計登録プロセス** のクイック タブで、作成した登録プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-263">Select the functionality profile that is linked to the store where the registration process should be activated, and then, on the **Fiscal registration process** FastTab, select the registration process that you just created.</span></span> <span data-ttu-id="5857c-264">POS での非会計イベントの登録を有効にするには、**機能** クイック タブで、**監査** オプションを **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-264">To enable registration of non-fiscal events in POS, on the **Functions** FastTab, set the **Audit** option to **No**.</span></span>
1. <span data-ttu-id="5857c-265">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-265">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
1. <span data-ttu-id="5857c-266">会計プリンターの接続先のハードウェア ステーションにリンクされているハードウェア プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-266">Select a hardware profile that is linked to the hardware station that the fiscal printer will be connected to.</span></span>
1. <span data-ttu-id="5857c-267">**会計周辺機器** クイック タブで、コネクタの技術的なプロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-267">On the **Fiscal peripherals** FastTab, select the connector technical profile.</span></span>
1. <span data-ttu-id="5857c-268">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> ハードウェア プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-268">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Hardware profiles**.</span></span>
1. <span data-ttu-id="5857c-269">プリンターのハードウェア プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-269">Set up hardware profiles for printers.</span></span>
1. <span data-ttu-id="5857c-270">**店舗** ページの **ハードウェア ステーション** クイック タブで、ハードウェア ステーションの設定を追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-270">On the **Stores** page, on the **Hardware stations** FastTab, add a setup for the hardware station.</span></span> <span data-ttu-id="5857c-271">必要に応じて、既に構成したネットワーク プリンターの IP アドレスを構成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-271">As required, configure IP addresses for the network printer that you configured earlier.</span></span>

## <a name="customer-information-management"></a><span data-ttu-id="5857c-272">顧客情報管理</span><span class="sxs-lookup"><span data-stu-id="5857c-272">Customer information management</span></span>

<span data-ttu-id="5857c-273">**顧客情報の追加** 操作を使用して、CNPJ (Cadastro Nacional da Pessoa Jurídica)/CPF (Cadastro de Pessoas Físicas) 番号などのブラジル固有の顧客税登録番号、および住所を販売トランザクションに追加できます。</span><span class="sxs-lookup"><span data-stu-id="5857c-273">The **Add customer information** operation can be used to add Brazil-specific customer tax registration numbers, such as CNPJ (Cadastro Nacional da Pessoa Jurídica)/CPF (Cadastro de Pessoas Físicas) numbers, and addresses to sales transactions.</span></span> <span data-ttu-id="5857c-274">顧客情報は、トランザクションに対して指定された顧客レコードから引き出す場合も、手動で入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="5857c-274">Customer information can be pulled from the customer record that is specified for the transaction, or it can be manually entered.</span></span> <span data-ttu-id="5857c-275">顧客情報を DANFE の会計レシートに印刷して、請求に使用できます。</span><span class="sxs-lookup"><span data-stu-id="5857c-275">The customer information can then be printed on DANFE fiscal receipts and used for invoicing purposes.</span></span>

<span data-ttu-id="5857c-276">Commerce 本社で **顧客住所の追加** を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5857c-276">To configure the **Add customer information** operation in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="5857c-277">**Retail と Commerce \> チャネル設定 \> POS 設定 \> POS \> ボタン グリッド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-277">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Button grids**.</span></span>
1. <span data-ttu-id="5857c-278">操作を表示するボタン グリッドを選択し、**ボタン グリッド デザイナー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="5857c-278">Select the button grid where the operation should appear, and then open **Button grid designer**.</span></span>
1. <span data-ttu-id="5857c-279">ボタンを追加し、**アクション** フィールドで **顧客情報の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-279">Add a button, and then, in the **Action** field, select **Add customer information**.</span></span>

<span data-ttu-id="5857c-280">画面のレイアウトとボタン グリッドの操作方法の詳細については、[販売時点管理 (POS) の画面レイアウト](../pos-screen-layouts.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-280">For more information about how to work with screen layouts and button grids, see [Screen layouts for the point of sale (POS)](../pos-screen-layouts.md).</span></span>

## <a name="set-up-parameters-for-statements"></a><span data-ttu-id="5857c-281">ステートメントのパラメーターを設定します</span><span class="sxs-lookup"><span data-stu-id="5857c-281">Set up parameters for statements</span></span>

1. <span data-ttu-id="5857c-282">**組織管理 \> 番号順序** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-282">Go to **Organization administration \> Number sequences**.</span></span>
1. <span data-ttu-id="5857c-283">各店舗 (作業単位) の小売明細書の番号順序を作成および設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-283">Create and set up number sequences for retail statements for each store (operating unit).</span></span>
1. <span data-ttu-id="5857c-284">**参照** クイック タブで、**小売店舗** 領域に対して 2 つの参照を追加します。1 つは **参照値** が **明細書番号** に設定され、もう 1 つは **伝票** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="5857c-284">On the **References** FastTab, add two references for the **Retail store** area: one where the **Reference** value is set to **Statement number** and one where it's set to **Voucher**.</span></span>
1. <span data-ttu-id="5857c-285">**Retail と Commerce \> カタログと品揃え** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-285">Go to **Retail and Commerce \> Catalog and assortments**.</span></span>
1. <span data-ttu-id="5857c-286">適切な製品を含む品揃えを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-286">Create an assortment that includes appropriate products.</span></span>
1. <span data-ttu-id="5857c-287">**Commerce チャネル** タブで、既に作成した店舗を追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-287">On the **Commerce channels** tab, add the stores that you created earlier.</span></span> <span data-ttu-id="5857c-288">次に、**公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-288">Then select **Publish**.</span></span>
1. <span data-ttu-id="5857c-289">**Retail と Commerce \> チャネル設定 \> チャネル カテゴリと製品属性** に移動し、チャネル更新を公開します。</span><span class="sxs-lookup"><span data-stu-id="5857c-289">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**, and publish channel updates.</span></span>
1. <span data-ttu-id="5857c-290">**販売とマーケティング \> 設定 > 返品 \> 廃棄コード** に移動し、廃棄コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-290">Go to **Sales and marketing \> Setup > Returns \> Disposition codes**, and add a disposition code.</span></span>
1. <span data-ttu-id="5857c-291">**Retail と Commerce \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-291">Go to **Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="5857c-292">ギフト カードの製品を選択し、**レジスターでブロック** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-292">Select a product for the gift card, and then select the **Blocked at register** check box.</span></span>
1. <span data-ttu-id="5857c-293">**Retail と Commerce \> 本社の設定 \> パラメーター \> コマース パラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="5857c-293">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span>
1. <span data-ttu-id="5857c-294">**顧客注文** タブで、既に追加した廃棄コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-294">On the **Customer orders** tab, enter the disposition code that you added earlier.</span></span>
1. <span data-ttu-id="5857c-295">**転記** タブで、ギフト カードのパラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="5857c-295">On the **Posting** tab, set up the parameters for the gift card.</span></span> <span data-ttu-id="5857c-296">これらのパラメータには、ギフト **ギフト カード会社** および **ギフト カード製品** フィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5857c-296">These parameters include the **Gift card company** and **Gift card product** fields.</span></span>

## <a name="configure-a-production-environment"></a><span data-ttu-id="5857c-297">運用環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5857c-297">Configure a production environment</span></span>

<span data-ttu-id="5857c-298">このセクションは、ブラジル向け Commerce のローカライズの Commerce コンポーネントを有効にするための配置ガイドを提供します。</span><span class="sxs-lookup"><span data-stu-id="5857c-298">This section provides deployment guidance that will help you enable Commerce components of the Commerce localization for Brazil.</span></span>

> [!NOTE]
> <span data-ttu-id="5857c-299">これらの手順の一部の手順は、使用している製品バージョンによって異なります。</span><span class="sxs-lookup"><span data-stu-id="5857c-299">Some steps in these procedures vary, depending on the product version that you're using.</span></span> <span data-ttu-id="5857c-300">詳細については、 [Dynamics 365 for Retail の新機能および変更された機能](../get-started/whats-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-300">For more information, see [What's new or changed in Dynamics 365 for Retail](../get-started/whats-new.md).</span></span>

### <a name="use-certificates-for-authentication-with-the-tax-authority-service-and-digital-signing-of-fiscal-documents"></a><span data-ttu-id="5857c-301">税務当局サービスによる認証と会計ドキュメントのデジタル署名に証明書を使用する</span><span class="sxs-lookup"><span data-stu-id="5857c-301">Use certificates for authentication with the tax authority service and digital signing of fiscal documents</span></span>

<span data-ttu-id="5857c-302">Application Object Server (AOS) のデジタル証明書は、Azure Key Vault に格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-302">A digital certificate for Application Object Server (AOS) must be stored in Azure Key Vault.</span></span>

<span data-ttu-id="5857c-303">Retail Server のデジタル証明書は、ローカルにインストールするか、Key Vault に格納する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-303">Digital certificates for Retail Server must be installed locally or stored in Key Vault.</span></span> <span data-ttu-id="5857c-304">Retail Server の両方の場所のタイプを同時に構成し、その優先順位に従って使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="5857c-304">Both location types for Retail Server can also be configured simultaneously and used according to their priorities.</span></span>

<span data-ttu-id="5857c-305">Key Vault ストレージを操作する方法の詳細については、[Azure Key Vault の使用を開始](/azure/key-vault/key-vault-get-started) および [Azure Key Vault クライアントの設定](../../finance/localizations/setting-up-azure-key-vault-client.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-305">For more information about how to work with Key Vault storage, see [Get started with Azure Key Vault](/azure/key-vault/key-vault-get-started) and [Set up the Azure Key Vault client](../../finance/localizations/setting-up-azure-key-vault-client.md).</span></span>

<span data-ttu-id="5857c-306">Key Vault または Commerce 本社が使用できない場合に、オフラインにするためのフェールオーバーをサポートする[小売店舗のユーザー定義の証明書プロファイル](./certificate-profiles-for-retail-stores.md) を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="5857c-306">You can also use the [User-defined certificate profiles for retail stores](./certificate-profiles-for-retail-stores.md) feature that supports failover to offline when Key Vault or Commerce headquarters isn't available.</span></span> <span data-ttu-id="5857c-307">この機能は、[小売チャンネルのシークレットを管理 ](../dev-itpro/manage-secrets.md) 機能を拡張します。</span><span class="sxs-lookup"><span data-stu-id="5857c-307">This feature extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature.</span></span>

> [!NOTE]
> <span data-ttu-id="5857c-308">NFC-e ドキュメントをオフライン代替モードで署名できるようにするには、POS のオフライン証明書ストレージに証明書をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-308">To enable NFC-e documents to be signed in offline contingency mode, you must install a certificate in the offline certificate storage of the POS.</span></span> <span data-ttu-id="5857c-309">詳細については、[オフライン代替モードでの商品の現金店頭払い売上の作成](latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) および[代替モードで発行された NFC-e の登録の延期](latam-bra-nfce-contingency-mode.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-309">For more information, see [Make a cash-and-carry sale of goods in offline contingency mode](latam-bra-nfce.md#scenario-3-make-a-cash-and-carry-sale-of-goods-in-offline-contingency-mode) and [Postponed registration of NFC-e issued in contingency mode](latam-bra-nfce-contingency-mode.md).</span></span>

#### <a name="configure-certificates-so-that-they-can-be-used-in-retail-server"></a><span data-ttu-id="5857c-310">Retail Server で使用できる証明書を構成する</span><span class="sxs-lookup"><span data-stu-id="5857c-310">Configure certificates so that they can be used in Retail Server</span></span>

<span data-ttu-id="5857c-311">Retail Server のブラジルの税務サービス拡張機能は、税務当局サービスによる認証と会計ドキュメントのデジタル署名に証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="5857c-311">The Brazilian tax service extension of Retail Server uses a certificate for authentication with the tax authority service and digital signing of fiscal documents.</span></span> <span data-ttu-id="5857c-312">Retail Server 証明書の設定は証明書プロファイルによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="5857c-312">The settings for Retail Server certificates are controlled by certificate profiles.</span></span>

<span data-ttu-id="5857c-313">Retail Server で使用できる証明書を構成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="5857c-313">To configure certificates so that they can be used in Retail Server, follow these steps.</span></span>

1. <span data-ttu-id="5857c-314">**システム管理 \> 設定 \> 証明書プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-314">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
1. <span data-ttu-id="5857c-315">適切な法人の証明書プロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-315">Create a certificate profile for the appropriate legal entities.</span></span>
1. <span data-ttu-id="5857c-316">各法人について、**設定** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5857c-316">For each legal entity, select **Settings**, and then follow these steps:</span></span>

    - <span data-ttu-id="5857c-317">ローカル証明書の場合は、**場所タイプ** フィールドが **ローカル証明書** に設定されているレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5857c-317">For the local certificate, create a record where the **Location type** field is set to **Local certificate**.</span></span> <span data-ttu-id="5857c-318">次に、**拇印** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5857c-318">Then, in the **Thumbprint** field, enter a value.</span></span>
    - <span data-ttu-id="5857c-319">Key Vault 証明書の場合は、**場所のタイプ** フィールドが **Key Vault** に設定されているレコードを作成し、**Key Vault 証明書** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-319">For the Key Vault certificate, create a record where the **Location type** field is set to **Key Vault**, and then select **Key Vault certificate**.</span></span>

<span data-ttu-id="5857c-320">証明書は、Retail Server または Key Vault が配置されているマシンのローカルの証明書のストレージにインストールされます。</span><span class="sxs-lookup"><span data-stu-id="5857c-320">Certificates can be installed in the local certificate storage of the machine where Retail Server is deployed or in Key Vault.</span></span> <span data-ttu-id="5857c-321">または、両方の場所タイプにインストールして同時に構成し、優先順位に従って使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="5857c-321">Alternatively, they can be installed in both location types and configured simultaneously so that they are used according to their priorities.</span></span>

#### <a name="configure-a-certificate-in-aos"></a><span data-ttu-id="5857c-322">AOS で証明書の構成</span><span class="sxs-lookup"><span data-stu-id="5857c-322">Configure a certificate in AOS</span></span>

<span data-ttu-id="5857c-323">税務当局サービスとの認証用の証明書は、Key Vault に格納されます。</span><span class="sxs-lookup"><span data-stu-id="5857c-323">A certificate for authentication with the tax authority service is stored in Key Vault.</span></span> <span data-ttu-id="5857c-324">この証明書は AOS で使用され、Commerce 本社を通じて、オフライン代替モードの POS で発行された NFC-e ドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="5857c-324">This certificate is used in AOS to submit, through Commerce headquarters, NFC-e documents that were issued in POS in offline contingency mode.</span></span> <span data-ttu-id="5857c-325">「破棄」要求および「置換によるキャンセル」要求のデジタル署名には、証明書も必要です。</span><span class="sxs-lookup"><span data-stu-id="5857c-325">The certificate is also required for digital signing of "discard" and "cancellation by substitution" requests.</span></span> <span data-ttu-id="5857c-326">証明書のパラメータは、会計施設の設定で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-326">Parameters of the certificate must be specified in the fiscal establishment settings.</span></span>

<span data-ttu-id="5857c-327">AOS で証明書を構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5857c-327">To configure a certificate in AOS, follow these steps.</span></span>

1. <span data-ttu-id="5857c-328">**組織管理 \> 組織 \> 会計機関 \> 会計施設** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5857c-328">Go to **Organization administration \> Organizations \> Fiscal establishments \> Fiscal establishments**.</span></span>
1. <span data-ttu-id="5857c-329">税務当局サービスによる認証と会計ドキュメントのデジタル署名に適切なデジタル証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="5857c-329">Select the appropriate digital certificate for authentication with the tax authority service and digital signing of fiscal documents.</span></span>

> [!NOTE]
> <span data-ttu-id="5857c-330">設定が完了したら、Commerce 本社で適切な配送ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-330">After the setup is completed, the appropriate distribution jobs must be run in Commerce headquarters.</span></span>

### <a name="configure-crt-extension-components"></a><span data-ttu-id="5857c-331">CRT 拡張コンポーネントを構成</span><span class="sxs-lookup"><span data-stu-id="5857c-331">Configure CRT extension components</span></span>

<span data-ttu-id="5857c-332">CRT 拡張コンポーネントを構成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5857c-332">To configure CRT extension components, follow these steps.</span></span>

1. <span data-ttu-id="5857c-333">CRT 用拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="5857c-333">Find the extension configuration file for CRT.</span></span>

    - <span data-ttu-id="5857c-334">**Commerce Scale Unit:** ファイルは **Commerceruntime.ext.config** という名前で、インターネット インフォメーション サービス (IIS) Commerce Scale Unit サイトの下の **bin\\ext** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="5857c-334">**Commerce Scale Unit:** The file is named **Commerceruntime.ext.config**, and it's located in the **bin\\ext** folder under the Internet Information Services (IIS) Commerce Scale Unit site location.</span></span>

2. <span data-ttu-id="5857c-335">拡張コンフィギュレーション ファイルで CRT の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="5857c-335">Register the CRT change in the extension configuration file.</span></span>

```xml
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalServiceBrazil" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalDocumentBrazil" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdBrazil" />
<add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxServiceBrazil" />
 ```

3. <span data-ttu-id="5857c-336">Local CRT on Modern POS の拡張コンフィギュレーション ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="5857c-336">Find the extension configuration file for Local CRT on Modern POS:</span></span>

    - <span data-ttu-id="5857c-337">**Local CRT on Modern POS:** ファイル名は **CommerceRuntime.MPOSOffline.Ext.config** で、ローカル CRT クライアント ブローカーの場所にあります。</span><span class="sxs-lookup"><span data-stu-id="5857c-337">**Local CRT on Modern POS:** The file is named **CommerceRuntime.MPOSOffline.Ext.config**, and it's located in the local CRT client broker location.</span></span>

4. <span data-ttu-id="5857c-338">拡張コンフィギュレーション ファイルで Local CRT on Modern POS の変更を登録します。</span><span class="sxs-lookup"><span data-stu-id="5857c-338">Register the local CRT on Modern POS change in the extension configuration file.</span></span>

 ```xml
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicReporting" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalDocumentBrazil.Offline" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ElectronicFiscalDocumentBrazil" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxRegistrationIdBrazil" />
 <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.TaxServiceBrazil" />
 ```

> [!WARNING]
> <span data-ttu-id="5857c-339">**Commerceruntime.config** および **CommerceRuntime.MPOSOffline.config** ファイルを編集してはいけません。</span><span class="sxs-lookup"><span data-stu-id="5857c-339">Don't edit the **Commerceruntime.config** and **CommerceRuntime.MPOSOffline.config** files.</span></span> <span data-ttu-id="5857c-340">これらのファイルはカスタマイズのためのものではありません。</span><span class="sxs-lookup"><span data-stu-id="5857c-340">These files aren't intended for any customizations.</span></span>

### <a name="enable-modern-pos-extension-components"></a><span data-ttu-id="5857c-341">Modern POS 拡張コンポーネントの有効化</span><span class="sxs-lookup"><span data-stu-id="5857c-341">Enable Modern POS extension components</span></span>

<span data-ttu-id="5857c-342">Modern POS 拡張コンポーネントを有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5857c-342">To enable Modern POS extension components, follow these steps.</span></span>

1. <span data-ttu-id="5857c-343">**RetailSdk\\POS\\ModernPOS.sln** でソリューションを開き、エラーなくコンパイルできるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="5857c-343">Open the solution at **RetailSdk\\POS\\ModernPOS.sln**, and make sure that it can be compiled without errors.</span></span> <span data-ttu-id="5857c-344">また、**実行** コマンドを使用して、Visual Studio から Modern POS を実行できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5857c-344">Additionally, confirm that you can run Modern POS from Visual Studio by using the **Run** command.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5857c-345">Modern POS をカスタマイズしないでください。</span><span class="sxs-lookup"><span data-stu-id="5857c-345">Modern POS must not be customized.</span></span> <span data-ttu-id="5857c-346">ユーザー アカウント制御 (UAC) を有効にして、要求に応じて以前にインストールした Modern POS のインスタンスをアンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5857c-346">You must enable User Account Control (UAC), and you must uninstall previously installed instances of Modern POS as required.</span></span>

1. <span data-ttu-id="5857c-347">**extensions.json** ファイルで、次の明細行を追加することによって拡張機能が読み込まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="5857c-347">Enable the extensions to be loaded by adding the following lines in the **extensions.json** file.</span></span>

    ```json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/ElectronicFiscalDocument.BR"
            },
            {
                "baseUrl": "Microsoft/TaxRegistrationId.BR"
            }
        ]
    }
    ```

    > [!NOTE]
    > <span data-ttu-id="5857c-348">詳細については、およびソース コード フォルダーを含め、拡張機能の読み込みを有効にする方法を示すサンプルについては、**Pos.Extensions** プロジェクトの readme.md ファイル内にある手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5857c-348">For more information, and for samples that show how to include source code folders and enable extensions to be loaded, see the instructions in the readme.md file of the **Pos.Extensions** project.</span></span>

1. <span data-ttu-id="5857c-349">ソリューションをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="5857c-349">Rebuild the solution.</span></span>
1. <span data-ttu-id="5857c-350">デバッガーでModern POS を実行し、機能をテストします。</span><span class="sxs-lookup"><span data-stu-id="5857c-350">Run Modern POS in the debugger, and test the functionality.</span></span>

### <a name="enable-cloud-pos-extension-components"></a><span data-ttu-id="5857c-351">Cloud POS 拡張コンポーネントの有効化</span><span class="sxs-lookup"><span data-stu-id="5857c-351">Enable Cloud POS extension components</span></span>

<span data-ttu-id="5857c-352">Cloud POS の拡張機能コンポーネントを **extensions.json** ファイルに読み込むには、次の行をファイルの適切な部分に追加します。</span><span class="sxs-lookup"><span data-stu-id="5857c-352">To enable the Cloud POS extension components to be loaded in the **extensions.json** file, add the following lines in the appropriate part of the file.</span></span>

```json
{
    "extensionPackages": [
        {
            "baseUrl": "Microsoft/ElectronicFiscalDocument.BR"
        },
        {
            "baseUrl": "Microsoft/TaxRegistrationId.BR"
        }
    ]
}
```

## <a name="additional-resources"></a><span data-ttu-id="5857c-353">追加リソース</span><span class="sxs-lookup"><span data-stu-id="5857c-353">Additional resources</span></span>

[<span data-ttu-id="5857c-354">ブラジル向け Commerce ローカライズ</span><span class="sxs-lookup"><span data-stu-id="5857c-354">Commerce localization for Brazil</span></span>](latam-bra-commerce-localization.md) 

[<span data-ttu-id="5857c-355">ブラジル向け Commerce POS の NFC-e 電子会計ドキュメント</span><span class="sxs-lookup"><span data-stu-id="5857c-355">NFC-e fiscal document functionality in Commerce POS for Brazil</span></span>](latam-bra-nfce.md)

[<span data-ttu-id="5857c-356">ブラジルの POS で顧客情報を管理</span><span class="sxs-lookup"><span data-stu-id="5857c-356">Manage customer information in POS for Brazil</span></span>](latam-bra-customer-information.md)

[<span data-ttu-id="5857c-357">ブラジルの Commerce POS での NFC-e ドキュメントのキャンセルと返却</span><span class="sxs-lookup"><span data-stu-id="5857c-357">Cancellation and return of NFC-e documents in Commerce POS for Brazil</span></span>](latam-bra-nfce-cancel-return.md)

[<span data-ttu-id="5857c-358">オフライン代替モードで発行された NFC-e ドキュメントの登録の延期</span><span class="sxs-lookup"><span data-stu-id="5857c-358">Postponed registration of NFC-e documents issued in offline contingency mode</span></span>](latam-bra-nfce-contingency-mode.md)

[<span data-ttu-id="5857c-359">Commerce 本社の小売明細書を介してブラジルの会計ドキュメントを投稿</span><span class="sxs-lookup"><span data-stu-id="5857c-359">Post Brazilian fiscal documents via retail statements in Commerce headquarters</span></span>](latam-bra-retail-statements.md)

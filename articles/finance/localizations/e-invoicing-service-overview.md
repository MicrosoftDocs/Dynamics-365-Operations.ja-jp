---
title: 電子請求書アドオン機能の概要
description: このトピックでは、Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management で電子請求のアドオンを設定する方法について説明します。
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
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffd48e173b66cc6d2571e666d5452a5eff05176c
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/19/2020
ms.locfileid: "4445363"
---
# <a name="electronic-invoicing-add-on-overview"></a><span data-ttu-id="c6ffa-103">電子請求書アドオン機能の概要</span><span class="sxs-lookup"><span data-stu-id="c6ffa-103">Electronic invoicing add-on overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6ffa-104">Microsoft Dynamics 365 Finance および、Dynamics 365 Supply Chain Management の電子請求書アドオンは、電子請求書ドキュメントの構成可能な処理と構成可能な訴求メント交換を可能にする高スケーラブルなマルチ テナントサービスです。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-104">The Electronic invoicing add-on for Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management is a hyper-scalable multitenant service that enables configurable processing of electronic invoice documents and configurable document exchange.</span></span> <span data-ttu-id="c6ffa-105">処理と統合のルールは完全に構成をすることが可能で、このロジックは財務と Supply Chain Management の外部で実行されます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-105">The processing and integration rules are fully configurable, and the logic is run outside Finance and Supply Chain Management.</span></span> <span data-ttu-id="c6ffa-106">本サービスは、主に企業間の電子請求書の処理を対象としていますが、それ以外の用途にも独自の構成をすることが可能です。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-106">The service is targeted mainly at e-invoice processing in business-to-government scenarios, but it can be custom-configured for other purposes.</span></span>

<span data-ttu-id="c6ffa-107">電子請求のアドオンを使用すると、次のような目標の達成に役立ちます :</span><span class="sxs-lookup"><span data-stu-id="c6ffa-107">The Electronic invoicing add-on can help you achieve the following goals:</span></span>

- <span data-ttu-id="c6ffa-108">国/地域固有の要件を迅速かつ簡単に取り入れる</span><span class="sxs-lookup"><span data-stu-id="c6ffa-108">Fast and easy adoption of country/region-specific requirements</span></span>
- <span data-ttu-id="c6ffa-109">電子請求書のアドオン ソリューションの標準化された実装</span><span class="sxs-lookup"><span data-stu-id="c6ffa-109">Standardized implementations of an Electronic invoicing add-on solution</span></span>
- <span data-ttu-id="c6ffa-110">ドキュメント履歴の追跡機能の強化</span><span class="sxs-lookup"><span data-stu-id="c6ffa-110">Enhanced traceability of document history</span></span>
- <span data-ttu-id="c6ffa-111">短い実装サイクル</span><span class="sxs-lookup"><span data-stu-id="c6ffa-111">Shorter implementation cycle</span></span>
- <span data-ttu-id="c6ffa-112">総保有コスト (TCO) を削減する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-112">Reduced total cost of ownership (TCO)</span></span>
- <span data-ttu-id="c6ffa-113">コードの変更を必要としない構成を簡単に調整する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-113">Easily adjustable configurations that don't required code changes</span></span>
- <span data-ttu-id="c6ffa-114">簡素化された構成のパッケージ化</span><span class="sxs-lookup"><span data-stu-id="c6ffa-114">Simplified configuration packaging</span></span>
- <span data-ttu-id="c6ffa-115">組み込みのエクスポート、インポート、統合、および電子請求書ドキュメントの処理における容易な拡張性</span><span class="sxs-lookup"><span data-stu-id="c6ffa-115">Built-in export, import, and integration, and easy extensibility in the processing of e-invoice documents</span></span>
- <span data-ttu-id="c6ffa-116">複数の会社間で同一のエクスポート、インポート、統合の構成を簡単に再利用する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-116">Easy reuse of the same export, import, and integration configurations across companies</span></span>

<span data-ttu-id="c6ffa-117">電子請求書のアドオンを使用するには、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトからインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-117">To use the Electronic invoicing add-on, you must install it from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="c6ffa-118">次に、セットアップ手順に従って、財務または Supply Chain Management との統合を有効化します。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-118">Next, follow the setup procedure to turn on the integration with Finance or Supply Chain Management.</span></span> <span data-ttu-id="c6ffa-119">詳細情報については、[電子請求書アドオンの使用を開始する](e-invoicing-get-started.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-119">For more information, see [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="availability"></a><span data-ttu-id="c6ffa-120">適用の対象</span><span class="sxs-lookup"><span data-stu-id="c6ffa-120">Availability</span></span>

<span data-ttu-id="c6ffa-121">初期段階において、電子請求書作成のアドオンは、プレビュー プログラムを介して選ばれた顧客が利用できます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-121">Initially, the Electronic invoicing add-on is available to selected customers through a preview program.</span></span> <span data-ttu-id="c6ffa-122">後日、より多くの顧客にプレビューを公開する予定です。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-122">Later, the preview will be opened to a wider range of customers.</span></span> <span data-ttu-id="c6ffa-123">最終的には、サービスが一般的に利用可能となります。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-123">Finally, the service will become generally available.</span></span> <span data-ttu-id="c6ffa-124">国/地域固有の要件に対応する機能は、リリースの段階によっては制限がされる場合があるため、サポートされている国/地域固有となるソリューションの範囲および、範囲を示す最新のドキュメントを常に確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-124">Because functionality that addresses country/region-specific requirements might be limited at different phases of the release, you should always check the most up-to-date documentation that highlights the coverage and scope of supported country/region-specific solutions.</span></span>

<span data-ttu-id="c6ffa-125">電子請求のアドオンは、次の Azure の地域で展開されます :</span><span class="sxs-lookup"><span data-stu-id="c6ffa-125">The Electronic invoicing add-on is deployed in the following Azure geographies:</span></span>

- <span data-ttu-id="c6ffa-126">米国</span><span class="sxs-lookup"><span data-stu-id="c6ffa-126">United States</span></span>
- <span data-ttu-id="c6ffa-127">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="c6ffa-127">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="c6ffa-128">電子請求書のアドオンは、オンプレミスのデプロイに対応していません。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-128">The Electronic invoicing add-on doesn't support on-premises deployments.</span></span>

## <a name="extended-configurability"></a><span data-ttu-id="c6ffa-129">拡張された設定可能性</span><span class="sxs-lookup"><span data-stu-id="c6ffa-129">Extended configurability</span></span>

<span data-ttu-id="c6ffa-130">電子請求のアドオンは、電子ドキュメントを作成して指定された当事者に送信する必要がある場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-130">The Electronic invoicing add-on can be used in scenarios where you must create and send an electronic document to the designated parties.</span></span> <span data-ttu-id="c6ffa-131">受信したデータに基づいて、構成可能な処理の流れを実行する目的に特化しています。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-131">It's specifically designed for running a configurable flow of processing actions, based on received data.</span></span> <span data-ttu-id="c6ffa-132">財務および Supply Chain Management で使用できる構成のオプションは、ドキュメント変換に限定されます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-132">The configurability options that are available in Finance and Supply Chain Management are limited to document transformation.</span></span> <span data-ttu-id="c6ffa-133">サービスは、その中で利用可能となる構成可能な統合を追加することで、これらのオプションを拡張します。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-133">The service extends these options by adding the configurable integrations that are available in it.</span></span> <span data-ttu-id="c6ffa-134">さらに、ブラジルの Nota fiscaleletrônica (NF-e) 、メキシコの Comprobante Fiscal por Internet (CFDI) 、または他の西ヨーロッパの Universal Business Language (UBL) /Pan-European Public Procurement OnLine (PEPPOL) 機能など、これまで利用可能であったすべての電子請求書機能は、エクスポートおよびインポート用の構成を使用して外部 Web サービスとの統合を可能にします。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-134">In addition, all the electronic invoice functionalities that were previously available, such as Brazilian Nota fiscal eletrônica (NF-e), Mexican Comprobante Fiscal Digital por Internet (CFDI), or other Western European Universal Business Language (UBL)/Pan-European Public Procurement OnLine (PEPPOL) functionalities, will use configurations for export and import, and to enable integrations with external web services.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="c6ffa-135">機能の特徴</span><span class="sxs-lookup"><span data-stu-id="c6ffa-135">Feature highlights</span></span>

- <span data-ttu-id="c6ffa-136">財務および Supply Chain Management との既成の統合</span><span class="sxs-lookup"><span data-stu-id="c6ffa-136">Out-of-box integration with Finance and Supply Chain management</span></span>
- <span data-ttu-id="c6ffa-137">べての国や地域の電子請求書プロセスの設定と監視に使用する一貫したユーザー エクスペリエンス</span><span class="sxs-lookup"><span data-stu-id="c6ffa-137">Consistent user experience for the configuration and monitoring of the e-invoice process for all countries or regions</span></span>
- <span data-ttu-id="c6ffa-138">新しい国や地域での電子請求書アドオン ソリューションの導入をより早く、より簡単に、より低コストで行う</span><span class="sxs-lookup"><span data-stu-id="c6ffa-138">Faster, easier, and less expensive adoption of Electronic invoicing add-on solutions in new countries or regions</span></span>
- <span data-ttu-id="c6ffa-139">Regulatory Configuration Services (規制構成サービス) およびグローバリゼーション機能の設定を通したサービスの構成</span><span class="sxs-lookup"><span data-stu-id="c6ffa-139">Configuration of the service through the Regulatory Configuration Service (RCS) and Globalization feature setup</span></span>
- <span data-ttu-id="c6ffa-140">RCS で定義されている構成を使用してビジネス データを複数の電子請求書フォーマット (XML、JavaScript Object Notation \[JSON\]、テキスト、カンマ区切り値\[CSV\]) に変換する :</span><span class="sxs-lookup"><span data-stu-id="c6ffa-140">Transformation of business data into multiple e-invoice formats (XML, JavaScript Object Notation \[JSON\], TXT, and comma-separated values \[CSV\]) by using configurations that are defined in RCS:</span></span>

    - <span data-ttu-id="c6ffa-141">電子請求書の変換設定が使用できない国や地域で利用可能な電子レポートの形式</span><span class="sxs-lookup"><span data-stu-id="c6ffa-141">Electronic reporting formats that are available for countries or regions where configurability for e-invoice transformation isn't available</span></span>

- <span data-ttu-id="c6ffa-142">外部 Web サービスへの電子請求書の送信を構成可能 (電子署名による認証処理を含む):</span><span class="sxs-lookup"><span data-stu-id="c6ffa-142">Configurable submission of e-invoices to external web services, including certification handling through digital signatures:</span></span>

    - <span data-ttu-id="c6ffa-143">複数の国に対する追加コンテンツとの、組み込みの簡単で拡張性のある、構成可能な統合</span><span class="sxs-lookup"><span data-stu-id="c6ffa-143">Built-in, easily extendable, and configurable integration with additional content for several countries</span></span>

    > [!NOTE]
    > <span data-ttu-id="c6ffa-144">現時点では、対応している直接送信は限られています。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-144">Currently, a limited number of direct submissions are supported.</span></span> <span data-ttu-id="c6ffa-145">詳細については、前述の [可用性](#availability) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-145">For more information, see the [Availability](#availability) section earlier in this topic.</span></span> <span data-ttu-id="c6ffa-146">対応範囲はは今後拡張する予定です。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-146">Support will be extended in the future.</span></span>

- <span data-ttu-id="c6ffa-147">構成可能な例外メッセージ処理を含む、Web サービスからのレスポンスの処理</span><span class="sxs-lookup"><span data-stu-id="c6ffa-147">Handling of responses from web services, including configurable exception message handling</span></span>
- <span data-ttu-id="c6ffa-148">電子署名への対応 (XMLDSig 署名アルゴリズムの使用など)</span><span class="sxs-lookup"><span data-stu-id="c6ffa-148">Support for electronic signatures (for example, by using the XMLDSig signing algorithm)</span></span>
- <span data-ttu-id="c6ffa-149">電子請求メッセージの一括処理</span><span class="sxs-lookup"><span data-stu-id="c6ffa-149">Batch processing of e-invoice messages</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="c6ffa-150">アーキテクチャとデータ フロー</span><span class="sxs-lookup"><span data-stu-id="c6ffa-150">Architecture and data flow</span></span>

<span data-ttu-id="c6ffa-151">LCS から電子請求書アドオンをインストールし、必要となるアプリケーションでの必要な設定が完了すると、安全な接続が確立されます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-151">When the Electronic invoicing add-on is installed from LCS, and the required setup is completed in all required applications, a secure connection is established.</span></span> <span data-ttu-id="c6ffa-152">このサービスは現在、米国およびヨーロッパのデータ センターに配置されています。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-152">The service is currently located in data centers in the United States and Europe.</span></span> <span data-ttu-id="c6ffa-153">したがって、サービスの場所は、関連する財務または、Supply Chain Management インスタンスの場所とは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-153">Therefore, the service location might differ from the location of the related Finance or Supply Chain Management instance.</span></span> <span data-ttu-id="c6ffa-154">電子請求書アドオンの設定を完了し、統合をオンにすると、電子請求書が送信されるたびに特定のドキュメントに関連するマスター データとトランザクション データが電子請求書アドオンに送信されます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-154">After you complete the setup of the Electronic invoicing add-on and turn on the integration, whenever an electronic invoice is sent, master data and transactional data that are related to a specific document are sent to the Electronic invoicing add-on.</span></span>

> [!NOTE]
> <span data-ttu-id="c6ffa-155">電子請求書やその他のドキュメントに個人データが含まれている場合は、この機能を使用する際に一般データ保護規則 (GDPR) や個人データの転送に関するその他規制に準拠していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-155">If your electronic invoice or any other document contains personal data, verify that your use of this feature meets the General Data Protection Regulation (GDPR) and other regulations that are related to the transfer of personal data.</span></span>

### <a name="high-level-description-of-the-data-flow"></a><span data-ttu-id="c6ffa-156">データ フローの高レベルな概要</span><span class="sxs-lookup"><span data-stu-id="c6ffa-156">High-level description of the data flow</span></span>

1. <span data-ttu-id="c6ffa-157">クライアントは、標準的なビジネス ドキュメントをサービスに送信します。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-157">The client sends a canonical business document to the service.</span></span>
2. <span data-ttu-id="c6ffa-158">サービスは、クライアントから受信したコンテキスト情報に基づいて、該当する処理フローを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-158">Based on the context information that is received from the client, the service selects the applicable processing flow.</span></span>
3. <span data-ttu-id="c6ffa-159">サービスが処理アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-159">The service runs the processing actions.</span></span> <span data-ttu-id="c6ffa-160">これらのアクションには、ビジネス ドキュメントを電子請求書に変換したり、電子署名を適用したり、外部の Web サービスにドキュメントを送信したりすることが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-160">These actions might include transforming the business document into an electronic invoice, applying an electronic signature, and submitting the document to an external web service.</span></span>
4. <span data-ttu-id="c6ffa-161">受信したドキュメントや処理したドキュメントは、顧客の Azure Blob Storage に保存されています。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-161">All the received and processed documents are stored in the customer's Azure Blob storage.</span></span>
5. <span data-ttu-id="c6ffa-162">処理に使用したテナントのシークレットと証明書はすべて、顧客の Azure Key Vault に保存されています。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-162">All the tenant secrets and certificates that were used for processing are stored in the customer's Azure key vault.</span></span>
6. <span data-ttu-id="c6ffa-163">このサービスは、送信されたビジネス ドキュメントの処理状況をクライアントにオンデマンドで提供します。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-163">The service provides on-demand information to the client about the processing status of the business document that was sent.</span></span>
7. <span data-ttu-id="c6ffa-164">クライアントは、処理の完了情報を受信し、すべてのログ情報を利用可能にします。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-164">The client receives information about the completed processing execution and makes all the log information available.</span></span> <span data-ttu-id="c6ffa-165">また、フローの処理中に作成、受信されたドキュメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-165">It also makes the document that was created or received during flow processing available.</span></span>

<span data-ttu-id="c6ffa-166">次の図は、電子請求書アドオンのデータの流れを示しています。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-166">The following illustration shows how data flows to and from the Electronic invoicing add-on.</span></span>

![電子請求書アドオン設定のデータ フロー](media/e-invoicing-service-data-flow-diagram-overview.png)

## <a name="privacy-notice"></a><span data-ttu-id="c6ffa-168">プライバシー通知</span><span class="sxs-lookup"><span data-stu-id="c6ffa-168">Privacy notice</span></span>
<span data-ttu-id="c6ffa-169">電子請求書を有効化して使用するには、税務登録 ID を含む一部のデータの送信が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-169">Enabling and using Electronic invoicing may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="c6ffa-170">これは、政府の web サービスとの統合に必要となる事前定義された形式で電子請求書を送信する目的で、税務当局によって認可された第三者機関に送信されます。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-170">This will be transmitted to third-party agencies authorized by the tax authorities for purposes of sending electronic invoices in the predefined formats required for integration with these government’s web services.</span></span> <span data-ttu-id="c6ffa-171">これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-171">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="c6ffa-172">詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6ffa-172">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6ffa-173">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6ffa-173">Additional resources</span></span>

- [<span data-ttu-id="c6ffa-174">電子請求書のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-174">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="c6ffa-175">ブラジル向け電子請求のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-175">Get started with the Electronic invoicing add-on for Brazil</span></span>](e-invoicing-bra-get-started.md)
- [<span data-ttu-id="c6ffa-176">メキシコ向け電子請求のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-176">Get started with the Electronic invoicing add-on for Mexico</span></span>](e-invoicing-mex-get-started.md)
- [<span data-ttu-id="c6ffa-177">イタリア向け電子請求書のアドオンの使用を開始する</span><span class="sxs-lookup"><span data-stu-id="c6ffa-177">Get started with the Electronic invoicing add-on for Italy</span></span>](e-invoicing-ita-get-started.md)
- [<span data-ttu-id="c6ffa-178">電子請求のアドオン設定</span><span class="sxs-lookup"><span data-stu-id="c6ffa-178">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)

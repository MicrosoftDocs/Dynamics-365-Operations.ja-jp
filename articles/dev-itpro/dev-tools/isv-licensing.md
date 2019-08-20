---
title: 独立系ソフトウェア ベンダー (ISV) ライセンス
description: このトピックでは、独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。 これには、ISV のライセンス機能の長所および機能に関する情報が含まれており、ISV ソリューションのライセンスを有効にする方法、パッケージの作成方法、顧客固有のライセンスの生成方法およびテスト目的で自己署名証明書を作成する方法について説明しています。
author: robadawy
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bccf09360b91bd58958b55436d098d64fd081246
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833534"
---
# <a name="independent-software-vendor-isv-licensing"></a><span data-ttu-id="f31da-104">独立系ソフトウェア ベンダー (ISV) ライセンス</span><span class="sxs-lookup"><span data-stu-id="f31da-104">Independent software vendor (ISV) licensing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f31da-105">このトピックでは、独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="f31da-105">This topic describes the independent software vendor (ISV) licensing feature.</span></span> <span data-ttu-id="f31da-106">これには、ISV のライセンス機能の長所および機能に関する情報が含まれており、ISV ソリューションのライセンスを有効にする方法、パッケージの作成方法、顧客固有のライセンスの生成方法およびテスト目的で自己署名証明書を作成する方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="f31da-106">It includes information about benefits and capabilities of the ISV licensing feature, and explains how to enable licensing for an ISV solution, create a package and generate a customer-specific license, and create self-signed certificates for test purposes.</span></span>

<span data-ttu-id="f31da-107">Microsoft Dynamics エコシステムには、独立系ソフトウェア ベンダー (ISV) が再パッケージ化可能な業種ソリューションをビルド、配置、販売して収益化できるようにするツールとフレームワークが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f31da-107">The Microsoft Dynamics ecosystem provides tools and frameworks that let independent software vendors (ISVs) build, deploy, sell, and therefore monetize vertical industry solutions that can be repackaged.</span></span> <span data-ttu-id="f31da-108">ISV ライセンス機能には、次の利点があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-108">The ISV licensing feature provides the following benefits:</span></span>

-   <span data-ttu-id="f31da-109">これは、顧客およびパートナーに ISV ソリューションのより安全なライセンス メカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="f31da-109">It provides a safer licensing mechanism for ISV solutions for customers and partners.</span></span> <span data-ttu-id="f31da-110">ISV ソリューションは、顧客が ISV から有効なライセンス キーを購入した場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="f31da-110">ISV solutions are enabled only if the customer has purchased a valid license key from the ISV.</span></span>
-   <span data-ttu-id="f31da-111">これにより、顧客が異なる ISV からの ISV ソリューションのライセンスをどのように処理するかが調整されるため、総保有コスト (TCO) を削減します。</span><span class="sxs-lookup"><span data-stu-id="f31da-111">It aligns how customers handle licenses for ISV solutions from different ISVs, and therefore lowers the total cost of ownership (TCO).</span></span>
-   <span data-ttu-id="f31da-112">ISV は、業界標準のフレームワークを使用して、ISV ライセンスを個別に生成、管理、配布することができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-112">ISVs can independently generate, manage, and distribute ISV licenses by using industry standard frameworks.</span></span>

<span data-ttu-id="f31da-113">この機能は、ISV 競合他社のコピー防止 (ソースベースの保護) を有効にしません。</span><span class="sxs-lookup"><span data-stu-id="f31da-113">This feature doesn't enable ISV competitor copycat protection (that is, source-based protection).</span></span>

## <a name="capabilities"></a><span data-ttu-id="f31da-114">処理能力</span><span class="sxs-lookup"><span data-stu-id="f31da-114">Capabilities</span></span>
<span data-ttu-id="f31da-115">このセクションでは、ISV ライセンス機能のさまざまな機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="f31da-115">This section describes various capabilities of the ISV licensing feature.</span></span>

### <a name="isvs-can-generate-their-own-licenses"></a><span data-ttu-id="f31da-116">ISV は独自のライセンスを生成可能</span><span class="sxs-lookup"><span data-stu-id="f31da-116">ISVs can generate their own licenses</span></span>

<span data-ttu-id="f31da-117">ISV は独自のライセンスを個別に生成し、ソリューションに適用し、これらのソリューションをパートナーおよび顧客に提供できます。</span><span class="sxs-lookup"><span data-stu-id="f31da-117">ISVs can independently generate their own licenses, apply them to solutions, and deliver those solutions to partners and customers.</span></span> <span data-ttu-id="f31da-118">各 ISV ライセンスでは、ISV ソリューションを保護するためのランタイム機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="f31da-118">Each ISV license enables run-time features that help protect the ISV solution.</span></span> <span data-ttu-id="f31da-119">また、各 ISV ライセンスは、ソフトウェアが ISV によって配布されていることを保証する ISV Authenticode 証明書に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f31da-119">Additionally, each ISV license is tied to an ISV Authenticode certificate, which guarantees that the software was distributed by the ISV.</span></span>

### <a name="a-run-time-check-makes-sure-that-an-isv-generated-license-key-exists-in-the-customers-environment"></a><span data-ttu-id="f31da-120">ランタイム チェックにより、ISV によって生成されたライセンス キーが顧客の環境に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="f31da-120">A run-time check makes sure that an ISV-generated license key exists in the customer's environment</span></span>

<span data-ttu-id="f31da-121">ライセンスに関連付けられた各 ISV ソリューションは、有効なライセンス キーが顧客の環境に存在する場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="f31da-121">Each ISV solution that is tied to a license runs only when a valid license key exists in the customer's environment.</span></span> <span data-ttu-id="f31da-122">したがって、ISV がソリューションをライセンスに結び付けても、顧客に有効なライセンス キーがない場合、ソリューションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="f31da-122">Therefore, if an ISV ties its solution to a license, but the customer doesn't have a valid license key, the solution doesn't run.</span></span>

### <a name="there-are-two-types-of-license-boolean-and-number"></a><span data-ttu-id="f31da-123">ライセンスには、ブール値と数値の 2 種類があります</span><span class="sxs-lookup"><span data-stu-id="f31da-123">There are two types of license: Boolean and Number</span></span>

<span data-ttu-id="f31da-124">ISV は**ブール値**および**番号**の 2 つのタイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f31da-124">ISVs can create two types of license: **Boolean** and **Number**.</span></span> <span data-ttu-id="f31da-125">ISV は、いずれかの種類のライセンスと有効期限を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-125">ISVs can associate an expiration date with either type of license.</span></span> <span data-ttu-id="f31da-126">この有効期限は ISV ライセンスにのみ適用され、システムの有効期限とは無関係です。</span><span class="sxs-lookup"><span data-stu-id="f31da-126">This expiration date is applied only to the ISV licenses and is independent of the system expiration date.</span></span> <span data-ttu-id="f31da-127">ブール値ライセンスは、単純な有効化ライセンスです。</span><span class="sxs-lookup"><span data-stu-id="f31da-127">A Boolean license is a simple activation license.</span></span> <span data-ttu-id="f31da-128">ライセンスのタイプ (**ブール値** または**数字**) は、ライセンス コード ノードのプロパティによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="f31da-128">The type of license (**Boolean** or **Number**) is set through a property in the license code node.</span></span> <span data-ttu-id="f31da-129">ISV は、独自のカスタム ロジックを記述し、ISV ライセンスで提供されている数を確認し、そのソリューションがライセンス条件内で使用されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f31da-129">ISVs can write their own custom logic to check the count that is provided in the ISV license, to make sure that their solutions are being used within the license terms.</span></span> <span data-ttu-id="f31da-130">詳細については、[ISV のライセンス フレームワーク](https://msdn.microsoft.com/library/jj677284.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f31da-130">For more information, see [Licensing Framework for ISVs](https://msdn.microsoft.com/library/jj677284.aspx).</span></span>

### <a name="license-validation-errors"></a><span data-ttu-id="f31da-131">ライセンス検証エラー</span><span class="sxs-lookup"><span data-stu-id="f31da-131">License validation errors</span></span>

<span data-ttu-id="f31da-132">ISV ライセンスがインポート後に無効になったとき、ISV ソリューションはサーバーが再起動されるまで実行を継続します。</span><span class="sxs-lookup"><span data-stu-id="f31da-132">When an ISV license becomes invalid after import, the ISV solution continues to run until the server is restarted.</span></span> <span data-ttu-id="f31da-133">(サーバーの再起動後、ソリューションは無効になっています。) Application Object Server (AOS) のインスタンスの起動時にエラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="f31da-133">(After the server is restarted, the solution is disabled.) An error is thrown when the instance of the Application Object Server (AOS) starts.</span></span> <span data-ttu-id="f31da-134">エラーはイベント ログに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="f31da-134">The error is written to the event log.</span></span>

## <a name="implementing-isv-licensing-in-a-solution"></a><span data-ttu-id="f31da-135">ソリューションへの ISV ライセンスの実装</span><span class="sxs-lookup"><span data-stu-id="f31da-135">Implementing ISV licensing in a solution</span></span>
<span data-ttu-id="f31da-136">ISV には証明機関 (CA) から有効な Authenticode 証明書 (X.509) が必要です。</span><span class="sxs-lookup"><span data-stu-id="f31da-136">ISVs must have a valid Authenticode certificate (X.509) from a certificate authority (CA).</span></span> <span data-ttu-id="f31da-137">Microsoft が、特定の CA をお勧めすることはありません。</span><span class="sxs-lookup"><span data-stu-id="f31da-137">Microsoft doesn't recommend any particular CA.</span></span> <span data-ttu-id="f31da-138">ただし、多くの企業がこれらの証明書を提供します。</span><span class="sxs-lookup"><span data-stu-id="f31da-138">However, many companies offer these certificates.</span></span> <span data-ttu-id="f31da-139">Authenticode 証明書は、さまざまなキー サイズに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f31da-139">Authenticode certificates come in various key sizes.</span></span> <span data-ttu-id="f31da-140">ISV ライセンス機能は、キー サイズが 1024 ビットと 2048 ビットの両方の証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f31da-140">The ISV licensing feature supports certificates of both 1024-bit and 2048-bit key sizes.</span></span> <span data-ttu-id="f31da-141">既定では、多くのプロバイダーが 2048 ビット キー サイズを使用しており、より強固な暗号化を提供するために ISV はこのビット キー サイズを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f31da-141">By default, many providers use the 2048-bit key size, and we recommend that ISVs use this bit key size, because it provides stronger encryption.</span></span> <span data-ttu-id="f31da-142">ただし、ISV に既に既存の 1024 ビット キー サイズがある場合、そのキー サイズは ISV ライセンス機能で動作します。</span><span class="sxs-lookup"><span data-stu-id="f31da-142">However, if an ISV already has an existing 1024-bit key size, that key size works with the ISV licensing feature.</span></span> <span data-ttu-id="f31da-143">**注記:** ISV ライセンス機能は、4096 ビット キー サイズをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f31da-143">**Note:** The ISV licensing feature doesn't support 4096-bit key sizes.</span></span> <span data-ttu-id="f31da-144">Authenticode 証明書はさまざまな暗号サービス プロバイダーを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-144">Authenticode certificates can have various cryptographic service providers.</span></span> <span data-ttu-id="f31da-145">ISV ライセンス機能は、Enhanced Cryptographic Provider を使います (Base Cryptographic Provider もカバーします)。</span><span class="sxs-lookup"><span data-stu-id="f31da-145">The ISV licensing feature uses Enhanced Cryptographic Provider (which also covers Base Cryptographic Provider).</span></span> <span data-ttu-id="f31da-146">Authenticode 証明書を購入できる多くの独立したプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="f31da-146">There are many independent providers that you can purchase an Authenticode certificate from.</span></span> <span data-ttu-id="f31da-147">Microsoft が、特定のプロバイダーをお勧めすることはありません。</span><span class="sxs-lookup"><span data-stu-id="f31da-147">Microsoft doesn't recommend any particular provider.</span></span> <span data-ttu-id="f31da-148">頻繁に使用されるプロバイダーには、Symantec VeriSign、Thawte、Go Daddy があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-148">Some providers that are often used are Symantec VeriSign, Thawte, and Go Daddy.</span></span>

## <a name="certificate-import-and-export"></a><span data-ttu-id="f31da-149">証明書のインポートおよびエクスポート</span><span class="sxs-lookup"><span data-stu-id="f31da-149">Certificate import and export</span></span>
<span data-ttu-id="f31da-150">証明書は、お客様のライセンス ファイルに署名し、インポート時にライセンス ファイルを検証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f31da-150">The certificate is used to sign your customer license files and validate the license files at the time of import.</span></span> <span data-ttu-id="f31da-151">Authenticode 証明書は、4 つのファイル形式をサポートします。</span><span class="sxs-lookup"><span data-stu-id="f31da-151">Authenticode certificates support four file formats.</span></span> <span data-ttu-id="f31da-152">ISV ライセンス機能については、2 つの形式で証明書ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="f31da-152">For the ISV licensing feature, you must have the certificate files in two formats:</span></span>

-   <span data-ttu-id="f31da-153">**個人情報交換 (pfx または PKCS \#12 とも呼ばれる)** – .pfx ファイル名拡張子を使用して、証明書、秘密キー、および証明書パスのすべての証明書のセキュリティ保護された保管をサポートする PKCS \#12 形式。</span><span class="sxs-lookup"><span data-stu-id="f31da-153">**Personal Information Exchange (PFX, also known as PKCS \#12)** – The PKCS \#12 format, which uses the .pfx file name extension, supports secure storage of certificates, private keys, and all certificates in a certification path.</span></span> <span data-ttu-id="f31da-154">PKCS \#12 形式は、証明書とそのプライベート キーをエクスポートするために使用される唯一のファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="f31da-154">The PKCS \#12 format is the only file format that can be used to export a certificate and its private key.</span></span>
-   <span data-ttu-id="f31da-155">**Base64 エンコード X.509** - Base64 形式では、単一の証明書の格納がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f31da-155">**Base64-encoded X.509** – The Base64 format supports storage of a single certificate.</span></span> <span data-ttu-id="f31da-156">この形式では、秘密キーまたは証明書パスの格納はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f31da-156">This format doesn't support storage of the private key or certification path.</span></span>

<span data-ttu-id="f31da-157">形式に制限があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-157">There is a restriction on the format.</span></span> <span data-ttu-id="f31da-158">PFX (PKCS \#12) 形式は、署名/生成目的でプライベート キーと共に証明書をエクスポートする場合にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-158">The PFX (PKCS \#12) format should be used only to export the certificate together with its private key for signing/generating purposes.</span></span> <span data-ttu-id="f31da-159">絶対に ISV 組織外に共有しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-159">It should never be shared outside the ISV organization.</span></span> <span data-ttu-id="f31da-160">.cer ファイル名拡張子を使用する DER でエンコードされたバイナリ X.509形式は、アプリケーション オブジェクト ツリー (AOT) ライセンスに埋め込まれる必要がある証明書の公開キーをエクスポートするために使用してください。</span><span class="sxs-lookup"><span data-stu-id="f31da-160">The DER-encoded binary X.509 format, which uses the .cer file name extension, should be used to export the public key of the certificate that must be embedded in the Application Object Tree (AOT) License.</span></span> <span data-ttu-id="f31da-161">この公開キーは、モデルを介して顧客に配布されます。</span><span class="sxs-lookup"><span data-stu-id="f31da-161">This public key is distributed to customers via the model.</span></span> <span data-ttu-id="f31da-162">これは、ライセンスが秘密キーを所有する ISV ライセンスによって署名されていることを確認するために、ライセンスのインポート時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f31da-162">It's used when a license is imported, to make sure that the license is signed by the ISV license that owns the private key.</span></span>

## <a name="enable-licensing-for-your-isv-solution"></a><span data-ttu-id="f31da-163">ISV ソリューションのライセンスの有効化</span><span class="sxs-lookup"><span data-stu-id="f31da-163">Enable licensing for your ISV solution</span></span>
<span data-ttu-id="f31da-164">ソリューションのライセンスを有効にするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f31da-164">Follow these steps to enable licensing for your solution.</span></span>

1.  <span data-ttu-id="f31da-165">ISV ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="f31da-165">Create an ISV solution.</span></span> 

    ![ISV ソリューションを作成しています](./media/isv1.png)

2.  <span data-ttu-id="f31da-167">リソースとしてプロジェクトに証明書の公開キー (.cer ファイル) を追加します。</span><span class="sxs-lookup"><span data-stu-id="f31da-167">Add the certificate's public key (.cer file) to your project as a resource.</span></span>
    1.  <span data-ttu-id="f31da-168">新しい品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f31da-168">Add a new item.</span></span> 

        ![新しい品目の追加](./media/isv2.png)

    2.  <span data-ttu-id="f31da-170">**ラベルおよびリソース**をクリックし、次に**リソース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f31da-170">Click **Labels And Resources**, and then click **Resource**.</span></span> 

        ![リソースをクリックする](./media/isv3.png)

    3.  <span data-ttu-id="f31da-172">リソースとして証明書の公開キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="f31da-172">Select the certificate's public key as the resource.</span></span> 

        ![リソースとして証明書の公開キーを選択](./media/isv4.png)

    4.  <span data-ttu-id="f31da-174">リソースとして、証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="f31da-174">Add the certificate as a resource.</span></span> 

        ![リソースとして証明書を追加](./media/isv5.png)


3.  <span data-ttu-id="f31da-176">ライセンス コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="f31da-176">Create a license code.</span></span> 

    ![ライセンス コードを作成しています](./media/isv6.png)

4.  <span data-ttu-id="f31da-178">ライセンス コードに証明書をマップします。</span><span class="sxs-lookup"><span data-stu-id="f31da-178">Map the certificate to the license code.</span></span> 

    ![ライセンス コードへの証明書のマッピング](./media/isv7.png)

5.  <span data-ttu-id="f31da-180">1 つまたは複数のコンフィギュレーション キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f31da-180">Create one or more configuration keys.</span></span> 

    ![コンフィギュレーション キーを作成しています](./media/isv8.png)

6.  <span data-ttu-id="f31da-182">ライセンス コードをコンフィギュレーション キーに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f31da-182">Associate the license code with the configuration keys.</span></span> 

    <span data-ttu-id="f31da-183">[</span><span class="sxs-lookup"><span data-stu-id="f31da-183">[</span></span>![ライセンス コードとコンフィギュレーション キーの関連付け](./media/isv9.png)

7.  <span data-ttu-id="f31da-185">コンフィギュレーション キーをソリューションの要素に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f31da-185">Associate a configuration key to an element in your solution.</span></span> <span data-ttu-id="f31da-186">たとえば、新しいフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="f31da-186">For example, create a new form.</span></span> 

    ![新しいフォームを作成しています](./media/isv10.png)

8.  <span data-ttu-id="f31da-188">フォームにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="f31da-188">Add a button to the form.</span></span> 

    ![新しいフォームへのボタンの追加](./media/isv11.png)

    <span data-ttu-id="f31da-190">このボタンは、最初はコンフィギュレーション キーで制御されていないため、表示されます。</span><span class="sxs-lookup"><span data-stu-id="f31da-190">The button will be visible, because it isn't controlled by a configuration key at first.</span></span> 

    ![最初に追加されるときに、新しいボタンが表示されます](./media/isv12.png)

9.  <span data-ttu-id="f31da-192">コンフィギュレーション キーをボタンに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f31da-192">Associate a configuration key with the button.</span></span> 

    ![コンフィギュレーション キーとボタンの関連付け](./media/isv13.png) 

    <span data-ttu-id="f31da-194">コンフィギュレーション キーが有効になり、利用可能になると、ボタンは表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="f31da-194">The button will no longer be visible, because the configuration key must be available and enabled.</span></span> 

    ![ボタンが表示されていません](./media/isv14.png)


## <a name="create-a-package-and-generate-a-customer-specific-license"></a><span data-ttu-id="f31da-196">パッケージを作成し、顧客固有のライセンスを生成する</span><span class="sxs-lookup"><span data-stu-id="f31da-196">Create a package and generate a customer-specific license</span></span>
1.  <span data-ttu-id="f31da-197">ライセンスを発行する顧客のテナント名と ID を収集します。</span><span class="sxs-lookup"><span data-stu-id="f31da-197">Collect the tenant name and ID for the customer to issue the license to.</span></span> <span data-ttu-id="f31da-198">(この情報は、**設定**&gt;**情報**で見つけることができます。)</span><span class="sxs-lookup"><span data-stu-id="f31da-198">(You can find this information at **Settings** &gt; **About**.)</span></span> 

    ![顧客のテナント名および ID](./media/isv15.png)

2.  <span data-ttu-id="f31da-200">顧客のライセンス (テナント ID と名前) を生成し、証明書のプライベート キーを使用してライセンスを登録します。</span><span class="sxs-lookup"><span data-stu-id="f31da-200">Generate a license for the customer (tenant ID and name), and sign the license by using the certificate's private key.</span></span> <span data-ttu-id="f31da-201">ライセンス ファイルを作成するには、**axutil genlicense** コマンドに、以下のパラメーターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-201">You must pass the following parameters to the **axutil genlicense** command to create the license file.</span></span>

    | <span data-ttu-id="f31da-202">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f31da-202">Parameter name</span></span>  | <span data-ttu-id="f31da-203">説明</span><span class="sxs-lookup"><span data-stu-id="f31da-203">Description</span></span>                                                                  |
    |-----------------|------------------------------------------------------------------------------|
    | <span data-ttu-id="f31da-204">ファイル</span><span class="sxs-lookup"><span data-stu-id="f31da-204">file</span></span>            | <span data-ttu-id="f31da-205">ライセンス ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="f31da-205">The name of your license file.</span></span>                                               |
    | <span data-ttu-id="f31da-206">licensecode</span><span class="sxs-lookup"><span data-stu-id="f31da-206">licensecode</span></span>     | <span data-ttu-id="f31da-207">Microsoft Visual Studio のライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="f31da-207">The name of your license code (from Microsoft Visual Studio).</span></span>                |
    | <span data-ttu-id="f31da-208">certificatepath</span><span class="sxs-lookup"><span data-stu-id="f31da-208">certificatepath</span></span> | <span data-ttu-id="f31da-209">証明書のプライベート キーのパス。</span><span class="sxs-lookup"><span data-stu-id="f31da-209">The path of your certificate's private key.</span></span>                                  |
    | <span data-ttu-id="f31da-210">パスワード</span><span class="sxs-lookup"><span data-stu-id="f31da-210">password</span></span>        | <span data-ttu-id="f31da-211">証明書のプライベート キーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="f31da-211">The password for your certificate's private key.</span></span>                             |
    | <span data-ttu-id="f31da-212">顧客</span><span class="sxs-lookup"><span data-stu-id="f31da-212">customer</span></span>        | <span data-ttu-id="f31da-213">(手順 1 のスクリーン ショットから) 顧客のテナント名。</span><span class="sxs-lookup"><span data-stu-id="f31da-213">The customer's tenant name (from the screen shot under step 1).</span></span>              |
    | <span data-ttu-id="f31da-214">serialnumber</span><span class="sxs-lookup"><span data-stu-id="f31da-214">serialnumber</span></span>    | <span data-ttu-id="f31da-215">顧客のテナント ID (スクリーン ショットに「シリアル番号」と表示されています)。</span><span class="sxs-lookup"><span data-stu-id="f31da-215">The customer's tenant ID (labeled "Serial number" in the screen shot).</span></span>       |
    | <span data-ttu-id="f31da-216">expirationdate</span><span class="sxs-lookup"><span data-stu-id="f31da-216">expirationdate</span></span>  | <span data-ttu-id="f31da-217">オプション: ライセンスの有効期限。</span><span class="sxs-lookup"><span data-stu-id="f31da-217">Optional: The expiration date for the license.</span></span>                               |
    | <span data-ttu-id="f31da-218">usercount</span><span class="sxs-lookup"><span data-stu-id="f31da-218">usercount</span></span>       | <span data-ttu-id="f31da-219">オプション: カスタム検証ロジックが必要に応じて使用できる数値。</span><span class="sxs-lookup"><span data-stu-id="f31da-219">Optional: The number that custom validation logic can use as required.</span></span> <span data-ttu-id="f31da-220">これはユーザーになる可能性がありますが、必ずしもユーザーに限定されません。</span><span class="sxs-lookup"><span data-stu-id="f31da-220">This could be users, but is not limited to users.</span></span> |

    <span data-ttu-id="f31da-221">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f31da-221">Here is an example.</span></span>

        C:\AOSService\PackagesLocalDirectory\Bin\axutil genlicense /file:c:\templicense.txt /certificatepath:c:\tempisvcert.pfx /licensecode:ISVLicenseCode /customer:TAEOfficial.ccsctp.net /serialnumber:4dbfcf74-c5a6-4727-b638-d56e51d1f381 /password:********



3.  <span data-ttu-id="f31da-222">ライセンスをターゲット環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="f31da-222">Import the license into the target environment.</span></span> <span data-ttu-id="f31da-223">**注記:** 実稼動システムでは、配置可能パッケージを使用して、Microsoft Dynamics Lifecycle Services (LCS) からこの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="f31da-223">**Note:** In production systems, you complete this step from Microsoft Dynamics Lifecycle Services (LCS), by using a deployable package.</span></span> <span data-ttu-id="f31da-224">詳細については、この記事の後半の「実稼働環境」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f31da-224">For more information, see the "Production environments" section later in this article.</span></span>

    | <span data-ttu-id="f31da-225">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="f31da-225">Parameter name</span></span>                | <span data-ttu-id="f31da-226">説明</span><span class="sxs-lookup"><span data-stu-id="f31da-226">Description</span></span>                                                                                            |
    |-------------------------------|--------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f31da-227">--setupmode importlicensefile</span><span class="sxs-lookup"><span data-stu-id="f31da-227">--setupmode importlicensefile</span></span> | <span data-ttu-id="f31da-228">ライセンスが読み込まれることをセットアップ ツールに通知するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-228">Use this parameter to inform the setup tool that a license will be loaded.</span></span>                             |
    | <span data-ttu-id="f31da-229">--metadatadir</span><span class="sxs-lookup"><span data-stu-id="f31da-229">--metadatadir</span></span>                 | <span data-ttu-id="f31da-230">メタデータ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-230">Use this parameter to specify the metadata directory.</span></span> <span data-ttu-id="f31da-231">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-231">You should use the default packages directory.</span></span>   |
    | <span data-ttu-id="f31da-232">--bindir</span><span class="sxs-lookup"><span data-stu-id="f31da-232">--bindir</span></span>                      | <span data-ttu-id="f31da-233">バイナリ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-233">Use this parameter to specify the binaries directory.</span></span> <span data-ttu-id="f31da-234">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-234">You should use the default packages directory.</span></span>   |
    | <span data-ttu-id="f31da-235">--sqlserver</span><span class="sxs-lookup"><span data-stu-id="f31da-235">--sqlserver</span></span>                   | <span data-ttu-id="f31da-236">このパラメーターを使用して Microsoft SQL Server を指定します。</span><span class="sxs-lookup"><span data-stu-id="f31da-236">Use this parameter to specify the Microsoft SQL Server.</span></span> <span data-ttu-id="f31da-237">1 ボックス環境では、ピリオド (**.**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-237">For one-box environment, use a period (**.**).</span></span> |
    | <span data-ttu-id="f31da-238">--sqluser</span><span class="sxs-lookup"><span data-stu-id="f31da-238">--sqluser</span></span>                     | <span data-ttu-id="f31da-239">SQL Server のユーザーを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-239">Use this parameter to specify the SQL Server user.</span></span> <span data-ttu-id="f31da-240">**AOSUser** に渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-240">You should pass in **AOSUser**.</span></span>                     |
    | <span data-ttu-id="f31da-241">--sqlpwd</span><span class="sxs-lookup"><span data-stu-id="f31da-241">--sqlpwd</span></span>                      | <span data-ttu-id="f31da-242">SQL Server のパスワードを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-242">Use this parameter to specify the SQL Server password.</span></span>                                                 |
    | <span data-ttu-id="f31da-243">--licensefilename</span><span class="sxs-lookup"><span data-stu-id="f31da-243">--licensefilename</span></span>             | <span data-ttu-id="f31da-244">読み込むライセンス ファイルを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="f31da-244">Use this parameter to specify the license file that will be loaded.</span></span>                                    |

    <span data-ttu-id="f31da-245">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="f31da-245">Here is an example.</span></span>

        C:\AOSService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --setupmode importlicensefile --metadatadir c:\packages --bindir c:\packages --sqlserver . --sqldatabase axdbrain --sqluser AOSUser --sqlpwd ******** --licensefilename c:\templicense.txt

4.  <span data-ttu-id="f31da-246">対応するコンフィギュレーション キーは、**ライセンス コンフィギュレーション** ページで使用可能になり、有効になります。</span><span class="sxs-lookup"><span data-stu-id="f31da-246">The corresponding configuration key will be available and enabled on the **License configuration** page.</span></span> <span data-ttu-id="f31da-247">既定では、コンフィギュレーションが有効です。</span><span class="sxs-lookup"><span data-stu-id="f31da-247">By default, the configuration is enabled.</span></span> <span data-ttu-id="f31da-248">たとえば、次のスクリーン ショットで **ISVConfigurationKey1** コンフィギュレーション キーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f31da-248">For example, see the **ISVConfigurationKey1** configuration key in the following screen shot.</span></span> 

    ![ライセンス設定ページで ISVConfigurationKey1 コンフィギュレーション キーを有効にする](./media/isv18.png)

5.  <span data-ttu-id="f31da-250">非実稼働インストールでは、Visual Studio からデータベースの同期プロセスを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-250">In non-production installations, you must start the database synchronization process from Visual Studio.</span></span>

<span data-ttu-id="f31da-251">コンフィギュレーション キーを有効にした後、次のスクリーン ショットに示すように、ボタンは表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="f31da-251">After the configuration key is enabled, the button become visible, as shown in the following screen shot.</span></span> 

![コンフィギュレーション キーを有効にするとボタンが表示されます](./media/isv19.png)

## <a name="protection-best-practices"></a><span data-ttu-id="f31da-253">保護のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="f31da-253">Protection best practices</span></span>
<span data-ttu-id="f31da-254">ソリューションは、2つの形式で配布することができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-254">Solutions can be delivered in two forms:</span></span>

-   <span data-ttu-id="f31da-255">モデル ファイル (ソース コード)</span><span class="sxs-lookup"><span data-stu-id="f31da-255">Model files (source code)</span></span>
-   <span data-ttu-id="f31da-256">配置可能パッケージ (binary)</span><span class="sxs-lookup"><span data-stu-id="f31da-256">Deployable packages (binary)</span></span>

<span data-ttu-id="f31da-257">構成キーとライセンス コードを保護するには、展開可能なパッケージを使用してバイナリ形式でリリースすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f31da-257">To protect your configuration keys and license codes, we recommend that you release them in binary form, by using a deployable package.</span></span> <span data-ttu-id="f31da-258">顧客は Visual Studio のこれらの要素をインストールして対話することができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-258">Customers will then be able to install and interact with those elements in Visual Studio.</span></span> <span data-ttu-id="f31da-259">顧客が配置可能パッケージ内の項目を参照することはできますが、ソース コードにアクセスしたり項目を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="f31da-259">Although customers will be able to refer to items in the deployable package, they won't be able to access source code or make modifications to the items.</span></span> <span data-ttu-id="f31da-260">(ただし、拡張機能を作成できます。) バイナリ形式でソリューションをリリースする機能の詳細は、すぐに利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f31da-260">(However, they can create extensions.) More details about the capability to release solutions in binary form will be available soon.</span></span> <span data-ttu-id="f31da-261">配置可能パッケージ (バイナリ) には、顧客がアクセスを必要とせず、カスタマイズできないようなクラスやその他のロジックも含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-261">The deployable package (binary) can also include classes and other logic that your customer doesn't require access to and should not be able to customize.</span></span> 

![保護されている ISV ソリューションと保護されていない ISV ソリューション](./media/isv20.png)

## <a name="production-environments"></a><span data-ttu-id="f31da-263">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="f31da-263">Production environments</span></span>
<span data-ttu-id="f31da-264">実稼働システムに ISV ライセンスをインストールするには、LCS によって展開可能なパッケージを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-264">To install ISV licenses in production systems, you must use a deployable package through LCS.</span></span> <span data-ttu-id="f31da-265">構成モード用テンプレート パッケージは、すべてのインストールの &lt;PackagesFolder&gt;\\bin\\CustomDeployablePackage\\ImportISVLicense.zip (パッケージ フォルダーは通常 j:\\AOSService\\PackagesLocalDirectory または c:\\AOSService\\PackagesLocalDirectory\\ の下にあります) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-265">You can find a template package for configuration mode at the following location in all installations: &lt;PackagesFolder&gt;\\bin\\CustomDeployablePackage\\ImportISVLicense.zip (Packages folder is typically under j:\\AOSService\\PackagesLocalDirectory or c:\\AOSService\\PackagesLocalDirectory\\)</span></span> 

![コンフィギュレーション モードのテンプレート パッケージの場所](./media/isv21.png)

1.  <span data-ttu-id="f31da-267">パッケージ テンプレートのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="f31da-267">Make a copy of the package template.</span></span>
2.  <span data-ttu-id="f31da-268">パッケージ テンプレート内の次のフォルダーにライセンス ファイルを配置: ImportISVLicense.zipAosServiceScriptsLicense</span><span class="sxs-lookup"><span data-stu-id="f31da-268">Put the license file in the following folder within the package template: ImportISVLicense.zipAosServiceScriptsLicense</span></span>

<span data-ttu-id="f31da-269">一度に複数のライセンスをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-269">More than one license can be installed at a time.</span></span> <span data-ttu-id="f31da-270">別のライセンスがいずれかに依存する場合は、それに応じた名前を確認します。</span><span class="sxs-lookup"><span data-stu-id="f31da-270">If one of the licenses depends on another, make sure that it's named accordingly.</span></span> <span data-ttu-id="f31da-271">(ライセンスはアルファベット順にインストールされます。)</span><span class="sxs-lookup"><span data-stu-id="f31da-271">(Licenses are installed in alphabetical order.)</span></span>

## <a name="appendix-create-self-signed-certificates-for-test-purposes"></a><span data-ttu-id="f31da-272">付録: テスト目的での自己署名証明書の作成</span><span class="sxs-lookup"><span data-stu-id="f31da-272">Appendix: Create self-signed certificates for test purposes</span></span>
<span data-ttu-id="f31da-273">**注記:** 自己署名証明書は、開発時にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="f31da-273">**Note:** Self-signed certificates can be used only during development.</span></span> <span data-ttu-id="f31da-274">これらは、実稼働環境でサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f31da-274">They aren't supported in production environments.</span></span>

1.  <span data-ttu-id="f31da-275">テストの目的で、 自己署名の CA 証明書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f31da-275">For test purposes, create a self-signed CA certificate.</span></span> <span data-ttu-id="f31da-276">Visual Studio のツール プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="f31da-276">Use the Visual Studio tools prompt to run the following command.</span></span>

        makecert -r -pe -n "CN=IsvCertTestAuthority O=IsvCertTestAuthority" -ss CA -sr LocalMachine -a sha256 -len 2048 -cy authority -sky signature -b 01/01/2016 -sv c:\temp\CA.pvk c:\temp\CA.cer

    <span data-ttu-id="f31da-277">詳細については、[MakeCert](https://msdn.microsoft.com/library/windows/desktop/aa386968(v=vs.85).aspx) のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f31da-277">For more information, see the [MakeCert](https://msdn.microsoft.com/library/windows/desktop/aa386968(v=vs.85).aspx) documentation.</span></span>

2.  <span data-ttu-id="f31da-278">CA を使用して証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="f31da-278">Create a certificate by using the CA.</span></span>

        makecert -pe -n "CN=IsvCertTest O=IsvCertTest" -ss ISVStore -sr LocalMachine -a sha256 -len 2048 -cy end -sky signature -eku 1.3.6.1.5.5.7.3.3 -ic c:\temp\ca.cer -iv c:\temp\ca.pvk -b **/**/**** -sv c:\temp\isvcert.pvk c:\temp\isvcert.cer

3.  <span data-ttu-id="f31da-279">ISV 証明書を PFX 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="f31da-279">Convert the ISV certificate to PFX format.</span></span>

        pvk2pfx -pvk c:\temp\isvcert.pvk -spc c:\temp\isvcert.cer -pfx c:\temp\isvcert.pfx -po ********

4.  <span data-ttu-id="f31da-280">テスト シナリオでは、すべての AOS インスタンスに手動で自己署名 CA 証明書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="f31da-280">For a test scenario, import the self-signed CA certificate manually on all the AOS instances.</span></span>

        certutil -addstore root c:\temp\ca.cer

    <span data-ttu-id="f31da-281">ただし、自己署名 ISV 証明書を使用していた場合、CA 証明書ではなくその証明書をインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f31da-281">However, if a self-signed ISV certificate was used, that certificate must be imported instead of the CA certificate.</span></span>

        certutil -addstore root c:\temp\isvcert.cer






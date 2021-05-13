---
title: 独立系ソフトウェア ベンダー (ISV) ライセンス
description: このトピックでは、独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。
author: jorisdg
ms.date: 05/08/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 604d7f813b46c493560570a78030dbf8d5485f63
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923285"
---
# <a name="independent-software-vendor-isv-licensing"></a><span data-ttu-id="47c89-103">独立系ソフトウェア ベンダー (ISV) ライセンス</span><span class="sxs-lookup"><span data-stu-id="47c89-103">Independent software vendor (ISV) licensing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47c89-104">このトピックでは、独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="47c89-104">This topic describes the independent software vendor (ISV) licensing feature.</span></span> <span data-ttu-id="47c89-105">これには、ISV のライセンス機能の長所および機能に関する情報が含まれており、ISV ソリューションのライセンスを有効にする方法、パッケージの作成方法、顧客固有のライセンスの生成方法およびテスト目的で自己署名証明書を作成する方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="47c89-105">It includes information about benefits and capabilities of the ISV licensing feature, and explains how to enable licensing for an ISV solution, create a package and generate a customer-specific license, and create self-signed certificates for test purposes.</span></span>

<span data-ttu-id="47c89-106">Microsoft Dynamics エコシステムには、独立系ソフトウェア ベンダー (ISV) が再パッケージ化可能な業種ソリューションをビルド、配置、販売して収益化できるようにするツールとフレームワークが用意されています。</span><span class="sxs-lookup"><span data-stu-id="47c89-106">The Microsoft Dynamics ecosystem provides tools and frameworks that let independent software vendors (ISVs) build, deploy, sell, and therefore monetize vertical industry solutions that can be repackaged.</span></span> <span data-ttu-id="47c89-107">ISV ライセンス機能には、次の利点があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-107">The ISV licensing feature provides the following benefits:</span></span>

-   <span data-ttu-id="47c89-108">これは、顧客およびパートナーに ISV ソリューションのより安全なライセンス メカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="47c89-108">It provides a safer licensing mechanism for ISV solutions for customers and partners.</span></span> <span data-ttu-id="47c89-109">ISV ソリューションは、顧客が ISV から有効なライセンス キーを購入した場合にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="47c89-109">ISV solutions are enabled only if the customer has purchased a valid license key from the ISV.</span></span>
-   <span data-ttu-id="47c89-110">これにより、顧客が異なる ISV からの ISV ソリューションのライセンスをどのように処理するかが調整されるため、総保有コスト (TCO) を削減します。</span><span class="sxs-lookup"><span data-stu-id="47c89-110">It aligns how customers handle licenses for ISV solutions from different ISVs, and therefore lowers the total cost of ownership (TCO).</span></span>
-   <span data-ttu-id="47c89-111">ISV は、業界標準のフレームワークを使用して、ISV ライセンスを個別に生成、管理、配布することができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-111">ISVs can independently generate, manage, and distribute ISV licenses by using industry standard frameworks.</span></span>

<span data-ttu-id="47c89-112">この機能は、ISV 競合他社のコピー防止 (ソースベースの保護) を有効にしません。</span><span class="sxs-lookup"><span data-stu-id="47c89-112">This feature doesn't enable ISV competitor copycat protection (that is, source-based protection).</span></span>

## <a name="capabilities"></a><span data-ttu-id="47c89-113">処理能力</span><span class="sxs-lookup"><span data-stu-id="47c89-113">Capabilities</span></span>
<span data-ttu-id="47c89-114">このセクションでは、ISV ライセンス機能のさまざまな機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="47c89-114">This section describes various capabilities of the ISV licensing feature.</span></span>

### <a name="isvs-can-generate-their-own-licenses"></a><span data-ttu-id="47c89-115">ISV は独自のライセンスを生成可能</span><span class="sxs-lookup"><span data-stu-id="47c89-115">ISVs can generate their own licenses</span></span>

<span data-ttu-id="47c89-116">ISV は独自のライセンスを個別に生成し、ソリューションに適用し、これらのソリューションをパートナーおよび顧客に提供できます。</span><span class="sxs-lookup"><span data-stu-id="47c89-116">ISVs can independently generate their own licenses, apply them to solutions, and deliver those solutions to partners and customers.</span></span> <span data-ttu-id="47c89-117">各 ISV ライセンスでは、ISV ソリューションを保護するためのランタイム機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="47c89-117">Each ISV license enables run-time features that help protect the ISV solution.</span></span> <span data-ttu-id="47c89-118">また、各 ISV ライセンスは、ソフトウェアが ISV によって配布されるようにする ISV Authenticode 証明書に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="47c89-118">Additionally, each ISV license is tied to an ISV Authenticode certificate, which ensures that the software was distributed by the ISV.</span></span>

### <a name="a-run-time-check-makes-sure-that-an-isv-generated-license-key-exists-in-the-customers-environment"></a><span data-ttu-id="47c89-119">ランタイム チェックにより、ISV によって生成されたライセンス キーが顧客の環境に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="47c89-119">A run-time check makes sure that an ISV-generated license key exists in the customer's environment</span></span>

<span data-ttu-id="47c89-120">ライセンスに関連付けられた各 ISV ソリューションは、有効なライセンス キーが顧客の環境に存在する場合にのみ実行されます。</span><span class="sxs-lookup"><span data-stu-id="47c89-120">Each ISV solution that is tied to a license runs only when a valid license key exists in the customer's environment.</span></span> <span data-ttu-id="47c89-121">したがって、ISV がソリューションをライセンスに結び付けても、顧客に有効なライセンス キーがない場合、ソリューションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="47c89-121">Therefore, if an ISV ties its solution to a license, but the customer doesn't have a valid license key, the solution doesn't run.</span></span>

### <a name="there-are-two-types-of-license-boolean-and-number"></a><span data-ttu-id="47c89-122">ライセンスには、ブール値と数値の 2 種類があります</span><span class="sxs-lookup"><span data-stu-id="47c89-122">There are two types of license: Boolean and Number</span></span>

<span data-ttu-id="47c89-123">ISV は **ブール値** および **番号** の 2 つのタイプを作成できます。</span><span class="sxs-lookup"><span data-stu-id="47c89-123">ISVs can create two types of license: **Boolean** and **Number**.</span></span> <span data-ttu-id="47c89-124">ISV は、いずれかの種類のライセンスと有効期限を関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-124">ISVs can associate an expiration date with either type of license.</span></span> <span data-ttu-id="47c89-125">この有効期限は ISV ライセンスにのみ適用され、システムの有効期限とは無関係です。</span><span class="sxs-lookup"><span data-stu-id="47c89-125">This expiration date is applied only to the ISV licenses and is independent of the system expiration date.</span></span> <span data-ttu-id="47c89-126">ブール値ライセンスは、単純な有効化ライセンスです。</span><span class="sxs-lookup"><span data-stu-id="47c89-126">A Boolean license is a simple activation license.</span></span> <span data-ttu-id="47c89-127">ライセンスのタイプ (**ブール値** または **数字**) は、ライセンス コード ノードのプロパティによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="47c89-127">The type of license (**Boolean** or **Number**) is set through a property in the license code node.</span></span> <span data-ttu-id="47c89-128">ISV は、独自のカスタム ロジックを記述し、ISV ライセンスで提供されている数を確認し、そのソリューションがライセンス条件内で使用されていることを確認できます。</span><span class="sxs-lookup"><span data-stu-id="47c89-128">ISVs can write their own custom logic to check the count that is provided in the ISV license, to make sure that their solutions are being used within the license terms.</span></span> <span data-ttu-id="47c89-129">詳細については、[ISV のライセンス フレームワーク](/dynamicsax-2012/developer/licensing-framework-for-isvs-of-microsoft-dynamics-ax)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c89-129">For more information, see [Licensing Framework for ISVs](/dynamicsax-2012/developer/licensing-framework-for-isvs-of-microsoft-dynamics-ax).</span></span>

### <a name="license-validation-errors"></a><span data-ttu-id="47c89-130">ライセンス検証エラー</span><span class="sxs-lookup"><span data-stu-id="47c89-130">License validation errors</span></span>

<span data-ttu-id="47c89-131">ISV ライセンスがインポート後に無効になったとき、ISV ソリューションはサーバーが再起動されるまで実行を継続します。</span><span class="sxs-lookup"><span data-stu-id="47c89-131">When an ISV license becomes invalid after import, the ISV solution continues to run until the server is restarted.</span></span> <span data-ttu-id="47c89-132">(サーバーの再起動後、ソリューションは無効になっています。) Application Object Server (AOS) のインスタンスの起動時にエラーがスローされます。</span><span class="sxs-lookup"><span data-stu-id="47c89-132">(After the server is restarted, the solution is disabled.) An error is thrown when the instance of the Application Object Server (AOS) starts.</span></span> <span data-ttu-id="47c89-133">エラーはイベント ログに書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="47c89-133">The error is written to the event log.</span></span>

## <a name="implementing-isv-licensing-in-a-solution"></a><span data-ttu-id="47c89-134">ソリューションへの ISV ライセンスの実装</span><span class="sxs-lookup"><span data-stu-id="47c89-134">Implementing ISV licensing in a solution</span></span>
<span data-ttu-id="47c89-135">ISV には証明機関 (CA) から有効な Authenticode 証明書 (X.509) が必要です。</span><span class="sxs-lookup"><span data-stu-id="47c89-135">ISVs must have a valid Authenticode certificate (X.509) from a certificate authority (CA).</span></span> <span data-ttu-id="47c89-136">Microsoft が、特定の CA をお勧めすることはありません。</span><span class="sxs-lookup"><span data-stu-id="47c89-136">Microsoft doesn't recommend any particular CA.</span></span> <span data-ttu-id="47c89-137">ただし、多くの企業がこれらの証明書を提供します。</span><span class="sxs-lookup"><span data-stu-id="47c89-137">However, many companies offer these certificates.</span></span> <span data-ttu-id="47c89-138">Authenticode 証明書は、さまざまなキー サイズに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="47c89-138">Authenticode certificates come in various key sizes.</span></span> <span data-ttu-id="47c89-139">ISV ライセンス機能は、キー サイズが 1024 ビットと 2048 ビットの両方の証明書をサポートします。</span><span class="sxs-lookup"><span data-stu-id="47c89-139">The ISV licensing feature supports certificates of both 1024-bit and 2048-bit key sizes.</span></span> <span data-ttu-id="47c89-140">既定では、多くのプロバイダーが 2048 ビット キー サイズを使用しており、より強固な暗号化を提供するために ISV はこのビット キー サイズを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="47c89-140">By default, many providers use the 2048-bit key size, and we recommend that ISVs use this bit key size, because it provides stronger encryption.</span></span> <span data-ttu-id="47c89-141">ただし、ISV に既に既存の 1024 ビット キー サイズがある場合、そのキー サイズは ISV ライセンス機能で動作します。</span><span class="sxs-lookup"><span data-stu-id="47c89-141">However, if an ISV already has an existing 1024-bit key size, that key size works with the ISV licensing feature.</span></span> 

> [!NOTE]
> <span data-ttu-id="47c89-142">ISV ライセンス機能は、4096 ビット キー サイズをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="47c89-142">The ISV licensing feature doesn't support 4096-bit key sizes.</span></span> <span data-ttu-id="47c89-143">Authenticode 証明書はさまざまな暗号サービス プロバイダーを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-143">Authenticode certificates can have various cryptographic service providers.</span></span> <span data-ttu-id="47c89-144">ISV ライセンス機能は、Enhanced Cryptographic Provider を使います (Base Cryptographic Provider もカバーします)。</span><span class="sxs-lookup"><span data-stu-id="47c89-144">The ISV licensing feature uses Enhanced Cryptographic Provider (which also covers Base Cryptographic Provider).</span></span> <span data-ttu-id="47c89-145">Authenticode 証明書を購入できる多くの独立したプロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="47c89-145">There are many independent providers that you can purchase an Authenticode certificate from.</span></span> <span data-ttu-id="47c89-146">Microsoft が、特定のプロバイダーをお勧めすることはありません。</span><span class="sxs-lookup"><span data-stu-id="47c89-146">Microsoft doesn't recommend any particular provider.</span></span> <span data-ttu-id="47c89-147">頻繁に使用されるプロバイダーには、Symantec VeriSign、Thawte、Go Daddy があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-147">Some providers that are often used are Symantec VeriSign, Thawte, and Go Daddy.</span></span>

## <a name="certificate-import-and-export"></a><span data-ttu-id="47c89-148">証明書のインポートおよびエクスポート</span><span class="sxs-lookup"><span data-stu-id="47c89-148">Certificate import and export</span></span>
<span data-ttu-id="47c89-149">証明書は、お客様のライセンス ファイルに署名し、インポート時にライセンス ファイルを検証するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="47c89-149">The certificate is used to sign your customer license files and validate the license files at the time of import.</span></span> <span data-ttu-id="47c89-150">Authenticode 証明書は、4 つのファイル形式をサポートします。</span><span class="sxs-lookup"><span data-stu-id="47c89-150">Authenticode certificates support four file formats.</span></span> <span data-ttu-id="47c89-151">ISV ライセンス機能については、2 つの形式で証明書ファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="47c89-151">For the ISV licensing feature, you must have the certificate files in two formats:</span></span>

-   <span data-ttu-id="47c89-152">**個人情報交換 (pfx または PKCS \#12 とも呼ばれる)** – .pfx ファイル名拡張子を使用して、証明書、秘密キー、および証明書パスのすべての証明書のセキュリティ保護された保管をサポートする PKCS \#12 形式。</span><span class="sxs-lookup"><span data-stu-id="47c89-152">**Personal Information Exchange (PFX, also known as PKCS \#12)** – The PKCS \#12 format, which uses the .pfx file name extension, supports secure storage of certificates, private keys, and all certificates in a certification path.</span></span> <span data-ttu-id="47c89-153">PKCS \#12 形式は、証明書とそのプライベート キーをエクスポートするために使用される唯一のファイル形式です。</span><span class="sxs-lookup"><span data-stu-id="47c89-153">The PKCS \#12 format is the only file format that can be used to export a certificate and its private key.</span></span>
-   <span data-ttu-id="47c89-154">**Base64 エンコード X.509** - Base64 形式では、単一の証明書の格納がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="47c89-154">**Base64-encoded X.509** – The Base64 format supports storage of a single certificate.</span></span> <span data-ttu-id="47c89-155">この形式では、秘密キーまたは証明書パスの格納はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="47c89-155">This format doesn't support storage of the private key or certification path.</span></span>

<span data-ttu-id="47c89-156">形式に制限があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-156">There is a restriction on the format.</span></span> <span data-ttu-id="47c89-157">PFX (PKCS \#12) 形式は、署名/生成目的でプライベート キーと共に証明書をエクスポートする場合にのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-157">The PFX (PKCS \#12) format should be used only to export the certificate together with its private key for signing/generating purposes.</span></span> <span data-ttu-id="47c89-158">絶対に ISV 組織外に共有しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-158">It should never be shared outside the ISV organization.</span></span> <span data-ttu-id="47c89-159">.cer ファイル名拡張子を使用する DER でエンコードされたバイナリ X.509形式は、アプリケーション オブジェクト ツリー (AOT) ライセンスに埋め込まれる必要がある証明書の公開キーをエクスポートするために使用してください。</span><span class="sxs-lookup"><span data-stu-id="47c89-159">The DER-encoded binary X.509 format, which uses the .cer file name extension, should be used to export the public key of the certificate that must be embedded in the Application Object Tree (AOT) License.</span></span> <span data-ttu-id="47c89-160">この公開キーは、モデルを介して顧客に配布されます。</span><span class="sxs-lookup"><span data-stu-id="47c89-160">This public key is distributed to customers via the model.</span></span> <span data-ttu-id="47c89-161">これは、ライセンスが秘密キーを所有する ISV ライセンスによって署名されていることを確認するために、ライセンスのインポート時に使用されます。</span><span class="sxs-lookup"><span data-stu-id="47c89-161">It's used when a license is imported, to make sure that the license is signed by the ISV license that owns the private key.</span></span>

## <a name="enable-licensing-for-your-isv-solution"></a><span data-ttu-id="47c89-162">ISV ソリューションのライセンスの有効化</span><span class="sxs-lookup"><span data-stu-id="47c89-162">Enable licensing for your ISV solution</span></span>
<span data-ttu-id="47c89-163">ソリューションのライセンスを有効にするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="47c89-163">Follow these steps to enable licensing for your solution.</span></span>

1. <span data-ttu-id="47c89-164">ISV ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-164">Create an ISV solution.</span></span> <span data-ttu-id="47c89-165">Visual Studio で、**ファイル \> 新しいプロジェクト** の順番にクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-165">In Visual Studio, click **File \> New project**.</span></span> <span data-ttu-id="47c89-166">**新しいプロジェクト** ダイアログ ボックスで、**インストール済 > テンプレート > Dynamics 365** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-166">In the **New Project** dialog, click **Installed > Templates > Dynamics 365**.</span></span>  <span data-ttu-id="47c89-167">**財務業務** プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-167">Create a **Finance Operations** project.</span></span> <span data-ttu-id="47c89-168">この例では、プロジェクトに **NewISVSolution** という名前を付けました。</span><span class="sxs-lookup"><span data-stu-id="47c89-168">In this example, we named the project **NewISVSolution**.</span></span>

    ![ISV ソリューションを作成しています](media/isv_new_isv_project.png)

2. <span data-ttu-id="47c89-170">リソースとしてプロジェクトに証明書の公開キー (.cer ファイル) を追加します。</span><span class="sxs-lookup"><span data-stu-id="47c89-170">Add the certificate's public key (.cer file) to your project as a resource.</span></span> <span data-ttu-id="47c89-171">テスト用の証明書を作成するには、[付録: テスト目的での自己署名証明書の作成](#appendix-create-self-signed-certificates-for-test-purposes) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c89-171">To create a certificate for testing, see [Appendix: Create self-signed certificates for test purposes](#appendix-create-self-signed-certificates-for-test-purposes).</span></span>

    1. <span data-ttu-id="47c89-172">ソリューション エクスプローラーで、プロジェクトを右クリックし、**追加 \> 新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-172">Right-click the project in Solution Explorer, then click **Add \> New item**.</span></span> 
    2. <span data-ttu-id="47c89-173">**インストール済み \> Dynamics 365 項目** で、**ラベルとリソース** をクリックし、**リソース** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="47c89-173">Under **Installed \> Dynamics 365 Items**, click **Labels And Resources**, and then select **Resource**.</span></span> <span data-ttu-id="47c89-174">リソースに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="47c89-174">Name the resource.</span></span> <span data-ttu-id="47c89-175">この例では、リソースに **ISVCert** という名前を付けました。</span><span class="sxs-lookup"><span data-stu-id="47c89-175">In this example, we named the resource **ISVCert**.</span></span>

        ![リソースをクリックする](media/isv_new_resource.png)

    3. <span data-ttu-id="47c89-177">**追加** をクリックし、証明書の公開キー ファイル (.cer ファイル) を選択します。</span><span class="sxs-lookup"><span data-stu-id="47c89-177">Click **Add** and select the certificate's public key file (.cer file).</span></span>

        ![リソースとして証明書の公開キーを選択](media/isv_select_cer.png)

    4. <span data-ttu-id="47c89-179">**開く** をクリックして証明書を追加します。</span><span class="sxs-lookup"><span data-stu-id="47c89-179">Click **Open** to add the certificate.</span></span>

        ![リソースとして証明書を追加](media/isv_resource_cer.png)

3. <span data-ttu-id="47c89-181">ライセンス コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-181">Create a license code.</span></span> <span data-ttu-id="47c89-182">ソリューション エクスプローラーで、プロジェクトを右クリックし、**追加 \> 新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-182">Right-click the project in Solution Explorer, then click **Add \> New item**.</span></span> <span data-ttu-id="47c89-183">**インストール済み \> Dynamics 365の項目** で、**構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47c89-183">Under **Installed \> Dynamics 365 Items**, choose **Configuration**.</span></span> <span data-ttu-id="47c89-184">一覧で、**ライセンス コード** を選択し、ライセンス コードに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="47c89-184">In the list, choose **License Code** and name the license code.</span></span> <span data-ttu-id="47c89-185">この例では、ライセンス コードに **ISVLicenseCode** という名前を付けました。</span><span class="sxs-lookup"><span data-stu-id="47c89-185">In this example, we named the license code **ISVLicenseCode**.</span></span> <span data-ttu-id="47c89-186">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-186">Click **Add**.</span></span>

    ![ライセンス コードを作成しています](media/isv_new_license_code.png)

4. <span data-ttu-id="47c89-188">ライセンス コードに証明書をマップします。</span><span class="sxs-lookup"><span data-stu-id="47c89-188">Map the certificate to the license code.</span></span> <span data-ttu-id="47c89-189">ライセンス コードの [プロパティ] ウィンドウで、**証明書** プロパティを証明書リソースに設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-189">In the Properties window for the license code, set the **Certificate** property to your certificate resource.</span></span> <span data-ttu-id="47c89-190">この例では、**証明書** を **ISVCert** に設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-190">In this example, we set **Certificate** to **ISVCert**.</span></span>

    ![ライセンス コードへの証明書のマッピング](media/isv_map_license_cert.png)

5. <span data-ttu-id="47c89-192">1 つまたは複数のコンフィギュレーション キーを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-192">Create one or more configuration keys.</span></span> <span data-ttu-id="47c89-193">ソリューション エクスプローラーで、プロジェクトを右クリックし、**追加 \> 新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-193">Right-click the project in Solution Explorer, then click **Add \> New item**.</span></span> <span data-ttu-id="47c89-194">**インストール済み \> Dynamics 365の項目** で、**構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47c89-194">Under **Installed \> Dynamics 365 Items**, choose **Configuration**.</span></span> <span data-ttu-id="47c89-195">一覧で、**コンフィギュレーション キー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47c89-195">In the list, choose **Configuration Key**.</span></span> <span data-ttu-id="47c89-196">キーに名前を付けて、**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-196">Name the key and click **Add**.</span></span> <span data-ttu-id="47c89-197">この例では、コンフィギュレーション キーに **ISVConfigurationKey1** という名前を付けました。</span><span class="sxs-lookup"><span data-stu-id="47c89-197">In this example, we named the configuration key **ISVConfigurationKey1**.</span></span>

    ![コンフィギュレーション キーを作成しています](media/isv_new_configuration_key.png)

6. <span data-ttu-id="47c89-199">ライセンス コードをコンフィギュレーション キーに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="47c89-199">Associate the license code with the configuration key.</span></span> <span data-ttu-id="47c89-200">ソリューション エクスプローラーで、コンフィギュレーション キーをダブルクリックして、[プロパティ] ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="47c89-200">In Solution Explorer, double-click the configuration key to open the Properties window.</span></span> <span data-ttu-id="47c89-201">[プロパティ] ウィンドウで、**LicenseCode** プロパティをライセンス コードに設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-201">In the Properties window, set the **LicenseCode** property to your license code.</span></span> <span data-ttu-id="47c89-202">この例では、**LicenseCode** を **ISVLicenseCode** に設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-202">In this example, we set the **LicenseCode** to **ISVLicenseCode**.</span></span>

    <span data-ttu-id="47c89-203">[</span><span class="sxs-lookup"><span data-stu-id="47c89-203">[</span></span>![ライセンス コードとコンフィギュレーション キーの関連付け](media/isv_select_license_code.png)

7. <span data-ttu-id="47c89-205">コンフィギュレーション キーをソリューションの要素に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="47c89-205">Associate a configuration key to an element in your solution.</span></span> <span data-ttu-id="47c89-206">たとえば、新しいフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-206">For example, create a new form.</span></span> <span data-ttu-id="47c89-207">ソリューション エクスプローラーで、プロジェクトを右クリックし、**追加 \> 新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-207">Right-click the project in Solution Explorer, then click **Add \> New item**.</span></span> <span data-ttu-id="47c89-208">**インストール済み \> Dynamics 365の項目** で、**ユーザー インターフェイス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="47c89-208">Under **Installed \> Dynamics 365 Items**, choose **User Interface**.</span></span> <span data-ttu-id="47c89-209">一覧で、**フォーム** を選択し、名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="47c89-209">In the list, choose **Form** and give it a name.</span></span> <span data-ttu-id="47c89-210">この例では、フォームに **ISVForm** という名前を付けました。</span><span class="sxs-lookup"><span data-stu-id="47c89-210">In this example, we named the form **ISVForm**.</span></span>

    ![新しいフォームを作成しています](media/isv_new_form.png)

8. <span data-ttu-id="47c89-212">フォームにボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="47c89-212">Add a button to the form.</span></span> <span data-ttu-id="47c89-213">ソリューション エクスプローラーで、フォームをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="47c89-213">Double-click the form in the Solution Explorer.</span></span> <span data-ttu-id="47c89-214">[デザイン] ウィンドウで右クリックし、**新規作成**、**ボタン** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="47c89-214">In the Design window, right-click and select **New**, and then **Button**.</span></span> <span data-ttu-id="47c89-215">**テキスト** プロパティを **ISVButton** に設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-215">Set the **Text** property to **ISVButton**.</span></span>

    ![新しいフォームへのボタンの追加](media/isv_button_designtime.png)

    <span data-ttu-id="47c89-217">実行時に、ボタンは最初はコンフィギュレーション キーで制御されていないため、表示されます。</span><span class="sxs-lookup"><span data-stu-id="47c89-217">At runtime, the button is visible because it isn't controlled by a configuration key at first.</span></span> 

    ![最初に追加されるときに、新しいボタンが表示されます](media/isv_button_visible_runtime.png)

9.  <span data-ttu-id="47c89-219">コンフィギュレーション キーをボタンに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="47c89-219">Associate a configuration key with the button.</span></span> <span data-ttu-id="47c89-220">ボタンの [プロパティ] ウィンドウで、**コンフィギュレーション キー** プロパティを コンフィギュレーションに設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-220">In the Properties window for the button, set the **Configuration Key** property to your configuration.</span></span> <span data-ttu-id="47c89-221">この例では、**コンフィギュレーション キー** を **ISVConfigurationKey1** に設定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-221">In this example, we set the **Configuration Key** to **ISVConfigurationKey1**.</span></span>

    ![コンフィギュレーション キーとボタンの関連付け](media/isv_select_key_for_button.png) 

    <span data-ttu-id="47c89-223">実行時に、コンフィギュレーション キーが使用可能で有効になっている必要があるため、ボタンは表示されません。</span><span class="sxs-lookup"><span data-stu-id="47c89-223">At runtime, the button is not visible because the configuration key must be available and enabled.</span></span> 

    ![ボタンが表示されていません](media/isv_button_invisible_runtime.png)


## <a name="create-a-package-and-generate-a-customer-specific-license"></a><span data-ttu-id="47c89-225">パッケージを作成し、顧客固有のライセンスを生成する</span><span class="sxs-lookup"><span data-stu-id="47c89-225">Create a package and generate a customer-specific license</span></span>
1.  <span data-ttu-id="47c89-226">ライセンスを発行する顧客のテナント名と ID を収集します。</span><span class="sxs-lookup"><span data-stu-id="47c89-226">Collect the tenant name and ID for the customer to issue the license to.</span></span> <span data-ttu-id="47c89-227">この情報については **ライセンス** タブの **設定 \> ヘルプ \& サポート \> バージョン情報** で確認できます。</span><span class="sxs-lookup"><span data-stu-id="47c89-227">You can find this information at **Settings \> Help \& Support \> About** on the **Licenses** tab.</span></span> 

    ![顧客のテナント名および ID](./media/isv_tenant_id.png)

2.  <span data-ttu-id="47c89-229">顧客のライセンス (テナント ID と名前) を生成し、証明書のプライベート キーを使用してライセンスを登録します。</span><span class="sxs-lookup"><span data-stu-id="47c89-229">Generate a license for the customer (tenant ID and name), and sign the license by using the certificate's private key.</span></span> <span data-ttu-id="47c89-230">ライセンス ファイルを作成するには、**axutil genlicense** コマンドに、以下のパラメーターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-230">You must pass the following parameters to the **axutil genlicense** command to create the license file.</span></span>

    | <span data-ttu-id="47c89-231">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="47c89-231">Parameter name</span></span>  | <span data-ttu-id="47c89-232">説明</span><span class="sxs-lookup"><span data-stu-id="47c89-232">Description</span></span>                                                                  |
    |-----------------|------------------------------------------------------------------------------|
    | <span data-ttu-id="47c89-233">ファイル</span><span class="sxs-lookup"><span data-stu-id="47c89-233">file</span></span>            | <span data-ttu-id="47c89-234">ライセンス ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="47c89-234">The name of your license file.</span></span>                                               |
    | <span data-ttu-id="47c89-235">licensecode</span><span class="sxs-lookup"><span data-stu-id="47c89-235">licensecode</span></span>     | <span data-ttu-id="47c89-236">Microsoft Visual Studio のライセンス コードの名前。</span><span class="sxs-lookup"><span data-stu-id="47c89-236">The name of your license code (from Microsoft Visual Studio).</span></span>                |
    | <span data-ttu-id="47c89-237">certificatepath</span><span class="sxs-lookup"><span data-stu-id="47c89-237">certificatepath</span></span> | <span data-ttu-id="47c89-238">証明書のプライベート キーのパス。</span><span class="sxs-lookup"><span data-stu-id="47c89-238">The path of your certificate's private key.</span></span>                                  |
    | <span data-ttu-id="47c89-239">パスワード</span><span class="sxs-lookup"><span data-stu-id="47c89-239">password</span></span>        | <span data-ttu-id="47c89-240">証明書のプライベート キーのパスワード。</span><span class="sxs-lookup"><span data-stu-id="47c89-240">The password for your certificate's private key.</span></span>                             |
    | <span data-ttu-id="47c89-241">顧客</span><span class="sxs-lookup"><span data-stu-id="47c89-241">customer</span></span>        | <span data-ttu-id="47c89-242">(手順 1 のスクリーンショットから) 顧客のテナント名。</span><span class="sxs-lookup"><span data-stu-id="47c89-242">The customer's tenant name (from the screenshot under step 1).</span></span>              |
    | <span data-ttu-id="47c89-243">serialnumber</span><span class="sxs-lookup"><span data-stu-id="47c89-243">serialnumber</span></span>    | <span data-ttu-id="47c89-244">顧客のテナント ID (スクリーンショットに "シリアル番号" と表示されています)。</span><span class="sxs-lookup"><span data-stu-id="47c89-244">The customer's tenant ID (labeled "Serial number" in the screenshot).</span></span>       |
    | <span data-ttu-id="47c89-245">expirationdate</span><span class="sxs-lookup"><span data-stu-id="47c89-245">expirationdate</span></span>  | <span data-ttu-id="47c89-246">オプション: ライセンスの有効期限。</span><span class="sxs-lookup"><span data-stu-id="47c89-246">Optional: The expiration date for the license.</span></span>                               |
    | <span data-ttu-id="47c89-247">usercount</span><span class="sxs-lookup"><span data-stu-id="47c89-247">usercount</span></span>       | <span data-ttu-id="47c89-248">オプション: カスタム検証ロジックが必要に応じて使用できる数値。</span><span class="sxs-lookup"><span data-stu-id="47c89-248">Optional: The number that custom validation logic can use as required.</span></span> <span data-ttu-id="47c89-249">これはユーザーになる可能性がありますが、必ずしもユーザーに限定されません。</span><span class="sxs-lookup"><span data-stu-id="47c89-249">This could be users, but is not limited to users.</span></span> |

    <span data-ttu-id="47c89-250">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="47c89-250">Here is an example.</span></span>
 
    ```Console
    C:\AOSService\PackagesLocalDirectory\Bin\axutil genlicense /file:c:\templicense.txt /certificatepath:c:\tempisvcert.pfx /licensecode:ISVLicenseCode /customer:TAEOfficial.ccsctp.net /serialnumber:4dbfcf74-c5a6-4727-b638-d56e51d1f381 /password:********
    ``` 


3.  <span data-ttu-id="47c89-251">ライセンスをターゲット環境にインポートします。</span><span class="sxs-lookup"><span data-stu-id="47c89-251">Import the license into the target environment.</span></span>

    > [!NOTE]
    > <span data-ttu-id="47c89-252">実稼動システムでは、配置可能パッケージを使用して、Microsoft Dynamics Lifecycle Services (LCS) からこの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="47c89-252">In production systems, you complete this step from Microsoft Dynamics Lifecycle Services (LCS), by using a deployable package.</span></span> <span data-ttu-id="47c89-253">詳細については、このトピックの後半の "実稼働環境" セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c89-253">For more information, see the "Production environments" section later in this topic.</span></span>

    | <span data-ttu-id="47c89-254">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="47c89-254">Parameter name</span></span>                | <span data-ttu-id="47c89-255">説明</span><span class="sxs-lookup"><span data-stu-id="47c89-255">Description</span></span>                                                                                            |
    |-------------------------------|--------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="47c89-256">--setupmode importlicensefile</span><span class="sxs-lookup"><span data-stu-id="47c89-256">--setupmode importlicensefile</span></span> | <span data-ttu-id="47c89-257">ライセンスが読み込まれることをセットアップ ツールに通知するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-257">Use this parameter to inform the setup tool that a license will be loaded.</span></span>                             |
    | <span data-ttu-id="47c89-258">--metadatadir</span><span class="sxs-lookup"><span data-stu-id="47c89-258">--metadatadir</span></span>                 | <span data-ttu-id="47c89-259">メタデータ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-259">Use this parameter to specify the metadata directory.</span></span> <span data-ttu-id="47c89-260">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-260">You should use the default packages directory.</span></span>   |
    | <span data-ttu-id="47c89-261">--bindir</span><span class="sxs-lookup"><span data-stu-id="47c89-261">--bindir</span></span>                      | <span data-ttu-id="47c89-262">バイナリ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-262">Use this parameter to specify the binaries directory.</span></span> <span data-ttu-id="47c89-263">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-263">You should use the default packages directory.</span></span>   |
    | <span data-ttu-id="47c89-264">--sqlserver</span><span class="sxs-lookup"><span data-stu-id="47c89-264">--sqlserver</span></span>                   | <span data-ttu-id="47c89-265">このパラメーターを使用して Microsoft SQL Server を指定します。</span><span class="sxs-lookup"><span data-stu-id="47c89-265">Use this parameter to specify the Microsoft SQL Server.</span></span> <span data-ttu-id="47c89-266">1 ボックス環境では、ピリオド (**.**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-266">For one-box environment, use a period (**.**).</span></span> |
    | <span data-ttu-id="47c89-267">--sqldatabase</span><span class="sxs-lookup"><span data-stu-id="47c89-267">--sqldatabase</span></span>                 | <span data-ttu-id="47c89-268">SQL Server データベースを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-268">Use this parameter to specify the SQL Server database.</span></span> <span data-ttu-id="47c89-269">1 ボックス環境では、**AXDB** を使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-269">For one-box environments, use **AXDB**.</span></span>     |
    | <span data-ttu-id="47c89-270">--sqluser</span><span class="sxs-lookup"><span data-stu-id="47c89-270">--sqluser</span></span>                     | <span data-ttu-id="47c89-271">SQL Server のユーザーを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-271">Use this parameter to specify the SQL Server user.</span></span> <span data-ttu-id="47c89-272">**axdbadminr** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-272">You should use **axdbadminr**.</span></span>                  |
    | <span data-ttu-id="47c89-273">--sqlpwd</span><span class="sxs-lookup"><span data-stu-id="47c89-273">--sqlpwd</span></span>                      | <span data-ttu-id="47c89-274">SQL Server のパスワードを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-274">Use this parameter to specify the SQL Server password.</span></span>                                                 |
    | <span data-ttu-id="47c89-275">--licensefilename</span><span class="sxs-lookup"><span data-stu-id="47c89-275">--licensefilename</span></span>             | <span data-ttu-id="47c89-276">読み込むライセンス ファイルを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="47c89-276">Use this parameter to specify the license file that will be loaded.</span></span>                                    |

    <span data-ttu-id="47c89-277">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="47c89-277">Here is an example.</span></span>

    ```Console
    C:\AOSService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --setupmode importlicensefile --metadatadir c:\packages --bindir c:\packages --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ******** --licensefilename c:\templicense.txt
    ```

4.  <span data-ttu-id="47c89-278">対応するコンフィギュレーション キーは、**ライセンス コンフィギュレーション** ページで使用可能になり、有効になります。</span><span class="sxs-lookup"><span data-stu-id="47c89-278">The corresponding configuration key will be available and enabled on the **License configuration** page.</span></span> <span data-ttu-id="47c89-279">既定では、コンフィギュレーションが有効です。</span><span class="sxs-lookup"><span data-stu-id="47c89-279">By default, the configuration is enabled.</span></span> <span data-ttu-id="47c89-280">たとえば、次のスクリーンショットで **ISVConfigurationKey1** コンフィギュレーション キーを参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c89-280">For example, see the **ISVConfigurationKey1** configuration key in the following screenshot.</span></span> 

    ![ライセンス設定ページで ISVConfigurationKey1 コンフィギュレーション キーを有効にする](media/isv_license_configuration_page.png)

5.  <span data-ttu-id="47c89-282">非実稼働インストールでは、Visual Studio からデータベースの同期プロセスを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-282">In non-production installations, you must start the database synchronization process from Visual Studio.</span></span>

<span data-ttu-id="47c89-283">コンフィギュレーション キーを有効にした後、次のスクリーンショットに示すように、ボタンは表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="47c89-283">After the configuration key is enabled, the button becomes visible, as shown in the following screenshot.</span></span> 

![コンフィギュレーション キーを有効にするとボタンが表示されます](media/isv_button_visible_runtime.png)

## <a name="protection-best-practices"></a><span data-ttu-id="47c89-285">保護のベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="47c89-285">Protection best practices</span></span>
<span data-ttu-id="47c89-286">ソリューションは、2つの形式で配布することができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-286">Solutions can be delivered in two forms:</span></span>

-   <span data-ttu-id="47c89-287">モデル ファイル (ソース コード)</span><span class="sxs-lookup"><span data-stu-id="47c89-287">Model files (source code)</span></span>
-   <span data-ttu-id="47c89-288">配置可能パッケージ (binary)</span><span class="sxs-lookup"><span data-stu-id="47c89-288">Deployable packages (binary)</span></span>

<span data-ttu-id="47c89-289">構成キーとライセンス コードを保護するには、展開可能なパッケージを使用してバイナリ形式でリリースすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="47c89-289">To protect your configuration keys and license codes, we recommend that you release them in binary form, by using a deployable package.</span></span> <span data-ttu-id="47c89-290">顧客は Visual Studio のこれらの要素をインストールして対話することができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-290">Customers will then be able to install and interact with those elements in Visual Studio.</span></span> <span data-ttu-id="47c89-291">顧客が配置可能パッケージ内の項目を参照することはできますが、ソース コードにアクセスしたり項目を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="47c89-291">Although customers will be able to refer to items in the deployable package, they won't be able to access source code or make modifications to the items.</span></span> <span data-ttu-id="47c89-292">(ただし、拡張機能を作成できます。) バイナリ形式でソリューションをリリースする機能の詳細は、すぐに利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="47c89-292">(However, they can create extensions.) More details about the capability to release solutions in binary form will be available soon.</span></span> <span data-ttu-id="47c89-293">配置可能パッケージ (バイナリ) には、顧客がアクセスを必要とせず、カスタマイズできないようなクラスやその他のロジックも含めることができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-293">The deployable package (binary) can also include classes and other logic that your customer doesn't require access to and should not be able to customize.</span></span> 

![保護されている ISV ソリューションと保護されていない ISV ソリューション](./media/isv_protected_solution.png)

## <a name="production-environments"></a><span data-ttu-id="47c89-295">実稼働環境</span><span class="sxs-lookup"><span data-stu-id="47c89-295">Production environments</span></span>
<span data-ttu-id="47c89-296">実稼働システムに ISV ライセンスをインストールするには、LCS によって展開可能なパッケージを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-296">To install ISV licenses in production systems, you must use a deployable package through LCS.</span></span> <span data-ttu-id="47c89-297">コンフィギュレーション モード用テンプレート パッケージは、すべてのインストールに関して次の場所にあります: \<PackagesFolder\>\\bin\\CustomDeployablePackage\\ImportISVLicense.zip (パッケージ フォルダーは通常次の下にあります j:\\AOSService\\PackagesLocalDirectory or c:\\AOSService\\PackagesLocalDirectory\\)</span><span class="sxs-lookup"><span data-stu-id="47c89-297">You can find a template package for configuration mode at the following location in all installations: \<PackagesFolder\>\\bin\\CustomDeployablePackage\\ImportISVLicense.zip (Packages folder is typically under j:\\AOSService\\PackagesLocalDirectory or c:\\AOSService\\PackagesLocalDirectory\\)</span></span> 

> [!div class="mx-imgBorder"]
> <span data-ttu-id="47c89-298">![コンフィギュレーション モードのテンプレート パッケージの場所](media/isv_template_location.png)</span><span class="sxs-lookup"><span data-stu-id="47c89-298">![Location of the template package for configuration mode](media/isv_template_location.png)</span></span>

1.  <span data-ttu-id="47c89-299">パッケージ テンプレートのコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-299">Make a copy of the package template.</span></span>
2.  <span data-ttu-id="47c89-300">パッケージ テンプレート内の次のフォルダーにライセンス ファイルを配置: ImportISVLicense.zip\\AosService\\Scripts\\License</span><span class="sxs-lookup"><span data-stu-id="47c89-300">Put the license file in the following folder within the package template: ImportISVLicense.zip\\AosService\\Scripts\\License</span></span>

<span data-ttu-id="47c89-301">一度に複数のライセンスをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-301">More than one license can be installed at a time.</span></span> <span data-ttu-id="47c89-302">別のライセンスがいずれかに依存する場合は、それに応じた名前を確認します。</span><span class="sxs-lookup"><span data-stu-id="47c89-302">If one of the licenses depends on another, make sure that it's named accordingly.</span></span> <span data-ttu-id="47c89-303">(ライセンスはアルファベット順にインストールされます。)</span><span class="sxs-lookup"><span data-stu-id="47c89-303">(Licenses are installed in alphabetical order.)</span></span>

## <a name="appendix-create-self-signed-certificates-for-test-purposes"></a><span data-ttu-id="47c89-304">付録: テスト目的での自己署名証明書の作成</span><span class="sxs-lookup"><span data-stu-id="47c89-304">Appendix: Create self-signed certificates for test purposes</span></span>

> [!NOTE]
> <span data-ttu-id="47c89-305">自己署名証明書は、開発時にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="47c89-305">Self-signed certificates can be used only during development.</span></span> <span data-ttu-id="47c89-306">これらは、実稼働環境でサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="47c89-306">They aren't supported in production environments.</span></span>

<span data-ttu-id="47c89-307">プラットフォーム更新プログラム 34 およびそれ以前のバージョン：（非推奨 - ライセンスの作成にSHA1ハッシュアルゴリズムを使用）</span><span class="sxs-lookup"><span data-stu-id="47c89-307">For Platform update 34 and earlier: (Deprecated - uses SHA1 hash algorithm for license creation)</span></span>

1. <span data-ttu-id="47c89-308">テストの目的で、 自己署名の CA 証明書を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="47c89-308">For test purposes, create a self-signed CA certificate.</span></span> <span data-ttu-id="47c89-309">Visual Studio のツール プロンプトを使用して、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="47c89-309">Use the Visual Studio tools prompt to run the following command.</span></span>

    ```Console
    makecert -r -pe -n "CN=IsvCertTestAuthority O=IsvCertTestAuthority" -ss CA -sr LocalMachine -a sha256 -len 2048 -cy authority -sky signature -b 01/01/2016 -sv c:\temp\CA.pvk c:\temp\CA.cer
    ```

    <span data-ttu-id="47c89-310">詳細については、[MakeCert](/windows/win32/seccrypto/makecert) のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="47c89-310">For more information, see the [MakeCert](/windows/win32/seccrypto/makecert) documentation.</span></span>

2. <span data-ttu-id="47c89-311">CA を使用して証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-311">Create a certificate by using the CA.</span></span>

    ```Console
    makecert -pe -n "CN=IsvCertTest O=IsvCertTest" -ss ISVStore -sr LocalMachine -a sha256 -len 2048 -cy end -sky signature -eku 1.3.6.1.5.5.7.3.3 -ic c:\temp\ca.cer -iv c:\temp\ca.pvk -b **/**/**** -sv c:\temp\isvcert.pvk c:\temp\isvcert.cer
    ```

3. <span data-ttu-id="47c89-312">ISV 証明書を PFX 形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="47c89-312">Convert the ISV certificate to PFX format.</span></span>

    ```Console
    pvk2pfx -pvk c:\temp\isvcert.pvk -spc c:\temp\isvcert.cer -pfx c:\temp\isvcert.pfx -po ********
    ```

4. <span data-ttu-id="47c89-313">テスト シナリオでは、すべての AOS インスタンスに手動で自己署名 CA 証明書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="47c89-313">For a test scenario, import the self-signed CA certificate manually on all the AOS instances.</span></span>

    ```Console
    certutil -addstore root c:\temp\ca.cer
    ```

    <span data-ttu-id="47c89-314">ただし、自己署名 ISV 証明書を使用していた場合、CA 証明書ではなくその証明書をインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="47c89-314">However, if a self-signed ISV certificate was used, that certificate must be imported instead of the CA certificate.</span></span>

    ```Console
    certutil -addstore root c:\temp\isvcert.cer
    ```

<span data-ttu-id="47c89-315">プラットフォーム更新プログラム 35 およびそれ以降のバージョン：（ライセンスの作成に SHA256 ハッシュ アルゴリズムを使用）</span><span class="sxs-lookup"><span data-stu-id="47c89-315">For Platform update 35 and later: (Uses SHA256 hash algorithm for license creation)</span></span>

1. <span data-ttu-id="47c89-316">テストの目的で、PowerShell コマンド `New-SelfSignedCertificate` を使用する自己署名証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-316">For test purposes, create a self-signed certificate using the PowerShell command `New-SelfSignedCertificate`:</span></span>
    1. <span data-ttu-id="47c89-317">証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-317">Create the certificate.</span></span> <span data-ttu-id="47c89-318">（メモ: 日付に応じて開始日と終了日を調整する）</span><span class="sxs-lookup"><span data-stu-id="47c89-318">(Note: adjust start and end dates accordingly.)</span></span>

        ```PowerShell
        $cert = New-SelfSignedCertificate -CertStoreLocation Cert:\LocalMachine\My -DnsName "IsvCert" -Type CodeSigningCert -KeyExportPolicy Exportable -HashAlgorithm sha256 -KeyLength 2048 -KeySpec Signature -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -NotBefore (Get-Date -Year 2020 -Month 1 -Day 1) -NotAfter (Get-Date -Year 2022 -Month 12 -Day 31)
        ```

    2. <span data-ttu-id="47c89-319">新しい証明書への参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="47c89-319">Get a reference to the new certificate.</span></span>

        ```PowerShell
        [String]$certPath = Join-Path -Path "cert:\LocalMachine\My\" -ChildPath "$($cert.Thumbprint)"
        ```

    3. <span data-ttu-id="47c89-320">証明書が使用するセキュリティで保護された文字列パスワードを作成します。</span><span class="sxs-lookup"><span data-stu-id="47c89-320">Create the secure string password that the certificate uses.</span></span> <span data-ttu-id="47c89-321">（"##############" を証明書のパスワードに置き換えます）</span><span class="sxs-lookup"><span data-stu-id="47c89-321">(Replace "##############" with the certificate password)</span></span>

        ```PowerShell
        [System.Security.SecureString]$certPassword = ConvertTo-SecureString -String "##############" -Force -AsPlainText
        ```

    4. <span data-ttu-id="47c89-322">パスワードを使用する **.pfx** ファイルとして証明書の秘密キーをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="47c89-322">Export the certificate private key as **.pfx** file using the password.</span></span>

        ```PowerShell
        Export-PfxCertificate -Cert $certPath -FilePath "C:\Temp\IsvCert.pfx" -Password $certPassword
        ```

    5. <span data-ttu-id="47c89-323">**.crt** ファイル形式で証明書の公開キーをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="47c89-323">Export the certificate public key as a **.cer** file.</span></span>

        ```PowerShell
        Export-Certificate -Cert $certPath -FilePath "C:\Temp\IsvCert.cer"
        ```

2. <span data-ttu-id="47c89-324">証明書をルート ストアに追加します。</span><span class="sxs-lookup"><span data-stu-id="47c89-324">Add the certificate to the root store.</span></span>

    ```PowerShell
    certutil -addstore root C:\Temp\IsvCert.cer
    ```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
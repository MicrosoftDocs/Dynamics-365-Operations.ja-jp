---
title: Modern POS (MSIX) 拡張機能パッケージへのコード署名
description: このトピックでは、Modern POS (MSIX) 拡張パッケージにコード署名する方法について説明します。
author: mugunthanm
ms.date: 04/13/2021
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 04-13-2020
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: e2e459a92c270d5df1a31769029e59cfe0172744
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193686"
---
# <a name="code-signing-a-modern-pos-msix-extension-package"></a><span data-ttu-id="8b75f-103">Modern POS (MSIX) 拡張機能パッケージへのコード署名</span><span class="sxs-lookup"><span data-stu-id="8b75f-103">Code signing a Modern POS (MSIX) extension package</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="8b75f-104">このトピックでは、Modern POS (MSIX) 拡張パッケージにコード署名する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8b75f-104">This topic explains how to code sign a Modern POS (MSIX) extension package.</span></span> <span data-ttu-id="8b75f-105">このトピックは、Retail SDK バージョン 10.0.18 以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="8b75f-105">This topic applies to the Retail SDK version 10.0.18 and later.</span></span>

<span data-ttu-id="8b75f-106">MPOS 拡張子の .appx ファイルはすべて、コード署名証明書によって署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b75f-106">All MPOS extension .appx files must be signed by a code signing certificate.</span></span> <span data-ttu-id="8b75f-107">運用には信頼済みの機関の証明書を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b75f-107">We recommend that you use a certificate from a trusted authority for production.</span></span> <span data-ttu-id="8b75f-108">ユニバーサル Windows プラットフォーム (UWP) アプリの署名の詳細については、[パーッケージの署名用の証明書を作成する](/windows/uwp/packaging/create-certificate-package-signing)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b75f-108">For information on signing a Universal Windows Platform (UWP) app, see [Create a certificate for package signing](/windows/uwp/packaging/create-certificate-package-signing).</span></span>

<span data-ttu-id="8b75f-109">ModernPos JavaScript プロジェクト ファイルに署名する証明書を含めるには、.proj ファイルを編集し、証明書の署名用のノードを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b75f-109">To include your certificate for signing in the ModernPos JavaScript project file, edit the .proj file and include the node for certificate signing:</span></span>

```XML
<PackageCertificateKeyFile Condition="Exists('.\MPOS_Extension_Certificate.pfx')">MPOS_Extension_Certificate.pfx</PackageCertificateKeyFile>
```

<span data-ttu-id="8b75f-110">開発目的用の自己署名証明書を使用する場合、証明書を信頼されたルート フォルダーに追加して、そのコンピュータで手動で信頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b75f-110">If you're using a self-signed certificate for development purpose, then the certificate must be manually trusted in that machine by adding it to the trusted root folder.</span></span>

<span data-ttu-id="8b75f-111">ビルド自動化中に、セキュリティで保護された場所やセキュリティで保護されたタスクから証明書をダウンロードして、含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="8b75f-111">You can also download and include a cert from secured location/secure task during your build automation.</span></span>

<span data-ttu-id="8b75f-112">ユニバーサル Windows プラットフォーム パッケージのコード署名に関する詳細については、次のリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="8b75f-112">For information about code signing Universal Windows App packages, see these links:</span></span>

+ [<span data-ttu-id="8b75f-113">ビルド ソリューションのビルド タスクの構成</span><span class="sxs-lookup"><span data-stu-id="8b75f-113">Configure the Build solution build task</span></span>](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-the-build-solution-build-task)
+ [<span data-ttu-id="8b75f-114">パーッケージの署名用の証明書を作成する</span><span class="sxs-lookup"><span data-stu-id="8b75f-114">Create a certificate for package signing</span></span>](/windows/msix/package/create-certificate-package-signing)

<span data-ttu-id="8b75f-115">GitHub のサンプルは、ビルド中に開発目的でのみ使用できる自己署名のテスト証明書を生成します。</span><span class="sxs-lookup"><span data-stu-id="8b75f-115">The sample in GitHub generates a self-signed test certificate during build for development purposes only.</span></span> <span data-ttu-id="8b75f-116">この証明書は、開発シナリオのブロックを解除する場合にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8b75f-116">This certificate is only available to unblock development scenarios.</span></span>

> [!WARNING]
> <span data-ttu-id="8b75f-117">この開発証明書を運用アプリの拡張パッケージに使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="8b75f-117">Do not use this development certificate for production app extension packages.</span></span>

<span data-ttu-id="8b75f-118">生成されたテスト証明書は、プロジェクトの中間出力ディレクトリで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="8b75f-118">The generated test certificate will be available in the project's intermediate output directory.</span></span>

- <span data-ttu-id="8b75f-119">既定では、場所は `bld\x86\Debug\MPOS_Extension_Certificate.pfx` です。</span><span class="sxs-lookup"><span data-stu-id="8b75f-119">By default, the location is `bld\x86\Debug\MPOS_Extension_Certificate.pfx`.</span></span>
- <span data-ttu-id="8b75f-120">開発マシンに拡張機能パッケージを正常にインストールするには、生成されたテスト証明書を手動で信頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b75f-120">The generated test certificate MUST be manually trusted for the extension package to be successfully installed on the development machine.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

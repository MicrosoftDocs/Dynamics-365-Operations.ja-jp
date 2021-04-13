---
title: オンプレミス配置でのドキュメントの生成、発行、および印刷
description: このトピックでは、オンプレミス展開でのドキュメントの生成、公開、印刷の機能について説明します。
author: RichdiMSFT
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 52c40d511bc75f439cf341a252e7a1fc06629ac8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749357"
---
# <a name="document-generation-publishing-and-printing-in-on-premises-deployments"></a><span data-ttu-id="5db7a-103">オンプレミス配置でのドキュメントの生成、発行、および印刷</span><span class="sxs-lookup"><span data-stu-id="5db7a-103">Document generation, publishing, and printing in on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5db7a-104">このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開でのドキュメントの生成、公開、印刷の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-104">This topic describes the capabilities for generating, publishing, and printing documents in on-premises deployments of Microsoft Dynamics 365 Finance + Operations (on-premises).</span></span> <span data-ttu-id="5db7a-105">アプリケーションでは、Microsoft SQL Server Reporting Services (SSRS) によるエンタープライズ ドキュメントの生成に対する、完全に統合された経験を提供します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-105">The application provides a fully integrated experience for enterprise document generation that is powered by Microsoft SQL Server Reporting Services (SSRS).</span></span> <span data-ttu-id="5db7a-106">任意のサポートされているデバイスからは、ユーザーは、業務プロセスにリンクされている業界標準のドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-106">From any supported device, users can produce standard industry documents that are linked to business processes.</span></span> <span data-ttu-id="5db7a-107">これらのドキュメントには、請求書、小切手、梱包明細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5db7a-107">These documents include sales invoices, checks, and packing slips.</span></span> <span data-ttu-id="5db7a-108">ユーザーがネットワーク プリンターに安全に接続できるように、管理者は組み込みのツールを使用してサービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-108">Built-in tools let administrators configure the service so that users can securely connect to network printers.</span></span>

<span data-ttu-id="5db7a-109">Microsoft Dynamics AX 2012 SQL Reporting Services フレームワーク上で構築されたソリューションをアップグレード、または [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) で利用可能なモダン ソリューションを活用することができます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-109">You can upgrade solutions that are built on the Microsoft Dynamics AX 2012 SQL Reporting Services framework, or you can take advantage of the modern solutions that are available in [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>

## <a name="document-publishing-services-secure-reliable-and-convenient"></a><span data-ttu-id="5db7a-110">ドキュメント公開サービス: セキュリティ、信頼性、便利</span><span class="sxs-lookup"><span data-stu-id="5db7a-110">Document publishing services: secure, reliable, and convenient</span></span>
<span data-ttu-id="5db7a-111">従業員は、移動に多くの時間を費やします。</span><span class="sxs-lookup"><span data-stu-id="5db7a-111">Employees spend lots of time on the go.</span></span> <span data-ttu-id="5db7a-112">したがって、従業員がリモートで作業している間、企業は作業員の生産性を維持する能力に依存します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-112">Therefore, businesses depend on their employees' ability to stay productive while they work remotely.</span></span> <span data-ttu-id="5db7a-113">ただし、現在でも、ドキュメントは業務トランザクションおよび記録管理のために不可欠です。</span><span class="sxs-lookup"><span data-stu-id="5db7a-113">However, even today, documents remain critical for business transactions and record keeping.</span></span>

<span data-ttu-id="5db7a-114">モバイル デバイスから、ネットワーク プリンターでドキュメントを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-114">From their mobile devices, users can print documents on network printers.</span></span> <span data-ttu-id="5db7a-115">また、ビジネス ドキュメントの作成を自動化したり、組み込みツールを使用してドキュメントを複数の受信者に送信するように指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-115">Users can also automate the creation of business documents and use built-in tools to configure instructions for routing documents to multiple recipients.</span></span>

<span data-ttu-id="5db7a-116">次のオプションがドキュメントの公開で使用できます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-116">The following options are available for document publishing:</span></span>

- <span data-ttu-id="5db7a-117">**電子メール** - サーバー経由でメールを配布し、レポートを添付ファイルとしてリンクします。</span><span class="sxs-lookup"><span data-stu-id="5db7a-117">**Email** – Distribute mail via a server, and link reports as attachments.</span></span>
- <span data-ttu-id="5db7a-118">**アーカイブ** - 将来の参照および規制順守のためにレポートを保管します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-118">**Archive** – Store reports for future reference and regulatory compliance.</span></span>
- <span data-ttu-id="5db7a-119">**ファイル** – ローカル印刷用にブラウザに直接ダウンロードされる PDF ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-119">**File** – Produce a PDF file that is downloaded directly to the browser for local printing.</span></span>
- <span data-ttu-id="5db7a-120">**印刷** – サポートされているすべてのプラットフォームからネットワーク プリンターに直接ドキュメントを送信します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-120">**Print** – Send documents directly to network printers from all supported platforms.</span></span> <span data-ttu-id="5db7a-121">これらのプラットフォームにはモバイル デバイスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5db7a-121">These platforms include mobile devices.</span></span>

![ドキュメント公開サービス](media/document-publishing-services.png)

<span data-ttu-id="5db7a-123">クラウド ホスト型ソリューションで使用できる情報アクセスのオプションの高いレベルの概要については、[ドキュメント印刷の概要](print-documents.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5db7a-123">For a high-level summary of the options for information access that are available in the cloud-hosted solution, see [Document printing overview](print-documents.md).</span></span>

## <a name="comparing-the-cloud-hosted-and-on-premises-services"></a><span data-ttu-id="5db7a-124">クラウド ホスト サービスとオンプレミス サービスの比較</span><span class="sxs-lookup"><span data-stu-id="5db7a-124">Comparing the cloud-hosted and on-premises services</span></span>
<span data-ttu-id="5db7a-125">クラウド ホスト サービスとは異なり、オンプレミス パブリッシング サービスではドキュメントは PDF ファイルとして生成され、自動的にブラウザにダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-125">Unlike the cloud-hosted service, the on-premises publishing service produces documents as PDF files that are automatically downloaded to the browser.</span></span> <span data-ttu-id="5db7a-126">したがって、ローカル接続デバイスを使用してドキュメントを保存したり、ハード コピーを印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-126">Therefore, users can save documents or print hard copies by using local connected devices.</span></span> <span data-ttu-id="5db7a-127">管理者は、組み込み管理ページを使用して、アプリケーションから直接ネットワーク プリンターへのアクセスを管理できます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-127">Administrators can manage access to network printers directly from the application, by using built-in administrative pages.</span></span> <span data-ttu-id="5db7a-128">必要に応じてレポートを操作したり、定期的にドキュメントを安全に生成して配布するための自動ジョブをスケジュールできます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-128">Users can interact with reports on demand, or they can schedule automatic jobs to securely generate and distribute documents on a recurring basis.</span></span>

<span data-ttu-id="5db7a-129">次の図は、ドキュメントの印刷に関係するコンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="5db7a-129">The following illustration shows the components that are involved in document printing.</span></span>

![ドキュメント印刷](media/Cloud-vs-on-premises.png)

<span data-ttu-id="5db7a-131">拡張機能を使用して、アプリケーション レポートで埋め込みドリルスルー リンクの可用性を管理する方法の詳細については、付録を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5db7a-131">For information about how to use extensions to manage availability of the embedded drill-through links in application reports, see the Appendix.</span></span>

## <a name="managing-access-to-network-printers"></a><span data-ttu-id="5db7a-132">ネットワーク プリンターへのアクセスの管理</span><span class="sxs-lookup"><span data-stu-id="5db7a-132">Managing access to network printers</span></span>
<span data-ttu-id="5db7a-133">管理者は、組み込みの管理ページを使用して、ネットワーク プリンターへのアクセスを管理できます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-133">Administrators can use built-in administrative pages to manage access to network printers.</span></span> <span data-ttu-id="5db7a-134">ネットワーク プリンターは会社ごとにセキュリティで保護され、アプリケーションのユーザーによって共有されます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-134">Network printers are secured per company and shared by users of the application.</span></span> <span data-ttu-id="5db7a-135">ユーザーが提供した設定に基づき、権限を持つドメイン アカウントを使用してドキュメントが出力されます。</span><span class="sxs-lookup"><span data-stu-id="5db7a-135">Documents are then printed by using a privileged domain account, based on settings that the user provides.</span></span> <span data-ttu-id="5db7a-136">オンプレミス配置では、プリンターや FAX などのドメイン リソースに接続するアダプターをインストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5db7a-136">In on-premises deployments, you don't have to install an adapter to connect to domain resources such as printers and fax machines.</span></span>

<span data-ttu-id="5db7a-137">次の図は、ネットワーク プリンターの管理に使用されるページを示しています。</span><span class="sxs-lookup"><span data-stu-id="5db7a-137">The following illustration shows the page that is used to manage network printers.</span></span>

![ネットワーク プリンターのページの管理](media/manage-network-printers.png)

## <a name="appendix"></a><span data-ttu-id="5db7a-139">付録</span><span class="sxs-lookup"><span data-stu-id="5db7a-139">Appendix</span></span>

### <a name="turning-on-embedded-links-in-business-documents"></a><span data-ttu-id="5db7a-140">ビジネス ドキュメントでのリンクの埋め込みを有効にする</span><span class="sxs-lookup"><span data-stu-id="5db7a-140">Turning on embedded links in business documents</span></span>
<span data-ttu-id="5db7a-141">PDF ドキュメントで埋め込みドリルスルー リンクの使用を可能にするコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="5db7a-141">Here is the code that you can use to make embedded drill-through links available in PDF documents.</span></span> 

```xpp
class Controller extends SrsReportRunController
{
    protected void preRunModifyContract()
    {
        this.parmReportContract().parmRdlContract().parmEnableFileDrillThrough(true);
        super();
    }
    static void main(Args _args)
    {
        ...
    }
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
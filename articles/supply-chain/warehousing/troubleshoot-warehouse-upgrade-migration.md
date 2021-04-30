---
title: 高度な倉庫管理へのアップグレードおよび移行のトラブルシューティング
description: このトピックでは、高度な倉庫管理へのアップグレードおよび移行中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 12dcadae2a65d71614a2eee9468ec93cac284a7b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907890"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a><span data-ttu-id="366b4-103">高度な倉庫管理へのアップグレードおよび移行のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="366b4-103">Troubleshoot upgrade and migration to advanced warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="366b4-104">このトピックでは、高度な倉庫管理へのアップグレードおよび移行中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="366b4-104">This topic describes how to fix common issues that you might encounter while you upgrade and migrate to advanced warehouse management.</span></span>

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a><span data-ttu-id="366b4-105">エラー メッセージ "java.security.cert.certPathValidatorException: 証明書パスのトラスト アンカーが見つかりません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="366b4-105">I receive the following error message: "java.security.cert.certPathValidatorException: Trust anchor for certification path is not found."</span></span>

### <a name="issue-description"></a><span data-ttu-id="366b4-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="366b4-106">Issue description</span></span>

<span data-ttu-id="366b4-107">オンプレミス環境の Android 8 以上で自己署名証明書が信頼されていない場合に、倉庫管理モバイル アプリにこのエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="366b4-107">You receive this error message in the Warehouse Management mobile app, because self-signed certificates aren't trusted on Android 8+ in on-premises environments.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="366b4-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="366b4-108">Issue resolution</span></span>

<span data-ttu-id="366b4-109">外部 (パブリック) 証明機関 (CA) を使用します。</span><span class="sxs-lookup"><span data-stu-id="366b4-109">Use an external (public) certifying authority (CA).</span></span> <span data-ttu-id="366b4-110">この問題の修正プログラムは、ウェアハウス アプリのバージョン 1.9.0.0 で入手できます。</span><span class="sxs-lookup"><span data-stu-id="366b4-110">A fix for this issue is available in version 1.9.0.0 of the warehouse app.</span></span> <span data-ttu-id="366b4-111">この問題と修正方法の詳細については、[倉庫管理モバイル アプリの接続の問題のトラブルシューティング](troubleshoot-warehouse-app-connection.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="366b4-111">For more information about this issue and how to fix it, see [Troubleshoot Warehouse Management mobile app connection issues](troubleshoot-warehouse-app-connection.md).</span></span>

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a><span data-ttu-id="366b4-112">基本倉庫管理から高度な倉庫管理に移行するために承認されたプロセスは何ですか。</span><span class="sxs-lookup"><span data-stu-id="366b4-112">What is the approved process for moving from basic warehousing to advanced warehousing?</span></span>

### <a name="issue-description"></a><span data-ttu-id="366b4-113">問題の説明</span><span class="sxs-lookup"><span data-stu-id="366b4-113">Issue description</span></span>

<span data-ttu-id="366b4-114">現在、在庫管理を実行していて基本在庫機能を使用しており、モバイル デバイス、ウェーブ、および作業を活用するために、高度な在庫管理に移行しようとしています。</span><span class="sxs-lookup"><span data-stu-id="366b4-114">You're currently running under stock/inventory management and using basic stock functionality, and you want to move to advanced warehousing to take advantage of mobile devices, waves, and work.</span></span> <span data-ttu-id="366b4-115">ただし、この移行を試みると問題が発生します。</span><span class="sxs-lookup"><span data-stu-id="366b4-115">However, you're experiencing issues when you try to make this move.</span></span> <span data-ttu-id="366b4-116">たとえば、保管分析コード (サイト、倉庫、および場所) を使用するように製品を変更することはできません。製品にはそれらに対するトランザクションが含まれているためです。</span><span class="sxs-lookup"><span data-stu-id="366b4-116">For example, you can't change your products so that they use storage dimensions (site, warehouse, and location), because the products have transactions against them.</span></span> <span data-ttu-id="366b4-117">そのため、基本倉庫管理から高度な倉庫管理に移行するために承認されたプロセスについて学習する必要があります。</span><span class="sxs-lookup"><span data-stu-id="366b4-117">Therefore, you must learn the approved process for moving from basic warehousing to advanced warehousing.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="366b4-118">問題の解決</span><span class="sxs-lookup"><span data-stu-id="366b4-118">Issue resolution</span></span>

<span data-ttu-id="366b4-119">基本倉庫管理から高度な倉庫管理に移行するプロセスの詳細については、次のブログの投稿とドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="366b4-119">For more information about the process for moving from basic warehousing to advanced warehousing, see the following blog posts and documentation:</span></span>

- [<span data-ttu-id="366b4-120">既存の品目と倉庫で倉庫管理プロセスを有効にする</span><span class="sxs-lookup"><span data-stu-id="366b4-120">Enable warehouse management process for existing items and warehouses</span></span>](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [<span data-ttu-id="366b4-121">Microsoft Dynamics AX WMS と新しい R3 倉庫および輸送機能への移行</span><span class="sxs-lookup"><span data-stu-id="366b4-121">Migration of Microsoft Dynamics AX WMS to new R3 warehouse and transportation functionality</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [<span data-ttu-id="366b4-122">WMSI/WMS2 項目の移行</span><span class="sxs-lookup"><span data-stu-id="366b4-122">WMSI/WMS2 item migration</span></span>](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [<span data-ttu-id="366b4-123">倉庫管理を Microsoft Dynamics AX 2012 から Supply Chain Management にアップグレードする</span><span class="sxs-lookup"><span data-stu-id="366b4-123">Upgrade warehouse management from Microsoft Dynamics AX 2012 to Supply Chain Management</span></span>](./upgrade-migration-warehouse-management-processes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Dynamics AX Intelligent Data Management Framework (AX 2012)
description: "The Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) を使用すると、システム管理者が Microsoft Dynamics AX インストールのパフォーマンスを最適化できます。 IDMF は、Microsoft Dynamics AX アプリケーションの正常性の評価と現在の使用パターンの分析を行い、データベース サイズの削減に役立ちます。"
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 13591
ms.assetid: 281449e5-2b65-4243-9234-60ef99405533
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 093108e62bcc622d6326b3095b57271584b0c4c6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="dynamics-ax-intelligent-data-management-framework-ax-2012"></a><span data-ttu-id="90cd5-104">Dynamics AX Intelligent Data Management Framework (AX 2012)</span><span class="sxs-lookup"><span data-stu-id="90cd5-104">Dynamics AX Intelligent Data Management Framework (AX 2012)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90cd5-105">The Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) を使用すると、システム管理者が Microsoft Dynamics AX インストールのパフォーマンスを最適化できます。</span><span class="sxs-lookup"><span data-stu-id="90cd5-105">The Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) lets system administrators optimize the performance of Microsoft Dynamics AX installations.</span></span> <span data-ttu-id="90cd5-106">IDMF は、Microsoft Dynamics AX アプリケーションの正常性の評価と現在の使用パターンの分析を行い、データベース サイズの削減に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="90cd5-106">IDMF assesses the health of the Microsoft Dynamics AX application, analyzes current usage patterns, and helps reduce database size.</span></span>

<span data-ttu-id="90cd5-107">IDMF が移動しました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-107">IDMF has moved.</span></span> <span data-ttu-id="90cd5-108">Microsoft Dynamics Lifecycle Services のダウンロード可能なツール セクションから利用できます。</span><span class="sxs-lookup"><span data-stu-id="90cd5-108">It is now available from the Downloadable tools sections of Microsoft Dynamics Lifecycle Services.</span></span> <span data-ttu-id="90cd5-109">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="90cd5-109">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>

### <a name="what-has-changed"></a><span data-ttu-id="90cd5-110">変更点</span><span class="sxs-lookup"><span data-stu-id="90cd5-110">What has changed</span></span>

<span data-ttu-id="90cd5-111">The Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) を使用すると、システム管理者が Microsoft Dynamics AX インストールのパフォーマンスを最適化できます。</span><span class="sxs-lookup"><span data-stu-id="90cd5-111">The Microsoft Dynamics AX Intelligent Data Management Framework (IDMF) lets system administrators optimize the performance of Microsoft Dynamics AX installations.</span></span> <span data-ttu-id="90cd5-112">IDMF は、Microsoft Dynamics AX アプリケーションの正常性の評価と現在の使用パターンの分析を行い、データベース サイズの削減に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="90cd5-112">IDMF assesses the health of the Microsoft Dynamics AX application, analyzes current usage patterns, and helps reduce database size.</span></span> <span data-ttu-id="90cd5-113">IDMF の 2014 年 10 月のリリースでは、Microsoft Dynamics AX 2012 R3 のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-113">In the October 2014 release of IDMF, support was added for Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="90cd5-114">IDMF の 2014 年 7 月のリリースでは、次の機能が変更されました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-114">In the July 2014 release of IDMF, the following features were changed:</span></span>

-   <span data-ttu-id="90cd5-115">AX 2012 R2 のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-115">Support was added for AX 2012 R2.</span></span>
-   <span data-ttu-id="90cd5-116">Microsoft Dynamics AX 3.0 および Microsoft Dynamics AX 4.0 のサポートが削除されました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-116">Support was removed for Microsoft Dynamics AX 3.0 and Microsoft Dynamics AX 4.0.</span></span>
-   <span data-ttu-id="90cd5-117">システム要件が更新されました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-117">System requirements have been updated.</span></span>
-   <span data-ttu-id="90cd5-118">スレッドのサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="90cd5-118">Threading support was added.</span></span>
-   <span data-ttu-id="90cd5-119">**ByFiscalYear** テンプレートは、非実稼働環境のテスト後に計画的にのみ実行する必要があるため、コンフィギュレーション可能で、既定では非表示です。</span><span class="sxs-lookup"><span data-stu-id="90cd5-119">The **ByFiscalYear** template is configurable, and has been hidden by default because it should only be run intentionally, after testing in a non-production environment.</span></span> <span data-ttu-id="90cd5-120">これにより生産のデータベースから財務トランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="90cd5-120">It removes financial transactions from the production database.</span></span>

<span data-ttu-id="90cd5-121">[サービスのダウンロード](http://go.microsoft.com/fwlink/?LinkID=228149) ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="90cd5-121">Go to the [Services Download](http://go.microsoft.com/fwlink/?LinkID=228149) page.</span></span>







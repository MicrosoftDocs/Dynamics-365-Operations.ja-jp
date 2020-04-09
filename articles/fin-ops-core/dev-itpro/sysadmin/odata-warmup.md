---
title: AOS 起動時に OData メタデータ キャッシュを作成する
description: このトピックでは、AOS 起動時に OData メタデータ キャッシュを作成する方法に関する情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 576a35971a940989f9b2d8d05f56f67c9e3057c1
ms.sourcegitcommit: b952b9f9066a5317259b8344db4c5d99eab4bf3c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/25/2020
ms.locfileid: "3165949"
---
# <a name="build-odata-metadata-cache-when-the-aos-starts"></a><span data-ttu-id="42585-103">AOS 起動時に OData メタデータ キャッシュを作成する</span><span class="sxs-lookup"><span data-stu-id="42585-103">Build OData metadata cache when the AOS starts</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="42585-104">Platform update 32 のリリースでは、最初の OData 要求が行われたときにではなく、Application Object Server (AOS) の起動時に OData メタデータ キャッシュを作成する機能が導入されました。</span><span class="sxs-lookup"><span data-stu-id="42585-104">With the release of Platform update 32, we have introduced the ability to build OData metadata cache when the Application Object Server (AOS) starts, instead of when the first OData request is made.</span></span> <span data-ttu-id="42585-105">これにより、AOS プロセスの再起動後の最初の OData 呼び出しの応答時間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="42585-105">This significantly decreases the response time for the first OData call after an AOS process restart.</span></span>

<span data-ttu-id="42585-106">このオプションは、AOS プロセスが再起動するたびに ビジネス プロセスが OData メタデータ キャッシュが作成されるのを待てない場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="42585-106">This option is useful if your business process can't wait for the OData metadata cache to be built each time that the AOS process restarts.</span></span> <span data-ttu-id="42585-107">この機能を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="42585-107">Follow these steps to turn on this feature.</span></span> 

1. <span data-ttu-id="42585-108">**システム管理** \> **設定** \> **システム パラメーター**に移動します。</span><span class="sxs-lookup"><span data-stu-id="42585-108">Go to **System administration** \> **Setup** \> **System parameters**.</span></span>
2. <span data-ttu-id="42585-109">**一般 タブ** で、**AOS 起動時に OData メタデータ キャッシュを作成する** を選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42585-109">On the **General Tab**, select **Build metadata cache when AOS starts**, and then select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="42585-110">この機能を有効にした場合は、AOS が既に実行されており、1 つの OData 要求を処理している必要があります。</span><span class="sxs-lookup"><span data-stu-id="42585-110">When you enable this functionality, the AOS should already be running and should have served one OData request.</span></span> <span data-ttu-id="42585-111">これは、キャッシュが既に作成されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="42585-111">This means that the cache is already built.</span></span> <span data-ttu-id="42585-112">この新しい機能は、次の AOS 再起動時に有効になります。</span><span class="sxs-lookup"><span data-stu-id="42585-112">This new functionality will take effect during the next AOS restart.</span></span>

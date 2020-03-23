---
title: 二重書き込みのシステム要件
description: このトピックでは、デュアル書き込みの接続設定についてのシステム要件について説明します。
author: ramasri
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 689594723d4fd55ef13d67ce08d0453751cf04cb
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112353"
---
# <a name="system-requirements-for-dual-write"></a><span data-ttu-id="4c79d-103">二重書き込みのシステム要件</span><span class="sxs-lookup"><span data-stu-id="4c79d-103">System requirements for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="4c79d-104">デュアル書き込みの接続設定には、次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="4c79d-104">The setup of a dual-write connection has the following requirements:</span></span>

+ <span data-ttu-id="4c79d-105">Finance and Operations アプリのビルドバージョン 10.0.9、およびプラットフォーム更新プログラム 33 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="4c79d-105">Finance and Operations apps that have build version 10.0.9 and platform update 33 or later</span></span>
+ <span data-ttu-id="4c79d-106">プラットフォーム バージョン 9.1.0000.11732 またはそれ以降の Microsoft Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="4c79d-106">Model-driven apps in Microsoft Dynamics 365 that have platform version 9.1.0000.11732 or later</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4c79d-107">データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並行して実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="4c79d-107">You can't run dual-write and the [Prospect to cash solution](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) for Data integrator side by side.</span></span> <span data-ttu-id="4c79d-108">データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c79d-108">If you're running the Prospect to cash solution for Data integrator, you must uninstall it.</span></span>

## <a name="one-version"></a><span data-ttu-id="4c79d-109">1 つのバージョン</span><span class="sxs-lookup"><span data-stu-id="4c79d-109">One Version</span></span>

<span data-ttu-id="4c79d-110">将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4c79d-110">Future updates of the dual-write solution will be available through One Version.</span></span>

---
title: 二重書き込みのシステム要件
description: このトピックでは、デュアル書き込みの接続設定についてのシステム要件について説明します。
author: RamaKrishnamoorthy
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
ms.author: ramasri
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2f54bcf2a6a5d85a197daccf940c0d5214124fe
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614326"
---
# <a name="system-requirements-for-dual-write"></a><span data-ttu-id="2b23e-103">二重書き込みのシステム要件</span><span class="sxs-lookup"><span data-stu-id="2b23e-103">System requirements for dual-write</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2b23e-104">デュアル書き込みの接続設定には、次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="2b23e-104">The setup of a dual-write connection has the following requirements:</span></span>

+ <span data-ttu-id="2b23e-105">Finance and Operations アプリのビルド バージョン 10.0.9 (10.0.383.20013) (品質更新プログラム)、および Platform update 33 以降</span><span class="sxs-lookup"><span data-stu-id="2b23e-105">Finance and Operations apps that have build version 10.0.9 (10.0.383.20013) (Quality update) and platform update 33 or later</span></span>
+ <span data-ttu-id="2b23e-106">プラットフォーム バージョン 9.1.0000.11732 またはそれ以降の Microsoft Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="2b23e-106">Model-driven apps in Microsoft Dynamics 365 that have platform version 9.1.0000.11732 or later</span></span>

<span data-ttu-id="2b23e-107">二重書き込みには、次の制限があります:</span><span class="sxs-lookup"><span data-stu-id="2b23e-107">Dual-write has these limitations:</span></span>

+ <span data-ttu-id="2b23e-108">データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並行して実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="2b23e-108">You can't run dual-write and the [Prospect to cash solution](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) for Data integrator side by side.</span></span> <span data-ttu-id="2b23e-109">データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b23e-109">If you're running the Prospect to cash solution for Data integrator, you must uninstall it.</span></span>
+ <span data-ttu-id="2b23e-110">二重書き込み設定は、Finance and Operations アプリの試用版インスタンスではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2b23e-110">Dual-write setup is not supported on trial instances of Finance and Operations apps.</span></span> 
+ <span data-ttu-id="2b23e-111">二重書き込みは、会社間のデータ共有をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="2b23e-111">Dual-write does not support cross-company data sharing.</span></span>

## <a name="one-version"></a><span data-ttu-id="2b23e-112">1 つのバージョン</span><span class="sxs-lookup"><span data-stu-id="2b23e-112">One Version</span></span>

<span data-ttu-id="2b23e-113">将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2b23e-113">Future updates of the dual-write solution will be available through One Version.</span></span>

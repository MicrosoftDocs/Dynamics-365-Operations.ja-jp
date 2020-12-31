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
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 45a62234319a7870d37e5d8f13425ea9cb3cd19e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685601"
---
# <a name="system-requirements-for-dual-write"></a><span data-ttu-id="38948-103">二重書き込みのシステム要件</span><span class="sxs-lookup"><span data-stu-id="38948-103">System requirements for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38948-104">デュアル書き込みの接続設定には、次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="38948-104">The setup of a dual-write connection has the following requirements:</span></span>

+ <span data-ttu-id="38948-105">Finance and Operations アプリのビルド バージョン 10.0.9 (10.0.383.20013) (品質更新プログラム)、および Platform update 33 以降</span><span class="sxs-lookup"><span data-stu-id="38948-105">Finance and Operations apps that have build version 10.0.9 (10.0.383.20013) (Quality update) and platform update 33 or later</span></span>
+ <span data-ttu-id="38948-106">プラットフォーム バージョン 9.1.0000.11732 またはそれ以降の Microsoft Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="38948-106">Model-driven apps in Microsoft Dynamics 365 that have platform version 9.1.0000.11732 or later</span></span>

<span data-ttu-id="38948-107">二重書き込みには、次の制限があります:</span><span class="sxs-lookup"><span data-stu-id="38948-107">Dual-write has these limitations:</span></span>

+ <span data-ttu-id="38948-108">データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並行して実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="38948-108">You can't run dual-write and the [Prospect to cash solution](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) for Data integrator side by side.</span></span> <span data-ttu-id="38948-109">データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="38948-109">If you're running the Prospect to cash solution for Data integrator, you must uninstall it.</span></span>
+ <span data-ttu-id="38948-110">二重書き込み設定は、Finance and Operations アプリの試用版インスタンスではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="38948-110">Dual-write setup is not supported on trial instances of Finance and Operations apps.</span></span>
+ <span data-ttu-id="38948-111">単一の Finance and Operations アプリ インスタンスおよび単一の Customer Engagement アプリ インスタンスを統合するには、二重書き込みを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38948-111">Dual-write must be used to integrate a single Finance and Operations app instance and a single customer engagement app instance.</span></span>
+ <span data-ttu-id="38948-112">二重書き込みでは現在、40 の法人に制限されています。</span><span class="sxs-lookup"><span data-stu-id="38948-112">Dual-write currently has a limit of 40 legal entities.</span></span>
+ <span data-ttu-id="38948-113">二重書き込みは、[会社間のデータ共有](../../sysadmin/cross-company-data-sharing.md) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="38948-113">Dual-write does not support [cross-company data sharing](../../sysadmin/cross-company-data-sharing.md).</span></span>
+ <span data-ttu-id="38948-114">二重書き込みでは、Finance and Operations アプリおよび Customer Engagement アプリを、同じ Microsoft Azure Active Directory (Azure AD) テナントに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="38948-114">Dual-write requires that the Finance and Operations app and the customer engagement app must be in the same Microsoft Azure Active Directory (Azure AD) tenant.</span></span>
+ <span data-ttu-id="38948-115">二重書き込みでは、Finance and Operations アプリおよび Customer Engagement アプリを、同じ Microsoft Azure データセンター テナントに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="38948-115">Dual-write requires that the Finance and Operations app and the customer engagement app must be deployed in the same Microsoft Azure datacenter.</span></span>

## <a name="one-version"></a><span data-ttu-id="38948-116">1 つのバージョン</span><span class="sxs-lookup"><span data-stu-id="38948-116">One Version</span></span>

<span data-ttu-id="38948-117">将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="38948-117">Future updates of the dual-write solution will be available through One Version.</span></span>

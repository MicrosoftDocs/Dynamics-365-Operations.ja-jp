---
title: 二重書き込みのシステム要件
description: このトピックでは、デュアル書き込みの接続設定についてのシステム要件について説明します。
author: RamaKrishnamoorthy
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4de3cb867b91bb93575673824a25cd0aa262a428
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754076"
---
# <a name="system-requirements-for-dual-write"></a><span data-ttu-id="13595-103">二重書き込みのシステム要件</span><span class="sxs-lookup"><span data-stu-id="13595-103">System requirements for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13595-104">デュアル書き込みの接続設定には、次の要件があります。</span><span class="sxs-lookup"><span data-stu-id="13595-104">The setup of a dual-write connection has the following requirements:</span></span>

+ <span data-ttu-id="13595-105">Finance and Operations アプリのビルド バージョン 10.0.9 (10.0.383.20013) (品質更新プログラム)、および Platform update 33 以降</span><span class="sxs-lookup"><span data-stu-id="13595-105">Finance and Operations apps that have build version 10.0.9 (10.0.383.20013) (Quality update) and platform update 33 or later</span></span>
+ <span data-ttu-id="13595-106">プラットフォーム バージョン 9.1.0000.11732 以降の Customer Engagement アプリ</span><span class="sxs-lookup"><span data-stu-id="13595-106">Customer engagement apps that have platform version 9.1.0000.11732 or later</span></span>

<span data-ttu-id="13595-107">二重書き込みには、次の制限があります:</span><span class="sxs-lookup"><span data-stu-id="13595-107">Dual-write has these limitations:</span></span>

+ <span data-ttu-id="13595-108">データ インテグレータに対して、二重書き込みと [見込み顧客の収益化ソリューション](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並行して実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="13595-108">You can't run dual-write and the [Prospect to cash solution](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) for Data integrator side by side.</span></span> <span data-ttu-id="13595-109">データ インテグレータで見込み顧客の収益化ソリューションを実行している場合は、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="13595-109">If you're running the Prospect to cash solution for Data integrator, you must uninstall it.</span></span>
+ <span data-ttu-id="13595-110">二重書き込み設定は、Finance and Operations アプリの試用版インスタンスではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="13595-110">Dual-write setup is not supported on trial instances of Finance and Operations apps.</span></span>
+ <span data-ttu-id="13595-111">単一の Finance and Operations アプリ インスタンスおよび単一の Customer Engagement アプリ インスタンスを統合するには、二重書き込みを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13595-111">Dual-write must be used to integrate a single Finance and Operations app instance and a single customer engagement app instance.</span></span>
+ <span data-ttu-id="13595-112">二重書き込みでは現在、40 の法人に制限されています。</span><span class="sxs-lookup"><span data-stu-id="13595-112">Dual-write currently has a limit of 40 legal entities.</span></span>
+ <span data-ttu-id="13595-113">二重書き込みは、[会社間のデータ共有](../../sysadmin/cross-company-data-sharing.md) をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="13595-113">Dual-write does not support [cross-company data sharing](../../sysadmin/cross-company-data-sharing.md).</span></span>
+ <span data-ttu-id="13595-114">二重書き込みでは、Finance and Operations アプリおよび Customer Engagement アプリを、同じ Microsoft Azure Active Directory (Azure AD) テナントに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="13595-114">Dual-write requires that the Finance and Operations app and the customer engagement app must be in the same Microsoft Azure Active Directory (Azure AD) tenant.</span></span>
+ <span data-ttu-id="13595-115">二重書き込みでは、Finance and Operations アプリおよび Customer Engagement アプリを、同じ Microsoft Azure データセンター テナントに配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="13595-115">Dual-write requires that the Finance and Operations app and the customer engagement app must be deployed in the same Microsoft Azure datacenter.</span></span>
+ <span data-ttu-id="13595-116">二重書き込みは、Finance and Operations アプリの **doInsert**、**doUpdate**、および **doDelete** イベントによりトリガーされません。</span><span class="sxs-lookup"><span data-stu-id="13595-116">Dual-write is not triggered by the **doInsert**, **doUpdate**, and **doDelete** events of Finance and Operations apps.</span></span> <span data-ttu-id="13595-117">二重書き込みをトリガーする場合は、Finance and Operations アプリの **挿入**、**更新**、**削除** イベントを使用します。</span><span class="sxs-lookup"><span data-stu-id="13595-117">Use the **Insert**, **Update**, and **Delete** events in Finance and Operations apps when you want to trigger dual-write.</span></span> 
+ <span data-ttu-id="13595-118">二重書き込みでは、分散トランザクションはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="13595-118">Dual-write doesn't support distributed transactions.</span></span> <span data-ttu-id="13595-119">たとえば、[製品受領書の転記プロセスがキャンセルされた](scm-field-service-procurement.md#cancelling-the-posting-process)場合、二重書き込みは製品受領書を Dataverse で作成する場合がありますが、Supply Chain Management では作成しません。</span><span class="sxs-lookup"><span data-stu-id="13595-119">For example, if the [product receipt posting process is cancelled](scm-field-service-procurement.md#cancelling-the-posting-process), dual-write might create the product receipt in Dataverse but not create it in Supply Chain Management.</span></span> 



## <a name="one-version"></a><span data-ttu-id="13595-120">1 つのバージョン</span><span class="sxs-lookup"><span data-stu-id="13595-120">One Version</span></span>

<span data-ttu-id="13595-121">将来的には、二重書き込みソリューションの更新は 1 つのバージョンから利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="13595-121">Future updates of the dual-write solution will be available through One Version.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
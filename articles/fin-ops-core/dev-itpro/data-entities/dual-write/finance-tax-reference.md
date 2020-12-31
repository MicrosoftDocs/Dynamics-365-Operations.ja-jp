---
title: 財務および税参照データへのアクセス
description: このトピックでは、財務および税参照データへのアクセスに関する情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 3003eabf970bc0883ff22d930b4a111925af1eeb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684034"
---
# <a name="access-to-finance-and-tax-reference-data"></a><span data-ttu-id="d50b3-103">財務および税参照データへのアクセス</span><span class="sxs-lookup"><span data-stu-id="d50b3-103">Access to finance and tax reference data</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d50b3-104">すべてのビジネスでは、会計暦年、取引が行われる通貨、ビジネスを運営する金銭が出入りする口座、税率、および送金為替などの、財務データの基本セットが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d50b3-104">Every business works with a basic set of financial data, such as the fiscal calendar year, the currency that business is transacted in, the accounts that the money to run the business comes in to or goes out of, tax rates, and remittance.</span></span> <span data-ttu-id="d50b3-105">このデータは Finance and Operations アプリにあります。</span><span class="sxs-lookup"><span data-stu-id="d50b3-105">This data resides in Finance and Operations apps.</span></span> <span data-ttu-id="d50b3-106">ただし、これは Dataverse に公開されているので、Microsoft Dynamics 365 のモデル駆動型アプリは財務および税データの単一のソースを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="d50b3-106">However, it's exposed to Dataverse so that model-driven apps in Microsoft Dynamics 365 can have a single source for finance and tax data.</span></span> <span data-ttu-id="d50b3-107">この方法により、データはビジネス エコシステム全体で統一されます。</span><span class="sxs-lookup"><span data-stu-id="d50b3-107">In this way, data is uniform across the business ecosystem.</span></span> 

<span data-ttu-id="d50b3-108">財務および税データは、次のマッピングを使用して統合されます。</span><span class="sxs-lookup"><span data-stu-id="d50b3-108">Finance and tax data is integrated by using the following mappings:</span></span>

+ [<span data-ttu-id="d50b3-109">統合された元帳</span><span class="sxs-lookup"><span data-stu-id="d50b3-109">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="d50b3-110">統合された税マスター</span><span class="sxs-lookup"><span data-stu-id="d50b3-110">Integrated tax master</span></span>](tax-mapping.md)

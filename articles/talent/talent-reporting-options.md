---
title: "Talent のレポート オプション"
description: "このトピックでは、顧客が Microsoft Dynamics 365 for Talent のレポートをカスタマイズしたり、新しいレポートを作成する場合の問題を解決する方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="reporting-options-in-talent"></a><span data-ttu-id="f1e2f-103">Talent のレポート オプション</span><span class="sxs-lookup"><span data-stu-id="f1e2f-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1e2f-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="f1e2f-104">**Environment details**</span></span>

<span data-ttu-id="f1e2f-105">この問題は、すべての環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-105">This issue applies to all environments.</span></span>

<span data-ttu-id="f1e2f-106">**現象**</span><span class="sxs-lookup"><span data-stu-id="f1e2f-106">**Symptom**</span></span>

<span data-ttu-id="f1e2f-107">顧客は Microsoft Dynamics 365 for Talent のレポートをカスタマイズしたり、新しいレポートを作成したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="f1e2f-108">**払出**</span><span class="sxs-lookup"><span data-stu-id="f1e2f-108">**Issue**</span></span>

<span data-ttu-id="f1e2f-109">ユーザーは、埋め込み Microsoft Power BI レポートをカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="f1e2f-110">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="f1e2f-110">**Solution**</span></span>

- <span data-ttu-id="f1e2f-111">アプリ用 Common Data Service にフローする Core HR データは、Power BI Desktop に PowerApps CD コネクタ経由でレポートできます。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="f1e2f-112">アプリ用 Common Data Service には Core HR データのサブセットが含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="f1e2f-113">Power BI およびダッシュボードの詳細については、[PowerApps Common Data Service を使用した Power BI レポートおよびダッシュボードの作成](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="f1e2f-114">電子申告 (ER) は、一部の Talent レポートで利用できます。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="f1e2f-115">顧客主導のカスタマイズは、ER コンフィギュレーション オプション経由で実行できます。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="f1e2f-116">データは、Microsoft Office 統合によって Talent が提供するさまざまなデータ エンティティを使用して、Microsoft Excel や Microsoft Word にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="f1e2f-117">**長期のソリューション**</span><span class="sxs-lookup"><span data-stu-id="f1e2f-117">**Long-term solution**</span></span>

<span data-ttu-id="f1e2f-118">追加の Power BI オプションが利用可能になり、さらに多くのデータとエンティティがアプリ用 Common Data Service の一部になります。</span><span class="sxs-lookup"><span data-stu-id="f1e2f-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>


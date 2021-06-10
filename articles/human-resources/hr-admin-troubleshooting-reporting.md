---
title: レポート オプション
description: この記事は、顧客が Microsoft Dynamics 365 Human Resources のレポートをカスタマイズしたり、新しいレポートを作成する場合の問題を解決する方法について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 64a03724d81745373d028d76a8cc64aab66efdbb
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053302"
---
# <a name="reporting-options"></a><span data-ttu-id="08c0a-103">レポート オプション</span><span class="sxs-lookup"><span data-stu-id="08c0a-103">Reporting options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="08c0a-104">**環境の詳細**</span><span class="sxs-lookup"><span data-stu-id="08c0a-104">**Environment details**</span></span>

<span data-ttu-id="08c0a-105">この問題は、すべての環境に適用されます。</span><span class="sxs-lookup"><span data-stu-id="08c0a-105">This issue applies to all environments.</span></span>

<span data-ttu-id="08c0a-106">**現象**</span><span class="sxs-lookup"><span data-stu-id="08c0a-106">**Symptom**</span></span>

<span data-ttu-id="08c0a-107">顧客は Microsoft Dynamics 365 Human Resources のレポートをカスタマイズしたり、新しいレポートを作成したいと考えています。</span><span class="sxs-lookup"><span data-stu-id="08c0a-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="08c0a-108">**出庫**</span><span class="sxs-lookup"><span data-stu-id="08c0a-108">**Issue**</span></span>

<span data-ttu-id="08c0a-109">ユーザーは、埋め込み Microsoft Power BI レポートをカスタマイズすることはできません。</span><span class="sxs-lookup"><span data-stu-id="08c0a-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="08c0a-110">**ソリューション**</span><span class="sxs-lookup"><span data-stu-id="08c0a-110">**Solution**</span></span>

- <span data-ttu-id="08c0a-111">Dataverse にフローする人事管理データは、Power BI Desktop に Power Apps Dataverse コネクタ経由でレポートできます。</span><span class="sxs-lookup"><span data-stu-id="08c0a-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="08c0a-112">Dataverse には、人事管理データのサブセットが含まれていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="08c0a-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="08c0a-113">Power BI およびダッシュ ボードの詳細については、[Power Apps Common Data Service を使用した Power BI レポートおよびダッシュ ボードの作成](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08c0a-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="08c0a-114">電子申告 (ER) は、一部の人事管理レポートで利用できます。</span><span class="sxs-lookup"><span data-stu-id="08c0a-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="08c0a-115">顧客主導のカスタマイズは、ER コンフィギュレーション オプション経由で実行できます。</span><span class="sxs-lookup"><span data-stu-id="08c0a-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="08c0a-116">データは、Microsoft Office 統合によって人事管理が提供するさまざまなデータ エンティティを使用して、Microsoft Excel や Microsoft Word にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="08c0a-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="08c0a-117">**長期のソリューション**</span><span class="sxs-lookup"><span data-stu-id="08c0a-117">**Long-term solution**</span></span>

<span data-ttu-id="08c0a-118">追加の Power BI オプションが利用可能になり、さらに多くのデータとエンティティが Dataverse の一部になります。</span><span class="sxs-lookup"><span data-stu-id="08c0a-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
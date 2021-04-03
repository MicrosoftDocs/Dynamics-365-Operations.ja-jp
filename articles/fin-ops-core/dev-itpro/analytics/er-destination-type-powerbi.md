---
title: Power BI ER 送信先タイプ
description: このトピックでは、送信ドキュメントに対して Power BI ER 送信先タイプをコンフィギュレーションする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 10.0.09
ms.openlocfilehash: a6b6a2e4bc3c0eca8185f501121d9d1ba1b4e063
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561977"
---
# <a name="power-bi-destination"></a><span data-ttu-id="a89e4-103">Power BI 出力先</span><span class="sxs-lookup"><span data-stu-id="a89e4-103">Power BI destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a89e4-104">送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、Microsoft Power BI 送信先をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="a89e4-104">You can configure a Microsoft Power BI destination for each folder or file component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="a89e4-105">送信先の設定に基づいて、生成されたドキュメントは以前にコンフィギュレーションされた SharePoint フォルダーに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a89e4-105">Based on the setting of the destination, a generated document is stored in a previously configured SharePoint folder.</span></span>

<span data-ttu-id="a89e4-106">**有効** を **はい** に設定し、ER コンフィギュレーションを使用して Dynamics 365 Finance インスタンスから Microsoft Power BI サービスへのデータ転送を調整します。</span><span class="sxs-lookup"><span data-stu-id="a89e4-106">Set **Enabled** to **Yes** to use your ER configuration to arrange the transfer of data from your Dynamics 365 Finance instance to Microsoft Power BI services.</span></span> <span data-ttu-id="a89e4-107">転送されたファイルは、その目的にコンフィギュレーションされている Microsoft SharePoint Server インスタンスに保存されます。</span><span class="sxs-lookup"><span data-stu-id="a89e4-107">The transferred files are stored on a Microsoft SharePoint Server instance that must be configured for that purpose.</span></span> <span data-ttu-id="a89e4-108">詳細については、[データを Power BI にプルする電子申告 (ER) の構成](general-electronic-reporting-report-configuration-get-data-powerbi.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a89e4-108">For more information, see [Configure Electronic reporting (ER) to pull data into Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md).</span></span>

<span data-ttu-id="a89e4-109">[![送信先の設定ページ](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span><span class="sxs-lookup"><span data-stu-id="a89e4-109">[![Destination setting page](./media/ER_Destinations-EnablePowerBIDestination.png)](./media/ER_Destinations-EnablePowerBIDestination.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a89e4-110">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a89e4-110">Additional resources</span></span>

- [<span data-ttu-id="a89e4-111">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="a89e4-111">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="a89e4-112">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="a89e4-112">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
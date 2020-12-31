---
title: Dynamics 365 Sales で Dynamics 365 Commerce 価格決定エンジンを使用する
description: このトピックでは、Microsoft Dynamics 365 Commerce 価格決定エンジンを使用して、Dynamics 365 Sales に売上の見積書を作成する方法について説明します。
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594921"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="75eda-103">Dynamics 365 Sales で Dynamics 365 Commerce 価格決定エンジンを使用する</span><span class="sxs-lookup"><span data-stu-id="75eda-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="75eda-104">このトピックでは、Microsoft Dynamics 365 Commerce 価格決定エンジンを使用して、Dynamics 365 Sales に売上の見積書を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="75eda-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="75eda-105">Dynamics 365 Commerce 価格設定エンジンは、店舗レベルの価格設定、提携ベースの価格設定、ロイヤルティ ベースの価格設定、組み合わせ割引、数量割引、しきい値割引など、ほとんどの B2C (企業と一般消費者) 価格設定のシナリオに対応しています。</span><span class="sxs-lookup"><span data-stu-id="75eda-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="75eda-106">価格決定エンジンでは、複雑なルールを使用して、特定の見積または注文に対して最適な価格を決定します。</span><span class="sxs-lookup"><span data-stu-id="75eda-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="75eda-107">[デュアル書き込み](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview)を使用する場合は、価格決定のニーズに対して 3 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="75eda-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="75eda-108">この静的な価格決定は、Dynamics 365 Sales の価格表、Dynamics 365 Supply Chain Management の価格決定エンジン、または Dynamics 365 Commerce の価格決定エンジンを使用して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="75eda-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="75eda-109">これらのオプションの中でも、 Commerce の価格設定エンジンは B2C シナリオに最適です。</span><span class="sxs-lookup"><span data-stu-id="75eda-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="75eda-110">Sales で Commerce の価格設定エンジンを使用する</span><span class="sxs-lookup"><span data-stu-id="75eda-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="75eda-111">現在、Commerce の価格決定エンジンは、販売での見積の作成にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="75eda-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="75eda-112">Commerce の価格決定エンジンと販売注文の統合は、まだ使用できません。</span><span class="sxs-lookup"><span data-stu-id="75eda-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="75eda-113">ユーザーが Sales で販売見積を開始すると、デュアル書き込みフレームワークによって、見積の詳細が Commerce にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="75eda-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="75eda-114">既存の見積明細行に対する変更や、Salesで新たに追加された見積明細行は、Commerce にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="75eda-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="75eda-115">ユーザーは、Commerce の価格決定エンジンを使用して見積に価格を指定する際に、**価格見積り** を選択して Commerce の価格決定エンジンに基づいて見積の価格を更新できます。</span><span class="sxs-lookup"><span data-stu-id="75eda-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="75eda-116">価格は、Sales と Commerce の両方で自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="75eda-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="75eda-117">必要条件</span><span class="sxs-lookup"><span data-stu-id="75eda-117">Prerequisites</span></span>

- <span data-ttu-id="75eda-118">Commerce の価格エンジンを Sales で使用するには、事前に [デュアル書き込みにおける見込顧客から売上へのプロセス](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/) の手順を実行しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="75eda-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="75eda-119">以下の手順で、手動入力の売買契約評価をオフにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="75eda-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="75eda-120">Commerce 環境で、**売掛金勘定 \> 設定 \> 売掛金勘定パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="75eda-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="75eda-121">**価格** タブの **売買契約評価**  クイックタブで、**手動入力** のチェックボックスをオフにし ます。</span><span class="sxs-lookup"><span data-stu-id="75eda-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75eda-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="75eda-122">Additional resources</span></span>

[<span data-ttu-id="75eda-123">二重書き込みの見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="75eda-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)

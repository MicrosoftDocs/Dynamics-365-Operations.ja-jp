---
title: Adyen 問題向け Dynamics 365 Payment Connector の問題解決
description: このトピックでは、Adyen 向け Microsoft Dynamics 365 Payment Connector に関する問題が発生した場合のサポートに役立つトラブルシューティング ガイドを提供します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585404"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="6bb02-103">Adyen 問題向け Dynamics 365 Payment Connector の問題解決</span><span class="sxs-lookup"><span data-stu-id="6bb02-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6bb02-104">このトピックでは、Adyen 向け Microsoft Dynamics 365 Payment Connector に関する問題が発生した場合のサポートに役立つトラブルシューティング ガイドを提供します。</span><span class="sxs-lookup"><span data-stu-id="6bb02-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="6bb02-105">説明</span><span class="sxs-lookup"><span data-stu-id="6bb02-105">Description</span></span>

<span data-ttu-id="6bb02-106">次の領域の Adyen 向け Dynamics 365 Payment Connector に問題があり、Adyen チームのサポートが必要です。</span><span class="sxs-lookup"><span data-stu-id="6bb02-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="6bb02-107">販売時点管理 (POS) の構成、Modern 販売時点管理 (MPOS)、コール センター、および Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="6bb02-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="6bb02-108">Adyen 支払サービス プロバイダ (PSP) 参照番号 (たとえば、手動キー入力 \[MKE\] 拒否を含む、拒否について質問がある場合)</span><span class="sxs-lookup"><span data-stu-id="6bb02-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="6bb02-109">テスト環境またはライブ マーチャント環境で機能していないもの</span><span class="sxs-lookup"><span data-stu-id="6bb02-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="6bb02-110">解像度</span><span class="sxs-lookup"><span data-stu-id="6bb02-110">Resolution</span></span>

<span data-ttu-id="6bb02-111">Adyen チームでプロセスをサポート開始するには、次の電子メール テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="6bb02-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="6bb02-112">トラブルシューティングを迅速化するには、電子メールに必要なすべての詳細が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6bb02-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="6bb02-113">フィールド</span><span class="sxs-lookup"><span data-stu-id="6bb02-113">Field</span></span>        | <span data-ttu-id="6bb02-114">先頭値</span><span class="sxs-lookup"><span data-stu-id="6bb02-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="6bb02-115">宛先</span><span class="sxs-lookup"><span data-stu-id="6bb02-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="6bb02-116">cc</span><span class="sxs-lookup"><span data-stu-id="6bb02-116">Cc</span></span>           | |
| <span data-ttu-id="6bb02-117">件名</span><span class="sxs-lookup"><span data-stu-id="6bb02-117">Subject line</span></span> | <span data-ttu-id="6bb02-118">Microsoft Dynamics サポート リクエスト</span><span class="sxs-lookup"><span data-stu-id="6bb02-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="6bb02-119">本文</span><span class="sxs-lookup"><span data-stu-id="6bb02-119">Body</span></span>         | <p><span data-ttu-id="6bb02-120">こんにちは サポート、</span><span class="sxs-lookup"><span data-stu-id="6bb02-120">Hi Support,</span></span></p><p><span data-ttu-id="6bb02-121">以下の問題についてサポートを提供してください:</span><span class="sxs-lookup"><span data-stu-id="6bb02-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="6bb02-122">マーチャント口座</span><span class="sxs-lookup"><span data-stu-id="6bb02-122">Merchant account</span></span></li><li><span data-ttu-id="6bb02-123">環境 (Test/Prod)</span><span class="sxs-lookup"><span data-stu-id="6bb02-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="6bb02-124">チャンネル (POS/ コール センター / コマース電子商取引)</span><span class="sxs-lookup"><span data-stu-id="6bb02-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="6bb02-125">PSP 参照番号、問題が特定のトランザクションに関係している場合 (Adyen Customer Area、または POS ターミナルのトランザクション メニューにある PSP 参照番号を参照できます。)</span><span class="sxs-lookup"><span data-stu-id="6bb02-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="6bb02-126">該当する場合、エラー メッセージのスクリーンショットまたは写真</span><span class="sxs-lookup"><span data-stu-id="6bb02-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="6bb02-127">イベント ビューアー ログ (.txt 形式)</span><span class="sxs-lookup"><span data-stu-id="6bb02-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="6bb02-128">問題と試したトラブルシューティングの手順</span><span class="sxs-lookup"><span data-stu-id="6bb02-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="6bb02-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6bb02-129">Additional resources</span></span>

[<span data-ttu-id="6bb02-130">Dynamics 365 Commerce の Adyen コネクタで支払を受取る</span><span class="sxs-lookup"><span data-stu-id="6bb02-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="6bb02-131">Adyen 向け Dynamics 365 Payment Connector</span><span class="sxs-lookup"><span data-stu-id="6bb02-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="6bb02-132">Dynamics 365 の Adyen 支払コネクタを設定</span><span class="sxs-lookup"><span data-stu-id="6bb02-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)

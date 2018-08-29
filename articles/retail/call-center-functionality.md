---
title: "コール センターの販売機能"
description: "このトピックは、Microsoft Dynamics 365 for Retail でのコール センターの販売機能の概要を示します。"
author: josaw1
manager: AnnBe
ms.date: 04/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailMCRChannelDetailPage, MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16361
ms.assetid: c8ed2ba4-8d06-4d99-9728-2a83e6d95ca9
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 2b536ad4f29a3bb76294ef2fba30c529c24f1375
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="call-center-sales-functionality"></a><span data-ttu-id="8e24b-103">コール センターの販売機能</span><span class="sxs-lookup"><span data-stu-id="8e24b-103">Call center sales functionality</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8e24b-104">Dynamics 365 for Retail では、コール センターはアプリケーションで定義できる Retail チャンネルのタイプです。</span><span class="sxs-lookup"><span data-stu-id="8e24b-104">In Dynamics 365 for Retail, a call center is a type of Retail channel that can be defined in the application.</span></span> <span data-ttu-id="8e24b-105">コール センター エンティティの特定チャンネルの定義は、システムが、コール センター チャンネルのユーザーによって作成される販売注文に、特定のデータ既定値および処理既定値を関連付けることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="8e24b-105">Defining a specific channel for your call center entities allows the system to tie specific data defaults and order processing defaults to sales orders created by a user of the call center channel.</span></span>

<span data-ttu-id="8e24b-106">コール センターの機能には、詳細な小売価格とプロモーション、カタログ、ギフト カード、ロイヤルティ プログラム、およびクーポンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8e24b-106">Call center features include advanced retail price and promotions, catalogs, gift cards, loyalty programs, and coupons.</span></span> <span data-ttu-id="8e24b-107">コール センター注文は、クロスチャンネル注文処理シナリオをサポートするため、販売時点管理 (POS) アプリケーションによっても利用されます。</span><span class="sxs-lookup"><span data-stu-id="8e24b-107">Call center orders are also leveraged by the point of sale (POS) application to support cross-channel order fulfillment scenarios.</span></span>

<span data-ttu-id="8e24b-108">コール センター モジュールが Retail 以外の他の業界により使用される間に、Dynamics 365 for Retail コール センター アプリケーションの現在のリリースが企業間 (B2B) の注文処理シナリオ、または大量の販売明細行がある注文シナリオでの使用に対して最適化されていない点に注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="8e24b-108">It's important to note that while the call center module can be utilized by other industries outside of Retail, the current release of the Dynamics 365 for Retail call center application hasn't been optimized for use in business-to-business (B2B) order processing scenarios, or scenarios where orders have a large amount of sales lines.</span></span> <span data-ttu-id="8e24b-109">標準的な直接消費者のトランザクション処理以外の注文処理に対してコール センター機能を利用するユーザーが、コール センター機能の有効性が機能性およびパフォーマンスのニーズを満たしているかをテストおよび検証するため、十分の時間をかけるようお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8e24b-109">It's recommended that users who want to utilize the call center features for order processing outside of typical direct-to-consumer transaction processing, take adequate time to test and validate that enabling call center functionality will meet functional and performance needs.</span></span>

<span data-ttu-id="8e24b-110">注文作成のサポートに加えて、コール センター モジュールは、ユーザーが顧客勘定を特定し、関連するすべての顧客の注文データおよび属性を確認しやすくするための、わかりやすい顧客サービス アプリケーションも提供します。</span><span class="sxs-lookup"><span data-stu-id="8e24b-110">In addition to supporting order creation, the call center module also provides a user-friendly customer service application that makes it easier for users to locate customer accounts and review all of the related customer order data and attributes.</span></span> <span data-ttu-id="8e24b-111">顧客サービス画面は、ユーザーが、顧客から来る最も一般的な注文関連の質問に回答するため、関連する注文関連データへのすばやいアクセスを可能にするよう設計されています。</span><span class="sxs-lookup"><span data-stu-id="8e24b-111">The customer service screen is designed to enable a user to quickly access order related data that will allow them to answer the most common order-related questions received from customers.</span></span>

<span data-ttu-id="8e24b-112">このページでは、設定、コンフィギュレーション、および Dynamics 365 for Retail のコール センター機能の機能使用に関連する該当ドキュメントへのリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="8e24b-112">This page provides links to relevant documentation related to the setup, configuration, and functional use of the call center features in Dynamics 365 for Retail.</span></span>

## <a name="configure-the-call-center"></a><span data-ttu-id="8e24b-113">コール センターのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e24b-113">Configure the call center</span></span>
[<span data-ttu-id="8e24b-114">注文処理オプションの設定</span><span class="sxs-lookup"><span data-stu-id="8e24b-114">Set up order processing options</span></span>](set-up-order-processing-options.md)

## <a name="configure-order-processing"></a><span data-ttu-id="8e24b-115">注文処理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e24b-115">Configure order processing</span></span>
[<span data-ttu-id="8e24b-116">詐欺警告の設定</span><span class="sxs-lookup"><span data-stu-id="8e24b-116">Set up fraud alerts</span></span>](set-up-fraud-alerts.md)

[<span data-ttu-id="8e24b-117">手動の注文保留</span><span class="sxs-lookup"><span data-stu-id="8e24b-117">Manual Order Holds</span></span>](work-with-order-holds.md)

## <a name="configure-payment-processing"></a><span data-ttu-id="8e24b-118">支払処理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e24b-118">Configure payment processing</span></span>
[<span data-ttu-id="8e24b-119">コール センターでの支払方法</span><span class="sxs-lookup"><span data-stu-id="8e24b-119">Payment methods in a call center</span></span>](work-with-payments.md)

## <a name="configure-delivery-modes"></a><span data-ttu-id="8e24b-120">出荷モードの構成</span><span class="sxs-lookup"><span data-stu-id="8e24b-120">Configure delivery modes</span></span>
[<span data-ttu-id="8e24b-121">コール センターの出荷モードと雑費の構成</span><span class="sxs-lookup"><span data-stu-id="8e24b-121">Configure call center delivery modes and charges</span></span>](configure-call-center-delivery.md)

## <a name="configure-direct-marketing"></a><span data-ttu-id="8e24b-122">直接マーケティングのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e24b-122">Configure direct marketing</span></span>
[<span data-ttu-id="8e24b-123">コール センターのカタログ</span><span class="sxs-lookup"><span data-stu-id="8e24b-123">Call center catalogs</span></span>](call-center-catalogs.md)

[<span data-ttu-id="8e24b-124">最新/頻度/金額 (RFM) 分析の設定</span><span class="sxs-lookup"><span data-stu-id="8e24b-124">Set up RFM analysis</span></span>](set-up-rfm-analysis.md)

## <a name="configure-continuity-programs"></a><span data-ttu-id="8e24b-125">連続プログラムのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8e24b-125">Configure continuity programs</span></span>
[<span data-ttu-id="8e24b-126">コール センターの連続プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="8e24b-126">Set up a continuity program for a call center</span></span>](set-up-continuity-program.md)



---
title: Retail ソフトウェア開発キット (SDK)
description: このトピックでは、Retail SDK に関する一般情報を提供します。 Retail SDK は、小売クライアントをカスタマイズするために使用できる、コード、コード サンプル、テンプレート、およびツールが含まれています。
author: RobinARH
manager: AnnBe
ms.date: 09/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 17771
ms.assetid: c54d34a5-32e2-4d0d-a1c2-4a9940d95ade
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2018-05-30
ms.dyn365.ops.version: AX 7.3.5
ms.openlocfilehash: 54144a2a0e6539c2cf89a7f8e551a335dc3b3cdb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564390"
---
# <a name="pos-override-request-handler-sdk"></a><span data-ttu-id="cd409-104">POS オーバーライド要求ハンドラー (SDK)</span><span class="sxs-lookup"><span data-stu-id="cd409-104">POS Override request handler (SDK)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd409-105">このトピックでは、POS 要求ハンドラーをオーバーライドする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="cd409-105">This topic explains how to override POS request handler.</span></span> <span data-ttu-id="cd409-106">POS ビジネス ロジックをオーバーライドするための新しい拡張パターンを導入しました。ビジネス ロジックをコア POS 業務フローに変更/追加するシナリオがある場合、このパターンに従うことができます。</span><span class="sxs-lookup"><span data-stu-id="cd409-106">We introduced new extension pattern for overriding the POS business logic, if you have any scenario where you want to modify/add some business logic to the core POS business flow then you can follow this pattern.</span></span>

<span data-ttu-id="cd409-107">例: シリアル品目を販売するとき、POS にはスキャン後にその品目のシリアル番号を入力するためのダイアログが表示されますが、コードを使用してシリアル番号を入力することでシリアル番号のプロセスを自動化する場合、このシリアル番号ハンドラーをオーバーライドしてカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="cd409-107">Ex: When you sell serial item, POS will show a dialog to enter the serial number for that item after the scan, but if you want to automate the serial number process by entering the serial number through code then you can override this serial number handler and customize.</span></span> <span data-ttu-id="cd409-108">POS のビジネス ロジックは、要求と応答に基づいています。</span><span class="sxs-lookup"><span data-stu-id="cd409-108">Any business logic in POS is based upon request and response.</span></span> <span data-ttu-id="cd409-109">そのため、関連する要求をオーバーライドし、ビジネス シナリオに従って応答を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="cd409-109">So, you can override the relevant request and return the response according to your business scenario.</span></span>

<span data-ttu-id="cd409-110">注意: すべての業務要求がカスタマイズできるように公開されるわけではありませんいくつかの要求のみオーバーライド可能です。</span><span class="sxs-lookup"><span data-stu-id="cd409-110">Note: Not all business request is exposed for customization only few requests are overridable.</span></span> <span data-ttu-id="cd409-111">ビジネス ロジックをカスタマイズする場合で、その要求がオーバーライド可能でない場合、サポート チケットを作成するか、LCS 機能拡張ツールでリクエストを登録します。</span><span class="sxs-lookup"><span data-stu-id="cd409-111">If you want to customize any business logic and if that request is not overrdiable then create a support ticket or log a request in the LCS extensibility tool.</span></span> <span data-ttu-id="cd409-112">この記事の後方では、オーバーライドできる要求の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="cd409-112">Later in this article we have listed the list of requests available for overriding.</span></span>

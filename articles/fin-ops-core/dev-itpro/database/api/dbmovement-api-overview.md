---
title: データベース移動 API
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) データベース移動アプリケーション プログラミング インターフェイス (API) の概要について説明します。
author: laneswenka
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 675b9812921248cfcd4338a5dcf6720c3b9e2f18
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752776"
---
# <a name="database-movement-api"></a><span data-ttu-id="b5298-103">データベース移動 API</span><span class="sxs-lookup"><span data-stu-id="b5298-103">Database Movement API</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5298-104">データベース移動アプリケーション プログラミング インターフェイス (API) は、Microsoft Dynamics 365 環境のデータ ライフサイクルを管理するために使用される RESTful エンドポイントです。</span><span class="sxs-lookup"><span data-stu-id="b5298-104">The Database Movement application programming interface (API) is a RESTful endpoint that is used to manage the data lifecycle of Microsoft Dynamics 365 environments.</span></span> <span data-ttu-id="b5298-105">これは、環境間でのデータベースのコピー、およびデータベース バックアップの一覧表示とダウンロードのために現在使用できる、バージョン管理された一連の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="b5298-105">It provides a versioned set of capabilities that you can currently use to copy databases between environments, and to list and download database backups.</span></span> <span data-ttu-id="b5298-106">後のリリースでは、更にサポートされているアクションの数が追加されます。</span><span class="sxs-lookup"><span data-stu-id="b5298-106">More supported actions will be added in later releases.</span></span>

## <a name="what-is-supported-by-the-database-movement-api"></a><span data-ttu-id="b5298-107">データベース移動 API では何がサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="b5298-107">What is supported by the Database Movement API?</span></span>

<span data-ttu-id="b5298-108">データベース移動 API では、次の Dynamics 365 サービスに対する RESTful エンドポイントが公開されます。</span><span class="sxs-lookup"><span data-stu-id="b5298-108">The Database Movement API exposes RESTful endpoints for the following Dynamics 365 services:</span></span>

* <span data-ttu-id="b5298-109">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b5298-109">Dynamics 365 Finance</span></span>
* <span data-ttu-id="b5298-110">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b5298-110">Dynamics 365 Supply Chain Management</span></span>
* <span data-ttu-id="b5298-111">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b5298-111">Dynamics 365 Commerce</span></span>

## <a name="next-steps"></a><span data-ttu-id="b5298-112">次のステップ</span><span class="sxs-lookup"><span data-stu-id="b5298-112">Next steps</span></span>

* <span data-ttu-id="b5298-113">[認証](dbmovement-api-authentication.md) の設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b5298-113">Learn how to set up [authentication](dbmovement-api-authentication.md).</span></span>
* <span data-ttu-id="b5298-114">[API リファレンス](./v1/dbmovement-api-v1-overview.md) を確認します。</span><span class="sxs-lookup"><span data-stu-id="b5298-114">Review the [API reference](./v1/dbmovement-api-v1-overview.md).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
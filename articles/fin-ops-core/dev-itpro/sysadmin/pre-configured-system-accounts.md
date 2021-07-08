---
title: コンフィギュレーション済みのシステム アカウント
description: このトピックでは、Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。
author: laneswenka
ms.date: 06/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 5d56f8bede3d312c39f0619c1969607da912e4eb
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216550"
---
# <a name="preconfigured-system-accounts"></a><span data-ttu-id="8bd0c-103">コンフィギュレーション済みのシステム アカウント</span><span class="sxs-lookup"><span data-stu-id="8bd0c-103">Preconfigured system accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8bd0c-104">構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-104">Pre-configured system accounts are included on deployed environments so that Microsoft can manage and operate the Finance and Operations service and provide specific features to customers.</span></span> <span data-ttu-id="8bd0c-105">次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-105">The following table provides information about each account, including the purpose and use case for the account.</span></span>  

> [!IMPORTANT] 
> <span data-ttu-id="8bd0c-106">システム アカウントを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-106">Do not delete these system accounts.</span></span> <span data-ttu-id="8bd0c-107">これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-107">Deleting these accounts will cause a disruption in key functionality provided by Microsoft.</span></span>

| <span data-ttu-id="8bd0c-108">口座の詳細</span><span class="sxs-lookup"><span data-stu-id="8bd0c-108">Account detail</span></span> | <span data-ttu-id="8bd0c-109">アカウントの目的/ユース ケース</span><span class="sxs-lookup"><span data-stu-id="8bd0c-109">Purpose/use case of the account</span></span>|
|---|---|
| `Axrunner` | <span data-ttu-id="8bd0c-110">このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-110">This account is used to monitor the health of the environment and provide alerts when necessary.</span></span><br><br><span data-ttu-id="8bd0c-111">**注**: このアカウントは、セルフサービス環境で非推奨になり、使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-111">**Note**: This account is deprecated with self-service environments and is no longer used.</span></span> |
| `FRServiceUser` | <span data-ttu-id="8bd0c-112">このアカウントは Financial Reporting のユーザー アカウントで、Management Reporter アプリケーションが  Finance and Operations と統合するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-112">This account is the Financial Reporting service user account, which is used by the Management Reporter application for integrations with Finance and Operations.</span></span> |
| `RetailServiceAccount` | <span data-ttu-id="8bd0c-113">このアカウントは、Retail サービスで Finance and Operations 環境に接続するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-113">This account is used for Retail services to connect to the Finance and Operations environment.</span></span> |
| <span data-ttu-id="8bd0c-114">`SysHealthServiceUser` または `Axping` (展開された製品バージョンによって異なる)</span><span class="sxs-lookup"><span data-stu-id="8bd0c-114">`SysHealthServiceUser` or `Axping` (depending on the deployed product version)</span></span> | <span data-ttu-id="8bd0c-115">このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8bd0c-115">This account is used to monitor the availability and health of the environment and provide alerts when necessary.</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: コンフィギュレーション済みのシステム アカウント
description: このトピックでは、Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。
author: laneswenka
ms.date: 11/07/2017
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
ms.openlocfilehash: 1c02a5b8e56c6afd1cca10a5d5aa2370bd5fdd48
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745941"
---
# <a name="preconfigured-system-accounts"></a><span data-ttu-id="5d90e-103">コンフィギュレーション済みのシステム アカウント</span><span class="sxs-lookup"><span data-stu-id="5d90e-103">Preconfigured system accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d90e-104">構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。</span><span class="sxs-lookup"><span data-stu-id="5d90e-104">Pre-configured system accounts are included on deployed environments so that Microsoft can manage and operate the Finance and Operations service and provide specific features to customers.</span></span> <span data-ttu-id="5d90e-105">次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="5d90e-105">The following table provides information about each account, including the purpose and use case for the account.</span></span>  

> [!IMPORTANT] 
> <span data-ttu-id="5d90e-106">システム アカウントを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="5d90e-106">Do not delete these system accounts.</span></span> <span data-ttu-id="5d90e-107">これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。</span><span class="sxs-lookup"><span data-stu-id="5d90e-107">Deleting these accounts will cause a disruption in key functionality provided by Microsoft.</span></span>

| <span data-ttu-id="5d90e-108">口座の詳細</span><span class="sxs-lookup"><span data-stu-id="5d90e-108">Account detail</span></span> | <span data-ttu-id="5d90e-109">アカウントの目的/ユース ケース</span><span class="sxs-lookup"><span data-stu-id="5d90e-109">Purpose/use case of the account</span></span>|
|---|---|
| `Axrunner` | <span data-ttu-id="5d90e-110">このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d90e-110">This account is used to monitor the health of the environment and provide alerts when necessary.</span></span> |
| `FRServiceUser` | <span data-ttu-id="5d90e-111">このアカウントは Financial Reporting のユーザー アカウントで、Management Reporter アプリケーションが  Finance and Operations と統合するために使用します。</span><span class="sxs-lookup"><span data-stu-id="5d90e-111">This account is the Financial Reporting service user account, which is used by the Management Reporter application for integrations with Finance and Operations.</span></span> |
| `RetailServiceAccount` | <span data-ttu-id="5d90e-112">このアカウントは、Retail サービスで Finance and Operations 環境に接続するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d90e-112">This account is used for Retail services to connect to the Finance and Operations environment.</span></span> |
| <span data-ttu-id="5d90e-113">`SysHealthServiceUser` または `Axping` (展開された製品バージョンによって異なる)</span><span class="sxs-lookup"><span data-stu-id="5d90e-113">`SysHealthServiceUser` or `Axping` (depending on the deployed product version)</span></span> | <span data-ttu-id="5d90e-114">このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d90e-114">This account is used to monitor the availability and health of the environment and provide alerts when necessary.</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
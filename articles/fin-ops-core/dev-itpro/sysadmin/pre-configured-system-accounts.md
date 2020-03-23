---
title: コンフィギュレーション済みのシステム アカウント
description: このトピックでは、Finance and Operations 環境で事前設定されているシステム アカウントについて説明します。
author: laneswenka
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2017-11-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: d7d429de1e263f79327ba93d7b8a890e54098b06
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096937"
---
# <a name="preconfigured-system-accounts"></a><span data-ttu-id="cb548-103">コンフィギュレーション済みのシステム アカウント</span><span class="sxs-lookup"><span data-stu-id="cb548-103">Preconfigured system accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb548-104">構成済みのシステム アカウントは、Microsoft が Finance and Operations サービスを管理および運用し、特定の機能をユーザーに提供できるように、配置された環境に含まれます。</span><span class="sxs-lookup"><span data-stu-id="cb548-104">Pre-configured system accounts are included on deployed environments so that Microsoft can manage and operate the Finance and Operations service and provide specific features to customers.</span></span> <span data-ttu-id="cb548-105">次のテーブルは、アカウントの目的とユース ケースを含む、各アカウントに関する情報を示しています。</span><span class="sxs-lookup"><span data-stu-id="cb548-105">The following table provides information about each account, including the purpose and use case for the account.</span></span>  

> [!IMPORTANT] 
> <span data-ttu-id="cb548-106">システム アカウントを削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="cb548-106">Do not delete these system accounts.</span></span> <span data-ttu-id="cb548-107">これらの勘定を削除すると、Microsoft が提供する主要な機能が中断されます。</span><span class="sxs-lookup"><span data-stu-id="cb548-107">Deleting these accounts will cause a disruption in key functionality provided by Microsoft.</span></span>

|                               <span data-ttu-id="cb548-108">口座の詳細</span><span class="sxs-lookup"><span data-stu-id="cb548-108">Account detail</span></span>                               |                                                                    <span data-ttu-id="cb548-109">アカウントの目的/ユース ケース</span><span class="sxs-lookup"><span data-stu-id="cb548-109">Purpose/use case of the account</span></span>                                                                    |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                  <span data-ttu-id="cb548-110">Axrunner</span><span class="sxs-lookup"><span data-stu-id="cb548-110">Axrunner</span></span>                                  |                                   <span data-ttu-id="cb548-111">このアカウントは、環境の稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb548-111">This account is used to monitor the health of the environment and provide alerts when necessary.</span></span>                                    |
|                               <span data-ttu-id="cb548-112">FRServiceUser</span><span class="sxs-lookup"><span data-stu-id="cb548-112">FRServiceUser</span></span>                                | <span data-ttu-id="cb548-113">これは Financial Reporting のユーザー アカウントで、Management Reporter アプリケーションが  Finance and Operations と統合するために使用します。</span><span class="sxs-lookup"><span data-stu-id="cb548-113">This is the Financial Reporting service user account, which is used by the Management Reporter application for integrations with Finance and Operations.</span></span> |
|                            <span data-ttu-id="cb548-114">RetailServiceAccount</span><span class="sxs-lookup"><span data-stu-id="cb548-114">RetailServiceAccount</span></span>                            |                              <span data-ttu-id="cb548-115">このアカウントは、Retail サービスで Finance and Operations 環境に接続するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb548-115">This account is used for Retail services to connect to the Finance and Operations environment.</span></span>                              |
| <span data-ttu-id="cb548-116">SysHealthServiceUser または Axping (展開された製品バージョンによって異なる)</span><span class="sxs-lookup"><span data-stu-id="cb548-116">SysHealthServiceUser or Axping (depending on the deployed product version)</span></span> |                           <span data-ttu-id="cb548-117">このアカウントは、環境の可用性と稼働状態を監視し、必要に応じて警告を提供するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb548-117">This account is used to monitor the availability and health of the environment and provide alerts when necessary.</span></span>                           |


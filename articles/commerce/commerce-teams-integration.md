---
title: Dynamics 365 Commerce と Microsoft Teams データ統合の概要
description: このトピックでは、 Microsoft Dynamics 365 Commerce と Microsoft Teams 統合の概要について説明しています。
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: b9289aca4f53eb2ae8f1fa06d5f80b7ee0bbab8e
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908470"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a><span data-ttu-id="0be34-103">Dynamics 365 Commerce と Microsoft Teams データ統合の概要</span><span class="sxs-lookup"><span data-stu-id="0be34-103">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0be34-104">このトピックでは、 Microsoft Dynamics 365 Commerce と Microsoft Teams 統合の概要について説明しています。</span><span class="sxs-lookup"><span data-stu-id="0be34-104">This topic presents an overview of Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

<span data-ttu-id="0be34-105">Dynamics 365 Commerce は Teams と統合され、顧客とその従業員が2つのアプリケーション間でタスク管理を同期することで生産性を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="0be34-105">Dynamics 365 Commerce is integrating with Teams to help customers and their employees improve productivity by synchronizing task management between the two applications.</span></span> <span data-ttu-id="0be34-106">Commerce とチームの統合によって提供されるシームレスなタスク管理により、店長と従業員はタスク リストを作成し、タスクを複数の店舗に割り当て、どちらのアプリケーションからでも店舗全体のタスクの状態を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="0be34-106">The seamless task management that Commerce and Teams integration provides lets store managers and employees create task lists, assign tasks to multiple stores, and track the status of tasks across stores, from either application.</span></span>

<span data-ttu-id="0be34-107">Commerce と Teams の統合は、Commerce Version 10.0.18 リリース時に利用できます。</span><span class="sxs-lookup"><span data-stu-id="0be34-107">Commerce and Teams integration is available as of the Commerce version 10.0.18 release.</span></span>

## <a name="key-features"></a><span data-ttu-id="0be34-108">主な機能</span><span class="sxs-lookup"><span data-stu-id="0be34-108">Key features</span></span>

<span data-ttu-id="0be34-109">ここでは、Commerce と Microsoft Teams の統合により実現する主な機能をご紹介します :</span><span class="sxs-lookup"><span data-stu-id="0be34-109">Here are some of the key features that the Commerce and Microsoft Teams integration provides:</span></span>

- <span data-ttu-id="0be34-110">店舗、作業者、アクセス許可、ビジネス コンテキストに関する組織構造や情報など、Commerce から得られる定義済の情報を活用して、Teams を提供します。</span><span class="sxs-lookup"><span data-stu-id="0be34-110">Provision Teams by taking advantage of well-defined information from Commerce, such as the organizational structure and information about stores, workers, permissions, and business context.</span></span>
- <span data-ttu-id="0be34-111">Commerce と Teams の間で進行中の変更 (新しい店舗の追加や新しい従業員の採用など) を容易に同期しますが、Commerce は組織構造データのマスター ソースとして維持します。</span><span class="sxs-lookup"><span data-stu-id="0be34-111">Easily synchronize ongoing changes (for example, the addition of new stores or hiring of new employees) between Commerce and Teams, but keep Commerce as the master source of organizational structure data.</span></span>
- <span data-ttu-id="0be34-112">作業員、店長、地域マネージャ、通信マネージャがどちらのアプリケーションからのタスク管理を処理するか支援するために、Commerce と Teams 間でタスク管理を統合します。</span><span class="sxs-lookup"><span data-stu-id="0be34-112">Integrate task management between Commerce and Teams to help store workers, store managers, regional managers, and communications managers handle task management from either application.</span></span>

## <a name="prerequisites-for-using-integration-features"></a><span data-ttu-id="0be34-113">統合機能を使用するための前提条件</span><span class="sxs-lookup"><span data-stu-id="0be34-113">Prerequisites for using integration features</span></span>

<span data-ttu-id="0be34-114">Microsoft Teams の統合機能を使い始める前に、以下の前提条件が満たされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0be34-114">The following prerequisites must be in place before you can start to use Microsoft Teams integration features:</span></span>

- <span data-ttu-id="0be34-115">Microsoft 365 Business Standard ライセンス (このライセンスには Teams が含まれています。)</span><span class="sxs-lookup"><span data-stu-id="0be34-115">Microsoft 365 Business Standard License (This license includes Teams.)</span></span>
- <span data-ttu-id="0be34-116">Azure Active Directory( Azure AD) すべての店長と従業員のアカウント</span><span class="sxs-lookup"><span data-stu-id="0be34-116">Azure Active Directory (Azure AD) accounts for all store managers and workers</span></span>
- <span data-ttu-id="0be34-117">Azure AD の認証が設定されている販売時点管理 (POS) システム</span><span class="sxs-lookup"><span data-stu-id="0be34-117">Point of sale (POS) systems that are configured with Azure AD authentication</span></span>

## <a name="conceptual-architecture"></a><span data-ttu-id="0be34-118">概念に関するアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="0be34-118">Conceptual architecture</span></span>

<span data-ttu-id="0be34-119">次の図は、サンフランシスコの店舗を例に、Dynamics 365 Commerce と Microsoft Teams の統合の概念的なアーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="0be34-119">The following illustration shows the conceptual architecture of Dynamics 365 Commerce and Microsoft Teams integration, using a San Francisco store as an example.</span></span> <span data-ttu-id="0be34-120">Teams と Commerce POS アプリケーションは、Microsoft Planner をリポジトリとして使用しているため、Teams から発行されたタスクは POS アプリケーションに表示され、POS アプリケーションで店長が作成したアドホック タスクは Teams に表示されるなど、アプリケーション間でシームレスなタスク管理が可能です。</span><span class="sxs-lookup"><span data-stu-id="0be34-120">Both Teams and the Commerce POS application use Microsoft Planner as a repository so that tasks published from Teams appear in the POS application and ad hoc tasks created by store managers in the POS application appear in Teams, resulting in a seamless task management experience between the applications.</span></span>    

![Commerce と Teams の統合のアーキテクチャ](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="0be34-122">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0be34-122">Additional resources</span></span>

[<span data-ttu-id="0be34-123">Dynamics 365 Commerce と Microsoft Teams の統合を有効化する</span><span class="sxs-lookup"><span data-stu-id="0be34-123">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="0be34-124">Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="0be34-124">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="0be34-125">Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる</span><span class="sxs-lookup"><span data-stu-id="0be34-125">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="0be34-126">Microsoft Teams でユーザーとロールを管理する</span><span class="sxs-lookup"><span data-stu-id="0be34-126">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="0be34-127">Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします</span><span class="sxs-lookup"><span data-stu-id="0be34-127">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="0be34-128">Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ</span><span class="sxs-lookup"><span data-stu-id="0be34-128">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)

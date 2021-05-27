---
title: Dynamics 365 Commerce と Microsoft Teams データ統合の概要
description: このトピックでは、 Microsoft Dynamics 365 Commerce と Microsoft Teams 統合の概要について説明しています。
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c22af9bf76818dd682b4147c3677cd1715e4cbf8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021992"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-overview"></a>Dynamics 365 Commerce と Microsoft Teams データ統合の概要

[!include [banner](includes/banner.md)]

このトピックでは、 Microsoft Dynamics 365 Commerce と Microsoft Teams 統合の概要について説明しています。

Dynamics 365 Commerce は Teams と統合され、顧客とその従業員が2つのアプリケーション間でタスク管理を同期することで生産性を向上させることができます。 Commerce とチームの統合によって提供されるシームレスなタスク管理により、店長と従業員はタスク リストを作成し、タスクを複数の店舗に割り当て、どちらのアプリケーションからでも店舗全体のタスクの状態を追跡できます。

Commerce と Teams の統合は、Commerce Version 10.0.18 リリース時に利用できます。

## <a name="key-features"></a>主な機能

ここでは、Commerce と Microsoft Teams の統合により実現する主な機能をご紹介します :

- 店舗、作業者、アクセス許可、ビジネス コンテキストに関する組織構造や情報など、Commerce から得られる定義済の情報を活用して、Teams を提供します。
- Commerce と Teams の間で進行中の変更 (新しい店舗の追加や新しい従業員の採用など) を容易に同期しますが、Commerce は組織構造データのマスター ソースとして維持します。
- 作業員、店長、地域マネージャ、通信マネージャがどちらのアプリケーションからのタスク管理を処理するか支援するために、Commerce と Teams 間でタスク管理を統合します。

## <a name="prerequisites-for-using-integration-features"></a>統合機能を使用するための前提条件

Microsoft Teams の統合機能を使い始める前に、以下の前提条件が満たされている必要があります。

- Microsoft 365 Business Standard ライセンス (このライセンスには Teams が含まれています。)
- Azure Active Directory( Azure AD) すべての店長と従業員のアカウント
- Azure AD の認証が設定されている販売時点管理 (POS) システム

## <a name="conceptual-architecture"></a>概念に関するアーキテクチャ

次の図は、サンフランシスコの店舗を例に、Dynamics 365 Commerce と Microsoft Teams の統合の概念的なアーキテクチャを示しています。 Teams と Commerce POS アプリケーションは、Microsoft Planner をリポジトリとして使用しているため、Teams から発行されたタスクは POS アプリケーションに表示され、POS アプリケーションで店長が作成したアドホック タスクは Teams に表示されるなど、アプリケーション間でシームレスなタスク管理が可能です。    

![Commerce と Teams の統合のアーキテクチャ](media/d365-commerce-teams-integration-conceptual-architecture.png)

## <a name="additional-resources"></a>追加リソース

[Dynamics 365 Commerce と Microsoft Teams の統合を有効化する](enable-teams-integration.md)

[Dynamics 365 Commerce から Microsoft Teams へのプロビジョニング](provision-teams-from-commerce.md)

[Microsoft Teams と Dynamics 365 Commerce の POS 間でタスク管理を同期させる](synchronize-tasks-teams-pos.md)

[Microsoft Teams でユーザーとロールを管理する](manage-user-roles-teams.md)

[Microsoft Teams に既存のチームがある場合は、店舗とチームをマッピングします](map-stores-existing-teams.md)

[Dynamics 365 Commerce と Microsoft Teams の統合に関する FAQ](teams-integration-faq.md)

---
title: 原価オブジェクト コントローラーのアクセス権の定義
description: このトピックでは、原価オブジェクト コント ローラーのアクセス権に関する情報を提供します。
author: AndersGirke
manager: AnnBe
ms.date: 06/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostControlWorkspace, CAMParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 290b16eeb99ac7ddb9b552b289215c99a0451660
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565912"
---
# <a name="access-rights-of-a-cost-object-controller"></a>原価オブジェクト コントローラーのアクセス権

[!include [banner](../includes/banner.md)]

**原価管理**ワークスペースは、マネージャーが原価オブジェクトのパフォーマンスを表示できる中心点です。 このワークスペースでは、マネージャーが原価経理担当者でない場合でも原価会計データを使用できます。 セキュリティ上の理由から、マネージャは自分が担当する特定の原価オブジェクトに関連付けられている原価計算データのみの参照が許可されます。

原価計算には、次の 4 つの固有のロールがあります。

| ロール名               | ライセンス      |
|-------------------------|--------------|
| 原価会計マネージャー | 活動     |
| 原価経理担当         | Operations   |
| 原価経理担当係   | Operations   |
| 原価オブジェクト コントローラー  | チーム メンバー |

ここでは**原価オブジェクト コントローラー** ロールをマネージャーに割り当てる方法について説明します

**原価オブジェクト コントローラー** ロールがマネージャーに割り当てられると、マネージャーは次の作業を実行できます。

- **原価管理**ワークスペースにアクセス (クライアントで)。

    - ドリルスルー経験をサポートするページへのドリルスルーおよび表示アクセス。

- **原価管理**ワークスペースにアクセス (モバイル アプリケーションで)。

> [!NOTE]
> **原価オブジェクト コントローラー**ロールは、ユーザーがどの原価オブジェクトへのアクセスや表示ができるかを制御しません。 行レベル セキュリティは、分析コード階層とアクセス リスト階層によって提供されます。

## <a name="grant-access-rights"></a>アクセス権の付与
次の例は、分析コード階層がどのように見えるかを示します。

**分析コード階層の詳細**

| 分析コード階層名 | 分析コード    | 分析コード階層タイプ名      | アクセス リスト階層 |
|--------------------------|--------------|------------------------------------|-----------------------|
| 組織             | コスト センター | 分析コード分類階層 | **有**               |

階層デザイナーの**ユーザー**クイック タブで、各ノードに 1 つまたは複数のユーザー ID を挿入できます。

|                                   | ユーザー            | 分析コード メンバーの範囲   |                         |
|-----------------------------------|------------------|---------------------------|-------------------------|
| **ノード**                         | **ユーザー ID**      | **移動元分析コード メンバー** | **移動先分析コード メンバー** |
| 組織                      | ベンジャミン、クレア |                           |                         |
| &nbsp;&nbsp;管理者                 | 4 月            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;財務   | アリシア           | CC002                     | CC003                   |
|                                   |                  | CC007                     | CC007                   |
| &nbsp;&nbsp;&nbsp;&nbsp;HR        | アーニー            | CC001                     | CC001                   |
| &nbsp;&nbsp;生産            | デビッド            |                           |                         |
| &nbsp;&nbsp;&nbsp;&nbsp;梱包業 | エレン            | CC005                     | CC005                   |
| &nbsp;&nbsp;&nbsp;&nbsp;組み立て  | クリス            | CC006                     | CC006                   |

> [!NOTE]
> 原価計算のすべてのエントリを表示できるように、原価経理担当者は階層の最上部に割り当てられる必要があります。

アクセス リスト階層およびセキュリティ設定を適用する前に、**原価会計パラメーター**ページの**一般**タブにある**原価オブジェクト分析コード メンバーに対する表示アクセスの有効化**オプションを**はい**に設定する必要があります (**原価会計** > **設定** > **パラメータ**)。

アクセス リスト階層の設定は、次の領域に表示されるデータを制御するために使用されます。

- **原価管理**ワークスペース (クライアント内):

    - ドリルスルーに使用されるページのデータ

- **原価管理**ワークスペース (モバイル アプリケーション内):

    - カードの残高

- Microsoft Power BI:

    - Power BI ビジュアル化に表示されるデータ
    - Microsoft Dynamics 365 for Finance and Operations クライアントに埋め込まれた Power BI ビジュアル化データ

> [!IMPORTANT]
> - アクセス リスト階層が Power BI のデータに影響を及ぼす前に、アクセス リスト階層と Power BI の行レベルのセキュリティがペアリングされる必要があります。 詳細については、「[原価会計コンテンツ パックのセキュリティ設定](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)」を参照してください。
> - このトピックでは、**原価管理**ワークスペースを使用するための前提条件を説明します。

その他のリソース

- [原価管理ワークスペース](cost-control-workspace.md)
- [分析コード階層](dimension-hierarchy.md)
- [原価会計コンテンツ パックのセキュリティ設定](../../dev-itpro/analytics/setup-security-cost-accounting-content-pack.md)

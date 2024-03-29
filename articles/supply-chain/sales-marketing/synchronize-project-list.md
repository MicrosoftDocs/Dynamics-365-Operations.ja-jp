---
title: Supply Chain Management から Field Service へのプロジェクト リストの同期
description: この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 71c0580953f01c2d29e99fa2928a0b4a3937d5c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899356"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Supply Chain Management から Field Service へのプロジェクト リストの同期

[!include[banner](../includes/banner.md)]

この記事では、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。

[![Supply Chain Management および Field Service 間の業務プロセスの同期。](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク
次のテンプレートと基本的なタスクは、Supply Chain Management から Field Service にプロジェクトの同期を実行するために使用されます。

**データ統合でのテンプレート**
- プロジェクト (Supply Chain Management から Field Service)

**データ統合プロジェクトのタスク**
- プロジェクト

プロジェクト リストの同期が処理される前に、次の同期タスクが必要です。
- アカウント (Sales から Supply Chain Management) 

## <a name="entity-set"></a>エンティティ セット
| Field Service           | サプライ チェーン マネジメント  |
|-------------------------|-------------------------|
|msdynce_externalprojects | プロジェクト                |

## <a name="entity-flow"></a>エンティティのフロー
プロジェクトは Supply Chain Management で作成されます。 **プロジェクト タイプ** を **時間、原材料** に、および **プロジェクト ステージ** を **処理中** に設定されたプロジェクトは、プロジェクト番号、プロジェクト名、プロジェクト ステージおよび顧客口座情報を含め、Field Service の **外部プロジェクト** エンティティに同期されます。 **外部プロジェクト** のリストは、Field Service のワーク オーダーと Supply Chain Management のプロジェクトをペアリングするために使用されます。

## <a name="field-service-crm-solution"></a>Field Service CRM ソリューション
**外部プロジェクト** エンティティは、Supply Chain Management からすべてのプロジェクトを取得します。 **外部プロジェクト** フィールドが、**ワーク オーダー** エンティティに追加されました。 これはルックアップ フィールドであるため、ワーク オーダーがプロジェクトにタグ付けられ、販売注文は Supply Chain Management によりプロジェクトに関連付けられます。 **システム ステータス** が **オープン – 処理中 (690,970,000)** から上位のステータスへ変更した後、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定
### <a name="supply-chain-management"></a>サプライ チェーン マネジメント
データ エンティティ プロジェクトの変更追跡を有効にします。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング


### <a name="projects-supply-chain-management-to-field-service-projects"></a>プロジェクト (Supply Chain Management から Field Service): プロジェクト

[![データ統合のテンプレートのマッピング。](./media/FSProject1.png)](./media/FSProject1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
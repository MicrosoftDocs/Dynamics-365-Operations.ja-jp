---
title: "Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合"
description: "このトピックでは、Talent と Finance and Operations の統合について説明します。"
author: jcart
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: 
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2018-10-8
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: ab6f4393cfc83aa9ab39dd3759a590fa4b5301b4
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="integration-from-dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations"></a>Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合

[!include[banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Talent と Dynamics 365 for Finance and Operations の統合のために使用できる機能について説明します。 [データ インテグレーター](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)と共に使用可能な Talent から Finance and Operations へのテンプレートにより、ジョブ、職位、および作業者のデータのフローが可能になります。 Talent から Finance and Operations へのデータ フロー。 テンプレートでは、Finance and Operations から Talent にデータを戻す機能は提供されません。 

![Talent のから Finance and Operations への統合フロー](./media/TalentFinOpsFlow.png)

Talent から Finance and Operations へのソリューションは、次のタイプのデータ同期を提供します。 

- Talent のジョブを管理し、Talent から Finance and Operations に同期します。
- Talent の職位と職位の割り当てを管理し、Talent から Finance and Operations に同期します。
- Talent の雇用を管理し、Talent から Finance and Operations に同期します。
- Talent の作業者と作業者住所を管理し、Talent から Finance and Operations に同期します。

## <a name="system-requirements-for-talent"></a>Talent のシステム要件
統合ソリューションには、次のバージョンの Talent および Finance and Operations アプリケーションが必要です。 
- CDS for Apps の Dynamics 365 for Talent。
- Dynamics 365 for Finance and Operations バージョン 7.2 以降。

## <a name="template-and-tasks"></a>テンプレートおよびタスク

テンプレートにアクセスするには、次の操作を行います。
1. [PowerApps 管理センター](https://admin.powerapps.com/)を開きます。 
1. **プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。 新しいプロジェクトは、Finance and Operations に統合する法人ごとに作成する必要があります。

Talent から Finance and Operations にレコードを同期するには、次のテンプレートを使用します。

- **データ統合でのテンプレートの名前:** Core HR (Talent CDS から Fin and Ops)

  > [!NOTE]
  > タスクの名前には、各アプリケーションで使用されるエンティティが含まれています。 ソース (Talent) は左にあり、ターゲット (Finance and Operations) は右にあります。

Talent から Finance and Operations にレコードを同期するには、次の基になるタスクを使用します。
- 職務権限から報酬職務権限。
- 部門から作業単位
- 部門から作業単位
- ジョブ タイプから報酬ジョブ タイプ
- ジョブからジョブ
- ジョブからジョブ詳細
- 職位タイプから職位タイプ
- ジョブ職位から職位
- ジョブ職位から職位親ジョブ割り当て
- 作業者から作業者
- 雇用から雇用
- 雇用から雇用詳細
- 職位作業者割り当てから職位作業者割り当て
- 作業者住所から作業者の住所 V2

## <a name="integration-considerations"></a>統合に関する考慮事項
Talent から Finance and Operations にデータを統合する場合は、統合が ID に基づいてレコードを一致させようとします。 一致が発生した場合、Finance and Operations のデータは、Talent の値で上書きされます。 ただし、論理的にさまざまなレコードが存在し、Talent または Finance and Operations のいずれかでそれぞれの番号順序に基づいて同一の ID が生成された場合に、問題が発生する場合があります。

これが発生する領域は、従業員番号を使用して一致が作成される作業者と、職位です。 ジョブは、番号順序を使用しません。その結果、同一のジョブ ID が Talent と Finance and Operations の両方で存在する場合は、Talent 情報により Finance and Operations 情報が上書きされます。 

重複する ID の問題を防ぐには、[番号順序](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json)に接頭語を追加するか、その他のシステムの範囲を超えている番号順序の開始番号を設定します。 

番号順序に含まれていない作業者住所に使用される場所 ID。 Talent から Finance and Operations に作業者住所を統合するとき、Finance and Operations に作業者の住所が既に存在する場合は、重複する住所レコードが作成される場合があります。 

次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。 

![テンプレートのマッピング](./media/IntegrationMapping.png)






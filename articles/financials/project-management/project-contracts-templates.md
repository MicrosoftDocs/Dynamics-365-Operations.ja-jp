---
title: "Project Service Automation からプロジェクト契約をプロジェクト契約に直接同期する Finance and Operations"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト契約およびプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 8d8e3268ae8c612bad87c3c6416f223219149ee6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-contracts-and-projects-from-project-service-automation-directly-to-project-contracts-and-projects-in-finance-and-operations"></a>Project Service Automation からプロジェクト契約とプロジェクトを、プロジェクト契約およびプロジェクトの Finance and Operations に直接同期します。

このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations へプロジェクト契約およびプロジェクトを、直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。

> [!NOTE] 
> Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4074835 をインストールする必要があります。

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Project Service Automation から Finance and Operations のデータ フロー

> [!NOTE]
> Project Service Automation から Finance and Operations の統合ソリューションを使用する前に、Dynamics 365 データ統合機能についてよく理解しておく必要があります。

Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。 データ統合機能で利用できる統合テンプレートは、Project Service Automation から Finance and Operations へのプロジェクト契約、プロジェクト、プロジェクト契約明細行、およびプロジェクト契約明細行のマイルストーンのデータのフローを有効にします。

次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。

[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>テンプレートおよびタスク

使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。

次のテンプレートおよび基本的なタスクは Project Service Automation から Finance and Operations へプロジェクト契約とプロジェクトを同期させるために使用されます。

- **データ統合でのテンプレートの名前:** プロジェクトおよび契約 (Project Service Automation から Finance and Operations)
- **プロジェクトのタスク名:**

  - プロジェクト契約は Project Service Automation から Finance and Operations
  - プロジェクトは Project Service Automation から Finance and Operations
  - プロジェクト契約明細行は Project Service Automation から Finance and Operations
  - プロジェクト契約明細行のマイルストーンは Project Service Automation から Finance and Operations

プロジェクト契約とプロジェクトの同期を行う前に、勘定を同期する必要があります。

## <a name="entity-set"></a>エンティティ セット

| Project Service Automation       | Finance and Operations                                 |
|----------------------------------|--------------------------------------------------------|
| 注文                           | プロジェクト契約の統合エンティティ。                |
| プロジェクト                         | プロジェクトの統合エンティティ。                         |
| 注文明細行                      | プロジェクト契約明細行の統合エンティティ。          |
| プロジェクト契約明細行のマイルストーン | プロジェクト契約明細行のマイルストーンの統合エンティティ。 |

## <a name="entity-flow"></a>エンティティのフロー

プロジェクト契約は Project Service Automation で管理され、プロジェクト契約として Finance and Operations に同期されます。 統合テンプレートの一部として、プロジェクト契約の Finance and Operations で統合ソースを設定することができます。

時間、実費払い、固定価格プロジェクトは Project Service Automation で管理され、プロジェクトとして Finance and Operations に同期されます。 テンプレート統合の一部として、プロジェクトの Finance and Operations で統合ソースを設定することができます。

プロジェクト契約明細行は Project Service Automation で管理され、プロジェクト契約の請求ルールとして Finance and Operations に同期されます。 請求方法が既定のプロジェクト タイプと異なる場合、契約明細行プロジェクトおよびプロジェクト グループのプロジェクト タイプは同期し更新されます。

プロジェクト契約明細行のマイルストーンは Project Service Automation で管理され、プロジェクト契約の請求ルールのマイルストーンとして Finance and Operations に同期されます。

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a>Finance and Operations 統合ソリューションと Project Service Automation

**プロジェクト契約 ID** フィールドは**プロジェクト契約**ページで使用できます。 このフィールドは統合をサポートするための自然で固有のキーとなっています。

新しいプロジェクト契約が作成され、**プロジェクト契約 ID** 値が存在しない場合、番号順序を使用して自動的に生成されます。 値は **ORD** で構成され、インクリメント番号順序、次に 6 文字の接尾語が続きます。 次に例を示します: **ORD-01022-Z4M9Q0**。

**プロジェクト番号**フィールドは、**プロジェクト** ページで使用できます。 このフィールドは統合をサポートするための自然で固有のキーとなっています。

新しいプロジェクトが作成され、**プロジェクト番号**値が存在しない場合、番号順序を使用して自動的に生成されます。 値は **PRJ** で構成され、インクリメント番号順序、次に 6 文字の接尾語が続きます。 次に例を示します: **PRJ-01049-CCNID0**。

Project Service Automation から Finance and Operations 統合ソリューションを適用した場合<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>、アップグレード スクリプトは既存のプロジェクト契約の**プロジェクト契約 ID** フィールドおよび Project Service Automation の既存のプロジェクトの**プロジェクト番号**フィールドを設定します。

## <a name="prerequisites-and-mapping-setup"></a>前提条件およびマッピングの設定

- プロジェクト契約とプロジェクトの同期を行う前に、勘定を同期する必要があります。
- 接続の設定、**msdyn\_organizationalunits** の統合キー フィールドのマッピングを **msdyn\_名前\[名前\]** へ追加します。 まず最初に、接続の設定にプロジェクトを追加する必要があります。 統合キーの詳細情報については、Dynamics 365 データ統合を参照してください。
- 接続の設定、**msdyn\_プロジェクト**の統合キー フィールドのマッピングを **msdynce\_projectnumber \[プロジェクト番号\]** へ追加します。 まず最初に、接続の設定にプロジェクトを追加する必要があります。 統合キーの詳細情報については、Dynamics 365 データ統合を参照してください。
- **SourceDataID** のプロジェクト契約およびプロジェクトは異なる値に更新、またはマッピングから削除することができます。 既定のテンプレート値は **Project Service Automation** です。
- **PaymentTerms** マッピングは、Finance and Operations で有効な支払条件が反映できるように更新する必要があります。 プロジェクト タスクからマッピングを削除することもできます。 既定値のマップにはデモ データの既定値があります。 次のテーブルでは、Project Service Automation の値を示します。

    | 先頭値 | 説明   |
    |-------|---------------|
    | 1     | 正味 30        |
    | 2     | 2%10, 正味 30 |
    | 3     | 正味 45        |
    | 4     | 正味 60        |

## <a name="power-query"></a>Power Query
次の条件が満たされた場合、フィルター処理する Microsoft Power Query を使用する必要があります。

- Microsoft Dynamics 365 for Sales の販売注文があります。
- Project Service Automation に複数の組織単位があり、これらの組織単位は Finance and Operations の複数の法人にマップされます。

Power Query を使用する必要がある場合は、これらのガイドラインに従います。

- プロジェクト契約 (Project Service Automation から Finance and Operations) テンプレートは**作業項目 (msdyn\_ordertype = 192350001)** タイプの販売注文のみを含む既定のフィルターです。 このフィルターでは、Finance and Operations での販売注文のプロジェクト契約が作成されていないことを保証します。 独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。
- 統合接続セットの法人に同期させる必要がある契約組織のみを含む Power Query フィルターを作成する必要があります。 Contoso 米国の契約組織単位とプロジェクト契約した USSI 法人に同期させる必要がありますが、Contoso グローバルの契約組織単位であるプロジェクト契約は USMF 法人に同期させる必要があります。 このフィルターをタスクのマッピングに追加しない場合、すべてのプロジェクト契約は契約組織単位に関係なく、接続セットに対して定義されている法人に同期されます。

## <a name="template-mapping-in-data-integration"></a>データ統合のテンプレートのマッピング

> [!NOTE] 
> **CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState**、および **AddressZipCode** フィールドは、プロジェクト契約の既定のマッピングに含まれません。 プロジェクト契約のこのデータを同期することが必要な場合に、マッピングを追加することができます。
> **説明**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber**、および **ProjectType** フィールドは、プロジェクトの既定のマッピングに含まれていません。 プロジェクトのこのデータを同期することが必要な場合に、マッピングを追加することができます。

次の図は、データ インテグレーターのタスク マッピングの例を示します。 マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。

[![テンプレートのマッピング](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![テンプレートのマッピング](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![テンプレートのマッピング](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![テンプレートのマッピング](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)


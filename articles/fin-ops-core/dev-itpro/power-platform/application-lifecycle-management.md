---
title: 仮想エンティティを使用するソリューションのアプリケーション ライフサイクル管理
description: このトピックでは、Finance and Operations の仮想エンティティを使用するソリューションのアプリケーション ライフサイクルについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: b36321386473efdcc9549c7b777a0bf051128785
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621418"
---
# <a name="application-lifecycle-management-for-solutions-that-use-virtual-entities"></a>仮想エンティティを使用するソリューションのアプリケーション ライフサイクル管理

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> この機能を使用するには、Finance and Operations アプリのバージョン 10.0.12 が必要ですが、Common Data Service にはサービス更新 189 が必要です。 Common Data Service のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

Finance and Operations 仮想エンティティを使用するエンド ツー エンド ソリューションのアプリケーション ライフサイクルには、Finance and Operations および Common Data Service の両方が含まれます。 詳細については、このトピックで説明します。

## <a name="solution-management"></a>ソリューション管理

Finance and Operations の仮想エンティティは、作成されるまで Common Data Service には存在しません。 仮想エンティティは、ソリューション内に作成する必要があります。 MicrosoftOperationsERPVE ソリューションは、この目的に使用されます。 このソリューションには、Finance and Operations のインスタンスから作成されたすべての仮想エンティティが含まれます。

MicrosoftOperationsERPVE は、[マネージド ソリューション](https://docs.microsoft.com/powerapps/developer/common-data-service/introduction-solutions)です。 定義上、マネージド ソリューションを生成した後で変更することはできません。 ただし、MicrosoftOperationsERPVE は、その中に含まれるコンポーネント (仮想エンティティ) を更新する特権を付与するマネージド ソリューションです。 したがって、新しい仮想エンティティを作成時にソリューションに追加したり、既存の仮想エンティティを必要に応じて更新したりできます。 ただし、マネージド ソリューションを変更する特権は、プラットフォーム自体に対してのみ使用できます。 ユーザーは直接ソリューションに変更を加えることはできません。

MicrosoftOperationsERPVE はマネージド ソリューションであるため、顧客、パートナー、および独立系ソフトウェアベンダー (ISV) によるソリューションは、それに対する依存関係を持つことになります。 この機能により、Finance and Operations の仮想エンティティを使用したり依存したりするソリューションに一貫したアプリケーション ライフサイクル管理 (ALM) が可能になります。

MicrosoftOperationsERPVE に依存するソリューションがエクスポートされると、ソリューションで使用される仮想エンティティのプレースホルダーがエクスポートされたソリューションに追加されます。 このソリューションを別の Common Data Service 環境にインポートすると、インポート プロセスによって、Common Data Service 環境に関連付けられている Finance and Operations インスタンスの MicrosoftOperationsERPVE ソリューションの依存 Finance and Operations 仮想エンティティが生成されます。 したがって、MicrosoftOperationsERPVE は、それに依存するソリューションをインポートする前に、既に存在している必要があります。 同じ日付を入力すると、エラー メッセージが表示されます。 また、依存エンティティが Finance and Operations インスタンスで使用できない場合は、そのエンティティの仮想エンティティは生成されません。 仮想エンティティは、使用可能なエンティティに対してのみ生成されます。

次の一覧は、Finance and Operations 仮想エンティティの動作を必要とし、Common Data Service 環境で使用できるようにする必要があるその他のソリューションを示しています。

- **MicrosoftOperationsERPCatalog**: このソリューションは、Finance and Operations インスタンスで利用可能なエンティティのカタログを提供します。 また、コンフィギュレーションの設定に使用される接続も提供されます。 詳細については、このトピックの後のセクションを参照してください。
- **MicrosoftOperationsVESupport**: このソリューションにより、Finance and Operations アプリの仮想エンティティ プロバイダーが提供されます。 プロバイダーは、Finance and Operations アプリおよび Common Data Service と通信できます。 詳細については、次のセクションを参照してください。
- **Dynamics365Company**: このソリューションは、**PrimaryCompanyContext** メタデータ値を持つすべての Finance and Operations エンティティによって参照される会社エンティティを追加します。

これらのソリューションはすべて、環境内に存在する必要があります。 それ以外の場合、仮想エンティティは Finance and Operations アプリでは使用できません。 これらのソリューションは、環境全体でのより容易な移植性を実現するためにパッケージ化されています。

## <a name="managing-entities-from-multiple-environments"></a>複数の環境からのエンティティの管理

MicrosoftOperationsVESupport ソリューションは、**msdyn\_financeandoperationsvirtualentity** エンティティで構成されます。 このエンティティは、接続の設定情報をキャプチャする Finance and Operations の仮想エンティティ データ ソースを表します。 このエンティティの各レコードは、Finance and Operations インスタンスへの接続を表します。

カタログを使用して、Common Data Service の仮想化に使用できる Finance and Operations インスタンス内のすべてのエンティティを一覧表示します (つまり、Open Data Protocol (\[OData\]) に対して有効になっている Finance and Operations のエンティティがすべて表示されます)。 カタログは、既定の MicrosoftOperationsERPCatalog ソリューションの一部であり、Finance and Operations インスタンスに適用できます。

各 Common Data Service 環境が常に 1 つの Finance and Operations インスタンスをポイントしている必要があり、各 Finance and Operations 環境は 1 つの Common Data Service 環境のみをポイントする必要があります。 したがって、**msdyn\_financeandoperationsvirtualentity** エンティティに含まれるレコードは 1 つだけにする必要があります。

カタログを表す **mserp\_financeandoperationsentity** エンティティは、Finance and Operations インスタンス内のエンティティを一覧表示するように照会できます。 このエンティティは仮想エンティティなので、Common Data Service にはカタログは保存されません。

カタログ エンティティの名前の先頭に接頭辞 "mserp\_" が付いていることに注意してください。 この接頭辞は、カタログ内のエンティティを Finance and Operations エンティティとして識別します。 MicrosoftOperationsERPVE ソリューションで Finance and Operations に生成される仮想エンティティのシステム名にも同じ接頭語が追加されます。 したがって、作成者は他のエンティティと Finance and Operations 仮想エンティティを区別することができます。 接頭辞はマネージド ソリューションで設定され、変更することはできません。

### <a name="managing-entities-from-multiple-isv-solutions"></a>複数の ISV ソリューションからのエンティティの管理

1 つ以上の ISV ソリューションが、Finance and Operations の仮想エンティティを使用する MicrosoftOperationsERPVE ソリューションへの依存関係を取得します。 Finance and Operations のユーザー定義エンティティは、Finance and Operations の標準のエンティティと同じカタログを使用するため、MicrosoftOperationsERPVE ソリューションでもカスタム Finance and Operations エンティティの仮想エンティティが生成されます。

Finance and Operations でエンティティの開発に対して確立されたガイドラインと ALM により、ISV ソリューション間に競合するエンティティ名がないことが保証されます。 したがって、複数の ISV ソリューションからカスタム Finance and Operations エンティティに対して Common Data Service で仮想エンティティが生成される場合、このタイプの競合は発生しません。 ユーザー定義エンティティを含む Finance and Operations エンティティのすべての仮想エンティティには、前に説明した "mserp\_" プレフィックスが付けられます。

### <a name="managing-a-finance-and-operation-instance-in-a-common-data-service-environment-for-virtual-entities"></a>仮想エンティティの Common Data Service 環境における Finance and Operation インスタンスの管理 

仮想エンティティの Common Data Service 環境には、1 つの Finance and Operations インスタンスをリンクする必要があります。 必要な接続設定情報は、Finance and Operations の仮想エンティティ データ ソースでキャプチャされます。 このデー タソースは、MicrosoftOperationsERPCatalog ソリューションに含まれています。

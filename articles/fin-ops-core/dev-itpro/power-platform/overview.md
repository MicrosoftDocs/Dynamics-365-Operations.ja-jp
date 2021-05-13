---
title: Finance and Operations と Microsoft Power Platform の統合
description: このトピックでは Finance and Operations および Microsoft Dataverse の Lifecycle Services を介して Power Platform の統合の概要を提供します。
author: Sunil-Garg
ms.date: 04/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 9b8d5a5703a42c3788cabfd051a7633bc849ec05
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908688"
---
# <a name="microsoft-power-platform-integration-with-finance-and-operations"></a>Finance and Operations と Microsoft Power Platform の統合

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> この機能を使用するには、Finance and Operations アプリのバージョン 10.0.12 が必要ですが、Dataverse にはサービス更新 189 が必要です。 Dataverse のリリース情報は、[最新バージョンの利用可能性](/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

Microsoft Power Platform は、Power Platform 管理者センターを介した Dynamics 365 アプリケーションの一連の機能を提供します。 現在、Finance and Operations アプリは Power Platform 管理センターによって管理されませんが、時間の経過とともに、Lifecycle Services (LCS) から管理センターに移行される管理機能がますます増えています。 暫定的に、顧客は、LCS の Power Platform 統合機能を介して、二重書き込み機能、仮想エンティティ、アドインなどの機能のロックを解除できるようになります。

このトピックでは、Power Platform 統合によってロックが解除されたさまざまな機能の概要と、設定手順の実行方法を提供します。

## <a name="prerequisite-reading"></a>前提条件の参照先

Power Platform, Microsoft Dataverse のアーキテクチャと Finance and Operations アプリの仮想エンティティを理解するには、それらのしくみを理解しておく必要があります。 したがって、次のドキュメントが前提条件になります。

- [Power Platform の管理](/power-platform/admin/admin-documentation)
- [Dataverse とは](/powerapps/maker/common-data-service/data-platform-intro)
- [エンティティ概要](/powerapps/maker/common-data-service/entity-overview)
- [エンティティの関連付けの概要](/powerapps/maker/common-data-service/relationships-overview)
- [外部データ ソースのデータを含む仮想エンティティの作成と編集](/powerapps/maker/common-data-service/create-edit-virtual-entities)
- [Power Apps ポータルについて](/powerapps/maker/portals/overview)
- [Power Apps でのアプリの作成の概要](/powerapps/maker/)

## <a name="tools-and-services-unlocked-with-power-platform-integration"></a>Power Platform 統合によってロックが解除されたツールとサービス
以下は、環境に Power Platform 統合を設定することでロックが解除されるさまざまなツールとサービスの一覧です。

### <a name="virtual-entities-for-finance-and-operations-apps"></a>Finance and Operations アプリの仮想エンティティ

Finance and Operations アプリは、Dataverse の仮想データ ソースであり、Dataverse および Microsoft Power Platform からの完全な作成、読み取り、更新、削除 (CRUD) 操作を可能にし ます。 定義上、仮想エンティティのデータは、Dataverse には存在しません。 その代わりに、データは属しているアプリケーションで引き続き存在します。 Dataverse から Finance and Operations エンティティに対して CRUD 操作を有効にするには 、エンティティを Dataverse の仮想エンティティとして使用できるようにする必要があります。 これにより、Finance and Operations アプリに存在するデータに対して、Dataverse と Microsoft Power Platform から CRUD 処理を実行できるようになります。

Finance and Operations 内のすべての Open Data Protocol (OData) エンティティは、Dataverse の仮想エンティティとして使用できます。したがって Power Platform でも使用できます。 作成者は、Finance and Operations から直接データを使用して Customer Engagement アプリのエクスペリエンスを構築できるようになりました。このとき、完全な CRUD 機能を使用でき、Dataverse にコピーする必要はありません。 Power Apps ポータルは、Finance and Operations の業務プロセスのコラボレーション シナリオを可能にする外部向けの Web サイトを構築するために使用できます。

#### <a name="virtual-entities-for-core-human-resources"></a>Core Human Resources の仮想エンティティ
Core Human Resources エンティティは、Finance and Operations エンティティと同じように仮想化することもできます。 詳細については、[Core HR の仮想エンティティ](../../../human-resources/hr-admin-integration-common-data-service-virtual-entities.md)を参照してください。


#### <a name="virtual-entities-vs-dual-write"></a>仮想エンティティ対二重書き込み
仮想エンティティは、データを Dataverse に物理的にコピーすることなく、Finance and Operations で Microsoft Power Platform を使用するメカニズムを提供します。 このガイダンスは、要件に二重書き込みまたはデータ統合、または仮想エンティティが必要かどうかを判断するために使用します。 仮想エンティティと二重書き込み/データ統合は、必要に応じて併用できる補完的なテクノロジです。 各テクノロジは、[統合戦略](../data-entities/integration-overview.md)で説明されているように、特定のシナリオに対して存在します。

### <a name="dual-write-functionality"></a>二重書き込み機能
二重書き込み機能は、Customer Engagement アプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する標準のインフラストラクチャです。 顧客、製品、人材、および業務に関するデータがアプリケーション境界を超えてフローする場合、組織のすべての部門が権利を持つことになります。

二重書き込み機能は、Finance and Operations アプリと Dataverse の間で密に結合された双方向の統合を提供します。 Finance and Operations アプリでのデータの変更によって Dataverse 書き込みが行われ、Dataverse のデータの変更によって Finance and Operations アプリケーションへの書き込みが行われます。 この自動化されたデータ フローによって、アプリ間で統合されたユーザー エクスペリエンスが提供されます。  二重書き込み機能の詳細については、[二重書き込みの概要](../data-entities/dual-write/dual-write-overview.md) を参照してください。

### <a name="add-ins-functionality"></a>アドイン機能
アドインを使用すると、Finance and Operations アプリの機能を拡張できます。 すべてのアドインは、サンドボックスおよび実稼働タイプの環境の環境詳細ページの Lifecycle Services を介してインストールされ、管理されます。 インストールされているアドインと各アドインの構成オプションに関するメタデータは、Power Platform 統合の一部としてプロビジョニングされている Microsoft Dataverse データベースに格納されます。 一部のアドインは、Dataverse データベースにビジネス データも格納します。 使用可能なアドインの詳細については、[アドインの概要](add-ins-overview.md) を参照してください。

## <a name="architecture"></a>アーキテクチャ

仮想エンティティは、Finance and Operations 以外にも有用な Dataverse の概念です。 次の図は、仮想エンティティの Finance and Operations プロバイダーを実装する方法を示しています。 6 つの主要メソッドがプロバイダーによって実装されます。 最初の 5 つのメソッドは、**Create**、**Update**、**Delete**、**Retrieve**、**RetrieveMultiple** という標準的な CRUD 操作です。 最後のメソッドである **PerformAction** は、このトピックで後述するように OData アクションを呼び出すために使用されます。 Finance and Operations 仮想エンティティ データ プロバイダー (図では "VE プラグイン" と表示) を呼び出すと、Finance and Operations の CDSVirtualEntityService Web API エンドポイントに対して Secure Sockets Layer (SSL)/トランスポート層セキュリティ (TLS) 1.2 セキュア Web 呼び出しが行われます。 その後、この Web サービスは、Finance and Operations 内の関連する物理エンティティへの呼び出しにクエリを変換し、それらのエンティティで CRUD 操作または OData 操作を呼び出します。 Finance and Operations エンティティはすべての操作で直接呼び出されるため、エンティティまたはバッキング テーブルのビジネス ロジックも呼び出されます。

[![Finance and Operations アプリの仮想エンティティのアーキテクチャ](../media/fovearchitecture.png)](../media/fovearchitecture.png)

呼び出し時、Dataverse から Finance and Operations アプリまで 2 つの変換点があります。 変換の最初のポイントは、エンティティの物理名などの概念を Finance and Operations エンティティ名に変換する VE プラグインにあります。 また、会社の参照などの既知の概念も変換されます。 Web サービス呼び出しでは、引き続き EntityCollection、Entity、および QueryExpression オブジェクトを使用して、実行される操作が表されます。このとき、VE プラグインから変換されたエンティティ名と概念が使用されます。 最後に、Finance and Operations の CDSVirtualEntityAdapterService Web API によって、QueryExpression から QueryBuildDataSource およびその他の内部 Finance and Operations 言語構成要素への変換が完了します。

仮想エンティティの一部としての Dataverse および Finance and Operations 間での呼び出しはすべて、コンフィギュレーションで指定されている Azure Active Directory (Azure AD) アプリケーションを使用して、サービス間 (S2S) 呼び出しとして実行されます。 このアプリケーションのユーザーは、CDSVirtualEntityAdapterService Web API とカタログ エンティティ CDSVirtualEntityListEntity に *のみ* アクセスできるようにする必要があります。 これらの特権は、CDSVirtualEntityApplication という名前の、標準のセキュリティ ロールに含まれています。 S2S 呼び出し中に、アクションを呼び出す Dataverse のユーザーの ID が Dataverse により提供されます。 CDSVirtualEntityAdapterService Web API は、Finance and Operations の関連付けられているユーザーを検索し、そのユーザーのコンテキストでクエリを実行します。 したがって、S2S 呼び出しでは、すべての Finance and Operations エンティティに明示的にアクセスする必要はありません。 代わりに、データ アクセスを決定するには、アクションを呼び出すユーザーの特権が必要な場合があります。

> [!NOTE]
> 仮想エンティティの呼び出しの待機時間を最適化するために、同じ Azure リージョンに Finance and Operations と Dataverse の両方を同一配置することをお勧めします。 同一配置する場合、仮想エンティティの間接費は 1 回の呼び出しあたり 30 ミリ秒 (ms) 未満である予定です。

Power Apps ポータルでは、仮想エンティティにもアクセスできます。 Power Apps ポータル認証は連絡先レコードに基づいているため、連絡先レコードと Finance and Operations ユーザーの間のマッピングは Dataverse の msdyn\_externalportalusermapping テーブルで管理されます。 このテーブルは、Dataverse の高度な特権を持つユーザーのみが編集できます。このユーザーは、ポータル ユーザーのセキュリティアクセスを Finance and Operations 仮想エンティティに対して制御する権限を持っています。 Power Apps ポータル アクセス用に設定されたすべての Finance and Operations ユーザーには、CDSVirtualEntityAuthorizedPortalUser セキュリティ ロールが割り当てられている必要があります。また、システム管理者またはセキュリティ管理者ロールを割り当てることはできません。 仮想エンティティに適用される Power Apps ポータル セキュリティ設定に関係なく、Finance and Operations アプリへの結果のクエリは常に関連付けられた Finance and Operations ユーザーとして実行され、そのユーザーのエンティティと行のセキュリティ設定に従います。 匿名ポータルのアクセスもサポートされます。 このタイプのアクセスとその実行方法については、[Power Apps ポータル参照](power-portal-reference.md)を参照してください。

## <a name="prerequisites-for-setting-up-the-power-platform-integration"></a>Power Platform 統合を設定するための前提条件
次の一覧は、Power Platform 統合を設定するための前提条件に関する詳細を提供します。

- テナントで少なくとも 1 ギガバイト (GB) の Power Platform データベース ストレージ容量スペースが使用可能であることを確認してください。 それ以外の場合、設定は失敗です。 [Power Platform管理センター](https://admin.powerplatform.microsoft.com/resources/capacity) にて、容量を表示できます。 
- Finance and Operations 環境管理者を識別します。 **環境の詳細** セクションにて、情報を確認できます。

    ![環境の詳細タブ](media/EnvironmentDetails.png)
    
- Power Platform 環境ガバナンス ポリシーを検証します。 検証するには、**グローバル管理者** または **Power Platform 管理者** である必要があります。
    
    1. [Power Platform 管理センター](https://admin.powerplatform.microsoft.com) にサイン インします。
    2. Power Platform サイトの右上端にあるギア アイコンを選択します。
    
        ![Power Platform の設定](media/PowerPlatformSettings.png)
    
- **全員** に Power Platform 実稼働環境の作成を許可しない組織のために、Finance and Operations 環境管理者のアカウントを次の Power Platform 管理ロールの 1 つを追加する必要があります。
    
    Finance and Operations 環境管理者は、次のいずれかのロールに追加する必要があります。 このアクションを実行するには、グローバル管理者が必要です。
    - Global 管理者
    - Dynamics 365 管理者
    - Power Platform 管理者
    
    詳細については、[サービス管理者ロールを使用したテナントの管理](/power-platform/admin/use-service-admin-role-manage-tenant) を参照してください。

- Power Platform 環境を作成するすべてのユーザーはライセンスが必要です。 Finance and Operations 環境管理者アカウントは、Microsoft 365 管理者センターを使用して **Dynamics 365 Unified Operations プラン** ライセンスを適用する必要があります。

## <a name="enabling-the-power-platform-integration"></a>Power Platform 統合の有効化
現在、Power Platform 統合は Finance and Operations 環境の配置後にのみ設定できます。  将来、Finance and Operations 環境自体を配置中や新しいサンドボックス環境と実稼働環境でも可能になります。

### <a name="set-up-after-environment-deployment"></a>環境を配置後に設定
Finance and Operations 環境が配置された後に設定するには、次の手順に従います。

1. Finance and Operations 環境が LCS を通じて展開された後、LCS の **環境詳細** ページが開きます。
2. **Power Platform 統合** セクションで、**設定** を選択します。
3. **Power Platform 環境の設定** ダイアログ ボックスで契約条件に同意し、ダイアログ ボックスの下部にある **設定** を選択します。

    > [!NOTE]
    > これにより、Power Platform 管理センターで Microsoft Dataverse ベースの環境がプロビジョニングされ、通常は 1GB のデータベース ストレージ容量が必要になります。  使用する Finance and Operations 環境と同じ名前が必要です。  二重書き込みプラットフォーム レベルのコンポーネントはインストールされますが、二重書き込みアプリケーション コンポーネントは設定または有効化されません。  これは別のアクションです。  

4. Microsoft Power Platform 環境が準備されているというメッセージが表示された場合は、**OK** を選択します。

    **環境詳細** ページの **Power Platform 統合** セクションに、Microsoft Power Platform 環境が準備されているというメッセージが表示されます。

5. 数分後、**環境の詳細** ページが更新されます。
6. **Power Platform 統合** セクションにおいて、**ステータス** フィールドの値が **環境設定が進行中** であることに注意してください。

    通常、設定は 60分 から 90分かかります。

    Dataverse 環境がプロビジョニングされた後、**新しいアドインのインストール** と **二重書き込みアプリケーション** ボタンが **Power Platform 統合** セクションで利用できます。

    ![新しいアドイン ボタンのインストール](media/InstallANewAddIn.png)
    <br/>
    ![二重書き込みアプリケーション ボタン](media/powerplat_integration_dwApp_button.png)

### <a name="troubleshooting-the-setup"></a>設定のトラブルシューティング
設定は、Dataverse ベースの環境を配置するさまざまなステージで失敗する可能性があります。   

![デュアル書き込みの失敗](media/Error.png)

- 設定が失敗すると、エラー メッセージが表示されます。  エラー メッセージに基づいて、ライセンスや容量の問題に対処する必要がある場合があります。  これらが解決されたら、LCS の **環境の詳細** ページの **Power Platform 統合** セクションにある **再開** ボタンを使用して設定を完了することができます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
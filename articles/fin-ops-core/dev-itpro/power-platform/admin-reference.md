---
title: Finance and Operations および Common Data Service 管理リファレンス
description: このトピックでは、Finance and Operations の仮想エンティティの設定およびコンフィギュレーションについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-05-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: ddfa10d019ca83323baeac2a152f5f1fd7db4c2a
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416594"
---
# <a name="finance-and-operations-and-common-data-service-admin-reference"></a>Finance and Operations および Common Data Service 管理リファレンス
[!include[banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> この機能を使用するには、Common Data Service のサービス更新プログラム 189 が必要です。 Common Data Service のリリース情報は、[最新バージョンの利用可能性](https://docs.microsoft.com/business-applications-release-notes/dynamics/released-versions/dynamics-365ce#all-version-availability)ページに発行されています。

このトピックでは、Common Data Service で Finance and Operations アプリの仮想エンティティを設定およびコンフィギュレーションする方法について手順を追って説明します。

## <a name="getting-the-solution"></a>ソリューションの入手
Finance and Operations 仮想エンティティ Common Data Service ソリューションは、[仮想エンティティ ソリューション](https://www.yammer.com/dynamicsaxfeedbackprograms/#/files/596330233856)からダウンロードする必要があります。

次のソリューションが Common Data Service にインストールされていることを確認します。 これらのソリューションは、ダウンロードしたパッケージから抽出する必要があります。

- **Dynamics365Company**: すべての Finance and Operations エンティティによって参照される**会社**エンティティを、PrimaryCompanyContext メタデータ値と共に追加します。

- **MicrosoftOperationsVESupport**: これにより、Finance and Operations 仮想エンティティ機能のコア サポートが提供されます。

- **MicrosoftOperationsERPCatalog**: これは、mserp_financeandoperationsentity 仮想エンティティを通じて使用できる Finance and Operations エンティティの一覧を提供します。

- **MicrosoftOperationsERPVE**: これは、表示されるときに生成された仮想エンティティを含む、API マネージド ソリューションです。

また、[PackageDeployer ツール](https://docs.microsoft.com/power-platform/admin/deploy-packages-using-package-deployer-windows-powershell#PD_tool)を使用して、Common Data Service でソリューション パッケージを単一の単位として直接インポートすることもできます。

## <a name="authentication-and-authorization"></a>認証と承認

ソリューションを Common Data Service 環境にインポートした後は、両方の環境を相互に接続するように設定する必要があります。 Common Data Service は、Azure Active Directory (AAD) アプリケーションに基づいて、サービス ツー サービス (S2S) 認証を使用して Finance and Operations を呼び出します。 この新しい AAD アプリケーションは、Common Data Service 環境の単一のインスタンスを表します。 Common Data Service と Finance and Operations の環境の組み合わせが複数存在する場合は、ペアごとに独立した AAD アプリケーションを作成して、Finance and Operations 環境と Common Data Service 環境の正しいペア間で確実に接続が確立されるようにする必要があります。 次の手順は、AAD アプリケーションの作成方法を示しています。

1.  <https://portal.azure.com> **\> Azure Active Directory \> アプリの登録** に移動します。

2.  **新規登録** を選択します。 次の情報を入力します。

    - **名前**: 一意の名前を入力します。

    - **アカウント タイプ**: **任意の Azure AD ディレクトリ**を入力します (単一またはマルチテナント)。

    - **リダイレクト URI**: 空白のままにします。

    - **登録** を選択します。

    - **アプリケーション (クライアント) ID** の値をメモしておきます。後の手順で必要となります。

3.  アプリケーションの対称キーを作成します。

    - 新しく作成されたアプリケーションで **証明書とシークレット** を選択します。

    - **新しいクライアント シークレット** を選択します。

    - 説明と有効期限を入力します。

    - **保存** を選択します。 キーが作成され、表示されます。 この値を後で使用するためにコピーします。

上で作成した AAD アプリケーションは、Common Data Service によって Finance and Operations アプリを呼び出すために使用されます。 したがって、Finance and Operations によって信頼され、Finance and Operations で適切な権限を持つユーザー アカウントに関連付けられている必要があり ます。 Finance and Operations では、特殊サービス ユーザーは、仮想エンティティ機能に対する権限*のみ*で作成することができます。その他の権限は必要ありません。 この手順を完了すると、上で作成した AAD アプリケーションのシークレットを使用するアプリケーションによって、この Finance and Operations 環境を呼び出して仮想エンティティの機能にアクセスできるようになります。

次の手順では、このプロセスを Finance and Operations アプリで実行していきます。

1.  Finance and Operations で、**システム管理 \> ユーザー \> ユーザー**の順に移動します。

2.  **新規作成**を選択して、新しいユーザーを追加します。 次の情報を入力します。

    - **ユーザー ID**: **cdsintegration** (または別の値) を入力します。

    - **ユーザー名**: **cds integration** (または別の値) を入力します。

    - **プロバイダー**: 既定値をそのまま使います。

    - **電子メール**: **cdsintegration** (または別の値) を入力します (有効な電子メール アカウントである必要は*ありません*)。

    - このユーザーにセキュリティ ロール **CDS 仮想エンティティ アプリケーション**を割り当てます。

    - **システム ユーザー**を含む他のすべてのロールを削除します。

3.  **システム管理 \> 設定 \> Azure Active Directory アプリケーション** の順に移動して Common Data Service を登録します。 

    - 新しい行を追加します。

    - **クライアント ID**: 上で作成された**アプリケーション (クライアント) ID**

    - **名前**: **CDS 統合** (または別の名前) を入力します。

    - **ユーザー ID**: 上記で作成されたユーザー ID。

プロセスの次の手順では、接続先の Finance and Operations インスタンスに Common Data Service を提供します。 以下の手順では、プロセスのこの部分について説明します。

1.  Common Data Service では、**詳細設定 \> 管理 \> 仮想エンティティ データ ソース**に移動します。

2.  "Finance and Operations" というデータ ソースを選択します。

3.  上記の手順に従って情報を入力します。

    - **ターゲット URL**: Finance and Operations にアクセスできる URL。

    - **OAuth URL** - https://login.windows.net/

    - **テナント ID**: "contoso.com" などのテナント。

    - **AAD アプリケーション ID**: 上で作成された**アプリケーション (クライアント) ID**。

    - **AAD アプリケーション シークレット**: 上で生成されたシークレット。

    - **AAD リソース**: 00000015-0000-0000-c000-000000000000 と入力します (これは、Finance and Operations を表す AAD アプリケーションです。常に同じ値であることを表します)。

4.  変更を保存します。

## <a name="enabling-virtual-entities"></a>仮想エンティティの有効化

Finance and Operations には多数の OData 対応エンティティが含まれているため、既定では、エンティティは Common Data Service の仮想エンティティとしては使用できません。 次の手順では、必要に応じてエンティティを仮想にすることができます。

1. Common Data Service で、**高度な検索**に移動します。

2. [利用可能な Finance and Operations エンティティ] を探して、**結果** を選択します。

![カタログ](../media/fovecatalog.png)

3. 有効にするエンティティを検索して開きます。

4. **表示** を **はい** に設定して保存します。 これにより、仮想エンティティが生成され、[高度な検索] ダイアログ ボックスなどの適切なすべてのメニューに表示されるようになります。

![VE の有効化](../media/foveenable.png)

## <a name="refreshing-virtual-entity-metadata"></a>仮想エンティティ メタデータの更新

仮想エンティティ メタデータは、Finance and Operations のエンティティ メタデータが変更されたと想定される場合に、強制的に更新できます。 これを行うには、**更新** を **はい** に設定して保存します。 これにより、Finance and Operations の最新のエンティティ定義が Common Data Service に同期され、仮想エンティティが更新されます。

<a name="referencing-virtual-entities"></a>仮想エンティティの参照
----------------------------

仮想エンティティはすべて MicrosoftOperationsERPVE ソリューションで生成され、API によって管理されます。 つまり、エンティティの表示/非表示を変更してもソリューションの項目は変化しますが、それでも依存できるマネージド ソリューションになります。 標準 ALM フローでは、ISV ソリューションの **既存の追加** オプションを使用して、このソリューションから仮想エンティティに対する標準参照を取得するだけです。 これにより、ソリューションの依存関係が見つからないと表示され、ソリューション インポート時にチェックされます。 インポート中に、指定された仮想エンティティがまだ存在しない場合は、追加の作業を必要とすることなく、自動的に表示されます。

仮想エンティティを使用するには

1.  Common Data Service で通常どおり別個のソリューションを作成します。これには、消費ロジックが含められます。

2.  **エンティティ \> 既存の追加** を選択します。 一覧から参照する仮想エンティティを選択します。

3.  追加する資産の選択を求めるメッセージが表示されたら、カスタマイズするフォーム、ビュー、またはその他の要素を選択し、**完了** を選択します。

開発ツールから、フォームなどの既存の要素を仮想エンティティに対して変更することができます。 また、新しいフォーム、ビュー、およびその他の要素を追加することもできます。

![ソリューション](../media/fovesolution.png)

ソリューションをエクスポートすると、MicrosoftOperationsERPVE ソリューションで生成された仮想エンティティへのハード依存関係が含められます。

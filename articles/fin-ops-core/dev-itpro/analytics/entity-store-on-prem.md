---
title: PowerBI.comとオンプレミス環境との統合
description: このトピックでは、 オンプレミス配置にてエンティティストアを有効にする方法を提供します。
author: MilindaV
manager: AnnBe
ms.date: 06/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EntityStoreOnPrem
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2019-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c4c91fcb0d0d94f0502184ddd3fb224774ff83
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771457"
---
# <a name="powerbicom-integration-with-on-premises-environments"></a>オンプレミス環境との PowerBI.com の統合

[!include [banner](../includes/banner.md)]

クラウド版では、Microsoft Power BI との緊密な統合を可能にするいくつかの機能が用意されています。 いくつかの機能は、オンプレミスの配置用にはまだ実装されていません。 ただし、オンプレミス配置でのエンティティ格納を利用することで、PowerBI.com を使って Finance and Operations のデータのレポートや分析ができるようになっています。 

このトピックでは、 Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム26 (2019年5月)以降にて動作する、オンプレミス配置で使用できる分析機能について概説します。

| 特性/機能                                                           | クラウド     | オンプレミス (プラットフォーム更新プログラム 26 またはそれ以降) |
|------------------------------------------------------------------------------|-----------|-------------------------------------------|
| 分析ワークスペース                                                        | 利用可 | **まだ実装されていません**<p>Entity Store上で構築されたレポートは、PowerBI.comと一緒に使うことができます。</p> |
| PowerBI.com からレポート、タイル、およびダッシュボードをクライアントに固定することができます。         | 利用可 | **まだ実装されていません** |
| アプリケーションのデータを使用した Power BI のレポートを作成および配布します。 | 使用可能 | **使用可能**<p>オンプレミスでエンティティストアを使用することで、既製のレポートを変更したり、新しいレポートを作成をすることができます。</p> |
| アプリケーション データをデータ ウェアハウスに抽出します。                    | 使用可能 | **使用可能** |

## <a name="enable-entity-store-on-premises"></a>エンティティストアをオンプレミスにて有効化する

このトピックでは [、オンプレミス環境の設定および配置 (プラットフォーム プラットフォーム 12 および それ以降)](../deployment/setup-deploy-on-premises-pu12.md) についての補足事項を提供します。 以下のセクション番号は、該当するトピックのセクション番号に対応しています。

### <a name="3-plan-your-users-and-service-accountsdeploymentsetup-deploy-on-premises-pu12mdplansvcacct"></a>[3. ユーザーとサービスのアカウントを準備する](../deployment/setup-deploy-on-premises-pu12.md#plansvcacct)

| ユーザー アカウント               | 型     | 目的 | ユーザー名 |
|----------------------------|----------|---------|-----------|
| AOS SQL AXDW DB 管理者 ユーザー | SQL ユーザー | アプリケーションは、このユーザーを使用して AXDW データベースに情報を入力します。 このユーザーは任意であり、エンティティストアに対応する必要がある場合にのみ作成する必要があります。 | axdwadmin |
| AOS SQL AXDW FB 管理者 ユーザー | SQL ユーザー | アプリケーションは、このユーザーを使用して AXDW データベースに情報を入力します。 このユーザーは任意であり、エンティティストアに対応する必要がある場合にのみ作成する必要があります。 | axdwruntimeuser |

### <a name="14-configure-the-databasesdeploymentsetup-deploy-on-premises-pu12mdconfiguredb"></a>[14. データベースの環境設定](../deployment/setup-deploy-on-premises-pu12.md#configuredb)

本セクションの以下手順は任意の設定です。

エンティティストアに使用するデータベースを作成する場合は、最初に ConfigTemplate .xml ファイルを変更する必要があります。

1. **DbServer - セキュリティ**で、 **axdwadmin** および **axdwruntimeuser** の **generateuser** フラグを **True**に設定します。 次の手順のスクリプトを実行すると、2つのユーザーが作成されます。 ユーザーのパスワードを設定するよう求められます。
2. 次のスクリプトを実行します。

        .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EntityStore
        .\Configure-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EntityStore

    Initialize-Database.ps1 スクリプトは、以下の処理を行います:

    - **AXDW** という名前の空のデータベースを作成します。 このデータベースは、エンティティストアに使用されます。
    - SQL認証が有効となった **Axdwadmin** という名前の新規ユーザーが作成され、パスワードの設定が求められます。
    - SQL認証が有効となった **axdwruntimeuser** という名前の新規ユーザーが作成され、パスワードの設定が求められます。
    - axdwadmin と axdwruntimeuser に対して、データベースへの **データベース\_所有者** 権限を付与します。

    Configure-Database.ps1 スクリプトは、以下の処理を行います:

    - 指定したデータベースファイル と ログの設定を行います。
    - VIEW SERVER STATE 権限を axdbadmin に付与します。
    - VIEW SERVER STATE 権限を axdwruntimeuser に付与します。

### <a name="15-encrypt-credentialsdeploymentsetup-deploy-on-premises-pu12mdencryptcred"></a>[15. 資格情報の暗号化](../deployment/setup-deploy-on-premises-pu12.md#encryptcred)

以下のように、Credentials.json ファイルを作成します。 **AosDWAuth** カテゴリは任意であり、エンティティストアが有効な場合にのみ使用されます。

    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        },
        "AosDWAuth": {
            "DWUser": "<encryptedDWUser>",
            "DWPwd": "<encryptedDWPassword>",
            "DWRuntimeUser": "<encryptedDWRuntimeUser>",
            "DWRuntimePwd": "<encryptedDWRuntimePassword>"
        }
    }

上記のコマンドの内容について説明します:

- **AccountPassword** は、Application Object Server (AOS) ドメインユーザー (contoso\\axserviceuser) 用の暗号化されたドメイン ユーザー パスワードです。
- **SqlUser** は、アプリケーション データベース (AXDB) にアクセス権限が付与されている暗号化された SQL ユーザー (axdbadmin) です。 **SqlPwd** は暗号化されたSQLパスワードです。
- **DWUser** は、エンティティストア データベース (axdw) へのアクセス権限が付与されている、暗号化されたSQLユーザー (axdwadmin) です。 **DWPwd** は、Initialize-Database.ps1 スクリプトの実行時に入力される暗号化されたSQLパスワードです。
- **DWRuntimeUser** は、エンティティストア データベース (AXDW) へのアクセス権限が付与されている、暗号化されたSQLユーザー (axdwruntimeuser) です。 **DWRuntimePwd** は、Initialize-Database.ps1 スクリプトの実行時に入力される暗号化されたSQLパスワードです。

## <a name="more-information"></a>詳細情報

エンティティストアは、プラットフォーム更新プログラム 26で有効となっています。

エンティティストアを行うデータベースとユーザーの作成は任意です。 Microsoft Dynamics Lifecycle Services (LCS)で配置の構成を行う際には、エンティティストアのカスタマイズを空白のままにしておくことができます。

エンティティストアを環境内で有効にする必要がある場合は、以下のタスクを完了する必要があります:

- 手順14に記載のスクリプトを使用することで、 **AXDW** データベースを作成することができます。
- 手順14に記載のスクリプトを使用することで、適切な権限を持つ **axdwadmin** と **axdwruntimeuser** ユーザーを作成することができます。 ユーザーは次のファイルで定義されています: ConfigTemplate.xml、DatabaseTopologyDefinition.xml
- 手順15に記載の **Credentials.json** ファイルを作成します。 手順14に記載されているように、ユーザー名とパスワードは、axdwadminおよびaxdwruntimeuserに対して定義する必要があり、暗号化する必要があります。
- エンティティストアを行うSQL Serverの名称および、データベースの名称は、LCSへの配置差処理中に設定される必要があります。

    - データベースの名称は手順14で作成され、DatabaseTopologyDefinitionファイルにて定義されています。 既定の名称は **AXDW** です。
    - SQL Serverの名称は、 Microsoft SQL Server またはAlwaysOnリスナー の完全修飾ドメイン名 (FQDN) となります。 このFQDNの例としては、 **sqlinstance.onprem.contoso.com** があります。 これはAXDWデータベースが作成されたサーバーです。

現在のところ、エンティティストアの有効化は最初の配置処理中にのみ行うことができます。 既存の環境で有効にする必要がある場合は、エンティティストアに対応しているプラットフォームの更新を使用して、当該環境を削除したのちに再度配置する必要があります。

## <a name="authoring-and-distributing-reports-by-using-entity-store-on-premises"></a>エンティティストア オンプレミスを使用したレポートの作成および配布

エンティティ格納は、含まれている運用データ ウェアハウスです。 これにより、パワー ユーザーやビジネス アナリストは、シンプルで豊富なデータを使用したレポートを作成することができます。 エンティティストアには集計測定値が含まれており、単純化されたスタースキーマを使用できます。 エンティティストアを使用してレポートを作成する方法の詳細については、 [ Power BI Desktopを使用して分析レポートを作成する](author-distribute-power-bi-reports.md)を参照してください。

オンプレミスの配置に固有となる、以下の手順についても注意してください。

- オンプレミス環境においては、実運用環境またはサンドボックス環境に Power BI レポートを配置するにあたってLCSを使用する必要はありません。 オンプレミス環境では、管理者はPowerBI.comデータセットを特定のエンティティー ストアデータベースに指定することができるため、LCSが提供する機能を使用する必要はありません。 ただし、オンプレミスのゲートウェイを設定して、オンプレミスのデータにPowerBI.comがアクセスできるようにする必要となる場合もあります。 ゲートウェイの詳細については、 [Power BI ゲートウェイのドキュメント](https://powerbi.microsoft.com/gateway/) を参照してください。
- クラウドベースのアプリケーション環境は、DirectQuery オプションを使用して作成されたレポートにのみ対応していますが、オンプレミスのエンティティ格納は、DirectQuery レポートとインポート モード レポートの両方に対応しています。
- 分析ワークスペースは、オンプレミス配置はに実装されていません。 分析ワークスペースでレポートを表示することはできませんが、PowerBI.com の環境にレポートを配置することができます。 そうすることで、PowerBI.com へのアクセス権限を持つユーザーがレポートを使用できるようになります。 PowerBI.comのレポートへのアクセスには、ユーザーが適切なライセンスを要求する場合があります。

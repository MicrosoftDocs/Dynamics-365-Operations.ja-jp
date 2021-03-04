---
title: オンプレミス障害復旧コンフィギュレーション
description: このトピックでは、ディザスター リカバリー用に Dynamics 365 Finance + Operations (オンプレミス) を構成する方法について説明します。
author: faix
manager: AnnBe
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: d9159d0d7a00d9d312ec3ca11cc244a62fd56389
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128741"
---
# <a name="on-premises-disaster-recovery-configuration"></a>オンプレミス障害復旧コンフィギュレーション
ディザスター リカバリーは、組織のオペレーションを危険にさらす可能性のあるイベントから保護するために、Dynamics 365 Finance + 操作 (オンプレミス) をオンプレミスで導入する際に重要となる考慮事項です。 このようなイベントの例としては、機材の故障、サイバー攻撃、電気的、物理的なデータの破損などによるデータセンターの停止が含まれます。

ディザスター リカバリーの中心となる概念は、データ復元環境を含む2番目のデータセンターを使用することです。 ディザスター リカバリーの計画、文書化、テストは、運用環境の設定と同様に慎重に行うことを推奨します。

### <a name="limitations-of-this-content"></a>このコンテンツの制限事項

このトピックでは、以下のコンポーネントのディザスター リカバリーに関する構成の詳細については説明しません。
  - Active Directory フェデレーション サービス (AD FS)
  - ファイルのストレージ
  - SQL Server

> [!NOTE]
> 高可用性の構成については、このトピックでは説明していません。 高可用性に必要な最小限の設定の詳細については、[オンプレミス配置に関するシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md#minimum-infrastructure-requirements)を参照してください。

### <a name="recommendations"></a>推奨事項

ディザスター リカバリー環境は、常に最新の Windows 更新プログラムで更新しておいてください。 ご利用の環境には最新のセキュリティ更新プログラムが適用されている必要がありますが、障害の発生時には更新が必要となりません。

Microsoft が指定した新しい前提条件を適用していることを確認します。 また、Service Fabric Cluster を更新して、必要に応じて証明書のローテーションを実行します。

このトピックを読んだ後で、チームが実施する必要のある手順を文書化してください。 その後は、予想外の問題が発生しないよう、手順を複数回実施して、発生する可能性のあるダウンタイムを最小限に抑えてください。

## <a name="overview"></a>概要

ディザスター リカバリーの基本構成では、別のデータセンター (セカンダリ データセンター) 内に実稼働環境の複製を配置し、そのデータセンターにデータベースを複製します。 災害イベントが発生した場合、いくつかの手動の手順を実施することで、セカンダリ データセンター内の環境をオンライン状態にすることができます。

以下の図では、必要となる設定の詳細を示しています。

![ディザスター リカバリー アーキテクチャ](media/DRArchitecture.png)

## <a name="environment-configuration"></a>環境のコンフィギュレーション

Lifecycle Services (LCS) では、運用環境は、**運用** と名付けた環境のスロットを使用して配置する必要があります。 ディザスター リカバリー環境では、LCS の追加の環境スロットが使用されません。 その代わりに、運用環境でスロットを再利用します。 

Finance and Operations AOS ノードと SQL Server は、同じデータセンター内に共存している必要があります。 詳細については、[オンプレミス展開のシステム要件](../../fin-ops/get-started/system-requirements-on-prem.md#network-requirements)を参照してください。

## <a name="deploying-code-packages-to-production"></a>運用環境にコード パッケージを配置する

コード パッケージを運用環境に配置する場合はディザスター リカバリー環境に配置する必要はありません。 この環境を使用せずに、Service Fabric サービスを配置しないようにする必要があります。

## <a name="environment-deployment-settings"></a>環境を配置する設定

ディザスター リカバリー環境は、運用環境と同様の構成にする必要があります。 以下の表に、ディザスター リカバリーに向けて共有される設定と固有となる設定を示します。

| 環境設定 | ディザスター リカバリー環境|
|---------------------------------|----------------|
| **Active Directory の設定**   |                |
| 管理者ユーザー              | 運用環境と同等|
| AD FS URL                        | 運用環境と同等|
| AOS の AD FS OpenId Connect クライアントID | 運用環境と同等|
| Financial Reporting の AD FS OpenId Connect クライアントID | 運用環境と同等|
| **SQL データベースの構成**  |                 |
| SQL Server の名称                 | 運用環境と同等 |
| AX データベース名                | 運用環境と同等 |
| Financial Reporting データベースの名前| 運用環境と同等 |
| **ファイル共有設定**         |                 |
| ドキュメント ストアのファイル共有   | 運用環境と同等 |
| ファイル共有証明書の拇印 | 運用環境と同等 |
| **SSRS コンフィギュレーション設定** |                 |
| SSRS インスタンスの IP アドレス     | 異なる場合があります <sup>1</sup> |
| SSRS 証明書の拇印     | 運用環境と同等 |
| **サービスの設定のコンフィギュレーション**  |                 |
| Dynamics 365 インスタンスの DNS ホスト名 | 異なる場合があります <sup>2</sup>|
| AOS サービス ユーザー                | 運用環境と同等 |
| MR アプリケーション サービスのユーザー     | 運用環境と同等 |
| MR プロセス サービスのユーザー         | 運用環境と同等 |
| MR click-once サービスのユーザー      | 運用環境と同等 |
| **アプリケーション証明書の設定** |                 |
| データの暗号化証明書の拇印| 運用環境と同等 |
| データ署名証明書の拇印 | 運用環境と同等   |
| セッション認証証明書のの拇印 | 運用環境と同等 |
| SSL 証明書の拇印       | 運用環境と同等 |
| Management reporter 証明書の拇印 | 運用環境と同等 |

<sup>1</sup> SSRS は IP が参照します。 ディザスター リカバリー環境で正確なマシンの IP を構成できない場合は、IP を別のものにすることができます。

<sup>2</sup> これはネットワークの構成によって異なります。 他の環境へのトラフィックの流用に対応できる負荷分散装置を使用している場合は、ホスト名を同じにすることができます。 この対応ができない場合は、別のホスト名を使用します。 

## <a name="sql-server-always-on-availability-configuration"></a>SQL Server の常時可用性を構成する

ビジネス データ データベース (AXDB) は、通常は SQL Server の常時可用性グループ機能を使用して、セカンダリ データセンターに複製する必要があります。 詳細については、[常時可用性グループ](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-sql-server?view=sql-server-2016)を参照してください。

| データベース | レプリケート済 |
|----------|------------|
| 業務データ (AXDB) | 有 |
| Financial Reporting  | 有 |
| BYODB                | 有 |
| OrchestratorData     | 有 |

## <a name="failing-over-to-disaster-recovery"></a>ディザスター リカバリーにフェイルオーバーする

### <a name="overview"></a>概要

障害イベントが発生した場合、プライマリ データセンターが使用できなくなった場合であっても、セカンダリ データセンター内では、以下のコンポーネントが使用できます。

![配置設定の拇印の例](media/DRArchitectureSingle.png)

障害が発生した最初の時点では、ディザスター リカバリー環境は空になります。 ここで存在するのは、複製された本番データのすべてを含む、構成済みの Service Fabric Cluster と SQL Server になります。 

ディザスター リカバリー環境をオンラインにするには、LCS を使用して運用環境で現在利用可能なものをディザスター リカバリー環境へと配置する必要があります。

>[!IMPORTANT]
> 続行する前に、運用環境で Dynamics Service Fabric サービスが実行されていないことを確認してください (部分的な障害が原因で失敗しているだけの場合)。

### <a name="deploy-the-localagent"></a>LocalAgent を配置する

LocalAgent のインストーラーと構成ファイルを LCS からディザスター リカバリー環境にダウンロードします。 構成ファイルを作成後に開きます。 ServiceFabric セクションの connectionEndpoint が、ディザスター リカバリー環境にあるサーバーの IP、または FQDN を指していることを確認します。 ファイルの変更後、そのファイルをローカルに保存し、通常どおり LocalAgent を配置します。

>[!IMPORTANT]
> LCS のコネクター設定には変更を加えないでください。 

メインの運用環境がオンラインに戻ってくるまで、この LocalAgent は LCS がメッセージ キューに入れたすべての要求を処理します。 そのため、運用環境でサービスが実行されていないことの確認が重要となります。 最終的には、オーケストレーター ノードがプライマリ データセンターに戻された際に、クラスターから LocalAgent のプロビジョニングを解除します。 

>[!CAUTION]
> LocalAgent は、一度に1つのデータセンターでのみ実行する必要があります。 この時点では、セカンダリ データセンターでのみ実行する必要があります。

### <a name="prepare-your-pre-deployment-scripts-optional"></a>配置前スクリプトの準備 (オプション)

配置の構成に変更が必要な場合は、配置前スクリプトを実行する必要があります。 このスクリプトでは、指定した値で config.json ファイルを修正する必要があります。 このスクリプトは、ユーザーが作成する必要があります。

config.json ファイルの場所は、以下のコマンドを実行sいて確認できます。

  ```sql
    select Location from DeploymentInstanceArtifact where AssetId='config.json' and DeploymentInstanceId = 'LCSENVIRONMENTID'
  ```

  > [!NOTE]
  > **LCSENVIRONMENTID** を環境の ID で置き換えます。 この ID は LCS 環境の詳細ページから取得することができます。 

SSRS ノードの IP が異なる場合は、次の値を変更する必要があります。

```json
        "biReporting": {
          "persistentVirtualMachineIPAddressSSRS": {
            "value": "192.168.5.31"
          },
          "reportingServers": {
            "value": "192.168.5.31"
          },
```

ホスト名を変更する場合は、次のように変更する必要があります。

```json
    "name": "AOS",
      "parameters": {
        "activeDirectory": {
          ...
          "aadValidAudience": {
            "value": "https://ax.contosoen05.com/"
          },
          ...
        "infrastructure": {
          "hostName": {
            "value": "ax.contosoen05.com"
          },
          ...
        }
    ...
    "name": "FinancialReporting",
      "parameters": {
        ...
        "aad": {
         ...
         "cookieDomain": {
            "value": "ax.contosoen05.com"
          },
          "validAudiences": {
            "value": "https://ax.contosoen05.com/"
          },
          ...
```

>[!IMPORTANT]
> 配置の際にホスト名の URL を変更する場合は、 AD FS サーバーが新規 URL を受け入れるように構成されていることを確認してください。 詳細については、[複数の環境で同じ AD FS インスタンスを再利用する](./onprem-reuseadfs.md)を参照してください。

ファイル共有機能が運用環境とディザスター リカバリー環境で共有されている場合、この配置前スクリプトを無効化する必要があります。 この機能は、ディザスター リカバリー環境に配置する場合にのみ有効にしてください。

### <a name="ensure-reports-get-deployed"></a>レポートを確実に配置する

データベースは既にに正常に同期されているため、通常、同期はスキップされます。 ただし、SSRS ノードが空であるため、レポートを同期するには、次の操作を実行します。

#### <a name="version-10013-or-later"></a>バージョン 10.0.13 、またはそれ以降

ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。

```sql
    UPDATE SF.synclog SET STATE=5, SyncStepName = 'ReportSyncstarted' WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CREATIONDATE DESC)
```


#### <a name="version-10012-or-earlier"></a>バージョン 10.0.12、または以前

ビジネス データ データベース (AXDB) に対して次のコマンドを実行します。

```sql
    DELETE FROM SF.synclog WHERE CODEPACKAGEVERSION in (SELECT TOP(1) CODEPACKAGEVERSION from SF.SYNCLOG ORDER BY CODEPACKAGEVERSION DESC)
```

>[!NOTE]
> バージョン 10.0.12、またはそれ以前のバージョンを使用している場合は、データベース全体が同期されます。

### <a name="deploy-your-environment"></a>環境の配置

環境を配置するには、以下の手順に従います。 

1. LCS で、ご利用の運用環境の環境ページに移動します。

1. **管理** を選択し、**更新の設定** を選択します。

    ![更新設定の適用](media/addf4f1d0c0a86d840a6a412f774e474.png)

1. 値を変更しないでください。 **準備** を選択します。

1. ダウンロードと準備が完了後は、**環境の更新** ボタンが表示されます。 このボタンを選択して、環境の更新を開始します

    ![環境の更新ボタン](media/0a9d43044593450f1a828c0dd7698024.png)

1. 環境が配置されると、ディザスター リカバリー環境を使用できるようになります。 

## <a name="using-your-disaster-recovery-environment"></a>ディザスター リカバリー環境を使用する

ディザスター リカバリー環境は、通常どおり使用できます。また、更新や修正プログラムを環境に適用する必要はありません。 環境に更新プログラムを適用する必要がある場合、フェイルバックのプロセスは以下に説明するものとは異なります。 この条件下でのフェイルバックについては、このトピックでは説明しません。

## <a name="failing-back-to-your-production-environment"></a>運用環境へのフェイルバック

>[!IMPORTANT]
> この時点では、運用環境で Dynamics Service Fabric サービスを実行する必要はありません。 

ディザスター リカバリー環境から運用環境への切り替えが可能なダウンタイムの時間枠を確保します。 ダウンタイムの時間枠で、ervice Fabric Explorer を介して、ディザスター リカバリー環境にあるオーケストレーター以外のすべてのノードを無効にします。 すべてのノードを無効化したら、SQL Server を運用データセンターにフェイルオーバーします。

フェイルオーバーが発生したら、プライマリ データセンターで AOS、SSRS、MR の各ノードを起動します。 検証テストを実行し、環境が予想どおりに機能していることを確認します。 環境が予想どおりに機能していると判断したら、ディザスター リカバリー環境から LocalAgent を削除し、運用環境に再インストールします。

すべての Dynamics Service Fabric サービスを手動で解除し、DR 環境をクリーンアップします。

>[!CAUTION]
> LCS のクリーンアップ機能を使用して、ディザスター リカバリー環境のクリーンアップを実行しないでください。 

### <a name="failback-checklist"></a>フェイルバックのチェックリスト

- 非オーケストレーター ノードは、ディザスター リカバリー データセンターでは無効となります。
- SQL Server がプライマリ データセンターにフェイルバックされます。
- LocalAgent は、ご利用のディザスター リカバリー データ センターからアンインストールされます。
- すべての Dynamics Service Fabric サービス (LocalAgent を含む) は、ご利用のプライマリ データセンターで実行されています。
- ご利用のディザスター リカバリー データセンターには、Dynamics Service Fabric サービスが配置されていません。 

>[!IMPORTANT]
> ご利用のプライマリ環境は通常どおり機能しており、チェックリストのすべての品目が確実に検証された後でサービスを実行することができます。

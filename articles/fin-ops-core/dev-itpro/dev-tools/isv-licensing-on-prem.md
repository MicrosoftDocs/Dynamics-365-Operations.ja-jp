---
title: 独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)
description: この記事では、オンプレミス環境における独立系ソフトウェア ベンダー (ISV) のライセンス機能について説明します。
author: faix
ms.date: 09/16/2022
ms.topic: article
ms.prod: dynamics-365
audience: Developer
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2018-03-07
ms.dyn365.ops.version: AX 7.3.0
ms.custom: 70381
ms.assetid: 90ae4ae6-f19a-4ea5-8bd9-1d45729b0636
ms.service: ''
ms.openlocfilehash: 221dba69fb377ae1762d7c32e3cfdbce7a73b5d1
ms.sourcegitcommit: e454c88823e3b42c50586e3f433b85ffd9185282
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/20/2022
ms.locfileid: "9543284"
---
# <a name="independent-software-vendor-isv-licensing-on-premises"></a>独立系ソフトウェア ベンダー (ISV) ライセンス (オンプレミス)

[!include [banner](../includes/banner.md)]

この記事では、独立系ソフトウェア ベンダー (ISV) ライセンスをオンプレミス配置にインポートする方法について説明します。

> [!IMPORTANT]
> この記事で説明するプロセスは、プラットフォーム更新プログラム 12 以降で展開されているオンプレミス環境のユーザーのみ利用できます。

ISV ライセンスの福利厚生についての一般情報、ソリューションのライセンスを有効にする方法についての情報、および自己署名証明書に関連するその他の情報については、[独立系ソフトウェア ベンダー (ISV) ライセンス](isv-licensing.md) を参照してください。

## <a name="generate-the-license-file"></a>ライセンス ファイルの生成

1. ライセンスを発行する顧客のテナント名と ID を収集します:

    1. 環境がホストされている Service Fabric Explorer のインスタンスに接続します。
    2. **クラスタ** &gt; **アプリケーション** &gt; **AXSFType** &gt; **ファブリック:\\AXSF** の順に移動し、次に右のページで、**詳細** タブを選択します。
    3. **パラメーター** テーブルで **License\_TenantDomainGuid** および **Licence\_TenantId** キーの値を検索します。

1. 顧客のライセンス (テナント ID と名前) を生成し、証明書のプライベート キーを使用してライセンスを登録します。 ライセンス ファイルを作成するには、次のパラメーターを  AXUtil **genlicense**  コマンドに渡す必要があります。 コマンドは XML ファイルを生成します。

    | パラメーター名  | 説明 |
    |-----------------|-------------|
    | ファイル            | ライセンス ファイルの名前。 |
    | licensecode     | Microsoft Visual Studio のライセンス コードの名前。 |
    | certificatepath | 証明書のプライベート キーのパス。 |
    | パスワード        | 証明書のプライベート キーのパスワード。 |
    | 顧客        | 顧客のテナント名。 |
    | serialnumber    | 顧客のテナント ID。 |
    | expirationdate  | オプション: ライセンスの有効期限。 |
    | usercount       | オプション: カスタム検証ロジックに必要となる可能性がある数値。 この数はユーザー数が可能ですが、ユーザーに限定されるものではありません。 |

    コマンドの例を次に示します。

    ```Console
    C:\AOSService\PackagesLocalDirectory\Bin\axutil genlicense /file:c:\templicense.txt /certificatepath:c:\tempisvcert.pfx /licensecode:ISVLicenseCode /customer:TAEOfficial.ccsctp.net /serialnumber:4dbfcf74-c5a6-4727-b638-d56e51d1f381 /password:********
    ```

## <a name="automated-import"></a>自動インポート

### <a name="prerequisites"></a>必要条件

- 環境は、Microsoft Dynamics 365 Finance + Operations (on-premises) バージョン 10.0.31 以降で配置またはサービスされます。
- 配置可能パッケージには、[運用環境用の独立系ソフトウェア ベンダ (ISV) ライセンス](isv-licensing.md#production-environments) に記載されているライセンス ファイルが含まれています。

### <a name="import-licenses"></a>ライセンスのインポート

環境および配置可能パッケージが前の前提条件を満たす場合、環境をサービスすると、ライセンスは自動的にインポートされます。 ライセンスのインポート手順は、データベースの同期の前に完了します。 したがって、この操作には追加のダウンタイムは不要になります。

## <a name="manual-import"></a>手動インポート

### <a name="prerequisites"></a>必要条件

オンプレミス環境に ISV ライセンス ファイルをインポートする前に、次の前提条件が満たされていることを確認します。

- 最新のバージョンのローカル エージェントは、環境が配置されたときに使用されました。
- 環境はプラットフォーム更新プログラム 12 で配置され、プラットフォーム更新プログラム 12 のすべての修正プログラムが適用されます。 Microsoft が ISV ライセンス シナリオの修正プログラムをリリースしたため、このステップは必須です。 最新の修正プログラムを入手するには、Microsoft Dynamics Lifecycle Services の **環境の詳細** ページでタイルを使用します。
- ISV ライセンスをインポートする前に、環境を展開し、Application Object Server (AOS) サービスを実行している必要があります。
- ISV ライセンスをインポートする前に、ISV ソリューションをオンプレミス環境に適用する必要があります。 ISV ソリューションは、配置フロー中に設置環境に適用できます。 または、Lifecycle Services の **更新プログラムの適用** フローを使用して配置後の手順として ISV ソリューションを適用することができます。 ライセンスをインポートする前に、ISV ソリューションが適用されていない場合、カスタマイズを使用できません。

### <a name="import-licenses"></a>ライセンスのインポート

オンプレミス プロジェクトに配置されているサンドボックス環境または運用環境では、次の手順を使用できます。

> [!NOTE]
> ISV ライセンスのインポートにはダウンタイムが必要なため、インポート時に環境内で業務トランザクションを実行することはできません。 インポートを実行するときは、システムを使用しているユーザがいないこと、公式ダウンタイム通知がすべてのユーザーに通知済みであることを確認してください。

1. 生成されたライセンスを fabric:/AXSF を実行しているマシンの 1 つのフォルダーにコピーし、fabric:/AXSF が正常であることを確認します。
1. AOS コンピューターのいずれかから **Import-LicensePackage.ps1** スクリプトを実行します。 このスクリプトは、Lifecycle Services 共有アセット ライブラリの **モデル** タブにある最新の **Microsoft Dynamics 365 Finance + Operations (on-premises)、配置スクリプト** フォルダーにあります。 次のパラメーターをスクリプトに渡す必要があります:

    - **LicenseFilesPath** – インポートする必要があるライセンス ファイルを含むフォルダーのパス。 
    - **SqlUser** – AOS を実行する credentials.json ファイルに指定されている同じユーザー。
    - **SqlPassword** – SQL への接続に使用できるパスワード。
    - **EnvironmentConfigPath** - 環境のコンフィギュレーション ファイル。 このファイルの名前は、config.json で、wp \\&lt; 環境名 &gt;\\ StandaloneSetup という形式のフォルダー内のエージェント共有の下にあります。

    コマンドを実行した後、ログ ファイルは、処理されるライセンス ファイルごとに生成されます。 ログ ファイルの名前は、{license\_file\_name}.output.log 形式と {license\_file\_name}.error.log 形式です。 データベース同期中に生成されるログは、dbsync.output.log および dbsync.error.log のような構造のファイルにあります。

    > [!NOTE]
    > インフラストラクチャ スクリプト 2.17.0 では、Import-LicensePackage.ps1 スクリプトは非推奨となり、自動フローが採用されました。 このスクリプトは、今後のリリースで削除される予定です。

1. スクリプトが正常に実行されたとき、コンフィギュレーション キーがインポートされて有効になっていることを検証します。 製品では、対応するコンフィギュレーション キーは、 **ライセンス コンフィギュレーション**  ページで使用可能になり、有効になります。 既定では、コンフィギュレーションが有効です。 たとえば、ISVConfigurationKey1 と呼ばれるコンフィギュレーション キーを追加した場合、コンフィギュレーション キーの一覧に表示されます。

コンフィギュレーション キーが有効になると、ISV ソリューションの変更は製品に表示されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

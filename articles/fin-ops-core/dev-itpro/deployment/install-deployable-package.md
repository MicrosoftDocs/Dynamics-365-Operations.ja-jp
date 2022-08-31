---
title: コマンド ラインから展開可能パッケージをインストールする
description: この記事では、コマンド ラインを使用して、バイナリ更新プログラムまたは環境で作成されたアプリケーション (AOT) 配置可能パッケージを適用する方法について説明します。
author: gianugo
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: gianura
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 24191
ms.assetid: 42d238d6-ff03-41b6-b2d5-c94bcdc37576
ms.openlocfilehash: a22e391f7501b810d41401d6a6273eec275374ce
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271475"
---
# <a name="install-deployable-packages-from-the-command-line"></a>コマンド ラインから展開可能パッケージをインストールする

[!include [banner](../includes/banner.md)]

この記事では、開発環境またはビルド環境で作成されたバイナリ更新プログラムまたはアプリケーション (AOT) の展開可能パッケージのいずれかをコマンド ラインを使用して適用する手順について説明します。

> [!IMPORTANT]
> ほとんどのタイプの環境については、配置可能パッケージを Microsoft Dynamics  Lifecycle Services (LCS) から直接環境に適用できます。 詳細については、[クラウド環境への更新プログラムの適用](apply-deployable-package-system.md)を参照してください。 したがって、この記事は主に、LCS による更新の適用をサポートしていない環境タイプに適用されます。 例としては、Microsoft Azure のローカル開発環境 (ダウンロード可能な仮想ハード ディスク [VHD])、マルチボックス開発/テスト環境 (LCS パートナーおよび試用プロジェクト) およびビルド環境があります。 ただし、LCS ではなくコマンド ラインを使用して展開可能パッケージをインストールする場合は、いつでもこの記事を使用することができます。

## <a name="key-concepts"></a>重要な概念
- **配置可能パッケージ** - 配置可能パッケージとは、任意の環境に適用できる配置の単位です。 Application Object Server (AOS)、更新されたアプリケーション パッケージ、または新しいアプリケーション パッケージのランタイム コンポーネントに対するバイナリの修正プログラムで構成できます。
- **AXUpdateInstaller** - AXUpdateInstaller は実行可能プログラムで、配置可能パッケージにバンドルされています。 パッケージがコンピューターにダウンロードされると、インストーラーを使用できます。
- **Runbook** – 展開ランブックは展開可能なパッケージを対象となる環境に適用させるために生成され、使われる一連の手順です。 ステップの一部が自動化され、一部は手動です。 AXUpdateInstaller は、これらの手順を一度に 1 つずつ正しい順序で実行できます。

## <a name="install-an-application-aot-deployable-package-on-a-development-environment"></a>開発環境でのアプリケーション (AOT) 配置可能パッケージのインストール
> [!NOTE]
> 次の手順は、カスタマイズ パッケージに対してのみ使用できます。 Microsoft Dynamics AX 2012 から財務と運用アプリへのアップグレードの一環として、データ アップグレード展開可能なパッケージを実行する場合は、**devinstall** パラメーターを使用しないでください。

AOT 配置可能パッケージはアプリケーションのカスタマイズおよび拡張機能を含むパッケージです。 開発またはデモ環境で AOT 配置可能パッケージをインストールするためだけにコマンド ラインを使用する場合、このセクションの指示に従います。 この記事の残りをスキップすることができます。

1. 仮想マシン (VM) で、配置可能パッケージの zip ファイルをダウンロードします。 非ユーザー フォルダーに zip ファイルが保存されていることを確認します。

    > [!NOTE]
    > ZIP ファイルをダウンロードした後、右クリックし **プロパティ** を選択します。 その後、**プロパティ** ダイアログ ボックスの **全般** タブで、**ブロック解除** を選択してファイルのロックを解除します。

2. ファイルを抽出します。
3. コマンド プロンプト ウィンドウを開き、配置可能パッケージを展開したフォルダーに移動します。
4. 次のコマンドを実行します。

    ```Console
    AXUpdateInstaller.exe devinstall
    ```

    **devinstall** オプションは、AOT の可能なパッケージを VM にインストールします。 
    
    > [!NOTE]
    > このコマンドは、データベース同期を実行しません。 配置可能なパッケージをインストールした後、Microsoft Visual Studio からデータベースの同期を実行する必要があります。

## <a name="collect-topology-configuration-data"></a>トポロジ コンフィギュレーション データを収集する
1. LCS で、**環境** ページの VM の名前を選択します。 **環境** ページで提供されているユーザー名とパスワードを使用して、VM へのリモート デスクトップの接続を確立します。
2. VM で、LCS から配置可能パッケージの zip ファイルをダウンロードします。 非ユーザー フォルダーに zip ファイルが保存されていることを確認します。

    > [!NOTE]
    > ZIP ファイルをダウンロードした後、右クリックし **プロパティ** を選択します。 その後、**プロパティ** ダイアログ ボックスの **全般** タブで、**ブロック解除** を選択してファイルのロックを解除します。
    
3. ファイルを抽出します。
4. 配置可能パッケージを展開したフォルダーで、**DefaultTopologyData.xml** というファイルを検索して開きます。 このファイルには、VM 名とインストール済みコンポーネントを指定する必要があります。

   - VM 名を指定するには、次の手順を実行します。

       1. ファイル エクスプローラーで、**この PC** を右クリックしてから、**プロパティ** を選択します。
       2. システム プロパティで、コンピューター名を検索して記録します (たとえば、**AOS 950ed2c3e7b**)。
       3. DefaultTopologyData.xml ファイルで、前の手順で示されているコンピューター名にマシン名を変更します。

   - インストールされたコンポーネントを指定するには、次の手順を実行します。

       1. 管理者としてコマンド プロンプト ウィンドウを開きます。
       2. 展開したフォルダーに移動し、コンピューターにインストールされているすべてのコンポーネントの一覧を表示するため、次のコマンドを実行します。

           ```Console
           AXUpdateInstaller.exe list
           ```

       3. コンポーネントの一覧で DefaultTopologyData.xml ファイルを更新します。

     VM 名とインストールされているコンポーネントの指定が完了したら、DefaultTopologyData.xml ファイルは次の図のようになります。
    
     ![トポロジ構成データ。](./media/defaulttopology.png)

5. **環境** ページに記載されているその他のすべて VM に対して 手順 1 ～ 4 を繰り返します。

## <a name="generate-a-runbook-from-the-topology"></a>トポロジから Runbook を生成します
DefaultTopologyData.xml ファイルのトポロジの情報に基づいて、各 VM の更新手順を示す Runbook ファイルを生成する必要があります。

- すべての VM で、次のコマンドを実行して Runbook を生成します。

    ```Console
    AXUpdateInstaller.exe generate -runbookid=[runbookID] -topologyfile=[topologyFile] -servicemodelfile=[serviceModelFile] -runbookfile=[runbookFile]
    ```

    このコマンドで使用されるパラメータの説明を次に示します。

  - **\[runbookID\]**- 配置可能パッケージを適用する開発者が指定するパラメータ。
  - **\[topologyFile\]**- DefaultTopologyData.xml ファイルのパス。
  - **\[serviceModelFile\]**- DefaultServiceModelData.xml ファイルのパス。
  - **\[runbookFile\]** - 生成する Runbook クファイルの名前 (たとえば、**AOSRunbook.xml**)。

    **例**

    ```Console
    AXUpdateInstaller.exe generate -runbookid="VAL200AA2BMEDIU-runbook" -topologyfile="DefaultTopologyData.xml" -servicemodelfile="DefaultServiceModelData.xml" -runbookfile="VAL200AA2BMEDIU-runbook.xml"
    ```

Runbook には、環境を更新するために実行する必要がある一連のステップが備わっています。 次の図は、Runbook ファイルの例を示します。 Runbook の各ステップは、ID、マシン名、およびステップ実行の詳細に関連付けられます。

[![Runbook ファイルの例。](./media/runbook-steps-1024x624.jpg)](./media/runbook-steps.jpg)

## <a name="install-a-deployable-package"></a>配置可能パッケージのインストール
1. Runbook ファイルに記載されている最初のマシン (VM) で、次の手順に従います。

    1. 次のコマンドを実行して、Runbook をインポートします。

        ```Console
        AXUpdateInstaller.exe import -runbookfile=[runbookFile]
        ```

        **例**

        ```Console
        AXUpdateInstaller.exe import -runbookfile="VAL200AA2BMEDIU-runbook.xml"
        ```

    2. Runbook を確認します。

        ```Console
        AXUpdateInstaller.exe list
        ```

    3. runbook を実行します。

        ```Console
        AXUpdateInstaller.exe execute -runbookid=[runbookID]
        ```

        **例**

        ```Console
        AXUpdateInstaller.exe execute -runbookid="VAL200AA2BMEDIU-runbook"
        ```

        AXUpdateInstaller は、各ステップが VM で実行された後に Runbook ファイルを更新します。 Runbook には、各ステップに関する情報も記録されます。

        手動ステップについては、指示に従い、Runbook でステップを完了済とマークする以下のコマンドを実行します。

        ```Console
        AXUpdateInstaller.exe execute -runbookID=[runbookID] -setstepcomplete=[stepID]
        ```

        **例**

        ```Console
        AXUpdateInstaller.exe execute -runbookid="VAL200AA2BMEDIU-runbook" -setstepcomplete=2
        ```

        どの段階中でもエラーが発生した場合は、そのステップのスクリプトまたは指示をデバッグし、それに応じて更新します。

    4. Runbook をエクスポートします。

        ```Console
        AXUpdateInstaller.exe export -runbookid=[runbookID] -runbookfile=[runbookFile]
        ```

        **例**

        ```Console
        AXUpdateInstaller.exe export -runbookid="VAL200AA2BMEDIU-runbook" -runbookfile="VAL200AA2BMEDIU-runbook.xml"
        ```

2. Runbook ファイルに記載されているその他のすべての VM で手順 1 を繰り返します。 1 ボックス環境では、開発、構築、およびデモ環境など、1 つの VM のみがあります。

## <a name="verify-installation"></a>インストールの確認
1. 新しい更新プログラムがインストールされていることを確認するには、次のコマンドを実行します。

    ```Console
    AXUpdateInstaller.exe list
    ```

2. Runbook を表示して、完了したステップを確認します。 手順が完了した runbook ファイルの例を次に示します。

    [![Runbook の完了したステップの例。](./media/image013-1024x978.png)](./media/image013.png)

## <a name="backup-the-runbook-file"></a>Runbook ファイルをバックアップします
- Runbook のすべての手順を完了した後、Runbook をエクスポートし、後で参照できるようにファイルをコンピューターの外部に保存します。 たとえば、このような状況で Runbook ファイルを使用する必要が生じる場合があります。

    - 生産などのダウンタイム要件を分析する必要があります。
    - 配置可能パッケージをインストールすることはできないため、マイクロソフトにファイルを送信する必要があります。

## <a name="troubleshooting"></a>トラブルシューティング
- runbook の段階で失敗した場合は、次のコマンドを実行して再実行できます。

    ```Console
    AXUpdateInstaller.exe execute -runbookid=[runbookID] -rerunstep=[stepID]
    ```

- バージョンの不一致やダウングレード、または同じ展開可能パッケージのインストールを防止するには、次のコマンドを実行します。

    ```Console
    AXUpdateInstaller.exe execute -runbookid=[runbook ID] -versioncheck=true
    ```

- データベースの同期を確認するには **aosservice\\scripts\\** フォルダー内の **dbsync.error.txt** ファイルを見つけて開き、エラーを探します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

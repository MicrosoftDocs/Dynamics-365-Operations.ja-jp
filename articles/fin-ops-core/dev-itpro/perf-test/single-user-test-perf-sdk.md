---
title: パフォーマンス SDK とタスク レコーダーによるシングルユーザー テスト
description: この記事では、Microsoft Visual Studio、パフォーマンス SDK、およびタスク レコーダー パフォーマンス テスト スクリプトを使用してシングルユーザー テストを行う方法について説明します。
author: josaw1
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.openlocfilehash: 40828ce6b4fbea235b1606de5d7d1a159b91c80c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278397"
---
# <a name="single-user-testing-using-performance-sdk-and-task-recorder"></a>パフォーマンス SDK とタスク レコーダーによるシングルユーザー テスト

[!include [banner](../includes/banner.md)]

Visual Studio および パフォーマンス ソフトウェア開発キット (SDK) を使用し、タスク レコーダーにて生成されたパフォーマンス テスト スクリプトとともシングルユーザー テストを行うには、この記事にある情報を使用してください。

> [!IMPORTANT]
> Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。
> + Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。 そのサポート サイクルが終了するまで継続して使用することができます。 
> + 詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。

## <a name="use-task-recorder-to-define-and-record-an-end-to-end-business-scenario"></a>タスクレコーダーを使用してエンドツーエンドの業務シナリオを定義し、記録します。

シングルユーザーテストを実行する前に、業務チームと協力してエンドツーエンドのシナリオを定義した上で、タスクレコーダーを使用して各シナリオのステップを記録することを強く推奨します。 タスク記録の作成方法についての詳細は、[タスク レコーダー リソース](../user-interface/task-recorder.md)を参照してください。 テストを行うべきシナリオは、顧客の業務要件によって異なります。 この記事では、「販売注文の作成および確認」を行うサンプルシナリオを使用します。

1. 財務担当者ペルソナとしてサインインします。
2. タスクレコーダー を有効にして、次の情報を含む販売注文の作成と確認を行います。

    - 顧客口座
    - 品目番号
    - 販売数量
    - サイト
    - 倉庫
    - 販売価格

3. 完了後、 **開発者記録として保存** を選択してXMLファイルをダウンロードします。

## <a name="configure-a-development-environment"></a>開発環境のコンフィギュレーション

1. [selenium-dotnet-strongnamed-3.13.1.zip](https://selenium-release.storage.googleapis.com/index.html?path=3.13/) と [IEDriverServer\_Win32\_3.13.0.zip](https://selenium-release.storage.googleapis.com/index.html?path=3.13/) をダウンロードします。
2. ファイルのブロックを解除し、解凍します。
3. **解凍先** のフォルダーで、. nupkgファイルを .zipファイルとして名前を変更し、解凍します。

    | 元のファイル名                          | 新しいファイル名                             |
    |---------------------------------------------|-------------------------------------------|
    | Selenium.Support.StrongNamed.3.13.1.nupkg   | Selenium.Support.StrongNamed.3.13.1.zip   |
    | Selenium.WebDriver.StrongNamed.3.13.1.nupkg | Selenium.WebDriver.StrongNamed.3.13.1.zip |

4. **PerfSDK** フォルダ配下に、 **Common\\External\\Selenium** というフォルダを作成します。

    [![新しい PerfSDK フォルダー。](./media/single-user-test-03.png)](./media/single-user-test-03.png)

5. 次のファイルをコピーして、上記の手順で作成したフォルダー **Common\\External\\Selenium** に保存します。

    - IEDriverServer\_Win32\_3.13.0.zip ファイルを解凍後に取得できる、IEDriverServer.exe
    - Selenium.WebDriver.StrongNamed.3.13.1.zip ファイルを解凍後に生成される、lib\\net45 フォルダ内の、WebDriver.dll と WebDriver.xml
    - Selenium.Support.StrongNamed.3.13.1.zip ファイルを解凍後に生成される、lib\\net45 フォルダ内の WebDriver.Support.dll と WebDriver.Support.xml

## <a name="generate-a-c-performance-test-from-task-recorder"></a>タスクレコーダーから C\# パフォーマンステストを生成する

エンドツーエンドのシナリオの記録が完了後、タスクレコーディングをもとに C\# パフォーマンス テスト スクリプトを生成する必要があります。 

1. 開発環境では、Microsoft Visual Studio を管理者権限で開きます。
2. **PerfSDK** フォルダから、 **PerfSDKSample** ソリューションを開きます。 Tier1 サンドボックス、またはクラウドホスト環境では、PerfSDKフォルダは一般的に \<Service volume\>:\\PerfSDK\\PerfSDKLocalDirectory にあります。

    [![PerfSDK ディレクトリ。](./media/single-user-test-05.png)](./media/single-user-test-05.png)

3. Common\\External\\Selenium フォルダー内の WebDriver.dll への参照を追加します。

    [![PerfSDKSample 参照。](./media/single-user-test-06.png)](./media/single-user-test-06.png)

4. **Dynamics 365** メニューにて **アドイン** を指定し、 **記録から C\# パフォーマンステストを作成** を選択します。
5. **タスクの記録をインポートする** ダイアログ ボックスで、以下の必要な詳細を入力します:

    - **レコーディングパス** エンドツーエンドシナリオにおける開発者記録ファイルの場所。
    - **プロジェクト** のパス: PerfSDKSampleプロジェクトの場所。 通常、パスは \<Your\_PerfSDK\_Folder\>\\SampleProject\\PerfSDKSample\\PerfSDKSample.csproj です。
    - **PerfSDKのパス** – PerfSDK の場所。 通常、パスは \<ServiceVolumeDrive\>\\PerfSDK\\PerfSDKLocalDirectory です。
    
6. 完了後、 **インポート** を選択します。 PerfSDKSample プロジェクトの **生成された** フォルダ配下に新しいC\# クラスが作成されます。

    [![生成されたフォルダ内の新しい C# クラス。](./media/single-user-test-09.png)](./media/single-user-test-09.png)

7. ソリューションをビルドします。

## <a name="run-single-user-testing-by-using-test-explorer-in-visual-studio"></a>Visual Studioの テストエクスプローラー を使用したシングル ユーザー テストの実行

1. 以下に示す方法で PerfSDKSample プロジェクトの **CloudEnvironment.config** ファイルを更新します。これにより、ご利用の環境の設定が反映されます。

    - **HostName** と **SOAPHostName** が開発環境と一致することを確認します。
    - **SelfMintingAdminUser** の **UserName** が開発環境の管理者アカウントと一致していることを確認してください。
    - **AuthenticatorConfigurationCollection** 要素の配下にある **AuthenticatorConfiguration** の各要素を **AadAuthenticator** を **selfmintedtokenauthenticator** に置き換えます。
    - **AzureActiveDirectoryConfiguration** 要素と **KeyVaultConfigurations** 要素をコメント行にします。

    [![更新およびコメントされたコードのサンプル。](./media/single-user-test-10.png)](./media/single-user-test-10.png)

2. Visual Studioの **テスト** メニューにて、 **Windows** を指定し、 **テストエクスプローラー** を選択します。
3. 実施したテストケースを右クリックし、 **選択したテストの実行** を選択します。

## <a name="tips-and-tricks"></a>ヒントや秘訣

タスクレコーダーとパフォーマンスSDKを使用したシングルユーザーテストには、以下のヒントと秘訣を参照してください。

- タスク レコーダーを使用して業務を取り込む前に、エンドツーエンドの業務シナリオを最初に実行します。
- タスクレコーダーを使用してシナリオを記録する場合は、ドロップダウンリストから値を選択するのではなく、手動で値を入力します。
- 記録したタスクを再生し、すべてが期待どおりに動作することを確認してください。
- ソリューションをビルド後にテストケースが表示されない場合は、 Visual Studio を再起動します。

## <a name="troubleshooting"></a>トラブルシューティング

パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: タスクレコーダーおよびパフォーマンスSDKを使用したシングルユーザーテスト
description: このトピックでは、Microsoft Visual Studio、パフォーマンス SDK、およびタスク レコーダー パフォーマンス テスト スクリプトを使用してシングルユーザー テストを行う方法について説明します。
author: hasaid
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb8d17d46986bc9c15d7a0dfd8e547e6bdeaf728
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092355"
---
# <a name="single-user-testing-with-task-recorder-and-the-performance-sdk"></a>タスク レコーダーおよびPerformance SDK を使用したシングル ユーザー テスト

[!include [banner](../includes/banner.md)]

Visual Studio および パフォーマンス ソフトウェア デベロップメント キット (SDK) を使用し、タスク レコーダーにて生成されたパフォーマンス テスト スクリプトとともシングルユーザーテストを行うには、このトピックに記載の内容を参考にしてください。

 > [!IMPORTANT]
  > Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。 将来的に、代替ソリューションの推奨を公開します。  
  > - Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。 そのサポート サイクルが終了するまで継続して使用することができます。 
  > - クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。 それまでの間は、同サービスの全機能を継続してご利用いただけます。 また、オンプレミス負荷テストに切り替えることがも可能です。 詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。
## <a name="prerequisites"></a>必要条件

このトピックで扱う手順を完了するには、プラットフォーム更新プログラム 21、またはそれ以降が設定された開発環境を用意する必要があります。
> [!IMPORTANT]
> Finance and Operations アプリが 21Vianet に配置されている場合は、10.0.11 またはそれ以降のプラットフォーム更新で開発する必要があります。

## <a name="use-task-recorder-to-define-and-record-an-end-to-end-business-scenario"></a>タスクレコーダーを使用してエンドツーエンドの業務シナリオを定義し、記録します。

シングルユーザーテストを実行する前に、業務チームと協力してエンドツーエンドのシナリオを定義した上で、タスクレコーダーを使用して各シナリオのステップを記録することを強く推奨します。 タスク記録の作成方法についての詳細は、[タスク レコーダー リソース](../user-interface/task-recorder.md)を参照してください。 テストを行うべきシナリオは、顧客の業務要件によって異なります。 このトピックでは、「販売注文の作成および確認」を行うサンプルシナリオを使用します。

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

    [![新規PerfSDKフォルダ](./media/single-user-test-03.png)](./media/single-user-test-03.png)

5. 次のファイルをコピーして、上記の手順で作成したフォルダー **Common\\External\\Selenium** に保存します。

    - IEDriverServer\_Win32\_3.13.0.zip ファイルを解凍後に取得できる、IEDriverServer.exe
    - Selenium.WebDriver.StrongNamed.3.13.1.zip ファイルを解凍後に生成される、lib\\net45 フォルダ内の、WebDriver.dll と WebDriver.xml
    - Selenium.Support.StrongNamed.3.13.1.zip ファイルを解凍後に生成される、lib\\net45 フォルダ内の WebDriver.Support.dll と WebDriver.Support.xml

## <a name="generate-a-c-performance-test-from-task-recorder"></a>タスクレコーダーから C\# パフォーマンステストを生成する

エンドツーエンドのシナリオの記録が完了後、タスクレコーディングをもとに C\# パフォーマンス テスト スクリプトを生成する必要があります。 

1. 開発環境では、Microsoft Visual Studio を管理者権限で開きます。
2. **PerfSDK** フォルダから、 **PerfSDKSample** ソリューションを開きます。 Tier1 サンドボックス、またはクラウドホスト環境では、PerfSDKフォルダは一般的に \<Service volumne\>:\\PerfSDK\\PerfSDKLocalDirectory にあります。

    [![PerfSDKディレクトリ](./media/single-user-test-05.png)](./media/single-user-test-05.png)

3. Common\\External\\Selenium フォルダー内の WebDriver.dll への参照を追加します。

    [![PerfSDKSample 参照](./media/single-user-test-06.png)](./media/single-user-test-06.png)

4. **Dynamics 365** メニューにて **アドイン** を指定し、 **記録から C\# パフォーマンステストを作成** を選択します。
5. **タスクの記録をインポートする** ダイアログ ボックスで、以下の必要な詳細を入力します:

    - **レコーディングパス** エンドツーエンドシナリオにおける開発者記録ファイルの場所。
    - **プロジェクト** のパス: PerfSDKSampleプロジェクトの場所。 通常、パスは \<Your\_PerfSDK\_Folder\>\\SampleProject\\PerfSDKSample\\PerfSDKSample.csproj です。
    - **PerfSDKのパス** – PerfSDK の場所。 通常、パスは \<ServiceVolumeDrive\>\\PerfSDK\\PerfSDKLocalDirectory です。
    
6. 完了後、 **インポート** を選択します。 PerfSDKSample プロジェクトの **生成された** フォルダ配下に新しいC\# クラスが作成されます。

    [![生成されたフォルダ内の新しいC#クラス](./media/single-user-test-09.png)](./media/single-user-test-09.png)

7. ソリューションをビルドします。

## <a name="run-single-user-testing-by-using-test-explorer-in-visual-studio"></a>Visual Studioの テストエクスプローラー を使用したシングル ユーザー テストの実行

1. 以下に示す方法で PerfSDKSample プロジェクトの **CloudEnvironment.config** ファイルを更新します。これにより、ご利用の環境の設定が反映されます。

    - **HostName** と **SOAPHostName** が開発環境と一致することを確認します。
    - **SelfMintingAdminUser** の **UserName** が開発環境の管理者アカウントと一致していることを確認してください。
    - **AuthenticatorConfigurationCollection** 要素の配下にある **AuthenticatorConfiguration** の各要素を **AadAuthenticator** を **selfmintedtokenauthenticator** に置き換えます。
    - **AzureActiveDirectoryConfiguration** 要素と **KeyVaultConfigurations** 要素をコメント行にします。

    [![更新およびコメント化されたコードのサンプル](./media/single-user-test-10.png)](./media/single-user-test-10.png)

2. Visual Studioの **テスト** メニューにて、 **Windows** を指定し、 **テストエクスプローラー** を選択します。
3. 実施したテストケースを右クリックし、 **選択したテストの実行** を選択します。

## <a name="tips-and-tricks"></a>ヒントや秘訣

タスクレコーダーとパフォーマンスSDKを使用したシングルユーザーテストには、以下のヒントと秘訣を参照してください。

- タスクレコーダーを使用して業務を取り込む前に、エンドツーエンドの業務シナリオを最初に実行します。
- タスクレコーダーを使用してシナリオを記録する場合は、ドロップダウンリストから値を選択するのではなく、手動で値を入力します。
- 記録したタスクを再生し、すべてが期待どおりに動作することを確認してください。
- ソリューションをビルド後にテストケースが表示されない場合は、 Visual Studio を再起動します。

## <a name="troubleshooting"></a>トラブルシューティング

パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
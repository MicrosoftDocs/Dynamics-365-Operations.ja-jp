---
title: パフォーマンス SDK と Azure DevOps を使用したマルチユーザー テスト
description: このトピックでは、Microsoft Azure DevOps、パフォーマンス SDK、およびタスク レコーダー パフォーマンス テスト スクリプトを使用してマルチユーザー テストを行う方法について説明します。
author: hasaid
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 9954
ms.assetid: 7b605810-e4da-4eb8-9a26-5389f99befcf
ms.search.region: Global
ms.author: jujoh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aec5c9350c0195fc1355207dcd694afbeb4337e2
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865946"
---
# <a name="multi-user-testing-with-the-performance-sdk-and-azure-devops"></a>パフォーマンス SDK および Azure DevOps を使用したマルチ ユーザー テスト

[!include [banner](../includes/banner.md)]

  > [!IMPORTANT]
  > Visual Studio 2019は Visual Studio の最新バージョンです。webパフォーマンスと負荷機能テストを実装しています。 将来的に、代替ソリューションの推奨を公開します。  
  > - Visual Studio および、オンプレミスでの負荷テストに向けたテストコント ローラー/テストエージェントをご利用の場合、 Visual Studio 2019が最新のバージョンになります。 そのサポート サイクルが終了するまで継続して使用することができます。 
  > - クラウド ベースの負荷テストサービスをご利用の場合、同サービスは 2020 年 3 月 31 日まで継続してご利用いただけます。 それまでの間は、同サービスの全機能を継続してご利用いただけます。 また、オンプレミス負荷テストに切り替えることがも可能です。 詳細については、 [クラウド ベース 負荷テストサービスの終了について](https://devblogs.microsoft.com/devops/cloud-based-load-testing-service-eol/) をご参照ください。

## <a name="prerequisites"></a>必要条件

このトピックの手順を完了する前に、次の前提条件が満たされていることを確認してください:

- 自身の Microsoft Azure サブスクリプションに、プラットフォーム更新プログラム 21 以降の開発環境があります。
- 開発環境には Microsoft Visual Studio Enterprise Edition があります。
- 開発環境と同じリリース (アプリケーション バージョンとプラットフォーム更新プログラム) の階層 2 以上のサンドボックスがあります。
- [タスク レコーダーおよびパフォーマンス SDK を使用したシングル ユーザー テスト](single-user-test-perf-sdk.md) のすべての手順と、 [パフォーマンス SDK およびローカル テスト コントローラーを使用したマルチ ユーザー テスト](multi-user-testing-local-test-controller.md) の "ローカル テスト コントローラーを使用したマルチユーザー テストの実行" を除くすべての手順を完了しました。

## <a name="prepare-the-perfsdksample-solution-for-multi-user-testing"></a>マルチユーザー テスト用の PerfSDKSample ソリューションの準備

1. 開発環境で Microsoft Visual Studio を Azure DevOps プロジェクトに接続します。

    [![[Team Foundation Serverに 接続] ダイアログ ボックス](./media/perfsdk-azuredevops-01.png)](./media/perfsdk-azuredevops-01.png)

    > [!NOTE]
    > Azure DevOps サーバーを追加する場合は、**https://\<YourAzureDevOpsAccount\>.visualstudio.com** を使用します。

2. Azure DevOps プロジェクト ダッシュボードで **Visual Studio で開く** を選択し、**プロンプト ウィンドウで許可** を選択します。

    [![Azure プロジェクト ダッシュボード](./media/perfsdk-azuredevops-02.png)](./media/perfsdk-azuredevops-02.png)

3. Visual Studio が開いたら、管理者として実行していることを確認します。そうでない場合は、それを閉じて管理者として再度開いてください。
4. K:\PerfSDK\PerfSDKLocalDirectory\SampleProject に移動して、ファイル、**vsonline.testsettings** を変更します。
5. **テストの設定** ダイアログ ボックスの **一般** タブで、**Visual Studio Team Services を使用したテストの実行** オプションを選択します。
6. **配置** タブで、 すべてのフィールド設定を [パフォーマンス SDK およびローカル テスト コントローラーを使用したマルチ ユーザー テスト](multi-user-testing-local-test-controller.md) で設定したままにします。

    [![配置タブ](./media/perfsdk-azuredevops-04.png)](./media/perfsdk-azuredevops-04.png)

7. **設定とクリーンアップ スクリプト** タブで、 **Visual Studio Online** フォルダの **setup.cmd** ファイルへ **設定スクリプト** フィールドをポイントします。

    [![設定とクリーンアップ スクリプト タブ](./media/perfsdk-azuredevops-05.png)](./media/perfsdk-azuredevops-05.png)

8. **追加設定** タブで、すべてのフィールド設定を [パフォーマンス SDK およびローカル テスト コントローラーを使用したマルチ ユーザー テスト](multi-user-testing-local-test-controller.md) で設定したままにします。

    [![追加設定タブ](./media/perfsdk-azuredevops-06.png)](./media/perfsdk-azuredevops-06.png)

9. **適用して閉じる** を選択します。

## <a name="run-multi-user-testing-by-using-azure-devops"></a>Azure DevOps を使用したマルチユーザー テストの実行

1. Visual Studio で **SampleLoadTest.loadtest** を開きます。
2. **負荷テストの実行** を選択します。

    [![負荷テストの実行オプション](./media/perfsdk-azuredevops-07.png)](./media/perfsdk-azuredevops-07.png)

    負荷テストが実行され、グラフに進行状況が表示されます。    
   
   [![SampleLoadTestLoadTest の進行状況グラフ](./media/perfsdk-azuredevops-08.png)](./media/perfsdk-azuredevops-08.png)

    [![SampleLoadTestLoadTest の進行状況グラフの続行](./media/perfsdk-azuredevops-09.png)](./media/perfsdk-azuredevops-09.png)

3. テスト出力を確認します。

    [![テスト出力画面 1](./media/perfsdk-azuredevops-10.png)](./media/perfsdk-azuredevops-10.png)

    [![テスト出力画面 2](./media/perfsdk-azuredevops-11.png)](./media/perfsdk-azuredevops-11.png)

    [![テスト出力画面 3](./media/perfsdk-azuredevops-12.png)](./media/perfsdk-azuredevops-12.png)

## <a name="tips"></a>ヒント

ローカル テスト コントローラーと Azure DevOps 間でマルチユーザー テストを切り替えるには、それぞれに **testsettings** のコピーを作成して **有効なテストの設定** として必要なコピーを選択します。

## <a name="troubleshooting"></a>トラブルシューティング

パフォーマンス SDK を使用するシングル ユーザーまたはマルチ ユーザーのテストの詳細については、[パフォーマンス SDK によるシングルユーザーまたはマルチユーザーのテストに関するトラブルシューティングガイド](troubleshoot-perf-sdk-user-testing.md) を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
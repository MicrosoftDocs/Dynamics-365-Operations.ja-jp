---
title: バージョン 10.0.10 から 10.0.13 における開発と ALM の変更
description: このトピックでは、開発ツール、ソフトウェア開発キット (SDK)、およびアプリケーション ライフサイクル管理 (ALM) の主要な変更点について説明します。
author: RobBertram
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2020-04-10
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: ccead497c5c87a036b799e87525c54ff2e156bb5
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128377"
---
# <a name="development-and-alm-changes-from-version-10010-to-10013"></a>バージョン 10.0.10 から 10.0.13 における開発と ALM の変更

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Commerce 環境の管理者は、更新を一時停止してから現在のバージョンに切り替えるのが一般的です。 このトピックは、安全に起動するために役立ちます。 開発ツールおよびビルド ツールには、大幅な変更や更新があります。

Microsoft は、互換性に影響する変更を含まない更新を提供するよう努めているため、これらの変更のためにカスタマイズをリファクタリングする必要はありません。 ベスト プラクティスのパターンに従い、以前のバージョンで開発されたカスタマイズを、最新サービスの更新プログラムに配置することができます。

## <a name="who-should-read-this-topic"></a>このトピックを読む必要のあるユーザー

技術上の役割 (開発者、管理者、またはマネージャー) を担っていて、Dynamics 365 Commerce を使用している場合は、このトピックを引き続きお読みください。 大幅な改善と変更があり、変更内容と他にどのような変更が予定されているかを説明する情報やドキュメントが豊富に用意されています。 このトピックの目的は、すべての情報を 1 つの場所にまとめることで、開発環境を更新したり、アプリケーション ライフサイクル管理 (ALM) プロセスを調整したりするための特定の変更についてより深く理解していただくことです。

## <a name="overall-improvements-changes-and-notes"></a>全体的な改善点、変更点、および注記

次の機能は、製品およびユーザー全体で使用できます。 すべてのバージョンに適用される機能と、バージョン 10.0.10 以降でのみ適用される機能があります。

- X++ の[オールインワン配置可能パッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md) は、すべてのカスタム コードと独立系ソフトウェア ベンダー (ISV) モデルを 1 つのカスタム パッケージに結合します。

    - バージョン 10.0.10 以降では、カードが存在しないカスタム支払コネクタを配置可能パッケージに含めることができます。
    - バージョン 10.0.13 では、オールインワン パッケージが **必須** になります。

- [Retail ソフトウェア開発キット (SDK)](retail-sdk/retail-sdk-overview.md) を使用して作成されたコマース配置可能パッケージは、アプリケーション オブジェクト サーバー (AOS) から除かれました。 代わりに、セルフサービス インストーラーを Microsoft Dynamics Lifecycle Services (LCS) にアップロードし、同期を使用します。 詳細については、「[Dynamics 365 Commerce のセルフサービス インストーラーの同期](synchronize-installers.md)」を参照してください。
- 次の目的では、専用ビルド マシンの代わりに、Microsoft によってホストされるビルド エージェントを使用します。

    - [アプリケーション配置可能パッケージ](../../fin-ops-core/dev-itpro/dev-tools/hosted-build-automation.md) をビルドする
    - [コマース配置可能パッケージ](retail-sdk/sdk-build-pipeline.md) をビルドする

    > [!NOTE]
    > ビルド エージェントを使用することで、Azure の消費が増えます。 ただし、専用のビルド サーバーを廃止できる場合は、コスト削減につながります。

各アプリケーション リリースの全般的な概要については、「新機能および変更された機能」のトピックを必ず確認してください。

- [Finance and Operations アプリ ホーム ページの新機能および変更された機能](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-changed?toc=/dynamics365/commerce/toc.json)
- [Dynamics 365 Commerce での新機能と変更](../get-started/whats-new-home-page.md)
- [プラットフォーム更新の新機能と変更された機能](../../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md)

## <a name="whats-changed-in-the-10010-release"></a>10.0.10 リリースの変更された機能

- カードが存在しないカスタム支払コネクタを X++ アプリケーション配置可能パッケージにネイティブに含めることができます。 詳細については、「[オールインワン配置可能パッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md)」を参照してください。
- セルフサービス インストーラーを LCS にアップロードし、同期を使用します。 詳細については、「[Dynamics 365 Commerce のセルフサービス インストーラーの同期](synchronize-installers.md)」を参照してください。

    > [!NOTE]
    > インストーラーをアップロードするプロセスは、手動プロセスです。 ただし、Microsoft は新しい Commerce 資産のタイプを [Dynamics 365 Finance and Operations の DevOps パイプライン ツール](https://marketplace.visualstudio.com/items?itemName=Dyn365FinOps.dynamics365-finops-tools) に組み込むことで、LCS へのアップロードを自動化できるよう取り組んでいます。

- 配置可能カスタム小売パッケージには、Adyen 支払ダイナミック リンク ライブラリ (DLL) を含める必要がなくなりました。

## <a name="whats-changed-in-the-10011-release"></a>10.0.11 リリースの変更された機能

- Retail SDK が Visual Studio 2017 に更新されました。 Visual Studio 2015 は、開発者向けの事前に構成された仮想マシン (VM) 用のテンプレートにインストールされます。 ただし、Retail SDK をビルドするには、Visual Studio 2017 がインストールされている必要があります。 したがって、[Visual Studio を手動で更新](retail-sdk/migrate-sdk.md#migrate-to-the-sdk-for-visual-studio-2017) して Retail SDK をリビルドする必要があります。

    Microsoft は、開発およびテスト環境のプロビジョニングに使用されるバーチャル ハード ディスク (VHD) テンプレートのリビルドに取り組んでいます。 この作業が完了すると、VHD テンプレートには Visual Studio 2017 が自動的に含まれます。 リビルドされたテンプレートが利用可能になる日付は確認されていませんが、Microsoft は、バージョン 10.0.13 が 2020 年 9 月に一般公開された後には準備が整うと予想しています。 詳細については、「[必要なアクション - .NET バージョン と Visual Studio 2017](https://community.dynamics.com/365/financeandoperations/b/newdynamicsax/posts/action-required---net-version-and-visual-studio-2017)」を参照してください。

    - Visual Studio 拡張機能をインストールすることにより、Visual Studio ツールをインストールします。 拡張機能をダウンロードするには、これらの手順に従います。

        1. LCS の共有アセット ライブラリから最新のサービス更新パッケージをダウンロードします。 このパッケージは ZIP ファイルです。
        2. ZIP ファイルを開いて、**DevToolsService\\Scripts** フォルダーを検索します。 
        3. **Script** フォルダーをローカル コンピューターに抽出します (例えば、**K:\\Temp\\Scripts**)。
        4. **Microsoft.Dynamics.Framework.Tools.Installer.vsix** ファイルを検索します。 このファイルのサイズは、約 150 メガバイト (MB) にする必要があります。
        5. ファイルを右クリックして、**開く** を選択します。

            ![Visual Studio 2017 Dynamics 365 拡張機能のインストーラーを開いています](media/vs2017-extensions.png)

        詳細については、「[Visual Studio 開発ツールの更新](../../fin-ops-core/dev-itpro/dev-tools/update-development-tools.md)」を参照してください。

    - Retail SDK をリビルドします。

        1. 変更されていないバージョン 10.0.11 の Retail SDK を含むフォルダーに移動します。
        2. Retail SDK の保管用のバックアップ コピーを作成します。
        3. Visual Studio 2017を管理者として開き、SDK フォルダーの各標準ソリューション ファイルを開きます。 おそらく、Visual Studio が終了して再び開始すること、およびコンピューターの再起動が必要であることを示すメッセージが表示されます。 **続行** を選択します。
        4. Visual Studio 2017のコマンド プロンプト ウィンドウを管理者として開き、正しいバージョンの Visual Studio 開発者コマンド プロンプトを使用していることを確認します。 Visual Studio 2017 は、開発者コマンド プロンプトのバージョン 15 を使用します (Visual Studio 2015 はバージョン 14 を使用します)。 バージョン番号がコマンド ウィンドウに表示されます。
        5. 標準 SDK をコンパイルできることを確認します。 **RetailSDK** フォルダーのルートに移動し、次のコマンドを実行します。

            ```plaintext
            msbuild /t:rebuild
            ```

        ビルドに失敗した場合は、前の手順のいずれかを省略している可能性があります。

- PackageReference (NuGet パッケージ参照) への参照が更新されます。 この変更により、プロジェクト参照を管理しやすくなりました。 また、この変更により、Retail SDK の *すべて* のカスタム プロジェクトを手動で更新する必要があります。 1 プロジェクトあたり約 5 分かかると予測されます。 標準プロジェクトがどのように更新されたかを確認し、それらの更新をモデルとして使用します。

    1. すべてをコンパイルできること、およびローカルの開発者コンピューターからパッケージを作成できることを確認してください。
    2. ビルド サーバーが Visual Studio 2017 に更新されていることを確認してください。

    > [!WARNING]
    > NuGet 参照フォルダーの名前が非常に長く、ファイル パスの制限値である 260 文字を超えるため、ビルド サーバーが失敗する可能性があります。

- Retail SDK ファイルサイズ: 変更されていない配置可能小売パッケージのサイズは現在、約 340 MB です。 カスタマイズが含まれている場合、ファイル サイズが 350 MB に増加する可能性があります。 Commerce Scale Unit (クラウド) (以前は Retail Cloud Scale Unit \[RCSU\] と呼ばれていた) にファイルを配置しようとすると、[300 MB を超えるパッケージ](retail-sdk/retail-sdk-packaging.md#deploy-the-packages) は配置できないことを示すエラー メッセージが表示されます。 この問題を解決するには、次の手順に従ってください。

    1. 「[配置可能パッケージの配置](retail-sdk/retail-sdk-packaging.md#deploy-the-packages)」の手順に従って、セルフサービス インストーラー ファイルを手動で削除します。
    2. より小さなパッケージを LCS にアップロードし、通常どおりに配置を続行します。

    > [!NOTE]
    > 配置可能パッケージに埋め込まれているビルド & デプロイ スクリプトは、セルフサービス インストーラーをチェックするためにハードコーディングされています。

## <a name="whats-changed-in-the-10012-release"></a>10.0.12 リリースの変更された機能

- より簡単に[コマース プロキシ](typescript-proxy-retail-pos.md) を生成することができます。

## <a name="whats-changed-in-the-10013-release"></a>10.0.13 リリースの変更された機能

- バージョン 10.0.13 では、X++ を使用するアプリケーション開発には Visual Studio 2017 が必要です。 まだ Visual Studio 2017 に更新していない場合は、このトピックで前述したバージョン 10.0.11 に関するセクションを確認してください。
- Microsoft は、開発およびテスト環境のプロビジョニングに使用される VHD テンプレートのリビルドに取り組んでいます。 この作業が完了すると、VHD テンプレートには Visual Studio 2017 が自動的に含まれます。 リビルドされたテンプレートが利用可能になる日付は確認されていませんが、Microsoft は、バージョン 10.0.13 が 2020 年 9 月に一般公開された後には準備が整うと予想しています。 詳細については、「[必要なアクション - .NET バージョン と Visual Studio 2017](https://community.dynamics.com/365/financeandoperations/b/newdynamicsax/posts/action-required---net-version-and-visual-studio-2017)」を参照してください。

## <a name="where-to-go-for-help"></a>ヘルプの参照先

1. まず、このトピックで前述した関連するトピックのすべての手順に従っていることを再度確認します。
2. パートナーに確認します。 パートナーは業務と設定について理解しています。 設定には、パートナーがすばやく特定して対処できる、一意のカスタマイズが含まれる場合があります。
3. [Retail SDK FAQ](retail-sdk/sdk-faq.md) を確認します。 一般的な問題が識別されると更新されます。
4. LCS を通してサポート リクエストを送信します。 問題に関してできるだけ多くの情報を提供してください。 リクエストを送信するときは、FastTrack ソリューション アーキテクトにコピーを送信します。
5. パートナー、サポート スペシャリスト、ソリューション アーキテクト、またはこれらの三者の組み合わせと画面を共有することが予期されます。 エラーを再現する準備を行います。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
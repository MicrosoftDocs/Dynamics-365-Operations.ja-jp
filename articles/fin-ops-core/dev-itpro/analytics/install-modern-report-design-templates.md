---
title: 現代レポートのデザイン テンプレートのインストール
description: この記事では、最新のレポート デザイン テンプレートをアプリケーション スイートにインストールする方法について説明します。
author: RichdiMSFT
ms.date: 10/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 82783
ms.assetid: 96676acf-a86b-4296-81db-b6ad6b4a46fb
ms.search.form: PrintMgmtSetupUIMain
ms.openlocfilehash: 25d82469c01c54f311b37e2022e3b5ac87e1a08c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281706"
---
# <a name="install-modern-report-design-templates"></a>現代レポートのデザイン テンプレートのインストール

[!include [banner](../includes/banner.md)]

この記事では、最新のレポート デザイン テンプレートをアプリケーション スイートにインストールする方法について説明します。 これらのサンプルを使用すると、ヘッダーとフッターに柔軟なブランドのあるグラフィックの豊富なビジネス ドキュメントを作成することができます。

## <a name="introduction"></a>はじめに

アプリケーション スイートの複数の主要なビジネス ドキュメント用のレポート デザインの形式を取る、新しい一連の開発者ツールを利用できます。 これらのレポート デザインは、アプリケーションで取引が生成されたときに、一般向けのドキュメントのヘッダーとフッターに柔軟なブランディングが表示されるように再設計されました。 次の図は、売上請求書の初期設計が最新の売上請求書の設計とどのように異なるかを示しています。

[![初期の売上請求書デザインおよび最新の売上請求書のデザインの例。](./media/design-comparison-1024x653.png)](./media/design-comparison.png)

インストールの完了後に、組み込みのブランド管理ツールを使用してアプリケーション ビジネス ドキュメントの最新のデザインに適用するブランド設定を定義できます。 ブランド管理ツールは、**組織管理** &gt; **設定** &gt; **ドキュメント ブランド** &gt; **ブランドの詳細** で利用可能です。

## <a name="why-arent-these-designs-the-default-designs-for-the-application-suite-reports"></a>これらのデザインがアプリケーション スイート レポートの既定のデザインでないのはなぜですか。

次の 2 つの主な理由が、レガシ ソリューションを維持しています。

- **最新のデザインには、コードが含まれていません。** レガシ ソリューションはコンフィギュレーション キーを認識し、地域によって異なる規制に関する要件を遵守する埋め込み Microsoft Visual Basic (VB) コードを使用することができますが、最新のレポート デザインでは柔軟性がはるかに少ないです。 最小限のコードが使用されている単純な設計によるメリットはありますが、各地域にわたる再利用性はありません。
- **最新のデザインは、すべてのビジネス ドキュメントで使用できるわけではありません。** サポートされているビジネス ドキュメントと最新のレポート設計の可用性との間にはギャップがあります。 レガシ デザインは審美的に満足できるものではありませんが、一貫性のある感覚を提供します。

> [!IMPORTANT]
> シンプルで現代的なデザインが **推奨されない** 展開もあります。 これは、顧客が実行時に、既存のアプリケーション構成設定を通じてドキュメントのレイアウトを制御する必要がない場合に使用します。

## <a name="apply-the-modern-designs"></a>最新のデザインを適用

最新のレポート デザインは、モデル ファイルにバンドルされ、Microsoft Dynamics Lifecycle Services (LCS) に転記されました。 したがって、既存のサブスクリプションから簡単にアクセスできます。 最新のレポート設計ソリューションを取得し、ローカルの開発環境にインストールするには、次の手順を使用します。 その後、最新のレポート デザインを適切なシナリオに組み込むために、何らかのカスタマイズを適用してください。

アプリケーション スイートに最新のレポート デザインをインストールするには、これらの手順に従います。

1. [LCS](https://lcs.dynamics.com/) にサインインして展開ダッシュボードにアクセスします。 その後、**共有アセット ライブラリ** ページで、**モデル** アセット タイプを選択し、**ApplicationSuiteModernDesigns** モデル ファイルをダウンロードします。 モデル ファイルを、開発環境からアクセスできる場所に保存します。

    > [!NOTE]
    > 使用しているアプリケーションのバージョンに適切なモデル ファイルを選択してください。

2. ローカルの開発環境にモデル ファイルをインポートします。 開発環境でモデル ファイルをインストールするには、ModelUtil.exe ツールと **-import** ディレクティブを使用します。 次に例を示します。

    ```Console
    ModelUtil.exe -import -metadatastorepath=[path of the metadata store] -file=[full path of the file to import]
    ```

3. **\<AOSServiceDrive\>:\\AOSService\\PackagesLocalDirectory\\bin** フォルダーに移動します。
4. 次のコマンドを実行します。

    ```Console
    ModelUtil.exe -import -metadatastorepath=J:\AOSService\PackagesLocalDirectory -file="E:\Test\AppSuiteModernDesigns.axmodel"
    ```

    モデル ファイルをインポートする方法の詳細については、 [モデルのエクスポートとインポート](../dev-tools/models-export-import.md) を参照してください。 モデル ファイルをインポートした後、Microsoft Visual Studio を開始します。 アプリケーション エクスプローラーで、**アプリケーション スイート - 最新のデザイン** コレクションが **AOT** ノードの下に表示されていることを確認します。 アプリケーション エクスプ ローラーを使用する方法の詳細については、[開発ツール チュートリアル](../dev-tools/introduction-visual-studio.md)を参照してください。

アプリケーション スイート最新デザイン モデルを正常にインポートしたので、アプリケーション スイートをリビルドしてメタデータ要素を更新する必要があります。

## <a name="build-the-application-suite"></a>アプリケーション スイートの構築

Application Suite Modern Designs モデルは、Application Suite モデルの拡張です。 すべてのアプリケーション参照がモデル拡張を対象とするように更新されるようにするには、Microsoft Visual Studio を使用してアプリケーション スイート モデルを構築する必要があります。

1. Visual Studio を起動するか、既存のインスタンスを使用します。
2. **Dynamics 365** メニューで、**モデルのビルド** を選択します。
3. 一覧で、**ApplicationSuite** パッケージのチェック ボックスをオンにします。

    [![Visual Studio の中の完全なビルド ダイアログ ボックス。](./media/BuildAppSuite.png)](./media/BuildAppSuite.png)

    > [!NOTE]
    > アプリケーション スイート最新デザイン モデルがパッケージ定義に含まれていることを確認します。

4. **ビルド** を選択し、アプリケーション スイートの完全なビルドを実行します。

このプロセスは、マシンの規模によっては最大 20 分かかる場合があります。

## <a name="deploy-the-modern-designs-one-box-environments"></a>最新のデザインを配置する (ワンボックス環境)

最新のレポート デザイン テンプレートを含むアプリケーション スイートをコンパイルした後、ローカルで変更を確認する必要があります。 変更を確認するには、ローカルで実行されている Microsoft SQL Server Reporting Services (SSRS) のインスタンスに新しい最新のレポート デザイン ソリューションを展開する必要があります。

最新のレポート デザインを既存のアプリケーション スイート レポートに反映させるには、これらの手順に従います。

1. アプリケーション スイート レポートを含むプロジェクトを作成します。 アプリケーション エクスプローラーの **アプリケーション スイートの最新のデザイン** モデルで、**レポート** ノードを展開してから **レポート** サブノードを展開します。 フォルダーですべての品目を選択して右クリックし、**新しいプロジェクトに追加** を選択します。
2. **新しいプロジェクト** ウィザードの操作を完了します。 すべての既定値を受け入れます。
3. ソリューション エクスプローラーで、プロジェクトを選択し、右クリックしてから、**レポートを配置する** を選択してビルドを配置し、ローカルにレポートを配置します。

既存のレポートに最新のレポート デザインを追加するとき、パラメータ処理と、標準のソリューションで使用されるデータ プロバイダーの両方を再利用できます。

## <a name="update-print-management-settings"></a>印刷管理の設定を更新

この時点で、アプリケーションから最新のレポート デザインにアクセスできるようになります。 運用環境に配置する前に、現代レポートのデザイン テンプレートに関するテスト検証を行うことを確認します。 テスト検証を行うには、アプリケーション ビジネス プロセスの最新のレポート デザインをアクティブにする必要があります。

最新のレポート デザイン ソリューションを既定のレポート デザインとして選択することにより、顧客の販売注文の印刷管理設定を更新するには、これらの手順に従います。

1. モジュールの **フォームの設定** ページを開きます。 たとえば、売掛金勘定に対して、**売掛金勘定** &gt; **設定** &gt; **フォーム** &gt; **フォーム設定** の順に選択します。
2. **印刷管理** を選択して **印刷管理設定** ページを開きます。
3. ツリーを展開し、**販売済注文確認書** ドキュメントの設定を見つけます。
4. **元 &lt; 既定 &gt;** を選択し、既定のドキュメントの工順の変更を開始します。
5. **レポート形式** リストで、**SalesConfirmModern.Report** を選択して現代レポートのデザイン ソリューションを有効にします。

    [![最新のデザインを選択するために使用される印刷管理の設定ページ。](./media/UpdatePrintMgtSettings.png)](./media/UpdatePrintMgtSettings.png)

6. 別のページを開きます。 このステップでは、保存操作が強制的に実行されます。
7. アプリケーションで最新のデザインを表示するために販売注文を転記します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

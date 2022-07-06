---
title: バージョン 8.0 から 10.0.X への環境の更新
description: この記事では、既存の財務と運用 8.0 環境を、10.0.X アプリケーション リリースに更新するために必要な手順について説明します。
author: laneswenka
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 78d5298e55f3749ab85084ad5c60f89a07ddaef7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866276"
---
# <a name="update-environments-from-version-80-to-100x"></a>バージョン 8.0 から 10.0.X への環境の更新

[!include [banner](../includes/banner.md)]

この記事では、既存の財務と運用 8.0 環境を、10.0.X アプリケーション リリースに更新するために必要な手順について説明します。

## <a name="background"></a>バックグラウンド

従来、アプリケーションの新しいバージョンへの移行には、追加の仮想マシンの展開、コード アップグレード、データ アップグレード、および Microsoft Dynamics サービス エンジニアリング (DSE) チームとの数日前の事前スケジューリングを含む厳格なアップグレードが必要でした。  最新バージョンの取得がより簡単になっており、これは継続的に改善されていきます。

> [!NOTE]
> フル アップグレードと比較した場合の更新エクスペリエンスをサポートしています。 これは、8.0 および 10.0.X アプリケーション スキーマ間には **データ アップグレードやコード アップグレードの手順が存在しない** ために可能です。 プラットフォーム アップデートを適用するのと同じように、対象となる環境が更新されます。

バージョン 8.0 から 10.0.X に更新するプロセスの概要は次のとおりです。

1. 10.0.X 開発者環境とビルド環境を展開します。
2. バージョン管理を分岐し、アプリケーション修正プログラムを削除します。
3. カスタム拡張機能や ISV ソリューションを再コンパイルします。
4. 1 つのソフトウェア展開可能パッケージを作成します。
5. 展開可能パッケージを 10.0.X バイナリ アップデート パッケージとマージします。
6. 検証用の対象環境を展開します。
7. 運用環境に展開します。

## <a name="deploy-100x-developer-and-build-environments"></a>10.0.X 開発者環境とビルド環境を配置します
Lifecycle Services を使用して 1 つ以上の開発者環境と 1 つの新しいビルド環境をアプリケーション 10.0.X リリースに配置します。

平均では、これには 3 ～ 4 時間かかり、同時に行うことができます。 ビルド環境で、**エージェント プールの新規作成** を行い、**詳細オプション** 画面でこの環境に割り当てます。

Azure DevOps で、既存のビルド定義にアクセスし、10.0.X 用の新しいエージェント プールを使用していないことを確認します。 これにより、新しいビルド エージェントが古いアプリケーション コードをコンパイルしようとしなくなります。

### <a name="apply-the-latest-binary-update-to-your-build-and-development-servers"></a>ビルドと開発サーバーに最新のバイナリ更新プログラムを適用する
Lifecycle Services で、手順 1 で配置した **ビルド サーバー** に移動します。 **環境の詳細** ページの下部にある **更新** タイルを使用して、使用可能な最新の更新プログラムを取得し、 **パッケージの保存** ボタンを使用してプロジェクトの **アセット ライブラリ** に保存します。  たとえば、10.0 Platform update 24 packageを **アセット ライブラリ** に保存できます。

これと同じパッケージを、パッケージを保存したビルド サーバーに加えて、配置した新しい 10.0.X 開発者環境のいずれかに適用します。

> [!NOTE]
> 10.0 プラットフォーム 更新プログラム24 ビルド サーバーを展開する際には、 **更新** ウィンドウから使用できる 10.0 プラットフォーム 更新プログラム24 などの最新の更新プログラムを取得することを推奨します。 タイルメニュー上、ビルド サーバーが「0」と表示されている場合は、お使いのバージョンに、共有アセットライブラリから関連するパッケージを取り込むことができます。 タイルメニュー上で 1つ 以上の数値が表示されている場合は、そのパッケージを取り込んで使用できます。

## <a name="begin-branch-work-for-version-control-and-remove-any-application-hotfixes"></a>バージョン管理の分岐作業を開始し、アプリケーション修正プログラムを削除
新しい環境が展開されるとき、更新の分岐作業を開始します。 例として、バージョン管理での次の分岐構造を使用します。  分岐の設計は顧客ごとに異なりますので、分岐の設定に基づき、それに応じてステップを調整するように注意してください。

[![VersionControl。](./media/VersionControl.png)](./media/VersionControl.png)

### <a name="prepare-using-visual-studio"></a>Visual Studio を使用する準備
その他の開発コンピューター (展開される新規コンピューター以外) で、Visual Studio を開き、ソース管理エクスプローラーに移動します。 10.0.X 更新用に分離される新しい分岐を作成します。

[![BranchFor81。](./media/BranchFor81.png)](./media/BranchFor81.png)

次に、この分岐で Microsoft パッケージ フォルダーを削除します。 削除する必要のある 8.0 での修正プログラムの適用するからチェックインした、ApplicationSuite などのパッケージがあります。 カスタム パッケージまたは ISV が残っているときのみ、分岐にこれらの変更をチェックインします。

>[!IMPORTANT]
> バージョン管理ワークスペースを新しい開発環境にマップする前に、これを行うことが重要です。 これは、Microsoft 修正プログラムが削除されて、作業環境に伝播され、手を触れていない 10.0.X アプリケーション コードが削除されることのないようにすることです。

## <a name="recompile-custom-extensions-andor-isv-solutions"></a>カスタム拡張機能や ISV ソリューションを再コンパイル
新しい開発環境にこの分岐をマッピングし、ソース コードが提供される場合に拡張および ISV ソリューションをコンパイルする準備が整いました。  ISV が提供されたバイナリ パッケージのみ持っている場合、それらをソース管理にチェックインできます。ビルド環境では、1 つのソフトウェア展開可能パッケージを生産するために、拡張パッケージとバイナリが結合されます。 このプロセスの追加の情報は、[サード パーティからの展開可能パッケージ](../dev-tools/manage-runtime-packages.md#deployable-packages-from-third-parties)にあります。  これは、後で 10.0.X バイナリ アップデートとパッケージを結合するときに役立ちます。

> [!NOTE]
> この **ステップは必要** です。10.0.X アプリケーション コードにはバイナリ レベルから 8.0 との互換性がないためです。 アプリケーションの将来のリリースでは、この手順はオプションとなります。

## <a name="produce-a-single-software-deployable-package"></a>1 つのソフトウェア展開可能パッケージを作成
開発者環境でコンパイルし、解決するためのエラーがない場合、以前設定した新しい 10.0.X ビルド環境エージェントを使用して Azure DevOps でビルドを開始します。 これが完了したら、展開可能パッケージ コンポーネントがビルド結果に添付されます。 このパッケージをダウンロードして、Lifecycle Services アセット ライブラリにアップロードします。  この 1 つのパッケージに、拡張機能と ISV ソリューションがすべて含まれています。

## <a name="merge-the-deployable-package-with-the-100x-binary-update-package"></a>展開可能パッケージを 10.0.X バイナリ アップデート パッケージとマージ
プロジェクトの **アセット ライブラリ** で、新しい 10.0.X ソフトウェアの配置可能パッケージ (ISV を含むカスタマイズ パッケージ) と、記事の先頭にある手順 1 で保存された 10.X PU2X バイナリ更新パッケージの両方を特定します。 両方のパッケージを強調表示し、**マージ** を選択します。 これにより、ファイルが、マージされた更新パッケージに結合されます。 このパッケージをさまざまなテスト環境に適用できます。

> [!NOTE]
> このマージしたパッケージを、異なる Lifecycle Services プロジェクトの間で移動することはできません。 マージの処理では、アセット ライブラリの他のパッケージを参照します。これらのパッケージは他のプロジェクトには存在しません。

## <a name="deploy-to-target-environments-for-validation"></a>検証用の対象環境を展開
マージされた更新パッケージを使用して、これをさまざまなテスト環境に展開します。  この方法の詳細については、[クラウド環境への更新プログラムの適用](../deployment/apply-deployable-package-system.md) を参照してください。  このマージ済の更新プログラム パッケージは、階層 1/OneBox 環境やと階層 2 サンドボックスに展開することができます。 少なくとも、サブスクリプションに付属しているサンドボックス第 2 層環境に展開する必要があります。  検証が完了したら、マージされた更新パッケージをリリース候補としてマークします。

## <a name="deploy-to-production"></a>運用環境に展開
アセット ライブラリでリリース候補をマークしたら、運用環境への展開をスケジューリングできます。  これは、他のソフトウェア展開可能パッケージの適用と同じプロセスに従います。

## <a name="known-issues"></a>既知の問題

### <a name="globalupdate-script-for-service-model-aosservice-with-error-the-specified-module-cprogram-filesmicrosoft-security-clientmpprovider"></a>サービスモデルの GlobalUpdate スクリプト: AOSService のエラー 'The specified module 'C:\Program Files\Microsoft Security Client\MpProvider' 
このエラーは一過性のものであるため、無視しても構いません。  これを無視するには、Lifecycle Services の **再開** をクリックします。

### <a name="deploying-the-100x-binary-update-to-developer-environments-causes-applicationsuite-compilation-errors"></a>10.0.X バイナリ更新プログラムを開発環境に配置すると、ApplicationSuite コンパイル エラーが発生
パッケージを 8.0 環境に適用でき、ソース コードが更新されます。  拡張パッケージのコンパイルには影響が及びません。  オーバーレイしており、ApplicationSuite パッケージからオブジェクトを削除し、再コンパイルしようとした場合、エラーが発生する場合があります。  これが解決されるまで、開発者環境を 10.0.X に再度展開し、バージョン管理からソース コードを同期してください。

### <a name="cannot-find-100x-binary-update-package-on-the-all-binary-updates-tile-on-the-my-environment-details-page"></a>環境の詳細ページのすべてのバイナリ更新タイルに 10.0.X バイナリ更新パッケージがない
当初は、パッケージが **すべてのバイナリ更新** タイルにあると伝えられました。 リリース 8.0 から最新のバイナリを取得するだけのユーザーがリリース 10.0.X に誤って更新しないようにするため、バイナリ パッケージを共有資産ライブラリに移動しました。 この記事は、この変更を反映するように更新されています。

### <a name="deployment-of-my-environment-fails-with-error-on-duplicate-objects"></a>重複するオブジェクトへの環境の配置がエラーで失敗する
既定では、Visual Studio でオブジェクトを拡張すると、Object.*Extension1* という名前で作成されます。 Microsoft により同じオブジェクトの新しい機能拡張が導入された場合、この名前は衝突する可能性があります。 この場合、展開は、次のようなエラーで失敗します。

```Console
Exception calling "CreateRuntimeProvider" with "1" argument(s): "Runtime metadata is invalid because the same metadata artifact has been defined in multiple assemblies. \nFirst 10 conflicting names: SystemAdministration.Extension1. \nSee metadata events for complete list."
```

これを防止するため、10.0.X 開発者コンピューターで拡張機能をコンパイルする必要があります。 この問題を解決するには、SystemAdministration.*Customer* など、バニティ拡張名前付け規則に従って拡張オブジェクトのいずれかの名前を変更します。

### <a name="deployment-on-my-environment-fails-with-error-on-dvts-or-etws"></a>DVT または ETW で環境での配置がエラーにより失敗する
DVT または ETWのステップが実行されると IIS/アプリケーション プールが完全に再開されない既知の問題があります。 DVT が環境の URL に接続しようとしているため、問題が発生します。 この問題を解決するには、LCS の展開で **再開** をクリックして、ステップを再試行します。  この問題を解決するため、タイマーと自動再試行が追加されます。




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
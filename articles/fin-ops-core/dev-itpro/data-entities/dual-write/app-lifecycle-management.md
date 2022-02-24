---
title: アプリケーション ライフサイクル管理
description: このトピックでは、二重書き込みソリューションに対応することの利点について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a86c8966bd43f7815289e84f9aae6c6f4d307b5a
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744653"
---
# <a name="application-lifecycle-management"></a>アプリケーション ライフサイクル管理

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

二重書き込みソリューションに対応することで、環境全体での二重書き込みテーブル マップの転送やバックアップ/復元など、基本的なアプリケーション ライフサイクル管理 (ALM) 機能を実現できます。 また、AppSource から Microsoft または独立系ソフトウェア ベンダー (ISV) が公開するソリューションを入手できるシナリオも有効にします。

## <a name="what-is-a-dual-write-solution"></a>二重書き込みソリューションとは何ですか?

二重書き込みソリューションには、1 つ以上の二重書き込み テーブル マップを含めることができます。 これらのマップは、ご使用の環境 (Microsoft Power Apps の **ソリューション** を選択) にインポートできます。 また、パッケージとして他の環境にエクスポートすることもできます。 Microsoft 公開のテーブル マップまたは ISV 公開のテーブル マップを AppSource からインポートして、テスト環境で変更し、テストして、準備が整ったら、実稼働環境にエクスポートします。 また、AppSource でソリューションを公開して、他のユーザーが使用できるようにすることもできます。

ソリューションには、マネージドとアンマネージドの 2 つのタイプがあります。

マネージド ソリューションを変更することはできませんが、インポート後にアンインストールできます。 アンマネージド ソリューションをインポートする場合は、そのソリューションのすべてのコンポーネントを環境に追加します。 既にカスタマイズしたコンポーネントを含むアンマネージド ソリューションをインポートすると、カスタマイズはインポート済みアンマネージド ソリューションのカスタマイズによって上書きされます。

ソリューションの詳細については、[ソリューションの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview) を参照してください。

## <a name="install-the-dual-write-core-solution"></a>二重書き込みコア ソリューションのインストール

二重書き込みコア ソリューションには、テーブル マップのメタデータが含まれており、環境にインストールする必要があります。

1. Power Apps の左ウィンドウで、**Solutions** を選択します。
2. **AppSource を開く** を選択し、**二重書き込みコア** という名前のソリューションを検索します。
3. プロンプトに従ってソリューションをインポートします。

    ![二重書き込みコア ソリューションのインポート](media/import-solution.png)

## <a name="install-the-dual-write-table-maps-solution"></a><a id="install-table-maps"></a> 二重書き込みテーブル マップ ソリューションのインストール

1. Power Apps の左ウィンドウで、**Solutions** を選択します。
2. **AppSource を開く** を選択し、**Finance and Operations パッケージ用 Dataverse アドイン** という名前のソリューションを検索します。
3. プロンプトに従ってソリューションをインポートします。
4. Finance and Operations アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたテーブル マップを適用します。 ソリューションを適用すると、既定のテーブル マップが公開されていることを確認できます。

    ![二重書き込みテーブル マップの公開](media/default-entity-maps.png)

Microsoft が公開した二重書き込みテーブル マップ ソリューションを環境に正常にインポートして適用しました。

## <a name="import-table-maps-through-a-dual-write-solution-and-apply-them-to-your-environment-new-environments"></a>二重書き込みソリューションを使用してテーブル マップをインポートし、環境に適用する (新しい環境)

このセクションでは、AppSource からテーブル マップをインポートし、環境に適用する方法について説明します。

![テーブル マップのインポートと適用](media/import-apply-entity-maps.png)

1. 二重書き込みコア ソリューションをインポートします。

    1. 新しい二重書き込み環境 (Finance and Operations アプリ環境と Dataverse 環境) を作成します。
    2. このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、AppSource の二重書き込みコア ソリューションを Power Apps にインストールします。
    3. 二重書き込みコア ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。

2. Microsoft 公開、または ISV 公開のテーブル マップ ソリューションをインポートします。

    1. [二重書き込みテーブル マップ ソリューションのインストール](#install-table-maps) の手順に従って、Power Apps の AppSource から Microsoft 公開、または ISV 公開のテーブル マップをダウンロードしてインストールします。
    2. テーブル マップ ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。

3. Finance and Operations アプリ環境に二重書き込みテーブル マップ ソリューションを適用します。

    [二重書き込みテーブル マップ ソリューションのインストール](#install-table-maps) セクションの説明に従って、Finance and Operations アプリの **二重書き込み** ページで **ソリューションの適用** を選択し、ダウンロードしたソリューションを適用します。

## <a name="update-table-maps-and-export-them-to-other-environments-as-a-solution"></a><a id="update-table-maps"></a> テーブル マップを更新し、ソリューションとして他の環境にエクスポートします

このセクションでは、カスタマイズ済みテーブル マップをソリューションとしてエクスポートし、それをバックアップとして使用して、環境間でアーティファクトを移動し、AppSource に発行する方法について説明します。

![カスタマイズされたマップをソリューションとしてエクスポート](media/export-maps-solution.png)

### <a name="customize-your-table-maps"></a>テーブル マップのカスタマイズ

最初の手順では、既存のテーブル マップを変更し、新しいテーブル マップを追加することによって、テーブル マップをカスタマイズします。

1. Finance and Operations アプリの **テーブル マッピング** タブで、ソリューションを使用してインストールした既定のテーブル マップのマッピングをカスタマイズします。 新しいテーブル マップを追加するには、**テーブルの追加** を選択します。 どちらの場合も、テーブル マップを保存するときに、パブリッシャーとバージョン番号を指定するように求められます。

    次の図は、**生年月日** という名前の新しい列を連絡先 - CDS 連絡先 V2 テーブル マップに追加して、既定のパブリッシャーを選択する方法を示しています。

    ![新しい生年月日の列の追加](media/add-new-birthday-field.png)

    > [!NOTE]
    > これらの変更済みテーブル マップを使用して[新しいソリューションを作成する](#create-new-solution) 場合は、同じパブリッシャーを指定する必要があります。

    次の図は、**アドレス帳** という名前の新しいテーブル マップを追加する方法を示しています。

    ![新しいアドレス帳テーブル マップの追加](media/add-address-book.png)

2. 変更および追加したテーブル マップを確認します。 それらを有効にしてテストし、期待どおりに機能することを確認してください。

    ![新しいテーブル マップの確認](media/confirm-new-entity-maps.png)

### <a name="create-a-new-dual-write-solution-and-add-your-components-customized-table-maps"></a><a id="create-new-solution"></a> 新しい二重書き込みソリューションを作成し、コンポーネントを追加する (カスタマイズ済みテーブル マップ)

マッピングをカスタマイズして新しいマッピングを追加したので、次の手順では、新しい二重書き込みソリューションを作成し、テーブル マップを追加します。

1. Power Apps の左ウィンドウで **ソリューション** を選択し、次に **新しいソリューション** を選択して、ソリューションを作成します。 この例では、ソリューションの名前は **MyCustomTableMaps** です。 前の手順で選択したのと同じパブリッシャーを選択してください。

    ![新しいソリューションの作成とテーブル マップの追加](media/add-map-to-solution.png)

2. **作成** を選択します。 新しいソリューションが **ソリューション** 一覧ページに表示されます。

    ![ソリューション 一覧ページの新しいソリューション](media/show-new-solution.png)

3. 二重書き込みソリューションを作成したので、前の手順で作成したカスタマイズ済みテーブル マップを追加できます。 作成した **MyCustomTableMaps** ソリューションを選択し、**既存の追加** を選択して、**その他** をポイントし、**二重書き込みテーブル マップ** を選択します。

    ![カスタマイズ済みテーブル マップをソリューションに追加](media/add-customized-maps.png)

4. 一覧で、カスタマイズ済みテーブル マップを選択し、ソリューションに追加します。 ソリューションには、カスタマイズ済みテーブルが含まれます。

    ![新しいソリューションのカスタマイズ済みテーブル](media/entities-new-solution.png)

これで、テーブルをカスタマイズし、ソリューションに追加しました。

### <a name="export-and-publish-your-solution"></a>ソリューションのエクスポートと発行

ソリューション チェッカーを実行して問題がないことを確認したら、作成したソリューションをエクスポートし、変更を公開します。

1. ソリューションの一覧でソリューションを選択し、**エクスポート** を選択します。
2. バージョン番号を更新し、ソリューションをマネージドまたはアンマネージド ソリューションとしてエクスポートするかどうかを選択します。 (マネージド ソリューションとしてエクスポートすることをお勧めします。) 次に **エクスポート** を選択します。

    ![バージョン番号の更新とエクスポート](media/update-version-number.png)

3. エクスポートする前に、**すべての変更の公開** を選択し、**問題点を確認** を選択します。 完了したら、**次へ** を選択して、すべての変更を公開します。

    ![変更の公開](media/export-and-publish.png)

    ソリューションは、そのすべてのコンポーネントと共に ZIP ファイルにエクスポートされます。

    ![ZIP ファイルにエクスポートされたソリューション](media/components-to-zip.png)

これで、テーブルをカスタマイズして、新しいソリューションに追加し、他の環境にインポートして適用できるソリューション ファイルを作成しました。 (この機能は、テスト環境と実稼動環境の間でテーブル マップを移動する場合に役立ちます。) 同様に、すべてのテーブル マップのバックアップを、ソリューションに追加し、そのソリューションをパッケージとしてエクスポートすることによって作成できます。 その後、そのパッケージを任意の環境にインポートして、テーブル マップを復元できます。

AppSource にパッケージを公開する方法の詳細については、[AppSource でアプリを公開](https://docs.microsoft.com/powerapps/developer/common-data-service/publish-app-appsource) を参照してください。

### <a name="test-your-exported-solution-package"></a>エクスポート済みソリューション パッケージのテスト

エクスポート済みソリューション パッケージは、インポートして別の環境に適用することでテストできます。

1. Power Apps で、**インポート** を選択し、パッケージを新しい環境にインポートします。

    ![パッケージを新しい環境にインポート](media/import-package.png)

2. 環境にインポートしたばかりのソリューションを適用します。

    ![ソリューションを環境に適用](media/apply-solution-to-environment.png)

3. 2 つのカスタマイズ済みテーブル マップが、二重書き込みテーブル マップの一覧ページに表示されることを確認します。

    ![一覧ページの 2 つのカスタマイズ済みテーブル マップ](media/entity-maps-in-list.png)

4. 前の手順で行ったカスタマイズが保持されていることを確認します。

    ![カスタマイズが保持されていることの確認](media/check-customizations.png)

### <a name="use-the-table-map-version"></a>テーブル マップ バージョンの使用

ソリューションには、テーブル マップの異なる実装が含まれる場合があります。 たとえば、連絡先 - CDS 連絡先 V2 テーブル マップのバージョンには、異なるパブリッシャーまたはより新しいバージョン番号が含まれる場合があります。 このような場合、**テーブル マップ バージョン** ボタンを使用して、環境で使用するテーブル マップを選択できます。

![環境で使用するテーブル マップの選択](media/select-entity-map.png)

## <a name="upgrade-existing-dual-write-environments-for-solution-awareness-existing-environments"></a>ソリューション認識の既存の二重書き込み環境をアップグレードする (既存の環境)

1. 二重書き込みコア ソリューションをインポートします。

    1. このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、二重書き込みコア ソリューションを AppSource から Power Apps にインポートします。
    2. 二重書き込みコア ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。

2. テーブル マップをアップグレードします。

    アップグレードを促す通知が表示されます。

    ![テーブル マップをアップグレードするプロンプト](media/upgrade-prompt.png)

    ページ上部の **テーブル マップのアップグレード** を選択します。

    ![テーブル マップのアップグレード](media/upgrade-entity-maps.png)

アップグレードには数分かかります。 完了すると、通知が表示されます。

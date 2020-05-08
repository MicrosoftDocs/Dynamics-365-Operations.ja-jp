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
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 971fedb5f059bce5eefb9abc9ae5419ab227750a
ms.sourcegitcommit: e9fadf6f6dafdcefaff8e23eaa3c85f53437db3f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3279120"
---
# <a name="application-lifecycle-management"></a>アプリケーション ライフサイクル管理

[!include [banner](../../includes/banner.md)]


二重書き込みソリューションに対応することで、環境全体での二重書き込みエンティティ マップの転送やバックアップ/復元など、基本的なアプリケーション ライフサイクル管理 (ALM) 機能を実現できます。 また、AppSource から Microsoft または独立系ソフトウェア ベンダー (ISV) が公開するソリューションを入手できるシナリオも有効にします。

## <a name="what-is-a-dual-write-solution"></a>二重書き込みソリューションとは何ですか?

二重書き込みソリューションには、1 つ以上の二重書き込みエンティティ マップを含めることができます。 これらのマップは、ご使用の環境 (Microsoft Power Apps の **ソリューション** を選択) にインポートできます。 また、パッケージとして他の環境にエクスポートすることもできます。 Microsoft 公開のエンティティ マップまたは ISV 公開のエンティティ マップを AppSource からインポートして、テスト環境で変更し、テストして、準備が整ったら、実稼働環境にエクスポートします。 また、AppSource でソリューションを公開して、他のユーザーが使用できるようにすることもできます。

ソリューションには、マネージドとアンマネージドの 2 つのタイプがあります。

マネージド ソリューションを変更することはできませんが、インポート後にアンインストールできます。 アンマネージド ソリューションをインポートする場合は、そのソリューションのすべてのコンポーネントを環境に追加します。 既にカスタマイズしたコンポーネントを含むアンマネージド ソリューションをインポートすると、カスタマイズはインポート済みアンマネージド ソリューションのカスタマイズによって上書きされます。

ソリューションの詳細については、[ソリューションの概要](https://docs.microsoft.com/powerapps/maker/common-data-service/solutions-overview) を参照してください。

## <a name="install-the-dual-write-core-solution"></a>二重書き込みコア ソリューションのインストール

二重書き込みコア ソリューションには、エンティティ マップのメタデータが含まれており、環境にインストールする必要があります。

1. Power Apps の左ウィンドウで、**ソリューション** を選択します。
2. **AppSource を開く** を選択し、**二重書き込みコア** という名前のソリューションを検索します。
3. プロンプトに従ってソリューションをインポートします。

    ![二重書き込みコア ソリューションのインポート](media/import-solution.png)

## <a name="install-the-dual-write-entity-maps-solution"></a>二重書き込みエンティティ マップ ソリューションのインストール

1. Power Apps の左ウィンドウで、**ソリューション** を選択します。
2. **AppSource を開く** を選択し、**Finance and Operations パッケージ用 Common Data Service アドイン** という名前のソリューションを検索します。
3. プロンプトに従ってソリューションをインポートします。
4. Finance and Operations アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたエンティティ マップを適用します。 ソリューションを適用すると、既定のエンティティ マップが公開されていることを確認できます。

    ![二重書き込みエンティティ マップの公開](media/default-entity-maps.png)

Microsoft が発行した二重書き込みエンティティ マップ ソリューションを環境に正常にインポートして適用しました。

## <a name="import-entity-maps-through-a-dual-write-solution-and-apply-them-to-your-environment-new-environments"></a>二重書き込みソリューションを使用してエンティティ マップをインポートし、環境に適用する (新しい環境)

このセクションでは、AppSource からエンティティ マップをインポートし、環境に適用する方法について説明します。

![エンティティマップのインポートと適用](media/import-apply-entity-maps.png)
    
1. 二重書き込みコア ソリューションをインポートします。

    1. 新しい二重書き込み環境 (Finance and Operations アプリ環境と Common Data Service 環境) を作成します。
    2. このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、AppSource の二重書き込みコア ソリューションを Power Apps にインストールします。
    3. 二重書き込みコア ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。

2. Microsoft 公開、または ISV 公開のエンティティー マップ ソリューションをインポートします。

    1. [二重書き込みエンティティ マップ ソリューションのインストール](#install-the-dual-write-entity-maps-solution) の手順に従って、Power Apps の AppSource から Microsoft 公開、または ISV 公開のエンティティー マップをダウンロードしてインストールします。
    2. エンティティー マップ ソリューションが Power Apps の **ソリューション** の下に一覧表示されていることを確認します。

3. Finance and Operations アプリ環境に二重書き込みエンティティ マップ ソリューションを適用します。

    [二重書き込みエンティティ マップ ソリューションのインストール](#install-the-dual-write-entity-maps-solution) セクションの説明に従って、Finance and Operations アプリの **二重書き込み** ページで **ソリューションの適用** を選択し、ダウンロードしたソリューションを適用します。

## <a name="update-entity-maps-and-export-them-to-other-environments-as-a-solution"></a>エンティティ マップを更新し、ソリューションとして他の環境にエクスポートします

このセクションでは、カスタマイズ済みエンティティ マップをソリューションとしてエクスポートし、それをバックアップとして使用して、環境間でアーティファクトを移動し、AppSource に発行する方法について説明します。

![カスタマイズされたマップをソリューションとしてエクスポート](media/export-maps-solution.png)

### <a name="customize-your-entity-maps"></a>エンティティ マップのカスタマイズ

最初の手順では、既存のエンティティ マップを変更し、新しいエンティティ マップを追加することによって、エンティティ マップをカスタマイズします。

1. Finance and Operations アプリの **エンティティ マッピング** タブで、ソリューションを使用してインストールした既定のエンティティ マップのマッピングをカスタマイズします。 新しいエンティティ マップを追加するには、**エンティティの追加** を選択します。 どちらの場合も、エンティティ マップを保存するときに、パブリッシャーとバージョン番号を指定するように求められます。

    次の図は、**生年月日** という名前の新しいフィールドを連絡先 - CDS 連絡先 V2 エンティティ マップに追加して、既定のパブリッシャーを選択する方法を示しています。

    ![新しい生年月日フィールドの追加](media/add-new-birthday-field.png)

    > [!NOTE]
    > これらの変更済みエンティティ マップを使用して [新しいソリューションを作成する](#create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps) 場合は、同じパブリッシャーを指定する必要があります。

    次の図は、**アドレス帳** という名前の新しいエンティティ マップを追加する方法を示しています。

    ![新しいアドレス帳エンティティ マップの追加](media/add-address-book.png)

2. 変更および追加したエンティティ マップを確認します。 それらを有効にしてテストし、期待どおりに機能することを確認してください。

    ![新しいアドレス帳エンティティ マップの追加](media/confirm-new-entity-maps.png)

### <a name="create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps"></a>新しい二重書き込みソリューションを作成し、コンポーネントを追加する (カスタマイズ済みエンティティ マップ)

マッピングをカスタマイズして新しいマッピングを追加したので、次の手順では、新しい二重書き込みソリューションを作成し、エンティティ マップを追加します。

1. Power Apps の左ウィンドウで **ソリューション** を選択し、次に **新しいソリューション** を選択して、ソリューションを作成します。 この例では、ソリューションの名前は **MyCustomEntityMaps** です。 前の手順で選択したのと同じパブリッシャーを選択してください。

    ![新しいソリューションの作成とエンティティ マップの追加](media/add-map-to-solution.png)

2. **作成**を選択します。 新しいソリューションが **ソリューション** 一覧ページに表示されます。

    ![ソリューション 一覧ページの新しいソリューション](media/show-new-solution.png)

3. 二重書き込みソリューションを作成したので、前の手順で作成したカスタマイズ済みエンティティ マップを追加できます。 作成した **MyCustomEntityMaps** ソリューションを選択し、**既存の追加** を選択して、**その他** をポイントし、**二重書き込みエンティティ マップ** を選択します。

    ![カスタマイズ済みエンティティ マップをソリューションに追加](media/add-customized-maps.png)

4. 一覧で、カスタマイズ済みエンティティ マップを選択し、ソリューションに追加します。 ソリューションには、カスタマイズ済みエンティティが含まれます。

    ![新しいソリューションのカスタマイズ済みエンティティ](media/entities-new-solution.png)

これで、エンティティをカスタマイズし、ソリューションに追加しました。

### <a name="export-and-publish-your-solution"></a>ソリューションのエクスポートと発行

ソリューション チェッカーを実行して問題がないことを確認したら、作成したソリューションをエクスポートし、変更を公開します。

1. ソリューションの一覧でソリューションを選択し、**エクスポート** を選択します。
2. バージョン番号を更新し、ソリューションをマネージドまたはアンマネージド ソリューションとしてエクスポートするかどうかを選択します。 (マネージド ソリューションとしてエクスポートすることをお勧めします。) 次に **エクスポート** を選択します。

    ![バージョン番号の更新とエクスポート](media/update-version-number.png)

3. エクスポートする前に、**すべての変更の公開** を選択し、**問題点を確認** を選択します。 完了したら、**次へ** を選択して、すべての変更を公開します。

    ![変更の公開](media/export-and-publish.png)

    ソリューションは、そのすべてのコンポーネントと共に ZIP ファイルにエクスポートされます。

    ![ZIP ファイルにエクスポートされたソリューション](media/components-to-zip.png)
    
これで、エンティティをカスタマイズして、新しいソリューションに追加し、他の環境にインポートして適用できるソリューション ファイルを作成しました。 (この機能は、テスト環境と実稼動環境の間でエンティティ マップを移動する場合に役立ちます。) 同様に、すべてのエンティティ マップのバックアップを、ソリューションに追加し、そのソリューションをパッケージとしてエクスポートすることによって作成できます。 その後、そのパッケージを任意の環境にインポートして、エンティティ マップを復元できます。

AppSource にパッケージを公開する方法の詳細については、[AppSource でアプリを公開](https://docs.microsoft.com/powerapps/developer/common-data-service/publish-app-appsource) を参照してください。

### <a name="test-your-exported-solution-package"></a>エクスポート済みソリューション パッケージのテスト

エクスポート済みソリューション パッケージは、インポートして別の環境に適用することでテストできます。

1. Power Apps で、**インポート** を選択し、パッケージを新しい環境にインポートします。

    ![パッケージを新しい環境にインポート](media/import-package.png)

2. 環境にインポートしたばかりのソリューションを適用します。

    ![ソリューションを環境に適用](media/apply-solution-to-environment.png)

3. 2 つのカスタマイズ済みエンティティ マップが、[二重書き込みエンティティ マップ] 一覧ページに表示されることを確認します。

    ![[リスト] ページの 2 つのカスタマイズ済みエンティティ マップ](media/entity-maps-in-list.png)

4. 前の手順で行ったカスタマイズが保持されていることを確認します。

    ![カスタマイズが保持されていることの確認](media/check-customizations.png)

### <a name="use-the-entity-map-version"></a>エンティティ マップ バージョンの使用

ソリューションには、エンティティ マップの異なる実装が含まれる場合があります。 たとえば、連絡先 - CDS 連絡先 V2 エンティティ マップのバージョンには、異なるパブリッシャーまたはより新しいバージョン番号が含まれる場合があります。 このような場合、**エンティティ マップ バージョン** ボタンを使用して、環境で使用するエンティティ マップを選択できます。

![環境で使用するエンティティ マップの選択](media/select-entity-map.png)

## <a name="upgrade-existing-dual-write-environments-for-solution-awareness-existing-environments"></a>ソリューション認識の既存の二重書き込み環境をアップグレードする (既存の環境)

1. 二重書き込みコア ソリューションをインポートします。

    1. このトピック前半の [二重書き込みコア ソリューションのインストール](#install-the-dual-write-core-solution) セクションの手順に従って、二重書き込みコア ソリューションを AppSource から Power Apps にインポートします。
    2. 二重書き込みコア ソリューションが PowerApps の **ソリューション** の下に一覧表示されていることを確認します。

2. エンティティ マップをアップグレードします。

    アップグレードを促す通知が表示されます。

    ![エンティティ マップをアップグレードするプロンプト](media/upgrade-prompt.png)

    ページ上部の **エンティティ マップのアップグレード** を選択します。

    ![エンティティ マップのアップグレード](media/upgrade-entity-maps.png)

アップグレードには数分かかります。 完了すると、通知が表示されます。

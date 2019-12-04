---
title: カスタム モデルの開発とオンプレミス環境への配置
description: このトピックでは、カスタマイズと拡張機能を開発し、オンプレミス環境に展開するプロセスについて説明します。
author: kfend
manager: AnnBe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 107013
ms.assetid: ''
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: cba62175bacf809eeb7a32530e35e24d8b71b941
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772353"
---
# <a name="develop-and-deploy-custom-models-to-on-premises-environments"></a>カスタム モデルの開発とオンプレミス環境への配置

[!include [banner](../includes/banner.md)]

このトピックでは、カスタマイズと拡張機能を開発してオンプレミス環境に配置する方法について説明します。 オンプレミス配置は、ローカル ビジネス データ (LBD) 環境とも呼ばれます。 。このトピックでは、このプロセスがライタイムのクラウド環境でのプロセスと異なる点について説明します。

このプロセスには、次の主要ステップが含まれています。

1. 開発環境とビルド環境の配置をします。
2. コードとカスタマイズの展開可能なパッケージを作成します。
3. 展開可能パッケージを Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトにアップロードします。
4. 配置可能なパッケージを含むオンプレミスのランタイム環境をコンフィギュレーションし、配置します。 この環境は、サンドボックス環境または実稼働環境のいずれかになります。

次のセクションでは、このプロセスの詳細について説明します。

## <a name="development-tools-and-platform"></a>開発ツールおよびプラットフォーム
クラウド アプリケーションまたはオンプレミス アプリケーションの開発、拡張、またカスタマイズに関係なく、開発プラットフォーム、ツール、および環境 (仮想マシン [VM]) は同じです。 ターゲットのランタイム環境がクラウド環境またはオンプレミス環境にあるかどうかに関係なく、カスタム コードは同じ開発用 VM 上で開発されます。

開発の詳細については、 [ホーム ページの開発とカスタマイズ](../dev-tools/developer-home-page.md) を参照してください。 拡張機能やカスタマイズの詳細については、[拡張機能のホーム ページ](../extensibility/extensibility-home-page.md) を参照してください。 構築、テスト、および継続的なデリバリーについての詳細については、 [継続的なデリバリーのホームページ](../dev-tools/continuous-delivery-home-page.md) を参照してください。

## <a name="deploy-development-and-build-environments"></a>開発環境とビルド環境の配備
Azure サブスクリプションを使用することにより、オンプレミス LCS プロジェクトを使用し、Microsoft Azure 上にビルドおよび配置環境を配置することができます。 または、ローカル開発用の仮想ハード ディスク (VHD) をダウンロードすることができます。

Azure サブスクリプションに開発環境またはビルド環境を展開する場合、または開発 VHD をダウンロードする場合は、LCS の **クラウド ホスト環境** ページを開きます。

[![クラウド ホスト環境のメニュー項目](./media/alm-flow-01.png)](./media/alm-flow-01.png)

次に、以下の手順を実行します。
    
1. **追加** をクリックします。 

    [![クラウド ホスト環境のボタンの追加](./media/alm-flow-02.png)](./media/alm-flow-02.png)
  
2. **Azure** または **ローカル** を選択します。 **ローカル** を選択した場合、開発 VHDを検索し、ダウンロードします。 **Azure** を選択した場合、次の 3 つのトポロジー、**ビルドおよびテスト**、**デモ**または**開発**から 1 つを選択するように求められます。
3. 配置の手順を完了し、Azure サブスクリプションに VM を配置します。

ローカルの開発 VHD を構成する方法の詳細については、 [開発環境の配置とアクセス](../dev-tools/access-instances.md#vm-that-is-running-on-premises) を参照してください。

> [!NOTE]
> 独自の Azure サブスクリプションに環境を展開するには、少なくとも 1 つの Azure コネクタを設定する必要があります。 Azure コネクタを設定するには、LCS で **プロジェクト設定** ページを開き、**Azure コネクタ** タブをクリックします。 その後、指示に従って Azure コネクタを追加します。 手順を完了するには、組織のテナント管理者でなければなりません。  
> [![プロジェクトの設定のメニュー項目](./media/alm-flow-03.png)](./media/alm-flow-03.png)

## <a name="create-and-upload-a-deployable-package-to-the-lcs-asset-library"></a>展開可能なパッケージを作成して LCS アセット ライブラリにアップロードする
開発のフェーズを完了し、サンド ボックスまたは実稼働環境にコードを配置する準備ができたら、モデルからアプリケーション配置可能パッケージを作成する必要があります。 このプロセスは、クラウド環境のプロセスと違いはありません。

自動ビルド (ビルド環境) を使用している場合、ビルド プロセスがアプリケーション配置可能パッケージを作成します。 また、ユーザーの開発環境で、Microsoft Visual Studio からアプリケーション展開可能パッケージを作成することもできます。 開発環境でアプリケーションの配備可能なパッケージを作成する方法の詳細については、 [モデルの展開可能なパッケージの作成](../deployment/create-apply-deployable-package.md) を参照してください。

配置可能なパッケージの準備ができたら、以下の手順に従って、そのパッケージを LCS プロジェクトの資産ライブラリにアップロードします。

1. **アセット ライブラリ**ページを開きます。

    [![資産ライブラリのメニュー項目](./media/alm-flow-04.png)](./media/alm-flow-04.png)

2. **ソフトウェア配置可能パッケージ** タブをクリックします。

    [![ソフトウェア配置可能パッケージ ファイル](./media/alm-flow-05.png)](./media/alm-flow-05.png)

3. 展開可能なパッケージをアップロードするには、プラス記号 (**+**) をクリックします。 

## <a name="configure-an-on-premises-runtime-environment-that-uses-your-code"></a>コードを使用するオンプレミスのランタイム環境をコンフィギュレーションする
2017 年 7 月リリースの Microsoft Dynamics 365 for Finance and Operations (オンプレミス) では、サンボックスの配置または実稼動環境中にのみカスタマイズや拡張機能を適用できます。

1. LCS プロジェクトで、**構成**をクリックして環境を配置します。

    [![サンドボックス 構成ボタン](./media/alm-flow-06.png)](./media/alm-flow-06.png)

2. 配置ツールで、環境名を入力する必要がある場合、**詳細設定**をクリックします。

    [![オンプレミス トポロジの詳細設定ボタン](./media/alm-flow-07.png)](./media/alm-flow-07.png)

3. **ソリューション資産のカスタマイズ** タブをクリックします。 

    [![配置設定カスタマイズ ソリューション資産タブ](./media/alm-flow-08.png)](./media/alm-flow-08.png)

4. **展開する AOT パッケージの選択**フィールドで、カスタマイズを含むアプリケーション (AOT) の展開可能パッケージを選択します。 このフィールドには、アセット ライブラリのすべての AOT パッケージがリストされます。
5. **完了**をクリックして**配置設定**ページを閉じ、環境の展開プロセスを続行します。

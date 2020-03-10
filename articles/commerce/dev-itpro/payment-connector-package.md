---
title: Service Fabric 配置でアプリケーション エクスプローラーの支払パッケージの作成
description: このトピックでは、アプリケーション エクスプローラーの支払パッケージを作成して、Dynamics 365 Commerce の Microsoft Azure Service Fabric 環境に配置する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 02/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a518d3ec50876164adfcbc18dd4dfdf1a18ab282
ms.sourcegitcommit: 1e181db51abbf70bbf1f9af8ad6d8c67bafe5adb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/25/2020
ms.locfileid: "3082099"
---
# <a name="create-payment-packaging-for-application-explorer-in-service-fabric-deployments"></a>Service Fabric 配置でアプリケーション エクスプローラーの支払パッケージの作成

[!include [banner](../../includes/banner.md)]

このトピックでは、アプリケーション エクスプローラーの支払パッケージを作成して、Dynamics 365 Commerce の Microsoft Azure Service Fabric 環境に配置する方法について説明します。

10.0.10 以前のリリースでは、コマース ソフトウェア開発キット (SDK) を使用して支払パッケージを作成します。 (以前は Commerce SDK は Retail SDK と呼ばれていました。) 10.0.10 リリース以降では、Visual Studio のみを使用して Application Object Server (AOS) 支払パッケージを作成できます。 この方法を使用して作成するパッケージは、Service Fabric 環境およびサービスとしてのインフラストラクチャ (IaaS) 環境の両方に配置できます。

> [!NOTE]
> 10.0.10 以前のリリースでは、単一の支払パッケージを作成し、それをアプリケーション エクスプローラーとコマース チャネルおよびクラウド コンポーネント (Commerce Scale Unit) の両方に使用できます。 10.0.10 リリースでは、2 つのパッケージを作成する必要があります。 1 つのパッケージはアプリケーション エクスプローラー用で、Dynamics 365 パッケージング モデルを使用して作成します。 もう 1 つのパッケージは、コマース チャネルとクラウド コンポーネント用で、コマース SDK を使用して作成します。 コマース SDK を使用してアプリケーション エクスプローラー支払パッケージを作成した以前の方法は、10.0.10 リリースの時点で廃止 (非推奨) となります。

Commerce Service Fabric 配置で配置できる支払パッケージを作成するには、次のセクションの手順を実行します。

> [!NOTE]
> コマース チャネルとクラウド コンポーネント用パッケージを作成するため、コマース SDK を使用する手順は変更されていません。 詳細については、「[コネクタの作成と配置](deploy-payment-connector.md)」を参照してください。

## <a name="create-an-aos-payment-package-in-the-10010-release"></a>10.0.10 リリースでの AOS 支払パッケージの作成

1. Visual Studio の、**Dynamics 365** メニューで、**モデル管理 \> モデルの作成**をクリックします。
2. モデル名、モデル発行元、およびその他の必要な詳細を入力します。 その後、**次へ** を選択します。

    モデル名には、**RetailPaymentConnectors** の接頭語を付ける必要があります。 この接頭語の後に、カスタム モデル名に関する情報を追加します。 たとえば、作成するモデルには **RetailPaymentConnectorsCustomConnector** という名前が付けられます。 **RetailPaymentConnectors** の接頭語で始まるモデル名のみが、コマース支払コネクタ オプションに読み込まれます。

    ![モデルの作成ウィザードでのパラメーター ページの追加](./media/CreateModel.png)

3. **新しいパッケージの作成**オプションを選択し、**次へ**を選択します。
4. 必要な参照パッケージを選択し、**次へ**を選択します。
5. **完了**を選択して、モデルの作成を終了します。
6. ソリューション エクスプローラーで、プロジェクトを選択し、**参照**を右クリックしてから、**参照の追加**を選択します。
7. すべての支払コネクタ アセンブリとその依存関係を、プロジェクトに参照として追加します。

    ![参照ダイアログ ボックスの追加](./media/Reference.png)

8. 支払コネクタに関連付けられているその他の支払 X++ 拡張機能がない場合、ソリューションをビルドします。
9. 配備可能なパッケージを作成するには、**Dynamics 365** メニューで、**配置 \> 配置パッケージの作成**を選択します。
10. 以前に作成したモデルを選択し、パッケージ ファイルの場所を指定してから、**作成**を選択します。

    ![配置パッケージ ダイアログ ボックスの作成](./media/Create.png)

    Visual Studio はモデルをビルドし、配置可能なパッケージを作成します。

10. 配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインしてから、LCS プロジェクトで、**資産ライブラリ** タイルを選択します。
11. 作成した展開可能なパッケージをアップロードします。

## <a name="apply-a-deployable-package"></a>配置可能パッケージの適用

配置可能パッケージの環境への適用方法については、 [クラウド環境への更新プログラムの適用](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。

## <a name="remove-a-deployable-package"></a>配置可能パッケージの削除

環境から配置可能パッケージをアンインストールまたは削除する方法についての詳細は、[パッケージのアンインストール](../../fin-ops-core/dev-itpro/deployment/uninstall-deployable-package.md) を参照してください。

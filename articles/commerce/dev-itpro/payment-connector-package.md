---
title: セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce でセルフサービス配置用にアプリケーション エクスプローラーの支払コネクタをパッケージ化する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 05/14/2020
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
ms.openlocfilehash: c3c75bb4ab1be13edf465f3ab45bdd692b207f73
ms.sourcegitcommit: 78a1aa37f9a1565135b139e36501b759e7b2f849
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2020
ms.locfileid: "3374809"
---
# <a name="create-payment-packaging-for-application-explorer-for-self-service-deployment"></a>セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce でセルフサービス配置用にアプリケーション エクスプローラーの支払コネクタをパッケージ化する方法について説明します。

10.0.10 より前のリリースでは、コマース ソフトウェア開発キット (SDK) を使用して支払コネクタ パッケージを作成します。 (以前は Commerce SDK は Retail SDK と呼ばれていました。) 10.0.10 リリース以降では、Visual Studio のみを使用して Application Object Server (AOS) 支払コネクタ パッケージを作成できます。 この方法を使用して作成したパッケージは、[オールイン ワンパッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md) を使用して、以前の展開とセルフサービス配置の両方に展開できます。

> [!NOTE]
> 10.0.10 以前のリリースでは、単一の支払パッケージを作成し、それをアプリケーション エクスプローラーとコマース チャネルおよびクラウド コンポーネント (Commerce Scale Unit) の両方に使用できます。 10.0.10 リリースでは、2 つのパッケージを作成する必要があります。 1 つのパッケージはアプリケーション エクスプローラー用で、Dynamics 365 パッケージング モデルを使用して作成します。 もう 1 つのパッケージは、コマース チャネルとクラウド コンポーネント用で、コマース SDK を使用して作成します。 コマース SDK を使用してアプリケーション エクスプローラー支払パッケージを作成した以前の方法は、10.0.10 リリースの時点で廃止 (非推奨) となります。

セルフ サービスで配置できる支払パッケージを作成するには、次のセクションの手順に従います。

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

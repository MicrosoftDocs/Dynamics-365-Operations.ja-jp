---
title: 財務と運用の展開のための Commerce 支払パッケージの作成
description: この記事では、Microsoft Dynamics 365 Commerce の財務と運用の展開に支払コネクタをパッケージ化する方法について説明します。
author: mugunthanm
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2020-02-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 22b77e4a4b8a19a37c709641b3833c0545ea9aa7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860269"
---
# <a name="create-commerce-payment-packaging-for-finance-and-operations-deployment"></a>財務と運用の展開のための Commerce 支払パッケージの作成

[!include [banner](../../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce の財務と運用の展開に支払コネクタをパッケージ化する方法について説明します。

10.0.10 より前のリリースでは、コマース ソフトウェア開発キット (SDK) を使用して支払コネクタ パッケージを作成します。 (以前は Commerce SDK は Retail SDK と呼ばれていました。) 10.0.10 リリース以降では、Visual Studio のみを使用して Application Object Server (AOS) 支払コネクタ パッケージを作成できます。 この方法を使用して作成したパッケージは、[オールイン ワンパッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md) を使用して、以前の展開とセルフサービス配置の両方に展開できます。

> [!NOTE]
> 10.0.10 以前のリリースでは、単一の支払パッケージを作成し、それをアプリケーション エクスプローラーとコマース チャネルおよびクラウド コンポーネント (Commerce Scale Unit) の両方に使用できます。 10.0.10 リリースでは、2 つのパッケージを作成する必要があります。 1 つのパッケージはアプリケーション エクスプローラー用で、Dynamics 365 パッケージング モデルを使用して作成します。 もう 1 つのパッケージは、コマース チャネルとクラウド コンポーネント用で、コマース SDK を使用して作成します。 コマース SDK を使用してアプリケーション エクスプローラー支払パッケージを作成した以前の方法は、10.0.10 リリースの時点で廃止 (非推奨) となります。

配置できる支払パッケージを作成するには、次のセクションの手順に従います。

> [!NOTE]
> コマース チャネルとクラウド コンポーネント用パッケージを作成するため、コマース SDK を使用する手順は変更されていません。 詳細については、「[コネクタの作成と配置](deploy-payment-connector.md)」を参照してください。

## <a name="create-an-aos-payment-package-in-the-10010-release"></a>10.0.10 リリースでの AOS 支払パッケージの作成

1. Visual Studio の、**Dynamics 365** メニューで、**モデル管理 \> モデルの作成** をクリックします。
2. モデル名、モデル発行元、およびその他の必要な詳細を入力します。 その後、**次へ** を選択します。

    モデル名には、**RetailPaymentConnectors** の接頭語を付ける必要があります。 この接頭語の後に、カスタム モデル名に関する情報を追加します。 たとえば、作成するモデルには **RetailPaymentConnectorsCustomConnector** という名前が付けられます。 **RetailPaymentConnectors** の接頭語で始まるモデル名のみが、コマース支払コネクタ オプションに読み込まれます。

    ![モデルの作成ウィザードにパラメーター ページを追加します。](./media/CreateModel.png)

3. **新しいパッケージの作成** オプションを選択し、**次へ** を選択します。
4. 必要な参照パッケージを選択し、**次へ** を選択します。
5. **完了** を選択して、モデルの作成を終了します。
6. ソリューション エクスプローラーで、プロジェクトを選択し、**参照** を右クリックしてから、**参照の追加** を選択します。
7. すべての支払コネクタ アセンブリとその依存関係を、プロジェクトに参照として追加します。

    ![参照ダイアログ ボックスを追加します。](./media/Reference.png)
    
[!NOTE]
> すべての支払いコネクタ dll は移動可能である必要があります。移動可能および移動不可の支払いコネクタ dll があると、コネクタの読み取り時に問題が発生します。

8. 拡張機能を実装するのに HTML と CSS ファイルが必要な場合 、それらをリソース ファイルとしてプロジェクトに追加します。 配置中は、HTML ファイルが AosService\WebRoot\Resources\Html フォルダーにコピーされます。 CSS ファイルは AosService\WebRoot\Resources\Styles フォルダーにコピーされ、次の URL 形式を使用してアクセスすることができます。

例: GetPaymentAcceptPoint の実装は、必要に応じてこの URL を返す更新する必要があります。

```
https://AOSUrl/resources/html/Myhtml.html
https://AOSUrl/resources/styles/Mycss.css
```
> [!NOTE]
> リソースとしてプロジェクトに追加された HTML および CSS ファイルは AosService\WebRoot\, にコピーされ、リソースとして追加された他のファイル形式は AosService\WebRoot\. にコピーされません。 AosService\WebRoot\ フォルダーのファイルが必要な場合、HTML ファイル形式に移行するか、またはサポートされていないファイル形式を外部でホストします。 外部でホストされている場合、カスタマイズまたはパートナーがホスティングを管理する必要があります。

9. 支払コネクタに関連付けられているその他の支払 X++ 拡張機能がない場合、ソリューションをビルドします。

> [!NOTE]
> 他の拡張機能パッケージが存在しない場合は、次の手順に進みます。 追加の拡張機能パッケージがある場合は、すべてを 1 つの配置可能なパッケージに結合させます。 これを行わないと、このパッケージは他のパッケージを上書きします。 詳細については、「[オールインワン配置可能パッケージ](../../fin-ops-core/dev-itpro/dev-tools/aio-deployable-packages.md)」を参照してください。

10. 配備可能なパッケージを作成するには、**Dynamics 365** メニューで、**配置 \> 配置パッケージの作成** を選択します。
11. 以前に作成したモデルを選択し、パッケージ ファイルの場所を指定してから、**作成** を選択します。


    ![配置パッケージ ダイアログ ボックスを作成します。](./media/Create.png)

    Visual Studio はモデルをビルドし、配置可能なパッケージを作成します。

12. 配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインしてから、LCS プロジェクトで、**資産ライブラリ** タイルを選択します。
13. 作成した展開可能なパッケージをアップロードします。

## <a name="apply-a-deployable-package"></a>配置可能パッケージの適用

配置可能パッケージの環境への適用方法については、 [クラウド環境への更新プログラムの適用](../../fin-ops-core/dev-itpro/deployment/apply-deployable-package-system.md) を参照してください。

## <a name="remove-a-deployable-package"></a>配置可能パッケージの削除

環境から配置可能パッケージをアンインストールまたは削除する方法についての詳細は、[パッケージのアンインストール](../../fin-ops-core/dev-itpro/deployment/uninstall-deployable-package.md) を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

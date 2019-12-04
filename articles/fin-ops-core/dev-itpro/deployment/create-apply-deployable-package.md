---
title: モデルの配置可能パッケージを作成する
description: このトピックでは、展開可能なパッケージを作成および適用するためのワークフローについて説明します。
author: robadawy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f9a7aee52ba422b177ed15890242b209fd050d6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772350"
---
# <a name="create-deployable-packages-of-models"></a>モデルの配置可能パッケージを作成する

[!include [banner](../includes/banner.md)]

AOT パッケージは、環境に適用することのできる、1 つまたは複数のモデルの配置およびコンパイル単位です。 これには、モデル メタデータ、バイナリ、レポートおよびその他の関連するリソースが含まれます。 1 つ以上の AOT パッケージは、デモ、サンド ボックスおよび生産環境でのコード (およびカスタマイズ) の配置に使用する車両の配置可能パッケージにパッケージすることができます。 この記事では、展開可能なパッケージの作成と適用のプロセスについて説明します。 

## <a name="overview-of-the-process"></a>プロセスの概要

ランタイム環境 (デモ、サンドボックスまたは実稼働) にコードおよびカスタマイズを配置するためには、ソリューションまたは実装の配置可能パッケージを作成する必要があります。 **Visual Studio 開発ツール**、またはビルド環境で使用可能な**ビルドの自動化プロセス**を使用して、配置可能パッケージを作成することができます。 これらの配置可能なパッケージは、アプリケーション配置可能パッケージまたは AOT 配置可能パッケージと呼ばれます。 以下のイメージはプロセスの概要です。 配置可能パッケージが作成されたら、LCS プロジェクトの資産ライブラリにアップロードする必要があります。 管理者は LCS 環境のページに移動し、**メンテナンス &gt; 更新プログラムの適用**ツールを使用してランタイム環境にパッケージを適用できます。 

![配置パッケージの作成と適用](./media/createandapplydeployablepackage.png)

> [!NOTE]
> アプリケーション配置可能パッケージにはソース コードが含まれていません。

> 本番環境への移行を目的にした配置可能パッケージを作成するには、ビルド環境を使用することを常にお勧めします。

## <a name="create-a-deployable-package"></a>配置可能パッケージの作成
配置可能パッケージを作成するにはビルド環境を使用することをお勧めします。 開発環境で配置可能パッケージを作成することもできます。 

開発環境では、開発とテストを完了した後で、次の手順に従って Visual Studio で配置可能パッケージを作成します。

1.  Microsoft Visual Studio で、**Dynamics 365** &gt; **配置** &gt; **配置パッケージの作成**を選択します。
![配置パッケージの作成](./media/createdeploymentpackage-986x1024.png)

2.  モデルを含むパッケージを選択し、展開可能なパッケージを作成する場所を選択します。 
![場所の選択](./media/pack4.png)

3.  配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、LCS プロジェクトで、**資産ライブラリ**タイルをクリックします。

4.  先ほど作成した展開可能なパッケージをアップロードします。

## <a name="apply-a-deployable-package"></a>配置可能パッケージの適用
展開可能なパッケージを環境に適用する方法については、 [クラウド環境に更新を適用する](apply-deployable-package-system.md) を参照してください。

## <a name="remove-a-deployable-package"></a>配置可能パッケージの削除
環境から配置可能パッケージをアンインストールしたり、削除したりするには、 [パッケージ のアンインストール](uninstall-deployable-package.md) の記事を参照してください。

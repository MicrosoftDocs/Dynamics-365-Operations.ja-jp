---
title: モデルの配置可能パッケージを作成する
description: このトピックでは、展開可能なパッケージを作成および適用するためのワークフローについて説明します。
author: jorisdg
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24211
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8121021b1bc015b83d79db5645582fa2310c502f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748795"
---
# <a name="create-deployable-packages-of-models"></a>モデルの配置可能パッケージを作成する

[!include [banner](../includes/banner.md)]

AOT パッケージは、環境に適用することのできる、1 つまたは複数のモデルの配置およびコンパイル単位です。 これには、モデル メタデータ、バイナリ、レポートおよびその他の関連するリソースが含まれます。 1 つ以上の AOT パッケージは、デモ、サンド ボックスおよび生産環境でのコード (およびカスタマイズ) の配置に使用する車両の配置可能パッケージにパッケージすることができます。 このトピックでは、展開可能なパッケージの作成と適用のプロセスについて説明します。 

## <a name="overview-of-the-process"></a>プロセスの概要

ランタイム環境 (デモ、サンドボックスまたは実稼働) にコードおよびカスタマイズを配置するためには、ソリューションまたは実装の配置可能パッケージを作成する必要があります。 **Visual Studio 開発ツール**、またはビルド環境で使用可能な **ビルドの自動化プロセス** を使用して、配置可能パッケージを作成することができます。 これらの配置可能なパッケージは、アプリケーション配置可能パッケージまたは AOT 配置可能パッケージと呼ばれます。 次の図は、プロセスの概要を表示します。 配置可能パッケージが作成されたら、Lifecycle Services (LCS) プロジェクトの資産ライブラリにアップロードする必要があります。 管理者は LCS 環境のページに移動し、**メンテナンス &gt; 更新プログラムの適用** ツールを使用してランタイム環境にパッケージを適用できます。 

> [!NOTE]
> 結合した AOT 配置可能パッケージを使用して、Commerce 用カスタム支払コネクタをパッケージ化する必要があります。 詳細については、[Service Fabric 配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。

![配置パッケージの作成と適用](./media/createandapplydeployablepackage.png)

> [!NOTE]
> アプリケーション配置可能パッケージにはソース コードが含まれていません。

> 本番環境への移行を目的にした配置可能パッケージを作成するには、ビルド環境を使用することを常にお勧めします。

## <a name="create-a-deployable-package"></a>配置可能パッケージの作成
配置可能パッケージを作成するにはビルド環境を使用することをお勧めします。 開発環境で配置可能パッケージを作成することもできます。 

開発環境では、開発とテストを完了した後で、次の手順に従って Visual Studio で配置可能パッケージを作成します。

1.  Microsoft Visual Studio で、**Dynamics 365** &gt; **配置** &gt; **配置パッケージの作成** を選択します。
![配置パッケージの作成](./media/createdeploymentpackage-986x1024.png)

2.  モデルを含むパッケージを選択し、展開可能なパッケージを作成する場所を選択します。 
![場所の選択](./media/pack4.png)

3.  配置可能パッケージが作成された後、Lifecycle Services にサインインし、LCS プロジェクトで、**資産ライブラリ** タイルをクリックします。

4.  先ほど作成した展開可能なパッケージをアップロードします。

## <a name="apply-a-deployable-package"></a>配置可能パッケージの適用
展開可能なパッケージを環境に適用する方法については、[クラウド環境に更新を適用する](apply-deployable-package-system.md)を参照してください。

## <a name="remove-a-deployable-package"></a>配置可能パッケージの削除
環境から配置可能パッケージをアンインストールしたり、削除したりするには、[パッケージ のアンインストール](uninstall-deployable-package.md)を参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
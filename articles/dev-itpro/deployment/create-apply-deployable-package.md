---
title: "配置可能パッケージの作成"
description: "このトピックでは、展開可能なパッケージを作成および適用するためのワークフローについて説明します。"
author: robadawy
manager: AnnBe
ms.date: 10/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 24211
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: ed666e4e6091c58171e6dc69b6d58927c654cf0f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="create-a-deployable-package-of-your-models-in-order-to-apply-it-to-a-runtime-environment"></a>ランタイム環境に適用するために、モデルの配置可能パッケージを作成する

[!include [banner](../includes/banner.md)]

AOT パッケージは、Microsoft Dynamics 365 for Finance and Operations 環境または Retail 環境の Microsoft Dynamics 365 に適用できる 1 つまたは複数のモデルの配置およびコンパイル単位です。 これには、モデル メタデータ、バイナリ、レポートおよびその他の関連するリソースが含まれます。 1 つ以上の AOT パッケージは、デモ、サンド ボックスおよび生産環境でのコード (およびカスタマイズ) の配置に使用する車両の配置可能パッケージにパッケージすることができます。 この記事では、展開可能なパッケージの作成と適用のプロセスについて説明します。 

## <a name="overview-of-the-process"></a>プロセスの概要

ランタイム環境 (デモ、サンドボックスまたは実稼働) にコードおよびカスタマイズを配置するためには、ソリューションまたは実装の配置可能パッケージを作成する必要があります。 **Visual Studio 開発ツール**、ビルド環境で有効な**ビルドの自動化プロセス**で配置可能パッケージを作成することができます。 これらの配置可能なパッケージは、アプリケーション配置可能パッケージまたは AOT 配置可能パッケージと呼ばれます。 以下のイメージはプロセスの概要です。 配置可能パッケージが作成されたら、LCS プロジェクトの資産ライブラリにアップロードする必要があります。 管理者は LCS 環境のページに移動し、**メンテナンス &gt; 更新プログラムの適用**ツールを使用してランタイム環境にパッケージを適用できます。 

![配置パッケージの作成と適用](./media/createandapplydeployablepackage.png)

> [!NOTE]
> アプリケーション配置可能パッケージにはソース コードが含まれていません。

## <a name="create-a-deployable-package"></a>配置可能パッケージの作成
開発ステージを完了すると、以下の手順に従って Visual Studio から配置可能パッケージを作成します。

1.  Microsoft Visual Studio で、**Dynamics 365** &gt; **配置** &gt; **配置パッケージの作成**を選択します。
![配置パッケージの作成](./media/createdeploymentpackage-986x1024.png)

2.  モデルを含むパッケージを選択し、展開可能なパッケージを作成する場所を選択します。 
![場所の選択](./media/pack4.png)

3.  配置可能パッケージが作成された後、Microsoft Dynamics Lifecycle Services (LCS) にサインインし、LCS プロジェクトで、**資産ライブラリ** タイルをクリックします。

4.  先ほど作成した展開可能なパッケージをアップロードします。

## <a name="apply-a-deployable-package"></a>配置可能パッケージの適用
展開可能なパッケージを環境に適用する方法については、[[展開可能なパッケージの適用](apply-deployable-package-system.md)] を参照してください。


---
title: 分析コード ベース製品コンフィギュレーションの概要
description: 分析コード ベースの製品コンフィギュレーションは、1 つの製品マスターと部品表から多くの製品バリアントを作成するための単純なソリューションを表します。
author: t-benebo
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19821"
- intro-internal
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9ba11a561f320a7f4e787e4fe3f4e6f4fb88bbfb
ms.sourcegitcommit: ca73177dedf40df16860eaf88b1c701c61992028
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2022
ms.locfileid: "9754113"
---
# <a name="dimension-based-product-configuration-overview"></a>分析コード ベース製品コンフィギュレーションの概要

[!include [banner](../includes/banner.md)]

分析コード ベースの製品コンフィギュレーションは、1 つの製品マスターと部品表から多くの製品バリアントを作成するための単純なソリューションを表します。

分析コード ベースの製品コンフィギュレーションは、3 つの組み込みの製品コンフィギュレーション テクノロジーの 1 つです。 他の 2 つのテクノロジは、定義済バリアントと制約ベースのコンフィギュレーションです。 3 つのテクノロジはすべて開始点として製品マスターを使用し、ユーザーは 1 つの製品マスターに多くの製品バリアントを作成できます。

## <a name="key-concepts"></a>重要な概念
分析コード ベースの製品コンフィギュレーションは次の重要な概念に基づいています。

-   製品マスター
-   製品分析コードのコンフィギュレーション
-   コンフィギュレーション グループ
-   部品表 (BOM)
-   コンフィギュレーション ルート
-   コンフィギュレーション ルール

### <a name="product-masters"></a>製品マスター

製品マスターは、製品コンフィギュレーション プロセスの開始点です。 分析コード ベースの製品コンフィギュレーションでは、この特定のコンフィギュレーション テクノロジを使用した製品マスターとコンフィギュレーション製品分析コードを含む製品分析コード グループが必要です。

### <a name="configuration-product-dimension"></a>製品分析コードのコンフィギュレーション

製品分析コードのコンフィギュレーションは、分析コード ベースのコンフィギュレーション テクノロジを使用した製品マスターの製品バリアントを識別するために使用します。 コンフィギュレーション分析コード値はユーザーが入力し、個々の製品バリアントの識別に役立ちます。

### <a name="configuration-groups"></a>コンフィギュレーション グループ

コンフィギュレーション グループは、中央レポジトリで定義され、すべての分析コード ベースの製品コンフィギュレーション モデルに使用できます。 コンフィギュレーション グループは、個々の BOM 明細行に関連付けられ、相互に排他的な明細行のグループをまとめます。 これは、1 つの製品バリアントに 1 つのグループの 1 つの明細行だけが選択できることを意味します。

### <a name="bill-of-materials-bom"></a>部品表 (BOM)

BOM は、分析コード ベースの製品コンフィギュレーションの構成要素を表します。 これには、製品バリアントに使用できるすべての異なる製品を含める必要があります。 BOM の各行は、コンフィギュレーション グループを参照できます。 明細行がコンフィギュレーション グループを参照しない場合は、すべての製品バリアントに含まれます。

### <a name="configuration-route"></a>コンフィギュレーション ルート

コンフィギュレーション ルートは、製品コンフィギュレーション プロセス中にユーザーが表示するときのコンフィギュレーション グループの順序を決定します。

### <a name="configuration-rules"></a>コンフィギュレーション ルール

コンフィギュレーション ルールは、ある BOM の 1 つのコンフィギュレーション グループに含まれている製品が、同じ BOM の別のコンフィギュレーション グループで他の製品を包含または排除することを確認するしくみを表します。

## <a name="product-modeling-process"></a>製品モデリング プロセス
分析コード ベースの製品の製品モデル作成のための正常な順序は、関連するコンフィギュレーション グループの定義で始まります。 BOM で使用されるすべての製品が、製品モデルが作成された会社にリリース済みであることを確認することは重要です。 ユーザーは、これらの構成要素を適切な場所で使用して、BOM を作成し、コンフィギュレーション グループを関連するすべての BOM 明細行に割り当てることができます。 BOM が完了すると、コンフィギュレーション ルートを、適切な順序でコンフィギュレーション グループの注文で定義できます。 [![分析コード ベース製品モデリング プロセス。](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) 一緒に使用する必要がある、または使用してはならない異なるコンフィギュレーション グループの特定の製品がある場合は、これらの製品関係を適用するコンフィギュレーション ルールを作成できます。 BOM が BOM バージョンを介して分析コード ベースの製品マスターと結ばれ、両方とも承認され有効化されると、製品コンフィギュレーションを作成して、各コンフィギュレーションの名前を入力できます。 コンフィギュレーションは、トランザクションが生成される前に定義することができ、また特定のコンフィギュレーションの必要性が発生したときに定義することができます。

### <a name="suggested-use"></a>推奨される使用

分析コード ベースのコンフィギュレーション テクノロジは、限られた可変性の製品に使用されます。また、標準的な製品分析コード サイズ、色、スタイル、およびコンフィギュレーションの組み合わせは、特定の製品バリアントを識別するのに不適切です。 例として、フレームの高さ、ホイールのサイズ、ブレーキ タイプ、およびさまざまなギヤを含む自転車が考えられます。

### <a name="next-step"></a><a name="sequence"></a>次のステップ

以下の 8 つのタスク ガイドは、実行する必要のある順番で一覧表示されています。 

1.  [分析コードベースの製品マスターの作成](tasks/create-dimension-based-product-master.md)
2.  [分析コードベースの製品マスターのリリース](tasks/release-dimension-based-product-master.md)
3.  [リリース済み製品マスターの基本設定の完了](tasks/complete-basic-setup-released-product-master.md)
4.  [コンフィギュレーション グループの定義](tasks/define-configuration-groups.md)
5.  [分析コードベースの製品マスターの部品表の作成](tasks/create-bill-materials-dimension-based-product-master.md)
6.  [コンフィギュレーション ルートの定義](tasks/define-configuration-route.md)
7.  [コンフィギュレーション ルールの作成](tasks/create-configuration-rules.md)
8.  [分析コードベースのコンフィギュレーションの作成](tasks/create-dimension-based-configurations.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
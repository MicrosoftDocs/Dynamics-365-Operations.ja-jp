---
title: ファントム品目
description: このトピックでは、部品表 (BOM) の明細行および Dynamics 365 Supply Chain Management のフォーミュラで、ファントム明細行タイプを使用する方法を詳細に説明します。
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432147"
---
# <a name="phantom-items"></a>ファントム品目

[!include [banner](../includes/banner.md)]

このトピックでは、部品表 (BOM) の明細行およびフォーミュラで、ファントム明細行タイプを利用する方法を詳細に説明します。 次の図では、(a) は製品 H およびパーツ F と G の BOM、(b) は製品 H およびパーツ F の工順シートです。

![製品 H およびパーツ F](media/product-H-part-F.png)


次の図は、2 つのレベルでの BOM 構造の例を示します。 完成した製品 H は、機械アセンブリの製品を表します。 機械アセンブリは、2 つの材料 (A と B) を持つ電気単位 (F)、および 2 つの材料 (C と D) も持つ梱包材のグループ (G) の 2 つの部分から構成されます。 他の材料 (E) は、機械の一般的なアセンブリで使用されます。

![製品 H およびパーツ F](media/product-H-part-B.png)

前の図は製品 H のエンジニアリング BOM を表します。この構造はパーツおよび機械アセンブリ全体のコンポーネントの適正な概要を提供します。 ただし、製品デザイナーがこの方法で表される BOM を好む場合でも、この構造では作業現場で機械が構築される方法が正しく表されていない場合があります。 

たとえば、前の図でエンジニアリング BOM は、その電気単位 F が別のワーク オーダーで別のパーツとして組み立てられていることを示します。 ただし、作業現場では、別のワーク オーダーとしてではなく、機械アセンブリ全体のパーツとして電気単位を組み立てるのにより最適であると判断される可能性があります。

このエンジニアリング BOM は、パーツ G が別のパーツであることも示します。 ただし、この構造では、パーツ G は現物パーツでなく梱包材のコレクションを表します。 

したがって、エンジニアリング BOM は製品のデザインおよびそのデザインのメンテナンスに大きな価値を提供しますが、製品の製造実行プロセスをサポートする最も論理的な方法ではない可能性があります。 対照的に、製造 BOM は製品を構築する最善の方法を表します。

次の図は、前のエンジニアリング BOM を製造 BOM に移行する方法を示します。 この図では、(a) は製品 H の BOM、b は製品 H の工順シートです。

この構造では、パーツ F および G の概念がなく、これらのパーツで構成される材料が次の BOM レベルに上昇したことを確認できます。 

2 つの操作シートがあったエンジニアリング BOM とは異なり、製造 BOM には 1 つの操作シートのみがあります。 パーツ G にリンクされた梱包操作も上昇し、製品 H の操作シートの一部になりました。電気単位のアセンブリは最初の操作です。 この単位は次の操作である機械アセンブリに使用されるため、この順序は理にかなっています。 最後の操作は、2 つの梱包材 (C と D) を消費する梱包操作です。

ファントム BOM 明細行タイプを通して、エンジニアリング BOM と製造 BOM 間での移行が有効になります。 「ファントム」という用語が示すように、パーツ F および G が 2 つの BOM タイプ間の移行中に実在しなくなりました。 この例では、エンジニアリング BOM で、ファントム明細行タイプがパーツ F および G の BOM 明細行に適用されます。 製造オーダーまたはバッチ オーダーが作成されると、エンジニアリング BOM は製造オーダーまたはバッチ オーダーにコピーされます。 次に、前の図に示すように、オーダーの見積時にエンジニアリング BOM から製造 BOM への移行が発生します。 2 番目の図の操作シートから、操作用に梱包材 C および D が入力されます。 

## <a name="multilevel-phantom-bom-structures"></a>複数レベルのファントム BOM 構造
次の図に示すように、ファントム明細行タイプは複数レベルの BOM 構造で使用できます。 この図では、(a) は製品 G の BOM、(b) はパーツ E と F および製品 G の工順シートです。 

![工順シートを含む製品 G およびパーツ F](media/product-G-route-sheet-G.png)


次の図では、パーツ E および F の BOM 明細行が、明細行タイプがファントムであるようコンフィギュレーションされている場合に、製造 BOM と工順シートの計算結果を示します。 この図では、(a) は製品 G の BOM、(b) は製品 G の工順シートです。

![製品 G](media/product-G.png)


## <a name="phantom-and-route-network"></a>ファントムおよび工順ネットワーク
ファントム BOM は、工順ネットワークのある BOM にも使用できます。 工順ネットワークでは、1 つ以上の操作が並列実行されます。 次の図は、複数レベルの BOM で使用される工順ネットワークの例を示します。 この図では、(a) は製品 G およびパーツ F のBOM、(b) は工順ネットワークのある製品 G およびパーツ F の工順シートです。

![製品 G およびパーツ F](media/product-G-part-F.png)


次の図では、(a) は製品 G およびパーツ F の BOM、(b) は製品 G およびパーツ F の工順シートです。

![工順シートを含む製品 G およびパーツ F](media/product-G-part-F-with-route-sheet.png)

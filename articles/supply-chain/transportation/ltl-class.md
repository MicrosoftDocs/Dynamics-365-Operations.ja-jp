---
title: トラック 1 台分未満 (LTL) のクラス
description: このトピックでは、トラック 1 台分未満 (LTL) のクラスについて説明し、Microsoft Dynamics 365 Supply Chain Management での設定方法について説明します。
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941813"
---
# <a name="less-than-truckload-ltl-classes"></a>トラック 1 台分未満 (LTL) のクラス

[!include [banner](../includes/banner.md)]

トラック 1 台分未満 (LTL) のクラスは、出荷可能な品目の分類に使用される貨物出荷クラスです。 一般に、製品または商品のすべてのタイプに、LTL 出荷の特定の貨物クラス番号に対応する貨物輸送分類 (NMFC) コードが設定されています。 LTL 貨物クラスは品目のカテゴリを表しますが、NMFC コードは 18 の各貨物クラスの特定の商品に関連しています。

この機能を使用すると、システムで次のタスクを実行できます:

- 会社で使用する LTL 貨物クラスを定義します。
- 各 LTL クラスを **NMFC コード** ページの NMFC コードに割り当てます。 詳細については、 [貨物輸送分類 (NMFC) コード](nmfc-codes.md) を参照してください。
- NMFC コード (および NMFC コードに関連付けられた LTL コード) を **製品** ページの各製品に割り当てます。
- NMFC コードが割り当てられている各製品の LTL クラスを正確に評価します。
- 国際的な LTL 標準を確認して、各 LTL クラスの梱包要件を決定します。 この方法により、製品が保護され、安全に出荷されることを確認できます。
- 各製品の LTL 貨物クラスに基づいて、正確な出荷見積を取得します。

このトピックでは、Microsoft Dynamics 365 Supply Chain Management で LTL クラスを作成する方法について説明します。

## <a name="create-an-ltl-class"></a>LTL クラスの作成

LTL クラスを作成するには、次の手順を実行します。

1. 次の手順のいずれかを実行します。

    - **倉庫管理 \> 設定 \> 在庫 \> LTL クラス** の順に移動します。
    - **輸送管理 \> 設定 \> 輸送標準 \> LTL クラス** の順に移動します。

2. アクション ウィンドウで **新規** を選択し、LTL クラスを作成します。 その後、次のフィールドを設定します:

    - **LTL クラス** – 商品タイプに対する会社の内部 LTL クラス識別子 (ID) を入力します。 ほとんどの会社では国際標準を使用しています。 その場合、このフィールドの値は **クラス** フィールドの値と一致します。 ただし、会社が独自の標準を使用している場合は、その標準に準拠するコードを入力します。
    - **名前** – 自分やほかのユーザーが各 NMFC コードに対して正しい LTL クラスを選択するのに役立つ内容を示す名前を入力します。
    - **クラス** – 商品タイプの国際標準 LTL クラス ID を入力します。 ここで入力するコードは、公式の標準に準拠している必要があります。

## <a name="example-set-up-ltl-classes"></a>例: LTL クラスの設定

次の例は、異なるタイプの製品で使用できる 2 つの異なる LTL クラスの設定方法を示します。

1. **倉庫管理 \> 設定 \> 在庫 \> LTL クラス** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. 新しい明細行で、次の値を設定します。

    - **LTL クラス :** *92.5*
    - **名前 :** *コンピューター、モニター、冷蔵庫*
    - **クラス :** *92.5*

1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**新規** を選択します。
1. 新しい明細行で、次の値を設定します。

    - **LTL クラス :** *125*
    - **名前 :** *小さな家庭電化製品*
    - **クラス :** *125*

1. アクション ウィンドウで、**保存** を選択します。

## <a name="additional-resources"></a>追加リソース

- [貨物輸送分類 (NMFC) コード](nmfc-codes.md)
- [船荷証券の作成](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

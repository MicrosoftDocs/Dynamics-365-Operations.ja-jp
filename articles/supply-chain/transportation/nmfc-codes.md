---
title: 国立モーター貨物の分類 (NMFC) コード
description: この記事では、Microsoft Dynamics 365 Supply Chain Management で国立モーター貨物の分類 (NMFC) コードの使用方法について説明します
author: Weijiesa
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c173057b8e1357790e780469c5806afb857be62a
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838338"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>国立モーター貨物の分類 (NMFC) コード

[!include [banner](../includes/banner.md)]

国立モーター貨物の分類 (NMFC) コードを使用すると、出荷可能な品目を分類できます。 NMFC コードは、商品をグループ化するために使用される指定です。 これにより、配送会社はトラックの適合性、積載の問題、問題の処理、および傷みやすさなどの考慮事項に基づいて品目を分類することで、出荷の商品を評価できます。 商品は、50 ～ 500 の範囲内の番号を使用して、18 貨物クラスのいずれかにグループ化されます。 商品がグループ化されるクラスは、密度、収納性、取り扱い、および責任の 4 つの輸送特性に対する評価に基づいています。 これらの特性の組み合わせで、商品の輸送性が確立されます。

NMFCコードは、トラックの負荷より小さい (LTL) すべての出荷品目に関連付けられます。 たとえば、ラップトップには 2.5 に分類される NMFC が割り当てられ、電気コードには 65 に分類される NMFC が割り当てられる場合があります。

この機能を使用すると、作業者が NMFC コードを使用して LTL 出荷品目を分類しやすくなります。 次にいくつか例を挙げます。

- 会社が船荷証券 (BOL) に貨物の説明を含めている場合、配送業者は貨物が何であるかをある程度知っています。 配送業者の多くは、出荷する貨物の種類に基づいてビジネス モデル全体を構築しているため、貨物の分類は重要です。
- この分類は特定の積荷の原価を決定するのに使用されるため、会社にとって不可欠な場合があります。
- 会社は、LTL 物流および輸送会社の収益性を特定できます。

この記事では、Microsoft Dynamics 365 Supply Chain Management での NMFC コードの使用方法について説明します。

## <a name="prerequisites"></a>必要条件

NMFC コードを作成する前に、そのコードにマップする必要があるすべての LTL 貨物クラスを設定する必要があります。 LTL 貨物クラスは品目のカテゴリを表しますが、NMFC コードは 18 の各貨物クラスの特定の商品に関連しています。 LTL クラスの使用方法の詳細については、[トラックの負荷より小さい (LTL) クラス](ltl-class.md)を参照してください。

## <a name="create-an-nmfc-code"></a>NMFC コードの作成

NMFC コードを作成するには、次の手順を実行します。

1. 次の手順のいずれかを実行します。

    - **倉庫管理 \> 設定 \> 在庫 \> NMFC コード** の順に移動します。
    - **輸送管理 \> 設定 \> 輸送標準 \> NMFC コード** の順に移動します。

1. **新規** を選択して、NMFC コードを作成します。 その後、次のフィールドを設定します:

    - **NMFC コード** – 商品タイプの NMFC コードを入力します。
    - **名前** – NMFC コードの名前を入力します。
    - **LTL クラス** – NMFC コードに関連付けられている LTL クラスを選択します。
    - **BOL 材料取り扱い単位** – 出荷の既定の処理タイプを定義します。

## <a name="example-set-up-nmfc-codes"></a>例: NMFC コードの設定

次の例は、異なる製品で使用できる 2 つの異なる NMFC コードの設定方法を示します。

1. **Warehouse management \> 設定 \> インベントリ \> NMFC コード** または **輸送管理 \> 設定 \> 輸送基準 \> NMFC コード** に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. 新しい明細行で、次の値を設定します。

    - **NMFC コード:** *92.5*
    - **名前:** *コンピューター*
    - **LTL クラス:** *92.5*
    - **BOL 材料取り扱い単位:** *単位*

1. アクション ウィンドウで、**保存** を選択します。
1. アクション ウィンドウで、**新規** を選択します。
1. 新しい明細行で、次の値を設定します。

    - **NMFC コード:** *125*
    - **名前:** *電話*
    - **LTL クラス:** *125*
    - **BOL 材料取り扱い単位:** *単位*

1. アクション ウィンドウで、**保存** を選択します。

## <a name="additional-resources"></a>追加リソース

- [トラックの負荷より小さい (LTL) クラス](ltl-class.md)
- [船荷証券の作成](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

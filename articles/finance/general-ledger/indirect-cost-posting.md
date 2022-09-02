---
title: 間接原価転記
description: この記事では、間接原価の転記、原価グループの作成、間接原価の原価シートへのノードの追加方法について説明します。
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, BOMCostGroup, ProjCategory, CostingVersion, CostSheetCalculationFactor
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 04af10760ec50d60cbbc31c233109dffb786933c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868434"
---
# <a name="indirect-cost-posting"></a>間接原価の転記

間接原価は、生産プロセスの単一の活動に直接関連付けされていない費用です。 たとえば、従業員の給与、会計部門の原価、家賃、光熱費、機械費などの間接費などの管理費があります。

## <a name="calculating-indirect-costs"></a>間接原価の計算をする

Microsoft Dynamics 365 Finance には、間接原価のレートを自動で計算する方法は存在されません。 間接原価の決定、間接原価コードの作成、原価シートの各間接原価のレートの管理を行う必要があります。

間接原価の計算に使用されるプロセスは、会社によって少し異なる場合があります。 ただし、一般に、このプロセスは次の基本的な手順で構成されます。

1. 生産で認識する間接原価の一覧を作成します。 このリストには、家賃、管理費、会計費用、法的手数料が含まれます。 生産ルートで認識される原材料費や人件費は含めるべきではありません。
2. すべての間接原価を合計します。 同様のタイプの間接原価をグループ化したり、別のタイプの間接原価を維持することができます。 総勘定元帳への転記に使用される主要勘定は、設定済の間接原価ごとに異なる場合があります。
3. 間接原価を係数と比較します。係数は吸収基準とも呼ばれます。 この係数は、何を選択してでも指定できます。 次にいくつかの一般的な例を挙げます。

    - 収益
    - 生産済の合計数量
    - 段取り時間
    - 実行時間

    間接原価の計算に使用する期間 (月、四半期、年など) を選択できます。 間接原価と係数の合計は、同じ時間で計算する必要があります。 以下の式は、関節原価残りの量の計算に使用します。

    *間接原価率* = *間接原価経費合計*&divide;*総係数*

4. 間接原価グループを作成します。
5. あなたの評価で原価シートを構成します。
6. 原価バージョンでの間接原価の原価を管理します。

> [!NOTE]
> **原価会計** モジュール を 使用すると、原価を累積し、生産、プロジェクト、総勘定元帳などのさまざまなソースから間接費を決定できます。 詳細については、[原価会計](/cost-accounting/cost-accounting-home-page.md) を参照してください。

> [!IMPORTANT]
> 各種の規制機関が、完成品の原価に間接費または間接費として含める原価のタイプに関するガイダンスを発行しています。 間接原価の構成を開始する前に、会計士や地域の規制に従って確認することをお勧めします。

## <a name="create-cost-groups-for-indirect-costs"></a>間接原価のグループを作成する

間接原価に使用するには、少なくとも 1 つの原価グループを作成する必要があります。 使用できる原価グループの数に制限はありません。 原価の計算方法と、さまざまなタイプの原価に対して異なるレートがあるかどうかを検討します。 たとえば、あなたの組織が食品を製造しているかどうかなどです。 原材料や完成品の中には、乾燥した商品で、倉庫管理に対する間接費が 1 つ含む場合があります。 その他の原材料や完成品は変更され、間接原価が高くなります。 この場合は、2 つの原価グループ **乾燥材料の間接費** と **冷蔵された材料の間接費** を作成します。

間接原価の原価グループを作成するには、次の手順に従います。

1. **生産管理 &gt; 設定 &gt; 工順 &gt; 原価グループ** の順に移動します。
2. **新規** を選択して、グループを作成します。
3. **原価 グループ** フィールドに、**MATOVH** のような原価 グループ固有の名前を入力します。
4. **名前** フィールドに、**材料の間接費** のような原価 グループの説明を入力します。
5. **原価 グループのタイプ** フィールドで、**間接** を選択します。
6. オプション : **動作** フィールド で、**固定費** または **変動費** を選択します。

## <a name="configure-the-costing-sheet-for-indirect-costs"></a>間接原価用の原価シートの構成

1 つ以上の原価グループを作成したら、間接原価を使用して原価シートを構成し、計算を定義できます。 この場合は、原価シートで間接原価をグループ化できます。 間接原価をグループ化する場合は、操作ヘッダーを原価シートに作成できます。 原価グループごとに 1 つ以上のノードを作成する必要があります。 間接原価の各原価グループに対して、1 つ以上の間接原価計算を追加できます。

### <a name="indirect-cost-node-types"></a>間接原価ノードの種類

このセクションでは、間接原価用のさまざまなタイプのノードについて説明します。

#### <a name="surcharge"></a>割増金

**割増金** は、最も一般的なタイプの間接原価の 1 つです。 製造オーダーの原価の吸収基準から原価の割合を計算します。 吸収の基準を定義するには、原価シートで材料または時間コンポーネントにリンクされる原価グループを選択します。

たとえば、3% の割増金を製造オーダーのすべての原材料の生産原価に追加できます。

#### <a name="rate"></a>率

**レート** タイプの間接原価は、製造オーダーに対する原価の吸収ベースから製造オーダーに固定金額の原価を追加するために使用されます。 このレートは、次の 3 つのサブタイプのいずれかを基に設定できます。

- **処理** - このレートは、ルートの実行時間に基づいて設定されます。
- **設定** - このレートは、ルートの設定時間に基づいて設定されます。
- **数量** - 生産される数量に基づいてレートが設定されます。

吸収の基準を定義するには、原価シートで材料または時間コンポーネントにリンクされる原価グループを選択します。

たとえば、原価シートの労務費グループのルートでの実行時間に基づいて、各製造オーダーに固定額 2.00 米ドル (USD) が追加されます。

#### <a name="output-unit-based"></a>生産単位基準

**出力単位ベース** のタイプの間接原価は、選択したサブタイプによって、原価シートの **レート** クイック タブで指定されている金額を乗算することで計算されます。 間接原価の乗数として完成品の数量、重量、または量を選択できます。

たとえば、生産される各数量の機械減価償却 1.50 米国ドルを計算する場合に、この数量を使用します。 別の例として、その量を使用して、2.00 米国ドルが選択したユニットで取るスペースの量に対する変更原価の計算を行います。

#### <a name="input-unit-based"></a>入力単位基準

**入力単位ベース** タイプの間接原価は、製造オーダーで消費される原材料の量に金額を乗算することで計算されます。 製造オーダーの入力の重量または量を使用して、合計を計算できます。 原価シートの **吸収基準** クイック タブで 1 つ以上の原価グループを選択することにより、計算を材料のサブセットに制限できます。

たとえば、製造オーダーに 1.00 米国ドルを追加するには、変更後の製品にリンクされている特定の原価グループに対して入力の量を使用します。

### <a name="create-a-total-node-for-indirect-costs-in-the-costing-sheet"></a>原価シートでの間接原価用の合計ノードを作成する

原価シートで間接原価の合計ノードを作成するには、次の手順に従います。

1. **原価管理 &gt; 間瀬s津原価会計ポリシー設定 &gt; 原価シート** に移動します。
2. ツリーで、製造された商品の原価を表すノードを選択します。
3. **新規** を選択して、ノードを作成します。
4. **ノード タイプを選択** フィールドで、**合計** を選択します。
5. **コード** フィールドに、ノードの固有 ID (**生産間接費など**) を入力します。
6. **ヘッダー** チェック ボックスを選択します。
7. **合計** チェック ボックスを選択します。
8.  **OK** を選択します。

### <a name="create-an-indirect-cost-group-node-in-the-costing-sheet"></a>原価シートで間接原価グループ ノードを作成する

原価シートで間接原価グループ ノードを作成するには、次の手順に従います。

1. **原価管理 &gt; 間瀬s津原価会計ポリシー設定 &gt; 原価シート** に移動します。
2. ツリーで、間接原価を作成するノードを選択します。 たとえば、**生産間接費** の合計ノードを選択します。
3. **新規** を選択して、ノードを作成します。
4. **ノード タイプの選択** フィールドで、**原価グループ** を選択します。
5. **コード** フィールドに、ノードの固有 ID (**TRANSP**) を入力します。
6. **説明** フィールドに、**輸送間接費** のような簡単な説明を入力します。
7.  **OK** を選択します。
8. **原価グループ** フィールド で、**OVH1: 輸送間接費** などの原価グループを選択します。

### <a name="create-a-surcharge-indirect-cost"></a>割増金の間接原価を作成する

原価シートで割増金の間接原価グループ ノードを作成するには、次の手順に従います。

1. **原価管理 &gt; 間瀬s津原価会計ポリシー設定 &gt; 原価シート** に移動します。
2. ツリーで、間接原価を作成する関節原価グループ ノードを選択します。 たとえば、**TRANSP - 輸送間接費** の合計ノードを選択します。
3. **新規** を選択して、ノードを作成します。
4. **ノード タイプを選択** フィールドで、**割増金** を選択します。
5. **コード** フィールドに、ノードの固有 ID (**輸送間接費など**) を入力します。
6.  **OK** を選択します。
7. **サブタイプ** フィールドで、**合計** を選択します。
8. **吸収ベース** クイック タブで、**新規** を選択して原価コードを新規作成します。
9. **コード** フィールド で、割増金の計算に使用する原価グループを選択します。
10. オプション : 計算に使用する追加の原価グループごとに手順 8 から 9 を繰り返します。
11. **割増金** クイック タブで、**新規** を選択してレートを作成します。
12. **バージョン** フィールドで、割増金を追加する原価バージョンを選択します。
13. オプション : **サイト** フィールドに、割増金を適用するサイトを入力します。
14. **パーセント** フィールドで、**吸収基準** クイック タブで定義された原価グループから製造オーダーに対して計算する割合を入力します。
15. **元帳転記** クイックタブで、**間接原価の見積** に対して使用する主要勘定、**消費された間接原価の見積原価、仕掛品**、**吸収された間接原価** および **消費された間接原価の原価、仕掛品** の各フィールドを選択します。
16. オプション : **財務分析コード** クイックタブで、トランザクションが総勘定元帳に転記される際に既定で入力する財務分析コードを指定します。

前の手順は、**割増金** タイプの間接原価を作成する方法を示しています。 同様の手順は、他のタイプの間接原価を作成するために使用されます。 次のセクションでは、各タイプの違いについて説明します。

#### <a name="rate"></a>率

- 手順 4 で、**割増金** の代わりに **レート** を選択します。
- 手順 7 で、**プロセス**、**設定**、または **合計** ではなく **数量** を選択します。
- 手順 11 で、**割増金** クイック タブの代わりに **レート** クイック タブを使用します。
- 手順 14 で、**パーセント** フィールドに割合ではなく、**金額** フィールドに金額を入力します。

#### <a name="output-unit-based"></a>生産単位基準

- 手順 4 で、**割増金** の代わりに **出力単位ベース** を選択します。
- 手順 7 で、**合計** ではなく、**数量**、**重量**、または **容量** を選択します。
- 手順 8 ～ 10 をスキップします。
- 手順 11 で、**割増金** クイック タブの代わりに **レート** クイック タブを使用します。

#### <a name="input-unit-based"></a>入力単位基準

- 手順 4 で、**割増金** の代わりに **入力単位ベース** を選択します。
- 手順 7 で、**合計** ではなく、**数量**、**重量** を選択します。
- 手順 11 で、**割増金** クイック タブの代わりに **レート** クイック タブを使用します。
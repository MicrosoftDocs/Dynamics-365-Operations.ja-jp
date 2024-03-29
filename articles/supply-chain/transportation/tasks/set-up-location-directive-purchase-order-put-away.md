---
title: 発注書のプット アウェイ場所のディレクティブを設定します
description: この記事では、簡単な場所ディレクティブの設定方法を説明します。
author: Weijiesa
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventFixedLocation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25484efd7be026bfc3a209fb52822b87d6b76cc2
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065497"
---
# <a name="set-up-a-location-directive-for-purchase-order-put-away"></a>発注書のプット アウェイ場所のディレクティブを設定します

[!include [banner](../../includes/banner.md)]

この記事では、簡単な場所ディレクティブの設定方法を説明します。 示されている例では、発注書に対して受領した品目を置く場所を決定するために使用される場所ディレクティブを作成します。 このタスク ガイドは、デモ データの会社 USMF で前述のデータを使用して実行できます。 事前条件: 廃棄コードを作成する必要があります。 この手順では、[ラベル書き換え] という廃棄コードを使用します。 自身のデータで場所ディレクティブを作成する場合は、倉庫と品目に対して倉庫管理プロセス (WMS) を設定する必要があります。 この手順は、倉庫マネージャーを対象としています。

1. ナビゲーション ウィンドウで、**モジュール > 倉庫管理 > 設定 > 場所のディレクティブ** の順に移動します。
2. **ワーク オーダー タイプ** フィールドで **発注書** を選択します。

## <a name="create-a-location-directive-header"></a>場所のディレクティブ ヘッダーの作成
1. **新規** を選択します。
2. **順序番号** フィールドに番号を入力します。 これは、選択した作業タイプのために場所のディレクティブを処理する順序です。 必要に応じて、その順序を変更できます。  
3. **名前** フィールドに値を入力します。 これは、このディレクティブの固有識別子です。  
4. **作業タイプ** フィールドで **プット** を選択します。 実効する作業のタイプを選択します。 ワーク オーダー タイプが発注書であるディレクティブでは、**プット** は唯一のサポートされている値です。  
5. **サイト** フィールドに値を入力します。
6. **倉庫** フィールドに値を入力します。 [ディレクティブ コード] を空白のままにします。  ディレクティブ コードを使用して、タイプが [プット] のワークオーダー明細行を特定のディレクティブにリンクします。 発注書の場合、作業テンプレートが決定される前に、タイプが [プット] のワーク オーダーの最終明細行の位置が解決されます。 そのため、作業テンプレートの最終明細行を特定のディレクティブに接続することはできません。   
7. **廃棄コード** フィールドに値を入力します。 廃棄コードは、場所のディレクティブの使用を制限します。そのため、場所のディレクティブ が使用されるのは、倉庫作業者がモバイル デバイスを使用して品目を登録する際にこの特定の値を入力する場合だけです。  
8. **保存** を選択します。

## <a name="edit-the-query-for-directive"></a>ディレクティブのクエリの編集
1. **クエリの編集** を選択します。 このディレクティブは、指定した廃棄コードにより、指定した倉庫に登録した品目に対しての使用を既に制限されています。 クエリを使用して他の制約を追加できます。  
2. **OK** を選択します。

## <a name="add-directive-lines"></a>ディレクティブ明細行の追加
1. **新規** を選択します。 これは、選択した作業タイプのために場所のディレクティブ明細行を処理する順序です。 必要に応じて、その順序を変更できます。  
2. **開始数量** フィールドに数値を入力します。 これはディレクティブの明細行が有効な最小数量です。  
3. **上限数量** フィールドに数値を入力します。
4. **単位** フィールドに値を入力します。 開始数量から上限数量までの単位が示されます。 フィールドを空白のままにすると、品目の在庫単位が使用されます。  
5. **数量の検索** フィールドで、オプションを選択します。
    - なし、またはライセンス プレート数量: 各ライセンス プレートに登録されている数量。  
    - 使用されている数量 : 登録されているすべての数量。  
    - 残余数量: 発注書明細行で指定された、まだ登録されていない数量。  
    - 予定数量: 発注書明細行で指定された、合計数量。  
6. **単位ごとに制限** チェック ボックスをオンまたはオフにします。 このオプションを選択し、**単位ごとに制限** ページで単位を指定する場合は、測定単位の品目のみが場所に配置できます。 たとえば、測定単位が PL (パレット) である場合、パレット内の品目のみが指定された場所に配置できます。  
7. **分割を許可** チェック ボックスをオンまたはオフにします。 これにより、ディレクティブは複数の場所に数量を分割することができます。  
8. **保存** を選択します。

## <a name="restrict-the-directive-line-to-a-specific-unit"></a>ディレクティブ明細行の特定の単位への制限
1. **単位ごとに制限** を選択します。 このボタンは、**単位ごとに制限** チェック ボックスをオンにしてから **保存** を押す場合にのみ使用できます。  
2. **単位** フィールドに値を入力します。
3. ページを閉じます。

## <a name="add-a-location-directive-action-line"></a>場所のディレクティブ アクション明細行の追加
1. **新規** を選択します。 これは、選択した作業タイプのために場所のディレクティブ アクション明細行を処理する順序です。 必要に応じて、その順序を変更できます。  
2. **名前** フィールドに値を入力します。 これは、このディレクティブ アクションの固有識別子です。  
3. **固定の場所の使用** フィールドで、オプションを選択します。
    - 固定場所および固定されていない場所 : クエリで指定された範囲内のすべての固定されていない場所は、製品の自身の固定場所と同様に有効です。  
    - 製品の固定の場所のみ: 製品の固定の場所は有効であり、すべての製品バリアントの固定の場所のセットは同じです。  
    - 製品バリアントの固定の場所のみ: 各製品バリアントに指定されている固定の場所だけが有効です。  
4. **戦略** フィールドで、オプションを選択します。 発注書のワーク オーダー タイプは、以下の戦略をサポートします。 
    - なし : 品目は見つかった最初の場所に配置されます。  
    - 連結: 品目は同様の品目が既に利用可能な場所に配置されています。  
    - 作業がない空の場所 : 品目は見つかった最初の空の場所に配置されています。 現物在庫がなく、入荷作業が予定されていない場合、その場所は空であると見なされます。  
5. **保存** を選択します。

## <a name="edit-the-query-for-directive-action-line"></a>ディレクティブ アクション明細行のクエリの編集
1. **クエリの編集** を選択します。
2. **追加** を選択します。
3. **フィールド** のフィールドに、`location profile ID` と入力します。 この例では、場所プロファイル ID を使用して可能な場所を制限します。  
4. **基準** フィールドに値を入力します。
5. **OK** を選択します。 倉庫のすべての可能なシナリオが対象となるまで、ディレクティブ明細行とディレクティブ アクションの追加を続行できます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
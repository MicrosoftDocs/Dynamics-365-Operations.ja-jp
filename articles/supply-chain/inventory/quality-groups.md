---
title: 品目品質グループ
description: この記事では、品目品質グループの使用および作成して、製品を論理的にグループ化し、品質指示の自動生成用に品質関連に割り当てる方法について説明します。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestQualityGroup, InventTestItemQualityGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf1ce49fa58fd1a8a5aa07636e0b2bd7e2fc10e4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875368"
---
# <a name="item-quality-groups"></a>品目品質グループ

[!include [banner](../includes/banner.md)]

品質グループとは、複数の品目に共通するテスト要件です。 この記事では、品目品質グループの使用および作成して、製品を論理的にグループ化し、品質指示の自動生成用に品質関連に割り当てる方法について説明します。

品質グループに割り当てられる品目、または品目に割り当てられる品質グループを、設定、編集、および表示するには、**在庫管理 \> 設定 \> 品質グループ** の順に移動します。 **テスト グループ** ページのテスト要件を定義した後、品質指示を自動生成するルールを定義できます。 プロセスを簡略化するため、個別の品目のルールは定義しません。 代わりに、**品質関連** ページの品質グループのルールを定義できます。

## <a name="example-of-an-item-quality-group"></a>品目品質グループの例

ある製造会社で、受入検査に同じテスト要件があるさまざまな原材料を購入しています。 そのため、その会社では品質グループを定義し、そのグループに原材料と関連付けた品目番号を割り当てます。 後で、同じテスト要件がある新しいタイプの原材料を購入します。 新しい材料の新しいテスト要件を設定せずに、既存の品質グループに新しい材料の品目番号を追加します。

また、同じ会社では同じ製造テスト要件の品目を製造し、同じ要件で出荷前テストを実行して品目を出荷しています。 したがって、この会社はさらに 2 つの品質グループを定義し、各グループに関連品目番号を割り当てます。

## <a name="create-a-quality-group"></a>品質グループの作成

品質グループを作成するには、次の手順に従います。

1. **在庫管理 \> 設定 \> 品質管理 \> 品質グループ** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **品質グループ** – 品質グループの固有の ID または名前を入力します。
    - **説明** – 品質グループの詳細説明を入力します。

1. ページを閉じます。

## <a name="manually-add-items-to-a-quality-group"></a>品目を品質グループに手動で追加する

品目を品質グループに手動で追加するには、次の手順に従います。

1. **在庫管理 \> 設定 \> 品質管理 \> 品質グループ** の順に移動します。
1. 品目を追加する品質グループを選択します。
1. アクション ペインで、**品目** を選択します。
1. アクション ウィンドウの、**品質グループの品目** ページで、**新規** を選択してグリッドに行を追加します。 次に、新しい行に対して、**品目番号** フィールドを追加する品目番号に設定します。
1. 追加する新しい品目ごとに前の手順を繰り返します。
1. ページを閉じます。

## <a name="add-multiple-items-to-a-quality-group"></a>複数品目を品質グループに追加する

複数品目を品質グループに追加するには、次の手順に従います。

1. **在庫管理 \> 設定 \> 品質管理 \> 品質グループ** の順に移動します。
1. 品目を追加する品質グループを作成および選択します。
1. アクション ペインで、**品目の追加** を選択します。
1. **照会** ダイアログ ボックスで、追加する品目のフィルター条件を入力します。 たとえば、特定の品目グループのすべての品目をフィルター処理する場合があります。
1. **OK** を選択します。
1. **品目の追加** ダイアログ ボックスで、クエリに一致するすべての品目がグリッドに表示されます。 結果を確認します。

    変更が必要な場合は、**選択** をオンにして **照会** ダイアログ ボックスに戻り、クエリを調整します。

1. 追加するすべての品目が結果に含まれる場合は、**OK** を選択します。
1. ページを閉じます。

## <a name="manually-associate-an-item-with-a-quality-group"></a>品目を品質グループに手動で関連付ける

品目を品質グループに手動で関連付けるには、次の手順に従います。

1. **在庫管理 \> 設定 \> 品質管理 \> 品目品質グループ** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **品目番号** – 追加する品目番号を選択します。
    - **品質グループ** – 品目に割り当てる品質グループを選択します。

1. 追加する必要がある品目と品質グループの組み合わせごとに、前の手順を繰り返します。
1. ページを閉じます。

## <a name="manually-add-a-quality-group-from-the-released-products-page"></a>リリース済製品ページからの品質グループを手動で追加する

**リリース済製品** ページからの品質グループを手動で追加するには、次の手順に従います。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 品質グループを割り当てる製品を選択します。
1. アクション ウィンドウの、**在庫の管理** タブの、**品質** グループで、**品目品質グループ** を選択します。
1. アクション ウィンドウの、**品質グループの品目** ページで、**新規** を選択してグリッドに行を追加します。 次に、新しい行に対して、**品質グループ** フィールドを製品に割り当てる品質グループに設定します。
1. 製品に割り当てる追加の品質グループごとに前の手順を繰り返します。
1. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理テスト機器](quality-test-instruments.md)
- [品質管理テスト](quality-tests.md)
- [品質管理テスト グループ](quality-test-groups.md)
- [品質管理テスト変数](quality-test-variables.md)
- [品質関連](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

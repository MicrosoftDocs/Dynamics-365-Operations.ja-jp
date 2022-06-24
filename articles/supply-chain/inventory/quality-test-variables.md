---
title: 品質管理テスト変数
description: この記事では、Microsoft Dynamics 365 Supply Chain Management の定性試験に使用できるテスト変数を作成する方法について説明します。
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10fe206b76f2e50e09cb6aaa6055614c2fe9425d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857637"
---
# <a name="quality-management-test-variables"></a>品質管理テスト変数

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics 365 Supply Chain Management の定性試験に使用できるテスト変数を作成する方法について説明します。

**テスト** ページで定義されているすべての定性試験について、テスト変数とその可能な結果 (結果) を定義する必要があります。 (定性試験の場合、**テスト** ページの **タイプ** フィールドは、*オプション* に設定されます。)

**テスト変数** ページを使用して、定性試験に関連付けられているテスト変数の可能な結果を設定、編集、および表示します。 それぞれの結果について、*合格* または *不合格* のいずれかの結果ステータスを割り当て、その結果がテスト結果として選択された場合にテストが合格か不合格かを示します。 **テスト グループ** ページを使用して、テスト変数と既定の結果を個々の定性試験に割り当てます。

すべてのテスト変数について、少なくとも 2 つの結果を定義することをお勧めします。1 つは結果ステータスが *合格* で、もう 1 つは結果ステータスが *不合格* です。 定義できる変数または結果の合計数に制限はありません。 また、複数のテストで同じテスト変数を使用して結果を記録できます。

## <a name="examples-of-test-variables"></a>テスト変数の例

### <a name="example-1"></a>例 1

製造会社で、製造材料に対する 2 つのテストを実行しています。 1 つのテストでは、pH レベルが色のストリップに関連付けられています。 許容できる pH レベルは明るい色で、許容できない pH レベルは暗い色です。 別のテストでは、複数の目視検査が実行され、品質作業員はその判断を使用して、品目が目視検査に合格か不合格かを決定します。

### <a name="example-2"></a>例 2

クッキーを製造しているある製造会社では、完成した製品の検査テストを採用しています。 この検査テストには、複数の変数があります。 1 つの変数は味で、そのために考えられる結果は、良および不良です。 2 つ目の変数は色で、そのために考えられる結果は、濃すぎる、薄すぎる、および適正です。

## <a name="create-a-test-variable"></a>テスト変数の作成

次の手順に従って、テスト変数を作成します。

1. **在庫管理 \> 設定 \> 品質管理 \> テスト変数** の順に移動します。
1. アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。 続いて、新しい行に次のフィールドを設定します:

    - **変数** – 変数の固有の ID または名前を入力します。
    - **説明** – 変数の詳細説明を入力します。

1. 新しい行がまだ選択されている間に、アクション ウィンドウで **結果** を選択します。
1. アクション ウィンドウの **テスト変数の結果** ページで、**新規** を選択して、グリッドに行を追加します。 続いて、新しい行に次のフィールドを設定します:

    - **結果** – 結果の固有の ID または名前を入力します。
    - **説明** – 結果の詳細説明を入力します。
    - **結果ステータス** – *合格* または *不合格* のいずれかを選択して、結果がテスト結果として選択された場合に、テストが合格か不合格かを示します。

1. 追加の結果ごとに前の手順を繰り返します。 少なくとも 1 つの結果の結果ステータスが *合格* であり、少なくとも 1 つの結果の結果ステータスが *不合格* であることを確認してください。
1. ページを閉じます。

## <a name="additional-resources"></a>追加リソース

- [品質管理テスト機器](quality-test-instruments.md)
- [品質管理テスト](quality-tests.md)
- [品質管理テスト グループ](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

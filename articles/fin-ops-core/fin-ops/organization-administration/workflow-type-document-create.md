---
title: ワークフロー ドキュメント クラスの作成
description: この記事では、ワークフロー ドキュメント クラスを作成する方法について説明します。
author: RobinARH
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 202694
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: fa773fc3e97a6c875e1a324a663583d60670e208
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894217"
---
# <a name="create-a-workflow-document-class"></a>ワークフロー ドキュメント クラスの作成

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

クエリでテーブルフィールドを定義して、ワークフロー条件を作成します。 一般的なシナリオでは、計算済フィールドはワークフローの動作を決定するために使用されます。 たとえば、テーブル内のすべてのレコードの動的な販売合計をワークフロー条件として使用し、ステップを使用するかどうかを決定できます。 ただし、クエリの制限としては、クエリ自体に計算済フィールドを定義できないことが挙げられます。 このクエリ制限を克服するには、ワークフロー ドキュメント クラスを使用する必要があります。 この記事では、ワークフロー ドキュメント クラスを作成する方法について説明します。

作成するワークフロー ドキュメント クラスは、アプリケーション エクスプローラーのクエリとパラメータ メソッドという 2 つの方法で、条件のテーブル フィールドを定義します。 クエリの名前を返すには、 [WorkflowDocument クラス](/previous-versions/dynamics/ax-2012/application-classes/gg798542(v=ax.60)) の **getQueryName** メソッドをオーバーライドする必要があります。 必要に応じて、クラスの特定の署名を持つパラメータ メソッドを追加して、計算済フィールドを追加することができます。 ワークフロー条件の詳細については、 [ワークフロー プロパティのコンフィギュレーション](configure-workflow-properties.md) と [ワークフローでの条件付き意思決定のコンフィギュレーション](configure-conditional-decision-workflow.md) を参照してください。

次の手順では、計算済フィールドのパラメータ メソッドを含むワークフロー ドキュメント クラスを作成する方法について説明します。 開始する前に、アクセスするデータを指定するクエリを作成する必要があります。 ワークフロー クエリの詳細については、 [ワークフロー タイプのクエリの作成](workflow-type-query.md) を参照してください。

> [!NOTE]
> **ワークフロー** ウィザードを使用してワークフロー タイプを作成した場合は、ウィザードはワークフロー ドキュメント クラスを既に作成しています。

## <a name="create-a-workflow-document-class"></a>ワークフロー ドキュメント クラスの作成

1. 新しいクエリを作成するには、次のいずれかのステップを実行します

    + アプリケーション エクスプローラーで、 **クラス** ノードを展開します。 **クラス** ノードを右クリックし、 **新しいクラス** を選択します。 クラス グループは、 **クラス** ノードの下に表示されます。 新しいクラスを右クリックし、 **名前変更** を選択して、ワークフロー ドキュメント クラスの名前を入力します。
    + **プロジェクト** メニューの **新しい項目の追加** を選択します。 **新しい項目の追加** ダイアログ ボックスで、 **クラス** を選択します。 クラス名を入力し、 **作成** を選択します。

2. 新しいクラスを展開し、 **classDeclaration** を選択し、クラス宣言を右クリックして、次に **編集** を選択します。
3. クラス宣言に次のコードを入力します。

    ```X++
    class <MyWorkflowDocumentClassName> extends WorkflowDocument
    {
    }
    ```

4. **エディター** ウィンドウを閉じ、 **はい** を選択して変更を保存します。
5. 新しいクラスを右クリックし、 **オーバーライド メソッド** をポイントして、次に **getQueryName** を選択します。 **GetQueryName** という名前のメソッド ノードがワークフロー ドキュメント クラス ノードの下に表示され、 **エディター** ウィンドウが表示されます。

    > [!NOTE]
    > オーバーライドする方法として **getQueryName** を選択してください。 [WorkflowDocument.getQuery メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg798533(v=ax.60)) は、 [WorkflowDocument.getQueryName メソッド](/previous-versions/dynamics/ax-2012/application-classes/gg798541(v=ax.60)) によって返される文字列に基づいて、実際のクエリを取得するために内部的にのみ使用されます。

6. **エディター** ウィンドウで、次のコードをクエリ メソッドに入力します。

    ```X++
    QueryName getQueryName()
    {
        return querystr(<MyWorkflowDocumentQueryName>);
    }
    ```

ワークフロー ドキュメント クラスを作成した後、それをワークフロー タイプにバインドできます。 詳細については、 [ワークフロー ドキュメント クラスとワークフロー タイプの関連付け](workflow-type-associate-document.md) を参照してください。

ワークフロー ドキュメント クラスに計算済フィールドを追加できるのは、次の条件を満たしている場合だけです。

- **parm \<name\>** という名前にする必要があります。
- **CompanyId**、 **TableId**、および **RecId** の各パラメータを定義する必要があります。
- 条件または通知メッセージを定義するフィールドの一覧に含まれる拡張データ型 (EDT) を返す必要があります。 EDTのラベルは、値を一意に識別する必要があります。

## <a name="add-a-calculated-field-to-the-workflow-document-class"></a>ワークフロー ドキュメント クラスへの計算済フィールドの追加

1. 計算済フィールドを追加するワークフロー ドキュメント クラスで、クラスを右クリックして、 **新しいメソッド** を選択します。 **クラス** ノードの下に新しいメソッド ノードが表示されます。
2. 新しいメソッド ノードを右クリックし、 **編集** を選択します。
3. 次の例に示す形式でコードを入力します。 この例では、計算済フィールドを追加して仕訳帳の貸方金額の合計を決定する方法を示します。

    ```X++
    public TotalJournalCreditAmount parmTotalJournalCreditAmount(CompanyId _companyId, TableId _tableId, RecId _recId)
    {
        // The calculateAmounts method contains business and validation logic
        this.calculateAmounts(_companyId, _tableId, _recId);
        return totalJournalCreditAmount;
    }
    ```

## <a name="see-also"></a>参照

[ワークフロー ドキュメント クラスとワークフロー タイプの関連付け](workflow-type-associate-document.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
---
title: テーブル マッピングと列マッピングのカスタマイズ
description: この記事では、テーブル マッピングと列マッピングをカスタマイズする方法について説明します。
author: nhelgren
ms.date: 03/20/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: nhelgren
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3617ec760e2238fddd6a24a85f32b70b93a8c7e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884775"
---
# <a name="customize-table-and-column-mappings"></a>テーブル マッピングと列マッピングのカスタマイズ

[!include [banner](../../includes/banner.md)]



標準のテーブル マップには、2 つのアプリ間のデータ フローを可能にする事前定義されたテーブル マッピングおよび列マッピングがあります。 このように、それらは "青写真" として機能します。 ただし、ビジネスごとに異なるため、既定のテーブル マップでは不十分な場合があります。 したがって、二重書き込みはテーブル マップおよび列マッピングを変更する方法を提供することにより、カスタマイズを完全にサポートします。

## <a name="customize-column-mappings-add-transforms-and-enable-filtering"></a>列マッピングのカスタマイズ、変換の追加、およびフィルタ処理の有効化

1. 財務と運用アプリの **二重書き込み** ページの **テーブル マッピング** タブで、カスタマイズするテーブル マップを選択します。

    > [!NOTE]
    > テーブル マッピングを変更する前に、停止する (実行しない) 必要があります。 そうしないと、変更は保存されません。

2. **テーブル マッピング** タブで、財務と運用アプリまたは Dataverse から新しい列またはカスタム列を選択して、フィールドをカスタマイズできます。

    ![列のカスタマイズ。](media/customize-a-field.png)

3. 同期の方向 (単一方向または双方向) をカスタマイズし、マップの種類を選択して変換を追加できます。

    ![同期の方向のカスタマイズと変換の追加。](media/customize-sync-direction.png)

    次の表で、使用可能な同期の方向について説明します。

    | 記号 | 説明 |
    |---|---|
    | ![等号。](media/equal-symbol.png) | 双方向の列の割り当て |
    | ![大なり/小なり記号。](media/greater-less-symbol.png) | 変換を使用する双方向の列の割り当て |
    | ![大なり記号。](media/greater-than-symbol.png) | 単一方向の列の割り当て (左から右) |
    | ![小なり記号。](media/less-than-symbol.png) | 単一方向の列の割り当て (右から左) |
    | ![右矢印。](media/right-arrow-symbol.png) | 変換を使用する単一方向の列の割り当て (左から右) |
    | ![左矢印キー。](media/left-arrow-symbol.png) | 変換を使用する単一方向の列の割り当て (右から左) |

    次の表で、使用可能な変換のタイプについて説明します。

    | 変換のタイプ | 説明 |
    |---|---|
    | 既定 | 既定値は、ソース列値が使用できない場合に、出力先の列に適用される値です。 対応するソース列がない場合に、出力先テーブルで必要な列には既定値を使用します。 |
    | 値のマップ | 値マップでは、あるテーブルに存在する値を他のテーブルの値にマップする方法を定義します。 |

4. 新しい列を追加するには、**マッピングの追加** を選択し、リストの既存の列またはカスタム列を選択します。

    次の図は、新しい **生年月日** の列を追加する例を示しています。

    ![新しい生年月日の列を追加します。](media/add-new-field.png)

5. 列マッピングのカスタマイズが完了したら **保存** を選択します。 次に、プロンプトに従って、パブリッシャーとバージョン番号を指定します。

    ![パブリッシャーとバージョン番号の指定。](media/choose-publisher-version.png)

### <a name="filter-your-data"></a>データのフィルタ処理

二重書き込みでは、Dataverse の [データ プロトコル (OData) を開く] フィルター式を使用してデータをフィルターできます。 財務と運用アプリの場合、フィルター処理は、クエリ範囲で使用される範囲式に似ています。

1. テーブル マッピング ページで、フィルター ボタン (じょうごのアイコン) を選択します。

    ![フィルター ボタン。](media/select-filter-icon.png)

2. **クエリの編集** ダイアログボックスで、フィルターを指定します。 この例では、指定されたフィルターは、アカウント タイプが **3** であるアカウントのみを返します。

    ![フィルターの指定。](media/specify-filters.png)

    次の表に、フィルター式の例を示します。

    | フィルター | Dataverse | 財務と運用アプリ |
    |---|---|---|
    |文字列フィールド (次を含む)| startswith(name, 'A')|(name like "A*")|
    |文字列フィールド (次を含まない)|not contains(name, 'A')|(!(name like "*A*"))|
    |列挙型フィールド| AccountType == '3'| (AccountType == AccountType::Customer)|
    |日付|TransactionDate le '2021-06-23'|(TransactionDate <= 23\06\2021)|
    |複数の条件の組み合わせ| numberofemployees gt 1000 and<br>numberofemployees le 2000 | ((numberofemployees > 1000) &&<br>(numberofemployees <= 2000)) |

    クエリ範囲で式を使用する方法の例については、[クエリ範囲での式の使用](/dynamicsax-2012/developer/using-expressions-in-query-ranges) を参照してください。

    現時点では、二重書き込みソース フィルターでのネストされたルックアップはサポートされていません。 テーブル列に対して直接、標準のフィルタ演算子のみがサポートされています。 例については、[標準フィルタ演算子](/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators) を参照してください。

## <a name="add-new-table-maps"></a>新しいテーブル マップの追加

Microsoft は引き続き新しいテーブルを追加していますが、標準またはカスタムのテーブル マップを追加することもできます。

次の例は、**アドレス帳** という名前の新しいテーブル マップを追加する方法を示しています。

1. 財務と運用アプリの **二重書き込み** ページで、**テーブル マップの追加** を選択します。

    ![新しいテーブル マップを追加します。](media/add-new-entity-map.png)

    > [!NOTE]
    > これらの変更済みテーブル マップを使用する[新しいソリューションを作成する](app-lifecycle-management.md#create-new-solution) 場合は、同じパブリッシャーを指定する必要があります。

2. 変更および追加したテーブル マップを確認します。 それらを有効にしてテストし、期待どおりに機能することを確認してください。

    ![テーブル マップを確認します。](media/confirm-entity-maps.png)

## <a name="next-steps"></a>次のステップ

[エラー管理と警告通知](errors-and-alerts.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

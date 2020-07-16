---
title: エンティティとフィールドのマッピングのカスタマイズ
description: このトピックでは、エンティティとフィールド マッピングをカスタマイズする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5df54a2c40646c32b0261328fd83145bac8d731e
ms.sourcegitcommit: eda612d7dc6fc5be2d5d2f27a7472c8d59e42d76
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500003"
---
# <a name="customize-entity-and-field-mappings"></a>エンティティとフィールドのマッピングのカスタマイズ

[!include [banner](../../includes/banner.md)]



すぐに使えるエンティティ マップには、2 つのアプリ間のデータ フローを可能にする事前定義されたエンティティおよびフィールド マッピングがあります。 このように、それらは "青写真" として機能します。 ただし、ビジネスごとに異なるため、既定のエンティティ マップでは不十分な場合があります。 したがって、二重書き込みは、エンティティ マップおよびフィールド マッピングを変更する方法を提供することにより、カスタマイズを完全にサポートします。

## <a name="customize-field-mappings-add-transforms-and-enable-filtering"></a>フィールド マッピングのカスタマイズ、変換の追加、およびフィルタ処理の有効化

1. Finance and Operations アプリの **二重書き込み** ページの **エンティティ マッピング** タブで、カスタマイズするエンティティ マップを選択します。

    > [!NOTE]
    > エンティティ マッピングを変更する前に、停止する (実行しない) 必要があります。 そうしないと、変更は保存されません。

2. **エンティティ マッピング** タブで、Finance and Operations アプリまたは Common Data Service から新しいフィールドまたはカスタム フィールドを選択して、フィールドをカスタマイズできます。

    ![フィールドのカスタマイズ](media/customize-a-field.png)

3. 同期の方向 (単一方向または双方向) をカスタマイズし、マップの種類を選択して変換を追加できます。

    ![同期の方向のカスタマイズと変換の追加](media/customize-sync-direction.png)

    次の表で、使用可能な同期の方向について説明します。

    | 記号 | 説明 |
    |---|---|
    | ![等号](media/equal-symbol.png) | 双方向のフィールド割り当て |
    | ![大なり/小なり記号](media/greater-less-symbol.png) | 変換を使用する双方向フィールド割り当て |
    | ![大なり記号](media/greater-than-symbol.png) | 単一方向フィールド割り当て (左から右) |
    | ![小なり記号](media/less-than-symbol.png) | 単一方向フィールド割り当て (右から左) |
    | ![右矢印キー](media/right-arrow-symbol.png) | 変換を使用する単一方向フィールド割り当て (左から右) |
    | ![左矢印キー](media/left-arrow-symbol.png) | 変換を使用する単一方向フィールド割り当て (右から左) |

    次の表で、使用可能な変換のタイプについて説明します。

    | 変換のタイプ | 説明 |
    |---|---|
    | 既定 | 既定値は、ソース フィールド値が使用できない場合に、宛先フィールドに適用される値です。 対応するソース フィールドがない場合に、宛先エンティティで必要なフィールドには既定値を使用します。 |
    | 値のマップ | 値マップでは、あるエンティティに存在する値を他のエンティティの値にマップする方法を定義します。 |

4. 新しいフィールドを追加するには、**マッピングの追加** を選択し、リストの既存のフィールドまたはカスタム フィールドを選択します。

    次の図は、新しい **生年月日** フィールドを追加する例を示しています。

    ![新しい生年月日フィールドの追加](media/add-new-field.png)

5. フィールド マッピングのカスタマイズが完了したら **保存** を選択します。 次に、プロンプトに従って、パブリッシャーとバージョン番号を指定します。

    ![パブリッシャーとバージョン番号の指定](media/choose-publisher-version.png)

### <a name="filter-your-data"></a>データのフィルタ処理

二重書き込みでは、Common Data Service の [データ プロトコル (OData) を開く] フィルター式を使用してデータをフィルターできます。 Finance and Operations アプリの場合、フィルター処理は、クエリ範囲で使用される範囲式に似ています。

1. [エンティティ マッピング] ページで、フィルター ボタン (じょうごのアイコン) を選択します。

    ![フィルター ボタン](media/select-filter-icon.png)

2. **クエリの編集** ダイアログボックスで、フィルターを指定します。 この例では、指定されたフィルターは、アカウント タイプが **3** であるアカウントのみを返します。

    ![フィルターの指定](media/specify-filters.png)

    次の表に、フィルター式の例を示します。

    | Common Data Service | Finance and Operations アプリ |
    |---|---|
    | Accounttype eq '3' | (accounttype == '3') |
    | numberofemployees gt 1000 and<br>numberofemployees le 2000 | ((numberofemployees > 1000) &&<br>(numberofemployees <= 2000)) |

    クエリ範囲で式を使用する方法の例については、[クエリ範囲での式の使用](https://docs.microsoft.com/dynamicsax-2012/developer/using-expressions-in-query-ranges) を参照してください。
    
    現時点では、二重書き込みソース フィルターでのネストされたルックアップはサポートされていません。 エンティティのフィールドに対して直接、標準のフィルタ演算子のみがサポートされています。 例については、[標準フィルタ演算子](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/query-data-web-api#standard-filter-operators) を参照してください。
    
## <a name="add-new-entity-maps"></a>新しいエンティティ マップの追加

Microsoft は引き続き新しいエンティティを追加していますが、標準またはカスタムのエンティティ マップを追加することもできます。

次の例は、**アドレス帳** という名前の新しいエンティティ マップを追加する方法を示しています。

1. Finance and Operations アプリの **二重書き込み** ページで、**エンティティ マップの追加** を選択します。

    ![新しいエンティティ マップの追加](media/add-new-entity-map.png)

    > [!NOTE]
    > これらの変更済みエンティティ マップを使用する [新しいソリューションを作成する](app-lifecycle-management.md#create-a-new-dual-write-solution-and-add-your-components-customized-entity-maps) 場合は、同じパブリッシャーを指定する必要があります。

2. 変更および追加したエンティティ マップを確認します。 それらを有効にしてテストし、期待どおりに機能することを確認してください。

    ![エンティティ マップの確認](media/confirm-entity-maps.png)

## <a name="next-steps"></a>次のステップ

[エラー管理と警告通知](errors-and-alerts.md)

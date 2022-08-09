---
title: 個人検索レポートを拡張
description: この記事では、財務と運用の個人検索レポートを拡張するためのプロセスを説明します。
author: rschloma
ms.date: 01/24/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: tfehr
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcc0c985371796d18b2dc2e3e0a6ada5af2853be
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066475"
---
# <a name="extend-the-person-search-report"></a>個人検索レポートを拡張

[!include [banner](../includes/banner.md)]

財務と運用アプリの個人検索レポートは、1 人のエンティティのコレクションを管理するように設計されたインテリジェント検索プロセッサによってサポートされています。 個人検索レポートは、財務と運用のデータを検索し、生成される識別子のセットを作成します。 それぞれの結果は、検索カテゴリ (たとえば、顧客) および関連するテーブルの結果レコードを参照します。 個人検索レポートの使用の詳細については、[個人検索レポート](gdpr-person-search-report.md) の記事を参照してください。

> [!NOTE]
> 個人検索では、Dynamics 365 Finance、Supply Chain Management、コマース、および人事管理に対して使用できます。 Microsoft Dynamics AX 2012 では今のところ担当者検索レポートは使用できません。

## <a name="add-another-entity-to-the-default-template"></a>既定のテンプレートへの別のエンティティの追加

任意のエンティティを既定の個人検索レポート テンプレートに追加することができます。 **データ管理** ワークスペースを開いて、**テンプレート** を選択します。 テンプレートにエンティティを追加します。 追加するエンティティには、個人検索レポートをフィルター処理するために使用されるフィールドの少なくとも 1 つが含まれている必要があります。 

## <a name="create-a-new-search-category"></a>新しい検索カテゴリを作成する

1. **PersonSearchResultCategory** 列挙型を使用して、作業者と申請者のような異なるカテゴリの結果を区別します。
2. 新しい結果タイプを作成するには、必要に応じて **PersonSearchResultCategory** 列挙型を拡張します。

## <a name="create-search-processing-for-the-new-search-category"></a>新しい検索カテゴリの検索処理を作成する

この例では、新しいプロセッサ クラスを作成します。

1. 新しい検索区分で **PersonSearchModule** 列挙型を拡張します。
2. **PersonSearchProcessor** クラスを拡張し、新しい個人検索モジュール領域をパラメータとして **PersonSearchProcessorFactoryAttribute** 属性を含むクラスを作成します。 
3. **PersonSearchProcessor** 拡張クラスで、目的の検索ロジックで **doSearch** メソッドをオーバーライドします。 次の例のように、新しいテーブル関係を作成するために **PersonSearchResult** テーブルを拡張します。

    ```xpp
    PersonSearchResultCategory::Customer needs a relation:PersonSearchResult.ResultRecId = CustTable.RecId,PersonSearchResult.ResultTableId = CustTable.TableId
    ```

## <a name="integrate-with-the-global-address-book-optional"></a>グローバル アドレス帳と統合 (オプション)

グローバル アドレス帳と統合する場合は、検出されたパーティー番号を **PersonSearchPartyNumberTmp** テーブルに挿入します。 **PersonSearchProcessor** の **findPartyLink** メソッドは、当事者番号を、ユーザー、顧客、仕入先などの他の検索コンポーネントにリンクします。

このメソッドにはデリゲート **onFindPartyLink** があり、当事者番号に基づいて検索する追加のコンポーネントを指定できます。

**PersonSearchCriteria** テーブルでは、エンド ユーザーが、システムで個人データの検索に使用するパラメーターを指定できます。

## <a name="create-new-search-criteria"></a>新しい検索基準を作成する

新しい検索条件を必要である場合は、これらの手順に従います。

1. **PersonSearchCriteriaName**、**PersonSearchCriteriaAddress**、および **PersonSearchCriteriaKnownId** を拡張または独自のテーブルを作成します。
2. 新しいデータ フィールドを表示するには、**PersonSearchDialog** フォームを拡張します。
3. 検索処理中に新しい条件を使用します。

**PersonSearch** フォームには、担当者の検索によって検出された結果のセットが表示されます。

## <a name="show-the-new-search-category-in-the-personsearch-form"></a>PersonSearch 形式で新しい検索カテゴリを表示

1. **PersonSearchResult** テーブルの新しいビューを作成します。 このビューは結果を新しい **PersonSearchResultCategory** に限定する必要があります。
2. ビューを結果レコードに結合させ、必要なフィールドのビューを作成します (たとえば、**PersonSearchResultCustomerView**)。
3. 新しいリレーションシップを新しいビューに作成するには、**PersonSearchResult** テーブルを拡張します。 このリレーションシップは、人物の検索 ID に結合する必要があります。
4. **PersonSearch** フォームを拡張します。

    1. データ ソースとして新しいビューを追加します。
    2. 結果のグリッドと **含む/除外** ボタンを使用して結果に新しいタブを追加します。
    3. **含む/除外** ボタンのイベント ハンドラーを作成して **PersonSearchResult** レコードを更新します。

        **PersonSearchEventHandler::updateMarkedOnButtonClicked()** メソッドが利便性のために用意されています。

> [!NOTE]
> 結果キャプションのレコード数を確認するには、**OnQueryExecuted** ビューのデータ ソース イベントでイベント ハンドラーを作成します。 次に、**PersonSearch** フォームで **setResultCountOnGridCaption()** メソッドを呼び出して、カウントを更新します。

各 **PersonSearchEntityFilterRelation** レコードは、フィルターを適用する場合、条件、フィルター テーブルおよび適用するフィールドを指定します。

フィルター関係のセットは、パッケージの構築時にテンプレート メタデータと比較されます。

フィルターを作成するためには、**PersonSearchResult** レコードと一致するフィルター カテゴリが存在する必要があります。 見つかったら、**PersonSearchResult** は、フィルター値が置かれているテーブル フィールドを参照します。

## <a name="create-new-filters"></a>新しいフィルタを作成する

1. **PersonSearchEntityFilterRelation** テーブルを拡張するには、Chain of Command (COC) を使用します。
2. 新しいフィルターのタイプとソースを決定する:

    1. フィルターが拡張データ型 (EDT) または列挙の場合は、**MetadataTypeId** をデータ型の ID に設定します。
    2. フィルターがソース テーブルのフィールドである場合は、ソース テーブルとソース フィールド ID を指定します。
    3. フィルターがエンティティ フィールドである場合は、エンティティ フィールド ID を指定します。

3. フィルター テーブルとフィルター フィールドを決定します。

    フィルター テーブルは、一致するカテゴリを使用した **PersonSearchResult** として使用可能でなければなりません。 それ以外の場合、フィルターは作成されません。

4. 新しいフィルター レコードを挿入します。

    個人検索フレームワークが、最初にフォームが開いたときに、すべての除外の初期化を自動的に管理します。 除外を使用すると、特定のエンティティ フィールドのフィルター構築機能を抑制できます。

## <a name="create-new-exclusions"></a>新しい除外を作成する

1. **PersonSearchEntityExclusion** テーブルを拡張するには、Chain of Command (COC) を使用します。
2. **CoC メソッド** で、エンティティ、エンティティ フィールド、除外が有効かどうかを指定します。
3. 新しい除外レコードを挿入します。

    個人検索フレームワークが、最初にフォームが開いたときに、すべての除外の初期化を自動的に管理します。

## <a name="additional-resources"></a>その他のリソース

欧州連合の一般的なデータ保護規則 (GDPR) に基づくデータの依頼への応答の一部として、個人検索レポートを拡張している場合、この規則に関する詳細については、[一般データ保護規則の概要](./gdpr-guide.md) を参照してください。

GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。


### <a name="disclaimer"></a>免責事項
(c)2018 Microsoft Corporation. All rights reserved. このドキュメントは、"現状のまま" 提供されます。 URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。 このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。 このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。 内部での参照を目的とする場合、このドキュメントをコピーして使用できます。 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

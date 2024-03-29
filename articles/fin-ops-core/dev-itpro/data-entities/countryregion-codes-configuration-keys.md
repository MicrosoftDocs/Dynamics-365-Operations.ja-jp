---
title: 国/地域コードとコンフィギュレーション キー
description: この記事では、構成キーと国/地域の両方の実装の観点から適用できるシナリオを説明します。
author: peakerbl
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 4644
ms.assetid: 86eda511-b1a6-46d2-bd0f-f9991b727f1a
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3fe63cf0102754267041d2f2835972498dfe6878
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070079"
---
# <a name="countryregion-codes-and-configuration-keys"></a>国/地域コードとコンフィギュレーション キー

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

この記事では、構成キーと国/地域の両方の実装の観点から適用できるシナリオを説明します。

### <a name="customer-table-schema"></a>顧客テーブル スキーマ

| フィールド名     | フィールド ラベル     | 国のコンテキスト |
|----------------|-----------------|-----------------|
| CustNum        | 顧客番号 |                 |
| CustName       | 顧客名   |                 |
| EinvoiceEANNum | EAN             | DK              |
| FiscalCode     | 会計年度コード     | IT              |

### <a name="sample-data"></a>サンプル データ

| CustNum | CustName        | EinvoiceEANNum{DK} | FiscalCode{IT} | DataAreaId |
|---------|-----------------|--------------------|----------------|------------|
| 1       | Contoso デンマーク | AA                 | {Empty}        | DK         |
| 2       | Contoso イタリア   | {Empty}            | DD             | IT         |

### <a name="sample-entity"></a>サンプル エンティティ

| フィールド名     | 国のコンテキスト |
|----------------|-----------------|
| CustomerNumber |                 |
| CustomerName   |                 |
| EAN            | DK              |
| FiscalCode     | IT              |

### <a name="scenario--field-level-only"></a>シナリオ: フィールド レベルでのみ

開発者のアイザックは、地域の設定を含むフィールドがある顧客エンティティを作成します。 エンティティは OData によって消費されます。

**読み取り操作の場合:** エンティティの消費者は、この情報を使用して、有効な地域マッピングを完了します。 コンシューマーは、その地域に必要ではないフィールドを無視します。 たとえば、デンマーク (DK) の消費者は、**EAN** フィールドおよびコア フィールドのみの値の読み取りに関連しています。

**書き込み操作の場合:** エンティティの消費者は、この情報を使用して、データを入力するために必要なフィールドのみを識別します。 コンシューマーは、地域のフィールドおよび関連するコア フィールドの検証が行われることを期待しています。

### <a name="behaviors--fields-only"></a>動作 – フィールドのみ

| シナリオ                        | 説明 |
|---------------------------------|-------------|
| デザイン                          | エンティティは、自動的にローカライズ プロパティを基になるフィールドから継承します。 |
| デザイン                          | 開発者は、エンティティ フィールドのローカライズ プロパティを上書きまたは設定することはできません。 これらのプロパティは、テーブルからのみ継承する必要があります。 マップされていないフィールドにのみ上書き。 |
| 読み取り動作 (OData メタデータ)  | OData のエンティティのコンシューマーは、メタデータまたは注釈を使用して、ローカライズするフィールドを指定します。 |
| 読み取り動作 (データ管理) | インポート/エクスポート フィールドでは、情報がエンドユーザーにわかりやすくなるように、メタデータに国/地域の値を表示します。 |
| 読み取り動作                   | 会社間の読み取り操作中に、ローカライズされたフィールドのデータは、コンテキストが一致した場合にのみ表示されます。 これが既にテーブル/ビューを通じて実装されている必要があることに注意してください。 |
| 読み取り動作 (パフォーマンス)     | 会社固有の読み取り操作中に、コンテキストが一致しない場合、ローカライズされたフィールドはクエリから削除されます。 |
| 書き込み                           | ローカライズされたフィールドへの書き込み操作中に、フィールドがコンテキストに一致しない場合はハード エラーが発生します。 |
| (共有テーブル)                  | データ ソースまたはフィールドに、共有 (グローバル) テーブルである国/地域が含まれている場合、キーが適用されていない場合と同じようにすべての工程が無視されます。 |

### <a name="behavior--data-source"></a>動作 – データ ソース

データ ソースで適用されるコンフィギュレーション キーと国/地域の動作は、フィールドの動作に似ています。 これらの値は、フィールド レベルに適用された場合と同様に、データ ソースから推測されます。 次に例を示します。

```Text
Entity E1

    |_ Data Source 1 (DS1)

        Field1

        Field2

    |_Data Source 2 (DS2) UK

        Field3

            Field4
```

#### <a name="evaluation-at-the-entity-e1-level"></a>エンティティ E1 レベルで評価

```Text
Entity E1

|_F1

|_F2

|_F3 (UK inferred)

|_F4 (UK inferred)
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

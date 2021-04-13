---
title: 検証、既定値、およびマップされていないフィールド
description: このトピックでは、データ エンティティの値を検証する方法、既定値を設定する方法、およびデータ ソース値にマップされていないフィールドを使用する方法について説明します。
author: Sunil-Garg
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 4624
ms.assetid: 7ea995fa-8ea0-403d-8a68-f19993c40a6d
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea6e8b13fd2efb0c7ad807cf3537c1d3c3a47650
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752778"
---
# <a name="validations-default-values-and-unmapped-fields"></a>検証、既定値、およびマップされていないフィールド

[!include [banner](../includes/banner.md)]

このトピックでは、データ エンティティの値を検証する方法、既定値を設定する方法、およびデータ ソース値にマップされないが、代わりに仮想または計算のデータが含まれるフィールド (マップされていないフィールド) を使用する方法について説明します。

## <a name="validations"></a>検証
検証は、フィールド レベルとレコード レベルの両方でエンティティをバックアップするテーブルで定義できます。 検証は、データ エンティティ レベルで定義することもできます。

### <a name="table-data-source-vs-entity-validation"></a>テーブル (データ ソース) とエンティティ検証

エンティティはテーブル (データ ソース) によって戻され、検証はフィールド レベル (**Table.validateField()**) とレコード レベル (**Table.validateWrite()**) の両方でテーブルに対して定義されます。 検証は、これらのテーブルを使用して構築されたデータ エンティティによって考慮されます。 これらの検証はデータ エンティティを戻すテーブルに組み込まれますが、検証はデータ エンティティ レベルで定義することもできます。 テーブルに基づく検証と同様に、エンティティに基づく検証はフィールド レベル (**DataEntity.validateField()**) またはレコード レベル (**DataEntity.validateWrite()**) で書き込むことができます。

### <a name="table-based-validation-behavior"></a>テーブル ベースの検証動作

テーブルの検証は CUD 操作の一部として自動的に実行されます。 **Table.ValidateField、AllowEdit、AllowEditOnCreate** フィールド レベルの検証は、データ エンティティで挿入または更新を実行する時に、自動的に発生します。 これは、すべてのパス (X++、OData など) に当てはまります。 これらの検証は、エンティティから個々のデータ ソースにフィールドがマップされるマッピング処理中に行われます。

[![redo1](./media/redo1-1024x582.png)](./media/redo1.png)

データ エンティティからフィールド値がマップされたデータ ソース フィールドにコピーされた後、フィールドの検証は設定されたフィールドで実行されます。 検証にはテーブル レベルの **validateField** が含まれ、**AllowEdit** および **AllowEditOnCreate** を検証します。 エラーにより検証が失敗した場合、残りのフィールドの検証が続行されます。 最後に、データ ソースのいずれかの検証プロセス中に発生したエラーが発生したかどうかを、検証によって確認します。 エラーがあった場合、この時点でプロセス エラーが発生するようになり、テーブル レベルの **validateWrite()** は呼び出されません。 バックエンド テーブルに対して **validateField** をスキップするには、コンシューマーは **DataEntity.skipDataSourceValidateField(Int \_DataEntityFieldId, ブール値 \_skip)** を呼び出します。 このメソッドのフィールド ID は、データ エンティティにマップされたフィールドのフィールド ID であり、フィールドに、バックエンド テーブルのフィールドではないことに注意してください。 次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの検証をスキップできます。

[![Over9](./media/over9.png)](./media/over9.png)

**Table.ValidateWrite** レコード レベル **Table.ValidateWrite** バックエンドテーブルに定義されている検証は、データ エンティティの挿入および更新を実行すると自動的に発生します。 これは、すべてのパス (X++、OData など) に当てはまります。 これらの検証は、実際の挿入または更新がデータ ソースに適用される直前に行われます。 検証が失敗すると、エラーが発生し、その他のデータ ソースのプロセスが停止されます。 

![redo2](./media/redo2-1024x636.png)

データ エンティティのすべてのバックエンド テーブルに対して **validateWrite** をスキップするには、コンシューマーは **DataEntity.skipDataSourceValidateWrite(ブール値 \_skip)** を呼び出します。 このメソッドは、すべてのデータソースに対して **validateWrite** をオンまたはオフにします。 次の API を使用すると、コンシューマーに関係なく、特定のデータ ソースの検証をスキップできます。

[![Over10](./media/over10.png)](./media/over10.png)

バック エンド テーブルに定義されている **Table.ValidateDelete** レコード レベル **ValidateDelete** 検証は、データ エンティティの削除を実行すると自動的に発生します。 これは、すべてのパス (X++、OData など) に当てはまります。 これらの検証は、削除がデータ ソースに適用される直前に行われます。 検証が失敗すると、エラーが発生し、その他のデータ ソースのプロセスが停止されます。

[![Over11](./media/over11.png)](./media/over11.png)

データ エンティティのすべてのバックエンド テーブルに対して **validateDelete** をスキップするには、コンシューマーは **DataEntity.skipDataSourceValidateDelete(ブール値 \_skip)** を呼び出します。 このメソッドは、すべてのデータソースに対して **validateDelete** をオンまたはオフにします。 次の API を使用すると、コンシューマーに関係なく、特定のデータ ソースの検証をスキップできます。

[![Over12](./media/over12.png)](./media/over12.png)

### <a name="entity-based-validation-behavior"></a>エンティティ ベースの検証動作

<table>
<thead>
<tr>
<th>検証</th>
<th>ターゲット</th>
<th>呼び出し側</th>
</tr>
</thead>
<tbody>
<tr>
<td>DataEntity.ValidateField</td>
<td><ul>
<li>データ型</li>
<li>必須の関係 (テーブルおよび拡張データ型 [EDT] の両方)</li>
<li>カスタム検証</li>
<li>基本マップのテーブル フィールドの <strong>validateField</strong> を呼び出さないでください。</li>
</ul></td>
<td><ul>
<li>OData から自動的に呼び出されます</li>
<li>フィールドが変更されたときに、フォーム エンジンで呼び出されます</li>
<li>挿入/更新が X++ コードから発生した場合は、自動的に呼び出されません</li>
</ul></td>
</tr>
<tr>
<td>DataEntity.ValidateWrite</td>
<td><ul>
<li>必須の列</li>
<li>関係 (テーブルおよび EDT の両方)</li>
<li>カスタム検証</li>
<li>基本テーブルのテーブル レベル <strong>validateWrite</strong> を呼び出さないでください。</li>
</ul></td>
<td><ul>
<li>OData から自動的に呼び出されます</li>
<li>レコードが保存されたときに、フォーム エンジンで呼び出されます</li>
<li>挿入/更新が X++ コードから発生した場合は、自動的に呼び出されません</li>
</ul></td>
</tr>
<tr>
<td>DataEntity.ValidateDelete</td>
<td><ul>
<li>DeleteActions</li>
<li>カスタム検証</li>
<li>基本テーブルの テーブル レベル <strong>validateDelete</strong> を呼び出さないでください。</li>
</ul></td>
<td><ul>
<li>OData から自動的に呼び出されます。</li>
<li>レコードが削除されたときに、フォーム エンジンで呼び出されます</li>
<li>削除が X++ コードから発生した場合は、自動的に呼び出されません</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="defaults"></a>既定
初期化と行には既定値を指定できます。

### <a name="initializations"></a>初期化

**DataEntity.initValue:** データ エンティティは、既定値で、エンティティ レベル **initValue** に存在するカスタム ロジックを使用して初期化されます。 このメソッドは、X++ からのデータ エンティティに対して挿入または更新が実行されたときに自動的に呼び出されることはありません。 必要な場合に明示的に呼び出す必要があります。 このメソッドは、新しいレコードが作成されるときにフォーム エンジンによって自動的に呼び出されます。 **DataEntity.initValue** は、データ エンティティで使用されるバック エンド テーブルの **initValue** メソッドを呼び出しません。 **Table.initValue:** テーブル レベル **initValue** は、バック エンド テーブル定義に従って、データ エンティティの挿入を実行するときに発生します。 これは、すべてのパス (X++、OData など) に当てはまります。 **Table.initValue** はエンティティがデータ ソース フィールドにマップされる直前に実行されます。

[![Over13](./media/over13.png)](./media/over13.png)

データ エンティティのすべてのバックエンド テーブルに対してエンティティ レベルの **initValue** をスキップするには、コンシューマーは **DataEntity.skipDataSourceInitValue(ブール値 \_skip)** を呼び出します。 このメソッドは、すべてのデータソースに対して **initValue** をオンまたはオフにします。 次の API を使用することによって、コンシューマーに関係なく、特定のフィールドの **initValue** をスキップできます。

[![Capturea](./media/capturea.png)](./media/capturea.png)

### <a name="defaultrow"></a>DefaultRow

**DataEntity.DefaultRow: DataEntity.DefaultRow** は、**defaultField** および **getDefaultingDependencies** と組み合わせて使用され、既定値を提供します。 X++ またはフォーム エンジンによって自動的に呼び出されません。 **Table.DefaultRow: Table.DefaultRow** は、データソースの挿入と検証の前に、マッピングが完了した後データソースに対して自動的に呼び出されます。

[![Captureb](./media/captureb.png)](./media/captureb.png)

## <a name="unmapped-fields"></a>マップされていないフィールド
データ エンティティは、データ ソースのフィールドに直接マップされているフィールドに *マップされていない* フィールドを追加できます。 マップされていないフィールドの値を生成するメカニズムは 2 つあります。

- カスタム X++ コード
- Microsoft SQL Server によって実行される SQL

マップされていない2種類のフィールドは、*仮想* と *計算* です。 マップされていないフィールドは常に読み取り操作をサポートしますが、機能仕様では、書き込み操作をサポートするための開発作業は必要とされない場合があります。

**仮想フィールド**

- 保持されないフィールド。
- カスタム X++ コードによって制御されます。
- 読み取り/書き込みは、カスタム X++ コードを通じて発生します。
- 通常は X++ コードを用いて計算される入力値に使用され、計算された列によって置き換わることはできません。

**計算フィールド**

- 値は、SQL ビューの計算列によって生成されます。
- 読み取り中に、データは SQL によって計算され、ビューから直接フェッチされます。
- 書き込みについては、カスタム X++ コードは入力値を解析し、データ エンティティの通常のフィールドに解析された値を書き込む必要があります。 値はエンティティのデータ ソースの通常のフィールドに格納されます。
- ほとんどの場合の読み取りに使用されます。
- 計算された列は SQL Server レベルで計算されている一方、仮想フィールドは、X++ の行ごとに計算された行であるため、可能な限り仮想フィールドではなく計算された列を使用することをお勧めします。

### <a name="properties-of-unmapped-fields"></a>マップされていないフィールドのプロパティ

<table>
<thead>
<tr>
<th>カテゴリ</th>
<th>氏名</th>
<th>種類</th>
<th>既定値</th>
<th>動作</th>
</tr>
</thead>
<tbody>
<tr>
<td>データ</td>
<td>IsComputedField</td>
<td>NoYes</td>
<td>有</td>
<td><ul>
<li><strong>はい:</strong> フィールドは、SQL ビューの計算済み列として同期されます。 X++ メソッドは列の SQL 定義文字列を計算する必要があります。 仮想列の定義は静的であり、エンティティが同期されているときに使用されます。 その後は、X++ メソッドは、実行時に呼び出されません。</li>
<li><strong>いいえ:</strong> フィールドは、入庫および出荷の値がカスタム コードによって完全に制御される真の仮想フィールドです。</li>
</ul></td>
</tr>
<tr>
<td>データ</td>
<td>ComputedFieldMethod</td>
<td>文字列</td>
<td></td>
<td>X++ の静的 <strong>DataEntity</strong> メソッドは、フィールド定義を生成する SQL 式の構築に使用されます。 <strong>IsComputedField</strong> プロパティが <strong>いいえ</strong> に設定されている場合、このプロパティは無効で無関係です。 このメソッドは、<strong>IsComputedField</strong> プロパティが <strong>はい</strong> に設定されている場合に必要です。</td>
</tr>
<tr>
<td>データ</td>
<td>ExtendedDataType</td>
<td>文字列</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### <a name="unmapped-field-comparison"></a>マップされていないフィールドの比較

<table>
<thead>
<tr>
<th></th>
<th>仮想フィールド</th>
<th>計算フィールド</th>
</tr>
</thead>
<tbody>
<tr>
<td>メタデータのプロパティ</td>
<td>No と算出されます</td>
<td><ul>
<li>計算済み = はいとなります。</li>
<li>計算フィールド メソッド = 静的メソッド</li>
</ul></td>
</tr>
<tr>
<td>既読</td>
<td><ul>
<li>X++ (override <strong>postLoad</strong>)</li>
<li>1 行ずつ</li>
</ul></td>
<td><ul>
<li>SQL 計算列</li>
<li>セット ベースの読み取り可能</li>
</ul></td>
</tr>
<tr>
<td>書き込み</td>
<td>X++ (override <strong>mapEntityToDataSource</strong>)</td>
<td>X++ (override <strong>mapEntityToDataSource</strong>)</td>
</tr>
<tr>
<td>メリット</td>
<td><ul>
<li>スキーマにバインドされていないため公開契約は同じですが、実装が変更される可能性があります</li>
<li>X++ メソッドの呼び出し</li>
</ul></td>
<td>高速読み込みで、大きなエクスポートはビューから直接発生が可能</td>
</tr>
</tbody>
</table>

### <a name="examples"></a>例

次のテーブルは、**UnitOfMeasure** のリレーションシップが存在する場合の計算例を示し、マップされていないフィールドにその値を表示します。

| 仮想フィールド | 計算フィールド |
|---------------|----------------|
| postLoad() で、*// UnitOfMeasureInternalCode.UnitOfMeasure//Set hasFixedInternalCode 値に、フィールドに基づいてレコードが存在するかどうかを確認します* (this.UnitOfMeasure)this.HasFixedInternalCodeVirtual = NoYes::Yes; else this.HasFixedInternalCodeVirtual = NoYes::No; の場合 | ComputedFieldMethod() で *// 任意の SQL 計算された列の明細書 (T2.RECID が NULL の場合は 0 ELSE 1)INTとして)* |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

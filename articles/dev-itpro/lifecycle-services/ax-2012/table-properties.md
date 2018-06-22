---
title: "表のプロパティ"
description: "このトピックでは、アプリケーション オブジェクト ツリー (AOT) におけるテーブル要素の <strong>プロパティ</strong> ウィンドウにあるプロパティについて説明します。 テーブル要素は、<strong>データ ディクショナリ</strong> &gt; <strong>テーブル</strong> にあります。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18141
ms.assetid: 1ad8b7e9-80b3-44a3-b57d-7e9fc88db038
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 28604cb27d187432ce46f81680605925b2c1b2c4
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="table-properties"></a>表のプロパティ

[!include [banner](../../includes/banner.md)]

このトピックでは、アプリケーション オブジェクト ツリー (AOT) におけるテーブル要素の <strong>プロパティ</strong> ウィンドウにあるプロパティについて説明します。 テーブル要素は、<strong>データ ディクショナリ</strong> &gt; <strong>テーブル</strong> にあります。

プロパティ値の設定に関するガイドラインについては、[テーブル プロパティのベスト プラクティス](http://msdn.microsoft.com/library/5def498e-107d-4a2b-a621-fbbe0243e399(AX.60).aspx) を参照してください。 次は、テーブル要素の下のサブ要素になっている AOT 要素のプロパティについてのトピックの一覧です。

## <a name="table-properties"></a>表のプロパティ
次のテーブルは、AOT でのテーブル要素のプロパティを示しています。

<table>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
<th>今回のバージョンの Microsoft Dynamics AX での新要素</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><span class="ui">抽象</span></strong></td>
<td>テーブルが継承をサポートするかどうかを指定します。 既定値は [<span class="ui">いいえ</span>] です。 値が<span class="ui">はい</span>である場合、テーブルが、<span class="code">update_recordset</span>および<span class="code">select</span> ステートメントのような X++ SQL ステートメントの直接ターゲットにはなりません。 このプロパティは、<span class="ui">SupportInheritance</span> プロパティが [<span class="ui">いいえ</span>] に設定されている場合は使用できません。 詳細については、「<a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">テーブル継承の概要</a>」を参照してください。</td>
<td>AX 2012</td>
</tr>
<tr class="even">
<td><strong><span class="ui">AnalysisDimensionType</span></strong></td>
<td><span class="ui">IsLookup</span> プロパティ設定に基づいて作成される分析コードのタイプを決定します。 次の値のいずれかを指定することができます。<ul>
<li><strong><span class="ui">自動</span></strong> - 表に事実データと分析コード データが含まれる可能性があることを指定します。 事実に基づくデータはメジャーを作成するために抽出されますが、<strong>BI ウィザード</strong>は、分析コード データを抽出して分析コードと属性を作成します。 1 つの子分析コードが親テーブルからの属性で作成されます。</li>
<li><strong><span class="ui">MasterInner</span></strong> - このテーブルと子テーブルの関係を作成する内部 (完全) 結合を指定します。 表およびテーブルの各レコードの組み合わせは、分析コードで生成されます。 1 つの子分析コードが親テーブルからの属性で作成されます。</li>
<li><strong><span class="ui">MasterLeftOuter</span></strong> - このテーブルと子テーブルの関係を作成する左外部結合を指定します。 分析コードには、このテーブルの値に基づいて追加の属性が設定されます。この属性は空にすることもできます。 1 つの子分析コードが親テーブルからの属性で作成されます。</li>
<li><strong><span class="ui">トランザクション</span></strong> - テーブルが厳密に事実データ (測定) を生成するために使用されることを指定します。 この設定は、テーブルにトランザクション データのみが含まれている場合に使用する必要があります。 テーブルから列挙型フィールドのみを含む 1 つの子分析コードが作成されます。 <strong><span class="ui">IsLookup</span></strong> プロパティが<strong><span class="ui">いいえ</span></strong>に設定
<li><strong><span class="ui">自動</span></strong> - 表に事実データと分析コード データが含まれる可能性があることを指定します。 事実に基づくデータはメジャーを作成するために抽出されますが、<strong>BI ウィザード</strong>は、分析コード データを抽出して分析コードと属性を作成します。 1 つの親と子の分析コードが作成されます。</li>
<li><strong><span class="ui">MasterInner</span></strong> - 適用できません。 <span class="ui">Auto</span> と同じ。</li>
<li><strong><span class="ui">MasterLeftOuter</span></strong> - 適用できません。 <span class="ui">Auto</span> と同じ。</li>
<li><strong><span class="ui">トランザクション</span></strong> - テーブルが厳密に事実データ (測定) を生成するために使用されることを指定します。 この設定は、テーブルにトランザクション データのみが含まれている場合に使用する必要があります。 テーブルから列挙値のみを含む 1 つの子分析コードが作成されます。</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">AnalysisIdentifier</span></strong></td>
<td>SQL Server Analysis Services (SSAS) キューブ内の分析コードの ID として使用するフィールドを指定します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">AOSAuthorization</span></strong></td>
<td>ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定します。 このプロパティを <strong><span class="ui">なし</span></strong> に設定すると、承認チェックは実行されません。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">CacheLookup</span></strong></td>
<td>ルックアップ操作中に取得されたレコードをキャッシュする方法を決定します。 この <strong><span class="ui">CacheLookup</span></strong> プロパティは、別のテーブルから継承しないテーブルのみに存在します。 継承ルート テーブルでは、AOT <span class="ui">プロパティ</span>ウィンドウを使用して、このプロパティを <strong><span class="ui">EntireTable</span></strong> に設定することはできません。 継承ルート テーブルにこの値を割り当てるために、他の手法を使用しないでください。 たとえば、この値を割り当てる <strong><span class="code">TreeNode</span></strong> クラスの <strong><span class="code">AOTsetProperty</span></strong> メソッドを使用しないでください。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">ClusterIndex</span></strong></td>
<td>クラスター インデックスを指定します。 このプロパティは、SQL 最適化の目的でのみ使用されます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">ConfigurationKey</span></strong></td>
<td>テーブルのコンフィギュレーション キーを指定します。 コンフィギュレーション キーにより、システム管理者はアプリケーションの特定の部分を有効または無効にすることができます。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">CountryRegionCodes</span></strong></td>
<td>テーブルが適用されるか有効な国/地域コードを指定します。 クライアント フレームワークおよびアプリケーションは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。 これは、カンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳に含まれるデータと一致する必要があります。</td>
<td>AX 2012</td>
</tr>
<tr class="odd">
<td><strong><span class="ui">CountryRegionContextField</span></strong></td>
<td>国のコンテキストを識別するために使用されるフィールドを指定します。 これは<strong><span class="ui">CountryRegionCodes</span></strong> プロパティに関連しています。</td>
<td>AX 2012</td>
</tr>
<tr class="even">
<td><strong><span class="ui">CreatedBy</span></strong></td>
<td>システムがテーブルのレコードの <strong><span class="code">CreatedBy</span></strong> フィールドを管理しているかどうかを示します。 このフィールドには、特定のレコードの作成者に関する情報が含まれます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">CreatedDateTime</span></strong></td>
<td>システムがテーブルのレコードの <strong><span class="code">CreationDate</span></strong> および <strong><span class="ui">CreationTime</span></strong> フィールドを管理しているかどうかを示します。 このフィールドには、レコードが最後に作成された日付が含まれます。</td>
<td>AX 2012</td>
</tr>
<tr class="even">
<td><strong><span class="ui">CreatedTransactionId</span></strong></td>
<td>システムがテーブルのレコードの <strong><span class="code">CreatedTransactionId</span></strong> フィールドを管理しているかどうかを示します。 このフィールドにはレコードを作成した取引に関する情報が含まれます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">CreateRecIdIndex</span></strong></td>
<td><strong>レコード ID</strong> フィールドでインデックスが作成されたかどうかを示します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">DeveloperDocumentation</span></strong></td>
<td>テーブルの目的を説明し、アプリケーションでどのように使用されるかを説明します。 説明は、通常 5 つ以下の構文で構成され、単一の段落として書かれます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">EntityRelationshipType</span></strong></td>
<td>共通エンティティ リレーションシップ (ER) データ モデルの表記法に従ってテーブルを分類します。 テーブルは、エンティティまたはリレーションシップとして分類されます。 エンティティはオブジェクトを表します。 リレーションシップは、2 つのオブジェクトの間の関連付けを表します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">拡張</span></strong></td>
<td>プロパティ値として選択された別のテーブルからテーブルを派生させます。 <span class="ui">SupportInheritance</span> プロパティが <span class="ui">Yes</span> に設定されている場合、値は null です。 詳細については、「<a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">テーブル継承の概要</a>」を参照してください。</td>
<td>AX 2012</td>
</tr>
<tr class="odd">
<td><strong><span class="ui">FormRef</span></strong></td>
<td>テーブルが参照されているときに発生する表示メニュー項目を指定します。 表示メニュー項目は、フォームに関連付けられます。 レポートのプライマリ インデックス フィールドを使用するとき、このフォームはレポート内のリンクとして使用できます。 プライマリ インデックスを指定するには、<strong><span class="code">PrimaryIndex</span></strong> プロパティを使用します。 このフィールドを空白のままにすると、システムではでテーブルと同じ名前のフォームを表示しようとします。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">ID</span></strong></td>
<td>システムによって生成されたテーブル <span class="code">ID</span> を指定します。 詳細については、「<a href="http://msdn.microsoft.com/library/2951f194-4362-460e-8607-7f9fc0022449(AX.60).aspx">アプリケーション オブジェクト ID</a>」を参照してください。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">IsLookup</span></strong></td>
<td>レポート モデルについては、テーブルの情報が、レポート モデルが生成されるときに参照する他のテーブルに組み込まれているかどうかを指定します。 OLAP キューブで、連結分析コードまたは異なる分析コードを生成するかどうかを決定します。 次の値のいずれかを指定することができます。
<ul>
<li><strong><span class="ui">はい</span></strong> - テーブルの属性が親分析コード (スター スキーマ) に連結されることを示します。</li>
<li><strong><span class="ui">いいえ</span></strong> - テーブル (スノーフレーク スキーマ) に対して個別の分析コードが生成されることを示します。</li>
</ul>
分析コードおよびスターとスノーフレーク スキーマの詳細については、<a href="http://go.microsoft.com/fwlink/?LinkId=115450">分析コードの概要 (SQL Server 2005 オンライン ブック)</a> を参照してください。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">ラベル</span></strong></td>
<td>テーブルのラベルを指定します。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">ListPageRef</span></strong></td>
<td>このレコードの種類の一覧を表示できるフォームをポイントする表示メニュー項目を指定します。</td>
<td>AX 2012</td>
</tr>
<tr class="even">
<td><strong><span class="ui">モデル</span></strong></td>
<td>テーブルがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 要素例には、テーブルまたはクラスがあります。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
<td>AX 2012</td>
</tr>
<tr class="odd">
<td><strong><span class="ui">ModifiedBy</span></strong></td>
<td>システムがテーブルのレコードの <strong><span class="code">ModifiedBy</span></strong> フィールドを管理しているかどうかを示します。 このフィールドは、レコードに最後の変更を行った人を記録します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">ModifiedDateTime</span></strong></td>
<td>システムがテーブルのレコードの <strong><span class="code">ModifiedDateTime</span></strong> フィールドを管理しているかどうかを示します。 このフィールドには、レコードの最終変更日が記録されます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">ModifiedTime</span></strong></td>
<td>システムがテーブルのレコードの <strong><span class="code">ModifiedTime</span></strong> フィールドを管理しているかどうかを示します。 このフィールドには、レコードが最後に変更された時刻が記録されます。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">名前</span></strong></td>
<td>テーブル名を指定します。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">OccEnabled</span></strong></td>
<td>テーブルでオプティミスティック同時実行モードを有効にするかどうかを指定します。 このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。 データは、実際の更新の実行時にのみロックされます。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">PreviewPartRef</span></strong></td>
<td>拡張プレビューで使用される<span class="ui">情報パーツ</span>または<span class="ui">フォーム パーツ</span>を指定します。 情報パーツは指定したクエリからデータ フィールドのコレクションを表示しています。 情報パーツはメタデータを使用してデータの表示方法を説明します。 フォーム パーツは、フォームへのポインターを表します。</td>
<td>AX 2012</td>
</tr>
<tr class="odd">
<td><strong><span class="ui">PrimaryIndex</span></strong></td>
<td>プライマリ インデックスを指定します。 固有のインデックスのみ選択することができます。 このプロパティは、データベースの最適化を目的として、またキャッシュ キーとして使用するユニーク索引を示すために使用されます。 プライマリ インデックスが指定されていない場合、最下位の ID の固有のインデックスは、キャッシュ キーとして使用されます。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">ReplacementKey</span></strong></td>
<td>一部のフォーム コントロール内のデータの識別子として表示するフィールドを指定します。</td>
<td>AX 2012</td>
</tr>
<tr class="odd">
<td><strong><span class="ui">ReportRef</span></strong></td>
<td>テーブルが参照されているときに発生する出力メニュー項目を指定します。 出力メニュー項目はレポートに関連付けられています。 レポートのプライマリ インデックス フィールドを使用するとき、このレポートはレポート内のリンクとして使用できます。 プライマリ インデックスを指定するには、<span class="code">PrimaryIndex</span> プロパティを使用します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">SaveDataPerCompany</span></strong></td>
<td>現在の会社のデータが保存されるかどうかを示します。 プロパティを<strong><span class="ui">いいえ</span></strong>に設定すると、データは会社識別子 (<span class="code">DataAreaId</span>) なしで保存されます。
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>メモ</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong><span class="code">SaveDataPerCompany</span></strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルをデータ ソースとして使用するフォーム デザインの <strong><span class="code">SetCompany</span></strong> プロパティもはいに設定する必要があります。</td>
</tr>
</tbody>
</table>
</div>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>ヒント</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>会社の略語はステータス行に表示されます。 略称をダブルクリックするとダイアログ ボックスが開き、別の会社に変更されます。</td>
</tr>
</tbody>
</table>
</div></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">SaveDataPerPartition</span></strong></td>
<td>テーブルに <strong><span class="code">Partition</span></strong> という名前のシステム フィールドが含まれているかどうかを示します。 これは、読み取り専用のシステム フィールドを意味します。 テーブルに<strong><span class="code">パーティション</span></strong> フィールドがない場合、各レコードに 1 つのパーティションに割り当てられます。 各レコードは、他のパーティションのコンテキストで実行されるデータ アクセス操作から隠されています。</td>
<td>AX 2012 R2</td>
</tr>
<tr class="even">
<td><strong><span class="ui">SearchLinkRefName</span></strong></td>
<td>エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目の名前を指定します。 <strong><span class="code">SearchLinkRefType</span></strong> プロパティが URL に設定されている場合、メニュー項目を、テーブル データが表示されている Web パーツ ページにリンクする <strong><span class="code">SearchLinkRefName</span></strong> プロパティ リストから選択します。 Web パーツ ページのフォームおよびレポートは、データを表示できます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">SearchLinkRefType</span></strong></td>
<td>エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目のタイプを指定します。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">SingularLabel</span></strong></td>
<td>テーブルに格納される品目の 1 つの名前を表示するために、レポート モデルまたはキューブで使用されるラベルを指定します。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">SupportInheritance</span></strong></td>
<td>このプロパティを <strong><span class="ui">Yes</span></strong> に設定ｓるうと、<strong><span class="ui">Extends</span></strong> や <strong><span class="ui">Abstract</span></strong> などの、その他の継承関連のプロパティの値を設定できます。
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>注意 </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>値を<strong><span class="ui">はい</span></strong>に設定するとき、テーブル上のどのフィールドも削除され、再度作成する必要があります。</td>
</tr>
</tbody>
</table>
</div>
詳細については、「<a href="http://msdn.microsoft.com/library/cb4803e7-9a29-4c54-be43-63722557dac6(AX.60).aspx">テーブル継承の概要</a>」を参照してください。</td>
<td>AX 2012</td>
</tr>
<tr class="even">
<td><strong><span class="ui">SystemTable</span></strong></td>
<td>テーブルをシステム テーブルとして表示するかどうかを示します。 エクスポートおよびインポート中にフィルターできます。 システム テーブルは、ログイン時に常に同期されます。 これは、ログインするとすぐに使用するテーブルに便利です。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">TableContents</span></strong></td>
<td>顧客間でセットアップ/パラメーター データを再利用する方法を指定します。 次の値が可能です。
<ul>
<li><strong><span class="ui">指定なし</span></strong> - ほとんどのテーブルで。</li>
<li><strong><span class="ui">既定のデータ</span></strong> - 郵便番号、単位、時間間隔などの顧客に依存しないデータに使用します。</li>
<li><strong><span class="ui">基本データ</span></strong> - カレンダー、グループ、およびパラメータなどの顧客に依存するデータを使用します。</li>
<li><strong><span class="ui">既定 + 基本データ</span></strong> - ローカル知覚が異なるデータに使用します。 たとえば、勘定科目表は、ドイツでは顧客に依存していませんが、世界の他のほとんどの場所では顧客に依存しています。</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">TableGroup</span></strong></td>
<td>テーブルが属するグループを決定します。 <a href="http://msdn.microsoft.com/library/3330d438-ab53-44db-9a9b-a044ed19608d(AX.60).aspx">テーブル グループ</a>は、テーブルに含まれるデータのタイプに応じてテーブルを分類する方法を提供します。 テーブルをデータ ソースとして使用することにより、フォーム内のテーブルから更新または削除するときにシステムがユーザーに確認を求めるかどうか定義するためにテーブル グループを使用することができます。 データをエクスポートするとき、テーブル グループを使用してレコードをフィルターすることができます。</td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">TableType</span></strong></td>
<td>Microsoft Dynamics AX 2009 にある<strong><span class="ui">一時的</span></strong>なプロパティを置き換えます。 詳細については、<a href="http://msdn.microsoft.com/library/9986b514-6079-499a-b491-9a95589f8229(AX.60).aspx">一時テーブルおよび TableType プロパティ</a> を参照してください。</td>
<td>AX 2012</td>
</tr>
<tr class="even">
<td><strong><span class="ui">TitleField1</span></strong>, <strong><span class="ui">TitleField2</span></strong></td>
<td>次の操作を実行できるようにします。
<ul>
<li>フォーム キャプションにテーブル フィールド データを追加します。</li>
<li>ルックアップ フォームに追加のフィールドを表示します。 詳細については、<a href="http://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx">方法: ルックアップ フォームでコントロールの追加</a>を参照してください。 <strong><span class="code">TitleField1</span></strong> プロパティは、フォーム上のフィールドでルックアップ リストを有効化するときにも使用されます。 <strong><span class="code">TitleField1</span></strong> および <strong><span class="code">TitleField2</span></strong> プロパティに指定するフィールドはキー値でマージすることができます</li>
<li>ツールヒントにフィールドの情報を表示します。</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><strong><span class="ui">TypicalRowCount</span></strong></td>
<td>テーブル内に通常表示されるレコード数を指定します。 <strong><span class="code">AnalysisSelection</span></strong> プロパティが設定されていない場合、<strong><span class="code">TypicalRowCount</span></strong> プロパティは、Microsoft SQL Server レポート サービスのレポート ビルダーを使用してレコードを選択する方法を決定します。 <strong><span class="code">TypicalRowCount</span></strong> プロパティの設定は、ドロップダウン リスト、リスト ボックス、フィルタリングされたリスト ボックスを使用してテーブル レコードを選択するかどうかに影響します。 詳細については、<a href="http://msdn.microsoft.com/library/5def498e-107d-4a2b-a621-fbbe0243e399(AX.60).aspx">テーブル プロパティのベスト プラクティス</a> を参照してください。</td>
<td></td>
</tr>
<tr class="even">
<td><strong><span class="ui">ValidTimeStateFieldType</span></strong></td>
<td>期間内のデータを追跡するときに使用するためのシステムの日付/時刻フィールドのタイプを指定します。</td>
<td>AX 2012</td>
</tr>
<tr class="odd">
<td><strong><span class="ui">表示</span></strong></td>
<td>テーブルがフォームやレポート内のデータ ソースとして使用される場合のアクセス権を指定します。 テーブルをフォーム内のデータ ソースとして使用する場合、フォームのアクセス権は、テーブルに対して定義されているアクセス権を超えることはできません。</td>
<td></td>
</tr>
</tbody>
</table>

## <a name="tables-and-report-models"></a>テーブルおよびレポート モデル
次のプロパティは、レポートに情報を追加するために使用されるレポート モデルに関連しています。
-   AnalysisSelection
-   AnalysisVisibility
-   IsLookup
-   SingularLabel
-   TypicalRowCount



<a name="additional-resources"></a>その他のリソース
--------

[AOT のデータ ディクショナリ ノード](http://msdn.microsoft.com/library/4d7d1f77-11b8-4d8a-a44c-85e7d288c368(AX.60).aspx)





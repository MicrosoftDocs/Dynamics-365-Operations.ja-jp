---
title: アプリケーション エクスプローラーのプロパティ
description: このトピックでは、アプリケーション エクスプローラーの品目向けに Microsoft Visual Studio のプロパティ ウィンドウに表示されるプロパティについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: reference
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 85213
ms.assetid: ca186dda-8a78-4969-9be0-b81be00892e5
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f86955197c8e79ff68ac6c2a161d6b8c980a9e65
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183381"
---
# <a name="application-explorer-properties"></a>アプリケーション エクスプローラーのプロパティ

[!include [banner](../includes/banner.md)]

このトピックでは、アプリケーション エクスプローラーの品目向けに Microsoft Visual Studio のプロパティ ウィンドウに表示されるプロパティについて説明します。

アプリケーション エクスプローラーの多くのノードは、それに関連付けられているプロパティを持つ要素を表します。 Microsoft Visual Studio の **プロパティ** ウィンドウで、これらのプロパティを読み取りまたは変更することができます。

## <a name="system-and-common-properties"></a>システムと共通プロパティ
アプリケーション エクスプローラーのほとんどのアプリケーション オブジェクトには、システム プロパティの標準セットがあります。 これらのシステム プロパティは読み取り専用です。 **プロパティ** ウィンドウを使用すると、アプリケーション エクスプローラーで任意の項目のプロパティを表示することができます。 **プロパティ** ウィンドウを開くには、アプリケーション エクスプローラーでノードを右クリックし、**プロパティ** をクリックします。 **カテゴリ**のタブの**プロパティ**ウィンドウで、多数のシステム プロパティが、**統計**ノードの下に表示されます。 この記事では、すべてではないが多くのアプリケーション エクスプローラー ノードで繰り返される追加の共通プロパティを示します。 次のテーブルは、多くのアプリケーション エクスプローラー ノードで検出されるシステム プロパティを示しています。 これらすべてのシステム プロパティは読み取り専用です。

| プロパティ     | 説明                                                       |
|--------------|-------------------------------------------------------------------|
| ChangedBy    | オブジェクト (多くの場合はリリース バージョン) を最後に変更したユーザー。 |
| ChangedDate  | オブジェクトが最後に変更された日付。                        |
| ChangedTime  | オブジェクトが最後に変更された時間。                        |
| CreatedBy    | オブジェクトを作成したユーザー。                                  |
| CreationDate | オブジェクトが作成された日付。                             |
| CreationTime | オブジェクトが作成された時間。                             |

次のテーブルは、すべてではないが、多くのアプリケーション エクスプローラー ノードで検出されるその他の一般的なプロパティを示しています。

| プロパティ          | 説明                                                                                                                                                                                                                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ConfigurationKey  | 要素へのアクセスまたは表示を制御するコンフィギュレーション キーを指定します。 ユーザーがコンフィギュレーション キーにアクセスできない場合は、要素は表示されません。 要素には、ページ、ページのコントロール、テーブル、およびその他の要素があります。                                                                            |
| LegacyID          | 以前のバージョンからの識別子要素です。 以前のバージョンからの更新中に、古い識別子が **LegacyID** に割り当てられます。 インストール固有の識別子は割り当てられず、ビジネス ロジックは保持されます。 このプロパティは、新しい要素には使用されません。                                             |
| NeededAccessLevel | ユーザーが必要とする最小アクセスレベル。 このプロパティは、読み取り専用です。                                                                                                                                                                                                                                           |
| 元金額            | アプリケーション エクスプローラー要素のグローバル一意識別子 (GUID)。 このプロパティは、同期中およびアップグレード時に要素を識別するために使用されます。 これは読み取り専用のプロパティで、システムが割り当てると値が変わることはありません。 システムのどの場所にも重複する元の GUID 値はありません。 |
| SecurityKey       | このプロパティは廃止されましたが、以前のバージョンからアップグレードされたシステムでは参照のために保持されます。                                                                                                                                                                                                       |

## <a name="base-enum-properties"></a>基本列挙型のプロパティ
次のテーブルに、列挙型で使用可能なプロパティを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AnalysisUsage</td>
<td>キューブにおける列挙値の役割を指定します。 この設定は、列挙を参照するすべてのテーブル フィールドに自動的に反映されます。 ただし、テーブル フィールドの設定を上書きできます。  次のオプションを使用できます。
<ul>
<li><strong>属性 </strong>- 列挙を参照するフィールドは、分析コードの属性です。</li>
<li><strong>なし</strong> - 列挙型を参照するフィールドは分析コードの属性ではありません。</li>
</ul></td>
</tr>
<tr class="even">
<td>ConfigurationKey</td>
<td>構成キーを指定します。</td>
</tr>
<tr class="odd">
<td>CountryRegionCodes</td>
<td>ビューが適用されるか有効な国/地域のコードを指定します。 このプロパティは、ISO (国際標準化機構) 国/地域コードをコンマで区切った単一の文字列のリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアント フレームワークおよびアプリケーションは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</td>
</tr>
<tr class="even">
<td>DisplayLength</td>
<td>表示される文字数を指定します。 既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>ヘルプ</td>
<td>フィールドのヘルプ文字列を作成します。 フィールドがページで使用されている場合は、ヘルプ文字列が表示されます。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>ページおよびレポートに表示されるラベルを指定します。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>テーブルがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルおよびクラスがあります。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="even">
<td>氏名</td>
<td>列挙名を指定します。 列挙名は、可能な列挙値または列挙値のタイプのいずれかを示す必要があります。 可能な値に従って呼ばれる列挙型の例には、<strong>InclExcl</strong> および <strong>NextPrevious</strong> があります。 列挙値タイプに従って呼ばれる列挙型例には、<strong>ArrivalPostingType</strong> および <strong>ListStatus</strong> があります。</td>
</tr>
<tr class="odd">
<td>スタイル</td>
<td>列挙型の既定の外観を変更します。  次のオプションを使用できます。
<ul>
<li>コンボ ボックス</li>
<li>オプション ボタン</li>
</ul></td>
</tr>
<tr class="even">
<td>UseEnumValue</td>
<td><strong>はい</strong>の値は、<strong>EnumValue</strong> プロパティの規定値が変更されたことを示します。 <strong>いいえ</strong>の値は、<strong>EnumValue</strong> プロパティを既定値にリセットします。</td>
</tr>
</tbody>
</table>

## <a name="extended-data-type-properties"></a>拡張データ型プロパティ
拡張データ型 (EDT) プロパティーは、すべての EDTs に共通であるか、または特定の基本データ型に対してのみ使用可能かに基づいて、以下のグループに分類されます。

### <a name="properties-that-are-common-to-all-edts"></a>すべての EDT に共通のプロパティ

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>配置</td>
<td>現在のテキストの配置を変更します。 <strong>左</strong>、<strong>右</strong>、または <strong>中央</strong> を選択できます。</td>
</tr>
<tr class="even">
<td>AnalysisDefaultSort</td>
<td>この EDT を含むレポート モデルでフィールドの既定の並べ替え順序を指定します。</td>
</tr>
<tr class="odd">
<td>AnalysisDefaultTotal</td>
<td>メジャーの集計関数を指定します。 <strong>AnalysisUsage</strong> プロパティが<strong>測定</strong>に設定されている場合、このプロパティを使用します。  次のオプションを使用できます。
<ul>
<li><strong>合計 </strong>- セット内のすべての値の合計を返します。</li>
<li><strong>カウント</strong> - セット内の null 以外の品目の数を返します。</li>
<li><strong>CountDistinct</strong> - セット内の特徴的な null 以外の品目の数を返します。</li>
<li><strong>最小</strong> - セット内の最小値を返します。</li>
<li><strong>最大</strong> - セット内の最大値を返します。</li>
<li><strong>なし</strong> - 集計関数は適用されません。</li>
<li><strong>自動 </strong>- このオプションは、派生 EDT に適用されます。 親 EDT が使用される <strong>AnalysisUsage</strong> プロパティの値。</li>
</ul>
フィールド レベルで集計関数をオーバーライドすることができます。 つまり、そのフィールドの <strong>AnalysisDefaultTotal</strong> プロパティを使用することで、フィールドの集計関数を変更できます。</td>
</tr>
<tr class="even">
<td>AnalysisGrouping</td>
<td>Microsoft SQL Server Reporting Services (SSRS) のレポート ビルダーを使用してフィールドがレポートに追加されるとき、この EDT フィールドを持つフィールドが既定でグループ化されるかどうかを指定します。 このプロパティは、通貨量について自動的に<strong>非推奨</strong>に設定されます。 一意であるその他のフィールドについては、このプロパティを<strong>非推奨</strong>に設定する必要があります。</td>
</tr>
<tr class="odd">
<td>AnalysisUsage</td>
<td>キューブにおける EDT の役割を指定します。 この設定は、EDT を参照するすべてのテーブル フィールドに自動的に反映されます。 ただし、テーブル フィールドの設定を上書きできます。  次のオプションを使用できます。
<ul>
<li><strong>属性 </strong>- EDT を参照するフィールドは、分析コードの属性です。</li>
<li><strong>測定 </strong>- EDT を参照するフィールドは測定です。</li>
<li><strong>両方 </strong>- EDT を参照するフィールドは、分析コードの属性と測定の両方です。</li>
<li><strong>なし </strong>- EDT を参照するフィールドは、分析コードの属性でも測定でもありません。</li>
<li><strong>自動 </strong>- このオプションは、派生 EDT に適用されます。 親 EDT が使用される <strong>AnalysisUsage</strong> プロパティの値。</li>
</ul>
<strong>注記:</strong> 列挙型に基づいたデータ型は測定することができません。</td>
</tr>
<tr class="even">
<td>ArrayLength</td>
<td>このプロパティは、読み取り専用です。 既定値は <strong>1</strong> です。 配列要素を EDT に追加するには、<strong>配列要素</strong> ノードを右クリックし、<strong>新規配列要素</strong> をクリックします。 <strong>ArrayLength</strong> プロパティの値が増加してこの変更を反映します。</td>
</tr>
<tr class="odd">
<td>ButtonImage</td>
<td>ページのルックアップ ボタンに EDT が使用されるときに表示されるイメージを指定します。  次のオプションを使用できます。
<ul>
<li><strong>方向キー</strong></li>
<li><strong>メール</strong> - たとえば、<strong>電子メール</strong>タイプに対してこのオプションを選択できます。</li>
<li><strong>URL</strong> - たとえば、<strong>URL</strong> タイプに対してこのオプションを選択できます。</li>
<li><strong>ThreeDots</strong> (...)</li>
<li><strong>OpenFile</strong> - たとえば、<strong>FilenameOpen</strong> および <strong>FilenameSave</strong> タイプに対してこのオプションを選択できます。</li>
<li><strong>カレンダー</strong> - たとえば、日付タイプに対してこのオプションを選択できます。</li>
</ul>
既定値は <strong>矢印</strong> です。</td>
</tr>
<tr class="even">
<td>CollectionLabel</td>
<td>この EDT を持つフィールドの複数系の名前を表示するために使用するラベルを指定します。</td>
</tr>
<tr class="odd">
<td>ConfigurationKey</td>
<td>EDT の構成キーを指定します。</td>
</tr>
<tr class="even">
<td>CountryRegionCodes</td>
<td>メニューが適用されるか有効な国/地域のコードを指定します。 このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</td>
</tr>
<tr class="odd">
<td>DisplayLength</td>
<td>ページまたはレポートに表示されている文字の最大数を指定します。</td>
</tr>
<tr class="even">
<td>EnumType</td>
<td>列挙されたデータ型を指定します。 このプロパティは、<strong>列挙</strong>型の EDT に対して設定する必要があります。</td>
</tr>
<tr class="odd">
<td>拡張</td>
<td>EDT を別の EDT に基づいて作成するには、このプロパティを使用します。</td>
</tr>
<tr class="even">
<td>FormHelp</td>
<td>ページ上のフィールドから参照を実行するときに使用するページを指定します。</td>
</tr>
<tr class="odd">
<td>HelpText</td>
<td>EDT のヘルプ文字列を作成します。 型がページで使用されている場合は、ヘルプ文字列が表示されます。</td>
</tr>
<tr class="even">
<td>ID</td>
<td>このプロパティは、読み取り専用です。</td>
</tr>
<tr class="odd">
<td>ラベル</td>
<td>ページやレポートでタイプが使用される場合にタイプに使用されるラベルを指定します。</td>
</tr>
<tr class="even">
<td>モデル</td>
<td>テーブルがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルおよびクラスがあります。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="odd">
<td>氏名</td>
<td>タイプの名前を指定します。 この名前は、X++ の型を参照するために使用されます。</td>
</tr>
<tr class="even">
<td>PresenceClass</td>
<td><strong>PresenceInfo</strong> オブジェクトのインスタンスを返すために、<strong>PresenceMethod</strong> プロパティと同時に使用する X++ クラスを指定します。</td>
</tr>
<tr class="odd">
<td>PresenceIndicatorAllowed</td>
<td>EDT を参照するコントロールでプレゼンスを使用するかどうかを指定します。 既定値は <strong>はい</strong> です。</td>
</tr>
<tr class="even">
<td>PresenceMethod</td>
<td><strong>PresenceClass</strong> プロパティで指定されている X++ クラスについては、コントロール データ値を使用して呼び出される必要がある X++ 静的クラス メソッドな方法を指定します。 このメソッドは、プレゼンス インジケータが必要とするデータを含む <strong>PresenceInfo</strong> オブジェクトのインスタンスを返します。</td>
</tr>
<tr class="odd">
<td>ReferenceTable</td>
<td>この EDT で参照されているテーブルと、それが主キーであることを指定します。 つまり、このプロパティは、この EDT が参照する主キー テーブルを示します。</td>
</tr>
<tr class="even">
<td>スタイル</td>
<td>EDT の既定の外観を変更します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>コンボ ボックス</li>
<li>オプション ボタン</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="properties-that-are-available-for-only-some-base-data-types"></a>一部の基本データ型のみに使用できるプロパティ

次の表に別途記載がない限り、これらのプロパティはすべて **自動** に設定してください。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>プロパティが存在する型を入力</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>調整</td>
<td>文字列</td>
<td>固定長の文字列については、入力される文字がパディング スペースの左側または右側に格納されるかどうかを指定します。 <strong>左</strong> または <strong>右</strong> を選択できます。 既定値は <strong>左</strong> です。</td>
</tr>
<tr class="even">
<td>AllowNegative</td>
<td>IntegerInt64Real</td>
<td>フィールドが負の値を受け入れることができるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>AutoInsSeparator</td>
<td>実数</td>
<td>システムが小数桁の区切り記号を自動的に挿入する必要があるかどうかを指定します。 たとえば、<strong>2222</strong> を入力する場合、システムは自動で <strong>2222.00</strong> を表示します。</td>
</tr>
<tr class="even">
<td>ChangeCase</td>
<td>文字列</td>
<td>文字列コントロールに入力されたテキストを書式設定する方法を指定します。 たとえば、テキストは全大文字として書式設定され、またはタイトルの大文字化を使用できます。 <strong>注記:</strong> このプロパティは、エンタープライズ ポータルではサポートされていません。</td>
</tr>
<tr class="odd">
<td>DateDay</td>
<td>DateUtcDateTime</td>
<td>日の表示方法を指定します。</td>
</tr>
<tr class="even">
<td>DateFormat</td>
<td>DateUtcDateTime</td>
<td>日付のレイアウトを指定します。</td>
</tr>
<tr class="odd">
<td>DateMonth</td>
<td>DateUtcDateTime</td>
<td>月の表示方法を指定します。</td>
</tr>
<tr class="even">
<td>DateSeparator</td>
<td>DateUtcDateTime</td>
<td>年、月、日の間の区切り記号を指定します。</td>
</tr>
<tr class="odd">
<td>DateYear</td>
<td>DateUtcDateTime</td>
<td>年の表示方法を指定します。</td>
</tr>
<tr class="even">
<td>DecimalSeparator</td>
<td>実数</td>
<td>小数桁の区切り文字を指定します。 既定の設定 (<strong>自動</strong>) が使用されると、システムの設定で指定されている少数桁の区切り文字が使用されます。</td>
</tr>
<tr class="odd">
<td>DisplaceNegative</td>
<td>IntegerInt64Real</td>
<td>負の数を左に揃えるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>DisplayHeight</td>
<td>文字列</td>
<td>EDT がページに表示されているときに同時に表示する行数を指定します。</td>
</tr>
<tr class="odd">
<td>EnumType</td>
<td>列挙</td>
<td>EDT を作成するために使用される基本列挙を指定します。</td>
</tr>
<tr class="even">
<td>FormatMST</td>
<td>実数</td>
<td>値を書式設定する必要があるマスター通貨を指定します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>有</li>
<li>無</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>NoOfDecimals</td>
<td>実数</td>
<td>値がページまたはレポートに表示されているときの小数点以下桁数を指定します。</td>
</tr>
<tr class="even">
<td>RotateSign</td>
<td>IntegerInt64Real</td>
<td>数値の符号を逆にする場合にこのオプションを選択します。 つまり、マイナス記号 (-) をプラス記号 (+) に、またはプラス記号をマイナス記号に変更します。</td>
</tr>
<tr class="odd">
<td>ShowZero</td>
<td>IntegerInt64Real</td>
<td>値 0 (ゼロ) を持つのフィールドを空のフィールドとして表示するかどうかを指定します。 このタイプのフィールドにある 0 の値が null であるまたは意味をなさない場合は、このプロパティを<strong>いいえ</strong>に設定します。</td>
</tr>
<tr class="even">
<td>SignDisplay</td>
<td>IntegerInt64Real</td>
<td>負の値の符号を表示するかどうかと、数値の前後に符号を表示するかどうかを指定します。 通常、このプロパティは <strong>Auto</strong> に設定する必要があります。 ただし、<strong>DisplaceNegative</strong> プロパティを使用している場合は  <strong>None</strong> に設定できます。</td>
</tr>
<tr class="odd">
<td>StringSize</td>
<td>文字列</td>
<td>文字列の最大サイズを指定します。</td>
</tr>
<tr class="even">
<td>ThousandSeparator</td>
<td>実数</td>
<td>1000 ごとに区切るために使用する記号を指定します。</td>
</tr>
<tr class="odd">
<td>TimeFormat</td>
<td>TimeUtcDateTime</td>
<td>時間を書式設定する方法を指定します。</td>
</tr>
<tr class="even">
<td>TimeHours</td>
<td>TimeUtcDateTime</td>
<td>時間を含めるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>TimeMinute</td>
<td>TimeUtcDateTime</td>
<td>分を含めるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>TimeSeconds</td>
<td>TimeUtcDateTime</td>
<td>秒を含めるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>TimeSeparator</td>
<td>TimeUtcDateTime</td>
<td>時間に使用される区切り記号を指定します。</td>
</tr>
<tr class="even">
<td>TimezonePreference</td>
<td>UtcDateTime</td>
<td>協定世界時 (UTC) から値を変換するタイム ゾーンを指定します。</td>
</tr>
</tbody>
</table>

## <a name="perspective-properties"></a>分析視点のプロパティ
アプリケーション エクスプローラーの**データ ディクショナリ** ノードには、**分析視点**ノードがあります。 分析視点は、キューブのメジャーと分析コードを含むテーブルとビューの集合です。 次のテーブルに、各分析視点に設定できるプロパティを示します。 分析視点で使用可能なシステム プロパティの詳細については、「システムと共通プロパティ」セクションを参照してください。 分析視点に関連付けられているテーブルのプロパティの詳細については、「テーブルのプロパティ」および「テーブル フィールドのプロパティ」セクションを参照してください。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ConfigurationKey</td>
<td>分析視点に割り当てられるコンフィギュレーション キーを指定します。 コンフィギュレーション キーは、生成されたレポート モデルに含まれる分析視点の構成を決定します。</td>
</tr>
<tr class="even">
<td>HelpText</td>
<td>レポート モデルの分析視点の説明として使用する文字列を作成します。</td>
</tr>
<tr class="odd">
<td>ID</td>
<td>分析視点の識別子を指定します。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>レポート モデルの分析視点に表示される名前を指定します。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>分析視点があるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="even">
<td>SharedDimensionContainer</td>
<td>分析視点で項目を共有するかどうかを指定します。 このプロパティを <strong>はい</strong> に設定すると、分析視点内の品目はプロジェクト内のその他のすべての分析視点に追加され、分析視点のキューブは作成されません。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="odd">
<td>用途</td>
<td>分析視点の具体化オプションを指定します。  次のオプションを使用できます。
<ul>
<li><strong>AdHocReporting </strong>- 分析視点は、トランザクションの Semantic Model Definition Language (SMDL) モデルを生成するために使用されます。</li>
<li><strong>OLAP </strong> - 分析視点は、Microsoft SQL Server Analysis Services (SSAS) ビジネス インテリジェンス プロジェクトでキューブを生成するために使用されます。</li>
<li><strong>両方 </strong>- 分析視点は、SSAS Business Intelligence プロジェクトでトランザクション SDML モデルと、キューブの両方を生成するために使用されます。</li>
<li><strong>なし</strong> - 分析視点は実現されません。</li>
</ul>
既定値は <strong>なし</strong> です。</td>
</tr>
</tbody>
</table>

## <a name="table-properties"></a>表のプロパティ
このセクションでは、アプリケーション エクスプローラーのテーブル要素の**プロパティ**ウィンドウに表示されるプロパティについて説明します。 テーブル要素は、**データ ディクショナリ** &gt; **テーブル** にあります。

### <a name="table-properties"></a>表のプロパティ

次のテーブルは、アプリケーション エクスプローラーでのテーブル要素のプロパティを示しています。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>抽象</td>
<td>テーブルが継承をサポートするかどうかを指定します。 既定値は <strong>いいえ</strong> です。 値が<strong>はい</strong>に設定されている場合、テーブルが、<strong>update_recordset</strong> および <strong>select</strong> ステートメントのような X++ SQL ステートメントの直接ターゲットにはなりません。 <strong>注記:</strong> <strong>SupportInheritance</strong> プロパティが<strong>いいえ</strong>に設定されている場合、このプロパティは使用できません。</td>
</tr>
<tr class="even">
<td>AnalysisDimensionType</td>
<td><strong>IsLookup</strong> プロパティの設定に基づいて作成される分析コードのタイプを指定します。 <strong>IsLookup</strong> プロパティが<strong>はい</strong>に設定されている場合、次のオプションを使用できます。
<ul>
<li><strong>自動 </strong>- テーブルは事実データと分析コード データの両方を含めることができます。 BI ウィザードは、分析コード データを抽出し、分析コードと属性を作成します。 事実データが抽出され、対策が作成されます。 親テーブルから属性を持つ 1 つの子分析コードが作成されます。</li>
<li><strong>MasterInner</strong> - 内部 (完全) 結合を使用して、このテーブルと子テーブルの関係を作成します。 表およびテーブルの各レコードの組み合わせは、分析コードで生成されます。 親テーブルから属性を持つ 1 つの子分析コードが作成されます。</li>
<li><strong>MasterLeftOuter</strong> - 左外部結合を使用して、このテーブルと子テーブルの関係を作成します。 分析コードには、このテーブルの値に基づいて、空の場合もある追加の属性が設定されます。 親テーブルから属性を持つ 1 つの子分析コードが作成されます。</li>
<li><strong>トランザクション </strong>- テーブルは事実データ (測定) のみを生成するために使用されます。 テーブルにトランザクション データのみが含まれている場合に、このオプションを使用する必要があります。 テーブルから列挙型フィールドのみを含む 1 つの子分析コードが作成されます。</li>
</ul>
<strong>IsLookup</strong> プロパティが<strong>いいえ</strong>に設定されている場合、次のオプションを使用できます。
<ul>
<li><strong>自動 </strong>- テーブルは事実データと分析コード データの両方を含めることができます。 BI ウィザードは、分析コード データを抽出して分析コードと属性を作成します。事実に基づくデータはメジャーを作成するために抽出されます。 1 つの親と子の分析コードが作成されます。</li>
<li><strong>MasterInner</strong> - 適用できません。 このオプションは<strong>自動</strong>と同じです。</li>
<li><strong>MasterLeftOuter</strong> - 適用できません。 このオプションは<strong>自動</strong>と同じです。</li>
<li><strong>トランザクション </strong>- テーブルは事実データ (測定) のみを生成するために使用されます。 テーブルにトランザクション データのみが含まれている場合に、このオプションを使用する必要があります。 テーブルから列挙値のみを含む 1 つの子分析コードが作成されます。</li>
</ul></td>
</tr>
<tr class="odd">
<td>AnalysisIdentifier</td>
<td>SSAS キューブ内の分析コードの識別子として使用するフィールドを指定します。</td>
</tr>
<tr class="even">
<td>AOSAuthorization</td>
<td>ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定します。 このプロパティを <strong>なし</strong> に設定すると、承認チェックは実行されません。</td>
</tr>
<tr class="odd">
<td>CacheLookup</td>
<td>ルックアップ操作中に取得されたレコードをキャッシュする方法を指定します。 このプロパティは、別のテーブルを継承しないテーブルにのみ存在します。 継承ルート テーブルで、アプリケーション エクスプローラー <strong>プロパティ</strong> ウィンドウを使用して、このプロパティを <strong>EntireTable</strong> に設定することはできません。 継承ルート テーブルにこの値を割り当てるために、他の手法を使用しないでください。 たとえば、この値を割り当てる <strong>TreeNode</strong> クラスの <strong>AOTsetProperty</strong> メソッドを使用しないでください。</td>
</tr>
<tr class="even">
<td>ClusterIndex</td>
<td>クラスター インデックスを指定します。 このプロパティは、SQL の最適化にのみ使用されます。</td>
</tr>
<tr class="odd">
<td>ConfigurationKey</td>
<td>テーブルのコンフィギュレーション キーを指定します。 コンフィギュレーション キーにより、システム管理者はアプリケーションの特定の部分を有効または無効にすることができます。</td>
</tr>
<tr class="even">
<td>CountryRegionCodes</td>
<td>テーブルが適用されるか有効な国/地域のコードを指定します。 このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアント フレームワークは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</td>
</tr>
<tr class="odd">
<td>CountryRegionContextField</td>
<td>国/地域のコンテキストを識別するために使用されるフィールドを指定します。 このプロパティは、<strong>CountryRegionCodes</strong> プロパティに関連しています。</td>
</tr>
<tr class="even">
<td>CreatedBy</td>
<td>システムがテーブルのレコードの <strong>CreatedBy</strong> フィールドを管理しているかどうかを指定します。 このフィールドには、レコードの作成者に関する情報が含まれます。</td>
</tr>
<tr class="odd">
<td>CreatedDateTime</td>
<td>システムがテーブルのレコードの <strong>CreationDate</strong> および <strong>CreationTime</strong> フィールドを管理しているかどうかを指定します。 このフィールドには、レコードが最後に作成された日付が含まれます。</td>
</tr>
<tr class="even">
<td>CreatedTransactionId</td>
<td>システムがテーブルのレコードの <strong>CreatedTransactionId</strong> フィールドを管理しているかどうかを指定します。 このフィールドにはレコードを作成した取引に関する情報が含まれます。</td>
</tr>
<tr class="odd">
<td>CreateRecIdIndex</td>
<td><strong>レコード ID</strong> フィールドのインデックスが作成されるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>DeveloperDocumentation</td>
<td>テーブルの目的を説明し、プログラムでどのように使用されているかを説明します。 通常、説明は 5 つ以下の構文で構成され、単一の段落として書かれます。</td>
</tr>
<tr class="odd">
<td>EntityRelationshipType</td>
<td>共通エンティティ リレーションシップ (ER) データ モデルの表記法に従ってテーブルを分類します。 テーブルは、エンティティまたはリレーションシップとして分類されます。 エンティティはオブジェクトを表すのに対し、関係は 2 つのオブジェクト間の関連を表します。</td>
</tr>
<tr class="even">
<td>拡張</td>
<td>特定のテーブルからの派生テーブル <strong>SupportInheritance</strong> プロパティが <strong>Yes</strong> に設定されている場合、値は <strong>null</strong> です。</td>
</tr>
<tr class="odd">
<td>FormRef</td>
<td>テーブルが参照されているときに発生する表示メニュー項目を指定します。 表示メニュー項目は、ページに関連付けられます。 レポートのプライマリ インデックス フィールドを使用するとき、このページはレポート内のリンクとして使用できます。 <strong>PrimaryIndex</strong> プロパティ使用して、プライマリ インデックスを指定します。 このプロパティを空白のままにすると、システムではでテーブルと同じ名前のページを表示しようとします。</td>
</tr>
<tr class="even">
<td>ID</td>
<td>システムが生成したテーブル ID。</td>
</tr>
<tr class="odd">
<td>IsLookup</td>
<td>レポート モデルについては、テーブルの情報が、レポート モデルが生成されるときに参照する他のテーブルに組み込まれているかどうかを指定するため、このプロパティを使用します。 オンライン分析処理 (OLAP) キューブについては、このプロパティを使用して、連結分析コードまたは異なる分析コードを生成するかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>はい </strong>- テーブルの属性は親分析コード (スター スキーマ) に連結される必要があります。</li>
<li><strong>いいえ</strong> - テーブル (スノーフレーク スキーマ) に対して個別の分析コードを生成します。</li>
</ul></td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>テーブルのラベルを指定します。</td>
</tr>
<tr class="odd">
<td>ListPageRef</td>
<td>このレコードの種類の一覧を表示できるページをポイントする表示メニュー項目を指定します。</td>
</tr>
<tr class="even">
<td>モデル</td>
<td>テーブルがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルおよびクラスがあります。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="odd">
<td>ModifiedBy</td>
<td>システムがテーブルのレコードの <strong>ModifiedBy</strong> フィールドを管理しているかどうかを指定します。 このフィールドには、レコードを最後に変更した人に関する情報が含まれます。 </td>
</tr>
<tr class="even">
<td>ModifiedDateTime</td>
<td>システムがテーブルのレコードの <strong>ModifiedDate</strong> フィールドを管理しているかどうかを指定します。 このフィールドには、レコードが最後に変更された日付が含まれます。</td>
</tr>
<tr class="odd">
<td>ModifiedTime</td>
<td>システムがテーブルのレコードの <strong>ModifiedDateTime</strong> フィールドを管理しているかどうかを指定します。 このフィールドには、レコードが最後に変更された日時が含まれます。</td>
</tr>
<tr class="even">
<td>氏名</td>
<td>テーブル名を指定します。</td>
</tr>
<tr class="odd">
<td>OccEnabled</td>
<td>テーブルでオプティミスティック同時実行モードを有効にするかどうかを指定します。 このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。 データは、実際の更新の実行時にのみロックされます。</td>
</tr>
<tr class="even">
<td>PreviewPartRef</td>
<td>拡張プレビューで使用される情報パーツまたはフォーム パーツを指定します。 情報パーツは指定したクエリからデータ フィールドのコレクションを表示しています。 メタデータを使用してデータの表示方法を説明します。 フォーム パーツは、ページへのポインターを表します。</td>
</tr>
<tr class="odd">
<td>PrimaryIndex</td>
<td>プライマリ インデックスを指定します。 固有のインデックスのみ選択することができます。 このプロパティは、データベースの最適化と、キャッシュ キーとして使用するユニークなインデックスを示すために使用されます。 プライマリ インデックスを指定しない場合、最下位の ID の固有のインデックスはキャッシュ キーとして使用されます。</td>
</tr>
<tr class="even">
<td>ReplacementKey</td>
<td>一部のページ コントロール内のデータの識別子として表示するフィールドを指定します。</td>
</tr>
<tr class="odd">
<td>ReportRef</td>
<td>テーブルが参照されているときに発生する出力メニュー項目を指定します。 出力メニュー項目はレポートに関連付けられています。 レポートのプライマリ インデックス フィールドを使用するとき、このレポートはレポート内のリンクとして使用できます。 <strong>PrimaryIndex</strong> プロパティ使用して、プライマリ インデックスを指定します。</td>
</tr>
<tr class="even">
<td>SaveDataPerCompany</td>
<td>現在の会社のデータが保存されるかどうかを指定します。 プロパティを<strong>いいえ</strong>に設定すると、データは会社識別子 (DataAreaId) なしで保存されます。 <strong>注記: </strong>テーブルの <strong>SaveDataPerCompany</strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルをデータ ソースとして使用するページ デザインの <strong>SetCompany</strong> プロパティも<strong>はい</strong>に設定する必要があります。 <strong>ヒント:</strong> ステータス行は、会社の略称を表示します。 略称をダブルクリックして、会社を変更できるダイアログ ボックスを開きます。</td>
</tr>
<tr class="odd">
<td>SaveDataPerPartition</td>
<td>テーブルに<strong>パーティション</strong>という名前のシステム フィールドがあるかどうかを示す値。 このプロパティは、読み取り専用になっています。 テーブルに<strong>パーティション</strong> フィールドがない場合、各レコードに 1 つのパーティションに割り当てられます。 各レコードは、他のパーティションのコンテキストで実行されるデータ アクセス操作から隠されます。</td>
</tr>
<tr class="even">
<td>SearchLinkRefName</td>
<td>エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目の名前を指定します。 <strong>SearchLinkRefType</strong> プロパティが <strong>URL</strong> に設定されている場合、テーブル データが表示されている Web パーツ ページにリンクするメニュー項目を選択します。 Web パーツ ページのフォームおよびレポートは、データを表示できます。</td>
</tr>
<tr class="odd">
<td>SearchLinkRefType</td>
<td>エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目のタイプを指定します。</td>
</tr>
<tr class="even">
<td>SingularLabel</td>
<td>テーブルに格納される品目の単数形の名前を表示するために、レポート モデルまたはキューブで使用されるラベルを指定します。</td>
</tr>
<tr class="odd">
<td>SupportInheritance</td>
<td>このプロパティを<strong>はい</strong>に設定すると、<strong>Extends</strong> および <strong>Abstract</strong> などの、その他の継承関連のプロパティの値を設定できます。 <strong>注意:</strong> このプロパティを<strong>はい</strong>に設定した場合、テーブル上のフィールドはすべて削除され、再度作成する必要があります。</td>
</tr>
<tr class="even">
<td>SystemTable</td>
<td>テーブルをシステム テーブルとして表示するかどうかを示します。 システム テーブルとして表示されるテーブルは、エクスポートおよびインポート中にフィルター処理できます。 システム テーブルは、サインイン時に常に同期されます。 したがって、このプロパティは、サインインするとすぐに使用するテーブルに便利です。</td>
</tr>
<tr class="odd">
<td>TableContents</td>
<td>顧客間でセットアップ/パラメーター データを再利用する方法を指定します。  次のオプションを使用できます。
<ul>
<li><strong>指定なし</strong> - ほとんどのテーブルにこのオプションを使用します。</li>
<li><strong>既定のデータ</strong> - このオプションは、郵便番号、単位、時間間隔など、顧客に依存しないデータに使用します。</li>
<li><strong>基本データ </strong>- カレンダー、グループ、およびパラメータなどの顧客に依存するデータ用のこのオプションを使用します。</li>
<li><strong>既定 + 基本データ</strong> - このオプションは、ローカル知覚が異なるデータに対して使用します。 たとえば、勘定科目表は、ドイツでは顧客に依存していませんが、他のほとんどの場所では顧客に依存しています。</li>
</ul></td>
</tr>
<tr class="even">
<td>TableGroup</td>
<td>テーブルが属するグループを指定します。 テーブル グループは、テーブルに含まれるデータのタイプに応じてテーブルを分類する方法を提供します。 テーブルをデータ ソースとして使用することにより、ページ上のテーブルからデータを更新または削除するときにシステムがユーザーに確認を求めるかどうか定義するためにテーブル グループを使用することができます。 データをエクスポートするとき、テーブル グループを使用してレコードをフィルターすることができます。</td>
</tr>
<tr class="odd">
<td>TableType</td>
<td>このプロパティは、Microsoft Dynamics AX 2009 にある<strong>一時的な</strong>プロパティを置き換えます。</td>
</tr>
<tr class="even">
<td>TitleField1、TitleField2</td>
<td>このプロパティは、次の方法で実現できます。
<ul>
<li>フォーム キャプションにテーブル フィールド データを追加します。</li>
<li>参照ページで追加のフィールドを表示します。 <strong>TitleField1</strong> プロパティは、ページ上のフィールドでルックアップ リストを有効化するときにも使用されます。 <strong>TitleField1</strong> および <strong>TitleField2</strong> プロパティに指定するフィールドは、キー値とマージできます。</li>
<li>ツールヒントにフィールドの情報を表示します。</li>
</ul></td>
</tr>
<tr class="odd">
<td>TypicalRowCount</td>
<td>テーブル内に通常表示されるレコード数を指定します。 <strong>AnalysisSelection</strong> プロパティが設定されていない場合、このプロパティにより SSRS のレポート ビルダーを使用してレコードを選択する方法が決定されます。 このプロパティの設定は、ドロップダウン リスト、リスト ボックス、フィルタリングされたリスト ボックスを使用してテーブル レコードを選択するかどうかに影響します。</td>
</tr>
<tr class="even">
<td>ValidTimeStateFieldType</td>
<td>期間内のデータを追跡するときにシステムが使用する日付/時刻フィールドのタイプを指定します。</td>
</tr>
<tr class="odd">
<td>表示</td>
<td>テーブルがページやレポート内のデータ ソースとして使用される場合のアクセス権を指定します。 テーブルをページ内のデータ ソースとして使用する場合、ページのアクセス権は、テーブルに対して定義されているアクセス権を超えることはできません。</td>
</tr>
</tbody>
</table>

### <a name="tables-and-report-models"></a>テーブルおよびレポート モデル

次のプロパティは、レポートに情報を追加するために使用されるレポート モデルに関連しています。

-   AnalysisSelection
-   AnalysisVisibility
-   IsLookup
-   SingularLabel
-   TypicalRowCount

## <a name="table-field-properties"></a>テーブル フィールド プロパティ
次のプロパティは、レポートに情報を追加するために使用されるレポート モデルに関連しています。

-   AnalysisDefaultTotal
-   AnalysisLabel
-   AnalysisTotaling
-   AnalysisUsage
-   AnalysisVisibility
-   CurrencyCode
-   CurrencyCodeField
-   CurrencyCodeTable

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>調整</td>
<td>文字列フィールドがデータベースに格納されるときに左揃えか右揃えかを指定します。 たとえば、11 文字列 &quot;hello world&quot; が <strong>40</strong> の<strong>StringSize</strong> 設定を持つ右揃えのフィールドに格納される場合、29 空白文字が接頭語として格納されます。 <strong>注記:</strong> <strong>調整</strong> 設定は、<strong>&gt;</strong>、<strong>&lt;</strong>、<strong>&gt;=</strong>、 <strong>&lt;=</strong> リレーショナル演算子を使用してテーブルの値を検索したときの検索結果に影響します。 <strong>==</strong> 演算子を使用する場合、検索結果に影響を与えることはありません。 <strong>調整</strong> 設定は、<strong>StringSize</strong> プロパティが <strong>(Memo)</strong> に設定されている場合無視されます。</td>
</tr>
<tr class="even">
<td>AliasFor</td>
<td>フィールドがエイリアスとなるテーブル フィールドを指定します。</td>
</tr>
<tr class="odd">
<td>AllowEdit</td>
<td>ユーザーがページの既存のレコードのデータを変更できるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>AllowEditOnCreate</td>
<td>新しいレコードが作成されるときにユーザーがフィールドにデータを入力できるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>AnalysisDefaultTotal</td>
<td>レポート モデルについては、このプロパティを使用して、テーブルの自動合計が SSRS およびレポート モデルを使用して構築されるレポートに表示されるときに、フィールド データを集計する方法を指定します。 既定値は<strong>いいえ</strong>で、フィールドが自動的に合計として表示されないことを示します。 OLAP キューブで、測定の集計関数を指定するため、このプロパティを使用します。 <strong>AnalysisUsage</strong> プロパティが<strong>測定</strong>に設定されている場合、このプロパティを使用します。  次のオプションを使用できます。
<ul>
<li><strong>合計 </strong>- セット内のすべての値の合計を返します。</li>
<li><strong>カウント</strong> - セット内の null 以外の品目の数を返します。</li>
<li><strong>CountDistinct</strong> - セット内の特徴的な null 以外の品目の数を返します。</li>
<li><strong>最小</strong> - セット内の最小値を返します。</li>
<li><strong>最大</strong> - セット内の最大値を返します。</li>
<li><strong>なし</strong> - 集計関数は適用されません。</li>
<li><strong>自動 </strong>- このオプションは、派生 EDT に適用されます。 親 EDT が使用される <strong>AnalysisUsage</strong> プロパティの値。</li>
</ul></td>
</tr>
<tr class="even">
<td>AnalysisLabel</td>
<td>テーブル フィールドの SSAS キューブ内のキャプションとして使用するラベルを指定します。 ラベルは、分析コード属性または測定のいずれかに適用されます。 このプロパティは、次のいずれかの条件に該当する場合に使用します。
<ul>
<li><strong>ラベル</strong> プロパティが定義されていません。</li>
<li><strong>ラベル</strong> プロパティは、分析コード属性のキャプションまたは SSAS キューブのメジャーとして機能しません。</li>
</ul></td>
</tr>
<tr class="odd">
<td>AnalysisUsage</td>
<td>キューブにおけるフィールドの役割を指定します。 次のオプションを使用できます。
<ul>
<li><strong>属性 </strong>- このフィールドは、分析コードの属性です。</li>
<li><strong>測定</strong> - このフィールドは、測定です。</li>
<li><strong>両方 </strong>- フィールドは、分析コードの属性と測定の両方です。</li>
<li><strong>なし </strong>- フィールドは、分析コードの属性でも測定でもありません。</li>
<li><strong>自動 </strong>- フィールドが基づいている EDT または列挙の <strong>AnalysisUsage</strong> プロパティの値を使用する必要があります。</li>
</ul></td>
</tr>
<tr class="even">
<td>ConfigurationKey</td>
<td>フィールドのコンフィギュレーション キーを設定します。</td>
</tr>
<tr class="odd">
<td>CountryRegionCodes</td>
<td>テーブル フィールドが適用されるか有効な国/地域のコードを指定します。 このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアント フレームワークおよびアプリケーションは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</td>
</tr>
<tr class="even">
<td>CountryRegionContextField</td>
<td>国/地域のコンテキストを識別するために使用されるフィールドを指定します。 <strong>CountryRegionCodes</strong> プロパティの説明を参照してください。</td>
</tr>
<tr class="odd">
<td>ExtendedDataType</td>
<td>このフィールドに使用する EDT を指定します。</td>
</tr>
<tr class="even">
<td>GroupPrompt</td>
<td>グループに表示されるときにフィールドに使用されるラベルを指定します。 <strong>ヒント:</strong> このプロパティを使用して、フィールド ラベルがフィールド グループのラベルに表示されるテキストを繰り返さないようにすることができます。 たとえば、ページのフィールド グループに<strong>顧客</strong>のラベルが付いている場合、フィールド グループに含まれているフィールドの <strong>GroupPrompt</strong> プロパティで、このテキストを含めないでください。</td>
</tr>
<tr class="odd">
<td>HelpText</td>
<td>フィールドのヘルプ文字列を指定します。 フィールドがページで使用されている場合は、ヘルプ文字列が表示されます。</td>
</tr>
<tr class="even">
<td>ID</td>
<td>システムが生成したフィールド ID。</td>
</tr>
<tr class="odd">
<td>IgnoreEDTRelation</td>
<td>このプロパティは、EDT 関係の移行中に使用されます。 EDT ノードからテーブル ノードにリレーションを移行するときは、任意のテーブル フィールドの無効なリレーションを省略できます。 無効なリレーションをスキップするには、このプロパティを <strong>はい</strong> に設定します。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>フィールドのラベルを指定します。 このラベルはページとレポートに表示されます。 このテーブルの前のプロパティ <strong>AnalysisLabel</strong> の説明も参照してください。</td>
</tr>
<tr class="odd">
<td>必須</td>
<td>ユーザーがページ上のフィールドにデータを追加する必要があるかどうかを指定します。 このプロパティを<strong>はい</strong>を設定し、各データ型の既定または初期化値がデータベースへの持続として許容できないことを示します。 次のリストは、ページの必須フィールドに使用できないいくつかの既定値を示しています。
<ul>
<li>空は str (文字列) フィールドには受け入れられません。</li>
<li>date および utcdatetime などの日付/時刻フィールドでは、最小日時は受け入れられません。</li>
<li>int、real、enum などの数値フィールドでは、0 (ゼロ) の値は受け入れられません。</li>
</ul>
Finance and Operations は、ほとんどの SQL データベース製品に標準的な <strong>null</strong> 値に対するセマンティクスをサポートしません。 フィールドはデータベースで Null にはなりません。 したがって、<strong>Mandatory</strong> プロパティは、<strong>null</strong> 値の概念とは関係ありません。 <strong>注意:</strong> 必須テーブル フィールドは、<strong>EnumType</strong> プロパティを列挙に設定できます。 整数値 <strong>0</strong> を持つ品目を含む列挙型としてフィールドを定義することがあります。 この場合、<strong>0</strong> はページで選択可能な項目ではありません。 フォーム システムは自動的に、<strong>必須</strong> プロパティの設定を強制する <strong>validateWrite</strong> メソッドを呼び出します。 ただし、<strong>必須</strong>プロパティはテーブル フィールドの値を挿入または更新する直接の X++ SQL の動作には影響を与えません。 直接の X++ SQL では、テーブル バッファ変数に <strong>validateWrite</strong> メソッドへの呼び出しを含めることができます。 バッファ変数は、<strong>xRecord</strong> クラスからメソッドを継承します。</td>
</tr>
<tr class="even">
<td>MinReadAccess</td>
<td>自動承認機能のモードを指定します。 自動認証には代理外部キーとルックアップの 2 つの操作モードがあります。 照会内の表に代理外部キー許可のタグが付けられていて、ユーザーがその表にアクセスすることはできませんが、明示的に拒否されていない場合、表へのアクセスが許可されます。 ただし、すべてのフィールドが表示されるわけではありません。 可視性は次の規則によって決まります。
<ul>
<li><strong>MinReadAccess</strong> を<strong>いいえ</strong>に設定する場合、フィールドへのアクセスは許可されません。</li>
<li><strong>MinReadAccess</strong> が<strong>はい</strong>に設定されている場合、フィールドへのビュー アクセスは許可されません。</li>
<li>それ以外の場合、フィールドがナチュラル キー自動識別グループの一部である場合、タイトル フィールドである場合、またはシステム フィールドである場合は、表示アクセスが許可されます。</li>
</ul>
クエリ内のテーブルがルックアップ承認用にタグされた場合、アクセスが、次のルールによって決定されます。
<ul>
<li><strong>MinReadAccess</strong> を<strong>いいえ</strong>に設定する場合、フィールドへのアクセスは許可されません。</li>
<li>それ以外の場合、表示アクセスは、このフィールドに許可されます。</li>
</ul></td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>テーブル フィールドがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="even">
<td>氏名</td>
<td>フィールドの名前を指定します。</td>
</tr>
<tr class="odd">
<td>関係コンテキスト</td>
<td>特定のテーブル関係へのフィールドのマッピングを指定します。 このプロパティは通常、通貨コードまたは数量に関連するデータをモデル化するために測定単位シナリオで使用されます。 フィールドに関連付けられた関係を使用して、通貨コードまたは数量の参照を表示することができます。 既定値はありません。</td>
</tr>
<tr class="even">
<td>SaveContents</td>
<td>フィールド データがデータベースに保存されるか、仮想フィールド データとして扱われるかを指定します。 仮想フィールドが表示されるとき、そのフィールドのデータが実行時に計算されます。 このデータはデータベースに物理的な表現はありません。 <strong>ヒント:</strong> 仮想のフィールドの代わりに、表示メソッドと編集メソッドを使用できます。</td>
</tr>
<tr class="odd">
<td>StringSize</td>
<td>フィールドの長さを文字数で設定します。 最大フィールドの長さは、データベースによって異なります。 <strong>(メモ)</strong> の値は、フィールドの長さが無制限であることを示します。</td>
</tr>
<tr class="even">
<td>種類</td>
<td>フィールドの基本データ型を指定します。</td>
</tr>
<tr class="odd">
<td>表示</td>
<td>ユーザー インターフェイスにフィールドを表示するかどうかを指定します。</td>
</tr>
</tbody>
</table>

## <a name="table-index-properties"></a>テーブル インデックスのプロパティ
次のテーブルに、テーブルのインデックスで使用可能なプロパティを示します。

| プロパティ              | 説明                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowDuplicates       | このプロパティを**はい**に設定すると、インデックスが非一意になる可能があります。 1 つ以上の固有のインデックスを作成しない場合、固有のインデックスは最初のインデックスと RecId を組み合わせて作成されます。                                                                                                                                                                                                                                                     |
| AlternateKey          | このインデックスが代替キーの一部かどうかを指定します。 インデックス フィールドは、すべてのレコードで一意の値を持つ必要があります。                                                                                                                                                                                                                                                                                                                                                   |
| ConfigurationKey      | コンフィギュレーション キーを設定します。 コンフィギュレーション キーによって無効にされているインデックス フィールドはインデックスから自動的に削除されます。                                                                                                                                                                                                                                                                                                                                     |
| 有効               | このプロパティを使用すると、インデックスを無効にすることができます。                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID                    | オブジェクトの社内 ID。                                                                                                                                                                                                                                                                                                                                                                                                                              |
| モデル                 | テーブル インデックスがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。                                                                                                                                                                   |
| 氏名                  | インデックス名を指定します。                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| UniqueAcrossCompanies | このプロパティは、Microsoft 内部でのみ使用されます。 使用可能な値は、**はい** および **いいえ** です。 既定値は **いいえ** です。 **AllowDuplicates** プロパティが **No** に設定されている場合、値は無視されます。 ただし、**AllowDuplicates** が**はい**に設定されると、**UniqueAcrossCompanies** の**はい**の値は一部の会社間のクエリのパフォーマンスを向上させることができます。 パフォーマンスの向上が、データのキャッシングを変更することによって得られます。 |
| ValidTimeStateKey     | このインデックス キーが親テーブルと有効時間状態の関係を決定するために使用されるかどうかを指定します。 既定値は **いいえ** です。 **ヒント:** このプロパティを有効にするには **AllowDuplicates** プロパティを**いいえ**、**AlternateKey** プロパティを**はい**に設定する必要があります。                                                                                                                                                                                   |
| ValidTimeStateMode    | 2 つの有効日レコードの間にギャップが許可されるかどうかを指定します。 既定値は **NoGap** です。 **ヒント:** このプロパティを有効にするには、**AllowDuplicates** プロパティを**いいえ**に、**AlternateKey** プロパティを**はい**に、 **ValidTimeStateKey** プロパティを**はい**に設定する必要があります。                                                                                                                                                                        |

**注記:** ページは最初のインデックスで並べ替えられます。

## <a name="table-relation-properties"></a>テーブル関係プロパティ
### <a name="list-of-properties"></a>プロパティのリスト

次のテーブルは、アプリケーション エクスプローラーでのテーブル リレーションのプロパティを示しています。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>基数</td>
<td>参照テーブルの各主キー値が現在のテーブルの外部キー列で発生しなければならない回数。 たとえば、<strong>OneMore</strong> 値は、1 以上で、0 ではないことを意味します。 この値は、すべての親キー値が子テーブルの外部キー列に最低 1 回現れなければならないことを示します。 ビジネス ルールが、販売された少なくとも 1 つの品目に関連する親 SalesTable テーブルのすべてのレコードを必要とする場合、SalesLine テーブルのリレーション ノードは、<strong>OneMore</strong> 値を使用します。 現在、<strong>基数</strong>プロパティは使用されていません。 ただし、今後のリリースはこのプロパティおよび <strong>RelatedTableCardinality</strong> プロパティを使用する可能性があります。</td>
</tr>
<tr class="even">
<td>CreateNavigationPropertyMethods</td>
<td><strong>はい</strong>の値は、各外部キー リレーション ノードのテーブル バッファ クラスでナビゲーション メソッドを生成するシステムに指示します。</td>
</tr>
<tr class="odd">
<td>EDTRelation</td>
<td>値が<strong>はい</strong>に設定されている場合、ソフトウェア ツールが古い EDT 関係からこの関係を現在の場所に移行するために使用されました。</td>
</tr>
<tr class="even">
<td>EntityRelationshipRole</td>
<td>このプロパティは、テーブルに定義された関係のセマンティクスを明確にするために使用されます。 ロール名は、名詞または名詞句のいずれかにする必要があります。 ロール名は、関連するオブジェクトに関連するテーブルの役割を示す必要があります。 あるいは、ロール名は、テーブルが関係内で果たす役割を示す現在の時制動詞で始まる短い語句でなければなりません。 ロール名は、関係があいまいではないときは必要ありません。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>このリレーションが含まれるモデル。</td>
</tr>
<tr class="even">
<td>氏名</td>
<td>関係のために選択した内容を示す名前。</td>
</tr>
<tr class="odd">
<td>NavigationPropertyMethodNameOverride</td>
<td>ナビゲーション メソッドの名前を指定します。 値が指定されていない場合、ナビゲーション メソッドは <strong>RelatedTableRole</strong> プロパティからの値を使用します。</td>
</tr>
<tr class="even">
<td>RelatedTableCardinality</td>
<td>現在のテーブルの一部またはすべてのレコードにおいて、現在のテーブルの外部キー フィールドの値を <strong>null</strong> にできるかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>ZeroOne</strong> 0 または 1 を意味します。 この値は、子レコードの外部キー フィールドが <strong>ヌル</strong> になる可能性があることを示します。</li>
<li><strong>ExactlyOne</strong> は、任意の子レコードで外部キーフィールドを <strong>null</strong> にできないことを示します。</li>
</ul></td>
</tr>
<tr class="odd">
<td>RelatedTableRole</td>
<td>この関係に参照される親テーブルの目的を説明するテキスト値を入力します。 指定された親テーブルを参照する 1 つリレーションのみがテーブルに存在するときは、親テーブルの名前を使用することができます。 場合によっては、テーブルに、指定された参照先の親テーブルとの関係が複数あります。 この場合、<strong>RelatedTableRole</strong> プロパティの値は、リレーションの目的を同じ親テーブルに対する他のリレーションと区別するために、リレーションについて十分説明する必要があります。 このプロパティ値は、アプリケーション エクスプローラー クエリでのデータ ソース リレーションの <strong>JoinRelation</strong> プロパティ値として使用できます。 標準的に、この使用方法は正常でない部分が少なくなるためお勧めです。 このプロパティは、<strong>UseDefaultRoleNames</strong> プロパティと連携します。</td>
</tr>
<tr class="even">
<td>RelationshipType</td>
<td>2 つのテーブル間の微妙な関係を示す値を選択します。 たとえば、<strong>構成</strong>値は、特定の親レコードに関連していない限り、子レコードが意味深く存在できないことを示します。 親建物テーブルのレコードを参照しない限り、フロア テーブルの 4 階のレコードは存在できません。 <strong>注記:</strong> DeleteActions は、このプロパティの設定と互換性があることが必要です。 構成の関係で、DeleteActions はカスケード動作の削除を含む必要があります。 現在、<strong>RelationshipType</strong> プロパティは使用されていません。 ただし、将来のリリースはこのプロパティを使用する可能性があります。</td>
</tr>
<tr class="odd">
<td>役割</td>
<td>関係の意味やロールを説明する名前を指定します。 たとえば、部門テーブルへの 1 つの関係は、従業員が現在所属する部門を追跡することができます。 別の関係では、従業員が移動を要求した部門を追跡できます。 これらの関係は両方とも部門テーブルとの関係ではありますが、さまざまな異なる役割を果たします。 このプロパティの値として、アンダースコア (_) の文字を使用し、子テーブルと親テーブルの名前を結合することをお勧めします。 たとえば、<strong>SalesTable_SalesLine</strong> を入力します。 このプロパティは、<strong>UseDefaultRoleNames</strong> プロパティと連携します。</td>
</tr>
<tr class="even">
<td>テーブル</td>
<td>リレーションが参照するテーブル。</td>
</tr>
<tr class="odd">
<td>UseDefaultRoleNames</td>
<td><strong>はい</strong>の値は、システムが<strong>ロール</strong>および <strong>RelatedTableRole</strong> プロパティの規定値を生成する必要があることを示します。 プロパティが<strong>はい</strong>に設定されている場合でも、<strong>ロール</strong>および <strong>RelatedTableRole</strong> に対して生成された値は、<strong>プロパティ</strong> ウィンドウに表示されません。 また、<strong>TreeNode</strong> クラスは、生成値を使用できません。 ただし、<strong>DictRelation</strong> リフレクション クラスでは生成された値が使用されます。</td>
</tr>
<tr class="even">
<td>検証</td>
<td><strong>はい</strong>の値は、ページがレコードを子テーブルに挿入するときに、関連するレコードが参照されている親テーブルに存在しないかぎり、挿入が拒否されたことを示します。 また、ページが親テーブルからレコードを削除すると、削除は拒否されるか、子テーブルで関連するレコードに重ねて表示されます。 <strong>RelationshipType</strong> プロパティが <strong>リンク</strong> に設定されているとき、値を <strong>いいえ</strong> に設定します。 いくつかのアップグレード シナリオなどの特別な一時的なケースでは、値を <strong>いいえ</strong> に設定する可能性もあります。 値の設定を <strong>はい</strong> に戻したとき、値が <strong>いいえ</strong> の間に挿入または削除されたレコードについては検証は実行されません。 <strong>注意:</strong> <strong>Validate</strong> プロパティの<strong>はい</strong>の値は、直接 X++ SQL データ操作が親レコードを削除したり、外部キーデータの整合性に違反する子レコードを挿入したりすることを防ぎません。</td>
</tr>
</tbody>
</table>

**注記:** **SaveDataPerCompany** プロパティが両方のテーブルに対して、**はい**に設定されている場合、システムは**DataAreaId** フィールドを各リレーションシップに追加します。

### <a name="relatedtablerole-and-query-joinrelation"></a>RelatedTableRole およびクエリ JoinRelation

このセクションでは、**RelatedTableRole** プロパティを使用して新しいクエリの作成を簡略化する方法について説明します。 テーブル関係上の **RelatedTableRole** プロパティの明示的な値を入力すると、その値を使用し、アプリケーション エクスプローラーにある**クエリ** &gt; **MyQuery** ノードのデータ ソースの関係の **JoinRelation** プロパティを設定できます。 この方法を使用して、1 つの場所に結合のフィールドを指定できます。 結合フィールドを変更した場合は、一箇所だけ結合を更新する必要があります。 **JoinRelation** プロパティの値を設定する前に、**フィールド**および **RelatedField** プロパティの値を削除する必要があります。

### <a name="createnavigationpropertymethods-and-relatedtablerole"></a>CreateNavigationPropertyMethods および RelatedTableRole

テーブル リレーションで、**CreateNavigationPropertyMethods** プロパティを **はい** に設定すると、テーブル バッファ クラスのナビゲーション メソッドが生成されます。 ナビゲーション メソッドは、外部キーのリレーションシップを使用してテーブル バッファの 2 つのインスタンスをリンクします。 **UnitOfWork** クラスは、このナビゲーション リンクが使用されている 1 つの領域です。 ナビゲーション メソッドの名前は、テーブル関連の **RelatedTableRole** プロパティの値からコピーされます。 この動作は、**RelatedTableRole** 値が **Properties** ウィンドウに明示的に設定され、**UseDefaultRoleNames** プロパティが **Yes** に設定されているため、**RelatedTableRole** 値を生成するときに使用されます。 プロパティ値は、子 CustTable バッファで次のナビゲーション メソッドを生成します。 ほとんど直接的に、ナビゲーション メソッドの名前は **RelatedTableRole** プロパティの値からをコピーされます。

    public final CustBankAccount BankAccounts([CustBankAccount relatedTable])

#### <a name="navigationpropertymethodnameoverride-property"></a>NavigationPropertyMethodNameOverride プロパティ

次のリストでは、システムがテーブル バッファ クラスでナビゲーション メソッドに対して生成する名前を上書きする必要がある場合について説明します。

-   テーブル クラスにはすでに **RelatedTableRole** プロパティの値と一致するメソッド名があります。
-   **RelatedTableRole** プロパティの値がメソッド名に使用できる最大長を超えています。

そのような場合、ナビゲーション メソッドの有効な名前を選択し、テーブル リレーションの **NavigationPropertyMethodNameOverride** プロパティの値としてその名前を割り当てる必要があります。

## <a name="understanding-the-relationshiptype-enumeration"></a>RelationshipType の列挙型を理解する
テーブル リレーションの下にノードを追加するとき、新しいリレーションの **RelationshipType** プロパティの値を設定できます。 **RelationshipType** プロパティの可能な値のリストは、**RelationshipType** 列挙型の要素のリストです。 このセクションでは、**RelationshipType** 列挙の各要素の意味について説明します。

### <a name="description-of-elements"></a>要素の説明

次のテーブルでは、**RelationshipType** プロパティの要素について説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>要素名</th>
<th>説明</th>
<th>自動推論</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>NotSpecified</td>
<td>この要素は、多くの場合 <strong>RelationshipType</strong> プロパティの既定値です。</td>
<td><strong>RelationshipType</strong>プロパティの値が <strong>NotSpecified</strong> のとき、システムは適切な値を設定します。 システムは、次の順序で値を推論します。
<ol>
<li>仕様</li>
<li>リンク</li>
<li>構成</li>
<li>集約</li>
<li>関連</li>
</ol>
たとえば、構成および集計の両方の基準が満たされている場合、構成が以前にリストで発生したため、システムは構成を暗示します。</td>
</tr>
<tr class="even">
<td>仕様</td>
<td>この要素はベース テーブルと派生テーブル関係テーブルのテーブル継承のみに適用されます。</td>
<td>テーブルの継承が関係する場合は常に <strong>RelationshipType</strong> プロパティを <strong>Specialization</strong> に設定します。</td>
</tr>
<tr class="odd">
<td>リンク</td>
<td>この要素は、非リレーショナルな関係です。 <strong>検証</strong>プロパティを<strong>いいえ</strong>に設定する必要があります。 このタイプのリレーションシップは、テーブルの多くのレコードを一覧表示するページと、テーブルの 1 つのレコードの詳細フィールドを提供するページとの間でのナビゲーションをサポートします。</td>
<td>リンクは、以前のバージョンからアップグレードしている間に EDT リンクの関係の移行をサポートするためにのみ使用されます。 移行ツールはこの型の関係を作成しますが、作成しないでください。</td>
</tr>
<tr class="even">
<td>構成</td>
<td>この要素は、集約関係のより強力なタイプです。 テーブルには、複数の構成関係を持つことはできません。 たとえば、建物は部屋で構成され、指定された部屋は複数の建物の中に存在します。</td>
<td>合成の基準を満たしていますが、<strong>集計</strong>または<strong>関連</strong>の値を手動で割り当てる場合、システムではその値は<strong>集計</strong>または<strong>関連</strong>としてそのまま残ります。</td>
</tr>
<tr class="odd">
<td>集約</td>
<td>この要素は、子テーブルが親テーブルのエンティティに従属するとみなされる場合に適しています。 </td>
<td>次のいずれかの条件が当てはまる場合、システムは集計を推論します。
<ul>
<li>親テーブルには、このリレーション ノードを使用するために定義されている削除アクション ノードがあります。</li>
<li>子テーブル内の関係に対して外部キー フィールドでは<strong>必須</strong>プロパティが<strong>はい</strong>に設定されています。</li>
</ul>
集計の基準を満たしていますが、<strong>関連</strong>の値を手動で割り当てる場合、システムではその値は<strong>関連</strong>としてそのまま残ります。</td>
</tr>
<tr class="even">
<td>関連</td>
<td>この要素は、標準の外部キーの概念です。</td>
<td>プロパティ値がどんな値にも設定されず、集約と合成の両方が不適切な場合は、<strong>RelationshipType</strong> プロパティを<strong>アソシエーション</strong>に設定する必要があります。</td>
</tr>
</tbody>
</table>

## <a name="view-properties"></a>プロパティの表示
ビューのプロパティは、テーブルのプロパティと同じです。 ただし、ビューは読み取り専用であるため、それらのプロパティのほとんどは変更できません。 これらのプロパティの一部には固定値があり、ビューを定義するクエリで使用されているデータ ソースから継承されたプロパティもあります。 ビューの次のプロパティは、SSRS を使用しているときのデータ分析に関連しています。 これらすべての既定のプロパティを変更できます。

-   AnalysisVisibility
-   AnalysisSelection
-   TypicalRowCount
-   IsLookup
-   SingularLabel

次のテーブルに、ビューに設定できるプロパティを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AOSAuthorization</td>
<td>データ アクセス許可の検証が必要なデータ アクセス操作を指定するには、このプロパティを使用します。</td>
</tr>
<tr class="even">
<td>CacheLookup</td>
<td>テーブルのレコード キャッシュ レベル。</td>
</tr>
<tr class="odd">
<td>ClusterIndex</td>
<td>表のクラスター インデックス (クラスター インデックスがある場合)。</td>
</tr>
<tr class="even">
<td>ConfigurationKey</td>
<td>ビューのコンフィギュレーション キーを設定します。</td>
</tr>
<tr class="odd">
<td>CountryRegionCodes</td>
<td>メニューが適用されるか有効な国/地域のコードを指定します。 このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</td>
</tr>
<tr class="even">
<td>CountryRegionContextField</td>
<td>国/地域のコンテキストを識別するために使用されるフィールドを指定します。 <strong>CountryRegionCodes</strong> プロパティの説明を参照してください。</td>
</tr>
<tr class="odd">
<td>DeveloperDocumentation</td>
<td>表示の目的を説明し、プログラムでどのように使用されているかを説明します。 通常、説明は 5 つ以下の構文で構成され、単一の段落として書かれます。</td>
</tr>
<tr class="even">
<td>EntityRelationshipType</td>
<td>共通エンティティ リレーションシップ (ER) データ モデルの表記法に従ってビューを分類します。 ビューは、エンティティまたはリレーションシップとして分類されます。 エンティティはオブジェクトを表すのに対し、関係は 2 つのオブジェクト間の関連を表します。</td>
</tr>
<tr class="odd">
<td>FormRef</td>
<td>ビューの既定のページを指定します。 既定のページは、ユーザーがページ上のフィールドのショートカット メニューを使用してメイン テーブルにジャンプするときに表示されるページです。 このページは、<strong>表示</strong>タイプのメニュー項目によって参照されます。 このプロパティを空白のままにすると、MorphX はユーザーが参照しているテーブルと同じ名前のページを有効化しようとします。</td>
</tr>
<tr class="even">
<td>ID</td>
<td>オブジェクトの社内 ID。</td>
</tr>
<tr class="odd">
<td>ラベル</td>
<td>ビューのユーザー フレンドリ名を指定します。</td>
</tr>
<tr class="even">
<td>ListPageRef</td>
<td>このレコードの種類の一覧を表示できるページをポイントする表示メニュー項目を指定します。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>ビューがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="even">
<td>氏名</td>
<td>ビューの名前を指定します この名前は、X++ 言語のビューを参照するときに使用されます。</td>
</tr>
<tr class="odd">
<td>PreviewPartRef</td>
<td>拡張プレビューで使用される情報パーツまたはフォーム パーツを指定します。 情報パーツは指定したクエリからデータ フィールドのコレクションを表示しています。 メタデータを使用してデータの表示方法を説明します。 フォーム パーツは、ページへのポインターを表します。</td>
</tr>
<tr class="even">
<td>PrimaryIndex</td>
<td>ビューのプライマリ インデックスを指定します。 固有のインデックスのみ選択することができます。 このプロパティは、データベースの最適化と、キャッシュ キーとして使用するユニークなインデックスを示すために使用されます。 プライマリ インデックスを指定しない場合、最下位の ID の固有のインデックスはキャッシュ キーとして使用されます。</td>
</tr>
<tr class="odd">
<td>クエリ</td>
<td>ビューのデータのソースであるクエリを指定します。 ビューに直接データ ソースを追加する代わりに、このプロパティを使用することができます。</td>
</tr>
<tr class="even">
<td>ReportRef</td>
<td>テーブルの既定のレポートの名前。</td>
</tr>
<tr class="odd">
<td>SaveDataPerCompany</td>
<td>会社に固有のテーブルに対してこのプロパティを <strong>はい</strong> に設定します。 データが会社間、インストール、データベース、アプリケーション エクスプ ローラー、トレース、または OLAP に関連する場合、<strong>いいえ</strong> に設定します。 たとえば、SysTraceTable または OLAPServerTable テーブルは、会社ごとの基準でデータをそのテーブルに保存するかどうか、またはデータが任意の会社への所属なしで利用できるかどうかを指定します。 テーブルの <strong>SaveDataPerCompany</strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルには、会社 id を含む <strong>DataAreaId</strong> 列が含まれます。 テーブルのプロパティが<strong>いいえ</strong>に設定されている場合、<strong>DataAreaId</strong> 列はテーブルから削除されます。</td>
</tr>
<tr class="even">
<td>SaveDataPerPartition</td>
<td>ビューに<strong>パーティション</strong>という名前のシステム フィールドがあるかどうかを示す値。 このプロパティは、読み取り専用になっています。 ビューに<strong>パーティション</strong> フィールドがない場合、各レコードに 1 つのパーティションに割り当てられます。 各レコードは、他のパーティションのコンテキストで実行されるデータ アクセス操作から隠されます。</td>
</tr>
<tr class="odd">
<td>SearchLinkRefName</td>
<td>エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目の名前。</td>
</tr>
<tr class="even">
<td>SearchLinkRefType</td>
<td>エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目のタイプ。</td>
</tr>
<tr class="odd">
<td>SystemTable</td>
<td>テーブルがシステム テーブルであるかどうかを示す値。 システム テーブルは、エクスポートおよびインポート中にフィルター処理でき、ログインしたときに常に同期されます。 したがって、このプロパティは、サインインするとすぐに使用するテーブルに便利です。</td>
</tr>
<tr class="even">
<td>TableContents</td>
<td>顧客間でセットアップ/パラメーター データを再利用する方法を指定します。  次のオプションを使用できます。
<ul>
<li><strong>指定なし</strong> - ほとんどのテーブルにこのオプションを使用します。</li>
<li><strong>既定のデータ</strong> - このオプションは、郵便番号、単位、時間間隔など、顧客に依存しないデータに使用します。</li>
<li><strong>基本データ</strong> - カレンダー、グループ、およびパラメータなどの顧客に依存するデータ用のこのオプションを使用します。</li>
<li><strong>既定 + 基本データ</strong> - このオプションは、ローカル知覚が異なるデータに対して使用します。 たとえば、勘定科目表は、ドイツでは顧客に依存していませんが、他のほとんどの場所では顧客に依存しています。</li>
</ul></td>
</tr>
<tr class="odd">
<td>TableGroup</td>
<td>ビューが属するグループを指定します。 テーブル グループは、テーブルに含まれるデータのタイプに応じてテーブルとビューを分類します。 ビューは、任意のテーブルと同じテーブル グループに属することができます。</td>
</tr>
<tr class="even">
<td>TitleField1、TitleField2</td>
<td>ビューのウィンドウ キャプションに表示される情報。 キャプションは、次の要素から構成されます。
<ul>
<li><strong>TitleField1</strong> ラベル。後にコロン (:) とスペースが続きます</li>
<li><strong>TitleField1</strong> に使用する列の現在のレコードの値、後にコンマ (,) が続きます。</li>
<li><strong>TitleField2</strong> に使用する列の現在のレコードの値。</li>
</ul></td>
</tr>
<tr class="odd">
<td>ValidTimeStateEnabled</td>
<td>ビューが基になるテーブルの有効な時間状態機能をサポートしているかどうかを指定します。 既定値は <strong>いいえ</strong> です。 このプロパティは、以下の両方の条件が true の場合にのみ <strong>はい</strong> に設定することができます。
<ul>
<li>基礎になるテーブルは有効時間状態テーブルです。</li>
<li>ビューの <strong>Fields</strong> リストには、<strong>ValidFrom</strong> および <strong>ValidTo</strong> があります。</li>
</ul></td>
</tr>
<tr class="even">
<td>表示</td>
<td>テーブルがページやレポート内のデータ ソースとして使用される場合のアクセス権を指定します。 テーブルをページ内のデータ ソースとして使用する場合、ページのアクセス権は、テーブルに対して定義されているアクセス権を超えることはできません。</td>
</tr>
</tbody>
</table>

## <a name="data-set-properties"></a>データ セットのプロパティ
このセクションでは、アプリケーション エクスプローラーのデータセット要素のプロパティについて説明します。 **データ セット** ノードは、アプリケーション エクスプローラーの高レベル ノードです。 データ セットは、エンタープライズ ポータルのデータへのアクセスに使用されます。

### <a name="description-of-properties"></a>プロパティの説明

次のテーブルは、アプリケーション エクスプローラーの データ セット ノードで使用可能なプロパティを示しています。

| プロパティ | 説明                   |
|----------|-------------------------------|
| 氏名     | データ セットの名前を設定します。 |

### <a name="data-sources-properties"></a>データ ソース プロパティ

次のテーブルでは、**データ ソース** ノードのプロパティについて説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ChangeGroupMode</td>
<td>データ ソースへの変更をコミットする方法を指定します。  次のオプションを使用できます。
<ul>
<li><strong>なし </strong>- データ セットに対するデータ ソースの変更は、他のデータ ソースの変更とは独立して行われます。</li>
<li><strong>ImplicitInnerOuter</strong> - 内部結合または外部結合のすべてのデータ ソースが 1 つの単位として機能します。 すべての変更が正常に確定した場合、またはエラーが発生した場合にはこれらはロールバックします。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="data-set-data-source-properties"></a>データ セットのデータ ソース プロパティ
次のテーブルでは、データ セット データ ソースで使用可能なプロパティについて説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowCheck</td>
<td>データ セットにアクセスする前にセキュリティ チェックを行うかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - ユーザーの読み取りアクセス許可は、データ セットにアクセスする前に検証されます。</li>
<li><strong>いいえ</strong> - ユーザーの読み取りアクセス許可は、データ セットにアクセスした後でのみが検証されます。 ユーザーが基になるデータ ソースに対して十分なアクセス許可を持っていない場合は、データは取得されません。</li>
</ul>
<strong>はい</strong> が既定値で、通常お勧めします。</td>
</tr>
<tr class="even">
<td>AllowCreate</td>
<td>ユーザーがデータ ソース内に (つまり、データ ソースのテーブルに) 新しいレコードを作成できるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>AllowDelete</td>
<td>ユーザーがデータ ソース内の (つまり、データ ソースのテーブルの) レコードを削除できるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>AllowEdit</td>
<td>ユーザーはデータを変更できかどうかを指定します。 <strong>ヒント:</strong> ここでは、データ ソース全体の <strong>AllowEdit</strong> プロパティを設定できます。 データ ソースの各フィールドにも同じプロパティが存在するため、個々のフィールドの変更を禁止することができます。</td>
</tr>
<tr class="odd">
<td>AutoNotify</td>
<td>このプロパティは、データ セットには使用されません。</td>
</tr>
<tr class="even">
<td>AutoQuery</td>
<td>このプロパティは、データ セットには使用されません。</td>
</tr>
<tr class="odd">
<td>AutoSearch</td>
<td>このプロパティは、データ セットには使用されません。</td>
</tr>
<tr class="even">
<td>CounterField</td>
<td>データ ソース内のフィールドのいずれかをデータ セットのカウンターとして指定します。 フィールドは、データ ソースの基になるテーブルのインデックスでなければならず、<strong>real</strong> 型である必要があります。 このプロパティは、データセットに挿入されるレコードに、データの実際の連続する位置に対応する行番号があることを保証します。 たとえば、新しい明細行が行の 3 と 4 の間で挿入されると、新しい明細行の行番号は 3.5 になります。</td>
</tr>
<tr class="odd">
<td>CrossCompanyAutoQuery</td>
<td>データ ソースが複数の会社のデータベースからデータを取得するかどうかを指定します。</td>
</tr>
<tr class="even">
<td>DelayActive</td>
<td>データ ソースに対するアクティブ メソッドの実行を遅延させるには、このプロパティを使用します。 このプロパティを<strong>はい</strong>に設定すると、有効なメソッドは 20 ミリ秒の遅延が発生した後にのみ有効になります。 ユーザーがデータ ソースをスクロールするとき、各レコードに対して、有効なメソッドは呼ばれません。 代わりに。 ユーザーが選択する最後のレコードに対してのみ呼び出されます。 <strong>ヒント:</strong><strong>DelayActive</strong> プロパティは、2 つのデータ ソースがリンクされている場合 (つまり <strong>LinkType</strong> プロパティが<strong>遅延</strong>に設定されている場合) に特に便利です。 このプロパティは、AutoJoin システムの一部です。 </td>
</tr>
<tr class="odd">
<td>指数</td>
<td>並べ替え順序を指定するために使用するインデックスを設定します。 テーブル上で任意のインデックスを選択することができます。 この方法でインデックスを指定する場合、そのインデックスは、データベースへの各クエリでインデックス ヒントとして使用されません。 インデックスは、このデータ ソースに基づいて、データ セット内のレコードのアクセス パスとソート順の両方を指定します。 レコードの最初のソート順は、次のようにして優先順位付けされます。
<ol>
<li>データ ソース クエリには、フィールドの並べ替えを追加する場合は、並べ替えの指定が使用されます。</li>
<li>インデックスがデータ ソースの<strong>インデックス</strong> プロパティで指定されている場合は、インデックスで暗黙的に指定された並べ替え順序を使用します。</li>
<li>データ ソースが別のデータ ソースと自動結合されている場合は、システムはこの結合における最も適切なインデックスを検索し、そのインデックスに従ってデータを並べ替えます。</li>
<li>何も指定されていない場合は、ページのデータ ソースで使用されるテーブルの最初のインデックス (最下位の ID を持つインデックス) で暗黙的に指定されている並べ替え順序が使用されます。</li>
</ol>
インデックス ヒントが指定されていないとき、データベース管理システムは適切なアクセス パスを特定します。 このアクセス パスは、提供されるクエリの情報に基づきます。 ユーザーは、クエリ ダイアログ ボックスを使用してページの並べ替え順序を変更できます。</td>
</tr>
<tr class="even">
<td>InsertAtEnd</td>
<td>ユーザーがテーブルに最後のレコードを過ぎてフォーカスを移動したときに、新しいレコードを作成するかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>InsertIfEmpty</td>
<td>テーブルにレコードが存在しない場合、空白のレコードを挿入するかどうかを指定します。 このプロパティを<strong>いいえ</strong>に設定すると、新しいレコードを手動で作成する必要があります。</td>
</tr>
<tr class="even">
<td>JoinSource</td>
<td>2 つのデータ ソースを結合するには、このプロパティを使用します。 2 つ以上のテーブルがデータ ソースとして使用され、それらを結合する場合にこのプロパティを設定します。</td>
</tr>
<tr class="odd">
<td>LinkType</td>
<td>2 つのデータ ソース間でアクティブなリンクを管理するには、このプロパティを使用します。 最初のデータ ソースでフォーカスが変更されると、2 番目のデータ ソース内の対応する 1 つまたは複数のレコードが選択されます。 たとえば、顧客テーブルおよびトランザクションのテーブルが、各顧客に対して使用されます。 ユーザーがある顧客から次の顧客にスクロールするとき、トランザクションの一覧が自動的に更新されて、現在の顧客のトランザクションが表示されます。 外部 (外部にリンクされた) データ ソースのこのプロパティを <strong>遅延</strong> に設定します。 リンクされたデータ ソースは、100 ミリ秒の遅延後にのみ更新されます。 この遅延は、ユーザーがデータ ソースをスクロールしている間に、リンクされたデータ ソースが更新されないようにするのに役立ちます。 更新は、ユーザーが最終的にレコードにフォーカスした後にのみ発生します。 このプロパティは、AutoJoin システムの一部です。 </td>
</tr>
<tr class="even">
<td>氏名</td>
<td>データ ソースの名前を設定します。 この名前は基になるテーブルの名前と同じである必要があります。</td>
</tr>
<tr class="odd">
<td>OnlyFetchActive</td>
<td>データ ソース内のすべてのフィールドをフェッチするか、データ セットにより使用されるフィールドのみをフェッチするかどうかを指定します。 このプロパティを<strong>はい</strong>に設定すると、データ セットからレコードを削除できません。 この制限は、不完全なレコードに対して削除操作が行われないことを保証するために、データの整合性を維持するのに役立ちます。</td>
</tr>
<tr class="even">
<td>OptionalRecordMode</td>
<td>外部結合テーブルでレコードの作成または削除動作を指定します。  次のオプションを使用できます。
<ul>
<li><strong>ImplicitCreate</strong> - データベースにレコードが保存されていない場合は、親レコードがアクティブになるとすぐに外部結合レコードと結合テーブルを作成します。 外部結合レコードまたは子レコードが変更されていない場合、親レコードがアクティブでなくなったときに削除されます。</li>
<li><strong>ExplicitCreate</strong> - データベースにレコードが保存されていない場合は、<strong>オプションのレコード</strong>チェックボックスを使用してユーザーが明示的に作成をトリガーするまで、このレコードを無効として扱います。 このレコードが存在するときは、このチェック ボックスをオフにすると、このレコードが削除されます。</li>
<li><strong>なし</strong> - 外部結合レコードに対しては、特別な作成または削除の動作は発生しません。</li>
</ul></td>
</tr>
<tr class="odd">
<td>StartPosition</td>
<td>のデータ セットにアクセスするときに最初のレコードと最後のレコードのどちらを現在のレコードにするかを指定します。</td>
</tr>
<tr class="even">
<td>テーブル</td>
<td>データ ソースとして使用されるテーブルを設定します。</td>
</tr>
<tr class="odd">
<td>ValidTimeStateAutoQuery</td>
<td>日付の有効性のクエリの種類を指定します (<strong>AsOfDate</strong> または <strong>DateRange</strong>)。</td>
</tr>
<tr class="even">
<td>ValidTimeStateUpdate</td>
<td>既存の日付の有効なレコードの更新の種類を指定します。  次のオプションを使用できます。
<ul>
<li><strong>CreateNewTimePeriod</strong> - 前のレコードになっているレコードでは、<strong>ValidTo</strong> 日付フィールドは、現在の日付よりも遅くない日付に設定されます。 同じトランザクションでは、新しい現在のレコードが <strong>ValidFrom</strong> フィールドを、前のレコードの <strong>ValidTo</strong> の日付の直後に設定します。</li>
<li><strong>修正</strong> - 既存の行の <strong>ValidFrom</strong> または <strong>ValidTo</strong> の値は、レコード セットが更新された後に日付有効データの有効期間を保持するように変更する必要があります。</li>
<li><strong>EffectiveBased </strong> - 過去のレコードは編集できません。 現在アクティブなレコードは、CreateNewTimePeriod モードに似た方法で編集されます。 修正モードと似た方法で、将来のレコードが編集されます。</li>
</ul>
既定値は <strong>CreateNewTimePeriod</strong> です。</td>
</tr>
</tbody>
</table>

## <a name="form-properties"></a>フォーム プロパティ
このセクションでは、アプリケーション エクスプローラーでフォームに設定するプロパティについて説明します。 一貫したアプリケーション インターフェイスを提供するために、多くのプロパティは**自動**値を持っています。 ドラッグ アンド ドロップ操作を使用してから複数のプロパティを手動で設定することにより、フォームを作成することができます。 フォームの名前を指定するには、フォームの **プロパティ** ウィンドウで **名前** プロパティを設定します。 フォーム最上位ノードのその他すべてのプロパティはシステム プロパティおよび読み取り専用です。

## <a name="form-design-properties"></a>フォーム デザイン プロパティ
フォームの**デザイン** ノードにあるほとんどのプロパティは、個々のコントロールにも存在します。 例には、**幅**および**高さ**プロパティが含まれます。 ただし、コントロールでプロパティを設定するのではなく、**デザイン** ノードでプロパティを設定する場合、フォーム全体に影響が生じます。 いくつかのプロパティは、**デザイン**ノードにのみ存在します。 次のテーブルにこれらのプロパティを示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AlignChild</td>
<td>グループ内のコントロールが、グループまたはフォーム デザイン全体の <strong>AlignChildren</strong> プロパティ設定に従っているかどうかを指定します。 たとえば、フォームの<strong>デザイン</strong>ノードで <strong>AlignChildren</strong> を<strong>はい</strong>に設定しても、特定のグループがその他のグループと共に配置されないようにします。 この場合、そのグループに対して <strong>AlignChild</strong> を<strong>いいえ</strong>に設定します。</td>
</tr>
<tr class="even">
<td>AlignChildren</td>
<td>コンテナー内の子コントロールを配置します。</td>
</tr>
<tr class="odd">
<td>AllowDocking</td>
<td>クライアント ワークスペースにフォームを関連付けることができるかどうかを指定します。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="even">
<td>AllowFormCompanyChange</td>
<td>フォームが会社間動的リンク ライブラリ (DLL) で子フォームとして使用される場合に会社の変更をサポートするかどうかを指定します。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="odd">
<td>AllowUserSetUp</td>
<td>ユーザーがフォーム上のコントロールを移動できるかどうかと、コントロール プロパティの値を変更できるかどうかを指定します。 このプロパティは、フォームのデザインにもあります。  次のオプションを使用できます。
<ul>
<li><strong>いいえ</strong> - ユーザーはこのコンテナー内のコントロールをカスタマイズできません。</li>
<li><strong>制限</strong> - ユーザーは個々のコントロールのプロパティを変更できますが、コントロールを移動することはできません。</li>
<li><strong>はい </strong>- ユーザーの設定に制限はありません。</li>
</ul>
既定値は <strong>はい</strong> です。 <strong>注意:</strong> コントロールの親コンテナのいずれかにユーザー設定レベルの制限がある場合、完全なユーザー設定は許可されません。 フォーム データ ソースの <strong>AllowAdd</strong> プロパティにより、ユーザーがフォームにフィールドを追加できるかどうかが決まります。</td>
</tr>
<tr class="even">
<td>AlwaysOnTop</td>
<td>フォームが常に他のウィンドウの上に Z オーダーで表示されるかどうかを指定します。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="odd">
<td>ArrangeMethod</td>
<td>行または列に子フィールド グループを配置するかどうかを指定します。</td>
</tr>
<tr class="even">
<td>ArrangeWhen</td>
<td>コンテナーのコントロールを配置するタイミングを指定します。  次のオプションを使用できます。
<ul>
<li>スタートアップ</li>
<li>オンデマンド</li>
<li>許可しない</li>
<li>既定</li>
<li>自動</li>
</ul>
既定値は <strong>スタートアップ</strong> です。</td>
</tr>
<tr class="odd">
<td>BackgroundColor</td>
<td>コントロールの背景に使用される色を指定します。 背景を不透明または透明にするには、<strong>BackStyle</strong> プロパティを使用します。</td>
</tr>
<tr class="even">
<td>BottomMargin</td>
<td>ピクセル単位でフォームの下部余白を設定します。 既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>キャプション</td>
<td>グループ化されたコントロールの見出しを指定します。 このプロパティのラベルを使用します。</td>
</tr>
<tr class="even">
<td>ColorScheme</td>
<td>コントロールのカラー パレットを指定します。 フォーム全体のカラー パレットを変更するには、最大のコンテナーの <strong>ColorScheme</strong> プロパティを設定し、個々のコントロールの規定値を保持します。</td>
</tr>
<tr class="odd">
<td>列</td>
<td>情報が表示される列数を指定します。 <strong>注意:</strong> 基になるテーブルのフィールド グループが 1 つ以上の列に分割されることはありません。</td>
</tr>
<tr class="even">
<td>ColumnSpace</td>
<td>コンテナー コントロール内の列の間にスペースの金額を設定します。</td>
</tr>
<tr class="odd">
<td>DataSource</td>
<td>コントローのデータの取得元のテーブルを指定します。 テーブル内の特定のフィールドを設定するには、<strong>DataField</strong> プロパティを使用します。 コントロールでは、別のフォームが開き、このプロパティによって指定されたコントロールのデータ ソースと 2 番目の形式で記録するその他のフォームのヘルプ保証でデータ ソースとの関係が動的に選択されます。 たとえば、顧客が 1 つのフォームで選択され、コントロールは顧客トランザクションを表示するフォームを開きます。 この場合、2 番目のフォームには現在の顧客に適用される顧客トランザクションの範囲が表示されます。 <strong>注意:</strong> <strong>DataSource</strong> と <strong>DataField</strong> プロパティを設定すると、その設定は、<strong>DataMethod</strong> または <strong>ExtendedDataType</strong> プロパティの設定を上書きします。</td>
</tr>
<tr class="even">
<td>フォント</td>
<td><strong>フォント</strong> ダイアログ ボックスを使用して、コントロールのフォント プロパティを変更します。 ダイアログ フォントを使用して、フォント、フォント スタイル、フォント サイズを指定します。</td>
</tr>
<tr class="odd">
<td>フレーム</td>
<td>このフォームが使用するフレーム スタイルを指定します。</td>
</tr>
<tr class="even">
<td>高さ</td>
<td>ピクセル単位でフォームまたはコントロールの高さを指定します。</td>
</tr>
<tr class="odd">
<td>HideIfEmpty</td>
<td>コンテナー コントロールが空の場合は、このプロパティを使用してコンテナー コントロールを非表示にします。 この場合、コントロールのサイズが 0 (ゼロ) であるため、コンテナの<strong>幅</strong>と<strong>高さ</strong>のプロパティが<strong>自動</strong>に設定されている場合、このプロパティは影響を及ぼしません。</td>
</tr>
<tr class="even">
<td>HideToolBar</td>
<td>ツールバーのフォーム固有ボタンを非表示にします。</td>
</tr>
<tr class="odd">
<td>ImageMode</td>
<td><strong>ImageName</strong> プロパティで指定されたビットマップがコントロールにどのように表示されるかを定義します。  次のオプションを使用できます。
<ul>
<li>標準</li>
<li>サイズを合わせる</li>
<li>左右に並べて表示</li>
<li>センター</li>
</ul>
既定値は <strong>通常</strong> です。</td>
</tr>
<tr class="even">
<td>ImageName</td>
<td>コントロールに表示されるイメージを指定します。 .bmp ファイルのみを選択することができます。 リソース ファイルのいずれかを使用するには、<strong>ImageResource</strong> プロパティを代わりに使用します。</td>
</tr>
<tr class="odd">
<td>ImageResource</td>
<td>イメージ リソース ファイルのイメージの 1 つを、コントロールのイメージとして使用します。 イメージの ID を指定します。 統合リソース ファイルからイメージのみを選択することができます。 別のファイル タイプを使用するには、<strong>ImageName</strong> プロパティを使用します。</td>
</tr>
<tr class="even">
<td>LabelFont</td>
<td><strong>ラベル</strong> プロパティに含まれているテキストのフォントを変更する</td>
</tr>
<tr class="odd">
<td>左</td>
<td>フォームの左上隅の位置を変更します。 事前に定義された設定がいくつかあります。 また、ピクセル単位で正確な位置を指定することができます。 次の事前定義済みの設定が使用できます。
<ul>
<li>自動 (左)</li>
<li>自動 (右)</li>
<li>左とじ</li>
<li>右端</li>
<li>センター</li>
</ul>
既定値は <strong>自動 (左)</strong> です。</td>
</tr>
<tr class="even">
<td>LeftMargin</td>
<td>フォームの既定の左余白を変更します。 利益幅はピクセル単位で指定されます。</td>
</tr>
<tr class="odd">
<td>MaximizeBox</td>
<td>外側のウィンドウの右上隅に最大化ボックスを含めるかどうかを指定します。 既定値は <strong>はい</strong> です。</td>
</tr>
<tr class="even">
<td>MinimizeBox</td>
<td>外側のウィンドウの右上隅に最小化ボックスを含めるかどうかを指定します。 既定値は <strong>はい</strong> です。</td>
</tr>
<tr class="odd">
<td>モード</td>
<td>フォームのデータ入力モードを指定します。</td>
</tr>
<tr class="even">
<td>モデル</td>
<td>フォームがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="odd">
<td>RightMargin</td>
<td>フォームの既定の右余白を変更します。 利益幅はピクセル単位で指定されます。</td>
</tr>
<tr class="even">
<td>SaveSize</td>
<td>このプロパティを <strong>はい</strong> に設定し、フォームのサイズを保存します。</td>
</tr>
<tr class="odd">
<td>ScrollBars</td>
<td>スクロール バーがフォームで有効になっているかどうかを指定します。</td>
</tr>
<tr class="even">
<td>SetCompany</td>
<td>フォームがフォーカスを受け取ったとき、システムが会社を変更します。 <strong>注記: </strong>テーブルの <strong>SaveDataPerCompany</strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルをデータ ソースとして使用するフォーム デザインの <strong>SetCompany</strong> プロパティも<strong>はい</strong>に設定する必要があります。</td>
</tr>
<tr class="odd">
<td>StatusBarStyle</td>
<td>フォーム内でのステータス バーの表示方法を指定します。 ステータス バーを非表示にする、ヘルプ情報のみを表示する、<strong>WindowType</strong> 設定に従ってステータス バーの要素を表示する、または常にステータス バー全部を表示する、を指定するには、このプロパティを使用します。 <strong>注記:</strong> <strong>ListPage</strong>、<strong>ContentPage</strong>、または<strong>ワークスペース</strong>の WindowType 設定を持つフォームは、このプロパティを無視します。</td>
</tr>
<tr class="even">
<td>スタイル</td>
<td>フォームのスタイルを指定します。 このプロパティは、フォームで使用されているフォーム設計パターンを制御します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>DetailsFormMaster</li>
<li>DetailsFormTransaction</li>
<li>ダイアログ</li>
<li>DropDialog</li>
<li>FormPart</li>
<li>ListPage</li>
<li>ルックアップ</li>
<li>SimpleList</li>
<li>SimpleListDetails</li>
<li>TableOfContents</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>TitleDataSource</td>
<td>フォーム キャプションで使用するデータ ソースを指定します。</td>
</tr>
<tr class="even">
<td>上</td>
<td>フォームの上部の位置を変更します。 事前に定義された設定がいくつかあります。 また、ピクセル単位で正確な位置を指定することができます。 次の事前定義済みの設定が使用できます。
<ul>
<li>自動</li>
<li>トップ エッジ</li>
<li>下端</li>
<li>センター</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>TopMargin</td>
<td>ピクセル単位でフォームの上部余白を設定します。 既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="even">
<td>UseCaptionFromMenuItem</td>
<td>フォーム キャプションを呼び出し元のメニュー項目のラベルで置き換えるかどうかを指定します。 このプロパティを使用すると、フォームを開いたときにフォームのキャプションを変更できます。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="odd">
<td>ViewEditMode</td>
<td>フォームが読み取り専用モードで開くか、フィールドを変更することができるフォームとして開くかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>表示 </strong>- 読み取り専用でフォームを開きます。</li>
<li><strong>編集</strong> - 編集モードでフォームを開きます。</li>
<li><strong>自動 </strong>- 適切なモードでフォームを開きます。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="even">
<td>表示</td>
<td>フォームを非表示にするには、このプロパティを使用します。 <strong>注意:</strong> <strong>表示</strong>プロパティを使用してアクセス制限を実施することはできません。 ユーザーは <strong>フォームの設定</strong> ダイアログ ボックスでコントロールの表示を変更できます。 アクセス制限を適用するには、代わりに <strong>Enabled</strong> および <strong>NeededAccessLevel</strong> プロパティを使用します。</td>
</tr>
<tr class="odd">
<td>幅</td>
<td>フォームの幅をピクセル単位で変更します。</td>
</tr>
<tr class="even">
<td>WindowResize</td>
<td>フォームのサイズを変更できるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>WindowType</td>
<td>ウィンドウのタイプを指定します。</td>
</tr>
<tr class="even">
<td>WorkflowDataSource</td>
<td>フォーム上のワークフローのルート データ ソースを設定します。 指定するルート データ ソースは、ワークフロー テンプレートの <strong>Document</strong> プロパティで使用されたクエリで指定されたルート データ ソースと同じである必要があります。</td>
</tr>
<tr class="odd">
<td>WorkflowEnabled</td>
<td>このプロパティを <strong>はい</strong> に設定し、フォームでワークフロー メニュー バーを有効にします。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="even">
<td>WorkflowType</td>
<td>以下の項目および動作を決定するワークフロー タイプを指定します。
<ul>
<li>使用するワークフロー ドキュメント。 ワークフロー ドキュメントは計算フィールドを公開し、ワークフローのデータ フィールドを公開するクエリを識別します。</li>
<li>ユーザーがタスクと承認を構成できるかどうか。</li>
<li>ワークフロー タイプが特定のモジュールに割り当てられているときに使用するワークフロー カテゴリ。</li>
<li>メニュー項目およびイベント ハンドラー</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="help-document-set-properties"></a>ヘルプ ドキュメントの設定プロパティ
ドキュメント セットは、ワークスペースに関連付けられているヘルプ ドキュメントのコレクションです。 コンテンツの要素を公開するときは、メタデータを使用して、コンテンツの要素または目次をドキュメント セットに追加します。 ワークスペースとドキュメント セットの関係を管理するために、Application Explorer には **Help Document Sets** という名前のノードが含まれています。 **Help Document Sets** ノードの各ドキュメント セットには、プロパティのコレクションが含まれます。 新しいドキュメント セットを追加またはドキュメント セットとワークスペース間の関係を変更する場合には、これらのプロパティを編集します。 **注意:** ワークスペースは、1 つのドキュメントセットにのみ関連付けることができます。 アプリケーション エクスプローラーで新しいドキュメント セットを追加してワークスペースに関連付けられますが、置き換えられたドキュメント セットからのドキュメントを表示することができなくなります。 通常、ヘルプ サーバーに公開するコンテンツ要素または目次エントリのドキュメント セットとして **UserDocumentation** を使用します。 次のテーブルでは、アプリケーション エクスプローラーの **Help Document Sets** ノードにあるドキュメント セットのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>種類</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DocumentSetName</td>
<td>文字列</td>
<td>ドキュメント セットを固有に識別する名前。 名前は 40 文字に制限されており、空白を含むことはできません。 コンテンツ要素または目次ファイル内の <strong>DocumentSets</strong> メタデータ要素の値を設定する場合は、このプロパティの値を使用します。</td>
</tr>
<tr class="even">
<td>DocumentSetDescription</td>
<td>文字列</td>
<td>ドキュメント セットに表示するテキストまたはラベル。 この値は、ヘルプ ビューアの <strong>オプション</strong> メニューにある <strong>Search content from</strong> 一覧に表示されます。</td>
</tr>
<tr class="odd">
<td>AddToApplicationHelpMenu</td>
<td>ブール型</td>
<td>ドキュメントがアプリケーション ワークスペースの <strong>ヘルプ</strong> メニューに表示されるように設定する場合、このプロパティを <strong>はい</strong> にします。</td>
</tr>
<tr class="even">
<td>AddToDeveloperHelpMenu</td>
<td>ブール型</td>
<td>ドキュメントが開発者ワークスペースの <strong>ヘルプ</strong> メニューに表示されるように設定する場合、このプロパティを <strong>はい</strong> にします。</td>
</tr>
<tr class="odd">
<td>UserDocumentSet</td>
<td>ブール型</td>
<td>このプロパティを <strong>はい</strong> に設定し、アプリケーション ワークスペースにドキュメント セットを関連付けます。 このプロパティを<strong>いいえ</strong>に設定すると、Microsoft がリリースしたコンテキストに応じた (F1) ヘルプを表示することはできません。</td>
</tr>
<tr class="even">
<td>DeveloperDocumentSet</td>
<td>ブール型</td>
<td>このプロパティを <strong>はい</strong> に設定し、開発ワークスペースにドキュメント セットを関連付けます。 このプロパティを<strong>いいえ</strong>に設定すると、Microsoft がリリースしたコンテキストに応じた (F1) ヘルプを表示することはできません。</td>
</tr>
<tr class="odd">
<td>ContentLocation</td>
<td>列挙</td>
<td>ドキュメントを取得する場所を指定する列挙値です。 次のテーブルでは、列挙型について説明します。
<table>
<thead>
<tr class="header">
<th>先頭値</th>
<th>ラベル</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>ヘルプ サーバー</td>
<td>ドキュメントはヘルプ サーバーに保存されています。 このオプションは、<strong>UserDocumentation</strong> ドキュメント セットおよびヘルプ サーバー上でファイルが公開されているドキュメント セットとともに使用されます。</td>
</tr>
<tr class="even">
<td>2</td>
<td>World Wide Web</td>
<td>ドキュメントは MSDN または類似の Web サイトに保存されています。 このオプションは、<strong>DeveloperDocumentation</strong> のドキュメント セットに必要です。他のドキュメント セットでは使用しないでください。</td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

## <a name="menu-properties"></a>メニューのプロパティ
次のテーブルは、アプリケーション エクスプローラーの **メニュー** ノードのメニューで使用可能なプロパティを示しています。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ConfigurationKey</td>
<td>メニューのコンフィギュレーション キーを設定します。</td>
</tr>
<tr class="even">
<td>CountryRegionCodes</td>
<td>メニューが適用されるか有効な国/地域のコードを指定します。 このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</td>
</tr>
<tr class="odd">
<td>DisabledImage</td>
<td>メニューが無効になっているときに使用するボタンの画像を指定します。 このプロパティが設定されていない場合、システムでは <strong>NormalImage</strong> プロパティの設定が使用され、画像が生成されます。</td>
</tr>
<tr class="even">
<td>DisabledImageLocation</td>
<td>無効なコントロールに使用される画像の場所を指定します。 ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。 このプロパティに選択した値によって、<strong>DisabledImage</strong> プロパティで使用可能な値が決まります。 プロパティが設定されていない場合、システムでは <strong>ImageLocation</strong> プロパティの設定が使用され、画像を生成します。</td>
</tr>
<tr class="odd">
<td>ImageLocation</td>
<td>使用される画像の場所を指定します。 ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。 このプロパティに選択した値によって、<strong>NormalImage</strong> プロパティで使用可能な値が決まります。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>ユーザーに表示されるメニューの名前を設定します。</td>
</tr>
<tr class="odd">
<td>MenuItemName</td>
<td>メニューに含めるメニュー項目を指定します。 使用可能な値は、<strong>MenuItemType</strong> プロパティの値によって異なります。</td>
</tr>
<tr class="even">
<td>MenuItemType</td>
<td>メニュー項目のタイプを指定します。 メニュー項目には 3 つのカテゴリがあります。
<ul>
<li>ディスプレイ</li>
<li>出力</li>
<li>アクション</li>
</ul>
このプロパティに設定する値によって、<strong>MenuItemName</strong> プロパティのリストに表示されるメニュー項目名のリストが決まります。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>メニューがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に配置できます。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素を配置することができます。</td>
</tr>
<tr class="even">
<td>NormalImage</td>
<td>メニューが有効になっているときに使用する画像を指定します。</td>
</tr>
<tr class="odd">
<td>パラメーター</td>
<td>オブジェクトに渡される 1 つ以上の値を指定します。 これらの値は、メソッドに渡されるパラメーターに似ています。 パラメーターは、タスクの実行に使用される値を提供します。 既定値はありません。</td>
</tr>
<tr class="even">
<td>SetCompany</td>
<td>このプロパティを<strong>はい</strong>に設定すると、メニューを開くたびに、会社は、メニューが最初に起動したときに指定された会社に変更されます。</td>
</tr>
<tr class="odd">
<td>ショートカット</td>
<td>メニューを開くキーボード ショートカットを指定します。 たとえば、Ctrl + F3 キーを押してメニューを開くことができます。 既定値はありません。</td>
</tr>
<tr class="even">
<td>ShowParentModule</td>
<td>メニュー項目の親モジュールに基づいてナビゲーション ウィンドウを更新するかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>はい </strong>- メニュー項目の親モジュールに基づいてナビゲーション ウィンドウを常に更新してください。</li>
<li><strong>いいえ</strong> - メニュー項目の親モジュールが、現在のモジュールと異なる場合でもナビゲーション ウィンドウを変更せずにそのままにします。</li>
</ul>
既定値は <strong>はい</strong> です。</td>
</tr>
</tbody>
</table>

## <a name="menu-item-properties"></a>メニュー項目のプロパティ
次のプロパティは、Web メニューに使用されるメニュー項目であっても、すべてのメニュー項目 (表示、出力、およびアクション) で使用できます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ConfigurationKey</td>
<td>メニュー項目を有効にするために必要なコンフィギュレーション キーを選択します。 オブジェクトが属しているモジュールのキーを使用します。</td>
</tr>
<tr class="even">
<td>CopyCallerQuery</td>
<td>ターゲット フォームへの呼び出し元のフォームからクエリをコピーするかどうかを指定します。 このプロパティを使用すると、元のフォームで表示されたものと同じデータをターゲット フォームに表示できます。 既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>CorrectPermissions</td>
<td>メニュー項目に特権が割り当てられるときに適切なアクセス許可を選択できるかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>自動</strong> - アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</li>
<li><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="even">
<td>CountryConfigurationKey</td>
<td>オプション: 標準のコンフィギュレーション キーに加えて、または代わりに、国/地域固有のコンフィギュレーション キーを選択します。</td>
</tr>
<tr class="odd">
<td>CountryRegionCodes</td>
<td>メニュー項目が有効な国/地域のコードを指定します。 このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。 値は、グローバル アドレス帳のデータと一致する必要があります。 クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</td>
</tr>
<tr class="even">
<td>CreatePermissions</td>
<td>メニュー項目に特権が割り当てられるときに作成アクセス許可を選択できるかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>自動</strong> - アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</li>
<li><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>DeletePermissions</td>
<td>メニュー項目に特権が割り当てられるときに削除アクセス許可を選択できるかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>自動</strong> - アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</li>
<li><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="even">
<td>DisabledImage</td>
<td>メニュー項目が無効になっているときに使用する画像を指定します。 このプロパティが設定されていない場合、システムでは <strong>NormalImage</strong> プロパティの設定が使用され、画像が生成されます。</td>
</tr>
<tr class="odd">
<td>DisabledImageLocation</td>
<td>無効なコントロールに使用される画像の場所を指定します。 ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。 このプロパティに選択した値によって、<strong>DisabledImage</strong> プロパティで使用可能な値が決まります。 プロパティが設定されていない場合、システムでは <strong>ImageLocation</strong> プロパティの設定が使用され、画像を生成します。</td>
</tr>
<tr class="even">
<td>EnumTypeParameter および EnumParameter</td>
<td>オプション: オブジェクトのパラメーターとして列挙型を選択し、<strong>EnumParameter</strong> プロパティの値として列挙値を選択します。 通常、これらのプロパティは、1 つのフォームが複数の状況で使用されている場合に使用されます。 <strong>EnumParameter</strong> 値に応じて、フォームの動作を変更することができます。 たとえば、<strong>PriceDiscGroup</strong> フォームは 3 つの表示メニュー項目 (<strong>PriceDiscGroup_ *</strong>) により使用され、それぞれが異なる <strong>EnumParameter</strong> 値を持ちます。 フォームの <strong>init</strong> メソッドでは、switch 構造が値を検証してからフォームが作成されます。</td>
</tr>
<tr class="odd">
<td>ExtendedDataSecurity</td>
<td>メニュー項目が 1 つの会社のコンテキストでなくすべての会社の下に表示されるかどうかを指定します。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="even">
<td>FormViewOption</td>
<td>使用するフォーム モードを指定します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>グリッド</li>
<li>細目</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>HelpText</td>
<td>メニュー項目のヘルプ文字列を作成します。 メニュー項目で開いたオブジェクト (フォームなど) を選択すると、ステータス バーにテキストが表示されます。 <strong>注記:</strong> メニュー項目のヘルプ トピックを書き込むには、アプリケーション エクスプローラーの<strong>アプリケーションのドキュメント/メニュー項目</strong>ノードで、メニュー項目と同じ名前のトピックを見つけます。 このトピックは、メニュー項目によって開かれたオブジェクトについて書かれたヘルプ トピックの代わりに表示されます。</td>
</tr>
<tr class="even">
<td>ImageLocation</td>
<td>コントロールに使用される画像の場所を指定します。 ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。 このプロパティに選択した値によって、<strong>NormalImage</strong> プロパティで使用可能な値が決まります。</td>
</tr>
<tr class="odd">
<td>ラベル</td>
<td>メニューやボタンの項目に対して表示される名前として使用するラベルを選択します。</td>
</tr>
<tr class="even">
<td>LinkedPermissionObject</td>
<td>別のオブジェクト (たとえば、フォームまたはレポートなど) のアクセス許可をメニュー項目に適用する場合は、そのオブジェクトを選択します。 通常、このプロパティはアクション メニュー項目に使用されます。</td>
</tr>
<tr class="odd">
<td>LinkedPermissionType</td>
<td><strong>LinkedPermissionObject</strong> プロパティにより指定されるオブジェクトのタイプを指定します。</td>
</tr>
<tr class="even">
<td>MultiSelect</td>
<td>メニュー項目をフォームの複数レコードに使用できるかどうかを選択します。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>テーブルがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に配置できます。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素を配置することができます。</td>
</tr>
<tr class="even">
<td>氏名</td>
<td>メニュー項目の名前。</td>
</tr>
<tr class="odd">
<td>NeededAccessLevel</td>
<td>メニュー項目がメニューまたはボタンに表示されるのに必要な最小アクセスを定義します。 このプロパティは、異なるユーザー グループのメニュー項目へのアクセスを設定するために使用されます。</td>
</tr>
<tr class="even">
<td>NeedsRecord</td>
<td>レコードが存在しない場合、メニュー項目を表すボタンを有効にするかどうかを指定します。 既定値は <strong>いいえ</strong> です。 アクションが完了することを保証するために、このプロパティを使用することができます。 たとえば、詳細フォームを開くメニュー項目ボタンがあります。 リスト ページにレコードが存在しない場合、ボタンを無効にする場合があります。</td>
</tr>
<tr class="odd">
<td>NormalImage</td>
<td>メニュー項目が有効化されたボタン コントロールに関連付けられている場合に使用される画像を指定します。</td>
</tr>
<tr class="even">
<td>オブジェクト</td>
<td><strong>Class</strong> プロパティで指定されているオブジェクト タイプのオブジェクトを選択します。</td>
</tr>
<tr class="odd">
<td>ObjectType</td>
<td>メニュー項目が開かれるオブジェクトのタイプを選択します。 <strong>注意:</strong> SSRS レポートのメニュー項目に <strong>SSRSReport</strong> を使用する必要があります。 新しいメニュー項目の <strong>SQLReportLibraryReport</strong> を使用しないでください。 <strong>SQLReportLibraryReport</strong> オプションは使用されてないため、今後のバージョンでは削除されます。</td>
</tr>
<tr class="even">
<td>OpenMode</td>
<td>ターゲット フォームの表示モードを指定します。 このプロパティを使用して、ターゲット フォームを編集モードまたは読み取り専用モードのいずれで開くかを指定します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>表示</li>
<li>編集</li>
<li>新規</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>パラメーター</td>
<td>オプション: オブジェクトに渡される引数を指定します。</td>
</tr>
<tr class="even">
<td>クエリ</td>
<td><strong>InitialQuery</strong> メソッドのターゲット フォームに渡されるクエリを選択します。</td>
</tr>
<tr class="odd">
<td>ReadPermissions</td>
<td>メニュー項目に特権が割り当てられるときに読み取りアクセス許可がセクションに利用可能かどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>自動</strong> - アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</li>
<li><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="even">
<td>ReportDesign</td>
<td>特定の SSRS レポート モデルに使用するレポート デザインを選択します。</td>
</tr>
<tr class="odd">
<td>RunOn</td>
<td>クライアント、サーバー、または呼び出し元の場所でメニュー項目を実行するかどうかを選択します。 このプロパティは、主にレポートを開くメニュー項目に使用されます。 このプロパティは、オブジェクトの <strong>RunOn</strong> プロパティが<strong>呼び出し元</strong>に設定されている場合にのみ、アプリケーション オブジェクトの実行場所を決定します。
<ul>
<li><strong>FormRun</strong> クラスは常にクライアント上で実行されるため、フォームはインスタンス化されてクライアント上で実行されます。</li>
<li><strong>ReportRun</strong> クラスは常に呼び出された場所で実行されるため、レポートは、インスタンス化され、メニュー項目の <strong>RunOn</strong> プロパティで指定されたとおりに実行されます。 プロパティを<strong>呼び出し元</strong>に設定する必要があります。 レポートをクライアントで実行するように設定すると、レポートはバッチで実行され、レポートは失敗します。 レポートをサーバーで実行するように設定すると、レポートは画面に表示され、レポートは失敗します。</li>
<li>クラスの<strong>メイン</strong> メソッドは、モディファイアーで指定されたとおりに実行されます。 クラス自体は、<strong>RunOn</strong> プロパティで指定されたとおりにインスタンス化されます。 インスタンス化は、<strong>main</strong> メソッドで発生する可能性があります。</li>
</ul></td>
</tr>
<tr class="even">
<td>UpdatePermissions</td>
<td>メニュー項目に特権が割り当てられるときに更新アクセス許可がセクションに利用可能かどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>自動</strong> - アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限のセクションで使用可能になります。</li>
<li><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限のセクションで選択できません。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>Web</td>
<td>メニュー項目を実行するときに開かれる URL を指定します。 このプロパティ値は使用されなくなりました。 このプロパティを使用しないでください。</td>
</tr>
<tr class="even">
<td>WebConfigurationKey</td>
<td>オプション: 標準のコンフィギュレーション キーだけでなく、Web 固有のコンフィギュレーション キーを選択します。 このプロパティは、Web メニュー項目にのみ適用されます。</td>
</tr>
<tr class="odd">
<td>WebMenuItemName</td>
<td>Web メニューに含めるメニュー項目を指定します。 使用可能な値は、<strong>WebMenuItemType</strong> プロパティの設定によって異なります。</td>
</tr>
<tr class="even">
<td>WebMenuItemType</td>
<td>Web メニュー項目のタイプを指定します。 Web メニュー項目には 2 つのカテゴリがあります。
<ul>
<li>URL</li>
<li>アクション</li>
</ul>
選択した値によって、<strong>WebMenuItemName</strong> プロパティで使用可能な Web メニュー項目名が決まります。</td>
</tr>
<tr class="odd">
<td>WebPage</td>
<td>メニュー項目にリンクされている Web ページを指定します。 このプロパティ値は使用されなくなりました。 このプロパティを使用しないでください。</td>
</tr>
<tr class="even">
<td>WebSecureTransaction</td>
<td>メニュー項目にセキュリティで保護されたトランザクション (SSL) が必要かどうかを選択します。 このプロパティは、Web メニュー項目にのみ適用されます。</td>
</tr>
</tbody>
</table>

**注記:** **パラメーター**または **EnumParameter** を使用すると、タイプの不一致などのエラーはコンパイル時ではなく、実行時にのみ検出されます。

## <a name="query-properties"></a>プロパティの照会
クエリ内では、クエリ自体のプロパティ、データ ソース、ソートに使用するフィールド、およびクエリの制限に使用する範囲を設定することができます。

### <a name="query-properties"></a>プロパティの照会

クエリのプロパティは、クエリの全体的な動作を決定します。 たとえば、クエリと通信できるように、ユーザーに表示されているフォームを指定できます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowCheck</td>
<td>このプロパティは、クエリでは無視されます。 フォームやレポートには効果的ではありません。</td>
</tr>
<tr class="even">
<td>AllowCrossCompany</td>
<td>ユーザーが読み取る権限を持っているすべての会社のデータが取得されるかどうかを指定します。 プロパティが、既定値である <strong>false</strong> に設定されている場合、現在のセッションの会社に対してのみデータが取得されます。</td>
</tr>
<tr class="odd">
<td>説明</td>
<td>オプション: クエリについて、何を返すかなどを説明します。 このプロパティは、Microsoft Office アドイン シナリオで役立ちます。</td>
</tr>
<tr class="even">
<td>フォーム</td>
<td>ユーザーがクエリを操作するときに MorphX が表示する必要があるクエリ フォームを指定します。 既定値は <strong>SysQueryForm</strong> です。</td>
</tr>
<tr class="odd">
<td>対話型</td>
<td>ユーザーがクエリを区切る、プリンター オプションを設定するなどして、レポートを操作できるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>リテラル</td>
<td>SQL ステートメントでリテラルがどのような方法で表示されるかを指定します。 <strong>forceLiterals</strong> オプションは、最適化時に Microsoft SQL Server データベースに対して <strong>where</strong> 句で使用される実際値を明らかにするように、カーネルに指示します。 <strong>forcePlaceholders</strong> オプションは、実際の値を明らかにしないようにカーネルに指示します。 <strong>注記:</strong> <strong>forceLiterals</strong> オプションは、コードを SQL インジェクション セキュリティの脅威にさらす可能性があるため、使用しないことをお勧めします。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>クエリがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="even">
<td>QueryType</td>
<td>クエリのタイプを指定します。  次のオプションを使用できます。
<ul>
<li>結合</li>
<li>結合</li>
</ul>
既定値は <strong>結合</strong> です。</td>
</tr>
<tr class="odd">
<td>検索可能</td>
<td>Microsoft SharePoint Business Catalog を検索するために使用できる一連のクエリの一部としてクエリを使用するかどうかを指定します。 このプロパティは、エンタープライズ検索機能を使用する場合に便利です。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="even">
<td>肩書き</td>
<td>クエリのヘッダー。</td>
</tr>
<tr class="odd">
<td>UserUpdate</td>
<td>クエリ フォームが再度開かれたときにその状態を維持する必要があるかどうかを指定します。 このプロパティを<strong>はい</strong>に設定すると、以前の設定が復元されます。 <strong>いいえ</strong>を設定すると、データを表示できますが、編集できない可能性があります。</td>
</tr>
<tr class="even">
<td>バージョン</td>
<td>バージョンは、クエリが更新されるたびに増加します。 このプロパティは、読み取り専用です。</td>
</tr>
</tbody>
</table>

### <a name="data-source-properties"></a>データ ソース プロパティ

次のプロパティは、データ ソースの特性を制御します。 追加のプロパティは、埋め込みデータ ソースとデータ ソースとの関係で使用できます。 また、データ ソース内のフィールドに対して 1 つのプロパティを設定することもできます。

| プロパティ            | 入手する場所                 | 説明                                                                                                                                                                                                                                                                                                                        |
|---------------------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowAdd            | データ ソース                          | ユーザーが実行時に並べ替えおよび範囲にフィールドを追加できるかどうかを指定します。                                                                                                                                                                                                                                                            |
| 法人             | データ ソース                          | データの取得元の会社を指定します。                                                                                                                                                                                                                                                                                         |
| 動的             | データ ソースのフィールド ノード         | データ ソース内のテーブルのすべてのフィールドを使用するかどうかを指定します。 このプロパティを**はい**に設定すると、データ ソース内のすべてのフィールドが使用されます。 **いいえ**を設定すると、一部のフィールドを削除することができます。 データ ソースがベース テーブルのとき、**はい** の値は、派生テーブルのすべてのフィールドが使用されていることを意味します。 |
| 有効             | データ ソース                          | このプロパティを**いいえ**に設定すると、データ ソース (およびすべての埋め込みデータ ソース) は無視されます。                                                                                                                                                                                                                                   |
| FetchMode           | 埋め込みデータ ソース                 | 1:1 の関係または 1:n の関係を通じてデータ ソースを関連付ける必要があるかどうかを指定します。 **注記:** レポートで使用されているデータ ソースの場合、1:1 のフェッチ モードを使用する結合関係を使用します。                                                                                                                                    |
| フィールド、RelatedField | 埋め込みデータソースでの関係 | リレーションで使用される親データ ソースおよび関連データ ソースのフィールドの名前。                                                                                                                                                                                                                          |
| FirstFast           | データ ソース                          | このプロパティを**はい**に設定すると、データベースでは、クエリからの最初のレコードが、他のレコードの前に取得される必要があるというヒントが表示されます。 この設定により、一部のデータベース システムでレコードの検索を最適化できるため、パフォーマンスが向上します。                                                              |
| FirstOnly           | データ ソース                          | このプロパティを**はい**に設定すると、データベースでは、クエリからの最初のレコードのみが必要であるというヒントが表示されます。 この設定により、一部のデータベース システムでレコードの検索を最適化できるため、パフォーマンスが向上します。                                                                                          |
| JoinMode            | 埋め込みデータ ソース                 | データ ソースからの出力を結合するために使用される方法を指定します。                                                                                                                                                                                                                                                           |
| 氏名                | データ ソース                          | データ ソースの名前を指定します。                                                                                                                                                                                                                                                                                               |
| リレーション           | 埋め込みデータ ソース                 | テーブルと EDT に対して定義されている関係をクエリ システムが使用するかどうかを指定します。 このプロパティを**はい**に設定すると、リレーションが変更された場合にクエリが自動的に更新されます。                                                                                                                                  |
| テーブル               | データ ソース                          | データ ソースとして使用されるテーブル、マップ、またはビューを指定します。 このプロパティは、並べ替え順序または範囲が定義された後は変更できません。                                                                                                                                                                                  |
| Table、RelatedTable | 埋め込みデータソースでの関係 | 親データ ソースおよび関連データ ソースの名前。                                                                                                                                                                                                                                                                    |
| UniqueId            | データ ソース                          | データ ソースの一意の番号。 このプロパティは、読み取り専用です。                                                                                                                                                                                                                                                                  |
| 更新              | データ ソース                          | クエリがデータベース内のレコードを更新できるかどうかを指定します。                                                                                                                                                                                                                                                                      |

### <a name="range-properties"></a>範囲のプロパティ

次のプロパティは、範囲指定の特性を決定します。 たとえば、実行時に、範囲の変更を許可されているかどうかを指定できます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>有効</td>
<td>範囲指定のフィールドを無効にするには、このプロパティを使用します。</td>
</tr>
<tr class="even">
<td>フィールド</td>
<td>範囲を定義するためのフィールドを指定します。</td>
</tr>
<tr class="odd">
<td>ラベル</td>
<td>範囲のラベルを入力します。</td>
</tr>
<tr class="even">
<td>ステータス</td>
<td>ユーザーが実行時にクエリ ダイアログ ボックスで範囲の変更を許可されているかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>オープン</strong> - ユーザーは範囲を表示および編集できます。</li>
<li><strong>ロック</strong> - ユーザーは、範囲のみを表示できます。</li>
<li><strong>非表示</strong> - ユーザーは範囲を表示または編集できません。</li>
</ul></td>
</tr>
<tr class="odd">
<td>金額</td>
<td>取得されるレコードの範囲を指定します。 列挙型を使用する場合は、テキスト文字列を使用しません。 列挙 ID を使用する必要があります。</td>
</tr>
</tbody>
</table>

## <a name="report-properties"></a>レポート プロパティ
レポートのプロパティのほとんどは、アプリケーション エクスプローラーのデザイン、デザイン セクション、コントロール ノードに設定されます。 レポートで使用可能なシステム プロパティの詳細については、「システムと共通プロパティ」セクションを参照してください。 次のテーブルでは、レポートのプロパティについて説明します。

| プロパティ    | 説明                                                                                                                                                                                                                                  |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AllowCheck  | ユーザーが表示するアクセス許可を持たないレポートを実行しようとしたときにメッセージが表示されるかどうかを指定します。 **はい** を選択し、メッセージが表示されることを指定します。                                                                                 |
| AutoJoin    | レポート クエリの範囲を設定するために **element.args** メソッドにより返されたレコードを使用するかどうかを指定します。                                                                                                                       |
| 対話型 | ユーザーがレポートに関連付けられているクエリを変更することで、表示するレコードを選択できるかどうかを指定します。                                                                                                                              |
| モデル       | レポートがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 他の層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。 |

## <a name="report-control-properties"></a>レポート管理プロパティ
次のテーブルでは、レポート コントロールのプロパティについて説明します。 コントロールに使用される追加のプロパティの詳細については、「フォームのコントロールのプロパティ」セクションを参照してください。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>配置</td>
<td>コントロールに表示される値の配置を指定します。</td>
</tr>
<tr class="even">
<td>AllowNegative</td>
<td>コントロールが負の値を受け入れるかどうかを指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>ArrayIndex</td>
<td>コントロールに表示される配列要素を指定します。 このコントロールは、配列要素を持つ拡張データ型に基づいています。 このプロパティは、テキストおよびシェイプ コントロールでは使用できません。</td>
</tr>
<tr class="even">
<td>AutoDeclaration</td>
<td>コントロールと同じ名前を持つ変数が作成されるかどうかを指定します。 このプロパティを<strong>はい</strong>に設定すると、X++ コードからレポートコントロールへのアクセスが容易になり、コンパイル時にエラーを見つけることができます。</td>
</tr>
<tr class="odd">
<td>AutoInsSeparator</td>
<td>小数点区切り記号が表示されるかどうかを指定します。 このプロパティは、数コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>BackgroundColor</td>
<td>コントロールの背景色を指定します。 このプロパティの設定は、<strong>BackStyle</strong> プロパティを使用して上書きできます。</td>
</tr>
<tr class="odd">
<td>BackStyle</td>
<td>コントロールの背景色が不透明であるか透明であるかを指定します。 このプロパティを<strong>透明</strong>に設定すると、動作はコントロールのタイプによって異なります。
<ul>
<li>ビットマップ コントロールについては、同じ色を持つピクセル単位は透過的です。</li>
<li>その他のすべてのコントロールについては、前景色が背景色として使用されます。</li>
</ul></td>
</tr>
<tr class="even">
<td>太字</td>
<td>太字のテキストの書式設定を指定します。</td>
</tr>
<tr class="odd">
<td>BottomMargin</td>
<td>コントロールの余白を指定します。</td>
</tr>
<tr class="even">
<td>ChangeCase</td>
<td>ユーザーが入力したテキストが大文字か小文字かを指定します。 このプロパティは、文字列、列挙、確認、および確認コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>ChangeLabelCase</td>
<td>レポートを印刷するときにコントロールのラベルを変更するかどうかを指定します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>None</li>
<li>大文字</li>
<li>lower case</li>
<li>タイトル ケース</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="even">
<td>ColorScheme</td>
<td>コントロールのカラー パレットを指定します。</td>
</tr>
<tr class="odd">
<td>ConfigurationKey</td>
<td>コントロールの構成キーを指定します。</td>
</tr>
<tr class="even">
<td>CSSClass</td>
<td>HTML での値の表示に使用するカスケード スタイル シート (CSS) を指定します。</td>
</tr>
<tr class="odd">
<td>DataField</td>
<td>コントロールのテーブル フィールドを指定します。 このプロパティは、テキスト、シェイプ、ボックス、およびビットマップ コントロールでは使用できません。</td>
</tr>
<tr class="even">
<td>DataMethod</td>
<td>コントロールのデータを示す表示方法を指定します。 このプロパティは、テキスト、シェイプ、およびボックス コントロールでは使用できません。</td>
</tr>
<tr class="odd">
<td>DateDay</td>
<td>曜日の形式を指定します。 このプロパティは、日付コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>DateFormat</td>
<td>日付の形式を指定します。 このプロパティは、日付コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>DateMonth</td>
<td>月の形式を指定します。 このプロパティは、日付コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>DateSeparator</td>
<td>月、日、年の間に表示される区切り記号を指定します。 このプロパティは、日付コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>DateYear</td>
<td>年の形式を指定します。 このプロパティは、日付コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>DecimalSeparator</td>
<td>小数点以下の値を区別するために使用する記号を指定します。 このプロパティは、数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>DisplaceNegative</td>
<td>値が負の数値の場合のグリッド コントロール内の値の新しい位置を指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>DynamicHeight</td>
<td>テキストの追加の行を表示するためにコントロールのサイズを変更するかどうかを指定します。 このプロパティを<strong>はい</strong>に設定すると、必要に応じて、ページ ヘッダー、ページ フッター、および繰り返し列見出しが自動的に追加されます。 このプロパティは、文字列コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>ExtendedDataType</td>
<td>コントロールに関連付けられているフィールドを基にする EDT を指定します。</td>
</tr>
<tr class="even">
<td>ExtraSumWidth</td>
<td>合計に対して許可される既定の幅を変更します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>フォント</td>
<td>フォントを指定します。</td>
</tr>
<tr class="even">
<td>フォントサイズ</td>
<td>フォント サイズを指定します。</td>
</tr>
<tr class="odd">
<td>ForegroundColor</td>
<td>コントロールの前景色を指定します。</td>
</tr>
<tr class="even">
<td>FormatMST</td>
<td>標準通貨形式を使用して値を書式設定するかどうかを指定します。 このプロパティは、数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>高さ</td>
<td>コントロールの高さを指定します。 コントロールが EDTに関連付けられている場合、その <strong>Height</strong> プロパティは EDT の <strong>DisplayLength</strong> プロパティを上書きします。 ビットマップ コントロールの <strong>Height</strong> プロパティを<strong>自動</strong>に設定すると、コントロールのサイズは、グラフィックのサイズに基づきます。</td>
</tr>
<tr class="even">
<td>ImageName</td>
<td>画像のファイル名を指定します。 このプロパティは、ビットマップ コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>ImageResource</td>
<td>表示するシステム リソースの ID を指定します。 リソース マクロは、これらの ID のリストを提供します。 マクロは、アプリケーション エクスプローラーの<strong>マクロ</strong> ノードの下にあります。 このプロパティは、ビットマップ コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>斜体</td>
<td>斜体のテキストの書式設定を指定します。</td>
</tr>
<tr class="odd">
<td>ラベル</td>
<td>コントロールのタイトルを指定します。 ラベルがここで指定されていない場合は、フィールドから継承されます。</td>
</tr>
<tr class="even">
<td>LabelBold</td>
<td>コントロールのラベルの太字設定を示す値を設定するか返します。</td>
</tr>
<tr class="odd">
<td>LabelCSSClass</td>
<td>HTML でのラベルのレンダリングに使用する CSS を指定します。</td>
</tr>
<tr class="even">
<td>LabelFont</td>
<td>フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型値を設定するか返します。</td>
</tr>
<tr class="odd">
<td>LabelFontSize</td>
<td>フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。</td>
</tr>
<tr class="even">
<td>LabelItalic</td>
<td>コントロール ラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</td>
</tr>
<tr class="odd">
<td>LabelLineBelow</td>
<td>コントロール タイトルの下線の形式を指定します。</td>
</tr>
<tr class="even">
<td>LabelLineThickness</td>
<td>列見出しの下の行の形式を指定します。</td>
</tr>
<tr class="odd">
<td>LabelPosition</td>
<td>コントロールのラベルの位置を設定するか返します。 有効な値は <strong>Left</strong> および <strong>Above</strong> です。</td>
</tr>
<tr class="even">
<td>LabelTabLeader</td>
<td>ラベルを制御するために一連の点を追加するかどうかを指定します。  次のオプションを使用できます。
<ul>
<li>自動</li>
<li>追加しない</li>
<li>追記を実行</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>LabelUnderline</td>
<td>コントロール ラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。</td>
</tr>
<tr class="even">
<td>LabelWidth</td>
<td>コントロールのラベルの幅を指定します。</td>
</tr>
<tr class="odd">
<td>左</td>
<td>コントロールの左揃えを指定します。</td>
</tr>
<tr class="even">
<td>LeftMargin</td>
<td>コントロールの左余白を指定します。</td>
</tr>
<tr class="odd">
<td>明細行</td>
<td>図形を形成する線の外観を指定します。 このプロパティは、シェイプ コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>LineAbove</td>
<td>コントロールの上の境界線の線のタイプを指定します。 レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</td>
</tr>
<tr class="odd">
<td>LineBelow</td>
<td>コントロールの下の境界線の線のタイプを指定します。 レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</td>
</tr>
<tr class="even">
<td>LineLeft</td>
<td>コントロールの左の境界線の線のタイプを指定します。 レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</td>
</tr>
<tr class="odd">
<td>LineRight</td>
<td>コントロールの右の境界線の線のタイプを指定します。 レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</td>
</tr>
<tr class="even">
<td>MenuItemLabel</td>
<td>メニュー項目のラベルを指定します。</td>
</tr>
<tr class="odd">
<td>MenuItemName</td>
<td>メニュー項目の名前を指定します。 使用可能なメニュー項目は、<strong>MenuItemType</strong> プロパティの設定によって異なります。</td>
</tr>
<tr class="even">
<td>MenuItemType</td>
<td>メニュー項目がアクション、表示、出力メニュー項目のどれであるかを指定します。 表示メニュー項目はフォーム用で、出力メニュー項目はレポート用です。 出力メニュー項目はクラス、ジョブ、またはクエリです。</td>
</tr>
<tr class="odd">
<td>MinNoOfDecimals</td>
<td>表示される小数点以下桁数の最小数を指定します。 末尾のゼロは表示されません。</td>
</tr>
<tr class="even">
<td>ModelFieldName</td>
<td>左揃えとコントロールの幅を決定するために使用されるフィールドを指定します。</td>
</tr>
<tr class="odd">
<td>NoOfDecimals</td>
<td>表示される小数点以下桁数を指定します。 既定値は <strong>20</strong> です。 このプロパティは、数コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>ResizeBitmap</td>
<td>コントロールのサイズに合わせてイメージのサイズを変更できるかどうかを指定します。 このプロパティは、ビットマップ コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>RightMargin</td>
<td>コントロールの余白を指定します。</td>
</tr>
<tr class="even">
<td>RotateSign</td>
<td>コントロールの符号を反転するかどうかを指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>ShowLabel</td>
<td>コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。 <strong>True</strong> の値は、ラベルが表示されることを示します。</td>
</tr>
<tr class="even">
<td>ShowPicAsText</td>
<td>画像ではなく、画像のファイル名を表示するかどうかを指定します。 このプロパティは、ビットマップ コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>ShowZero</td>
<td>0 (ゼロ) の値が表示されるかどうかを指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>SignDisplay</td>
<td>数値の符号の表示方法を指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>SumAll</td>
<td>すべての値の合計が計算されるかどうかを指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>SumNeg</td>
<td>すべての負の値の合計が計算されるかどうかを指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>SumPos</td>
<td>すべての正の値の合計が計算されるかどうかを指定します。 このプロパティは、整数および実数コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>テーブル</td>
<td>コントロールのソース タイプを指定します。 このプロパティは、テキスト、シェイプ、ボックス、およびビットマップ コントロールでは使用できません。</td>
</tr>
<tr class="odd">
<td>テキスト</td>
<td>コントロールに表示されるテキスト文字列を指定します。 このプロパティは、テキスト コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>TimeFormat</td>
<td>時間が 24 時間制と午前/午後形式のどちらで表示されるかを指定します。 このプロパティは、時間コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>TimeHours</td>
<td>時間を表示するかどうかを指定します。 このプロパティは、時間コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>TimeMinutes</td>
<td>分を表示するかどうかを指定します。 このプロパティは、時間コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>TimeSeconds</td>
<td>秒を表示するかどうかを指定します。 このプロパティは、時間コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>TimeSeparator</td>
<td>時間、分、秒を分けるために使用される記号を指定します。 このプロパティは、時間コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>太さ</td>
<td>コントロールの境界線の太さを指定します。</td>
</tr>
<tr class="even">
<td>ThousandSeparator</td>
<td>1000 ごとに区切るために使用する記号を指定します。 このプロパティは、数コントロールでのみ使用できます。</td>
</tr>
<tr class="odd">
<td>上</td>
<td>コントロールの上揃えを指定します。</td>
</tr>
<tr class="even">
<td>TopMargin</td>
<td>コントロールの余白を指定します。</td>
</tr>
<tr class="odd">
<td>種類</td>
<td>表示される図形のタイプを指定します。 このプロパティは、シェイプ コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>TypeHeaderPrompt</td>
<td>コントロール タイトルとコントロール値の間にスペースを入力するために点線を追加するかどうかを指定します。 このプロパティは、テキストおよび確認でのみ使用できます。</td>
</tr>
<tr class="odd">
<td>下線</td>
<td>下線付きのテキストの書式設定を指定します。</td>
</tr>
<tr class="even">
<td>表示</td>
<td>コントロールが表示されるかどうかを示す値を設定するか返します。 <strong>True</strong> の値は、コントロールが表示されていることを示します。</td>
</tr>
<tr class="odd">
<td>WarnIfMissing</td>
<td>イメージがレポートに表示されない場合にメッセージを表示するかどうかを指定します。 このプロパティは、ビットマップ コントロールでのみ使用できます。</td>
</tr>
<tr class="even">
<td>WebMenuItemName</td>
<td>Web メニューに含めるメニュー項目を指定します。 使用可能な値は、<strong>WebMenuItemType</strong> プロパティの設定によって異なります。</td>
</tr>
<tr class="odd">
<td>WebMenuItemType</td>
<td>メニュー項目のタイプを指定します。 Web メニュー項目には 2 つのカテゴリがあります。
<ul>
<li>URL</li>
<li>アクション</li>
</ul>
選択した値によって、<strong>WebMenuItemName</strong> プロパティで使用可能な Web メニュー項目名が決まります。</td>
</tr>
<tr class="even">
<td>WebTarget</td>
<td>Web レポートのコントロールの場所を指定します。</td>
</tr>
<tr class="odd">
<td>幅</td>
<td>コントロールの幅を指定します。 コントロールが EDTに関連付けられている場合、その <strong>Width</strong> プロパティは EDT の <strong>DisplayLength</strong> プロパティを上書きします。 ビットマップ コントロールの <strong>Width</strong> プロパティを<strong>自動</strong>に設定すると、コントロールのサイズは、グラフィックのサイズに基づきます。</td>
</tr>
</tbody>
</table>

## <a name="report-design-properties"></a>レポート設計プロパティ
次のテーブルでは、レポート デザイン プロパティについて説明します。

| プロパティ                                   | 説明                                                                                                                                                                              |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ArrangeMethod                              | レポート セクションのコントロールのレイアウトを指定します。                                                                                                                                 |
| ArrangeWhen                                | レポート コントロールが配置されるタイミングを指定します。                                                                                                                                               |
| BottomMargin                               | 下部の余白を指定します。 このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                           |
| キャプション                                    | ユーザー インターフェイスのレポートに表示される名前を指定します。                                                                                                                     |
| ColorScheme                                | カラー パレットを指定します。                                                                                                                                                               |
| 列                                    | 列の数を指定します。                                                                                                                                                           |
| ColumnSpace                                | 列の間のスペースを指定します。                                                                                                                                                       |
| フォント、フォントサイズ、斜体、下線および太字 | テキストの書式設定を指定します。 **ツール** メニューの **Options** &gt; **Fonts** をクリックすることで、**Font** プロパティおよび **FontSize** プロパティの設定は、設定する値を上書きできます。 |
| ForegroundColor                            | 前景色を指定します。                                                                                                                                                            |
| 高さ                                     | 高さを指定します。                                                                                                                                                                      |
| LeftMargin                                 | 左余白を指定します。 このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                             |
| LineAbove                                  | セクションの上の境界線の線のタイプを指定します。 レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。                                       |
| LineBelow                                  | セクションの下の境界線の線のタイプを指定します。 レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。                                    |
| LineLeft                                   | セクションの左の境界線の線のタイプを指定します。 レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。                                      |
| LineRight                                  | セクションの右の境界線の線のタイプを指定します。 レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。                                     |
| ResolutionX、ResolutionY                   | グリッド線間の間隔を指定します。                                                                                                                                                  |
| RightMargin                                | 右余白を指定します。 このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                            |
| ルーラー                                      | デザインを編集するときに表示されるルーラーの単位を指定します。 デザインを編集するには、**AutoDesignSpecs** または**生成されたデザイン** を右クリックし、**編集** をクリックします。                 |
| 太さ                                  | セクションの境界線の太さを指定します。                                                                                                                                               |
| TopMargin                                  | 上余白を指定します。 このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                              |

## <a name="report-design-section-properties"></a>レポート設計セクション プロパティ
次のテーブルでは、レポート デザイン セクションのプロパティについて説明します。 レポートのデザインに使用される追加のプロパティの詳細については、「レポートのデザインのプロパティ」セクションを参照してください。


|                 プロパティ                  |                                                                                                                                                                        説明                                                                                                                                                                        |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|               ArrangeMethod               |                                                                                                                                                 レポート セクションのコントロールのレイアウトを指定します。                                                                                                                                                  |
|                ArrangeWhen                |                                                                                        コンテナーのコントロールを配置するタイミングを指定します。 <strong>スタートアップ</strong>、<strong>オンデマンド</strong>、または <strong>なし</strong> を選択できます。                                                                                         |
|                   太字                    |                                                                                                                                       コントロールにテキストを表示するのに使用されたフォントの重量を取得または設定します。                                                                                                                                        |
|                  下                   |                                                                                                                                                     レポートの下部の位置を変更します。                                                                                                                                                      |
|               BottomMargin                |                                                                                                   下部の余白を指定します。 このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                                                                    |
|                ColorScheme                |                                                                                                                                                                カラー パレットを指定します。                                                                                                                                                                 |
|          ColumnHeadingsStrategy           | 列見出しのレイアウトを指定します。 このプロパティを <strong>WordWrap</strong> と設定すると、見出しは列の最長フィールドよりも長い場合にラップします。 ヘッダーは、最大 8 つの明細行までラップできます。 8 つの明細行より長いヘッダーは切り詰められます。 <strong>注記:</strong> 言語によって、ヘッダーの長さが異なります。 |
|                  列                  |                                                                                                                                                              列の数を指定します。                                                                                                                                                               |
|                Columnspace                |                                                                                                                                                            列の間のスペースを指定します。                                                                                                                                                             |
|                   フォント                    |                                                       テキストの書式設定を指定します。 <strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。                                                        |
|                 フォントサイズ                  |                                                       テキストの書式設定を指定します。 <strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。                                                        |
|              ForegroundColor              |                                                                                                                                                               前景色を指定します。                                                                                                                                                               |
|                GrandHeader                |                                                                          <strong>HeaderText</strong> プロパティの値が表示されるかどうかを指定します。 <strong>GrandHeader</strong> プロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。                                                                          |
|                GrandTotal                 |                                                                          <strong>FooterText</strong> プロパティの値が表示されるかどうかを指定します。 <strong>GrandTotal</strong> プロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。                                                                           |
|                HeaderText                 |                                                       <strong>GrandHeader</strong> プロパティが <strong>Yes</strong> に設定されているとき、セクションの最初のレコードの上に表示されるテキストを指定します。 このプロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。                                                       |
|                  高さ                   |                                                                                                                                                                    高さを指定します。                                                                                                                                                                    |
|                  斜体                   |                                                       テキストの書式設定を指定します。 <strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。                                                        |
|     LabelTopMargin、LabelBottomMargin     |                                                                                                                                                   列見出しの上下にある余白を指定します。                                                                                                                                                    |
|                LeftMargin                 |                                                                                                    左余白を指定します。 このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                                                                     |
| LineAbove、LineBelow、LineLeft、LineRight |                                                                                                          セクション境界線の線のタイプを指定します。 レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。                                                                                                          |
|                    マップ                    |                                                                   データの表示に使用するマップを指定します。 マップ フィールドを 1 つまたは複数のテーブル内のフィールドに関連付けることができます。 このプロパティを使用すると、同じフィールド名を使用して、異なるテーブルの異なる名前を持つフィールドにアクセスできます。                                                                   |
|             NoOfHeadingLines              |                                         列見出しを表示するために使用される行数を指定します。 プロパティを <strong>0</strong> (ゼロ) に設定すると、列のヘッダーは表示されません。 いくつかのフィールドを含むレポートでは、すべてのフィールドが表示されていることを確認する行の数を増やします。                                          |
|                RightMargin                |                                                                                                    右余白を指定します。 このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                                                                    |
|                ResolutionX                |                                                                                                                                                          グリッド線間の間隔を指定します。                                                                                                                                                          |
|                ResolutionY                |                                                                                                                                                          グリッド線間の間隔を指定します。                                                                                                                                                          |
|                   ルーラー                   |                                                                      デザインを編集するときに表示されるルーラーの単位を指定します。 デザインを編集するには、<strong>AutoDesignSpecs</strong> または<strong>生成された</strong>デザイン を右クリックし、<strong>編集</strong> をクリックします。                                                                      |
|                   テーブル                   |                                                                                                                                                          セクションのソース タイプを指定します。                                                                                                                                                           |
|                 太さ                 |                                                                                                                                                        セクションの境界線の太さを指定します。                                                                                                                                                         |
|                    上                    |                                                                                                                                                       レポートの上部の位置を変更します。                                                                                                                                                       |
|                 TopMargin                 |                                                                                                     上余白を指定します。 このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。                                                                                                     |
|                 下線                 |                                                       テキストの書式設定を指定します。 <strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。                                                        |

## <a name="report-query-properties"></a>レポート クエリ プロパティ
次のテーブルでは、レポート クエリのプロパティについて説明します。 追加のレポート プロパティの詳細については、「レポート プロパティ」および「システムと共通プロパティ」セクションを参照してください。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowCheck</td>
<td>チェック フラグの許可を取得または設定します。</td>
</tr>
<tr class="even">
<td>AllowCrossCompany</td>
<td>会社間フラグの許可を取得または設定します。 このフラグは、クエリの実行が企業間で行われるかどうかを示します。</td>
</tr>
<tr class="odd">
<td>説明</td>
<td>クエリのテキストの説明。 このオプションのプロパティは、Office アドイン シナリオでよく使用されます。</td>
</tr>
<tr class="even">
<td>フォーム</td>
<td>ユーザーの操作に使用されるフォームを指定します。</td>
</tr>
<tr class="odd">
<td>対話型</td>
<td>ユーザーがクエリを区切る、プリンター オプションを設定するなどして、レポートを操作できるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>リテラル</td>
<td>SQL ステートメントでリテラルがどのような方法で表示されるかを指定します。</td>
</tr>
<tr class="odd">
<td>モデル</td>
<td>レポート クエリがあるモデルを指定します。 モデルは、レイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 他の層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="even">
<td>QueryType</td>
<td>クエリのタイプを指定します。  次のオプションを使用できます。
<ul>
<li>結合</li>
<li>結合</li>
</ul>
既定値は <strong>結合</strong> です。</td>
</tr>
<tr class="odd">
<td>検索可能</td>
<td>SharePoint Business Catalog を検索するために使用できる一連のクエリの一部としてクエリを使用できるかどうかを指定します。 このプロパティは、エンタープライズ検索機能を使用する場合に便利です。 既定値は <strong>いいえ</strong> です。</td>
</tr>
<tr class="even">
<td>肩書き</td>
<td>クエリのタイトルを指定します。</td>
</tr>
<tr class="odd">
<td>UserUpdate</td>
<td>ユーザーがクエリを更新できるかどうかを指定します。</td>
</tr>
<tr class="even">
<td>バージョン</td>
<td>これは、読み取り専用の内部プロパティです。</td>
</tr>
</tbody>
</table>

## <a name="security-code-permission-properties"></a>セキュリティ コードに対するアクセス許可のプロパティ
コード アクセス許可は、メニュー項目またはサービス操作に関連付けられたアクセス許可のグループです。 セキュリティ ロールでメニュー項目にアクセスできるときは、そのロールで、そのメニュー項目に対してコードのアクセス許可の範囲内で記載された他のアプリケーション エクスプ ローラーの品目にもアクセスできます。 アクセスの程度は、コード許可ノードで定義されている特定のアクセス許可によって制御されます。

### <a name="securable-objects"></a>セキュリティ設定が可能なオブジェクト

コードに対するアクセス許可は、セキュリティ保護可能なオブジェクトへのアクセス許可の付与に使用されます。 次のリストは、アプリケーション エクスプローラーのコード アクセス許可の階層を示しています。

-   セキュリティ
    -   コードに対するアクセス許可
        -   YourCodePermission
            -   テーブル
            -   サーバー メソッド
            -   関連付けられたオブジェクト
                -   フォーム
                -   Web コントロール
                -   レポート

コード権限は、**関連付けられたオブジェクト** ノードの下でセキュリティ保護可能なオブジェクトへのアクセス レベルを上書きすることもできます。

### <a name="code-permission-properties"></a>コードに対するアクセス許可のプロパティ

次の表は、Application Explorer の**セキュリティ** &gt; **コード パーミッション** &gt; **YourCodePermission** のノードのプロパティを示しています。

| プロパティ | 要求済み | 説明                                                                                                                        |
|----------|----------|------------------------------------------------------------------------------------------------------------------------------------|
| 氏名     | 有      | コードに対するアクセス許可の名前。 コードのアクセス許可を使用すると、**メソッド** プロパティで指定されたクラス メソッドを実行できます。 |
| クラス    | オプション | このコードに対するアクセス許可に関連付けられているクラス。                                                                            |
| 方法   | オプション | このコードに対するアクセス許可に関連付けられているメソッド。                                                                           |

### <a name="table-properties"></a>表のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **テーブル** &gt; **YourTable** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>テーブル</td>
<td>有</td>
<td>テーブルの名前。</td>
</tr>
<tr class="even">
<td>EffectiveAccess</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</td>
</tr>
<tr class="odd">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="server-method-properties"></a>サーバー メソッド プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Server Methods** &gt; **YourServerMethod** でのノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>クラス</td>
<td>有</td>
<td>サーバー クラスの名前。</td>
</tr>
<tr class="even">
<td>方法</td>
<td>有</td>
<td><strong>SysEntryPointAttribute</strong> 属性でタグ付けされた安全なサーバー メソッド。</td>
</tr>
<tr class="odd">
<td>EffectiveAccess</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</li>
<li><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</li>
</ul></td>
</tr>
<tr class="even">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="form-properties"></a>フォーム プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **関連付けられたオブジェクト** &gt; **フォーム** &gt; **YourForm** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>フォーム</td>
<td>有</td>
<td>フォームの名前。</td>
</tr>
<tr class="even">
<td>AccessLevel</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、フォームに対するすべてのアクセスを禁止することができます。</td>
</tr>
<tr class="odd">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="web-control-properties"></a>Web コントロールのプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **関連付けられたオブジェクト** &gt; **Web コントロール** &gt; **YourWebControl** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WebControl</td>
<td>有</td>
<td>Web コントロールの名前。</td>
</tr>
<tr class="even">
<td>AccessLevel</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、Web コントロールに対するすべてのアクセスを禁止することができます。</td>
</tr>
<tr class="odd">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="report-properties"></a>レポート プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **関連付けられたオブジェクト** &gt; **レポート** &gt; **YourReport** のノードのプロパティについて説明します。

| プロパティ  | 要求済み | 説明                                |
|-----------|----------|--------------------------------------------|
| 氏名      | 有      | レポート デザインの名前。             |
| レポート     | 有      | レポートのフル ネーム。               |
| ManagedBy | オプション | このプロパティは、自動化ツールで使用されます。 |

## <a name="security-duty-properties"></a>セキュリティ職務権限のプロパティ
セキュリティ アクセス許可は特権に、特権は職務に組み込まれています。 職務は、ユーザーに特定のビジネス機能へのアクセスを提供する関連特権のグループとして定義されます。 アプリケーション エクスプローラーでは、これらの権限は職務権限のノードにまとめられます。

### <a name="best-practices"></a>ベスト プラクティス

このセクションでは、職務のベスト プラクティス ルールについて説明します。

-   すべての職務はロールに割り当てられるべきです。
-   すべての職務はプロセス サイクルの一部であるべきです。
-   職務権限は特定のビジネス機能を表すため、職務権限の名前はほとんど変わりません。 たとえば、会社が請求の支払いをします。 請求書の支払方法の詳細は変更する可能性がありますが、請求書支払いの重要な機能は変更されません。 新しい職務を作成する代わりに、職務の権限サブノードを変更する必要があります。
-   プロセス サイクルの名前はほとんど変わりません。

### <a name="duty-hierarchy-in-application-explorer"></a>アプリケーション エクスプ ローラーの職務階層

次のリストは、アプリケーション エクスプローラーの職務権限のノードの階層を示しています。

-   セキュリティ
    -   職務権限
        -   YourDuty
            -   権限

### <a name="duty-properties"></a>職務プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **職務権限** &gt; **YourDuty** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>職務権限の名前。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>有</td>
<td>ユーザー インターフェイスの職務権限で表示されるテキスト。</td>
</tr>
<tr class="odd">
<td>説明</td>
<td>有</td>
<td>職務権限の説明。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - 職務権限を有効にします。</li>
<li><strong>いいえ</strong> - 職務権限を無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="privilege-properties"></a>権限のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **職務権限** &gt; **YourDuty** &gt; **権限** &gt; **YourPrivilege** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>権限の名前。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - 権限を有効にします。</li>
<li><strong>いいえ</strong> - 権限を無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="security-privilege-properties"></a>セキュリティ権限のプロパティ
権限は、アクセス許可のグループです。 各権限ノードの下にあるノードは、ユーザーがアクセスできるセキュリティ保護可能オブジェクトを識別し、各オブジェクトのアクセス レベルを設定します。

### <a name="best-practices"></a>ベスト プラクティス

このセクションでは、権限のベスト プラクティス ルールについて説明します。

-   特権を使用すると、ジョブを実行するために必要なアクセス特権を指定することができます。
-   特権を使用すると、関連するセキュリティ保護可能なオブジェクトのアクセス許可をグループ化することができます。 たとえば、メニュー項目およびそのコントロールは密接に関係しています。
-   権限はセキュリティ ロールに直接割り当てることができます。 ただし、特権ではなく職務またはプロセス サイクルを割り当てると、セキュリティ設定が管理しやすくなります。

### <a name="securable-objects"></a>セキュリティ設定が可能なオブジェクト

権限は、セキュリティ保護可能なオブジェクトへのアクセス許可の付与に使用されます。 以下のリストは、アプリケーション エクスプローラーの **セキュリティ** &gt; **特権** ノードの下の階層を示しています。

-   セキュリティ
    -   権限
        -   YourPrivilege
            -   エントリ ポイント
            -   アクセス許可
                -   テーブル
                -   サーバー メソッド
                -   フォーム

権限は、アプリケーション エクスプローラーの他の場所で定義されているとおりに、セキュリティ保護可能なオブジェクトへのアクセス レベルを上書きすることができます。 たとえば、権限は、アプリケーション エクスプローラーの**フォーム** &gt; **YourForm** &gt; **アクセス許可** &gt; **更新** &gt; **テーブル** &gt; **YourTable** の下で、**EffectiveAccess** プロパティにより定義されるアクセス許可を上書きできます。

### <a name="privilege-properties"></a>権限のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>権限の名前。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>有</td>
<td>ユーザー インターフェイスの権限で表示されるテキスト。</td>
</tr>
<tr class="odd">
<td>説明</td>
<td>有</td>
<td>権限の説明。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - 権限を有効にします。</li>
<li><strong>いいえ</strong> - 権限を無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="entry-point-properties"></a>エントリ ポイント プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **エントリ** **ポイント** &gt; **YourEntryPoint** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>エントリ ポイントの名前。</td>
</tr>
<tr class="even">
<td>ObjectType</td>
<td>有</td>
<td>エントリ ポイントのオブジェクト タイプ。  次のオプションを使用できます。
<ul>
<li>MenuItemDisplay</li>
<li>MenuItemOutput</li>
<li>MenuItemAction</li>
<li>ServiceOperation</li>
<li>WebActionItem</li>
<li>WebURLItem</li>
<li>WebManagedContent</li>
</ul></td>
</tr>
<tr class="odd">
<td>ObjectName</td>
<td>有</td>
<td>エントリ ポイントのオブジェクト名。</td>
</tr>
<tr class="even">
<td>ObjectChildName</td>
<td>オプション</td>
<td>サービス メソッド名を表す値。 <strong>注記:</strong> <strong>ObjectType</strong> プロパティが <strong>ServiceOperation</strong> に設定されている場合にのみ、このプロパティの値を指定します。</td>
</tr>
<tr class="odd">
<td>AccessLevel</td>
<td>有</td>
<td>アクセス許可の値。 <strong>ServiceOperation</strong> を除くすべてのオブジェクト タイプに関しては、次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>AccessLevel</strong>プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、エントリ ポイントに対するすべてのアクセスを禁止することができます。 修正アクセス許可は、時間状態テーブルが関係する場合にのみ適用されます。 このアクセス許可は、時間状態テーブルで更新レコードを発行する権限を与えます。 <strong>ServiceOperation</strong> オブジェクト タイプに関しては、次のオプションを使用できます。
<ul>
<li><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</li>
<li><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="table-properties"></a>表のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **アクセス許可** &gt; **テーブル** &gt; **YourTable** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>テーブル</td>
<td>有</td>
<td>テーブルの名前。</td>
</tr>
<tr class="even">
<td>EffectiveAccess</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 修正アクセス許可は、時間状態テーブルが関係する場合にのみ適用されます。 このアクセス許可は、時間状態テーブルのレコードを更新する権限を与えます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</td>
</tr>
<tr class="odd">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="server-method-properties"></a>サーバー メソッド プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **アクセス許可** &gt; **サーバー メソッド** &gt; **YourServerMethod** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>クラス</td>
<td>有</td>
<td>サーバー クラスの名前。</td>
</tr>
<tr class="even">
<td>方法</td>
<td>有</td>
<td><strong>SysEntryPointAttribute</strong> 属性でタグ付けされた安全なサーバー メソッドの名前。</td>
</tr>
<tr class="odd">
<td>EffectiveAccess</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</li>
<li><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</li>
</ul></td>
</tr>
<tr class="even">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="form-properties"></a>フォーム プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **アクセス許可** &gt; **フォーム** &gt; **YourForm** のノードのプロパティについて説明します。

| プロパティ | 要求済み | 説明           |
|----------|----------|-----------------------|
| フォーム     | 有      | フォームの名前。 |

## <a name="security-process-cycle-properties"></a>セキュリティ プロセス サイクル プロパティ
プロセス サイクルは、職務のグループです。 プロセス サイクルは、高度なジョブ機能を表します。 特定のジョブ機能を実行する詳細については時間の経過とともに変化しますが、概念とそのジョブ機能の名前はおそらく変化しません。

### <a name="best-practices"></a>ベスト プラクティス

このセクションでは、プロセス サイクルのベスト プラクティス ルールについて説明します。

-   各職務権限は、プロセス サイクルの一部である必要があります
-   プロセス サイクルを使用して、ジョブ機能の職務のグループを編成します。

### <a name="process-cycle-hierarchy-in-application-explorer"></a>アプリケーション エクスプローラーのプロセス サイクル

次のリストは、アプリケーション エクスプローラーのプロセス サイクル ノードの階層を示しています。

-   セキュリティ
    -   プロセス サイクル
        -   YourProcessCycle
            -   職務権限

### <a name="process-cycle-properties"></a>サイクル プロパティの処理

T次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **プロセス** **サイクル** &gt; **YourProcessCycle** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>プロセス サイクルの名前。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>有</td>
<td>ユーザー インターフェイスのプロセス サイクルで表示されるテキスト。</td>
</tr>
<tr class="odd">
<td>説明</td>
<td>有</td>
<td>プロセス サイクルの説明。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - プロセス サイクルを有効にします。</li>
<li><strong>いいえ</strong> - プロセス サイクルを無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="duty-properties"></a>職務プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **プロセス サイクル** &gt; **YourProcessCycle** &gt; **職務権限** &gt; **YourDuty** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>職務権限の名前。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - 職務権限を有効にします。</li>
<li><strong>いいえ</strong> - 職務権限を無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="security-policy-properties"></a>セキュリティ ポリシーのプロパティ
開発者およびシステム管理者は、テーブル内のデータ レコードのサブセットへのアクセスを拒否するセキュリティ ポリシーを作成できます。

### <a name="constrained-tables-of-a-policy"></a>ポリシーの制約付きテーブル

アプリケーション エクスプローラー内のセキュリティ ポリシーの **制限付きテーブル** ノードの下に、テーブルおよびビューを追加することができます。 これらのテーブルとビューは、ポリシーの **Query** プロパティに名前が付けられたクエリのデータ ソース テーブルに関連しています。 次のリストは、アプリケーション エクスプローラーのセキュリティ ポリシーの階層を示しています。

-   セキュリティ
    -   ポリシー
        -   YourPolicy
            -   制約付きテーブル
                -   YourConstrainedTable
                    -   YourConstrainedSubTable
                -   YourConstrainedView

各**制約付きテーブル**ノードは、制約されたテーブルおよびビューの任意の数を含むことができます。 また、各制約付きテーブルは、制約付きサブテーブルの任意の数を含むことができます。

### <a name="security-policy-properties"></a>セキュリティ ポリシーのプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ポリシー** &gt; **YourPolicy** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>セキュリティ ポリシーの名前。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>有</td>
<td>ユーザー インターフェイスのセキュリティ ポリシーで表示されるテキスト。</td>
</tr>
<tr class="odd">
<td>PrimaryTable</td>
<td>有</td>
<td>セキュリティ ポリシー クエリのデータ ソースで指定されているテーブル。</td>
</tr>
<tr class="even">
<td>クエリ</td>
<td>有</td>
<td>ポリシーで指定された制約付きテーブルからデータをフィルタリングするためにポリシーが使用するクエリ。</td>
</tr>
<tr class="odd">
<td>UseNotExistJoin</td>
<td>有</td>
<td>セキュリティ クエリを<strong>存在しない</strong>結合または<strong>存在する</strong>結合として適用する必要があるかどうかを示す値。</td>
</tr>
<tr class="even">
<td>PolicyGroup</td>
<td>無</td>
<td>管理者と開発者は、このプロパティを使用して、関連するセキュリティ ポリシーのグループをすばやく識別できます。 システム管理者または開発者が作成したセキュリティ ポリシー グループの名前のいずれかを選択できます。 実行時にこのプロパティは使用されません。</td>
</tr>
<tr class="odd">
<td>ConstrainedTable</td>
<td>有</td>
<td>セキュリティ ポリシーが主テーブルから返されるレコードのデータ値を制限するかどうかをコントロールする値。  次のオプションを使用できます。
<ul>
<li><strong>はい  </strong>- セキュリティ ポリシーはプライマリ テーブルには適用されます。</li>
<li><strong>いいえ</strong> - セキュリティ ポリシーはプライマリ テーブルには適用されません。</li>
</ul></td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>システムが実行時間に、ポリシーを適用するかどうかをコントロールする値。  次のオプションを使用できます。
<ul>
<li><strong>はい  </strong>- セキュリティ ポリシーを有効にします。</li>
<li><strong>いいえ </strong> - セキュリティ ポリシーを無効にします。</li>
</ul></td>
</tr>
<tr class="odd">
<td>工程</td>
<td>有</td>
<td>ポリシーが適用されるデータ操作をコントロールする値。  次のオプションを使用できます。
<ul>
<li>選択</li>
<li>挿入</li>
<li>更新</li>
<li>消去</li>
<li>挿入、更新、削除</li>
<li>すべての工程</li>
</ul></td>
</tr>
<tr class="even">
<td>ContextType</td>
<td>有</td>
<td>セキュリティ ポリシーのコンテキスト タイプをコントロールする値。  次のオプションを使用できます。
<ul>
<li><strong>ContextString </strong> - <strong>ContextString</strong> プロパティの値を指定する必要があります。 セキュリティ ポリシーは、ポリシーに特定のアプリケーション コンテキストを使用します。</li>
<li><strong>RoleName  </strong>- セキュリティ ポリシーは、<strong>RoleName</strong> の値に割り当てられているアプリケーション ユーザーにのみ適用されます。</li>
<li><strong>RoleProperty  </strong>- この値は、<strong>ContextString</strong> と組み合わせて使用され、複数のロール コンテキストを指定します。</li>
</ul></td>
</tr>
<tr class="odd">
<td>ContextString</td>
<td>有</td>
<td>このプロパティは、<strong>ContextType</strong> プロパティと組み合わせて使用されます。 アプリケーションまたは複数のロール コンテキストを指定するために使用できます。</td>
</tr>
</tbody>
</table>

## <a name="security-role-properties"></a>セキュリティ ロールのプロパティ
ロールは、ユーザーに付与できるアクセス許可のコレクションを表します。 各ロール ノードの下にある入れ子になったノードは、ユーザーがアクセスできるさまざまなセキュリティ保護可能オブジェクトを識別し、各アクセス レベルを指定します。

### <a name="role-node-in-application-explorer"></a>アプリケーション エクスプローラーでのロール ノード

ロールは、セキュリティ保護可能なオブジェクトへのアクセス許可の付与に使用されます。 次のリストは、アプリケーション エクスプローラーのロール ノードの階層を示しています。

-   セキュリティ
    -   ロール
        -   YourRole
            -   職務権限
            -   権限
            -   アクセス許可
                -   テーブル
                -   フォーム
                -   サーバー メソッド
            -   サブロール

ロールは通常、セキュリティ税、および場合によってはセキュリティ権限に関連付けられます。 ロール内のセキュリティ保護可能なオブジェクトへのアクセス レベルは、職務、権限、またはその両方から派生します。 ロールは、**アクセス許可** ノードの下でセキュリティ保護可能なオブジェクトへのアクセス レベルを上書きすることもできます。

### <a name="role-properties"></a>役割のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **YourRole** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>ロールの名前。</td>
</tr>
<tr class="even">
<td>ラベル</td>
<td>有</td>
<td>ユーザー インターフェイスのロールで表示されるテキスト。</td>
</tr>
<tr class="odd">
<td>説明</td>
<td>有</td>
<td>ロールの説明。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - ロールを有効にします。</li>
<li><strong>いいえ</strong> - ロールを無効にします。</li>
</ul></td>
</tr>
<tr class="odd">
<td>PastDataAccess</td>
<td>有</td>
<td>有効日フィールドのあるテーブルの過去のデータ アクセス。  次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>PastDataAccess</strong> プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</td>
</tr>
<tr class="even">
<td>CurrentDataAccess</td>
<td>有</td>
<td>有効日フィールドのあるテーブルの現在のデータ アクセス。</td>
</tr>
<tr class="odd">
<td>FutureDataAccess</td>
<td>有</td>
<td>有効日フィールドのあるテーブルの将来のデータ アクセス。</td>
</tr>
<tr class="even">
<td>ContextString</td>
<td>オプション</td>
<td>セキュリティ ポリシーによって使用できるユーザー定義の文字列。</td>
</tr>
</tbody>
</table>

### <a name="duty-properties"></a>職務プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **職務権限** &gt; **YourDuty** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>職務権限の名前。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - 職務権限を有効にします。</li>
<li><strong>いいえ</strong> - 職務権限を無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="privilege-properties"></a>権限のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **YourPrivilege** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>権限の名前。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - 権限を有効にします。</li>
<li><strong>いいえ</strong> - 権限を無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="table-properties"></a>表のプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **テーブル** &gt; **YourTable** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>テーブル</td>
<td>有</td>
<td>テーブルの名前。</td>
</tr>
<tr class="even">
<td>EffectiveAccess</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li>既読</li>
<li>更新</li>
<li>新規</li>
<li>修正</li>
<li>消去</li>
<li>NoAccess</li>
</ul>
<strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。 読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。 削除のアクセス許可には他のすべての権限が含まれます。 アクセス許可には、更新と読み取りが含まれます。 アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</td>
</tr>
<tr class="odd">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="form-properties"></a>フォーム プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **フォーム** &gt; **YourForm** のノードのプロパティについて説明します。

| プロパティ | 要求済み | 説明           |
|----------|----------|-----------------------|
| フォーム     | 有      | フォームの名前。 |

### <a name="server-method-properties"></a>サーバー メソッド プロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **サーバー メソッド** &gt; **YourServerMethod** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>クラス</td>
<td>有</td>
<td>サーバー クラスの名前。</td>
</tr>
<tr class="even">
<td>方法</td>
<td>有</td>
<td><strong>SysEntryPointAttribute</strong> 属性でタグ付けされた安全なサーバー メソッドの名前。</td>
</tr>
<tr class="odd">
<td>EffectiveAccess</td>
<td>有</td>
<td>アクセス許可の値。  次のオプションを使用できます。
<ul>
<li><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</li>
<li><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</li>
</ul></td>
</tr>
<tr class="even">
<td>ManagedBy</td>
<td>オプション</td>
<td>このプロパティは、自動化ツールで使用されます。</td>
</tr>
</tbody>
</table>

### <a name="subrole-properties"></a>サブロールのプロパティ

次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **サブロール** &gt; **YourSubRole** のノードのプロパティについて説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>要求済み</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>氏名</td>
<td>有</td>
<td>サブロールの名前。</td>
</tr>
<tr class="even">
<td>有効</td>
<td>有</td>
<td>職務権限が有効かどうかを示す値。  次のオプションを使用できます。
<ul>
<li><strong>はい</strong> - サブロールを有効にします。</li>
<li><strong>いいえ</strong> - サブロールを無効にします。</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="web-menu-properties"></a>Web メニューのプロパティ
次のデーブルでは、Web メニューとサブメニューに固有のプロパティについて説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ConfigurationKey</td>
<td>このメニューの表示の制御に使用されるコンフィギュレーション キーを指定します。 ユーザーがコンフィギュレーション キーにアクセスできない場合は、メニューは表示されません。</td>
</tr>
<tr class="even">
<td>HighlightSelected</td>
<td>このプロパティは、サポートされていません。</td>
</tr>
<tr class="odd">
<td>ラベル</td>
<td>Web メニューまたはサブメニューの最上位レベル ノードに表示されるテキストを指定します。 値は 250 文字を超えることはできません。</td>
</tr>
<tr class="even">
<td>MenuItemName</td>
<td>メニューまたはサブメニューの最上位ノードをクリックしたときにアクセスするメニュー項目を指定します。 使用可能なオプションは、<strong>MenuItemType</strong> プロパティの設定によって異なります。</td>
</tr>
<tr class="odd">
<td>MenuItemType</td>
<td>メニューまたはサブメニューの最上位ノードによりアクセスされるメニュー項目の種類を指定します。 <strong>アクション</strong> または <strong>URL</strong> を選択できます。</td>
</tr>
<tr class="even">
<td>モデル</td>
<td>モデルを指定します。 モデルはレイヤー内の要素の論理グループです。 要素例には、テーブルまたはクラスが含まれます。 要素は、レイヤー内の 1 つのモデルに正確に存在します。 上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</td>
</tr>
<tr class="odd">
<td>SetCompany</td>
<td>このプロパティは、フォームがフォーカスを受け取ったときにシステムを変更します。 <strong>SaveDataPerCompany</strong> プロパティが <strong>はい</strong> に設定されている場合、テーブルをデータ ソースとして使用するフォーム デザインの <strong>SetCompany</strong> プロパティも <strong>はい</strong> に設定する必要があります。</td>
</tr>
<tr class="even">
<td>ShowParentModule</td>
<td>メニュー項目の親モジュールに基づいて QuickLaunch を更新するかどうかを指定します。  次のオプションを使用できます。
<ul>
<li><strong>はい  </strong>- メニュー項目の親モジュールに基づいて QuickLaunch を常に更新してください。</li>
<li><strong>いいえ </strong> - メニュー項目の親モジュールが、現在のモジュールと異なる場合でも QuickLaunch を変更せずにそのままにします。</li>
</ul>
既定値は <strong>はい</strong> です。</td>
</tr>
</tbody>
</table>

## <a name="web-menu-item-properties"></a>Web メニュー項目のプロパティ
次のデーブルでは、Web メニュー項目に固有のプロパティについて説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>プロパティ</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ビッグ</td>
<td>アクション ウィンドウに使用されるボタンのサイズを指定します。  次のオプションを使用できます。
<ul>
<li><strong>はい  </strong>- ボタンはフル サイズで表示され、グループの先頭に位置します。</li>
<li><strong>いいえ </strong> - ボタンは小さいサイズで表示され、グループの右側にあります。</li>
</ul></td>
</tr>
<tr class="even">
<td>CloseDialogBehavior</td>
<td>ダイアログ ボックスが閉じるときに親ウィンドウで実行されるアクションを指定します。  次のオプションを使用できます。
<ul>
<li><strong>自動  </strong>- ダイアログ ボックスの使用方法に応じて、適切な更新アクションが、ダイアログ ボックスが閉じたときに実行されます。</li>
<li><strong>RefreshDataSource  </strong>- 親フォーム上の読み取り専用データ ソースは更新されます。 このオプションは、現在の選択を保存し、データソースに対して <strong>Research()</strong> 操作を実行します。</li>
<li><strong>RefreshPage  </strong>- ページを更新します。</li>
<li><strong>送信  </strong>- 親ページを更新します。</li>
<li><strong>なし  </strong>- アクションは実行されません。</li>
</ul>
既定値は <strong>自動</strong> です。</td>
</tr>
<tr class="odd">
<td>HideActionPane</td>
<td>開いているページにアクション ウィンドウを表示するかどうかを指定します。</td>
</tr>
<tr class="even">
<td>ホームページ</td>
<td>ページがロール センター ページであり、メイン エンタープライズ ポータル サイトに配置されるかどうかを指定します。</td>
</tr>
<tr class="odd">
<td>NeedsRecord</td>
<td>このプロパティを<strong>はい</strong>に設定すると、データ セットにレコードがないとき、メニュー項目が表示されます。</td>
</tr>
<tr class="even">
<td>PageDefinition</td>
<td>Web メニュー項目が指し示すページ。</td>
</tr>
<tr class="odd">
<td>パラメーター</td>
<td>開いているページに渡される引数を指定します。 各パラメーターは以下のフォーム<em>名前</em>=<em>値</em>を必要とします。また複数のパラメーターを渡す場合、次の例に示すように、アンパサンド (&amp;) で区切らなくてはなりません。例: mode=2&amp;category=1</td>
</tr>
<tr class="even">
<td>URL</td>
<td>移動先の URL を指定します。</td>
</tr>
<tr class="odd">
<td>WebConfigurationKey</td>
<td>Web メニュー項目を有効にするために必要なコンフィギュレーション キーを選択します。 オブジェクトが属しているモジュールのキーを使用します。</td>
</tr>
<tr class="even">
<td>WindowMode</td>
<td>開いているページに使用するウィンドウのタイプを指定します。  次のオプションを使用できます。
<ul>
<li><strong>インライン </strong> - 開いているページは、ブラウザの既存の内容に置き換えられます。 Web メニュー項目にダイアログ ボックスからアクセスしている場合、新しいブラウザー ウィンドウで開くページが開きます。</li>
<li><strong>モーダル </strong> - 開いているダイアログ ボックスがない場合は、新しいダイアログ ボックスが作成されます。 Web メニュー項目にダイアログ ボックスからアクセスしている場合、現在のダイアログ ボックスのコンテンツが開いているページに置き換えられます。</li>
<li><strong>NewModal </strong> - 開いているページは常に新しいダイアログ ボックスで開きます。</li>
<li><strong>NewWindow </strong> - 開いているページは新しいブラウザー ウィンドウで開きます。</li>
</ul></td>
</tr>
<tr class="odd">
<td>WindowParameters</td>
<td>SharePoint ダイアログ ボックスの外観を制御する追加のパラメーターを指定します。 パラメータは、かっこ ({}) で囲み、コンマで区切る必要があります。 次の例は、ダイアログボックスのサイズが 400 × 300 ピクセルになり、<strong>閉じる</strong>ボタンまたは<strong>最大化</strong>ボタンが表示されるように <strong>WindowParameters</strong> プロパティを設定する方法を示しています。{width:400, height:300, showClose:false, allowMaximize:false}</td>
</tr>
<tr class="even">
<td>WindowSize</td>
<td>開いているページに使用するウィンドウのサイズを指定します。  次のオプションを使用できます。
<ul>
<li><strong>最小 </strong>– 330 × 200 ピクセル</li>
<li><strong>小 </strong>– 550 × 450 ピクセル</li>
<li><strong>中 </strong>– 800 × 630 ピクセル</li>
<li><strong>大 </strong>– 930 × 630 ピクセル</li>
<li><strong>最大 </strong> - メインのブラウザー ウィンドウの境界内に収まる最大のサイズ</li>
</ul></td>
</tr>
</tbody>
</table>






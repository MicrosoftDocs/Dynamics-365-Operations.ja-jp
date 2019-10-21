---
title: 拡張機能とオーバーレイによってカスタマイズする
description: このトピックでは、モデル要素のソース コードとメタ データをカスタマイズするオーバーレイと拡張機能の 2 つの方法、およびサポートされている拡張機能の詳細について説明します。
author: robadawy
manager: AnnBe
ms.date: 09/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 26961
ms.assetid: 8a2b3107-247d-4362-8d4d-6ee6257abfcc
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8efbfb8e70c9051bb67233ec8d683ea1ba7ece9b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191648"
---
# <a name="customize-through-extension-and-overlayering"></a>拡張機能とオーバーレイによってカスタマイズする

[!include [banner](../includes/banner.md)]

このトピックでは、モデル要素のソース コードとメタ データをカスタマイズするオーバーレイと拡張機能の 2 つの方法、およびサポートされている拡張機能の詳細について説明します。

## <a name="overlayering"></a>オーバーレイヤー

Microsoft またはサードパーティの Microsoft パートナーによって出荷されている、モデル要素のソース コードとメタデータをカスタマイズできます。 モデルのメタデータとソース コードをカスタマイズするために、開発者はカスタマイズするモデルにオーバーレイする新しいモデルを作成する必要があります。 たとえば、ソリューション開発者は SLN レイヤーでコードを提供でき、独立系ソフトウェア ベンダーは ISV レイヤーを使用でき、さらにますおよび付加価値再販業者は VAR レイヤーを使用することができます。 上部レイヤ (この例では VAR レイヤ) で定義された機能は、下部レイヤの機能を上書きできます。 オーバーレイ モデルはソース モデルと同じ **パッケージ**に属し、ソース モデルよりも高いレイヤーに属している必要があります。 オーバーレイヤーは、メタデータとソース コードの高度なカスタマイズを実行する強力なツールですが、ソリューションを新しいバージョンにアップグレードする費用が高くなる場合があります。 

<!--Click on this [link](https://mix.office.com/watch/1ol6ov90jrd4w) to open an Office Mix that provides a good introduction on how to customize model elements.-->

## <a name="extensions"></a>拡張子
*拡張機能* を使用することにより、アプリケーションをカスタマイズすることができます。 拡張子により既存のモデル要素およびソース コードに機能を追加できます。 拡張子は、次の機能を提供します。

-   新しいモデル要素を作成しています。
-   既存のモデル要素を拡張します。
-   クラスの拡張子を使用して、ソース コードを拡張します。
-   ビジネス ロジックのカスタマイズ。 ビジネス ロジックをカスタマイズする方法に以下の内容が含まれます。
    -   データ イベントなどのフレームワーク イベントに応答するイベント ハンドラーを作成しています。
    -   アプリケーションで定義されているイベントの委任に応答するイベント ハンドラーを作成しています。
    -   新しいプラグインを作成しています。

開始するには、[[拡張機能を使用してモデル要素をカスタマイズする](customize-model-elements-extensions.md)] チュートリアルを確認するか完了してください。

## <a name="extension-models-and-packages"></a>拡張モデルおよびパッケージ
新しいモデル要素、新しいコード、または拡張機能のみを含むモデルを作成することができます。 このモデルは独自の独立したアセンブリにコンパイルされます。 これらのアセンブリは、関連するメタデータおよびランタイム コンポーネントと一緒に (展開可能なパッケージ ファイルとして) パッケージ化し、ランタイム サンドボックスまたは実稼働環境に展開することができます。 拡張モデルを作成するには、モデルの作成ウィザードを開き、2番目のステップで **新しいパッケージを作成** を選択します。 

![./media/1_cust.png](./media/1_cust.png) 

拡張モデルの使用には、以下を含むいくつかの利点があります。

-   **アプリケーション ライフサイクル管理 (ALM):** 拡張モデルは、配置、ビルド、テストの自動化、および顧客への配信のパフォーマンスを簡素化し、向上させます。
-   **デザイン時間業績:** モデルやプロジェクトを構築しても、アプリケーション全体を再コンパイルする必要はありません。
-   **サービス:** クラウド上で Microsoft はユーザーのカスタマイズに影響を与えずに、インストール、パッチ、アップグレード、および内部 APIs の変更を行えます。
-   **アップグレード:** オーバレイヤーとは異なり、拡張機能が新しいバージョンにアップグレードするコストを削減し、同時にこのアプローチによりコストのかかるコードとメタデータの競合を排除します。

次の図は、拡張がアセンブリでどのように分離されるかを示しています。 

![media/ax7customization1.png](media/ax7customization1.png)

## <a name="code-extensions"></a>コードの拡張子
3 つの方法でソース コードを拡張することができます。

-   イベント (フレームワーク イベントおよびデリゲート) をサブスクライブすることにより
-   プラグインを書き込むことによって。
-   クラスの拡張機能 (別名、クラス強化) を作成して、以下のセクションを参照してください。

フレームワーク イベントの以下の特性を理解する必要があります。

-   イベントは、マルチキャスト デリゲートとして実装されます。つまり、複数のイベント ハンドラーを特定のイベントにサブスクライブすることができます。
-   イベントはブロードキャストされます。イベント ハンドラーへの呼び出しの優先順位はありません。
-   基準メソッドのトランザクション スコープ内で、イベント ハンドラーを実行します。

### <a name="events"></a>イベント

イベントは、基本メソッドの前後の操作として生成されます。 つまり、基本メソッドが呼び出される前と完了後にコードを実行する機会があります。 Microsoft Dynamics AX 2012 で XPP イベントが導入されました。このイベントは、今回のリリースでも使用でき、拡張機能でサブスクライブできます。

### <a name="plug-ins"></a>プラグイン

プラグインは、基本アプリケーションで定義されている拡張ポイントです。 クラス ファクトリ パターンを使用することにより、プラグインでは基本機能を置き換えることができます。 プラグインの実装方法については、チュートリアル [拡張機能を使用してモデル要素をカスタマイズする](customize-model-elements-extensions.md) を参照してください。

### <a name="class-extensions"></a>クラスの拡張機能

クラスの拡張機能を使用すると、既存のクラス、テーブル、フォームにメソッドや変数を追加して、クラスを拡張することができます。 詳細については、トピック [クラスの拡張機能](class-extensions.md) を参照してください。

## <a name="form-extensions"></a>フォーム拡張子
コントロールおよびデータ ソースを拡張することにより、フォームの機能を拡張することができます。 たとえば、フォーム拡張子で、以下の点を実行できます。

-   新しいコントロールを追加します。
-   コントロールを有効または無効にします。
-   コントロールのテキストまたはラベルのプロパティを変更します。
-   コントロールの可視性を変更します。
-   フォームのヘルプ テキストを変更します。
-   フォームのキャプションを変更します。
-   新しいデータ ソースを追加します。
-   フォーム パーツを追加します。

フォームでコントロールを並べ替えるなど、フォームをカスタマイズする他の方法は、将来のリリースに含まれる予定です。 Microsoft Dynamics AX 2012 では、フォーム メソッドを上書きすることができます。 現在のバージョンでは、フォーム メソッドの基本実装から呼び出されるイベント ハンドラーを実装するのに拡張機能を使用します。 次のテーブルに、各メソッドとそれに関連するイベントを示します。

|**公開済フォーム DataSource メソッド**|**前のイベント**|**後続のイベント**|
|---|---|---|
|有効|該当なし|有効化|
|削除|削除中|削除済|
|validateWrite|ValidatingWriting|ValidatedWrite|
|write|書き込み|記述済み|
|作成|作成中|作成済|
|executeQuery|該当なし|QueryExecuted|
|linkActive|該当なし|PostLinkActive|
|init|該当なし|初期化済み|
|validateDelete|ValidatingDelete|ValidatedDelete|
|reread|該当なし|再表示|
|selectionChanged|該当なし|SelectionChanged|
|markChanged|該当なし|MarkChanged|
|leaveRecord|LeavingRecord|LeftRecord|


|**公開済フォーム オブジェクト メソッド**|**前のイベント**|**後続のイベント**
|---|---|---|
|init|初期化|初期化済み
|閉じる|決算済み|該当なし
|run|該当なし|PostRun
|有効化|該当なし|有効化


|**公開済フォーム コントロール メソッド**|**前のイベント**|**後続のイベント**
|---|---|---|
|modified|該当なし|変更済
|検証|検証中|検証済み
|leave|終了|LostFocus
|入力|該当なし|入力
|gotFocus|該当なし|GotFocus
|clicked|該当なし|クリックされた
|selectionChange|SelectionChanging|該当なし
|pageActivated|該当なし|PageActivated
|allowPageDeactivate|AllowPageDeactivate|該当なし
|expand|展開|拡大
|tabChanged|該当なし|TabChanged
|dialogClosed|該当なし|DialogClosed

### <a name="code-behind-extension-forms"></a>拡張フォームの後にあるコード

クラス拡張機能を使用して、フォーム拡張機能と関連付けられた X++ ロジックを記述することができます。 これにより、イベント ハンドラーを形成および制御するためにアクセス可能な状態変数の定義が可能になります。 コードをオーバーレイせずにフォーム メソッドをオーバーライドすることもできます。 例については、[こちら](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/10/11/code-behind-extension-forms-how-to-add-state-variable-and-override-methods-without-overlayering)のブログ記事をご覧ください。

## <a name="table-extensions"></a>テーブル拡張
テーブル拡張を作成して、テーブルのデザインおよびロジックを拡張することができます。 新しいフィールド、フィールド グループ、インデックス、マップおよび関係を追加することができます。 また、既存のフィールド グループに新しいフィールドを追加して、テーブル フィールドのラベルを変更し、作成者、作成日時、修正者、修正日時のプロパティを変更することができます。 テーブル拡張機能を使用して、フィールドの拡張データ型プロパティを変更し、現在の EDT から派生した EDT にそれを設定することもできます (*これはプラットフォーム更新プログラム 8 の時点で使用可能です*)。

Microsoft Dynamics AX 2012 では、テーブルの基本クラスの仮想メソッドをオーバーライドして、作成、読み取り、更新、または削除などのテーブルの処理中に発生した動作を制御できました。 現在のバージョンでは、代わりにテーブル メソッドの基本実装から呼び出されるイベント ハンドラーを実装するのに拡張機能を使用します。 次のテーブルに、各テーブルとそれに関連するイベントを示します。

|**公開済テーブル メソッド**|**前のイベント**|**後続のイベント**|
|---|---|---|
|validateWrite|ValidatingWrite|ValidatedWrite|
|validateDelete|ValidatingDelete|ValidatedDelete|
|validateField|ValidatingField|ValidatedField|
|validateFieldValue|ValidatingFieldValue|ValidatedFieldValue|
|modifiedField|ModifyingField|ModifiedField|
|modifiedFieldValue|ModifyingFieldValue|ModifiedFieldValue|
|挿入|挿入|挿入済|
|更新|更新中|更新済|
|消去|削除中|削除済|
|Initvalue|InitializingRecord|InitializedRecord|
|FinalDeleteValidation|操作が基礎データベース テーブルにコミットされる前に、テーブル オブジェクトに対して削除操作が実行された時に実行されます。|該当なし|
|FinalInsertValidation|操作が基礎データベース テーブルにコミットされる前に、テーブル オブジェクトに対して挿入操作が実行された時に実行されます。|該当なし|
|FinalReadValidation|テーブル オブジェクトに対して、読み取り操作が行われた時に実行されます。|該当なし|
|FinalUpdateValidation|操作が基礎データベース テーブルにコミットされる前に、テーブル オブジェクトに対して更新操作が実行された時に実行されます。|該当なし|

検証イベントは、**DataEventArgs** パラメーターを使用して結果を取得して返します。 表示および編集メソッド モディファイアーは、テーブル拡張機能でサポートされています。

## <a name="view-and-data-entity-extensions"></a>表示およびデータ エンティティの拡張機能
テーブルの拡張機能で使用可能な機能の大半を実行できるように、ビューまたはデータ エンティティを拡張することができます。

## <a name="enum-extensions"></a>列挙拡張子
拡張可能とマークされている (IsExtensible=True) 任意の列挙値を拡張することができます。 

[![extensibleenums](./media/extensibleenums-300x158.png)](./media/extensibleenums.png) 

列挙型を拡張することによって、新しい列挙値を追加することができます。 拡張可能な列挙を処理するとき、次のことに留意することが重要です。

1.  たとえば、列挙値の整数値に依存する X++ ロジックを持つことはできません。 *(Enum1.v1 &gt; Enum1.v2).の場合...* は拡張可能な列挙ではサポートされていません)
2.  拡張可能な Enums の Enums 値がデータベースに同期されると、次の操作が行われます。
    -   ベースライン列挙に属している整数値は確定的であり、メタデータから生成されます。
    -   拡張子である整数値は、同期プロセス中に生成され、確定的ではありません。

## <a name="edt-extensions"></a>EDT 拡張子
次の任意のプロパティを変更するため、EDT 要素を拡張することができます。

-   フォーム ヘルプ
-   ラベル
-   文字列サイズ
-   ヘルプ テキスト

## <a name="query-extensions"></a>クエリの拡張機能
クエリ要素を拡張して以下の内容を達成することができます。

-   既存のデータ ソースに範囲を追加します。
-   既存のデータ ソースに新しい (埋め込み) のデータ ソースを追加します。
-   既存のデータ ソースに新しいフィールドを追加します。

## <a name="menu-extensions"></a>メニューの拡張機能
メニュー要素を拡張して以下の内容を達成することができます。

1.  新しいメニュー項目、サブメニュー、メニューの参照を追加し、既存のメニューへの参照を並べて表示します。
2.  **表示** プロパティをいいえに設定して、既存のメニュー項目、タイル、またはメニュー内のサブメニューを非表示にします。

#### <a name="menuextensionsmediamenuextensions-300x137pngmediamenuextensionspng"></a>[![menuextensions](./media/menuextensions-300x137.png)](./media/menuextensions.png)

## <a name="security-role-and-duty-extensions"></a>セキュリティ ロールおよび職務権限拡張機能
セキュリティ ロールまたはセキュリティ職務権限を拡張して、これらの要素に新しい職務/特権を追加することができます。

## <a name="report-extensions"></a>レポート拡張機能
拡張機能を使用してレポートおよびビジネス ドキュメントをカスタマイズすることができます。以下のものはさらに学習するためのチュートリアルの一覧です。 

[拡張機能を使用してアプリケーション スイート レポートをカスタマイズする](../analytics/customize-app-suite-reports-with-extensions.md): 標準アプリケーションのレポート ソリューションのカスタマイズは、純粋な「拡張」モデルを使用して完全にサポートをされています。  この記事では、アプリケーション スイート コンポーネントをオーバーレイすることなく、標準のアプリケーション レポートに最も一般的なカスタマイズを追加する方法について説明します。  次にいくつか挙げます… 

[方法: ビジネス ドキュメントのカスタム デザイン](../analytics/custom-designs-business-docs.md): この記事では、「純粋な」拡張モデルを使用して、既存のアプリケーション ビジネス ドキュメントのカスタムレポートデザインを作成する手順について説明します。 カスタム レポート デザインをアプリケーション ドキュメント インスタンスに関連付けるには、以下の手順に従います。 

[方法: アプリケーション スイート レポート データ セットを展開する](../analytics/expand-app-suite-report-data-sets.md): この記事では、レポート データ プロバイダー (RDP) クラスで X++ ビジネスロジックを使用して作成された既存のレポート データ セットの展開について説明します。 カスタムのデリゲート ハンドラーおよびテーブル拡張機能を使用して、...なしに追加のフィールド データと計算の両方またはいずれかを含めます。 

[方法: レポート メニュー項目の拡張](../analytics/extend-report-menu-items.md): この記事では、最小限のコード変更で、既存のアプリケーション メニューを拡大してナビゲーションをリダイレクトするプロセスについて説明します。 この手法を使用すると、既存のアプリケーションに対するすべての参照を追跡し、置き換えることの不便を避けることができます。

## <a name="label-extensions"></a>ラベルの拡張機能
ラベルの文字列値を変更、同じラベル ファイルに新しいラベルを追加、または新しい言語を追加するために、ラベル拡張ファイルを作成することができます。 ラベル拡張ファイルを作成するには、その名前に\_拡張子の接尾辞を付ける必要があります。 たとえば、フリート管理モデルの **FLM** ラベルを拡張するには、次の操作をします。

1.  フリート管理を参照するモデルに属するプロジェクトを作成します (フリート管理拡張モデルの例)。
2.  プロジェクトに新しいラベル ファイルを追加し、**FLM\_Extension** という名前をつけます。
3.  FLM\_Extension ラベル ファイル内では、ラベルを新規作成、またはフリート管理モデルの **FLM** ラベル ファイルで定義されたラベルの値を修正することができます。 新しいラベルを定義するか、元の FLM ラベル ファイルに既に存在するラベルを再定義するには、標準のラベル エディターを使用します。
4.  目標が FLM ラベルの翻訳を作成することである場合、プロジェクトの FLM\_Extension 要素を右クリックして**新しい言語の追加**を選択します。 FLM ラベルに翻訳ファイルを追加するウィザードに従います。

> [!NOTE]
> 別のモデルに FLM_Extension ファイルが既に存在する場合、N が任意の整数である (たとえば、FLM_Extension2、FLM_Extension3、... など) **FLM_ExtensionN** というファイル名を付けることができます。

## <a name="extension-of-countryregion-codes"></a>国/地域コードの拡張子

> [!NOTE]
> この機能は、Platform update 7 以降で利用できます。


**国/地域コード** プロパティにより、開発者は現在の法人のプライマリ住所に基づく特定の地域や国に機能を制限できます。 開発者は、メニュー拡張、メニュー項目拡張、表拡張 (およびフィールド)、フォーム拡張 (フォーム制御)、EDT 拡張、列挙拡張、および表示拡張の各拡張要素タイプに国地域コード プロパティを設定することにより、この機能を拡張できます。

拡張機能で追加の国/地域コードを指定することができます。 要素に関連付けられた有効な国/地域 (実行時) は、ベースライン要素とそのすべての拡張機能からのすべてのコードの結合になります。

## <a name="event-argument-types"></a>イベント引数タイプ
イベントが発生すると、上記のセクションで説明したデリゲートはトリガーされた状態になります。 このセクションでは、イベントの引数として渡される引数のタイプの詳細を示します。 以下のテーブルの一部のエントリでは、イベント引数を指定する列に null があります。つまり、渡される引数はありません。この場合、関連する情報が最初の引数 (通常は送信者と呼ばれる) です。

|                                 |                                  |
|---------------------------------|----------------------------------|
| **イベント**                       | **引数タイプ**                |
| onDefaultedField                | DefaultFieldEventArgs            |
| onDefaultedRow                  | NULL                             |
| onDefaultingField               | DefaultFieldEventArgs            |
| onDefaultingRow                 | NULL                             |
| onDeleted                       | NULL                             |
| onDeletedEntityDataSource       | DataEntityContextResultEventArgs |
| onDeleting                      | NULL                             |
| onDeletingEntityDataSource      | DataEntityContextResultEventArgs |
| onFindingEntityDataSource       | DataValidationEventArgs          |
| onFoundEntityDataSource         | DataEntityContextRecordEventArgs |
| onGettingDefaultingDependencies | DefaultingDependenciesEventArgs  |
| onGotDefaultingDependencies     | DefaultingDependenciesEventArgs  |
| onInitializedEntityDataSource   | DataEntityContextEventArgs       |
| onInitializedRecord             | NULL                             |
| onInitializingEntityDataSource  | DataEntityContextEventArgs       |
| onInitializingRecord            | NULL                             |
| onInserted                      | NULL                             |
| onInsertedEntityDataSource      | DataEntityContextResultEventArgs |
| onInserting                     | NULL                             |
| onInsertingEntityDataSource     | DataEntityContextResultEventArgs |
| onMappedDatasourceToEntity      | DataEntityContextEventArgs       |
| onMappedEntityToDataSource      | DataEntityContextEventArgs       |
| onMappingDatasourceToEntity     | DataEntityContextEventArgs       |
| onMappingEntityToDataSource     | DataEntityContextEventArgs       |
| onModifiedField                 | ModifyFieldEventArgs             |
| onModifiedFieldValue            | ModifyFieldValueEventArgs        |
| onModifyingField                | ModifyFieldEventArgs             |
| onModifyingFieldValue           | ModifyFieldValueEventArgs        |
| onPersistedEntity               | DataEntityContextEventArgs       |
| onPersistingEntity              | DataEntityContextEventArgs       |
| onPostedLoad                    | NULL                             |
| onPostingLoad                   | NULL                             |
| onUpdated                       | NULL                             |
| onUpdatedEntityDataSource       | DataEntityContextResultEventArgs |
| onUpdating                      | NULL                             |
| onUpdatingEntityDataSource      | DataEntityContextResultEventArgs |
| onValidatedDelete               | ValidateEventArgs                |
| onValidatedField                | ValidateFieldEventArgs           |
| onValidatedFieldValue           | ValidateFieldValueEventArgs      |
| onValidatedWrite                | ValidateEventArgs                |
| onValidatingDelete              | ValidateEventArgs                |
| onValidatingField               | ValidateFieldEventArgs           |
| onValidattingFieldValue         | ValidateFieldValueEventArgs      |
| onValidatingWrite               | ValidateEventArgs                |

## <a name="development-tools-support"></a>開発ツール サポート
Visual Studio の開発ツールは、拡張機能を作成して作業するための統合された機能を提供します。 たとえば、**アプリケーション エクスプ ローラー**で要素名を右クリックするときに、その要素の拡張機能を作成することができます。 

[![3\_顧客](./media/3_cust.png)](./media/3_cust.png) 

拡張機能を作成するには、**ソリューション エクスプローラー**の現在のプロジェクトが、**アプリケーション エクスプ ローラー**で選択された要素のモデルを参照するモデルに属している必要があります。 特定のプロジェクトのモデルを表示するには、プロジェクトのプロパティを表示します。 

[![4\_顧客](./media/4_cust.png)](./media/4_cust.png) 

Visual Studio は、現在のプロジェクトまたは新しいプロジェクトのいずれかで、拡張機能ファイルを作成します。 ソース コードとして、またはデザイナーを使用することにより、拡張ファイルで作業することができます。 他の任意のモデルをパッケージ化するのとまったく同じように、コード拡張モデルをパッケージ化し展開してください。 **Dynamics 365** メニューで、**配置**をポイントし、**配置パッケージの作成**をクリックして、パッケージ名のチェック ボックスを選択します。

### <a name="framework-events"></a>フレームワーク イベント

テーブル、フォーム データ ソース、フォーム コントロール、拡張イベントをサポートする他の要素タイプは、**イベント** コレクション ノードの下に使用可能なイベント (およびデリゲート) をリストします。 たとえば、テーブル拡張機能の**イベント**ノードの表示は、フレームワークによって定義されるイベントを表示し、アプリケーション開発者により定義されるメソッドを委任します。 

[![5\_顧客](./media/5_cust.png)](./media/5_cust.png) 

**注記**: テーブルのイベント、フォームイベント、フォーム データ ソース イベント、フォーム コントロール イベントなどのイベントが、さまざまな要素タイプとサブ要素タイプのデザイナーに公開されています。 イベントを操作するイベント ノードのコンテキスト メニューを開きます。 

[![6\_顧客](./media/6_cust.png)](./media/6_cust.png)

-   ***イベント ハンドラー メソッドのコピー**: このオプションは、メソッドシグネチャをクリップボードにコピーします。 任意の X++ コード エディターに貼り付けて、選択したイベントをサブスクライブするメソッドを定義することができます。
-   **イベント ハンドラーの検索** – 選択したイベントに登録されているすべてのメソッドを検索して一覧表示します。


## <a name="additional-resources"></a>その他のリソース

[拡張機能を使用してモデル要素をカスタマイズする](customize-model-elements-extensions.md)




---
title: "システム定義ボタン"
description: "このトピックでは、システム定義のボタンについて説明します。"
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 28271
ms.assetid: 23b4dade-cb99-4c61-bd1e-cf2aeafddea4
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 11e09ec422229830cb2b7d364a43380ed458a246
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="system-defined-buttons"></a>システム定義ボタン

[!include [banner](../includes/banner.md)]

このトピックでは、システム定義のボタンについて説明します。

## <a name="overview"></a>概要

システム定義のいくつかのボタンが、アクション ウィンドウに自動的に存在します。 一般に、これらのシステム定義ボタンは、エンドユーザーに適用され、使用可能な状態を保持する必要があります。 ただし、まれなケースでは (たとえば、より専門的な管理が必要な場合、またはシステム定義ボタンが特定のフォームには役立たないまたは該当しない)、開発者は明確に抑制するまたはシステム定義ボタンを上書きする必要がある場合があります。 たとえば、ある状況では、複数の「新規」オプションからユーザーが選択できるようにするメニュー ボタンは、システム定義された**新規**ボタンの方が望ましい場合があります。

## <a name="list-of-system-defined-buttons"></a>システム定義ボタンのリスト
次のテーブルは、システム定義ボタンの完全な一覧を示しています。 これらのテーブルは、条件付きまたは完全に抑制または上書きする必要がある場合に役立つ情報も提供します。

### <a name="common-buttons"></a>一般的なボタン

| ボタン       | ボタン名マクロ\*              | コメント                                                                                             |
|--------------|----------------------------------|------------------------------------------------------------------------------------------------------|
| 輸出       |                                  | このボタンを抑制しないでください。                                                                          |
| 添付       | \#SystemDefinedAttachButton      | 添付ファイル用に設定されていないフォームでは表示しないため、このボタンを抑制しないでください。 |
| フィルターの表示 | \#SystemDefinedShowFiltersButton | 既定では、目次フォームは**表示**=**いいえ**になっています。                                                         |

\* システム定義のボタン名マクロは、 SysSystemDefinedButtons マクロ ファイルにあります。

### <a name="buttons-that-are-specific-to-details-forms"></a>詳細フォームに固有のボタン

これらのボタンは、詳細フォームの経験の不可欠な部分です。 したがって、これらのボタンを非表示にする必要はほとんどありません。

| ボタン              | ボタン名マクロ\*                    | コメント                                                |
|---------------------|----------------------------------------|---------------------------------------------------------|
| ビューの変更         | \#SystemDefinedShowMenuButton          | このボタンは、**オプション**アクション ペイン タブの下にあります。 |
| グリッド ビュー           | \#SystemDefinedGridViewButton          |                                                         |
| 詳細ビュー        | \#SystemDefinedDetailsViewButton       |                                                         |
| 行の詳細の表示   | \#SystemDefinedLineDetailsViewButton   |                                                         |
| ヘッダーの詳細ビュー | \#SystemDefinedHeaderDetailsViewButton |                                                         |
| リストを表示           | \#SystemDefinedShowListButton          |                                                         |

\* システム定義のボタン名マクロは、 SysSystemDefinedButtons マクロ ファイルにあります。

## <a name="form-styles-that-have-no-system-defined-buttons"></a>システム定義ボタンのないフォーム スタイル
さまざまなフォーム スタイルについては、システム定義されたボタンの追加に意味がない主な理由は、これらのフォームが標準のアクション ウィンドウを持っていないことです。 次のフォーム スタイルは、システム定義のボタンを受け取ることはありません。

-   ダッシュボード
-   ダイアログ
-   DropDialog
-   FormPart
-   ルックアップ
-   サイトマップ
-   ウィザード

## <a name="suppressing-most-or-all-of-the-system-defined-buttons"></a>システム定義のボタンの大部分またはすべてを非表示
フォーム上のシステム定義ボタンのほとんどまたはすべてを非表示にしている場合は、フォームのスタイル (**Form.Design.Style**) またはパターンを再確認し、フォームの目的を再検討する必要があります。 代わりにフォームをダイアログにすべきでしょうか。 (デフォルトでは、ダイアログにはシステム定義のボタンは表示されません。) 多くの場合、このような状況でのフォームは**スタイル**=**自動**であり、ダイアログとしてはより適切です。 フォームを技術的にダイアログにする必要がある場合、同時にすべてのシステム定義されたボタンを自動的に非表示にできるメタデータまたはコードは現在ありません。 フォームをシステム定義のボタンを受け取らないフォーム スタイルに切り替える場合を除き、各ボタンを個別に抑制/オーバーライドにする必要があります (この記事の他のセクションを参照)。 このシナリオは非常に稀です。

## <a name="new-and-delete-system-buttons"></a>新規システムおよびシステムの削除のボタン
**新規** および **削除** ボタンは、現在カーネルによって追加され、特殊なメタデータ プロパティを使用して制御されます。 これらのボタンは、常にフォーム上の最初のマスター データソースで機能します。

### <a name="when-are-these-buttons-available-by-default"></a>これらのボタンは既定ではいつ有効になりますか

フォームには通常、システム定義された**新規**および**削除**ボタンがあります。 これらのボタンは、次の条件でフォームに表示されます。

-   フォームには、システム定義のボタンを使用できるスタイルがあります。
-   フォームには 1 つ以上のデータ ソースがあります。

### <a name="how-do-i-affect-the-visibility-of-the-new-and-delete-buttons-on-a-form-but-still-allow-the-standard-new-and-delete-tasks-to-fire-via-keyboard-shortcuts"></a>フォームの新規および削除ボタンの表示にどのように影響を与えますか。ただしキーボードのショートカットを介して標準の新規および削除タスクを起動できますか。

フォームでの **新規** ボタンと **削除** ボタンの表示/非表示を制御するには、**Form.Design** の **ShowNewButton** および **ShowDeleteButton** プロパティを使用します。 データ ソースでユーザーがまだレコードを作成して削除できる場合、キーボード ショートカットはシステム ボタンが表示されない場合でも引き続き機能することに注意してください。

| プロパティ                     | 先頭値 | 説明                                                |
|------------------------------|-------|------------------------------------------------------------|
| Form.Design.ShowNewButton    | 無    | フォーム上でシステム定義の **新規** ボタンを非表示にします。    |
| Form.Design.ShowDeleteButton | 無    | フォーム上でシステム定義の **削除** ボタンを非表示にします。 |

### <a name="how-do-i-affect-the-state-enableddisabled-of-the-new-and-delete-buttons-and-the-associated-task-behavior-on-a-form"></a>新規および削除ボタンの状態 (有効/無効)、およびフォームで関連するタスクの動作にどのように影響しますか。

フォーム上の **新規** および **削除** ボタンの状態と、関連するタスクの動作の両方に影響を及ぼすには、**AllowCreate** と **AllowDelete** のプロパティを指定します。 また、このアプローチを使用して、**新規**と**削除**ボタンを無効にする場合、関連付けられているキーボード ショートカットは無効になります。

| プロパティ                                                   | 先頭値 | 説明                                                                                                  |
|------------------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------|
| Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowCreate | 無    | フォームはレコードの作成を許可しません。 フォームに無効なシステム定義の **新規** ボタンがあります。               |
| Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowCreate | 有   | このフォームはレコードの作成を可能にします。 フォームには、システム定義の **新規** ボタンが有効になっています (表示されている場合)。    |
| Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowDelete | 無    | フォームはレコードの削除を許可しません。 フォームに無効なシステム定義の **削除** ボタンがあります。            |
| Form.Datasources.&lt;FirstMasterDatasource&gt;.AllowDelete | 有   | このフォームはレコードの削除を可能にします。 フォームには、システム定義の **削除** ボタンが有効になっています (表示されている場合)。 |

**注記:** フォームに新規レコード アクションがある場合、ボタン コントロールはシステム定義の**新規**ボタンの有効状態を上書きします。

### <a name="how-do-i-change-the-behavior-of-the-new-task-either-by-clicking-the-button-or-by-using-the-keyboard-shortcut"></a>新しいタスク (ボタンをクリックするまたはキーボード ショートカットを使用するかのいずれか) の動作をどのように変更しますか。

新しいタスクの動作を変更するメカニズムは 3 つあります。

- **新しいレコード アクション** プロパティを使用します。 このプロパティは、現在、**Form.Design** でのみ使用可能であり、フォーム上で **New** コマンドを呼び出す**すべての** CommandButton (セカンダリ コレクションにバインドされている CommandButtons も含まれる) に対して参照されたアクションがトリガーされます。 今後、**新しいレコード アクション** プロパティがすべてのコンテナー コントロールに配置され、プロパティのスコープにわたるコントロールが向上します。 現時点では、**新しいレコード アクション** プロパティもメニュー ボタンまたはドロップ ダイアログ ボタンとして定義できないことに注意してください。

  |          プロパティ           |             先頭値              |                              説明                              |
  |-----------------------------|--------------------------------|-----------------------------------------------------------------------|
  | Form.Design.NewRecordAction | フォームからのコントロール名 | このプロパティは、指定されたアクションを実行するための新規タスクをオーバーライドします。 |


- (推奨)イベントを使用します。 特に、レコードの作成と削除の前後に実行することを意図したコードを配置できる場合、これらのアクションのプリイベントとポストイベントがあります。 以下のコード例をご覧ください。

      [Form]
      public class Form1 extends FormRun
      {
          public void init()
          {
              super();
              element.dataHelper().RecordCreating += eventhandler(this.PreRecordCreate);
              element.dataHelper().RecordCreated  += eventhandler(this.PostRecordCreate);
              // similar methods exist for deletion:
              // element.dataHelper().RecordDeleting, element.dataHelper().RecordDeleted
              //
              // explicit actions can be triggered via:
              // element.dataHelper().RecordCreate(), element.dataHelper().RecordDelete()        
          }
          public void PreRecordCreate(FormRunServiceArgs _cancellableArgs)
          {
              //  I can add my logic here that gets invoked before the global creation task
              // if I need to, I can cancel the "super" of the task by doing:
              // _cancellableArgs.cancel()
          }
          public void PostRecordCreate()
          {
              //  I can add my logic here that gets invoked after the global creation task
          }
      }

- 対応するデータ ソースの、**create()** または **delete()** メソッドで上書きを作成します。

### <a name="how-do-i-change-the-behavior-of-the-new-button-but-not-the-task"></a>新しいボタン (ただしタスクではない) の動作をどのように変更しますか。

システム定義された**新規**ボタンを、複数の「新規」オプションからユーザーに選択させるメニュー ボタンに置き変える場合を考えてみましょう。 したがって、次のタスクを実行できます。

1.  システム定義された**新規**ボタンを非表示にします。
2.  新しいアクションに対する独自のボタンをモデル化します。

ただし、この時点で、キーボード ショートカットが呼び出されると、新規のシステム動作も起動します。 キーボード ショートカットを押したときにモデル化された**新規**ボタンを起動するようにするには、このボタンを **Form.Design** の NewRecordAction として設定する必要があります。 前のセクションで触れたように、アクションは現在フォーム上の新しいタスクを呼び出すすべての CommandButtons に対して起動されます。 したがって、このアプローチは、複数のデータソースを持つフォームでは使用しないでください。

## <a name="edit-done-save-and-restore-system-buttons"></a>編集、実行、保存、およびシステム ボタンを復元

**編集**、**実行**、**保存**、および **復元** ボタンでは、ユーザーが必要に応じてフォームの編集モードを切り替えることができます。 この機能は重要であるため、これらのボタンは現在抑制できません。 ただし、フォームが常に**編集**モードまたは**表示**モードである必要がある場合、**ViewEditMode** プロパティを使用して効果を達成でき、ボタンはフォームに表示されません。 ほとんどのフォームが **ViewEditMode**=**Auto** のままになることに注意してください。フォームが読み取り専用の場合、または常に編集可能になる場合を除いて、純粋に外観上の理由で **ViewEditMode**=**View** または **ViewEditMode=Edit** に設定しないでください。

| Form.Design.ViewEditMode | フォーム動作                                                     | システム定義ボタンの動作                                                                                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 表示                     | フォームは常に **表示** モードです。                              | フレームワークが必要ではないとみなすため、これらのボタン (**編集**、**完了**、**保存**、および**復元**) のいずれも表示されません。                                                                                               |
| 編集                     | フォームは常に **編集** モードです。                              | **保存**および**元に戻す**ボタンのみが表示されるのは、ユーザーが**編集**モードを終了することができないからです。 **元に戻す** ボタンは、フレームワークによって指定された **オプション** タブにあります。                                                                    |
| 自動                     | フォームは、**表示** モードと **編集** モードの間で切り替えることができます。 | **表示**モードでは、**編集**ボタンはアクション ウィンドウに表示されます。 **編集**モードでは、**保存**ボタンはアクション ウィンドウに表示されており、**読み取りモード**および**元に戻す**ボタンはフレームワークによって指定された**オプション** タブに表示されます。 |

### <a name="can-i-conditionally-suppress-or-show-the-edit-button"></a>条件付きで 編集ボタンを隠すまたは表示できますか？

あるポイントでフォームが編集可能で、他のポイントで読み取り専用にすると、ユーザーがフォームを編集できるかどうかを判断するロジックを使用して、実行時に **ViewEditMode** プロパティを設定できます。 フォームを読み取り専用にする必要があるときは、**ViewEditMode**=**表示** を設定します。 フォームの編集または表示のいずれかができるとき、**ViewEditMode**=**自動** を設定します。

### <a name="how-do-i-run-additional-code-when-the-edit-button-is-clicked"></a>編集ボタンをクリックするときに追加コードを実行するにはどうすればよいですか。

**編集** ボタンをクリックしたときに追加のコードを実行させるには、イベントを使用します (「新しいタスクの動作を変更する方法 (ボタンをクリックするか、キーボード ショートカットを使用する)」の例を参照してください)。 この記事の前半のセクション)。 具体的には、次のイベントを使用します。

-   現在の表示/編集モードの切替えをサブスクライブするには、次のイベントを使用します。
    -   element.viewEditModeHelper().EditModeSwitching
    -   element.viewEditModeHelper().EditModeSwitche
-   現在の表示/編集モードを照会するには、次のイベントを使用します。
    -   element.viewEditModeHelper().isInEditMode()
    -   element.viewEditModeHelper().IsInViewMode()
-   現在の表示/編集モードの切替えをトリガーするには、次のイベントを使用します。
    -   element.viewEditModeHelper().setViewEditMode(ViewEditMode::Edit)

## <a name="refresh-popout-and-close-system-buttons"></a>[更新]、[ポップアウト]、[閉じる] システム ボタン
**更新**、**ポップアウト**、および**閉じる** ボタンは、アクション ウィンドウの右側にあるシステム ボタンです。 **更新** ボタンは、フォーム上のすべてのデータを更新するために使用されます。 **ポップアウト** ボタンを使用すると、現在のフォームが別のウィンドウに移動します。 **閉じる** ボタンは、フォームを閉じます (基本的に、このボタンはブラウザの **戻る** ボタンをクリックします)。 これらのシステム ボタンは不可欠なコンポーネントであり、現時点では抑制することはできません。

## <a name="other-system-defined-buttons"></a>他のシステム定義ボタン
残りのシステム定義のボタンは **Form.Init** 中に追加されます。 同じ名前のコントロールが存在しない場合にのみ追加されます。

### <a name="how-do-i-run-additional-code-together-with-a-system-defined-button-or-change-the-behavior-of-the-button"></a>システム定義されたボタンと共に追加コードを実行する、またはボタンの動作を変更するにはどうすればよいですか。

-   表示切り替えボタン (たとえば、グリッド ビュー、詳細ビュー、ヘッダービュー、または明細行ビューに切り替えるボタン) については、個々の TabPage で **pageActivated()** メソッドを上書きする必要があります。
-   プリイベント/ポストイベントを持つシステム定義されたボタン (たとえば、**新規**、**削除**、および**編集**) については、適切なイベントにサブスクライブすることができます。 これらのボタンの特定のイベントについては、**新規作成**/**削除** ボタンと **編集** ボタンの対応するセクションを参照してください。
-   タスクを直接呼び出さないシステム定義のボタン (たとえば、**SystemDefinedShowMenuButton** および **SystemDefinedShowListButton**) については、**registerOverrideMethod()** の呼び出しを通してボタンの上書きを登録でき、システム定義ボタンをクリックしたときに追加コードが実行されるようにします。

        public void overrideFunction(FormCommandButtonControl _command)
            {
                // Put any pre-super code here 
               // This serves as the call to super()
                _command.clicked(); 
                // Put any post-super code here
            }

### <a name="how-do-i-suppress-any-of-these-system-defined-buttons-on-a-form-but-without-suppressing-any-corresponding-task"></a>対応するタスクを抑制することなく、フォーム上のこれらのシステム定義されたボタンのいずれかを抑制するにはどうすればよいですか。

一般に、システム ボタンのいずれかを非表示にすることはお勧めしません。 それらの存在は、フォーム上のアクションに一貫性をもたらします。 ただし、それが役立たないある状況によっては、ボタンが現在表示されます。 これらの状況の多くに対処する将来の作業項目があります。 たとえば、次のタスクの作業項目があります。

-   添付ファイルを許可するように構成されていないフォームで **添付** ボタンを非表示にします。
-   グリッドがないフォームで **エクスポート** ボタンを非表示にします。
-   メイン グリッドがないフォームで **フィルターを表示する** ボタンを非表示にします。

ただし、これらのボタンのいずれかを抑制する必要がある場合 (決して推奨しません)、次のコード例に示すように、コードを通してコントロールを検索し、可視性を **false** に設定できます。 利用可能な場合、SysSystemDefinedButtons マクロを使用して、ボタン名を参照します。

    FormCommandButtonControl attachButton;

       public void init()
       {
            #SysSystemDefinedButtons

            super();

            attachButton= this.control(this.controlId(#SystemDefinedAttachButton)) as FormCommandButtonControl; 
            attachButton.visible(false); 
        }





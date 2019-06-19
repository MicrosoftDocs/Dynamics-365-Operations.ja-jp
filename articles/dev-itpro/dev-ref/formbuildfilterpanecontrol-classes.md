---
title: F クラス (FormBuildFilterPaneControl から FormBuildRealControl)
description: 文字 F で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 60083
ms.assetid: a68797b9-a230-4f72-980e-43101e9b1dd2
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a19fcd01df491bbbc106bd3ebd32681bdb31c861
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595454"
---
# <a name="f-classes-formbuildfilterpanecontrol-to-formbuildrealcontrol"></a>F クラス (FormBuildFilterPaneControl から FormBuildRealControl)

[!include [banner](../includes/banner.md)]

文字 F で始まるシステム API クラス。

<a name="class-formbuildfilterpanecontrol"></a>クラス FormBuildFilterPaneControl
--------------------------------

    class FormBuildFilterPaneControl extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignChild(\[boolean value\])                                                                |                                                                                                                                           |
| public boolean alignChildren(\[boolean value\])                                                             |                                                                                                                                           |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                  |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                       |
| public int allowUserSetup(\[int value\])                                                                    |                                                                                                                                           |
| public int arrangeGuide(\[int value\])                                                                      |                                                                                                                                           |
| public int arrangeMethod(\[int value\])                                                                     |                                                                                                                                           |
| public int arrangeWhen(\[int value\])                                                                       |                                                                                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                           |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                           |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                           |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                   |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                     |                                                                                                                                           |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                        |                                                                                                                                           |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                           |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                          |                                                                                                                                           |
| public int columnspaceValue(\[int value\])                                                                  |                                                                                                                                           |
| public int columnsValue(\[int value\])                                                                      |                                                                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                       |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                 |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                           |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                           |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                  |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                           |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                   |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                   |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public boolean hideIfEmpty(\[boolean value\])                                                               |                                                                                                                                           |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                           |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                          |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                              |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                           |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                           |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                           |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                           |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                           |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                           |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                           |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                           |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                           |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                           |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                           |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                           |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                           |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                           |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                           |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                           |
| public int topMode(\[int value\])                                                                           |                                                                                                                                           |
| public int topValue(\[int value\])                                                                          |                                                                                                                                           |
| public int type(\[int value\])                                                                              |                                                                                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                           |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                           |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                           |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                           |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                    |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                            |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                           |

### <a name="method-alignchild"></a>メソッド alignChild

    public boolean alignChild([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-alignchildren"></a>メソッド alignChildren

    public boolean alignChildren([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowusersetup"></a>メソッド allowUserSetup

    public int allowUserSetup([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangeguide"></a>メソッド arrangeGuide

    public int arrangeGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangemethod"></a>メソッド arrangeMethod

    public int arrangeMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangewhen"></a>メソッド arrangeWhen

    public int arrangeWhen([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

    public int bottomMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-columns"></a>メソッド columns

    public int columns([int value], [ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsmode"></a>メソッド columnsMode

    public ColumnsMode columnsMode([ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspace"></a>メソッド columnspace

    public int columnspace([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspacemode"></a>メソッド columnspaceMode

    public AutoMode columnspaceMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspacevalue"></a>メソッド columnspaceValue

    public int columnspaceValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsvalue"></a>メソッド columnsValue

    public int columnsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginmode"></a>メソッド leftMarginMode

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

    public int leftMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginmode"></a>メソッド rightMarginMode

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

    public int rightMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginmode"></a>メソッド topMarginMode

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginvalue"></a>メソッド topMarginValue

    public int topMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildfunctionbuttoncontrol"></a>クラス FormBuildFunctionButtonControl
    class FormBuildFunctionButtonControl extends FormBuildControl

FormBuildFunctionButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                  |
| public int alignment(\[int value\])                                                                         |                                                                                                                                           |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                       |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                        |
| public boolean autoRefreshData(\[boolean value\])                                                           |                                                                                                                                           |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                         |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                            |
| public boolean big(\[boolean value\])                                                                       |                                                                                                                                           |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                               |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                  |
| public int buttonDisplay(\[int value\])                                                                     | ボタン コントロールの外観を取得または設定します。                                                                                        |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                   |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                               |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                       |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                 |
| public int copyCallerQuery(\[int value\])                                                                   |                                                                                                                                           |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                           |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                           |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                           |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                  |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォーム上の既定のボタンにするかどうかを指定します。                                                                   |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                            |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                           |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                            |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                           |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                       |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                 |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                 |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                           |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                       |
| public int formViewOption(\[int value\])                                                                    |                                                                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                   |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                            |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                   |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                  |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                           |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                          |
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                           |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                              |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                           |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                           |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                           |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                           |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                           |
| public str menuItemName(\[str value\])                                                                      |                                                                                                                                           |
| public MenuItemType menuItemType(\[MenuItemType value\])                                                    |                                                                                                                                           |
| public int multiSelect(\[int value\])                                                                       |                                                                                                                                           |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                           |
| public int needsRecord(\[int value\])                                                                       |                                                                                                                                           |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                           |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                           |
| public int openMode(\[int value\])                                                                          |                                                                                                                                           |
| public str parameters(\[str value\])                                                                        | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                    |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                           |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                           |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                           |
| public boolean sendExternalContext(\[boolean value\])                                                       |                                                                                                                                           |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                           |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                           |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。           |
| public int style(\[int value\])                                                                             |                                                                                                                                           |
| public str text(\[str value\])                                                                              |                                                                                                                                           |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                           |
| public int topMode(\[int value\])                                                                           |                                                                                                                                           |
| public int topValue(\[int value\])                                                                          |                                                                                                                                           |
| public int type(\[int value\])                                                                              |                                                                                                                                           |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                       |
| public int userData(\[int value\])                                                                          |                                                                                                                                           |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                           |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                           |
| public boolean value(\[boolean value\])                                                                     |                                                                                                                                           |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                           |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                           |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                           |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                           |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                    |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                            |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                    |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                           |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-autorefreshdata"></a>メソッド autoRefreshData

    public boolean autoRefreshData([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-big"></a>メソッド big

    public boolean big([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-buttondisplay"></a>メソッド buttonDisplay

ボタン コントロールの外観を取得または設定します。

    public int buttonDisplay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 5 までの整数。

#### <a name="remarks"></a>備考

プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。 このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。 返される整数値には、次のようなボタン コントロールの外観が含まれます。

| 値です。 | 説明。                                                     |
|--------|------------------------------------------------------------------|
| 0      | テキストのみ。                                                       |
| 1      | イメージのみ。                                                      |
| 2      | テキストと画像。画像はテキストの下に表示されます。           |
| 3      | テキストと画像。画像はテキストの上に表示されます。           |
| 4      | テキストと画像。画像はテキストの左に表示されます。  |
| 5      | テキストと画像。画像はテキストの右に表示されます。 |

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づく値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-copycallerquery"></a>メソッド copyCallerQuery

    public int copyCallerQuery([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-defaultbutton"></a>メソッド defaultButton

ボタンをフォーム上の既定のボタンにするかどうかを指定します。

    public boolean defaultButton([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ボタンが既定のボタンである場合は true。それ以外の場合は、false。

### <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

    public str disabledImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画像ファイルのフル ネーム。 システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。

#### <a name="remarks"></a>備考

このプロパティは、disabledResource プロパティに優先します。 これらのプロパティの両方が設定されている場合に使用されます。

### <a name="method-disabledimagelocation"></a>メソッド disabledImageLocation

    public int disabledImageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledresource"></a>メソッド disabledResource

無効なボタン画像として使用する画像リソース ID を取得または設定します。

    public int disabledResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

無効なボタン画像として使用する画像リソース ID。 アイコンとビットマップ イメージの両方がサポートされます。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-forcedtooverflow"></a>メソッド forcedToOverflow

    public boolean forcedToOverflow([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-formviewoption"></a>メソッド formViewOption

    public int formViewOption([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-keytip"></a>メソッド keyTip

    public str keyTip([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-multiselect"></a>メソッド multiSelect

    public int multiSelect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-needsrecord"></a>メソッド needsRecord

    public int needsRecord([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-openmode"></a>メソッド openMode

    public int openMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-primary"></a>メソッド primary

    public boolean primary([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-saverecord"></a>メソッド saveRecord

    public boolean saveRecord([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sendexternalcontext"></a>メソッド sendExternalContext

    public boolean sendExternalContext([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-shortkey"></a>メソッド shortkey

    public int shortkey([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showshortcut"></a>メソッド showShortCut

    public boolean showShortCut([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public boolean value([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildgridcontrol"></a>クラス FormBuildGridControl
    class FormBuildGridControl extends FormBuildControl

FormBuildGridControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public int activeBackColor(\[int value\])                                                                   |                                                                                                                                         |
| public int activeForeColor(\[int value\])                                                                   |                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int alternateRowShading(\[int value\])                                                               |                                                                                                                                         |
| public boolean autoDataGroup(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int bottomMargin(\[int value\])                                                                      |                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public str dataGroup(\[str value\])                                                                         |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                     |
| public str defaultAction(\[str value\])                                                                     |                                                                                                                                         |
| public str defaultActionLabel(\[str value\])                                                                |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public boolean exportAllowed(\[boolean value\])                                                             |                                                                                                                                         |
| public str exportLabel(\[str value\])                                                                       |                                                                                                                                         |
| public boolean gridLines(\[boolean value\])                                                                 |                                                                                                                                         |
| public int gridLinesStyle(\[int value\])                                                                    |                                                                                                                                         |
| public str groupBy(\[str value\])                                                                           |                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public boolean highlightActive(\[boolean value\])                                                           |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMargin(\[int value\])                                                                        |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int moreRowsIndicator(\[int value\])                                                                 |                                                                                                                                         |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         | コントロールに指定されたコントロールを移動します。                                                                                               |
| public boolean multiSelect(\[boolean value\])                                                               |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int rightMargin(\[int value\])                                                                       |                                                                                                                                         |
| public int scrollbars(\[int value\])                                                                        |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean showColLabels(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean showRowLabels(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMargin(\[int value\])                                                                         |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public boolean useUserLayout(\[boolean value\])                                                             |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int visibleCols(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode visibleColsMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int visibleColsValue(\[int value\])                                                                  |                                                                                                                                         |
| public int visibleRows(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode visibleRowsMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int visibleRowsValue(\[int value\])                                                                  |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-activebackcolor"></a>メソッド activeBackColor

    public int activeBackColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-activeforecolor"></a>メソッド activeForeColor

    public int activeForeColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-alternaterowshading"></a>メソッド alternateRowShading

    public int alternateRowShading([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodatagroup"></a>メソッド autoDataGroup

    public boolean autoDataGroup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datagroup"></a>メソッド dataGroup

    public str dataGroup([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-defaultaction"></a>メソッド defaultAction

    public str defaultAction([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-defaultactionlabel"></a>メソッド defaultActionLabel

    public str defaultActionLabel([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-exportallowed"></a>メソッド exportAllowed

    public boolean exportAllowed([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-exportlabel"></a>メソッド exportLabel

    public str exportLabel([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-gridlines"></a>メソッド gridLines

    public boolean gridLines([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-gridlinesstyle"></a>メソッド gridLinesStyle

    public int gridLinesStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-groupby"></a>メソッド groupBy

    public str groupBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-highlightactive"></a>メソッド highlightActive

    public boolean highlightActive([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-morerowsindicator"></a>メソッド moreRowsIndicator

    public int moreRowsIndicator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

#### <a name="return-value"></a>戻り値

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

### <a name="method-multiselect"></a>メソッド multiSelect

    public boolean multiSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-scrollbars"></a>メソッド scrollbars

    public int scrollbars([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showcollabels"></a>メソッド showColLabels

    public boolean showColLabels([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showrowlabels"></a>メソッド showRowLabels

    public boolean showRowLabels([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblecols"></a>メソッド visibleCols

    public int visibleCols([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblecolsmode"></a>メソッド visibleColsMode

    public AutoMode visibleColsMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblecolsvalue"></a>メソッド visibleColsValue

    public int visibleColsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblerows"></a>メソッド visibleRows

    public int visibleRows([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblerowsmode"></a>メソッド visibleRowsMode

    public AutoMode visibleRowsMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-visiblerowsvalue"></a>メソッド visibleRowsValue

    public int visibleRowsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildgroupcontrol"></a>クラス FormBuildGroupControl
    class FormBuildGroupControl extends FormBuildControl

FormBuildGroupControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignChild(\[boolean value\])                                                                |                                                                                                                                         |
| public boolean alignChildren(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int allowUserSetup(\[int value\])                                                                    |                                                                                                                                         |
| public int arrangeGuide(\[int value\])                                                                      |                                                                                                                                         |
| public int arrangeMethod(\[int value\])                                                                     |                                                                                                                                         |
| public int arrangeWhen(\[int value\])                                                                       |                                                                                                                                         |
| public boolean autoDataGroup(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                         |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                         |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                         |
| public boolean breakable(\[boolean value\])                                                                 |                                                                                                                                         |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                 |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                     |                                                                                                                                         |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                        |                                                                                                                                         |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int columnspaceValue(\[int value\])                                                                  |                                                                                                                                         |
| public int columnsValue(\[int value\])                                                                      |                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public str dataGroup(\[str value\])                                                                         |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int frameOptionButton(\[int value\])                                                                 |                                                                                                                                         |
| public int framePosition(\[int value\])                                                                     |                                                                                                                                         |
| public int frameType(\[int value\])                                                                         |                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public boolean hideIfEmpty(\[boolean value\])                                                               |                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                         |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                         |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         | コントロールに指定されたコントロールを移動します。                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int optionValue(\[int value\])                                                                       |                                                                                                                                         |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                         |
| public boolean saveFilter(\[boolean value\])                                                                |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                         |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                         |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public boolean useUserLayout(\[boolean value\])                                                             |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-alignchild"></a>メソッド alignChild

    public boolean alignChild([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-alignchildren"></a>メソッド alignChildren

    public boolean alignChildren([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allowusersetup"></a>メソッド allowUserSetup

    public int allowUserSetup([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangeguide"></a>メソッド arrangeGuide

    public int arrangeGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangemethod"></a>メソッド arrangeMethod

    public int arrangeMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrangewhen"></a>メソッド arrangeWhen

    public int arrangeWhen([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodatagroup"></a>メソッド autoDataGroup

    public boolean autoDataGroup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

    public int bottomMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-breakable"></a>メソッド breakable

    public boolean breakable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに基づいて値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-columns"></a>メソッド columns

    public int columns([int value], [ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsmode"></a>メソッド columnsMode

    public ColumnsMode columnsMode([ColumnsMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspace"></a>メソッド columnspace

    public int columnspace([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspacemode"></a>メソッド columnspaceMode

    public AutoMode columnspaceMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-columnspacevalue"></a>メソッド columnspaceValue

    public int columnspaceValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-columnsvalue"></a>メソッド columnsValue

    public int columnsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datagroup"></a>メソッド dataGroup

    public str dataGroup([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-frameoptionbutton"></a>メソッド frameOptionButton

    public int frameOptionButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-frameposition"></a>メソッド framePosition

    public int framePosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-frametype"></a>メソッド frameType

    public int frameType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginmode"></a>メソッド leftMarginMode

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

    public int leftMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

#### <a name="return-value"></a>戻り値

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-optionvalue"></a>メソッド optionValue

    public int optionValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginmode"></a>メソッド rightMarginMode

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

    public int rightMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-savefilter"></a>メソッド saveFilter

    public boolean saveFilter([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginmode"></a>メソッド topMarginMode

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginvalue"></a>メソッド topMarginValue

    public int topMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildguidcontrol"></a>クラス FormBuildGuidControl
    class FormBuildGuidControl extends FormBuildControl

FormBuildGuidControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                |
| public int direction(\[int value\])                                                                         |                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                         |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public Guid value(\[Guid value\])                                                                           |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fasttabsummary"></a>メソッド fastTabSummary

    public int fastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public Guid value([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildhtmlcontrol"></a>クラス FormBuildHTMLControl
    class FormBuildHTMLControl extends FormBuildControl

FormBuildHTMLControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                 |
| public str className(\[str value\])                                                                         |                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public str custom(\[str value\])                                                                            |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public boolean rTLCapable(\[boolean value\])                                                                |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-classname"></a>メソッド className

    public str className([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-custom"></a>メソッド custom

    public str custom([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpTextproperty を設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rtlcapable"></a>メソッド rTLCapable

    public boolean rTLCapable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildintcontrol"></a>クラス FormBuildIntControl
    class FormBuildIntControl extends FormBuildControl

FormBuildIntControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int allowNegative(\[int value\])                                                                     |                                                                                                                                         |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                |
| public int direction(\[int value\])                                                                         |                                                                                                                                         |
| public int displaceNegative(\[int value\], \[AutoMode mode\])                                               |                                                                                                                                         |
| public AutoMode displaceNegativeMode(\[AutoMode mode\])                                                     |                                                                                                                                         |
| public int displaceNegativeValue(\[int value\])                                                             |                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                         |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                         |
| public int rotateSign(\[int value\])                                                                        |                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                         |
| public int showZero(\[int value\])                                                                          |                                                                                                                                         |
| public int signDisplay(\[int value\])                                                                       |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int value(\[int value\])                                                                             |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allownegative"></a>メソッド allowNegative

    public int allowNegative([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegative"></a>メソッド displaceNegative

    public int displaceNegative([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegativemode"></a>メソッド displaceNegativeMode

    public AutoMode displaceNegativeMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegativevalue"></a>メソッド displaceNegativeValue

    public int displaceNegativeValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fasttabsummary"></a>メソッド fastTabSummary

    public int fastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rotatesign"></a>メソッド rotateSign

    public int rotateSign([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showzero"></a>メソッド showZero

    public int showZero([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-signdisplay"></a>メソッド signDisplay

    public int signDisplay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public int value([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildlistboxcontrol"></a>クラス FormBuildListBoxControl
    class FormBuildListBoxControl extends FormBuildControl

FormBuildListBoxControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                          |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public EnumId enumType(\[EnumId value\])                                                                    |                                                                                                                                         |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public boolean hideFirstEntry(\[boolean value\])                                                            |                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public int item(\[int value\])                                                                              |                                                                                                                                         |
| public int items(\[int value\])                                                                             |                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public int selection(\[int value\])                                                                         |                                                                                                                                         |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public str text(\[str value\])                                                                              |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-enumtype"></a>メソッド enumType

    public EnumId enumType([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hidefirstentry"></a>メソッド hideFirstEntry

    public boolean hideFirstEntry([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public int item([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-items"></a>メソッド items

    public int items([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selection"></a>メソッド selection

    public int selection([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildlistcontrol"></a>クラス FormBuildListControl
    class FormBuildListControl extends FormBuildControl

FormBuildListControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public boolean autoArrange(\[boolean value\])                                                               |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                           |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public boolean canScroll(\[boolean value\])                                                                 |                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public boolean checkBox(\[boolean value\])                                                                  |                                                                                                                                         |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public boolean columnHeader(\[boolean value\])                                                              |                                                                                                                                         |
| public boolean columnHeaderButton(\[boolean value\])                                                        |                                                                                                                                         |
| public boolean columnImages(\[boolean value\])                                                              |                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean editLabels(\[boolean value\])                                                                |                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public boolean gridLines(\[boolean value\])                                                                 |                                                                                                                                         |
| public boolean headerdragdrop(\[boolean value\])                                                            |                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public int itemAlign(\[int value\])                                                                         |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public boolean oneClickActivate(\[boolean value\])                                                          |                                                                                                                                         |
| public boolean rowSelect(\[boolean value\])                                                                 |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean showSelAlways(\[boolean value\])                                                             |                                                                                                                                         |
| public boolean singleSelection(\[boolean value\])                                                           |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int sort(\[int value\])                                                                              |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public boolean trackSelect(\[boolean value\])                                                               |                                                                                                                                         |
| public boolean twoClickActivate(\[boolean value\])                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewType(\[int value\])                                                                          |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-autoarrange"></a>メソッド autoArrange

    public boolean autoArrange([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-canscroll"></a>メソッド canScroll

    public boolean canScroll([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-checkbox"></a>メソッド checkBox

    public boolean checkBox([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-columnheader"></a>メソッド columnHeader

    public boolean columnHeader([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-columnheaderbutton"></a>メソッド columnHeaderButton

    public boolean columnHeaderButton([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-columnimages"></a>メソッド columnImages

    public boolean columnImages([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-editlabels"></a>メソッド editLabels

    public boolean editLabels([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-gridlines"></a>メソッド gridLines

    public boolean gridLines([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-headerdragdrop"></a>メソッド headerdragdrop

    public boolean headerdragdrop([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-itemalign"></a>メソッド itemAlign

    public int itemAlign([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-oneclickactivate"></a>メソッド oneClickActivate

    public boolean oneClickActivate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rowselect"></a>メソッド rowSelect

    public boolean rowSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showselalways"></a>メソッド showSelAlways

    public boolean showSelAlways([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-singleselection"></a>メソッド singleSelection

    public boolean singleSelection([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-sort"></a>メソッド sort

    public int sort([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-trackselect"></a>メソッド trackSelect

    public boolean trackSelect([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-twoclickactivate"></a>メソッド twoClickActivate

    public boolean twoClickActivate([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-viewtype"></a>メソッド viewType

    public int viewType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildmanagedhostcontrol"></a>クラス FormBuildManagedHostControl
    class FormBuildManagedHostControl extends FormBuildControl

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                           |
| public str assemblyName(\[str value\])                                                                      |                                                                                                                                               |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                            |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                     |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                               |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                               |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                               |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                             |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                       |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                       |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public boolean hideIfEmpty(\[boolean value\])                                                               |                                                                                                                                               |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                               |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                              |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                  |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                               |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                               |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                               |
| public boolean rTLCapable(\[boolean value\])                                                                |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                               |
| public int sizing(\[int value\])                                                                            |                                                                                                                                               |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                               |
| public int topMode(\[int value\])                                                                           |                                                                                                                                               |
| public int topValue(\[int value\])                                                                          |                                                                                                                                               |
| public int type(\[int value\])                                                                              |                                                                                                                                               |
| public str typeName(\[str value\])                                                                          |                                                                                                                                               |
| public int userData(\[int value\])                                                                          |                                                                                                                                               |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                               |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                               |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                               |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                               |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                               |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                               |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                        |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                               |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-assemblyname"></a>メソッド assemblyName

    public str assemblyName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hideifempty"></a>メソッド hideIfEmpty

    public boolean hideIfEmpty([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rtlcapable"></a>メソッド rTLCapable

    public boolean rTLCapable([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-sizing"></a>メソッド sizing

    public int sizing([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-typename"></a>メソッド typeName

    public str typeName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildmenubuttoncontrol"></a>クラス FormBuildMenuButtonControl
    class FormBuildMenuButtonControl extends FormBuildControl

FormBuildMenuButtonControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public int acquireFocus(\[int value\])                                                                      |                                                                                                                                               |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                      |
| public int alignment(\[int value\])                                                                         |                                                                                                                                               |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                           |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                            |
| public boolean autoRefreshData(\[boolean value\])                                                           |                                                                                                                                               |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                             |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                                 |
| public boolean big(\[boolean value\])                                                                       |                                                                                                                                               |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                                   |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                      |
| public int bottomMargin(\[int value\])                                                                      |                                                                                                                                               |
| public int buttonDisplay(\[int value\])                                                                     | ボタン コントロールの外観を取得または設定します。                                                                                            |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                                   |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                                 |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                     |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                               |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                               |
| public boolean defaultButton(\[boolean value\])                                                             | ボタンをフォーム上の既定のボタンにするかどうかを指定します。                                                                       |
| public str disabledImage(\[str value\])                                                                     | コントロールの無効な画像を取得または設定します。                                                                                                |
| public int disabledImageLocation(\[int value\])                                                             |                                                                                                                                               |
| public int disabledResource(\[int value\])                                                                  | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                                                |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                               |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                             |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                           |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                                     |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                                     |
| public boolean forcedToOverflow(\[boolean value\])                                                          |                                                                                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                           |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                       |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                                |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                       |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                      |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                               |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                              |
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                               |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                  |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                               |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                               |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                               |
| public int leftMargin(\[int value\])                                                                        |                                                                                                                                               |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                               |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                               |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         | コントロールに指定されたコントロールを移動します。                                                                                                     |
| public int multiSelect(\[int value\])                                                                       |                                                                                                                                               |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                               |
| public int needsRecord(\[int value\])                                                                       |                                                                                                                                               |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                               |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                               |
| public boolean primary(\[boolean value\])                                                                   |                                                                                                                                               |
| public int rightMargin(\[int value\])                                                                       |                                                                                                                                               |
| public boolean saveRecord(\[boolean value\])                                                                |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                               |
| public int shortkey(\[int value\])                                                                          |                                                                                                                                               |
| public boolean showShortCut(\[boolean value\])                                                              |                                                                                                                                               |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。               |
| public int style(\[int value\])                                                                             |                                                                                                                                               |
| public str text(\[str value\])                                                                              |                                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                               |
| public int topMargin(\[int value\])                                                                         |                                                                                                                                               |
| public int topMode(\[int value\])                                                                           |                                                                                                                                               |
| public int topValue(\[int value\])                                                                          |                                                                                                                                               |
| public int type(\[int value\])                                                                              |                                                                                                                                               |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                           |
| public int userData(\[int value\])                                                                          |                                                                                                                                               |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                               |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                               |
| public boolean useUserLayout(\[boolean value\])                                                             |                                                                                                                                               |
| public boolean value(\[boolean value\])                                                                     |                                                                                                                                               |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                               |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                               |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                               |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                               |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                        |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                               |

### <a name="method-acquirefocus"></a>メソッド acquireFocus

    public int acquireFocus([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-autorefreshdata"></a>メソッド autoRefreshData

    public boolean autoRefreshData([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-big"></a>メソッド big

    public boolean big([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-buttondisplay"></a>メソッド buttonDisplay

ボタン コントロールの外観を取得または設定します。

    public int buttonDisplay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 5 までの整数。

#### <a name="remarks"></a>備考

プロパティ値は、テキスト、画像、またはその両方のいずれをボタンに表示するかを定義します。 このプロパティは、テキストと画像の両方が表示されている場合は、テキストと画像の相対位置も制御します。 返される整数値には、次のようなボタン コントロールの外観が含まれます。

| 値です。 | 説明。                                                     |
|--------|------------------------------------------------------------------|
| 0      | テキストのみ。                                                       |
| 1      | イメージのみ。                                                      |
| 2      | テキストと画像。画像はテキストの下に表示されます。           |
| 3      | テキストと画像。画像はテキストの上に表示されます。           |
| 4      | テキストと画像。画像はテキストの左に表示されます。  |
| 5      | テキストと画像。画像はテキストの右に表示されます。 |

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-defaultbutton"></a>メソッド defaultButton

ボタンをフォーム上の既定のボタンにするかどうかを指定します。

    public boolean defaultButton([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ボタンが既定のボタンである場合は true。それ以外の場合は、false。

### <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

    public str disabledImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画像ファイルのフル ネーム。 システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。

#### <a name="remarks"></a>備考

このプロパティは、disabledResource プロパティに優先します。 これらのプロパティの両方が設定されている場合に使用されます。

### <a name="method-disabledimagelocation"></a>メソッド disabledImageLocation

    public int disabledImageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledresource"></a>メソッド disabledResource

無効なボタン画像として使用する画像リソース ID を取得または設定します。

    public int disabledResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

無効なボタン画像として使用する画像リソース ID。 アイコンとビットマップ イメージの両方がサポートされます。

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-forcedtooverflow"></a>メソッド forcedToOverflow

    public boolean forcedToOverflow([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-keytip"></a>メソッド keyTip

    public str keyTip([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

    public int moveControl(int controlId, [int insertAfterControlId])

#### <a name="parameters"></a>パラメーター

controlId  

<!-- -->

insertAfterControlId  

#### <a name="return-value"></a>戻り値

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

#### <a name="remarks"></a>備考

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

### <a name="method-multiselect"></a>メソッド multiSelect

    public int multiSelect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-needsrecord"></a>メソッド needsRecord

    public int needsRecord([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-primary"></a>メソッド primary

    public boolean primary([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-saverecord"></a>メソッド saveRecord

    public boolean saveRecord([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-shortkey"></a>メソッド shortkey

    public int shortkey([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showshortcut"></a>メソッド showShortCut

    public boolean showShortCut([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-useuserlayout"></a>メソッド useUserLayout

    public boolean useUserLayout([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-value"></a>メソッド value

    public boolean value([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildobjectset"></a>クラス FormBuildObjectSet
    class FormBuildObjectSet extends Object

FormBuildObjectSet クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                         | 説明                                                                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public int id()                |                                                                                                                                         |
| public str name(\[str value\]) | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public void finalize()         |                                                                                                                                         |

### <a name="method-id"></a>メソッド id

    public int id()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-formbuildprogresscontrol"></a>クラス FormBuildProgressControl
    class FormBuildProgressControl extends FormBuildControl

FormBuildProgressControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int direction(\[int value\])                                                                         |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int pos(\[int value\])                                                                               |                                                                                                                                         |
| public int progressType(\[int value\])                                                                      |                                                                                                                                         |
| public int rangeHi(\[int value\])                                                                           |                                                                                                                                         |
| public int rangeLo(\[int value\])                                                                           |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int step(\[int value\])                                                                              |                                                                                                                                         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-pos"></a>メソッド pos

    public int pos([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-progresstype"></a>メソッド progressType

    public int progressType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rangehi"></a>メソッド rangeHi

    public int rangeHi([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rangelo"></a>メソッド rangeLo

    public int rangeLo([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-step"></a>メソッド step

    public int step([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildradiocontrol"></a>クラス FormBuildRadioControl
    class FormBuildRadioControl extends FormBuildControl

FormBuildRadioControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                           |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                         |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                         |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                         |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                         |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                 |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public int columns(\[int value\])                                                                           |                                                                                                                                         |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public EnumId enumType(\[EnumId value\])                                                                    |                                                                                                                                         |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int framePosition(\[int value\])                                                                     |                                                                                                                                         |
| public int frameType(\[int value\])                                                                         |                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public boolean hideFirstEntry(\[boolean value\])                                                            |                                                                                                                                         |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public int item(\[int value\])                                                                              |                                                                                                                                         |
| public int items(\[int value\])                                                                             |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                         |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                         |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                         |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                         |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public int selection(\[int value\])                                                                         |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public str text(\[str value\])                                                                              |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                         |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                         |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-bottommargin"></a>メソッド bottomMargin

    public int bottomMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

    public AutoMode bottomMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

    public int bottomMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

    public str caption([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールのキャプションとして使用される文字列。

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                        |
|--------|-------------------------------|
| 0      | 既定。                      |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。        |

### <a name="method-columns"></a>メソッド columns

    public int columns([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-enumtype"></a>メソッド enumType

    public EnumId enumType([EnumId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-frameposition"></a>メソッド framePosition

    public int framePosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-frametype"></a>メソッド frameType

    public int frameType([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hidefirstentry"></a>メソッド hideFirstEntry

    public boolean hideFirstEntry([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-item"></a>メソッド item

    public int item([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-items"></a>メソッド items

    public int items([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmargin"></a>メソッド leftMargin

    public int leftMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginmode"></a>メソッド leftMarginMode

    public AutoMode leftMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

    public int leftMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmargin"></a>メソッド rightMargin

    public int rightMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginmode"></a>メソッド rightMarginMode

    public AutoMode rightMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

    public int rightMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-selection"></a>メソッド selection

    public int selection([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-text"></a>メソッド text

    public str text([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmargin"></a>メソッド topMargin

    public int topMargin([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginmode"></a>メソッド topMarginMode

    public AutoMode topMarginMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmarginvalue"></a>メソッド topMarginValue

    public int topMarginValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="class-formbuildrealcontrol"></a>クラス FormBuildRealControl
    class FormBuildRealControl extends FormBuildControl

FormBuildRealControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                |
| public int alignment(\[int value\])                                                                         |                                                                                                                                         |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                     |
| public int allowNegative(\[int value\])                                                                     |                                                                                                                                         |
| public int arrayIndex(\[int value\])                                                                        |                                                                                                                                         |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                      |
| public int autoInsSeparator(\[int value\])                                                                  |                                                                                                                                         |
| public int backgroundColor(\[int value\])                                                                   | コントロールの背景色を取得または設定します。                                                                                       |
| public int backStyle(\[int value\])                                                                         | コントロールの背景色を透明にできるかどうかを決定します。                                                                           |
| public int bold(\[int value\])                                                                              | コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。                                                             |
| public int border(\[int value\])                                                                            | コントロールの境界線のスタイルを取得または設定します。                                                                                |
| public int cacheDataMethod(\[int value\])                                                                   |                                                                                                                                         |
| public int characterSet(\[int value\])                                                                      | フォントの文字セットを取得または設定します。                                                                                             |
| public int colorScheme(\[int value\])                                                                       | コントロールの配色を取得または設定します。                                                                                           |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                     |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                               |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                         |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                         |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                         |
| public str dataMethod(\[str value\])                                                                        |                                                                                                                                         |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                         |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                |
| public int decimalSeparator(\[int value\])                                                                  |                                                                                                                                         |
| public int direction(\[int value\])                                                                         |                                                                                                                                         |
| public int displaceNegative(\[int value\], \[AutoMode mode\])                                               |                                                                                                                                         |
| public AutoMode displaceNegativeMode(\[AutoMode mode\])                                                     |                                                                                                                                         |
| public int displaceNegativeValue(\[int value\])                                                             |                                                                                                                                         |
| public int displayHeight(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayHeightMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayHeightValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayLength(\[int value\], \[AutoMode mode\])                                                  |                                                                                                                                         |
| public AutoMode displayLengthMode(\[AutoMode mode\])                                                        |                                                                                                                                         |
| public int displayLengthValue(\[int value\])                                                                |                                                                                                                                         |
| public int displayTarget(\[int value\])                                                                     |                                                                                                                                         |
| public int dragDrop(\[int value\])                                                                          | コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。                                                       |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトを有効または無効にするかどうかを決定します。                                                                                     |
| public ExtendedTypeId extendedDataType(\[ExtendedTypeId value\])                                            |                                                                                                                                         |
| public int fastTabSummary(\[int value\])                                                                    |                                                                                                                                         |
| public str font(\[str value\])                                                                              | 使用するコントロールのフォントの名前を取得または設定します。                                                                               |
| public int fontSize(\[int value\])                                                                          | 使用するコントロールのフォントのサイズを取得または設定します。                                                                               |
| public int foregroundColor(\[int value\])                                                                   | 使用するコントロールのテキストの色を取得または設定します。                                                                                     |
| public int formatMST(\[int value\])                                                                         |                                                                                                                                         |
| public int height(int value, \[int mode\])                                                                  | コントロールの高さを取得または設定します。                                                                                                 |
| public int heightMode(\[int value\])                                                                        | コントロールの高さの計算方法を取得または設定します。                                                                          |
| public int heightValue(\[int value\])                                                                       | コントロールの高さを取得または設定します。                                                                                                 |
| public str helpText(\[str value\])                                                                          | フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。                                |
| public str hierarchyParent(\[str value\])                                                                   |                                                                                                                                         |
| public int id()                                                                                             | コントロールの ID を取得します。                                                                                                        |
| public int iMEMode(\[int value\])                                                                           |                                                                                                                                         |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                            |
| public boolean italic(\[boolean value\])                                                                    |                                                                                                                                         |
| public str label(\[str value\])                                                                             | コントロールのラベルを取得または設定します。                                                                                                   |
| public int labelAlignment(\[int value\])                                                                    |                                                                                                                                         |
| public int labelBold(\[int value\])                                                                         |                                                                                                                                         |
| public int labelCharacterSet(\[int value\])                                                                 |                                                                                                                                         |
| public str labelFont(\[str value\])                                                                         |                                                                                                                                         |
| public int labelFontSize(\[int value\])                                                                     |                                                                                                                                         |
| public int labelForegroundColor(\[int value\])                                                              |                                                                                                                                         |
| public int labelGuide(\[int value\])                                                                        |                                                                                                                                         |
| public int labelHeight(int value, \[int mode\])                                                             |                                                                                                                                         |
| public int labelHeightMode(\[int value\])                                                                   |                                                                                                                                         |
| public int labelHeightValue(\[int value\])                                                                  |                                                                                                                                         |
| public boolean labelItalic(\[boolean value\])                                                               |                                                                                                                                         |
| public int labelPosition(\[int value\])                                                                     |                                                                                                                                         |
| public boolean labelUnderline(\[boolean value\])                                                            |                                                                                                                                         |
| public int labelWidth(int value, \[int mode\])                                                              |                                                                                                                                         |
| public int labelWidthMode(\[int value\])                                                                    |                                                                                                                                         |
| public int labelWidthValue(\[int value\])                                                                   |                                                                                                                                         |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                         |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                         |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                         |
| public int limitText(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                         |
| public AutoMode limitTextMode(\[AutoMode mode\])                                                            |                                                                                                                                         |
| public int limitTextValue(\[int value\])                                                                    |                                                                                                                                         |
| public int lookupButton(\[int value\])                                                                      |                                                                                                                                         |
| public boolean mandatory(\[boolean value\])                                                                 |                                                                                                                                         |
| public int minNoOfDecimals(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode minNoOfDecimalsMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int minNoOfDecimalsValue(\[int value\])                                                              |                                                                                                                                         |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                         |
| public int noOfDecimals(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                         |
| public AutoMode noOfDecimalsMode(\[AutoMode mode\])                                                         |                                                                                                                                         |
| public int noOfDecimalsValue(\[int value\])                                                                 |                                                                                                                                         |
| public int promptrect(\[int value\])                                                                        |                                                                                                                                         |
| public Real realValue(\[Real value\])                                                                       |                                                                                                                                         |
| public boolean replaceOnLookup(\[boolean value\])                                                           |                                                                                                                                         |
| public int rotateSign(\[int value\])                                                                        |                                                                                                                                         |
| public int searchAfterInput(\[int value\])                                                                  |                                                                                                                                         |
| public int searchMode(\[int value\])                                                                        |                                                                                                                                         |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                         |
| public boolean showLabel(\[boolean value\])                                                                 |                                                                                                                                         |
| public int showZero(\[int value\])                                                                          |                                                                                                                                         |
| public int signDisplay(\[int value\])                                                                       |                                                                                                                                         |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。         |
| public int style(\[int value\])                                                                             |                                                                                                                                         |
| public int thousandSeparator(\[int value\])                                                                 |                                                                                                                                         |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                         |
| public int topMode(\[int value\])                                                                           |                                                                                                                                         |
| public int topValue(\[int value\])                                                                          |                                                                                                                                         |
| public int type(\[int value\])                                                                              |                                                                                                                                         |
| public boolean underline(\[boolean value\])                                                                 | コントロール内のテキストの下線プロパティを設定するか返します。                                                                     |
| public int userData(\[int value\])                                                                          |                                                                                                                                         |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                         |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                         |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                         |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                         |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                         |
| public int viewEditMode(\[int value\])                                                                      |                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                         |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                  |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                          |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                  |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                         |

### <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

    public boolean alignControl([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

コントロールの左上隅は、最も長いラベルに従って配置されます。

### <a name="method-alignment"></a>メソッド alignment

    public int alignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

    public boolean allowEdit([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールを編集することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="method-allownegative"></a>メソッド allowNegative

    public int allowNegative([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-arrayindex"></a>メソッド arrayIndex

    public int arrayIndex([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

    public boolean autoDeclaration([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

コントロールには同じ名前を付けることはできません。

### <a name="method-autoinsseparator"></a>メソッド autoInsSeparator

    public int autoInsSeparator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-backgroundcolor"></a>メソッド backgroundColor

コントロールの背景色を取得または設定します。

    public int backgroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-backstyle"></a>メソッド backStyle

コントロールの背景色を透明にできるかどうかを決定します。

    public int backStyle([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールの背景が透明の場合は 1、それ以外の場合は、0 です。

### <a name="method-bold"></a>メソッド bold

コントロール内のテキストを出力するのに使用されるフォントの重量を取得または設定します。

    public int bold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

0 から 9 までの間の整数値。

#### <a name="remarks"></a>備考

返される整数には、次のようなフォントの重量が含まれます。

-   0 既定のフォントの重量を使用します。
-   1 シン。
-   2 エクストラ ライト。
-   3. ライト。
-   4 標準。
-   5 中。
-   6 セミボールド。
-   7 太字。
-   8 極太。
-   9 ヘビー。

### <a name="method-border"></a>メソッド border

コントロールの境界線のスタイルを取得または設定します。

    public int border([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 4 までの整数。

#### <a name="remarks"></a>備考

返される整数には、次のようなコントロールの境界線のスタイルが含まれます。

| 値です。 | 説明。 |
|--------|--------------|
| 0      | 自動。        |
| 1      | 3D。          |
| 2      | 単一明細行。 |
| 3      | 均一。        |
| 4      | なし。        |

### <a name="method-cachedatamethod"></a>メソッド cacheDataMethod

    public int cacheDataMethod([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-characterset"></a>メソッド characterSet

フォントの文字セットを取得または設定します。

    public int characterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

フォントの文字セット示す整数値。

#### <a name="remarks"></a>備考

返される整数の値は、次のテーブルに従って文字セットを示します。

| 値です。 | 説明。         |
|--------|----------------------|
| 0      | ANSI\_CHARSET        |
| 1      | DEFAULT\_CHARSET     |
| 2      | SYMBOL\_CHARSET      |
| 77     | MAC\_CHARSET         |
| 128    | SHIFTJIS\_CHARSET    |
| 129    | HANGUL\_CHARSET      |
| 134    | GB2312\_CHARSET      |
| 136    | CHINESEBIG5\_CHARSET |
| 161    | GREEK\_CHARSET       |
| 162    | TURKISH\_CHARSET     |
| 163    | VIETNAMESE\_CHARSET  |
| 186    | BALTIC\_CHARSET      |
| 204    | RUSSIAN\_CHARSET     |
| 238    | EASTEUROPE\_CHARSET  |
| 255    | OEM\_CHARSET         |

次のテーブルの値は、韓国語版 Microsoft Windows の値です。

| 値です。 | 説明。   |
|--------|----------------|
| 130    | JOHAB\_CHARSET |

次のテーブルの値は、中東言語版用 Microsoft Windows の値です。

| 値です。 | 説明。    |
|--------|-----------------|
| 177    | HEBREW\_CHARSET |
| 178    | ARABIC\_CHARSET |

次のテーブルの値は、タイ語版 Microsoft Windows の値です。

| 値です。 | 説明。  |
|--------|---------------|
| 222    | THAI\_CHARSET |

既定の文字セットは、現在のシステム ロケールに応じて、値に対して設定されます。 たとえば、システム ロケールが英語 (米国) である場合、ANSI\_CHARSET として設定されます。 詳細については [MSDN Web サイト](https://go.microsoft.com/fwlink/?LinkID=85972) で LOGFONT 構造を参照してください。

### <a name="method-colorscheme"></a>メソッド colorScheme

コントロールの配色を取得または設定します。

    public int colorScheme([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ゼロから 2 までの整数。

#### <a name="remarks"></a>備考

配色は次の表に従って定義されます。

| 値です。 | スタイル。                         |
|--------|--------------------------------|
| 0      | 既定。                       |
| 1      | Microsoft Windows パレット。 |
| 2      | 真の配色。         |

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

    public int containerId()

#### <a name="return-value"></a>戻り値

親コンテナーの ID。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

    public FieldId countryRegionContextField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datafield"></a>メソッド dataField

    public FieldId dataField([FieldId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datamethod"></a>メソッド dataMethod

    public str dataMethod([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datarelationpath"></a>メソッド dataRelationPath

    public str dataRelationPath([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

    public int dataSource([AnyType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

使用されるデータ ソースの ID。

### <a name="method-decimalseparator"></a>メソッド decimalSeparator

    public int decimalSeparator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-direction"></a>メソッド direction

    public int direction([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegative"></a>メソッド displaceNegative

    public int displaceNegative([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegativemode"></a>メソッド displaceNegativeMode

    public AutoMode displaceNegativeMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displacenegativevalue"></a>メソッド displaceNegativeValue

    public int displaceNegativeValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheight"></a>メソッド displayHeight

    public int displayHeight([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightmode"></a>メソッド displayHeightMode

    public AutoMode displayHeightMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displayheightvalue"></a>メソッド displayHeightValue

    public int displayHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylength"></a>メソッド displayLength

    public int displayLength([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthmode"></a>メソッド displayLengthMode

    public AutoMode displayLengthMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-displaylengthvalue"></a>メソッド displayLengthValue

    public int displayLengthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-displaytarget"></a>メソッド displayTarget

    public int displayTarget([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

    public int dragDrop([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

### <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

    public boolean enabled([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトが有効である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="method-extendeddatatype"></a>メソッド extendedDataType

    public ExtendedTypeId extendedDataType([ExtendedTypeId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-fasttabsummary"></a>メソッド fastTabSummary

    public int fastTabSummary([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-font"></a>メソッド font

使用するコントロールのフォントの名前を取得または設定します。

    public str font([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

Tahoma や Verdana など、使用するフォントの名前。

### <a name="method-fontsize"></a>メソッド fontSize

使用するコントロールのフォントのサイズを取得または設定します。

    public int fontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ポイント単位のフォントの高さ。

### <a name="method-foregroundcolor"></a>メソッド foregroundColor

使用するコントロールのテキストの色を取得または設定します。

    public int foregroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

パックされた RGB カラーを含む整数。

#### <a name="remarks"></a>備考

返される整数には、次のようにパックされた RGB カラーが含まれます。

-   下位バイトには赤の相対強度の値が含まれています。
-   2 番目のバイトには緑の値が入っています。
-   3 番目のバイトには青の値が入っています。
-   上位バイトはゼロでなければなりません。
-   1 バイトの最大値は 255 です。

### <a name="method-formatmst"></a>メソッド formatMST

    public int formatMST([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

    public int height(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの高さ。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

### <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

    public int heightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

計算モード。

#### <a name="remarks"></a>備考

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

### <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

    public int heightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位の高さ。

#### <a name="remarks"></a>備考

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

### <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

    public str helpText([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画面の下部に表示される文字列。

#### <a name="remarks"></a>備考

プロパティ シートを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

### <a name="method-hierarchyparent"></a>メソッド hierarchyParent

    public str hierarchyParent([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

    public int id()

#### <a name="return-value"></a>戻り値

コントロールの ID。

### <a name="method-imemode"></a>メソッド iMEMode

    public int iMEMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

    public boolean isContainer()

#### <a name="return-value"></a>戻り値

コントロールがコンテナー コントロールかどうかを示すブール値。

### <a name="method-italic"></a>メソッド italic

    public boolean italic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-labelalignment"></a>メソッド labelAlignment

    public int labelAlignment([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelbold"></a>メソッド labelBold

    public int labelBold([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelcharacterset"></a>メソッド labelCharacterSet

    public int labelCharacterSet([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfont"></a>メソッド labelFont

    public str labelFont([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelfontsize"></a>メソッド labelFontSize

    public int labelFontSize([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelforegroundcolor"></a>メソッド labelForegroundColor

    public int labelForegroundColor([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelguide"></a>メソッド labelGuide

    public int labelGuide([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheight"></a>メソッド labelHeight

    public int labelHeight(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightmode"></a>メソッド labelHeightMode

    public int labelHeightMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelheightvalue"></a>メソッド labelHeightValue

    public int labelHeightValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelitalic"></a>メソッド labelItalic

    public boolean labelItalic([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelposition"></a>メソッド labelPosition

    public int labelPosition([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelunderline"></a>メソッド labelUnderline

    public boolean labelUnderline([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidth"></a>メソッド labelWidth

    public int labelWidth(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthmode"></a>メソッド labelWidthMode

    public int labelWidthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-labelwidthvalue"></a>メソッド labelWidthValue

    public int labelWidthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-left"></a>メソッド left

    public int left(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-leftmode"></a>メソッド leftMode

    public int leftMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-leftvalue"></a>メソッド leftValue

    public int leftValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-limittext"></a>メソッド limitText

    public int limitText([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextmode"></a>メソッド limitTextMode

    public AutoMode limitTextMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-limittextvalue"></a>メソッド limitTextValue

    public int limitTextValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-lookupbutton"></a>メソッド lookupButton

    public int lookupButton([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-mandatory"></a>メソッド mandatory

    public boolean mandatory([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-minnoofdecimals"></a>メソッド minNoOfDecimals

    public int minNoOfDecimals([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-minnoofdecimalsmode"></a>メソッド minNoOfDecimalsMode

    public AutoMode minNoOfDecimalsMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-minnoofdecimalsvalue"></a>メソッド minNoOfDecimalsValue

    public int minNoOfDecimalsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
コントロールに割り当てる名前。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始める必要があります。
-   250 文字を超えることはできません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededpermission"></a>メソッド neededPermission

    public int neededPermission([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-noofdecimals"></a>メソッド noOfDecimals

    public int noOfDecimals([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-noofdecimalsmode"></a>メソッド noOfDecimalsMode

    public AutoMode noOfDecimalsMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-noofdecimalsvalue"></a>メソッド noOfDecimalsValue

    public int noOfDecimalsValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-promptrect"></a>メソッド promptrect

    public int promptrect([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-realvalue"></a>メソッド realValue

    public Real realValue([Real value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-replaceonlookup"></a>メソッド replaceOnLookup

    public boolean replaceOnLookup([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-rotatesign"></a>メソッド rotateSign

    public int rotateSign([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchafterinput"></a>メソッド searchAfterInput

    public int searchAfterInput([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-searchmode"></a>メソッド searchMode

    public int searchMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showlabel"></a>メソッド showLabel

    public boolean showLabel([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showzero"></a>メソッド showZero

    public int showZero([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-signdisplay"></a>メソッド signDisplay

    public int signDisplay([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押してコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

    public boolean skip([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの skip プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロールに移動するためにユーザーが TAB キーを押すとコントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="method-style"></a>メソッド style

    public int style([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-thousandseparator"></a>メソッド thousandSeparator

    public int thousandSeparator([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-top"></a>メソッド top

    public int top(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-topmode"></a>メソッド topMode

    public int topMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-topvalue"></a>メソッド topValue

    public int topValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-type"></a>メソッドのタイプ

    public int type([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-underline"></a>メソッド underline

コントロール内のテキストの下線プロパティを設定するか返します。

    public boolean underline([boolean value])

#### <a name="parameters"></a>パラメーター

値  
コントロールの underline プロパティに割り当てる値 (オプション)。

#### <a name="return-value"></a>戻り値

コントロール内のテキストが下線付きである場合は true。それ以外の場合は、false。

### <a name="method-userdata"></a>メソッド userData

    public int userData([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitem"></a>メソッド userDataItem

    public int userDataItem([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-userdataitems"></a>メソッド userDataItems

    public int userDataItems([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacing"></a>メソッド verticalSpacing

    public int verticalSpacing([int value], [AutoMode mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

    public AutoMode verticalSpacingMode([AutoMode mode])

#### <a name="parameters"></a>パラメーター

モード  

#### <a name="return-value"></a>戻り値

### <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

    public int verticalSpacingValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-vieweditmode"></a>メソッド viewEditMode

    public int viewEditMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

    public int width(int value, [int mode])

#### <a name="parameters"></a>パラメーター

値  

<!-- -->

モード  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

### <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

    public int widthMode([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

現在の計算モードを示す整数値。

#### <a name="remarks"></a>備考

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

### <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

    public int widthValue([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ピクセル単位のコントロールの幅。

#### <a name="remarks"></a>備考

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

### <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

    public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])

#### <a name="parameters"></a>パラメーター

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  






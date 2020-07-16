---
title: FormBuildActionPaneTabControl クラス
description: このトピックでは、FormBuildActionPaneTabControl クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9a623622e31bbb71e08741c88df20f30fccd62e3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502658"
---
# <a name="class-formbuildactionpanetabcontrol"></a>クラス FormBuildActionPaneTabControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildActionPaneTabControl extends FormBuildControl
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean alignChild(\[boolean value\])                                                                |                                                                                                                                               |
| public boolean alignChildren(\[boolean value\])                                                             |                                                                                                                                               |
| public boolean alignControl(\[boolean value\])                                                              | コントロールを配置するかどうかを決定します。                                                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                                           |
| public int allowUserSetup(\[int value\])                                                                    |                                                                                                                                               |
| public int arrangeGuide(\[int value\])                                                                      |                                                                                                                                               |
| public int arrangeMethod(\[int value\])                                                                     |                                                                                                                                               |
| public int arrangeWhen(\[int value\])                                                                       |                                                                                                                                               |
| public boolean autoDeclaration(\[boolean value\])                                                           | システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。                                            |
| public int bottomMargin(\[int value\], \[AutoMode mode\])                                                   |                                                                                                                                               |
| public AutoMode bottomMarginMode(\[AutoMode mode\])                                                         |                                                                                                                                               |
| public int bottomMarginValue(\[int value\])                                                                 |                                                                                                                                               |
| public str caption(\[str value\])                                                                           | コントロールのキャプションを取得または設定します。                                                                                                       |
| public int columns(\[int value\], \[ColumnsMode mode\])                                                     |                                                                                                                                               |
| public ColumnsMode columnsMode(\[ColumnsMode mode\])                                                        |                                                                                                                                               |
| public int columnspace(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                               |
| public AutoMode columnspaceMode(\[AutoMode mode\])                                                          |                                                                                                                                               |
| public int columnspaceValue(\[int value\])                                                                  |                                                                                                                                               |
| public int columnsValue(\[int value\])                                                                      |                                                                                                                                               |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                    | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                                           |
| public int containerId()                                                                                    | コントロールの親コンテナーの ID を取得します。                                                                                     |
| public str countryRegionCodes(\[str value\])                                                                |                                                                                                                                               |
| public FieldId countryRegionContextField(\[FieldId value\])                                                 |                                                                                                                                               |
| public str dataRelationPath(\[str value\])                                                                  |                                                                                                                                               |
| public int dataSource(\[AnyType value\])                                                                    | コントロールまたはフォームで使用されるデータ ソースを取得または設定します。                                                                      |
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
| public int imageLocation(\[int value\])                                                                     |                                                                                                                                               |
| public boolean isContainer()                                                                                | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                  |
| public str keyTip(\[str value\])                                                                            |                                                                                                                                               |
| public int left(int value, \[int mode\])                                                                    |                                                                                                                                               |
| public int leftMargin(\[int value\], \[AutoMode mode\])                                                     |                                                                                                                                               |
| public AutoMode leftMarginMode(\[AutoMode mode\])                                                           |                                                                                                                                               |
| public int leftMarginValue(\[int value\])                                                                   |                                                                                                                                               |
| public int leftMode(\[int value\])                                                                          |                                                                                                                                               |
| public int leftValue(\[int value\])                                                                         |                                                                                                                                               |
| public int moveControl(int controlId, \[int insertAfterControlId\])                                         | コントロールに ID で指定されているコントロールを移動します。                                                                                       |
| public str name(\[str value\])                                                                              | フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededPermission(\[int value\])                                                                  |                                                                                                                                               |
| public str normalImage(\[str value\])                                                                       |                                                                                                                                               |
| public int normalResource(\[int value\])                                                                    |                                                                                                                                               |
| public int rightMargin(\[int value\], \[AutoMode mode\])                                                    |                                                                                                                                               |
| public AutoMode rightMarginMode(\[AutoMode mode\])                                                          |                                                                                                                                               |
| public int rightMarginValue(\[int value\])                                                                  |                                                                                                                                               |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                                                   |                                                                                                                                               |
| public boolean skip(\[boolean value\])                                                                      |                                                                                                                                               |
| public int top(int value, \[int mode\])                                                                     |                                                                                                                                               |
| public int topMargin(\[int value\], \[AutoMode mode\])                                                      |                                                                                                                                               |
| public AutoMode topMarginMode(\[AutoMode mode\])                                                            |                                                                                                                                               |
| public int topMarginValue(\[int value\])                                                                    |                                                                                                                                               |
| public int topMode(\[int value\])                                                                           |                                                                                                                                               |
| public int topValue(\[int value\])                                                                          |                                                                                                                                               |
| public int type(\[int value\])                                                                              |                                                                                                                                               |
| public int userData(\[int value\])                                                                          |                                                                                                                                               |
| public int userDataItem(\[int value\])                                                                      |                                                                                                                                               |
| public int userDataItems(\[int value\])                                                                     |                                                                                                                                               |
| public boolean useUserLayout(\[boolean value\])                                                             |                                                                                                                                               |
| public int verticalSpacing(\[int value\], \[AutoMode mode\])                                                |                                                                                                                                               |
| public AutoMode verticalSpacingMode(\[AutoMode mode\])                                                      |                                                                                                                                               |
| public int verticalSpacingValue(\[int value\])                                                              |                                                                                                                                               |
| public boolean visible(\[boolean value\])                                                                   |                                                                                                                                               |
| public int width(int value, \[int mode\])                                                                   | コントロールの幅を取得または設定します。                                                                                                        |
| public int widthMode(\[int value\])                                                                         | コントロールの幅の計算方法を取得または設定します。                                                                                |
| public int widthValue(\[int value\])                                                                        | コントロールの幅を取得または設定します。                                                                                                        |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                               |

## <a name="method-alignchild"></a>メソッド alignChild

```xpp
public boolean alignChild([boolean value])
```

### <a name="parameters---alignchild"></a>パラメーター - alignChild

値  

### <a name="return-value---alignchild"></a>戻り値 - alignChild

## <a name="method-alignchildren"></a>メソッド alignChildren

```xpp
public boolean alignChildren([boolean value])
```

### <a name="parameters---alignchildren"></a>パラメーター - alignChildren

値  

### <a name="return-value---alignchildren"></a>戻り値 - alignChildren

## <a name="method-aligncontrol"></a>メソッド alignControl

コントロールを配置するかどうかを決定します。

```xpp
public boolean alignControl([boolean value])
```

### <a name="parameters---aligncontrol"></a>パラメーター - alignControl

値  

### <a name="return-value---aligncontrol"></a>戻り値 - alignControl

コントロールをアラインする必要がある場合は true。それ以外の場合は false。

### <a name="remarks---aligncontrol"></a>備考 - alignControl

コントロールの左上隅は、最も長いラベルに従って配置されます。

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを編集することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

## <a name="method-allowusersetup"></a>メソッド allowUserSetup

```xpp
public int allowUserSetup([int value])
```

### <a name="parameters---allowusersetup"></a>パラメーター - allowUserSetup

値  

### <a name="return-value---allowusersetup"></a>戻り値 - allowUserSetup

## <a name="method-arrangeguide"></a>メソッド arrangeGuide

```xpp
public int arrangeGuide([int value])
```

### <a name="parameters---arrangeguide"></a>パラメーター - arrangeGuide

値  

### <a name="return-value---arrangeguide"></a>戻り値 - arrangeGuide

## <a name="method-arrangemethod"></a>メソッド arrangeMethod

```xpp
public int arrangeMethod([int value])
```

### <a name="parameters---arrangemethod"></a>パラメーター - arrangeMethod

値  

### <a name="return-value---arrangemethod"></a>戻り値 - arrangeMethod

## <a name="method-arrangewhen"></a>メソッド arrangeWhen

```xpp
public int arrangeWhen([int value])
```

### <a name="parameters---arrangewhen"></a>パラメーター - arrangeWhen

値  

### <a name="return-value---arrangewhen"></a>戻り値 - arrangeWhen

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

システムがコントロールと同じ名前を持つメンバー変数を宣言できるかどうかを決定します。

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

このコントロールのためにメンバー変数を宣言することができる場合は true。それ以外の場合は、false。

### <a name="remarks---autodeclaration"></a>備考 - autoDeclaration

コントロールには同じ名前を付けることはできません。

## <a name="method-bottommargin"></a>メソッド bottomMargin

```xpp
public int bottomMargin([int value], [AutoMode mode])
```

### <a name="parameters---bottommargin"></a>パラメーター - bottomMargin

値  

<!-- -->

モード  

### <a name="return-value---bottommargin"></a>戻り値 - bottomMargin

## <a name="method-bottommarginmode"></a>メソッド bottomMarginMode

```xpp
public AutoMode bottomMarginMode([AutoMode mode])
```

### <a name="parameters---bottommarginmode"></a>パラメーター - bottomMarginMode

モード  

### <a name="return-value---bottommarginmode"></a>戻り値 - bottomMarginMode

## <a name="method-bottommarginvalue"></a>メソッド bottomMarginValue

```xpp
public int bottomMarginValue([int value])
```

### <a name="parameters---bottommarginvalue"></a>パラメーター - bottomMarginValue

値  

### <a name="return-value---bottommarginvalue"></a>戻り値 - bottomMarginValue

## <a name="method-caption"></a>メソッド caption

コントロールのキャプションを取得または設定します。

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  

### <a name="return-value---caption"></a>戻り値 - caption

コントロールのキャプションとして使用される文字列。

## <a name="method-columns"></a>メソッド columns

```xpp
public int columns([int value], [ColumnsMode mode])
```

### <a name="parameters---columns"></a>パラメーター - columns

値  

<!-- -->

モード  

### <a name="return-value---columns"></a>戻り値 - columns

## <a name="method-columnsmode"></a>メソッド columnsMode

```xpp
public ColumnsMode columnsMode([ColumnsMode mode])
```

### <a name="parameters---columnsmode"></a>パラメーター - columnsMode

モード  

### <a name="return-value---columnsmode"></a>戻り値 - columnsMode

## <a name="method-columnspace"></a>メソッド columnspace

```xpp
public int columnspace([int value], [AutoMode mode])
```

### <a name="parameters---columnspace"></a>パラメーター - columnspace

値  

<!-- -->

モード  

### <a name="return-value---columnspace"></a>戻り値 - columnspace

## <a name="method-columnspacemode"></a>メソッド columnspaceMode

```xpp
public AutoMode columnspaceMode([AutoMode mode])
```

### <a name="parameters---columnspacemode"></a>パラメーター - columnspaceMode

モード  

### <a name="return-value---columnspacemode"></a>戻り値 - columnspaceMode

## <a name="method-columnspacevalue"></a>メソッド columnspaceValue

```xpp
public int columnspaceValue([int value])
```

### <a name="parameters---columnspacevalue"></a>パラメーター - columnspaceValue

値  

### <a name="return-value---columnspacevalue"></a>戻り値 - columnspaceValue

## <a name="method-columnsvalue"></a>メソッド columnsValue

```xpp
public int columnsValue([int value])
```

### <a name="parameters---columnsvalue"></a>パラメーター - columnsValue

値  

### <a name="return-value---columnsvalue"></a>戻り値 - columnsValue

## <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

コントロールに割り当てられるコンフィギュレーションの ID。

### <a name="remarks---configurationkey"></a>備考 - configurationKey

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

## <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a>戻り値 - containerId

親コンテナーの ID。

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a>パラメーター - countryRegionCodes

値  

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

## <a name="method-countryregioncontextfield"></a>メソッド countryRegionContextField

```xpp
public FieldId countryRegionContextField([FieldId value])
```

### <a name="parameters---countryregioncontextfield"></a>パラメーター - countryRegionContextField

値  

### <a name="return-value---countryregioncontextfield"></a>戻り値 - countryRegionContextField

## <a name="method-datarelationpath"></a>メソッド dataRelationPath

```xpp
public str dataRelationPath([str value])
```

### <a name="parameters---datarelationpath"></a>パラメーター - dataRelationPath

値  

### <a name="return-value---datarelationpath"></a>戻り値 - dataRelationPath

## <a name="method-datasource"></a>メソッド dataSource

コントロールまたはフォームで使用されるデータ ソースを取得または設定します。

```xpp
public int dataSource([AnyType value])
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

値  

### <a name="return-value---datasource"></a>戻り値 - dataSource

使用されるデータ ソースの ID。

## <a name="method-displaytarget"></a>メソッド displayTarget

```xpp
public int displayTarget([int value])
```

### <a name="parameters---displaytarget"></a>パラメーター - displayTarget

値  

### <a name="return-value---displaytarget"></a>戻り値 - displayTarget

## <a name="method-dragdrop"></a>メソッド dragDrop

コントロールのドラッグ アンド ドロップ操作を有効または無効にするかどうかを決定します。

```xpp
public int dragDrop([int value])
```

### <a name="parameters---dragdrop"></a>パラメーター - dragDrop

値  

### <a name="return-value---dragdrop"></a>戻り値 - dragDrop

ドラッグ アンド ドロップ操作が有効な場合は 1、それ以外の場合は、false です。

## <a name="method-enabled"></a>メソッド enabled

オブジェクトを有効または無効にするかどうかを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供する、エラー メッセージなどの、表示のためにのみ使用されるコントロールを無効にすることもできます。

## <a name="method-height"></a>メソッド height

コントロールの高さを取得または設定します。

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a>パラメーター - height

値  

<!-- -->

モード  

### <a name="return-value---height"></a>戻り値 - height

ピクセル単位のコントロールの高さ。

### <a name="remarks---height"></a>備考 - height

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って高さを計算します:

| モード。            | 高さの計算。                                                                       |
|------------------|-------------------------------------------------------------------------------------------|
| -1 正確。        | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 0 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 1 列の高さ。 | フォームのレイアウトによって、コントロールの高さが決まります。                              |

高さと高さ計算モードは別々に設定できます。

## <a name="method-heightmode"></a>メソッド heightMode

コントロールの高さの計算方法を取得または設定します。

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a>パラメーター - heightMode

値  

### <a name="return-value---heightmode"></a>戻り値 - heightMode

計算モード。

### <a name="remarks---heightmode"></a>備考 - heightMode

次の表に従って高さを計算します:

| モード。          | 高さの計算。                                                                       |
|----------------|-------------------------------------------------------------------------------------------|
| 正確。         | コントロールのピクセル単位の正確な高さが使用されます。                                       |
| 自動。          | コントロールの高さは自動的に計算され、value パラメーターは無視されます。 |
| 列の高さ | フォームのレイアウトによって、コントロールの高さが決まります。                              |

計算モードが [自動] または [列の高さ] に設定されている場合は、コントロールの高さが変わることがあります。

## <a name="method-heightvalue"></a>メソッド heightValue

コントロールの高さを取得または設定します。

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

ピクセル単位の高さ。

### <a name="remarks---heightvalue"></a>備考 - heightValue

正確な高さ計算モードが使用されていない限り、コントロールの高さは変更されません。

## <a name="method-helptext"></a>メソッド helpText

フィールドやコントロールのポイント時に、画面の下部に表示されるヘルプ テキストを取得または設定します。

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

画面の下部に表示される文字列。

### <a name="remarks---helptext"></a>備考 - helpText

プロパティ ダイアログ ボックスを使用してオブジェクトの HelpText プロパティを設定します。 ヘルプ テキストは 250 文字を超えてはいけません。

## <a name="method-hideifempty"></a>メソッド hideIfEmpty

```xpp
public boolean hideIfEmpty([boolean value])
```

### <a name="parameters---hideifempty"></a>パラメーター - hideIfEmpty

値  

### <a name="return-value---hideifempty"></a>戻り値 - hideIfEmpty

## <a name="method-hierarchyparent"></a>メソッド hierarchyParent

```xpp
public str hierarchyParent([str value])
```

### <a name="parameters---hierarchyparent"></a>パラメーター - hierarchyParent

値  

### <a name="return-value---hierarchyparent"></a>戻り値 - hierarchyParent

## <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

コントロールの ID。

## <a name="method-imagelocation"></a>メソッド imageLocation

```xpp
public int imageLocation([int value])
```

### <a name="parameters---imagelocation"></a>パラメーター - imageLocation

値  

### <a name="return-value---imagelocation"></a>戻り値 - imageLocation

## <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

コントロールがコンテナー コントロールかどうかを示すブール値。

## <a name="method-keytip"></a>メソッド keyTip

```xpp
public str keyTip([str value])
```

### <a name="parameters---keytip"></a>パラメーター - keyTip

値  

### <a name="return-value---keytip"></a>戻り値 - keyTip

## <a name="method-left"></a>メソッド left

```xpp
public int left(int value, [int mode])
```

### <a name="parameters---left"></a>パラメーター - left

値  

<!-- -->

モード  

### <a name="return-value---left"></a>戻り値 - left

## <a name="method-leftmargin"></a>メソッド leftMargin

```xpp
public int leftMargin([int value], [AutoMode mode])
```

### <a name="parameters---leftmargin"></a>パラメーター - leftMargin

値  

<!-- -->

モード  

### <a name="return-value---leftmargin"></a>戻り値 - leftMargin

## <a name="method-leftmarginmode"></a>メソッド leftMarginMode

```xpp
public AutoMode leftMarginMode([AutoMode mode])
```

### <a name="parameters---leftmarginmode"></a>パラメーター - leftMarginMode

モード  

### <a name="return-value---leftmarginmode"></a>戻り値 - leftMarginMode

## <a name="method-leftmarginvalue"></a>メソッド leftMarginValue

```xpp
public int leftMarginValue([int value])
```

### <a name="parameters---leftmarginvalue"></a>パラメーター - leftMarginValue

値  

### <a name="return-value---leftmarginvalue"></a>戻り値 - leftMarginValue

## <a name="method-leftmode"></a>メソッド leftMode

```xpp
public int leftMode([int value])
```

### <a name="parameters---leftmode"></a>パラメーター - leftMode

値  

### <a name="return-value---leftmode"></a>戻り値 - leftMode

## <a name="method-leftvalue"></a>メソッド leftValue

```xpp
public int leftValue([int value])
```

### <a name="parameters---leftvalue"></a>パラメーター - leftValue

値  

### <a name="return-value---leftvalue"></a>戻り値 - leftValue

## <a name="method-movecontrol"></a>メソッド moveControl

コントロールに ID で指定されているコントロールを移動します。

```xpp
public int moveControl(int controlId, [int insertAfterControlId])
```

### <a name="parameters---movecontrol"></a>パラメーター - moveControl

controlId  

<!-- -->

insertAfterControlId  

### <a name="return-value---movecontrol"></a>戻り値 - moveControl

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

### <a name="remarks---movecontrol"></a>備考 - moveControl

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - 名前

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - 名前

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-neededpermission"></a>メソッド neededPermission

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a>パラメーター - neededPermission

値  

### <a name="return-value---neededpermission"></a>戻り値 - neededPermission

## <a name="method-normalimage"></a>メソッド normalImage

```xpp
public str normalImage([str value])
```

### <a name="parameters---normalimage"></a>パラメーター - normalImage

値  

### <a name="return-value---normalimage"></a>戻り値 - normalImage

## <a name="method-normalresource"></a>メソッド normalResource

```xpp
public int normalResource([int value])
```

### <a name="parameters---normalresource"></a>パラメーター - normalResource

値  

### <a name="return-value---normalresource"></a>戻り値 - normalResource

## <a name="method-rightmargin"></a>メソッド rightMargin

```xpp
public int rightMargin([int value], [AutoMode mode])
```

### <a name="parameters---rightmargin"></a>パラメーター - rightMargin

値  

<!-- -->

モード  

### <a name="return-value---rightmargin"></a>戻り値 - rightMargin

## <a name="method-rightmarginmode"></a>メソッド rightMarginMode

```xpp
public AutoMode rightMarginMode([AutoMode mode])
```

### <a name="parameters---rightmarginmode"></a>パラメーター - rightMarginMode

モード  

### <a name="return-value---rightmarginmode"></a>戻り値 - rightMarginMode

## <a name="method-rightmarginvalue"></a>メソッド rightMarginValue

```xpp
public int rightMarginValue([int value])
```

### <a name="parameters---rightmarginvalue"></a>パラメーター - rightMarginValue

値  

### <a name="return-value---rightmarginvalue"></a>戻り値 - rightMarginValue

## <a name="method-securitykey"></a>メソッド securityKey

```xpp
public SecurityKeyId securityKey([SecurityKeyId value])
```

### <a name="parameters---securitykey"></a>パラメーター - securityKey

値  

### <a name="return-value---securitykey"></a>戻り値 - securityKey

## <a name="method-skip"></a>メソッド skip

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  

### <a name="return-value---skip"></a>戻り値 - skip

## <a name="method-top"></a>メソッド top

```xpp
public int top(int value, [int mode])
```

### <a name="parameters---top"></a>パラメーター - top

値  

<!-- -->

モード  

### <a name="return-value---top"></a>戻り値 - top

## <a name="method-topmargin"></a>メソッド topMargin

```xpp
public int topMargin([int value], [AutoMode mode])
```

### <a name="parameters---topmargin"></a>パラメーター - topMargin

値  

<!-- -->

モード  

### <a name="return-value---topmargin"></a>戻り値 - topMargin

## <a name="method-topmarginmode"></a>メソッド topMarginMode

```xpp
public AutoMode topMarginMode([AutoMode mode])
```

### <a name="parameters---topmarginmode"></a>パラメーター - topMarginMode

モード  

### <a name="return-value---topmarginmode"></a>戻り値 - topMarginMode

## <a name="method-topmarginvalue"></a>メソッド topMarginValue

```xpp
public int topMarginValue([int value])
```

### <a name="parameters---topmarginvalue"></a>パラメーター - topMarginValue

値  

### <a name="return-value---topmarginvalue"></a>戻り値 - topMarginValue

## <a name="method-topmode"></a>メソッド topMode

```xpp
public int topMode([int value])
```

### <a name="parameters---topmode"></a>パラメーター - topMode

値  

### <a name="return-value---topmode"></a>戻り値 - topMode

## <a name="method-topvalue"></a>メソッド topValue

```xpp
public int topValue([int value])
```

### <a name="parameters---topvalue"></a>パラメーター - topValue

値  

### <a name="return-value---topvalue"></a>戻り値 - topValue

## <a name="method-type"></a>メソッドのタイプ

```xpp
public int type([int value])
```

### <a name="parameters---type"></a>パラメーター - タイプ

値  

### <a name="return-value---type"></a>戻り値 - type

## <a name="method-userdata"></a>メソッド userData

```xpp
public int userData([int value])
```

### <a name="parameters---userdata"></a>パラメーター - userData

値  

### <a name="return-value---userdata"></a>戻り値 - userData

## <a name="method-userdataitem"></a>メソッド userDataItem

```xpp
public int userDataItem([int value])
```

### <a name="parameters---userdataitem"></a>パラメーター - userDataItem

値  

### <a name="return-value---userdataitem"></a>戻り値 - userDataItem

## <a name="method-userdataitems"></a>メソッド userDataItems

```xpp
public int userDataItems([int value])
```

### <a name="parameters---userdataitems"></a>パラメーター - userDataItems

値  

### <a name="return-value---userdataitems"></a>戻り値 - userDataItems

## <a name="method-useuserlayout"></a>メソッド useUserLayout

```xpp
public boolean useUserLayout([boolean value])
```

### <a name="parameters---useuserlayout"></a>パラメーター - useUserLayout

値  

### <a name="return-value---useuserlayout"></a>戻り値 - useUserLayout

## <a name="method-verticalspacing"></a>メソッド verticalSpacing

```xpp
public int verticalSpacing([int value], [AutoMode mode])
```

### <a name="parameters---verticalspacing"></a>パラメーター - verticalSpacing

値  

<!-- -->

モード  

### <a name="return-value---verticalspacing"></a>戻り値 - verticalSpacing

## <a name="method-verticalspacingmode"></a>メソッド verticalSpacingMode

```xpp
public AutoMode verticalSpacingMode([AutoMode mode])
```

### <a name="parameters---verticalspacingmode"></a>パラメーター - verticalSpacingMode

モード  

### <a name="return-value---verticalspacingmode"></a>戻り値 - verticalSpacingMode

## <a name="method-verticalspacingvalue"></a>メソッド verticalSpacingValue

```xpp
public int verticalSpacingValue([int value])
```

### <a name="parameters---verticalspacingvalue"></a>パラメーター - verticalSpacingValue

値  

### <a name="return-value---verticalspacingvalue"></a>戻り値 - verticalSpacingValue

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-width"></a>メソッド width

コントロールの幅を取得または設定します。

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  

<!-- -->

モード  

### <a name="return-value---width"></a>戻り値 - width

ピクセル単位のコントロールの幅。

### <a name="remarks---width"></a>備考 - width

値のパラメータを省略すると、正確なモードが使用されます。 次の表に従って幅を計算します:

| モード。           | 幅計算。                                                                       |
|-----------------|------------------------------------------------------------------------------------------|
| -1 正確。       | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 0 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 1 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

幅と幅計算モードは別々に設定できます。

## <a name="method-widthmode"></a>メソッド widthMode

コントロールの幅の計算方法を取得または設定します。

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthValue

値  

### <a name="return-value---widthmode"></a>戻り値 - widthMode

現在の計算モードを示す整数値。

### <a name="remarks---widthmode"></a>備考 - widthMode

次の表に従って幅を計算します:

| モード。         | 幅計算。                                                                       |
|---------------|------------------------------------------------------------------------------------------|
| 正確。        | コントロールのピクセル単位の正確な幅が使用されます。                                       |
| 自動。         | コントロールの幅は自動的に計算され、value パラメーターは無視されます。 |
| 列の幅。 | フォームのレイアウトによって、コントロールの幅が決まります。                              |

モードが [自動] または [列の幅] に設定されている場合は、コントロールの幅が変わることがあります。

## <a name="method-widthvalue"></a>メソッド widthValue

コントロールの幅を取得または設定します。

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

ピクセル単位のコントロールの幅。

### <a name="remarks---widthvalue"></a>備考 - widthValue

コントロールの幅を変更するには、正確な幅の計算モードを使用します。

## <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a>パラメーター - registerOverrideMethod

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  


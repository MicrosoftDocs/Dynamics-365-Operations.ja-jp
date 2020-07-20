---
title: FormBuildControl クラス
description: このトピックでは、FormBuildControl クラスについて説明します。
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
ms.openlocfilehash: 8a2d9dd0aa0f8d5ebc81e5b0a233b2b7071e9a31
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502970"
---
# <a name="class-formbuildcontrol"></a>クラス FormBuildControl

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildControl extends Object
```

FormBuildControl クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                    | 説明                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| public FormBuildControl addControl(FormControlType controlType, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\]) | 指定したコントロール タイプに基づいて、コントロールにコントロールを追加します。                                                                                |
| public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\])          |                                                                                                                                                    |
| public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                                               | 指定したデータ フィールド情報に基づいて、コントロールにコントロールを追加します。                                                                      |
| public boolean allowEdit(\[boolean value\])                                                                                               |                                                                                                                                                    |
| public boolean autoDeclaration(\[boolean value\])                                                                                         |                                                                                                                                                    |
| public boolean canAddDataField(int dataSourceId, FieldId fieldId, \[int arrayIndex\])                                                     | 指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示す値を取得します。                                  |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])                                                                  |                                                                                                                                                    |
| public int containerId()                                                                                                                  | コントロールの親コンテナーの ID を取得します。                                                                                          |
| public int controlCount()                                                                                                                 | コントロールに含まれるコントロールの数を取得します。                                                                                |
| public FormBuildControl controlNum(int controlNo)                                                                                         | 指定したインデックスを使用して、上位のコントロールを取得します。                                                                                        |
| public str countryRegionCodes(\[str value\])                                                                                              |                                                                                                                                                    |
| public boolean editAutoPostback(\[boolean value\])                                                                                        |                                                                                                                                                    |
| public boolean enabled(\[boolean value\])                                                                                                 |                                                                                                                                                    |
| public str helpText(\[str value\])                                                                                                        |                                                                                                                                                    |
| public str extendedStyle(\[str value\])                                                                                                   |                                                                                                                                                    |
| public int height(int value, \[int mode\])                                                                                                |                                                                                                                                                    |
| public int heightMode(\[int value\])                                                                                                      |                                                                                                                                                    |
| public int heightValue(\[int value\])                                                                                                     |                                                                                                                                                    |
| public str GetXppILImplementation()                                                                                                       |                                                                                                                                                    |
| public boolean hasUserSetting()                                                                                                           | コントロールにカスタム ユーザー設定があるかどうかを示します。                                                                                            |
| public int id()                                                                                                                           | コントロールの ID を取得します。                                                                                                                   |
| public boolean isContainer()                                                                                                              | コントロールがコンテナー コントロールかどうかを示す値を取得します。                                                                       |
| public boolean markAsUserAdd(\[boolean value\])                                                                                           | ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。                                                                                              |
| public int moveControl(int controlId, \[int insertAfterId\])                                                                              | コントロールに指定されたコントロールを移動します。                                                                                                          |
| public str name(\[str value\])                                                                                                            |                                                                                                                                                    |
| public int neededPermission(\[int value\])                                                                                                |                                                                                                                                                    |
| public container SysObsoleteAttribute()                                                                                                   |                                                                                                                                                    |
| public str previewPartRef(\[str value\])                                                                                                  |                                                                                                                                                    |
| public boolean skip(\[boolean value\])                                                                                                    |                                                                                                                                                    |
| public boolean SysObsoleteAttribute(container data)                                                                                       |                                                                                                                                                    |
| public int userDisable(\[int value\])                                                                                                     | ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。                                                                |
| public int userHeight(\[int value\])                                                                                                      | コントロールのカスタム ユーザーの高さを取得または設定します。                                                                                               |
| public int userHide(\[int value\])                                                                                                        | コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。                                                                 |
| public int userOrgContainer(\[int value\])                                                                                                | コントロールの組織コンテナを取得または設定します。                                                                                           |
| public int userOrgSibling(\[int value\])                                                                                                  | コントロールの組織兄弟を取得または設定します。                                                                                             |
| public str userPromptText(\[str value\])                                                                                                  | コントロールのユーザーラベル テキストを取得または設定します。                                                                                                  |
| public int userSecurityLevel(\[int value\])                                                                                               | コントロールのユーザー セキュリティ レベルを取得または設定します。                                                                                              |
| public int userSkip(\[int value\])                                                                                                        | ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。 |
| public int userWidth(\[int value\])                                                                                                       | ピクセル単位でコントロールの幅を設定するか返します。                                                                                                |
| public boolean visible(\[boolean value\])                                                                                                 |                                                                                                                                                    |
| public int width(int value, \[int mode\])                                                                                                 |                                                                                                                                                    |
| public int widthMode(\[int value\])                                                                                                       |                                                                                                                                                    |
| public int widthValue(\[int value\])                                                                                                      |                                                                                                                                                    |
| public void RegisterXppILImplementation(str className)                                                                                    |                                                                                                                                                    |
| public void new(FormContainer container)                                                                                                  |                                                                                                                                                    |
| public void resetUserSetting()                                                                                                            | コントロールのユーザー設定をリセットします。                                                                                                          |

## <a name="method-addcontrol"></a>メソッド addControl

指定したコントロール タイプに基づいて、コントロールにコントロールを追加します。

```xpp
public FormBuildControl addControl(FormControlType controlType, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrol"></a>パラメーター - addControl

controlType  
新しいコントロールの名前を設定する文字列値。

<!-- -->

controlName  
新しいコントロールの名前を設定する文字列値。

<!-- -->

insertAfter  

<!-- -->

pushFront  

### <a name="return-value---addcontrol"></a>戻り値 - addControl

新たに追加されたコントロールを表す FormBuildControl オブジェクトです。

## <a name="method-addcontrolex"></a>メソッド addControlEx

```xpp
public FormBuildControl addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrolex"></a>パラメーター - addControlEx

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

### <a name="return-value---addcontrolex"></a>戻り値 - addControlEx

## <a name="method-adddatafield"></a>メソッド addDataField

指定したデータ フィールド情報に基づいて、コントロールにコントロールを追加します。

```xpp
public FormBuildControl addDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---adddatafield"></a>パラメーター - addDataField

dataSourceId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

fieldId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

arrayIndex  
データ フィールド型のインデックスを示す整数値。オプション。

### <a name="return-value---adddatafield"></a>戻り値 - addDataField

新たに追加されたコントロールを表す FormBuildControl オブジェクトです。

### <a name="remarks---adddatafield"></a>備考 - addDataField

追加するコントロールのタイプは、指定されたデータ フィールド情報に基づいて自動的に決定されます。 値が指定されていないときは、arrayIndex パラメーターが既定値の 1 であるため、最初のインデックスが想定されます。

## <a name="method-allowedit"></a>メソッド allowEdit

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

## <a name="method-autodeclaration"></a>メソッド autoDeclaration

```xpp
public boolean autoDeclaration([boolean value])
```

### <a name="parameters---autodeclaration"></a>パラメーター - autoDeclaration

値  

### <a name="return-value---autodeclaration"></a>戻り値 - autoDeclaration

## <a name="method-canadddatafield"></a>メソッド canAddDataField

指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示す値を取得します。

```xpp
public boolean canAddDataField(int dataSourceId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---canadddatafield"></a>パラメーター - canAddDataField

dataSourceId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

fieldId  
データ フィールド型のインデックスを示す整数値。オプション。

<!-- -->

arrayIndex  
データ フィールド型のインデックスを示す整数値。オプション。

### <a name="return-value---canadddatafield"></a>戻り値 - canAddDataField

指定されたデータ フィールドを、子コントロールとしてコントロールに追加できるかどうかを示すブール値。

## <a name="method-configurationkey"></a>メソッド configurationKey

```xpp
public ConfigurationKeyId configurationKey([ConfigurationKeyId value])
```

### <a name="parameters---configurationkey"></a>パラメーター - configurationKey

値  

### <a name="return-value---configurationkey"></a>戻り値 - configurationKey

## <a name="method-containerid"></a>メソッド containerId

コントロールの親コンテナーの ID を取得します。

```xpp
public int containerId()
```

### <a name="return-value---containerid"></a>戻り値 - containerId

親コンテナーの ID。

## <a name="method-controlcount"></a>メソッド controlCount

コントロールに含まれるコントロールの数を取得します。

```xpp
public int controlCount()
```

### <a name="return-value---controlcount"></a>戻り値 - controlCount

コンテナー コントロールの場合、コントロール内に含まれているコントロールの数を示す整数値。それ以外の場合は、0 。

## <a name="method-controlnum"></a>メソッド controlNum

指定したインデックスを使用して、上位のコントロールを取得します。

```xpp
public FormBuildControl controlNum(int controlNo)
```

### <a name="parameters---controlnum"></a>パラメーター - controlNum

controlNo  
取得する子コントロールのインデックスを示す整数値。

### <a name="return-value---controlnum"></a>戻り値 - controlNum

コンテナー コントロールである場合は、指定されたインデックスを持つ子コントロールを表す FormBuildControl オブジェクト; それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="remarks---controlnum"></a>備考 - controlNum

指定した controlNo パラメーターが範囲外にある場合は、例外が発生します。

## <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

```xpp
public str countryRegionCodes([str value])
```

### <a name="parameters---countryregioncodes"></a>パラメーター - countryRegionCodes

値  

### <a name="return-value---countryregioncodes"></a>戻り値 - countryRegionCodes

## <a name="method-editautopostback"></a>メソッド editAutoPostback

```xpp
public boolean editAutoPostback([boolean value])
```

### <a name="parameters---editautopostback"></a>パラメーター - editAutoPostback

値  

### <a name="return-value---editautopostback"></a>戻り値 - editAutoPostback

## <a name="method-enabled"></a>メソッド enabled

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  

### <a name="return-value---enabled"></a>戻り値 - enabled

## <a name="method-helptext"></a>メソッド helpText

```xpp
public str helpText([str value])
```

### <a name="parameters---helptext"></a>パラメーター - helpText

値  

### <a name="return-value---helptext"></a>戻り値 - helpText

## <a name="method-extendedstyle"></a>メソッド extendedStyle

```xpp
public str extendedStyle([str value])
```

### <a name="parameters---extendedstyle"></a>パラメーター - extendedStyle

値  

### <a name="return-value---extendedstyle"></a>戻り値 - extendedStyle

## <a name="method-height"></a>メソッド height

```xpp
public int height(int value, [int mode])
```

### <a name="parameters---height"></a>パラメーター - height

値  

<!-- -->

モード  

### <a name="return-value---height"></a>戻り値 - height

## <a name="method-heightmode"></a>メソッド heightMode

```xpp
public int heightMode([int value])
```

### <a name="parameters---heightmode"></a>パラメーター - heightMode

値  

### <a name="return-value---heightmode"></a>戻り値 - heightMode

## <a name="method-heightvalue"></a>メソッド heightValue

```xpp
public int heightValue([int value])
```

### <a name="parameters---heightvalue"></a>パラメーター - heightValue

値  

### <a name="return-value---heightvalue"></a>戻り値 - heightValue

## <a name="method-getxppilimplementation"></a>メソッド GetXppILImplementation

```xpp
public str GetXppILImplementation()
```

### <a name="return-value---getxppilimplementation"></a>戻り値 - GetXppILImplementation

## <a name="method-hasusersetting"></a>メソッド hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示します。

```xpp
public boolean hasUserSetting()
```

### <a name="return-value---hasusersetting"></a>戻り値 - hasUserSetting

コントロールにカスタム ユーザー設定があるかどうかを示すブール値。

## <a name="method-id"></a>メソッド id

コントロールの ID を取得します。

```xpp
public int id()
```

### <a name="return-value---id"></a>戻り値 - id

コントロールの ID。

## <a name="method-iscontainer"></a>メソッド isContainer

コントロールがコンテナー コントロールかどうかを示す値を取得します。

```xpp
public boolean isContainer()
```

### <a name="return-value---iscontainer"></a>戻り値 - isContainer

コントロールがコンテナー コントロールかどうかを示すブール値。

## <a name="method-markasuseradd"></a>メソッド markAsUserAdd

ユーザーが追加したコントロールとしてコントロールをマークしたりマークを解除したりします。

```xpp
public boolean markAsUserAdd([boolean value])
```

### <a name="parameters---markasuseradd"></a>パラメーター - markAsUserAdd

値  
コントロールをユーザーが追加したコントロールとしてマークするかどうかを示すブール値。

### <a name="return-value---markasuseradd"></a>戻り値 - markAsUserAdd

ユーザーが追加したコントロールとして、コントロールがマークされたかどうかを示すブール値。

## <a name="method-movecontrol"></a>メソッド moveControl

コントロールに指定されたコントロールを移動します。

```xpp
public int moveControl(int controlId, [int insertAfterId])
```

### <a name="parameters---movecontrol"></a>パラメーター - moveControl

controlId  
後にコントロールを挿入するコントロールの ID を示す整数値。オプション。

<!-- -->

insertAfterId  
後にコントロールを挿入するコントロールの ID を示す整数値。オプション。

### <a name="return-value---movecontrol"></a>戻り値 - moveControl

コントロールが正常に移動した場合は 1、それ以外の場合、0 です。

### <a name="remarks---movecontrol"></a>備考 - moveControl

一般に、指定したコントロールをコントロールに含めることができ、現在のコンテナーから移動できる場合、このメソッドは成功します。 ただし、場合によっては、参照グループ コントロールのインスタンス コントロールなど、コントロールを移動できません。

## <a name="method-name"></a>メソッド名

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - 名前

値  

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-neededpermission"></a>メソッド neededPermission

```xpp
public int neededPermission([int value])
```

### <a name="parameters---neededpermission"></a>パラメーター - neededPermission

値  

### <a name="return-value---neededpermission"></a>戻り値 - neededPermission

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public container SysObsoleteAttribute()
```

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-previewpartref"></a>メソッド previewPartRef

```xpp
public str previewPartRef([str value])
```

### <a name="parameters---previewpartref"></a>パラメーター - previewPartRef

値  

### <a name="return-value---previewpartref"></a>戻り値 - previewPartRef

## <a name="method-skip"></a>メソッド skip

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  

### <a name="return-value---skip"></a>戻り値 - skip

## <a name="method-sysobsoleteattribute"></a>メソッド SysObsoleteAttribute

```xpp
public boolean SysObsoleteAttribute(container data)
```

### <a name="parameters---sysobsoleteattribute"></a>パラメーター - SysObsoleteAttribute

データ  

### <a name="return-value---sysobsoleteattribute"></a>戻り値 - SysObsoleteAttribute

## <a name="method-userdisable"></a>メソッド userDisable

ユーザーのコントロールが無効になっているかどうかを示す値を取得または設定します。

```xpp
public int userDisable([int value])
```

### <a name="parameters---userdisable"></a>パラメーター - userDisable

値  
ユーザーのコントロールが無効になっているかどうかを示す値 (オプション)。

### <a name="return-value---userdisable"></a>戻り値 - userDisable

ユーザーのコントロールが無効になっている場合は 1、それ以外の場合は、0 です。

## <a name="method-userheight"></a>メソッド userHeight

コントロールのカスタム ユーザーの高さを取得または設定します。

```xpp
public int userHeight([int value])
```

### <a name="parameters---userheight"></a>パラメーター - userHeight

値  
コントロールのユーザーの高さ (オプション)。

### <a name="return-value---userheight"></a>戻り値 - userHeight

コントロールのカスタム ユーザーの高さ。

## <a name="method-userhide"></a>メソッド userHide

コントロールがユーザーから非表示になっているかどうかを示す値を取得または設定します。

```xpp
public int userHide([int value])
```

### <a name="parameters---userhide"></a>パラメーター - userHide

値  
コントロールがユーザーから非表示になっているどうかを示す値 (オプション)。

### <a name="return-value---userhide"></a>戻り値 - userHide

コントロールがユーザーから非表示になっている場合は 1、それ以外の場合は、0 です。

### <a name="remarks---userhide"></a>備考 - userHide

ユーザーは、コントロールが表示されたときにコントロールを右クリックするか、元のコントロールが非表示のときに他のコントロールを右クリックして、コントロールを非表示にするかどうかを指定します。 右クリックにより、コントロールを非表示または表示するために使用できるメニューを開きます。 このメソッドを使用すると、プログラムによって値を決定して設定できます。

## <a name="method-userorgcontainer"></a>メソッド userOrgContainer

コントロールの組織コンテナを取得または設定します。

```xpp
public int userOrgContainer([int value])
```

### <a name="parameters---userorgcontainer"></a>パラメーター - userOrgContainer

値  
コントロールに設定する組織コンテナー (オプション)。

### <a name="return-value---userorgcontainer"></a>戻り値 - userOrgContainer

コントロールの組織コンテナー。

## <a name="method-userorgsibling"></a>メソッド userOrgSibling

コントロールの組織兄弟を取得または設定します。

```xpp
public int userOrgSibling([int value])
```

### <a name="parameters---userorgsibling"></a>パラメーター - userOrgSibling

値  
コントロールに設定する組織の兄弟 (オプション)。

### <a name="return-value---userorgsibling"></a>戻り値 - userOrgSibling

コントロールの組織の兄弟。

## <a name="method-userprompttext"></a>メソッド userPromptText

コントロールのユーザーラベル テキストを取得または設定します。

```xpp
public str userPromptText([str value])
```

### <a name="parameters---userprompttext"></a>パラメーター - userPromptText

値  
コントロールに設定するユーザー ラベルのテキスト (オプション)。

### <a name="return-value---userprompttext"></a>戻り値 - userPromptText

コントロールのユーザーラベル テキスト。

## <a name="method-usersecuritylevel"></a>メソッド userSecurityLevel

コントロールのユーザー セキュリティ レベルを取得または設定します。

```xpp
public int userSecurityLevel([int value])
```

### <a name="parameters---usersecuritylevel"></a>パラメーター - userSecurityLevel

値  
コントロールに設定するユーザー セキュリティ レベル (オプション)。

### <a name="return-value---usersecuritylevel"></a>戻り値 - userSecurityLevel

コントロールのユーザー セキュリティ レベル。

## <a name="method-userskip"></a>メソッド userSkip

ユーザーが Tab キーを押してフォーム内のコントロールを移動するときにフォーム コントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public int userSkip([int value])
```

### <a name="parameters---userskip"></a>パラメーター - userSkip

値  
userSkip プロパティに割り当てる値 (オプション)。 コントロールをスキップするユーザーの設定が有効な場合、この値は 1、それ以外の場合は 0 です。

### <a name="return-value---userskip"></a>戻り値 - userSkip

コントロールをスキップするユーザーの設定が有効な場合は 1、それ以外の場合は 0 です。

## <a name="method-userwidth"></a>メソッド userWidth

ピクセル単位でコントロールの幅を設定するか返します。

```xpp
public int userWidth([int value])
```

### <a name="parameters---userwidth"></a>パラメーター - userWidth

値  
コントロールの幅として使用するピクセル数 (オプション)。

### <a name="return-value---userwidth"></a>戻り値 - userWidth

ユーザーがコントロールの幅として指定したピクセル数。ユーザーが文字の幅を指定しなかった場合は 0 (ゼロ)。

### <a name="remarks---userwidth"></a>備考 - userWidth

userWidth メソッドは、文字数の 6 倍に基づいてピクセル単位の幅を返します。 たとえば、ユーザーのコントロールの幅として 30 文字が指定されている場合、戻り値は 6 \* 30 = 180 となります。 コントロールの幅を文字で指定するには、コントロールを右クリックして、文字指定を行う設定フォームを開きます。

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-width"></a>メソッド width

```xpp
public int width(int value, [int mode])
```

### <a name="parameters---width"></a>パラメーター - width

値  

<!-- -->

モード  

### <a name="return-value---width"></a>戻り値 - width

## <a name="method-widthmode"></a>メソッド widthMode

```xpp
public int widthMode([int value])
```

### <a name="parameters---widthmode"></a>パラメーター - widthValue

値  

### <a name="return-value---widthmode"></a>戻り値 - widthMode

## <a name="method-widthvalue"></a>メソッド widthValue

```xpp
public int widthValue([int value])
```

### <a name="parameters---widthvalue"></a>パラメーター - widthValue

値  

### <a name="return-value---widthvalue"></a>戻り値 - widthValue

## <a name="method-registerxppilimplementation"></a>メソッド RegisterXppILImplementation

```xpp
public void RegisterXppILImplementation(str className)
```

### <a name="parameters---registerxppilimplementation"></a>パラメーター - RegisterXppILImplementation

className  

## <a name="method-new"></a>メソッド new

```xpp
public void new(FormContainer container)
```

### <a name="parameters---new"></a>パラメーター - new

コンテナー  

## <a name="method-resetusersetting"></a>メソッド resetUserSetting

コントロールのユーザー設定をリセットします。

```xpp
public void resetUserSetting()
```


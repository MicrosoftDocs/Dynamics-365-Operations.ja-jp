---
title: X++ 属性クラス
description: このトピックでは、X++ での属性の使用について説明します。
author: pvillads
ms.date: 08/27/2021
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8311a54973a23c5a032def3704e43e4a87b6ed7b
ms.sourcegitcommit: b294840b8e12aaa2775dd73b2ba9481ecc3d91d5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2021
ms.locfileid: "7463534"
---
# <a name="x-attribute-classes"></a>X++ 属性クラス

[!include [banner](../includes/banner.md)]

このトピックでは、X++ での属性の使用について説明します。

属性は、**SysAttribute** クラスを拡張 (継承) する非抽象クラスです。 属性は型およびメソッドに関するメタデータを表すか、または保存します。 属性はクラス、クラス フィールド、クラス メソッド、インターフェイスまたはテーブルに関連付けることができます。

属性はデリゲートとメソッドのハンドラーに適用され、ハンドラーをこれらの対象にマッピングします。

## <a name="creating-an-attribute-class"></a>属性クラスを作成しています

属性クラスは **SysAttribute** クラスを直接拡張したり、**SysAttribute** クラスのすべての子孫を拡張することもできます。 **SysAttribute** クラスは、**abstract** と宣言されているため、属性として使用できません。 次の例は、作成できる通常の属性クラスの宣言とデザインを示しています。

```xpp
public class PracticeAttribute extends SysAttribute
{
    // Fields in the classDeclaration.
    StartEnd startEndEnum;
    str reason;
    // Constructor.
    public void new(StartEnd _startEndEnum, str _reason)
    {
        startEndEnum  = _startEndEnum;
        reason = _reason;
    }
    // Other methods can go here.
}
```

### <a name="decorating-a-class-with-an-attribute"></a>属性を持つクラスの修飾

次の例では、前の例で与えられた **PracticeAttribute** で装飾されたクラスとメソッドを示しています。 属性のコンストラクターがパラメーターを取らない場合、パラメーターのかっこはオプションになります。 属性の修飾は、かっこのない `[AnotherAttribute]` であり可能性があります。

```xpp
[PracticeAttribute(StartEnd::End, "Use the RegularClass class at the end.")]
public class RegularClass
{
    [PracticeAttribute(Startend::Start, "Use the rehearse method at the start.")]
    public int rehearse()
    {
        // Logic goes here.
    }
    // More fields and methods belong here.
}
```

接尾語が `Attribute` の場合は、属性名の接尾語を省略できます。 たとえば、前の例では `[Practice]` を `[PracticeAttribute]` の代わりに使用できます。

### <a name="attribute-constructors"></a>属性コンストラクター

コンストラクターがパラメーターを持つようにすることで、クラスを修飾するためにメタデータが使用されるたびに、属性クラスが作成済みメタデータを格納するようにできます。 コンストラクターのパラメータは、**int**、**enum**、または **str** などの、プリミティブ型のリテラルにする必要があります。 コンパイラは、属性クラスのインスタンスを構築しません。 属性クラスの名前、およびコンストラクターのリテラル値を格納します。 したがって、属性コンストラクター内のロジックが例外をスローすると、その属性を持つクラスを修飾することによって例外が見つかりません。 例外は、後でプロセスがクラスを調べて、それが装飾されている属性を見るときに見つかります。 属性が作成されたときです。

### <a name="naming-conventions"></a>名前付け規則

すべての属性クラスには名前に接尾語 **属性** があります。 **属性** サフィックスは、推奨される名前付け規則ですが、システム要件ではありません。 **アプリケーション エクスプローラー** 内のクラスを選択して **プロパティ** ウインドウで **拡張** プロパティを確認することにより、クラスが **SysAttribute** から直接 **拡張** されるか決定することができます。

## <a name="sysobsoleteattribute"></a>SysObsoleteAttribute

システムは、**SysObsoleteAttribute** クラスを含むいくつかの属性を提供します。 **SysObsoleteAttribute** クラスの 1 つの使用方法は、ソース コード内の特定のメソッドが呼び出された場合、コンパイルが失敗することをコンパイラに通知することです。 コンパイラはコンパイルを拒否し、この属性の使用に格納されている特定のメッセージを表示します。 **SysObsoleteAttribute** クラスを使用すると、エラーではなく問題の警告メッセージをコンパイラに通知することもできます。

### <a name="sysobsoleteattribute-code-example"></a>SysObsoleteAttribute コードの例

```xpp
[SysObsoleteAttribute("The Automobile class might have faster performance.", false)]
class Bicycle
{
    // Members of the Bicycle class go here.
}
```

## <a name="metadata-reflection"></a>メタデータ リフレクション

クラスに関連付けられている属性メタデータを検索するには、リフレクションを使用します。 属性リフレクションに使用するクラスは次のとおりです。

- **DictClass** クラス - クラスおよびインタフェース用です。
- **DictMethod** クラス - クラス、インターフェイス、またはテーブルのメソッド用です。

前のリフレクション クラスで、属性メタデータを反映した方法は次のとおりです。

- **getAllAttributes** メソッド
- **getAttribute** メソッド
- **getAttributedClasses** メソッド
- **getAttributes** メソッド

> [!NOTE]
> X++ コードから特定の属性で飾られたすべてのメソッドまたはクラスをリストするメカニズムはありません。 ただし、X++ コンパイラは、相互参照データベースにこの情報を記録するため、そこから情報を得ることができます。

### <a name="metadata-reflection-code-example"></a>メタデータ リフレクションのコードの例

メソッドを修飾する属性のメタデータ値を検索するには、**DictMethod** クラスを使用します。 次のコード例では、**SysEntryPointAttribute** クラスを属性として使用しています。 メソッド名およびそのメソッドを含むクラスの名前にパラメーター値を受け入れます。 **parmChecked** メソッドは、**SysEntryPointAttribute** クラスに固有であり、基本クラス **SysAttribute** からから継承されません。 各属性クラスは、メタデータの独自のメソッド名を持つことが可能です。

```xpp
static public int MetadataOfSysEntryPointAttributeOnMethod
        (
        str _sNameOfClass,
        str _sNameOfMethod
        )
{
    // Return Values:
    // 0 == Has the attribute, its metadata value is false;
    // 1 == Has the attribute, its metadata value is true;
    // 2 == The method lacks the SysEntryPointAttribute.
    int nReturnValue = -1,
        nClassId;
    boolean boolParmChecked;
    DictMethod dm;
    Object attributeAsObject;
    SysEntryPointAttribute sepAttribute;
    Global::info("Starting AttributeReflection" 
        + " ::MetadataOfSysEntryPointAttributeOnMethod ....");
    Global::info(strFmt
        ("Parameters are: _sNameOfClass = %1 ,  _sNameOfMethod = %2 .", 
        _sNameOfClass, _sNameOfMethod)
        );
    nClassId = Global::className2Id(_sNameOfClass);
    dm = new DictMethod
        (UtilElementType::ClassInstanceMethod,
        nClassId,
        _sNameOfMethod
        );
    attributeAsObject = dm.getAttribute("SysEntryPointAttribute");
    if (attributeAsObject is SysEntryPointAttribute)
    {
        sepAttribute = attributeAsObject as SysEntryPointAttribute;
        boolParmChecked = sepAttribute.parmChecked();
        if (boolParmChecked)
            nReturnValue = 1;
        else
            nReturnValue = 0;
        Global::info(
            strFmt("Return value is %1.",
                nReturnValue)
            );
    }
    else
    {
        nReturnValue = 2;
        Global::error("Object is not a SysEntryPointAttribute??");
    }
    return nReturnValue;
}
/*** Output displayed in the Infolog.
Message (05:03:22 pm)
Starting AttributeReflection ::MetadataOfSysEntryPointAttributeOnMethod ....
Parameters are: _sNameOfClass = CustCustomerService ,  _sNameOfMethod = create .
Return value is 1.
***/
/**************
// Simple AOT > Jobs job to run the method.
static void AttributeReflection33Job(Args _args)
{
    AttributeReflection::MetadataOfSysEntryPointAttributeOnMethod
        ("CustCustomerService", "create");
}
**************/
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

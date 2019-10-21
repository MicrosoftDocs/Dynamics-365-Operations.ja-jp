---
title: X++ 属性クラス
description: このトピックでは、X++ での属性の使用について説明します。
author: pvillads
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150243
ms.assetid: 9c927660-3268-4a77-9a83-97759a487483
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5d01785db5eff5575143acaa3cf17c68ec6c6987
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183357"
---
# <a name="x-attribute-classes"></a><span data-ttu-id="3d78e-103">X++ 属性クラス</span><span class="sxs-lookup"><span data-stu-id="3d78e-103">X++ attribute classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d78e-104">このトピックでは、X++ での属性の使用について説明します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-104">This topic describes the use of attributes in X++.</span></span>

<span data-ttu-id="3d78e-105">属性は、**SysAttribute** クラスを拡張 (継承) する非抽象クラスです。</span><span class="sxs-lookup"><span data-stu-id="3d78e-105">An attribute is a non-abstract class that extends (inherits from) the **SysAttribute** class.</span></span> <span data-ttu-id="3d78e-106">属性は型およびメソッドに関するメタデータを表すか、または保存します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-106">Attributes represent or store metadata about types and methods.</span></span> <span data-ttu-id="3d78e-107">属性はクラス、インターフェイス、クラスのメソッド、インターフェイスまたはテーブルに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-107">An attribute can be attached to a class, an interface, or a method of a class, interface, or table.</span></span>

## <a name="creating-an-attribute-class"></a><span data-ttu-id="3d78e-108">属性クラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="3d78e-108">Creating an attribute class</span></span>
<span data-ttu-id="3d78e-109">属性クラスは **SysAttribute** クラスを直接拡張したり、**SysAttribute** クラスのすべての子孫を拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-109">An attribute class can extend the **SysAttribute** class directly, or it can extend any descendant of the **SysAttribute** class.</span></span> <span data-ttu-id="3d78e-110">**SysAttribute** クラスは、**abstract** と宣言されているため、属性として使用できません。</span><span class="sxs-lookup"><span data-stu-id="3d78e-110">The **SysAttribute** class cannot be used as an attribute because it is declared **abstract**.</span></span> <span data-ttu-id="3d78e-111">次の例は、作成できる通常の属性クラスの宣言とデザインを示しています。</span><span class="sxs-lookup"><span data-stu-id="3d78e-111">The following example shows the declaration and design of an ordinary attribute class that you could create.</span></span>

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

### <a name="decorating-a-class-with-an-attribute"></a><span data-ttu-id="3d78e-112">属性を持つクラスの修飾</span><span class="sxs-lookup"><span data-stu-id="3d78e-112">Decorating a class with an attribute</span></span>

<span data-ttu-id="3d78e-113">次の例では、前の例で与えられた **PracticeAttribute** で装飾されたクラスとメソッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="3d78e-113">The following example shows a class and a method that are decorated with the **PracticeAttribute** given in the previous example.</span></span> <span data-ttu-id="3d78e-114">属性のコンストラクターがパラメーターを取らない場合、パラメーターのかっこはオプションになります。</span><span class="sxs-lookup"><span data-stu-id="3d78e-114">If the constructor of the attribute takes no parameters, the parentheses for the parameters are optional.</span></span> <span data-ttu-id="3d78e-115">属性の修飾は、かっこのない `[AnotherAttribute]` であり可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3d78e-115">The attribute decoration could be `[AnotherAttribute]` without parentheses.</span></span>

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

### <a name="attribute-constructors"></a><span data-ttu-id="3d78e-116">属性コンストラクター</span><span class="sxs-lookup"><span data-stu-id="3d78e-116">Attribute constructors</span></span>

<span data-ttu-id="3d78e-117">コンストラクターがパラメーターを持つようにすることで、クラスを修飾するためにメタデータが使用されるたびに、属性クラスが作成済みメタデータを格納するようにできます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-117">You can enable your attribute class to store tailored metadata each time it is used to decorate a class, by having its constructor take parameters.</span></span> <span data-ttu-id="3d78e-118">コンストラクターのパラメータは、**int**、**enum**、または **str** などの、プリミティブ型のリテラルにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d78e-118">The parameters for the constructor must be literals of the primitive types, such as **int,** **enum,** or **str**.</span></span> <span data-ttu-id="3d78e-119">コンパイラは、属性クラスのインスタンスを構築しません。</span><span class="sxs-lookup"><span data-stu-id="3d78e-119">The compiler does not construct an instance of the attribute class.</span></span> <span data-ttu-id="3d78e-120">属性クラスの名前、およびコンストラクターのリテラル値を格納します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-120">It stores the name of the attribute class, plus the literal values for its constructor.</span></span> <span data-ttu-id="3d78e-121">したがって、属性コンストラクター内のロジックが例外をスローすると、その属性を持つクラスを修飾することによって例外が見つかりません。</span><span class="sxs-lookup"><span data-stu-id="3d78e-121">Therefore, if the logic in an attribute constructor would throw an exception, the exception would not be found by decorating a class with the attribute.</span></span> <span data-ttu-id="3d78e-122">例外は、後でプロセスがクラスを調べて、それが装飾されている属性を見るときに見つかります。</span><span class="sxs-lookup"><span data-stu-id="3d78e-122">The exception would be found later when a process looks at a class to see the attribute it is decorated with.</span></span> <span data-ttu-id="3d78e-123">属性が作成されたときです。</span><span class="sxs-lookup"><span data-stu-id="3d78e-123">That is when the attribute is constructed.</span></span>

### <a name="naming-conventions"></a><span data-ttu-id="3d78e-124">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="3d78e-124">Naming conventions</span></span>

<span data-ttu-id="3d78e-125">すべての属性クラスには名前に接尾語**属性**があります。</span><span class="sxs-lookup"><span data-stu-id="3d78e-125">All attribute classes have the suffix **Attribute** in their name.</span></span> <span data-ttu-id="3d78e-126">**属性** サフィックスは、推奨される名前付け規則ですが、システム要件ではありません。</span><span class="sxs-lookup"><span data-stu-id="3d78e-126">The **Attribute** suffix is the name convention that we recommend, but it is not a system requirement.</span></span> <span data-ttu-id="3d78e-127">**アプリケーション エクスプローラー** 内のクラスを選択して **プロパティ** ウインドウで **拡張** プロパティを確認することにより、クラスが **SysAttribute** から直接 **拡張** されるか決定することができます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-127">You can determine whether a class **extends** directly from **SysAttribute** by selecting the class in the **Application Explorer** and reviewing the **Extends** property in the **Properties** window.</span></span>

## <a name="sysobsoleteattribute"></a><span data-ttu-id="3d78e-128">SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="3d78e-128">SysObsoleteAttribute</span></span>
<span data-ttu-id="3d78e-129">システムは、**SysObsoleteAttribute** クラスを含むいくつかの属性を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-129">The system provides several attributes, including the **SysObsoleteAttribute** class.</span></span> <span data-ttu-id="3d78e-130">**SysObsoleteAttribute** クラスの 1 つの使用方法は、ソース コード内の特定のメソッドが呼び出された場合、コンパイルが失敗することをコンパイラに通知することです。</span><span class="sxs-lookup"><span data-stu-id="3d78e-130">One use of the **SysObsoleteAttribute** class is to notify the compiler that the compile should fail if a particular method is called in the source code.</span></span> <span data-ttu-id="3d78e-131">コンパイラはコンパイルを拒否し、この属性の使用に格納されている特定のメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-131">The compiler rejects the compile, and displays the specific message that is stored in this use of the attribute.</span></span> <span data-ttu-id="3d78e-132">**SysObsoleteAttribute** クラスを使用すると、エラーではなく問題の警告メッセージをコンパイラに通知することもできます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-132">The **SysObsoleteAttribute** class can also be used to notify the compiler to issue warning messages instead of errors.</span></span>

### <a name="sysobsoleteattribute-code-example"></a><span data-ttu-id="3d78e-133">SysObsoleteAttribute コードの例</span><span class="sxs-lookup"><span data-stu-id="3d78e-133">SysObsoleteAttribute code example</span></span>

    [SysObsoleteAttribute("The Automobile class might have faster performance.", false)]
    class Bicycle
    {
        // Members of the Bicycle class go here.
    }

## <a name="metadata-reflection"></a><span data-ttu-id="3d78e-134">メタデータ リフレクション</span><span class="sxs-lookup"><span data-stu-id="3d78e-134">Metadata reflection</span></span>
<span data-ttu-id="3d78e-135">クラスに関連付けられている属性メタデータを検索するには、リフレクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-135">You use reflection to find the attribute metadata that is attached to a class.</span></span> <span data-ttu-id="3d78e-136">属性リフレクションに使用するクラスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3d78e-136">The classes to use for attribute reflection are as follows:</span></span>

-   <span data-ttu-id="3d78e-137">**DictClass** クラス - クラスおよびインタフェース用です。</span><span class="sxs-lookup"><span data-stu-id="3d78e-137">**DictClass** class – For classes and interfaces.</span></span>
-   <span data-ttu-id="3d78e-138">**DictMethod** クラス - クラス、インターフェイス、またはテーブルのメソッド用です。</span><span class="sxs-lookup"><span data-stu-id="3d78e-138">**DictMethod** class – For methods on classes, interfaces, or tables.</span></span>

<span data-ttu-id="3d78e-139">前のリフレクション クラスで、属性メタデータを反映した方法は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3d78e-139">On the previous reflection classes, the methods for reflecting on attribute metadata are as follows:</span></span>

-   <span data-ttu-id="3d78e-140">**getAllAttributes** メソッド</span><span class="sxs-lookup"><span data-stu-id="3d78e-140">**getAllAttributes** method</span></span>
-   <span data-ttu-id="3d78e-141">**getAttribute** メソッド</span><span class="sxs-lookup"><span data-stu-id="3d78e-141">**getAttribute** method</span></span>
-   <span data-ttu-id="3d78e-142">**getAttributedClasses** メソッド</span><span class="sxs-lookup"><span data-stu-id="3d78e-142">**getAttributedClasses** method</span></span>
-   <span data-ttu-id="3d78e-143">**getAttributes** メソッド</span><span class="sxs-lookup"><span data-stu-id="3d78e-143">**getAttributes** method</span></span>

> [!NOTE]
> <span data-ttu-id="3d78e-144">X++ コードから特定の属性で飾られたすべてのメソッドまたはクラスをリストするメカニズムはありません。</span><span class="sxs-lookup"><span data-stu-id="3d78e-144">There is no mechanism for listing all methods or classes that are adorned with a particular attribute from X++ code.</span></span> <span data-ttu-id="3d78e-145">ただし、X++ コンパイラは、相互参照データベースにこの情報を記録するため、そこから情報を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-145">However, because the X++ compiler records this information in the cross reference database, the information can be mined from there.</span></span>

### <a name="metadata-reflection-code-example"></a><span data-ttu-id="3d78e-146">メタデータ リフレクションのコードの例</span><span class="sxs-lookup"><span data-stu-id="3d78e-146">Metadata reflection code example</span></span>

<span data-ttu-id="3d78e-147">メソッドを修飾する属性のメタデータ値を検索するには、**DictMethod** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d78e-147">You use the **DictMethod** class to find the metadata value of an attribute that is decoration on a method.</span></span> <span data-ttu-id="3d78e-148">次のコード例では、**SysEntryPointAttribute** クラスを属性として使用しています。</span><span class="sxs-lookup"><span data-stu-id="3d78e-148">The following code example uses the **SysEntryPointAttribute** class as the attribute.</span></span> <span data-ttu-id="3d78e-149">メソッド名およびそのメソッドを含むクラスの名前にパラメーター値を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="3d78e-149">It accepts your parameter values for the method name, and for the name of the class that contains the method.</span></span> <span data-ttu-id="3d78e-150">**parmChecked** メソッドは、**SysEntryPointAttribute** クラスに固有であり、基本クラス **SysAttribute** からから継承されません。</span><span class="sxs-lookup"><span data-stu-id="3d78e-150">The **parmChecked** method is particular to the **SysEntryPointAttribute** class, and it is not inherited from its base class **SysAttribute**.</span></span> <span data-ttu-id="3d78e-151">各属性クラスは、メタデータの独自のメソッド名を持つことが可能です。</span><span class="sxs-lookup"><span data-stu-id="3d78e-151">Each attribute class can have its own method name for its metadata.</span></span>

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




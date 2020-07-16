---
title: xArgs クラス
description: このトピックでは、xArgs クラスについて説明します。
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
ms.openlocfilehash: af53fba162249101e502e770fb306682770bfdff
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502995"
---
# <a name="class-xargs"></a><span data-ttu-id="ffba5-103">クラス xArgs</span><span class="sxs-lookup"><span data-stu-id="ffba5-103">Class xArgs</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class xArgs extends Object
```

<span data-ttu-id="ffba5-104">xArgs クラスは、アプリケーション オブジェクト間の名前、呼び出し元、パラメーターなどの引数を渡すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-104">The xArgs class is used to pass arguments such as a name, a caller, and parameters between application objects.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffba5-105">備考</span><span class="sxs-lookup"><span data-stu-id="ffba5-105">Remarks</span></span>

<span data-ttu-id="ffba5-106">フォーム、レポートおよびクエリはすべてこのクラスを、コンストラクターで最初の引数として使用します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-106">Forms, reports and queries all use this class as their first argument in the constructor.</span></span> <span data-ttu-id="ffba5-107">このクラスを使用する適切な方法は、xArgs オブジェクトを作成し、名前文字列を指定してから、フォーム コンストラクタまたは ClassFactory メソッドに xArgs オブジェクトを渡すことです。</span><span class="sxs-lookup"><span data-stu-id="ffba5-107">The preferred way to use this class is to construct an xArgs object, supply a name-string, and then pass the xArgs object to the forms constructor or a ClassFactory method.</span></span> <span data-ttu-id="ffba5-108">これらのクラスの中の 1 つに渡された xArgs オブジェクトを参照する場合は、そのクラスの args メソッドを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-108">If you want to refer to the xArgs object passed to one of these classes, it can be reached using args method of that class.</span></span> <span data-ttu-id="ffba5-109">追加情報を新しいクラスに渡すために使用できるメソッドは 4 つあります。</span><span class="sxs-lookup"><span data-stu-id="ffba5-109">There are four methods that can be used to pass extra information to the new class:</span></span>

-   <span data-ttu-id="ffba5-110">parm - 文字列を渡すため</span><span class="sxs-lookup"><span data-stu-id="ffba5-110">The parm - to pass strings</span></span>
-   <span data-ttu-id="ffba5-111">parmEnum および parmEnumType メソッド - 列挙値を渡すため</span><span class="sxs-lookup"><span data-stu-id="ffba5-111">The parmEnum and parmEnumType methods - to pass enumeration values</span></span>
-   <span data-ttu-id="ffba5-112">parmObject メソッド - 任意の型のオブジェクトを渡すため</span><span class="sxs-lookup"><span data-stu-id="ffba5-112">The parmObject method - to pass an object of any type</span></span>

<span data-ttu-id="ffba5-113">呼び出し元から送信された xArgs クラスのインスタンスは、カーネルによって自動的に、または呼び出し元によって明示的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-113">The instance of the xArgs class that is sent from the caller can be created automatically by the kernel or explicitly by the caller.</span></span> <span data-ttu-id="ffba5-114">呼び出し元がメニュー項目を使用してオブジェクトを呼び出すとき、カーネル コードによって、xArgs クラスのインスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-114">When the caller uses a menu item to call an object, an instance of the xArgs class is created by the kernel code.</span></span> <span data-ttu-id="ffba5-115">メニュー項目名は、使用するメニュー項目の名前に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-115">The menu item name will be set to the name of the menu item used.</span></span> <span data-ttu-id="ffba5-116">メニュー項目に、EnumParameter、Parameters、EnumParameter、または EnumTypeParameter プロパティが設定されている場合、カーネルは xArgs クラスのこのインスタンスに対して Parm、ParmEnum、または ParmEnumType プロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-116">If the menu item has values for the Parameters, EnumParameter, or EnumTypeParameter properties set, the kernel will set the values of the corresponding Parm, ParmEnum, or ParmEnumType properties for this instance of the xArgs class.</span></span>

## <a name="examples"></a><span data-ttu-id="ffba5-117">例</span><span class="sxs-lookup"><span data-stu-id="ffba5-117">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ffba5-118">メソッド</span><span class="sxs-lookup"><span data-stu-id="ffba5-118">Methods</span></span>

| <span data-ttu-id="ffba5-119">方法</span><span class="sxs-lookup"><span data-stu-id="ffba5-119">Method</span></span>                                                                                                       | <span data-ttu-id="ffba5-120">説明</span><span class="sxs-lookup"><span data-stu-id="ffba5-120">Description</span></span>                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffba5-121">public boolean allowUseOfPreloadedForm(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-121">public boolean allowUseOfPreloadedForm(\[boolean value\])</span></span>                                                    | <span data-ttu-id="ffba5-122">このインスタンスに対して起動されたフォームが、プリロードされたフォーム プールから取得されたものかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-122">Determines if the form launched for this instance may come from the pre-loaded form pool.</span></span>                                             |
| <span data-ttu-id="ffba5-123">public int arrIdx(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-123">public int arrIdx(\[int value\])</span></span>                                                                             |                                                                                                                                       |
| <span data-ttu-id="ffba5-124">public Object caller(\[Object value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-124">public Object caller(\[Object value\])</span></span>                                                                       | <span data-ttu-id="ffba5-125">xArgs クラスのこのインスタンスを作成したオブジェクトのインスタンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-125">Gets or sets the instance of the object that created this instance of the xArgs class.</span></span>                                                |
| <span data-ttu-id="ffba5-126">public IDispatcherProxy callerDispatcher()</span><span class="sxs-lookup"><span data-stu-id="ffba5-126">public IDispatcherProxy callerDispatcher()</span></span>                                                                   |                                                                                                                                       |
| <span data-ttu-id="ffba5-127">public FormControl callerFormControl(\[FormControl value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-127">public FormControl callerFormControl(\[FormControl value\])</span></span>                                                  |                                                                                                                                       |
| <span data-ttu-id="ffba5-128">public str callerName()</span><span class="sxs-lookup"><span data-stu-id="ffba5-128">public str callerName()</span></span>                                                                                      |                                                                                                                                       |
| <span data-ttu-id="ffba5-129">public UtilElementType callerType()</span><span class="sxs-lookup"><span data-stu-id="ffba5-129">public UtilElementType callerType()</span></span>                                                                          |                                                                                                                                       |
| <span data-ttu-id="ffba5-130">public Guid callerId()</span><span class="sxs-lookup"><span data-stu-id="ffba5-130">public Guid callerId()</span></span>                                                                                       |                                                                                                                                       |
| <span data-ttu-id="ffba5-131">public str clientId(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-131">public str clientId(\[str value\])</span></span>                                                                           |                                                                                                                                       |
| <span data-ttu-id="ffba5-132">public CopyCallerQuery copyCallerQuery(\[CopyCallerQuery value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-132">public CopyCallerQuery copyCallerQuery(\[CopyCallerQuery value\])</span></span>                                            |                                                                                                                                       |
| <span data-ttu-id="ffba5-133">public TableId dataset()</span><span class="sxs-lookup"><span data-stu-id="ffba5-133">public TableId dataset()</span></span>                                                                                     | <span data-ttu-id="ffba5-134">呼び出し元オブジェクトが動作しているテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-134">Gets the table ID of the table in which the caller object is working.</span></span>                                                                 |
| <span data-ttu-id="ffba5-135">public str designName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-135">public str designName(\[str value\])</span></span>                                                                         | <span data-ttu-id="ffba5-136">レポートまたはフォームでデザインを示す文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-136">Gets or sets a string that indicates a design on a report or form.</span></span>                                                                    |
| <span data-ttu-id="ffba5-137">public ExtendedTypeId extType(\[ExtendedTypeId edt\], \[int arrayIndex\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-137">public ExtendedTypeId extType(\[ExtendedTypeId edt\], \[int arrayIndex\])</span></span>                                    |                                                                                                                                       |
| <span data-ttu-id="ffba5-138">public FormViewOption formViewOption(\[FormViewOption value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-138">public FormViewOption formViewOption(\[FormViewOption value\])</span></span>                                               |                                                                                                                                       |
| <span data-ttu-id="ffba5-139">public InitialQueryParameter initialQuery(\[InitialQueryParameter initialQueryParameter\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-139">public InitialQueryParameter initialQuery(\[InitialQueryParameter initialQueryParameter\])</span></span>                   |                                                                                                                                       |
| <span data-ttu-id="ffba5-140">public FieldId lookupField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-140">public FieldId lookupField(\[FieldId value\])</span></span>                                                                | <span data-ttu-id="ffba5-141">指定されたレコードの検索に使用するテーブルのフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-141">Gets or sets the field ID in a table to use to look up a specified record.</span></span>                                                            |
| <span data-ttu-id="ffba5-142">public Common lookupRecord(\[Common value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-142">public Common lookupRecord(\[Common value\])</span></span>                                                                 | <span data-ttu-id="ffba5-143">指定されたテーブルのレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-143">Finds a record in the specified table.</span></span>                                                                                                |
| <span data-ttu-id="ffba5-144">public TableId lookupTable(\[TableId value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-144">public TableId lookupTable(\[TableId value\])</span></span>                                                                |                                                                                                                                       |
| <span data-ttu-id="ffba5-145">public str lookupValue(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-145">public str lookupValue(\[str value\])</span></span>                                                                        | <span data-ttu-id="ffba5-146">テーブルのフィールドで値を検索する LookupField メソッドで使用する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-146">Gets or sets a string to use with the LookupField method to find a value in a field of a table.</span></span>                                       |
| <span data-ttu-id="ffba5-147">public str managedContentItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-147">public str managedContentItemName(\[str value\])</span></span>                                                             |                                                                                                                                       |
| <span data-ttu-id="ffba5-148">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-148">public str menuItemName(\[str value\])</span></span>                                                                       | <span data-ttu-id="ffba5-149">アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-149">Gets or sets the name of the menu item to use to start the application object.</span></span>                                                        |
| <span data-ttu-id="ffba5-150">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-150">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                                                     | <span data-ttu-id="ffba5-151">アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-151">Gets or sets the type of the menu item to use to start the called application object.</span></span>                                                 |
| <span data-ttu-id="ffba5-152">public MultiSelectionContext multiSelectionContext()</span><span class="sxs-lookup"><span data-stu-id="ffba5-152">public MultiSelectionContext multiSelectionContext()</span></span>                                                         |                                                                                                                                       |
| <span data-ttu-id="ffba5-153">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-153">public str name(\[str value\])</span></span>                                                                               | <span data-ttu-id="ffba5-154">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-154">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>             |
| <span data-ttu-id="ffba5-155">public Object object(\[Object value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-155">public Object object(\[Object value\])</span></span>                                                                       | <span data-ttu-id="ffba5-156">新しいインスタンスを開く対象となるオブジェクトのアプリケーション名を取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-156">Gets and sets the application name of the object for which to open a new instance.</span></span>                                                    |
| <span data-ttu-id="ffba5-157">public OpenMode openMode(\[OpenMode value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-157">public OpenMode openMode(\[OpenMode value\])</span></span>                                                                 |                                                                                                                                       |
| <span data-ttu-id="ffba5-158">public Int64 parentWnd(\[Int64 value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-158">public Int64 parentWnd(\[Int64 value\])</span></span>                                                                      |                                                                                                                                       |
| <span data-ttu-id="ffba5-159">public str parm(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-159">public str parm(\[str value\])</span></span>                                                                               | <span data-ttu-id="ffba5-160">呼び出されるオブジェクトのさまざまな情報を指定する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-160">Gets or sets a string that specifies miscellaneous information for the called object.</span></span>                                                 |
| <span data-ttu-id="ffba5-161">public AnyType parmEnum(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-161">public AnyType parmEnum(\[int value\])</span></span>                                                                       | <span data-ttu-id="ffba5-162">parmEnumType メソッドで指定されている列挙型の列挙値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-162">Gets or sets the enumeration value of the enumeration type that is specified in the parmEnumType method.</span></span>                              |
| <span data-ttu-id="ffba5-163">public int parmEnumType(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-163">public int parmEnumType(\[int value\])</span></span>                                                                       | <span data-ttu-id="ffba5-164">任意の列挙タイプの ID 値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-164">Gets or sets the ID value of any enumeration type.</span></span>                                                                                    |
| <span data-ttu-id="ffba5-165">public Object parmObject(\[Object value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-165">public Object parmObject(\[Object value\])</span></span>                                                                   | <span data-ttu-id="ffba5-166">呼び出されるオブジェクトに渡す任意のオブジェクトのインスタンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-166">Gets or sets the instance of any object to pass to the called object.</span></span>                                                                 |
| <span data-ttu-id="ffba5-167">public Common record(\[Common value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-167">public Common record(\[Common value\])</span></span>                                                                       | <span data-ttu-id="ffba5-168">呼び出し元オブジェクトが動作しているテーブルのレコードを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-168">Gets or sets the record from the table on which the caller object is working.</span></span>                                                         |
| <span data-ttu-id="ffba5-169">public FieldId refField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-169">public FieldId refField(\[FieldId value\])</span></span>                                                                   |                                                                                                                                       |
| <span data-ttu-id="ffba5-170">public str getRequestContextQuery()</span><span class="sxs-lookup"><span data-stu-id="ffba5-170">public str getRequestContextQuery()</span></span>                                                                          |                                                                                                                                       |
| <span data-ttu-id="ffba5-171">public str requestContextQuery(str value)</span><span class="sxs-lookup"><span data-stu-id="ffba5-171">public str requestContextQuery(str value)</span></span>                                                                    |                                                                                                                                       |
| <span data-ttu-id="ffba5-172">public FieldId selectField(\[FieldId value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-172">public FieldId selectField(\[FieldId value\])</span></span>                                                                |                                                                                                                                       |
| <span data-ttu-id="ffba5-173">public str toString()</span><span class="sxs-lookup"><span data-stu-id="ffba5-173">public str toString()</span></span>                                                                                        | <span data-ttu-id="ffba5-174">xArgs のインスタンスの文字列形式を取得します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-174">Retrieves a string representation of an instance of the xArgs.</span></span>                                                                        |
| <span data-ttu-id="ffba5-175">public boolean applyRecordAsDynalink(\[boolean applyAsDynalink\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-175">public boolean applyRecordAsDynalink(\[boolean applyAsDynalink\])</span></span>                                            |                                                                                                                                       |
| <span data-ttu-id="ffba5-176">public void onCallerChanged(\[Object value\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-176">public void onCallerChanged(\[Object value\])</span></span>                                                                |                                                                                                                                       |
| <span data-ttu-id="ffba5-177">public void new(\[AnyType nameOrCaller\], \[Object object\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-177">public void new(\[AnyType nameOrCaller\], \[Object object\])</span></span>                                                 | <span data-ttu-id="ffba5-178">このクラスのインスタンスを構築します。このインスタンスは、FormRun クラスや ReportRun クラスなどの上位クラスに情報を渡すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-178">Constructs an instance of this class, which is used to pass information to high-level classes such as the FormRun or ReportRun class.</span></span> |
| <span data-ttu-id="ffba5-179">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ffba5-179">public void finalize()</span></span>                                                                                       | <span data-ttu-id="ffba5-180">メモリから xArgs クラスの現在のインスタンスを削除します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-180">Removes the current instance of the xArgs class from memory.</span></span>                                                                          |
| <span data-ttu-id="ffba5-181">public void setupArgs(str parm, int enumType, AnyType enumValue, \[str menuItemName\], \[int menuItemType\])</span><span class="sxs-lookup"><span data-stu-id="ffba5-181">public void setupArgs(str parm, int enumType, AnyType enumValue, \[str menuItemName\], \[int menuItemType\])</span></span> |                                                                                                                                       |

## <a name="method-allowuseofpreloadedform"></a><span data-ttu-id="ffba5-182">メソッド allowUseOfPreloadedForm</span><span class="sxs-lookup"><span data-stu-id="ffba5-182">Method allowUseOfPreloadedForm</span></span>

<span data-ttu-id="ffba5-183">このインスタンスに対して起動されたフォームが、プリロードされたフォーム プールから取得されたものかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-183">Determines if the form launched for this instance may come from the pre-loaded form pool.</span></span>

```xpp
public boolean allowUseOfPreloadedForm([boolean value])
```

### <a name="parameters---allowuseofpreloadedform"></a><span data-ttu-id="ffba5-184">パラメーター - allowUseOfPreloadedForm</span><span class="sxs-lookup"><span data-stu-id="ffba5-184">Parameters - allowUseOfPreloadedForm</span></span>

<span data-ttu-id="ffba5-185">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-185">value</span></span>  
<span data-ttu-id="ffba5-186">読み込まれたフォームがプリロードされたフォーム プールから取得できるかどうかを決定するブール値。</span><span class="sxs-lookup"><span data-stu-id="ffba5-186">A Boolean value that determines whether the loaded form can come from the pre-loaded form pool.</span></span>

### <a name="return-value---allowuseofpreloadedform"></a><span data-ttu-id="ffba5-187">戻り値 - allowUseOfPreloadedForm</span><span class="sxs-lookup"><span data-stu-id="ffba5-187">Return Value - allowUseOfPreloadedForm</span></span>

<span data-ttu-id="ffba5-188">このインスタンスのために起動されるフォームが事前に読み込まれたフォーム プールから取得される可能性がある場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ffba5-188">true if the form launched for this instance may come from the pre-loaded form pool; otherwise, false.</span></span>

### <a name="remarks---allowuseofpreloadedform"></a><span data-ttu-id="ffba5-189">備考 - allowUseOfPreloadedForm</span><span class="sxs-lookup"><span data-stu-id="ffba5-189">Remarks - allowUseOfPreloadedForm</span></span>

<span data-ttu-id="ffba5-190">事前に読み込まれているフォームの使用は、既定で許可されています。</span><span class="sxs-lookup"><span data-stu-id="ffba5-190">Use of a pre-loaded form is permitted by default.</span></span> <span data-ttu-id="ffba5-191">事前に読み込まれたフォームを使用して悪影響があった場合にのみ、これを false に設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-191">Set this to false only if there are undesired side-effects from the use of a pre-loaded form.</span></span>

## <a name="method-arridx"></a><span data-ttu-id="ffba5-192">メソッド arrIdx</span><span class="sxs-lookup"><span data-stu-id="ffba5-192">Method arrIdx</span></span>

```xpp
public int arrIdx([int value])
```

### <a name="parameters---arridx"></a><span data-ttu-id="ffba5-193">パラメーター - arrIdx</span><span class="sxs-lookup"><span data-stu-id="ffba5-193">Parameters - arrIdx</span></span>

<span data-ttu-id="ffba5-194">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-194">value</span></span>  

### <a name="return-value---arridx"></a><span data-ttu-id="ffba5-195">戻り値 - arrIdx</span><span class="sxs-lookup"><span data-stu-id="ffba5-195">Return Value - arrIdx</span></span>

## <a name="method-caller"></a><span data-ttu-id="ffba5-196">メソッド caller</span><span class="sxs-lookup"><span data-stu-id="ffba5-196">Method caller</span></span>

<span data-ttu-id="ffba5-197">xArgs クラスのこのインスタンスを作成したオブジェクトのインスタンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-197">Gets or sets the instance of the object that created this instance of the xArgs class.</span></span>

```xpp
public Object caller([Object value])
```

### <a name="parameters---caller"></a><span data-ttu-id="ffba5-198">パラメーター - caller</span><span class="sxs-lookup"><span data-stu-id="ffba5-198">Parameters - caller</span></span>

<span data-ttu-id="ffba5-199">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-199">value</span></span>  
<span data-ttu-id="ffba5-200">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-200">The value to set; optional.</span></span>

### <a name="return-value---caller"></a><span data-ttu-id="ffba5-201">戻り値 - caller</span><span class="sxs-lookup"><span data-stu-id="ffba5-201">Return Value - caller</span></span>

<span data-ttu-id="ffba5-202">呼び出し元オブジェクトの現在のインスタンス。</span><span class="sxs-lookup"><span data-stu-id="ffba5-202">The current instance of the caller object.</span></span>

## <a name="method-callerdispatcher"></a><span data-ttu-id="ffba5-203">メソッド callerDispatcher</span><span class="sxs-lookup"><span data-stu-id="ffba5-203">Method callerDispatcher</span></span>

```xpp
public IDispatcherProxy callerDispatcher()
```

### <a name="return-value---callerdispatcher"></a><span data-ttu-id="ffba5-204">戻り値 - callerDispatcher</span><span class="sxs-lookup"><span data-stu-id="ffba5-204">Return Value - callerDispatcher</span></span>

## <a name="method-callerformcontrol"></a><span data-ttu-id="ffba5-205">メソッド callerFormControl</span><span class="sxs-lookup"><span data-stu-id="ffba5-205">Method callerFormControl</span></span>

```xpp
public FormControl callerFormControl([FormControl value])
```

### <a name="parameters---callerformcontrol"></a><span data-ttu-id="ffba5-206">パラメーター - callerFormControl</span><span class="sxs-lookup"><span data-stu-id="ffba5-206">Parameters - callerFormControl</span></span>

<span data-ttu-id="ffba5-207">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-207">value</span></span>  

### <a name="return-value---callerformcontrol"></a><span data-ttu-id="ffba5-208">戻り値 - callerFormControl</span><span class="sxs-lookup"><span data-stu-id="ffba5-208">Return Value - callerFormControl</span></span>

## <a name="method-callername"></a><span data-ttu-id="ffba5-209">メソッド callerName</span><span class="sxs-lookup"><span data-stu-id="ffba5-209">Method callerName</span></span>

```xpp
public str callerName()
```

### <a name="return-value---callername"></a><span data-ttu-id="ffba5-210">戻り値 - callerName</span><span class="sxs-lookup"><span data-stu-id="ffba5-210">Return Value - callerName</span></span>

## <a name="method-callertype"></a><span data-ttu-id="ffba5-211">メソッド callerType</span><span class="sxs-lookup"><span data-stu-id="ffba5-211">Method callerType</span></span>

```xpp
public UtilElementType callerType()
```

### <a name="return-value---callertype"></a><span data-ttu-id="ffba5-212">戻り値 - callerType</span><span class="sxs-lookup"><span data-stu-id="ffba5-212">Return Value - callerType</span></span>

## <a name="method-callerid"></a><span data-ttu-id="ffba5-213">メソッド callerId</span><span class="sxs-lookup"><span data-stu-id="ffba5-213">Method callerId</span></span>

```xpp
public Guid callerId()
```

### <a name="return-value---callerid"></a><span data-ttu-id="ffba5-214">戻り値 - callerId</span><span class="sxs-lookup"><span data-stu-id="ffba5-214">Return Value - callerId</span></span>

## <a name="method-clientid"></a><span data-ttu-id="ffba5-215">メソッド clientId</span><span class="sxs-lookup"><span data-stu-id="ffba5-215">Method clientId</span></span>

```xpp
public str clientId([str value])
```

### <a name="parameters---clientid"></a><span data-ttu-id="ffba5-216">パラメーター - clientId</span><span class="sxs-lookup"><span data-stu-id="ffba5-216">Parameters - clientId</span></span>

<span data-ttu-id="ffba5-217">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-217">value</span></span>  

### <a name="return-value---clientid"></a><span data-ttu-id="ffba5-218">戻り値 - clientId</span><span class="sxs-lookup"><span data-stu-id="ffba5-218">Return Value - clientId</span></span>

## <a name="method-copycallerquery"></a><span data-ttu-id="ffba5-219">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-219">Method copyCallerQuery</span></span>

```xpp
public CopyCallerQuery copyCallerQuery([CopyCallerQuery value])
```

### <a name="parameters---copycallerquery"></a><span data-ttu-id="ffba5-220">パラメーター - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-220">Parameters - copyCallerQuery</span></span>

<span data-ttu-id="ffba5-221">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-221">value</span></span>  

### <a name="return-value---copycallerquery"></a><span data-ttu-id="ffba5-222">戻り値 - copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-222">Return Value - copyCallerQuery</span></span>

## <a name="method-dataset"></a><span data-ttu-id="ffba5-223">メソッド dataset</span><span class="sxs-lookup"><span data-stu-id="ffba5-223">Method dataset</span></span>

<span data-ttu-id="ffba5-224">呼び出し元オブジェクトが動作しているテーブルのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-224">Gets the table ID of the table in which the caller object is working.</span></span>

```xpp
public TableId dataset()
```

### <a name="return-value---dataset"></a><span data-ttu-id="ffba5-225">戻り値 - dataset</span><span class="sxs-lookup"><span data-stu-id="ffba5-225">Return Value - dataset</span></span>

<span data-ttu-id="ffba5-226">呼び出し元オブジェクトが動作しているテーブルのテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="ffba5-226">The table ID of the table in which the caller object is working.</span></span>

### <a name="remarks---dataset"></a><span data-ttu-id="ffba5-227">備考 - dataset</span><span class="sxs-lookup"><span data-stu-id="ffba5-227">Remarks - dataset</span></span>

<span data-ttu-id="ffba5-228">戻り値は、レコード メソッドで呼び出し元から転送されているレコードの種類を識別するために、頻繁に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-228">The returned value is often used to identify which type of record is being transferred from the caller in the record method.</span></span>

## <a name="method-designname"></a><span data-ttu-id="ffba5-229">メソッド designName</span><span class="sxs-lookup"><span data-stu-id="ffba5-229">Method designName</span></span>

<span data-ttu-id="ffba5-230">レポートまたはフォームでデザインを示す文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-230">Gets or sets a string that indicates a design on a report or form.</span></span>

```xpp
public str designName([str value])
```

### <a name="parameters---designname"></a><span data-ttu-id="ffba5-231">パラメーター - designName</span><span class="sxs-lookup"><span data-stu-id="ffba5-231">Parameters - designName</span></span>

<span data-ttu-id="ffba5-232">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-232">value</span></span>  
<span data-ttu-id="ffba5-233">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-233">The value to set; optional.</span></span>

### <a name="return-value---designname"></a><span data-ttu-id="ffba5-234">戻り値 - designName</span><span class="sxs-lookup"><span data-stu-id="ffba5-234">Return Value - designName</span></span>

## <a name="method-exttype"></a><span data-ttu-id="ffba5-235">メソッド extType</span><span class="sxs-lookup"><span data-stu-id="ffba5-235">Method extType</span></span>

```xpp
public ExtendedTypeId extType([ExtendedTypeId edt], [int arrayIndex])
```

### <a name="parameters---exttype"></a><span data-ttu-id="ffba5-236">パラメーター - extType</span><span class="sxs-lookup"><span data-stu-id="ffba5-236">Parameters - extType</span></span>

<span data-ttu-id="ffba5-237">edt</span><span class="sxs-lookup"><span data-stu-id="ffba5-237">edt</span></span>  

<!-- -->

<span data-ttu-id="ffba5-238">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="ffba5-238">arrayIndex</span></span>  

### <a name="return-value---exttype"></a><span data-ttu-id="ffba5-239">戻り値 - extType</span><span class="sxs-lookup"><span data-stu-id="ffba5-239">Return Value - extType</span></span>

## <a name="method-formviewoption"></a><span data-ttu-id="ffba5-240">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="ffba5-240">Method formViewOption</span></span>

```xpp
public FormViewOption formViewOption([FormViewOption value])
```

### <a name="parameters---formviewoption"></a><span data-ttu-id="ffba5-241">パラメーター - formViewOption</span><span class="sxs-lookup"><span data-stu-id="ffba5-241">Parameters - formViewOption</span></span>

<span data-ttu-id="ffba5-242">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-242">value</span></span>  

### <a name="return-value---formviewoption"></a><span data-ttu-id="ffba5-243">戻り値 - formViewOption</span><span class="sxs-lookup"><span data-stu-id="ffba5-243">Return Value - formViewOption</span></span>

## <a name="method-initialquery"></a><span data-ttu-id="ffba5-244">メソッド initialQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-244">Method initialQuery</span></span>

```xpp
public InitialQueryParameter initialQuery([InitialQueryParameter initialQueryParameter])
```

### <a name="parameters---initialquery"></a><span data-ttu-id="ffba5-245">パラメーター - initialQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-245">Parameters - initialQuery</span></span>

<span data-ttu-id="ffba5-246">initialQueryParameter</span><span class="sxs-lookup"><span data-stu-id="ffba5-246">initialQueryParameter</span></span>  

### <a name="return-value---initialquery"></a><span data-ttu-id="ffba5-247">戻り値 - initialQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-247">Return Value - initialQuery</span></span>

## <a name="method-lookupfield"></a><span data-ttu-id="ffba5-248">メソッド lookupField</span><span class="sxs-lookup"><span data-stu-id="ffba5-248">Method lookupField</span></span>

<span data-ttu-id="ffba5-249">指定されたレコードの検索に使用するテーブルのフィールド ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-249">Gets or sets the field ID in a table to use to look up a specified record.</span></span>

```xpp
public FieldId lookupField([FieldId value])
```

### <a name="parameters---lookupfield"></a><span data-ttu-id="ffba5-250">パラメーター - lookupField</span><span class="sxs-lookup"><span data-stu-id="ffba5-250">Parameters - lookupField</span></span>

<span data-ttu-id="ffba5-251">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-251">value</span></span>  
<span data-ttu-id="ffba5-252">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-252">The value to set; optional.</span></span>

### <a name="return-value---lookupfield"></a><span data-ttu-id="ffba5-253">戻り値 - lookupField</span><span class="sxs-lookup"><span data-stu-id="ffba5-253">Return Value - lookupField</span></span>

<span data-ttu-id="ffba5-254">指定されたレコードを検索するために使用するテーブル内のフィールドのフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="ffba5-254">The field ID of a field in a table to use to look up a specified record.</span></span>

### <a name="remarks---lookupfield"></a><span data-ttu-id="ffba5-255">備考 - lookupField</span><span class="sxs-lookup"><span data-stu-id="ffba5-255">Remarks - lookupField</span></span>

<span data-ttu-id="ffba5-256">戻り値は、呼び出されたオブジェクトが LookupRecord メソッド内の指定されたレコードまたは LookupValue メソッドで指定された文字列を検索するために、使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-256">The returned value can be used by the called object to look up the specified record in the LookupRecord method or the string specified in the LookupValue method.</span></span> <span data-ttu-id="ffba5-257">たとえば、以下を使用して検索するフィールドを設定することができます: xArgs.lookupField(fieldnum(TableName, FieldName));</span><span class="sxs-lookup"><span data-stu-id="ffba5-257">For example, the field to look up could be set with the following: xArgs.lookupField(fieldnum(TableName, FieldName));</span></span>

## <a name="method-lookuprecord"></a><span data-ttu-id="ffba5-258">メソッド lookupRecord</span><span class="sxs-lookup"><span data-stu-id="ffba5-258">Method lookupRecord</span></span>

<span data-ttu-id="ffba5-259">指定されたテーブルのレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-259">Finds a record in the specified table.</span></span>

```xpp
public Common lookupRecord([Common value])
```

### <a name="parameters---lookuprecord"></a><span data-ttu-id="ffba5-260">パラメーター - lookupRecord</span><span class="sxs-lookup"><span data-stu-id="ffba5-260">Parameters - lookupRecord</span></span>

<span data-ttu-id="ffba5-261">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-261">value</span></span>  
<span data-ttu-id="ffba5-262">レコードを検索するテーブル。</span><span class="sxs-lookup"><span data-stu-id="ffba5-262">The table in which to find a record.</span></span>

### <a name="return-value---lookuprecord"></a><span data-ttu-id="ffba5-263">戻り値 - lookupRecord</span><span class="sxs-lookup"><span data-stu-id="ffba5-263">Return Value - lookupRecord</span></span>

<span data-ttu-id="ffba5-264">指定されたテーブルのレコード。</span><span class="sxs-lookup"><span data-stu-id="ffba5-264">A record in the specified table.</span></span>

### <a name="remarks---lookuprecord"></a><span data-ttu-id="ffba5-265">備考 - lookupRecord</span><span class="sxs-lookup"><span data-stu-id="ffba5-265">Remarks - lookupRecord</span></span>

<span data-ttu-id="ffba5-266">このメソッドは、呼び出されたオブジェクトが lookupField メソッドから返されるフィールド ID と組み合わせて使用され、このメソッドによって返されるレコード内のフィールドの値を検索します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-266">This method can be used by the called object in combination with the field ID that is returned from the lookupField method to find the value of the field in the record that is returned by this method.</span></span>

## <a name="method-lookuptable"></a><span data-ttu-id="ffba5-267">メソッド lookupTable</span><span class="sxs-lookup"><span data-stu-id="ffba5-267">Method lookupTable</span></span>

```xpp
public TableId lookupTable([TableId value])
```

### <a name="parameters---lookuptable"></a><span data-ttu-id="ffba5-268">パラメーター - lookupTable</span><span class="sxs-lookup"><span data-stu-id="ffba5-268">Parameters - lookupTable</span></span>

<span data-ttu-id="ffba5-269">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-269">value</span></span>  

### <a name="return-value---lookuptable"></a><span data-ttu-id="ffba5-270">戻り値 - lookupTable</span><span class="sxs-lookup"><span data-stu-id="ffba5-270">Return Value - lookupTable</span></span>

## <a name="method-lookupvalue"></a><span data-ttu-id="ffba5-271">メソッド lookupValue</span><span class="sxs-lookup"><span data-stu-id="ffba5-271">Method lookupValue</span></span>

<span data-ttu-id="ffba5-272">テーブルのフィールドで値を検索する LookupField メソッドで使用する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-272">Gets or sets a string to use with the LookupField method to find a value in a field of a table.</span></span>

```xpp
public str lookupValue([str value])
```

### <a name="parameters---lookupvalue"></a><span data-ttu-id="ffba5-273">パラメーター - lookupValue</span><span class="sxs-lookup"><span data-stu-id="ffba5-273">Parameters - lookupValue</span></span>

<span data-ttu-id="ffba5-274">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-274">value</span></span>  
<span data-ttu-id="ffba5-275">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-275">The value to set; optional.</span></span>

### <a name="return-value---lookupvalue"></a><span data-ttu-id="ffba5-276">戻り値 - lookupValue</span><span class="sxs-lookup"><span data-stu-id="ffba5-276">Return Value - lookupValue</span></span>

<span data-ttu-id="ffba5-277">LookupField メソッドで値を検索するために使用する文字列。</span><span class="sxs-lookup"><span data-stu-id="ffba5-277">A string to use with the LookupField method to find a value.</span></span>

## <a name="method-managedcontentitemname"></a><span data-ttu-id="ffba5-278">メソッド managedContentItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-278">Method managedContentItemName</span></span>

```xpp
public str managedContentItemName([str value])
```

### <a name="parameters---managedcontentitemname"></a><span data-ttu-id="ffba5-279">パラメーター - managedContentItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-279">Parameters - managedContentItemName</span></span>

<span data-ttu-id="ffba5-280">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-280">value</span></span>  

### <a name="return-value---managedcontentitemname"></a><span data-ttu-id="ffba5-281">戻り値 - managedContentItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-281">Return Value - managedContentItemName</span></span>

## <a name="method-menuitemname"></a><span data-ttu-id="ffba5-282">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-282">Method menuItemName</span></span>

<span data-ttu-id="ffba5-283">アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-283">Gets or sets the name of the menu item to use to start the application object.</span></span>

```xpp
public str menuItemName([str value])
```

### <a name="parameters---menuitemname"></a><span data-ttu-id="ffba5-284">パラメーター - menuItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-284">Parameters - menuItemName</span></span>

<span data-ttu-id="ffba5-285">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-285">value</span></span>  
<span data-ttu-id="ffba5-286">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-286">The value to set; optional.</span></span>

### <a name="return-value---menuitemname"></a><span data-ttu-id="ffba5-287">戻り値 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-287">Return Value - menuItemName</span></span>

<span data-ttu-id="ffba5-288">アプリケーション オブジェクトを開始するのに使用するメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="ffba5-288">The name of the menu item to use to start the application object.</span></span>

### <a name="remarks---menuitemname"></a><span data-ttu-id="ffba5-289">備考 - menuItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-289">Remarks - menuItemName</span></span>

<span data-ttu-id="ffba5-290">たとえば、メニュー項目を設定するには、以下を使用できます: xArgs.menuItemName(menuitemdisplaystr(CostingVersionPeriodic));</span><span class="sxs-lookup"><span data-stu-id="ffba5-290">For example, to set the menu item you could use the following: xArgs.menuItemName(menuitemdisplaystr(CostingVersionPeriodic));</span></span>

## <a name="method-menuitemtype"></a><span data-ttu-id="ffba5-291">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="ffba5-291">Method menuItemType</span></span>

<span data-ttu-id="ffba5-292">アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-292">Gets or sets the type of the menu item to use to start the called application object.</span></span>

```xpp
public MenuItemType menuItemType([MenuItemType value])
```

### <a name="parameters---menuitemtype"></a><span data-ttu-id="ffba5-293">パラメーター - menuItemType</span><span class="sxs-lookup"><span data-stu-id="ffba5-293">Parameters - menuItemType</span></span>

<span data-ttu-id="ffba5-294">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-294">value</span></span>  
<span data-ttu-id="ffba5-295">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-295">The value to set; optional.</span></span>

### <a name="return-value---menuitemtype"></a><span data-ttu-id="ffba5-296">戻り値 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="ffba5-296">Return Value - menuItemType</span></span>

<span data-ttu-id="ffba5-297">アプリケーション オブジェクトの呼び出しを開始するのに使用するメニュー項目のタイプ。</span><span class="sxs-lookup"><span data-stu-id="ffba5-297">The type of the menu item to use to start the called application object.</span></span>

### <a name="remarks---menuitemtype"></a><span data-ttu-id="ffba5-298">備考 - menuItemType</span><span class="sxs-lookup"><span data-stu-id="ffba5-298">Remarks - menuItemType</span></span>

<span data-ttu-id="ffba5-299">メニュー項目タイプは、表示、出力、またはアクションの列挙型のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="ffba5-299">The menu item type will be one of the Display, Output, or Action enumeration values.</span></span>

## <a name="method-multiselectioncontext"></a><span data-ttu-id="ffba5-300">メソッド multiSelectionContext</span><span class="sxs-lookup"><span data-stu-id="ffba5-300">Method multiSelectionContext</span></span>

```xpp
public MultiSelectionContext multiSelectionContext()
```

### <a name="return-value---multiselectioncontext"></a><span data-ttu-id="ffba5-301">戻り値 - multiSelectionContext</span><span class="sxs-lookup"><span data-stu-id="ffba5-301">Return Value - multiSelectionContext</span></span>

## <a name="method-name"></a><span data-ttu-id="ffba5-302">メソッド名</span><span class="sxs-lookup"><span data-stu-id="ffba5-302">Method name</span></span>

<span data-ttu-id="ffba5-303">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-303">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="ffba5-304">パラメーター - name</span><span class="sxs-lookup"><span data-stu-id="ffba5-304">Parameters - name</span></span>

<span data-ttu-id="ffba5-305">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-305">value</span></span>  
<span data-ttu-id="ffba5-306">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-306">The value to set; optional.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="ffba5-307">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="ffba5-307">Return Value - name</span></span>

<span data-ttu-id="ffba5-308">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="ffba5-308">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="ffba5-309">備考 - name</span><span class="sxs-lookup"><span data-stu-id="ffba5-309">Remarks - name</span></span>

<span data-ttu-id="ffba5-310">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffba5-310">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="ffba5-311">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-311">Begins with a letter.</span></span>
-   <span data-ttu-id="ffba5-312">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="ffba5-312">Does not exceed 250 characters.</span></span>
-   <span data-ttu-id="ffba5-313">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-313">May include numbers and underscore characters.</span></span>
-   <span data-ttu-id="ffba5-314">句読点やスペースを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-314">May include punctuation or spaces.</span></span>
-   <span data-ttu-id="ffba5-315">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="ffba5-315">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

<span data-ttu-id="ffba5-316">たとえば、アプリケーション オブジェクトからフォームを呼び出すには、args.name(formstr(FormName)); を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-316">For example, to call a form from an application object you can use: args.name(formstr(FormName));</span></span>

## <a name="method-object"></a><span data-ttu-id="ffba5-317">メソッド object</span><span class="sxs-lookup"><span data-stu-id="ffba5-317">Method object</span></span>

<span data-ttu-id="ffba5-318">新しいインスタンスを開く対象となるオブジェクトのアプリケーション名を取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-318">Gets and sets the application name of the object for which to open a new instance.</span></span>

```xpp
public Object object([Object value])
```

### <a name="parameters---object"></a><span data-ttu-id="ffba5-319">パラメーター - object</span><span class="sxs-lookup"><span data-stu-id="ffba5-319">Parameters - object</span></span>

<span data-ttu-id="ffba5-320">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-320">value</span></span>  
<span data-ttu-id="ffba5-321">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-321">The value to set; optional.</span></span>

### <a name="return-value---object"></a><span data-ttu-id="ffba5-322">戻り値 - object</span><span class="sxs-lookup"><span data-stu-id="ffba5-322">Return Value - object</span></span>

<span data-ttu-id="ffba5-323">新しいインスタンスを開く対象となるオブジェクトのアプリケーション名。</span><span class="sxs-lookup"><span data-stu-id="ffba5-323">The application name of the object for which to open a new instance.</span></span>

### <a name="remarks---object"></a><span data-ttu-id="ffba5-324">備考 - object</span><span class="sxs-lookup"><span data-stu-id="ffba5-324">Remarks - object</span></span>

<span data-ttu-id="ffba5-325">value パラメーターは、次のオブジェクトのいずれかのタイプである場合があります。</span><span class="sxs-lookup"><span data-stu-id="ffba5-325">The value parameter may be one of the following types of objects:</span></span>

-   <span data-ttu-id="ffba5-326">フォーム</span><span class="sxs-lookup"><span data-stu-id="ffba5-326">Form</span></span>
-   <span data-ttu-id="ffba5-327">報告</span><span class="sxs-lookup"><span data-stu-id="ffba5-327">Report</span></span>
-   <span data-ttu-id="ffba5-328">ジョブ</span><span class="sxs-lookup"><span data-stu-id="ffba5-328">Job</span></span>
-   <span data-ttu-id="ffba5-329">クラス</span><span class="sxs-lookup"><span data-stu-id="ffba5-329">Class</span></span>
-   <span data-ttu-id="ffba5-330">クエリ。</span><span class="sxs-lookup"><span data-stu-id="ffba5-330">Query.</span></span>

## <a name="method-openmode"></a><span data-ttu-id="ffba5-331">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="ffba5-331">Method openMode</span></span>

```xpp
public OpenMode openMode([OpenMode value])
```

### <a name="parameters---openmode"></a><span data-ttu-id="ffba5-332">パラメーター - openMode</span><span class="sxs-lookup"><span data-stu-id="ffba5-332">Parameters - openMode</span></span>

<span data-ttu-id="ffba5-333">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-333">value</span></span>  

### <a name="return-value---openmode"></a><span data-ttu-id="ffba5-334">戻り値 - openMode</span><span class="sxs-lookup"><span data-stu-id="ffba5-334">Return Value - openMode</span></span>

## <a name="method-parentwnd"></a><span data-ttu-id="ffba5-335">メソッド parentWnd</span><span class="sxs-lookup"><span data-stu-id="ffba5-335">Method parentWnd</span></span>

```xpp
public Int64 parentWnd([Int64 value])
```

### <a name="parameters---parentwnd"></a><span data-ttu-id="ffba5-336">パラメーター - parentWnd</span><span class="sxs-lookup"><span data-stu-id="ffba5-336">Parameters - parentWnd</span></span>

<span data-ttu-id="ffba5-337">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-337">value</span></span>  

### <a name="return-value---parentwnd"></a><span data-ttu-id="ffba5-338">戻り値 - parentWnd</span><span class="sxs-lookup"><span data-stu-id="ffba5-338">Return Value - parentWnd</span></span>

## <a name="method-parm"></a><span data-ttu-id="ffba5-339">メソッド parm</span><span class="sxs-lookup"><span data-stu-id="ffba5-339">Method parm</span></span>

<span data-ttu-id="ffba5-340">呼び出されるオブジェクトのさまざまな情報を指定する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-340">Gets or sets a string that specifies miscellaneous information for the called object.</span></span>

```xpp
public str parm([str value])
```

### <a name="parameters---parm"></a><span data-ttu-id="ffba5-341">パラメーター - parm</span><span class="sxs-lookup"><span data-stu-id="ffba5-341">Parameters - parm</span></span>

<span data-ttu-id="ffba5-342">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-342">value</span></span>  
<span data-ttu-id="ffba5-343">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-343">The value to set; optional.</span></span>

### <a name="return-value---parm"></a><span data-ttu-id="ffba5-344">戻り値 - parm</span><span class="sxs-lookup"><span data-stu-id="ffba5-344">Return Value - parm</span></span>

<span data-ttu-id="ffba5-345">呼び出されるオブジェクトのさまざまな情報を指定する文字列の値。</span><span class="sxs-lookup"><span data-stu-id="ffba5-345">The value of the string that specifies miscellaneous information for the called object.</span></span>

## <a name="method-parmenum"></a><span data-ttu-id="ffba5-346">メソッド parmEnum</span><span class="sxs-lookup"><span data-stu-id="ffba5-346">Method parmEnum</span></span>

<span data-ttu-id="ffba5-347">parmEnumType メソッドで指定されている列挙型の列挙値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-347">Gets or sets the enumeration value of the enumeration type that is specified in the parmEnumType method.</span></span>

```xpp
public AnyType parmEnum([int value])
```

### <a name="parameters---parmenum"></a><span data-ttu-id="ffba5-348">パラメーター - parmEnum</span><span class="sxs-lookup"><span data-stu-id="ffba5-348">Parameters - parmEnum</span></span>

<span data-ttu-id="ffba5-349">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-349">value</span></span>  
<span data-ttu-id="ffba5-350">設定する列挙型のキー。オプション。</span><span class="sxs-lookup"><span data-stu-id="ffba5-350">The key of an enumeration value to set; optional.</span></span>

### <a name="return-value---parmenum"></a><span data-ttu-id="ffba5-351">戻り値 - parmEnum</span><span class="sxs-lookup"><span data-stu-id="ffba5-351">Return Value - parmEnum</span></span>

<span data-ttu-id="ffba5-352">parmEnumType メソッドで指定されている列挙型の列挙値。</span><span class="sxs-lookup"><span data-stu-id="ffba5-352">The enumeration value of the enumeration type that is specified in the parmEnumType method.</span></span>

### <a name="remarks---parmenum"></a><span data-ttu-id="ffba5-353">備考 - parmEnum</span><span class="sxs-lookup"><span data-stu-id="ffba5-353">Remarks - parmEnum</span></span>

<span data-ttu-id="ffba5-354">このメソッドは、次の parmEnumType メソッドでよく使用されます: args.parmEnumType(enumnum(AssetBookType));args.parmEnumType(enumnum(AssetBookType));</span><span class="sxs-lookup"><span data-stu-id="ffba5-354">This method is often used with the parmEnumType method: args.parmEnumType(enumnum(AssetBookType));args.parmEnumType(enumnum(AssetBookType));</span></span>

## <a name="method-parmenumtype"></a><span data-ttu-id="ffba5-355">メソッド parmEnumType</span><span class="sxs-lookup"><span data-stu-id="ffba5-355">Method parmEnumType</span></span>

<span data-ttu-id="ffba5-356">任意の列挙タイプの ID 値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-356">Gets or sets the ID value of any enumeration type.</span></span>

```xpp
public int parmEnumType([int value])
```

### <a name="parameters---parmenumtype"></a><span data-ttu-id="ffba5-357">パラメーター - parmEnumType</span><span class="sxs-lookup"><span data-stu-id="ffba5-357">Parameters - parmEnumType</span></span>

<span data-ttu-id="ffba5-358">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-358">value</span></span>  
<span data-ttu-id="ffba5-359">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-359">The value to set; optional.</span></span>

### <a name="return-value---parmenumtype"></a><span data-ttu-id="ffba5-360">戻り値 - parmEnumType</span><span class="sxs-lookup"><span data-stu-id="ffba5-360">Return Value - parmEnumType</span></span>

<span data-ttu-id="ffba5-361">列挙型の ID 値。</span><span class="sxs-lookup"><span data-stu-id="ffba5-361">The ID value of the enumeration type.</span></span>

### <a name="remarks---parmenumtype"></a><span data-ttu-id="ffba5-362">備考 - parmEnumType</span><span class="sxs-lookup"><span data-stu-id="ffba5-362">Remarks - parmEnumType</span></span>

<span data-ttu-id="ffba5-363">このメソッドは、parmEnum メソッドとともに使用され、呼び出されたオブジェクトに列挙型の特定の値を送信します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-363">This method is used with the parmEnum method to send a specific value of an enumeration type to the called object.</span></span> <span data-ttu-id="ffba5-364">例: args.parmEnumType(enumnum(AssetBookType));args.parmEnum(AssetBookType::ValueModel);</span><span class="sxs-lookup"><span data-stu-id="ffba5-364">For example: args.parmEnumType(enumnum(AssetBookType));args.parmEnum(AssetBookType::ValueModel);</span></span>

## <a name="method-parmobject"></a><span data-ttu-id="ffba5-365">メソッド parmObject</span><span class="sxs-lookup"><span data-stu-id="ffba5-365">Method parmObject</span></span>

<span data-ttu-id="ffba5-366">呼び出されるオブジェクトに渡す任意のオブジェクトのインスタンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-366">Gets or sets the instance of any object to pass to the called object.</span></span>

```xpp
public Object parmObject([Object value])
```

### <a name="parameters---parmobject"></a><span data-ttu-id="ffba5-367">パラメーター - parmObject</span><span class="sxs-lookup"><span data-stu-id="ffba5-367">Parameters - parmObject</span></span>

<span data-ttu-id="ffba5-368">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-368">value</span></span>  
<span data-ttu-id="ffba5-369">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-369">The value to set; optional.</span></span>

### <a name="return-value---parmobject"></a><span data-ttu-id="ffba5-370">戻り値 - parmObject</span><span class="sxs-lookup"><span data-stu-id="ffba5-370">Return Value - parmObject</span></span>

<span data-ttu-id="ffba5-371">呼び出されるオブジェクトに渡すオブジェクトのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="ffba5-371">The instance of an object to pass to the called object.</span></span>

### <a name="remarks---parmobject"></a><span data-ttu-id="ffba5-372">備考 - parmObject</span><span class="sxs-lookup"><span data-stu-id="ffba5-372">Remarks - parmObject</span></span>

<span data-ttu-id="ffba5-373">オブジェクト多くの場合、クラスになります。</span><span class="sxs-lookup"><span data-stu-id="ffba5-373">The object will often be a class.</span></span>

## <a name="method-record"></a><span data-ttu-id="ffba5-374">メソッド record</span><span class="sxs-lookup"><span data-stu-id="ffba5-374">Method record</span></span>

<span data-ttu-id="ffba5-375">呼び出し元オブジェクトが動作しているテーブルのレコードを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-375">Gets or sets the record from the table on which the caller object is working.</span></span>

```xpp
public Common record([Common value])
```

### <a name="parameters---record"></a><span data-ttu-id="ffba5-376">パラメーター - record</span><span class="sxs-lookup"><span data-stu-id="ffba5-376">Parameters - record</span></span>

<span data-ttu-id="ffba5-377">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-377">value</span></span>  
<span data-ttu-id="ffba5-378">設定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="ffba5-378">The value to set; optional.</span></span>

### <a name="return-value---record"></a><span data-ttu-id="ffba5-379">戻り値 - record</span><span class="sxs-lookup"><span data-stu-id="ffba5-379">Return Value - record</span></span>

<span data-ttu-id="ffba5-380">呼び出し元オブジェクトが動作しているテーブルのレコード。</span><span class="sxs-lookup"><span data-stu-id="ffba5-380">The record from the table on which the caller object is working.</span></span>

### <a name="remarks---record"></a><span data-ttu-id="ffba5-381">備考 - record</span><span class="sxs-lookup"><span data-stu-id="ffba5-381">Remarks - record</span></span>

<span data-ttu-id="ffba5-382">このメソッドは、呼び出し元のオブジェクトが現在使用しているレコードの値にアクセスするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-382">This method is used to access the values in the record that the calling object is currently using.</span></span>

## <a name="method-reffield"></a><span data-ttu-id="ffba5-383">メソッド refField</span><span class="sxs-lookup"><span data-stu-id="ffba5-383">Method refField</span></span>

```xpp
public FieldId refField([FieldId value])
```

### <a name="parameters---reffield"></a><span data-ttu-id="ffba5-384">パラメーター - refField</span><span class="sxs-lookup"><span data-stu-id="ffba5-384">Parameters - refField</span></span>

<span data-ttu-id="ffba5-385">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-385">value</span></span>  

### <a name="return-value---reffield"></a><span data-ttu-id="ffba5-386">戻り値 - refField</span><span class="sxs-lookup"><span data-stu-id="ffba5-386">Return Value - refField</span></span>

## <a name="method-getrequestcontextquery"></a><span data-ttu-id="ffba5-387">メソッド getRequestContextQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-387">Method getRequestContextQuery</span></span>

```xpp
public str getRequestContextQuery()
```

### <a name="return-value---getrequestcontextquery"></a><span data-ttu-id="ffba5-388">戻り値 - getRequestContextQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-388">Return Value - getRequestContextQuery</span></span>

## <a name="method-requestcontextquery"></a><span data-ttu-id="ffba5-389">メソッド requestContextQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-389">Method requestContextQuery</span></span>

```xpp
public str requestContextQuery(str value)
```

### <a name="parameters---requestcontextquery"></a><span data-ttu-id="ffba5-390">パラメーター - requestContextQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-390">Parameters - requestContextQuery</span></span>

<span data-ttu-id="ffba5-391">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-391">value</span></span>  

### <a name="return-value---requestcontextquery"></a><span data-ttu-id="ffba5-392">戻り値 - requestContextQuery</span><span class="sxs-lookup"><span data-stu-id="ffba5-392">Return Value - requestContextQuery</span></span>

## <a name="method-selectfield"></a><span data-ttu-id="ffba5-393">メソッド selectField</span><span class="sxs-lookup"><span data-stu-id="ffba5-393">Method selectField</span></span>

```xpp
public FieldId selectField([FieldId value])
```

### <a name="parameters---selectfield"></a><span data-ttu-id="ffba5-394">パラメーター - selectField</span><span class="sxs-lookup"><span data-stu-id="ffba5-394">Parameters - selectField</span></span>

<span data-ttu-id="ffba5-395">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-395">value</span></span>  

### <a name="return-value---selectfield"></a><span data-ttu-id="ffba5-396">戻り値 - selectField</span><span class="sxs-lookup"><span data-stu-id="ffba5-396">Return Value - selectField</span></span>

## <a name="method-tostring"></a><span data-ttu-id="ffba5-397">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="ffba5-397">Method toString</span></span>

<span data-ttu-id="ffba5-398">xArgs のインスタンスの文字列形式を取得します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-398">Retrieves a string representation of an instance of the xArgs.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="ffba5-399">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="ffba5-399">Return Value - toString</span></span>

<span data-ttu-id="ffba5-400">xArgs クラスのインスタンスの説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="ffba5-400">A string that contains a description of the instance of the xArgs class.</span></span>

## <a name="method-applyrecordasdynalink"></a><span data-ttu-id="ffba5-401">メソッド applyRecordAsDynalink</span><span class="sxs-lookup"><span data-stu-id="ffba5-401">Method applyRecordAsDynalink</span></span>

```xpp
public boolean applyRecordAsDynalink([boolean applyAsDynalink])
```

### <a name="parameters---applyrecordasdynalink"></a><span data-ttu-id="ffba5-402">パラメーター - applyRecordAsDynalink</span><span class="sxs-lookup"><span data-stu-id="ffba5-402">Parameters - applyRecordAsDynalink</span></span>

<span data-ttu-id="ffba5-403">applyAsDynalink</span><span class="sxs-lookup"><span data-stu-id="ffba5-403">applyAsDynalink</span></span>  

### <a name="return-value---applyrecordasdynalink"></a><span data-ttu-id="ffba5-404">戻り値 - applyRecordAsDynalink</span><span class="sxs-lookup"><span data-stu-id="ffba5-404">Return Value - applyRecordAsDynalink</span></span>

## <a name="method-oncallerchanged"></a><span data-ttu-id="ffba5-405">メソッド onCallerChanged</span><span class="sxs-lookup"><span data-stu-id="ffba5-405">Method onCallerChanged</span></span>

```xpp
public void onCallerChanged([Object value])
```

### <a name="parameters---oncallerchanged"></a><span data-ttu-id="ffba5-406">パラメーター - onCallerChanged</span><span class="sxs-lookup"><span data-stu-id="ffba5-406">Parameters - onCallerChanged</span></span>

<span data-ttu-id="ffba5-407">値</span><span class="sxs-lookup"><span data-stu-id="ffba5-407">value</span></span>  

## <a name="method-new"></a><span data-ttu-id="ffba5-408">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ffba5-408">Method new</span></span>

<span data-ttu-id="ffba5-409">このクラスのインスタンスを構築します。このインスタンスは、FormRun クラスや ReportRun クラスなどの上位クラスに情報を渡すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-409">Constructs an instance of this class, which is used to pass information to high-level classes such as the FormRun or ReportRun class.</span></span>

```xpp
public void new([AnyType nameOrCaller], [Object object])
```

### <a name="parameters---new"></a><span data-ttu-id="ffba5-410">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="ffba5-410">Parameters - new</span></span>

<span data-ttu-id="ffba5-411">nameOrCaller</span><span class="sxs-lookup"><span data-stu-id="ffba5-411">nameOrCaller</span></span>  
<span data-ttu-id="ffba5-412">オブジェクトの引数。オプション。</span><span class="sxs-lookup"><span data-stu-id="ffba5-412">An object argument; optional.</span></span> <span data-ttu-id="ffba5-413">このパラメーターは、xArgs クラスのインスタンスを作成するために使用され、nameOrCaller パラメーターが呼び出し元の引数である場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-413">This parameter is used to create the instance of the xArgs class and is used when the nameOrCaller parameter is a caller argument.</span></span>

<!-- -->

<span data-ttu-id="ffba5-414">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="ffba5-414">object</span></span>  
<span data-ttu-id="ffba5-415">オブジェクトの引数。オプション。</span><span class="sxs-lookup"><span data-stu-id="ffba5-415">An object argument; optional.</span></span> <span data-ttu-id="ffba5-416">このパラメーターは、xArgs クラスのインスタンスを作成するために使用され、nameOrCaller パラメーターが呼び出し元の引数である場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-416">This parameter is used to create the instance of the xArgs class and is used when the nameOrCaller parameter is a caller argument.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="ffba5-417">備考 - new</span><span class="sxs-lookup"><span data-stu-id="ffba5-417">Remarks - new</span></span>

<span data-ttu-id="ffba5-418">xArgs オブジェクトを作成するには、(呼び出し元、オブジェクト) のペアまたは Name 引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-418">To create an xArgs object, either supply a (Caller, Object) pair or a Name argument.</span></span> <span data-ttu-id="ffba5-419">どちらの引数もオプションであり適切な方法を呼び出すことによって構築した後すべての値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ffba5-419">Both arguments are optional and all values can be set after it is constructed by calling the appropriate methods.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="ffba5-420">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ffba5-420">Method finalize</span></span>

<span data-ttu-id="ffba5-421">メモリから xArgs クラスの現在のインスタンスを削除します。</span><span class="sxs-lookup"><span data-stu-id="ffba5-421">Removes the current instance of the xArgs class from memory.</span></span>

```xpp
public void finalize()
```

## <a name="method-setupargs"></a><span data-ttu-id="ffba5-422">メソッド setupArgs</span><span class="sxs-lookup"><span data-stu-id="ffba5-422">Method setupArgs</span></span>

```xpp
public void setupArgs(str parm, int enumType, AnyType enumValue, [str menuItemName], [int menuItemType])
```

### <a name="parameters---setupargs"></a><span data-ttu-id="ffba5-423">パラメーター - setupArgs</span><span class="sxs-lookup"><span data-stu-id="ffba5-423">Parameters - setupArgs</span></span>

<span data-ttu-id="ffba5-424">parm</span><span class="sxs-lookup"><span data-stu-id="ffba5-424">parm</span></span>  

<!-- -->

<span data-ttu-id="ffba5-425">enumType</span><span class="sxs-lookup"><span data-stu-id="ffba5-425">enumType</span></span>  

<!-- -->

<span data-ttu-id="ffba5-426">enumValue</span><span class="sxs-lookup"><span data-stu-id="ffba5-426">enumValue</span></span>  

<!-- -->

<span data-ttu-id="ffba5-427">menuItemName</span><span class="sxs-lookup"><span data-stu-id="ffba5-427">menuItemName</span></span>  

<!-- -->

<span data-ttu-id="ffba5-428">menuItemType</span><span class="sxs-lookup"><span data-stu-id="ffba5-428">menuItemType</span></span>  


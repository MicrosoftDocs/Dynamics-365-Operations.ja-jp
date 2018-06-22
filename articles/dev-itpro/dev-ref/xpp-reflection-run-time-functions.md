---
title: "X++ リフレクション ランタイム関数"
description: "このトピックでは、リフレクション ランタイム関数について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 31381
ms.assetid: d0d4043e-5abb-42ae-bcc2-c6b678f4ef5b
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2da9be1bec598fa86c24f22e0c47cd1eaa32a44f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="x-reflection-run-time-functions"></a><span data-ttu-id="6972f-103">X++ リフレクション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="6972f-103">X++ reflection run-time functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6972f-104">このトピックでは、リフレクション ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="6972f-104">This topic describes the reflection run-time functions.</span></span>

<a name="classidget"></a><span data-ttu-id="6972f-105">classIdGet</span><span class="sxs-lookup"><span data-stu-id="6972f-105">classIdGet</span></span>
----------

<span data-ttu-id="6972f-106">初期化されるオブジェクトが属しているクラスの数値識別子 (クラス ID) を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-106">Retrieves the numeric identifier (the class ID) of the class that the object that is initialized belongs to.</span></span>

    int classIdGet(class object)

### <a name="parameters"></a><span data-ttu-id="6972f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-107">Parameters</span></span>

| <span data-ttu-id="6972f-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-108">Parameter</span></span> | <span data-ttu-id="6972f-109">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-109">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="6972f-110">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6972f-110">object</span></span>    | <span data-ttu-id="6972f-111">クラス ID を取得するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="6972f-111">The object to get the class ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-112">Return value</span></span>

<span data-ttu-id="6972f-113">指定されたオブジェクトのクラス ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-113">The class ID of the specified object.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-114">例</span><span class="sxs-lookup"><span data-stu-id="6972f-114">Example</span></span>

    static void classIdGetExample(Args _args)
    {
            int i;
            WorkTimeCheck w;

            i = classIdGet(w);
            print "Class ID for object is " + int2Str(i);
    }

## <a name="dimof"></a><span data-ttu-id="6972f-115">dimOf</span><span class="sxs-lookup"><span data-stu-id="6972f-115">dimOf</span></span>
<span data-ttu-id="6972f-116">X++ 配列内で領域が割り当てられているインデックス要素の番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-116">Retrieves the number of index elements that space has been allocated for in an X++ array.</span></span>

    int dimOf(anytype object)

### <a name="parameters"></a><span data-ttu-id="6972f-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-117">Parameters</span></span>

| <span data-ttu-id="6972f-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-118">Parameter</span></span> | <span data-ttu-id="6972f-119">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-119">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="6972f-120">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6972f-120">object</span></span>    | <span data-ttu-id="6972f-121">分析コード サイズを決定するための配列。</span><span class="sxs-lookup"><span data-stu-id="6972f-121">The array to determine the dimension size of.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-122">Return value</span></span>

<span data-ttu-id="6972f-123">*オブジェクト* パラメーターの値が配列である場合、値は配列の要素の数になります。それ以外の場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="6972f-123">If the value of the *object* parameter is an array, the number of elements in the array; otherwise, **0** (zero).</span></span>

### <a name="remarks"></a><span data-ttu-id="6972f-124">備考</span><span class="sxs-lookup"><span data-stu-id="6972f-124">Remarks</span></span>

<span data-ttu-id="6972f-125">**dimOf** 関数は、次の X++ プリミティブ型として宣言されている X++ 配列に使用されます。</span><span class="sxs-lookup"><span data-stu-id="6972f-125">The **dimOf** function is intended for X++ arrays that are declared as the following X++ primitive types:</span></span>

-   <span data-ttu-id="6972f-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="6972f-126">boolean</span></span>
-   <span data-ttu-id="6972f-127">日付</span><span class="sxs-lookup"><span data-stu-id="6972f-127">date</span></span>
-   <span data-ttu-id="6972f-128">int</span><span class="sxs-lookup"><span data-stu-id="6972f-128">int</span></span>
-   <span data-ttu-id="6972f-129">int64</span><span class="sxs-lookup"><span data-stu-id="6972f-129">int64</span></span>
-   <span data-ttu-id="6972f-130">real</span><span class="sxs-lookup"><span data-stu-id="6972f-130">real</span></span>
-   <span data-ttu-id="6972f-131">utcDateTime</span><span class="sxs-lookup"><span data-stu-id="6972f-131">utcDateTime</span></span>

<span data-ttu-id="6972f-132">たとえば **int iAmounts\[6\];** です。</span><span class="sxs-lookup"><span data-stu-id="6972f-132">An example is **int iAmounts\[6\];**.</span></span> <span data-ttu-id="6972f-133">列挙値および拡張データ型の配列も、前述のプリミティブ データ型のいずれかに最終的に基づいている場合はサポートされています (**int** など) 。</span><span class="sxs-lookup"><span data-stu-id="6972f-133">Arrays of enumeration values and extended data types are also supported if they are ultimately based on one of the preceding primitive data types (such as **int**).</span></span> <span data-ttu-id="6972f-134">**dimOf** 機能は、すべての X++ プリミティブ型の配列を受け入れるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="6972f-134">The **dimOf** function doesn't accept arrays of all X++ primitive types.</span></span> <span data-ttu-id="6972f-135">**dimOf** 関数が受け入れない配列タイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="6972f-135">Here are the array types that the **dimOf** function doesn't accept:</span></span>

-   <span data-ttu-id="6972f-136">**str**</span><span class="sxs-lookup"><span data-stu-id="6972f-136">**str**</span></span>
-   <span data-ttu-id="6972f-137">**コンテナー**</span><span class="sxs-lookup"><span data-stu-id="6972f-137">**container**</span></span>
-   <span data-ttu-id="6972f-138">**anytype**</span><span class="sxs-lookup"><span data-stu-id="6972f-138">**anytype**</span></span>
-   <span data-ttu-id="6972f-139">クラス オブジェクトの配列</span><span class="sxs-lookup"><span data-stu-id="6972f-139">Arrays of class objects</span></span>
-   <span data-ttu-id="6972f-140">**配列**クラスのインスタンス</span><span class="sxs-lookup"><span data-stu-id="6972f-140">Instances of the **Array** class</span></span>

### <a name="example"></a><span data-ttu-id="6972f-141">例</span><span class="sxs-lookup"><span data-stu-id="6972f-141">Example</span></span>

    static void JobDimOfArrays(Args _args)
    {
            int iAmounts[20], iCounts[];
            ABCModel enumAbcModel[22]; // Enum
            ABCModelType exdtAbcModelType[24]; // Extended data type
            anytype anyThings[26];
            str sNames[28];
            Array myArrayObj; // Class

            info("Start of job.");
            info("--(Next, normal int array, dimOf() accepts it.)");
            info(int2Str(dimOf(iAmounts)));
            info("--(Next, normal enum array, dimOf() accepts it.)");
            info(int2Str(dimOf(enumAbcModel)));
            info("--(Next, normal extended data type array (based on enum), dimOf() accepts it.)");
            info(int2Str(dimOf(exdtAbcModelType)));
            info("--(Next, dynamic int array, dimension not yet set.)");
            info(int2Str(dimOf(iCounts)));
            info("--(Next, dynamic int array, after dimension established.)");

            iCounts[13] = 13;
            info(int2Str(dimOf(iCounts)));
            info(" == == == == == (Next, array types that dimOf() does not support.)");
            info("--(Next, normal anytype array, dimOf() always returns 0.)");
            info(int2Str(dimOf(anyThings)));
            info("--(Next, an instance of class X++ Array, dimOf() always returns 0.)");

            myArrayObj = new Array(Types::Integer);
            myArrayObj.value(1,501);
            info(int2Str(dimOf(myArrayObj)));
            info("--(Next, the lastIndex method provides size information about Array instances.)");
            info(int2Str(myArrayObj.lastIndex()));
            info("--(Next, normal str array, dimOf() does not accept it, job is halted.)");
            info(int2Str(dimOf(sNames)));
            info("End of job.");

    }
    /************  Actual Infolog output
    Message (11:10:06 am)
    Start of job.
    --(Next, normal int array, dimOf() accepts it.)
    20
    --(Next, normal enum array, dimOf() accepts it.)
    22
    --(Next, normal extended data type array (based on enum), dimOf() accepts it.)
    24
    --(Next, dynamic int array, dimension not yet set.)
    0
    --(Next, dynamic int array, after dimension established.)
    16
    == == == == == (Next, array types that dimOf() does not support.)
    --(Next, normal anytype array, dimOf() always returns 0.)
    0
    --(Next, an instance of class X++ Array, dimOf() always returns 0.)
    0
    --(Next, the lastIndex method provides size information about Array instances.)
    1
    --(Next, normal str array, dimOf() does not accept it, job is halted.)
    Error executing code: Illegal operation on this type of array. (C)JobsJobDimOfArrays - line 41
    ************/
    /***********  Pop-up error dialog box
    "Internal error number 25 in script."
    This error is caused by the code line...
    info(int2Str(dimOf(iCounts)));
    ...before iCounts was assigned at any index.
    ***********/

## <a name="fieldid2name"></a><span data-ttu-id="6972f-142">fieldId2Name</span><span class="sxs-lookup"><span data-stu-id="6972f-142">fieldId2Name</span></span>
<span data-ttu-id="6972f-143">テーブルの ID 番号とフィールドの ID 番号で指定されているフィールドの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-143">Retrieves a string that represents the name of the field that is specified by a table ID number and a field ID number.</span></span>

    str fieldId2Name(int tableid, int fieldid)

### <a name="parameters"></a><span data-ttu-id="6972f-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-144">Parameters</span></span>

| <span data-ttu-id="6972f-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-145">Parameter</span></span> | <span data-ttu-id="6972f-146">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-146">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6972f-147">tableid</span><span class="sxs-lookup"><span data-stu-id="6972f-147">tableid</span></span>   | <span data-ttu-id="6972f-148">テーブルの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6972f-148">The ID number of the table.</span></span> <span data-ttu-id="6972f-149">**注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6972f-149">**Note:** Use the **tableName2Id** function to specify the ID of a table.</span></span> |
| <span data-ttu-id="6972f-150">fieldid</span><span class="sxs-lookup"><span data-stu-id="6972f-150">fieldid</span></span>   | <span data-ttu-id="6972f-151">フィールドの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6972f-151">The ID number of the field.</span></span>                                                                           |

### <a name="return-value"></a><span data-ttu-id="6972f-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-152">Return value</span></span>

<span data-ttu-id="6972f-153">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-153">The name of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="6972f-154">備考</span><span class="sxs-lookup"><span data-stu-id="6972f-154">Remarks</span></span>

<span data-ttu-id="6972f-155">フィールド名の印刷可能なバージョンを返すには、**fieldId2PName** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6972f-155">To return a printable version of the field name, use the **fieldId2PName** function.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-156">例</span><span class="sxs-lookup"><span data-stu-id="6972f-156">Example</span></span>

<span data-ttu-id="6972f-157">次の例では、フィールド ID が 7 の Customer (CustGroup) テーブルのフィールド名に **fn** を設定しています。</span><span class="sxs-lookup"><span data-stu-id="6972f-157">The following example sets **fn** to the name of the field in the Customer (CustGroup) table that has a field ID of 7.</span></span>

    static void fieldId2NameExample(Args _arg)
    {
            str fn;
            fn = fieldId2Name(tableName2Id("Customer"),7);
    }

## <a name="fieldid2pname"></a><span data-ttu-id="6972f-158">fieldId2PName</span><span class="sxs-lookup"><span data-stu-id="6972f-158">fieldId2PName</span></span>
<span data-ttu-id="6972f-159">テーブルの ID 番号とフィールドの ID 番号で指定されているフィールドの出力可能な名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-159">Retrieves the printable name of the field that is specified by a table ID number and a field ID number.</span></span>

    str fieldId2PName(int tableid, int fieldid)

### <a name="parameters"></a><span data-ttu-id="6972f-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-160">Parameters</span></span>

| <span data-ttu-id="6972f-161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-161">Parameter</span></span> | <span data-ttu-id="6972f-162">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-162">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6972f-163">tableid</span><span class="sxs-lookup"><span data-stu-id="6972f-163">tableid</span></span>   | <span data-ttu-id="6972f-164">テーブルの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6972f-164">The ID number of the table.</span></span> <span data-ttu-id="6972f-165">**注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6972f-165">**Note:** Use the **tableName2Id** function to specify the ID of a table.</span></span> |
| <span data-ttu-id="6972f-166">fieldid</span><span class="sxs-lookup"><span data-stu-id="6972f-166">fieldid</span></span>   | <span data-ttu-id="6972f-167">フィールドの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6972f-167">The ID number of the field.</span></span> <span data-ttu-id="6972f-168">**注記:** フィールドの ID を指定するには、**fieldName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6972f-168">**Note:** Use the **fieldName2Id** function to specify the ID of a field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-169">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-169">Return value</span></span>

<span data-ttu-id="6972f-170">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-170">The name of the field.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-171">例</span><span class="sxs-lookup"><span data-stu-id="6972f-171">Example</span></span>

    static void fieldId2PNameExample(Args _arg)
    {
            str name;
            tableid _tableId;
            fieldid _fieldid;

            _tableId = tableName2Id("Address");
            _fieldId = fieldName2Id(_tableId, "Name");
            name = fieldId2PName(_tableId, _fieldid);
            print name;
    }

## <a name="fieldname2id"></a><span data-ttu-id="6972f-172">fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="6972f-172">fieldName2Id</span></span>
<span data-ttu-id="6972f-173">テーブルの ID 番号とフィールドの ID 番号で指定されているテーブル フィールドのフィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-173">Retrieves the field ID of the table field that is specified by a table ID number and a field ID number.</span></span>

    int fieldName2Id(int tableid, str fieldname)

### <a name="parameters"></a><span data-ttu-id="6972f-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-174">Parameters</span></span>

| <span data-ttu-id="6972f-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-175">Parameter</span></span> | <span data-ttu-id="6972f-176">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-176">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6972f-177">tableid</span><span class="sxs-lookup"><span data-stu-id="6972f-177">tableid</span></span>   | <span data-ttu-id="6972f-178">テーブルの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="6972f-178">The ID number of the table.</span></span> <span data-ttu-id="6972f-179">**注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="6972f-179">**Note:** Use the **tableName2Id** function to specify the ID of a table.</span></span> |
| <span data-ttu-id="6972f-180">fieldname</span><span class="sxs-lookup"><span data-stu-id="6972f-180">fieldname</span></span> | <span data-ttu-id="6972f-181">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-181">The name of the field.</span></span>                                                                                |

### <a name="return-value"></a><span data-ttu-id="6972f-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-182">Return value</span></span>

<span data-ttu-id="6972f-183">*tableid* および *fieldname* パラメーターにより指定されているフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-183">The ID of the field that is specified by the *tableid* and *fieldname* parameters.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-184">例</span><span class="sxs-lookup"><span data-stu-id="6972f-184">Example</span></span>

    static void fieldName2IdExample(Args _arg)
    {
            int id;

            id = fieldName2Id(tableName2Id("Address"), "Name");
            // Returns 6. Name is the 6th field in the Address table.
            print id;
    }

## <a name="indexid2name"></a><span data-ttu-id="6972f-185">indexId2Name</span><span class="sxs-lookup"><span data-stu-id="6972f-185">indexId2Name</span></span>
<span data-ttu-id="6972f-186">インデックスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-186">Retrieves the name of an index.</span></span>

    str indexId2Name(int tableid, int indexid)

### <a name="parameters"></a><span data-ttu-id="6972f-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-187">Parameters</span></span>

| <span data-ttu-id="6972f-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-188">Parameter</span></span> | <span data-ttu-id="6972f-189">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-189">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="6972f-190">tableid</span><span class="sxs-lookup"><span data-stu-id="6972f-190">tableid</span></span>   | <span data-ttu-id="6972f-191">インデックスが属するテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-191">The ID of the table that the index belongs to.</span></span> |
| <span data-ttu-id="6972f-192">indexid</span><span class="sxs-lookup"><span data-stu-id="6972f-192">indexid</span></span>   | <span data-ttu-id="6972f-193">インデックスの ID です。</span><span class="sxs-lookup"><span data-stu-id="6972f-193">The ID of the index.</span></span>                           |

### <a name="return-value"></a><span data-ttu-id="6972f-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-194">Return value</span></span>

<span data-ttu-id="6972f-195">インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-195">The name of the index.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-196">例</span><span class="sxs-lookup"><span data-stu-id="6972f-196">Example</span></span>

    static void indexId2NameExample(Args _arg)
    {
            str s;
            tableid id;
            indexid idx;

            id  = tableName2Id("Address");
            idx = indexName2Id(id, "AddrIdx");
            s = indexId2Name(id, idx);
            print "The result of calling indexId2Name is " + s;
    }

## <a name="indexname2id"></a><span data-ttu-id="6972f-197">indexName2Id</span><span class="sxs-lookup"><span data-stu-id="6972f-197">indexName2Id</span></span>
<span data-ttu-id="6972f-198">インデックスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-198">Retrieves the ID of an index.</span></span>

    int indexName2Id(int tableid, str indexname)

### <a name="parameters"></a><span data-ttu-id="6972f-199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-199">Parameters</span></span>

| <span data-ttu-id="6972f-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-200">Parameter</span></span> | <span data-ttu-id="6972f-201">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-201">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="6972f-202">tableid</span><span class="sxs-lookup"><span data-stu-id="6972f-202">tableid</span></span>   | <span data-ttu-id="6972f-203">インデックスが属するテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-203">The ID of the table that the index belongs to.</span></span> |
| <span data-ttu-id="6972f-204">indexname</span><span class="sxs-lookup"><span data-stu-id="6972f-204">indexname</span></span> | <span data-ttu-id="6972f-205">インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-205">The name of the index.</span></span>                         |

### <a name="return-value"></a><span data-ttu-id="6972f-206">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-206">Return value</span></span>

<span data-ttu-id="6972f-207">インデックスの ID です。</span><span class="sxs-lookup"><span data-stu-id="6972f-207">The ID of the index.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-208">例</span><span class="sxs-lookup"><span data-stu-id="6972f-208">Example</span></span>

    static void indexName2IdExample(Args _arg)
    {
            indexid idx;
            tableid id;

            id  = tableName2Id("Address");
            idx = indexName2Id(id, "AddrIdx");
            print "Index ID for index name AddrIdx of table Address is " + int2Str(idx);
    }

## <a name="refprintall-no-content"></a><span data-ttu-id="6972f-209">refPrintAll (コンテンツなし)</span><span class="sxs-lookup"><span data-stu-id="6972f-209">refPrintAll (no content)</span></span>
<span data-ttu-id="6972f-210">集計</span><span class="sxs-lookup"><span data-stu-id="6972f-210">Summary</span></span>

    void refPrintAll(class object, str filename, str title)

### <a name="parameters"></a><span data-ttu-id="6972f-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-211">Parameters</span></span>

| <span data-ttu-id="6972f-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-212">Parameter</span></span> | <span data-ttu-id="6972f-213">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-213">Description</span></span> |
|-----------|-------------|
| <span data-ttu-id="6972f-214">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6972f-214">object</span></span>    | <span data-ttu-id="6972f-215">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-215">Description</span></span> |
| <span data-ttu-id="6972f-216">filename</span><span class="sxs-lookup"><span data-stu-id="6972f-216">filename</span></span>  | <span data-ttu-id="6972f-217">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-217">Description</span></span> |
| <span data-ttu-id="6972f-218">title</span><span class="sxs-lookup"><span data-stu-id="6972f-218">title</span></span>     | <span data-ttu-id="6972f-219">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-219">Description</span></span> |

## <a name="tableid2name"></a><span data-ttu-id="6972f-220">tableId2Name</span><span class="sxs-lookup"><span data-stu-id="6972f-220">tableId2Name</span></span>
<span data-ttu-id="6972f-221">テーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-221">Retrieves a string that contains the name of a table.</span></span>

    str tableId2Name(int _tableid)

### <a name="parameters"></a><span data-ttu-id="6972f-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-222">Parameters</span></span>

| <span data-ttu-id="6972f-223">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-223">Parameter</span></span> | <span data-ttu-id="6972f-224">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-224">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="6972f-225">\_tableid</span><span class="sxs-lookup"><span data-stu-id="6972f-225">\_tableid</span></span> | <span data-ttu-id="6972f-226">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-226">The ID of the table.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-227">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-227">Return value</span></span>

<span data-ttu-id="6972f-228">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-228">The name of the table.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-229">例</span><span class="sxs-lookup"><span data-stu-id="6972f-229">Example</span></span>

    static void tableId2NameExample(Args _arg)
    {
            str s;
            tableid id;

            // Get the ID for table name Address.
            id = tableName2Id("Address");
            print "ID for table name Address is " + int2Str(id);

            // Get the name from the table ID.
            s = tableId2Name(id);
            print "Name for table ID " + int2Str(id) + " is " + s;

            // Get the printable name from the table ID.
            s = tableId2PName(id);
            print "Printable name for table ID " + int2Str(id) + " is " + s;
    }

## <a name="tableid2pname"></a><span data-ttu-id="6972f-230">tableId2PName</span><span class="sxs-lookup"><span data-stu-id="6972f-230">tableId2PName</span></span>
<span data-ttu-id="6972f-231">テーブルの出力可能な名前 (ラベル) を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-231">Retrieves a string that contains the printable name (the label) of a table.</span></span>

    str tableId2PName(int _fieldid)

### <a name="parameters"></a><span data-ttu-id="6972f-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-232">Parameters</span></span>

| <span data-ttu-id="6972f-233">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-233">Parameter</span></span> | <span data-ttu-id="6972f-234">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-234">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="6972f-235">\_fieldid</span><span class="sxs-lookup"><span data-stu-id="6972f-235">\_fieldid</span></span> | <span data-ttu-id="6972f-236">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-236">The ID of the table.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-237">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-237">Return value</span></span>

<span data-ttu-id="6972f-238">テーブルのラベル。</span><span class="sxs-lookup"><span data-stu-id="6972f-238">The label of the table.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-239">例</span><span class="sxs-lookup"><span data-stu-id="6972f-239">Example</span></span>

    static void tableId2NameExample(Args _arg)
    {
            str s;
            tableid id;

            // Get the ID for table name Address.
            id = tableName2Id("Address");
            print "ID for table name Address is " + int2Str(id);

            // Get the name from the table ID.
            s = tableId2Name(id);
            print "Name for table ID " + int2Str(id) + " is " + s;

            // Get the printable name from the table ID.
            s = tableId2PName(id);
            print "Printable name for table ID " + int2Str(id) + " is " + s;
    }

## <a name="tablename2id"></a><span data-ttu-id="6972f-240">tableName2Id</span><span class="sxs-lookup"><span data-stu-id="6972f-240">tableName2Id</span></span>
<span data-ttu-id="6972f-241">テーブルの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-241">Retrieves the ID of a table.</span></span>

    int tableName2Id(str _name)

### <a name="parameters"></a><span data-ttu-id="6972f-242">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-242">Parameters</span></span>

| <span data-ttu-id="6972f-243">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-243">Parameter</span></span> | <span data-ttu-id="6972f-244">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-244">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="6972f-245">\_名前</span><span class="sxs-lookup"><span data-stu-id="6972f-245">\_name</span></span>    | <span data-ttu-id="6972f-246">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="6972f-246">The name of the table.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-247">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-247">Return value</span></span>

<span data-ttu-id="6972f-248">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="6972f-248">The ID of the table.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-249">例</span><span class="sxs-lookup"><span data-stu-id="6972f-249">Example</span></span>

    static void tableName2IdExample(Args _arg)
    {
            str s;
            tableid id;

            // Get the ID for the Address table name.
            id = tableName2Id("Address");
            print "ID for the Address table name is " + int2Str(id);

            // Get the name from the table ID.
            s = tableId2Name(id);
            print "Name for table ID " + int2Str(id) + " is " + s;

            // Get the printable name from the table ID.
            s = tableId2PName(id);
            print "Printable name for table ID " + int2Str(id) + " is " + s;
    }

## <a name="typeof"></a><span data-ttu-id="6972f-250">typeOf</span><span class="sxs-lookup"><span data-stu-id="6972f-250">typeOf</span></span>
<span data-ttu-id="6972f-251">要素のタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="6972f-251">Retrieves the type of an element.</span></span>

    enum typeOf(anytype _object)

### <a name="parameters"></a><span data-ttu-id="6972f-252">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-252">Parameters</span></span>

| <span data-ttu-id="6972f-253">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6972f-253">Parameter</span></span> | <span data-ttu-id="6972f-254">説明</span><span class="sxs-lookup"><span data-stu-id="6972f-254">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="6972f-255">\_オブジェクト</span><span class="sxs-lookup"><span data-stu-id="6972f-255">\_object</span></span>  | <span data-ttu-id="6972f-256">タイプを返す対象の要素。</span><span class="sxs-lookup"><span data-stu-id="6972f-256">The element to return the type for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="6972f-257">戻り値</span><span class="sxs-lookup"><span data-stu-id="6972f-257">Return value</span></span>

<span data-ttu-id="6972f-258">**タイプ**システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="6972f-258">A **Types** system enumeration value.</span></span>

### <a name="example"></a><span data-ttu-id="6972f-259">例</span><span class="sxs-lookup"><span data-stu-id="6972f-259">Example</span></span>

<span data-ttu-id="6972f-260">次の例では、コンテナ内の最初の要素、**c** が単一の整数を含む別のコンテナーであるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="6972f-260">The following example tests whether the first element in a container, **c**, is another container that contains a single integer.</span></span>

    if(typeof(conpeek(c, 1)) != Types::Container ||
    conlen(conpeek(c, 1)) != 1 ||
    typeof(conpeek(conpeek(c, 1), 1)) != Types::Integer)
    {
            // More code.
    }





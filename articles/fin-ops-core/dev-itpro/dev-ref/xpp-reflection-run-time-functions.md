---
title: X++ リフレクション ランタイム関数
description: このトピックでは、リフレクション ランタイム関数について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 31381
ms.assetid: d0d4043e-5abb-42ae-bcc2-c6b678f4ef5b
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cbabf876f4dc40761b1b4c70af155d2a07dd7b2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191594"
---
# <a name="x-reflection-runtime-functions"></a><span data-ttu-id="84a0d-103">X++ リフレクション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="84a0d-103">X++ reflection runtime functions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84a0d-104">このトピックでは、リフレクション ランタイム関数について説明します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-104">This topic describes the reflection run-time functions.</span></span>

<a name="classidget"></a><span data-ttu-id="84a0d-105">classIdGet</span><span class="sxs-lookup"><span data-stu-id="84a0d-105">classIdGet</span></span>
----------

<span data-ttu-id="84a0d-106">初期化されるオブジェクトが属しているクラスの数値識別子 (クラス ID) を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-106">Retrieves the numeric identifier (the class ID) of the class that the object that is initialized belongs to.</span></span>

    int classIdGet(class object)

### <a name="parameters"></a><span data-ttu-id="84a0d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-107">Parameters</span></span>

| <span data-ttu-id="84a0d-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-108">Parameter</span></span> | <span data-ttu-id="84a0d-109">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-109">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="84a0d-110">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="84a0d-110">object</span></span>    | <span data-ttu-id="84a0d-111">クラス ID を取得するオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="84a0d-111">The object to get the class ID for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-112">Return value</span></span>

<span data-ttu-id="84a0d-113">指定されたオブジェクトのクラス ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-113">The class ID of the specified object.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-114">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-114">Example</span></span>

    static void classIdGetExample(Args _args)
    {
            int i;
            WorkTimeCheck w;

            i = classIdGet(w);
            print "Class ID for object is " + int2Str(i);
    }

## <a name="dimof"></a><span data-ttu-id="84a0d-115">dimOf</span><span class="sxs-lookup"><span data-stu-id="84a0d-115">dimOf</span></span>
<span data-ttu-id="84a0d-116">X++ 配列内で領域が割り当てられているインデックス要素の番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-116">Retrieves the number of index elements that space has been allocated for in an X++ array.</span></span>

    int dimOf(anytype object)

### <a name="parameters"></a><span data-ttu-id="84a0d-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-117">Parameters</span></span>

| <span data-ttu-id="84a0d-118">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-118">Parameter</span></span> | <span data-ttu-id="84a0d-119">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-119">Description</span></span>                                   |
|-----------|-----------------------------------------------|
| <span data-ttu-id="84a0d-120">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="84a0d-120">object</span></span>    | <span data-ttu-id="84a0d-121">分析コード サイズを決定するための配列。</span><span class="sxs-lookup"><span data-stu-id="84a0d-121">The array to determine the dimension size of.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-122">Return value</span></span>

<span data-ttu-id="84a0d-123">*オブジェクト* パラメーターの値が配列である場合、値は配列の要素の数になります。それ以外の場合は **0** (ゼロ) になります。</span><span class="sxs-lookup"><span data-stu-id="84a0d-123">If the value of the *object* parameter is an array, the number of elements in the array; otherwise, **0** (zero).</span></span>

### <a name="remarks"></a><span data-ttu-id="84a0d-124">備考</span><span class="sxs-lookup"><span data-stu-id="84a0d-124">Remarks</span></span>

<span data-ttu-id="84a0d-125">**dimOf** 関数は、次の X++ プリミティブ型として宣言されている X++ 配列に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84a0d-125">The **dimOf** function is intended for X++ arrays that are declared as the following X++ primitive types:</span></span>

-   <span data-ttu-id="84a0d-126">ブール値</span><span class="sxs-lookup"><span data-stu-id="84a0d-126">boolean</span></span>
-   <span data-ttu-id="84a0d-127">日付</span><span class="sxs-lookup"><span data-stu-id="84a0d-127">date</span></span>
-   <span data-ttu-id="84a0d-128">int</span><span class="sxs-lookup"><span data-stu-id="84a0d-128">int</span></span>
-   <span data-ttu-id="84a0d-129">int64</span><span class="sxs-lookup"><span data-stu-id="84a0d-129">int64</span></span>
-   <span data-ttu-id="84a0d-130">real</span><span class="sxs-lookup"><span data-stu-id="84a0d-130">real</span></span>
-   <span data-ttu-id="84a0d-131">utcDateTime</span><span class="sxs-lookup"><span data-stu-id="84a0d-131">utcDateTime</span></span>

<span data-ttu-id="84a0d-132">たとえば **int iAmounts\[6\];** です。</span><span class="sxs-lookup"><span data-stu-id="84a0d-132">An example is **int iAmounts\[6\];**.</span></span> <span data-ttu-id="84a0d-133">列挙値および拡張データ型の配列も、前述のプリミティブ データ型のいずれかに最終的に基づいている場合はサポートされています (**int** など) 。</span><span class="sxs-lookup"><span data-stu-id="84a0d-133">Arrays of enumeration values and extended data types are also supported if they are ultimately based on one of the preceding primitive data types (such as **int**).</span></span> <span data-ttu-id="84a0d-134">**dimOf** 機能は、すべての X++ プリミティブ型の配列を受け入れるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="84a0d-134">The **dimOf** function doesn't accept arrays of all X++ primitive types.</span></span> <span data-ttu-id="84a0d-135">**dimOf** 関数が受け入れない配列タイプを次に示します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-135">Here are the array types that the **dimOf** function doesn't accept:</span></span>

-   <span data-ttu-id="84a0d-136">**str**</span><span class="sxs-lookup"><span data-stu-id="84a0d-136">**str**</span></span>
-   <span data-ttu-id="84a0d-137">**コンテナー**</span><span class="sxs-lookup"><span data-stu-id="84a0d-137">**container**</span></span>
-   <span data-ttu-id="84a0d-138">**anytype**</span><span class="sxs-lookup"><span data-stu-id="84a0d-138">**anytype**</span></span>
-   <span data-ttu-id="84a0d-139">クラス オブジェクトの配列</span><span class="sxs-lookup"><span data-stu-id="84a0d-139">Arrays of class objects</span></span>
-   <span data-ttu-id="84a0d-140">**配列**クラスのインスタンス</span><span class="sxs-lookup"><span data-stu-id="84a0d-140">Instances of the **Array** class</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-141">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-141">Example</span></span>

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

## <a name="fieldid2name"></a><span data-ttu-id="84a0d-142">fieldId2Name</span><span class="sxs-lookup"><span data-stu-id="84a0d-142">fieldId2Name</span></span>
<span data-ttu-id="84a0d-143">テーブルの ID 番号とフィールドの ID 番号で指定されているフィールドの名前を表す文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-143">Retrieves a string that represents the name of the field that is specified by a table ID number and a field ID number.</span></span>

    str fieldId2Name(int tableid, int fieldid)

### <a name="parameters"></a><span data-ttu-id="84a0d-144">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-144">Parameters</span></span>

| <span data-ttu-id="84a0d-145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-145">Parameter</span></span> | <span data-ttu-id="84a0d-146">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-146">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a0d-147">tableid</span><span class="sxs-lookup"><span data-stu-id="84a0d-147">tableid</span></span>   | <span data-ttu-id="84a0d-148">テーブルの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="84a0d-148">The ID number of the table.</span></span> <span data-ttu-id="84a0d-149">**注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-149">**Note:** Use the **tableName2Id** function to specify the ID of a table.</span></span> |
| <span data-ttu-id="84a0d-150">fieldid</span><span class="sxs-lookup"><span data-stu-id="84a0d-150">fieldid</span></span>   | <span data-ttu-id="84a0d-151">フィールドの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="84a0d-151">The ID number of the field.</span></span>                                                                           |

### <a name="return-value"></a><span data-ttu-id="84a0d-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-152">Return value</span></span>

<span data-ttu-id="84a0d-153">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-153">The name of the field.</span></span>

### <a name="remarks"></a><span data-ttu-id="84a0d-154">備考</span><span class="sxs-lookup"><span data-stu-id="84a0d-154">Remarks</span></span>

<span data-ttu-id="84a0d-155">フィールド名の印刷可能なバージョンを返すには、**fieldId2PName** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-155">To return a printable version of the field name, use the **fieldId2PName** function.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-156">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-156">Example</span></span>

<span data-ttu-id="84a0d-157">次の例では、フィールド ID が 7 の Customer (CustGroup) テーブルのフィールド名に **fn** を設定しています。</span><span class="sxs-lookup"><span data-stu-id="84a0d-157">The following example sets **fn** to the name of the field in the Customer (CustGroup) table that has a field ID of 7.</span></span>

    static void fieldId2NameExample(Args _arg)
    {
            str fn;
            fn = fieldId2Name(tableName2Id("Customer"),7);
    }

## <a name="fieldid2pname"></a><span data-ttu-id="84a0d-158">fieldId2PName</span><span class="sxs-lookup"><span data-stu-id="84a0d-158">fieldId2PName</span></span>
<span data-ttu-id="84a0d-159">テーブルの ID 番号とフィールドの ID 番号で指定されているフィールドの出力可能な名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-159">Retrieves the printable name of the field that is specified by a table ID number and a field ID number.</span></span>

    str fieldId2PName(int tableid, int fieldid)

### <a name="parameters"></a><span data-ttu-id="84a0d-160">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-160">Parameters</span></span>

| <span data-ttu-id="84a0d-161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-161">Parameter</span></span> | <span data-ttu-id="84a0d-162">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-162">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a0d-163">tableid</span><span class="sxs-lookup"><span data-stu-id="84a0d-163">tableid</span></span>   | <span data-ttu-id="84a0d-164">テーブルの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="84a0d-164">The ID number of the table.</span></span> <span data-ttu-id="84a0d-165">**注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-165">**Note:** Use the **tableName2Id** function to specify the ID of a table.</span></span> |
| <span data-ttu-id="84a0d-166">fieldid</span><span class="sxs-lookup"><span data-stu-id="84a0d-166">fieldid</span></span>   | <span data-ttu-id="84a0d-167">フィールドの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="84a0d-167">The ID number of the field.</span></span> <span data-ttu-id="84a0d-168">**注記:** フィールドの ID を指定するには、**fieldName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-168">**Note:** Use the **fieldName2Id** function to specify the ID of a field.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-169">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-169">Return value</span></span>

<span data-ttu-id="84a0d-170">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-170">The name of the field.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-171">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-171">Example</span></span>

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

## <a name="fieldname2id"></a><span data-ttu-id="84a0d-172">fieldName2Id</span><span class="sxs-lookup"><span data-stu-id="84a0d-172">fieldName2Id</span></span>
<span data-ttu-id="84a0d-173">テーブルの ID 番号とフィールドの ID 番号で指定されているテーブル フィールドのフィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-173">Retrieves the field ID of the table field that is specified by a table ID number and a field ID number.</span></span>

    int fieldName2Id(int tableid, str fieldname)

### <a name="parameters"></a><span data-ttu-id="84a0d-174">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-174">Parameters</span></span>

| <span data-ttu-id="84a0d-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-175">Parameter</span></span> | <span data-ttu-id="84a0d-176">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-176">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84a0d-177">tableid</span><span class="sxs-lookup"><span data-stu-id="84a0d-177">tableid</span></span>   | <span data-ttu-id="84a0d-178">テーブルの ID 番号。</span><span class="sxs-lookup"><span data-stu-id="84a0d-178">The ID number of the table.</span></span> <span data-ttu-id="84a0d-179">**注記:** テーブルの ID を指定するには、**tableName2Id** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-179">**Note:** Use the **tableName2Id** function to specify the ID of a table.</span></span> |
| <span data-ttu-id="84a0d-180">fieldname</span><span class="sxs-lookup"><span data-stu-id="84a0d-180">fieldname</span></span> | <span data-ttu-id="84a0d-181">フィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-181">The name of the field.</span></span>                                                                                |

### <a name="return-value"></a><span data-ttu-id="84a0d-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-182">Return value</span></span>

<span data-ttu-id="84a0d-183">*tableid* および *fieldname* パラメーターにより指定されているフィールドの ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-183">The ID of the field that is specified by the *tableid* and *fieldname* parameters.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-184">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-184">Example</span></span>

    static void fieldName2IdExample(Args _arg)
    {
            int id;

            id = fieldName2Id(tableName2Id("Address"), "Name");
            // Returns 6. Name is the 6th field in the Address table.
            print id;
    }

## <a name="indexid2name"></a><span data-ttu-id="84a0d-185">indexId2Name</span><span class="sxs-lookup"><span data-stu-id="84a0d-185">indexId2Name</span></span>
<span data-ttu-id="84a0d-186">インデックスの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-186">Retrieves the name of an index.</span></span>

    str indexId2Name(int tableid, int indexid)

### <a name="parameters"></a><span data-ttu-id="84a0d-187">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-187">Parameters</span></span>

| <span data-ttu-id="84a0d-188">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-188">Parameter</span></span> | <span data-ttu-id="84a0d-189">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-189">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="84a0d-190">tableid</span><span class="sxs-lookup"><span data-stu-id="84a0d-190">tableid</span></span>   | <span data-ttu-id="84a0d-191">インデックスが属するテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-191">The ID of the table that the index belongs to.</span></span> |
| <span data-ttu-id="84a0d-192">indexid</span><span class="sxs-lookup"><span data-stu-id="84a0d-192">indexid</span></span>   | <span data-ttu-id="84a0d-193">インデックスの ID です。</span><span class="sxs-lookup"><span data-stu-id="84a0d-193">The ID of the index.</span></span>                           |

### <a name="return-value"></a><span data-ttu-id="84a0d-194">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-194">Return value</span></span>

<span data-ttu-id="84a0d-195">インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-195">The name of the index.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-196">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-196">Example</span></span>

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

## <a name="indexname2id"></a><span data-ttu-id="84a0d-197">indexName2Id</span><span class="sxs-lookup"><span data-stu-id="84a0d-197">indexName2Id</span></span>
<span data-ttu-id="84a0d-198">インデックスの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-198">Retrieves the ID of an index.</span></span>

    int indexName2Id(int tableid, str indexname)

### <a name="parameters"></a><span data-ttu-id="84a0d-199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-199">Parameters</span></span>

| <span data-ttu-id="84a0d-200">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-200">Parameter</span></span> | <span data-ttu-id="84a0d-201">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-201">Description</span></span>                                    |
|-----------|------------------------------------------------|
| <span data-ttu-id="84a0d-202">tableid</span><span class="sxs-lookup"><span data-stu-id="84a0d-202">tableid</span></span>   | <span data-ttu-id="84a0d-203">インデックスが属するテーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-203">The ID of the table that the index belongs to.</span></span> |
| <span data-ttu-id="84a0d-204">indexname</span><span class="sxs-lookup"><span data-stu-id="84a0d-204">indexname</span></span> | <span data-ttu-id="84a0d-205">インデックスの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-205">The name of the index.</span></span>                         |

### <a name="return-value"></a><span data-ttu-id="84a0d-206">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-206">Return value</span></span>

<span data-ttu-id="84a0d-207">インデックスの ID です。</span><span class="sxs-lookup"><span data-stu-id="84a0d-207">The ID of the index.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-208">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-208">Example</span></span>

    static void indexName2IdExample(Args _arg)
    {
            indexid idx;
            tableid id;

            id  = tableName2Id("Address");
            idx = indexName2Id(id, "AddrIdx");
            print "Index ID for index name AddrIdx of table Address is " + int2Str(idx);
    }

## <a name="tableid2name"></a><span data-ttu-id="84a0d-209">tableId2Name</span><span class="sxs-lookup"><span data-stu-id="84a0d-209">tableId2Name</span></span>
<span data-ttu-id="84a0d-210">テーブルの名前を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-210">Retrieves a string that contains the name of a table.</span></span>

    str tableId2Name(int _tableid)

### <a name="parameters"></a><span data-ttu-id="84a0d-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-211">Parameters</span></span>

| <span data-ttu-id="84a0d-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-212">Parameter</span></span> | <span data-ttu-id="84a0d-213">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-213">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="84a0d-214">\_tableid</span><span class="sxs-lookup"><span data-stu-id="84a0d-214">\_tableid</span></span> | <span data-ttu-id="84a0d-215">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-215">The ID of the table.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-216">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-216">Return value</span></span>

<span data-ttu-id="84a0d-217">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-217">The name of the table.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-218">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-218">Example</span></span>

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

## <a name="tableid2pname"></a><span data-ttu-id="84a0d-219">tableId2PName</span><span class="sxs-lookup"><span data-stu-id="84a0d-219">tableId2PName</span></span>
<span data-ttu-id="84a0d-220">テーブルの出力可能な名前 (ラベル) を含む文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-220">Retrieves a string that contains the printable name (the label) of a table.</span></span>

    str tableId2PName(int _fieldid)

### <a name="parameters"></a><span data-ttu-id="84a0d-221">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-221">Parameters</span></span>

| <span data-ttu-id="84a0d-222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-222">Parameter</span></span> | <span data-ttu-id="84a0d-223">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-223">Description</span></span>          |
|-----------|----------------------|
| <span data-ttu-id="84a0d-224">\_fieldid</span><span class="sxs-lookup"><span data-stu-id="84a0d-224">\_fieldid</span></span> | <span data-ttu-id="84a0d-225">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-225">The ID of the table.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-226">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-226">Return value</span></span>

<span data-ttu-id="84a0d-227">テーブルのラベル。</span><span class="sxs-lookup"><span data-stu-id="84a0d-227">The label of the table.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-228">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-228">Example</span></span>

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

## <a name="tablename2id"></a><span data-ttu-id="84a0d-229">tableName2Id</span><span class="sxs-lookup"><span data-stu-id="84a0d-229">tableName2Id</span></span>
<span data-ttu-id="84a0d-230">テーブルの ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-230">Retrieves the ID of a table.</span></span>

    int tableName2Id(str _name)

### <a name="parameters"></a><span data-ttu-id="84a0d-231">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-231">Parameters</span></span>

| <span data-ttu-id="84a0d-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-232">Parameter</span></span> | <span data-ttu-id="84a0d-233">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-233">Description</span></span>            |
|-----------|------------------------|
| <span data-ttu-id="84a0d-234">\_名前</span><span class="sxs-lookup"><span data-stu-id="84a0d-234">\_name</span></span>    | <span data-ttu-id="84a0d-235">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="84a0d-235">The name of the table.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-236">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-236">Return value</span></span>

<span data-ttu-id="84a0d-237">テーブルの ID。</span><span class="sxs-lookup"><span data-stu-id="84a0d-237">The ID of the table.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-238">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-238">Example</span></span>

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

## <a name="typeof"></a><span data-ttu-id="84a0d-239">typeOf</span><span class="sxs-lookup"><span data-stu-id="84a0d-239">typeOf</span></span>
<span data-ttu-id="84a0d-240">要素のタイプを取得します。</span><span class="sxs-lookup"><span data-stu-id="84a0d-240">Retrieves the type of an element.</span></span>

    enum typeOf(anytype _object)

### <a name="parameters"></a><span data-ttu-id="84a0d-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-241">Parameters</span></span>

| <span data-ttu-id="84a0d-242">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84a0d-242">Parameter</span></span> | <span data-ttu-id="84a0d-243">説明</span><span class="sxs-lookup"><span data-stu-id="84a0d-243">Description</span></span>                         |
|-----------|-------------------------------------|
| <span data-ttu-id="84a0d-244">\_オブジェクト</span><span class="sxs-lookup"><span data-stu-id="84a0d-244">\_object</span></span>  | <span data-ttu-id="84a0d-245">タイプを返す対象の要素。</span><span class="sxs-lookup"><span data-stu-id="84a0d-245">The element to return the type for.</span></span> |

### <a name="return-value"></a><span data-ttu-id="84a0d-246">戻り値</span><span class="sxs-lookup"><span data-stu-id="84a0d-246">Return value</span></span>

<span data-ttu-id="84a0d-247">**タイプ**システム列挙値。</span><span class="sxs-lookup"><span data-stu-id="84a0d-247">A **Types** system enumeration value.</span></span>

### <a name="example"></a><span data-ttu-id="84a0d-248">例</span><span class="sxs-lookup"><span data-stu-id="84a0d-248">Example</span></span>

<span data-ttu-id="84a0d-249">次の例では、コンテナ内の最初の要素、**c** が単一の整数を含む別のコンテナーであるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="84a0d-249">The following example tests whether the first element in a container, **c**, is another container that contains a single integer.</span></span>

    if(typeof(conpeek(c, 1)) != Types::Container ||
    conlen(conpeek(c, 1)) != 1 ||
    typeof(conpeek(conpeek(c, 1), 1)) != Types::Integer)
    {
            // More code.
    }



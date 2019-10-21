---
title: X++ プリミティブ データ型
description: このトピックでは、X++のプリミティブ データ型について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150183
ms.assetid: 0ff4e759-851d-4b53-aa67-6f03eee53f02
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a12e14ebb7627a3cce29b8f68353ed6d5424af55
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550148"
---
# <a name="x-primitive-data-types"></a><span data-ttu-id="cf872-103">X++ プリミティブ データ型</span><span class="sxs-lookup"><span data-stu-id="cf872-103">X++ Primitive data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf872-104">このトピックでは、X++のプリミティブ データ型について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf872-104">This topic describes primitive data types in X++.</span></span> <span data-ttu-id="cf872-105">X++ のプリミティブ データ型は、**anytype**、**boolean**、**date**、**enum**、**guid**、**int**、**int64**、**real**、**str**、**timeOfDay**、および **utcdatetime** です。</span><span class="sxs-lookup"><span data-stu-id="cf872-105">The primitive data types in X++ are **anytype**, **boolean**, **date**, **enum**, **guid**, **int**, **int64**, **real**, **str**, **timeOfDay**, and **utcdatetime**.</span></span>

## <a name="anytype"></a><span data-ttu-id="cf872-106">anytype</span><span class="sxs-lookup"><span data-stu-id="cf872-106">anytype</span></span>

<span data-ttu-id="cf872-107">**anytype** データ型は任意のデータ型のプレースホルダーです。</span><span class="sxs-lookup"><span data-stu-id="cf872-107">The **anytype** data type is a placeholder for any data type.</span></span> <span data-ttu-id="cf872-108">このタイプの変数は、引数および戻り値としてのみ使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-108">You should use variables of this type only as arguments and return values.</span></span> <span data-ttu-id="cf872-109">**anytype** を変数として使用するには、最初に変数に値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-109">To use **anytype** as a variable, you must first assign a value to it.</span></span> <span data-ttu-id="cf872-110">それ以外の場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="cf872-110">Otherwise, a run-time error occurs.</span></span> <span data-ttu-id="cf872-111">**anytype** 値に割り当てた後、別のデータ型に変換することはできません。</span><span class="sxs-lookup"><span data-stu-id="cf872-111">After you've assigned a value to **anytype**, you can't convert it to another data type.</span></span> <span data-ttu-id="cf872-112">式に **anytype** の変数を使用できますが、通常は引数および戻り値の型として使用されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-112">Although you can use **anytype** variables in expressions, they're usually used as arguments and return types.</span></span> <span data-ttu-id="cf872-113">サイズ、精度、有効範囲、既定値、**anytype** の範囲は、割り当てた変換タイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="cf872-113">The size, precision, scope, default value, and range of **anytype** depend on the conversion type that you assign to it.</span></span> <span data-ttu-id="cf872-114">変換対象のデータ タイプを使用するように、**anytype** を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-114">You can use **anytype** just as you use the data type that you convert it to.</span></span> <span data-ttu-id="cf872-115">たとえば、整数を割り当てる場合、変数にリレーショナル演算子と算術演算子を適用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-115">For example, if you assign an integer, you can then apply relational and arithmetic operators to the variable.</span></span> <span data-ttu-id="cf872-116">**anytype** 変数は値をタイプに割り当てるとき、日付、列挙 (enum)、整数、実数、文字列、拡張データ型 (EDT) (レコード)、クラス、またはコンテナーを自動的に変換します。</span><span class="sxs-lookup"><span data-stu-id="cf872-116">An **anytype** variable is automatically converted to a date, enumeration (enum), integer, real, string, extended data type (EDT) (record), class, or container when a value is assigned to the type.</span></span> <span data-ttu-id="cf872-117">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **any2date**、**any2enum**、**any2int**、**any2real**、**any2str**。</span><span class="sxs-lookup"><span data-stu-id="cf872-117">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **any2date**, **any2enum**, **any2int**, **any2real**, and **any2str**.</span></span> <span data-ttu-id="cf872-118">**anytype** に変換した後は、変数を別のデータ型に変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="cf872-118">You can't change the variable to another data type after you've converted it to **anytype**.</span></span>

### <a name="anytype-examples"></a><span data-ttu-id="cf872-119">anytype 例</span><span class="sxs-lookup"><span data-stu-id="cf872-119">anytype examples</span></span>

    // An example of using anytype variables.
    public static str range(anytype _from, anytype _to)
    {
        return queryValue(_from) + '..' + queryValue(_to);
    }

    // Another example of using anytype variables.
    void put(int position, anytype data)
    {
        record = conPoke (record, position, data);
    }

    public void AnytypeMethod()
    {
        // An example of automatic conversion for anytype.
        anytype a;
        a = "text"; // Automatically assigns a string literal.
    }

## <a name="boolean"></a><span data-ttu-id="cf872-120">ブール値</span><span class="sxs-lookup"><span data-stu-id="cf872-120">boolean</span></span>

<span data-ttu-id="cf872-121">**ブール** データ型には、**true** または **false** のいずれかとして評価される値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf872-121">The **boolean** data type contains a value that is evaluated as either **true** or **false**.</span></span> <span data-ttu-id="cf872-122">**ブール** 式が予期される場所では、引当済のリテラル キーワード **true** および **false** を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-122">You can use the reserved literal keywords **true** and **false** wherever a **boolean** expression is expected.</span></span> <span data-ttu-id="cf872-123">**boolean** のサイズは 1 byte です。</span><span class="sxs-lookup"><span data-stu-id="cf872-123">The size of a **boolean** is 1 byte.</span></span> <span data-ttu-id="cf872-124">既定値は、**false** で、内部表示は、短い番号です。</span><span class="sxs-lookup"><span data-stu-id="cf872-124">The default value is **false**, and the internal representation is a short number.</span></span> <span data-ttu-id="cf872-125">**ブール**は、自動的に **int**、**date**、または **real** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-125">A **boolean** is automatically converted to an **int**, **date**, or **real**.</span></span> <span data-ttu-id="cf872-126">明示的な変換関数はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-126">It has no explicit conversion functions.</span></span> <span data-ttu-id="cf872-127">**ブール** の内部テーブル現は整数です。</span><span class="sxs-lookup"><span data-stu-id="cf872-127">The internal representation of a **boolean** is an integer.</span></span> <span data-ttu-id="cf872-128">**ブール値** タイプとして宣言された変数には任意の整数値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-128">You can assign any integer value to a variable that is declared as the **boolean** type.</span></span> <span data-ttu-id="cf872-129">整数値 **0** (ゼロ) は **false** と評価され、他のすべての整数値は **true** と評価されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-129">The integer value **0** (zero) is evaluated as **false**, and all other integer values are evaluated as **true**.</span></span> <span data-ttu-id="cf872-130">**ブール**の内部表示は整数なので、**ブール**値は自動的に整数と実数に変換されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-130">Because the internal representation of a **boolean** is an integer, **boolean** values are automatically converted to integers and reals.</span></span>

### <a name="boolean-examples"></a><span data-ttu-id="cf872-131">ブール値の例</span><span class="sxs-lookup"><span data-stu-id="cf872-131">boolean examples</span></span>

    public void BooleanMethod()
    {
        // Simple declaration of a boolean variable, b.
        boolean b;

        // Multiple declarations of booleans.
        boolean b1, b2;

        // Boolean variable is initialized to true.
        boolean b3 = true;

        // Declares a dynamic array of booleans.
        boolean b4[];

        // This example shows the most common usage of a boolean: a boolean in
        // a conditional statement and as a result of a logical expression.
        void main()
        {
            // Declares a boolean called exprValue.
            boolean exprValue;

            // Assigns ExprValue the value of (7*6 == 42), which equates to true.
            exprValue = (7*6 == 42);

            // If the conditional statement is true, print "OK".
            if (exprValue)
            {
                print "OK";  //"OK" is printed because the expression is true.
            }
        }
    }

## <a name="date"></a><span data-ttu-id="cf872-132">日付</span><span class="sxs-lookup"><span data-stu-id="cf872-132">date</span></span>

<span data-ttu-id="cf872-133">**date** データ型は、年、月、日を格納します。</span><span class="sxs-lookup"><span data-stu-id="cf872-133">The **date** data type contains the day, month, and year.</span></span> <span data-ttu-id="cf872-134">日付は、次の構文を使用してリテラルとして記述できます。**日付リテラル = 日 \\ 月 \\ 年**。</span><span class="sxs-lookup"><span data-stu-id="cf872-134">Dates can be written as literals by using the following syntax: **Date literal = day \\ month \\ year**.</span></span> <span data-ttu-id="cf872-135">その年の 4 桁の数字を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-135">You must use four digits for the year.</span></span> <span data-ttu-id="cf872-136">**日付**データ型は、1900 年 1 月 1 日～ 2154 年 12 月 31 日の日付を保持できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-136">The **date** data type can hold dates between January 1, 1900, and December 31, 2154.</span></span> <span data-ttu-id="cf872-137">**date** のサイズは 32 ビットです。</span><span class="sxs-lookup"><span data-stu-id="cf872-137">The size of a **date** is 32 bits.</span></span> <span data-ttu-id="cf872-138">既定値は、**null** で、内部表示は、日付です。</span><span class="sxs-lookup"><span data-stu-id="cf872-138">The default value is **null**, and the internal representation is a date.</span></span> <span data-ttu-id="cf872-139">**日付**に暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-139">A **date** has no implicit conversions.</span></span> <span data-ttu-id="cf872-140">ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2date**、 **date2str**、 **date2num**、 **int2date**。</span><span class="sxs-lookup"><span data-stu-id="cf872-140">However, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2date**, **date2str**, **date2num**, and **int2date**.</span></span> <span data-ttu-id="cf872-141">日付に対し、整数を加算または減算することができます。これにより将来の日付または、過去の日付に移動します。</span><span class="sxs-lookup"><span data-stu-id="cf872-141">You can add and subtract integers from dates, which moves the date some days into the future and past respectively.</span></span> <span data-ttu-id="cf872-142">それぞれの日付を減算することにより、差異が日数で計算されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-142">Subtracting dates from each other will calculate the difference in days.</span></span> <span data-ttu-id="cf872-143">ただし、2つの日付を一緒に加算することはできず、コンパイラ エラーの原因になります。</span><span class="sxs-lookup"><span data-stu-id="cf872-143">However, adding two dates together is not possible and will lead to a compiler error.</span></span>

### <a name="date-examples"></a><span data-ttu-id="cf872-144">date の例</span><span class="sxs-lookup"><span data-stu-id="cf872-144">date examples</span></span>

    public void DateMethod()
    {
        // Simple declaration of a date variable, d.
       date d;

        // Multiple declaration of two date variables.
        date d1, d2;

        // A date variable, d3, is initialized to the 21st of November 1998.
        date d3 = 21\11\1998;

        // Declaration of a dynamic array of dates.
        date d4[];

        // Using arithmetic operators with integer variables and dates.
        void myMethod()
        {
            int anInteger;
            date aDate;
            // Sets the date variable aDate to January 1, 1998.
            aDate = 1\1\1998;
            // Sets the integer variable anInteger to 30.
            anInteger = 30;
            // Uses an integer value in the computation of dates.
            // This sets aDate to aDate + 30; that is the 31st of January 1998.
            aDate = aDate + anInteger;

            // Create 2 variables, set bDate, and then subtract from that date.
            date bDate;
            int dateDifference;
            bDate = 2\10\1998; 
            dateDifference = bDate - aDate; // dateDifference will equal 244.
        }
    }

## <a name="enum"></a><span data-ttu-id="cf872-145">列挙型</span><span class="sxs-lookup"><span data-stu-id="cf872-145">enum</span></span>

<span data-ttu-id="cf872-146">**列挙**はリテラルのリストです。</span><span class="sxs-lookup"><span data-stu-id="cf872-146">An **enum** is a list of literals.</span></span> <span data-ttu-id="cf872-147">**列挙**を使用する前に、アプリケーション エクスプローラーで宣言する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-147">Before you can use an **enum**, you must declare it in Application Explorer.</span></span> <span data-ttu-id="cf872-148">リテラルの値は、内部的に整数で表されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-148">The literal values are represented internally as integers.</span></span> <span data-ttu-id="cf872-149">最初のリテラルは数字 0、次のリテラルは 1、次のリテラルは 2 というように続きます。</span><span class="sxs-lookup"><span data-stu-id="cf872-149">The first literal has the number 0, the next literal has the number 1, the next literal has the number 2, and so on.</span></span> <span data-ttu-id="cf872-150">式の中では **列挙型** の値を整数として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-150">You can use **enum** values as integers in expressions.</span></span> <span data-ttu-id="cf872-151">最初のエントリの既定値は、**0** で、内部表示は、短い番号です。</span><span class="sxs-lookup"><span data-stu-id="cf872-151">The default value for the first entry is **0**, and the internal representation is a short number.</span></span> <span data-ttu-id="cf872-152">**列挙**値は自動的に**ブール**、**int**、または **real** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-152">An **enum** value is automatically converted to a **boolean**, **int**, or **real**.</span></span> <span data-ttu-id="cf872-153">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **enum2str** および **str2enum**。</span><span class="sxs-lookup"><span data-stu-id="cf872-153">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **enum2str** and **str2enum**.</span></span> <span data-ttu-id="cf872-154">百種類の列挙型が標準アプリケーションに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="cf872-154">Hundreds of enumerable types are built into the standard application.</span></span> <span data-ttu-id="cf872-155">たとえば、**NoYes** 列挙には関連付けられている 2 つのリテラルがあります: **No** は **0** の値を、および**Yes**は **1** の値です。</span><span class="sxs-lookup"><span data-stu-id="cf872-155">For example, the **NoYes** enum has two associated literals: **No** has the value **0**, and **Yes** has the value **1**.</span></span> <span data-ttu-id="cf872-156">必要なだけ列挙型を作成して、最大で 251 (0 ~ 250) のリテラルを単一列挙型で宣言することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-156">You can create as many enum types as you want, and you can declare up to 251 (0 to 250) literals in a single enum type.</span></span> <span data-ttu-id="cf872-157">**列挙型**の値を参照するには、列挙型の名前、2 つのコロン、およびリテラルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf872-157">To reference an **enum** value, enter the name of the enum, two colons, and then the name of the literal.</span></span> <span data-ttu-id="cf872-158">たとえば、**NoYes** 列挙でリテラルの **No** を使用するには、**NoYes::No** を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf872-158">For example, to use the literal **No** in the **NoYes** enum, enter **NoYes::No**.</span></span>

### <a name="create-an-enum"></a><span data-ttu-id="cf872-159">列挙型を作成する</span><span class="sxs-lookup"><span data-stu-id="cf872-159">Create an enum</span></span>

1.  <span data-ttu-id="cf872-160">ソリューション エクスプローラーで、プロジェクトを右クリックして**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf872-160">In Solution Explorer, right-click the project, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="cf872-161">**アーティファクト** で、**データ型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf872-161">Under **Artifacts**, select **Data Types**.</span></span>
3.  <span data-ttu-id="cf872-162">**基本列挙**をクリックし、を新しい項目の種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf872-162">Click **Base Enum** to select the new item type.</span></span>
4.  <span data-ttu-id="cf872-163">**名前**フィールドに、列挙型の名前を入力してから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf872-163">In the **Name** field, enter a name for the enum, and then click **Add**.</span></span> <span data-ttu-id="cf872-164">新しい列挙型がプロジェクトに追加され、新しい要素の列挙型デザイナーが開きます。</span><span class="sxs-lookup"><span data-stu-id="cf872-164">A new enum is added to the project, and the enum designer for the new element is opened.</span></span>
5.  <span data-ttu-id="cf872-165">列挙型デザイナーで、列挙名を右クリックしてから**新しい要素**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cf872-165">In the enum designer, right-click the enum name, and then click **New Element**.</span></span>
6.  <span data-ttu-id="cf872-166">**プロパティ** ウィンドウで、列挙要素の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf872-166">In the **Properties** window, enter the name of the enum element.</span></span>

### <a name="enum-examples"></a><span data-ttu-id="cf872-167">列挙型の例</span><span class="sxs-lookup"><span data-stu-id="cf872-167">enum examples</span></span>

    public void EnumMethod()
    {
        // Declare the enum (a NoYes enum) in the Application Explorer.
        NoYes done;

        // An array of Criteria enums.
        Criteria crit[100];
    }

## <a name="guid"></a><span data-ttu-id="cf872-168">guid</span><span class="sxs-lookup"><span data-stu-id="cf872-168">guid</span></span>

<span data-ttu-id="cf872-169">**guid** データ型は、*グローバルに一意の識別子* (GUID) 値を保持します。</span><span class="sxs-lookup"><span data-stu-id="cf872-169">The **guid** data type holds a *globally unique identifier* (GUID) value.</span></span> <span data-ttu-id="cf872-170">GUID は、固有の識別子が必要な場合に、すべてのコンピューターとネットワークで使用できる整数です。</span><span class="sxs-lookup"><span data-stu-id="cf872-170">A GUID is an integer that can be used across all computers and networks, wherever a unique identifier is required.</span></span> <span data-ttu-id="cf872-171">数字が重複することはあまりありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-171">It's unlikely that the number will be duplicated.</span></span> <span data-ttu-id="cf872-172">有効な GUID は、次のすべての仕様を満たします。</span><span class="sxs-lookup"><span data-stu-id="cf872-172">A valid GUID meets all the following specifications:</span></span>

-   <span data-ttu-id="cf872-173">32 桁の 16 進数が必要です。</span><span class="sxs-lookup"><span data-stu-id="cf872-173">It must have 32 hexadecimal digits.</span></span>
-   <span data-ttu-id="cf872-174">次の場所では埋め込まれるダッシュ文字が 4 つ必要です: 8-4-4-4-12。</span><span class="sxs-lookup"><span data-stu-id="cf872-174">It must have four dash characters that are embedded at the following locations: 8-4-4-4-12.</span></span>
-   <span data-ttu-id="cf872-175">文字列の先頭と末尾の中かっこ ({}) はオプションです。</span><span class="sxs-lookup"><span data-stu-id="cf872-175">Braces ({}) at the beginning and end of a string are optional.</span></span> <span data-ttu-id="cf872-176">たとえば、「12345678-BBBb-cCCCC-0000-123456789012」および「{12345678-BBBb-cCCCC-0000-123456789012}」両方共有効な GUID 文字列です。</span><span class="sxs-lookup"><span data-stu-id="cf872-176">For example, both "12345678-BBBb-cCCCC-0000-123456789012" and "{12345678-BBBb-cCCCC-0000-123456789012}" are valid GUID strings.</span></span>
-   <span data-ttu-id="cf872-177">かっこを追加するかどうかに応じて、合計 36 文字または 38 文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-177">It must have a total of either 36 or 38 characters, depending on whether braces are added.</span></span>
-   <span data-ttu-id="cf872-178">a 〜 f (または A 〜 F) の 16 進数は、大文字、小文字、または混在することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-178">The hexadecimal digits a–f (or A–F) can be uppercase, lowercase, or mixed.</span></span>

<span data-ttu-id="cf872-179">**guid** のサイズは 16 byte または 128 ビットです。</span><span class="sxs-lookup"><span data-stu-id="cf872-179">The size of a **guid** is 16 bytes or 128 bits.</span></span> <span data-ttu-id="cf872-180">次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**any2guid**、**guid2str**、**newGuid**、**str2guid**、**Global::guidFromString**、および **Global::stringFromGuid** も使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-180">The following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **any2guid**, **guid2str**, **newGuid**, **str2guid**, **Global::guidFromString**, and **Global::stringFromGuid**.</span></span>

### <a name="guid-examples"></a><span data-ttu-id="cf872-181">guid の例</span><span class="sxs-lookup"><span data-stu-id="cf872-181">guid examples</span></span>

<span data-ttu-id="cf872-182">次の例は、**guid** 関数の使い方を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf872-182">The following set of examples shows how to use the **guid** functions.</span></span> <span data-ttu-id="cf872-183">これらの例のコード出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cf872-183">The code output of these examples follows.</span></span>

    // An example of how to use the GUID functions.
    static void GuidRoundTripJob(Args _args)
    {
        guid guid2;
        str string3;

        // Convert a guid to a string, and back to a guid.
        guid2 = newGuid();
        info(strFmt("Info_a1:  guid2 == %1", guid2));
        string3 = guid2str(guid2);
        info(strFmt("Info_a2:  string3 == %1", string3));
        guid2 = str2guid(string3);
        info(strFmt("Info_a3:  guid2 == %1", guid2));

        // Test string representations of a guid. Mixing upper and lower case letters does not affect the guid.
        guid2 = str2guid("BB345678-abcd-ABCD-0000-bbbbffff9012");
        string3 = guid2str(guid2);
        info(strFmt("Info_b1:  8-4-4-4-12 format for dashes works (%1)", string3));
        info(strFmt("Info_b2:  Mixed upper and lower case works."));

        // Test invalid dash locations, see output is all zeros. Dash locations must be exact.
        guid2 = str2guid("CC2345678abcd-ABCD-0000-cccc9012");
        string3 = guid2str(guid2);
        info(strFmt("Info_c1:  These embedded dash locations are required.  %1", string3));

        // Braces {} are optional.
        guid2 = str2guid("{DD345678-abcd-ABCD-0000-ddddaaaa9012}");
        string3 = guid2str(guid2);
        info(strFmt("Info_d1:  Braces {} are optional (%1)", string3));
    }

### <a name="guid-code-output"></a><span data-ttu-id="cf872-184">guid コード出力</span><span class="sxs-lookup"><span data-stu-id="cf872-184">guid code output</span></span>

<span data-ttu-id="cf872-185">次の出力は、情報ログに表示されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-185">The following output appears in the Infolog.</span></span> <span data-ttu-id="cf872-186">文字列にはオプションの中かっこが含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cf872-186">Note that the string includes the optional braces.</span></span>

    Message (02:26:46 pm)
    Info_a1:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a2:  string3 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_a3:  guid2 == {93945629-734B-475E-99CE-6AA7AFA43259}
    Info_b1:  8-4-4-4-12 format for dashes works ({BB345678-ABCD-ABCD-0000-BBBBFFFF9012})
    Info_b2:  Mixed upper and lower case works.
    Info_c1:  These embedded dash locations are required.  {00000000-0000-0000-0000-000000000000}
    Info_d1:  Braces {} are optional ({DD345678-ABCD-ABCD-0000-DDDDAAAA9012})

## <a name="int-and-int64"></a><span data-ttu-id="cf872-187">int および int64</span><span class="sxs-lookup"><span data-stu-id="cf872-187">int and int64</span></span>

<span data-ttu-id="cf872-188">*整数*は小数点以下の桁数のない数字です。</span><span class="sxs-lookup"><span data-stu-id="cf872-188">*Integers* are numbers that have no decimal places.</span></span> <span data-ttu-id="cf872-189">**int** および **int64** の、2 つの整数タイプがあります。</span><span class="sxs-lookup"><span data-stu-id="cf872-189">There are two integer types: **int** and **int64**.</span></span> <span data-ttu-id="cf872-190">整数は、繰り返しのステートメントの制御変数または配列のインデックスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-190">Integers are used as control variables in repetitive statements or as indexes in arrays.</span></span> <span data-ttu-id="cf872-191">また、整数式が必要で、リレーショナル演算子と算術演算子の両方を適用することができる任意の場所で *整数リテラル* を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-191">You can also use *integer literals* anywhere that an integer expression is expected, and both relational and arithmetic operators can be applied.</span></span> <span data-ttu-id="cf872-192">整数リテラルは **32768** のように、コードに直接入力された整数。</span><span class="sxs-lookup"><span data-stu-id="cf872-192">An integer literal is the integer as it's entered directly in the code, such as **32768**.</span></span> <span data-ttu-id="cf872-193">**Int** は 32 ビット幅で、**int64** は 64 ビット幅です。</span><span class="sxs-lookup"><span data-stu-id="cf872-193">An **int** is 32 bits wide, and an **int64** is 64 bits wide.</span></span> <span data-ttu-id="cf872-194">既定値は、**0** で、内部表示は、長い番号です。</span><span class="sxs-lookup"><span data-stu-id="cf872-194">The default value is **0**, and the internal representation is a long number.</span></span> <span data-ttu-id="cf872-195">整数は自動的に **boolean**、**enum** または **real** に変換されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-195">An integer is automatically converted to a **boolean**, **enum**, or **real**.</span></span> <span data-ttu-id="cf872-196">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2int**、**int2str**、**str2int64**、**int642str**。</span><span class="sxs-lookup"><span data-stu-id="cf872-196">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2int**, **int2str**, **str2int64**, and **int642str**.</span></span> <span data-ttu-id="cf872-197">**int** の範囲は \[-2,147,483,647 : 2,147,483,647\]、**int64** の範囲は \[-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808\] です。</span><span class="sxs-lookup"><span data-stu-id="cf872-197">The range of an **int** is \[-2,147,483,647 : 2,147,483,647\], and the range of an **int64** is \[-9,223,372,036,854,775,808 : 9,223,372,036,854,775,808\].</span></span> <span data-ttu-id="cf872-198">全整数はこれらの範囲のいずれかでリテラルとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-198">All integers in either of these ranges can be used as literals.</span></span>

### <a name="int-and-int64-examples"></a><span data-ttu-id="cf872-199">int および int64 の例</span><span class="sxs-lookup"><span data-stu-id="cf872-199">int and int64 examples</span></span>

<span data-ttu-id="cf872-200">次の例は、整数を宣言して式で使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf872-200">The following example shows how to declare integers and use them in expressions.</span></span> <span data-ttu-id="cf872-201">**int64** に最大整数プラス 1 を代入しようとすると、数値は 32 ビット数として解釈されるため、間違った結果になります。</span><span class="sxs-lookup"><span data-stu-id="cf872-201">If you try to assign the largest integer plus 1 to an **int64**, you get the wrong result, because the number is interpreted as a 32-bit number.</span></span> <span data-ttu-id="cf872-202">したがって、番号は折り返され、代わりに -2,147,483,647 として格納されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-202">Therefore, the number is wrapped around and stored as -2,147,483,647 instead.</span></span> <span data-ttu-id="cf872-203">この問題を防ぐためには、番号の最後に "u" を追加します。</span><span class="sxs-lookup"><span data-stu-id="cf872-203">To prevent this behavior, add "u" to the end of the number.</span></span> <span data-ttu-id="cf872-204">たとえば、**int64 I = 0x8000 0000u** (0x8000 0000 は 2,147,483,648 です) を入力します。</span><span class="sxs-lookup"><span data-stu-id="cf872-204">For example, enter **int64 i = 0x8000 0000u** (0x8000 0000 is 2,147,483,648).</span></span>

    public void IntegerMethod()
    {
        // Declaration of an integer variable, i.
        int i;

        // Declaration of two int64 variables.
        int64 i1, i2;

        // An integer variable is initialized to the value 100.
        int i3 = 100;

        // Declaration of a dynamic array of integers.
        int i4[];
        void element()
        {
            // Two integer variables are declared and initialized.
            int k = 1, j = 2;

            // j is assigned the result of j + ((i + i) DIV 2).
            j +=(i + i) div 2;

            // This results in: j=3.

            if (j > 2 )
            {
                print "J is greater than 2";
            }
            else
            {
                print "J is NOT greater than 2";
            }
        }
    }

## <a name="real"></a><span data-ttu-id="cf872-205">real</span><span class="sxs-lookup"><span data-stu-id="cf872-205">real</span></span>

<span data-ttu-id="cf872-206">**実数**変数は、整数に加えて小数値を保持できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-206">A **real** variable can hold decimal values in addition to integers.</span></span> <span data-ttu-id="cf872-207">*10 進リテラル* は **実数** が予期される場所ではどこでも使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-207">You can use *decimal literals* anywhere that a **real** is expected.</span></span> <span data-ttu-id="cf872-208">10 進数リテラルは、**2.123876** のように、コードで直接入力された 10 進数です。</span><span class="sxs-lookup"><span data-stu-id="cf872-208">A decimal literal is the decimal as it's entered directly in the code, such as **2.123876**.</span></span> <span data-ttu-id="cf872-209">実数リテラルは、**1.0e3** などの指数の表記を使用して記述することもできます。</span><span class="sxs-lookup"><span data-stu-id="cf872-209">Real literals can also be written by using exponential notation, such as **1.0e3**.</span></span> <span data-ttu-id="cf872-210">Reals は、すべての式で使用することができ、リレーショナル演算子と算術演算子の両方と共に使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-210">Reals can be used in all expressions, and they can be used with both relational and arithmetic operators.</span></span> <span data-ttu-id="cf872-211">**実数**は、16桁の有効な数値の精度があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-211">A **real** has a precision of 16 significant digits.</span></span> <span data-ttu-id="cf872-212">**real** の既定値は **0.0** で、内部表示はバイナリコード化されたデジタル (BCD) 番号です。</span><span class="sxs-lookup"><span data-stu-id="cf872-212">The default value for a **real** is **0.0**, and the internal representation is a binary-coded digital (BCD) number.</span></span> <span data-ttu-id="cf872-213">BCD エンコードにより、0.1 の倍数の値の正確な表現が可能になります。</span><span class="sxs-lookup"><span data-stu-id="cf872-213">The BCD encoding enables exact representations of values that are multiples of 0.1.</span></span> <span data-ttu-id="cf872-214">**実数** 変数の範囲は、-(10)¹²⁷ から (10)¹²⁷ です。</span><span class="sxs-lookup"><span data-stu-id="cf872-214">The range of a **real** variable is -(10)¹²⁷ through (10)¹²⁷.</span></span> <span data-ttu-id="cf872-215">この範囲内のすべての実数は X++ でリテラルとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-215">All reals in this range can be used as literals in X++.</span></span> <span data-ttu-id="cf872-216">**実数**変数は、自動的に**ブール**、**enum**、または **int** に変換されます。結果が整数の場合、または演算子が整数演算子の場合には、**実数**は整数に変換されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-216">A **real** variable is automatically converted to a **boolean**, **enum**, or **int**. If the result is an integer, or if the operator is an integer operator, the **real** is converted to an integer.</span></span> <span data-ttu-id="cf872-217">結果が**ブール値**である場合、**実数**が**ブール値**に変換されたりします。</span><span class="sxs-lookup"><span data-stu-id="cf872-217">If the result is a **boolean**, the **real** is converted to a **boolean**, and so on.</span></span> <span data-ttu-id="cf872-218">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2num**、**num2str**。</span><span class="sxs-lookup"><span data-stu-id="cf872-218">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2num** and **num2str**.</span></span> <span data-ttu-id="cf872-219">X++ **実数** と Microsoft .NET Framework **System.Decimal** 間の直接割り当てによって、値が正しく変換されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-219">Direct assignments between X++ **real** and Microsoft .NET Framework **System.Decimal** convert the value correctly.</span></span> <span data-ttu-id="cf872-220">換算関数を呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-220">A call to a conversion function isn't required.</span></span> <span data-ttu-id="cf872-221">*10 進数*は、符号、0 から 9 の範囲内の数値、および数値の整数と小数点以下を区切る浮動小数点の位置を表すスケーリング係数で構成される浮動小数点値です。</span><span class="sxs-lookup"><span data-stu-id="cf872-221">A *decimal number* is a floating-point value that consists of a sign, a numeric value where each digit is in the range 0 through 9, and a scaling factor that indicates the position of a floating decimal point that separates the integral and fractional parts of the numeric value.</span></span> <span data-ttu-id="cf872-222">**実数**値のバイナリ表現は、1 ビットの符号、96ビットの整数、スケーリング係数で構成されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-222">The binary representation of a **real** value consists of a 1-bit sign, a 96-bit integer number, and a scaling factor.</span></span> <span data-ttu-id="cf872-223">拡大縮小係数は、96 ビット整数を分割し、小数部の部分を指定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-223">The scaling factor is used to divide the 96-bit integer and specify what part of it is a decimal fraction.</span></span> <span data-ttu-id="cf872-224">拡大縮小係数は、0 から 28 の範囲の指数に暗黙的に 10 を引いたものです。</span><span class="sxs-lookup"><span data-stu-id="cf872-224">The scaling factor is implicitly the number 10 raised to an exponent in the range 0 through 28.</span></span> <span data-ttu-id="cf872-225">したがって、10 進数のバイナリ表現は (\[-2⁹⁶ ～ 2⁹⁶\] ÷ 10(0\\ ～\\ 28)) を表します。ここで -(2⁹⁶-1) は表現できる最小値と等しく、2⁹⁶-1 は最大値になります。</span><span class="sxs-lookup"><span data-stu-id="cf872-225">Therefore, the binary representation of a decimal value represents (\[-2⁹⁶ through 2⁹⁶\] ÷ 10(0\\ through\\ 28)), where -(2⁹⁶-1) is the minimum value that can be expressed and 2⁹⁶-1 is the maximum value.</span></span> <span data-ttu-id="cf872-226">**注記:** Finance and Operations アプリケーションで**実数**値を表すために使用されるタイプは、変換された Microsoft Dynamics AX 2012 の X++ から変更されています。</span><span class="sxs-lookup"><span data-stu-id="cf872-226">**Note:** The type that is used to represent **real** values in Finance and Operations applications has changed from the interpreted X++ of Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="cf872-227">ただし、新しいタイプは、古いタイプが表すことができるすべての値を表すことができるので、コードを書き直す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-227">However, you don't have to rewrite any code, because the new type can express all the values that the old type could express.</span></span> <span data-ttu-id="cf872-228">完全な開示のためにこの材料を提供します。</span><span class="sxs-lookup"><span data-stu-id="cf872-228">We provide this material in the interest of full disclosure only.</span></span> <span data-ttu-id="cf872-229">**実数**タイプのすべてのインスタンスが .NET 小数タイプ (**System.Decimal**) のインスタンスとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-229">All instances of the **real** type are now implemented as instances of the .NET decimal type (**System.Decimal**).</span></span> <span data-ttu-id="cf872-230">以前のバージョンでの **real** 型と同様に、バイナリ コード化された小数点以下の型での decimal 型は丸め誤差に対する対応力があります。</span><span class="sxs-lookup"><span data-stu-id="cf872-230">Just as the **real** type in previous versions, the decimal type in a binary-coded decimal type is resilient to rounding errors.</span></span> <span data-ttu-id="cf872-231">以前のバージョンと異なる 10 進型の範囲と解像度。</span><span class="sxs-lookup"><span data-stu-id="cf872-231">The range and resolution of the decimal type differ from previous versions.</span></span> <span data-ttu-id="cf872-232">元の X++ **実数** 型は 16 桁と小数点の位置を定義した指数をサポートしていました。</span><span class="sxs-lookup"><span data-stu-id="cf872-232">The original X++ **real** type supported 16 digits and an exponent that defined the position of the decimal point.</span></span> <span data-ttu-id="cf872-233">ただし、Finance and Operations アプリケーションの**実数**タイプは 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) から -79,228,162,514,264,337,593,543,950,335 (-\[2⁹⁶-1\]) の範囲の 10 進数を表します。</span><span class="sxs-lookup"><span data-stu-id="cf872-233">However, the X++ **real** type for Finance and Operations applications can represent decimal numbers in the range 79,228,162,514,264,337,593,543,950,335 (2⁹⁶-1) through -79,228,162,514,264,337,593,543,950,335 (-\[2⁹⁶-1\]).</span></span> <span data-ttu-id="cf872-234">新しい**実数**タイプにはさらに丸めが必要です。</span><span class="sxs-lookup"><span data-stu-id="cf872-234">Rounding is still required for the new **real** type.</span></span> <span data-ttu-id="cf872-235">たとえば、次のコードは、1 ではなく 0.9999999999999999999999999999 という結果を生成します。</span><span class="sxs-lookup"><span data-stu-id="cf872-235">For example, the following code produces a result of 0.9999999999999999999999999999 instead of 1.</span></span> <span data-ttu-id="cf872-236">1/3 の値を正確に表せる小数点以下の桁数はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-236">No number of decimals will suffice to represent the value of 1/3 accurately.</span></span> <span data-ttu-id="cf872-237">ここで得られる不一致は、有限数の小数しか提供されないことによるものです。</span><span class="sxs-lookup"><span data-stu-id="cf872-237">The discrepancy obtained here is due to the fact that only a finite number of decimals are provided.</span></span> <span data-ttu-id="cf872-238">必要な小数点以下の桁数まで丸めるには、**round** 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="cf872-238">You should use the **round** function to round to the number of decimals required.</span></span>

    // An example of using the debugger to show the value of the variables.
    public static void UseTheDebugger(Args a)
    {
        real dividend = 1.0;
        real divisor = 3.0;
        str stringvalue;
        System.Decimal valueAsDecimal;
        real value = dividend/divisor * divisor; 
        valueAsDecimal = value;
        info(valueAsDecimal.ToString("G28"));
        // An example of using the Round function to round to the number of decimals required.
        value  = round(value, 2);
    }

### <a name="real-examples"></a><span data-ttu-id="cf872-239">real の例</span><span class="sxs-lookup"><span data-stu-id="cf872-239">real examples</span></span>

    public void RealMethod()
    {
        // Simple declaration of a real variable, r.
        real r;

        // Multiple declaration of two real variables.
        real r1, r2;

        // A real variable is initialized to the approximate value of pi.
        real r3 = 3.1415;

        // Declaration of a dynamic array of reals.
        real r4[];

        // An example of a real literal written using exponential notation.
        real r;
        r = 1.000e3;
        r = 1.2345e+3;
        r = 1.2345e+03;
        r = 1234.5e4;
        r = 1.0e1; // Means 1.0E1 
    }

    // An example of automatic conversions.
    void main()
    {
        // Declares a variable of type integer with the name exprValue.
        int exprValue;

        // Declares a real variable with the name area.
        real area = 3.141528;
        exprValue = Area/3;

        // The expression Area/3 is a real expression because
        // division is a real operator, and the result is 1.047176. This result is
        // automatically converted (actually truncated) to an integer with the value 1,
        // because exprValue is an integer.
    }

    // An example of a real being converted to .NET System.Decimal.
    void AnotherMain(Args _args)
    {
        real real9;
        System.Decimal sysdec1;

        // Direct assignments supported between these types.
        sysdec1 = 2.3456;
        real9 = sysdec1;
        info(strFmt("strFmt says real9 == %1", real9));
    }

    /***
    Message (05:48:43 pm)
    strFmt says real9 == 2.35
    ***/

    // An example of using reals in expressions.
    void myMethod()
    {
        // Two real variables are declared and initialized.
        real i = 2.5, j = 2.5;

        // j is assigned the result of j * i, so j=6.25.
        j = j * i;
        if (j > (i * 2)) // If j > 5 
        {
            print "Great"; // "Great" is printed.
        }
        else
        {
           print "Oops"; // else "Oops" is printed.
        }
    }

## <a name="str"></a><span data-ttu-id="cf872-240">str</span><span class="sxs-lookup"><span data-stu-id="cf872-240">str</span></span>

<span data-ttu-id="cf872-241">**str** 変数 (*文字列*) は、テキスト、ヘルプ行、住所、電話番号などとして使用される文字の並びです。</span><span class="sxs-lookup"><span data-stu-id="cf872-241">A **str** variable (a *string*) is a sequence of characters that are used as texts, help lines, addresses, telephone numbers, and so on.</span></span> <span data-ttu-id="cf872-242">文字列を宣言するには、**str** キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf872-242">To declare a string, use the **str** keyword.</span></span> <span data-ttu-id="cf872-243">*文字列リテラル*引用符 ("") で囲まれた文字です。</span><span class="sxs-lookup"><span data-stu-id="cf872-243">*String literals* are characters that are enclosed in quotation marks ("").</span></span> <span data-ttu-id="cf872-244">文字列式が必要な場合はいつでも、文字列リテラルを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-244">String literals can be used wherever string expressions are expected.</span></span> <span data-ttu-id="cf872-245">文字列リテラルの例には、「StringLit」および「Hello World」が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cf872-245">Examples of string literals include "StringLit" and "Hello World".</span></span> <span data-ttu-id="cf872-246">文字列を複数の行にまたがるようにするには、その前にアットマーク (@) を付けます。</span><span class="sxs-lookup"><span data-stu-id="cf872-246">If you want the string to span more than one line, precede it with an at sign (@).</span></span> <span data-ttu-id="cf872-247">比較などの論理式では文字列を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-247">You can use strings in logical expressions, such as comparisons.</span></span> <span data-ttu-id="cf872-248">また、+ 演算子を使用することで文字列を連結することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-248">You can also concatenate strings by using the + operator.</span></span> <span data-ttu-id="cf872-249">文字列の既定値は **空**で、内部表示は文字のリストです。</span><span class="sxs-lookup"><span data-stu-id="cf872-249">The default value for a string is **empty**, and the internal representation is a list of characters.</span></span> <span data-ttu-id="cf872-250">文字列の自動変換はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-250">There are no automatic conversions for strings.</span></span> <span data-ttu-id="cf872-251">ただし、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) が使用できます: **str2int**、**str2int64**、**int2str**、**str2num**、**num2str**、**str2date**、および **date2str**。</span><span class="sxs-lookup"><span data-stu-id="cf872-251">However, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2int**, **str2int64**, **int2str**, **str2num**, **num2str**, **str2date**, and **date2str**.</span></span> <span data-ttu-id="cf872-252">文字列は、無制限の文字数を保持できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-252">A string can hold an unlimited number of characters.</span></span> <span data-ttu-id="cf872-253">ただし、変数の宣言で文字列の最大の長さを指定できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-253">However, you can specify the maximum length of a string in the variable declaration.</span></span> <span data-ttu-id="cf872-254">文字列はその最大長に切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="cf872-254">The string is then truncated to that maximum length.</span></span> <span data-ttu-id="cf872-255">例として次のセクションに表示します。</span><span class="sxs-lookup"><span data-stu-id="cf872-255">An example is shown in the next section.</span></span>

### <a name="str-examples"></a><span data-ttu-id="cf872-256">str の例</span><span class="sxs-lookup"><span data-stu-id="cf872-256">str examples</span></span>

    void StringMethod()
    {
        // Declare a dynamic string of unlimited length.
        str unlimitedString;

        // Declare a string with a maximum of 64 characters
        // in order to force a truncation, initialized to "A".
        str 64 maxLengthString = "A";

        // Declare an array of 100 strings.
       str 30 hundredStrings[100];

        // Using strings in expressions.
        void myMethod()
        {
            // Two strings are declared and initialized.
            str a="Hello", b="World";

            // The concatenation of a, " " and b is printed in a window.
            print a+" "+b;
        }
    }

## <a name="timeofday"></a><span data-ttu-id="cf872-257">timeOfDay</span><span class="sxs-lookup"><span data-stu-id="cf872-257">timeOfDay</span></span>

<span data-ttu-id="cf872-258">**timeOfDay** (時間) データ型は、午前 0 時から経過した秒数を表す整数値です。</span><span class="sxs-lookup"><span data-stu-id="cf872-258">The **timeOfDay** (time) data type is an integer value that represents the number of seconds that have passed since midnight.</span></span> <span data-ttu-id="cf872-259">整数と同様に、**timeOfDay** 変数はリテラルとして使用することができます。</span><span class="sxs-lookup"><span data-stu-id="cf872-259">Like integers, **timeOfDay** variables can be used as literals.</span></span> <span data-ttu-id="cf872-260">リレーショナルおよび算術演算子は、**timeOfDay** 変数に適用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-260">Relational and arithmetic operators can be applied to **timeOfDay** variables.</span></span> <span data-ttu-id="cf872-261">**timeOfDay** 変数も式で使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-261">A **timeOfDay** variable can also be used in expressions.</span></span> <span data-ttu-id="cf872-262">**timeOfDay** データ型の範囲は \[0;86,400\] のクローズ区間にあります。</span><span class="sxs-lookup"><span data-stu-id="cf872-262">The range of a **timeOfDay** data type is in the closed interval \[0; 86,400\].</span></span> <span data-ttu-id="cf872-263">86,400 (23: 59:59) を超える値は解釈できません。</span><span class="sxs-lookup"><span data-stu-id="cf872-263">Values above 86,400 (23:59:59) can't be interpreted.</span></span> <span data-ttu-id="cf872-264">**timeOfDay** 変数は、自動的に**ブール**、**enum**、または**実数**に変換されます。</span><span class="sxs-lookup"><span data-stu-id="cf872-264">A **timeOfDay** variable is automatically converted to a **boolean**, **enum**, or **real**.</span></span> <span data-ttu-id="cf872-265">また、次の明示的な [変換関数](xpp-conversion-run-time-functions.md) を使用できます: **str2time**、**time2str**。</span><span class="sxs-lookup"><span data-stu-id="cf872-265">Additionally, the following explicit [conversion functions](xpp-conversion-run-time-functions.md) can be used: **str2time** and **time2str**.</span></span>

### <a name="timeofday-examples"></a><span data-ttu-id="cf872-266">timeOfDay の例</span><span class="sxs-lookup"><span data-stu-id="cf872-266">timeOfDay examples</span></span>

    public void TimeofdayMethod()
    {
        // Declaration of a timeOfDay variable, time1.
        timeOfDay time1;

        // Declaration and initialization of a timeOfDay variable to 00:21:35.
        timeOfDay time2 = 1295;
    }

## <a name="utcdatetime"></a><span data-ttu-id="cf872-267">utcdatetime</span><span class="sxs-lookup"><span data-stu-id="cf872-267">utcdatetime</span></span>

<span data-ttu-id="cf872-268">**utcdatetime** データ型は、**date** 型と **timeOfDay** 型を結合します。</span><span class="sxs-lookup"><span data-stu-id="cf872-268">The **utcdatetime** data type combines the **date** type and the **timeOfDay** type.</span></span> <span data-ttu-id="cf872-269">**utcdatetime** 変数には、タイム ゾーンに関する情報も含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf872-269">A **utcdatetime** variable also holds information about the time zone.</span></span> <span data-ttu-id="cf872-270">ただし、この情報はコードではアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="cf872-270">However, this information can't be accessed in code.</span></span> <span data-ttu-id="cf872-271">**utcdatetime** リテラルの形式は、**yyyy-mm-ddThh:mm:ss** です。</span><span class="sxs-lookup"><span data-stu-id="cf872-271">The format for a **utcdatetime** literal is **yyyy-mm-ddThh:mm:ss**.</span></span> <span data-ttu-id="cf872-272">大文字「T」が必要です。</span><span class="sxs-lookup"><span data-stu-id="cf872-272">The uppercase "T" is required.</span></span> <span data-ttu-id="cf872-273">この形式は引用符を使用せずに記述できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-273">This format can be written without quotation marks.</span></span> <span data-ttu-id="cf872-274">最小値は、**1900-01-01T00:00:00** で、最大値は **1900-01-01T00:00:00** です。</span><span class="sxs-lookup"><span data-stu-id="cf872-274">The minimum value is **1900-01-01T00:00:00**, and the maximum value is **1900-01-01T00:00:00**.</span></span> <span data-ttu-id="cf872-275">この最大値は、**date** と **timeOfDay** の上位範囲に一致します。</span><span class="sxs-lookup"><span data-stu-id="cf872-275">This maximum value matches the upper range of **date** and **timeOfDay**.</span></span> <span data-ttu-id="cf872-276">**utcdatetime** の最小単位は 1 秒です。</span><span class="sxs-lookup"><span data-stu-id="cf872-276">The smallest unit of time in **utcdatetime** is one second.</span></span> <span data-ttu-id="cf872-277">宣言されているもののまた初期化されていない **utcdatetime** 変数の規定値は、 **1900-01-01T00:00:00** です。</span><span class="sxs-lookup"><span data-stu-id="cf872-277">A **utcdatetime** variable that has been declared but hasn't been initialized has the default value **1900-01-01T00:00:00**.</span></span> <span data-ttu-id="cf872-278">この値は、**DateTimeUtil::minValue()** によって返される値です。</span><span class="sxs-lookup"><span data-stu-id="cf872-278">This value is the value that is returned by **DateTimeUtil::minValue()**.</span></span> <span data-ttu-id="cf872-279">一部の機能は、この最小値の入力パラメーターを **null** として扱います。</span><span class="sxs-lookup"><span data-stu-id="cf872-279">Some functions treat an input parameter of this minimum value as **null**.</span></span> <span data-ttu-id="cf872-280">たとえば、**DateTimeUtil::toStr** メソッドは、空の文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="cf872-280">For example, the **DateTimeUtil::toStr** method returns an empty string.</span></span> <span data-ttu-id="cf872-281">ただし、**DateTimeUtil::addSeconds** メソッドは使用可能な **utcdatetime** 値を返します。</span><span class="sxs-lookup"><span data-stu-id="cf872-281">However, the **DateTimeUtil::addSeconds** method returns a usable **utcdatetime** value.</span></span> <span data-ttu-id="cf872-282">**utcdatetime** データ型の暗黙的な変換はありません。</span><span class="sxs-lookup"><span data-stu-id="cf872-282">There are no implicit conversions for the **utcdatetime** data type.</span></span> <span data-ttu-id="cf872-283">**DateTimeUtil** クラスは、**utcdatetime** 値を操作するために使用できるさまざまなメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="cf872-283">The **DateTimeUtil** class provides many methods that you can use to manipulate **utcdatetime** values.</span></span> <span data-ttu-id="cf872-284">次の明示的な [変換関数](xpp-conversion-run-time-functions.md)、**str2datetime** および **datetime2str** も使用できます。</span><span class="sxs-lookup"><span data-stu-id="cf872-284">The following explicit [conversion functions](xpp-conversion-run-time-functions.md) can also be used: **str2datetime** and **datetime2str**.</span></span> <span data-ttu-id="cf872-285">また、**グローバル** クラスは、**utcDateTime2SystemDateTime** と **CLRSystemDateTime2UtcDateTime** 変換メソッドを提供して、共通言語ランタイム (CLR) 相互運用をサポートします。</span><span class="sxs-lookup"><span data-stu-id="cf872-285">Additionally, the **Global** class provides the **utcDateTime2SystemDateTime** and **CLRSystemDateTime2UtcDateTime** conversion methods to support common language runtime (CLR) interop.</span></span> <span data-ttu-id="cf872-286">比較演算子は、**utcdatetime** データ型で使用できる唯一の演算子です。</span><span class="sxs-lookup"><span data-stu-id="cf872-286">Comparison operators are the only type of operators that can be used with the **utcdatetime** data type.</span></span> <span data-ttu-id="cf872-287">次の演算子を使用して、2つの **utcdatetime** 値を比較することができます: !=、&lt;、&lt;=、==、&gt;、および &gt;=。</span><span class="sxs-lookup"><span data-stu-id="cf872-287">The following operators can be used to compare two **utcdatetime** values: !=, &lt;, &lt;=, ==, &gt;, and &gt;=.</span></span> <span data-ttu-id="cf872-288">テーブルに **utcdatetime** フィールドを追加するときは、そのフィールドを EDT にもとづいて決めることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="cf872-288">When you add a **utcdatetime** field to a table, we recommend that you base the field on an EDT.</span></span>

### <a name="utcdatetime-examples"></a><span data-ttu-id="cf872-289">utcdatetime の例</span><span class="sxs-lookup"><span data-stu-id="cf872-289">utcdatetime examples</span></span>

    public void UtcdatetimeMethod()
    {
        // Declaring a utcdatetime literal.
        utcdatetime myUtc2 = 1988-07-20T13:34:45;

        // Another example of declaring a utcdatetime literal.
        int iDay = DateTimeUtil::day(1988-07-20T13:34:45);

        // utcdatetime using a quoted string parameter into the DateTimeUtil::parse method.
        utcdatetime myUtc4 = DateTimeUtil::parse("1988-07-20T13:34:45");
    }

---
title: アプリケーション オブジェクト ツリー (AOT) を使用してテーブルを作成する
description: このトピックでは、アプリケーション オブジェクト ツリー (AOT) を使用してデータを格納するテーブルを作成する方法について説明します。
author: kfend
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 18161
ms.assetid: 96e1f184-d049-46c3-a4ef-12641361f356
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 00096736e29667fe3df1d12cc9b1902e1b920b15
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983636"
---
# <a name="create-tables-by-using-the-application-object-tree-aot"></a><span data-ttu-id="07205-103">アプリケーション オブジェクト ツリー (AOT) を使用してテーブルを作成する</span><span class="sxs-lookup"><span data-stu-id="07205-103">Create tables by using the Application Object Tree (AOT)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07205-104">アプリケーション オブジェクト ツリー (AOT) を使用してデータを格納するテーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="07205-104">Create tables to store data in by using the Application Object Tree (AOT).</span></span>

> [!NOTE]
> <span data-ttu-id="07205-105">新しいテーブルを作成する前に、Microsoft Dynamics AX に付属のテーブルを確認して既存のテーブルを使用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="07205-105">Before creating new tables, review the tables that ship with Microsoft Dynamics AX to determine whether you can use existing tables.</span></span> <span data-ttu-id="07205-106">詳細については、「[アプリケーション テーブル](https://msdn.microsoft.com/library/a905f039-ef71-4c61-8f3f-71dadf27b09e(AX.60).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-106">For more information, see [Application Tables](https://msdn.microsoft.com/library/a905f039-ef71-4c61-8f3f-71dadf27b09e(AX.60).aspx).</span></span>

<span data-ttu-id="07205-107">テーブル フィールドは、プリミティブ データ型または拡張データ型に基づいています。</span><span class="sxs-lookup"><span data-stu-id="07205-107">Table fields are based on a primitive data type or an extended data type.</span></span> <span data-ttu-id="07205-108">詳細については、[プリミティブ データ型](https://msdn.microsoft.com/library/29e7d464-b72d-4a86-a982-12f9e90e704e(AX.60).aspx) および [方法: 拡張データ型の作成](https://msdn.microsoft.com/library/6292481f-1d73-46e9-8b46-18ab7de9a71d(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-108">For more information, see [Primitive Data Types](https://msdn.microsoft.com/library/29e7d464-b72d-4a86-a982-12f9e90e704e(AX.60).aspx) and [How to: Create an Extended Data Type](https://msdn.microsoft.com/library/6292481f-1d73-46e9-8b46-18ab7de9a71d(AX.60).aspx).</span></span> <span data-ttu-id="07205-109">AutoReport および AutoLookup グループは、テーブルを作成するときに自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="07205-109">The AutoReport and AutoLookup groups are automatically created when you create a table.</span></span> <span data-ttu-id="07205-110">詳細については、[フォームの自動レポートの実装](https://msdn.microsoft.com/library/86ee1f62-8325-4bcb-a884-a5ae521355c8(AX.60).aspx) および [方法: ルックアップ フォームでコントロールの追加](https://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-110">For more information, see [Implementing Automatic Reports for Forms](https://msdn.microsoft.com/library/86ee1f62-8325-4bcb-a884-a5ae521355c8(AX.60).aspx) and [How to: Add a Control with a Lookup Form](https://msdn.microsoft.com/library/2e365e4b-842a-44eb-b0fa-6fa4c8c1e0fe(AX.60).aspx).</span></span> <span data-ttu-id="07205-111">AOT オブジェクトの変更を管理するために、バージョン管理システムが利用できます。</span><span class="sxs-lookup"><span data-stu-id="07205-111">To manage changes to AOT objects, a version control system is available.</span></span> <span data-ttu-id="07205-112">詳細については、[バージョン管理システム](https://msdn.microsoft.com/library/522708f8-80a0-4bfd-9634-b7cb868d1874(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-112">For more information, see [Version Control System](https://msdn.microsoft.com/library/522708f8-80a0-4bfd-9634-b7cb868d1874(AX.60).aspx).</span></span>

## <a name="create-a-table"></a><span data-ttu-id="07205-113">テーブルの作成</span><span class="sxs-lookup"><span data-stu-id="07205-113">Create a Table</span></span>
1.  <span data-ttu-id="07205-114">AOT で、**データ ディクショナリ** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="07205-114">In the AOT, expand the **Data Dictionary** node.</span></span>
2.  <span data-ttu-id="07205-115">**テーブル** ノードを右クリックし、**新しいテーブル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07205-115">Right-click the **Tables** node, and then select **New Table**.</span></span>
3.  <span data-ttu-id="07205-116">テーブルを右クリックし、**プロパティ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07205-116">Right-click the table, and then click **Properties**.</span></span>
4.  <span data-ttu-id="07205-117">**Name** プロパティを変更することにより、テーブルの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="07205-117">Rename the table by modifying the **Name** property.</span></span>
5.  <span data-ttu-id="07205-118">テーブルを一時的に指定するには、**一時的な** プロパティを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="07205-118">To specify the table as temporary, set the **Temporary** property to **Yes**.</span></span> <span data-ttu-id="07205-119">詳細については、 [アプリケーション オブジェクト ツリー (AOT) のテーブルプロパティ](table-properties.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-119">For more information, see [Table properties in the Application Object Tree (AOT)](table-properties.md).</span></span>
6.  <span data-ttu-id="07205-120">必要に応じて、追加のテーブル プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="07205-120">Modify additional table properties, as needed.</span></span> <span data-ttu-id="07205-121">詳細については、 [アプリケーション オブジェクト ツリー (AOT) のテーブルプロパティ](table-properties.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-121">For more information, see [Table properties in the Application Object Tree (AOT)](table-properties.md).</span></span>
7.  <span data-ttu-id="07205-122">テーブルを削除するには、それを右クリックし、**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07205-122">To delete the table, right-click it, and then click **Delete**.</span></span>

## <a name="add-fields-to-a-table"></a><span data-ttu-id="07205-123">テーブルにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="07205-123">Add Fields to a Table</span></span>

> [!NOTE]
> <span data-ttu-id="07205-124">テーブル レコードのどこにもデータを含まないフィールドのみを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="07205-124">You can delete only fields that do not contain data in any of the table records.</span></span> <span data-ttu-id="07205-125">既存のフィールドのデータ型を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="07205-125">You cannot modify the data type of an existing field.</span></span>

1.  <span data-ttu-id="07205-126">テーブルの **フィールド** ノードを右クリックします。</span><span class="sxs-lookup"><span data-stu-id="07205-126">Right-click the **Fields** node of your table.</span></span>
2.  <span data-ttu-id="07205-127">**新規**をクリックし、フィールドの基になるプリミティブ データ型を選択します。</span><span class="sxs-lookup"><span data-stu-id="07205-127">Click **New**, and then choose a primitive data type to base your field on.</span></span> <span data-ttu-id="07205-128">特定の拡張データ型のフィールドを基準に計画する場合は、拡張データ型の基準となるプリミティブ データ タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="07205-128">If you plan to base the field on a specific extended data type, you must choose a primitive data type that the extended data type is based on.</span></span>
3.  <span data-ttu-id="07205-129">拡張データ型に基づいてフィールドを設定するには、**ExtendedDataType** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="07205-129">To base the field on an extended data type, set the **ExtendedDataType** property.</span></span>
4.  <span data-ttu-id="07205-130">必要に応じて、追加のフィールド プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="07205-130">Modify additional field properties, as needed.</span></span> <span data-ttu-id="07205-131">詳細については、 [アプリケーション オブジェクト ツリー (AOT) のテーブルプロパティ](table-properties.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="07205-131">For more information, see [Table properties in the Application Object Tree (AOT)](table-properties.md).</span></span>
5.  <span data-ttu-id="07205-132">フィールドを削除するには、フィールドを右クリックし、**削除** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="07205-132">To delete the field, right-click it, and then click **Delete**.</span></span>

### <a name="restart-the-aos-after-adding-fields-to-tables"></a><span data-ttu-id="07205-133">フィールドをテーブルに追加した後、AOS を再起動</span><span class="sxs-lookup"><span data-stu-id="07205-133">Restart the AOS after Adding Fields to Tables</span></span>

<span data-ttu-id="07205-134">開発時にテーブルにデータを挿入するとき、データの挿入に使用する SQL ステートメントは AOS でキャッシュされます。</span><span class="sxs-lookup"><span data-stu-id="07205-134">When you insert data in a table during development, the SQL statement you use to insert the data is cached in the AOS.</span></span> <span data-ttu-id="07205-135">次に、テーブルに新しいフィールドを追加して、データベースへの変更を保持する場合があります。</span><span class="sxs-lookup"><span data-stu-id="07205-135">Next you might add a new field to the table and persist the change to the database.</span></span> <span data-ttu-id="07205-136">これにより、新しいフィールドを含むようにステートメントが更新されないため、キャッシュ内の SQL ステートメントが無効になります。</span><span class="sxs-lookup"><span data-stu-id="07205-136">This causes the SQL statement in the cache to become stale, because the statement is not updated to include the new field.</span></span> <span data-ttu-id="07205-137">古いステートメントを再利用すると、新しいフィールドは無視されるか、エラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="07205-137">If you reuse the stale statement, the new field is ignored, or an error might occur.</span></span> <span data-ttu-id="07205-138">この問題を回避するには、スキーマ変更をデータベースに保持した後で AOS を再起動します。</span><span class="sxs-lookup"><span data-stu-id="07205-138">To avoid this problem, restart the AOS after you persist table schema changes to the database.</span></span> <span data-ttu-id="07205-139">AOS が再起動すると、キャッシュは空になります。</span><span class="sxs-lookup"><span data-stu-id="07205-139">The cache is empty when the AOS restarts.</span></span>

<a name="additional-resources"></a><span data-ttu-id="07205-140">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="07205-140">Additional resources</span></span>
--------

<span data-ttu-id="07205-141">[テーブル ブラウザを使用して、表示、追加、変更、またはレコードを削除する](https://msdn.microsoft.com/library/89402b55-02ea-40bc-ad0e-0774b1655426(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="07205-141">[Use the Table Browser to View, Add, Modify, or Delete Records](https://msdn.microsoft.com/library/89402b55-02ea-40bc-ad0e-0774b1655426(AX.60).aspx)</span></span>

<span data-ttu-id="07205-142">[方法: テーブルへのリレーションの追加](https://msdn.microsoft.com/library/1b164b99-de08-4557-8da5-1931d9469ca1(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="07205-142">[How to: Add a Relation to a Table](https://msdn.microsoft.com/library/1b164b99-de08-4557-8da5-1931d9469ca1(AX.60).aspx)</span></span>

<span data-ttu-id="07205-143">[方法: インデックスを作成する](https://msdn.microsoft.com/library/5c412c46-724b-4498-ab42-51725f15c71a(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="07205-143">[How to: Create an Index](https://msdn.microsoft.com/library/5c412c46-724b-4498-ab42-51725f15c71a(AX.60).aspx)</span></span>

<span data-ttu-id="07205-144">[テーブル、ビュー、およびマップ](https://msdn.microsoft.com/library/9c62bde0-46a1-4b48-87b2-778a68627cd1(AX.60).aspx)</span><span class="sxs-lookup"><span data-stu-id="07205-144">[Tables, Views, and Maps](https://msdn.microsoft.com/library/9c62bde0-46a1-4b48-87b2-778a68627cd1(AX.60).aspx)</span></span>




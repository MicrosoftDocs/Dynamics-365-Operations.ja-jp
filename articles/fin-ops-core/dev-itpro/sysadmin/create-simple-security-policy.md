---
title: セキュリティ ポリシーを作成する
description: このトピックでは、顧客グループの範囲に基づいて、顧客および顧客グループへのアクセスを保護する単純なセキュリティ ポリシーを作成する方法について説明します。
author: Peakerbl
ms.date: 07/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: IT Pro
ms.reviewer: sericks
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 9e33a16ffe865ecb3af14e28d2f221d7f23f76fa
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745989"
---
# <a name="create-a-security-policy"></a><span data-ttu-id="1cbfc-103">セキュリティ ポリシーを作成する</span><span class="sxs-lookup"><span data-stu-id="1cbfc-103">Create a security policy</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="1cbfc-104">このトピックでは、顧客グループの範囲に基づいて、顧客および顧客グループへのアクセスを保護する単純なセキュリティ ポリシーを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-104">This topic explains how to create a simple security policy that secures access to customers and customer groups, based on a range for a customer group.</span></span>

## <a name="add-a-new-query"></a><span data-ttu-id="1cbfc-105">新しいクエリの追加</span><span class="sxs-lookup"><span data-stu-id="1cbfc-105">Add a new query</span></span>

1.  <span data-ttu-id="1cbfc-106">Visual Studio にて、プロジェクト/ソリューションに XDSQCustGroup10 などの新しいクエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-106">In Visual Studio, add a new query, such as XDSQCustGroup10, to your project/solution.</span></span> <span data-ttu-id="1cbfc-107">クエリは、**制約** テーブルからのデータ アクセスを制限するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-107">The query will be used to restrict data access from the **Constraint** table.</span></span>

    ![新しいクエリの追加](media/71c5206330564e8c2612a61a5a211dba.png)

2.  <span data-ttu-id="1cbfc-109">**データ ソース** を右クリックし、**新しいデータ ソース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-109">Right-click **Data Sources**, and the select **New Data Source**.</span></span>

3.  <span data-ttu-id="1cbfc-110">**テーブル** フィールドで、プライマリ テーブル名を **CustGroup** と入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-110">In the **Table** field, enter the primary table name **CustGroup**.</span></span>

4.  <span data-ttu-id="1cbfc-111">**範囲** を右クリックし、**新しい範囲** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-111">Right-click **Ranges**, and then select **New Range**.</span></span>

5.  <span data-ttu-id="1cbfc-112">**有効** フィールドを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-112">Set the **Enabled** field to **Yes**.</span></span>

6.  <span data-ttu-id="1cbfc-113">**データ ソース** フィールドで、プライマリ テーブル名を、この場合は「CustGroup」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-113">In the **Data Source** field, enter the primary table name, in this case, ‘CustGroup’.</span></span>

7.  <span data-ttu-id="1cbfc-114">**値フィールド** で **10** と入力して、CustGroup フィールドの範囲を定義することで、CustGroup の値が 10 であるデータへアクセスを制限します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-114">In the **Value field**, enter **10** to restrict access to data where CustGroup has value of 10, by defining the Range for the CustGroup field.</span></span>

    ![値フィールドで、10 と入力](media/c970ccc0649fcd2ee4e2b9a9819eb2fc.png)

## <a name="add-a-new-security-policy"></a><span data-ttu-id="1cbfc-116">新しいセキュリティ ポリシーの追加</span><span class="sxs-lookup"><span data-stu-id="1cbfc-116">Add a new security policy</span></span>

1.  <span data-ttu-id="1cbfc-117">XDSCustTableOnCustGroup10 などの新しいセキュリティ ポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-117">Add a new security policy, such as XDSCustTableOnCustGroup10.</span></span>

    ![セキュリティ ポリシーの追加](media/118355845fa679f8f004e516f0691cff.png)

2.  <span data-ttu-id="1cbfc-119">**制約付きテーブル** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-119">Set **Constrained Table** to **Yes**.</span></span> <span data-ttu-id="1cbfc-120">これにより、プライマリ テーブルへのアクセスもセキュリティで保護されます。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-120">This will also secure access to the primary table.</span></span> <span data-ttu-id="1cbfc-121">この例では、これが **CustGroup** テーブルです。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-121">In this example this is the **CustGroup** table.</span></span>

3.  <span data-ttu-id="1cbfc-122">**コンテキスト タイプ** フィールドを **RoleName** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-122">Set the **Context Type** field to **RoleName**.</span></span>

4.  <span data-ttu-id="1cbfc-123">**有効** フィールドを、**はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-123">Set the **Enabled** field to **Yes**.</span></span>

5.  <span data-ttu-id="1cbfc-124">**操作** フィールドを **AllOperations** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-124">Set the **Operation** field to **AllOperations**.</span></span> <span data-ttu-id="1cbfc-125">**操作** の他の使用可能な値には、**選択**、**挿入**、**更新**、**削除**、および **InsertUpdateDelete** などがあります。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-125">Other available values for **Operation** include **Select**, **Insert**, **Update**, **Delete**, and **InsertUpdateDelete**.</span></span>

6.  <span data-ttu-id="1cbfc-126">**プライマリ テーブル** フィールドを **CustGroup** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-126">Set **Primary Table** field to **CustGroup**.</span></span>

7.  <span data-ttu-id="1cbfc-127">**クエリ** フィールドに、上記で作成したクエリの名前、たとえば 「XDSQCustGroup10」 を設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-127">Set the **Query** field to the name of the query created above, for example ‘XDSQCustGroup10’.</span></span>

8.  <span data-ttu-id="1cbfc-128">**ロール名** フィールドを 「TradeSalesClerk」に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-128">Set the **Role Name** field to ‘TradeSalesClerk’.</span></span> <span data-ttu-id="1cbfc-129">**コンテキスト タイプ** がこのポリシーの RoleName に設定されているため、ユーザー ロールの AOT 名を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-129">Because **Context Type** is set to RoleName for this policy, it is required to enter the AOT name for a user role.</span></span>

    ![ロール名フィールドで、TradeSalesClerk を入力](media/9ad07f1e403cadfc3f1a52c2433e42c7.png)

8.  <span data-ttu-id="1cbfc-131">次に、制約されたテーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-131">Next, add constrained tables.</span></span> <span data-ttu-id="1cbfc-132">この簡単な例では、テーブルを 1 つ追加します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-132">In this simple example add one table.</span></span>

    ![制約付きテーブルの追加](media/e366725fa084d308b7f02a89a3e6175b.png)

    <span data-ttu-id="1cbfc-134">a.</span><span class="sxs-lookup"><span data-stu-id="1cbfc-134">a.</span></span>  <span data-ttu-id="1cbfc-135">**制約付きテーブル** を右クリックし、**新しい \> 制約付きテーブル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-135">Right-click **Constrained tables**, and then select **New \> Constrained Table**.</span></span>

    <span data-ttu-id="1cbfc-136">b.</span><span class="sxs-lookup"><span data-stu-id="1cbfc-136">b.</span></span>  <span data-ttu-id="1cbfc-137">**制約付き** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-137">Set **Constrained** to **Yes**.</span></span>

    <span data-ttu-id="1cbfc-138">c.</span><span class="sxs-lookup"><span data-stu-id="1cbfc-138">c.</span></span>  <span data-ttu-id="1cbfc-139">**名前** フィールドで、制約付きテーブル、たとえば 「CustTable」 を入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-139">In the **Name** field, enter the Constrained table, for example ‘CustTable’.</span></span>

    <span data-ttu-id="1cbfc-140">d.</span><span class="sxs-lookup"><span data-stu-id="1cbfc-140">d.</span></span>  <span data-ttu-id="1cbfc-141">**テーブル リレーション** フィールドで、プライマリ テーブルにリレーション、この例では 「custgroup」 と入力します。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-141">In the **Table Relation** field, enter the relationship to the primary table, in this case ‘CustGroup’.</span></span>

10.  <span data-ttu-id="1cbfc-142">最後の手順として、ソリューションをビルドおよび同期し、ポリシーを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1cbfc-142">As a final step, it is required that you build and synchronize the solution to activate the policy.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
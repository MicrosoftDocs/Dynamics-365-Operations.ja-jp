---
title: 場所と関係者のリレーションシップ タイプの追加
description: このトピックでは、新規の場所および関係者のリレーションシップ タイプを追加する方法について説明します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e38d0bd75ad865b7885182f798beb43551576beb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770899"
---
# <a name="add-location-and-party-relationship-types"></a><span data-ttu-id="207b7-103">場所と関係者のリレーションシップ タイプの追加</span><span class="sxs-lookup"><span data-stu-id="207b7-103">Add location and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="207b7-104">場所のロールの追加</span><span class="sxs-lookup"><span data-stu-id="207b7-104">Add location roles</span></span>

<span data-ttu-id="207b7-105">住所および連絡先情報について、新たに場所ロールを追加するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="207b7-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="207b7-106">**住所および連絡先情報の目的**ページに追加します。</span><span class="sxs-lookup"><span data-stu-id="207b7-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="207b7-107">新規ロールは **LogisticsLocationRole** テーブルにタイプ = 0 で保存されます。これは、ロールが **LogisticsLocationRoleType** 列挙型とその拡張で定義されたシステム ロールではないことを示しています。</span><span class="sxs-lookup"><span data-stu-id="207b7-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="207b7-108">ユーザーは住所や連絡先情報を作成するときに、このロールを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="207b7-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![住所とコンテンツ情報の目的](media/Address-Contact.PNG)

-  <span data-ttu-id="207b7-110">**LogisticsLocationRoleType** 列挙型拡張に追加し、データベースの同期プロセスで設定します。</span><span class="sxs-lookup"><span data-stu-id="207b7-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="207b7-111">**LogisticsLocationRoleType** 列挙型に拡張を作成し、新規ロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="207b7-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType 列挙の拡張](media/Logistics.PNG)

    2. <span data-ttu-id="207b7-113">新規ロールのリソース ファイルを新たに作成し、そのプロパティの値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="207b7-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![新規リソース ファイル](media/Resource.PNG)
        
    3.  <span data-ttu-id="207b7-115">データ設定クラスを作成し、新規ロールを設定するハンドラー メソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="207b7-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![データ設定](media/Dirdata.PNG)

    4.  <span data-ttu-id="207b7-117">新規場所ロールの設定をテストするには、実行可能なクラスを作成し、Main() の DirDataPopulation::insertLogisticsLocationRoles() を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="207b7-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="207b7-118">このプロセスが完了すると、**LogisticsLocationRole** テーブルでタイプ \>0 で設定した新規ロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="207b7-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="207b7-119">**住所と連絡先情報の目的**ページに新規ロールが表示されます。</span><span class="sxs-lookup"><span data-stu-id="207b7-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![新規の場所の挿入](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="207b7-121">関係者のリレーションシップ タイプの追加</span><span class="sxs-lookup"><span data-stu-id="207b7-121">Add party relationship types</span></span> 

<span data-ttu-id="207b7-122">新規リレーションシップ タイプを追加するには次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="207b7-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="207b7-123">**リレーションシップ タイプ**ページに追加します。</span><span class="sxs-lookup"><span data-stu-id="207b7-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="207b7-124">新規リレーションシップは **DirRelationshipTypeTable** に、systemtype = 0 で保存されます。</span><span class="sxs-lookup"><span data-stu-id="207b7-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![関係タイプ](media/Relationship.PNG)

-  <span data-ttu-id="207b7-126">**DirSystemRelationshipType** 列挙型拡張に追加し、データベースの同期プロセスで設定します。</span><span class="sxs-lookup"><span data-stu-id="207b7-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="207b7-127">**DirSystemRelationshipType** 列挙に拡張を作成して、新規リレーションシップ タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="207b7-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="207b7-128">この新規タイプの初期化子を作成します。</span><span class="sxs-lookup"><span data-stu-id="207b7-128">Create an initializer for this new type.</span></span> <span data-ttu-id="207b7-129">コア コードで複数の例を見つけることができます。そのうちの 1 つが **DirRelationshipTypeChildInitialize** です。</span><span class="sxs-lookup"><span data-stu-id="207b7-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="207b7-130">これは、関係者のリレーションシップ タイプが「子ども」の初期化子のクラスです。</span><span class="sxs-lookup"><span data-stu-id="207b7-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="207b7-131">このコードをコピーして貼り付けることで、初期化子を使って開始し、強調表示されたエリアを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="207b7-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild 初期化子](media/DirRelationship.PNG)

    3.  <span data-ttu-id="207b7-133">新規リレーションシップ タイプの設定をテストするには、実行可能なクラスを作成し、Main() の DirDataPopulation::insertDirRelationshipTypes() を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="207b7-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="207b7-134">**DirRelationshipTypeTable** に新規リレーションシップ タイプが表示され、**リレーションシップ タイプ**ページでこの新規リレーションシップ タイプが利用可能となります。</span><span class="sxs-lookup"><span data-stu-id="207b7-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![実行可能なクラス](media/Runnable.PNG)

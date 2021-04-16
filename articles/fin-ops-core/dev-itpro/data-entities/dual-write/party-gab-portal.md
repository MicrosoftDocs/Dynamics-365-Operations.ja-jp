---
title: Power Portal を当事者のデータ モデルで使用する
description: このトピックでは、二重書き込みの当事者データ モデルに対する Power Portal Web ロールの変更について説明します。
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833093"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="c2a5b-103">Power Portal を当事者のデータ モデルで使用する</span><span class="sxs-lookup"><span data-stu-id="c2a5b-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c2a5b-104">二重書き込みアプリケーション オーケストレーション ソリューションのバージョン 2.0.999.0 以降には、アカウントと連絡先のテーブルの当事者およびグローバル アドレス帳に対するデータ モデルの変更が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="c2a5b-105">この変更により、高度な業務シナリオをサポートする多対多のリレーションが可能になります。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="c2a5b-106">これらの変更は、顧客ポータルを含め、実際には使用していたか、二重書き込みをインストールする前に環境に存在していた顧客ポータルを含め、ポータル Web ロールではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="c2a5b-107">Web ロールを予定通り動作させるには、新しいデータ モデルを使用して新しい Web ロールを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="c2a5b-108">簡単に言うと、テーブルの対話の方法は変更されましたが、顧客ポータルのテーブルのアクセス許可は変更されないということです。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="c2a5b-109">このトピックでは、新しい高度なデータ モデルと機能する新しい Web ロールを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="c2a5b-110">次の図は、当事者とグローバル アドレス帳データ モデルを **持たない** テーブル リレーションシップを示しています。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![当事者モデルを使用しない](media/without-party-model.PNG)

<span data-ttu-id="c2a5b-112">次の図は、当事者とグローバル アドレス帳データ モデルを **持つ** テーブル リレーションシップを示しています。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![当事者モデルを使用する](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="c2a5b-114">テーブルの新しいアクセス許可を作成する</span><span class="sxs-lookup"><span data-stu-id="c2a5b-114">Create a new table permission</span></span>

<span data-ttu-id="c2a5b-115">これらの新しいテーブルのアクセス許可を作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="c2a5b-116">[Power Apps](https://make.powerapps.com) にサインインし、アプリに移動します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="c2a5b-117">ポータル管理アプリを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="c2a5b-118">サイド バーで、**セキュリティ > テーブルのアクセス許可** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="c2a5b-119">新しいアクセス許可を 3 つ作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="c2a5b-120">連絡先から当事者への接続</span><span class="sxs-lookup"><span data-stu-id="c2a5b-120">Contact to Party connection</span></span>
    + <span data-ttu-id="c2a5b-121">当事者からアカウントへの接続</span><span class="sxs-lookup"><span data-stu-id="c2a5b-121">Party to Account connection</span></span>
    + <span data-ttu-id="c2a5b-122">アカウントから注文への接続</span><span class="sxs-lookup"><span data-stu-id="c2a5b-122">Account to Order connection</span></span>

4. <span data-ttu-id="c2a5b-123">次のパラメーターを設定して、連絡先から当事者との接続に対する新しいアクセス許可を作成して保存します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="c2a5b-124">**名前**: 当事者からアカウントへの接続 (または選択した項目)</span><span class="sxs-lookup"><span data-stu-id="c2a5b-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="c2a5b-125">**テーブル名**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="c2a5b-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="c2a5b-126">**Web サイト**: 顧客ポータル</span><span class="sxs-lookup"><span data-stu-id="c2a5b-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c2a5b-127">**範囲**: 連絡先</span><span class="sxs-lookup"><span data-stu-id="c2a5b-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="c2a5b-128">**特権**: すべて選択</span><span class="sxs-lookup"><span data-stu-id="c2a5b-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c2a5b-129">**Web ロール**: 認証されたユーザー、顧客担当者 (または選択された項目)</span><span class="sxs-lookup"><span data-stu-id="c2a5b-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="c2a5b-130">次のパラメーターを設定して、当事者からアカウントへの接続に対する新しいアクセス許可を作成して保存します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="c2a5b-131">**名前**: 当事者からアカウントへの接続 (または選択した項目)</span><span class="sxs-lookup"><span data-stu-id="c2a5b-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="c2a5b-132">**テーブル名**: account</span><span class="sxs-lookup"><span data-stu-id="c2a5b-132">**Table Name**: account</span></span>
    + <span data-ttu-id="c2a5b-133">**Web サイト**: 顧客ポータル</span><span class="sxs-lookup"><span data-stu-id="c2a5b-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c2a5b-134">**範囲**: 親</span><span class="sxs-lookup"><span data-stu-id="c2a5b-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="c2a5b-135">**特権**: すべて選択</span><span class="sxs-lookup"><span data-stu-id="c2a5b-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c2a5b-136">**親テーブルのアクセス許可**: 連絡先から当事者への接続</span><span class="sxs-lookup"><span data-stu-id="c2a5b-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="c2a5b-137">次のパラメーターを設定して、アカウントから注文への接続に対する新しいアクセス許可を作成して保存します。</span><span class="sxs-lookup"><span data-stu-id="c2a5b-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="c2a5b-138">**名前**: アカウントから注文への接続 (または選択した項目)</span><span class="sxs-lookup"><span data-stu-id="c2a5b-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="c2a5b-139">**テーブル名**: salesorder</span><span class="sxs-lookup"><span data-stu-id="c2a5b-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="c2a5b-140">**Web サイト**: 顧客ポータル</span><span class="sxs-lookup"><span data-stu-id="c2a5b-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="c2a5b-141">**範囲**: 親</span><span class="sxs-lookup"><span data-stu-id="c2a5b-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="c2a5b-142">**特権**: すべて選択</span><span class="sxs-lookup"><span data-stu-id="c2a5b-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="c2a5b-143">**親テーブルのアクセス許可**: 当事者からアカウントへの接続</span><span class="sxs-lookup"><span data-stu-id="c2a5b-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

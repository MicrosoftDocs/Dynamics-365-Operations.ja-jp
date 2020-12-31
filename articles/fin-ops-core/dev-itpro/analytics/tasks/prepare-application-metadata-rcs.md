---
title: RCS で使用するアプリケーション メタデータを準備する
description: このトピックの手順では、Regulatory Configuration Service (RCS) の ER モデル マッピング コンフィギュレーションを設計するためのアプリケーションのメタデータを含む、新しい電子レポート (ER) コンフィギュレーションの作成方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dbc1ca45a39f2a5c3309276f9e2f5d2b7d2ba5f7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684094"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="8bb01-103">RCS で使用するアプリケーション メタデータを準備する</span><span class="sxs-lookup"><span data-stu-id="8bb01-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8bb01-104">次の手順では、システム管理者または電子報告開発者ロールのユーザーが、Regulatory Configuration Service (RCS) の ER モデル マッピング コンフィギュレーションを設計するためのアプリケーションのメタデータを含む、新しい電子レポート (ER) コンフィギュレーションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="8bb01-105">このコンフィギュレーションは、対外貿易トランザクションにアクセスするためのサンプル ER モデル マッピング コンフィギュレーションを設計するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8bb01-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="8bb01-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。これらの手順はすべての会社で実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8bb01-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="8bb01-107">これらの手順を完了するには、まず [コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) のトピックにある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb01-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8bb01-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="8bb01-108">Prerequisites</span></span>
1.    <span data-ttu-id="8bb01-109">**組織管理** > **ワークスペース** > **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="8bb01-110">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、**アクティブ** としてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="8bb01-111">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーを作成し、有効としてマークする](er-configuration-provider-mark-it-active-2016-11.md) という手順のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb01-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="8bb01-112">**メタデータ コンフィギュレーション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="8bb01-113">対外貿易ビジネスのドメインからの情報を含む電子ドキュメントを生成する Finance and Operation アプリケーションの ER ソリューションを設計するために RCS を使用することを想定しています。</span><span class="sxs-lookup"><span data-stu-id="8bb01-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="8bb01-114">ER データ モデルと必要なデータ ソース間のマッピングを指定するには、RCS で Finance and Operation アプリケーションのメタデータにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb01-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="8bb01-115">そのため、ER ソリューション設計の一部として、選択したビジネス ドメインに対する生成 ER レポートに現在必要とされるすべてのメタデータを含む、新しい ER メタデータ コンフィギュレーションを構成します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="8bb01-116">メタデータ コンフィギュレーションの追加</span><span class="sxs-lookup"><span data-stu-id="8bb01-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="8bb01-117">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8bb01-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="8bb01-118">**名前** フィールドに、「対外貿易メタデータ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="8bb01-119">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="8bb01-120">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="8bb01-121">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8bb01-122">アプリケーション全体、選択したモデル、または選択したモジュールのすべてのメタデータを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8bb01-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="8bb01-123">この場合、レコードのテーブル、列挙体、および拡張データ型のメタデータが自動的に追加されことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8bb01-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="8bb01-124">メタデータの追加のタイプが必要な場合、手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb01-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="8bb01-125">メタデータ項目を手動で選択することにより、一部の対外貿易トランザクションがメタデータに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="8bb01-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="8bb01-126">**データ ソースの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="8bb01-127">**テーブルのレコード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="8bb01-128">クイック フィルターを使用し、「Intrastat」の値で **名前** フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="8bb01-129">**イントラスタット** テーブル レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="8bb01-130">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-130">Click **OK**.</span></span>
  
<span data-ttu-id="8bb01-131">Intrastat のレコード テーブルに関するメタデータ情報を追加しました。</span><span class="sxs-lookup"><span data-stu-id="8bb01-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="8bb01-132">ツリーで、**テーブルのレコード Intrastat**\>**Relations** を展開します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="8bb01-133">ツリーで、**テーブルのレコード Intrastat**\>**Relations\IntrastatCommodity (テーブル レコード EcoResCategory)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="8bb01-134">**メタデータの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8bb01-135">選択したレコード テーブルに必要な関係に関するメタデータは、手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8bb01-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="8bb01-136">**データ ソースの追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="8bb01-137">**列挙** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="8bb01-138">クイック フィルターを使用し、「IntrastatDirection」の値で **名前** フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="8bb01-139">**IntrastatDirection の列挙** レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="8bb01-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="8bb01-140">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="8bb01-141">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="8bb01-142">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8bb01-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="8bb01-143">メタデータ コンフィギュレーションのドラフト バージョンの完了</span><span class="sxs-lookup"><span data-stu-id="8bb01-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="8bb01-144">**状態の変更** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="8bb01-145">**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="8bb01-146">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="8bb01-147">完了したバージョン **1** の選択</span><span class="sxs-lookup"><span data-stu-id="8bb01-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="8bb01-148">完了したバージョンのメタデータ コンフィギュレーションをアプリケーションから XML ファイルとしてエクスポートする</span><span class="sxs-lookup"><span data-stu-id="8bb01-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="8bb01-149">**交換** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="8bb01-150">**XML ファイルとしてエクスポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="8bb01-151">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8bb01-151">Click **OK**.</span></span> 
    
<span data-ttu-id="8bb01-152">作成された ER メタデータ コンフィギュレーションは、RCS にインポートすることができ、対外取引ビジネス ドメインのメタデータに関する情報のソースとして使用することのできる XML ファイルとして保存されています。</span><span class="sxs-lookup"><span data-stu-id="8bb01-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="8bb01-153">この情報に基づいて、アプリケーション メタデータと ER データ モデルとの間のマッピングを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="8bb01-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>

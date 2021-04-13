---
title: アプリケーション コネクタ
description: このトピックでは、Microsoft Power Automate およびロジック アプリのアプリケーション コネクタに関する情報を提供します。
author: Sunil-Garg
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: ''
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 9fb6a0cc4cbf8a6d837cc45579b05f496a5313f1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750552"
---
# <a name="application-connector"></a><span data-ttu-id="09cc9-103">アプリケーション コネクタ</span><span class="sxs-lookup"><span data-stu-id="09cc9-103">Application Connector</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="09cc9-104">アプリケーション コネクタを使用して Microsoft Power Automate、Power Apps、データ インテグレーター、および Logic Apps を Finance and Operations と統合できます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-104">The application connector allows Microsoft Power Automate, Power Apps, Data Integrator, and Logic Apps to integrate with Finance and Operations.</span></span> <span data-ttu-id="09cc9-105">外部アプリケーションは、有効なトリガーとアクションを使用することで、それらと統合することできます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-105">An external application can use the available trigger and actions to integrate with them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="09cc9-106">アプリケーション の コネクタ は Dynamics 365 Finance + Operations (オンプレミス) インスタンス との統合には使用できません。</span><span class="sxs-lookup"><span data-stu-id="09cc9-106">The Application Connector cannot be used for integrations with Dynamics 365 Finance + Operations (on-premises) instances.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="09cc9-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="09cc9-107">Prerequisites</span></span>
<span data-ttu-id="09cc9-108">先に進む前に、コネクタについて理解するための前提条件として、次のトピックをお読みください。</span><span class="sxs-lookup"><span data-stu-id="09cc9-108">We recommend that you read the following topics as a prerequisite to familiarize yourself with connectors before proceeding further</span></span>

- [<span data-ttu-id="09cc9-109">コネクタ</span><span class="sxs-lookup"><span data-stu-id="09cc9-109">Connectors</span></span>](https://docs.microsoft.com/connectors/) 
- [<span data-ttu-id="09cc9-110">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="09cc9-110">Data management package REST API</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api?toc=/fin-and-ops/toc.json)
- [<span data-ttu-id="09cc9-111">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="09cc9-111">Open Data Protocol (OData)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata?toc=/fin-and-ops/toc.json) 
- [<span data-ttu-id="09cc9-112">定期統合</span><span class="sxs-lookup"><span data-stu-id="09cc9-112">Recurring integrations</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/recurring-integrations?toc=/fin-and-ops/toc.json) 

## <a name="triggers"></a><span data-ttu-id="09cc9-113">トリガー</span><span class="sxs-lookup"><span data-stu-id="09cc9-113">Triggers</span></span>
<span data-ttu-id="09cc9-114">ビジネス イベントは、*ビジネス イベントが発生した場合* にトリガーを使用して公開されます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-114">Business events are exposed using the trigger *When a business event occurs*.</span></span> <span data-ttu-id="09cc9-115">ビジネス イベントに関する詳細については、[Microsoft Power Automate](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) のビジネス イベントおよび[ビジネス イベント](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="09cc9-115">For detailed information about business events, refer to [Business events in Microsoft Power Automate](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) and [Business events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page).</span></span>

## <a name="actions"></a><span data-ttu-id="09cc9-116">アクション</span><span class="sxs-lookup"><span data-stu-id="09cc9-116">Actions</span></span>

<span data-ttu-id="09cc9-117">このセクションでは、コネクタで使用できるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-117">This section describes the actions that are available in the connector.</span></span>

<span data-ttu-id="09cc9-118">**レコードの取得**</span><span class="sxs-lookup"><span data-stu-id="09cc9-118">**Get a record**</span></span>

<span data-ttu-id="09cc9-119">このアクションは、ターゲット インスタンスから特定のデータ エンティティのレコードをフェッチするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-119">This action can be used to fetch a record for a specific data entity from the target instance.</span></span>

<span data-ttu-id="09cc9-120">*インスタンス* は、コネクタが接続するアプリケーションのターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-120">*Instance* refers to the URL of the target instance of the application to which the connector must connect.</span></span> <span data-ttu-id="09cc9-121">予測値は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-121">The expected value is to enter the URL without the ‘https://’ prefix or choose one from the drop-down menu.</span></span> <span data-ttu-id="09cc9-122">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="09cc9-122">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="09cc9-123">*エンティティ名* は、レコードをフェッチする必要があるデータ エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-123">*Entity name* refers to the data entity from which the record must be fetched.</span></span> <span data-ttu-id="09cc9-124">ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-124">The drop-down menu shows the list of data entities from the target environment.</span></span>

<span data-ttu-id="09cc9-125">*オブジェクト ID* は、フェッチする必要のあるレコードを一意に識別するために指定する必要のある主キーのフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-125">*Object ID* refers to the primary keys fields that must be specified to uniquely identify the record that must be fetched.</span></span> <span data-ttu-id="09cc9-126">エンティティで定義されている順序で、コンマ区切りの値のリストとして値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="09cc9-126">The values must be specified as a comma-separated list of values in the order that is defined in the entity.</span></span>

<span data-ttu-id="09cc9-127">**レコードの作成**</span><span class="sxs-lookup"><span data-stu-id="09cc9-127">**Create a record**</span></span>

<span data-ttu-id="09cc9-128">このアクションを使用して、データ エンティティのデータ レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-128">This action can be used to create data records for a data entity.</span></span>

<span data-ttu-id="09cc9-129">*インスタンス* は、コネクタが接続するターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-129">*Instance* refers to the URL of the target instance to which the connector must connect.</span></span> <span data-ttu-id="09cc9-130">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-130">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="09cc9-131">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="09cc9-131">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="09cc9-132">*エンティティ名* は、レコードを作成する必要があるデータ エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-132">*Entity name* refers to the data entity in which the record must be created.</span></span> <span data-ttu-id="09cc9-133">ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-133">The dropdown menu shows the list of data entities from the target environment.</span></span>

<span data-ttu-id="09cc9-134">表示されるフィールドの一覧は、選択したデータ エンティティに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="09cc9-134">Based on the selected data entity, the list of fields displayed will be vary.</span></span>

<span data-ttu-id="09cc9-135">**レコードの更新**</span><span class="sxs-lookup"><span data-stu-id="09cc9-135">**Update a record**</span></span>

<span data-ttu-id="09cc9-136">このアクションを使用して、データ エンティティの既存のデータ レコードを更新できます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-136">This action can be used to update an existing data record for a data entity.</span></span> <span data-ttu-id="09cc9-137">使用方法は、レコード アクションの作成と同じです。</span><span class="sxs-lookup"><span data-stu-id="09cc9-137">The usage is the same as the create a record action.</span></span>

<span data-ttu-id="09cc9-138">**レコードの削除**</span><span class="sxs-lookup"><span data-stu-id="09cc9-138">**Delete a record**</span></span>

<span data-ttu-id="09cc9-139">このアクションを使用して、データ エンティティの既存のデータ レコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-139">This action can be used to delete an existing data record for a data entity.</span></span> <span data-ttu-id="09cc9-140">使用方法は、レコード アクションの取得と同じです。</span><span class="sxs-lookup"><span data-stu-id="09cc9-140">The usage is the same as the get a record action.</span></span>

<span data-ttu-id="09cc9-141">**アクションの実行**</span><span class="sxs-lookup"><span data-stu-id="09cc9-141">**Execute action**</span></span>

<span data-ttu-id="09cc9-142">このアクションを使用して、ビジネス アクションを実行するメソッドをデータ エンティティ上で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-142">This action can be used to invoke methods on a data entity to perform a business action.</span></span>

<span data-ttu-id="09cc9-143">*インスタンス* は、コネクタが接続するターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-143">*Instance* refers to the URL of the target instance to which the connector must connect.</span></span> <span data-ttu-id="09cc9-144">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-144">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="09cc9-145">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="09cc9-145">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="09cc9-146">*アクション* は、実行する必要があるデータ エンティティ上のメソッドを参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-146">*Action* refers to the method on the data entity that must be executed.</span></span> <span data-ttu-id="09cc9-147">表示されるフィールドの一覧は、選択したメソッドに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="09cc9-147">Based on the selected method, the list of fields displayed will be vary.</span></span> <span data-ttu-id="09cc9-148">これらのフィールドは、選択したメソッドのパラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-148">These fields represent the parameters for the selected method.</span></span>

<span data-ttu-id="09cc9-149">**エンティティの一覧を取得する**</span><span class="sxs-lookup"><span data-stu-id="09cc9-149">**Get list of entities**</span></span>

<span data-ttu-id="09cc9-150">このアクションを使用してエンティティの一覧を取得し、開発中のアプリで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-150">This action can be used to get the list of entities for further use in the app that is being developed.</span></span>

<span data-ttu-id="09cc9-151">*インスタンス* は、コネクタが接続するターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-151">*Instance* refers to the URL of the target instance to which the connector must connect.</span></span> <span data-ttu-id="09cc9-152">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="09cc9-152">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="09cc9-153">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="09cc9-153">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="09cc9-154">**テーブルに存在するリスト項目**</span><span class="sxs-lookup"><span data-stu-id="09cc9-154">**List items present in the table**</span></span>

<span data-ttu-id="09cc9-155">このアクションは、エンティティからレコードの一覧を取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="09cc9-155">This action can be used to get the list of records from an entity.</span></span> <span data-ttu-id="09cc9-156">このアクションは、会社間でのデータの読み取りをサポートします。</span><span class="sxs-lookup"><span data-stu-id="09cc9-156">This action supports cross-company reading of data.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: アプリケーション コネクタ
description: このトピックでは、Microsoft Power Automate およびロジック アプリのアプリケーション コネクタに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: ''
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 3d3b14aa6fa9e70a16dd7626481bd04da363020b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769624"
---
# <a name="application-connector"></a><span data-ttu-id="0c28d-103">アプリケーション コネクタ</span><span class="sxs-lookup"><span data-stu-id="0c28d-103">Application Connector</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0c28d-104">アプリケーション コネクタを使用して Microsoft Power Automate、 Power Apps、データ インテグレーター、およびロジック アプリを Finance and Operations と統合できます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-104">The application connector allows Microsoft Power Automate, Power Apps, Data Integrator, and Logic Apps to integrate with Finance and Operations.</span></span> <span data-ttu-id="0c28d-105">外部アプリケーションは、有効なトリガーとアクションを使用することで、それらと統合することできます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-105">An external application can use the available trigger and actions to integrate with them.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0c28d-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="0c28d-106">Prerequisites</span></span>
<span data-ttu-id="0c28d-107">先に進む前に、コネクタについて理解するための前提条件として、次のトピックをお読みください。</span><span class="sxs-lookup"><span data-stu-id="0c28d-107">We recommend that you read the following topics as a prerequisite to familiarize yourself with connectors before proceeding further</span></span>

- [<span data-ttu-id="0c28d-108">コネクタ</span><span class="sxs-lookup"><span data-stu-id="0c28d-108">Connectors</span></span>](https://docs.microsoft.com/connectors/) 
- [<span data-ttu-id="0c28d-109">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="0c28d-109">Data management package REST API</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api?toc=/fin-and-ops/toc.json)
- [<span data-ttu-id="0c28d-110">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="0c28d-110">Open Data Protocol (OData)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata?toc=/fin-and-ops/toc.json) 
- [<span data-ttu-id="0c28d-111">定期統合</span><span class="sxs-lookup"><span data-stu-id="0c28d-111">Recurring integrations</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/recurring-integrations?toc=/fin-and-ops/toc.json) 

## <a name="triggers"></a><span data-ttu-id="0c28d-112">トリガー</span><span class="sxs-lookup"><span data-stu-id="0c28d-112">Triggers</span></span>
<span data-ttu-id="0c28d-113">ビジネス イベントは、*ビジネス イベントが発生した場合*にトリガーを使用して公開されます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-113">Business events are exposed using the trigger *When a business event occurs*.</span></span> <span data-ttu-id="0c28d-114">ビジネス イベントに関する詳細については、 [Microsoft Power Automate のビジネス イベント](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) および [ビジネス イベント](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c28d-114">For detailed information about business events, refer to [Business events in Microsoft Power Automate](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) and [Business events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page).</span></span>

## <a name="actions"></a><span data-ttu-id="0c28d-115">アクション</span><span class="sxs-lookup"><span data-stu-id="0c28d-115">Actions</span></span>

<span data-ttu-id="0c28d-116">このセクションでは、コネクタで使用できるアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-116">This section describes the actions that are available in the connector.</span></span>

<span data-ttu-id="0c28d-117">**レコードの取得**</span><span class="sxs-lookup"><span data-stu-id="0c28d-117">**Get a record**</span></span>

<span data-ttu-id="0c28d-118">このアクションは、ターゲット インスタンスから特定のデータ エンティティのレコードをフェッチするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-118">This action can be used to fetch a record for a specific data entity from the target instance.</span></span>

<span data-ttu-id="0c28d-119">*インスタンス*は、コネクタが接続するアプリケーションのターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-119">*Instance* refers to the URL of the target instance of the application to which the connector must connect.</span></span> <span data-ttu-id="0c28d-120">予測値は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-120">The expected value is to enter the URL without the ‘https://’ prefix or choose one from the drop-down menu.</span></span> <span data-ttu-id="0c28d-121">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="0c28d-121">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="0c28d-122">*エンティティ名*は、レコードをフェッチする必要があるデータ エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-122">*Entity name* refers to the data entity from which the record must be fetched.</span></span> <span data-ttu-id="0c28d-123">ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-123">The drop-down menu shows the list of data entities from the target environment.</span></span>

<span data-ttu-id="0c28d-124">*オブジェクト ID* は、フェッチする必要のあるレコードを一意に識別するために指定する必要のある主キーのフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-124">*Object ID* refers to the primary keys fields that must be specified to uniquely identify the record that must be fetched.</span></span> <span data-ttu-id="0c28d-125">エンティティで定義されている順序で、コンマ区切りの値のリストとして値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c28d-125">The values must be specified as a comma-separated list of values in the order that is defined in the entity.</span></span>

<span data-ttu-id="0c28d-126">**レコードの作成**</span><span class="sxs-lookup"><span data-stu-id="0c28d-126">**Create a record**</span></span>

<span data-ttu-id="0c28d-127">このアクションを使用して、データ エンティティのデータ レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-127">This action can be used to create data records for a data entity.</span></span>

<span data-ttu-id="0c28d-128">*インスタンス*は、コネクタが接続するターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-128">*Instance* refers to the URL of the target instance to which the connector must connect.</span></span> <span data-ttu-id="0c28d-129">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-129">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="0c28d-130">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="0c28d-130">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="0c28d-131">*エンティティ名*は、レコードを作成する必要があるデータ エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-131">*Entity name* refers to the data entity in which the record must be created.</span></span> <span data-ttu-id="0c28d-132">ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-132">The dropdown menu shows the list of data entities from the target environment.</span></span>

<span data-ttu-id="0c28d-133">表示されるフィールドの一覧は、選択したデータ エンティティに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="0c28d-133">Based on the selected data entity, the list of fields displayed will be vary.</span></span>

<span data-ttu-id="0c28d-134">**レコードの更新**</span><span class="sxs-lookup"><span data-stu-id="0c28d-134">**Update a record**</span></span>

<span data-ttu-id="0c28d-135">このアクションを使用して、データ エンティティの既存のデータ レコードを更新できます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-135">This action can be used to update an existing data record for a data entity.</span></span> <span data-ttu-id="0c28d-136">使用方法は、レコード アクションの作成と同じです。</span><span class="sxs-lookup"><span data-stu-id="0c28d-136">The usage is the same as the create a record action.</span></span>

<span data-ttu-id="0c28d-137">**レコードの削除**</span><span class="sxs-lookup"><span data-stu-id="0c28d-137">**Delete a record**</span></span>

<span data-ttu-id="0c28d-138">このアクションを使用して、データ エンティティの既存のデータ レコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-138">This action can be used to delete an existing data record for a data entity.</span></span> <span data-ttu-id="0c28d-139">使用方法は、レコード アクションの取得と同じです。</span><span class="sxs-lookup"><span data-stu-id="0c28d-139">The usage is the same as the get a record action.</span></span>

<span data-ttu-id="0c28d-140">**アクションの実行**</span><span class="sxs-lookup"><span data-stu-id="0c28d-140">**Execute action**</span></span>

<span data-ttu-id="0c28d-141">このアクションを使用して、ビジネス アクションを実行するメソッドをデータ エンティティ上で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-141">This action can be used to invoke methods on a data entity to perform a business action.</span></span>

<span data-ttu-id="0c28d-142">*インスタンス*は、コネクタが接続するターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-142">*Instance* refers to the URL of the target instance to which the connector must connect.</span></span> <span data-ttu-id="0c28d-143">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-143">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="0c28d-144">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="0c28d-144">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

<span data-ttu-id="0c28d-145">*アクション*は、実行する必要があるデータ エンティティ上のメソッドを参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-145">*Action* refers to the method on the data entity that must be executed.</span></span> <span data-ttu-id="0c28d-146">表示されるフィールドの一覧は、選択したメソッドに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="0c28d-146">Based on the selected method, the list of fields displayed will be vary.</span></span> <span data-ttu-id="0c28d-147">これらのフィールドは、選択したメソッドのパラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-147">These fields represent the parameters for the selected method.</span></span>

<span data-ttu-id="0c28d-148">**エンティティの一覧を取得する**</span><span class="sxs-lookup"><span data-stu-id="0c28d-148">**Get list of entities**</span></span>

<span data-ttu-id="0c28d-149">このアクションを使用してエンティティの一覧を取得し、開発中のアプリで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0c28d-149">This action can be used to get the list of entities for further use in the app that is being developed.</span></span>

<span data-ttu-id="0c28d-150">*インスタンス*は、コネクタが接続するターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-150">*Instance* refers to the URL of the target instance to which the connector must connect.</span></span> <span data-ttu-id="0c28d-151">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="0c28d-151">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="0c28d-152">これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="0c28d-152">This lists of all the environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Power Automate, Power Apps, or Logic App.</span></span>

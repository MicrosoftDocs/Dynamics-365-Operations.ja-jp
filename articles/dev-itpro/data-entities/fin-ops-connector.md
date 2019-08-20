---
title: Finance and Operations コネクタ
description: このトピックでは、Finance and Operations Connector for Microsoft Flow およびロジック アプリの情報を提供します。
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
ms.openlocfilehash: e6a9318ed86ce2dce5887726c1065949b0bf4169
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862924"
---
# <a name="finance-and-operations-connector"></a><span data-ttu-id="217bc-103">Finance and Operations コネクタ</span><span class="sxs-lookup"><span data-stu-id="217bc-103">Finance and Operations Connector</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="217bc-104">Dynamics 365 for Finance and Operations Connector を使用して Microsoft Flow、PowerApps、データ インテグレーター、およびロジック アプリを Dynamics 365 for Finance and Operations のインスタンスと統合できます。</span><span class="sxs-lookup"><span data-stu-id="217bc-104">The Dynamics 365 for Finance and Operations connector allows Microsoft Flow, PowerApps, Data Integrator, and Logic Apps to integrate with an instance of Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="217bc-105">外部アプリケーションは、有効なトリガーとアクションを使用することで、Finance and Operations と統合することできます。</span><span class="sxs-lookup"><span data-stu-id="217bc-105">An external application can use the available trigger and actions to integrate with Finance and Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="217bc-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="217bc-106">Prerequisites</span></span>
<span data-ttu-id="217bc-107">先に進む前に、コネクタについて理解するための前提条件として、次のトピックをお読みください。</span><span class="sxs-lookup"><span data-stu-id="217bc-107">We recommend that you read the following topics as a prerequisite to familiarize yourself with connectors before proceeding further</span></span>

- [<span data-ttu-id="217bc-108">コネクタ</span><span class="sxs-lookup"><span data-stu-id="217bc-108">Connectors</span></span>](https://docs.microsoft.com/connectors/) 
- [<span data-ttu-id="217bc-109">データ管理パッケージ REST API</span><span class="sxs-lookup"><span data-stu-id="217bc-109">Data management package REST API</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api?toc=/fin-and-ops/toc.json)
- [<span data-ttu-id="217bc-110">データ プロトコル (OData) を開く</span><span class="sxs-lookup"><span data-stu-id="217bc-110">Open Data Protocol (OData)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/odata?toc=/fin-and-ops/toc.json) 
- [<span data-ttu-id="217bc-111">定期統合</span><span class="sxs-lookup"><span data-stu-id="217bc-111">Recurring integrations</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/recurring-integrations?toc=/fin-and-ops/toc.json) 

## <a name="triggers"></a><span data-ttu-id="217bc-112">トリガー</span><span class="sxs-lookup"><span data-stu-id="217bc-112">Triggers</span></span>
<span data-ttu-id="217bc-113">Finance and Operations のビジネス イベントは、*ビジネス イベントが発生した場合*にトリガーを使用して公開されます。</span><span class="sxs-lookup"><span data-stu-id="217bc-113">Business events in Finance and Operations are exposed using the trigger *When a business event occurs*.</span></span> <span data-ttu-id="217bc-114">ビジネス イベントに関する詳細については、[Microsoft Flow](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) のビジネス イベントおよび[ビジネス イベント](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="217bc-114">For detailed information about business events, refer to [Business events in Microsoft Flow](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) and [Business events](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/home-page).</span></span>

## <a name="actions"></a><span data-ttu-id="217bc-115">アクション</span><span class="sxs-lookup"><span data-stu-id="217bc-115">Actions</span></span>

<span data-ttu-id="217bc-116">このセクションでは、Dynamics 365 for Finance and Operations Connector で使用できりうアクションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="217bc-116">This section describes the actions that are available in the Dynamics 365 for Finance and Operations connector.</span></span>

<span data-ttu-id="217bc-117">**レコードの取得**</span><span class="sxs-lookup"><span data-stu-id="217bc-117">**Get a record**</span></span>

<span data-ttu-id="217bc-118">このアクションを使用して、Finance and Operations のターゲット インスタンスから特定のデータ エンティティのレコードをフェッチできます。</span><span class="sxs-lookup"><span data-stu-id="217bc-118">This action can be used to fetch a record for a specific data entity from the target instance of Finance and Operations.</span></span>

<span data-ttu-id="217bc-119">*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-119">*Instance* refers to the URL of the target instance of Dynamics 365 for Finance and Operations to which the connector must connect.</span></span> <span data-ttu-id="217bc-120">予測値は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="217bc-120">The expected value is to enter the URL without the ‘https://’ prefix or choose one from the drop-down menu.</span></span> <span data-ttu-id="217bc-121">これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="217bc-121">This lists of all the Finance and Operations environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Microsoft Flow, PowerApps, or Logic App.</span></span>

<span data-ttu-id="217bc-122">*エンティティ名前*は、レコードをフェッチする必要がある Finance and Operations 内のデータ エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-122">*Entity name* refers to the data entity in Finance and Operations from which the record must be fetched.</span></span> <span data-ttu-id="217bc-123">ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="217bc-123">The drop-down menu shows the list of data entities from the target environment.</span></span>

<span data-ttu-id="217bc-124">*オブジェクト ID* は、フェッチする必要のあるレコードを一意に識別するために指定する必要のある主キーのフィールドを参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-124">*Object ID* refers to the primary keys fields that must be specified to uniquely identify the record that must be fetched.</span></span> <span data-ttu-id="217bc-125">エンティティで定義されている順序で、コンマ区切りの値のリストとして値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="217bc-125">The values must be specified as a comma-separated list of values in the order that is defined in the entity.</span></span>

<span data-ttu-id="217bc-126">**レコードの作成**</span><span class="sxs-lookup"><span data-stu-id="217bc-126">**Create a record**</span></span>

<span data-ttu-id="217bc-127">このアクションを使用して、データ エンティティのデータ レコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="217bc-127">This action can be used to create data records for a data entity.</span></span>

<span data-ttu-id="217bc-128">*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-128">*Instance* refers to the URL of the target instance of Dynamics 365 for Finance and Operations to which the connector must connect.</span></span> <span data-ttu-id="217bc-129">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="217bc-129">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="217bc-130">これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="217bc-130">This lists of all the Finance and Operations environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Microsoft Flow, PowerApps, or Logic App.</span></span>

<span data-ttu-id="217bc-131">*エンティティ名前*は、レコードを作成する必要がある Finance and Operations 内のデータ エンティティを参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-131">*Entity name* refers to the data entity in Finance and Operations in which the record must be created.</span></span> <span data-ttu-id="217bc-132">ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="217bc-132">The dropdown menu shows the list of data entities from the target environment.</span></span>

<span data-ttu-id="217bc-133">表示されるフィールドの一覧は、選択したデータ エンティティに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="217bc-133">Based on the selected data entity, the list of fields displayed will be vary.</span></span>

<span data-ttu-id="217bc-134">**レコードの更新**</span><span class="sxs-lookup"><span data-stu-id="217bc-134">**Update a record**</span></span>

<span data-ttu-id="217bc-135">このアクションを使用して、データ エンティティの既存のデータ レコードを更新できます。</span><span class="sxs-lookup"><span data-stu-id="217bc-135">This action can be used to update an existing data record for a data entity.</span></span> <span data-ttu-id="217bc-136">使用方法は、レコード アクションの作成と同じです。</span><span class="sxs-lookup"><span data-stu-id="217bc-136">The usage is the same as the create a record action.</span></span>

<span data-ttu-id="217bc-137">**レコードの削除**</span><span class="sxs-lookup"><span data-stu-id="217bc-137">**Delete a record**</span></span>

<span data-ttu-id="217bc-138">このアクションを使用して、データ エンティティの既存のデータ レコードを削除できます。</span><span class="sxs-lookup"><span data-stu-id="217bc-138">This action can be used to delete an existing data record for a data entity.</span></span> <span data-ttu-id="217bc-139">使用方法は、レコード アクションの取得と同じです。</span><span class="sxs-lookup"><span data-stu-id="217bc-139">The usage is the same as the get a record action.</span></span>

<span data-ttu-id="217bc-140">**アクションの実行**</span><span class="sxs-lookup"><span data-stu-id="217bc-140">**Execute action**</span></span>

<span data-ttu-id="217bc-141">このアクションを使用して、ビジネス アクションを実行するメソッドをデータ エンティティ上で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="217bc-141">This action can be used to invoke methods on a data entity to perform a business action.</span></span>

<span data-ttu-id="217bc-142">*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-142">*Instance* refers to the URL of the target instance of Dynamics 365 for Finance and Operations to which the connector must connect.</span></span> <span data-ttu-id="217bc-143">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="217bc-143">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="217bc-144">これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="217bc-144">This lists of all the Finance and Operations environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Microsoft Flow, PowerApps, or Logic App.</span></span>

<span data-ttu-id="217bc-145">*アクション*は、Finance and Operations で実行する必要があるデータ エンティティ上のメソッドを参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-145">*Action* refers to the method on the data entity that must be executed in Finance and Operations.</span></span> <span data-ttu-id="217bc-146">表示されるフィールドの一覧は、選択したメソッドに基づいて異なります。</span><span class="sxs-lookup"><span data-stu-id="217bc-146">Based on the selected method, the list of fields displayed will be vary.</span></span> <span data-ttu-id="217bc-147">これらのフィールドは、選択したメソッドのパラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="217bc-147">These fields represent the parameters for the selected method.</span></span>

<span data-ttu-id="217bc-148">**エンティティの一覧を取得する**</span><span class="sxs-lookup"><span data-stu-id="217bc-148">**Get list of entities**</span></span>

<span data-ttu-id="217bc-149">このアクションを使用してエンティティの一覧を取得し、開発中のアプリで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="217bc-149">This action can be used to get the list of entities for further use in the app that is being developed.</span></span>

<span data-ttu-id="217bc-150">*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。</span><span class="sxs-lookup"><span data-stu-id="217bc-150">*Instance* refers to the URL of the target instance of Dynamics 365 for Finance and Operations to which the connector must connect.</span></span> <span data-ttu-id="217bc-151">この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="217bc-151">The syntax for this value is to enter the URL without the ‘https://’ prefix or choose one from the drop- menu.</span></span> <span data-ttu-id="217bc-152">これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。</span><span class="sxs-lookup"><span data-stu-id="217bc-152">This lists of all the Finance and Operations environments that are deployed in the Azure Active Directory tenant for the user account that was used to sign in to the specific client like Microsoft Flow, PowerApps, or Logic App.</span></span>

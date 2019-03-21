---
title: ビジネス イベント
description: このトピックは、外部システムが Dynamics 365 for Finance and Operations から通知を受信するためのメカニズムを提供するビジネス イベントに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: b1d2e78cde1f68706603d464cda4e4eeae7ec963
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "777215"
---
# <a name="business-events"></a><span data-ttu-id="3ce17-103">ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="3ce17-103">Business events</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3ce17-104">ビジネス イベントは外部システムが Microsoft Dynamics 365 for Finance and Operations から通知を受信するメカニズムを提供します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-104">Business events provide a mechanism that lets external systems receive notifications from Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3ce17-105">これにより、システムは、ビジネス イベントに対してビジネス アクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-105">In this way, the systems can perform business actions in response to the business events.</span></span>

<span data-ttu-id="3ce17-106">ビジネス プロセスの実行時に、ビジネス イベントが発生します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-106">Business events occur when a business process is run.</span></span> <span data-ttu-id="3ce17-107">ビジネス プロセス中には、それに参加するユーザーは、ビジネス プロセスを構成するタスクを完了するビジネス アクションを実行します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-107">During a business process, users who participate in it perform business actions to complete the tasks that make up the business process.</span></span> 

<span data-ttu-id="3ce17-108">Finance and Operations では、ユーザーが実行するビジネス アクションは、ワークフロー アクションまたは非ワークフロー アクションのいずれかにすることを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-108">In Finance and Operations, a business action that a user performs can be either a workflow action or a non-workflow action.</span></span> <span data-ttu-id="3ce17-109">購買要求の承認はワークフロー アクションの例で、発注書の確認は非ワークフロー アクションの例です。</span><span class="sxs-lookup"><span data-stu-id="3ce17-109">Approval of a purchase requisition is an example of a workflow action, whereas confirmation of a purchase order is an example of a non-workflow action.</span></span> <span data-ttu-id="3ce17-110">どちらのタイプのアクションも、統合および通知のシナリオで、外部システムが使用できるビジネス イベントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-110">Both types of actions can generate business events that external systems can use in integration and notification scenarios.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="3ce17-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="3ce17-111">Prerequisites</span></span>

- <span data-ttu-id="3ce17-112">ビジネス イベントは Microsoft Flow およびAzureメッセージング サービス経由で利用できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-112">Business events can be consumed via Microsoft Flow and Azure messaging services.</span></span> <span data-ttu-id="3ce17-113">したがって、ビジネス イベントを使用するには、顧客がこのようなアセットのサブスクリプションを契約している必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-113">Therefore, customers must bring their subscriptions to such asset(s) to use business events.</span></span>
- <span data-ttu-id="3ce17-114">ビジネス イベントは、Platform 更新プログラム 24 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-114">Business events are available in Platform update 24 and later.</span></span> <span data-ttu-id="3ce17-115">そのため、少なくともPlatform 更新プログラム 24 が必要です。</span><span class="sxs-lookup"><span data-stu-id="3ce17-115">Therefore, at least Platform update 24 is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ce17-116">ビジネス イベントを Finance and Operations からデータをエクスポートするためのメカニズムと考えることはできません。</span><span class="sxs-lookup"><span data-stu-id="3ce17-116">Business events must not be considered a mechanism for exporting data out of Finance and Operations.</span></span> <span data-ttu-id="3ce17-117">定義上は、ビジネス イベントは簡易で軽快であることになっています。</span><span class="sxs-lookup"><span data-stu-id="3ce17-117">By definition, business events are supposed to be lightweight and nimble.</span></span> <span data-ttu-id="3ce17-118">データ エクスポートのシナリオを実行するために大量のペイロードを搭載することは想定していません。</span><span class="sxs-lookup"><span data-stu-id="3ce17-118">They aren't intended to carry large payloads to fulfill data export scenarios.</span></span>

## <a name="enabling-business-events"></a><span data-ttu-id="3ce17-119">ビジネス イベントの有効化</span><span class="sxs-lookup"><span data-stu-id="3ce17-119">Enabling business events</span></span>

<span data-ttu-id="3ce17-120">既定では、ビジネス イベント機能は無効になっています。</span><span class="sxs-lookup"><span data-stu-id="3ce17-120">By default, the business event functionality is turned off.</span></span> <span data-ttu-id="3ce17-121">有効にするには、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="3ce17-121">To turn it on, follow one of these steps.</span></span>

- <span data-ttu-id="3ce17-122">非実稼働環境では、次のSQLステートメントを実行してBusinessEventsMaster フライトを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3ce17-122">In non-production environments, turn on the BusinessEventsMaster flight by running the following SQL statement</span></span>

    ```
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, FLIGHTSERVICEID) VALUES ('BusinessEventsMaster', 1, 12719367)
    ```

- <span data-ttu-id="3ce17-123">この SQL ステートメントを実行した後、各 AOS 上の web.config ファイル内に、以下が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-123">After running the SQL statement, ensure that the following is set in the web.config file on each of the AOS's.</span></span> <span data-ttu-id="3ce17-124">key="DataAccess.FlightingServiceCatalogID" value="12719367"</span><span class="sxs-lookup"><span data-stu-id="3ce17-124">key="DataAccess.FlightingServiceCatalogID" value="12719367"</span></span>

- <span data-ttu-id="3ce17-125">IISRESETの実行</span><span class="sxs-lookup"><span data-stu-id="3ce17-125">Perform an IISRESET</span></span>

- <span data-ttu-id="3ce17-126">実稼動環境では、Microsoft でサポート ケースを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-126">In production environments, you must create a support case with Microsoft.</span></span>

## <a name="business-events-that-are-implemented-in-finance-and-operations"></a><span data-ttu-id="3ce17-127">Finance and Operationsに実装されているビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="3ce17-127">Business events that are implemented in Finance and Operations</span></span>

<span data-ttu-id="3ce17-128">Finance and Operations では、ビジネス イベントは、最初から用意されているいくつかのビジネス プロセスに実装されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-128">In Finance and Operations, business events are implemented in some business processes out of the box.</span></span> <span data-ttu-id="3ce17-129">これらのビジネス イベントには、ワークフローおよび非ワークフロー ビジネス イベントの両方が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-129">These business events include both workflow and non-workflow business events.</span></span> <span data-ttu-id="3ce17-130">詳細については、「[アプリケーションのビジネス イベント](app-business-events.md)」および「[ワークフロー ビジネス イベント](business-events-workflow.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ce17-130">For more information, see [Application business events](app-business-events.md) and [Workflow business events](business-events-workflow.md).</span></span>

<span data-ttu-id="3ce17-131">開発者は、拡張機能を使用して、新しいビジネス イベントを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-131">A developer must use extensions to implement new business events.</span></span> <span data-ttu-id="3ce17-132">詳細については、「[ビジネス イベント開発者ドキュメント](business-events-dev-doc.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ce17-132">For more information, see [Business events developer documentation](business-events-dev-doc.md).</span></span>

## <a name="business-event-catalog"></a><span data-ttu-id="3ce17-133">ビジネス イベント カタログ</span><span class="sxs-lookup"><span data-stu-id="3ce17-133">Business event catalog</span></span>

<span data-ttu-id="3ce17-134">ビジネス イベント カタログには、使用している Finance and Operations のインスタンスで使用できるビジネス イベントが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-134">The business event catalog lists the business events that are available in the instance of Finance and Operations that you're using.</span></span> <span data-ttu-id="3ce17-135">カタログは、どのビジネス イベントが使用可能かを示し、カテゴリ、ビジネス イベントのIDおよび名前でフィルタ処理することができるため、便利です。</span><span class="sxs-lookup"><span data-stu-id="3ce17-135">The catalog is useful because it shows which business events are available, and you can filter it by category, business event ID, and name.</span></span>

<span data-ttu-id="3ce17-136">ビジネス イベントのカテゴリは、Finance and Operationsにおいて、そのソースを識別します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-136">The category of a business event identifies its source in Finance and Operations.</span></span> <span data-ttu-id="3ce17-137">ワークフロー システムから生成されたビジネス イベントは、**ワークフロー** カテゴリに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-137">Business events that originate from the workflow system are assigned to the **Workflow** category.</span></span> <span data-ttu-id="3ce17-138">他のモジュールから生成されたビジネス イベントについては、モジュール名はカテゴリ名として使用されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-138">For business events that originate from other modules, the module name is used as the category name.</span></span> 

<span data-ttu-id="3ce17-139">ビジネス イベント カタログは、配置時のデータベースの同期中に作成されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-139">The business event catalog is built during database synchronization at the time of deployment.</span></span> <span data-ttu-id="3ce17-140">したがって、ユーザーは、カタログでビジネス イベントの完全な一覧を確認することになります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-140">Therefore, users should see the complete list of business events in the catalog.</span></span> <span data-ttu-id="3ce17-141">ただし、カタログの明示的な更新が必要な場合は、**管理 \> 再構築ビジネス イベント カタログ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-141">However, if an explicit update of the catalog is required, you can select **Manage \> Rebuild business events catalog**.</span></span>

![ビジネス イベント カタログ](../media/businesseventscatalog.png)

<span data-ttu-id="3ce17-143">各ビジネス イベントについて、ビジネス イベント カタログは説明を表示します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-143">For each business event, the business event catalog shows a description.</span></span> <span data-ttu-id="3ce17-144">この説明は、ビジネス イベントおよびビジネス プロセス内のコンテキストを理解するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-144">This description can help you better understand the business event and its context in the business process.</span></span> <span data-ttu-id="3ce17-145">カタログには、イベントに送信されるデータ フィールドの一覧も表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-145">The catalog also shows the list of data fields that will be sent out in the event.</span></span>

<span data-ttu-id="3ce17-146">外部の統合システムが開発中にビジネス イベントのペイロードのスキーマを必要とする場合、**ダウンロード スキーマ**を選択して JavaScript Object Notation (JSON) スキーマをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="3ce17-146">In scenarios where external integration systems require the schema of the payload for a business event during development, you can select **Download schema** to download the JavaScript Object Notation (JSON) schema.</span></span>

<span data-ttu-id="3ce17-147">簡単に言うと、ビジネス イベント カタログは、実装に必要なビジネス イベントを識別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-147">In summary, the business event catalog helps identify the business events that are required for an implementation.</span></span> <span data-ttu-id="3ce17-148">各ビジネス イベントのスキーマを識別することもできます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-148">It also helps identify the schema for each business event.</span></span>

<span data-ttu-id="3ce17-149">次のステップでは、エンドポイントを管理します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-149">The next step is to manage the endpoints.</span></span>

## <a name="managing-endpoints"></a><span data-ttu-id="3ce17-150">エンドポイントの管理</span><span class="sxs-lookup"><span data-stu-id="3ce17-150">Managing endpoints</span></span>

<span data-ttu-id="3ce17-151">エンドポイントを使用して、Finance and Operations がビジネス イベントを送る必要がある宛先を管理できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-151">Endpoints let you manage the destinations that Finance and Operations must send business events to.</span></span> <span data-ttu-id="3ce17-152">次のタイプのエンドポイントが現在サポートされています。</span><span class="sxs-lookup"><span data-stu-id="3ce17-152">The following types of endpoints are currently supported.</span></span> <span data-ttu-id="3ce17-153">したがって、すぐにこれらのメッセージングおよびイベント ブローカーのエンドポイントを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-153">Therefore, endpoints can be created for these messaging and event brokers out of the box.</span></span>

- <span data-ttu-id="3ce17-154">Azure Service Bus キュー</span><span class="sxs-lookup"><span data-stu-id="3ce17-154">Azure Service Bus Queue</span></span>
- <span data-ttu-id="3ce17-155">Azure Service Bus トピック</span><span class="sxs-lookup"><span data-stu-id="3ce17-155">Azure Service Bus Topic</span></span>
- <span data-ttu-id="3ce17-156">Azure Event Grid</span><span class="sxs-lookup"><span data-stu-id="3ce17-156">Azure Event Grid</span></span>
- <span data-ttu-id="3ce17-157">Azure イベント ハブ</span><span class="sxs-lookup"><span data-stu-id="3ce17-157">Azure Event Hub</span></span>
- <span data-ttu-id="3ce17-158">HTTPS</span><span class="sxs-lookup"><span data-stu-id="3ce17-158">HTTPS</span></span>
- <span data-ttu-id="3ce17-159">Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="3ce17-159">Microsoft Flow</span></span>

<span data-ttu-id="3ce17-160">消費者にビジネス イベントを組織化して配布するため、複数のエンドポイントが必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-160">Some scenarios might require multiple endpoints for organized distribution of business events to consumers.</span></span> <span data-ttu-id="3ce17-161">このようなシナリオをサポートするため、複数のエンドポイントを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-161">You can create multiple endpoints to support these scenarios.</span></span>

<span data-ttu-id="3ce17-162">Azure ベースのエンドポイントは、顧客の Azure サブスクリプションに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-162">The Azure-based endpoints must be in the customer's Azure subscription.</span></span> <span data-ttu-id="3ce17-163">たとえば、イベント グリッドをエンドポイントとして使用する場合は、エンドポイントが顧客の Azure サブスクリプションに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-163">For example, if Event Grid is used as an endpoint, the endpoint must be in the customer's Azure subscription.</span></span>

<span data-ttu-id="3ce17-164">Finance and Operations はエンドポイントを提供しません。</span><span class="sxs-lookup"><span data-stu-id="3ce17-164">Finance and Operations doesn't provision the endpoints.</span></span> <span data-ttu-id="3ce17-165">用意されているイベントをエンドポイントに送信するだけです。</span><span class="sxs-lookup"><span data-stu-id="3ce17-165">It just sends events to the endpoints that are provided.</span></span> <span data-ttu-id="3ce17-166">顧客が Azure サブスクリプションでこれらのエンドポイントを使用している場合、追加費用が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-166">Customer might incur additional costs if they use these endpoints in their Azure subscription.</span></span>

![ビジネス イベントのエンドポイント](../media/businesseventsendpoint.png)

### <a name="create-an-azure-service-bus-queue-endpoint"></a><span data-ttu-id="3ce17-168">Azure Service Bus キュー エンドポイントの作成</span><span class="sxs-lookup"><span data-stu-id="3ce17-168">Create an Azure Service Bus Queue endpoint</span></span>

<span data-ttu-id="3ce17-169">新しいエンドポイントを作成するには、**新規作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-169">To create a new endpoint, select **New**.</span></span> <span data-ttu-id="3ce17-170">次に、**エンドポイントの種類**フィールドで、適切なエンドポイントの種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-170">Then, in the **Endpoint type** field, select the appropriate endpoint type.</span></span> <span data-ttu-id="3ce17-171">Service Bus キューにエンドポイントを作成するには、**Azure Service Busキュー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-171">To create an endpoint to a Service Bus queue, select **Azure Service Bus Queue**.</span></span>

![ビジネス イベントの新規エンドポイント](../media/businesseventsnewendpoint1.png)

<span data-ttu-id="3ce17-173">**次へ**を選択し、エンドポイントおよび Service Busキューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-173">Select **Next**, and specify the name of the endpoint and the Service Bus queue.</span></span> <span data-ttu-id="3ce17-174">また、Azure メッセージング リソースにシークレットを提供するために、Azure Key Vault を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-174">In addition, you must set up Azure Key Vault to provide the secret to the Azure messaging resource.</span></span> <span data-ttu-id="3ce17-175">また、Azure Active Directory (Azure AD) アプリケーション ID およびアプリケーション シークレットを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-175">You must also set up the Azure Active Directory (Azure AD) application ID and application secret.</span></span>

![ビジネス イベントの新規エンドポイント](../media/businesseventsnewendpoint2.png)

<span data-ttu-id="3ce17-177">**キュー名**フィールドに、Azure の Azure Service Bus キューの構成で作成した**Azure Service Bus キュー**名を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-177">In the **Queue Name** field, enter the **Azure Service Bus Queue** name that you created in the Azure Service Bus Queue configuration in Azure.</span></span>  

![ビジネス イベント キュー名](../media/BusinessEventsSBQueueName.PNG)

<span data-ttu-id="3ce17-179">**Azure Active Directory アプリケーションID**フィールドに、Azure ポータルの Azure AD で作成されたアプリケーションIDを入力します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-179">In the **Azure Active Directory application ID** field, enter the application ID that is created in Azure AD in the Azure portal.</span></span>

![ビジネス イベントの Azure AD のコンフィギュレーション](../media/businesseventsaad1.png)

<span data-ttu-id="3ce17-181">**Azure アプリケーション シークレット** フィールドに、アプリケーションのシークレット値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-181">In the **Azure application secret** field, enter the secret value for the application.</span></span>

![ビジネス イベントの Azure AD のコンフィギュレーション](../media/businesseventsaad2.png)

<span data-ttu-id="3ce17-183">**Key Vault DNS 名**フィールドに、Key Vault設定名を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-183">In the **Key vault DNS name** field, enter the name from your Key Vault setup.</span></span>

![ビジネス イベントの Azure Key Vault のコンフィギュレーション](../media/businesseventskeyvault1.png)

<span data-ttu-id="3ce17-185">**Key Vault シークレット名**フィールドに、Key Vaultに作成する必要があるエンドポイント リソースのシークレット名を入力します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-185">In the **Key vault secret name** field, enter the secret name for the endpoint resource that must be created in Key Vault.</span></span>

![ビジネス イベントの Azure Key Vault のコンフィギュレーション](../media/businesseventskeyvault2.png)

<span data-ttu-id="3ce17-187">Azure では、**Key Vault シークレット**の値は Azure Service Busの**プライマリ接続文字列**の値になります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-187">The **Key Vault Secret** value, in Azure, will be the Azure Service Bus **Primary Connection String** value.</span></span> <span data-ttu-id="3ce17-188">この値は**共有アクセス ポリシー > RootManagedSharedAccessKey** で構成した Azure Service Bus で確認できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-188">This value is found in the Azure Service Bus that you configured in **Shared Access Policies > RootManagedSharedAccessKey**.</span></span>

![ビジネス イベントの Azure Key Vault のキー値](../media/BusinessEventsKVSValue.PNG)

> [!IMPORTANT]
> <span data-ttu-id="3ce17-190">また、登録された Azure アプリケーションは、Key Vault のアクセス ポリシーで設定された Key Vault に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-190">The Azure application that was registered must be also added to the Key Vault set up under Access policies in the Key Vault.</span></span> <span data-ttu-id="3ce17-191">この設定を完了するには、**キー、シークレット、および証明書の管理**テンプレートを選択し、アプリケーションを**プリンシパル**として選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-191">For this setup to be complete, select the **Key, Secret & Certificate Management** template and then select the application as the **principal**.</span></span>

### <a name="create-an-azure-service-bus-topic-endpoint"></a><span data-ttu-id="3ce17-192">Azure Service Bus トピック エンドポイントの作成</span><span class="sxs-lookup"><span data-stu-id="3ce17-192">Create an Azure Service Bus Topic endpoint</span></span>

<span data-ttu-id="3ce17-193">Service Bus トピックにエンドポイントを作成するには、**新規**を選択し、次に**エンドポイントの種類**フィールドで、**Azure Service Bus トピック**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-193">To create an endpoint to a Service Bus topic, select **New**, and then, in the **Endpoint type** field, select **Azure Service Bus Topic**.</span></span> <span data-ttu-id="3ce17-194">**トピック名**フィールドは、Service Bus トピック名に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-194">The **Topic name** field must be set to the name of the Service Bus topic.</span></span> <span data-ttu-id="3ce17-195">Key Vault の情報は、Azure Service Bus キュー エンドポイントの設定と同じ方法で設定されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-195">Key Vault information is set up in the same way that it is set up for an Azure Service Bus Queue endpoint.</span></span>

### <a name="create-an-azure-event-grid-endpoint"></a><span data-ttu-id="3ce17-196">Azure イベント グリッド エンドポイントの作成</span><span class="sxs-lookup"><span data-stu-id="3ce17-196">Create an Azure Event Grid endpoint</span></span>

<span data-ttu-id="3ce17-197">エンドポイントを作成するには、Azure ポータルで **Azure イベント グリッド トピック**を作成して構成し、次に**ビジネス イベント ワークスペース**でイベント グリッド トピックにエンドポイントを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-197">To create an endpoint, you need to create and configure an **Azure Event Grid Topic** in Azure Portal, and then create an endpoint to the Event Grid Topic in the **Business Events Workspace**.</span></span> <span data-ttu-id="3ce17-198">**エンドポイント**タブに移動し、**新規**を選択し、**エンドポイントの種類**で **Azure イベント グリッド**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-198">Go to the **Endpoints** tab, select **New**, and then select **Azure Event Grid** as the **Endpoint type**.</span></span> <span data-ttu-id="3ce17-199">**エンドポイント URL** フィールドで、**Azure イベント グリッド トピック**からURLを入力します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-199">In the **Endpoint URL** field, enter the URL from the **Azure Event Grid Topic**.</span></span> <span data-ttu-id="3ce17-200">これは、イベント グリッド トピックの**概要**セクションの**トピック エンドポイント**の値です。</span><span class="sxs-lookup"><span data-stu-id="3ce17-200">This is the **Topic Endpoint** value in the **Overview** section of your Event Grid Topic.</span></span>

![ビジネス イベントのイベント グリッド エンドポイントの値](../media/BusinessEventsEGTopicsEndpoint.PNG)

<span data-ttu-id="3ce17-202">Key Vault の情報は、Azure Service Bus キュー エンドポイントの設定と同じ方法で設定されますが、Key Vault シークレットだけはService Bus 接続文字列ではなく、イベント グリッドの資格情報に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-202">Key Vault information is set up in the same way that it is set up for an Azure Service Bus Queue endpoint, except the Key Vault secret should now point to the Event Grid credential, rather than the Service Bus connection string.</span></span>  <span data-ttu-id="3ce17-203">イベント グリッドの資格情報は、設定セクションの**アクセス キー**で作成されたイベント グリッドで確認できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-203">The Event Grid Crendtial can be found under the Event Grid you created in the **Access Keys** section under Settings.</span></span> 

![ビジネス イベントのイベント グリッド資格情報の値](../media/BusinessEventsEGKeyValue.PNG)

<span data-ttu-id="3ce17-205">必要なエンドポイントを作成したら、次に、ビジネス イベントを有効にします。</span><span class="sxs-lookup"><span data-stu-id="3ce17-205">After you've created the endpoints that you require, the next step is to activate the business events.</span></span>


## <a name="activating-business-events"></a><span data-ttu-id="3ce17-206">ビジネス イベントの有効化</span><span class="sxs-lookup"><span data-stu-id="3ce17-206">Activating business events</span></span>

<span data-ttu-id="3ce17-207">既定では、ビジネス イベント カタログのビジネス イベントは有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="3ce17-207">Business events in the business event catalog aren't active by default.</span></span> <span data-ttu-id="3ce17-208">カタログから必要なビジネス イベントを有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-208">From the catalog, you can activate any business events that you require.</span></span> <span data-ttu-id="3ce17-209">1つまたは複数のビジネス イベントを選択し、**有効化**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-209">Select one or more business events, and then select **Activate**.</span></span>

![ビジネス イベントの有効化](../media/businesseventsactivation.png)

<span data-ttu-id="3ce17-211">ビジネス イベントは、すべての法人または特定の法人のいずれかで有効化できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-211">Business events can be activated either in all legal entities or in specific legal entities.</span></span> <span data-ttu-id="3ce17-212">**法人**フィールドを空白のままにすると、選択したビジネス イベントは*すべて*の法人で有効化されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-212">If you leave the **Legal entity** field blank, the selected business events will be activated in *all* legal entities.</span></span> <span data-ttu-id="3ce17-213">ビジネス イベントが特定の法人に対してのみ必要な場合は、法人ごとに個別に構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-213">If a business event is required only for specific legal entities, it must be configured separately for each legal entity.</span></span>

<span data-ttu-id="3ce17-214">有効化されるビジネス イベントにエンドポイントを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-214">Endpoints must be assigned to the business events that are activated.</span></span>

<span data-ttu-id="3ce17-215">ビジネス プロセスの実行時にビジネス イベントが発生した場合、システムは有効化されたビジネス イベントに対してのみ、発信処理を行います。</span><span class="sxs-lookup"><span data-stu-id="3ce17-215">When business events occur as business processes are run, the system will do outbound processing only for business events that have been activated.</span></span>

<span data-ttu-id="3ce17-216">ビジネス イベントが有効化されると、**有効なイベント**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-216">After business events are activated, they appear on the **Active events** tab.</span></span>

![有効なビジネス イベント](../media/businesseventsactivetab.png)

<span data-ttu-id="3ce17-218">**の有効なイベント**タブで、ビジネス イベントを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-218">From the **Active events** tab, you can inactivate business events.</span></span> <span data-ttu-id="3ce17-219">システムは、無効化されたイベントには発信処理を行いません。</span><span class="sxs-lookup"><span data-stu-id="3ce17-219">The system won't do outbound processing for inactivated events.</span></span>

<span data-ttu-id="3ce17-220">ビジネス イベントが無効化されると、**無効なイベント**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-220">After businessevents are inactivated, they appear on the **Inactive events** tab.</span></span>

![無効なビジネス イベント](../media/businesseventsinactivetab.png)

<span data-ttu-id="3ce17-222">統合環境におけるシステムの管理活動のためにビジネス イベントの処理をある期間停止する必要がある場合、ビジネス イベントを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-222">Business events can be inactivated when processing of business events must be paused for a period because of specific system maintenance activities in the integration landscape.</span></span>

<span data-ttu-id="3ce17-223">ビジネス要件を変更するときに、ビジネス イベントが不要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-223">When business requirements change, some business events might no longer be required.</span></span> <span data-ttu-id="3ce17-224">この場合、有効なイベントの一覧から削除するのではなく、無効にできます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-224">In this case, you can inactivate them instead of deleting them from the list of active events.</span></span> <span data-ttu-id="3ce17-225">この方法は、ビジネス イベントのエラーの履歴を保持する必要がある場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-225">This approach is useful if the history of errors for the business events must be preserved.</span></span> <span data-ttu-id="3ce17-226">無効化されたビジネス イベントは、無効のまま保持する必要があるビジネスがなくなった場合、後で削除することができます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-226">Inactivated business events can be deleted later, when there is no longer a business need to keep them inactivated.</span></span>

## <a name="errors"></a><span data-ttu-id="3ce17-227">エラー</span><span class="sxs-lookup"><span data-stu-id="3ce17-227">Errors</span></span>

<span data-ttu-id="3ce17-228">システムがビジネス イベントの発信処理を行う間にエラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-228">While the system does outbound processing of business events, errors can occur.</span></span> <span data-ttu-id="3ce17-229">これらのエラーにより、システムがエンドポイントにビジネス イベントを正常に送付できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-229">These errors might prevent the system from successfully delivering a business event to the endpoint.</span></span> <span data-ttu-id="3ce17-230">エラーが発生した場合、システムはビジネス イベントを正常に処理するため、何度か再試行します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-230">If an error occurs, the system retries several times to successfully process the business event.</span></span> <span data-ttu-id="3ce17-231">しかし、試行が全く成功しなかった場合は、ビジネス イベントはエラー ログに保存されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-231">However, if all attempts are unsuccessful, the business event is saved in an error log.</span></span>

<span data-ttu-id="3ce17-232">エラー ログには、**有効なイベント**、**無効なイベント**、および**エラー**タブからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-232">Error logs can be accessed from the **Active events**, **Inactive events**, and **Errors** tabs.</span></span> <span data-ttu-id="3ce17-233">**エラー**タブにはすべてのビジネス イベントのすべてのエラーが表示され、他の2つのタブには特定のビジネス イベントに関連するエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-233">The **Errors** tab shows all errors across all business events, whereas the other two tabs show errors in the context of a specific business event.</span></span>

<span data-ttu-id="3ce17-234">**再送信**アクションを使用して、各エラーにおける発信処理を必要に応じて行うことができます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-234">You can do on-demand outbound processing on each error by using the **Resend** action.</span></span> <span data-ttu-id="3ce17-235">このアクションは、発信処理ロジックを起動します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-235">This action invokes the outbound processing logic.</span></span> <span data-ttu-id="3ce17-236">このロジックには、再試行が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-236">This logic includes retries.</span></span> <span data-ttu-id="3ce17-237">発信処理がそれでも成功しない場合は、エラー ログにエラーが記録されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-237">If the outbound processing is still unsuccessful, the error is logged in the error log.</span></span> <span data-ttu-id="3ce17-238">この場合、**エラー**タブの**最終処理時間**フィールドに、イベントの処理が発生した最終時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-238">In this case, the **Last process time** field on the **Errors** tab indicates when the last attempt to process the event occurred.</span></span>

<span data-ttu-id="3ce17-239">エラーを正常に処理できない場合は、必要に応じて**ダウンロード ペイロード** オプションを使用し、イベントからペイロードをダウンロードしてオフライン処理します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-239">If an error can't be successfully processed, you can use the **Download payload** option to download the payload from the event for offline processing, as you require.</span></span>

> [!NOTE]
> <span data-ttu-id="3ce17-240">エンドポイントが削除され、新しいエンドポイントがビジネス イベントに関連付けられている場合は、ビジネス イベントに関連付けられているすべてのエラーは引き続き再送信できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-240">If an endpoint is deleted and a new endpoint is associated with business events, all errors that are associated with the business events can still be resent.</span></span> <span data-ttu-id="3ce17-241">この場合、システムは発信処理システムを実行し、対応するビジネス イベントに関連付けられている新しいエンドポイントに送信します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-241">In this case, the system will do outbound processing to send to the new endpoint that is associated with the corresponding business event.</span></span> <span data-ttu-id="3ce17-242">この機能により、コンフィギュレーションのミスやその他のエラー状態から上手に復旧できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-242">This functionality allows for graceful recovery from misconfiguration or other error states.</span></span>

## <a name="business-event-consumption-models"></a><span data-ttu-id="3ce17-243">ビジネス イベント消費モデル</span><span class="sxs-lookup"><span data-stu-id="3ce17-243">Business event consumption models</span></span>

<span data-ttu-id="3ce17-244">実装の統合の要件と統合ソリューションの設計はさまざまです。</span><span class="sxs-lookup"><span data-stu-id="3ce17-244">The integration requirements and integration solution design for implementations vary.</span></span> <span data-ttu-id="3ce17-245">統合の要件は、ビジネス イベントの消費モデルの識別に影響します。</span><span class="sxs-lookup"><span data-stu-id="3ce17-245">The integration requirements play a role in identifying the consumption model for business events.</span></span> <span data-ttu-id="3ce17-246">次の図は、Finance and Operations が利用できる消費モデルを示しています。</span><span class="sxs-lookup"><span data-stu-id="3ce17-246">The following illustration shows the consumption models that Finance and Operations makes available.</span></span>

![ビジネス イベント消費モデル](../media/businesseventsconsumptionmodel.png)

<span data-ttu-id="3ce17-248">簡単に言うと、ビジネス イベントを使用した統合を設計する際に、次の点を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-248">In summary, you must consider the following points when you design integrations that use business events:</span></span>

- <span data-ttu-id="3ce17-249">ビジネス イベントは Microsoft Flow、Service Bus またはイベント グリッドで消費できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-249">Business events can be consumed via Microsoft Flow, Service Bus, or Event Grid.</span></span>
- <span data-ttu-id="3ce17-250">Microsoft Flow、Service Bus またはイベント グリッドを使用するには、顧客は自分でサブスクリプションを契約する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-250">Customers must bring their own subscriptions to use Microsoft Flow, Service Bus, or Event Grid.</span></span>
- <span data-ttu-id="3ce17-251">ビジネス イベントは、すべての法人または特定の法人で有効化できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-251">A business event can be activated in all legal entities or in specific legal entities.</span></span>
- <span data-ttu-id="3ce17-252">法人のビジネス イベントは、1つのエンドポイントにのみ送信できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-252">A business event in a legal entity can be sent to only one endpoint.</span></span> <span data-ttu-id="3ce17-253">メッセージング ブローカーにより、一対多 (1: n) の消費が可能になります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-253">Messaging brokers make one-to-many (1:N) consumption available.</span></span>
- <span data-ttu-id="3ce17-254">特定の法人にまたがるビジネス イベントは、特定のエンドポイントまたは同一のエンドポイントに送信できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-254">A business event across unique legal entities can be sent to unique endpoints or the same endpoints.</span></span>
- <span data-ttu-id="3ce17-255">Microsoft Flow はビジネス イベントを直接購読できます。</span><span class="sxs-lookup"><span data-stu-id="3ce17-255">Microsoft Flow can directly subscribe to business events.</span></span>
- <span data-ttu-id="3ce17-256">Service Bus またはイベント グリッド エンドポイントなどのエンドポイントにより、*n* 個のコンシューマーがイベントを購読して受信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="3ce17-256">Endpoints such as Service Bus or Event Grid endpoints enable *n* consumers to subscribe to and receive the events.</span></span>

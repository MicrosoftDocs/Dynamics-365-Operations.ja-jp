---
title: 店舗での顧客管理
description: このトピックでは、小売業者が Microsoft Dynamics 365 Commerce の販売時点管理 (POS) で顧客管理機能を有効にする方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8a1b360ba6a2d32e38e101f25f108094a00190c8
ms.sourcegitcommit: 8a14eac1c27f10c2b1b02ac9ad82339f5e127602
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2021
ms.locfileid: "5555050"
---
# <a name="customer-management-in-stores"></a><span data-ttu-id="8f681-103">店舗での顧客管理</span><span class="sxs-lookup"><span data-stu-id="8f681-103">Customer management in stores</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f681-104">このトピックでは、小売業者が Microsoft Dynamics 365 Commerce の販売時点管理 (POS) で顧客管理機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f681-104">This topic explains how retailers can enable customer management capabilities at the point of sale (POS) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8f681-105">店舗の関係者が POS で顧客レコードを作成および編集できることが重要です。</span><span class="sxs-lookup"><span data-stu-id="8f681-105">It's important that store associates can create and edit customer records at the POS.</span></span> <span data-ttu-id="8f681-106">このようにして、電子メール アドレス、電話番号、住所などの顧客情報の更新を取得できます。</span><span class="sxs-lookup"><span data-stu-id="8f681-106">In that way, they can capture any updates to customer information such as the email address, phone number, and address.</span></span> <span data-ttu-id="8f681-107">これらのシステムの有効性は、顧客データの正確性に依存するため、この情報はマーケティングなどの下流システムで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8f681-107">This information is helpful in downstream systems such as marketing, because the effectiveness of those systems depends on the accuracy of their customer data.</span></span>

<span data-ttu-id="8f681-108">販売担当者は、2 つの POS エントリ ポイントから顧客作成ワークフローをトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="8f681-108">Sales associates can trigger the customer creation workflow from two POS entry points.</span></span> <span data-ttu-id="8f681-109">**顧客の追加** 操作にマップされているボタンを選択、もしくは検索結果のアプリ バーで **顧客の作成** を選択できます。</span><span class="sxs-lookup"><span data-stu-id="8f681-109">They can select a button that is mapped to the **Customer add** operation, or they can select **Create customer** on the app bar on the search results page.</span></span> <span data-ttu-id="8f681-110">どちらの場合も、**新規顧客** ダイアログ ボックスが表示され、販売担当者は、顧客の名前、電子メール アドレス、電話番号、住所、およびビジネスに関連する追加情報など、必要な顧客の詳細情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="8f681-110">In both cases, the **New customer** dialog box appears, where sales associates can enter required customer details, such as the customer's name, email address, phone number, address, and any additional information that is relevant to the business.</span></span> <span data-ttu-id="8f681-111">この追加情報は、顧客に関連付けられている顧客属性を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="8f681-111">That additional information can be captured by using the customer attributes that are associated with the customer.</span></span> <span data-ttu-id="8f681-112">顧客属性の詳細については、[顧客属性](dev-itpro/customer-attributes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f681-112">For more information about customer attributes, see [Customer attributes](dev-itpro/customer-attributes.md).</span></span>

<span data-ttu-id="8f681-113">販売担当者は、副次的な電子メール アドレスと電話番号を取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="8f681-113">Sales associates can also capture secondary email addresses and phone numbers.</span></span> <span data-ttu-id="8f681-114">また、それらの副次的な電子メール アドレスまたは電話番号を介してマーケティング情報を受け取る顧客の好みを取得できます。</span><span class="sxs-lookup"><span data-stu-id="8f681-114">Additionally, they can capture the customer's preference about receiving marketing information via any of those secondary email addresses or phone numbers.</span></span> <span data-ttu-id="8f681-115">この機能を有効にするには、小売業者は、Commerce 本社の **機能管理** ワークスペースで **複数の電子メール アドレスと電話番号を取得し、これら連絡先でのマーケティングに同意する** 機能をオンにする必要があります (**システム管理 \> ワークスペース \> 機能管理**)。</span><span class="sxs-lookup"><span data-stu-id="8f681-115">To enable this capability, retailers must turn on the **Capture multiple emails and phone numbers and consent for marketing on these contacts** feature in the **Feature management** workspace in Commerce headquarters (**Systems administration \> Workspaces \> Feature management**).</span></span>

## <a name="default-customer-properties"></a><span data-ttu-id="8f681-116">既定の顧客プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f681-116">Default customer properties</span></span>

<span data-ttu-id="8f681-117">小売業者は、Commerce 本社 の **すべての店舗** ページ (**Retail と Commerce \> チャネル \> 店舗**) を使用して、既定の顧客を各店舗に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="8f681-117">Retailers can use the **All stores** page in Commerce headquarters (**Retail and Commerce \> Channels \> Stores**) to associate a default customer with each store.</span></span> <span data-ttu-id="8f681-118">次に、Commerce は、既定の顧客に定義されたプロパティを、作成された全ての新しい顧客レコードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="8f681-118">Commerce then copies the properties that are defined for the default customer to all new customer records that are created.</span></span> <span data-ttu-id="8f681-119">たとえば、**顧客の作成** ダイアログ ボックスには、店舗に関連付けられている既定の顧客から継承されたプロパティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-119">For example, the **Create customer** dialog box shows properties that are inherited from the default customer that is associated with the store.</span></span> <span data-ttu-id="8f681-120">このプロパティには、顧客タイプ、顧客グループ、レシートの基本設定、通貨、言語が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f681-120">Those properties include the customer type, customer group, receipt preference, currency, and language.</span></span> <span data-ttu-id="8f681-121">所属 (顧客のグループ) も既定の顧客から継承されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-121">Any affiliations (groupings of customers) are also inherited from the default customer.</span></span> <span data-ttu-id="8f681-122">ただし、財務分析コードは、既定の顧客自体からではなく、既定の顧客に関連付けられている顧客グループから継承されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-122">However, financial dimensions are inherited from the customer group that is associated with the default customer, not from the default customer itself.</span></span>

<span data-ttu-id="8f681-123">販売担当者は、1 人の顧客に対して複数の住所を取り込む場合があります。</span><span class="sxs-lookup"><span data-stu-id="8f681-123">Sales associates can capture multiple addresses for a customer.</span></span> <span data-ttu-id="8f681-124">顧客の名前と電話番号は、各住所に関連付けられている連絡先情報から継承されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-124">The customer's name and phone number are inherited from the contact information that is associated with each address.</span></span> <span data-ttu-id="8f681-125">顧客レコードの **住所** クイック タブには、販売担当者が編集できる **目的** フィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f681-125">The **Addresses** FastTab of a customer record includes a **Purpose** field that sales associates can edit.</span></span> <span data-ttu-id="8f681-126">顧客タイプが **個人** の場合、既定値は **自宅** になります。</span><span class="sxs-lookup"><span data-stu-id="8f681-126">If the customer type is **Person**, the default value is **Home**.</span></span> <span data-ttu-id="8f681-127">顧客タイプが **組織** の場合、既定値は **勤務先** になります。</span><span class="sxs-lookup"><span data-stu-id="8f681-127">If the customer type is **Organization**, the default value is **Business**.</span></span> <span data-ttu-id="8f681-128">このフィールドがサポートするその他の値には、**自宅**、**オフィス**、および **ポスト** が含まれます。</span><span class="sxs-lookup"><span data-stu-id="8f681-128">Other values that this field supports include **Home**, **Office**, and **Post box**.</span></span> <span data-ttu-id="8f681-129">住所の **国** フィールドの値は、**組織管理 \> 組織 \> 作業単位** の Commerce 本社にある **作業単位** ページで指定された基本住所から継承されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-129">The value of the **Country** field for an address is inherited from the primary address that is specified on the **Operating unit** page in Commerce headquarters at **Organization administration \> Organizations \> Operating units**.</span></span>

## <a name="sync-customers-and-async-customers"></a><span data-ttu-id="8f681-130">顧客の同期と顧客の非同期</span><span class="sxs-lookup"><span data-stu-id="8f681-130">Sync customers and Async customers</span></span>

<span data-ttu-id="8f681-131">Commerce には、同期と非同期の 2 つの顧客作成モードがあります。</span><span class="sxs-lookup"><span data-stu-id="8f681-131">In Commerce, there are two modes of customer creation: Synchronous (or Sync) and Asynchronous (or Async).</span></span> <span data-ttu-id="8f681-132">既定では、顧客は同期的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-132">By default, customers are created synchronously.</span></span> <span data-ttu-id="8f681-133">つまり、これらはリアルタイムに Commerce 本社に作成されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-133">In other words, they are created in Commerce headquarters in real time.</span></span> <span data-ttu-id="8f681-134">同期顧客作成モードは、新しい顧客をチャネル間で検索するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="8f681-134">The Sync customer creation mode is beneficial because new customers are immediately searchable across channels.</span></span> <span data-ttu-id="8f681-135">ただし、欠点もあります。</span><span class="sxs-lookup"><span data-stu-id="8f681-135">However, it also has a drawback.</span></span> <span data-ttu-id="8f681-136">Commerce 本社への [Commerce Data Exchange: リアルタイム サービス](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service)呼び出しを生成するため、多数の顧客作成呼び出しが同時に行われると、パフォーマンスに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8f681-136">Because it generates [Commerce Data Exchange: Real-time Service](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) calls to Commerce headquarters, performance can be affected if many concurrent customer creation calls are made.</span></span>

<span data-ttu-id="8f681-137">店舗の機能プロファイルで **顧客を非同期モードで作成** オプションが **はい** に設定されている場合 (**Retail と Commerce \> チャネル設定 \> オンライン ストアの設定 \> 機能プロファイル**)、チャネル データベースに顧客レコードを作成するためにリアルタイム サービス コールは使用されません。</span><span class="sxs-lookup"><span data-stu-id="8f681-137">If the **Create customer in async mode** option is set to **Yes** in the store's functionality profile (**Retail and Commerce \> Channel setup \> Online store setup \> Functionality profiles**), Real-time Service calls aren't used to create customer records in the channel database.</span></span> <span data-ttu-id="8f681-138">非同期顧客作成モードは、Commerce 本社のパフォーマンスには影響しません。</span><span class="sxs-lookup"><span data-stu-id="8f681-138">The Async customer creation mode doesn't affect the performance of Commerce headquarters.</span></span> <span data-ttu-id="8f681-139">一時的なグローバル固有識別子 (GUID) は、すべての新しい非同期顧客レコードに割り当てられ、顧客 ID として使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-139">A temporary globally unique identifier (GUID) is assigned to every new Async customer record and used as the customer account ID.</span></span> <span data-ttu-id="8f681-140">この GUID は、POS ユーザーには示されません。</span><span class="sxs-lookup"><span data-stu-id="8f681-140">This GUID isn't shown to POS users.</span></span> <span data-ttu-id="8f681-141">代わりに、これらのユーザーには、顧客 ID として **同期を保留中** と表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-141">Instead, those users will see **Pending sync** as the customer account ID.</span></span> <span data-ttu-id="8f681-142">この構成では、顧客は非同期で作成されますが、顧客レコードの編集は常に同期で行われることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8f681-142">Although this configuration forces customers to be created asynchronously, note that edits to customer records are always done synchronously.</span></span>

### <a name="convert-async-customers-to-sync-customers"></a><span data-ttu-id="8f681-143">非同期顧客を同期顧客に変換する</span><span class="sxs-lookup"><span data-stu-id="8f681-143">Convert Async customers to Sync customers</span></span>

<span data-ttu-id="8f681-144">非同期顧客を同期顧客に変換するには、最初に P ジョブを実行して、非同期顧客を Commerce 本社に送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f681-144">To convert Async customers to Sync customers, you must first run the P-job to send the Async customers to Commerce headquarters.</span></span> <span data-ttu-id="8f681-145">次に、**非同期モードから顧客とビジネス パートナーを同期する** ジョブを実行して、顧客 ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="8f681-145">Then run the **Synchronize customers and business partners from async mode** job to create customer account IDs.</span></span> <span data-ttu-id="8f681-146">最後に、**1010** ジョブを実行して、新しい顧客 ID をチャネルに同期します。</span><span class="sxs-lookup"><span data-stu-id="8f681-146">Finally, run the **1010** job to sync the new customer account IDs to the channels.</span></span>

### <a name="async-customer-limitations"></a><span data-ttu-id="8f681-147">非同期顧客の制限</span><span class="sxs-lookup"><span data-stu-id="8f681-147">Async customer limitations</span></span>

<span data-ttu-id="8f681-148">現在、非同期顧客機能には次の制限があります。</span><span class="sxs-lookup"><span data-stu-id="8f681-148">The Async customer functionality currently has the following limitations:</span></span>

- <span data-ttu-id="8f681-149">顧客が Commerce 本社で作成され、新しい顧客 ID がチャネルに同期されない限り、非同期顧客レコードを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="8f681-149">Async customer records can't be edited unless the customer has been created in Commerce headquarters and the new customer account ID has been synced back to the channel.</span></span>
- <span data-ttu-id="8f681-150">所属を非同期顧客に関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="8f681-150">Affiliations can't be associated with Async customers.</span></span> <span data-ttu-id="8f681-151">したがって、新しい非同期顧客は、既定の顧客から所属を継承しません。</span><span class="sxs-lookup"><span data-stu-id="8f681-151">Therefore, new Async customers don't inherit affiliations from the default customer.</span></span>
- <span data-ttu-id="8f681-152">新しい顧客 ID をチャネルに同期しない限り、ロイヤルティ カードを非同期顧客に発行することはできません。</span><span class="sxs-lookup"><span data-stu-id="8f681-152">Loyalty cards can't be issued to Async customers unless the new customer account ID has been synced back to the channel.</span></span>
- <span data-ttu-id="8f681-153">非同期顧客は、副次的な電子メール アドレスと電話番号を取得できません。</span><span class="sxs-lookup"><span data-stu-id="8f681-153">Secondary email addresses and phone numbers can't be captured for Async customers.</span></span>

### <a name="customer-creation-in-pos-offline-mode"></a><span data-ttu-id="8f681-154">POS オフライン モードでの顧客作成</span><span class="sxs-lookup"><span data-stu-id="8f681-154">Customer creation in POS offline mode</span></span>

<span data-ttu-id="8f681-155">非同期顧客作成モードが有効になっている間に POS がオフラインになると、新しい顧客レコードが非同期で作成されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-155">If the POS goes offline while the Async customer creation mode is enabled, new customer records are created asynchronously.</span></span> <span data-ttu-id="8f681-156">非同期顧客作成モードが無効になっているときに POS がオフラインになると、システムは自動的に非同期顧客作成モードに切り替わります。</span><span class="sxs-lookup"><span data-stu-id="8f681-156">If the POS goes offline while the Async customer creation mode is disabled, the system automatically switches to the Async customer creation mode.</span></span> <span data-ttu-id="8f681-157">つまり、非同期顧客作成モードが無効になっている場合でも、顧客レコードは非同期で作成される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8f681-157">In other words, customer records might be created asynchronously even if the Async customer creation mode is disabled.</span></span> <span data-ttu-id="8f681-158">したがって、Commerce 本社の管理者は、P ジョブ、**非同期モードからの顧客とビジネス パートナーの同期** ジョブ、および **1010** ジョブの定期的なバッチ ジョブを作成およびスケジュールする必要があります。これにより、すべての非同期顧客が Commerce 本社で同期顧客に変換されます。</span><span class="sxs-lookup"><span data-stu-id="8f681-158">Therefore, Commerce headquarters administrators must create and schedule a recurring batch job for the P-job, the **Synchronize customers and business partners from async mode** job, and the **1010** job, so that any Async customers are converted to Sync customers in Commerce headquarters.</span></span>

> [!NOTE]
> <span data-ttu-id="8f681-159">**コマース チャネル スキーマ** ページで **共有顧客データ テーブルのフィルター** オプションが **はい** に設定されている場合 (**Retail と Commerce \> 本社の設定 \> コマース スケジューラ \> チャネル データベース グループ**)、顧客レコードは POS オフライン モードでは作成されません。</span><span class="sxs-lookup"><span data-stu-id="8f681-159">If the **Filter shared customer data tables** option is set to **Yes** on the **Commerce channel schema** page (**Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database group**), customer records aren't created in POS offline mode.</span></span> <span data-ttu-id="8f681-160">詳細については、[オフライン データの除外](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f681-160">For more information, see [Offline data exclusion](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f681-161">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8f681-161">Additional resources</span></span>

[<span data-ttu-id="8f681-162">顧客属性</span><span class="sxs-lookup"><span data-stu-id="8f681-162">Customer attributes</span></span>](dev-itpro/customer-attributes.md)

[<span data-ttu-id="8f681-163">オフライン データの除外</span><span class="sxs-lookup"><span data-stu-id="8f681-163">Offline data exclusion</span></span>](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
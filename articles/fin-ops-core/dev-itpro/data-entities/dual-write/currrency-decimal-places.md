---
title: デュアル書き込みの通貨データ タイプの移行
description: このトピックでは、デュアル書き込みでサポートされている通貨の小数点以下の桁数を変更する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: c4f663ae36f7d4ea3db9888e618f2fe3bf8c3256
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748950"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="6fa01-103">デュアル書き込みの通貨データ タイプの移行</span><span class="sxs-lookup"><span data-stu-id="6fa01-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6fa01-104">サポートされている通貨値の小数位の数は、最大 10 個まで増やすことができます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="6fa01-105">既定の制限は、小数点以下 4 桁です。</span><span class="sxs-lookup"><span data-stu-id="6fa01-105">The default limit is four decimal places.</span></span> <span data-ttu-id="6fa01-106">小数点以下の桁数を増やすことで、デュアル書き込みを使用してデータを同期する場合にデータが失われないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="6fa01-107">小数桁数の増加は、オプトインの変更になります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="6fa01-108">それを実装するには、Microsoft に支援を依頼する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="6fa01-109">小数点以下の桁数を変更するプロセスには、次の 2 つのステップがあります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="6fa01-110">Microsoft からの移行を要求します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="6fa01-111">Dataverse の小数点以下の変化桁数。</span><span class="sxs-lookup"><span data-stu-id="6fa01-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="6fa01-112">この Finance and Operations アプリと Dataverse は、通貨値の小数点以下の桁数が同じであることをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="6fa01-113">これを行わないと、この情報がアプリ間で同期されている場合にデータが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="6fa01-114">移行プロセスでは、通貨と為替レートの値の格納方法が再設定されますが、データは変更されません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="6fa01-115">移行が完了した後、通貨コードと価格の小数桁数を増やすことができ、ユーザーが入力および表示するデータの小数点以下の精度を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="6fa01-116">移行はオプションです。</span><span class="sxs-lookup"><span data-stu-id="6fa01-116">Migration is optional.</span></span> <span data-ttu-id="6fa01-117">小数点以下の桁数を増やすことをお勧めする場合は、移行を検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6fa01-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="6fa01-118">小数点が 4 桁以上の値を必要としない組織では、移行する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="6fa01-119">Microsoft からの移行の要求</span><span class="sxs-lookup"><span data-stu-id="6fa01-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="6fa01-120">Dataverse での既存の通貨列の保管では、4 桁以上の小数点以下の桁数はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="6fa01-121">したがって、移行プロセス中に、データベースの新しい内部列に通貨の値がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="6fa01-122">このプロセスは、すべてのデータが移行されるまで継続して実行されます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="6fa01-123">移行が終了すると、内部的には古い記憶域タイプが新しい記憶域タイプに置き換えられますが、データ値は変更されません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="6fa01-124">通貨列では、10 桁までの小数位をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="6fa01-125">移行プロセス中は、Dataverse を中断せずに引き続き使用することができます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="6fa01-126">同時に、為替レートが変更され、現在の 10 回の制限ではなく 12 桁までの小数位をサポートするようになります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="6fa01-127">この変更は、小数点以下の桁数が Finance and Operations アプリと Dataverse の両方で同じになるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="6fa01-128">移行によってデータが変更されることはありません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-128">Migration doesn't change any data.</span></span> <span data-ttu-id="6fa01-129">通貨列と為替レート列を変換すると、管理者は、各取引通貨および価格の小数点以下の桁数を指定して、通貨列の小数位を最大 10 桁使用するようにシステムを構成できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="6fa01-130">移行の要求</span><span class="sxs-lookup"><span data-stu-id="6fa01-130">Request a migration</span></span>

<span data-ttu-id="6fa01-131">この機能を使用できるようにするには、**CDSExpandDecimal@microsoft.com** にメールをして、次の情報を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="6fa01-132">**件名:** \<organizationID\> の 10 進数サポートを有効にする要求</span><span class="sxs-lookup"><span data-stu-id="6fa01-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="6fa01-133">**本文:** 自分の組織 \<organizationID\> に対して拡張 10 進数サポートを有効にしたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="6fa01-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="6fa01-134">次の手順については、Microsoft の担当者が 2 ~ 3 営業日以内に連絡を差し上げます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="6fa01-135">移行を要求するときには、次の詳細を把握し、それに応じて計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="6fa01-136">データを移行するために必要な時間は、システムのデータ量によって異なります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="6fa01-137">大規模なデータベースの移行には数日間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="6fa01-138">移行の実行中は、インデックスに追加の領域が必要になるので、データベースのサイズは一時的に増加します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="6fa01-139">この追加領域の大部分は、移行の完了時に解放されます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="6fa01-140">移行プロセス中にエラーが発生して移行の完了を妨げる場合は、Microsoft サポートに警告が発生するので、サポート スタッフがそのように介入できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="6fa01-141">ただし、移行中にエラーが発生した場合でも、Dataverse はそのまま通常使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="6fa01-142">移行プロセスを元に戻すことはできません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="6fa01-143">小数点以下の桁数を変更する</span><span class="sxs-lookup"><span data-stu-id="6fa01-143">Changing the number of decimal places</span></span>

<span data-ttu-id="6fa01-144">移行が完了した後に、Dataverse は小数点以下の桁数が多い数値を保存できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="6fa01-145">管理者は、特定の通貨コードと価格設定に使用する小数位の数を選択できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="6fa01-146">Microsoft Power Apps、Power BI、Power Automate のユーザーは、より多くの小数点以下がある数字を表示して使用できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="6fa01-147">この変更を行うには、Power Apps の次の設定を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="6fa01-148">**システム設定: 価格決定の通貨の精度** - **システム全体の価格決定に使用される通貨の有効桁数を設定** 列は、**価格決定の精度** が選択された場合に、通貨が組織に対してどのように動作するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="6fa01-149">**業務管理: 通貨** - **通貨の精度** 列では、特定の通貨での小数点以下の桁数を独自に指定できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="6fa01-150">組織全体の設定にはフォールバックがあります。</span><span class="sxs-lookup"><span data-stu-id="6fa01-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="6fa01-151">次に、いくつか制限を示します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-151">There are some limitations:</span></span>

+ <span data-ttu-id="6fa01-152">テーブルで通貨列を構成することはできません。</span><span class="sxs-lookup"><span data-stu-id="6fa01-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="6fa01-153">**価格決定** と **トランザクションの通貨** レベルでは、小数点以下 4 桁以上を指定できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="6fa01-154">システム設定: 価格決定の通貨の精度</span><span class="sxs-lookup"><span data-stu-id="6fa01-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="6fa01-155">移行が完了した後、管理者は通貨の有効桁数を設定できます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="6fa01-156">**設定 \>管理** に移動して、**システム設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="6fa01-157">その後、**全般** タブで、次の図に示すように、**システム全体の価格決定に使用される通貨桁数を設定** 列の値を変更します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![通貨のシステム設定](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="6fa01-159">業務管理: 通貨</span><span class="sxs-lookup"><span data-stu-id="6fa01-159">Business Management: Currencies</span></span>

<span data-ttu-id="6fa01-160">特定の通貨の通貨の有効桁数と、価格決定に使用される通貨の桁数が異なる場合は、この通貨を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="6fa01-161">**設定\>業務管理** に移動して、**通貨** を選択して、通貨を選択して変更します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="6fa01-162">次の図に示すように、**通貨桁数** 列を目的の小数点以下の桁数に設定します。</span><span class="sxs-lookup"><span data-stu-id="6fa01-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![特定のロケールの通貨設定](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="6fa01-164">テーブル: 通貨列</span><span class="sxs-lookup"><span data-stu-id="6fa01-164">tables: Currency column</span></span>

<span data-ttu-id="6fa01-165">特定の通貨列に対して構成可能な小数位の数は 4 つに制限されます。</span><span class="sxs-lookup"><span data-stu-id="6fa01-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
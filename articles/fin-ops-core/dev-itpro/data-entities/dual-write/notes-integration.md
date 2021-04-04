---
title: メモ統合
description: このトピックでは、二重書き込みでのメモ データの統合について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.search.validFrom: 2021-02-22
ms.openlocfilehash: 221be52b4d66aaa47f9a1919d5d0b9f8459b7ff9
ms.sourcegitcommit: db9b35ce6968cad8874b3c13d4c02d84e2617c8b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2021
ms.locfileid: "5577609"
---
# <a name="note-integration"></a><span data-ttu-id="0ebd4-103">メモ統合</span><span class="sxs-lookup"><span data-stu-id="0ebd4-103">Note integration</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0ebd4-104">多くの場合、業務プロセス中に Microsoft Dynamics 365 ユーザーは顧客に関する情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-104">During business processes, Microsoft Dynamics 365 users often gather information about their customers.</span></span> <span data-ttu-id="0ebd4-105">この情報は、活動およびメモとして記録されます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-105">This information is recorded as activities and notes.</span></span> <span data-ttu-id="0ebd4-106">このトピックでは、二重書き込みでのメモ データの統合について説明します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-106">This topic describes the integration of note data in dual-write.</span></span>

<span data-ttu-id="0ebd4-107">顧客情報は、次のように分類できます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-107">Customer information can be classified in the following ways:</span></span>

+ <span data-ttu-id="0ebd4-108">**顧客の代わりに Dynamics 365 ユーザーが処理する実用的な情報** - 例えば Contoso (Dynamics 365ユーザー) が Game Show を実行している場合など。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-108">**Actionable information that a Dynamics 365 user handles on behalf of a customer** – For example, Contoso (a Dynamics 365 user) is conducting a game show.</span></span> <span data-ttu-id="0ebd4-109">Contoso の顧客の 1 人 (顧客) が、Game Show に参加したいと思っています。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-109">One of Contoso's customers (a customer) wants to attend the game show.</span></span> <span data-ttu-id="0ebd4-110">顧客は、Contoso の従業員に対し、Game Show でのスロットの予約を求める場合があります。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-110">The customer asks a Contoso employee to book a slot in the game show for them.</span></span> <span data-ttu-id="0ebd4-111">予約は Contoso のイベント出席者のカレンダーで発生します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-111">The booking occurs in Contoso's event attendee's calendar.</span></span>
+ <span data-ttu-id="0ebd4-112">**Dynamics 365 ユーザーの実用的な情報** - たとえば、Surface ユニットを購入する顧客は、出荷前にデバイスを贈り物用に包装する必要があるという特別な指示を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-112">**Actionable information for a Dynamics 365 user** – For example, a customer who is purchasing a Surface unit enters special instructions that indicate that the device should be gift wrapped before delivery.</span></span> <span data-ttu-id="0ebd4-113">これらの指示は、梱包を担当する Contoso の従業員が処理する必要がある、実用的な情報です。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-113">These instructions are actionable information that should be handled by the Contoso employee who is responsible for packaging.</span></span>
+ <span data-ttu-id="0ebd4-114">**非実用的な情報** - 例えば、顧客は Contoso ストアにアクセスし、店舗スタッフとの会話の中で、*Halo* のゲームとゲーム用アクセサリに関心を示します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-114">**Non-actionable information** – For example, a customer visits the Contoso store and, during their conversation with a store associate, expresses interest in *Halo* games and gaming accessories.</span></span> <span data-ttu-id="0ebd4-115">店舗スタッフはこの情報をメモします。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-115">The store associate makes a note of this information.</span></span> <span data-ttu-id="0ebd4-116">その後、製品の推奨エンジンを使用して、顧客に対して推奨事項を作成します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-116">The product recommendations engine then uses it to make recommendations to the customer.</span></span>

<span data-ttu-id="0ebd4-117">一般に、実用的な情報は、Finance and Operations アプリと Customer Engagement アプリに *活動* として記録されます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-117">In general, actionable information is captured as *activities* in Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="0ebd4-118">非実用的な情報は、Finance and Operations アプリに *メモ*、Customer Engagement アプリに *注釈* として記録されます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-118">Non-actionable information is captured as *notes* in Finance and Operations apps, and as *annotations* in customer engagement apps.</span></span>

> [!TIP]
> <span data-ttu-id="0ebd4-119">メモは非実用的な情報を対象としていますが、メモを使用して実用的な情報を保管および処理する場合、アプリがその使用を妨げることはありません。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-119">Although notes are intended for non-actionable information, the apps won't prevent you from using them to store and handle actionable information if you want to use them in that way.</span></span>

<span data-ttu-id="0ebd4-120">Microsoft は現在、メモ統合のための機能をリリースしています。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-120">Microsoft is currently releasing functionality for note integration.</span></span> <span data-ttu-id="0ebd4-121">(活動統合の機能は、後でリリースされます)。メモの統合は、顧客、仕入先、販売注文、および発注書に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-121">(Functionality for activity integration will be released later.) Note integration is available for customers, vendors, sales orders, and purchase orders.</span></span>

## <a name="create-a-note-in-a-customer-engagement-app"></a><span data-ttu-id="0ebd4-122">Customer Engagement アプリでのメモの作成</span><span class="sxs-lookup"><span data-stu-id="0ebd4-122">Create a note in a customer engagement app</span></span>

<span data-ttu-id="0ebd4-123">Customer Engagement アプリでメモを作成し、それを Finance and Operations アプリに同期させるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-123">To create a note in a customer engagement app and then sync it to a Finance and Operations app, follow these steps.</span></span>

1. <span data-ttu-id="0ebd4-124">Customer Engagement アプリで、顧客の勘定レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-124">In the customer engagement app, open the account record for a customer.</span></span>
2. <span data-ttu-id="0ebd4-125">**タイムライン** ウィンドウでプラス記号 (**+**) を選択してから、**メモ** を選択してメモを作成します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-125">In the **Timeline** pane, select the plus sign (**+**), and then select **Note** to create a note.</span></span>

    ![Customer Engagement アプリでのメモの作成](media/notes-ce-1.png)

3. <span data-ttu-id="0ebd4-127">タイトルおよび説明を入力し、**メモの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-127">Enter a title and description, and then select **Add note**.</span></span>

    ![タイトルと説明を入力する](media/notes-ce-2.png)

    <span data-ttu-id="0ebd4-129">新しいメモが顧客のタイムラインに追加されます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-129">The new note is added to the customer timeline.</span></span>

    ![顧客のタイムライン上の新しいメモ](media/notes-ce-3.png)

4. <span data-ttu-id="0ebd4-131">Finance and Operations アプリにサイン インし、同じ顧客レコードを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-131">Sign in to the Finance and Operations app, and open the same customer record.</span></span> <span data-ttu-id="0ebd4-132">右上隅の **添付ファイル** ボタン (クリップの記号) はレコードに添付ファイルがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-132">Notice that the **Attachments** button (paperclip symbol) in the upper-right corner indicates that the record has an attachment.</span></span>

    ![添付ファイルに関する通知](media/notes-ce-4.png)

5. <span data-ttu-id="0ebd4-134">**添付ファイル** ボタンを選択して **添付ファイル** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-134">Select the **Attachments** button to open the **Attachments** page.</span></span> <span data-ttu-id="0ebd4-135">Customer Engagement アプリで作成したメモを見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-135">You should find the note that you created in the customer engagement app.</span></span>

    ![Customer Engagement アプリからのメモ](media/notes-ce-5.png)

<span data-ttu-id="0ebd4-137">メモに対する更新は、Finance and Operations アプリとCustomer Engagement アプリ間で相互に同期されます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-137">Any updates to the note are synced back and forth between the Finance and Operations app and the customer engagement app.</span></span>

## <a name="create-a-note-in-a-finance-and-operations-app"></a><span data-ttu-id="0ebd4-138">Finance and Operations アプリでのメモの作成</span><span class="sxs-lookup"><span data-stu-id="0ebd4-138">Create a note in a Finance and Operations app</span></span>

<span data-ttu-id="0ebd4-139">Finance and Operations アプリでメモを作成し、Customer Engagement アプリに同期させることもできます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-139">You can also create a note in a Finance and Operations app, and it will be synced to a customer engagement app.</span></span>

<span data-ttu-id="0ebd4-140">Finance and Operations アプリでメモを作成し、Customer Engagement アプリに同期させるには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-140">To create a note in a Finance and Operations app and then sync it to a customer engagement app, follow these steps.</span></span>

1. <span data-ttu-id="0ebd4-141">Finance and Operations アプリの **添付ファイル** ページで、**新規作成**\>**メモ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-141">In the Finance and Operations app, on the **Attachments** page, select **New** \> **Note**.</span></span>

    ![Finance and Operations アプリでのメモの作成](media/notes-fo-1.png)

2. <span data-ttu-id="0ebd4-143">タイトルと簡単な手順のセットを入力し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-143">Enter a title and a brief set of instructions, and then select **Save**.</span></span>

    ![タイトルと手順を入力する](media/notes-fo-2.png)

3. <span data-ttu-id="0ebd4-145">Customer Engagement アプリで、レコードを更新します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-145">In the customer engagement app, update the record.</span></span> <span data-ttu-id="0ebd4-146">新しいメモをタイムラインで見つける必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-146">You should find the new note on the timeline.</span></span>

    ![Customer Engagement アプリのタイムライン上の新しいメモ](media/notes-fo-3.png)

<span data-ttu-id="0ebd4-148">メモは、内部または外部のどちらかとして分類できます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-148">You can classify a note as either internal or external.</span></span>

- <span data-ttu-id="0ebd4-149">Finance and Operations アプリの、**添付ファイル** ページ、次いで **制限** フィールドで **内部** または **外部** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-149">In the Finance and Operations app, on the **Attachments** page, open the note, and then, in the **Restriction** field, select **Internal** or **External**.</span></span>

    ![制限フィールド](media/notes-fo-4.png)

<span data-ttu-id="0ebd4-151">URL を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-151">You can also create a URL.</span></span>

1. <span data-ttu-id="0ebd4-152">Finance and Operations アプリの **添付ファイル** ページで、**新規作成**\>**URL** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-152">In the Finance and Operations app, on the **Attachments** page, select **New** \> **URL**.</span></span>
2. <span data-ttu-id="0ebd4-153">タイトルと URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-153">Enter a title and the URL.</span></span>
3. <span data-ttu-id="0ebd4-154">**制限** フィールドで、**内部** または **外部** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-154">In the **Restriction** field, select **Internal** or **External**.</span></span>

    ![Finance and Operations アプリでの URL の作成](media/notes-fo-5.png)

4. <span data-ttu-id="0ebd4-156">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-156">Select **Save**.</span></span>

    <span data-ttu-id="0ebd4-157">Customer Engagement アプリには URL タイプはないので、URL はメモとして二重書き込み機能と統合されています。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-157">Because customer engagement apps don't have a URL type, the URL is integrated with dual-write as a note.</span></span>

    ![Customer Engagement アプリでのメモとして表示される URL の作成](media/notes-ce-6.png)

> [!NOTE]
> <span data-ttu-id="0ebd4-159">添付ファイルはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-159">File attachments aren't supported.</span></span>

## <a name="templates"></a><span data-ttu-id="0ebd4-160">テンプレート</span><span class="sxs-lookup"><span data-stu-id="0ebd4-160">Templates</span></span>

<span data-ttu-id="0ebd4-161">メモ統合には、次の表に示すように、データ操作中に連携して動作するテーブル マップのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-161">Note integration includes a collection of table maps that work together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="0ebd4-162">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="0ebd4-162">Finance and Operations app</span></span> | <span data-ttu-id="0ebd4-163">Customer Engagement アプリ</span><span class="sxs-lookup"><span data-stu-id="0ebd4-163">Customer engagement app</span></span> | <span data-ttu-id="0ebd4-164">説明</span><span class="sxs-lookup"><span data-stu-id="0ebd4-164">Description</span></span> |
|----------------------------|-------------------------|-------------|
| [<span data-ttu-id="0ebd4-165">顧客の添付ファイル</span><span class="sxs-lookup"><span data-stu-id="0ebd4-165">Customer Attachments</span></span>](mapping-reference.md#230) | <span data-ttu-id="0ebd4-166">注釈</span><span class="sxs-lookup"><span data-stu-id="0ebd4-166">Annotations</span></span> | <span data-ttu-id="0ebd4-167">テキスト形式と URL を使用して顧客固有の (組織と人の両方の) 情報を取り込む企業。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-167">Businesses that use plain text and URLs to capture customer-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="0ebd4-168">仕入先ドキュメントの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="0ebd4-168">Vendor document attachments</span></span>](mapping-reference.md#231) | <span data-ttu-id="0ebd4-169">注釈</span><span class="sxs-lookup"><span data-stu-id="0ebd4-169">Annotations</span></span> | <span data-ttu-id="0ebd4-170">テキスト形式と URL を使用して仕入れ先固有の (組織と人の両方の) 情報を取り込む企業。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-170">Businesses that use plain text and URLs to capture vendor-specific information (for both organizations and persons).</span></span> |
| [<span data-ttu-id="0ebd4-171">販売注文のヘッダー ドキュメント添付</span><span class="sxs-lookup"><span data-stu-id="0ebd4-171">Sales order header document attachments</span></span>](mapping-reference.md#229) | <span data-ttu-id="0ebd4-172">注釈</span><span class="sxs-lookup"><span data-stu-id="0ebd4-172">Annotations</span></span> | <span data-ttu-id="0ebd4-173">テキスト形式と URL を使用して販売注文固有の情報を取り込む企業。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-173">Businesses that use plain text and URLs to capture sales order–specific information.</span></span> |
| [<span data-ttu-id="0ebd4-174">発注書のヘッダー ドキュメントの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="0ebd4-174">Purchase order header document attachments</span></span>](mapping-reference.md#232) | <span data-ttu-id="0ebd4-175">注釈</span><span class="sxs-lookup"><span data-stu-id="0ebd4-175">Annotations</span></span> | <span data-ttu-id="0ebd4-176">テキスト形式と URL を使用して発注書固有の情報を取り込む企業。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-176">Businesses that use plain text and URLs to capture purchase order–specific information.</span></span> |

<span data-ttu-id="0ebd4-177">詳細については、[二重書き込みマッピングのリファレンス](mapping-reference.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0ebd4-177">For more information, see [Dual-write mapping reference](mapping-reference.md).</span></span>

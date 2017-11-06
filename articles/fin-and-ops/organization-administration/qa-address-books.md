---
title: "アドレス帳 FAQ"
description: 
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 960e2cfac8b770f0e9e4d1e4136e6005ee3a0c7d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="address-books-faq"></a><span data-ttu-id="f5016-102">アドレス帳 FAQ</span><span class="sxs-lookup"><span data-stu-id="f5016-102">Address books FAQ</span></span>

[!include[banner](../includes/banner.md)]




<a name="how-do-i-check-for-duplicate-records"></a><span data-ttu-id="f5016-103">どのようにして重複レコードを確認しますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-103">How do I check for duplicate records?</span></span>
-------------------------------------

<span data-ttu-id="f5016-104">**グローバル アドレス帳**リスト ページから重複レコードを確認できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-104">You can check for duplicate records directly from the **Global address book** list page.</span></span> <span data-ttu-id="f5016-105">アクション ペインの [**関係者**] タブで、[**管理**] グループから、[**重複の確認**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5016-105">On the Action Pane, on the **Party** tab, in the **Maintain** group, click **Check for duplicates**.</span></span> <span data-ttu-id="f5016-106">次に、重複チェックに含める値を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5016-106">Then select the values to include in the check for duplicates.</span></span>

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a><span data-ttu-id="f5016-107">アドレス帳から関係者レコードの一括追加や一括削除はできますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-107">Can I bulk add or delete party records from an address book?</span></span>
<span data-ttu-id="f5016-108">はい、アドレス帳に複数の関係者レコードを追加したり、複数の関係者レコードを削除したりできます。</span><span class="sxs-lookup"><span data-stu-id="f5016-108">Yes, you can add multiple party records to an address book and also remove multiple party records.</span></span>

-   <span data-ttu-id="f5016-109">アドレス帳に複数の関係者レコードを追加するには、**グローバル アドレス帳**リスト ページで、リストから関係者を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5016-109">To add multiple party records to an address book, on the **Global address book** list page, select the parties in the list.</span></span> <span data-ttu-id="f5016-110">次に、アクション ペインの [**関係者**] タブで、[**管理**] グループから、[**関係者の割り当て**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5016-110">Then, on the Action Pane, on the **Party** tab, in the **Maintain** group, click **Assign parties**.</span></span> <span data-ttu-id="f5016-111">選択した関係者レコードを追加するアドレス帳を選択し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5016-111">Select the address books to add the selected party records to, and then click **OK**.</span></span> <span data-ttu-id="f5016-112">選択したすべての関係者レコードが、選択したすべてのアドレス帳に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-112">All the selected party records are added to the address books that you selected.</span></span>
-   <span data-ttu-id="f5016-113">アドレス帳から複数の関係者レコードを削除するには、**グローバル アドレス帳**リスト ページで、リストから関係者を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5016-113">To remove multiple party records from an address book, on the **Global address book** list page, select the parties in the list.</span></span> <span data-ttu-id="f5016-114">次に、アクション ペインの [**関係者**] タブで、[**管理**] グループから、[**関係者を削除します**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5016-114">Then, on the Action Pane, on the **Party** tab, in the **Maintain** group, click **Remove parties**.</span></span> <span data-ttu-id="f5016-115">関係者を削除するアドレス帳を選択し、[**OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5016-115">Select the address books to remove the parties from, and then click **OK**.</span></span> <span data-ttu-id="f5016-116">選択したすべての関係者レコードが、選択したすべてのアドレス帳から削除されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-116">All the selected party records are removed from the address books that you selected.</span></span>

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a><span data-ttu-id="f5016-117">レコードの関係者タイプを変更できますか。または、古いレコードを削除して新しいレコードを作成する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-117">Can I change the party type of a record, or do I have to delete the old record and create a new one?</span></span>
<span data-ttu-id="f5016-118">場合によっては、レコードの関係者タイプを人物から組織、または組織から人物に変更する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="f5016-118">Occasionally, you might have to change the party type of a record from person to organization or from organization to person.</span></span> <span data-ttu-id="f5016-119">たとえば、ナンシーは、Fabrikam U.K. 販売チームのメンバーです。</span><span class="sxs-lookup"><span data-stu-id="f5016-119">For example, Nancy is a member of the sales team for Fabrikam U.K.</span></span> <span data-ttu-id="f5016-120">ロンドンでの展示会で 6 人の新しい見込顧客に会いました。</span><span class="sxs-lookup"><span data-stu-id="f5016-120">At a trade show in London, she meets six new prospects.</span></span> <span data-ttu-id="f5016-121">ナンシーは、各見込顧客について見込顧客の関係者レコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="f5016-121">Nancy creates a prospect party record for each prospect.</span></span> <span data-ttu-id="f5016-122">ナンシーがレコードを保存すると、各レコードは、グローバル アドレス帳にも作成されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-122">When Nancy saves the records, each record is also created in the global address book.</span></span> <span data-ttu-id="f5016-123">Fabrikam は、既定の関係者タイプを組織に設定しましたが、新規見込顧客の 2 人は、人物のレコード タイプにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5016-123">Fabrikam has set the default party type to organization, but two of the new prospects should have a record type of person.</span></span> <span data-ttu-id="f5016-124">したがって、ナンシーは展示会から戻ったら、2 つの見込顧客レコードの関係者タイプを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5016-124">Therefore, when Nancy returns from the trade show, she must change the party type of the two prospect records.</span></span> <span data-ttu-id="f5016-125">関係者タイプを別の関係者タイプに変更するには、グローバル アドレス帳で最初に新しい関係者レコードを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5016-125">To change a party record from one party type to another, you must first create a new party record of the correct type in the global address book.</span></span> <span data-ttu-id="f5016-126">この新しいレコードと古い関係者レコードを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="f5016-126">You then associate the old party record with this new record.</span></span> <span data-ttu-id="f5016-127">新しい関係者の関連付けを作成した後、誤ったレコード タイプがある元の関係者レコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="f5016-127">After you have made the new party association, delete the original party record that has the incorrect record type.</span></span>

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a><span data-ttu-id="f5016-128">どのようにして関係者レコードの名前や住所を変更しますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-128">How do I change the name or address of a party record?</span></span>
<span data-ttu-id="f5016-129">関係者レコードの名前と、そのレコードと関連付けられる住所は、いつでも更新できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-129">You can update the name of a party record, and the addresses that are associated with that record, at any time.</span></span>

-   <span data-ttu-id="f5016-130">関係者レコードの名前を更新するには、関係者レコードを開き、アクション ペインで、[**編集**] をクリックします 。</span><span class="sxs-lookup"><span data-stu-id="f5016-130">To update the name of a party record, open the party record, and then, on the Action Pane, click **Edit**.</span></span> <span data-ttu-id="f5016-131">[**全般**] クイック タブで、関係者の新しい名前を入力し、レコードを保存します。</span><span class="sxs-lookup"><span data-stu-id="f5016-131">On the **General** FastTab, enter the new name for the party, and then save the record.</span></span>
-   <span data-ttu-id="f5016-132">次に関係者レコードの住所を更新するには、関係者レコードを開き、[**住所**] クイック タブで、更新する住所を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5016-132">To update an address for a party record, open the party record, and then, on the **Addresses** FastTab, select the address to update.</span></span> <span data-ttu-id="f5016-133">[**編集**] をクリックして、**住所の編集**ページをクリックし、住所または住所パラメーターに必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="f5016-133">Click **Edit**, and then, on the **Edit address** page, make the required changes to the address or address parameters.</span></span>

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a><span data-ttu-id="f5016-134">1 つのレコードに複数の関係者レコードをマージできますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-134">Can I merge two or more party records into one record?</span></span>
<span data-ttu-id="f5016-135">場合によっては、複数の関係者レコードを 1 つのレコードにマージしなければならないことがあります。</span><span class="sxs-lookup"><span data-stu-id="f5016-135">Occasionally, you might want to merge two or more party records into a single record.</span></span> <span data-ttu-id="f5016-136">このような状況は、意図的か意図的でないかにかかわらず、重複した関係者レコードを 1 つ以上作成するときに発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="f5016-136">This can occur if you create one or more duplicate party records, either on purpose or unintentionally.</span></span> <span data-ttu-id="f5016-137">関係者レコードをマージする場合は、保持するレコードを 1 つ選択します。</span><span class="sxs-lookup"><span data-stu-id="f5016-137">When you merge party records, you select one record to keep.</span></span> <span data-ttu-id="f5016-138">他のレコードの情報は、このレコードにマージされます。</span><span class="sxs-lookup"><span data-stu-id="f5016-138">The information from the other records is then merged into this record.</span></span> <span data-ttu-id="f5016-139">たとえば、Fabrikam に関する情報が A、B、C という 3 つの関係者レコードに格納されていることがわかり、関係者レコード A を保持することにしたとします。そのため、関係者レコード B、C に格納されている情報は、関係者レコード A にマージされます。関係者レコードをマージできない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="f5016-139">For example, you discover that information about Fabrikam is stored in three party records: A, B, and C. You decide to keep party record A. Therefore, the information that is stored in party records B and C will be merged into party record A. There are some situations where you can't merge party records:</span></span>

-   <span data-ttu-id="f5016-140">関係者レコードが同じ法人の同じ関係者ロール (顧客、仕入先など) に関連付けられている場合、それらのレコードはマージできません。</span><span class="sxs-lookup"><span data-stu-id="f5016-140">You can’t merge party records that are associated with the same party role, such as customer or vendor, in the same legal entity.</span></span> <span data-ttu-id="f5016-141">例えば、当事者 A は法人 123 の顧客に関連付けられ、当事者 B は法人 123 の異なる顧客に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f5016-141">For example, party A is associated with a customer in legal entity 123, and party B is associated with a different customer in legal entity 123.</span></span> <span data-ttu-id="f5016-142">これらのパーティ コードは、マージされていないとマージできません。マージされたパーティ レコードは、同じ法人の複数の顧客に関連付けられるため、これは許可されていません。</span><span class="sxs-lookup"><span data-stu-id="f5016-142">These party records can’t be merged, because if they were merged, the merged party record would be associated with multiple customers in the same legal entity, and this isn't allowed.</span></span> <span data-ttu-id="f5016-143">ただし、関係者 B が法人 123 内の仕入先に関連付けられている場合や、別の法人内の顧客に関連付けられている場合は、レコードをマージできます。</span><span class="sxs-lookup"><span data-stu-id="f5016-143">However, the records can be merged if party B is associated with a vendor in legal entity 123 or with a customer in a different legal entity.</span></span>
-   <span data-ttu-id="f5016-144">同じ法人、チーム、または作業単位の内部関係者組織レコードはマージできません。</span><span class="sxs-lookup"><span data-stu-id="f5016-144">You can’t merge internal party organization records in the same legal entity, team, or operating unit.</span></span>

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a><span data-ttu-id="f5016-145">グローバル アドレス帳または顧客ページや仕入先ページなど、別の場所に関係者レコードを作成する必要はありますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-145">Should I create a party record in the global address book or in another place, such as the Customer or Vendor page?</span></span>
<span data-ttu-id="f5016-146">グローバル アドレス帳または適切なエンティティのページで関係者レコードを入力できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-146">You can enter party records either in the global address book or on the appropriate entity page.</span></span> <span data-ttu-id="f5016-147">1 つの場所にレコードを追加すると、必ず同じレコードがもう一方の場所に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-147">When you add a record in one location, the same record is always added in the other location.</span></span> <span data-ttu-id="f5016-148">たとえば、グローバル アドレス帳の顧客の関係者レコードを追加する場合、レコードは、**顧客**ページにも追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-148">For example, if you add a party record for a customer in the global address book, the record is also added on the **Customer** page.</span></span> <span data-ttu-id="f5016-149">同様に、**顧客**ページに顧客の関係者レコードを追加する場合、レコードは、グローバル アドレス帳にも追加されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-149">Likewise, if you add a party record for a customer on the **Customer** page, the record is also added in the global address book.</span></span> <span data-ttu-id="f5016-150">新しい関係者レコードを入力する場所を決定するために次のガイドラインを使用します。</span><span class="sxs-lookup"><span data-stu-id="f5016-150">Use the following guidelines to decide where you should enter new party records:</span></span>

-   <span data-ttu-id="f5016-151">**エンティティ タイプがわからないときに関係者レコードを作成する場合** – 関係者レコードを作成する必要があるが、エンティティが顧客または営業案件かどうかなど、エンティティ タイプがわからない場合、グローバル アドレス帳にレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="f5016-151">**Creating a party record when you don't know the entity type** – If you must create a party record but don't know the entity type (for example, you don't know whether the entity is a customer or an opportunity), create the record in the global address book.</span></span> <span data-ttu-id="f5016-152">エンティティ タイプを後で選択できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-152">You can select the entity type later.</span></span>
-   <span data-ttu-id="f5016-153">**エンティティ タイプがわかっているときに関係者レコードを作成する場合** – 関係者のエンティティ タイプがわかっている場合、そのタイプに適切なページでレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-153">**Creating a party record when you know the entity type** – If you know the entity type for the party, you can create a record on the applicable page for that type.</span></span> <span data-ttu-id="f5016-154">たとえば、**顧客**ページで顧客のレコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="f5016-154">For example, create a record for a customer on the **Customer** page.</span></span> <span data-ttu-id="f5016-155">適切なエンティティ ページを使用してレコードを作成および保存すると、レコードがグローバル アドレス帳で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-155">When you create and save a record by using the appropriate entity page, the record is automatically created in the global address book.</span></span>

## <a name="can-i-translate-address-information-for-party-records"></a><span data-ttu-id="f5016-156">関係者レコードの住所情報を翻訳できますか。</span><span class="sxs-lookup"><span data-stu-id="f5016-156">Can I translate address information for party records?</span></span>
<span data-ttu-id="f5016-157">Microsoft Dynamics 365 for Finance and Operations のユーザーの言語 (システム言語) で情報を表示して、販売注文などのドキュメントでは別の言語で表示するように住所情報の翻訳を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-157">You can set up translations of address information, so that the information appears in your user language (system language) in Microsoft Dynamics 365 for Finance and Operations but in another language on documents such as sales orders.</span></span> <span data-ttu-id="f5016-158">国/地域名、住所の目的、名前の順序の翻訳を入力できます。</span><span class="sxs-lookup"><span data-stu-id="f5016-158">You can enter translations for country/region names, address purposes, and name sequences.</span></span> <span data-ttu-id="f5016-159">たとえば、システム言語がデンマーク語で、フランスの顧客に販売注文を作成するとします。</span><span class="sxs-lookup"><span data-stu-id="f5016-159">For example, your system language is Danish, and you create a sales order for a customer in France.</span></span> <span data-ttu-id="f5016-160">この場合、プログラムではデンマーク語で顧客レコードを表示しつつ、印刷した販売注文にはフランス語で住所情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f5016-160">In this case, you can view the customer record in Danish in the program but display the address information in French on the printed sales order.</span></span> <span data-ttu-id="f5016-161">翻訳を設定した場合、一覧に各品目の翻訳を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5016-161">When you set up translations, you should enter a translation for every item in the list.</span></span> <span data-ttu-id="f5016-162">翻訳が入力されていない品目は、システム言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-162">Any item that you don't enter a translation for will appear in the system language.</span></span> <span data-ttu-id="f5016-163">たとえば、システムの言語が、デンマーク語で、スペインの顧客にドキュメントを送信するとします。</span><span class="sxs-lookup"><span data-stu-id="f5016-163">For example, your system language is Danish, and you send a document to a customer in Spain.</span></span> <span data-ttu-id="f5016-164">住所情報にスペイン語 (ESP) の翻訳を入力しなかった場合、その情報は、システムと印刷資料ともにデンマーク語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="f5016-164">If you haven't entered Spanish (ESP) translations for the address information, that information will appear in Danish both in the program and on the printed document.</span></span>




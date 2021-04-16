---
title: テンプレート BOM
description: テンプレート BOM (部品表) は、定期的にサービスされるサービス対象のコンポーネントの標準化された一覧を提供します。
author: ShylaThompson
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b514aeed48180bb1b14be8b3d95d55d44d2ca8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824331"
---
# <a name="template-boms"></a><span data-ttu-id="da041-103">テンプレート BOM</span><span class="sxs-lookup"><span data-stu-id="da041-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="da041-104">テンプレート BOM (部品表) は、定期的なサービス対象のコンポーネントの一覧を標準化された形式で表示します。</span><span class="sxs-lookup"><span data-stu-id="da041-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="da041-105">テンプレート BOM に記載されるコンポーネントは、サービス対象の個々のサブコンポーネントを表します。</span><span class="sxs-lookup"><span data-stu-id="da041-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="da041-106">サービス対象にテンプレート BOM を適用して、サービス対象について交換されたサブコンポーネントのレコードを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="da041-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="da041-107">サービス合意またはサービス注文にテンプレート BOM を適用するには、サービス対象の関係に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="da041-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="da041-108">1 つのサービス対象に適用できるテンプレートは 1 つだけです。</span><span class="sxs-lookup"><span data-stu-id="da041-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="da041-109">テンプレート BOM の作成</span><span class="sxs-lookup"><span data-stu-id="da041-109">Create a template BOM</span></span>

<span data-ttu-id="da041-110">次の表は、テンプレート BOM を作成するために使用できるさまざまな方法について説明しています。</span><span class="sxs-lookup"><span data-stu-id="da041-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="da041-111">方法</span><span class="sxs-lookup"><span data-stu-id="da041-111">Method</span></span></p></th>
<th><p><span data-ttu-id="da041-112">説明</span><span class="sxs-lookup"><span data-stu-id="da041-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="da041-113">生産</span><span class="sxs-lookup"><span data-stu-id="da041-113">Production</span></span></p></td>
<td><p><span data-ttu-id="da041-114">テンプレート BOM は製造オーダーに基づきます。</span><span class="sxs-lookup"><span data-stu-id="da041-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="da041-115">このオプションは、実稼働環境で使用している場合のみ適用できます。</span><span class="sxs-lookup"><span data-stu-id="da041-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="da041-116">メリットは、品目を構成するコンポーネントの最新の詳細なリストを維持できることです。</span><span class="sxs-lookup"><span data-stu-id="da041-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da041-117">品目 BOM</span><span class="sxs-lookup"><span data-stu-id="da041-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="da041-118">テンプレート BOM は、品目 BOM に基づきます。</span><span class="sxs-lookup"><span data-stu-id="da041-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="da041-119">品目 BOM は、生産 BOM とは異なり、品目を構成するコンポーネントの静的な一覧です。</span><span class="sxs-lookup"><span data-stu-id="da041-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="da041-120">既存のテンプレート</span><span class="sxs-lookup"><span data-stu-id="da041-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="da041-121">このテンプレートは、既存のテンプレート BOM に基づきます。</span><span class="sxs-lookup"><span data-stu-id="da041-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="da041-122">手持在庫</span><span class="sxs-lookup"><span data-stu-id="da041-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="da041-123">サービス対象について頻繁に交換される予備部品がわかっている場合は、手動でテンプレート BOM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="da041-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="da041-124">この方法を使用すると、テンプレートに含まれるコンポーネントが作業場所の実際の要件を反映していることの確認が容易になります。</span><span class="sxs-lookup"><span data-stu-id="da041-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="da041-125">サービス合意またはサービス注文へのテンプレート BOM の適用</span><span class="sxs-lookup"><span data-stu-id="da041-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="da041-126">テンプレート BOM を、サービス合意、サービス注文、またはその両方に適用できます。</span><span class="sxs-lookup"><span data-stu-id="da041-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="da041-127">一般にサービス合意には、顧客との長期的な関係があります。</span><span class="sxs-lookup"><span data-stu-id="da041-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="da041-128">サービス BOM に記録される交換の履歴は、サービス合意にとって有用なデータです。</span><span class="sxs-lookup"><span data-stu-id="da041-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="da041-129">サービス対象へのサービスの実行履歴を記録するサービス注文にテンプレート BOM を適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="da041-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="da041-130">サービス BOM の履歴のコピー</span><span class="sxs-lookup"><span data-stu-id="da041-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="da041-131">サービス BOM 明細行の履歴は、複数のサービス合意間でコピーできます。</span><span class="sxs-lookup"><span data-stu-id="da041-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="da041-132">サービス合意間でサービスの履歴をコピーすることによって、品目の交換の記録を維持できます。</span><span class="sxs-lookup"><span data-stu-id="da041-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="da041-133">**例**</span><span class="sxs-lookup"><span data-stu-id="da041-133">**Example**</span></span>

<span data-ttu-id="da041-134">顧客の車に対して 3 年間のサービス合意を結びました。</span><span class="sxs-lookup"><span data-stu-id="da041-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="da041-135">この期間中に、顧客は会社が提供する上質のサービスに慣れてきます。</span><span class="sxs-lookup"><span data-stu-id="da041-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="da041-136">したがって、契約が切れた後、顧客は新しい合意の設定を望みます。</span><span class="sxs-lookup"><span data-stu-id="da041-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="da041-137">この時点で、会社に有利な合意を交渉できます。</span><span class="sxs-lookup"><span data-stu-id="da041-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="da041-138">交換されたコンポーネントに関する記録が将来役立つかもしれないので、サービス BOM の履歴を新しい合意にコピーします。</span><span class="sxs-lookup"><span data-stu-id="da041-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="da041-139">テンプレート BOM の変更</span><span class="sxs-lookup"><span data-stu-id="da041-139">Modify the template BOM</span></span>

<span data-ttu-id="da041-140">サービス対象に関連付けられていないテンプレート BOM の明細行は変更または削除できます。</span><span class="sxs-lookup"><span data-stu-id="da041-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="da041-141">テンプレート BOM をサービス対象に関連付けた後に、初めて BOM のローカル バージョンを変更できます。</span><span class="sxs-lookup"><span data-stu-id="da041-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="da041-142">テンプレート BOM のローカル バージョンの設定をコピーする場合は、ローカル バージョンに基づいて新しいテンプレート BOM を作成できます。</span><span class="sxs-lookup"><span data-stu-id="da041-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="da041-143">詳細については、[サービス BOM の変更](modify-service-bom.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="da041-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="da041-144">BOM 内の品目を交換する場合は、BOM デザイナで BOM 明細行の交換を登録できます。</span><span class="sxs-lookup"><span data-stu-id="da041-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="da041-145">必要に応じて、交換オブジェクトのサービス注文明細行を作成できます。</span><span class="sxs-lookup"><span data-stu-id="da041-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="da041-146">サービス注文明細行を作成すると、交換品目の請求書を作成できます。</span><span class="sxs-lookup"><span data-stu-id="da041-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="da041-147">交換のためのサービス注文明細行を作成しない場合、サービス対象の履歴を追跡するために交換登録が維持されます。</span><span class="sxs-lookup"><span data-stu-id="da041-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="da041-148">BOM 明細行の情報の表示方法の変更</span><span class="sxs-lookup"><span data-stu-id="da041-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="da041-149">すべてのテンプレート BOM とサービス BOM の BOM 明細行の情報の表示方法を変更できます。</span><span class="sxs-lookup"><span data-stu-id="da041-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="da041-150">すべてのテンプレート BOM とサービス BOM に変更が適用されます。</span><span class="sxs-lookup"><span data-stu-id="da041-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="da041-151">これには、サービス対象に関連付けられている明細行も含まれます。</span><span class="sxs-lookup"><span data-stu-id="da041-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="da041-152">テンプレート BOM 用の番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="da041-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="da041-153">テンプレート BOM を使用するには、2 つの番号順序を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da041-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="da041-154">テンプレート BOM に 1 つの番号順序を、BOM 履歴行番号にもう 1 つの番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="da041-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="da041-155">番号順序が使用され、ID を必要とするレコードに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="da041-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="da041-156">テンプレート BOM または BOM 履歴行番号に番号順序を割り当てるには、その前に、番号順序コードを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da041-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="da041-157">番号順序の設定</span><span class="sxs-lookup"><span data-stu-id="da041-157">Set up number sequences</span></span>

1.  <span data-ttu-id="da041-158">**Number sequences** リスト ページで、テンプレート BOM と BOM 履歴行番号の番号順序を作成します。</span><span class="sxs-lookup"><span data-stu-id="da041-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="da041-159">**サービス管理** \> **設定** \> **サービス管理パラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="da041-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="da041-160">**番号順序** をクリックし、**番号順序** フォームで作成した番号順序の参照に対する番号順序コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="da041-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="da041-161">フォームを閉じて、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="da041-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="da041-162">BOM 履歴行番号はシステムによって使用され、BOM 履歴トランザクションをサービス合意またはサービス注文に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="da041-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="da041-163">この番号は、ユーザー インターフェイスには表示されません。</span><span class="sxs-lookup"><span data-stu-id="da041-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="da041-164">参照</span><span class="sxs-lookup"><span data-stu-id="da041-164">See also</span></span>

[<span data-ttu-id="da041-165">テンプレート BOM の作成</span><span class="sxs-lookup"><span data-stu-id="da041-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="da041-166">対象関係でのテンプレート BOM の管理</span><span class="sxs-lookup"><span data-stu-id="da041-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="da041-167">サービス BOM の変更</span><span class="sxs-lookup"><span data-stu-id="da041-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
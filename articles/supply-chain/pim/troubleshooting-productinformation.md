---
title: 製品情報のトラブルシューティング
description: このトピックでは、製品情報を操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 87b04998889b86a79fd8dabde422147c5494b003
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516825"
---
# <a name="troubleshoot-product-information"></a><span data-ttu-id="48ef7-103">製品情報のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="48ef7-103">Troubleshoot product information</span></span>

<span data-ttu-id="48ef7-104">このトピックでは、製品情報を操作する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-104">This topic describes how to fix issues that you might encounter while you work with product information.</span></span>

## <a name="i-cant-delete-a-released-product"></a><span data-ttu-id="48ef7-105">リリースされた製品を削除できません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-105">I can't delete a released product.</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-106">Issue description</span></span>

<span data-ttu-id="48ef7-107">リリースされた製品およびそのすべてのバリアントは、リリースされた製品に関連するトランザクションが存在しない場合にのみ削除できます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-107">You can delete a released product and all its variants only if the released product doesn't have any related transactions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-108">Issue resolution</span></span>

<span data-ttu-id="48ef7-109">リリースされた製品または製品マスターを削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="48ef7-109">Follow these steps to delete a released product or product master.</span></span>

1. <span data-ttu-id="48ef7-110">品目の未処理トランザクションをすべて閉じます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-110">Close all open transactions for the items.</span></span>
1. <span data-ttu-id="48ef7-111">在庫を 0 (ゼロ) に減らします。</span><span class="sxs-lookup"><span data-stu-id="48ef7-111">Reduce the inventory to 0 (zero).</span></span>
1. <span data-ttu-id="48ef7-112">在庫計算を実行します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-112">Perform inventory closing.</span></span>
1. <span data-ttu-id="48ef7-113">削除する製品マスターのすべての製品バリアントを削除します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-113">Delete all product variants for the product master that you want to delete.</span></span>

## <a name="can-i-change-the-item-number-of-a-released-product"></a><span data-ttu-id="48ef7-114">リリースされた製品の品目番号を変更できますか。</span><span class="sxs-lookup"><span data-stu-id="48ef7-114">Can I change the item number of a released product?</span></span>

<span data-ttu-id="48ef7-115">ほとんどの場合、この変更によってデータが破損するため、リリースされた製品の品目番号を編集できません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-115">In most cases, you can't edit item numbers for released products, because that change will cause data to become corrupted.</span></span> <span data-ttu-id="48ef7-116">この品目番号を編集できるのは、リリースされた製品の主キーを以前名前変更したことにより発生したデータの破損を修復する必要がある場合のみです。これについては、[Platform update 24 により Finance and Operations 10.0.0 で削除または廃止された機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24)の一覧に掲載されています。</span><span class="sxs-lookup"><span data-stu-id="48ef7-116">You can edit the item number only if you must repair data corruption that was caused by a previous rename of the primary key of that released product, as mentioned in the list of [removed or deprecated features for Finance and Operations 10.0.0 with Platform update 24](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md#finance-and-operations-1000-with-platform-update-24).</span></span>

<span data-ttu-id="48ef7-117">リリースされた製品の品目番号を編集できるようにする場合は、[アイデア ポータルでこのアイデアに投票](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25)してください。</span><span class="sxs-lookup"><span data-stu-id="48ef7-117">If you want to be able to edit item numbers for released products, [vote for this idea in Ideas portal](https://experience.dynamics.com/ideas/idea/?ideaid=660fcb15-875d-ea11-b698-0003ff68bc25).</span></span>

## <a name="the-default-flushing-principle-from-the-product-isnt-being-entered-on-the-bill-of-materials-line"></a><span data-ttu-id="48ef7-118">製品からの既定の部品消費ルールが部品表明細行に入力されていません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-118">The default flushing principle from the product isn't being entered on the bill of materials line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-119">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-119">Issue description</span></span>

<span data-ttu-id="48ef7-120">部品表 (BOM) 明細行に品目を追加しても、その品目に対して設定されている既定の部品消費ルール情報は使用されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-120">When you add an item to a bill of materials (BOM) line, the system doesn't use the default flushing principle information that is set up for the item.</span></span> <span data-ttu-id="48ef7-121">つまり、品目からの部品消費ルールは **BOM 明細行** ページに表示されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-121">In other words, the flushing principle from the item doesn't appear on the **BOM line** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-122">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-122">Issue resolution</span></span>

<span data-ttu-id="48ef7-123">BOM 明細行で部品消費ルールを指定した場合、その BOM 明細行に適用されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-123">If you specify a flushing principle on a BOM line, it will apply to that BOM line.</span></span> <span data-ttu-id="48ef7-124">ただし、部品消費ルールが空白の場合、または BOM 明細行で設定されていない場合は、BOM 明細行に表示されなくても、その BOM 明細行には品目に対して設定されている部品消費ルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-124">However, if the flushing principle is blank, or if it isn't set on a BOM line, the flushing principle that is set on the item will still apply to that BOM line, even though it isn't shown on the BOM line.</span></span>

<span data-ttu-id="48ef7-125">通常、Microsoft Dynamics 365 Supply Chain Management のその他の機能の既定のロジックでは、この方法は使用されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-125">The defaulting logic for other features in Microsoft Dynamics 365 Supply Chain Management doesn't usually work in this way.</span></span> <span data-ttu-id="48ef7-126">ただし、現在の動作を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-126">However, the current behavior can't be changed.</span></span> <span data-ttu-id="48ef7-127">そうしないと、それに依存する既存のカスタマイズの一部が失われることがあります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-127">Otherwise, some existing customizations that rely on it might be broken.</span></span>

## <a name="the-system-lets-me-save-duplicate-bar-codes-for-different-items-or-for-the-same-item-that-has-different-dimensions"></a><span data-ttu-id="48ef7-128">システムでは、さまざまな品目または分析コードが異なる同じ品目に対して重複するバーコードを保存できます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-128">The system lets me save duplicate bar codes for different items or for the same item that has different dimensions.</span></span>

<span data-ttu-id="48ef7-129">現在は、システムによって固有のバーコードが適用されておらず、この制限の追加は破壊的変更となります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-129">The system doesn't currently enforce unique bar codes, and the addition of this restriction would be a breaking change.</span></span> <span data-ttu-id="48ef7-130">実際、Microsoft では、この変更によってお客様の既存のインストールが壊れるという証拠を持っています。</span><span class="sxs-lookup"><span data-stu-id="48ef7-130">In fact, Microsoft has evidence that some existing customer installations would be broken by this change.</span></span> <span data-ttu-id="48ef7-131">ただし、将来この機能を有効にするため、より広範な設計変更を検討する予定です。</span><span class="sxs-lookup"><span data-stu-id="48ef7-131">However, we will consider a broader design change to enable this feature in the future.</span></span>

## <a name="i-receive-the-following-error-message-when-i-edit-item-record-templates-the-warehouse-location-cannot-be-created-because-the-item-is-not-stocked-to-stock-items-the-stocked-product-option-on-the-associated-item-model-group-must-be-selected"></a><span data-ttu-id="48ef7-132">品目レコード テンプレートを編集すると、エラー メッセージ "品目の在庫がないため、倉庫の場所を作成できません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-132">I receive the following error message when I edit item record templates: "The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="48ef7-133">品目の在庫を確保するには、関連付けられている品目モデル グループの在庫製品オプションを選択する必要があります" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-133">To stock items, the Stocked product option on the associated item model group must be selected."</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-134">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-134">Issue description</span></span>

<span data-ttu-id="48ef7-135">この問題は、次の手順に従って、在庫のない品目のテンプレートを作成しようとした場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-135">This issue occurs if you follow these steps to try to create a template for an item that isn't stocked.</span></span>

1. <span data-ttu-id="48ef7-136">まだ在庫のないリリース済製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-136">Open a released product that isn't stocked.</span></span>
1. <span data-ttu-id="48ef7-137">アクション ペインの **オプション** タブで、**レコード情報** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-137">On the Action Pane, on the **Options** tab, select **Record info**.</span></span>
1. <span data-ttu-id="48ef7-138">**レコード情報** ダイアログ ボックスで、**会社コード テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-138">In the **Record information** dialog box, select **Company accounts template**.</span></span>

<span data-ttu-id="48ef7-139">この場合、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-139">In this case, you receive the following error message:</span></span>

> <span data-ttu-id="48ef7-140">品目の在庫がないため、倉庫の場所を作成できません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-140">The warehouse location cannot be created because the item is not stocked.</span></span> <span data-ttu-id="48ef7-141">品目の在庫を確保するには、関連付けられている品目モデル グループの在庫製品オプションを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-141">To stock items, the Stocked product option on the associated item model group must be selected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-142">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-142">Issue resolution</span></span>

<span data-ttu-id="48ef7-143">製品テンプレートを作成するプロセスには、追加の製品固有のロジックが必要です。</span><span class="sxs-lookup"><span data-stu-id="48ef7-143">The process of creating product templates requires extra product-specific logic.</span></span> <span data-ttu-id="48ef7-144">したがって、この目的では、汎用の **会社コード テンプレート** ボタンを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-144">Therefore, you can't use the generic **Company accounts template** button for this purpose.</span></span> <span data-ttu-id="48ef7-145">代わりに、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-145">Instead, follow these steps.</span></span>

1. <span data-ttu-id="48ef7-146">リリース済製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-146">Open a released product.</span></span>
1. <span data-ttu-id="48ef7-147">アクション ペインで、**製品** タブの **新規** グループで、**テンプレート \> 共有テンプレートの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-147">On the Action Pane, on the **Product** tab, in the **New** group, select **Template \> Create shared template**.</span></span>

## <a name="default-help-text-that-is-added-in-product-attributes-isnt-entered-in-a-released-product"></a><span data-ttu-id="48ef7-148">製品属性に追加された既定のヘルプ テキストは、リリース済み製品に入力されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-148">Default Help text that is added in product attributes isn't entered in a released product.</span></span>

<span data-ttu-id="48ef7-149">製品属性に追加された説明およびヘルプ テキストは、リリース済み製品では既定で表示または入力できません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-149">A description and Help text that are added in the product attributes aren't visible or entered by default in the released products.</span></span> <span data-ttu-id="48ef7-150">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="48ef7-150">This behavior is by design.</span></span>

## <a name="the-default-quantity-that-is-entered-differs-when-its-registered-from-a-bom-and-when-its-registered-from-a-bom-version"></a><span data-ttu-id="48ef7-151">入力される既定の数量が、BOM から登録されるときと、BOM バージョンから登録されたときで異なります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-151">The default quantity that is entered differs when it's registered from a BOM and when it's registered from a BOM version.</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-152">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-152">Issue description</span></span>

<span data-ttu-id="48ef7-153">既定では、BOM に品目を追加すると、数量が、選択された製品の **既定の注文設定** ページの **最小注文数量** フィールドで定義されている数量ではなく、1 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-153">By default, when you add an item to a BOM, the quantity is set to 1 instead of the quantity that is defined in the **Min. order quantity** field on the **Default order settings** page for a selected product.</span></span> <span data-ttu-id="48ef7-154">ただし、BOM バージョンから品目を追加する場合で、品目とバリアントが選択されている場合、既定で入力された数量は、特定の分析コードに対する既定の注文設定で設定された最小数量を考慮します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-154">However, when you add an item from a BOM version, and the item and variant are selected, the quantity that is entered by default takes into account the minimum quantity that is set in the default order settings for the specific dimensions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-155">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-155">Issue resolution</span></span>

<span data-ttu-id="48ef7-156">この動作は予期されています。</span><span class="sxs-lookup"><span data-stu-id="48ef7-156">This behavior is expected.</span></span> <span data-ttu-id="48ef7-157">ただし、BOM ではロジックが異なり、BOM バージョンは既知の問題であるという事実もあります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-157">However, the fact that the logic differs in the BOM and the BOM version is a known issue.</span></span> <span data-ttu-id="48ef7-158">それでも、変更はさまざまな顧客のシナリオに影響する可能性があるため、この動作は変更されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-158">Nevertheless, this behavior won't be changed, because a change could affect many different customer scenarios.</span></span>

## <a name="in-the-released-product-details-i-cant-change-the-attached-images-that-were-uploaded-from-the-product-document-attachments-data-entity"></a><span data-ttu-id="48ef7-159">リリース済み製品の詳細では、製品ドキュメントの添付ファイル データ エンティティからアップロードされた添付画像を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-159">In the released product details, I can't change the attached images that were uploaded from the Product document attachments data entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-160">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-160">Issue description</span></span>

<span data-ttu-id="48ef7-161">この問題は、*製品ドキュメントの添付ファイル* データ エンティティを使用して画像を品目に関連付けた場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-161">This issue can occur when you attach an image to an item by using the *Product document attachments* data entity.</span></span> <span data-ttu-id="48ef7-162">この場合、品目の品目画像が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-162">In this case, the item image is shown for the item.</span></span> <span data-ttu-id="48ef7-163">ただし、**画像の変更** を選択した場合、アップロードした画像の一覧には何も表示されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-163">However, if you select **Change image**, nothing is shown in the list of uploaded images.</span></span> <span data-ttu-id="48ef7-164">また、この品目の添付ファイルは表示されません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-164">Additionally, no attachments are shown for the item.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-165">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-165">Issue resolution</span></span>

<span data-ttu-id="48ef7-166">*EcoResProductDocumentAttachmentEntity* エンティティ (*製品ドキュメントの添付ファイル*) は、*製品* のドキュメント添付ファイルをインポートしますが、*リリース済製品* の添付ファイルはインポートしません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-166">The *EcoResProductDocumentAttachmentEntity* entity (*Product document attachments*) imports document attachments for *products* but not for *released products*.</span></span> <span data-ttu-id="48ef7-167">(リリース済み製品は *品目* と呼ばれることもあります)。**リリース済み製品の詳細** ページで、品目の添付ファイルを表示するには、代わりに *EcoResReleasedProductDocumentAttachmentEntity* エンティティ (*リリース済み製品ドキュメント添付ファイル*) を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-167">(Released products are also known as *items*.) To view the attachments for an item on the **Released product details** page, you must use the *EcoResReleasedProductDocumentAttachmentEntity* entity (*Released product document attachments*) instead.</span></span>

## <a name="the-microsoft-flow-connector-shows-the-following-error-message-update-not-allowed-for-field-productnumber"></a><span data-ttu-id="48ef7-168">Microsoft Flow コネクタに、エラーメッセージ "ProductNumber フィールドの更新は許可されていません" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-168">The Microsoft Flow connector shows the following error message: "Update not allowed for field 'ProductNumber'."</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-169">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-169">Issue description</span></span>

<span data-ttu-id="48ef7-170">この問題は、*リリース済み製品* エンティティ V2 と Microsoft Flow を使用して **製品番号** フィールドを更新しようとすると発生します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-170">This issue occurs if you try to update the **Product number** field by using the *Released products* entity V2 and Microsoft Flow.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-171">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-171">Issue resolution</span></span>

<span data-ttu-id="48ef7-172">この動作は予期されています。</span><span class="sxs-lookup"><span data-stu-id="48ef7-172">This behavior is expected.</span></span> <span data-ttu-id="48ef7-173">リリース済み製品の製品番号を編集する機能は、データの破損を防ぐため、Dynamics 365 Finance and Operations 10.0.0 プラットフォーム更新プログラム 24 で削除されました。</span><span class="sxs-lookup"><span data-stu-id="48ef7-173">The ability to edit the product number for a released product was removed in Dynamics 365 Finance and Operations 10.0.0 with platform update 24 to help prevent data corruption.</span></span> <span data-ttu-id="48ef7-174">リリース済み製品の主キーの以前の名前変更によって発生したデータ破損を修復する必要がある例外的なケースでは、Microsoft サポートに対して、この制限を一時的に解除するように依頼することができます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-174">In exceptional cases, where you must repair data corruption that was caused by a previous rename of the primary key of a released product, you can ask Microsoft Support to temporarily remove this restriction.</span></span>

## <a name="i-cant-create-a-released-product-variant-in-another-legal-entity"></a><span data-ttu-id="48ef7-175">別の法人にリリース済の製品バリアントを作成できません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-175">I can't create a released product variant in another legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-176">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-176">Issue description</span></span>

<span data-ttu-id="48ef7-177">バリアントを指定しないで製品マスターをリリースし、必要に応じて各法人 (会社) にバリアントを作成する場合は、バリアントの提案を使用してバリアントをリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-177">If you try to release a product master without variants, and then create the variants in each legal entity (company) as they are required, you won't be able to release the variants by using variant suggestions.</span></span> <span data-ttu-id="48ef7-178">バリアントを手動で作成することもできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-178">You also won't be able to manually create the variants.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-179">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-179">Issue resolution</span></span>

<span data-ttu-id="48ef7-180">この動作は仕様です。</span><span class="sxs-lookup"><span data-stu-id="48ef7-180">This behavior is by design.</span></span> <span data-ttu-id="48ef7-181">製品マスターの関係と、マスターで実行できる分析コードは、共有レベルで維持されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-181">The relations of a product master and the dimensions that the master can take are kept at a shared level.</span></span> <span data-ttu-id="48ef7-182">したがって、これらの分析コードがリリースされた特定の法人で共有の製品マスターに対して使用できる分析コードを作成し、分析コードが必要な各法人にプロセスをレプリケートすることはできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-182">Therefore, you can't create the available dimensions for a shared product master in the specific legal entity where those dimensions are released and then replicate the process in each legal entity where the dimensions are required.</span></span> <span data-ttu-id="48ef7-183">代わりに、設計されたプロセスに対応するようにリリース プロセスを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48ef7-183">Instead, you must change your release process to adapt to the designed process.</span></span>

<span data-ttu-id="48ef7-184">製品のリリース プロセスは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="48ef7-184">Here is the process for releasing products.</span></span>

1. <span data-ttu-id="48ef7-185">法人にリリースできる共有製品マスターと分析コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="48ef7-185">Create the shared product master and the dimensions that can be released to the legal entities.</span></span>
1. <span data-ttu-id="48ef7-186">バリアント提案を使用するか、リリースする必要のある組み合わせを手動で追加することによって、製品を法人にリリースします。</span><span class="sxs-lookup"><span data-stu-id="48ef7-186">Release the products to the legal entities either by using variant suggestions or by manually adding the combinations that should be released.</span></span>

<span data-ttu-id="48ef7-187">または、リリース済み製品を直接作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-187">Alternatively, you can directly create the released product.</span></span>

## <a name="when-i-release-a-variant-in-another-company-i-receive-the-following-error-message-product-variant-with-specified-dimensions-has-already-been-created"></a><span data-ttu-id="48ef7-188">別の会社でバリアントをリリースすると、エラー メッセージ "指定された分析コードを持つ商品バリエーションは既に作成されています" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-188">When I release a variant in another company, I receive the following error message: "Product variant with specified dimensions has already been created."</span></span>

### <a name="issue-description"></a><span data-ttu-id="48ef7-189">問題の説明</span><span class="sxs-lookup"><span data-stu-id="48ef7-189">Issue description</span></span>

<span data-ttu-id="48ef7-190">製品バリアントが会社 A で既にリリースされている場合に、**リリース済み製品バリアント** ページの **新規** ボタンを使用して会社 B でそのバリアントをリリースしようとすると 、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-190">If a product variant has already been released in a company A, and you try to release it in company B by using the **New** button on the **Released product variants** page, you will receive the following error message:</span></span>

> <span data-ttu-id="48ef7-191">指定された分析コードを持つ製品バリアントは、既に作成されています。</span><span class="sxs-lookup"><span data-stu-id="48ef7-191">Product variant with specified dimensions has already been created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="48ef7-192">問題の解決</span><span class="sxs-lookup"><span data-stu-id="48ef7-192">Issue resolution</span></span>

<span data-ttu-id="48ef7-193">**リリース済製品バリアント** ページの **新規** ボタンをクリックするとバリアントが作成され、会社コンテキストでリリースされます。</span><span class="sxs-lookup"><span data-stu-id="48ef7-193">The **New** button on the **Released product variants** page creates the variant and releases it in the company context.</span></span> <span data-ttu-id="48ef7-194">バリアントが既に作成されている場合は、**新規** ボタンを使用して別の会社にリリースすることはできません。</span><span class="sxs-lookup"><span data-stu-id="48ef7-194">If the variant has already been created, you can't use the **New** button to release it in another company.</span></span>

<span data-ttu-id="48ef7-195">この問題を解決するには、**製品マスター** ページを開き、**製品のリリース** を選択して、目的の会社の既存のバリアントをリリースします。</span><span class="sxs-lookup"><span data-stu-id="48ef7-195">To fix the issue, open the **Product master** page, and select **Release product** to release the existing variant in the desired company.</span></span>

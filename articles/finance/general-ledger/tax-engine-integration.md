---
title: 税エンジンの統合
description: このトピックでは、税エンジンの統合について説明します。
author: yijialuan
manager: AnnBe
ms.date: 12/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable
audience: IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: f38e566ffa74d58742665bfba27135646eccc74b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175678"
---
# <a name="tax-engine-integration"></a><span data-ttu-id="53d63-103">税エンジンの統合</span><span class="sxs-lookup"><span data-stu-id="53d63-103">Tax engine integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53d63-104">[税エンジン](tax-engine.md) (GTE とも呼ばれます) を Dynamics 365 Finance と統合するには、税計算のために税エンジンとやり取りする X++ コードを実装する必要があります。それは結果を消費して、伝票および税トランザクションの税金の表示、計算、および転記を行います。</span><span class="sxs-lookup"><span data-stu-id="53d63-104">To integrate the [Tax engine](tax-engine.md) (also referred to as GTE) with Dynamics 365 Finance, you must implement X++ code that interacts with the Tax engine for tax calculation, and that consumes the results to show, account, and post tax for voucher and tax transactions.</span></span> <span data-ttu-id="53d63-105">(税計算では、税調整を含める、または除外することができます。)</span><span class="sxs-lookup"><span data-stu-id="53d63-105">(The tax calculation can either include or exclude tax adjustment.)</span></span> 

> [!NOTE]
> <span data-ttu-id="53d63-106">税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="53d63-106">The Tax engine functionality is only available for legal entities with a primary address in India.</span></span>

## <a name="tax-engine-integration-models"></a><span data-ttu-id="53d63-107">税エンジンの統合モデル</span><span class="sxs-lookup"><span data-stu-id="53d63-107">Tax engine integration models</span></span>
<span data-ttu-id="53d63-108">税エンジンの統合には 3 つのモデルがあります。</span><span class="sxs-lookup"><span data-stu-id="53d63-108">There are three models for Tax engine integration:</span></span>

- <span data-ttu-id="53d63-109">税エンジン サービスを使用した税エンジン インターフェース</span><span class="sxs-lookup"><span data-stu-id="53d63-109">Tax engine interfaces with the Tax engine service</span></span>
- <span data-ttu-id="53d63-110">税 ビジネス サービス</span><span class="sxs-lookup"><span data-stu-id="53d63-110">Tax business service</span></span>
- <span data-ttu-id="53d63-111">Finance アプリケーション統合:</span><span class="sxs-lookup"><span data-stu-id="53d63-111">Finance application integration:</span></span>
    - <span data-ttu-id="53d63-112">アプリケーションの統合</span><span class="sxs-lookup"><span data-stu-id="53d63-112">Application integration</span></span>
    - <span data-ttu-id="53d63-113">会計の統合</span><span class="sxs-lookup"><span data-stu-id="53d63-113">Accounting integration</span></span>

![GTE 統合モデル](./media/gte-3-models.PNG)

###  <a name="tax-engine-interfaces-with-the-tax-engine-service-model"></a><span data-ttu-id="53d63-115">税エンジン サービス モデルを使用した税エンジン インターフェース</span><span class="sxs-lookup"><span data-stu-id="53d63-115">Tax engine interfaces with the Tax engine service model</span></span>

<span data-ttu-id="53d63-116">このモデルは、Finance の統合フレームワークの一部です。</span><span class="sxs-lookup"><span data-stu-id="53d63-116">This model is part of the Finance integration framework.</span></span> <span data-ttu-id="53d63-117">したがって、パートナーや顧客にはほとんど取得の必要がありません。</span><span class="sxs-lookup"><span data-stu-id="53d63-117">Therefore, almost no uptake is required for partners or customers.</span></span>

<span data-ttu-id="53d63-118">ITaxEngine インターフェースとその実装には、税エンジンの基本操作が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53d63-118">The ITaxEngine interface and its implementation contain the basic operations of the Tax engine.</span></span> <span data-ttu-id="53d63-119">これらの操作には、税エンジンを介した税の計算、Finance テーブルへの計算結果の保持、トランザクションの税務書類の取得、税エンジンキャッシュと Finance テーブルの両方からの税務書類の削除が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d63-119">These operations include calculating tax through the tax engine, persisting the calculated result to Finance tables, retrieving the tax document for the transaction, and deleting the tax document from both the Tax engine cache and Finance tables.</span></span>

<span data-ttu-id="53d63-120">ITaxDocument インターフェイスと実装のセットにより、税エンジンが計算して返す税務書類から情報を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="53d63-120">The set of ITaxDocument interfaces and implementations enables information to be read from a tax document that the Tax engine calculates and returns.</span></span> <span data-ttu-id="53d63-121">このセットには、ITaxDocument、ITaxDocumentLine、ITaxDocumentField、ITaxDocumentComponentLine、およびITaxDocumentMeasure が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d63-121">This set includes ITaxDocument, ITaxDocumentLine, ITaxDocumentField, ITaxDocumentComponentLine, and ITaxDocumentMeasure.</span></span>

![GTE インターフェイス](./media/gte-itaxdocument_interfaces.jpg)

<span data-ttu-id="53d63-123">これらのインタフェースは、ITaxDocumentLine から指定されたフィールド値 (**ITaxDocumentField**) および ITaxDocumentComponentLine から予測される数値 (**ITaxDocumentMeasure**) を取得するためのメソッドも提供します。</span><span class="sxs-lookup"><span data-stu-id="53d63-123">These interfaces also provide methods for retrieving a specified field value (**ITaxDocumentField**) from ITaxDocumentLine and an expected measure value (**ITaxDocumentMeasure**) from ITaxDocumentComponentLine.</span></span>

- <span data-ttu-id="53d63-124">ITaxDocumentMetaData インターフェイスのセットにより、税務文書からモデル情報を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="53d63-124">The set of ITaxDocumentMetaData interfaces enables model information to be read from a tax document.</span></span> <span data-ttu-id="53d63-125">このセットには、ITaxDocumentMetaData、ITaxDocumentLineMetaData、ITaxDocumentComponentLineMetaData、および ITaxDocumentMeasureMetaData が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d63-125">This set includes ITaxDocumentMetaData, ITaxDocumentLineMetaData, ITaxDocumentComponentLineMetaData, and ITaxDocumentMeasureMetaData.</span></span>
- <span data-ttu-id="53d63-126">ITaxDocumentEnumerator および ITaxDocumentMeataDataEnumerator インターフェイスのセットは、ITaxDocumentLine、ITaxDocumentField、ITaxDocumentComponentLine、および ITaxDocumentMeasure などの税務書類関連オブジェクトのリストを読み取るための列挙子を提供します。</span><span class="sxs-lookup"><span data-stu-id="53d63-126">The set of ITaxDocumentEnumerator and ITaxDocumentMeataDataEnumerator interfaces provides an enumerator to read a list of tax document–related objects, such as ITaxDocumentLine, ITaxDocumentField, ITaxDocumentComponentLine, and ITaxDocumentMeasure.</span></span>

### <a name="tax-business-service-model"></a><span data-ttu-id="53d63-127">税ビジネス サービス モデル</span><span class="sxs-lookup"><span data-stu-id="53d63-127">Tax business service model</span></span>

<span data-ttu-id="53d63-128">税ビジネス サービス モデルは、Finance の統合フレームワークの一部であり、パートナーや顧客にはほとんど取得の必要がありません。</span><span class="sxs-lookup"><span data-stu-id="53d63-128">The Tax business service model is part of the Finance integration framework, and almost no uptake is required for partners or customers.</span></span> <span data-ttu-id="53d63-129">このモデルは、Finance アプリケーションが基本的な操作のために税エンジンと相互作用することをサポートします。</span><span class="sxs-lookup"><span data-stu-id="53d63-129">This model supports the interactions that the Finance application has with the Tax engine for basic operations.</span></span> <span data-ttu-id="53d63-130">インタフェース モデルとアプリケーション モデルの両方を使用して、税の計算、会計、および転記を行います。</span><span class="sxs-lookup"><span data-stu-id="53d63-130">It uses both the interface model and the application model to calculate, account, and post tax.</span></span> <span data-ttu-id="53d63-131">税ビジネス サービス モデルでは、次の方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="53d63-131">The Tax business service model provides the following methods:</span></span>

<table>
<tr>
<td><span data-ttu-id="53d63-132"><strong>メソッド</strong></span><span class="sxs-lookup"><span data-stu-id="53d63-132"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="53d63-133"><strong>説明</strong>
</span><span class="sxs-lookup"><span data-stu-id="53d63-133"><strong>Description</strong>
</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-134">税の計算</span><span class="sxs-lookup"><span data-stu-id="53d63-134">CalculateTax</span></span></td>
    <td> <span data-ttu-id="53d63-135"><strong>ダーティー</strong>とマークされている場合は、税務書類を削除してから税金を計算します。</span><span class="sxs-lookup"><span data-stu-id="53d63-135">Delete a tax document if it&#39;s marked as <strong>Dirty</strong>, and then calculate tax.</span></span><ul>
<li><span data-ttu-id="53d63-136"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-136"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-137"><strong>出力</strong>: 税務署類オブジェクト</span><span class="sxs-lookup"><span data-stu-id="53d63-137"><strong>Output</strong>: Tax document object</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-138">税の再計算</span><span class="sxs-lookup"><span data-stu-id="53d63-138">RecalculateTax</span></span></td>
<td><span data-ttu-id="53d63-139">明示的に税務書類を再計算します。</span><span class="sxs-lookup"><span data-stu-id="53d63-139">Explicitly recalculate a tax document.</span></span>
<ul>
<li><span data-ttu-id="53d63-140"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-140"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-141"><strong>出力</strong>: 税務署類オブジェクト</span><span class="sxs-lookup"><span data-stu-id="53d63-141"><strong>Output</strong>: Tax document object</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-142">SaveTaxDocument</span><span class="sxs-lookup"><span data-stu-id="53d63-142">SaveTaxDocument</span></span></td>
<td><span data-ttu-id="53d63-143">税務書類を Finance データベースに保存します。</span><span class="sxs-lookup"><span data-stu-id="53d63-143">Persist a tax document to the Finance database.</span></span>
 <ul>
<li><span data-ttu-id="53d63-144"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-144"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-145"><strong>出力</strong>: 該当なし</span><span class="sxs-lookup"><span data-stu-id="53d63-145"><strong>Output</strong>: Not applicable</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-146">GetTaxDocumentBySource</span><span class="sxs-lookup"><span data-stu-id="53d63-146">GetTaxDocumentBySource</span></span></td>
<td><span data-ttu-id="53d63-147">ソース トランザクション ID に基づいて税務書類を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="53d63-147">Read a tax document, based on the source transaction identifier.</span></span> <ul>
<li><span data-ttu-id="53d63-148"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-148"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-149"><strong>出力</strong>: 税務署類オブジェクト</span><span class="sxs-lookup"><span data-stu-id="53d63-149"><strong>Output</strong>: Tax document object</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-150">GetTaxDocumentLineBySource</span><span class="sxs-lookup"><span data-stu-id="53d63-150">GetTaxDocumentLineBySource</span></span></td>
<td><span data-ttu-id="53d63-151">ソース トランザクション明細行 ID に基づいて税務書類明細行を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="53d63-151">Read a tax document line, based on the source transaction line identifier.</span></span> <ul>
<li><span data-ttu-id="53d63-152"><strong>入力</strong>: トランザクション明細行識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-152"><strong>Input</strong>: Transaction line identifier</span></span></li>
<li><span data-ttu-id="53d63-153"><strong>出力</strong>: 税務署類明細行オブジェクト</span><span class="sxs-lookup"><span data-stu-id="53d63-153"><strong>Output</strong>: Tax document line object</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-154">GetTaxDocumentTaxStatus</span><span class="sxs-lookup"><span data-stu-id="53d63-154">GetTaxDocumentTaxStatus</span></span></td>
<td><span data-ttu-id="53d63-155">関連するトランザクションの税務書類のステータスを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="53d63-155">Read the status of a tax document for the associated transaction.</span></span>
 <ul>
<li><span data-ttu-id="53d63-156"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-156"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-157"><strong>出力</strong>: 税務署類オブジェクト</span><span class="sxs-lookup"><span data-stu-id="53d63-157"><strong>Output</strong>: Tax document object</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-158">MarkTaxDocumentTaxStatus</span><span class="sxs-lookup"><span data-stu-id="53d63-158">MarkTaxDocumentTaxStatus</span></span></td>
<td><span data-ttu-id="53d63-159">下線を引いたトランザクションが更新されたら、税務文書を<strong>ダーティー</strong>としてマークします。</span><span class="sxs-lookup"><span data-stu-id="53d63-159">Mark a tax document as <strong>Dirty</strong> when the underlining transaction has been updated.</span></span> <ul>
<li><span data-ttu-id="53d63-160"><strong>入力</strong>: 課税対象文書の識別子、税務書類のステータス</span><span class="sxs-lookup"><span data-stu-id="53d63-160"><strong>Input</strong>: Taxable document identifier, Tax document status</span></span></li>
<li><span data-ttu-id="53d63-161"><strong>出力</strong>: 該当なし</span><span class="sxs-lookup"><span data-stu-id="53d63-161"><strong>Output</strong>: Not applicable</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-162">DeleteTaxDocument</span><span class="sxs-lookup"><span data-stu-id="53d63-162">DeleteTaxDocument</span></span></td>
<td><span data-ttu-id="53d63-163">トランザクションが削除された場合に、税務書類を削除します。</span><span class="sxs-lookup"><span data-stu-id="53d63-163">Delete a tax document when the transaction is deleted.</span></span> <ul>
<li><span data-ttu-id="53d63-164"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-164"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-165"><strong>出力</strong>: 該当なし</span><span class="sxs-lookup"><span data-stu-id="53d63-165"><strong>Output</strong>: Not applicable</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-166">PostTax</span><span class="sxs-lookup"><span data-stu-id="53d63-166">PostTax</span></span></td>
<td><span data-ttu-id="53d63-167">トランザクションの税金を転記します。</span><span class="sxs-lookup"><span data-stu-id="53d63-167">Post tax for the transaction.</span></span> <ul>
<li><span data-ttu-id="53d63-168"><strong>入力</strong>: 転記する必要がある税の元帳伝票、課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-168"><strong>Input</strong>: Ledger voucher for the tax that must be posted, Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-169"><strong>出力</strong>: 該当なし</span><span class="sxs-lookup"><span data-stu-id="53d63-169"><strong>Output</strong>: Not applicable</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-170">TransferTaxDocument</span><span class="sxs-lookup"><span data-stu-id="53d63-170">TransferTaxDocument</span></span></td>
<td><span data-ttu-id="53d63-171">ソースがサポートしているトランザクションから別のトランザクションに税務書類を転送します。</span><span class="sxs-lookup"><span data-stu-id="53d63-171">Transfer a tax document from one transaction that the source supports to another transaction.</span></span>
<ul>
<li><span data-ttu-id="53d63-172"><strong>入力</strong>: ソース トランザクション、ターゲット トランザクション</span><span class="sxs-lookup"><span data-stu-id="53d63-172"><strong>Input</strong>: Source transaction, Target transaction</span></span></li>
<li><span data-ttu-id="53d63-173"><strong>出力</strong>: 該当なし</span><span class="sxs-lookup"><span data-stu-id="53d63-173"><strong>Output</strong>: Not applicable</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="53d63-174">PostTaxDocument</span><span class="sxs-lookup"><span data-stu-id="53d63-174">PostTaxDocument</span></span></td>
<td><span data-ttu-id="53d63-175">税務文書のステータスを <strong>転記済</strong>に変更するだけです。</span><span class="sxs-lookup"><span data-stu-id="53d63-175">Just change the status of the tax document to <strong>Posted</strong>.</span></span> <ul>
<li><span data-ttu-id="53d63-176"><strong>入力</strong>: 課税対象文書の識別子</span><span class="sxs-lookup"><span data-stu-id="53d63-176"><strong>Input</strong>: Taxable document identifier</span></span></li>
<li><span data-ttu-id="53d63-177"><strong>出力</strong>: 該当なし</span><span class="sxs-lookup"><span data-stu-id="53d63-177"><strong>Output</strong>: Not applicable</span></span></li>
</ul>
</td>
</tr>
</table>

### <a name="finance-application-integration"></a><span data-ttu-id="53d63-178">Finance アプリケーション統合</span><span class="sxs-lookup"><span data-stu-id="53d63-178">Finance application integration</span></span>

<span data-ttu-id="53d63-179">Finance からのトランザクション情報は、税エンジンに送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-179">Transaction information from Finance should be sent to the Tax engine.</span></span> <span data-ttu-id="53d63-180">同時に、税の会計と転記は、Finance の実装と整合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-180">At the same time, the accounting and posting of tax should be aligned with the Finance implementation.</span></span> <span data-ttu-id="53d63-181">そのため、Finance アプリケーションでは 3 つの部分が作成されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-181">Therefore, three parts are created in the Finance application:</span></span>

- <span data-ttu-id="53d63-182">課税対象文書</span><span class="sxs-lookup"><span data-stu-id="53d63-182">Taxable document</span></span>
- <span data-ttu-id="53d63-183">税会計</span><span class="sxs-lookup"><span data-stu-id="53d63-183">Tax accounting</span></span>
- <span data-ttu-id="53d63-184">税転記</span><span class="sxs-lookup"><span data-stu-id="53d63-184">Tax posting</span></span>

<span data-ttu-id="53d63-185">一方、統合では、輸送文書フレームワークを使用して、Finance トランザクションと税務書類の間の関係を維持します。</span><span class="sxs-lookup"><span data-stu-id="53d63-185">Meanwhile, the integration uses the transit document framework to maintain the relationship between the Finance transaction and the tax document.</span></span>

#### <a name="application-integration"></a><span data-ttu-id="53d63-186">アプリケーションの統合</span><span class="sxs-lookup"><span data-stu-id="53d63-186">Application integration</span></span>

##### <a name="taxable-document"></a><span data-ttu-id="53d63-187">課税対象文書</span><span class="sxs-lookup"><span data-stu-id="53d63-187">Taxable document</span></span>

<span data-ttu-id="53d63-188">課税対象文書は、一連のデータ プロバイダーを使用して、トランザクションの情報をカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="53d63-188">A taxable document encapsulates transaction information by using a set of data providers.</span></span> <span data-ttu-id="53d63-189">トランザクションの情報は、TaxableDocument オブジェクトによってラップされます。</span><span class="sxs-lookup"><span data-stu-id="53d63-189">Transaction information is wrapped by a TaxableDocument object.</span></span> <span data-ttu-id="53d63-190">このオブジェクトの TaxableDocumentDescriptor オブジェクトは、トランザクションとは何かを説明し、税モデル属性をトランザクション データにバインドする一連のデータ プロバイダーをリストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-190">A TaxableDocumentDescriptor object in this object should describe what the transaction is, and it should list a set of data providers that bind tax model attributes with transaction data.</span></span>

![課税対象文書](media/gte-taxable-doc.png)

<span data-ttu-id="53d63-192">**TaxableDocumentDescriptor** は、一連の TaxableDocumentTypeDefinition インターフェイスを実装し、トランザクションとは何かを説明するクラスです。</span><span class="sxs-lookup"><span data-stu-id="53d63-192">**TaxableDocumentDescriptor** is the class that implements a set of TaxableDocumentTypeDefinition interfaces and describes what the transaction is.</span></span> <span data-ttu-id="53d63-193">技術的には、TaxableDocumentDescriptors は Finance のテーブル ベースですが、TaxableDocumentTypeDefinitions はよりビジネス主導型であり、主に税の設定条件に使用されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-193">Technically, TaxableDocumentDescriptors are the Finance table bases, whereas TaxableDocumentTypeDefinitions are more business-driven and are used mainly for tax configuration conditions.</span></span>

<span data-ttu-id="53d63-194">次の例では、TaxableDocumentDescriptorPurchaseOrderParm は、同じ PurchParmTable テーブルを共有する 3 つのインターフェースを実装します。</span><span class="sxs-lookup"><span data-stu-id="53d63-194">In the following example, TaxableDocumentDescriptorPurchaseOrderParm implements three interfaces that share the same PurchParmTable table.</span></span>

![共有テーブルの例](media/gte-example-shared-table.png)

<span data-ttu-id="53d63-196">追加の属性が税コンフィギュレーションに追加され、それらがルックアップ、条件、式、またはその他のコンフィギュレーションに使用される場合は、属性をトランザクション データとバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-196">If additional attributes are added to a tax configuration, and they are used for lookup, condition, formula, or other configurations, you should bind the attributes with transaction data.</span></span> <span data-ttu-id="53d63-197">したがって、トランザクションに対応するデータ プロバイダー クラスを変更して、このようなデータ バインディングが行われるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-197">Therefore, you should modify the corresponding data provider classes for a transaction so that they do this type of data binding.</span></span>

> [!NOTE]
> <span data-ttu-id="53d63-198">追加のトランザクションが GTE をサポートする必要がある場合は、関連する TaxableDocumentTypeDefinitions、TaxableDocumentDescriptors、および TaxableDocumentDataProviders を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-198">If additional transactions should support GTE, you should create related TaxableDocumentTypeDefinitions, TaxableDocumentDescriptors, and TaxableDocumentDataProviders.</span></span>

##### <a name="transit-document"></a><span data-ttu-id="53d63-199">輸送文書</span><span class="sxs-lookup"><span data-stu-id="53d63-199">Transit document</span></span>

<span data-ttu-id="53d63-200">輸送文書は、次の 2 つの目的に使用される Finance の既存のフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="53d63-200">A transit document is an existing framework in Finance that is used for the following two purposes:</span></span>

- <span data-ttu-id="53d63-201">トランザクションおよび輸送文書間の関係を維持します。</span><span class="sxs-lookup"><span data-stu-id="53d63-201">Maintain the relationship between a transaction and a transit document.</span></span>
- <span data-ttu-id="53d63-202">あるトランザクションから別のトランザクションにドキュメントを転送します。</span><span class="sxs-lookup"><span data-stu-id="53d63-202">Transfer the document from one transaction to another transaction.</span></span>

<span data-ttu-id="53d63-203">このフレームワークを使用すると、トランザクションのドキュメントを簡単に見つけて輸送履歴を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="53d63-203">This framework lets you easily find a transaction's document and track the transit history.</span></span> <span data-ttu-id="53d63-204">たとえば、VendInvoiceInfoTable から税務書類が作成され、輸送ドキュメントでは VendInvoiceInfoTable と TaxDocument の関係が維持されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-204">For example, a tax document is created from VendInvoiceInfoTable, and then the transit document maintains the relationship between VendInvoiceInfoTable and TaxDocument.</span></span> <span data-ttu-id="53d63-205">発注書が請求されると、VendInvoiceInfoTable からの税務書類が VendInvoiceJour に転送されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-205">When a purchase order is invoiced, the tax document from VendInvoiceInfoTable is transferred to VendInvoiceJour.</span></span>

> [!NOTE] 
> <span data-ttu-id="53d63-206">追加のトランザクションが税エンジンをサポートする必要がある場合は、ヘッダー レベルと明細行レベルの両方から、どのトランザクションに税務書類があるかを説明するための輸送ドキュメント フレームワークのルールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-206">If additional transactions should support the Tax engine, you should define a rule for the transit document framework to describe which transaction should have a tax document from both the header level and the line level.</span></span> <span data-ttu-id="53d63-207">ルールには、ソース トランザクションからターゲット トランザクションへの輸送アクションも定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-207">The rule should also define the transit action from the source transaction to the target transaction.</span></span>

#### <a name="transaction-integration"></a><span data-ttu-id="53d63-208">トランザクションの統合</span><span class="sxs-lookup"><span data-stu-id="53d63-208">Transaction integration</span></span>

<span data-ttu-id="53d63-209">トランザクションの統合は個別でのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="53d63-209">Transaction integration occurs only on a case-by-case basis.</span></span> <span data-ttu-id="53d63-210">各トランザクションおよびシナリオに対して、税 ビジネス サービスは税計算、税の仮定、および税転記に対して適切な方法で呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-210">For each transaction and scenario, the Tax business service should be called in the appropriate manner for tax calculation, tax assumption, and tax posting.</span></span> <span data-ttu-id="53d63-211">例については、このトピックで後述する [Finance 統合の例 – 発注請求書](#example-finance-integration--purchase-order-invoice) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="53d63-211">For an example, see the [Finance integration example – Purchase order invoice](#example-finance-integration--purchase-order-invoice) section later in this topic.</span></span>

#### <a name="accounting-integration"></a><span data-ttu-id="53d63-212">会計の統合</span><span class="sxs-lookup"><span data-stu-id="53d63-212">Accounting integration</span></span>

##### <a name="tax-accounting"></a><span data-ttu-id="53d63-213">税会計</span><span class="sxs-lookup"><span data-stu-id="53d63-213">Tax accounting</span></span>

<span data-ttu-id="53d63-214">Finance トランザクションの会計には、元伝票会計と非元伝票会計の 2 つの部分があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-214">The accounting of Finance transactions has two parts: source document accounting and non-source document accounting.</span></span> <span data-ttu-id="53d63-215">同じ動作が税エンジンの税務会計にも当てはまります。税務会計は、以下の両面で Finance の実装と統合されています。</span><span class="sxs-lookup"><span data-stu-id="53d63-215">The same behavior applies to Tax engine tax accounting, which is integrated with the Finance implementation on both sides:</span></span>

- <span data-ttu-id="53d63-216">発注書やフ自由書式の請求書などの元伝票のトランザクションでは、税務書類が作成されたときに税のアカウント情報が取得されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-216">For source document transactions, such as a purchase order or free text invoice, the account information for tax is fetched when the tax document is created.</span></span>
- <span data-ttu-id="53d63-217">販売注文や一般仕訳帳などの非元伝票トランザクションの場合、アカウント情報は税が転記されるときに決定されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-217">For non-source document transactions, such as a sales order or general journal, the account information is determined when tax is posted.</span></span>

> [!NOTE]
> <span data-ttu-id="53d63-218">追加の元伝票トランザクションに税エンジンのサポートが必要な場合は、指定されたビジネス イベントと金額に対して AccountingJournalizationRule と AccountingDistributionRule を拡張するための元伝票関連クラスを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-218">If any additional source document transaction requires Tax engine support, you should create source document–related classes to extend AccountingJournalizationRule and AccountingDistributionRule for the specified business event and monetary amount.</span></span>

##### <a name="tax-engine-tax-posting"></a><span data-ttu-id="53d63-219">税エンジン税転記</span><span class="sxs-lookup"><span data-stu-id="53d63-219">Tax engine tax posting</span></span>

<span data-ttu-id="53d63-220">現在、税エンジンの税転記により、TaxTrans、TaxTrans\_IN (インドの国/地域コードで実行している場合)、および TaxTrans の関連伝票が生成されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-220">Currently, Tax engine tax posting generates TaxTrans, TaxTrans\_IN (if you're running under the India country/region code), and a related voucher for TaxTrans.</span></span> <span data-ttu-id="53d63-221">**taxTrans** フィールドに税務書類の属性または基準を入力するには、**TaxAcctTaxTransTaxDocAttrMapping** および **TaxAcctTxTransTaxDocMeasureMapping** を使用してマッピングを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-221">In order for the **taxTrans** field to be filled with attributes or measures from the tax document, the mapping should be provided via **TaxAcctTaxTransTaxDocAttrMapping** and **TaxAcctTxTransTaxDocMeasureMapping**.</span></span>

<span data-ttu-id="53d63-222">次の図は、TaxTrans および伝票の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="53d63-222">The following illustration shows how TaxTrans and the voucher are created.</span></span>

![TaxTrans および伝票の作成](media/gte-create-taxtrans-voucher.png)

> [!NOTE]
> <span data-ttu-id="53d63-224">**taxTrans** フィールドに税務書類の追加フィールドを入力する必要がある場合は、 **TaxAcctTaxTransTaxDocAttrMapping** クラス、**TaxAcctTxTransTaxDocMeasureMapping** クラス、またはこれらのクラスのいずれかの拡張クラスをデータ バインディングに適切な方法で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-224">If **taxTrans** fields should be filled with additional fields from the tax document, you should update the **TaxAcctTaxTransTaxDocAttrMapping** class, the **TaxAcctTxTransTaxDocMeasureMapping** class, or the extended classes of one of these classes in the appropriate manner for data binding.</span></span>

## <a name="example-finance-integration--purchase-order-invoice"></a><span data-ttu-id="53d63-225">例: Finance の統合 – 発注請求書</span><span class="sxs-lookup"><span data-stu-id="53d63-225">Example: Finance integration – Purchase order invoice</span></span>

<span data-ttu-id="53d63-226">このセクションでは、税エンジンが発注請求書とどのように統合されるかの例を示します。</span><span class="sxs-lookup"><span data-stu-id="53d63-226">This section provides an example of how the Tax engine is integrated with purchase order invoices.</span></span> <span data-ttu-id="53d63-227">関連するトランザクション テーブルには、VendInvoiceInfoTable、VendInvoiceInfoLine、VendInvoiceJour、およびVendInvoiceTrans が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d63-227">Related transaction tables include VendInvoiceInfoTable, VendInvoiceInfoLine, VendInvoiceJour, and VendInvoiceTrans.</span></span>

### <a name="integration-checklist"></a><span data-ttu-id="53d63-228">統合 チェックリスト</span><span class="sxs-lookup"><span data-stu-id="53d63-228">Integration checklist</span></span>

<span data-ttu-id="53d63-229">以下の表は、発注請求書との統合に関連するすべての該当する変更をまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="53d63-229">The following table summarizes all relevant changes that are related to the integration with purchase order invoices.</span></span>

<table>
<tr>
<th colspan="2"><span data-ttu-id="53d63-230">トランザクションの取得のチェックリスト</span><span class="sxs-lookup"><span data-stu-id="53d63-230">Transaction uptake checklist</span></span></th>
<th><span data-ttu-id="53d63-231">説明</span><span class="sxs-lookup"><span data-stu-id="53d63-231">Description</span></span></th>
<th><span data-ttu-id="53d63-232">AOT オブジェクト</span><span class="sxs-lookup"><span data-stu-id="53d63-232">AOT object</span></span></th>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="53d63-233">定義</span><span class="sxs-lookup"><span data-stu-id="53d63-233">Definition</span></span></td>
<td><span data-ttu-id="53d63-234">課税対象文書を定義します。</span><span class="sxs-lookup"><span data-stu-id="53d63-234">Define a taxable document.</span></span></td>
<td><span data-ttu-id="53d63-235">課税対象文書タイプとトランザクションの説明を作成します。</span><span class="sxs-lookup"><span data-stu-id="53d63-235">Create the taxable document type and description to describe what the transaction is.</span></span></td>
<td><span data-ttu-id="53d63-236">TaxableDocumentTypeDefinitionPurchaseInvoice</span><span class="sxs-lookup"><span data-stu-id="53d63-236">TaxableDocumentTypeDefinitionPurchaseInvoice</span></span><br>
<span data-ttu-id="53d63-237">TaxableDocumentDescriptorPurchaseInvoice</span><span class="sxs-lookup"><span data-stu-id="53d63-237">TaxableDocumentDescriptorPurchaseInvoice</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-238">データ プロバイダーを定義します。</span><span class="sxs-lookup"><span data-stu-id="53d63-238">Define data providers.</span></span></td>
<td><span data-ttu-id="53d63-239">トランザクション データを GTE に提供するデータ プロバイダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="53d63-239">Create data providers to provide transaction data to GTE.</span></span></td>
<td><span data-ttu-id="53d63-240">TaxableDocumentTypeDefinitionPurchaseInvoice</span><span class="sxs-lookup"><span data-stu-id="53d63-240">TaxableDocumentTypeDefinitionPurchaseInvoice</span></span><br>
<span data-ttu-id="53d63-241">TaxableDocumentDescriptorPurchaseInvoice</span><span class="sxs-lookup"><span data-stu-id="53d63-241">TaxableDocumentDescriptorPurchaseInvoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="53d63-242">作成</span><span class="sxs-lookup"><span data-stu-id="53d63-242">Creation</span></span></td>
<td><span data-ttu-id="53d63-243">トランザクションに<strong>税務書類</strong>ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="53d63-243">Add the <strong>Tax document</strong> button on a transaction.</span></span></td>
<td><span data-ttu-id="53d63-244">トランザクション ページに<strong>税務書類</strong>ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="53d63-244">Add the <strong>Tax document</strong> button to the transaction pages.</span></span></td>
<td><span data-ttu-id="53d63-245">VendEditInvoice</span><span class="sxs-lookup"><span data-stu-id="53d63-245">VendEditInvoice</span></span><br>
<span data-ttu-id="53d63-246">VendInvoiceInfoListPage</span><span class="sxs-lookup"><span data-stu-id="53d63-246">VendInvoiceInfoListPage</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-247">トランザクションの合計と統合します。</span><span class="sxs-lookup"><span data-stu-id="53d63-247">Integrate with transaction totals.</span></span></td>
<td><span data-ttu-id="53d63-248"><strong>合計</strong>ボタンをクリックすると、税務書類を作成します。</span><span class="sxs-lookup"><span data-stu-id="53d63-248">Create the tax document when the <strong>Totals</strong> button is clicked.</span></span></td>
<td><span data-ttu-id="53d63-249">PurchTotals_ParmTrans.calcTax()</span><span class="sxs-lookup"><span data-stu-id="53d63-249">PurchTotals_ParmTrans.calcTax()</span></span><br>
<span data-ttu-id="53d63-250">PurchTotals_ParmTransEdit.calcTax()</span><span class="sxs-lookup"><span data-stu-id="53d63-250">PurchTotals_ParmTransEdit.calcTax()</span></span><br>
<span data-ttu-id="53d63-251">PurchTotals_ParmTransEditInvoice.calcTax()</span><span class="sxs-lookup"><span data-stu-id="53d63-251">PurchTotals_ParmTransEditInvoice.calcTax()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-252">元伝票と統合します。</span><span class="sxs-lookup"><span data-stu-id="53d63-252">Integrate with a source document.</span></span></td>
<td><span data-ttu-id="53d63-253">仕入請求書は元伝票トランザクションなので、税が計算されるときに元伝票を作成します。</span><span class="sxs-lookup"><span data-stu-id="53d63-253">Because a purchase invoice is a source document transaction, create a source document when tax is calculated.</span></span></td>
<td><span data-ttu-id="53d63-254">AccDistRuleProductTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="53d63-254">AccDistRuleProductTaxMeasure</span></span><br>
<span data-ttu-id="53d63-255">AccJourRuleVendPaymReqTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="53d63-255">AccJourRuleVendPaymReqTaxMeasure</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="53d63-256">削除 </span><span class="sxs-lookup"><span data-stu-id="53d63-256">Deletion</span></span></td>
<td><span data-ttu-id="53d63-257">トランザクションを削除します。</span><span class="sxs-lookup"><span data-stu-id="53d63-257">Delete a transaction.</span></span></td>
<td><span data-ttu-id="53d63-258">トランザクションが削除される場合、税務書類を削除します。</span><span class="sxs-lookup"><span data-stu-id="53d63-258">Delete the tax document when a transaction is deleted.</span></span></td>
<td><span data-ttu-id="53d63-259">VendInvoiceInfoTable.delete()</span><span class="sxs-lookup"><span data-stu-id="53d63-259">VendInvoiceInfoTable.delete()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-260">トランザクション明細行を削除します。</span><span class="sxs-lookup"><span data-stu-id="53d63-260">Delete a transaction line.</span></span></td>
<td><span data-ttu-id="53d63-261">トランザクション明細行が削除される場合に、税を再計算します。</span><span class="sxs-lookup"><span data-stu-id="53d63-261">Recalculate tax when a transaction line is deleted.</span></span></td>
<td><span data-ttu-id="53d63-262">VendInvoiceInfoLine.delete()</span><span class="sxs-lookup"><span data-stu-id="53d63-262">VendInvoiceInfoLine.delete()</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="53d63-263">更新</span><span class="sxs-lookup"><span data-stu-id="53d63-263">Update</span></span></td>
<td><span data-ttu-id="53d63-264">トランザクション ヘッダー情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="53d63-264">Update transaction header information.</span></span></td>
<td><span data-ttu-id="53d63-265">トランザクション ヘッダー レベルで税に影響するフィールドが更新されると、税を再計算します。</span><span class="sxs-lookup"><span data-stu-id="53d63-265">Recalculate tax when fields that affect tax are updated at the transaction header level.</span></span></td>
<td><span data-ttu-id="53d63-266">VendInvoiceInfoTable.update()</span><span class="sxs-lookup"><span data-stu-id="53d63-266">VendInvoiceInfoTable.update()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-267">トランザクション明細行情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="53d63-267">Update transaction line information.</span></span></td>
<td><span data-ttu-id="53d63-268">トランザクション明細行で税に影響するフィールドが更新されると、税を再計算します。</span><span class="sxs-lookup"><span data-stu-id="53d63-268">Recalculate tax when fields that affect tax are updated on a transaction line.</span></span></td>
<td><span data-ttu-id="53d63-269">VendInvoiceInfoLine.update()</span><span class="sxs-lookup"><span data-stu-id="53d63-269">VendInvoiceInfoLine.update()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-270">税情報を更新します。</span><span class="sxs-lookup"><span data-stu-id="53d63-270">Update tax information.</span></span></td>
<td><span data-ttu-id="53d63-271">税情報のフィールドが更新されると、税を再計算します。</span><span class="sxs-lookup"><span data-stu-id="53d63-271">Recalculate tax when tax information fields are updated.</span></span></td>
<td><span data-ttu-id="53d63-272">TransTaxinformation.Write() (ページのデータ ソース)</span><span class="sxs-lookup"><span data-stu-id="53d63-272">TransTaxinformation.Write() (page data source)</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="53d63-273">転記</span><span class="sxs-lookup"><span data-stu-id="53d63-273">Posting</span></span></td>
<td><span data-ttu-id="53d63-274">税務書類の移行ルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="53d63-274">Define a tax document transition rule.</span></span></td>
<td><span data-ttu-id="53d63-275">あるトランザクションから別のトランザクションへの税務書類の転送に関するルールを定義します。</span><span class="sxs-lookup"><span data-stu-id="53d63-275">Define a rule for the transfer of a tax document from one transaction to another transaction.</span></span></td>
<td><span data-ttu-id="53d63-276">TaxDocumentTransitRuleEventHandler.initTransitDocumentTransactionRuleList()</span><span class="sxs-lookup"><span data-stu-id="53d63-276">TaxDocumentTransitRuleEventHandler.initTransitDocumentTransactionRuleList()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-277">税務書類を転送します。</span><span class="sxs-lookup"><span data-stu-id="53d63-277">Transfer a tax document.</span></span></td>
<td><span data-ttu-id="53d63-278">転記中にあるトランザクションから別のトランザクションに税務書類を転送します。</span><span class="sxs-lookup"><span data-stu-id="53d63-278">Transfer the tax document from one transaction to another transaction during posting.</span></span></td>
<td><span data-ttu-id="53d63-279">PurchaseInvoiceJournalCreate.endCreate()</span><span class="sxs-lookup"><span data-stu-id="53d63-279">PurchaseInvoiceJournalCreate.endCreate()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-280">税金を転記します。</span><span class="sxs-lookup"><span data-stu-id="53d63-280">Post tax.</span></span></td>
<td><span data-ttu-id="53d63-281">トランザクションの転記時に、税を転記します。</span><span class="sxs-lookup"><span data-stu-id="53d63-281">Post tax during transaction posting.</span></span></td>
<td><span data-ttu-id="53d63-282">PurchaseInvoiceJournalPost.PostTax()</span><span class="sxs-lookup"><span data-stu-id="53d63-282">PurchaseInvoiceJournalPost.PostTax()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-283">在庫税を追加します。</span><span class="sxs-lookup"><span data-stu-id="53d63-283">Add inventory tax.</span></span></td>
<td><span data-ttu-id="53d63-284">在庫に対する課税が可能な場合は、在庫に税を追加します。</span><span class="sxs-lookup"><span data-stu-id="53d63-284">Add tax to inventory if a tax load on inventory is available.</span></span></td>
<td><span data-ttu-id="53d63-285">PurchaseInvoiceJournalPost.PostInventory()</span><span class="sxs-lookup"><span data-stu-id="53d63-285">PurchaseInvoiceJournalPost.PostInventory()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-286">税務書類を転記します。</span><span class="sxs-lookup"><span data-stu-id="53d63-286">Post a tax document.</span></span></td>
<td><span data-ttu-id="53d63-287">トランザクションの伝票が転記された後に、税務書類を転記します。</span><span class="sxs-lookup"><span data-stu-id="53d63-287">Post the tax document after the transaction voucher is posted.</span></span> <span data-ttu-id="53d63-288">結果として、税務書類のステータスが、<strong>転記済</strong>に更新され、レコードが関連テーブルに生成されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-288">As a result, the tax document status is updated to <strong>Posted</strong>, and records are generated in relation tables.</span></span></td>
<td><span data-ttu-id="53d63-289">PurchaseInvoiceJournalPost.endUpdate()</span><span class="sxs-lookup"><span data-stu-id="53d63-289">PurchaseInvoiceJournalPost.endUpdate()</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="53d63-290">照会</span><span class="sxs-lookup"><span data-stu-id="53d63-290">Inquiry</span></span></td>
<td><span data-ttu-id="53d63-291">仕訳帳に<strong>税務書類</strong>ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="53d63-291">Add the <strong>Tax document</strong> button on a journal.</span></span></td>
<td><span data-ttu-id="53d63-292">照会用に、ジャーナル ページに<strong>税務書類</strong>ボタンを追加します。</span><span class="sxs-lookup"><span data-stu-id="53d63-292">Add the <strong>Tax document</strong> button to the journal page for inquiry purposes.</span></span></td>
<td><span data-ttu-id="53d63-293">VendInvoiceJournal</span><span class="sxs-lookup"><span data-stu-id="53d63-293">VendInvoiceJournal</span></span></td>
</tr>
</table>

### <a name="define-a-taxable-document"></a><span data-ttu-id="53d63-294">課税対象文書の定義</span><span class="sxs-lookup"><span data-stu-id="53d63-294">Define a taxable document</span></span>

<span data-ttu-id="53d63-295">**TaxableDocumentTypeDefintionPurchaseInvoice** および **TaxableDocumentDescriptorPurchaseInvoice** は、税エンジンの課税対象文書として仕入請求書を定義するクラスです。</span><span class="sxs-lookup"><span data-stu-id="53d63-295">**TaxableDocumentTypeDefintionPurchaseInvoice** and **TaxableDocumentDescriptorPurchaseInvoice** are the classes that define a purchase invoice as a taxable document for the Tax engine.</span></span>

![課税対象文書クラス](media/gte-classes-taxable-document.png)

<span data-ttu-id="53d63-297">TaxableDocumentTypeDefinitionPurchaseInvoice は、課税対象文書として仕入請求書を定義するインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="53d63-297">TaxableDocumentTypeDefinitionPurchaseInvoice is the interface that defines a purchase invoice as a taxable document.</span></span>

![仕入請求書の課税対象文書](media/gte-purch-invoice-taxable-doc.png)

<span data-ttu-id="53d63-299">**TaxableDocumentDescriptorPurchaseInvoice.getDataProvider()** は、仕入請求書に使用されるデータ プロバイダー クラスを指定します。</span><span class="sxs-lookup"><span data-stu-id="53d63-299">**TaxableDocumentDescriptorPurchaseInvoice.getDataProvider()** specifies the data provider class that is used for a purchase invoice.</span></span>

![仕入請求書のデータ プロバイダー](media/gte-data-provider-class-purch.png)

### <a name="define-data-providers"></a><span data-ttu-id="53d63-301">データ プロバイダーの定義</span><span class="sxs-lookup"><span data-stu-id="53d63-301">Define data providers</span></span>

<span data-ttu-id="53d63-302">次の図は、税関連の操作でトランザクション データを税エンジンに送信するために使用されるデータ プロバイダーを示しています。</span><span class="sxs-lookup"><span data-stu-id="53d63-302">The following illustration shows the data providers that are used to send transaction data to the Tax engine for any tax-related operation.</span></span>

![GTE のデータ プロバイダー](media/gte-data-providers.png)

<span data-ttu-id="53d63-304">**TaxableDocPurchaseInvoiceDataProvider.buildQuery()** は、VendInvoiceInfoTable や VendInvoiceInfoLine など、すべての関連トランザクションに対するクエリを提供します。</span><span class="sxs-lookup"><span data-stu-id="53d63-304">**TaxableDocPurchaseInvoiceDataProvider.buildQuery()** provides a query for all related transactions, such as VendInvoiceInfoTable and VendInvoiceInfoLine.</span></span> <span data-ttu-id="53d63-305">また、行のデータ プロバイダーで各データ ソースを登録します。</span><span class="sxs-lookup"><span data-stu-id="53d63-305">It also registers each data source with a row data provider.</span></span> <span data-ttu-id="53d63-306">たとえば、VendInvoiceInfoTable データ ソースは、TableDocVendInvoiceInfoTableRowDP で登録されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-306">For example, the VendInvoiceInfoTable data source is registered with TableDocVendInvoiceInfoTableRowDP.</span></span>

![VendInvoiceInfoTable データ ソース](media/gte-example-vend-invoice.png)

<span data-ttu-id="53d63-308">TaxableDocVendInvoiceInfoTableRowDP は **TaxableDocPurchTableRowDataProvider** クラスを拡張してトランザクション ヘッダー関連情報を設定し、TaxableDocVendInvoiceInfoLineRowDP は **TaxableDocPurchLineRowDataProvider** を拡張して請求明細行関連の情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="53d63-308">TaxableDocVendInvoiceInfoTableRowDP extends the **TaxableDocPurchTableRowDataProvider** class to set up transaction header–related information, whereas TaxableDocVendInvoiceInfoLineRowDP extends **TaxableDocPurchLineRowDataProvider** to set up invoice line–related information.</span></span>

<span data-ttu-id="53d63-309">次の表に、Finance にマップされている課税対象文書フィールドの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="53d63-309">The following table lists the taxable document fields that are mapped in Finance.</span></span>

| <span data-ttu-id="53d63-310">課税対象文書フィールド</span><span class="sxs-lookup"><span data-stu-id="53d63-310">Taxable document field</span></span>         | <span data-ttu-id="53d63-311">AOT オブジェクトのロジック</span><span class="sxs-lookup"><span data-stu-id="53d63-311">Logic in the AOT object</span></span>                                                     | <span data-ttu-id="53d63-312">必須</span><span class="sxs-lookup"><span data-stu-id="53d63-312">Required</span></span>                     | <span data-ttu-id="53d63-313">既定値</span><span class="sxs-lookup"><span data-stu-id="53d63-313">Default value</span></span> |
|--------------------------------|-----------------------------------------------------------------------------|------------------------------|---------------|
| <span data-ttu-id="53d63-314">SubLines</span><span class="sxs-lookup"><span data-stu-id="53d63-314">SubLines</span></span>                       | <span data-ttu-id="53d63-315">TaxableDocumentLineObject.getSubLines</span><span class="sxs-lookup"><span data-stu-id="53d63-315">TaxableDocumentLineObject.getSubLines</span></span>                                       | <span data-ttu-id="53d63-316">有</span><span class="sxs-lookup"><span data-stu-id="53d63-316">Yes</span></span>                          | |
| <span data-ttu-id="53d63-317">フィールド</span><span class="sxs-lookup"><span data-stu-id="53d63-317">Fields</span></span>                         | <span data-ttu-id="53d63-318">TaxableDocumentLineObject.getFields</span><span class="sxs-lookup"><span data-stu-id="53d63-318">TaxableDocumentLineObject.getFields</span></span>                                         | <span data-ttu-id="53d63-319">有</span><span class="sxs-lookup"><span data-stu-id="53d63-319">Yes</span></span>                          | |
| <span data-ttu-id="53d63-320">ModelFieldName</span><span class="sxs-lookup"><span data-stu-id="53d63-320">ModelFieldName</span></span>                 | <span data-ttu-id="53d63-321">TaxableDocumentLineObject.parmModelFieldName</span><span class="sxs-lookup"><span data-stu-id="53d63-321">TaxableDocumentLineObject.parmModelFieldName</span></span>                                | <span data-ttu-id="53d63-322">有</span><span class="sxs-lookup"><span data-stu-id="53d63-322">Yes</span></span>                          | |
| <span data-ttu-id="53d63-323">TaxAdjustment</span><span class="sxs-lookup"><span data-stu-id="53d63-323">TaxAdjustment</span></span>                  | <span data-ttu-id="53d63-324">TaxEngineIntegrationAXContractEventHandler.getLineAdjustment</span><span class="sxs-lookup"><span data-stu-id="53d63-324">TaxEngineIntegrationAXContractEventHandler.getLineAdjustment</span></span>                | <span data-ttu-id="53d63-325">無</span><span class="sxs-lookup"><span data-stu-id="53d63-325">No</span></span>                           | |
| <span data-ttu-id="53d63-326">TableId</span><span class="sxs-lookup"><span data-stu-id="53d63-326">TableId</span></span>                        | <span data-ttu-id="53d63-327">TaxableDocumentLineObject.getTransactionLineTableId</span><span class="sxs-lookup"><span data-stu-id="53d63-327">TaxableDocumentLineObject.getTransactionLineTableId</span></span>                         | <span data-ttu-id="53d63-328">有</span><span class="sxs-lookup"><span data-stu-id="53d63-328">Yes</span></span>                          | |
| <span data-ttu-id="53d63-329"> Recid</span><span class="sxs-lookup"><span data-stu-id="53d63-329">RecId</span></span>                          | <span data-ttu-id="53d63-330">TaxableDocumentLineObject.getTransactionLineRecordId</span><span class="sxs-lookup"><span data-stu-id="53d63-330">TaxableDocumentLineObject.getTransactionLineRecordId</span></span>                        | <span data-ttu-id="53d63-331">有</span><span class="sxs-lookup"><span data-stu-id="53d63-331">Yes</span></span>                          | |
| <span data-ttu-id="53d63-332">課税対象文書タイプ</span><span class="sxs-lookup"><span data-stu-id="53d63-332">Taxable Document Type</span></span>          | <span data-ttu-id="53d63-333">TaxableDocumentDescriptor.createRow</span><span class="sxs-lookup"><span data-stu-id="53d63-333">TaxableDocumentDescriptor.createRow</span></span>                                         | <span data-ttu-id="53d63-334">有</span><span class="sxs-lookup"><span data-stu-id="53d63-334">Yes</span></span>                          | |
| <span data-ttu-id="53d63-335">スキップ済 (ドキュメント レベル)</span><span class="sxs-lookup"><span data-stu-id="53d63-335">Skipped (Document level)</span></span>       | <span data-ttu-id="53d63-336">TaxableDocumentDescriptor.createRow</span><span class="sxs-lookup"><span data-stu-id="53d63-336">TaxableDocumentDescriptor.createRow</span></span>                                         | <span data-ttu-id="53d63-337">有</span><span class="sxs-lookup"><span data-stu-id="53d63-337">Yes</span></span>                          | <span data-ttu-id="53d63-338">無</span><span class="sxs-lookup"><span data-stu-id="53d63-338">No</span></span> |
| <span data-ttu-id="53d63-339">DistributionSide</span><span class="sxs-lookup"><span data-stu-id="53d63-339">DistributionSide</span></span>               | <span data-ttu-id="53d63-340">TaxableDocumentObject.getDistributionSide</span><span class="sxs-lookup"><span data-stu-id="53d63-340">TaxableDocumentObject.getDistributionSide</span></span>                                   | <span data-ttu-id="53d63-341">有</span><span class="sxs-lookup"><span data-stu-id="53d63-341">Yes</span></span>                          | <span data-ttu-id="53d63-342">自動</span><span class="sxs-lookup"><span data-stu-id="53d63-342">Auto</span></span> |
| <span data-ttu-id="53d63-343">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="53d63-343">ExchangeRates</span></span>                  | <span data-ttu-id="53d63-344">TaxEngineIntegrationAXContractEventHandler.getExchangeRate</span><span class="sxs-lookup"><span data-stu-id="53d63-344">TaxEngineIntegrationAXContractEventHandler.getExchangeRate</span></span>                  | <span data-ttu-id="53d63-345">有</span><span class="sxs-lookup"><span data-stu-id="53d63-345">Yes</span></span>                          | |
| <span data-ttu-id="53d63-346">ReportingCurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="53d63-346">ReportingCurrencyExchangeRates</span></span> | <span data-ttu-id="53d63-347">TaxEngineIntegrationAXContractEventHandler.getReportingCurrencyExchangeRate</span><span class="sxs-lookup"><span data-stu-id="53d63-347">TaxEngineIntegrationAXContractEventHandler.getReportingCurrencyExchangeRate</span></span> | <span data-ttu-id="53d63-348">有</span><span class="sxs-lookup"><span data-stu-id="53d63-348">Yes</span></span>                          | |
| <span data-ttu-id="53d63-349">税務書類の目的</span><span class="sxs-lookup"><span data-stu-id="53d63-349">Tax Document Purpose</span></span>           | <span data-ttu-id="53d63-350">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-350">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-351">有</span><span class="sxs-lookup"><span data-stu-id="53d63-351">Yes</span></span>                          | <span data-ttu-id="53d63-352">取引</span><span class="sxs-lookup"><span data-stu-id="53d63-352">Transaction</span></span> |
| <span data-ttu-id="53d63-353">トランザクション通貨</span><span class="sxs-lookup"><span data-stu-id="53d63-353">Transaction Currency</span></span>           | <span data-ttu-id="53d63-354">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-354">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-355">有</span><span class="sxs-lookup"><span data-stu-id="53d63-355">Yes</span></span>                          | |
| <span data-ttu-id="53d63-356">トランザクション日付</span><span class="sxs-lookup"><span data-stu-id="53d63-356">Transaction Date</span></span>               | <span data-ttu-id="53d63-357">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-357">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-358">有</span><span class="sxs-lookup"><span data-stu-id="53d63-358">Yes</span></span>                          | |
| <span data-ttu-id="53d63-359">スキップ済 (明細行レベル)</span><span class="sxs-lookup"><span data-stu-id="53d63-359">Skipped (Line level)</span></span>           | <span data-ttu-id="53d63-360">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-360">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-361">有</span><span class="sxs-lookup"><span data-stu-id="53d63-361">Yes</span></span>                          | <span data-ttu-id="53d63-362">無</span><span class="sxs-lookup"><span data-stu-id="53d63-362">No</span></span> |
| <span data-ttu-id="53d63-363">税提示方法</span><span class="sxs-lookup"><span data-stu-id="53d63-363">Tax Direction</span></span>                  | <span data-ttu-id="53d63-364">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-364">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-365">有</span><span class="sxs-lookup"><span data-stu-id="53d63-365">Yes</span></span>                          | <span data-ttu-id="53d63-366">消費税収入</span><span class="sxs-lookup"><span data-stu-id="53d63-366">Sales tax receivable</span></span> |
| <span data-ttu-id="53d63-367">元帳への転記</span><span class="sxs-lookup"><span data-stu-id="53d63-367">Post To Ledger</span></span>                 | <span data-ttu-id="53d63-368">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-368">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-369">有</span><span class="sxs-lookup"><span data-stu-id="53d63-369">Yes</span></span>                          | <span data-ttu-id="53d63-370">有</span><span class="sxs-lookup"><span data-stu-id="53d63-370">Yes</span></span> |
| <span data-ttu-id="53d63-371">会計の有効化</span><span class="sxs-lookup"><span data-stu-id="53d63-371">Enable Accounting</span></span>              | <span data-ttu-id="53d63-372">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-372">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-373">有</span><span class="sxs-lookup"><span data-stu-id="53d63-373">Yes</span></span>                          | <span data-ttu-id="53d63-374">有</span><span class="sxs-lookup"><span data-stu-id="53d63-374">Yes</span></span> |
| <span data-ttu-id="53d63-375">行タイプ</span><span class="sxs-lookup"><span data-stu-id="53d63-375">Line Type</span></span>                      | <span data-ttu-id="53d63-376">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span><span class="sxs-lookup"><span data-stu-id="53d63-376">TaxableDocumentRowDataProviderLine.fillInFrameworkFields</span></span>                    | <span data-ttu-id="53d63-377">有</span><span class="sxs-lookup"><span data-stu-id="53d63-377">Yes</span></span>                          | <span data-ttu-id="53d63-378">ライン</span><span class="sxs-lookup"><span data-stu-id="53d63-378">Line</span></span> |
| <span data-ttu-id="53d63-379">インポート注文</span><span class="sxs-lookup"><span data-stu-id="53d63-379">Import Order</span></span>                   | <span data-ttu-id="53d63-380">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-380">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-381">有</span><span class="sxs-lookup"><span data-stu-id="53d63-381">Yes</span></span>                          | <span data-ttu-id="53d63-382">無</span><span class="sxs-lookup"><span data-stu-id="53d63-382">No</span></span> |
| <span data-ttu-id="53d63-383">エクスポート注文</span><span class="sxs-lookup"><span data-stu-id="53d63-383">Export Order</span></span>                   | <span data-ttu-id="53d63-384">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-384">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-385">有</span><span class="sxs-lookup"><span data-stu-id="53d63-385">Yes</span></span>                          | <span data-ttu-id="53d63-386">無</span><span class="sxs-lookup"><span data-stu-id="53d63-386">No</span></span> |
| <span data-ttu-id="53d63-387">GST 構成スキーム</span><span class="sxs-lookup"><span data-stu-id="53d63-387">GST Composition Scheme</span></span>         | <span data-ttu-id="53d63-388">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-388">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-389">有</span><span class="sxs-lookup"><span data-stu-id="53d63-389">Yes</span></span>                          | <span data-ttu-id="53d63-390">無</span><span class="sxs-lookup"><span data-stu-id="53d63-390">No</span></span> |
| <span data-ttu-id="53d63-391">構成スキーム</span><span class="sxs-lookup"><span data-stu-id="53d63-391">Composition Scheme</span></span>             | <span data-ttu-id="53d63-392">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-392">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-393">無</span><span class="sxs-lookup"><span data-stu-id="53d63-393">No</span></span>                           | <span data-ttu-id="53d63-394">無</span><span class="sxs-lookup"><span data-stu-id="53d63-394">No</span></span> |
| <span data-ttu-id="53d63-395">顧客タイプ</span><span class="sxs-lookup"><span data-stu-id="53d63-395">Customer Type</span></span>                  | <span data-ttu-id="53d63-396">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-396">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-397">有</span><span class="sxs-lookup"><span data-stu-id="53d63-397">Yes</span></span>                          | <span data-ttu-id="53d63-398">なし</span><span class="sxs-lookup"><span data-stu-id="53d63-398">None</span></span> |
| <span data-ttu-id="53d63-399">仮評価</span><span class="sxs-lookup"><span data-stu-id="53d63-399">Provisional Assessment</span></span>         | <span data-ttu-id="53d63-400">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-400">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-401">無</span><span class="sxs-lookup"><span data-stu-id="53d63-401">No</span></span>                           | <span data-ttu-id="53d63-402">無</span><span class="sxs-lookup"><span data-stu-id="53d63-402">No</span></span> |
| <span data-ttu-id="53d63-403">外部関係者</span><span class="sxs-lookup"><span data-stu-id="53d63-403">Foreign party</span></span>                  | <span data-ttu-id="53d63-404">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-404">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-405">無</span><span class="sxs-lookup"><span data-stu-id="53d63-405">No</span></span>                           | <span data-ttu-id="53d63-406">無</span><span class="sxs-lookup"><span data-stu-id="53d63-406">No</span></span> |
| <span data-ttu-id="53d63-407">評価の種類</span><span class="sxs-lookup"><span data-stu-id="53d63-407">Nature of Assesse</span></span>              | <span data-ttu-id="53d63-408">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-408">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-409">無</span><span class="sxs-lookup"><span data-stu-id="53d63-409">No</span></span>                           | <span data-ttu-id="53d63-410">法人</span><span class="sxs-lookup"><span data-stu-id="53d63-410">Company</span></span> |
| <span data-ttu-id="53d63-411">優先的関係者</span><span class="sxs-lookup"><span data-stu-id="53d63-411">Preferrential Party</span></span>            | <span data-ttu-id="53d63-412">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-412">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-413">無</span><span class="sxs-lookup"><span data-stu-id="53d63-413">No</span></span>                           | <span data-ttu-id="53d63-414">無</span><span class="sxs-lookup"><span data-stu-id="53d63-414">No</span></span> |
| <span data-ttu-id="53d63-415">GTA 商業仕入先</span><span class="sxs-lookup"><span data-stu-id="53d63-415">GTA-Commercial vendor</span></span>          | <span data-ttu-id="53d63-416">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-416">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-417">無</span><span class="sxs-lookup"><span data-stu-id="53d63-417">No</span></span>                           | <span data-ttu-id="53d63-418">無</span><span class="sxs-lookup"><span data-stu-id="53d63-418">No</span></span> |
| <span data-ttu-id="53d63-419">元帳通貨</span><span class="sxs-lookup"><span data-stu-id="53d63-419">Ledger Currency</span></span>                | <span data-ttu-id="53d63-420">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-420">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-421">有</span><span class="sxs-lookup"><span data-stu-id="53d63-421">Yes</span></span>                          | |
| <span data-ttu-id="53d63-422">合計割引率</span><span class="sxs-lookup"><span data-stu-id="53d63-422">Total Discount Percentage</span></span>      | <span data-ttu-id="53d63-423">TaxableDocumentRowDataProviderHeader.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-423">TaxableDocumentRowDataProviderHeader.fillInFields</span></span>                           | <span data-ttu-id="53d63-424">無</span><span class="sxs-lookup"><span data-stu-id="53d63-424">No</span></span>                           | |
| <span data-ttu-id="53d63-425">免税</span><span class="sxs-lookup"><span data-stu-id="53d63-425">Exempt</span></span>                         | <span data-ttu-id="53d63-426">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-426">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-427">有</span><span class="sxs-lookup"><span data-stu-id="53d63-427">Yes</span></span>                          | <span data-ttu-id="53d63-428">無</span><span class="sxs-lookup"><span data-stu-id="53d63-428">No</span></span> |
| <span data-ttu-id="53d63-429">目的</span><span class="sxs-lookup"><span data-stu-id="53d63-429">Purpose</span></span>                        | <span data-ttu-id="53d63-430">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-430">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-431">有</span><span class="sxs-lookup"><span data-stu-id="53d63-431">Yes</span></span>                          | <span data-ttu-id="53d63-432">取引</span><span class="sxs-lookup"><span data-stu-id="53d63-432">Transaction</span></span> |
| <span data-ttu-id="53d63-433">税込価格</span><span class="sxs-lookup"><span data-stu-id="53d63-433">Prices include sales tax</span></span>       | <span data-ttu-id="53d63-434">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-434">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-435">有</span><span class="sxs-lookup"><span data-stu-id="53d63-435">Yes</span></span>                          | <span data-ttu-id="53d63-436">無</span><span class="sxs-lookup"><span data-stu-id="53d63-436">No</span></span> |
| <span data-ttu-id="53d63-437">配送日</span><span class="sxs-lookup"><span data-stu-id="53d63-437">Delivery Date</span></span>                  | <span data-ttu-id="53d63-438">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-438">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-439">無</span><span class="sxs-lookup"><span data-stu-id="53d63-439">No</span></span>                           | |
| <span data-ttu-id="53d63-440">DiscountAmount</span><span class="sxs-lookup"><span data-stu-id="53d63-440">DiscountAmount</span></span>                 | <span data-ttu-id="53d63-441">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-441">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-442">無</span><span class="sxs-lookup"><span data-stu-id="53d63-442">No</span></span>                           | |
| <span data-ttu-id="53d63-443">正味金額</span><span class="sxs-lookup"><span data-stu-id="53d63-443">Net Amount</span></span>                     | <span data-ttu-id="53d63-444">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-444">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-445">無</span><span class="sxs-lookup"><span data-stu-id="53d63-445">No</span></span>                           | |
| <span data-ttu-id="53d63-446">件数</span><span class="sxs-lookup"><span data-stu-id="53d63-446">Quantity</span></span>                       | <span data-ttu-id="53d63-447">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-447">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-448">無</span><span class="sxs-lookup"><span data-stu-id="53d63-448">No</span></span>                           | |
| <span data-ttu-id="53d63-449">消費状態</span><span class="sxs-lookup"><span data-stu-id="53d63-449">Consumption State</span></span>              | <span data-ttu-id="53d63-450">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-450">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-451">無</span><span class="sxs-lookup"><span data-stu-id="53d63-451">No</span></span>                           | |
| <span data-ttu-id="53d63-452">返金</span><span class="sxs-lookup"><span data-stu-id="53d63-452">Return</span></span>                         | <span data-ttu-id="53d63-453">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-453">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-454">有</span><span class="sxs-lookup"><span data-stu-id="53d63-454">Yes</span></span>                          | <span data-ttu-id="53d63-455">無</span><span class="sxs-lookup"><span data-stu-id="53d63-455">No</span></span> |
| <span data-ttu-id="53d63-456">処分アクション</span><span class="sxs-lookup"><span data-stu-id="53d63-456">Disposition Action</span></span>             | <span data-ttu-id="53d63-457">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-457">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-458">いいえ (返品あり)</span><span class="sxs-lookup"><span data-stu-id="53d63-458">No (Yes for a return)</span></span>        | <span data-ttu-id="53d63-459">クレジット</span><span class="sxs-lookup"><span data-stu-id="53d63-459">Credit</span></span> |
| <span data-ttu-id="53d63-460">課税金額</span><span class="sxs-lookup"><span data-stu-id="53d63-460">Assessable Value</span></span>               | <span data-ttu-id="53d63-461">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-461">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-462">有</span><span class="sxs-lookup"><span data-stu-id="53d63-462">Yes</span></span>                          | |
| <span data-ttu-id="53d63-463">州間</span><span class="sxs-lookup"><span data-stu-id="53d63-463">Inter-State</span></span>                    | <span data-ttu-id="53d63-464">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-464">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-465">有</span><span class="sxs-lookup"><span data-stu-id="53d63-465">Yes</span></span>                          | <span data-ttu-id="53d63-466">無</span><span class="sxs-lookup"><span data-stu-id="53d63-466">No</span></span> |
| <span data-ttu-id="53d63-467">カスタム税率コードのインポート</span><span class="sxs-lookup"><span data-stu-id="53d63-467">Import Custom Tariff Code</span></span>      | <span data-ttu-id="53d63-468">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-468">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-469">いいえ (インポート注文はあり)</span><span class="sxs-lookup"><span data-stu-id="53d63-469">No (Yes for an import order)</span></span> | |
| <span data-ttu-id="53d63-470">カスタム税率コードのエクスポート</span><span class="sxs-lookup"><span data-stu-id="53d63-470">Export Custom Tariff Code</span></span>      | <span data-ttu-id="53d63-471">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-471">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-472">いいえ (エクスポート注文はあり)</span><span class="sxs-lookup"><span data-stu-id="53d63-472">No (Yes for an export order)</span></span> | |
| <span data-ttu-id="53d63-473">IEC 番号</span><span class="sxs-lookup"><span data-stu-id="53d63-473">IEC Number</span></span>                     | <span data-ttu-id="53d63-474">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-474">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-475">無</span><span class="sxs-lookup"><span data-stu-id="53d63-475">No</span></span>                           | |
| <span data-ttu-id="53d63-476">最大小売価格</span><span class="sxs-lookup"><span data-stu-id="53d63-476">Maximum Retail Price</span></span>           | <span data-ttu-id="53d63-477">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-477">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-478">無</span><span class="sxs-lookup"><span data-stu-id="53d63-478">No</span></span>                           | |
| <span data-ttu-id="53d63-479">パーティ GST 登録番号</span><span class="sxs-lookup"><span data-stu-id="53d63-479">Party GST Registration Number</span></span>  | <span data-ttu-id="53d63-480">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-480">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-481">有</span><span class="sxs-lookup"><span data-stu-id="53d63-481">Yes</span></span>                          | |
| <span data-ttu-id="53d63-482">GST 登録番号</span><span class="sxs-lookup"><span data-stu-id="53d63-482">GST Registration Number</span></span>        | <span data-ttu-id="53d63-483">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-483">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-484">有</span><span class="sxs-lookup"><span data-stu-id="53d63-484">Yes</span></span>                          | |
| <span data-ttu-id="53d63-485">HSN コード</span><span class="sxs-lookup"><span data-stu-id="53d63-485">HSN Code</span></span>                       | <span data-ttu-id="53d63-486">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-486">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-487">有</span><span class="sxs-lookup"><span data-stu-id="53d63-487">Yes</span></span>                          | |
| <span data-ttu-id="53d63-488">SAC</span><span class="sxs-lookup"><span data-stu-id="53d63-488">SAC</span></span>                            | <span data-ttu-id="53d63-489">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-489">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-490">有</span><span class="sxs-lookup"><span data-stu-id="53d63-490">Yes</span></span>                          | |
| <span data-ttu-id="53d63-491">サービス カテゴリ</span><span class="sxs-lookup"><span data-stu-id="53d63-491">Service Category</span></span>               | <span data-ttu-id="53d63-492">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-492">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-493">有</span><span class="sxs-lookup"><span data-stu-id="53d63-493">Yes</span></span>                          | <span data-ttu-id="53d63-494">内向き</span><span class="sxs-lookup"><span data-stu-id="53d63-494">Inward</span></span> |
| <span data-ttu-id="53d63-495">ITC カテゴリ</span><span class="sxs-lookup"><span data-stu-id="53d63-495">ITC Category</span></span>                   | <span data-ttu-id="53d63-496">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-496">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-497">有</span><span class="sxs-lookup"><span data-stu-id="53d63-497">Yes</span></span>                          | <span data-ttu-id="53d63-498">入力</span><span class="sxs-lookup"><span data-stu-id="53d63-498">Input</span></span> |
| <span data-ttu-id="53d63-499">仕損</span><span class="sxs-lookup"><span data-stu-id="53d63-499">Is Scrap</span></span>                       | <span data-ttu-id="53d63-500">TaxableDocumentRowDataProviderLine.fillInFields</span><span class="sxs-lookup"><span data-stu-id="53d63-500">TaxableDocumentRowDataProviderLine.fillInFields</span></span>                             | <span data-ttu-id="53d63-501">いいえ (販売注文はあり)</span><span class="sxs-lookup"><span data-stu-id="53d63-501">No (Yes for a sales order)</span></span>   | <span data-ttu-id="53d63-502">無</span><span class="sxs-lookup"><span data-stu-id="53d63-502">No</span></span> |

### <a name="add-the-tax-document-button-on-a-transaction"></a><span data-ttu-id="53d63-503">トランザクションに税務書類ボタンを追加する</span><span class="sxs-lookup"><span data-stu-id="53d63-503">Add the Tax document button on a transaction</span></span>

<span data-ttu-id="53d63-504">税エンジンで税計算をトリガーする 1 つの方法は、トランザクションに追加する**税務書類**ボタンを使用することです。</span><span class="sxs-lookup"><span data-stu-id="53d63-504">One way to trigger tax calculation in the Tax engine is through a **Tax document** button that you add on the transaction.</span></span> <span data-ttu-id="53d63-505">このボタンをクリックすると、トランザクション データが事前定義された課税対象文書オブジェクトとして税エンジンに送信され、税計算が税エンジンでトリガーされます。</span><span class="sxs-lookup"><span data-stu-id="53d63-505">When this button is clicked, transactional data is sent to the Tax engine as a predefined taxable document object, and tax calculation is triggered in the Tax engine.</span></span> <span data-ttu-id="53d63-506">ボタンは通常、**VendEditInvoice** などのトランザクション ページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-506">The button is usually added to a transaction page, such as **VendEditInvoice**.</span></span> <span data-ttu-id="53d63-507">税が計算された直後に、結果が税務書類のユーザー インターフェイス (UI) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-507">Immediately after tax is calculated, the result appears in the tax document user interface (UI).</span></span>

![アクション ペインの税務書類ボタン](media/gte-vend-taxdocument.png)

![taxdocumentlauncher プロパティ](media/gte-vend-taxdocumentlauncher.png)

### <a name="integrate-with-transaction-totals"></a><span data-ttu-id="53d63-510">トランザクションの合計との統合</span><span class="sxs-lookup"><span data-stu-id="53d63-510">Integrate with transaction totals</span></span>

<span data-ttu-id="53d63-511">**合計**ボタンは税金額、割引額、合計額などのトランザクションの財務情報を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-511">The **Totals** button is used to show a transaction's financial information, such as the tax amount, discount amount, and total amounts.</span></span> <span data-ttu-id="53d63-512">合計ページに表示される税額も、仕訳帳の請求金額に追加されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-512">The tax amount that appears on the total page will also be added to the invoiced amount of the journal.</span></span>

<span data-ttu-id="53d63-513">Finance の既存の実装では、この機能を処理するために **PurchTotals** クラスのセットが作成されています。</span><span class="sxs-lookup"><span data-stu-id="53d63-513">For an existing implementation of Finance, a set of **PurchTotals** classes is created to handle this functionality.</span></span> <span data-ttu-id="53d63-514">したがって、税エンジン関連のコードがクラスの **calcTax** メソッドに挿入され、予想される税金の合計金額が確実に開始されるようになります。</span><span class="sxs-lookup"><span data-stu-id="53d63-514">Therefore, Tax engine-related code is inserted into the class's **calcTax** method to help guarantee that the expected tax total amount is initiated.</span></span>

![calcTax メソッド](media/gte-trx-totals.png)

<span data-ttu-id="53d63-516">既存のロジックとの調整のため、既存の **taxTotal** パラメーターを使用して、トランザクション全体の税額を表示します。</span><span class="sxs-lookup"><span data-stu-id="53d63-516">For alignment with the existing logic, the existing **taxTotal** parameter is used to show the tax amount for the whole transaction.</span></span> <span data-ttu-id="53d63-517">**taxTotalGTE** という名前の新しいパラメーターは、仕入先に転記される税を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-517">A new parameter that is named **taxTotalGTE** is used to show the tax that is posted to the vendor.</span></span> <span data-ttu-id="53d63-518">逆請求など、場合によっては、**taxTotal** の値が **taxTotalGTE** の値と一致しません。</span><span class="sxs-lookup"><span data-stu-id="53d63-518">In some cases, such as a reverse charge, the **taxTotal** value doesn't equal the **taxTotalGTE** value.</span></span> <span data-ttu-id="53d63-519">したがって、**taxTotal** が仕訳の転記に使用され、**taxTotalGTE** は**合計**ページで合計税額を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-519">Therefore, **taxTotal** will be used for journal posting, whereas **taxTotalGTE** will be used on **Totals** pages to show the total tax amount.</span></span>

### <a name="integrate-with-a-source-document"></a><span data-ttu-id="53d63-520">元伝票との統合</span><span class="sxs-lookup"><span data-stu-id="53d63-520">Integrate with a source document</span></span>

<span data-ttu-id="53d63-521">仕入請求書は、元伝票のトランザクションです。</span><span class="sxs-lookup"><span data-stu-id="53d63-521">A purchase invoice is a source document transaction.</span></span> <span data-ttu-id="53d63-522">したがって、税エンジンから計算された税の結果は、Finance の既存の元伝票フレームワークと統合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-522">Therefore, the calculated tax result from the Tax engine should be integrated with the existing source document framework in Finance.</span></span> <span data-ttu-id="53d63-523">主要なロジックはすでに完成しており、税エンジン統合フレームワークによって処理されています。</span><span class="sxs-lookup"><span data-stu-id="53d63-523">The main logic is already completed and handled by the Tax engine integration framework.</span></span> <span data-ttu-id="53d63-524">ただし、各元伝票トランザクションについては、配分ルールおよび仕訳ルールを会計目的で定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-524">However, for each source document transaction, the distribution and journalization rules should still be defined for accounting purposes.</span></span>

![配分ルールと仕訳ルール](media/gte-distribution-journalization-rule.png)

<span data-ttu-id="53d63-526">仕入請求書用に **AcctDistRuleProductTaxMeasure** および **AccJourRuleVendPaymReqTaxMeasure** の 2 つのクラスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-526">Two classes are created for a purchase invoice: **AcctDistRuleProductTaxMeasure** and **AccJourRuleVendPaymReqTaxMeasure**.</span></span>

![AcctDistRuleProductTaxMeasure クラス](media/gte-class1.png)

![AccJourRuleVendPaymReqTaxMeasure クラス](media/gte-class2.png)

<span data-ttu-id="53d63-529">元伝票クラスが正しく作成されると、配分ページには、計算された税金とコンポーネント ラベル、税額、および勘定科目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-529">When the source document classes are created correctly, the distribution page should show calculated tax together with the component label, tax amount, and ledger account.</span></span>

![勘定配布](media/gte-accounting-distribution.png)

### <a name="delete-a-transaction"></a><span data-ttu-id="53d63-531">トランザクションの削除</span><span class="sxs-lookup"><span data-stu-id="53d63-531">Delete a transaction</span></span>

<span data-ttu-id="53d63-532">仕入請求書が削除されると、関連する税務書類も削除されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-532">When a purchase invoice is deleted, the associated tax document should also be deleted.</span></span> <span data-ttu-id="53d63-533">関連する税務書類を削除するには、VendInvoiceInfoTable の**削除**メソッドで TaxBusinessService を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="53d63-533">To delete an associated tax document, call TaxBusinessService in the **delete** method of VendInvoiceInfoTable.</span></span>

![トランザクションの削除方法](media/gte-delete-trx.png)

### <a name="delete-a-transaction-line"></a><span data-ttu-id="53d63-535">トランザクション明細行を削除する</span><span class="sxs-lookup"><span data-stu-id="53d63-535">Delete a transaction line</span></span>

<span data-ttu-id="53d63-536">トランザクション明細行が削除されると、税務書類を再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-536">When a transaction line is deleted, the tax document should be recalculated.</span></span> <span data-ttu-id="53d63-537">パフォーマンス上の理由から、トランザクション明細行が削除された直後に GTE が税を再計算することはありません。</span><span class="sxs-lookup"><span data-stu-id="53d63-537">For performance reasons, GTE doesn't recalculate tax immediately after a transaction line is deleted.</span></span> <span data-ttu-id="53d63-538">代わりに、税務書類のステータスを**ダーティー**に更新します。</span><span class="sxs-lookup"><span data-stu-id="53d63-538">Instead, it updates the tax document's status to **Dirty**.</span></span> <span data-ttu-id="53d63-539">表示または転記できるように税務書類が取得されると、GTE は状態が **ダーティー** かどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="53d63-539">When a tax document is retrieved so that it can be viewed or posted, GTE checks whether the status is **Dirty**.</span></span> <span data-ttu-id="53d63-540">ステータスによっては、再計算が行われます。</span><span class="sxs-lookup"><span data-stu-id="53d63-540">Depending on the status, recalculation occurs.</span></span>

![税務書類のステータス](media/gte-tax-doc-status1.png)

![税務書類のステータスの変更](media/gte-tax-doc-status2.png)

### <a name="update-transaction-header-information"></a><span data-ttu-id="53d63-543">トランザクション ヘッダー情報を更新する</span><span class="sxs-lookup"><span data-stu-id="53d63-543">Update transaction header information</span></span>

<span data-ttu-id="53d63-544">一部のトランザクション ヘッダー情報は税の計算に影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="53d63-544">Some transaction header information can affect tax calculation.</span></span> <span data-ttu-id="53d63-545">例には、トランザクションの日付と通貨が含まれます。</span><span class="sxs-lookup"><span data-stu-id="53d63-545">Examples include the transaction date and currency.</span></span> <span data-ttu-id="53d63-546">したがって、この種の情報が別の値に更新された場合は、後で再計算できるよう税務書類を**ダーティー**としてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-546">Therefore, when this type of information is updated to a different value, the tax document should be marked as **Dirty** so that it can be recalculated later.</span></span>

![税務書類のダーティー ステータス](media/gte-trx-header-info.png)

<span data-ttu-id="53d63-548">次の方法は、仕入請求書の税計算に影響を与える可能性のあるフィールドを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="53d63-548">The following method lists fields that might affect tax calculation for a purchase invoice.</span></span>

![税計算に影響を与えるフィールドを一覧表示する方法](media/gte-tax-calc-purchase.png)

### <a name="update-transaction-line-information"></a><span data-ttu-id="53d63-550">トランザクション明細行情報を更新する</span><span class="sxs-lookup"><span data-stu-id="53d63-550">Update transaction line information</span></span>

<span data-ttu-id="53d63-551">同様に、いくつかのトランザクション明細行フィールドの更新も、税計算に影響します。</span><span class="sxs-lookup"><span data-stu-id="53d63-551">Similarly, the update of some transaction line fields also affects tax calculation.</span></span>

![税計算に影響を与えるトランザクション明細行](media/gte-update-trx-line-info.png)

### <a name="update-tax-information"></a><span data-ttu-id="53d63-553">税情報を更新する</span><span class="sxs-lookup"><span data-stu-id="53d63-553">Update tax information</span></span>

<span data-ttu-id="53d63-554">トランザクション明細行の税情報は、税計算に大きな影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="53d63-554">The tax information of a transaction line has a major effect on tax calculation.</span></span> <span data-ttu-id="53d63-555">ロジックはアプリケーション オブジェクト ツリー (AOT) **TransTaxInformation** ページで管理されています。</span><span class="sxs-lookup"><span data-stu-id="53d63-555">The logic is maintained on the Application Object Tree (AOT) **TransTaxInformation** page.</span></span> <span data-ttu-id="53d63-556">このページはそれ以上の取得を必要としない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-556">This page might not require further uptake.</span></span>

### <a name="define-a-tax-document-transit-rule"></a><span data-ttu-id="53d63-557">税務書類の輸送ルールを定義する</span><span class="sxs-lookup"><span data-stu-id="53d63-557">Define a tax document transit rule</span></span>

<span data-ttu-id="53d63-558">仕入請求書および仕訳帳に税務書類を関連付けるには、ルールを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-558">A rule should be defined to associate a purchase invoice and journal with the tax document.</span></span> <span data-ttu-id="53d63-559">**TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleList()** では、VendInvoiceInfoTable、VendInvoiceInfoLine、VendInvoiceJour、VendInvoiceTrans の各ルールを定義して、税務書類または税務書類行をトランザクション テーブルに関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-559">In **TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleList()**, rules are defined for VendInvoiceInfoTable, VendInvoiceInfoLine, VendInvoiceJour, and VendInvoiceTrans to specify that the tax document or tax document row should be associated with the transaction table.</span></span>

![税務書類の輸送ルール](media/gte-tax-doc-transit-rule.png)

<span data-ttu-id="53d63-561">**TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleExtList()** には、トランザクションから仕訳帳への輸送アクションの拡張ルールの定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53d63-561">**TaxDocumentTransitRuleEventHandler::initTransitDocumentRuleExtList()** includes extended rule definitions of a transit action from the transaction to the journal.</span></span>

![税務書類の輸送ルールの拡張](media/gte-tax-doc-transit-rule-ext.png)

### <a name="transfer-a-tax-document"></a><span data-ttu-id="53d63-563">税務書類を転送する</span><span class="sxs-lookup"><span data-stu-id="53d63-563">Transfer a tax document</span></span>

<span data-ttu-id="53d63-564">トランザクションから仕訳帳が作成される場合、税務書類を仕訳帳に転送する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-564">When a journal is created from a transaction, the tax document should be transferred to the journal.</span></span> <span data-ttu-id="53d63-565">次のコードは、税務書類を仕入請求書から仕入請求書の仕訳帳に転送します。</span><span class="sxs-lookup"><span data-stu-id="53d63-565">The following code transfers a tax document from a purchase invoice to a purchase invoice journal.</span></span>

![税務書類を転送する](media/gte-transfer-tax-document.png)

### <a name="post-tax"></a><span data-ttu-id="53d63-567">税を転記する</span><span class="sxs-lookup"><span data-stu-id="53d63-567">Post tax</span></span>

<span data-ttu-id="53d63-568">税の転記は、仕入請求書の仕訳帳が転記されるときに発生します。</span><span class="sxs-lookup"><span data-stu-id="53d63-568">Tax posting occurs when the purchase invoice journal is posted.</span></span> <span data-ttu-id="53d63-569">したがって、**FormLetterJournalPost.postTax()** 基本クラスで **TaxBusinessService::PostTax()** が仕入請求書の仕訳帳を転記するために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-569">Therefore, **TaxBusinessService::PostTax()** is called in the **FormLetterJournalPost.postTax()** base class to post the purchase invoice journal.</span></span>

![税の転記](media/gte-post-tax.png)

### <a name="add-inventory-tax"></a><span data-ttu-id="53d63-571">在庫税を追加する</span><span class="sxs-lookup"><span data-stu-id="53d63-571">Add inventory tax</span></span>

<span data-ttu-id="53d63-572">在庫に転記する必要がある税は、在庫トランザクションに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-572">Tax that must be posted to inventory should be added to an inventory transaction.</span></span>

<span data-ttu-id="53d63-573">次の例は、**taxEngineInventMovement().updateTaxFinancial()** クラス メソッドを使用して、在庫に対する税を転記する**在庫**モジュールのロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="53d63-573">The following example shows logic in the **Inventory** module that posts tax for inventory by using the **taxEngineInventMovement().updateTaxFinancial()** class method.</span></span>

![在庫税を追加する](media/gte-purchinvoicejournalpost.png)

### <a name="post-a-tax-document"></a><span data-ttu-id="53d63-575">税務書類を転記する</span><span class="sxs-lookup"><span data-stu-id="53d63-575">Post a tax document</span></span>

<span data-ttu-id="53d63-576">税が転記されたら、税務書類を転記したことを示すステータスに税務書類を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53d63-576">After tax is posted, the tax document should be updated to a status that indicates that the tax document has been posted.</span></span>

![税務書類を転記する](media/gte-tax-document-status.png)

<span data-ttu-id="53d63-578">上記のメソッドが呼び出されると、GeneralDournalEntry と仕訳帳トランザクションの関係を維持するために、TaxDocumentGeneralJournalEntryLink テーブルに追加のレコードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-578">When the preceding method is called, an additional record is created in the TaxDocumentGeneralJournalEntryLink table to maintain the relationship between GeneralJournalEntry and the journal transaction.</span></span> <span data-ttu-id="53d63-579">このレコードは GTE が GeneralJournalEntry レベルで税務書類を簡単に取得するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="53d63-579">This record will help GTE easily fetch the tax document at the GeneralJournalEntry level.</span></span>

![税務書類の仕訳帳入力](media/gte-taxdocumentgeneraljournalentrylink.png)

## <a name="debugging"></a><span data-ttu-id="53d63-581">デバッグ</span><span class="sxs-lookup"><span data-stu-id="53d63-581">Debugging</span></span>

<span data-ttu-id="53d63-582">税エンジンのデバッグは、主にトランザクション データの検証と計算された税務書類の結果に基づいて行われます。</span><span class="sxs-lookup"><span data-stu-id="53d63-582">Debugging of the Tax engine is done mainly on the validation of transaction data and the calculated tax document result.</span></span> <span data-ttu-id="53d63-583">トランザクションデータと計算結果はどちらも JavaScript Object Notation (JSON) 文字列形式です。</span><span class="sxs-lookup"><span data-stu-id="53d63-583">Both the transaction data and the calculated result are in JavaScript Object Notation (JSON) string format.</span></span>

### <a name="debugging-transaction-data"></a><span data-ttu-id="53d63-584">トランザクション データのデバッグ</span><span class="sxs-lookup"><span data-stu-id="53d63-584">Debugging transaction data</span></span>

<span data-ttu-id="53d63-585">次の図に示すように、**TaxEngineServiceProxy.calculate()** にブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="53d63-585">Put a breakpoint in **TaxEngineServiceProxy.calculate()**, as shown in the following illustration.</span></span>

![トランザクション データのデバッグ](media/gte-debug-transaction-data.png)

<span data-ttu-id="53d63-587">**JsonStr** には、データ プロバイダーによって作成されたすべてのトランザクション データ情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53d63-587">**JsonStr** contains all the transaction data information that is prepared by data providers.</span></span> <span data-ttu-id="53d63-588">オンラインの JSON ビューアーを使用して、税モデルの属性にデータが正しく設定されているかどうかを簡単に識別できます。</span><span class="sxs-lookup"><span data-stu-id="53d63-588">You can use any online JSON viewer to easily identify whether data is correctly set for tax model attributes.</span></span>

### <a name="debugging-the-tax-document"></a><span data-ttu-id="53d63-589">税務書類のデバッグ</span><span class="sxs-lookup"><span data-stu-id="53d63-589">Debugging the tax document</span></span>

<span data-ttu-id="53d63-590">税エンジンが計算に対してエラーを返した場合、すべての結果は上記のメソッドの **RET** 属性に設定されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-590">If the Tax engine returns errors for a calculation, all the results will be set to the **RET** attribute in the preceding method.</span></span> <span data-ttu-id="53d63-591">属性にクイック ウォッチ コマンドを使用すると、税エンジンからの完全なエラーを簡単に理解できます。</span><span class="sxs-lookup"><span data-stu-id="53d63-591">By using a Quick Watch command on the attribute, you can easily understand the full error from the Tax engine.</span></span>

<span data-ttu-id="53d63-592">税エンジンが問題を返さない場合、税務書類の結果は以下の表に保持されます。</span><span class="sxs-lookup"><span data-stu-id="53d63-592">If the Tax engine returns no issues, the tax document result will be persisted into the following tables:</span></span>

- <span data-ttu-id="53d63-593">TaxDocument</span><span class="sxs-lookup"><span data-stu-id="53d63-593">TaxDocument</span></span>
- <span data-ttu-id="53d63-594">TaxDocumentRow</span><span class="sxs-lookup"><span data-stu-id="53d63-594">TaxDocumentRow</span></span>
- <span data-ttu-id="53d63-595">TaxDocumentJson</span><span class="sxs-lookup"><span data-stu-id="53d63-595">TaxDocumentJson</span></span>

<span data-ttu-id="53d63-596">これらのテーブルを照会して JSON 文字列を取得することで、オンラインの JSON ビューアーを介して結果の詳細を簡単に確認できます。</span><span class="sxs-lookup"><span data-stu-id="53d63-596">By querying these tables to obtain the JSON string, you can easily check the result details via any online JSON viewer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53d63-597">追加リソース</span><span class="sxs-lookup"><span data-stu-id="53d63-597">Additional resources</span></span>

- [<span data-ttu-id="53d63-598">税エンジンの概要</span><span class="sxs-lookup"><span data-stu-id="53d63-598">Tax engine overview</span></span>](tax-engine.md)
- [<span data-ttu-id="53d63-599">税エンジンの拡張</span><span class="sxs-lookup"><span data-stu-id="53d63-599">Extending the Tax engine</span></span>](extend-tax-engine-configurations.md)
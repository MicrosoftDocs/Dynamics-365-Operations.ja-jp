---
title: ER 電子メール送信先のタイプ
description: このトピックでは、送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、電子メール送信先をコンフィギュレーションする方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019866"
---
# <span data-ttu-id="e4002-103"><a name="EmailDestinationType">電子メールの送信先</a></span><span class="sxs-lookup"><span data-stu-id="e4002-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4002-104">送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、電子メール送信先をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e4002-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="e4002-105">送信先の設定に基づいて、生成されたドキュメントは電子メールの添付ファイルとして配信されます。</span><span class="sxs-lookup"><span data-stu-id="e4002-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="e4002-106">**有効** を **はい** に設定し、出力ファイルを電子メールで送信します。</span><span class="sxs-lookup"><span data-stu-id="e4002-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="e4002-107">このオプションを有効にすると、電子メールの受信者を指定して、電子メールの件名および本文を編集できます。</span><span class="sxs-lookup"><span data-stu-id="e4002-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="e4002-108">電子メールの件名および本文の定型文を設定したり、ER [フォーミュラ](er-formula-language.md) を使用して電子メールのテキストを動的に作成したりできます。</span><span class="sxs-lookup"><span data-stu-id="e4002-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="e4002-109">2 つの方法で ER の電子メール アドレスを構成できます。</span><span class="sxs-lookup"><span data-stu-id="e4002-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="e4002-110">コンフィギュレーションは、印刷管理機能で完了したのと同じ方法で完了することができ、またフォーミュラを介した ER コンフィギュレーションへの直接参照を使用して電子メールアドレスを解決することもできます。</span><span class="sxs-lookup"><span data-stu-id="e4002-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="e4002-111">[![電子メール送信先の有効化](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="e4002-112">電子メール アドレス タイプ</span><span class="sxs-lookup"><span data-stu-id="e4002-112">Email address types</span></span>

<span data-ttu-id="e4002-113">**To** や **Cc** フィールドで**編集**を選択すると、**電子メールの送信先**ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e4002-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="e4002-114">使用する電子メール アドレス タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e4002-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="e4002-115">現在、**コンフィギュレーション電子メール**および**印刷管理**電子メールのタイプがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e4002-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="e4002-116">[![電子メールのタイプの選択](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="e4002-117">印刷管理</span><span class="sxs-lookup"><span data-stu-id="e4002-117">Print management</span></span>

<span data-ttu-id="e4002-118">**印刷管理電子メール** タイプを選択する場合、**To** フィールドに固定の電子メール アドレスを入力できます。</span><span class="sxs-lookup"><span data-stu-id="e4002-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="e4002-119">[![固定電子メール アドレスの構成](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="e4002-120">固定されていない電子メール アドレスを使用するには、ファイルの送信先の電子メール ソース タイプを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4002-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="e4002-121">**顧客**、**仕入先**、**見込顧客**、**連絡先**、**競合他社**、**作業者**、**申請者**、**見込み仕入先**、**不許可仕入先**の値がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e4002-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="e4002-122">電子メール ソース タイプを選択したら、**電子メール ソース** フィールドの横のボタンを使用して、**フォーミュラ デザイナー** フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4002-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="e4002-123">このフォームを使用して、実行時に処理されたドキュメントから選択されたソース タイプ フォームの**関係者のアカウント**を返すフォーミュラを電子メールの送信先に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="e4002-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="e4002-124">[![電子メールのソース アカウントのコンフィギュレーション](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="e4002-125">フォーミュラは ER コンフィギュレーションに固有です。</span><span class="sxs-lookup"><span data-stu-id="e4002-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="e4002-126">**フォーミュラ** フィールドで、顧客または仕入先の関係者タイプにドキュメント固有の参照を入力します。</span><span class="sxs-lookup"><span data-stu-id="e4002-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="e4002-127">入力せずに、顧客または仕入先を表すデータ ソース ノードを検索でき、フォーミュラを更新するには**データ ソースの追加**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="e4002-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="e4002-128">たとえば、**ISO 20022 の口座振替**のコンフィギュレーションを使用する場合、仕入先を表すノードは、`'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID` です。</span><span class="sxs-lookup"><span data-stu-id="e4002-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="e4002-129">`"DE-001"` などの文字列値を入力し、フォーミュラを保存した場合、仕入先 **DE-001** の連絡担当者に電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="e4002-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="e4002-130">[![ER フォーミュラ デザイナー ページ](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="e4002-131">[![電子メールのソース アカウントのコンフィギュレーション](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="e4002-132">コンフィギュレーション電子メール</span><span class="sxs-lookup"><span data-stu-id="e4002-132">Configuration email</span></span>

<span data-ttu-id="e4002-133">使用するコンフィギュレーションが**電子メール アドレス**を返すデータ ソースにノードを持つ場合にこの電子メール タイプを使用します。</span><span class="sxs-lookup"><span data-stu-id="e4002-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="e4002-134">フォーミュラ デザイナーでデータ ソースと機能を使用して、正しく書式設定された電子メール アドレスを取得できます。</span><span class="sxs-lookup"><span data-stu-id="e4002-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="e4002-135">たとえば、**ISO 20022 の口座振替**のコンフィギュレーションを使用する場合、仕入先の連絡先担当者の電子メールアドレスを表すノードは、`'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email` です。</span><span class="sxs-lookup"><span data-stu-id="e4002-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="e4002-136">[![電子メール アドレス ソースのコンフィギュレーション](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="e4002-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4002-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e4002-137">Additional resources</span></span>

- [<span data-ttu-id="e4002-138">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="e4002-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e4002-139">電子申告 (ER) の送信先</span><span class="sxs-lookup"><span data-stu-id="e4002-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="e4002-140">電子申告 (ER) のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="e4002-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)

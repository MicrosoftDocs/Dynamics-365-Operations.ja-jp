---
title: ER コンフィギュレーション先
description: この手順では、フォルダーまたはファイルなどの電子申告 (ER) の出力コンポーネントにさまざまな出力先を設定して使用する方法を示します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbef5410d0e6f15fbb5025f3831486d55cd06216
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185063"
---
# <a name="er-configure-destinations"></a><span data-ttu-id="36b62-103">ER コンフィギュレーション先</span><span class="sxs-lookup"><span data-stu-id="36b62-103">ER Configure destinations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="36b62-104">この手順では、フォルダーまたはファイルなどの電子申告 (ER) の出力コンポーネントにさまざまな出力先を設定して使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="36b62-104">This procedure demonstrates how to set up and use different destinations for Electronic reporting (ER) output components, such as a folder or a file.</span></span> <span data-ttu-id="36b62-105">この手順の作成に使用するデモ データの会社は DEMF です。</span><span class="sxs-lookup"><span data-stu-id="36b62-105">The demo data company used to create this procedure is DEMF.</span></span> <span data-ttu-id="36b62-106">ドイツが法人の一次的住所のある国/地域になっていますが、この手順ではあらゆる法人を使用できます。</span><span class="sxs-lookup"><span data-stu-id="36b62-106">Germany is the country\region of the legal entity’s primary address, however you can use any legal entity for this procedure.</span></span> 

<span data-ttu-id="36b62-107">この例で使用する形式は ISO20022 債権移動ですが、既にインポートした形式であればどんな形式でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="36b62-107">The format used in this example is ISO20022 Credit transfer, but you can use any format that you have already imported.</span></span> <span data-ttu-id="36b62-108">この手順は 1 つのファイルと1つの出力先からなる設定の例であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="36b62-108">Note, this procedure is an example of a single file and a single destination setup.</span></span> <span data-ttu-id="36b62-109">電子レポート送信先管理に関する詳細については、Dynamics 365 Finance ヘルプで確認できます。</span><span class="sxs-lookup"><span data-stu-id="36b62-109">More information about Electronic reporting destination management can be found in the Dynamics 365 Finance Help.</span></span>

1. <span data-ttu-id="36b62-110">[組織管理] > [電子申告] > [電子申告の送信先] に選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-110">Go to Organization administration > Electronic reporting > Electronic reporting destination.</span></span>
2. <span data-ttu-id="36b62-111">形式の送信先のための新しいセットを作成するには、[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-111">Click New to create a new set of destinations for a format.</span></span>
3. <span data-ttu-id="36b62-112">[参照] フィールドで、送信先をコンフィギュレーションする形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-112">In the Reference field, select a format for which you want to configure destinations.</span></span>
    * <span data-ttu-id="36b62-113">選択する値がない場合、電子申告の形式のコンフィギュレーションをインポートしていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="36b62-113">If you don't have a value to select, it means that you have not imported any Electronic reporting format configurations.</span></span> <span data-ttu-id="36b62-114">出力先を設定する前に、形式のコンフィギュレーションをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="36b62-114">You must import a format configuration before setting up destinations.</span></span>  
4. <span data-ttu-id="36b62-115">新しいファイルの送信先を作成するには、[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-115">Click New to create a new file destination.</span></span>
    * <span data-ttu-id="36b62-116">フォルダーまたはファイルなどの同じ形式の各生産コンポーネントに対して 1 つのファイル出力先を作成できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="36b62-116">Note, you can create one file destination for each output component of the same format, such as a folder or a file.</span></span> <span data-ttu-id="36b62-117">設定で出力先を個別に有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="36b62-117">You will be able to enable and disable destinations separately in the settings.</span></span>  
5. <span data-ttu-id="36b62-118">[名称] フィールドで、出力コンポーネントのわかりやすい名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="36b62-118">In the Name field, enter the user-friendly name of output component.</span></span>
    * <span data-ttu-id="36b62-119">「支払ファイル」や「管理レポート」などわかりやすい名前を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="36b62-119">We recommend that you use meaningful names, such as "Payment file" or "Control report".</span></span> <span data-ttu-id="36b62-120">これらの名前は、出力先の設定とともにコンフィギュレーション ランタイムでユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="36b62-120">These names will be presented to users at configuration runtime along with the destination settings.</span></span>  
6. <span data-ttu-id="36b62-121">ファイル名で、形式固有のファイルまたはフォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-121">In the File name, select a file or folder that is specific to the format.</span></span>
7. <span data-ttu-id="36b62-122">[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-122">Click Settings.</span></span>
8. <span data-ttu-id="36b62-123">[有効] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-123">Select Yes in the Enabled field.</span></span>
    * <span data-ttu-id="36b62-124">各タブの [有効] のチェック ボックスで、各出力先を個別に有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="36b62-124">The Enabled check box on each tab enables and disables each destination separately.</span></span> <span data-ttu-id="36b62-125">この例では、ファイル生成時にメール受信者への出力ファイルの送信を有効にします。</span><span class="sxs-lookup"><span data-stu-id="36b62-125">In this example, you'll enable sending an output file to a mail recipient when the file is generated.</span></span>  
9. <span data-ttu-id="36b62-126">[編集] をクリックし、電子メールの受信者を設定します。</span><span class="sxs-lookup"><span data-stu-id="36b62-126">Click Edit, to set up email recipients.</span></span>
10. <span data-ttu-id="36b62-127">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-127">Click Add.</span></span>
11. <span data-ttu-id="36b62-128">[管理電子メールの印刷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-128">Click Print Management email.</span></span>
12. <span data-ttu-id="36b62-129">[電子メール ソース ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-129">In the Email source  field, select an option.</span></span>
    * <span data-ttu-id="36b62-130">顧客または仕入先のタイプなど、さまざまな電子メールのソース タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="36b62-130">You can select different email source types, such as a customer or a vendor type.</span></span> <span data-ttu-id="36b62-131">これは、電子メール ソースの式によって返される引数のタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="36b62-131">This defines the type of argument that will be returned by the Email source account formula.</span></span> <span data-ttu-id="36b62-132">次の手順で説明する電子メール ソースの式は、電子メール ソースをバインドします。</span><span class="sxs-lookup"><span data-stu-id="36b62-132">The Email source account formula, described in a following step, is the place where you bind an email source.</span></span> <span data-ttu-id="36b62-133">式が仕入先を返す場合、[仕入先] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-133">Select Vendor if your formula will return a vendor account.</span></span> <span data-ttu-id="36b62-134">ISO 20022 の口座振替のコンフィギュレーションの例を使用している場合、[仕入先] を使用します。</span><span class="sxs-lookup"><span data-stu-id="36b62-134">Use Vendor if you are using the ISO 20022 Credit Transfer configuration example.</span></span>  
13. <span data-ttu-id="36b62-135">[電子メール ソースをバインドする] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-135">Click Email source bind button.</span></span>
14. <span data-ttu-id="36b62-136">式で、前に選択した関係者タイプにドキュメント固有の参照を入力します。</span><span class="sxs-lookup"><span data-stu-id="36b62-136">In the Formula, enter a document-specific reference to a party type that you selected earlier.</span></span>
    * <span data-ttu-id="36b62-137">入力する代わりに、関係者の口座を表すデータ ソース ノードを検索できます。また [データ ソースの追加] ボタンをクリックして、式を更新することができます。</span><span class="sxs-lookup"><span data-stu-id="36b62-137">Instead of typing, you can find a data source node that represents the party account, and click the Add data source button to update the formula.</span></span> <span data-ttu-id="36b62-138">たとえば、ISO 20022 の債権移動コンフィギュレーションを使用する場合、仕入先口座を表すノードは、'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID となります。</span><span class="sxs-lookup"><span data-stu-id="36b62-138">For example, if you use the ISO 20022 Credit Transfer configuration, the node representing a vendor account is '$PaymentsForCoveringLetter'.Creditor.Identification.SourceID.</span></span> <span data-ttu-id="36b62-139">それ以外の場合は、「DE-001」など任意の文字列型の値を入力して式を保存します。</span><span class="sxs-lookup"><span data-stu-id="36b62-139">Otherwise, enter any string value, such as "DE-001", to save a formula.</span></span>  
15. <span data-ttu-id="36b62-140">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-140">Click Save.</span></span>
16. <span data-ttu-id="36b62-141">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="36b62-141">Close the page.</span></span>
17. <span data-ttu-id="36b62-142">「編集して関係者の連絡先情報を環境設定する」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-142">Click Edit to configure contact details for the party.</span></span>
18. <span data-ttu-id="36b62-143">[一次的連絡先] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36b62-143">Select Yes in the Primary contact field.</span></span>
    * <span data-ttu-id="36b62-144">各種のオプションを使用して、関係者のどのタイプの連絡先をメール アドレスとして使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="36b62-144">You may use different options to indicate what contact type of the party should be used as an email address for this destination.</span></span> <span data-ttu-id="36b62-145">この例では、一次的連絡先 を使用します。</span><span class="sxs-lookup"><span data-stu-id="36b62-145">We use primary contact in this example.</span></span>  
19. <span data-ttu-id="36b62-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-146">Click OK.</span></span>
20. <span data-ttu-id="36b62-147">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-147">Click OK.</span></span>
21. <span data-ttu-id="36b62-148">[件名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="36b62-148">In the Subject field, type a value.</span></span>
22. <span data-ttu-id="36b62-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36b62-149">Click OK.</span></span>

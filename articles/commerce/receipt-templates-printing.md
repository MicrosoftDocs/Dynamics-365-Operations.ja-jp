---
title: 受領書フォーマットを設定しデザインします
description: この記事は、フォーム レイアウトを変更して、レシート、請求書、およびその他の文書の印刷方法を制御する方法について説明します。 Dynamics 365 Commerce には、さまざまな種類のフォーム レイアウトを簡単に作成および変更するフォーム レイアウト デザイナーが用意されています。
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c44798c6b879ebd95618d976beebe1d41b40dcdd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243748"
---
# <a name="set-up-and-design-receipt-formats"></a><span data-ttu-id="59cca-104">受領書フォーマットを設定しデザインします</span><span class="sxs-lookup"><span data-stu-id="59cca-104">Set up and design receipt formats</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59cca-105">この記事は、フォーム レイアウトを変更して、レシート、請求書、およびその他の文書の印刷方法を制御する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="59cca-105">This article describes how to modify form layouts to control how receipts, invoices, and other documents are printed.</span></span> <span data-ttu-id="59cca-106">Dynamics 365 Commerce には、さまざまな種類のフォーム レイアウトを簡単に作成および変更するフォーム レイアウト デザイナーが用意されています。</span><span class="sxs-lookup"><span data-stu-id="59cca-106">Dynamics 365  Commerce includes a form layout designer that you can use to easily create and modify various kinds of form layouts.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59cca-107">Retail Modern POS と Cloud POS からレシートやその他の文書を印刷するために、フォーム レイアウトおよびレシート プロファイルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59cca-107">You must set up form layouts and receipt profiles to print receipts and other documents from Retail Modern POS and Cloud POS.</span></span> <span data-ttu-id="59cca-108">レシート プロファイルに複数のフォーム レイアウトを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="59cca-108">You can include multiple form layouts in a receipt profile.</span></span> <span data-ttu-id="59cca-109">ハードウェア プロファイルを変更して、プリンタにレシート プロファイルを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="59cca-109">You can then assign the receipt profile to a printer by modifying a hardware profile.</span></span>

## <a name="set-up-a-receipt-format"></a><span data-ttu-id="59cca-110">受領書フォーマットの設定</span><span class="sxs-lookup"><span data-stu-id="59cca-110">Set up a receipt format</span></span>

1. <span data-ttu-id="59cca-111">**Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS** &gt; **受領書フォーマット** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-111">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Receipt formats**.</span></span>
2. <span data-ttu-id="59cca-112">**受領書フォーマット** ページにて、**新規** をクリックし、新しいフォーム レイアウトを作成するか、既存のフォーム レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="59cca-112">On the **Receipt format** page, click **New** to create a new form layout, or select an existing form layout.</span></span>
3. <span data-ttu-id="59cca-113">**受領書フォーマット** フィールドで、フォーム レイアウトの ID を入力して、このレイアウトを使用するレシート タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="59cca-113">In the **Receipt format** field, enter an identifier for the form layout, and then select the type of receipt that this layout is used for.</span></span> <span data-ttu-id="59cca-114">また、**タイトル** フィールドにレシートの説明と短縮名を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="59cca-114">You can also enter a description and a short name for the receipt in the **Title** field.</span></span>
4. <span data-ttu-id="59cca-115">**概要** クイック タブで、印刷動作を定義するオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="59cca-115">On the **General** FastTab, select an option to define the print behavior:</span></span>

    - <span data-ttu-id="59cca-116">**常に印刷する** – 必要に応じて、レシートが自動的に印刷されます。</span><span class="sxs-lookup"><span data-stu-id="59cca-116">**Always print** – The receipt is printed automatically, as appropriate.</span></span>
    - <span data-ttu-id="59cca-117">**印刷しない** – レシートは印刷されません。</span><span class="sxs-lookup"><span data-stu-id="59cca-117">**Do not print** – The receipt isn't printed.</span></span>
    - <span data-ttu-id="59cca-118">**ユーザーに確認する** – ユーザーはレシートを印刷するように求められます。</span><span class="sxs-lookup"><span data-stu-id="59cca-118">**Prompt user** – The user is prompted to print the receipt.</span></span>
    - <span data-ttu-id="59cca-119">**必要時** – このオプションは、ギフト レシートにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="59cca-119">**As required** – This option is used only for gift receipts.</span></span> <span data-ttu-id="59cca-120">ギフト レシートが必要な場合は、このオプションを選択すると、ユーザーは **変更** ページからギフト レシートを印刷できます。</span><span class="sxs-lookup"><span data-stu-id="59cca-120">When this option is selected, the user can print a gift receipt from the **Change** page, if a gift receipt is required.</span></span>

## <a name="print-images"></a><span data-ttu-id="59cca-121">画像の印刷</span><span class="sxs-lookup"><span data-stu-id="59cca-121">Print images</span></span>

<span data-ttu-id="59cca-122">レシート デザイナーには、レシートに印刷される画像の指定に使用できる **ロゴ** 変数が含まれています。</span><span class="sxs-lookup"><span data-stu-id="59cca-122">The receipt designer includes a **Logo** variable that can be used to specify images to be printed on the receipt.</span></span> <span data-ttu-id="59cca-123">**ロゴ** 変数を使用して領収書に含める画像は、モノクロのビットマップ(.bmp)ファイルタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="59cca-123">Images that are included in receipts using the **Logo** variable should be monochrome bitmap (.bmp) file types.</span></span> <span data-ttu-id="59cca-124">レシートデザイナーで .bmp 画像を指定していても、プリンタへの送信時に印刷されない場合、ファイルサイズが大きすぎるか、画像のピクセル サイズがプリンタに対応していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="59cca-124">If a .bmp image is specified in the receipt designer, but is not printing when sent to the printer, the file size may be too large or the pixel dimensions on the image are not compatible with the printer.</span></span> <span data-ttu-id="59cca-125">この場合は、画像ファイルの解像度を下げてみてください。</span><span class="sxs-lookup"><span data-stu-id="59cca-125">If this occurs, try reducing the image file resolution.</span></span>   

## <a name="design-a-receipt-format"></a><span data-ttu-id="59cca-126">受領書フォーマットのデザイン</span><span class="sxs-lookup"><span data-stu-id="59cca-126">Design a receipt format</span></span>

<span data-ttu-id="59cca-127">フォーム レイアウト デザイナーを使用して、フォーム文書のレイアウトをグラフィカルに作成します。</span><span class="sxs-lookup"><span data-stu-id="59cca-127">Use the form layout designer to graphically create the layout of the form document.</span></span> <span data-ttu-id="59cca-128">**受領書フォーマット デザイナー** ページには 3 つのセクションがあります。**ヘッダー**、**明細行**、および **フッター** です。</span><span class="sxs-lookup"><span data-stu-id="59cca-128">The **Receipt format designer** page has three sections: **Header**, **Lines**, and **Footer**.</span></span> <span data-ttu-id="59cca-129">3 つのすべてのセクションの要素を使用するフォーム レイアウトもあれば、1 つまたは 2 つのセクションの要素しか使用しないフォーム レイアウトもあります。</span><span class="sxs-lookup"><span data-stu-id="59cca-129">Some types of form layouts use elements from all three sections, whereas other types use elements from only one or two sections.</span></span> <span data-ttu-id="59cca-130">各セクションで使用できる要素を表示するには、ページの左側のナビゲーション ウィンドウのボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-130">To view the elements that are available for each section, click the appropriate button in the navigation pane on the left side of the page.</span></span>

1. <span data-ttu-id="59cca-131">**Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS** &gt; **受領書フォーマット** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-131">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Receipt formats**.</span></span>
2. <span data-ttu-id="59cca-132">**受領書フォーマット** ページで、フォーム レイアウトを選択し、**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-132">On the **Receipt format** page, select a form layout, and then click **Designer**.</span></span>
3. <span data-ttu-id="59cca-133">コマース デザイナー ホストのインストールを開始するには、**実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-133">Click **Run** to start to install the Commerce designer host.</span></span>
4. <span data-ttu-id="59cca-134">ワンクリック デザイナーのインストールを開始する場合、Internet Explorer ウィンドウの下部に表示される通知バーの **開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-134">On the Notification bar that appears at the bottom of the Internet Explorer window, click **Open** to start to install the one-click designer.</span></span> <span data-ttu-id="59cca-135">(通知バーは、他のブラウザの別の場所に表示されることがあります。) 進行状況インジケータは、インストール プロセスの進行状況を示します。</span><span class="sxs-lookup"><span data-stu-id="59cca-135">(The Notification bar might appear in a different location in other browsers.) The progress indicator shows the progress of the installation process.</span></span>
5. <span data-ttu-id="59cca-136">インストール完了後に、デザイナーを開始する場合、コマースのユーザー名とパスワードを入力し、**サインイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-136">After the installation is completed, enter your Commerce user name and password, and then click **Sign in** to start the designer.</span></span>
6. <span data-ttu-id="59cca-137">資格情報を検証しデザイナーを開始した後に、受領書フォーマットを作成するか、または既存のフォーマットを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="59cca-137">After your credentials are validated and the designer starts, you can start to design the receipt format or modify an existing format.</span></span>
7. <span data-ttu-id="59cca-138">フォームの要素を作成するには、**ヘッダー**、**明細行**、または **フッター** セクションを選択し、セクションの要素をワークスペースにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="59cca-138">To create the elements of the form, select the **Header**, **Lines**, or **Footer** section, and then drag an element from that section to the workspace.</span></span> <span data-ttu-id="59cca-139">ほとんどの要素は、データベースからデータが自動的に入力される変数で構成されます。</span><span class="sxs-lookup"><span data-stu-id="59cca-139">Most elements contain variables that are automatically populated with data from the database.</span></span> <span data-ttu-id="59cca-140">**テキスト** などのその他の要素は、カスタム テキストをレシートに印刷できます。</span><span class="sxs-lookup"><span data-stu-id="59cca-140">Other elements, such as **Text**, let you print custom text on the receipt.</span></span>

    > [!NOTE]
    > <span data-ttu-id="59cca-141">それぞれのセクションで使用する行数は、そのセクションの右下隅にある数値を調整することで選択できます。</span><span class="sxs-lookup"><span data-stu-id="59cca-141">You can specify how many lines each section spans by adjusting the number in the lower-right corner of that section.</span></span> <span data-ttu-id="59cca-142">セクションを変更しやすいように、セクション下部のサイズ変更バーをドラッグして、その高さを増やします。</span><span class="sxs-lookup"><span data-stu-id="59cca-142">To make it easier to modify a section, increase its height by dragging the sizing bar at the bottom of the section.</span></span> <span data-ttu-id="59cca-143">ワークスペースのセクションの高さは、実際のレシートの行数に影響しません。</span><span class="sxs-lookup"><span data-stu-id="59cca-143">The height of the section on the workspace doesn't affect the number of lines on the actual receipt.</span></span>

8. <span data-ttu-id="59cca-144">要素をワークスペースにドラッグした後、ページ下部にある **オブジェクト情報** ウィンドウでパーツのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="59cca-144">After you drag an element to the workspace, set the properties for the part in the **Object information** pane at the bottom of the page.</span></span> <span data-ttu-id="59cca-145">次の 1 つまたは複数の設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="59cca-145">Enter one or more of the following settings:</span></span>

    - <span data-ttu-id="59cca-146">**配置** – フィールドの配置を **左** または **右** に設定します。</span><span class="sxs-lookup"><span data-stu-id="59cca-146">**Align** – Set the alignment of the field to either **Left** or **Right**.</span></span>
    - <span data-ttu-id="59cca-147">**充填文字** - 空白文字を指定します。</span><span class="sxs-lookup"><span data-stu-id="59cca-147">**Fill char** – Specify the white space character.</span></span> <span data-ttu-id="59cca-148">既定では、空白を使用しますが、任意の文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="59cca-148">By default, an empty space is used, but you can enter any character.</span></span>
    - <span data-ttu-id="59cca-149">**接頭語** - フィールドの先頭に表示される値を入力します。</span><span class="sxs-lookup"><span data-stu-id="59cca-149">**Prefix** – Enter the value that appears at the beginning of the field.</span></span> <span data-ttu-id="59cca-150">この設定は、レイアウトの **明細行** セクションにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="59cca-150">This setting applies only to the **Lines** section of the layout.</span></span>
    - <span data-ttu-id="59cca-151">**文字** – 要素に変数が含まれている場合に、フィールドに含めることができる文字の最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="59cca-151">**Characters** – Specify the maximum number of characters that the field can contain if the element contains a variable.</span></span> <span data-ttu-id="59cca-152">フィールドのテキストが指定した文字数よりも長い場合は、フィールドに合わせて切り詰められます。</span><span class="sxs-lookup"><span data-stu-id="59cca-152">If the text in the field is longer than the number of character that you specify, the text is truncated to fit the field.</span></span>
    - <span data-ttu-id="59cca-153">**変数** - 要素が変数を含むためにカスタマイズできない場合は、このチェック ボックスが自動的にオンになります。</span><span class="sxs-lookup"><span data-stu-id="59cca-153">**Variable** – This check box is selected automatically if the element contains a variable and can't be customized.</span></span>
    - <span data-ttu-id="59cca-154">**フォントの種類** - フォント スタイルを **通常** または **太字** に設定します。</span><span class="sxs-lookup"><span data-stu-id="59cca-154">**Font type** – Set the font style to either **Regular** or **Bold**.</span></span> <span data-ttu-id="59cca-155">太字の文字は、通常の文字の 2 倍のスペースを使用します。</span><span class="sxs-lookup"><span data-stu-id="59cca-155">Bold letters use two times as much space as regular letters.</span></span> <span data-ttu-id="59cca-156">したがって、一部の文字が切り詰められる場合があります。</span><span class="sxs-lookup"><span data-stu-id="59cca-156">Therefore, some characters might be truncated.</span></span>
    - <span data-ttu-id="59cca-157">**フォント サイズ** - フォント サイズを **通常** または **大** に設定します。</span><span class="sxs-lookup"><span data-stu-id="59cca-157">**Font size** – Set the font size to either **Regular** or **Large**.</span></span> <span data-ttu-id="59cca-158">[大] の文字は [通常] の文字より 2 倍高くなります。</span><span class="sxs-lookup"><span data-stu-id="59cca-158">Large letters are two times higher than regular letters.</span></span> <span data-ttu-id="59cca-159">したがって、[大] の文字を使用すると、レシートでテキストが重なる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="59cca-159">Therefore, using large letters may lead to overlapping text in the receipt.</span></span>
    - <span data-ttu-id="59cca-160">**削除** – 選択したパーツをフォーム レイアウトから削除する場合は、このボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="59cca-160">**Delete** – Click this button to remove the selected part from the form layout.</span></span>

## <a name="assign-receipt-profiles"></a><span data-ttu-id="59cca-161">レシート プロファイルの割り当て</span><span class="sxs-lookup"><span data-stu-id="59cca-161">Assign receipt profiles</span></span>

<span data-ttu-id="59cca-162">ハードウェア プロファイルを通じてレシート プロファイルがプリンタへ直接割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="59cca-162">Receipt profiles are assigned directly to printers through the hardware profile.</span></span>

1. <span data-ttu-id="59cca-163">**Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **ハードウェア プロファイル** をクリックして、ハードウェア プロファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="59cca-163">Open the hardware profile by clicking **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profiles** &gt; **Hardware profile**.</span></span>
2. <span data-ttu-id="59cca-164">次に、プリンタを選択し、**レシート プロファイル** フィールドで、レジスターを使用してレシート プロファイルを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="59cca-164">Select the printer, and then, in the **Receipt profile** field, assign the receipt profile to use on the register.</span></span>

> [!NOTE]
> <span data-ttu-id="59cca-165">2 つのプリンターを使用する場合、１ つ目のプリンターは標準の 40 列のサーマル レシートの印刷に使用できます。</span><span class="sxs-lookup"><span data-stu-id="59cca-165">If two printers are used, one printer can be used to print standard 40-column thermal receipts.</span></span> <span data-ttu-id="59cca-166">2 番目のプリンタは、通常、詳細情報を要求する全ページのレシート タイプの印刷に使用されます。</span><span class="sxs-lookup"><span data-stu-id="59cca-166">The second printer is typically used to print full-page receipt types that require more information.</span></span> <span data-ttu-id="59cca-167">これらのレシート タイプでは、顧客注文のレシートおよび顧客請求書が含まれます。</span><span class="sxs-lookup"><span data-stu-id="59cca-167">These receipt types include customer order receipts and customer invoices.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
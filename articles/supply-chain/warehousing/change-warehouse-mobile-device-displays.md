---
title: "倉庫モバイル デバイスの表示設定"
description: "この記事では、モバイル デバイスの表示の外観を設定する方法、キーボード ショートカットをボタンのようなコントロールにマッピングする方法を説明します。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFColor, WHSRFColorPicker, WHSWorkUserDisplaySettings
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 29071
ms.assetid: 931a02e8-b561-45e3-9c44-06b875ced1b4
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 16f332da00d2230ecb4cebc526b6456314564e55
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="warehouse-mobile-device-display-settings"></a><span data-ttu-id="aecde-103">倉庫モバイル デバイスの表示設定</span><span class="sxs-lookup"><span data-stu-id="aecde-103">Warehouse mobile device display settings</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aecde-104">この記事では、モバイル デバイスの表示の外観を設定する方法、キーボード ショートカットをボタンのようなコントロールにマッピングする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="aecde-104">This article describes how to set up the appearance of a mobile device display and map keyboard shortcuts to controls such as buttons.</span></span> 

<span data-ttu-id="aecde-105">この項目は、倉庫管理での「詳細な倉庫保管」機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="aecde-105">This article applies to "advanced warehousing" features in Warehouse management.</span></span> <span data-ttu-id="aecde-106">モバイル デバイスは、倉庫作業者が実行するタスクの多くに使用できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-106">Mobile devices can be used for many of the tasks that warehouse workers perform.</span></span>

## <a name="specify-styles-and-map-keyboard-shortcuts"></a><span data-ttu-id="aecde-107">スタイルを指定し、キーボード ショートカットをマッピングします。</span><span class="sxs-lookup"><span data-stu-id="aecde-107">Specify styles and map keyboard shortcuts</span></span>
<span data-ttu-id="aecde-108">モバイル デバイスのコンフィギュレーションの一部として、モバイル デバイスの異なるレイアウトを定義できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-108">As part of the mobile device configuration, you can define different layouts for mobile devices.</span></span> <span data-ttu-id="aecde-109">これを行うには、カスケード スタイル シート (CSS) のファイルや、Active Server Page Extension (ASPX) ファイルの名前を知る必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-109">To do this, you must know the name of the Cascading Style Sheets (CSS) file and the Active Server Page Extension (ASPX) file.</span></span> <span data-ttu-id="aecde-110">既定のファイルは、倉庫モバイル デバイスのポータルインストールの一部としてインストールされます。</span><span class="sxs-lookup"><span data-stu-id="aecde-110">Default files are installed as part of the Warehouse Mobile Devices Portal installation.</span></span> <span data-ttu-id="aecde-111">ファイル名がわからない場合は、システム管理者に尋ねます。</span><span class="sxs-lookup"><span data-stu-id="aecde-111">If you don’t know the file names, ask your system administrator.</span></span> <span data-ttu-id="aecde-112">新しいスタイルを**モバイル デバイス表示設定**ページで定義できます:</span><span class="sxs-lookup"><span data-stu-id="aecde-112">You can define a new style on the **Mobile device display settings** page:</span></span>

-    <span data-ttu-id="aecde-113">**CSS ファイル**フィールドで CSS ファイルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="aecde-113">In the **CSS file** field, enter the name of your CSS file.</span></span> <span data-ttu-id="aecde-114">.css ファイル名拡張子を含めてください。</span><span class="sxs-lookup"><span data-stu-id="aecde-114">Include the .css file name extension.</span></span>
-   <span data-ttu-id="aecde-115">**モバイル デバイス表示設定ビュー**フィールドで、ASPX ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="aecde-115">In the **Mobile device display settings view** field, specify the ASPX file.</span></span> <span data-ttu-id="aecde-116">.aspx ファイル名拡張子を**含めない**でください。</span><span class="sxs-lookup"><span data-stu-id="aecde-116">Do **not** include the .aspx file name extension.</span></span>

<span data-ttu-id="aecde-117">CSS と ASPX ファイルは、Internet Information Services (IIS) アプリケーションがそれらを読み込むために、特定のディレクトリにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-117">The CSS and ASPX files must be located in a specific directory, so that the Internet Information Services (IIS) application can load them.</span></span> <span data-ttu-id="aecde-118">異なるブラウザでモバイル デバイスの機能を実行する場合、あるいは、異なるレイアウト コントロールを要求するさまざまな種類のハードウェアを実行する場合、異なる CSS のファイルを定義しておくと便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-118">It might be useful to define different CSS files if you're running the mobile device functionality in different browsers or on different kinds of hardware that require different layout control.</span></span> <span data-ttu-id="aecde-119">テキストの背景色、フォント、フォント サイズ、ボタンの幅と動作などの簡単な設定は、異なる CSS ファイルを使用して、簡単に制御できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-119">Simple settings such as the background color, the font and font size for text, and the width and behavior of buttons, can easily be controlled by different use of CSS files.</span></span> <span data-ttu-id="aecde-120">ASPX ファイルは、サーバー側 ASP.NET アプリケーションの携帯サイトの表示に使用されます。</span><span class="sxs-lookup"><span data-stu-id="aecde-120">The ASPX file is used to display the mobile site on the server-side ASP.NET application.</span></span> <span data-ttu-id="aecde-121">このファイルは HTML の全体的な構造の設定を制御します。HTML および JavaScript の重大な構造の問題がある場合、および、特定のデバイスでこのコードを変更する必要がある場合にのみ、この機能をカスタマイズすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="aecde-121">The file controls how the overall structure of the HTML is laid out. It's a good idea to customize this functionality only if you have serious structural issues with the HTML and JavaScript, and must change this code for your specific devices.</span></span> <span data-ttu-id="aecde-122">モバイル デバイスのページで HTML コントロールをマッピングするには、**モバイル デバイス表示設定**ページの**キーボード ショートカット**フィールドで、キーの数値コードを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="aecde-122">To map the HTML controls on the mobile device page to keyboard shortcuts, on the **Mobile device display settings** page, in the **Keyboard shortcut** field, assign the numeric codes for the keys.</span></span> <span data-ttu-id="aecde-123">モバイル デバイスで数値文字のコードを検索する場合、**キーボード ショートカットのコードを表示**メニューを使用できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-123">You can use the **View codes for keyboard shortcuts** menu on the mobile device to find the numeric character codes.</span></span> <span data-ttu-id="aecde-124">使用するハードウェアによって、マッピングが異なる場合があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="aecde-124">Note that the mappings might differ, depending on the hardware that is used.</span></span> <span data-ttu-id="aecde-125">マッピングを作成するには、次の構文を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-125">You must use the following syntax to create the mapping:</span></span>

<span data-ttu-id="aecde-126">&lt;制御名&gt;(&lt;キー名&gt;)=&lt;キー コード&gt;;</span><span class="sxs-lookup"><span data-stu-id="aecde-126">&lt;control name&gt;(&lt;key name&gt;)=&lt;key code&gt;;</span></span>

<span data-ttu-id="aecde-127">構文の一部の説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="aecde-127">Here is an explanation of the parts of the syntax:</span></span>

-   <span data-ttu-id="aecde-128">**&lt;制御名&gt;** – HTML で表示するコントロール (ボタンなど) の名前。</span><span class="sxs-lookup"><span data-stu-id="aecde-128">**&lt;control name&gt;** – The name of the control (for example, a button) that is rendered in HTML.</span></span>
-   <span data-ttu-id="aecde-129">**(&lt;キー名&gt;)** – ショートカットを作成するキーボード キーの名前。</span><span class="sxs-lookup"><span data-stu-id="aecde-129">**(&lt;key name&gt;)** – The name of the keyboard key that you’re creating the shortcut for.</span></span>
-   <span data-ttu-id="aecde-130">**&lt;キー コード&gt;** – ショートカット キーに使用するキーの数値文字のコード。</span><span class="sxs-lookup"><span data-stu-id="aecde-130">**&lt;Key code&gt;** – The numeric character code for the key to use as the shortcut key.</span></span>

<span data-ttu-id="aecde-131">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="aecde-131">Here is an example:</span></span>

<span data-ttu-id="aecde-132">キャンセル (Esc) =27; 完全 (F2) =113</span><span class="sxs-lookup"><span data-stu-id="aecde-132">Cancel(Esc)=27; Full(F2)=113</span></span>

<span data-ttu-id="aecde-133">**キャンセル**ボタンを含むすべてのページで、ボタンにはこのテキストがあります:</span><span class="sxs-lookup"><span data-stu-id="aecde-133">On all pages that include a **Cancel** button, the button will have this text:</span></span>

<span data-ttu-id="aecde-134">**(Esc) キャンセル**</span><span class="sxs-lookup"><span data-stu-id="aecde-134">**(Esc) Cancel**</span></span>

<span data-ttu-id="aecde-135">キーボードの ESC キーを押すと、**キャンセル**ボタンが有効になります。</span><span class="sxs-lookup"><span data-stu-id="aecde-135">Pressing the Esc key on the keyboard will activate the **Cancel** button.</span></span> <span data-ttu-id="aecde-136">特定のデバイスにスタイル、およびキーボード ショートカットの設定を適用するには、**基準**フィールドでマッピングを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-136">To apply the style and keyboard shortcut settings to a specific device, you must create a mapping in the **Criteria** field.</span></span> <span data-ttu-id="aecde-137">マッピングを作成するには、.NET 正規表現を使用する必要があり、次のように、式は縦棒 (|) で区切る 3 つのセクションで構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-137">You must use a .NET regular expression to create the mapping, and the expression must consist of three sections that are separated by a vertical bar (|), as shown here:</span></span>

<span data-ttu-id="aecde-138">Request.UserHostAddress=&lt;ユーザーのホスト アドレス&gt;|HostName=&lt;ユーザーのホスト名&gt;|Request.UserAgent=&lt;ユーザー エージェント&gt;</span><span class="sxs-lookup"><span data-stu-id="aecde-138">Request.UserHostAddress=&lt;user host address&gt;|HostName=&lt;user host name&gt;|Request.UserAgent=&lt;user agent&gt;</span></span>

<span data-ttu-id="aecde-139">式の一部の説明を次に示します。</span><span class="sxs-lookup"><span data-stu-id="aecde-139">Here is an explanation of the parts of the expression:</span></span>

-   <span data-ttu-id="aecde-140">**&lt;ユーザーのホスト アドレス&gt;** – 要求元の IP アドレスに一致する .NET 正規表現。</span><span class="sxs-lookup"><span data-stu-id="aecde-140">**&lt;user host address&gt;** – A .NET regular expression that matches the requestor IP address.</span></span>
-   <span data-ttu-id="aecde-141">**&lt;ユーザーのホスト名&gt;** – 要求元のネットワーク名に一致する .NET 正規表現。</span><span class="sxs-lookup"><span data-stu-id="aecde-141">**&lt;user host name&gt;** – A .NET regular expression that matches the network name of the requestor.</span></span>
-   <span data-ttu-id="aecde-142">**&lt;ユーザー エージェント&gt;** – 要求元が使用するブラウザーの ID に一致する .NET 正規表現。</span><span class="sxs-lookup"><span data-stu-id="aecde-142">**&lt;user agent&gt;** – A .NET regular expression that matches the identifier of the browser that the requestor uses.</span></span>

<span data-ttu-id="aecde-143">次の例では、Internet Explorer 8 の使用を有効にします。</span><span class="sxs-lookup"><span data-stu-id="aecde-143">The following example enables Internet Explorer 8 to be used:</span></span>

<span data-ttu-id="aecde-144">Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0</span><span class="sxs-lookup"><span data-stu-id="aecde-144">Request.UserHostAddress=.\*|HostName=.\*|Request.UserAgent=MSIE\\s8\\.0</span></span>

<span data-ttu-id="aecde-145">モバイル デバイスの**表示設定のサーバー コンフィギュレーションを表示**メニューを設定の情報の検索に使用できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-145">You can use the **View server configuration for display settings** menu on the mobile device to find the information about the setup.</span></span>

## <a name="define-text-colors-for-messages"></a><span data-ttu-id="aecde-146">メッセージのテキストカラーを定義します。</span><span class="sxs-lookup"><span data-stu-id="aecde-146">Define text colors for messages</span></span>
<span data-ttu-id="aecde-147">**モバイル デバイスのテキスト カラー**ページでエラー メッセージなど、システムによって生成されるメッセージで使用されるさまざな色を管理できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-147">You can use the **Mobile device text colors** page to control the various colors that are used in system-generated messages, such as error messages.</span></span> <span data-ttu-id="aecde-148">たとえば、テキストカラーにより、メッセージの目的または重要度を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="aecde-148">For example, the text color can indicate the purpose or severity of the message.</span></span> <span data-ttu-id="aecde-149">以下のタイプのメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="aecde-149">The following types of messages are shown.</span></span>

| <span data-ttu-id="aecde-150">メッセージ タイプ</span><span class="sxs-lookup"><span data-stu-id="aecde-150">Message type</span></span> | <span data-ttu-id="aecde-151">説明</span><span class="sxs-lookup"><span data-stu-id="aecde-151">Description</span></span>                                                                                                                                                                            |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aecde-152">既定</span><span class="sxs-lookup"><span data-stu-id="aecde-152">Default</span></span>      | <span data-ttu-id="aecde-153">既定のメッセージでは、倉庫モバイル デバイス ポータルに CSS ファイルで定義される、既定の色設定がすべてのメッセージに使用されます。</span><span class="sxs-lookup"><span data-stu-id="aecde-153">Default messages use the default color settings for all messages, as defined by the CSS file for the Warehouse Mobile Device Portal.</span></span>                                                   |
| <span data-ttu-id="aecde-154">エラー</span><span class="sxs-lookup"><span data-stu-id="aecde-154">Error</span></span>        | <span data-ttu-id="aecde-155">エラー メッセージは、ユーザーが続行する前に解決しなければならない問題を示します。</span><span class="sxs-lookup"><span data-stu-id="aecde-155">Error messages indicate an issue that the user must resolve before he or she can continue.</span></span>                                                                                             |
| <span data-ttu-id="aecde-156">成功</span><span class="sxs-lookup"><span data-stu-id="aecde-156">Success</span></span>      | <span data-ttu-id="aecde-157">成功メッセージは、アクションが成功したことを確定します。</span><span class="sxs-lookup"><span data-stu-id="aecde-157">Success messages confirm that an action was successful.</span></span>                                                                                                                                |
| <span data-ttu-id="aecde-158">警告</span><span class="sxs-lookup"><span data-stu-id="aecde-158">Warning</span></span>      | <span data-ttu-id="aecde-159">警告メッセージは、作業者が続行するのに問題がある、あるいは問題がある可能性があることを作業者に通知します。</span><span class="sxs-lookup"><span data-stu-id="aecde-159">Warning messages inform the worker that there is an issue, or that there could be an issue if the worker continues.</span></span> <span data-ttu-id="aecde-160">ただし、作業者は続行するために、問題を解決する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="aecde-160">However, the worker doesn't have to resolve the issue to continue.</span></span> |

<span data-ttu-id="aecde-161">色を選択するには、**色の選択**ページで、パレットをクリックするか、16 進値の色コードを入力します。</span><span class="sxs-lookup"><span data-stu-id="aecde-161">To select the color, on the **Select color** page, click in the palette or type a hexadecimal color code.</span></span>

## <a name="define-the-date-format-to-use-on-mobile-devices"></a><span data-ttu-id="aecde-162">モバイル デバイスで使用する日付形式の定義</span><span class="sxs-lookup"><span data-stu-id="aecde-162">Define the date format to use on mobile devices</span></span>
<span data-ttu-id="aecde-163">各インストールで許容される日付形式の一覧を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="aecde-163">You can extend the list of accepted date formats for each installation.</span></span> <span data-ttu-id="aecde-164">たとえば、この機能は作業者がモバイル デバイス上で日付を入力しやすくなる形式を用意したい場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="aecde-164">This capability can be useful if, for example, you want to provide a format that makes it easier for a worker to enter dates on a mobile device.</span></span> <span data-ttu-id="aecde-165">既定の形式は、**ユーザー オプション**ページの、**言語**フィールドで指定された、ユーザーの既定の言語によって決まります。</span><span class="sxs-lookup"><span data-stu-id="aecde-165">The default format is determined by the user's default language, which is specified in the **Language** field on the **User options** page.</span></span> <span data-ttu-id="aecde-166">(特定の倉庫のユーザーに従業員を関連付ける場合も、同じページを使用します)。**注記:** 倉庫モバイル デバイス ポータルは、**言語と地域の基本設定**ページの、**日付、時刻、数字の形式**フィールドを使用しません。</span><span class="sxs-lookup"><span data-stu-id="aecde-166">(The same page is also used to associate an employee with a specific warehouse work user.) **Note:** The Warehouse Mobile Devices Portal doesn't use the setting of the **Date time and number format** field on the **Language and region preferences** page.</span></span> <span data-ttu-id="aecde-167">日付の形式を変更するには、Microsoft .NET Framework の正規表現を理解する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-167">To change a date format, you must be familiar with regular expressions in the Microsoft .NET Framework.</span></span> <span data-ttu-id="aecde-168">詳細については、「[.NET Framework の正規表現](http://go.microsoft.com/fwlink/?LinkId=391260)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aecde-168">For more information, see [.NET Framework Regular Expressions](http://go.microsoft.com/fwlink/?LinkId=391260).</span></span> <span data-ttu-id="aecde-169">日付の形式を定義するには、倉庫モバイル デバイス ポータル サーバーの Content\\Settings\\Dates.ini にある Dates.ini ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="aecde-169">To define date formats, edit the Dates.ini file that is located at Content\\Settings\\Dates.ini on the Warehouse Mobile Devices Portal server.</span></span> <span data-ttu-id="aecde-170">このファイルは日付の形式を指定するために .NET 正規表現を使用します。</span><span class="sxs-lookup"><span data-stu-id="aecde-170">This file uses .NET regular expressions to specify the date format.</span></span> <span data-ttu-id="aecde-171">次の例で示すように、正規表現には日、月、年 (DDMMYY) のための名前の付いたグループを作成する、下位表現を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-171">The regular expression must contain subexpressions that create named groups for day, month, and year (DDMMYY), as shown in the following example:</span></span>

<span data-ttu-id="aecde-172">^(?&lt;日&gt;\\d{2})(?&lt;月&gt;\\d{2})(?&lt;年&gt;\\d{2})$</span><span class="sxs-lookup"><span data-stu-id="aecde-172">^(?&lt;day&gt;\\d{2})(?&lt;month&gt;\\d{2})(?&lt;year&gt;\\d{2})$</span></span>

<span data-ttu-id="aecde-173">各下位表現には、日、および月に 1 桁か 2 桁、年に 1 桁から 4 桁が必要です。</span><span class="sxs-lookup"><span data-stu-id="aecde-173">Each subexpression requires one to two digits for the day and month, and one to four digits for the year.</span></span> <span data-ttu-id="aecde-174">たとえば、年の名前を付けられたグループを定義する次の下位表現で、最小で 2 桁、最大で 4 桁が必要です。</span><span class="sxs-lookup"><span data-stu-id="aecde-174">For example, the following subexpression defines a named group for a year, and requires a minimum of two digits or a maximum of four digits:</span></span>

<span data-ttu-id="aecde-175">(?&lt;年&gt;\\d{2,4})</span><span class="sxs-lookup"><span data-stu-id="aecde-175">(?&lt;year&gt;\\d{2,4})</span></span>

<span data-ttu-id="aecde-176">同じファイル内で複数の表現を指定できます。</span><span class="sxs-lookup"><span data-stu-id="aecde-176">You can specify more than one expression in the same file.</span></span> <span data-ttu-id="aecde-177">各表現は別々の行である必要があります。</span><span class="sxs-lookup"><span data-stu-id="aecde-177">Each expression must be on a separate line.</span></span> <span data-ttu-id="aecde-178">一致する最初の表現が日付の解析に使用されます。</span><span class="sxs-lookup"><span data-stu-id="aecde-178">The first expression that is matched is used to parse the date.</span></span>

<a name="additional-resources"></a><span data-ttu-id="aecde-179">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="aecde-179">Additional resources</span></span>
--------

[<span data-ttu-id="aecde-180">倉庫作業用のモバイル デバイスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="aecde-180">Configuration of mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)





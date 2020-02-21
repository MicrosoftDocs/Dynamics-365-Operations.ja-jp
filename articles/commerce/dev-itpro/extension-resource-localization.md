---
title: コマース拡張リソースおよびラベル ファイルのローカライズ
description: このトピックでは、POS UI ラベル、POS メッセージ、入庫ラベル、および Commerce Scale Unit または CRT のエラー メッセージを変更する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7f0f60a3396751e15d167b890c1f3aac25e440de
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004573"
---
# <a name="localize-commerce-extension-resources-and-label-files"></a><span data-ttu-id="89479-103">コマース拡張リソースおよびラベル ファイルのローカライズ</span><span class="sxs-lookup"><span data-stu-id="89479-103">Localize Commerce extension resources and label files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="89479-104">このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Commerce Scale Unit または Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89479-104">This topic explains how to modify labels in the point of sale (POS) user interface (UI), POS messages (error, warning, and information), receipt labels, and error messages for Commerce Scale Unit or Commerce Runtime Services (CRT).</span></span> <span data-ttu-id="89479-105">カスタム エラー メッセージを同じ方法で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="89479-105">You can also add custom error messages for in the same way.</span></span> <span data-ttu-id="89479-106">ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="89479-106">However, for new POS extension labels, you should use the localization framework in the POS extension.</span></span>

## <a name="pos-labels-and-messages-error-warning-and-information"></a><span data-ttu-id="89479-107">POS ラベルおよびメッセージ (エラー、警告、および情報)</span><span class="sxs-lookup"><span data-stu-id="89479-107">POS labels and messages (error, warning, and information)</span></span>

<span data-ttu-id="89479-108">このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89479-108">This section explains how to modify POS UI labels and POS messages by overriding the default strings.</span></span>

### <a name="override-pos-ui-labels-and-messages"></a><span data-ttu-id="89479-109">POS UI ラベルおよびメッセージの上書き</span><span class="sxs-lookup"><span data-stu-id="89479-109">Override POS UI labels and messages</span></span>

<span data-ttu-id="89479-110">**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="89479-110">You can override the default strings in the POS by using the language text entries on the **Language text** page.</span></span> <span data-ttu-id="89479-111">POS 文字列を変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="89479-111">Follow these steps to change POS strings.</span></span>

1. <span data-ttu-id="89479-112">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="89479-112">Sign in to Commerce.</span></span>
2. <span data-ttu-id="89479-113">**Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="89479-113">Go to **Retail and Commerce &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Language text**.</span></span>
3. <span data-ttu-id="89479-114">**言語テキスト**ページの、**POS** タブの **POS 言語テキスト**グリッドで、**追加**ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="89479-114">On the **Language text** page, on the **POS** tab, in the **POS language text** grid, select the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="89479-115">たとえば、POS サインイン ページの**オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の**従業員 ID** に変更したいとします。</span><span class="sxs-lookup"><span data-stu-id="89479-115">For example, you want to change the label of the **Operator ID** field on the POS sign-in page to **Employee ID** for US English (en-us).</span></span> <span data-ttu-id="89479-116">この場合、**POS 言語テキスト**グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="89479-116">In this case, add the following entry in the **POS language text** grid.</span></span>

    | <span data-ttu-id="89479-117">言語 ID</span><span class="sxs-lookup"><span data-stu-id="89479-117">Language ID</span></span> | <span data-ttu-id="89479-118">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="89479-118">Text ID</span></span> | <span data-ttu-id="89479-119">テキスト</span><span class="sxs-lookup"><span data-stu-id="89479-119">Text</span></span>        |
    |-------------|---------|-------------|
    | <span data-ttu-id="89479-120">ja</span><span class="sxs-lookup"><span data-stu-id="89479-120">en-us</span></span>       | <span data-ttu-id="89479-121">502</span><span class="sxs-lookup"><span data-stu-id="89479-121">502</span></span>     | <span data-ttu-id="89479-122">従業員 ID</span><span class="sxs-lookup"><span data-stu-id="89479-122">Employee ID</span></span> |

    > [!NOTE]
    > <span data-ttu-id="89479-123">POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89479-123">For information about how to get the text ID for POS strings, see the next section.</span></span>

4. <span data-ttu-id="89479-124">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89479-124">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="89479-125">**Retail とコマース &gt; Retail とコマース IT &gt; 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="89479-125">Go to **Retail and Commerce &gt; Retail and Commerce IT &gt; Distribution schedule**.</span></span>
6. <span data-ttu-id="89479-126">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89479-126">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>
7. <span data-ttu-id="89479-127">データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="89479-127">After the data is pushed, sign off, and then sign in to Cloud POS or Modern POS to see the changed labels.</span></span>

### <a name="get-the-text-id-for-pos-strings"></a><span data-ttu-id="89479-128">POS 文字列のテキスト ID を取得します</span><span class="sxs-lookup"><span data-stu-id="89479-128">Get the text ID for POS strings</span></span>

<span data-ttu-id="89479-129">POS 文字列のテキスト ID を取得するには、デバッグ モードで Retail ソフトウェア開発キット (SDK) を使用して、POS を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89479-129">To get the text ID for a POS string, you must run the POS by using the Retail software development kit (SDK) in Debug mode.</span></span> <span data-ttu-id="89479-130">POS では、テキスト ID を文字列 ID と呼びます。</span><span class="sxs-lookup"><span data-stu-id="89479-130">In the POS, text IDs are referred to as string IDs.</span></span>

1. <span data-ttu-id="89479-131">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="89479-131">Start Microsoft Visual Studio 2015 in Administrator mode.</span></span>
2. <span data-ttu-id="89479-132">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="89479-132">Open **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="89479-133">**ソリューション構成**プロパティを**デバッグ**に、**ソリューション プラットフォーム**プロパティを **x86** に、および**配置**プロパティを**ローカル コンピューター**に設定します。</span><span class="sxs-lookup"><span data-stu-id="89479-133">Set the **Solution configuration** property to **Debug**, the **Solution platforms** property to **x86**, and the **Deploy** property to **Local machine**.</span></span>
4. <span data-ttu-id="89479-134">ソリューションをコンパイル、およびビルドしてから、**配置\>ローカル コンピューター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89479-134">Compile and build the solution, and then select **Deploy \> Local Machine**.</span></span>
5. <span data-ttu-id="89479-135">POS 配置後、オペレーター ID およびパスワードを使いログインします。</span><span class="sxs-lookup"><span data-stu-id="89479-135">After the POS is deployed, sign in to it by using your operator ID and password.</span></span>
6. <span data-ttu-id="89479-136">POS ウィンドウの右上で**設定**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="89479-136">Select the **Settings** button in the upper right of the POS window.</span></span>
7. <span data-ttu-id="89479-137">**設定**ページの**開発者モード**で、**開発者モード**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="89479-137">On the **Settings** page, under **Developer mode**, set the **Developer Mode** option to **Yes**.</span></span>
8. <span data-ttu-id="89479-138">**文字列 ID の表示**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="89479-138">Set the **Show Strings IDs** option to **Yes**.</span></span>
9. <span data-ttu-id="89479-139">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="89479-139">Sign out of the POS, and then sign in again.</span></span> <span data-ttu-id="89479-140">POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="89479-140">The POS now shows the strings IDs in front of all the labels and messages.</span></span> 

### <a name="troubleshooting"></a><span data-ttu-id="89479-141">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="89479-141">Troubleshooting</span></span>

<span data-ttu-id="89479-142">**開発者モード**オプションが POS の**設定**ページに表示されない場合は、デバッグ モードで動作していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="89479-142">If the **Developer Mode** option doesn't appear on the **Settings** page in the POS, verify that you're running in Debug mode.</span></span> <span data-ttu-id="89479-143">**pos.js** ファイルを開き、**Config.isDebugMode** が **true** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89479-143">Open the **pos.js** file, and verify that **Config.isDebugMode** is set to **true**.</span></span> <span data-ttu-id="89479-144">**false** に設定されている場合、値を **true** に変更し、再度 POS を配置します。</span><span class="sxs-lookup"><span data-stu-id="89479-144">If it's set to **false**, change the value to **true**, and then deploy the POS again.</span></span> <span data-ttu-id="89479-145">**pos.js** ファイル内で **Config.isDebugMode** が見つからない場合。</span><span class="sxs-lookup"><span data-stu-id="89479-145">If you are unable to find **Config.isDebugMode** in the **pos.js** file.</span></span> <span data-ttu-id="89479-146">JavaScript コンソールで **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** コマンドを実行して、開発者モードを起動します。</span><span class="sxs-lookup"><span data-stu-id="89479-146">then run the **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** command in the JavaScript console to turn on the developer mode.</span></span> <span data-ttu-id="89479-147">F12 を押下して 開発者コマンドツールを起動し、 **コンソール** タブを選択して JavaScript コンソールを開きます。</span><span class="sxs-lookup"><span data-stu-id="89479-147">Press F12 to launch the developer command tools and select the **Console** tab to open the JavaScript console.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89479-148">クイック テストを行い、文字列 ID を取得するために、pos.js ファイル**のみ**を編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89479-148">You should edit the pos.js file **only** to do quick testing and to get string IDs.</span></span> <span data-ttu-id="89479-149">そのような場合、ファイルを編集した後に、変更内容を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="89479-149">In these cases, after you edit the file, you should revert your changes.</span></span> <span data-ttu-id="89479-150">Microsoft のコア ファイルに加えた変更は展開中に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="89479-150">Any changes that you make in Microsoft cores files will be overridden during deployment.</span></span> <span data-ttu-id="89479-151">そのため、変更は失われます。</span><span class="sxs-lookup"><span data-stu-id="89479-151">Therefore, you will lose the changes.</span></span> <span data-ttu-id="89479-152">また、将来のバージョンでは、pos.js ファイルの編集をサポートしない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="89479-152">Additionally, future versions might not support editing the pos.js file.</span></span>

## <a name="error-messages-or-receipt-strings"></a><span data-ttu-id="89479-153">エラー メッセージまたは入庫文字列</span><span class="sxs-lookup"><span data-stu-id="89479-153">Error messages or receipt strings</span></span>

<span data-ttu-id="89479-154">このセクションでは、既定の文字列を上書きすることによってエラー メッセージ、または入庫文字列を変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89479-154">This section explains how to modify error messages, or receipt strings, by overriding the default strings.</span></span> <span data-ttu-id="89479-155">新規、カスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="89479-155">It also explains how you can add new, custom error messages, or receipt strings.</span></span>

### <a name="override-error-messages-or-receipt-strings"></a><span data-ttu-id="89479-156">エラー メッセージまたは入庫文字列を上書きする</span><span class="sxs-lookup"><span data-stu-id="89479-156">Override error messages or receipt strings</span></span>

1. <span data-ttu-id="89479-157">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="89479-157">Sign in to Commerce.</span></span>
2. <span data-ttu-id="89479-158">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="89479-158">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Language text**.</span></span>
3. <span data-ttu-id="89479-159">**言語テキスト** ページで、**追加**ボタンをクリックして、上書きする文字列の言語 ID、テキスト ID、およびテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="89479-159">On the **Language text** page, click the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="89479-160">たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」</span><span class="sxs-lookup"><span data-stu-id="89479-160">For example, when users enter an incorrect user name or password during sign-in, the POS shows the following error message: "We didn't recognize the user name or password.</span></span> <span data-ttu-id="89479-161">もう一度やり直してください。」</span><span class="sxs-lookup"><span data-stu-id="89479-161">Please try again."</span></span> <span data-ttu-id="89479-162">英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。</span><span class="sxs-lookup"><span data-stu-id="89479-162">For US English, you want to change the message to "Please enter valid user name or password."</span></span> <span data-ttu-id="89479-163">この場合、**言語テキスト** グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="89479-163">In this case, add the following entry in the **language text** grid.</span></span>

    | <span data-ttu-id="89479-164">言語 ID</span><span class="sxs-lookup"><span data-stu-id="89479-164">Language ID</span></span> | <span data-ttu-id="89479-165">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="89479-165">Text ID</span></span>                                                              | <span data-ttu-id="89479-166">テキスト</span><span class="sxs-lookup"><span data-stu-id="89479-166">Text</span></span>                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | <span data-ttu-id="89479-167">ja</span><span class="sxs-lookup"><span data-stu-id="89479-167">en-us</span></span>       | <span data-ttu-id="89479-168">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span><span class="sxs-lookup"><span data-stu-id="89479-168">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span></span> | <span data-ttu-id="89479-169">有効なユーザー名またはパスワードを入力してください</span><span class="sxs-lookup"><span data-stu-id="89479-169">Please enter valid user name or password</span></span> |

    > [!NOTE]
    > <span data-ttu-id="89479-170">エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89479-170">For information about how to get the text ID for error messages and receipt strings, see the next section.</span></span>

4. <span data-ttu-id="89479-171">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89479-171">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="89479-172">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="89479-172">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
6. <span data-ttu-id="89479-173">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="89479-173">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

### <a name="get-the-text-id-for-messages-or-receipt-strings"></a><span data-ttu-id="89479-174">メッセージまたは入庫文字列のテキスト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="89479-174">Get the text ID for messages or receipt strings</span></span>

1. <span data-ttu-id="89479-175">**…\\RetailSDK\\ドキュメント\\リソース**に移動します。</span><span class="sxs-lookup"><span data-stu-id="89479-175">Go to **…\\RetailSDK\\Documents\\Resources**.</span></span>
2. <span data-ttu-id="89479-176">Visual Studio で、次のリソース ファイルのいずれかを開きます。</span><span class="sxs-lookup"><span data-stu-id="89479-176">In Visual Studio, open one of the following resource files:</span></span>

    - <span data-ttu-id="89479-177">**エラー メッセージを変更するには:** RuntimeExceptionMessages.resx</span><span class="sxs-lookup"><span data-stu-id="89479-177">**To modify error messages:** RuntimeExceptionMessages.resx</span></span>
    - <span data-ttu-id="89479-178">**入力された文字列の変更:** RuntimeReceiptMessages.resx</span><span class="sxs-lookup"><span data-stu-id="89479-178">**To modify receipt strings:** RuntimeReceiptMessages.resx</span></span>

    <span data-ttu-id="89479-179">リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。</span><span class="sxs-lookup"><span data-stu-id="89479-179">For every message in the resource file, Visual Studio shows a name and a value.</span></span>

3. <span data-ttu-id="89479-180">**値**列で、変更するテキストを検索します。</span><span class="sxs-lookup"><span data-stu-id="89479-180">In the **Value** column, search for the text that you want to change.</span></span>
4. <span data-ttu-id="89479-181">その値に対応する名前をコピーします。</span><span class="sxs-lookup"><span data-stu-id="89479-181">Copy the name that corresponds to that value.</span></span> <span data-ttu-id="89479-182">この名前をテキスト ID として**言語テキスト** グリッドに入力します。</span><span class="sxs-lookup"><span data-stu-id="89479-182">You enter this name as the text ID in the **language text** grid.</span></span>

### <a name="add-custom-error-messages-or-receipt-strings"></a><span data-ttu-id="89479-183">カスタム エラー メッセージまたは入庫文字列を追加する</span><span class="sxs-lookup"><span data-stu-id="89479-183">Add custom error messages or receipt strings</span></span>

<span data-ttu-id="89479-184">新しいエラー メッセージまたは新しい入庫文字列を、**言語テキスト** ページで追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="89479-184">You can also add new error messages or new receipt strings, on the **Language text** page.</span></span> <span data-ttu-id="89479-185">この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。</span><span class="sxs-lookup"><span data-stu-id="89479-185">In this way, you support localization instead of hard-coding everything in the code.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89479-186">すべてのメッセージのテキスト ID は **Microsoft\_Dynamics\_Commerce\_** から始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="89479-186">The text ID of all your new messages must start with **Microsoft\_Dynamics\_Commerce\_**.</span></span>

<span data-ttu-id="89479-187">たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。</span><span class="sxs-lookup"><span data-stu-id="89479-187">For example, you want to add a new exception message in US English (en-us) and UK English (en-uk).</span></span> <span data-ttu-id="89479-188">この場合、**言語テキスト** ページでの次のエントリに類似したエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="89479-188">In this case, add entries that resemble the follow entries on the **Language text** page.</span></span>

| <span data-ttu-id="89479-189">言語 ID</span><span class="sxs-lookup"><span data-stu-id="89479-189">Language ID</span></span> | <span data-ttu-id="89479-190">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="89479-190">Text ID</span></span>                                 | <span data-ttu-id="89479-191">テキスト</span><span class="sxs-lookup"><span data-stu-id="89479-191">Text</span></span>                    |
|-------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="89479-192">ja</span><span class="sxs-lookup"><span data-stu-id="89479-192">en-us</span></span>       | <span data-ttu-id="89479-193">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="89479-193">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="89479-194">アメリカ英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="89479-194">My new message in US English</span></span> |
| <span data-ttu-id="89479-195">en-uk</span><span class="sxs-lookup"><span data-stu-id="89479-195">en-uk</span></span>       | <span data-ttu-id="89479-196">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="89479-196">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="89479-197">英国英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="89479-197">My new message in UK English</span></span> |

> [!NOTE]
> <span data-ttu-id="89479-198">この例では、**CustomId1** が新しいメッセージのテキスト ID です。</span><span class="sxs-lookup"><span data-stu-id="89479-198">In this example, **CustomId1** is the text ID for the new message.</span></span> <span data-ttu-id="89479-199">使用したい任意のテキスト ID を使用することができます。ただし、**Microsoft_Dynamics_Commerce_** で始まる場合に限ります</span><span class="sxs-lookup"><span data-stu-id="89479-199">You can use any text ID that you want, provided that it starts with **Microsoft_Dynamics_Commerce_**.</span></span>

<span data-ttu-id="89479-200">次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="89479-200">The following example shows how to use this new message in your CRT extension code.</span></span>

```C#
throw new CommerceException("Microsoft_Dynamics_Commerce_CustomId1", ExceptionSeverity.Warning, null, "Custom error")
                    {
                        LocalizedMessage = "My new message in US English.",
                        LocalizedMessageParameters = new object[] { }
                    };
```

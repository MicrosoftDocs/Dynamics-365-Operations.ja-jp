---
title: Retail 拡張リソースおよびラベル ファイルのローカライズ
description: このトピックでは、POS UI ラベル、POS メッセージ、入庫ラベル、および Retail サーバーまたは CRT のエラー メッセージを変更する方法について説明します。 Retail サーバーまたは CRT のカスタム エラー メッセージを追加する方法についても説明します。
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
ms.openlocfilehash: 2aa401a1ce7821840375c7d583365cddc978df63
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934922"
---
# <a name="localize-retail-extension-resources-and-label-files"></a><span data-ttu-id="6d99d-104">Retail 拡張リソースおよびラベル ファイルのローカライズ</span><span class="sxs-lookup"><span data-stu-id="6d99d-104">Localize Retail extension resources and label files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6d99d-105">このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Retail サーバーまたは Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-105">This topic explains how to modify labels in the point of sale (POS) user interface (UI), POS messages (error, warning, and information), receipt labels, and error messages for Retail server or Commerce Runtime Services (CRT).</span></span> <span data-ttu-id="6d99d-106">Retail サーバーまたは CRT のカスタム エラー メッセージを、同じ方法で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-106">You can also add custom error messages for Retail server or CRT in the same way.</span></span> <span data-ttu-id="6d99d-107">ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-107">However, for new POS extension labels, you should use the localization framework in the POS extension.</span></span>



## <a name="retail-pos-labels-and-messages-error-warning-and-information"></a><span data-ttu-id="6d99d-108">Retail POS ラベルおよびメッセージ (エラー、警告、および情報)</span><span class="sxs-lookup"><span data-stu-id="6d99d-108">Retail POS labels and messages (error, warning, and information)</span></span>

<span data-ttu-id="6d99d-109">このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-109">This section explains how to modify POS UI labels and POS messages by overriding the default strings.</span></span>

### <a name="override-pos-ui-labels-and-messages"></a><span data-ttu-id="6d99d-110">POS UI ラベルおよびメッセージの上書き</span><span class="sxs-lookup"><span data-stu-id="6d99d-110">Override POS UI labels and messages</span></span>

<span data-ttu-id="6d99d-111">**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-111">You can override the default strings in the POS by using the language text entries on the **Language text** page.</span></span> <span data-ttu-id="6d99d-112">POS 文字列を変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-112">Follow these steps to change POS strings.</span></span>

1. <span data-ttu-id="6d99d-113">Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-113">Sign in to Retail.</span></span>
2. <span data-ttu-id="6d99d-114">**小売 &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-114">Go to **Retail &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Language text**.</span></span>
3. <span data-ttu-id="6d99d-115">**言語テキスト**ページの、**POS** タブの **POS 言語テキスト**グリッドで、**追加**ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-115">On the **Language text** page, on the **POS** tab, in the **POS language text** grid, select the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="6d99d-116">たとえば、POS サインイン ページの**オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の**従業員 ID** に変更したいとします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-116">For example, you want to change the label of the **Operator ID** field on the POS sign-in page to **Employee ID** for US English (en-us).</span></span> <span data-ttu-id="6d99d-117">この場合、**POS 言語テキスト**グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-117">In this case, add the following entry in the **POS language text** grid.</span></span>

    | <span data-ttu-id="6d99d-118">言語 ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-118">Language ID</span></span> | <span data-ttu-id="6d99d-119">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-119">Text ID</span></span> | <span data-ttu-id="6d99d-120">テキスト</span><span class="sxs-lookup"><span data-stu-id="6d99d-120">Text</span></span>        |
    |-------------|---------|-------------|
    | <span data-ttu-id="6d99d-121">ja</span><span class="sxs-lookup"><span data-stu-id="6d99d-121">en-us</span></span>       | <span data-ttu-id="6d99d-122">502</span><span class="sxs-lookup"><span data-stu-id="6d99d-122">502</span></span>     | <span data-ttu-id="6d99d-123">従業員 ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-123">Employee ID</span></span> |

    > [!NOTE]
    > <span data-ttu-id="6d99d-124">POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d99d-124">For information about how to get the text ID for POS strings, see the next section.</span></span>

4. <span data-ttu-id="6d99d-125">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-125">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="6d99d-126">**小売 &gt; 小売 IT &gt; 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-126">Go to **Retail &gt; Retail IT &gt; Distribution schedule**.</span></span>
6. <span data-ttu-id="6d99d-127">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-127">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>
7. <span data-ttu-id="6d99d-128">データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-128">After the data is pushed, sign off, and then sign in to Cloud POS or Modern POS to see the changed labels.</span></span>

### <a name="get-the-text-id-for-pos-strings"></a><span data-ttu-id="6d99d-129">POS 文字列のテキスト ID を取得します</span><span class="sxs-lookup"><span data-stu-id="6d99d-129">Get the text ID for POS strings</span></span>

<span data-ttu-id="6d99d-130">POS 文字列のテキスト ID を取得するには、デバッグ モードで Retail ソフトウェア開発キット (SDK) を使用して、POS を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d99d-130">To get the text ID for a POS string, you must run the POS by using the Retail software development kit (SDK) in Debug mode.</span></span> <span data-ttu-id="6d99d-131">POS では、テキスト ID を文字列 ID と呼びます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-131">In the POS, text IDs are referred to as string IDs.</span></span>

1. <span data-ttu-id="6d99d-132">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-132">Start Microsoft Visual Studio 2015 in Administrator mode.</span></span>
2. <span data-ttu-id="6d99d-133">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-133">Open **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="6d99d-134">**ソリューション構成**プロパティを**デバッグ**に、**ソリューション プラットフォーム**プロパティを **x86** に、および**配置**プロパティを**ローカル コンピューター**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-134">Set the **Solution configuration** property to **Debug**, the **Solution platforms** property to **x86**, and the **Deploy** property to **Local machine**.</span></span>
4. <span data-ttu-id="6d99d-135">ソリューションをコンパイル、およびビルドしてから、**配置\>ローカル コンピューター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-135">Compile and build the solution, and then select **Deploy \> Local Machine**.</span></span>
5. <span data-ttu-id="6d99d-136">POS 配置後、オペレーター ID およびパスワードを使いログインします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-136">After the POS is deployed, sign in to it by using your operator ID and password.</span></span>
6. <span data-ttu-id="6d99d-137">POS ウィンドウの右上で**設定**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-137">Select the **Settings** button in the upper right of the POS window.</span></span>
7. <span data-ttu-id="6d99d-138">**設定**ページの**開発者モード**で、**開発者モード**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-138">On the **Settings** page, under **Developer mode**, set the **Developer Mode** option to **Yes**.</span></span>
8. <span data-ttu-id="6d99d-139">**文字列 ID の表示**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-139">Set the **Show Strings IDs** option to **Yes**.</span></span>
9. <span data-ttu-id="6d99d-140">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-140">Sign out of the POS, and then sign in again.</span></span> <span data-ttu-id="6d99d-141">POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="6d99d-141">The POS now shows the strings IDs in front of all the labels and messages.</span></span> 

### <a name="troubleshooting"></a><span data-ttu-id="6d99d-142">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="6d99d-142">Troubleshooting</span></span>

<span data-ttu-id="6d99d-143">**開発者モード**オプションが POS の**設定**ページに表示されない場合は、デバッグ モードで動作していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6d99d-143">If the **Developer Mode** option doesn't appear on the **Settings** page in the POS, verify that you're running in Debug mode.</span></span> <span data-ttu-id="6d99d-144">**pos.js** ファイルを開き、**Config.isDebugMode** が **true** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-144">Open the **pos.js** file, and verify that **Config.isDebugMode** is set to **true**.</span></span> <span data-ttu-id="6d99d-145">**false** に設定されている場合、値を **true** に変更し、再度 POS を配置します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-145">If it's set to **false**, change the value to **true**, and then deploy the POS again.</span></span> <span data-ttu-id="6d99d-146">**pos.js** ファイル内で **Config.isDebugMode** が見つからない場合。</span><span class="sxs-lookup"><span data-stu-id="6d99d-146">If you are unable to find **Config.isDebugMode** in the **pos.js** file.</span></span> <span data-ttu-id="6d99d-147">JavaScript コンソールで **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** コマンドを実行して、開発者モードを起動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-147">then run the **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** command in the JavaScript console to turn on the developer mode.</span></span> <span data-ttu-id="6d99d-148">F12 を押下して 開発者コマンドツールを起動し、 **コンソール** タブを選択して JavaScript コンソールを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-148">Press F12 to launch the developer command tools and select the **Console** tab to open the JavaScript console.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d99d-149">クイック テストを行い、文字列 ID を取得するために、pos.js ファイル**のみ**を編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d99d-149">You should edit the pos.js file **only** to do quick testing and to get string IDs.</span></span> <span data-ttu-id="6d99d-150">そのような場合、ファイルを編集した後に、変更内容を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d99d-150">In these cases, after you edit the file, you should revert your changes.</span></span> <span data-ttu-id="6d99d-151">Microsoft のコア ファイルに加えた変更は展開中に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-151">Any changes that you make in Microsoft cores files will be overridden during deployment.</span></span> <span data-ttu-id="6d99d-152">そのため、変更は失われます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-152">Therefore, you will lose the changes.</span></span> <span data-ttu-id="6d99d-153">また、将来のバージョンでは、pos.js ファイルの編集をサポートしない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6d99d-153">Additionally, future versions might not support editing the pos.js file.</span></span>

## <a name="retail-server-or-crt-error-messages-or-receipt-strings"></a><span data-ttu-id="6d99d-154">Retail サーバーや CRT エラー メッセージ、または入庫文字列</span><span class="sxs-lookup"><span data-stu-id="6d99d-154">Retail server or CRT error messages, or receipt strings</span></span>

<span data-ttu-id="6d99d-155">このセクションでは、既定の文字列を上書きすることによって Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-155">This section explains how to modify Retail server or CRT error messages, or receipt strings, by overriding the default strings.</span></span> <span data-ttu-id="6d99d-156">新規、Retail サーバーまたは CRT のカスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-156">It also explains how you can add new, custom Retail server or CRT error messages, or receipt strings.</span></span>

### <a name="override-retail-server-or-crt-error-messages-or-receipt-strings"></a><span data-ttu-id="6d99d-157">Retail サーバーや CRT エラー メッセージ、または入庫文字列を上書き</span><span class="sxs-lookup"><span data-stu-id="6d99d-157">Override Retail server or CRT error messages, or receipt strings</span></span>

1. <span data-ttu-id="6d99d-158">Retail へサインインします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-158">Sign in to Retail.</span></span>
2. <span data-ttu-id="6d99d-159">**小売 \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-159">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Language text**.</span></span>
3. <span data-ttu-id="6d99d-160">**言語テキスト**ページの、**Retail サーバー**タブの **Retail サーバー言語テキスト**グリッドで、**追加**ボタンをクリックして言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-160">On the **Language text** page, on the **Retail server** tab, in the **Retail server language text** grid, click the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="6d99d-161">たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」</span><span class="sxs-lookup"><span data-stu-id="6d99d-161">For example, when users enter an incorrect user name or password during sign-in, the POS shows the following error message: "We didn't recognize the user name or password.</span></span> <span data-ttu-id="6d99d-162">もう一度やり直してください。」</span><span class="sxs-lookup"><span data-stu-id="6d99d-162">Please try again."</span></span> <span data-ttu-id="6d99d-163">英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-163">For US English, you want to change the message to "Please enter valid user name or password."</span></span> <span data-ttu-id="6d99d-164">この場合、**Retail サーバー 言語テキスト**グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-164">In this case, add the following entry in the **Retail server language text** grid.</span></span>

    | <span data-ttu-id="6d99d-165">言語 ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-165">Language ID</span></span> | <span data-ttu-id="6d99d-166">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-166">Text ID</span></span>                                                              | <span data-ttu-id="6d99d-167">テキスト</span><span class="sxs-lookup"><span data-stu-id="6d99d-167">Text</span></span>                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | <span data-ttu-id="6d99d-168">ja</span><span class="sxs-lookup"><span data-stu-id="6d99d-168">en-us</span></span>       | <span data-ttu-id="6d99d-169">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span><span class="sxs-lookup"><span data-stu-id="6d99d-169">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span></span> | <span data-ttu-id="6d99d-170">有効なユーザー名またはパスワードを入力してください</span><span class="sxs-lookup"><span data-stu-id="6d99d-170">Please enter valid user name or password</span></span> |

    > [!NOTE]
    > <span data-ttu-id="6d99d-171">Retail サーバーまたは CRT エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6d99d-171">For information about how to get the text ID for Retail server or CRT error messages, and receipt strings, see the next section.</span></span>

4. <span data-ttu-id="6d99d-172">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-172">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="6d99d-173">**小売 \> 小売 IT \> 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-173">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
6. <span data-ttu-id="6d99d-174">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-174">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

### <a name="get-the-text-id-for-retail-server-or-crt-messages-or-receipt-strings"></a><span data-ttu-id="6d99d-175">Retail サーバーまたは CRT メッセージ、または入庫文字列のためのテキスト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-175">Get the text ID for Retail server or CRT messages, or receipt strings</span></span>

1. <span data-ttu-id="6d99d-176">**…\\RetailSDK\\ドキュメント\\リソース**に移動します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-176">Go to **…\\RetailSDK\\Documents\\Resources**.</span></span>
2. <span data-ttu-id="6d99d-177">Visual Studio で、次のリソース ファイルのいずれかを開きます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-177">In Visual Studio, open one of the following resource files:</span></span>

    - <span data-ttu-id="6d99d-178">**Retail server または CRT エラー メッセージを変更する:** RuntimeExceptionMessages.resx</span><span class="sxs-lookup"><span data-stu-id="6d99d-178">**To modify Retail server or CRT error messages:** RuntimeExceptionMessages.resx</span></span>
    - <span data-ttu-id="6d99d-179">**入力された文字列の変更:** RuntimeReceiptMessages.resx</span><span class="sxs-lookup"><span data-stu-id="6d99d-179">**To modify receipt strings:** RuntimeReceiptMessages.resx</span></span>

    <span data-ttu-id="6d99d-180">リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-180">For every message in the resource file, Visual Studio shows a name and a value.</span></span>

3. <span data-ttu-id="6d99d-181">**値**列で、変更するテキストを検索します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-181">In the **Value** column, search for the text that you want to change.</span></span>
4. <span data-ttu-id="6d99d-182">その値に対応する名前をコピーします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-182">Copy the name that corresponds to that value.</span></span> <span data-ttu-id="6d99d-183">この名前をテキストID として **Retail サーバー言語テキスト** グリッドに入力します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-183">You enter this name as the text ID in the **Retail server language text** grid.</span></span>

### <a name="add-custom-retail-server-or-crt-error-messages-or-receipt-strings"></a><span data-ttu-id="6d99d-184">カスタム Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を追加</span><span class="sxs-lookup"><span data-stu-id="6d99d-184">Add custom Retail server or CRT error messages, or receipt strings</span></span>

<span data-ttu-id="6d99d-185">新しい Retail サーバーまたは CRT エラー メッセージ、または、新しい入庫文字列を **Retail サーバー言語テキスト** グリッドに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="6d99d-185">You can also add new Retail server or CRT error messages, or new receipt strings, in the **Retail server language text** grid.</span></span> <span data-ttu-id="6d99d-186">この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-186">In this way, you support localization instead of hard-coding everything in the code.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d99d-187">すべてのメッセージのテキスト ID は **Microsoft\_Dynamics\_Commerce\_** から始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d99d-187">The text ID of all your new messages must start with **Microsoft\_Dynamics\_Commerce\_**.</span></span>

<span data-ttu-id="6d99d-188">たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。</span><span class="sxs-lookup"><span data-stu-id="6d99d-188">For example, you want to add a new exception message in US English (en-us) and UK English (en-uk).</span></span> <span data-ttu-id="6d99d-189">この場合、**Retail サーバー言語テキスト**グリッドでの次のエントリに類似したエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-189">In this case, add entries that resemble the follow entries in the **Retail server language text** grid.</span></span>

| <span data-ttu-id="6d99d-190">言語 ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-190">Language ID</span></span> | <span data-ttu-id="6d99d-191">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="6d99d-191">Text ID</span></span>                                 | <span data-ttu-id="6d99d-192">テキスト</span><span class="sxs-lookup"><span data-stu-id="6d99d-192">Text</span></span>                    |
|-------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="6d99d-193">ja</span><span class="sxs-lookup"><span data-stu-id="6d99d-193">en-us</span></span>       | <span data-ttu-id="6d99d-194">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="6d99d-194">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="6d99d-195">アメリカ英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="6d99d-195">My new message in US English</span></span> |
| <span data-ttu-id="6d99d-196">en-uk</span><span class="sxs-lookup"><span data-stu-id="6d99d-196">en-uk</span></span>       | <span data-ttu-id="6d99d-197">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="6d99d-197">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="6d99d-198">英国英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="6d99d-198">My new message in UK English</span></span> |

> [!NOTE]
> <span data-ttu-id="6d99d-199">この例では、**CustomId1** が新しいメッセージのテキスト ID です。</span><span class="sxs-lookup"><span data-stu-id="6d99d-199">In this example, **CustomId1** is the text ID for the new message.</span></span> <span data-ttu-id="6d99d-200">使用したい任意のテキスト ID を使用することができます。ただし、**Microsoft_Dynamics_Commerce_** で始まる場合に限ります</span><span class="sxs-lookup"><span data-stu-id="6d99d-200">You can use any text ID that you want, provided that it starts with **Microsoft_Dynamics_Commerce_**.</span></span>

<span data-ttu-id="6d99d-201">次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6d99d-201">The following example shows how to use this new message in your CRT extension code.</span></span>

```C#
throw new CommerceException("Microsoft_Dynamics_Commerce_CustomId1", ExceptionSeverity.Warning, null, "Custom error")
                    {
                        LocalizedMessage = "My new message in US English.",
                        LocalizedMessageParameters = new object[] { }
                    };
```

---
title: Retail 拡張リソースおよびラベル ファイルのローカライズ
description: このトピックでは、POS UI ラベル、POS メッセージ、入庫ラベル、および Retail サーバーまたは CRT のエラー メッセージを変更する方法について説明します。 Retail サーバーまたは CRT のカスタム エラー メッセージを追加する方法についても説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: margoc
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 116cd847aa50eec7edbe13e7f51ed89cec290e72
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569276"
---
# <a name="localize-retail-extension-resources-and-label-files"></a><span data-ttu-id="305f4-104">Retail 拡張リソースおよびラベル ファイルのローカライズ</span><span class="sxs-lookup"><span data-stu-id="305f4-104">Localize Retail extension resources and label files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="305f4-105">このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Retail サーバーまたは Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="305f4-105">This topic explains how to modify labels in the point of sale (POS) user interface (UI), POS messages (error, warning, and information), receipt labels, and error messages for Retail server or Commerce Runtime Services (CRT).</span></span> <span data-ttu-id="305f4-106">Retail サーバーまたは CRT のカスタム エラー メッセージを、同じ方法で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="305f4-106">You can also add custom error messages for Retail server or CRT in the same way.</span></span> <span data-ttu-id="305f4-107">ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="305f4-107">However, for new POS extension labels, you should use the localization framework in the POS extension.</span></span>

<span data-ttu-id="305f4-108">このトピックは、 最新の更新プログラムが適用された Microsoft Dynamics 365 for Finance and Operations 7.2、最新の更新プログラムが適用された Microsoft Dynamics 365 for Retail 7.2 とそれ以降のバージョンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="305f4-108">This topic is applicable to Microsoft Dynamics 365 for Finance and Operations 7.2 with the latest update, Microsoft Dynamics 365 for Retail 7.2 with the latest update, and to later versions.</span></span>

## <a name="retail-pos-labels-and-messages-error-warning-and-information"></a><span data-ttu-id="305f4-109">Retail POS ラベルおよびメッセージ (エラー、警告、および情報)</span><span class="sxs-lookup"><span data-stu-id="305f4-109">Retail POS labels and messages (error, warning, and information)</span></span>

<span data-ttu-id="305f4-110">このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="305f4-110">This section explains how to modify POS UI labels and POS messages by overriding the default strings.</span></span>

### <a name="override-pos-ui-labels-and-messages"></a><span data-ttu-id="305f4-111">POS UI ラベルおよびメッセージの上書き</span><span class="sxs-lookup"><span data-stu-id="305f4-111">Override POS UI labels and messages</span></span>

<span data-ttu-id="305f4-112">**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="305f4-112">You can override the default strings in the POS by using the language text entries on the **Language text** page.</span></span> <span data-ttu-id="305f4-113">POS 文字列を変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="305f4-113">Follow these steps to change POS strings.</span></span>

1. <span data-ttu-id="305f4-114">Retail または Finance and Operations へのサインイン</span><span class="sxs-lookup"><span data-stu-id="305f4-114">Sign in to Retail or Finance and Operations.</span></span>
2. <span data-ttu-id="305f4-115">**小売 &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="305f4-115">Go to **Retail &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Language text**.</span></span>
3. <span data-ttu-id="305f4-116">**言語テキスト**ページの、**POS** タブの **POS 言語テキスト**グリッドで、**追加**ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="305f4-116">On the **Language text** page, on the **POS** tab, in the **POS language text** grid, select the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="305f4-117">たとえば、POS サインイン ページの**オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の**従業員 ID** に変更したいとします。</span><span class="sxs-lookup"><span data-stu-id="305f4-117">For example, you want to change the label of the **Operator ID** field on the POS sign-in page to **Employee ID** for US English (en-us).</span></span> <span data-ttu-id="305f4-118">この場合、**POS 言語テキスト**グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="305f4-118">In this case, add the following entry in the **POS language text** grid.</span></span>

    | <span data-ttu-id="305f4-119">言語 ID</span><span class="sxs-lookup"><span data-stu-id="305f4-119">Language ID</span></span> | <span data-ttu-id="305f4-120">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="305f4-120">Text ID</span></span> | <span data-ttu-id="305f4-121">テキスト</span><span class="sxs-lookup"><span data-stu-id="305f4-121">Text</span></span>        |
    |-------------|---------|-------------|
    | <span data-ttu-id="305f4-122">ja</span><span class="sxs-lookup"><span data-stu-id="305f4-122">en-us</span></span>       | <span data-ttu-id="305f4-123">502</span><span class="sxs-lookup"><span data-stu-id="305f4-123">502</span></span>     | <span data-ttu-id="305f4-124">従業員 ID</span><span class="sxs-lookup"><span data-stu-id="305f4-124">Employee ID</span></span> |

    > [!NOTE]
    > <span data-ttu-id="305f4-125">POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="305f4-125">For information about how to get the text ID for POS strings, see the next section.</span></span>

4. <span data-ttu-id="305f4-126">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="305f4-126">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="305f4-127">**小売 &gt; 小売 IT &gt; 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="305f4-127">Go to **Retail &gt; Retail IT &gt; Distribution schedule**.</span></span>
6. <span data-ttu-id="305f4-128">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="305f4-128">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>
7. <span data-ttu-id="305f4-129">データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="305f4-129">After the data is pushed, sign off, and then sign in to Cloud POS or Modern POS to see the changed labels.</span></span>

### <a name="get-the-text-id-for-pos-strings"></a><span data-ttu-id="305f4-130">POS 文字列のテキスト ID を取得します</span><span class="sxs-lookup"><span data-stu-id="305f4-130">Get the text ID for POS strings</span></span>

<span data-ttu-id="305f4-131">POS 文字列のテキスト ID を取得するには、デバッグ モードで Retail ソフトウェア開発キット (SDK) を使用して、POS を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="305f4-131">To get the text ID for a POS string, you must run the POS by using the Retail software development kit (SDK) in Debug mode.</span></span> <span data-ttu-id="305f4-132">POS では、テキスト ID を文字列 ID と呼びます。</span><span class="sxs-lookup"><span data-stu-id="305f4-132">In the POS, text IDs are referred to as string IDs.</span></span>

1. <span data-ttu-id="305f4-133">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="305f4-133">Start Microsoft Visual Studio 2015 in Administrator mode.</span></span>
2. <span data-ttu-id="305f4-134">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="305f4-134">Open **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="305f4-135">**ソリューション構成**プロパティを**デバッグ**に、**ソリューション プラットフォーム**プロパティを **x86** に、および**配置**プロパティを**ローカル コンピューター**に設定します。</span><span class="sxs-lookup"><span data-stu-id="305f4-135">Set the **Solution configuration** property to **Debug**, the **Solution platforms** property to **x86**, and the **Deploy** property to **Local machine**.</span></span>
4. <span data-ttu-id="305f4-136">ソリューションをコンパイル、およびビルドしてから、**配置\>ローカル コンピューター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="305f4-136">Compile and build the solution, and then select **Deploy \> Local Machine**.</span></span>
5. <span data-ttu-id="305f4-137">POS 配置後、オペレーター ID およびパスワードを使いログインします。</span><span class="sxs-lookup"><span data-stu-id="305f4-137">After the POS is deployed, sign in to it by using your operator ID and password.</span></span>
6. <span data-ttu-id="305f4-138">POS ウィンドウの右上で**設定**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="305f4-138">Select the **Settings** button in the upper right of the POS window.</span></span>
7. <span data-ttu-id="305f4-139">**設定**ページの**開発者モード**で、**開発者モード**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="305f4-139">On the **Settings** page, under **Developer mode**, set the **Developer Mode** option to **Yes**.</span></span>
8. <span data-ttu-id="305f4-140">**文字列 ID の表示**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="305f4-140">Set the **Show Strings IDs** option to **Yes**.</span></span>
9. <span data-ttu-id="305f4-141">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="305f4-141">Sign out of the POS, and then sign in again.</span></span> <span data-ttu-id="305f4-142">POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="305f4-142">The POS now shows the strings IDs in front of all the labels and messages.</span></span> 

### <a name="troubleshooting"></a><span data-ttu-id="305f4-143">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="305f4-143">Troubleshooting</span></span>

<span data-ttu-id="305f4-144">**開発者モード**オプションが POS の**設定**ページに表示されない場合は、デバッグ モードで動作していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="305f4-144">If the **Developer Mode** option doesn't appear on the **Settings** page in the POS, verify that you're running in Debug mode.</span></span> <span data-ttu-id="305f4-145">**pos.js** ファイルを開き、**Config.isDebugMode** が **true** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="305f4-145">Open the **pos.js** file, and verify that **Config.isDebugMode** is set to **true**.</span></span> <span data-ttu-id="305f4-146">**false** に設定されている場合、値を **true** に変更し、再度 POS を配置します。</span><span class="sxs-lookup"><span data-stu-id="305f4-146">If it's set to **false**, change the value to **true**, and then deploy the POS again.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="305f4-147">クイック テストを行い、文字列 ID を取得するために、pos.js ファイル**のみ**を編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="305f4-147">You should edit the pos.js file **only** to do quick testing and to get string IDs.</span></span> <span data-ttu-id="305f4-148">そのような場合、ファイルを編集した後に、変更内容を元に戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="305f4-148">In these cases, after you edit the file, you should revert your changes.</span></span> <span data-ttu-id="305f4-149">Microsoft のコア ファイルに加えた変更は展開中に上書きされます。</span><span class="sxs-lookup"><span data-stu-id="305f4-149">Any changes that you make in Microsoft cores files will be overridden during deployment.</span></span> <span data-ttu-id="305f4-150">そのため、変更は失われます。</span><span class="sxs-lookup"><span data-stu-id="305f4-150">Therefore, you will lose the changes.</span></span> <span data-ttu-id="305f4-151">また、将来のバージョンでは、pos.js ファイルの編集をサポートしない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="305f4-151">Additionally, future versions might not support editing the pos.js file.</span></span>

## <a name="retail-server-or-crt-error-messages-or-receipt-strings"></a><span data-ttu-id="305f4-152">Retail サーバーや CRT エラー メッセージ、または入庫文字列</span><span class="sxs-lookup"><span data-stu-id="305f4-152">Retail server or CRT error messages, or receipt strings</span></span>

<span data-ttu-id="305f4-153">このセクションでは、既定の文字列を上書きすることによって Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="305f4-153">This section explains how to modify Retail server or CRT error messages, or receipt strings, by overriding the default strings.</span></span> <span data-ttu-id="305f4-154">新規、Retail サーバーまたは CRT のカスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="305f4-154">It also explains how you can add new, custom Retail server or CRT error messages, or receipt strings.</span></span>

### <a name="override-retail-server-or-crt-error-messages-or-receipt-strings"></a><span data-ttu-id="305f4-155">Retail サーバーや CRT エラー メッセージ、または入庫文字列を上書き</span><span class="sxs-lookup"><span data-stu-id="305f4-155">Override Retail server or CRT error messages, or receipt strings</span></span>

1. <span data-ttu-id="305f4-156">Retail または Finance and Operations へのサインイン</span><span class="sxs-lookup"><span data-stu-id="305f4-156">Sign in to Retail or Finance and Operations.</span></span>
2. <span data-ttu-id="305f4-157">**小売 \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="305f4-157">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Language text**.</span></span>
3. <span data-ttu-id="305f4-158">**言語テキスト**ページの、**Retail サーバー**タブの **Retail サーバー言語テキスト**グリッドで、**追加**ボタンをクリックして言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="305f4-158">On the **Language text** page, on the **Retail server** tab, in the **Retail server language text** grid, click the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="305f4-159">たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」</span><span class="sxs-lookup"><span data-stu-id="305f4-159">For example, when users enter an incorrect user name or password during sign-in, the POS shows the following error message: "We didn't recognize the user name or password.</span></span> <span data-ttu-id="305f4-160">もう一度やり直してください。」</span><span class="sxs-lookup"><span data-stu-id="305f4-160">Please try again."</span></span> <span data-ttu-id="305f4-161">英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。</span><span class="sxs-lookup"><span data-stu-id="305f4-161">For US English, you want to change the message to "Please enter valid user name or password."</span></span> <span data-ttu-id="305f4-162">この場合、**Retail サーバー 言語テキスト**グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="305f4-162">In this case, add the following entry in the **Retail server language text** grid.</span></span>

    | <span data-ttu-id="305f4-163">言語 ID</span><span class="sxs-lookup"><span data-stu-id="305f4-163">Language ID</span></span> | <span data-ttu-id="305f4-164">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="305f4-164">Text ID</span></span>                                                              | <span data-ttu-id="305f4-165">テキスト</span><span class="sxs-lookup"><span data-stu-id="305f4-165">Text</span></span>                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | <span data-ttu-id="305f4-166">ja</span><span class="sxs-lookup"><span data-stu-id="305f4-166">en-us</span></span>       | <span data-ttu-id="305f4-167">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span><span class="sxs-lookup"><span data-stu-id="305f4-167">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span></span> | <span data-ttu-id="305f4-168">有効なユーザー名またはパスワードを入力してください</span><span class="sxs-lookup"><span data-stu-id="305f4-168">Please enter valid user name or password</span></span> |

    > [!NOTE]
    > <span data-ttu-id="305f4-169">Retail サーバーまたは CRT エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="305f4-169">For information about how to get the text ID for Retail server or CRT error messages, and receipt strings, see the next section.</span></span>

4. <span data-ttu-id="305f4-170">アクション ウィンドウで、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="305f4-170">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="305f4-171">**小売 \> 小売 IT \> 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="305f4-171">Go to **Retail \> Retail IT \> Distribution schedule**.</span></span>
6. <span data-ttu-id="305f4-172">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="305f4-172">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

### <a name="get-the-text-id-for-retail-server-or-crt-messages-or-receipt-strings"></a><span data-ttu-id="305f4-173">Retail サーバーまたは CRT メッセージ、または入庫文字列のためのテキスト ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="305f4-173">Get the text ID for Retail server or CRT messages, or receipt strings</span></span>

1. <span data-ttu-id="305f4-174">**…\\RetailSDK\\ドキュメント\\リソース**に移動します。</span><span class="sxs-lookup"><span data-stu-id="305f4-174">Go to **…\\RetailSDK\\Documents\\Resources**.</span></span>
2. <span data-ttu-id="305f4-175">Visual Studio で、次のリソース ファイルのいずれかを開きます。</span><span class="sxs-lookup"><span data-stu-id="305f4-175">In Visual Studio, open one of the following resource files:</span></span>

    - <span data-ttu-id="305f4-176">**Retail server または CRT エラー メッセージを変更する:** RuntimeExceptionMessages.resx</span><span class="sxs-lookup"><span data-stu-id="305f4-176">**To modify Retail server or CRT error messages:** RuntimeExceptionMessages.resx</span></span>
    - <span data-ttu-id="305f4-177">**入力された文字列の変更:** RuntimeReceiptMessages.resx</span><span class="sxs-lookup"><span data-stu-id="305f4-177">**To modify receipt strings:** RuntimeReceiptMessages.resx</span></span>

    <span data-ttu-id="305f4-178">リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。</span><span class="sxs-lookup"><span data-stu-id="305f4-178">For every message in the resource file, Visual Studio shows a name and a value.</span></span>

3. <span data-ttu-id="305f4-179">**値**列で、変更するテキストを検索します。</span><span class="sxs-lookup"><span data-stu-id="305f4-179">In the **Value** column, search for the text that you want to change.</span></span>
4. <span data-ttu-id="305f4-180">その値に対応する名前をコピーします。</span><span class="sxs-lookup"><span data-stu-id="305f4-180">Copy the name that corresponds to that value.</span></span> <span data-ttu-id="305f4-181">この名前をテキストID として **Retail サーバー言語テキスト** グリッドに入力します。</span><span class="sxs-lookup"><span data-stu-id="305f4-181">You enter this name as the text ID in the **Retail server language text** grid.</span></span>

### <a name="add-custom-retail-server-or-crt-error-messages-or-receipt-strings"></a><span data-ttu-id="305f4-182">カスタム Retail サーバーまたは CRT エラー メッセージ、または入庫文字列を追加</span><span class="sxs-lookup"><span data-stu-id="305f4-182">Add custom Retail server or CRT error messages, or receipt strings</span></span>

<span data-ttu-id="305f4-183">新しい Retail サーバーまたは CRT エラー メッセージ、または、新しい入庫文字列を **Retail サーバー言語テキスト** グリッドに追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="305f4-183">You can also add new Retail server or CRT error messages, or new receipt strings, in the **Retail server language text** grid.</span></span> <span data-ttu-id="305f4-184">この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。</span><span class="sxs-lookup"><span data-stu-id="305f4-184">In this way, you support localization instead of hard-coding everything in the code.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="305f4-185">すべてのメッセージのテキスト ID は **Microsoft\_Dynamics\_Commerce\_** から始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="305f4-185">The text ID of all your new messages must start with **Microsoft\_Dynamics\_Commerce\_**.</span></span>

<span data-ttu-id="305f4-186">たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。</span><span class="sxs-lookup"><span data-stu-id="305f4-186">For example, you want to add a new exception message in US English (en-us) and UK English (en-uk).</span></span> <span data-ttu-id="305f4-187">この場合、**Retail サーバー言語テキスト**グリッドでの次のエントリに類似したエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="305f4-187">In this case, add entries that resemble the follow entries in the **Retail server language text** grid.</span></span>

| <span data-ttu-id="305f4-188">言語 ID</span><span class="sxs-lookup"><span data-stu-id="305f4-188">Language ID</span></span> | <span data-ttu-id="305f4-189">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="305f4-189">Text ID</span></span>                                 | <span data-ttu-id="305f4-190">テキスト</span><span class="sxs-lookup"><span data-stu-id="305f4-190">Text</span></span>                    |
|-------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="305f4-191">ja</span><span class="sxs-lookup"><span data-stu-id="305f4-191">en-us</span></span>       | <span data-ttu-id="305f4-192">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="305f4-192">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="305f4-193">アメリカ英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="305f4-193">My new message in US English</span></span> |
| <span data-ttu-id="305f4-194">en-uk</span><span class="sxs-lookup"><span data-stu-id="305f4-194">en-uk</span></span>       | <span data-ttu-id="305f4-195">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="305f4-195">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="305f4-196">英国英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="305f4-196">My new message in UK English</span></span> |

> [!NOTE]
> <span data-ttu-id="305f4-197">この例では、**CustomId1** が新しいメッセージのテキスト ID です。</span><span class="sxs-lookup"><span data-stu-id="305f4-197">In this example, **CustomId1** is the text ID for the new message.</span></span> <span data-ttu-id="305f4-198">使用したい任意のテキスト ID を使用することができます。ただし、**Microsoft_Dynamics_Commerce_** で始まる場合に限ります</span><span class="sxs-lookup"><span data-stu-id="305f4-198">You can use any text ID that you want, provided that it starts with **Microsoft_Dynamics_Commerce_**.</span></span>

<span data-ttu-id="305f4-199">次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="305f4-199">The following example shows how to use this new message in your CRT extension code.</span></span>

```C#
throw new CommerceException("Microsoft_Dynamics_Commerce_CustomId1", ExceptionSeverity.Warning, null, "Custom error")
                    {
                        LocalizedMessage = "My new message in US English.",
                        LocalizedMessageParameters = new object[] { }
                    };
```

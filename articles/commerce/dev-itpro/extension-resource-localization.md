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
ms.search.region: Global
ms.search.industry: retail
ms.author: mumani
ms.search.validFrom: 2018-05-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 34b35df30e39497db6b0c9dfcb8760155a666954
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681570"
---
# <a name="localize-commerce-extension-resources-and-label-files"></a><span data-ttu-id="e256e-103">コマース拡張リソースおよびラベル ファイルのローカライズ</span><span class="sxs-lookup"><span data-stu-id="e256e-103">Localize Commerce extension resources and label files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e256e-104">このトピックでは、販売時点管理 (POS) ユーザー インターフェイス (UI)、POS メッセージ (エラー、警告、および情報)、入庫ラベル、および Commerce Scale Unit または Commerce Runtime のサービス (CRT) のエラー メッセージの点にラベルを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e256e-104">This topic explains how to modify labels in the point of sale (POS) user interface (UI), POS messages (error, warning, and information), receipt labels, and error messages for Commerce Scale Unit or Commerce Runtime Services (CRT).</span></span> <span data-ttu-id="e256e-105">カスタム エラー メッセージを同じ方法で追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="e256e-105">You can also add custom error messages for in the same way.</span></span> <span data-ttu-id="e256e-106">ただし、新しい POS 拡張ラベルの場合は、POS 拡張のローカライズ フレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="e256e-106">However, for new POS extension labels, you should use the localization framework in the POS extension.</span></span>

## <a name="pos-labels-and-messages-error-warning-and-information"></a><span data-ttu-id="e256e-107">POS ラベルおよびメッセージ (エラー、警告、および情報)</span><span class="sxs-lookup"><span data-stu-id="e256e-107">POS labels and messages (error, warning, and information)</span></span>

<span data-ttu-id="e256e-108">このセクションでは、既定の文字列を上書きすることによって、POS UI ラベルおよび POS メッセージを変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e256e-108">This section explains how to modify POS UI labels and POS messages by overriding the default strings.</span></span>

### <a name="override-pos-ui-labels-and-messages"></a><span data-ttu-id="e256e-109">POS UI ラベルおよびメッセージの上書き</span><span class="sxs-lookup"><span data-stu-id="e256e-109">Override POS UI labels and messages</span></span>

<span data-ttu-id="e256e-110">**言語テキスト** ページの言語テキスト エントリを使用して、POS の既定の文字列を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="e256e-110">You can override the default strings in the POS by using the language text entries on the **Language text** page.</span></span> <span data-ttu-id="e256e-111">POS 文字列を変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="e256e-111">Follow these steps to change POS strings.</span></span>

1. <span data-ttu-id="e256e-112">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="e256e-112">Sign in to Commerce.</span></span>
2. <span data-ttu-id="e256e-113">**Retail とコマース &gt; チャネル設定 &gt; POS 設定 &gt; POS プロファイル &gt; 言語テキスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e256e-113">Go to **Retail and Commerce &gt; Channel setup &gt; POS setup &gt; POS profiles &gt; Language text**.</span></span>
3. <span data-ttu-id="e256e-114">**言語テキスト** ページの、**POS** タブの **POS 言語テキスト** グリッドで、**追加** ボタンを選択して言語 ID、テキスト ID、および上書きする文字列のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="e256e-114">On the **Language text** page, on the **POS** tab, in the **POS language text** grid, select the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="e256e-115">たとえば、POS サインイン ページの **オペレーター ID** フィールドのラベルを、アメリカ英語 (en-us) の **従業員 ID** に変更したいとします。</span><span class="sxs-lookup"><span data-stu-id="e256e-115">For example, you want to change the label of the **Operator ID** field on the POS sign-in page to **Employee ID** for US English (en-us).</span></span> <span data-ttu-id="e256e-116">この場合、**POS 言語テキスト** グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="e256e-116">In this case, add the following entry in the **POS language text** grid.</span></span>

    | <span data-ttu-id="e256e-117">言語 ID</span><span class="sxs-lookup"><span data-stu-id="e256e-117">Language ID</span></span> | <span data-ttu-id="e256e-118">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="e256e-118">Text ID</span></span> | <span data-ttu-id="e256e-119">テキスト</span><span class="sxs-lookup"><span data-stu-id="e256e-119">Text</span></span>        |
    |-------------|---------|-------------|
    | <span data-ttu-id="e256e-120">ja</span><span class="sxs-lookup"><span data-stu-id="e256e-120">en-us</span></span>       | <span data-ttu-id="e256e-121">502</span><span class="sxs-lookup"><span data-stu-id="e256e-121">502</span></span>     | <span data-ttu-id="e256e-122">従業員 ID</span><span class="sxs-lookup"><span data-stu-id="e256e-122">Employee ID</span></span> |

    > [!NOTE]
    > <span data-ttu-id="e256e-123">POS 文字列のテキスト ID を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e256e-123">For information about how to get the text ID for POS strings, see the next section.</span></span>

4. <span data-ttu-id="e256e-124">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e256e-124">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="e256e-125">**Retail とコマース &gt; Retail とコマース IT &gt; 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e256e-125">Go to **Retail and Commerce &gt; Retail and Commerce IT &gt; Distribution schedule**.</span></span>
6. <span data-ttu-id="e256e-126">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e256e-126">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>
7. <span data-ttu-id="e256e-127">データをプッシュ後、クラウド POS または Modern POS でログインし、変更済のラベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="e256e-127">After the data is pushed, sign off, and then sign in to Cloud POS or Modern POS to see the changed labels.</span></span>

### <a name="get-the-text-id-for-pos-strings"></a><span data-ttu-id="e256e-128">POS 文字列のテキスト ID を取得します</span><span class="sxs-lookup"><span data-stu-id="e256e-128">Get the text ID for POS strings</span></span>

<span data-ttu-id="e256e-129">POS 文字列のテキスト ID を取得するには、最新の POS/Cloud POS アプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="e256e-129">To get the text ID for a POS string, open the Modern POS/Cloud POS application.</span></span> <span data-ttu-id="e256e-130">F12 を押下して 開発者コマンドツールを起動し、 **コンソール** タブを選択して JavaScript コンソールを開きます。</span><span class="sxs-lookup"><span data-stu-id="e256e-130">Press F12 to launch the developer command tools and select the **Console** tab to open the JavaScript console.</span></span> <span data-ttu-id="e256e-131">JavaScript コンソールで **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** コマンドを実行して、開発者モードを起動します。</span><span class="sxs-lookup"><span data-stu-id="e256e-131">Run the **Commerce.Helpers.DeveloperModeHelper.setDeveloperMode(true);** command in the JavaScript console to turn on the developer mode.</span></span>

<span data-ttu-id="e256e-132">JavaScript コンソールで開発者モードを有効にした後、**開発者モード** の下にある POS の **設定** ページに移動し、**開発者モード** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e256e-132">After enabling the developer mode in the JavaScript console, navigate to the **Settings** page in POS, under the **Developer mode**, set **Developer Mode** to **Yes**.</span></span> <span data-ttu-id="e256e-133">**文字列 ID の表示** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e256e-133">Set **Show Strings IDs** to **Yes**.</span></span> <span data-ttu-id="e256e-134">POS からサインアウトし、再度サインインします。</span><span class="sxs-lookup"><span data-stu-id="e256e-134">Sign out of the POS, and then sign in again.</span></span> <span data-ttu-id="e256e-135">POS には、すべてのラベルとメッセージの前に文字列 ID が表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="e256e-135">The POS now shows the strings IDs in front of all the labels and messages.</span></span>


## <a name="error-messages-or-receipt-strings"></a><span data-ttu-id="e256e-136">エラー メッセージまたは入庫文字列</span><span class="sxs-lookup"><span data-stu-id="e256e-136">Error messages or receipt strings</span></span>

<span data-ttu-id="e256e-137">このセクションでは、既定の文字列を上書きすることによってエラー メッセージ、または入庫文字列を変更する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e256e-137">This section explains how to modify error messages, or receipt strings, by overriding the default strings.</span></span> <span data-ttu-id="e256e-138">新規、カスタム エラー メッセージ、または入庫文字列を追加する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="e256e-138">It also explains how you can add new, custom error messages, or receipt strings.</span></span>

### <a name="override-error-messages-or-receipt-strings"></a><span data-ttu-id="e256e-139">エラー メッセージまたは入庫文字列を上書きする</span><span class="sxs-lookup"><span data-stu-id="e256e-139">Override error messages or receipt strings</span></span>

1. <span data-ttu-id="e256e-140">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="e256e-140">Sign in to Commerce.</span></span>
2. <span data-ttu-id="e256e-141">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e256e-141">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Language text**.</span></span>
3. <span data-ttu-id="e256e-142">**言語テキスト** ページで、**追加** ボタンをクリックして、上書きする文字列の言語 ID、テキスト ID、およびテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="e256e-142">On the **Language text** page, click the **Add** button to add the language ID, text ID, and text for the string that you want to override.</span></span>

    <span data-ttu-id="e256e-143">たとえば、サインイン中にユーザーが間違ったユーザー名またはパスワードを入力すると、POS に次のエラー メッセージが表示されます: 「ユーザー名またはパスワードが認識されませんでした。」</span><span class="sxs-lookup"><span data-stu-id="e256e-143">For example, when users enter an incorrect user name or password during sign-in, the POS shows the following error message: "We didn't recognize the user name or password.</span></span> <span data-ttu-id="e256e-144">もう一度やり直してください。」</span><span class="sxs-lookup"><span data-stu-id="e256e-144">Please try again."</span></span> <span data-ttu-id="e256e-145">英語 (US) では、メッセージを「有効なユーザー名またはパスワードを入力してください」に変更します。</span><span class="sxs-lookup"><span data-stu-id="e256e-145">For US English, you want to change the message to "Please enter valid user name or password."</span></span> <span data-ttu-id="e256e-146">この場合、**言語テキスト** グリッドで次のエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="e256e-146">In this case, add the following entry in the **language text** grid.</span></span>

    | <span data-ttu-id="e256e-147">言語 ID</span><span class="sxs-lookup"><span data-stu-id="e256e-147">Language ID</span></span> | <span data-ttu-id="e256e-148">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="e256e-148">Text ID</span></span>                                                              | <span data-ttu-id="e256e-149">テキスト</span><span class="sxs-lookup"><span data-stu-id="e256e-149">Text</span></span>                                     |
    |-------------|----------------------------------------------------------------------|------------------------------------------|
    | <span data-ttu-id="e256e-150">ja</span><span class="sxs-lookup"><span data-stu-id="e256e-150">en-us</span></span>       | <span data-ttu-id="e256e-151">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span><span class="sxs-lookup"><span data-stu-id="e256e-151">Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidAuthenticationCredentials</span></span> | <span data-ttu-id="e256e-152">有効なユーザー名またはパスワードを入力してください</span><span class="sxs-lookup"><span data-stu-id="e256e-152">Please enter valid user name or password</span></span> |

    > [!NOTE]
    > <span data-ttu-id="e256e-153">エラー メッセージのテキスト ID、および入庫文字列を取得する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e256e-153">For information about how to get the text ID for error messages and receipt strings, see the next section.</span></span>

4. <span data-ttu-id="e256e-154">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e256e-154">On the Action Pane, select **Save**.</span></span>
5. <span data-ttu-id="e256e-155">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e256e-155">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
6. <span data-ttu-id="e256e-156">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e256e-156">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

### <a name="get-the-text-id-for-messages-or-receipt-strings"></a><span data-ttu-id="e256e-157">メッセージまたは入庫文字列のテキスト ID を取得する</span><span class="sxs-lookup"><span data-stu-id="e256e-157">Get the text ID for messages or receipt strings</span></span>

1. <span data-ttu-id="e256e-158">**…\\RetailSDK\\ドキュメント\\リソース** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e256e-158">Go to **…\\RetailSDK\\Documents\\Resources**.</span></span>
2. <span data-ttu-id="e256e-159">Visual Studio で、次のリソース ファイルのいずれかを開きます。</span><span class="sxs-lookup"><span data-stu-id="e256e-159">In Visual Studio, open one of the following resource files:</span></span>

    - <span data-ttu-id="e256e-160">**エラー メッセージを変更するには:** RuntimeExceptionMessages.resx</span><span class="sxs-lookup"><span data-stu-id="e256e-160">**To modify error messages:** RuntimeExceptionMessages.resx</span></span>
    - <span data-ttu-id="e256e-161">**入力された文字列の変更:** RuntimeReceiptMessages.resx</span><span class="sxs-lookup"><span data-stu-id="e256e-161">**To modify receipt strings:** RuntimeReceiptMessages.resx</span></span>

    <span data-ttu-id="e256e-162">リソース ファイル内のすべてのメッセージについて、Visual Studio は名前と値を表示します。</span><span class="sxs-lookup"><span data-stu-id="e256e-162">For every message in the resource file, Visual Studio shows a name and a value.</span></span>

3. <span data-ttu-id="e256e-163">**値** 列で、変更するテキストを検索します。</span><span class="sxs-lookup"><span data-stu-id="e256e-163">In the **Value** column, search for the text that you want to change.</span></span>
4. <span data-ttu-id="e256e-164">その値に対応する名前をコピーします。</span><span class="sxs-lookup"><span data-stu-id="e256e-164">Copy the name that corresponds to that value.</span></span> <span data-ttu-id="e256e-165">この名前をテキスト ID として **言語テキスト** グリッドに入力します。</span><span class="sxs-lookup"><span data-stu-id="e256e-165">You enter this name as the text ID in the **language text** grid.</span></span>

### <a name="add-custom-error-messages-or-receipt-strings"></a><span data-ttu-id="e256e-166">カスタム エラー メッセージまたは入庫文字列を追加する</span><span class="sxs-lookup"><span data-stu-id="e256e-166">Add custom error messages or receipt strings</span></span>

<span data-ttu-id="e256e-167">新しいエラー メッセージまたは新しい入庫文字列を、**言語テキスト** ページで追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="e256e-167">You can also add new error messages or new receipt strings, on the **Language text** page.</span></span> <span data-ttu-id="e256e-168">この方法で、コード内のハードコーディングのすべての代わりにローカライズをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e256e-168">In this way, you support localization instead of hard-coding everything in the code.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e256e-169">すべてのメッセージのテキスト ID は **Microsoft\_Dynamics\_Commerce\_** から始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e256e-169">The text ID of all your new messages must start with **Microsoft\_Dynamics\_Commerce\_**.</span></span>

<span data-ttu-id="e256e-170">たとえば、アメリカ英語 (en-us) と英国英語 (en-uk) で新しい例外メッセージを追加したいとします。</span><span class="sxs-lookup"><span data-stu-id="e256e-170">For example, you want to add a new exception message in US English (en-us) and UK English (en-uk).</span></span> <span data-ttu-id="e256e-171">この場合、**言語テキスト** ページでの次のエントリに類似したエントリを追加します。</span><span class="sxs-lookup"><span data-stu-id="e256e-171">In this case, add entries that resemble the follow entries on the **Language text** page.</span></span>

| <span data-ttu-id="e256e-172">言語 ID</span><span class="sxs-lookup"><span data-stu-id="e256e-172">Language ID</span></span> | <span data-ttu-id="e256e-173">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="e256e-173">Text ID</span></span>                                 | <span data-ttu-id="e256e-174">テキスト</span><span class="sxs-lookup"><span data-stu-id="e256e-174">Text</span></span>                    |
|-------------|-----------------------------------------|-------------------------|
| <span data-ttu-id="e256e-175">ja</span><span class="sxs-lookup"><span data-stu-id="e256e-175">en-us</span></span>       | <span data-ttu-id="e256e-176">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="e256e-176">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="e256e-177">アメリカ英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="e256e-177">My new message in US English</span></span> |
| <span data-ttu-id="e256e-178">en-uk</span><span class="sxs-lookup"><span data-stu-id="e256e-178">en-uk</span></span>       | <span data-ttu-id="e256e-179">Microsoft_Dynamics_Commerce_CustomId1</span><span class="sxs-lookup"><span data-stu-id="e256e-179">Microsoft_Dynamics_Commerce_CustomId1</span></span> | <span data-ttu-id="e256e-180">英国英語での新しいメッセージ</span><span class="sxs-lookup"><span data-stu-id="e256e-180">My new message in UK English</span></span> |

> [!NOTE]
> <span data-ttu-id="e256e-181">この例では、**CustomId1** が新しいメッセージのテキスト ID です。</span><span class="sxs-lookup"><span data-stu-id="e256e-181">In this example, **CustomId1** is the text ID for the new message.</span></span> <span data-ttu-id="e256e-182">使用したい任意のテキスト ID を使用することができます。ただし、**Microsoft_Dynamics_Commerce_** で始まる場合に限ります</span><span class="sxs-lookup"><span data-stu-id="e256e-182">You can use any text ID that you want, provided that it starts with **Microsoft_Dynamics_Commerce_**.</span></span>

<span data-ttu-id="e256e-183">次の例では、この新しいメッセージを CRT 拡張コードで使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e256e-183">The following example shows how to use this new message in your CRT extension code.</span></span>

```C#
throw new CommerceException("Microsoft_Dynamics_Commerce_CustomId1", ExceptionSeverity.Warning, null, "Custom error")
                    {
                        LocalizedMessage = "My new message in US English.",
                        LocalizedMessageParameters = new object[] { }
                    };
```

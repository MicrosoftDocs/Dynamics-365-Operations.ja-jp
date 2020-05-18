---
title: ローカライズ可能なラベルの作成
description: この記事では、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ可能なラベルを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 18531
ms.assetid: 73615d1b-9088-496e-989e-d8996f30e76b
ms.search.region: Global
ms.author: shshabazz
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05ba812cc76a7c5c1e90f41f85863626ade28247
ms.sourcegitcommit: 17fe0218e8e3f2f4c57c73c0c438a6ebf1ef32a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/01/2020
ms.locfileid: "3329927"
---
# <a name="create-localizable-labels"></a><span data-ttu-id="ffb11-103">ローカライズ可能なラベルの作成</span><span class="sxs-lookup"><span data-stu-id="ffb11-103">Create localizable labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffb11-104">この記事では、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ可能なラベルを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-104">This article explains how to create localizable labels for client components and HTML/JavaScript controls.</span></span>

<span data-ttu-id="ffb11-105">この記事では、クライアント コンポーネントと HTML/JavaScript コントロールの**ローカライズ可能な**ラベルを作成するプロセスについて詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-105">This article details the process for creating **localizable** labels for client components and HTML/JavaScript controls.</span></span> <span data-ttu-id="ffb11-106">このプロセスでは、既存のローカライズ ツールとラベル用のプロセスを使用して、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ  サポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-106">This process uses the existing localization tools and process for labels to bring localization support to client components and HTML/JavaScript controls.</span></span> <span data-ttu-id="ffb11-107">次のプロセスでは、クライアント コンポーネントと HTML/JavaScript コントロールでラベルを使用できるように、ラベル ファイルを JavaScript に相当するものにシリアル化できるラベル リソース コントローラーが使用されています。</span><span class="sxs-lookup"><span data-stu-id="ffb11-107">The following process relies on the label resource controller that can serialize label files into their JavaScript equivalents so that the labels can be used by the client components and HTML/JavaScript controls.</span></span> <span data-ttu-id="ffb11-108">ラベル リソース コントローラーは自動的に配置されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-108">The label resource controller is deployed automatically.</span></span> <span data-ttu-id="ffb11-109">/Resources/Labels エンドポイントに配置されている MVC サービスです。</span><span class="sxs-lookup"><span data-stu-id="ffb11-109">It is an MVC service that is located at the /Resources/Labels endpoint.</span></span>

## <a name="1-create-a-label-file"></a><span data-ttu-id="ffb11-110">1. ラベル ファイルの作成</span><span class="sxs-lookup"><span data-stu-id="ffb11-110">1. Create a label file</span></span>
<span data-ttu-id="ffb11-111">開発者ツールを使用して、コントロールの領域に新しいラベル ファイルを作成するか、コントロールの領域に既存のラベル ファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-111">Use the developer tools to create a new label file for your control's area, or use an existing label file for your control's area.</span></span> <span data-ttu-id="ffb11-112">コントロールの領域は、チームによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-112">A control's area is determined by the owning team.</span></span>

-   <span data-ttu-id="ffb11-113">拡張可能なコントロールについては、目標として、HTM リソース ファイルごとに 1 つのラベル ファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb11-113">For extensible controls, your goal should be to create one label file for each HTM resource file.</span></span> <span data-ttu-id="ffb11-114">複数の HTM リソースは、同じラベルのセットを共有している場合、1 つだけのラベル ファイルが HTM リソース ファイルのセットに対して必要となります。</span><span class="sxs-lookup"><span data-stu-id="ffb11-114">If multiple HTM resources share the same set of labels, only one label file should be required for the set of HTM resource files.</span></span>
-   <span data-ttu-id="ffb11-115">クライアント コントロールおよびコンポーネントでは、一般に、多くの同じ機能 (たとえば、入力コントロール: StringEdit、コンボボックス、チェックボックスなど) を共有するコントロールは、同じラベル ファイルも共有する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb11-115">For client controls and components, in general, controls that share a lot of the same functionality (for example, the Input controls: StringEdit, ComboBox, CheckBox, and so on) should also share the same label file.</span></span>

<span data-ttu-id="ffb11-116">*X ++ のみで使用されるラベルを含めて、ラベル ファイルは使用しないでください。*</span><span class="sxs-lookup"><span data-stu-id="ffb11-116">*Don't use a label file that also contains labels that are only used in X++.*</span></span> <span data-ttu-id="ffb11-117">ラベル ファイル全体がクライアントによってロードされると、シリアル化されるため、クライアント コンポーネント/コントロールで必要とされないラベルを別のラベル ファイルに保存してください。</span><span class="sxs-lookup"><span data-stu-id="ffb11-117">The whole label file is serialized when it’s loaded by the client, so be sure to keep the labels that aren't required by the client components/controls in a separate label file.</span></span>

## <a name="2-add-label-strings-to-the-label-file"></a><span data-ttu-id="ffb11-118">2. ラベル ファイルにラベル文字列を追加する</span><span class="sxs-lookup"><span data-stu-id="ffb11-118">2. Add label strings to the label file</span></span>
<span data-ttu-id="ffb11-119">開発者ツールを使用して、ラベル文字列をラベル ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-119">Use the developer tools to add label strings to the label file.</span></span> <span data-ttu-id="ffb11-120">**拡張可能なコントロールの例:**</span><span class="sxs-lookup"><span data-stu-id="ffb11-120">**Example for extensible controls:**</span></span>

-   <span data-ttu-id="ffb11-121">**ラベル ファイル名:** ClockControl</span><span class="sxs-lookup"><span data-stu-id="ffb11-121">**Label file name:** ClockControl</span></span>
-   <span data-ttu-id="ffb11-122">**ラベル ID:** Seconds</span><span class="sxs-lookup"><span data-stu-id="ffb11-122">**Label ID:** Seconds</span></span>
-   <span data-ttu-id="ffb11-123">**ラベル文字列:** seconds</span><span class="sxs-lookup"><span data-stu-id="ffb11-123">**Label string:** seconds</span></span>

## <a name="3-request-the-label-file-as-a-javascript-file-by-using-resource-manager"></a><span data-ttu-id="ffb11-124">3. リソース マネージャーを使用して、ラベル ファイルを JavaScript ファイルとして要求する</span><span class="sxs-lookup"><span data-stu-id="ffb11-124">3. Request the label file as a JavaScript file by using Resource manager</span></span>
<span data-ttu-id="ffb11-125">タグ読み込みスクリプトを使用して、JavaScript ファイルを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-125">Use the script loading tag to load the JavaScript file.</span></span> <span data-ttu-id="ffb11-126">ローディング タグは、ラベル リソース コントローラーがそこにあるため、/Resources/Labels のラベル ファイルを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ffb11-126">The loading tag should reference the label file from /Resources/Labels, because the label resource controller is located there.</span></span> <span data-ttu-id="ffb11-127">**注記:** 拡張可能なコントロールの場合、コントローラーは自動的にラベル ファイル名を JavaScript のラベル ID の先頭に追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-127">**Note:** For extensible controls, the controller automatically appends the label file name to the beginning of the label identifier in JavaScript.</span></span>

```javascript
<script src="/Resources/Labels/ClockControl.js"></script>
```

<span data-ttu-id="ffb11-128">返される JavaScript ファイルには、次の例のようなコードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-128">The JavaScript file that is returned will contain code that resembles the following example.</span></span>

```javascript
Globalize.addCultureInfo("en-us", {
    messages: {
        ClockControl_Seconds: "seconds"
    }
});
```

<span data-ttu-id="ffb11-129">カルチャ情報は、現在のユーザーのカルチャに基づいて自動的に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-129">The culture information is injected automatically, based on the current user's culture.</span></span> <span data-ttu-id="ffb11-130">コントロールの部分でユーザーのカルチャの設定、変更、読み取りに必要なアクションはありません。</span><span class="sxs-lookup"><span data-stu-id="ffb11-130">No action is required on the part of the control to set, modify, or read the user's culture.</span></span> <span data-ttu-id="ffb11-131">上記のコードは、jQuery Globalize ラベル記憶域に各ラベル文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-131">The preceding code adds each of your label strings to the jQuery Globalize label storage.</span></span> <span data-ttu-id="ffb11-132">HTML と JavaScript 全体でラベルを参照することができます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-132">You can then reference your labels throughout your HTML and JavaScript.</span></span> <span data-ttu-id="ffb11-133">スクリプト ファイルにある JavaScript コードは、ブラウザーによってファイルが読み込まれた時点で実行されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-133">The JavaScript code in the script file is run the moment that the file is loaded by the browser.</span></span> <span data-ttu-id="ffb11-134">したがって、ラベルはすぐに使用できる状態になります。</span><span class="sxs-lookup"><span data-stu-id="ffb11-134">Therefore, your labels are immediately ready for use.</span></span> <span data-ttu-id="ffb11-135">HTML に他のスクリプト読み込みタグの**後**、ラベルスクリプトの読み込みタグを必ず追加してください。</span><span class="sxs-lookup"><span data-stu-id="ffb11-135">Be sure to add the label script loading tag **after** any other script loading tags in your HTML.</span></span> <span data-ttu-id="ffb11-136">スクリプト読み込みタグは、上から順に処理されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-136">The script loading tags are processed in order, from top to bottom.</span></span> <span data-ttu-id="ffb11-137">最後にラベル スクリプトを読み込むことによって、他のスクリプトが競合を起こさないようにするか、スクリプト ラベル ファイルに設定されているラベルを上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-137">By loading the label script last, you help guarantee that no other scripts cause conflicts or override the labels that are set in the script label file.</span></span>

## <a name="4-use-localizable-labels-in-html-and-javascript"></a><span data-ttu-id="ffb11-138">4. HTML と JavaScript でローカライズ可能なラベルを使用する</span><span class="sxs-lookup"><span data-stu-id="ffb11-138">4. Use localizable labels in HTML and JavaScript</span></span>
<span data-ttu-id="ffb11-139">次のフレームワーク アプリケーション プログラミング インターフェイス (API) は、HTML (内部 **data-dyn-bind**) または JavaScript でラベルにアクセスするために使用できます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-139">The following framework application programming interface (API) can be used in HTML (inside **data-dyn-bind**) or in JavaScript to access the labels.</span></span> <span data-ttu-id="ffb11-140">**HTML**</span><span class="sxs-lookup"><span data-stu-id="ffb11-140">**HTML**</span></span>

```javascript
<!-- Example of using a localizable label with a Label Control. Supply the label to the "Text" property on the control -->
<div data-dyn-role="Label" data-dyn-bind="Text: $dyn.label('ClockControl_Seconds')"></div>
<!-- Example of using a localizable label with a basic HTML element. Supply the label to the "text" binding handler for the element -->
<div data-dyn-bind="text: $dyn.label('ClockControl_Seconds')"></div>
```

<span data-ttu-id="ffb11-141">**JavaScript**</span><span class="sxs-lookup"><span data-stu-id="ffb11-141">**JavaScript**</span></span>

```javascript
/* Example of using a localizable label in JavaScript. */
var string mylabel = $dyn.label('ClockControl_Seconds');
```

<span data-ttu-id="ffb11-142">HTML または JavaScript の変数を介してラベル ID を渡すこともできます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-142">You can also pass the label ID via a variable in HTML or JavaScript.</span></span> <span data-ttu-id="ffb11-143">**HTML**</span><span class="sxs-lookup"><span data-stu-id="ffb11-143">**HTML**</span></span>

```javascript
<div data-dyn-bind="text: $dyn.label($data.SecondsLabel)"></div>
```

<span data-ttu-id="ffb11-144">**JavaScript**</span><span class="sxs-lookup"><span data-stu-id="ffb11-144">**JavaScript**</span></span>

```javascript
var string mylabel = $dyn.label(self.SecondsLabel);
```

<span data-ttu-id="ffb11-145">**$dyn.label** API は、適切な名前のラベルを検索し、ユーザーにテキストを表示するために使用する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-145">The **$dyn.label** API will find the appropriately named label and return the string that can be used to display text to the user.</span></span> <span data-ttu-id="ffb11-146">この API は、現在のユーザーのカルチャに基づいてラベルを自動的に選択します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-146">This API will automatically select the label, based on the current user's culture.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ffb11-147">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="ffb11-147">Troubleshooting</span></span>
<span data-ttu-id="ffb11-148">ラベル ファイルが正しく作成され、そのラベルが展開されている場合は、ブラウザから直接、ラベルファイルの JavaScript バージョンを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-148">If you have correctly created a label file, and the label has been deployed, you should be able to load the JavaScript version of the label file directly from the browser.</span></span> <span data-ttu-id="ffb11-149">JavaScript のラベル ファイルには、クライアントのホーム ページに移動して、URL にパス **/Resources/Labels/MyLabelFile.js** を加えてアクセスすることができます。ここで **MyLabelFile** は言語の接尾語なしのラベル ファイル名です。</span><span class="sxs-lookup"><span data-stu-id="ffb11-149">You can access the JavaScript label file by navigating to the home page in the client and appending the following path to the URL: **/Resources/Labels/MyLabelFile.js**, where **MyLabelFile** is the name of the label file without the language suffix.</span></span> <span data-ttu-id="ffb11-150">MyLabelFile.en-us という名前の配置されたラベル ファイルのについては、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="ffb11-150">For a deployed label file that is named MyLabelFile.en-us, follow these steps:</span></span>

1. <span data-ttu-id="ffb11-151">ホーム ページに移動して、サインインします。</span><span class="sxs-lookup"><span data-stu-id="ffb11-151">Navigate to the home page, and sign in.</span></span> <span data-ttu-id="ffb11-152">(ワン ボックス配置では、ホーム ページの URL は<https://usncax1aos.cloud.onebox.dynamics.com/en/> です。)</span><span class="sxs-lookup"><span data-stu-id="ffb11-152">(On one-box deployments, the URL of the home page is <https://usncax1aos.cloud.onebox.dynamics.com/en/>.)</span></span>
2. <span data-ttu-id="ffb11-153">目的の言語が**オプション** &gt; **言語および地域**で設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-153">Make sure that the desired language has been set by going to **Options** &gt; **Language and Region**.</span></span> <span data-ttu-id="ffb11-154">(目的の言語に設定されている場合は言語を変更する必要はありません。) ユーザーの言語が現在のセッションで設定されたので、ラベル リソース コントローラーは、ラベル ファイルが読み込まれるときに使用する言語を認識します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-154">(You don't have to change the language if it's already set to the language that you want.) Now that the user's language has been set in the current session, the label resource controller will know what language to use when the label file is loaded.</span></span>
3. <span data-ttu-id="ffb11-155">JavaScript バージョンのラベル ファイルを読み込むには、<strong>Resources/Labels/MyLabelFile.js</strong> を URL に追加してラベル ファイルに移動します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-155">To load the JavaScript version of the label file, navigate to the label file by adding <strong>Resources/Labels/MyLabelFile.js</strong> to the URL.</span></span> <span data-ttu-id="ffb11-156">(ワン ボックス配置では、全体の URL は<https://usncax1aos.cloud.onebox.dynamics.com/en/Resources/Labels/MyLabelFile.js> です。)</span><span class="sxs-lookup"><span data-stu-id="ffb11-156">(On one-box deployments, the whole URL is <https://usncax1aos.cloud.onebox.dynamics.com/en/Resources/Labels/MyLabelFile.js>.)</span></span>
4. <span data-ttu-id="ffb11-157">対応するラベル ファイルは JSON シリアル化され、ブラウザーは現在のタブにテキストを表示するか、.js ファイルのダウンロードを促すメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="ffb11-157">The corresponding label file will be JSON-serialized, and the browser will either show the text on the current tab or prompt you to download the .js file.</span></span> <span data-ttu-id="ffb11-158">ファイルをダウンロードする場合、ローカルでそれを開き、検査できます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-158">If you download the file, you can then open it locally to inspect it.</span></span>

<span data-ttu-id="ffb11-159">ブラウザーにファイルが見つからない場合は、ラベルの名前を誤って入力した、またはラベルを正しく展開しなかった可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ffb11-159">If the browser doesn't find the file, you might have mistyped the name of the label, or you might not have deployed the label correctly.</span></span> <span data-ttu-id="ffb11-160">Web フォルダー/リソース/ラベルのラベルに物理的な .js ファイルはありません。</span><span class="sxs-lookup"><span data-stu-id="ffb11-160">There is never a physical .js file for the label in the web folder /Resources/Labels.</span></span> <span data-ttu-id="ffb11-161">.js ファイルは、ラベル リソース コントローラーによって動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-161">The .js file is dynamically generated by the label resource controller.</span></span>

### <a name="microsoft-visual-studio-form-previewer"></a><span data-ttu-id="ffb11-162">Microsoft Visual Studioフォーム プレビューアー</span><span class="sxs-lookup"><span data-stu-id="ffb11-162">Microsoft Visual Studio form previewer</span></span>

<span data-ttu-id="ffb11-163">フォーム プレビューアーは、ラベル リソース コントローラー経由でラベルを読み込むようには現在設定されていません。</span><span class="sxs-lookup"><span data-stu-id="ffb11-163">The form previewer isn't currently configured to load labels via the label resource controller.</span></span> <span data-ttu-id="ffb11-164">フォーム プレビューアーは、コード ビハインド (/Resources/Scripts にあります) の .js ファイルに直接定義されているラベルのみを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-164">The form previewer will load only labels that are defined directly in the .js file for the code behind (located at /Resources/Scripts).</span></span> <span data-ttu-id="ffb11-165">フォーム プレビューアを更新して、ラベル リソース コントローラから .js ファイルをロードできるようになるまでは、コントロールのコード ビハインドの .js ファイルにもラベルを定義するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ffb11-165">Until the form previewer is updated so that it can load .js files from the label resource controller, make sure that you also define the labels in the .js file for the code behind of the control.</span></span> <span data-ttu-id="ffb11-166">これらのラベルへの依存関係は、将来の更新で削除されます。</span><span class="sxs-lookup"><span data-stu-id="ffb11-166">The dependency on these labels will be removed in a future update.</span></span>




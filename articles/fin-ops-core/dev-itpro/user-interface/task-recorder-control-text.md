---
title: コントロールに対してタスク レコーダーが生成するテキストの制御
description: この記事では、タスク レコーダーがコントロールに対して生成する命令ラベルを決定する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 17711
ms.assetid: 9b75a1e3-cc76-4a2f-ae30-7e5a485b30b1
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b1627ab3b5151c6db228bc21513e6ac97c9cd9f
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093040"
---
# <a name="control-the-text-that-task-recorder-generates-for-a-control"></a><span data-ttu-id="bae65-103">コントロールに対してタスク レコーダーが生成するテキストの制御</span><span class="sxs-lookup"><span data-stu-id="bae65-103">Control the text that Task Recorder generates for a control</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bae65-104">この記事では、タスク レコーダーがコントロールに対して生成する命令ラベルを決定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bae65-104">This article describes how Task recorder determines what instruction label to generate for controls.</span></span> <span data-ttu-id="bae65-105">また、これらのラベルがユーザーにとって意味があることを確認できる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bae65-105">It then explains how you can make sure that these labels are meaningful for the user.</span></span>

<span data-ttu-id="bae65-106">タスク ガイド、Microsoft Word 文書、およびヘルプ コンテンツは、可読性のためにコンテンツ作成標準に適合するように、すべてのコントロールには有用で意味のある指示ラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="bae65-106">Every control must have useful and meaningful instruction labels, so that the task guide, Microsoft Word document, and Help content meet Content Publishing standards for readability.</span></span> <span data-ttu-id="bae65-107">最初に、次の 2 つの項目を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bae65-107">We must first define two terms:</span></span>

-   <span data-ttu-id="bae65-108">**コントロール ラベル** - コントロールのラベル プロパティから取得される値です。</span><span class="sxs-lookup"><span data-stu-id="bae65-108">**Control label** – The value that comes from the label property on the control.</span></span>
-   <span data-ttu-id="bae65-109">**命令ラベル** – コントロールがそのコントロールの使用方法について記述する際にタスク レコーダーに指示するラベル (「OK をクリック」、「ファーストネームフィールドに「John」と入力します」など)。</span><span class="sxs-lookup"><span data-stu-id="bae65-109">**Instruction label** – The label that a control instructs Task recorder to use when it's describing how to use that control (for example, “Click OK” or “In the First name field, enter ‘John’”).</span></span>

<span data-ttu-id="bae65-110">コントロールがタスク レコーダーにイベントを記録するとき、次の 3 つの方法を使用して、ユーザーに表示される命令ラベルを決定できます。</span><span class="sxs-lookup"><span data-stu-id="bae65-110">When a control logs an event to Task recorder, three methods can be used to determine the instruction label that is shown to the user:</span></span>

-   <span data-ttu-id="bae65-111">タスク レコーダー イベントのログの一部として、コントロールは使用する正確な命令ラベル ID を指定することがあります。</span><span class="sxs-lookup"><span data-stu-id="bae65-111">As part of logging the Task recorder event, the control might specify an exact instruction label ID to use.</span></span> <span data-ttu-id="bae65-112">ベスト プラクティスとして、ラベル ID に名前を付ける方法は以下のとおりです。\[クライアント コントロール タイプ名\]\_\[プロパティまたはコマンド名\]指示ラベル ID の手動仕様については、この記事の後半のコード例を参照してください (**OptionalInstructionLabelIDOverride**)。</span><span class="sxs-lookup"><span data-stu-id="bae65-112">As a best practice, here is how label IDs should be named: \[client control type name\]\_\[property or command name\] For manual specification of an instruction label ID, see the code example later in this article (**OptionalInstructionLabelIDOverride**).</span></span>
-   <span data-ttu-id="bae65-113">コントロールが命令ラベル ID を明示的に指定していない場合、Task Recorder は SysTaskRecorderLabel ファイルを参照して、次の命名構文に適合する既存の命令ラベル ID を検索しようとします: \[client control type name\]\_\[property or command name\]。このタイプの命令ラベル ID が見つかった場合、タスク レコーダーはそれを使用します。</span><span class="sxs-lookup"><span data-stu-id="bae65-113">If the control doesn't explicitly specify an instruction label ID, Task recorder looks in the SysTaskRecorderLabel file to try to find an existing instruction label ID that fits the following naming syntax: \[client control type name\]\_\[property or command name\] If an instruction label ID of this type is found, Task recorder uses it.</span></span>
-   <span data-ttu-id="bae65-114">ラベルが、上記の方法を使用して特定できない場合、タスク レコーダは、より汎用的な指示ラベルに転用されます。</span><span class="sxs-lookup"><span data-stu-id="bae65-114">If a label can't be determined by using the preceding methods, Task recorder falls back to a more general-purpose instruction label.</span></span> <span data-ttu-id="bae65-115">一般的な指示ラベルは、SysTaskRecorder ラベル ファイルにあります。</span><span class="sxs-lookup"><span data-stu-id="bae65-115">The general purpose instruction labels are in the SysTaskRecorder label file.</span></span> <span data-ttu-id="bae65-116">コマンド用の汎用命令ラベルが 1つ とプロパティ用の汎用命令ラベルがもう 1 つあります。</span><span class="sxs-lookup"><span data-stu-id="bae65-116">There is one general-purpose instruction label for commands and another for properties.</span></span>
    -   <span data-ttu-id="bae65-117">コマンドの一般的な指示ラベルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="bae65-117">Here is the general purpose instruction label for commands:</span></span>
        -   <span data-ttu-id="bae65-118">**ラベル ID:** CommandUserAction</span><span class="sxs-lookup"><span data-stu-id="bae65-118">**Label ID:** CommandUserAction</span></span>
        -   <span data-ttu-id="bae65-119">**ラベル文字列:** %2 %1</span><span class="sxs-lookup"><span data-stu-id="bae65-119">**Label string:** %2 the %1</span></span>
    -   <span data-ttu-id="bae65-120">プロパティの一般的な指示ラベルを次に示します。</span><span class="sxs-lookup"><span data-stu-id="bae65-120">Here is the general purpose instruction label for properties:</span></span>
        -   <span data-ttu-id="bae65-121">**ラベル ID:** PropertySetValue</span><span class="sxs-lookup"><span data-stu-id="bae65-121">**Label ID:** PropertySetValue</span></span>
        -   <span data-ttu-id="bae65-122">**ラベル文字列:** %1 フィールドに %2 と入力する</span><span class="sxs-lookup"><span data-stu-id="bae65-122">**Label string:** In the %1 field, enter %2</span></span>

<span data-ttu-id="bae65-123">タスク レコーダーは、(前の 3 つの方法のいずれかで) 使用する命令ラベルを決定すると、次の引数を使用してそのラベルの文字列の書式設定を行います。</span><span class="sxs-lookup"><span data-stu-id="bae65-123">When Task recorder has determined which instruction label to use (via one of the preceding three methods), it strFormats the label by using the following arguments:</span></span>

-   <span data-ttu-id="bae65-124">**%1** – この引数は、コントロール ラベルです。</span><span class="sxs-lookup"><span data-stu-id="bae65-124">**%1** – This argument is the control label.</span></span> <span data-ttu-id="bae65-125">タスク レコーダーは、対話可能なラベルを調べることによってコントロール ラベルを取得します。</span><span class="sxs-lookup"><span data-stu-id="bae65-125">Task recorder gets the control label by inspecting the label on the intractable.</span></span> <span data-ttu-id="bae65-126">ただし、コントロールはこのラベルを上書きし、個々のラベルを提供します。</span><span class="sxs-lookup"><span data-stu-id="bae65-126">However, a control can override this label and provide its own label.</span></span> <span data-ttu-id="bae65-127">この記事の後半のサンプル コードを参照してください (**OptionalControlLabelOverride**)。</span><span class="sxs-lookup"><span data-stu-id="bae65-127">See the code example later in this article (**OptionalControlLabelOverride**).</span></span>
-   <span data-ttu-id="bae65-128">**%2** – この引数は、値 (プロパティの場合) またはコマンド名 (コマンドの場合) のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="bae65-128">**%2** –  This argument is either the value (for properties) or the command name (for commands).</span></span> <span data-ttu-id="bae65-129">この値は、イベントのロギングの一部として、コントロールがタスク レコーダーに送信した値になります。</span><span class="sxs-lookup"><span data-stu-id="bae65-129">This value will be the value that the control sent to Task recorder as part of logging the event.</span></span> <span data-ttu-id="bae65-130">ただし、生データの値は、エンドユーザーにとって醜いまたは意味がないものです。</span><span class="sxs-lookup"><span data-stu-id="bae65-130">However, the raw data value can be ugly or meaningless to an end user.</span></span> <span data-ttu-id="bae65-131">したがって、コントロールでは、未処理のデータ値の代わりにタスク レコーダーが表示できる値のユーザー フレンドリなバージョンを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="bae65-131">Therefore, a control can also provide a more user-friendly version of the value that Task recorder can display instead of the raw data value.</span></span> <span data-ttu-id="bae65-132">この記事の後半のサンプル コードを参照してください (**OptionalValueLabelOverride**)。</span><span class="sxs-lookup"><span data-stu-id="bae65-132">See the code example later in this article (**OptionalValueLabelOverride**).</span></span>
-   <span data-ttu-id="bae65-133">**%3**–**%5** – これらはコマンド引数であり、めったに使用されません。</span><span class="sxs-lookup"><span data-stu-id="bae65-133">**%3**–**%5** – These are command arguments and are used rarely.</span></span> <span data-ttu-id="bae65-134">ただし、たとえば、グリッドはそれらを使用して行番号を記録します。</span><span class="sxs-lookup"><span data-stu-id="bae65-134">However, grids use them to record the row number, for example.</span></span>

## <a name="case-study"></a><span data-ttu-id="bae65-135">事例研究</span><span class="sxs-lookup"><span data-stu-id="bae65-135">Case study</span></span>
<span data-ttu-id="bae65-136">改善の事例研究のようにチェック ボックス コントロールを使用しましょう。</span><span class="sxs-lookup"><span data-stu-id="bae65-136">Let's use the Checkbox control as a case study for improvement.</span></span> <span data-ttu-id="bae65-137">現在、方法 1 または方法 2 (この記事の前のセクションを参照) のいずれかを介するチェックボックスに対して命令ラベルが指定されていません。</span><span class="sxs-lookup"><span data-stu-id="bae65-137">Currently, an instruction label isn't specified for the Checkbox via either method 1 or method 2 (see the previous section of this article).</span></span> <span data-ttu-id="bae65-138">したがって、代わりに汎用プロパティ命令ラベルが使用されます。</span><span class="sxs-lookup"><span data-stu-id="bae65-138">Therefore, the general-purpose property instruction label is used instead.</span></span> <span data-ttu-id="bae65-139">他のユーザーが、**失敗した場合に情報ログを表示する** という名前のフィールドのチェック ボックスをオンにし記録する場合、現在の出荷タスク レコーダーは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="bae65-139">If someone records selecting the Checkbox for a field that is named **Show infolog on failure**, the Task recorder output currently looks like this:</span></span>


> <span data-ttu-id="bae65-140">失敗時に情報ログ表示フィールドで、True と入力します。</span><span class="sxs-lookup"><span data-stu-id="bae65-140">In the Show infolog on failure field, enter True.</span></span>

<span data-ttu-id="bae65-141">ただし、通常エンド ユーザーは、チェック ボックスを **True** に設定することの意味を理解していない場合があります。</span><span class="sxs-lookup"><span data-stu-id="bae65-141">However, typical end users might not know what it means to set a Checkbox to **True**.</span></span> <span data-ttu-id="bae65-142">したがって、次のようなラベルを生成するためのチェック ボックスの改善が推奨されます。</span><span class="sxs-lookup"><span data-stu-id="bae65-142">Therefore, a suggested improvement is for the Checkbox to produce a label that looks like this:</span></span>

> <span data-ttu-id="bae65-143">失敗時に情報ログ表示をチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="bae65-143">Check Show infolog on failure.</span></span>

<span data-ttu-id="bae65-144">こうした改善を行うには、新しいラベル ID を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bae65-144">To make this improvement, someone must add a new label ID.</span></span> <span data-ttu-id="bae65-145">その後、イベントがメソッド 1 を使用してタスク レコーダーにログオンしているときに、そのユーザーはラベル ID を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bae65-145">That user must then use the label ID when the event is logged to Task recorder by using method 1:</span></span>

-   <span data-ttu-id="bae65-146">**ラベル ID:** Checkbox\_Value</span><span class="sxs-lookup"><span data-stu-id="bae65-146">**Label ID:** Checkbox\_Value</span></span>
-   <span data-ttu-id="bae65-147">**ラベル文字列:** 「%2 %1」</span><span class="sxs-lookup"><span data-stu-id="bae65-147">**Label string:** "%2 %1."</span></span>

<span data-ttu-id="bae65-148">この変更により、次のような出力が生成されます。</span><span class="sxs-lookup"><span data-stu-id="bae65-148">This change produces output that looks like this:</span></span>

> <span data-ttu-id="bae65-149">失敗時に infolog を表示します。</span><span class="sxs-lookup"><span data-stu-id="bae65-149">True Show infolog on failure.</span></span>

<span data-ttu-id="bae65-150">これは見たいものではありません。</span><span class="sxs-lookup"><span data-stu-id="bae65-150">This isn't quite what we want to see.</span></span> <span data-ttu-id="bae65-151">したがって、チェックボックスがプロパティ変更イベントをタスク レコーダーに記録すると、「チェック」または「チェック解除」のいずれかを示す特定の<*値ラベル* を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="bae65-151">Therefore, in addition, when the Checkbox logs the property change event to Task recorder, it should pass in a specific *value label* that says either “Check” or “Uncheck.”</span></span> <span data-ttu-id="bae65-152">コントロールが明示的に値ラベルを指定した場合、タスク レコーダーは記録された生データ値 (この場合は **True** または **False**) の代わりにその値ラベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="bae65-152">If the control explicitly specifies a value label, Task recorder will use that value label instead of the raw data value that was recorded (**True** or **False**, in this case).</span></span> <span data-ttu-id="bae65-153">この記事の後半のサンプル コードを参照してください (**OptionalValueLabelOverride**)。</span><span class="sxs-lookup"><span data-stu-id="bae65-153">See the code example later in this article (**OptionalValueLabelOverride**).</span></span> <span data-ttu-id="bae65-154">ユーザーが新しいラベルを作成し、イベントがタスク レコーダーに記録されたときの値ラベルを指定すると、コントロールは適切なテキスト出力を行います。</span><span class="sxs-lookup"><span data-stu-id="bae65-154">After the user creates the new label and specifies the value label when the event is logged to Task recorder, the control will have suitable text output:</span></span>

> <span data-ttu-id="bae65-155">失敗時に情報ログ表示をチェックしてください。</span><span class="sxs-lookup"><span data-stu-id="bae65-155">Check Show infolog on failure.</span></span>

<span data-ttu-id="bae65-156">最後に、チェック ボックスには、チェック ボックスの「例の値」を使用するため、2 番目の命令ラベルが必要です。</span><span class="sxs-lookup"><span data-stu-id="bae65-156">Finally, the Checkbox should have a second instruction label for “example value” usage of the Checkbox.</span></span> <span data-ttu-id="bae65-157">「値の例」は、タスク レコーダーがユーザーに対して指示ラベルを表示する特別な方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bae65-157">“Example value” represents a special way that Task recorder displays an instruction label to the user.</span></span> <span data-ttu-id="bae65-158">タスク記録の作成者は、タスク ガイドが、ガイドが記録されたときに入力されたものと同じ値を入力することをユーザーに指示するかどうか、またはビジネス要件に固有の独自の値を入力することをユーザーに指示するかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="bae65-158">The author of the task recording can specify whether the task guide should instruct users to enter the same values that were entered when the guide was recorded, or whether the task guide should instruct users to enter their own values that are specific to their business requirements.</span></span> <span data-ttu-id="bae65-159">値指示ラベルの例では、以下のラベル ID 構文が表示されます。\[クライアント コントロール タイプ名\]\_\[プロパティ名\]\_チェックボックス例に対する例。値ラベルは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="bae65-159">Example value instruction labels have the following label ID syntax: \[client control type name\]\_\[property name\]\_Example For the Checkbox example, the value label would look like this:</span></span>

-   <span data-ttu-id="bae65-160">**ラベル ID:** Checkbox\_Value\_Example</span><span class="sxs-lookup"><span data-stu-id="bae65-160">**Label ID:** Checkbox\_Value\_Example</span></span>
-   <span data-ttu-id="bae65-161">**ラベル文字列:** 「%1 フィールドをオンまたはオフにします」。</span><span class="sxs-lookup"><span data-stu-id="bae65-161">**Label string:** “Check or uncheck the %1 field.”</span></span>

<span data-ttu-id="bae65-162">次のコード例は、X++ コントロールによってプロパティ変更イベントがタスク レコーダーに記録される様子を示しています。</span><span class="sxs-lookup"><span data-stu-id="bae65-162">The following code example shows how property change events are logged to Task recorder by an X++ control.</span></span> <span data-ttu-id="bae65-163">C++ カーネル コントロールには、同様のアプリケーション プログラミング インターフェイス (API) が存在します。</span><span class="sxs-lookup"><span data-stu-id="bae65-163">Similar application programming interfaces (APIs) exist for C++ kernel controls.</span></span> <span data-ttu-id="bae65-164">コマンド イベントに、同種の API があります。</span><span class="sxs-lookup"><span data-stu-id="bae65-164">Command events have a similar API.</span></span>

```xpp
[FormPropertyAttribute(FormPropertyKind::Value, #MyPropertyName)]
    public str value(str_value = valueProperty.parmValue())
    {
        if(!prmIsDefault(_value))
        {
            using (var scope = SysTaskRecorder::addPropertyUserAction(#MyPropertyName, this, _value, [OptionalInstructionLabelIDOverride], [OptionalValueLabelOverride], [OptionalControlLabelOverride]))
            {
                // Property set logic goes here
                valueProperty.setValueOrBinding(_value);
            }
        }
    }
```



---
title: iOS および Android 用 Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドの実装
description: このトピックでは、拡張機能を使用してカスタム フィールドを実装するための共通のパターンを示します。
author: KimANelson
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 48854c15e429d51dcf30ea804eb636dee7965443
ms.sourcegitcommit: a356299be9a593990d9948b3a6b754bd058a5b3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/21/2020
ms.locfileid: "3080775"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="1d6fc-103">iOS および Android 用 Microsoft Dynamics 365 Project Timesheet モバイル アプリのカスタム フィールドの実装</span><span class="sxs-lookup"><span data-stu-id="1d6fc-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d6fc-104">このトピックでは、拡張機能を使用してカスタム フィールドを実装するための共通のパターンを示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="1d6fc-105">トピックの対象は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-105">The following topics are covered:</span></span>

- <span data-ttu-id="1d6fc-106">カスタム フィールド フレームワークでサポートされるさまざまなデータ型</span><span class="sxs-lookup"><span data-stu-id="1d6fc-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="1d6fc-107">タイムシート エントリに読み取り専用または編集可能なフィールドを表示し、ユーザーが入力した値をデータベースに再保存する方法</span><span class="sxs-lookup"><span data-stu-id="1d6fc-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="1d6fc-108">タイムシート ヘッダーに読み取り専用フィールドを表示する方法</span><span class="sxs-lookup"><span data-stu-id="1d6fc-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="1d6fc-109">他のカスタム ビジネス ロジックを統合して、フィールドに既定値を入力し、追加の検証を行う方法</span><span class="sxs-lookup"><span data-stu-id="1d6fc-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="1d6fc-110">対象者</span><span class="sxs-lookup"><span data-stu-id="1d6fc-110">Audience</span></span>

<span data-ttu-id="1d6fc-111">このトピックは、Apple iOS および Google Android で利用可能な Microsoft Dynamics 365 Project Timesheet モバイル アプリケーションにカスタムフィールドを統合する開発者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="1d6fc-112">読者が X++ 開発とプロジェクト タイムシート機能をよく使用していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="1d6fc-113">データ契約 – TSTimesheetCustomField X++ クラス</span><span class="sxs-lookup"><span data-stu-id="1d6fc-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="1d6fc-114">**TSTimesheetCustomField** クラスは、X++ データ契約クラスで、タイムシート機能のカスタム フィールドに関する情報を表します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="1d6fc-115">モバイル アプリにカスタム フィールドを表示するために、TSTimesheetDetails データ契約と TSTimesheetEntry データ契約の両方にカスタム フィールド オブジェクトのリストが渡されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="1d6fc-116">**TSTimesheetDetails** - タイムシートのヘッダー契約。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="1d6fc-117">**TSTimesheetEntry** - タイムシートのトランザクション契約。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="1d6fc-118">同じプロジェクト情報と **timesheetLineRecId** 値を持つオブジェクトのグループが 1 つの明細行を構成します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="1d6fc-119">fieldBaseType (タイプ)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="1d6fc-120">**TsTimesheetCustom** オブジェクトの **FieldBaseType** プロパティによって、アプリに表示されるフィールドのタイプが決定されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="1d6fc-121">次の**タイプ**の値がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="1d6fc-122">タイプの値</span><span class="sxs-lookup"><span data-stu-id="1d6fc-122">Types value</span></span> | <span data-ttu-id="1d6fc-123">型</span><span class="sxs-lookup"><span data-stu-id="1d6fc-123">Type</span></span>              | <span data-ttu-id="1d6fc-124">摘要</span><span class="sxs-lookup"><span data-stu-id="1d6fc-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="1d6fc-125">0</span><span class="sxs-lookup"><span data-stu-id="1d6fc-125">0</span></span>           | <span data-ttu-id="1d6fc-126">文字列 (および列挙)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-126">String (and Enum)</span></span> | <span data-ttu-id="1d6fc-127">このフィールドは、テキスト フィールドとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="1d6fc-128">1</span><span class="sxs-lookup"><span data-stu-id="1d6fc-128">1</span></span>           | <span data-ttu-id="1d6fc-129">整数</span><span class="sxs-lookup"><span data-stu-id="1d6fc-129">Integer</span></span>           | <span data-ttu-id="1d6fc-130">この値は、小数点以下を含まない数字として表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="1d6fc-131">2</span><span class="sxs-lookup"><span data-stu-id="1d6fc-131">2</span></span>           | <span data-ttu-id="1d6fc-132">実績</span><span class="sxs-lookup"><span data-stu-id="1d6fc-132">Real</span></span>              | <span data-ttu-id="1d6fc-133">この値は、小数点以下を含む数字として表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="1d6fc-134">アプリで通貨として実数値を表示するには、**fieldExtenededType** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="1d6fc-135">**numberOfDecimals** プロパティを使用し、表示される小数点以下の桁数を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="1d6fc-136">3</span><span class="sxs-lookup"><span data-stu-id="1d6fc-136">3</span></span>           | <span data-ttu-id="1d6fc-137">日</span><span class="sxs-lookup"><span data-stu-id="1d6fc-137">Date</span></span>              | <span data-ttu-id="1d6fc-138">日付の形式は、**ユーザー オプション**の**言語と国/地域の基本設定**の下で指定される、ユーザーの**日付、時刻、および数字の形式**の設定によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="1d6fc-139">4</span><span class="sxs-lookup"><span data-stu-id="1d6fc-139">4</span></span>           | <span data-ttu-id="1d6fc-140">ブール型</span><span class="sxs-lookup"><span data-stu-id="1d6fc-140">Boolean</span></span>           | |
| <span data-ttu-id="1d6fc-141">15</span><span class="sxs-lookup"><span data-stu-id="1d6fc-141">15</span></span>          | <span data-ttu-id="1d6fc-142">GUID</span><span class="sxs-lookup"><span data-stu-id="1d6fc-142">GUID</span></span>              | |
| <span data-ttu-id="1d6fc-143">16</span><span class="sxs-lookup"><span data-stu-id="1d6fc-143">16</span></span>          | <span data-ttu-id="1d6fc-144">Int64</span><span class="sxs-lookup"><span data-stu-id="1d6fc-144">Int64</span></span>             | |

- <span data-ttu-id="1d6fc-145">**stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定されていない場合、自由書式のフィールドがユーザーに提供されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="1d6fc-146">**stringLength** プロパティを使用し、ユーザーが入力できる最大文字列長を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="1d6fc-147">**stringOptions** プロパティが **TSTimesheetCustomField** オブジェクトで指定された場合、これらのリスト要素が、ユーザーがオプション ボタン (ラジオ ボタン) を使用して選択できる唯一の値になります。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="1d6fc-148">この場合、文字列フィールドは、ユーザーの入力を目的とする列挙値として機能します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="1d6fc-149">データベースに値を列挙として保存するには、コマンド チェーンを使用してデータベースに保存する前に、手動で文字列値を列挙値にマップします (このトピックで後述する「TSTimesheetEntryService クラスでコマンド チェーンを使用し、アプリからデータベースにタイムシート エントリを再保存する」のセクションの例を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="1d6fc-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="1d6fc-151">このプロパティを使用して、通貨として実数値の書式設定をすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="1d6fc-152">この方法は、**fieldBaseType** の値が**実数**である場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="1d6fc-153">**TSCustomFieldExtendedType:None** – 書式設定は適用されません。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="1d6fc-154">**TSCustomFieldExtendedType::Currency** – 通貨として値の書式設定します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="1d6fc-155">通貨の書式設定が有効な場合、**stringValue** フィールドを使用してアプリに表示する通貨コードを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="1d6fc-156">値は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-156">The value is a read-only value.</span></span>

    <span data-ttu-id="1d6fc-157">**realValue** フィールドには、データベースに保存する必要のある金額が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="1d6fc-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="1d6fc-159">このプロパティを使用して、カスタム フィールドを必要のあるアプリ内の場所を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="1d6fc-160">**TSCustomFieldSection::Header** – このフィールドはアプリの**詳細を表示**セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="1d6fc-161">これらのフィールドは、常に読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-161">These fields are always read-only.</span></span>
- <span data-ttu-id="1d6fc-162">**TSCustomFieldSection::Line** – このフィールドはタイムシート エントリで最初から用意されている明細行フィールドすべての後に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="1d6fc-163">これらのフィールドは、編集可能または読み取り専用のいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="1d6fc-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="1d6fc-165">このプロパティにより、アプリによって指定される値がデータベースに再保存される時にフィールドを識別します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="1d6fc-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="1d6fc-167">このプロパティにより、アプリによって指定される値がデータベースに再保存される時にフィールドを識別します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="1d6fc-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-168">isEditable (NoYes)</span></span>

<span data-ttu-id="1d6fc-169">このプロパティを**はい**に設定し、ユーザーが編集可能なタイムシート エントリ セクションのフィールドを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="1d6fc-170">このプロパティを**いいえ**に設定し、フィールドを読み取り専用にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="1d6fc-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="1d6fc-172">このプロパティを**はい**に設定し、タイムシート エントリ セクションの必須のフィールドを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="1d6fc-173">label (str)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-173">label (str)</span></span>

<span data-ttu-id="1d6fc-174">このプロパティにより、アプリのフィールドの次に表示されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="1d6fc-175">stringOptions (文字列のリスト)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="1d6fc-176">このプロパティは、**fieldBaseType** が**文字列**に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="1d6fc-177">**stringOptions** が設定されている場合、オプション ボタン (ラジオ ボタン) により選択可能な文字列値は、リストの文字列によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="1d6fc-178">文字列が指定されなかった場合、文字列フィールドの自由書式のテキストが許可されます (このトピックで後述する「TSTimesheetEntryService クラスでコマンド チェーンを使用し、アプリからデータベースにタイムシート エントリを再保存する」のセクションの例を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="1d6fc-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-179">stringLength (int)</span></span>

<span data-ttu-id="1d6fc-180">このプロパティにより、文字列フィールドの長さの最大値を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="1d6fc-181">**fieldBaseType** が**文字列**に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="1d6fc-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="1d6fc-183">このプロパティにより、実数フィールドに表示される小数点以下の桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="1d6fc-184">**fieldBaseType** が**実数**に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="1d6fc-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-185">orderSequence (int)</span></span>

<span data-ttu-id="1d6fc-186">このプロパティにより、複数のカスタム フィールドが指定された場合に、カスタム フィールドがアプリに表示される順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="1d6fc-187">番号が小さいフィールドが最初に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="1d6fc-188">booleanValue (ブール型)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-188">booleanValue (boolean)</span></span>

<span data-ttu-id="1d6fc-189">**ブール型**のタイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドのブール値を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="1d6fc-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-190">guidValue (guid)</span></span>

<span data-ttu-id="1d6fc-191">**GUID** のタイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドのグローバル一意識別子 (GUID) を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="1d6fc-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-192">int64Value (int64)</span></span>

<span data-ttu-id="1d6fc-193">**Int64** タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの int64 値を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="1d6fc-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-194">intValue (int)</span></span>

<span data-ttu-id="1d6fc-195">**Int** タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの int 値を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="1d6fc-196">realValue (実数)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-196">realValue (real)</span></span>

<span data-ttu-id="1d6fc-197">**実数**タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの実数値を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="1d6fc-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-198">stringValue (str)</span></span>

<span data-ttu-id="1d6fc-199">**文字列**タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの文字列値を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="1d6fc-200">通貨として書式設定された**実数**タイプのフィールドにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="1d6fc-201">これらのフィールドについて、このプロパティはアプリに通貨コードを渡すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="1d6fc-202">dateValue (日付)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-202">dateValue (date)</span></span>

<span data-ttu-id="1d6fc-203">**日付**タイプのフィールドの場合、このプロパティはサーバーとアプリの間でフィールドの日付値を渡します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="1d6fc-204">タイムシート エントリ セクションのカスタム フィールドの表示および保存</span><span class="sxs-lookup"><span data-stu-id="1d6fc-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="1d6fc-205">タイムシート エントリを作成するモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="1d6fc-206">「テスト文字列」と呼ばれる「時間エントリ」に最初から用意されているフィールドとカスタム フィールドが、すでに設定されている「2 番目のオプション」の列挙値と共に表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![アプリのテスト文字列のカスタム フィールド](media/timesheet-entry.jpg)



<span data-ttu-id="1d6fc-208">「テスト文字列」のカスタム フィールドで使用可能な列挙オプションのいずれかを選択しているユーザーのモバイル アプリのスクリーンショットは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="1d6fc-209">ラジオ ボタンとして表示されている「1 番目のオプション」と「2 番目のオプション」の 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="1d6fc-210">現在、2 番目のオプションが選択されています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-210">The second option is currently selected.</span></span>

![テスト文字列のカスタム フィールドのオプション ボタン (ラジオ ボタン)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="1d6fc-212">カスタム フィールドが含まれるように TSTimesheetLine テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="1d6fc-213">一般的なシナリオでは、タイムシート エントリ セクションのカスタム フィールドのデータが TSTimesheetLine テーブルに保存されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="1d6fc-214">ただし、他のテーブルは、指定された TSTimesheetTrans レコードに基づいてデータが取得された場合、またはTSTimesheetTransレコードに基づいてデータを取得できる場合、または固有のレコード コンテキストを持たない場合に使用されます (たとえば、プロジェクト パラメーターでフィールドが読み取り専用として設定されている場合です)。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="1d6fc-215">カスタム フィールドには、バッキングのデータベース レコードを持つ必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="1d6fc-216">X++ ロジックに基づいて動的に生成することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="1d6fc-217">この方法は読み取り専用のシナリオで役に立ちます (動的に生成されたカスタム フィールド値の例については、「TSTimesheetDetails クラスでコマンド チェーンを使用し、buildCustomFieldListForHeader メソッドによりタイムシートの詳細を入力する」のセクションを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="1d6fc-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="1d6fc-218">アプリケーション オブジェクト ツリーの Visual Studio のスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="1d6fc-219">TSTimesheetLine テーブルの拡張機能とカスタム フィールドとして追加された TestLineString フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![行文字列](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="1d6fc-221">TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、タイムシート エントリ セクションにフィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="1d6fc-222">このコードにより、アプリのフィールドの表示設定を制御します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="1d6fc-223">たとえば、フィールドのタイプ、ラベル、フィールドが必須であるかどうか、またフィールドが表示されるセクションを制御します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="1d6fc-224">次の例は、時間入力の文字列フィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="1d6fc-225">このフィールドには、**1 番目のオプション**と**2 番目のオプション**の 2 つのオプションがあり、オプション ボタン (ラジオ ボタン) を介して使用可能です。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="1d6fc-226">アプリのフィールドは、TSTimesheetLine テーブルに追加される **TestLineString** フィールドに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="1d6fc-227">**TSTimesheetCustomField::newFromMetatdata()** メソッドを使用して、**fieldBaseType**、**tableName**、**fieldname**、**label**、**isEditable**、**isMandatory**、**stringLength**、および **numberOfDecimals** のカスタム フィールド プロパティの初期化を簡略化することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="1d6fc-228">これらのパラメーターは、必要に応じて手動で設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-228">You can also set these parameters manually, as you prefer.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="1d6fc-229">TSTimesheetEntry クラスの buildCustomFieldListForEntry メソッドのコマンド チェーンを使用して、タイムシート エントリに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="1d6fc-230">**buildCustomFieldListForEntry** メソッドは、モバイル アプリの保存されたタイムシートの明細行に値を入力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="1d6fc-231">TSTimesheetTrans レコードをパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="1d6fc-232">レコードのフィールドを使用して、アプリのカスタム フィールドの値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="1d6fc-233">TSTimesheetEntryService クラスのコマンド チェーンを使用して、アプリからデータベースにタイムシートのエントリを再保存します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="1d6fc-234">通常の方法でデータベースにカスタム フィールドを再保存するには、複数のメソッドを拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="1d6fc-235">**timesheetLineNeedsUpdating** メソッドを使用して、明細行レコードがアプリでユーザーによって変更されたかどうか、およびデータベースに保存する必要があるかどうかを特定します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="1d6fc-236">パフォーマンスが問題にならない場合は、このメソッドを簡略化し、常に **True** を返すようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="1d6fc-237">**populateTimesheetLineFromEntryDuringCreate** および **populateTimesheetLineFromEntryDuringUpdate** メソッドを拡張し、指定された TSTimesheetEntry データ コントラクト レコードから TSTimesheetLine データベース レコードに値を入力できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="1d6fc-238">次の例では、データベース フィールドと入力フィールドの間のマッピングが X++ コードを介して手動で行われる方法に注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="1d6fc-239">**TSTimesheetEntry** オブジェクトにマップされているカスタム フィールドを TSTimesheetLineweek データベース テーブル に再書き込みする必要がある場合、**populateTimesheetWeekFromEntry** メソッドは拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="1d6fc-240">次の例では、ユーザーが未加工の文字列値としてデータベースに選択した **firstOption** または **secondOption** の値を保存します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="1d6fc-241">データベース フィールドが**列挙**タイプのフィールドである場合、これらの値を手動で列挙値にマップし、データベース テーブルの列挙フィールドに保存することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="1d6fc-242">タイムシート ヘッダー セクションのカスタム フィールドの表示</span><span class="sxs-lookup"><span data-stu-id="1d6fc-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="1d6fc-243">ユーザーがタイムシートを表示しているモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="1d6fc-244">「詳細を表示」オプションを表示するために、右上隅にある「詳細情報」ボタンが選択されています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![詳細なコマンドを表示](media/show-more.png)

<span data-ttu-id="1d6fc-246">タイムシートの「詳細」セクションを表示しているモバイル アプリのスクリーンショットを次に示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="1d6fc-247">「このタイムシートの稼動率 (計算されたカスタム フィールド)」と呼ばれるカスタム フィールドがタイムシートのヘッダー セクションに追加されました。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="1d6fc-248">「0.667」の読み取り専用値がカスタム フィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-248">A read-only value of "0.667" is set on the custom field.</span></span>

![詳細セクション](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="1d6fc-250">カスタム フィールドが含まれるように TSTimesheetTable テーブルを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="1d6fc-251">一般的なシナリオでは、ヘッダー セクションのカスタム フィールドのデータが TSTimesheetHeader テーブルから引き出されることがあります。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="1d6fc-252">ただし、他のテーブルは、指定された TSTimesheetTable のレコードに基づいてデータが取得された場合、またはTSTimesheetTransレコードに基づいてデータを取得できる場合、または固有のレコード コンテキストを持たない場合に使用されます (たとえば、プロジェクト パラメーターでフィールドが読み取り専用として設定されている場合です)。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="1d6fc-253">カスタム フィールドには、バッキングのデータベース レコードを持つ必要がないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="1d6fc-254">X++ ロジックに基づいて動的に生成することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="1d6fc-255">次の例はこの方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="1d6fc-256">ヘッダー セクションのフィールドは、アプリでは常に読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="1d6fc-257">TSTimesheetSettings クラスの buildCustomFieldList メソッドのコマンド チェーンを使用して、ヘッダー セクションにフィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="1d6fc-258">このコードにより、アプリのフィールドの表示設定を制御します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="1d6fc-259">たとえば、フィールドのタイプ、ラベル、フィールドが必須であるかどうか、またフィールドが表示されるセクションを制御します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="1d6fc-260">次の例では、アプリのヘッダー セクションに計算された値を表示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-260">The following example shows a computed value in the header section in the app.</span></span>

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="1d6fc-261">TSTimesheetDetails クラスの buildCustomFieldListForHeader メソッドのコマンド チェーンを使用して、タイムシートの詳細を記入します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="1d6fc-262">**buildCustomFieldListForHeader** メソッドは、モバイル アプリのタイムシート ヘッダーの詳細を記入するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="1d6fc-263">TSTimesheetTable レコードをパラメーターとして使用します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="1d6fc-264">レコードのフィールドを使用して、アプリのカスタム フィールドの値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="1d6fc-265">次の例では、データベースから値を読み取ることができません。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="1d6fc-266">代わりに、X++ ロジックを使用して、アプリに表示される計算値を生成します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="1d6fc-267">他のコンフィギュレーションの可能性または機能拡張の機会</span><span class="sxs-lookup"><span data-stu-id="1d6fc-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="1d6fc-268">アプリへの追加検証の追加</span><span class="sxs-lookup"><span data-stu-id="1d6fc-268">Adding additional validation for the app</span></span>

<span data-ttu-id="1d6fc-269">タイムシート機能に対するデータベース レベルでの既存のロジックは、期待どおりに動作します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="1d6fc-270">保存または送信操作の完了を中断して特定のエラー メッセージを表示するために、コマンド チェーン拡張機能を介してコードに**エラーをスロー (「ユーザーへのメッセージ」)** を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="1d6fc-271">便利で拡張可能なメソッドの 3 つの例を示します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="1d6fc-272">タイムシートの明細行に対する保存操作中に TSTimesheetLine テーブルの **validateWrite** が **False** を返す場合、エラー メッセージがモバイル アプリに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="1d6fc-273">アプリでタイムシートの送信中に TSTimesheetTable テーブルの **validateSubmit** が **False** を返す場合、エラー メッセージがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="1d6fc-274">TSTimesheetLine テーブルの**挿入**メソッドの実行中にフィールドを入力するロジック (たとえば、**明細行プロパティ**) も実行されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="1d6fc-275">コンフィギュレーションにより、最初から用意されているフィールドを非表示また読み取り専用としてマーキング</span><span class="sxs-lookup"><span data-stu-id="1d6fc-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="1d6fc-276">プロジェクト パラメーターから、最初から用意されているフィールドをモバイル アプリで読み取り専用または非表示にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="1d6fc-277">**プロジェクト管理と会計パラメーター** ページの**タイムシート** タブで、**モバイル タイムシート** セクションのオプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![プロジェクト パラメーター](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="1d6fc-279">拡張機能を介して選択可能な活動の変更</span><span class="sxs-lookup"><span data-stu-id="1d6fc-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="1d6fc-280">プロジェクトに対して選択可能な活動は、**TsTimesheetProjectService** クラスの **getActivitiesForProject()** および **getActivityQuery()** メソッドを介して入力されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="1d6fc-281">コマンド チェーンを使用してこの動作を変更し、特定のプロジェクトに対して選択可能な活動のビジネス シナリオに一致させることができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="1d6fc-282">タイムシート エントリに既定のプロジェクト カテゴリを入力する</span><span class="sxs-lookup"><span data-stu-id="1d6fc-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="1d6fc-283">タイムシート エントリの既定のプロジェクト カテゴリの入力は、3 つのレベルで発生します。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="1d6fc-284">コマンド チェーンを使用してこれらのレベルのいずれかまたはすべてにおける動作を拡張することにより、目的の動作を実現することができます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="1d6fc-285">次の階層が使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="1d6fc-286">アプリは、プロジェクト リソースからの既定のカテゴリの配置を試みます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="1d6fc-287">この既定のカテゴリは、**TSTimesheetSettingsService** クラスの **getCurrentUserResource** および **getDelegatedResourcesForCurrentUser** メソッドで設定されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="1d6fc-288">プロジェクト リソース レベルで既定のカテゴリが指定されていない場合、アプリはプロジェクト活動からの取得を試みます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="1d6fc-289">この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getActivitiesForProject** メソッドで設定されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="1d6fc-290">プロジェクト活動レベルで既定のカテゴリが指定されていない場合、既定のカテゴリはプロジェクトのパラメーターから取得されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="1d6fc-291">この既定のカテゴリは、**TSTimesheetProjectService** クラスの **getProjectDetailsbyRule** メソッドで設定されます。</span><span class="sxs-lookup"><span data-stu-id="1d6fc-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>

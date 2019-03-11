---
title: Office の統合の概念と機能
description: このトピックでは、Microsoft Office の統合の概念と機能について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25511
ms.assetid: 36ba2da0-ee9b-4f84-b705-751303ccec33
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84822c38ca77afc3bff5a76cc41c4a6fda4b37a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368854"
---
# <a name="office-integration-concepts-and-features"></a><span data-ttu-id="59728-103">Office の統合の概念と機能</span><span class="sxs-lookup"><span data-stu-id="59728-103">Office integration concepts and features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59728-104">このトピックでは、Microsoft Office の統合の概念と機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="59728-104">This topic reviews Microsoft Office integration concepts and features.</span></span> <span data-ttu-id="59728-105">統合はいくつかの技術に依存します。</span><span class="sxs-lookup"><span data-stu-id="59728-105">The integration depends on several technologies:</span></span>

-   <span data-ttu-id="59728-106">Microsoft Azure での作業</span><span class="sxs-lookup"><span data-stu-id="59728-106">Working in Microsoft Azure</span></span>
-   <span data-ttu-id="59728-107">Azure Active Directory (Azure AD) での作業</span><span class="sxs-lookup"><span data-stu-id="59728-107">Working with Azure Active Directory (Azure AD)</span></span>
-   <span data-ttu-id="59728-108">複数のブラウザーで Web クライアントを実行</span><span class="sxs-lookup"><span data-stu-id="59728-108">Running a web client in multiple browsers</span></span>

<span data-ttu-id="59728-109">Microsoft Office の統合機能は、生産的環境を提供し、Office 製品を使用して作業を遂行するユーザーを支援します。</span><span class="sxs-lookup"><span data-stu-id="59728-109">The Microsoft Office integration capabilities provide users with a productive environment that helps them get the job done by using Office products.</span></span>

## <a name="excel-data-connector-add-in"></a><span data-ttu-id="59728-110">Excel Data Connector アドイン</span><span class="sxs-lookup"><span data-stu-id="59728-110">Excel Data Connector add-in</span></span>
<span data-ttu-id="59728-111">Microsoft Excel は、データを変更してすばやく分析することができます。</span><span class="sxs-lookup"><span data-stu-id="59728-111">Microsoft Excel can change and quickly analyze data.</span></span> <span data-ttu-id="59728-112">Excel Data Connector アプリは、公開されたデータ エンティティに作成された Excel ブックおよび OData サービスとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="59728-112">The Excel Data Connector app interacts with Excel workbooks and OData services that are created for publicly exposed data entities.</span></span> <span data-ttu-id="59728-113">Excel Data Connector アドインを使用すると、Excel がユーザー エクスペリエンスのシームレスな部分となることができます。</span><span class="sxs-lookup"><span data-stu-id="59728-113">The Excel Data Connector add-in enables Excel to become a seamless part of the user experience.</span></span> <span data-ttu-id="59728-114">Excel Data Connector アドインは、Office Web アドイン フレームワークを使用して構築されます。</span><span class="sxs-lookup"><span data-stu-id="59728-114">The Excel Data Connector add-in is built by using the Office Web add-ins framework.</span></span> <span data-ttu-id="59728-115">アドインは作業ウィンドウで実行されます。</span><span class="sxs-lookup"><span data-stu-id="59728-115">The add-in runs in a task pane.</span></span> <span data-ttu-id="59728-116">Office Web アドインは、埋め込み Internet Explorer ブラウザー ウィンドウ内で実行される Web アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="59728-116">Office Web Add-ins are web applications that run inside an embedded Internet Explorer browser window.</span></span> 

<span data-ttu-id="59728-117">[![1\_Office](./media/1_office.png)](./media/1_office.png)</span><span class="sxs-lookup"><span data-stu-id="59728-117">[![1\_Office](./media/1_office.png)](./media/1_office.png)</span></span>

### <a name="microsoft-dynamics-ax-2012-architecture-vs-microsoft-dynamics-365-for-finance-and-operations-architecture"></a><span data-ttu-id="59728-118">Microsoft Dynamics AX 2012 のアーキテクチャと Microsoft Dynamics 365 for Finance and Operations のアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="59728-118">Microsoft Dynamics AX 2012 architecture vs. Microsoft Dynamics 365 for Finance and Operations architecture</span></span>

<span data-ttu-id="59728-119">バージョン間にはいくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="59728-119">There are several differences between versions.</span></span> <span data-ttu-id="59728-120">両方で、Excel で実行する軽量のアドインを構築し、アプリケーションに接続するサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="59728-120">For both, we built lightweight add-ins that run in Excel and use services to connect to the application.</span></span>

#### <a name="dynamics-ax-2012"></a><span data-ttu-id="59728-121">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="59728-121">Dynamics AX 2012</span></span>

<span data-ttu-id="59728-122">Excel &gt; VSTO (.NET) Add-in &gt; Windows Communication foundation (WCF) &gt; AOS &gt; AX Services and Tables &gt; AX クエリ エンジン &gt; Database の Active Directory (AD) &gt; AIF SOAP サービスによる認証</span><span class="sxs-lookup"><span data-stu-id="59728-122">Excel &gt; VSTO (.NET) Add-in &gt; Windows Communication foundation (WCF) &gt; Authentication through Active Directory (AD) &gt; AIF SOAP services on the AOS &gt; AX Services and Tables &gt; AX query engine &gt; Database</span></span>

#### <a name="dynamics-365-for-finance-and-operations"></a><span data-ttu-id="59728-123">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="59728-123">Dynamics 365 for Finance and Operations</span></span>

<span data-ttu-id="59728-124">Excel &gt; Office Web Add-in (JS + HTML) &gt; JavaScript OData API (Olingo) &gt; AOS &gt; AX Entities &gt; AX LINQ プロバイダー &gt; AX Database の Azure Active Directory (AAD) &gt; AX OData サービスによる認証</span><span class="sxs-lookup"><span data-stu-id="59728-124">Excel &gt; Office Web Add-in (JS + HTML) &gt; JavaScript OData API (Olingo) &gt; Authentication through Azure Active Directory (AAD) &gt; AX OData services on the AOS &gt; AX Entities &gt; AX LINQ provider &gt; AX Database</span></span>

### <a name="office-add-in-explained"></a><span data-ttu-id="59728-125">Office アドインの説明</span><span class="sxs-lookup"><span data-stu-id="59728-125">Office Add-in explained</span></span>

<span data-ttu-id="59728-126">Excel Data Connector アプリケーションは、ブックの右側にある作業ウィンドウに配置されます。</span><span class="sxs-lookup"><span data-stu-id="59728-126">The Excel Data Connector app is located in a task pane on the right side of a workbook.</span></span> <span data-ttu-id="59728-127">[![2\_Office](./media/2_office.png)](./media/2_office.png) 次の表では、アドインの各部について説明します。</span><span class="sxs-lookup"><span data-stu-id="59728-127">[![2\_Office](./media/2_office.png)](./media/2_office.png) The following table describes the parts of the add-in.</span></span> <span data-ttu-id="59728-128">数値は、前のスクリーンショットの数値に対応しています。</span><span class="sxs-lookup"><span data-stu-id="59728-128">The numbers correspond to the numbers in the preceding screen shot.</span></span>

| <span data-ttu-id="59728-129">数値</span><span class="sxs-lookup"><span data-stu-id="59728-129">Number</span></span> | <span data-ttu-id="59728-130">氏名</span><span class="sxs-lookup"><span data-stu-id="59728-130">Name</span></span>                             | <span data-ttu-id="59728-131">説明</span><span class="sxs-lookup"><span data-stu-id="59728-131">Description</span></span>                                                                                                                                                                                                                                                                          |
|--------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59728-132">1</span><span class="sxs-lookup"><span data-stu-id="59728-132">1</span></span>      | <span data-ttu-id="59728-133">アドイン プライマリ タイトル</span><span class="sxs-lookup"><span data-stu-id="59728-133">Add-in primary title</span></span>             | <span data-ttu-id="59728-134">Office Web アドイン フレームワークに提供されるアドインのタイトル。</span><span class="sxs-lookup"><span data-stu-id="59728-134">The title of the add-in that is provided to the Office Web Add-ins framework.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="59728-135">2</span><span class="sxs-lookup"><span data-stu-id="59728-135">2</span></span>      | <span data-ttu-id="59728-136">アドイン セカンダリ タイトル</span><span class="sxs-lookup"><span data-stu-id="59728-136">Add-in secondary title</span></span>           | <span data-ttu-id="59728-137">アドインによって提供されるアドインのタイトル。</span><span class="sxs-lookup"><span data-stu-id="59728-137">The title of the add-in that is provided by the add-in.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="59728-138">3</span><span class="sxs-lookup"><span data-stu-id="59728-138">3</span></span>      | <span data-ttu-id="59728-139">求人者名</span><span class="sxs-lookup"><span data-stu-id="59728-139">Source name</span></span>                      | <span data-ttu-id="59728-140">選択したデータ テーブルのデータを提供するエンティティのラベル。</span><span class="sxs-lookup"><span data-stu-id="59728-140">The label of the entity that provides data for the selected data table.</span></span> <span data-ttu-id="59728-141">ラベルの上にマウス ポインターを移動すると、対応する名前を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="59728-141">You can hover over the label to see the corresponding name.</span></span>                                                                                                                                                  |
| <span data-ttu-id="59728-142">4</span><span class="sxs-lookup"><span data-stu-id="59728-142">4</span></span>      | <span data-ttu-id="59728-143">フィールド名</span><span class="sxs-lookup"><span data-stu-id="59728-143">Field name</span></span>                       | <span data-ttu-id="59728-144">選択したデータ テーブル列のデータを提供するエンティティのフィールド。</span><span class="sxs-lookup"><span data-stu-id="59728-144">The label of the field that provides data for the selected data table column.</span></span> <span data-ttu-id="59728-145">ラベルの上にマウス ポインターを移動すると、対応する名前とタイプを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="59728-145">You can hover over the label to see the corresponding name and type.</span></span>                                                                                                                                   |
| <span data-ttu-id="59728-146">5</span><span class="sxs-lookup"><span data-stu-id="59728-146">5</span></span>      | <span data-ttu-id="59728-147">[更新] ボタン</span><span class="sxs-lookup"><span data-stu-id="59728-147">Refresh button</span></span>                   | <span data-ttu-id="59728-148">ブックのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="59728-148">Refresh the data in the workbook.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="59728-149">6</span><span class="sxs-lookup"><span data-stu-id="59728-149">6</span></span>      | <span data-ttu-id="59728-150">公開ボタン</span><span class="sxs-lookup"><span data-stu-id="59728-150">Publish button</span></span>                   | <span data-ttu-id="59728-151">ブック内のデータの変更を発行します。</span><span class="sxs-lookup"><span data-stu-id="59728-151">Publish the data changes in the workbook.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="59728-152">7</span><span class="sxs-lookup"><span data-stu-id="59728-152">7</span></span>      | <span data-ttu-id="59728-153">デザイン ボタン</span><span class="sxs-lookup"><span data-stu-id="59728-153">Design button</span></span>                    | <span data-ttu-id="59728-154">デザイン時エクスペリエンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="59728-154">Open the design-time experience.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="59728-155">8</span><span class="sxs-lookup"><span data-stu-id="59728-155">8</span></span>      | <span data-ttu-id="59728-156">ステータス バー</span><span class="sxs-lookup"><span data-stu-id="59728-156">Status bar</span></span>                       | <span data-ttu-id="59728-157">ステータス バーには、一時的な情報のアラートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="59728-157">The status bar provides brief temporary information alerts.</span></span> <span data-ttu-id="59728-158">ステータス バーで表示される情報は、**メッセージ** ダイアログ ボックスでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="59728-158">Information that is appears in the status bar also appears in the **Messages** dialog box.</span></span>                                                                                                                               |
| <span data-ttu-id="59728-159">9</span><span class="sxs-lookup"><span data-stu-id="59728-159">9</span></span>      | <span data-ttu-id="59728-160">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="59728-160">Options button</span></span>                   | <span data-ttu-id="59728-161">**オプション**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="59728-161">Open the **Options** dialog box.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="59728-162">10</span><span class="sxs-lookup"><span data-stu-id="59728-162">10</span></span>     | <span data-ttu-id="59728-163">メッセージ ボタン</span><span class="sxs-lookup"><span data-stu-id="59728-163">Messages button</span></span>                  | <span data-ttu-id="59728-164">プログラムがユーザーに提供する情報メッセージ、警告、およびエラーを表示している**メッセージ**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="59728-164">Open the **Messages** dialog box, which displays the information messages, warnings, and errors that the program provides to the user.</span></span> <span data-ttu-id="59728-165">ユーザーが関心を持つ可能性がある警告またはエラーの数を提供するために、**メッセージ**ボタンの横に番号が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="59728-165">A number sometimes appears next to the **Messages** button to provide a count of the warnings or errors that the user might be interested in.</span></span> |
| <span data-ttu-id="59728-166">11</span><span class="sxs-lookup"><span data-stu-id="59728-166">11</span></span>     | <span data-ttu-id="59728-167">データを含む Excel データ テーブル</span><span class="sxs-lookup"><span data-stu-id="59728-167">Excel data table containing data</span></span> | <span data-ttu-id="59728-168">この列ヘッダーのフィルターとソート コントロールをこのデータで使用できます。</span><span class="sxs-lookup"><span data-stu-id="59728-168">The filter and sort controls in the columns headers can be used on this data.</span></span> <span data-ttu-id="59728-169">データの変更が公開される前にフィルターを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59728-169">The filters must be removed before data changes are published.</span></span>                                                                                                                                         |
| <span data-ttu-id="59728-170">12</span><span class="sxs-lookup"><span data-stu-id="59728-170">12</span></span>     | <span data-ttu-id="59728-171">Office Web アドイン メニュー</span><span class="sxs-lookup"><span data-stu-id="59728-171">Office Web Add-ins menu</span></span>          | <span data-ttu-id="59728-172">Office Web アドイン メニュー ボタンでは、いくつかの標準的なリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="59728-172">The Office Web Add-ins menu button provides several standard links.</span></span> <span data-ttu-id="59728-173">最も重要なリンクは、アドインをリロードするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="59728-173">The most important of the links is used to reload the add-in.</span></span> <span data-ttu-id="59728-174">アドインは、再度読み込まれると、アドインに関連付けられているテーブルに格納されているブックのすべてのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="59728-174">When the add-in is reloaded, it updates all the data for the workbook that is contained in tables that are associated with the add-in.</span></span>             |

### <a name="authentication"></a><span data-ttu-id="59728-175">認証</span><span class="sxs-lookup"><span data-stu-id="59728-175">Authentication</span></span>

<span data-ttu-id="59728-176">OData は、サーバーと同じ認証スタック上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="59728-176">OData sits on the same authentication stack as the server.</span></span> <span data-ttu-id="59728-177">アドインは、OAuth を使用して認証を容易にします。</span><span class="sxs-lookup"><span data-stu-id="59728-177">The add-in uses OAuth to facilitate authentication.</span></span>

### <a name="lookups-and-drop-down-lists"></a><span data-ttu-id="59728-178">ルックアップおよびドロップダウン リスト</span><span class="sxs-lookup"><span data-stu-id="59728-178">Lookups and drop-down lists</span></span>

<span data-ttu-id="59728-179">表のセルをクリックすると、そのセルに関連付けられているルックアップ、列挙ドロップダウン リスト、または日付の選択が、ソースおよびフィールドの情報の下にあるアドイン内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="59728-179">When you click in a table cell, any lookup, enumeration drop-down list, or date picker that is associated with that cell will be shown inside the add-in, underneath the source and field information.</span></span> <span data-ttu-id="59728-180">アドイン内で選択した値は、現在選択したテーブル セルに配置されます。</span><span class="sxs-lookup"><span data-stu-id="59728-180">Any value that you select inside the add-in is put into the currently selected table cell.</span></span>

### <a name="adding-and-deleting-records"></a><span data-ttu-id="59728-181">レコードの追加と削除</span><span class="sxs-lookup"><span data-stu-id="59728-181">Adding and deleting records</span></span>

<span data-ttu-id="59728-182">レコードを追加するには、テーブルのすぐ下の行に入力するか、Tab キーを使用してテーブルの最後の行の最後のセルから移動します。</span><span class="sxs-lookup"><span data-stu-id="59728-182">To add a record, either start typing in a row directly below a table, or use the Tab key to tab away from the last cell of the last row in the table.</span></span> <span data-ttu-id="59728-183">レコードを削除するには、行ラベル (1、2、3、など) をクリックして行を選択し、その行のすべてのセルを削除します。</span><span class="sxs-lookup"><span data-stu-id="59728-183">To delete a record, select the row by clicking the row label (1, 2, 3, and so on), and delete all the cells in that row.</span></span> <span data-ttu-id="59728-184">変更を発行するには、**発行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59728-184">To publish the changes, click **Publish**.</span></span> <span data-ttu-id="59728-185">**メッセージ**ダイアログ ボックスには、追加、編集、および削除されたレコード数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="59728-185">The **Messages** dialog box shows how many records were added, edited, and deleted.</span></span>

## <a name="workbook-designer"></a><span data-ttu-id="59728-186">ブック デザイナー</span><span class="sxs-lookup"><span data-stu-id="59728-186">Workbook Designer</span></span>
<span data-ttu-id="59728-187">**ブック デザイナー** ページを使用すると、エンティティおよび一連のフィールドを含む、編集可能なカスタム エクスポート ブックを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="59728-187">You can use the **Workbook Designer** page to design an editable custom export workbook that contains an entity and a set of fields.</span></span> <span data-ttu-id="59728-188">**ブックブック デザイナー** (**ExportToExcelWorkbookDesigner**)] ページを開くには、**Common&gt;Common&gt;Office統合&gt;Excel ワークブック デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59728-188">To open the **Workbook Designer** (**ExportToExcelWorkbookDesigner**) page, click **Common &gt; Common &gt; Office Integration &gt; Excel workbook designer**.</span></span> <span data-ttu-id="59728-189">データ編集を公開する前に、エンティティのすべてのキー フィールドは Excel テーブルに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59728-189">Before you can publish data edits, all the key fields of the entity must be in the Excel table.</span></span> <span data-ttu-id="59728-190">キー フィールドには、それらの横に鍵の記号があります。</span><span class="sxs-lookup"><span data-stu-id="59728-190">Key fields have a key symbol next to them.</span></span> <span data-ttu-id="59728-191">レコードを正常に作成または更新するには、Excel テーブルにすべての必須フィールドがなければなりません。</span><span class="sxs-lookup"><span data-stu-id="59728-191">To successfully create or update a record, it must have all the mandatory fields in the Excel table.</span></span> <span data-ttu-id="59728-192">必須フィールドには、その横にアスタリスク (\*) があります。</span><span class="sxs-lookup"><span data-stu-id="59728-192">Mandatory fields have an asterisk (\*) next to them.</span></span> 

<span data-ttu-id="59728-193">[![3\_Office](./media/3_office.png)](./media/3_office.png)</span><span class="sxs-lookup"><span data-stu-id="59728-193">[![3\_Office](./media/3_office.png)](./media/3_office.png)</span></span> 

<span data-ttu-id="59728-194">ブックを作成するには、アプリ バーの **ブックの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59728-194">To retrieve the resulting workbook, click **Create workbook** in the app bar.</span></span> 

<span data-ttu-id="59728-195">エンティティが公開するデータを表示するには、**関連するフォームの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="59728-195">Click **View related form** to see the data that the entity exposes.</span></span> <span data-ttu-id="59728-196">このボタンは、**FormRef** プロパティ値を持つエンティティでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="59728-196">This button is only enabled for entities that have a **FormRef** property value.</span></span>

## <a name="export-api"></a><span data-ttu-id="59728-197">API のエクスポート</span><span class="sxs-lookup"><span data-stu-id="59728-197">Export API</span></span>
### <a name="the-open-in-microsoft-office-menu-and-static-exports"></a><span data-ttu-id="59728-198">Microsoft Office で開くメニューと静的なエクスポート</span><span class="sxs-lookup"><span data-stu-id="59728-198">The Open in Microsoft Office menu and static exports</span></span>

<span data-ttu-id="59728-199">**Microsoft Office で開く** メニューは、データ ソースを持つすべてのページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="59728-199">The **Open in Microsoft Office** menu is available on any page that has a data source.</span></span> <span data-ttu-id="59728-200">**Microsoft Office で開く** メニューには、次の 3 種類のオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="59728-200">The **Open in Microsoft Office** menu provides three types of options:</span></span>

-   <span data-ttu-id="59728-201">**Excel で開く**オプションは、現在のページと同じルート データ ソースを共有するエンティティおよびエンティティに基づくテンプレートに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="59728-201">**Open in Excel** options that are automatically added for entities and entity-based templates that share the same root data source as the current page.</span></span> <span data-ttu-id="59728-202">これらのオプションにより、データを Excel に読み込み、それらのエンティティの OData サービスにデータ変更を公開しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="59728-202">These options make it easier to read data into Excel and publish data changes back to the OData services for those entities.</span></span>
-   <span data-ttu-id="59728-203">**Excel で開く**オプションは、エクスポート API を使用して手動で追加します。</span><span class="sxs-lookup"><span data-stu-id="59728-203">**Open in Excel** options that are manually added via the Export API.</span></span> <span data-ttu-id="59728-204">これらのオプションは、カスタム生成のエクスポートまたはカスタム テンプレートのエクスポートとすることができます。</span><span class="sxs-lookup"><span data-stu-id="59728-204">These options can be custom-generated exports or custom template exports.</span></span>
-   <span data-ttu-id="59728-205">**Excel にエクスポート**オプションは、ページ上のすべての表示可能なグリッドに対して自動的に追加されるオプションです。</span><span class="sxs-lookup"><span data-stu-id="59728-205">**Export to Excel** options that are automatically added for all the visible grids on the page.</span></span> <span data-ttu-id="59728-206">これらのオプションは、グリッドからのデータの静的なエクスポートです。</span><span class="sxs-lookup"><span data-stu-id="59728-206">These options are static exports of data from a grid.</span></span>

### <a name="export-api"></a><span data-ttu-id="59728-207">API のエクスポート</span><span class="sxs-lookup"><span data-stu-id="59728-207">Export API</span></span>

<span data-ttu-id="59728-208">エクスポート API は、そのページのカスタム エクスポート オプションを提供するためのページで使用されます。</span><span class="sxs-lookup"><span data-stu-id="59728-208">The Export API is used on a page to provide custom export options for that page.</span></span> <span data-ttu-id="59728-209">エクスポート API は、開発者が次の作業を実行できる 3 つの部分で構成されます。</span><span class="sxs-lookup"><span data-stu-id="59728-209">The Export API consists of three parts that let a developer perform the following tasks:</span></span>

-   <span data-ttu-id="59728-210">ページの **エクスポート** ページに表示されるカスタム エクスポート オプションのセットを提供します。</span><span class="sxs-lookup"><span data-stu-id="59728-210">Provide a set of custom export options that appear on the **Export** menu on a page.</span></span>
-   <span data-ttu-id="59728-211">カスタム生成のエクスポートのためのコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="59728-211">Provide the context for a custom-generated export.</span></span>
-   <span data-ttu-id="59728-212">カスタム テンプレート エクスポートのためのテンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="59728-212">Provide the template for a custom template export.</span></span>

### <a name="custom-generated-exports"></a><span data-ttu-id="59728-213">カスタム生成されたエクスポート</span><span class="sxs-lookup"><span data-stu-id="59728-213">Custom-generated exports</span></span>

<span data-ttu-id="59728-214">カスタム生成のエクスポートを提供するには、ExporttoExcelIGeneratedCustomExport インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="59728-214">To provide a custom-generated export, implement the ExporttoExcelIGeneratedCustomExport interface.</span></span> <span data-ttu-id="59728-215">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-215">Here is an example.</span></span>

    public class FMCustomer extends FormRun implements ExportToExcelIGeneratedCustomExport

<span data-ttu-id="59728-216">**getExportOptions** メソッドを実装し、返されるリストにエクスポート オプションを追加して、エクスポート オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="59728-216">Add an export option by implementing the **getExportOptions** method and adding an export option to the list that is returned.</span></span> <span data-ttu-id="59728-217">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-217">Here is an example.</span></span>

```
    public List getExportOptions()
    {
        List exportOptions = new List(Types::Class); 
        ExportToExcelExportOption exportOption = ExportToExcelExportOption::construct(ExportToExcelExportType::CustomGenerated);
        exportOption.setDisplayNameWithDataEntity(tablestr(FMCustomerEntity));
        exportOptions.addEnd(exportOption); 
        return exportOptions;
    }
```

<span data-ttu-id="59728-218">**ExportToExcelExportOption.id()** メソッドをチェックした後、**getDataEntityContext** メソッドを実装して適切な **exportOption** の **ExportToExcelDataEntityContext** を返すことにより、エクスポート コンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="59728-218">Provide the export context by implementing the **getDataEntityContext** method and returning an **ExportToExcelDataEntityContext** for the appropriate **exportOption** after the **ExportToExcelExportOption.id()** method is checked.</span></span> <span data-ttu-id="59728-219">コンテキストは、生成されるブックに含めるデータ エンティティとフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="59728-219">The context specifies the data entity and fields to include in the workbook that is generated.</span></span> <span data-ttu-id="59728-220">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-220">Here is an example.</span></span> 

```
    public ExportToExcelDataEntityContext getDataEntityContext(ExportToExcelExportOption _exportOption)
    {
        ExportToExcelDataEntityContext context = null;
        if (_exportOption.id() == ExportToExcelExportOption::DefaultId)
        {
            context = ExportToExcelDataEntityContext::construct(tablestr(FMCustomerEntity), tablefieldgroupstr(FMCustomerEntity, AutoReport));
        }
        return context;
    }
```

### <a name="custom-template-exports"></a><span data-ttu-id="59728-221">カスタム テンプレートのエクスポート</span><span class="sxs-lookup"><span data-stu-id="59728-221">Custom template exports</span></span>

<span data-ttu-id="59728-222">カスタム テンプレートのエクスポートを提供するには、**ExportToExcelITemplateCustomExport** インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="59728-222">To provide a custom template export, implement the **ExportToExcelITemplateCustomExport** interface.</span></span> <span data-ttu-id="59728-223">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-223">Here is an example.</span></span>

```
    public class FMRental extends FormRun implements ExportToExcelIGeneratedCustomExport, ExportToExcelITemplateCustomExport
```

<span data-ttu-id="59728-224">**getExportOptions** メソッドを実装し、返されるリストにエクスポート オプションを追加して、エクスポート オプションを追加します。</span><span class="sxs-lookup"><span data-stu-id="59728-224">Add an export option by implementing the **getExportOptions** method and adding an export option to the list that is returned.</span></span> <span data-ttu-id="59728-225">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-225">Here is an example.</span></span>

```
    public List getExportOptions()
    {
        List exportOptions = new List(Types::Class);
        //Other options...
        ExportToExcelExportOption exportOption2 = ExportToExcelExportOption::construct(ExportToExcelExportType::CustomTemplate, int2str(2));
        exportOption2.displayName("Analyze rentals");
        exportOptions.addEnd(exportOption2);        
        return exportOptions;
    }
```

<span data-ttu-id="59728-226">**ExportToExcelExportOption.id** メソッドをチェックした後、**getTemplate** メソッドを実装して適切な **exportOption** の **System.IO.Stream** を返すことにより、エクスポート テンプレートを提供します。</span><span class="sxs-lookup"><span data-stu-id="59728-226">Provide the export template by implementing the **getTemplate** method and returning a **System.IO.Stream** for the appropriate **exportOption** after the **ExportToExcelExportOption.id** method is checked.</span></span> <span data-ttu-id="59728-227">テンプレートは、アプリケーション オブジェクト ツリー (AOT) のリソースとして保存でき、**Microsoft.Dynamics.Ax.Xpp.MetadataSupport::GetResourceContentStream** メソッドを使用して実行時に取得できます。</span><span class="sxs-lookup"><span data-stu-id="59728-227">Templates can be stored as Application Object Tree (AOT) resources and retrieved at run time by using the **Microsoft.Dynamics.Ax.Xpp.MetadataSupport::GetResourceContentStream** method.</span></span> <span data-ttu-id="59728-228">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-228">Here is an example.</span></span>

```
    public System.IO.Stream getTemplate(ExportToExcelExportOption _exportOption)
    {
        System.IO.Stream stream = null;
        if (_exportOption.id() == int2str(2))
        {
            stream = Microsoft.Dynamics.Ax.Xpp.MetadataSupport::GetResourceContentStream(resourcestr(FMRentalEditableExportTemplate));
        }
        return stream;
    }
```

<span data-ttu-id="59728-229">インターフェイスを満たすために **updateTemplateSettings** メソッドを実装する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="59728-229">You must also implement the **updateTemplateSettings** method to satisfy the interface.</span></span> <span data-ttu-id="59728-230">最終的に、このメソッドはフィルタリング情報を提供するために使用されますが、その機能はまだ開発中です。</span><span class="sxs-lookup"><span data-stu-id="59728-230">Eventually, this method will be used to provide filtering information, but that capability is still under development.</span></span> <span data-ttu-id="59728-231">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="59728-231">Here is an example.</span></span>

```
    public void updateTemplateSettings(ExportToExcelExportOption _exportOption, Microsoft.Dynamics.Platform.Integration.Office.ExportToExcelHelper.SettingsEditor _settingsEditor)
    {
    }
```

## <a name="document-management"></a><span data-ttu-id="59728-232">ドキュメント管理</span><span class="sxs-lookup"><span data-stu-id="59728-232">Document management</span></span>
<span data-ttu-id="59728-233">ドキュメントの管理は、Azure Blob storage および SharePoint Online でレコードの添付ファイルの保存をサポートします。</span><span class="sxs-lookup"><span data-stu-id="59728-233">Document management supports saving record attachments in Azure Blob storage and SharePoint Online.</span></span> <span data-ttu-id="59728-234">データベースの記憶域は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="59728-234">Database storage is deprecated.</span></span> <span data-ttu-id="59728-235">ドキュメントはアプリケーションを介してのみアクセスでき、データベースのパフォーマンスに悪影響を及ぼさないストレージを提供できるという利点があるため Azure Blob ストレージは、データベースのストレージと同等です。</span><span class="sxs-lookup"><span data-stu-id="59728-235">Azure Blob storage is equivalent to storage in the database since documents can only be accessed through the application and it provides the added benefit of providing storage that doesn't negatively affect the performance of the database.</span></span> <span data-ttu-id="59728-236">Azure blob storage は既定でありすぐに動作します。</span><span class="sxs-lookup"><span data-stu-id="59728-236">Azure blob storage is the default and works immediately.</span></span> <span data-ttu-id="59728-237">SharePoint テナントは自動的に検出されるため、O365 ライセンスを持っている場合 SharePoint の記憶域がすぐに機能します。例: TenantA.onmicrosoft.com O365/AAD テナントのユーザーは SharePoint サイトとして TenantA.sharepoint.com を取得します。</span><span class="sxs-lookup"><span data-stu-id="59728-237">SharePoint storage will work immediately if you have an O365 license since we auto-discover the SharePoint tenant e.g. a user on the TenantA.onmicrosoft.com O365/AAD tenant gets TenantA.sharepoint.com as the SharePoint site.</span></span> <span data-ttu-id="59728-238">ユーザーがドキュメントの管理が無効になっている場合、それを有効にするには、**オプション &gt; 一般 &gt; その他**をクリックし、**ドキュメント処理の有効オプション**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="59728-238">If document management has been turned off by the user, turn it on by clicking **Options &gt; General &gt; Miscellaneous** and setting **Document handling active** to **Yes**.</span></span> 

<span data-ttu-id="59728-239">[![4\_Office](./media/4_office.png)](./media/4_office.png)</span><span class="sxs-lookup"><span data-stu-id="59728-239">[![4\_Office](./media/4_office.png)](./media/4_office.png)</span></span> 

<span data-ttu-id="59728-240">データを持つページでは、**添付**ボタンが右上隅に表示されます。</span><span class="sxs-lookup"><span data-stu-id="59728-240">On any page that has data, an **Attach** button will be available in the upper-right corner.</span></span> 

<span data-ttu-id="59728-241">[![5\_Office](./media/5_office.png)](./media/5_office.png)</span><span class="sxs-lookup"><span data-stu-id="59728-241">[![5\_Office](./media/5_office.png)](./media/5_office.png)</span></span> 

<span data-ttu-id="59728-242">**添付ファイル** ページには、前のページで選択したレコードに関連付けられている添付ファイル (ドキュメント) のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="59728-242">The **Attachments** page provides a view of the attachments (documents) that are associated with the record that was selected on the previous page.</span></span> <span data-ttu-id="59728-243">アプリ バーの **新規** ボタン (**+**) をクリックすると、レコードに新しいアタッチメントを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="59728-243">You can add new attachments to the record by clicking the **New** button (**+**) in the app bar.</span></span> <span data-ttu-id="59728-244">**ファイル**および**画像**ドキュメント タイプについては、関連ファイルを提供するように求められます。</span><span class="sxs-lookup"><span data-stu-id="59728-244">For the **File** and **Image** document types, you will be prompted to provide the associated file.</span></span>

### <a name="document-preview"></a><span data-ttu-id="59728-245">ドキュメントのプレビュー</span><span class="sxs-lookup"><span data-stu-id="59728-245">Document preview</span></span>

<span data-ttu-id="59728-246">サポート対象のファイルの種類のプレビューは、**プレビュー**クイック タブで提供されます。</span><span class="sxs-lookup"><span data-stu-id="59728-246">A preview for supported file types is provided on the **Preview** FastTab.</span></span> <span data-ttu-id="59728-247">PNG イメージやテキスト ファイルなどの基本的なドキュメント タイプは、既定でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="59728-247">Basic document types, such as PNG images and text files, are supported by default.</span></span> <span data-ttu-id="59728-248">Microsoft Word、Excel、および PowerPoint ファイルなどの Office ドキュメント タイプは、実稼動 Office Web Apps サーバーを使用する必要があり、OneBox コンフィギュレーションを利用できない場合もあます。</span><span class="sxs-lookup"><span data-stu-id="59728-248">Office document types, such as Microsoft Word, Excel, and PowerPoint files, must use a production Office Web Apps Server, which might not be available in a OneBox configuration.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="59728-249">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="59728-249">Frequently asked questions</span></span>

### <a name="office-licensing"></a><span data-ttu-id="59728-250">Office ライセンス</span><span class="sxs-lookup"><span data-stu-id="59728-250">Office Licensing</span></span>

#### <a name="what-office-365-licenses-are-available"></a><span data-ttu-id="59728-251">どのような Office 365 ライセンスがありますか ?</span><span class="sxs-lookup"><span data-stu-id="59728-251">What Office 365 licenses are available?</span></span>

<span data-ttu-id="59728-252">「[Office 365 ライセンス オプション](https://products.office.com/en-us/business/compare-office-365-for-business-plans)」が多数あります。</span><span class="sxs-lookup"><span data-stu-id="59728-252">There are lots of [Office 365 license options](https://products.office.com/en-us/business/compare-office-365-for-business-plans).</span></span> <span data-ttu-id="59728-253">所属されている組織にとって、意味のあるライセンスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="59728-253">You should select the license that makes sense for your organization.</span></span>

#### <a name="after-purchasing-an-office-365-license-what-needs-to-be-done-to-set-up-sharepoint-storage-for-attachments"></a><span data-ttu-id="59728-254">Office 365 のライセンスを購入した後、添付ファイル用に SharePoint ストレージを設定するために何を行う必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="59728-254">After purchasing an Office 365 license, what needs to be done to set up SharePoint storage for attachments?</span></span>

<span data-ttu-id="59728-255">ドキュメント パラメーター フォームを開いて、SharePoint サーバーが自動的に検出および設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="59728-255">Open the Document Parameters form and ensure that the SharePoint server has been automatically discovered and set.</span></span> <span data-ttu-id="59728-256">ここで、ドキュメント タイプを開くか作成し、"SharePoint" へのドキュメント タイプの場所を設定し、ファイルを保存する必要があるフォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="59728-256">Now open or create a Document Type, set the Document Type's location to "SharePoint" and select the folder that the files should be stored in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59728-257">追加リソース</span><span class="sxs-lookup"><span data-stu-id="59728-257">Additional resources</span></span>

[<span data-ttu-id="59728-258">Office 統合ラボとチュートリアル</span><span class="sxs-lookup"><span data-stu-id="59728-258">Office Integration lab and walkthroughs</span></span>](office-integration-tutorial.md)

[<span data-ttu-id="59728-259">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="59728-259">Office Integration Troubleshooting</span></span>](office-integration-troubleshooting.md)

[<span data-ttu-id="59728-260">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="59728-260">Application stack and server architecture</span></span>](../dev-tools/application-stack-server-architecture.md)

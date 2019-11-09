---
title: オフィス統合の概要
description: このトピックでは、Microsoft Office の統合の概念と機能について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25511
ms.assetid: 36ba2da0-ee9b-4f84-b705-751303ccec33
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78fc5a86b9e827b13a71d173e551d7041fa74c0d
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578269"
---
# <a name="office-integration-overview"></a><span data-ttu-id="49f9b-103">オフィス統合の概要</span><span class="sxs-lookup"><span data-stu-id="49f9b-103">Office integration overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49f9b-104">このトピックでは、Microsoft Office の統合の概念と機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-104">This topic reviews Microsoft Office integration concepts and features.</span></span> <span data-ttu-id="49f9b-105">統合はいくつかの技術に依存します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-105">The integration depends on several technologies:</span></span>

-   <span data-ttu-id="49f9b-106">Microsoft Azure での作業</span><span class="sxs-lookup"><span data-stu-id="49f9b-106">Working in Microsoft Azure</span></span>
-   <span data-ttu-id="49f9b-107">Azure Active Directory (Azure AD) での作業</span><span class="sxs-lookup"><span data-stu-id="49f9b-107">Working with Azure Active Directory (Azure AD)</span></span>
-   <span data-ttu-id="49f9b-108">複数のブラウザーで Web クライアントを実行</span><span class="sxs-lookup"><span data-stu-id="49f9b-108">Running a web client in multiple browsers</span></span>

<span data-ttu-id="49f9b-109">Microsoft Office の統合機能は、生産的環境を提供し、Office 製品を使用して作業を遂行するユーザーを支援します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-109">The Microsoft Office integration capabilities provide users with a productive environment that helps them get the job done by using Office products.</span></span>

## <a name="excel-data-connector-add-in"></a><span data-ttu-id="49f9b-110">Excel Data Connector アドイン</span><span class="sxs-lookup"><span data-stu-id="49f9b-110">Excel Data Connector add-in</span></span>
<span data-ttu-id="49f9b-111">Microsoft Excel は、データを変更してすばやく分析することができます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-111">Microsoft Excel can change and quickly analyze data.</span></span> <span data-ttu-id="49f9b-112">Excel Data Connector アプリは、公開されたデータ エンティティに作成された Excel ブックおよび OData サービスとやり取りします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-112">The Excel Data Connector app interacts with Excel workbooks and OData services that are created for publicly exposed data entities.</span></span> <span data-ttu-id="49f9b-113">Excel Data Connector アドインを使用すると、Excel がユーザー エクスペリエンスのシームレスな部分となることができます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-113">The Excel Data Connector add-in enables Excel to become a seamless part of the user experience.</span></span> <span data-ttu-id="49f9b-114">Excel Data Connector アドインは、Office Web アドイン フレームワークを使用して構築されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-114">The Excel Data Connector add-in is built by using the Office Web add-ins framework.</span></span> <span data-ttu-id="49f9b-115">アドインは作業ウィンドウで実行されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-115">The add-in runs in a task pane.</span></span> <span data-ttu-id="49f9b-116">Office Web アドインは、埋め込み Internet Explorer ブラウザー ウィンドウ内で実行される Web アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="49f9b-116">Office Web Add-ins are web applications that run inside an embedded Internet Explorer browser window.</span></span> 

<span data-ttu-id="49f9b-117">[![Excel データ コネクタ アプリのスクリーン ショット](./media/1_office.png)](./media/1_office.png)</span><span class="sxs-lookup"><span data-stu-id="49f9b-117">[![Screen shot of Excel Data Connector app](./media/1_office.png)](./media/1_office.png)</span></span>

### <a name="dynamics-ax-2012-architecture-vs-finance-and-operations-architecture"></a><span data-ttu-id="49f9b-118">Dynamics AX 2012 アーキテクチャ 対 Finance and Operations アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="49f9b-118">Dynamics AX 2012 architecture vs. Finance and Operations architecture</span></span>

<span data-ttu-id="49f9b-119">バージョン間にはいくつかの違いがあります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-119">There are several differences between versions.</span></span> <span data-ttu-id="49f9b-120">両方で、Excel で実行する軽量のアドインを構築し、アプリケーションに接続するサービスを使用します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-120">For both, we built lightweight add-ins that run in Excel and use services to connect to the application.</span></span>

#### <a name="dynamics-ax-2012"></a><span data-ttu-id="49f9b-121">Dynamics AX 2012</span><span class="sxs-lookup"><span data-stu-id="49f9b-121">Dynamics AX 2012</span></span>

<span data-ttu-id="49f9b-122">Excel &gt; VSTO (.NET) Add-in &gt; Windows Communication foundation (WCF) &gt; AOS &gt; AX Services and Tables &gt; AX クエリ エンジン &gt; Database の Active Directory (AD) &gt; AIF SOAP サービスによる認証</span><span class="sxs-lookup"><span data-stu-id="49f9b-122">Excel &gt; VSTO (.NET) Add-in &gt; Windows Communication foundation (WCF) &gt; Authentication through Active Directory (AD) &gt; AIF SOAP services on the AOS &gt; AX Services and Tables &gt; AX query engine &gt; Database</span></span>

#### <a name="finance-and-operations"></a><span data-ttu-id="49f9b-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="49f9b-123">Finance and Operations</span></span>

<span data-ttu-id="49f9b-124">Excel &gt; Office Web Add-in (JS + HTML) &gt; JavaScript OData API (Olingo) &gt; AOS &gt; AX Entities &gt; AX LINQ プロバイダー &gt; AX Database の Azure Active Directory (AAD) &gt; AX OData サービスによる認証</span><span class="sxs-lookup"><span data-stu-id="49f9b-124">Excel &gt; Office Web Add-in (JS + HTML) &gt; JavaScript OData API (Olingo) &gt; Authentication through Azure Active Directory (AAD) &gt; AX OData services on the AOS &gt; AX Entities &gt; AX LINQ provider &gt; AX Database</span></span>

### <a name="office-add-in-explained"></a><span data-ttu-id="49f9b-125">Office アドインの説明</span><span class="sxs-lookup"><span data-stu-id="49f9b-125">Office Add-in explained</span></span>

<span data-ttu-id="49f9b-126">Excel Data Connector アプリケーションは、ブックの右側にある作業ウィンドウに配置されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-126">The Excel Data Connector app is located in a task pane on the right side of a workbook.</span></span> <span data-ttu-id="49f9b-127">[![テーブルに対応する番号付き要素による Excel データ コネクターの場所を表示するスクリーン ショット](./media/2_office.png)](./media/2_office.png) 次の表で、アドインの各部について説明します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-127">[![Screen shot showing location of Excel Data Connector app with numbered elements corresponding to table](./media/2_office.png)](./media/2_office.png) The following table describes the parts of the add-in.</span></span> <span data-ttu-id="49f9b-128">数値は、前のスクリーンショットの数値に対応しています。</span><span class="sxs-lookup"><span data-stu-id="49f9b-128">The numbers correspond to the numbers in the preceding screen shot.</span></span>

| <span data-ttu-id="49f9b-129">数値</span><span class="sxs-lookup"><span data-stu-id="49f9b-129">Number</span></span> | <span data-ttu-id="49f9b-130">氏名</span><span class="sxs-lookup"><span data-stu-id="49f9b-130">Name</span></span>                             | <span data-ttu-id="49f9b-131">説明</span><span class="sxs-lookup"><span data-stu-id="49f9b-131">Description</span></span>                                                                                                                                                                                                                                                                          |
|--------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49f9b-132">1</span><span class="sxs-lookup"><span data-stu-id="49f9b-132">1</span></span>      | <span data-ttu-id="49f9b-133">アドイン プライマリ タイトル</span><span class="sxs-lookup"><span data-stu-id="49f9b-133">Add-in primary title</span></span>             | <span data-ttu-id="49f9b-134">Office Web アドイン フレームワークに提供されるアドインのタイトル。</span><span class="sxs-lookup"><span data-stu-id="49f9b-134">The title of the add-in that is provided to the Office Web Add-ins framework.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="49f9b-135">2</span><span class="sxs-lookup"><span data-stu-id="49f9b-135">2</span></span>      | <span data-ttu-id="49f9b-136">アドイン セカンダリ タイトル</span><span class="sxs-lookup"><span data-stu-id="49f9b-136">Add-in secondary title</span></span>           | <span data-ttu-id="49f9b-137">アドインによって提供されるアドインのタイトル。</span><span class="sxs-lookup"><span data-stu-id="49f9b-137">The title of the add-in that is provided by the add-in.</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="49f9b-138">3</span><span class="sxs-lookup"><span data-stu-id="49f9b-138">3</span></span>      | <span data-ttu-id="49f9b-139">求人者名</span><span class="sxs-lookup"><span data-stu-id="49f9b-139">Source name</span></span>                      | <span data-ttu-id="49f9b-140">選択したデータ テーブルのデータを提供するエンティティのラベル。</span><span class="sxs-lookup"><span data-stu-id="49f9b-140">The label of the entity that provides data for the selected data table.</span></span> <span data-ttu-id="49f9b-141">ラベルの上にマウス ポインターを移動すると、対応する名前を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-141">You can hover over the label to see the corresponding name.</span></span>                                                                                                                                                  |
| <span data-ttu-id="49f9b-142">4</span><span class="sxs-lookup"><span data-stu-id="49f9b-142">4</span></span>      | <span data-ttu-id="49f9b-143">フィールド名</span><span class="sxs-lookup"><span data-stu-id="49f9b-143">Field name</span></span>                       | <span data-ttu-id="49f9b-144">選択したデータ テーブル列のデータを提供するエンティティのフィールド。</span><span class="sxs-lookup"><span data-stu-id="49f9b-144">The label of the field that provides data for the selected data table column.</span></span> <span data-ttu-id="49f9b-145">ラベルの上にマウス ポインターを移動すると、対応する名前とタイプを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-145">You can hover over the label to see the corresponding name and type.</span></span>                                                                                                                                   |
| <span data-ttu-id="49f9b-146">5</span><span class="sxs-lookup"><span data-stu-id="49f9b-146">5</span></span>      | <span data-ttu-id="49f9b-147">[更新] ボタン</span><span class="sxs-lookup"><span data-stu-id="49f9b-147">Refresh button</span></span>                   | <span data-ttu-id="49f9b-148">ブックのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-148">Refresh the data in the workbook.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="49f9b-149">6</span><span class="sxs-lookup"><span data-stu-id="49f9b-149">6</span></span>      | <span data-ttu-id="49f9b-150">公開ボタン</span><span class="sxs-lookup"><span data-stu-id="49f9b-150">Publish button</span></span>                   | <span data-ttu-id="49f9b-151">ブック内のデータの変更を発行します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-151">Publish the data changes in the workbook.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="49f9b-152">7</span><span class="sxs-lookup"><span data-stu-id="49f9b-152">7</span></span>      | <span data-ttu-id="49f9b-153">デザイン ボタン</span><span class="sxs-lookup"><span data-stu-id="49f9b-153">Design button</span></span>                    | <span data-ttu-id="49f9b-154">デザイン時エクスペリエンスを開きます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-154">Open the design-time experience.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="49f9b-155">8</span><span class="sxs-lookup"><span data-stu-id="49f9b-155">8</span></span>      | <span data-ttu-id="49f9b-156">ステータス バー</span><span class="sxs-lookup"><span data-stu-id="49f9b-156">Status bar</span></span>                       | <span data-ttu-id="49f9b-157">ステータス バーには、一時的な情報のアラートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-157">The status bar provides brief temporary information alerts.</span></span> <span data-ttu-id="49f9b-158">ステータス バーで表示される情報は、**メッセージ** ダイアログ ボックスでも表示されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-158">Information that is appears in the status bar also appears in the **Messages** dialog box.</span></span>                                                                                                                               |
| <span data-ttu-id="49f9b-159">9</span><span class="sxs-lookup"><span data-stu-id="49f9b-159">9</span></span>      | <span data-ttu-id="49f9b-160">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="49f9b-160">Options button</span></span>                   | <span data-ttu-id="49f9b-161">**オプション**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-161">Open the **Options** dialog box.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="49f9b-162">10</span><span class="sxs-lookup"><span data-stu-id="49f9b-162">10</span></span>     | <span data-ttu-id="49f9b-163">メッセージ ボタン</span><span class="sxs-lookup"><span data-stu-id="49f9b-163">Messages button</span></span>                  | <span data-ttu-id="49f9b-164">プログラムがユーザーに提供する情報メッセージ、警告、およびエラーを表示している**メッセージ**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-164">Open the **Messages** dialog box, which displays the information messages, warnings, and errors that the program provides to the user.</span></span> <span data-ttu-id="49f9b-165">ユーザーが関心を持つ可能性がある警告またはエラーの数を提供するために、**メッセージ**ボタンの横に番号が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-165">A number sometimes appears next to the **Messages** button to provide a count of the warnings or errors that the user might be interested in.</span></span> |
| <span data-ttu-id="49f9b-166">11</span><span class="sxs-lookup"><span data-stu-id="49f9b-166">11</span></span>     | <span data-ttu-id="49f9b-167">データを含む Excel データ テーブル</span><span class="sxs-lookup"><span data-stu-id="49f9b-167">Excel data table containing data</span></span> | <span data-ttu-id="49f9b-168">この列ヘッダーのフィルターとソート コントロールをこのデータで使用できます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-168">The filter and sort controls in the columns headers can be used on this data.</span></span> <span data-ttu-id="49f9b-169">データの変更が公開される前にフィルターを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-169">The filters must be removed before data changes are published.</span></span>                                                                                                                                         |
| <span data-ttu-id="49f9b-170">12</span><span class="sxs-lookup"><span data-stu-id="49f9b-170">12</span></span>     | <span data-ttu-id="49f9b-171">Office Web アドイン メニュー</span><span class="sxs-lookup"><span data-stu-id="49f9b-171">Office Web Add-ins menu</span></span>          | <span data-ttu-id="49f9b-172">Office Web アドイン メニュー ボタンでは、いくつかの標準的なリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-172">The Office Web Add-ins menu button provides several standard links.</span></span> <span data-ttu-id="49f9b-173">最も重要なリンクは、アドインをリロードするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-173">The most important of the links is used to reload the add-in.</span></span> <span data-ttu-id="49f9b-174">アドインは、再度読み込まれると、アドインに関連付けられているテーブルに格納されているブックのすべてのデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-174">When the add-in is reloaded, it updates all the data for the workbook that is contained in tables that are associated with the add-in.</span></span>             |

### <a name="authentication"></a><span data-ttu-id="49f9b-175">認証</span><span class="sxs-lookup"><span data-stu-id="49f9b-175">Authentication</span></span>

<span data-ttu-id="49f9b-176">OData は、サーバーと同じ認証スタック上に配置されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-176">OData sits on the same authentication stack as the server.</span></span> <span data-ttu-id="49f9b-177">アドインは、OAuth を使用して認証を容易にします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-177">The add-in uses OAuth to facilitate authentication.</span></span>

### <a name="lookups-and-drop-down-lists"></a><span data-ttu-id="49f9b-178">ルックアップおよびドロップダウン リスト</span><span class="sxs-lookup"><span data-stu-id="49f9b-178">Lookups and drop-down lists</span></span>

<span data-ttu-id="49f9b-179">表のセルをクリックすると、そのセルに関連付けられているルックアップ、列挙ドロップダウン リスト、または日付の選択が、ソースおよびフィールドの情報の下にあるアドイン内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-179">When you click in a table cell, any lookup, enumeration drop-down list, or date picker that is associated with that cell will be shown inside the add-in, underneath the source and field information.</span></span> <span data-ttu-id="49f9b-180">アドイン内で選択した値は、現在選択したテーブル セルに配置されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-180">Any value that you select inside the add-in is put into the currently selected table cell.</span></span>

### <a name="adding-and-deleting-records"></a><span data-ttu-id="49f9b-181">レコードの追加と削除</span><span class="sxs-lookup"><span data-stu-id="49f9b-181">Adding and deleting records</span></span>

<span data-ttu-id="49f9b-182">レコードを追加するには、テーブルのすぐ下の行に入力するか、Tab キーを使用してテーブルの最後の行の最後のセルから移動します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-182">To add a record, either start typing in a row directly below a table, or use the Tab key to tab away from the last cell of the last row in the table.</span></span> <span data-ttu-id="49f9b-183">レコードを削除するには、行ラベル (1、2、3、など) をクリックして行を選択し、その行のすべてのセルを削除します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-183">To delete a record, select the row by clicking the row label (1, 2, 3, and so on), and delete all the cells in that row.</span></span> <span data-ttu-id="49f9b-184">変更を発行するには、**発行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-184">To publish the changes, click **Publish**.</span></span> <span data-ttu-id="49f9b-185">**メッセージ**ダイアログ ボックスには、追加、編集、および削除されたレコード数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-185">The **Messages** dialog box shows how many records were added, edited, and deleted.</span></span>

## <a name="workbook-designer"></a><span data-ttu-id="49f9b-186">ブック デザイナー</span><span class="sxs-lookup"><span data-stu-id="49f9b-186">Workbook Designer</span></span>
<span data-ttu-id="49f9b-187">**ブック デザイナー** ページを使用すると、エンティティおよび一連のフィールドを含む、編集可能なカスタム エクスポート ブックを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-187">You can use the **Workbook Designer** page to design an editable custom export workbook that contains an entity and a set of fields.</span></span> <span data-ttu-id="49f9b-188">**ブックブック デザイナー** (**ExportToExcelWorkbookDesigner**)] ページを開くには、**Common&gt;Common&gt;Office統合&gt;Excel ワークブック デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-188">To open the **Workbook Designer** (**ExportToExcelWorkbookDesigner**) page, click **Common &gt; Common &gt; Office Integration &gt; Excel workbook designer**.</span></span> <span data-ttu-id="49f9b-189">データ編集を公開する前に、エンティティのすべてのキー フィールドは Excel テーブルに存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-189">Before you can publish data edits, all the key fields of the entity must be in the Excel table.</span></span> <span data-ttu-id="49f9b-190">キー フィールドには、それらの横に鍵の記号があります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-190">Key fields have a key symbol next to them.</span></span> <span data-ttu-id="49f9b-191">レコードを正常に作成または更新するには、Excel テーブルにすべての必須フィールドがなければなりません。</span><span class="sxs-lookup"><span data-stu-id="49f9b-191">To successfully create or update a record, it must have all the mandatory fields in the Excel table.</span></span> <span data-ttu-id="49f9b-192">必須フィールドには、その横にアスタリスク (\*) があります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-192">Mandatory fields have an asterisk (\*) next to them.</span></span> 

<span data-ttu-id="49f9b-193">[![必須項目の一覧を示すスクリーン ショット](./media/3_office.png)](./media/3_office.png)</span><span class="sxs-lookup"><span data-stu-id="49f9b-193">[![Screen shot showing list of mandatory fields](./media/3_office.png)](./media/3_office.png)</span></span> 

<span data-ttu-id="49f9b-194">ブックを作成するには、アプリ バーの **ブックの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-194">To retrieve the resulting workbook, click **Create workbook** in the app bar.</span></span> 

<span data-ttu-id="49f9b-195">エンティティが公開するデータを表示するには、**関連するフォームの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-195">Click **View related form** to see the data that the entity exposes.</span></span> <span data-ttu-id="49f9b-196">このボタンは、**FormRef** プロパティ値を持つエンティティでのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="49f9b-196">This button is only enabled for entities that have a **FormRef** property value.</span></span>

## <a name="document-management"></a><span data-ttu-id="49f9b-197">ドキュメント管理</span><span class="sxs-lookup"><span data-stu-id="49f9b-197">Document management</span></span>
<span data-ttu-id="49f9b-198">ドキュメントの管理は、Azure Blob storage および SharePoint Online でレコードの添付ファイルの保存をサポートします。</span><span class="sxs-lookup"><span data-stu-id="49f9b-198">Document management supports saving record attachments in Azure Blob storage and SharePoint Online.</span></span> <span data-ttu-id="49f9b-199">データベースの記憶域は非推奨です。</span><span class="sxs-lookup"><span data-stu-id="49f9b-199">Database storage is deprecated.</span></span> <span data-ttu-id="49f9b-200">ドキュメントはアプリケーションを介してのみアクセスでき、データベースのパフォーマンスに悪影響を及ぼさないストレージを提供できるという利点があるため Azure Blob ストレージは、データベースのストレージと同等です。</span><span class="sxs-lookup"><span data-stu-id="49f9b-200">Azure Blob storage is equivalent to storage in the database since documents can only be accessed through the application and it provides the added benefit of providing storage that doesn't negatively affect the performance of the database.</span></span> <span data-ttu-id="49f9b-201">Azure blob storage は既定でありすぐに動作します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-201">Azure blob storage is the default and works immediately.</span></span> <span data-ttu-id="49f9b-202">SharePoint テナントは自動的に検出されるため、O365 ライセンスを持っている場合 SharePoint の記憶域がすぐに機能します。例: TenantA.onmicrosoft.com O365/AAD テナントのユーザーは SharePoint サイトとして TenantA.sharepoint.com を取得します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-202">SharePoint storage will work immediately if you have an O365 license since we auto-discover the SharePoint tenant e.g. a user on the TenantA.onmicrosoft.com O365/AAD tenant gets TenantA.sharepoint.com as the SharePoint site.</span></span> <span data-ttu-id="49f9b-203">ユーザーがドキュメントの管理が無効になっている場合、それを有効にするには、**オプション &gt; 一般 &gt; その他**をクリックし、**ドキュメント処理の有効オプション**を**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-203">If document management has been turned off by the user, turn it on by clicking **Options &gt; General &gt; Miscellaneous** and setting **Document handling active** to **Yes**.</span></span> 

<span data-ttu-id="49f9b-204">[![Yes に設定されたドキュメント処理の有効オプションを示すスクリーン ショット](./media/4_office.png)](./media/4_office.png)</span><span class="sxs-lookup"><span data-stu-id="49f9b-204">[![Screen shot showing Document handling active option set to Yes](./media/4_office.png)](./media/4_office.png)</span></span> 

<span data-ttu-id="49f9b-205">データを持つページでは、**添付**ボタンが右上隅に表示されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-205">On any page that has data, an **Attach** button will be available in the upper-right corner.</span></span> 

<span data-ttu-id="49f9b-206">[![添付ボタンを表示するスクリーン ショット](./media/5_office.png)](./media/5_office.png)</span><span class="sxs-lookup"><span data-stu-id="49f9b-206">[![Screen shot showing Attach button](./media/5_office.png)](./media/5_office.png)</span></span> 

<span data-ttu-id="49f9b-207">**添付ファイル** ページには、前のページで選択したレコードに関連付けられている添付ファイル (ドキュメント) のビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-207">The **Attachments** page provides a view of the attachments (documents) that are associated with the record that was selected on the previous page.</span></span> <span data-ttu-id="49f9b-208">アプリ バーの **新規** ボタン (**+**) をクリックすると、レコードに新しいアタッチメントを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-208">You can add new attachments to the record by clicking the **New** button (**+**) in the app bar.</span></span> <span data-ttu-id="49f9b-209">**ファイル**および**画像**ドキュメント タイプについては、関連ファイルを提供するように求められます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-209">For the **File** and **Image** document types, you will be prompted to provide the associated file.</span></span>

### <a name="document-preview"></a><span data-ttu-id="49f9b-210">ドキュメントのプレビュー</span><span class="sxs-lookup"><span data-stu-id="49f9b-210">Document preview</span></span>

<span data-ttu-id="49f9b-211">サポート対象のファイルの種類のプレビューは、**プレビュー**クイック タブで提供されます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-211">A preview for supported file types is provided on the **Preview** FastTab.</span></span> <span data-ttu-id="49f9b-212">PNG イメージやテキスト ファイルなどの基本的なドキュメント タイプは、既定でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="49f9b-212">Basic document types, such as PNG images and text files, are supported by default.</span></span> <span data-ttu-id="49f9b-213">Microsoft Word、Excel、および PowerPoint ファイルなどの Office ドキュメント タイプは、実稼動 Office Web Apps サーバーを使用する必要があり、OneBox コンフィギュレーションを利用できない場合もあます。</span><span class="sxs-lookup"><span data-stu-id="49f9b-213">Office document types, such as Microsoft Word, Excel, and PowerPoint files, must use a production Office Web Apps Server, which might not be available in a OneBox configuration.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="49f9b-214">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="49f9b-214">Frequently asked questions</span></span>

### <a name="office-licensing"></a><span data-ttu-id="49f9b-215">Office ライセンス</span><span class="sxs-lookup"><span data-stu-id="49f9b-215">Office Licensing</span></span>

#### <a name="what-office-365-licenses-are-available"></a><span data-ttu-id="49f9b-216">どのような Office 365 ライセンスがありますか ?</span><span class="sxs-lookup"><span data-stu-id="49f9b-216">What Office 365 licenses are available?</span></span>

<span data-ttu-id="49f9b-217">「[Office 365 ライセンス オプション](https://products.office.com/business/compare-office-365-for-business-plans)」が多数あります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-217">There are lots of [Office 365 license options](https://products.office.com/business/compare-office-365-for-business-plans).</span></span> <span data-ttu-id="49f9b-218">所属されている組織にとって、意味のあるライセンスを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="49f9b-218">You should select the license that makes sense for your organization.</span></span>

#### <a name="after-purchasing-an-office-365-license-what-needs-to-be-done-to-set-up-sharepoint-storage-for-attachments"></a><span data-ttu-id="49f9b-219">Office 365 のライセンスを購入した後、添付ファイル用に SharePoint ストレージを設定するために何を行う必要がありますか?</span><span class="sxs-lookup"><span data-stu-id="49f9b-219">After purchasing an Office 365 license, what needs to be done to set up SharePoint storage for attachments?</span></span>

<span data-ttu-id="49f9b-220">ドキュメント パラメーター フォームを開いて、SharePoint サーバーが自動的に検出および設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="49f9b-220">Open the Document Parameters form and ensure that the SharePoint server has been automatically discovered and set.</span></span> <span data-ttu-id="49f9b-221">ここで、ドキュメント タイプを開くか作成し、"SharePoint" へのドキュメント タイプの場所を設定し、ファイルを保存する必要があるフォルダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="49f9b-221">Now open or create a Document Type, set the Document Type's location to "SharePoint" and select the folder that the files should be stored in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49f9b-222">追加リソース</span><span class="sxs-lookup"><span data-stu-id="49f9b-222">Additional resources</span></span>

[<span data-ttu-id="49f9b-223">Office 統合ラボとチュートリアル</span><span class="sxs-lookup"><span data-stu-id="49f9b-223">Office Integration lab and walkthroughs</span></span>](office-integration-tutorial.md)

[<span data-ttu-id="49f9b-224">Office 統合のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="49f9b-224">Office Integration Troubleshooting</span></span>](office-integration-troubleshooting.md)

[<span data-ttu-id="49f9b-225">アプリケーション スタックおよびサーバーのアーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="49f9b-225">Application stack and server architecture</span></span>](../dev-tools/application-stack-server-architecture.md)
---
title: 実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する
description: このトピックでは、構成されたデータ フローと変換をよりよく理解するために、実行された ER 形式のデータ ソースをデバッグする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680785"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="e0146-103">実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する</span><span class="sxs-lookup"><span data-stu-id="e0146-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="e0146-104">電子レポート（ER）ソリューションを [構成](tasks/er-format-configuration-2016-11.md) してアウトバウンド文書を生成する場合、アプリケーションからデータを取得し、生成される出力にデータを入力するために使用する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="e0146-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="e0146-105">ER ソリューションのライフ サイクル サポートをより効率的には、ご利用のソリューションを、ER [データモデル](general-electronic-reporting.md#DataModelComponent) とその [マッピング](general-electronic-reporting.md#ModelMappingComponent) コンポーネント、および [ER](general-electronic-reporting.md#FormatComponentOutbound)フォーマットとそのマッピング コンポーネントで構成する必要があります。モデル マッピングがアプリケーション固有のものであるのに対し、他のコンポーネントはアプリケーションに依存しないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e0146-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="e0146-106">したがって、一部の ER コンポーネントは、生成された出力にデータを入力するプロセスに [影響を与える](general-electronic-reporting.md#FormatComponentOutbound) 場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="e0146-107">生成された出力のデータは、アプリケーション データベースの同じデータとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="e0146-108">そのような場合は、どの ER コンポーネントがデータ変換を担当しているかを特定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="e0146-109">ER データソース デバッガー機能を実行すると、この調査に必要な時間と費用を大幅に削減できます。</span><span class="sxs-lookup"><span data-stu-id="e0146-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="e0146-110">ER 形式の実行を中断して、データソース デバッガ インターフェイスを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="e0146-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="e0146-111">この機能では、使用可能なデータソースを参照し、実行する個別のデータソースを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e0146-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="e0146-112">この手動実行では、ER 形式の実稼働中にデータソースの実行をシミュレートします。</span><span class="sxs-lookup"><span data-stu-id="e0146-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="e0146-113">結果は、受信したデータを分析するページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e0146-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="e0146-114">データソースのデバッグ機能を有効にするには、ER ユーザー パラメーターで、**形式実行時にデータのデバッグを有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0146-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="e0146-115">その後、ER 形式を実行してアウトバウンド ドキュメントを生成する際に、データソースのデバッグを開始できます。</span><span class="sxs-lookup"><span data-stu-id="e0146-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="e0146-116">**デバッグを開始する** オプションを使用して、[ER オペレーション デザイナー](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) で構成された ER 形式のデータソースのデバッグを開始することもできます。</span><span class="sxs-lookup"><span data-stu-id="e0146-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="e0146-117">このトピックでは、実行された ER 形式のデータソース デバッグを開始するためのガイドラインを示します。</span><span class="sxs-lookup"><span data-stu-id="e0146-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="e0146-118">ここでは、データフローとデータ変換を理解する上で、どのような情報が役立つのかを解説しています。</span><span class="sxs-lookup"><span data-stu-id="e0146-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="e0146-119">このトピックでは、仕入先支払処理の業務プロセスを例として使用します。</span><span class="sxs-lookup"><span data-stu-id="e0146-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="e0146-120">制限</span><span class="sxs-lookup"><span data-stu-id="e0146-120">Limitations</span></span>

<span data-ttu-id="e0146-121">データソースデバッガーを使用すると、送信ドキュメントの生成時に実行する ER 形式のデータソース内のデータにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e0146-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="e0146-122">インバウンド ドキュメントの解析に使用する ER 形式のデータソースのデバッグには使用できません。</span><span class="sxs-lookup"><span data-stu-id="e0146-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="e0146-123">次の ER 形式の設定は、現在データソース デバッグでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="e0146-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="e0146-124">形式の変換</span><span class="sxs-lookup"><span data-stu-id="e0146-124">Format transformations</span></span>
- <span data-ttu-id="e0146-125">形式とマッピングの検証ルール</span><span class="sxs-lookup"><span data-stu-id="e0146-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="e0146-126">式を有効にする</span><span class="sxs-lookup"><span data-stu-id="e0146-126">Enabling expressions</span></span>
- <span data-ttu-id="e0146-127">イン メモリ データ コレクションの詳細</span><span class="sxs-lookup"><span data-stu-id="e0146-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e0146-128">必要条件</span><span class="sxs-lookup"><span data-stu-id="e0146-128">Prerequisites</span></span>

- <span data-ttu-id="e0146-129">このトピックの例を完了するには、次のいずれかの [ロール](../sysadmin/tasks/assign-users-security-roles.md) にアクセスできる必要があります：</span><span class="sxs-lookup"><span data-stu-id="e0146-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="e0146-130">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="e0146-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="e0146-131">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="e0146-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e0146-132">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e0146-132">System administrator</span></span>

- <span data-ttu-id="e0146-133">この会社は、**DEMF** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="e0146-134">このトピックの [付録1](#appendix1) の手順に従って、仕入先支払の処理に必要となる Microsoft ER ソリューションのコンポーネントをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="e0146-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="e0146-135">本トピックの [付録2](#appendix2) に記載の手順に従って、ダウンロードした ER ソリューションを使用して、ベンダーの支払い処理のための買掛金を準備してください。</span><span class="sxs-lookup"><span data-stu-id="e0146-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="e0146-136">仕入先の支払いを処理して支払いファイルを取得する</span><span class="sxs-lookup"><span data-stu-id="e0146-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="e0146-137">本トピックの [付録3](#appendix3) に記載の手順に従って、仕入先の支払いを処理します。</span><span class="sxs-lookup"><span data-stu-id="e0146-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![仕入先の支払い処理中](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="e0146-139">ZIP ファイルをご利用のコンピューターにダウンロード し、保存します。</span><span class="sxs-lookup"><span data-stu-id="e0146-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="e0146-140">ZIP ファイルから **ISO20022 Credit transfer.xml** 支払ファイルを抽出します。</span><span class="sxs-lookup"><span data-stu-id="e0146-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="e0146-141">XML ファイル ビューアーを使用して、抽出した支払ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="e0146-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="e0146-142">支払ファイルでは、仕入先の銀行口座の国際銀行口座番号 (IBAN) コードにスペースが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="e0146-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="e0146-143">したがって、**銀行口座** ページで [入力](#enteredIBANcode) した値とは異なります。</span><span class="sxs-lookup"><span data-stu-id="e0146-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![空白のない IBAN コード](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="e0146-145">ER データソースデバッガーを使用して、ER ソリューションのどのコンポーネントが IBAN コードのスペースの切り捨てに使用されているかを説明します。</span><span class="sxs-lookup"><span data-stu-id="e0146-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="e0146-146">データソースのデバッグを有効にする</span><span class="sxs-lookup"><span data-stu-id="e0146-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="e0146-147">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e0146-148">**構成** ページ、アクション ウィンドウ、**構成** タブ、**詳細設定** グループで、**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="e0146-149">**形式実行時にデータのデバッグを有効にする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0146-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e0146-150">このパラメーターはユーザーに固有のものまたは会社固有のものであることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e0146-150">This parameter is user-specific and company-specific.</span></span>

    ![ユーザー パラメーター ダイアログ ボックス](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="e0146-152">仕入先支払の処理のデバッグ</span><span class="sxs-lookup"><span data-stu-id="e0146-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="e0146-153">本トピックの [付録3](#appendix3) に記載の手順に従って、仕入先の支払いを処理します。</span><span class="sxs-lookup"><span data-stu-id="e0146-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="e0146-154">メッセージ ボックスで、**はい** を選択して、仕支入の支払い処理を中断し、代わりに **デバッグ データソース** のページでデータ ソースのデバッグを開始することを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0146-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![確認用メッセージボックス](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="e0146-156">支払処理に使用されるデバッグ データ ソース</span><span class="sxs-lookup"><span data-stu-id="e0146-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="e0146-157">モデル マッピングのデバッグ</span><span class="sxs-lookup"><span data-stu-id="e0146-157">Debug the model mapping</span></span>

1. <span data-ttu-id="e0146-158">アクション ウィンドウの **デバッグ データソース** で、**モデル マッピング** を選択してこの ER コンポーネントからデバッグを開始します。</span><span class="sxs-lookup"><span data-stu-id="e0146-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="e0146-159">左側の [データソース] ウィンドウで、**\$notSentTransactions** データソースを選択し、**すべてのレコードの読み取り** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="e0146-160">**1 レコードの読み取り**、**10 レコードの読み取り**、**100 レコードの読み取り**、または **すべてのレコードの読み取り** を選択して、選択したデータ ソースから適切な数のレコードを強制的に読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="e0146-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="e0146-161">このように、実行中の ER 形式からデータソースへのアクセスをシミュレートすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0146-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="e0146-162">右のデータ ウィンドウで、**すべて展開する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="e0146-163">**レコード リスト** タイプの選択されたデータソースに 1 つのレコードが含まれていることがわかります。</span><span class="sxs-lookup"><span data-stu-id="e0146-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="e0146-164">**\$notSentTransactions** データソースを展開し、入れ子になった **vendBankAccountInTransactionCompany()** メソッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="e0146-165">**vendBankAccountInTransactionCompany()** メソッドを展開し、入れ子になった **IBAN** フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="e0146-166">**値の取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-166">Select **Get value**.</span></span>

    <span data-ttu-id="e0146-167">**値の取得**  を選択すると、選択したデータソースの選択したフィールドの値を読み取ることができます。</span><span class="sxs-lookup"><span data-stu-id="e0146-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="e0146-168">このように、実行中の ER 形式からこのフィールドへのアクセスをシミュレートすることができます。</span><span class="sxs-lookup"><span data-stu-id="e0146-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="e0146-169">**すべて展開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-169">Select **Expand all**.</span></span>

    ![モデル マッピングの IBAN フィールドの値](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="e0146-171">このように、仕入先の銀行口座に対して返される IBAN コードにスペースが含まれているため、モデル マッピングではスペースが切り捨てられることはありません。</span><span class="sxs-lookup"><span data-stu-id="e0146-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="e0146-172">したがって、データ ソースのデバッグを続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="e0146-173">形式マッピングのデバッグ</span><span class="sxs-lookup"><span data-stu-id="e0146-173">Debug the format mapping</span></span>

1. <span data-ttu-id="e0146-174">アクション ウィンドウの **デバッグ データソース** で、**形式のマッピング** を選択してこの ER コンポーネントからデバッグを継続します。</span><span class="sxs-lookup"><span data-stu-id="e0146-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="e0146-175">**\$PaymentByDebtor** データソースを選択し、**すべてのレコードの読み取り** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="e0146-176">**\$PaymentByDebtor** を展開します。</span><span class="sxs-lookup"><span data-stu-id="e0146-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="e0146-177">**\$PaymentByDebtor.Lines** を展開し 、**すべてのレコードの読み取り** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="e0146-178">**\$PaymentByDebtor.Lines.CreditorAccount** を展開します。</span><span class="sxs-lookup"><span data-stu-id="e0146-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="e0146-179">**\$PaymentByDebtor.Lines.CreditorAccount.Identification** を展開し、**\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="e0146-180">**値の取得** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-180">Select **Get value**.</span></span>
8. <span data-ttu-id="e0146-181">**すべて展開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-181">Select **Expand all**.</span></span>

    ![形式マッピングの IBAN フィールドの値](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="e0146-183">このように、仕入先の銀行口座に返されるIBANコードにはスペースが含まれているため、形式マッピングのデータソースはスペースの切り捨てに責任を負いません。</span><span class="sxs-lookup"><span data-stu-id="e0146-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="e0146-184">したがって、データ ソースのデバッグを続行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="e0146-185">形式のデバッグ</span><span class="sxs-lookup"><span data-stu-id="e0146-185">Debug the format</span></span>

1. <span data-ttu-id="e0146-186">アクション ウィンドウの **デバッグ データソース** で、**形式** を選択してこの ER コンポーネントからデバッグを継続します。</span><span class="sxs-lookup"><span data-stu-id="e0146-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="e0146-187">形式の要素を展開して **20022** \> **XMLHeader** \> **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** を選択し、**すべてのレコードの読み取り** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="e0146-188">形式の要素を展開して **ISO20022CTReports** \> **XMLHeader** \> **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** を選択し、**すべてのレコードの読み取り** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="e0146-189">形式の要素を展開して **ISO20022CTReports** \> **XMLHeader** \> **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** を選択し、**値を取得する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="e0146-190">**すべて展開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-190">Select **Expand all**.</span></span>

    ![形式の IBAN フィールドの値](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="e0146-192">このように、仕入先の銀行口座に対して返される IBAN コードにスペースが含まれているため、形式のバインドではスペースが切り捨てられることはありません。</span><span class="sxs-lookup"><span data-stu-id="e0146-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="e0146-193">したがって、**BankIBAN** 要素は、スペースを切り捨てる形式変換を使用するように構成されます。</span><span class="sxs-lookup"><span data-stu-id="e0146-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="e0146-194">データ ソース デバッガーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e0146-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="e0146-195">形式の変換を確認する</span><span class="sxs-lookup"><span data-stu-id="e0146-195">Review the format transformations</span></span>

1. <span data-ttu-id="e0146-196">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e0146-197">**構成** ページで、**支払モデル** \> **ISO20022 クレジット転送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="e0146-198">**デザイナー** を選択し、続いて要素を展開して **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![形式デザイナー ページの BankIBAN 要素](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="e0146-200">このように、**BankIBAN** 要素は、**英数字以外を削除** するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e0146-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="e0146-201">**変換** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN 要素が使用する変換タブ](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="e0146-203">このように、**英数字以外の** 変換は、提供されたテキスト文字列からスペースを切り捨てる式を使用するように構成されています。</span><span class="sxs-lookup"><span data-stu-id="e0146-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="e0146-204">操作デザイナーでデバッグを開始する</span><span class="sxs-lookup"><span data-stu-id="e0146-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="e0146-205">ER 形式の下書きバージョンを操作デザイナーから直接実行できるように構成した場合は、アクション ウィンドウで **デバッグの開始** を選択することにより、データソース デバッガーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e0146-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![形式デザイナー ページのデバッグ開始ボタン](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="e0146-207">編集中の ER 形式の形式マッピングと形式コンポーネントのデバッグが可能です。</span><span class="sxs-lookup"><span data-stu-id="e0146-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="e0146-208">モデル マッピング デザイナーでデバッグを開始する</span><span class="sxs-lookup"><span data-stu-id="e0146-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="e0146-209">**モデル マッピング** ページから実行できる ER モデル マッピングを構成した場合、アクション ウィンドウで **デバッグの開始** を選択すると、データ ソース デバッガーにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e0146-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![モデル マッピング デザイナー ページのデバッグ開始ボタン](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="e0146-211">編集中の ER マッピングのモデル マッピング コンポーネントは、デバッグが可能です。</span><span class="sxs-lookup"><span data-stu-id="e0146-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="e0146-212">付録 1：ER ソリューションを入手する</span><span class="sxs-lookup"><span data-stu-id="e0146-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="e0146-213">ER ソリューションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="e0146-213">Download an ER solution</span></span>

<span data-ttu-id="e0146-214">ER ソリューションを使用して、処理された仕入先決済の電子決済ファイルをする場合は、 Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリまたはグローバル リポジトリから入手可能な **ISO20022 クレジット転送** ER 決済フォーマットを [ダウンロード](download-electronic-reporting-configuration-lcs.md) することができます。</span><span class="sxs-lookup"><span data-stu-id="e0146-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![構成リポジトリ ページの ER 決済形式のインポート](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="e0146-216">選択された ER 形式に加えて、**ISO20022 クレジット転送** ER ソリューションの一環として、以下の[構成](general-electronic-reporting.md#Configuration) を Microsoft Dynamics 365 Finance インスタンスに自動的にインポートする必要があります：</span><span class="sxs-lookup"><span data-stu-id="e0146-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="e0146-217">**支払モデル** [ER データ モデル 構成](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="e0146-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="e0146-218">**ISO20022 クレジット連想** [ER 形式の構成](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="e0146-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="e0146-219">**支払 モデル マッピング 1611** [ER モデル マッピングの構成](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="e0146-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="e0146-220">**支払 モデルのマッピング先 SO20022** ER モデル マッピングの構成</span><span class="sxs-lookup"><span data-stu-id="e0146-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="e0146-221">これらの構成は、ER フレームワークの **構成** ページ（**組織管理** \> **電子レポート** \> **構成**）で確認できます。</span><span class="sxs-lookup"><span data-stu-id="e0146-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![構成ページでインポートされた ER 構成](./media/er-data-debugger-configurations.png)

<span data-ttu-id="e0146-223">上記のいずれかの構成が構成ツリーに表示されない場合は、**ISO20022 クレジット転送** ER 支払形式と同じ方法でダウンロードし、LCS 共有アセットライブラリから手動でダウンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e0146-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="e0146-224">ダウンロードした ER ソリューションの分析</span><span class="sxs-lookup"><span data-stu-id="e0146-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="e0146-225">モデル マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="e0146-225">Review the model mapping</span></span>

1. <span data-ttu-id="e0146-226">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e0146-227">**支払モデル** \> **支払モデルのマッピング 1611** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="e0146-228">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0146-228">Select **Designer**.</span></span>
4. <span data-ttu-id="e0146-229">マッピング レコード **支払モデル マッピング ISO20022 CT** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="e0146-230">**デザイナー** を選択し、開いているモデル マッピングを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0146-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="e0146-231">データモデルの **支払** フィールドは、処理中のベンダーの支払いラインのリストを返す **\$notSentTransactions** データ ソースにバインドされていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="e0146-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![モデル マッピング デザイナー ページの支払フィールド](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="e0146-233">形式マッピングを確認する</span><span class="sxs-lookup"><span data-stu-id="e0146-233">Review the format mapping</span></span>

1. <span data-ttu-id="e0146-234">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e0146-235">**支払モデル** \> **ISO20022 クレジット転送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="e0146-236">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e0146-236">Select **Designer**.</span></span>
4. <span data-ttu-id="e0146-237">**マッピング** タブで、開いている形式のマッピングを確認します。</span><span class="sxs-lookup"><span data-stu-id="e0146-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="e0146-238">**ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** のファイルは **\$PaymentByDebtor** データ ソースにバインドされており。このデータ ソースは、データ モデルの **支払い** フィールドのレコードをグループ化するように構成されていることを留意してください。</span><span class="sxs-lookup"><span data-stu-id="e0146-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![形式デザイナー ページの PmtInf 要素](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="e0146-240">形式を確認する</span><span class="sxs-lookup"><span data-stu-id="e0146-240">Review the format</span></span>

1. <span data-ttu-id="e0146-241">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e0146-242">**支払モデル** \> **ISO20022 クレジット転送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="e0146-243">**デザイナー** を選択し、開いている形式を確認します。</span><span class="sxs-lookup"><span data-stu-id="e0146-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="e0146-244">**ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** が、支払いファイルに仕入先アカウントの IBAN コードを入力するように設定されていることを留意してください。</span><span class="sxs-lookup"><span data-stu-id="e0146-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![形式デザイナー ページの BankIBAN 要素](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="e0146-246">付録 2：買掛金勘定を構成する</span><span class="sxs-lookup"><span data-stu-id="e0146-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="e0146-247">仕入先プロパティの変更</span><span class="sxs-lookup"><span data-stu-id="e0146-247">Modify a vendor property</span></span>

1. <span data-ttu-id="e0146-248">**買掛金勘定** \> **仕入先** \> **すべての仕入先** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="e0146-249">アクション ウィンドウで、仕入先に **DE-01002** を選択し、**設定** グループの **仕入先** タブで、**銀行口座** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="e0146-250">**ID** クイックタブの **IBAN** フィールド に、<a name="enteredIBANcode"></a>**GB33 BUKB 2020 1555 5555 55** を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0146-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="e0146-251">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-251">Select **Save**.</span></span>

![仕入先の銀行口座ページで設定された IBAN フィールド](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="e0146-253">支払方法の設定</span><span class="sxs-lookup"><span data-stu-id="e0146-253">Set up a method of payment</span></span>

1. <span data-ttu-id="e0146-254">**買掛金勘定** \> **支払設定** \> **支払方法** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="e0146-255">支払方法 **SEPA CT** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="e0146-256">**ファイル形式** セクションの **ファイル形式** クイック タブで、 **一般的なエクスポート形式** のオプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e0146-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="e0146-257">**形式の構成のエクスポート** フィールドで、ER 形式に **ISO20022 クレジット転送** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="e0146-258">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-258">Select **Save**.</span></span>

![支払方法ページにおけるファイル形式の設定](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="e0146-260">仕入先の支払を追加する</span><span class="sxs-lookup"><span data-stu-id="e0146-260">Add a vendor payment</span></span>

1. <span data-ttu-id="e0146-261">**買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="e0146-262">新しい支払仕訳帳を追加します。</span><span class="sxs-lookup"><span data-stu-id="e0146-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="e0146-263">**明細行** を選択し、新しい支払明細行を追加します。</span><span class="sxs-lookup"><span data-stu-id="e0146-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="e0146-264">**口座** フィールドで、仕入先に **DE-01002** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="e0146-265">**Debit** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="e0146-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="e0146-266">**支払方法** フィールドで、**SEPA CT** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="e0146-267">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-267">Select **Save**.</span></span>

![仕入先支払ページに追加された仕入先の支払](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="e0146-269">付録 3：仕入先の支払いを処理する</span><span class="sxs-lookup"><span data-stu-id="e0146-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="e0146-270">**買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e0146-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="e0146-271">**仕入先支払仕訳帳** ページで、上記手順で作成した 支払仕訳帳を選択し、**明細行** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="e0146-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="e0146-272">支払明細行を選択し、**支払ステータス** \> **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="e0146-273">**支払の生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="e0146-274">**支払方法** フィールドで、**SEPA CT** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="e0146-275">**銀行口座** フィールドで、 **DEMF OPER** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="e0146-276">**支払いの生成** ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="e0146-277">**電子レポート パラメーター** ダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e0146-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>

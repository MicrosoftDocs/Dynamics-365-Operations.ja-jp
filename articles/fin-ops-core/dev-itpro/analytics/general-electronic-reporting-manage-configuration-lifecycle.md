---
title: 電子申告 (ER) コンフィギュレーション ライフサイクルの管理
description: このトピックでは、Dynamics 365 Finance の電子申告 (ER) コンフィギュレーションのライフ サイクルを管理する方法について説明します。
author: NickSelin
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52aba53b5323a9c6c4331cd8de7e932bb9c3547e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893204"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="c6569-103">電子申告 (ER) コンフィギュレーション ライフサイクルの管理</span><span class="sxs-lookup"><span data-stu-id="c6569-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6569-104">このトピックでは、Dynamics 365 Finance の電子申告 (ER) コンフィギュレーションのライフ サイクルを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c6569-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="c6569-105">概要</span><span class="sxs-lookup"><span data-stu-id="c6569-105">Overview</span></span>

<span data-ttu-id="c6569-106">電子申告 (ER) は、法律の要件および国固有の電子ドキュメントをサポートするエンジンです。</span><span class="sxs-lookup"><span data-stu-id="c6569-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="c6569-107">一般に、ER は、各電子ドキュメントに関して次のタスクの実行を想定しています。</span><span class="sxs-lookup"><span data-stu-id="c6569-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="c6569-108">詳細については、[電子申告 (ER) の概要](general-electronic-reporting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c6569-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="c6569-109">電子ドキュメントのテンプレートを設計します:</span><span class="sxs-lookup"><span data-stu-id="c6569-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="c6569-110">ドキュメントに表示できるデータのソースを識別します:</span><span class="sxs-lookup"><span data-stu-id="c6569-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="c6569-111">データ テーブル、データ エンティティ、クラスなど基になるデータ。</span><span class="sxs-lookup"><span data-stu-id="c6569-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="c6569-112">実行日および時刻、タイム ゾーンなどプロセス固有のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c6569-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="c6569-113">実行時にエンドユーザーが指定するユーザー入力パラメーター。</span><span class="sxs-lookup"><span data-stu-id="c6569-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="c6569-114">必要なドキュメントの要素、および最終ドキュメントの形式を指定するトポロジを定義します。</span><span class="sxs-lookup"><span data-stu-id="c6569-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="c6569-115">データソース経由でドキュメントの形式コンポーネントにバインドされ、定義されたドキュメント要素に選択したデータ ソースから要求されるデータ フローのコンフィギュレーションを行い、プロセスの制御ロジックを指定します。</span><span class="sxs-lookup"><span data-stu-id="c6569-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="c6569-116">他のインスタンスでテンプレートが使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c6569-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="c6569-117">作成したドキュメント テンプレートを ER のコンフィギュレーションに変換し、現在のアプリケーション インスタンスからコンフィギュレーションをローカルまたは Lifecycle Services (LCS) に保存できる XML パッケージとしてエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="c6569-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in Lifecycle Services (LCS).</span></span>
    - <span data-ttu-id="c6569-118">ER コンフィギュレーションをアプリケーション ドキュメント テンプレートに変換します。</span><span class="sxs-lookup"><span data-stu-id="c6569-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="c6569-119">ローカルまたは LCS に保存されている XML パッケージを、現在のインスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="c6569-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="c6569-120">電子ドキュメント テンプレートをカスタマイズします:</span><span class="sxs-lookup"><span data-stu-id="c6569-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="c6569-121">LCS からテンプレートを ER コンフィギュレーションとして現在のインスタンスに取り込みます。</span><span class="sxs-lookup"><span data-stu-id="c6569-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="c6569-122">基本バージョンを参照しながら、カスタム バージョンの ER コンフィギュレーションを設計します。</span><span class="sxs-lookup"><span data-stu-id="c6569-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="c6569-123">アプリケーションで使用できるように、特定の業務プロセスを含むテンプレートを連結します。</span><span class="sxs-lookup"><span data-stu-id="c6569-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="c6569-124">設定をコンフィギュレーションし、プロセスに関連したパラメーターでそのコンフィギュレーションを参照して、アプリケーションで ER コンフィギュレーションの使用を開始できるようにします。</span><span class="sxs-lookup"><span data-stu-id="c6569-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="c6569-125">たとえば、特定の買掛金勘定の支払方法の ER コンフィギュレーションを参照して、請求書の処理についての電子支払メッセージを生成します。</span><span class="sxs-lookup"><span data-stu-id="c6569-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="c6569-126">特定の業務プロセスでテンプレートを使用します:</span><span class="sxs-lookup"><span data-stu-id="c6569-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="c6569-127">特定の業務プロセスで ER コンフィギュレーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="c6569-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="c6569-128">たとえば、ER コンフィギュレーションを参照する支払方法が選択された場合の請求書の処理についての電子支払メッセージの生成。</span><span class="sxs-lookup"><span data-stu-id="c6569-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="c6569-129">概念</span><span class="sxs-lookup"><span data-stu-id="c6569-129">Concepts</span></span>
<span data-ttu-id="c6569-130">次のロールおよび関連活動が、ER コンフィギュレーション ライフサイクルに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="c6569-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="c6569-131">役割</span><span class="sxs-lookup"><span data-stu-id="c6569-131">Role</span></span>                                       | <span data-ttu-id="c6569-132">活動</span><span class="sxs-lookup"><span data-stu-id="c6569-132">Activities</span></span>                                                      | <span data-ttu-id="c6569-133">説明</span><span class="sxs-lookup"><span data-stu-id="c6569-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="c6569-134">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="c6569-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="c6569-135">ER コンポーネントを作成および管理します (モデル、形式)。</span><span class="sxs-lookup"><span data-stu-id="c6569-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="c6569-136">ER のドメイン固有のデータ モデルを設計し、電子ドキュメントの必須のテンプレートを作成し、それらを結合するビジネス ユーザー。</span><span class="sxs-lookup"><span data-stu-id="c6569-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="c6569-137">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="c6569-137">Electronic reporting developer</span></span>             | <span data-ttu-id="c6569-138">データ モデルのマップを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="c6569-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="c6569-139">必要な財務データ ソースを選択し、ER のドメイン固有のデータ モデルに結合する専門家。</span><span class="sxs-lookup"><span data-stu-id="c6569-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="c6569-140">会計監修者</span><span class="sxs-lookup"><span data-stu-id="c6569-140">Accounting supervisor</span></span>                      | <span data-ttu-id="c6569-141">ER のコンポーネントを参照するプロセス関連の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="c6569-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="c6569-142">たとえば、特定の買掛金勘定支払方法で使用して請求書処理用に電子支払メッセージを生成する ER のコンフィギュレーション設定を許可する **会計監修者** のロール。</span><span class="sxs-lookup"><span data-stu-id="c6569-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="c6569-143">買掛金勘定支払係</span><span class="sxs-lookup"><span data-stu-id="c6569-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="c6569-144">特定の業務プロセスで ER コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="c6569-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="c6569-145">たとえば、特定の支払方法に対して構成されている ER 形式に基づいて請求書処理用に電子支払のメッセージが生成されるようにするのを許可する **買掛金勘定支払の担当者** ロール。</span><span class="sxs-lookup"><span data-stu-id="c6569-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="c6569-146">ER コンフィギュレーションの開発ライフサイクル</span><span class="sxs-lookup"><span data-stu-id="c6569-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="c6569-147">ER に関連する次の理由から、個別の Finance and Operations インスタンスとしての開発環境で、ER 構成を作成することをお勧めします:</span><span class="sxs-lookup"><span data-stu-id="c6569-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="c6569-148">**電子申告開発者** ロールまたは **電子申告機能コンサルタント** ロールのユーザーは、テスト目的でコンフィギュレーションを編集し、実行できます。</span><span class="sxs-lookup"><span data-stu-id="c6569-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="c6569-149">このシナリオでは、インスタンスで使用する業務データと業績について有害なおそれがあるテーブルおよびクラス メソッドが呼び出されることがあります。</span><span class="sxs-lookup"><span data-stu-id="c6569-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="c6569-150">ER コンフィギュレーションの ER データ ソースとしてのクラスおよびテーブル メソッドの使用は、エントリ ポイントおよび記録された会社の内容によって制限されません。</span><span class="sxs-lookup"><span data-stu-id="c6569-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="c6569-151">**電子申告開発者** ロールまたは **電子申告機能コンサルタント** ロールのユーザーは、機密情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c6569-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="c6569-152">開発環境で設計された ER コンフィギュレーションは、コンフィギュレーション評価 (適切な統合プロセス、結果の正確性、パフォーマンス)、およびロールにおけるアクセス権の正確性、職務分掌など品質保証のために、テスト環境に [アップロード](#data-persistence-consideration) できます。</span><span class="sxs-lookup"><span data-stu-id="c6569-152">ER configurations that are designed in the development environment can be [uploaded](#data-persistence-consideration) to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="c6569-153">ER コンフィギュレーションの交換を可能にする機能は、この目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c6569-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="c6569-154">認定された ER コンフィギュレーションは、LCS にアップロードしてサービスのサブスクライバーと共有するか、または内部で使用する実稼働環境に [インポート](#data-persistence-consideration) することができます。</span><span class="sxs-lookup"><span data-stu-id="c6569-154">Proven ER configurations can be uploaded to LCS to share them with service subscribers, or they can be [imported](#data-persistence-consideration) to the production environment for internal use.</span></span>

![ER コンフィギュレーション ライフサイクル](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a><span data-ttu-id="c6569-156"><a name="data-persistence-consideration" /> データ持続性の考慮事項</span><span class="sxs-lookup"><span data-stu-id="c6569-156"><a name="data-persistence-consideration" />Data persistence consideration</span></span>

<span data-ttu-id="c6569-157">ER [コンフィギュレーション](general-electronic-reporting.md#Configuration) のさまざまな [バージョン](general-electronic-reporting.md#component-versioning) を Finance インスタンスに個別に [インポート](tasks/er-import-configuration-lifecycle-services.md) できます。</span><span class="sxs-lookup"><span data-stu-id="c6569-157">You can individually [import](tasks/er-import-configuration-lifecycle-services.md) different [versions](general-electronic-reporting.md#component-versioning) of an ER [configuration](general-electronic-reporting.md#Configuration) to your Finance instance.</span></span> <span data-ttu-id="c6569-158">新しいバージョンの ER コンフィギュレーションをインポートするとき、システムはこのコンフィギュレーションのドラフト バージョンのコンテンツを制御します。</span><span class="sxs-lookup"><span data-stu-id="c6569-158">When a new version of an ER configuration is imported, the system controls the content of the draft version of this configuration:</span></span>

   - <span data-ttu-id="c6569-159">インポートされたバージョンが、現在の Finance インスタンスにおけるこのコンフィギュレーションの最も新しいバージョンより低い場合、そのコンフィギュレーションのドラフト バージョンのコンテンツは変更されないままです。</span><span class="sxs-lookup"><span data-stu-id="c6569-159">When the imported version is lower than the highest version of this configuration in the current Finance instance, the content of the draft version of this configuration remains unchanged.</span></span>
   - <span data-ttu-id="c6569-160">インポートされたバージョンが、現在の Finance インスタンスにおけるこのコンフィギュレーションのその他のバージョンより新しい場合、インポートされたバージョンのコンテンツはこのコンフィギュレーションのドラフト バージョンにコピーされ、最後に完了したバージョンの編集を続行できます。</span><span class="sxs-lookup"><span data-stu-id="c6569-160">When the imported version is higher than any other version of this configuration in the current Finance instance, the content of the imported version is copied to the draft version of this configuration to let you continue editing the last completed version.</span></span>

<span data-ttu-id="c6569-161">このコンフィギュレーションが現在有効化されているコンフィギュレーション [プロバイダー](general-electronic-reporting.md#Provider) によって所有されている場合、このコンフィギュレーションのドラフト バージョンは、**コンフィギュレーション** ページの **バージョン** クイックタブに表示されます (**組織管理** > **電子申告** > **コンフィギュレーション**)。</span><span class="sxs-lookup"><span data-stu-id="c6569-161">If this configuration is owned by the configuration [provider](general-electronic-reporting.md#Provider) that is currently activated, the draft version of this configuration is visible to you on the **Versions** FastTab of the **Configurations** page (**Organization administration** > **Electronic reporting** > **Configurations**).</span></span> <span data-ttu-id="c6569-162">関連する ER デザイナーを使用して、コンフィギュレーションのドラフト バージョンを選択し、そのコンテンツを [変更](er-quick-start2-customize-report.md#ConfigureDerivedFormat) することができます。</span><span class="sxs-lookup"><span data-stu-id="c6569-162">You can select the draft version of the configuration and [modify](er-quick-start2-customize-report.md#ConfigureDerivedFormat) its content by using the relevant ER designer.</span></span> <span data-ttu-id="c6569-163">ER コンフィギュレーションのドラフト バージョンを編集した場合、そのコンテンツは現在の Finance インスタンスにおけるこのコンフィギュレーションの最も新しいバージョンのコンテンツとは一致しなくなります。</span><span class="sxs-lookup"><span data-stu-id="c6569-163">When you have edited the draft version of an ER configuration, its content no longer matches the content of the highest version of this configuration in the current Finance instance.</span></span> <span data-ttu-id="c6569-164">変更が失われるのを回避するために、システムは、このコンフィギュレーションのバージョンが現在の Finance インスタンスにおけるこのコンフィギュレーションの最も新しいバージョンよりも新しいため、インポートを続行できないというエラーを表示します。</span><span class="sxs-lookup"><span data-stu-id="c6569-164">To prevent the loss of your changes, the system displays an error that the import is unable to continue because the version of this configuration is higher than the highest version of this configuration in the current Finance instance.</span></span> <span data-ttu-id="c6569-165">これが発生した場合、たとえば形式コンフィギュレーション **X** を使用しているときは、**形式 'X' バージョンは完了していません** というエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c6569-165">When this happens, for example with the format configuration **X**, the **Format 'X' version is not completed** error is displayed.</span></span>

<span data-ttu-id="c6569-166">ドラフト バージョンで導入した変更を元に戻すには、**バージョン** クイックタブで Finance の ER コンフィギュレーションの最も新しい完了または共有バージョンを選択し、**このバージョンを取得** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="c6569-166">To undo the changes that you introduced in the draft version, select the highest completed or shared version of your ER configuration in Finance on the **Versions** FastTab, and then select the **Get this version** option.</span></span> <span data-ttu-id="c6569-167">選択したバージョンのコンテンツがドラフト バージョンにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="c6569-167">The content of the selected version is copied to the draft version.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6569-168">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c6569-168">Additional resources</span></span>

[<span data-ttu-id="c6569-169">電子申告 (ER) の概要</span><span class="sxs-lookup"><span data-stu-id="c6569-169">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

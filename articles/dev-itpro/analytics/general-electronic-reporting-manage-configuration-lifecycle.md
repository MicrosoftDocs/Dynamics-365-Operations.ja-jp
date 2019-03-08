---
title: 電子申告 (ER) コンフィギュレーション ライフサイクルの管理
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations ソリューションの電子申告 (ER) コンフィギュレーションのライフ サイクルを管理する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5724ba62bfb2c6e75ae895dc9285966c25f387a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "344803"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="7e0b5-103">電子申告 (ER) コンフィギュレーション ライフサイクルの管理</span><span class="sxs-lookup"><span data-stu-id="7e0b5-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e0b5-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations ソリューションの電子申告 (ER) コンフィギュレーションのライフ サイクルを管理する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for the Microsoft Dynamics 365 for Finance and Operations solution.</span></span>

## <a name="overview"></a><span data-ttu-id="7e0b5-105">概要</span><span class="sxs-lookup"><span data-stu-id="7e0b5-105">Overview</span></span>

<span data-ttu-id="7e0b5-106">電子申告 (ER) は、Microsoft Dynamics 365 for Finance and Operations の法律の要件および国固有の電子ドキュメントをサポートするエンジンです。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="7e0b5-107">一般に、ER は、各電子ドキュメントに関して次のタスクの実行を想定しています。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="7e0b5-108">詳細については、「[電子申告の概要](general-electronic-reporting.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-108">For more details, see [Electronic reporting overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="7e0b5-109">電子ドキュメントのテンプレートを設計します:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="7e0b5-110">ドキュメントに表示できるデータのソースを識別します:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="7e0b5-111">データ テーブル、データ エンティティ、クラスなど基になる Finance and Operations データ。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-111">Underlying Finance and Operations data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="7e0b5-112">実行日および時刻、タイム ゾーンなどプロセス固有のプロパティ。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="7e0b5-113">実行時にエンドユーザーが指定するユーザー入力パラメーター。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="7e0b5-114">必要なドキュメントの要素、および最終ドキュメントの形式を指定するトポロジを定義します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="7e0b5-115">データソース経由でドキュメントの形式コンポーネントにバインドされ、定義されたドキュメント要素に選択したデータ ソースから要求されるデータ フローのコンフィギュレーションを行い、プロセスの制御ロジックを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="7e0b5-116">他の Finance and Operations インスタンスでテンプレートが使用できるようにします:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-116">Make a template available so that it can be used in other Finance and Operations instances:</span></span>

    - <span data-ttu-id="7e0b5-117">Finance and Operations で作成したドキュメント テンプレートを ER のコンフィギュレーションに変換し、現在の Finance and Operations インスタンスからコンフィギュレーションを XML パッケージとしてエクスポートし、ローカルまたは LCS に保存します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-117">Transform a document template that was created in Finance and Operations into an ER configuration, and export the configuration from the current Finance and Operations instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="7e0b5-118">ER コンフィギュレーションを Finance and Operations ドキュメント テンプレートに変換します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-118">Transform an ER configuration into a Finance and Operations document template.</span></span>
    - <span data-ttu-id="7e0b5-119">ローカルまたは LCS に格納されている XML パッケージを、現在の Finance and Operations インスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-119">Import an XML package that is stored either locally or in LCS into the current Finance and Operations instance.</span></span>

- <span data-ttu-id="7e0b5-120">電子ドキュメント テンプレートをカスタマイズします:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="7e0b5-121">LCS からテンプレートを ER コンフィギュレーションとして現在の Finance and Operations インスタンスに取り込みます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-121">Bring a template from LCS into the current Finance and Operations instance as an ER configuration.</span></span>
    - <span data-ttu-id="7e0b5-122">基本バージョンを参照しながら、カスタム バージョンの ER コンフィギュレーションを設計します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="7e0b5-123">Finance and Operations で使用できるように、特定の業務プロセスを含むテンプレートを連結します:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-123">Integrate a template with a particular business process, so that it's available in Finance and Operations:</span></span>

    - <span data-ttu-id="7e0b5-124">Finance and Operations の設定をコンフィギュレーションし、プロセスに関連したパラメーターでそのコンフィギュレーションを参照して、ER を使用開始できるようにします。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-124">Configure settings so that Finance and Operations starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="7e0b5-125">たとえば、特定の買掛金勘定の支払方法の ER コンフィギュレーションを参照して、請求書の処理についての電子支払メッセージを生成します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="7e0b5-126">特定の業務プロセスでテンプレートを使用します:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="7e0b5-127">特定の業務プロセスで ER コンフィギュレーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="7e0b5-128">たとえば、ER コンフィギュレーションを参照する支払方法が選択された場合の請求書の処理についての電子支払メッセージの生成。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="7e0b5-129">概念</span><span class="sxs-lookup"><span data-stu-id="7e0b5-129">Concepts</span></span>
<span data-ttu-id="7e0b5-130">次のロールおよび関連活動が、ER コンフィギュレーション ライフサイクルに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="7e0b5-131">役割</span><span class="sxs-lookup"><span data-stu-id="7e0b5-131">Role</span></span>                                       | <span data-ttu-id="7e0b5-132">活動</span><span class="sxs-lookup"><span data-stu-id="7e0b5-132">Activities</span></span>                                                      | <span data-ttu-id="7e0b5-133">説明</span><span class="sxs-lookup"><span data-stu-id="7e0b5-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="7e0b5-134">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="7e0b5-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="7e0b5-135">ER コンポーネントを作成および管理します (モデル、形式)。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="7e0b5-136">ER のドメイン固有のデータ モデルを設計し、電子ドキュメントの必須のテンプレートを作成し、それらを結合するビジネス ユーザー。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="7e0b5-137">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="7e0b5-137">Electronic reporting developer</span></span>             | <span data-ttu-id="7e0b5-138">データ モデルのマップを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="7e0b5-139">必要な Finance and Operations データ ソースを選択し、ER のドメイン固有のデータ モデルに結合する Finance and Operations の専門家</span><span class="sxs-lookup"><span data-stu-id="7e0b5-139">A Finance and Operations specialist who selects the required Finance and Operations data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="7e0b5-140">会計監修者</span><span class="sxs-lookup"><span data-stu-id="7e0b5-140">Accounting supervisor</span></span>                      | <span data-ttu-id="7e0b5-141">ER のコンポーネントを参照するプロセス関連の設定を構成します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="7e0b5-142">たとえば、特定の買掛金勘定支払方法で使用して請求書処理用に電子支払メッセージを生成する ER のコンフィギュレーション設定を許可する**会計監修者**のロール。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="7e0b5-143">買掛金勘定支払係</span><span class="sxs-lookup"><span data-stu-id="7e0b5-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="7e0b5-144">特定の業務プロセスで ER コンポーネントを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="7e0b5-145">たとえば、特定の支払方法に対して構成されている ER 形式に基づいて請求書処理用に電子支払のメッセージが生成されるようにするのを許可する**買掛金勘定支払の担当者**ロール。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="7e0b5-146">ER コンフィギュレーションの開発ライフサイクル</span><span class="sxs-lookup"><span data-stu-id="7e0b5-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="7e0b5-147">ER に関連する次の理由から、個別の Finance and Operations インスタンスとしての開発環境で、ER コンフィギュレーションを作成することをお勧めします:</span><span class="sxs-lookup"><span data-stu-id="7e0b5-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="7e0b5-148">**電子申告開発者**ロールまたは**電子申告機能コンサルタント**ロールのユーザーは、テスト目的でコンフィギュレーションを編集し、実行できます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="7e0b5-149">このシナリオでは、Finance and Operations インスタンスの業務データと業績について有害なおそれがあるクラスおよびテーブル メソッドが呼び出されることがあります。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the Finance and Operations instance.</span></span>
- <span data-ttu-id="7e0b5-150">ER コンフィギュレーションの ER データ ソースとしてのクラスおよびテーブル メソッドの使用は Finance and Operations エントリ ポイントおよび記録された会社の内容によって制限されません。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by Finance and Operations entry points and logged company content.</span></span> <span data-ttu-id="7e0b5-151">**電子申告開発者**ロールまたは**電子申告機能コンサルタント**ロールのユーザーは、機密情報にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="7e0b5-152">開発環境で設計された ER コンフィギュレーションは、コンフィギュレーション評価 (適切な統合プロセス、結果の正確性、パフォーマンス)、およびロールにおけるアクセス権の正確性、職務分掌など品質保証のために、テスト環境にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="7e0b5-153">ER コンフィギュレーションの交換を可能にする機能は、この目的に使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="7e0b5-154">最後に、次の図に示すように、認定された ER コンフィギュレーションは、サービスのサブスクライバーと共有する LCS に、あるいは内部で使用する実稼働環境にアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="7e0b5-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![ER コンフィギュレーション ライフサイクル](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="7e0b5-156">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7e0b5-156">Additional resources</span></span>

[<span data-ttu-id="7e0b5-157">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="7e0b5-157">Electronic reporting overview</span></span>](general-electronic-reporting.md)

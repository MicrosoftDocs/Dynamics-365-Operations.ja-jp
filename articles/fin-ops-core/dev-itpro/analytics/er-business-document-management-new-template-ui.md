---
title: ビジネス ドキュメント管理の新しいドキュメント ユーザー インターフェイス
description: このトピックでは、電子申告のビジネス ドキュメント管理機能で新しいドキュメント ユーザー インターフェイスを使用する方法について説明します。
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f8099f2f6872c34c30de918a6fc5fd27bcde958
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565713"
---
# <a name="new-document-user-interface-in-business-document-management"></a><span data-ttu-id="c406c-103">ビジネス ドキュメント管理の新しいドキュメント ユーザー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c406c-103">New document user interface in Business document management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c406c-104">ビジネス ドキュメント管理により、ビジネス ユーザーは Microsoft 365 サービスまたは適切な Microsoft Office デスクトップ アプリケーションを使用して、ビジネス ドキュメント テンプレートを編集することができます。</span><span class="sxs-lookup"><span data-stu-id="c406c-104">Business document management lets business users edit business document templates by using a Microsoft 365 service or the appropriate Microsoft Office desktop application.</span></span> <span data-ttu-id="c406c-105">編集にはデザインの変更や新しい配置が含まれ、、ユーザーが追加のデータを含めるためのプレースホルダーを追加するのにソース コードを変更する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c406c-105">Edits might include design changes or new deployments, or users might add placeholders to include additional data without having to change the source code.</span></span> <span data-ttu-id="c406c-106">ビジネス ドキュメント管理の使用方法の詳細については、[ビジネス ドキュメント管理の概要](er-business-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c406c-106">For more information about how to work with Business document management, see [Business document management overview](er-business-document-management.md).</span></span>

<span data-ttu-id="c406c-107">新しいドキュメント ユーザー インターフェイス (UI) は、より明確で使いやすくなっています。</span><span class="sxs-lookup"><span data-stu-id="c406c-107">The new document user interface (UI) is clearer and more comfortable to use.</span></span> <span data-ttu-id="c406c-108">**ビジネス ドキュメント** エリアには、現在のプロバイダーに対して使用可能なテンプレートのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c406c-108">The **Business document** area shows only the templates that are available for the current provider.</span></span>

<span data-ttu-id="c406c-109">**新しいドキュメント** ボタンを使用すると、ユーザーは別のプロバイダーによって提供される電子申告 (ER) 形式コンフィギュレーションのテンプレートの作成および編集ができます。</span><span class="sxs-lookup"><span data-stu-id="c406c-109">The **New document** button lets users create and edit a template in an Electronic reporting (ER) format configuration that is provided by another provider.</span></span> <span data-ttu-id="c406c-110">このトピックの例において、プロバイダーは Microsoft です。</span><span class="sxs-lookup"><span data-stu-id="c406c-110">In the example in this topic, the provider is Microsoft.</span></span>

## <a name="make-the-new-document-ui-in-business-document-management-available"></a><span data-ttu-id="c406c-111">ビジネス ドキュメント管理の新しいドキュメント UI を有効にする</span><span class="sxs-lookup"><span data-stu-id="c406c-111">Make the new document UI in Business document management available</span></span>

<span data-ttu-id="c406c-112">ビジネス ドキュメント管理の新しいドキュメント UI の使用を開始するには、**機能管理** ワークスペースで、**ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c406c-112">To start to use the new document UI in Business document management, you must turn on the **Office-like UI experience for Business document management** feature in the **Feature management** workspace.</span></span>

<span data-ttu-id="c406c-113">すべての法人に対してこの機能を有効にするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c406c-113">Follow these steps to turn on this feature for all legal entities.</span></span>

1. <span data-ttu-id="c406c-114">**機能管理** ワークスペースの **新規** タブで、リスト内の **ビジネス ドキュメント管理の Office 同様の UI エクスペリエンス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c406c-114">In the **Feature management** workspace, on the **New** tab, select the **Office-like UI experience for Business document management** feature in the list.</span></span>
2. <span data-ttu-id="c406c-115">**直ちに有効化** を選択し、選択した機能をオンにします。</span><span class="sxs-lookup"><span data-stu-id="c406c-115">Select **Enable now** to turn on the selected feature.</span></span>
3. <span data-ttu-id="c406c-116">ページを更新して、新しい機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="c406c-116">Refresh the page to access the new feature.</span></span>

### <a name="edit-templates-that-are-owned-by-other-providers"></a><span data-ttu-id="c406c-117">他のプロバイダーが所有するテンプレートを編集</span><span class="sxs-lookup"><span data-stu-id="c406c-117">Edit templates that are owned by other providers</span></span>

1. <span data-ttu-id="c406c-118">**ビジネス ドキュメント管理** ワークスペースで、**新規ドキュメント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c406c-118">In the **Business document management** workspace, select **New document**.</span></span>

    ![ビジネス ドキュメント管理のワークスペース](./media/BDM_overview_new_template1.png)

2. <span data-ttu-id="c406c-120">ダイアログ ボックスでテンプレートとして使用するドキュメントを選択し、**ドキュメントの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c406c-120">In the dialog box, select the document to use as a template, and then select **Create document**.</span></span>

    ![ビジネス ドキュメントのダイアログボックス](./media/BDM_overview_new_template2.png)

3. <span data-ttu-id="c406c-122">新規のダイアログボックスの **タイトル** フィールドで、必要に応じてタイトルを変更します。</span><span class="sxs-lookup"><span data-stu-id="c406c-122">In the new dialog box, in the **Title** field, change the title as you require.</span></span> <span data-ttu-id="c406c-123">このタイトル テキストは、自動的に作成される新しい ER 形式コンフィギュレーションに名前を付けるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c406c-123">The title text is used to name the new ER format configuration that is automatically created.</span></span> <span data-ttu-id="c406c-124">このコンフィギュレーション (**顧客 FTI レポート (GER) コピー**) のドラフト バージョンには、編集したテンプレートが含まれ、現在のユーザーに対して ER 形式を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c406c-124">The draft version of this configuration (**Customer FTI report (GER) Copy**) will contain the edited template and will be used to run this ER format for the current user.</span></span> <span data-ttu-id="c406c-125">他のすべてのユーザーは、基本 ER 形式コンフィギュレーションからの元のテンプレートを使用して、この ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="c406c-125">The original template from the base ER format configuration will be used to run this ER format for every other user.</span></span>
4. <span data-ttu-id="c406c-126">**名前** フィールドで、自動的に作成される編集可能なテンプレートの最初のリビジョンの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="c406c-126">In the **Name** field, change the name of the first revision of the editable template that will be automatically created.</span></span>
5. <span data-ttu-id="c406c-127">**コメント** フィールドで、自動的に作成される編集可能なテンプレートのリビジョンの注釈を更新します。</span><span class="sxs-lookup"><span data-stu-id="c406c-127">In the **Comment** field, update the remarks for the revision of the editable template that will be automatically created.</span></span>
6. <span data-ttu-id="c406c-128">**OK** を選択して、編集プロセスの開始を確認します。</span><span class="sxs-lookup"><span data-stu-id="c406c-128">Select **OK** to confirm the start of the editing process.</span></span>

    ![ドキュメント作成のダイアログボックス](./media/BDM_overview_new_template3.png)

<span data-ttu-id="c406c-130">**新規ドキュメント** ボタンは、ユーザーは別のプロバイダーによって提供される電子申告 (ER) 形式コンフィギュレーションのテンプレートの作成および編集のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c406c-130">The **New document** button is used to create and edit a template in an ER format configuration that is provided by another provider.</span></span> <span data-ttu-id="c406c-131">この例において、プロバイダーは Microsoft です。</span><span class="sxs-lookup"><span data-stu-id="c406c-131">In this example, the provider is Microsoft.</span></span> <span data-ttu-id="c406c-132">**新規ドキュメント** を選択すると、現在のプロバイダーと他のプロバイダーが所有するすべてのテンプレートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c406c-132">When you select **New document**, you can view all the templates that are owned by current and other providers.</span></span> <span data-ttu-id="c406c-133">テンプレートを選択すると、編集用に開かれます。</span><span class="sxs-lookup"><span data-stu-id="c406c-133">After you select the template, it's opened for editing.</span></span> <span data-ttu-id="c406c-134">編集したテンプレートは、自動的に生成される新規 ER 形式コンフィギュレーションで保存されます。</span><span class="sxs-lookup"><span data-stu-id="c406c-134">The edited template will then be stored in a new ER format configuration that is automatically generated.</span></span>

<span data-ttu-id="c406c-135">詳細については、[ビジネス ドキュメント管理の概要](er-business-document-management.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c406c-135">For more information, see [Business document management overview](er-business-document-management.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
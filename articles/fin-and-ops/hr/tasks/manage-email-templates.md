---
title: 電子メール テンプレートの管理
description: このトピックでは、電子メールのテンプレートを管理する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationWordBookmark, HRMApplicationEmailTemplate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ecfa720dfa9b3ed6ee15ec68498d2a46612a9ae
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867490"
---
# <a name="manage-email-templates"></a><span data-ttu-id="073eb-103">電子メール テンプレートの管理</span><span class="sxs-lookup"><span data-stu-id="073eb-103">Manage email templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="073eb-104">組織のデータベースから新しいドキュメントのブックマークに情報を転送し、申請者および候補者との効率的なやり取りを支援するテンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="073eb-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="073eb-105">これを行うには、標準テキストを含むテンプレートとシステム データの挿入先となるいくつかのブックマークを作成できます。</span><span class="sxs-lookup"><span data-stu-id="073eb-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="073eb-106">たとえば、申請者の住所と連絡先情報を、申請者とのやり取りに使用できる Microsoft Word 文書に挿入します。</span><span class="sxs-lookup"><span data-stu-id="073eb-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="073eb-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="073eb-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="073eb-108">電子メール テンプレートで使用するブックマークの選択</span><span class="sxs-lookup"><span data-stu-id="073eb-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="073eb-109">ナビゲーション ウィンドウで、**モジュール > 人事管理 > 採用 > 通信 > 申請ブックマーク**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="073eb-109">In the navigation pane, go to **Modules > Human Resources > Recruitment > Communication > Application bookmarks**.</span></span>
2. <span data-ttu-id="073eb-110">一覧で、目的の対応状況を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="073eb-111">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-111">Select **Edit**.</span></span>
4. <span data-ttu-id="073eb-112">選択した対応アクションに関して、電子メール テンプレートに使用できるフィールドを選択し、それらを [ブックマーク] フィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="073eb-112">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="073eb-113">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="073eb-113">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="073eb-114">電子メール テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="073eb-114">Create an email template</span></span>
1. <span data-ttu-id="073eb-115">ナビゲーション ウィンドウで、**モジュール > 人事管理 > 採用 > 通信 > 申請用電子メール テンプレート**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="073eb-115">In the navigation pane, go to **Modules > Human resources > Recruitment > Communication > Application e-mail templates**.</span></span>
2. <span data-ttu-id="073eb-116">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-116">Select **New**.</span></span>
3. <span data-ttu-id="073eb-117">**対応状況** フィールドで、**面接** を選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-117">In the **Correspondence action** field, select **Interview**.</span></span> <span data-ttu-id="073eb-118">この電子メール通信タイプに使用するブックマークを含む対応アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-118">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="073eb-119">**電子メール テンプレート** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="073eb-119">In the **E-mail template** field, type a value.</span></span>
5. <span data-ttu-id="073eb-120">**件名** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="073eb-120">In the **Subject** field, type a value.</span></span>
6. <span data-ttu-id="073eb-121">**テキスト** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="073eb-121">In the **Text** field, type a value.</span></span>
7. <span data-ttu-id="073eb-122">一覧で、目的の [ブックマーク] フィールドを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-122">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="073eb-123">電子メール メッセージの入力を続け、任意の箇所にブックマーク フィールドを挿入します。</span><span class="sxs-lookup"><span data-stu-id="073eb-123">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
9. <span data-ttu-id="073eb-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="073eb-124">Select **Save**.</span></span>


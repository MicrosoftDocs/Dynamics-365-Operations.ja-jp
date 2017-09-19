--- 
title: "電子メール テンプレートの管理"
description: "組織のデータベースから新しいドキュメントのブックマークに情報を転送し、申請者および候補者との効率的なやり取りを支援するテンプレートを使用できます。"
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1eeaf1675b6653ab2c8c04d05ec1bff3cd0bb18d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="manage-email-templates"></a><span data-ttu-id="1e152-103">電子メール テンプレートの管理</span><span class="sxs-lookup"><span data-stu-id="1e152-103">Manage email templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1e152-104">組織のデータベースから新しいドキュメントのブックマークに情報を転送し、申請者および候補者との効率的なやり取りを支援するテンプレートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="1e152-104">You can transfer information from your organization’s database to the bookmarks in a new document and use it in templates that help you communicate efficiently with applicants and candidates.</span></span> <span data-ttu-id="1e152-105">これを行うには、標準テキストを含むテンプレートとシステム データの挿入先となるいくつかのブックマークを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1e152-105">To do this, you create a template that contains standard text and some bookmarks where the system data should be inserted.</span></span> <span data-ttu-id="1e152-106">たとえば、申請者の住所と連絡先情報を、申請者とのやり取りに使用できる Microsoft Word ドキュメントに挿入します。</span><span class="sxs-lookup"><span data-stu-id="1e152-106">For example, you can insert address and contact information for an applicant into a Microsoft Word document that you can use when communicating with that applicant.</span></span> <span data-ttu-id="1e152-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="1e152-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="select-which-bookmarks-to-use-in-your-email-templates"></a><span data-ttu-id="1e152-108">電子メール テンプレートで使用するブックマークの選択</span><span class="sxs-lookup"><span data-stu-id="1e152-108">Select which bookmarks to use in your email templates</span></span>
1. <span data-ttu-id="1e152-109">[申請ブックマーク] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1e152-109">Go to Application bookmarks.</span></span>
2. <span data-ttu-id="1e152-110">一覧で、目的の対応状況を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1e152-110">In the list, find and select the desired correspondence action.</span></span>
3. <span data-ttu-id="1e152-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e152-111">Click Edit.</span></span>
4. <span data-ttu-id="1e152-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="1e152-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1e152-113">選択した対応アクションに関して、電子メール テンプレートに使用できるフィールドを選択し、それらを [ブックマーク] フィールドに移動します。</span><span class="sxs-lookup"><span data-stu-id="1e152-113">Select the fields you would like to be able to use in an email template for the selected Correspondence action and move them to the Bookmark fields.</span></span>  
5. <span data-ttu-id="1e152-114">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1e152-114">Close the page.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="1e152-115">電子メール テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="1e152-115">Create an email template</span></span>
1. <span data-ttu-id="1e152-116">[人事管理] > [採用] > [通信] > [申請用電子メール テンプレート] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="1e152-116">Go to Human resources > Recruitment > Communication > Application e-mail templates.</span></span>
2. <span data-ttu-id="1e152-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e152-117">Click New.</span></span>
3. <span data-ttu-id="1e152-118">[対応状況] フィールドで、[面接] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1e152-118">In the Correspondence action field, select 'Interview'.</span></span>
    * <span data-ttu-id="1e152-119">この電子メール通信タイプに使用するブックマークを含む対応アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1e152-119">Select the correspondence action that contains the bookmarks to use for this type of email communication.</span></span>  
4. <span data-ttu-id="1e152-120">[電子メール テンプレート] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1e152-120">In the E-mail template field, type a value.</span></span>
5. <span data-ttu-id="1e152-121">[件名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1e152-121">In the Subject field, type a value.</span></span>
6. <span data-ttu-id="1e152-122">[テキスト] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1e152-122">In the Text field, type a value.</span></span>
7. <span data-ttu-id="1e152-123">一覧で、目的の [ブックマーク] フィールドを検索し、選択します。</span><span class="sxs-lookup"><span data-stu-id="1e152-123">In the list, find and select the desired bookmark field.</span></span>
8. <span data-ttu-id="1e152-124">電子メール メッセージの入力を続け、任意の箇所にブックマーク フィールドを挿入します。</span><span class="sxs-lookup"><span data-stu-id="1e152-124">Continue typing your email message, inserting the bookmark fields where you need them.</span></span>
    * <span data-ttu-id="1e152-125">電子メール メッセージの入力を続け、任意の箇所にブックマーク フィールドを挿入します。</span><span class="sxs-lookup"><span data-stu-id="1e152-125">Continue typing your email message inserting the bookmark fields where desired.</span></span>  
9. <span data-ttu-id="1e152-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1e152-126">Click Save.</span></span>


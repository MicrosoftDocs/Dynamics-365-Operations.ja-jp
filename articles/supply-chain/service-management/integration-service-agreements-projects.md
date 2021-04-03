---
title: サービス合意とプロジェクトの統合
description: サービス合意およびサービス合意項目を操作する場合、プロジェクト管理と会計の領域で設定するデータを使用します。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd0a7de17e8ff098220fd183b714b77225cc217f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247313"
---
# <a name="integration-for-service-agreements-and-projects"></a><span data-ttu-id="3e1c6-103">サービス合意とプロジェクトの統合</span><span class="sxs-lookup"><span data-stu-id="3e1c6-103">Integration for service agreements and projects</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="3e1c6-104">サービス合意およびサービス合意項目を操作する場合、**プロジェクト管理と会計** の次の領域で設定するデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-104">When you work with service agreements and service agreement lines, you use data that is set up in the following areas in **Project management and accounting**.</span></span>

## <a name="project-prices"></a><span data-ttu-id="3e1c6-105">プロジェクト価格</span><span class="sxs-lookup"><span data-stu-id="3e1c6-105">Project prices</span></span>

<span data-ttu-id="3e1c6-106">サービス合意トランザクションの原価および販売価格は、サービス合意に関連付けられたプロジェクトに適用される原価価格設定から算出されます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-106">The cost and the sales price for a service agreement transaction are derived from the cost price setup that applies to the project that is attached to the service agreement.</span></span> <span data-ttu-id="3e1c6-107">原価価格および販売価格は、プロジェクト、従業員、およびカテゴリ別に設定できます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-107">Cost and sales prices can be set up by project, employee, and category.</span></span> 

## <a name="project-validation"></a><span data-ttu-id="3e1c6-108">プロジェクトの検証</span><span class="sxs-lookup"><span data-stu-id="3e1c6-108">Project validation</span></span>

<span data-ttu-id="3e1c6-109">サービス合意明細行で選択できるプロジェクト、従業員、およびカテゴリは、**プロジェクト管理と会計** の検証設定で制限できます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-109">The projects, employees, and categories that are available for selection on a service agreement line can be limited by the validation setup in **Project management and accounting**.</span></span> <span data-ttu-id="3e1c6-110">検証設定を使用すると、従業員、プロジェクト、およびカテゴリを組み合わせてアクセスを制御できます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-110">By using the validation setup, you can combine employees, projects, and categories for control access.</span></span> 

## <a name="project-line-properties"></a><span data-ttu-id="3e1c6-111">プロジェクト明細行プロパティ</span><span class="sxs-lookup"><span data-stu-id="3e1c6-111">Project line properties</span></span>

<span data-ttu-id="3e1c6-112">明細行プロパティは、サービス合意明細行に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-112">A line property is entered automatically for a service agreement line.</span></span>

<span data-ttu-id="3e1c6-113">明細行プロパティは、**プロジェクト管理と会計** の **明細行プロパティ** フォームで作成されます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-113">Line properties are created in the **Line properties** form in **Project management and accounting**.</span></span> <span data-ttu-id="3e1c6-114">サービス合意に入力される明細行プロパティは、サービス合意に対して選択したプロジェクトに関連付けられ、以降、サービス合意明細行に継承されます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-114">The line property that is entered on a service agreement is attached to the project that is selected for the service agreement and inherited subsequently by the service agreement line.</span></span> 

## <a name="default-offset-accounts"></a><span data-ttu-id="3e1c6-115">既定の相手勘定</span><span class="sxs-lookup"><span data-stu-id="3e1c6-115">Default offset accounts</span></span>

<span data-ttu-id="3e1c6-116">経費トランザクションを入力すると、トランザクションに対して、既定の経費相手勘定が自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-116">If you enter an expense transaction, a default expense offset account is selected automatically for the transaction.</span></span> <span data-ttu-id="3e1c6-117">既定の経費勘定は、現在のサービス合意に関連付けられているプロジェクトに対して設定します。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-117">The default expense account is set up for the project that is attached to the current service agreement.</span></span>

## <a name="project-categories"></a><span data-ttu-id="3e1c6-118">プロジェクト カテゴリ</span><span class="sxs-lookup"><span data-stu-id="3e1c6-118">Project categories</span></span>

<span data-ttu-id="3e1c6-119">サービス合意項目で使用できるカテゴリは、**プロジェクト管理と会計** の **プロジェクト カテゴリ** フォームで設定します。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-119">The categories that are available for service agreement lines are set up in the **Project categories** form in **Project management and accounting**.</span></span> 

> [!NOTE]
> <P><span data-ttu-id="3e1c6-120"><STRONG>プロジェクト カテゴリ</STRONG>フォームの<STRONG>プロジェクト</STRONG>タブの<STRONG>仕訳帳で有効</STRONG>チェック ボックスがオンになっているカテゴリを選択できます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-120">Categories that have the <STRONG>Active in journals</STRONG> check box selected on the <STRONG>Project</STRONG> tab in the <STRONG>Project categories</STRONG> form are available for selection.</span></span> <span data-ttu-id="3e1c6-121">ただし、<STRONG>プロジェクト管理および会計パラメーター</STRONG>フォームの<STRONG>仕訳帳</STRONG>タブで<STRONG>有効ではないカテゴリ</STRONG>チェック ボックスがオンになっている場合、すべてのカテゴリは選択可能です。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-121">However, if the <STRONG>Inactive categories</STRONG> check box is selected on the <STRONG>Journals</STRONG> tab in the <STRONG>Project management and accounting parameters</STRONG> form, all categories are available for selection.</span></span></P>

## <a name="project-parameters"></a><span data-ttu-id="3e1c6-122">プロジェクト パラメーター</span><span class="sxs-lookup"><span data-stu-id="3e1c6-122">Project parameters</span></span>

<span data-ttu-id="3e1c6-123">**プロジェクト管理および会計パラメーター** フォームの **仕訳帳** タブで **退職済作業者** フィールドが選択されている場合、**サービス契約** および **サービス注文** フォームで無効な従業員と有効な従業員を選択できます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-123">If the **Terminated workers** field on the **Journals** tab in the **Project management and accounting parameters** form is selected, you can select inactive employees and active employees in the **Service agreements** and **Service orders** forms.</span></span>

<span data-ttu-id="3e1c6-124">また、**サービス注文** フォームの **プロジェクト** タブで、**開始時刻** および **終了時刻** フィールドを有効にして、サービス注文明細行に開始時刻と終了時刻を入力することもできます。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-124">Also, you can enable the **Start time** and **End time** fields on the **Project** tab in the **Service orders** form to enter starting and ending times on service order lines.</span></span>

## <a name="enable-the-starting-and-ending-time-feature-for-service-orders"></a><span data-ttu-id="3e1c6-125">サービス注文の開始時刻と終了時刻の機能の有効化</span><span class="sxs-lookup"><span data-stu-id="3e1c6-125">Enable the starting and ending time feature for service orders</span></span>

1.  <span data-ttu-id="3e1c6-126">**プロジェクト管理と会計** \> **設定** \> **プロジェクト管理および会計パラメーター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-126">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="3e1c6-127">**仕訳帳** タブをクリックし、**開始時刻と終了時刻の表示** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-127">Click the **Journals** tab, and then select the **Show start/end times** check box.</span></span>

3.  <span data-ttu-id="3e1c6-128">**プロジェクト管理および会計** \> **設定** \> **仕訳帳** \> **仕訳帳名** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-128">Click **Project management and accounting** \> **Setup** \> **Journals** \> **Journal names**.</span></span>

4.  <span data-ttu-id="3e1c6-129">サービス注文に関連付けられている仕訳帳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-129">Select the journal name that is attached to the service order.</span></span>

5.  <span data-ttu-id="3e1c6-130">**一般** タブをクリックし、**開始時刻と終了時刻の表示** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-130">Click the **General** tab, and then select the **Show start/end times** check box.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3e1c6-131"><STRONG>サービス管理パラメーター</STRONG>フォームの<STRONG>仕訳帳</STRONG>タブの<STRONG>時間</STRONG>フィールドで、サービス注文の仕訳帳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="3e1c6-131">Select the journal name for the service order in the <STRONG>Hour</STRONG> field on the <STRONG>Journals</STRONG> tab in the <STRONG>Service management parameters</STRONG> form.</span></span></P>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
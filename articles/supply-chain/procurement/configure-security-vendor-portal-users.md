---
title: 仕入先ポータル ユーザー セキュリティ
description: この記事では、仕入先ポータルを使用する外部仕入先のセキュリティを設定する方法を説明します。 この情報は、2016 年 2 月 &amp; 2016 年 5 月バージョン Dynamics AX にのみ適用されます。
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8539837adc5c5e775d073f142f00afc9f14de669
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807851"
---
# <a name="vendor-portal-user-security"></a><span data-ttu-id="9ea0c-104">仕入先ポータルのユーザー セキュリティ</span><span class="sxs-lookup"><span data-stu-id="9ea0c-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ea0c-105">この記事では、仕入先ポータルを使用する外部仕入先のセキュリティを設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="9ea0c-106">この情報は、2016 年 2 月 &amp; 2016 年 5 月バージョン Dynamics AX にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="9ea0c-107">仕入先のポータルの機能は、Dynamics 365 for Operations バージョン 1611 で拡張された仕入先コラボレーション機能に変わりました。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="9ea0c-108">仕入先コラボレーションのセキュリティ設定の詳細については、「[仕入先共同作業の設定と管理](set-up-maintain-vendor-collaboration.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="9ea0c-109">仕入先ポータルは、外部仕入先に発注書 (PO) に関する限定されたセットの情報を公開します。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="9ea0c-110">お使いの Dynamics AX 環境の追加情報に仕入先が誤ってアクセスしないように、Microsoft Dynamics AX の仕入先ポータルのユーザーのアクセス許可を正しく設定することは重要です。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="9ea0c-111">**重要:** 他のユーザーとは異なり、外部仕入先には **システム ユーザー** ロールがあるべきではありません。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="9ea0c-112">**システム ユーザー** ロールは、外部ユーザーに適していない一連の機能へのアクセスを制御します。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="9ea0c-113">仕入先ポータルのユーザー設定</span><span class="sxs-lookup"><span data-stu-id="9ea0c-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="9ea0c-114">仕入先ポータルを使用する誰かのユーザー アカウントを作成する前に、仕入先ポータルのコラボレーションを設定する仕入先を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="9ea0c-115">**仕入先** ページの **概要** タブにある **発注書コラボレーション** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="9ea0c-116">仕入先ポータルを使用する外部仕入先は、次の設定をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="9ea0c-117">仕入先の Azure Active Directory (AAD) のユーザー アカウントを、Dynamics AX の **ユーザー** ページに登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="9ea0c-118">仕入先には、**システム ユーザー** ロールではなく、**仕入先 (外部)** セキュリティ ロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="9ea0c-119">**注記:** Dynamics AX の新しいユーザー アカウントを作成するとき、**SystemUser** ロールが、自動的に付与されます。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="9ea0c-120">したがって、そのロールを削除して、受信する警告メッセージを知らせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="9ea0c-121">仕入先ユーザーに、発注書のビューに発注書のテーブルから追加のフィールドを追加するアクセス許可を付与すべきではありません。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="9ea0c-122">**ユーザー** タブの、**個人用設定** タブで、**許可された明示的な個人用設定** オプションをユーザーに対し **いいえ** に設定します。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="9ea0c-123">ユーザー アカウントは登録済の連絡担当者と関連付けられる必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="9ea0c-124">**ユーザー** ページの、**名前** フィールドで連絡担当者を選択します。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="9ea0c-125">選択した担当者には、関連する仕入先への **連絡先** ロールがあるべきです。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="9ea0c-126">同じ担当者が複数の仕入先の仕入先ポータルへアクセスする必要がある場合 (おそらく、異なる法人に対して)、その人のユーザー アカウントのそれぞれが、同じ登録済の連絡担当者と関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="9ea0c-127">**仕入先 (外部)** ロールには、仕入先ポータルで使用できる機能を使用するために必要な、すべての基本機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="9ea0c-128">この設定により、外部ユーザーに表示されるユーザー インターフェイスは対象とするシナリオのみにフォーカスするようにできます。</span><span class="sxs-lookup"><span data-stu-id="9ea0c-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9ea0c-129">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9ea0c-129">Additional resources</span></span>
--------

[<span data-ttu-id="9ea0c-130">仕入先ポータルを使用して、仕入先と連携</span><span class="sxs-lookup"><span data-stu-id="9ea0c-130">Collaborate with vendors by using the Vendor portal</span></span>](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
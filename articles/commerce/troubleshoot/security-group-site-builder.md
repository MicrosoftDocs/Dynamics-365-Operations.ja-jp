---
title: 初期配置中に Commerce サイト ビルダーのセキュリティ グループを構成できない
description: このトピックでは、新しい eコマース テナントの初期配置中に、Microsoft Dynamics Lifecycle Services (LCS) で eコマース コンポーネントを作成するときに、Commerce サイト ビルダーの Microsoft Azure Active Directory (Azure AD) セキュリティ グループがオプションとして表示されない場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585414"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="46e31-103">初期配置中に Commerce サイト ビルダーのセキュリティ グループを構成できない</span><span class="sxs-lookup"><span data-stu-id="46e31-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46e31-104">このトピックでは、新しい eコマース テナントの初期配置中に、Microsoft Dynamics Lifecycle Services (LCS) で eコマース コンポーネントを作成するときに、Commerce サイト ビルダーの Microsoft Azure Active Directory (Azure AD) セキュリティ グループがオプションとして表示されない場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="46e31-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="46e31-105">説明</span><span class="sxs-lookup"><span data-stu-id="46e31-105">Description</span></span>

<span data-ttu-id="46e31-106">Commerce サイト ビルダー コンポーネントを含む新しい eコマース テナントを配置するプロセスの一部として eコマース コンポーネントを作成した場合、Azure AD セキュリティ グループはダイアログ ボックスにオプションとして表示されません。</span><span class="sxs-lookup"><span data-stu-id="46e31-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="46e31-107">解像度</span><span class="sxs-lookup"><span data-stu-id="46e31-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="46e31-108">正しいテナントのユーザーでの eコマース サイトのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="46e31-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="46e31-109">[Azure ポータル](https://portal.azure.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="46e31-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="46e31-110">eコマース サイトの LCS プロジェクトがプロビジョニングされたテナントで、[Azure Active Directory を使用して基本グループを作成してメンバーを追加する](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal) の手順に従ってください 。</span><span class="sxs-lookup"><span data-stu-id="46e31-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="46e31-111">[LCS](https://lcs.dynamics.com/) に移動し、作成した Azure AD セキュリティ グループと同じテナントを共有するアカウントを使用してサインインします。</span><span class="sxs-lookup"><span data-stu-id="46e31-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="46e31-112">このアカウントは、Azure AD セキュリティ グループを表示するためのアクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="46e31-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="46e31-113">設定手順を完了して、eコマース サイトを構成します。</span><span class="sxs-lookup"><span data-stu-id="46e31-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="46e31-114">eコマース コンポーネントをプロビジョニングすると、セキュリティ グループがダイアログ ボックスのオプションとして表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="46e31-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="46e31-115">ダイアログ ボックスのフィールドにセキュリティ グループの一覧が表示されるようにするには、作成した Azure AD セキュリティ グループの名前を入力した後に **入力** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46e31-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="46e31-116">検索結果には、ユーザーがアクセスできる、検索テキストで始まるすべての Azure AD セキュリティ グループが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="46e31-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="46e31-117">より短い検索用語を使用して、より広範な検索結果を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="46e31-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46e31-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="46e31-118">Additional resources</span></span>

[<span data-ttu-id="46e31-119">Azure Active Directory を使用して基本グループを作成してメンバーを追加する</span><span class="sxs-lookup"><span data-stu-id="46e31-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="46e31-120">新しい eコマース テナントの配置</span><span class="sxs-lookup"><span data-stu-id="46e31-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)

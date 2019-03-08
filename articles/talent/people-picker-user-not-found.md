---
title: ユーザーが Attract または Onboard の人員ピッカーで見つからない
description: このトピックでは、社内テナントのユーザーが Dynamics 365 for Talent Attract または Onboard アプリケーションの人員ピッカーに表示されない場合の対処方法について説明します。
author: ChrisChua
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: chrichua
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2d4a74ee2cc65153c1f9fdc1b42c2fc440d188d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305218"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="72409-103">Azure Active Directory ユーザーが人員ピッカーで見つからない</span><span class="sxs-lookup"><span data-stu-id="72409-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="72409-104">出庫</span><span class="sxs-lookup"><span data-stu-id="72409-104">Issue</span></span>

<span data-ttu-id="72409-105">テナント用 Microsoft Azure Active Directory (Azure AD) で特定の有効なユーザーが、Dynamics 365 for Talent Attract または Onboard アプリケーションの人員ピッカーで名前を検索する際に表示されません。</span><span class="sxs-lookup"><span data-stu-id="72409-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="72409-106">原因</span><span class="sxs-lookup"><span data-stu-id="72409-106">Cause</span></span>

<span data-ttu-id="72409-107">特定のユーザー タイプは、現在 Attract および Onboard アプリケーションでサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="72409-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="72409-108">ユーザーが Azure AD 企業間 (B2B) ゲスト ユーザーではないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="72409-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="72409-109">「ユーザー タイプ」の情報は、Azure ポータルの Azure Active Directory ブレードにあります。</span><span class="sxs-lookup"><span data-stu-id="72409-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="72409-110">Azure B2B の詳細については、[Azure Active Directory B2B のゲスト ユーザー アクセスとは](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72409-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="72409-111">B2B 以外のユーザーの場合、**ユーザー** オブジェクトに未完了の「ユーザー タイプ」プロパティを持つ可能性のある特定のユーザーがいます。</span><span class="sxs-lookup"><span data-stu-id="72409-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="72409-112">これは、Azure AD Powershell モジュールを使用して検証および修正できます。</span><span class="sxs-lookup"><span data-stu-id="72409-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="72409-113">詳細については、「[Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72409-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="72409-114">解像度</span><span class="sxs-lookup"><span data-stu-id="72409-114">Resolution</span></span>

<span data-ttu-id="72409-115">この問題を解決するにあたり次の手順を実行するために、Azure Active Directory テナントの「グローバル管理者」のアクセス許可または **User.ReadWrite.All** のアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="72409-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="72409-116">影響を受けるユーザーの「ユーザー タイプ」を確認します。</span><span class="sxs-lookup"><span data-stu-id="72409-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="72409-117">コマンドは次の情報を返します。</span><span class="sxs-lookup"><span data-stu-id="72409-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="72409-118">ユーザーの **UserType** プロパティに注意してください。</span><span class="sxs-lookup"><span data-stu-id="72409-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="72409-119">**UserType** が空白、たとえば「メンバー」もしくは「ゲスト」ではない場合、次のコマンドを使用して **UserType** を更新してください。</span><span class="sxs-lookup"><span data-stu-id="72409-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```

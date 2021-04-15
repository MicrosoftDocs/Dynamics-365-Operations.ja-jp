---
title: サインイン リンクが eコマース サイトにリダイレクトする
description: このトピックでは、サインイン リンクがサインイン ページに移動するのではなく、eコマース サイトにリダイレクトする場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
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
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ee2ac8636dad8d31719971b2cc17c8b923f07959
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801462"
---
# <a name="sign-in-link-redirects-back-to-an-e-commerce-site"></a><span data-ttu-id="1ad6d-103">サインイン リンクが eコマース サイトにリダイレクトする</span><span class="sxs-lookup"><span data-stu-id="1ad6d-103">Sign-in link redirects back to an e-commerce site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ad6d-104">このトピックでは、サインイン リンクがサインイン ページに移動するのではなく、eコマース サイトにリダイレクトする場合に役立つトラブルシューティング ガイドを示します。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-104">This topic provides troubleshooting guidance that can help when a sign-in link redirects back to the e-commerce site instead of going to the sign-in page.</span></span>

## <a name="description"></a><span data-ttu-id="1ad6d-105">説明</span><span class="sxs-lookup"><span data-stu-id="1ad6d-105">Description</span></span>

<span data-ttu-id="1ad6d-106">Commerce サイト ビルダーで新しい Microsoft Azure Active Directory B2C (Azure AD B2C) テナントを構成すると、**サインイン** リンクを選択したユーザーは、サインイン ページに移動せずに、主要な eコマースのランディング ページにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-106">After you configure a new Microsoft Azure Active Directory B2C (Azure AD B2C) tenant in Commerce site builder, users who select the **Sign in** link are redirected back to the main e-commerce landing page without going to the sign-in page.</span></span>

## <a name="resolution"></a><span data-ttu-id="1ad6d-107">解像度</span><span class="sxs-lookup"><span data-stu-id="1ad6d-107">Resolution</span></span>

### <a name="confirm-that-the-reply-url-is-correctly-configured-in-the-azure-ad-b2c-application"></a><span data-ttu-id="1ad6d-108">Azure AD B2C アプリケーションで返信 URL が正しく構成されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="1ad6d-108">Confirm that the reply URL is correctly configured in the Azure AD B2C application</span></span>

<span data-ttu-id="1ad6d-109">Azure AD B2C アプリケーションで返信 URL が正しく構成されていることを確認するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-109">To confirm that the reply URL is correctly configured in the Azure AD B2C application, follow these steps.</span></span>

1. <span data-ttu-id="1ad6d-110">[Azure ポータル](https://portal.azure.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-110">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="1ad6d-111">サイト アクセス用に作成した Azure AD B2C アプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-111">Select the Azure AD B2C application that you created for your site access.</span></span>
1. <span data-ttu-id="1ad6d-112">Azure AD B2C の設定中に作成したアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-112">Select the application that you created during the Azure AD B2C setup.</span></span>
1. <span data-ttu-id="1ad6d-113">次の図の例に示すように、**返信 URL** で、リストにサイト ドメイン URL と eコマースが生成した URL の両方のエントリが含まれていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-113">Under **Reply URL**, make sure that the list includes entries for both the site domain URL and the e-commerce-generated URL, as shown in the example in the following illustration.</span></span>

    ![Azure AD B2C 返信 URL エントリ](media/aad-b2c-reply-url.jpg)

> [!NOTE]
> <span data-ttu-id="1ad6d-115">サイト ドメイン URL と eコマースで生成された URL の両方が、先頭または末尾のスラッシュを含まない有効な URL 形式である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ad6d-115">Both the site domain URL and the e-commerce-generated URL must be in a valid URL format that doesn't include leading or trailing slashes.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ad6d-116">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1ad6d-116">Additional resources</span></span>

[<span data-ttu-id="1ad6d-117">Azure Active Directory B2C にWeb アプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="1ad6d-117">Register a web application in Azure Active Directory B2C</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-register-applications?tabs=app-reg-ga#register-a-web-application)

[<span data-ttu-id="1ad6d-118">Commerce での B2C テナントの設定</span><span class="sxs-lookup"><span data-stu-id="1ad6d-118">Set up a B2C tenant in Commerce</span></span>](../set-up-b2c-tenant.md)

---
title: トランザクションと領収書メールに QR コードまたはバーコードを追加
description: このトピックでは、注文 ID を Microsoft Dynamics 365 Commerce のトランザクションと領収書メールに表す QR コードおよびバーコードの入力方法を説明します。
author: bicyclingfool
manager: annbe
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3cc4fcb1237f8409a89b3d4818c132c60c57b5a0
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555425"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="530ed-103">トランザクションと領収書メールに QR コードまたはバーコードを追加</span><span class="sxs-lookup"><span data-stu-id="530ed-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="530ed-104">このトピックでは、注文 ID を Microsoft Dynamics 365 Commerce のトランザクションと領収書メールに表す QR コードおよびバーコードの入力方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="530ed-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="530ed-105">小売環境での注文ルックアップ プロセスを速くするために、トランザクションの電子メールに簡単に QR コードとバーコードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="530ed-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="530ed-106">電子メールに QR コードとバーコードを挿入するには、生成および表示サービスから QR コードとバーコード イメージを要求する HTM **\<img\>** タグを使用します。</span><span class="sxs-lookup"><span data-stu-id="530ed-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="530ed-107">Microsoft は、このサービスを提供しません。</span><span class="sxs-lookup"><span data-stu-id="530ed-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="530ed-108">ただし、クエリ文字列に渡された値に基づき、動的に生成される QR コードまたはバーコードを出すたくさんの無料または安いサービスがあります。</span><span class="sxs-lookup"><span data-stu-id="530ed-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="530ed-109">トランザクション電子メールに QR コードまたはバーコードを追加</span><span class="sxs-lookup"><span data-stu-id="530ed-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="530ed-110">E コマース購買の一部として送信されるトランザクション電子メールに、QR コードまたはバーコードを挿入するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="530ed-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="530ed-111">トランザクション電子メール テンプレートのソース HTML を開き、QR コードまたはバーコード サービスにポイントする HTML **\<img\>** タグを追加します。</span><span class="sxs-lookup"><span data-stu-id="530ed-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="530ed-112">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="530ed-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="530ed-113">前例の内容について説明します:</span><span class="sxs-lookup"><span data-stu-id="530ed-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="530ed-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** は、QR コードまたはコード サービスのドメインを表します。</span><span class="sxs-lookup"><span data-stu-id="530ed-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="530ed-115">**データ** は、QR コードまたはバーコード サービスが、QR コードまたはバーコードとしてレンダリングする必要があるコンテンツを受け取るために使用するパラメータをー表します。</span><span class="sxs-lookup"><span data-stu-id="530ed-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="530ed-116">その値 **%salesid%** は、パラメーターに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="530ed-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="530ed-117">この例では、値がイメージの代替テキストとしても使用されます。</span><span class="sxs-lookup"><span data-stu-id="530ed-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="530ed-118">**param1** および **param2** は、追加のオプション パラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="530ed-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="530ed-119">**小売とコマース \> 本社の設定 \> パラメーター \> 組織の電子メール テンプレート** に移動し、更新済の HTML を適切なトランザクション電子メール テンプレートにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="530ed-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="530ed-120">パラメーターは、QR コードとコード サービス プロバイダ間で異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="530ed-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="530ed-121">したがって、値を割り当てる必要があるパラメータを確認するために、サービス プロバイダーに問い合わせしてください。</span><span class="sxs-lookup"><span data-stu-id="530ed-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="530ed-122">領収書メールに QR コードまたはバーコードを追加</span><span class="sxs-lookup"><span data-stu-id="530ed-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="530ed-123">販売時点設定 (POS) で購買が行われた後に送信するレシートの電子メールに、QR バーコードまたはバーコードを挿入するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="530ed-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="530ed-124">領収書メール テンプレートのソース HTML を開き、QR コードまたはバーコード サービスにポイントする HTML **\<img\>** タグを追加します。</span><span class="sxs-lookup"><span data-stu-id="530ed-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="530ed-125">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="530ed-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="530ed-126">前例の内容について説明します:</span><span class="sxs-lookup"><span data-stu-id="530ed-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="530ed-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** は、QR コードまたはコード サービスのドメインを表します。</span><span class="sxs-lookup"><span data-stu-id="530ed-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="530ed-128">**データ** は、QR コードまたはバーコード サービスが、QR コードまたはバーコードとしてレンダリングする必要があるコンテンツを受け取るために使用するパラメータをー表します。</span><span class="sxs-lookup"><span data-stu-id="530ed-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="530ed-129">その値 **%receiptid%** は、パラメーターに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="530ed-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="530ed-130">この例では、値がイメージの代替テキストとしても使用されます。</span><span class="sxs-lookup"><span data-stu-id="530ed-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="530ed-131">**param1** および **param2** は、追加のオプション パラメーターを表します。</span><span class="sxs-lookup"><span data-stu-id="530ed-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="530ed-132">**小売とコマース \> 本社設定 \> パラメーター \> 組織の電子メール テンプレート** に移動し、更新済の HTML を電子メール ID **emailrecpt** を持つ電子メール テンプレートにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="530ed-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="530ed-133">パラメーターは、QR コードとコード サービス プロバイダ間で異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="530ed-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="530ed-134">したがって、値を割り当てる必要があるパラメータを確認するために、サービス プロバイダーに問い合わせしてください。</span><span class="sxs-lookup"><span data-stu-id="530ed-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="530ed-135">追加リソース</span><span class="sxs-lookup"><span data-stu-id="530ed-135">Additional resources</span></span>

[<span data-ttu-id="530ed-136">Modern POS (MPOS) からの電子メール レシートの送信</span><span class="sxs-lookup"><span data-stu-id="530ed-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="530ed-137">トランザクション イベント用の電子メール テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="530ed-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)

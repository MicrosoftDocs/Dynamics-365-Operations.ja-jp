---
title: レべル 1 Retail Server 仮想マシンに対してデバッグする eコマースの開発環境の設定
description: このトピックでは、レべル 1 Retail Server 仮想マシン (VM) に対してデバッグする eコマースの開発環境を設定する方法について説明します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 38a616c418c3b32490c9adaf69a69af0d47d3478
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019449"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="c2499-103">レべル 1 Retail Server 仮想マシンに対してデバッグする eコマースの開発環境の設定</span><span class="sxs-lookup"><span data-stu-id="c2499-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c2499-104">このトピックでは、レべル 1 Retail Server 仮想マシン (VM) に対してデバッグする eコマースの開発環境を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c2499-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="c2499-105">説明</span><span class="sxs-lookup"><span data-stu-id="c2499-105">Description</span></span>

<span data-ttu-id="c2499-106">Microsoft Dynamics 365 Commerce レベル 1 環境は、通常 Commerce Runtime (CRT) と販売時点管理 (POS) 拡張機能開発用に配置されます。</span><span class="sxs-lookup"><span data-stu-id="c2499-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="c2499-107">これらはスタンドアロンの環境です。</span><span class="sxs-lookup"><span data-stu-id="c2499-107">They are standalone environments.</span></span> <span data-ttu-id="c2499-108">アーキテクチャにおけるサービスとしてのソフトウェア (SaaS) の性質のため、eコマース コンポーネントは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="c2499-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="c2499-109">一部のシナリオでは、レベル 1 環境の拡張機能への呼び出しをテストして、eコマース コンポーネントから拡張機能をデバッグすることができます。</span><span class="sxs-lookup"><span data-stu-id="c2499-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="c2499-110">一般的は手順については、[レベル 1 の Commerce 開発環境に対するデバッグ](../e-commerce-extensibility/debug-tier-1.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c2499-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="c2499-111">レベル 1 環境に対してデバッグする場合、サイトが別の Retail Server を呼び出しているため、サーバー間の呼び出しによって、コンテンツ セキュリティ ポリシーに関連するさまざまなエラーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="c2499-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="c2499-112">次の図は、製品の詳細ページでバリアントが選択されたときに発生する可能性があるエラーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2499-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![製品の詳細ページでバリアントが選択されたときのエラー](media/unhandled-rejection-error.jpg)

<span data-ttu-id="c2499-114">次の図では、ブラウザーのデバッガー ツール (F12 開発者ツール) における同様のエラーの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2499-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="c2499-115">このエラー メッセージには、コンテンツ セキュリティ ポリシー ディレクティブの違反を示しています。</span><span class="sxs-lookup"><span data-stu-id="c2499-115">The error message mentions violation of the content security policy directive.</span></span>

![デバッガー ツールのエラー](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="c2499-117">解像度</span><span class="sxs-lookup"><span data-stu-id="c2499-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="c2499-118">Commerce サイト ビルダーでサイトのコンテンツ セキュリティ ポリシーを無効にする</span><span class="sxs-lookup"><span data-stu-id="c2499-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="c2499-119">作業しているサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="c2499-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="c2499-120">**設定** を選択し、**拡張機能** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2499-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="c2499-121">**コンテンツ セキュリティ ポリシー** タブで、**コンテンツ セキュリティ ポリシーを無効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2499-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="c2499-122">**保存と公開** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c2499-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="c2499-123">企業と顧客間 (B2C) サインインは、ローカルの開発環境では機能しません。</span><span class="sxs-lookup"><span data-stu-id="c2499-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="c2499-124">ただし、必要に応じてゲスト チェックアウトを使用するか、ページ モックを作成して、ユーザーのサインインをシミュレートできます。</span><span class="sxs-lookup"><span data-stu-id="c2499-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2499-125">追加リソース</span><span class="sxs-lookup"><span data-stu-id="c2499-125">Additional resources</span></span>

[<span data-ttu-id="c2499-126">eコマース オンライン拡張機能の開発を開始する</span><span class="sxs-lookup"><span data-stu-id="c2499-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="c2499-127">eコマース サイトでのコンテンツ セキュリティ ポリシー (CSP) の管理</span><span class="sxs-lookup"><span data-stu-id="c2499-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)

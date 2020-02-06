---
title: サイトに言語を追加する
description: このトピックでは、Microsoft Dynamics 365 Commerce サイトに追加の言語のサポートを追加する方法について説明します。
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 111bcaba971b6223f670176135574633d2f1c5ec
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914622"
---
# <a name="add-languages-to-your-site"></a><span data-ttu-id="43962-103">サイトに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="43962-103">Add languages to your site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="43962-104">このトピックでは、Microsoft Dynamics 365 Commerce サイトに追加の言語のサポートを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="43962-104">This topic explains how to add support for additional languages to a Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="43962-105">概要</span><span class="sxs-lookup"><span data-stu-id="43962-105">Overview</span></span>

<span data-ttu-id="43962-106">Web サイトは、Dynamics 365 Commerce がサポートする任意の言語にローカライズできます。</span><span class="sxs-lookup"><span data-stu-id="43962-106">You can localize your website into any language that Dynamics 365 Commerce supports.</span></span> <span data-ttu-id="43962-107">(サポートされている言語の一覧については、このトピックの後半で説明されています。) Web サイトに言語を追加するには、まず、サイトにバインドされているオンライン ストアに言語を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43962-107">(The list of supported languages appears later in this topic.) To add a language on your website, you must first add it to an online store that is bound to your site.</span></span>

## <a name="add-a-language-to-an-online-store"></a><span data-ttu-id="43962-108">オンライン ストアに言語を追加する</span><span class="sxs-lookup"><span data-stu-id="43962-108">Add a language to an online store</span></span>

<span data-ttu-id="43962-109">オンライン ストアに言語を追加するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="43962-109">To add a language to an online store, follow these steps.</span></span>

1. <span data-ttu-id="43962-110">サイトの Dynamics 365 Retail 環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="43962-110">Open the Dynamics 365 Retail environment for your site.</span></span>
1. <span data-ttu-id="43962-111">**Retail \> チャネル \> オンライン ストア**の順に移動して、環境用にコンフィギュレーションされているオンライン ストアの一覧にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="43962-111">Go to **Retail \> Channels \> Online stores** to access the list of online stores that are configured for your environment.</span></span> <span data-ttu-id="43962-112">または、検索用語として**オンライン ストア**を入力します。</span><span class="sxs-lookup"><span data-stu-id="43962-112">Alternatively, enter **online stores** as a search term.</span></span>
1. <span data-ttu-id="43962-113">言語を追加するオンライン ストアを選択します。</span><span class="sxs-lookup"><span data-stu-id="43962-113">Select the online store to add a language for.</span></span>
1. <span data-ttu-id="43962-114">**言語**クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="43962-114">On the **Languages** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="43962-115">**言語**フィールドで、追加する言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="43962-115">In the **Language** field, select the language to add.</span></span>

<span data-ttu-id="43962-116">追加した言語が使用可能になり、サイト作成環境で使用するようにサイトをコンフィギュレーションできるようになります。</span><span class="sxs-lookup"><span data-stu-id="43962-116">The language that you added will now be available so that you can configure your site to use it in the site authoring environment.</span></span>

### <a name="languages-that-are-supported-by-dynamics-365-commerce"></a><span data-ttu-id="43962-117">Dynamics 365 Commerce でサポートされる言語</span><span class="sxs-lookup"><span data-stu-id="43962-117">Languages that are supported by Dynamics 365 Commerce</span></span>

- <span data-ttu-id="43962-118">af</span><span class="sxs-lookup"><span data-stu-id="43962-118">af</span></span>
- <span data-ttu-id="43962-119">ar</span><span class="sxs-lookup"><span data-stu-id="43962-119">ar</span></span>
- <span data-ttu-id="43962-120">ar-ae</span><span class="sxs-lookup"><span data-stu-id="43962-120">ar-ae</span></span>
- <span data-ttu-id="43962-121">ar-bh</span><span class="sxs-lookup"><span data-stu-id="43962-121">ar-bh</span></span>
- <span data-ttu-id="43962-122">ar-dz</span><span class="sxs-lookup"><span data-stu-id="43962-122">ar-dz</span></span>
- <span data-ttu-id="43962-123">ar-eg</span><span class="sxs-lookup"><span data-stu-id="43962-123">ar-eg</span></span>
- <span data-ttu-id="43962-124">ar-iq</span><span class="sxs-lookup"><span data-stu-id="43962-124">ar-iq</span></span>
- <span data-ttu-id="43962-125">ar-jo</span><span class="sxs-lookup"><span data-stu-id="43962-125">ar-jo</span></span>
- <span data-ttu-id="43962-126">ar-kw</span><span class="sxs-lookup"><span data-stu-id="43962-126">ar-kw</span></span>
- <span data-ttu-id="43962-127">ar-lb</span><span class="sxs-lookup"><span data-stu-id="43962-127">ar-lb</span></span>
- <span data-ttu-id="43962-128">ar-ly</span><span class="sxs-lookup"><span data-stu-id="43962-128">ar-ly</span></span>
- <span data-ttu-id="43962-129">ar-ma</span><span class="sxs-lookup"><span data-stu-id="43962-129">ar-ma</span></span>
- <span data-ttu-id="43962-130">ar-om</span><span class="sxs-lookup"><span data-stu-id="43962-130">ar-om</span></span>
- <span data-ttu-id="43962-131">ar-qa</span><span class="sxs-lookup"><span data-stu-id="43962-131">ar-qa</span></span>
- <span data-ttu-id="43962-132">ar-sa</span><span class="sxs-lookup"><span data-stu-id="43962-132">ar-sa</span></span>
- <span data-ttu-id="43962-133">ar-sy</span><span class="sxs-lookup"><span data-stu-id="43962-133">ar-sy</span></span>
- <span data-ttu-id="43962-134">ar-tn</span><span class="sxs-lookup"><span data-stu-id="43962-134">ar-tn</span></span>
- <span data-ttu-id="43962-135">ar-ye</span><span class="sxs-lookup"><span data-stu-id="43962-135">ar-ye</span></span>
- <span data-ttu-id="43962-136">be</span><span class="sxs-lookup"><span data-stu-id="43962-136">be</span></span>
- <span data-ttu-id="43962-137">bg</span><span class="sxs-lookup"><span data-stu-id="43962-137">bg</span></span>
- <span data-ttu-id="43962-138">ca</span><span class="sxs-lookup"><span data-stu-id="43962-138">ca</span></span>
- <span data-ttu-id="43962-139">cs</span><span class="sxs-lookup"><span data-stu-id="43962-139">cs</span></span>
- <span data-ttu-id="43962-140">da</span><span class="sxs-lookup"><span data-stu-id="43962-140">da</span></span>
- <span data-ttu-id="43962-141">de</span><span class="sxs-lookup"><span data-stu-id="43962-141">de</span></span>
- <span data-ttu-id="43962-142">de-at</span><span class="sxs-lookup"><span data-stu-id="43962-142">de-at</span></span>
- <span data-ttu-id="43962-143">de-ch</span><span class="sxs-lookup"><span data-stu-id="43962-143">de-ch</span></span>
- <span data-ttu-id="43962-144">de-li</span><span class="sxs-lookup"><span data-stu-id="43962-144">de-li</span></span>
- <span data-ttu-id="43962-145">de-lu</span><span class="sxs-lookup"><span data-stu-id="43962-145">de-lu</span></span>
- <span data-ttu-id="43962-146">el</span><span class="sxs-lookup"><span data-stu-id="43962-146">el</span></span>
- <span data-ttu-id="43962-147">en-029</span><span class="sxs-lookup"><span data-stu-id="43962-147">en-029</span></span>
- <span data-ttu-id="43962-148">en-au</span><span class="sxs-lookup"><span data-stu-id="43962-148">en-au</span></span>
- <span data-ttu-id="43962-149">en-bz</span><span class="sxs-lookup"><span data-stu-id="43962-149">en-bz</span></span>
- <span data-ttu-id="43962-150">en-ca</span><span class="sxs-lookup"><span data-stu-id="43962-150">en-ca</span></span>
- <span data-ttu-id="43962-151">en-gb</span><span class="sxs-lookup"><span data-stu-id="43962-151">en-gb</span></span>
- <span data-ttu-id="43962-152">en-ie</span><span class="sxs-lookup"><span data-stu-id="43962-152">en-ie</span></span>
- <span data-ttu-id="43962-153">en-in</span><span class="sxs-lookup"><span data-stu-id="43962-153">en-in</span></span>
- <span data-ttu-id="43962-154">en-jm</span><span class="sxs-lookup"><span data-stu-id="43962-154">en-jm</span></span>
- <span data-ttu-id="43962-155">en-my</span><span class="sxs-lookup"><span data-stu-id="43962-155">en-my</span></span>
- <span data-ttu-id="43962-156">en-nz</span><span class="sxs-lookup"><span data-stu-id="43962-156">en-nz</span></span>
- <span data-ttu-id="43962-157">en-sg</span><span class="sxs-lookup"><span data-stu-id="43962-157">en-sg</span></span>
- <span data-ttu-id="43962-158">en-tt</span><span class="sxs-lookup"><span data-stu-id="43962-158">en-tt</span></span>
- <span data-ttu-id="43962-159">ja</span><span class="sxs-lookup"><span data-stu-id="43962-159">en-us</span></span>
- <span data-ttu-id="43962-160">en-za</span><span class="sxs-lookup"><span data-stu-id="43962-160">en-za</span></span>
- <span data-ttu-id="43962-161">es</span><span class="sxs-lookup"><span data-stu-id="43962-161">es</span></span>
- <span data-ttu-id="43962-162">es-ar</span><span class="sxs-lookup"><span data-stu-id="43962-162">es-ar</span></span>
- <span data-ttu-id="43962-163">es-bo</span><span class="sxs-lookup"><span data-stu-id="43962-163">es-bo</span></span>
- <span data-ttu-id="43962-164">es-cl</span><span class="sxs-lookup"><span data-stu-id="43962-164">es-cl</span></span>
- <span data-ttu-id="43962-165">es-co</span><span class="sxs-lookup"><span data-stu-id="43962-165">es-co</span></span>
- <span data-ttu-id="43962-166">es-cr</span><span class="sxs-lookup"><span data-stu-id="43962-166">es-cr</span></span>
- <span data-ttu-id="43962-167">es-do</span><span class="sxs-lookup"><span data-stu-id="43962-167">es-do</span></span>
- <span data-ttu-id="43962-168">es-ec</span><span class="sxs-lookup"><span data-stu-id="43962-168">es-ec</span></span>
- <span data-ttu-id="43962-169">es-gt</span><span class="sxs-lookup"><span data-stu-id="43962-169">es-gt</span></span>
- <span data-ttu-id="43962-170">es-hn</span><span class="sxs-lookup"><span data-stu-id="43962-170">es-hn</span></span>
- <span data-ttu-id="43962-171">es-mx</span><span class="sxs-lookup"><span data-stu-id="43962-171">es-mx</span></span>
- <span data-ttu-id="43962-172">es-ni</span><span class="sxs-lookup"><span data-stu-id="43962-172">es-ni</span></span>
- <span data-ttu-id="43962-173">es-pa</span><span class="sxs-lookup"><span data-stu-id="43962-173">es-pa</span></span>
- <span data-ttu-id="43962-174">es-pe</span><span class="sxs-lookup"><span data-stu-id="43962-174">es-pe</span></span>
- <span data-ttu-id="43962-175">es-pr</span><span class="sxs-lookup"><span data-stu-id="43962-175">es-pr</span></span>
- <span data-ttu-id="43962-176">es-py</span><span class="sxs-lookup"><span data-stu-id="43962-176">es-py</span></span>
- <span data-ttu-id="43962-177">es-sv</span><span class="sxs-lookup"><span data-stu-id="43962-177">es-sv</span></span>
- <span data-ttu-id="43962-178">es-tr</span><span class="sxs-lookup"><span data-stu-id="43962-178">es-tr</span></span>
- <span data-ttu-id="43962-179">es-uy</span><span class="sxs-lookup"><span data-stu-id="43962-179">es-uy</span></span>
- <span data-ttu-id="43962-180">es-ve</span><span class="sxs-lookup"><span data-stu-id="43962-180">es-ve</span></span>
- <span data-ttu-id="43962-181">et</span><span class="sxs-lookup"><span data-stu-id="43962-181">et</span></span>
- <span data-ttu-id="43962-182">eu</span><span class="sxs-lookup"><span data-stu-id="43962-182">eu</span></span>
- <span data-ttu-id="43962-183">fa</span><span class="sxs-lookup"><span data-stu-id="43962-183">fa</span></span>
- <span data-ttu-id="43962-184">fi</span><span class="sxs-lookup"><span data-stu-id="43962-184">fi</span></span>
- <span data-ttu-id="43962-185">fo</span><span class="sxs-lookup"><span data-stu-id="43962-185">fo</span></span>
- <span data-ttu-id="43962-186">fr</span><span class="sxs-lookup"><span data-stu-id="43962-186">fr</span></span>
- <span data-ttu-id="43962-187">fr-be</span><span class="sxs-lookup"><span data-stu-id="43962-187">fr-be</span></span>
- <span data-ttu-id="43962-188">fr-ca</span><span class="sxs-lookup"><span data-stu-id="43962-188">fr-ca</span></span>
- <span data-ttu-id="43962-189">fr-ch</span><span class="sxs-lookup"><span data-stu-id="43962-189">fr-ch</span></span>
- <span data-ttu-id="43962-190">fr-lu</span><span class="sxs-lookup"><span data-stu-id="43962-190">fr-lu</span></span>
- <span data-ttu-id="43962-191">hi</span><span class="sxs-lookup"><span data-stu-id="43962-191">hi</span></span>
- <span data-ttu-id="43962-192">時間</span><span class="sxs-lookup"><span data-stu-id="43962-192">hr</span></span>
- <span data-ttu-id="43962-193">hu</span><span class="sxs-lookup"><span data-stu-id="43962-193">hu</span></span>
- <span data-ttu-id="43962-194">は</span><span class="sxs-lookup"><span data-stu-id="43962-194">is</span></span>
- <span data-ttu-id="43962-195">it</span><span class="sxs-lookup"><span data-stu-id="43962-195">it</span></span>
- <span data-ttu-id="43962-196">it-ch</span><span class="sxs-lookup"><span data-stu-id="43962-196">it-ch</span></span>
- <span data-ttu-id="43962-197">ja</span><span class="sxs-lookup"><span data-stu-id="43962-197">ja</span></span>
- <span data-ttu-id="43962-198">lt</span><span class="sxs-lookup"><span data-stu-id="43962-198">lt</span></span>
- <span data-ttu-id="43962-199">lv</span><span class="sxs-lookup"><span data-stu-id="43962-199">lv</span></span>
- <span data-ttu-id="43962-200">mk</span><span class="sxs-lookup"><span data-stu-id="43962-200">mk</span></span>
- <span data-ttu-id="43962-201">ミリ秒</span><span class="sxs-lookup"><span data-stu-id="43962-201">ms</span></span>
- <span data-ttu-id="43962-202">mt</span><span class="sxs-lookup"><span data-stu-id="43962-202">mt</span></span>
- <span data-ttu-id="43962-203">nb-no</span><span class="sxs-lookup"><span data-stu-id="43962-203">nb-no</span></span>
- <span data-ttu-id="43962-204">nl</span><span class="sxs-lookup"><span data-stu-id="43962-204">nl</span></span>
- <span data-ttu-id="43962-205">nl-be</span><span class="sxs-lookup"><span data-stu-id="43962-205">nl-be</span></span>
- <span data-ttu-id="43962-206">nn-no</span><span class="sxs-lookup"><span data-stu-id="43962-206">nn-no</span></span>
- <span data-ttu-id="43962-207">pl</span><span class="sxs-lookup"><span data-stu-id="43962-207">pl</span></span>
- <span data-ttu-id="43962-208">pt-br</span><span class="sxs-lookup"><span data-stu-id="43962-208">pt-br</span></span>
- <span data-ttu-id="43962-209">ro</span><span class="sxs-lookup"><span data-stu-id="43962-209">ro</span></span>
- <span data-ttu-id="43962-210">ru</span><span class="sxs-lookup"><span data-stu-id="43962-210">ru</span></span>
- <span data-ttu-id="43962-211">ru-ru</span><span class="sxs-lookup"><span data-stu-id="43962-211">ru-ru</span></span>
- <span data-ttu-id="43962-212">sk</span><span class="sxs-lookup"><span data-stu-id="43962-212">sk</span></span>
- <span data-ttu-id="43962-213">sl</span><span class="sxs-lookup"><span data-stu-id="43962-213">sl</span></span>
- <span data-ttu-id="43962-214">sq</span><span class="sxs-lookup"><span data-stu-id="43962-214">sq</span></span>
- <span data-ttu-id="43962-215">sr</span><span class="sxs-lookup"><span data-stu-id="43962-215">sr</span></span>
- <span data-ttu-id="43962-216">sr-la</span><span class="sxs-lookup"><span data-stu-id="43962-216">sr-la</span></span>
- <span data-ttu-id="43962-217">sv</span><span class="sxs-lookup"><span data-stu-id="43962-217">sv</span></span>
- <span data-ttu-id="43962-218">sv-fi</span><span class="sxs-lookup"><span data-stu-id="43962-218">sv-fi</span></span>
- <span data-ttu-id="43962-219">th</span><span class="sxs-lookup"><span data-stu-id="43962-219">th</span></span>
- <span data-ttu-id="43962-220">tn</span><span class="sxs-lookup"><span data-stu-id="43962-220">tn</span></span>
- <span data-ttu-id="43962-221">tr</span><span class="sxs-lookup"><span data-stu-id="43962-221">tr</span></span>
- <span data-ttu-id="43962-222">uk</span><span class="sxs-lookup"><span data-stu-id="43962-222">uk</span></span>
- <span data-ttu-id="43962-223">ur</span><span class="sxs-lookup"><span data-stu-id="43962-223">ur</span></span>
- <span data-ttu-id="43962-224">xh</span><span class="sxs-lookup"><span data-stu-id="43962-224">xh</span></span>
- <span data-ttu-id="43962-225">zh-hans</span><span class="sxs-lookup"><span data-stu-id="43962-225">zh-hans</span></span>
- <span data-ttu-id="43962-226">zh-hk</span><span class="sxs-lookup"><span data-stu-id="43962-226">zh-hk</span></span>
- <span data-ttu-id="43962-227">zh-sg</span><span class="sxs-lookup"><span data-stu-id="43962-227">zh-sg</span></span>
- <span data-ttu-id="43962-228">zu</span><span class="sxs-lookup"><span data-stu-id="43962-228">zu</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43962-229">追加リソース</span><span class="sxs-lookup"><span data-stu-id="43962-229">Additional resources</span></span>

[<span data-ttu-id="43962-230">ロゴの追加</span><span class="sxs-lookup"><span data-stu-id="43962-230">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="43962-231">サイト テーマの選択</span><span class="sxs-lookup"><span data-stu-id="43962-231">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="43962-232">CSS 上書きファイルの作業</span><span class="sxs-lookup"><span data-stu-id="43962-232">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="43962-233">ファビコンの追加</span><span class="sxs-lookup"><span data-stu-id="43962-233">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="43962-234">ようこそメッセージの追加</span><span class="sxs-lookup"><span data-stu-id="43962-234">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="43962-235">著作権に関する注意事項の追加</span><span class="sxs-lookup"><span data-stu-id="43962-235">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="43962-236">サイト ページにスクリプト コードを追加してテレメトリをサポートする</span><span class="sxs-lookup"><span data-stu-id="43962-236">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
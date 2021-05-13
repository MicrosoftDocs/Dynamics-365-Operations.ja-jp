---
title: Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) でプレビューされる機能について説明します。
author: tonyafehr
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-XX-XX
ms.dyn365.ops.version: Platform 26
ms.openlocfilehash: db657179d31337480c4fbf2f095dddd224ecd6b2
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923177"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-platform-update-26-may-2019"></a><span data-ttu-id="30441-103">Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 (2019 年 5 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="30441-103">What's new or changed in Dynamics 365 for Finance and Operations platform update 26 (May 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30441-104">このトピックでは Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="30441-104">This topic describes features that are new or changed in Dynamics 365 for Finance and Operations platform update 26.</span></span> <span data-ttu-id="30441-105">このバージョンのビルド番号は 7.0.5257 です。</span><span class="sxs-lookup"><span data-stu-id="30441-105">This version has a build number of 7.0.5257.</span></span> <span data-ttu-id="30441-106">プラットフォーム更新プログラム 26 の詳細については [追加リソース](whats-new-platform-update-26.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30441-106">For more information about Platform update 26, see [Additional resources](whats-new-platform-update-26.md#additional-resources).</span></span>

## <a name="business-events-generally-available"></a><span data-ttu-id="30441-107">一般的に利用可能なビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="30441-107">Business events generally available</span></span>
<span data-ttu-id="30441-108">[ビジネス イベント](../../dev-itpro/business-events/home-page.md) は現在一般に利用できます。</span><span class="sxs-lookup"><span data-stu-id="30441-108">[Business events](../../dev-itpro/business-events/home-page.md) are now generally available.</span></span> <span data-ttu-id="30441-109">これは、ビジネス イベントがプレビュー外であり、フライトを有効にすることなく既定で利用可能なことを意味します。</span><span class="sxs-lookup"><span data-stu-id="30441-109">This means that business events are out of preview and are available by default, without having to enable the flight.</span></span> 

## <a name="1n-support-for-microsoft-power-automate-to-subscribe-to-business-events"></a><span data-ttu-id="30441-110">Microsoft Power Automate の 1:N サポートでビジネス イベントを購読する</span><span class="sxs-lookup"><span data-stu-id="30441-110">1:N support for Microsoft Power Automate to subscribe to business events</span></span>
<span data-ttu-id="30441-111">複数の Power Automate アプリが、同じ法人内の同じビジネス イベントを購読することができます。</span><span class="sxs-lookup"><span data-stu-id="30441-111">Multiple Power Automate apps can subscribe to the same business event in the same legal entity.</span></span> <span data-ttu-id="30441-112">[Microsoft Power Automate のビジネス イベント](../../dev-itpro/business-events/business-events-flow.md) は通知の送信や承認フローのトリガーなどのタスクに活用できます。</span><span class="sxs-lookup"><span data-stu-id="30441-112">The [Business events in Microsoft Power Automate](../../dev-itpro/business-events/business-events-flow.md) can be leveraged for tasks such as sending notifications and triggering approval flows.</span></span> 

## <a name="workflow-business-events"></a><span data-ttu-id="30441-113">ワークフロー ビジネス イベント</span><span class="sxs-lookup"><span data-stu-id="30441-113">Workflow business events</span></span>
<span data-ttu-id="30441-114">[ワークフロー ビジネス イベント](../../dev-itpro/business-events/business-events-workflow.md) は承認フローのトリガーに特に優れたターゲットです。</span><span class="sxs-lookup"><span data-stu-id="30441-114">The [Workflow business events](../../dev-itpro/business-events/business-events-workflow.md) are a particularly good target for triggering approval flows.</span></span> <span data-ttu-id="30441-115">**ワークフロー作業項目** イベントは、 Power Automate の作業項目の完了を容易にする目的で、検証 および OData 完了アクションと組み合わせて使用できます。</span><span class="sxs-lookup"><span data-stu-id="30441-115">The **Workflow workitem** event can be used in conjunction with the validate and complete OData actions to facilitate completion of a work item in Power Automate.</span></span> <span data-ttu-id="30441-116">作業項目の完成を促進する Power Automate テンプレートは進行中であり、関連するより多くの情報が近い将来 [ワークフロー ビジネス イベント](../../dev-itpro/business-events/business-events-workflow.md)ページで利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="30441-116">Power Automate templates for facilitating completion of a work item are in progress and more information about them will be available on the [Workflow business events](../../dev-itpro/business-events/business-events-workflow.md) page in the near future.</span></span>

## <a name="business-events-are-idempotent"></a><span data-ttu-id="30441-117">ビジネス イベントは、べき等です</span><span class="sxs-lookup"><span data-stu-id="30441-117">Business events are idempotent</span></span>
<span data-ttu-id="30441-118">ビジネス イベントは、べき等です。</span><span class="sxs-lookup"><span data-stu-id="30441-118">Business events are idempotent.</span></span> <span data-ttu-id="30441-119">これはビジネス イベントのペイロードは、ControlNumber と呼ばれる一意で増え続ける番号を持つことを意味します。</span><span class="sxs-lookup"><span data-stu-id="30441-119">This means that the payload of a business event has a unique and ever increasing number called the ControlNumber.</span></span> <span data-ttu-id="30441-120">この制御番号は、イベントの堅牢な処理を確実にするため、重複検出ロジックと故障出荷検出ロジックの適用に顧客が使用できます。</span><span class="sxs-lookup"><span data-stu-id="30441-120">This control number can be used by consumers to apply duplicate detection logic and out of order delivery detection logic to ensure robust processing of events.</span></span>

## <a name="azure-data-lake-integration---cdm-folder-and-model-improvements"></a><span data-ttu-id="30441-121">Azure Data Lake 統合 - CDM フォルダーとモデルの改善</span><span class="sxs-lookup"><span data-stu-id="30441-121">Azure Data Lake integration - CDM folder and model improvements</span></span> 
<span data-ttu-id="30441-122">Azure Data Lake のエンティティ ストアは、プラットフォーム更新プログラム 25 のパブリック プレビューとして利用できます。</span><span class="sxs-lookup"><span data-stu-id="30441-122">Entity store in Azure Data Lake is available as public preview with Platform update 25.</span></span> <span data-ttu-id="30441-123">プラットフォーム更新プログラム 26 では、複数の環境で同じストレージ アカウントを使用できるようにフォルダ構造が改善されました。</span><span class="sxs-lookup"><span data-stu-id="30441-123">In Platform update 26, we have made improvements to the folder structure to enable multiple environments to use the same storage account.</span></span> <span data-ttu-id="30441-124">また、エンティティ間の関係など追加のプロパティもモデルに含めました。</span><span class="sxs-lookup"><span data-stu-id="30441-124">We have also included additional properties in the model, including relationships between entities.</span></span> <span data-ttu-id="30441-125">これは PowerBI.com によって導入された機能を使用して、モデルの関係を Power BI データセットに表示できます。</span><span class="sxs-lookup"><span data-stu-id="30441-125">This will enable relationships in the model to appear in the Power BI dataset with the features introduced by PowerBI.com.</span></span>

## <a name="feature-callouts"></a><span data-ttu-id="30441-126">機能のコールアウト</span><span class="sxs-lookup"><span data-stu-id="30441-126">Feature callouts</span></span>
<span data-ttu-id="30441-127">Finance and Operations の新しい機能が定期的に開発されています。</span><span class="sxs-lookup"><span data-stu-id="30441-127">New features are regularly being developed for Finance and Operations.</span></span> <span data-ttu-id="30441-128">ドキュメントは新機能の説明に役立ちますが、役立つ場合にはユーザーの新機能に対する認識を製品内で直接高めます。</span><span class="sxs-lookup"><span data-stu-id="30441-128">While documentation is helpful for explaining new features, raising awareness of these new capabilities to users directly in the product when they are encountered is powerful.</span></span> <span data-ttu-id="30441-129">このために、プラットフォーム更新プログラム 26 で利用できる [機能のコールアウト](../../dev-itpro/user-interface/feature-callouts.md) はユーザーに新しい機能を示して、オプションで機能の詳細を知るためのハイパーリンクをユーザーに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="30441-129">To this end, [Feature callouts](../../dev-itpro/user-interface/feature-callouts.md) are available in Platform update 26 to point out a new capability to a user and optionally provide a hyperlink for the user to learn more about the feature.</span></span>  

## <a name="extensibility-enhancements"></a><span data-ttu-id="30441-130">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="30441-130">Extensibility enhancements</span></span>
<span data-ttu-id="30441-131">プラットフォーム更新プログラム 26 に含まれる [プラットフォーム拡張機能の 3 番目の波](/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility3) は、2019 年 4 月リリース ノートにドキュメントされています。</span><span class="sxs-lookup"><span data-stu-id="30441-131">The [third wave of platform extensibility enhancements](/business-applications-release-notes/April19/dynamics365-finance-operations/platform-extensibility3) included in Platform update 26 is documented in the April 2019 Release notes.</span></span> <span data-ttu-id="30441-132">7 つの機能強化の詳細が説明されており、強調すべきひとつは、コマンド チェーンが他のメソッド拡張をターゲットにして拡張可能になったことです。</span><span class="sxs-lookup"><span data-stu-id="30441-132">There are seven enhancements detailed, with one of the highlights being that Chain of Command can now target and extend other method extensions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30441-133">追加リソース</span><span class="sxs-lookup"><span data-stu-id="30441-133">Additional resources</span></span>

### <a name="platform-update-26-bug-fixes"></a><span data-ttu-id="30441-134">プラットフォーム アップデート 26 のバグ修正プログラム</span><span class="sxs-lookup"><span data-stu-id="30441-134">Platform update 26 bug fixes</span></span>
<span data-ttu-id="30441-135">プラットフォーム更新 26 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、この [KB 資料](https://fix.lcs.dynamics.com/Issue/Details?bugId=313846&dbType=3&qc=a4ba239cdec6f528657f529750b68845b75580e5fdb0ad6060c4bc33f8da67f8)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30441-135">For information about the bug fixes included in each of the updates that are part of Platform update 26, sign in to Lifecycle Services (LCS) and view this [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=313846&dbType=3&qc=a4ba239cdec6f528657f529750b68845b75580e5fdb0ad6060c4bc33f8da67f8).</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="30441-136">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="30441-136">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="30441-137">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="30441-137">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="30441-138">[2019 年 4 月リリース ノートをご覧ください](/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="30441-138">[Check out the April '19 release notes](/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="30441-139">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="30441-139">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="30441-140">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="30441-140">Removed and deprecated features</span></span>
<span data-ttu-id="30441-141">[Finance and Operations の削除または廃止された機能](../../dev-itpro/migration-upgrade/deprecated-features.md) トピックでは、Dynamics 365 for Finance and Operations の削除または廃止された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="30441-141">The [Removed or deprecated features for Finance and Operations](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="30441-142">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="30441-142">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="30441-143">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="30441-143">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="30441-144">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [Finance and Operations の削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="30441-144">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features for Finance and Operations](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="30441-145">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="30441-145">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="30441-146">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="30441-146">Typically these are functional updates that need to be made to the compiler.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
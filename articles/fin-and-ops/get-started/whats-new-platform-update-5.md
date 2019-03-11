---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 5 (2017 年 3 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 5 の新機能または変更された機能について説明します。 このバージョンは 2017 年 3 月にリリースされ、ビルド番号は 7.0.4475.16165 です。
author: tonyafehr
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 273193
ms.assetid: 025acbbf-7c05-407c-bed2-cde1935e11c9
ms.search.region: Global
ms.author: tfehr
ms.dyn365.ops.version: Platform update 5
ms.search.validFrom: 2017-03-31
ms.openlocfilehash: 2be5f671df4b5eaf53c0186d479a0a3cf46785e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369454"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-5-march-2017"></a><span data-ttu-id="02177-104">Dynamics 365 for Operations プラットフォーム更新プログラム 5 (2017 年 3 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="02177-104">What's new or changed in Dynamics 365 for Operations platform update 5 (March 2017)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="02177-105">このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 5 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="02177-105">This topic describes features that are either new or changed in Dynamics 365 for Operations platform update 5.</span></span> <span data-ttu-id="02177-106">このバージョンは 2017 年 3 月にリリースされ、ビルド番号は 7.0.4475.16165 です。</span><span class="sxs-lookup"><span data-stu-id="02177-106">This version was released in March 2017 and has a build number of 7.0.4475.16165.</span></span>

## <a name="development-and-customization"></a><span data-ttu-id="02177-107">開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="02177-107">Development and customization</span></span>

| <span data-ttu-id="02177-108">機能</span><span class="sxs-lookup"><span data-stu-id="02177-108">Feature</span></span> | <span data-ttu-id="02177-109">これが重要である理由</span><span class="sxs-lookup"><span data-stu-id="02177-109">Why this is important</span></span> |
|---------|-----------------------|
| <span data-ttu-id="02177-110">要求または応答シナリオの EventHandlerResult クラス</span><span class="sxs-lookup"><span data-stu-id="02177-110">EventHandlerResult classes in request or response scenarios</span></span> | <span data-ttu-id="02177-111">デリゲート (イベント) ロジックがサブスクライブ (イベント ハンドラー) を必要とするシナリオに対して EventHandlerResult クラスを使用して、複数のサブスクライブおよび複数の結果があるときに結果が失われないようにするため、少なくとも 1 つの応答を提供できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="02177-111">You can now use the EventHandlerResult class for scenarios where the delegate (event) logic requires its subscribers (event handlers) to provide at least one response so that no result is lost when there are multiple subscribers and multiple results.</span></span> |
| <span data-ttu-id="02177-112">カスタマイズ分析のレポート (CAR) の妥当性</span><span class="sxs-lookup"><span data-stu-id="02177-112">Customization Analysis Report (CAR) justification</span></span> | <span data-ttu-id="02177-113">ベスト プラクティス警告をモデルの AxIgnoreDiagnosticList フォルダーの抑制ファイル内に抑制し、妥当性を含める場合、妥当性テキストがモデルの CAR レポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="02177-113">When you suppress a best practice warning within a suppression file in the AxIgnoreDiagnosticList folder of your model, and include a justification, the justification text will appear in the CAR report of your model.</span></span> <span data-ttu-id="02177-114">妥当性を含む抑制ファイルの例については、&lt;パッケージ ローカル ディレクトリ&gt;\\ディレクトリ\\ディレクトリ\\AxIgnoreDiagnosticList\\ディレクトリ\_BPSuppressions.xml を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02177-114">For an example of a suppression file that includes justifications, see &lt;Packages Local Directory&gt;\\Directory\\Directory\\AxIgnoreDiagnosticList\\Directory\_BPSuppressions.xml.</span></span> |
| <span data-ttu-id="02177-115">テレメトリ</span><span class="sxs-lookup"><span data-stu-id="02177-115">Telemetry</span></span> | <span data-ttu-id="02177-116">モデルが構築されると、テレメトリ フレームワークが、顧客と ISV コードによって参照される Microsoft のクラスおよびメソッドに関する情報を収集します。</span><span class="sxs-lookup"><span data-stu-id="02177-116">When a model is built, the telemetry framework collects information about Microsoft classes and methods that are referenced by customer and ISV code.</span></span> <span data-ttu-id="02177-117">これにより、標準アプリケーション コードのどの部分が下位互換性要件に含まれているかに関する多くの必要な情報が Microsoft に提供されます。</span><span class="sxs-lookup"><span data-stu-id="02177-117">This provides Microsoft with much needed information regarding what part of the standard application code is included in backward compatibility requirements.</span></span> |
| <span data-ttu-id="02177-118">X++ コンパイラおよび try catch ブロック</span><span class="sxs-lookup"><span data-stu-id="02177-118">X++ compiler and try catch blocks</span></span> | <span data-ttu-id="02177-119">これで、X++ コンパイラは、try catchブロック用のわずかに異なるコードを生成します。</span><span class="sxs-lookup"><span data-stu-id="02177-119">The X++ compiler now generates code that is slightly different for try catch blocks.</span></span> <span data-ttu-id="02177-120">以前、システムは DuplicateKey と UpdateConflict 例外を catch all 句の一部としてキャッチしていました。</span><span class="sxs-lookup"><span data-stu-id="02177-120">Before, the system would catch the DuplicateKey and UpdateConflict exceptions as part of the catch all clause.</span></span> <span data-ttu-id="02177-121">これは、取引が実行されているときに try catch が使用された場合、最終的にデータの整合性の問題の原因となる可能性のある問題が発生しました。</span><span class="sxs-lookup"><span data-stu-id="02177-121">This introduced some problems that could ultimately lead to data consistency problems if the try catch was used when a transaction is running.</span></span> <span data-ttu-id="02177-122">ここで、示された 2 つの例外は実行中のトランザクションをロールバックしないため特別であり、catch すべてで取得されなくなります。</span><span class="sxs-lookup"><span data-stu-id="02177-122">Now, the two exceptions mentioned, which are special because they do not roll back a running transaction, are no longer caught in the catch all.</span></span> <span data-ttu-id="02177-123">詳細については、 ブログ投稿の [X++、Catch](https://blogs.msdn.microsoft.com/mfp/2016/11/24/x-the-catch/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02177-123">For more information, see the blog post [X++, the catch](https://blogs.msdn.microsoft.com/mfp/2016/11/24/x-the-catch/).</span></span> |

## <a name="personalization"></a><span data-ttu-id="02177-124">個人用設定</span><span class="sxs-lookup"><span data-stu-id="02177-124">Personalization</span></span>

| <span data-ttu-id="02177-125">機能</span><span class="sxs-lookup"><span data-stu-id="02177-125">Feature</span></span> | <span data-ttu-id="02177-126">これが重要である理由</span><span class="sxs-lookup"><span data-stu-id="02177-126">Why this is important</span></span> |
|---------|-----------------------|
| <span data-ttu-id="02177-127">パーソナル化の拡張された管理機能</span><span class="sxs-lookup"><span data-stu-id="02177-127">Enhanced administration features for personalization</span></span> | <span data-ttu-id="02177-128">パーソナル化管理者は、現在、ユーザー グループのフォームのパーソナル化を適用または削除できます。</span><span class="sxs-lookup"><span data-stu-id="02177-128">The personalization administrator can now apply or remove form personalizations for groups of users.</span></span> <span data-ttu-id="02177-129">以前は、個人用設定の管理は一度に 1 人のユーザーのみ可能でした。</span><span class="sxs-lookup"><span data-stu-id="02177-129">Previously personalization administration was only possible one user at a time.</span></span> <span data-ttu-id="02177-130">詳細については、[ユーザー エクスペリエンスのパーソナライズ](personalize-user-experience.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02177-130">For more information, see [Personalize the user experience](personalize-user-experience.md).</span></span> |

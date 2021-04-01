---
title: 生産フロー バージョンの有効期限の定義
description: 特定の日付の生産フロー バージョンの有効性と処理を終了する、または有効なバージョンから新しいバージョンへの変更を計画するために、バージョンの有効期限を設定する必要があります。
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87063653eb78209caaefd3fafa7783f425e710b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257294"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="f5afb-103">生産フロー バージョンの有効期限の定義</span><span class="sxs-lookup"><span data-stu-id="f5afb-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f5afb-104">特定の日付の生産フロー バージョンの有効性と処理を終了する、または有効なバージョンから新しいバージョンへの変更を計画するために、バージョンの有効期限を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f5afb-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="f5afb-105">そのバージョンを無効化する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f5afb-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="f5afb-106">生産フロー バージョンを終了する有効期限を設定します。</span><span class="sxs-lookup"><span data-stu-id="f5afb-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="f5afb-107">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5afb-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f5afb-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="f5afb-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f5afb-109">既に定義されているバージョンがある生産フローを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5afb-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="f5afb-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5afb-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f5afb-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f5afb-111">Click Edit.</span></span>
5. <span data-ttu-id="f5afb-112">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="f5afb-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f5afb-113">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="f5afb-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="f5afb-114">有効期限においては、新しいバージョンが開始されたり、または有効化されません。</span><span class="sxs-lookup"><span data-stu-id="f5afb-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="f5afb-115">また、この生産フローのジョブを作成するか、または開始することもできなくなります。</span><span class="sxs-lookup"><span data-stu-id="f5afb-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="f5afb-116">しかし、有効期限以降に開始したジョブは完了できます。</span><span class="sxs-lookup"><span data-stu-id="f5afb-116">You can still complete started jobs after the expiration date.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
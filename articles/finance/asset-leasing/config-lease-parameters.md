---
title: リースのパラメーターを構成する (プレビュー版)
description: このトピックでは、セキュリティ情報やアカウンティング設定などの資産リースの構成方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bb8372c5e4a1d7183b5d793b142fed92e833d5a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210436"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="add3c-103">リースのパラメーターを構成する</span><span class="sxs-lookup"><span data-stu-id="add3c-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="add3c-104">構成の設定によっては資産リースの動作に影響します。</span><span class="sxs-lookup"><span data-stu-id="add3c-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="add3c-105">これらの設定には、仕訳帳名、一般パラメーター、転記プロファイルの設定が含まれます。</span><span class="sxs-lookup"><span data-stu-id="add3c-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="add3c-106">**資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="add3c-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="add3c-107">**リース** タブで、**一般** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="add3c-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="add3c-108">**手動での分類の上書きを許可する** パラメータでは、支払スケジュールを確定する前にリースの分類を上書きできるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="add3c-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="add3c-109">現在の法人から他の法人に転記できるかどうかは、**クロスエンティティ バッチ** パラメーターによって決まります。</span><span class="sxs-lookup"><span data-stu-id="add3c-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="add3c-110">このパラメーターがオンになっている場合は、アクセス権のある法人の仕訳帳エントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="add3c-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="add3c-111">**確認済リースの削除を許可する** オプションを **はい** に設定すると、確認済みの支払スケジュールを削除できます。</span><span class="sxs-lookup"><span data-stu-id="add3c-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="add3c-112">転記済または未転記のトランザクションが関連付けられている場合、このオプションを設定してもリースを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="add3c-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="add3c-113">削除されたリース レコードは復元できません。</span><span class="sxs-lookup"><span data-stu-id="add3c-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="add3c-114">削除されたリースのレコードを手動、またはデータエンティティを通じてアップロードした場合、アップロードされた情報は、既存のリースの更新ではなく、新しいものとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="add3c-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="add3c-115">このオプションを **はい** に設定し、帳簿の移行タイプが **累積キャッチアップ オプション A または B** に設定されている場合、システムは **追加借入利子率** フィールドを **帳簿設定** ページの **移行時の追加借入利子率** フィールドの値に設定します。</span><span class="sxs-lookup"><span data-stu-id="add3c-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="add3c-116">このオプションが **いいえ** に設定されている場合、ヘッドリースの金利は、帳簿の種類切替えに関係なく、**帳簿の詳細** ページの **追加借入利子率** フィールドの値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="add3c-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="add3c-117">**決済が完了した帳簿バージョンでの減価償却取消を許可する** オプションを **はい** に設定すると、減価償却経費トランザクションを取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="add3c-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="add3c-118">経費トランザクションは、帳簿のバージョンが決算済であっても取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="add3c-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="add3c-119">このオプションは **いいえ** のままにしておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="add3c-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="add3c-120">このオプションの設定は、決済済みの帳簿が誤って減価償却されないようにする検証と制御に使用されます。</span><span class="sxs-lookup"><span data-stu-id="add3c-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="add3c-121">このオプションを  **いいえ** に設定すると、正味簿価額と将来の減価償却計算を正確に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="add3c-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
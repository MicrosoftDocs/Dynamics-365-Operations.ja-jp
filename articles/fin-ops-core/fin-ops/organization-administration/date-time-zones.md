---
title: 日時データとタイム ゾーン
description: この記事では、日付、日時フィールド、タイム ゾーンに関する情報を提供します。
author: pvillads
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, SystemDate
audience: IT Pro
ms.reviewer: sericks
ms.custom: 13571
ms.assetid: 3ce95bf2-02d7-44b5-95bc-cae6ae27e78e
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d7b018368ade2b8c6ba88c6a9b46811f1fe2a18e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747688"
---
# <a name="datetime-data-and-time-zones"></a><span data-ttu-id="3d83a-103">日時データとタイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="3d83a-103">Date/time data and time zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d83a-104">この記事では、日付、日時フィールド、タイム ゾーンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-104">This article provides information about date and time fields, and time zones.</span></span>

## <a name="date-and-time-fields"></a><span data-ttu-id="3d83a-105">実行日時フィールド</span><span class="sxs-lookup"><span data-stu-id="3d83a-105">Date and time fields</span></span>

<span data-ttu-id="3d83a-106">データベースの異なるデータ型に対応する 3 種類の日付と時刻のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="3d83a-106">There are three types of date and time fields that correspond to different data types in the database:</span></span>

- <span data-ttu-id="3d83a-107">**結合された日時フィールド** – これらのフィールドは推奨される日付と時刻データの入力方法です。</span><span class="sxs-lookup"><span data-stu-id="3d83a-107">**Combined date/time fields** – These fields are the preferred method of entering date and time data.</span></span> <span data-ttu-id="3d83a-108">**utcdatetime** データ型は、単一フィールドの日付と時刻のデータを協定世界時 (UTC) で格納します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-108">The **utcdatetime** data type stores time and date data in a single field in Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3d83a-109">UTC は、世界時で時計と時間が規定される主要な標準時間です。</span><span class="sxs-lookup"><span data-stu-id="3d83a-109">UTC is the primary time standard by which the world regulates clocks and time.</span></span> <span data-ttu-id="3d83a-110">約 1 秒以内で、0 度の経度での太陽時を示し、夏時間には従いません。</span><span class="sxs-lookup"><span data-stu-id="3d83a-110">It is, within about 1 second, mean solar time at 0° longitude; it does not observe daylight saving time.</span></span> <span data-ttu-id="3d83a-111">世界中のタイム ゾーンは、UTC に正または負のオフセットを適用して表されます。</span><span class="sxs-lookup"><span data-stu-id="3d83a-111">Time zones around the world are expressed using positive or negative offsets from UTC.</span></span> <span data-ttu-id="3d83a-112">事実上、UTC がグリニッジ標準時 (GMT) と交換可能であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="3d83a-112">For most purposes, UTC is considered interchangeable with Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="3d83a-113">現在の UTC のバージョンは、国際電気通信連合の勧告 (ITU-R TF.460-6) によって定義されています。</span><span class="sxs-lookup"><span data-stu-id="3d83a-113">The current version of UTC is defined by International Telecommunications Union Recommendation (ITU-R TF.460-6).</span></span>
- <span data-ttu-id="3d83a-114">**日付フィールド** - これらのフィールドは、日付の入力にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d83a-114">**Date fields** – These fields are used to enter dates only.</span></span> <span data-ttu-id="3d83a-115">**date** データ型は、年、月、日を格納します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-115">The **date** data type stores a day, month, and year.</span></span> <span data-ttu-id="3d83a-116">ただし、これらの値は UTC で格納されず、タイム ゾーンに関連付けることもできません。</span><span class="sxs-lookup"><span data-stu-id="3d83a-116">However, these values are not stored in UTC and cannot be associated with a time zone.</span></span>
- <span data-ttu-id="3d83a-117">**時刻フィールド** – これらのフィールドは現在の日付の午前 0 時からの経過秒数を表示するために使用します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-117">**Time fields** – These fields are used to display the number of seconds that have elapsed since midnight on the current date.</span></span> <span data-ttu-id="3d83a-118">**timeofDay** データ型は、整数値を格納します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-118">The **timeofDay** data type stores an integer value.</span></span> <span data-ttu-id="3d83a-119">時刻の値は UTC で格納されません。</span><span class="sxs-lookup"><span data-stu-id="3d83a-119">Time values are not stored in UTC.</span></span>

## <a name="time-zones"></a><span data-ttu-id="3d83a-120">タイム ゾーン</span><span class="sxs-lookup"><span data-stu-id="3d83a-120">Time zones</span></span>

<span data-ttu-id="3d83a-121">UTC 時刻を現地時間で 表すには、タイム ゾーンを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d83a-121">To express UTC times in the local time, you must provide a time zone.</span></span> <span data-ttu-id="3d83a-122">タイム ゾーンは、ローカル時刻に相当する UTC からの補正時間を制御します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-122">The time zone controls the offset from UTC that is the equivalent of the local time.</span></span> <span data-ttu-id="3d83a-123">たとえば、モスクワの補正時間は UTC+3 になります。</span><span class="sxs-lookup"><span data-stu-id="3d83a-123">For example, the offset for Moscow is UTC+3.</span></span> <span data-ttu-id="3d83a-124">優先タイム ゾーンは、コンピュータの Windows ロケールに従って最初に設定されますが、管理者によって変更されている場合もあります。</span><span class="sxs-lookup"><span data-stu-id="3d83a-124">Your preferred time zone is first set according to the Windows locale of your computer, although it might have been changed by an administrator.</span></span> <span data-ttu-id="3d83a-125">優先タイム ゾーンは、結合された日付と時刻を表示する場合にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="3d83a-125">Your preferred time zone is used only when displaying combined dates and times.</span></span> <span data-ttu-id="3d83a-126">ユーザーの優先タイム ゾーンを設定するには、**ユーザー** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-126">To set the preferred time zone for a user, go to **Users** page.</span></span> <span data-ttu-id="3d83a-127">ページにシステムのユーザーのリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d83a-127">The page will show the list of users of the system.</span></span> <span data-ttu-id="3d83a-128">優先タイム ゾーンを設定するユーザーを選択し、**ユーザー オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d83a-128">Select the user that you want to set the preferred time zone for, and click **User options**.</span></span> <span data-ttu-id="3d83a-129">**言語と地域** タブで、優先タイム ゾーンを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d83a-129">On the **Language and region** tab, select the preferred time zone.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
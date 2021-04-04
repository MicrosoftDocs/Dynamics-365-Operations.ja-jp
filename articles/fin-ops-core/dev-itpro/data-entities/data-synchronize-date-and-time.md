---
title: インポート ジョブで日時を同期する
description: インポート ジョブで UTC タイム ゾーンを使用して、タイム ゾーンの変換に関する問題を回避します。
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570484"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="85621-103">インポート ジョブで日時を同期する</span><span class="sxs-lookup"><span data-stu-id="85621-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85621-104">インポート ジョブのタイム ゾーンを協定世界時 (UTC) に設定することが重要です。</span><span class="sxs-lookup"><span data-stu-id="85621-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="85621-105">別の設定を使用すると、インポート データに予期しない日付と時刻が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="85621-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="85621-106">正しい設定を行わないと、インポート プロセスで UTC の日付がローカル形式に変換され、システム設定で再度変換されます。</span><span class="sxs-lookup"><span data-stu-id="85621-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="85621-107">この二重変換によって、アプリケーション間で日付が変更されます。</span><span class="sxs-lookup"><span data-stu-id="85621-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="85621-108">たとえば、二重変換では、ローカル タイム ゾーンの違いにより Dynamics 365 Human Resources と Dynamics 365 Finance の間で従業員の開始日が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="85621-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="85621-109">インポート ジョブを UTC に設定すると、この問題が解決します。</span><span class="sxs-lookup"><span data-stu-id="85621-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="85621-110">Dynamics 365 Finance and Operations で、**データ管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="85621-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="85621-111">**プロジェクトのインポート** を選択し、プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="85621-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="85621-112">**ソースの日付形式** で **CSV-Unicode** を選択します。</span><span class="sxs-lookup"><span data-stu-id="85621-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="85621-113">[![ソースの日付形式を UTC に変更](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="85621-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="85621-114">**タイム ゾーン** を **協定世界タイムゾーン** に変更し、**言語** を **En-US** に変更します。</span><span class="sxs-lookup"><span data-stu-id="85621-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
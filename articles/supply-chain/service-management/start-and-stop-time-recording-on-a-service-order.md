---
title: サービス注文の時刻記録の開始および停止
description: サービス注文の時刻記録を開始および停止します。
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cc205daa35c898147559427b071d1d2c2720de3a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817464"
---
# <a name="start-and-stop-time-recording-on-a-service-order"></a><span data-ttu-id="c29b9-103">サービス注文の時刻記録の開始および停止</span><span class="sxs-lookup"><span data-stu-id="c29b9-103">Start and stop time recording on a service order</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c29b9-104">この手順を使用して、サービス レベルの契約が定義されるサービス注文の時刻記録を開始および停止します。</span><span class="sxs-lookup"><span data-stu-id="c29b9-104">Use this procedure to start and stop time recording for a service order for which a service level agreement is defined.</span></span>

## <a name="start-time-recording"></a><span data-ttu-id="c29b9-105">時刻記録の開始</span><span class="sxs-lookup"><span data-stu-id="c29b9-105">Start time recording</span></span>

1.  <span data-ttu-id="c29b9-106">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c29b9-106">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="c29b9-107">**サービス注文** タブをクリックします。**サービス レベル契約** グループの **アクション ウィンドウ** で、**開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c29b9-107">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Start**.</span></span>

3.  <span data-ttu-id="c29b9-108">時刻記録を開始する日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="c29b9-108">Enter the date and time that the time recording should be started.</span></span>

## <a name="stop-time-recording"></a><span data-ttu-id="c29b9-109">時刻記録の停止</span><span class="sxs-lookup"><span data-stu-id="c29b9-109">Stop time recording</span></span>

1.  <span data-ttu-id="c29b9-110">**サービス管理** \> **共通** \> **サービス注文** \> **サービス注文** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="c29b9-110">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="c29b9-111">**サービス注文** タブをクリックします。**サービス レベル契約** グループの **アクション ウィンドウ** で、**停止** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c29b9-111">Click the **Service order** tab. On the **Action Pane**, in the **Service level agreement** group, click **Stop**.</span></span>

3.  <span data-ttu-id="c29b9-112">時刻記録を停止する日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="c29b9-112">Enter the date and time that the time recording should be stopped.</span></span>

4.  <span data-ttu-id="c29b9-113">**失効理由を追加** を選択し、**ステージ理由コード** リストで理由コードを選択し、時間記録を停止する理由を指定します。</span><span class="sxs-lookup"><span data-stu-id="c29b9-113">Select **Add a revocation reason**, and select a reason code in the **Stage reason code** list to provide a reason for stopping the time recording.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c29b9-114"><STRONG>サービス管理パラメーター</STRONG>フォームで<STRONG>時間超過の理由コード</STRONG>が選択される場合、時刻記録を停止する前に理由コードを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c29b9-114">If <STRONG>Reason code on exceeding time</STRONG> is selected in the <STRONG>Service management parameters</STRONG> form, you must provide a reason code before you can stop the time recording.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="c29b9-115">参照</span><span class="sxs-lookup"><span data-stu-id="c29b9-115">See also</span></span>

<span data-ttu-id="c29b9-116">[SLA 時刻記録の開始 (フォーム)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="c29b9-116">[Start SLA time recording (form)](https://technet.microsoft.com/library/hh242297\(v=ax.60\))</span></span>

<span data-ttu-id="c29b9-117">[SLA 時刻記録の停止 (フォーム)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="c29b9-117">[Stop SLA time recording (form)](https://technet.microsoft.com/library/hh242241\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
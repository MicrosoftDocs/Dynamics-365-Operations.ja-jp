---
title: 完了レポート仕訳帳が転記されるとエラーが発生する
description: 完了レポート仕訳帳を転記すると、注文済み注文数量を減らすことができないというエラー メッセージが表示されます。
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026666"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="60a10-103">完了レポート仕訳帳が転記されるとエラーが発生する</span><span class="sxs-lookup"><span data-stu-id="60a10-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="60a10-104">KB 番号: 4612891</span><span class="sxs-lookup"><span data-stu-id="60a10-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="60a10-105">現象</span><span class="sxs-lookup"><span data-stu-id="60a10-105">Symptoms</span></span>

<span data-ttu-id="60a10-106">**完了レポート** 仕訳帳を転記すると、エラーが発生し 、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="60a10-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="60a10-107">注文済数量を削減できません。十分な数の注文済ステータスの未処理の在庫トランザクションがありません。</span><span class="sxs-lookup"><span data-stu-id="60a10-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="60a10-108">品目は購買、受取り、または登録済みです。</span><span class="sxs-lookup"><span data-stu-id="60a10-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="60a10-109">このエラーは、**完了レポート** 仕訳帳の最初の行で **エラー数量** フィールドが設定され、最後の行で **商品数量** フィールドが設定されている場合にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="60a10-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="60a10-110">最後の行で **エラー数量** フィールドが設定されている場合、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="60a10-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="60a10-111">解像度</span><span class="sxs-lookup"><span data-stu-id="60a10-111">Resolution</span></span>

<span data-ttu-id="60a10-112">このエラーを防ぐには、**生産管理パラメーター** ページを開き、**全般** タブで、**エラー数量を含む残数量の増加** オプションを *はい* に設定します 。</span><span class="sxs-lookup"><span data-stu-id="60a10-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>

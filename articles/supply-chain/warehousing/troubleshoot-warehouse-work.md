---
title: 倉庫作業のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫作業の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837444"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="a7119-103">倉庫作業のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="a7119-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7119-104">このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫作業の処理中に発生する可能性がある問題を修正する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a7119-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="a7119-105">空の払出と空白の入庫が追跡分析コード グループで許可されている場合に、シリアル番号品目を含むライセンス プレートを移動できません。</span><span class="sxs-lookup"><span data-stu-id="a7119-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="a7119-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a7119-106">Issue description</span></span>

<span data-ttu-id="a7119-107">追跡用分析コード グループでシリアル番号が *払出時空白可* および *受入時空白可* に設定されている場合、および同じ場所に複数のライセンス プレートがあり、シリアル番号があるものとないものがある場合、**移動** メニュー項目を使用してライセンス プレートを移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="a7119-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a7119-108">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a7119-108">Issue resolution</span></span>

<span data-ttu-id="a7119-109">この問題は、[KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) で展開された変更によって修正されます。</span><span class="sxs-lookup"><span data-stu-id="a7119-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="a7119-110">この変更により、空白の受入と払出が許可されている場合に、**シリアル番号** フィールドがオプションとして設定されます。</span><span class="sxs-lookup"><span data-stu-id="a7119-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="a7119-111">移動処理を行うとき、倉庫管理モバイル アプリで次のエラー メッセージを受信します: "このプロセスでは、在庫所有者 %1 が許可されていません。"</span><span class="sxs-lookup"><span data-stu-id="a7119-111">I receive the following error message in the Warehouse Management mobile app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="a7119-112">問題の説明</span><span class="sxs-lookup"><span data-stu-id="a7119-112">Issue description</span></span>

<span data-ttu-id="a7119-113">倉庫管理モバイル アプリを使用して移動を行うときに、**所有者** 追跡用分析コードが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="a7119-113">The **Owner** tracking dimension is missing when the Warehouse Management mobile app is used to make movements.</span></span> <span data-ttu-id="a7119-114">Supply Chain Management クライアントからの通常の在庫移動仕訳帳が意図したとおりに機能し、**所有者** 分析コードが入力されている場合にのみ転記できます。</span><span class="sxs-lookup"><span data-stu-id="a7119-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="a7119-115">問題の解決</span><span class="sxs-lookup"><span data-stu-id="a7119-115">Issue resolution</span></span>

<span data-ttu-id="a7119-116">Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。</span><span class="sxs-lookup"><span data-stu-id="a7119-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="a7119-117">現在、倉庫管理プロセスでは、法人によって所有されている在庫のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="a7119-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
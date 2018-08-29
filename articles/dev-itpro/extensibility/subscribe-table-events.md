---
title: "テーブル レコードの有効期間中の業務処理の実行"
description: "このトピックでは、テーブル レコードの有効期間中に実行できる業務処理に関する情報を提供します。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/11/2017
ms.topic: index-page
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f3caf7db2165ecdf3ef93c51ba9e8761854e6f87
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="perform-business-actions-throughout-the-lifecycle-of-table-records"></a><span data-ttu-id="ca669-103">テーブル レコードの有効期間中の業務処理の実行</span><span class="sxs-lookup"><span data-stu-id="ca669-103">Perform business actions throughout the lifecycle of table records</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca669-104">ビジネス ワークフローの一環として、レコードは定期的に挿入、更新、および削除されます。</span><span class="sxs-lookup"><span data-stu-id="ca669-104">As part of your business workflows, records are regularly inserted, updated, and deleted.</span></span> <span data-ttu-id="ca669-105">システムの動作をカスタマイズするために、最も頻繁に使用される一部のレコード操作にフックすることができます。</span><span class="sxs-lookup"><span data-stu-id="ca669-105">To customize the system behavior, you can hook into some of the record operations that are most often used.</span></span> <span data-ttu-id="ca669-106">たとえば、レコードの追加のフィールドに入力、追加のデータ検証を実行、または関連するテーブルに追加データを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="ca669-106">For example, you can fill additional fields on the record, perform additional data validation, or insert additional data into related tables.</span></span> <span data-ttu-id="ca669-107">テーブルで利用できる複数のイベントを使用して、拡張機能を通じてこれらのカスタマイズを実現できます。</span><span class="sxs-lookup"><span data-stu-id="ca669-107">Several events that are available on the table let you achieve those customizations through extensions.</span></span> <span data-ttu-id="ca669-108">コードによって、これらのイベントをサブスクライブすることが、またはイベントの実行の前後にロジックを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="ca669-108">Your code can subscribe to these events, and can insert your logic before or after the event is run.</span></span>

<span data-ttu-id="ca669-109">サブスクライブできるイベントの一覧については、[拡張機能とオーバーレイによるカスタマイズ](customization-overlayering-extensions.md#table-extensions)にある「テーブルの拡張機能」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ca669-109">For a list of the events that you can subscribe to, see the "Table extensions" section in [Customize with extensions and overlayering](customization-overlayering-extensions.md#table-extensions).</span></span>


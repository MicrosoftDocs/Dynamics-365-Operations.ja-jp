---
title: テーブル レコードの有効期間中の業務処理の実行
description: このトピックでは、テーブル レコードの有効期間中に実行できる業務処理に関する情報を提供します。
author: ivanv-microsoft
ms.date: 07/11/2017
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: a71e833329544e40c86a9e144c162e1e8f3c89e5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744217"
---
# <a name="perform-business-actions-throughout-the-lifecycle-of-table-records"></a><span data-ttu-id="76788-103">テーブル レコードの有効期間中の業務処理の実行</span><span class="sxs-lookup"><span data-stu-id="76788-103">Perform business actions throughout the lifecycle of table records</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76788-104">ビジネス ワークフローの一環として、レコードは定期的に挿入、更新、および削除されます。</span><span class="sxs-lookup"><span data-stu-id="76788-104">As part of your business workflows, records are regularly inserted, updated, and deleted.</span></span> <span data-ttu-id="76788-105">システムの動作をカスタマイズするために、最も頻繁に使用される一部のレコード操作にフックすることができます。</span><span class="sxs-lookup"><span data-stu-id="76788-105">To customize the system behavior, you can hook into some of the record operations that are most often used.</span></span> <span data-ttu-id="76788-106">たとえば、レコードの追加のフィールドに入力、追加のデータ検証を実行、または関連するテーブルに追加データを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="76788-106">For example, you can fill additional fields on the record, perform additional data validation, or insert additional data into related tables.</span></span> <span data-ttu-id="76788-107">テーブルで利用できる複数のイベントを使用して、拡張機能を通じてこれらのカスタマイズを実現できます。</span><span class="sxs-lookup"><span data-stu-id="76788-107">Several events that are available on the table let you achieve those customizations through extensions.</span></span> <span data-ttu-id="76788-108">コードによって、これらのイベントをサブスクライブすることが、またはイベントの実行の前後にロジックを挿入することができます。</span><span class="sxs-lookup"><span data-stu-id="76788-108">Your code can subscribe to these events, and can insert your logic before or after the event is run.</span></span>

<span data-ttu-id="76788-109">サブスクライブできるイベントの一覧については、[拡張機能とオーバーレイによるカスタマイズ](customization-overlayering-extensions.md#table-extensions)にある「テーブルの拡張機能」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="76788-109">For a list of the events that you can subscribe to, see the "Table extensions" section in [Customize through extension and overlayering](customization-overlayering-extensions.md#table-extensions).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
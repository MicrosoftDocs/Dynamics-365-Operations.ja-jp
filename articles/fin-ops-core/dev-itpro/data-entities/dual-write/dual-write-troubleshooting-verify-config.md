---
title: Finance and Operations アプリと Common Data Service でデュアル書き込みの構成を確認する
description: このトピックでは、Finance and Operations アプリと Common Data Service 間でデュアル書き込みが構成されているかどうかを確認する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997233"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="21381-103">Finance and Operations アプリと Common Data Service でデュアル書き込みの構成を確認する</span><span class="sxs-lookup"><span data-stu-id="21381-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="21381-104">このトピックでは、Finance and Operations アプリと Common Data Service 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="21381-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="21381-105">このトピックでは、Finance and Operations アプリと Common Data Service 間でデュアル書き込みの構成を確認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="21381-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="21381-106">Finance and Operations アプリでデュアル書き込みが構成されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="21381-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="21381-107">更新プログラムでレコードの保存時に発生したエラーがデュアル書き込みに起因するものであるかどうかを確認するには、まずデュアル書き込みが構成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="21381-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="21381-108">Finance and Operations アプリで管理者権限が付与されている場合は、 **ワークスペース \> データ管理** に移動して、 **デュアル書き込み** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="21381-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="21381-109">リンクされた環境の詳細と実行中のエンティティ マッピングの一覧が表示される場合は、デュアル書き込みが構成されています。</span><span class="sxs-lookup"><span data-stu-id="21381-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![管理者権限が付与されている場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_1.png)

+ <span data-ttu-id="21381-111">管理者権限が付与されていない場合は、 *エンティティ \<entity name\>にデータを書き込めません* というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="21381-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="21381-112">次の図に示す例では、Finance and Operations アプリで顧客レコードを作成することはできません。デュアル書き込みが構成されているものの、Common Data Service に顧客グループおよび支払条件参照データがに存在しないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="21381-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![管理者権限が付与されていない場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_2.png)

<span data-ttu-id="21381-114">Finance and Operations アプリでデータを作成する際に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21381-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="21381-115">Common Data Service アプリでデュアル書き込みが構成されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="21381-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="21381-116">データの作成時に、Common Data Service ページに **会社** フィールドが表示されている場合は、デュアル書き込みが構成されています。</span><span class="sxs-lookup"><span data-stu-id="21381-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Common Data Service の接続を確認します](media/verify_cds.png)

<span data-ttu-id="21381-118">Common Data Service でデータの作成時に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21381-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="21381-119">Common Data Service でデータの作成時にエラーが発生した場合にエラーの詳細の確認する方法については、[ Common Data Service でプラグイン追跡ログを有効化してエラーの詳細を確認する](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="21381-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>

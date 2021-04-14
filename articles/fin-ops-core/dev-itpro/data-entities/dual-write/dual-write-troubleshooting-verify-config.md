---
title: Finance and Operations アプリと Dataverse でのデュアル書き込み構成の検証
description: このトピックでは、Finance and Operations アプリと Dataverse 間でデュアル書き込みが構成されているかどうかを確認する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748852"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="66007-103">Finance and Operations アプリと Dataverse でのデュアル書き込み構成の検証</span><span class="sxs-lookup"><span data-stu-id="66007-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="66007-104">このトピックでは、Finance and Operations アプリと Dataverse 間のデュアル書き込み統合に関するトラブルシューティングの情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="66007-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="66007-105">このトピックでは、Finance and Operations アプリと Dataverse 間でデュアル書き込みの構成を確認する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="66007-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="66007-106">Finance and Operations アプリでデュアル書き込みが構成されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="66007-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="66007-107">更新プログラムで行の保存時に発生したエラーがデュアル書き込みに起因するものであるかどうかを確認するには、まずデュアル書き込みが構成されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="66007-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="66007-108">Finance and Operations アプリで管理者権限が付与されている場合は、**ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="66007-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="66007-109">リンクされた環境の詳細と実行中のテーブル マップの一覧が表示される場合は、デュアル書き込みが構成されています。</span><span class="sxs-lookup"><span data-stu-id="66007-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![管理者権限が付与されている場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_1.png)

+ <span data-ttu-id="66007-111">管理者権限が付与されていない場合は、*エンティティ \<entity name\>にデータを書き込めません* というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="66007-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="66007-112">次の図に示す例では、Finance and Operations アプリで顧客行を作成することはできません。デュアル書き込みが構成されているものの、Dataverse に顧客グループおよび支払条件参照データがに存在しないことが原因です。</span><span class="sxs-lookup"><span data-stu-id="66007-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![管理者権限が付与されていない場合に Finance and Operations アプリの接続を確認する](media/verify_fin_ops_2.png)

<span data-ttu-id="66007-114">Finance and Operations アプリでデータを作成する際に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66007-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="66007-115">Dataverse アプリでデュアル書き込みが構成されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="66007-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="66007-116">データの作成時に、Dataverse ページに **会社** 列が表示されている場合は、デュアル書き込みが構成されています。</span><span class="sxs-lookup"><span data-stu-id="66007-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Dataverse の接続を確認します](media/verify_cds.png)

<span data-ttu-id="66007-118">Dataverse でデータの作成時に発生する問題の修正方法については、[ライブ同期に関する問題のトラブルシューティング](dual-write-troubleshooting-live-sync.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66007-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="66007-119">Dataverse でデータの作成時にエラーが発生した場合にエラーの詳細の確認する方法については、[ Dataverse でプラグイン追跡ログを有効化してエラーの詳細を確認する](dual-write-troubleshooting.md#enable-view-trace) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66007-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
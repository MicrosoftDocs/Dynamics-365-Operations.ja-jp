---
title: "銀行仕訳帳の複合エンティティの更新"
description: "追加のBankTransactionType フィールドに複合 BankJournalEntity を追加するには以下の手順が必要です。"
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 18b2b228f287a946eb18536b1ea93b0d6af6900c
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="6c80f-103">銀行仕訳帳の複合エンティティの更新</span><span class="sxs-lookup"><span data-stu-id="6c80f-103">Update the bank journal composite entity</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6c80f-104">追加のBankTransactionType フィールドに複合 BankJournalEntity を追加するには以下の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="6c80f-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="6c80f-105">次の手順を使用して、複合の BankJournalEntity に追加の BankTransactionType フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="6c80f-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="6c80f-106">次の銀行仕訳帳の複合エンティティ、エンティティ、ステージング テーブルをコンパイルして同期:</span><span class="sxs-lookup"><span data-stu-id="6c80f-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="6c80f-107">複合エンティティ\\銀行仕訳帳エンティティ</span><span class="sxs-lookup"><span data-stu-id="6c80f-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="6c80f-108">エンティティ\\銀行仕訳帳ヘッダー エンティティ</span><span class="sxs-lookup"><span data-stu-id="6c80f-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="6c80f-109">エンティティ\\銀行仕訳帳明細行エンティティ</span><span class="sxs-lookup"><span data-stu-id="6c80f-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="6c80f-110">テーブル\\銀行仕訳帳ヘッダー ステージング</span><span class="sxs-lookup"><span data-stu-id="6c80f-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="6c80f-111">テーブル\\銀行仕訳帳明細行ステージング</span><span class="sxs-lookup"><span data-stu-id="6c80f-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="6c80f-112">データ管理\\データ プロジェクト</span><span class="sxs-lookup"><span data-stu-id="6c80f-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="6c80f-113">**データ ソース**レイアウトの**銀行トランザクション**タイプを公開します。</span><span class="sxs-lookup"><span data-stu-id="6c80f-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="6c80f-114">ソースデータ形式 = XML-Element</span><span class="sxs-lookup"><span data-stu-id="6c80f-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="6c80f-115">エンティティ名 = 銀行仕訳帳</span><span class="sxs-lookup"><span data-stu-id="6c80f-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="6c80f-116">データ ファイルのアップロード = 新しいバージョンの SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="6c80f-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="6c80f-117">既存のファイルを上書きするには、[**はい**]をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c80f-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="6c80f-118">最初からマッピングを生成するためには、[**はい**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c80f-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="6c80f-119">銀行トランザクション タイプがマップされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c80f-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="6c80f-120">明細行エンティティの [**マップの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6c80f-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="6c80f-121">銀行トランザクション タイプがソースからステージングにマップされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="6c80f-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="6c80f-122">新しい明細書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="6c80f-122">Import the new statement.</span></span>






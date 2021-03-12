---
title: 銀行仕訳帳の複合エンティティの更新
description: 追加のBankTransactionType フィールドに複合 BankJournalEntity を追加するには以下の手順が必要です。
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6c990208f26dde26b7adc306198f7cd16e0e69b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978917"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="7bb8e-103">銀行仕訳帳の複合エンティティの更新</span><span class="sxs-lookup"><span data-stu-id="7bb8e-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bb8e-104">追加のBankTransactionType フィールドに複合 BankJournalEntity を追加するには以下の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="7bb8e-105">次の手順を使用して、複合の BankJournalEntity に追加の BankTransactionType フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="7bb8e-106">次の銀行仕訳帳の複合エンティティ、エンティティ、ステージング テーブルをコンパイルして同期:</span><span class="sxs-lookup"><span data-stu-id="7bb8e-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="7bb8e-107">複合エンティティ\\銀行仕訳帳エンティティ</span><span class="sxs-lookup"><span data-stu-id="7bb8e-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="7bb8e-108">エンティティ\\銀行仕訳帳ヘッダー エンティティ</span><span class="sxs-lookup"><span data-stu-id="7bb8e-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="7bb8e-109">エンティティ\\銀行仕訳帳明細行エンティティ</span><span class="sxs-lookup"><span data-stu-id="7bb8e-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="7bb8e-110">テーブル\\銀行仕訳帳ヘッダー ステージング</span><span class="sxs-lookup"><span data-stu-id="7bb8e-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="7bb8e-111">テーブル\\銀行仕訳帳明細行ステージング</span><span class="sxs-lookup"><span data-stu-id="7bb8e-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="7bb8e-112">データ管理\\データ プロジェクト</span><span class="sxs-lookup"><span data-stu-id="7bb8e-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="7bb8e-113">**データ ソース** レイアウトの **銀行トランザクション** タイプを公開します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="7bb8e-114">ソースデータ形式 = XML-Element</span><span class="sxs-lookup"><span data-stu-id="7bb8e-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="7bb8e-115">エンティティ名 = 銀行仕訳帳</span><span class="sxs-lookup"><span data-stu-id="7bb8e-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="7bb8e-116">データ ファイルのアップロード = 新しいバージョンの SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="7bb8e-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="7bb8e-117">既存のファイルを上書きするには、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="7bb8e-118">最初からマッピングを生成するためには、**はい** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="7bb8e-119">銀行トランザクション タイプがマップされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="7bb8e-120">明細行エンティティの **マップの表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="7bb8e-121">銀行トランザクション タイプがソースからステージングにマップされたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="7bb8e-122">新しい明細書をインポートします。</span><span class="sxs-lookup"><span data-stu-id="7bb8e-122">Import the new statement.</span></span>





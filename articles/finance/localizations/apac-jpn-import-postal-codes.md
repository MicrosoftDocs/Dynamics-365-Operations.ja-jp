---
title: 日本の郵便番号のインポート
description: このトピックでは、日本の郵便番号をインポートする方法について説明します。
author: yijialuan
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 384e8debce3fc5ca74d054b4c5aa6ed9548f11b0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175794"
---
# <a name="import-postal-codes-for-japan"></a><span data-ttu-id="d4214-103">日本の郵便番号のインポート</span><span class="sxs-lookup"><span data-stu-id="d4214-103">Import postal codes for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4214-104">日本では、日本郵便局が Dynamics 365 Finance にインポート可能な郵便番号コード ファイルを提供します。</span><span class="sxs-lookup"><span data-stu-id="d4214-104">In Japan, the Japan Postal Office provides a ZIP code file that you can import into Dynamics 365 Finance.</span></span> <span data-ttu-id="d4214-105">このトピックでは、郵便番号をインポートするためのプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d4214-105">This topic walks you through the process for importing ZIP/postal codes.</span></span> <span data-ttu-id="d4214-106">この例では、デモ データの会社 JPMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="d4214-106">This example uses the JPMF demo data company.</span></span>

## <a name="prepare-the-zip-code-file"></a><span data-ttu-id="d4214-107">郵便番号コード ファイルを準備します。</span><span class="sxs-lookup"><span data-stu-id="d4214-107">Prepare the ZIP code file</span></span>

1. <span data-ttu-id="d4214-108">[日本郵便局のホーム ページ](https://www.post.japanpost.jp/zipcode/download.html) からコンマ区切り値 (CSV) ファイルをダウンロードします</span><span class="sxs-lookup"><span data-stu-id="d4214-108">Download the comma-separated values (CSV) file from the [Japan Postal Office home page](https://www.post.japanpost.jp/zipcode/download.html).</span></span>
2. <span data-ttu-id="d4214-109">ファイルを編集するために開き、列見出しのために次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="d4214-109">Open the file for editing, and add the following row for column headings.</span></span>

        LocalAuthCode,OldZipCode,ZipCode,PrefectureName,KanaCity,KanaStreetName,State,City,StreetName,MoreZipCodeFlag,SmallerAreaFlag,StreetChomeFlag,MoreStreetFlag,UpdateFlag,Reason

3. <span data-ttu-id="d4214-110">ファイルで、7 桁に満たない郵便番号コードには前にゼロを追加します。</span><span class="sxs-lookup"><span data-stu-id="d4214-110">In the file, add zeros before any ZIP code that has fewer than seven digits.</span></span> <span data-ttu-id="d4214-111">(7 桁に満たない郵便番号コードは認められません。)</span><span class="sxs-lookup"><span data-stu-id="d4214-111">(ZIP codes that have fewer than seven digits won't be accepted.)</span></span>

## <a name="create-a-data-import-project-and-import-the-data"></a><span data-ttu-id="d4214-112">データのインポート プロジェクトを作成し、データをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d4214-112">Create a data import project and import the data</span></span>
1. <span data-ttu-id="d4214-113">**システム管理** > **ワークスペース** > **データ管理**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d4214-113">Go **System administration** > **Workspaces** > **Data management**.</span></span>
2. <span data-ttu-id="d4214-114">**インポート**をクリックしてインポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d4214-114">Click **Import** to create an import project.</span></span>
3. <span data-ttu-id="d4214-115">名前を入力し、**日本の郵便番号**をエンティティの名前として選択します。</span><span class="sxs-lookup"><span data-stu-id="d4214-115">Enter a name, and select **ZIP Postal Code Japan** as the entity name.</span></span>
4. <span data-ttu-id="d4214-116">データ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="d4214-116">Upload the data file.</span></span>
5. <span data-ttu-id="d4214-117">**インポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d4214-117">Click **Import**.</span></span>
6. <span data-ttu-id="d4214-118">インポート プロセスの結果を検証します。</span><span class="sxs-lookup"><span data-stu-id="d4214-118">Validate the results of the import process.</span></span>
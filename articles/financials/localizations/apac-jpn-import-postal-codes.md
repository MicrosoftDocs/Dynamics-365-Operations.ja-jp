---
title: "日本の郵便番号のインポート"
description: "このトピックでは、日本の郵便番号をインポートする方法について説明します。"
author: yijialuan
manager: AnnBe
ms.date: 05/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 86929c3a9be668fbaefd2c7cfda8b266ef9c638e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="import-postal-codes-for-japan"></a><span data-ttu-id="24f14-103">日本の郵便番号のインポート</span><span class="sxs-lookup"><span data-stu-id="24f14-103">Import postal codes for Japan</span></span>

<span data-ttu-id="24f14-104">日本では、日本郵便局が Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition にインポート可能な郵便番号コード ファイルを提供します。</span><span class="sxs-lookup"><span data-stu-id="24f14-104">In Japan, the Japan Postal Office provides a ZIP code file that you can import into Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="24f14-105">このトピックでは、郵便番号をインポートするためのプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="24f14-105">This topic walks you through the process for importing ZIP/postal codes.</span></span> <span data-ttu-id="24f14-106">この例では、デモ データの会社 JPMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="24f14-106">This example uses the JPMF demo data company.</span></span>

## <a name="prepare-the-zip-code-file"></a><span data-ttu-id="24f14-107">郵便番号コード ファイルを準備します。</span><span class="sxs-lookup"><span data-stu-id="24f14-107">Prepare the ZIP code file</span></span>

1. <span data-ttu-id="24f14-108">日本郵便局のホーム ページからコンマ区切り値 (CSV) ファイルをダウンロードします: <http://www.post.japanpost.jp/zipcode/download.html></span><span class="sxs-lookup"><span data-stu-id="24f14-108">Download the comma-separated values (CSV) file from the Japan Postal Office home page: <http://www.post.japanpost.jp/zipcode/download.html></span></span>
2. <span data-ttu-id="24f14-109">ファイルを編集するために開き、列見出しのために次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="24f14-109">Open the file for editing, and add the following row for column headings.</span></span>

        LocalAuthCode,OldZipCode,ZipCode,PrefectureName,KanaCity,KanaStreetName,State,City,StreetName,MoreZipCodeFlag,SmallerAreaFlag,StreetChomeFlag,MoreStreetFlag,UpdateFlag,Reason

3. <span data-ttu-id="24f14-110">ファイルで、7 桁に満たない郵便番号コードには前にゼロを追加します。</span><span class="sxs-lookup"><span data-stu-id="24f14-110">In the file, add zeros before any ZIP code that has fewer than seven digits.</span></span> <span data-ttu-id="24f14-111">(7 桁に満たない郵便番号コードは認められません。)</span><span class="sxs-lookup"><span data-stu-id="24f14-111">(ZIP codes that have fewer than seven digits won't be accepted.)</span></span>

## <a name="create-a-data-import-project-and-import-the-data"></a><span data-ttu-id="24f14-112">データのインポート プロジェクトを作成し、データをインポートします。</span><span class="sxs-lookup"><span data-stu-id="24f14-112">Create a data import project and import the data</span></span>
1. <span data-ttu-id="24f14-113">[**システム管理**] > [**ワークスペース**] > [**データ管理**] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="24f14-113">Go **System administration** > **Workspaces** > **Data management**.</span></span>
2. <span data-ttu-id="24f14-114">[**インポート**] をクリックしてインポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="24f14-114">Click **Import** to create an import project.</span></span>
3. <span data-ttu-id="24f14-115">名前を入力し、[**日本の郵便番号**] をエンティティの名前として選択します。</span><span class="sxs-lookup"><span data-stu-id="24f14-115">Enter a name, and select **ZIP Postal Code Japan** as the entity name.</span></span>
4. <span data-ttu-id="24f14-116">データ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="24f14-116">Upload the data file.</span></span>
5. <span data-ttu-id="24f14-117">[**インポート**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="24f14-117">Click **Import**.</span></span>
6. <span data-ttu-id="24f14-118">インポート プロセスの結果を検証します。</span><span class="sxs-lookup"><span data-stu-id="24f14-118">Validate the results of the import process.</span></span>


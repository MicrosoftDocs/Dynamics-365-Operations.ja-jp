---
title: 日本の郵便番号のインポート
description: このトピックでは、日本の郵便番号をインポートする方法について説明します。
author: yijialuan
manager: AnnBe
ms.date: 11/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 49e6f5efda8cb06b6dc083df875cd76371331644
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258171"
---
# <a name="import-postal-codes-for-japan"></a><span data-ttu-id="f2268-103">日本の郵便番号のインポート</span><span class="sxs-lookup"><span data-stu-id="f2268-103">Import postal codes for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2268-104">日本では、日本郵便局が Dynamics 365 Finance にインポート可能な郵便番号コード ファイルを提供します。</span><span class="sxs-lookup"><span data-stu-id="f2268-104">In Japan, the Japan Postal Office provides a ZIP code file that you can import into Dynamics 365 Finance.</span></span> <span data-ttu-id="f2268-105">このトピックでは、郵便番号をインポートするためのプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f2268-105">This topic walks you through the process for importing ZIP/postal codes.</span></span> <span data-ttu-id="f2268-106">この例では、デモ データの会社 JPMF を使用します。</span><span class="sxs-lookup"><span data-stu-id="f2268-106">This example uses the JPMF demo data company.</span></span>

## <a name="prepare-the-zip-code-file"></a><span data-ttu-id="f2268-107">郵便番号コード ファイルを準備します。</span><span class="sxs-lookup"><span data-stu-id="f2268-107">Prepare the ZIP code file</span></span>

1. <span data-ttu-id="f2268-108">[日本郵便局のホーム ページ](https://www.post.japanpost.jp/zipcode/download.html) からコンマ区切り値 (CSV) ファイルをダウンロードします</span><span class="sxs-lookup"><span data-stu-id="f2268-108">Download the comma-separated values (CSV) file from the [Japan Postal Office home page](https://www.post.japanpost.jp/zipcode/download.html).</span></span>

2. <span data-ttu-id="f2268-109">ファイルを開いて、ファイル エンコードを「Shift JIS」から「UTF-16 LE」に変換します (メモ帳 ++ などのフリー ソフトウェアを使用してソース ファイルを開き、エンコードを UCS-2 LE BOM に変換することができます)。</span><span class="sxs-lookup"><span data-stu-id="f2268-109">Open the file and convert the file encoding from “Shift-JIS” to “UTF-16 LE” (you can use free software such as Notepad++ for Windows to open the source file and convert the encode to UCS-2 LE BOM.)</span></span>

3. <span data-ttu-id="f2268-110">編集のためファイルを開き、列見出しのために次の行を追加します。</span><span class="sxs-lookup"><span data-stu-id="f2268-110">Open the file for editing, and add the following row for the column headings.</span></span>

    ```Text
    LocalAuthCode,OldZipCode,ZipCode,PrefectureName,KanaCity,KanaStreetName,State,City,StreetName,MoreZipCodeFlag,SmallerAreaFlag,StreetChomeFlag,MoreStreetFlag,UpdateFlag,Reason
    ```
    
4. <span data-ttu-id="f2268-111">ファイルで、7 桁に満たない郵便番号コードには前にゼロを追加します。</span><span class="sxs-lookup"><span data-stu-id="f2268-111">In the file, add zeros before any ZIP code that has fewer than seven digits.</span></span> <span data-ttu-id="f2268-112">7 桁に満たない郵便番号コードは認められません。</span><span class="sxs-lookup"><span data-stu-id="f2268-112">ZIP codes that have fewer than seven digits won't be accepted.)</span></span>

## <a name="create-a-data-import-project-and-import-the-data"></a><span data-ttu-id="f2268-113">データのインポート プロジェクトを作成し、データをインポートします。</span><span class="sxs-lookup"><span data-stu-id="f2268-113">Create a data import project and import the data</span></span>
1. <span data-ttu-id="f2268-114">**システム管理** > **ワークスペース** > **データ管理** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f2268-114">Go **System administration** > **Workspaces** > **Data management**.</span></span>
2. <span data-ttu-id="f2268-115">**インポート** をクリックしてインポート プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f2268-115">Click **Import** to create an import project.</span></span>
3. <span data-ttu-id="f2268-116">名前を入力し、**日本の郵便番号** をエンティティの名前として選択します。</span><span class="sxs-lookup"><span data-stu-id="f2268-116">Enter a name, and select **ZIP Postal Code Japan** as the entity name.</span></span>
4. <span data-ttu-id="f2268-117">データ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f2268-117">Upload the data file.</span></span>
5. <span data-ttu-id="f2268-118">インポート プロジェクトのソース ファイル形式を「CSV (Unicode)」に設定します。</span><span class="sxs-lookup"><span data-stu-id="f2268-118">Set the source file format of the importing project to “CSV(Unicode)”.</span></span>
6. <span data-ttu-id="f2268-119">**インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f2268-119">Click **Import**.</span></span>
7. <span data-ttu-id="f2268-120">結果を検証します。</span><span class="sxs-lookup"><span data-stu-id="f2268-120">Validate the results.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
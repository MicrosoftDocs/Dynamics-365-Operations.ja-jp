--- 
title: "JBA 支払ファイル形式の有効化 (日本)"
description: "日本では、電子資金決済 (EFT) のファイル形式は全国銀行協会 (JBA) により指定されています。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4e9ff0f343f622cc7891bc707af784cd25de77ae
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="enable-the-jba-payment-file-format-japan"></a><span data-ttu-id="5d6de-103">JBA 支払ファイル形式の有効化 (日本)</span><span class="sxs-lookup"><span data-stu-id="5d6de-103">Enable the JBA payment file format (Japan)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d6de-104">日本では、電子資金決済 (EFT) のファイル形式は全国銀行協会 (JBA) により指定されています。</span><span class="sxs-lookup"><span data-stu-id="5d6de-104">In Japan, the Japanese Bankers Association (JBA) has specified a file format for electronic fund transfers (EFT).</span></span> 



<span data-ttu-id="5d6de-105">この手順では、JBA の支払モデルのインポートおよび仕入先の支払方法に対する JBA の支払ファイルの有効化について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d6de-105">This procedure walks you through importing the JBA payment model and enabling the JBA payment file for vendor methods of payment.</span></span> 



<span data-ttu-id="5d6de-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="5d6de-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="import-the-jba-payment-model"></a><span data-ttu-id="5d6de-107">JBA 支払モデルのインポート</span><span class="sxs-lookup"><span data-stu-id="5d6de-107">Import the JBA payment model</span></span>
1. <span data-ttu-id="5d6de-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d6de-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5d6de-109">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d6de-109">Click Repositories.</span></span>
3. <span data-ttu-id="5d6de-110">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d6de-110">Click Open.</span></span>
4. <span data-ttu-id="5d6de-111">ツリー内で、[支払モデル] \JBA [支払いモデル] \JBA [支払ファイル (JP)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d6de-111">In the tree, select 'Payment model\JBA Payment model\JBA Payment file (JP)'.</span></span>
5. <span data-ttu-id="5d6de-112">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d6de-112">Click Import.</span></span>
6. <span data-ttu-id="5d6de-113">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d6de-113">Click Yes.</span></span>

## <a name="use-the-jba-payment-file-in-the-vendor-method-of-payment"></a><span data-ttu-id="5d6de-114">仕入先の支払方法での JBA 支払ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="5d6de-114">Use the JBA payment file in the vendor method of payment</span></span>
1. <span data-ttu-id="5d6de-115">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d6de-115">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="5d6de-116">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d6de-116">Click Edit.</span></span>
3. <span data-ttu-id="5d6de-117">[ファイル形式] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="5d6de-117">Expand or collapse the File formats section.</span></span>
4. <span data-ttu-id="5d6de-118">[一般的な電子申告] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="5d6de-118">Select the Generic electronic reporting check box.</span></span>
5. <span data-ttu-id="5d6de-119">[書式設定のコンフィギュレーションのエクスポート] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5d6de-119">In the Export format configuration field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5d6de-120">一覧で、JBA [支払ファイル (JP)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d6de-120">In the list, select JBA Payment file (JP).</span></span>
7. <span data-ttu-id="5d6de-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d6de-121">Click Save.</span></span>


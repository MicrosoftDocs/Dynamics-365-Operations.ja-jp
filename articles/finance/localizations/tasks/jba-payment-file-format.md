---
title: JBA 支払ファイル形式の有効化
description: 日本では、電子資金決済 (EFT) のファイル形式は全国銀行協会 (JBA) により指定されています。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport,  VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 870526dc1019e65ca1b0337ef85d17aa1f6375a3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988281"
---
# <a name="enable-the-jba-payment-file-format"></a><span data-ttu-id="dce47-103">JBA 支払ファイル形式の有効化</span><span class="sxs-lookup"><span data-stu-id="dce47-103">Enable the JBA payment file format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dce47-104">日本では、電子資金決済 (EFT) のファイル形式は全国銀行協会 (JBA) により指定されています。</span><span class="sxs-lookup"><span data-stu-id="dce47-104">In Japan, the Japanese Bankers Association (JBA) has specified a file format for electronic fund transfers (EFT).</span></span> 



<span data-ttu-id="dce47-105">この手順では、JBA の支払モデルのインポートおよび仕入先の支払方法に対する JBA の支払ファイルの有効化について説明します。</span><span class="sxs-lookup"><span data-stu-id="dce47-105">This procedure walks you through importing the JBA payment model and enabling the JBA payment file for vendor methods of payment.</span></span> 



<span data-ttu-id="dce47-106">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="dce47-106">This procedure was created using the demo data company JPMF.</span></span>


## <a name="import-the-jba-payment-model"></a><span data-ttu-id="dce47-107">JBA 支払モデルのインポート</span><span class="sxs-lookup"><span data-stu-id="dce47-107">Import the JBA payment model</span></span>
1. <span data-ttu-id="dce47-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dce47-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="dce47-109">[リポジトリ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce47-109">Click Repositories.</span></span>
3. <span data-ttu-id="dce47-110">[開く] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce47-110">Click Open.</span></span>
4. <span data-ttu-id="dce47-111">ツリー内で、[支払モデル] \JBA [支払いモデル] \JBA [支払ファイル (JP)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="dce47-111">In the tree, select 'Payment model\JBA Payment model\JBA Payment file (JP)'.</span></span>
5. <span data-ttu-id="dce47-112">[インポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce47-112">Click Import.</span></span>
6. <span data-ttu-id="dce47-113">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce47-113">Click Yes.</span></span>

## <a name="use-the-jba-payment-file-in-the-vendor-method-of-payment"></a><span data-ttu-id="dce47-114">仕入先の支払方法での JBA 支払ファイルの使用</span><span class="sxs-lookup"><span data-stu-id="dce47-114">Use the JBA payment file in the vendor method of payment</span></span>
1. <span data-ttu-id="dce47-115">[買掛金勘定] > [支払設定] > [支払方法] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dce47-115">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="dce47-116">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce47-116">Click Edit.</span></span>
3. <span data-ttu-id="dce47-117">[ファイル形式] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="dce47-117">Expand or collapse the File formats section.</span></span>
4. <span data-ttu-id="dce47-118">[一般的な電子申告] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="dce47-118">Select the Generic electronic reporting check box.</span></span>
5. <span data-ttu-id="dce47-119">[書式設定のコンフィギュレーションのエクスポート] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="dce47-119">In the Export format configuration field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dce47-120">一覧で、JBA [支払ファイル (JP)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="dce47-120">In the list, select JBA Payment file (JP).</span></span>
7. <span data-ttu-id="dce47-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dce47-121">Click Save.</span></span>


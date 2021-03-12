---
title: レジスターの作成と関連付け
description: この手順では、販売時点管理 (POS) レジスターを作成する方法を示します。
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2415945c5a8f73e095627d638fcc572c50ffe8ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964898"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="584ce-103">レジスターの作成と関連付け</span><span class="sxs-lookup"><span data-stu-id="584ce-103">Create and associate registers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="584ce-104">この手順では、販売時点管理 (POS) レジスターを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="584ce-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="584ce-105">この手順では、デモ データ会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="584ce-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="584ce-106">小売りとコマース > チャネル設定 > POS 設定 > レジスターの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="584ce-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="584ce-107">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="584ce-107">Click New.</span></span>
3. <span data-ttu-id="584ce-108">[レジスター番号] フィールドに、新しいレジスターの ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="584ce-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="584ce-109">レジスター ID には、レジスターを所属する店舗とその店舗内の場所にマップするためのコードが通常含まれます。</span><span class="sxs-lookup"><span data-stu-id="584ce-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="584ce-110">[名前] フィールドに、レジスターの内容を説明する名前を入力します..</span><span class="sxs-lookup"><span data-stu-id="584ce-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="584ce-111">[店舗番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="584ce-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="584ce-112">[ハードウェア プロファイル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="584ce-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="584ce-113">ハードウェア プロファイルはキャッシュ ドロワーやレシート プリンターなど、レジスターに接続される周辺機器を指定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="584ce-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="584ce-114">[ビジュアル プロファイル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="584ce-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="584ce-115">視覚プロファイルは POS のバックグラウンド、ログイン ページ、および POS のテーマで使用されている画像を指定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="584ce-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="584ce-116">[EFT POS レジスター番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="584ce-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="584ce-117">EFT POS レジスター番号はどの支払ターミナルが認証要求を送信しているかを支払処理担当者に通知するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="584ce-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="584ce-118">この値は、"ターミナル ID" または "TID" と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="584ce-118">This value is often called the "Terminal ID" or "TID".</span></span> <span data-ttu-id="584ce-119">TID は、支払デバイスのステッカーの明細行から見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="584ce-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="584ce-120">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="584ce-120">Click Save.</span></span>


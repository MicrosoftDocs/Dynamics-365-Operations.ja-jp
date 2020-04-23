---
title: Dynamics 365 for Finance and Operations – Warehousing アプリでのカメラを使用したバーコードのスキャン
description: このトピックでは、モバイル デバイスでカメラを使用してバーコードをスキャンするため Dynamics 365 for Finance and Operations – Warehousing アプリを設定する方法について説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9d3b807b18a0a9c7d24763a2a2a7ea9eccf9c2bb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205866"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a><span data-ttu-id="a8fc1-103">Dynamics 365 Supply Chain Management – Warehousing アプリでのカメラを使用したバーコードのスキャン</span><span class="sxs-lookup"><span data-stu-id="a8fc1-103">Scan bar codes using a camera in Dynamics 365 Supply Chain Management - Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8fc1-104">このトピックでは、モバイル デバイスでカメラを使用してバーコードをスキャンするため Dynamics 365 for Finance and Operations – Warehousing アプリを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-104">This topic explains how to set up Dynamics 365 for Finance and Operations – Warehousing app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="a8fc1-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="a8fc1-105">Prerequisites</span></span>
<span data-ttu-id="a8fc1-106">この機能を使用するには、インストールされている Warehousing アプリのバージョン 1.2.0.0 が必要であり、デバイスにはカメラが必要です。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-106">To use this feature, you need to have version 1.2.0.0 of the Warehousing app installed, and your device must have a camera.</span></span> <span data-ttu-id="a8fc1-107">更新した後にアプリを開く際に、カメラを使用するアプリを許可するように求められます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="a8fc1-108">デバイスにカメラがない場合、プロンプトは表示されず、カメラをスキャナーとして使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="a8fc1-109">段取り</span><span class="sxs-lookup"><span data-stu-id="a8fc1-109">Setup</span></span>
<span data-ttu-id="a8fc1-110">Warehousing アプリケーションの表示設定では、バーコードのスキャンにカメラを使用すべきかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="a8fc1-111">**スキャナーとしてカメラを使用** を有効にした場合、優先入力モードを **スキャン** に設定した各入力フィールドでカメラを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="a8fc1-112">入力フィールドをスキャン可能にする必要があるかどうかをコントロールするには、**倉庫保管アプリ フィールド名**ページで、**優先入力モード**を**スキャン**に設定します。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="a8fc1-113">このオプションが選択されている場合、倉庫保管アプリでスキャンするのにカメラを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="a8fc1-114">Warehousing でアプリ フィールド名を構成する方法については、[倉庫保管アプリでアプリ フィールド名をコンフィギュレーションする](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="a8fc1-115">サポートされているバーコード形式</span><span class="sxs-lookup"><span data-stu-id="a8fc1-115">Supported bar code formats</span></span>
<span data-ttu-id="a8fc1-116">サポートされている最も一般的なバーコード形式には、コード 128、コード 39、コード 93、EAN-8、EAN-13、UPC-E、UPC-A、および QR コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="a8fc1-117">ナビゲーション</span><span class="sxs-lookup"><span data-stu-id="a8fc1-117">Navigation</span></span>
<span data-ttu-id="a8fc1-118">カメラ ページは、優先入力モードをスキャンに設定した入力フィールドの各ページで開始されます。カメラ ページに来ると次のオプションを使用して移動します。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="a8fc1-119">[タスクと詳細] ページに戻るには [戻る] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="a8fc1-120">手動で入力するためのページに移動するには [タスクと詳細] ページにある鉛筆をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="a8fc1-121">[カメラ] ページに戻るには [タスクと詳細] ページでカメラをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="a8fc1-122">[タスクと詳細] ページ</span><span class="sxs-lookup"><span data-stu-id="a8fc1-122">Task and details page</span></span> | <span data-ttu-id="a8fc1-123">[カメラ] ページ</span><span class="sxs-lookup"><span data-stu-id="a8fc1-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![カメラ スキャンのタスク例の詳細ページ](./media/camera-scanning-example-task-detail-page50.png)          | ![カメラ スキャン例のカメラ ページをもっと小さくする](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="a8fc1-126">[カメラ] ページで、[カメラ] ボタンをクリックすると、バー コードを識別しようとしているときにグレー表示になります。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="a8fc1-127">バーコードが 5 秒以内で識別されない場合は、プロセスがタイムアウトになり、[カメラ] ボタンがもう一度利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="a8fc1-128">それからもう一度バーコードをスキャンすることができます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="a8fc1-129">バーコードにカメラの視点を定めると、最適な結果で、バーコードはかっこ内に合わせられた状態になります。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="a8fc1-130">バーコードが正常にスキャンされると、結果が処理され、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="a8fc1-131">次の手順で優先入力モードが [スキャン] に設定された別の入力フィールドを含む場合、[カメラ] ページが再び開始します。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="a8fc1-132">次の手順が [スキャン] フィールドでない場合、[カメラ] ページは開始しません。</span><span class="sxs-lookup"><span data-stu-id="a8fc1-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>


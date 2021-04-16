---
title: Warehouse Management モバイル アプリでカメラを使用してバーコードをスキャンする
description: このトピックでは、Warehouse Management モバイル アプリを設定して、モバイル デバイスでカメラを使用してバーコードをスキャンする方法について説明します。
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831221"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="d05eb-103">Warehouse Management モバイル アプリでカメラを使用してバーコードをスキャンする</span><span class="sxs-lookup"><span data-stu-id="d05eb-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d05eb-104">このトピックでは、Warehouse Management モバイル アプリを設定して、モバイル デバイスでカメラを使用してバーコードをスキャンする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="d05eb-105">段取り</span><span class="sxs-lookup"><span data-stu-id="d05eb-105">Setup</span></span>

<span data-ttu-id="d05eb-106">Warehouse Management モバイル アプリの表示設定では、バーコードのスキャンにカメラを使用すべきかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d05eb-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="d05eb-107">**スキャナーとしてカメラを使用** を有効にした場合、優先入力モードを **スキャン** に設定した各入力フィールドでカメラを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d05eb-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="d05eb-108">入力フィールドをスキャン可能にする必要があるかどうかをコントロールするには、**倉庫保管アプリ フィールド名** ページで、**優先入力モード** を **スキャン** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="d05eb-109">このオプションが選択されている場合、Warehouse Management モバイル アプリでのスキャンにカメラを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d05eb-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="d05eb-110">詳細情報については、[Warehouse Management モバイル アプリのフィールドを構成する](configure-app-field-names-priorities-warehouse.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d05eb-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="d05eb-111">サポートされているバーコード形式</span><span class="sxs-lookup"><span data-stu-id="d05eb-111">Supported bar code formats</span></span>

<span data-ttu-id="d05eb-112">サポートされている最も一般的なバーコード形式には、コード 128、コード 39、コード 93、EAN-8、EAN-13、UPC-E、UPC-A、および QR コードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d05eb-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="d05eb-113">ナビゲーション</span><span class="sxs-lookup"><span data-stu-id="d05eb-113">Navigation</span></span>

<span data-ttu-id="d05eb-114">カメラ ページは、**優先入力モード** を *スキャン* に設定した入力フィールドの各ページで開始されます。カメラ ページに来ると次のオプションを使用して移動します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="d05eb-115">**タスクと詳細** ページに戻るには [戻る] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="d05eb-116">手動で入力するためのページに移動するには **タスクと詳細** ページにある鉛筆を選択します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="d05eb-117">[カメラ] ページに戻るには **タスクと詳細** ページでカメラを選択します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="d05eb-118">[カメラ] ページで、[カメラ] ボタンを選択すると、バー コードを識別しようとしているときにグレー表示になります。</span><span class="sxs-lookup"><span data-stu-id="d05eb-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="d05eb-119">バーコードが 5 秒以内で識別されない場合は、プロセスがタイムアウトになり、[カメラ] ボタンがもう一度利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="d05eb-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="d05eb-120">それからもう一度バーコードをスキャンすることができます。</span><span class="sxs-lookup"><span data-stu-id="d05eb-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="d05eb-121">バーコードにカメラの視点を定めると、最適な結果で、バーコードはかっこ内に合わせられた状態になります。</span><span class="sxs-lookup"><span data-stu-id="d05eb-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="d05eb-122">バーコードが正常にスキャンされると、結果が処理され、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="d05eb-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="d05eb-123">次の手順で優先入力モードが [スキャン] に設定された別の入力フィールドを含む場合、[カメラ] ページが再び開始します。</span><span class="sxs-lookup"><span data-stu-id="d05eb-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="d05eb-124">次の手順が [スキャン] フィールドでない場合、[カメラ] ページは開始しません。</span><span class="sxs-lookup"><span data-stu-id="d05eb-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
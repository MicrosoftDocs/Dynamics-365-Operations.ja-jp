---
title: 集荷のチェックイン モジュール
description: このトピックでは、集荷のチェックイン モジュールを取り上げ、Microsoft Dynamics 365 Commerce で構成する方法について説明します。
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270586"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="e1ab4-103">集荷のチェックイン モジュール</span><span class="sxs-lookup"><span data-stu-id="e1ab4-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1ab4-104">このトピックでは、集荷のチェックイン モジュールを取り上げ、Microsoft Dynamics 365 Commerce で構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e1ab4-105">集荷のチェックイン モジュールは、店舗にその到着を通知する Dynamics 365 Commerce 顧客チェックイン機能を使用する顧客の確認ページを提供します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="e1ab4-106">また、集荷のチェックイン モジュールにより、注文の配送を容易にする追加情報を顧客から収集するフォームを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="e1ab4-107">この情報には、顧客の駐車場の番号、および車両の作成とモデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="e1ab4-108">モジュール プロパティ</span><span class="sxs-lookup"><span data-stu-id="e1ab4-108">Module properties</span></span>

| <span data-ttu-id="e1ab4-109">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="e1ab4-109">Property name</span></span> | <span data-ttu-id="e1ab4-110">値</span><span class="sxs-lookup"><span data-stu-id="e1ab4-110">Values</span></span> | <span data-ttu-id="e1ab4-111">説明</span><span class="sxs-lookup"><span data-stu-id="e1ab4-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e1ab4-112">確認テキスト</span><span class="sxs-lookup"><span data-stu-id="e1ab4-112">Confirmation text</span></span> | <span data-ttu-id="e1ab4-113">テキスト文字列</span><span class="sxs-lookup"><span data-stu-id="e1ab4-113">Text string</span></span> | <span data-ttu-id="e1ab4-114">チェックイン確認ページに表示されるヘッダーのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="e1ab4-115">QR コードの表示</span><span class="sxs-lookup"><span data-stu-id="e1ab4-115">Show QR code</span></span> | <span data-ttu-id="e1ab4-116">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e1ab4-116">**True** or **False**</span></span> | <span data-ttu-id="e1ab4-117">このプロパティが **True** に設定されている場合、チェックイン確認ページには注文確認 ID を表す QR コードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="e1ab4-118">追加情報のヘッダー</span><span class="sxs-lookup"><span data-stu-id="e1ab4-118">Additional information heading</span></span> | <span data-ttu-id="e1ab4-119">テキスト文字列</span><span class="sxs-lookup"><span data-stu-id="e1ab4-119">Text string</span></span> | <span data-ttu-id="e1ab4-120">追加情報フィールドが構成されている場合に表示されるヘッダーのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="e1ab4-121">追加情報キー</span><span class="sxs-lookup"><span data-stu-id="e1ab4-121">Additional information keys</span></span> | <span data-ttu-id="e1ab4-122">リソース ID/リソース値のペア</span><span class="sxs-lookup"><span data-stu-id="e1ab4-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="e1ab4-123">各キーは、フォーム フィールドと、顧客からの追加情報を収集するために使用する関連付けられたラベルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="e1ab4-124">追加情報キー \> リソース ID</span><span class="sxs-lookup"><span data-stu-id="e1ab4-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="e1ab4-125">テキスト文字列</span><span class="sxs-lookup"><span data-stu-id="e1ab4-125">Text string</span></span> | <span data-ttu-id="e1ab4-126">各情報キーは、フォーム フィールドと、顧客からの追加情報を収集するために使用する関連付けられたラベルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="e1ab4-127">このプロパティは、追加情報キーを識別します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-127">This property identifies the additional information key.</span></span> <span data-ttu-id="e1ab4-128">販売時点管理 (POS) で作成されたタスクでは、このプロパティの値は指示フィールドのラベルとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="e1ab4-129">追加情報キー \> リソース値</span><span class="sxs-lookup"><span data-stu-id="e1ab4-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="e1ab4-130">テキスト文字列</span><span class="sxs-lookup"><span data-stu-id="e1ab4-130">Text string</span></span> | <span data-ttu-id="e1ab4-131">POS でのタスクのテキスト フィールドのラベル。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="e1ab4-132">追加情報キー \> 必須</span><span class="sxs-lookup"><span data-stu-id="e1ab4-132">Additional information keys \> Required</span></span> | <span data-ttu-id="e1ab4-133">**True** または **False**</span><span class="sxs-lookup"><span data-stu-id="e1ab4-133">**True** or **False**</span></span> | <span data-ttu-id="e1ab4-134">このプロパティで、続行する前に顧客がフォーム フィールドに入力する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="e1ab4-135">このプロパティが **True** に設定されている場合、フォーム ラベルの横にアスタリスクが表示され、値が入力されていない場合に null チェックを実行して顧客が続行することを防止します。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="e1ab4-136">ページに集荷のチェックイン モジュールを追加する</span><span class="sxs-lookup"><span data-stu-id="e1ab4-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="e1ab4-137">集荷のチェックイン モジュールは、チェックイン確認のために新しく作成するページに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="e1ab4-138">そのページは、メールの **ここにいます** のリンクまたはボタンを選択した顧客のためのチェックイン確認エクスペリエンスとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="e1ab4-139">追加情報フォームを構成する</span><span class="sxs-lookup"><span data-stu-id="e1ab4-139">Configure the additional information form</span></span>

<span data-ttu-id="e1ab4-140">既定では、追加情報キーが構成されていない場合、モジュールには顧客のチェックイン確認ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="e1ab4-141">チェックイン確認が表示されると、注文の集荷を行う店舗の POS でタスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="e1ab4-142">1 つ以上の追加情報キーを構成する場合、顧客は最初に情報の入力を求められます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="e1ab4-143">**送信** を選択すると、チェックイン確認が表示され、POS でタスクが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e1ab4-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e1ab4-144">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e1ab4-144">Additional resources</span></span>

[<span data-ttu-id="e1ab4-145">販売時点管理 (POS) での顧客チェックイン通知を有効にする</span><span class="sxs-lookup"><span data-stu-id="e1ab4-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)

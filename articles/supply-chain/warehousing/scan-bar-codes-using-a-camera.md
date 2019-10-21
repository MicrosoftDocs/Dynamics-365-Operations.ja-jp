---
title: Dynamics 365 Supply Chain Management – Warehousing アプリでのカメラを使用したバーコードのスキャン
description: このトピックでは、モバイル デバイスでカメラを使用してバーコードをスキャンするため Dynamics 365 Supply Chain Management - Warehousing アプリを設定する方法について説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8062a981f792bcfed2713d3cb6a42f414394f6a4
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251466"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a>Dynamics 365 Supply Chain Management – Warehousing アプリでのカメラを使用したバーコードのスキャン

[!include [banner](../includes/banner.md)]

このトピックでは、モバイル デバイスでカメラを使用してバーコードをスキャンするため Dynamics 365 Supply Chain Management - Warehousing アプリを設定する方法について説明します。 

## <a name="prerequisites"></a>必要条件
この機能を使用するには、インストールされている Warehousing アプリのバージョン 1.2.0.0 が必要であり、デバイスにはカメラが必要です。 更新した後にアプリを開く際に、カメラを使用するアプリを許可するように求められます。 デバイスにカメラがない場合、プロンプトは表示されず、カメラをスキャナーとして使用することはできません。 

## <a name="setup"></a>段取り
Warehousing アプリケーションの表示設定では、バーコードのスキャンにカメラを使用すべきかを選択できます。 **スキャナーとしてカメラを使用** を有効にした場合、優先入力モードを **スキャン** に設定した各入力フィールドでカメラを使用できます。 

入力フィールドをスキャン可能にする必要があるかどうかをコントロールするには、**倉庫保管アプリ フィールド名**ページで、**優先入力モード**を**スキャン**に設定します。 このオプションが選択されている場合、倉庫保管アプリでスキャンするのにカメラを使用できます。 Warehousing でアプリ フィールド名を構成する方法については、[倉庫保管アプリでアプリ フィールド名をコンフィギュレーションする](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse) を参照してください。

## <a name="supported-bar-code-formats"></a>サポートされているバーコード形式
サポートされている最も一般的なバーコード形式には、コード 128、コード 39、コード 93、EAN-8、EAN-13、UPC-E、UPC-A、および QR コードが含まれます。 

## <a name="navigation"></a>ナビゲーション
カメラ ページは、優先入力モードをスキャンに設定した入力フィールドの各ページで開始されます。カメラ ページに来ると次のオプションを使用して移動します。
- [タスクと詳細] ページに戻るには [戻る] ボタンをクリックします。 
- 手動で入力するためのページに移動するには [タスクと詳細] ページにある鉛筆をクリックします。
- [カメラ] ページに戻るには [タスクと詳細] ページでカメラをクリックします。 

| [タスクと詳細] ページ | [カメラ] ページ | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

[カメラ] ページで、[カメラ] ボタンをクリックすると、バー コードを識別しようとしているときにグレー表示になります。 バーコードが 5 秒以内で識別されない場合は、プロセスがタイムアウトになり、[カメラ] ボタンがもう一度利用可能になります。 それからもう一度バーコードをスキャンすることができます。

バーコードにカメラの視点を定めると、最適な結果で、バーコードはかっこ内に合わせられた状態になります。 バーコードが正常にスキャンされると、結果が処理され、次の手順に進みます。 次の手順で優先入力モードが [スキャン] に設定された別の入力フィールドを含む場合、[カメラ] ページが再び開始します。 次の手順が [スキャン] フィールドでない場合、[カメラ] ページは開始しません。


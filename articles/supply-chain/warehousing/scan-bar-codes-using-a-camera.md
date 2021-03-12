---
title: 倉庫アプリでのカメラを使用したバーコードのスキャン
description: このトピックでは、倉庫アプリを設定して、モバイル デバイスでカメラを使用してバーコードをスキャンする方法について説明します。
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
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 71ec15b2568eefd8bea99e64c258a65461a7ad95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965643"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>倉庫アプリでのカメラを使用したバーコードのスキャン

[!include [banner](../includes/banner.md)]

このトピックでは、倉庫アプリを設定して、モバイル デバイスでカメラを使用してバーコードをスキャンする方法について説明します。 

## <a name="prerequisites"></a>必要条件
この機能を使用するには、インストールされている倉庫アプリのバージョン 1.2.0.0 が必要であり、デバイスにはカメラが必要です。 更新した後にアプリを開く際に、カメラを使用するアプリを許可するように求められます。 デバイスにカメラがない場合、プロンプトは表示されず、カメラをスキャナーとして使用することはできません。 

## <a name="setup"></a>セットアップ
倉庫アプリケーションの表示設定では、バーコードのスキャンにカメラを使用すべきかを選択できます。 **スキャナーとしてカメラを使用** を有効にした場合、優先入力モードを **スキャン** に設定した各入力フィールドでカメラを使用できます。 

入力フィールドをスキャン可能にする必要があるかどうかをコントロールするには、**倉庫保管アプリ フィールド名** ページで、**優先入力モード** を **スキャン** に設定します。 このオプションが選択されている場合、倉庫アプリでのスキャンにカメラを使用できます。 倉庫管理でアプリ フィールド名を構成する方法については、[倉庫アプリでアプリ フィールド名を構成する](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse) を参照してください。

## <a name="supported-bar-code-formats"></a>サポートされているバーコード形式
サポートされている最も一般的なバーコード形式には、コード 128、コード 39、コード 93、EAN-8、EAN-13、UPC-E、UPC-A、および QR コードが含まれます。 

## <a name="navigation"></a>ナビゲーション
カメラ ページは、優先入力モードをスキャンに設定した入力フィールドの各ページで開始されます。カメラ ページに来ると次のオプションを使用して移動します。
- [タスクと詳細] ページに戻るには [戻る] ボタンをクリックします。 
- 手動で入力するためのページに移動するには [タスクと詳細] ページにある鉛筆をクリックします。
- [カメラ] ページに戻るには [タスクと詳細] ページでカメラをクリックします。 

| [タスクと詳細] ページ | [カメラ] ページ | 
| :---------------------: | :--------------------: |
| ![カメラ スキャンのタスク例の詳細ページ](./media/camera-scanning-example-task-detail-page50.png)          | ![カメラ スキャン例のカメラ ページをもっと小さくする](./media/camera-scanning-example-camera-page50.png)          |

[カメラ] ページで、[カメラ] ボタンをクリックすると、バー コードを識別しようとしているときにグレー表示になります。 バーコードが 5 秒以内で識別されない場合は、プロセスがタイムアウトになり、[カメラ] ボタンがもう一度利用可能になります。 それからもう一度バーコードをスキャンすることができます。

バーコードにカメラの視点を定めると、最適な結果で、バーコードはかっこ内に合わせられた状態になります。 バーコードが正常にスキャンされると、結果が処理され、次の手順に進みます。 次の手順で優先入力モードが [スキャン] に設定された別の入力フィールドを含む場合、[カメラ] ページが再び開始します。 次の手順が [スキャン] フィールドでない場合、[カメラ] ページは開始しません。


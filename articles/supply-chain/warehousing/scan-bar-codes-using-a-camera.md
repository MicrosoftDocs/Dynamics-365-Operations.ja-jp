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
ms.openlocfilehash: 62280b8401c1f7d5dc859a2130981405e69d03cfb5383123d7069e71e6cb1f47
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711666"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Warehouse Management モバイル アプリでカメラを使用してバーコードをスキャンする

[!include [banner](../includes/banner.md)]

このトピックでは、Warehouse Management モバイル アプリを設定して、モバイル デバイスでカメラを使用してバーコードをスキャンする方法について説明します。

## <a name="setup"></a>段取り

Warehouse Management モバイル アプリの表示設定では、バーコードのスキャンにカメラを使用すべきかを選択できます。 **スキャナーとしてカメラを使用** を有効にした場合、優先入力モードを **スキャン** に設定した各入力フィールドでカメラを使用できます。

入力フィールドをスキャン可能にする必要があるかどうかをコントロールするには、**倉庫保管アプリ フィールド名** ページで、**優先入力モード** を **スキャン** に設定します。 このオプションが選択されている場合、Warehouse Management モバイル アプリでのスキャンにカメラを使用できます。 詳細情報については、[Warehouse Management モバイル アプリのフィールドを構成する](configure-app-field-names-priorities-warehouse.md) を参照してください。

## <a name="supported-bar-code-formats"></a>サポートされているバーコード形式

サポートされている最も一般的なバーコード形式には、コード 128、コード 39、コード 93、EAN-8、EAN-13、UPC-E、UPC-A、および QR コードが含まれます。

## <a name="navigation"></a>ナビゲーション

カメラ ページは、**優先入力モード** を *スキャン* に設定した入力フィールドの各ページで開始されます。カメラ ページに来ると次のオプションを使用して移動します。

- **タスクと詳細** ページに戻るには [戻る] ボタンを選択します。
- 手動で入力するためのページに移動するには **タスクと詳細** ページにある鉛筆を選択します。
- [カメラ] ページに戻るには **タスクと詳細** ページでカメラを選択します。

[カメラ] ページで、[カメラ] ボタンを選択すると、バー コードを識別しようとしているときにグレー表示になります。 バーコードが 5 秒以内で識別されない場合は、プロセスがタイムアウトになり、[カメラ] ボタンがもう一度利用可能になります。 それからもう一度バーコードをスキャンすることができます。

バーコードにカメラの視点を定めると、最適な結果で、バーコードはかっこ内に合わせられた状態になります。 バーコードが正常にスキャンされると、結果が処理され、次の手順に進みます。 次の手順で優先入力モードが [スキャン] に設定された別の入力フィールドを含む場合、[カメラ] ページが再び開始します。 次の手順が [スキャン] フィールドでない場合、[カメラ] ページは開始しません。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
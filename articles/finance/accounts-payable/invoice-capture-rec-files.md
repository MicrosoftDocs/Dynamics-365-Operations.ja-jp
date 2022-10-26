---
title: Invoice Capture の受信ファイル
description: この記事では、Invoice capture で、さまざまなソースから請求書ファイルを収集する方法について説明します。
author: sunfzam
ms.date: 10/13/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c55540d11a67d4d4c4c8477d51cb6f1f5777767
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690132"
---
# <a name="invoice-capture-received-files"></a>Invoice Capture の受信ファイル

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Invoice Capture では、**受信したファイル** ページは、さまざまなソースから請求書ファイルを受信する中心的な場所です。

## <a name="upload-invoice-files"></a>請求書ファイルのアップロード

買掛金勘定 (AP) の担当者は、**ファイルのアップロード** を選択して **アップロード** のダイアログ ボックスを開きます。 AP 担当がファイルを選択すると、**アップロード** ボタンを使用できるようになります。

## <a name="include-or-obsolete-invoice-files"></a>請求書ファイルを含める、または廃棄する

エラーや警告が発生した請求書を選択し、アクション ペインで対応するボタンを選択することで、請求書の取り込みや廃止をすることができます。 古いファイルとしてマークされた請求書は、**受領済 (古いファイル)** ビューに表示されません。

## <a name="view-captured-invoices"></a>取り込まれた請求書の表示

受信したファイルが正常に認識されると、取り込まれた請求書の情報が AI モデルから返され、Microsoft Dataverse に入力されます。 AP 担当は、**取り込み済み請求書の表示** を選択して、請求書の詳細を確認することができます。 必要に応じて、元の請求書ファイルをダウンロードできます。

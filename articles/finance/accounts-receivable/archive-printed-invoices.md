---
title: 印刷された顧客請求書にハッシュ番号を付けてアーカイブする
description: このトピックでは、ハッシュ番号付きの印刷された顧客請求書を保存するアーカイブを有効にする方法について説明します。
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018981"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>印刷された顧客請求書にハッシュ番号を付けてアーカイブする

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

一部の国では、一部のドキュメントの印刷と共に計算されたハッシュ番号をシステムに保存する法的要件があります。 ハッシュ番号は、関係機関への報告や監査時に使用できます。

このトピックでは、ハッシュ番号付きの印刷された顧客請求書を保存するアーカイブを設定する方法について説明します。

## <a name="prerequisites"></a>必要条件

- **機能管理** ワークスペースで、機能を有効にし、**印刷された顧客請求書をハッシュ番号でアーカイブします**。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。
- **印刷管理** で必要なドキュメントの印刷可能な形式を説明します。

この機能は次のドキュメントに適用できます。

**売掛金勘定**
- 顧客請求書
- 顧客訂正票
- 自由書式の請求書
- 自由書式の訂正票

**プロジェクト管理および会計**
- プロジェクト請求書
- プロジェクト訂正票

## <a name="configure-customer-master-data"></a>顧客マスター データの構成
顧客データを構成し、印刷した請求書を添付ファイルとして自動的に保存する機能を有効にする場合は、次の手順を実行します。

1. **売掛金勘定** > **すべての顧客** に移動します。 
2. 顧客を選択し、**eInvoice の添付ファイル** フィールドの **E-INVOCE** セクションで、**請求書と出荷** FastTab から、**はい** を選びます。

## <a name="print-invoices"></a>請求書の印刷
前の手順で設定した顧客の自由形式、顧客、およびプロジェクト請求書または貸方伝票を転記および印刷できます。

印刷された請求書の **添付ファイル** ページを開きます。 **ドキュメント ハッシュ番号** フィールドの **追加の詳細** フィールド グループから、**添付ファイル** FastTab で、印刷済み請求書の計算された保存済ハッシュ番号を探します。

![添付ファイル のハッシュ番号](media/attach-hash-num.jpg)


---
title: 税サービスにアクセスできませんでした
description: この記事では、税計算サービスにアクセスする際のエラーをトラブルシューティングする方法について説明します。
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 65d819b97be3d1238bc0ecfc201b4e24edac8616
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861225"
---
# <a name="failed-to-access-tax-service"></a>税サービスにアクセスできませんでした

[!include [banner](../includes/banner.md)]


この記事では、税計算サービスの "税務サービスにアクセスに失敗しました" エラーを修正する方法について説明します。

## <a name="symptoms"></a>現象

Microsoft Dynamics 365 Finance で、**税** \> **設定** \> **税コンフィギュレーション** \> **税サービスのパラメーター** の順に移動します。 **全般** タブ で、**税計算を有効にする** オプションを有効にします。 **機能の設定名** フィールドで値を選択しようとする場合は、エラーが発生します。 エラー メッセージには "税務サービスにアクセスに失敗しました" と書かれています。

## <a name="cause"></a>原因

このエラーが発生するのは、財務が税計算サービスにアクセスできないためです。

## <a name="resolution"></a>解決策 

1. Microsoft Dynamics Lifecycle Services (LCS) にログインします。
2. **環境** ページの **環境アドイン** タブで、**税計算** 項目を見つけて、そのステータスを確認します。 ステータスが **インストール中** または **インストール済** である必要 があります。 税計算サービス アドインがインストールされていない場合は、エラーが表示されます。

## <a name="mitigation"></a>軽減策

1. LCS の **財務** ページの **Power Platform 統合** セクションで、**新しいアドインのインストール** を選択します。
2. ページの下にスクロールし、**税計算** アドインを選択してインストールします。
3. 財務環境に戻って、税計算サービスにアクセスしてみてください。

> [!NOTE]
> 税計算サービスをインストールする前に、[税計算サービスの前提条件](global-get-started-with-tax-calculation-service.md#prerequisites)を確認してください。
> 
> **Power Platform 統合** セクションを利用できないのでアドインをインストールできない場合は、[アドインの概要](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md)を参照してください。 アドインのインストール後もエラーが発生する場合は、システム管理者に問い合わせてください。

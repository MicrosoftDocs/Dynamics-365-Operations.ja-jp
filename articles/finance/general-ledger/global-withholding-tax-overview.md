---
title: グローバル源泉徴収税
description: このトピックでは、グローバルな源泉徴収税機能とこの設定方法に関する情報を提供します。 グローバル源泉徴収税の機能は、仕入先トランザクションと顧客トランザクションに対して機能強化されており、源泉徴収税が品目レベルで計算されます。
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075741"
---
# <a name="global-withholding-tax"></a>グローバル源泉徴収税

[!include [banner](../includes/banner.md)]

このトピックでは、グローバルな源泉徴収税機能とこの設定方法について解説します。 この機能は、 バージョン 10.0.17 またはそれ以降で使用できます。

グローバル源泉徴収税の機能は、仕入先トランザクションと顧客トランザクションに対して機能強化されており、源泉徴収税が品目レベルで計算されます。 購入取引による源泉徴収票の残高は、源泉徴収票の決済口座に対して源泉徴収票決済のジョブを実行することで決済できます。

> [!NOTE]
> グローバル源泉徴収税では、発注書、仕入先請求書、および販売注文ページの **請求金額の管理** 機能はサポートされていません。

## <a name="turn-on-global-withholding-tax"></a>グローバル源泉徴収税の有効化

1. **機能の管理** ワークスペースで、一覧から **フローバル源泉徴収税** 機能を選択し、**すぐに有効化する** を選択します。
2. **税 \> 設定 \> パラメータ \> 総勘定元帳のパラメータ** に移動し、**源泉徴収税** タブで、**グローバル源泉徴収税を有効にする** オプションを **はい** に設定します。
3. **保存** を選択します。
4. Web ブラウザーのページを更新します。

> [!NOTE]
> ローカライズされた源泉徴収税ソリューションが既に存在する国/地域では、グローバル源泉徴収税の機能を有効にできません。 この領域には、インド、ブラジル、タイ、サウジアラビア、アイルランド、英国、米国が含まれますが、これに限定されないものとします。

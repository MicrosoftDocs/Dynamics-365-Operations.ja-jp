---
title: 倉庫作業のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫作業の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 08cc074fe851b952ebfc942ae3d1cb05240d3b91
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837444"
---
# <a name="troubleshoot-warehouse-work"></a>倉庫作業のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫作業の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>空の払出と空白の入庫が追跡分析コード グループで許可されている場合に、シリアル番号品目を含むライセンス プレートを移動できません。

### <a name="issue-description"></a>問題の説明

追跡用分析コード グループでシリアル番号が *払出時空白可* および *受入時空白可* に設定されている場合、および同じ場所に複数のライセンス プレートがあり、シリアル番号があるものとないものがある場合、**移動** メニュー項目を使用してライセンス プレートを移動することはできません。

### <a name="issue-resolution"></a>問題の解決

この問題は、[KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) で展開された変更によって修正されます。 この変更により、空白の受入と払出が許可されている場合に、**シリアル番号** フィールドがオプションとして設定されます。

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>移動処理を行うとき、倉庫管理モバイル アプリで次のエラー メッセージを受信します: "このプロセスでは、在庫所有者 %1 が許可されていません。"

### <a name="issue-description"></a>問題の説明

倉庫管理モバイル アプリを使用して移動を行うときに、**所有者** 追跡用分析コードが見つかりません。 Supply Chain Management クライアントからの通常の在庫移動仕訳帳が意図したとおりに機能し、**所有者** 分析コードが入力されている場合にのみ転記できます。

### <a name="issue-resolution"></a>問題の解決

Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 現在、倉庫管理プロセスでは、法人によって所有されている在庫のみがサポートされています。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
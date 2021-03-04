---
title: 倉庫管理での引当のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645123"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>倉庫管理での引当のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>"予約に依存する作業が作成されているため、"引当を削除できません" というエラー メッセージを受信します。

### <a name="issue-description"></a>問題の説明

販売明細行に対して未処理の作業があるため、その販売明細行の在庫引当を解除できません。

### <a name="issue-resolution"></a>問題の解決

未処理の梱包グループ作業があるかどうかを調べて、品目を梱包ステーションから別の場所 (*Baydoor* など) に移動します。 **作業の作成履歴ログ** ページと **作業の詳細** ページのレコードを確認して、在庫が物理的に引当されているかどうかを確認し、その作業を完了または削除して引当を解放します。

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>エラー メッセージ "品目 %2 の在庫トランザクションが不足しているため、在庫数量 - %1 を更新できませんでした...." が表示されます。

### <a name="issue-description"></a>問題の説明

この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。 次に、完全なエラー メッセージの全文を示します。

> 品目 %2 (分析コード サイズ=%3、色=%4、追加=%5、サイト=%6、倉庫=%7、場所=%8、在庫ステータス=あり、ライセンス プレート=%9、ロット ID %12 での参照 ID %11 のバッチ番号=%10) の在庫トランザクションが不足しているため、在庫数量 -%1 を更新できませんでした。

### <a name="issue-resolution"></a>問題の解決

在庫トランザクションで、数量が物理的に引当されていないことを確認してください。 たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>エラー メッセージ "在庫で使用できるのは 0.00 のみであるため、現物手持在庫...を引当することはできません" が表示されます。

### <a name="issue-description"></a>問題の説明

この問題は、指定された分析コードを含む十分な在庫トランザクションがないために、システムで在庫数量を更新できない場合に発生する可能性があります。 次に、完全なエラー メッセージの全文を示します。

> 在庫で使用できるのは 0.00 のみであるため、現物手持在庫 (サイト=%1、倉庫=%2、在庫ステータス=あり、バッチ番号=%3、所有者=%4: %5) を引当することはできません。

### <a name="issue-resolution"></a>問題の解決

この問題は、未処理の作業が原因で発生している可能性があります。 作業を完了するか、作業の作成を行わずに入庫します。 在庫トランザクションで、数量が物理的に引当されていないことを確認してください。 たとえば、品質指示、在庫ブロック レコード、または出荷注文が、これらのトランザクションによって開かれている場合があります。

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>エラー メッセージ "ウェーブに割り当てるには、積荷明細行は、その場所より上の分析コードを指定する必要があります。 これらの分析コードを割り当てるには、積荷明細行を準備して再作成します" が表示されます。

### <a name="issue-description"></a>問題の説明

"上のバッチ" 引当階層を持つ品目 (**場所** 分析コードの *上* に **バッチ番号** 分析コードが配置されている) を使用すると、部分数量に対する **積荷計画ワークベンチ** ページの **倉庫にリリース** コマンドが機能しません。 このエラー メッセージが表示され、部分数量に対して作業が作成されません。

ただし、"下のバッチ" 引当階層を持つ品目 (**場所** 分析コードの *下* に **バッチ番号** 分析コードが配置されている) を使用した場合、部分数量に対する **積荷計画ワークベンチ** ページから積荷をリリースできます。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。 引当階層で **場所** 分析コードの上に分析コードを配置する場合は、倉庫へのリリース前に指定する必要があります。 Microsoft は、この問題を評価し、積荷計画ワークベンチから倉庫に対するリリースにおける制限事項であると判断しました。 **場所** の上に 1 つ以上の分析コードが指定されていない場合、部分的な数量をリリースすることはできません。

詳細については、[柔軟な倉庫レベル分析コードの引当ポリシー](flexible-warehouse-level-dimension-reservation.md)を参照してください。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
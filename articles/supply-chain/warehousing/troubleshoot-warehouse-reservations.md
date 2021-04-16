---
title: 倉庫管理での引当のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。
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
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828109"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>倉庫管理での引当のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での倉庫引当の処理中に発生する可能性がある問題を修正する方法について説明します。

バッチ番号とシリアル番号の登録に関連するトピックについては、[倉庫バッチおよびシリアル予約階層に関するトラブルシューティング](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) を参照してください。

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

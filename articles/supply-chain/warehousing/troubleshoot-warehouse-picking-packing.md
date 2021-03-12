---
title: ピッキングと梱包のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management でピッキングおよび梱包する際に発生する可能性がある一般的な問題の修正方法について説明します。
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2cce1038ed393fc8a7bb489a37fc0921b0ac755e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993936"
---
# <a name="troubleshoot-picking-and-packing"></a>ピッキングと梱包のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management でピッキングおよび梱包する際に発生する可能性がある一般的な問題の修正方法について説明します。

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a>エラー メッセージ "分析コード シリアル番号が設定されている場合、分析コードの場所を空白にすることはできません" が表示されます。

### <a name="issue-description"></a>問題の説明

このエラー メッセージは、高度な倉庫管理 (WMS) が有効になっている倉庫を使用してシリアル品目の移動オーダーを作成し、作業が完了した後、出荷を確認しようとした場合に表示されます。

### <a name="issue-resolution"></a>問題の解決

"移動元" 倉庫の流通倉庫の **既定の受入場所** フィールドが空白になっています。 この問題を解決するには、流通倉庫の既定の受入場所を指定します。 この場所がライセンス プレートによって制御されていることを確認してください。

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a>"ライセンス プレートが無効です" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

ライセンス プレート ID をスキャンすると、倉庫アプリでこのエラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

ライセンス プレート ID がライセンス プレート テーブルに存在し、ライセンス プレートの品目と数量が使用可能である (つまりブロックされていない) ことを確認してください。

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a>エラー メッセージ "フィールド \[積載重量\] (=-%1) には正の数のみを含めることができます。 更新はキャンセルされました" が表示されます。

### <a name="issue-description"></a>問題の説明

梱包場所からステージング場所への作業またはステージング場所からドッキング場所への作業を処理するときに未処理の作業がある場合に、このエラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

この問題を解決するには、**システム管理 \> 定期タスク \>データベース \> 整合性チェック** を実行し、**倉庫積荷重量の整合性チェック** のプロセスを実行します。

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>"単位 %1 の数量が有効ではありません" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

複数のバッチ間で *分割ピッキング* を実行しようとすると、このエラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

倉庫の作業者は、倉庫アプリで *ショート ピッキング* プロセスを使用する必要があります。 同じ場所から複数のバッチを選択する場合は、ウェアハウス アプリの **完全** オプションを使用することもできます。

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a>ライセンス プレートとして管理されている場所に在庫を移動できません。

### <a name="issue-description"></a>問題の説明

積荷のピッキング済数量を減少させることはできません。

### <a name="issue-resolution"></a>問題の解決

以前のバージョンでは、積荷のピッキング済数量を減少させることはできません。 ただし、現在では、ライセンス プレートによって制御された場所にピッキング解除できるようになりました。 **ピッキング済数量の削減** ページでは、**場所** 値と **ライセンス プレート** 値の両方を積荷明細行に指定する必要があります。

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a>納品書を印刷することはできますか。または倉庫でコンテンツを梱包できますか。

### <a name="issue-description"></a>問題の説明

**作業監査テンプレート行の更新** ページで、倉庫またはサイト別に納品書または梱包コンテンツを印刷しようとしています。

### <a name="issue-resolution"></a>問題の解決

印刷管理設定を使用してドキュメントを印刷する場合は、**作業監査テンプレート行の更新** ページの **印刷設定の編集** を選択するのではなく、印刷管理を使用してスコープ (サイト/倉庫) を制限します。

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>販売注文から転記された後に梱包明細をキャンセルできません。

### <a name="issue-description"></a>問題の説明

WMS に対してピッキングおよび出荷プロセスが有効になっている場合は、販売注文から転記された後に梱包明細をキャンセルすることはできません。

### <a name="issue-resolution"></a>問題の解決

WMS が有効になっている品目に対して転記された梱包明細を修正するには、注文からではなく、積荷から転記を行う必要があります。 Microsoft は、この問題を評価し、それが機能上の制限であることを確認しました。 一般に、倉庫管理プロセスを通じてピッキングおよび出荷された販売注文は、梱包明細として、積荷または出荷と販売注文ドキュメント自体から更新することができます。 ただし、梱包明細の販売注文を販売注文ドキュメントから更新した場合は、梱包明細の取消を、積荷または販売注文から行うことはできません。 したがって、積荷から梱包明細の転記を使用することをお勧めします。 この場合、積荷から実行する必要がある取消が有効になります。

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a>エラー メッセージ "クラスターのための十分な作業が見つかりません" が表示されます。

### <a name="issue-description"></a>問題の説明

*システム主導のクラスター ピッキング* プロセスを使用するとき、(たとえば 10 個の職位をピッキング可能な) クラスター プロファイルを構成している場合は、10 個の職位にピッキングするために十分な作業があればそのプロセスは計画どおりに機能します。 ただし、ピッキングする職位が 8 しかない場合、1 つのクラスターに十分な作業がないので、このエラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

この問題を修正するには、クラスター プロファイルを編集し、**職位のアクティブ化** オプションを *いいえ* に設定します。

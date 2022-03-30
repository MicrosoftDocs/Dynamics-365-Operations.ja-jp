---
title: テスト中の要求データとセッション データの予期しない違い
description: 倉庫アプリケーションのタスク検証結果における要求データとセッション データの間に予期しない違いが発生します。
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456940"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>テスト中の要求データとセッション データの予期しない違い

エラー コード: WarehouseErrorIceRequestInquestValidationError

## <a name="symptoms"></a>現象

[倉庫アプリケーションのタスク検証フレームワーク](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat) を使用している場合、検証者は次のエラー メッセージを返します。

> テスト中の要求データとセッション データの間で予期しない違いがあります。 倉庫モバイル デバイス XML プロトコルに違反しました。REQUEST_XML_TAMPERING

## <a name="cause"></a>原因

このエラーは、テストの実行で正常に実行された最後のステップの出力が、次のステップに記録された入力と一致しない場合に発生します。 この状況は、タスクの検証者が、前のステップの出力を後続のステップの入力として使用しないので、生じる可能性があります。 代わりに、各ステップの入力として記録された XML を使用します。

ほとんどの場合、タスクを再実行するとエラーが発生しますが、テストでは同じタスクの前の実行で変更または削除されたレコードが一部必要です。

## <a name="resolution"></a>解決策

倉庫アプリのタスク検証テストは、例ではなくべき等な操作を実行しますが、基になるデータを変更します。 したがって、タスクを再実行する前に、関連データのリセットが必要になる場合があります。

1. 最後に成功したテスト ステップの出力 XML を確認して、テストの実行が終了した場所を確認します。
1. テストを検査し、必要なすべての販売注文、移動オーダー、作業ヘッダー、その他のレコードが存在し、予期される状態にある状態を確認します。
1. 欠落しているレコードまたは変更されたレコードを作成または編集します。 または、新しいテスト設定を作成し、有効な既存のレコードを使用するテストをデザインします。

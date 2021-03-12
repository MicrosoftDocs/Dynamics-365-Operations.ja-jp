---
title: 積荷構築と出荷のトラブルシューティング
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management での積荷構築と出荷の処理中に発生する可能性がある問題を修正する方法について説明します。
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
ms.openlocfilehash: f49a91afe9281f912d6d3579ac8e52cb1d8e5b5d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994033"
---
# <a name="troubleshoot-load-building-and-shipments"></a>積荷構築と出荷のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Supply Chain Management での積荷構築と出荷の処理中に発生する可能性がある問題を修正する方法について説明します。

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>"無効な在庫分析コードがあるため、この注文明細行には積荷明細行を作成できません" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

返品販売注文を倉庫にリリースするときに、次のエラー メッセージが表示されます。

> 無効な在庫分析コードがあるため、この注文明細行には積荷明細行を作成できません。 引当階層の場所分析コードの下に配置されている在庫分析コードを参照することはできません。 無効な分析コードを注文明細行から削除します。

### <a name="issue-resolution"></a>問題の解決

残念ながら、この製品は、販売返品プロセスの積荷プロセスをサポートしていません。 したがって、返品販売注文を倉庫にリリースすることはできません。

販売注文トランザクションで、引当階層の **場所** 分析コードの下に配置されている在庫分析コードを参照することはできません。 無効な分析コードを注文明細行から削除すると解決できます。

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>エラー メッセージ "いずれかの明細行が既に積荷にあります。 倉庫にリリースできません" が表示されます。

### <a name="issue-description"></a>問題の説明

手動で積荷を作成する場合、または販売注文明細行のエントリが発生する前に積荷を作成するようにプロセスを設定した場合は、後続のリリースが手動で行われること、および積荷からの工順と評価が使用されることを前提としています。

倉庫に対して自動リリースを実行しようとしたが、ウェーブ プロセスで作業を作成できなかった、というシナリオも考えられます。 したがって、この場合も未処理の出荷または積荷が作成されます。 その場合、未処理の出荷または積荷を削除するか、ウェーブを手動で再処理するまで、この未処理の出荷または積荷により、自動的に注文をリリースする試みがブロックされます。

### <a name="issue-resolution"></a>問題の解決

倉庫へのリリース前に負荷が存在しない場合にのみ、販売注文ページからリリースするか、販売注文のリリース ページから自動リリースを行うことができます。 ウェーブが処理されると、自動的に積荷が作成されます。

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>エラー メッセージ "納品書の修正を処理できません。 納品書の修正でサポートされていないために倉庫管理プロセスの対象となる品目のみが納品書に含まれています" が表示されます。

### <a name="issue-description"></a>問題の説明

**キャンセル** ボタンが使用できないため、納品書を転記した後にキャンセルすることはできません。 また、納品書を修正することもできません。 実行しようとすると、このエラー メッセージが表示されます。

### <a name="issue-resolution"></a>問題の解決

高度な倉庫管理 (WMS) が有効になっている品目に対して転記された梱包明細を修正するには、注文から直接ではなく、積荷から転記する必要があります。

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>ウェーブではなく出庫積荷から作業を作成する方法はありますか。

### <a name="issue-description"></a>問題の説明

この問題を再現する 1 つの方法を次に示します。

1. 販売注文または移動オーダーを使用して、出庫積荷を手動で作成します。
2. 積荷を倉庫にリリースします。
3. ピッキング作業がまだ生成されていないことに注意してください。

### <a name="issue-resolution"></a>問題の解決

積荷がリリースされたときに作業をすぐに生成する必要がある場合は、それに応じてウェーブ テンプレートを構成する必要があります。 ウェーブ テンプレートでは、次のオプションを *はい* に設定します。

- ウェーブの作成を自動化
- 倉庫へのリリース時にウェーブを処理する
- ウェーブを自動的にリリースする

## <a name="i-cant-re-release-a-partially-shipped-load"></a>部分的に出荷された積荷を再リリースすることはできません。

### <a name="issue-description"></a>問題の説明

部分的に出荷された積荷を倉庫にリリースすることはできません。 倉庫にリリースすると、"操作完了" のメッセージが表示されますが、何も発生せず、残りの数量に対して作業が作成されません。 この問題は、輸送積荷機能を使用しているときに不完全な引当がある場合に発生します。

### <a name="issue-resolution"></a>問題の解決

[KB の問題 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("部分的に出荷された積荷が再ウェーブおよび再処理される") は[リリース 10.0.15](../get-started/whats-new-scm-10-0-15.md) で修正されています。

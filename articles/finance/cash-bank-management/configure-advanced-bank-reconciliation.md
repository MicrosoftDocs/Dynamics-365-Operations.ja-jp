---
title: 詳細な口座調整の設定プロセス
description: 詳細な口座調整機能では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 Finance での銀行トランザクションに合わせて自動的に調整することができます。 この資料では、調整のプロセスの設定について説明します。
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1757f7901a12a5b0fc3de730953c5b79cbefb
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715446"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>詳細な口座調整の設定プロセス

[!include [banner](../includes/banner.md)]

詳細な口座調整機能では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 Finance での銀行トランザクションに合わせて自動的に調整することができます。 この資料では、調整のプロセスの設定について説明します。  

詳細な口座調整機能を使用する前に設定する必要のあるいくつかの要素があります。 口座取引明細書のインポート設定の情報については、[詳細な口座調整のインポート処理の設定](set-up-advanced-bank-reconciliation-import-process.md)を参照してください。  調整プロセスの設定の要件は、次のとおりです。

## <a name="transaction-codes"></a>トランザクション コード
トランザクション コードは、銀行調整の照合ルールの一部として使用できます。 トランザクション コードは Finance と口座取引明細書間の同じタイプのトランザクションのみの照合に役立ちます。 このタイプの照合を行うには、まず Finance の銀行トランザクションに使用するトランザクション タイプを定義し、銀行で使用する明細書の取引コードにそれらのタイプをマップします。 銀行トランザクションのトランザクション タイプは、**銀行トランザクション タイプ** ページで定義されます。 またこれによって、トランザクション タイプに関連付けられた転記に使用する主勘定を定義します。 

銀行トランザクション コードを定義した後、これらを電子口座取引明細書で使用するトランザクション コードにマップします。 このマッピング プロセスは、**取引コード マッピング** ページを使用を使用して実行されます。 トランザクション コードのマッピングは、銀行ごと個別に完了します。

## <a name="matching-rules-and-matching-rule-sets"></a>照合ルールおよび照合ルール セット
照合ルールによって、Finance 銀行トランザクションと口座取引明細書トランザクションとの間の自動調整の基準を定義できます。 照合ルールの設定は、**調整照合ルール** ページで行います。 詳細については、「[口座調整照合ルールの設定](set-up-bank-reconciliation-matching-rules.md)」を参照してください。 

照合ルール セットを使用して、口座調整プロセス中に順番に実行する照合ルールのグループを定義します。  照合ルール セットは、**調整照合ルール セット** ページで構成されています。

## <a name="cash-and-bank-management-parameters"></a>現金および銀行管理パラメーター
**現金および銀行管理パラメーター** ページに詳細な口座調整プロセスに固有のいくつものパラメーターがあります。  **借方/貸方欄の明細行の金額の表示** は、**口座取引明細書** ページの金額の表示を変更します。 このオプションを選択した場合、口座取引明細書トランザクションの金額が、借方列と貸方列に別々に表示されます。 このオプションを選択しなかった場合、口座取引明細書トランザクションの金額が、単一の金額列に適切な記号で表示されます。 

[パラメーター] ページで設定された検証オプションは、照合ルールで設定された選択を上書きします。 たとえば、[パラメーター] ページで設定された日付の違いを超える明細書を手動あるいは自動で照合することはできません。 また、**トランザクション タイプ マッピングの検証** へのオプションを選択した場合、トランザクション タイプは、トランザクションが手動あるいは自動で照合されるために Finance 銀行トランザクションと口座取引明細書トランザクション間でマップされる必要があります。 

**現金および銀行管理パラメーター** ページで必要な番号順序を構成する必要もあります。  **番号順序** タブで、**ID、明細書 ID、調整 ID、および口座調整** 参照をダウンロードするための番号順序コードを設定します。

## <a name="bank-account-reconciliation-options"></a>銀行口座調整のオプション
まず、銀行口座の詳細な口座調整を有効にする必要があります。 詳細な口座調整機能が有効になった後、いくつかの追加オプションが、**銀行口座** ページで使用可能です。 

**電子支払の確認としての口座取引明細の使用** 機能は、口座調整機能を電子支払ステータスと機能的に統合します。 これが有効になると、電子支払ステータスが **送信** に設定されているため、銀行ドキュメントが自動的に作成されます。 さらに、支払が照合、調整、転記された後、電子支払ステータスは、**送信** から **受信** に更新されます。 

**ステートメントでの銀行口座名** フィールドは、電子口座取引明細書の銀行口座に使用する名前です。 この名前は、複数の銀行口座の情報を含む可能性のあるステートメントから銀行口座にどのトランザクションをインポートするかを決定する際に使用されます。 

**インポート後の調整** へのオプションは、自動的に口座取引明細書の検証、新しい銀行調整とワークシートの作成および既定の照合ルール セットの実行を行います。 この機能は、手動で照合する必要があるトランザクションの時点までのプロセスを自動化します。 銀行口座の設定は、インポートする時点では既定値です。





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

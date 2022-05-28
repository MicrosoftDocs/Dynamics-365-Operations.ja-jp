---
title: 訂正票での元の請求書への参照 (仕入先請求書)
description: このトピックでは、訂正票を作成する際に元の請求書への参照を作成する方法について説明します。
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 698a23a98f027014c89073203e6d9dfa5539a2f6
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689188"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>訂正票での元の請求書への参照 (仕入先請求書)

[!include [banner](../includes/banner.md)]

このトピックでは、訂正票を作成する際に元の請求書への参照を作成する方法について説明します。

## <a name="prerequisites"></a>必要条件

**機能管理** ワークスペースで、**仕入先請求書の請求の貸方転記を有効にする** 機能を有効にします。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

このトピックで説明する機能は、以下のドキュメントに適用されます。

**買掛金勘定:**

- 発注書
- 請求仕訳帳
- 仕入帳

**総勘定元帳:**

- 一般仕訳帳

## <a name="define-a-reference-to-an-original-invoice"></a>元の請求書への参照を定義する

以下の手順で、指定したビジネス ドキュメントのタイプにオリジナルの請求書への参照を定義します。

### <a name="vendor-credit-note-purchase-order"></a>仕入先訂正票 (発注書)

1. **買掛金勘定** \> **発注書** \> **すべての発注書** に移動します。
2. 新しい発注書を作成するか、既存の発注書を使用して貸方書を作成します。
3. アクション ペインの、**請求書** タブで、**導入** グループから **貸方請求書** を選択します。
4. 訂正の理由と元の請求書の参照先を入力します。

### <a name="vendor-credit-note-ledger-journals"></a>仕入先訂正票 (仕訳元帳)

1. 次の手順のいずれかを実行します。

    - **買掛金勘定** \> **請求仕訳帳** の順に移動します。
    - **買掛金勘定** \> **請求書の登録** の順に移動します。
    - **総勘定元帳** \> **仕訳入力** \> **一般仕訳帳** の順に移動します。

2. 新規仕訳帳と新規仕訳帳明細行を作成します。
3. アクション ウィンドウで、**機能** \> **貸方請求書** を選択します。
4. 訂正の理由と元の請求書の参照先を入力します。

> [!NOTE]
> **勘定タイプ** フィールドが **仕入先** に設定されている場合は、**貸方請求書** コマンドが一般仕訳伝票に表示されます。

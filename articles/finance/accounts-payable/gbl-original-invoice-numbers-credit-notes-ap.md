---
title: 訂正票での元の請求書への参照 (仕入先請求書)
description: この記事では、訂正票を作成する際に元の請求書への参照を作成する方法について説明します。
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: 39cf4eb7eef1a83abeb7bd44fa7b2abefee0806e
ms.sourcegitcommit: 8eb0cafe5ad20be2c4fff684e88d7d3f2249f820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2022
ms.locfileid: "9409667"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>訂正票での元の請求書への参照 (仕入先請求書)

[!include [banner](../includes/banner.md)]

一部の国や地域では、印刷された訂正票またはレポーティング ルーチンに元の請求書への参照を含めるという法的要件があります。 この記事では、訂正票を作成する際に元の請求書への参照を作成する方法について説明します。

## <a name="prerequisites"></a>必要条件

**機能管理** ワークスペースで、**仕入先請求書の請求の貸方転記を有効にする** 機能を有効にします。 詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。

この記事で説明する機能は、以下のドキュメントに適用されます。

**買掛金勘定:**

- 発注書
- 請求仕訳帳
- 仕入帳

**総勘定元帳:**

- 一般仕訳帳

## <a name="define-a-reference-to-an-original-invoice"></a>元の請求書への参照を定義する

元の請求書への参照を定義するには、次の高レベルの手順が含まれます:
1. 仕入先請求書を作成して転記します。
2. 仕入先訂正票を作成します。
3. 請求書を訂正票にリンクするには、請求の貸方記入を使用します。
4. 訂正票を転記します。

以下の手順で、指定したビジネス ドキュメントのタイプにオリジナルの請求書への参照を定義します。

### <a name="vendor-credit-note-purchase-order"></a>仕入先訂正票 (発注書)

1. **買掛金勘定** > **発注書** > **すべての発注書** の順に移動します。
2. 新しい発注書を作成するか、既存の発注書を使用して訂正票を作成します。
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

---
title: 税計算パラメーター内の空の税機能リスト
description: このトピックでは、[税計算パラメータ] ページの税機能の一覧が空白になっている問題のトラブルシューティング方法について説明します。
author: wangchen
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 5b87499042c9c4bfe76e182b170adf4f1cfeac4b
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388567"
---
# <a name="empty-tax-feature-list-in-tax-calculation-parameters"></a>税計算パラメーター内の空の税機能リスト

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="symptom"></a>現象

Regulatory Configuration Service (RCS) に機能が公開されているので、Microsoft Dynamics 365 Finance で使用することができます 。 ただし、財務を開いて、**税金** \> **設定** \> **税コンフィギュレーション** \> **税計算パラメーター** に移動し、**機能の設定名** フィールドで値を選択しようとする場合、値の一覧は空です。

## <a name="reason"></a>理由

通常、この問題が発生するのは、財務環境と RCS 環境が同じテナントの下にないためです。

### <a name="rcs-tenant"></a>RCS テナント

ご利用の RCS テナントの ID を検索するには、次の手順を実行します。

1. RCS の URL 全体をコピーします。 URL は次のようなものになるでしょう: [`https://rcs-rts-sf-ed22b5aeea8-int-westus2.configure.global.int.dynamics.com/namespaces/817ff7a0-0d77-4aba-9360-3c9749e2c5de/?cmp=dat&mi=RCSFeatureDomainsWorkspace`]。
2. InPrivate ブラウザ ウィンドウを開き、RCS URL をアドレス バーに貼り付け、**Enter** キーを押します。 サインイン ページにアクセスして、RCS テナント ID を確認できます。 たとえば、サインイン ページの URL が `https://login.microsoftonline.com/d335a570-a05b-4bc5-8eb3-c42c65f9560d` である場合、テナント ID は、`https://login.microsoftonline.com/` または **d335a570-a05b-4bc5-8eb3-c42c65f9560d** の後に表示される情報です。

### <a name="finance-environment-tenant-id"></a>財務環境テナント ID

財務環境のテナント ID を検索するには、RCS テナント検索手順と同じ手順を使います。 ただし、完全な RCS URL ではなく、財務環境の完全な URL をコピーして貼り付けます。

## <a name="resolution"></a>解決策

2 つのテナント ID が異なる場合は、このトピックで説明されている問題が発生します。 同じ場合は、関連しない問題が発生します。 その場合は、Microsoft サポートに連絡することをお勧めします。

### <a name="solution-1"></a>ソリューション 1

RCS 環境を、財務環境がサインインしているのと同じテナントにサインインします。 次に、税金機能を作成して公開します。

### <a name="solution-2"></a>ソリューション 2

税金機能を RCS の財務テナントと共有します。

1. RCS で、**グローバリゼーション機能**\> **税計算** の順にクリックします。
2. 共有する機能を選択して、次に、**組織** タブで **共有先** を選択します。
3. **組織ドメイン名** フィールドで、名前を入力します。 たとえば、**contoso.onmicrosoft.com** と入力します。
4. **共有** を選択します。

![外部組織ドロップダウン ダイアログ ボックスを共有します。](media/ShareTaxFeature.png)

---
title: ギフト カードの会社間データ共有
description: この記事では、Microsoft Dynamics 365 Commerce を構成して、データ領域間で Dynamics 365 Finance データ共有機能を使用してギフト カード データを同期する方法について説明します。
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: b56890b546c3cd74b75cf447e62495733ea8d288
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/31/2022
ms.locfileid: "9387069"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>ギフト カードの会社間データ共有

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

この記事では、Microsoft Dynamics 365 Commerce を構成して、Dynamics 365 Finance データ共有機能を使用してギフト カード データを同期する方法について説明します。 次に、データ レコード共有機能を使用して、2 つのデータ領域間で会社間でデータを共有できます。 こうすることで、Commerce 内部ギフト テーブルが 2 つの会社エンティティ間でデータを共有できます。 Dynamics 365 Finance の会社間データ共有の詳細については、[会社間データ共有](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing)を参照してください。

## <a name="key-terms"></a>重要な用語

| 相談 | Description |
|---|---|
| 法人 | Dynamics 365 Finance 環境の法人。 |
| ギフト カード | Dynamics 365 Commerce 内部ギフト カード製品。 |

## <a name="prerequisites"></a>必要条件

ユーザーは、[会社間データ共有](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing)の説明に従って、会社間データ共有のための環境を構成する必要があります。

ギフト カード テーブルで重複レコード共有 (DRS) を有効にするには、**RetailGiftCardTable** の **DataSharingType** フィールドを **複写** に設定する必要があります。 詳細については、[開発者向け会社間データ共有](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev) を参照してください。

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>ギフト カードの会社間データ共有を構成する

ギフト カードのために会社間データ共有を構成にするには、以下の手順を実行します。

1. Commerce headquarters で、**システム管理者\>セットアップ\>会社間データ共有のコンフィギュレーション** の順に移動します。
1. アクション ペインで **新規** を選択し、データ共有レコードを追加します。
1. **名前** フィールドに、新しいデータ共有レコードの名前を入力します (たとえば、**Gift Cards**)。
1. **共有するテーブルとフィールド** セクションで、**追加** を選択します。
1. **新しいテーブルの共有** ダイアログ ボックスの **テーブル名** フィールドに、**RETAILGIFTCARDTABLE** (小売ギフト カード用のテーブル) と入力します。 **テーブル ラベル** フィールドは、自動的に **ギフト カード テーブル** に設定されると思います。
1. **会社ごとにデータを保存する**、**一意のインデックスを持つ**、**まだ共有していない** チェック ボックスがオンになっていることを確認します。 これらのチェック ボックスをオンにすると、データ共有機能に関連する検証がトリガされます。
1. **テーブルの追加** を選択します。 **ギフト カード テーブル (RetailGiftCardTable)** レコードが、**共有するテーブルおよびフィールド** の下に表示されます。 共有のためにテーブルに自動的に関連付けられるすべてのテーブル フィールドを表示するには、キャレット (^) 記号を選択します。
1. **これらのテーブルのセクションでレコードを共有する会社** で、**追加** を選択して、データを共有する会社を追加します。
1. **会社** の下の行にあるドロップダウン リストで会社を選択します。
1. **名前** フィールドに、会社名を入力します。
1. ステップ 8～10 を繰り返して会社行を追加します。
1. 会社の行の追加が完了したら、アクション ウィンドウで **有効化** を選択 します。
1. 「このアクションは営業時間外に実行することをお勧めします。 ポリシー内のテーブルに対する同時トランザクション操作は失敗します。 続行しますか?」という警告メッセージが表示されます。 **はい** を選択して同意します。
1. 「すべての共有会社の間で、すべての既存データを今すぐコピーしますか? **はい** を選択して同意します。

両方のメッセージに合意すると、構成されている会社全体でデータのコピーがテーブルによって開始されます。 すると、ある会社のギフト カードに対して発生した残高がもう一方の会社に表示されます。

## <a name="additional-resources"></a>追加リソース

[支払に関するよく寄せられる質問](payments-retail.md)

[チェックアウト モジュール](../add-checkout-module.md)

[支払モジュール](../payment-module.md)

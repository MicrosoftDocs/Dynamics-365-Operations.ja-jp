---
title: 生産需要に基づく委託販売在庫の所有権の変更
description: この手順は、生産中における在庫需要があるときに委託製品在庫所有者を仕入先から自らの法人に変更する方法を示します。
author: perlynne
manager: tfehr
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c50affa05b8df53d31660854f4d1ead6aeff820
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204243"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>生産需要に基づく委託販売在庫の所有権の変更

[!include [banner](../../includes/banner.md)]

この手順は、生産中における在庫需要があるときに委託製品在庫所有者を仕入先から自らの法人に変更する方法を示します。 所有権を変更するには、在庫所有権変更仕訳を作成、転記します。 所有権変更は、既存の生産需要に基づき、この記録で示されるように手作業で作成します。 通常、現場の監督者がこの作業を実施します。 デモ データ会社 USMF でこの手順を使うか、または独自のデータを使うことができます。 自分のデータを使用する場合は、次の条件があることを確認します: 在庫所有権変更に設定された在庫仕訳、物理的に記録された仕入先所有の手持在庫品目、原材料の複数の製造オーダーライン この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。

> [!NOTE]
> 出庫委託販売プロセスはそのままサポートされておらず、自動的な所有権仕訳のプロセスもサポートされていません。

## <a name="create-an-inventory-ownership-journal"></a>在庫所有権仕訳を作成する
1. [在庫管理] > [仕訳入力] > [品目] > [在庫所有権変更] の順に移動します。
2. [新規] をクリックします。
    * 在庫所有権変更仕訳は、委託製品在庫の所有者を仕入先から現事業者に変更するために用いられます。 この所有権を変更するには、仕入先所有の手持在庫を解除して現事業者で当該在庫を受領します。  
3. [名前] フィールドで値を入力または選択します。
    * 所有権変更の仕訳種類がある在庫仕訳名のみ選択できます。  
4. [OK] をクリックします。
5. [機能] をクリックします。
6. [製造オーダーから仕訳帳明細行を作成] をクリックします。
    * 原材料消費の需要を有する製品を問い合わせることで所有権変更処理を変更することができます。  
7. フィールドを含む在庫払出では、オプションを選択します。
    * このオプションによって、在庫トランザクションの状態別にフィルターすることができます。 たとえば、物理的状況を選択、保存している在庫の仕訳を作成できます。  
8. [対象に含めるレコード] セクションを展開します。
    * このセクションでは、追加のフィルターを適用することができます。 たとえば、特定の原材料の日付を選択できます。  
9. [OK] をクリックします。

## <a name="post-the-inventory-ownership-change-journal"></a>在庫所有権変更仕訳を転記する
1. [転記] をクリックします。
    * 仕訳を記帳する際、仕入先所有の在庫は「所有権変更」の参照で解除されます。 その後在庫は、購入注文製品受領書で更新された在庫トランザクションを使用して手持ちの在庫として受領されます。 記帳済み仕訳に関連するトランザクションのみが作成されることに注意してください。 在庫トランザクションの予定は作成されません。  
2. [OK] をクリックします。
3. ページを閉じます。


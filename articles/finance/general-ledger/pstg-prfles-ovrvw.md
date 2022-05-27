---
title: 転記プロファイルの概要
description: このトピックでは Microsoft Dynamics 365 アプリ全体での転記プロファイルの使用方法について説明します。
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9ad33d9a34bc449b81ec6d02a78b9ca1653aca5
ms.sourcegitcommit: 96f936267d3f314f06da6ce6f809eba2ec3b205f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/24/2022
ms.locfileid: "8018382"
---
# <a name="posting-profiles-overview"></a>転記プロファイルの概要

Finance and Operations のアプリでは、*転記プロファイル* という用語は、補助元帳勘定を主勘定に変換する方法を制御する構成を記述するために使用され、転記プロファイルは一般会計に転記されるトランザクションで使用できます。 たとえば、転記プロファイルは請求書の転記時に顧客がどのように売掛金勘定の主勘定に変換するかを制御します。

一部のモジュールと機能には、名前に "転記プロファイル" という語を含むページがあります (**顧客転記プロファイル** や **仕入先転記プロファイル** など)。 また、一部のモジュールには、補助元帳から生成されるトランザクションの元帳転記を構成する複数のオプションがあります。 たとえば、**生産管理** モジュールでは、生産グループ、リソース、またはリソース グループ別に転記を設定できます。

多くのタイプのトランザクションでは、転記プロファイルの代わりに転記の定義があります。 サポートされている文書では、転記プロファイルの代わりに転記の定義を使用して、勘定項目の主勘定と財務分析コードを分類できます。 債務または事前の債務の使用を計画している場合は、会計項目の勘定を定義するために転記の定義が必要です。

転記プロファイル、転記の定義、または **自動トランザクションの勘定** ページを構成する前に、構成する法人の **勘定科目表** ページで勘定科目表を構成する必要があります。

## <a name="posting-types"></a>転記タイプ

Finance and Operations アプリでは、転記タイプを使用して、借方または貸方の一般カテゴリーを定義します。 このカテゴリーは、一般会計の主勘定からは独立しています。 一般会計の借方または貸方にはいくつかの転記タイプがあります。

1 つの伝票には 1 つ以上の転記タイプを設定できます。 たとえば、勘定および相手勘定が **元帳** に設定されている一般仕訳帳を介して転記されるトランザクションは、借方と貸方の両方に対して **仕訳元帳** の転記タイプがあります 。 一方、仕入先請求書には複数の転記タイプがあります。 これらの転記タイプには、仕入先残高の 1 行と相殺項目の追加の明細行 (**仕訳元帳** など) が含まれます。

転記タイプは、**伝票トランザクション** ページの **全般** タブで **転記タイプ** フィールドに表示されます。

> [!TIP]
> **パーソナル化** ツール バーを使用して、**概要** タブのグリッドに **転記タイプ** フィールドを追加するか、または移動することができます。 この方法で、このフィールドに簡単にアクセスしたり伝票を表示することができます。

## <a name="detail-settings-for-a-posting-profile"></a>転記プロファイルの詳細設定 

転記プロファイルの構成時、**アカウント コード** フィールドは設定のレベルを定義します。 **テーブル**、**グループ**、**すべて** のオプションを選択できます。 一致は最初の一致の後に停止し、順序は最も具体的なレベルから最も具体性の低いレベルとなります。 **アカウント コード** フィールドの名前が若干異なる場合でも、このフィールドの動作と機能は変わりません。 たとえば、在庫転記プロファイルには、**品目コード** フィールドと **アカウント コード** フィールドが含まれます。 どちらのフィールドにも **テーブル**、**グループ**、**すべて** の値があります。

転記プロファイルの **主勘定** フィールドが空白のままで、**自動トランザクションの勘定** ページまたはモジュール固有または機能固有のページで主勘定を構成しきっていない場合は、転記タイプが使用されるトランザクションを転記するときにエラー メッセージが表示されます。 通常は、"\[転記タイプ\] の勘定が見つかりません" というメッセージが表示されます。

### <a name="table-value"></a>テーブル値

**テーブル** の値 は、転記プロファイルに関連付けられているマスター レコードを参照します。 各テーブル レコードは 1 つの値に固有です。 **アカウント コード** フィールドの後に表示されるフィールドの値を指定します。 通常、このフィールドは **勘定** または **勘定グループ番号** になります。 正確な名前は、表示されるページによって異なります。

たとえば、顧客転記プロファイルを使用している場合は、**テーブル** の値は特定の顧客を表します。 **アカウント コード** フィールドで **テーブル** を選択した場合は、**勘定/グループ番号** フィールドで顧客を選択する必要があります。

**テーブル** の値は最も具体的なタイプのレコードを表します。 **グループ** または **すべて** の値が選択されている別のレコードを構成している場合でも、常にこの値が使用されます。 この値は、**自動トランザクションの勘定** ページで既定値として作成した値も上書きされます。

転記プロファイルの管理の基本メカニズムとして **テーブル** 値を使用することをお勧めしません。これは、マスター データ レコードごとに別個の転記プロファイルを管理すると、データ品質上の問題が発生する可能性があるからです。 また、各マスター データ レコードに対して個別の転記プロファイルを管理および調整することは困難です。 この値は、転記プロファイルで例外を管理するために使用する必要があります。

### <a name="group-value"></a>グループ値

**グループ** 値は、転記プロファイルに関連付けられているマスター レコードによってサポートされるグループ化レコードを参照します。 各グループ レコードは 1 つの値に固有です。 **アカウント コード** フィールドの後に表示されるフィールドの値を指定します。 通常、このフィールドは **勘定** または **勘定グループ番号** になります。 正確な名前は、表示されるページによって異なります。

**グループ** の値を使用するには、まずグループを構成し、それを勘定の 1 つ以上 のレコードにリンクする必要があります。 **グループ** の値は **テーブル** の値より具体性が低くなりますが、**すべて** の値より具体性があります。 テーブルに対してレコードが構成されていない場合、そのレコードが属するグループのレコードが検索されます。

たとえば、顧客転記プロファイルを使って作業している場合に、**アカウント コード** フィールドで **グループ** を選択した場合、**勘定/グループ番号** フィールドで顧客グループを選択する必要があります。 **顧客グループ** ページでは顧客グループを事前に定義する必要があります。そして、顧客を作成する際は、顧客グループを指定する必要があります。

特定の転記タイプに対して複数の主勘定を追跡する必要がある場合は、**グループ** 値を使用することをお勧めします。 たとえば、売掛金勘定取引の主勘定が 3 つ、1 つは通常の顧客用、1 つは従業員用、もう 1 つは会社間販売用がある場合です。 この場合は、顧客を区分する 3 つの顧客グループを作成することをお勧めします。 その後、各顧客グループを顧客転記プロファイルの正しい主勘定にマップします。 次の表に、この例の 3 つの顧客グループを示します。

| 顧客グループ | Name | Description |
|----------------|------|-------------|
| EXT | 外部顧客 | このグループは、すべての標準の外部向け顧客に対して使用されます。 |
| EMP | 従業員 | このグループは、あなたの組織から購買を行うすべての従業員に使用されます。 |
| INT | 会社間販売 | このグループは、統合販売や発注書を使う会社間顧客勘定すべてで使用します。 |

次に、この転記プロファイルで 3 つの明細行を設定します。 各明細行で、**グループ** 値と関連する主勘定を選択します。

### <a name="all-value"></a>すべての値

**すべて** の値は、設定がすべてのレコードに適用されます。 **アカウント コード** フィールドで **すべて** の値を選択した場合、**勘定/グループ番号** フィールドは使用できません。また、構成を適用する特定のレコードを 選択することはできません。

**すべて** の値が最も具体性が低い場合。 これは、システムで **テーブル** または **グループ** の値との一致が見つからない場合にのみ使用されます。 特定の転記タイプに対して主勘定が 1 つしかない場合は、**すべて** の値を選択する必要があります。

たとえば、顧客転記プロファイルを使用している場合は、指定した主要勘定が、特定のテーブル (顧客) またはグループ (顧客グループ) のレコードを持たない他のすべての顧客および顧客グループに適用されます。

### <a name="category"></a>カテゴリ

在庫転記プロファイルには、販売カテゴリまたは調達カテゴリに固有の追加値があります。 この値は **テーブル** の値と似て、特定の販売カテゴリーまたは調達カテゴリーにのみ適用されます。

### <a name="default-value"></a>既定値

**勘定コード** フィールドが **すべて** に設定されている転記プロファイルで転記タイプのレコードを作成しない場合に、**グループ** または **テーブル** の値に対応する転記プロファイル レコードが見つからな場合は、**自動トランザクションの勘定** ページで指定できる既定値に戻ります。 詳細については、[自動トランザクションの勘定](accounts-for-auto-transactions.md) を参照してください。

## <a name="clearing-accounts"></a>清算勘定

会計では通常、*精算勘定* という用語がよく使用されます。 Microsoft Dynamics 365 アプリの一部の転記タイプは精算勘定です。 つまり、別のトランザクションが転記された場合に勘定の残高が精算または取り消されます。 たとえば、発注書製品の入庫を転記すると、製品の見積原価と、税金と購買注文明細行の請求金額の合計が、購買計上転記タイプに負債として転記されます。 後で発注書を請求すると、残高が購買計上転記タイプから取り消され、買掛金勘定の取引勘定に移動します。

## <a name="additional-resources"></a>追加リソース

Dynamics 365 Finance、Dynamics 365 Supply Chain Management、Dynamics 365 Commerce、および Dynamics 365 Project Operations の多くのモジュールには、総勘定元帳への転記方法を制御する転記プロファイルまたは追加構成があります。 各モジュールの転記プロファイルと転記設定の詳細については、次のトピックを参照してください。

- [自動トランザクションの勘定](accounts-for-auto-transactions.md)
- [買掛金勘定の転記](accts-payble-posting.md)
- [買掛金勘定の転記](accts-recvble-posting.md)
- [資産リースの転記](../asset-leasing/set-up-lease-posting-accts.md)
- 資産管理の転記 (近日予定)
- 現金および銀行管理パラメーター (近日予定)
- 通貨再評価転記勘定 (近日予定)
- 経費管理の転記 (近日予定)
- [固定資産転記プロファイル](../fixed-assets/tasks/set-up-fixed-asset-posting-profiles.md)
- 会社間勘定の転記 (近日予定)
- 在庫転記プロファイル (近日予定)
- [陸揚原価の転記](../../supply-chain/landed-cost/costing-parameters-setup.md)
- [転記の定義の概要](posting-definitions.md)
- 生産管理の転記 (近日予定)
- プロジェクト管理および会計の転記 (近日予定)
- サービス管理の転記 (近日予定)
- 税金の転記 (近日予定)
- 時間と出勤の転記 (近日予定)
- 輸送管理の転記 (近日予定)
- リベート管理の転記プロファイル (近日予定)
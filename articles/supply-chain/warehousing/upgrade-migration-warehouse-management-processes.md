---
title: "Microsoft Dynamics AX 2012 から Finance and Operations への倉庫管理のアップグレード"
description: "このトピックでは、製品および倉庫管理の移行オプションの概要を示します。"
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocationWHSProcessEnablement, WHSLocationProfile, InventTableStorageDimensionGroupChange, InventUpdateBlockedItem, WHSParameters, WHSReservationHierarchy, WHSUOMSeqGroupTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1714054
ms.assetid: 79a1a3b9-3a36-4162-8839-ec39b5e26602
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0ff3a22b89ce22096198d2e1dd1ea9ed10239a9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="upgrade-warehouse-management-from-microsoft-dynamics-ax-2012-to-finance-and-operations"></a>Microsoft Dynamics AX 2012 から Finance and Operations への倉庫管理のアップグレード

[!include [banner](../includes/banner.md)]

このトピックでは、WMSII モジュールを実行している Microsoft Dynamics AX 2012 R3 から Microsoft Dynamics 365 for Finance and Operations にアップグレードするプロセスの概要を示します。

Finance および Operations は、Microsoft Dynamics AX 2012 のレガシ **WMSII** モジュールをサポートしていません。 代わりに、**倉庫管理**モジュールが使用できます。 WMSII モジュールでは、場所とパレット ID の在庫分析コードを資産在庫用に選択することができます。ただし、パレット ID の在庫分析コードは、Finance and Operations の資産在庫で使用することはできません。

アップグレード時に、パレット ID の在庫分析コードを使用する保管分析コード グループに関連付けられているすべての製品が識別され、ブロック済としてマークされますが、アップグレード用にはプロセスされません。

## <a name="upgrading-to-finance-and-operations-when-ax-2012-r3-wmsii-is-used"></a>AX 2012 R3 WMSII を使用している場合、Finance および Operations にアップグレードします。
アップグレード後、**品目の保管分析コード グループの変更**フォームの一連のオプションを使用して、アップグレード中にブロックされた製品のブロック解除、およびそれらの製品のトランザクションの処理ができます。

### <a name="enabling-items-in-finance-and-operations"></a>Finance および Operations の有効な品目
Finance および Operations では、品目の追跡は倉庫管理プロセスに含まれているため、この変更が必要になります。 これらのプロセスのために、すべての倉庫およびその場所は、場所プロファイルに関連づける必要があります。 倉庫管理プロセスを使用する場合は、以下がコンフィギュレーションされている必要があります。
-   既存の倉庫は、倉庫管理プロセスを使用するために有効にする必要があります 
-   既存のリリース済製品は、倉庫管理プロセスを使用する保管分析コード グループと関連付ける必要があります 

ソースの保管分析コード グループがパレット ID の在庫分析コードを使用する場合、パレット ID の在庫分析コードを使用する既存の手持ち在庫の場所は、**ライセンスプレートの追跡を使用**パラメーターが選択されている場所プロファイルと関連付ける必要があります。 もし既存の倉庫を、倉庫管理プロセスを使用するために有効にしないなら、既存の手持ち在庫の保管分析コード グループを、サイト、倉庫、場所の在庫分析コードのみを処理するグループに変更することができます。 

> [!NOTE] 
>  未処理の在庫トランザクションが存在する場合でも、品目の保管分析コード グループを変更することができます。

## <a name="find-products-that-were-blocked-because-of-pallet-id"></a>パレット ID が原因でブロックされた商品を検索します
アップグレード中にブロックされ処理できないリリース済製品の一覧を表示するには、**在庫管理**&gt;、**設定**&gt;、**在庫**&gt;、**在庫更新に対してブロックされている品目**の順にクリックします。

## <a name="change-storage-dimension-group-for-blocked-products"></a>ブロックされた製品の保管分析コード グループを変更します 
 
倉庫管理プロセスの一部として使用されるには、品目が、場所の在庫分析コードが有効で、**倉庫管理プロセスの使用**パラメーターが選択されている保管分析コード グループに関連付けられている必要があります。 この設定を選択すると、サイト、倉庫、在庫状態、場所、およびライセンスプレートの在庫分析コードが有効になります。

アップグレード中にブロックされた製品のブロックを解除するには、製品の新しい保管分析コード グループを選択してください。 未処理の在庫トランザクションが存在する場合でも、保管分析コード グループを変更することができることに注意してください。 アップグレード中にブロックされた品目を使用するには、2 つのオプションがあります:

-   品目の保管分析コード グループを、サイト、倉庫、および場所の在庫分析コードのみ使用する保管分析コード グループに変更します。 この変更の結果として、パレット ID の在庫分析コードは使用されません。
-   品目の保管分析コード グループを、倉庫管理プロセスを使用する在庫分析コードの保管分析コード グループに変更します。 この変更の結果として、ライセンスプレートの在庫分析コードが使用されます。

## <a name="configure-warehouse-management-processes"></a>倉庫管理プロセスのコンフィギュレーション
リリースされた製品を**倉庫管理**モジュールで使用する前に、製品は**倉庫管理プロセスを使用**パラメーターが選択された保管分析コード グループを使用する必要があります。

### <a name="enable-warehouses-to-use-warehouse-management-processes"></a>倉庫管理プロセスを使用するために、倉庫を有効にします

1.  少なくとも 1 つの新しい場所プロファイルを作成します。
2.  **倉庫管理**&gt;**設定**&gt;**倉庫管理プロセスの有効化**&gt;**倉庫設定の有効化**をクリックします。
3.  **倉庫設定の有効化** ページで、有効にする必要がある倉庫を追加します。 ページ上に直接、または Microsoft Office 統合のどちらかを使用して、このステップを完了できます。
4.  すべての場所に場所プロファイルを割り当てます。 この手順は、ページから直接 Microsoft Office 統合を使用して簡単に実行することができます。 データのエクスポートとインポートまたは、[データ管理](../../dev-itpro/data-entities/data-entities.md) でデータ エンティティプロセスのいずれかを行うことができます。
5.  変更の検証。 検証プロセスの一部として、データの整合性のさまざまな検証が実行されます。 より大きなアップグレード プロセスの一部として、発生した問題をソースの実装上で調整する必要があるかもしれません。 この場合は、追加のデータ アップグレードが必要になります。
6.  変更の処理。

### <a name="change-the-storage-dimension-group-for-items-so-that-it-uses-warehouse-management-processes"></a>倉庫管理プロセスを使用するために、品目の保管分析コード グループを変更します。

1.  新しい**在庫状態**値を作成し、**倉庫管理パラメーター**設定の**既定の在庫状態 ID** として割り当てます。
2.  新しい**倉庫管理プロセスの使用**パラメーターが選択されている保管分析コード グループを作成します。
3.  **引当階層** ページで、品目の保管および追跡用分析コード グループに沿って、新しい引当階層を定義します。
4.  少なくとも品目の在庫単位に使用されている同じ単位が含まれる、1 つまたはそれ以上の単位順序グループを作成します。
5.  **倉庫管理**&gt;、**設定**&gt;、**倉庫管理プロセスの有効化**&gt;、**品目の保管分析コード グループの変更**の順にクリックします。
6.  **品目の保管分析コード グループの変更** ページで、品目番号、保管分析コード グループ、および単位順序グループを追加します。 ページ上に直接、Microsoft Office 統合の使用、または[データ管理](../../dev-itpro/data-entities/data-entities.md)にあるデータ エンティティプロセスを使用してこのステップを完了できます。
7.  変更の検証。 検証プロセスの一部として、データの整合性のさまざまな検証が実行されます。 より大きなアップグレード プロセスの一部として、発生した問題をソースの実装上で調整する必要があるかもしれません。 この場合は、追加のデータ アップグレードが必要になります。
8.  変更の処理。 すべての在庫分析コードの更新にはしばらく時間がかかる場合があります。 バッチ ジョブタスクを使用して、進捗状況を監視することができます。


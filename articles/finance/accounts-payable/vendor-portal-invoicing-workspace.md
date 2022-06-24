---
title: 仕入先コラボレーションの請求ワークスペース
description: この記事では、仕入先請求書を表示する方法、および仕入先コラボレーションの請求ワークスペースの表示から請求書を送信する方法について説明します。
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9ef4204e0be437b50af047704e07600653c877c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896553"
---
# <a name="vendor-collaboration-invoicing-workspace"></a>仕入先コラボレーションの請求ワークスペース

[!include [banner](../includes/banner.md)]

この記事では、仕入先請求書を表示する方法、および **仕入先コラボレーションの請求** ワークスペースの表示から請求書を送信する方法について説明します。

**仕入先コラボレーションの請求** ワークスペースは、仕入先請求書の情報を表示したり、ワークフロー機能を使用して請求書を提出するために使用されます。


## <a name="vendor-collaboration-invoicing-workspace"></a>仕入先コラボレーションの請求ワークスペース

### <a name="summary-tiles"></a>概要タイル

**集計** タイルには、選択された仕入先の請求書の概要が示されます。 これらの状況によって請求書を表示できます。
-   下書きの請求書がワークフローに対して提出されませんでした。
-   提出済で承認されていない請求書は、仕入先が提出した請求書ですが、これらはアプリケーションには転記されていません。
-   承認され、支払されていない請求書が転記されましたが、完全には支払われていません。
-   支払済の請求書は、アプリケーションに全額支払われた請求書です。

タイルをクリックすると、フィルター処理された **請求書の一覧** ページが開きます。

### <a name="tabular-lists"></a>表形式リスト

**表形式リスト** セクションでは、請求の状態は概要タイル (**下書き** と **提出済**、**未承認** リスト) と同様の方法で分割されます。 **下書き** の状態では、請求書がワークフローに提出されるかまたは削除されます。 最後の表形式の一覧は、請求書を検索するためのオプションです。 検索する際、検索をより迅速に行うために、フィルター処理することができます。

### <a name="all-vendor-invoices-list-page"></a>すべての仕入先請求書リスト ページ

**仕入先コラボレーション請求書** リストページの全ての転記済みおよび未転記の仕入先請求書を表示できます。 このリストページを使用して、請求書の支払状態を表示します。 支払ステータスには、**未転記**、**未払**、**部分的な支払**、**全額支払** が含まれます。
発注書から新しい請求書を作成する

**仕入先コラボレーションの請求** ワークスペースで **新規** のアクションを選択して、新しい仕入先請求書を作成します。 仕入先から発注書番号および請求書番号が提供されている必要があります。 既定では、仕入先の発注書の明細行はすべて、新しい請求書に表示されます。 数量、および原価情報は、現在の仕入先請求書からワークフローに送信する前に編集できます。 請求書に情報を送信する前に、ファイル、メモ、画像ファイルおよび URL を添付することができます。

詳細については次を参照してください。[外部仕入先との仕入先コラボレーション](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

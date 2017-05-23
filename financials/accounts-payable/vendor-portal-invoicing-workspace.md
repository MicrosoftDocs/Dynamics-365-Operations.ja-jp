---
title: "仕入先コラボレーションの請求ワークスペース"
description: "このトピックでは、仕入先請求書を表示する方法、および仕入先コラボレーションの請求ワークスペースの表示から請求書を送信する方法について説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 7aebcdf0578d931d326420b42e2b220407049bc6
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="vendor-collaboration-invoicing-workspace"></a>仕入先コラボレーションの請求ワークスペース

[!include[banner](../includes/banner.md)]


このトピックでは、仕入先請求書を表示する方法、および仕入先コラボレーションの請求ワークスペースの表示から請求書を送信する方法について説明します。

[**仕入先コラボレーションの請求**] ワークスペースが、仕入先請求書の情報を表示するために使用され、ワークフロー機能を使用して Microsoft Dynamics 365 for Operations に請求書を提出するために使用されます。
仕入先コラボレーションの請求ワークスペース
----------------------------------------

### <a name="summary-tiles"></a>概要タイル

[**集計**] タイルには、選択された仕入先の請求書の概要が示されます。 これらの状況によって請求書を表示できます。
-   下書きの請求書がワークフローに対して提出されませんでした。
-   提出済で承認されていない請求書が、仕入先が提出した請求書ですが、これらは Dynamics 365 for Operations には転記されていません。
-   承認され、支払されていない請求書が、Dynamics 365 for Operations には転記されましたが、完全には支払われていません。
-   支払済の請求書は、Dynamics 365 for Operations に全額支払われた請求書です。

タイルをクリックすると、フィルター処理された [**請求書の一覧**] ページが開きます。
### <a name="tabular-lists"></a>表形式リスト

[**表形式リスト**] セクションでは、請求の状態は概要タイル (下書きと提出済、未承認リスト) と同様の方法で分割されます。 下書きの状態では、請求書がワークフローに提出されるかまたは削除されます。 最後の表形式の一覧は、請求書を検索するためのオプションです。 検索する際、検索をより迅速に行うために、フィルター処理することができます。
すべての仕入先請求書リスト ページ
-----------------------------

**仕入先コラボレーション請求書** リストページの全ての転記済みおよび未転記の仕入先請求書を表示できます。 このリストページを使用して、請求書の支払状態を表示します。 支払状態には、未転記、未払、部分的な支払、全額支払が含まれます。
発注書から新しい請求書を作成する
--------------------------------------------

[**仕入先コラボレーションの請求**] ワークスペースで [**新規**] のアクションを選択して、新しい仕入先請求書を作成します。 仕入先から発注書番号および請求書番号が提供されている必要があります。 既定では、仕入先の発注書の明細行はすべて、新しい請求書に表示されます。 数量、および原価情報は、現在の仕入先請求書からワークフローに送信する前に編集できます。 請求書に情報を送信する前に、ファイル、メモ、画像ファイルおよび URL を添付することができます。



詳細については次を参照してください。[仕入先ポータルを使用して、仕入先と連携](/dynamics365/operations/supply-chain/procurement/collaborate-vendors-vendor-portal)




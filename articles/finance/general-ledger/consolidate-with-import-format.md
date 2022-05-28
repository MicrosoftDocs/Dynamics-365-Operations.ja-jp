---
title: 連結に使用するインポート形式
description: このトピックでは、複数の法人からの財務データを連結する際に使用するインポート形式に関する説明をします。
author: jinniew
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5bea69d72ac93d29ae67dd6d762e1376d9a282f0
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735786"
---
# <a name="import-format-for-consolidation"></a>連結に使用するインポート形式

[!include [banner](../includes/banner.md)]

このトピックでは、複数の法人からの財務データを連結する際に使用するインポート形式に関する説明をします。 インポート形式は、テキスト (.txt) ファイルで保存する必要があります。

## <a name="import-format"></a>インポート形式

次の表に、インポート時の連結で使用するインポート形式の一覧を示します。

| レコード テーブル | 書式設定 | 摘要 |
|--------------|---------|-------|
| 1            | 170150、グッドウィル、4 | <ul><li>レコード テーブル</li><li>ソースの主勘定 ID</li><li>主勘定の明細</li><li>主勘定のタイプ</li></ul> |
| 2            | 110130、2015/01/01、1、USD、0、0、80699.39、0、1 | <ul><li>主勘定 ID</li><li>取引日付</li><li>会計年度期間のタイプ (**0** = 開始、 **1** = 営業、 **2** = 決算)</li><li>取引通貨</li><li>借方または貸方 (**0** = 借方、**1** = 貸方)</li><li>転記階層</li><li>取引金額</li><li>件数</li><li>ローカル RecID (トランザクションの一意の int64 値)</li></ul> |
| 3            | USMF0000009、2017/01/01、FY2017、1、2017,01,01、602200、USD、6053.6.0 | <ul><li>入力番号 (予算ヘッダー 取引番号)</li><li>予算ヘッダーの既定の日付</li><li>予算モデル ID</li><li>予算タイプ (**1** - 元の予算、**2** - 転送、**3** - リビジョン、**4** - 債務、**5** - 事前予算、**6** - 繰越予算、**7** - プロジェクト、**8** - 固定資産、**9** - 需要予測、**10** - 供給予測、**11** - 償却、**12** - 暫定予算。)</li><li>明細行の日付</li><li>明細行の主勘定 ID</li><li>明細行の通貨コード</li><li>明細行の金額、取引通貨</li><li>明細 (経費または収益) 予算タイプのリスト整数値</li></ul> |
| 4            | DEMF | RecordCompany は、ソースの法人です。 |
| 5            | 110130、2015/01/01、1、USD、0、0、80699.39、0、1 | <ul><li>主勘定 ID</li><li>トランザクション日</li><li>会計年度期間のタイプ (0 = 開始、 1 = 営業、 2 = 決算)</li><li>トランザクション通貨</li><li>借方または貸方 (0 = 借方、1 = 貸方)</li><li>転記階層</li><li>トランザクション金額</li><li>件数</li><li>ローカル RecID (トランザクションの一意の int64 値)</li></ul>  |
| 6            | BusinessUnit、1 部門、2 | セグメント順序で定義されている財務分析コードの属性。<p>**エクスポート** ページを使用して、属性の定義方法を確認できます。</p> |
| 7            | 002,1,658 | <ul><li>財務分析コードの値</li><li>RecordDimensions で提供されるインデックスとしての財務分析コード</li><li>RecordTrans または RecordTrans2 の固有レコード ID に関連付けられた一意のレコード ID</li></ul> |
| 8            | 002,1,1 | <ul><li>RecordBudget のトランザクションに関連付けられている分析コードの値</li><li>RecordDimensions で提供されるインデックスとしての財務分析コード</li><li>ファイル内のトランザクション明細行の順序に対応する、曖昧な行レコード ID</li></ul> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

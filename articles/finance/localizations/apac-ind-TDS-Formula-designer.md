---
title: TDS 計算の式デザイナー
description: この記事では、トランザクションに関連付けられた TDS グループのそれぞれの TDS 税コードに対して定義されている式に基づいて、源泉徴収税 (TDS) がどのように計算されるかの例を示しています。
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1196f7258c898a55f3f29ddce7457e6f527185d8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889864"
---
# <a name="formula-designer-for-tds-calculations"></a>TDS 計算の式デザイナー

[!include [banner](../includes/banner.md)]

この記事では、TDS の税コードごとに定義された計算式に基づいて、源泉徴収税 (TDS) がどのように計算されるかの例を示しています。 TDS 税コードは、トランザクションに関連付けられた TDS グループで定義されます。 TDS 式を設計する前に、TDSに必要な基本的な設定を以下の手順で行います。 

- **源泉徴収税グループ** ページを使って、TDSコンポーネントグループを設定します。 
- **源泉徴収税コンポーネント** ページを使用して、TDS コンポーネントを設定し、TDS コンポーネントグループを TDS コンポーネントに関連付けます。 
- **源泉徴収税コード** ページを使用して、TDS の税コードの設定と、TDS コンポーネントを税コードに関連付けます。 
- **源泉徴収税グループ** ページを使って、TDS税グループを設定します。 続いて、TDS の税コードを税グループに関連付け、**式デザイナー** ページを使って式を定義します。 

**式の例**

この例では、TDS グループ 「Rent」 は、仕入先 A に対して作成される購買請求書に関連付けることができます。請求金額は $100,000 です。 請求書の TDS 計算を表示するには、次の表を参照してください。

| TDS グループ                                                   | TDS グループに関連付けられた TDS 税コード | 先頭値              | 課税対象 (式デザイナー) | 計算式 (式デザイナー) | 基準額 | 計算済 TDS の金額 |
| ------------------------------------------------------------ | --------------------------------------- | ------------------ | --------------------------------- | :----------------------------------------: | ----------- | --------------------- |
| 賃料                                                         | TDS (TDS コンポーネント-TDS)                | 10%                | 総額                      |                                            | 100,000      | 10,000                 |
| 割増金 (TDS コンポーネント - 割増金)                         | 10%                                     | 総額を除く | +TDS                              |                   10000                    | 1.000        |                       |
| PE-Cess (TDS コンポーネント - PE-Cess)                            | 2%                                      | 総額を除く | +TDS+割増金                    |                   11000                    | 220         |                       |
| SHE Cess (TDS コンポーネント - SHE Cess)                          | 1%                                      | 総額を除く | +TDS+割増金                    |                   11000                    | 110         |                       |
| **請求書** **に** **対して** **計算された** **TDS** の **合計** | **11,330**                               |                    |                                   |                                            |             |                       |

伝票ノ入力は次のように作成されます。

| 口座           | 借方  | 与信 |
| ----------------- | ------ | ------ |
| 賃料              | 100,000 |        |
| 仕入先 A          |        | 100,000 |
| 仕入先 A          | 11,330  |        |
| TDS 買掛金       |        | 10,000  |
| 割増金買掛金 |        | 1.000   |
| PE-Cess 買掛金   |        | 220    |
| SHE Cess 買掛金  |        | 110    |

---
title: TDS 特約証明書番号を記録する
description: この記事では、仕入先に発行された源泉徴収 (TDS) 特約証明書の番号を記録する方法について説明します。
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
ms.openlocfilehash: 116bc5c4b4f5f0b95d05dc73f2a012fbbc065bf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846616"
---
# <a name="record-tds-concession-certificate-numbers"></a>TDS 特約証明書番号を記録する

[!include [banner](../includes/banner.md)]

この記事では、仕入先に発行された源泉徴収 (TDS) 特約証明書の番号を記録する方法について説明します。

1. **税 \> 間接税 \> 源泉徴収税 \> 源泉徴収税特約** の順に移動します。
2. **税タイプ** フィールドで、TDS 税タイプの特約証明書を記録する **TDS** を選択します。
3. **概要** タブ で 、**Alt+N** キーを押して明細行を作成します。

    [![新しい明細行のヘッダー。](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. **源泉徴収税コード** フィールドで、仕入先特約証明書の発行対象である TDS 税コードを選択します。 **源泉徴収税コード名** フィールドに、源泉徴収税コードの名前が表示されます。
5. **開始日** フィールドと **終了日** フィールドで 、TDS税コードを使用して特約ベースで仕入先の TDS を計算する特約証明書の有効期間を定義します。
6. **注釈** フィールド に、注釈を入力します。
7. **セクション** フィールドに、TDS 特約証明書の使用を変更する法的セクション コードを入力します。

    セクション コードが 197 の場合、値 "A" は、フォーム 26Q の [非控除/控除の理由] 列とフォーム 27Q の [非控除/控除の理由/控除額の引き下げ/総額設定 (使用する場合)] 列の両方に表示されます。 セクション コードが 197A の場合、両方の場所に値 "B" が表示されます。

8. 仕入先の TDS 特約証明書番号を記録する **証明書** クイック タブを選択します。
9. **仕入先アカウント** フィールドで、TDS 特約証明書を発行する仕入先を選択します。
10. **開始日** フィールドおよび **終了日** フィールドで 、TDS 特約証明書の有効期間を定義します。

    特約ベースでの TDS の計算は、仕入先の証明書が作成された期間に基づいて行われます。

11. **証明書** フィールドに、TDS特約証明書番号を入力します。

    [![証明書クイック タブ。](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. ページを閉じます。

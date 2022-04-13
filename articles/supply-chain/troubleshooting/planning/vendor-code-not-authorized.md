---
title: 仕入先コードが特定の製品および日付に対して承認されていない場合
description: 計画オーダーを確定する、または発注書に明細行を追加しようとすると、仕入先コードが製品と日付に対して承認されていないというエラー メッセージが表示されます。
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 917526dfcefb36ce6e59af6f1f5bebc23ee6e53f
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/26/2022
ms.locfileid: "8489059"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>仕入先コードが特定の製品および日付に対して承認されていない場合

エラーコード: SYP4881415

## <a name="symptoms"></a>現象

計画オーダーを確定する、または発注書に明細行を追加しようとする際に、次のエラー メッセージが表示されます:

> 仕入先コード %1 は、%3 の %2 に対して承認されていません。

## <a name="cause"></a>原因

**承認仕入先チェック メソッド** フィールドが指定された製品に対して *警告のみ* または *許可しない* に設定され、仕入先には現在その製品を供給する権限がないためです。

## <a name="resolution"></a>解決策

この問題を解決するには、関連する製品の仕入先チェックを無効にするか、仕入先を承認します。

製品の仕入先チェックを無効にするには、次の手順を実行します。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 関連する製品を開きます。
1. **購買** クイック タブで、**承認仕入先チェック メソッド** フィールドを *警告のみ* または *許可しない* 以外の値に設定します。

製品の仕入先を承認するには、次の手順を実行します。

1. **製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。
1. 関連する品目を開きます。
1. アクション ウィンドウの、**購買** タブの、**承認仕入先** グループで、**設定** を選択します。
1. **承認仕入先** リスト ページで、行をグリッドに追加し、それに対して次の値を設定します:

    - **仕入先** – 現在の製品を承認する仕入先を選択します。
    - **有効日** – 仕入先が承認される最初の日付を選択します。
    - **有効期限** – 仕入先が承認されている最後の日付を選択します。

詳細については、[特定の製品に対する仕入先の承認](../../procurement/tasks/approve-vendors-specific-products.md)を参照してください。

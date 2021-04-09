---
title: バッチ追跡品目の処理の改善
description: このトピックでは、明細書転記プロセス時のバッチ追跡品目のバッチの処理に対して行われた改善について説明します。
author: josaw1
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 2453ed711d47e062c82d3888ff471b770b5bb2ef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799712"
---
# <a name="improved-handling-of-batch-tracked-items"></a>バッチ追跡品目の処理の改善


[!include [banner](includes/banner.md)]


販売時点管理 (POS) では、バッチ追跡品目のバッチ番号を販売時に取得することはできません。 ただし、特定の構成では、顧客の注文または明細書の転記を通じて販売が本社に転記されるとき、Microsoft Dynamics システムは、バッチ追跡品目に対して有効なバッチ番号が存在することと、請求プロセスで有効なバッチ番号が使用されることを想定しています。

製品に対して有効なバッチ番号が存在する場合は、顧客注文の請求プロセスと、明細書の転記からの販売注文請求プロセスでそのバッチ番号が使用されます。 それ以外の場合、顧客注文請求プロセスは転記できず、POS ユーザーにはエラー メッセージが表示されます。 その結果、明細書を転記しようとするとエラー状態になります。 このエラー状態は、製品のマイナス在庫が有効になっていても発生します。

Retail バージョン 10.0.4 以降で行われた改善では、バッチ追跡品目に対してマイナス在庫が有効になっているとき、在庫が 0 (ゼロ) であるか、またはバッチ番号が使用できない場合、明細書の転記を通じた顧客注文の請求と販売注文の請求がブロックされないことが保証されます。 この新しい機能では、バッチ番号が使用できないとき、販売明細行の既定のバッチ ID が使用されます。

顧客注文に使用される既定のバッチ ID を定義するには、**コマース パラメーター** ページの **顧客注文** タブの **注文** クイック タブで、**既定のバッチ ID** フィールドを設定します。

明細書の転記を通じた販売注文の請求に使用される既定のバッチ ID を定義するには、**コマース パラメーター** ページの **転記** タブの **在庫更新** クイック タブで、**既定のバッチ ID** フィールドを設定します。

> [!NOTE]
> この機能は、特定の店舗倉庫および品目に対して高度な倉庫管理が有効になっている場合にのみ使用できます。 後のリリースでは、この機能は、高度な倉庫管理が使用されていない場合にもサポートされます。

> [!NOTE]
> 倉庫管理が複雑でない場合、明細書を転記する際にバッチ追跡項目の処理を改善するためのサポートが Retail バージョン 10.0.5 に導入されました。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
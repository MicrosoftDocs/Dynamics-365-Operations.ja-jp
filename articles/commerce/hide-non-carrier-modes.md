---
title: POS の出荷オプションから配送業者以外の配送モードを非表示にする
description: この記事では、販売時点管理 (POS) アプリケーションで出荷注文が作成された際、配送業者以外の配送モードが選択に表示されないようにする構成オプションについて説明します。
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 469e6ebb8afed26a6bf25f4c9c3ab8f7f4ac78ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897008"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>POS の出荷オプションから配送業者以外の配送モードを非表示にする


[!include [banner](includes/banner.md)]

この記事では、販売時点管理 (POS) アプリケーションで使用可能な構成オプションについて説明します。 この構成オプションにより、POS で出荷注文が作成された際の配送モードの選択動作が変更されます。

POS で顧客の出荷注文を作成する際、出荷の配送モードを選択できます。 この機能は、注文全体が出荷されているか、選択された明細行のみであるかにかかわらず使用可能です。

既定では、配送モードが選択されたダイアログ ボックスには、チャネル、品目、および配送先住所の組み合わせに対する有効な配送モードがすべて表示されます。 これらの配送モードは、**配送モード** ページの Headquarters (**販売とマーケティング \> 設定 \> 配送 \> 配送モード**) で定義されます。 「配送業者以外」の配送モード、たとえば **Carryout** や **Pickup** などは、ダイアログ ボックスでの選択のために表示されることがあります。

ただし、このダイアログ ボックスには、配送業者以外の配送モードを隠すことができる機能が追加されています。 この機能を有効にするには、**Commerce パラメーター** ページの、**顧客注文** タブで、**出荷注文に対する配送モードのみを表示** オプションを **はい** に設定します。 この機能を有効にして、情報をチャネル データベースに同期するための適切な配送ジョブを実行した後は、POS での出荷順序の作成プロセス中に、配送業者以外の配送モードは表示されないようになります。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
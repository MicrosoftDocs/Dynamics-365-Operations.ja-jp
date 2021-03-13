---
title: POS の出荷オプションから配送業者以外の配送モードを非表示にする
description: このトピックでは、販売時点管理 (POS) アプリケーションで出荷注文が作成された際、配送業者以外の配送モードが選択に表示されないようにする構成オプションについて説明します。
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: fcacb4243e78607d19d2c57aff5debe04d85d6f2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009724"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>POS の出荷オプションから配送業者以外の配送モードを非表示にする


[!include [banner](includes/banner.md)]

このトピックでは、販売時点管理 (POS) アプリケーションで使用可能な構成オプションについて説明します。 この構成オプションにより、POS で出荷注文が作成された際の配送モードの選択動作が変更されます。

POS で顧客の出荷注文を作成する際、出荷の配送モードを選択できます。 この機能は、注文全体が出荷されているか、選択された明細行のみであるかにかかわらず使用可能です。

既定では、配送モードが選択されたダイアログ ボックスには、チャネル、品目、および配送先住所の組み合わせに対する有効な配送モードがすべて表示されます。 これらの配送モードは、**配送モード** ページの Headquarters (**販売とマーケティング \> 設定 \> 配送 \> 配送モード**) で定義されます。 「配送業者以外」の配送モード、たとえば **Carryout** や **Pickup** などは、ダイアログ ボックスでの選択のために表示されることがあります。

ただし、このダイアログ ボックスには、配送業者以外の配送モードを隠すことができる機能が追加されています。 この機能を有効にするには、**Commerce パラメーター** ページの、**顧客注文** タブで、**出荷注文に対する配送モードのみを表示** オプションを **はい** に設定します。 この機能を有効にして、情報をチャネル データベースに同期するための適切な配送ジョブを実行した後は、POS での出荷順序の作成プロセス中に、配送業者以外の配送モードは表示されないようになります。

---
title: 廃棄コードの設定
description: この手順では、返品注文の受信プロセスでモバイル デバイスで使用できる廃棄コードの設定を中心に説明します。
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSDispositionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c98526423b28fcb6c4e00a9f2cfd84d5a9119e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977016"
---
# <a name="set-up-dispositions-codes"></a>廃棄コードの設定

[!include [banner](../../includes/banner.md)]

この手順では、返品注文の受信プロセスでモバイル デバイスで使用できる廃棄コードの設定を中心に説明します。 廃棄コードは、品目を受け取るときに使用できるルールのコレクションです。 たとえば、作業ユーザーがモバイル デバイスを使用して破損した品目を受け取る場合に、そのユーザーは破損した品目の廃棄コードをスキャンする必要があります。 受入済の商品の在庫状態、作業テンプレート、および場所のディレクティブは、スキャンした廃棄コードから決定することができます。 発注書の入荷プロセスおよび完了したプロセスの製造オーダー レポートでは、廃棄コードの使用はオプションです。 販売注文の返品入庫プロセスでは、品目がモバイル デバイスを使用して登録されている場合、廃棄コードの使用は必須です。  このガイドは、デモ データの会社 USMF を使用して作成されました。 この手順は、倉庫マネージャーを対象としています。 

1. [倉庫管理] > [設定] > [モバイル デバイス] > [廃棄コード] の順に移動します。
2. [新規] をクリックします。
    * 顧客からの返品に使用する新しい廃棄コードを作成します。  
3. [廃棄コード] フィールドに値を入力します。
4. [在庫状態] フィールドで、在庫ブロックのある在庫状態を選択します。
    * USMF を使用している場合は、[ブロック] を選択します。 注文明細行の既定のステータスをオーバーライドする場合は、廃棄コードに在庫状態を追加できます。  
5. [作業テンプレート] フィールドに値を入力します。
    * オプション: 返品注文に関連付けられる作業テンプレート コードを選択します。 値が入力されていない場合は、作業テンプレートは、システムでコンフィギュレーションされた標準のルールを使用して解決されます。 作業テンプレートを選択すると、この廃棄コードを使用できるプロセスが制限されます。 たとえば、廃棄コードが、発注書のワーク オーダー タイプを持つ作業テンプレートを含む場合、顧客からの返品された品目の登録に使用することはできません。  
6. [返品廃棄コード] フィールドに値を入力します。
    * 返品廃棄コードにより、登録された品目の返品注文プロセスの残りが決まります。 この例では、顧客は貸方票を受け取る必要があります。 アクションの貸方を含む返品廃棄コードを追加します。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
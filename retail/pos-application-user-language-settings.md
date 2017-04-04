---
title: "POSアプリケーションとユーザー言語設定"
description: "このトピックでは、Retail POSの現代 (MPOS) での言語設定を変更するPOS.を曇らせる方法について説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmWorker, RetailStoreTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78891
ms.assetid: 0030940c-e0a5-4345-9511-8c3bd1f487ad
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf5b75572529bb497d3079752de187f30aa59294
ms.lasthandoff: 03/31/2017


---

# <a name="pos-application-and-user-language-settings"></a>POSアプリケーションとユーザー言語設定

このトピックでは、Retail POSの現代 (MPOS) での言語設定を変更するPOS.を曇らせる方法について説明します。

<a name="overview"></a>概要
========

言語設定と変換は、店舗とユーザーの設定によって異なる場合により、Retail POSの現代) (MPOSおよびクラウドPOSサポート環境。 たとえば、店舗は英語が顧客に対して共通であっても、複数の労働災害は、フランスの変換を持つアプリケーションを使用するには、以下地域で検索できます。

## <a name="data-language"></a>データ言語
ユーザーの設定に関係なく、MPOSおよびクラウドPOSによって、データに使用する変換を決定する、店舗の言語設定を常に使用します。 これは、すべてのユーザーは、顧客に一貫性経験があることを確認します。  データの例は次のとおりです。:

-   製品
-   属性と値
-   カテゴリ名
-   印刷または電子メール送信されたトランザクション受領書
-   支払方法名
-   ライン ディスプレイ メッセージ

店舗の言語は、主要なPOSのログイン画面のユーザーがログオンする前に不明であるため、使用されます。 変換を店舗の言語に使用できない場合は、POSは、会社の言語に戻ります。

### <a name="configuring-the-stores-language-setting"></a>店舗の言語設定のコンフィギュレーション

店舗の言語設定は**では**から**すべての小売店舗Retail Store **]ページで、**一般的な地域の設定の &gt; 言語に &gt; 設定されます。 **各店舗の言語を選択している場合でも、ドロップを使用します。

## <a name="user-interface-language"></a>ユーザー インターフェイス言語
POSユーザーの言語設定は、アプリケーションのユーザー インターフェイスで使用される換算が決まります。 これは、データとしては考慮されないすべてのラベル、メニュー、およびを示します。 一つの例外がPOSボタン グリッドに表示されるテキストです。 ボタン グリッドは、換算はサポートされません。したがって、ボタンの定義にテキストを常に示します。 サポートするには、ボタンに変更し、コピーし、別のボタン グリッドを管理し、必要に応じてユーザーに割り当てる必要があります。

### <a name="configuring-the-users-language-setting"></a>ユーザーの言語設定のコンフィギュレーション

POSユーザーの言語設定は** **ワーカー**ページでは設定されています**から**すべての小売ための &gt; 言語**。  これは、主要なプロファイル]タブで設定されていない。  この設定は、POS.で使用されません。 ユーザーの言語が設定されていないか、翻訳が使用できない言語に設定されている場合、POSは店舗の言語に戻ります。  

|             |                            |                                                                   |
|-------------|----------------------------|-------------------------------------------------------------------|
| ** **       | ** UIの言語** ** **      | [**データ言語 (製品、受領書フォーマット、ライン ディスプレイなど)**] |
| **会社** | 既定                    | 既定                                                           |
| **店舗**   | 会社を上書き          | 会社を上書き                                                 |
| **User**    | 店舗又は会社を上書き | なし                                                             |





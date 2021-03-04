---
title: 政府助成金の圧縮記帳ドキュメントの作成および割り当て
description: 日本では、圧縮記帳ドキュメントとは、政府助成金によって支援された固定資産に添えるドキュメントのことです。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetReductionEntryProfile_JP, AssetTable, AssetBook
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e698bdc8feb584a1e4f56257307064d0eda03a28
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408199"
---
# <a name="create-and-assign-a-reduction-entry-document-for-a-government-grant-subsidy"></a>政府助成金の圧縮記帳ドキュメントの作成および割り当て

[!include [banner](../../includes/banner.md)]

日本では、圧縮記帳ドキュメントとは、政府助成金によって支援された固定資産に添えるドキュメントのことです。 圧縮記帳の証明書には、圧縮記帳メソッド、減価償却の方法、理由、有効性、補助金のしきい値など、政府補助金に関する詳細が含まれています。



圧縮記帳ドキュメントの詳細は、圧縮記帳金額を計算および転記するのに使用されます。



このタスクを使用して、圧縮記帳ドキュメントの作成方法および固定資産への適用方法を把握します。



このタスクを完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順では、JPMF デモ会社のデータを使用します。


## <a name="create-a-new-reduction-entry-document"></a>新しい圧縮記帳ドキュメントの作成
1. [固定資産] > [定期処理タスク] > [圧縮記帳] > [圧縮記帳の文書] の順に移動します。
2. [新規] をクリックします。
3. [圧縮記帳] フィールドに値を入力します。
4. [圧縮記帳のタイプ] フィールドで、オプションを選択します。
    * 政府助成金の仕訳入力方法を選択します。  
5. [減価償却方法] フィールドで、オプションを選択します。
    * このフィールドは、[圧縮記帳のタイプ] フィールドで [積立金方式] を選択した場合にのみ使用できます。     減価償却方法は、固定資産に使用する方法と同じにする必要があります。  
    * 助成金の原因、失効日、政府助成金最高額の最大レートなどの追加情報を記録することができます。  
    * [助成金の償却] タブで、固定資産の償却およびそれに関連する助成金について政府から要求された条件を入力できます。 この情報は、固定資産を廃棄するかどうか、または廃棄する場合にその時期はいつかを知りたいときに参照されます。  
6. [保存] をクリックします。

## <a name="assign-the-reduction-entry-document-to-a-fixed-asset-book"></a>固定資産帳簿への圧縮記帳ドキュメントの割り当て
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. [新規] をクリックします。
    * 支援された資産がシステムに既に入力されている場合、既存の固定資産の編集を選択することもできます。  
3. [固定資産グループ] フィールドに値を入力します。
4. [帳簿] をクリックします。
5. クイック フィルターを使用して、目的の帳簿を除外します。
6. [圧縮記帳] フィールドに値を入力します。
7. ドキュメントの日付を入力します。
8. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
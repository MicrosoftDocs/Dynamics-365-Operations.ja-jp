---
title: ER コンフィギュレーション先
description: この手順では、フォルダーまたはファイルなどの電子申告 (ER) の出力コンポーネントにさまざまな出力先を設定して使用する方法を示します。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
ms.openlocfilehash: 3c8d03e9783013183fbe76cb36014fa9e1e1cbed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291057"
---
# <a name="er-configure-destinations"></a>ER コンフィギュレーション先

[!include [banner](../../includes/banner.md)]

この手順では、フォルダーまたはファイルなどの電子申告 (ER) の出力コンポーネントにさまざまな出力先を設定して使用する方法を示します。 この手順の作成に使用するデモ データの会社は DEMF です。 ドイツが法人の第一の住所が所在する国/地域となっていますが、この手順ではあらゆる法人を使用できます。 

この例で使用する形式は ISO20022 債権移動ですが、既にインポートした形式であればどんな形式でも使用できます。 この手順は 1 つのファイルと1つの出力先からなる設定の例であることに注意してください。 電子申告の送信先管理に関する詳細については、Dynamics 365 Finance のヘルプで確認できます。

1. [組織管理] > [電子申告] > [電子申告の送信先] に選択します。
2. 形式の送信先のための新しいセットを作成するには、[新規] をクリックします。
3. [参照] フィールドで、送信先をコンフィギュレーションする形式を選択します。
    * 選択する値がない場合、電子申告の形式のコンフィギュレーションをインポートしていないことを意味します。 出力先を設定する前に、形式のコンフィギュレーションをインポートする必要があります。  
4. 新しいファイルの送信先を作成するには、[新規] をクリックします。
    * フォルダーまたはファイルなどの同じ形式の各生産コンポーネントに対して 1 つのファイル出力先を作成できることに注意してください。 設定で出力先を個別に有効または無効にすることができます。  
5. [名称] フィールドで、出力コンポーネントのわかりやすい名称を入力します。
    * 「支払ファイル」や「管理レポート」などわかりやすい名前を使用することをお勧めします。 これらの名前は、出力先の設定とともにコンフィギュレーション ランタイムでユーザーに表示されます。  
6. ファイル名で、形式固有のファイルまたはフォルダーを選択します。
7. [設定] をクリックします。
8. [有効] フィールドで、[はい] を選択します。
    * 各タブの [有効] のチェック ボックスで、各出力先を個別に有効または無効にできます。 この例では、ファイル生成時にメール受信者への出力ファイルの送信を有効にします。  
9. [編集] をクリックし、電子メールの受信者を設定します。
10. [追加] をクリックします。
11. [管理電子メールの印刷] をクリックします。
12. [電子メール ソース ] フィールドで、オプションを選択します。
    * 顧客または仕入先のタイプなど、さまざまな電子メールのソース タイプを選択できます。 これは、電子メール ソースの式によって返される引数のタイプを示します。 次の手順で説明する電子メール ソースの式は、電子メール ソースをバインドします。 式が仕入先を返す場合、[仕入先] を選択します。 ISO 20022 の口座振替のコンフィギュレーションの例を使用している場合、[仕入先] を使用します。  
13. [電子メール ソースをバインドする] ボタンをクリックします。
14. 式で、前に選択した関係者タイプにドキュメント固有の参照を入力します。
    * 入力する代わりに、関係者の口座を表すデータ ソース ノードを検索できます。また [データ ソースの追加] ボタンをクリックして、式を更新することができます。 たとえば、ISO 20022 の債権移動コンフィギュレーションを使用する場合、仕入先口座を表すノードは、'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID となります。 それ以外の場合は、「DE-001」など任意の文字列型の値を入力して式を保存します。  
15. [保存] をクリックします。
16. ページを閉じます。
17. 「編集して関係者の連絡先情報を環境設定する」をクリックします。
18. [一次的連絡先] フィールドで、[はい] を選択します。
    * 各種のオプションを使用して、関係者のどのタイプの連絡先をメール アドレスとして使用するかを決定します。 この例では、一次的連絡先 を使用します。  
19. [OK] をクリックします。
20. [OK] をクリックします。
21. [件名] フィールドに値を入力します。
22. [OK] をクリックします。



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

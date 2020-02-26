---
title: ER 電子メール送信先のタイプ
description: このトピックでは、送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、電子メール送信先をコンフィギュレーションする方法に関する情報を提供します。
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019866"
---
# <a name="EmailDestinationType">電子メールの送信先</a>

[!include [banner](../includes/banner.md)]

送信ドキュメントを生成するようにコンフィギュレーションされている電子申告 (ER) 形式の各フォルダーまたはファイル コンポーネントに対して、電子メール送信先をコンフィギュレーションできます。 送信先の設定に基づいて、生成されたドキュメントは電子メールの添付ファイルとして配信されます。

**有効** を **はい** に設定し、出力ファイルを電子メールで送信します。 このオプションを有効にすると、電子メールの受信者を指定して、電子メールの件名および本文を編集できます。 電子メールの件名および本文の定型文を設定したり、ER [フォーミュラ](er-formula-language.md) を使用して電子メールのテキストを動的に作成したりできます。 

2 つの方法で ER の電子メール アドレスを構成できます。 コンフィギュレーションは、印刷管理機能で完了したのと同じ方法で完了することができ、またフォーミュラを介した ER コンフィギュレーションへの直接参照を使用して電子メールアドレスを解決することもできます。

[![電子メール送信先の有効化](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)

## <a name="email-address-types"></a>電子メール アドレス タイプ

**To** や **Cc** フィールドで**編集**を選択すると、**電子メールの送信先**ダイアログ ボックスが表示されます。 使用する電子メール アドレス タイプを選択できます。 現在、**コンフィギュレーション電子メール**および**印刷管理**電子メールのタイプがサポートされています。

[![電子メールのタイプの選択](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)

### <a name="print-management"></a>印刷管理

**印刷管理電子メール** タイプを選択する場合、**To** フィールドに固定の電子メール アドレスを入力できます。 

[![固定電子メール アドレスの構成](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)

固定されていない電子メール アドレスを使用するには、ファイルの送信先の電子メール ソース タイプを選択する必要があります。 **顧客**、**仕入先**、**見込顧客**、**連絡先**、**競合他社**、**作業者**、**申請者**、**見込み仕入先**、**不許可仕入先**の値がサポートされます。 電子メール ソース タイプを選択したら、**電子メール ソース** フィールドの横のボタンを使用して、**フォーミュラ デザイナー** フォームを開きます。 このフォームを使用して、実行時に処理されたドキュメントから選択されたソース タイプ フォームの**関係者のアカウント**を返すフォーミュラを電子メールの送信先に関連付けることができます。

[![電子メールのソース アカウントのコンフィギュレーション](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)

フォーミュラは ER コンフィギュレーションに固有です。 **フォーミュラ** フィールドで、顧客または仕入先の関係者タイプにドキュメント固有の参照を入力します。 入力せずに、顧客または仕入先を表すデータ ソース ノードを検索でき、フォーミュラを更新するには**データ ソースの追加**ボタンを選択します。 たとえば、**ISO 20022 の口座振替**のコンフィギュレーションを使用する場合、仕入先を表すノードは、`'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID` です。

`"DE-001"` などの文字列値を入力し、フォーミュラを保存した場合、仕入先 **DE-001** の連絡担当者に電子メールが送信されます。


[![ER フォーミュラ デザイナー ページ](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)

[![電子メールのソース アカウントのコンフィギュレーション](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)



### <a name="configuration-email"></a>コンフィギュレーション電子メール

使用するコンフィギュレーションが**電子メール アドレス**を返すデータ ソースにノードを持つ場合にこの電子メール タイプを使用します。 フォーミュラ デザイナーでデータ ソースと機能を使用して、正しく書式設定された電子メール アドレスを取得できます。 たとえば、**ISO 20022 の口座振替**のコンフィギュレーションを使用する場合、仕入先の連絡先担当者の電子メールアドレスを表すノードは、`'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email` です。

[![電子メール アドレス ソースのコンフィギュレーション](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)

## <a name="additional-resources"></a>追加リソース

- [電子申告 (ER) の概要](general-electronic-reporting.md)
- [電子申告 (ER) の送信先](electronic-reporting-destinations.md)
- [電子申告 (ER) のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md)

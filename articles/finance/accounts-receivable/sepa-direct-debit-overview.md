---
title: SEPA の口座引落の概要
description: この記事では、欧州委員会が設定する単一ユーロ支払地域 (SEPA) に関する情報について説明します。
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, CustBankAccounts, CustParameters, CustTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "11144"
- intro-internal
ms.assetid: 3277c9b6-e46e-40c9-aa76-9b0449467842
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d63cac6c21ec5c5340204f409648516047bb94d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909159"
---
# <a name="sepa-direct-debit-overview"></a>SEPA の口座引落の概要

[!include [banner](../includes/banner.md)]

単一ユーロ支払地域 (SEPA) は欧州委員会によって設定され、個人、事業または組織および銀行がどの国または地域にあるかに関係なく、すべての電子支払は国内と見なされます。 国内支払と国境を越えた支払の間に違いはありません。 SEPA には、28 の欧州連合 (EU) の加盟国とアイスランド、リヒテンシュタイン、ノルウェー、スイス、およびモナコとサンマリノが含まれます。 SEPA により、欧州経済領域 (EEA) 内の支払トランザクションの単一市場が形成されます。 最終的に、SEPA により、銀行、事業、および個人が扱う支払形式の数を減らすと予想されます。   

## <a name="what-is-the-goal-of-sepa-direct-debits"></a>SEPA の口座引落の目的は何ですか。

署名済み委任状が顧客によって債権者に許可された場合、SEPA の口座引落により、債権者は顧客の銀行口座から資金を回収することができます。 顧客は債権者が支払を回収することを承認する委任状に署名し、顧客の銀行に支払の回収を指示します。 

SEPA 口座引落は、SEPA の 32 の国/地域内で国内および国境を越えたユーロ口座引落に使用できるはじめての支払手段です。 

2 つのスキームを使用できます: SEPA Core 口座引落スキームおよび SEPA 企業間 (B2B) 口座引落スキーム。 スキームは両方とも同じファイル形式を使用します。

## <a name="what-is-the-core-direct-debit-scheme"></a>Core 口座引落スキームとは何ですか。
SEPA Core 口座引落スキームは、基本スキームです。 次の属性があります。
-   資金の振替はユーロです (銀行口座に他の通貨の資金が含まれる場合でも)。
-   顧客および債権者は、SEPA 内にある信用機関の口座を保有している必要があります。
-   顧客が債権者に署名済委任状を付与する必要があります。
-   委任状は、最後の回収が開始されてから 36 か月後に有効期限が切れます。
-   債権者は、委任状が有効の間また最後の回収の後の少なくとも 14 か月間は、委任状を保管しておく必要があります。
-   スキームは、単一 (一回) または定期的な口座引落回収に使用する場合があります。
-   顧客には、自分の口座から引き落とされてから 8 週間まで、"何の質問もなしに" 払戻しを受ける権利があります。

## <a name="what-is-the-sepa-business-to-business-b2b-direct-debit-scheme"></a>SEPA 企業間 (B2B) 口座引落スキームとは何ですか。
SEPA B2B 口座引落スキームは、企業間のトランザクションに適用され、SEPA Core 口座引落スキーム上に構築されます。 主な違いは次のとおりです。
-   SEPA B2B 口座引落スキームは、顧客が一私人 (消費者) の場合は使用できません。
-   顧客には、承認されたトランザクションの払戻を取得する権利がありません。
-   顧客銀行は、委任状の情報に対して回収を確認して、その回収が承認されたことを確認する必要があります。 顧客銀行と顧客は、口座引落ごとに実行される検証に同意する必要があります。
-   このスキームでは、口座引落を提示するタイムラインが短縮され、返品期間が減少します。

## <a name="can-i-use-the-cor1-scheme-for-direct-debit-mandates"></a>口座引落手順については COR1 スキームを使用することもできますか。
はい。 オーストリア、ベルギー、ドイツ、フランス、イタリア、スペイン、およびオランダにおける SEPA 口座引落の委任状については COR1 スキームを使用できます。 スキームでは、債権者の口座引落コレクションのための、より短い事前通知期間が用意されています。

## <a name="what-are-international-bank-account-numbers-iban-and-bank-identifier-codes-bic"></a>国際銀行番号 (IBAN) および金融機関識別コード (BIC) とは何ですか。
国際銀行番号が (IBAN) および銀行識別コード (BIC) は SEPA の 32 の国/地域の口座を識別するために使用されます。 SWIFT コード フィールドに BIC を入力し、IBAN フィールドに IBAN を入力します。 両方のフィールドは、銀行口座のページにある [銀行口座] タブの [追加 ID] クイック タブにあります。 これは債権者の銀行口座および顧客の銀行口座の両方に当てはまります。

## <a name="where-do-i-enter-creditor-identifiers-direct-debit-ids"></a>どこで債権者の識別子 (口座引落 ID) を入力しますか。
SEPA では、各債権者は固有の債権者識別子で識別されます。 この識別子により、顧客および顧客銀行は各口座引落をフィルター処理でき、顧客の指示によって、口座取引を処理または拒否できます。 債権者が自分の銀行を通じてこの識別子を要求する必要があります。 法人の銀行口座の [口座引落 ID] フィールドにこの識別子を入力します。

## <a name="what-are-mandates"></a>委任状とは何ですか。
顧客は債権者が支払を回収することを承認する委任状に署名し、顧客の銀行に支払の回収を指示します。 顧客は、用紙フォームでまたは電子的に委任状を発行できます。 既定では、委任状は、口座引落が最後に開始されてから 36 か月に有効期限が切れます。

## <a name="where-do-i-specify-the-sepa-direct-debit-file-format-iso-20022"></a>SEPA 口座引落ファイル形式 (ISO 20022) をどこで指定しますか。
SEPA のデータ形式は、ISO 20022 のメッセージの標準に基づきます。 [一般的な電子申告] チェック ボックスをオンにし、支払の売掛金勘定の方法をコンフィギュレーションするときにエクスポート形式のコンフィギュレーションとして SEPA 口座振替形式を選択します。 顧客支払仕訳帳の支払ファイルを生成すると、その支払方法を使用します。

## <a name="in-what-file-formats-can-i-generate-sepa-direct-debit-payment-files"></a>どのファイル形式で SEPA 口座引落支払ファイルを生成できますか。
SEPA 口座引落用の電子支払ファイルを次の形式で生成します。
-   ベルギー、ドイツ、スペイン、フランス、イタリア、オランダの PAIN.008.001.02 XML ファイル形式で SEPA 口座引落支払ファイルを生成できます。
-   SEPA 口座引落支払はオーストリアの PAIN.008.001.02 XML ファイル形式とドイツの PAIN.008.003.02 XML ファイル形式でファイルします。

## <a name="how-do-refunds-and-returns-work-with-sepa-direct-debits"></a>払戻および返品は SEPA 口座引落ではどのように扱われますか。
両方の SEPA 口座引落のスキームで、顧客には払戻の一定の権利があります。 顧客は、理由を与えずに、期日から 8 週間の間に承認されたトランザクションを取り消すことができます。 無許可のトランザクションの場合、期間は期日から 13 か月に延長されます。 [顧客トランザクション] ページの [支払いのキャンセル] ボタンを使用して、既に支払われたどんな支払でも手動で取り消すことができます。







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: 確認後支払ファイルの設定と生成
description: このトピックでは、確認後支払を設定し、確認後支払ファイルを生成する方法を説明します。
author: abruer
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: a5579eae5117a7a3ca517bbcc235c2ed2d925d7f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512364"
---
# <a name="set-up-and-generate-positive-pay-files"></a>確認後支払ファイルの設定と生成

[!include [banner](../includes/banner.md)]

このトピックでは、確認後支払を設定し、確認後支払ファイルを生成する方法を説明します。 

確認後支払を設定し、銀行に渡す小切手の電子リストを生成します。 次に、小切手が銀行に提出されたら、銀行はそれを小切手リストと比較します。 小切手がリストの小切手と一致する場合、銀行は小切手を決済します。 小切手がリスト内の小切手と一致しない場合、銀行は確認のために小切手を保留にします。

## <a name="security-for-positive-pay-files"></a>確認後支払ファイルのセキュリティ
確認後支払ファイルには、受取人と小切手金額に関する機密情報が含まれている場合があります。 したがって、ファイルを生成時から銀行がそのファイルを受領するまで、適切なセキュリティ対策をかならず使用します。 確認後支払ファイルは、Web ブラウザで指定した場所にダウンロードされます。 確認後支払ファイルには機密情報が含まれている場合があるので、承認されたユーザーのみが、Microsoft Dynamics 365 for Finance and Operations 内のこの情報を生成および表示するためのアクセス権限を持つことが重要です。 次の表を活用すれば、必要な権限を判断するのに役立ちます。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>タスク</th>
<th>権限</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>確認後支払ファイルを<strong>銀行口座</strong>リスト ページあるいは<strong>銀行口座</strong>ページから生成します。</td>
<td><ul>
<li><strong>銀行の確認後支払情報の管理</strong>(BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong>(BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>確認後支払ファイルを生成</strong> ページから複数の法人と銀行口座の確認後支払ファイルを生成します。</td>
<td><ul>
<li><strong>銀行の確認後支払情報の管理</strong>(BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong>(BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>確認後支払ファイルの概要</strong> ページで確認後支払ファイルを表示します。</td>
<td><strong>複数の法人に関する銀行確認後支払情報の表示</strong>(BankPositivePayView)</td>
</tr>
<tr class="even">
<td><strong>確認後支払ファイルの概要</strong> ページで銀行の確認後支払ファイルを確認します。</td>
<td><strong>確認後支払ファイルの確認</strong>(BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td><strong>確認後支払ファイルの概要</strong> ページで銀行の確認後支払ファイルを取り消します。</td>
<td><strong>確認後支払ファイルの取り消し</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>確認後支払形式の設定
確認後支払ファイルは、データ エンティティを使用して作成されます。 確認後支払ファイルを生成する前に、小切手情報を銀行と通信できる形式に変換するのに使用する変換入力形式を設定する必要があります。 **確認後支払形式** ページで、ファイル形式の ID と説明を作成できます。 変換入力形式は、XML タイプにする必要があります。 特定の形式は、使用している変換ファイルによって異なります。 たとえば、サンプル XSLT (Extensible Stylesheet Language Transformations) ファイルは**XML-Element**形式を使用するよう指定されています。 **変換に使用されるファイルのアップロード** アクションを使用して、銀行が必要な形式の変換ファイルの場所を指定します。

## <a name="example-xslt-file-for-positive-pay-file"></a>例: 確認後支払ファイル用 XSLT ファイル
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>銀行口座への確認後支払形式の割り当て
確認後支払情報を生成する銀行口座ごとに、前のセクションで指定した確認後支払形式を割り当てる必要があります。 **銀行口座** ページで、銀行口座に対応する確認後支払形式を選択します。 **確認後の開始日** フィールドに、確認後支払ファイルを生成する最初の日付を入力します。 このフィールドに日付を入力することが重要です。 それ以外の場合は、生成する最初の確認後支払ファイルは、この銀行口座に対して作成されているすべての小切手が含まれます。

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>確認後支払ファイルの番号順序の割り当て
各確認後支払ファイルには固有の番号を付ける必要があります。 **現金及び銀行管理パラメーター** ページの **番号順序** タブを使用して確認後支払ファイルの番号順序を作成します。

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>一つの銀行口座に対する確認後支払ファイルの生成
一つの法人と一つの銀行口座に対する確認後支払ファイルを生成できます。 複数の法人と銀行口座の確認後支払ファイルを同時に生成する方法についての情報は、次のセクションを参照してください。 一つの法人と一つの銀行口座の確認後支払ファイルを生成するには、**銀行口座** ページから **確認後支払ファイルの生成** ダイアログ ボックスを開きます。 **締め日** フィールドで、確認後支払ファイルに含める最終確認日付を入力します。 この最終確認日付までに、確認後支払ファイルにまだ含まれていないすべての小切手がファイルに含まれます。

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>複数の銀行口座に対する確認後支払ファイルの生成
複数の銀行口座の確認後支払ファイルを生成するには、**確認後支払ファイルを生成** 定期処理タスクを使用します。 ファイルの確認後支払形式を選択し、すべての法人あるいは選択した法人に対してファイルを生成するかを指定します。 指定した確認後支払形式あるいは選択した銀行口座を使用するすべての銀行口座の確認後支払ファイルを生成することもできます。 **締め日** フィールドで、確認後支払ファイルに含める最終確認日付を入力します。 この最終確認日付までに、確認後支払ファイルにまだ含まれていないすべての小切手がファイルに含まれます。

## <a name="view-the-results-of-positive-pay-file-generation"></a>確認後支払ファイルの生成の結果を表示します。
確認後支払ファイルが生成された後、**確認後支払ファイルの概要** ページで結果を表示できます。 個々の小切手の詳細を表示するには、**確認後支払ファイル** 詳細ページを使用します。

## <a name="confirm-a-positive-pay-file"></a>確認後支払ファイルを確認する
確認後支払ファイルに記載されている小切手が支払われた後、銀行から確認番号を受け取ります。 その後、確認後支払ファイルを確認できます。 **確認後支払ファイルの概要** ページで、ステータスが **作成済み** になっている確認後支払ファイルを選択し、次に **確認入力** アクションを選択します。 確認後支払ファイルを確認する際、銀行から受け取った確認番号が記録されます。

## <a name="recall-a-positive-pay-file"></a>確認後支払ファイルの取り消し
確認後支払ファイルを変更する必要がある場合は、それを取り消すことができます。 **確認後支払ファイルの概要** ページで、ステータスが **作成済み** になっている確認後支払ファイルを選択し、次に **取り消し** アクションを選択します。 確認後支払ファイルの小切手ごとに、小切手が確認後支払ファイルに含まれているかどうかを示すフィールドがリセットされます。 その後、取り消した小切手を含む新しい確認後支払ファイルを作成できます。




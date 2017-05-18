---
title: "登録 ID"
description: "このトピックでは、登録 ID の設定と使用に関する情報を提供します。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DirPartTaxRegistrationSearch, LogisticsPostalAddress, TaxRegistrationLegislationTypes, TaxRegistrationType
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264824
ms.assetid: e86f0a35-be58-4ef5-b5ab-bcfc495eaa13
ms.search.region: Global
ms.author: vlru
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 712eb9ec22f4eea4a969a7bd23b7d3728b35772e
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="registration-ids"></a>登録 ID

[!include[banner](../includes/banner.md)]


このトピックでは、登録 ID の設定と使用に関する情報を提供します。

多くの国や地域には、登録番号または ID を記録するためのさまざまな規則と条件があります。 このトピックでは、異なる欧州諸国/地域の関係者に必要な設定の概要とサポートされる登録タイプの処理について説明します。 すべての国や地域には、それぞれの管轄で提供される登録番号に関連するさまざまな国固有の機能をサポートするための要件があります。 登録番号の例には、社会保障番号 (SSN)、連邦税 ID (TIN)、および欧州 VAT ID (EU VAT ID) などがあります。 この機能は、一部のヨーロッパ諸国の国別要件を考慮に入れ、すべての地域のすべての国に統一されたフレームワークを提供します。 次のセクションでは、登録 ID を設定して処理するために使用される情報の流れ全体について説明します。

## <a name="registration-type-creation"></a>登録タイプの作成
登録 ID を入力する前に、各関係者が対象となる登録番号のタイプごとに登録タイプを設定する必要があります。 [**組織管理**] &gt; [**グローバル アドレス帳**] &gt; [**登録タイプ**] &gt; [**登録タイプ**] ページに進み、異なる国/地域の仕入先、顧客、作業者、法人の登録タイプを作成して管理します。

|フィールド                 |説明      |
|------------------------------|----------------------------|                                                                           
| 氏名                | 登録タイプの名前。 |                                                                           
| 説明         | 登録タイプの説明。 |
| 国/地域      | 国/地域の固有 ID。|
| 税務署長殿       | 登録タイプに関連付けられる税務当局。|
| 次のものに制限       | なし、個人、組織の税登録タイプに適用する制限の種類。|
| 書式設定              | 登録タイプの検証フォーマット。|
| 更新可能      | 登録タイプに対する登録番号を入力した後で更新できる場合に定義します。|
| 固有              | 登録タイプの登録番号が他と重複しない場合に定義します。 |
| 主要国 | 当事者が特定の国で 1 つ以上の住所に関連付けられ、登録 ID がこれらの住所すべてに有効である場合、その国での基本住所を 1 つ指定する必要があります。 基本として 1 つの ID のみ登録できます。 国の住所の基本にのみ登録番号を入力できる場合に定義します。 |

## <a name="assign-a-registration-type-to-a-registration-category"></a>登録カテゴリへの登録タイプの割り当て
登録カテゴリは、税、関税、他の目的に関して特定の国/地域で使用するを許可された国/地域の登録 ID です。 このカテゴリは、特定の登録 ID (チェック ディジットなど含む) および異なるレポートに含まれる登録 ID の検証ルールを定義します。 [**組織管理**] &gt; [**グローバル アドレス帳**] &gt; [**登録タイプ**] &gt; [**登録カテゴリ**] のページを使用して、サポートされている登録カテゴリに特定の国の登録タイプを割り当てます。

| フィールド            | 説明|
|-----------------------|----------------|
| 登録タイプ     | 特定の国/地域での登録タイプ。|
| 次のものに制限         | 制限の種類は、なし、個人、組織の税登録タイプに適用されます。|
| 登録カテゴリ | 国で使用するために承認された固有の登録 ID。 AX7.1 カテゴリでのサポートの完全な一覧は以下のとおりです。 |

## <a name="enter-registration-ids-for-global-address-book-records"></a>グローバル アドレス帳レコードの登録 ID を入力します。
Microsoft Dynamics 365 for Operations のグローバル アドレス帳 (GAB) には、顧客、仕入先、連絡先、取引関係、法人の連結された住所情報が含まれます。 詳細については、「[グローバル アドレス帳の概要](/dynamics365/operations/organization-administration/overview-global-address-book)」を参照してください。 グローバル アドレス帳に格納されている関係者レコードは、1 つ以上の住所レコードを格納できます。 これらの住所は、請求または配送など、さまざまな目的で使用されます。 顧客、仕入先、作業者、法人の住所情報に対する登録 ID を設定できます。 登録 ID を入力する関係者 (法人、仕入先、顧客、作業者) レコードを検索し、関係者、法人、仕入先、顧客、作業者に関連するフォームでの**登録 ID** をクリックして、**アドレスの管理**ページを開きます。 [**税登録**] タブで、[**追加**] をクリックし、登録 ID に関する次の情報を入力します。

|フィールド                |説明                                                |
|---------------------|-----------------------------------------------------------|
| 登録タイプ   | 選択した国/地域での登録タイプ。     |
| 登録番号 | 当事者の登録 ID。                                |
| 説明         | 登録番号の説明。               |
| 項             | 登録番号に関する追加情報。 |
| 発行機関      | 登録番号を発行した機関。        |
| 発行日         | 登録番号の発行日。              |
| 開始           | 登録番号の有効日。           |
| 有効期限          | 登録番号の有効期限。          |

> [!NOTE]
> 法人、仕入先、顧客の課税控除番号は、VAT ID に関連して関係者に対して入力された登録 ID から選択できます。

## <a name="search-for-records-by-registration-id"></a>登録 ID ごとのレコードの検索
登録 ID に基づいた関係者レコードの検索が、関係者、法人、仕入先、顧客、および作業者に関連するフォームで使用できます。 [**登録 ID 検索**] をクリックして、**登録 ID 検索基準**ページを開きます。 検索基準を指定して [**検索**] をクリックします。 グローバル アドレス帳から選択されたレコードと関係者レコードに関連付けられているタイプがシステムによって表示されます。

## <a name="supported-registration-categories"></a>サポートされる登録カテゴリ
次の表に、Dynamics 365 for Operations でサポートされている登録タイプを示します。 登録 ID について Microsoft Dynamics AX 2012 のフィールドで使い慣れている場合、この表を使って Dynamics 365 for Operations の登録カテゴリにそれらのフィールドをマップします。

| Dynamics 365 for Operations の登録カテゴリ         |国/地域  | Dynamics AX 2012 の用語/フィールド|
|---------------------------------------------------------------|---------------------|---------------------------------|
| VAT                                                        | 欧州連合 (EU) のすべての国|  課税控除番号 (AX2012 R3 での法律タイプ TAX ID)|
| エンタープライズ ID (COID)                                          | ベルギー チェコ共和国 エストニア ハンガリー ラトビア リトアニア ポーランド スイス | 企業番号 (EnterpriseNumber) 登録番号 (RegNum\_W) 登録番号 (RegNum\_W) 登録番号 (RegNum\_W) 登録番号 (RegNum\_W) 企業コード (EnterpriseCode) 登録番号 (RegNum\_W) UID (AX2012 R3 での法律タイプ UID) |
| 支店 ID                                                     | ベルギー            | 支店番号 (BranchNumber)|
| Spisová značka (登録番号、発行機関、セクション) | チェコ共和国     | 挿入番号 (CommercialRegisterInsetNumber) 商業登記で維持 (CommercialRegister) 商業登記のセクション (CommercialRegisterSection)|
| 税関顧客 ID                                           | フィンランド | 税関顧客番号 (CustomsCustomerNumber\_FI)|
| INN                                                           | ロシア連邦| INN (AX2012 R3 での法律タイプ INN)|
| RRC                                                           | ロシア連邦| RRC (AX2012 R3 での法律タイプ RRC)|
| OKDP                                                          | ロシア連邦| OKDP (AX2012 R3 での法律タイプ OKDP)|
| OKPO                                                          | ロシア連邦| OKPO (AX2012 R3 での法律タイプ OKPO)|
| RCOAD                                                         | ロシア連邦| RCOAD (AX2012 R3 での法律タイプ RCOAD)|
| OGRN                                                          | ロシア連邦| OGRN (AX2012 R3 での法律タイプ OGRN) |
| SNILS                                                         | ロシア連邦| SNILS (AX2012 R3 での法律タイプ SNILS)|
| CIFTS                                                         | ロシア連邦| CIFTS (AX2012 R3 での法律タイプ CIFTS)|

必須の前提条件を含む登録 ID 処理の詳細については、Lifecycle Services (LCS) での VAT ID に関する次のタスク記録を参照してください。

-   VAT ID の設定
-   仕入先の VAT ID 登録
-    VAT ID を使用する関係者の検索






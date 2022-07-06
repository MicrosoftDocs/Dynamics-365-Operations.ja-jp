---
title: 当事者およびグローバル アドレス帳のトラブルシューティング
description: この記事では、二重書き込みの当事者の機能およびグローバル アドレス帳の機能に関する問題の修正に役立つトラブルシューティング情報を提供します。
author: RamaKrishnamoorthy
ms.date: 07/30/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2136952ba6e4eeb938fc24a4be426a5b4b52e49
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892878"
---
# <a name="party-and-global-address-book-troubleshooting"></a>当事者およびグローバル アドレス帳のトラブルシューティング

[!include [banner](../../includes/banner.md)]



この記事では、二重書き込みの当事者の機能およびグローバル アドレス帳の機能に関する問題の修正に役立つトラブルシューティング情報を提供します。

## <a name="verify-these-prerequisites"></a>これらの前提条件の確認

当事者およびグローバル アドレス帳機能を使用する前に、これらが正しく構成されていることを確認してください。

+ 統合キー。

    | マップ | 鍵用に使っています |
    |-----|------|
    | 口座 |  accountnumber [口座番号]<br>msdyn_company.cdm_companycode [会社 (会社コード)] |
    | 連絡 | msdyn_contactpersonid [口座番号/連絡担当者 ID]<br>msdyn_company.cdm_companycode [会社 (会社コード)] |
    | 顧客/仕入先の連絡先 | msdyn_contactforpartynumber [当事者番号の連絡先]<br>msdyn_associatedcompanyid.cdm_companycode [関連する会社 (会社コード)] |
    | 仕入先 | msdyn_vendoraccountnumber [仕入れ先口座番号]<br>msdyn_company.cdm_companycode [会社 (会社コード)]|

+ マップのバージョン。 詳細については、[当事者とグローバル アドレス帳](party-gab.md#setup)を参照してください。

## <a name="error-about-location-id-key-when-you-try-to-add-an-address"></a>住所を追加しようとする場合の場所 ID キーに関するエラー

財務と運用アプリや Microsoft Dataverse のアカウントまたは連絡先に住所を追加しようとする場合、次のようなエラー メッセージが表示される場合があります。

*エンティティ msdyn_partypostaladdresses へのデータの書き込みに失敗しました。DirPartyPostalAdlocationCDSEntity への書き込みに失敗し、次のエラー メッセージが表示されました。要求に失敗しました。ステータス コード BadRequest、CDS エラー コード: 0x80040265、応答メッセージ: プラグインでエラーが発生しました。場所 ID の属性値を持つレコードが既に存在します。エンティティ キーの場所 ID キーは固有の値がこの属性のセットに含まれている必要があります。一意の値を選択してやり直してください。*

この問題を修正するには、**アドレス** テーブルのキーが、次の表に示すように設定されている必要があります。

プロパティ | 先頭値
---|---
表示名 | 場所キー
氏名 | msdyn_locationkey
フィールド | msdn_locationid、parentid
状態 | 有効
システム ジョブ | (空白)

二重書き込み当事者およびグローバル アドレス帳ソリューションがインストールされていない場合、このテーブルのキーは **msdyn_locationid** フィールドに設定されます。 二重書き込みアプリケーション オーケストレーション ソリューションの最新バージョン (2.2.2.60 以降) をインストールします。 これにより、**アドレス** テーブルに作成された前のキーが置き換えられます。

## <a name="error-when-you-try-to-run-customers-vendors-or-contacts-v2-maps"></a>顧客、仕入先、または連絡先 V2 マップを実行しようとする場合のエラー

**顧客**、**仕入先**、または **連絡先 V2** マップを実行しようとする場合、次のエラー メッセージが表示される場合があります。

*顧客 V3 (アカウント): プロジェクトの検証に失敗しました。スキーマに出力先フィールド msdyn_billingaccount.accountnumber が見つかりません。スキーマに出力先フィールド msdyn_primarycontact.msyn_contactforpartynumber が見つかりません。*

Dataverse の **msdyn_company** テーブルで定義された複数のキーがあります。 二重書き込みでは、どのキーが統合キーとして適切かを判断できません。任意のキーが統合キーとしてランダムに割り当てられます。 この問題を修正するには、[当事者およびグローバル アドレス帳](party-gab.md#setup)の手順 8 の説明に従って、統合キーを手動で更新します 。 次に、テーブルのマッピングを更新します。 出力先フィールドが見つからないとのエラーは表示されなくなります。

## <a name="error-that-the-party-id-is-different-between-finance-and-operations-apps-and-dataverse"></a>財務と運用アプリと Dataverse との間で当事者 ID が異なるエラー

財務と運用アプリと Dataverse との間で、**顧客**、**仕入先**、または **連絡先 V2** マップの当事者 ID が異なっているというメッセージが表示される場合があります。

この問題を修正するには、[当事者およびグローバル アドレス帳](party-gab.md#setup)の手順 7 の説明に従って、マップの最新バージョンを使用します。

## <a name="errors-when-upgrading-dual-write-party-and-global-address-book-solutions"></a>二重書き込み当事者およびグローバル アドレス帳ソリューションをアップグレードする時のエラー

二重書き込み当事者およびグローバル アドレス帳ソリューションを 2.4.0155 からそれ以降のバージョンにアップグレードする場合、エラー メッセージが表示される場合があります。

当事者およびグローバル アドレス帳機能は、2021 年 1 月 と 2 月にプレビュー用にリリースされた時、二重書き込みオーケストレーション ソリューションの一部でした。 この機能は、顧客からのフィードバックに基づいて、別個のソリューションとして一般提供用にリリースされました。 この機能は、別個のソリューションとしてオプションで提供されます。 当事者およびグローバル アドレス帳機能を含む二重書き込みオーケストレーション ソリューションのプレビュー バージョンを使用している場合は、二重書き込みオーケストレーション ソリューションをアンインストールするか、Dataverse 環境をリセットして、最新のソリューションを取得する必要があります。

二重書き込み当事者およびグローバル アドレス帳ソリューションには、次のソリューションが含まれます。

+ **当事者** - 当事者、郵便番号、および電子アドレスのスキーマが含まれます。
+ **Dynamics365GABExtended** - **勘定**、**仕入先**、**連絡先**、当事者の **連絡先** 機能をサポートするために行うコードおよびスキーマの変更すべてが含まれます。 このサポートは **、Dynamics365FinanceExtended** および **Dynamics365SupplyChainExtended** ソリューションから分離されました。
+ **Dynamics365GABDualWriteEntityMaps** - グローバル アドレス帳機能に必要な二重書き込みマッピングの変更すべてが含まれます。
+ **Dynamics365GABParty_Anchor**

## <a name="error-when-you-try-to-create-a-new-contact-from-the-view-contact-form"></a>連絡先の表示フォームから新しい連絡先を作成しようとする場合のエラー

財務と運用アプリの **連絡先の表示** フォームから新しい連絡先を作成しようとする場合、次のエラー メッセージが表示される場合があります。

*エンティティ msdyn_contactforparties にデータを書き込めません。{000006057} 値を使用して msdyn_parties を参照できません。{000020} 値を使用して cdm_workers を参照できません。*

この問題を修正するには、**連絡先の追加** フォームを使用して **連絡先** レコードを作成します。

## <a name="error-when-you-try-to-update-a-contact"></a>連絡先を更新しようとする場合のエラー

財務と運用アプリの Dataverse 由来の連絡先を更新しようとする場合、次のようなエラー メッセージが表示される場合があります。

*エンティティ msdyn_contactforparties へのデータの書き込みに失敗しました。smmContactPersonV2Entity への書き込みに失敗し、次のエラー メッセージが表示されました。ステータス コード BadRequest および CDS エラー コード: 0x0 応答メッセージ: 入力パラメータの検証中にエラーが発生しました: Microsoft.OData.ODataException: リテラル「」を予測されるタイプ「Edm.Int32」に変換できません。*

この問題を修正するには、最新の二重書き込み当事者およびグローバル アドレス帳ソリューションをインストールします。 この問題は バージョン 3.0.0.26 で修正されました。

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>新規の顧客、仕入先、または連絡先を Dataverse に作成する場合のエラー

新規の顧客、仕入先、連絡先を Dataverse に作成しようとする場合、次のエラー メッセージが表示される場合があります。

*当事者のタイプを「DirOrdirization」から「DirPerson」に更新することはできません。代わりに、既存の当事者を削除し、その後、新しいタイプの挿入を実行する必要があります。*

この問題は、ユーザーが 1 つの財務と運用アプリを異なる Dataverse 組織に接続しようとする場合、または既存の Dataverse 組織をリセットしようとする場合、非運用環境で発生します。 この問題は、Dataverse の **msdyn_party** テーブルにある当事者 ID の番号順序が原因です。 次の一連のイベントによってエラーが発生します。

1. Dataverse にアカウントが作成されます。 Dataverse では、当事者 ID が **Party-001** で当事者タイプが **組織** の新しい当事者が作成されます。 
2. 新しいアカウントが財務と運用アプリに送信されます。
3. その後、Dataverse 環境がリセットされるか、同じ財務と運用アプリ環境が別の Dataverse 組織に再び接続されます。
4. この時点で Dataverse に新しい連絡先を作成します。 **msdyn_party** の番号順序は、**Party-001** で開始されます。 この時、当事者レコードは、**Party-001** および当事者タイプが **個人** として作成されます。
5. データは財務と運用アプリに同期されます。 財務と運用アプリには既に **Party-001** が **組織** として存在するため、エラーが発生します。

この問題を修正するには、**msdyn_party** テーブルの **msdyn_partynumber** フィールドの自動番号順序を、別の自動番号順序に変更します。

## <a name="error-when-you-run-the-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>当事者郵便番号と当事者電子住所の初期同期を実行する場合のエラー

当事者の郵便番号と当事者の電子住所の初期同期を実行しようとする場合に、"**当事者** 番号が見つかりませんでした" などのエラーが表示される場合があります。

**個人** と **組織** タイプの当事者のみをフィルタ処理するため、財務と運用アプリで **DirPartyCDSEntity** エンティティに範囲が追加されています。 その結果、**CDS 関係者 - msdyn_parties** マッピングの初期同期は、**法人** や **作業単位** など、他のタイプの当事者とは同期しません。 **CDS 関係者の郵便番号 (msdyn_partypostaladdresses)** または **関係者の連絡先 V3 (msdyn_partyelectronicaddresses)** で最初の同期を実行するとき、**当事者** 番号が Dataverse に見つからないなどのエラーが表示される場合があります。

すべてのタイプの関係者が Dataverse に正常に同期するために、財務と運用アプリ エンティティで当事者タイプの範囲を削除しています。 今後の更新については、この記事に戻って確認してください。 

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

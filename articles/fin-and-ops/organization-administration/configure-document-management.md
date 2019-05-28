---
title: ドキュメント管理のコンフィギュレーション
description: このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。
author: ChrisGarty
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6f0552df9e3cce3cd2c44390a5b6feef39c4e1e0
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507508"
---
# <a name="configure-document-management"></a>ドキュメント管理のコンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、添付ファイルおよびレコードのメモを格納するように、ドキュメント管理 (ドキュメント処理) を構成する方法について説明します。 これには、この機能に関連する概念および機能に関する情報が含まれています。

ドキュメントの管理の詳細については、簡単なビデオ [Dynamics 365 for Finance and Operations でのドキュメント管理](https://www.youtube.com/watch?v=p4rl1CkiLN4&feature=youtu.be)をご視聴ください。

## <a name="configure-document-types"></a>ドキュメント タイプのコンフィギュレーション

ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。 各ドキュメント タイプは、固有の場所に格納されることができます。

ドキュメント タイプの既定のセットが用意されています。 これらのドキュメント タイプを使用すると、ファイル、イメージ、メモ、または URL として添付ファイルを分類できます。 **ファイル** および **画像** の既定のドキュメント タイプは、場所として **Azure ストレージ**を使用するよう構成されます。

新しいドキュメント タイプを作成するには、次の手順に従います。

1. **ドキュメント タイプ**ページに移動します。
2. **新規** をクリックします。
3. **タイプ** フィールドに、**SharePoint** または **HR** ドキュメントなどの新しいドキュメント タイプの短縮名を入力します。
4. **名前**フィールドに、**SharePoint ファイル**または **HR ドキュメント**などの長い名前を入力します。
5. **クラス** フィールドで、ドキュメント タイプの動作を定義するクラスを指定します。

    - **ファイルの添付** - ユーザーはファイルを要求されます。
    - **URL の添付** - ユーザーは、`http://www.microsoft.com` のように、**メモ**フィールドに URL を入力することができます。 **添付ファイル** ページの **開く** ボタンをクリックすると [参照] タブに URL が開きます。
    - **簡易メモ** – ユーザーは **メモ** フィールドに簡易メモを追加できます。

6. **クラス** フィールドで**ファイルの添付**を指定した場合、**場所**フィールドで使用する記憶域メカニズムを指定します。
7. **場所** フィールドで **SharePoint** を指定した場合、**SharePoint アドレス** フィールドで Microsoft SharePoint アドレスを指定します。 これを行うには、**編集** ボタン (鉛筆シンボル) をクリックし、**フォルダー選択** ダイアログ ボックスをオンにします。

## <a name="configure-sharepoint-storage"></a>SharePoint 記憶域のコンフィギュレーション

Microsoft SharePoint Online は、ネイティブでサポートされる保存場所の 1 つです。 現在、SharePoint Online だけがサポートされています。 オンプレミス SharePoint (ローカル SharePoint サーバー) のサポートは将来追加される可能性があります。

SharePoint ストレージを使用するには、ドキュメント タイプの**場所**フィールドを **SharePoint** に設定します。 その後、**SharePoint アドレス** フィールドに、有効な SharePoint アドレスを入力します。

SharePoint 記憶域を構成するには、次の手順を実行します。

1. **ドキュメント管理パラメータ**ページに移動します。
2. **SharePoint** タブの**既定の SharePoint サーバー**フィールドで、contosoax7.sharepoint.com など、SharePoint サイトに対して自動的に検出されたホスト名を確認します。 通常、SharePoint ホスト名は tenantname.sharepoint.com の形式で、そのテナントのアカウントは `user1@tenantname.onmicrosoft.com` の形式で示されます。

    既定の SharePoint サーバーが指定されていない場合は、通常、テナントの SharePoint サイトが存在しないか、有効な Microsoft Office 365 ライセンスが現在のユーザー (管理者) に関連付けられていません。

4. オプション: **SharePoint 接続**のテスト をクリックし、指定された SharePoint ホスト名をテストします。
5. オプション: **SharePoint を開く**をクリックし、指定された SharePoint ホスト名をブラウザーで開きます。

### <a name="troubleshooting-sharepoint-communication"></a>SharePoint 通信のトラブルシューティング

SharePoint 通信は、次の条件が満たされた場合にのみ、現在のユーザーに対して機能します。

- Office 365 ライセンスが、ユーザーのアカウントに関連付けられています。
- ユーザーは、外部ユーザーではなくテナントの一般的なユーザーです (別のテナントのユーザーなど)。
- テナント用の SharePoint サイト (たとえば、Contoso.SharePoint.com など) が存在します。

## <a name="configure-file-types"></a>ファイルの種類のコンフィギュレーション

許可されているファイル拡張子のリストを変更することで、ユーザーがレコードに添付できるファイルの種類を制御できます。

ファイル タイプを指定するには、次の手順に従います。

1. **ドキュメント管理パラメータ**ページに移動します。
2. **ファイル タイプ**タブで、既定のファイル タイプを確認します。
3. ユーザーがレコードに添付できないファイル タイプを削除し、ユーザーがレコードに添付できるファイル タイプを追加します。

## <a name="configure-document-preview"></a>ドキュメント プレビューのコンフィギュレーション

添付ファイルのプレビューには、Microsoft Office Online Server で提供される Web アプリ オープン プラットフォーム インターフェイス (WOPI) を使用します。 **ドキュメント管理パラメーター** ページの**全般**タブの **Office Web Apps サーバー** フィールドで、添付ファイルのプレビューに使用する Office Online サーバー インスタンスを指定します。 既定値は [`https://onenote.officeapps.live.com`] です。 この値は、クラウド ベースの WOPI サーバーを指しています。

### <a name="for-an-on-premises-environment"></a>オンプレミス環境について

環境がオンプレミス上にあるとき、既定のクラウド ベースの WOPI サーバーは添付ファイルを読み込んでプレビューを提供することはできません。 プレビューが必要な場合は、[オンプレミス Office Online サーバー インスタンスをインストールし](https://technet.microsoft.com/library/jj219455.aspx)、それを環境内で構成する必要あります。 **Office Web アプリケーション サーバー** フィールドを、インストールされている Office Online Server インスタンスのホスト名に設定し、**保存**をクリックします。

プレビューが必要な場合は、**Office Web アプリケーション サーバー** フィールドを `https://localhost` に設定します。 プレビューは、その後は、エラー メッセージではなく、「プレビューを利用できません」というメッセージを表示します。

## <a name="other-configuration"></a>他のコンフィギュレーション

これらのオプションが使用されることはほとんどありませんが、考慮すべきその他のコンフィギュレーション オプションを次に示します。

- **ドキュメント管理パラメーター**ページの、**一般**タブで、**ドキュメント テーブルの使用**オプションを使用して、**アクティブ ドキュメント テーブル**許可リストを有効にすることができます。 このオプションを**はい**に設定すると、他のすべてのテーブルの添付ファイルが無効になります。 したがって、必要なときにのみこのオプションをオンにしてください。
- **ドキュメント管理パラメーター**ページの、**全般**タブで、**最大ファイル サイズ(単位: メガバイト)** フィールドを使用して、添付ファイルの最大ファイル サイズを設定できます。 ユーザーがファイルを提供する機能は、構成ファイルで環境に対して設定されているファイル サイズ制限でも制限されることに注意してください。 これらの設定ファイルは、クライアント ページから変更することはできません。
- **オプション** ページ (**設定** \> **ユーザー オプション**) では、**基本設定** タブで、**ドキュメント処理の有効化** オプションを使用して、ドキュメント処理を無効にします (ドキュメント管理)。

## <a name="accessing-document-management-attachments"></a>ドキュメント管理添付ファイルへのアクセス 

ドキュメント管理は、データ ソースを含む殆どのフォームのトップにある**添付**ボタン (キーボード ショートカット: **Ctrl**+**Shift**+**A**) として、ユーザーに表示されます。 **添付**ボタンをクリックすると、フォーム上で現在選択されているコントロールのデータ ソースのコンテキストで**添付ファイル** フォームが開きます。

**添付** ボタンには、現在選択されているレコードの添付ファイルの数も表示されるため、ユーザーはそのフォームを開かなくても、現在のレコードに添付ファイルがあるかどうかを確認することができます。 カウントには 0 ～ 9、次に 9+ が表示され、パフォーマンスの影響と大きなカウントの決定と表示の視覚的ノイズが制限されます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-is-the-difference-between-document-handling-and-document-management"></a>ドキュメント処理とドキュメント管理の違いは何ですか。

ドキュメント処理とドキュメント管理の違いはありません。 両方とも同じ機能を示します。 異なるバージョンの製品では、異なる用語が使用されています。

### <a name="what-is-the-difference-between-document-management-and-print-management"></a>ドキュメント処理と印刷管理の違いは何ですか。

ドキュメント管理では、メモ、ドキュメント、および他のファイルを追加し記録できます。

印刷管理では選択したレポートの印刷設定を制御することができます。 印刷設定には、コピー数、印刷先、およびレポートに含めることができる多言語テキストが含まれます。 詳細については、[Document Reporting Services の概要](../../dev-itpro/analytics/document-reporting-services.md) を参照してください。

### <a name="what-is-the-difference-between-document-types-and-file-types"></a>ドキュメント タイプとファイル タイプの違いは何ですか。

ドキュメント タイプは、レコードに添付したドキュメント、または作成するテンプレートを分類するために使用します。 各ドキュメント タイプは、固有の場所に格納されることができます。 ドキュメント タイプのテーブルの名前は DocuType です。

ファイル タイプには、Microsoft Word ドキュメントおよび画像が含まれます。 ファイル タイプは、.txt、.png、.doc、.xlsx、または .pdf などのファイルの拡張子で表されます。

### <a name="does-document-management-integrate-with-office-365"></a>ドキュメント管理は Office 365 と統合されますか。

はい。 SharePoint 記憶域はネイティブでサポートされ、ドキュメント タイプの保管場所として選択できます。 さらに、任意の URL アドレス指定可能なファイルを **URL** ドキュメント タイプ経由で添付できます。

### <a name="how-does-the-default-storage-location-for-document-management-change-in-on-premises-environments"></a>オンプレミス環境では、ドキュメント管理の既定の保管場所はどのように変更されますか？

オンプレミス環境の場合、添付ファイルの Azure Blob ストレージ プロバイダーはファイル フォルダー ストレージ プロバイダーに置き換えられ、添付ファイルはクラウドに格納される代わりにオンプレミスに保存されます。 したがって、添付ファイルの既定の保管場所はファイル フォルダとなります。

### <a name="if-i-accidentally-delete-an-attachment-stored-in-azure-blob-storage-can-it-be-restored"></a>誤ってAzureブロブ ストレージに格納されている添付ファイルを削除した場合、復元できますか。

Azureブロブ ストレージに格納されている添付ファイルが誤って削除された場合は、完全に削除されたことになり、ファイルへの参照情報も削除されてしまうため、復元や修復することができません。

### <a name="is-the-database-information-about-attachments-stored-separately-from-the-attachments-themselves"></a>添付ファイルに関するデータベースの情報は、添付ファイルそのものとは別の場所に保存されていますか？

添付ファイルの情報はDocuRefテーブルおよびDocuViewテーブルに格納されています。 DocuRefテーブルは、主に添付ファイルに関する情報を保持しています。 DocuRefの情報は、DocuViewレコードに関連付けられている情報と連携しています。 DocuRefテーブルは、添付ファイルを保持しています。 ファイルはデータベースの外に保存されるため、バックアップから復元するなどのデータベース上の操作は添付ファイルに関するデータベース情報のみに作用し、添付ファイルそのものには作用しません。
